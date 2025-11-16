## Código fuente

### Método Inicio de Sesión:

```csharp
public LoginViewModel(IAuthService authService)
{
    _authService = authService;
    LoginCommand = new Command(async () => await OnLoginClicked());
}

private async Task OnLoginClicked()
{
    if (IsBusy)
        return;

    IsBusy = true;
    ErrorMessage = string.Empty;

    try
    {
        if (string.IsNullOrWhiteSpace(Username) || string.IsNullOrWhiteSpace(Password))
        {
            ErrorMessage = "Por favor ingrese usuario y contraseña";
            IsBusy = false;
            return;
        }

        var user = await _authService.LoginAsync(Username, Password);
        if (user != null)
        {
            // CAMBIO AQUÍ: Determinar la ruta según el rol
            if (user.Role == "Cocina" || user.Role == "Kitchen")
            {
                // Navegar a la vista de cocina
                await Shell.Current.GoToAsync("//kitchen");
            }
            else
            {
                // Navegar a la vista de mesas (mozo)
                await Shell.Current.GoToAsync("//tables");
            }
        }
        else
        {
            ErrorMessage = "Usuario o contraseña incorrectos";
        }
    }
    catch (Exception ex)
    {
        ErrorMessage = $"Error al iniciar sesión: {ex.Message}";
    }
    finally
    {
        IsBusy = false;
    }
}
```

### Registrar un pedido:

```csharp
private async Task SendToKitchen()
{
    var itemsToOrder = AllMenuItems.Where(i => i.Quantity > 0).ToList();
    if (!itemsToOrder.Any())
    {
        await Shell.Current.DisplayAlert("⚠️ Atención", "No ha seleccionado ningún plato.", "OK");
        return;
    }

    try
    {
        if (_currentOrder == null)
        {
            _currentOrder = await _orderService.CreateOrderAsync(TableId, 1);
        }

        foreach (var item in itemsToOrder)
        {
            var orderItem = new Model.OrderItem
            {
                MenuItemId = item.MenuItemId,
                MenuItemName = item.Name,
                Price = item.Price,
                Quantity = item.Quantity,
                Notes = item.Observation
            };

            await _orderService.AddItemToOrderAsync(_currentOrder.OrderId, orderItem);
        }

        await _orderService.UpdateOrderStatusAsync(_currentOrder.OrderId, Model.OrderStatus.SentToKitchen);
        await _tableService.AssignOrderToTableAsync(TableId, _currentOrder);

        OrderState = OrderState.SentToKitchen;

        await Shell.Current.DisplayAlert("✅ Pedido Enviado", "El pedido ha sido enviado a cocina correctamente.", "OK");
    }
    catch (Exception ex)
    {
        await Shell.Current.DisplayAlert("❌ Error", $"Error al enviar el pedido: {ex.Message}", "OK");
    }
}
```

### Actualizar el estado del pedido:

```csharp
private async Task MarkOrderAsReady(KitchenOrderViewModel order)
{
    if (order == null) return;

    try
    {
        IsBusy = true;

        // Actualizar el estado a "Ready"
        await _orderService.UpdateOrderStatusAsync(order.OrderId, OrderStatus.Ready);

        // Remover de la lista
        PendingOrders.Remove(order);

        await Shell.Current.DisplayAlert("✅ Pedido Listo", $"{order.TableName} está listo para servir.", "OK");
    }
    catch (Exception ex)
    {
        await Shell.Current.DisplayAlert("❌ Error", $"Error al marcar como listo: {ex.Message}", "OK");
    }
    finally
    {
        IsBusy = false;
    }
}
```

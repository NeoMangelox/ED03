## Pseudocódigo de los requisitos de sistema más importantes (Requisitos funcionales mandatorios)

- En esta sección colocarán los pseudocódigos correspondientes a los requisitos funcionales más importantes del software.
- Mínimamente 02 pseudocodigos y máximo 03 pseudoodigos.

* ViewModel de inicio de sesión (Login)
```C#
Clase LoginViewModel
    Variables:
        authService       // Servicio de autenticación
        username           // Texto ingresado por el usuario
        password           // Contraseña ingresada
        errorMessage       // Texto del error actual
        hasError           // Verdadero si hay error
        isBusy             // Verdadero si el sistema está procesando
        LoginCommand        // Acción de iniciar sesión

    Método Constructor(authService)
        this.authService = authService
        LoginCommand = Acción => ejecutar OnLoginClicked()

    Método OnLoginClicked()
        Si isBusy = verdadero entonces
            salir del método
        isBusy = verdadero
        errorMessage = ""
        Si username está vacío O password está vacío entonces
            errorMessage = "Por favor ingrese usuario y contraseña"
            hasError = verdadero
            isBusy = falso
            salir del método
        FinSi
        Intentar:
            usuario = authService.LoginAsync(username, password)
            Si usuario existe entonces
                Navegar a la pantalla "//tables"
            Sino
                errorMessage = "Usuario o contraseña incorrectos"
                hasError = verdadero
            FinSi
        Capturar excepción ex:
            errorMessage = "Error al iniciar sesión: " + ex.mensaje
            hasError = verdadero
        Finalmente:
            isBusy = falso
    FinMétodo
    Evento OnPropertyChanged(propiedad)
        // Notifica a la interfaz que una propiedad cambió
FinClase
```
* ViewModel del módulo de Menú/Pedidos
```C#
Clase MenuViewModel
    Variables privadas:
        menuService
        orderService
        tableService
        isBusy ← falso
        selectedCategory ← ""
        tableId, orderId ← 0
        currentOrder ← nulo
        currentTable ← nulo

    Colecciones públicas:
        MenuItems ← lista vacía
        Categories ← lista vacía

    Propiedades públicas:
        selectedCategory (al cambiar valor → llamar LoadMenuItemsByCategory)
        tableInfo (retorna "Mesa [número]" si hay mesa actual, caso contrario "Mesa desconocida")
        isBusy (notifica cambios a la vista)

    Comandos:
        selectCategoryCommand → ejecuta OnSelectCategory
        addToOrderCommand → ejecuta OnAddToOrder(menuItem)
        viewOrderCommand → ejecuta OnViewOrder
        goBackCommand → ejecuta OnGoBack

    Constructor(menuService, orderService, tableService):
        asigna dependencias a variables
        inicializa colecciones y comandos
        llama LoadCategories()

    Método ApplyQueryAttributes(query):
        obtiene tableId y orderId desde el diccionario de parámetros
        llama LoadTableInfo()
        llama LoadOrderInfo()

    Método LoadTableInfo():
        currentTable ← obtener mesa por id usando tableService
        notificar cambio de propiedad TableInfo

    Método LoadOrderInfo():
        si orderId > 0:
            currentOrder ← obtener orden por id usando orderService

    Método LoadCategories():
        isBusy ← verdadero
        limpiar Categories
        intentar:
            menuItems ← obtener todos los ítems del menú desde menuService
            categories ← categorías únicas de los ítems
            agregar cada categoría a Categories
            si hay categorías:
                selectedCategory ← primera categoría
        capturar error:
            mostrar alerta "Error al cargar las categorías"
        finalmente:
            isBusy ← falso

    Método LoadMenuItemsByCategory():
        isBusy ← verdadero
        limpiar MenuItems
        intentar:
            items ← obtener ítems de menú según categoría seleccionada
            agregar cada item a MenuItems
        capturar error:
            mostrar alerta "Error al cargar los ítems del menú"
        finalmente:
            isBusy ← falso

    Método OnSelectCategory(category):
        selectedCategory ← category

    Método OnAddToOrder(menuItem):
        intentar:
            si currentOrder es nulo:
                userId ← 1  // valor temporal
                crear nueva orden con tableId, userId
                asignar orden a mesa usando tableService

            crear nuevo orderItem con datos de menuItem
            agregar item a la orden usando orderService
            mostrar alerta "Ítem agregado a la orden"
        capturar error:
            mostrar alerta "Error al agregar ítem a la orden"

    Método OnViewOrder():
        si existe currentOrder:
            navegar a vista "orderview" con orderId y tableId
        si no:
            mostrar alerta "No hay una orden activa para esta mesa"

    Método OnGoBack():
        navegar a pantalla anterior
Fin Clase
```

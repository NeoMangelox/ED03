# Principales Reglas de Negocio
Este documento define las principales **reglas de negocio** que deben cumplirse en el sistema POS para un restaurante de atención completa. Estas reglas establecen cómo debe funcionar el sistema más allá de la lógica técnica.

---

## 1. Gestión de Mesas
- Una mesa solo puede estar en uno de los siguientes estados: **disponible, ocupada, cerrada**.
- Una mesa ocupada debe estar siempre asociada a un mozo responsable.
- No se puede cerrar una mesa si aún tiene pedidos pendientes de pago.

---

## 2. Pedidos
- Cada pedido debe estar vinculado a una única mesa y a un mozo que lo registró.
- El pedido debe tener un estado: **pendiente, en preparación, listo, entregado**.
- Los pedidos solo pueden modificarse o anularse si están en estado **pendiente**.
- Cada pedido debe contener al menos un ítem del menú.

---

## 3. Menú y Platos
- Todo plato debe pertenecer a una categoría (ejemplo: entradas, bebidas, postres).
- Los precios de los platos deben ser positivos y no nulos.
- Un plato no puede eliminarse si forma parte de pedidos registrados; en ese caso, solo puede marcarse como **inactivo**.

---

## 4. Pagos
- Una cuenta no puede marcarse como pagada hasta que todos los pedidos de la mesa estén cerrados.
- Los métodos de pago aceptados son **efectivo** y **tarjeta** (otros métodos requieren configuración adicional).
- Se permite dividir la cuenta únicamente en pagos que sumen el monto total de la mesa.

---

## 5. Usuarios y Roles
- Cada usuario debe estar asociado a un rol: **Administrador, Mozo o Cocinero**.
- Solo el **Administrador** puede:
  - Gestionar el menú (CRUD de platos).
  - Crear, editar o eliminar usuarios.
  - Acceder a reportes de ventas.
- Los **Mozos** solo pueden gestionar mesas y pedidos.
- Los **Cocineros** solo pueden visualizar pedidos y actualizar su estado.

---

## 6. Reportes
- El sistema debe permitir generar reportes de:
  - Ventas diarias.
  - Pedidos por mesa.
  - Movimientos de caja.
- Los reportes deben generarse únicamente para fechas válidas (no futuras).

---

## 7. Inventario (opcional)
- Cada plato puede estar vinculado a insumos del stock.
- No puede registrarse un pedido de un plato si los insumos asociados no tienen suficiente cantidad disponible.
- El stock debe actualizarse automáticamente con cada pedido confirmado.

---

## 8. Restricciones Generales
- El sistema debe garantizar que **ninguna transacción quede incompleta** (pedido, pago o cierre de mesa).
- Las operaciones críticas (pagos, modificaciones, anulación de pedidos) deben quedar registradas en un **historial de auditoría**.
- Toda comunicación entre mozo y cocina debe registrarse en tiempo real, evitando duplicación de pedidos.

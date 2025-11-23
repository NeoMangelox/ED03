# Principales Reglas de Negocio

Este documento define las reglas de negocio que guiarán el desarrollo del sistema POS, separando claramente las reglas del **Producto Mínimo Viable (MVP)** de aquellas que corresponden a funcionalidades de **mejoras futuras**.

---

## 1. Reglas de Negocio del Prototipo

Estas son las reglas que rigen el funcionamiento del **entregable final de la versión 1.0**, enfocadas exclusivamente en el flujo central.

### Gestión de Mesas
- Una mesa solo puede estar en uno de dos estados: **Disponible** o **Ocupada**.
- Una mesa cambia de `Disponible` a `Ocupada` cuando el mozo inicia la toma de un pedido.
- Una mesa cambia de `Ocupada` a `Disponible` únicamente al registrar el pago a través de la acción "Pagado".

### Pedidos
- Cada pedido (comanda) debe estar vinculado a una única mesa en estado `Ocupada`.
- Un pedido debe tener al menos un ítem del menú para poder ser enviado a cocina.
- El pedido debe tener uno de dos estados: **Pendiente** (recién enviado por el mozo) o **Listo para entregar** (marcado por cocina).
- No se permite la modificación o anulación de un pedido una vez enviado. En caso de error, se debe anular la comanda completa y crear una nueva.

### Menú y Platos
- El menú es de **solo lectura** para el mozo durante la toma de pedidos.
- Todo plato debe pertenecer a una categoría (ej. Entradas, Principales, Bebidas).
- Los precios de los platos deben ser positivos y no nulos.

### Pagos
- Para una mesa `Ocupada`, se debe poder generar una cuenta que sume el total de los ítems consumidos.
- El sistema no gestiona diferentes métodos de pago. La acción final es un único botón de "Pagado" o "Registrar Pago".
- Al registrar el pago, la mesa asociada cambia automáticamente a estado `Disponible`.

### Restricciones Generales del Flujo
- La comunicación entre la interfaz del mozo y la pantalla de cocina debe ser en tiempo real, sin necesidad de refrescar manualmente.
- El sistema debe evitar la duplicación de pedidos al ser enviados a cocina.
- Las transacciones críticas del flujo (envío de pedido a cocina, marca de pedido como listo, registro de pago) deben ser atómicas y confirmarse para mantener la integridad del sistema.

---

## 2. Reglas de Negocio para Futuras Versiones (Mejoras)

Estas reglas se han identificado como valiosas pero están **explícitamente pospuestas** para futuros incrementos del software, una vez que el flujo central del MVP esté operativo.

### Gestión de Usuarios y Roles
- Cada usuario debe estar asociado a un rol: **Administrador, Mozo o Cocinero**.
- Solo el **Administrador** podrá gestionar el menú, usuarios y acceder a reportes.
- Los **Mozos** solo podrán gestionar mesas y pedidos.
- Los **Cocineros** solo podrán visualizar pedidos y actualizar su estado.

### Modificación y Anulación de Pedidos
- Los pedidos podrán modificarse o anularse si están en estado **pendiente**.
- Se deberá registrar un historial de auditoría para las modificaciones y anulaciones.

### Administración del Menú (CRUD)
- Un plato no puede eliminarse si forma parte de pedidos registrados; en su lugar, deberá marcarse como **inactivo**.
- Solo los usuarios con rol de **Administrador** podrán crear, leer, actualizar y eliminar (CRUD) platos y categorías.

### Pagos Avanzados y Reportes
- Se permitirán múltiples métodos de pago (efectivo, tarjeta, etc.).
- Se permitirá dividir una cuenta en varios pagos.
- El sistema deberá generar reportes de ventas diarias, pedidos por mesa y movimientos de caja para fechas válidas.

### Inventario
- Cada plato podría estar vinculado a insumos del stock.
- No se podrá registrar un pedido si los insumos asociados no tienen stock suficiente.
- El stock debe actualizarse automáticamente con cada pedido confirmado.
## 8. Restricciones Generales
- El sistema debe garantizar que **ninguna transacción quede incompleta** (pedido, pago o cierre de mesa).
- Las operaciones críticas (pagos, modificaciones, anulación de pedidos) deben quedar registradas en un **historial de auditoría**.
- Toda comunicación entre mozo y cocina debe registrarse en tiempo real, evitando duplicación de pedidos.

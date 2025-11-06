
# Introducción

## Contexto
Se plantea el desarrollo de un sistema de Punto de Venta (POS) orientado a restaurantes de atención completa, enfocado en su primera versión en optimizar el flujo operativo central.

## Justificación
La necesidad surge de un problema común en el dominio gastronómico: la coordinación eficiente entre mozos y cocina. Este proceso, cuando se gestiona manualmente, suele provocar errores en la toma de pedidos, demoras en la atención y dificultades en el control del ciclo de vida del pedido en la mesa.

El proyecto busca cubrir esta necesidad general a través de un **Producto Mínimo Viable (MVP)** que resuelva el flujo crítico, sin depender de un cliente particular, ya que cualquier restaurante de atención completa comparte esta problemática fundamental:
- Manejo simplificado de estados de mesas.
- Toma y envío de pedidos a cocina.
- Comunicación básica del estado de los pedidos.
- Generación de cuentas y cierre de mesas.

## Propósito
El propósito es diseñar y desarrollar una aplicación POS que establezca un **flujo central robusto y simplificado** para la operación diaria de restaurantes. Esta primera versión (MVP) se centrará exclusivamente en la dinámica esencial entre mozo, mesa, cocina y pago, creando una base sólida sobre la cual se podrán construir funcionalidades de mejora en futuras iteraciones. La solución representará un aporte al dominio de negocio gastronómico al resolver el núcleo del problema operativo.

## Alcance del Producto Mínimo Viable (MVP)
El entregable final de esta versión se limita estrictamente a las siguientes funcionalidades, consideradas el flujo central e indispensable:
- **Gestión de Mesas (Simplificada):** Implementación de un mapa visual con dos estados: `Disponible` y `Ocupada`. Las acciones son `Abrir Mesa` y `Cerrar Mesa`.
- **Toma y Envío de Pedidos:** Permitir al mozo seleccionar platos de un menú estático para una mesa ocupada, agregar cantidades y una observación, y enviar la comanda a cocina con la acción "Enviar a Cocina".
- **Comunicación con Cocina:** Una vista para cocina que muestre los pedidos con dos estados: `Pendiente` (al ser enviado) y `Listo para entregar` (al ser marcado por cocina).
- **Menú (Solo Lectura):** Visualización de un menú estático (cargado desde un archivo JSON o similar), organizado por categorías con precios.
- **Generación de Cuenta y Cierre:** Capacidad de calcular el total de los consumos de una mesa y registrar un pago simple que cambie el estado de la mesa a `Disponible`.

### Mejoras Futuras (Fuera del Alcance Inicial)
Para mantener el enfoque en el MVP, las siguientes funcionalidades, aunque identificadas como valiosas, se posponen para versiones posteriores:
- **Módulo CRUD de Menú:** Permitir la administración remota de platos, precios y categorías.
- **Reportes de Gestión:** Generación de reportes de ventas, análisis de productos y control de caja.
- **Gestión de Usuarios y Roles:** Implementación de un sistema de login y permisos diferenciados (mozo, cocina, administrador).
- **Modificación/Anulación de Pedidos:** Funcionalidad para editar ítems de una comanda ya enviada.
- **Estados Detallados del Pedido:** Seguimiento individual del estado de cada plato (ej. "en preparación", "listo").
- **Integración de Métodos de Pago:** Soporte para tarjetas de crédito, desglose de impuestos e impresión de tickets.

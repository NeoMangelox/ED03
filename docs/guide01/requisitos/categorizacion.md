# Categorización lógica de requisitos

## 1. Requisitos funcionales mandatorios (MVP)

Estos son los requisitos que definen el **entregable final de la versión 1.0 (MVP)**, tal como se especifica en el documento "El Flujo Central". Son el mínimo indispensable para que el sistema cumpla con su función principal.

- **Gestión de mesas (Simplificada)**: Implementación de un mapa de mesas visual con dos estados mínimos: `Disponible` y `Ocupada`. Las acciones son `Abrir/Marcar mesa como Ocupada` al tomar un pedido y `Cerrar/Marcar mesa como Disponible` al registrar el pago.
- **Toma y envío de pedidos**: El mozo debe poder seleccionar una mesa ocupada, agregar platos (desde un menú de solo lectura), cantidades y una observación, para luego enviar la comanda a cocina mediante la acción "Enviar a Cocina".
- **Comunicación y estados de pedido con cocina**: Crear una vista para cocina que muestre los pedidos enviados. Los pedidos tendrán dos estados unificados: `Pendiente` (aparece al ser enviado) y `Listo para entregar` (marcado por cocina).
- **Menú (Solo Lectura)**: Visualización del menú para que los mozos puedan tomar pedidos. El menú será estático (cargado desde un archivo o hardcodeado), mostrando platos, precios y categorías. No se permite su modificación.
- **Notificación de pedido listo**: La interfaz del mozo debe indicar visualmente (ej. un ícono o notificación) cuando cocina marca un pedido como "Listo para entregar".
- **Generación de cuenta y cierre de mesa**: Para una mesa ocupada, se debe poder calcular y mostrar el total de los platos pedidos. La acción final es un botón de "Registrar Pago y Cerrar Mesa" (ej. "Pagado") que cambia el estado de la mesa a `Disponible`.

---

## 2. Requisitos funcionales de mejora (Futuras Versiones)

Estos requisitos, identificados en el análisis, se posponen deliberadamente para futuras versiones, tal como se indica en la sección "Qué se pospone" y "Qué NO hacer en el MVP" del documento base.

- **Modificación/Anulación de pedidos**: Permitir editar o cancelar ítems de una comanda ya enviada. Para el MVP, se anularía la comanda entera.
- **CRUD de platos, precios y categorías**: Módulo completo para que el administrador pueda crear, leer, actualizar y eliminar información del menú de forma remota.
- **Gestión de usuarios con roles**: Implementación de un sistema de login y roles (mozo, cocina, administrador) con distintos niveles de acceso. Para el MVP, se asume un único rol de "mozo".
- **Reportes básicos**: Generación de reportes de ventas diarias, control de caja y análisis de pedidos para la gestión interna.
- **Estados de pedido detallados por plato**: Seguimiento individual del estado de cada plato (ej. "en preparación", "listo") en lugar de un estado unificado por comanda.
- **Integración con métodos de pago complejos**: Soporte para tarjetas de crédito, desglose de impuestos e impresión de tickets físicos.
- **Integración con impresoras en cocina/barra**: Los pedidos se imprimen automáticamente en las áreas de preparación.
- **División de cuenta entre clientes**: Permite fraccionar una cuenta en varias partes según el consumo.
- **Historial de pedidos por mesa/cliente**: Facilita la identificación de hábitos de consumo o gestión de reclamos.
- **Promociones y descuentos configurables**: Habilita ofertas especiales (combos, happy hour, etc.).
- **Reservas de mesas**: Gestiona anticipadamente la ocupación del restaurante.
- **Modo offline parcial**: Permite seguir operando en caso de caída de la red, sincronizando datos al restablecerse.
- **Soporte multilenguaje para menú**: Útil en zonas turísticas o con clientes extranjeros.
- **Control de insumos y stock**: Da seguimiento a existencias de ingredientes para planificar compras.

---

## 3. Requisitos funcionales sin valor organizacional

No aportan directamente a los objetivos operativos del restaurante y consumen recursos de desarrollo que podrían enfocarse en el flujo central.

- **Gamificación para mozos**: Sistemas de ranking de desempeño, puntos o medallas.
- **Personalización visual excesiva**: Cambios de temas y colores por usuario.
- **Chat interno mozo–cocina**: Redundante si el flujo de estados de los pedidos ya comunica lo necesario.
- **Avatares o stickers en pedidos**: Elementos decorativos sin utilidad práctica para la operación.
- **Integración con redes sociales del restaurante**: No corresponde a la función core de un sistema POS.

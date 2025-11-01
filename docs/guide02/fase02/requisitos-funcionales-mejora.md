## Descripción detallada de requisitos funcionales de mejora del software

Esta parte ya fue trabajada en la sección Requisitos funcionales de mejora en:

[Guía 01 - Categorización lógica de requisitos](../../guide01/requisitos/categorizacion.md#categorizacion-logica-de-requisitos-organizacion-de-los-requisitos-de-usuario).

* **Integración con impresoras en cocina/barra:** Las boletas o facturas de los pedidos se imprimen automáticamente para otorgar un registro
fisico del consumo al cliente.
* **División de cuenta entre clientes:** El sistema permite dividir una cuenta total en varias partes, asignando a cada cliente los platos o
bebidas que consumió. También se pueden realizar divisiones por porcentaje o monto específico. Esta funcionalidad es especialmente útil para
grupos o mesas compartidas, mejorando la experiencia del cliente y simplificando el proceso de cobro al cierre de la mesa.
* **Historial de pedidos por mesa/cliente:** Se mantiene un registro histórico de los pedidos realizados por mesa o cliente frecuente. Esta
información puede consultarse para analizar hábitos de consumo, preferencias y recurrencias, así como para atender reclamos o aclaraciones
sobre pedidos pasados. Además, sirve de base para implementar programas de fidelización o personalización del servicio.
* **Promociones y descuentos configurables:** El sistema ofrece la posibilidad de definir y aplicar promociones especiales, como combos,
descuentos por horario (happy hour), por volumen de compra o por fidelidad del cliente. Los administradores pueden configurar las condiciones
y vigencia de cada promoción, las cuales se aplican automáticamente al tomar pedidos. Esto ayuda a impulsar las ventas y mejorar la gestión
comercial del restaurante.
* **Notificaciones al mozo cuando pedido está listo:** Cuando la cocina o barra marca un pedido como “listo”, el sistema envía una notificación
instantánea al mozo asignado (por ejemplo, mediante una alerta en su dispositivo o terminal). Esto permite que el mozo retire el pedido a tiempo
y lo entregue sin demoras, mejorando la coordinación entre el personal y reduciendo los tiempos de espera del cliente.
* **Reservas de mesas:** Este módulo permite gestionar reservas anticipadas de mesas. El sistema muestra la disponibilidad en un calendario o
plano del local, registrando el nombre del cliente, fecha, hora, cantidad de personas y observaciones. Esto optimiza la planificación de la
ocupación y evita sobrecargas en horas pico.
* **Modo offline parcial:** En caso de caída de la red o desconexión temporal del servidor, el sistema entra en un modo offline parcial,
permitiendo seguir registrando pedidos y operaciones básicas sin interrupción. Una vez que la conexión se restablece, los datos se sincronizan
automáticamente con el servidor central. Este requisito garantiza continuidad operativa, incluso ante fallos de conectividad interna.
* **Soporte multilenguaje para menú:** El sistema incluye la opción de mostrar el menú en diferentes idiomas, como español, inglés o portugués,
entre otros. Los administradores pueden traducir los nombres y descripciones de los platos desde la interfaz de configuración. Esta característica
es ideal para restaurantes en zonas turísticas o con clientela internacional, facilitando la comunicación y mejorando la experiencia del cliente.
* **Control de insumos y stock:** Permite gestionar y monitorear el inventario de ingredientes e insumos utilizados en la preparación de los platos.
Cada vez que se registra un pedido, el sistema descuenta automáticamente las cantidades correspondientes del stock. Además, genera alertas cuando
ciertos productos alcanzan niveles mínimos, ayudando a planificar compras, evitar quiebres de stock y reducir desperdicios.

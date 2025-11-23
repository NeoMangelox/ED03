## Descripción detallada de requisitos funcionales mandatorios del software

Este apartado detalla los requisitos funcionales mandatorios para el desarrollo del sistema POS, enfocándose exclusivamente en el flujo central de operación. Las funcionalidades aquí descritas son las esenciales para validar el modelo de negocio y se basan en la simplificación deliberada de procesos, posponiendo características complejas para futuras versiones.

*   **Gestión de Mesas (Simplificada):**
    Este módulo permite visualizar el estado de las mesas y gestionar su ciclo de vida básico. Para el Prototipo, se implementa un mapa de mesas visual con únicamente dos estados mandatorios:
    *   **Disponible:** La mesa está libre y puede ser asignada a clientes.
    *   **Ocupada:** La mesa tiene un pedido activo.
    Las acciones principales son "Abrir/Marcar mesa como Ocupada" al tomar el primer pedido y "Cerrar/Marcar mesa como Disponible" al registrar el pago.
    *   **Simplificación del Prototipo:** Se pospone el estado "en camino" (pedido en preparación) para simplificar la gestión. El estado del pedido se manejará de forma independiente en el módulo de cocina.

*   **Toma y Envío de Pedidos (El Corazón del Prototipo):**
    El sistema permite que el mozo seleccione una mesa en estado **Ocupada** y registre los platos solicitados a través de una interfaz digital. Esta interfaz debe mostrar el menú (estático para esta versión) y permitir seleccionar ítems, cantidades y añadir una observación simple. La acción clave es el botón **"Enviar a Cocina"**, que notifica automáticamente el pedido al área de preparación.

*   **Comunicación con Cocina y Estados de Pedido (Unificados):**
    Este requisito garantiza que los pedidos enviados por los mozos aparezcan instantáneamente en una vista simple para la cocina. Para el Prototipo, los pedidos tendrán dos estados mínimos:
    *   **Pendiente:** Aparece en la lista de cocina en cuanto el mozo lo envía.
    *   **Listo para entregar:** La cocina marca el pedido completo de una mesa como listo.
    El mozo puede visualizar en su interfaz cuándo un pedido cambia a "Listo para entregar".
    *   **Simplificación del Prototipo:** Se pospone un flujo detallado por plato (ej. "entrada lista, main en preparación"). Para la v1.0, se marca toda la comanda de una mesa como "lista".

*   **Menú (Solo Lectura):**
    El sistema debe mostrar un menú estático para que los mozos puedan tomar los pedidos. Este menú debe incluir los platos, sus precios y estar organizado por categorías (Ej: Entradas, Principales, etc.).
    *   **Simplificación del Prototipo:** No se requiere el módulo CRUD (Crear, Leer, Actualizar, Borrar) para la administración del menú. Para esta versión, el menú puede ser cargado desde un archivo estático (como un JSON) o estar hardcodeado en la aplicación.

*   **Generación de Cuenta y Cierre de Mesa:**
    Cuando una mesa está **Ocupada**, el mozo debe tener una opción para "Ver Cuenta" o "Cerrar Mesa". La funcionalidad mandatoria es:
    *   Calcular y mostrar el total a pagar sumando todos los platos pedidos en esa mesa.
    *   Proveer un botón de **"Registrar Pago y Cerrar Mesa"** que cambie el estado de la mesa a **Disponible**.
    *   **Simplificación del Prototipo:** No se requiere integración con métodos de pago complejos ni desglose de impuestos. Un simple botón que registre el pago como "Pagado" es suficiente para el cierre del ciclo.

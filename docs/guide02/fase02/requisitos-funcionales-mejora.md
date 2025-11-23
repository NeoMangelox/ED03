## Descripción detallada de requisitos funcionales de mejora del software

Este apartado detalla las funcionalidades que constituirán las siguientes iteraciones del software, construidas sobre la base sólida del prototipo final a entregar. Estas mejoras abordan las limitaciones y simplificaciones que se establecieron intencionalmente en la versión 1.0 para priorizar el flujo central de operación. Cada punto describe cómo se expandirá la capacidad del sistema para añadir valor, robustez y funcionalidades de negocio más avanzadas.

*   **CRUD de Platos, Precios y Categorías:**
    *   **Mejora sobre el prototipo:** La versión 1.0 utilizaba un menú estático (hardcodeado o desde un archivo JSON). Esta mejora implementará el módulo completo de Crear, Leer, Actualizar y Eliminar (CRUD) para que el administrador pueda gestionar el menú de forma remota y dinámica. Esto incluye añadir nuevos platos, modificar precios, actualizar descripciones y reorganizar categorías, reflejando los cambios al instante en las interfaces de los mozos.

*   **Modificación de Pedidos:**
    *   **Mejora sobre el prototipo:** El prototipo evitaba esta funcionalidad para simplificar el flujo, requiriendo anular la comanda entera en caso de error. Esta mejora permitirá a los mozos editar o cancelar ítems específicos de un pedido antes de que sea marcado como "Listo" por cocina, ofreciendo la flexibilidad necesaria para corregir errores o cambios del cliente de manera granular y eficiente.

*   **Gestión de Usuarios con Roles:**
    *   **Mejora sobre el prototipo:** El prototipo asumía que todos los usuarios eran "mozos" con los mismos permisos. Esta funcionalidad introducirá un sistema de autenticación (login) y roles diferenciados (ej. Mozo, Cocina, Administrador), cada uno con permisos específicos para garantizar la seguridad y el control de las operaciones, permitiendo que el administrador acceda a configuraciones y reportes, mientras que los demás roles solo ven las interfaces pertinentes a su trabajo.

*   **Generación de Cuenta Detallada y Registro de Pagos:**
    *   **Mejora sobre el prototipo:** El prototipo se limitaba a mostrar un total y un botón de "Pagado". Esta mejora expandirá el cierre de mesa para incluir:
        *   **Desglose de cuenta:** Mostrar un desglose detallado de cada plato, su precio unitario, cantidades e impuestos.
        *   **División de cuenta:** Permitir dividir la cuenta total entre varios clientes, ya sea por platos consumidos o por montos iguales.
        *   **Registro de métodos de pago:** Habilitar el registro de diferentes formas de pago (efectivo, tarjeta, transferencia, etc.).
        *   **Integración con impresoras:** Permitir la impresión física de tickets o facturas para el cliente.

*   **Reportes Básicos:**
    *   **Mejora sobre el prototipo:** El prototipo no incluía funcionalidades de análisis. Esta mejora añadirá un módulo de reportes que permita al administrador analizar las operaciones del restaurante, generando datos automáticos sobre: platos más y menos pedidos, ingresos diarios/semanales, tiempo promedio de atención por mesa, y rendimiento de los mozos. Esto convierte los datos operativos en información estratégica para el negocio.

*   **Mejoras en la Comunicación y Estados:**
    *   **Mejora sobre el prototipo:** El prototipo establecía un flujo de pedido simple (Pendiente -> Listo). Esta mejora puede refinar la comunicación y los estados de dos maneras:
        *   **Notificaciones mejoradas al mozo:** Evolucionar el simple ícono de "Pedido Listo" a notificaciones más robustas (ej. alertas sonoras, vibración en el dispositivo) para asegurar que el mozo no se pierda ninguna señal.
        *   **Flujo detallado por plato:** Permitir que cocina marque el estado de cada plato dentro de una comanda (ej. "Entrada lista", "Principal en preparación"), dando una visión más granular al mozo y al cliente.

*   **Control de Insumos y Stock:**
    *   **Mejora sobre el prototipo:** Esta es una funcionalidad completamente nueva que se integra sobre el flujo existente. Permitirá gestionar el inventario de ingredientes, descontando automáticamente del stock cada vez que se registra un pedido. Generará alertas de stock bajo y facilitará la planificación de compras, conectando directamente las ventas con la operación de cocina y proveedores.

*   **Reservas de Mesas:**
    *   **Mejora sobre el prototipo:** El prototipo se enfocaba en la gestión en tiempo real de las mesas ocupadas. Este módulo añadirá la capacidad de planificar el futuro, permitiendo gestionar reservas anticipadas a través de un calendario que optimice la ocupación y mejore la experiencia del cliente antes de su llegada.

*   **Funcionalidades Adicionales de Valor:**
    *   **Promociones y Descuentos Configurables:** Permitirá definir y aplicar automáticamente descuentos o combos (ej. 2x1, happy hour), una capacidad de negocio que el prototipo simplificado no podía manejar.
    *   **Modo Offline Parcial:** Añadirá robustez al sistema, permitiendo continuar operando (tomar pedidos) en caso de caída de la red, sincronizando los datos una vez que la conexión se restablezca.
    *   **Soporte Multilenguaje para Menú:** Expanderá el alcance del restaurante a clientes internacionales, permitiendo que el menú se muestre en varios idiomas, una mejora sobre el menú estático y monolingüe del prototipo.

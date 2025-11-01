## Descripción detallada de requisitos funcionales mandatorios del software

Este apartado ya fue trabajado en la sección "Requisitos funcionales" de:

[RTM de la Guía 01](../../guide01/requisitos/rtm.md#Especificación-de-requisitos-de-software)

* Gestión de mesas: Este módulo permite abrir, cerrar y asignar mesas a mozos dentro del sistema. Su objetivo es mantener un control
preciso de la ocupación del local en tiempo real, evitando confusiones o duplicaciones. Las mesas se pueden encontrar en 3 estados:
Disponible (mesa sin clientes), en camino (pedido en preparacion), ocupado (mesa con clientes).
* Toma y envío de pedidos por mozo: El sistema permite que el mozo registre los pedidos directamente desde una interfaz digital
(por ejemplo, una tablet o terminal). Cada pedido incluye los platos seleccionados, cantidad, observaciones y número de mesa.
Una vez confirmado, el pedido se envía automáticamente al área de cocina, eliminando la necesidad de notas manuales y reduciendo
errores de comunicación.
* Comunicación en tiempo real con cocina: Este requisito garantiza una sincronización inmediata entre el sistema del mozo y la interfaz
de cocina. En cuanto un pedido es registrado, aparece instantáneamente en la pantalla de cocina con todos los detalles necesarios
(platos, cantidades, comentarios, hora, mesa). De esta forma, el personal de cocina puede comenzar la preparación sin demoras,
mejorando la eficiencia y los tiempos de atención.
* Modificación/anulación de pedidos antes de preparación: Permite al mozo editar o cancelar pedidos mientras aún no han sido
procesados por cocina. Esto otorga flexibilidad ante errores en la toma de pedidos o cambios de decisión del cliente.
* Estados de pedido: Cada pedido pasa por diferentes estados operativos, como pendiente, en preparación o listo para entregar.
Estos estados se actualizan automáticamente conforme el personal de cocina avanza en su trabajo. El mozo puede visualizar estos
estados en su interfaz, lo que le permite saber cuándo retirar un plato y entregarlo al cliente, mejorando la coordinación interna.
* CRUD de platos, precios y categorías: El administrador tiene acceso a un módulo donde puede crear, leer, actualizar y eliminar
(CRUD) los elementos del menú. Esto incluye platos, bebidas, precios, descripciones y categorías (entradas, principales, postres,
etc.). Los cambios se reflejan automáticamente en todas las interfaces del sistema, garantizando que el menú esté siempre actualizado
y evitando inconsistencias.
* Gestión de usuarios: El sistema maneja diferentes roles de usuario (mozo, cocina, administrador), cada uno con niveles de acceso
específicos. Por ejemplo, los mozos pueden tomar pedidos, pero no modificar precios; cocina puede cambiar estados de preparación,
pero no acceder a reportes; y el administrador tiene acceso completo. Esto asegura la seguridad y el control sobre las operaciones
del sistema.
* Generación de cuenta detallada: Cuando los clientes finalizan su consumo, el sistema genera una cuenta detallada por mesa, con el
desglose de platos pedidos, cantidades, precios unitarios, impuestos y total a pagar. La cuenta puede imprimirse o mostrarse en
pantalla. Este proceso minimiza errores manuales y agiliza el cierre de las mesas.
* Registro de pagos: El sistema permite registrar los pagos realizados por los clientes, indicando el método de pago (efectivo,
tarjeta, transferencia, etc.) y el monto recibido.
* Reportes básicos: Incluye un módulo que genera reportes automáticos sobre las operaciones del día: Cantidad de pedidos, ingresos promedios
tiempo de espera promedio, platillos mas pedidos, platillos menos pedidos, etc.

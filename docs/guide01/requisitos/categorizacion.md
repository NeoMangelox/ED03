# Categorización lógica de requisitos
## 1. Requisitos funcionales mandatorios

Son los mínimos indispensables para que el sistema POS cumpla su función.

- **Gestión de mesas**: permite abrir, cerrar y asignar mesas a mozos, manteniendo control sobre la ocupación del local.
- **Toma y envío de pedidos por mozo**: el mozo registra los pedidos en el sistema y estos llegan automáticamente a cocina.
- **Comunicación en tiempo real con cocina**: asegura que los pedidos aparezcan de inmediato en la interfaz de cocina.
- **Modificación/anulación de pedidos antes de preparación**: da flexibilidad si el cliente cambia de opinión o el mozo cometió un error.
- **Estados de pedido**: cada pedido se etiqueta como _pendiente, en preparación o listo_ para que el mozo tenga visibilidad del progreso.
- **CRUD de platos, precios y categorías**: el administrador puede crear, leer, actualizar y eliminar información del menú.
- **Gestión de usuarios**: define roles (mozo, cocina, administrador) con distintos niveles de acceso.
- **Generación de cuenta detallada**: al finalizar, se imprime o muestra la cuenta con el desglose del consumo por mesa.
- **Registro de pagos**: se registran métodos de pago como efectivo, tarjeta u otros.
- **Reportes básicos**: consolida información de ventas diarias, caja y pedidos por mesa para la gestión interna.

---

## 2. Requisitos funcionales de mejora
No son críticos, pero incrementan eficiencia y comodidad en la operación.
- **Integración con impresoras en cocina/barra**: los pedidos se imprimen automáticamente en áreas de preparación.
- **División de cuenta entre clientes**: permite fraccionar una cuenta en varias partes según el consumo.
- **Historial de pedidos por mesa/cliente**: facilita la identificación de hábitos de consumo o reclamos.
- **Promociones y descuentos configurables**: habilita ofertas especiales (combos, happy hour, etc.).
- **Notificaciones al mozo cuando pedido está listo**: mejora la coordinación y reduce tiempos de espera.
- **Reservas de mesas**: gestiona anticipadamente la ocupación del restaurante.
- **Modo offline parcial**: permite seguir operando en caso de caída de la red interna, sincronizando datos cuando se restablezca la conexión.
- **Soporte multilenguaje para menú**: útil en zonas turísticas o con clientes extranjeros.
- **Control de insumos y stock**: da seguimiento a existencias de ingredientes para planificar compras y evitar quiebres de stock.

---

## 3. Requisitos funcionales sin valor organizacional
No aportan directamente a los objetivos del restaurante y consumen recursos de desarrollo.
- **Gamificación para mozos**: ranking de desempeño, puntos o medallas.
- **Personalización visual excesiva**: cambios de temas y colores por usuario.
- **Chat interno mozo–cocina**: redundante si el flujo de pedidos ya está definido.
- **Avatares o stickers en pedidos**: elemento decorativo sin utilidad práctica.
- **Integración con redes sociales del restaurante**: no corresponde a la función de un POS.

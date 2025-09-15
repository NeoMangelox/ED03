# Especificación de requisitos de software

## Requisitos Funcionales
### RF-01: Gestión de Mesas
**Descripción:**  
El sistema debe permitir la apertura, cierre y asignación de mesas a mozos.
### RF-02: Toma y Envío de Pedidos
**Descripción:**  
El mozo registra un pedido en su dispositivo y este debe enviarse en tiempo real a la cocina.
### RF-03: Comunicación en Tiempo Real con Cocina
**Descripción:**  
Los pedidos ingresados deben visualizarse en la pantalla de cocina inmediatamente.  
**Implementación técnica:**  
- Cada pedido se actualiza en la interfaz de cocina sin necesidad de refrescar manualmente.  
### RF-04: Modificación/Anulación de Pedidos
**Descripción:**  
Los pedidos pueden modificarse o anularse siempre que el estado sea *pendiente*.
### RF-05: Estados de Pedido
**Descripción:**  
El sistema debe manejar los estados: *pendiente, en preparación, listo*.
### RF-06: CRUD de Platos, Precios y Categorías
**Descripción:**  
El administrador debe poder crear, leer, actualizar y eliminar platos del menú.
### RF-07: Gestión de Usuarios
**Descripción:**  
El sistema debe diferenciar roles: *Administrador, Mozo, Cocina*.  
### RF-08: Generación de Cuenta Detallada
**Descripción:**  
El sistema debe generar un comprobante con los ítems consumidos, cantidades y subtotales.
### RF-09: Registro de Pagos
**Descripción:**  
El sistema debe registrar pagos en efectivo y tarjeta.
### RF-10: Reportes Básicos
**Descripción:**  
El sistema debe generar reportes de ventas diarias, pedidos por mesa y estado de caja.
## Requisitos No Funcionales
- **Portabilidad:** El sistema debe ejecutarse en Windows 10/11 con .NET MAUI y ser accesible desde tablets Android conectadas a la red local.
- **Mantenibilidad:** El código debe seguir estándares de C# y patrones de diseño (MVVM), facilitando correcciones y mejoras.
- **Usabilidad:** La interfaz debe ser intuitiva, con botones grandes y navegación sencilla para mozos y cocina.
- **Velocidad de procesamiento:** El sistema debe registrar pedidos en < 2 segundos y actualizar en cocina en tiempo real (< 1 segundo de latencia en red local).
- **Restricciones técnicas:**
    - Base de datos MySQL como motor principal.
    - Comunicación en red local (LAN).
    - Dependencia de Visual Studio 2022 como IDE principal.
    - Framework: .NET 7/8 con MAUI.
## Prototipo no funcional
https://www.figma.com/proto/4wBwUvjQrFGwKMhntmZdTj/POS-Restaurante-Proyecto?page-id=0%3A1&node-id=2-4&p=f&viewport=331%2C629%2C0.28&t=jBfD6N3HLExX0O9M-1&scaling=scale-down&content-scaling=fixed

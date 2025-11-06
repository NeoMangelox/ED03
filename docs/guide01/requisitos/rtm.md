# Especificación de requisitos de software

## Requisitos Funcionales (Mandatorios para el MVP)

A continuación se detallan los requisitos funcionales que conforman el **alcance del entregable final de la versión 1.0**, basados en el documento "El Flujo Central".

### RF-01: Gestión de Mesas (Simplificada)
**Descripción:**  
El sistema debe presentar un mapa visual de las mesas del restaurante. Cada mesa debe tener dos estados: `Disponible` y `Ocupada`. El mozo podrá `Abrir/Marcar mesa como Ocupada` al iniciar un pedido y `Cerrar/Marcar mesa como Disponible` al registrar el pago.

### RF-02: Toma y Envío de Pedidos
**Descripción:**  
El mozo debe poder seleccionar una mesa en estado `Ocupada`, agregar platos desde un menú de solo lectura, especificar cantidades y añadir una observación de texto simple. La acción principal es un botón "Enviar a Cocina" que registra la comanda.

### RF-03: Comunicación en Tiempo Real con Cocina
**Descripción:**  
Al ser enviado un pedido (RF-02), este debe visualizarse inmediatamente en una vista dedicada para cocina sin necesidad de refrescar manualmente.  
**Implementación técnica:**  
- La actualización de la interfaz de cocina debe ser automática y en tiempo real.

### RF-04: Estados de Pedido (Unificados)
**Descripción:**  
El sistema debe manejar dos estados para la comanda de una mesa: `Pendiente` (cuando el mozo lo envía) y `Listo para entregar` (cuando cocina lo marca como preparado). No se requiere un estado "en preparación".

### RF-05: Menú de Solo Lectura
**Descripción:**  
El sistema debe mostrar un menú estático para la toma de pedidos. Este menú contendrá platos, precios y estará organizado por categorías (ej. Entradas, Principales). La información del menú no podrá ser modificada a través de la aplicación en esta versión.

### RF-06: Generación de Cuenta y Cierre de Mesa
**Descripción:**  
Para una mesa `Ocupada`, el sistema debe permitir calcular y mostrar el total a pagar sumando todos los platos de su comanda. Debe existir una acción de "Registrar Pago" (ej. un botón "Pagado") que, al ser ejecutada, cambie el estado de la mesa a `Disponible`.

### RF-07: Notificación de Pedido Listo
**Descripción:**  
Cuando cocina marca un pedido como `Listo para entregar` (RF-04), la interfaz del mozo debe actualizar el estado de la mesa correspondiente para indicar visualmente que el pedido está listo para ser servido.

---
## Requisitos No Funcionales
- **Portabilidad:** El sistema debe ejecutarse en Windows 10/11 con .NET MAUI y ser accesible desde tablets Android conectadas a la red local.
- **Mantenibilidad:** El código debe seguir estándares de C# y patrones de diseño (MVVM), facilitando correcciones y mejoras futuras.
- **Usabilidad:** La interfaz debe ser intuitiva, con botones grandes y navegación sencilla para mozos y cocina, minimizando la curva de aprendizaje.
- **Velocidad de procesamiento:** El sistema debe registrar pedidos en < 2 segundos y actualizar la vista de cocina en tiempo real (< 1 segundo de latencia en red local).
- **Restricciones técnicas:**
    - Base de datos MySQL como motor principal.
    - Comunicación en red local (LAN).
    - Dependencia de Visual Studio 2022 como IDE principal.
    - Framework: .NET 7/8 con MAUI.

## Prototipo no funcional
https://www.figma.com/proto/4wBwUvjQrFGwKMhntmZdTj/POS-Restaurante-Proyecto?page-id=0%3A1&node-id=2-4&p=f&viewport=331%2C629%2C0.28&t=jBfD6N3HLExX0O9M-1&scaling=scale-down&content-scaling=fixed

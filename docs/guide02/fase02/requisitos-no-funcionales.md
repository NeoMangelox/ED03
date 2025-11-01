## Descripción detallada de requisitos no funcionales del software

Este apartado ya fue trabajado en la sección "Requisitos no funcionales" de:

[RTM de la Guía 01](../../guide01/requisitos/rtm.md#Especificación-de-requisitos-de-software)

* **Portabilidad:** El sistema debe ser compatible con múltiples plataformas dentro del entorno operativo previsto. En concreto,
deberá ejecutarse correctamente en Windows 10 y Windows 11 mediante el uso del framework .NET MAUI, garantizando una interfaz y
comportamiento consistentes en ambas versiones. Asimismo, debe ser accesible desde tablets Android conectadas a la red local (LAN),
permitiendo que los mozos o personal de atención utilicen la aplicación sin depender de conexión a internet. Esto asegura una
experiencia multiplataforma fluida y facilita la adopción del sistema en distintos dispositivos dentro del restaurante.
* **Mantenibilidad:** El código fuente del sistema debe estar estructurado y documentado siguiendo los estándares de programación en
C# y aplicando el patrón de diseño MVVM (Model-View-ViewModel), propio de aplicaciones en .NET MAUI. Esta práctica garantiza una
separación clara de responsabilidades entre la lógica de negocio, la interfaz y los datos, permitiendo que futuras correcciones,
actualizaciones o ampliaciones del sistema puedan realizarse de forma ágil y con bajo riesgo de introducir errores. Además, se
recomienda el uso de nombres descriptivos, comentarios adecuados y control de versiones (Git) para facilitar la colaboración
entre desarrolladores.
* **Usabilidad:** La interfaz gráfica debe ser intuitiva, clara y accesible para usuarios con distintos niveles de experiencia
tecnológica (mozos, personal de cocina, administradores). Los botones y controles de interacción deben tener tamaño suficiente
para su uso en pantallas táctiles y deben estar organizados de manera lógica, priorizando las funciones más utilizadas. La navegación
debe ser simple y directa, reduciendo la cantidad de pasos necesarios para completar tareas frecuentes (por ejemplo, registrar un
pedido o cambiar su estado). Este requisito busca asegurar una experiencia de usuario fluida, reduciendo errores operativos y
tiempos de capacitación del personal.
* **Velocidad de procesamiento:** El sistema debe garantizar un desempeño óptimo y tiempos de respuesta bajos para mantener
la eficiencia operativa del restaurante.
  * El registro de pedidos por parte del mozo no debe superar los 2 segundos desde la confirmación hasta el almacenamiento en la
base de datos.
  * La actualización de pedidos en la interfaz de cocina debe reflejarse en tiempo real, con una latencia máxima de 1 segundo
dentro de la red local.

  Estos parámetros aseguran que las operaciones se realicen sin retrasos perceptibles, permitiendo una comunicación fluida entre
las áreas y evitando cuellos de botella durante los horarios de alta demanda.
* **Restricciones técnicas:** El desarrollo y despliegue del sistema estarán sujetos a ciertas limitaciones tecnológicas definidas
por el entorno de trabajo:
  * Base de datos: Se utilizará MySQL como motor principal, tanto por su estabilidad como por su compatibilidad con .NET MAUI a
    través de conectores estándar (por ejemplo, MySQL Connector/NET).
  * Comunicación: El sistema operará dentro de una red local (LAN), asegurando la conexión entre terminales de mozos, cocina y
    administración sin depender de internet.
  * Entorno de desarrollo: El proyecto debe desarrollarse en Visual Studio 2022, aprovechando sus herramientas de depuración,
    diseño de interfaces y administración de proyectos MAUI.
  * Framework: Se utilizará .NET 7 o .NET 8 como base tecnológica, garantizando compatibilidad con las últimas versiones del
    framework y aprovechando mejoras en rendimiento, seguridad y soporte multiplataforma.

   Estas restricciones definen el entorno técnico estándar en el que el sistema será diseñado, probado y mantenido, asegurando
 coherencia en la arquitectura y facilidad de soporte a largo plazo.

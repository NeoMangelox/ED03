## Descripción detallada de requisitos no funcionales del software

Este apartado define las cualidades y restricciones técnicas que debe cumplir el software para asegurar que el prototipo sea robusto, eficiente y una base sólida para futuras iteraciones. Estos requisitos son fundamentales para que el flujo central de operación funcione de manera fluida y confiable en el entorno real de un restaurante.

*   **Portabilidad y Entorno Operativo:**
    El prototipo debe operar dentro de un ecosistema tecnológico específico y controlado para garantizar su funcionalidad principal. Se requiere:
    *   **Compatibilidad multiplataforma:** El sistema debe ejecutarse en un PC con Windows 10 o 11 (para la vista de cocina/administración) y en tablets Android (para los mozos), utilizando el framework .NET MAUI. Esto asegura una experiencia consistente en los dispositivos clave del flujo del prototipo.
    *   **Operación en Red Local (LAN):** Es importante que el sistema funcione de forma autónoma dentro de la red local del restaurante, sin requerir conexión a internet. Esto es crucial para la **comunicación en tiempo real** entre la tablet del mozo y la pantalla de cocina, que es el corazón del prototipo.

*   **Mantenibilidad (Cimiento para el Crecimiento):**
    Dado que el prototipo es la base sobre la cual se construirán funcionalidades futuras (CRUD, roles, reportes), la mantenibilidad es un requisito crítico.
    *   **Arquitectura limpia:** El código debe seguir el patrón MVVM (Model-View-ViewModel) y estándares de programación en C#. Esto permite una separación clara entre la interfaz de usuario y la lógica de negocio, facilitando la **incorporación de las mejoras post-prototipo** sin reescribir el sistema.
    *   **Documentación y control de versiones:** El proyecto debe utilizar Git para el control de versiones y contar con una documentación clara que permita a nuevos desarrolladores entender y modificar el código de forma ágil y segura.

*   **Usabilidad (Adopción Rápida y Sin Errores):**
    El éxito del prototipo depende de que el personal lo adopte de inmediato. La interfaz debe ser extremadamente simple e intuitiva para minimizar la curva de aprendizaje y los errores operativos.
    *   **Diseño enfocado en el flujo:** La interfaz debe priorizar las acciones del prototipo: tomar un pedido, enviar a cocina, marcar como listo y cerrar la mesa. Los botones deben ser grandes y claros para su uso en pantallas táctiles, y la navegación debe requerir el mínimo de pasos posibles para completar estas tareas.
    *   **Claridad en los estados:** El mapa de mesas y la lista de pedidos de cocina deben mostrar visualmente los estados (Disponible, Ocupada, Pendiente, Listo) de forma inequívoca para evitar confusiones.

*   **Velocidad de Procesamiento (Fluidez Operativa):**
    Para que el sistema agilice y no entorpezca el servicio, los tiempos de respuesta deben ser casi instantáneos dentro de la red local.
    *   **Registro de pedidos:** La acción de "Enviar a Cocina" debe completarse y reflejarse en la base de datos en **menos de 2 segundos**.
    *   **Comunicación en tiempo real:** La latencia máxima entre que un mozo envía un pedido y este aparece en la pantalla de cocina debe ser de **menos de 1 segundo**.
    Estos parámetros son la base para cumplir la promesa de una comunicación fluida y eficiente, evitando cuellos de botella en horas pico.

*   **Restricciones Técnicas (Stack de Desarrollo del prototipo):**
    El desarrollo del prototipo se ceñirá a un conjunto de tecnologías específicas para asegurar coherencia, eficiencia y soporte.
    *   **Base de datos:** Se utilizará **MySQL** por su fiabilidad y rendimiento en entornos de red local.
    *   **Framework:** Se desarrollará con **.NET 7 o .NET 8** y **.NET MAUI** para cumplir con los requisitos de portabilidad.
    *   **Entorno de desarrollo:** El proyecto se gestionará principalmente con **Visual Studio 2022**.
    Estas restricciones definen la caja de herramientas técnica para construir el prototipo de manera estandarizada y efectiva.

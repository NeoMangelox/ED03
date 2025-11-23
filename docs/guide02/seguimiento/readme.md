## Seguimiento

En esta sección se presenta el seguimiento de la planificación del proyecto de prototipo de software. Se detalla la ejecución real de las actividades, las cuales concluyeron el 24 de noviembre de 2025, y se realiza una evaluación comparativa entre la planificación inicial y el resultado final del proyecto.

### Plan del Proyecto: Versión Programada vs. Versión Real

A continuación, se presenta una tabla que compara las fechas y el estado de las actividades planificadas inicialmente con la ejecución real, reflejando la decisión clave de modificar el alcance del proyecto durante la fase de implementación.

| ID | Actividad / Tarea | Planificación Inicial (Programado) | Ejecución Real (Real) | Estado Final | Observaciones del Desvío |
|:---:|:---|:---|:---|:---|:---|
| 1 | **Proyecto POS Restaurante** | 25/08/25 - 24/11/25 | 25/08/25 - 24/11/25 | **Completado** | El proyecto culminó en la fecha prevista, pero con un alcance reducido. |
| 2 | **Análisis de requisitos** | 25/08/25 - 17/09/25 | 25/08/25 - 17/09/25 | **Completado** | El análisis inicial cubría los 3 roles. La validación posterior confirmó la eliminación del rol Administrador. |
| 3 | Recopilación de requisitos | 25/08/25 - 08/09/25 | 25/08/25 - 08/09/25 | Completado | Se recopilaron requisitos para los 3 roles iniciales. |
| 4 | Documentación de casos de uso | 09/09/25 - 17/09/25 | 09/09/25 - 17/09/25 | **Completado (Modificado)** | Se documentaron inicialmente todos los casos de uso. Los del administrador se archivaron. |
| 5 | Validación de requisitos | 18/09/25 - 26/09/25 | 18/09/25 - 26/09/25 | **Completado (Modificado)** | Se validó el nuevo alcance reducido (Mozo y Cocina) como viable para el tiempo restante. |
| 6 | **Diseño del sistema** | 29/09/25 - 07/10/25 | 29/09/25 - 07/10/25 | **Completado (Modificado)** | Se eliminó el diseño de la base de datos y las interfaces para la gestión de usuarios y métricas. |
| 7 | Modelo de datos (ERD) | 29/09/25 - 01/10/25 | 29/09/25 - 01/10/25 | **Completado (Modificado)** | El modelo se simplificó, eliminando tablas relacionadas con usuarios y configuraciones administrativas. |
| 8 | Diseño de interfaces | 02/10/25 - 07/10/25 | 02/10/25 - 07/10/25 | **Completado (Modificado)** | Se diseñaron únicamente las interfaces para el Mozo y la Cocina. |
| 9 | **Implementación** | 08/10/25 - 14/11/25 | 08/10/25 - 14/11/25 | **Completado (Con cambios)** | El esfuerzo se concentró exclusivamente en el flujo Mozo-Cocina. |
| 10 | Desarrollo Backend | 08/10/25 - 05/11/25 | 08/10/25 - 05/11/25 | **Completado (Reducido)** | No se desarrollaron los endpoints para creación de usuarios, edición de menú ni generación de métricas. |
| 11 | Desarrollo Frontend | 08/10/25 - 05/11/25 | 08/10/25 - 05/11/25 | **Completado (Reducido)** | No se desarrolló el panel de administración ni sus funcionalidades asociadas. |
| 12 | Integración Backend-Frontend | 06/11/25 - 14/11/25 | 06/11/25 - 14/11/25 | **Completado** | La integración fue más simple al no incluir el módulo de administrador. |
| 13 | **Pruebas** | 08/10/25 - 14/11/25 | 08/10/25 - 14/11/25 | **Completado (Enfoque reducido)** | Los planes de prueba se actualizaron para validar únicamente el flujo de pedido entre Mozo y Cocina. |
| 14 | **Entrega Final** | 17/11/25 - 24/11/25 | 17/11/25 - 24/11/25 | **Completado** | Se entregó un prototipo funcional con el alcance reducido. |
| 15 | Documentación final | 17/11/25 - 24/11/25 | 17/11/25 - 24/11/25 | **Completado** | La documentación refleja el estado final del proyecto, explicando la reducción de alcance. |

---

### Resumen y Análisis Comparativo

Tras una evaluación detallada comparando la versión **programada** con la **real**, el equipo de desarrollo (ED) ha identificado los siguientes aspectos de relevancia:

1.  **Reducción de Alcance como Decisión Crítica:** El desvío más importante del plan fue la modificación de los requisitos a mitad de la fase de implementación. El plan original contemplaba un sistema con tres roles (Administrador, Mozo, Cocina) y funcionalidades de gestión (creación de usuarios, edición dinámica de menú, visualización de métricas). La versión final se centró exclusivamente en el flujo operativo core (Mozo-Cocina), eliminando por completo el rol y las funciones de administrador.

2.  **Causa Principal: Estimación Inicial Optimista:** La razón fundamental de este cambio fue la constatación, durante el desarrollo, de que la ambición del proyecto inicial superaba la capacidad de ejecución del equipo en el tiempo estipulado. El plan original era poco realista, y continuar con él habría comprometido gravemente la calidad o incluso la entrega de un prototipo funcional.

3.  **Impacto en el Resultado Final:** La decisión tuvo un impacto dual. Por un lado, implicó la **pérdida de funcionalidades de alto valor** para el posible cliente dueño del restaurante, que no fueron incluidas en el prototipo entregado. Por otro lado, fue una medida de **mitigación de riesgos indispensable** que permitió asegurar la entrega de un producto funcional, robusto y que demostraba con éxito el proceso de negocio principal para el cual fue concebido.

4.  **Lección Aprendida sobre Planificación Ágil:** Esta experiencia destaca la importancia de la flexibilidad y la capacidad de adaptación en la gestión de proyectos. Si bien la planificación inicial sirve como una hoja de ruta, es fundamental estar dispuesto a reevaluar el alcance basándose en el progreso real. Adoptar un enfoque de **Producto Mínimo Viable (MVP)** desde el inicio habría permitido enfocar los esfuerzos en el flujo Mozo-Cocina desde el principio, considerando las funciones administrativas como una segunda fase o futuras ampliaciones, optimizando así el uso de los recursos y el tiempo.

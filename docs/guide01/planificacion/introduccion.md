# Introducción a la Planificación del Proyecto

## Resumen
El presente proyecto consiste en el desarrollo de una aplicación de Punto de Venta (POS) para restaurantes de atención completa, enfocada en su primera versión en la ejecución de su **flujo central operativo**. El sistema busca resolver el problema crítico de la comunicación entre mozos y cocina, el control del ciclo de vida de la mesa y el pedido, y el cierre de cuentas de forma simplificada. La solución no está dirigida a un cliente particular, sino al dominio general del sector gastronómico, donde estos problemas son recurrentes. Funcionalidades como reportes avanzados o administración de menús se consideran **mejoras futuras**.

## Descripción
El proyecto plantea la implementación de un software instalado en una computadora local que servirá como servidor de base de datos, conectado a dispositivos móviles o terminales utilizados por mozos y cocina. El **alcance del Prototipo** se limita a las siguientes funcionalidades principales:
- **Gestión simplificada de mesas** con dos estados: `Disponible` y `Ocupada`.
- **Toma y envío de pedidos** desde un menú de solo lectura.
- **Comunicación en tiempo real** entre el mozo y la cocina, con estados de pedido `Pendiente` y `Listo para entregar`.
- **Generación de cuenta simple** y registro de pago para el cierre de mesa.

Funcionalidades como el control de stock, reservas o reportes administrativos están documentadas en la hoja de ruta para futuras versiones, pero quedan **excluidas del entregable inicial**.

## Objetivos
- **General**: Desarrollar un sistema POS que establezca un **flujo central robusto y eficiente** para restaurantes de atención completa, sentando las bases para una solución completa y escalable.
- **Específicos (Prototipo)**:
  - Implementar un módulo de **gestión de mesas simplificada**.
  - Incorporar la **toma y envío de pedidos** con comunicación en tiempo real a cocina.
  - Facilitar la **generación de cuentas y el registro de un pago simple** para liberar mesas.
  - Establecer una arquitectura de software modular que permita incorporar **mejoras futuras** (CRUD de menú, reportes, gestión de usuarios) de forma incremental.

## Presupuesto
El proyecto considera un presupuesto estimado para cubrir el desarrollo del **alcance del Prototipo**:
- Desarrollo de software para las funcionalidades del flujo central.
- Infraestructura mínima (servidor local, tablets o terminales para pruebas).
- Capacitación básica del personal en el uso del flujo central.
El costo detallado será ajustado en función de las tecnologías seleccionadas y el alcance final definido para esta primera versión.

## Tiempo
Se estima un tiempo de **13 semanas** para el desarrollo y entrega del **Prototipo**, dividido en:
1.  **Análisis y diseño (enfocado en Prototipo)**: 4 semanas.
2.  **Desarrollo e integración (flujo central)**: 5 semanas.
3.  **Pruebas y validación (del Prototipo)**: 2 semanas.
4.  **Entrega del Prototipo + documentación final**: 1 semana.

## Limitaciones
- Dependencia de la estabilidad de la red local para el funcionamiento en tiempo real.
- Posible necesidad de hardware adicional según el tamaño del restaurante.
- El **alcance inicial (Prototipo) no incluye funcionalidades avanzadas** como reportes de ventas, gestión de usuarios con roles, modificación de pedidos o control de stock, las cuales están planificadas como mejoras futuras.
- Falta de integración inicial con facturación electrónica o sistemas de pago externos, que podrían ser requeridos en algunos contextos regulatorios.

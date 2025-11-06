# Validación de Requisitos de Software

La siguiente matriz valida los requisitos funcionales separándolos en dos grupos claros: los **requisitos mandatorios para el Producto Mínimo Viable (MVP)**, cuyo alcance está definido por el documento "El Flujo Central", y los **requisitos de mejora**, que han sido validados como valiosos pero pospuestos para futuras versiones.

## Criterios de validación
- **AD**: Alineación con el dominio gastronómico (¿es útil en un restaurante de atención completa?).
- **FT**: Factibilidad técnica (¿el equipo puede implementarlo con C# MAUI + MySQL en el plazo?).
- **RO**: Relevancia organizacional (¿aporta valor directo al *flujo central* del restaurante?).
- **CL**: Claridad (¿el requisito está bien definido y no es ambiguo?).

## Matriz de validación

### Requisitos del MVP (Mandatorios para la Versión 1.0)
Estos requisitos han sido validados como el núcleo indispensable y serán el entregable final de la primera versión.

| ID | Requisito | AD | FT | RO | CL | Resultado |
|---|---|---|---|---|---|---|
| MVP-RF-01 | Gestión de Mesas (Simplificada) | ✔️ | ✔️ | ✔️ | ✔️ | **Válido para MVP** |
| MVP-RF-02 | Toma y Envío de Pedidos | ✔️ | ✔️ | ✔️ | ✔️ | **Válido para MVP** |
| MVP-RF-03 | Comunicación en Tiempo Real con Cocina | ✔️ | ✔️ | ✔️ | ✔️ | **Válido para MVP** |
| MVP-RF-04 | Estados de Pedido (Pendiente y Listo) | ✔️ | ✔️ | ✔️ | ✔️ | **Válido para MVP** |
| MVP-RF-05 | Menú (Solo Lectura) | ✔️ | ✔️ | ✔️ | ✔️ | **Válido para MVP** |
| MVP-RF-06 | Notificación de Pedido Listo al Mozo | ✔️ | ✔️ | ✔️ | ✔️ | **Válido para MVP** |
| MVP-RF-07 | Generación de Cuenta y Cierre de Mesa | ✔️ | ✔️ | ✔️ | ✔️ | **Válido para MVP** |

---

### Requisitos de Mejora (Futuras Versiones)
Estos requisitos han sido validados como factibles y útiles, pero **quedan explícitamente excluidos del alcance del MVP** para garantizar el enfoque en el flujo central.

| ID | Requisito | AD | FT | RO | CL | Resultado |
|---|---|---|---|---|---|---|
| RF-04 | Modificación/anulación de pedidos | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |
| RF-05 | Estados de pedido (detallados) | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |
| RF-06 | CRUD de platos, precios y categorías | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |
| RF-07 | Gestión de usuarios y roles | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |
| RF-08 | Generación de cuenta detallada (impresión) | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |
| RF-09 | Registro de pagos (múltiples métodos) | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |
| RF-10 | Reportes básicos | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |
| RF-11 | Integración con impresoras | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |
| RF-12 | División de cuenta | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |
| RF-13 | Historial de pedidos | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |
| RF-14 | Promociones y descuentos | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |
| RF-16 | Reservas de mesas | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |
| RF-17 | Modo offline parcial | ✔️ | ⚠️ | ⚠️ | ✔️ | **Postergado (Alto riesgo técnico)** |
| RF-18 | Soporte multilenguaje | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado (Baja prioridad)** |
| RF-19 | Control de insumos y stock | ✔️ | ✔️ | ⚠️ | ✔️ | **Postergado** |

## Observaciones
- Los requisitos **MVP-RF-01 a MVP-RF-07** han sido validados como críticos y suficientes para construir el flujo central operativo. Su relevancia organizacional (RO) es máxima, ya que resuelven el problema principal de coordinación entre mozo y cocina.
- Los requisitos marcados como **Postergado** (RF-04 a RF-19), aunque factibles y alineados con el dominio, tienen una relevancia organizacional secundaria para la *primera versión*. Aportan valor, pero no son indispensables para que el restaurante opere digitalmente. Se han documentado como el backlog para futuros incrementos.
- **RF-17 (Modo offline)** presenta un riesgo técnico alto y su complejidad podría desviar recursos del núcleo del MVP, por lo que su prioridad es baja.
- **RF-18 (Soporte multilenguaje)** tiene un valor dependiente del contexto, por lo que se considera de baja prioridad general.

## Conclusión
El sistema se desarrollará **exclusivamente** con los requisitos validados para el MVP (MVP-RF-01 a MVP-RF-07). Este alcance es claro, factible y está enfocado en entregar valor de forma rápida.

Los requisitos clasificados como "Postergado" conforman la hoja de ruta para las versiones 2.0 y posteriores. Su implementación se evaluará de forma incremental una vez que el flujo central esté establecido y en operación.

# Validación de Requisitos de Software

La siguiente matriz valida los requisitos funcionales **mandatorios** y **de mejora** según criterios objetivos, considerando que no existe un cliente específico.  

## Criterios de validación
- **AD**: Alineación con el dominio gastronómico (¿es útil en un restaurante de atención completa?).  
- **FT**: Factibilidad técnica (¿el equipo puede implementarlo con C# MAUI + MySQL en el plazo?).  
- **RO**: Relevancia organizacional (¿aporta valor directo a la operación del restaurante?).  
- **CL**: Claridad (¿el requisito está bien definido y no es ambiguo?).  

## Matriz de validación

| ID    | Requisito                                    | AD | FT | RO | CL | Resultado |
|-------|----------------------------------------------|----|----|----|----|-----------|
| RF-01 | Gestión de mesas                             | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-02 | Toma y envío de pedidos                      | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-03 | Comunicación en tiempo real con cocina       | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-04 | Modificación/anulación de pedidos            | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-05 | Estados de pedido                            | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-06 | CRUD de platos, precios y categorías         | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-07 | Gestión de usuarios                          | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-08 | Generación de cuenta detallada               | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-09 | Registro de pagos                            | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-10 | Reportes básicos                             | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-11 | Integración con impresoras                   | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-12 | División de cuenta                           | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-13 | Historial de pedidos                         | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-14 | Promociones y descuentos                     | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-15 | Notificaciones al mozo                       | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-16 | Reservas de mesas                            | ✔️ | ✔️ | ✔️ | ✔️ | Válido |
| RF-17 | Modo offline parcial                         | ✔️ | ⚠️ | ✔️ | ✔️ | Válido con riesgo (sincronización compleja) |
| RF-18 | Soporte multilenguaje                        | ✔️ | ✔️ | ⚠️ | ✔️ | Opcional (valor limitado según contexto) |
| RF-19 | Control de insumos y stock                   | ✔️ | ✔️ | ✔️ | ✔️ | Válido |

## Observaciones
- Todos los requisitos **mandatorios (RF-01 a RF-10)** son **válidos y críticos**.  
- Los requisitos de mejora **RF-11 a RF-19** son factibles, pero algunos presentan matices:  
  - **RF-17 (Modo offline)**: técnicamente complejo en un equipo pequeño, requiere análisis de costos y tiempo.  
  - **RF-18 (Multilenguaje)**: útil solo en contextos turísticos, se clasifica como opcional.  

## Conclusión
El sistema puede implementarse con los requisitos validados. Para reducir riesgos, se recomienda priorizar los **mandatorios** en la primera versión e implementar los de **mejora** de forma incremental según disponibilidad de tiempo y recursos.  

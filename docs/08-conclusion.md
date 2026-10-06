# Conclusiones

## Conclusiones y recomendaciones

La entrega reúne el análisis del problema, los requisitos y el diseño estratégico de Intiva, junto con el avance de UX documentado para TP1. Las conclusiones distinguen lo diseñado de los resultados que todavía requieren implementación y validación.

### Sobre el Capítulo I: Introducción

- Las 5W y 2H y el diagrama de Ishikawa organizan posibles causas de las dificultades de gestión financiera. Las fuentes consultadas permiten contextualizar el problema, pero no prueban que la solución propuesta produzca mejoras en los usuarios.
- Lean UX define hipótesis y metas de negocio. Los incrementos de retención y margen, los 500 grupos activos y el CSAT del 75% son objetivos propuestos; necesitan una línea base e instrumentos de medición.
- Los segmentos se distinguen por su responsabilidad en las finanzas personales y del hogar. Los datos por edad del INEI contextualizan el acceso a cuentas, sin demostrar por sí solos el rol financiero de una persona.

### Sobre el Capítulo II: Requirements Elicitation & Analysis

- Las seis entrevistas registran necesidades de facilidad de uso, seguimiento de gastos, privacidad y recordatorios. Se emplean para orientar el diseño, sin generalizar sus hallazgos a toda la población.
- Los porcentajes de los gráficos heredados no tienen una matriz de respuestas que permita verificar su base de cálculo. El análisis mantiene una lectura cualitativa hasta conciliar esos datos.
- La comparación de Fintonic, Monefy y Plum orienta el posicionamiento de Intiva hacia la gestión personal y familiar. No demuestra exclusividad ni valida una ventaja competitiva en el mercado.

### Sobre el Capítulo III: Requirements Specification

- El alcance incorpora US 001 a US 033 y diez épicas. US 032 establece una captura de gastos pendiente de confirmación; US 033 define aceptación, corrección y confirmación de la categoría Otros ante baja confianza.
- TS 023 mantiene el registro manual cuando se deniega o revoca el acceso a notificaciones. TS 024 propone orquestación con n8n y un intento de envío de respaldo por FCM cuando el flujo no responde.
- Los criterios de aceptación permiten preparar pruebas funcionales. Describir un escenario esperado no acredita que ya haya sido implementado ni que la prueba haya pasado.

### Sobre el Capítulo IV: Strategic-Level Software Design

- El diseño conserva un monolito modular con ocho módulos de dominio en la base de referencia. Subscriptions se registra como contexto previsto. Los bounded contexts internos no equivalen a microservicios desplegados por separado.
- La inspección de la revisión 3cd9d92 de `intiva-api-platform` confirma el acceso directo de Analytics a repositorios de Finances y Savings. Esa dependencia se mantiene como deuda de diseño.
- Los listeners de eventos de la base se ejecutan en proceso. No se encontró una configuración asíncrona que permita afirmar que están fuera de la operación o de su transacción. AD-07 requiere concretar esa separación antes de atribuirle mejoras de latencia.
- La captura pendiente, el clasificador y n8n son ampliaciones propuestas para TP1. La confianza de clasificación, el comportamiento ante errores y los tiempos de respuesta deberán evaluarse en la implementación.

### Sobre el Capítulo VI: Solution UX Design

- El capítulo contiene guías de estilo y arquitectura de información, así como la landing adaptada, sus wireframes para escritorio y móvil, doce wireframes de aplicación y tres wireflows elaborados para TP1.
- Las pantallas representan permiso opcional, revisión del gasto, corrección de categoría, descarte y continuidad manual. La trazabilidad permite relacionar esos estados con US 030, US 032, US 033, TS 023 y TS 024.
- Las nueve imágenes y los frames editables de Figma evidencian el diseño. Los montos y porcentajes mostrados son ejemplos; no representan precisión del modelo ni resultados de pruebas con usuarios.

### Recomendaciones

- Completar el diseño táctico del Capítulo V y las secciones restantes de mock-ups y prototipado. El Capítulo VII aún no contiene evidencias de implementación, pruebas, validación o despliegue de la entrega actual.
- Conciliar la matriz de respuestas de las entrevistas, los precios y datos del equipo de la landing y las versiones del stack con sus fuentes correspondientes.
- Actualizar los diagramas gráficos de arquitectura para incorporar el proveedor de clasificación y n8n, manteniendo la distinción entre módulos internos y unidades desplegables.
- Probar la confirmación y el descarte sin efectos anticipados sobre el saldo, los permisos revocados, los formatos desconocidos, la baja confianza y la indisponibilidad de n8n o del proveedor de IA.
- Definir el cálculo de confianza y contrastar las sugerencias con casos del dominio. Verificar también autorización entre grupos, ejecución de listeners y respuestas del envío de notificaciones.
- Validar la facilidad de uso con personas de ambos segmentos antes de concluir que el producto reduce el esfuerzo de registro o mejora la coordinación familiar.

## Video About-the-Team

[Enlace al video de presentación del equipo](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202319950_upc_edu_pe/IQB_Q8u14DyQT4TXefm7wQfSAakkU-BGVGYdRbP-bV8M77M?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=P0yw1r)

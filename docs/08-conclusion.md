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

- El alcance incorpora US 001 a US 034 y once épicas. US 032 exige aprobación unánime del fondo familiar, US 033 permite aceptar o corregir categorías IA y US 034 define asistencia para gastos hormiga y metas.
- TS 023 define autorización, unanimidad y conciliación del smart contract; TS 024 restringe datos y valida respuestas del adaptador de IA. Las notificaciones habituales conservan FCM (TS 017).
- Los criterios de aceptación permiten preparar pruebas funcionales. Describir un escenario esperado no acredita que ya haya sido implementado ni que la prueba haya pasado.

### Sobre el Capítulo IV: Strategic-Level Software Design

- El capítulo IV propone un monolito modular y describe los contextos que organizan el dominio. Subscriptions se registra como contexto previsto en el diseño estratégico.
- La clasificación, la asistencia IA y la aprobación por contrato son propuestas de TP1. La calidad de las respuestas, la red, las firmas y la confirmación deben validarse en la implementación.

### Sobre el Capítulo VI: Solution UX Design

- El capítulo contiene guías de estilo y arquitectura de información, así como la landing adaptada, sus wireframes para escritorio y móvil, doce wireframes de aplicación y tres wireflows elaborados para TP1.
- Las pantallas representan categorización, asistencia financiera, propuestas, aprobación unánime y estados de confirmación, rechazo y error. Se relacionan con US 032, US 033, US 034, TS 023 y TS 024.
- Las imágenes y composiciones vectoriales de Figma documentan el diseño corregido. Sus montos son ilustrativos; no representan precisión de IA ni contratos desplegados.

### Recomendaciones

- Completar el diseño táctico del Capítulo V y las secciones restantes de mock-ups y prototipado. El Capítulo VII aún no contiene evidencias de implementación, pruebas, validación o despliegue de la entrega actual.
- Conciliar la matriz de respuestas de las entrevistas, los precios y datos del equipo de la landing y las versiones del stack con sus fuentes correspondientes.
- Extender los diagramas estratégicos con los adaptadores de IA y blockchain, manteniendo la distinción entre módulos y servicios externos.
- Probar unanimidad, rechazo, votos duplicados o no autorizados, cambios de propuesta y fallos de red, sin débitos anticipados ni duplicados.
- Evaluar la categorización y las recomendaciones con casos del dominio, sin presentar confianza como precisión medida. Verificar continuidad manual e información mínima autorizada.
- Validar la facilidad de uso con personas de ambos segmentos antes de concluir que el producto reduce el esfuerzo de registro o mejora la coordinación familiar.

## Video About-the-Team

[Enlace al video de presentación del equipo](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202319950_upc_edu_pe/IQB_Q8u14DyQT4TXefm7wQfSAakkU-BGVGYdRbP-bV8M77M?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=P0yw1r)

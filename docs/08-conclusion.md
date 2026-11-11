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

- EP 011 reúne la planificación financiera. US 032 cubre proyección, edición y aprobación; US 035 cubre seguimiento y avisos en la segunda etapa. US 033 y US 034 conservan categorización y asistencia.
- TS 023 valida titularidad y versión y evita duplicar cambios al aplicar el plan; TS 024 valida las respuestas de IA. FCM conserva el canal push (TS 017).
- Los criterios de aceptación permiten preparar pruebas funcionales. Describir un escenario esperado no acredita que ya haya sido implementado ni que la prueba haya pasado.

### Sobre el Capítulo IV: Strategic-Level Software Design

- El capítulo IV propone un monolito modular y describe los contextos que organizan el dominio. Subscriptions se registra como contexto previsto en el diseño estratégico.

### Sobre el Capítulo V: Tactical-Level Software Design

- El diseño táctico documenta las cuatro capas de ocho bounded contexts, junto con diagramas de componentes, clases y base de datos. El plan separa la propuesta editable de la ejecución autorizada y conserva el resultado de cada acción.
- La categorización y el asistente IA se integran mediante puertos y adaptadores; las recomendaciones no ejecutan gastos ni modifican metas. Communications conserva el envío directo de notificaciones por FCM.

### Sobre el Capítulo VI: Solution UX Design

- El capítulo contiene guías de estilo y arquitectura de información, así como la landing adaptada, sus wireframes para escritorio y móvil, doce wireframes de aplicación y tres wireflows elaborados para TP1.
- Las pantallas muestran categorización, asistencia y planificación: proyección, borrador, aprobación, aplicación y error.
- Las imágenes y composiciones vectoriales de Figma documentan el diseño corregido. Sus montos son ilustrativos; no representan precisión de IA ni integraciones desplegadas.

### TP1: Conclusiones del equipo

El equipo consolidó el diseño táctico y la experiencia de usuario de Intiva, relacionando los requisitos del proyecto con las capas del software, la organización de la información y las pantallas de la solución. Los aportes de los cuatro integrantes permiten revisar el comportamiento esperado de IA agéntica antes de su implementación.

**Leonardo Solis — Capítulo V.** El diseño de las capas de dominio, interfaz, aplicación e infraestructura permite identificar dónde se aplican las reglas de negocio y dónde se resuelven las integraciones externas. Los diagramas de componentes, clases y base de datos ofrecen una referencia para implementar cada bounded context. Separar el borrador del plan aprobado protege el consentimiento y evita repetir acciones.

**Camila Loli — Secciones 6.1 y 6.2.** Las guías de estilo y la arquitectura de información establecen criterios comunes para la presentación de Intiva en web y móvil. Las etiquetas y la navegación deben ayudar a distinguir una sugerencia de IA, una propuesta pendiente y un gasto validado. La consistencia del diseño deberá contrastarse con pruebas de comprensión y uso en ambos segmentos de usuarios.


**Omar Rivera — Secciones 6.4.3 y 6.4.4.** Los mock-ups y los user flows permiten revisar la presentación de las pantallas y su relación con los objetivos del usuario. La correspondencia con los wireflows ayuda a mantener las mismas acciones y condiciones en el diseño visual. Estos materiales sirven como base para conectar el prototipo y evaluar las tareas de registro, consulta y aprobación familiar.

**Conclusión conjunta.** El TP1 establece una base de diseño compartida para la implementación de Intiva. La siguiente etapa requiere comprobar la calidad de las respuestas de IA, la aprobación de la versión vigente y la aplicación sin duplicados y la facilidad de uso de los recorridos. Las evidencias actuales respaldan las decisiones de diseño; los beneficios esperados de ahorro, menor esfuerzo y coordinación familiar deberán medirse con la solución implementada.

### Recomendaciones

- Implementar y verificar el diseño táctico del Capítulo V y completar la interacción del prototipo a partir de los mock-ups y flujos del Capítulo VI. El Capítulo VII aún no contiene evidencias de implementación, pruebas, validación o despliegue de la entrega actual.
- Conciliar la matriz de respuestas de las entrevistas, los precios y datos del equipo de la landing y las versiones del stack con sus fuentes correspondientes.
- Mantener alineados los diagramas estratégicos y tácticos con los adaptadores de IA y servicios de planificación, distinguiendo módulos del backend y servicios externos.
- Probar borradores con datos insuficientes, versiones obsoletas, fallos parciales y reintentos sin duplicados.
- Evaluar la categorización y las recomendaciones con casos del dominio, sin presentar confianza como precisión medida. Verificar continuidad manual e información mínima autorizada.
- Validar la facilidad de uso con personas de ambos segmentos antes de concluir que el producto reduce el esfuerzo de registro o mejora la coordinación familiar.

## Video About-the-Team

[Enlace al video de presentación del equipo](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202319950_upc_edu_pe/IQB_Q8u14DyQT4TXefm7wQfSAakkU-BGVGYdRbP-bV8M77M?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=P0yw1r)

# Conclusiones

## Conclusiones y recomendaciones

El TB2 reúne el diseño de arquitectura y experiencia de Intiva, la validación con ambos segmentos y los resultados del Sprint 1. El alcance verificado corresponde a una PoC local del plan mensual con Gemini.

### Sobre el Capítulo I: Introducción

- Las 5W y 2H y el diagrama de Ishikawa organizan posibles causas de las dificultades de gestión financiera. Las fuentes consultadas permiten contextualizar el problema, pero no prueban que la solución propuesta produzca mejoras en los usuarios.
- Lean UX define hipótesis y metas de negocio. Los incrementos de retención y margen, los 500 grupos activos y el CSAT del 75% son objetivos propuestos; necesitan una línea base e instrumentos de medición.
- Los segmentos se distinguen por su responsabilidad en las finanzas personales y del hogar. Los datos por edad del INEI contextualizan el acceso a cuentas, sin demostrar por sí solos el rol financiero de una persona.

### Sobre el Capítulo II: Requirements Elicitation & Analysis

- Las seis entrevistas registran necesidades de facilidad de uso, seguimiento de gastos, privacidad y recordatorios. Se emplean para orientar el diseño, sin generalizar sus hallazgos a toda la población.
- Los porcentajes de los gráficos heredados no tienen una matriz de respuestas que permita verificar su base de cálculo. El análisis mantiene una lectura cualitativa hasta conciliar esos datos.
- La comparación de Fintonic, Monefy y Plum orienta el posicionamiento de Intiva hacia la gestión personal y familiar. No demuestra exclusividad ni valida una ventaja competitiva en el mercado.

### Sobre el Capítulo III: Requirements Specification

- EP 011 reúne la planificación financiera. US 032 cubre proyección, edición y aprobación; US 035 cubre seguimiento y avisos en la segunda etapa. US 033 y US 034 conservan la categorización y el asistente, que solo recomienda. Las funciones de IA están disponibles para toda persona con sesión iniciada, y las suscripciones (EP 004) se postergan.
- TS 023 valida titularidad y versión y evita duplicar cambios al aplicar el plan; TS 024 integra Gemini mediante Spring AI y valida sus respuestas; TS 025 y TS 026 definen RabbitMQ y la base de datos por microservicio. FCM conserva el canal push (TS 017).
- Los criterios de aceptación permiten preparar pruebas funcionales. Describir un escenario esperado no acredita que ya haya sido implementado ni que la prueba haya pasado.

### Sobre el Capítulo IV: Strategic-Level Software Design

- El capítulo IV adopta microservicios, uno por bounded context, cada uno con su propia base de datos. La regla de integración es REST para consultas y validaciones, y RabbitMQ para avisos, lo que elimina el acceso directo de Analytics a los datos de otros contextos que tenía el backend anterior.
- La IA agéntica se concentra en el microservicio AI Agent, el único que usa Gemini (mediante Spring AI). El agente reúne datos y prepara el plan mensual por su cuenta, pero los límites solo se aplican cuando la persona aprueba una versión, y el chat solo recomienda.
- Las suscripciones se registran como un contexto válido que se posterga a una etapa posterior; por eso no tienen microservicio en esta versión.

### Sobre el Capítulo V: Tactical-Level Software Design

- El diseño táctico documenta las cuatro capas de nueve bounded contexts, desplegados como microservicios, junto con diagramas de componentes, clases y base de datos. El plan separa el borrador editable de la aplicación autorizada y conserva el resultado de cada acción.
- El modelo de IA solo tiene herramientas de lectura: las recomendaciones del chat no registran gastos ni modifican metas, y las acciones del plan las aplica el servicio después de la aprobación, con claves idempotentes. Communications recibe por eventos los avisos de los demás servicios y los envía por FCM.

### Sobre el Capítulo VI: Solution UX Design

- El capítulo contiene guías de estilo y arquitectura de información, así como la landing adaptada, sus wireframes para escritorio y móvil, doce wireframes de aplicación y tres wireflows elaborados para TP1.
- Las pantallas muestran categorización, asistencia y planificación: proyección, borrador, aprobación, aplicación y error.
- Las imágenes y composiciones vectoriales de Figma documentan el diseño corregido. Sus montos son ilustrativos; no representan precisión de IA ni integraciones desplegadas.

### Sobre el Capítulo VII: Product Implementation, Validation & Deployment

- La configuración del desarrollo define un mismo entorno para los cuatro integrantes: GitFlow, Conventional Commits, guías de estilo por lenguaje, Docker Compose en local y Azure Container Apps para los microservicios.
- La sección 7.2 registra la implementación y las pruebas del plan mensual. Se comprobó por API que repetir la aprobación de la misma versión conserva un solo límite, un solo evento de aplicación y un solo aviso.
- La sección 7.3 reúne una entrevista por segmento y una evaluación heurística. Estas evidencias orientan ajustes de UX. La facilidad de uso de la aplicación integrada requiere una prueba adicional con usuarios.

### TP1: Conclusiones del equipo

El equipo consolidó el diseño táctico y la experiencia de usuario de Intiva, relacionando los requisitos del proyecto con las capas del software, la organización de la información y las pantallas de la solución. Los aportes de los cuatro integrantes permiten revisar el comportamiento esperado de IA agéntica antes de su implementación.

**Leonardo Solis — Capítulo V.** El diseño de las capas de dominio, interfaz, aplicación e infraestructura permite identificar dónde se aplican las reglas de negocio y dónde se resuelven las integraciones externas. Los diagramas de componentes, clases y base de datos ofrecen una referencia para implementar cada bounded context. Separar el borrador del plan aprobado protege el consentimiento y evita repetir acciones.

**Camila Loli — Secciones 6.1 y 6.2.** Las guías de estilo y la arquitectura de información establecen criterios comunes para la presentación de Intiva en web y móvil. Las etiquetas y la navegación deben ayudar a distinguir una sugerencia de IA, una propuesta pendiente y un gasto validado. La consistencia del diseño deberá contrastarse con pruebas de comprensión y uso en ambos segmentos de usuarios.


**Didier Meza — Secciones 6.3, 6.4.1 y 6.4.2.** La landing, los wireframes y los wireflows organizan los tres recorridos de IA (categorización, asistente y plan mensual) con sus rutas de corrección, descarte, espera y error. Representar estas alternativas desde el wireframe permite que la aprobación del plan y la continuidad manual queden claras antes de diseñar las pantallas finales.

**Omar Rivera — Secciones 6.4.3 y 6.4.4.** Los mock-ups y los user flows permiten revisar la presentación de las pantallas y su relación con los objetivos del usuario. La correspondencia con los wireflows ayuda a mantener las mismas acciones y condiciones en el diseño visual. Estos materiales sirven como base para conectar el prototipo y evaluar las tareas de registro, consulta y aprobación familiar.

**Conclusión conjunta.** El TP1 establece una base de diseño compartida para la implementación de Intiva. La siguiente etapa requiere comprobar la calidad de las respuestas de IA, la aprobación de la versión vigente y la aplicación sin duplicados y la facilidad de uso de los recorridos. Las evidencias actuales respaldan las decisiones de diseño; los beneficios esperados de ahorro, menor esfuerzo y coordinación familiar deberán medirse con la solución implementada.

### TB2: Conclusiones del equipo

La arquitectura objetivo separa los contextos en microservicios detrás de Spring Cloud Gateway. El Sprint 1 verificó localmente la integración del agente, Finances, Savings y Communications con PostgreSQL y RabbitMQ. El backend modular mantiene las funciones que todavía no se han migrado.

Gemini generó un plan a partir de gastos de prueba. La aprobación persistió el límite editado y el reintento de la misma versión conservó un solo aviso. La segunda ejecución verificó un aporte previsto, un recordatorio programado y un aviso al superar el límite. Los mock-ups, el prototipo y los testimonios documentan los recorridos esperados. Quedan pendientes la demostración desde Android y la evidencia de publicación.

### Recomendaciones

- Completar la demostración en Android y registrar las URLs, versiones y resultados de la primera publicación de los productos en la sección 7.2.1.7.
- Conciliar la matriz de respuestas de las entrevistas, los precios y datos del equipo de la landing y las versiones del stack con sus fuentes correspondientes.
- Mantener alineados los diagramas de los capítulos IV y V cuando cambie un microservicio, un evento o una relación entre contextos, y versionar el catálogo de eventos (DT-02).
- Probar borradores con datos insuficientes, versiones obsoletas, fallos parciales y reintentos sin duplicados.
- Evaluar la categorización y las recomendaciones con casos del dominio, sin presentar confianza como precisión medida. Verificar continuidad manual e información mínima autorizada.
- Validar la facilidad de uso con personas de ambos segmentos antes de concluir que el producto reduce el esfuerzo de registro o mejora la coordinación familiar.

## Video About-the-Team

[Enlace al video de presentación del equipo](https://upcedupe-my.sharepoint.com/:v:/g/personal/u202319950_upc_edu_pe/IQB_Q8u14DyQT4TXefm7wQfSAakkU-BGVGYdRbP-bV8M77M?nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D&e=P0yw1r)

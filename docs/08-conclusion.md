# Conclusiones

## Conclusiones y recomendaciones

A partir del trabajo desarrollado hasta el momento en los Capítulos I, II, III y IV para el producto **Intiva** de la startup **Resolum**, el equipo llega a las siguientes conclusiones generales:

### Sobre el Capítulo I: Introducción

- La aplicación de la técnica de las 5W y 2H, junto con el diagrama de Ishikawa, permitió confirmar que el manejo inadecuado de ingresos, gastos y ahorros no responde a una causa única, sino a factores educativos, informativos, contextuales y de gestión que se refuerzan entre sí. Esto valida que Intiva debe atacar el problema desde varios frentes (educación financiera, automatización del registro y visualización de datos) y no solo con una funcionalidad puntual.
- El proceso Lean UX permitió pasar de una idea general de "app de finanzas" a un conjunto de hipótesis medibles (retención, CSAT, grupos familiares activos, margen por suscripciones), lo que le dio una base validable al resto del proyecto.
- Se identificaron dos segmentos objetivo claramente diferenciados —jóvenes con problemas de gasto y ahorro, y responsables de la economía familiar—, cuyas necesidades, si bien relacionadas, requieren distintos niveles de control y colaboración dentro del producto.

### Sobre el Capítulo II: Requirements Elicitation & Analysis

- El análisis competitivo frente a Fintonic, Monefy y Plum evidenció que la ventaja competitiva de Intiva no está en la automatización bancaria ni en la simplicidad extrema del registro, sino en un enfoque educativo y de gamificación que ayuda al usuario a comprender sus propios hábitos financieros.
- Las entrevistas a ambos segmentos confirmaron los hallazgos del Capítulo I: existe una fuerte dependencia de herramientas informales (Excel, notas, billeteras digitales) que resultan tediosas de mantener, además de dificultades recurrentes para recordar fechas de pago y para tener visibilidad conjunta de las finanzas familiares.
- Los User Personas, el User Task Matrix, el Empathy Mapping y el As-Is Scenario Mapping coinciden en un mismo diagnóstico: la carga operativa del registro manual genera frustración (Carlos Castillo) y agotamiento por conciliación de gastos compartidos (María Palacios), lo que sustenta directamente la necesidad de automatizar el registro y centralizar la información familiar.

### Sobre el Capítulo III: Requirements Specification

- El To-Be Scenario Mapping tradujo los puntos de dolor identificados en journeys concretos de mejora, mostrando que el valor percibido del producto depende tanto de la automatización técnica (lectura de notificaciones, alertas, dashboards) como de la experiencia emocional que se busca generar (seguridad, control, tranquilidad).
- La descomposición en Epics y User Stories (US 001 a US 031, más las historias técnicas) demuestra una cobertura funcional completa del ciclo de vida del usuario: desde el conocimiento de la plataforma y la autenticación, pasando por el manejo de cuentas financieras, categorías, límites de gasto y metas de ahorro, hasta la gestión de grupos familiares, las alertas y la visualización de datos.
- Los criterios de aceptación redactados en formato Given-When-Then dejan una base clara y verificable para las etapas de diseño técnico, implementación y pruebas de los siguientes capítulos.

### Sobre el Capítulo IV: Strategic-Level Software Design

- El Attribute-Driven Design permitió priorizar los drivers arquitectónicos (usabilidad, escalabilidad, seguridad y rendimiento) a partir de las historias de usuario más críticas, en lugar de definir la arquitectura de forma aislada de los requisitos del negocio.
- El EventStorming y el Domain Message Flows Modeling, documentados mediante Domain Storytelling sobre el comportamiento real de `intiva-api-platform`, hicieron visibles ocho bounded contexts (IAM, Profiles, Categories & Financial Accounts, Finances, Financial Goals/Savings, Household, Communications y Analytics) y dos mecanismos de integración que conviven en el sistema: llamadas explícitas a un Anti-Corruption Layer y suscripción directa a eventos de dominio.
- El Context Mapping y la discusión de diseño "¿qué pasaría si...?" identificaron un hallazgo relevante para la arquitectura: *Analytics* accede a los repositorios de *Finances* y *Savings* de forma directa, rompiendo el patrón ACL usado en el resto del sistema, lo cual queda registrado como un punto a revisar en el diseño táctico.
- Los diagramas de Software Architecture (system landscape, contexto, contenedores y despliegue) trasladan las decisiones estratégicas del negocio a una representación técnica concreta, dejando la base necesaria para el diseño a nivel táctico (Capítulo V) y la implementación (Capítulo VII).

### Conclusión general

En conjunto, los cuatro capítulos desarrollados muestran una progresión coherente: el problema identificado en el Capítulo I se valida con evidencia real en el Capítulo II, se traduce en requisitos verificables en el Capítulo III y se resuelve mediante decisiones arquitectónicas trazables a esos mismos requisitos en el Capítulo IV. Los Capítulos V, VI y VII (diseño táctico, diseño UX de la solución e implementación, validación y despliegue del producto) quedan pendientes de desarrollo y son necesarios para cerrar el ciclo completo del proyecto, en particular para resolver el hallazgo de acceso directo a repositorios detectado en el Context Mapping y para validar con usuarios reales el producto implementado.

### Recomendaciones

- Priorizar en el diseño táctico una solución para el acceso directo de *Analytics* a los repositorios de *Finances* y *Savings* (por ejemplo, mediante ACL o vistas materializadas), de modo que la arquitectura sea consistente en todos los bounded contexts.
- Completar las entrevistas de validación (Capítulo VII) retomando a los mismos segmentos objetivo entrevistados en el Capítulo II, para verificar si las hipótesis de Lean UX planteadas en el Capítulo I se cumplen con el producto implementado.
- Mantener la trazabilidad ya lograda entre User Stories, Quality Attribute Scenarios y bounded contexts al momento de avanzar con el diseño táctico y la implementación, de manera que cada decisión técnica siga siendo justificable frente a una necesidad real del usuario.

## Video About-the-Team

\<Enlace al video de presentación del equipo\>

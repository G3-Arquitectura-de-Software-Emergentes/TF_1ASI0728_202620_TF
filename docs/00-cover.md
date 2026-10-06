<div align="center">

![Logo UPC](https://upload.wikimedia.org/wikipedia/commons/f/fc/UPC_logo_transparente.png)

Universidad Peruana de Ciencias Aplicadas

Carrera de Ingeniería de Software

Ciclo 8

**1ASI0728**

**Arquitecturas de Software Emergentes**

Sección

**16363**

**Informe de Trabajo Final**

Docente

**Marino Humberto Jara Palacios**

Startup

**Balanza**

Producto

**Intiva**

**Integrantes**

| Código     | Apellidos y Nombres           |
|------------|--------------------------------|
| u202110385   | Loli Ramirez, Camila Cristina |
| u202319950   | Meza Solórzano,Didier Sebastián          |
| u20211g163   | Solis Solis, Leonardo José          |
| u202214214   | Rivera Ticllacuri, Omar Harold          |

**Setiembre 2026**

</div>

<div style="page-break-after: always;"></div>

## Registro de Versiones del Informe

| Versión | Fecha | Autor | Descripción de modificación |
| ------- | ----- | ----- | ---------------------------- |
| TB1 | 16/09/2026 | Loli Ramirez, Camila Cristina<br>Meza Solórzano,Didier Sebastián<br>Solis Solis, Leonardo José<br>Rivera Ticllacuri, Omar Harold | Revisión de los capítulos I, II, III y finalización del capítulo IV |
| TP1 | 05/10/2026 | Meza Solórzano, Didier Sebastián | Desarrollo de las secciones 6.3, 6.3.1, 6.3.2, 6.4.1 y 6.4.2: actualización de la landing de Intiva para IA y smart contracts, wireframes para escritorio y móvil, doce wireframes de aplicación y tres wireflows. Incorporación de nueve imágenes de evidencia y enlaces a Figma; revisión de la trazabilidad con las historias de usuario y técnicas; corrección de los enlaces de entrevistas y registro del aporte individual en Student Outcome. |
| TP1 — corrección | 05/10/2026 | Meza Solórzano, Didier Sebastián | Corrección del nombre de la startup a Balanza, restauración del capítulo IV a su versión previa a la revisión transversal y retiro de enlaces y conclusiones asociados al backend y al informe usados como ejemplos de otro proyecto. |
| TP1 — 6.4.3 y 6.4.4 | 06/10/2026 | Rivera Ticllacuri, Omar Harold | Desarrollo de las secciones 6.4.3 y 6.4.4: mock-ups de la aplicación Android y del sitio web, y User Flows UF01 a UF06 de la página Mockup - User flow - Prototyping de Figma, con su trazabilidad a los wireflows F01 a F03 y su vinculación con la sección TP1. |
| TP1 — alcance tecnológico | 06/10/2026 | Meza Solórzano, Didier Sebastián | Alineación transversal a IA y smart contracts: revisión de US 032, incorporación de US 034 y EP 011, corrección de TS 023 y TS 024, decisiones estratégicas y diseño táctico del capítulo V, landing, wireframes, wireflows y mock-ups afectados; actualización de evidencias, conclusiones, bibliografía y Student Outcome. |
| TP1 — Capítulo V | 06/10/2026 | Solis Solis, Leonardo José | Desarrollo del diseño táctico de IAM, Profiles, Categories, Finances, Savings, Household, Communications y Analytics: capas de dominio, interfaz, aplicación e infraestructura; diagramas de componentes, clases de dominio y diseño de base de datos. |
| TP1 — 6.1 y 6.2 | 06/10/2026 | Loli Ramirez, Camila Cristina | Desarrollo de las guías de estilo generales y por plataforma: marca, tipografías, colores, espaciado y tono. Documentación de los sistemas de organización, etiquetado, búsqueda y navegación, y de los SEO tags y meta tags de Intiva. |
| TP1 — 6.3, 6.4.1 y 6.4.2 | 06/10/2026 | Meza Solórzano, Didier Sebastián | Consolidación del diseño de landing, wireframes de escritorio y móvil, landing mock-up, doce wireframes de aplicación y tres wireflows para categorización IA, asistencia financiera y aprobación unánime del fondo. Incorporación de imágenes y enlaces a los frames de Figma. |
| TP1 — consolidación UX de aplicación | 06/10/2026 | Rivera Ticllacuri, Omar Harold | Consolidación de mock-ups y user flows de aplicación, con acciones principales, rutas alternativas y relación con los wireflows del entregable. Se documentan las pantallas de IA y del fondo familiar, manteniendo el prototipado interactivo pendiente de validación. |

<div style="page-break-after: always;"></div>

## Project Report Collaboration Insights

URL del repositorio del Project Report en GitHub: [TF_1ASI0728_202620_TF — develop](https://github.com/G3-Arquitectura-de-Software-Emergentes/TF_1ASI0728_202620_TF/tree/develop)

## TB1:

El equipo realizó la redacción y revisión de los capítulos I, II, III y finalizó el capítulo IV. La coordinación de esta entrega se realizó distribuyendo las actividades de análisis, redacción, diseño y revisión entre los integrantes, consolidando los avances para la entrega del TB1.

## TP1

El equipo desarrolló el diseño táctico y la experiencia de usuario de Intiva para el TP1. Leonardo elaboró el Capítulo V; Camila, las guías de estilo y la arquitectura de información; Didier, la landing, los wireframes y wireflows; y Omar, los mock-ups y user flows. Los aportes se integraron en el reporte y Figma, considerando IA para la asistencia financiera y smart contracts para la aprobación unánime de gastos familiares.

<div style="page-break-after: always;"></div>

## Contenido

- [Capítulo I: Introducción](#capítulo-i-introducción)
  - [1.1. Startup Profile](#11-startup-profile)
    - [1.1.1. Descripción de la Startup](#111-descripción-de-la-startup)
    - [1.1.2. Perfiles de integrantes del equipo](#112-perfiles-de-integrantes-del-equipo)
  - [1.2. Solution Profile](#12-solution-profile)
    - [1.2.1. Antecedentes y problemática](#121-antecedentes-y-problemática)
    - [1.2.2. Lean UX Process](#122-lean-ux-process)
      - [1.2.2.1. Lean UX Problem Statements](#1221-lean-ux-problem-statements)
      - [1.2.2.2. Lean UX Assumptions](#1222-lean-ux-assumptions)
      - [1.2.2.3. Lean UX Hypothesis Statements](#1223-lean-ux-hypothesis-statements)
      - [1.2.2.4. Lean UX Canvas](#1224-lean-ux-canvas)
  - [1.3. Segmentos objetivo](#13-segmentos-objetivo)
- [Capítulo II: Requirements Elicitation \& Analysis](#capítulo-ii-requirements-elicitation--analysis)
  - [2.1. Competidores](#21-competidores)
    - [2.1.1. Análisis competitivo](#211-análisis-competitivo)
    - [2.1.2. Estrategias y tácticas frente a competidores](#212-estrategias-y-tácticas-frente-a-competidores)
  - [2.2. Entrevistas](#22-entrevistas)
    - [2.2.1. Diseño de entrevistas](#221-diseño-de-entrevistas)
    - [2.2.2. Registro de entrevistas](#222-registro-de-entrevistas)
    - [2.2.3. Análisis de entrevistas](#223-análisis-de-entrevistas)
  - [2.3. Needfinding](#23-needfinding)
    - [2.3.1. User Personas](#231-user-personas)
    - [2.3.2. User Task Matrix](#232-user-task-matrix)
    - [2.3.3. Empathy Mapping](#233-empathy-mapping)
    - [2.3.4. As-is Scenario Mapping](#234-as-is-scenario-mapping)
  - [2.4. Ubiquitous Language](#24-ubiquitous-language)
- [Capítulo III: Requirements Specification](#capítulo-iii-requirements-specification)
  - [3.1. To-Be Scenario Mapping](#31-to-be-scenario-mapping)
  - [3.2. User Stories](#32-user-stories)
  - [3.3. Impact Mapping](#33-impact-mapping)
  - [3.4. Product Backlog](#34-product-backlog)
- [Capítulo IV: Strategic-Level Software Design](#capítulo-iv-strategic-level-software-design)
  - [4.1. Strategic-Level Attribute-Driven Design](#41-strategic-level-attribute-driven-design)
    - [4.1.1. Design Purpose](#411-design-purpose)
    - [4.1.2. Attribute-Driven Design Inputs](#412-attribute-driven-design-inputs)
      - [4.1.2.1. Primary Functionality (Primary User Stories)](#4121-primary-functionality-primary-user-stories)
      - [4.1.2.2. Quality Attribute Scenarios](#4122-quality-attribute-scenarios)
      - [4.1.2.3. Constraints](#4123-constraints)
    - [4.1.3. Architectural Drivers Backlog](#413-architectural-drivers-backlog)
    - [4.1.4. Architectural Design Decisions](#414-architectural-design-decisions)
    - [4.1.5. Quality Attribute Scenario Refinements](#415-quality-attribute-scenario-refinements)
  - [4.2. Strategic-Level Domain-Driven Design](#42-strategic-level-domain-driven-design)
    - [4.2.1. EventStorming](#421-eventstorming)
    - [4.2.2. Candidate Context Discovery](#422-candidate-context-discovery)
    - [4.2.3. Domain Message Flows Modeling](#423-domain-message-flows-modeling)
    - [4.2.4. Bounded Context Canvases](#424-bounded-context-canvases)
    - [4.2.5. Context Mapping](#425-context-mapping)
  - [4.3. Software Architecture](#43-software-architecture)
    - [4.3.1. Software Architecture System Landscape Diagram](#431-software-architecture-system-landscape-diagram)
    - [4.3.2. Software Architecture Context Level Diagrams](#432-software-architecture-context-level-diagrams)
    - [4.3.3. Software Architecture Container Level Diagrams](#433-software-architecture-container-level-diagrams)
    - [4.3.4. Software Architecture Deployment Diagrams](#434-software-architecture-deployment-diagrams)
- [Capítulo V: Tactical-Level Software Design](05-cha05-tactical-level-software-design.md)
  - [5.1. Bounded Context: Identity and Access Management (IAM)](05-cha05-tactical-level-software-design.md#51-bounded-context-identity-and-access-management-iam)
  - [5.2. Bounded Context: Profiles](05-cha05-tactical-level-software-design.md#52-bounded-context-profiles)
  - [5.3. Bounded Context: Categories & Financial Accounts](05-cha05-tactical-level-software-design.md#53-bounded-context-categories--financial-accounts)
  - [5.4. Bounded Context: Finances](05-cha05-tactical-level-software-design.md#54-bounded-context-finances)
  - [5.5. Bounded Context: Financial Goals (Savings)](05-cha05-tactical-level-software-design.md#55-bounded-context-financial-goals-savings)
  - [5.6. Bounded Context: Household](05-cha05-tactical-level-software-design.md#56-bounded-context-household)
  - [5.7. Bounded Context: Communications](05-cha05-tactical-level-software-design.md#57-bounded-context-communications)
  - [5.8. Bounded Context: Analytics](05-cha05-tactical-level-software-design.md#58-bounded-context-analytics)
- [Capítulo VI: Solution UX Design](#capítulo-vi-solution-ux-design)
  - [6.1. Style Guidelines](#61-style-guidelines)
    - [6.1.1. General Style Guidelines](#611-general-style-guidelines)
    - [6.1.2. Web, Mobile \& Devices Style Guidelines](#612-web-mobile--devices-style-guidelines)
  - [6.2. Information Architecture](#62-information-architecture)
    - [6.2.1. Organization Systems](#621-organization-systems)
    - [6.2.2. Labeling Systems](#622-labeling-systems)
    - [6.2.3. Searching Systems](#623-searching-systems)
    - [6.2.4. SEO Tags and Meta Tags](#624-seo-tags-and-meta-tags)
    - [6.2.5. Navigation Systems](#625-navigation-systems)
  - [6.3. Landing Page UI Design](#63-landing-page-ui-design)
    - [6.3.1. Landing Page Wireframe](#631-landing-page-wireframe)
    - [6.3.2. Landing Page Mock-up](#632-landing-page-mock-up)
  - [6.4. Applications UX/UI Design](#64-applications-uxui-design)
    - [6.4.1. Applications Wireframes](#641-applications-wireframes)
    - [6.4.2. Applications Wireflow Diagrams](#642-applications-wireflow-diagrams)
    - [6.4.3. Applications Mock-ups](#643-applications-mock-ups)
    - [6.4.4. Applications User Flow Diagrams](#644-applications-user-flow-diagrams)
  - [6.5. Applications Prototyping](#65-applications-prototyping)
- [Capítulo VII: Product Implementation, Validation \& Deployment](#capítulo-vii-product-implementation-validation--deployment)
  - [7.1. Software Configuration Management](#71-software-configuration-management)
    - [7.1.1. Software Development Environment Configuration](#711-software-development-environment-configuration)
    - [7.1.2. Source Code Management](#712-source-code-management)
    - [7.1.3. Source Code Style Guide \& Conventions](#713-source-code-style-guide--conventions)
    - [7.1.4. Software Deployment Configuration](#714-software-deployment-configuration)
  - [7.2. Solution Implementation](#72-solution-implementation)
    - [7.2.1. Sprint 1](#721-sprint-1)
      - [7.2.1.1. Sprint Planning 1](#7211-sprint-planning-1)
      - [7.2.1.2. Sprint Backlog 1](#7212-sprint-backlog-1)
      - [7.2.1.3. Development Evidence for Sprint Review](#7213-development-evidence-for-sprint-review)
      - [7.2.1.4. Testing Suite Evidence for Sprint Review](#7214-testing-suite-evidence-for-sprint-review)
      - [7.2.1.5. Execution Evidence for Sprint Review](#7215-execution-evidence-for-sprint-review)
      - [7.2.1.6. Services Documentation Evidence for Sprint Review](#7216-services-documentation-evidence-for-sprint-review)
      - [7.2.1.7. Software Deployment Evidence for Sprint Review](#7217-software-deployment-evidence-for-sprint-review)
      - [7.2.1.8. Team Collaboration Insights during Sprint](#7218-team-collaboration-insights-during-sprint)
  - [7.3. Validation Interviews](#73-validation-interviews)
    - [7.3.1. Diseño de Entrevistas](#731-diseño-de-entrevistas)
    - [7.3.2. Registro de Entrevistas](#732-registro-de-entrevistas)
    - [7.3.3. Evaluaciones según heurísticas](#733-evaluaciones-según-heurísticas)
  - [7.4. Video About-the-Product](#74-video-about-the-product)
- [Conclusiones](#conclusiones)
  - [Conclusiones y recomendaciones](#conclusiones-y-recomendaciones)
  - [Video About-the-Team](#video-about-the-team)
- [Bibliografía](#bibliografía)
- [Anexos](#anexos)
  - [Anexo A: Videos de Exposiciones](#anexo-a-videos-de-exposiciones)

<div style="page-break-after: always;"></div>

## Student Outcome

| Criterio específico | Acciones Realizadas | Conclusiones |
| --- | --- | --- |
| Comunica oralmente sus ideas y/o resultados con objetividad a público de diferentes especialidades y niveles jerárquicos, en el marco del desarrollo de un proyecto en ingeniería. | **AV1: Meza Solórzano, Didier Sebastian:** Participé en la exposición de los hallazgos del análisis competitivo y las entrevistas del Capítulo 2, así como de las decisiones estratégicas de diseño (Attribute-Driven Design) del Capítulo 4, explicando los drivers arquitectónicos y las restricciones técnicas del proyecto a mis compañeros de equipo.<br><br>**AV1: Rivera Ticllacuri, Omar Harold:** Expuse el perfil del equipo (Capítulo 1) y el diseño estratégico DDD del Capítulo 4 (EventStorming, Domain Message Flows, Bounded Context Canvases y Context Mapping) a mis compañeros.<br><br>**AV1: Loli Ramirez, Camila Cristina:** Expuse al equipo las decisiones arquitectónicas del Capítulo 4 y el porqué de elegir el monolito modular y la caché cache-aside, además de los resultados del EventStorming y del descubrimiento de contextos candidatos en Miro.<br><br>**AV1: Solis Solis, Leonardo José:** Participé en la sustentación de los mapas de escenarios (As-Is y To-Be) del Capítulo 3, y en la exposición de los diagramas de arquitectura C4 (Contexto y Contenedores) del Capítulo 4, detallando de forma clara la interacción entre nuestros componentes internos y los servicios externos.<br><br>**TP1: Solis Solis, Leonardo José:** Preparé los diagramas del Capítulo V como apoyo visual para explicar las responsabilidades de las cuatro capas de cada bounded context y la relación entre sus componentes, clases y tablas. Organicé el material del diseño táctico para su sustentación.<br><br>**TP1: Loli Ramirez, Camila Cristina:** Organicé las guías de estilo y los sistemas de información de 6.1 y 6.2 como material para explicar la identidad visual, las etiquetas, las búsquedas y la navegación de Intiva en web y móvil.<br><br>**TP1: Meza Solórzano, Didier Sebastián:** Preparé la landing, los wireframes y los tres wireflows como apoyo para explicar la categorización IA, la asistencia financiera y la aprobación unánime del fondo. Representé las alternativas de corrección, rechazo, espera y error.<br><br>**TP1: Rivera Ticllacuri, Omar Harold:** Organicé los mock-ups y los user flows de 6.4.3 y 6.4.4 como apoyo visual para explicar los objetivos del usuario, las acciones de cada pantalla y las rutas principales y alternativas. | **TB1:** La participación en las exposiciones permitió comunicar de manera clara y objetiva los resultados obtenidos, las decisiones de diseño y la arquitectura del proyecto, facilitando que el equipo comprenda los principales aspectos técnicos y estratégicos desarrollados.<br><br>**TP1:** La organización de los diagramas y diseños como apoyo visual permitió preparar una explicación común del diseño táctico, las guías de estilo y los recorridos de Intiva, incluyendo la revisión de sugerencias de IA y la aprobación unánime del fondo familiar. |
| Comunica en forma escrita ideas y/o resultados con objetividad a público de diferentes especialidades y niveles jerárquicos, en el marco del desarrollo de un proyecto en ingeniería. | **AV1: Meza Solórzano, Didier Sebastian:** Redacté el análisis competitivo, el registro y análisis de entrevistas, y el needfinding del Capítulo 2, además del Design Purpose, los Primary User Stories, los Quality Attribute Scenarios, los Constraints y el Architectural Drivers Backlog del Capítulo 4, documentando cada decisión con criterios de aceptación y justificación técnica.<br><br>**AV1: Rivera Ticllacuri, Omar Harold:** Redacté mi perfil en el Capítulo 1 y, en el Capítulo 4, toda la sección 4.2 (Domain Message Flows Modeling, Bounded Context Canvases de los 8 contextos y Context Mapping), incluyendo el hallazgo de que Analytics accede directamente a los repositorios de Finances y Savings sin ACL.<br><br>**AV1: Loli Ramirez, Camila Cristina:** Redacté las secciones 4.1.4 y 4.1.5 (iteraciones del Quality Attribute Workshop, decisiones AD-01 a AD-19, deudas de diseño y refinamiento de los escenarios de calidad) y las secciones 4.2.1 y 4.2.2 (EventStorming y descubrimiento de los ocho contextos candidatos). También realicé la revisión del Capítulo 1.<br><br>**AV1: Solis Solis, Leonardo Jose:** Estructuré y redacté las Historias de Usuario, Historias Técnicas y Spike Stories del Capítulo 3 con sus respectivos criterios de aceptación. Asimismo, documenté la explicación técnica de los diagramas de Landscape, Contexto y Contenedores en el Capítulo 4.<br><br>**TP1: Solis Solis, Leonardo José:** Documenté el Capítulo V: Domain Layer, Interface Layer, Application Layer e Infrastructure Layer de los ocho bounded contexts, con diccionarios de clases y diagramas de componentes, clases de dominio y base de datos.<br><br>**TP1: Loli Ramirez, Camila Cristina:** Redacté las secciones 6.1 y 6.2: marca, tipografías, paleta, espaciado, tono y lineamientos por plataforma; sistemas de organización, etiquetado, búsqueda y navegación; SEO tags y meta tags.<br><br>**TP1: Meza Solórzano, Didier Sebastián:** Documenté 6.3, 6.3.1, 6.3.2, 6.4.1 y 6.4.2: landing, wireframes de escritorio y móvil, mock-up, doce wireframes de aplicación y tres wireflows. Incorporé imágenes y enlaces a Figma y relacioné el diseño con US 032, US 033, US 034, TS 023 y TS 024. Consolidé la revisión del alcance de IA y smart contracts y las evidencias del informe.<br><br>**TP1: Rivera Ticllacuri, Omar Harold:** Documenté los mock-ups de aplicación de 6.4.3 y los user flows de 6.4.4, relacionando objetivos, pantallas, acciones y alternativas con los wireflows y las evidencias de Figma. | **TB1:** La documentación realizada permitió organizar y comunicar de forma clara los requerimientos, hallazgos y decisiones técnicas del proyecto, dejando evidencia del análisis y sustento utilizado para definir la solución arquitectónica.<br><br>**TP1:** La documentación de los capítulos V y VI integra las responsabilidades del software, los lineamientos visuales y los recorridos del usuario. La relación entre requisitos, diagramas, pantallas y evidencias permite revisar el alcance de IA y smart contracts y orientar la implementación. |

<div style="page-break-after: always;"></div>

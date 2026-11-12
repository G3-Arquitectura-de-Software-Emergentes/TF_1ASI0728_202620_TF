# Capítulo VII: Product Implementation, Validation & Deployment

En este capítulo se documenta la implementación de Intiva: la configuración del entorno de trabajo, la gestión del código fuente, las convenciones de estilo y el despliegue de los productos (landing page, aplicación móvil, aplicación web y microservicios), así como el avance de cada sprint y la validación con usuarios.

## 7.1. Software Configuration Management

En esta sección se definen las herramientas, prácticas y convenciones que usará el equipo de Balanza durante el desarrollo de Intiva. El objetivo es que los cuatro integrantes trabajen con el mismo entorno, sigan las mismas reglas al escribir y versionar el código, y desplieguen cada producto de forma ordenada.

### 7.1.1. Software Development Environment Configuration

**Project Management**

- **GitHub:** es la plataforma central del proyecto. Además de alojar el código, el informe se redacta en archivos Markdown dentro de un repositorio, de modo que cada integrante agrega sus avances en una rama y los integra mediante *pull requests*.
- **Discord y Google Meet:** se usarán para las reuniones del equipo, en las que se revisan los avances, se toman decisiones sobre el proyecto y se reparten las tareas de cada sprint.
- **WhatsApp:** se usará para coordinar tareas del día a día, avisar de cambios en el repositorio y recordar las fechas de entrega.

**Requirements Management**

- **Trello:** se usará para gestionar el Product Backlog y el Sprint Backlog. Cada tarjeta corresponde a una historia de usuario o tarea técnica, tiene un responsable y avanza por las columnas To-do, In-Process, To-Review y Done.

**Product UX/UI Design**

- **Miro:** se usó para las sesiones de EventStorming, el descubrimiento de bounded contexts y los mapas As-Is de los User Personas.
- **Figma:** se usa para diseñar de forma colaborativa la guía de estilo, los wireframes, los mock-ups, los user flows y el prototipo de la aplicación móvil, la aplicación web y la landing page.

**Software Development**

- **Java y Spring Boot en IntelliJ IDEA:** los microservicios se desarrollarán con Java 21 (LTS) y Spring Boot, junto con Spring Web, Spring Data JPA, Spring Security, JWT y Lombok (C-01). Habrá un microservicio por bounded context. Se escogió IntelliJ IDEA porque integra Maven, la depuración y la refactorización del código.
- **Spring AI y Gemini API (Google AI Studio):** el agente financiero será un microservicio propio, construido con Spring AI para mantenerse dentro del mismo stack de Java. Usará el modelo Gemini mediante su API, cuya clave se genera en Google AI Studio y se guarda como variable de entorno, nunca en el código. Con *tool calling*, el agente no se limita a conversar: consulta los datos del usuario a través de las APIs de los otros microservicios y prepara acciones concretas, como un límite de gasto, que solo se guardan cuando el usuario las aprueba.
- **Kotlin y Jetpack Compose en Android Studio:** la aplicación móvil será nativa para Android 8.0 o superior. Usará Jetpack Compose para la interfaz, Compose Navigation, Hilt para la inyección de dependencias, Retrofit para consumir la API y Room para la persistencia local (C-03). Se usará Android Studio por su emulador y sus herramientas de inspección de interfaces.
- **Vue en Visual Studio Code:** la aplicación web se desarrollará con Vue y Vite, PrimeVue como librería de componentes, Pinia para el manejo de estado, Axios para las peticiones HTTP y Vue-i18n para el cambio de idioma (C-02). Se usará pnpm como gestor de paquetes.
- **Astro en Visual Studio Code:** la landing page se construirá con Astro y Tailwind CSS, lo que permite generar un sitio estático, rápido y disponible en español e inglés (C-04).

**Bases de datos y caché**

- **PostgreSQL y pgAdmin 4:** cada microservicio tendrá su propia base de datos dentro de un mismo servidor PostgreSQL, y ninguno podrá consultar la base de datos de otro. pgAdmin 4 se usará para administrar y consultar las tablas durante el desarrollo.
- **Redis:** se usará como caché en memoria para las métricas del panel y los códigos temporales de recuperación (TS 014).
- **Room (SQLite):** almacenará en el celular los datos que la aplicación móvil necesita sin conexión.

**Microservicios y comunicación entre servicios**

- **Spring Cloud Gateway:** será el API Gateway, el único punto de entrada para la aplicación móvil y la aplicación web. Enrutará cada petición al microservicio correspondiente según su ruta (`/api/v1/{recurso}`), sin exponer directamente los servicios internos. Se escogió porque es parte del ecosistema Spring y se configura igual que el resto de microservicios.
- **RabbitMQ:** será el message broker para la comunicación asíncrona. Cuando un servicio necesita una respuesta para continuar, llama por REST a otro servicio; cuando solo avisa que algo pasó (por ejemplo, que se registró un gasto), publica un evento en RabbitMQ y los servicios interesados lo procesan después.
- **Docker y Docker Compose:** cada microservicio se empaquetará en una imagen Docker. Con Docker Compose el equipo levantará en local los servicios, el gateway, PostgreSQL, Redis y RabbitMQ con un solo comando, en una red interna.
- No se usará un servidor de descubrimiento de servicios como Eureka, porque la red interna de Docker en local y Azure Container Apps en la nube ya resuelven los servicios por su nombre.

**Software Documentation**

- **Markdown en GitHub:** formato del informe del proyecto y de los archivos README de cada repositorio.
- **Structurizr:** se usa para elaborar los diagramas C4 de contexto, contenedores, componentes y despliegue.
- **Swagger UI (OpenAPI):** cada microservicio expondrá la documentación de sus endpoints REST con springdoc-openapi, que también permite probarlos desde el navegador.
- **OBS Studio y OneDrive:** OBS Studio se usará para grabar las entrevistas de validación y los videos del producto, y OneDrive para alojar esos videos y compartir sus enlaces en el informe.

**Software Testing**

- **JUnit 5 y Mockito:** se usarán para las pruebas unitarias de las entidades, los servicios de dominio y los servicios de aplicación de cada microservicio.
- **Spring Boot Test:** permitirá las pruebas de integración de los controladores y los repositorios.
- **Gherkin:** los criterios de aceptación de las historias de usuario se escribirán como escenarios Dado / Cuando / Entonces, tal como se definieron en el Capítulo III.
- **Postman:** se usará para probar manualmente los endpoints a través del API Gateway, con colecciones compartidas por el equipo.

### 7.1.2. Source Code Management

Para el control de versiones se usará Git, y GitHub como plataforma de alojamiento de los repositorios. Todos los repositorios estarán dentro de la organización del equipo, de modo que cada integrante tenga acceso a ellos y los cambios se revisen mediante *pull requests* antes de integrarse.

**Repositorios**

Los nombres de los repositorios seguirán el formato usado en la versión anterior de Intiva (intiva-landing-page, intiva-web-application, intiva-mobile-application e intiva-api-platform). Todo el backend estará en un solo repositorio, con una carpeta por microservicio, además del API Gateway y la configuración de Docker Compose. Así, el equipo puede levantar todos los servicios juntos y revisar en un mismo *pull request* los cambios que afectan a más de uno.

- Organización en GitHub: https://github.com/G3-Arquitectura-de-Software-Emergentes
- Informe del proyecto: https://github.com/G3-Arquitectura-de-Software-Emergentes/TF_1ASI0728_202620_TF


| Repositorio | Contenido | Enlace |
| --- | --- | --- |
| Landing page | Sitio estático en Astro | https://github.com/G3-Arquitectura-de-Software-Emergentes/intiva-landing-page |
| Aplicación móvil | Aplicación Android en Kotlin | https://github.com/G3-Arquitectura-de-Software-Emergentes/Intiva-mobile-application |
| Backend | Microservicios en Spring Boot (una carpeta por servicio), Spring Cloud Gateway y Docker Compose | https://github.com/G3-Arquitectura-de-Software-Emergentes/intiva-api-platform |

**Estrategia de ramas: GitFlow**

Se seguirá el modelo GitFlow, propuesto por Vincent Driessen (https://nvie.com/posts/a-successful-git-branching-model/), porque separa el trabajo en curso de las versiones estables y permite que varios integrantes desarrollen funcionalidades al mismo tiempo sin afectar lo que ya está publicado.

- **main:** contiene solo versiones estables, listas para desplegarse. Cada integración a esta rama se marca con una etiqueta de versión.
- **develop:** rama de integración. Aquí se juntan las funcionalidades terminadas antes de preparar una nueva versión.
- **feature/\*:** parten de develop y contienen una sola funcionalidad. Se nombran en inglés y en *kebab-case*, según la funcionalidad o el microservicio. Por ejemplo: `feature/ai-monthly-plan`, `feature/household-invitations`. Al terminar, se integran a develop mediante un *pull request* revisado por otro integrante.
- **release/\*:** parten de develop cuando se prepara una nueva versión. En ellas solo se corrigen detalles menores y se actualiza el número de versión antes de integrarla a main y a develop. Por ejemplo: `release/1.0.0`.
- **hotfix/\*:** parten de main para corregir un error urgente en producción y se integran tanto a main como a develop. Por ejemplo: `hotfix/1.0.1`.

**Versionado semántico**

Para numerar las versiones se usará Semantic Versioning 2.0.0 (https://semver.org/), con el formato `MAJOR.MINOR.PATCH`:

- **MAJOR:** cambios incompatibles con la versión anterior, por ejemplo, un cambio en un contrato de la API que obliga a actualizar los clientes.
- **MINOR:** nuevas funcionalidades compatibles con la versión anterior.
- **PATCH:** corrección de errores sin afectar la compatibilidad.

Cada versión publicada en main se marcará con una etiqueta de Git, por ejemplo `v1.0.0`.

**Convenciones para los mensajes de commit**

Los mensajes de commit seguirán la especificación Conventional Commits (https://www.conventionalcommits.org/en/v1.0.0/), con el formato `type(scope): description`. Se escribirán en inglés, en tiempo presente y en modo imperativo, y el *scope* indicará el microservicio o módulo afectado. Los tipos que se usarán son:

- **feat:** nueva funcionalidad.
- **fix:** corrección de un error.
- **docs:** cambios en la documentación.
- **refactor:** reestructuración del código sin cambiar su comportamiento.
- **test:** creación o actualización de pruebas.
- **chore:** cambios en la configuración, las dependencias o el proceso de construcción.


### 7.1.3. Source Code Style Guide & Conventions

En esta sección se presentan las convenciones de estilo que seguirá el equipo en cada lenguaje del proyecto, para que el código sea consistente y fácil de leer sin importar quién lo haya escrito.

**Convenciones generales**

- Todo el código (clases, variables, archivos, endpoints y ramas) se escribe en inglés. Los textos que ve el usuario están en español e inglés mediante archivos de traducción.
- Los nombres deben describir lo que hacen; se evitan las abreviaturas poco claras.
- Las claves, contraseñas y URLs de los servicios no se escriben en el código. Se manejan con variables de entorno, y cada repositorio incluye un archivo `.env.example` con los nombres de las variables necesarias, sin sus valores.

**Backend: Java y Spring Boot**

- Se sigue el Google Java Style Guide (https://google.github.io/styleguide/javaguide.html).
- Clases e interfaces en *PascalCase*; métodos y variables en *camelCase*; constantes en *UPPER_SNAKE_CASE*; paquetes en minúscula.
- Las carpetas de los microservicios se nombran en *kebab-case* con el sufijo `-service`, por ejemplo `finances-service` o `agent-service`.
- Cada microservicio organiza sus paquetes según las capas definidas en AD-02: `domain.model`, `domain.services`, `application.internal`, `infrastructure` e `interfaces.rest`.
- Las clases llevan un sufijo según su función. Por ejemplo: `TransactionsController`, `TransactionCommandService`, `TransactionQueryService`, `TransactionRepository`, `CreateTransactionCommand` y `TransactionResource`.
- Los endpoints REST siguen el patrón `/api/v1/{recurso}`, con sustantivos en plural, en minúscula y en *kebab-case* (C-05). Por ejemplo: `/api/v1/savings-goals`.
- Los eventos que se publican en RabbitMQ se nombran en pasado y en *PascalCase*, como `TransactionRegistered` o `MonthlyPlanApproved`.

**Aplicación móvil: Kotlin y Jetpack Compose**

- Se siguen las Kotlin Coding Conventions (https://kotlinlang.org/docs/coding-conventions.html) y la guía de estilo de Kotlin para Android (https://developer.android.com/kotlin/style-guide).
- Las funciones `@Composable` que dibujan interfaz se nombran en *PascalCase* como sustantivos, por ejemplo `TransactionCard` o `HomeScreen`, según las Compose API Guidelines (https://github.com/androidx/androidx/blob/androidx-main/compose/docs/compose-api-guidelines.md).
- El código se organiza por funcionalidad (por ejemplo, `transactions`, `savings`, `household`), y dentro de cada una se separan las capas de datos, dominio y presentación.
- Los ViewModels terminan en `ViewModel` y los repositorios en `Repository`.

**Aplicación web: Vue y JavaScript**

- Se sigue la guía de estilo oficial de Vue (https://vuejs.org/style-guide/), con sus reglas esenciales y fuertemente recomendadas.
- Los componentes se nombran en *PascalCase* y con más de una palabra, por ejemplo `ExpenseChart.vue` o `ReportFilters.vue`.
- Los *composables* empiezan con `use` (por ejemplo, `useReports`) y los stores de Pinia siguen el patrón `useXStore` (por ejemplo, `useAuthStore`).
- Variables y funciones en *camelCase*; carpetas y archivos que no son componentes en *kebab-case*.

**Landing page: Astro, HTML y CSS**

- Para el marcado y los estilos se sigue el Google HTML/CSS Style Guide (https://google.github.io/styleguide/htmlcssguide.html).
- Los componentes de Astro se nombran en *PascalCase* (por ejemplo, `HeroSection.astro`) y las páginas en *kebab-case*.
- Los estilos se escriben con las clases utilitarias de Tailwind CSS, y los textos de cada idioma se guardan en archivos de traducción separados.

**Pruebas de aceptación: Gherkin**

- Se siguen las convenciones de la referencia oficial de Gherkin (https://cucumber.io/docs/gherkin/reference/).
- Cada historia de usuario tiene un archivo `.feature` con sus escenarios, redactados desde el punto de vista del usuario y con la estructura Dado (*Given*), Cuando (*When*) y Entonces (*Then*), igual que en el Capítulo III.

### 7.1.4. Software Deployment Configuration

Para desplegar Intiva se usarán servicios en la nube que publican cada producto a partir de su repositorio en GitHub. Así, cada versión estable queda disponible para los usuarios sin que el equipo tenga que configurar servidores manualmente para cada cambio.

**Herramientas**

- **Landing page: Vercel.** Vercel se conecta al repositorio de la landing, construye el sitio de Astro y publica una nueva versión cada vez que se integra un cambio en main. También genera una vista previa por cada *pull request*, lo que permite revisar los cambios antes de publicarlos.
- **Aplicación web: Vercel.** La aplicación Vue se publicará del mismo modo, con la URL del API Gateway configurada como variable de entorno del proyecto.
- **Aplicación móvil: Firebase App Distribution.** Un flujo de GitHub Actions compilará y firmará el APK cada vez que se suba una rama `release/*` y lo enviará a Firebase App Distribution, desde donde los integrantes y los usuarios de prueba podrán instalarlo (TS 021).
- **Microservicios: Azure Container Apps.** Cada microservicio y el API Gateway se desplegarán como contenedores en Azure Container Apps (TS 020). Este servicio ejecuta las imágenes Docker, resuelve los nombres de los servicios en su red interna y permite que solo el gateway quede expuesto a internet.
- **Base de datos: Azure Database for PostgreSQL.** Un servidor gestionado alojará la base de datos de cada microservicio.
- **Caché: Redis Cloud.** Se mantiene como servicio gestionado para la caché (TS 022).
- **Proveedor de IA: Gemini API.** No requiere despliegue propio. El microservicio del agente se conecta a la API con su clave, guardada como secreto en Azure.

**Prueba de concepto local**

Antes del despliegue en Azure, la prueba de concepto se levantará en local con Docker Compose. En esta etapa se implementarán tres microservicios completos: el agente de IA, Finances y Communications, junto con Spring Cloud Gateway, PostgreSQL y RabbitMQ. Con ellos se demuestra el recorrido principal: el agente propone un límite de gasto, el usuario lo aprueba, Finances lo guarda y Communications recibe el evento para notificarlo.

**Flujo de despliegue**

1. El integrante termina su funcionalidad en una rama `feature/*` y abre un *pull request* hacia develop, que otro integrante revisa antes de integrarlo.
2. Al preparar una versión, se crea una rama `release/x.y.z`, se verifica su funcionamiento y se integra a main con su etiqueta de versión.
3. Vercel detecta el cambio en main y publica automáticamente la landing page y la aplicación web.
4. Al subir la rama `release/*` de la aplicación móvil, GitHub Actions genera el APK y lo distribuye mediante Firebase App Distribution.
5. Se construyen las imágenes Docker de los microservicios y del API Gateway, y se despliegan en Azure Container Apps con sus variables de entorno (conexión a Azure Database for PostgreSQL, Redis, RabbitMQ y clave de la Gemini API).
6. Los clientes (aplicación móvil y aplicación web) se comunican con los servicios únicamente mediante HTTPS a través del API Gateway.

## 7.3. Validation Interviews

La validación busca comprobar si los dos segmentos entienden la propuesta de Intiva en la landing y pueden usar la aplicación para registrar un gasto, revisar una recomendación y preparar un plan mensual. Esta ronda incluye **dos entrevistas: una por segmento**. Se usará la versión disponible y se indicará si se prueba una aplicación desplegada o un prototipo.

### 7.3.1. Diseño de Entrevistas

- **Segmento 1:** integrantes de familias que participan en gastos del hogar y llevan, o intentan llevar, un registro personal.
- **Segmento 2:** responsables de la economía familiar que organizan presupuestos, metas o vencimientos del hogar.
- **Duración:** 10 a 12 minutos por sesión. Para la evidencia se editarán 3 a 5 minutos por entrevista y se consolidarán en un MP4. La grabación se realizará con OBS Studio y el archivo se alojará en OneDrive. En el informe se incluirá un enlace de lectura por entrevista o el enlace al video consolidado con el minuto de inicio de cada sesión. Cada bloque tendrá nombre autorizado, segmento y fecha.
- **Preparación:** usar una cuenta de prueba con movimientos, ingresos y metas ficticios. Solicitar permiso para grabar, incluir capturas y, si aplica, usar un extracto del testimonio. No usar credenciales ni montos personales reales.

**Antes de preguntar:** pedir permiso para grabar, mostrar la landing y recorrer brevemente las pantallas correspondientes a cada sesión. Para medir si los controles se encuentran sin ayuda, dejar que la persona intente la tarea antes de señalarle dónde tocar. Si ya se le explicó el camino, registrar la sesión como guiada.

**Apertura del moderador:** «Estamos evaluando Intiva, no tu desempeño. Usa la página como lo harías normalmente y cuéntame qué piensas al navegar. Si algo te confunde, dilo con confianza. ¿Nos autorizas a grabar la sesión para el informe del curso?».

| Tarea | Consigna para leer | Evidencia que observar |
| --- | --- | --- |
| T1 · Landing, ambos segmentos | «Mira la página. ¿Para qué crees que sirve Intiva y dónde entrarías para probarla?» | Si identifica el propósito y encuentra el acceso sin ayuda. |
| T2 · Registrar gasto, ambos segmentos | «Registra una compra de supermercado de S/ 48.90. Si no estás de acuerdo con la categoría sugerida, cámbiala.» | Si distingue sugerir de guardar y puede cambiar la categoría antes de registrar. |
| T3 · Asistente, ambos segmentos | «Busca qué gastos pequeños se repiten y revisa cómo se relacionan con una meta de ahorro.» | Si encuentra el asistente y explica qué es una recomendación. |
| T4 · Plan mensual, segmento 1 | «Mira cuánto podrías gastar en Comida el próximo mes y revisa qué pasa si tu límite es S/ 500.» | Si distingue S/ 580 proyectados de S/ 500 de límite y reconoce la diferencia de S/ 80. |
| T4 · Plan mensual, segmento 2 | «Prepara un plan para el próximo mes. Revisa el límite de Comida, un aporte previsto de S/ 100 y un recordatorio para el día 15. Cambia un valor y aprueba la versión elegida.» | Si encuentra los controles, entiende cuándo se aplica el plan y distingue un aporte previsto de un movimiento de dinero. Si un control es estático, registrar la limitación del prototipo. |

**Preguntas después de la demostración:** ¿Qué entendiste que hace Intiva? ¿En qué situación usarías lo que viste? ¿En qué parte esperabas encontrar la opción y qué te hizo dudar? Según el flujo: ¿cómo supiste que el gasto se guardó?, ¿cómo distinguiste lo gastado de lo proyectado?, o ¿qué crees que cambia cuando apruebas el plan? Si la persona usó el producto y quiere compartir su opinión: «¿Qué parte te resultó útil y por qué?». Grabar su respuesta espontánea; no dictarle un elogio.

**Registro por tarea:** ✓ sin ayuda · ~ con ayuda · ✗ no completada · N/E no evaluable en la versión probada. Anotar primer clic, duda, ayuda, resultado y minuto. No guiar de entrada; si la persona se atasca, preguntar «¿Qué esperarías encontrar aquí?» y registrar la ayuda si la recibe.

### 7.3.2. Registro de Entrevistas

Se presenta una ficha por segmento. Los resúmenes describen el contenido previsto de cada video. Las capturas, enlaces y tiempos se añadirán tras la grabación.

#### Segmento 1: Integrantes de familias con problemas de gestión financiera

**Entrevista S1-02 — Valeria Ponce**

| Evidencia | Datos de la entrevista |
| --- | --- |
| **Captura:** | **Nombres y apellidos:** Valeria Ponce |
| **Video (OneDrive):** | **Edad:** 21 años |
| **Inicio:** | **Distrito:** San Juan de Miraflores |
| **Duración:** | **Fecha:** |
| | **Tarea:** Corrección de categoría |
| | **Resumen:** El video está previsto para mostrar la revisión de un gasto de S/ 48.90, el cambio de categoría de «Otros» a «Alimentación» y la confirmación del guardado. También incluye la diferencia entre las compras pequeñas ya registradas y los S/ 580 estimados para Comida el próximo mes. |

#### Segmento 2: Responsables de la economía familiar

**Entrevista S2-01 — Ricardo Medina**

| Evidencia | Datos de la entrevista |
| --- | --- |
| **Captura:** | **Nombres y apellidos:** Ricardo Medina |
| **Video (OneDrive):** | **Edad:** 34 años |
| **Inicio:** | **Distrito:** Chorrillos |
| **Duración:** | **Fecha:** |
| | **Tarea:** Presupuesto familiar |
| | **Resumen:** El video está previsto para mostrar la revisión del presupuesto del hogar: S/ 580 proyectados frente a un límite de S/ 500 para Comida, el ajuste de un aporte previsto de S/ 100 a S/ 80 y la revisión del recordatorio de pago del día 15. El recorrido termina en la consulta del estado del plan tras aprobarlo. |

### 7.3.3. Evaluaciones según heurísticas

**Sitio y aplicación a evaluar:** landing page y aplicación de Intiva. El alcance incluye la versión disponible del flujo de planificación con IA.

**Tareas a evaluar**

1. Identificar qué ofrece Intiva y localizar el acceso desde la landing.
2. Registrar un gasto, corregir la categoría sugerida y comprobar que se guardó.
3. Consultar los gastos hormiga y distinguir lo gastado de lo proyectado.
4. Comparar el gasto proyectado con el límite y revisar el borrador mensual.
5. Editar un aporte previsto y revisar el recordatorio antes de aprobar el plan.
6. Interpretar los estados de aplicación y reconocer si queda alguna acción pendiente.

**Fuera del alcance:** autenticación, suscripciones, pagos o transferencias reales, y notificaciones automáticas de seguimiento mensual.

**Escala de severidad**

| Nivel | Descripción |
| --- | --- |
| 1 | Superficial: afecta la presentación, pero la tarea se puede completar con normalidad. |
| 2 | Menor: causa una duda o demora, pero existe una forma clara de continuar. |
| 3 | Mayor: dificulta completar la tarea o puede llevar a una decisión equivocada. |
| 4 | Muy grave: bloquea la tarea principal o puede provocar una acción difícil de revertir. |

**Tabla de resumen**

Los siguientes problemas son puntos por verificar en la versión evaluada. La severidad es preliminar y se ajustará según lo que ocurra al realizar la tarea.

| N.º | Problema por verificar | Severidad | Heurística o principio | Recomendación |
| --- | --- | ---: | --- | --- |
| 1 | La sugerencia de categoría se confunde con un gasto guardado. | 2 | Usabilidad · Visibilidad del estado del sistema | Distinguir «Gasto sin guardar» de «Gasto registrado». |
| 2 | La opción para cambiar la categoría queda lejos de la sugerencia. | 2 | Arquitectura de información · Encontrabilidad | Colocar «Cambiar» junto a la categoría sugerida. |
| 3 | El monto proyectado puede leerse como un gasto ya realizado. | 3 | Usabilidad · Correspondencia con el mundo real | Mostrar el período junto al importe y distinguir «Ya gastado» de «Estimado para el próximo mes». |
| 4 | El riesgo por categoría no se entiende si se expresa solo con color. | 2 | Diseño inclusivo · Información perceptible | Acompañar el color con texto, por ejemplo, «S/ 80 sobre el límite». |
| 5 | El aporte previsto se puede interpretar como un débito inmediato. | 3 | Usabilidad · Prevención de errores | Indicar antes de aprobar que se guardará el monto previsto y que no se descontará dinero. |
| 6 | Un error general no permite saber qué cambios del plan quedaron pendientes. | 3 | Usabilidad · Recuperación de errores | Mostrar el estado por acción y permitir reintentar solo las pendientes. |

## 7.4. Video About-the-Product

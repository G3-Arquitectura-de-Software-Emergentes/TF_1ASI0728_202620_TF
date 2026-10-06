# Capítulo VI: Solution UX Design

En este capítulo se desarrolla el diseño de la solución planteada para Intiva, la propuesta de Resolum para la gestión de ingresos, gastos y ahorros personales y familiares. Para ello, se definen las guías de estilo y la arquitectura de información que se seguirán en la landing page y en la aplicación móvil, para que el diseño sea coherente y fácil de usar para nuestros segmentos objetivo.

## 6.1. Style Guidelines

En esta sección se explican las guías de estilo para la landing page y la aplicación móvil. Con ellas buscamos que ambos productos se vean coherentes entre sí y que los usuarios reconozcan el estilo de Intiva.

### 6.1.1. General Style Guidelines

**Branding**

*Brand Overview*

Intiva es una plataforma digital que ayudará a las personas y a las familias a registrar sus ingresos y gastos, controlar su presupuesto mediante límites de gasto y planificar metas de ahorro de forma individual o compartida. Nace de una problemática identificada en las entrevistas: la mayoría de usuarios lleva sus finanzas en hojas de Excel, notas del celular o revisando manualmente sus billeteras digitales (Yape, Plin, apps bancarias), lo que vuelve el registro tedioso y deja la información fragmentada entre los integrantes del hogar. Intiva busca centralizar esa información, presentarla de forma visual y acompañar al usuario con alertas y recordatorios para que tome mejores decisiones financieras. Su eslogan, "Controla tus finanzas, transforma tu vida", resume esa promesa.

*Brand Name*

El nombre "Intiva" se relaciona con la idea de manejar las finanzas de forma intuitiva, ya que buscamos que ahorrar y organizar las finanzas sea algo sencillo e intuitivo para cualquier persona, sin necesidad de conocimientos financieros previos. Por eso, el nombre representa una herramienta cercana que ayuda a controlar los gastos y alcanzar metas de ahorro. Además, es un nombre corto, moderno y fácil de recordar y de pronunciar tanto en español como en inglés, lo que permitirá usarlo sin cambios en las dos versiones de idioma de la landing page y como nombre de la aplicación en Google Play.

*Logo*

A continuación, se muestra el logo diseñado para Intiva:

<img src="../assets/img/cap06/logo-intiva.png" width="200" alt="Logo de Intiva"/>

*Logo de Intiva. Fuente: elaboración propia.*

El logo de Intiva está compuesto por un isotipo y un logotipo. El isotipo es un rombo blanco de esquinas redondeadas que contiene un cuadrado índigo con un rayo, símbolo que representa la energía y la rapidez con la que la aplicación permitirá tomar el control del dinero: registrar un movimiento o revisar el presupuesto tomará solo unos segundos. El logotipo "Intiva" se escribe en una tipografía sans-serif de trazo grueso, que transmite solidez y confianza. Se presenta sobre el color índigo principal de la marca y se acompaña del eslogan. En espacios reducidos, como el favicon o la barra de navegación de la landing page, se usará una versión simplificada: un cuadrado índigo con la inicial de la marca.

**Typography**

Para la tipografía escogimos tres fuentes de Google Fonts, cada una para un tipo de texto distinto. Así es más fácil distinguir qué es más importante en cada pantalla.

Para los títulos y encabezados usaremos Manrope (Headline). Es una fuente moderna y algo compacta, por lo que los títulos se ven bien sin ocupar mucho espacio en pantallas pequeñas.

Para los textos de cuerpo, descripciones, formularios y botones usaremos Inter (Body). Esta fuente fue creada para pantallas y se lee bien incluso en tamaños pequeños, lo que ayuda en las listas de movimientos y en los mensajes de alerta.

Para las etiquetas y los montos de dinero usaremos Space Grotesk (Label). Escogimos una fuente aparte para los números porque los montos son el dato más importante en una aplicación de finanzas y queremos que el usuario los encuentre rápido.

| Estilo | Fuente | Uso | Tamaño (landing / app) | Peso |
| --- | --- | --- | --- | --- |
| Display | Manrope | Titular principal de la landing y saldo total | 64 px / 32 sp | Bold / ExtraBold |
| Headline | Manrope | Títulos de sección y de pantalla | 36 a 48 px / 24 sp | Bold |
| Title | Manrope | Títulos de tarjetas y subsecciones | 20 a 24 px / 18 sp | Bold |
| Body | Inter | Textos descriptivos y contenido de formularios | 16 a 18 px / 16 sp | Regular |
| Body small | Inter | Textos secundarios, fechas y ayudas | 14 px / 12 a 13 sp | Regular |
| Button | Inter | Botones y llamadas a la acción | 16 px / 14 sp | SemiBold |
| Label | Space Grotesk | Etiquetas, chips y navegación | 12 a 14 px / 10 a 12 sp | Medium |
| Amount | Space Grotesk | Montos de dinero | 16 a 28 px / 16 a 28 sp | Medium / Bold |

**Colors**

Para escoger los colores pensamos en cómo queremos que se sientan los usuarios, ya que en las entrevistas muchos dijeron que manejar su dinero les genera estrés. Armamos la paleta con el sistema de color de Material Design 3, a partir de cuatro colores base.

El color primario es un índigo (`#534AB7`). Transmite confianza y seriedad, algo necesario en una aplicación que maneja el dinero de las familias, pero se ve más moderno y cercano que el azul que suelen usar los bancos. Lo usaremos en los botones principales, en la opción activa de la navegación y en la tarjeta de saldo.

El color secundario es un verde lima (`#CDEB45`), que se asocia con energía y crecimiento. Como contrasta mucho con el índigo, llama la atención, así que lo usaremos en las llamadas a la acción, en los botones de registro y en el progreso de las metas de ahorro. Sus tonos más oscuros (como `#556500`) servirán para mostrar los ingresos.

El color terciario es un tono cobrizo (`#8A4900`). Lo usaremos como acento en acciones de edición y en algunas categorías, para diferenciar elementos sin quitarle protagonismo a los colores principales.

El color neutro es un gris con un ligero tono violeta (`#78767E`). Con su escala de tonos lo usaremos en fondos, bordes y textos secundarios, y combina bien con el índigo.

Además, usaremos un rojo (`#BA1A1A`) para los gastos, los límites superados y la acción de eliminar. Cada color tiene una escala de tonos, de oscuro a claro, que nos permite crear fondos suaves, estados de botones y un modo oscuro sin perder contraste en los textos.

A continuación se presenta la guía de estilo de Intiva, que reúne la paleta de colores, las tipografías y algunos componentes base (botones, buscador, barras de progreso, barra de navegación y botones de íconos):

![Guía de estilo de Intiva](../assets/img/cap06/style-guide-intiva.png)

*Guía de estilo de Intiva: paleta de colores, tipografías y componentes base. Fuente: elaboración propia en Figma.*

También usaremos colores para indicar el estado de las finanzas, de modo que el usuario lo entienda sin leer el detalle: verde cuando un límite de gasto va bien, ámbar cuando está cerca de alcanzarse y rojo cuando se supera. Para no depender solo del color, cada estado irá acompañado de un texto, y los montos se mostrarán con signo ("+" para ingresos y "−" para gastos).

**Spacing**

El espaciado se basará en múltiplos de 4 y 8 para que la información se vea ordenada. Los valores cambian según el producto:

Para Landing Page:
- Button padding:
    - Vertical: 16px
    - Horizontal: 32px
- Input fields:
    - Altura: 48px
    - Espacio entre campos: 16px
- Ancho máximo del contenido: 1280px
- Margen lateral: 24px (móvil) a 32px (escritorio)
- Margin entre secciones: 96px (móvil) a 128px (escritorio)
- Espacio entre título y subtítulo de sección: 24px

Para Android:
- Button padding:
    - Vertical: 12dp
    - Horizontal: 16dp
- Botón principal de pantalla completa: 56dp de altura
- Input fields:
    - Altura: 56dp
    - Espacio entre campos: 16dp
- Margin lateral de pantalla: 20dp
- Margin entre secciones:
    - Principales: 24dp
    - Internas: 16dp
- Spacing entre textos:
    - Título y subtítulo: 4dp
    - Párrafos: 12dp
- Área táctil mínima: 48dp

**Shapes**

Usaremos esquinas redondeadas para que la interfaz se vea amigable: 8 para inputs y botones pequeños, 12 para tarjetas y chips, 16 para tarjetas destacadas y paneles inferiores, y forma de píldora o círculo para botones de la landing page, avatares, filtros y el botón flotante.

**Tone of voice**

Usaremos un tono cercano y sencillo. En las entrevistas vimos que los términos financieros técnicos confunden a los usuarios, por lo que evitaremos la jerga y trataremos al usuario de "tú" (por ejemplo, "Aquí está el resumen de tus finanzas hoy"). Cuando el usuario logre algo, se lo haremos saber ("¡Cumpliste tu meta de ahorro!"), y las alertas solo informarán lo que pasó, sin regañar ("Has superado tu presupuesto en Entretenimiento"), junto con una opción para resolverlo. Queremos que el usuario sienta que Intiva lo ayuda con sus gastos y que no lo juzga.

### 6.1.2. Web, Mobile & Devices Style Guidelines

Intiva contará con dos productos: una landing page, que será el sitio web estático para dar a conocer la solución, y una aplicación móvil nativa para Android. Se priorizó Android porque, según las entrevistas, la mayoría de usuarios de ambos segmentos utiliza dispositivos con este sistema operativo.

**Landing Page**

- Diseño responsive con enfoque *mobile first*, ya que gran parte del tráfico llegará desde el celular, por ejemplo al compartir el enlace por WhatsApp.
- Puntos de quiebre: móvil (< 768 px), tablet (768 a 1023 px) y escritorio (≥ 1024 px). En móvil, el contenido pasará a una sola columna y el menú superior se convertirá en un menú hamburguesa.
- Alternará secciones oscuras (con un índigo casi negro) y claras para marcar el ritmo de lectura.
- El botón principal será de color Secondary (lima) con texto oscuro, para destacar sobre los fondos índigo y oscuros; el botón secundario será transparente con borde.
- Estará disponible en español e inglés, con un selector de idioma en la barra de navegación.
- Todos los elementos interactivos tendrán un contorno visible al recibir foco con el teclado, y las imágenes tendrán texto alternativo.

**Aplicación móvil (Android)**

- Seguirá los lineamientos de Material Design 3, para que la aplicación se sienta natural para los usuarios de Android, utilizando sus componentes: barra superior, barra de navegación inferior, botón flotante, chips, paneles inferiores (*bottom sheets*) y diálogos.
- Las dimensiones se definirán en `dp` y los textos en `sp`, para respetar el tamaño de letra configurado por el usuario en su teléfono.
- Se diseñará sobre un ancho de referencia de 360 a 390 dp, que corresponde a los dispositivos Android de gama media que usan nuestros segmentos objetivo.
- Los botones de acción principal ocuparán todo el ancho de la pantalla y estarán en la parte inferior, para alcanzarlos fácilmente con el pulgar.
- Para registrar montos se usará un teclado numérico propio con dígitos grandes, evitando abrir el teclado del sistema.
- Se usarán los íconos de Material Symbols, con un ícono propio por cada categoría de gasto (por ejemplo, un carrito para supermercado o cubiertos para alimentación).

## 6.2. Information Architecture

En esta parte del informe se presenta la arquitectura de información planeada para los productos de Intiva (landing page y aplicación móvil): la organización de la información, las etiquetas, el sistema de búsqueda, los meta tags y la forma de navegación. Con esto buscamos que la interfaz sea fácil de entender para nuestros segmentos objetivo.

### 6.2.1. Organization Systems

**Organización visual (jerárquica)**

Se utilizará una jerarquía visual para que el usuario siga el contenido en orden de importancia. Para ello, se usarán distintos tamaños y pesos de texto, de modo que los títulos y los montos sean lo primero que se lea, y las descripciones y fechas queden en un segundo plano. Por ejemplo, en la pantalla de inicio de la aplicación se mostrará primero el saldo total, luego el estado del presupuesto y, finalmente, los movimientos recientes. En la landing page, la propuesta de valor y el botón de descarga aparecerán antes que cualquier otra información.

**Organización secuencial**

Se aplicará en los procesos que tienen pasos definidos, para que el usuario sepa en todo momento en qué paso se encuentra:

- Registro e inicio: presentación de la aplicación (onboarding) → registro o inicio de sesión → configuración inicial.
- Registro de un movimiento: tipo (gasto o ingreso) → monto → categoría → cuenta → fecha → guardar. Este proceso se diseñará para completarse en cinco pasos o menos, tal como se definió en el escenario de usabilidad del Capítulo IV.
- Creación de una meta de ahorro: nombre → monto objetivo → fecha límite → individual o familiar → confirmar.
- Recuperación de contraseña: ingresar correo → verificar código → nueva contraseña.

En la landing page, las secciones también seguirán un orden pensado para convencer al visitante: propuesta de valor → funcionalidades → beneficios → cómo funciona → planes → testimonios → equipo → llamada a la acción final.

**Esquemas de categorización**

- Por tópico: las funcionalidades de la aplicación se agruparán según el tema que atienden: Transacciones, Control de presupuesto (límites de gasto), Metas de ahorro, Grupo familiar, Notificaciones y Perfil. Los movimientos también se categorizarán por tópico (Alimentación, Transporte, Vivienda, Salud, Educación, Entretenimiento, Otros para gastos; Salario, Freelance, Negocio, Inversión, Otros para ingresos).
- Cronológico: el historial de movimientos, las notificaciones y los aportes a metas se mostrarán del más reciente al más antiguo, agrupados por día ("Hoy", "Ayer"). Los recordatorios de pago se ordenarán por la fecha de vencimiento más próxima.
- Por audiencia: se diferenciará la información según el tipo de usuario. El responsable de la economía familiar (administrador del grupo) podrá invitar integrantes, asignar roles y crear metas o límites familiares, mientras que un integrante solo verá y registrará movimientos del grupo. En la landing page, los planes estarán orientados a cada tipo de usuario (individual o familiar).
- Alfabético: se usará en listas de selección largas, como la lista de categorías (después de las más usadas) y la lista de integrantes del grupo familiar.

### 6.2.2. Labeling Systems

Para el sistema de etiquetas se usarán palabras cortas, en español y sin tecnicismos financieros, acompañadas de íconos que faciliten entender cada función a simple vista. Para la aplicación móvil se usarán los íconos de Material Symbols (https://fonts.google.com/icons), que siguen la guía de estilo de Android.

En la landing page se usarán las siguientes etiquetas:
* "Inicio"
* "Funcionalidades"
* "Beneficios"
* "Cómo funciona"
* "Planes"
* "Equipo"
* "Testimonios"
* "Iniciar Sesión"
* "Descargar App"

En la aplicación móvil, la navegación principal tendrá las siguientes etiquetas:
* "Inicio"
* "Transacciones"
* "Metas"
* "Familia"
* "Perfil"

Asimismo, se usarán etiquetas de acción como:
* "Gasto" / "Ingreso"
* "Guardar"
* "Cancelar"
* "Aportar"
* "Invitar miembro"
* "Aplicar filtros"
* "Ajustar límite"
* "Cerrar sesión"

Por último, se usarán etiquetas de estado para que el usuario identifique rápidamente la situación de sus finanzas: "A buen ritmo", "¡Cerca del límite!" y "Límite alcanzado" (límites de gasto), "En progreso" y "Meta alcanzada" (metas de ahorro), y "Admin" y "Miembro" (roles del grupo familiar).

### 6.2.3. Searching Systems

En el caso de la landing page, no se contará con una barra de búsqueda, ya que su contenido es acotado. Solo tendrá disponibles secciones claras accesibles desde el menú superior y botones de llamada a la acción para llevar al usuario a la aplicación.

En el caso de la aplicación móvil, la búsqueda se usará principalmente en el historial de transacciones, que es donde la información crece con el uso:

* Búsqueda por texto: el usuario podrá escribir el nombre o una palabra clave del movimiento (por ejemplo, "supermercado" o "luz") y se mostrará la lista de coincidencias.
* Filtros rápidos: debajo del buscador habrá opciones para mostrar "Todos", solo "Ingresos" o solo "Gastos".
* Filtros avanzados: se podrá filtrar por rango de fechas ("Este mes", "Mes pasado", "Últimos 3 meses" o un rango personalizado), tipo de movimiento y una o varias categorías.

En otras secciones, como las metas de ahorro o las notificaciones, la información se filtrará mediante pestañas (por ejemplo, metas "Personales" y "Familiares"). Si una búsqueda no tiene resultados, se mostrará un mensaje claro con la opción de limpiar los filtros.

### 6.2.4. SEO Tags and Meta Tags

Para los SEO Tags y Meta Tags se decidió implementar palabras clave que mejoren la probabilidad de encontrar Intiva en los motores de búsqueda.

**Landing Page:**

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Intiva - Administra tus finanzas en familia</title>
<meta name="description" content="Controla tus gastos, ahorra en familia y alcanza tus metas con Intiva. Simple, visual y en equipo.">
<meta name="keywords" content="finanzas personales, finanzas familiares, control de gastos, presupuesto familiar, metas de ahorro, app de ahorro, Intiva">
<meta name="author" content="Resolum">
<meta name="robots" content="index, follow">

<!-- Versiones de idioma -->
<link rel="alternate" hreflang="es" href="https://intiva.vercel.app/es/">
<link rel="alternate" hreflang="en" href="https://intiva.vercel.app/en/">

<!-- Vista previa al compartir el enlace (WhatsApp, Facebook, LinkedIn) -->
<meta property="og:title" content="Intiva - Administra tus finanzas en familia">
<meta property="og:description" content="Controla tus gastos, ahorra en familia y alcanza tus metas.">
<meta property="og:image" content="https://intiva.vercel.app/logo.png">
<meta property="og:url" content="https://intiva.vercel.app/">
<meta property="og:type" content="website">
```

Con estos tags, la landing page tendrá más oportunidades de aparecer entre las primeras opciones cuando una persona busque cómo organizar sus finanzas o las de su familia. Las etiquetas `hreflang` indicarán al buscador qué versión mostrar según el idioma del usuario, y las etiquetas Open Graph permitirán mostrar una vista previa con imagen, título y descripción cuando el enlace se comparta por WhatsApp, la aplicación más usada por los entrevistados.

**Aplicación Móvil (App Store Optimization):**

* App Title: Intiva - Finanzas en Familia
* App Subtitle: Controla tus gastos, define límites y ahorra en familia
* App Keywords: control de gastos, presupuesto, ahorro, finanzas personales, finanzas familiares, metas de ahorro
* App Category: Finanzas
* App Description: "Intiva te ayuda a tomar el control de tu dinero. Registra tus gastos e ingresos en segundos, define límites de gasto y recibe alertas antes de superarlos. Crea metas de ahorro solo o con tu familia y revisa a dónde va tu dinero desde un solo lugar. Una solución simple, visual y en equipo."

### 6.2.5. Navigation Systems

Para la landing page se usará una navegación jerárquica de una sola página, con un menú superior fijo cuyos enlaces llevarán a cada sección. "Descargar App" e "Iniciar Sesión" serán las principales llamadas a la acción, y el botón de descarga se repetirá en varias secciones para que el visitante pueda actuar desde cualquier punto de la página. En pantallas pequeñas, el menú se agrupará en un menú hamburguesa.

Para la aplicación móvil se escogieron distintos patrones conocidos de Mobile UI. A continuación se explica cómo funcionará cada uno:

* "Sticky" Fixed Navigation: se usará una barra de navegación inferior fija con los botones "Inicio", "Transacciones", "Metas", "Familia" y "Perfil", siempre al alcance del pulgar.
* Content-based Navigation: al tocar un elemento del contenido se accederá a su detalle. Por ejemplo, al tocar un movimiento se verá su información completa; al tocar una meta, su progreso y aportes; y al tocar una notificación, la pantalla relacionada con ella (por ejemplo, el límite de gasto superado).
* Floating Action Button: se usará un botón flotante "+" para la acción más frecuente de cada sección, como crear una nueva meta o un nuevo límite de gasto.
* Vertical Navigation: se usará para que los usuarios recorran listas como el historial de movimientos, las metas, los integrantes del grupo y las notificaciones.
* Tabs: se usarán pestañas para separar información relacionada dentro de una misma sección, como metas "Personales" y "Familiares".
* Swipe Navigation: en las pantallas de bienvenida (onboarding), el usuario avanzará deslizando hacia la izquierda.
* Bottom Sheets: se usarán paneles inferiores para acciones rápidas sin salir de la pantalla actual, como aplicar filtros al historial.
* Popovers: se usarán ventanas emergentes en distintos casos:
    * Confirmar la eliminación de un movimiento, una meta o una categoría.
    * Avisar que se superó un límite de gasto, con la opción de ajustarlo.
    * Aceptar o rechazar una invitación a un grupo familiar.
    * Confirmar la salida de un grupo familiar o la eliminación de un integrante.

## 6.3. Landing Page UI Design

La propuesta de TP1 adapta el diseño de Intiva desarrollado en Fundamentos de Arquitectura de Software a los requisitos de Arquitecturas de Software Emergentes. Se conserva la gestión financiera personal y familiar y se incorpora la captura asistida de gastos desde notificaciones, la sugerencia de categorías con inteligencia artificial y la automatización de alertas. Resolum corresponde a la startup e Intiva al producto.

El diseño toma como fuente de requisitos el [capítulo III](03-cha03-requirements-specification.md), especialmente US 001, US 002, US 032, US 033, TS 023 y TS 024. El [reporte del ciclo anterior](https://docs.google.com/document/d/1utbegMuuFidUGZj1odoYluc3qPa8piI2bcIJNg168pM/edit) se utiliza como antecedente, mientras que los nuevos criterios de aceptación se obtienen de la rama `develop` del informe actual.

Los entregables editables están en el [archivo Figma de Intiva](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2005-721). La página **TP1 · IA y automatización** contiene los wireframes y wireflows nuevos; **Page 1** conserva la base del ciclo anterior y la landing actualizada. Esta sección documenta diseño propuesto, sin atribuir a las tecnologías una implementación o una validación con usuarios que todavía no se ha realizado.

### 6.3.1. Landing Page Wireframe

El wireframe organiza la comunicación de valor desde el problema hasta la acción de descargar la aplicación. La propuesta central es **“Menos registro, más control en familia”**: la automatización reduce el esfuerzo de registro y la IA ayuda a clasificar, manteniendo la decisión final en el usuario. La captura mediante notificaciones se presenta como una función opcional de Android, coherente con TS 023.

| Bloque | Contenido y propósito | Trazabilidad |
| --- | --- | --- |
| Navegación | Acceso a inicio, funcionalidades, funcionamiento, equipo y planes. | US 001, US 002 |
| Hero y llamadas a la acción | Propuesta de valor, descarga en Google Play y acceso a la explicación de funcionamiento. | US 001, US 002 |
| Problema | Tiempo dedicado al registro, gastos sin clasificar y vencimientos olvidados. | US 002 |
| Funcionalidades | Captura asistida, categorías con confianza visible y recordatorios. | US 032, US 033, US 030 |
| Cómo funciona | Crear cuenta, autorizar fuentes y revisar/confirmar movimientos; espacio previsto para video explicativo. | US 002, TS 023, US 032 |
| Privacidad y control | Fuentes financieras autorizadas, revocación del permiso y alternativa manual. | TS 023 |
| Equipo y planes | Presentación del equipo actual y comparación de opciones de suscripción. | US 001, US 008 |
| Escenarios y cierre | Ejemplos académicos de uso familiar, segunda llamada a la acción y enlaces legales. | US 001, US 002 |

**Desktop.** La vista de 1440 px ordena las secciones en una lectura vertical, con acciones distinguibles y bloques independientes que facilitan la posterior implementación adaptable.

![Wireframe desktop de la landing de Intiva](../assets/img/cap06/landing-wireframe-desktop.png)

*Figura 6.3.1-A. Wireframe de la landing para escritorio. [Abrir frame editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2007-675).*

**Mobile.** La vista de 390 px reorganiza los contenidos en una columna, reduce la navegación a un menú y mantiene visibles las acciones de descarga y la explicación del control sobre la automatización.

![Wireframe móvil de la landing de Intiva](../assets/img/cap06/landing-wireframe-mobile.png)

*Figura 6.3.1-B. Wireframe de la landing móvil. [Abrir frame editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2007-725).*

Las áreas de equipo, video y planes del wireframe indican contenido que deberá completarse o validarse con el equipo. Los escenarios académicos no representan testimonios de clientes reales. La distribución de las nuevas funciones por plan no queda definida por estas pantallas.

### 6.3.2. Landing Page Mock-up

El mock-up adapta el frame existente **Intiva Landing Page (Desktop)**. Se conserva su composición y lenguaje visual, con fondos claros, acentos violetas, títulos en Plus Jakarta Sans y textos de apoyo en Inter. Las modificaciones actualizan el hero, las funcionalidades, los pasos de uso y los escenarios para explicar la captura de notificaciones y la clasificación asistida.

La comunicación evita presentar la captura como sincronización bancaria directa: una notificación reconocida produce una sugerencia pendiente y el saldo cambia después de la confirmación. La IA propone una categoría que el usuario puede aceptar o corregir; ante baja confianza se solicita confirmación de “Otros”. Las alertas facilitan el seguimiento de vencimientos, sin efectuar pagos por cuenta del usuario.

![Mock-up actualizado de la landing de Intiva](../assets/img/cap06/landing-mockup.png)

*Figura 6.3.2-A. Mock-up de la landing adaptado para TP1. [Abrir frame editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=3-2).*

Los precios y nombres de integrantes conservados en el diseño previo son referencias visuales y deben conciliarse con los planes y la composición del equipo actual antes de publicar una landing funcional. El mock-up no acredita disponibilidad comercial de las nuevas funcionalidades.

## 6.4. Applications UX/UI Design

### 6.4.1. Applications Wireframes

Los doce wireframes complementan las pantallas existentes de registro, movimientos, cuentas, metas, grupo familiar y notificaciones. La ampliación se concentra en los estados nuevos que exige EP 010 y en las alertas automatizadas. Las pantallas utilizan capas editables, contenedores con disposición automática y botones como instancias reutilizables. Se mantiene Manrope para encabezados de la aplicación e Inter para el contenido.

| ID | Pantalla | Decisión o estado representado | Requisito |
| --- | --- | --- | --- |
| WF01 | Captura automática | Explicar permiso opcional; configurar acceso en Android o continuar manualmente. | TS 023 |
| WF02 | Fuentes autorizadas | Seleccionar aplicaciones financieras y desactivar captura. Los nombres mostrados son ejemplos de fuentes por validar. | TS 023 |
| WF03 | Por confirmar | Listar una sugerencia con monto, comercio, fuente y estado pendiente; mantener el saldo actual. | US 032, escenario 1 |
| WF04 | Revisar gasto | Revisar y corregir datos; aceptar/cambiar categoría, confirmar o descartar. | US 032, escenarios 2–3; US 033 |
| WF05 | Elegir categoría | Sustituir la categoría sugerida y registrar la corrección para futuras sugerencias. | US 033, escenario 3 |
| WF06 | Confirma la categoría | Comercio desconocido o baja confianza: proponer Otros y pedir confirmación explícita. | US 033, escenario 4 |
| WF07 | Gasto registrado | Comunicar registro definitivo y saldo actualizado. | US 032, escenario 2 |
| WF08 | Registro manual | Continuar cuando se deniega/revoca el permiso o no se reconoce el formato; solicitar sugerencia de IA desde el registro manual. | TS 023; US 032, escenario 4; US 033 |
| WF09 | Recordatorios | Consultar avisos y acceder a su detalle; representar agrupación de alertas. | US 030, TS 024 |
| WF10 | Detalle de recordatorio | Revisar monto, vencimiento y estado; distinguir marcar como pagado de ejecutar un pago. | US 030 |
| WF11 | Sugerencia descartada | Confirmar que el descarte no registra movimiento ni modifica saldo. | US 032, escenario 3 |
| WF12 | No pudimos guardar | Mantener datos y ofrecer reintento/retorno sin mostrar un éxito no confirmado. | Estado adicional de recuperación |

**Permisos y captura.** La primera composición cubre el consentimiento, la selección de fuentes, la bandeja de pendientes y la revisión de un gasto detectado.

![Wireframes WF01 a WF04 de captura asistida](../assets/img/cap06/wireframes-capture.png)

*Figura 6.4.1-A. WF01–WF04. [Abrir composición editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2006-594).*

**IA y resultados.** La segunda composición incluye corrección, baja confianza, registro definitivo y continuidad mediante registro manual. El 92% mostrado ilustra cómo comunicar la confianza; no es una medición de precisión del modelo ni define un umbral técnico.

![Wireframes WF05 a WF08 de categorías y resultados](../assets/img/cap06/wireframes-ai.png)

*Figura 6.4.1-B. WF05–WF08. [Abrir composición editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2006-704).*

**Alertas y alternativas.** La tercera composición representa los recordatorios, su detalle, el descarte y la recuperación ante un fallo al guardar.

![Wireframes WF09 a WF12 de recordatorios y estados alternativos](../assets/img/cap06/wireframes-alerts.png)

*Figura 6.4.1-C. WF09–WF12. [Abrir composición editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2006-806).*

Los montos, comercios, fuentes y fechas son datos de demostración. En el ejemplo de confirmación, S/ 1,240.00 − S/ 48.90 = S/ 1,191.10. El mismo saldo inicial permanece en los ejemplos de descarte y error. Los campos representados describen la estructura del formulario; la interacción completa, el teclado, las validaciones de entrada y los estados de carga se concretarán en los mock-ups y prototipos de aplicación a cargo del equipo.

### 6.4.2. Applications Wireflow Diagrams

Los wireflows relacionan representaciones de pantallas con acciones y resultados. Las flechas indican la secuencia principal y las notas de cada composición especifican las ramas alternativas. Son diagramas de navegación para diseño; no constituyen un prototipo interactivo terminado.

**F01. Activación y confirmación RPA.** El usuario configura el acceso, selecciona fuentes, abre la bandeja y revisa el gasto. Confirmar registra el movimiento y actualiza el saldo. Si deniega o revoca el permiso, utiliza WF08; las notificaciones ajenas a fuentes autorizadas se descartan sin guardar contenido y los formatos no reconocidos no crean sugerencias.

![Wireflow de activación y confirmación RPA](../assets/img/cap06/wireflow-rpa.png)

*Figura 6.4.2-A. F01. [Abrir wireflow editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2007-758).*

**F02. Aceptación y corrección de categoría IA.** La sugerencia se solicita desde el registro manual o acompaña al gasto detectado. El usuario acepta la categoría o abre WF05 para reemplazarla. Ante baja confianza, WF06 solicita confirmar Otros o elegir otra categoría. Tras aplicar la elección se regresa a revisión y se confirma el gasto.

![Wireflow de aceptación y corrección de categoría IA](../assets/img/cap06/wireflow-ai.png)

*Figura 6.4.2-B. F02. [Abrir wireflow editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2007-847).*

**F03. Recordatorios y continuidad de alertas.** El usuario abre un recordatorio, consulta su detalle y vuelve a las alertas. La nota técnica relaciona esta experiencia con TS 024: Communications invoca n8n para formato, agrupación y canal; si el webhook falla, envía el aviso de respaldo directamente por Firebase Cloud Messaging, sin la agrupación del flujo. La decisión de respaldo ocurre internamente y no agrega una tarea de configuración al usuario.

![Wireflow de recordatorios y continuidad de alertas](../assets/img/cap06/wireflow-alerts.png)

*Figura 6.4.2-C. F03. [Abrir wireflow editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2007-920).*

| Condición | Transición | Resultado esperado |
| --- | --- | --- |
| Permiso concedido | WF01 → ajustes Android → WF02 → WF03 | Captura habilitada para fuentes autorizadas. |
| Permiso denegado o revocado | WF01/WF02 → WF08 | Registro manual disponible. |
| Confirmación de gasto | WF03 → WF04 → WF07 | Registro definitivo y saldo actualizado. |
| Descarte | WF04 → WF11 → WF03 | Sin movimiento ni cambio de saldo. |
| Categoría aceptada | WF04 → confirmar → WF07 | Se guarda la categoría sugerida. |
| Categoría corregida | WF04 → WF05 → WF04 → WF07 | Se guarda la elección y se registra la corrección. |
| Baja confianza | WF08/WF04 → WF06 → WF04 → WF07 | Otros requiere aceptación explícita; se permite reemplazarlo vía WF05. |
| Error al guardar | WF04 → WF12 → reintentar o WF04 | Sin éxito anticipado; datos disponibles para recuperación. |
| Recordatorio | Notificación → WF09 → WF10 → WF09 | Detalle accesible tanto con envío normal como con respaldo. |

La numeración de estas secciones sigue el índice vigente del repositorio: **6.4.2** corresponde a Wireflow Diagrams, **6.4.3** a Applications Mock-ups y **6.4.4** a Applications User Flow Diagrams. Las secciones de estilo, arquitectura de información, mock-ups de aplicación y prototipado quedan bajo las responsabilidades acordadas con los otros integrantes.

# Capítulo VI: Solution UX Design

En este capítulo se desarrolla el diseño de la solución planteada para Intiva, la propuesta de Balanza para la gestión de ingresos, gastos y ahorros personales y familiares. Para ello, se definen las guías de estilo y la arquitectura de información que se seguirán en la landing page, la aplicación móvil y la aplicación web, para que el diseño sea coherente y fácil de usar para nuestros segmentos objetivo.

## 6.1. Style Guidelines

En esta sección se explican las guías de estilo para la landing page, la aplicación móvil y la aplicación web. Con ellas buscamos que los tres productos se vean coherentes entre sí y que los usuarios reconozcan el estilo de Intiva.

### 6.1.1. General Style Guidelines

**Branding**

*Brand Overview*

Intiva es una plataforma digital que ayudará a las personas y a las familias a registrar sus ingresos y gastos, controlar su presupuesto mediante límites de gasto y planificar metas de ahorro de forma individual o compartida. Nace de una problemática identificada en las entrevistas: la mayoría de usuarios lleva sus finanzas en hojas de Excel, notas del celular o revisando manualmente sus billeteras digitales (Yape, Plin, apps bancarias), lo que vuelve el registro tedioso y deja la información fragmentada entre los integrantes del hogar. Intiva busca centralizar esa información, presentarla de forma visual y acompañar al usuario con alertas y recordatorios para que tome mejores decisiones financieras. Para reducir el registro manual, la aplicación podrá detectar gastos a partir de las notificaciones de las apps financieras y sugerir su categoría con inteligencia artificial, pero siempre será el usuario quien revise y confirme cada movimiento. Su eslogan, "Controla tus finanzas, transforma tu vida", resume esa promesa, y en la landing page se comunica con el mensaje "Menos registro, más control en familia".

*Brand Name*

El nombre "Intiva" se relaciona con la idea de manejar las finanzas de forma intuitiva, ya que buscamos que ahorrar y organizar las finanzas sea algo sencillo e intuitivo para cualquier persona, sin necesidad de conocimientos financieros previos. Por eso, el nombre representa una herramienta cercana que ayuda a controlar los gastos y alcanzar metas de ahorro. Además, es un nombre corto, moderno y fácil de recordar y de pronunciar tanto en español como en inglés, lo que permitirá usarlo sin cambios en las dos versiones de idioma de la landing page y como nombre de la aplicación en Google Play.

*Logo*

A continuación, se muestra el logo diseñado para Intiva:

<img src="../assets/img/cap06/logo-intiva.png" width="200" alt="Logo de Intiva"/>

*Logo de Intiva. Fuente: elaboración propia.*

El logo de Intiva está compuesto por un isotipo y un logotipo. El isotipo es un rombo blanco de esquinas redondeadas que contiene un cuadrado índigo con un rayo, símbolo que representa la energía y la rapidez con la que la aplicación permitirá tomar el control del dinero: el registro y la consulta del presupuesto son tareas principales del producto. El tiempo de ejecución se evaluará mediante las pruebas de usabilidad definidas en QAS-01. El logotipo "Intiva" se escribe en una tipografía sans-serif de trazo grueso, que transmite solidez y confianza. Se presenta sobre el color índigo principal de la marca y se acompaña del eslogan. En espacios reducidos, como el favicon, la barra de navegación de la landing page o la barra lateral de la aplicación web, se usará una versión simplificada: un cuadrado índigo con la inicial de la marca.

**Typography**

Para la tipografía escogimos fuentes de Google Fonts, cada una para un tipo de texto distinto. Así es más fácil distinguir qué es más importante en cada pantalla.

Para los títulos y encabezados de la aplicación móvil y de la aplicación web usaremos Manrope (Headline). Es una fuente moderna y algo compacta, por lo que los títulos se ven bien sin ocupar mucho espacio en pantallas pequeñas.

En la landing page, los títulos usarán Plus Jakarta Sans. Tiene trazos más gruesos en sus pesos altos, por lo que funciona bien en titulares grandes, que son lo primero que ve un visitante.

Para los textos de cuerpo, descripciones, formularios y botones usaremos Inter (Body) en los tres productos. Esta fuente fue creada para pantallas y se lee bien incluso en tamaños pequeños, lo que ayuda en las listas de movimientos y en los mensajes de alerta.

Para las etiquetas y los montos de dinero usaremos Space Grotesk (Label). Escogimos una fuente aparte para los números porque los montos son el dato más importante en una aplicación de finanzas y queremos que el usuario los encuentre rápido.

| Estilo | Fuente | Uso | Tamaño (web / app) | Peso |
| --- | --- | --- | --- | --- |
| Display | Plus Jakarta Sans (landing) / Manrope (app y web) | Titular principal de la landing y saldo total | 64 px / 32 sp | ExtraBold / Bold |
| Headline | Plus Jakarta Sans (landing) / Manrope (app y web) | Títulos de sección y de pantalla | 36 a 48 px / 24 sp | Bold |
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

Además, usaremos un rojo (`#BA1A1A`) para los gastos, los límites superados y la acción de eliminar. Cada color tiene una escala de tonos, de oscuro a claro, que nos permite crear fondos suaves, estados de botones y un modo oscuro. El contraste debe comprobarse para cada combinación de texto, fondo y estado; la existencia de una escala de tonos no garantiza por sí sola su legibilidad.

A continuación se presenta la guía de estilo de Intiva, que reúne la paleta de colores, las tipografías y algunos componentes base (botones, buscador, barras de progreso, barra de navegación y botones de íconos):

![Guía de estilo de Intiva](../assets/img/cap06/style-guide-intiva.png)

*Guía de estilo de Intiva: paleta de colores, tipografías y componentes base. Fuente: elaboración propia en Figma.*

También usaremos colores para indicar el estado de las finanzas, de modo que el usuario lo entienda sin leer el detalle: verde cuando un límite de gasto va bien, ámbar cuando está cerca de alcanzarse y rojo cuando se supera. Los gastos detectados automáticamente que todavía no se confirman se mostrarán en tonos neutros, para diferenciarlos de los movimientos ya registrados. Para no depender solo del color, cada estado irá acompañado de un texto, y los montos se mostrarán con signo ("+" para ingresos y "−" para gastos).

**Spacing**

El espaciado se basará en múltiplos de 4 y 8 para que la información se vea ordenada. Los valores cambian según el producto:

Para Landing Page y aplicación web:
- Button padding:
    - Vertical: 16px
    - Horizontal: 32px
- Input fields:
    - Altura: 48px
    - Espacio entre campos: 16px
- Ancho máximo del contenido: 1280px
- Margen lateral: 24px (móvil) a 32px (escritorio)
- Margin entre secciones de la landing: 96px (móvil) a 128px (escritorio)
- Espacio entre título y subtítulo de sección: 24px
- Espacio entre tarjetas del panel web: 24px

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

Usaremos un tono cercano y sencillo. En las entrevistas vimos que los términos financieros técnicos confunden a los usuarios, por lo que evitaremos la jerga y trataremos al usuario de "tú" (por ejemplo, "Aquí está el resumen de tus finanzas hoy"). Cuando el usuario logre algo, se lo haremos saber ("¡Cumpliste tu meta de ahorro!"), y las alertas solo informarán lo que pasó, sin regañar ("Has superado tu presupuesto en Entretenimiento"), junto con una opción para resolverlo. Al hablar de la captura automática y de la IA seremos claros sobre lo que hacen y lo que no: por ejemplo, "Este gasto todavía no modifica tu saldo" o "La confianza es orientativa; puedes cambiar la categoría". Queremos que el usuario sienta que Intiva lo ayuda con sus gastos, que no lo juzga y que él mantiene el control de su información.

### 6.1.2. Web, Mobile & Devices Style Guidelines

Intiva contempla una landing informativa, una aplicación móvil Android para el registro diario y una aplicación web para consultar gráficos y reportes. Las entrevistas mencionan el uso de celulares y computadoras. La elección de Android también responde a TS 007 y al acceso a notificaciones requerido por TS 023; no se fundamenta en porcentajes de dispositivos cuya base de cálculo aún no está documentada.

**Landing Page**

- Diseño responsive con enfoque *mobile first*, para permitir el acceso desde el celular, por ejemplo al compartir el enlace por WhatsApp.
- Puntos de quiebre: móvil (< 768 px), tablet (768 a 1023 px) y escritorio (≥ 1024 px). En móvil, el contenido pasará a una sola columna y el menú superior se convertirá en un menú hamburguesa.
- Usará fondos claros con acentos índigo, y el botón principal será de color Secondary (lima) para que destaque; el botón secundario será transparente con borde.
- Estará disponible en español e inglés, con un selector de idioma en la barra de navegación.
- Todos los elementos interactivos tendrán un contorno visible al recibir foco con el teclado, y las imágenes tendrán texto alternativo.

**Aplicación móvil (Android)**

- Seguirá los lineamientos de Material Design 3, para que la aplicación se sienta natural para los usuarios de Android, utilizando sus componentes: barra superior, barra de navegación inferior, botón flotante, chips, paneles inferiores (*bottom sheets*) y diálogos.
- Las dimensiones se definirán en `dp` y los textos en `sp`, para respetar el tamaño de letra configurado por el usuario en su teléfono.
- Se diseñará sobre un ancho de referencia de 360 a 390 dp, como referencia de diseño adaptable; la distribución se verificará en distintos tamaños de pantalla.
- Los botones de acción principal ocuparán todo el ancho de la pantalla y estarán en la parte inferior, para alcanzarlos fácilmente con el pulgar.
- Para registrar montos se usará un teclado numérico propio con dígitos grandes, evitando abrir el teclado del sistema.
- El permiso para leer notificaciones se pedirá con una pantalla propia que explique para qué sirve, antes de llevar al usuario a los ajustes de Android, y siempre habrá una opción para continuar con el registro manual.
- Se usarán los íconos de Material Symbols, con un ícono propio por cada categoría de gasto (por ejemplo, un carrito para supermercado o cubiertos para alimentación).

**Aplicación web**

- Estará pensada para laptops y computadoras de escritorio, con una barra lateral fija de navegación y un área de contenido organizada en tarjetas y gráficos.
- En pantallas menores a 768 px, la barra lateral se reemplazará por una barra de navegación inferior con íconos.
- Usará las mismas fuentes y colores de la aplicación móvil, para que el usuario reconozca la información al pasar de un dispositivo a otro. Los gráficos usarán el índigo y el lima como colores principales de sus series.
- Contará con modo claro y modo oscuro, y permitirá cambiar el idioma entre español e inglés.
- Se usarán los íconos de PrimeIcons, que acompañan a la librería de componentes PrimeVue.

## 6.2. Information Architecture

En esta parte del informe se presenta la arquitectura de información planeada para los productos de Intiva (landing page, aplicación móvil y aplicación web): la organización de la información, las etiquetas, el sistema de búsqueda, los meta tags y la forma de navegación. Con esto buscamos que la interfaz sea fácil de entender para nuestros segmentos objetivo.

### 6.2.1. Organization Systems

**Organización visual (jerárquica)**

Se utilizará una jerarquía visual para que el usuario siga el contenido en orden de importancia. Para ello, se usarán distintos tamaños y pesos de texto, de modo que los títulos y los montos sean lo primero que se lea, y las descripciones y fechas queden en un segundo plano. Por ejemplo, en la pantalla de inicio de la aplicación móvil se mostrará primero el saldo total, luego el estado del presupuesto y, finalmente, los movimientos recientes. En el panel de la aplicación web, los indicadores principales (balance total, ingresos, gastos y ahorro del mes) aparecerán arriba y los gráficos de detalle debajo. En la landing page, la propuesta de valor y el botón de descarga aparecerán antes que cualquier otra información.

**Organización secuencial**

Se aplicará en los procesos que tienen pasos definidos, para que el usuario sepa en todo momento en qué paso se encuentra:

- Registro e inicio: presentación de la aplicación (onboarding) → registro o inicio de sesión → configuración inicial.
- Registro manual de un movimiento: tipo (gasto o ingreso) → monto → categoría → cuenta → fecha → guardar. Este proceso se diseñará para completarse en cinco pasos o menos, tal como se definió en el escenario de usabilidad del Capítulo IV.
- Captura asistida de un gasto: activar la captura → elegir las apps financieras autorizadas → revisar el gasto detectado → aceptar o cambiar la categoría sugerida → confirmar o descartar. El saldo solo cambiará después de confirmar.
- Creación de una meta de ahorro: nombre → monto objetivo → fecha límite → individual o familiar → confirmar.
- Recuperación de contraseña: ingresar correo → verificar código → nueva contraseña.
- Generación de un reporte en la aplicación web: tipo de reporte → período → integrantes incluidos → descargar.

En la landing page, las secciones también seguirán un orden pensado para convencer al visitante: propuesta de valor → problema que resolvemos → funcionalidades → cómo funciona → privacidad y control → equipo → planes → escenarios de uso → llamada a la acción final.

**Esquemas de categorización**

- Por tópico: las funcionalidades de la aplicación móvil se agruparán según el tema que atienden: Transacciones, Captura asistida, Control de presupuesto (límites de gasto), Metas de ahorro, Grupo familiar, Notificaciones y Perfil. La aplicación web se dividirá en Panel y Reportes. Los movimientos también se categorizarán por tópico (Alimentación, Transporte, Vivienda, Salud, Educación, Entretenimiento, Otros para gastos; Salario, Freelance, Negocio, Inversión, Otros para ingresos).
- Cronológico: el historial de movimientos, las notificaciones y los aportes a metas se mostrarán del más reciente al más antiguo, agrupados por día ("Hoy", "Ayer"). Los recordatorios de pago se ordenarán por la fecha de vencimiento más próxima.
- Por audiencia: se diferenciará la información según el tipo de usuario. El responsable de la economía familiar (administrador del grupo) podrá invitar integrantes, asignar roles y crear metas o límites familiares, mientras que un integrante solo verá y registrará movimientos del grupo. Además, la aplicación web estará orientada sobre todo al responsable de la economía familiar, que es quien revisa los reportes del hogar.
- Por estado: los gastos detectados automáticamente se mantendrán separados en una lista de pendientes ("Por confirmar") hasta que el usuario los revise, y no se mezclarán con el historial de movimientos ya registrados.
- Alfabético: se usará en listas de selección largas, como la lista de categorías (después de las más usadas) y la lista de integrantes del grupo familiar.

### 6.2.2. Labeling Systems

Para el sistema de etiquetas se usarán palabras cortas, en español y sin tecnicismos financieros, acompañadas de íconos que faciliten entender cada función a simple vista. Para la aplicación móvil se usarán los íconos de Material Symbols (https://fonts.google.com/icons), que siguen la guía de estilo de Android, y para la aplicación web, los de PrimeIcons.

En la landing page se usarán las siguientes etiquetas:
* "Inicio"
* "Funcionalidades"
* "Cómo funciona"
* "Equipo"
* "Planes"
* "Descargar en Google Play"
* "Ver cómo funciona"
* "Descargar app"
* "Términos de Servicio", "Privacidad" y "Ayuda" (pie de página)

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

Para la captura asistida y la categorización con IA se usarán etiquetas que dejen claro que el usuario decide:
* "Captura automática"
* "Fuentes autorizadas"
* "Por confirmar"
* "Revisar gasto"
* "Confirmar gasto" / "Descartar sugerencia"
* "Aceptar categoría" / "Cambiar categoría"
* "Continuar manualmente"

En la aplicación web se usarán las etiquetas "Panel", "Reportes", "Descargar reporte", "Notificaciones" y "Cerrar sesión".

Por último, se usarán etiquetas de estado para que el usuario identifique rápidamente la situación de sus finanzas: "A buen ritmo", "¡Cerca del límite!" y "Límite alcanzado" (límites de gasto), "En progreso" y "Meta alcanzada" (metas de ahorro), "Pendiente de confirmación" y "Categoría sugerida por IA" junto con su nivel de confianza (captura asistida), y "Admin" y "Miembro" (roles del grupo familiar).

### 6.2.3. Searching Systems

En el caso de la landing page, no se contará con una barra de búsqueda, ya que su contenido es acotado. Solo tendrá disponibles secciones claras accesibles desde el menú superior y botones de llamada a la acción para llevar al usuario a la aplicación.

En el caso de la aplicación móvil, la búsqueda se usará principalmente en el historial de transacciones, que es donde la información crece con el uso:

* Búsqueda por texto: el usuario podrá escribir el nombre o una palabra clave del movimiento (por ejemplo, "supermercado" o "luz") y se mostrará la lista de coincidencias.
* Filtros rápidos: debajo del buscador habrá opciones para mostrar "Todos", solo "Ingresos" o solo "Gastos".
* Filtros avanzados: se podrá filtrar por rango de fechas ("Este mes", "Mes pasado", "Últimos 3 meses" o un rango personalizado), tipo de movimiento y una o varias categorías.

En otras secciones, como las metas de ahorro o las notificaciones, la información se filtrará mediante pestañas (por ejemplo, metas "Personales" y "Familiares"). Si una búsqueda no tiene resultados, se mostrará un mensaje claro con la opción de limpiar los filtros.

En la aplicación web no habrá búsqueda por texto, ya que muestra información resumida. En su lugar, el usuario podrá filtrar los gráficos por período (1 mes, 6 meses o 1 año) y configurar los reportes por tipo (general, ingresos, gastos o ahorros), período e integrantes del grupo familiar.

### 6.2.4. SEO Tags and Meta Tags

Los metadatos propuestos describen el contenido de la landing y configuran su presentación en buscadores y redes sociales. Su aplicación deberá verificarse en el sitio desplegado; no garantiza una posición determinada en los resultados de búsqueda.

**Landing Page:**

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Intiva - Menos registro, más control en familia</title>
<meta name="description" content="Registra tus gastos con ayuda de las notificaciones de tus apps financieras, recibe sugerencias de categoría con IA y organiza las finanzas de tu familia con Intiva.">
<meta name="author" content="Balanza">
<meta name="robots" content="index, follow">

<!-- URLs de diseño: sustituir por las rutas definitivas verificadas al desplegar -->
<!-- Versiones de idioma -->
<link rel="alternate" hreflang="es" href="https://intiva.vercel.app/es/">
<link rel="alternate" hreflang="en" href="https://intiva.vercel.app/en/">

<!-- Vista previa al compartir el enlace (WhatsApp, Facebook, LinkedIn) -->
<meta property="og:title" content="Intiva - Menos registro, más control en familia">
<meta property="og:description" content="Captura asistida de gastos, categorías con IA y alertas para organizar las finanzas de tu familia.">
<meta property="og:image" content="https://intiva.vercel.app/logo.png">
<meta property="og:url" content="https://intiva.vercel.app/">
<meta property="og:type" content="website">
```

El título y la descripción permiten comunicar el contenido de la página; Google puede utilizar la descripción en el fragmento de búsqueda. La etiqueta `keywords` no se incluye porque Google no la utiliza para indexación ni ranking. `hreflang` identifica las versiones de idioma y Open Graph define la vista previa al compartir. Las URL y la imagen del ejemplo deberán corresponder a recursos publicados antes de su uso. [Referencia: Google Search Central](https://developers.google.com/search/docs/crawling-indexing/special-tags).

**Aplicación web:**

La aplicación web contiene información financiera privada, por lo que no buscará aparecer en los buscadores. Solo la pantalla de inicio de sesión tendrá un título y una descripción, y las páginas a las que se entra con sesión iniciada usarán `<meta name="robots" content="noindex, nofollow">` como instrucción de indexación. La privacidad depende de la autenticación y autorización del backend; `noindex` no es un control de acceso. [Referencia: Google Search Central](https://developers.google.com/search/docs/fundamentals/get-started-developers).

**Aplicación Móvil (App Store Optimization):**

* App Title: Intiva - Finanzas en Familia
* Mensaje breve propuesto para la ficha de Google Play: Registra gastos más rápido, define límites y ahorra en familia
* Términos para redactar la ficha de Google Play: control de gastos, registro automático de gastos, categorías con IA, presupuesto, ahorro, finanzas familiares, metas de ahorro
* App Category: Finanzas
* App Description: "Intiva te ayuda a tomar el control de tu dinero. Detecta tus gastos a partir de las notificaciones de tus apps financieras y te sugiere su categoría, para que solo tengas que revisarlos y confirmarlos. Define límites de gasto y recibe alertas antes de superarlos. Crea metas de ahorro solo o con tu familia y revisa a dónde va tu dinero desde un solo lugar."

### 6.2.5. Navigation Systems

Para la landing page se usará una navegación jerárquica de una sola página, con un menú superior fijo cuyos enlaces ("Inicio", "Funcionalidades", "Cómo funciona", "Equipo" y "Planes") llevarán a cada sección. "Descargar en Google Play" será la principal llamada a la acción y se repetirá al final de la página para que el visitante pueda actuar desde cualquier punto. En pantallas pequeñas, el menú se agrupará en un menú hamburguesa.

Para la aplicación móvil se escogieron distintos patrones conocidos de Mobile UI. A continuación se explica cómo funcionará cada uno:

* "Sticky" Fixed Navigation: se usará una barra de navegación inferior fija con los botones "Inicio", "Transacciones", "Metas", "Familia" y "Perfil", siempre al alcance del pulgar.
* Content-based Navigation: al tocar un elemento del contenido se accederá a su detalle. Por ejemplo, al tocar un movimiento se verá su información completa; al tocar una meta, su progreso y aportes; al tocar un gasto detectado, la pantalla para revisarlo; y al tocar una notificación, la pantalla relacionada con ella (por ejemplo, el límite de gasto superado o el detalle de un recordatorio).
* Floating Action Button: se usará un botón flotante "+" para la acción más frecuente de cada sección, como crear una nueva meta o un nuevo límite de gasto.
* Vertical Navigation: se usará para que los usuarios recorran listas como el historial de movimientos, los gastos por confirmar, las metas, los integrantes del grupo y las notificaciones.
* Tabs: se usarán pestañas para separar información relacionada dentro de una misma sección, como metas "Personales" y "Familiares".
* Swipe Navigation: en las pantallas de bienvenida (onboarding), el usuario avanzará deslizando hacia la izquierda.
* Bottom Sheets: se usarán paneles inferiores para acciones rápidas sin salir de la pantalla actual, como aplicar filtros al historial o elegir otra categoría para un gasto.
* Popovers: se usarán ventanas emergentes en distintos casos:
    * Confirmar la eliminación de un movimiento, una meta o una categoría.
    * Avisar que se superó un límite de gasto, con la opción de ajustarlo.
    * Pedir confirmación cuando la IA no esté segura de la categoría y proponga "Otros".
    * Confirmar que se descarta un gasto detectado, sin registrar ningún movimiento.
    * Aceptar o rechazar una invitación a un grupo familiar.
    * Confirmar la salida de un grupo familiar o la eliminación de un integrante.

Para la aplicación web se usará una barra lateral fija con las secciones "Panel" y "Reportes" y la opción "Cerrar sesión". En la barra superior estarán el título de la página, el acceso a las notificaciones, el cambio de idioma y el cambio entre modo claro y oscuro.

## 6.3. Landing Page UI Design

Para TP1 actualizamos el diseño de Intiva con tres funciones: captura de gastos desde notificaciones financieras, sugerencia de categorías mediante inteligencia artificial y recordatorios automatizados. Estas funciones se integran al registro de movimientos y al control de las finanzas personales y familiares.

El diseño toma como fuente de requisitos el [capítulo III](03-cha03-requirements-specification.md), especialmente US 001, US 002, US 032, US 033, TS 023 y TS 024. Los criterios de aceptación corresponden al informe actual en la rama `develop`.

Los diseños se encuentran en el [archivo Figma de Intiva](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2005-721). En el archivo, **Page 1** contiene la información general de la aplicación: la guía de estilo, las pantallas base y los flujos de usuario existentes (onboarding, perfil y cuentas, transacciones, control de presupuesto, metas de ahorro, grupo familiar, y notificaciones y dashboard). La sección **TP1 · IA y automatización** contiene lo nuevo de esta entrega: la landing actualizada, los wireframes WF01 a WF12 y los wireflows F01 a F03. Las pantallas muestran el comportamiento previsto para la aplicación en esta etapa de diseño.

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

El wireframe reserva espacios para presentar al equipo, explicar el uso de la aplicación mediante un video y comparar los planes. Los casos de uso ilustran situaciones de las finanzas familiares. La asignación de las nuevas funciones a cada plan se definirá con las condiciones de suscripción.

### 6.3.2. Landing Page Mock-up

El mock-up adapta el frame existente **Intiva Landing Page (Desktop)**. Se conserva su composición y lenguaje visual, con fondos claros, acentos violetas, títulos en Plus Jakarta Sans y textos de apoyo en Inter. Las modificaciones actualizan el hero, las funcionalidades, los pasos de uso y los escenarios para explicar la captura de notificaciones y la clasificación asistida.

La comunicación evita presentar la captura como sincronización bancaria directa: una notificación reconocida produce una sugerencia pendiente y el saldo cambia después de la confirmación. La IA propone una categoría que el usuario puede aceptar o corregir; ante baja confianza se solicita confirmación de “Otros”. Las alertas facilitan el seguimiento de vencimientos, sin efectuar pagos por cuenta del usuario.

![Mock-up actualizado de la landing de Intiva](../assets/img/cap06/landing-mockup.png)

*Figura 6.3.2-A. Mock-up de la landing adaptado para TP1. [Abrir frame editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=3-2).*

El mock-up conserva los contenidos de precios y equipo del diseño base. Estos contenidos están pendientes de actualización para su publicación; la adaptación de TP1 se concentra en presentar las nuevas funcionalidades.

## 6.4. Applications UX/UI Design

### 6.4.1. Applications Wireframes

Los doce wireframes complementan las pantallas existentes de registro, movimientos, cuentas, metas, grupo familiar y notificaciones. La ampliación se concentra en los estados nuevos que exige EP 010 y en las alertas automatizadas. La distribución mantiene los encabezados, campos y acciones en el mismo orden para facilitar la revisión de cada movimiento. Se mantiene Manrope para encabezados de la aplicación e Inter para el contenido.

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

**IA y resultados.** La segunda composición incluye corrección, baja confianza, registro definitivo y continuidad mediante registro manual. El valor de confianza del 92% es un dato de ejemplo para el diseño. El umbral de baja confianza y la forma de obtener ese valor deberán definirse y comprobarse durante la implementación del clasificador.

![Wireframes WF05 a WF08 de categorías y resultados](../assets/img/cap06/wireframes-ai.png)

*Figura 6.4.1-B. WF05–WF08. [Abrir composición editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2006-704).*

**Alertas y alternativas.** La tercera composición representa los recordatorios, su detalle, el descarte y la recuperación ante un fallo al guardar.

![Wireframes WF09 a WF12 de recordatorios y estados alternativos](../assets/img/cap06/wireframes-alerts.png)

*Figura 6.4.1-C. WF09–WF12. [Abrir composición editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2006-806).*

Los montos, comercios, fuentes y fechas son datos de demostración. En el ejemplo de confirmación, S/ 1,240.00 − S/ 48.90 = S/ 1,191.10. El mismo saldo inicial permanece en los ejemplos de descarte y error. Los wireframes definen la estructura de los formularios y sus acciones principales. Las validaciones de campos, el teclado y los estados de carga se detallarán en el diseño y prototipado de la aplicación.

### 6.4.2. Applications Wireflow Diagrams

Los wireflows relacionan representaciones de pantallas con acciones y resultados. Las flechas indican la secuencia principal y las notas de cada composición especifican las ramas alternativas. Cada recorrido permite identificar la pantalla de origen, la acción del usuario y el estado resultante.

**F01. Activación y confirmación RPA.** El usuario configura el acceso, selecciona fuentes, abre la bandeja y revisa el gasto. Confirmar registra el movimiento y actualiza el saldo. Si deniega o revoca el permiso, utiliza WF08; las notificaciones ajenas a fuentes autorizadas se descartan sin guardar contenido y los formatos no reconocidos no crean sugerencias.

![Wireflow de activación y confirmación RPA](../assets/img/cap06/wireflow-rpa.png)

*Figura 6.4.2-A. F01. [Abrir wireflow editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2007-758).*

**F02. Aceptación y corrección de categoría IA.** La sugerencia se solicita desde el registro manual o acompaña al gasto detectado. El usuario acepta la categoría o abre WF05 para reemplazarla. Ante baja confianza, WF06 solicita confirmar Otros o elegir otra categoría. Tras aplicar la elección se regresa a revisión y se confirma el gasto.

![Wireflow de aceptación y corrección de categoría IA](../assets/img/cap06/wireflow-ai.png)

*Figura 6.4.2-B. F02. [Abrir wireflow editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2007-847).*

**F03. Recordatorios y continuidad de alertas.** El usuario abre un recordatorio, consulta su detalle y vuelve a las alertas. La nota técnica relaciona esta experiencia con TS 024: Communications invoca n8n para formato, agrupación y canal; si el webhook falla, envía el aviso de respaldo directamente por Firebase Cloud Messaging, sin el formateo ni la agrupación del flujo. La decisión de respaldo ocurre internamente y no agrega una tarea de configuración al usuario.

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

### 6.4.3. Applications Mock-ups

Esta sección presenta los mock-ups de la aplicación móvil (Android) y de la aplicación web. En cada pantalla se aplican los principios de diseño, los elementos visuales, el diseño inclusivo y la arquitectura de información definidos en los apartados [6.1](#61-style-guidelines) y [6.2](#62-information-architecture), así como el Design System de Intiva. Los mock-ups se elaboran en Figma, en el mismo archivo de los wireframes y wireflows. Las pantallas base de la aplicación se toman de Page 1, y las pantallas nuevas (WF01 a WF12) de la sección TP1.

**Aplicación de la paleta por función.** Cada color cumple un rol fijo en todas las pantallas:

| Rol | Color | Uso en los mock-ups |
| --- | --- | --- |
| Primario | Índigo `#534AB7` | Botones principales, pestaña activa de la navegación inferior y tarjeta de saldo total. |
| Secundario | Lima `#CDEB45` | Llamadas a la acción de registro (Guardar, Confirmar gasto) y progreso de metas de ahorro. Sobre el lima se usa texto oscuro para mantener el contraste. |
| Terciario | Cobre `#8A4900` | Acciones de edición y algunas categorías. |
| Neutro | Gris violeta `#78767E` | Fondos, bordes, divisores y textos secundarios. |
| Error | Rojo `#BA1A1A` | Gastos, límites superados y acción de eliminar. |
| Estados de límite | Verde (a buen ritmo) y ámbar (cerca del límite) | Siempre acompañados de un texto. Los gastos por confirmar se muestran en tonos neutros. |

**Tipografía e iconografía.** Manrope en títulos, Inter en textos y botones, y Space Grotesk en montos, que se muestran con signo ("+" para ingresos y "−" para gastos). Los íconos son Material Symbols en la aplicación móvil y PrimeIcons en la aplicación web.

**Principios de diseño inclusivo aplicados.**
- Contraste verificado para cada combinación de texto, fondo y estado.
- Ningún estado depende solo del color: cada uno incluye un texto.
- Áreas táctiles de al menos 48 dp en Android, y botones principales a todo el ancho en la parte inferior de la pantalla.
- Dimensiones en dp y textos en sp, para respetar el tamaño de letra configurado en el teléfono.
- Contorno de foco visible en la aplicación web, para la navegación con teclado.

**Mock-ups de la aplicación móvil**

**Inicio.** Muestra primero el saldo total, después el estado del presupuesto y al final los movimientos recientes, según la jerarquía visual de [6.2.1](#621-organization-systems).

![Mockup de Inicio](../assets/img/cap06/Mockup10.png)

*Figura 6.4.3-A. Mock-up de la pantalla Inicio. [Abrir Mockup editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=0-1).*.*

**Registro manual de un movimiento.** Muestra los cinco pasos del registro (tipo, monto, categoría, cuenta y fecha) con teclado numérico propio y botón de guardado en la parte inferior. Corresponde a WF08.

![Mockup de Manual de un movimiento](../assets/img/cap06/Mockup11.png)

*Figura 6.4.3-B. Mock-up del registro manual de un movimiento.[Abrir Mockup editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2005-721).*

**Captura automática: permiso y fuentes.** Explica para qué sirve el permiso de notificaciones, permite elegir las fuentes autorizadas y ofrece continuar manualmente. Corresponde a WF01 y WF02.

![Mockup de automática: permiso y fuentes](../assets/img/cap06/Mockup12.png)

*Figura 6.4.3-C. Mock-up de permiso y fuentes autorizadas. [Abrir Mockup editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2005-721).*

**Por confirmar y revisión de un gasto.** Presenta la sugerencia pendiente en tonos neutros, con monto, comercio y fuente, y la pantalla de revisión con las acciones de aceptar o cambiar la categoría, confirmar o descartar. Corresponde a WF03 y WF04.

![Mockup de aconfirmar y revisión de un gasto.](../assets/img/cap06/Mockup13.png)

*Figura 6.4.3-D. Mock-up de la bandeja Por confirmar y de la revisión de un gasto. [Abrir Mockup editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2005-721).*

**Categoría y resultado.** Muestra la selección de otra categoría, la confirmación de "Otros" ante baja confianza y el mensaje de gasto registrado con el saldo actualizado. Corresponde a WF05, WF06 y WF07.

![Mockup de Cateogrias y resultado](../assets/img/cap06/Mock2.png)

*Figura 6.4.3-E. Mock-up de elegir categoría, confirmación de Otros y gasto registrado. [Abrir Mockup editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2005-721).*

**Recordatorios y error al guardar.** Muestra la lista de recordatorios, su detalle (monto, vencimiento y estado) y la pantalla de recuperación ante un error, que conserva los datos. Corresponde a WF09, WF10 y WF12.

![Mockup de recordatorios y errores](../assets/img/cap06/Mock6.png)

*Figura 6.4.3-E. Mock-up de recordatorio y su detalles. [Abrir Mockup editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2005-721).*

**Mock-ups de la aplicación web**

**Panel.** Ubica los indicadores principales (balance total, ingresos, gastos y ahorro del mes) en la parte superior y los gráficos de detalle debajo, con la barra lateral fija y el filtro de período (1 mes, 6 meses o 1 año). Los gráficos usan índigo y lima como colores de sus series.

![Mockup de aplicacion web](../assets/img/cap06/Mock7.png)

*Figura 6.4.3-G. Mock-up del Panel de la aplicación web. [Abrir Mockup editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=0-1).*

**Reportes.** Muestra la configuración del reporte por tipo (general, ingresos, gastos o ahorros), período e integrantes, y la acción de descarga.

![Mockup de Mock-up del Panel de la aplicación web](../assets/img/cap06/Mockup14.png)

*Figura 6.4.3-G. Mock-up del Panel de la aplicación web. [Abrir Mockup editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=0-1).*

### 6.4.4. Applications User Flow Diagrams

Esta sección presenta los User Flows de las aplicaciones de la solución. Están en la sección **Applications User Flow Diagrams** de la página [Mockup - User flow - Prototyping](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2005-721). Hay un User Flow por cada user goal, identificado con el código UF y el código G del objetivo. Cada flujo se deriva de un wireflow de [6.4.2](#642-applications-wireflow-diagrams) (F01, F02 o F03), o es una subruta de uno de ellos cuando el flujo es secundario.

Los actores corresponden a las audiencias de [6.2.1](#621-organization-systems): el **usuario de Intiva** (individual o integrante del grupo), y el **visitante web**. Para los flujos principales se describe además un escenario académico con dos personas de ejemplo: Carlos y María.

Cada diagrama incluye la ruta esperada (**happy path**, línea continua en el diagrama) y las rutas alternativas (**unhappy paths**, línea discontinua). Las condiciones se marcan con un rombo. Las pantallas se citan con su código de wireframe.

**Aplicación Android**

**UF01. Registrar un gasto detectado**

- **User goal:** "Quiero registrar un gasto detectado sin perder el control de mis datos."
- **Actor y escenario:** Carlos, que busca reducir la carga de transcribir una compra, pero quiere comprobar el importe y decidir qué se registra.
- **Happy path:** WF01 (configurar acceso) → WF02 (fuentes guardadas) → WF03 (sugerencia pendiente de confirmación) → WF04 (revisar gasto) → "Confirmar gasto" → WF07 (gasto registrado). El saldo pasa de S/ 1,240.00 a S/ 1,191.10 solo después de una respuesta exitosa.
- **Unhappy paths:**
    - Permiso denegado o revocado → WF08 (registro manual disponible).
    - Notificación de una fuente no autorizada o con formato no reconocido → se descarta sin guardar contenido y no crea sugerencia.
    - Descarte de la sugerencia → WF11, sin movimiento ni cambio de saldo.
    - Error al guardar → WF12.

![Userflow de Registrar un gasto detectado](../assets/img/cap06/Userflow1.png)
![Userflow de Registrar un gasto detectado](../assets/img/cap06/Userflow2.png)


*Figura 6.4.4-A. User Flow UF01. [Abrir diagrama editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2045-2348).*

**UF02. Aceptar o corregir la categoría sugerida por IA**

- **User goal:** "Quiero aceptar o corregir la categoría sugerida antes de confirmar mi gasto."
- **Actor y escenario:** María, que quiere que la compra quede en la categoría correcta aunque la propuesta de IA no refleje su criterio.
- **Happy path:** WF08 (solicitar categoría IA) → WF04 (revisar) → "Aceptar categoría" y "Confirmar gasto" → WF07.
- **Alternative path (corregir):** WF04 → WF05 (elegir categoría) → WF04 → "Confirmar gasto" → WF07.
- **Unhappy path:** baja confianza o comercio desconocido → WF06, donde "Otros" exige confirmación explícita. Confirmar la categoría vuelve a WF04 y no guarda el gasto por sí solo.

![Userflow de Aceptar o corregir la categoría sugerida por IA](../assets/img/cap06/Userflow3.png)

*Figura 6.4.4-B. User Flow UF02. [Abrir diagrama editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2045-2348).*

**UF03. Revisar y actualizar un vencimiento**

- **User goal:** "Quiero revisar un vencimiento y actualizar su estado cuando ya lo pagué."
- **Actor y escenario:** usuario de Intiva que necesita consultar fecha e importe de un servicio y distinguir los recordatorios atendidos de los pendientes, sin efectuar pagos desde Intiva.
- **Happy path:** notificación o Alertas → WF09 (estado Pendiente) → WF10 (detalle) → "Marcar como pagado" → WF09 (estado Pagado).
- **Unhappy paths:**
    - Salir del detalle sin marcar → WF09 con estado Pendiente, sin cambios.
    - Si el envío normal falla, se usa el aviso de respaldo sin formato ni agrupación y se abre el mismo detalle WF10.
- **Restricción:** "Marcar como pagado" solo actualiza el estado del recordatorio. No realiza transferencias ni débitos, y no reduce el saldo.

![Userflow deRevisar y actualizar un vencimiento](../assets/img/cap06/Userflow4.png)

*Figura 6.4.4-C. User Flow UF03. [Abrir diagrama editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2045-2348).*

**UF04. Registrar manualmente sin captura**

- **User goal:** "Quiero registrar un gasto manualmente sin autorizar la captura de notificaciones."
- **Actor y escenario:** usuario de Intiva que prefiere ingresar el gasto por su cuenta, o que necesita continuar después de denegar o revocar el permiso de captura.
- **Happy path:** WF01 → "Continuar manualmente" → WF08 → WF04 (revisar) → "Guardar gasto" → WF07 (saldo actualizado tras guardado exitoso).
- **Alternative paths:** elegir otra categoría → WF05 → WF04. Pedir ayuda de IA → revisión en WF04, y si la confianza es baja se sigue UF02.
- **Unhappy path:** error al guardar → WF12. Los datos y el saldo previo se conservan, y no se muestra ningún éxito.

![Userflow de Registrar manualmente sin captura](../assets/img/cap06/Userflow5.png)

*Figura 6.4.4-D. User Flow UF04. [Abrir diagrama editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2045-2348).*

**UF05. Controlar fuentes y revocar captura**

- **User goal:** "Quiero elegir mis fuentes financieras y poder desactivar o revocar la captura."
- **Actor y escenario:** usuario de Intiva que quiere limitar qué notificaciones financieras procesa la app.
- **Happy path:** Perfil → WF01 (permiso) → WF02 (fuentes) → "Guardar fuentes".
- **Alternative paths:**
    - Desactivar la captura dentro de Intiva → WF08. El registro manual sigue disponible.
    - Desactivar una sola fuente → WF02 guarda la selección. El permiso general de Android sigue concedido.
    - Denegar o revocar el acceso en los ajustes de Android (nodo externo) → WF08.

Intiva controla qué fuentes procesa, mientras que el acceso general a notificaciones se controla en Android. Desactivar una fuente no revoca el permiso completo.

![Userflow de Controlar fuentes y revocar captura](../assets/img/cap06/Userflow6.png)

*Figura 6.4.4-E. User Flow UF05. [Abrir diagrama editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2045-2348).*

**Sitio web**

**UF06. Evaluar Intiva desde la landing**

- **User goal:** "Quiero comprender la propuesta de Intiva y decidir si me interesa usarla."
- **Actor y escenario:** visitante web que busca entender la utilidad del registro asistido, las condiciones de privacidad y qué información queda por confirmar.
- **Happy path:** landing → beneficios, control y privacidad → decisión de evaluar → CTA "Descargar app" (ilustrativo).
- **Unhappy path:** la información del equipo y los planes aún no está confirmada → la landing lo indica como pendiente y el visitante sigue consultando otras secciones.
- **Límite:** el CTA es ilustrativo. No se dibuja una descarga completada ni una creación de cuenta, y la publicación en Google Play sigue pendiente.

UF06 es una meta web y no deriva de F01, F02 ni F03.

![Userflow Evaluar Intiva desde la landing](../assets/img/cap06/Userflow7.png)
![Userflow Evaluar Intiva desde la landing](../assets/img/cap06/Userflow8.png)

*Figura 6.4.4-F. User Flow UF06. [Abrir diagrama editable](https://www.figma.com/design/wV6U6QQC4MEYfj8PQArde5/Intiva-Platform-Application-Emergentes?node-id=2045-2348).*
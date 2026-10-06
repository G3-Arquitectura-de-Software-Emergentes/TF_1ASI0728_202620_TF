

# Capítulo VI: Solution UX Design

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

# Capítulo VII: Product Implementation, Validation & Deployment

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

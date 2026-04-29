# JustDemo-REQUEST.md — [Nombre del Proyecto]

> **Flujo:** JustDemo · CognitionBase  
> **Versión de plantilla:** 1.1  
> **Prerequisito:** Esta plantilla solo debe completarse si la idea ya pasó el `justgotomarket-IDEAS-FILTER-CHECKLIST.md`. Si la idea no ha sido filtrada, comenzar por ahí.  
> **Instrucciones:** Reemplaza cada `[COMPLETAR]` con el valor real. Los bloques `> Ej:` son ejemplos basados en el proyecto ARCO Legal — borrarlos al completar. Este documento alimenta directamente a `/gsd-new-project` y al agente de Blueprint; si un campo queda vacío, el flujo se detiene en Intake.
> **Paradigma JustGoToMarket:** El cliente final **compra un resultado**, no una herramienta. La tecnología —sea automatización, agente IA, plataforma o procesamiento de datos— es el habilitador del servicio, no el servicio en sí. Este landing valida si el mercado está dispuesto a pagar por ese resultado, no si quiere acceder a un software.

---

## 1. PROYECTO

<!-- Identidad mínima del proyecto. El slug se usa para nombre de repo, carpeta, subdominio por defecto. -->

**nombre:** [COMPLETAR]
> Ej: `ARCO Legal`

**slug:** [COMPLETAR]
> Ej: `arco-legal` _(kebab-case, sin espacios, sin caracteres especiales)_

**descripcion_una_linea:** [COMPLETAR]
> Ej: `Plataforma SaaS que gestiona el ciclo completo de solicitudes ARCO+ para empresas chilenas antes de que entre en vigencia la Ley 21.719.`
> _(≤ 140 caracteres. Es el input principal para el headline del landing.)_

**mensaje_clave:** [COMPLETAR]
> Ej: `La Ley 21.719 entra en vigencia en diciembre 2026 con multas de hasta 20.000 UTM — ARCO Legal cubre el ciclo completo: recepción, gestión y recolección de datos desde tus plataformas.`
> _(La propuesta de valor central. No tiene que ser el copy final — es la dirección para el agente de copywriting.)_

**deadline_landing:** [COMPLETAR]
> Ej: `2026-05-15` _(Si no hay fecha, se aplica el KPI por defecto del Protocolo Iron-Legion: 7–10 días hábiles desde aprobación del Blueprint.)_

---

## 2. AUDIENCIA Y PROBLEMA

<!-- El visitante ideal del landing. Cuanto más específico y en "sus propias palabras", mejor copy genera el agente. -->
<!-- Esta sección también captura los atributos del problema que justifican el ingreso al flujo JustDemo. -->

**perfil_ict:** [COMPLETAR]
> Ej: `Gerente General, Gerente Legal, o DPO de una empresa chilena que trata datos personales de clientes o empleados.`

**empresa_tipo:** [COMPLETAR]
> Ej: `PyME chilena (20–500 empleados), cualquier industria, sin DPO ni herramientas de compliance propias.`

**problema_en_sus_palabras:** [COMPLETAR]
> Ej: `"No tenemos proceso para recibir solicitudes de datos. Si llega una, no sabemos ni quién la atiende ni en cuánto tiempo hay que responder."`
> _(Verbatim o paráfrasis de cómo el cliente describe el dolor. Fuente: entrevistas, reseñas, conversaciones de ventas.)_

**frecuencia_del_problema:** [COMPLETAR]
> Opciones: `diario` | `semanal` | `mensual` | `por-ciclo-de-negocio`
> Ej: `mensual` _(Cada mes que opera la empresa sin proceso ARCO+ es un mes de exposición regulatoria activa.)_
> _(El problema debe ser recurrente para el mismo afectado — no un evento puntual. Ref: Criterio 2 del Filter Checklist.)_

**indicador_de_resolucion:** [COMPLETAR]
> Ej: `100% de solicitudes ARCO+ respondidas dentro del plazo legal de 30 días, con trazabilidad completa en cada caso.`
> _(El indicador objetivo y medible que confirma que el problema fue resuelto. Debe ser específico — "mejorar el proceso" no califica. Ref: Criterio 1-E3 del Filter Checklist.)_

**evidencia_de_mercado:** [COMPLETAR]
> Ej: `Toda empresa chilena que trata datos personales debe cumplir la Ley 21.719 (vigencia dic 2026). Universo estimado: +5.000 PyMEs chilenas en el segmento objetivo.`
> _(Señal de que existen al menos 50 empresas o 200 personas con este problema dispuestas a pagar. Puede ser indirecta: competidores, regulación, entrevistas, búsquedas. Ref: Criterio 3-M1 del Filter Checklist.)_

**urgencia:** [COMPLETAR]
> Ej: `La Ley 21.719 entra en vigencia el 1 de diciembre de 2026. Las multas aplican desde el día 1. Construir un proceso desde cero toma meses.`
> _(Por qué deben actuar ahora y no después.)_

**objeciones:**
<!-- Lista de razones por las que el visitante dudaría en convertir. El landing debe anticiparlas. -->
- [COMPLETAR]
- [COMPLETAR]
- [COMPLETAR]

> Ej:
>
> - `"Somos una empresa pequeña, esto no aplica para nosotros."`
> - `"¿Cuánto tiempo lleva implementarlo antes de diciembre?"`
> - `"¿Necesitamos integrar todos nuestros sistemas desde el principio?"`

**temperatura_trafico:** [COMPLETAR]
> Opciones: `frio` | `tibio` | `caliente`
> Ej: `tibio` _(Ya saben que la Ley 21.719 existe, pero no han investigado soluciones.)_
> _(Frío = no saben quién eres. Tibio = conocen el problema. Caliente = ya están evaluando opciones.)_

**fuente_trafico_principal:** [COMPLETAR]
> Opciones: `linkedin-ads` | `google-ads` | `busqueda-organica` | `email` | `referido-directo` | `otro`
> Ej: `linkedin-ads`
> _(Define el nivel de contexto que el visitante trae al llegar. Afecta directamente el copy del hero.)_

---

## 3. SOLUCIÓN

<!-- Lo que ofrece el servicio. Énfasis en el resultado que recibe el cliente, no en las features del sistema. -->
<!-- Paradigma JustGoToMarket: el cliente compra un resultado, no una herramienta. La tecnología es el medio. -->

**modelo_de_servicio:** [COMPLETAR]
> Opciones: `resultado-sin-plataforma` | `resultado-via-plataforma`
> Ej: `resultado-via-plataforma` _(El cliente interactúa con una plataforma para gestionar solicitudes, pero lo que compra es la garantía de cumplimiento — no el acceso al software.)_
> _(`resultado-sin-plataforma`: el cliente recibe el resultado sin interactuar con ningún sistema. Ej: reporte mensual enviado por email. `resultado-via-plataforma`: el cliente usa una interfaz, pero la promesa de valor es el resultado que esa interfaz facilita, no el acceso en sí.)_

**que_hace:** [COMPLETAR]
> Ej: `Gestiona el ciclo completo de cada solicitud ARCO+: canal único de recepción para titulares, tracking automático de plazos, gestión por el operador y recolección de datos desde las plataformas de la empresa mediante conectores.`

**por_que_funciona:** [COMPLETAR]
> Ej: `Elimina los dos problemas estructurales: la falta de canal de recepción con control de plazos, y la búsqueda manual de datos en múltiples sistemas.`
> _(El mecanismo — por qué esta solución específica resuelve el problema cuando otras no.)_

**transformacion:** [COMPLETAR]
> Ej: `De "no tenemos proceso para solicitudes ARCO+" a "100% de solicitudes respondidas dentro del plazo legal, con trazabilidad completa."`
> _(Formato: "De [estado actual doloroso] a [estado futuro deseado]". El estado futuro debe expresarse como un resultado para el cliente, no como una función del sistema.)_

**diferenciadores:**
<!-- Máximo 3. Específicos y verificables — evitar "solución integral" y similares. -->
- [COMPLETAR]
- [COMPLETAR]
- [COMPLETAR]

> Ej:
>
> - `Flujo completo de punta a punta — no solo un tracker de plazos, sino gestión + respuesta + recolección de datos.`
> - `Sistema de conectores extensible (BUK, Google Drive, API abierta) — los datos se recolectan automáticamente desde los sistemas actuales.`
> - `Disponible como SaaS o on-premise — cubre empresas con restricciones regulatorias de residencia de datos (banca, salud, gobierno).`

**proof_points:**
<!-- Números reales, logos de clientes, testimoniales. Si el producto es pre-lanzamiento, dejar vacío y el agente construirá credibilidad desde el contexto regulatorio. -->
- [COMPLETAR o dejar vacío si pre-lanzamiento]

> Ej (pre-lanzamiento): _(vacío — el landing usará la urgencia regulatoria y el equipo como señal de credibilidad)_

---

## 4. LANDING PAGE

<!-- Datos que el agente de copywriting y el Blueprint necesitan para diseñar la página. -->

**cta_principal_accion:** [COMPLETAR]
> Ej: `Agendar una demo de 20 minutos`
> _(Qué hace el visitante al hacer clic. Define el diseño entero del landing. Opciones comunes: "agendar demo", "unirse a lista de espera", "solicitar acceso anticipado", "ver el producto en acción".)_

**cta_principal_texto_boton:** [COMPLETAR]
> Ej: `Ver ARCO Legal en acción`
> _(El texto exacto del botón principal. Fórmula: [Verbo acción] + [Qué obtienen]. Evitar: "Enviar", "Registrarse", "Más información".)_

**secciones_obligatorias:**
<!-- Secciones que DEBEN aparecer en el landing. El agente decide el resto según best practices. -->
- [COMPLETAR]

> Ej:
>
> - `Hero (headline + subheadline + CTA)`
> - `Problema (por qué la inacción es costosa — tabla de multas)`
> - `Solución (qué hace ARCO Legal, 3 pilares)`
> - `Cómo funciona (workflow en 4 pasos)`
> - `Demo CTA (acceso al demo interactivo)`
> - `FAQ (objeciones principales)`
> - `CTA final`

**tono_de_voz:** [COMPLETAR]
> Opciones: `formal-profesional` | `conversacional-directo` | `tecnico-accesible`
> Ej: `formal-profesional`
> _(Para productos de compliance/legal, formal-profesional. Para SaaS dev tools, conversacional-directo. Para plataformas B2B mixtas, técnico-accesible.)_

**idioma:** [COMPLETAR]
> Default: `es` _(Si se necesita versión en inglés, es un entregable separado — declararlo en v2_nice_to_have.)_

---

## 5. DEMO

<!-- El "Aha! Moment" — el instante donde el visitante entiende visceralmente el resultado que recibirá si contrata el servicio. El Blueprint lo convierte en diseño técnico y de UX. -->
<!-- El demo no tiene que mostrar un software completo — tiene que mostrar el resultado que el cliente obtiene. Enfocarse en el "qué recibe el cliente", no en "qué hace el sistema". -->

**tipo_demo:** [COMPLETAR]
> Opciones: `video-pregrabado` | `prototipo-interactivo` | `simulacion-funcional` | `demo-en-vivo-agendada`
> Ej: `prototipo-interactivo`
> _(Cada tipo tiene un esfuerzo de build diferente. Video-pregrabado es el más rápido. Simulación-funcional es el más convincente pero más costoso. Demo-en-vivo requiere agendamiento.)_

**aha_moment_hipotesis:** [COMPLETAR]
> Ej: `El visitante ve cómo una solicitud ARCO+ llega al sistema, queda registrada automáticamente con un countdown de 30 días y aparece en el tablero Kanban — sin que nadie tuviera que hacer nada manualmente.`
> _(El momento específico donde el visitante piensa "esto resuelve exactamente mi problema". Descríbelo como una escena: qué ve, qué pasa, qué siente.)_

**flujo_demo:**
<!-- 3 a 5 pasos que el visitante experimenta en el demo. El agente de Blueprint los convierte en pantallas/interacciones. -->
1. [COMPLETAR]
2. [COMPLETAR]
3. [COMPLETAR]

> Ej:
>
> 1. `El titular envía una solicitud ARCO+ a través del formulario público de la empresa.`
> 2. `La solicitud aparece en el tablero Kanban de ARCO Legal con estado "Recibida" y un countdown automático de 30 días.`
> 3. `El operador avanza la solicitud a "Recolección de datos" — el sistema lanza el conector a BUK y Google Drive para recopilar los datos del titular.`
> 4. `El operador responde al titular con un clic. El sistema registra la respuesta con comprobante de cumplimiento.`

**herramienta_agendamiento:** [COMPLETAR si tipo_demo = demo-en-vivo-agendada, sino "N/A"]
> Ej: `N/A` _(Si es demo-en-vivo, incluir la URL de Calendly o equivalente.)_

---

## 6. DESPLIEGUE

<!-- Datos técnicos y operacionales que habilitan el build y el deploy. Sin URL confirmada, el flujo no puede completar la Etapa 7. -->

**url_destino:** [COMPLETAR]
> Ej: `arcolegal.cl` o `arcolegal.cognitionbase.io`
> _(URL completa donde vivirá el landing en producción. Si aún no está disponible, indicar el subdominio de staging que se usará mientras tanto.)_

**dns_gestionado_por:** [COMPLETAR]
> Ej: `Manuel Reyes — acceso a Cloudflare` _(Nombre + plataforma DNS. Necesario para la Etapa 7.)_

**dns_listo:** [COMPLETAR]
> Opciones: `true` | `false`
> _(Si es false, incluir plazo estimado en comentario.)_

**branding:**

- **logo:** [COMPLETAR o "generar"]
  > Ej: `generar` _(Si no existe logo, el agente generará uno desde la narrativa. Si existe, proveer URL o ruta al archivo SVG/PNG.)_

- **colores:** [COMPLETAR o "generar"]
  > Ej: `generar` _(Si no hay paleta definida, el agente la genera desde la narrativa. Si existe, proveer hex codes primario + secundario + acento.)_

- **tipografia:** [COMPLETAR o "generar"]
  > Ej: `generar` _(Si no hay tipografía definida, el agente usa Inter por defecto. Si existe, proveer nombre de la fuente y peso.)_

**analytics_herramienta:** [COMPLETAR]
> Default: `ga4`
> Ej: `ga4` _(Opciones: ga4 | plausible | mixpanel | hotjar | ninguno. Si se quiere más de una, listar.)_

**integraciones:**
<!-- Servicios externos que el CTA o el formulario deben conectar. -->
- [COMPLETAR]

> Ej:
>
> - `calendly` _(El CTA "Agendar demo" abre el widget de Calendly.)_
> - `resend` _(Confirmación de agendamiento por email.)_
> _(Opciones comunes: formulario-propio | calendly | mailchimp | resend | hubspot | salesforce | ninguno)_

**stack_override:** [COMPLETAR o "null"]
> Default (`null`): CB Standard — Next.js 14 + Tailwind CSS + Vercel + TypeScript
> Ej: `null`
> _(Solo completar si hay restricciones específicas. Ej: "WordPress obligatorio por política del cliente", "No puede usar Vercel por restricciones de residencia de datos".)_

---

## 7. CRITERIO DE ÉXITO (Gate para Landing2MVP)

<!-- Define cuándo el Idea2Landing "terminó" con éxito y puede iniciar el flujo Landing2MVP. Sin este criterio definido, el landing no tiene DoD real. -->

**metrica_tipo:** [COMPLETAR]
> Opciones: `demos-agendados` | `leads-capturados` | `tasa-conversion` | `willingness-to-pay` | `otro`
> Ej: `demos-agendados`

**metrica_objetivo:** [COMPLETAR]
> Ej: `10 demos agendados en los primeros 14 días desde el go-live`
> _(Ser específico. "Tener tracción" no es una métrica. "10 demos agendados" sí lo es.)_

**plazo_evaluacion_dias:** [COMPLETAR]
> Ej: `14` _(Días desde el go-live del landing para hacer la primera evaluación de la métrica.)_

---

## 8. SCOPE GSD

<!-- Esta sección alimenta directamente a REQUIREMENTS.md de GSD. Define el contrato de entrega antes de que el Blueprint planifique. -->

**v1_must_have:**
<!-- Qué DEBE estar funcionando para que el landing se considere entregado. DoD del Idea2Landing. -->
- [COMPLETAR]

> Ej:
>
> - `Landing responsivo (mobile + desktop) desplegado en URL de producción`
> - `Hero section con headline, subheadline y CTA principal operativo`
> - `Demo accesible desde el CTA — al menos prototipo interactivo o video`
> - `Formulario/agendamiento conectado y enviando datos reales`
> - `GA4 instalado y disparando evento de conversión en el CTA`
> - `SEO básico: title, meta description, OG tags`
> - `SSL activo en URL de producción`

**v2_nice_to_have:**
<!-- Qué puede esperar al siguiente ciclo o post-lanzamiento. -->
- [COMPLETAR]

> Ej:
>
> - `Blog o sección de recursos sobre Ley 21.719`
> - `Versión en inglés del landing`
> - `Hotjar o herramienta de heatmaps`
> - `Chat en vivo o widget de soporte`
> - `Página de pricing`

**out_of_scope:**
<!-- Qué explícitamente NO debe hacer GSD en este ciclo. Evita que el agente "mejore" cosas fuera del acuerdo. -->
- [COMPLETAR]

> Ej:
>
> - `Desarrollo de la plataforma ARCO Legal (eso es Landing2MVP)`
> - `Integraciones con sistemas externos del cliente (BUK, Google Drive, etc.)`
> - `Panel de administración o autenticación de usuarios`
> - `Multi-tenancy o configuración por empresa`

**constraints:**
<!-- Restricciones técnicas, regulatorias o de negocio que el agente debe respetar. -->
- [COMPLETAR]

> Ej:
>
> - `El landing no debe recolectar datos personales más allá del email/nombre para el agendamiento (ironía regulatoria — ARCO Legal debe cumplir la Ley 21.719 desde el día 1)`
> - `Tiempo de carga < 3 segundos en mobile (Core Web Vitals: LCP < 2.5s)`
> - `No usar librerías con licencias no permisivas (MIT/Apache únicamente)`

---

## 9. CONTEXTO ADICIONAL

<!-- Cualquier información relevante que no cabe en las secciones anteriores. Documentos de referencia, decisiones estratégicas ya tomadas, personas clave, links útiles. -->

**documentos_de_referencia:**

- [COMPLETAR o "ninguno"]

> Ej: `Narrativa estratégica completa en Proyecto - Arco Legal.pdf`

**decisiones_ya_tomadas:**
<!-- Decisiones estratégicas o técnicas que NO deben ser cuestionadas por el Blueprint. -->
- [COMPLETAR o "ninguno"]

> Ej:
>
> - `Manual-first: el landing debe validar el mercado antes de automatizar. No construir integraciones automáticas en v1.`
> - `PyMEs primero: el copy y el pricing apuntan a empresas de 20–500 empleados.`
> - `SaaS por defecto, on-premise como opción — mencionarlo en el landing.`

**equipo:**

- **SRM (responsable del intake):** [COMPLETAR]
- **Lead Dev AI (responsable del Blueprint):** [COMPLETAR]
- **Contacto técnico (DNS/dominio):** [COMPLETAR]

> Ej: SRM: Manuel Reyes · Lead Dev AI: Marcelo Ampuero · Contacto DNS: Manuel Reyes (Cloudflare)

---

## CHECKLIST DE INTAKE (SRM)

> El SRM valida este checklist antes de aprobar el ingreso al flujo. Si algún campo obligatorio está incompleto, se devuelve al solicitante con indicación del campo faltante.

**Campos obligatorios — sin estos el flujo NO inicia:**

- [ ] `nombre` completado
- [ ] `slug` completado
- [ ] `descripcion_una_linea` completado
- [ ] `mensaje_clave` completado
- [ ] `perfil_ict` completado
- [ ] `problema_en_sus_palabras` completado
- [ ] `frecuencia_del_problema` completado _(recurrencia del problema — Criterio 2)_
- [ ] `indicador_de_resolucion` completado _(métrica objetiva de resolución — Criterio 1-E3)_
- [ ] `evidencia_de_mercado` completado _(señal de universo potencial — Criterio 3-M1)_
- [ ] `urgencia` completado
- [ ] `modelo_de_servicio` completado
- [ ] `que_hace` completado
- [ ] `transformacion` completado
- [ ] `cta_principal_accion` completado
- [ ] `cta_principal_texto_boton` completado
- [ ] `tono_de_voz` completado
- [ ] `tipo_demo` completado
- [ ] `aha_moment_hipotesis` completado
- [ ] `url_destino` completado (puede ser staging si producción no está lista)
- [ ] `dns_gestionado_por` completado
- [ ] `metrica_objetivo` completado
- [ ] `v1_must_have` completado (al menos 3 ítems)
- [ ] `out_of_scope` completado (al menos 1 ítem)

**Campos opcionales con fallback — el Blueprint los resuelve si faltan:**

- [ ] `branding` → fallback: generar desde narrativa
- [ ] `analytics_herramienta` → fallback: GA4
- [ ] `stack_override` → fallback: CB Standard (Next.js + Tailwind + Vercel)
- [ ] `idioma` → fallback: `es`
- [ ] `deadline_landing` → fallback: 7–10 días hábiles desde Blueprint aprobado
- [ ] `proof_points` → fallback: credibilidad desde contexto regulatorio/equipo
- [ ] `flujo_demo` → fallback: el Blueprint lo define a partir del `aha_moment_hipotesis`

# CognitionBase — Servicios y Flujos Operativos para Tableros Kanban

> **Fecha:** 2026-04-26
> **Propósito:** Descripción de los servicios de CognitionBase y el diseño de sus flujos operativos como tableros Kanban para la gestión de tareas.

---

## Servicios de CognitionBase

CognitionBase opera como incubadora de productos digitales bajo dos servicios especializados:

---

### Servicio 1: Idea2Market

**Objetivo:** Transformar ideas de negocio en productos digitales validados (MVP) con velocidad y eficiencia radical, orquestando agentes de IA.

El servicio opera como dos sub-flujos secuenciales separados por un **gate de validación de tracción**:

```
Idea2Landing (I2LP)  →  [gate: métrica de tracción]  →  Landing2MVP (L2MVP)
```

#### Sub-servicio 1.1 — Idea2Landing (I2LP)

Transforma una idea validada en un **landing page funcional con demo interactivo**, desplegado en producción en 7–10 días hábiles. El objetivo no es el landing en sí — es validar si el mercado responde a la propuesta de valor antes de invertir en desarrollo complejo.

- **Input:** `REQUEST.md` validado por el SRM (4 bloques: Narrativa Estratégica, Marketing Digital, Datos Operacionales, GSD Scope)
- **Output:** Landing live + demo interactivo + analytics activo
- **Stack estándar:** Next.js + Tailwind CSS + Vercel + GA4
- **Responsable de orquestación:** Lead Dev AI & SDM

#### Sub-servicio 1.2 — Landing2MVP (L2MVP)

Entrega de un MVP funcional en **menos de 6 semanas**, condicionado a que el landing supere el gate de tracción definido en el `REQUEST.md`.

- **Input:** Landing validado con métrica de gate cumplida
- **Output:** MVP funcional desplegado en producción
- **Ejecución:** Equipo Westworld (agentes de IA coordinados + profesionales humanos)
- **Calidad:** Auditoría automática de seguridad y eficacia en cada pull request

---

### Servicio 2: Technical Evaluations

**Objetivo:** Garantizar la excelencia del talento en el ecosistema 23people mediante el diseño y ejecución de evaluaciones técnicas de alto nivel para procesos de selección.

- **Input:** Solicitud de evaluación técnica (perfil del candidato, rol, competencias a evaluar)
- **Output:** Informe de evaluación técnica entregado
- **KPI clave:** Lead-Time promedio de entrega + Throughput semanal/mensual

---

## Roles Operativos

| Rol | Responsabilidad |
|-----|-----------------|
| **SRM** (Service Request Manager) | Gestión de demanda upstream. Clasifica, prioriza y valida administrativamente las solicitudes antes de ingresarlas al flujo técnico. |
| **Lead Dev AI & SDM** | Service Delivery Manager de ambos servicios. Supervisa el flujo técnico (downstream), calidad, métricas de ciclo y orquestación de Westworld. |
| **Devs AI — Westworld** | Ejecutores de élite. Equipo híbrido (humanos + agentes IA) que lleva la entrega desde el blueprint hasta producción. |

---

## Tableros Kanban Propuestos

Se proponen **4 tableros Kanban** que cubren la totalidad de los flujos operativos de CognitionBase:

---

### Tablero 1 — Upstream: Gestión de Solicitudes (SRM)

**Responsable:** SRM
**Propósito:** Gestionar la demanda entrante de ambos servicios (Idea2Market y Technical Evaluations). Controla el flujo desde que llega una solicitud hasta que se aprueba para ingresar al flujo técnico.

| # | Columna | Criterio de entrada | Trabajo en la etapa | Criterio de salida |
|---|---------|--------------------|--------------------|-------------------|
| 1 | **📥 Solicitud Recibida** | Llega una nueva solicitud (idea o evaluación) | Registrar la solicitud con tipo, solicitante y fecha | Solicitud registrada y asignada al SRM |
| 2 | **🔍 Revisión & Clasificación** | Solicitud asignada al SRM | Clasificar por tipo de servicio. Verificar información mínima disponible. Identificar campos faltantes | Solicitud clasificada y con responsable definido |
| 3 | **📝 Completar REQUEST.md** | Solicitud clasificada | Trabajar con el solicitante para completar todos los campos requeridos del `REQUEST.md`. Verificar campos bloqueantes | `REQUEST.md` completo con campos bloqueantes rellenos o fallbacks declarados |
| 4 | **✅ Aprobado — Listo para flujo técnico** | `REQUEST.md` validado sin campos bloqueantes vacíos | Aprobar formalmente el ingreso al flujo técnico. Notificar al Lead Dev AI | Tarjeta traspasada al tablero técnico correspondiente |
| 5 | **❌ Descartado / En espera** | Solicitud que no cumple criterios o está en pausa | Documentar motivo de descarte o bloqueo | — |

**Campos bloqueantes del REQUEST.md (Idea2Market):**
- `url_destino`
- `cta_principal_accion`
- `aha_moment_hipotesis`
- `metrica_objetivo` (gate para Landing2MVP)
- `v1_must_have`

---

### Tablero 2 — Downstream: Idea2Landing (I2LP)

**Responsable:** Lead Dev AI & SDM + Equipo Westworld
**Propósito:** Llevar un `REQUEST.md` aprobado hasta un landing page funcional con demo interactivo en producción.

| # | Columna | Criterio de entrada | Trabajo en la etapa | Criterio de salida (DoD) |
|---|---------|--------------------|--------------------|--------------------------|
| 1 | **📥 Intake Validado** | `REQUEST.md` aprobado por SRM | Recibir el proyecto en el flujo técnico. Crear carpeta del proyecto y artefactos iniciales | Proyecto registrado en el tablero con carpeta creada |
| 2 | **📐 Blueprint** | Proyecto en el tablero | Lead Dev AI genera el plano técnico: arquitectura del landing, flujo del demo, orquestación de agentes. Genera `PROJECT.md`, `REQUIREMENTS.md`, `ROADMAP.md`, `STATE.md` | Blueprint aprobado por Lead Dev AI antes de tocar código |
| 3 | **✍️ Copy & Marketing Design** | Blueprint aprobado | Agente de copywriting (Iron-Legion) genera el copy completo del landing basado en Narrativa Estratégica y Datos de Marketing Digital | Copy aprobado internamente |
| 4 | **🎨 UI/UX Design** | Copy aprobado | Diseño responsivo del landing (mobile + desktop) incluyendo flujo del demo hasta el Aha! Moment | Diseño aprobado en mobile y desktop |
| 5 | **🛠️ Build: Landing + Demo** | Diseño aprobado + entorno staging disponible | Dev AI implementa landing y demo sobre el stack estándar (o `stack_override`). Demo accesible desde el CTA principal | Landing navegable en staging, demo funcional, sin errores críticos |
| 6 | **🔎 QA, SEO & Analytics** | Landing en staging completo | Lighthouse score aceptable. GA4 disparando eventos clave. Sin errores de consola. SSL configurado. Open Graph y meta tags correctos | Todos los puntos del checklist en verde |
| 7 | **🚀 Deploy a Producción** | QA aprobado | Deploy a la URL destino. Cliente recibe acceso a dashboard de analytics | URL pública live + SSL activo + cliente con acceso a analytics confirmado |
| 8 | **📊 En Seguimiento (Gate)** | Landing en producción | Monitorear la métrica de gate definida en `REQUEST.md` (leads, conversión, demos completados) | Métrica de gate alcanzada → traspasar a tablero L2MVP |

**Checklist de QA (etapa 6):**
- [ ] Lighthouse: Performance, Accessibility y SEO aceptables
- [ ] GA4: eventos `page_view`, `cta_click`, `demo_start` activos
- [ ] Sin errores de consola en mobile y desktop
- [ ] SSL/HTTPS configurado
- [ ] Open Graph y meta tags correctos para redes sociales

---

### Tablero 3 — Downstream: Landing2MVP (L2MVP)

**Responsable:** Lead Dev AI & SDM + Equipo Westworld
**Propósito:** Desarrollar el MVP funcional en menos de 6 semanas a partir de un landing que superó el gate de tracción.

| # | Columna | Criterio de entrada | Trabajo en la etapa | Criterio de salida (DoD) |
|---|---------|--------------------|--------------------|--------------------------|
| 1 | **✅ Gate Superado — Listo para MVP** | Métrica de gate del landing cumplida | Confirmar decisión de avanzar. Crear `L2MVP-REQUEST.md` si no existe | Proyecto aprobado formalmente para desarrollo de MVP |
| 2 | **📐 Architecture & Sprint Planning** | Proyecto aprobado para MVP | Lead Dev AI define arquitectura técnica del MVP. Crea backlog inicial. Define sprints y criterios de aceptación | Backlog creado, sprints definidos, arquitectura aprobada |
| 3 | **🔨 En Desarrollo (Sprint activo)** | Sprint planificado | Westworld ejecuta el sprint: features, integraciones, base de datos, autenticación, etc. PR con auditoría automática de seguridad | Sprint completado con todos los criterios de aceptación cumplidos |
| 4 | **🔎 Review & QA** | Sprint completado | Lead Dev AI revisa entregables. QA funcional, de seguridad y de rendimiento | Aprobado para staging o producción |
| 5 | **🚀 Deploy Incremental / Producción** | Review aprobado | Deploy a staging o producción según el sprint. Cliente con acceso para validación | MVP funcional en producción o staging con acceso del cliente |
| 6 | **✅ MVP Entregado** | MVP en producción validado por cliente | Entrega formal. Documentación de handoff. KPIs de post-entrega iniciados | Cliente confirma recepción. Período de 7 días para defects abierto |

**KPI crítico:** Post-Delivery Defect Rate ≤ 1 bug en los 7 días posteriores a la entrega.

---

### Tablero 4 — Technical Evaluations

**Responsable:** Lead Dev AI & SDM + Equipo Westworld
**Propósito:** Gestionar el ciclo completo de diseño y ejecución de evaluaciones técnicas para procesos de selección del ecosistema 23people.

| # | Columna | Criterio de entrada | Trabajo en la etapa | Criterio de salida (DoD) |
|---|---------|--------------------|--------------------|--------------------------|
| 1 | **📥 Solicitud Recibida** | Solicitud de evaluación técnica del equipo de selección | Registrar candidato, rol a evaluar y competencias requeridas | Solicitud registrada con responsable asignado |
| 2 | **📝 Diseño de Evaluación** | Solicitud con perfil completo | Diseñar el set de evaluación: prueba técnica, desafío de código, caso práctico o entrevista estructurada según el rol | Evaluación diseñada y aprobada por Lead Dev AI |
| 3 | **⚙️ Ejecución** | Evaluación diseñada + candidato disponible | Aplicar la evaluación al candidato. Recopilar respuestas, código o entregables | Evaluación completada con todos los entregables del candidato recopilados |
| 4 | **📊 Análisis & Corrección** | Entregables del candidato completos | Analizar resultados. Puntuar y documentar hallazgos. Identificar fortalezas y brechas | Análisis completo con scoring documentado |
| 5 | **📄 Informe Final** | Análisis completo | Redactar informe de evaluación técnica con resultado, justificación y recomendación | Informe revisado y aprobado internamente |
| 6 | **✅ Entregado** | Informe aprobado | Enviar informe al equipo de selección dentro del lead-time objetivo | Confirmación de recepción por parte del equipo de selección |

---

## Resumen de Tableros

| Tablero | Tipo | Responsable principal | Flujo que gestiona |
|---------|------|-----------------------|--------------------|
| Upstream: Gestión de Solicitudes | Upstream | SRM | Demanda de ambos servicios |
| Downstream: Idea2Landing | Downstream | Lead Dev AI | I2LP: Idea → Landing en producción |
| Downstream: Landing2MVP | Downstream | Lead Dev AI | L2MVP: Landing validado → MVP en producción |
| Technical Evaluations | Independiente | Lead Dev AI | Evaluaciones técnicas para selección 23people |

---

## Notas Operativas Generales

- **Bloqueos:** Cualquier tarjeta que no pueda avanzar debe marcarse como bloqueada con nota clara del motivo y responsable de desbloquearlo.
- **WIP Limit recomendado:** Definir límite de trabajo en progreso por columna para evitar cuellos de botella (a definir por el equipo).
- **Revisión del tablero:** Revisión semanal del estado de todas las tarjetas activas en cada tablero.
- **Devolución de tarjetas:** Es válido devolver una tarjeta a una etapa anterior si se descubre información que invalida supuestos clave. Documentar el motivo.
- **Trazabilidad entre tableros:** Las tarjetas que avanzan de Upstream → I2LP, o de I2LP → L2MVP, deben mantener referencia cruzada al proyecto de origen.

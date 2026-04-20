# RESEARCH: Framework para Descriptores de Cargo Formales — CognitionBase

**Fecha:** 2026-04-20
**Path de investigación:** `.researches/20260420-job-descriptor-framework-cognitionbase/`
**Referencia base:** `docs/cognitionbase/3 - Permanent Docs/jobs/LEAD-DEV-AI.md`

---

## 1. Framework Conceptual: Cargo vs Rol vs Función vs Responsabilidad

### Jerarquía

```
CARGO / POSICIÓN  (slot formal en el organigrama — va en el contrato)
    └── ejerce uno o más ROLES  (patrón de comportamiento operativo)
            └── cada rol agrupa FUNCIONES  (dominio de acción)
                    └── cada función implica RESPONSABILIDADES  (obligaciones específicas de resultado)
                            └── cada responsabilidad descompone en TAREAS  (unidad atómica — va en procedimientos, no en JDs)
```

### Tabla de Definiciones

| Término | Definición Operativa | Ejemplo CognitionBase |
|---------|---------------------|----------------------|
| **Cargo** | Unidad organizacional formal con un ocupante. Aparece en contrato y organigrama. | Lead Dev AI |
| **Rol** | Conjunto de comportamientos y expectativas en un contexto operativo. Puede cambiar de cargo sin redefinir el cargo. | SDM (Service Delivery Manager) |
| **Función** | Agrupación de actividades relacionadas que producen un resultado definido. Dominio de acción dentro de un rol/cargo. | "Arquitectura de Producto (Blueprinting)" |
| **Responsabilidad** | Obligación específica de resultado o conducta. Nivel más granular del JD. | "Transformar ideas de producto en Blueprints técnicos con esquema de datos" |
| **Tarea** | Unidad atómica de trabajo. No aparece en JDs — va en manuales operativos. | "Crear diagrama ER para cada nuevo producto" |

### Reglas Clave

- **Cargo ≠ Rol:** Un cargo es permanente/formal; un rol es operativo/contextual. Puedes reasignar un rol sin cambiar el cargo.
- **Función ≠ Responsabilidad:** La función agrupa; la responsabilidad especifica.
- **"Posición" en español:** equivale al slot individual (puede haber 3 posiciones del mismo cargo). En uso coloquial chileno, "cargo" y "posición" se usan como sinónimos.

---

## 2. Template Recomendado: Descriptor de Cargo (Lean JD para AI-First Startups)

```markdown
# Perfil de Posición: [Nombre del Cargo]

**Empresa:** CognitionBase (Spinoff de innovación de 23people.io)
**Nivel:** [Junior | Mid | Senior | Staff]
**Modalidad:** [Remoto | Híbrido | Presencial]
**Fecha de actualización:** YYYY-MM-DD

---

## 1. Propósito del Cargo
[2-3 oraciones: por qué existe este cargo, qué valor produce, qué problema resuelve]

---

## 2. Posición en la Estructura
- **Reporta a:** [Cargo]
- **Es reportado por:** [Cargos que reportan, o "N/A"]
- **Colabora con:** [Cargos laterales clave]

---

## 3. Roles Ejercidos
**Rol Principal — [Nombre]:** [descripción 1-2 líneas]
**Rol Secundario — [Nombre]:** [descripción 1-2 líneas] *(si aplica)*

---

## 4. Funciones y Responsabilidades Principales
* **[Función]:** [descripción orientada a output]
* **[Función]:** [descripción orientada a output]
[5-8 funciones máximo]

---

## 5. Indicadores de Desempeño (KPIs del Cargo)
* **[KPI]:** [definición y target si aplica]
[3-5 KPIs]

---

## 6. Requisitos del Cargo (Excluyentes)
[Cada ítem aquí = knock-out en selección]
* **[Competencia]:** [nivel requerido]

---

## 7. Competencias Técnicas Clave
| Competencia | Nivel Esperado |
|-------------|----------------|
| [Skill]     | [Básico / Avanzado / Experto] |

---

## 8. Requisitos Deseables
* [Nice-to-have, no knock-out]

---

## 9. Niveles del Cargo *(solo para cargos con seniority track)*
| Dimensión   | Junior | Mid | Senior |
|-------------|--------|-----|--------|
| Scope       | ...    | ... | ...    |
| Autonomy    | ...    | ... | ...    |
| Impact      | ...    | ... | ...    |
| Mentorship  | ...    | ... | ...    |
```

### Secciones Obligatorias vs Opcionales

| Sección | Obligatoria | Notas |
|---------|-------------|-------|
| Propósito del Cargo | Sí | Responde "¿por qué existe este cargo?" |
| Posición en la Estructura | Sí | Organigrama mínimo |
| Roles Ejercidos | Sí (en CognitionBase) | Crítico cuando el cargo ejerce múltiples roles |
| Funciones y Responsabilidades | Sí | 5-8 funciones, redactadas en output |
| KPIs del Cargo | Sí (cultura data-driven) | 3-5 métricas que el cargo mueve |
| Requisitos Excluyentes | Sí | Son los knock-outs de selección |
| Competencias Técnicas | Recomendable | Referencia SFIA para naming |
| Requisitos Deseables | Opcional | Nice-to-have |
| Niveles del Cargo | Opcional | Solo si hay track de seniority |

---

## 3. Cómo Modelar Cargos con Múltiples Roles

### Patrón Recomendado para CognitionBase: Role Stack + mini-RACI

**En el descriptor de cargo** (sección "Roles Ejercidos"):

```markdown
## Roles Ejercidos

Este cargo ejerce dos roles operativos en CognitionBase:

**Rol Principal — Technical Lead (AI-First):**
Lidera la arquitectura técnica, la calidad de entregas y la mentalidad AI-First del equipo.

**Rol Secundario — SDM (Service Delivery Manager):**
Gestiona el flujo de solicitudes validadas por el SRM, asegurando que ingresen, se ejecuten
y se entreguen cumpliendo los SLAs y DoDs acordados.

> Esta dualidad es propia de la fase actual de CognitionBase. A medida que el equipo escale,
> el rol SDM podrá separarse en una posición independiente.
```

**Documento complementario opcional** (role-sdm.md / role card):

```markdown
# Role Card: SDM (Service Delivery Manager)

**Actualmente ejercido por:** Lead Dev AI
**Puede ser separado en posición independiente cuando:** el equipo supere N personas o el volumen de servicios lo justifique

## Propósito del Rol
Garantizar que las solicitudes validadas fluyan eficientemente desde el SRM hasta la entrega final.

## Outputs Clave del Rol
- Solicitudes ingresadas al flujo con level of quality correcto
- Entregas que cumplen DoDs y expectativas del cliente
- KPIs de Cycle-Time y Lead-Time dentro del target

## Interacciones del Rol
- Recibe: SRM (solicitudes validadas)
- Entrega a: SRM / Cliente (entregables finales)
- Gestiona: Iron-Legion (Dev AI + Agentes)
```

### Tres Patrones Disponibles

| Patrón | Descripción | Cuándo usar |
|--------|-------------|-------------|
| **Role Stack** | Descriptor único con sección "Roles Ejercidos" que lista roles explícitamente | Recomendado: startups lean, cargos que combinan liderazgo técnico + gestión |
| **Hybrid Role** | Descriptor integra funciones de ambos roles sin separación explícita | No recomendado: oscurece la dualidad y dificulta separar roles futuros |
| **Role Cards + RACI** | Documento separado mapea roles ↔ cargos. Complementa al descriptor. | Como capa adicional en equipos de 8+ personas |

### Niveles de Proficiencia en Role Cards

Cuando un mismo rol puede ejercerse con profundidades funcionalmente distintas, la Role Card debe incluir una tabla de niveles de proficiencia (A/B/C). Estos niveles son atributos del rol, no del cargo.

En el Descriptor de Cargo, Sección "Roles Ejercidos", se declara qué nivel de proficiencia se espera para ese cargo:

```markdown
**Rol Principal — Gestionador de Flujos de Trabajo (Nivel B):**
Gestiona el flujo Kanban del equipo, mide Cycle Time/Lead Time y produce
reportes de rendimiento operativo periódicos.
```

> Ver Sección 4b para la distinción entre proficiencia del rol y seniority del cargo.

---

## 4. Manejo de Niveles de Experiencia (Seniority Tracks)

### Recomendación: Modelo A (Cargo Único con Track Embebido)

Para CognitionBase en etapa actual, un solo descriptor por tipo de cargo con una sección de niveles al final. Reduce overhead de mantenimiento.

### Las 6 Dimensiones de Seniority (Radford/Mercer simplificado)

| Dimensión | Junior | Mid | Senior |
|-----------|--------|-----|--------|
| **Scope of Work** | Tareas asignadas, bien definidas | Proyectos con ambigüedad moderada | Sistemas / iniciativas estratégicas |
| **Autonomy** | Supervisado | Semi-autónomo | Define su propio trabajo |
| **Impact** | Individual | Equipo pequeño | Organización / producto |
| **Technical Complexity** | Conocido, predecible | Moderado, requiere análisis | Ambiguo, requiere diseño desde cero |
| **Mentorship** | Recibe mentoring | Mentoring puntual | Mentoring sistemático como parte del rol |
| **Communication** | Interna al equipo | Cross-team | Stakeholders / C-level |

### Aplicación a Dev AI en CognitionBase

```markdown
## Niveles del Cargo

| Dimensión     | Junior Dev AI             | Mid Dev AI                      | Senior Dev AI                        |
|---------------|---------------------------|----------------------------------|---------------------------------------|
| Scope         | Features definidas        | Módulos con ambigüedad moderada  | Arquitecturas de producto / sistemas  |
| Autonomy      | Bajo supervisión del Lead | Semi-autónomo, valida con Lead   | Autónomo, propone arquitecturas       |
| Impact        | Feature individual        | Sprint / entregable              | Velocidad y calidad del equipo        |
| AI Complexity | Uso de agentes definidos  | Diseño de flujos AI moderados    | Orquestación AI-First desde cero      |
| Mentorship    | Recibe                    | Puede dar mentoring puntual      | Mentoring sistemático de juniors      |
```

---

## 4b. Proficiencia por Rol vs. Seniority del Cargo

### Distinción Fundamental

Estas dos dimensiones son **ortogonales** — no colapsan ni se reemplazan mutuamente:

| Dimensión | Dónde se define | Qué modela |
|---|---|---|
| **Seniority Track** | Descriptor de Cargo, Sección 9 | *Cómo* trabaja la persona (autonomy, scope, impact, communication) |
| **Proficiency Level del Rol** | Role Card | *Qué sabe hacer* dentro del dominio funcional específico del rol |

Un Senior puede ejercer un rol en Nivel A si ese dominio es nuevo para él. Un Junior puede tener Nivel B en el mismo rol si lleva 3 años ejerciéndolo. El seniority track del cargo no predetermina el nivel de proficiencia en un rol.

### Cuándo Definir Niveles en una Role Card

Incluir tabla de niveles A/B/C en la Role Card cuando el mismo rol puede ejercerse con **capacidades funcionalmente distintas en profundidad**, sin que cambie la identidad del rol.

**No corresponde** crear roles separados cuando la diferencia es de profundidad (ej: "Gestionador Básico" vs "Gestionador Analítico") — eso fragmenta innecesariamente. Un solo rol con niveles internos preserva la trazabilidad de crecimiento.

### Escala de Proficiencia Recomendada

3 niveles (A/B/C) para CognitionBase en etapa actual. Mapeable a SFIA niveles 3–5 si se adopta el framework completo en el futuro.

| Nivel | Nombre Genérico | Descripción |
|---|---|---|
| A | **Ejecutor** | Aplica el proceso definido. Ejecuta con supervisión o guía. |
| B | **Analista** | Ejecuta y mide. Produce datos sobre el proceso y propone mejoras con sustento. |
| C | **Arquitecto** | Diseña, rediseña y transfiere. Define cómo debe funcionar el proceso para otros. |

### Ejemplo Aplicado: Gestionador de Flujos de Trabajo

| Nivel | Capacidades |
|---|---|
| A — Ejecutor | Ingresa solicitudes con calidad correcta. Mueve ítems según el proceso Kanban definido. Identifica y escala bloqueos. Verifica DoD antes de cerrar. Controla WIP dentro del límite. |
| B — Analista | Todo lo de A. Además: calcula Cycle Time y Lead Time por tipo de solicitud. Produce reportes de rendimiento (throughput, aging, WIP trends). Identifica cuellos de botella con datos. Propone ajustes al proceso con sustento métrico. |
| C — Arquitecto | Todo lo de B. Además: diseña o rediseña el flujo completo (columnas, políticas, DoDs). Define targets de Cycle/Lead Time. Implementa mejoras sistémicas. Entrena a otros en el proceso. |

### Regla de Asignación en el Descriptor de Cargo

En la Sección "Roles Ejercidos" del descriptor, declarar el nivel de proficiencia esperado para ese cargo:

```markdown
**Rol Principal — Gestionador de Flujos de Trabajo (Nivel B):**
Gestiona el flujo Kanban del equipo, mide Cycle Time/Lead Time y produce
reportes de rendimiento operativo periódicos.
```

Dos cargos distintos pueden ejercer el mismo rol en niveles distintos:

- "Coordinador Equipo A (Nivel A)": gestiona el flujo
- "Coordinador Equipo B (Nivel B)": gestiona el flujo y reporta métricas operativas

---

## 5. Nomenclatura Recomendada para CognitionBase

### Mapa de Términos

| Contexto | Término a Usar | Ejemplo |
|----------|---------------|---------|
| Contrato laboral / documento legal | **Cargo** | "Cargo: Lead Dev AI" |
| Descriptor formal / JD | **Perfil de Posición** o **Descriptor de Cargo** | Encabezado del documento |
| Comunicación operativa diaria (Notion, Slack) | **Rol** | "Tu rol como SDM esta semana..." |
| Organigrama / headcount | **Posición** | "Tenemos 2 posiciones abiertas de Dev AI" |
| LinkedIn / marca personal | **Title externo** | "AI Engineering Lead @ CognitionBase" |
| Documentos en inglés | **Job Position** (formal) / **Role** (operativo) | Según contexto |

### Convención Propuesta

```
Cargo Formal:     Lead Dev AI
Roles Ejercidos:  Technical Lead + SDM
Título Externo:   AI Engineering Lead @ CognitionBase
```

---

## 6. Frameworks Modernos — Cuáles Aplican en CognitionBase

| Framework | ¿Aplica ahora? | ¿Cómo? |
|-----------|----------------|--------|
| **Radford/Mercer Job Architecture** | Referencia solamente | Usar su nomenclatura de niveles (P1-P6) como referencia conceptual. No implementar la architecture completa hasta >20 personas. |
| **RACI** | Sí, parcial | Implementar RACI simplificado (solo R+A) para procesos clave: Idea2Market, Technical Evaluations. Complementa los descriptores. |
| **SFIA (Skills Framework for Information Age)** | Referencia para naming | Usar SFIA para nombrar y describir competencias técnicas. Evita inventar terminología. Especialmente útil para roles de software y AI. |
| **Competency Frameworks** | Sí, embebido | Incluir tabla de competencias técnicas en el descriptor. No construir un competency framework separado todavía. |
| **OKR-Linked JD** | Sí | Incluir sección de KPIs en el descriptor. Conecta el cargo con métricas reales (Cycle Time, Lead Time, DoD compliance). |
| **Role Cards** | Sí, nivel 2 | Crear role cards separadas para SDM y SRM como documentos complementarios al descriptor de cargo. |

---

## 7. Ejemplo Aplicado: Descriptor Mejorado Lead Dev AI

El descriptor existente en `LEAD-DEV-AI.md` es sólido en contenido pero le faltan:

1. **Sección "Propósito del Cargo"** — actualmente el propósito está mezclado con el contexto de empresa.
2. **Sección "Posición en la Estructura"** — no dice a quién reporta ni quién le reporta.
3. **Sección "Roles Ejercidos"** — la dualidad Technical Lead + SDM está implícita, debería ser explícita.
4. **Sección "KPIs del Cargo"** — se mencionan KPIs en las funciones pero no hay una sección dedicada.
5. **Sección "Competencias Técnicas"** — los requisitos son buenos pero no están en formato de competencias con nivel.
6. **Fecha de actualización** — falta.

### Gaps del Borrador Actual vs Template Recomendado

| Sección del Template | Estado en Borrador | Acción |
|----------------------|--------------------|--------|
| Identificación + metadata | Parcial (falta fecha) | Agregar fecha de actualización |
| Propósito del Cargo | Mezclado con contexto empresa (sección 1) | Separar en sección propia de 3 oraciones |
| Posición en la Estructura | Ausente | Agregar: reporta a CEO/fundador, reportado por Dev AI team |
| Roles Ejercidos | Implícito en sección 2 | Hacer explícito con sección propia |
| Funciones y Responsabilidades | Sí (sección 2) — buenas | Revisar redacción para orientar más a output |
| KPIs del Cargo | Mencionados en función 4 | Extraer a sección propia con 3-5 KPIs |
| Requisitos Excluyentes | Sí (sección 3) | Bien estructurados, mantener |
| Competencias Técnicas | Ausente como tabla | Convertir los requisitos en tabla con nivel |
| Requisitos Deseables | Sí (sección 4) | Mantener |

---

## 8. Stack Documental Recomendado para CognitionBase

```
Nivel 1 — Descriptores de Cargo (por cargo formal):
  jobs/
    LEAD-DEV-AI.md        ← mejorar con template
    DEV-AI.md             ← crear (con seniority track)
    SRM.md                ← crear

Nivel 2 — Role Cards (por rol operativo, opcional pero recomendable):
  roles/
    role-sdm.md
    role-srm.md
    role-tech-lead.md
    role-gestionador-flujos.md   ← incluir tabla de niveles A/B/C (ver Sección 4b)

  > Las Role Cards son documentos reutilizables: un mismo rol puede referenciarse
  > desde múltiples descriptores de cargo. Cuando el rol tiene variación de profundidad
  > funcional, incluir la tabla de niveles A/B/C como sección estándar de la Role Card.

Nivel 3 — RACI por proceso (cuando el equipo >5-6 personas):
  processes/
    raci-idea2market.md
    raci-tech-evaluation.md
```

---

## 8b. Market Research: Benchmarks para Lead Dev AI (2025-2026)

**Fuente:** `.planning/research/03-lead-dev-ai-market-research.md`

### Roles Equivalentes en el Mercado

El Lead Dev AI de CognitionBase es equivalente a: **AI Engineering Lead** (startups), **Staff AI Engineer** (scaleups), **Head of AI Engineering** (medianas).

### Requisitos de Mercado — Consenso (2025-2026)

- **Experiencia base:** 8+ años de ingeniería, 2+ años en sistemas LLM/agentes en producción
- **Frameworks obligatorios (>70% postings):** LangGraph, CrewAI, AutoGen, Claude Agents SDK, OpenAI Agents SDK
- **MCP (Model Context Protocol):** estándar emergente adoptado por OpenAI, Cursor, VS Code; ya aparece en postings senior
- **Observabilidad LLM:** LangSmith, Langfuse, RAGAS — no negociable para roles senior
- **AI coding workflow propio y transferible:** Claude Code, Cursor — se espera que el líder lo enseñe al equipo
- **Model tiering:** saber asignar tareas a modelos rápidos/baratos vs. potentes según el agente

### Stack de Producción Dominante en AI Startups (2025-2026)

```
Frontend:       Next.js + Vercel
Database:       Supabase (Postgres + Auth + Edge Functions)
AI Layer:       LangGraph / CrewAI / Anthropic Agents SDK + MCP servers
Observabilidad: LangSmith o Langfuse
Coding:         Claude Code + Cursor
```

### Bandas Salariales Chile

| Perfil | Rango mensual bruto |
|--------|---------------------|
| Senior Software Engineer (general) | CLP $3.8M–$5.7M |
| Tech Lead / Senior Lead (local) | CLP $5M–$7M |
| Lead Dev AI con especialización AI | CLP $5M–$9M |
| Premiums AI/DevOps/Cybersecurity vs. general | +15–20% |

### Gaps del Borrador vs. Best-in-Class

| Gap | Estado en JD actualizado |
|-----|--------------------------|
| Sin tech stack específico | Resuelto — tabla de 13 competencias |
| Sin KPIs como sección dedicada | Resuelto — sección 6 con 5 KPIs |
| Sin "Roles Ejercidos" explícito | Resuelto — sección 4 con patrón Role Stack |
| Sin salary range | Resuelto — CLP $5M–$8M en sección 12 |
| Sin primeros 90 días | Resuelto — sección 10 con estructura 30/60/90 |
| Sin path de crecimiento | Resuelto — sección 11 con 3 trayectorias |
| Sin proceso de selección | Resuelto — sección 13 con 5 etapas |
| Requisitos demasiado genéricos | Resuelto — requisitos con herramientas nombradas |

---

## 9. Decisiones y Open Questions

### Decisiones Tomadas en esta Investigación

1. Usar **Role Stack** (Patrón A) para documentar Lead Dev AI con su dualidad Technical Lead + SDM.
2. Usar **Modelo A** (cargo único con seniority track embebido) para Dev AI.
3. **No implementar** Radford/Mercer job architecture completa ahora — solo referencia conceptual.
4. Adoptar **SFIA** como vocabulario de referencia para competencias técnicas, no como sistema completo.
5. Incluir sección de **KPIs** en todos los descriptores (cultura output-first).
6. Término formal en español: **"Cargo"** para documentos legales; **"Rol"** para operativa.

### Open Questions

- ¿Cuál es el cargo formal del SRM? ¿Tiene funciones adicionales más allá del rol SRM?
- ¿El CEO/fundador tiene un cargo formal documentado o se gestiona de forma diferente?
- ¿Se desea incluir rangos salariales en los descriptores o mantenerlos separados?
- ¿Cuál es el criterio para separar el rol SDM en una posición independiente? (¿volumen de servicios? ¿número de Devs AI?)

---

## 9b. Referencia de Mercado: Niveles GetOnBrd (Chile/LATAM)

**Fuente:** https://www.getonbrd.com/help/politica-de-niveles-de-experiencia-seniorities
**Relevancia:** GetOnBrd es la plataforma principal de empleos tech en Chile/LATAM. CognitionBase publicará sus ofertas ahí.

### Escala de Seniority GetOnBrd

GetOnBrd define 5 niveles basados en competencias (no en años de experiencia):

| Nivel GetOnBrd | Criterio clave |
|---|---|
| **No Experience** | Sin autonomía; requiere supervisión constante |
| **Junior** | Supervisión frecuente; aprende independientemente |
| **Semi-Senior** | Supervisión mínima; toma decisiones sobre su propio trabajo |
| **Senior** | Sin supervisión de pares; revisa y enseña a otros; lidera equipos pequeños |
| **Expert** | Lidera equipos grandes y multicapa; estrategia corporativa; asesora C-suite |

### Mapeo al Framework CognitionBase

| Framework interno (Radford/Mercer ref.) | GetOnBrd | Nota |
|---|---|---|
| Junior | Junior | Equivalencia directa |
| Mid | Semi-Senior | Nivel propio del mercado LATAM — no existe en frameworks anglosajones |
| Senior | Senior | Equivalencia directa |
| Staff | Expert | GetOnBrd no tiene nivel "Staff"; "Expert" es el arquetipo equivalente |

### Decisiones de Publicación

1. **Lead Dev AI en GetOnBrd:** publicar como **Senior**. El cargo cae en el límite Senior/Expert; Senior es más preciso para el estadio actual y evita sobredimensionar expectativas salariales.
2. **Título externo vs. nivel de plataforma:** el título "AI Engineering Lead" en GetOnBrd comunica seniority sin requerir el nivel Expert.
3. **"Semi-Senior" en track Dev AI:** cuando se creen posiciones Mid Dev AI, publicarlas en GetOnBrd como Semi-Senior. Afecta bandas salariales esperadas por el mercado chileno.
4. **"Staff" no existe en GetOnBrd:** el nivel Staff del framework interno no tiene slot en la plataforma. Cualquier cargo Staff se publica como Senior o Expert según el perfil específico.

---

## 10. Validación de Universalidad del Framework

**Fecha:** 2026-04-20
**Caso de prueba:** Líder de Marketing en empresa tecnológica mediana/pequeña
**Fuente:** `.planning/research/02-marketing-lead-validation.md`

### Conclusión General

El framework es **universal en su estructura**. No requiere variantes por área funcional. Los únicos ajustes son **parámetros contextuales** dentro de secciones existentes, no cambios estructurales al template.

### Validación por Componente

| Componente del Framework | ¿Universal? | Observación |
|--------------------------|-------------|-------------|
| **Jerarquía Cargo → Rol → Función → Responsabilidad** | Sí | Válida para cualquier dominio. En Marketing las responsabilidades tienden más a ser de resultado de negocio; en Engineering, de proceso técnico. La distinción conceptual es idéntica. |
| **Patrón Role Stack** | Sí — más relevante aún | Un Líder de Marketing en startup ejerce típicamente 4 roles (Demand Gen, Brand, Content, Events). El patrón aplica y es incluso más crítico que en cargos técnicos. |
| **Template de 9 secciones** | Sí | Todas las secciones aplican a Marketing. No falta ninguna sección; solo cambian los valores de cada sección. |
| **6 Dimensiones de Seniority** | Mayormente sí | 5 de 6 son universales. "Technical Complexity" debe renombrarse como **"Domain Complexity"** y especificarse por función. |
| **Sección KPIs** | Sí — especialmente crítica | En Marketing los KPIs son métricas de negocio directas (MQLs, pipeline, CAC). La sección KPIs es aún más importante en Marketing que en Engineering. |

### La Única Adaptación Necesaria: "Domain Complexity"

La dimensión "Technical Complexity" del seniority track es la única que requiere re-etiquetado contextual. La propuesta es usar **"Domain Complexity"** en el template base, con especificaciones por función:

| Área Funcional | Nombre Específico de la Dimensión |
|----------------|----------------------------------|
| Engineering / AI | Technical Complexity |
| Marketing | Channel & Market Complexity |
| Operaciones | Process & Systems Complexity |
| Finanzas | Regulatory & Financial Complexity |
| Ventas | Deal & Account Complexity |

Las demás dimensiones (Scope, Autonomy, Impact, Mentorship, Communication) son universales sin modificación.

### Diferencia Real entre Dominios: Textura, no Estructura

La única diferencia relevante entre cargos técnicos y no técnicos es de **textura**:

- **Engineering:** funciones con límites más definidos, responsabilidades orientadas a artefactos (código, arquitectura), competencias técnicas evaluables con criterios precisos.
- **Marketing:** funciones con mayor interdependencia y overlap, responsabilidades orientadas a resultados de negocio (revenue, pipeline, brand), competencias medidas por experiencia en herramientas y canales.

La distinción función/responsabilidad es **igualmente válida** en ambos dominios. En Marketing:

- **Función** = dominio de acción: "Gestión de Demanda", "Marketing de Contenidos", "Gestión de Marca"
- **Responsabilidad** = obligación de resultado: "Alcanzar 50 MQLs por trimestre con CAC < $X"

### KPIs Canónicos para Líder de Marketing en Tech

| KPI | Categoría |
|-----|-----------|
| MQLs generados por trimestre | Demanda |
| Pipeline de marketing generado ($) | Demanda / Negocio |
| Tasa de conversión MQL → SQL | Alineación Marketing-Ventas |
| CAC (Customer Acquisition Cost) | Eficiencia |
| Costo por MQL | Eficiencia |
| Crecimiento de tráfico orgánico | Contenido / SEO |

---

## 11. Ejemplo Aplicado: Descriptor de Líder de Marketing

El siguiente ejemplo demuestra el template de 9 secciones aplicado a un cargo no técnico en una empresa tech mediana/pequeña.

```markdown
# Perfil de Posición: Líder de Marketing

**Empresa:** [Empresa Tech]
**Nivel:** Senior / Lead
**Modalidad:** Híbrido
**Fecha de actualización:** 2026-04-20

---

## 1. Propósito del Cargo

El Líder de Marketing existe para convertir la visibilidad de la empresa en demanda calificada y en
una marca reconocida en su segmento. Es el responsable de que el equipo de ventas tenga un pipeline
continuo de prospectos que conocen y confían en la empresa antes del primer contacto comercial.

---

## 2. Posición en la Estructura

- **Reporta a:** CEO / COO
- **Es reportado por:** Marketing Specialist / Coordinator (cuando el equipo crece)
- **Colabora con:** Ventas (alineación MQL→SQL), Producto (product marketing), Diseño (marca)

---

## 3. Roles Ejercidos

Este cargo ejerce cuatro roles operativos:

**Rol Principal — Demand Generation Manager:**
Diseña y ejecuta la estrategia de generación de demanda (SEO, SEM, email, paid social, eventos)
para llenar el pipeline de ventas con MQLs calificados.

**Rol Secundario — Brand Manager:**
Gestiona la identidad de marca, la narrativa de empresa y la coherencia en todos los canales.

**Rol Secundario — Content Strategist:**
Define la arquitectura de contenidos, el calendario editorial y la estrategia de distribución.

**Rol Secundario — Event Coordinator:**
Planifica la participación de la empresa en eventos estratégicos para visibilidad y generación de leads.

> Esta multiplicidad de roles es característica de la etapa actual. A medida que el equipo crezca,
> los roles de Brand, Content y Events pueden separarse en posiciones independientes.

---

## 4. Funciones y Responsabilidades Principales

* **Gestión de Demanda:** Diseñar, ejecutar y optimizar campañas para alcanzar los objetivos trimestrales de MQLs y pipeline de marketing.
* **Marketing Digital:** Gestionar el ecosistema digital (SEO, SEM, social, email) garantizando crecimiento del tráfico orgánico y eficiencia en canales paid.
* **Gestión de Marca:** Asegurar coherencia de marca en todos los materiales; gestionar la narrativa de empresa hacia el mercado objetivo.
* **Marketing de Contenidos:** Producir y distribuir contenido relevante para el ICP que genere demanda y posicione la empresa como referente.
* **Participación en Eventos:** Seleccionar, gestionar y maximizar el ROI de la participación en eventos del sector.
* **Analítica y Reporte:** Medir y reportar el performance de todas las iniciativas; traducir datos en decisiones de optimización.
* **Alineación con Ventas:** Definir criterios de calificación de leads y revisar la calidad del pipeline generado.

---

## 5. Indicadores de Desempeño (KPIs del Cargo)

* **MQLs generados por trimestre:** [target según capacidad del equipo de ventas]
* **Pipeline de marketing generado:** [$X en oportunidades calificadas por trimestre]
* **Tasa de conversión MQL → SQL:** [target acordado con ventas]
* **Costo por MQL:** [target según presupuesto disponible]
* **Crecimiento de tráfico orgánico:** [% trimestral]

---

## 6. Requisitos del Cargo (Excluyentes)

* **Experiencia en demand generation:** Mínimo 3 años gestionando campañas B2B con métricas de pipeline y MQLs.
* **Gestión de presupuesto de marketing:** Experiencia con accountability de ROMI.
* **Marketing automation:** Dominio de al menos una plataforma (HubSpot, Marketo, o equivalente).
* **Capacidad analítica:** Habilidad para leer datos de marketing y tomar decisiones basadas en métricas.

---

## 7. Competencias Técnicas Clave

| Competencia / Herramienta | Nivel Esperado |
|---------------------------|----------------|
| CRM / Marketing Automation (HubSpot / Marketo) | Avanzado |
| Google Ads / LinkedIn Ads | Avanzado |
| Google Analytics / GA4 | Avanzado |
| SEO (on-page, off-page, contenido) | Intermedio-Avanzado |
| Email marketing y nurturing | Avanzado |

---

## 8. Requisitos Deseables

* Experiencia en marketing de SaaS o servicios tech B2B
* Conocimiento de ABM (Account-Based Marketing)
* Experiencia construyendo equipos de marketing desde cero

---

## 9. Niveles del Cargo

| Dimensión | Marketing Specialist | Marketing Lead | Head of Marketing |
|-----------|---------------------|----------------|-------------------|
| Scope | Campañas de un canal | Multi-canal, gestión de pipeline | Estrategia de marketing completa |
| Autonomy | Supervisado | Semi-autónomo, valida con CEO | Define estrategia y presupuesto |
| Impact | Campaña individual | Pipeline trimestral | Revenue y posicionamiento de marca |
| Domain Complexity | Un canal conocido | Multi-canal, atribución simple | Full-funnel, brand + demand, ABM |
| Mentorship | Recibe | Mentoring puntual | Forma y lidera equipo |
| Communication | Interna al equipo | Cross-team (ventas, producto) | C-level, board, agencias, mercado |
```

---

*Investigación completada: 2026-04-20*
*Fuentes: SHRM, Radford/Mercer frameworks, SFIA v9, mejores prácticas de GitHub/Stripe/Linear para career ladders, literatura de job architecture para tech startups. Validación de universalidad: HubSpot Marketing benchmarks, Forrester SiriusDecisions, Gartner Marketing 2024, Lenny's Newsletter, a16z portfolio company practices.*

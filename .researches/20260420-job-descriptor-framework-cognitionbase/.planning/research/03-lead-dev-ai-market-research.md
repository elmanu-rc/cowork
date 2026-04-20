# Research: Market Benchmarks y Mejores Prácticas — Lead Dev AI (AI-First Startup)

**Fecha:** 2026-04-20
**Propósito:** Enriquecer el descriptor de cargo Lead Dev AI de CognitionBase con benchmarks de mercado, landscape de herramientas de orquestación AI, y mejores prácticas de job descriptors para roles técnicos senior.

---

## 1. Benchmarks de Mercado: ¿Qué Piden las Empresas AI-First para Roles Equivalentes?

### Roles Equivalentes en el Mercado Global

Los roles más cercanos al Lead Dev AI de CognitionBase en el mercado son:

- **AI Engineering Lead** (startups de Series A-B)
- **Staff AI Engineer** (scaleups con ingeniería madura)
- **Head of AI Engineering** (empresas medianas con departamento de AI)
- **Senior Agentic AI Engineer** (empresas especializadas en agentes)

### Requisitos Técnicos Más Frecuentes (2025-2026)

Basado en análisis de postings de Datadog, Capital One, Deloitte, y startups de la ecosistema LangChain/CrewAI/Anthropic:

**Experiencia base:**

- 8+ años de ingeniería de software, con mínimo 2+ años enfocados en sistemas LLM/agentes en producción
- Demostrable experiencia llevando agentes de PoC a producción con observabilidad real

**Frameworks de agentes (requeridos en >70% de postings):**

- LangGraph — modelado de workflows AI como grafos dirigidos con estado persistente
- CrewAI — orquestación basada en roles/tareas, baja barrera de entrada
- AutoGen (Microsoft Research) — conversación asíncrona multi-agente
- Claude Agents SDK / Anthropic Agents API — arquitectura con constitutional AI
- OpenAI Agents SDK — lanzado en marzo 2025, amplia adopción

**Protocolos y estándares emergentes:**

- MCP (Model Context Protocol) — estándar de Anthropic para conectar modelos con herramientas externas. Lanzado en Nov 2024, adoptado por OpenAI en marzo 2025. 97M+ descargas mensuales del SDK. Ya es requisito en postings senior.
- A2A Protocol — protocolo de comunicación agent-to-agent, emergente en 2026

**Observabilidad y evaluación de LLMs (requeridos en roles senior):**

- LangSmith, RAGAS, Arize, PromptFlow
- Definición de métricas de calidad para sistemas AI en producción

**Stack de desarrollo productivo:**

- AI coding tools: Claude Code, Cursor, GitHub Copilot, Windsurf — se espera que el líder tenga un workflow personal que lo haga 2-3x más rápido Y sepa transferirlo al equipo
- Infraestructura: Docker, Kubernetes, cloud (AWS/GCP/Azure), CI/CD para sistemas AI

**Liderazgo técnico específico a AI:**

- Model tiering: saber cuándo usar modelos rápidos/baratos (Claude Haiku, GPT-4o-mini) vs. modelos potentes (Claude Sonnet, GPT-5) según el agente/tarea
- Experience definiendo y manteniendo guardrails de safety y compliance para agentes autónomos

### Stack de Producción Más Común en AI Startups (2025-2026)

Para Landing Pages, Demos y MVPs (caso CognitionBase):

```
Frontend:        Next.js + Vercel (deploy instantáneo)
Database:        Supabase (Postgres + Auth + Storage + Edge Functions)
AI Layer:        LangGraph / CrewAI / Anthropic Agents SDK + MCP servers
Observability:   LangSmith o Langfuse
Coding:          Claude Code + Cursor
Payments:        Stripe
Analytics:       PostHog o Vercel Analytics
```

---

## 2. Bandas Salariales para Roles Senior AI en LATAM (2025-2026)

### Datos de Mercado

**Chile (mercado local):**

- Senior Software Engineer (general): CLP 35M–57M anuales (USD ~38K–62K)
- Tech Lead / Senior Lead: USD $5,000–$7,000/mes para trabajo remoto internacional
- AI/ML Engineer senior (especialización): premiums de 15–20% sobre senior general
- Proyección: sueldos de AI, DevOps y ciberseguridad crecerán 12–18% en 2026

**Benchmark Lead Dev AI en CognitionBase (estimado):**

- Mercado chileno local (híbrido): CLP 5M–8M/mes bruto (USD ~5,500–8,700/mes)
- Con especialización AI demostrable: CLP 6M–9M/mes bruto
- Nota: CognitionBase opera como spinoff de 23people, empresa ya establecida — contexto de empleador conocido en el mercado

**LATAM regional (remoto para clientes USD):**

- Senior AI Engineer: USD $4,000–$8,000/mes
- AI Engineering Lead / Head of AI: USD $8,000–$15,000/mes
- Nota: el rango es amplio por variación de país, cliente (local vs. USD), y nivel real de seniority

**Tasa de cambio referencia (2026-04-18):** 1 USD = $920 CLP

---

## 3. Landscape de Frameworks AI para Orquestación (2025-2026)

### Mapa del Ecosistema

#### Tier 1: Frameworks Maduros y Ampliamente Adoptados

| Framework | Fortaleza | Curva de Aprendizaje | Casos de uso ideales |
|-----------|-----------|---------------------|---------------------|
| **LangGraph** | Workflows stateful, branching paralelo, lógica condicional precisa | Media-Alta | Flujos complejos que requieren estado persistente, debugging exhaustivo |
| **CrewAI** | Role-based agents, API muy legible, rápido de prototipar | Baja | Equipos con múltiples agentes con roles definidos; MVPs rápidos |
| **AutoGen** | Conversación asíncrona multi-agente, buena para tareas largas | Media | Tareas de larga duración, agentes especializados que se coordinan |

#### Tier 2: SDKs de Proveedores (Crecimiento Fuerte)

| SDK | Proveedor | Diferenciador | Relevancia para CognitionBase |
|-----|-----------|---------------|-------------------------------|
| **Claude Agents SDK** | Anthropic | Constitutional AI built-in, safety por diseño | Alta — alineación con el stack AI de CognitionBase |
| **OpenAI Agents SDK** | OpenAI | Amplia adopción, ecosistema maduro | Alta — estándar de facto en muchos equipos |
| **Google ADK** | Google | Integración con Vertex AI | Media — relevante si se usan modelos Gemini |
| **Strands Agents** | AWS | Integración con Bedrock | Baja-Media para CognitionBase |

#### Tier 3: Protocolos y Estándares (Capa de Interoperabilidad)

| Protocolo | Origen | Estado | Relevancia |
|-----------|--------|--------|------------|
| **MCP (Model Context Protocol)** | Anthropic (Nov 2024) | Adoptado por OpenAI, Cursor, VS Code, Claude. 97M+ SDK downloads. Entra en Linux Foundation AAIF (Dic 2025) | Crítica — es el estándar emergente para conectar LLMs con herramientas |
| **A2A Protocol** | Industria (2026) | Emergente | Relevante a futuro para comunicación agent-to-agent |

### Patrón Best Practice: Model Tiering

Un patrón clave de producción que distingue a ingenieros senior en 2025-2026:

```
Routing Agent (Haiku / GPT-4o-mini):  triage, clasificación, routing — barato y rápido
↓
Specialist Agents (Sonnet / GPT-4o):  razonamiento, generación de código, análisis
↓
Review / Safety Agent (Sonnet):        validación, guardrails, compliance check
↓
Output
```

El Lead Dev AI debe conocer este patrón y poder aplicarlo en las entregas de CognitionBase.

### Observabilidad — Pilar No Negociable

Independiente del framework elegido, todo sistema agentic en producción requiere:

- Tracing de llamadas LLM (LangSmith, Langfuse)
- Métricas de calidad (RAGAS para RAG, métricas custom para agentes)
- Alertas por degradación de calidad o costo
- Mecanismo de revisión humana (human-in-the-loop)

---

## 4. Mejores Prácticas de Job Descriptors para Talento Técnico Senior

### Qué Incluyen los JDs de Alta Conversión

**Estructura que funciona para roles senior (basado en análisis de LinkedIn, Indeed, Growth Shuttle 2026):**

1. **Claridad inmediata de scope** — en las primeras 3 líneas, el candidato debe entender exactamente qué tamaño de equipo lidera, en qué dominio, y qué problema resuelve
2. **Compensación transparente** — incluir salary range sube la calidad de aplicaciones; candidatos senior no aplican a postings sin rango
3. **Tech stack específico** — candidatos senior quieren saber exactamente con qué trabajan antes de invertir tiempo en aplicar
4. **Crecimiento profesional** — qué puede aprender o hacia dónde puede crecer en el cargo
5. **Primeros 90 días** — reduce incertidumbre; candidatos senior quieren saber cómo luce el éxito temprano
6. **Cultura sin buzzwords** — "work hard, play hard" y "rockstar" alejan candidatos senior; prefieren descripción directa y honesta
7. **Proceso de selección claro** — cuántas etapas, cuánto tiempo, qué evalúan

**Longitud óptima:** 800–1,200 palabras para publicación en LinkedIn/careers page. Más largo se abandona en mobile.

**Formato:** Bullets para responsabilidades y requisitos. Párrafos para contexto y cultura. H2 claros para navegación.

### Lo Que Aleja a Candidatos Senior en 2025

- Listas de requisitos de >12 ítems (señal de que el equipo no sabe qué necesita)
- "Rockstar", "ninja", "guru" — desprestigian al empleador
- Sin rango salarial (candidatos senior lo interpretan como señal de oferta por debajo del mercado)
- Sin descripción de la stack o vaga ("experiencia en tecnologías modernas")
- Descripción de funciones orientadas a actividades, no a resultados

### El 90-Day Success Plan como Diferenciador

Incluir una sección "¿Cómo se ve el éxito en los primeros 90 días?" mejora significativamente la conversión porque:

- Comunica que la empresa tiene claridad de expectativas (señal de madurez)
- Permite al candidato auto-filtrar (si el plan no le parece factible, no aplica — ahorra tiempo a ambos)
- Alinea expectativas antes del primer día

**Estructura de los 90 días para un Lead Dev AI:**

- **Días 1-30 (Aprende):** Onboarding técnico, conocer los servicios, entender los KPIs actuales
- **Días 31-60 (Contribuye):** Primera entrega end-to-end, primera propuesta de mejora al flujo
- **Días 61-90 (Lidera):** Primer ciclo completo de entrega autónomo, Iron-Legion operando a velocidad de crucero

---

## 5. Gaps del Borrador Actual vs. Best-in-Class

Sobre la base del análisis anterior, el borrador de `LEAD-DEV-AI.md` le faltan las siguientes secciones para ser un JD de alto impacto:

| Gap | Impacto en Conversión | Solución |
|-----|----------------------|----------|
| **Sin tech stack específico** | Alto — candidatos senior no aplican | Agregar tabla de competencias técnicas con herramientas concretas |
| **Sin KPIs del cargo como sección** | Medio — rompe con cultura Output-First | Extraer a sección dedicada con 4-5 métricas |
| **Sin sección "Roles Ejercidos"** | Medio — ambigüedad sobre la dualidad del cargo | Sección explícita Technical Lead + SDM |
| **Sin salary range** | Alto — señal negativa para candidatos senior | Incluir rango en CLP o indicar "conversacional" + benchmark |
| **Sin primeros 90 días** | Medio — reduce incertidumbre y mejora auto-filtro | Sección "Éxito en los primeros 90 días" |
| **Sin path de crecimiento** | Medio — candidatos senior evalúan futuro | Agregar párrafo sobre hacia dónde puede crecer el cargo |
| **Requisitos demasiado genéricos** | Alto — "stacks modernos" no discrimina | Especificar: LangGraph, CrewAI, MCP, Next.js, Supabase, etc. |

---

## 6. Fuentes

- Indeed, Dice, Datadog Careers, Capital One Careers — postings de Staff AI Engineer / Agentic AI Engineer (Abril 2026)
- remotely talents, qubit-labs, mismo.team, howdy.com — salary benchmarks LATAM 2025-2026
- Talently, it-hunter.cl, levels.fyi — salary data Chile específicamente
- langfuse.com, getmaxim.ai, gurusup.com, datacamp.com — comparativas de frameworks AI
- modelcontextprotocol.io, linuxfoundation.org, thoughtworks.com — MCP y ecosistema agentic
- growthshuttle.com, techtarget.com, indeed.com/hire — best practices para JDs de talento técnico
- asana.com, clearcompany.com — 30-60-90 day onboarding plans

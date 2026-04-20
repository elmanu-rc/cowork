# Research: Validación del Framework para Cargos No Técnicos — Caso Líder de Marketing

**Fecha:** 2026-04-20
**Propósito:** Determinar si el framework Cargo → Rol → Función → Responsabilidad, el patrón Role Stack y el template de 9 secciones son universales o requieren variantes para cargos no técnicos, usando como caso de prueba el cargo de Líder de Marketing en una empresa tecnológica.

---

## 1. ¿El Framework Cargo → Rol → Función → Responsabilidad Aplica para Cargos No Técnicos?

### Veredicto: Sí, con una diferencia de textura, no de estructura

La jerarquía conceptual es válida para cualquier dominio funcional. La distinción cargo/rol/función/responsabilidad no es específica de ingeniería de software: proviene de teoría organizacional (SHRM, Mercer, job architecture) y se aplica a cualquier área de una empresa.

**Diferencia real en Marketing vs Engineering:**

En ingeniería, la distinción entre función y responsabilidad suele ser relativamente clara porque las funciones tienen límites técnicos más definidos (ej: "Arquitectura de sistemas" es claramente distinto de "Code review"). En Marketing, las funciones tienen mayor interdependencia y overlap:

- La función "Gestión de campañas de demanda" intersecta inevitablemente con "Gestión de contenidos", "Gestión de marca" y "Analítica de marketing".
- Las responsabilidades de Marketing tienden a ser más relacionales y dinámicas (dependen del ciclo de compra del mercado, del comportamiento del buyer) que las de Engineering (que dependen más de specs técnicas internas).

**Sin embargo, la jerarquía sigue siendo operativa:**

```
CARGO: Líder de Marketing
    └── ejerce ROLES: Demand Gen Manager, Brand Manager, Content Strategist, Event Coordinator
            └── cada rol agrupa FUNCIONES: "Gestión de pipeline de demanda", "Gestión de marca", etc.
                    └── cada función implica RESPONSABILIDADES: "Alcanzar objetivo trimestral de MQLs", etc.
                            └── cada responsabilidad descompone en TAREAS: "Crear campaña en HubSpot para segmento X"
```

### Diferencia de Modelado: Responsabilidades de Resultado vs Responsabilidades de Proceso

En cargos de Engineering, las responsabilidades tienden a ser **responsabilidades de proceso** ("Revisar cada PR antes de merge", "Mantener DoDs actualizados"). En Marketing, la tendencia es a **responsabilidades de resultado** directamente ligadas a métricas de negocio:

- "Garantizar que el pipeline de marketing aporte un mínimo de $X en oportunidades calificadas por trimestre"
- "Mantener el CAC por debajo de $Y en el canal de adquisición digital"

Esto no invalida el framework; refuerza el principio Output-First. En Marketing, el output es aún más visible y directamente medible que en algunas áreas técnicas.

---

## 2. El Patrón Role Stack para Cargos de Marketing con Múltiples Roles

### Veredicto: Completamente válido — es incluso más crítico en Marketing que en Engineering

El cargo de Líder de Marketing en una empresa tech mediana o pequeña típicamente ejerce cuatro roles simultáneos:

| Rol | Descripción | % tiempo estimado (startup) |
|-----|-------------|----------------------------|
| **Demand Gen Manager** | Diseña y ejecuta estrategia de generación de demanda (paid, SEO, email, eventos) para llenar el pipeline de ventas | 40-50% |
| **Brand Manager** | Gestiona identidad de marca, tono de comunicación, coherencia visual y narrativa | 15-20% |
| **Content Strategist** | Define arquitectura de contenidos, calendario editorial, distribución de contenido | 20-25% |
| **Event Coordinator** | Planifica y ejecuta participación en eventos (sponsorships, demos, meetups, webinars) | 10-15% |

Este es un caso de **Role Stack más pronunciado que en engineering**: un Lead Dev AI ejerce 2 roles; un Líder de Marketing puede ejercer 4.

### ¿Cómo se adapta el patrón Role Stack?

La sección "Roles Ejercidos" del template funciona igual, con extensión a roles adicionales:

```markdown
## Roles Ejercidos

Este cargo ejerce cuatro roles operativos:

**Rol Principal — Demand Generation Manager:**
Diseña y ejecuta la estrategia de generación de demanda para llenar el pipeline de ventas con MQLs calificados.

**Rol Secundario — Brand Manager:**
Gestiona la identidad, narrativa y coherencia de marca en todos los canales de comunicación.

**Rol Secundario — Content Strategist:**
Define la arquitectura de contenidos, el calendario editorial y la estrategia de distribución.

**Rol Secundario — Event Coordinator:**
Planifica la participación de la empresa en eventos relevantes para visibilidad de marca y generación de leads.

> Esta multiplicidad de roles es característica de empresas tech en etapa de crecimiento temprano/medio.
> A medida que el equipo de marketing crezca, los roles de Brand, Content y Events pueden separarse
> en posiciones independientes.
```

### Límite del Patrón: Cuando 4 Roles Generan Ambigüedad de Prioridades

Con 4 roles, el riesgo del Role Stack es que el ocupante no tenga claridad sobre qué priorizar cuando los roles compiten por tiempo. La solución es declarar explícitamente el **rol principal** (usualmente Demand Gen en startups tech, donde el CEO prioriza pipeline) y tratar los demás como secundarios.

---

## 3. Las 6 Dimensiones de Seniority (Radford/Mercer) — ¿Universales para Marketing?

### Veredicto: 5 de 6 son universales; "Technical Complexity" requiere re-etiquetado

| Dimensión | ¿Aplica a Marketing? | Adaptación requerida |
|-----------|---------------------|---------------------|
| **Scope of Work** | Sí, directa | Sin cambios |
| **Autonomy** | Sí, directa | Sin cambios |
| **Impact** | Sí, directa | Sin cambios |
| **Technical Complexity** | Parcialmente | En Marketing se reemplaza por **"Ambigüedad Estratégica"** o **"Channel Complexity"** |
| **Mentorship** | Sí, directa | Sin cambios |
| **Communication** | Sí, mayor énfasis | En Marketing la dimensión de comunicación con stakeholders (C-level, Board, ventas) es más central que en Engineering |

### Dimensión Alternativa para Marketing: "Strategic Ambiguity / Market Complexity"

En lugar de "Technical Complexity" (que mide dificultad técnica del trabajo), para Marketing es más relevante:

**"Channel & Market Complexity":** mide la capacidad de operar en entornos de alta ambigüedad de mercado, con múltiples canales, buyers con comportamientos variables y métricas de atribución no lineales.

| Dimensión | Marketing Junior | Marketing Mid | Marketing Senior/Lead |
|-----------|-----------------|---------------|----------------------|
| Scope | Campañas definidas, un canal | Multi-canal, cierta ambigüedad | Estrategia de mercado, presupuesto total |
| Autonomy | Bajo supervisión | Semi-autónomo, valida con lead | Define estrategia y presupuesto |
| Impact | Campaña individual | Quarter/canal | Revenue pipeline completo |
| Channel Complexity | Un canal conocido (ej: email) | Multi-canal con atribución simple | Full-funnel, atribución compleja, brand + demand |
| Mentorship | Recibe | Mentoring puntual a juniors | Mentoring sistemático, forma el equipo |
| Communication | Interna al equipo | Cross-team (ventas, producto) | C-level, board, agencias, eventos públicos |

### Conclusión sobre Universalidad de las 6 Dimensiones

La dimensión "Technical Complexity" es la única que requiere adaptación contextual por dominio funcional. Las otras 5 son completamente universales. La propuesta es renombrar esa dimensión como **"Domain Complexity"** en el template base, con una nota que indica que cada área funcional puede especificarla:

- Engineering: "Technical Complexity"
- Marketing: "Channel & Market Complexity"
- Operaciones: "Process & Systems Complexity"
- Finanzas: "Regulatory & Financial Complexity"

---

## 4. Convenciones de la Industria para Títulos y Niveles en Marketing Tech

### Jerarquía de Títulos en Marketing (B2B Tech / SaaS)

La jerarquía más común en empresas tech (startups a scaleups) es la siguiente:

```
Individual Contributors:
  Marketing Coordinator / Marketing Analyst (Junior)
  Marketing Specialist / Demand Gen Specialist / Content Specialist (Mid)
  Marketing Manager / Demand Gen Manager / Content Manager (Senior IC)
  Senior Marketing Manager / Growth Manager (Senior IC avanzado)

Management Track:
  Marketing Lead / Team Lead (liderando 1-3 personas)
  Marketing Manager (liderando equipo pequeño, ~3-5 personas)
  Head of Marketing / VP of Marketing (liderando departamento)
  CMO / Chief Marketing Officer (liderando función completa, C-level)

Especialidades frecuentes:
  Growth Lead / Growth Manager (foco en growth hacking / PLG)
  Demand Generation Manager (foco en pipeline)
  Brand Manager (foco en marca e identidad)
  Product Marketing Manager / PMM (intersección producto-marketing)
  Content Strategist (foco en contenidos)
  SEO Manager / Paid Acquisition Manager (canales específicos)
```

### Mapa de Equivalencias Radford para Marketing (niveles P)

| Título | Equivalente Radford | Descripción |
|--------|-------------------|-------------|
| Marketing Coordinator | P1-P2 | Ejecuta tareas definidas bajo supervisión |
| Marketing Specialist | P2-P3 | Semi-autónomo en su canal/área |
| Marketing Manager | P3-P4 | Autónomo, impacto en equipo o función |
| Senior Marketing Manager | P4-P5 | Dirige iniciativas estratégicas, cross-team |
| Head of Marketing / VP | P5-P6 o M3-M4 | Lidera departamento, impacto organizacional |
| CMO | M5 o E-band | C-level, impacto en empresa completa |

### Títulos en Startups Pequeñas (caso CognitionBase-like)

En una empresa tech de 5-15 personas, el cargo de "Líder de Marketing" suele tener los títulos externos más comunes:

- **Growth Lead** (si el foco es growth hacking + pipeline)
- **Marketing Lead** (genérico, común en startups hispanas)
- **Head of Marketing** (si tiene autonomía estratégica total aunque sea team of one)
- **Demand Generation Manager** (si el foco principal es pipeline)

El título externo (LinkedIn) puede diferir del cargo interno. Una empresa de 8 personas puede tener un "Head of Marketing" que ejecuta operacionalmente lo que en una empresa de 200 haría un "Marketing Manager".

---

## 5. KPIs Canónicos para Líder de Marketing en Empresas Tech

### KPIs del Funnel de Demanda (los más universales)

| KPI | Definición | Quién lo mueve |
|-----|-----------|----------------|
| **MQLs generados** | Leads calificados por marketing según criterios acordados (ICP, engagement score, etc.) | Demand Gen / Toda el área |
| **SQL conversion rate** | % de MQLs que ventas acepta como SQLs (Sales Qualified Leads) | Marketing + Alineación con Ventas |
| **Pipeline generado por marketing** | Valor monetario ($) de oportunidades abiertas atribuidas a marketing | Demand Gen |
| **CAC (Customer Acquisition Cost)** | Costo total de marketing + ventas / nuevos clientes adquiridos | Marketing + Finanzas |
| **Costo por MQL** | Presupuesto de marketing / MQLs generados | Demand Gen |
| **Retorno sobre inversión en marketing (ROMI)** | Revenue atribuido a marketing / inversión en marketing | CMO / Marketing Lead |

### KPIs de Contenido y Marca

| KPI | Definición | Relevancia |
|-----|-----------|------------|
| **Organic traffic** | Sesiones orgánicas al sitio web | SEO / Content |
| **Engagement rate** | Interacciones / impresiones en redes sociales | Social / Brand |
| **Share of Voice** | Presencia de la marca vs competidores en el mercado | Brand |
| **Brand awareness / recall** | Medición de reconocimiento (encuestas, búsquedas directas) | Brand |
| **Email open rate / CTR** | Performance de campañas de email nurturing | Demand Gen / Content |

### KPIs de Eventos

| KPI | Definición |
|-----|-----------|
| **Leads generados por evento** | MQLs atribuidos a participación en eventos |
| **Costo por lead de evento** | Inversión en evento / leads generados |
| **Pipeline atribuido a eventos** | Oportunidades que tuvieron primer touchpoint en un evento |

### KPIs Recomendados para el Template (para un Líder de Marketing en Startup Tech)

```markdown
## 5. Indicadores de Desempeño (KPIs del Cargo)

* **MQLs generados por trimestre:** [target según ciclo de ventas]
* **Pipeline de marketing generado:** [$X en oportunidades calificadas por trimestre]
* **Costo por MQL:** [target según presupuesto y benchmark del sector]
* **Tasa de conversión MQL → SQL:** [target acordado con el equipo de ventas]
* **Crecimiento de tráfico orgánico:** [% de crecimiento trimestral / anual]
```

Nota: En una startup de 5-15 personas con un solo cargo de marketing, los KPIs de negocio (pipeline, MQLs) son más relevantes que los KPIs de canal (engagement rate, CTR) porque el Líder de Marketing es accountable del resultado, no solo de la actividad.

---

## 6. ¿El Template de 9 Secciones es Suficientemente Genérico?

### Análisis Sección por Sección

| Sección | ¿Funciona para Marketing? | Ajuste requerido |
|---------|--------------------------|-----------------|
| **1. Propósito del Cargo** | Sí, completamente | Ninguno |
| **2. Posición en la Estructura** | Sí, completamente | Ninguno |
| **3. Roles Ejercidos** | Sí — especialmente importante para Marketing que tiene más roles simultáneos | Aumentar el número de roles listados (hasta 4) |
| **4. Funciones y Responsabilidades** | Sí | Nota: en Marketing, las funciones tienden a ser más transversales; puede necesitarse explicitar la relación entre funciones y roles |
| **5. KPIs del Cargo** | Sí — es la sección más crítica en Marketing | Los KPIs deben incluir métricas de negocio (pipeline, MQLs), no solo actividad |
| **6. Requisitos Excluyentes** | Sí | En Marketing los excluyentes son más de experiencia (haber gestionado campañas end-to-end) que de certificación formal |
| **7. Competencias Técnicas** | Sí, con variación | Para Marketing: herramientas (HubSpot, Google Ads, Analytics), no lenguajes de programación; nivel "Avanzado" tiene significado diferente |
| **8. Requisitos Deseables** | Sí, completamente | Ninguno |
| **9. Niveles del Cargo** | Sí | Reemplazar "Technical Complexity" por "Channel & Market Complexity" |

### ¿Falta alguna sección para Marketing?

**Sección potencial para Marketing: "Stack de Herramientas" (Martech Stack)**

En cargos de marketing digital, la familiaridad con herramientas específicas (CRM, automation, analytics, ad platforms) es relevante como discriminador, similar al stack tecnológico en Engineering. Esta información actualmente puede ir en la sección 7 (Competencias Técnicas), pero en Marketing suele ser más una lista de herramientas que una tabla de competencias con niveles.

**Recomendación:** No crear una sección separada. Adaptar la sección 7 para que en Marketing liste herramientas del martech stack con nivel de uso esperado. El template base es suficientemente flexible para esto.

### Conclusión sobre Universalidad del Template

El template de 9 secciones **es universal**. No requiere variantes por área funcional, pero requiere **parámetros contextuales** dentro de cada sección:

- Los KPIs cambian según el dominio (MQLs en Marketing, Cycle Time en Engineering)
- Las competencias técnicas cambian (herramientas de martech vs stack de software)
- La dimensión de seniority "Technical Complexity" necesita ser renombrada según el área (ver sección 3 de este documento)

---

## 7. Función vs Responsabilidad en el Contexto de Marketing

### La Distinción Aplicada

La distinción función/responsabilidad es igualmente válida en Marketing, pero la manera de aplicarla es diferente:

**Función:** Dominio de acción con un output definible a nivel de área. Responde "¿en qué área actúa el cargo?".
**Responsabilidad:** Obligación específica de resultado. Responde "¿qué debe garantizar el cargo?".

### Ejemplos Aplicados

| Función | Responsabilidades dentro de la función |
|---------|---------------------------------------|
| **Gestión de Demanda** | Alcanzar el objetivo trimestral de MQLs; Mantener el costo por MQL dentro del target definido; Entregar informe semanal de pipeline a la dirección |
| **Marketing Digital** | Garantizar posicionamiento orgánico en keywords prioritarias; Gestionar presupuesto de paid acquisition con ROAS positivo; Producir calendario de contenidos con cadencia semanal |
| **Gestión de Marca** | Asegurar coherencia visual y narrativa en todos los materiales; Gestionar relación con agencias de diseño/comunicación; Actualizar brand guidelines con cada lanzamiento de producto |
| **Participación en Eventos** | Seleccionar y gestionar participación en 2-3 eventos anuales estratégicos; Generar pipeline atribuible a cada evento; Representar la marca con presencia activa en comunidades del sector |

### Regla Práctica para Redactar en Marketing

- **Función** → sustantivo que nombra el dominio: "Gestión de Demanda", "Marketing de Contenidos", "Gestión de Marca"
- **Responsabilidad** → verbo de resultado + objeto + criterio de éxito: "Alcanzar 50 MQLs por trimestre con costo por MQL < $200"

La diferencia respecto a Engineering no es conceptual sino de naturaleza del output: en Engineering el output suele ser un artefacto (código, arquitectura, documentación); en Marketing el output suele ser un resultado de negocio o un activo de comunicación.

---

## Fuentes y Referencias

- **Demand Gen / B2B Marketing frameworks:** HubSpot Marketing benchmarks, Forrester SiriusDecisions waterfall model (MQL→SQL conversion), Terminus ABM framework
- **Titulación y niveles en Marketing tech:** Radford Global Technology Survey, LinkedIn Jobs data para títulos de marketing en SaaS/tech (2023-2025), Levels.fyi expansión a funciones no-engineering
- **KPIs de Marketing:** Gartner Marketing benchmarks 2024, HubSpot State of Marketing Report 2024, Lenny's Newsletter (benchmarks SaaS growth)
- **Job Architecture en funciones no técnicas:** Mercer Job Evaluation methodology, World at Work job leveling guides
- **Marketing role design en startups:** "Founding Marketer" archetype (Lenny's Newsletter), "T-shaped marketer" model (Buffer), "Growth Lead" role definition (a16z portfolio companies)

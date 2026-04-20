# Research: Framework para Descriptores de Cargo Formales en Tech Startups

**Fecha:** 2026-04-20
**Fuente:** Síntesis de frameworks SHRM, Mercer/Radford, HRCI, competency frameworks modernos, y mejores prácticas para tech startups AI-first.

---

## 1. Estructura Canónica de un Descriptor de Cargo Formal

Un descriptor de cargo formal ("job description" o JD) tiene entre 7 y 10 secciones según el marco de referencia. Las secciones consideradas **obligatorias** por SHRM (Society for Human Resource Management) y la mayoría de los competency frameworks modernos son:

### Secciones Obligatorias

| # | Sección | Contenido |
|---|---------|-----------|
| 1 | **Identificación del Cargo** | Título del cargo, área/departamento, nivel de seniority, modalidad (presencial/remoto/híbrido), fecha de última actualización |
| 2 | **Propósito / Misión del Cargo** | Párrafo de 2-3 oraciones que responde: ¿por qué existe este cargo? ¿qué valor produce para la organización? |
| 3 | **Posición en la Estructura** | A quién reporta (línea directa), quiénes reportan a este cargo (si aplica), relaciones laterales clave |
| 4 | **Funciones / Responsabilidades Principales** | Lista de 5-8 responsabilidades nucleares. Idealmente agrupadas por dominio. Verbos de acción en infinitivo o tercera persona. |
| 5 | **Roles Ejercidos** | Qué roles operativos ejerce el ocupante (puede ser uno o varios). Este campo diferencia el cargo del rol. |
| 6 | **Requisitos del Cargo (Excluyentes)** | Hard skills, soft skills, experiencia mínima, educación mínima. Todo excluyente = knock-out en selección. |
| 7 | **Competencias Requeridas** | Competencias conductuales y técnicas. Puede ser un perfil por niveles (básico/avanzado/experto). |
| 8 | **Indicadores de Desempeño** | KPIs o métricas que el cargo es accountable de mover. Conecta cargo con resultados medibles. |
| 9 | **Requisitos Deseables** | Habilidades o experiencias nice-to-have, no knock-out. |
| 10 | **Condiciones del Cargo** | Rango salarial (opcional), tipo de contrato, ubicación, beneficios especiales si aplica. |

### Secciones Opcionales (para contexto)

- **Contexto organizacional:** descripción de la empresa/equipo (útil en JDs públicos para atraer talento)
- **Stack tecnológico:** tecnologías específicas requeridas (común en tech)
- **Cultura y valores:** cómo se espera que el ocupante encarne la cultura

### Nota sobre startups pequeñas

Para empresas con <20 personas, se puede comprimir a 6 secciones mínimas:

1. Identificación + modalidad
2. Misión del cargo
3. Funciones principales (5-7)
4. Requisitos excluyentes
5. Competencias clave
6. KPIs del cargo

---

## 2. Distinción Conceptual: Cargo vs Posición vs Rol vs Función vs Responsabilidad

Esta es una de las confusiones más frecuentes en RRHH moderno. La taxonomía varía por tradición (anglosajona vs latina), pero la distinción más útil operativamente es la siguiente:

### Jerarquía Conceptual (de más abstracto a más concreto)

```
CARGO / POSICIÓN
    └── ejerce uno o más ROLES
            └── cada rol agrupa FUNCIONES
                    └── cada función implica RESPONSABILIDADES
```

### Definiciones

| Término | Definición | Ejemplo |
|---------|-----------|---------|
| **Cargo / Posición** ("Job" / "Position") | La unidad organizacional formal. Es el "slot" en el organigrama. Tiene un nombre, un nivel, y un ocupante humano específico. Aparece en el contrato laboral. | "Lead Dev AI" en CognitionBase |
| **Rol** ("Role") | Un conjunto de comportamientos y expectativas que una persona asume en un contexto operativo específico. Un cargo puede ejercer múltiples roles. Un rol puede ser ejercido por diferentes cargos. | "SDM (Service Delivery Manager)" — rol operativo ejercido por el Lead Dev AI |
| **Función** ("Function" / "Duty") | Una agrupación de actividades relacionadas que contribuyen a un resultado definido. Es un dominio de acción dentro de un rol. | "Arquitectura de Producto (Blueprinting)" — función dentro del cargo Lead Dev AI |
| **Responsabilidad** ("Responsibility") | Una obligación específica de resultado o conducta. Nivel más granular. Es lo que el ocupante debe hacer o garantizar. | "Recibir ideas de producto y transformarlas en Blueprints técnicos que incluyan el esquema de datos" |
| **Tarea** ("Task") | La unidad más atómica de trabajo. Deriva de una responsabilidad. Típicamente no aparece en descriptores de cargo (va en manuales operativos o procedimientos). | "Crear diagrama ER para cada nuevo producto" |

### Reglas de Distinción Clave

1. **Cargo ≠ Rol:** Un cargo es una posición formal con un ocupante. Un rol es un patrón de comportamiento operativo. Puedes cambiar quién ejerce un rol sin cambiar el cargo.

2. **Función ≠ Responsabilidad:** Una función agrupa; una responsabilidad especifica. "Liderazgo de equipo" es una función; "garantizar que los Devs AI tengan 1:1 semanal" es una responsabilidad dentro de esa función.

3. **Posición vs Cargo:** En la tradición anglosajona, "position" es el slot individual (puede haber 3 posiciones del mismo cargo) y "job" es el cargo como categoría. En español, "cargo" cubre ambos. En contextos formales chilenos, se usa "cargo" para referirse a la posición individual.

4. **La diferencia operativa que importa:** El descriptor de cargo define **funciones y responsabilidades**. Los **roles** son una capa de mapeo operativo que puede documentarse por separado (role cards, RACI, etc.).

---

## 3. Modelado de un Cargo con Múltiples Roles Simultáneos

Este es el caso del Lead Dev AI de CognitionBase: el cargo ejerce tanto el rol técnico (Lead Dev AI) como el rol de gestión de entrega (SDM).

### Patrones Existentes en la Literatura

#### Patrón A: Role Stack (Apilamiento de Roles)

El cargo tiene un rol primario y uno o más roles secundarios. Se documenta explícitamente en el descriptor.

```
Cargo: Lead Dev AI
  Rol Primario: Technical Lead
  Rol Secundario: SDM (Service Delivery Manager)
```

Este patrón es común en startups y scale-ups donde la estructura es lean. Es el modelo de GitHub (donde el "Staff Engineer" puede ejercer como tech lead Y como project lead en distintos contextos).

#### Patrón B: Hybrid Role Definition

El descriptor de cargo integra las funciones de ambos roles en una sola estructura, sin separar explícitamente por rol. Las funciones se agrupan por dominio, no por rol.

Ventaja: más simple de leer. Desventaja: oscurece la naturaleza dual del cargo, dificultando futuras separaciones cuando el equipo crece.

#### Patrón C: Role-Responsibility Matrix (extensión del RACI)

Un documento separado (Role Card o RACI) mapea qué roles existen en el equipo y qué cargo los ejerce actualmente. El descriptor de cargo lista las funciones; el RACI muestra el mapa de roles.

```
| Rol         | Ejercido Por            | % del tiempo estimado |
|-------------|-------------------------|-----------------------|
| Tech Lead   | Lead Dev AI             | 60%                   |
| SDM         | Lead Dev AI             | 40%                   |
```

### Recomendación para CognitionBase

**Usar Patrón A + elemento del Patrón C:**

En el descriptor de cargo, incluir una sección explícita "Roles Ejercidos" que liste los roles con breve descripción. Opcionalmente, incluir un RACI liviano en un documento separado del equipo. Esto permite:

- Claridad para el candidato/ocupante sobre la naturaleza dual del cargo
- Capacidad de separar los roles cuando el equipo crezca (crear un SDM separado)
- Trazabilidad de decisiones organizacionales

**Template para sección "Roles Ejercidos":**

```
## Roles Ejercidos

Este cargo ejerce dos roles operativos dentro de CognitionBase:

**Rol Primario — Technical Lead (AI-First):**
[descripción breve del rol técnico]

**Rol Secundario — SDM (Service Delivery Manager):**
[descripción breve del rol de entrega]

Nota: Esta dualidad es característica de la fase actual de CognitionBase.
A medida que el equipo escale, el rol SDM podrá separarse en una posición independiente.
```

---

## 4. Niveles de Experiencia (Seniority Tracks) Dentro de un Cargo

### Modelos Existentes

#### Modelo A: Cargo Único con Track de Seniority (más común en startups)

Un solo descriptor de cargo con una sección "Niveles" que define las variaciones por seniority. Usado por Stripe, Linear, Notion en sus primeras etapas.

```
Cargo: Dev AI
  Nivel Junior: < 2 años exp, bajo supervisión, foco en tareas definidas
  Nivel Mid:    2-4 años exp, autonomía en tareas, comienza a diseñar soluciones
  Nivel Senior: > 4 años exp, autonomía total, define arquitectura, mentoriza
```

**Ventaja:** Una sola plantilla para mantener, fácil de escalar. Cada nivel tiene sus propios requisitos y compensación, pero comparten la misma estructura de funciones.

#### Modelo B: Descriptores Separados por Nivel (más formal, corporativo)

Cada nivel tiene su propio descriptor completo. Común en empresas grandes con job architecture formal (Mercer, Radford).

Ejemplo de nomenclatura: "Dev AI I", "Dev AI II", "Dev AI III" o "Junior Dev AI", "Dev AI", "Senior Dev AI".

**Desventaja para startups:** overhead de mantenimiento. Si cambias las funciones del cargo, debes actualizar 3 documentos.

#### Modelo C: Career Ladder Separado

El descriptor de cargo define el cargo en su forma canónica (usualmente la versión "Senior" o "Mid"). Un documento separado (Career Ladder) define las diferencias entre niveles.

Usado por: Dropbox, Buffer, CircleCI (quien publicó su career ladder).

### Dimensiones que Definen un Nivel

Los frameworks más maduros (Radford, Mercer, Levels.fyi) usan estas dimensiones para separar niveles:

| Dimensión | Junior | Mid | Senior |
|-----------|--------|-----|--------|
| **Scope of Work** | Tareas asignadas | Proyectos con ambigüedad moderada | Sistemas / iniciativas estratégicas |
| **Autonomy** | Supervisado | Semi-autónomo | Autónomo, define su propio trabajo |
| **Impact** | Individual | Equipo pequeño | Organización o producto |
| **Technical Complexity** | Conocido, bien definido | Moderado, requiere análisis | Ambiguo, requiere diseño desde cero |
| **Mentorship** | Recibe mentoring | Puede dar mentoring puntual | Mentoring sistemático como parte del rol |
| **Communication** | Interna al equipo | Cross-team | Stakeholders externos, C-level |

### Recomendación para CognitionBase

Dado el tamaño actual, usar **Modelo A** (cargo único con track de seniority) para el cargo "Dev AI". Para el cargo "Lead Dev AI", es un cargo Senior por definición (no tiene variantes de nivel en esta etapa). Si en el futuro se necesitan variantes (ej: "Principal Dev AI"), se puede añadir al descriptor existente.

---

## 5. Terminología: "Job Position" vs "Role" vs "Cargo"

### Mapa de Términos por Contexto

| Término | Idioma | Contexto de Uso | Connotación |
|---------|--------|-----------------|-------------|
| **Cargo** | Español | Documentos legales/contractuales, descriptor formal, organigrama | Formal, legal. Es el término que aparece en el contrato laboral en Chile. |
| **Posición** | Español | Organigrama, comunicación interna informal | Más informal que "cargo". A veces equivalente, a veces indica el slot específico. |
| **Rol** | Español | Operativa, comunicación de equipo, RACI | Operativo, no legal. Describe lo que la persona hace en la práctica. |
| **Job** | Inglés | Compensación, job architecture, benchmarking | Neutro, abarca el cargo como categoría. "Job family", "job level". |
| **Position** | Inglés | Organigrama, headcount, selección | El slot individual. "We have 3 open positions for the job of Dev AI." |
| **Role** | Inglés | Operativa, RACI, dailies, comunicación ágil | Igual que en español: comportamiento operativo, no posición formal. |
| **Title** | Inglés | LinkedIn, firma de email, marca personal | Título de presentación. Puede diferir del cargo formal. |

### Recomendación de Nomenclatura para CognitionBase

1. **En documentos formales** (descriptores, contratos): usar **"Cargo"** en español o **"Job Position"** en inglés.
2. **En comunicación operativa** (Notion, Slack, dailies): usar **"Rol"** o **"Role"**.
3. **En el organigrama y headcount**: usar **"Posición"** o **"Position"**.
4. **En el perfil de LinkedIn y firma**: usar el título tal como se quiera proyectar externamente (puede ser más marketeable que el cargo formal, ej: "AI Engineering Lead" vs "Lead Dev AI").

**Convención propuesta para CognitionBase:**

```
Cargo Formal (contrato/descriptor): Lead Dev AI
Rol(es) Ejercido(s): Technical Lead, SDM
Título Externo (LinkedIn): AI Engineering Lead @ CognitionBase
```

---

## 6. Frameworks Modernos Aplicables a Startups AI-First Pequeñas

### 6.1 Job Architecture (Radford / Mercer / Willis Towers Watson)

**Qué es:** Un sistema de clasificación de cargos que los organiza en familias, subfamilias, niveles y bandas de compensación. Es la base del benchmarking salarial.

**Radford** (Aon): el más usado en tech startups globales. Usa niveles P1-P6 para individual contributors y M1-M4 para managers.

**Mercer**: más usado en empresas medianas y grandes. Similar estructura.

**¿Aplica en startups pequeñas (<20 personas)?** Parcialmente. La job architecture completa es overhead innecesario. Pero es útil:

- Tomar prestada la **nomenclatura de niveles** (P1/P2/P3 o L1/L2/L3) para comunicación interna.
- Usar las **descripciones genéricas de nivel** como referencia para calibrar lo que "Senior" significa en el mercado.
- Referencia para **benchmarking salarial** cuando sea necesario escalar.

**Recomendación:** No implementar job architecture formal ahora. Adoptarla como referencia conceptual cuando el equipo supere 15-20 personas o cuando se necesite benchmarking externo serio.

### 6.2 RACI (Responsible, Accountable, Consulted, Informed)

**Qué es:** Una matriz de asignación de responsabilidades por proceso/decisión. No define cargos; define quién hace qué en cada proceso.

**¿Aplica?** Sí, pero con matices:

- Muy útil para clarificar los **roles operativos** en equipos pequeños donde un cargo ejerce múltiples roles.
- En CognitionBase específicamente, es útil para documentar el flujo SRM → SDM → Dev AI → entrega.
- No reemplaza el descriptor de cargo; lo complementa.

**RACI simplificado para startups:** Usar solo R (Responsible) y A (Accountable) en una tabla liviana. C e I agregan overhead.

### 6.3 Competency Frameworks

**Qué es:** Un catálogo de competencias (técnicas y conductuales) con definición de niveles de dominio (1-5 o básico/avanzado/experto). Frameworks conocidos: SFIA (Skills Framework for the Information Age), DORA competencies, OECD competency framework.

**SFIA** es especialmente relevante para roles de software/AI: tiene categorías específicas para desarrollo de software, IA, data, y gestión técnica.

**¿Aplica en startups pequeñas?** Con adaptación:

- Adoptar SFIA como **referencia de lenguaje** para describir competencias técnicas (evita inventar ruedas).
- No implementar SFIA completo (demasiado pesado). Tomar las competencias relevantes y adaptarlas.
- Para startups AI-first, añadir competencias específicas de IA que SFIA está comenzando a incorporar (prompt engineering, AI system design, MLOps).

### 6.4 OKR-Linked Job Descriptions

**Qué es:** Tendencia moderna (popularizada por empresas como Spotify y Basecamp) de ligar las responsabilidades del cargo a los OKRs o métricas del equipo. El descriptor de cargo no solo describe funciones sino que establece qué métricas moverá el ocupante.

**¿Aplica?** Muy sí para CognitionBase: la cultura Output-First hace que este enfoque sea natural. Incluir una sección "Indicadores del Cargo" que liste los KPIs que el ocupante impacta directamente (Cycle Time, Lead Time, etc.).

### 6.5 Role Cards (alternativa ligera a JDs completos)

**Qué es:** Un formato corto (1 página) que describe un rol operativo específico: propósito, outputs esperados, interacciones clave, métricas. Usado por empresas ágiles que quieren menos burocracia.

**¿Aplica?** Útil para los **roles** (SDM, SRM) como documentos complementarios al descriptor de cargo. No reemplaza el JD formal, pero documenta el comportamiento esperado en el contexto operativo.

---

## 7. Enfoque Pragmático para Empresas AI-First Pequeñas

### El Problema del "Goldilocks"

Las startups pequeñas enfrentan una tensión entre:

- **Demasiado formal:** Job descriptions de 10 secciones con competency matrices que nadie lee y son un pain de mantener.
- **Demasiado informal:** Sin estructura, lo que genera ambigüedad sobre expectativas, dificulta el onboarding y complica el crecimiento.

La zona correcta para CognitionBase (5-15 personas, cultura AI-First):

### Framework "Lean JD" para AI-First Startups

**Principio 1: Un descriptor por cargo, no por persona.**
El cargo define el rol, no quién lo ocupa. Cuando cambia el ocupante, el descriptor debería necesitar ajustes mínimos.

**Principio 2: Output-First en el descriptor.**
Las funciones deben estar redactadas en términos de outputs esperados, no de actividades. No "revisar código" sino "garantizar que cada entrega cumpla los DoDs definidos".

**Principio 3: Roles explícitos, no implícitos.**
Si un cargo ejerce dos roles, documentarlo. La ambigüedad de rol es la principal fuente de conflicto en startups pequeñas de alto rendimiento.

**Principio 4: KPIs en el descriptor.**
Incluir 3-5 métricas que el cargo mueve. Conecta el cargo con la cultura data-driven.

**Principio 5: Living document.**
El descriptor se revisa con cada cambio significativo en las responsabilidades (no anualmente de forma burocrática). El campo "fecha de última actualización" es importante.

**Principio 6: Seniority como track, no como descriptor separado.**
Para equipos pequeños, mantener un solo descriptor por tipo de cargo con una sección de niveles. Reduce overhead.

**Principio 7: Separar el cargo del título externo.**
El cargo formal (Lead Dev AI) puede diferir del título de LinkedIn (AI Engineering Lead). Documentar ambos.

### Stack Documental Recomendado para CognitionBase

```
Nivel 1 — Descriptor de Cargo (por cargo formal):
  - Lead Dev AI.md
  - Dev AI.md  (con track Junior/Mid/Senior)
  - SRM.md
  
Nivel 2 — Role Cards (por rol operativo):
  - role-sdm.md  (Service Delivery Manager)
  - role-srm.md  (Service Request Manager)
  - role-tech-lead.md

Nivel 3 — RACI liviano (por proceso clave):
  - raci-idea2market.md
  - raci-tech-evaluation.md
```

Este stack cubre formalidad necesaria sin burocracia excesiva. El nivel 2 y 3 son opcionales en etapa temprana pero muy recomendables cuando el equipo supere 5-6 personas.

---

## 8. Ejemplo de Template Completo (Lean JD)

### Template: Descriptor de Cargo — CognitionBase

```markdown
# Perfil de Posición: [Nombre del Cargo]

**Empresa:** CognitionBase (Spinoff de innovación de 23people.io)
**Nivel:** [Junior | Mid | Senior | Staff]
**Modalidad:** [Remoto | Híbrido | Presencial]
**Fecha de actualización:** YYYY-MM-DD

---

## 1. Propósito del Cargo
[2-3 oraciones: por qué existe este cargo, qué valor produce, qué problema resuelve para CognitionBase]

---

## 2. Posición en la Estructura
- **Reporta a:** [Cargo]
- **Es reportado por:** [Cargos que reportan a esta posición, o "N/A"]
- **Colabora directamente con:** [SRM, Lead Dev AI, etc.]

---

## 3. Roles Ejercidos
[Lista de roles operativos que ejerce este cargo]

**Rol Principal — [Nombre del Rol]:**
[Descripción del rol en 1-2 líneas]

**Rol Secundario — [Nombre del Rol]:** *(si aplica)*
[Descripción del rol en 1-2 líneas]

---

## 4. Funciones y Responsabilidades Principales
[5-8 funciones. Agrupar por dominio. Usar verbos de acción.]

* **[Nombre de la Función]:** [Descripción orientada a output]
* **[Nombre de la Función]:** [Descripción orientada a output]
...

---

## 5. Indicadores de Desempeño (KPIs del Cargo)
[3-5 métricas que el ocupante impacta directamente]

* **[KPI]:** [definición y target si aplica]
* **[KPI]:** ...

---

## 6. Requisitos del Cargo (Excluyentes)
[Hard y soft skills obligatorios. Cada ítem aquí es un knock-out en selección.]

* **[Competencia]:** [descripción del nivel requerido]
...

---

## 7. Competencias Técnicas Clave
[Skills técnicos específicos, con nivel esperado]

| Competencia | Nivel Esperado |
|-------------|----------------|
| [Skill]     | [Básico/Avanzado/Experto] |

---

## 8. Requisitos Deseables
[Nice-to-have, no knock-out]

* [Deseable 1]
* [Deseable 2]

---

## 9. Niveles del Cargo *(completar si el cargo tiene track de seniority)*

| Dimensión | Junior | Mid | Senior |
|-----------|--------|-----|--------|
| Scope | ... | ... | ... |
| Autonomy | ... | ... | ... |
| Impact | ... | ... | ... |
| Mentorship | ... | ... | ... |
```

---

## 9. Candidatos para Notas Zettelkasten

Los siguientes conceptos son suficientemente atómicos y permanentes para convertirse en notas permanentes:

1. **Distinción Cargo / Rol / Función / Responsabilidad** — taxonomía jerárquica fundamental para diseño organizacional
2. **Modelado de cargos con múltiples roles (Role Stack)** — patrón estructural en organizaciones lean
3. **Job Architecture en startups** — cuándo y cómo adoptar Radford/Mercer parcialmente
4. **Output-First en descriptores de cargo** — principio de redacción que conecta cargo con resultado
5. **Career Ladder vs Seniority Track embebido** — decisión de diseño documental para equipos pequeños
6. **SFIA como referencia para competencias técnicas** — framework agnóstico de empresa para naming de skills
7. **Role Cards como complemento al JD formal** — formato liviano para documentar comportamiento operativo
8. **Separación entre cargo formal y título externo** — distinción necesaria en startups con marca personal fuerte

---

*Fin del documento de research.*

# STATE: Job Descriptor Framework — CognitionBase

**Última actualización:** 2026-04-20
**Estado:** Investigación completada

---

## Decisiones Tomadas

| # | Decisión | Rationale |
|---|----------|-----------|
| 1 | Usar **Role Stack** (patrón A) para Lead Dev AI | Hace explícita la dualidad Technical Lead + SDM, permite separar roles futuros sin reescribir el cargo |
| 2 | Usar **cargo único con seniority track embebido** para Dev AI | Reduce overhead de mantenimiento en etapa temprana |
| 3 | **No implementar** Radford/Mercer job architecture completa | Demasiado overhead para equipo <20 personas; solo como referencia conceptual |
| 4 | Adoptar **SFIA** como vocabulario de referencia para competencias | Evita inventar términos; agnóstico de empresa; tiene cobertura para roles AI |
| 5 | Incluir sección de **KPIs** en todos los descriptores | Coherente con cultura Output-First y Data-driven de CognitionBase |
| 6 | **"Cargo"** para documentos formales/legales; **"Rol"** para operativa diaria | Distinción clara que evita confusión entre posición formal y comportamiento operativo |
| 7 | Separar **título externo** (LinkedIn) del cargo formal | Permite marca personal más marketeable sin comprometer formalidad interna |

---

## Open Questions

| # | Pregunta | Impacto |
|---|----------|---------|
| 1 | ¿Cuál es el cargo formal del SRM? ¿Tiene funciones adicionales más allá del rol SRM? | Necesario para crear el descriptor SRM.md |
| 2 | ¿El CEO/fundador tiene un cargo formal documentado? | Define si se necesita un descriptor para esa posición |
| 3 | ¿Se incluyen rangos salariales en los descriptores? | Decisión de política, impacta si los JDs son documentos públicos o internos |
| 4 | ¿Cuál es el criterio para separar el rol SDM en posición independiente? | Ayuda a documentar el trigger point en el descriptor Lead Dev AI |

---

## Artifacts Creados

| Archivo | Descripción |
|---------|-------------|
| `.planning/PROJECT.md` | Scope y criterios de éxito de esta investigación |
| `.planning/RESEARCH.md` | Síntesis completa: framework, template, patrones, nomenclatura, ejemplos aplicados |
| `.planning/research/01-job-descriptor-framework.md` | Research notes detalladas con todos los frameworks y fuentes (foco Engineering/AI) |
| `.planning/research/02-marketing-lead-validation.md` | Validación de universalidad del framework — caso Líder de Marketing |

---

## Decisiones Adicionales (Validación de Universalidad — 2026-04-20)

| # | Decisión | Rationale |
|---|----------|-----------|
| 8 | El framework **es universal** — no requiere variantes por área funcional | Validado contra el caso de Líder de Marketing: jerarquía, Role Stack, template de 9 secciones y 5 de 6 dimensiones de seniority aplican sin cambios estructurales |
| 9 | Renombrar "Technical Complexity" como **"Domain Complexity"** en el template base | Es la única dimensión de seniority no universal; cada área funcional especifica su variante (Engineering: Technical Complexity; Marketing: Channel & Market Complexity) |
| 10 | El **Role Stack** aplica y es más relevante aún para cargos de Marketing | Un Líder de Marketing en startup típicamente ejerce 4 roles simultáneos vs. 2 en cargos técnicos; documentarlo es aún más crítico |
| 11 | KPIs de cargos de Marketing son **métricas de negocio directas** (MQLs, pipeline, CAC), no de actividad | Refuerza el principio Output-First del framework; la sección KPIs es más crítica en Marketing que en Engineering |

---

## Open Questions Adicionales

| # | Pregunta | Impacto |
|---|----------|---------|
| 5 | ¿Cuántos roles simultáneos puede ejercer un cargo antes de que el Role Stack se vuelva inmanejable? | Define cuándo el Role Stack debe forzar la separación de posiciones; relevante para cargos con >4 roles |
| 6 | ¿Debe el template distinguir entre "Funciones" y "Responsabilidades" como secciones separadas, o mantenerlas integradas? | En Marketing la distinción es más importante que en Engineering por la mayor interdependencia de funciones |

---

## Decisiones Adicionales (Market Research + JD Enriquecido — 2026-04-20)

| # | Decisión | Rationale |
|---|----------|-----------|
| 12 | **Incluir salary range** en el descriptor publicable de Lead Dev AI | Best practice confirmada: candidatos senior no aplican sin rango; CLP $5M–$8M/mes es el benchmark Chile para el perfil |
| 13 | **Especificar stack técnico concreto** en la sección de competencias | Candidatos senior quieren saber exactamente con qué trabajan; stack recomendado: Next.js, Supabase, LangGraph, CrewAI, Claude SDK, MCP |
| 14 | **Incluir proceso de selección** en el JD publicable | Reduce ansiedad del candidato; las 5 etapas y ~2-3 semanas están documentadas |
| 15 | **Incluir sección "Éxito en los primeros 90 días"** | Diferenciador probado para alta conversión; estructura 30/60/90 aplicada al contexto CognitionBase |
| 16 | **Incluir path de crecimiento** | Candidatos senior evalúan el futuro; se documentan 3 trayectorias naturales desde el cargo |
| 17 | **MCP (Model Context Protocol) como requisito Intermedio** | Standard emergente adoptado por OpenAI, Cursor, VS Code; 97M+ SDK downloads; ya aparece en postings senior de 2025-2026 |

---

## Open Questions Actualizadas

| # | Pregunta | Estado |
|---|----------|--------|
| 1 | ¿Cuál es el cargo formal del SRM? ¿Tiene funciones adicionales más allá del rol SRM? | Pendiente — necesario para `SRM.md` |
| 2 | ¿El CEO/fundador tiene un cargo formal documentado? | Pendiente |
| 3 | ¿Se confirma el rango salarial CLP $5M–$8M para el descriptor publicable? | Pendiente validación interna |
| 4 | ¿Cuál es el criterio para separar el rol SDM en posición independiente? | Pendiente |
| 5 | ¿Cuántos roles simultáneos puede ejercer un cargo antes de que el Role Stack se vuelva inmanejable? | Pendiente |
| 6 | ¿Debe el template distinguir "Funciones" y "Responsabilidades" como secciones separadas? | Pendiente |

---

## Próximos Pasos Sugeridos

1. **Completado** — Descriptor `LEAD-DEV-AI.md` revisado y enriquecido con 13 secciones (template completo aplicado)
2. Crear `DEV-AI.md` con seniority track (Junior/Mid/Senior)
3. Crear `SRM.md` (requiere responder Open Question #1)
4. Crear role cards complementarias para SDM y SRM (Nivel 2 del stack documental)
5. Crear RACI liviano para el proceso Idea2Market
6. Actualizar el template base para reflejar "Domain Complexity" en lugar de "Technical Complexity"

---
type: reference-note
source_type: article
source_name: "Radford/Mercer Job Architecture; SFIA v9; GetOnBrd Política de Seniorities"
source_url: https://www.getonbrd.com/help/politica-de-niveles-de-experiencia-seniorities
created_at: 2026-04-20 12:22:18
updated_at: 2026-04-20 12:22:18
aliases: [seniority-track, proficiencia-rol, dimensiones-ortogonales-cargo]
tags: [job-architecture, seniority, role-design, organizaciones, career-ladders]
---

En el diseño de cargos existen dos dimensiones de "nivel" que son **ortogonales entre sí** y se confunden con frecuencia:

| Dimensión | Dónde se define | Qué modela |
|---|---|---|
| **Seniority Track (Nivel del Cargo)** | Descriptor de Cargo, sección "Niveles" | *Cómo* trabaja la persona: autonomía, alcance, impacto, comunicación |
| **Proficiencia en Rol (Nivel A/B/C)** | Role Card del rol específico | *Qué tan profundo* sabe hacer algo dentro del dominio funcional del rol |

Son ortogonales: **un Senior puede tener Nivel A en un rol nuevo** si ese dominio es nuevo para él. **Un Junior puede tener Nivel B** en ese mismo rol si lleva años ejerciéndolo.

---

## Seniority Track — Las 6 Dimensiones

Basado en el modelo Radford/Mercer simplificado:

| Dimensión | Junior | Mid | Senior |
|---|---|---|---|
| **Scope of Work** | Tareas asignadas, bien definidas | Proyectos con ambigüedad moderada | Sistemas / iniciativas estratégicas |
| **Autonomy** | Supervisado | Semi-autónomo | Define su propio trabajo |
| **Impact** | Individual | Equipo pequeño | Organización / producto |
| **Domain Complexity** | Conocido, predecible | Moderado, requiere análisis | Ambiguo, requiere diseño desde cero |
| **Mentorship** | Recibe mentoring | Mentoring puntual | Mentoring sistemático como parte del rol |
| **Communication** | Interna al equipo | Cross-team | Stakeholders / C-level |

> "Domain Complexity" es la adaptación universal de "Technical Complexity". En Marketing sería "Channel & Market Complexity"; en Finanzas, "Regulatory & Financial Complexity". Las demás 5 dimensiones son universales sin modificación.

---

## Proficiencia en Rol — Escala A/B/C

Atributo del **rol**, no del cargo. Se define en la Role Card del rol. Aplica cuando el mismo rol puede ejercerse con capacidades funcionalmente distintas en profundidad.

| Nivel | Nombre | Descripción |
|---|---|---|
| **A** | Ejecutor | Aplica el proceso definido. Ejecuta con supervisión o guía. |
| **B** | Analista | Ejecuta y mide. Produce datos sobre el proceso y propone mejoras con sustento. |
| **C** | Arquitecto | Diseña, rediseña y transfiere. Define cómo debe funcionar el proceso para otros. |

Mapeable a SFIA niveles 3–5 si se adopta el framework completo.

En el Descriptor de Cargo, la sección "Roles Ejercidos" declara el nivel de proficiencia esperado:

```markdown
**Rol Principal — Gestionador de Flujos de Trabajo (Nivel B):**
Gestiona el flujo Kanban del equipo, mide Cycle Time/Lead Time y produce
reportes de rendimiento operativo periódicos.
```

---

## References

- Radford/Mercer Job Architecture — modelo de seniority con dimensiones de scope, autonomy e impact
- SFIA v9 — escala de 7 niveles de responsabilidad para competencias tecnológicas (referencia para mapeo A/B/C → niveles 3–5)
- GetOnBrd — Política de niveles de experiencia (seniorities) para el mercado tech Chile/LATAM: No Experience / Junior / Semi-Senior / Senior / Expert

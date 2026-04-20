---
type: reference-note
source_type: article
source_name: "Radford/Mercer Job Architecture; SHRM; SFIA v9; GetOnBrd"
source_url:
created_at: 2026-04-20 12:22:18
updated_at: 2026-04-20 12:22:18
aliases: [job-descriptor-framework, framework-jd, diseño-cargos-formal]
tags: [job-architecture, descriptores-de-cargo, organizaciones, role-design, startups, career-ladders]
---

Un **Descriptor de Cargo** (o Job Description) es el documento formal que captura la totalidad de un cargo en una organización: su propósito, su lugar en la estructura, los roles que ejerce, las funciones que agrupa, los resultados que se le exigen y los requisitos para ocuparlo.

Existen tres conceptos relacionados pero distintos que el framework debe modelar por separado:

| Concepto | Nota de referencia |
|---|---|
| La jerarquía de términos: Cargo → Rol → Función → Responsabilidad → Tarea | [[2026-04-20_taxonomia-cargo-jerarquia]] |
| Seniority del cargo vs. Proficiencia en el rol (dimensiones ortogonales) | [[2026-04-20_seniority-vs-proficiencia-rol]] |
| Cómo documentar cargos que ejercen múltiples roles (Role Stack / Role Cards) | [[2026-04-20_patron-role-stack]] |

---

## Template de Descriptor de Cargo (9 secciones)

Estructura recomendada para startups y organizaciones lean:

| # | Sección | Obligatoria | Notas |
|---|---|---|---|
| 1 | **Propósito del Cargo** | Sí | 2–3 oraciones: por qué existe, qué valor produce |
| 2 | **Posición en la Estructura** | Sí | Reporta a / Es reportado por / Colabora con |
| 3 | **Roles Ejercidos** | Sí | Patrón Role Stack si hay dualidad de roles |
| 4 | **Funciones y Responsabilidades** | Sí | 5–8 funciones, redactadas en output |
| 5 | **KPIs del Cargo** | Sí | 3–5 métricas que el cargo mueve directamente |
| 6 | **Requisitos Excluyentes** | Sí | Knock-outs de selección — cada ítem elimina candidatos |
| 7 | **Competencias Técnicas** | Recomendable | Tabla con nivel esperado (SFIA como referencia de naming) |
| 8 | **Requisitos Deseables** | Opcional | Nice-to-have, no knock-out |
| 9 | **Niveles del Cargo** | Opcional | Solo si hay seniority track (Junior / Mid / Senior) |

---

## Nomenclatura por contexto

| Contexto | Término | Ejemplo |
|---|---|---|
| Contrato laboral / documento legal | **Cargo** | "Cargo: Lead Dev AI" |
| Descriptor formal / JD | **Perfil de Posición** o **Descriptor de Cargo** | Encabezado del documento |
| Comunicación operativa diaria | **Rol** | "Tu rol como SDM esta semana..." |
| Organigrama / headcount | **Posición** | "Tenemos 2 posiciones abiertas de Dev AI" |
| LinkedIn / marca personal | **Title externo** | "AI Engineering Lead @ Empresa" |

---

## Stack documental recomendado

```
Nivel 1 — Descriptores de Cargo (por cargo formal)
  jobs/
    lead-dev-ai.md
    dev-ai.md
    srm.md

Nivel 2 — Role Cards (por rol operativo, reutilizables)
  roles/
    role-sdm.md         ← incluye tabla A/B/C si el rol tiene variación de profundidad
    role-srm.md
    role-tech-lead.md

Nivel 3 — RACI por proceso (cuando el equipo supera 5–6 personas)
  processes/
    raci-idea2market.md
    raci-tech-evaluation.md
```

---

## References

- Radford/Mercer Job Architecture — framework de referencia para niveles y job families
- SHRM (Society for Human Resource Management) — estándares de job design y job descriptions
- SFIA v9 (Skills Framework for the Information Age) — vocabulario de competencias técnicas
- GetOnBrd — Política de seniorities para el mercado tech Chile/LATAM

---
type: reference-note
source_type: article
source_name: "SHRM Job Design; GitHub / Stripe / Linear Engineering Career Ladders"
source_url:
created_at: 2026-04-20 12:22:18
updated_at: 2026-04-20 12:22:18
aliases: [role-stack, role-cards, cargos-multiples-roles]
tags: [job-architecture, role-design, startups, descriptores-de-cargo, organizaciones]
---

En organizaciones lean (especialmente startups), un mismo cargo suele ejercer más de un rol operativo simultáneamente. Existen tres patrones para documentar esto en el descriptor de cargo:

| Patrón | Descripción | Cuándo usar |
|---|---|---|
| **Role Stack** | Descriptor único con sección "Roles Ejercidos" que lista roles explícitamente | Recomendado: startups, cargos con dualidad técnica + gestión |
| **Hybrid Role** | Descriptor integra funciones de todos los roles sin separación explícita | No recomendado: oscurece la dualidad y dificulta separar roles en el futuro |
| **Role Cards + RACI** | Documentos separados por rol, complementan al descriptor | Como capa adicional en equipos de 8+ personas |

---

## Patrón Role Stack (recomendado)

Se agrega una sección "Roles Ejercidos" al descriptor. Cada rol se declara con nombre, descripción breve y nivel de proficiencia esperado (A/B/C, ver → [[2026-04-20_seniority-vs-proficiencia-rol]]):

```markdown
## Roles Ejercidos

**Rol Principal — Technical Lead (AI-First):**
Lidera la arquitectura técnica, la calidad de entregas y la mentalidad AI-First del equipo.

**Rol Secundario — SDM (Service Delivery Manager) (Nivel B):**
Gestiona el flujo de solicitudes validadas, asegurando que ingresen, se ejecuten
y se entreguen cumpliendo los SLAs y DoDs acordados.
```

> Esta dualidad es propia de fases tempranas. A medida que el equipo escale, los roles secundarios pueden separarse en posiciones independientes.

---

## Role Cards (patrón complementario)

Documentos independientes por rol, reutilizables: el mismo rol puede referenciarse desde múltiples descriptores de cargo. Estructura mínima:

- **Propósito del Rol**
- **Outputs Clave**
- **Interacciones** (quién entrega, quién recibe)
- **Niveles de Proficiencia A/B/C** — incluir cuando el rol tiene variación funcional en profundidad

La ventaja principal: permite asignar el mismo rol a distintos cargos con distintos niveles de proficiencia sin duplicar definiciones.

---

## Criterio para separar un rol en posición independiente

No existe una regla universal, pero las señales más comunes son:
- El volumen de trabajo del rol supera la capacidad de quien lo ejerce junto a su rol principal
- El equipo supera 5–8 personas y la coordinación requiere dedicación exclusiva
- El rol requiere competencias que no están presentes en el cargo actual

---

## References

- SHRM — Job Design Guidelines: principios de diseño de cargos y separación de roles
- GitHub Engineering Career Ladder — ejemplo de role clarity en cargos técnicos con múltiples responsabilidades
- Stripe Engineering Levels — modelo de career ladders con separación explícita de IC vs. management tracks
- Linear (Craft-driven Product Development) — ejemplo de documentación de roles en producto tech lean

---
type: reference-note
source_type: article
source_name: "Radford/Mercer Job Architecture; SHRM Job Design Guidelines; SFIA v9"
source_url:
created_at: 2026-04-20 12:22:18
updated_at: 2026-04-20 12:22:18
aliases: [jerarquía-jd, job-descriptor-taxonomy, taxonomía-cargo]
tags: [job-architecture, descriptores-de-cargo, organizaciones, role-design, startups]
---

En el diseño formal de cargos existe una jerarquía de cinco niveles que va desde la unidad organizacional más amplia hasta la acción más atómica:

```
CARGO
  └── ejerce uno o más ROLES
        └── cada rol agrupa FUNCIONES
              └── cada función implica RESPONSABILIDADES
                    └── cada responsabilidad descompone en TAREAS
```

## Definiciones operativas

| Término | Qué es | Ejemplo |
|---|---|---|
| **Cargo** | Unidad organizacional formal con un ocupante. Aparece en contrato y organigrama. | Lead Dev AI |
| **Rol** | Conjunto de comportamientos y expectativas en un contexto operativo. Puede reasignarse sin redefinir el cargo. | SDM (Service Delivery Manager) |
| **Función** | Agrupación de actividades relacionadas que producen un resultado definido. Dominio de acción dentro de un rol o cargo. | "Arquitectura de Producto (Blueprinting)" |
| **Responsabilidad** | Obligación específica de resultado o conducta. Es el nivel más granular que aparece en un descriptor de cargo (JD). | "Transformar ideas de producto en Blueprints técnicos con esquema de datos" |
| **Tarea** | Unidad atómica de trabajo. **No aparece en JDs** — va en manuales o procedimientos operativos. | "Crear diagrama ER para cada nuevo producto" |

## Reglas clave

- **Cargo ≠ Rol**: el cargo es permanente y formal; el rol es operativo y contextual. Se puede reasignar un rol a otro cargo sin tocar el contrato.
- **Función ≠ Responsabilidad**: la función agrupa dominios de acción; la responsabilidad especifica qué resultado concreto se debe lograr dentro de ese dominio.
- **Las tareas no van en descriptores de cargo**: son demasiado atómicas. Pertenecen a manuales de operación o SOPs. Incluirlas en un JD lo vuelve rígido e inmanejable.
- **Un cargo puede ejercer múltiples roles**: especialmente en startups o equipos lean. Ver nota → [[2026-04-20_patron-role-stack]].

---

## References

- Radford/Mercer Job Architecture Framework — nomenclatura estándar de niveles P1–P6 y diseño de job families
- SHRM (Society for Human Resource Management) — guías de job design y job descriptions
- SFIA v9 (Skills Framework for the Information Age) — framework de competencias para roles de tecnología e información

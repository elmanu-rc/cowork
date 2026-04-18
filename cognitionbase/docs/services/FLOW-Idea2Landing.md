# Flujo: Idea2Landing

> **Versión:** 0.1 (draft)
> **Fecha:** 2026-04-17
> **Origen:** Sesión de diseño con Manuel Reyes — ver `DISCOVERY-Idea2Landing-Flow.md` para el razonamiento completo.
> **Posición en el servicio:** Sub-flujo 1 de Idea2Market. Precede al gate de validación de tracción y al flujo Landing2MVP.

---

## 1. Propósito

Transformar una idea de negocio validada en un **landing page funcional con demo interactivo**, desplegado en producción, en 7–10 días hábiles. El objetivo no es el landing en sí — es validar si el mercado responde a la propuesta de valor *antes* de invertir en desarrollo complejo.

---

## 2. Input requerido: REQUEST.md

El flujo no puede iniciarse sin un `REQUEST.md` validado por el SRM. Este documento es el artefacto de entrada unificado y está compuesto por 4 bloques:

| Bloque | Contenido | Quién lo necesita |
|--------|-----------|-------------------|
| **Narrativa Estratégica** | Audiencia, problema en sus palabras, urgencia, solución, transformación, proof points, tono de voz | Copy skill / agente de copywriting |
| **Datos de Marketing Digital** | CTA principal (acción + texto del botón), fuente de tráfico, temperatura del público, secciones obligatorias, objeciones | Diseño y copy del landing |
| **Datos Operacionales** | URL destino, DNS, branding, analytics, integraciones, stack override | Build y deploy |
| **GSD Scope** | v1_must_have, v2_nice_to_have, out_of_scope, constraints, métrica de gate para Landing2MVP | Blueprint y REQUIREMENTS.md |

### Campos que bloquean el flujo (sin fallback posible)

Si alguno de estos está vacío, el SRM no puede aprobar el Intake:

- `url_destino` — sin URL no hay deploy
- `cta_principal_accion` — define la estructura entera del landing
- `aha_moment_hipotesis` — el Blueprint no puede diseñar el demo sin esto
- `metrica_objetivo` — sin esto el landing no tiene DoD real
- `v1_must_have` — contrato mínimo de entrega

### Campos con fallback declarado

El Blueprint resuelve estos si no están presentes:

- `branding` → generar desde narrativa
- `analytics_herramienta` → GA4
- `stack_override` → CB Standard (Next.js + Tailwind + Vercel)
- `idioma` → `es`
- `deadline_landing` → 7–10 días hábiles
- `flujo_demo` → Blueprint lo define a partir de `aha_moment_hipotesis`

---

## 3. El campo más importante: `aha_moment_hipotesis`

El "Aha! Moment" es el instante donde el visitante entiende visceralmente el valor del producto. Es la hipótesis central que orienta el diseño del demo y la estructura del Blueprint.

**Cómo escribirlo:** no como feature list, sino como escena narrativa.

> ❌ "El sistema trackea plazos automáticamente."
>
> ✅ "El visitante ve cómo una solicitud ARCO+ llega al sistema, queda registrada automáticamente con un countdown de 30 días y aparece en el tablero Kanban — sin que nadie tuviera que hacer nada manualmente."

Sin una escena concreta, el Blueprint genera un demo genérico que no convierte.

---

## 4. Etapas del flujo

```
[INPUT] REQUEST.md validado
    ↓
[1] Intake & Validación (SRM)
    ↓
[2] Blueprint (Lead Dev AI)
    ↓
[3] Copy & Marketing Design
    ↓
[4] UI/UX Design
    ↓
[5] Build: Landing + Demo
    ↓
[6] QA, SEO & Analytics
    ↓
[7] Deploy a Producción
    ↓
[OUTPUT] Landing live + Demo accesible + Analytics activo
```

### Etapa 1 — Intake & Validación

**Responsable:** SRM

El SRM verifica que el REQUEST.md esté completo antes de ingresar el proyecto al flujo técnico. Revisa que los campos bloqueantes estén presentes y que los fallbacks estén declarados cuando aplican.

**DoD:** checklist de inputs 100% completo (o fallbacks explícitamente declarados).

---

### Etapa 2 — Blueprint

**Responsable:** Lead Dev AI

Con el REQUEST.md aprobado, el Lead Dev AI genera el **Blueprint**: el plano maestro técnico del proyecto. Define la arquitectura del landing, el flujo del demo, la orquestación de agentes y la estrategia del Aha! Moment. También genera los artefactos GSD iniciales a partir del REQUEST.md.

| Artefacto GSD | Se alimenta de |
|---------------|----------------|
| `PROJECT.md` | Narrativa + Audiencia + Solución |
| `REQUIREMENTS.md` | Bloque GSD Scope (v1/v2/out-of-scope) |
| `ROADMAP.md` | Generado automáticamente desde REQUIREMENTS.md |
| `STATE.md` | Bloque Operacional (DNS, branding, stack, constraints) |

**DoD:** Blueprint aprobado por Lead Dev AI antes de tocar código.

---

### Etapa 3 — Copy & Marketing Design

**Responsable:** Agente de copywriting (Iron-Legion)

Genera el copy completo del landing a partir de la Narrativa Estratégica y los Datos de Marketing Digital del REQUEST.md. La temperatura del tráfico y la fuente principal condicionan el tono y estructura del hero. Las objeciones declaradas se trabajan en FAQ o secciones de garantía.

**DoD:** copy aprobado internamente antes de iniciar el diseño visual.

---

### Etapa 4 — UI/UX Design

**Responsable:** Agente de diseño (Iron-Legion)

Diseña el landing responsivo (mobile + desktop) usando el copy aprobado como base. Incluye el flujo del demo interactivo hasta el Aha! Moment.

**DoD:** diseño aprobado en mobile y desktop.

---

### Etapa 5 — Build: Landing + Demo

**Responsable:** Dev AI (Iron-Legion)

Implementa el landing y el demo sobre el stack estándar (Next.js + Tailwind + Vercel) o el stack declarado en `stack_override`. El demo debe ser accesible desde el CTA principal.

**DoD:** landing navegable en staging, demo funcional desde el CTA, sin errores críticos.

---

### Etapa 6 — QA, SEO & Analytics

**Responsable:** Dev AI + Lead Dev AI

Verifica que el landing cumpla los estándares mínimos de calidad antes del deploy.

Checklist:

- Lighthouse score aceptable (Performance, Accessibility, SEO)
- GA4 disparando eventos clave (page_view, cta_click, demo_start)
- Sin errores de consola en mobile y desktop
- SSL configurado
- Open Graph y meta tags para redes sociales

**DoD:** todos los puntos del checklist en verde.

---

### Etapa 7 — Deploy a Producción

**Responsable:** Dev AI + Lead Dev AI

Deploy a la URL destino declarada en el REQUEST.md. El cliente recibe acceso a la dashboard de analytics.

**DoD:** URL pública live, SSL activo, cliente con acceso confirmado a analytics.

---

## 5. Output del flujo

Al completar la etapa 7, el output es:

- **Landing page** funcional y responsiva en la URL destino
- **Demo interactivo** accesible desde el CTA principal
- **Analytics activo** (GA4 u herramienta declarada) con eventos configurados
- **Acceso del cliente** a la dashboard de métricas

---

## 6. Gate hacia Landing2MVP

La métrica del gate no es global — se define en el campo `metrica_objetivo` del REQUEST.md al inicio del proyecto, ya que depende del tipo de producto y mercado.

Ejemplos de métricas de gate:

- X leads capturados en N días
- Y% de visitantes completan el demo
- Z% tasa de conversión del CTA principal

**Quién decide:** está pendiente definir formalmente quién autoriza el paso al siguiente flujo (¿SRM, Lead Dev AI, cliente?). Ver preguntas abiertas.

---

## 7. Stack estándar CB

| Capa | Tecnología |
|------|-----------|
| Frontend | Next.js + Tailwind CSS |
| Deploy | Vercel |
| Analytics | GA4 |
| Branding | Generado desde narrativa (si no se provee) |

El cliente puede declarar `stack_override` en el REQUEST.md para reemplazar cualquier capa.

---

## 8. Artefactos del flujo

| Artefacto | Descripción |
|-----------|-------------|
| `REQUEST.md` | Input del flujo. Documento unificado con los 4 bloques requeridos. |
| `REQUEST-TEMPLATE.md` | Plantilla con instrucciones por campo y ejemplos. Ubicación: `docs/REQUEST-TEMPLATE.md`. |
| `Blueprint` | Plano técnico generado por Lead Dev AI en etapa 2. |
| Landing live | URL pública en producción. |

---

## 9. Preguntas abiertas

1. **¿Quién completa el REQUEST.md?** ¿El cliente, el SRM, o ambos en conjunto? Algunos campos técnicos (stack, integraciones) pueden requerir apoyo del SRM.

2. **¿El REQUEST.md reemplaza o complementa el documento de narrativa estratégica?** Hoy pueden coexistir (ej. PDF de narrativa + REQUEST.md). ¿Deberían unificarse formalmente?

3. **¿Cómo se versiona el REQUEST.md?** Si el cliente cambia URL o CTA a mitad del flujo, ¿qué pasa con el Blueprint ya aprobado?

4. **¿Cuáles son las fases GSD del flujo Idea2Landing?** Las etapas de este documento aún no están mapeadas formalmente a las fases GSD (discuss → plan → execute → verify).

5. **¿Quién autoriza el gate hacia Landing2MVP?** Debe quedar definido formalmente quién valida que la métrica se cumplió y habilita el siguiente flujo.

---

*Para el razonamiento detrás de cada decisión de diseño, ver `DISCOVERY-Idea2Landing-Flow.md`.*

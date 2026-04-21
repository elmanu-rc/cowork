# Descubrimientos: Diseño del Flujo Idea2Landing

> **Fecha:** 2026-04-17  
> **Participantes:** Manuel Reyes + Claude (CognitionBase Cowork)  
> **Contexto:** Sesión de diseño del flujo Idea2Landing como primera etapa del servicio Idea2Market de CognitionBase. Proyecto de referencia: ARCO Legal (PDF de narrativa estratégica).

---

## 1. Decisión Arquitectural: Idea2Market se divide en dos flujos

El flujo Idea2Market descrito en COGNITIONBASE.md es demasiado amplio para operar como un solo proceso. Se divide en dos sub-flujos secuenciales con un gate de validación entre ellos:

**Idea2Landing** → _(gate: métrica de tracción)_ → **Landing2MVP**

**Rationale:** El landing page sirve para validar si el mercado responde a la propuesta de valor *antes* de invertir en desarrollo complejo del producto. Si el landing no convierte, el problema puede estar en el mensaje, la audiencia o la solución — y es mucho más barato descubrirlo ahí que después de 6 semanas de MVP.

El gate entre flujos debe definirse en el REQUEST.md al inicio del proyecto (no es una métrica global fija), ya que depende del tipo de producto y del mercado.

---

## 2. Etapas del flujo Idea2Landing

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

**DoD por etapa:**
- **Intake:** checklist de inputs 100% completo (o fallbacks declarados)
- **Blueprint:** plano técnico aprobado por Lead Dev AI antes de tocar código
- **Copy:** copy aprobado internamente antes de diseñar
- **UI/UX:** diseño responsivo aprobado (mobile + desktop)
- **Build:** landing navegable en staging, demo funcional desde el CTA
- **QA:** Lighthouse aceptable, GA4 disparando eventos, sin errores en mobile
- **Deploy:** URL pública live, SSL activo, cliente con acceso a analytics

---

## 3. El gap del input actual: ARCO Legal como caso de estudio

El PDF "Proyecto - Arco Legal" es un ejemplo del tipo de documento que hoy llega como input al flujo. Cubre bien la narrativa estratégica pero le faltan tres capas completas:

| Capa | Cobertura en PDF | Necesidad real |
|------|-----------------|----------------|
| Narrativa estratégica | ✅ Completa | Audiencia, problema, solución, estrategia, métricas |
| Marketing digital | ⚠️ Parcial | CTA, fuente de tráfico, temperatura del público, tono de voz — ausentes |
| Operacional | ❌ Ausente | URL, DNS, branding, analytics, integraciones, deadline |
| GSD Scope | ❌ Ausente | V1/V2/out-of-scope, constraints, gate para Landing2MVP |

**Conclusión:** el documento de narrativa estratégica es condición necesaria pero no suficiente para iniciar el flujo. Se necesita un formulario de intake operacional complementario. El REQUEST.md unifica ambas cosas.

---

## 4. Estructura del REQUEST.md: 4 bloques con propósitos distintos

### Bloque 1 — Narrativa Estratégica
Lo que el copywriting skill necesita para generar copy. Fuente: el documento de idea.
Campos clave: audiencia, problema en sus palabras, urgencia, solución, transformación, proof points, tono de voz.

### Bloque 2 — Datos de Marketing Digital
Lo que determina el diseño y estructura del landing. Ausente en documentos de idea típicos.
Campos clave: CTA principal (acción + texto del botón), fuente de tráfico, temperatura del público, secciones obligatorias.

### Bloque 3 — Datos Operacionales
Lo que habilita el build y el deploy. Sin estos, el flujo no puede completar las etapas 6 y 7.
Campos clave: URL de destino, DNS, branding (o "generar"), analytics, integraciones, stack override.

### Bloque 4 — GSD Scope
Lo que permite generar REQUIREMENTS.md sin preguntas adicionales. Nuevo respecto a documentos previos.
Campos clave: v1_must_have, v2_nice_to_have, out_of_scope, constraints, gate para Landing2MVP.

---

## 5. Integración con GSD: cómo REQUEST.md mapea a artefactos GSD

Cuando se ejecuta `/gsd-new-project` con el REQUEST.md como contexto, el sistema puede generar directamente:

| Artefacto GSD | Se alimenta de |
|---------------|---------------|
| `PROJECT.md` | Secciones 1 (Proyecto) + 3 (Solución) + 2 (Audiencia) |
| `REQUIREMENTS.md` | Sección 8 (Scope GSD) — v1/v2/out-of-scope con trazabilidad de fases |
| `ROADMAP.md` | GSD lo genera automáticamente a partir de REQUIREMENTS.md |
| `STATE.md` | Sección 6 (Despliegue) — dns_listo, branding status, stack decisions, constraints |
| `.planning/research/` | GSD lanza agentes de investigación paralelos usando la narrativa como base |

**El objetivo del REQUEST.md respecto a GSD:** eliminar la fase de preguntas de `/gsd-new-project` (o reducirla al mínimo), alimentando el contexto que GSD necesita para planificar directamente.

---

## 6. Campos críticos vs. campos con fallback

Una distinción fundamental para el diseño del Intake:

**Campos que bloquean el flujo si están vacíos** (sin fallback posible):
- `url_destino` — no se puede deployar a ningún lado
- `cta_principal_accion` — define el diseño entero del landing
- `aha_moment_hipotesis` — el Blueprint no puede diseñar el demo sin esto
- `metrica_objetivo` — sin esto el landing no tiene DoD real (¿cuándo terminamos?)
- `v1_must_have` — contrato de entrega mínimo

**Campos con fallback declarado** (el Blueprint los resuelve si faltan):
- `branding` → generar desde narrativa
- `analytics_herramienta` → GA4
- `stack_override` → CB Standard (Next.js + Tailwind + Vercel)
- `idioma` → `es`
- `deadline_landing` → 7–10 días hábiles
- `flujo_demo` → Blueprint lo define a partir de `aha_moment_hipotesis`

---

## 7. Insights del copywriting skill aplicados al REQUEST.md

La consulta al skill `coreyhaines31-marketingskills:copywriting` identificó campos que los documentos de idea típicos nunca incluyen pero que son determinantes para el copy del landing:

**`problema_en_sus_palabras`** — el agente de copywriting no debe usar el lenguaje del producto para describir el problema; debe usar el lenguaje del cliente. Son campos separados: `problema_en_sus_palabras` (cómo lo describe el visitante) vs. `que_hace` (cómo lo describe el producto).

**`temperatura_trafico`** — determina cuánto espacio dedicar a educación vs. conversión. Un visitante frío desde LinkedIn Ads no sabe quién eres; uno tibio ya conoce que la Ley 21.719 existe. El mismo headline no funciona para ambos.

**`fuente_trafico_principal`** — afecta el copy del hero directamente. Si el tráfico viene de un anuncio sobre la Ley 21.719, el hero puede asumir ese contexto. Si viene de búsqueda orgánica, no puede.

**`objeciones`** — las dudas que el visitante tiene antes de convertir. El landing debe anticiparlas (FAQ, garantías, comparativas). Sin declararlas, el agente las inventa.

---

## 8. El campo más importante del REQUEST.md: `aha_moment_hipotesis`

El "Aha! Moment" es el instante donde el visitante entiende visceralmente el valor del producto. Es la hipótesis central del demo y del Blueprint.

**Por qué es el más importante:** GSD construye el flujo del demo a partir de esta hipótesis. Sin una escena concreta ("el visitante ve X, pasa Y, siente Z"), el Blueprint genera algo genérico que no convierte. Con una escena específica, el agente puede diseñar cada pantalla/interacción con ese momento como destino.

**Cómo escribirlo bien:** no como feature list, sino como escena narrativa. No "el sistema trackea plazos automáticamente" sino "el visitante ve cómo una solicitud ARCO+ llega al sistema, queda registrada automáticamente con un countdown de 30 días y aparece en el tablero Kanban — sin que nadie tuviera que hacer nada manualmente."

---

## 9. Artefactos producidos en esta sesión

| Artefacto | Ubicación | Descripción |
|-----------|-----------|-------------|
| `REQUEST-TEMPLATE.md` | `docs/REQUEST-TEMPLATE.md` | Plantilla completa con 9 secciones, instrucciones por campo, ejemplos basados en ARCO Legal y checklist de Intake |

**Pendiente (identificado pero no creado):**
- `REQUEST-ARCO-LEGAL.md` — el REQUEST.md completado con los datos reales de ARCO Legal, útil como ejemplo de referencia para futuros proyectos

---

## 10. Preguntas abiertas para próximas sesiones

1. **¿Quién completa el REQUEST.md?** ¿El cliente que trae la idea, el SRM, o ambos en conjunto? El nivel técnico de algunos campos (stack, integraciones) puede requerir apoyo del SRM.

2. **¿El REQUEST.md reemplaza o complementa el documento de narrativa estratégica?** Hoy conviven (el PDF de ARCO Legal + el REQUEST.md). ¿Deberían unificarse, o la narrativa estratégica sigue siendo un artefacto separado que se referencia desde el REQUEST.md?

3. **¿Cómo se versiona el REQUEST.md?** Si el cliente cambia la URL o el CTA a mitad del flujo, ¿qué pasa con el Blueprint ya aprobado?

4. **¿Cuáles son las fases GSD del flujo Idea2Landing?** El REQUEST.md está diseñado para alimentar `/gsd-new-project`, pero las fases concretas (discuss → plan → execute → verify) del landing aún no están mapeadas.

5. **¿Cómo se documenta el resultado del gate Landing2MVP?** ¿Quién decide formalmente que la métrica se cumplió y autoriza el inicio del siguiente flujo?

# Evaluación de Checklist — Idea: Evaluación de Nivel de Inglés

**Idea evaluada:** Servicio de evaluación de nivel de inglés (CEFR) para procesos de selección Tech  
**Fecha de evaluación:** 2026-04-26  
**Evaluado por:** [completar]  
**Checklist de referencia:** `tasks/20260426-jgtm-problem-filter-checklist/checklist-filtro-problemas.md`

---

## Paso 0 — Descalificadores Automáticos

- [x] **D1.** ~~El cliente quiere comprar una herramienta o acceso a un software, no un resultado concreto.~~
  → **No aplica.** El proveedor y el cliente final compran un resultado: el reporte de nivel CEFR por postulante. La tecnología es interna al servicio.

- [x] **D2.** ~~La solución requiere hardware físico o presencia física como componente central de entrega.~~
  → **No aplica.** La evaluación puede realizarse de forma remota (voz/texto digital). No hay dependencia física.

- [x] **D3.** ~~El problema ocurrirá una única vez (proyecto one-time, migración puntual, evento único).~~
  → **No aplica.** Los procesos de selección tech son continuos. El proveedor recibe lotes de CVs de forma recurrente.

- [x] **D4.** ~~No existe forma conocida de medir si el problema fue resuelto o no.~~
  → **No aplica.** El resultado es directamente medible: nivel CEFR asignado por postulante, tiempo de entrega del reporte, volumen procesado por período.

> **Resultado Paso 0:** ✅ Sin descalificadores. Continuar evaluación.

---

## Criterio 1 — Especificidad

- [x] **E1.** El problema puede describirse en una sola oración sin ambigüedades.
  → *"Evaluar el nivel de inglés CEFR de postulantes tech y entregar un reporte consolidado, reduciendo el tiempo y aumentando el volumen de evaluaciones por período."* Acotado, sin vaguedad.

- [x] **E2.** Se puede identificar con precisión quién tiene el problema: segmento, cargo, industria y contexto específico.
  → Proveedor: empresa especializada en servicios de aprendizaje de inglés que opera como subcontratista de evaluación para procesos de selección Tech. Segmento perfectamente definido.

- [x] **E3.** Existe al menos un indicador objetivo que permite verificar si el problema fue resuelto.
  → Indicadores disponibles: (a) tiempo promedio por evaluación [días/horas], (b) número de evaluaciones procesadas por semana/mes, (c) concordancia del nivel CEFR asignado vs. criterio experto (accuracy). Todos medibles.

- [x] **E4.** La promesa de valor puede expresarse como un resultado tangible que el cliente recibe.
  → *"El proveedor puede entregar reportes de nivel CEFR de N postulantes en X horas, con la misma precisión que hoy."* Concreto y verificable.

> **Resultado Criterio 1:** ✅ **4/4** — APRUEBA

---

## Criterio 2 — Recurrencia

- [x] **R1.** El problema le ocurre a la misma persona o empresa de forma repetida.
  → El proveedor recibe lotes de CVs de forma continua, vinculado al flujo de selección de sus clientes. El proceso de evaluación ocurre múltiples veces por semana o mes.

- [x] **R2.** La frecuencia es predecible y no depende de circunstancias extraordinarias.
  → Los procesos de selección Tech son sostenidos en el tiempo. Si bien el volumen puede variar, el proceso existe de forma permanente mientras las empresas contraten profesionales.

- [x] **R3.** El afectado lo vive como un dolor sostenido, no como un inconveniente puntual.
  → La limitación de throughput por llamadas individuales es una restricción estructural del modelo actual, no un problema que desaparezca espontáneamente.

> **Resultado Criterio 2:** ✅ **3/3** — APRUEBA

---

## Criterio 3 — Mercado Potencial

- [x] **M1.** Se puede estimar un universo de potenciales clientes y ese universo es significativo.
  → Hay dos ángulos: (a) empresas proveedoras de servicios de evaluación de inglés que operan a escala (potencialmente decenas en Latam); (b) directamente, empresas de selección Tech o áreas de RRHH de empresas tech que contratan en volumen y necesitan evaluaciones de inglés. El segmento de empresas tech en Latam que requiere evaluaciones de inglés en sus procesos de selección es amplio. ⚠️ *Nota: el tamaño exacto del segmento del proveedor directo (empresas como la descrita) podría ser acotado; convendría verificar si el modelo escala a otros proveedores o si se puede ir directamente al cliente final.*

- [x] **M2.** Hay evidencia directa o indirecta de disposición a pagar.
  → El hecho de que ya exista un proveedor que cobra por este servicio es evidencia directa de que el mercado paga. La empresa que encarga las evaluaciones ya destina presupuesto a esto.

- [x] **M3.** El precio potencial del servicio es viable.
  → Las evaluaciones de inglés tienen precios de mercado conocidos (USD 15–50+ por evaluación dependiendo del formato). Un modelo automatizado o semi-automatizado tiene costos de entrega significativamente menores que el modelo de llamadas individuales, lo que hace viable el margen.

- [x] **M4** *(señal de validación)*. Existen competidores o soluciones parciales en el mercado.
  → Sí: Duolingo English Test, IELTS Online, plataformas de hiring como Karat o HackerRank (con módulos de inglés). Estos validan que el mercado existe, aunque no están enfocados en el nicho de evaluación rápida para selección tech en Latam.

> **Resultado Criterio 3:** ✅ **M1 + M2 + M3** cumplidos (+ M4 como señal de respaldo) — APRUEBA
>
> ⚠️ **Observación sobre M1:** Se recomienda validar si el modelo de negocio apunta al proveedor de inglés como cliente directo (mercado acotado) o si puede escalar hacia empresas de selección o áreas de RRHH directamente (mercado más amplio). Esta distinción afecta el tamaño real del mercado potencial.

---

## Criterio 4 — Apalancamiento Tecnológico

- [x] **T1.** La solución puede entregarse como un servicio (el cliente recibe un resultado, no opera un software).
  → Sí. El proveedor sigue entregando reportes CEFR. El cliente final nunca ve la tecnología. CognitionBase construye la automatización interna del proceso.

- [x] **T2.** Existe un flujo de datos o información procesable que puede ser automatizado o asistido por IA.
  → Sí, y es rico: respuestas de voz (→ ASR + análisis lingüístico), respuestas escritas (→ NLP), transcripciones estructuradas (→ scoring automático). El insumo es procesable digitalmente en todas sus formas.

- [x] **T3.** El problema puede resolverse mediante automatización, agentes IA, procesamiento de datos o Ingeniería de Software.
  → Sí. Stack aplicable: modelos de lenguaje para evaluación lingüística, ASR para procesamiento de voz, scoring calibrado con criterio CEFR, flujo de revisión humana para casos límite. Todo dentro del dominio tecnológico de CognitionBase.

- [x] **T4.** Tenemos acceso al conocimiento experto del dominio necesario para garantizar la calidad.
  → El proveedor posee el conocimiento experto en evaluación CEFR. El acuerdo con ellos es precisamente lo que habilita la calibración de los modelos. CognitionBase aporta el stack técnico; el proveedor aporta el criterio metodológico. La combinación cubre T4.

> **Resultado Criterio 4:** ✅ **4/4** — APRUEBA

---

## Resultado Final

| # | Criterio                         | Resultado |
|---|----------------------------------|-----------|
| 0 | Descalificadores automáticos     | ✅ Ninguno |
| 1 | Especificidad (4/4)              | ✅ Aprueba (4/4) |
| 2 | Recurrencia (3/3)                | ✅ Aprueba (3/3) |
| 3 | Mercado Potencial (M1+M2+M3)     | ✅ Aprueba (con observación en M1) |
| 4 | Apalancamiento Tecnológico (4/4) | ✅ Aprueba (4/4) |

### ✅ INGRESA AL BACKLOG

La idea cumple todos los criterios del filtro. Se recomienda avanzar al flujo de estructuración del **JustDemo Service**.

---

## Próximos Pasos Sugeridos

1. **Clarificar el segmento cliente objetivo** antes de construir el demo: ¿el proveedor de inglés como cliente directo, o empresas de selección/RRHH directamente? Esto impacta el tamaño de mercado y la propuesta de valor del landing.
2. **Validar el volumen actual** del proveedor: ¿cuántas evaluaciones por mes? Esto define el impacto potencial y ancla la propuesta de mejora con números concretos.
3. **Acordar acceso a metodología** CEFR del proveedor para calibrar los modelos.
4. Estructurar el JustDemo: landing funcional con demo interactiva que muestre el flujo automatizado de evaluación y el reporte resultante.

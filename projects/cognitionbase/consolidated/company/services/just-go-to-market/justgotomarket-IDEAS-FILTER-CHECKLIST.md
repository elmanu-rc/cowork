# Checklist de Filtro de Problemas — JustGoToMarket

> **Propósito:** Evaluar objetivamente si un problema cumple con los criterios para ingresar al backlog de JustGoToMarket. Un problema debe pasar **todos los criterios** para ser considerado. Si falla en uno, se descarta sin excepciones.
>
> **Quién lo aplica:** SRM (Service Request Manager) durante el proceso de clasificación upstream.

---

## Paso 0 — Descalificadores Automáticos

Evaluar primero. Si cualquiera de estas condiciones aplica, **rechazar de inmediato sin continuar**.

- [ ] **D1.** El cliente quiere comprar una herramienta o acceso a un software, no un resultado concreto.
- [ ] **D2.** La solución requiere hardware físico o presencia física como componente central de entrega.
- [ ] **D3.** El problema ocurrirá una única vez (proyecto one-time, migración puntual, evento único).
- [ ] **D4.** No existe forma conocida de medir si el problema fue resuelto o no.

> **Regla:** Si algún ítem está marcado → ❌ **RECHAZADO AUTOMÁTICAMENTE**. Documentar cuál y por qué.

---

## Criterio 1 — Especificidad

**El problema está bien acotado y permite formular una promesa de valor concreta y verificable.**

- [ ] **E1.** El problema puede describirse en una sola oración, sin ambigüedades ni términos vagos (ej: "mejorar la eficiencia" no califica; "reducir el tiempo de X de N días a M horas" sí).
- [ ] **E2.** Se puede identificar con precisión quién tiene el problema: segmento, cargo, industria y contexto específico.
- [ ] **E3.** Existe al menos un indicador objetivo que permite verificar si el problema fue resuelto (tiempo, costo, tasa de error, volumen, etc.).
- [ ] **E4.** La promesa de valor puede expresarse como un resultado tangible que el cliente recibe (ej: "el cliente recibe X cada Y días").

> **Regla:** Se requieren **4/4** para aprobar este criterio.

---

## Criterio 2 — Recurrencia

**El problema no es un evento único; ocurre con una frecuencia predecible para el mismo afectado.**

- [ ] **R1.** El problema le ocurre a la misma persona o empresa de forma repetida (diario / semanal / mensual / por ciclo de negocio).
- [ ] **R2.** La frecuencia es predecible y no depende de circunstancias extraordinarias o irrepetibles.
- [ ] **R3.** El afectado lo vive como un dolor sostenido, no como un inconveniente puntual que ya olvidó.

> **Regla:** Se requieren **3/3** para aprobar este criterio.

---

## Criterio 3 — Mercado Potencial

**Existe un número significativo de potenciales clientes que enfrentan este problema y estarían dispuestos a pagar.**

- [ ] **M1.** Se puede estimar un universo de potenciales clientes y ese universo es lo suficientemente grande como para justificar la inversión *(mínimo orientativo: +50 empresas o +200 personas que encajan en el segmento objetivo)*.
- [ ] **M2.** Hay evidencia directa o indirecta de disposición a pagar: alguien ya cobra por resolver algo parecido, el segmento tiene presupuesto conocido para este tipo de problemas, o se obtuvo señal explícita de interés.
- [ ] **M3.** El precio potencial del servicio es viable: se puede estimar un precio que cubra el costo de entrega más un margen razonable sin ser prohibitivo para el segmento.
- [ ] **M4** *(opcional, señal de validación)*. Existen competidores o soluciones parciales actualmente en el mercado, lo que confirma que el problema es real y que hay mercado activo.

> **Regla:** Se requieren **M1 + M2 + M3** (obligatorios). M4 es evidencia de respaldo, no excluyente.

---

## Criterio 4 — Apalancamiento Tecnológico

**La solución puede construirse sobre nuestra experiencia en Ingeniería de Software, IA y conocimiento experto del dominio.**

- [ ] **T1.** La solución puede entregarse como un servicio donde el cliente recibe un resultado — no como un producto de software que el cliente opera por su cuenta.
- [ ] **T2.** Existe un flujo de datos, documentos o información procesable que puede ser automatizado o asistido por IA como parte del núcleo de la solución.
- [ ] **T3.** El problema puede resolverse (total o parcialmente) mediante automatización, agentes IA, procesamiento de datos o Ingeniería de Software — sin depender de recursos físicos o habilidades no tecnológicas como componente crítico.
- [ ] **T4.** Tenemos acceso al conocimiento experto del dominio necesario (interno en el equipo, o vía un experto identificable) para garantizar la calidad de la solución.

> **Regla:** Se requieren **4/4** para aprobar este criterio.

---

## Resultado de la Evaluación

| # | Criterio                         | Resultado |
|---|----------------------------------|-----------|
| 0 | Descalificadores automáticos     | ✅ Ninguno / ❌ [indicar cuál] |
| 1 | Especificidad (4/4)              | ✅ Aprueba / ❌ Falla [indicar ítem] |
| 2 | Recurrencia (3/3)                | ✅ Aprueba / ❌ Falla [indicar ítem] |
| 3 | Mercado Potencial (M1+M2+M3)     | ✅ Aprueba / ❌ Falla [indicar ítem] |
| 4 | Apalancamiento Tecnológico (4/4) | ✅ Aprueba / ❌ Falla [indicar ítem] |

### Decisión Final

- **Todos los criterios en ✅ →** `INGRESA AL BACKLOG` — pasar al flujo de estructuración del JustDemo Service.
- **Algún criterio en ❌ →** `RECHAZADO` — documentar criterio fallido y razón específica. Notificar a quien propuso el problema con feedback concreto.

---

## Notas de Aplicación

**Ante la duda en un criterio:** Antes de rechazar, se permite una sesión corta de descubrimiento (máximo 30 minutos) con quien propone el problema para obtener la información faltante. Si tras esa sesión el criterio sigue sin poder verificarse, se rechaza.

**Un rechazo no es definitivo:** Un problema rechazado puede re-evaluarse si quien lo propone presenta nueva información que cambie la evaluación de los criterios fallidos.

**El checklist no reemplaza el juicio:** Los criterios son filtros objetivos, pero la decisión final puede considerar contexto estratégico. En ese caso, la excepción debe documentarse y ser aprobada explícitamente por el SDM.

**Sobre M4 (competidores):** La ausencia de competidores no descalifica un problema — puede ser un mercado no atendido. Pero la presencia de competidores es una señal positiva fuerte que refuerza M1 y M2.

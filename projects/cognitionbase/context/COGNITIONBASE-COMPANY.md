# Proyecto: CognitionBase - The Definitive Digital Product Incubator

## 1. Visión General

CognitionBase es un spinoff de **23people** diseñado para ser el motor de innovación y desarrollo de productos digitales del grupo. Opera bajo un modelo de servicios especializado:

- **Idea2Market Service:** Transforma ideas de negocio en productos digitales validados (MVP) con una velocidad y eficiencia radical, apalancándose en la orquestación de agentes de IA.
- **Technical Evaluations Service:** Garantiza la excelencia del talento en el ecosistema 23people mediante el diseño y ejecución de evaluaciones técnicas de alto nivel para procesos de selección.

## 2. Misión

Ser la **Incubadora de Productos Digitales definitiva**, eliminando la fricción entre la conceptualización y la validación de mercado, utilizando una estructura de élite altamente automatizada llamada **Iron-Legion**.

## 3. El Protocolo Iron-Legion (GSD-Inspired)

Inspirado en los principios de **Get Shit Done (GSD)**, el protocolo prioriza el impacto sobre la ceremonia, la entrega sobre la documentación excesiva y la responsabilidad absoluta (*Extreme Ownership*).

### Principios Fundamentales

- **Output-First:** No se inicia nada sin definir cómo se ve el éxito (Landing funcional o MVP operable).
- **Atomic Decomposition:** Las ideas se rompen en unidades de entrega mínimas que los agentes de IA puedan ejecutar en ciclos de horas.
- **Bias for Action:** Ante la duda, se elige el camino del despliegue. La perfección se alcanza mediante la iteración en producción, no en el diseño.
- **Boring Tools for High Speed:** Se utilizan stacks probados y de baja fricción para maximizar la velocidad de entrega.

## 4. Servicio: De Idea a Mercado

El servicio Idea2Market opera como dos sub-flujos secuenciales con un gate de validación entre ellos:

**Idea2Landing (I2LP)** → *(gate: métrica de tracción definida por proyecto)* → **Landing2MVP (L2MVP)**

### Flujo 1: Idea2Landing (I2LP)

- **Input:** `I2LP-REQUEST-[project-name].md` validado — documento unificado con narrativa estratégica, datos de marketing digital, datos operacionales y GSD scope.
- **Etapas:** Intake & Validación → Blueprint → Copy & Marketing Design → UI/UX Design → Build (Landing + Demo) → QA, SEO & Analytics → Deploy a Producción.
- **Output:** Landing live + demo interactivo accesible + analytics activo.
- **Tiempo objetivo:** No definido.

> Para detalle completo del flujo, artefactos y campos del REQUEST.md, ver `docs/services/I2LP-FLOW.md`.

### Flujo 2: Landing2MVP (L2MVP)

- **Objetivo:** Entrega de un MVP funcional en **< 6 semanas**, condicionado a que el landing supere el gate de tracción definido.
- **Ejecución:** Desarrollo asistido por la Iron-Legion (Agentes de IA coordinados).
- **Calidad:** Auditoría automática de seguridad y eficacia en cada pull request.

## 5. Roles y Responsabilidades Operativas

- **Lead Dev AI & SDM (Service Delivery Manager):** Actúa como el **Service Delivery Manager (SDM)** de ambos servicios. Es responsable de la calidad técnica, la supervisión del flujo de trabajo (Downstream Kanban), el cumplimiento de las métricas de ciclo y la orquestación de la Iron-Legion. Es el puente entre el diseño del Blueprint y la entrega final.
- **SRM (Service Request Manager):** Encargado de la gestión de la demanda y el Kanban ascendente (Upstream). Clasifica, prioriza y valida administrativamente las solicitudes (ideas o evaluaciones) antes de ingresarlas al flujo técnico, asegurando que los requisitos estén claros para el equipo de entrega.
- **Devs AI (Iron-Legion):** Ejecutores de élite que operan y afinan los flujos de trabajo basados en agentes.

## 6. Métricas de Éxito (KPIs)

1. **I2LP Cycle-Time:** Tiempo desde la validación del `I2LP-REQUEST-[project-name].md` hasta el despliegue del landing y demo funcional. No definido aun.
2. **LP2MVP Cycle-Time:** Tiempo desde la validación del `L2MVP-REQUEST-[project-name].md` hasta el despliegue del MVP funcional. No definido aun.
3. **Automation Ratio:** % de tareas de ingeniería asistidas por IA.
4. **Tech Evaluations Lead-Time:** Tiempo promedio de entrega de informes de evaluación técnica.
5. **Tech Evaluations Throughput:** Número de evaluaciones técnicas completadas por período (semana/mes).
6. **Post-Delivery Defect Rate:** Número de bugs o correcciones solicitadas por el cliente dentro de los 7 días posteriores a la entrega, por tipo de entrega (Landing, Demo, MVP, Informe). Target: ≤1 por entrega.

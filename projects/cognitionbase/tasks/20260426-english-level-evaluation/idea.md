# Idea: Servicio de Evaluación de Nivel de Inglés para Procesos de Selección Tech

**Fecha de registro:** 2026-04-26  
**Estado:** En evaluación — pendiente revisión checklist JustGoToMarket

---

## Descripción del Problema

Las empresas que realizan procesos de selección de profesionales Tech necesitan evaluar el nivel de inglés (escala CEFR: A1, A2, B1, B2, C1, C2) de cada postulante como parte del flujo de selección.

Actualmente, este proceso es delegado a un proveedor externo especializado en servicios de aprendizaje del idioma inglés. El flujo vigente funciona así:

1. Se envía al proveedor un correo con el conjunto de CVs de postulantes a evaluar.
2. El proveedor llama individualmente a cada postulante y realiza una entrevista acotada.
3. Durante la entrevista, el evaluador humano determina el nivel CEFR del postulante mediante sus respuestas orales.
4. El proveedor genera y entrega un reporte consolidado con el nivel de inglés de cada postulante.

## Dolor Identificado

El proceso actual tiene limitaciones claras:

- **Velocidad:** Cada evaluación requiere una llamada individual, lo que vuelve el proceso lento cuando el volumen de postulantes es alto.
- **Escalabilidad:** El throughput está limitado por la disponibilidad de evaluadores humanos.
- **Costo operativo:** El modelo de llamadas individuales es intensivo en tiempo humano especializado.

## Hipótesis de Solución

El proveedor tiene conocimiento experto en metodología de evaluación CEFR y en las características lingüísticas que definen cada nivel. Se cree que este conocimiento, combinado con el estado del arte en modelos de lenguaje (LLMs), procesamiento de voz (ASR) y evaluación automática de competencias lingüísticas, podría:

- Reducir significativamente el tiempo por evaluación.
- Aumentar el volumen de evaluaciones procesadas por período.
- Mantener o mejorar la precisión del nivel CEFR asignado, apoyado en la supervisión experta del proveedor.

La tecnología sería un habilitador interno del servicio del proveedor. El cliente final (la empresa que usa el servicio de selección) seguiría recibiendo el mismo resultado: un reporte con el nivel de inglés de cada postulante.

## Modelo de Servicio Propuesto

CognitionBase construye la infraestructura tecnológica que permite al proveedor procesar evaluaciones de inglés de forma automatizada o semi-automatizada, apalancando:

- Modelos de lenguaje para análisis de respuestas escritas u orales.
- ASR (Automatic Speech Recognition) para transcripción de respuestas de voz.
- Scoring automático calibrado con el conocimiento experto del proveedor (escala CEFR).
- Dashboard o flujo de revisión para que el evaluador humano supervise y valide casos límite.

El resultado final que recibe el cliente no cambia: un reporte de nivel CEFR por postulante. Lo que cambia es la velocidad, el costo y la escala con que el proveedor puede entregarlo.

## Partes Involucradas

- **Cliente directo de CognitionBase:** La empresa proveedora de servicios de aprendizaje de inglés.
- **Cliente final (usuario del resultado):** Las empresas que contratan el servicio de evaluación para sus procesos de selección Tech.
- **Sujeto evaluado:** Los postulantes a posiciones Tech.

## Notas y Preguntas Abiertas

- ¿El proveedor tiene interés en ceder o compartir su metodología de evaluación para entrenar/calibrar modelos?
- ¿Cuántas evaluaciones por mes maneja actualmente el proveedor? Esto define el impacto potencial.
- ¿El cliente final tiene expectativas de tiempo de entrega que hoy no se cumplen?
- ¿Hay regulaciones o estándares de calidad que la evaluación deba cumplir (Cambridge, ALTE, etc.)?

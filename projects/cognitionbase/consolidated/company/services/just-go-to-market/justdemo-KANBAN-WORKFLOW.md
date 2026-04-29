# Flujo Kanban — JustDemo

El flujo JustDemo recibe un **Request** y entrega **evidencia verificable** de que tres entregables están desplegados en producción: el landing page, el demo y la guía para medir la tracción del landing.

---

## Etapas del flujo

### 1. Backlog

El request entra al sistema. Aún no hay trabajo activo sobre él — es simplemente la captura de la necesidad.

**Criterio de salida:**

- El request está registrado con suficiente información para poder ser trabajado: qué se necesita, quién lo solicita y cuál es el contexto de uso.
- Ha sido priorizado y hay capacidad disponible para comenzar a definirlo.

---

### 2. Por hacer

Se determina con precisión qué debe construirse. El foco está en acotar el alcance de los tres entregables antes de tocar cualquier línea de código o contenido.

**Criterio de salida:**

- El landing tiene definido su propósito, audiencia, mensaje principal y URL objetivo en producción.
- El demo tiene definido su alcance: qué flujo muestra, qué datos usa y en qué entorno debe correr.
- La guía tiene definidas las métricas que medirá, la fuente de datos de cada una y el período de medición inicial.
- Los tres entregables tienen un responsable asignado.

---

### 3. Construyendo

Se ejecuta el trabajo de creación: el landing, el demo y la guía se desarrollan en paralelo o en secuencia según el equipo.

**Criterio de salida:**

- El landing está completo y funcional en un entorno de staging o local.
- El demo corre sin errores y cubre el flujo definido en la etapa anterior.
- La guía está redactada con instrucciones accionables para medir cada métrica definida.
- Los tres entregables están listos para ser revisados por alguien distinto a quien los construyó.

---

### 4. En revisión

Los tres entregables son evaluados antes de ir a producción. El objetivo es detectar problemas de calidad, coherencia o alineación con lo definido en la etapa 2.

**Criterio de salida:**

- El landing comunica el mensaje correcto, carga sin errores y está optimizado para la acción que se quiere provocar.
- El demo corre de principio a fin sin errores en el entorno de revisión.
- La guía es comprensible para alguien externo al equipo y las métricas son medibles con las herramientas disponibles.
- No hay observaciones bloqueantes pendientes de resolver.

---

### 5. Desplegando

Los tres entregables se llevan a producción. Esta etapa cubre el proceso técnico de despliegue: CI/CD, configuración de dominio, variables de entorno y cualquier dependencia de infraestructura.

**Criterio de salida:**

- El landing está publicado en su URL de producción definitiva.
- El demo está accesible en producción con los datos y configuración correctos.
- La guía está publicada o distribuida en el canal acordado con el solicitante.
- No hay errores de despliegue sin resolver.

---

### 6. Verificando en producción

Se confirma que todo funciona como se espera en el entorno real y se recolecta la evidencia que se entregará al solicitante.

**Criterio de salida:**

- El landing carga correctamente en su URL de producción desde un navegador sin sesión activa.
- El demo corre de principio a fin en producción sin errores.
- La guía es accesible desde el canal de distribución acordado.
- Se cuenta con evidencia documentada: capturas de pantalla o video del landing y el demo en vivo, URL pública de cada entregable, y métricas baseline iniciales del landing (visitas, tasa de rebote u otra métrica de tracción definida en la etapa 2).

---

### 7. Entregado

La evidencia se entrega al solicitante y el ciclo se cierra.

**Criterio de salida:**

- El solicitante recibió el paquete de evidencia con los tres entregables verificados.
- El solicitante confirmó que lo recibido corresponde a lo que solicitó.
- La tarjeta está cerrada y no hay acciones pendientes derivadas de este request.

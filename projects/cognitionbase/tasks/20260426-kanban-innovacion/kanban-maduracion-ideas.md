# Flujo Kanban: Maduración de Ideas de Innovación — CognitionBase

## Propósito

Este flujo define el proceso estándar para llevar una idea inmadura de proyecto de innovación hasta un landing page desplegado en producción con métricas de tracción activas. Cada columna representa una etapa con criterios de entrada y salida claros, y entregables específicos que deben completarse antes de avanzar.

---

## Columnas del Flujo

### 1. 💡 Idea Cruda

**Propósito:** Punto de entrada del flujo. Captura cualquier idea inicial de proyecto, sin necesidad de estructura ni madurez.

**Criterio de entrada:**
- Existe una intuición, observación o propuesta de proyecto, aunque sea vaga o incompleta.

**Trabajo en esta etapa:**
- Escribir la idea en una o dos oraciones: ¿Qué problema podría resolverse? ¿Para quién?
- No se requiere investigación ni validación previa.

**Criterio de salida:**
- La idea está registrada y asignada a un responsable de formalizarla.
- Existe al menos una frase que describe el problema o la oportunidad.

---

### 2. 📄 Formalización de Idea

**Propósito:** Convertir la idea cruda en un documento estructurado que sirva como base para el equipo. Esta etapa transforma la intuición en una narrativa coherente y estratégica.

**Criterio de entrada:**
- La idea está registrada en la columna anterior con responsable asignado.

**Trabajo en esta etapa:**
Redactar el documento **"Perfil de Idea v1"** que incluya:

| Sección | Descripción |
|---|---|
| **Contexto** | Situación actual del mercado o entorno que hace relevante esta idea |
| **Desafío** | Problema concreto que se quiere resolver y para quién |
| **Solución** | Descripción de la propuesta de valor y cómo aborda el desafío |
| **Plan Estratégico** | Enfoque general: segmento objetivo, modelo de negocio tentativo, diferenciación |
| **Plan de Ejecución** | Primeros pasos, recursos necesarios, riesgos identificados y supuestos clave |

**Criterio de salida:**
- El documento "Perfil de Idea v1" está completo en todas sus secciones.
- Ha sido revisado por al menos un miembro del equipo distinto al autor.
- El equipo ha dado luz verde para avanzar al brief de contenido.

**Entregable:** `perfil-idea-v1.md` (o equivalente en el sistema de documentación del equipo)

---

### 3. 📝 Brief de Contenido

**Propósito:** Definir con precisión los mensajes clave, el perfil del cliente y los elementos de comunicación que guiarán el diseño y desarrollo del landing page.

**Criterio de entrada:**
- El documento "Perfil de Idea v1" está aprobado.

**Trabajo en esta etapa:**
Redactar el documento **"Brief de Contenido"** que incluya:

| Sección | Descripción |
|---|---|
| **Perfil de Cliente Ideal (ICP)** | Quién es el usuario/cliente objetivo: industria, rol, dolores, contexto, nivel de sofisticación |
| **Propuesta Única de Valor (UVP)** | Frase concisa que comunica el beneficio principal y la diferenciación frente a alternativas |
| **Características de la Solución** | Lista priorizada de funcionalidades o atributos clave del producto/servicio |
| **Llamado a la Acción (CTA)** | Qué se espera que haga el visitante: agendar demo, registrarse, contactar, etc. |
| **Mensajes secundarios** | Argumentos de apoyo, prueba social, casos de uso o analogías útiles |
| **Tono y voz** | Personalidad de la marca: formal/informal, técnico/accesible, aspiracional/pragmático |
| **Preguntas frecuentes anticipadas** | Objeciones o dudas comunes que el landing debe responder |

**Criterio de salida:**
- El Brief de Contenido está completo y aprobado por el responsable de la idea.
- El equipo de diseño/desarrollo tiene claridad suficiente para construir el landing.

**Entregable:** `brief-contenido.md` (o equivalente)

---

### 4. 🛠️ Implementación

**Propósito:** Construir todos los componentes necesarios para el lanzamiento: el landing page, el demo, los mecanismos de contacto y las herramientas de medición.

**Criterio de entrada:**
- El Brief de Contenido está aprobado.
- Existe un entorno de staging o desarrollo disponible.

**Trabajo en esta etapa:**

#### 4.1 Landing Page
- Desarrollar el landing page siguiendo el Brief de Contenido.
- Incluir todas las secciones: hero, UVP, características, CTA, testimonios/prueba social (si aplica), FAQ.
- Diseño responsivo y optimizado para velocidad de carga.

#### 4.2 Demo
- Preparar un demo funcional, grabación de pantalla o prototipo navegable que muestre la solución en acción.
- Embeber o vincular el demo desde el landing page.

#### 4.3 Mecanismos de Contacto
- Configurar dirección de correo de contacto dedicada al proyecto (ej. `hola@proyecto.cl`).
- Instalar formulario de contacto o botón de "Quiero saber más" conectado al correo.
- Opcionalmente: configurar integración con herramienta de CRM o lista de correo.

#### 4.4 Google Analytics
- Crear propiedad en Google Analytics 4 para el proyecto.
- Instalar el snippet de tracking en el landing page.
- Configurar eventos clave: visita a página, clic en CTA, envío de formulario.
- Verificar que los eventos se estén registrando correctamente en modo debug.

**Criterio de salida:**
- El landing page está completo y revisado internamente.
- El demo es accesible desde el landing.
- El correo de contacto y formulario funcionan de extremo a extremo.
- Google Analytics registra tráfico y eventos correctamente en staging.
- Se ha realizado una revisión de QA en distintos dispositivos y navegadores.

---

### 5. ✅ Listo

**Propósito:** El proyecto está en producción y activo. El landing page es públicamente accesible, el demo está disponible y las métricas de tracción están siendo capturadas.

**Criterio de entrada:**
- Todos los criterios de salida de la etapa de Implementación están cumplidos.
- El dominio o URL de producción está configurado y apuntando al landing.

**Checklist de cierre:**

- [ ] Landing page desplegado en URL de producción (ej. `https://proyecto.cl` o subdominio).
- [ ] SSL/HTTPS activo.
- [ ] Demo accesible desde el landing.
- [ ] Formulario/correo de contacto operativo en producción.
- [ ] Google Analytics 4 registrando eventos en producción.
- [ ] Dashboard básico de métricas configurado (sesiones, clics en CTA, conversiones).
- [ ] Equipo notificado del lanzamiento con la URL de producción.

**Entregable final:** URL pública del landing page con métricas activas.

---

## Resumen Visual del Flujo

```
[💡 Idea Cruda] → [📄 Formalización] → [📝 Brief de Contenido] → [🛠️ Implementación] → [✅ Listo]
```

| Etapa | Responsable sugerido | Entregable clave |
|---|---|---|
| Idea Cruda | Cualquier miembro del equipo | Idea registrada (1-2 oraciones) |
| Formalización | Responsable de la idea | `perfil-idea-v1.md` |
| Brief de Contenido | Responsable + equipo de producto | `brief-contenido.md` |
| Implementación | Equipo de diseño/desarrollo | Landing + demo + GA + contacto |
| Listo | Responsable de la idea | URL en producción con métricas activas |

---

## Notas de Operación

- **Bloqueos:** Si una tarjeta no puede avanzar por falta de información o recursos, debe marcarse como bloqueada con una nota clara del motivo.
- **Revisiones:** Las etapas de Formalización y Brief de Contenido requieren revisión explícita antes de avanzar. No es suficiente que el autor declare el documento como listo.
- **Iteración:** Es válido devolver una tarjeta a una etapa anterior si se descubre información que invalida supuestos clave.
- **Frecuencia de revisión del tablero:** Se recomienda una revisión semanal del estado de todas las tarjetas activas.

# CLAUDE.md

This file provides guidance to Claude when working with content in this repository.

## Project Overview

This is the project that contains the information about the CognitionBase company. Here different tasks related to the company are documented.

Mas información sobre CognitionBase: `context/company/COGNITIONBASE.md`

## Content Organization

Esta carpeta contiene dos subcarpetas principales: `context` y `tasks`.

- `context` — Almacena contenido validado y estable, disponible como referencia en múltiples sesiones. Úsalo como fuente de verdad para el proyecto. NO TIENES PERMITIDO ESCRIBIR EN ESTA CARPETA SIN UNA CONFIRMACIÓN EXPLICITA DEL USUARIO.

- `tasks` — Contiene contenido temporal asociado a tareas específicas. Ignora su contenido preexistente, ya que puede estar incompleto o sin validar.

## Guidelines for Claude

### Restricción de escritura en carpeta context

No escribir nunca en la carpeta `context/` del proyecto CognitionBase sin autorización explícita e inequívoca del usuario.

**Why:** La carpeta `context/` almacena información validada y estable. El usuario dejó en claro que una solicitud como "actualiza este archivo" no constituye autorización — hay que pedir permiso explícito antes de tocar cualquier archivo en esa carpeta.

**How to apply:** Cuando se pida editar o actualizar un archivo en `context/`, el flujo correcto es:

1. Crear el contenido propuesto en `tasks/YYYYMMDD-hhmm-[slug]/`
2. Presentar el resultado al usuario para revisión
3. Esperar que el usuario diga explícitamente algo como "tienes permiso para editarlo en context" o equivalente
4. Solo entonces mover o copiar el contenido a `context/`

# Tareas Frecuentes - Product Studio

> Plantillas de tareas comunes con inputs/outputs definidos.

---

## 1. PRD de Feature (GENESIS App)

### Input Requerido
- Nombre de la feature
- Plataforma (mobile/web)
- Problema que resuelve
- Requisitos conocidos

### Output
- Carpeta `outputs/prds/feature-[nombre]/`
  - PRD.md
  - CLAUDE.md (context file)

### Tiempo Estimado
~25 minutos

---

## 2. PRD de Feature (NGX COACH)

### Input Requerido
- Nombre de la feature
- Usuario (coach/admin)
- Problema para el coach
- Integraciones requeridas

### Output
- Carpeta `outputs/prds/coach-[nombre]/`
  - PRD.md
  - CLAUDE.md

### Tiempo Estimado
~25 minutos

---

## 3. PRD de Agente ADK

### Input Requerido
- Nombre del agente
- Pilar al que pertenece
- Responsabilidades
- Interacciones con otros agentes

### Output
- Carpeta `outputs/prds/agent-[nombre]/`
  - PRD.md (usando template ADK-A2A)
  - CLAUDE.md
  - skeleton/ (opcional)

### Tiempo Estimado
~30 minutos

---

## 4. PRD de Workflow n8n

### Input Requerido
- Nombre del workflow
- Trigger (webhook/schedule/evento)
- Pasos del flujo
- Integraciones necesarias

### Output
- Carpeta `outputs/prds/workflow-[nombre]/`
  - PRD.md
  - workflow-template.json (si aplica)

### Tiempo Estimado
~20 minutos

---

## 5. Handoff Package Completo

### Input Requerido
- PRD de referencia
- Coding agent destino
- Nivel de contexto deseado
- Tarea específica

### Output
- Carpeta `outputs/handoffs/[tarea]/`
  - CONTEXT.md
  - TASK.md
  - MASTER_PROMPT.md
  - references/ (si aplica)

### Tiempo Estimado
~20 minutos

---

## 6. Handoff para Bug Fix

### Input Requerido
- Descripción del bug
- Ubicación en código
- Pasos para reproducir
- Comportamiento esperado

### Output
- Carpeta `outputs/handoffs/fix-[nombre]/`
  - CONTEXT.md (minimal)
  - TASK.md
  - MASTER_PROMPT.md

### Tiempo Estimado
~10 minutos

---

## 7. Extracción de Requisitos

### Input Requerido
- Conversación o documento fuente
- Tipo de proyecto

### Output
- `outputs/prds/requirements-[nombre].md`
  - Requisitos categorizados
  - Gaps identificados
  - Preguntas de clarificación

### Tiempo Estimado
~15 minutos

---

## 8. Skeleton de Feature Mobile

### Input Requerido
- PRD de referencia
- Feature name

### Output
- `outputs/handoffs/[feature]/skeleton/`
  - Estructura de componentes
  - Hooks
  - Services
  - Types
  - Tests básicos

### Tiempo Estimado
~15 minutos

---

## 9. Skeleton de Agente ADK

### Input Requerido
- PRD de referencia
- Nombre del agente

### Output
- `outputs/handoffs/agent-[nombre]/skeleton/`
  - agent.py
  - tools/
  - prompts/
  - tests/

### Tiempo Estimado
~15 minutos

---

## 10. Context File para Proyecto Existente

### Input Requerido
- Nombre del proyecto
- PRD existente
- Coding agent destino

### Output
- `outputs/handoffs/[proyecto]/`
  - CLAUDE.md o GEMINI.md

### Tiempo Estimado
~10 minutos

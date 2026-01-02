# Tareas Frecuentes — Product Studio

> Plantillas de tareas para documentación técnica. Filosofía: Lethal Specificity.

---

## 📋 TAREA: PRD de Feature

### Input Requerido
- Nombre de la feature
- Plataforma (Mobile/Web/Backend)
- Descripción del problema que resuelve
- Prioridad (Alta/Media/Baja)
- Agentes involucrados (si aplica)

### Output Esperado
- PRD completo usando template
- Guardado en `outputs/prds/[feature]-prd-[fecha].md`

### Checklist Específico
- [ ] Problem statement claro
- [ ] User stories completas
- [ ] Scope definido (in/out)
- [ ] Tasks granulares y estimadas
- [ ] Dependencias identificadas
- [ ] Criterios de éxito medibles

---

## 🤖 TAREA: PRD de Agente

### Input Requerido
- Nombre del agente
- Framework (ADK/Agent SDK/LangGraph)
- Propósito del agente
- Tools que necesita
- Modelo base (Gemini/Claude)

### Output Esperado
- PRD de agente usando template ADK/A2A
- Guardado en `outputs/prds/[agente]-prd-[fecha].md`

### Checklist Específico
- [ ] System prompt definido
- [ ] Tools especificados
- [ ] A2A config si aplica
- [ ] Integration points claros
- [ ] Testing requirements

---

## 📦 TAREA: Context File (CLAUDE.md)

### Input Requerido
- Nombre del proyecto
- Tipo (Feature/Agent/Workflow/Bugfix)
- Stack tecnológico
- Tarea específica a realizar

### Output Esperado
- CLAUDE.md optimizado para Claude Code
- Guardado en `outputs/context/[proyecto]-CLAUDE.md`

### Checklist Específico
- [ ] Quick reference en primeras líneas
- [ ] Paths exactos incluidos
- [ ] Comandos completos
- [ ] DO NOT section presente
- [ ] Tarea actual clara

---

## 🎯 TAREA: Handoff Package

### Input Requerido
- Descripción de la tarea
- Proyecto afectado
- Coding agent destino
- Archivos relevantes

### Output Esperado
- Carpeta con CONTEXT.md, TASK.md, MASTER_PROMPT.md
- Guardado en `outputs/handoffs/[tarea]-[fecha]/`

### Checklist Específico
- [ ] Contexto mínimo viable
- [ ] Tarea específica y clara
- [ ] Prompt de inicio funcional
- [ ] Referencias incluidas

---

## 🔄 TAREA: PRD de Workflow

### Input Requerido
- Nombre del workflow
- Plataforma (n8n/Cloud Functions)
- Trigger type
- Objetivo del workflow
- Servicios/APIs involucrados

### Output Esperado
- PRD de workflow completo
- Guardado en `outputs/prds/[workflow]-prd-[fecha].md`

### Checklist Específico
- [ ] Trigger claramente definido
- [ ] Pasos documentados
- [ ] Error handling especificado
- [ ] Credentials listadas
- [ ] Testing scenarios

---

## 📐 TAREA: API Spec

### Input Requerido
- Endpoint (método + path)
- Servicio al que pertenece
- Propósito del endpoint
- Autenticación requerida

### Output Esperado
- Especificación completa del endpoint
- Guardado en `outputs/specs/api-[endpoint]-[fecha].md`

### Checklist Específico
- [ ] Request schema completo
- [ ] Response schemas (success + errors)
- [ ] Ejemplos incluidos
- [ ] Error codes documentados

---

## 🗄️ TAREA: Database Schema

### Input Requerido
- Nombre de tabla/modelo
- Propósito
- Relaciones con otras tablas
- Queries esperadas

### Output Esperado
- Especificación de schema
- Guardado en `outputs/specs/db-[tabla]-[fecha].md`

### Checklist Específico
- [ ] Tipos correctos
- [ ] Constraints definidos
- [ ] Indexes sugeridos
- [ ] RLS policies si aplica

---

## 🔍 TAREA: Requirements Extraction

### Input Requerido
- Documento o conversación fuente
- Contexto del proyecto
- Stakeholders involucrados

### Output Esperado
- Lista de requisitos categorizados
- Guardado en `outputs/analysis/requirements-[proyecto]-[fecha].md`

### Checklist Específico
- [ ] Funcionales separados de técnicos
- [ ] Prioridades asignadas
- [ ] Gaps identificados
- [ ] Preguntas de clarificación

---

## 🐛 TAREA: Bug Fix Handoff

### Input Requerido
- Descripción del bug
- Steps to reproduce
- Expected vs actual behavior
- Archivos relevantes

### Output Esperado
- Handoff package para bugfix
- Guardado en `outputs/handoffs/bugfix-[nombre]-[fecha]/`

### Checklist Específico
- [ ] Bug claramente descrito
- [ ] Reproducible steps
- [ ] Archivos relevantes identificados
- [ ] Suggested approach si es posible
- [ ] Testing criteria

---

## Principios de Este Workspace

### Lethal Specificity
```
❌ "Crea el componente de usuario"
✅ "Crea /src/components/UserProfile.tsx que renderiza nombre, email
    y avatar del usuario usando el hook useUser() de /src/hooks/useUser.ts"
```

### Minimal Viable Context
```
Por cada línea pregúntate: "¿Esto previene un modo de fallo?"
Si no → elimínalo
```

### Agent-First Design
```
- Headers consistentes (# ## ###)
- Jerarquías claras
- Dependencias explícitas
- Código en bloques con lenguaje especificado
```

---

**RECORDATORIO:** Los coding agents fallan por AMBIGÜEDAD, no por complejidad. Sé específico.

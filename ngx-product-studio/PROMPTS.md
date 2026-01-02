# Prompts Probados — Product Studio

> Prompts para documentación técnica y PRDs. La filosofía es "Lethal Specificity" - coding agents fallan por ambigüedad, no complejidad.

---

## 📋 PRDs de Features

### Feature Mobile (GENESIS App)
```
Genera PRD para feature de GENESIS app: [NOMBRE DE FEATURE]

Contexto:
- Plataforma: Mobile (Expo SDK 54, React Native 0.81)
- Pantalla/flujo afectado: [DESCRIPCIÓN]
- Agentes involucrados: [LISTA]
- Prioridad: [Alta/Media/Baja]

Incluir:
1. Overview (qué y por qué)
2. Problem Statement (dolor que resuelve)
3. User Stories (como usuario quiero...)
4. Scope (in/out)
5. UI/UX Spec (pantallas, flujos, estados)
6. Technical Spec (componentes, hooks, APIs)
7. Implementation Tasks (granulares, estimadas)
8. Dependencies
9. Testing Requirements
10. Success Metrics
11. Risks

Usar template: templates/prd/standard-prd.md
Guardar en: outputs/prds/
```

### Feature Web (NGX COACH)
```
Genera PRD para feature de NGX COACH: [NOMBRE]

Contexto:
- Plataforma: Web (Next.js 15)
- Sección afectada: [DESCRIPCIÓN]
- Usuario: Coach humano
- Prioridad: [Alta/Media/Baja]

Enfoque específico:
- Cómo ayuda al coach a gestionar clientes
- Integración con datos de STELLA
- Interacción con NGX ENGINE

Usar template: templates/prd/standard-prd.md
Guardar en: outputs/prds/
```

---

## 🤖 PRDs de Agentes

### Agente ADK/A2A
```
Genera PRD para agente NGX: [NOMBRE_AGENTE]

Framework: Google ADK + A2A Protocol
Deployment: Vertex AI Agent Engine
Modelo base: Gemini 3 Pro / Gemini 2.5 Flash

Incluir:
1. Overview (propósito del agente)
2. Capabilities (qué puede hacer)
3. Agent Definition (system prompt, personalidad)
4. Tools (herramientas que usa)
5. Sub-Agents (si orquesta otros)
6. A2A Configuration (AgentCard, endpoints)
7. Integration NGX (cómo se conecta al ecosistema)
8. Deployment Spec
9. Testing Requirements
10. Monitoring & Logging

Usar template: templates/prd/adk-a2a-prd.md
Guardar en: outputs/prds/
```

### Agente con Agent SDK (Claude)
```
Genera PRD para agente Claude: [NOMBRE]

Framework: Anthropic Agent SDK
Uso: [Interno / Herramienta operativa]

Incluir:
1. Purpose
2. Capabilities
3. Tools (MCP servers, custom tools)
4. Hooks (pre/post processing)
5. Subagents (si aplica)
6. Configuration
7. Testing

Referencia: skill agent-sdk
```

---

## 🔄 PRDs de Workflows

### Workflow n8n
```
Genera PRD para workflow n8n: [NOMBRE]

Trigger: [Webhook / Schedule / Event]
Objetivo: [DESCRIPCIÓN]
Integraciones: [LISTA DE SERVICIOS]

Incluir:
1. Overview
2. Trigger Conditions
3. Flow Steps (nodo por nodo)
4. Data Transformations
5. Error Handling
6. Credentials Required
7. Testing Scenarios

Guardar en: outputs/prds/
```

### Workflow Cloud Functions
```
Genera PRD para Cloud Function: [NOMBRE]

Trigger: [HTTP / Pub/Sub / Schedule]
Runtime: Python 3.11 / Node.js
Objetivo: [DESCRIPCIÓN]

Incluir:
1. Purpose
2. Trigger & Input Schema
3. Processing Logic
4. Output Schema
5. Error Handling
6. Dependencies
7. Deployment Config
```

---

## 📦 Context Files

### CLAUDE.md para Proyecto
```
Genera CLAUDE.md para proyecto: [NOMBRE]

Tipo: [Feature / Agent / Workflow / Bug fix]
Stack: [Mobile / Web / Backend / AI]

Incluir:
1. Quick Reference (lo esencial en 30 seg)
2. Project Structure (paths importantes)
3. Key Files (qué hace cada uno)
4. Commands (cómo correr, testear, deploy)
5. Current Task (qué hacer específicamente)
6. Patterns (convenciones del proyecto)
7. DO NOT (errores a evitar)

Optimizado para Claude Code.
Guardar en: outputs/context/
```

### GEMINI.md para Proyecto
```
Genera GEMINI.md para proyecto: [NOMBRE]

Adaptar CLAUDE.md para Gemini CLI:
- Formato más estructurado
- Menos contexto implícito
- Instrucciones más explícitas

Guardar en: outputs/context/
```

---

## 🎯 Handoff Packages

### Handoff para Tarea Específica
```
Genera handoff package para: [DESCRIPCIÓN DE TAREA]

Coding agent destino: [Claude Code / Gemini CLI / Codex]
Proyecto: [NOMBRE]
Scope: [Específico - solo esta tarea]

Incluir:
1. CONTEXT.md (mínimo viable)
2. TASK.md (qué hacer exactamente)
3. MASTER_PROMPT.md (prompt de inicio)
4. references/ (archivos necesarios)

Principio: Minimal Viable Context - solo lo necesario para esta tarea.
Guardar en: outputs/handoffs/[tarea]-[fecha]/
```

### Handoff para Bug Fix
```
Genera handoff package para bug: [DESCRIPCIÓN]

Incluir:
1. Bug Description (qué falla)
2. Steps to Reproduce
3. Expected vs Actual
4. Relevant Files
5. Suggested Approach
6. Testing Criteria

Guardar en: outputs/handoffs/bugfix-[nombre]-[fecha]/
```

---

## 📐 Especificaciones

### API Endpoint Spec
```
Genera especificación para endpoint: [MÉTODO] [PATH]

Servicio: [NOMBRE_SERVICIO]
Propósito: [DESCRIPCIÓN]

Incluir:
1. Endpoint Definition
2. Request Schema (params, body, headers)
3. Response Schema (success, errors)
4. Authentication
5. Rate Limits
6. Examples
7. Error Codes
```

### Database Schema Spec
```
Genera especificación para tabla/modelo: [NOMBRE]

Database: Supabase PostgreSQL
Contexto: [PARA QUÉ SE USA]

Incluir:
1. Table Definition
2. Columns (tipos, constraints)
3. Relationships
4. Indexes
5. RLS Policies
6. Example Queries
```

---

## 🔍 Análisis

### Requirements Extraction
```
Extrae requisitos de esta conversación/documento: [CONTENIDO]

Categorizar en:
1. Functional Requirements
2. Technical Requirements  
3. Non-Functional Requirements
4. Constraints
5. Assumptions
6. Questions/Gaps

Output: Lista estructurada con prioridades.
```

### Gap Analysis
```
Analiza gaps en este PRD: [NOMBRE/CONTENIDO]

Verificar:
- [ ] Todos los flujos cubiertos
- [ ] Edge cases identificados
- [ ] Dependencias claras
- [ ] Criterios de éxito medibles
- [ ] Riesgos documentados

Output: Lista de gaps + preguntas de clarificación.
```

---

## Cómo Usar Este Archivo

1. **Identificar** tipo de documento necesario
2. **Copiar** prompt apropiado
3. **Personalizar** variables
4. **Ejecutar** con máxima especificidad
5. **Verificar** con checklist de PRD standards
6. **Guardar** en outputs/

---

**FILOSOFÍA DEL WORKSPACE:**

- **Lethal Specificity:** Paths exactos, versiones específicas, comandos completos
- **Minimal Viable Context:** Solo lo que previene un modo de fallo
- **Agent-First Design:** Estructura para parsing de máquina

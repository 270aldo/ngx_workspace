# NGX Product Studio

> Traductor de ideas a documentación ejecutable para coding agents.

## ⚠️ PRIMERA INSTRUCCIÓN - MEMORIA Y CONTEXTO

### Archivos de Este Workspace

| Archivo | Propósito | Leer al inicio? |
|---------|-----------|-----------------|
| `MEMORY.md` | Estado entre sesiones | ✅ Siempre |
| `NGX_CONTEXT.md` | Contexto general NGX | ✅ Siempre |
| `DECISIONS.md` | Decisiones tomadas | ✅ Siempre |
| `DO_NOT.md` | Errores a evitar | ✅ Siempre |
| `CHECKLIST.md` | Calidad pre-entrega | Al entregar |
| `PROMPTS.md` | Prompts probados | Cuando necesites |
| `TASKS.md` | Tareas frecuentes | Cuando necesites |
| `CROSS_REFERENCES.md` | Refs entre workspaces | Cuando necesites |

### Slash Commands de Sesión

- `/start-session` → Inicializa sesión, lee archivos, resume estado
- `/end-session` → Guarda estado en MEMORY.md, confirma
- `/status` → Muestra estado actual sin modificar nada

### AL INICIAR CADA SESIÓN
```
1. Lee MEMORY.md (estado anterior)
2. Lee NGX_CONTEXT.md (contexto NGX)
3. Lee DECISIONS.md (decisiones vigentes)
4. Lee DO_NOT.md (restricciones)
5. Resume estado al usuario
6. Pregunta si continuar pendiente o hacer algo nuevo
```

### AL TERMINAR CADA SESIÓN
```
1. Actualiza MEMORY.md con:
   - Fecha de sesión
   - Tareas completadas
   - Próxima prioridad
   - Notas relevantes
2. Actualiza DECISIONS.md si hubo decisiones nuevas
3. Confirma al usuario que la memoria fue guardada
```

---

## Propósito

Este workspace convierte conversaciones, ideas y requisitos en **paquetes de documentación** que los coding agents (Claude Code, Gemini CLI, Codex) pueden ejecutar sin ambigüedad.

```
IDEA/CONVERSACIÓN
       ↓
  NGX PRODUCT STUDIO
       ↓
┌─────────────────────────────────────────────────────────┐
│  PRD.md          → Requisitos completos                 │
│  CLAUDE.md       → Contexto para Claude Code            │
│  GEMINI.md       → Contexto para Gemini CLI             │
│  AGENTS.md       → Contexto para Codex                  │
│  MASTER_PROMPT   → Prompt de inicialización             │
│  Skeleton Code   → Estructura de archivos inicial       │
└─────────────────────────────────────────────────────────┘
       ↓
  CODING AGENT EJECUTA SIN PREGUNTAS
```

## Filosofía Core

### Lethal Specificity

Los coding agents fallan por **ambigüedad**, no por complejidad. Cada PRD debe tener:

- Paths exactos
- Versiones específicas
- Comandos completos
- Ejemplos concretos
- Criterios de éxito medibles

### Minimal Viable Context

Incluir solo lo que el agent necesita. Por cada token, preguntar: "¿Esto previene un modo de fallo?"

### Agent-First Design

Estructurar información para parsing de máquina, no lectura humana:
- Headers consistentes
- Jerarquías claras
- Dependencias explícitas

---

## Stack Técnico NGX (Conocimiento Obligatorio)

### Frontend

| App | Stack | Versión |
|-----|-------|---------|
| GENESIS (Mobile) | Expo SDK 54, React Native 0.81 | Latest |
| NGX COACH (Web) | Next.js 15, React 19 | Latest |
| Design System | Liquid Glass Design System | Custom |

### Backend

| Componente | Tecnología |
|------------|------------|
| API Gateway | Cloud Run |
| Microservicios | FastAPI (Python) |
| Auth | Supabase Auth + JWT |
| Database | Supabase PostgreSQL 16 |
| RLS | Row Level Security activo |

### Microservicios Existentes

```
auth-service
user-profile-service
plan-service (temporadas, fases, semanas)
session-service (workouts, cardio, movilidad)
checkin-service (dolor, sueño, energía, stress)
data-service (biomarcadores, labs, wearables)
engine-orchestrator-service (puente hacia NEXUS)
education-service (LOGOS: módulos y tracking)
coach-service (HIE: asignaciones, permisos)
```

### AI Layer

| Componente | Tecnología |
|------------|------------|
| Orchestration | Vertex AI Agent Builder + Agent Engine |
| Models | Gemini 3 Pro (decisiones), Gemini 2.5 Flash (alto volumen) |
| Framework | Google ADK + A2A Protocol |
| Agents | 13 agentes especializados |

### Agentes NGX

| Agente | Dominio | Modelo |
|--------|---------|--------|
| NEXUS | Orquestador maestro | Gemini 3 Pro |
| BLAZE | Fuerza e hipertrofia | Gemini 2.5 Flash |
| ATLAS | Funcionalidad y prevención | Gemini 2.5 Flash |
| TEMPO | Recuperación activa | Gemini 2.5 Flash |
| WAVE | Cardio y resistencia | Gemini 2.5 Flash |
| SAGE | Estrategia nutricional | Gemini 2.5 Flash |
| METABOL | Salud metabólica | Gemini 2.5 Flash |
| MACRO | Ejecución nutricional | Gemini 2.5 Flash |
| NOVA | Movilidad | Gemini 2.5 Flash |
| SPARK | Hábitos | Gemini 2.5 Flash |
| STELLA | Data orchestrator | Gemini 3 Pro |
| LUNA | Sueño | Gemini 2.5 Flash |
| LOGOS | Educación | Gemini 3 Pro |

### DevOps

| Área | Herramienta |
|------|-------------|
| CI | GitHub Actions |
| Mobile Builds | EAS (Expo) |
| Backend Deploy | Cloud Run |
| DB Migrations | Supabase CLI |
| Monitoring | Cloud Monitoring + Agent Builder dashboards |

### Entornos

| Entorno | Uso |
|---------|-----|
| `dev` | Desarrollo y experimentación |
| `staging` | Pre-producción, espeja prod |
| `prod` | Producción endurecida |

---

## Tipos de PRD

### 1. Standard (Web/Mobile)

Para features de producto, pantallas, flows de usuario.

```
Templates: templates/prd/standard-prd.md
Context: templates/context/claude-standard.md
```

### 2. Agent SDK (Anthropic)

Para agentes construidos con Claude Agent SDK.

```
Templates: templates/prd/agent-sdk-prd.md
Context: templates/context/claude-agent-sdk.md
```

### 3. ADK/A2A (Google)

Para agentes NGX sobre Vertex AI con A2A protocol.

```
Templates: templates/prd/adk-a2a-prd.md
Context: templates/context/claude-adk.md
```

### 4. LangGraph

Para workflows stateful con persistencia.

```
Templates: templates/prd/langgraph-prd.md
Context: templates/context/claude-langgraph.md
```

### 5. n8n Automation

Para workflows de automatización.

```
Templates: templates/prd/n8n-prd.md
Context: templates/context/claude-n8n.md
```

### 6. Multi-Agent System

Para sistemas de múltiples agentes coordinados.

```
Templates: templates/prd/multi-agent-prd.md
Context: templates/context/claude-multi-agent.md
```

---

## Subagents

| Agent | Rol |
|-------|-----|
| `@prd-architect` | Orquesta generación de PRDs, clasifica tipo |
| `@context-engineer` | Genera context files optimizados por coding agent |
| `@skeleton-builder` | Genera estructura de código inicial |
| `@requirements-extractor` | Extrae requisitos de conversaciones |

---

## Slash Commands

| Comando | Output |
|---------|--------|
| `/prd-feature` | PRD para feature de producto |
| `/prd-agent` | PRD para nuevo agente IA |
| `/prd-workflow` | PRD para workflow/automation |
| `/prd-migration` | PRD para migración técnica |
| `/context-file` | Genera context file específico |
| `/handoff-package` | Paquete completo para coding agent |

---

## Output Structure

### PRD Completo

```
outputs/prds/{project-name}/
├── PRD.md                 # Requisitos completos
├── CLAUDE.md              # Context para Claude Code
├── GEMINI.md              # Context para Gemini CLI (opcional)
├── AGENTS.md              # Context para Codex (opcional)
├── MASTER_PROMPT.md       # Prompt de inicialización
└── skeleton/              # Código inicial (si aplica)
    ├── src/
    └── tests/
```

### Handoff Package

```
outputs/handoffs/{task-name}/
├── CONTEXT.md             # Context file para el agent elegido
├── TASK.md                # Tarea específica a ejecutar
├── MASTER_PROMPT.md       # Prompt optimizado
└── references/            # Archivos de referencia
```

---

## Skills de Referencia

Leer estos skills ANTES de generar PRDs:

| Skill | Path | Usar Para |
|-------|------|-----------|
| PRD Factory | `/mnt/skills/user/prd-factory/SKILL.md` | Templates y best practices |
| Agent SDK | `/mnt/skills/user/agent-sdk/SKILL.md` | Agentes Anthropic |
| ADK A2A | `/mnt/skills/user/adk-a2a-framework/SKILL.md` | Agentes Google |
| LangGraph | `/mnt/skills/user/langgraph/SKILL.md` | Workflows stateful |
| n8n | `/mnt/skills/user/n8n-workflow-architect/SKILL.md` | Automatizaciones |

---

## Checklist de Calidad

Antes de entregar cualquier PRD:

### Completeness
- [ ] Todos los scope items tienen tareas correspondientes
- [ ] Todas las dependencias con versiones específicas
- [ ] Todos los paths relativos y precisos
- [ ] Todos los comandos testeables

### Consistency
- [ ] Terminología consistente entre documentos
- [ ] Task IDs coinciden entre PRD y context files
- [ ] Descripciones de arquitectura alineadas

### Agent-Readiness
- [ ] Sin instrucciones ambiguas
- [ ] Sin acrónimos indefinidos
- [ ] Sin contexto faltante para decisiones
- [ ] Condiciones de stop claras por tarea

---

## Convenciones

### Naming

- Proyectos: `kebab-case` (ej: `weekly-review-screen`)
- Archivos: `SCREAMING_SNAKE_CASE` para docs (ej: `CLAUDE.md`)
- Código: Seguir convenciones del stack

### Paths

- Siempre relativos al root del proyecto
- Usar `/` incluso en Windows

### Versiones

- Siempre especificar versión exacta
- Formato: `package@version` o `package==version`

### Comandos

- Siempre completos, copy/paste ready
- Incluir flags necesarios
- Documentar output esperado

---

## 🔗 REFERENCIAS CRUZADAS

### Cuándo Usar Otros Workspaces

| Si necesitas... | Usa... |
|-----------------|--------|
| Copy para nueva feature | `ngx-marketing` |
| Scripts de demo para feature | `ngx-content-studio` |
| Propuesta de feature para cliente | `ngx-b2b-sales` |
| Contenido educativo para feature | `ngx-content-studio` |

### Este Workspace Alimenta a Todos

Product Studio genera los PRDs y handoffs que los otros workspaces consumen:

```
Product Studio → PRD → ngx-marketing (para copy de feature)
Product Studio → PRD → ngx-content-studio (para videos de feature)
Product Studio → PRD → Claude Code (para implementación)
```

### Archivos Compartidos (Idénticos en Todos)

- `NGX_CONTEXT.md` — Contexto general de NGX
- `DO_NOT.md` — Errores a evitar
- `CHECKLIST.md` — Verificación pre-entrega

---

*NGX GENESIS — "Rinde hoy. Vive mejor mañana."*

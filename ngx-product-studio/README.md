# NGX Product Studio

> Traductor de ideas a documentación ejecutable para coding agents.

## 🎯 Propósito

Convierte conversaciones, ideas y requisitos en **paquetes de documentación** que los coding agents (Claude Code, Gemini CLI, Codex) pueden ejecutar sin ambigüedad.

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

## 🤖 Subagents

| Agent | Rol |
|-------|-----|
| `@prd-architect` | Orquesta generación, clasifica proyectos |
| `@context-engineer` | Genera context files optimizados |
| `@skeleton-builder` | Genera estructura de código inicial |
| `@requirements-extractor` | Extrae requisitos de contexto |

## ⚡ Slash Commands

| Comando | Output |
|---------|--------|
| `/prd-feature` | PRD para feature de producto (UI, pantallas) |
| `/prd-agent` | PRD para agente IA (ADK, Agent SDK, LangGraph) |
| `/prd-workflow` | PRD para workflow/automation (n8n) |
| `/handoff-package` | Paquete optimizado para tarea específica |

## 📦 Tipos de PRD

| Tipo | Template | Uso |
|------|----------|-----|
| **Standard** | standard-prd.md | Features UI, pantallas, flows |
| **ADK/A2A** | adk-a2a-prd.md | Agentes NGX sobre Vertex AI |
| **Agent SDK** | agent-sdk-prd.md | Agentes con Claude |
| **LangGraph** | langgraph-prd.md | Workflows stateful |
| **n8n** | n8n-prd.md | Automatizaciones |

## 📋 Ejemplos de Uso

### Nueva Feature en GENESIS App

```
/prd-feature name="Weekly Review Screen" platform=mobile target=claude

Output:
├── PRD.md              # Specs de la pantalla
├── CLAUDE.md           # Contexto para Claude Code
├── MASTER_PROMPT.md    # "Implementa esta pantalla..."
└── skeleton/           # Código inicial
```

### Nuevo Agente NGX

```
/prd-agent name="COACH" framework=adk type=orchestrator a2a=true

Output:
├── PRD.md              # Requisitos del agente
├── CLAUDE.md           # Contexto de desarrollo
├── skeleton/
│   ├── agent/agent.py  # Skeleton ADK
│   └── a2a/agent_card.json
```

### Workflow de Automatización

```
/prd-workflow name="Lead Qualification" platform=n8n trigger=webhook ai=true

Output:
├── PRD.md              # Lógica del workflow
├── CLAUDE.md           # Contexto
├── skeleton/
│   └── workflow.json   # Skeleton n8n
```

### Handoff a Coding Agent

```
/handoff-package project="GENESIS Mobile" agent=claude task="Implementar onboarding"

Output:
├── CONTEXT.md          # Solo lo necesario
├── TASK.md             # Tarea específica
├── MASTER_PROMPT.md    # Prompt optimizado
```

## 🧰 Stack NGX (Conocimiento Integrado)

El workspace conoce todo el stack técnico:

| Capa | Tecnología |
|------|------------|
| **Mobile** | Expo SDK 54, React Native 0.81 |
| **Web** | Next.js 15, React 19 |
| **Backend** | FastAPI, Cloud Run |
| **Database** | Supabase PostgreSQL 16 |
| **AI** | Vertex AI Agent Engine, Gemini 3/2.5 |
| **Agents** | 13 agentes (NEXUS, BLAZE, SAGE, etc.) |

## 📁 Estructura del Proyecto

```
ngx-product-studio/
├── CLAUDE.md                    # Contexto maestro
├── README.md                    # Este archivo
├── .claude/
│   ├── agents/                  # 4 subagents
│   │   ├── prd-architect.md
│   │   ├── context-engineer.md
│   │   ├── skeleton-builder.md
│   │   └── requirements-extractor.md
│   ├── commands/                # Slash commands
│   │   ├── prd-feature.md
│   │   ├── prd-agent.md
│   │   ├── prd-workflow.md
│   │   └── handoff-package.md
│   └── rules/
│       └── prd-standards.md     # Estándares de calidad
├── templates/
│   ├── prd/                     # Templates de PRD
│   │   ├── standard-prd.md
│   │   └── adk-a2a-prd.md
│   └── context/                 # Templates de context files
│       ├── claude-context.md
│       └── master-prompt.md
├── references/                  # Documentación de referencia
└── outputs/
    ├── prds/                    # PRDs generados
    └── handoffs/                # Handoff packages
```

## 🎨 Filosofía de Diseño

### Lethal Specificity

Los coding agents fallan por **ambigüedad**, no por complejidad.

```
❌ "Implementa autenticación"
✅ "Implementa Supabase Auth con magic links. El usuario recibe email, 
    hace click, es redirigido a /auth/callback que intercambia el token."
```

### Minimal Viable Context

Por cada token, pregunta: "¿Esto previene un modo de fallo?"

### Agent-First Design

Estructura para parsing de máquina, no lectura humana.

## 🔗 Skills de Referencia

Este workspace integra conocimiento de:

- **prd-factory** — Templates y best practices
- **agent-sdk** — Anthropic Agent SDK
- **adk-a2a-framework** — Google ADK y A2A
- **langgraph** — Workflows stateful
- **n8n-workflow-architect** — Automatizaciones

## 📊 Valor del Workspace

| Sin Product Studio | Con Product Studio |
|--------------------|--------------------|
| Explicas contexto cada vez | Contexto pre-cargado |
| PRDs inconsistentes | PRDs estructurados |
| Coding agents piden clarificaciones | Ejecutan directo |
| 30 min explicando | 5 min revisando |
| Resultados variables | Resultados consistentes |

---

**NGX GENESIS** — *Rinde hoy. Vive mejor mañana.*

# /prd-agent

Genera un PRD completo para un agente de IA (Agent SDK, ADK, o custom).

## Uso

```
/prd-agent name="COACH" framework=adk type=orchestrator
```

## Parámetros

| Parámetro | Requerido | Opciones | Default | Descripción |
|-----------|-----------|----------|---------|-------------|
| `name` | ✅ | Texto | - | Nombre del agente |
| `framework` | ✅ | adk/agent-sdk/langgraph | - | Framework a usar |
| `type` | ❌ | specialist/orchestrator/workflow | specialist | Tipo de agente |
| `model` | ❌ | gemini-3-pro/gemini-2.5-flash/claude-sonnet | auto | Modelo base |
| `a2a` | ❌ | true/false | false | Incluir A2A Agent Card |
| `target` | ❌ | claude/gemini | claude | Coding agent target |

## Frameworks

### ADK (Google)

Para agentes NGX que corren en Vertex AI Agent Engine.

```
/prd-agent name="BLAZE" framework=adk type=specialist model=gemini-2.5-flash
```

Output incluye:
- Agent definition con ADK
- Custom tools
- A2A Agent Card (si a2a=true)
- Deploy commands para Agent Engine

### Agent SDK (Anthropic)

Para agentes que usan Claude como base.

```
/prd-agent name="VoiceQualifier" framework=agent-sdk type=specialist
```

Output incluye:
- ClaudeAgentOptions configuration
- Custom tools via MCP
- Hooks para logging/security
- Subagent patterns (si orchestrator)

### LangGraph

Para workflows stateful con persistencia.

```
/prd-agent name="LeadNurture" framework=langgraph type=workflow
```

Output incluye:
- State definition
- Graph structure
- Node implementations
- Persistence config

## Ejemplos

### Nuevo agente NGX (ADK)
```
/prd-agent name="COACH" framework=adk type=orchestrator model=gemini-3-pro a2a=true

Output:
├── PRD.md
├── CLAUDE.md
├── MASTER_PROMPT.md
├── skeleton/
│   ├── agent/
│   │   └── agent.py
│   ├── tools/
│   │   └── client_tools.py
│   └── a2a/
│       └── agent_card.json
```

### Voice agent con Agent SDK
```
/prd-agent name="HotLeadAgent" framework=agent-sdk type=specialist

Output:
├── PRD.md
├── CLAUDE.md
├── MASTER_PROMPT.md
├── skeleton/
│   ├── src/
│   │   ├── agent.py
│   │   └── tools/
│   └── tests/
```

### Workflow de onboarding
```
/prd-agent name="OnboardingFlow" framework=langgraph type=workflow

Output:
├── PRD.md
├── CLAUDE.md
├── MASTER_PROMPT.md
├── skeleton/
│   ├── src/
│   │   ├── graph.py
│   │   ├── state.py
│   │   └── nodes/
│   └── tests/
```

## PRD Sections (Agent)

1. **Overview** — Nombre, framework, tipo, modelo
2. **Purpose** — Qué hace el agente, para quién
3. **Capabilities** — Qué puede hacer
4. **Limitations** — Qué NO puede hacer
5. **Tools** — Herramientas disponibles
6. **Instructions** — System prompt del agente
7. **Integration** — Cómo se integra con el sistema
8. **A2A Configuration** — Si es A2A-enabled
9. **Deployment** — Cómo deployar
10. **Testing** — Cómo probar el agente
11. **Monitoring** — Métricas y observability

## Agent Types

### Specialist

Agente enfocado en un dominio específico.

```python
Agent(
    name="BLAZE",
    model="gemini-2.5-flash",
    instruction="Expert en entrenamiento de fuerza...",
    tools=[workout_generator, exercise_lookup]
)
```

### Orchestrator

Agente que coordina otros agentes.

```python
Agent(
    name="NEXUS",
    model="gemini-3-pro",
    instruction="Orquestador maestro que delega...",
    sub_agents=[blaze, sage, logos],
    tools=[user_context, decision_logger]
)
```

### Workflow

Agente con estado persistente y control flow.

```python
graph = StateGraph(State)
graph.add_node("intake", intake_node)
graph.add_node("process", process_node)
graph.add_conditional_edges(...)
```

## Notas

- Para agentes NGX existentes, el PRD documenta mejoras/cambios
- Para nuevos agentes, incluye integration points con NEXUS
- El skeleton incluye tests básicos
- A2A Agent Cards siguen el schema v1.0

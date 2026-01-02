# /prd-workflow

Genera un PRD completo para un workflow de automatización (n8n, integrations, pipelines).

## Uso

```
/prd-workflow name="Lead Qualification" platform=n8n trigger=webhook
```

## Parámetros

| Parámetro | Requerido | Opciones | Default | Descripción |
|-----------|-----------|----------|---------|-------------|
| `name` | ✅ | Texto | - | Nombre del workflow |
| `platform` | ✅ | n8n/cloud-functions/custom | - | Plataforma de ejecución |
| `trigger` | ❌ | webhook/schedule/event/manual | webhook | Cómo se dispara |
| `ai` | ❌ | true/false | false | Si incluye AI agents |
| `target` | ❌ | claude/gemini | claude | Coding agent target |

## Ejemplos

### Workflow n8n con webhook
```
/prd-workflow name="Lead Qualification" platform=n8n trigger=webhook ai=true

Output:
├── PRD.md
├── CLAUDE.md
├── MASTER_PROMPT.md
├── skeleton/
│   ├── workflow.json
│   ├── credentials.md
│   └── scripts/
│       └── test_webhook.sh
```

### Pipeline de procesamiento scheduled
```
/prd-workflow name="Daily Metrics Sync" platform=n8n trigger=schedule

Output:
├── PRD.md
├── CLAUDE.md
├── MASTER_PROMPT.md
├── skeleton/
│   └── workflow.json
```

### Workflow con AI agent integrado
```
/prd-workflow name="Support Ticket Router" platform=n8n trigger=webhook ai=true

Output incluye:
- Workflow JSON con AI Agent node
- Configuración de LangChain nodes
- Memory setup
- Tool configurations
```

## PRD Sections (Workflow)

1. **Overview** — Nombre, plataforma, trigger
2. **Purpose** — Qué automatiza, por qué
3. **Trigger Configuration** — Cómo se dispara
4. **Workflow Steps** — Paso a paso
5. **Data Flow** — Qué datos fluyen
6. **Integrations** — Servicios conectados
7. **AI Integration** — Si usa agentes IA
8. **Error Handling** — Qué pasa si falla
9. **Credentials** — Qué credenciales necesita
10. **Testing** — Cómo probar
11. **Monitoring** — Cómo monitorear

## Workflow Patterns

### Webhook Processing
```
Webhook → Validate → Transform → Action → Response
```

### Scheduled Task
```
Schedule → Fetch → Process → Output → Log
```

### AI Agent Pipeline
```
Trigger → AI Agent → [Tools] → Response
              ↓
           Memory
```

### Multi-Step Approval
```
Request → Validate → [Human Approval] → Execute → Notify
```

### Data Sync
```
Schedule → Fetch Source → Transform → Upsert Target → Log
```

## n8n Specifics

### Nodes Comunes

| Node | Uso |
|------|-----|
| Webhook | Entry point HTTP |
| Code | Transformaciones custom |
| HTTP Request | Llamadas a APIs |
| AI Agent | Integración LangChain |
| Supabase | CRUD a la DB |
| Slack/Email | Notificaciones |
| IF/Switch | Branching logic |

### Data Access Patterns

```javascript
// Webhook data
const data = $input.first().json.body;

// Previous node data
const items = $input.all();

// Environment variables
const apiKey = $env.API_KEY;
```

### Output Format

```javascript
return [{
  json: {
    success: true,
    data: processedData
  }
}];
```

## AI Agent Configuration

Si `ai=true`, incluye:

```javascript
// AI Agent node config
{
  type: "n8n-nodes-langchain.agent",
  parameters: {
    agent: "conversationalAgent",
    text: "={{$json.body.message}}"
  }
}

// Connected nodes
// - Language Model (OpenAI/Anthropic)
// - Tools (HTTP, Supabase, custom)
// - Memory (Buffer/Postgres)
```

## Notas

- Los workflows n8n se exportan como JSON importable
- Las credenciales se documentan pero no se incluyen valores
- Si ai=true, se configura el AI Agent node con best practices
- Se incluyen scripts de test para webhooks

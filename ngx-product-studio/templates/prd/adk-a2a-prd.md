# {AGENT_NAME} Agent

> {One-liner description of the agent's purpose}

## Overview

| Field | Value |
|-------|-------|
| **Name** | {agent_name} |
| **Type** | {Specialist/Orchestrator} |
| **Framework** | Google ADK |
| **Model** | {gemini-3-pro-preview/gemini-2.5-flash} |
| **A2A Enabled** | {Yes/No} |
| **Status** | Draft |
| **Target Agent** | Claude Code |
| **Created** | {date} |

---

## Purpose

### What This Agent Does

{Describe the agent's primary function and capabilities}

### Who Uses This Agent

{Describe the users/systems that interact with this agent}

### Why This Agent Exists

{Business/technical justification for this agent}

---

## Capabilities

### Can Do

- {Capability 1}
- {Capability 2}
- {Capability 3}

### Cannot Do (Limitations)

- {Limitation 1}
- {Limitation 2}

### Safety Boundaries

- ❌ No medical diagnoses
- ❌ No extreme protocols
- ❌ {Other safety rule}

---

## Agent Definition

### Core Configuration

```python
from google.adk.agents import Agent

{agent_name_lower} = Agent(
    name="{agent_name_lower}",
    model="gemini-2.5-flash",  # or gemini-3-pro-preview for complex reasoning
    instruction="""{AGENT_INSTRUCTION}
    
    You are {agent_name}, a specialized agent for {domain}.
    
    Your responsibilities:
    - {responsibility 1}
    - {responsibility 2}
    
    Guidelines:
    - {guideline 1}
    - {guideline 2}
    
    You have access to the following tools:
    - {tool 1}: {description}
    - {tool 2}: {description}
    """,
    tools=[
        {tool_1},
        {tool_2},
    ],
    # sub_agents=[...] if orchestrator
)
```

### Agent Type Details

#### If Specialist

```python
# Single-domain expert
Agent(
    name="{name}",
    model="gemini-2.5-flash",  # Cost-efficient for domain tasks
    instruction="...",
    tools=[domain_specific_tools],
)
```

#### If Orchestrator

```python
# Coordinates multiple specialists
Agent(
    name="{name}",
    model="gemini-3-pro-preview",  # Better reasoning for orchestration
    instruction="...",
    sub_agents=[specialist_1, specialist_2, ...],
    tools=[orchestration_tools],
)
```

---

## Tools

### Required Tools

| Tool | Type | Purpose |
|------|------|---------|
| {tool_name} | {Built-in/Custom} | {what it does} |

### Tool Implementations

#### {Tool Name}

```python
from google.adk.tools import Tool

@Tool(description="{description for the LLM}")
def {tool_name}({params}) -> {return_type}:
    """
    {Detailed description}
    
    Args:
        {param}: {description}
    
    Returns:
        {description of return value}
    """
    # Implementation
    {implementation}
    return {result}
```

### Built-in Tools Used

| Tool | Import | Purpose |
|------|--------|---------|
| `google_search` | `from google.adk.tools import google_search` | Web search |
| `code_interpreter` | `from google.adk.tools import code_interpreter` | Execute code |

---

## Sub-Agents (If Orchestrator)

### Agent Registry

| Agent | Role | Model | When to Delegate |
|-------|------|-------|------------------|
| {sub_agent} | {role} | {model} | {trigger condition} |

### Delegation Logic

```python
instruction = """
When to delegate to sub-agents:

- {SubAgent1}: Use when {condition}
- {SubAgent2}: Use when {condition}

Orchestration rules:
- {rule 1}
- {rule 2}
"""
```

---

## A2A Configuration (If Enabled)

### Agent Card

```json
{
  "$schema": "https://a2a-protocol.org/schemas/agent-card/v1.json",
  "name": "{agent_name}",
  "description": "{description}",
  "version": "1.0.0",
  "provider": {
    "name": "NGX GENESIS",
    "url": "https://ngxgenesis.com"
  },
  "capabilities": {
    "streaming": true,
    "tools": true,
    "multimodal": false
  },
  "skills": [
    {
      "name": "{skill_name}",
      "description": "{skill_description}",
      "inputSchema": {
        "type": "object",
        "properties": {
          "{param}": {"type": "string", "description": "{desc}"}
        }
      }
    }
  ],
  "endpoints": {
    "chat": "/v1/chat",
    "health": "/health"
  },
  "authentication": {
    "type": "bearer",
    "instructions": "Use NGX API key"
  }
}
```

### A2A Server Setup

```python
from google.adk.a2a import A2AServer

server = A2AServer(
    agent={agent_name_lower},
    port=8080,
    agent_card_path="./agent_card.json"
)

# Run
server.run()
```

---

## Integration with NGX

### With NEXUS (Orchestrator)

```python
# In NEXUS definition
from agents.{agent_name_lower} import {agent_name_lower}

nexus = Agent(
    name="nexus",
    model="gemini-3-pro-preview",
    sub_agents=[
        {agent_name_lower},
        # other agents...
    ],
)
```

### With Backend Services

```python
# Tool that calls NGX backend
@Tool(description="Get user data from NGX backend")
async def get_user_context(user_id: str) -> dict:
    async with httpx.AsyncClient() as client:
        response = await client.get(
            f"{NGX_BACKEND_URL}/v1/users/{user_id}/context",
            headers={"Authorization": f"Bearer {JWT}"}
        )
        return response.json()
```

### With Supabase

```python
from supabase import create_client

supabase = create_client(SUPABASE_URL, SUPABASE_KEY)

@Tool(description="Store agent decision")
async def log_decision(user_id: str, decision: dict) -> bool:
    result = supabase.table("agent_decisions").insert({
        "user_id": user_id,
        "agent": "{agent_name}",
        "decision": decision,
    }).execute()
    return bool(result.data)
```

---

## Deployment

### To Agent Engine

```bash
# Deploy to Vertex AI Agent Engine
adk deploy agent_engine \
  --project=ngx-genesis-prod \
  --region=us-central1 \
  --agent-name={agent_name_lower} \
  ./agent

# Verify deployment
adk agents list --project=ngx-genesis-prod
```

### To Cloud Run (Alternative)

```bash
# Build container
adk build --output=docker ./agent

# Deploy to Cloud Run
gcloud run deploy {agent_name_lower} \
  --image=gcr.io/ngx-genesis-prod/{agent_name_lower} \
  --region=us-central1 \
  --allow-unauthenticated=false
```

### Environment Variables

| Variable | Purpose | Source |
|----------|---------|--------|
| `GOOGLE_CLOUD_PROJECT` | GCP Project ID | Secret Manager |
| `SUPABASE_URL` | Supabase endpoint | Secret Manager |
| `SUPABASE_KEY` | Supabase service key | Secret Manager |

---

## Testing

### Unit Tests

```python
# test_agent.py
import pytest
from agent import {agent_name_lower}

@pytest.mark.asyncio
async def test_basic_response():
    response = await {agent_name_lower}.invoke({
        "messages": [{"role": "user", "content": "Hello"}]
    })
    assert response is not None

@pytest.mark.asyncio
async def test_tool_use():
    response = await {agent_name_lower}.invoke({
        "messages": [{"role": "user", "content": "{trigger tool use}"}]
    })
    assert "tool_calls" in response or "result" in response
```

### Integration Tests

```python
@pytest.mark.asyncio
async def test_with_nexus():
    # Test agent as sub-agent of NEXUS
    pass

@pytest.mark.asyncio
async def test_supabase_integration():
    # Test Supabase tool
    pass
```

### Manual Testing

```bash
# Run locally
adk run ./agent

# Test via CLI
adk chat ./agent

# Test via web UI
adk web ./agent
```

---

## Monitoring

### Metrics to Track

| Metric | Description | Alert Threshold |
|--------|-------------|-----------------|
| Latency | Response time | > 5s |
| Error Rate | Failed invocations | > 5% |
| Token Usage | Tokens per request | > 10k |
| Tool Calls | Tool invocations per request | > 10 |

### Logging

```python
import logging

logging.basicConfig(level=logging.INFO)
logger = logging.getLogger("{agent_name}")

# Log tool calls
@Tool(description="...")
def my_tool(param: str) -> str:
    logger.info(f"Tool called with: {param}")
    result = do_something(param)
    logger.info(f"Tool result: {result}")
    return result
```

### Dashboards

- Agent Builder Dashboard: Latency, errors, tool calls
- Cloud Monitoring: Custom metrics
- Supabase Dashboard: Database queries

---

## Implementation Tasks

### Phase 1: Core Agent

| Task ID | Description | Acceptance Criteria |
|---------|-------------|---------------------|
| T1.1 | Create agent definition | Agent responds to basic queries |
| T1.2 | Implement tools | Tools execute correctly |
| T1.3 | Write unit tests | >80% coverage |

### Phase 2: Integration

| Task ID | Description | Acceptance Criteria |
|---------|-------------|---------------------|
| T2.1 | Integrate with NEXUS | NEXUS can delegate to agent |
| T2.2 | Add Supabase tools | Data persists correctly |
| T2.3 | Add A2A support | Agent Card valid |

### Phase 3: Deployment

| Task ID | Description | Acceptance Criteria |
|---------|-------------|---------------------|
| T3.1 | Deploy to staging | Agent accessible via API |
| T3.2 | Set up monitoring | Dashboards show metrics |
| T3.3 | Deploy to production | Agent live |

---

## Dependencies

```txt
# requirements.txt
google-adk>=1.21.0
google-cloud-aiplatform>=1.40.0
supabase>=2.0.0
httpx>=0.25.0
pytest>=7.0.0
pytest-asyncio>=0.21.0
```

---

## Risks & Mitigations

| Risk | Mitigation |
|------|------------|
| Model hallucination | Implement tool-grounded responses |
| High latency | Use gemini-2.5-flash for simple tasks |
| Cost overrun | Set token limits, monitor usage |
| Safety violations | Implement Model Armor policies |

---

## Open Questions

- [ ] {Question that needs answering}

---

## Appendix

### Example Conversations

**User**: {example input}
**Agent**: {expected output}

### Related Agents

| Agent | Relationship |
|-------|--------------|
| NEXUS | Orchestrator (parent) |
| {other} | {relationship} |

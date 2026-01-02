# /prd-feature

Genera un PRD completo para un feature de producto (UI, pantalla, flow).

## Uso

```
/prd-feature name="Weekly Review Screen" platform=mobile target=claude
```

## Parámetros

| Parámetro | Requerido | Opciones | Default | Descripción |
|-----------|-----------|----------|---------|-------------|
| `name` | ✅ | Texto | - | Nombre del feature |
| `platform` | ✅ | mobile/web/both | - | Plataforma target |
| `target` | ❌ | claude/gemini/codex/all | claude | Coding agent target |
| `priority` | ❌ | p0/p1/p2 | p1 | Prioridad del feature |
| `skeleton` | ❌ | true/false | true | Generar código inicial |

## Ejemplos

### Feature móvil para Claude Code
```
/prd-feature name="Onboarding Flow" platform=mobile target=claude priority=p0
```

### Feature web para múltiples agents
```
/prd-feature name="Client Dashboard" platform=web target=all
```

### Feature sin skeleton
```
/prd-feature name="Settings Screen" platform=mobile skeleton=false
```

## Output

```
outputs/prds/{feature-name}/
├── PRD.md                 # Requisitos completos
├── CLAUDE.md              # Context para Claude Code
├── GEMINI.md              # Context para Gemini CLI (si target=all)
├── AGENTS.md              # Context para Codex (si target=all)
├── MASTER_PROMPT.md       # Prompt de inicialización
└── skeleton/              # Código inicial (si skeleton=true)
    ├── components/
    ├── hooks/
    ├── services/
    └── __tests__/
```

## PRD Sections Incluidas

1. **Overview** — Nombre, tipo, status, target
2. **Problem Statement** — Qué problema resuelve
3. **Solution** — Cómo lo resuelve
4. **User Stories** — Como [usuario], quiero [acción], para [beneficio]
5. **Scope** — In-scope, out-of-scope
6. **UI/UX Specification** — Wireframes, flows, estados
7. **Technical Specification** — Arquitectura, data model, APIs
8. **Implementation Tasks** — Tasks con acceptance criteria
9. **Dependencies** — Packages con versiones
10. **Testing Strategy** — Unit, integration, E2E
11. **Success Metrics** — Cómo medir éxito
12. **Risks** — Riesgos y mitigaciones

## Proceso

1. **Clasificación** — Identifica tipo de feature
2. **Extracción** — Extrae requisitos de contexto
3. **Gap Analysis** — Pregunta si falta info crítica
4. **Generación PRD** — Crea documento completo
5. **Context Files** — Genera para target agent(s)
6. **Master Prompt** — Crea prompt optimizado
7. **Skeleton** — Genera código inicial (si aplica)

## Integración con Stack NGX

El PRD incluirá automáticamente:

**Para Mobile (GENESIS)**
- Expo SDK 54 patterns
- React Native 0.81 components
- Supabase integration
- Navigation patterns

**Para Web (NGX COACH)**
- Next.js 15 App Router
- React 19 patterns
- Supabase + RLS
- Auth patterns

## Notas

- Si el feature requiere backend, se incluyen endpoints en el PRD
- Si interactúa con agentes IA, se documenta la integración
- El skeleton sigue los patterns existentes de NGX

# /handoff-package

Genera un paquete optimizado para entregar una tarea específica a un coding agent.

## Uso

```
/handoff-package project="GENESIS Mobile" agent=claude task="Implementar pantalla de onboarding"
```

## Parámetros

| Parámetro | Requerido | Opciones | Default | Descripción |
|-----------|-----------|----------|---------|-------------|
| `project` | ✅ | Texto | - | Proyecto donde trabajar |
| `agent` | ✅ | claude/gemini/codex | - | Coding agent target |
| `task` | ✅ | Texto | - | Descripción de la tarea |
| `context` | ❌ | minimal/standard/full | standard | Nivel de contexto |
| `references` | ❌ | Paths | - | Archivos de referencia |

## Diferencia vs PRD

| PRD | Handoff Package |
|-----|-----------------|
| Documento completo de producto | Paquete para tarea específica |
| Para planificación | Para ejecución inmediata |
| Múltiples tasks | Una sola task |
| Requiere análisis | Listo para ejecutar |

## Output

```
outputs/handoffs/{task-slug}/
├── CONTEXT.md             # Context file optimizado
├── TASK.md                # Tarea específica con criterios
├── MASTER_PROMPT.md       # Prompt de inicialización
└── references/            # Archivos de referencia copiados
```

## Ejemplos

### Handoff a Claude Code
```
/handoff-package project="GENESIS Mobile" agent=claude task="Implementar weekly review screen" context=standard

Output:
├── CONTEXT.md
│   └── Stack NGX, patterns, estructura
├── TASK.md
│   └── Tarea específica, acceptance criteria
├── MASTER_PROMPT.md
│   └── "Implementa la pantalla de weekly review..."
└── references/
    └── existing-screens/  # Ejemplos de pantallas existentes
```

### Handoff con referencias específicas
```
/handoff-package project="NGX COACH" agent=claude task="Añadir filtros al client dashboard" references="/path/to/dashboard.tsx,/path/to/types.ts"
```

### Handoff minimalista
```
/handoff-package project="Backend" agent=gemini task="Crear endpoint de check-in" context=minimal
```

## CONTEXT.md Structure

```markdown
# {PROJECT} Context

## Quick Reference

| Item | Value |
|------|-------|
| Project | {project} |
| Stack | {tech stack} |
| Entry Point | {main file} |

## Project Structure

```
{relevant structure only}
```

## Relevant Files

| File | Purpose |
|------|---------|
| {file} | {why relevant to this task} |

## Patterns to Follow

{Only patterns relevant to the task}

## Dependencies

{Only deps relevant to the task}

## Do NOT

{Task-specific things to avoid}
```

## TASK.md Structure

```markdown
# Task: {TASK_NAME}

## Objective

{Qué lograr en una oración}

## Context

{Por qué esta tarea existe, qué problema resuelve}

## Requirements

### Must Do
- [ ] {requisito obligatorio}

### Should Do
- [ ] {requisito importante}

### Nice to Have
- [ ] {requisito opcional}

## Files to Create/Modify

| File | Action | Changes |
|------|--------|---------|
| {path} | Create/Modify | {qué hacer} |

## Step-by-Step Guide

1. {paso específico}
2. {paso específico}
3. {paso específico}

## Acceptance Criteria

- [ ] {criterio medible y verificable}
- [ ] {criterio medible y verificable}

## Validation

```bash
# Comando para verificar
{test command}

# Output esperado
{expected output}
```

## Common Pitfalls

- {error común}: {cómo evitar}

## Reference Examples

Ver `references/` para ejemplos de:
- {qué hay en references}
```

## MASTER_PROMPT.md Structure

```markdown
# Master Prompt

## Initialization

```
Eres un coding agent trabajando en {PROJECT}.

Tu tarea es: {TASK}

## Context
{brief context}

## Requirements
{requirements list}

## Validation
Cuando termines, verifica:
{acceptance criteria}

## Start
Comienza por {first step}.
```

## Follow-up Prompts

### Si encuentra blocker
```
{qué hacer si hay un problema}
```

### Al completar
```
{qué reportar al terminar}
```
```

## Context Levels

### Minimal

Solo lo esencial para la tarea.

```markdown
- Stack: {tech}
- Files: {relevant files only}
- Task: {task}
```

### Standard (Default)

Contexto balanceado.

```markdown
- Stack completo
- Estructura del proyecto
- Patterns relevantes
- Files relevantes
- Task con steps
```

### Full

Todo el contexto disponible.

```markdown
- Stack completo
- Estructura completa
- Todos los patterns
- Dependencias completas
- Historia/decisiones
- Task con steps detallados
```

## Best Practices

### Para Claude Code

- Incluir paths explícitos
- Comandos bash completos
- Ejemplos de código existente
- Test commands

### Para Gemini CLI

- Similar a Claude
- Referencias a GCP si aplica

### Para Codex

- Muy estructurado
- Tasks numeradas
- Menos prosa

## Notas

- El handoff es para **una tarea específica**, no un proyecto completo
- Se copia solo el contexto **relevante** para esa tarea
- El master prompt está optimizado para **ejecución inmediata**
- Las references se copian al directorio de output

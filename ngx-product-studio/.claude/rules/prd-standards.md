# PRD Quality Standards

Estándares obligatorios para toda documentación generada en NGX Product Studio.

---

## 🎯 Principios Core

### 1. Lethal Specificity

Los coding agents fallan por **ambigüedad**, no por complejidad.

```
❌ VAGO
"Implementa autenticación con Supabase"

✅ ESPECÍFICO
"Implementa autenticación con Supabase Auth:
1. Magic links (no passwords)
2. El flujo es: LoginScreen → signInWithOtp → email → deep link → /auth/callback
3. Session se guarda en AsyncStorage con key 'supabase-session'
4. Usar el hook useAuth() existente en /hooks/useAuth.ts"
```

### 2. Minimal Viable Context

Por cada token, pregunta: "¿Esto previene un modo de fallo?"

```
❌ EXCESO
[3 páginas de historia del proyecto]

✅ MÍNIMO
"Stack: Expo SDK 54 + Supabase. Entry: apps/genesis/. Test: npm test"
```

### 3. Agent-First Design

Estructura para parsing de máquina, no lectura humana.

```
❌ PROSA
"Deberías empezar por crear el componente y luego..."

✅ ESTRUCTURADO
Task 1: Create component
Files: src/components/MyComponent.tsx
Steps:
1. Create file
2. Add imports
3. Implement logic
```

---

## 📋 PRD Checklist

### Completeness

- [ ] Todos los scope items tienen tareas correspondientes
- [ ] Todas las dependencias tienen versiones específicas
- [ ] Todos los paths son relativos y correctos
- [ ] Todos los comandos son copy/paste ready
- [ ] Todos los acceptance criteria son medibles

### Consistency

- [ ] Terminología consistente entre documentos
- [ ] Task IDs coinciden en PRD y context files
- [ ] Descripciones de arquitectura alineadas
- [ ] Patterns referenciados existen

### Agent-Readiness

- [ ] Sin instrucciones ambiguas
- [ ] Sin acrónimos indefinidos
- [ ] Sin contexto faltante para decisiones
- [ ] Condiciones de stop claras por tarea
- [ ] Validation steps definidos

---

## 🚫 Anti-Patterns

### En PRDs

| Anti-Pattern | Por Qué Es Malo | Corrección |
|--------------|-----------------|------------|
| "Implementa la UI" | Demasiado vago | Especificar componentes, estados, interacciones |
| "Usa best practices" | No accionable | Especificar qué practices |
| "Similar al otro módulo" | Requiere contexto | Dar path exacto y qué copiar |
| Sin acceptance criteria | No sé cuándo terminar | Agregar criterios medibles |
| Tasks sin dependencias | Orden incorrecto | Especificar qué depende de qué |

### En Context Files

| Anti-Pattern | Corrección |
|--------------|------------|
| Incluir TODO el proyecto | Solo lo relevante a la tarea |
| Comandos incompletos | Incluir flags y paths |
| Patterns sin ejemplos | Agregar código ejemplo |
| Sin DO NOT section | Agregar limitaciones explícitas |

### En Master Prompts

| Anti-Pattern | Corrección |
|--------------|------------|
| Prompt de una línea | Expandir con contexto |
| Sin validation steps | Agregar cómo verificar |
| Sin scope boundaries | Definir qué NO hacer |

---

## 📐 Formato Obligatorio

### Headers

```markdown
# Título Principal

## Sección Mayor

### Subsección

#### Detalle (raramente necesario)
```

### Tasks

```markdown
### Task {N}: {Nombre Descriptivo}

**ID**: T{N}

**Depends on**: {T1, T2, ...} o "None"

**Goal**: {Una oración clara}

**Files**:
| File | Action | Changes |
|------|--------|---------|
| `path/file.ts` | Create/Modify | {qué} |

**Steps**:
1. {Paso específico}
2. {Paso específico}

**Acceptance Criteria**:
- [ ] {Criterio medible}

**Validation**:
```bash
{comando}
# Expected: {output}
```
```

### Code Blocks

```markdown
```typescript
// Siempre incluir language tag
// Siempre incluir comentarios explicativos
const example = "value";
```
```

### Tables

```markdown
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| value | value | value |
```

---

## 🔧 Naming Conventions

### Projects

```
kebab-case
weekly-review-screen
lead-qualification-workflow
blaze-agent
```

### Files (Documentation)

```
SCREAMING_SNAKE_CASE.md
PRD.md
CLAUDE.md
MASTER_PROMPT.md
```

### Directories

```
kebab-case/
weekly-review/
agent-sdk/
```

### Task IDs

```
T{phase}.{number}
T1.1, T1.2, T2.1
```

---

## 📊 Versiones y Dependencies

### Siempre Especificar Versión

```
❌ "Usar React"
✅ "react@19.0.0"

❌ "Instalar Supabase"
✅ "@supabase/supabase-js@2.45.0"
```

### Formato por Ecosistema

```bash
# npm
package@x.y.z

# Python
package==x.y.z

# Go
package v1.2.3
```

---

## 📁 Paths

### Siempre Relativos

```
❌ /Users/aldo/projects/ngx/src/component.tsx
✅ src/component.tsx
✅ apps/genesis/src/component.tsx
```

### Usar Forward Slash

```
❌ apps\genesis\src
✅ apps/genesis/src
```

---

## 🔍 Validation Standards

### Todo Task Necesita Validation

```markdown
**Validation**:
```bash
# Comando para verificar
npm test -- MyComponent

# Expected: All tests passing
```
```

### Tipos de Validation

| Tipo | Cuándo | Ejemplo |
|------|--------|---------|
| Test | Siempre | `npm test` |
| Type check | TypeScript | `npm run typecheck` |
| Lint | Siempre | `npm run lint` |
| Manual | UI changes | "Open app, navigate to X, verify Y" |
| API | Backend | `curl -X GET ...` |

---

## 📝 Writing Style

### Voz Activa

```
❌ "The component should be created"
✅ "Create the component"
```

### Imperativo

```
❌ "You should implement the hook"
✅ "Implement the hook"
```

### Conciso

```
❌ "In order to properly implement this feature, you will need to first..."
✅ "Steps: 1. Create file 2. Add imports 3. Implement"
```

---

## ✅ Pre-Delivery Checklist

Antes de entregar cualquier PRD/context file:

### Structure
- [ ] Tiene todas las secciones requeridas
- [ ] Headers en orden correcto
- [ ] Tables formateadas correctamente
- [ ] Code blocks con language tags

### Content
- [ ] Sin TODOs o placeholders
- [ ] Sin información contradictoria
- [ ] Todos los links/paths verificados
- [ ] Ejemplos son válidos

### Completeness
- [ ] Scope definido (in/out)
- [ ] Dependencies con versiones
- [ ] Tasks con acceptance criteria
- [ ] Validation para cada task

### Quality
- [ ] Sin ambigüedades
- [ ] Sin acrónimos sin definir
- [ ] Lethal specificity aplicada
- [ ] Copy/paste ready

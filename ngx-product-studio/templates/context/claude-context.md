# {PROJECT_NAME}

> {One-liner description}

## Quick Reference

| Item | Value |
|------|-------|
| **Type** | {Standard/Agent/Workflow} |
| **Platform** | {Mobile/Web/Backend/AI} |
| **Stack** | {primary technologies} |
| **Entry Point** | {main file or directory} |
| **Test Command** | `{test command}` |
| **Run Command** | `{dev command}` |

---

## NGX Stack Reference

### Mobile (GENESIS)
- **Framework**: Expo SDK 54, React Native 0.81
- **Entry**: `apps/genesis/`
- **State**: Zustand
- **Navigation**: React Navigation 6
- **Styling**: StyleSheet + Liquid Glass Design System

### Web (NGX COACH)
- **Framework**: Next.js 15, React 19
- **Entry**: `apps/ngx-coach/`
- **State**: Zustand + React Query
- **Styling**: Tailwind + shadcn/ui

### Backend
- **Framework**: FastAPI (Python)
- **Hosting**: Cloud Run
- **Database**: Supabase PostgreSQL 16
- **Auth**: Supabase Auth + JWT
- **RLS**: Enabled on all tables

### AI Layer
- **Platform**: Vertex AI Agent Engine
- **Models**: Gemini 3 Pro / 2.5 Flash
- **Framework**: Google ADK + A2A Protocol
- **Agents**: 13 specialized (NEXUS, BLAZE, SAGE, etc.)

---

## Project Structure

```
{project}/
├── {dir}/
│   ├── {file}           # {purpose}
│   └── {subdir}/
│       └── {file}       # {purpose}
├── {dir}/
│   └── {file}           # {purpose}
└── {config_files}       # {purpose}
```

---

## Key Files

| File | Purpose | When to Modify |
|------|---------|----------------|
| `{path}` | {description} | {when} |
| `{path}` | {description} | {when} |

---

## Development Commands

```bash
# Install dependencies
{install command}

# Start development server
{dev command}

# Run tests
{test command}

# Run specific test file
{specific test command}

# Build for production
{build command}

# Type check
{typecheck command}

# Lint
{lint command}
```

---

## Implementation Tasks

### Task 1: {Task Name}

**ID**: T1

**Goal**: {What to achieve}

**Files to create/modify**:
| File | Action | Changes |
|------|--------|---------|
| `{path}` | {Create/Modify} | {what to do} |

**Steps**:
1. {Specific step with details}
2. {Specific step with details}
3. {Specific step with details}

**Code Example**:
```{language}
{code example showing expected pattern}
```

**Acceptance Criteria**:
- [ ] {Measurable criterion}
- [ ] {Measurable criterion}

**Validation**:
```bash
# How to verify this task is complete
{validation command}

# Expected output
{expected output}
```

---

### Task 2: {Task Name}

**ID**: T2

**Depends on**: T1

{... same structure as Task 1 ...}

---

## Patterns to Follow

### {Pattern Name}

**When to use**: {situation}

```{language}
// Example implementation
{code example}
```

### {Pattern Name}

**When to use**: {situation}

```{language}
// Example implementation
{code example}
```

---

## Data Models

### {Model Name}

```typescript
interface {ModelName} {
  id: string;
  {field}: {type};
  {field}: {type};
  createdAt: Date;
  updatedAt: Date;
}

type Create{ModelName}Input = Omit<{ModelName}, 'id' | 'createdAt' | 'updatedAt'>;
type Update{ModelName}Input = Partial<Create{ModelName}Input>;
```

### Supabase Schema

```sql
CREATE TABLE {table_name} (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  {field} {TYPE} {constraints},
  created_at TIMESTAMPTZ DEFAULT NOW(),
  updated_at TIMESTAMPTZ DEFAULT NOW()
);

-- RLS Policy
ALTER TABLE {table_name} ENABLE ROW LEVEL SECURITY;

CREATE POLICY "Users can access own data" ON {table_name}
  FOR ALL
  TO authenticated
  USING (auth.uid() = user_id);
```

---

## API Endpoints

### {Endpoint Group}

| Method | Path | Purpose |
|--------|------|---------|
| GET | `/v1/{resource}` | List all |
| GET | `/v1/{resource}/:id` | Get one |
| POST | `/v1/{resource}` | Create |
| PATCH | `/v1/{resource}/:id` | Update |
| DELETE | `/v1/{resource}/:id` | Delete |

**Request/Response Examples**:

```bash
# Create
curl -X POST {base_url}/v1/{resource} \
  -H "Authorization: Bearer $TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "{field}": "{value}"
  }'

# Response
{
  "data": {
    "id": "uuid",
    "{field}": "{value}"
  },
  "meta": {}
}
```

---

## Dependencies

### Install Command

```bash
# All dependencies
{install all command}
```

### Key Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| {package} | {x.y.z} | {why needed} |

---

## Testing

### Test Structure

```
__tests__/
├── unit/
│   └── {component}.test.{ts|tsx}
├── integration/
│   └── {flow}.test.{ts|tsx}
└── e2e/
    └── {scenario}.test.{ts|tsx}
```

### Running Tests

```bash
# All tests
{test all command}

# With coverage
{test coverage command}

# Watch mode
{test watch command}
```

### Test Patterns

```{language}
// Unit test example
describe('{Component}', () => {
  it('should {expected behavior}', () => {
    // Arrange
    {setup}
    
    // Act
    {action}
    
    // Assert
    {assertion}
  });
});
```

---

## Common Issues

### {Issue Title}

**Symptom**: {what you see}

**Cause**: {why it happens}

**Solution**:
```bash
{fix command or code}
```

### {Issue Title}

**Symptom**: {what you see}

**Solution**:
```bash
{fix command or code}
```

---

## Environment Variables

| Variable | Purpose | Where to Set |
|----------|---------|--------------|
| `{VAR_NAME}` | {purpose} | `.env.local` |

```bash
# .env.local
{VAR_NAME}={value}
```

---

## DO NOT

- ❌ {Thing to avoid}
- ❌ {Thing to avoid}
- ❌ {Thing to avoid}
- ❌ Modify files outside the scope of tasks
- ❌ Skip tests
- ❌ Ignore TypeScript errors
- ❌ Use `any` type without justification

---

## Completion Checklist

Before marking tasks complete:

- [ ] All acceptance criteria met
- [ ] Tests passing
- [ ] No TypeScript errors
- [ ] No linting errors
- [ ] Code follows existing patterns
- [ ] New files in correct locations

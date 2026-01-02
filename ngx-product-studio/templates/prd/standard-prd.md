# {PROJECT_NAME}

> {One-liner description - max 10 words}

## Overview

| Field | Value |
|-------|-------|
| **Name** | {project_name} |
| **Type** | Standard (UI/Feature) |
| **Platform** | {Mobile/Web/Both} |
| **Status** | Draft |
| **Priority** | {P0/P1/P2} |
| **Target Agent** | {Claude Code/Gemini CLI/Codex} |
| **Created** | {date} |

---

## Problem Statement

### The Problem

{Describe the specific problem this feature solves}

### Who Has This Problem

{Target user segment and their context}

### Current State

{How users currently handle this - the pain}

### Impact

{What happens if we don't solve this}

---

## Solution

### Proposed Solution

{High-level description of what we're building}

### Key Benefits

- {Benefit 1}
- {Benefit 2}
- {Benefit 3}

### Success Definition

{How do we know we've succeeded}

---

## User Stories

### Primary Flow

```
As a {user type}
I want to {action}
So that {benefit}
```

### Secondary Flows

```
As a {user type}
I want to {action}
So that {benefit}
```

---

## Scope

### In-Scope

- [ ] {Feature/functionality 1}
- [ ] {Feature/functionality 2}
- [ ] {Feature/functionality 3}

### Out-of-Scope

| Item | Reason |
|------|--------|
| {item} | {why it's out of scope} |

### Assumptions

- {Assumption about user behavior}
- {Assumption about technical constraints}
- {Assumption about data availability}

---

## UI/UX Specification

### Screens/Views

#### {Screen Name}

**Purpose**: {What this screen does}

**Entry Points**:
- {How user gets here}

**Layout**:
```
┌─────────────────────────────────┐
│           Header                │
├─────────────────────────────────┤
│                                 │
│         Main Content            │
│                                 │
├─────────────────────────────────┤
│         Actions                 │
└─────────────────────────────────┘
```

**Components**:
| Component | Description | States |
|-----------|-------------|--------|
| {name} | {description} | {loading/error/empty/success} |

**Interactions**:
- {Interaction 1}: {behavior}
- {Interaction 2}: {behavior}

### User Flow

```
[Entry] → [Screen 1] → [Action] → [Screen 2] → [Exit]
                ↓
           [Error State]
```

### States

| State | Trigger | Display |
|-------|---------|---------|
| Loading | Initial load | Skeleton/spinner |
| Empty | No data | Empty state message |
| Error | API failure | Error message + retry |
| Success | Data loaded | Content |

---

## Technical Specification

### Architecture

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   Screen    │ ──▶ │    Hook     │ ──▶ │   Service   │
└─────────────┘     └─────────────┘     └─────────────┘
                                              │
                                              ▼
                                        ┌─────────────┐
                                        │  Supabase   │
                                        └─────────────┘
```

### Data Model

#### Tables

```sql
-- {table_name}
CREATE TABLE {table_name} (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  {field} {TYPE} {constraints},
  created_at TIMESTAMPTZ DEFAULT NOW(),
  updated_at TIMESTAMPTZ DEFAULT NOW()
);

-- RLS Policy
ALTER TABLE {table_name} ENABLE ROW LEVEL SECURITY;

CREATE POLICY "{policy_name}" ON {table_name}
  FOR {ALL/SELECT/INSERT/UPDATE/DELETE}
  TO authenticated
  USING (auth.uid() = user_id);
```

#### Types

```typescript
interface {TypeName} {
  id: string;
  {field}: {type};
  createdAt: Date;
  updatedAt: Date;
}
```

### API Endpoints

| Method | Path | Request | Response | Purpose |
|--------|------|---------|----------|---------|
| GET | `/v1/{resource}` | - | `{Type}[]` | List all |
| GET | `/v1/{resource}/:id` | - | `{Type}` | Get one |
| POST | `/v1/{resource}` | `Create{Type}` | `{Type}` | Create |
| PATCH | `/v1/{resource}/:id` | `Update{Type}` | `{Type}` | Update |
| DELETE | `/v1/{resource}/:id` | - | `void` | Delete |

### Integration Points

| System | Purpose | Method |
|--------|---------|--------|
| Supabase Auth | Authentication | JWT validation |
| {Agent} | {purpose} | API call to Agent Engine |

---

## Implementation Tasks

### Phase 1: Foundation

| Task ID | Description | Acceptance Criteria | Estimate |
|---------|-------------|---------------------|----------|
| T1.1 | {Task description} | {Measurable criteria} | {hours} |
| T1.2 | {Task description} | {Measurable criteria} | {hours} |

### Phase 2: Core Features

| Task ID | Description | Acceptance Criteria | Estimate |
|---------|-------------|---------------------|----------|
| T2.1 | {Task description} | {Measurable criteria} | {hours} |
| T2.2 | {Task description} | {Measurable criteria} | {hours} |

### Phase 3: Polish

| Task ID | Description | Acceptance Criteria | Estimate |
|---------|-------------|---------------------|----------|
| T3.1 | {Task description} | {Measurable criteria} | {hours} |

---

## Dependencies

### External Packages

| Package | Version | Purpose |
|---------|---------|---------|
| {package} | {x.y.z} | {why needed} |

### Internal Dependencies

| Module | Purpose |
|--------|---------|
| {module} | {why needed} |

### Service Dependencies

| Service | Purpose | Status |
|---------|---------|--------|
| Supabase | Database | ✅ Existing |
| {service} | {purpose} | {status} |

---

## Testing Strategy

### Unit Tests

| Component | Test Cases |
|-----------|------------|
| {component} | {what to test} |

### Integration Tests

| Flow | Test Cases |
|------|------------|
| {flow} | {what to test} |

### E2E Tests

| Scenario | Steps |
|----------|-------|
| {scenario} | {high-level steps} |

### Test Commands

```bash
# Run unit tests
{test command}

# Run integration tests
{test command}

# Run E2E
{test command}
```

---

## Success Metrics

| Metric | Target | Measurement |
|--------|--------|-------------|
| {metric} | {target value} | {how to measure} |

---

## Risks & Mitigations

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| {risk} | {H/M/L} | {H/M/L} | {how to mitigate} |

---

## Open Questions

- [ ] {Question that needs answering}

---

## Appendix

### References

- {Link to related doc}
- {Link to design}

### Glossary

| Term | Definition |
|------|------------|
| {term} | {definition} |

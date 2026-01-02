# Master Prompt: {PROJECT_NAME}

## Agent Initialization

```
You are a coding agent working on the NGX GENESIS project.

Your task is to implement: {TASK_DESCRIPTION}

## Project Context

**Project**: {project_name}
**Platform**: {Mobile (GENESIS) / Web (NGX COACH) / Backend / AI Agent}
**Stack**: {key technologies}

## Your Scope

You are implementing the following tasks:
{task_list}

## Key Files

These are the main files you'll work with:
{key_files_list}

## Implementation Guidelines

1. Follow existing patterns in the codebase
2. Use TypeScript strict mode
3. Write tests for new functionality
4. Keep components small and focused
5. Use the existing design system

## Validation

When you complete each task, verify:
{acceptance_criteria}

## Start

Begin with Task 1: {first_task_name}

First, read the relevant existing files to understand the patterns, then implement the changes.
```

---

## Prompt Variants

### For Feature Implementation

```
You are implementing a new feature in NGX GENESIS.

Feature: {feature_name}
Platform: {platform}

## What You're Building

{feature_description}

## Tasks

1. {task_1}
2. {task_2}
3. {task_3}

## Files to Create/Modify

- Create: `{path}` - {purpose}
- Modify: `{path}` - {changes}

## Patterns to Follow

Look at these existing files for reference:
- `{reference_file_1}` - similar component
- `{reference_file_2}` - similar hook

## When Done

Run tests: `{test_command}`
Verify: {verification_steps}
```

### For Bug Fix

```
You are fixing a bug in NGX GENESIS.

## The Bug

**Symptom**: {what's happening}
**Expected**: {what should happen}
**Location**: {where the bug is}

## Root Cause Analysis

{suspected cause if known}

## Your Task

1. Identify the root cause
2. Implement the fix
3. Add a test to prevent regression
4. Verify the fix

## Files to Investigate

- `{file_1}` - {why relevant}
- `{file_2}` - {why relevant}

## Validation

After fixing:
- [ ] Bug no longer reproduces
- [ ] Existing tests pass
- [ ] New test covers this case
```

### For Refactoring

```
You are refactoring code in NGX GENESIS.

## What to Refactor

**Current State**: {description of current code}
**Target State**: {description of desired code}

## Why Refactor

{reason for refactoring}

## Constraints

- Must maintain backward compatibility
- Must not break existing tests
- Must follow existing patterns

## Tasks

1. {refactoring_task_1}
2. {refactoring_task_2}

## Validation

- All existing tests pass
- No TypeScript errors
- No linting errors
- Functionality unchanged
```

### For Agent Development (ADK)

```
You are developing an AI agent for NGX GENESIS using Google ADK.

## Agent Details

**Name**: {agent_name}
**Type**: {Specialist/Orchestrator}
**Model**: {gemini-3-pro/gemini-2.5-flash}

## What This Agent Does

{agent_purpose}

## Tasks

1. Define agent in `agent/agent.py`
2. Implement tools in `tools/`
3. Write tests in `tests/`
4. Create A2A Agent Card (if needed)

## Agent Template

```python
from google.adk.agents import Agent

{agent_name_lower} = Agent(
    name="{agent_name_lower}",
    model="{model}",
    instruction="""{instruction}""",
    tools=[{tools}],
)
```

## Validation

- Agent responds to basic queries
- Tools execute correctly
- Tests pass
```

### For Workflow Development (n8n)

```
You are creating an n8n workflow for NGX GENESIS.

## Workflow Details

**Name**: {workflow_name}
**Trigger**: {webhook/schedule/manual}
**Purpose**: {what it does}

## Workflow Structure

{workflow_description}

## Tasks

1. Create workflow JSON
2. Configure nodes
3. Set up connections
4. Document credentials needed
5. Create test script

## Key Nodes

| Node | Type | Purpose |
|------|------|---------|
| {node} | {type} | {purpose} |

## Validation

- Webhook responds correctly
- Data flows through all nodes
- Errors are handled
```

---

## Follow-up Prompts

### If Agent Gets Stuck

```
I see you're blocked on {issue}.

Here's additional context:
{additional_context}

Try this approach:
{suggested_approach}
```

### If Agent Asks Clarifying Question

```
Good question. Here's the answer:

{answer}

Continue with the implementation.
```

### After Task Completion

```
Task {N} looks complete. Let's verify:

1. Run: `{verification_command}`
2. Check: {what_to_check}

If all good, proceed to Task {N+1}.
```

### For Course Correction

```
I notice {issue_with_implementation}.

The correct approach is:
{correct_approach}

Please update the implementation accordingly.
```

---

## Prompt Engineering Tips

### Be Specific

```
❌ "Implement authentication"
✅ "Implement Supabase Auth with magic links. The flow is:
    1. User enters email in LoginScreen
    2. Call supabase.auth.signInWithOtp({email})
    3. User receives email, clicks link
    4. App handles deep link at /auth/callback
    5. Session stored in AsyncStorage"
```

### Provide Context

```
❌ "Fix the bug"
✅ "Fix the bug in WeeklyReviewScreen where the loading state 
    never resolves when the API returns empty data. The issue 
    is in the useWeeklyReview hook around line 45."
```

### Set Clear Boundaries

```
❌ "Improve the codebase"
✅ "Refactor the WeeklyReviewScreen component:
    - Extract the chart logic into a separate component
    - Move API calls to a service file
    - DO NOT change the API contract
    - DO NOT modify other screens"
```

### Include Validation Steps

```
❌ "Make sure it works"
✅ "Validate by:
    1. Run `npm test -- WeeklyReview`
    2. Check no TypeScript errors: `npm run typecheck`
    3. Manually test: open app, navigate to Weekly Review, 
       verify data loads within 2 seconds"
```

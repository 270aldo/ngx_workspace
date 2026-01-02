# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## What Is This Repository

**ngx_workspace** is a collection of 6 specialized Claude Code workspaces for NGX GENESIS operations. Each workspace is a configuration system (not a code repository) that uses Claude Code CLI to generate marketing content, sales materials, PRDs, operational documents, and financial reports.

**NGX GENESIS** is a Performance & Longevity platform with 13 AI agents, targeting professionals aged 30-60.

---

## Workspace Architecture

```
ngx_workspace/
├── ngx-marketing/        # B2C marketing: emails, ads, funnels, HYBRID sales
├── ngx-b2b-sales/        # B2B sales: proposals, pipeline, Founding Coaches
├── ngx-content-studio/   # Multimedia: podcasts, videos, VEO/SORA prompts
├── ngx-product-studio/   # PRDs, technical docs, handoffs for coding agents
├── ngx-operations/       # SOPs, daily checklists, metrics, workflows
└── ngx-finance/          # P&L, projections, invoices, budget tracking
```

Each workspace contains:
- `CLAUDE.md` — Primary instructions (read this first in each workspace)
- `MEMORY.md` — Session persistence between conversations
- `NGX_CONTEXT.md` — Brand context (shared across workspaces)
- `DECISIONS.md` — Documented decisions
- `DO_NOT.md` — Errors to avoid
- `.claude/commands/` — Slash commands
- `.claude/agents/` — Specialized subagents
- `.claude/rules/` — Behavior rules
- `templates/` — Reusable document templates
- `outputs/` — Generated content
- `dashboards/` — Interactive HTML dashboards

---

## How to Work in This Repository

### Session Workflow

Every workspace uses the same session pattern:

```bash
# 1. Navigate to the workspace you need
cd ngx-marketing  # or ngx-b2b-sales, ngx-finance, etc.

# 2. Start Claude Code
claude

# 3. Initialize session (reads MEMORY.md, NGX_CONTEXT.md, DECISIONS.md, DO_NOT.md)
/start-session

# 4. Work using workspace-specific commands
/email-sequence type=welcome lead_magnet=ngx-transform

# 5. End session (saves state to MEMORY.md)
/end-session
```

### Shared Commands (All Workspaces)

| Command | Purpose |
|---------|---------|
| `/start-session` | Initialize session, read context files, resume state |
| `/end-session` | Save state to MEMORY.md, confirm persistence |
| `/status` | Show current workspace state without modifications |

---

## Workspace-Specific Commands

### ngx-marketing
| Command | Purpose |
|---------|---------|
| `/email-sequence` | Generate email sequences for lead magnets |
| `/ad-variations` | Create Meta/Google/LinkedIn ad variations |
| `/audit-funnel` | Audit landing pages and funnels |
| `/hybrid-qualify` | Qualify leads for HYBRID ($199/mo) vs ASCEND ($99/mo) |
| `/hybrid-call-script` | Generate HYBRID closing call scripts |

### ngx-b2b-sales
| Command | Purpose |
|---------|---------|
| `/prospect-research` | Research and qualify B2B prospects |
| `/proposal-create` | Create Founding Coach or gym proposals |
| `/sales-script` | Generate discovery or closing call scripts |
| `/pipeline-report` | Weekly pipeline status report |
| `/email-b2b` | B2B outreach email sequences |

### ngx-content-studio
| Command | Purpose |
|---------|---------|
| `/podcast-episode` | Full podcast episode with NGX agents |
| `/video-package` | Pre-production: storyboard, shot list, VEO/SORA prompts |
| `/content-package` | Multi-format content package |

### ngx-product-studio
| Command | Purpose |
|---------|---------|
| `/prd-feature` | PRD for GENESIS mobile or NGX COACH web features |
| `/prd-agent` | PRD for ADK/A2A agents |
| `/handoff-package` | Context package for coding agents |

### ngx-operations
| Command | Purpose |
|---------|---------|
| `/daily-checklist` | Generate daily MITs and time blocks |
| `/weekly-review` | Weekly review with wins, obstacles, metrics |
| `/sop-create` | Create structured SOPs |

### ngx-finance
| Command | Purpose |
|---------|---------|
| `/monthly-pnl` | P&L with MoM comparison |
| `/runway-calc` | Calculate runway with scenarios |
| `/invoice-create` | Generate invoices |

---

## Brand Voice: "Verdad Directa"

**Formula:** CONFRONTA → FUNDAMENTA → RESUELVE

### Three Communication Modes

| Mode | Name | When to Use | Energy |
|------|------|-------------|--------|
| A | El Experto | Educate, explain "why" | Medium |
| B | La Verdad | Hooks, break myths, capture attention | High |
| C | El Arquitecto | Show the system, convert | Reserved |

### Audience Treatment

- **30-45 years:** TÚ (informal, direct)
- **45-60 years:** USTED (respectful, professional)

### Never Do

- Use PRIME/LONGEVITY archetypes (obsolete)
- Mention "executives/CEOs" as main segment
- Make absolute promises ("100% guaranteed")
- Use more than 1-2 emojis per piece
- Use cyan color (always violet #6D00FF)
- Create false urgency

### Always Do

- Adapt treatment by audience age
- Mention correct agent for each function (BLAZE for training, LUNA for sleep, etc.)
- Explain technical terms when used
- End with a concrete action
- Admit limitations before selling benefits

---

## The 13 NGX Agents

| Agent | Domain |
|-------|--------|
| GENESIS/NEXUS | Master orchestrator |
| BLAZE | Strength training, hypertrophy |
| ATLAS | Mobility, prevention, older adults |
| TEMPO | Recovery, HRV, fatigue |
| WAVE | Cardio, VO2max |
| SAGE | Nutritional strategy |
| METABOL | Glucose, biomarkers |
| MACRO | Practical meals, portions |
| NOVA | Flexibility |
| SPARK | Habits, consistency |
| STELLA | Mental performance |
| LUNA | Sleep optimization |
| LOGOS | Education, explanations |

---

## Products

### B2C
| Product | Price | Description |
|---------|-------|-------------|
| ASCEND | $99/mo | 13 AI agents, self-directed |
| HYBRID | $199/mo | 13 agents + weekly human coaching |

### B2B (Founding Coaches)
| Phase | Price |
|-------|-------|
| Pilot (3 months) | $0 (feedback required) |
| Post-pilot | $199/mo (founder price) |
| Regular | $299/mo |

---

## Dashboard Style Guide

When creating HTML dashboards:

```css
/* Colors */
--bg-primary: #0D0D0D;
--bg-card: #1A1A1A;
--border: #2A2A2A;
--accent: #6D00FF;
--text-primary: #FFFFFF;
--text-secondary: #A0A0A0;
--success: #00FF88;
--warning: #FFB800;
--danger: #FF4444;

/* Typography */
font-family: 'Inter', sans-serif;  /* Body */
font-family: 'Space Grotesk', sans-serif;  /* Headers */

/* Cards */
border-radius: 12px;
backdrop-filter: blur(10px);
```

---

## Cross-Workspace References

| If you need... | Use workspace... |
|----------------|------------------|
| Email sequences for leads | ngx-marketing |
| B2B proposals | ngx-b2b-sales |
| Podcast/video content | ngx-content-studio |
| PRDs for features | ngx-product-studio |
| SOPs and checklists | ngx-operations |
| Financial reports | ngx-finance |

---

## Repository Status

**All 6 workspaces are complete:**
- 264 files total
- 56 slash commands
- 33 specialized agents
- 6 HTML dashboards
- Full template coverage

---

## Key Files Reference

| File | Purpose |
|------|---------|
| `README.md` | Package overview |
| `SETUP_GUIDE.md` | Installation and usage guide |
| `NGX_COMMANDS_CATALOG.md` | All 56 commands across workspaces |
| `NGX_CONTEXT_QUICK.md` | Quick brand/product context |

---

## Important Notes

1. **This is NOT a code repository** — It's a collection of Claude Code workspace configurations for content generation
2. **Each workspace is independent** — Navigate to the specific workspace folder before starting Claude Code
3. **Memory persists via MEMORY.md** — Always use `/start-session` and `/end-session` to maintain state
4. **Outputs go to /outputs/** — Generated content is saved in each workspace's outputs folder

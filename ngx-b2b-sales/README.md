# NGX B2B Sales Command Center

> Centro de comando para ventas B2B de NGX GENESIS — Founding Coaches Program

## 🚀 Quick Start

```bash
cd ngx-b2b-sales
claude
```

## 📋 Subagents Disponibles

| Agent | Descripción | Modelo |
|-------|-------------|--------|
| `@prospect-researcher` | Investigar y calificar leads B2B | Sonnet |
| `@sales-script-writer` | Scripts de llamadas de venta | Opus |
| `@proposal-architect` | Propuestas y one-pagers | Opus |
| `@b2b-email-architect` | Secuencias de email B2B | Opus |
| `@linkedin-strategist` | Contenido y outreach LinkedIn | Sonnet |
| `@case-study-creator` | Crear case studies de coaches | Opus |
| `@pipeline-analyst` | Análisis de pipeline y forecasting | Sonnet |
| `@onboarding-designer` | Diseñar experiencias de onboarding | Sonnet |

## ⚡ Comandos Principales

```bash
# Investigar un prospect
/prospect-research name="Juan Pérez" instagram=@juanfitness

# Generar script de llamada
/sales-script type=discovery prospect="Juan Pérez"

# Crear propuesta formal
/proposal-create prospect="Juan Pérez" tier=founding

# Secuencia de email B2B
/email-b2b type=outreach prospect="Juan Pérez"

# Contenido LinkedIn
/linkedin-content type=story topic="building in public"

# Crear case study
/case-study coach="María García" results="duplicó clientes"

# Reporte de pipeline
/pipeline-report period=this-week

# Plan de onboarding
/onboarding-plan coach="Juan Pérez"
```

## 🎯 Programa Founding Coaches

| Concepto | Valor |
|----------|-------|
| **Piloto (3 meses)** | $0 (feedback semanal) |
| **Post-piloto** | $199/mes |
| **Setup único** | $299 USD |
| **Clientes incluidos** | Hasta 30 activos |
| **Lugares disponibles** | 10 |

## 📊 Métricas Objetivo

| Fase | Coaches | MRR | Timeline |
|------|---------|-----|----------|
| Founding | 5-10 | $2,495 | Mes 1-3 |
| Growth | 15-30 | $7,485 | Mes 4-6 |
| Scale | 50+ | $24,950 | Mes 12 |

## 🔗 Integraciones

- **n8n** — Automatización de workflows
- **Notion** — CRM y documentación
- **LinkedIn** — Outreach y contenido

## 📁 Estructura

```
ngx-b2b-sales/
├── .claude/
│   ├── agents/      # 8 subagents
│   ├── commands/    # 8 slash commands
│   └── rules/       # Reglas de voz B2B
├── skills/          # Metodologías de venta
├── templates/       # Propuestas, emails, scripts
├── dashboards/      # Pipeline dashboard
└── outputs/         # Contenido generado
```

## 📞 Proceso de Venta

```
PROSPECCIÓN → DESCUBRIMIENTO → DEMO → PROPUESTA → CIERRE → ONBOARDING
```

**Principio:** No vendemos en la primera llamada. Creamos CHAMPIONS.

---

**NGX GENESIS** — *"Rinde hoy. Vive mejor mañana."*

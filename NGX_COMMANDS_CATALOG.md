# NGX Workspaces — Catálogo de Comandos

> Referencia rápida de todos los slash commands disponibles en los 4 workspaces.
> Usar en Claude Code con `/nombre-comando`

---

## 🔄 Comandos Compartidos (Todos los Workspaces)

Estos comandos están disponibles en los 4 workspaces:

| Comando | Descripción |
|---------|-------------|
| `/start-session` | Inicializa sesión: lee MEMORY.md, NGX_CONTEXT.md, DECISIONS.md, DO_NOT.md. Resume estado y pregunta qué hacer. |
| `/end-session` | Finaliza sesión: actualiza MEMORY.md con tareas completadas, próxima prioridad, notas. Confirma guardado. |
| `/status` | Muestra estado actual del workspace sin modificar nada. Útil para orientarse. |

---

## 📣 NGX Marketing Command Center

**Propósito:** Emails, funnels, ads, copy B2C

| Comando | Descripción |
|---------|-------------|
| `/email-sequence` | Genera secuencia de emails para lead magnet o nurturing. Define cantidad, objetivo, audiencia. |
| `/ad-variations` | Crea variaciones de ads para Meta, Google o LinkedIn. Incluye copy, headlines, CTAs. |
| `/audit-funnel` | Audita un funnel completo: landing, lead magnet, thank you, emails, sales page. Score + recomendaciones. |
| `/audit-weekly` | Genera reporte de auditoría semanal de marketing. Wins, problemas, acciones. |
| `/content-week` | Planifica contenido de una semana completa: posts, emails, ads según tema central. |
| `/social-batch` | Genera batch de posts para redes sociales. Educativos, autoridad, engagement. |
| `/report-weekly` | Genera reporte ejecutivo semanal de marketing con métricas y próximos pasos. |
| `/hybrid-qualify` | Califica un lead para HYBRID. Determina si es HOT, WARM o COLD. |
| `/hybrid-call-script` | Genera script para videollamada de cierre HYBRID (25-45 min, 7 pasos). |
| `/hybrid-pipeline` | Actualiza y visualiza pipeline de ventas HYBRID. |

---

## 💼 NGX B2B Sales Command Center

**Propósito:** Prospección, propuestas, pipeline B2B, Founding Coaches

| Comando | Descripción |
|---------|-------------|
| `/prospect-research` | Investiga un prospecto B2B: tamaño, servicios, dolor probable, ángulo de entrada. |
| `/email-b2b` | Genera email de outreach B2B: primer contacto o follow-up. Personalizado, sin pitch largo. |
| `/proposal-create` | Crea propuesta completa para coach/gym. Situación, solución, pricing, próximos pasos. |
| `/sales-script` | Genera script para llamada B2B: discovery o cierre. Incluye preguntas y manejo de objeciones. |
| `/pipeline-report` | Genera reporte de pipeline semanal: prospectos, calls, propuestas, deals. |
| `/linkedin-content` | Crea contenido LinkedIn B2B: posts, artículos, mensajes de conexión. |
| `/case-study` | Genera case study de cliente: desafío, solución, resultados, quote. |
| `/onboarding-plan` | Crea plan de onboarding para nuevo Founding Coach. |

---

## 🎬 NGX Content Studio

**Propósito:** Podcasts, videos, pre-producción multimedia

| Comando | Descripción |
|---------|-------------|
| `/podcast-episode` | Genera episodio completo de podcast con agentes NGX. Script, diálogos, notas de producción. |
| `/podcast-clip` | Extrae clips cortos (1-3 min) de un episodio para redes sociales. |
| `/video-package` | Crea paquete de pre-producción video: storyboard, shot list, prompts VEO/SORA/Kling. |
| `/content-package` | Genera paquete completo de contenido: podcast + clips + video + posts. Todo alineado. |

---

## 📐 NGX Product Studio

**Propósito:** PRDs, documentación técnica, handoffs para coding agents

| Comando | Descripción |
|---------|-------------|
| `/prd-feature` | Genera PRD completo para feature de GENESIS (mobile) o NGX COACH (web). |
| `/prd-agent` | Genera PRD para agente ADK/A2A: system prompt, tools, A2A config, deployment. |
| `/prd-workflow` | Genera PRD para workflow n8n o Cloud Function. |
| `/handoff-package` | Crea paquete de handoff para coding agent: CONTEXT.md, TASK.md, MASTER_PROMPT.md. |

---

## 🔧 NGX Operations Hub

**Propósito:** SOPs, métricas diarias, dashboards, workflows

| Comando | Descripción |
|---------|-------------|
| `/daily-checklist` | Genera checklist diario con 5 MITs, bloques de tiempo y hora de corte. |
| `/weekly-review` | Crea reporte semanal: 3 wins, 3 obstáculos, métricas, prioridades. |
| `/monthly-report` | Genera reporte mensual completo con dashboard y plan de acción. |
| `/sop-create` | Crea SOP estructurado: trigger, pasos, checklist, troubleshooting. |
| `/metrics-dashboard` | Genera dashboard HTML de métricas con estilo NGX dark theme. |
| `/workflow-document` | Documenta workflow n8n: diagrama, inputs/outputs, troubleshooting. |

---

## 💰 NGX Finance

**Propósito:** P&L, proyecciones, presupuesto, facturación

| Comando | Descripción |
|---------|-------------|
| `/monthly-pnl` | Genera P&L mensual con ingresos, gastos, márgenes y comparación MoM. |
| `/runway-calc` | Calcula runway actual con escenarios y fechas críticas. |
| `/projection-create` | Crea proyección financiera con 3 escenarios (conservador/base/optimista). |
| `/budget-review` | Revisa presupuesto vs gastos reales con alertas de variación. |
| `/invoice-create` | Genera factura estructurada con número único y términos de pago. |
| `/unit-economics` | Analiza LTV, CAC, payback period y viabilidad del modelo. |

---

## 📊 Resumen Rápido

| Workspace | Total Commands | Foco Principal |
|-----------|---------------|----------------|
| Marketing | 13 | Emails, ads, funnels, HYBRID B2C |
| B2B Sales | 11 | Prospección, propuestas, pipeline |
| Content Studio | 7 | Podcast, video, pre-producción |
| Product Studio | 7 | PRDs, documentación, handoffs |
| Operations Hub | 9 | SOPs, métricas, workflows |
| Finance | 9 | P&L, proyecciones, facturación |

**Total: 56 comandos** (3 compartidos × 6 workspaces + comandos específicos)

---

## 💡 Tips de Uso

### Iniciar Cualquier Sesión
```bash
cd ngx-{workspace}
claude
/start-session
```

### Terminar Cualquier Sesión
```
/end-session
```

### Ver Estado sin Modificar
```
/status
```

### Flujo Típico de Trabajo
```
/start-session
[Claude resume estado, pregunta qué hacer]
[Tu respuesta]
[Trabajo...]
/end-session
[Claude guarda estado, confirma]
```

---

## 📁 Ubicación de los Comandos

```
ngx-{workspace}/
└── .claude/
    └── commands/
        ├── start-session.md
        ├── end-session.md
        ├── status.md
        └── [comandos específicos].md
```

Cada archivo `.md` en `commands/` define un slash command.

---

## 🔗 Cuándo Usar Cada Workspace

| Necesito... | Workspace |
|-------------|-----------|
| Email sequence para leads | Marketing |
| Ads para Meta/Google | Marketing |
| Auditar un funnel | Marketing |
| Script de cierre HYBRID | Marketing |
| Propuesta para coach/gym | B2B Sales |
| Investigar prospecto | B2B Sales |
| Contenido LinkedIn B2B | B2B Sales |
| Episodio de podcast | Content Studio |
| Video con VEO/SORA | Content Studio |
| PRD de feature | Product Studio |
| PRD de agente ADK | Product Studio |
| Handoff para Claude Code | Product Studio |
| Checklist diario | Operations Hub |
| SOP de proceso | Operations Hub |
| Dashboard de métricas | Operations Hub |
| P&L mensual | Finance |
| Calcular runway | Finance |
| Proyección financiera | Finance |
| Crear factura | Finance |

---

*Documento generado: Diciembre 2025*
*NGX GENESIS — Rinde hoy. Vive mejor mañana.*

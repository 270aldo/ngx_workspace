# NGX Marketing Command Center

> Sistema de inteligencia operativa de marketing para NGX GENESIS usando Claude Code CLI

![NGX](https://img.shields.io/badge/NGX-GENESIS-6D00FF?style=for-the-badge)
![Claude Code](https://img.shields.io/badge/Claude-Code_CLI-000000?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-22C55E?style=for-the-badge)

## 🎯 Propósito

Este repositorio es un **Command Center de Marketing** que utiliza Claude Code CLI para:

- 📝 Generar contenido alineado con la voz de marca "Verdad Directa"
- 📧 Crear secuencias de email y copy de ventas estilo Hormozi
- 🔍 Auditar funnels y landing pages automáticamente
- 📊 Generar reportes y dashboards de performance
- 🤖 Conectar con n8n para automatización de workflows

**NO es un repositorio de código tradicional.** Es un sistema de inteligencia operativa.

## 🚀 Quick Start

### Requisitos
- Claude Code CLI instalado y autenticado
- Claude in Chrome extension (para auditorías)
- Acceso a MCPs configurados (n8n, Canva, Notion)

### Uso

```bash
# Clonar repositorio
git clone git@github.com:tu-usuario/ngx-marketing.git
cd ngx-marketing

# Abrir Claude Code
claude

# Verificar que los subagents están disponibles
/help

# Ejecutar tu primer comando
/content-week audience=30-45 focus=awareness
```

## 📁 Estructura

```
ngx-marketing/
├── .claude/
│   ├── agents/           # 7 subagents especializados
│   ├── commands/         # Slash commands personalizados
│   └── rules/            # Reglas de voz de marca
├── .mcp.json             # Configuración de MCPs
├── CLAUDE.md             # Contexto maestro del workspace
├── skills/               # Skills locales
│   ├── ngx-brand-voice/
│   └── ngx-funnel-criteria/
├── templates/            # Templates reutilizables
├── dashboards/           # Dashboards interactivos
├── knowledge/            # Documentos de referencia
└── outputs/              # Contenido generado
```

## 🤖 Subagents Disponibles

| Agent | Descripción | Modelo |
|-------|-------------|--------|
| `@content-strategist` | Planificación de contenido | Opus |
| `@copywriter-hormozi` | Copy de alto impacto | Opus |
| `@email-architect` | Secuencias de email | Opus |
| `@social-creator` | Contenido para redes | Sonnet |
| `@ads-specialist` | Copy para Meta Ads | Sonnet |
| `@funnel-analyst` | Análisis de métricas | Sonnet |
| `@funnel-auditor` | Auditoría de landings | Opus |
| `@hybrid-sales-agent` | Ventas HYBRID ($199/mes) | Opus |

## ⚡ Comandos Principales

```bash
# Planificar contenido semanal
/content-week audience=30-45 focus=awareness

# Generar secuencia de emails
/email-sequence type=welcome lead_magnet=stress-signature days=7

# Auditar una landing page
/audit-funnel https://ngxgenesis.com/stress-signature type=landing

# Auditoría semanal programada
/audit-weekly

# Generar reporte semanal
/report-weekly
```

### 💎 Comandos HYBRID Sales

```bash
# Calificar un lead como HYBRID o ASCEND
/hybrid-qualify name="María García" source=lead_magnet lead_magnet=ngx-transform

# Generar script de llamada de venta
/hybrid-call-script name="María García" pain_points="disciplina,tiempo"

# Reporte de pipeline HYBRID
/hybrid-pipeline period=this-week
```

## 📊 Dashboard de Auditorías

El dashboard interactivo se encuentra en `dashboards/funnel-audit-dashboard.html`

Características:
- Score histórico por URL
- Trending de issues
- Comparativa semana vs semana
- Alertas de regresiones
- Estilo NGX (dark mode, violeta #6D00FF)

## 💎 Dashboard HYBRID Sales

Dashboard de ventas HYBRID en `dashboards/hybrid-sales-dashboard.html`

Características:
- Funnel de conversión HYBRID
- Pipeline de leads activos
- Objeciones más comunes
- Revenue MRR histórico
- Métricas de tasa de cierre

## 🎨 Voz de Marca

Este workspace está configurado para seguir la voz "Verdad Directa":

> **"Confrontamos con respeto, fundamentamos con ciencia, resolvemos con sistemas."**

### Los 3 Modos
- **Modo A (Experto):** Educar, explicar el "por qué"
- **Modo B (Verdad):** Confrontar, hooks, captar atención
- **Modo C (Arquitecto):** Mostrar sistema, convertir

### Fórmula NGX
```
CONFRONTA → FUNDAMENTA → RESUELVE
```

## 🔗 MCPs Conectados

- **n8n:** Automatización de workflows
- **Canva:** Generación de diseños
- **Notion:** Documentación y planning
- **Claude in Chrome:** Auditoría de navegador

## 📋 Checklist de Contenido

Antes de publicar cualquier contenido, verificar:

- [ ] Tratamiento correcto (tú para 30-45 / usted para 45-60)
- [ ] Sin términos prohibidos (PRIME, LONGEVITY, promesas absolutas)
- [ ] Agente correcto mencionado
- [ ] Acción concreta al final
- [ ] Tono "Verdad Directa"
- [ ] Visual con violeta #6D00FF
- [ ] Máximo 1-2 emojis

## 🗓️ Auditorías Programadas

Las auditorías semanales se ejecutan:
- **Frecuencia:** Cada lunes
- **Hora:** 9:00 AM
- **URLs:** Landing principal + Lead magnets + Checkouts

Para programar con Claude in Chrome:
```
Schedule /audit-weekly to run every Monday at 9:00 AM
```

## 📈 Métricas Objetivo

| Etapa | KPI | Meta |
|-------|-----|------|
| TOFU | Leads/mes | 500-1000 |
| MOFU | Email open rate | >30% |
| BOFU | Conversiones/mes | 15-60 |
| Funnel | Score promedio | >80 |

## 🤝 Contribución

Este es un repositorio interno de NGX. Para contribuir:

1. Crea una rama para tu cambio
2. Documenta cualquier nuevo subagent o comando
3. Asegúrate de que el contenido sigue la voz de marca
4. Solicita review antes de merge

---

**NGX GENESIS** — *"Rinde hoy. Vive mejor mañana."*

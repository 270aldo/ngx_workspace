# MASTER_PROMPT: Completar NGX Workspaces

> Este prompt es para Claude Code. Cópialo al iniciar sesión en la carpeta raíz de ngx-workspaces.

---

## CONTEXTO

Tienes 6 workspaces de configuración para NGX GENESIS. Cada workspace es una carpeta independiente con:
- `CLAUDE.md` — Instrucciones principales (ya completo)
- `MEMORY.md` — Sistema de persistencia (ya completo)
- `.claude/commands/` — Comandos slash (ya completos)
- `.claude/agents/` — Agentes especializados (ya completos)
- `dashboards/` — Dashboards HTML (INCOMPLETO en varios)
- `templates/` — Templates de documentos (INCOMPLETO en varios)
- `skills/` — Skills especializados (INCOMPLETO en Content Studio)

## TU MISIÓN

Completar lo que falta en cada workspace según el PRD en `PRD_COMPLETAR_WORKSPACES.md`.

---

## INSTRUCCIONES GENERALES

### Estilo de Dashboards HTML

```css
/* Colores */
--background: #0D0D0D;
--card-bg: #1A1A1A;
--card-border: #2A2A2A;
--accent: #6D00FF;
--accent-glow: rgba(109, 0, 255, 0.3);
--text-primary: #FFFFFF;
--text-secondary: #A0A0A0;
--success: #00FF88;
--warning: #FFB800;
--danger: #FF4444;

/* Tipografía */
font-family: 'Inter', sans-serif;
/* Headers: 'Space Grotesk' */

/* Cards */
border-radius: 12px;
backdrop-filter: blur(10px);
border: 1px solid var(--card-border);
```

### Estructura de Templates

```markdown
# [Nombre del Template]

**Versión:** 1.0
**Propósito:** [Una línea]

---

## [Sección 1]

[Contenido con placeholders claros usando [CORCHETES]]

---

## [Sección 2]

[Más contenido...]

---

*Template creado: [fecha]*
```

### Ubicación de Archivos

```
Dashboards → workspace/dashboards/[nombre]-dashboard.html
Templates → workspace/templates/[categoria]/[nombre]-template.md
Skills → workspace/skills/[nombre]/SKILL.md
```

---

## TAREAS POR WORKSPACE

### 1. NGX Operations Hub (`ngx-operations/`)

**Crear:**

```
dashboards/ops-metrics-dashboard.html
templates/sop-template.md
templates/daily-checklist-template.md
templates/weekly-review-template.md
templates/monthly-report-template.md
sops/cliente-onboarding-sop.md
sops/contenido-publicacion-sop.md
sops/weekly-review-sop.md
```

**Dashboard ops-metrics debe incluir:**
- Header con fecha y semana
- KPIs: Tareas completadas, % cumplimiento, horas
- Checklist interactivo del día
- Lista de SOPs más usados
- Status de workflows
- Alertas de items pendientes

---

### 2. NGX Finance (`ngx-finance/`)

**Crear:**

```
dashboards/finance-dashboard.html
templates/invoices/invoice-template.md
templates/reports/monthly-pnl-template.md
templates/projections/projection-template.md
templates/reports/budget-tracking-template.md
```

**Dashboard finance debe incluir:**
- Header con mes y status general
- KPIs: MRR, Runway, Burn rate
- Gráfico de MRR (placeholder con datos de ejemplo)
- Breakdown de gastos por categoría
- Clientes por producto
- Alertas de presupuesto

---

### 3. NGX Marketing (`ngx-marketing/`)

**Crear:**

```
templates/ads/meta-ad-template.md
templates/ads/google-ad-template.md
templates/ads/linkedin-ad-template.md
templates/landing/landing-page-template.md
templates/landing/lead-magnet-page-template.md
templates/social/instagram-post-template.md
templates/social/linkedin-post-template.md
templates/social/twitter-thread-template.md
```

---

### 4. NGX B2B Sales (`ngx-b2b-sales/`)

**Crear:**

```
templates/proposals/founding-coach-proposal.md
templates/proposals/gym-studio-proposal.md
templates/scripts/discovery-call-script.md
templates/scripts/closing-call-script.md
templates/scripts/objection-handling.md
templates/case-studies/case-study-template.md
templates/emails/cold-outreach-sequence.md
templates/emails/follow-up-sequence.md
```

---

### 5. NGX Content Studio (`ngx-content-studio/`)

**Crear:**

```
dashboards/content-production-dashboard.html
templates/podcast/episode-structure-template.md
templates/podcast/show-notes-template.md
templates/video/shot-list-template.md
templates/video/storyboard-template.md
templates/prompts/image-prompt-template.md
skills/veo31/SKILL.md (copiar de /mnt/skills/user/ngx-veo31-content-factory/)
skills/sora2/SKILL.md (copiar de /mnt/skills/user/ngx-sora2-content-factory/)
skills/elevenlabs/SKILL.md (copiar de /mnt/skills/user/ngx-voice-engine/)
```

**Dashboard content-production debe incluir:**
- Pipeline de contenido por etapa
- Calendario semanal
- Assets pendientes
- Métricas de publicación

---

### 6. NGX Product Studio (`ngx-product-studio/`)

**Crear:**

```
dashboards/prd-tracker-dashboard.html
templates/prd-mobile-feature.md
templates/prd-web-feature.md
templates/prd-n8n-workflow.md
```

**Dashboard prd-tracker debe incluir:**
- Lista de PRDs activos con status
- PRDs completados (archivo)
- Handoffs pendientes para coding agents
- Timeline/roadmap simplificado

---

## ORDEN DE EJECUCIÓN

```
1. ngx-operations/dashboards/ops-metrics-dashboard.html
2. ngx-operations/templates/*.md
3. ngx-operations/sops/*.md
4. ngx-finance/dashboards/finance-dashboard.html
5. ngx-finance/templates/**/*.md
6. ngx-marketing/templates/**/*.md
7. ngx-b2b-sales/templates/**/*.md
8. ngx-content-studio/dashboards/content-production-dashboard.html
9. ngx-content-studio/templates/**/*.md
10. ngx-content-studio/skills/**/* (copiar de /mnt/skills/)
11. ngx-product-studio/dashboards/prd-tracker-dashboard.html
12. ngx-product-studio/templates/*.md
```

---

## VERIFICACIÓN

Después de cada archivo creado, verifica:

**Para HTML:**
```bash
# Abrir en navegador para verificar
open [archivo].html
# O en Linux
xdg-open [archivo].html
```

**Para Markdown:**
```bash
# Verificar que existe y tiene contenido
cat [archivo].md | head -20
```

---

## EJEMPLO DE DASHBOARD (Referencia)

Usa este como base para los dashboards faltantes:

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[Nombre] Dashboard — NGX</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --bg-primary: #0D0D0D;
            --bg-card: #1A1A1A;
            --border: #2A2A2A;
            --accent: #6D00FF;
            --accent-glow: rgba(109, 0, 255, 0.3);
            --text-primary: #FFFFFF;
            --text-secondary: #A0A0A0;
            --success: #00FF88;
            --warning: #FFB800;
            --danger: #FF4444;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background: var(--bg-primary);
            color: var(--text-primary);
            min-height: 100vh;
            padding: 24px;
        }
        
        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 32px;
        }
        
        .header h1 {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 28px;
            font-weight: 700;
        }
        
        .header .date {
            color: var(--text-secondary);
            font-size: 14px;
        }
        
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 32px;
        }
        
        .card {
            background: var(--bg-card);
            border: 1px solid var(--border);
            border-radius: 12px;
            padding: 20px;
        }
        
        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 16px;
        }
        
        .card-title {
            font-size: 14px;
            color: var(--text-secondary);
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }
        
        .card-value {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 32px;
            font-weight: 700;
        }
        
        .card-change {
            font-size: 12px;
            padding: 4px 8px;
            border-radius: 4px;
        }
        
        .card-change.positive {
            background: rgba(0, 255, 136, 0.1);
            color: var(--success);
        }
        
        .card-change.negative {
            background: rgba(255, 68, 68, 0.1);
            color: var(--danger);
        }
        
        .section-title {
            font-family: 'Space Grotesk', sans-serif;
            font-size: 18px;
            margin-bottom: 16px;
        }
        
        .list-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 0;
            border-bottom: 1px solid var(--border);
        }
        
        .list-item:last-child {
            border-bottom: none;
        }
        
        .status-badge {
            font-size: 12px;
            padding: 4px 12px;
            border-radius: 20px;
        }
        
        .status-badge.active {
            background: rgba(109, 0, 255, 0.2);
            color: var(--accent);
        }
        
        .status-badge.pending {
            background: rgba(255, 184, 0, 0.2);
            color: var(--warning);
        }
        
        .status-badge.done {
            background: rgba(0, 255, 136, 0.2);
            color: var(--success);
        }
        
        @media (max-width: 768px) {
            body {
                padding: 16px;
            }
            
            .header h1 {
                font-size: 22px;
            }
            
            .card-value {
                font-size: 26px;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>[Nombre] Dashboard</h1>
        <span class="date" id="currentDate"></span>
    </div>
    
    <div class="grid">
        <div class="card">
            <div class="card-header">
                <span class="card-title">KPI 1</span>
                <span class="card-change positive">+12%</span>
            </div>
            <div class="card-value">$1,234</div>
        </div>
        
        <div class="card">
            <div class="card-header">
                <span class="card-title">KPI 2</span>
                <span class="card-change negative">-5%</span>
            </div>
            <div class="card-value">56</div>
        </div>
        
        <div class="card">
            <div class="card-header">
                <span class="card-title">KPI 3</span>
            </div>
            <div class="card-value">89%</div>
        </div>
    </div>
    
    <div class="card">
        <h2 class="section-title">Lista de Items</h2>
        <div class="list-item">
            <span>Item 1</span>
            <span class="status-badge active">Activo</span>
        </div>
        <div class="list-item">
            <span>Item 2</span>
            <span class="status-badge pending">Pendiente</span>
        </div>
        <div class="list-item">
            <span>Item 3</span>
            <span class="status-badge done">Completado</span>
        </div>
    </div>
    
    <script>
        // Set current date
        const now = new Date();
        const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
        document.getElementById('currentDate').textContent = now.toLocaleDateString('es-MX', options);
    </script>
</body>
</html>
```

---

## AL TERMINAR

1. Ejecuta verificación de todos los archivos:
```bash
find . -name "*.html" -o -name "*.md" | wc -l
# Debe ser significativamente mayor que antes
```

2. Verifica que cada workspace tiene su dashboard:
```bash
for ws in ngx-*/; do
    echo "=== $ws ==="
    ls -la "$ws/dashboards/"*.html 2>/dev/null || echo "NO DASHBOARD"
done
```

3. Lista los templates creados:
```bash
find . -path "*/templates/*" -name "*.md" | wc -l
```

---

## NOTAS IMPORTANTES

1. **No modifiques** los archivos existentes (CLAUDE.md, comandos, agentes)
2. **Sí crea** los archivos nuevos listados arriba
3. **Usa placeholders claros** como `[NOMBRE]`, `[FECHA]`, `[VALOR]`
4. **Mantén consistencia** en estilo y formato entre workspaces
5. **Verifica** cada archivo después de crearlo

---

*MASTER_PROMPT v1.0 — Para uso con Claude Code*

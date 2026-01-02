# NGX Workspaces - Guía de Comandos

---

## Quick Start

```bash
# Ir a un workspace
cd ~/ngx_workspace/ngx-[nombre]

# Iniciar Claude Code
claude

# Ver comandos disponibles
/help
```

---

## 1. Operations Hub

**Ubicación:** `ngx-operations/`

### Comandos Disponibles

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `/daily-checklist` | Genera checklist del día | `/daily-checklist` |
| `/weekly-review` | Crea reporte semanal | `/weekly-review` |
| `/monthly-report` | Genera reporte mensual | `/monthly-report diciembre` |
| `/create-sop` | Crea nuevo SOP | `/create-sop onboarding-vip` |
| `/ops-status` | Resumen de operaciones | `/ops-status` |

### Prompts Útiles

```
"Genera mi checklist para hoy basado en las prioridades pendientes"

"Crea un SOP para el proceso de cancelación de membresía"

"Dame el resumen semanal de operaciones"

"¿Qué tareas llevan más de 48 horas pendientes?"

"Prepara el reporte mensual de diciembre con métricas de cumplimiento"
```

### Archivos de Referencia

```
templates/
├── sop-template.md              → Base para nuevos SOPs
├── daily-checklist-template.md  → Checklist diario
├── weekly-review-template.md    → Review semanal
└── monthly-report-template.md   → Reporte mensual

sops/
├── onboarding-cliente.md        → SOP de onboarding
├── publicar-contenido.md        → SOP de publicación
└── facturacion-mensual.md       → SOP de facturación
```

---

## 2. Finance

**Ubicación:** `ngx-finance/`

### Comandos Disponibles

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `/invoice` | Genera factura | `/invoice cliente:Juan producto:HYBRID` |
| `/pnl` | Reporte P&L | `/pnl mes:diciembre` |
| `/projection` | Proyección financiera | `/projection meses:6` |
| `/budget-check` | Revisa presupuesto | `/budget-check` |
| `/mrr-report` | Reporte de MRR | `/mrr-report` |

### Prompts Útiles

```
"Genera una factura para Juan Pérez por NGX HYBRID temporada completa"

"Crea el P&L de diciembre 2025"

"Haz una proyección financiera a 6 meses asumiendo 10% growth mensual"

"¿Cuál es mi runway actual?"

"Compara gastos de este mes vs el anterior"

"Genera reporte de MRR con breakdown por producto"
```

### Archivos de Referencia

```
templates/
├── invoices/
│   └── invoice-template.md       → Template de factura
├── reports/
│   └── monthly-pnl-template.md   → Template P&L
├── projections/
│   └── projection-template.md    → Template proyecciones
└── budget/
    └── budget-tracking-template.md → Tracking de budget
```

---

## 3. Marketing

**Ubicación:** `ngx-marketing/`

### Comandos Disponibles

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `/meta-ad` | Crea ad para Meta | `/meta-ad producto:ASCEND audiencia:40+` |
| `/google-ad` | Crea ad para Google | `/google-ad keywords:fitness coaching` |
| `/landing` | Estructura landing page | `/landing producto:HYBRID` |
| `/social-post` | Genera post social | `/social-post plataforma:instagram tipo:carousel` |
| `/funnel-audit` | Audita el funnel | `/funnel-audit` |
| `/campaign` | Crea campaña completa | `/campaign nombre:NewYear objetivo:leads` |

### Prompts Útiles

```
"Crea 3 variaciones de ad para Meta targeting hombres 40-55 interesados en fitness"

"Genera un carousel de Instagram sobre los 13 agentes de NGX"

"Estructura una landing page para NGX HYBRID con enfoque en resultados"

"Escribe 5 hooks para reels sobre pérdida de grasa después de los 40"

"Crea copy para Google Ads con keywords: coaching fitness personalizado"

"Dame ideas de contenido para la semana enfocado en BLAZE"
```

### Archivos de Referencia

```
templates/
├── ads/
│   ├── meta-ad-template.md       → Ads Meta/FB/IG
│   └── google-ad-template.md     → Ads Google Search
├── landing/
│   └── landing-page-template.md  → Estructura landing
└── social/
    └── social-post-template.md   → Posts sociales

dashboards/
├── funnel-audit-dashboard.html   → Auditoría de funnel
└── hybrid-sales-dashboard.html   → Sales de HYBRID
```

---

## 4. B2B Sales

**Ubicación:** `ngx-b2b-sales/`

### Comandos Disponibles

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `/proposal` | Genera propuesta | `/proposal tipo:gym cliente:FitLife` |
| `/discovery-prep` | Prepara discovery call | `/discovery-prep prospecto:CoachMaria` |
| `/email-sequence` | Crea secuencia email | `/email-sequence tipo:cold-outbound` |
| `/case-study` | Documenta caso éxito | `/case-study cliente:GymX` |
| `/objection-handler` | Maneja objeciones | `/objection-handler objecion:precio` |
| `/pipeline-status` | Estado del pipeline | `/pipeline-status` |

### Prompts Útiles

```
"Crea una propuesta para el gym FitLife con 200 miembros"

"Prepárame para una discovery call con María, coach de nutrición con 15 clientes"

"Genera una secuencia de 4 emails para outbound frío a coaches"

"¿Cómo manejo la objeción 'es muy caro'?"

"Crea un case study basado en estos resultados: [datos]"

"Dame el script para una llamada de cierre"

"Escribe un email de follow-up para alguien que pidió tiempo para pensar"
```

### Archivos de Referencia

```
templates/
├── proposals/
│   ├── founding-coach-proposal.md  → Propuesta Founding Coaches
│   └── gym-studio-proposal.md      → Propuesta Gyms/Studios
├── scripts/
│   └── discovery-call-script.md    → Script discovery call
├── case-studies/
│   └── case-study-template.md      → Template case study
└── emails/
    └── b2b-sequence-templates.md   → Secuencias de email

dashboards/
└── pipeline-dashboard.html         → Pipeline de ventas
```

---

## 5. Product Studio

**Ubicación:** `ngx-product-studio/`

### Comandos Disponibles

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `/prd` | Crea PRD | `/prd tipo:mobile feature:onboarding` |
| `/prd-n8n` | PRD para workflow | `/prd-n8n workflow:lead-scoring` |
| `/prd-web` | PRD para web | `/prd-web feature:dashboard-v2` |
| `/prd-status` | Estado de PRDs | `/prd-status` |
| `/handoff` | Preparar handoff | `/handoff prd:MOB-202512-001` |
| `/roadmap` | Ver roadmap | `/roadmap quarter:Q1` |

### Prompts Útiles

```
"Crea un PRD para renovar el onboarding de la app mobile"

"Necesito un PRD para un workflow de n8n que haga lead scoring automático"

"Genera PRD para añadir widgets de LUNA al dashboard web"

"¿Cuál es el estado de los PRDs activos?"

"Prepara el handoff del PRD de onboarding para el equipo de desarrollo"

"Dame el roadmap de Q1 2026"

"Prioriza estos 5 features para el próximo sprint"
```

### Archivos de Referencia

```
templates/
└── prd/
    ├── n8n-workflow-prd.md    → PRD para workflows n8n
    ├── mobile-feature-prd.md  → PRD para features mobile
    └── web-feature-prd.md     → PRD para features web

dashboards/
└── prd-tracker-dashboard.html  → Tracker de PRDs
```

---

## 6. Content Studio

**Ubicación:** `ngx-content-studio/`

### Comandos Disponibles

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `/veo` | Genera video con VEO | `/veo tipo:broll descripcion:workout` |
| `/sora` | Genera imagen/video | `/sora tipo:thumbnail tema:5ejercicios` |
| `/voice` | Genera voice-over | `/voice script:"Bienvenidos a NGX"` |
| `/podcast-plan` | Planea episodio | `/podcast-plan tema:sueño invitado:DrSleep` |
| `/shot-list` | Crea shot list | `/shot-list video:tutorial-app` |
| `/storyboard` | Genera storyboard | `/storyboard video:ad-hybrid` |
| `/content-calendar` | Ver calendario | `/content-calendar semana:próxima` |

### Prompts Útiles

```
"Genera prompts para 5 thumbnails de YouTube sobre entrenamiento 40+"

"Crea un shot list para filmar un tutorial de la app"

"Planea el episodio 24 del podcast sobre la ciencia del sueño"

"Escribe el script para un voice-over de 30 segundos para un ad"

"Dame ideas de B-roll para generar con VEO para videos de workout"

"Crea un storyboard para un reel de 30 segundos sobre BLAZE"

"¿Qué contenido tenemos programado para esta semana?"

"Genera 3 variaciones de thumbnail para 'Mi rutina con NGX GENESIS'"
```

### Archivos de Referencia

```
skills/
├── veo31/
│   └── SKILL.md            → Skill VEO 3.1
├── sora2/
│   └── SKILL.md            → Skill SORA 2
└── elevenlabs/
    └── SKILL.md            → Skill ElevenLabs

templates/
├── podcast/
│   └── episode-template.md  → Template episodio
├── video/
│   ├── shot-list-template.md    → Shot list
│   └── storyboard-template.md   → Storyboard
└── image/
    └── prompt-template.md   → Librería de prompts

dashboards/
└── content-production-dashboard.html → Dashboard producción
```

---

## Atajos de Terminal Recomendados

Añade a tu `~/.zshrc` o `~/.bashrc`:

```bash
# NGX Workspace Aliases
alias ngx-ops="cd ~/ngx_workspace/ngx-operations && claude"
alias ngx-fin="cd ~/ngx_workspace/ngx-finance && claude"
alias ngx-mkt="cd ~/ngx_workspace/ngx-marketing && claude"
alias ngx-sales="cd ~/ngx_workspace/ngx-b2b-sales && claude"
alias ngx-prod="cd ~/ngx_workspace/ngx-product-studio && claude"
alias ngx-content="cd ~/ngx_workspace/ngx-content-studio && claude"

# Quick access
alias ngx="cd ~/ngx_workspace"
```

Después ejecuta:
```bash
source ~/.zshrc
```

Ahora puedes simplemente escribir:
```bash
ngx-sales    # Abre Claude en B2B Sales
ngx-content  # Abre Claude en Content Studio
```

---

## Tips de Uso

### 1. Contexto Automático
Claude carga automáticamente el contexto del workspace. No necesitas explicar qué es NGX cada vez.

### 2. Templates como Base
Siempre usa los templates existentes como punto de partida, no empieces de cero.

### 3. Outputs Organizados
Los resultados se guardan en `outputs/` de cada workspace, organizados por fecha.

### 4. Combinar Workspaces
Puedes referenciar outputs de otros workspaces:
```
"Usa el case study de ngx-b2b-sales/outputs/ para crear contenido social"
```

### 5. Dashboards en Browser
Abre los dashboards HTML directamente en tu browser:
```bash
open dashboards/pipeline-dashboard.html
```

---

## Flujos de Trabajo Comunes

### Crear y Vender a un Gym

```
1. ngx-sales → /proposal tipo:gym cliente:NombreGym
2. ngx-sales → /discovery-prep prospecto:ContactoGym
3. ngx-sales → /email-sequence tipo:post-call
4. ngx-marketing → /case-study (después de cerrar)
```

### Lanzar Contenido Semanal

```
1. ngx-content → /content-calendar semana:próxima
2. ngx-content → /podcast-plan tema:X
3. ngx-content → /shot-list video:Y
4. ngx-content → /sora tipo:thumbnails
5. ngx-content → /voice script:intro
```

### Nuevo Feature de Producto

```
1. ngx-prod → /prd tipo:mobile feature:nombre
2. ngx-prod → /handoff prd:ID
3. ngx-content → crear contenido de lanzamiento
4. ngx-marketing → /campaign nombre:launch-feature
```

---

*NGX Workspaces Commands Cheatsheet v1.0*

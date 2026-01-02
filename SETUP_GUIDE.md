# NGX Workspaces — Guía de Setup

> Cómo instalar, configurar y usar los 6 workspaces de NGX.

---

## Requisitos Previos

- **Claude Code** instalado (`npm install -g @anthropic-ai/claude-code`)
- **Terminal** con acceso a carpetas locales
- **Los 6 ZIPs** descargados

---

## Instalación

### Paso 1: Crear carpeta base

```bash
mkdir -p ~/ngx-workspaces
cd ~/ngx-workspaces
```

### Paso 2: Descomprimir los 6 workspaces

```bash
unzip ngx-marketing-command-center.zip
unzip ngx-b2b-sales-command-center.zip
unzip ngx-content-studio.zip
unzip ngx-product-studio.zip
unzip ngx-operations-hub.zip
unzip ngx-finance.zip
```

### Paso 3: Verificar estructura

```bash
ls -la
# Debes ver:
# ngx-marketing/
# ngx-b2b-sales/
# ngx-content-studio/
# ngx-product-studio/
# ngx-operations/
# ngx-finance/
```

---

## Cómo Usar un Workspace

### Método 1: Claude Code (Recomendado)

```bash
# 1. Entrar al workspace
cd ~/ngx-workspaces/ngx-marketing

# 2. Iniciar Claude Code
claude

# 3. Claude lee CLAUDE.md automáticamente
# 4. Iniciar sesión de trabajo
/start-session

# 5. Usar comandos específicos
/email-sequence type=welcome lead_magnet=ngx-transform

# 6. Al terminar
/end-session
```

### Método 2: Claude Desktop (Projects)

1. Abrir Claude Desktop
2. Crear nuevo Project: "NGX Marketing Command Center"
3. En Project Knowledge, subir estos archivos del workspace:
   - `CLAUDE.md`
   - `NGX_CONTEXT.md`
   - `MEMORY.md`
   - `DECISIONS.md`
   - `DO_NOT.md`
   - Carpeta `.claude/` completa
   - Carpeta `skills/` si existe
4. En System Prompt del proyecto, pegar:
   ```
   Lee CLAUDE.md al inicio de cada conversación y sigue sus instrucciones.
   ```
5. Listo para usar

---

## Los 6 Workspaces

### 1. NGX Marketing Command Center

**Carpeta:** `ngx-marketing/`
**Propósito:** Marketing B2C, emails, ads, funnels, HYBRID

**Comandos principales:**
```
/start-session          # Iniciar
/email-sequence         # Crear secuencia de emails
/ad-variations          # Generar variaciones de ads
/audit-funnel           # Auditar funnel completo
/hybrid-qualify         # Calificar lead para HYBRID
/hybrid-call-script     # Script de llamada de cierre
/end-session            # Guardar y cerrar
```

**Primera tarea sugerida:**
```
/start-session
/email-sequence type=welcome lead_magnet=ngx-transform audience=30-45
```

---

### 2. NGX B2B Sales Command Center

**Carpeta:** `ngx-b2b-sales/`
**Propósito:** Ventas B2B, coaches, propuestas, pipeline

**Comandos principales:**
```
/start-session
/prospect-research      # Investigar prospecto
/email-b2b              # Email de prospección
/proposal-create        # Crear propuesta
/sales-script           # Script de llamada
/pipeline-report        # Reporte de pipeline
/end-session
```

**Primera tarea sugerida:**
```
/start-session
/prospect-research name="[Nombre del coach]" instagram="@handle"
```

---

### 3. NGX Content Studio

**Carpeta:** `ngx-content-studio/`
**Propósito:** Contenido multimedia, podcasts, videos

**Comandos principales:**
```
/start-session
/podcast-episode        # Crear episodio completo
/podcast-clip           # Extraer clips de episodio
/video-package          # Paquete de video (VEO/SORA)
/content-package        # Paquete multi-formato
/end-session
```

**Primera tarea sugerida:**
```
/start-session
/podcast-episode topic="Por qué fallan el 80% de los programas de fitness" agents=BLAZE,SAGE
```

---

### 4. NGX Product Studio

**Carpeta:** `ngx-product-studio/`
**Propósito:** PRDs, documentación técnica, handoffs

**Comandos principales:**
```
/start-session
/prd-feature            # PRD para feature de app
/prd-agent              # PRD para agente ADK
/prd-workflow           # PRD para workflow n8n
/handoff-package        # Paquete para coding agent
/end-session
```

**Primera tarea sugerida:**
```
/start-session
/prd-feature name="Daily Check-in" platform=genesis-mobile
```

---

### 5. NGX Operations Hub

**Carpeta:** `ngx-operations/`
**Propósito:** SOPs, métricas, workflows diarios

**Comandos principales:**
```
/start-session
/daily-checklist        # Checklist del día
/weekly-review          # Reporte semanal
/monthly-report         # Reporte mensual
/sop-create             # Crear SOP nuevo
/metrics-dashboard      # Dashboard de métricas
/workflow-document      # Documentar workflow n8n
/end-session
```

**Primera tarea sugerida:**
```
/start-session
/daily-checklist
```

---

### 6. NGX Finance

**Carpeta:** `ngx-finance/`
**Propósito:** P&L, proyecciones, presupuesto, facturas

**Comandos principales:**
```
/start-session
/monthly-pnl            # P&L mensual
/runway-calc            # Calcular runway
/projection-create      # Proyección financiera
/budget-review          # Revisar presupuesto
/invoice-create         # Crear factura
/unit-economics         # Analizar unit economics
/end-session
```

**Primera tarea sugerida:**
```
/start-session
/runway-calc
```

---

## Flujo de Trabajo Diario Recomendado

### Mañana (15 min)

```bash
cd ~/ngx-workspaces/ngx-operations
claude
/start-session
/daily-checklist
/end-session
```

### Durante el día (según necesidad)

```bash
# Si necesitas crear contenido de marketing
cd ~/ngx-workspaces/ngx-marketing
claude
/start-session
# ... trabajo ...
/end-session

# Si necesitas trabajar en ventas B2B
cd ~/ngx-workspaces/ngx-b2b-sales
claude
# etc.
```

### Viernes (30 min)

```bash
cd ~/ngx-workspaces/ngx-operations
claude
/start-session
/weekly-review
/end-session

cd ~/ngx-workspaces/ngx-finance
claude
/start-session
/budget-review
/end-session
```

---

## Archivos Importantes en Cada Workspace

| Archivo | Propósito | Cuándo se actualiza |
|---------|-----------|---------------------|
| `CLAUDE.md` | Instrucciones principales | Raramente |
| `MEMORY.md` | Estado entre sesiones | Cada `/end-session` |
| `NGX_CONTEXT.md` | Contexto de marca/producto | Cuando cambie pricing/producto |
| `DECISIONS.md` | Decisiones tomadas | Cuando se tome decisión importante |
| `DO_NOT.md` | Errores a evitar | Cuando se identifique error recurrente |

---

## Troubleshooting

### Claude no lee CLAUDE.md

```bash
# Verificar que estás en la carpeta correcta
pwd
# Debe mostrar: ~/ngx-workspaces/ngx-[workspace]

# Verificar que existe CLAUDE.md
ls -la CLAUDE.md
```

### Comando no funciona

```bash
# Verificar que existe el comando
ls .claude/commands/

# Los comandos disponibles aparecen ahí
```

### Quiero ver qué hay en el workspace

```bash
# Ver estructura completa
find . -type f -name "*.md" | head -20
```

---

## Actualizar NGX_CONTEXT.md

Si cambian los precios o el producto, actualiza `NGX_CONTEXT.md` en TODOS los workspaces:

```bash
# Editar el archivo maestro
nano ~/ngx-workspaces/ngx-marketing/NGX_CONTEXT.md

# Copiar a todos los demás
cp ~/ngx-workspaces/ngx-marketing/NGX_CONTEXT.md ~/ngx-workspaces/ngx-b2b-sales/
cp ~/ngx-workspaces/ngx-marketing/NGX_CONTEXT.md ~/ngx-workspaces/ngx-content-studio/
cp ~/ngx-workspaces/ngx-marketing/NGX_CONTEXT.md ~/ngx-workspaces/ngx-product-studio/
cp ~/ngx-workspaces/ngx-marketing/NGX_CONTEXT.md ~/ngx-workspaces/ngx-operations/
cp ~/ngx-workspaces/ngx-marketing/NGX_CONTEXT.md ~/ngx-workspaces/ngx-finance/
```

---

## Siguiente Paso

Los workspaces están listos para usar, pero algunos tienen contenido incompleto (dashboards, templates faltantes).

Ver `PRD_COMPLETAR_WORKSPACES.md` para las instrucciones de completar lo que falta.

---

*NGX Workspaces v1.0 — Diciembre 2025*

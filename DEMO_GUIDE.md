# NGX Workspaces - Demo Guiada

---

## Setup Completado ✅

Los aliases ya están configurados en tu terminal.

**Para activarlos en tu sesión actual:**
```bash
source ~/.zshrc
```

---

## Aliases Disponibles

### Workspaces
| Comando | Qué hace |
|---------|----------|
| `ngx` | Va a ~/ngx_workspace |
| `ngx-ops` | Abre Claude en Operations |
| `ngx-fin` | Abre Claude en Finance |
| `ngx-mkt` | Abre Claude en Marketing |
| `ngx-sales` | Abre Claude en B2B Sales |
| `ngx-prod` | Abre Claude en Product Studio |
| `ngx-content` | Abre Claude en Content Studio |

### Dashboards
| Comando | Qué abre |
|---------|----------|
| `ngx-dash-ops` | Dashboard Operations |
| `ngx-dash-fin` | Dashboard Finance |
| `ngx-dash-sales` | Dashboard Sales Pipeline |
| `ngx-dash-prod` | Dashboard PRD Tracker |
| `ngx-dash-content` | Dashboard Content Production |

### Ayuda
| Comando | Qué hace |
|---------|----------|
| `ngx-help` | Muestra el cheatsheet de comandos |

---

## Demo 1: Crear una Propuesta de Ventas

### Paso 1: Abrir el workspace
```bash
ngx-sales
```

### Paso 2: En Claude, pedir la propuesta
```
Crea una propuesta para el gym "FitLife" con estos datos:
- Contacto: María García
- Ubicación: CDMX
- 350 miembros
- Quieren ofrecer NGX como add-on premium
- Budget: $15,000 MXN/mes
```

### Paso 3: Claude usará el template
Claude automáticamente usa `templates/proposals/gym-studio-proposal.md` y lo personaliza.

### Paso 4: Resultado
La propuesta se guarda en `outputs/proposals/fitlife-proposal-2025-12.md`

---

## Demo 2: Planear Contenido de Video

### Paso 1: Abrir el workspace
```bash
ngx-content
```

### Paso 2: Pedir un shot list
```
Necesito un shot list para un video de YouTube:
"5 Ejercicios Esenciales para Hombres de 40+"
- Duración: 8-10 minutos
- Locación: Gym moderno
- Estilo: Educativo pero dinámico
```

### Paso 3: Pedir thumbnails
```
Genera 3 prompts de thumbnail para SORA para este video
```

### Paso 4: Pedir voice-over
```
Escribe el script para un voice-over de intro de 20 segundos
```

---

## Demo 3: Generar Reporte Financiero

### Paso 1: Abrir el workspace
```bash
ngx-fin
```

### Paso 2: Pedir el P&L
```
Genera el P&L de diciembre con estos datos:

Ingresos:
- 15 suscripciones ASCEND ($100 c/u)
- 8 clientes HYBRID ($1,200 c/u)
- 2 contratos COACH ($500/mes c/u)

Gastos:
- Servidores: $200
- Marketing: $1,500
- Tools/Software: $300
- Contractor: $800
```

---

## Demo 4: Flujo Completo de Producto

### Paso 1: Crear PRD
```bash
ngx-prod
```
```
Crea un PRD para añadir "Dark Mode" a la app mobile de NGX GENESIS
```

### Paso 2: Crear contenido de lanzamiento
```bash
ngx-content
```
```
Basándome en el PRD de Dark Mode, crea:
1. 3 posts de Instagram anunciando el feature
2. Script para un reel de 30 segundos
3. Copy para email a usuarios
```

### Paso 3: Configurar campaña
```bash
ngx-mkt
```
```
Crea una mini-campaña para el lanzamiento de Dark Mode:
- 2 ads para Instagram Stories
- 1 email a la base de usuarios
- Copy para push notification
```

---

## Ver Dashboards en Acción

Abre cada dashboard en tu browser:

```bash
# Ver todos los dashboards
ngx-dash-ops      # Operaciones
ngx-dash-fin      # Finanzas
ngx-dash-sales    # Pipeline de ventas
ngx-dash-prod     # PRDs y roadmap
ngx-dash-content  # Producción de contenido
```

Los dashboards son interactivos - puedes hacer click en elementos, filtrar, y ver detalles.

---

## Tips Pro

### 1. Combinar Workspaces
Puedes referenciar outputs de otros workspaces:
```
"Usa el case study que generamos en ngx-sales para crear
un carousel de Instagram"
```

### 2. Guardar Prompts Exitosos
Cuando un prompt funcione bien, guárdalo en `templates/` del workspace.

### 3. Personalizar Templates
Los templates son tu punto de partida. Edítalos para que reflejen tu estilo y necesidades.

### 4. Usar Dashboards como Referencia
Abre el dashboard mientras trabajas para tener contexto visual.

### 5. Outputs Organizados
Todo lo que generes se puede guardar en `outputs/` organizado por fecha y tipo.

---

## Estructura de Archivos por Workspace

```
ngx-[workspace]/
├── .claude/
│   ├── agents/      → Definiciones de agentes AI
│   ├── commands/    → Comandos disponibles
│   └── rules/       → Reglas de comportamiento
├── dashboards/      → HTML interactivos
├── templates/       → Plantillas base
├── skills/          → Prompts especializados (Content Studio)
├── sops/            → Procedimientos (Operations)
└── outputs/         → Resultados generados
```

---

## Siguiente Nivel: MCPs

Los workspaces pueden conectarse a MCPs para:
- **Notion** → Sincronizar tareas y docs
- **Google Drive** → Guardar outputs directamente
- **Slack** → Notificaciones automáticas
- **Supabase** → Datos en tiempo real para dashboards

Para configurar MCPs, edita `.claude/settings.json` en cada workspace.

---

## ¿Necesitas Ayuda?

```bash
# Ver todos los comandos disponibles
ngx-help

# O pregúntame directamente en cualquier workspace
"¿Qué comandos tengo disponibles aquí?"
```

---

*NGX Workspaces Demo Guide v1.0*

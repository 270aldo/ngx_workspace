# NGX Operations Hub

> Centro de comando para operaciones diarias, SOPs y métricas de NGX.

## ⚠️ PRIMERA INSTRUCCIÓN - MEMORIA Y CONTEXTO

**Archivos de este workspace:**

| Archivo | Cuándo Leer | Propósito |
|---------|-------------|-----------|
| `MEMORY.md` | **Siempre al inicio** | Estado entre sesiones |
| `NGX_CONTEXT.md` | Cuando necesites contexto NGX | Info compartida de marca/producto |
| `DECISIONS.md` | Antes de contradecir algo | Decisiones ya tomadas |
| `DO_NOT.md` | Antes de entregar | Errores a evitar |
| `CHECKLIST.md` | Antes de entregar | Calidad pre-entrega |
| `PROMPTS.md` | Cuando necesites inspiración | Prompts probados |
| `TASKS.md` | Para tareas frecuentes | Flujos optimizados |

**Slash Commands de Sesión:**
- `/start-session` → Inicializa, lee archivos, resume estado
- `/end-session` → Guarda estado en MEMORY.md
- `/status` → Muestra estado actual sin modificar

**AL INICIAR CADA SESIÓN:**
1. Lee `MEMORY.md` completo
2. Lee `NGX_CONTEXT.md` para contexto
3. Revisa `DECISIONS.md` para decisiones activas
4. Revisa `DO_NOT.md` para errores a evitar
5. Resume el estado actual al usuario
6. Pregunta si continuar con la tarea pendiente o hacer algo nuevo

**AL TERMINAR CADA SESIÓN:**
1. Actualiza `MEMORY.md` con:
   - Fecha de sesión
   - Tareas completadas
   - Próxima prioridad
   - Notas relevantes
2. Si hubo decisiones nuevas, agrégalas a `DECISIONS.md`
3. Confirma al usuario que la memoria fue guardada

---

## Propósito

Este workspace gestiona las **operaciones diarias** de NGX:

- **SOPs** — Procedimientos estandarizados para tareas recurrentes
- **Métricas** — Dashboards y tracking de KPIs
- **Workflows diarios** — Checklists y rutinas operativas
- **Reportes** — Semanales, mensuales, de estado
- **Automatizaciones** — Documentación de workflows n8n

---

## Estructura del Workspace

```
ngx-operations/
├── CLAUDE.md              ← Este archivo
├── MEMORY.md              ← Estado persistente
├── NGX_CONTEXT.md         ← Contexto compartido NGX
├── DECISIONS.md           ← Decisiones tomadas
├── DO_NOT.md              ← Errores a evitar
├── CHECKLIST.md           ← Calidad pre-entrega
├── PROMPTS.md             ← Prompts probados
├── TASKS.md               ← Tareas frecuentes
├── CROSS_REFERENCES.md    ← Referencias entre workspaces
├── .claude/
│   ├── commands/          ← Slash commands
│   ├── agents/            ← Agentes especializados
│   └── rules/             ← Reglas del workspace
├── sops/                  ← Procedimientos operativos
├── dashboards/            ← Dashboards HTML
├── templates/             ← Templates de SOPs y reportes
├── outputs/               ← Entregas generadas
└── knowledge/             ← Documentación de referencia
```

---

## Agentes Disponibles

| Agente | Rol | Cuándo Usarlo |
|--------|-----|---------------|
| `ops-manager` | Coordinador de operaciones | Planificación diaria/semanal |
| `sop-architect` | Diseñador de SOPs | Crear procedimientos nuevos |
| `metrics-analyst` | Analista de métricas | Dashboards y KPIs |
| `workflow-designer` | Diseñador de automatizaciones | Documentar flujos n8n |

---

## Comandos Disponibles

| Comando | Descripción |
|---------|-------------|
| `/start-session` | Inicializa sesión de trabajo |
| `/end-session` | Guarda estado y cierra sesión |
| `/status` | Muestra estado actual |
| `/daily-checklist` | Genera checklist diario |
| `/weekly-review` | Crea reporte semanal de operaciones |
| `/monthly-report` | Genera reporte mensual completo |
| `/sop-create` | Crea nuevo SOP desde descripción |
| `/metrics-dashboard` | Genera dashboard de métricas |
| `/workflow-document` | Documenta un workflow n8n |

---

## Filosofía Operativa

### Principios

1. **Documentar todo** — Si se hace más de una vez, necesita SOP
2. **Medir lo importante** — Solo KPIs que impulsen acción
3. **Automatizar lo repetitivo** — Tiempo = recurso escaso
4. **Revisar semanalmente** — Sin revisión no hay mejora

### Métricas Clave NGX

| Categoría | KPIs |
|-----------|------|
| **Leads** | Nuevos leads/semana, tasa conversión lead magnet |
| **Ventas** | MRR, nuevos clientes, churn |
| **Contenido** | Posts/semana, engagement, reach |
| **Producto** | Bugs abiertos, features shipped |
| **Operaciones** | Tareas completadas, SLA cumplido |

---

## Flujo de Trabajo Típico

```
Inicio de semana:
/start-session
/weekly-review (revisar semana anterior)
/daily-checklist (planificar lunes)

Durante la semana:
/daily-checklist (cada mañana)
/sop-create (cuando identifiques proceso repetitivo)

Fin de semana:
/weekly-review
/end-session
```

---

## Reglas del Workspace

1. **SOPs deben ser accionables** — Pasos claros, sin ambigüedad
2. **Métricas con contexto** — Número sin comparación no sirve
3. **Reportes concisos** — Máximo 1 página para semanales
4. **Checklists verificables** — Cada item debe poder marcarse como hecho

---

## Integración con Otros Workspaces

| Necesito... | Workspace |
|-------------|-----------|
| Crear campaña de marketing | Marketing Command Center |
| Propuesta para coach | B2B Sales Command Center |
| Contenido multimedia | Content Studio |
| PRD de feature | Product Studio |
| Proyecciones financieras | Finance |

---

*NGX Operations Hub — Orden en el caos.*

# NGX Finance

> Centro de control financiero para NGX GENESIS.

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

Este workspace gestiona las **finanzas** de NGX:

- **Proyecciones** — Forecasts de ingresos y gastos
- **Budget tracking** — Control de presupuesto
- **Facturación** — Gestión de invoices
- **Análisis financiero** — P&L, unit economics, runway
- **Reportes** — Mensuales, trimestrales

---

## Estructura del Workspace

```
ngx-finance/
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
├── dashboards/            ← Dashboards financieros
├── templates/
│   ├── invoices/          ← Templates de facturas
│   ├── reports/           ← Templates de reportes
│   └── projections/       ← Templates de proyecciones
├── outputs/
│   ├── reports/           ← Reportes generados
│   └── invoices/          ← Facturas generadas
└── knowledge/             ← Documentación de referencia
```

---

## Agentes Disponibles

| Agente | Rol | Cuándo Usarlo |
|--------|-----|---------------|
| `financial-analyst` | Analista financiero | Proyecciones, análisis, unit economics |
| `budget-tracker` | Controlador de presupuesto | Tracking de gastos, alertas |
| `invoice-processor` | Gestor de facturación | Crear y gestionar facturas |

---

## Comandos Disponibles

| Comando | Descripción |
|---------|-------------|
| `/start-session` | Inicializa sesión de trabajo |
| `/end-session` | Guarda estado y cierra sesión |
| `/status` | Muestra estado actual |
| `/monthly-pnl` | Genera P&L mensual |
| `/runway-calc` | Calcula runway actual |
| `/projection-create` | Crea proyección financiera |
| `/budget-review` | Revisa estado del presupuesto |
| `/invoice-create` | Genera factura |
| `/unit-economics` | Analiza unit economics |

---

## Modelo Financiero NGX

### Productos y Precios

| Producto | Precio | Modelo |
|----------|--------|--------|
| **ASCEND** | $100/mes | 3 meses mínimo = $300/temporada |
| **HYBRID** | $1,200/temporada | 12 semanas con coach |
| **Founding Coaches** | $0 piloto → $199/mes | B2B |
| **Coaches Regular** | $299/mes | B2B |

### Estructura de Costos Típica

| Categoría | Ejemplos |
|-----------|----------|
| **Infraestructura** | GCP, Supabase, Vercel |
| **APIs IA** | Anthropic, Google AI, ElevenLabs |
| **Marketing** | Ads, herramientas |
| **Servicios** | Dominios, emails, tools |

### Métricas Clave

| Métrica | Qué Mide |
|---------|----------|
| **MRR** | Ingresos recurrentes mensuales |
| **ARR** | MRR × 12 |
| **CAC** | Costo de adquisición de cliente |
| **LTV** | Valor de vida del cliente |
| **LTV:CAC** | Ratio de eficiencia |
| **Churn** | Tasa de cancelación |
| **Runway** | Meses de operación con caja actual |
| **Burn Rate** | Gastos mensuales |

---

## Flujo de Trabajo Típico

```
Inicio de mes:
/start-session
/monthly-pnl (cerrar mes anterior)
/budget-review (revisar vs plan)
/runway-calc (actualizar runway)

Durante el mes:
/invoice-create (cuando hay venta)
/budget-review (check semanal)

Fin de mes:
/monthly-pnl
/projection-create (actualizar forecast)
/end-session
```

---

## Reglas del Workspace

1. **Números verificados** — Nunca inventar datos financieros
2. **Conservador en proyecciones** — Mejor sorpresa positiva que negativa
3. **Separar fijo de variable** — Claridad en estructura de costos
4. **Runway siempre visible** — Saber cuánto tiempo tienes
5. **Unit economics claros** — Saber si el modelo funciona

---

## Integración con Otros Workspaces

| Necesito... | Workspace |
|-------------|-----------|
| Datos de ventas | Marketing / B2B Sales |
| Costos de contenido | Content Studio |
| Costos de desarrollo | Product Studio |
| Métricas operativas | Operations Hub |

---

## Disclaimer

Este workspace asiste con análisis financiero pero no reemplaza:
- Contador profesional para impuestos
- Asesor legal para contratos
- Auditor para estados financieros oficiales

Para decisiones financieras importantes, consulta con profesionales.

---

*NGX Finance — Claridad en los números.*

# PRD: n8n Workflow - [Nombre del Workflow]

---

**PRD ID:** WF-[YYYYMM]-[NNN]
**Autor:** [Nombre]
**Fecha:** [DD de Mes, YYYY]
**Status:** [ ] Draft [ ] En Revisión [ ] Aprobado [ ] En Desarrollo [ ] Completado
**Prioridad:** [ ] P0 (Crítico) [ ] P1 (Alto) [ ] P2 (Medio) [ ] P3 (Bajo)

---

## 1. Resumen Ejecutivo

### Problema a Resolver
```
[Describir el problema o proceso manual que este workflow automatiza]
```

### Solución Propuesta
```
[Descripción breve del workflow y cómo resuelve el problema]
```

### Métricas de Éxito

| Métrica | Actual | Objetivo | Cómo Medir |
|---------|--------|----------|------------|
| [Tiempo ahorrado] | [X hrs/semana] | [Y hrs/semana] | [Método] |
| [Errores reducidos] | [X%] | [Y%] | [Método] |
| [Throughput] | [X/día] | [Y/día] | [Método] |

---

## 2. Contexto del Workflow

### Proceso Actual (Manual)

```
Paso 1: [Descripción del paso manual actual]
   ↓
Paso 2: [Descripción]
   ↓
Paso 3: [Descripción]
   ↓
Paso N: [Resultado final]
```

**Tiempo promedio:** [X minutos/horas]
**Frecuencia:** [Diaria/Semanal/Por evento]
**Responsable actual:** [Rol o persona]

### Pain Points del Proceso Actual

- ❌ [Pain point 1]
- ❌ [Pain point 2]
- ❌ [Pain point 3]

### Por Qué n8n

```
[Justificación de usar n8n vs otras alternativas:
 - Zapier, Make, código custom, etc.]
```

---

## 3. Especificación del Workflow

### Diagrama de Flujo

```
┌─────────────────┐
│     TRIGGER     │
│  [Tipo: _____]  │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│    PASO 1       │
│  [Descripción]  │
└────────┬────────┘
         │
    ┌────┴────┐
    │ IF/ELSE │
    └────┬────┘
    ┌────┴────┐
    │         │
    ▼         ▼
┌───────┐ ┌───────┐
│ SI    │ │ NO    │
└───┬───┘ └───┬───┘
    │         │
    ▼         ▼
┌───────┐ ┌───────┐
│ Paso  │ │ Paso  │
│  2a   │ │  2b   │
└───┬───┘ └───┬───┘
    └────┬────┘
         │
         ▼
┌─────────────────┐
│    OUTPUT       │
│  [Resultado]    │
└─────────────────┘
```

### Trigger

| Campo | Valor |
|-------|-------|
| **Tipo** | [ ] Webhook [ ] Schedule [ ] Manual [ ] App Event |
| **Configuración** | [Detalles del trigger] |
| **Frecuencia** | [Si aplica] |
| **Payload esperado** | [Estructura de datos entrantes] |

### Nodos del Workflow

#### Nodo 1: [Nombre]
| Aspecto | Detalle |
|---------|---------|
| **Tipo** | [HTTP Request / Function / IF / Set / etc.] |
| **Servicio** | [Gmail, Notion, Slack, etc.] |
| **Acción** | [GET, POST, Update, Create, etc.] |
| **Input** | [Datos que recibe] |
| **Output** | [Datos que produce] |
| **Credenciales** | [Tipo de auth requerida] |

#### Nodo 2: [Nombre]
| Aspecto | Detalle |
|---------|---------|
| **Tipo** | [Tipo de nodo] |
| **Servicio** | [Servicio] |
| **Acción** | [Acción] |
| **Input** | [Datos] |
| **Output** | [Datos] |
| **Credenciales** | [Auth] |

*[Repetir para cada nodo]*

### Lógica Condicional

```javascript
// Condición principal
if (item.status === 'active' && item.score >= 50) {
  // Rama A: Lead calificado
  return { qualified: true };
} else {
  // Rama B: Nurturing
  return { qualified: false };
}
```

### Transformaciones de Datos

```javascript
// Ejemplo de transformación en Function node
const transformedData = {
  fullName: `${$input.first_name} ${$input.last_name}`,
  score: calculateScore($input.activity),
  segment: determineSegment($input),
  timestamp: new Date().toISOString()
};

return { json: transformedData };
```

---

## 4. Integraciones

### Servicios Conectados

| Servicio | Rol en Workflow | Credencial | Rate Limits |
|----------|-----------------|------------|-------------|
| [Servicio 1] | [Trigger/Action] | [OAuth/API Key] | [X req/min] |
| [Servicio 2] | [Action] | [OAuth/API Key] | [X req/min] |
| [Servicio 3] | [Action] | [OAuth/API Key] | [X req/min] |

### APIs Externas

| API | Endpoint | Método | Payload |
|-----|----------|--------|---------|
| [API 1] | `[/endpoint]` | `[POST]` | `[estructura]` |
| [API 2] | `[/endpoint]` | `[GET]` | `[params]` |

### Webhooks Salientes

| Destino | URL Pattern | Payload | Retries |
|---------|-------------|---------|---------|
| [Sistema 1] | `[url]` | `[estructura]` | [N] |

---

## 5. Manejo de Errores

### Estrategia de Error Handling

| Error Tipo | Acción | Notificación |
|------------|--------|--------------|
| API timeout | Retry x3, delay 30s | Slack si falla |
| Invalid data | Log + skip | Email alert |
| Auth failure | Stop workflow | Email + Slack |
| Rate limit | Wait + retry | Log only |

### Fallback Logic

```javascript
// En caso de error en nodo principal
try {
  // Lógica principal
} catch (error) {
  // Fallback: [descripción de acción alternativa]
  // Notificar: [método de notificación]
  // Log: [qué información guardar]
}
```

### Alertas y Notificaciones

| Evento | Canal | Destinatario | Template |
|--------|-------|--------------|----------|
| Workflow fail | Slack | #ops-alerts | Error alert |
| Success summary | Email | [team] | Daily digest |
| Warning | Slack | #dev | Warning alert |

---

## 6. Performance y Límites

### Capacidad Esperada

| Métrica | Valor Esperado | Límite Máximo |
|---------|----------------|---------------|
| Ejecuciones/hora | [N] | [M] |
| Tiempo por ejecución | [X seg] | [Y seg timeout] |
| Data procesada/día | [X MB] | [Y MB] |

### Optimizaciones

- [ ] Batch processing para volumen alto
- [ ] Caching de datos frecuentes
- [ ] Parallel execution donde posible
- [ ] Deduplicación de requests

---

## 7. Testing y Validación

### Casos de Test

| Caso | Input | Expected Output | Status |
|------|-------|-----------------|--------|
| Happy path | [Input válido] | [Output esperado] | [ ] |
| Edge case 1 | [Input límite] | [Output esperado] | [ ] |
| Error case | [Input inválido] | [Error handling] | [ ] |
| Empty data | [Vacío] | [Skip/default] | [ ] |

### Datos de Prueba

```json
{
  "test_input": {
    "field1": "value1",
    "field2": "value2"
  },
  "expected_output": {
    "result": "expected_result"
  }
}
```

### Checklist Pre-Deploy

- [ ] Todos los casos de test pasan
- [ ] Credenciales en environment variables
- [ ] Error handling implementado
- [ ] Logs configurados
- [ ] Alertas configuradas
- [ ] Documentación actualizada
- [ ] Rollback plan definido

---

## 8. Deployment

### Environment Variables

| Variable | Descripción | Ejemplo |
|----------|-------------|---------|
| `API_KEY_[SERVICE]` | API key para [servicio] | `xxx-xxx-xxx` |
| `WEBHOOK_SECRET` | Secret para validar webhooks | `hash` |
| `ENV` | Ambiente (prod/dev/staging) | `prod` |

### Rollout Plan

| Fase | % Tráfico | Duración | Criterio Avance |
|------|-----------|----------|-----------------|
| Canary | 10% | 1 día | 0 errores críticos |
| Partial | 50% | 2 días | < 0.1% error rate |
| Full | 100% | - | Métricas estables |

### Rollback

```
En caso de issues:
1. Desactivar workflow en n8n
2. Ejecutar proceso manual (backup)
3. Notificar a [equipo]
4. Documentar issue en [sistema]
```

---

## 9. Monitoreo Post-Launch

### Métricas a Trackear

| Métrica | Herramienta | Alerta Si |
|---------|-------------|-----------|
| Success rate | n8n built-in | < 95% |
| Avg execution time | n8n built-in | > [X]s |
| Errors/hour | n8n + Slack | > [N] |
| Queue size | n8n | > [M] |

### Dashboard Link

```
[Link al dashboard de monitoreo en n8n / Grafana / etc.]
```

---

## 10. Documentación

### Para Operaciones

```
Cómo ejecutar manualmente:
1. [Paso 1]
2. [Paso 2]

Cómo pausar:
1. [Paso]

Cómo debuggear:
1. [Paso 1]
2. [Paso 2]
```

### Para Desarrollo

```
Repositorio: [link]
Branch: [branch name]
Workflow ID: [id en n8n]
```

---

## 11. Timeline y Handoff

### Fases de Implementación

| Fase | Fechas | Responsable | Entregable |
|------|--------|-------------|------------|
| PRD Final | [Fecha] | Product | Documento aprobado |
| Desarrollo | [Fecha-Fecha] | Dev | Workflow funcional |
| Testing | [Fecha-Fecha] | QA | Test report |
| Deploy | [Fecha] | DevOps | Live workflow |
| Monitoreo | [Fecha+] | Ops | Dashboard |

### Handoff Checklist

**Product → Dev:**
- [ ] PRD aprobado
- [ ] Acceso a servicios otorgado
- [ ] Credenciales compartidas seguras
- [ ] Casos de test definidos

**Dev → Ops:**
- [ ] Workflow exportado (JSON)
- [ ] Documentación de operación
- [ ] Runbook de troubleshooting
- [ ] Alertas configuradas

---

## 12. Apéndices

### A. Glosario

| Término | Definición |
|---------|------------|
| [Término 1] | [Definición] |
| [Término 2] | [Definición] |

### B. Referencias

- [Documentación n8n relevante]
- [APIs de servicios integrados]
- [PRDs relacionados]

### C. Historial de Cambios

| Fecha | Versión | Cambio | Autor |
|-------|---------|--------|-------|
| [Fecha] | 1.0 | Creación inicial | [Autor] |
| [Fecha] | 1.1 | [Cambio] | [Autor] |

---

*Template PRD n8n Workflow NGX v1.0*

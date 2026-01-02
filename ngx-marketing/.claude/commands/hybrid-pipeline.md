---
description: Genera reporte del pipeline de ventas HYBRID con métricas y próximos pasos
arguments:
  - name: period
    description: Período del reporte (this-week, last-week, this-month)
    default: this-week
  - name: format
    description: Formato de salida (markdown, summary)
    default: markdown
---

# Reporte de Pipeline HYBRID

**Período:** $ARGUMENTS.period
**Formato:** $ARGUMENTS.format

---

## Instrucciones para @hybrid-sales-agent

Genera un reporte completo del pipeline de ventas HYBRID.

### ESTRUCTURA DEL PIPELINE HYBRID

```
LEAD CAPTURED
    ↓
QUALIFIED (HYBRID vs ASCEND)
    ↓
CALL SCHEDULED
    ↓
CALL COMPLETED
    ↓
PROPOSAL SENT
    ↓
CLOSED WON / CLOSED LOST
    ↓
ONBOARDING
```

---

## TEMPLATE DE REPORTE

```markdown
# PIPELINE HYBRID - REPORTE SEMANAL
**Período:** [fecha inicio] - [fecha fin]
**Generado:** [fecha]

---

## RESUMEN EJECUTIVO

### Métricas Clave

| Métrica | Esta Semana | Meta | Status |
|---------|-------------|------|--------|
| Leads calificados HYBRID | [X] | 5 | 🟢/🟡/🔴 |
| Llamadas agendadas | [X] | 3 | 🟢/🟡/🔴 |
| Llamadas completadas | [X] | 3 | 🟢/🟡/🔴 |
| Cierres | [X] | 1 | 🟢/🟡/🔴 |
| Revenue HYBRID | $[X] | $597 | 🟢/🟡/🔴 |

### Conversion Rates

| Transición | Rate |
|------------|------|
| Lead → Calificado HYBRID | [X%] |
| Calificado → Llamada agendada | [X%] |
| Llamada agendada → Completada | [X%] |
| Llamada → Cierre | [X%] |
| **Overall: Lead → Cliente** | **[X%]** |

---

## PIPELINE POR ETAPA

### 🎯 Leads Calificados HYBRID (Pendiente llamada)

| Nombre | Fuente | Score | Días en etapa | Próximo paso |
|--------|--------|-------|---------------|--------------|
| [Nombre] | [Fuente] | [X]/14 | [X] días | [Acción] |

### 📞 Llamadas Agendadas

| Nombre | Fecha/Hora | Preparación | Notas |
|--------|------------|-------------|-------|
| [Nombre] | [Fecha] | ✅/❌ | [Notas] |

### ✅ Llamadas Completadas (Pendiente decisión)

| Nombre | Fecha llamada | Resultado | Follow-up |
|--------|---------------|-----------|-----------|
| [Nombre] | [Fecha] | [Interesado/Objeciones/No] | [Fecha] |

### 💰 Cerrados Esta Semana

| Nombre | Fecha cierre | Valor | Inicio onboarding |
|--------|--------------|-------|-------------------|
| [Nombre] | [Fecha] | $597 | [Fecha] |

### ❌ Perdidos Esta Semana

| Nombre | Etapa perdida | Razón | Aprendizaje |
|--------|---------------|-------|-------------|
| [Nombre] | [Etapa] | [Razón] | [Qué aprendimos] |

---

## ANÁLISIS DE CONVERSIÓN

### ¿Dónde perdemos más leads?

| Etapa | Leads perdidos | % del total | Razón principal |
|-------|----------------|-------------|-----------------|
| [Etapa 1] | [X] | [X%] | [Razón] |
| [Etapa 2] | [X] | [X%] | [Razón] |

### Objeciones más comunes

| Objeción | Frecuencia | Tasa de superación |
|----------|------------|-------------------|
| Precio | [X] | [X%] |
| Necesito pensarlo | [X] | [X%] |
| No es buen momento | [X] | [X%] |
| Prefiero ASCEND | [X] | [X%] |

---

## FORECAST

### Próximos 7 días

| Escenario | Cierres esperados | Revenue |
|-----------|-------------------|---------|
| Conservador | [X] | $[X] |
| Probable | [X] | $[X] |
| Optimista | [X] | $[X] |

### Próximos 30 días

| Escenario | Cierres esperados | Revenue |
|-----------|-------------------|---------|
| Conservador | [X] | $[X] |
| Probable | [X] | $[X] |
| Optimista | [X] | $[X] |

---

## ACCIONES PRIORITARIAS

### Esta semana DEBE:

1. **[Acción 1]** — [Nombre del lead] — [Por qué es urgente]
2. **[Acción 2]** — [Nombre del lead] — [Por qué es urgente]
3. **[Acción 3]** — [Nombre del lead] — [Por qué es urgente]

### Leads en riesgo:

| Nombre | Días sin actividad | Acción sugerida |
|--------|-------------------|-----------------|
| [Nombre] | [X] días | [Acción] |

---

## CLIENTES HYBRID ACTIVOS

### En Onboarding (Primeros 30 días)

| Nombre | Día de programa | Engagement | Riesgo |
|--------|-----------------|------------|--------|
| [Nombre] | Día [X] | Alto/Medio/Bajo | 🟢/🟡/🔴 |

### Activos (Mes 2-3)

| Nombre | Mes | Progreso | Riesgo de churn |
|--------|-----|----------|-----------------|
| [Nombre] | Mes [X] | [Descripción] | 🟢/🟡/🔴 |

### Próximos a Renovar

| Nombre | Fecha fin | Intención | Acción |
|--------|-----------|-----------|--------|
| [Nombre] | [Fecha] | Renovar/Bajar a ASCEND/Cancelar | [Acción] |

---

## MÉTRICAS DE NEGOCIO

| Métrica | Actual | Meta Mes | Meta Q1 |
|---------|--------|----------|---------|
| MRR HYBRID | $[X] | $[X] | $[X] |
| Clientes HYBRID activos | [X] | [X] | [X] |
| Churn rate | [X%] | <10% | <5% |
| LTV promedio | $[X] | $1,791 | $1,791 |
| CAC HYBRID | $[X] | <$100 | <$75 |

---

*Próximo reporte: [fecha]*
```

---

## Output

Guarda en: `outputs/hybrid/$(date +%Y-%m-%d)-hybrid-pipeline-report.md`

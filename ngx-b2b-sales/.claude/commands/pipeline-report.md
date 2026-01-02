---
description: Genera un reporte de análisis del pipeline de ventas B2B
arguments:
  - name: period
    description: Período del reporte (this-week|last-week|this-month|last-month)
    default: this-week
  - name: type
    description: Tipo de análisis (full|velocity|forecast|conversion)
    default: full
---

# Reporte de Pipeline B2B

**Período:** $ARGUMENTS.period
**Tipo:** $ARGUMENTS.type

---

## Instrucciones para @pipeline-analyst

Genera el reporte de pipeline según el tipo solicitado:

### Tipos de Reporte:

**full** → Reporte semanal completo
- Resumen ejecutivo
- Pipeline por etapa
- Top deals por probabilidad
- Deals en riesgo
- Conversion analysis
- Forecast 30 días
- Actividad de la semana
- Insights y recomendaciones
- Closed lost analysis

**velocity** → Análisis de velocidad de ventas
- Sales Velocity = (Deals × Win Rate × Deal Value) ÷ Sales Cycle
- Análisis de cada componente
- Recomendaciones para mejorar cada uno
- Comparación con período anterior

**forecast** → Proyección de cierre
- Deals en Proposal y Negotiation
- Probabilidad ponderada
- Escenarios: Conservador / Probable / Optimista
- Revenue proyectado
- Acciones para acelerar

**conversion** → Análisis de conversión
- Conversion rate por etapa
- Cuello de botella identificado
- Comparación con benchmarks
- Recomendaciones específicas

### Métricas a incluir:

**Pipeline:**
- Total Pipeline Value
- Weighted Pipeline
- Deals activos
- Nuevos vs Movidos vs Cerrados

**Actividad:**
- Prospects identificados
- Emails enviados
- Llamadas realizadas
- Demos completadas
- Propuestas enviadas

**Tiempo:**
- Time to first response
- Discovery → Demo time
- Demo → Proposal time
- Total sales cycle

### Formato:
- Tablas claras
- Status indicators (🟢🟡🔴)
- Comparación con período anterior
- Acciones concretas

---

## Output

Guarda en: `outputs/reports/$(date +%Y-%m-%d)-pipeline-$ARGUMENTS.type-report.md`

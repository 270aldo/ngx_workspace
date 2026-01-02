---
description: Genera el reporte semanal consolidado de marketing NGX con métricas, insights y próximos pasos
arguments:
  - name: period
    description: Período del reporte (this-week|last-week|custom)
    default: last-week
  - name: include_audit
    description: Incluir resumen de última auditoría de funnel (true|false)
    default: true
  - name: format
    description: Formato de salida (markdown|html)
    default: markdown
---

# Reporte Semanal de Marketing NGX

**Período:** $ARGUMENTS.period
**Incluir auditoría:** $ARGUMENTS.include_audit
**Formato:** $ARGUMENTS.format

---

## Instrucciones para @funnel-analyst

Genera el reporte semanal consolidado siguiendo esta estructura:

### 1. Recopilar Datos

**Fuentes de datos:**
- Outputs de campañas en `outputs/ads/`
- Emails enviados en `outputs/emails/`
- Contenido publicado en `outputs/social/`
- Auditorías en `outputs/audits/`

**Métricas a incluir:**
- Leads capturados (por lead magnet)
- CPL por canal
- Email open/click rates
- Engagement en social
- Conversiones a ASCEND/HYBRID
- Score promedio del funnel (si include_audit=true)

### 2. Estructura del Reporte

```markdown
# 📊 REPORTE SEMANAL DE MARKETING NGX

**Período:** [fecha inicio] - [fecha fin]
**Generado:** [fecha y hora]

---

## 🎯 RESUMEN EJECUTIVO

### Highlights de la Semana
- ✅ [Logro 1]
- ✅ [Logro 2]
- ⚠️ [Área de atención]

### Métricas Clave vs Objetivos

| Métrica | Actual | Objetivo | Status |
|---------|--------|----------|--------|
| Leads | [X] | 125/sem | 🟢/🟡/🔴 |
| CPL | $[X] | <$5 | 🟢/🟡/🔴 |
| Email Open Rate | [X%] | >30% | 🟢/🟡/🔴 |
| Conversiones | [X] | 4-6/sem | 🟢/🟡/🔴 |

---

## 📈 PERFORMANCE POR CANAL

### Paid Media (Meta Ads)
- **Spend:** $[X] de $250/semana
- **Leads:** [X]
- **CPL:** $[X]
- **CTR:** [X%]

**Top Ad:**
> "[Copy del mejor ad]"
> CTR: [X%] | Conversiones: [X]

### Email Marketing
- **Emails enviados:** [X]
- **Open Rate promedio:** [X%]
- **Click Rate promedio:** [X%]
- **Unsubscribes:** [X]

**Mejor Subject Line:**
> "[Subject]" - [X%] open rate

### Contenido Orgánico
- **Posts publicados:** [X]
- **Reach total:** [X]
- **Engagement promedio:** [X%]

**Top Post:**
> [Descripción] - [X] engagement

---

## 🧲 PERFORMANCE POR LEAD MAGNET

| Lead Magnet | Leads | CPL | → MQL | → Customer |
|-------------|-------|-----|-------|------------|
| Stress Signature | [X] | $[X] | [X%] | [X] |
| NGX Transform | [X] | $[X] | [X%] | [X] |
| LOGOS Dictionary | [X] | $[X] | [X%] | [X] |
| Metabolic Age | [X] | $[X] | [X%] | [X] |

**Insight:** [Cuál funciona mejor y por qué]

---

## 👥 PERFORMANCE POR AUDIENCIA

### Audiencia 30-45 años
- Leads: [X] ([X%] del total)
- CPL: $[X]
- Conversion rate: [X%]

### Audiencia 45-60 años
- Leads: [X] ([X%] del total)
- CPL: $[X]
- Conversion rate: [X%]

**Insight:** [Comparativa y recomendaciones]

---

## 🔍 RESUMEN DE AUDITORÍA DE FUNNEL
(Si include_audit=true)

**Score Promedio:** [X]/100
**Cambio vs semana anterior:** [±X]

### Issues Críticos Activos
1. [Issue 1] - [Página]
2. [Issue 2] - [Página]

### Mejoras Implementadas Esta Semana
- [Mejora 1]
- [Mejora 2]

---

## 💡 INSIGHTS Y APRENDIZAJES

### Lo Que Funcionó
1. [Insight 1 con datos]
2. [Insight 2 con datos]

### Lo Que No Funcionó
1. [Problema 1 y posible causa]
2. [Problema 2 y posible causa]

### Hipótesis Para Testear
1. [Hipótesis 1]
2. [Hipótesis 2]

---

## 🎯 PLAN PARA PRÓXIMA SEMANA

### Prioridades
1. **[Prioridad 1]** - Responsable: [@agent]
2. **[Prioridad 2]** - Responsable: [@agent]
3. **[Prioridad 3]** - Responsable: [@agent]

### Tests A/B Planificados
- [ ] [Test 1]
- [ ] [Test 2]

### Contenido a Producir
- [ ] [Contenido 1]
- [ ] [Contenido 2]

### Budget Allocation
| Canal | % Budget | Monto |
|-------|----------|-------|
| Meta Ads | [X%] | $[X] |
| [Otro] | [X%] | $[X] |

---

## 📋 CHECKLIST DE CIERRE

- [ ] Métricas actualizadas en dashboard
- [ ] Auditoría semanal ejecutada
- [ ] Issues críticos escalados
- [ ] Plan de próxima semana aprobado
- [ ] Budget revisado y ajustado

---

*Próximo reporte: [fecha]*
*Generado por NGX Marketing Command Center*
```

### 3. Output

**Si format=markdown:**
Guardar en: `outputs/reports/$(date +%Y-%m-%d)-weekly-report.md`

**Si format=html:**
Generar versión HTML con estilo NGX (dark mode, violeta #6D00FF)
Guardar en: `outputs/reports/$(date +%Y-%m-%d)-weekly-report.html`

### 4. Notificaciones

Después de generar el reporte:
- Si hay métricas rojas (bajo objetivo): Destacar en resumen ejecutivo
- Si hay issues críticos de auditoría: Incluir call-to-action
- Sugerir acciones específicas para cada problema identificado

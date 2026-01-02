---
description: Ejecuta auditoría semanal completa de todas las páginas críticas del funnel NGX y genera dashboard actualizado
arguments:
  - name: urls
    description: Lista de URLs a auditar (separadas por coma) o "default" para URLs estándar
    default: default
  - name: compare
    description: Comparar con auditoría anterior (true|false)
    default: true
---

# Auditoría Semanal NGX - $(date +%Y-%m-%d)

Ejecutando auditoría semanal completa del funnel NGX.

---

## URLs a Auditar

### Si urls = default
Auditar las siguientes URLs críticas:

1. **Landing Principal GENESIS**
   - URL: https://ngxgenesis.com
   - Tipo: landing
   
2. **Landing Stress Signature Analyzer**
   - URL: https://ngxgenesis.com/stress-signature
   - Tipo: landing
   
3. **Landing NGX Transform**
   - URL: https://ngxgenesis.com/transform
   - Tipo: landing
   
4. **Landing LOGOS Dictionary**
   - URL: https://ngxgenesis.com/logos-dictionary
   - Tipo: landing
   
5. **Landing Metabolic Age Calculator**
   - URL: https://ngxgenesis.com/metabolic-age
   - Tipo: landing
   
6. **Checkout ASCEND**
   - URL: https://ngxgenesis.com/checkout/ascend
   - Tipo: checkout
   
7. **Checkout HYBRID**
   - URL: https://ngxgenesis.com/checkout/hybrid
   - Tipo: checkout

### Si urls = custom
Auditar las URLs proporcionadas: $ARGUMENTS.urls

---

## Proceso de Auditoría

Para cada URL, @funnel-auditor debe:

1. **Ejecutar auditoría completa** (type=landing o type=checkout según corresponda)
2. **Capturar métricas** de cada categoría
3. **Identificar issues** clasificados por severidad
4. **Registrar scores** para tracking histórico

---

## Comparación con Auditoría Anterior

Si compare = true:
1. Cargar última auditoría de `outputs/audits/`
2. Comparar scores por categoría
3. Identificar:
   - 📈 Mejoras (score subió >5 puntos)
   - 📉 Regresiones (score bajó >5 puntos)
   - ➡️ Sin cambio
4. Alertar si algún score bajó >10 puntos

---

## Output Esperado

### 1. Reportes Individuales
Guardar en: `outputs/audits/$(date +%Y-%m-%d)-[nombre-pagina]-audit.md`

### 2. Reporte Consolidado
Guardar en: `outputs/audits/$(date +%Y-%m-%d)-weekly-summary.md`

Incluir:
```markdown
# AUDITORÍA SEMANAL NGX - [Fecha]

## Resumen Ejecutivo

| Página | Score | Δ vs Anterior | Status |
|--------|-------|---------------|--------|
| [página] | [X]/100 | [±X] | 🟢/🟡/🔴 |

## Score Promedio del Funnel: [X]/100

## Top 3 Issues Críticos del Funnel
1. [Issue 1] - Página: [X] - Impacto: [descripción]
2. [Issue 2] - ...
3. [Issue 3] - ...

## Top 3 Mejoras vs Semana Anterior
1. [Mejora 1] - Página: [X]
2. [Mejora 2] - ...
3. [Mejora 3] - ...

## Acciones Requeridas Esta Semana
- [ ] [Acción 1]
- [ ] [Acción 2]
- [ ] [Acción 3]
```

### 3. Actualizar Dashboard
Actualizar el archivo: `dashboards/funnel-audit-dashboard.html`

Con los nuevos datos para:
- Gráfico de scores históricos
- Tabla de status actual
- Alertas activas
- Tendencias

---

## Notificaciones

Si alguna página tiene:
- Score < 60: 🔴 ALERTA CRÍTICA
- Score bajó >10 puntos: 🔴 ALERTA DE REGRESIÓN
- Issues críticos nuevos: 🟡 REQUIERE ATENCIÓN

Documentar alertas en el reporte y considerar notificación inmediata.

---

## Programación

Esta auditoría debería ejecutarse:
- **Frecuencia:** Semanal (cada lunes)
- **Hora sugerida:** 9:00 AM (antes de inicio de semana laboral)

Para programar con Claude in Chrome:
"Schedule this audit to run every Monday at 9:00 AM"

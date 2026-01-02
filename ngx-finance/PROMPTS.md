# NGX Finance — Prompts Probados

> Prompts optimizados para tareas financieras frecuentes.

---

## 1. Monthly P&L

```
Genera el P&L (Profit & Loss) de [MES].

Ingresos:
- ASCEND: [N] clientes × $100 = $[X]
- HYBRID: [N] temporadas × $1,200 = $[X]
- B2B Coaches: [N] × $299 = $[X]
- Otros: $[X]

Gastos:
- Infraestructura (GCP, Supabase, Vercel): $[X]
- APIs IA (Anthropic, Google, ElevenLabs): $[X]
- Marketing (Ads): $[X]
- Servicios (dominios, tools): $[X]
- Otros: $[X]

Genera:
1. P&L estructurado con totales
2. Margen bruto y neto
3. Comparación vs mes anterior
4. Notas sobre variaciones significativas
5. Recomendaciones si hay problemas

Formato: Tabla estructurada + análisis.
```

---

## 2. Runway Calculation

```
Calcula el runway actual de NGX.

Datos:
- Caja actual: $[X]
- MRR actual: $[X]
- Burn rate mensual: $[X]
- Crecimiento MRR esperado: [X%]/mes

Genera:
1. Runway en meses (sin crecimiento)
2. Runway ajustado (con crecimiento proyectado)
3. Fecha estimada de break-even
4. Fecha crítica (6 meses antes de quedarse sin caja)
5. Recomendaciones: qué hacer si runway < 12 meses

Formato: Análisis claro con números y fechas.
```

---

## 3. Financial Projection

```
Crea proyección financiera a [N] meses.

Supuestos:
- Clientes actuales: [N]
- Crecimiento mensual esperado: [X%]
- Churn mensual: [X%]
- CAC promedio: $[X]
- Presupuesto marketing: $[X]/mes

Genera 3 escenarios:
1. **Conservador** (50% del objetivo)
2. **Base** (objetivo)
3. **Optimista** (150% del objetivo)

Para cada escenario incluir:
- MRR mes a mes
- Clientes acumulados
- Gastos proyectados
- P&L proyectado
- Break-even estimado

Formato: Tabla con los 3 escenarios + gráfico si posible.
```

---

## 4. Budget Review

```
Revisa el presupuesto de [PERÍODO].

Presupuesto:
[LISTA DE CATEGORÍAS CON MONTOS]

Gastos reales:
[LISTA DE GASTOS POR CATEGORÍA]

Analiza:
1. Variación por categoría (% sobre/bajo presupuesto)
2. Categorías problemáticas (>10% variación)
3. Tendencia vs meses anteriores
4. Recomendaciones de ajuste
5. Alertas si hay riesgo

Formato: Tabla comparativa + análisis.
```

---

## 5. Unit Economics Analysis

```
Analiza los unit economics de NGX.

Datos:
- Precio promedio por cliente: $[X]
- CAC (costo de adquisición): $[X]
- Churn mensual: [X%]
- Costo variable por cliente/mes: $[X]
- Costo fijo mensual: $[X]

Calcula:
1. LTV (Lifetime Value)
2. LTV:CAC ratio
3. Payback period
4. Margen de contribución
5. Break-even en clientes

Evalúa:
- ¿El modelo es viable? (LTV:CAC > 3)
- ¿Payback es aceptable? (< 12 meses)
- ¿Qué palancas mover para mejorar?

Formato: Análisis con números y recomendaciones.
```

---

## 6. Invoice Creation

```
Genera factura para:

Cliente: [NOMBRE]
Email: [EMAIL]
Concepto: [PRODUCTO/SERVICIO]
Monto: $[X] USD
Período: [FECHAS]
Método de pago: [MÉTODO]

Incluye:
1. Número de factura (formato: NGX-YYYYMM-NNN)
2. Fecha de emisión
3. Datos de NGX
4. Datos del cliente
5. Desglose de servicios
6. Total
7. Instrucciones de pago
8. Términos y condiciones básicos

Formato: Markdown estructurado para convertir a PDF.
```

---

## 7. Cost Optimization

```
Analiza oportunidades de optimización de costos.

Gastos actuales por categoría:
[LISTA DE GASTOS]

Para cada categoría evalúa:
1. ¿Es esencial o nice-to-have?
2. ¿Hay alternativa más barata?
3. ¿Se puede negociar mejor precio?
4. ¿Se puede reducir uso?
5. Ahorro potencial

Prioriza por:
- Impacto (ahorro potencial)
- Esfuerzo (facilidad de implementar)
- Riesgo (qué se pierde)

Output: Lista priorizada de optimizaciones con ROI estimado.
```

---

## 8. Revenue Forecast

```
Genera forecast de ingresos para [PERÍODO].

Datos actuales:
- Clientes por producto: [DESGLOSE]
- Pipeline de ventas: [LISTA]
- Tasa de conversión histórica: [X%]
- Churn esperado: [X%]

Considera:
- Estacionalidad (si aplica)
- Lanzamientos planeados
- Cambios de pricing
- Capacidad de entrega

Genera:
1. Forecast mensual por producto
2. Total proyectado
3. Rango de confianza (pesimista - optimista)
4. Supuestos clave
5. Riesgos al forecast

Formato: Tabla + análisis de supuestos.
```

---

## 9. Cash Flow Projection

```
Proyecta el flujo de caja para [PERÍODO].

Caja inicial: $[X]

Entradas esperadas:
- Ingresos recurrentes: $[X]/mes
- Ventas nuevas proyectadas: $[X]/mes
- Otros: $[X]

Salidas esperadas:
- Gastos fijos: $[X]/mes
- Gastos variables: $[X]/mes
- Inversiones planeadas: $[X]

Genera:
1. Flujo de caja mensual
2. Saldo acumulado mes a mes
3. Punto más bajo de caja
4. Alertas si hay riesgo de caja negativa
5. Recomendaciones

Formato: Tabla mes a mes + análisis.
```

---

## 10. Investment Analysis

```
Analiza la inversión en [PROYECTO/HERRAMIENTA].

Inversión requerida: $[X]
Inversión recurrente: $[X]/mes

Beneficios esperados:
- Ahorro de tiempo: [X] horas/mes
- Aumento de conversión: [X%]
- Reducción de churn: [X%]
- Otros: [DESCRIBIR]

Calcula:
1. ROI a 6 y 12 meses
2. Payback period
3. NPV (si aplica)
4. Análisis de sensibilidad

Recomendación:
- ¿Invertir ahora, después, o no invertir?
- Condiciones para reconsiderar

Formato: Análisis estructurado con recomendación clara.
```

---

*Usar estos prompts como base y adaptar según necesidad.*

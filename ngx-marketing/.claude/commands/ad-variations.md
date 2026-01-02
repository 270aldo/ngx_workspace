---
description: Genera múltiples variaciones de copy para ads de Meta (Facebook/Instagram)
arguments:
  - name: objective
    description: Objetivo de campaña (awareness|leads|conversions)
    required: true
  - name: lead_magnet
    description: Lead magnet a promocionar (stress-signature|ngx-transform|logos-dictionary|metabolic-age|recovery-score|sleep-guide|product)
    required: true
  - name: variations
    description: Número de variaciones a generar
    default: 5
  - name: audience
    description: Audiencia target (30-45|45-60)
    default: 30-45
---

# Generación de Variaciones de Ads

**Objetivo:** $ARGUMENTS.objective
**Lead Magnet:** $ARGUMENTS.lead_magnet
**Variaciones:** $ARGUMENTS.variations
**Audiencia:** $ARGUMENTS.audience

---

## Instrucciones para @ads-specialist

Genera variaciones de ads para testing A/B siguiendo estas especificaciones:

### Framework de Variación

Para cada ad, generar variaciones en:

1. **Hook (Primera línea)**
   - Variación A: Pregunta confrontacional
   - Variación B: Declaración provocadora
   - Variación C: Dato/número impactante
   - Variación D: Historia personal
   - Variación E: Mito desmentido

2. **Angle (Enfoque del mensaje)**
   - Pain: Enfocado en el problema
   - Gain: Enfocado en el beneficio
   - Logic: Enfocado en la razón/datos
   - Fear: Enfocado en consecuencia de no actuar
   - Social: Enfocado en prueba social

### Configuración por Lead Magnet

**stress-signature:**
- Agente: SPARK
- Pain point: Estrés saboteando resultados
- Gain: Control de energía
- Audiencia natural: 30-45

**ngx-transform:**
- Agente: BLAZE
- Pain point: No ver resultados
- Gain: Visualizar transformación
- Audiencia natural: 30-45

**metabolic-age:**
- Agente: METABOL
- Pain point: Envejecimiento acelerado
- Gain: Rejuvenecimiento metabólico
- Audiencia natural: 45-60

**logos-dictionary:**
- Agente: LOGOS
- Pain point: Confusión/desinformación
- Gain: Conocimiento = poder
- Audiencia natural: Ambas

**product (ASCEND/HYBRID):**
- Agente: GENESIS
- Pain point: Programas genéricos
- Gain: Sistema personalizado
- Mostrar value stack

### Formato de Output

```markdown
# VARIACIONES DE ADS: [Lead Magnet]

**Objetivo:** [objetivo]
**Audiencia:** [audiencia]
**Fecha:** [fecha]

---

## VARIACIÓN 1: [Nombre del angle]

### Primary Text
[Hook - primera línea]

[Body - 2-3 líneas de agitación]

[Solución - 1-2 líneas]

[CTA]

### Headlines (3 opciones)
1. [Headline A]
2. [Headline B]
3. [Headline C]

### Description
[30 caracteres]

### Notas
- Angle: [pain|gain|logic|fear|social]
- Hook type: [pregunta|declaración|dato|historia|mito]
- Creativo sugerido: [descripción]

---

## VARIACIÓN 2: [Nombre del angle]
...

---

## MATRIZ DE TESTING RECOMENDADA

| Test | Variable | Control | Variante |
|------|----------|---------|----------|
| 1 | Hook | Var 1 | Var 2 |
| 2 | Angle | Pain | Gain |
| 3 | CTA | [A] | [B] |

## MÉTRICAS OBJETIVO

| Métrica | Target |
|---------|--------|
| CTR | >1.5% |
| CPL | <$[X] |
| Relevance | >7 |

## PRESUPUESTO DE TEST SUGERIDO

- Por variación: $20-30
- Duración mínima: 3-5 días
- Audiencia mínima: 1,000 impresiones
```

### Reglas de Copy

**Adaptación 30-45:**
- Tratamiento: Tú
- Tono: Directo, coloquial
- Énfasis: Eficiencia, datos
- Ejemplo hook: "Tu app de fitness no tiene idea de que dormiste mal."

**Adaptación 45-60:**
- Tratamiento: Usted
- Tono: Respetuoso, profesional
- Énfasis: Seguridad, longevidad
- Ejemplo hook: "Después de los 45, su cuerpo necesita un sistema que lo entienda."

### Output

Guardar en: `outputs/ads/$(date +%Y-%m-%d)-$ARGUMENTS.lead_magnet-variations.md`

---
description: Genera una secuencia de email B2B para outreach o follow-up
arguments:
  - name: type
    description: Tipo de secuencia (outreach|post-connection|post-demo|nurture|reengagement)
    required: true
  - name: prospect
    description: Nombre del prospect (para secuencias individuales)
  - name: industry
    description: Industria/nicho del prospect (crossfit|funcional|nutricion|etc)
  - name: pain_point
    description: Dolor principal a destacar
  - name: days
    description: Número de días de la secuencia
    default: "7"
---

# Secuencia de Email B2B

**Tipo:** $ARGUMENTS.type
**Prospect:** $ARGUMENTS.prospect
**Industria:** $ARGUMENTS.industry
**Dolor principal:** $ARGUMENTS.pain_point
**Duración:** $ARGUMENTS.days días

---

## Instrucciones para @b2b-email-architect

Genera una secuencia de email B2B completa siguiendo los principios:

### Diferencias B2B vs B2C
- Tono: Peer-to-peer, consultivo
- Longitud: 50-150 palabras máximo
- CTA: Agendar llamada o responder
- Frecuencia: Máximo 2-3 emails/semana

### Según el tipo:

**outreach** → Secuencia de prospección fría (5 emails, 14 días)
1. Día 1: Abrir la puerta (referencia a su contenido)
2. Día 4: Agregar valor sin pedir nada
3. Día 7: Provocar curiosidad
4. Día 10: Social proof
5. Día 14: Breakup email

**post-connection** → Post aceptación de LinkedIn (3 emails, 7 días)
1. Día 1: Agradecer + pregunta de valor
2. Día 3: Insight relevante
3. Día 7: Soft pitch para llamada

**post-demo** → Follow-up después de demo (4 emails, 10 días)
1. Día 0: Resumen + one-pager
2. Día 3: Abordar objeción principal
3. Día 6: Urgencia suave (escasez real)
4. Día 10: Última oportunidad

**nurture** → Largo plazo para no-listos (1/semana)
- Emails de valor puro
- Insights, tips, case studies
- Sin venta directa

**reengagement** → Reactivar prospects fríos (3 emails, 7 días)
1. Día 1: Check-in casual
2. Día 4: Nuevo ángulo/valor
3. Día 7: Cerrar archivo

### Cada email debe incluir:
- Subject line (<50 caracteres)
- Body (<150 palabras)
- CTA claro
- Firma simple

### Personalización:
- Si hay nombre de prospect, personalizar cada email
- Si hay industria, adaptar ejemplos y lenguaje
- Si hay dolor, enfocarse en él

---

## Output

Guarda en: `outputs/emails/$(date +%Y-%m-%d)-$ARGUMENTS.type-sequence.md`

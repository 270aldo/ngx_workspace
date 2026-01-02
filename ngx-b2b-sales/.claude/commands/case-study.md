---
description: Genera un case study de un Founding Coach para usar como social proof
arguments:
  - name: coach
    description: Nombre del coach
    required: true
  - name: type
    description: Tipo de case study (full|linkedin|quote|video-script)
    default: full
  - name: results
    description: Resultados principales logrados
    required: true
  - name: timeframe
    description: Tiempo usando NGX
  - name: before_clients
    description: Número de clientes antes
  - name: after_clients
    description: Número de clientes después
---

# Case Study

**Coach:** $ARGUMENTS.coach
**Tipo:** $ARGUMENTS.type
**Resultados:** $ARGUMENTS.results
**Tiempo con NGX:** $ARGUMENTS.timeframe
**Clientes antes:** $ARGUMENTS.before_clients
**Clientes después:** $ARGUMENTS.after_clients

---

## Instrucciones para @case-study-creator

Genera el case study según el tipo solicitado:

### Tipos:

**full** → Case study completo (1-2 páginas)
- Resumen con métricas
- El coach (background)
- El desafío (situación + problemas)
- La solución (por qué NGX + implementación)
- Los resultados (métricas + impacto cualitativo)
- La transformación (antes vs después)
- Consejo para otros coaches
- CTA

**linkedin** → Post de LinkedIn con case study
- Formato corto (600-900 caracteres)
- Hook → Problema → Resultados → Quote → CTA
- Optimizado para engagement

**quote** → Testimoniales extraídos
- Quote corto (para ads, <20 palabras)
- Quote medio (para propuestas, 2-3 frases)
- Quote largo (para case study, 4-5 frases)
- Atribución completa

**video-script** → Guión para testimonial en video
- 60-90 segundos
- Estructura: Intro → Problema → Solución → Resultados → Cierre
- Notas de producción

### Datos necesarios:
- Si no tengo todos los datos, usar placeholders [X]
- Indicar qué información falta para completar

### Tono:
- Auténtico, no publicitario
- Enfocado en la transformación
- Con datos concretos siempre que sea posible

---

## Output

Guarda en: `outputs/case-studies/$(date +%Y-%m-%d)-$ARGUMENTS.coach-$ARGUMENTS.type.md`

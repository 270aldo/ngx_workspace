---
description: Genera un script de llamada de venta personalizado para un prospect
arguments:
  - name: type
    description: Tipo de llamada (discovery|demo|close|followup)
    required: true
  - name: prospect
    description: Nombre del prospect
    required: true
  - name: pain_points
    description: Dolores identificados del prospect
  - name: tools_used
    description: Herramientas que usa actualmente
  - name: objections
    description: Objeciones anticipadas
---

# Script de Llamada de Venta

**Tipo:** $ARGUMENTS.type
**Prospect:** $ARGUMENTS.prospect
**Dolores:** $ARGUMENTS.pain_points
**Herramientas actuales:** $ARGUMENTS.tools_used
**Objeciones anticipadas:** $ARGUMENTS.objections

---

## Instrucciones para @sales-script-writer

Genera un script de llamada completo siguiendo la metodología NGX B2B:

### Principio Fundamental
> NO vendemos en la primera llamada. Creamos CHAMPIONS.

### Según el tipo de llamada:

**discovery** → Script de descubrimiento (20-30 min)
- Foco en conectar y entender dolor
- NO mencionar producto en detalle
- Terminar con cita para demo

**demo** → Script de demostración (30-45 min)
- Recap de dolor
- Visión del futuro
- Demo en vivo
- Presentar oferta Founding Coaches
- Manejar objeciones

**close** → Script de cierre (15-20 min)
- Resolver últimas dudas
- Presentar términos finales
- Cerrar el deal

**followup** → Script de re-engagement (10-15 min)
- Reconectar después de silencio
- Identificar qué cambió
- Re-calificar interés

### Personalización requerida:
- Usar nombre del prospect
- Incorporar dolores específicos
- Mencionar herramientas que usa
- Preparar respuestas a objeciones anticipadas

---

## Output

Guarda en: `outputs/scripts/$(date +%Y-%m-%d)-$ARGUMENTS.prospect-$ARGUMENTS.type-script.md`

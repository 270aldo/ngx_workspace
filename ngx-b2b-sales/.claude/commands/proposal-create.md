---
description: Genera una propuesta comercial personalizada para un prospect B2B
arguments:
  - name: prospect
    description: Nombre del prospect
    required: true
  - name: type
    description: Tipo de documento (one-pager|proposal|comparison|roi)
    default: proposal
  - name: tier
    description: Tier de oferta (founding|regular|studio)
    default: founding
  - name: pain_points
    description: Dolores específicos identificados
  - name: competitor
    description: Competidor a comparar (para type=comparison)
---

# Propuesta Comercial B2B

**Prospect:** $ARGUMENTS.prospect
**Tipo:** $ARGUMENTS.type
**Tier:** $ARGUMENTS.tier
**Dolores:** $ARGUMENTS.pain_points
**Competidor:** $ARGUMENTS.competitor

---

## Instrucciones para @proposal-architect

Genera el documento de venta siguiendo los templates definidos:

### Según el tipo:

**one-pager** → 1 página con resumen visual
- Problema → Solución → Lo que incluye → Oferta
- Para compartir internamente
- CTA claro

**proposal** → Propuesta formal 2-3 páginas
- Resumen ejecutivo personalizado
- Situación actual vs con NGX
- Solución detallada
- Inversión y términos
- Próximos pasos
- FAQs

**comparison** → Comparativa vs competidor
- Tabla comparativa
- Diferenciadores clave
- Ejemplo concreto de la diferencia

**roi** → Calculadora de ROI
- Inversión
- Tiempo ahorrado
- Clientes adicionales posibles
- Revenue proyectado
- Payback period

### Según el tier:

**founding** → Oferta Founding Coaches
- Piloto: $0 (3 meses)
- Post-piloto: $199/mes
- Setup: $299
- Hasta 30 clientes

**regular** → Oferta precio regular
- $299/mes
- Setup: $499
- Hasta 30 clientes

**studio** → Oferta para estudios
- $500-1,500/mes
- White-label disponible
- Múltiples coaches

### Personalización requerida:
- Nombre del prospect en todo el documento
- Dolores específicos mencionados en llamadas
- Herramientas actuales que usa
- Responder objeciones que planteó

---

## Output

Guarda en: `outputs/proposals/$(date +%Y-%m-%d)-$ARGUMENTS.prospect-$ARGUMENTS.type.md`

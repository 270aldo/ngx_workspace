---
description: Califica un lead para determinar si es candidato HYBRID o ASCEND
arguments:
  - name: name
    description: Nombre del lead
    required: true
  - name: source
    description: Fuente del lead (lead_magnet, ad, organic, referral)
    default: lead_magnet
  - name: lead_magnet
    description: Lead magnet que descargó (si aplica)
    required: false
  - name: notes
    description: Notas adicionales sobre el lead
    required: false
---

# Calificación de Lead HYBRID vs ASCEND

**Lead:** $ARGUMENTS.name
**Fuente:** $ARGUMENTS.source
**Lead Magnet:** $ARGUMENTS.lead_magnet
**Notas:** $ARGUMENTS.notes

---

## Instrucciones para @hybrid-sales-agent

Genera una calificación completa usando el siguiente framework:

### 1. ANÁLISIS INICIAL

Basándote en la fuente y lead magnet, evalúa:

**Señales iniciales de HYBRID:**
- Lead magnets de transformación (NGX Transform, Metabolic Age)
- Fuentes de alto intent (referral, búsqueda directa)
- Menciones de frustración o intentos previos

**Señales iniciales de ASCEND:**
- Lead magnets educativos (LOGOS Dictionary)
- Fuentes de curiosidad (contenido orgánico)
- Perfil tech-savvy

### 2. PREGUNTAS DE CALIFICACIÓN SUGERIDAS

Genera 5 preguntas personalizadas para este lead específico que ayuden a determinar:
1. Historial de intentos previos
2. Nivel de autodisciplina
3. Necesidad de accountability
4. Presupuesto disponible
5. Urgencia/motivación

### 3. SCORING PRELIMINAR

| Criterio | Puntos | Evaluación |
|----------|--------|------------|
| Múltiples fracasos previos | 0-3 | [Evaluar] |
| Autodisciplina baja | 0-2 | [Evaluar] |
| Prefiere guía | 0-3 | [Evaluar] |
| Presupuesto $200+ | 0-2 | [Evaluar] |
| Evento de vida urgente | 0-2 | [Evaluar] |
| Edad 45+ | 0-1 | [Evaluar] |
| Condición de salud | 0-1 | [Evaluar] |

**SCORE PRELIMINAR:** [X]/14

### 4. RECOMENDACIÓN

- 0-4 puntos → **ASCEND** (nurture con contenido educativo)
- 5-8 puntos → **HYBRID CANDIDATO** (agendar llamada de calificación)
- 9+ puntos → **HYBRID FUERTE** (agendar llamada de venta)

### 5. SIGUIENTE PASO SUGERIDO

[Acción específica: email, llamada, nurture sequence]

### 6. SCRIPT DE PRIMER CONTACTO

[Mensaje personalizado para este lead según su perfil]

---

## Output

Guarda en: `outputs/hybrid/$(date +%Y-%m-%d)-$ARGUMENTS.name-qualification.md`

---
description: Planifica el calendario de contenido para la próxima semana
arguments:
  - name: audience
    description: Audiencia objetivo (30-45|45-60|ambas)
    default: ambas
  - name: focus
    description: Foco del contenido (awareness|nurture|conversion|balanced)
    default: balanced
  - name: lead_magnet
    description: Lead magnet a destacar esta semana (opcional)
    required: false
  - name: agent
    description: Agente NGX a protagonizar (opcional)
    required: false
---

# Planificación de Contenido Semanal

**Semana:** $(date +%Y-%m-%d) - $(date -d "+6 days" +%Y-%m-%d)
**Audiencia:** $ARGUMENTS.audience
**Foco:** $ARGUMENTS.focus
**Lead Magnet destacado:** $ARGUMENTS.lead_magnet
**Agente protagonista:** $ARGUMENTS.agent

---

## Instrucciones para @content-strategist

Genera un calendario de contenido para la próxima semana considerando:

### Distribución por Modo
- **Modo B (Verdad):** 40% - Hooks, captar atención
- **Modo A (Experto):** 35% - Educar, generar entendimiento
- **Modo C (Arquitecto):** 25% - Mostrar sistema, convertir

### Distribución por Canal
| Canal | Posts/Semana | Formatos |
|-------|--------------|----------|
| Instagram | 5-7 | Reels, Carruseles, Stories |
| Facebook | 3-4 | Posts largos, Videos |
| LinkedIn | 2-3 | Posts narrativos |
| Email | 2-3 | Newsletter, Nurture |

### Ajustes por Foco

**Si focus = awareness:**
- Priorizar Modo B
- Más contenido en IG y TikTok
- Hooks confrontacionales
- Lead magnets como CTA

**Si focus = nurture:**
- Priorizar Modo A
- Más contenido educativo largo
- Email como canal principal
- Conexión con agentes específicos

**Si focus = conversion:**
- Priorizar Modo C
- Más contenido de producto
- Testimoniales y casos de uso
- CTAs hacia ASCEND/HYBRID

**Si focus = balanced:**
- Distribución equitativa
- Mezcla de formatos
- Cobertura de todo el funnel

### Consideraciones de Audiencia

**Si audience = 30-45:**
- Tono: Tú, directo
- Canales: Instagram, TikTok
- Temas: Eficiencia, datos, resultados
- Lead magnets: Stress Signature, NGX Transform

**Si audience = 45-60:**
- Tono: Usted, respetuoso
- Canales: Facebook, LinkedIn
- Temas: Longevidad, prevención, credibilidad
- Lead magnets: Metabolic Age, Sleep Guide

---

## Output Esperado

Genera el calendario en formato:

```markdown
## CALENDARIO DE CONTENIDO
### Semana [fecha] - [fecha]

#### Lunes [fecha]
| Hora | Canal | Tipo | Modo | Tema | Hook | CTA |
|------|-------|------|------|------|------|-----|
| 10:00 | IG | Reel | B | [tema] | [hook] | [cta] |
| 14:00 | FB | Post | A | [tema] | [hook] | [cta] |

#### Martes [fecha]
...

### Notas de Producción
- [Assets necesarios]
- [Conexiones entre piezas]
- [Consideraciones especiales]

### Métricas Objetivo
- Reach objetivo: [X]
- Engagement objetivo: [X%]
- Leads objetivo: [X]
```

Guarda el calendario en: `outputs/content/$(date +%Y-%m-%d)-content-calendar.md`

---

## Después de la Planificación

Una vez aprobado el calendario, delega la ejecución:
- Copy de posts → @social-creator
- Secuencias de email → @email-architect
- Copy de ads si hay → @ads-specialist

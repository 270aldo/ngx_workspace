---
description: Genera un batch de posts para redes sociales optimizados para cada plataforma
arguments:
  - name: platform
    description: Plataforma objetivo (instagram|facebook|linkedin|tiktok|all)
    required: true
  - name: count
    description: Número de posts a generar
    default: 5
  - name: theme
    description: Tema o pilar (training|nutrition|mindset|system|mixed)
    default: mixed
  - name: audience
    description: Audiencia target (30-45|45-60|both)
    default: both
  - name: formats
    description: Formatos a incluir (reels|carousels|posts|stories|all)
    default: all
---

# Generación de Batch de Contenido Social

**Plataforma:** $ARGUMENTS.platform
**Cantidad:** $ARGUMENTS.count posts
**Tema:** $ARGUMENTS.theme
**Audiencia:** $ARGUMENTS.audience
**Formatos:** $ARGUMENTS.formats

---

## Instrucciones para @social-creator

Genera un batch de contenido social siguiendo estas especificaciones:

### Distribución de Modos
Para cada batch, asegurar:
- 40% Modo B (Verdad) — Hooks, captar atención
- 35% Modo A (Experto) — Educar
- 25% Modo C (Arquitecto) — Mostrar sistema

### Distribución de Agentes por Tema

**Si theme = training:**
- BLAZE (40%) — Fuerza, hipertrofia
- ATLAS (20%) — Movilidad, prevención
- TEMPO (20%) — Recuperación
- WAVE (20%) — Cardio

**Si theme = nutrition:**
- SAGE (40%) — Estrategia nutricional
- MACRO (30%) — Comidas prácticas
- METABOL (30%) — Salud metabólica

**Si theme = mindset:**
- SPARK (40%) — Hábitos
- STELLA (30%) — Mindset
- LUNA (30%) — Sueño

**Si theme = system:**
- GENESIS (50%) — Sistema completo
- LOGOS (50%) — Educación

**Si theme = mixed:**
- Distribuir equitativamente entre pilares

### Formato de Output por Post

```markdown
## POST [N] de [TOTAL]

**Plataforma:** [plataforma]
**Formato:** [reel|carousel|post|story]
**Modo:** [A|B|C]
**Agente:** [nombre]
**Audiencia:** [30-45|45-60]

---

### Contenido

[Si es REEL/TIKTOK:]
**Duración:** [X] segundos
**Hook (0-3s):** [texto]
**Script completo:**
```
[script con timestamps]
```
**Texto en pantalla:** [overlays sugeridos]
**Audio:** [sugerencia de música/voz]

[Si es CARRUSEL:]
**Slides:** [número]
**Slide 1 (Hook):** [texto + visual]
**Slide 2-N:** [contenido]
**Slide Final (CTA):** [texto]

[Si es POST:]
**Copy:**
[texto del post]

**Imagen sugerida:** [descripción]

[Para todos:]
**Caption:** [150-200 caracteres]
**Hashtags:** [3-5 relevantes]
**CTA:** [acción deseada]

---

**Notas de producción:**
- [Nota 1]
- [Nota 2]
```

### Reglas Específicas por Plataforma

**Instagram:**
- Reels: 7-30 segundos, hook en 0.5s
- Carruseles: 5-10 slides, primera slide impactante
- Caption: 150-200 chars + hashtags separados
- Hashtags: 3-5 relevantes (no spam)

**Facebook:**
- Posts más largos permitidos
- Tono formal para 45-60 (usted)
- Videos: 1-3 minutos educativos
- Links funcionan bien

**LinkedIn:**
- Tono profesional pero personal
- Historia de founder funciona
- Sin contenido "fitfluencer"
- Datos y resultados tangibles

**TikTok:**
- 15-60 segundos
- Autenticidad sobre producción
- Hook inmediato (0.3s)
- Trends adaptados a NGX

### Output Final

Guardar en: `outputs/social/$(date +%Y-%m-%d)-$ARGUMENTS.platform-batch.md`

Incluir:
1. Resumen del batch (posts por modo, por agente)
2. Todos los posts con formato completo
3. Calendario sugerido de publicación
4. Assets necesarios para producción

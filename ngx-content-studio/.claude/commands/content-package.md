# /content-package

Genera un paquete completo de contenido multi-formato desde un solo tema. Un topic → podcast clip + video + thumbnail + copy, todo coordinado visualmente.

## Uso

```
/content-package topic="Recuperación activa" --podcast-clip --reels --thumbnail --carousel
```

## Parámetros

| Parámetro | Requerido | Descripción |
|-----------|-----------|-------------|
| `topic` | ✅ | Tema central del contenido |
| `agents` | ❌ | Agentes a usar (default: auto-selección) |

### Flags de Contenido (incluir los que necesites)

| Flag | Output |
|------|--------|
| `--podcast-clip` | Clip de podcast 2-3 min con voice direction |
| `--podcast-full` | Episodio completo 10+ min |
| `--reels` | Video vertical 30-60s para IG/TikTok |
| `--youtube-short` | Video vertical optimizado YouTube |
| `--youtube-long` | Video horizontal 2-5 min |
| `--thumbnail` | Prompts para thumbnail |
| `--carousel` | Graphics para carrusel Instagram |
| `--linkedin-post` | Copy + graphic para LinkedIn |
| `--stories` | Serie de 3-5 stories |

## Ejemplos

### Paquete mínimo (clip + video + thumb)
```
/content-package topic="¿Por qué no ves resultados?" agents="BLAZE,SPARK" --podcast-clip --reels --thumbnail
```

### Paquete completo de campaña
```
/content-package topic="El mito de las 8 horas de sueño" agents="LUNA,TEMPO" --podcast-full --reels --youtube-short --thumbnail --carousel --linkedin-post
```

### Solo visual
```
/content-package topic="5 señales de sobreentrenamiento" agents="TEMPO" --reels --thumbnail --carousel
```

## Output

El comando genera un MEGA-PAQUETE organizado por tipo:

```
═══════════════════════════════════════════════════════════════════
CONTENT PACKAGE: [TOPIC]
═══════════════════════════════════════════════════════════════════

📋 RESUMEN
───────────────────────────────────────────────────────────────────
Topic: [Tema]
Agents: [Lista]
Formatos incluidos: [Lista de flags activados]
Tiempo estimado de producción: [X horas]

🎙️ PODCAST
═══════════════════════════════════════════════════════════════════
[Si --podcast-clip o --podcast-full]

## SCRIPT
[Script completo con timestamps]

## VOICE DIRECTION
[Segmentado por agente con tags ElevenLabs]

## DERIVED CONTENT
[Clips, quotes, descripción]

🎬 VIDEO - REELS/TIKTOK
═══════════════════════════════════════════════════════════════════
[Si --reels]

## CREATIVE BRIEF
[Objetivo, audience, message]

## STORYBOARD
[Frame por frame]

## SHOT LIST - PROMPTS VEO 3.1
[Prompts copy/paste ready]

## VOICE SCRIPT
[Si hay VO]

## POST-PRODUCTION NOTES
[Tips Premiere]

🎬 VIDEO - YOUTUBE
═══════════════════════════════════════════════════════════════════
[Si --youtube-short o --youtube-long]

[Mismo formato que Reels pero optimizado para YouTube]

🖼️ THUMBNAIL
═══════════════════════════════════════════════════════════════════
[Si --thumbnail]

## OPCIÓN A
[Prompt Nano Banana Pro]

## OPCIÓN B
[Prompt alternativo]

## TEXT OVERLAY
[Texto a agregar en post]

📱 CAROUSEL
═══════════════════════════════════════════════════════════════════
[Si --carousel]

## SLIDE 1 - COVER
[Prompt + texto]

## SLIDE 2-N - CONTENT
[Prompts + contenido]

## SLIDE FINAL - CTA
[Prompt + call to action]

💼 LINKEDIN
═══════════════════════════════════════════════════════════════════
[Si --linkedin-post]

## COPY
[Post completo]

## GRAPHIC PROMPT
[Imagen para acompañar]

📖 STORIES
═══════════════════════════════════════════════════════════════════
[Si --stories]

## STORY 1-5
[Contenido + prompt visual]

✍️ COPY PACKAGE (TODOS LOS FORMATOS)
═══════════════════════════════════════════════════════════════════

## TÍTULOS A/B
[Opciones de título]

## CAPTIONS POR PLATAFORMA
- Instagram: [...]
- TikTok: [...]
- YouTube: [...]
- LinkedIn: [...]

## HASHTAGS
[Sets por plataforma]

## DESCRIPCIÓN LARGA
[Para YouTube/Podcast]

📋 EXECUTION CHECKLIST
═══════════════════════════════════════════════════════════════════

□ Audio
  □ Generar en ElevenLabs
  □ Exportar WAV
  
□ Video Reels
  □ Shot 1 en VEO
  □ Shot 2 en VEO
  □ [...]
  □ Ensamblar en Premiere
  □ Export
  
□ Video YouTube
  □ [...]
  
□ Imágenes
  □ Thumbnail en Nano Banana
  □ Carousel slides
  
□ Publicación
  □ Subir a Instagram
  □ Subir a TikTok
  □ Subir a YouTube
  □ Publicar en LinkedIn
```

## Coherencia Visual

El paquete asegura coherencia entre todos los formatos:

- **Mismos agentes** aparecen en podcast, video, thumbnail
- **Mismo mensaje** adaptado a cada plataforma
- **Misma paleta** (#6D00FF) en todos los visuales
- **Mismo tono** (Verdad Directa) en todo el copy
- **Cross-references** — el video menciona el podcast, etc.

## Agent Auto-Selection

Si no especificas `agents`, se seleccionan automáticamente basado en el topic:

| Tema | Agentes Sugeridos |
|------|-------------------|
| Entrenamiento, fuerza | BLAZE, ATLAS |
| Nutrición | SAGE, MACRO |
| Sueño, recuperación | LUNA, TEMPO |
| Mindset, hábitos | STELLA, SPARK |
| Salud metabólica | METABOL, SAGE |
| Educativo general | LOGOS + especialista |
| Cardio | WAVE, TEMPO |
| Movilidad | NOVA, ATLAS |

## Workflow Sugerido

```
DÍA 1: PRODUCCIÓN
├── 1. Generar audio en ElevenLabs (30 min)
├── 2. Generar shots de video (1-2 horas)
├── 3. Generar imágenes (30 min)
└── 4. Ensamblar en Premiere (1-2 horas)

DÍA 2: PUBLICACIÓN
├── 1. Subir podcast (si aplica)
├── 2. Publicar Reels/TikTok
├── 3. Publicar YouTube
├── 4. Publicar LinkedIn
└── 5. Subir Stories
```

## Notas

- El paquete está diseñado para producción eficiente en batch
- Todos los prompts son copy/paste ready
- Los clips de podcast se identifican como momentos de alto engagement
- El thumbnail tiene múltiples opciones para A/B testing
- El copy está adaptado a las mejores prácticas de cada plataforma

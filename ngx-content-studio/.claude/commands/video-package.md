# /video-package

Genera un paquete completo de pre-producción de video con storyboard, shot list, y prompts listos para copiar/pegar en VEO 3.1, SORA 2 Pro, o Kling.

## Uso

```
/video-package topic="Introducción a TEMPO" platform=reels duration=30 engine=veo agents="TEMPO"
```

## Parámetros

| Parámetro | Requerido | Opciones | Default | Descripción |
|-----------|-----------|----------|---------|-------------|
| `topic` | ✅ | Texto libre | - | Tema/concepto del video |
| `platform` | ✅ | tiktok/reels/shorts/youtube/linkedin | - | Plataforma destino |
| `duration` | ❌ | Segundos | 30 | Duración objetivo |
| `engine` | ❌ | veo/sora/kling | veo | Engine de generación |
| `agents` | ❌ | Lista de agentes | NEXUS | Agentes que aparecen |
| `founder` | ❌ | true/false | false | Si Aldo aparece (fuerza sora) |
| `type` | ❌ | intro/ad/educational/testimonial | intro | Tipo de contenido |
| `voice` | ❌ | true/false | true | Si incluir voice script |

## Ejemplos

### Video intro de agente
```
/video-package topic="Conoce a BLAZE" platform=reels duration=30 engine=veo agents="BLAZE" type=intro
```

### Ad con fundador
```
/video-package topic="Por qué creé NGX" platform=youtube duration=60 founder=true type=testimonial
```

### Contenido educativo
```
/video-package topic="3 errores en tu recuperación" platform=tiktok duration=45 agents="TEMPO,LUNA" type=educational
```

### Video largo para YouTube
```
/video-package topic="El sistema de 13 agentes explicado" platform=youtube duration=180 agents="NEXUS,BLAZE,SAGE,LOGOS" type=educational
```

## Output

El comando genera un paquete completo:

### 1. Creative Brief
```
- Objetivo del video
- Target audience
- Key message (Performance + Longevity)
- Tone & style
- Platform specs
- Success metrics
```

### 2. Script
```
- Escenas numeradas
- Diálogo/VO exacto por escena
- Duración por escena
- Audio cues (música, SFX)
- Transiciones
```

### 3. Storyboard
```
Para cada shot:
┌─────────────────────────────────────────────┐
│ SHOT [#]                        [Duración]  │
├─────────────────────────────────────────────┤
│ VISUAL: [Qué se ve]                         │
│ CAMERA: [Tipo + movimiento]                 │
│ ACTION: [Qué sucede]                        │
│ AUDIO: [Diálogo, SFX, música]               │
│ TRANSITION: [A siguiente shot]              │
└─────────────────────────────────────────────┘
```

### 4. Shot List con Prompts (COPY/PASTE READY)
```
Para cada shot:
──────────────────────────────────────────────
SHOT [#] | [Duración] | Engine: [VEO/SORA/Kling]
──────────────────────────────────────────────
PROPÓSITO: [Para qué es este shot]

PROMPT (copiar completo):
"""
[Prompt optimizado listo para pegar]
"""

SETTINGS:
- Duration: [X] seconds
- Resolution: 1080p
- Aspect Ratio: [9:16/16:9]

REFERENCE IMAGES: [Si aplica]
──────────────────────────────────────────────
```

### 5. Voice Script (si voice=true)
```
- Script segmentado por escena
- Tags de emoción ElevenLabs
- Timing para sync con video
- Settings recomendados
```

### 6. Post-Production Notes
```
- Sequence settings Premiere
- Assembly order
- Transiciones sugeridas
- Color correction tips
- Audio levels
- Export settings
```

### 7. Copy Package
```
- Títulos A/B
- Caption por plataforma
- Hashtags
- Descripción
```

## Specs por Plataforma

| Plataforma | Aspect | Duración Óptima | Hook Time |
|------------|--------|-----------------|-----------|
| TikTok | 9:16 | 15-60s | 0.5s |
| Reels | 9:16 | 15-60s | 1s |
| Shorts | 9:16 | 15-60s | 1s |
| YouTube | 16:9 | Flexible | 3s |
| LinkedIn | 16:9 | 15-60s | 2s |

## Workflow de Ejecución

```
1. GENERACIÓN DE SHOTS
   └── Abrir VEO/SORA/Kling
   └── Copiar prompt del Shot 1
   └── Generar → Revisar → Aprobar o regenerar
   └── Repetir para cada shot
   └── Descargar todos los clips

2. AUDIO (si aplica)
   └── Copiar voice script a ElevenLabs
   └── Generar audio
   └── Exportar WAV

3. PREMIERE PRO
   └── Importar clips de video
   └── Importar audio
   └── Ensamblar según storyboard
   └── Aplicar transiciones
   └── Color correct (asegurar violeta consistente)
   └── Ajustar audio levels
   └── Agregar texto/graphics si necesario

4. EXPORT
   └── H.264, 15-20 Mbps
   └── AAC 320kbps

5. PUBLISH
   └── Subir a plataforma
   └── Copiar caption
   └── Agregar hashtags
```

## Engine Decision Guide

| Situación | Engine | Razón |
|-----------|--------|-------|
| Solo agentes NGX | VEO 3.1 | Mejor consistencia, audio nativo |
| Aldo aparece | SORA 2 | CAMEO feature |
| Shots de 25s+ | SORA 2 | Storyboard feature |
| Multi-elementos | Kling | Elements feature |
| Máxima consistencia | VEO 3.1 | JSON prompting |

## Notas

- Si `founder=true`, el engine se fuerza a SORA 2 Pro para usar CAMEO
- Videos >60s se dividen en múltiples shots para ensamblar
- Los prompts incluyen paleta NGX obligatoria (#6D00FF, sin cyan)
- Cada shot está diseñado para ser generado independientemente
- Las transiciones se aplican en post, no en generación

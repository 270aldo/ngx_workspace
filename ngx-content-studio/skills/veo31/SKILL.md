# Skill: VEO 3.1 Video Generation

---

## Overview

Skill para generar videos con Google VEO 3.1. Crea B-roll, clips promocionales, y contenido de video usando AI.

**Comando:** `/veo-generate`
**Alias:** `/veo`, `/video-gen`

---

## Triggers

Este skill se activa cuando el usuario:

- Menciona generar videos con AI
- Necesita B-roll o clips de video
- Pide contenido de video para redes
- Menciona VEO, Veo 3.1, o generación de video
- Necesita animaciones o motion graphics simples

---

## Capabilities

### Lo que puede hacer VEO 3.1

| Capacidad | Descripción | Duración Max |
|-----------|-------------|--------------|
| Text-to-Video | Generar video desde prompt | 8-16 segundos |
| Image-to-Video | Animar una imagen estática | 8 segundos |
| B-Roll Generation | Clips genéricos de apoyo | 4-8 segundos |
| Motion Graphics | Elementos animados simples | 4-8 segundos |
| Transitions | Transiciones personalizadas | 2-4 segundos |

### Estilos Soportados

- Cinematic (4K look)
- Documentary
- Commercial/Advertising
- Social Media (vertical)
- Abstract/Artistic
- Product showcase
- Lifestyle/Fitness
- Corporate/Professional

---

## Prompt Structure

### Template Base

```
[ESTILO]: [Descripción del estilo visual]
[SUBJECT]: [Qué/Quién aparece en el video]
[ACTION]: [Qué está pasando]
[SETTING]: [Dónde ocurre]
[CAMERA]: [Movimiento de cámara]
[MOOD]: [Atmósfera/Tono]
[LIGHTING]: [Tipo de iluminación]
[DURATION]: [Duración deseada]
```

### Ejemplo: B-Roll Fitness

```
ESTILO: Cinematic, 4K, shallow depth of field
SUBJECT: Athletic man in his 40s, wearing NGX branded gear
ACTION: Performing a deadlift with perfect form, slow motion
SETTING: Modern minimalist gym, dark moody atmosphere
CAMERA: Slow orbit around subject, low angle
MOOD: Powerful, determined, focused
LIGHTING: Dramatic side lighting, some lens flare
DURATION: 6 seconds
```

### Ejemplo: Producto

```
ESTILO: Commercial, clean, premium feel
SUBJECT: Smartphone displaying NGX GENESIS app
ACTION: App interface animating, showing workout data
SETTING: White/grey gradient background
CAMERA: Slow push in with subtle rotation
MOOD: Modern, tech-forward, aspirational
LIGHTING: Soft studio lighting, no harsh shadows
DURATION: 4 seconds
```

---

## Best Practices

### DO ✅

- Ser específico con detalles visuales
- Incluir movimiento de cámara
- Especificar iluminación
- Mencionar el estilo visual deseado
- Indicar la duración aproximada
- Describir la acción frame by frame si es compleja

### DON'T ❌

- Prompts vagos o genéricos
- Demasiados elementos en un solo clip
- Acciones muy complejas
- Texto legible en video (no confiable)
- Rostros específicos de personas reales
- Logos o marcas registradas

---

## Workflow de Generación

```
1. BRIEF
   └─ Definir objetivo del video
   └─ Identificar uso (social, web, ads)
   └─ Establecer duración total necesaria

2. SHOT LIST
   └─ Desglosar en clips individuales
   └─ Crear prompt para cada clip
   └─ Definir orden de edición

3. GENERATE
   └─ Ejecutar prompts en VEO
   └─ Generar 2-3 variaciones por clip
   └─ Seleccionar los mejores

4. REFINE
   └─ Ajustar prompts si necesario
   └─ Regenerar clips que no funcionan
   └─ Exportar en resolución final

5. POST-PRODUCTION
   └─ Color grading si necesario
   └─ Añadir audio/música
   └─ Integrar con footage real
```

---

## NGX Content Presets

### Preset: NGX Workout B-Roll

```
Base Settings:
- Style: Cinematic fitness
- Color: Warm blacks, purple accents (#6D00FF highlights)
- Camera: Dynamic, energetic
- Lighting: Gym lighting, dramatic

Prompt Template:
"Cinematic fitness footage, [ATHLETE TYPE] performing [EXERCISE],
modern gym environment with dark moody lighting, purple accent
lights, slow motion, shallow depth of field, 4K quality"
```

### Preset: NGX Tech/App

```
Base Settings:
- Style: Clean tech commercial
- Color: Dark backgrounds, vibrant UI
- Camera: Slow, controlled movements
- Lighting: Soft, studio quality

Prompt Template:
"Premium tech commercial style, smartphone/device showing
[APP SCREEN], floating in space with subtle rotation,
dark gradient background, soft glow, 4K quality"
```

### Preset: NGX Lifestyle

```
Base Settings:
- Style: Aspirational lifestyle
- Color: Warm, golden hour feel
- Camera: Smooth, steady
- Lighting: Natural, beautiful

Prompt Template:
"Lifestyle footage, [PERSON DESCRIPTION] [ACTIVITY],
[SETTING], golden hour lighting, cinematic look,
authentic and aspirational mood, 4K quality"
```

---

## Output Specifications

### Para Diferentes Plataformas

| Plataforma | Aspect Ratio | Resolución | FPS |
|------------|--------------|------------|-----|
| YouTube | 16:9 | 4K (3840x2160) | 24/30 |
| Instagram Reels | 9:16 | 1080x1920 | 30 |
| TikTok | 9:16 | 1080x1920 | 30 |
| Instagram Feed | 1:1 | 1080x1080 | 30 |
| Twitter/X | 16:9 | 1920x1080 | 30 |
| LinkedIn | 16:9 | 1920x1080 | 30 |

---

## Integration con Pipeline

### Conexión con Otros Skills

```
VEO 3.1 Output
     │
     ├──> /edit-video (post-producción)
     │
     ├──> /elevenlabs (añadir VO)
     │
     └──> /publish-content (programar)
```

### Archivo de Salida

Los videos generados se guardan en:
```
ngx-content-studio/
└── outputs/
    └── video/
        └── veo/
            └── [YYYY-MM-DD]/
                ├── clip_001_v1.mp4
                ├── clip_001_v2.mp4
                └── metadata.json
```

---

## Troubleshooting

| Issue | Causa Probable | Solución |
|-------|----------------|----------|
| Video borroso | Prompt demasiado complejo | Simplificar, un subject |
| Movimiento raro | Acción no clara | Describir paso a paso |
| Estilo incorrecto | Prompt genérico | Añadir referencias de estilo |
| Generación fallida | Contenido no permitido | Revisar políticas de uso |
| Duración corta | Límite de API | Dividir en múltiples clips |

---

## Ejemplo de Uso Completo

### Request
```
Usuario: "Necesito B-roll para un video de YouTube sobre NGX GENESIS.
Quiero mostrar a alguien entrenando con la app."
```

### Response
```
Voy a generar 4 clips de B-roll para tu video:

**Clip 1: Hero Shot**
Prompt: "Cinematic fitness footage, fit man in his 40s checking
smartphone app while resting between sets, modern dark gym,
purple accent lighting, shallow DOF, 4K, 6 seconds"

**Clip 2: Workout Action**
Prompt: "Athletic person performing dumbbell rows, side angle,
slow motion, dramatic lighting, moody gym atmosphere, 4K,
4 seconds"

**Clip 3: App Close-up**
Prompt: "Smartphone screen showing fitness app interface,
workout data animating, dark background with subtle purple
glow, clean tech commercial style, 4 seconds"

**Clip 4: Success/Results**
Prompt: "Person smiling looking at phone after workout,
satisfied expression, warm lighting, gym background out
of focus, aspirational mood, 4 seconds"

¿Quieres que genere estos clips o ajusto algo?
```

---

## Recursos

- [VEO Documentation](https://ai.google.dev/gemini-api/docs/video)
- [Best Practices Guide](#)
- [NGX Brand Guidelines](#)

---

*Skill VEO 3.1 Video Generation v1.0*

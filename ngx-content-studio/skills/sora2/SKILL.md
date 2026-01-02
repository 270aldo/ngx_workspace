# Skill: SORA 2 Video & Image Generation

---

## Overview

Skill para generar videos e imágenes con OpenAI SORA 2. Ideal para thumbnails, key visuals, y contenido visual de alta calidad.

**Comando:** `/sora-generate`
**Alias:** `/sora`, `/sora2`

---

## Triggers

Este skill se activa cuando el usuario:

- Necesita thumbnails para videos
- Quiere generar imágenes promocionales
- Pide key visuals para campañas
- Menciona SORA o generación de imágenes
- Necesita contenido visual conceptual
- Requiere visualizaciones abstractas

---

## Capabilities

### Video Generation

| Capacidad | Descripción | Especificaciones |
|-----------|-------------|------------------|
| Text-to-Video | Video desde descripción | Hasta 20 segundos |
| Extend | Alargar video existente | +5-10 segundos |
| Remix | Variar video existente | Misma duración |
| Storyboard | Generar secuencia | Múltiples clips |

### Image Generation

| Capacidad | Descripción | Resolución Max |
|-----------|-------------|----------------|
| Hero Images | Imágenes principales | 4K |
| Thumbnails | Miniaturas YouTube/Social | 1920x1080 |
| Social Graphics | Posts, Stories | Variable |
| Conceptual Art | Visualizaciones abstractas | 4K |

---

## Prompt Engineering

### Estructura Óptima para SORA

```
[MEDIUM]: Photo/Video/Illustration/3D Render
[SUBJECT]: Descripción detallada del sujeto principal
[ENVIRONMENT]: Entorno y contexto
[STYLE]: Estilo artístico/visual específico
[LIGHTING]: Condiciones de luz
[CAMERA]: Ángulo, lente, movimiento
[MOOD]: Atmósfera emocional
[TECHNICAL]: Especificaciones técnicas
```

### Ejemplo: Thumbnail YouTube

```
MEDIUM: Photorealistic digital art
SUBJECT: Muscular man in his 40s with determined expression,
         arms crossed, wearing dark athletic gear with subtle
         purple accents
ENVIRONMENT: Dark modern gym background, out of focus,
             with purple LED accent lighting
STYLE: YouTube thumbnail style, bold and eye-catching,
       high contrast
LIGHTING: Dramatic rim lighting from behind, soft fill
          from front
CAMERA: Medium close-up, slightly low angle for power
MOOD: Confident, powerful, inspiring
TECHNICAL: 1920x1080, centered composition,
           space for text on left side
```

### Ejemplo: Video Promocional

```
MEDIUM: Cinematic video footage
SUBJECT: Professional athlete using smartphone app,
         looking at screen with satisfied expression
ENVIRONMENT: High-end home gym, morning light streaming
             through windows, minimalist decor
STYLE: Premium commercial aesthetic, Apple-style
       production value
LIGHTING: Natural window light, soft and warm
CAMERA: Slow dolly in, shallow depth of field,
        4K cinematic
MOOD: Aspirational, calm, successful
TECHNICAL: 16:9, 24fps, 8 seconds duration
```

---

## NGX Visual Templates

### Template: YouTube Thumbnail

```
Configuración Base:
- Resolución: 1920x1080 (16:9)
- Estilo: Bold, high-contrast, click-worthy
- Colores: Dark backgrounds, purple accents (#6D00FF)
- Espacio para texto: 40% del área

Prompt Base:
"YouTube thumbnail style, [SUBJECT], dark moody background
with purple (#6D00FF) accent lighting, high contrast,
dramatic, eye-catching, space for text overlay on
[LEFT/RIGHT] side, 1920x1080"
```

### Template: Instagram Post

```
Configuración Base:
- Resolución: 1080x1080 (1:1) o 1080x1350 (4:5)
- Estilo: Premium, aspirational
- Colores: NGX brand palette
- Composición: Central subject

Prompt Base:
"Premium fitness lifestyle photography, [SUBJECT],
[ENVIRONMENT], professional lighting, Instagram-worthy
aesthetic, aspirational mood, high-end feel,
[ASPECT RATIO]"
```

### Template: Podcast Cover

```
Configuración Base:
- Resolución: 3000x3000 (1:1)
- Estilo: Clean, professional, recognizable
- Elementos: Guest photo area, branding
- Legibilidad: Alto contraste

Prompt Base:
"Podcast cover art, professional portrait style,
dark gradient background with subtle purple glow,
space for text and guest photo, clean modern design,
3000x3000 square format"
```

---

## Best Practices

### Para Thumbnails ✅

```
DO:
- Incluir espacio para texto
- Alta constraste y colores vibrantes
- Expresiones faciales fuertes
- Composición clara
- Consistencia de estilo

DON'T:
- Demasiado detalle
- Colores apagados
- Composición compleja
- Texto pequeño integrado
- Múltiples puntos focales
```

### Para Videos ✅

```
DO:
- Describir movimiento claramente
- Especificar duración
- Indicar estilo cinematográfico
- Mencionar transiciones
- Definir ritmo visual

DON'T:
- Acciones muy complejas
- Diálogos o labios sincronizados
- Textos animados elaborados
- Efectos especiales extremos
- Cambios de escena múltiples
```

---

## Workflow Completo

### Generación de Thumbnail

```
1. BRIEF
   └─ Título del video
   └─ Mensaje clave
   └─ Elementos requeridos

2. CONCEPT
   └─ Boceto rápido (mental o sketch)
   └─ Definir composición
   └─ Elegir template

3. PROMPT
   └─ Construir prompt detallado
   └─ Incluir espacio para texto
   └─ Especificar colores brand

4. GENERATE
   └─ Generar 3-5 variaciones
   └─ Evaluar opciones

5. SELECT & REFINE
   └─ Elegir la mejor
   └─ Ajustes menores si necesario

6. POST-PROCESS
   └─ Añadir texto
   └─ Ajustar colores
   └─ Exportar
```

---

## Output Specifications

### Resoluciones por Uso

| Uso | Resolución | Formato | Notas |
|-----|------------|---------|-------|
| YouTube Thumb | 1920x1080 | PNG/JPG | Max 2MB |
| IG Post Square | 1080x1080 | JPG | Feed |
| IG Post Portrait | 1080x1350 | JPG | Feed optimal |
| IG Story/Reel | 1080x1920 | JPG/MP4 | Vertical |
| Twitter/X | 1600x900 | PNG | 16:9 |
| LinkedIn | 1200x627 | PNG | Article |
| Podcast | 3000x3000 | PNG | Hi-res |

---

## Integración con Pipeline

### Conexión con Otros Skills

```
SORA 2 Output
     │
     ├──> Canva/Figma (añadir texto)
     │
     ├──> /optimize-image (compresión)
     │
     └──> /publish-content (programar)
```

### Archivos de Salida

```
ngx-content-studio/
└── outputs/
    └── images/
        └── sora/
            └── [YYYY-MM-DD]/
                ├── thumbnail_v1.png
                ├── thumbnail_v2.png
                ├── thumbnail_v3.png
                └── metadata.json
```

---

## Ejemplos de Uso

### Request: Thumbnail para Video de Workout

```
Usuario: "Necesito un thumbnail para mi video
'5 ejercicios que todo hombre de 40+ debe hacer'"
```

### Response

```
Generando thumbnail con SORA 2:

**Prompt:**
"YouTube thumbnail, fit man in his mid-40s with confident
expression performing a deadlift, dark modern gym background,
dramatic purple (#6D00FF) rim lighting, high contrast,
bold and eye-catching style, professional photography look,
space for text overlay on the left third, 1920x1080,
centered subject, slight low angle for power pose"

**Variaciones generadas:**
1. Pose frontal con mancuernas
2. Vista lateral con barra
3. Close-up expresión determinada

¿Cuál prefieres o ajusto algo?
```

### Request: Cover para Podcast

```
Usuario: "Necesito un cover para el episodio 24 del podcast,
el tema es 'La ciencia del sueño'"
```

### Response

```
Generando podcast cover con SORA 2:

**Prompt:**
"Podcast episode cover art, artistic visualization of sleep
and recovery, abstract representation of peaceful sleep with
subtle tech elements, dark navy and purple gradient background,
ethereal glowing elements suggesting rest and rejuvenation,
clean modern design with space for episode number and title,
3000x3000 square, premium aesthetic"

**Elementos a incluir después:**
- Logo NGX GENESIS
- "Ep. 24"
- Título del episodio
- Nombre del invitado (si aplica)

¿Te parece bien este concepto?
```

---

## Troubleshooting

| Issue | Causa | Solución |
|-------|-------|----------|
| Imagen genérica | Prompt vago | Añadir más detalles específicos |
| Rostros deformados | Limitación del modelo | Evitar close-ups extremos |
| Colores incorrectos | No especificados | Incluir códigos hex |
| Composición mala | Sin guía de layout | Especificar "space for text on X" |
| Estilo inconsistente | Sin referencia | Usar templates predefinidos |

---

## Tips Avanzados

### Consistency Across Thumbnails

Para mantener consistencia en una serie:

```
1. Crear un "style reference" en el prompt:
   "...consistent with previous thumbnails,
   same lighting style, same color treatment..."

2. Usar los mismos parámetros base

3. Mantener el mismo template de composición

4. Documentar prompts que funcionan bien
```

### A/B Testing de Thumbnails

```
Generar variaciones para testing:

A) Enfoque en rostro/expresión
B) Enfoque en acción
C) Enfoque en resultado

Testear con YouTube Analytics:
- CTR (Click-Through Rate)
- Impresiones
- Watch time correlation
```

---

## Recursos

- [SORA Documentation](https://openai.com/sora)
- [NGX Brand Guidelines](#)
- [Thumbnail Templates Library](#)

---

*Skill SORA 2 Video & Image Generation v1.0*

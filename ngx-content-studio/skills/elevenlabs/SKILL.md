# Skill: ElevenLabs Voice Generation

---

## Overview

Skill para generar voces con ElevenLabs. Crea voice-overs, narraciones, y contenido de audio para videos, podcasts, y anuncios.

**Comando:** `/voice-generate`
**Alias:** `/elevenlabs`, `/vo`, `/narration`

---

## Triggers

Este skill se activa cuando el usuario:

- Necesita voice-over para videos
- Quiere narración para contenido
- Pide audio para ads o promos
- Menciona ElevenLabs o TTS
- Necesita doblaje o localización
- Requiere audio para contenido automatizado

---

## Capabilities

### Text-to-Speech

| Feature | Descripción | Uso Ideal |
|---------|-------------|-----------|
| Voice Generation | Texto a voz natural | Narraciones, VO |
| Voice Cloning | Clonar voz existente | Consistencia de marca |
| Multilingual | Múltiples idiomas | Localización |
| Emotional Control | Control de tono | Ads, storytelling |
| Speed Control | Ajuste de velocidad | Tutoriales, ads |

### Voces Disponibles

**Voces Premium (Recomendadas para NGX):**

| Voz | Características | Uso Recomendado |
|-----|-----------------|-----------------|
| Josh | Masculina, profunda, autoritativa | Contenido principal |
| Marcus | Masculina, cálida, confiable | Tutoriales |
| Adam | Masculina, energética, dinámica | Ads, promos |
| Bella | Femenina, profesional, clara | Narraciones |
| Elli | Femenina, joven, amigable | Social content |
| Rachel | Femenina, cálida, mature | Podcasts |

**Voz Clonada NGX:**

| Voz | Uso | Notas |
|-----|-----|-------|
| Aldo (Clone) | Contenido oficial | Requiere samples |
| NGX Brand Voice | Consistencia de marca | Voz oficial |

---

## Prompt Structure

### Script Formatting

```
[VOZ]: Nombre de la voz a usar
[IDIOMA]: es-MX / en-US / etc.
[TONO]: Profesional / Energético / Cálido / Serio
[VELOCIDAD]: 0.8x - 1.2x (1.0 = normal)
[PAUSA]: Usar ... para pausas
[ÉNFASIS]: Usar *palabra* para enfatizar

---SCRIPT---

[El texto a narrar]

---FIN SCRIPT---
```

### Ejemplo: Video Intro

```
VOZ: Josh
IDIOMA: es-MX
TONO: Profesional, inspirador
VELOCIDAD: 1.0x

---SCRIPT---

¿Listo para transformar tu rendimiento?

Con NGX GENESIS... tienes *trece agentes de inteligencia artificial*
trabajando para ti... veinticuatro siete.

Entrenamiento. Nutrición. Sueño. Energía.

Todo optimizado. Todo *personalizado*.

Bienvenido al futuro del fitness.

---FIN SCRIPT---
```

### Ejemplo: Ad Copy

```
VOZ: Adam
IDIOMA: es-MX
TONO: Energético, urgente
VELOCIDAD: 1.1x

---SCRIPT---

¡Alto! Si tienes más de cuarenta años...

Y sientes que ya probaste *todo* para estar en forma...

Esto es para ti.

NGX GENESIS. Trece agentes de AI. Un objetivo: *tu mejor versión*.

Pruébalo gratis por catorce días.

---FIN SCRIPT---
```

---

## Voice Settings

### Parámetros de Control

| Parámetro | Rango | Descripción |
|-----------|-------|-------------|
| Stability | 0-1 | Consistencia de voz (0.5 recomendado) |
| Clarity | 0-1 | Claridad de pronunciación (0.75 rec) |
| Style | 0-1 | Expresividad (0.5 para neutral) |
| Speed | 0.5-2.0 | Velocidad de habla |

### Presets por Tipo de Contenido

**Preset: Video Narration**
```json
{
  "stability": 0.5,
  "clarity": 0.75,
  "style": 0.4,
  "speed": 1.0
}
```

**Preset: Advertisement**
```json
{
  "stability": 0.4,
  "clarity": 0.8,
  "style": 0.6,
  "speed": 1.1
}
```

**Preset: Tutorial**
```json
{
  "stability": 0.6,
  "clarity": 0.85,
  "style": 0.3,
  "speed": 0.95
}
```

**Preset: Podcast Intro**
```json
{
  "stability": 0.5,
  "clarity": 0.7,
  "style": 0.5,
  "speed": 1.0
}
```

---

## Script Writing Best Practices

### DO ✅

```
- Escribir como se habla (contracciones, flujo natural)
- Usar puntuación para ritmo
- Marcar pausas con ... o [PAUSA]
- Indicar énfasis con *asteriscos*
- Dividir oraciones largas
- Incluir pronunciación de términos técnicos
- Especificar números (veinticuatro, no 24)
```

### DON'T ❌

```
- Oraciones muy largas sin pausas
- Jerga o siglas sin contexto
- Números como dígitos (usar palabras)
- URLs completas (mejor "visita nuestra web")
- Formato robótico o demasiado formal
- Texto copiado directamente de blogs
```

---

## Workflow de Generación

```
1. SCRIPT DRAFT
   └─ Escribir borrador del texto
   └─ Leer en voz alta para timing
   └─ Ajustar para naturalidad

2. FORMAT
   └─ Añadir marcas de pausa
   └─ Marcar énfasis
   └─ Especificar pronunciaciones

3. VOICE SELECT
   └─ Elegir voz apropiada
   └─ Ajustar parámetros

4. GENERATE
   └─ Generar primera versión
   └─ Evaluar resultado

5. ITERATE
   └─ Ajustar script si necesario
   └─ Modificar parámetros
   └─ Regenerar

6. EXPORT
   └─ Descargar en formato requerido
   └─ Normalizar audio si necesario
```

---

## Output Specifications

### Formatos de Audio

| Formato | Calidad | Uso |
|---------|---------|-----|
| MP3 192kbps | Estándar | Web, social |
| MP3 320kbps | Alta | Videos |
| WAV | Lossless | Producción |
| OGG | Web optimized | Apps |

### Especificaciones Técnicas

| Parámetro | Valor Recomendado |
|-----------|-------------------|
| Sample Rate | 44.1kHz o 48kHz |
| Bit Depth | 16-bit o 24-bit |
| Channels | Mono (VO) o Stereo |
| Loudness | -16 LUFS (YouTube) |

---

## Integración con Pipeline

### Conexión con Otros Skills

```
ElevenLabs Output
     │
     ├──> /edit-audio (post-producción)
     │
     ├──> /edit-video (añadir a video)
     │
     ├──> /podcast-produce (episodios)
     │
     └──> /publish-content (programar)
```

### Archivos de Salida

```
ngx-content-studio/
└── outputs/
    └── audio/
        └── elevenlabs/
            └── [YYYY-MM-DD]/
                ├── vo_intro_v1.mp3
                ├── vo_intro_v2.mp3
                └── metadata.json
```

---

## Casos de Uso NGX

### 1. Video Intro/Outro

```
DURACIÓN: 10-15 segundos
VOZ: Josh o voz clonada Aldo
TONO: Profesional, inspirador

Template:
"Bienvenido a [CANAL/SERIE].
Soy [NOMBRE] y esto es [TEMA DEL VIDEO].
Empecemos."
```

### 2. Ad Voice-Over

```
DURACIÓN: 15-30 segundos
VOZ: Adam (energético) o Marcus (confiable)
TONO: Urgente pero profesional

Estructura:
- Hook (3s): Captar atención
- Problema (5s): Identificar pain point
- Solución (7s): Presentar NGX
- CTA (5s): Llamada a la acción
```

### 3. Tutorial Narration

```
DURACIÓN: Variable
VOZ: Marcus o Bella
TONO: Claro, paciente, instructivo

Tips:
- Velocidad 0.95x para claridad
- Pausas entre secciones
- Repetir términos clave
```

### 4. Podcast Intro

```
DURACIÓN: 20-30 segundos
VOZ: Josh o voz de marca
TONO: Profesional, amigable

Elementos:
- Nombre del podcast
- Tagline
- Breve descripción del episodio
- Disclaimer si necesario
```

---

## Ejemplos Completos

### Request: VO para Video YouTube

```
Usuario: "Necesito un voice-over para la intro de mi video
sobre los 5 mejores ejercicios para hombres de 40+"
```

### Response

```
Generando VO con ElevenLabs:

**Configuración:**
- Voz: Josh
- Idioma: Español (México)
- Velocidad: 1.0x
- Tono: Profesional, inspirador

**Script:**

"Si tienes más de cuarenta años... y crees que tu mejor
momento físico ya pasó...

Estás equivocado.

Hoy te voy a mostrar *cinco ejercicios* que pueden
transformar tu cuerpo... sin importar cuánto tiempo
llevas sin entrenar.

Estos son los movimientos que los expertos recomiendan...
y que yo mismo uso cada semana.

Quédate hasta el final... porque el *número cinco* es
el que más impacto tiene en tu salud a largo plazo.

Empecemos."

**Duración estimada:** 35 segundos
**Archivo:** vo_intro_5ejercicios_v1.mp3

¿Quieres que genere o ajusto el script?
```

---

## Troubleshooting

| Issue | Causa | Solución |
|-------|-------|----------|
| Pronunciación rara | Palabra no reconocida | Escribir fonéticamente |
| Tono robótico | Stability muy alto | Reducir a 0.4-0.5 |
| Demasiado rápido | Speed alto | Reducir velocidad |
| Pausas ausentes | Sin puntuación | Añadir ... y comas |
| Énfasis incorrecto | No marcado | Usar *asteriscos* |

### Pronunciaciones Especiales

| Término | Escribir Como |
|---------|---------------|
| NGX | "ene ge equis" |
| GENESIS | "yénesis" |
| BLAZE | "bléis" |
| MACRO | "macro" |
| LUNA | "luna" |
| 24/7 | "veinticuatro siete" |

---

## Recursos

- [ElevenLabs Documentation](https://elevenlabs.io/docs)
- [Voice Library](https://elevenlabs.io/voice-library)
- [NGX Audio Guidelines](#)

---

*Skill ElevenLabs Voice Generation v1.0*

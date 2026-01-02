# /podcast-clip

Genera un clip corto de podcast (2-5 min) enfocado en un solo momento/topic. Ideal para contenido derivado, Reels de audio, o teasers.

## Uso

```
/podcast-clip agents="LUNA,BLAZE" topic="¿Entreno si dormí mal?" duration=3
```

## Parámetros

| Parámetro | Requerido | Opciones | Default | Descripción |
|-----------|-----------|----------|---------|-------------|
| `agents` | ✅ | 2-3 agentes | - | Agentes participantes |
| `topic` | ✅ | Texto libre | - | Tema/pregunta específica |
| `duration` | ❌ | 2/3/5 | 3 | Duración en minutos |
| `format` | ❌ | debate/answer/tip | answer | Estilo del clip |
| `video` | ❌ | true/false | false | Incluir prompts video |

## Formatos

### DEBATE (2-3 agentes con posiciones opuestas)
```
/podcast-clip agents="BLAZE,WAVE" topic="¿Cardio en días de fuerza?" format=debate duration=3
```

### ANSWER (1-2 agentes respondiendo una pregunta)
```
/podcast-clip agents="SAGE" topic="¿Cuánta proteína necesito?" format=answer duration=2
```

### TIP (Consejo rápido y accionable)
```
/podcast-clip agents="SPARK" topic="Un hábito para empezar mañana" format=tip duration=2
```

## Output

### 1. Script del Clip
```
═══════════════════════════════════════════════════════════════════
NGX PODCAST CLIP
═══════════════════════════════════════════════════════════════════

TITLE: [Título del clip]
DURATION: [X] minutos
AGENTS: [Lista]
FORMAT: [debate/answer/tip]

───────────────────────────────────────────────────────────────────
SCRIPT
───────────────────────────────────────────────────────────────────

[00:00] 

[AGENTE]: (tono)
[Diálogo...]

[00:15]

[AGENTE]: (tono)
[Diálogo...]

[continúa...]

───────────────────────────────────────────────────────────────────
```

### 2. Voice Direction
```
───────────────────────────────────────────────────────────────────
VOICE DIRECTION - ELEVENLABS
───────────────────────────────────────────────────────────────────

AGENTE 1 | [Nombre]
"""
[Script con tags de emoción]
"""
Settings: Stability X, Clarity X, Style X

AGENTE 2 | [Nombre]
"""
[Script con tags de emoción]
"""
Settings: Stability X, Clarity X, Style X
```

### 3. Clip Metadata
```
───────────────────────────────────────────────────────────────────
CLIP METADATA
───────────────────────────────────────────────────────────────────

HOOK (primera línea para caption):
"[Primera línea impactante]"

KEY QUOTE:
"[Cita más memorable]" — [AGENTE]

WHY IT WORKS:
[Por qué este clip tiene potencial viral]

TÍTULOS SUGERIDOS:
1. [Opción 1]
2. [Opción 2]

HASHTAGS:
#NGX #[topic tags]
```

### 4. Video Prompts (si video=true)
```
───────────────────────────────────────────────────────────────────
VIDEO PROMPTS - [ENGINE]
───────────────────────────────────────────────────────────────────

SHOT 1 | [Duración]
PROMPT:
"""
[Prompt completo]
"""

[etc.]
```

## Usos Comunes

| Uso | Configuración |
|-----|---------------|
| Teaser de episodio | Extraer momento clave del episodio largo |
| Audiogram para Reels | Clip de audio + waveform visual |
| Respuesta a pregunta frecuente | format=answer, 2 min |
| Debate picante | format=debate, 3-5 min |
| Tip diario | format=tip, 2 min |

## Notas

- Los clips son autocontenidos — no requieren contexto del episodio completo
- El hook debe funcionar en los primeros 3 segundos
- Ideal para repurposing en múltiples plataformas
- Puede extraerse de un episodio existente o crearse standalone

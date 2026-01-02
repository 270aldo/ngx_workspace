# /podcast-episode

Genera un episodio completo de podcast con todo el paquete de pre-producción listo para ejecución manual.

## Uso

```
/podcast-episode agents="BLAZE,SAGE" topic="¿Necesitas suplementos?" format=debate duration=10
```

## Parámetros

| Parámetro | Requerido | Opciones | Default | Descripción |
|-----------|-----------|----------|---------|-------------|
| `agents` | ✅ | 2-5 agentes | - | Agentes participantes separados por coma |
| `topic` | ✅ | Texto libre | - | Tema del episodio |
| `format` | ❌ | debate/educational/casual/interview/solo | educational | Formato del episodio |
| `duration` | ❌ | 5/10/15/20/30 | 10 | Duración en minutos |
| `host` | ❌ | none/nexus/aldo | nexus | Quién modera/introduce |
| `video` | ❌ | true/false | false | Incluir prompts de video |
| `engine` | ❌ | veo/sora | veo | Engine de video (si video=true) |

## Ejemplos

### Debate básico
```
/podcast-episode agents="BLAZE,WAVE" topic="¿Cardio mata ganancias?" format=debate duration=10
```

### Educativo con video
```
/podcast-episode agents="SAGE,METABOL,LOGOS" topic="Cómo leer tus biomarcadores" format=educational duration=15 video=true engine=veo
```

### Entrevista con Aldo
```
/podcast-episode agents="ATLAS" topic="Fitness después de los 50" format=interview host=aldo duration=20
```

## Output

El comando genera un paquete completo que incluye:

### 1. Script Completo
- Diálogos con timestamps
- Notas de producción (pausa, énfasis, tono)
- Marcadores de agente
- Estructura por segmentos

### 2. Voice Direction (ElevenLabs)
- Script segmentado por agente
- Tags de emoción
- Settings recomendados por voz
- Timing guide con sync points

### 3. Derived Content
- 3-5 clips sugeridos con timestamps
- Quotes destacados para graphics
- Títulos A/B para testing
- Descripción lista para plataformas
- Hashtags estratégicos
- Concepto de thumbnail

### 4. Video Prompts (si video=true)
- Storyboard visual
- Shot list con prompts VEO/SORA
- Specs técnicos por escena
- Notas de post-producción

### 5. Copy Package
- Títulos optimizados
- Descripciones por plataforma
- Captions para redes

## Workflow de Ejecución

```
1. AUDIO
   └── Copiar scripts a ElevenLabs Studio
   └── Ajustar settings por voz
   └── Generar y exportar

2. VIDEO (si aplica)
   └── Copiar prompts a VEO/SORA/Kling
   └── Generar shots individuales
   └── Importar a Premiere

3. POST-PRODUCCIÓN
   └── Ensamblar audio + video
   └── Agregar transiciones
   └── Color correction
   └── Exportar

4. PUBLICACIÓN
   └── Copiar descripciones
   └── Agregar hashtags
   └── Subir thumbnail
   └── Programar
```

## Notas

- Los agentes deben existir en el roster de 13 agentes NGX
- Si `host=aldo` y `video=true`, se recomienda `engine=sora` para usar CAMEO
- Para episodios >30 min, considera dividir en partes
- Los clips sugeridos son puntos de alto engagement identificados en el script

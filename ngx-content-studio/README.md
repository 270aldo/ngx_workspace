# NGX Content Studio

> Centro de Pre-Producción para Contenido Multimedia NGX GENESIS

## 🎯 Propósito

NGX Content Studio genera **paquetes de pre-producción completos** para contenido multimedia. No automatiza la generación final — produce scripts, storyboards, prompts y specs listos para ejecutar manualmente en las plataformas.

```
Tú defines el contenido → Claude genera el paquete → Tú ejecutas en plataformas → Editas en Premiere
```

## 🎙️ El Podcast de Agentes NGX

El podcast es una pieza **estratégica** para el modelo de negocio:

| Impacto B2C | Impacto B2B |
|-------------|-------------|
| Usuarios conocen a los 13 agentes | Coaches ven el sistema en acción |
| Aprenden el "por qué" (LOGOS) | Entienden la propuesta de valor |
| Contenido diferenciador | Evidencia de sofisticación tecnológica |

## 🤖 Subagents Disponibles

| Agent | Rol |
|-------|-----|
| `@content-director` | Orquesta producción, decide workflow |
| `@podcast-producer` | Scripts de episodios, derived content |
| `@video-director` | Storyboards, shot lists, prompts VEO/SORA |
| `@voice-engineer` | Voice direction ElevenLabs |
| `@image-creator` | Prompts Nano Banana Pro, thumbnails |
| `@copywriter` | Títulos, descripciones, captions |

## ⚡ Slash Commands

### Podcast

| Comando | Descripción |
|---------|-------------|
| `/podcast-episode` | Episodio completo con todo el paquete |
| `/podcast-clip` | Clip corto 2-5 min |

### Video

| Comando | Descripción |
|---------|-------------|
| `/video-package` | Paquete completo de producción de video |

### Paquetes

| Comando | Descripción |
|---------|-------------|
| `/content-package` | Un tema → múltiples formatos coordinados |

## 📦 Output: Paquetes de Pre-Producción

### Paquete de Podcast
```
1. Script completo con timestamps
2. Voice direction para ElevenLabs
3. Derived content (clips, quotes, thumbnails)
4. Video prompts (opcional)
5. Copy para plataformas
```

### Paquete de Video
```
1. Creative brief
2. Storyboard frame por frame
3. Shot list con prompts COPY/PASTE READY
4. Voice script (si hay VO)
5. Notas de post-producción
6. Copy package
```

## 🎬 Plataformas de Ejecución

### Video
- **VEO 3.1 (Flow)** — Agentes, contenido educativo
- **SORA 2 Pro** — Contenido con Aldo (CAMEO)
- **Kling 2.1** — Multi-elementos, efectos

### Audio
- **ElevenLabs** — Voces de los 13 agentes

### Imagen
- **Nano Banana Pro** — Thumbnails, graphics

## 📋 Ejemplos de Uso

### Episodio de podcast con video
```
/podcast-episode agents="BLAZE,SAGE" topic="¿Necesitas suplementos?" format=debate duration=10 video=true engine=veo
```

### Video para Reels
```
/video-package topic="Introducción a TEMPO" platform=reels duration=30 engine=veo agents="TEMPO"
```

### Paquete completo de campaña
```
/content-package topic="Recuperación activa" --podcast-clip --reels --thumbnail --carousel
```

## 🎨 Estándares Visuales

### Paleta NGX (Obligatoria)
- **Primary**: #6D00FF (Electric Violet)
- **Secondary**: #7D1AFF
- **Background**: #050505
- **Surface**: #0A0A0A

### Prohibido
- ❌ Cyan (#00D4FF, #06B6D4)
- ❌ Blue (#3B82F6)

## 📁 Estructura del Proyecto

```
ngx-content-studio/
├── CLAUDE.md                    # Contexto maestro
├── README.md                    # Este archivo
├── .claude/
│   ├── agents/                  # 6 subagents
│   ├── commands/                # Slash commands
│   └── rules/                   # Estándares
├── agents-database/             # Base de datos de los 13 agentes
├── dashboards/
└── outputs/
    ├── podcasts/
    ├── videos/
    ├── images/
    └── packages/
```

## 🔄 Workflow Típico

```
1. DEFINE
   └── Qué contenido necesitas
   └── Para qué plataforma
   └── Qué agentes participan

2. GENERA
   └── Usa el comando apropiado
   └── Recibe paquete completo

3. EJECUTA
   └── Copia scripts a ElevenLabs
   └── Copia prompts a VEO/SORA
   └── Genera assets

4. EDITA
   └── Importa a Premiere
   └── Ensambla según storyboard
   └── Color correct, audio levels

5. PUBLICA
   └── Copia descriptions/captions
   └── Sube a plataformas
```

## 📊 Skills Integrados

El proyecto utiliza estas skills de `/mnt/skills/user/`:

- `ngx-podcast-factory` — Scripts de podcast
- `ngx-creative-production` — Briefs y storyboards
- `ngx-veo31-content-factory` — Prompts VEO
- `ngx-sora2-content-factory` — Prompts SORA
- `kling-video-director` — Prompts Kling
- `nano-banana-pro` — Prompts de imagen
- `ngx-voice-engine` — Voice direction
- `ngx-cinematic-director` — Visión narrativa
- `ngx-copywriting-engine` — Copy y textos

---

**NGX GENESIS** — *Rinde hoy. Vive mejor mañana.*

# NGX CONTENT STUDIO

> **Centro de Pre-Producción para Contenido Multimedia NGX GENESIS**
> Version: 1.0.0 | Diciembre 2025

---

## ⚠️ PRIMERA INSTRUCCIÓN - MEMORIA Y CONTEXTO

### Archivos de Este Workspace

| Archivo | Propósito | Leer al inicio? |
|---------|-----------|-----------------|
| `MEMORY.md` | Estado entre sesiones | ✅ Siempre |
| `NGX_CONTEXT.md` | Contexto general NGX | ✅ Siempre |
| `DECISIONS.md` | Decisiones tomadas | ✅ Siempre |
| `DO_NOT.md` | Errores a evitar | ✅ Siempre |
| `CHECKLIST.md` | Calidad pre-entrega | Al entregar |
| `PROMPTS.md` | Prompts probados | Cuando necesites |
| `TASKS.md` | Tareas frecuentes | Cuando necesites |
| `CROSS_REFERENCES.md` | Refs entre workspaces | Cuando necesites |

### Slash Commands de Sesión

- `/start-session` → Inicializa sesión, lee archivos, resume estado
- `/end-session` → Guarda estado en MEMORY.md, confirma
- `/status` → Muestra estado actual sin modificar nada

### AL INICIAR CADA SESIÓN
```
1. Lee MEMORY.md (estado anterior)
2. Lee NGX_CONTEXT.md (contexto NGX)
3. Lee DECISIONS.md (decisiones vigentes)
4. Lee DO_NOT.md (restricciones)
5. Resume estado al usuario
6. Pregunta si continuar pendiente o hacer algo nuevo
```

### AL TERMINAR CADA SESIÓN
```
1. Actualiza MEMORY.md con:
   - Fecha de sesión
   - Tareas completadas
   - Próxima prioridad
   - Notas relevantes
2. Actualiza DECISIONS.md si hubo decisiones nuevas
3. Confirma al usuario que la memoria fue guardada
```

---

## 🎯 PROPÓSITO DE ESTE WORKSPACE

Este es el **estudio de pre-producción** para todo el contenido multimedia de NGX GENESIS. Aquí se generan los paquetes de producción que luego se ejecutan manualmente en las plataformas correspondientes.

**IMPORTANTE:** Este proyecto NO automatiza la generación final. Produce:
- Scripts listos para ElevenLabs
- Prompts listos para VEO 3.1, SORA 2 Pro, Kling
- Prompts listos para Nano Banana Pro
- Storyboards y shot lists para producción
- Todo organizado y listo para copiar/pegar

**Flujo de trabajo:**
```
Claude genera paquete → Tú ejecutas en plataformas → Editas en Premiere
```

---

## 🎙️ EL PODCAST DE AGENTES NGX

### Valor Estratégico

El podcast es una pieza FUNDAMENTAL para el modelo de negocio:

| Impacto | B2C | B2B |
|---------|-----|-----|
| **Awareness** | Usuarios conocen a los 13 agentes | Coaches ven el sistema en acción |
| **Educación** | Aprenden el "por qué" (LOGOS) | Entienden la propuesta de valor |
| **Diferenciación** | Contenido que nadie más tiene | Ven tecnología que querrían |
| **Confianza** | Agentes con personalidad real | Evidencia de sofisticación |

> *"Nuestra competencia es a la vez nuestros clientes. Los trainers que quieran competir, lo querrán desde el día que lo vean."*

### Formatos de Episodio

| Formato | Estructura | Mejor Para |
|---------|------------|------------|
| **DEBATE** | Intro → Posición 1 → Posición 2 → Clash → Resolución | Mitos, X vs Y |
| **EDUCATIONAL** | Hook → Problema → Ciencia → Aplicación → Resumen | How-to, conceptos |
| **CASUAL** | Conversación libre con anclas | Engagement, relatabilidad |
| **INTERVIEW** | Intro → Preguntas → Deep-dives → Takeaways | Spotlights de agentes |
| **SOLO** | Hook → Historia → Insight → CTA | Manifestos, TED-style |

---

## 🤖 SISTEMA DE 13 AGENTES NGX

### Roster Completo

| Agente | Dominio | Estilo de Voz | Color |
|--------|---------|---------------|-------|
| **NEXUS** | Orquestador | Estratégico, big-picture | #6D00FF |
| **BLAZE** | Fuerza/Hipertrofia | Intenso, motivacional, directo | #EF4444 |
| **ATLAS** | Funcional | Sabio, protector, paciente | #F59E0B |
| **TEMPO** | Recuperación | Calmado, analítico | #6D00FF |
| **WAVE** | Cardio | Energético, rítmico | #6D00FF |
| **SAGE** | Nutrición (Estrategia) | Educativo, preciso, científico | #22C55E |
| **METABOL** | Salud Metabólica | Clínico pero cálido | #8B5CF6 |
| **MACRO** | Nutrición (Ejecución) | Práctico, directo, sin rodeos | #F97316 |
| **NOVA** | Movilidad | Fluido, mindful | #EC4899 |
| **SPARK** | Hábitos | Alentador, celebra progreso | #FBBF24 |
| **STELLA** | Mindset | Empático, empoderador | #A855F7 |
| **LUNA** | Sueño | Calmante, nocturno | #6366F1 |
| **LOGOS** | Educación | Didáctico, explica el "por qué" | #6D00FF |

### Voz de Aldo (Host)

Cuando Aldo participa como host:
- **Tono**: Cálido, directo, curioso, ocasionalmente irreverente
- **Rol**: Hace las preguntas que el usuario haría, conecta agentes
- **Idioma**: Español mexicano, natural, a veces code-switches
- **Frase**: "A ver, pero explícame como si...", "Esto es lo que yo haría..."

---

## 🎬 PLATAFORMAS DE EJECUCIÓN

### Video

| Plataforma | Uso Principal | Specs |
|------------|---------------|-------|
| **VEO 3.1 (Flow)** | Agentes, contenido educativo, multi-shot | 8s base, hasta 148s, 1080p |
| **SORA 2 Pro** | Contenido con Aldo (CAMEO), 25s de un shot | Hasta 25s, 1080p |
| **Kling 2.1** | Multi-elementos, efectos especiales | Variable |

### Audio

| Plataforma | Uso Principal |
|------------|---------------|
| **ElevenLabs** | Voces de los 13 agentes + Aldo |
| **ElevenLabs Studio** | Podcasts completos con conversaciones |

### Imagen

| Plataforma | Uso Principal |
|------------|---------------|
| **Nano Banana Pro** | Thumbnails, graphics, infográficos |
| **Gemini 3 Pro Image** | Generación de imágenes de alta calidad |

---

## 📦 OUTPUT: PAQUETES DE PRE-PRODUCCIÓN

### Paquete de Podcast

```
1. SCRIPT COMPLETO
   - Diálogos con timestamps [00:00]
   - Notas de producción (pausa), (énfasis)
   - Marcadores de agente [BLAZE]:

2. VOICE DIRECTION (ElevenLabs)
   - Script segmentado por agente
   - Voice IDs asignados
   - Tags de emoción [excited], [serious]
   - Instrucciones de cadencia

3. VIDEO PROMPTS (si se visualiza)
   - Prompt por escena/momento
   - Plataforma recomendada (VEO/SORA)
   - Specs técnicos

4. DERIVED CONTENT
   - 3-5 clips sugeridos con timestamps
   - Quotes para graphics
   - Títulos A/B
   - Descripción
   - Concepto de thumbnail
```

### Paquete de Video

```
1. CREATIVE BRIEF
   - Objetivo, audiencia, mensaje clave
   - Plataforma y specs

2. SCRIPT
   - Escenas numeradas
   - Diálogo/VO exacto
   - Duración por escena

3. STORYBOARD
   - Frame por frame
   - Descripción visual
   - Cámara y movimiento
   - Duración

4. SHOT LIST CON PROMPTS
   - Shot 1: [Prompt completo para VEO/SORA]
   - Shot 2: [Prompt completo para VEO/SORA]
   - ...

5. VOICE SCRIPT
   - Si hay VO externo
   - Tags de ElevenLabs

6. POST-PRODUCTION NOTES
   - Tips de edición
   - Transiciones sugeridas
   - Música/SFX recomendados
```

---

## 🎨 ESTÁNDARES VISUALES NGX

### Paleta de Colores

| Color | Hex | Uso |
|-------|-----|-----|
| Electric Violet | #6D00FF | Primario, highlights |
| Violet Hover | #7D1AFF | Elementos interactivos |
| Deep Purple | #5B21B6 | Acentos secundarios |
| Background | #050505 | Base oscura |
| Surface | #0A0A0A | Cards, paneles |

**PROHIBIDO**: #00D4FF, #06B6D4, #3B82F6 (cyan/blue)

### Ambiente NGX Lab

```
Futuristic fitness laboratory, dark matte surfaces, 
violet (#6D00FF) LED accent lighting, floating holographic data displays,
premium dark aesthetic, cinematic quality.

Lighting: Violet key light (front-left), purple fill (right), ambient violet rim
```

---

## 🔧 HERRAMIENTAS DISPONIBLES

### Subagents

| Agent | Rol | Modelo |
|-------|-----|--------|
| `@content-director` | Orquesta producción, decide workflow | Opus |
| `@podcast-producer` | Scripts de episodios, formatos, derived content | Opus |
| `@video-director` | Storyboards, shot lists, prompts VEO/SORA/Kling | Opus |
| `@voice-engineer` | Voice direction ElevenLabs, tags, cadencia | Sonnet |
| `@image-creator` | Prompts Nano Banana, thumbnails, graphics | Sonnet |
| `@copywriter` | Títulos, descripciones, captions | Opus |

### Slash Commands

**Podcast:**
- `/podcast-episode` — Episodio completo con todo el paquete
- `/podcast-clip` — Solo un momento/clip específico
- `/podcast-series` — Serie de episodios relacionados

**Video:**
- `/video-package` — Paquete completo de producción
- `/video-ad` — Creative para ads con prompts
- `/video-sequence` — Secuencia multi-shot

**Imagen:**
- `/thumbnail` — Thumbnail con prompt Nano Banana
- `/image-batch` — Lote de imágenes relacionadas

**Paquetes:**
- `/content-package` — Un tema → todo el contenido
- `/weekly-content` — Calendario semanal completo

### Skills Integrados

- `ngx-podcast-factory` — Scripts y voces de agentes
- `ngx-creative-production` — Briefs y storyboards
- `ngx-veo31-content-factory` — Prompts VEO 3.1
- `ngx-sora2-content-factory` — Prompts SORA 2 Pro
- `kling-video-director` — Prompts Kling
- `nano-banana-pro` — Prompts de imagen
- `ngx-voice-engine` — Voice direction ElevenLabs
- `ngx-cinematic-director` — Visión narrativa
- `ngx-copywriting-engine` — Copy y textos

---

## 📋 CHECKLIST DE CALIDAD

### Podcast

- [ ] Cada agente suena distinto y auténtico
- [ ] Conversación natural (no robótica)
- [ ] Timestamps alineados con duración
- [ ] Voice direction incluye tags de emoción
- [ ] Derived content completo
- [ ] Balanza Performance + Longevity

### Video

- [ ] Prompts usan paleta violeta (no cyan)
- [ ] Cada shot tiene prompt completo
- [ ] Specs técnicos claros (duración, ratio, resolución)
- [ ] Storyboard alineado con script
- [ ] Notes de post-producción incluidas

### General

- [ ] Sin terminología obsoleta (PRIME/LONGEVITY)
- [ ] Mensaje alineado a "Performance & Longevity"
- [ ] CTA claro si aplica
- [ ] Plataforma de destino especificada

---

## 📁 ESTRUCTURA DEL WORKSPACE

```
ngx-content-studio/
├── CLAUDE.md                    # Este archivo
├── README.md
├── .mcp.json
│
├── .claude/
│   ├── agents/                  # 6 subagents
│   ├── commands/                # Slash commands
│   └── rules/                   # Estándares de calidad
│
├── skills/                      # Referencias de skills
│   ├── podcast/
│   ├── video/
│   ├── audio/
│   └── image/
│
├── templates/                   # Templates reutilizables
│   ├── podcast/
│   ├── video/
│   ├── storyboard/
│   └── voice/
│
├── agents-database/             # Base de datos de los 13 agentes
│
├── dashboards/
│   └── content-calendar.html
│
└── outputs/
    ├── podcasts/
    ├── videos/
    ├── images/
    └── packages/
```

---

## 🎯 POSICIONAMIENTO

> **"Performance & Longevity" — Rinde hoy. Vive mejor mañana.**

Todo el contenido debe reflejar esta dualidad:
- **Performance**: Resultados hoy, métricas, progreso visible
- **Longevity**: Protección a futuro, salud sostenible, décadas no días

---

## 💡 EJEMPLOS DE USO

### Podcast Completo

```
/podcast-episode agents="BLAZE,SAGE" topic="¿Necesitas suplementos?" format=debate duration=10
```

Output:
- Script completo con timestamps
- Voice direction para ElevenLabs
- 5 clips sugeridos
- Quotes destacados
- Concepto de thumbnail

### Video con Todo

```
/video-package topic="Introducción a TEMPO" platform=reels engine=veo
```

Output:
- Creative brief
- Script con escenas
- Storyboard frame por frame
- Prompts VEO listos para copiar
- Voice script si hay VO
- Notes de post-producción

### Paquete Completo

```
/content-package topic="Recuperación activa" 
  --podcast-clip 
  --reels 
  --thumbnail
```

Output:
- Clip de podcast 2 min
- Video Reels 30s con prompts
- Thumbnail con prompt Nano Banana
- Todo coordinado visualmente

---

## 🔗 REFERENCIAS CRUZADAS

### Cuándo Usar Otros Workspaces

| Si necesitas... | Usa... |
|-----------------|--------|
| Copy para landing page | `ngx-marketing` |
| Email para promocionar contenido | `ngx-marketing` |
| PRD para feature de contenido | `ngx-product-studio` |
| Script de venta para video | `ngx-b2b-sales` |

### Cómo Compartir Entre Workspaces

1. Genera el output en el workspace correcto
2. Copia el archivo a este workspace si lo usarás frecuentemente
3. Referencia la ubicación en MEMORY.md

### Archivos Compartidos (Idénticos en Todos)

- `NGX_CONTEXT.md` — Contexto general de NGX
- `DO_NOT.md` — Errores a evitar
- `CHECKLIST.md` — Verificación pre-entrega
- `agents-database/all-agents.md` — Personalidades de agentes (específico de Content Studio)

---

*NGX GENESIS — "Rinde hoy. Vive mejor mañana."*

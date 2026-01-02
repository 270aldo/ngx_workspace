# Tareas Frecuentes - Content Studio

> Plantillas de tareas comunes con inputs/outputs definidos.

---

## 1. Episodio de Podcast Completo

### Input Requerido
- Agentes participantes (2-3)
- Tema del episodio
- Duración objetivo (15/20/30 min)
- Audiencia (B2C/B2B)

### Output
- Carpeta `outputs/podcasts/ep-[num]-[tema]/`
  - script.md (completo con timestamps)
  - voice-prompts/ (por agente)
  - show-notes.md

### Tiempo Estimado
~30 minutos

---

## 2. Clip de Podcast para Redes

### Input Requerido
- Episodio fuente
- Momento a extraer
- Duración (30/60/90 seg)
- Plataforma destino

### Output
- `outputs/podcasts/clips/[episodio]-clip-[num].md`
- Script del clip
- Caption + hashtags

### Tiempo Estimado
~10 minutos

---

## 3. Video Promocional (Lead Magnet)

### Input Requerido
- Lead magnet a promocionar
- Duración (30/60/90 seg)
- Plataforma destino
- Estilo visual

### Output
- Carpeta `outputs/videos/promo-[nombre]/`
  - script.md
  - shot-list.md
  - prompts-video.md (VEO/SORA)

### Tiempo Estimado
~20 minutos

---

## 4. Video de Agente Individual

### Input Requerido
- Nombre del agente
- Propósito (educativo/promo/engagement)
- Duración (60/90/120 seg)
- Audiencia

### Output
- Carpeta `outputs/videos/agente-[nombre]/`
  - script.md
  - visual-description.md
  - voice-config.md

### Tiempo Estimado
~15 minutos

---

## 5. Micro-Lesson (2-3 min)

### Input Requerido
- Tema de la lección
- Agente presentador
- Nivel (básico/intermedio/avanzado)
- Formato (explainer/tutorial/Q&A)

### Output
- `outputs/videos/lessons/[tema].md`
- Script estructurado
- Prompts visuales

### Tiempo Estimado
~15 minutos

---

## 6. Carrusel Educativo

### Input Requerido
- Tema
- Agente presentador
- # de slides (5-10)
- Plataforma (Instagram/LinkedIn)

### Output
- `outputs/images/carruseles/[tema]/`
  - slides.md (contenido por slide)
  - caption.md
  - prompts-visual.md

### Tiempo Estimado
~15 minutos

---

## 7. Thumbnails (3 variaciones)

### Input Requerido
- Video/episodio para thumbnail
- Estilo deseado
- Texto overlay

### Output
- `outputs/images/thumbnails/[video].md`
- 3 prompts para Nano Banana Pro

### Tiempo Estimado
~5 minutos

---

## 8. Creative Brief Completo

### Input Requerido
- Tipo de pieza (video/podcast/campaña)
- Objetivo
- Audiencia
- Mensaje clave
- Timeline

### Output
- `outputs/packages/brief-[nombre].md`
- Brief completo con todos los parámetros

### Tiempo Estimado
~15 minutos

---

## 9. Storyboard

### Input Requerido
- Video a storyboardear
- Duración total
- Script o concepto

### Output
- `outputs/packages/storyboard-[nombre].md`
- Tabla con escenas detalladas

### Tiempo Estimado
~20 minutos

---

## 10. Configuración de Voz (Agente)

### Input Requerido
- Nombre del agente
- Propósito de uso

### Output
- `outputs/packages/voice-[agente].md`
- Parámetros ElevenLabs
- Notas de dirección

### Tiempo Estimado
~10 minutos

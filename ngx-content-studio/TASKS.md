# Tareas Frecuentes — Content Studio

> Plantillas de tareas comunes en producción de contenido. Este workspace genera PAQUETES, no outputs finales.

---

## 🎙️ TAREA: Episodio de Podcast

### Input Requerido
- Agentes participantes (1-3)
- Tema del episodio
- Audiencia objetivo (B2C/B2B/ambos)
- Duración deseada (10/15/20 min)

### Output Esperado
- Script completo con diálogos
- Prompts de voz por agente (ElevenLabs)
- Notas de producción
- Guardado en `outputs/podcasts/[tema]-[fecha]/`

### Checklist Específico
- [ ] Personalidades de agentes correctas
- [ ] Diálogos naturales (no robóticos)
- [ ] Momento de tensión/debate incluido
- [ ] CTA orgánico al final
- [ ] Duración aproximada correcta

---

## 🎬 TAREA: Video Corto (15-60 seg)

### Input Requerido
- Concepto/mensaje del video
- Plataforma destino (IG/TikTok/YT/Ads)
- Plataforma de generación (VEO/SORA/Kling)
- Duración exacta

### Output Esperado
- Storyboard (frames clave)
- Shot list con timestamps
- Prompts de generación por escena
- Dirección de audio/música
- Guardado en `outputs/videos/[nombre]-[fecha]/`

### Checklist Específico
- [ ] Hook en primeros 3 segundos
- [ ] Prompts específicos por plataforma
- [ ] Duración dentro del límite
- [ ] Estilo visual NGX (dark, violeta)
- [ ] CTA claro si aplica

---

## 🎤 TAREA: Script con Voz

### Input Requerido
- Agente que habla
- Texto/mensaje a comunicar
- Contexto (podcast/video/app/ad)
- Duración aproximada

### Output Esperado
- Script con texto exacto
- Dirección de voz detallada
- Configuración ElevenLabs sugerida
- Guardado en `outputs/voice/[agente]-[tema]-[fecha].md`

### Checklist Específico
- [ ] Voz del agente correcta
- [ ] Direcciones de tono incluidas
- [ ] Pausas y énfasis marcados
- [ ] Compatible con ElevenLabs

---

## 🖼️ TAREA: Prompts de Imagen

### Input Requerido
- Concepto de la imagen
- Plataforma destino
- Dimensiones requeridas
- Texto en imagen (si hay)

### Output Esperado
- Prompt principal optimizado
- 2-3 variaciones para A/B
- Especificaciones técnicas
- Guardado en `outputs/images/[nombre]-[fecha].md`

### Checklist Específico
- [ ] Colores NGX especificados
- [ ] Estilo visual consistente
- [ ] Resolución/dimensiones correctas
- [ ] Optimizado para Nano Banana Pro

---

## 📦 TAREA: Paquete de Campaña

### Input Requerido
- Tema/objetivo de la campaña
- Plataformas objetivo
- Duración de la campaña
- Tipos de contenido requeridos

### Output Esperado
- Carpeta completa con todos los assets
- Documento índice de contenidos
- Calendario de publicación sugerido
- Guardado en `outputs/packages/[campaña]-[fecha]/`

### Checklist Específico
- [ ] Todos los formatos incluidos
- [ ] Mensaje consistente en todo
- [ ] Paquete autocontenido
- [ ] Instrucciones de ejecución claras

---

## 📚 TAREA: Contenido LOGOS

### Input Requerido
- Tema educativo
- Nivel (básico/intermedio/avanzado)
- Formato (artículo/quiz/interactivo)
- Duración de lectura objetivo

### Output Esperado
- Contenido completo estructurado
- Quiz de verificación (si aplica)
- Guardado en `outputs/education/[tema]-[fecha].md`

### Checklist Específico
- [ ] Tono LOGOS (didáctico, empoderador)
- [ ] "Por qué" explicado, no solo "qué"
- [ ] Aplicación práctica incluida
- [ ] Nivel apropiado para audiencia

---

## 🎬 TAREA: Clips Extraíbles

### Input Requerido
- Episodio o contenido fuente
- Cantidad de clips deseados
- Duración por clip (1-3 min)
- Plataformas destino

### Output Esperado
- Scripts de cada clip
- Timestamps del contenido original
- Sugerencias de hook/caption
- Guardado en `outputs/clips/[episodio]-clips-[fecha]/`

### Checklist Específico
- [ ] Clips autocontenidos
- [ ] Hooks fuertes
- [ ] Variedad de momentos
- [ ] Optimizados para plataforma

---

## 📅 TAREA: Paquete Semanal

### Input Requerido
- Semana objetivo (fechas)
- Tema central
- Plataformas activas
- Recursos disponibles

### Output Esperado
- Todo el contenido de la semana
- Calendario de publicación
- Guardado en `outputs/weekly/semana-[fecha]/`

### Checklist Específico
- [ ] Todos los días cubiertos
- [ ] Variedad de formatos
- [ ] Tema consistente
- [ ] Realista para producir

---

## Flujo de Trabajo Recomendado

```
1. Recibir brief/idea
2. Identificar tarea en TASKS.md
3. Verificar inputs completos
4. Usar prompt de PROMPTS.md
5. Generar paquete completo
6. Verificar con CHECKLIST.md
7. Guardar en outputs/
8. Usuario ejecuta manualmente en plataformas
```

---

**RECORDATORIO:** Este workspace NO ejecuta la generación final. Produce paquetes que el usuario ejecuta en VEO, SORA, ElevenLabs, etc.

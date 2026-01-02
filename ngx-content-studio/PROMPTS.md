# Prompts Probados — Content Studio

> Prompts para pre-producción de contenido multimedia. Este workspace genera PAQUETES listos para ejecutar manualmente en las plataformas.

---

## 🎙️ Podcast de Agentes

### Episodio Completo
```
Genera episodio de podcast donde [AGENTE1] y [AGENTE2] discuten [TEMA].

Duración: [10/15/20] minutos
Formato: Conversación entre dos agentes NGX
Audiencia: [B2C usuarios / B2B coaches / ambos]

Estructura:
1. Intro (NEXUS presenta el tema) - 1 min
2. [AGENTE1] abre con su perspectiva - 3 min
3. [AGENTE2] responde/complementa - 3 min
4. Debate/tensión constructiva - 5 min
5. Resolución y síntesis - 2 min
6. Llamada a acción - 1 min

Incluir:
- Diálogos naturales (no robóticos)
- Personalidades correctas de cada agente
- Momento de tensión/desacuerdo
- Resolución que integra ambas perspectivas

Guardar en: outputs/podcasts/
```

### Clip de Podcast (1-3 min)
```
Genera clip corto extraíble del episodio [NOMBRE/TEMA].

Duración: [1/2/3] minutos
Objetivo: [Awareness / Engagement / Education]
Plataforma destino: [Instagram Reels / TikTok / YouTube Shorts]

El clip debe:
- Ser autocontenido (entendible sin contexto)
- Tener hook en primeros 3 segundos
- Incluir momento memorable
- Terminar con gancho o CTA

Incluir: Timestamps del episodio original + script del clip.
```

### Episodio Solo (Un Agente)
```
Genera episodio donde [AGENTE] explica [TEMA] a profundidad.

Duración: [8/10/12] minutos
Formato: Monólogo educativo con personalidad del agente

Estructura:
1. Hook + por qué importa - 1 min
2. Concepto principal explicado - 3 min
3. Aplicación práctica - 3 min
4. Errores comunes a evitar - 2 min
5. Resumen + CTA - 1 min

Voz del agente según NGX_CONTEXT.md y Agent Voice Bible.
```

---

## 🎬 Video (VEO 3.1 / SORA 2)

### Paquete de Video Corto
```
Genera paquete de pre-producción para video de [DURACIÓN] segundos.

Plataforma de generación: [VEO 3.1 / SORA 2 Pro / Kling]
Plataforma destino: [Instagram / TikTok / YouTube / Ads]
Objetivo: [Awareness / Education / Conversion]

Incluir:
1. Concepto creativo (1 párrafo)
2. Storyboard (escena por escena)
3. Shot list con timestamps
4. Prompts de generación por escena
5. Dirección de audio/música
6. Texto en pantalla (si aplica)

Guardar en: outputs/videos/
```

### Video de Agente Hablando
```
Genera paquete para video de [AGENTE] explicando [TEMA].

Duración: [15/30/60] segundos
Estilo: Agente hablando a cámara

Incluir:
1. Script completo con timestamps
2. Prompt de generación de video (VEO/SORA)
3. Prompt de voz (ElevenLabs)
4. Descripción visual del agente
5. Background/ambiente sugerido

Referencias: NGX_CONTEXT.md + Agent Voice Bible
```

### Video Cinematográfico
```
Genera paquete para video cinematográfico de marca.

Concepto: [DESCRIPCIÓN DEL CONCEPTO]
Duración: [30/60/90] segundos
Tono: [Épico / Inspiracional / Educativo / Testimonial]

Incluir:
1. Tratamiento creativo
2. Storyboard detallado (6-12 frames)
3. Shot list con especificaciones técnicas
4. Prompts de generación por shot
5. Música/audio sugerido
6. Color grading sugerido
7. Transiciones entre shots

Guardar en: outputs/videos/
```

---

## 🎤 Voz (ElevenLabs)

### Configuración de Voz de Agente
```
Genera configuración de voz para [AGENTE] en ElevenLabs.

Incluir:
1. Descripción de la voz objetivo
2. Voice settings (stability, similarity, style)
3. Texto de prueba (3-5 frases características)
4. Ajustes por contexto (explicando vs motivando vs conversando)

Referencia: Agent Voice Bible
```

### Script con Dirección de Voz
```
Genera script para [AGENTE] con dirección de voz detallada.

Tema: [TEMA]
Duración: [SEGUNDOS/MINUTOS]
Contexto: [Podcast / Video / Intro app / Ad]

Por cada sección incluir:
- Texto exacto a narrar
- Dirección de tono (velocidad, emoción, énfasis)
- Pausas indicadas
- Palabras a enfatizar
```

---

## 🖼️ Imágenes (Nano Banana Pro)

### Thumbnail para YouTube
```
Genera prompt para thumbnail de YouTube.

Tema del video: [TEMA]
Estilo: [NGX dark mode / Agente destacado / Texto grande]

El prompt debe:
- Describir composición exacta
- Especificar colores NGX (violeta #6D00FF)
- Incluir texto si aplica
- Ser optimizado para Nano Banana Pro
```

### Imagen para Redes Sociales
```
Genera prompt para imagen de [PLATAFORMA].

Concepto: [DESCRIPCIÓN]
Dimensiones: [1:1 / 4:5 / 9:16 / 16:9]
Texto en imagen: [SI/NO - QUÉ TEXTO]

Incluir variaciones de prompt para A/B testing.
```

### Avatar/Render de Agente
```
Genera prompt para render de [AGENTE].

Pose/Acción: [DESCRIPCIÓN]
Ambiente: [DESCRIPCIÓN]
Estilo: [Cinematográfico / Ilustración / 3D render]

Especificaciones:
- Símbolo en pecho correcto
- Color de ojos correcto
- Iluminación sugerida
- Resolución objetivo
```

---

## 📦 Paquetes de Contenido

### Paquete Completo de Campaña
```
Genera paquete de contenido completo para campaña de [TEMA].

Incluir:
1. Episodio de podcast (2 agentes)
2. 3 clips extraíbles
3. 1 video corto (30 seg)
4. 5 imágenes para redes
5. Copy para posts

Todo alineado con el mismo mensaje y tema.
Guardar en: outputs/packages/[campaña]-[fecha]/
```

### Paquete Semanal de Contenido
```
Genera paquete de contenido para semana de [FECHA].

Tema central: [TEMA]
Plataformas: [LISTA]

Incluir:
- 1 episodio de podcast
- 2 videos cortos
- 5 posts de redes (copy + visual sugerido)
- 1 email de newsletter

Organizar por día de publicación.
```

---

## 📚 Contenido Educativo (LOGOS)

### Módulo Educativo
```
Genera contenido educativo sobre [TEMA] para LOGOS.

Formato: [Artículo / Quiz / Explicación interactiva]
Nivel: [Básico / Intermedio / Avanzado]
Duración de lectura: [3/5/10] minutos

Estructura:
1. Por qué importa (contexto)
2. Concepto explicado claramente
3. Aplicación práctica
4. Errores comunes
5. Quiz de verificación (3-5 preguntas)

Tono: LOGOS (didáctico, empoderador, paciente)
```

### Explicación "¿Por qué?"
```
Genera explicación de LOGOS para decisión de NGX ENGINE.

Decisión: [DESCRIPCIÓN DE LA DECISIÓN]
Usuario: [CONTEXTO DEL USUARIO]
Agente que propuso: [AGENTE]

La explicación debe:
- Ser clara y accesible
- Dar el "por qué" no solo el "qué"
- Incluir ciencia cuando sea relevante
- Empoderar al usuario (no solo obedecer)

Tono: Educativo, no condescendiente.
```

---

## Cómo Usar Este Archivo

1. **Identificar** el tipo de contenido a crear
2. **Copiar** el prompt apropiado
3. **Personalizar** las variables
4. **Ejecutar** y verificar con checklist
5. **Guardar** el paquete completo en outputs/

---

**RECORDATORIO:** Este workspace genera PAQUETES DE PRE-PRODUCCIÓN. La ejecución final (generar video en VEO, voz en ElevenLabs, etc.) se hace manualmente.

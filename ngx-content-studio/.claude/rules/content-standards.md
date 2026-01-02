# NGX Content Standards

Reglas obligatorias para toda producción de contenido NGX GENESIS.

---

## 🎨 Visual Standards

### Paleta de Colores

**USAR:**
| Color | Hex | Contexto |
|-------|-----|----------|
| Electric Violet | #6D00FF | Primario, highlights, key lighting |
| Violet Hover | #7D1AFF | Secundario, acentos |
| Deep Purple | #5B21B6 | Sombras, profundidad |
| Background | #050505 | Fondos principales |
| Surface | #0A0A0A | Cards, áreas secundarias |
| White | #FFFFFF | Texto principal |
| Muted | #A1A1AA | Texto secundario |

**PROHIBIDO:**
- ❌ #00D4FF (Cyan)
- ❌ #06B6D4 (Cyan)
- ❌ #3B82F6 (Blue)
- ❌ Fondos blancos o claros
- ❌ Estética "corporate blue"

### Si VEO/SORA Genera Cyan

Nota en post-producción para color correct hacia violeta.

---

## 📝 Brand Voice Standards

### Voz Principal: "Verdad Directa"

**Principios:**
1. Confrontar con respeto
2. Fundamentar con ciencia
3. Resolver con sistemas

### Palabras Clave

**USAR:**
- Temporada (no "programa")
- Construir (no "ganar")
- Protocolo (no "dieta")
- Sistema (no "plan")
- Evidencia (no "opinión")

**EVITAR:**
- Transformación mágica
- Resultados rápidos
- Secretos
- Hack
- Truco
- Fácil
- Sin esfuerzo

### Posicionamiento

Todo contenido debe reflejar:

```
PERFORMANCE          +          LONGEVITY
(Resultados hoy)                (Protección mañana)
```

**Ejemplos:**
- ❌ "Gana músculo rápido"
- ✅ "Construye músculo que dure décadas"

- ❌ "Quema grasa"
- ✅ "Optimiza tu composición corporal de forma sostenible"

---

## 🤖 Agent Standards

### Voces Distintas

Cada agente DEBE sonar único. Nunca genérico.

### Uso de Frases Características

- Usar naturalmente, no forzar
- Máximo 1-2 por intervención larga
- Deben fluir en la conversación

### Interacciones Entre Agentes

- Permiten desacuerdo respetuoso
- Build on ideas (no solo responder)
- Interrupciones naturales ocasionales
- Momentos de acuerdo genuino

### Prohibido

- Agentes que suenan igual
- Respuestas genéricas sin expertise
- Terminología de arquetipos (PRIME/LONGEVITY)
- Agentes que se contradicen a sí mismos

---

## 🎙️ Audio Standards

### ElevenLabs

**Tags de emoción:**
- Usar apropiadamente por personalidad de agente
- No sobre-usar (máximo 3-4 por segmento)
- Pausas naturales entre ideas

**Settings por tipo de agente:**
| Tipo | Stability | Clarity | Style |
|------|-----------|---------|-------|
| Intenso (BLAZE) | 0.35 | 0.80 | 0.60 |
| Calmado (LUNA) | 0.60 | 0.70 | 0.20 |
| Educativo (LOGOS) | 0.50 | 0.75 | 0.30 |
| Energético (WAVE) | 0.40 | 0.70 | 0.50 |

### Timing

- Pausas entre agentes: 0.5-1s
- Pausas dramáticas: 1.5-2s
- Transiciones de tema: 1s

---

## 🎬 Video Standards

### Prompts

**Estructura obligatoria (VEO 3.1):**
```
[SUBJECT] + [ACTION] + [SETTING] + [STYLE] + [CAMERA] + [LIGHTING] + [AUDIO] + [CONSTRAINTS]
```

**Incluir siempre:**
- Color hex específico (#6D00FF)
- Duración y aspect ratio
- Movimiento de cámara
- Audio description

### Duración por Plataforma

| Plataforma | Óptimo | Hook Time |
|------------|--------|-----------|
| TikTok | 15-45s | 0.5s |
| Reels | 15-60s | 1s |
| YouTube Shorts | 15-60s | 1s |
| YouTube Long | Flexible | 3s |
| LinkedIn | 15-60s | 2s |

### Engine Selection

| Situación | Engine |
|-----------|--------|
| Solo agentes | VEO 3.1 |
| Fundador aparece | SORA 2 Pro |
| Multi-elementos | Kling |
| Máxima consistencia | VEO 3.1 + JSON |

---

## 📋 Delivery Standards

### Paquetes Completos

Nunca entregar parciales. Siempre incluir:
- [ ] Scripts/prompts copy/paste ready
- [ ] Specs técnicos claros
- [ ] Notas de producción
- [ ] Copy para plataformas

### Organización

- Secciones claramente separadas
- Orden de ejecución lógico
- Settings explícitos
- Tips de troubleshooting

### Formato de Prompts

```
──────────────────────────────────────────────────────────────────
SHOT [#] | [Duración] | Engine: [VEO/SORA/Kling]
──────────────────────────────────────────────────────────────────
PROPÓSITO: [Para qué es este shot]

PROMPT (copiar completo):
"""
[Prompt aquí - listo para copy/paste]
"""

SETTINGS:
- Duration: [X] seconds
- Resolution: 1080p
- Aspect Ratio: [ratio]
```

---

## ✅ Quality Checklist

### Podcast

- [ ] Cada agente suena distinto
- [ ] Datos/métricas específicos incluidos
- [ ] Balanza Performance + Longevity
- [ ] Sin terminología de arquetipos
- [ ] Flujo natural de conversación
- [ ] Timestamps alineados con duración
- [ ] Notas de producción incluidas
- [ ] Derived content completo

### Video

- [ ] Prompts usan paleta violeta
- [ ] Cada shot tiene prompt completo
- [ ] Specs técnicos claros
- [ ] Storyboard alineado con script
- [ ] Notes de post-producción incluidas
- [ ] Transiciones definidas

### Copy

- [ ] Voz "Verdad Directa" consistente
- [ ] Balance Performance + Longevity
- [ ] CTAs claros y accionables
- [ ] Sin palabras prohibidas
- [ ] Adaptado a cada plataforma

---

## 🚫 Nunca Hacer

1. Entregar prompts sin specs técnicos
2. Usar cyan/blue en cualquier visual
3. Generar agentes que suenan genéricos
4. Prometer resultados rápidos/fáciles
5. Olvidar el derived content
6. Ignorar el balance Performance + Longevity
7. Entregar paquetes incompletos

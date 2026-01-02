---
description: Genera contenido para LinkedIn orientado a coaches fitness (B2B)
arguments:
  - name: type
    description: Tipo de post (story|insight|listicle|contrarian|bts|case-study)
    required: true
  - name: topic
    description: Tema específico del post
    required: true
  - name: count
    description: Número de posts a generar
    default: "1"
  - name: coach_name
    description: Nombre del coach (para case-study)
---

# Contenido LinkedIn B2B

**Tipo:** $ARGUMENTS.type
**Tema:** $ARGUMENTS.topic
**Cantidad:** $ARGUMENTS.count
**Coach (si aplica):** $ARGUMENTS.coach_name

---

## Instrucciones para @linkedin-strategist

Genera contenido LinkedIn siguiendo la estrategia B2B de NGX:

### Pilares de Contenido
- 40% Educación para coaches
- 25% Building in public
- 20% Insights de IA/Tech
- 15% Promoción directa

### Según el tipo:

**story** → Narrativa personal del journey
- Gancho emocional
- Arco: Problema → Lucha → Aprendizaje
- Cierre con reflexión
- 800-1200 caracteres

**insight** → Una idea valiosa en pocas líneas
- Observación clara
- Desarrollo breve
- Conclusión accionable
- 400-800 caracteres

**listicle** → Tips, errores, lecciones
- Formato: "X [cosas] que [resultado]"
- Items concisos (1-2 líneas cada uno)
- Cierre con pregunta
- 600-1000 caracteres

**contrarian** → Opinión que desafía el status quo
- Take polémico pero defendible
- Argumento sólido
- Invitar al debate
- 400-800 caracteres

**bts** → Behind the scenes de construcción
- Update de desarrollo
- Lo que funciona/no funciona
- Transparencia
- 400-600 caracteres

**case-study** → Testimonial de coach
- Problema → Solución → Resultados
- Métricas concretas
- Quote del coach
- CTA suave
- 600-900 caracteres

### Formato LinkedIn
- Espacios entre líneas (mobile-first)
- Sin emojis excesivos
- 3-5 hashtags relevantes
- Pregunta al final para engagement

### NO hacer:
- Posts de más de 1500 caracteres
- Venta agresiva
- Copiar formatos virales sin adaptar
- Ignorar el contexto de coaches

---

## Output

Guarda en: `outputs/linkedin/$(date +%Y-%m-%d)-$ARGUMENTS.type-post.md`

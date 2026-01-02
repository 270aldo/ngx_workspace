---
description: Investiga y califica un prospect B2B para el programa Founding Coaches
arguments:
  - name: name
    description: Nombre del prospect
    required: true
  - name: instagram
    description: Handle de Instagram (@usuario)
  - name: linkedin
    description: URL de perfil de LinkedIn
  - name: website
    description: URL del sitio web
  - name: notes
    description: Notas adicionales sobre el prospect
---

# Investigación de Prospect B2B

**Prospect:** $ARGUMENTS.name
**Instagram:** $ARGUMENTS.instagram
**LinkedIn:** $ARGUMENTS.linkedin
**Website:** $ARGUMENTS.website
**Notas:** $ARGUMENTS.notes

---

## Instrucciones para @prospect-researcher

Realiza una investigación completa de este prospect siguiendo el proceso definido:

### 1. Información Básica
- Nombre completo
- Ubicación
- Nicho/especialidad

### 2. Análisis de Presencia Digital
- Seguidores y engagement
- Tipo de contenido
- Frecuencia de publicación
- Testimoniales visibles

### 3. Análisis de Negocio
- Servicios que ofrece
- Rango de precios (si visible)
- Herramientas que menciona
- Señales de volumen de clientes

### 4. Calificación
- Score 1-100 basado en criterios ICP
- Clasificación: A (hot), B (warm), C (cold)
- Recomendación de acción
- Ángulo de entrada sugerido

---

## Output

Guarda en: `outputs/pipeline/$(date +%Y-%m-%d)-$ARGUMENTS.name-research.md`

Después de la investigación:
- Si es A → Sugiere pasar a @sales-script-writer
- Si es B → Sugiere pasar a @b2b-email-architect para nurturing
- Si es C → Documenta razones y archiva

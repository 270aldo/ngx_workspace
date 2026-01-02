---
description: Ejecuta auditoría completa de una página o flujo del funnel NGX usando Chrome automation
arguments:
  - name: url
    description: URL a auditar
    required: true
  - name: type
    description: Tipo de auditoría (landing|checkout|full-flow|quick)
    default: quick
  - name: device
    description: Dispositivo a auditar (desktop|mobile|both)
    default: both
---

# Auditoría de Funnel NGX

Ejecutando auditoría de: **$ARGUMENTS.url**
Tipo: **$ARGUMENTS.type**
Dispositivos: **$ARGUMENTS.device**

---

## Instrucciones para @funnel-auditor

Usa Claude in Chrome para ejecutar esta auditoría siguiendo estos pasos:

### Si type = quick
1. Navega a la URL proporcionada
2. Evalúa visualmente (desktop y mobile si device=both)
3. Verifica CTA principal
4. Revisa copy contra criterios NGX
5. Genera reporte resumido (score + 3 issues principales)

### Si type = landing
1. Auditoría visual completa (desktop + mobile)
2. Evaluación de copy (modos, voz, tratamiento)
3. Test de formulario si existe
4. Verificación de links
5. Check de identidad visual NGX
6. Reporte completo con scores por categoría

### Si type = checkout
1. Navegar al checkout desde la página principal
2. Evaluar claridad del proceso
3. Verificar campos del formulario
4. Evaluar mensajes de confianza (garantía, seguridad)
5. Test de usabilidad del proceso

### Si type = full-flow
1. Comenzar en la URL proporcionada
2. Seguir el journey completo como un usuario real
3. Documentar cada paso con observaciones
4. Identificar fricciones en cada transición
5. Generar reporte de journey completo

---

## Criterios de Evaluación

### Identidad Visual NGX
- Color primario: #6D00FF (Violeta)
- Fondo: #0A0A0A
- Cards con blur y gradientes oscuros
- Sombras neón en botones
- SIN cyan, SIN colores brillantes

### Voz de Marca
- Fórmula: CONFRONTA → FUNDAMENTA → RESUELVE
- Tratamiento: tú (30-45) / usted (45-60)
- Sin promesas absolutas
- Sin urgencia falsa
- Máximo 1-2 emojis

### UX/Conversión
- CTA visible above the fold
- Propuesta de valor clara en <3 segundos
- Formularios de 2-4 campos máximo
- Touch targets ≥44px en mobile

---

## Output Esperado

Guarda el reporte en: `outputs/audits/$(date +%Y-%m-%d)-$ARGUMENTS.type-audit.md`

El reporte debe incluir:
1. Score general (1-100)
2. Scores por categoría
3. Issues críticos (🔴)
4. Issues importantes (🟡)
5. Oportunidades de mejora (🟢)
6. Lo que está bien (✅)
7. Próximos pasos recomendados

Si es la primera auditoría de esta URL, establece baseline.
Si ya existe auditoría anterior, incluye comparación.

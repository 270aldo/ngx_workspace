---
description: Genera una secuencia de emails completa para un lead magnet o propósito específico
arguments:
  - name: type
    description: Tipo de secuencia (welcome|nurture|conversion|reengagement|hybrid-nurture)
    required: true
  - name: lead_magnet
    description: Lead magnet de entrada (stress-signature|ngx-transform|logos-dictionary|metabolic-age|recovery-score|sleep-guide)
    required: false
  - name: days
    description: Duración de la secuencia en días
    default: 7
  - name: audience
    description: Audiencia target (30-45|45-60)
    default: 30-45
---

# Generación de Secuencia de Email

**Tipo:** $ARGUMENTS.type
**Lead Magnet:** $ARGUMENTS.lead_magnet
**Duración:** $ARGUMENTS.days días
**Audiencia:** $ARGUMENTS.audience

---

## Instrucciones para @email-architect

Genera una secuencia de emails completa siguiendo las especificaciones.

### Configuración por Tipo

**welcome:**
- Trigger: Descarga de lead magnet
- Objetivo: Entregar valor, establecer confianza, primera oferta
- Estructura: Entrega → Valor → Historia → Sistema → Prueba social → Oferta

**nurture:**
- Trigger: Post-welcome sin conversión
- Objetivo: Mantener engagement, educar, preparar para oferta
- Frecuencia: 1 email/semana

**conversion:**
- Trigger: Lead calificado no convertido
- Objetivo: Cerrar venta de ASCEND
- Estructura: Urgencia suave, testimoniales, garantía

**reengagement:**
- Trigger: Inactivo +30 días
- Objetivo: Reactivar o despedir limpiamente
- Tono: Honesto, sin presión

**hybrid-nurture:**
- Trigger: Interés mostrado en HYBRID
- Objetivo: Educar sobre valor del coaching, agendar llamada
- Duración: 14 días típicamente

### Adaptación por Audiencia

**30-45 años:**
- Tratamiento: Tú
- Tono: Directo, coloquial
- Énfasis: Eficiencia, datos, resultados
- CTAs: "Comenzar", "Probarlo", "Ver cómo funciona"

**45-60 años:**
- Tratamiento: Usted
- Tono: Respetuoso, profesional
- Énfasis: Seguridad, longevidad, prevención
- CTAs: "Conocer más", "Descubrir", "Consultar"

### Adaptación por Lead Magnet

**stress-signature (SPARK):**
- Agente protagonista: SPARK
- Tema central: Gestión de energía y estrés
- Conexión: Cómo el estrés sabotea resultados

**ngx-transform (BLAZE):**
- Agente protagonista: BLAZE
- Tema central: Transformación física
- Conexión: Visualización → Realidad con sistema

**logos-dictionary (LOGOS):**
- Agente protagonista: LOGOS
- Tema central: Conocimiento es poder
- Conexión: De términos a sistema completo

**metabolic-age (METABOL):**
- Agente protagonista: METABOL
- Tema central: Edad biológica y longevidad
- Conexión: Revertir el envejecimiento metabólico

---

## Output Esperado

```markdown
# SECUENCIA DE EMAIL: [Nombre]

**Tipo:** [tipo]
**Trigger:** [cuándo se activa]
**Audiencia:** [target]
**Duración:** [X] días

---

## Email 1 - Día 0
**Subject:** [subject line]
**Preview:** [preview text]

[BODY COMPLETO DEL EMAIL]

---

**Métricas Objetivo:**
- Open Rate: [X%]
- Click Rate: [X%]

---

## Email 2 - Día 1
...

---

## Notas de Implementación
- Tags recomendados: [lista]
- Segmentación: [criterios]
- A/B tests sugeridos: [lista]
```

Guarda en: `outputs/emails/$(date +%Y-%m-%d)-$ARGUMENTS.type-sequence.md`

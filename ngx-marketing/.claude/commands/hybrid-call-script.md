---
description: Genera un script de llamada de venta HYBRID personalizado para un lead específico
arguments:
  - name: name
    description: Nombre del lead
    required: true
  - name: qualification
    description: Ruta al archivo de calificación (si existe)
    required: false
  - name: pain_points
    description: Dolores identificados del lead
    required: false
  - name: objections
    description: Objeciones anticipadas
    required: false
  - name: age_range
    description: Rango de edad (30-45 o 45-60)
    default: 30-45
---

# Script de Llamada HYBRID

**Lead:** $ARGUMENTS.name
**Rango de edad:** $ARGUMENTS.age_range
**Dolores:** $ARGUMENTS.pain_points
**Objeciones anticipadas:** $ARGUMENTS.objections

---

## Instrucciones para @hybrid-sales-agent

Genera un script de llamada personalizado de 20-30 minutos.

### PREPARACIÓN PRE-LLAMADA

1. Revisar calificación previa (si existe)
2. Investigar perfil del lead
3. Preparar respuestas a objeciones anticipadas
4. Tener oferta y link de pago listos

### ESTRUCTURA DEL SCRIPT

---

## FASE 1: CONEXIÓN (3 min)

**Objetivo:** Romper el hielo y establecer rapport.

**Apertura personalizada según fuente del lead:**

[Si descargó lead magnet]:
> "Hola [NOMBRE], gracias por tomarte el tiempo. Vi que descargaste [LEAD MAGNET]. ¿Qué fue lo que más te llamó la atención?"

[Si viene de ad]:
> "Hola [NOMBRE], gracias por agendar. Vi que te interesó nuestro anuncio sobre [TEMA]. Cuéntame, ¿qué está pasando con [TEMA] en tu vida ahora mismo?"

[Si es referido]:
> "Hola [NOMBRE], [REFERIDOR] me habló muy bien de ti. Me dijo que estás buscando [OBJETIVO]. ¿Es correcto?"

**Nota de tono:** Usar TÚ para 30-45, considerar USTED para 45-60 si el lead parece formal.

---

## FASE 2: DESCUBRIMIENTO (7 min)

**Objetivo:** Entender el dolor real y confirmar que es candidato HYBRID.

**Preguntas de profundización:**

> "Cuéntame un poco de tu historia con el fitness. ¿Cuánto tiempo llevas intentando [OBJETIVO]?"

[ESCUCHAR - NO INTERRUMPIR]

> "¿Qué has intentado antes? ¿Apps, gym, dietas, coaches?"

[ESCUCHAR]

> "¿Y qué pasó? ¿Por qué no funcionó?"

[ESCUCHAR - Esta es la pregunta clave]

> "En una escala del 1-10, ¿qué tan disciplinado te consideras con el ejercicio?"

[Si dice menos de 7, es señal HYBRID]

> "¿Qué es lo que más te frustra de tu situación actual?"

[ESCUCHAR - Identificar el dolor emocional]

---

## FASE 3: AGITACIÓN (5 min)

**Objetivo:** Hacer el dolor presente e insoportable.

**Reflejo del dolor:**

> "Déjame ver si entendí bien. Llevas [X TIEMPO] intentando [OBJETIVO]. Has probado [INTENTOS PREVIOS]. Y sigues en el mismo lugar. ¿Es correcto?"

[PAUSA - Esperar confirmación]

**Consecuencias:**

> "¿Qué crees que va a pasar si sigues haciendo lo mismo los próximos 6 meses?"

[PAUSA LARGA - Dejar que procesen]

> "¿Y en 2 años?"

[PAUSA]

**Contraste:**

> "Ahora imagina lo opuesto. Imagina que en 3 meses ya [OBJETIVO LOGRADO]. ¿Cómo cambiaría tu vida?"

[Dejar que visualicen el éxito]

---

## FASE 4: SOLUCIÓN (5 min)

**Objetivo:** Presentar HYBRID como el puente entre su dolor y su meta.

**Introducción del sistema:**

> "Lo que describes es exactamente para lo que creamos HYBRID. No es solo una app. No es solo coaching. Es ambos trabajando juntos."

**Los 13 agentes:**

> "Por un lado tienes 13 especialistas de IA trabajando 24/7: uno para tu entrenamiento, otro para nutrición, otro para recuperación, otro para sueño... todos coordinados para ti."

**El coaching humano:**

> "Por otro lado tienes una llamada semanal conmigo donde revisamos tu progreso, ajustamos lo que no está funcionando, y te mantengo accountable."

**La combinación:**

> "¿Sabes por qué las apps fallan? Porque no hay nadie que te empuje. ¿Y por qué el coaching tradicional falla? Porque un humano no puede darte atención 24/7."

> "HYBRID resuelve ambos problemas. ¿Tiene sentido?"

---

## FASE 5: OFERTA (5 min)

**Objetivo:** Presentar precio con confianza y justificación de valor.

**La inversión:**

> "HYBRID es una inversión de $199 al mes, con un compromiso mínimo de 3 meses."

[PAUSA - Dejar que procesen el precio]

**El desglose:**

> "Son $597 en total por:
> - Acceso completo a los 13 agentes IA ($99/mes de valor)
> - Llamada semanal de coaching 1:1 ($200/mes de valor)  
> - Ajustes personalizados según tu progreso
> - Acceso directo por WhatsApp entre llamadas
> - Un sistema probado que ya funciona"

**La garantía:**

> "Y tenemos una garantía: si después de 30 días de uso activo no ves progreso, te devolvemos el primer mes completo. Sin preguntas."

**Escasez (si aplica):**

> "Solo trabajo con [X] clientes HYBRID al mismo tiempo para poder dar atención real. Ahora mismo tengo [X] lugares disponibles."

---

## FASE 6: CIERRE (5 min)

**Objetivo:** Obtener decisión.

**Pregunta de cierre:**

> "Basado en todo lo que hablamos, creo que HYBRID es exactamente lo que necesitas para finalmente [OBJETIVO]. ¿Qué preguntas tienes antes de empezar?"

[MANEJAR OBJECIONES - Ver sección abajo]

**Cierre alternativo:**

> "¿Prefieres pagar los 3 meses de una vez con 10% de descuento ($537), o mes a mes ($199)?"

**Si dice que sí:**

> "Excelente. Te mando el link de pago ahora mismo. Una vez confirmado, agendamos tu primera sesión de onboarding esta semana."

---

## MANEJO DE OBJECIONES PERSONALIZADAS

[Generar respuestas específicas basadas en $ARGUMENTS.objections]

### Objeción: Precio
[Respuesta personalizada]

### Objeción: Tiempo
[Respuesta personalizada]

### Objeción: Necesito pensarlo
[Respuesta personalizada]

---

## NOTAS POST-LLAMADA

Documentar:
- [ ] ¿Cerró? Sí/No
- [ ] Si no cerró, ¿por qué?
- [ ] Objeciones reales vs anticipadas
- [ ] Siguiente paso acordado
- [ ] Fecha de follow-up

---

## Output

Guarda en: `outputs/hybrid/$(date +%Y-%m-%d)-$ARGUMENTS.name-call-script.md`

# Prompts Probados — B2B Sales Command Center

> Prompts optimizados para ventas B2B. En B2B no vendemos en la primera interacción. Creamos champions.

---

## 🔍 Prospección

### Investigación de Prospecto
```
Investiga al prospecto [NOMBRE/EMPRESA] para preparar outreach.

Buscar:
- Tamaño del negocio (clientes, revenue estimado)
- Servicios que ofrece
- Presencia digital (web, redes)
- Dolor probable según perfil
- Ángulo de entrada ideal

Guardar en: outputs/pipeline/research-[nombre]-[fecha].md
```

### Calificación de Lead B2B
```
Evalúa si [NOMBRE] es buen fit para Founding Coaches.

Criterios:
- [ ] Mínimo 5-10 clientes activos
- [ ] Presencia digital activa
- [ ] Frustración con escalar visible
- [ ] Apertura a tecnología
- [ ] Capacidad de dar feedback

Output: Score (1-10) + recomendación (Pursue/Nurture/Pass)
```

---

## 📧 Emails B2B

### Primer Contacto (Cold)
```
Genera email de primer contacto para [NOMBRE], [TIPO: coach/gym/clínica].

Dolor identificado: [DOLOR]
Ángulo de entrada: [POR QUÉ NGX LES AYUDA]

Estructura:
1. Hook personalizado (referencia específica a ellos)
2. Observación sobre su negocio
3. Problema que probablemente tienen
4. Una línea sobre cómo ayudamos
5. CTA simple (responder o 15 min call)

Máximo 150 palabras. Sin pitch largo.
```

### Secuencia de Follow-up
```
Genera 3 follow-ups para [NOMBRE] que no respondió.

Email original enviado: [FECHA]
Resumen del mensaje: [RESUMEN]

Cadencia: 3-5-7 días
Cada follow-up debe agregar valor nuevo, no solo "checking in".
```

### Email Post-Llamada
```
Genera email de seguimiento después de llamada con [NOMBRE].

Puntos discutidos: [LISTA]
Objeciones: [LISTA]
Próximo paso acordado: [DESCRIPCIÓN]

Incluir recap + respuesta a objeciones + CTA claro.
```

---

## 📞 Scripts de Llamada

### Discovery Call (20-30 min)
```
Genera script de discovery call para [TIPO DE PROSPECTO].

Estructura:
1. Apertura + agenda (2 min)
2. Sobre su negocio actual (5 min)
3. Dolores y frustraciones (8 min)
4. Qué han intentado (3 min)
5. Visión ideal (3 min)
6. Introducir NGX brevemente (5 min)
7. Próximos pasos (3 min)

Incluir preguntas clave y señales de fit/no-fit.
```

### Llamada de Cierre Founding Coaches
```
Genera script para cerrar Founding Coach con [NOMBRE].

Background: [RESUMEN DE CALLS ANTERIORES]
Objeciones anticipadas: [LISTA]

Precio: $0 × 3 meses (piloto) → $199/mes después (vs $299 regular)

Incluir manejo de objeciones y transición a onboarding.
```

### Manejo de Objeciones B2B
```
Genera respuestas para estas objeciones:

1. "Es muy caro / No tengo presupuesto"
2. "Mis clientes no usarían una app"
3. "Ya tengo mi sistema"
4. "No tengo tiempo para aprender"
5. "Necesito consultarlo con mi socio"

Por cada una: Validar → Reframe → Pregunta → Transición
```

---

## 📄 Propuestas

### Propuesta Coach Individual
```
Genera propuesta para [NOMBRE], coach con [N] clientes.

Dolor principal: [DOLOR]
Objetivo: [OBJETIVO]

Estructura:
1. Resumen ejecutivo
2. Entendimiento de su situación
3. Solución: Founding Coaches Program
4. Qué incluye
5. Timeline
6. Inversión ($0 piloto → $199/mes)
7. Próximos pasos

Guardar en: outputs/proposals/
```

### Propuesta Gym/Studio
```
Genera propuesta para [NOMBRE], [gym/studio] con [N] coaches.

Ajustar enfoque:
- Escalar equipo completo
- ROI en retención de clientes
- Integración con operación actual

Pricing: Por coach o flat fee según tamaño.
```

---

## 📊 Pipeline

### Reporte Semanal de Pipeline
```
Genera reporte de pipeline.

Incluir:
- Prospectos nuevos
- Contactados
- Calls completadas
- Propuestas enviadas
- Deals cerrados/perdidos

Formato: Resumen + Funnel + Calientes + Blockers + Acciones
Guardar en: outputs/reports/
```

### Post-Mortem Deal Perdido
```
Analiza por qué perdimos a [NOMBRE].

Etapa donde se perdió: [ETAPA]
Objeción final: [OBJECIÓN]

Preguntas:
- ¿Era fit real?
- ¿Qué señales ignoramos?
- ¿Qué haríamos diferente?
```

---

## 📱 LinkedIn B2B

### Contenido para LinkedIn
```
Genera [3-5] posts de LinkedIn B2B.

Tema: [TEMA]
Audiencia: Coaches, dueños de gyms
Objetivo: [Awareness/Engagement/Leads]

Por post: Hook + Body + CTA sutil + Hashtags
```

### Mensaje de Conexión
```
Genera mensaje de conexión para [TIPO].

Máximo 300 chars. NO pitch. Razón clara para conectar.
Punto en común si existe: [PUNTO]
```

---

## 📚 Case Studies

### Case Study Founding Coach
```
Genera case study de [NOMBRE].

Antes: [SITUACIÓN]
Implementación: [QUÉ HICIERON]
Resultados: [MÉTRICAS]
Quote: [CITA]

Estructura: Desafío → Solución → Implementación → Resultados → Quote
Guardar en: outputs/case-studies/
```

---

**RECORDATORIO:** En B2B, el objetivo es crear champions que se vendan la idea internamente, no cerrar en la primera llamada.

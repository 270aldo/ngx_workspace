# NGX B2B SALES COMMAND CENTER

> **Centro de Comando de Ventas B2B para NGX GENESIS**
> Version: 1.0.0 | Diciembre 2025

---

## ⚠️ PRIMERA INSTRUCCIÓN - MEMORIA Y CONTEXTO

### Archivos de Este Workspace

| Archivo | Propósito | Leer al inicio? |
|---------|-----------|-----------------|
| `MEMORY.md` | Estado entre sesiones | ✅ Siempre |
| `NGX_CONTEXT.md` | Contexto general NGX | ✅ Siempre |
| `DECISIONS.md` | Decisiones tomadas | ✅ Siempre |
| `DO_NOT.md` | Errores a evitar | ✅ Siempre |
| `CHECKLIST.md` | Calidad pre-entrega | Al entregar |
| `PROMPTS.md` | Prompts probados | Cuando necesites |
| `TASKS.md` | Tareas frecuentes | Cuando necesites |
| `CROSS_REFERENCES.md` | Refs entre workspaces | Cuando necesites |

### Slash Commands de Sesión

- `/start-session` → Inicializa sesión, lee archivos, resume estado
- `/end-session` → Guarda estado en MEMORY.md, confirma
- `/status` → Muestra estado actual sin modificar nada

### AL INICIAR CADA SESIÓN
```
1. Lee MEMORY.md (estado anterior)
2. Lee NGX_CONTEXT.md (contexto NGX)
3. Lee DECISIONS.md (decisiones vigentes)
4. Lee DO_NOT.md (restricciones)
5. Resume estado al usuario
6. Pregunta si continuar pendiente o hacer algo nuevo
```

### AL TERMINAR CADA SESIÓN
```
1. Actualiza MEMORY.md con:
   - Fecha de sesión
   - Tareas completadas
   - Próxima prioridad
   - Notas relevantes
2. Actualiza DECISIONS.md si hubo decisiones nuevas
3. Confirma al usuario que la memoria fue guardada
```

---

## 🎯 PROPÓSITO DE ESTE WORKSPACE

Este es el centro de comando de ventas B2B para NGX GENESIS. Aquí se gestiona todo el ciclo de ventas B2B: prospección, nurturing, propuestas, cierre y onboarding de coaches.

**Diferencia con B2C:** En B2B no vendemos en la primera llamada. Creamos **champions** que se vendan la idea internamente.

---

## 🧬 CONTEXTO NGX B2B

### Qué es NGX GENESIS for Coaches

> **"El primer equipo de 13 especialistas IA que trabaja CONTIGO"**

NGX GENESIS for Coaches no es otra plataforma de gestión de clientes. Es el primer sistema donde un coach tiene acceso a un **equipo completo de 13 especialistas IA** trabajando junto a él en cada cliente.

### El Problema que Resolvemos

Los trainers profesionales enfrentan un dilema imposible:

| Problema | Impacto |
|----------|---------|
| **Escalar = perder calidad** | Más clientes significa menos atención por persona |
| **Herramientas fragmentadas** | Software de programación + CRM + mensajería + nutrición = caos |
| **Cero inteligencia real** | Las plataformas actuales son bases de datos glorificadas |
| **Tiempo en tareas operativas** | Horas respondiendo preguntas básicas |

### La Solución NGX

> *"No vendes tu tiempo. Vendes el acceso a un equipo de 13 especialistas que trabajan contigo."*

**GENESIS Brain** = El asistente IA del coach que conoce a TODOS sus clientes.

---

## 🏔️ PIRÁMIDE DE MERCADO B2B

La misma infraestructura, diferentes empaques. Cada nivel desbloquea el siguiente.

| Nivel | Cliente | Precio | Propuesta |
|-------|---------|--------|-----------|
| **1. Trainers** | Coaches individuales elite | $299/mes | Escala tu negocio sin perder calidad |
| **2. Studios** | Boutique fitness, CrossFit, Pilates | $500-1,500/mes | Tu app white-label + equipo de agentes |
| **3. Gyms Premium** | Cadenas premium, clubes deportivos | $2,000-5,000/mes | Enterprise + API + analytics avanzados |
| **4. Clínicas** | Rehabilitación, medicina deportiva | $5,000-15,000/mes | Agentes especializados + integración clínica |
| **5. Gobierno** | Salud pública, IMSS | Contrato | Salud para todos |

**FOCO ACTUAL:** Nivel 1 - Trainers individuales (Founding Coaches Program)

---

## 🎖️ FOUNDING COACHES PROGRAM

### Oferta Actual

| Concepto | Valor |
|----------|-------|
| **Piloto (3 meses)** | $0 (a cambio de feedback semanal estructurado) |
| **Post-Piloto** | $199/mes (precio de fundador vs $299 regular) |
| **Setup único** | $299 USD |
| **Clientes incluidos** | Hasta 20-30 activos |
| **Garantía** | 30 días de uso activo o devolución del setup |

### Beneficios Exclusivos Founding Coaches

1. **Acceso anticipado** — Antes del lanzamiento público
2. **Pricing de fundador** — Tarifa garantizada de por vida
3. **Influencia directa** — Feedback moldea el desarrollo
4. **Reconocimiento** — Badge oficial + case study destacado
5. **Red exclusiva** — Grupo privado de Founding Coaches

### Lo Que Incluye

**Para el Coach:**
- Dashboard completo para gestionar clientes
- Consultas ilimitadas a los 13 agentes
- GENESIS Brain (asistente IA personal)
- LOGOS con conexión a PubMed
- Analytics de progreso por cliente
- Onboarding 1:1 personalizado
- Canal directo con Aldo (fundador)

**Para sus Clientes:**
- App GENESIS completa
- Acceso a los 13 agentes especializados
- Temporadas personalizadas automáticas
- Branding del coach visible

---

## 👤 PERFIL DEL FOUNDING COACH IDEAL (ICP)

### Criterios de Calificación

| Criterio | Mínimo | Ideal |
|----------|--------|-------|
| **Clientes activos** | 5-10 | 20+ |
| **Precio por cliente** | $50/mes | $100+/mes |
| **Presencia digital** | Básica | Audiencia establecida |
| **Frustración con herramientas** | Media | Alta |
| **Ubicación** | LATAM | México, Colombia, Argentina |
| **Disposición feedback** | Sí | Entusiasta |

### Señales de Buen Fit

✅ Ya tiene negocio establecido (no está empezando)
✅ Cobra premium por sus servicios
✅ Usa múltiples herramientas que no se integran
✅ Ha intentado escalar y sintió el techo
✅ Valora tecnología como herramienta, no reemplazo
✅ Quiere ser early adopter

### Señales de Mal Fit

❌ Busca solución mágica sin esfuerzo
❌ No tiene clientes actuales
❌ Cobra muy bajo (<$30/cliente)
❌ Resistente a tecnología
❌ No tiene tiempo para dar feedback
❌ Espera que "esté perfecto"

---

## 📞 METODOLOGÍA DE VENTA B2B

### Principio Fundamental

> **NO vendemos en la primera llamada. Creamos CHAMPIONS.**

Un champion es alguien que:
- Entiende profundamente el valor
- Se vende la idea a sí mismo
- Evangeliza internamente (si hay socios/equipo)

### Proceso de Venta (5 Fases)

```
1. PROSPECCIÓN
   └── Identificar → Calificar → Priorizar

2. DESCUBRIMIENTO (Llamada 1)
   └── Conectar → Preguntar → Escuchar → NO vender

3. DEMOSTRACIÓN (Llamada 2)
   └── Visión → Demo → Diferenciadores → Objeciones

4. PROPUESTA (Llamada 3 o async)
   └── Oferta formal → Negociación → Cierre

5. ONBOARDING (Post-venta)
   └── Setup → Training → Primeros 30 días → Feedback loop
```

### Framework de Descubrimiento

**Preguntas clave:**
1. "¿Cuántos clientes manejas actualmente?"
2. "¿Cuál es tu mayor frustración del día a día?"
3. "¿Qué herramientas usas actualmente?"
4. "Si pudieras resolver UNA cosa de tu negocio, ¿cuál sería?"
5. "Si mañana te llegaran 10 clientes nuevos, ¿podrías atenderlos con la misma calidad?"

**La pregunta reveladora:**
> "Si mañana te llegaran 10 clientes nuevos, ¿podrías atenderlos con la misma calidad que a los actuales?"

La respuesta casi siempre es NO. Ese es el dolor.

### Manejo de Objeciones

| Objeción | Respuesta |
|----------|-----------|
| "Es muy caro" | "¿Cuánto tiempo pasas al día en WhatsApp? Si son 2 horas, eso es $X de tu tiempo. GENESIS Brain no reemplaza esas horas, pero las hace más productivas." |
| "No estoy seguro si funciona para mí" | "Por eso existe la garantía. Úsalo 30 días activamente. Si no ves mejora, te devuelvo el setup." |
| "Necesito pensarlo" | "Totalmente válido. ¿Qué es lo que necesitas pensar exactamente? Los lugares de Founding Coach son limitados..." |
| "La IA no puede reemplazar mi toque personal" | "100% de acuerdo. GENESIS Brain trabaja CONTIGO, no en lugar de ti. Es como tener un equipo de asistentes." |

---

## 📊 KPIs Y MÉTRICAS B2B

### Pipeline Metrics

| Métrica | Meta |
|---------|------|
| Prospects identificados/mes | 20-30 |
| Llamadas de descubrimiento/mes | 10-15 |
| Demos realizadas/mes | 5-8 |
| Propuestas enviadas/mes | 3-5 |
| Cierres/mes | 1-2 |
| Conversion rate (prospect→demo) | 30-50% |
| Conversion rate (demo→cierre) | 30-40% |

### Revenue Metrics

| Fase | Coaches | MRR | ARR |
|------|---------|-----|-----|
| **Founding (Mes 3)** | 5 | $2,495 | $29,940 |
| **Growth (Mes 6)** | 15 | $7,485 | $89,820 |
| **Scale (Mes 12)** | 50 | $24,950 | $299,400 |

### Onboarding Metrics

| Métrica | Meta |
|---------|------|
| Tiempo a primera sesión | <48 horas |
| Uso diario GENESIS Brain (por coach) | 3-5 consultas |
| NPS de coaches | >50 |
| Churn rate mensual | <5% |

---

## 📧 CANALES DE COMUNICACIÓN B2B

### Outbound

| Canal | Uso | Frecuencia |
|-------|-----|------------|
| **Email directo** | Outreach inicial, follow-ups | 2-3/semana por prospect |
| **LinkedIn DM** | Conexión inicial, contenido | Diario |
| **WhatsApp** | Post-conexión, cierre | Según relación |
| **Llamada** | Discovery, demo, cierre | Agendadas |

### Content Marketing B2B

| Tipo | Canal | Frecuencia |
|------|-------|------------|
| Posts educativos | LinkedIn | 3-4/semana |
| Case studies | LinkedIn + Email | 1/mes |
| Behind the scenes | LinkedIn Stories | 2-3/semana |
| Webinars/Lives | LinkedIn Live | 1/mes |
| Newsletter B2B | Email | 1/semana |

---

## 🎨 VOZ B2B NGX

### Diferencias con B2C

| Aspecto | B2C | B2B |
|---------|-----|-----|
| **Tratamiento** | Tú/Usted según edad | Tú (peer-to-peer) |
| **Tono** | Confrontacional + educativo | Consultivo + colaborativo |
| **Foco** | Transformación personal | ROI del negocio |
| **Urgencia** | Emocional | Racional (escasez real) |
| **Proof** | Testimoniales | Case studies + métricas |

### Principios de Comunicación B2B

1. **Peer-to-peer** — Hablo como colega, no como vendedor
2. **Problema primero** — Siempre empiezo por su dolor
3. **ROI claro** — Traduzco beneficios a números
4. **Escasez real** — Solo 10 lugares de Founding Coaches (verdad)
5. **Fundador presente** — Aldo está disponible directamente

### Frase Clave

> "Nuestra competencia es a la vez nuestros clientes. Los trainers que querrían competir conmigo, desde el día que vean lo que NGX puede hacer, lo querrán para ellos."

---

## 🤖 SUBAGENTS DISPONIBLES

| Agent | Descripción | Modelo |
|-------|-------------|--------|
| `@prospect-researcher` | Investigar y calificar leads B2B | Sonnet |
| `@sales-script-writer` | Scripts de llamadas de venta | Opus |
| `@proposal-architect` | Propuestas y one-pagers | Opus |
| `@b2b-email-architect` | Secuencias de email B2B | Opus |
| `@linkedin-strategist` | Contenido y outreach LinkedIn | Sonnet |
| `@case-study-creator` | Crear case studies de coaches | Opus |
| `@pipeline-analyst` | Análisis de pipeline y forecasting | Sonnet |
| `@onboarding-designer` | Diseñar experiencias de onboarding | Sonnet |

---

## ⚡ COMANDOS PRINCIPALES

```bash
# Investigar un prospect
/prospect-research name="Juan Pérez" instagram=@juanfitness

# Generar script de llamada de descubrimiento
/sales-script type=discovery prospect="Juan Pérez"

# Crear propuesta formal
/proposal-create prospect="Juan Pérez" tier=founding

# Generar secuencia de email B2B
/email-sequence-b2b type=outreach industry=crossfit

# Crear case study
/case-study coach="María García" results="duplicó clientes en 60 días"

# Reporte de pipeline
/pipeline-report period=this-month
```

---

## 📁 ESTRUCTURA DEL WORKSPACE

```
ngx-b2b-sales/
├── .claude/
│   ├── agents/        # 8 subagents especializados
│   ├── commands/      # Slash commands
│   └── rules/         # Reglas de voz B2B
├── .mcp.json          # Configuración de MCPs
├── CLAUDE.md          # Este archivo
├── skills/
│   ├── ngx-b2b-voice/
│   └── ngx-sales-methodology/
├── templates/
│   ├── proposals/
│   ├── emails/
│   ├── scripts/
│   └── case-studies/
├── knowledge/         # Documentos de referencia
├── dashboards/
│   └── pipeline-dashboard.html
└── outputs/
    ├── proposals/
    ├── emails/
    ├── scripts/
    ├── reports/
    └── pipeline/
```

---

## 🎯 FASES DE CRECIMIENTO

### Fase 1: Validación (2025)
- **Objetivo:** Demostrar que el sistema funciona con usuarios reales
- **Meta:** 10 coaches activos, $3,000 MRR, NPS >8
- **Acciones:** Founding Coaches, case studies, documentar resultados

### Fase 2: Escala Inicial (2025-2026)
- **Objetivo:** Crecer base de trainers y abrir nivel studios
- **Meta:** 100 coaches, 5 studios, $30,000 MRR
- **Acciones:** Expandir outreach, primer studio piloto, white-label

### Fase 3: Expansión (2026-2027)
- **Objetivo:** Dominar mercado LATAM y abrir nivel enterprise
- **Meta:** 1,000 trainers, 50 studios, $150,000+ MRR
- **Acciones:** México, Colombia, Argentina, gyms premium

### Fase 4: Diversificación (2027-2029)
- **Objetivo:** Entrar a verticales de salud especializada
- **Meta:** Clínicas de rehabilitación, medicina deportiva
- **Acciones:** Agentes especializados, integraciones clínicas

### Fase 5: Misión (2029-2030)
- **Objetivo:** Impacto a nivel nacional
- **Meta:** Piloto con gobierno, app gratuita para seguro social
- **Acciones:** Caso de negocio sector público

---

## 📋 CHECKLIST DE VENTA

### Pre-Llamada de Descubrimiento
- [ ] Investigué el perfil del prospect
- [ ] Conozco su audiencia y contenido
- [ ] Identifiqué posibles dolores
- [ ] Preparé preguntas de descubrimiento
- [ ] Tengo claro que NO voy a vender

### Post-Llamada de Descubrimiento
- [ ] Documenté dolores identificados
- [ ] Califiqué el prospect (A/B/C)
- [ ] Agendé siguiente paso
- [ ] Envié resumen por email
- [ ] Actualicé pipeline

### Pre-Demo
- [ ] Personalicé la demo según dolores
- [ ] Preparé respuestas a objeciones probables
- [ ] Tengo lista la oferta Founding Coaches
- [ ] Preparé one-pager para enviar después

### Post-Cierre
- [ ] Envié link de pago
- [ ] Agendé onboarding 1:1
- [ ] Agregué a grupo de Founding Coaches
- [ ] Inicié proceso de case study

---

## 🔗 REFERENCIAS CRUZADAS

### Cuándo Usar Otros Workspaces

| Si necesitas... | Usa... |
|-----------------|--------|
| Email sequences para nurturing | `ngx-marketing` |
| PRD para feature de NGX COACH | `ngx-product-studio` |
| Video para demo/propuesta | `ngx-content-studio` |
| Landing page copy | `ngx-marketing` |

### Cómo Compartir Entre Workspaces

1. Genera el output en el workspace correcto
2. Copia el archivo a `knowledge/` de este workspace si lo usarás frecuentemente
3. Referencia la ubicación en MEMORY.md

### Archivos Compartidos (Idénticos en Todos)

- `NGX_CONTEXT.md` — Contexto general de NGX
- `DO_NOT.md` — Errores a evitar
- `CHECKLIST.md` — Verificación pre-entrega

---

*NGX GENESIS — "Rinde hoy. Vive mejor mañana."*

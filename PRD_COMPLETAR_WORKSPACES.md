# PRD: Completar NGX Workspaces

> Product Requirements Document para completar los 6 workspaces de NGX.

**Versión:** 1.0
**Fecha:** Diciembre 2025
**Autor:** NGX Operations
**Status:** Ready for Implementation

---

## 1. Resumen Ejecutivo

### Qué Existe

6 workspaces de configuración para Claude Code/Desktop:
- NGX Marketing Command Center
- NGX B2B Sales Command Center
- NGX Content Studio
- NGX Product Studio
- NGX Operations Hub
- NGX Finance

### Qué Falta

| Workspace | Faltante |
|-----------|----------|
| Marketing | Templates de ads, landing, social |
| B2B Sales | Templates de proposals, scripts, case studies |
| Content Studio | Dashboard, Skills (VEO, SORA, ElevenLabs) |
| Product Studio | Dashboard de PRDs |
| Operations | Dashboard de métricas, Templates de SOPs |
| Finance | Dashboard financiero, Templates de facturas/reportes |

### Objetivo

Completar cada workspace para que sea 100% funcional y autosuficiente.

---

## 2. Estado Actual por Workspace

### 2.1 NGX Marketing Command Center

**Ubicación:** `ngx-marketing/`

**Completo:**
- ✅ CLAUDE.md (456 líneas)
- ✅ 8 agentes con contenido completo
- ✅ 13 comandos definidos
- ✅ 3 skills (brand-voice, hybrid-sales, funnel-criteria)
- ✅ 2 dashboards HTML (hybrid-sales, funnel-audit)
- ✅ Sistema de memoria
- ✅ 1 template de email (welcome-sequence)

**Faltante:**
- ❌ Templates de ads (Meta, Google, LinkedIn)
- ❌ Templates de landing pages
- ❌ Templates de social posts
- ❌ Templates de copy para diferentes formatos

**Prioridad:** Alta

---

### 2.2 NGX B2B Sales Command Center

**Ubicación:** `ngx-b2b-sales/`

**Completo:**
- ✅ CLAUDE.md completo
- ✅ 8 agentes
- ✅ 11 comandos
- ✅ 2 skills (b2b-voice, sales-methodology)
- ✅ 1 dashboard HTML (pipeline)
- ✅ Sistema de memoria

**Faltante:**
- ❌ Template de proposal (Founding Coaches)
- ❌ Template de proposal (Gyms/Studios)
- ❌ Template de case study
- ❌ Templates de emails B2B por etapa
- ❌ Template de script de llamada

**Prioridad:** Alta

---

### 2.3 NGX Content Studio

**Ubicación:** `ngx-content-studio/`

**Completo:**
- ✅ CLAUDE.md completo
- ✅ 6 agentes
- ✅ 7 comandos
- ✅ 1 regla (content-standards)
- ✅ Sistema de memoria
- ✅ Database de agentes (all-agents.md)

**Faltante:**
- ❌ Dashboard de producción de contenido
- ❌ Skill de VEO 3.1 (integrar desde skills del proyecto)
- ❌ Skill de SORA 2 (integrar desde skills del proyecto)
- ❌ Skill de ElevenLabs
- ❌ Templates de podcast (estructura de episodio)
- ❌ Templates de video (shot list, storyboard)
- ❌ Templates de prompts para imagen

**Prioridad:** Media

---

### 2.4 NGX Product Studio

**Ubicación:** `ngx-product-studio/`

**Completo:**
- ✅ CLAUDE.md completo
- ✅ 4 agentes
- ✅ 7 comandos
- ✅ 1 regla (prd-standards)
- ✅ Sistema de memoria
- ✅ 2 templates PRD (standard, adk-a2a)
- ✅ 2 templates context (claude-context, master-prompt)

**Faltante:**
- ❌ Dashboard de PRDs activos/completados
- ❌ Template de PRD para workflows n8n
- ❌ Template de PRD para features mobile
- ❌ Template de PRD para features web

**Prioridad:** Media

---

### 2.5 NGX Operations Hub

**Ubicación:** `ngx-operations/`

**Completo:**
- ✅ CLAUDE.md completo
- ✅ 4 agentes
- ✅ 9 comandos
- ✅ 1 regla (ops-standards)
- ✅ Sistema de memoria
- ✅ PROMPTS.md con 10 prompts
- ✅ TASKS.md con flujos

**Faltante:**
- ❌ Dashboard de métricas operativas
- ❌ Template de SOP estándar
- ❌ Template de daily checklist
- ❌ Template de weekly review
- ❌ Template de monthly report
- ❌ SOPs iniciales (onboarding cliente, publicar contenido, etc.)

**Prioridad:** Alta

---

### 2.6 NGX Finance

**Ubicación:** `ngx-finance/`

**Completo:**
- ✅ CLAUDE.md completo
- ✅ 3 agentes
- ✅ 9 comandos
- ✅ 1 regla (finance-standards)
- ✅ Sistema de memoria
- ✅ PROMPTS.md con 10 prompts
- ✅ TASKS.md con flujos

**Faltante:**
- ❌ Dashboard financiero (MRR, runway, burn rate)
- ❌ Template de factura NGX
- ❌ Template de P&L mensual
- ❌ Template de proyección financiera
- ❌ Template de budget tracking

**Prioridad:** Alta

---

## 3. Especificaciones de lo Faltante

### 3.1 Dashboards HTML

**Estilo requerido:**
- Dark theme: fondo `#0D0D0D`, cards `#1A1A1A`
- Acento violeta: `#6D00FF`
- Tipografía: Space Grotesk (headers), Inter (body)
- Glassmorphism sutil en cards
- Interactividad con JavaScript vanilla
- Responsive (mobile-first)

**Referencia:** Ver dashboards existentes en `ngx-marketing/dashboards/`

#### Dashboard: Operations Metrics

**Ubicación:** `ngx-operations/dashboards/ops-metrics-dashboard.html`

**Secciones:**
1. **Header:** Fecha, semana del año
2. **KPIs principales:** Tareas completadas, % cumplimiento, horas trabajadas
3. **Checklist del día:** Lista interactiva
4. **SOPs más usados:** Top 5 con links
5. **Workflows activos:** Status de n8n workflows
6. **Alertas:** Items pendientes >48h

#### Dashboard: Finance Overview

**Ubicación:** `ngx-finance/dashboards/finance-dashboard.html`

**Secciones:**
1. **Header:** Mes actual, estado general (verde/amarillo/rojo)
2. **KPIs principales:** MRR, Runway (meses), Burn rate
3. **Gráfico:** MRR últimos 6 meses (si hay datos)
4. **Breakdown gastos:** Por categoría con % del total
5. **Clientes:** Activos por producto
6. **Alertas:** Gastos sobre presupuesto, runway bajo

#### Dashboard: Content Production

**Ubicación:** `ngx-content-studio/dashboards/content-production-dashboard.html`

**Secciones:**
1. **Header:** Semana de contenido
2. **Pipeline:** Contenido en producción por etapa
3. **Calendario:** Vista semanal de publicaciones
4. **Assets:** Videos/imágenes pendientes de crear
5. **Métricas:** Posts esta semana, engagement promedio

#### Dashboard: PRD Tracker

**Ubicación:** `ngx-product-studio/dashboards/prd-tracker-dashboard.html`

**Secciones:**
1. **PRDs activos:** Lista con status
2. **PRDs completados:** Archivo
3. **Handoffs pendientes:** Listos para coding agents
4. **Timeline:** Roadmap visual simplificado

---

### 3.2 Templates

#### Marketing Templates

**`templates/ads/meta-ad-template.md`**
```markdown
# Template: Meta Ad

## Información Básica
- **Campaña:** [nombre]
- **Objetivo:** [conversión|tráfico|awareness]
- **Audiencia:** [30-45|45-60]
- **Budget diario:** $[X]

## Creative

### Primary Text (125 chars visible)
[Hook principal]

### Headline (40 chars)
[Beneficio clave]

### Description (30 chars)
[CTA o diferenciador]

### CTA Button
[Ver más|Registrarse|Más información]

## Variaciones A/B
### Variación A
- Primary: [texto]
- Headline: [texto]

### Variación B
- Primary: [texto]
- Headline: [texto]

## Notas
- Landing URL: [url]
- Pixel events: [lista]
```

**`templates/ads/google-ad-template.md`**
```markdown
# Template: Google Search Ad

## Configuración
- **Campaña:** [nombre]
- **Keywords:** [lista]
- **Match type:** [broad|phrase|exact]

## Ad Copy

### Headlines (30 chars c/u, mínimo 3)
1. [headline]
2. [headline]
3. [headline]

### Descriptions (90 chars c/u, mínimo 2)
1. [description]
2. [description]

### Display URL Path
ngxgenesis.com/[path1]/[path2]

## Extensions
- Sitelinks: [lista]
- Callouts: [lista]
- Structured snippets: [lista]
```

**`templates/landing/landing-page-template.md`**
```markdown
# Template: Landing Page

## Meta
- **URL:** [url]
- **Objetivo:** [lead magnet|venta|waitlist]
- **Audiencia:** [30-45|45-60]

## Estructura

### Hero Section
- **Headline:** [H1 - problema/solución]
- **Subheadline:** [Expandir propuesta]
- **CTA primario:** [texto botón]
- **Visual:** [descripción imagen/video]

### Problema
- **Headline:** [El problema que resolvemos]
- **Bullets:** 
  - [Dolor 1]
  - [Dolor 2]
  - [Dolor 3]

### Solución
- **Headline:** [Cómo NGX lo resuelve]
- **Descripción sistema:** [párrafo]
- **Agentes destacados:** [cuáles y por qué]

### Social Proof
- **Testimoniales:** [2-3]
- **Métricas:** [si hay]
- **Logos:** [si aplica]

### Oferta
- **Producto:** [ASCEND|HYBRID]
- **Precio:** [$X]
- **Incluye:** [lista]
- **Garantía:** [texto]

### CTA Final
- **Headline:** [Urgencia/refuerzo]
- **Botón:** [texto]

### Footer
- Links legales
- Contacto
```

**`templates/social/social-post-template.md`**
```markdown
# Template: Social Post

## Meta
- **Plataforma:** [Instagram|LinkedIn|Twitter]
- **Tipo:** [carrusel|single|video|story]
- **Objetivo:** [engagement|tráfico|awareness]

## Contenido

### Hook (primera línea)
[Captura atención]

### Body
[Contenido principal]

### CTA
[Acción deseada]

### Hashtags
[Lista de hashtags]

## Visual
- **Descripción:** [qué mostrar]
- **Texto en imagen:** [si aplica]
- **Formato:** [1:1|4:5|16:9|9:16]

## Notas de publicación
- **Mejor hora:** [hora]
- **Día:** [día]
- **Cross-post:** [otras plataformas]
```

---

#### B2B Sales Templates

**`templates/proposals/founding-coach-proposal.md`**
```markdown
# Propuesta: Programa Founding Coaches

**Para:** [Nombre del Coach]
**Fecha:** [fecha]
**Válida hasta:** [fecha + 7 días]

---

## Resumen Ejecutivo

[Nombre], te invitamos a ser parte del grupo exclusivo de Founding Coaches de NGX GENESIS.

**Qué obtienes:**
- 3 meses de acceso gratuito a NGX COACH
- Acceso a los 13 agentes IA para tus clientes
- Precio de fundador garantizado: $199/mes (vs $299 regular)
- Influencia directa en el desarrollo del producto
- Reconocimiento como Founding Coach

**Qué pedimos:**
- Feedback semanal estructurado (15 min)
- Mínimo 3 clientes activos usando el sistema
- Disponibilidad para calls mensuales de producto

---

## El Problema que Resolvemos

[Personalizar según pain points del coach]

---

## La Solución: NGX COACH

### Para Ti (El Coach)
- Dashboard de todos tus clientes
- COACH AI que responde sobre cualquier cliente
- Visibilidad de lo que hacen los 13 agentes
- Control total sobre planes y ajustes

### Para Tus Clientes
- App GENESIS con experiencia premium
- 13 agentes trabajando para ellos
- Tu marca, tu relación, potenciada por IA

---

## Timeline

| Semana | Actividad |
|--------|-----------|
| 1 | Onboarding y setup |
| 2-4 | Primeros clientes activos |
| 5-8 | Iteración basada en feedback |
| 9-12 | Evaluación y decisión de continuidad |

---

## Inversión

| Período | Precio |
|---------|--------|
| Meses 1-3 (Piloto) | $0 |
| Mes 4 en adelante | $199/mes (precio fundador) |
| Precio regular (no-fundador) | $299/mes |

---

## Próximos Pasos

1. Confirmar interés respondiendo este documento
2. Call de 30 min para resolver dudas
3. Firma de acuerdo de Founding Coach
4. Inicio de onboarding

---

**Contacto:**
Aldo — Founder, NGX GENESIS
[email]
[calendario para agendar]

---

*Esta propuesta es confidencial y exclusiva para [Nombre].*
```

**`templates/scripts/discovery-call-script.md`**
```markdown
# Script: Discovery Call B2B

**Duración:** 30 minutos
**Objetivo:** Calificar prospecto, entender necesidades, proponer siguiente paso

---

## Apertura (2 min)

"[Nombre], gracias por tomarte el tiempo. Antes de empezar, ¿tienes los 30 minutos completos o hay algo que debamos considerar?"

[Esperar confirmación]

"Perfecto. Mi objetivo hoy es entender tu situación actual, ver si NGX puede ayudarte, y si tiene sentido, definir un siguiente paso. ¿Te parece bien esa estructura?"

---

## Contexto del Coach (8 min)

### Situación actual
"Cuéntame sobre tu negocio de coaching. ¿Cuántos clientes manejas actualmente?"

"¿Qué tipo de servicios ofreces? ¿Presencial, online, híbrido?"

"¿Cuál es tu ticket promedio por cliente?"

### Herramientas actuales
"¿Qué herramientas usas para gestionar a tus clientes? ¿Programación, seguimiento, comunicación?"

"¿Qué tan satisfecho estás con esas herramientas del 1 al 10?"

### Dolor principal
"Si pudieras resolver UN problema de tu operación mañana, ¿cuál sería?"

---

## Presentación NGX (10 min)

"Basado en lo que me cuentas, déjame explicarte cómo NGX podría ayudarte."

[Adaptar según dolores identificados]

### Demo rápida (si aplica)
"¿Te gustaría ver cómo se ve el dashboard de un coach?"

[Compartir pantalla si es video call]

---

## Calificación (5 min)

### Budget
"El programa Founding Coaches tiene 3 meses gratuitos y después $199/mes. ¿Es algo que encaja en tu presupuesto?"

### Timeline
"¿Cuándo te gustaría tener algo así funcionando?"

### Decision maker
"¿Eres tú quien toma esta decisión o hay alguien más que deba estar involucrado?"

---

## Cierre (5 min)

### Si califica
"Me parece que hay un fit claro. El siguiente paso sería enviarte la propuesta formal del programa Founding Coaches y agendar un call de onboarding. ¿Te funciona?"

### Si no califica
"Aprecio tu tiempo. Creo que en este momento [razón] no hace el mejor fit. ¿Te parece si te mantengo en el radar y te contacto cuando [condición]?"

### Si necesita pensar
"Entiendo. ¿Qué información adicional necesitas para tomar la decisión? Te la envío y agendamos un follow-up de 15 min para [fecha]."

---

## Post-Call

- [ ] Enviar resumen por email en <24h
- [ ] Agregar a CRM con notas
- [ ] Agendar follow-up si quedó pendiente
- [ ] Enviar propuesta si calificó
```

---

#### Operations Templates

**`templates/sop-template.md`**
```markdown
# SOP: [Nombre del Proceso]

**Versión:** 1.0
**Última actualización:** [fecha]
**Responsable:** [quién]
**Tiempo estimado:** [X minutos]

---

## Objetivo

[Qué logra este proceso en una oración]

---

## Trigger

Este proceso se ejecuta cuando:
- [Condición 1]
- [Condición 2]

---

## Prerequisitos

Antes de empezar, asegúrate de tener:
- [ ] [Recurso/acceso 1]
- [ ] [Recurso/acceso 2]
- [ ] [Herramienta necesaria]

---

## Pasos

### 1. [Nombre del paso]

**Acción:** [Verbo + qué hacer específicamente]

**Detalles:**
- [Detalle adicional si necesario]
- [Detalle adicional si necesario]

**Output:** [Qué produce este paso]

---

### 2. [Nombre del paso]

**Acción:** [Verbo + qué hacer específicamente]

**Output:** [Qué produce este paso]

---

### 3. [Nombre del paso]

[Continuar patrón...]

---

## Checklist de Verificación

Al terminar, verifica:
- [ ] [Verificación 1]
- [ ] [Verificación 2]
- [ ] [Verificación 3]

---

## Troubleshooting

### Problema: [Descripción]
**Solución:** [Qué hacer]

### Problema: [Descripción]
**Solución:** [Qué hacer]

---

## Output Esperado

Al completar este proceso debes tener:
- [Output 1]
- [Output 2]

---

## Historial de Cambios

| Versión | Fecha | Cambio |
|---------|-------|--------|
| 1.0 | [fecha] | Creación inicial |
```

**`templates/weekly-review-template.md`**
```markdown
# Weekly Review: Semana [N] — [Fechas]

---

## Resumen Ejecutivo

[2-3 oraciones sobre cómo fue la semana]

---

## Métricas

| Métrica | Esta Semana | Semana Anterior | Δ |
|---------|-------------|-----------------|---|
| Leads nuevos | | | |
| Conversiones | | | |
| Contenido publicado | | | |
| Tareas completadas | | | |

---

## Top 3 Wins

1. **[Win 1]** — [Por qué importa]
2. **[Win 2]** — [Por qué importa]
3. **[Win 3]** — [Por qué importa]

---

## Top 3 Obstáculos

1. **[Obstáculo 1]** — [Qué lo causó] — [Acción tomada o propuesta]
2. **[Obstáculo 2]** — [Qué lo causó] — [Acción tomada o propuesta]
3. **[Obstáculo 3]** — [Qué lo causó] — [Acción tomada o propuesta]

---

## Tareas Completadas

- [x] [Tarea 1]
- [x] [Tarea 2]
- [x] [Tarea 3]

## Tareas No Completadas (carry over)

- [ ] [Tarea 1] — Razón: [por qué no se completó]
- [ ] [Tarea 2] — Razón: [por qué no se completó]

---

## Prioridades Próxima Semana

1. **[Prioridad 1]** — [Criterio de éxito]
2. **[Prioridad 2]** — [Criterio de éxito]
3. **[Prioridad 3]** — [Criterio de éxito]

---

## Notas Adicionales

[Cualquier contexto importante para la siguiente semana]

---

*Generado: [fecha y hora]*
```

---

#### Finance Templates

**`templates/invoices/invoice-template.md`**
```markdown
# FACTURA

**Número:** NGX-[YYYYMM]-[NNN]
**Fecha de emisión:** [fecha]
**Fecha de vencimiento:** [fecha + 15 días]

---

## De

**NGX GENESIS**
[Dirección fiscal]
[RFC si aplica]
[Email de facturación]

---

## Para

**[Nombre del cliente]**
[Dirección]
[RFC si aplica]
[Email]

---

## Detalle

| Concepto | Período | Cantidad | Precio Unitario | Total |
|----------|---------|----------|-----------------|-------|
| [Producto/Servicio] | [fechas] | 1 | $[X] USD | $[X] USD |

---

## Resumen

| | |
|---|---|
| Subtotal | $[X] USD |
| IVA (16%) | $[X] USD |
| **Total** | **$[X] USD** |

---

## Instrucciones de Pago

**Método preferido:** [Stripe/PayPal/Transferencia]

**Transferencia bancaria:**
- Banco: [nombre]
- Cuenta: [número]
- CLABE: [número]
- Beneficiario: [nombre]

**PayPal:** [email]

**Stripe:** [link de pago]

---

## Términos

- Pago a 15 días de la fecha de emisión
- Pagos tardíos pueden incurrir en cargos adicionales
- Para dudas: [email de soporte]

---

*Gracias por tu confianza en NGX GENESIS.*
```

**`templates/reports/monthly-pnl-template.md`**
```markdown
# P&L Mensual: [Mes Año]

---

## Resumen Ejecutivo

| Métrica | Valor | vs Mes Anterior |
|---------|-------|-----------------|
| Ingresos Totales | $[X] | [+/-X%] |
| Gastos Totales | $[X] | [+/-X%] |
| **Resultado Neto** | **$[X]** | [+/-X%] |
| Margen Neto | [X%] | [+/-X pp] |

---

## Ingresos

| Fuente | Clientes | Ingreso | % del Total |
|--------|----------|---------|-------------|
| NGX ASCEND | [N] | $[X] | [X%] |
| NGX HYBRID | [N] | $[X] | [X%] |
| B2B Coaches | [N] | $[X] | [X%] |
| Otros | - | $[X] | [X%] |
| **Total Ingresos** | | **$[X]** | 100% |

---

## Gastos

| Categoría | Monto | % del Total | vs Presupuesto |
|-----------|-------|-------------|----------------|
| Infraestructura | $[X] | [X%] | [+/-X%] |
| APIs IA | $[X] | [X%] | [+/-X%] |
| Marketing | $[X] | [X%] | [+/-X%] |
| Servicios | $[X] | [X%] | [+/-X%] |
| Otros | $[X] | [X%] | [+/-X%] |
| **Total Gastos** | **$[X]** | 100% | [+/-X%] |

### Detalle Infraestructura
- GCP: $[X]
- Supabase: $[X]
- Vercel: $[X]
- Otros: $[X]

### Detalle APIs IA
- Anthropic: $[X]
- Google AI: $[X]
- ElevenLabs: $[X]
- Otros: $[X]

### Detalle Marketing
- Meta Ads: $[X]
- Google Ads: $[X]
- Herramientas: $[X]

---

## Análisis

### Variaciones Significativas

**[Categoría con variación >10%]:**
- Causa: [explicación]
- Acción: [qué se hará]

### Tendencias

[Observaciones sobre tendencias de ingresos/gastos]

---

## Métricas de Negocio

| Métrica | Valor |
|---------|-------|
| MRR | $[X] |
| ARR proyectado | $[X] |
| Clientes activos totales | [N] |
| ARPU | $[X] |
| CAC (este mes) | $[X] |
| Runway (meses) | [N] |

---

## Notas

[Cualquier contexto adicional relevante]

---

*Generado: [fecha]*
```

---

## 4. Skills Faltantes (Content Studio)

### Skill: VEO 3.1

Copiar desde `/mnt/skills/user/ngx-veo31-content-factory/` al workspace:
- `ngx-content-studio/skills/veo31/SKILL.md`

### Skill: SORA 2

Copiar desde `/mnt/skills/user/ngx-sora2-content-factory/` al workspace:
- `ngx-content-studio/skills/sora2/SKILL.md`

### Skill: ElevenLabs

Crear o copiar desde `/mnt/skills/user/ngx-voice-engine/`:
- `ngx-content-studio/skills/elevenlabs/SKILL.md`

---

## 5. Orden de Implementación

### Fase 1: Alta Prioridad (Semana 1)

1. **Operations Hub**
   - [ ] Dashboard de métricas
   - [ ] Template de SOP
   - [ ] Template de weekly review
   - [ ] 3 SOPs iniciales

2. **Finance**
   - [ ] Dashboard financiero
   - [ ] Template de factura
   - [ ] Template de P&L

3. **Marketing**
   - [ ] Template de Meta ads
   - [ ] Template de Google ads
   - [ ] Template de landing page

### Fase 2: Media Prioridad (Semana 2)

4. **B2B Sales**
   - [ ] Template de proposal Founding Coaches
   - [ ] Template de discovery call script
   - [ ] Template de case study

5. **Product Studio**
   - [ ] Dashboard de PRDs

### Fase 3: Baja Prioridad (Semana 3)

6. **Content Studio**
   - [ ] Dashboard de producción
   - [ ] Integrar skills (VEO, SORA, ElevenLabs)
   - [ ] Templates de podcast/video

---

## 6. Criterios de Aceptación

### Para Dashboards

- [ ] Carga sin errores en navegador
- [ ] Dark theme correcto (#0D0D0D, #6D00FF)
- [ ] Responsive en mobile
- [ ] Interactividad funciona (si aplica)
- [ ] Datos de ejemplo incluidos

### Para Templates

- [ ] Formato markdown válido
- [ ] Todas las secciones tienen placeholder claro
- [ ] Instrucciones de uso incluidas
- [ ] Guardado en carpeta correcta

### Para Skills

- [ ] SKILL.md con descripción y triggers
- [ ] Ejemplos incluidos
- [ ] Referencias a documentación externa si aplica

---

## 7. Definición de "Completo"

Un workspace está **completo** cuando:

1. ✅ Todos los comandos definidos producen output útil
2. ✅ Existe al menos 1 dashboard funcional
3. ✅ Existen templates para las tareas principales
4. ✅ Skills necesarios están integrados
5. ✅ MEMORY.md tiene estructura para trackear trabajo
6. ✅ Un usuario nuevo puede usar el workspace sin ayuda externa

---

*PRD v1.0 — NGX Workspaces Completion*

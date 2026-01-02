# NGX MARKETING COMMAND CENTER

> **Workspace de Inteligencia de Marketing para NGX GENESIS**
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

Este es el centro de comando de marketing para NGX GENESIS. Aquí se genera, optimiza y audita todo el contenido de marketing del ecosistema B2C.

**NO es un repositorio de código.** Es un sistema de inteligencia operativa que usa Claude Code CLI para:
- Generar contenido alineado con la voz de marca
- Crear secuencias de email y copy de ventas
- Auditar funnels y landing pages automáticamente
- Conectar con n8n para automatización de workflows

---

## 🧬 CONTEXTO NGX GENESIS

### Qué es NGX
NGX (NEOGEN-X) es un ecosistema de **Performance & Longevity** que usa inteligencia híbrida (IA + humano) para:
- Diseñar temporadas de entrenamiento y hábitos (8/12/16 semanas)
- Ajustar fases y semanas según datos reales (sueño, energía, dolor, adherencia, biomarcadores)
- Explicar al usuario qué hace, por qué y cómo impacta su futuro físico y mental

### Target Principal
Personas de **30-60 años** que buscan:
- Ganar músculo / fuerza
- Perder grasa con criterio
- Mejorar rendimiento y energía diaria
- Cuidar articulaciones y salud metabólica
- Proteger su longevidad física y cognitiva

### Productos B2C
| Producto | Precio | Descripción |
|----------|--------|-------------|
| **ASCEND** | $99/mes | Sistema completo de 13 agentes IA |
| **HYBRID** | $199/mes | Sistema + coaching humano 3 meses |

### Posicionamiento
> **"Performance & Longevity" — Rinde hoy. Vive mejor mañana.**

---

## 💎 MÓDULO HYBRID SALES

### Qué es HYBRID

HYBRID es el producto premium que combina:
- **13 agentes IA** trabajando 24/7 (personalización)
- **Coaching humano semanal** (accountability)

> "HYBRID es para personas que saben que necesitan ayuda para ser consistentes. No es debilidad — es inteligencia."

### HYBRID vs ASCEND

| Aspecto | ASCEND ($99) | HYBRID ($199) |
|---------|--------------|---------------|
| 13 Agentes IA | ✅ | ✅ |
| Temporadas personalizadas | ✅ | ✅ |
| Coaching humano | ❌ | ✅ Semanal |
| Check-ins personalizados | ❌ | ✅ |
| Accountability | Auto-dirigido | Guiado |
| Ideal para | Autodisciplinados | Necesitan guía |

### Calificación HYBRID vs ASCEND

**Señales de HYBRID:**
- Múltiples fracasos previos
- Autodisciplina <6/10
- Prefiere guía sobre autonomía
- Presupuesto $200+/mes
- Edad 40+ (generalmente)

**Señales de ASCEND:**
- Autodisciplinado declarado
- Ya entrena consistentemente
- Sensible al precio
- Prefiere autonomía

### Comandos HYBRID

```bash
# Calificar un lead
/hybrid-qualify name="María" source=lead_magnet lead_magnet=stress-signature

# Generar script de llamada
/hybrid-call-script name="María" pain_points="disciplina,tiempo"

# Reporte de pipeline HYBRID
/hybrid-pipeline period=this-week
```

### Métricas HYBRID

| Métrica | Meta |
|---------|------|
| Leads calificados HYBRID/semana | 5 |
| Llamadas/semana | 3 |
| Tasa de cierre | 33% |
| MRR HYBRID | $796+ |

---

## 🤖 SISTEMA DE 13 AGENTES NGX

### NEXUS/GENESIS — Orquestador Maestro
Coordina al resto de agentes. Recibe eventos y decide qué agentes intervienen.

### Pilar 1: Rendimiento Físico
| Agente | Especialidad |
|--------|--------------|
| **BLAZE** | Entrenamiento de fuerza, hipertrofia, periodización |
| **ATLAS** | Movilidad funcional, prevención, adultos mayores |
| **TEMPO** | Recuperación, HRV, gestión de fatiga |
| **WAVE** | Cardio, resistencia, VO2max |

### Pilar 2: Nutrición
| Agente | Especialidad |
|--------|--------------|
| **SAGE** | Estrategia nutricional, ciencia de la alimentación |
| **METABOL** | Glucosa, biomarcadores, salud hormonal |
| **MACRO** | Comidas prácticas, porciones, timing |
| **NOVA** | Flexibilidad, calidad de movimiento |

### Pilar 3: Mente y Descanso
| Agente | Especialidad |
|--------|--------------|
| **SPARK** | Formación de hábitos, consistencia, motivación |
| **STELLA** | Rendimiento mental, barreras psicológicas |
| **LUNA** | Optimización del sueño, ritmo circadiano |

### Transversal
| Agente | Especialidad |
|--------|--------------|
| **LOGOS** | Educación, explicación, autonomía del usuario |

---

## 📢 VOZ DE MARCA: "VERDAD DIRECTA"

### Definición
> **"Confrontamos con respeto, fundamentamos con ciencia, resolvemos con sistemas."**

### Los 6 Pilares de Comunicación
1. **HONESTIDAD PRIMERO** — Admitir limitaciones antes de vender beneficios
2. **ACCIÓN INMEDIATA** — Toda comunicación termina con un paso concreto
3. **EXPLICACIÓN EFICIENTE** — Simple → Por qué → Detalles (para quien quiera)
4. **CONFIANZA TRANQUILA** — Seguridad sin gritar, sin emojis excesivos
5. **RESPONSABILIDAD VISIBLE** — El fundador está presente, no escondido
6. **HÍBRIDO POR DISEÑO** — IA + Humano según contexto, no por dogma

### Los 3 Modos de Comunicación

| Modo | Nombre | Cuándo se usa | Energía |
|------|--------|---------------|---------|
| **A** | El Experto | Educar, explicar el "por qué" | Media |
| **B** | La Verdad | Confrontar, hooks, romper mitos | Alta |
| **C** | El Arquitecto | Mostrar el sistema, el "cómo" | Reservada |

### Fórmula NGX
**CONFRONTA → FUNDAMENTA → RESUELVE**

### Selector de Modo por Contexto

| Objetivo | Modo |
|----------|------|
| Que entiendan algo (educar) | A - Experto |
| Que paren y presten atención | B - Verdad |
| Que confíen en NGX (convertir) | C - Arquitecto |

| Formato | Modo |
|---------|------|
| Hook / Ad / Reel / Primer frame | B - Verdad |
| Video largo / Blog / Email educativo | A - Experto |
| Landing page / Email de venta / Demo | C - Arquitecto |

---

## 👥 ADAPTACIÓN POR AUDIENCIA

### Audiencia 30-45 años
- **Trato:** Tuteo, directo, sin rodeos
- **Perfil:** Profesionales activos, familiarizados con tecnología
- **Buscan:** Eficiencia, datos, resultados medibles
- **Ejemplo Modo B:** *"Tu app de fitness no tiene idea de que dormiste 4 horas. ¿Y así esperas que te ayude?"*

### Audiencia 45-60 años
- **Trato:** Usted, respetuoso, honesto sobre limitaciones
- **Perfil:** Ejecutivos/profesionales establecidos
- **Buscan:** Longevidad, salud preventiva, credibilidad
- **Ejemplo Modo B:** *"Después de los 45, entrenar igual que a los 30 puede ser contraproducente. Su cuerpo responde diferente ahora — y eso no es debilidad, es biología."*

---

## 🧲 LEAD MAGNETS

| Lead Magnet | Agente | Audiencia | Hook |
|-------------|--------|-----------|------|
| **Stress Signature Analyzer** | SPARK | 30-45 | "Descubre cómo el estrés está saboteando tus resultados" |
| **NGX Transform** | BLAZE | 30-45 | "Ve tu transformación antes de empezar" |
| **LOGOS Dictionary** | LOGOS | Ambas | "El conocimiento te libera" |
| **Metabolic Age Calculator** | METABOL | 45-60 | "Su edad biológica puede ser diferente a la del calendario" |
| **Recovery Score Assessment** | TEMPO | 45-60 | "¿Está recuperándose correctamente?" |
| **Sleep Optimization Guide** | LUNA | 45-60 | "El sueño es el pilar de la longevidad" |

---

## 📊 ARQUITECTURA DEL FUNNEL

```
TOFU (Awareness)
├── Ads → Contenido Educativo → Lead Magnet Landing
├── Meta: Capturar email con valor inmediato
└── KPI: 500-1000 leads/mes

MOFU (Nurture)
├── Email Sequence → Contenido Profundo → Webinar/Demo
├── Meta: Educar y generar confianza
└── KPI: >30% open rate

BOFU (Conversión)
├── Sales Page → Trial/Demo → Conversación SPARK → Compra
├── Meta: Convertir a ASCEND o HYBRID
└── KPI: 15-60 suscriptores/mes
```

---

## 📧 SECUENCIAS DE EMAIL

### Welcome Sequence (7 días)
| Día | Tipo | Contenido |
|-----|------|-----------|
| 0 | Entrega | Bienvenida + acceso al lead magnet |
| 1 | Valor | Contenido educativo relacionado |
| 2 | Historia | Por qué creé NGX (Aldo's story) |
| 4 | Sistema | Cómo funcionan los 13 agentes |
| 6 | Prueba social | Testimonial o caso de uso |
| 7 | Oferta | Invitación a ASCEND |

### Nurture Sequence (Post-Welcome)
- Semana 1: "Por qué los programas genéricos no funcionan"
- Semana 2: "La ciencia de la periodización"
- Semana 3: "Conoce a [AGENTE relevante]"
- Semana 4: "El costo de no tener un sistema"

---

## ⚠️ RESTRICCIONES DE CONTENIDO

### NUNCA usar
- ❌ Arquetipos PRIME/LONGEVITY (obsoletos)
- ❌ "Ejecutivos/CEOs" como segmento principal
- ❌ Promesas absolutas ("garantizado 100%")
- ❌ Mayúsculas excesivas o signos de exclamación repetidos
- ❌ Más de 1-2 emojis por pieza de contenido
- ❌ Cyan como color (usar violeta #6D00FF)
- ❌ Discursos motivacionales vacíos

### SIEMPRE incluir
- ✅ Tratamiento correcto (tú/usted según audiencia)
- ✅ Mención al agente correcto para la función
- ✅ Explicación de términos técnicos si se usan
- ✅ Acción concreta al final
- ✅ Limitaciones antes de beneficios (Honestidad Primero)

---

## 🔧 HERRAMIENTAS DISPONIBLES

### Subagents
- `@content-strategist` — Planificación de contenido semanal/mensual
- `@copywriter-hormozi` — Copy estilo $100M Offers
- `@email-architect` — Secuencias de email completas
- `@social-creator` — Posts para Instagram, Facebook, LinkedIn
- `@ads-specialist` — Copy y creativos para Meta Ads
- `@funnel-analyst` — Análisis de métricas y optimización
- `@funnel-auditor` — Auditoría visual y funcional de landings
- `@hybrid-sales-agent` — Calificación y venta de HYBRID ($199/mes)

### Slash Commands
- `/content-week` — Planifica contenido de la semana
- `/email-sequence` — Genera secuencia de emails
- `/social-batch` — Crea batch de posts sociales
- `/ad-variations` — Genera variaciones de ads
- `/audit-funnel` — Audita una URL del funnel
- `/report-weekly` — Genera reporte semanal de marketing
- `/hybrid-qualify` — Califica lead como HYBRID o ASCEND
- `/hybrid-call-script` — Script personalizado de llamada HYBRID
- `/hybrid-pipeline` — Reporte de pipeline de ventas HYBRID

### MCPs Conectados
- **n8n** — Automatización de workflows
- **Canva** — Generación de diseños
- **Notion** — Documentación y planning
- **Claude-in-Chrome** — Automatización del navegador

---

## 📁 ESTRUCTURA DEL WORKSPACE

```
ngx-marketing/
├── .claude/
│   ├── agents/        # Subagents especializados
│   ├── commands/      # Slash commands
│   └── rules/         # Reglas de comportamiento
├── .mcp.json          # Configuración de MCPs
├── skills/            # Skills locales
│   ├── ngx-brand-voice/
│   └── ngx-funnel-criteria/
├── templates/         # Templates reutilizables
│   ├── emails/
│   ├── social/
│   ├── ads/
│   └── landing/
├── knowledge/         # Documentos de referencia
├── dashboards/        # Dashboards interactivos
└── outputs/           # Contenido generado
    ├── emails/
    ├── social/
    ├── ads/
    ├── reports/
    └── audits/
```

---

## 🎨 IDENTIDAD VISUAL

### Colores
- **Primario:** #6D00FF (Violeta NGX)
- **Fondo:** #0A0A0A (Negro profundo)
- **Cards:** rgba(18,18,18,0.9) → rgba(10,10,10,0.9)
- **Bordes:** rgba(255,255,255,0.05)
- **NUNCA:** Cyan, colores brillantes

### Efectos
- Backdrop blur en cards
- Sombras neón en botones (violeta)
- Gradientes sutiles en fondos
- Hover states con transform
- Múltiples capas de sombras

---

## 📋 CHECKLIST PRE-PUBLICACIÓN

Antes de publicar cualquier contenido:

- [ ] ¿Usé el tratamiento correcto? (tú para 30-45 / usted para 45-60)
- [ ] ¿Evité términos prohibidos?
- [ ] ¿Mencioné al agente correcto para la función?
- [ ] ¿Expliqué términos técnicos si los usé?
- [ ] ¿El contenido termina con una acción concreta?
- [ ] ¿Admití limitaciones antes de vender beneficios?
- [ ] ¿El tono es "Verdad Directa"?
- [ ] ¿Visual usa violeta #6D00FF?
- [ ] ¿Máximo 1-2 emojis estratégicos?

---

## 🚀 COMANDOS RÁPIDOS

```bash
# Planificar semana de contenido
/content-week audience=30-45 focus=awareness

# Generar secuencia de email para lead magnet
/email-sequence lead_magnet="Stress Signature" days=7

# Crear batch de 10 posts sociales
/social-batch platform=instagram count=10 theme=education

# Auditar landing page
/audit-funnel https://ngxgenesis.com/stress-signature type=full

# Generar reporte semanal
/report-weekly
```

---

## 🔗 REFERENCIAS CRUZADAS

### Cuándo Usar Otros Workspaces

| Si necesitas... | Usa... |
|-----------------|--------|
| Copy para propuesta B2B | `ngx-b2b-sales` (ya tiene templates) |
| PRD para nueva feature | `ngx-product-studio` primero |
| Scripts de video/podcast | `ngx-content-studio` |
| Prompts para imágenes | `ngx-content-studio` |

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

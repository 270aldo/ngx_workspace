# NGX GENESIS — Contexto Compartido

> **Documento de referencia para todos los workspaces NGX**
> Fuente: MASTER SOURCE OF TRUTH V9.0

---

## 1. ¿Qué es NGX?

**NGX GENESIS** es una plataforma de **Performance & Longevity** que combina inteligencia artificial y coaching humano para diseñar temporadas inteligentes de entrenamiento, nutrición y hábitos.

**Tagline:** *"Rinde hoy. Vive mejor mañana."*

**Posicionamiento único:** Performance + Longevity integrados, no separados.

---

## 2. Filosofía Core

> **"Conocimiento es poder. IA es amplificador. Humanos somos directores."**

### Principios Operativos

- **Temporadas, no rutinas random** — Programas de 8/12/16 semanas con fases claras
- **IA + Humano > IA o Humano** — Modelo híbrido (HIE)
- **Educación como diferenciador** — LOGOS enseña el "por qué"
- **Anti-humo por diseño** — Principios sólidos > tendencias virales
- **Números cerrados** — $99, $499, no $97 o $497

### Comunicación: Verdad Directa

- Confrontar con respeto
- Fundamentar con ciencia
- Resolver con sistemas

---

## 3. Target Audience

**Primario:** Profesionales 30-60 años que se toman en serio su salud

**Características:**
- Valoran eficiencia y datos
- Dispuestos a invertir en resultados
- Buscan guía experta, no solo información
- Quieren entender el "por qué"

**NO es para:**
- Curiosos sin compromiso
- Quienes buscan soluciones mágicas
- Menores de 30 sin historial de entrenamiento

---

## 4. Sistema de 13 Agentes

### NEXUS — Orquestador Maestro

Coordina todo el sistema. Recibe eventos, decide qué agentes intervienen, resuelve conflictos entre propuestas.

### Pilar 1: Rendimiento Físico

| Agente | Rol | Descripción |
|--------|-----|-------------|
| **BLAZE** | Entrenamiento principal | Fuerza, hipertrofia, periodización |
| **ATLAS** | Funcionalidad | Movilidad funcional, prevención, longevidad física |
| **TEMPO** | Recuperación | HRV, deload, gestión de estrés |
| **WAVE** | Cardio | VO2max, resistencia, zonas cardíacas |

### Pilar 2: Nutrición

| Agente | Rol | Descripción |
|--------|-----|-------------|
| **SAGE** | Estrategia nutricional | Ciencia nutricional, el "por qué" |
| **METABOL** | Salud metabólica | Glucosa, biomarcadores, hormonas |
| **MACRO** | Ejecución nutricional | Comidas prácticas, porciones, timing |

### Pilar 3: Comportamiento

| Agente | Rol | Descripción |
|--------|-----|-------------|
| **NOVA** | Movilidad | Flexibilidad, calidad de movimiento |
| **SPARK** | Hábitos | Formación de hábitos, consistencia |

### Pilar 4: Datos

| Agente | Rol | Descripción |
|--------|-----|-------------|
| **STELLA** | Data Orchestrator | Recopila y analiza datos de entrenamiento, sueño, biomarcadores |

### Pilar 5: Salud Femenina

| Agente | Rol | Descripción |
|--------|-----|-------------|
| **LUNA** | Women's Health | Ciclo, perimenopausia, menopausia, PCOS |

### Capa Transversal: Educación

| Agente | Rol | Descripción |
|--------|-----|-------------|
| **LOGOS** | Educación | Traduce decisiones en explicaciones, módulos educativos, quizzes |

---

## 5. Arquitectura de Producto

### NGX ENGINE

Motor central de personalización que convierte datos, objetivos y contexto en:

- **Temporadas** — 8/12/16 semanas de programa completo
- **Fases** — 4-6 semanas (acumulación, intensificación, refinamiento, recuperación)
- **Semanas** — Microciclos con distribución de fuerza, cardio, movilidad

Ajusta:
- **Día a día** → Volumen/intensidad según recuperación y dolor
- **Semana a semana** → Según adherencia y progreso
- **Cambio de fase** → Según datos acumulados y fatiga

### HIE (Hybrid Intelligence Engine)

**HIE = NGX ENGINE + Coach humano + Consola NGX COACH**

- El usuario siempre usa la misma app: GENESIS
- Cuando entra HIE, se le asigna un coach
- El coach trabaja en NGX COACH (consola web)
- NGX ENGINE genera propuestas → coach afina y valida
- LOGOS explica al usuario lo que está ocurriendo

**Principio:** La IA no reemplaza al coach, lo potencia.

### LOGOS

Capa educativa transversal que:
- Traduce decisiones del sistema en explicaciones
- Genera módulos educativos y micro-quizzes
- Responde "¿Por qué?" en cada decisión
- Apoya al coach en modo HIE

---

## 6. Productos y Precios

### B2C — Precios Oficiales

| Plan | Precio | Estructura | Incluye |
|------|--------|------------|---------|
| **NGX ASCEND** | **$100 USD/mes** | Compromiso 3 meses = $300/temporada | GENESIS completo, NGX ENGINE, LOGOS, STELLA básico. Sin coach humano. |
| **NGX HYBRID** | **$1,200 USD/temporada** | Pago único (12 semanas) | Todo ASCEND + coach humano semanal, onboarding 1:1, check-ins semanales, review de temporada. |

### Filosofía de Temporadas

- **NGX vende TEMPORADAS, no suscripciones mensuales**
- Una temporada = programa completo con inicio y fin
- ASCEND: 3 meses mínimo (1 temporada)
- HYBRID: 12 semanas de coaching intensivo
- El usuario ve: Temporada → Fases → Semanas → "Qué toca hoy"

### Números Cerrados

- $100, $300, $1,200 — NO $99, $297, $1,197
- Refleja posicionamiento premium y Verdad Directa
- Filtra curiosos, atrae comprometidos

### B2B — GENESIS for Coaches

| Plan | Precio | Descripción |
|------|--------|-------------|
| **Founding Coaches (Piloto)** | $0 × 3 meses | A cambio de feedback semanal estructurado |
| **Founding Coaches (Post-piloto)** | $199/mes | Tarifa de fundador garantizada (vs $299 regular) |
| **Precio Regular** | $299/mes | Acceso completo a NGX COACH + agentes para sus clientes |

---

## 7. Stack Técnico (Resumen)

| Capa | Tecnología |
|------|------------|
| **Mobile (GENESIS)** | Expo SDK 54, React Native 0.81 |
| **Web (NGX COACH)** | Next.js 15, React 19 |
| **Backend** | FastAPI microservices, Cloud Run |
| **Database** | Supabase PostgreSQL 16, RLS habilitado |
| **AI Platform** | Vertex AI Agent Builder + Agent Engine |
| **Models** | Gemini 3 Pro (decisiones complejas), Gemini 2.5 Flash (alto volumen) |
| **Protocol** | A2A (Agent-to-Agent) para comunicación entre agentes |

---

## 8. Modelo de Negocio

### B2C (Núcleo Actual)

```
Lead Magnet → Email Sequence → Calificación → ASCEND o HYBRID
```

- **ASCEND:** Self-service, automático, para usuarios autónomos
- **HYBRID:** High-touch, videollamada de cierre, para quienes necesitan guía

### B2B (Ruta Paralela)

```
Prospección → Demo → Piloto 90 días → Founding Coach → Renovación
```

- Los coaches usan NGX COACH para gestionar sus clientes
- Los clientes de coaches usan GENESIS (app)
- El coach accede a los 13 agentes como copilots

### Filosofía de Pricing

- **Números cerrados:** $100, $300, $1,200 — no $99 o $1,197
- **Verdad Directa:** El precio refleja el posicionamiento premium
- **Temporadas:** Compromiso real, no suscripciones descartables
- **Filtro intencional:** Atraer clientes serios, no curiosos

---

## 9. Ventaja Competitiva (MOAT)

El moat de NGX **NO es la tecnología**. Competidores con más recursos eventualmente desarrollarán sistemas similares.

**El moat real:**

| Dimensión | Ventaja |
|-----------|---------|
| **Personajes** | 13 agentes con personalidades únicas, voces distintas, conexión emocional |
| **Storytelling** | Narrativas que trascienden funcionalidad, universo de marca coherente |
| **Contenido** | Videos cinematográficos, podcasts de agentes, cortometrajes |
| **Creatividad** | Visión artística del fundador, originalidad que no se replica con dinero |
| **Time-to-Market** | 3 años de desarrollo, curva de aprendizaje ya completada |

### Modelo Dual (B2C + B2B)

> *"Nuestra competencia es a la vez nuestros clientes. Los trainers que quieran competir, lo querrán desde el día que lo vean."*

---

## 10. Visión a Largo Plazo

**Meta 2035:** Ser el estándar global de optimización humana guiada por IA, donde 1 de cada 10 personas entre 30-60 años que se toman en serio su salud usen NGX.

**Roadmap:**

1. **Consolidar GENESIS + HIE (B2C)** — MVP estable con temporadas funcionando end-to-end
2. **Fortalecer datos y medición** — Integraciones con wearables, paneles avanzados de STELLA
3. **Escalar HIE** — Onboarding estructurado de coaches NGX
4. **Abrir ruta B2B** — NGX COACH como plataforma para terceros

---

## 11. Fundador

| Atributo | Detalle |
|----------|---------|
| **Nombre** | Aldo |
| **Rol** | Founder & CEO |
| **Background** | Entrenador personal con 10 certificaciones especializadas |
| **Ubicación** | Hermosillo, Sonora, México |
| **Diferenciador** | Autodidacta en IA, combina expertise fitness con visión tecnológica |
| **Tiempo de Desarrollo** | ~3 años dedicados |

---

## 12. Documentos de Referencia

| Documento | Propósito |
|-----------|-----------|
| **MASTER SOURCE OF TRUTH V9.0** | Fuente única de verdad conceptual |
| **NGX_Vision_Documento_Ejecutivo** | Visión estratégica fundacional |
| **NGX_Vision_Manifiesto_Narrativo** | Filosofía y narrativa de marca |
| **NGX_Brand_Voice_Guide** | Tono, voz, estilo de comunicación |
| **NGX_Agent_Voice_Bible** | Personalidades y voces de los 13 agentes |
| **NGX_Sales_Playbook** | Metodología de ventas B2C y B2B |
| **NGX_Technical_Implementation_Guide** | Arquitectura técnica detallada |

---

*NGX GENESIS — Performance & Longevity*
*"Rinde hoy. Vive mejor mañana."*

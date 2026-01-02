# Referencias Cruzadas entre Workspaces

> Guía para saber cuándo un workspace necesita outputs de otro.

---

## Mapa de Workspaces

```
┌─────────────────────────────────────────────────────────────┐
│                    NGX WORKSPACES                           │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ┌─────────────────┐       ┌─────────────────┐             │
│  │ PRODUCT STUDIO  │──────▶│ CONTENT STUDIO  │             │
│  │ (PRDs, docs)    │       │ (Videos, podcast)│             │
│  └────────┬────────┘       └────────┬────────┘             │
│           │                         │                       │
│           ▼                         ▼                       │
│  ┌─────────────────┐       ┌─────────────────┐             │
│  │ MARKETING       │◀─────▶│ B2B SALES       │             │
│  │ (Copy, emails)  │       │ (Propuestas)    │             │
│  └─────────────────┘       └─────────────────┘             │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## Cuándo Usar Cada Workspace

### NGX Marketing Command Center
**Usar para:**
- Email sequences (nurturing, ventas, onboarding)
- Copy para landing pages y ads
- Contenido para redes sociales
- Auditorías de funnels
- Scripts de venta HYBRID (B2C)

**NO usar para:**
- Propuestas B2B (usar B2B Sales)
- Scripts de video (usar Content Studio)
- PRDs técnicos (usar Product Studio)

---

### NGX B2B Sales Command Center
**Usar para:**
- Propuestas para coaches/gyms
- Emails de prospección B2B
- Scripts de llamadas B2B
- Case studies
- Contenido LinkedIn B2B
- Pipeline y seguimiento

**NO usar para:**
- Emails B2C (usar Marketing)
- Contenido de marca (usar Content Studio)
- Documentación técnica (usar Product Studio)

---

### NGX Content Studio
**Usar para:**
- Scripts de podcast (agentes debatiendo)
- Paquetes de pre-producción video
- Prompts para VEO 3.1, SORA 2, Kling
- Prompts para ElevenLabs (voces)
- Storyboards y shot lists
- Contenido educativo LOGOS

**NO usar para:**
- Copy de ventas (usar Marketing)
- Propuestas comerciales (usar B2B Sales)
- PRDs de features (usar Product Studio)

---

### NGX Product Studio
**Usar para:**
- PRDs de features (mobile, web)
- PRDs de agentes (ADK/A2A)
- Documentación técnica
- Context files para coding agents
- Handoff packages
- Especificaciones de producto

**NO usar para:**
- Copy de marketing (usar Marketing)
- Contenido de marca (usar Content Studio)
- Materiales de venta (usar Marketing o B2B Sales)

---

## Flujos Comunes

### Lanzar Feature Nueva
```
1. Product Studio → PRD de la feature
2. [Desarrollo]
3. Marketing → Copy para anuncio
4. Content Studio → Video de lanzamiento
```

### Campaña B2B
```
1. B2B Sales → Investigación de prospectos
2. B2B Sales → Propuesta personalizada
3. Marketing → Email de seguimiento (si se usa secuencia)
4. Content Studio → Video demo (si aplica)
```

### Episodio de Podcast
```
1. Content Studio → Script completo
2. Content Studio → Prompts de voz (ElevenLabs)
3. Content Studio → Prompts de video (VEO/SORA)
4. Marketing → Clips para redes (si aplica)
```

### Email Sequence Nuevo
```
1. Marketing → Estrategia y estructura
2. Marketing → Todos los emails
3. Content Studio → Imágenes/GIFs (si aplica)
```

---

## Cómo Solicitar Output de Otro Workspace

Si estás en un workspace y necesitas algo de otro:

```markdown
## Solicitud Cross-Workspace

**Desde:** [workspace actual]
**Para:** [workspace destino]
**Necesito:** [descripción específica]
**Para usarlo en:** [contexto]
**Deadline:** [fecha si aplica]
```

### Ejemplo:
```markdown
## Solicitud Cross-Workspace

**Desde:** B2B Sales
**Para:** Content Studio
**Necesito:** Video demo de 2 minutos mostrando NGX COACH
**Para usarlo en:** Propuesta para GymX
**Deadline:** Antes de llamada del viernes
```

---

## Archivos Compartidos (en todos los workspaces)

| Archivo | Propósito | Modificar? |
|---------|-----------|------------|
| `NGX_CONTEXT.md` | Contexto general NGX | Solo si cambia algo fundamental |
| `DECISIONS.md` | Decisiones tomadas | Sí, cuando hay decisiones nuevas |
| `DO_NOT.md` | Reglas y restricciones | Sí, cuando hay errores nuevos |
| `CHECKLIST.md` | Calidad pre-entrega | Raramente |
| `MEMORY.md` | Estado de sesión | Cada sesión |

---

**NOTA:** Si un cambio en NGX_CONTEXT.md aplica a todos los workspaces, debe actualizarse en TODOS.

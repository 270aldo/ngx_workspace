# PRD: Mobile Feature - [Nombre del Feature]

---

**PRD ID:** MOB-[YYYYMM]-[NNN]
**Autor:** [Nombre]
**Fecha:** [DD de Mes, YYYY]
**Status:** [ ] Draft [ ] En Revisión [ ] Aprobado [ ] En Desarrollo [ ] Completado
**Prioridad:** [ ] P0 (Crítico) [ ] P1 (Alto) [ ] P2 (Medio) [ ] P3 (Bajo)
**Plataforma:** [ ] iOS [ ] Android [ ] Ambas

---

## 1. Resumen Ejecutivo

### Problema
```
[Describir el problema del usuario que este feature resuelve]
```

### Solución
```
[Descripción breve del feature propuesto]
```

### Impacto Esperado

| Métrica | Actual | Objetivo | Timeline |
|---------|--------|----------|----------|
| [Retención D7] | [X%] | [Y%] | [N semanas] |
| [Engagement] | [X sesiones] | [Y sesiones] | [N semanas] |
| [Conversión] | [X%] | [Y%] | [N semanas] |

---

## 2. Contexto del Producto

### Agentes NGX Involucrados

| Agente | Rol en Feature | Integración |
|--------|----------------|-------------|
| NEXUS | [Orquestación] | [Cómo se integra] |
| BLAZE | [Entrenamiento] | [Cómo se integra] |
| [Otro] | [Rol] | [Integración] |

### User Stories

**Como** [tipo de usuario],
**Quiero** [acción/feature],
**Para** [beneficio/razón].

#### Story 1: [Título]
```
Como usuario de NGX GENESIS,
quiero [acción específica],
para [beneficio concreto].

Criterios de Aceptación:
- [ ] [Criterio 1]
- [ ] [Criterio 2]
- [ ] [Criterio 3]
```

#### Story 2: [Título]
```
Como usuario de NGX GENESIS,
quiero [acción específica],
para [beneficio concreto].

Criterios de Aceptación:
- [ ] [Criterio 1]
- [ ] [Criterio 2]
```

### Jobs to Be Done (JTBD)

| Situación | Motivación | Resultado Esperado |
|-----------|------------|-------------------|
| Cuando [situación] | Quiero [motivación] | Para [resultado] |

---

## 3. Diseño de la Solución

### Flujo de Usuario

```
┌─────────────┐
│   Entry     │
│   Point     │
└──────┬──────┘
       │
       ▼
┌─────────────┐
│   Screen 1  │
│   [Nombre]  │
└──────┬──────┘
       │
   ┌───┴───┐
   │       │
   ▼       ▼
┌─────┐ ┌─────┐
│ A   │ │ B   │
│     │ │     │
└──┬──┘ └──┬──┘
   │       │
   └───┬───┘
       │
       ▼
┌─────────────┐
│   Success   │
│   State     │
└─────────────┘
```

### Wireframes / Mockups

#### Screen 1: [Nombre de Pantalla]

```
┌────────────────────────┐
│ ← [Header]        ⚙️   │
├────────────────────────┤
│                        │
│   [Componente Hero]    │
│                        │
├────────────────────────┤
│   [Sección 1]          │
│   ┌────────────────┐   │
│   │  Card/Item     │   │
│   └────────────────┘   │
│   ┌────────────────┐   │
│   │  Card/Item     │   │
│   └────────────────┘   │
├────────────────────────┤
│   [CTA Principal]      │
│   ┌────────────────┐   │
│   │    BUTTON      │   │
│   └────────────────┘   │
├────────────────────────┤
│  🏠   📊   ➕   👤   ⚙️  │
└────────────────────────┘
```

**Elementos:**
- Header: [Descripción]
- Hero: [Descripción]
- Cards: [Descripción]
- CTA: [Descripción]

#### Screen 2: [Nombre de Pantalla]

```
[Wireframe de la siguiente pantalla]
```

### Estados de UI

| Estado | Descripción | Visual |
|--------|-------------|--------|
| Empty | Sin datos disponibles | [Descripción] |
| Loading | Cargando contenido | [Skeleton/Spinner] |
| Success | Operación exitosa | [Feedback visual] |
| Error | Error ocurrido | [Mensaje + Acción] |
| Partial | Datos parciales | [Descripción] |

---

## 4. Especificaciones Técnicas

### Stack Tecnológico

| Aspecto | Tecnología |
|---------|------------|
| Framework | React Native / Expo |
| State Management | [Context/Redux/Zustand] |
| Navigation | React Navigation |
| API Client | [Axios/Fetch/React Query] |
| UI Components | [Library] |

### Arquitectura

```
┌─────────────────────────────────┐
│           UI Layer              │
│  Screens / Components           │
└───────────────┬─────────────────┘
                │
┌───────────────┴─────────────────┐
│         State Layer             │
│  Context / Stores / Hooks       │
└───────────────┬─────────────────┘
                │
┌───────────────┴─────────────────┐
│         Service Layer           │
│  API Calls / Business Logic     │
└───────────────┬─────────────────┘
                │
┌───────────────┴─────────────────┐
│           API Layer             │
│  Backend / External Services    │
└─────────────────────────────────┘
```

### Componentes Nuevos

| Componente | Tipo | Props | Reutilizable |
|------------|------|-------|--------------|
| [Componente1] | [Screen/Component] | [Props principales] | [ ] Sí [ ] No |
| [Componente2] | [Screen/Component] | [Props principales] | [ ] Sí [ ] No |

### API Endpoints Requeridos

| Método | Endpoint | Body | Response | Notas |
|--------|----------|------|----------|-------|
| `GET` | `/api/[resource]` | - | `{ data: [...] }` | [Notas] |
| `POST` | `/api/[resource]` | `{ field: value }` | `{ id: "..." }` | [Notas] |
| `PUT` | `/api/[resource]/:id` | `{ field: value }` | `{ success: true }` | [Notas] |

### Modelos de Datos

```typescript
interface FeatureData {
  id: string;
  userId: string;
  // [Campos específicos del feature]
  createdAt: Date;
  updatedAt: Date;
}

interface FeatureState {
  data: FeatureData | null;
  loading: boolean;
  error: string | null;
}
```

### Integraciones con Agentes

| Agente | Tipo de Integración | Endpoint/Método |
|--------|---------------------|-----------------|
| NEXUS | Orquestación | `nexus.coordinate()` |
| BLAZE | Recomendaciones | `blaze.getWorkout()` |
| [Agente] | [Tipo] | [Método] |

---

## 5. UX/UI Specifications

### Design System

| Elemento | Especificación |
|----------|----------------|
| Colores | Primary: #6D00FF, Background: #0A0A0A |
| Tipografía | Space Grotesk (headers), Inter (body) |
| Spacing | 4px grid system |
| Border Radius | 8px (small), 16px (medium), 24px (large) |
| Shadows | `0 4px 16px rgba(0,0,0,0.3)` |

### Animaciones

| Animación | Duración | Easing | Trigger |
|-----------|----------|--------|---------|
| [Transición 1] | [300ms] | [ease-out] | [Evento] |
| [Transición 2] | [200ms] | [spring] | [Evento] |

### Gestos

| Gesto | Acción | Feedback |
|-------|--------|----------|
| Swipe left | [Acción] | [Visual feedback] |
| Long press | [Acción] | [Haptic + visual] |
| Pull to refresh | [Acción] | [Animación] |

### Accesibilidad

- [ ] VoiceOver/TalkBack labels
- [ ] Contraste mínimo 4.5:1
- [ ] Touch targets mínimo 44x44pt
- [ ] Reducir movimiento respetado
- [ ] Dynamic type soportado (iOS)

---

## 6. Offline & Performance

### Estrategia Offline

| Funcionalidad | Offline Support | Sync Strategy |
|---------------|-----------------|---------------|
| [Feature 1] | [ ] Full [ ] Partial [ ] None | [Strategy] |
| [Feature 2] | [ ] Full [ ] Partial [ ] None | [Strategy] |

### Caching

| Dato | Cache Duration | Invalidación |
|------|----------------|--------------|
| [Dato 1] | [X minutos/horas] | [Trigger] |
| [Dato 2] | [X minutos/horas] | [Trigger] |

### Performance Targets

| Métrica | Target | Crítico |
|---------|--------|---------|
| Time to Interactive | < 2s | < 3s |
| First Contentful Paint | < 1s | < 1.5s |
| Memory usage | < 100MB | < 150MB |
| Battery impact | Bajo | Medio |

---

## 7. Analytics & Tracking

### Eventos a Trackear

| Evento | Trigger | Propiedades |
|--------|---------|-------------|
| `feature_viewed` | Screen mount | `{ screen_name, user_id }` |
| `action_completed` | Acción exitosa | `{ action_type, duration }` |
| `error_occurred` | Error | `{ error_type, screen }` |

### Funnels

```
Vista Feature → Interacción → Completado
    100%      →     60%     →    40%
```

### Experimentos (A/B Tests)

| Experimento | Variantes | Métrica Primaria | Hipótesis |
|-------------|-----------|------------------|-----------|
| [Exp 1] | Control, V1, V2 | [Métrica] | [Hipótesis] |

---

## 8. Casos Edge y Errores

### Casos Edge

| Caso | Comportamiento Esperado |
|------|-------------------------|
| Sin conexión | [Comportamiento] |
| Session expirada | [Comportamiento] |
| Datos incompletos | [Comportamiento] |
| Primera vez (onboarding) | [Comportamiento] |

### Manejo de Errores

| Error | Mensaje al Usuario | Acción |
|-------|-------------------|--------|
| Network error | "Sin conexión. Reintenta." | Botón retry |
| Server error | "Algo salió mal. Intenta más tarde." | Link soporte |
| Validation error | "[Error específico]" | Highlight campo |

---

## 9. Testing

### Unit Tests

| Componente | Casos a Testear |
|------------|-----------------|
| [Componente 1] | [Lista de casos] |
| [Componente 2] | [Lista de casos] |

### Integration Tests

| Flujo | Casos |
|-------|-------|
| [Flujo 1] | Happy path, Error path |
| [Flujo 2] | Happy path, Edge cases |

### E2E Tests (Detox/Maestro)

| Test | Steps | Expected Result |
|------|-------|-----------------|
| [Test 1] | [Steps] | [Result] |
| [Test 2] | [Steps] | [Result] |

### Device Testing Matrix

| Device | OS Version | Priority |
|--------|------------|----------|
| iPhone 14 Pro | iOS 17 | P0 |
| iPhone SE | iOS 16 | P1 |
| Pixel 7 | Android 14 | P0 |
| Samsung S21 | Android 13 | P1 |

---

## 10. Rollout Plan

### Feature Flags

| Flag | Descripción | Default |
|------|-------------|---------|
| `feature_[name]_enabled` | Activa el feature | `false` |
| `feature_[name]_v2` | Variante V2 | `false` |

### Rollout Phases

| Fase | % Usuarios | Duración | Criterio Avance |
|------|------------|----------|-----------------|
| Internal | 0% (team only) | 1 semana | 0 bugs críticos |
| Beta | 5% | 1 semana | Feedback positivo |
| Soft Launch | 25% | 1 semana | Métricas estables |
| Full Launch | 100% | - | - |

### Rollback Plan

```
1. Desactivar feature flag
2. Notificar a usuarios afectados
3. Revertir a versión anterior si necesario
4. Post-mortem si hubo issues
```

---

## 11. Timeline

### Milestones

| Milestone | Fecha | Responsable |
|-----------|-------|-------------|
| PRD Aprobado | [Fecha] | Product |
| Design Complete | [Fecha] | Design |
| Development Complete | [Fecha] | Dev |
| QA Complete | [Fecha] | QA |
| Beta Release | [Fecha] | DevOps |
| Full Release | [Fecha] | Product |

### Sprint Breakdown

| Sprint | Deliverables |
|--------|--------------|
| Sprint 1 | [Lista de entregables] |
| Sprint 2 | [Lista de entregables] |
| Sprint 3 | [Lista de entregables] |

---

## 12. Recursos y Dependencias

### Equipo

| Rol | Persona | Dedicación |
|-----|---------|------------|
| Product | [Nombre] | [%] |
| Design | [Nombre] | [%] |
| iOS Dev | [Nombre] | [%] |
| Android Dev | [Nombre] | [%] |
| QA | [Nombre] | [%] |

### Dependencias

| Dependencia | Owner | Status | Blocker? |
|-------------|-------|--------|----------|
| [API endpoint X] | Backend | [Status] | [ ] |
| [Design assets] | Design | [Status] | [ ] |
| [Tercero/SDK] | External | [Status] | [ ] |

---

## 13. Apéndices

### A. Competitive Analysis

| Competidor | Feature Similar | Diferenciador NGX |
|------------|-----------------|-------------------|
| [Comp 1] | [Feature] | [Diferenciador] |
| [Comp 2] | [Feature] | [Diferenciador] |

### B. User Research

```
[Resumen de insights de user research relevante]
```

### C. Historial de Cambios

| Fecha | Versión | Cambio | Autor |
|-------|---------|--------|-------|
| [Fecha] | 1.0 | Creación inicial | [Autor] |

---

*Template PRD Mobile Feature NGX v1.0*

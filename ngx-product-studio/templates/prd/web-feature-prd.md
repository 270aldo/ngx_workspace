# PRD: Web Feature - [Nombre del Feature]

---

**PRD ID:** WEB-[YYYYMM]-[NNN]
**Autor:** [Nombre]
**Fecha:** [DD de Mes, YYYY]
**Status:** [ ] Draft [ ] En Revisión [ ] Aprobado [ ] En Desarrollo [ ] Completado
**Prioridad:** [ ] P0 (Crítico) [ ] P1 (Alto) [ ] P2 (Medio) [ ] P3 (Bajo)
**Aplicación:** [ ] Coach Dashboard [ ] Admin Portal [ ] Landing/Marketing [ ] Web App

---

## 1. Resumen Ejecutivo

### Problema
```
[Describir el problema que este feature resuelve para usuarios web]
```

### Solución
```
[Descripción breve del feature propuesto]
```

### Target Users

| Segmento | Descripción | % de Base |
|----------|-------------|-----------|
| Coaches | [Descripción del uso] | [X%] |
| Admins | [Descripción del uso] | [X%] |
| End Users | [Descripción del uso] | [X%] |

### Métricas de Éxito

| Métrica | Actual | Objetivo | Cómo Medir |
|---------|--------|----------|------------|
| [Conversión] | [X%] | [Y%] | [Analytics] |
| [Time on page] | [X min] | [Y min] | [Analytics] |
| [Task completion] | [X%] | [Y%] | [Analytics] |

---

## 2. Contexto del Producto

### Ecosistema NGX Web

```
┌─────────────────────────────────────────────────────────┐
│                    NGX Web Platform                      │
├─────────────────┬─────────────────┬─────────────────────┤
│  Coach Dashboard │   Admin Portal  │   Marketing Site    │
│  - Client mgmt   │   - Analytics   │   - Landing pages   │
│  - COACH AI      │   - User mgmt   │   - Pricing         │
│  - Reports       │   - Settings    │   - Blog            │
└─────────────────┴─────────────────┴─────────────────────┘
                            │
                   [Este feature aquí]
```

### User Stories

**Como** [tipo de usuario web],
**Quiero** [acción/feature],
**Para** [beneficio/razón].

#### Story 1: [Título]
```
Como coach usando el dashboard,
quiero [acción específica],
para [beneficio concreto].

Criterios de Aceptación:
- [ ] [Criterio 1]
- [ ] [Criterio 2]
- [ ] [Criterio 3]
```

#### Story 2: [Título]
```
Como administrador,
quiero [acción específica],
para [beneficio concreto].

Criterios de Aceptación:
- [ ] [Criterio 1]
- [ ] [Criterio 2]
```

### Relación con Agentes NGX

| Agente | Rol en Dashboard | API/Endpoint |
|--------|------------------|--------------|
| COACH AI | Chat asistente | `/api/coach-ai` |
| NEXUS | Orquestación | `/api/nexus` |
| [Agente] | [Rol] | [Endpoint] |

---

## 3. Diseño de la Solución

### Information Architecture

```
Coach Dashboard
├── Home (Overview)
├── Clients
│   ├── Client List
│   ├── Client Detail
│   │   ├── Progress
│   │   ├── Plans
│   │   └── Messages
│   └── Add Client
├── [NUEVO FEATURE] ← Este feature
│   ├── [Sub-section 1]
│   ├── [Sub-section 2]
│   └── [Sub-section 3]
├── Analytics
├── Settings
└── Help
```

### Page Layout

#### Main View: [Nombre de Página]

```
┌────────────────────────────────────────────────────────────────────┐
│  SIDEBAR  │                      HEADER                            │
│           │  [Breadcrumb]                           [User] [Notif] │
│  🏠 Home  ├────────────────────────────────────────────────────────┤
│  👥 Clients│                                                        │
│  📊 Analytics│              MAIN CONTENT AREA                       │
│  ⚙️ Settings│                                                        │
│           │  ┌──────────────────────────────────────────────────┐  │
│  ──────── │  │                                                  │  │
│           │  │              [Primary Content]                   │  │
│  📦 [NEW] │  │                                                  │  │
│    └ Sub1 │  └──────────────────────────────────────────────────┘  │
│    └ Sub2 │                                                        │
│    └ Sub3 │  ┌────────────────┐  ┌────────────────┐                │
│           │  │   Card/Widget  │  │   Card/Widget  │                │
│           │  └────────────────┘  └────────────────┘                │
│           │                                                        │
└───────────┴────────────────────────────────────────────────────────┘
```

#### Component Breakdown

| Área | Componentes | Comportamiento |
|------|-------------|----------------|
| Header | Breadcrumb, Search, User Menu | Sticky top |
| Sidebar | Navigation, Badges | Collapsible en mobile |
| Main | Content cards, Tables, Forms | Scrollable |
| Footer | Pagination, Actions | Sticky bottom (si aplica) |

### Wireframes por Sección

#### Section 1: [Nombre]

```
┌────────────────────────────────────────────────┐
│  ┌──────────────────────────────────────────┐  │
│  │           Section Header                 │  │
│  │  Title                    [Action Btn]   │  │
│  └──────────────────────────────────────────┘  │
│                                                │
│  ┌────────┐ ┌────────┐ ┌────────┐ ┌────────┐  │
│  │ Stat 1 │ │ Stat 2 │ │ Stat 3 │ │ Stat 4 │  │
│  │  123   │ │  456   │ │   78%  │ │  $1.2K │  │
│  └────────┘ └────────┘ └────────┘ └────────┘  │
│                                                │
│  ┌──────────────────────────────────────────┐  │
│  │              Data Table                  │  │
│  │  Column 1 │ Column 2 │ Column 3 │ Actions│  │
│  │  ─────────┼──────────┼──────────┼────────│  │
│  │  Row 1    │ Data     │ Data     │  ...   │  │
│  │  Row 2    │ Data     │ Data     │  ...   │  │
│  │  Row 3    │ Data     │ Data     │  ...   │  │
│  └──────────────────────────────────────────┘  │
│                                                │
│              [Pagination: 1 2 3 ... 10]        │
└────────────────────────────────────────────────┘
```

### Estados de UI

| Estado | Descripción | Componentes |
|--------|-------------|-------------|
| Empty State | Sin datos | Ilustración + CTA |
| Loading | Cargando | Skeleton screens |
| Error | Error de carga | Alert + Retry |
| Success | Acción exitosa | Toast notification |
| Partial Load | Datos parciales | Skeleton parcial |

### Responsive Breakpoints

| Breakpoint | Comportamiento |
|------------|----------------|
| Desktop (≥1280px) | Sidebar expandido, grid 3 columnas |
| Laptop (1024-1279px) | Sidebar condensado, grid 2 columnas |
| Tablet (768-1023px) | Sidebar overlay, grid 2 columnas |
| Mobile (<768px) | Bottom nav, stack vertical |

---

## 4. Especificaciones Técnicas

### Stack Tecnológico

| Capa | Tecnología |
|------|------------|
| Framework | Next.js 14+ (App Router) |
| Styling | Tailwind CSS |
| UI Components | shadcn/ui |
| State | React Query + Zustand |
| Forms | React Hook Form + Zod |
| Charts | Chart.js / Recharts |
| Auth | [Supabase Auth / NextAuth] |

### Arquitectura de Componentes

```
src/
├── app/
│   └── (dashboard)/
│       └── [feature]/
│           ├── page.tsx          # Main page
│           ├── layout.tsx        # Feature layout
│           ├── loading.tsx       # Loading state
│           ├── error.tsx         # Error boundary
│           └── [subpage]/
│               └── page.tsx
├── components/
│   └── [feature]/
│       ├── FeatureCard.tsx
│       ├── FeatureTable.tsx
│       ├── FeatureForm.tsx
│       └── index.ts
├── hooks/
│   └── use[Feature].ts
├── lib/
│   └── [feature]/
│       ├── api.ts               # API calls
│       ├── types.ts             # TypeScript types
│       └── utils.ts             # Helper functions
└── stores/
    └── [feature]Store.ts
```

### API Endpoints

| Método | Endpoint | Request | Response | Auth |
|--------|----------|---------|----------|------|
| `GET` | `/api/[feature]` | `?page=1&limit=10` | `{ data, pagination }` | Bearer |
| `GET` | `/api/[feature]/:id` | - | `{ item }` | Bearer |
| `POST` | `/api/[feature]` | `{ ...fields }` | `{ id, ...item }` | Bearer |
| `PUT` | `/api/[feature]/:id` | `{ ...fields }` | `{ ...updated }` | Bearer |
| `DELETE` | `/api/[feature]/:id` | - | `{ success }` | Bearer |

### TypeScript Interfaces

```typescript
// types.ts
export interface Feature {
  id: string;
  name: string;
  // [campos específicos]
  createdAt: Date;
  updatedAt: Date;
}

export interface FeatureListParams {
  page?: number;
  limit?: number;
  search?: string;
  filter?: string;
  sortBy?: string;
  sortOrder?: 'asc' | 'desc';
}

export interface FeatureListResponse {
  data: Feature[];
  pagination: {
    total: number;
    page: number;
    limit: number;
    totalPages: number;
  };
}

export interface FeatureFormData {
  name: string;
  // [campos del form]
}
```

### Validación (Zod Schema)

```typescript
import { z } from 'zod';

export const featureFormSchema = z.object({
  name: z.string().min(2, 'Nombre debe tener al menos 2 caracteres'),
  email: z.string().email('Email inválido'),
  // [más campos]
});

export type FeatureFormValues = z.infer<typeof featureFormSchema>;
```

### Server Actions (Next.js)

```typescript
// actions.ts
'use server'

export async function createFeature(data: FeatureFormData) {
  // Validación
  // Llamada a DB/API
  // Revalidate cache
  // Return result
}

export async function updateFeature(id: string, data: FeatureFormData) {
  // ...
}

export async function deleteFeature(id: string) {
  // ...
}
```

---

## 5. UX/UI Specifications

### Design Tokens (NGX Brand)

```css
/* Colors */
--primary: #6D00FF;
--primary-hover: #8B33FF;
--background: #0A0A0A;
--card: #141414;
--border: #2A2A2A;
--text: #FFFFFF;
--text-muted: #888888;
--success: #00FF88;
--warning: #FFB800;
--danger: #FF4444;

/* Typography */
--font-heading: 'Space Grotesk', sans-serif;
--font-body: 'Inter', sans-serif;

/* Spacing */
--space-unit: 4px;
/* Use: space-[1-12] = 4px to 48px */

/* Radius */
--radius-sm: 8px;
--radius-md: 12px;
--radius-lg: 16px;
--radius-xl: 24px;

/* Shadows */
--shadow-card: 0 4px 16px rgba(0, 0, 0, 0.3);
--shadow-hover: 0 8px 32px rgba(109, 0, 255, 0.2);
```

### Componentes shadcn/ui a Usar

| Componente | Uso |
|------------|-----|
| Button | CTAs, Actions |
| Card | Content containers |
| Table | Data display |
| Form, Input, Select | Form controls |
| Dialog/Sheet | Modals |
| Dropdown Menu | Actions menu |
| Tabs | Section navigation |
| Toast | Notifications |
| Skeleton | Loading states |
| Badge | Status indicators |

### Micro-interacciones

| Interacción | Animación | Duración |
|-------------|-----------|----------|
| Button hover | Scale + glow | 150ms |
| Card hover | Lift + border color | 200ms |
| Modal open | Fade + scale | 200ms |
| Toast | Slide in | 300ms |
| Page transition | Fade | 150ms |

### Accessibility Checklist

- [ ] Keyboard navigation funcional
- [ ] Focus visible states
- [ ] ARIA labels donde necesario
- [ ] Color contrast ≥ 4.5:1
- [ ] Screen reader compatible
- [ ] Skip links si necesario
- [ ] Form error messages asociados
- [ ] Loading states anunciados

---

## 6. SEO & Performance (Si aplica)

### Meta Tags

```html
<title>[Page Title] | NGX GENESIS</title>
<meta name="description" content="[Description]" />
<meta property="og:title" content="[OG Title]" />
<meta property="og:description" content="[OG Description]" />
<meta property="og:image" content="[OG Image URL]" />
```

### Core Web Vitals Targets

| Métrica | Target | Max Aceptable |
|---------|--------|---------------|
| LCP | < 2.5s | < 4s |
| FID | < 100ms | < 300ms |
| CLS | < 0.1 | < 0.25 |

### Optimizations

- [ ] Image optimization (next/image)
- [ ] Code splitting por ruta
- [ ] Lazy loading de componentes pesados
- [ ] Prefetch de rutas probables
- [ ] Cache headers apropiados
- [ ] Bundle size monitoring

---

## 7. Security

### Autenticación y Autorización

| Acción | Requiere Auth | Roles Permitidos |
|--------|---------------|------------------|
| Ver lista | Sí | Coach, Admin |
| Crear | Sí | Coach, Admin |
| Editar | Sí | Owner, Admin |
| Eliminar | Sí | Admin |

### Input Validation

```typescript
// Server-side validation
const validateInput = (data: unknown) => {
  const parsed = featureFormSchema.safeParse(data);
  if (!parsed.success) {
    throw new ValidationError(parsed.error);
  }
  return parsed.data;
};
```

### CSRF Protection

- [ ] Tokens CSRF en forms
- [ ] SameSite cookies
- [ ] Origin validation

### Rate Limiting

| Endpoint | Límite | Ventana |
|----------|--------|---------|
| API general | 100 req | 1 min |
| Búsqueda | 30 req | 1 min |
| Creación | 10 req | 1 min |

---

## 8. Testing

### Unit Tests

```typescript
// Example test structure
describe('FeatureComponent', () => {
  it('renders correctly', () => {});
  it('handles empty state', () => {});
  it('handles loading state', () => {});
  it('handles error state', () => {});
  it('calls API on action', () => {});
});
```

### Integration Tests

| Flujo | Casos |
|-------|-------|
| Create flow | Happy path, Validation errors, API errors |
| Edit flow | Happy path, Concurrent edits, Permission denied |
| Delete flow | Happy path, Confirm dialog, Cascade effects |

### E2E Tests (Playwright)

| Test | Steps |
|------|-------|
| Full CRUD flow | Navigate → Create → Edit → Delete |
| Search & Filter | Search → Apply filters → Clear |
| Pagination | Navigate pages → Change limit |

### Test Coverage Targets

| Tipo | Cobertura |
|------|-----------|
| Unit | > 80% |
| Integration | > 60% |
| E2E | Critical paths |

---

## 9. Analytics & Monitoring

### Eventos a Trackear

| Evento | Propiedades | Trigger |
|--------|-------------|---------|
| `feature_page_view` | `{ page, user_role }` | Page load |
| `feature_created` | `{ feature_type, user_id }` | Create success |
| `feature_search` | `{ query, results_count }` | Search executed |
| `feature_error` | `{ error_type, page }` | Error occurred |

### Error Monitoring (Sentry)

```typescript
// Error boundary integration
Sentry.captureException(error, {
  tags: { feature: '[feature_name]' },
  extra: { userId, action }
});
```

### Performance Monitoring

- [ ] Real User Monitoring (RUM)
- [ ] API latency tracking
- [ ] Error rate dashboards
- [ ] Alertas de degradación

---

## 10. Deployment

### Feature Flags

| Flag | Descripción | Default |
|------|-------------|---------|
| `web_feature_[name]` | Activa el feature | `false` |
| `web_feature_[name]_v2` | Variante mejorada | `false` |

### Environments

| Environment | URL | Propósito |
|-------------|-----|-----------|
| Development | localhost:3000 | Local dev |
| Preview | feature-xxx.vercel.app | PR previews |
| Staging | staging.ngxgenesis.com | Pre-prod testing |
| Production | app.ngxgenesis.com | Live |

### Rollout Plan

| Fase | % Usuarios | Validación |
|------|------------|------------|
| Internal | Team only | Manual QA |
| Beta | 10% | Error rates < 0.1% |
| Canary | 25% | Métricas estables |
| GA | 100% | - |

### Rollback

```
1. Revertir deploy en Vercel
2. Desactivar feature flag
3. Notificar equipo
4. Investigar root cause
5. Post-mortem
```

---

## 11. Timeline

### Milestones

| Milestone | Fecha | Owner |
|-----------|-------|-------|
| PRD Final | [Fecha] | Product |
| Design Handoff | [Fecha] | Design |
| API Ready | [Fecha] | Backend |
| Frontend Complete | [Fecha] | Frontend |
| QA Complete | [Fecha] | QA |
| Launch | [Fecha] | Product |

### Sprint Planning

| Sprint | Focus | Deliverables |
|--------|-------|--------------|
| Sprint 1 | Foundation | Setup, routing, basic UI |
| Sprint 2 | Core Features | CRUD, forms, validation |
| Sprint 3 | Polish | Edge cases, animations, tests |
| Sprint 4 | Launch Prep | QA fixes, monitoring, docs |

---

## 12. Handoff Checklist

### Design → Development

- [ ] Figma designs finalizados
- [ ] Design tokens exportados
- [ ] Assets preparados (iconos, imágenes)
- [ ] Prototipos interactivos (si aplica)
- [ ] Edge cases documentados

### Development → QA

- [ ] Feature deployada en staging
- [ ] Test cases documentados
- [ ] Credenciales de prueba
- [ ] Known issues listados
- [ ] Runbook de testing

### QA → Launch

- [ ] Todos los tests pasando
- [ ] Bugs críticos resueltos
- [ ] Performance validada
- [ ] Cross-browser testing completo
- [ ] Documentación actualizada

---

## 13. Apéndices

### A. Glossario

| Término | Definición |
|---------|------------|
| [Término] | [Definición] |

### B. Decisiones de Diseño

| Decisión | Alternativas Consideradas | Razón |
|----------|---------------------------|-------|
| [Decisión] | [Alternativas] | [Razón] |

### C. Referencias

- [Link a Figma]
- [Link a API docs]
- [Link a PRDs relacionados]

### D. Historial de Cambios

| Fecha | Versión | Cambio | Autor |
|-------|---------|--------|-------|
| [Fecha] | 1.0 | Creación inicial | [Autor] |

---

*Template PRD Web Feature NGX v1.0*

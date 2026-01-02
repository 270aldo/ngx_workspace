# NGX GENESIS — Contexto para Claude Code

> Resumen ejecutivo del proyecto para que Claude Code entienda el contexto.

---

## Qué es NGX GENESIS

Plataforma de **Performance & Longevity** con 13 agentes IA especializados.

**Tagline:** "Rinde hoy. Vive mejor mañana."

**Target:** Profesionales 30-60 años

**Diferenciador:** Sistema de agentes que se comunican entre sí y adaptan planes en tiempo real.

---

## Los 13 Agentes

| Agente | Especialidad |
|--------|--------------|
| NEXUS | Orquestador central |
| BLAZE | Entrenamiento |
| ATLAS | Movilidad y postura |
| TEMPO | Recuperación |
| WAVE | Cardio y resistencia |
| SAGE | Protocolos longevidad |
| METABOL | Metabolismo |
| MACRO | Nutrición |
| NOVA | Suplementación |
| SPARK | Energía y estrés |
| STELLA | Hábitos |
| LUNA | Sueño |
| LOGOS | Educación |

---

## Productos

### B2C

| Producto | Precio | Descripción |
|----------|--------|-------------|
| ASCEND | $100/mes | App con 13 agentes, mínimo 3 meses |
| HYBRID | $1,200/temporada | 12 semanas con coach humano + IA |

### B2B

| Producto | Precio | Descripción |
|----------|--------|-------------|
| Founding Coaches | $0 → $199/mes | Piloto 3 meses gratis |
| NGX COACH Regular | $299/mes | Dashboard para coaches |

---

## Voz de Marca: "Verdad Directa"

**Fórmula:** CONFRONTA → FUNDAMENTA → RESUELVE

**Principios:**
1. Honestidad Primero
2. Acción Inmediata
3. Explicación Eficiente
4. Confianza Tranquila (sin hype)
5. Responsabilidad Visible (fundador presente)
6. Híbrido por Diseño (IA + Humano)

**Tratamiento:**
- 30-45 años: TÚ (directo, coloquial)
- 45-60 años: USTED (respetuoso, profesional)

---

## Tech Stack

- **Backend:** Supabase + 31 FastAPI microservices
- **Frontend:** React Native (mobile), Next.js (web)
- **Agentes:** Google ADK/A2A en Vertex AI
- **Automatización:** n8n
- **Video:** VEO 3.1, SORA 2 Pro
- **Voz:** ElevenLabs
- **IA:** Claude (interno), Gemini (usuarios)

---

## Estructura de Workspaces

```
ngx-workspaces/
├── ngx-marketing/          # B2C marketing, emails, ads, funnels
├── ngx-b2b-sales/          # Ventas B2B, coaches, proposals
├── ngx-content-studio/     # Contenido multimedia, podcasts, video
├── ngx-product-studio/     # PRDs, documentación técnica
├── ngx-operations/         # SOPs, métricas, workflows
└── ngx-finance/            # P&L, proyecciones, facturación
```

---

## Colores de Marca

```css
--primary: #6D00FF;        /* Violeta NGX */
--background: #0D0D0D;     /* Negro profundo */
--card: #1A1A1A;           /* Gris oscuro */
--text: #FFFFFF;           /* Blanco */
--text-muted: #A0A0A0;     /* Gris texto */
--success: #00FF88;        /* Verde */
--warning: #FFB800;        /* Amarillo */
--danger: #FF4444;         /* Rojo */
```

---

## Founder

**Aldo** — Ex entrenador personal (10 certificaciones), 3 años aprendiendo programación y AI. Bootstrapped, financiado por su pareja. Basado en Hermosillo, Sonora, México.

---

## Fase Actual

Pre-lanzamiento. Validando B2C y B2B simultáneamente.

---

*Contexto v1.0 — Diciembre 2025*

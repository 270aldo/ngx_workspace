# NGX Operations Hub — Tareas Frecuentes

> Flujos optimizados para tareas operativas recurrentes.

---

## 1. Daily Checklist

**Frecuencia:** Cada mañana

**Input requerido:**
- Tareas pendientes de ayer
- Calendario del día
- Deadlines de la semana

**Output esperado:**
- Checklist con 5 MITs (Most Important Tasks)
- Bloques de tiempo asignados
- Hora de corte del día

**Checklist:**
- [ ] Máximo 5 tareas prioritarias
- [ ] Estimación de tiempo por tarea
- [ ] Bloque para trabajo profundo incluido
- [ ] Realista (no más de 6-8 horas de trabajo)

---

## 2. Weekly Review

**Frecuencia:** Viernes o domingo

**Input requerido:**
- Métricas de la semana (leads, ventas, contenido)
- Lista de tareas completadas vs planeadas
- Obstáculos encontrados

**Output esperado:**
- Reporte de 1 página
- 3 wins, 3 problemas, 3 prioridades siguiente semana
- Comparación vs semana anterior

**Checklist:**
- [ ] Datos verificados (no inventados)
- [ ] Comparación con período anterior
- [ ] Acciones concretas para próxima semana
- [ ] Máximo 1 página

---

## 3. Monthly Report

**Frecuencia:** Último día del mes

**Input requerido:**
- Métricas completas del mes
- Weekly reviews del mes
- Objetivos del mes vs resultados

**Output esperado:**
- Documento ejecutivo 2-3 páginas
- Dashboard de métricas
- Plan de acción para siguiente mes

**Checklist:**
- [ ] Todas las métricas incluidas
- [ ] Comparación MoM (month over month)
- [ ] Análisis de causas (no solo números)
- [ ] Objetivos SMART para próximo mes

---

## 4. Create SOP

**Frecuencia:** Cuando se identifica proceso repetitivo

**Input requerido:**
- Nombre del proceso
- Descripción de lo que hace
- Pasos actuales (aunque sean informales)
- Herramientas involucradas

**Output esperado:**
- SOP en formato markdown
- Guardado en `/sops/[nombre]-sop.md`
- Checklist de verificación incluido

**Checklist:**
- [ ] Trigger claro (qué inicia el proceso)
- [ ] Pasos numerados y específicos
- [ ] Cada paso es una acción (verbo)
- [ ] Incluye qué hacer si falla
- [ ] Output esperado definido

---

## 5. Metrics Dashboard

**Frecuencia:** Semanal o bajo demanda

**Input requerido:**
- KPIs a mostrar
- Datos del período
- Período de comparación

**Output esperado:**
- Dashboard HTML interactivo
- Guardado en `/dashboards/`
- Estilo NGX dark theme

**Checklist:**
- [ ] Todos los KPIs solicitados
- [ ] Comparación con período anterior
- [ ] Indicadores visuales (↑↓→)
- [ ] Colores correctos (verde/amarillo/rojo)
- [ ] Responsive o al menos legible

---

## 6. Document Workflow

**Frecuencia:** Cuando se crea o modifica workflow n8n

**Input requerido:**
- Nombre del workflow
- Propósito
- Trigger y nodos principales
- Credenciales/APIs usadas

**Output esperado:**
- Documentación markdown completa
- Diagrama mermaid del flujo
- Troubleshooting guide

**Checklist:**
- [ ] Propósito claro en primera línea
- [ ] Diagrama de flujo incluido
- [ ] Dependencias documentadas
- [ ] Sección de troubleshooting
- [ ] Instrucciones para modificar

---

## 7. Priority Planning

**Frecuencia:** Inicio de semana o cuando hay sobrecarga

**Input requerido:**
- Lista de todas las tareas pendientes
- Deadlines conocidos
- Objetivos principales del período

**Output esperado:**
- Matriz Eisenhower completada
- Lista priorizada de ejecución
- Tareas a delegar/eliminar identificadas

**Checklist:**
- [ ] Todas las tareas clasificadas
- [ ] Orden de ejecución claro
- [ ] Tareas eliminables identificadas
- [ ] Tiempo estimado total realista

---

## 8. Process Audit

**Frecuencia:** Mensual o cuando hay problemas

**Input requerido:**
- SOP o proceso a auditar
- Problemas reportados
- Feedback de quien lo ejecuta

**Output esperado:**
- Score de calidad (1-10)
- Lista de mejoras
- SOP actualizado si necesario

**Checklist:**
- [ ] Cada paso revisado
- [ ] Oportunidades de automatización evaluadas
- [ ] Mejoras priorizadas por impacto
- [ ] SOP actualizado si hubo cambios

---

## 9. Incident Documentation

**Frecuencia:** Cuando ocurre un problema significativo

**Input requerido:**
- Qué pasó y cuándo
- Impacto
- Cómo se resolvió

**Output esperado:**
- Incident report completo
- Análisis de causa raíz
- Acciones preventivas

**Checklist:**
- [ ] Timeline preciso
- [ ] 5 Whys completado
- [ ] Acciones correctivas definidas
- [ ] Acciones preventivas definidas
- [ ] SOP actualizado si aplica

---

## 10. Automation Analysis

**Frecuencia:** Cuando se identifica proceso manual repetitivo

**Input requerido:**
- Descripción del proceso
- Frecuencia
- Tiempo que toma
- Pasos manuales

**Output esperado:**
- Análisis de viabilidad
- Herramientas sugeridas
- ROI estimado
- Recomendación go/no-go

**Checklist:**
- [ ] ROI calculado (tiempo ahorrado vs esfuerzo)
- [ ] Herramienta específica recomendada
- [ ] Complejidad evaluada
- [ ] Recomendación clara con justificación

---

*Cada tarea sigue el patrón: Input → Proceso → Output → Verificación*

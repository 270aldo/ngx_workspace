# NGX Operations Hub — Prompts Probados

> Prompts optimizados para tareas operativas frecuentes.

---

## 1. Daily Checklist

```
Genera mi checklist diario para [DÍA].

Contexto:
- Tareas pendientes de ayer: [LISTA]
- Reuniones programadas: [LISTA]
- Deadlines esta semana: [LISTA]

Quiero un checklist con:
1. Máximo 5 tareas prioritarias (MIT - Most Important Tasks)
2. Tareas de mantenimiento (emails, admin)
3. Un bloque de tiempo para trabajo profundo
4. Hora de corte sugerida

Formato: Checklist accionable con estimación de tiempo por tarea.
```

---

## 2. Weekly Review

```
Genera mi reporte semanal de operaciones.

Datos de la semana:
- Leads generados: [N]
- Conversiones: [N]
- Contenido publicado: [N posts]
- Tareas completadas: [N de M]
- Horas trabajadas: [N]

Incluye:
1. Wins de la semana (máximo 3)
2. Obstáculos encontrados
3. Métricas vs semana anterior (% cambio)
4. Top 3 prioridades para próxima semana
5. Una cosa a mejorar

Formato: Ejecutivo, 1 página máximo.
```

---

## 3. Monthly Report

```
Genera mi reporte mensual de [MES].

Métricas del mes:
- MRR: $[X]
- Nuevos clientes: [N]
- Churn: [N]
- Leads totales: [N]
- Tasa de conversión: [X%]
- Contenido: [N] posts, [N] videos
- NPS/Feedback: [X]

Incluye:
1. Resumen ejecutivo (3 líneas)
2. Comparación vs mes anterior
3. Comparación vs objetivo
4. Top 3 logros
5. Top 3 problemas
6. Acciones correctivas propuestas
7. Objetivos para próximo mes

Formato: Documento estructurado con gráficos si aplica.
```

---

## 4. SOP Creation

```
Crea un SOP para: [PROCESO]

Contexto:
- Frecuencia: [diario/semanal/mensual/ad-hoc]
- Responsable: [quién]
- Tiempo estimado: [X minutos]
- Herramientas necesarias: [lista]

El SOP debe incluir:
1. Objetivo del proceso
2. Trigger (qué lo inicia)
3. Pasos numerados con acciones específicas
4. Checklist de verificación
5. Qué hacer si algo falla
6. Output esperado

Formato: Markdown estructurado, listo para guardar en /sops/
```

---

## 5. Metrics Dashboard

```
Genera un dashboard de métricas para [PERÍODO].

Métricas a incluir:
- [LISTA DE KPIS]

Requisitos:
- Visualización clara
- Comparación vs período anterior
- Indicador de tendencia (↑↓→)
- Colores: verde=bien, amarillo=atención, rojo=problema

Formato: HTML interactivo con estilo NGX dark theme (#0D0D0D fondo, #6D00FF acentos).
```

---

## 6. Workflow Documentation

```
Documenta el siguiente workflow de n8n:

Nombre: [NOMBRE]
Propósito: [QUÉ HACE]
Trigger: [QUÉ LO INICIA]
Nodos principales: [LISTA]

Genera:
1. Descripción general
2. Diagrama de flujo (mermaid)
3. Inputs requeridos
4. Outputs generados
5. Dependencias (APIs, credenciales)
6. Troubleshooting común
7. Cómo modificarlo

Formato: Markdown para documentación técnica.
```

---

## 7. Automation Opportunity

```
Analiza este proceso para identificar oportunidades de automatización:

Proceso: [DESCRIPCIÓN]
Frecuencia: [CUÁNTAS VECES]
Tiempo actual: [MINUTOS POR VEZ]
Pasos manuales: [LISTA]

Evalúa:
1. ¿Es automatizable? (sí/parcial/no)
2. Herramientas sugeridas (n8n, Zapier, script, etc.)
3. Esfuerzo de implementación (horas)
4. ROI estimado (tiempo ahorrado/mes)
5. Complejidad (1-5)
6. Recomendación: ¿Vale la pena automatizar ahora?

Formato: Análisis estructurado con recomendación clara.
```

---

## 8. Priority Matrix

```
Ayúdame a priorizar estas tareas usando la matriz Eisenhower:

Tareas:
[LISTA DE TAREAS]

Para cada tarea determina:
- Urgente: ¿Tiene deadline próximo?
- Importante: ¿Impacta objetivos principales?

Genera:
1. Matriz 2x2 con tareas clasificadas
2. Orden de ejecución recomendado
3. Tareas a delegar o eliminar
4. Tiempo bloqueado sugerido

Formato: Visual + lista priorizada.
```

---

## 9. Process Audit

```
Audita el siguiente proceso operativo:

Proceso: [NOMBRE]
SOP actual: [LINK O CONTENIDO]
Frecuencia de uso: [X veces/semana]
Problemas reportados: [LISTA]

Analiza:
1. ¿Los pasos son claros y completos?
2. ¿Hay pasos redundantes?
3. ¿Falta algo crítico?
4. ¿Se puede simplificar?
5. ¿Hay oportunidad de automatizar?

Output:
- Score de calidad (1-10)
- Lista de mejoras sugeridas
- SOP revisado si aplica
```

---

## 10. Incident Report

```
Documenta el siguiente incidente operativo:

Fecha/Hora: [CUÁNDO]
Qué pasó: [DESCRIPCIÓN]
Impacto: [QUÉ SE AFECTÓ]
Cómo se detectó: [CÓMO SUPIMOS]
Resolución: [QUÉ SE HIZO]

Genera:
1. Timeline del incidente
2. Causa raíz (5 Whys)
3. Acciones correctivas
4. Acciones preventivas
5. Lecciones aprendidas
6. Actualización de SOP si aplica

Formato: Documento de incident report.
```

---

*Usar estos prompts como base y adaptar según necesidad.*

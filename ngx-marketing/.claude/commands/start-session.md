# /start-session

Inicializa una sesión de trabajo en este workspace.

## Comportamiento

Al ejecutar este comando, Claude Code debe:

1. **Leer archivos de contexto** (en este orden):
   - `NGX_CONTEXT.md` — Contexto general de NGX
   - `MEMORY.md` — Estado de sesiones anteriores
   - `DECISIONS.md` — Decisiones tomadas previamente
   - `DO_NOT.md` — Reglas y restricciones

2. **Generar resumen de estado**:
   ```
   ## Estado de Sesión
   
   **Última sesión:** [fecha]
   **Última tarea:** [descripción]
   **Pendientes:** [lista]
   **Decisiones activas:** [número]
   ```

3. **Preguntar al usuario**:
   ```
   ¿Continuamos con [tarea pendiente] o hacemos algo nuevo?
   ```

## Ejemplo de Output

```
✅ Sesión iniciada

## Estado de Sesión

**Última sesión:** 2024-12-28
**Última tarea:** Email sequence para leads fríos (completada)
**Pendientes:** Ajustar CTA del email 5
**Decisiones activas:** 3

¿Continuamos con el ajuste del CTA o hacemos algo nuevo?
```

## Notas

- Este comando NO modifica ningún archivo
- Si MEMORY.md está vacío, indicarlo y preguntar qué hacer
- Si hay errores leyendo archivos, reportarlos

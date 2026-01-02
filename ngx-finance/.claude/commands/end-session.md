# /end-session

Finaliza una sesión de trabajo y guarda el estado.

## Comportamiento

Al ejecutar este comando, Claude Code debe:

1. **Solicitar información al usuario** (si no la tiene):
   ```
   Para guardar la sesión necesito:
   - ¿Qué tareas completamos hoy?
   - ¿Cuál es la próxima prioridad?
   - ¿Alguna nota importante para la próxima sesión?
   ```

2. **Actualizar MEMORY.md** con:
   - Fecha de sesión actual
   - Tareas completadas
   - Próxima prioridad
   - Notas relevantes

3. **Actualizar DECISIONS.md** (si hubo decisiones nuevas):
   - Agregar decisiones tomadas durante la sesión

4. **Confirmar al usuario**:
   ```
   ✅ Sesión guardada
   
   ## Resumen
   - Tareas completadas: [lista]
   - Próxima prioridad: [descripción]
   - Decisiones nuevas: [número]
   
   La próxima sesión continuará desde aquí.
   ```

## Ejemplo de Output

```
✅ Sesión guardada

## Resumen

**Tareas completadas:**
- Email sequence leads fríos (7 emails)
- Revisión de copy para ad de Meta

**Próxima prioridad:** 
Crear variaciones de ads para A/B testing

**Decisiones nuevas:** 1
- Usar "usted" para audiencia 45+ en emails

**Archivos generados:**
- outputs/emails/lead-frio-sequence-2024-12-28.md
- outputs/ads/meta-ad-v1-2024-12-28.md

La próxima sesión continuará desde aquí.
```

## Notas

- Este comando SÍ modifica MEMORY.md y posiblemente DECISIONS.md
- Siempre confirmar antes de guardar
- Listar archivos generados durante la sesión

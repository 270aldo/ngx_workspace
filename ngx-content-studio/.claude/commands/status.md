# /status

Muestra el estado actual del workspace sin modificar nada.

## Comportamiento

Al ejecutar este comando, Claude Code debe:

1. **Leer y mostrar estado de MEMORY.md**:
   ```
   ## Estado Actual
   
   **Última sesión:** [fecha]
   **Última tarea:** [descripción]
   **Próxima prioridad:** [descripción]
   ```

2. **Mostrar decisiones activas de DECISIONS.md**:
   ```
   ## Decisiones Activas
   
   - [decisión 1]
   - [decisión 2]
   ```

3. **Mostrar archivos recientes en outputs/**:
   ```
   ## Archivos Recientes
   
   - outputs/emails/[archivo]
   - outputs/ads/[archivo]
   ```

4. **Mostrar errores pendientes de DO_NOT.md** (si hay):
   ```
   ## Errores Pasados a Evitar
   
   - [error documentado]
   ```

## Ejemplo de Output

```
## Estado del Workspace

**Última sesión:** 2024-12-28
**Última tarea:** Email sequence leads fríos
**Próxima prioridad:** Ajustar CTA email 5

---

## Decisiones Activas (3)

1. Usar "usted" para audiencia 45+
2. No usar emojis en emails B2B
3. CTAs siempre en español

---

## Archivos Recientes

- outputs/emails/lead-frio-sequence-2024-12-28.md
- outputs/ads/meta-ad-v1-2024-12-28.md
- outputs/reports/weekly-2024-12-28.md

---

## Errores a Evitar

- Precio incorrecto de HYBRID (usar $1,200, no $1,199)
```

## Notas

- Este comando NO modifica ningún archivo
- Es solo lectura/consulta
- Útil para orientarse al inicio o durante una sesión

# NGX Session Memory

> Este archivo mantiene el estado entre sesiones de Claude Code.
> Claude Code DEBE leer este archivo al iniciar y actualizarlo al terminar.

---

## Estado Actual

**Última sesión**: [FECHA]
**Última tarea completada**: [DESCRIPCIÓN]
**Próxima prioridad**: [DESCRIPCIÓN]

---

## Tareas Completadas

| Fecha | Tarea | Resultado |
|-------|-------|-----------|
| - | - | - |

---

## Tareas Pendientes

| Prioridad | Tarea | Contexto |
|-----------|-------|----------|
| - | - | - |

---

## Decisiones Tomadas

| Fecha | Decisión | Razón |
|-------|----------|-------|
| - | - | - |

---

## Contexto Importante

[Información que debe persistir entre sesiones]

---

## Notas de Sesión Anterior

[Lo que Claude Code debe saber de la sesión anterior]

---

**INSTRUCCIÓN PARA CLAUDE CODE:**

Al INICIAR sesión:
1. Lee este archivo completo
2. Resume el estado actual al usuario
3. Pregunta si continuar con la prioridad pendiente

Al TERMINAR sesión:
1. Actualiza "Última sesión" con fecha actual
2. Actualiza "Última tarea completada"
3. Actualiza "Próxima prioridad"
4. Agrega notas relevantes
5. Guarda el archivo

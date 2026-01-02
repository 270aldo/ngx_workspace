---
description: Diseña un plan de onboarding personalizado para un nuevo Founding Coach
arguments:
  - name: coach
    description: Nombre del coach
    required: true
  - name: clients
    description: Número de clientes que tiene
  - name: tools
    description: Herramientas que usa actualmente
  - name: experience
    description: Nivel de experiencia tech (basic|intermediate|advanced)
    default: intermediate
---

# Plan de Onboarding

**Coach:** $ARGUMENTS.coach
**Clientes:** $ARGUMENTS.clients
**Herramientas actuales:** $ARGUMENTS.tools
**Nivel tech:** $ARGUMENTS.experience

---

## Instrucciones para @onboarding-designer

Diseña un plan de onboarding personalizado:

### Objetivos del Onboarding
1. Time to First Value: <24 hrs
2. Activación día 7: >80%
3. NPS día 14: >50

### Criterios de Activación
Un coach está activado cuando:
- ✅ 3+ clientes en la plataforma
- ✅ 5+ consultas a GENESIS Brain
- ✅ Revisó insights de 1+ cliente
- ✅ Completó sesión 1:1

### Según nivel de experiencia:

**basic** → Más soporte, más touchpoints
- Sesión 1:1 de 45-60 min
- Video tutoriales adicionales
- Check-in día 3, 5, 7
- Línea directa para dudas

**intermediate** → Balance
- Sesión 1:1 de 30-45 min
- Guía de Quick Start
- Check-in día 3, 7
- Grupo de Founding Coaches

**advanced** → Mínimo viable
- Sesión 1:1 de 30 min
- Documentación self-serve
- Check-in día 7
- Acceso a features avanzadas rápido

### Plan a Generar:

1. **Timeline de 14 días**
   - Día 0: Bienvenida + accesos
   - Día 1-2: Onboarding 1:1
   - Día 3-7: Activación guiada
   - Día 8-14: Profundización

2. **Emails personalizados**
   - Email de bienvenida
   - Email día 3 (check-in)
   - Email día 7 (primer milestone)
   - Email día 14 (feedback)

3. **Agenda de sesión 1:1**
   - Setup de cuenta
   - Agregar primeros clientes
   - Momento Aha
   - Próximos pasos

4. **Métricas a trackear**
   - Clientes agregados
   - Consultas realizadas
   - Features usadas
   - Soporte necesitado

5. **Playbook de rescate**
   - Qué hacer si no activa día 7
   - Scripts de llamada de rescate

---

## Output

Guarda en: `outputs/onboarding/$(date +%Y-%m-%d)-$ARGUMENTS.coach-onboarding-plan.md`

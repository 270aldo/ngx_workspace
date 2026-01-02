# SOP: Onboarding de Cliente Nuevo

**Versión:** 1.0
**Última actualización:** 2025-01-01
**Responsable:** Operations
**Tiempo estimado:** 45 minutos

---

## Objetivo

Configurar completamente a un nuevo cliente en el sistema NGX para que pueda empezar a usar el producto sin fricciones.

---

## Trigger

Este proceso se ejecuta cuando:
- Un cliente completa el pago de NGX ASCEND o NGX HYBRID
- Un Founding Coach confirma participación en el programa piloto

---

## Prerequisitos

Antes de empezar, asegúrate de tener:
- [ ] Email del cliente confirmado
- [ ] Nombre completo del cliente
- [ ] Producto adquirido (ASCEND/HYBRID/COACH)
- [ ] Comprobante de pago recibido
- [ ] Acceso al panel de Supabase
- [ ] Acceso a la plataforma de email marketing

---

## Pasos

### 1. Crear Usuario en Base de Datos

**Acción:** Crear registro del cliente en Supabase

**Detalles:**
- Ir a Supabase → Table Editor → `users`
- Crear nuevo registro con:
  - `email`: Email del cliente
  - `name`: Nombre completo
  - `subscription_type`: ASCEND | HYBRID | COACH
  - `subscription_status`: active
  - `started_at`: Fecha actual
  - `trial_ends_at`: NULL (o fecha si aplica)

**Output esperado:** ID de usuario generado

---

### 2. Configurar Acceso a la App

**Acción:** Enviar invitación para crear cuenta

**Detalles:**
- Usar el sistema de invitación de Supabase Auth
- Verificar que el email de invitación se envíe correctamente
- El cliente recibirá link para crear contraseña

**Output esperado:** Email de invitación enviado

---

### 3. Crear Perfil Inicial de Agentes

**Acción:** Preparar la configuración base de los 13 agentes

**Detalles:**
- Crear registro en `user_profiles` con defaults
- Los agentes se configurarán con el onboarding quiz
- Verificar que NEXUS esté habilitado como orquestador

**Output esperado:** Perfil de agentes creado con configuración default

---

### 4. Agregar a Email Marketing

**Acción:** Agregar cliente a la lista correspondiente

**Detalles:**
- Agregar a lista: `clientes-activos`
- Agregar tag según producto: `ascend` | `hybrid` | `coach`
- Iniciar secuencia de onboarding automática
- Verificar que el email no esté en blacklist

**Output esperado:** Cliente en lista con tags correctos

---

### 5. Enviar Welcome Kit

**Acción:** Enviar email de bienvenida personalizado

**Detalles:**
- Usar template: `welcome-[producto]`
- Incluir:
  - Link para descargar app (si ASCEND/HYBRID)
  - Credenciales de acceso
  - Link al onboarding quiz
  - Contacto de soporte
  - Calendario para agendar call (si HYBRID)

**Output esperado:** Email de bienvenida enviado

---

### 6. Agendar Call de Onboarding (Solo HYBRID)

**Acción:** Coordinar primera sesión con el coach

**Detalles:**
- Enviar link de Calendly para agendar
- Disponibilidad: Dentro de los primeros 5 días
- Duración: 45 minutos
- Preparar agenda de la call

**Output esperado:** Call agendada en calendario

---

### 7. Actualizar CRM

**Acción:** Registrar cliente en sistema de tracking

**Detalles:**
- Cambiar status de lead a `customer`
- Registrar fecha de conversión
- Agregar notas del proceso de venta
- Asignar a pipeline de "Clientes Activos"

**Output esperado:** CRM actualizado

---

### 8. Notificar al Equipo

**Acción:** Comunicar internamente el nuevo cliente

**Detalles:**
- Enviar mensaje a Slack #nuevos-clientes
- Incluir: Nombre, producto, canal de adquisición
- Celebrar el win 🎉

**Output esperado:** Equipo notificado

---

## Checklist de Verificación

Al terminar, verifica:
- [ ] Cliente puede hacer login en la app
- [ ] Perfil de agentes creado
- [ ] Email de bienvenida recibido (revisar spam)
- [ ] Cliente en lista de email correcta
- [ ] CRM actualizado con status "customer"
- [ ] Call de onboarding agendada (si HYBRID)

---

## Troubleshooting

### Problema: Email de invitación no llega
**Síntomas:** Cliente no recibe email después de 10 minutos
**Solución:**
1. Verificar email en Supabase Auth → Users
2. Revisar logs de email en provider
3. Pedir al cliente revisar spam
4. Re-enviar invitación manualmente

### Problema: Error al crear usuario en Supabase
**Síntomas:** Error de duplicado o validación
**Solución:**
1. Verificar si usuario ya existe
2. Revisar formato de email
3. Verificar que no haya restricción de dominio

### Problema: Cliente no puede hacer login
**Síntomas:** "Invalid credentials" o "User not found"
**Solución:**
1. Verificar que completó el registro
2. Enviar link de reset password
3. Verificar status en Supabase Auth

---

## Output Esperado

Al completar este proceso debes tener:
- Usuario activo en la plataforma
- Cliente puede acceder a la app
- Email de bienvenida recibido
- Cliente listo para empezar a usar los agentes

---

## Referencias

- [Supabase Dashboard](https://app.supabase.com)
- [Panel de Email Marketing]
- Template: `/templates/emails/welcome-sequence.md`

---

## Historial de Cambios

| Versión | Fecha | Autor | Cambio |
|---------|-------|-------|--------|
| 1.0 | 2025-01-01 | Aldo | Creación inicial |

---

*SOP Onboarding Cliente NGX v1.0*

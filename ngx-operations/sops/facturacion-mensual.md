# SOP: Facturación Mensual

**Versión:** 1.0
**Última actualización:** 2025-01-01
**Responsable:** Finance/Operations
**Tiempo estimado:** 30-45 minutos

---

## Objetivo

Generar y enviar todas las facturas mensuales a clientes activos de NGX GENESIS, asegurando el cobro correcto y puntual.

---

## Trigger

Este proceso se ejecuta cuando:
- Es el día 1 del mes (para subscripciones mensuales)
- Un cliente solicita factura específica
- Hay un pago manual que requiere factura

---

## Prerequisitos

Antes de empezar, asegúrate de tener:
- [ ] Lista actualizada de clientes activos
- [ ] Precios vigentes por producto
- [ ] Plantilla de factura actualizada
- [ ] Datos fiscales de cada cliente (si aplica)
- [ ] Acceso al sistema de pagos (Stripe/PayPal)
- [ ] Acceso a email de facturación

---

## Pasos

### 1. Obtener Lista de Clientes a Facturar

**Acción:** Exportar lista de clientes con subscripción activa

**Detalles:**
- Ir a Supabase → `subscriptions` table
- Filtrar por `status = 'active'`
- Exportar: ID, nombre, email, producto, precio, fecha inicio
- Verificar que no haya duplicados
- Separar por tipo de facturación (automática vs manual)

**Output esperado:** Lista de clientes a facturar

---

### 2. Verificar Pagos Automáticos (Stripe)

**Acción:** Confirmar cobros exitosos del mes

**Detalles:**
- Ir a Stripe Dashboard → Payments
- Filtrar por el mes actual
- Identificar:
  - ✅ Pagos exitosos
  - ❌ Pagos fallidos
  - ⏳ Pagos pendientes
- Documentar cualquier fallo para seguimiento

**Output esperado:** Reporte de pagos del mes

---

### 3. Generar Facturas

**Acción:** Crear factura para cada cliente

**Detalles:**

Para cada cliente:
1. Abrir template de factura
2. Completar datos:
   - **Número:** NGX-[YYYYMM]-[NNN] (secuencial)
   - **Fecha emisión:** Día actual
   - **Fecha vencimiento:** +15 días
   - **Cliente:** Nombre y datos fiscales
   - **Concepto:** Subscripción [PRODUCTO] - [Mes Año]
   - **Monto:** Precio del producto
   - **IVA:** 16% si aplica
   - **Total:** Subtotal + IVA

3. Guardar como PDF
4. Nombrar archivo: `NGX-YYYYMM-NNN_NombreCliente.pdf`

**Output esperado:** Facturas PDF generadas

---

### 4. Enviar Facturas

**Acción:** Enviar cada factura por email

**Detalles:**
- Subject: `Factura NGX GENESIS - [Mes Año] | #NGX-YYYYMM-NNN`
- Body: Usar template de email de factura
- Adjuntar: PDF de la factura
- CC: facturacion@ngxgenesis.com (registro interno)
- Verificar que el email se envía correctamente

**Template de email:**
```
Hola [Nombre],

Adjunto encontrarás tu factura correspondiente a [Mes Año].

Detalles:
- Factura: #NGX-YYYYMM-NNN
- Concepto: Subscripción [PRODUCTO]
- Monto: $[X] USD
- Vencimiento: [Fecha]

Si tienes alguna pregunta sobre esta factura, responde a este email.

Gracias por ser parte de NGX GENESIS.

— Equipo NGX
```

**Output esperado:** Todas las facturas enviadas

---

### 5. Gestionar Pagos Fallidos

**Acción:** Dar seguimiento a cobros no exitosos

**Detalles:**
Para cada pago fallido:
1. Identificar razón del fallo (Stripe → Payment → Failed)
2. Enviar email de notificación al cliente
3. Reintentar cobro si es posible
4. Documentar en CRM
5. Si persiste después de 3 intentos: marcar para contacto directo

**Email de pago fallido:**
```
Hola [Nombre],

Tuvimos un problema al procesar tu pago de [Mes].

Por favor verifica:
- Que tu tarjeta esté vigente
- Que tengas fondos disponibles
- Que no haya restricciones del banco

Puedes actualizar tu método de pago aquí: [Link]

Si necesitas ayuda, responde a este email.

— Equipo NGX
```

**Output esperado:** Pagos fallidos gestionados

---

### 6. Actualizar Registros

**Acción:** Documentar todo el proceso de facturación

**Detalles:**
- Actualizar spreadsheet de facturación con:
  - Facturas generadas
  - Facturas enviadas
  - Pagos confirmados
  - Pagos pendientes
- Actualizar Supabase con status de factura
- Guardar copias de facturas en carpeta del mes

**Output esperado:** Registros actualizados

---

### 7. Generar Reporte del Mes

**Acción:** Crear resumen de facturación mensual

**Detalles:**
- Total facturado: $[X]
- Número de facturas: [N]
- Cobros exitosos: [N] ($[X])
- Cobros fallidos: [N] ($[X])
- Pendientes de cobro: [N] ($[X])
- Tasa de cobro exitoso: [X%]

**Output esperado:** Reporte de facturación del mes

---

## Checklist de Verificación

Al terminar, verifica:
- [ ] Todas las facturas generadas con número secuencial
- [ ] Todas las facturas enviadas por email
- [ ] Pagos fallidos identificados y gestionados
- [ ] Registros actualizados en spreadsheet
- [ ] Copias de facturas guardadas
- [ ] Reporte mensual generado

---

## Troubleshooting

### Problema: Cliente no recibe factura
**Síntomas:** Cliente dice que no llegó el email
**Solución:**
1. Verificar email correcto en sistema
2. Pedir revisar spam/promociones
3. Re-enviar desde otra cuenta
4. Ofrecer envío por WhatsApp como alternativa

### Problema: Error en monto de factura
**Síntomas:** Cliente reporta monto incorrecto
**Solución:**
1. Verificar precio en sistema
2. Si hay error: generar nota de crédito
3. Emitir factura corregida
4. Documentar el error y causa

### Problema: Stripe no procesa reintento
**Síntomas:** Cobro sigue fallando
**Solución:**
1. Contactar cliente directamente
2. Ofrecer link de pago manual
3. Considerar pausa de servicio si no responde
4. Escalar a caso de cobranza

---

## Output Esperado

Al completar este proceso debes tener:
- Todas las facturas del mes generadas y enviadas
- Pagos confirmados registrados
- Pagos fallidos en seguimiento
- Reporte mensual de facturación

---

## Precios Vigentes

| Producto | Precio Mensual | IVA | Total |
|----------|----------------|-----|-------|
| NGX ASCEND | $100 USD | N/A | $100 USD |
| NGX HYBRID | $400 USD/mes (temporada) | N/A | $400 USD |
| NGX COACH (Founding) | $199 USD | N/A | $199 USD |
| NGX COACH (Regular) | $299 USD | N/A | $299 USD |

---

## Calendario de Facturación

| Día | Acción |
|-----|--------|
| 1 | Generar facturas del mes |
| 1-3 | Enviar todas las facturas |
| 5 | Primer seguimiento pagos fallidos |
| 10 | Segundo seguimiento |
| 15 | Fecha límite de pago |
| 16+ | Escalación de no-pagos |

---

## Referencias

- Template de factura: `/templates/invoices/invoice-template.md`
- [Stripe Dashboard](https://dashboard.stripe.com)
- [PayPal Business](https://business.paypal.com)

---

## Historial de Cambios

| Versión | Fecha | Autor | Cambio |
|---------|-------|-------|--------|
| 1.0 | 2025-01-01 | Aldo | Creación inicial |

---

*SOP Facturación Mensual NGX v1.0*

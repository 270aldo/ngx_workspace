# DO NOT — Errores a Evitar

> Este archivo documenta errores comunes y restricciones absolutas.
> Claude Code DEBE leer esto al inicio de cada sesión.

---

## 🚫 NUNCA HACER (Reglas Absolutas)

### Precios
- **NO** usar $99 → usar **$100**
- **NO** usar $297 o $299 → usar **$300**
- **NO** usar $1,197 o $1,199 → usar **$1,200**
- **NO** inventar precios que no existen
- **NO** ofrecer descuentos no autorizados

### Productos
- **NO** mencionar features que no existen
- **NO** prometer integraciones no implementadas
- **NO** confundir ASCEND con HYBRID
- **NO** decir que ASCEND incluye coach humano
- **NO** cambiar nombres de agentes

### Voz de Marca
- **NO** usar tono "bro" o demasiado casual
- **NO** usar clickbait o promesas exageradas
- **NO** copiar estilo de competidores
- **NO** usar emojis excesivos (máximo 1-2 por pieza)
- **NO** tutear a audiencia 45-60 (usar "usted")

### Técnico
- **NO** crear archivos fuera de `outputs/`
- **NO** modificar archivos en `templates/` sin permiso
- **NO** borrar contenido de `MEMORY.md` sin confirmar
- **NO** ignorar el checklist de calidad

### Contenido
- **NO** generar contenido sin verificar NGX_CONTEXT.md
- **NO** inventar testimoniales o casos de estudio
- **NO** usar estadísticas sin fuente
- **NO** copiar contenido de otros (plagiar)

---

## ⚠️ EVITAR (Mejores Prácticas)

### Comunicación
- Evitar jerga técnica con audiencia no-técnica
- Evitar párrafos largos en emails (máximo 3-4 líneas)
- Evitar CTAs múltiples (1 CTA principal por pieza)
- Evitar tonos condescendientes o paternalistas

### Estructura
- Evitar documentos sin headers claros
- Evitar listas sin contexto
- Evitar outputs sin nombre descriptivo
- Evitar archivos sin fecha en el nombre cuando aplique

### Proceso
- Evitar empezar sin leer MEMORY.md
- Evitar terminar sin actualizar MEMORY.md
- Evitar ignorar decisiones previas en DECISIONS.md
- Evitar saltarse el checklist de calidad

---

## 📝 Errores Pasados (Aprendizajes)

| Fecha | Error | Corrección | Impacto |
|-------|-------|------------|---------|
| - | - | - | - |

---

**INSTRUCCIÓN PARA CLAUDE CODE:**
Si estás a punto de hacer algo de la lista "NUNCA HACER", DETENTE y pregunta al usuario. No hay excepciones.

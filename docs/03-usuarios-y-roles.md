# 03 — Usuarios y roles

## Enfoque general

Existirá una sola plataforma con experiencias diferenciadas por permisos. Una persona podrá ser cliente, proveedor o tener ambos roles cuando el modelo de datos lo permita.

## Cliente

### Necesidades

- Explicar rápidamente qué problema tiene.
- Encontrar opciones confiables.
- Comparar precio, experiencia y disponibilidad.
- Conocer el estado de su solicitud.
- Calificar o reportar una experiencia.

### Acciones principales

- Gestionar su perfil.
- Crear y cancelar solicitudes bajo reglas definidas.
- Revisar cotizaciones.
- Aceptar una cotización.
- Confirmar el resultado del servicio.
- Calificar y reportar.

## Proveedor

El término proveedor incluye inicialmente trabajadores independientes, técnicos y pequeños negocios de servicios.

### Necesidades

- Conseguir oportunidades relevantes.
- Mostrar experiencia y confianza.
- Cotizar sin procesos complicados.
- Administrar trabajos aceptados.
- Construir reputación.

### Acciones principales

- Gestionar perfil profesional.
- Registrar categorías y zonas.
- Completar verificación.
- Ver oportunidades compatibles.
- Enviar, retirar o actualizar cotizaciones según reglas.
- Administrar servicios adjudicados.

## Administrador

### Responsabilidades

- Proteger la calidad y seguridad de la plataforma.
- Verificar proveedores.
- Administrar catálogos.
- Investigar reportes.
- Aplicar suspensiones justificadas.
- Auditar acciones sensibles.

El administrador no debe modificar silenciosamente acuerdos entre cliente y proveedor. Las acciones sensibles deberán quedar registradas.

## Estados de verificación sugeridos

```text
Pendiente → En revisión → Verificado
                     └→ Rechazado
Verificado → Suspendido
```

Los requisitos exactos de verificación deberán definirse considerando normativa, privacidad y operación real en Bolivia.

## Autorización

- Los permisos deben comprobarse en la API.
- Ocultar un botón en la interfaz no reemplaza la autorización del servidor.
- Las operaciones administrativas deben exigir un rol explícito.
- Los usuarios solamente deben acceder a información necesaria para su función.

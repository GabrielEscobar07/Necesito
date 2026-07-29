# ADR 0003 — Una cuenta con múltiples roles

- **Estado:** Aceptada.
- **Fecha:** 2026-07-28.

## Contexto

Una persona que ofrece servicios también puede necesitar contratar a otro profesional. Crear aplicaciones o cuentas separadas duplicaría identidad, contacto, autenticación y mantenimiento.

## Decisión

La plataforma utilizará una sola cuenta de usuario. Esa cuenta podrá tener perfil de cliente, perfil de proveedor o ambos. La experiencia visual permitirá cambiar de modo, mientras el backend aplicará permisos por rol y propiedad de cada recurso.

El rol administrador se asignará de forma controlada y no estará disponible en el registro público.

## Consecuencias positivas

- Menos cuentas duplicadas.
- Inicio de sesión único.
- Una sola aplicación web/PWA.
- Posibilidad de reutilizar datos comunes de forma controlada.
- Menor costo de desarrollo y mantenimiento.

## Consecuencias y cuidados

- La navegación deberá indicar claramente el modo activo.
- Tener un rol no concede acceso a recursos ajenos.
- Los perfiles de cliente y proveedor deben mantenerse separados de la identidad base.
- Las acciones administrativas requieren permisos adicionales y auditoría.
- Las notificaciones deberán indicar a qué contexto pertenecen.

## Alternativas descartadas

### Dos aplicaciones independientes

Descartada para el MVP por duplicar frontend, autenticación, despliegues y componentes.

### Dos cuentas por persona

Descartada por generar duplicados, confusión y problemas para recuperar identidad e historial.
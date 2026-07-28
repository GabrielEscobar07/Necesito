# ADR-0001 — Aplicación unificada con experiencias por rol

- **Estado:** Aceptada
- **Fecha:** 2026-07-28

## Contexto

La plataforma tendrá clientes que solicitan servicios, proveedores que cotizan y administradores que supervisan la operación. Se evaluó crear aplicaciones web separadas para cada tipo de usuario.

## Decisión

Construir inicialmente una sola aplicación web/PWA con áreas, rutas y permisos diferenciados por rol.

La API y la base de datos también serán compartidas. Una cuenta podrá soportar más de un rol cuando el modelo funcional se defina completamente.

## Consecuencias positivas

- Menor duplicación de componentes y configuración.
- Una sola experiencia de autenticación.
- Menor costo de desarrollo y despliegue.
- Diseño y reglas consistentes.
- Posibilidad de cambiar entre modo cliente y proveedor en el futuro.

## Riesgos y mitigaciones

- La aplicación puede crecer demasiado: se organizará por áreas y módulos.
- Una autorización incorrecta podría exponer funciones: la API validará todos los permisos.
- Las experiencias pueden confundirse: la navegación será distinta según contexto y rol.

## Alternativas consideradas

### Dos aplicaciones web separadas

Rechazada para el MVP por duplicar configuración, componentes, despliegues y mantenimiento.

### Aplicación móvil separada desde el inicio

Rechazada hasta validar el producto. Se mantiene React Native con Expo como evolución futura.

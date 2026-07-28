# 06 — Arquitectura inicial

## Estilo

La primera versión utilizará un **monolito modular** dentro de un monorepositorio.

```text
Web/PWA Next.js
       │ HTTPS/JSON
       ▼
API ASP.NET Core
       │
       ▼
PostgreSQL
```

## Razones

- Reduce complejidad operativa al comenzar.
- Permite desarrollar y desplegar una sola API.
- Conserva transacciones simples entre módulos.
- Facilita depuración, pruebas y cambios rápidos.
- Puede dividirse posteriormente si existe una razón técnica o de negocio.

## Módulos candidatos del backend

```text
Identity
Users
Providers
ServiceCatalog
ServiceRequests
Quotes
Jobs
Reviews
Moderation
Notifications
```

Estos nombres son candidatos, no proyectos creados todavía. Se confirmarán al modelar el dominio.

## Responsabilidades preliminares

- **Identity:** autenticación, sesiones y autorización.
- **Users:** perfiles y datos generales.
- **Providers:** perfil profesional, categorías, zonas y verificación.
- **ServiceCatalog:** categorías y tipos de servicio.
- **ServiceRequests:** solicitudes publicadas por clientes.
- **Quotes:** propuestas enviadas por proveedores.
- **Jobs:** contratación, ejecución y cierre.
- **Reviews:** reputación y calificaciones.
- **Moderation:** reportes, suspensiones y auditoría.
- **Notifications:** avisos internos y futuros canales externos.

## Límites

- Cada módulo será responsable de sus reglas y datos.
- No se accederá arbitrariamente a la lógica interna de otro módulo.
- Los contratos entre módulos deberán ser explícitos.
- El código compartido se mantendrá mínimo.
- No se crearán microservicios durante el MVP.

## Frontend

La aplicación web tendrá una base común y áreas protegidas por rol:

```text
/                    Sitio público
/solicitudes         Experiencia de cliente
/proveedor            Experiencia profesional
/admin                Administración
```

Las rutas definitivas se decidirán al diseñar navegación y autenticación.

## Datos

PostgreSQL será la fuente principal de verdad. Las operaciones críticas, como aceptar una cotización, deberán ejecutarse transaccionalmente.

## Integraciones futuras

Correo, WhatsApp, mapas, almacenamiento de imágenes y pagos se tratarán como adaptadores externos. Ninguna integración debe quedar acoplada directamente al dominio central.

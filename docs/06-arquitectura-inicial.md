# 06 — Arquitectura inicial

## Estilo

La primera versión utilizará un **monolito modular** dentro de un monorepositorio.

```text
Web/PWA Next.js
       │ HTTPS/JSON
       ▼
API ASP.NET Core
       │ Entity Framework Core
       ▼
MySQL
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
Profiles
Catalog
Verification
ServiceRequests
Quotes
Engagements
Reviews
TrustAndSafety
Notifications
```

Estos nombres son candidatos, no proyectos creados todavía. Se confirmarán al modelar la solución de ASP.NET Core.

## Responsabilidades preliminares

- **Identity:** autenticación, sesiones y autorización.
- **Profiles:** perfiles de cliente y proveedor.
- **Catalog:** categorías, especialidades, ciudades y zonas.
- **Verification:** documentos y revisión de proveedores.
- **ServiceRequests:** solicitudes publicadas por clientes.
- **Quotes:** propuestas enviadas por proveedores.
- **Engagements:** contratación, ejecución y cierre.
- **Reviews:** reputación y calificaciones.
- **TrustAndSafety:** reportes, suspensiones y auditoría.
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
/cliente             Experiencia de cliente
/proveedor           Experiencia profesional
/admin               Administración
```

La interfaz se diseñará mobile-first con componentes reutilizables, estados de carga y error, formularios accesibles y separación entre datos públicos y privados.

## Datos

MySQL será la fuente principal de verdad. Las operaciones críticas, como aceptar una cotización, deberán ejecutarse transaccionalmente.

Cada entorno tendrá una base independiente:

```text
necesito_dev       Desarrollo local
necesito_test      Pruebas automatizadas
necesito_prod      Producción futura
```

Los nombres son provisionales. Nunca se compartirán tablas o credenciales con otros sistemas.

## Ubicación

La primera etapa utilizará ciudad, zona y coordenadas opcionales. La dirección exacta permanecerá protegida según el estado de la contratación. No se incorporará una tecnología geográfica adicional hasta validar una necesidad concreta.

## Integraciones futuras

Correo, WhatsApp, mapas, almacenamiento de imágenes y pagos se tratarán como adaptadores externos. Ninguna integración debe quedar acoplada directamente al dominio central.
# ADR 0004 — MySQL como base de datos principal

- **Estado:** Aceptada.
- **Fecha:** 2026-07-29.

## Contexto

El diseño inicial contemplaba PostgreSQL y PostGIS. El equipo decidió usar MySQL porque ya posee experiencia operativa con este motor en el Sistema Administrativo La Vieja TATTOO, lo que reduce la curva de aprendizaje y facilita el mantenimiento inicial.

El proyecto Necesito seguirá siendo completamente independiente: no compartirá la misma base, tablas, usuarios de aplicación ni datos con el sistema administrativo.

## Decisión

Utilizar **MySQL** como base de datos relacional principal del MVP.

La base local se levantará de forma reproducible mediante Docker Compose y tendrá credenciales exclusivas mediante variables de entorno. El nombre provisional para desarrollo será `necesito_dev`.

ASP.NET Core accederá a MySQL mediante una capa de persistencia definida posteriormente. Las migraciones serán la fuente de verdad del esquema.

## Consecuencias positivas

- Aprovecha experiencia previa del equipo.
- Reduce herramientas diferentes durante el inicio.
- Permite transacciones, restricciones, índices y relaciones suficientes para el MVP.
- Cuenta con soporte maduro desde .NET mediante proveedores compatibles.
- Puede ejecutarse localmente con Docker Compose.

## Consecuencias y cuidados

- No se utilizará PostGIS, porque es una extensión de PostgreSQL.
- La ubicación inicial se modelará con ciudad, zona, dirección protegida y, cuando sea necesario, latitud/longitud.
- Las búsquedas geográficas avanzadas se evaluarán más adelante usando capacidades espaciales de MySQL o un servicio especializado.
- No se reutilizará la base del Sistema Administrativo La Vieja TATTOO.
- Cada entorno tendrá su propia base, usuario y contraseña.
- La elección del proveedor de Entity Framework Core deberá comprobar compatibilidad con la versión de .NET y MySQL elegidas.

## Alternativas consideradas

### PostgreSQL con PostGIS

Era la decisión original y sigue siendo una alternativa fuerte para geolocalización avanzada, pero añade otro motor que el equipo tendría que administrar desde el comienzo.

### Compartir la base del sistema administrativo

Rechazada. Mezclar proyectos produciría acoplamiento, riesgo de seguridad, migraciones conflictivas y pérdida de independencia.

## Revisión futura

La decisión podrá revisarse únicamente si aparecen necesidades geográficas, de escala o de operación que MySQL no resuelva adecuadamente y existe evidencia suficiente para justificar una migración.
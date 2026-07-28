# ADR-0002 — Monolito modular como arquitectura inicial

- **Estado:** Aceptada
- **Fecha:** 2026-07-28

## Contexto

El producto contempla usuarios, proveedores, solicitudes, cotizaciones, contrataciones, reputación y administración. Aunque podría crecer considerablemente, el equipo necesita desarrollar y validar primero una versión inicial.

## Decisión

Implementar la API como un monolito modular en ASP.NET Core.

Los módulos tendrán límites y responsabilidades explícitos, pero se desplegarán juntos y utilizarán inicialmente una misma instancia de PostgreSQL.

## Consecuencias positivas

- Menor complejidad operativa.
- Desarrollo y depuración más sencillos.
- Transacciones consistentes entre funciones relacionadas.
- Menos infraestructura y menor costo inicial.
- Separación interna suficiente para evolucionar posteriormente.

## Riesgos y mitigaciones

- Acoplamiento entre módulos: se definirán contratos y reglas de dependencia.
- Crecimiento desordenado: cada funcionalidad pertenecerá a un módulo.
- Base de datos compartida: se respetará la propiedad lógica de datos por módulo.

## Alternativas consideradas

### Microservicios

Rechazados para el MVP por aumentar despliegues, observabilidad, comunicación distribuida y costo operativo sin una necesidad comprobada.

### Monolito sin módulos explícitos

Rechazado porque facilitaría el crecimiento desordenado y dificultaría una separación futura.

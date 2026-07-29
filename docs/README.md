# Documentación del proyecto

Esta carpeta reúne la documentación funcional, técnica y de planificación de Necesito. El nombre del producto continúa siendo provisional.

## Fundamentos

| Documento | Propósito |
|---|---|
| [01 — Visión del proyecto](01-vision-del-proyecto.md) | Problema, propuesta de valor y dirección general. |
| [02 — Alcance inicial](02-alcance-inicial.md) | Incluido y excluido en la primera etapa. |
| [03 — Usuarios y roles](03-usuarios-y-roles.md) | Actores, permisos y necesidades. |
| [04 — Flujo del servicio](04-flujo-del-servicio.md) | Ciclo desde la solicitud hasta la calificación. |
| [05 — Stack tecnológico](05-stack-tecnologico.md) | Tecnologías elegidas y propósito. |
| [06 — Arquitectura inicial](06-arquitectura-inicial.md) | Estructura lógica del sistema. |
| [07 — Roadmap](07-roadmap.md) | Etapas previstas del producto. |
| [08 — Glosario](08-glosario.md) | Términos compartidos por el equipo. |
| [09 — Plan de la etapa 0](09-plan-etapa-0.md) | Estado de preparación previa al código. |

## Definición del MVP

| Documento | Propósito |
|---|---|
| [10 — Requisitos del MVP](10-requisitos-del-mvp.md) | Requisitos funcionales y no funcionales. |
| [11 — Reglas de negocio](11-reglas-de-negocio.md) | Restricciones que protegen el flujo. |
| [12 — Historias de usuario](12-historias-de-usuario-mvp.md) | Necesidades priorizadas y aceptación resumida. |
| [13 — Modelo de dominio](13-modelo-de-dominio-inicial.md) | Módulos, entidades y relaciones conceptuales. |
| [14 — Estados y transiciones](14-estados-y-transiciones.md) | Ciclos de vida de solicitudes, cotizaciones y servicios. |
| [15 — Verificación y confianza](15-verificacion-y-confianza.md) | Proceso y límites de la verificación. |
| [16 — Seguridad y privacidad](16-seguridad-y-privacidad.md) | Protección de cuentas, documentos y ubicación. |
| [17 — Mapa de navegación](17-mapa-de-navegacion.md) | Áreas públicas y paneles por rol. |
| [18 — Notificaciones](18-notificaciones-y-comunicacion.md) | Eventos y canales previstos. |
| [19 — Aceptación del MVP](19-criterios-de-aceptacion-del-mvp.md) | Condiciones para una prueba controlada. |

## Planificación

| Documento | Propósito |
|---|---|
| [20 — Backlog inicial](20-backlog-inicial.md) | Épicas y prioridades de implementación. |
| [21 — Riesgos y pendientes](21-riesgos-supuestos-y-pendientes.md) | Hipótesis, riesgos y decisiones abiertas. |
| [22 — Inicio técnico](22-plan-de-inicio-tecnico.md) | Orden para preparar web, API y PostgreSQL. |

## Decisiones de arquitectura

Las decisiones importantes se registran en [`adr/`](adr/README.md). Actualmente se documentan la aplicación unificada, el monolito modular y una cuenta con múltiples roles.

## Reglas de mantenimiento

- Actualizar el documento afectado cuando cambie una regla del producto.
- Evitar duplicar definiciones en distintos archivos.
- Marcar claramente hipótesis y decisiones pendientes.
- Mantener los documentos independientes de un nombre comercial definitivo.
- Registrar decisiones estructurales mediante ADR.
- Convertir el backlog en Issues pequeños cuando comience la implementación.
- No presentar decisiones provisionales como requisitos legales confirmados.
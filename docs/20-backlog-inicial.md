# 20 — Backlog inicial

## Uso

Este backlog organiza el trabajo por resultados. Los elementos se convertirán posteriormente en Issues de GitHub más pequeños y estimables.

## Épica 0 — Preparación técnica

- [ ] Verificar Git, Node.js, gestor de paquetes, .NET SDK y Docker Desktop.
- [x] Clonar el repositorio localmente.
- [ ] Inicializar Next.js con TypeScript y Tailwind en `apps/web`.
- [ ] Inicializar ASP.NET Core en `apps/api`.
- [ ] Crear MySQL con Docker Compose usando una base exclusiva para Necesito.
- [ ] Configurar Entity Framework Core y migraciones para MySQL.
- [ ] Definir variables de entorno de ejemplo.
- [ ] Confirmar comunicación web → API → base de datos.
- [ ] Crear validaciones iniciales de CI.

## Épica 1 — Identidad y acceso — P0

- [ ] Registro e inicio de sesión.
- [ ] Recuperación de acceso.
- [ ] Roles cliente, proveedor y administrador.
- [ ] Autorización por rol y recurso.
- [ ] Cambio de modo cliente/proveedor.

## Épica 2 — Catálogo y zonas — P0

- [ ] Categorías iniciales.
- [ ] Especialidades.
- [ ] Ciudades y zonas.
- [ ] Administración de disponibilidad de catálogos.

## Épica 3 — Perfil proveedor y verificación — P0

- [ ] Perfil profesional.
- [ ] Categorías y zonas de atención.
- [ ] Carga protegida de documentos.
- [ ] Flujo de revisión administrativa.
- [ ] Estado y distintivo de verificación.

## Épica 4 — Solicitudes — P0

- [ ] Crear y guardar borrador.
- [ ] Publicar solicitud.
- [ ] Adjuntar fotografías.
- [ ] Consultar historial y estados.
- [ ] Cancelar o vencer solicitud.
- [ ] Filtrar proveedores compatibles.

## Épica 5 — Cotizaciones — P0

- [ ] Enviar cotización.
- [ ] Editar o retirar antes de aceptar.
- [ ] Comparar propuestas.
- [ ] Aceptar una sola propuesta.
- [ ] Marcar cotizaciones restantes.

## Épica 6 — Contrataciones — P0

- [ ] Crear contratación desde cotización.
- [ ] Compartir datos mínimos de coordinación.
- [ ] Gestionar estados válidos.
- [ ] Registrar cancelación y motivo.
- [ ] Confirmar finalización.

## Épica 7 — Reputación — P1

- [ ] Registrar calificación.
- [ ] Calcular promedio y cantidad.
- [ ] Moderar comentarios.
- [ ] Mostrar reputación en perfiles y cotizaciones.

## Épica 8 — Administración y soporte — P1

- [ ] Panel de verificaciones.
- [ ] Gestión de usuarios y suspensiones.
- [ ] Gestión de categorías y zonas.
- [ ] Reportes e incidencias.
- [ ] Auditoría de acciones sensibles.

## Épica 9 — Notificaciones — P1

- [ ] Centro de notificaciones.
- [ ] Avisos de nuevas cotizaciones y contrataciones.
- [ ] Avisos de verificación y reportes.
- [ ] Correo para eventos críticos.

## Épica 10 — Calidad y lanzamiento controlado — P1

- [ ] Pruebas de reglas críticas.
- [ ] Pruebas de integración.
- [ ] Datos semilla de demostración.
- [ ] Revisión responsive y accesibilidad.
- [ ] Registro de errores y salud del sistema.
- [ ] Copias de seguridad y recuperación.
- [ ] Términos, privacidad y proceso de soporte.

## Posterior al MVP — P2

- [ ] Búsqueda geográfica avanzada con capacidades espaciales de MySQL o servicio especializado.
- [ ] SignalR y comunicación en tiempo real.
- [ ] Redis cuando exista una necesidad medida.
- [ ] Notificaciones push.
- [ ] Pagos internos y garantías.
- [ ] Planes comerciales.
- [ ] Nuevas ciudades y categorías.
- [ ] Aplicación React Native con Expo.
- [ ] Proveedores empresariales y repuestos.
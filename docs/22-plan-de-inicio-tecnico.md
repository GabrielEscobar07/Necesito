# 22 — Plan de inicio técnico

## Objetivo

Definir el orden de trabajo para comenzar a programar después de revisar esta documentación. Las versiones exactas se comprobarán antes de crear los proyectos.

## Hito T0 — Preparar el equipo

1. Verificar Git y acceso a GitHub.
2. Verificar Visual Studio Code.
3. Verificar una versión estable y compatible de Node.js.
4. Elegir el gestor de paquetes del frontend.
5. Verificar el .NET SDK compatible con el backend.
6. Verificar Docker Desktop y su motor.
7. Clonar `GabrielEscobar07/Necesito`.
8. Abrir la raíz del repositorio, no carpetas aisladas.

**Resultado:** entorno listo y documentado.

## Hito T1 — Inicializar el monorepositorio

1. Crear Next.js con React, TypeScript y Tailwind en `apps/web`.
2. Crear ASP.NET Core Web API en `apps/api`.
3. Mantener ambos proyectos ejecutables de manera independiente.
4. Añadir archivos de variables de entorno de ejemplo sin secretos.
5. Configurar comprobaciones de formato y análisis estático.
6. Actualizar instrucciones del README.

**Resultado:** web y API muestran una respuesta mínima local.

## Hito T2 — Base de datos local

1. Crear MySQL con Docker Compose.
2. Crear una base exclusiva, provisionalmente `necesito_dev`.
3. Definir volumen persistente de desarrollo.
4. Configurar cadena de conexión mediante variables de entorno.
5. Añadir comprobación de salud.
6. Configurar Entity Framework Core con un proveedor compatible para MySQL.
7. Crear y aplicar la primera migración.

**Resultado:** la API se conecta a una base reproducible e independiente.

## Hito T3 — Esqueleto modular

Crear módulos iniciales sin implementar todo el negocio:

- Identity.
- Profiles.
- Catalog.
- Verification.
- Requests.
- Quotes.
- Engagements.
- Reviews.
- TrustAndSafety.
- Notifications.

**Resultado:** límites claros dentro del monolito y dependencias controladas.

## Hito T4 — Primer corte vertical

Implementar un recorrido pequeño de extremo a extremo:

1. Crear una categoría de prueba.
2. Crear una solicitud mínima.
3. Guardarla en MySQL.
4. Consultarla desde la API.
5. Mostrarla en la web.

Todavía sin autenticación completa ni diseño final.

**Resultado:** se comprueba web → API → base de datos.

## Hito T5 — Primer flujo real

Implementar progresivamente:

1. Identidad y roles.
2. Perfil proveedor.
3. Solicitud.
4. Cotización.
5. Aceptación y contratación.
6. Estados.
7. Calificación.
8. Administración mínima.

## Reglas de ejecución

- Trabajar una tarea pequeña por rama.
- Abrir Pull Request antes de integrar cambios importantes.
- No incluir secretos ni contraseñas.
- No compartir la base ni las credenciales con el sistema administrativo.
- No agregar Redis, SignalR o tecnología geográfica avanzada hasta que una necesidad concreta lo justifique.
- Mantener el proyecto ejecutable al final de cada hito.
- Actualizar documentación junto con cualquier cambio de reglas.
- Crear pruebas para reglas críticas antes de expandir módulos.

## Definición de terminado del arranque

La etapa de arranque termina cuando otra persona puede clonar el repositorio, ejecutar las instrucciones, levantar web, API y MySQL, aplicar migraciones y comprobar el primer recorrido vertical sin conocimiento oculto.
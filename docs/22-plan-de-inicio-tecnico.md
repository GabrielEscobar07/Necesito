# 22 — Plan de inicio técnico

## Objetivo

Definir el orden de trabajo para comenzar a programar después de revisar esta documentación. No contiene todavía comandos ni versiones cerradas porque deberán verificarse al iniciar la etapa técnica.

## Hito T0 — Preparar el equipo

1. Verificar Git y acceso a GitHub.
2. Instalar o actualizar Visual Studio Code.
3. Verificar una versión estable y compatible de Node.js.
4. Elegir el gestor de paquetes del frontend.
5. Instalar el .NET SDK compatible con el backend.
6. Instalar Docker Desktop y comprobar virtualización.
7. Clonar `GabrielEscobar07/Necesito`.
8. Abrir la raíz del repositorio, no carpetas aisladas.

**Resultado:** entorno listo y documentado.

## Hito T1 — Inicializar el monorepositorio

1. Crear Next.js con React, TypeScript y Tailwind en `apps/web`.
2. Crear ASP.NET Core Web API en `apps/api`.
3. Mantener ambos proyectos ejecutables de manera independiente.
4. Añadir archivos de variables de entorno de ejemplo sin secretos.
5. Actualizar instrucciones del README.

**Resultado:** web y API muestran una respuesta mínima local.

## Hito T2 — Base de datos local

1. Crear PostgreSQL con Docker Compose.
2. Definir volumen persistente de desarrollo.
3. Configurar cadena de conexión mediante variables de entorno.
4. Añadir comprobación de salud.
5. Elegir y configurar la estrategia de acceso a datos y migraciones en .NET.

**Resultado:** la API se conecta a una base reproducible.

## Hito T3 — Esqueleto modular

Crear módulos iniciales sin implementar todo el negocio:

- Identity.
- Profiles.
- Catalog.
- Verification.
- Requests.
- Quotes.
- Engagements o Contracts.
- Reviews.
- TrustAndSafety.
- Notifications.

**Resultado:** límites claros dentro del monolito y dependencias controladas.

## Hito T4 — Primer corte vertical

Implementar un recorrido pequeño de extremo a extremo:

1. Crear una categoría de prueba.
2. Crear una solicitud mínima.
3. Guardarla en PostgreSQL.
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
- No agregar Redis, SignalR o PostGIS hasta que una necesidad concreta lo justifique.
- Mantener el proyecto ejecutable al final de cada hito.
- Actualizar documentación junto con cualquier cambio de reglas.
- Crear pruebas para reglas críticas antes de expandir módulos.

## Definición de terminado del arranque

La etapa de arranque termina cuando otra persona puede clonar el repositorio, ejecutar las instrucciones, levantar web, API y PostgreSQL, aplicar migraciones y comprobar el primer recorrido vertical sin conocimiento oculto.
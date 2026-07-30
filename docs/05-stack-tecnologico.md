# 05 — Stack tecnológico

## Objetivo

Seleccionar tecnologías maduras, mantenibles y adecuadas para una plataforma web con crecimiento gradual.

## Aplicación web/PWA

- **Next.js:** framework principal.
- **React:** interfaz basada en componentes.
- **TypeScript:** tipado estático y mejor mantenimiento.
- **Tailwind CSS:** sistema de estilos utilitario.

La aplicación incluirá las experiencias de cliente, proveedor y administración dentro del mismo frontend, separadas mediante rutas, permisos y componentes.

## Backend/API

- **ASP.NET Core con C#:** API, autenticación, autorización y reglas de negocio.
- Diseño inicial como **monolito modular**.
- Los módulos se comunicarán dentro del mismo proceso al inicio.
- **OpenAPI:** documentación y prueba de contratos HTTP.

## Persistencia

- **MySQL:** base de datos relacional principal.
- **Entity Framework Core:** acceso a datos y migraciones desde .NET.
- **Proveedor compatible para MySQL:** se seleccionará al fijar la versión de .NET y MySQL.

El proyecto tendrá una base exclusiva. No reutilizará las tablas ni las credenciales del Sistema Administrativo La Vieja TATTOO.

La ubicación inicial se almacenará mediante ciudad, zona, referencias protegidas y coordenadas opcionales. Las búsquedas geográficas avanzadas se evaluarán posteriormente usando capacidades espaciales de MySQL o un servicio especializado.

## Capacidades futuras

- **SignalR:** notificaciones o comunicación en tiempo real.
- **Redis:** caché, rate limiting distribuido u otras necesidades comprobadas.
- **React Native con Expo:** aplicación móvil futura reutilizando contratos y conocimientos del frontend.

SignalR y Redis están previstos, pero no son requisitos del primer arranque técnico.

## Infraestructura

- **Docker:** entornos reproducibles.
- **Docker Compose:** ejecución local de servicios relacionados.
- **GitHub:** repositorio, revisión de cambios y automatización futura.
- **Visual Studio Code:** editor principal del proyecto.

## Calidad profesional prevista

- ESLint y formateo automático para el frontend.
- Analizadores y formato de C# para el backend.
- Pruebas unitarias y de integración.
- GitHub Actions para validación automática.
- Variables de entorno para configuración y secretos.
- Diseño de interfaz mobile-first, accesible y basado en componentes reutilizables.

## Principio de adopción

Una herramienta futura solamente se incorporará cuando resuelva una necesidad demostrable. Evitaremos agregar infraestructura únicamente porque podría ser útil algún día.

## Versiones

Las versiones exactas se fijarán cuando se inicialicen los proyectos. Se elegirán versiones estables, compatibles entre sí y con soporte vigente en ese momento.
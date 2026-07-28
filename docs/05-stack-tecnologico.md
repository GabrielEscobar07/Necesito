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

## Persistencia

- **PostgreSQL:** base de datos relacional principal.
- **PostGIS:** extensión futura para consultas geográficas y zonas de cobertura.

PostGIS no debe introducirse hasta que exista un caso geográfico claramente definido.

## Capacidades futuras

- **SignalR:** notificaciones o comunicación en tiempo real.
- **Redis:** caché, rate limiting distribuido u otras necesidades comprobadas.
- **React Native con Expo:** aplicación móvil futura reutilizando contratos y conocimientos del frontend.

SignalR y Redis están previstos, pero no son requisitos del primer arranque técnico.

## Infraestructura

- **Docker:** entornos reproducibles.
- **Docker Compose:** ejecución local de servicios relacionados.
- **GitHub:** repositorio, revisión de cambios y automatización futura.

## Principio de adopción

Una herramienta futura solamente se incorporará cuando resuelva una necesidad demostrable. Evitaremos agregar infraestructura únicamente porque podría ser útil algún día.

## Versiones

Las versiones exactas se fijarán cuando se inicialicen los proyectos. Se elegirán versiones estables y con soporte vigente en ese momento.

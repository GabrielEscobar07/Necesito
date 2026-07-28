# Necesito

> **Nombre provisional del proyecto.** Plataforma web/PWA para conectar personas que necesitan un servicio con trabajadores y proveedores verificados en Bolivia.

## Estado del proyecto

**Fase 0 — Definición, documentación y preparación del repositorio.**

El proyecto todavía no contiene código de aplicación. La prioridad actual es definir el producto, su alcance inicial, sus reglas y la arquitectura que guiará el desarrollo.

## Visión

Necesito busca facilitar la contratación de servicios confiables. Un cliente podrá publicar una necesidad, recibir cotizaciones de profesionales compatibles, comparar propuestas y contratar una opción dentro de la misma plataforma.

La primera operación se plantea para Santa Cruz de la Sierra, con posibilidad de expansión posterior al resto de Bolivia.

## Alcance inicial

La primera versión se concentrará en servicios a domicilio de:

- Electricidad.
- Plomería.
- Aire acondicionado y refrigeración.

La plataforma estará preparada para incorporar posteriormente limpieza, jardinería, carpintería, construcción, reparación de equipos, servicios empresariales, proveedores y otras categorías.

## Tipos de usuario

- **Cliente:** publica solicitudes, recibe cotizaciones, contrata y califica.
- **Trabajador o proveedor:** crea un perfil profesional, completa su verificación, recibe oportunidades y envía cotizaciones.
- **Administrador:** verifica perfiles, administra categorías y atiende reportes o incidencias.

Una misma cuenta podrá estar preparada para actuar como cliente y proveedor mediante roles diferenciados.

## Flujo principal

1. El cliente describe el servicio que necesita.
2. La plataforma identifica categoría y ubicación.
3. Los proveedores compatibles reciben la oportunidad.
4. Los proveedores interesados envían una cotización.
5. El cliente compara propuestas y selecciona una.
6. El servicio se realiza y posteriormente puede calificarse.

## Stack tecnológico previsto

| Área | Tecnología |
|---|---|
| Web/PWA | Next.js, React y TypeScript |
| Estilos | Tailwind CSS |
| Backend/API | ASP.NET Core con C# |
| Base de datos | PostgreSQL |
| Geolocalización futura | PostGIS |
| Tiempo real futuro | SignalR |
| Caché futura | Redis |
| Contenedores | Docker y Docker Compose |
| Aplicación móvil futura | React Native con Expo |

## Arquitectura inicial

Se utilizará un **monolito modular** alojado en un monorepositorio. Existirá una sola aplicación web/PWA con experiencias diferenciadas por rol, una API principal y una base de datos PostgreSQL.

```text
Necesito/
├── apps/
│   ├── web/                 # Next.js: cliente, proveedor y administración
│   └── api/                 # ASP.NET Core
├── docs/                    # Producto, alcance, arquitectura y decisiones
├── infrastructure/          # Docker, base de datos y despliegue
├── scripts/                 # Automatizaciones de desarrollo y mantenimiento
├── tests/                   # Pruebas generales e integración
├── .github/                 # Plantillas y automatizaciones de GitHub
├── .editorconfig
├── .gitattributes
├── .gitignore
├── CONTRIBUTING.md
├── SECURITY.md
└── README.md
```

## Documentación

El índice completo está disponible en [`docs/README.md`](docs/README.md).

Documentos principales:

- [Visión del proyecto](docs/01-vision-del-proyecto.md)
- [Alcance inicial](docs/02-alcance-inicial.md)
- [Usuarios y roles](docs/03-usuarios-y-roles.md)
- [Flujo del servicio](docs/04-flujo-del-servicio.md)
- [Stack tecnológico](docs/05-stack-tecnologico.md)
- [Arquitectura inicial](docs/06-arquitectura-inicial.md)
- [Roadmap](docs/07-roadmap.md)
- [Glosario](docs/08-glosario.md)
- [Plan de la etapa 0](docs/09-plan-etapa-0.md)
- [Registro de decisiones técnicas](docs/adr/README.md)

## Convenciones iniciales

- Rama estable: `main`.
- Nuevos cambios: ramas cortas y descriptivas.
- Commits: formato Conventional Commits.
- Secretos y credenciales: nunca se almacenan en Git.
- Cada decisión estructural importante debe registrarse mediante un ADR.

Consulta [`CONTRIBUTING.md`](CONTRIBUTING.md) antes de realizar cambios.

## Seguridad

Las vulnerabilidades no deben publicarse como incidencias abiertas. Consulta [`SECURITY.md`](SECURITY.md).

## Licencia

Actualmente el proyecto no tiene una licencia de código abierto. El contenido se mantiene bajo control de su propietario hasta que se defina una licencia formal.

## Responsable inicial

Proyecto iniciado por [GabrielEscobar07](https://github.com/GabrielEscobar07).

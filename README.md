# Necesito

> **Nombre provisional del proyecto.** Plataforma web/PWA para conectar personas que necesitan un servicio con trabajadores y proveedores verificados en Bolivia.

## Estado del proyecto

**Fase 0 — Base documental completada; preparación para iniciar la arquitectura técnica.**

El repositorio todavía no contiene código de aplicación. Ya se documentaron alcance, requisitos, reglas, historias de usuario, dominio, estados, seguridad, navegación, backlog y criterios de aceptación. Las hipótesis marcadas como provisionales deberán validarse durante el proyecto.

## Visión

Necesito busca facilitar la contratación de servicios confiables. Un cliente podrá publicar una necesidad, recibir cotizaciones de profesionales compatibles, comparar propuestas y contratar una opción dentro de la misma plataforma.

La primera operación se plantea para Santa Cruz de la Sierra, con posibilidad de expansión posterior al resto de Bolivia.

## Alcance inicial

La primera versión se concentrará en servicios a domicilio de:

- Electricidad.
- Plomería.
- Aire acondicionado y refrigeración.

Después podrá incorporar limpieza, jardinería, carpintería, construcción, reparación de equipos, servicios empresariales, proveedores y repuestos.

## Producto unificado

Existirá una sola aplicación web/PWA con experiencias diferenciadas:

- **Cliente:** publica solicitudes, recibe cotizaciones, contrata y califica.
- **Proveedor:** crea su perfil, completa verificación, recibe oportunidades y cotiza.
- **Administrador:** verifica perfiles, administra catálogos y atiende incidencias.

Una misma cuenta podrá tener perfiles de cliente y proveedor y cambiar de modo sin duplicar su identidad.

## Flujo principal

1. El cliente describe el servicio que necesita.
2. La plataforma identifica categoría y zona.
3. Proveedores compatibles reciben la oportunidad.
4. Los interesados envían cotizaciones.
5. El cliente compara y selecciona una propuesta.
6. Se crea una contratación.
7. El servicio se realiza, finaliza y puede calificarse.

## Stack previsto

| Área | Tecnología |
|---|---|
| Web/PWA | Next.js, React y TypeScript |
| Estilos | Tailwind CSS |
| Backend/API | ASP.NET Core con C# |
| Base de datos | PostgreSQL |
| Ubicación futura | PostGIS |
| Tiempo real futuro | SignalR |
| Caché futura | Redis |
| Contenedores | Docker y Docker Compose |
| Aplicación móvil futura | React Native con Expo |

## Arquitectura

Se utilizará un **monolito modular** en un monorepositorio:

```text
Necesito/
├── apps/
│   ├── web/                 # Next.js: cliente, proveedor y administración
│   └── api/                 # ASP.NET Core
├── docs/                    # Producto, arquitectura y planificación
├── infrastructure/          # Docker, PostgreSQL y despliegue
├── scripts/                 # Automatizaciones
├── tests/                   # Pruebas generales e integración
├── .github/                 # Plantillas y automatizaciones de GitHub
├── CONTRIBUTING.md
├── SECURITY.md
└── README.md
```

## Documentación

El índice completo está en [`docs/README.md`](docs/README.md).

Documentos recomendados para comprender el proyecto:

1. [Visión](docs/01-vision-del-proyecto.md) y [alcance](docs/02-alcance-inicial.md).
2. [Requisitos](docs/10-requisitos-del-mvp.md) y [reglas de negocio](docs/11-reglas-de-negocio.md).
3. [Historias de usuario](docs/12-historias-de-usuario-mvp.md).
4. [Modelo de dominio](docs/13-modelo-de-dominio-inicial.md) y [estados](docs/14-estados-y-transiciones.md).
5. [Seguridad y privacidad](docs/16-seguridad-y-privacidad.md).
6. [Backlog](docs/20-backlog-inicial.md) y [plan de inicio técnico](docs/22-plan-de-inicio-tecnico.md).
7. [Registro de decisiones](docs/adr/README.md).

## Convenciones

- Rama estable: `main`.
- Cambios en ramas cortas y descriptivas.
- Commits con Conventional Commits.
- Secretos y credenciales nunca se almacenan en Git.
- Decisiones estructurales importantes se registran mediante ADR.
- Las reglas del dominio deben validarse también en la API.

Consulta [`CONTRIBUTING.md`](CONTRIBUTING.md) antes de realizar cambios.

## Seguridad

Las vulnerabilidades no deben publicarse como incidencias abiertas. Consulta [`SECURITY.md`](SECURITY.md).

## Licencia

Actualmente el proyecto no tiene licencia de código abierto. El contenido permanece bajo control de su propietario hasta definir una licencia formal.

## Responsable inicial

Proyecto iniciado por [GabrielEscobar07](https://github.com/GabrielEscobar07).
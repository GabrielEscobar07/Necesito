# 09 — Plan de la etapa 0

## Objetivo

Terminar la preparación conceptual y técnica necesaria antes de implementar funcionalidades.

## Completado

- [x] Crear repositorio en GitHub.
- [x] Definir nombre provisional.
- [x] Crear estructura inicial del monorepositorio.
- [x] Crear README principal.
- [x] Documentar visión y alcance.
- [x] Documentar usuarios y flujo principal.
- [x] Registrar stack y arquitectura inicial.
- [x] Establecer convenciones de contribución y seguridad.

## Pendiente antes del código

- [ ] Validar el problema mediante entrevistas cuando exista disponibilidad.
- [ ] Definir historias de usuario del MVP.
- [ ] Definir reglas de negocio y estados definitivos.
- [ ] Diseñar el modelo conceptual de datos.
- [ ] Definir criterios de verificación de proveedores.
- [ ] Definir tratamiento de ubicación y privacidad.
- [ ] Definir política inicial de cancelaciones y reportes.
- [ ] Diseñar el mapa de navegación.
- [ ] Confirmar requisitos del entorno local.

## Primer hito técnico posterior

Cuando la etapa documental esté suficientemente clara:

1. Instalar y verificar Git, Node.js, un gestor de paquetes, .NET SDK y Docker Desktop.
2. Clonar el repositorio.
3. Inicializar `apps/web` con Next.js, React y TypeScript.
4. Inicializar `apps/api` con ASP.NET Core.
5. Configurar PostgreSQL en Docker Compose.
6. Comprobar comunicación local entre web, API y base de datos.

No se iniciará este hito hasta revisar las reglas básicas del dominio.

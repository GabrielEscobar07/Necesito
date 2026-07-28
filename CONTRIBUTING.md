# Guía de contribución

Este documento define las reglas iniciales para mantener el repositorio ordenado y trazable.

## Antes de comenzar

1. Revisa el `README.md` y la documentación dentro de `/docs`.
2. Confirma que el cambio corresponde al alcance actual.
3. Evita introducir nuevas tecnologías sin registrar primero la decisión.
4. Nunca incluyas contraseñas, tokens, archivos `.env` ni datos personales reales.

## Estrategia de ramas

La rama `main` representa el estado estable del proyecto. Todo cambio relevante debe realizarse en una rama separada.

Formato recomendado:

```text
feature/nombre-de-funcionalidad
fix/nombre-del-problema
chore/tarea-tecnica
docs/tema-documentado
refactor/area-refactorizada
```

Ejemplos:

```text
feature/registro-clientes
docs/modelo-cotizaciones
chore/configuracion-docker
```

## Commits

Se utilizará Conventional Commits:

```text
feat: agrega registro inicial de clientes
fix: corrige validación de teléfono
docs: documenta flujo de cotización
chore: configura herramientas del repositorio
refactor: reorganiza módulo de solicitudes
test: agrega pruebas de creación de solicitud
```

Los mensajes deben describir un cambio concreto y estar escritos en presente.

## Pull Requests

Cada Pull Request debe:

- Tener un título claro.
- Explicar qué cambia y por qué.
- Indicar cómo fue validado.
- Mantenerse enfocado en una sola tarea.
- Actualizar la documentación cuando corresponda.

## Estilo de desarrollo

- TypeScript en modo estricto para la aplicación web.
- Análisis de nulabilidad habilitado en C#.
- Nombres de código en inglés y documentación funcional en español.
- Dependencias externas justificadas y actualizadas.
- Módulos con responsabilidades claras.
- Pruebas para reglas de negocio críticas.

## Decisiones de arquitectura

Una decisión estructural debe documentarse como ADR en `docs/adr/` antes o junto con su implementación.

## Revisión de seguridad

Antes de confirmar un cambio:

- Revisa que no contenga secretos.
- Valida entradas del usuario.
- Evita registrar información sensible en logs.
- Comprueba permisos y autorización por rol.

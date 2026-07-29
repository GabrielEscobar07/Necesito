# 19 — Criterios de aceptación del MVP

## Propósito

Definir cuándo la primera versión puede considerarse funcional para una prueba controlada en Santa Cruz de la Sierra.

## Recorrido principal obligatorio

El MVP es aceptable cuando puede demostrarse de principio a fin que:

1. Una persona crea una cuenta de cliente.
2. Publica una solicitud válida de electricidad, plomería o aire acondicionado/refrigeración.
3. Un proveedor con categoría y zona compatibles puede verla.
4. El proveedor envía una cotización válida.
5. El cliente recibe y compara la propuesta.
6. El cliente acepta una cotización.
7. El sistema crea una contratación y bloquea la aceptación de otras propuestas.
8. Las partes actualizan los estados permitidos.
9. La contratación finaliza.
10. El cliente registra una calificación.

## Administración obligatoria

Debe ser posible:

- Revisar y decidir una verificación de proveedor.
- Activar o desactivar categorías y zonas.
- Consultar el historial de una solicitud y contratación.
- Recibir y resolver un reporte básico.
- Suspender una cuenta con motivo y auditoría.

## Seguridad mínima

- Un usuario no puede consultar o modificar recursos privados de otro usuario sin permiso.
- Un proveedor no puede cotizar cuando no está habilitado.
- Un cliente no puede aceptar dos cotizaciones para la misma solicitud.
- Una calificación no puede crearse antes de finalizar.
- Los documentos de verificación no se exponen públicamente.
- Los secretos no están versionados.
- Las acciones administrativas sensibles quedan registradas.

## Calidad mínima

- La interfaz principal funciona en ancho móvil y escritorio.
- Formularios muestran errores comprensibles.
- Los estados visibles coinciden con la API.
- El proyecto puede levantarse siguiendo instrucciones documentadas.
- Las migraciones de base de datos pueden ejecutarse desde cero.
- Existen pruebas automatizadas para reglas críticas.
- Los errores importantes se registran sin revelar contraseñas, tokens o documentos.

## Datos de prueba

La demostración debe incluir:

- Un cliente.
- Dos proveedores, al menos uno verificado.
- Las tres categorías iniciales.
- Zonas iniciales de Santa Cruz definidas para prueba.
- Una solicitud con varias cotizaciones.
- Una contratación finalizada y calificada.
- Una verificación observada o rechazada.
- Un reporte administrativo.

## Exclusiones aceptadas

El MVP puede considerarse válido sin pagos internos, rastreo, chat avanzado, Redis, SignalR, PostGIS, aplicación móvil nativa ni operación nacional.

## Condición de lanzamiento controlado

Cumplir los criterios técnicos no autoriza por sí solo un lanzamiento público. Antes se deben validar términos, privacidad, proceso de soporte, criterios de verificación y capacidad administrativa.
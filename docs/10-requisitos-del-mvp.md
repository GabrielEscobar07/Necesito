# 10 — Requisitos del MVP

## Propósito

Definir qué debe hacer la primera versión funcional de Necesito y qué condiciones mínimas deberá cumplir. Estos requisitos son una base de trabajo y podrán ajustarse después de entrevistar a clientes y proveedores reales.

## Requisitos funcionales

### Cuenta y acceso

- **RF-001:** permitir registro mediante nombre, teléfono o correo y contraseña.
- **RF-002:** permitir inicio y cierre de sesión.
- **RF-003:** permitir recuperación segura de acceso.
- **RF-004:** permitir que una cuenta tenga rol de cliente, proveedor o ambos.
- **RF-005:** impedir el acceso a funciones administrativas sin autorización.

### Perfil de cliente

- **RF-010:** mantener datos básicos de contacto.
- **RF-011:** permitir registrar ubicaciones de servicio.
- **RF-012:** mostrar solicitudes, cotizaciones, contrataciones y calificaciones propias.

### Perfil de proveedor

- **RF-020:** permitir crear un perfil profesional.
- **RF-021:** permitir seleccionar categorías, especialidades y zonas de atención.
- **RF-022:** permitir cargar información y documentos para verificación.
- **RF-023:** mostrar claramente el estado de verificación.
- **RF-024:** permitir activar o pausar la disponibilidad para recibir oportunidades.

### Solicitudes de servicio

- **RF-030:** permitir al cliente crear una solicitud con categoría, descripción, ubicación y urgencia.
- **RF-031:** permitir adjuntar fotografías de manera opcional.
- **RF-032:** permitir guardar una solicitud como borrador antes de publicarla.
- **RF-033:** permitir consultar el historial y estado de cada solicitud.
- **RF-034:** distribuir la oportunidad únicamente a proveedores compatibles y habilitados.
- **RF-035:** permitir cancelar una solicitud según sus reglas y estado.

### Cotizaciones

- **RF-040:** permitir al proveedor enviar precio, descripción, disponibilidad y vigencia.
- **RF-041:** impedir más de una cotización activa del mismo proveedor para la misma solicitud.
- **RF-042:** permitir editar o retirar una cotización mientras no haya sido aceptada.
- **RF-043:** permitir al cliente comparar cotizaciones recibidas.
- **RF-044:** permitir aceptar una sola cotización por solicitud.

### Contratación y servicio

- **RF-050:** crear una contratación al aceptar una cotización.
- **RF-051:** registrar los cambios de estado de la contratación.
- **RF-052:** permitir que proveedor y cliente confirmen hitos del servicio.
- **RF-053:** permitir reportar un inconveniente.
- **RF-054:** permitir finalizar el servicio sin procesar pagos dentro de la plataforma durante el MVP.

### Reputación

- **RF-060:** permitir al cliente calificar un servicio finalizado.
- **RF-061:** permitir una sola calificación por contratación.
- **RF-062:** mostrar reputación agregada sin revelar datos privados.
- **RF-063:** permitir reportar contenido o conducta inapropiada.

### Administración

- **RF-070:** permitir revisar y resolver verificaciones.
- **RF-071:** gestionar categorías, especialidades y zonas habilitadas.
- **RF-072:** consultar usuarios, solicitudes, cotizaciones y contrataciones.
- **RF-073:** registrar suspensiones y motivos.
- **RF-074:** revisar reportes e incidencias.
- **RF-075:** conservar trazabilidad de acciones administrativas importantes.

## Requisitos no funcionales

- **RNF-001 — Seguridad:** contraseñas almacenadas mediante algoritmos de hash adecuados; nunca en texto plano.
- **RNF-002 — Privacidad:** acceso a datos personales limitado por rol y necesidad.
- **RNF-003 — Rendimiento:** las operaciones habituales deberán responder de forma razonable en conexiones móviles.
- **RNF-004 — Adaptabilidad:** interfaz mobile-first y utilizable en computadora, tableta y teléfono.
- **RNF-005 — Accesibilidad:** formularios con etiquetas, navegación por teclado y mensajes comprensibles.
- **RNF-006 — Auditabilidad:** cambios sensibles con usuario, fecha y motivo.
- **RNF-007 — Mantenibilidad:** separación por módulos dentro del monolito.
- **RNF-008 — Portabilidad:** ejecución local reproducible mediante Docker cuando se habilite la etapa técnica.
- **RNF-009 — Disponibilidad:** manejo claro de errores y posibilidad de reintentar operaciones seguras.
- **RNF-010 — Observabilidad:** registro de errores y eventos importantes sin exponer secretos.
- **RNF-011 — Internacionalización futura:** textos preparados para no quedar dispersos en el código.
- **RNF-012 — Integridad:** las transiciones inválidas de estados deben rechazarse también en la API.

## Criterio de control

Un requisito nuevo entra en el MVP solamente cuando es indispensable para completar, proteger o administrar el flujo de solicitud, cotización, contratación y calificación.
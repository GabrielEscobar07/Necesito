# 12 — Historias de usuario del MVP

## Convención

- **P0:** indispensable para probar el flujo principal.
- **P1:** importante para operar de forma segura.
- **P2:** mejora posterior al primer recorrido completo.

## Visitante y cuenta

### HU-001 — Conocer la plataforma — P0

Como visitante, quiero comprender cómo funciona Necesito para decidir si publicar una necesidad u ofrecer mis servicios.

**Aceptación:** la página inicial diferencia claramente ambas acciones y muestra las categorías disponibles.

### HU-002 — Crear una cuenta — P0

Como persona, quiero registrarme para utilizar funciones privadas.

**Aceptación:** los datos obligatorios se validan, la contraseña se protege y no se crean cuentas duplicadas con el mismo identificador confirmado.

### HU-003 — Cambiar de modo — P1

Como usuario con ambos perfiles, quiero cambiar entre modo cliente y modo proveedor sin crear otra cuenta.

**Aceptación:** cada modo muestra únicamente su navegación y permisos correspondientes.

## Cliente

### HU-010 — Publicar una solicitud — P0

Como cliente, quiero describir el servicio que necesito para recibir cotizaciones compatibles.

**Aceptación:** se exige categoría, descripción y ubicación; las fotografías son opcionales; el cliente confirma antes de publicar.

### HU-011 — Revisar el estado — P0

Como cliente, quiero ver el estado de mis solicitudes para saber qué está ocurriendo.

**Aceptación:** cada solicitud muestra estado actual, fechas relevantes y acciones permitidas.

### HU-012 — Comparar cotizaciones — P0

Como cliente, quiero comparar precio, alcance, disponibilidad y reputación para elegir una propuesta.

**Aceptación:** solo se muestran cotizaciones activas de la solicitud y sus datos comparables.

### HU-013 — Aceptar una cotización — P0

Como cliente, quiero seleccionar una propuesta para contratar al proveedor.

**Aceptación:** se solicita confirmación, se crea una contratación y no se puede aceptar otra cotización para la misma solicitud.

### HU-014 — Cancelar una solicitud — P1

Como cliente, quiero cancelar una solicitud que ya no necesito.

**Aceptación:** la acción depende del estado, exige motivo y no elimina el historial.

### HU-015 — Calificar — P1

Como cliente, quiero calificar un servicio finalizado para ayudar a futuros usuarios.

**Aceptación:** solo se habilita una vez por contratación finalizada y el comentario pasa por reglas de contenido.

## Proveedor

### HU-020 — Crear perfil profesional — P0

Como proveedor, quiero indicar mis especialidades y zonas para recibir oportunidades adecuadas.

**Aceptación:** puede elegir categorías habilitadas, describir experiencia y seleccionar zonas de atención.

### HU-021 — Solicitar verificación — P0

Como proveedor, quiero enviar mis datos para demostrar que mi perfil fue revisado.

**Aceptación:** el sistema informa requisitos, permite enviar la solicitud y muestra su estado.

### HU-022 — Ver oportunidades — P0

Como proveedor habilitado, quiero consultar solicitudes compatibles para decidir cuáles cotizar.

**Aceptación:** no se revela dirección exacta antes de la contratación y solo aparecen oportunidades permitidas por categoría y zona.

### HU-023 — Enviar una cotización — P0

Como proveedor, quiero proponer precio, alcance y disponibilidad.

**Aceptación:** todos los campos obligatorios se validan y no puede existir más de una cotización activa propia por solicitud.

### HU-024 — Gestionar una cotización — P1

Como proveedor, quiero editar o retirar una propuesta que todavía no fue aceptada.

**Aceptación:** después de la aceptación no existe edición unilateral.

### HU-025 — Gestionar el trabajo adjudicado — P0

Como proveedor contratado, quiero consultar datos de coordinación y actualizar los hitos permitidos.

**Aceptación:** solo las partes y administradores autorizados acceden a la contratación.

### HU-026 — Pausar disponibilidad — P1

Como proveedor, quiero dejar de recibir oportunidades temporalmente.

**Aceptación:** pausar no borra perfil, cotizaciones ni trabajos existentes.

## Administración

### HU-030 — Revisar una verificación — P0

Como administrador, quiero aprobar, observar o rechazar una solicitud de verificación.

**Aceptación:** se registra decisión, responsable, fecha y motivo; el proveedor recibe el resultado.

### HU-031 — Gestionar categorías y zonas — P1

Como administrador, quiero habilitar o deshabilitar categorías y zonas sin borrar el historial.

**Aceptación:** los cambios futuros no alteran registros históricos.

### HU-032 — Atender reportes — P1

Como administrador, quiero revisar incidencias para tomar medidas justificadas.

**Aceptación:** cada reporte conserva estado, evidencia, notas y resolución.

### HU-033 — Suspender una cuenta — P1

Como administrador, quiero limitar temporalmente una cuenta riesgosa.

**Aceptación:** se exige motivo, se registra auditoría y la persona no puede iniciar nuevas operaciones restringidas.

## Historias posteriores al MVP

Pagos internos, chat en tiempo real, rastreo, suscripciones, promoción pagada, aplicación nativa, venta de repuestos y asignación automática quedan fuera de estas historias iniciales.
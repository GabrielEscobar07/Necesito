# 13 — Modelo de dominio inicial

## Objetivo

Describir los conceptos centrales antes de diseñar tablas o clases. Este documento no es todavía un esquema definitivo de PostgreSQL.

## Módulos del monolito

1. **Identidad y acceso:** cuentas, autenticación, roles y permisos.
2. **Perfiles:** información de clientes y proveedores.
3. **Catálogo:** categorías, especialidades y zonas de operación.
4. **Verificación:** solicitudes, documentos y decisiones.
5. **Solicitudes:** necesidades publicadas por clientes.
6. **Cotizaciones:** propuestas realizadas por proveedores.
7. **Contrataciones:** acuerdo resultante de una cotización aceptada.
8. **Reputación:** calificaciones y comentarios.
9. **Confianza y soporte:** reportes, suspensiones y moderación.
10. **Notificaciones:** avisos generados por eventos del sistema.
11. **Auditoría:** trazabilidad de acciones sensibles.

## Entidades principales

### Usuario

Representa la cuenta de acceso.

Datos conceptuales: identificador, nombre, teléfono, correo, credenciales, estado, fecha de registro y última actividad. No debe contener directamente toda la información profesional.

### Rol y asignación de rol

Define capacidades de cliente, proveedor y administrador. Un usuario puede tener varios roles, excepto permisos administrativos que requieren asignación controlada.

### Perfil de cliente

Extiende a Usuario con preferencias o información necesaria para solicitar servicios.

### Perfil de proveedor

Contiene nombre profesional, descripción, experiencia declarada, disponibilidad, estado público, reputación calculada y estado de verificación.

### Categoría de servicio

Agrupa servicios como electricidad, plomería y aire acondicionado/refrigeración. Puede tener especialidades y estar activa o inactiva.

### Zona de servicio

Representa áreas habilitadas inicialmente dentro de Santa Cruz de la Sierra. Su diseño deberá permitir futuras ciudades y departamentos.

### Especialidad del proveedor

Relaciona proveedor con categoría o especialidad y permite registrar estado, experiencia declarada y disponibilidad.

### Solicitud de verificación

Registra el proceso de revisión de un proveedor: fecha, estado, observaciones y resolución administrativa.

### Documento de verificación

Referencia un archivo protegido, su tipo, estado y vigencia cuando corresponda. No debe exponerse públicamente.

### Solicitud de servicio

Necesidad creada por un cliente. Incluye categoría, título, descripción, zona, referencia de ubicación, urgencia, estado y fechas.

### Adjunto de solicitud

Fotografía u otro archivo permitido asociado a una solicitud, con metadatos y controles de acceso.

### Cotización

Propuesta de un proveedor para una solicitud. Incluye monto, moneda, descripción del alcance, disponibilidad, vigencia y estado.

### Contratación

Se crea al aceptar una cotización. Conserva una copia lógica de los términos aceptados, partes, estado y fechas relevantes.

### Historial de estado

Registra cambios de estado de solicitudes, cotizaciones, verificaciones, contrataciones y reportes. Incluye actor, fecha, origen y motivo.

### Calificación

Evaluación asociada a una contratación finalizada. Contiene puntuación, comentario, estado de moderación y autor.

### Reporte o incidencia

Permite denunciar conducta, contenido o problemas relacionados con usuario, solicitud o contratación.

### Notificación

Aviso dirigido a un usuario por un evento. Registra tipo, contenido, fecha, canal y estado de lectura o envío.

### Evento de auditoría

Registra acciones administrativas o de seguridad que requieren trazabilidad.

## Relaciones clave

```text
Usuario 1 ── 0..1 PerfilCliente
Usuario 1 ── 0..1 PerfilProveedor
Usuario N ── N Rol
PerfilProveedor N ── N Categoría
Cliente 1 ── N Solicitud
Solicitud 1 ── N Cotización
Proveedor 1 ── N Cotización
Solicitud 1 ── 0..1 Contratación
Cotización 1 ── 0..1 Contratación
Contratación 1 ── 0..1 Calificación
Proveedor 1 ── N SolicitudVerificación
```

## Principios de modelado

- Usar identificadores estables que no expongan secuencias internas públicamente.
- Conservar fechas en UTC y presentar hora local en la interfaz.
- Preferir estados y baja lógica para registros con valor histórico.
- No almacenar archivos grandes directamente en tablas sin una decisión técnica explícita.
- Separar datos públicos, privados y administrativos.
- Evitar que la interfaz sea la única responsable de validar reglas.
- Añadir campos de creación, actualización y, cuando aplique, actor responsable.

## Pendientes para el diseño de base de datos

- Tipo de identificadores.
- Estrategia de autenticación y sesiones.
- Estructura exacta de ciudades, zonas y coordenadas.
- Almacenamiento de archivos.
- Campos obligatorios de verificación.
- Política de retención y eliminación de datos.
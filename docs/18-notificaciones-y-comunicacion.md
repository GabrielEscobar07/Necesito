# 18 — Notificaciones y comunicación

## Objetivo

Definir qué acontecimientos requieren avisar a una persona sin convertir el MVP en un sistema complejo de mensajería.

## Canales por etapas

### MVP

- Centro de notificaciones dentro de la plataforma.
- Correo electrónico para eventos importantes cuando el usuario tenga correo confirmado.

### Futuro

- Notificaciones push de la PWA.
- WhatsApp o SMS mediante proveedores externos y con consentimiento.
- SignalR para actualizaciones en tiempo real.
- Preferencias detalladas por canal.

La selección de canales externos deberá considerar costo, normativa, consentimiento y confiabilidad en Bolivia.

## Eventos para clientes

- Solicitud publicada.
- Nueva cotización recibida.
- Cotización retirada o vencida.
- Cotización aceptada y contratación creada.
- Cambio relevante del servicio.
- Cancelación por proveedor o administración.
- Solicitud de confirmación de finalización.
- Habilitación para calificar.
- Respuesta a un reporte.

## Eventos para proveedores

- Nueva oportunidad compatible.
- Solicitud modificada de forma relevante o cancelada.
- Cotización aceptada, no seleccionada o vencida.
- Nueva contratación.
- Cambio de coordinación o estado.
- Cancelación del cliente o administración.
- Nueva observación o decisión de verificación.
- Reporte o medida administrativa que deba conocer.

## Eventos administrativos

- Nueva solicitud de verificación.
- Reporte de seguridad o conducta.
- Acumulación anormal de cancelaciones.
- Error operacional que requiera atención.

## Reglas

- Toda notificación debe tener tipo, destinatario, fecha, referencia y estado.
- Una notificación no reemplaza la validación del estado real del recurso.
- No incluir documentos, direcciones completas ni datos sensibles en asuntos de correo.
- Los envíos externos deberán ser reintentables sin duplicar efectos del negocio.
- Los avisos promocionales estarán separados de los operativos y requerirán preferencias adecuadas.
- La ausencia de entrega de un correo no debe corromper una contratación.

## Comunicación entre cliente y proveedor

Durante el MVP se priorizará la información estructurada: solicitud, cotización, observaciones y datos de coordinación después de contratar. Un chat interno completo queda fuera del alcance inicial.

Antes de agregar chat se deberán resolver moderación, archivos, bloqueo, retención, notificaciones y protección de datos.
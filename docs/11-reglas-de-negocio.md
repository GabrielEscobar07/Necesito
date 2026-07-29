# 11 — Reglas de negocio

## Estado del documento

Las reglas marcadas como **provisionales** deberán validarse con usuarios reales antes del lanzamiento.

## Cuentas y roles

- **RN-001:** una persona tendrá una sola cuenta principal.
- **RN-002:** la misma cuenta podrá actuar como cliente y proveedor mediante perfiles y permisos diferenciados.
- **RN-003:** el rol administrativo no podrá autoasignarse desde el registro público.
- **RN-004:** una cuenta suspendida no podrá publicar, cotizar ni aceptar nuevas contrataciones.

## Proveedores y verificación

- **RN-010:** solo proveedores activos podrán recibir nuevas oportunidades.
- **RN-011:** la plataforma distinguirá entre perfil no verificado, en revisión, verificado, observado y rechazado.
- **RN-012:** la aprobación será realizada por un administrador durante el MVP.
- **RN-013:** una verificación confirma que se revisó determinada información; no garantiza la calidad de cada trabajo.
- **RN-014:** cambios relevantes en identidad o datos profesionales podrán exigir una nueva revisión.
- **RN-015:** los documentos de verificación no serán visibles públicamente.

## Solicitudes

- **RN-020:** toda solicitud deberá tener cliente, categoría, descripción y zona o ubicación válida.
- **RN-021:** una solicitud podrá estar en borrador, publicada, con cotizaciones, adjudicada, cancelada, vencida o cerrada.
- **RN-022:** una solicitud publicada podrá recibir cotizaciones hasta que se adjudique, cancele o venza.
- **RN-023:** la plataforma no deberá mostrar la dirección exacta a todos los proveedores antes de la contratación. Esta regla es provisional hasta validar el flujo de ubicación.
- **RN-024:** el cliente es responsable de describir la necesidad con información suficiente y lícita.
- **RN-025:** solicitudes peligrosas, ilegales o fuera de las categorías admitidas podrán bloquearse.

## Distribución de oportunidades

- **RN-030:** un proveedor será compatible cuando su categoría, zona, disponibilidad y estado lo permitan.
- **RN-031:** aparecer como compatible no obliga al proveedor a cotizar.
- **RN-032:** el MVP no asignará automáticamente un trabajador ni prometerá tiempos de llegada.
- **RN-033:** la lógica de distribución deberá evitar revelar datos personales innecesarios.

## Cotizaciones

- **RN-040:** una cotización deberá indicar monto, moneda, alcance básico, disponibilidad y vigencia.
- **RN-041:** los montos iniciales se expresarán en bolivianos, salvo una futura decisión explícita.
- **RN-042:** un proveedor tendrá como máximo una cotización activa por solicitud.
- **RN-043:** una cotización aceptada ya no podrá editarse unilateralmente.
- **RN-044:** costos adicionales deberán acordarse fuera o dentro de un mecanismo posterior; el MVP registrará únicamente la cotización aceptada y las observaciones.
- **RN-045:** la plataforma no cobrará ni custodiará el pago en el MVP.

## Contratación

- **RN-050:** aceptar una cotización crea una contratación entre cliente y proveedor.
- **RN-051:** una solicitud solo puede tener una cotización aceptada.
- **RN-052:** las demás cotizaciones quedarán no seleccionadas cuando exista una contratación.
- **RN-053:** cliente y proveedor verán los datos necesarios para coordinar después de la contratación.
- **RN-054:** los estados no podrán retroceder libremente; las correcciones sensibles requerirán trazabilidad.

## Cancelaciones e incidencias

- **RN-060:** una solicitud sin contratación podrá cancelarse indicando un motivo.
- **RN-061:** una contratación podrá cancelarse por cliente, proveedor o administrador según su estado.
- **RN-062:** cancelaciones repetidas podrán activar revisión administrativa.
- **RN-063:** una incidencia no elimina automáticamente la contratación ni la reputación.
- **RN-064:** el administrador podrá suspender temporalmente una cuenta ante riesgos razonables, dejando motivo y evidencia.

## Calificaciones

- **RN-070:** solo una contratación finalizada habilita calificación.
- **RN-071:** solo el cliente contratante podrá calificar al proveedor en el MVP.
- **RN-072:** una contratación admite una calificación activa.
- **RN-073:** comentarios ofensivos, discriminatorios o con datos personales podrán moderarse.
- **RN-074:** la reputación deberá distinguir cantidad de trabajos y promedio para evitar interpretaciones engañosas.

## Administración y auditoría

- **RN-080:** toda aprobación, rechazo, suspensión o cambio administrativo sensible deberá registrar responsable, fecha y motivo.
- **RN-081:** no se eliminarán físicamente registros críticos cuando la conservación sea necesaria para auditoría; se usarán estados o baja lógica.
- **RN-082:** los administradores accederán únicamente a la información necesaria para su función.

## Pendientes de validación

- Vigencia predeterminada de solicitudes y cotizaciones.
- Políticas de cancelación y posibles penalizaciones.
- Criterios exactos para mostrar dirección y teléfono.
- Tratamiento de servicios urgentes o de riesgo.
- Modelo comercial y comisiones futuras.
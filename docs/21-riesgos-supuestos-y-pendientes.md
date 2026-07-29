# 21 — Riesgos, supuestos y decisiones pendientes

## Objetivo

Evitar que las hipótesis se confundan con hechos confirmados.

## Supuestos actuales

- Existe interés de clientes por comparar varias cotizaciones.
- Los proveedores aceptarían responder oportunidades desde una plataforma.
- Las tres categorías iniciales permiten validar el flujo.
- Santa Cruz de la Sierra ofrece una escala adecuada para comenzar.
- La verificación mejora la confianza suficiente para influir en la contratación.
- Una PWA puede cubrir la primera etapa sin aplicaciones nativas separadas.

Todos estos supuestos requieren validación.

## Riesgos de producto

### Poca oferta o demanda inicial

Sin suficientes clientes o proveedores, la plataforma no genera valor. Mitigación: lanzamiento acotado por categorías y zonas, incorporación manual inicial y medición del tiempo hasta la primera cotización.

### Cotizaciones difíciles de comparar

Algunos trabajos requieren inspección antes de precio final. Mitigación: permitir alcance, condiciones y precio estimado o visita, sin presentar todos los servicios como precio cerrado.

### Percepción excesiva de garantía

El distintivo verificado podría interpretarse como garantía de calidad. Mitigación: explicar claramente qué se revisó y mostrar reputación e historial por separado.

### Desintermediación

Cliente y proveedor pueden coordinar fuera de la plataforma. Mitigación futura: ofrecer valor real en historial, reputación, soporte, garantías o pagos, sin bloquear artificialmente el contacto.

### Cancelaciones y falta de asistencia

Pueden reducir la confianza. Mitigación: registrar motivos, medir comportamiento y establecer políticas después de obtener evidencia.

### Servicios de riesgo

Electricidad y refrigeración pueden implicar peligros. Mitigación: advertencias, categorías claras, requisitos profesionales cuando correspondan y exclusión de instrucciones inseguras.

## Riesgos técnicos

- Diseñar demasiada infraestructura antes de validar el producto.
- Exponer ubicaciones o documentos por errores de autorización.
- Crear estados inconsistentes entre frontend y backend.
- Dependencia prematura de servicios externos.
- Almacenar archivos sin política de seguridad.
- Falta de copias de seguridad y recuperación.
- Complejidad por incorporar PostGIS, Redis o SignalR antes de necesitarlos.

## Riesgos operativos

- Capacidad limitada para revisar verificaciones y reportes.
- Criterios administrativos inconsistentes.
- Falta de horarios y canales de soporte.
- Dificultad para comprobar documentos.
- Responsabilidad ante disputas o daños.

## Decisiones pendientes antes de producción

- Nombre comercial definitivo y disponibilidad de marca/dominio.
- Entidad responsable y datos legales del servicio.
- Política de privacidad y términos de uso.
- Documentos exactos para verificar cada categoría.
- Política de ubicación y momento de revelar la dirección.
- Vigencia de solicitudes y cotizaciones.
- Cancelaciones, faltas de asistencia y disputas.
- Modelo de monetización.
- Tratamiento de impuestos, comprobantes y pagos futuros.
- Canal de soporte y tiempos de respuesta.
- Política de retención y eliminación de datos.

## Entrevistas pendientes

Cuando exista tiempo, entrevistar al menos:

- Personas que hayan contratado electricidad, plomería o refrigeración recientemente.
- Técnicos independientes.
- Pequeñas empresas proveedoras.
- Personas que administren edificios o negocios.

Preguntas centrales:

- ¿Cómo encuentran hoy al técnico?
- ¿Qué información necesitan antes de contratar?
- ¿Qué genera desconfianza?
- ¿Cotizan a distancia o requieren visita?
- ¿Qué haría que respondan rápidamente?
- ¿Qué problemas ocurren después de contratar?
- ¿Pagarían o aceptarían comisión por algún beneficio específico?

## Métricas iniciales propuestas

- Solicitudes publicadas.
- Porcentaje que recibe al menos una cotización.
- Tiempo hasta primera cotización.
- Cotizaciones por solicitud.
- Porcentaje de solicitudes adjudicadas.
- Servicios finalizados.
- Cancelaciones por parte y motivo.
- Proveedores activos semanalmente.
- Tiempo de revisión de verificaciones.
- Reportes por contratación.

Las métricas deberán usarse para aprender, no para declarar éxito sin contexto.
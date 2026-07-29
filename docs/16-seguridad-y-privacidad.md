# 16 — Seguridad y privacidad

## Alcance

Este documento define principios del producto. La implementación técnica detallada se diseñará cuando comience el backend y deberá complementarse con revisión legal antes de producción.

## Clasificación de información

### Pública

Nombre profesional, descripción autorizada, categorías, zona general, reputación y distintivos visibles.

### Privada entre las partes

Datos de coordinación necesarios después de una contratación, como dirección exacta o teléfono, según la política final.

### Confidencial administrativa

Documentos de identidad, evidencia de verificación, reportes, notas internas y medidas de seguridad.

### Técnica sensible

Contraseñas, tokens, claves, secretos, registros de seguridad y configuraciones privadas. Nunca deben almacenarse en el repositorio.

## Principios de privacidad

- Minimización: recopilar solo lo necesario.
- Finalidad: explicar para qué se usa cada dato.
- Acceso limitado: cada rol ve lo requerido para su tarea.
- Retención controlada: no conservar indefinidamente sin motivo.
- Exactitud: permitir corregir información personal.
- Transparencia: informar cambios importantes en el tratamiento.
- Seguridad por defecto: no exponer dirección, teléfono o documentos públicamente.

## Ubicación

Propuesta inicial pendiente de validación:

- Antes de contratar, el proveedor ve una zona aproximada o referencia suficiente para cotizar.
- Después de aceptar una cotización, las partes reciben la información necesaria para coordinar.
- Las coordenadas exactas no se publican en listados.
- Las fotografías deberán revisarse para reducir exposición accidental de documentos, rostros o direcciones cuando sea posible.

## Controles mínimos futuros

- Hash seguro de contraseñas.
- Confirmación de medios de contacto.
- Autorización por rol y por propiedad del recurso.
- Protección contra intentos automatizados y abuso.
- Validación de archivos, tamaño y tipos permitidos.
- Registro de eventos de seguridad.
- Rotación de secretos y variables de entorno.
- Copias de seguridad cifradas cuando contengan datos sensibles.
- Cifrado en tránsito mediante HTTPS.
- Actualización periódica de dependencias.

## Archivos y documentos

- Usar almacenamiento privado con acceso temporal o controlado.
- No confiar únicamente en la extensión del archivo.
- Limitar tamaño y formatos.
- Separar archivos públicos de documentos de verificación.
- Evitar nombres de archivo que revelen información sensible.
- Registrar quién accede a documentos administrativos cuando sea viable.

## Derechos y operaciones de datos

La plataforma deberá prepararse para:

- Consultar datos propios.
- Corregir información.
- Solicitar desactivación o eliminación cuando sea legalmente posible.
- Conservar ciertos registros cuando exista obligación, fraude, disputa o necesidad legítima documentada.

No se prometerá eliminación total inmediata sin revisar las obligaciones aplicables.

## Incidentes

Ante una posible exposición:

1. Limitar el acceso afectado.
2. Conservar evidencia técnica.
3. Evaluar datos y usuarios involucrados.
4. Corregir la causa.
5. Informar según corresponda.
6. Documentar acciones y aprendizajes.

## Amenazas iniciales a considerar

- Cuentas falsas y suplantación.
- Acceso de un usuario a recursos ajenos.
- Enumeración de teléfonos o correos.
- Carga de archivos maliciosos.
- Exposición de ubicaciones.
- Abuso de calificaciones o reportes.
- Robo de sesión.
- Secretos incluidos accidentalmente en Git.
- Acciones administrativas sin auditoría.

## Antes de producción

Será necesaria una política de privacidad, términos de uso, procedimiento de reportes y revisión de las normas aplicables en Bolivia. Estos textos no deberán copiarse de otra plataforma sin revisión profesional.
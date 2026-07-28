# Política de seguridad

## Reporte responsable

No publiques vulnerabilidades, credenciales o datos sensibles mediante una incidencia pública de GitHub.

Mientras no exista un canal de seguridad dedicado, informa el problema directamente al propietario del repositorio mediante un medio privado.

## Información que debe incluir el reporte

- Descripción del problema.
- Área afectada.
- Pasos mínimos para reproducirlo.
- Impacto esperado.
- Evidencia sin datos personales reales.
- Posible mitigación, si se conoce.

## Reglas obligatorias del repositorio

- No almacenar secretos, tokens, contraseñas o claves privadas.
- No confirmar archivos `.env` reales.
- No utilizar datos personales de clientes o proveedores en pruebas.
- Mantener dependencias y runtimes soportados.
- Aplicar autorización en el servidor, no solamente en la interfaz.
- Validar archivos, imágenes y datos enviados por usuarios.

## Alcance futuro

Antes de operar con usuarios reales deberán definirse formalmente:

- Gestión de sesiones y autenticación.
- Verificación de proveedores.
- Protección de datos personales.
- Auditoría de acciones administrativas.
- Copias de seguridad y recuperación.
- Respuesta ante incidentes.

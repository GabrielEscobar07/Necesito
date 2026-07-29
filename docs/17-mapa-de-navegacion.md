# 17 — Mapa de navegación inicial

## Objetivo

Organizar una sola aplicación web/PWA con experiencias diferenciadas para visitantes, clientes, proveedores y administradores.

## Área pública

```text
/
├── /como-funciona
├── /categorias
├── /profesionales
├── /seguridad-y-confianza
├── /iniciar-sesion
└── /registro
```

La página principal tendrá dos acciones predominantes:

- **Necesito un servicio.**
- **Quiero ofrecer mis servicios.**

## Área de cliente

```text
/cliente
├── /cliente/solicitudes
│   ├── /cliente/solicitudes/nueva
│   └── /cliente/solicitudes/[id]
├── /cliente/cotizaciones
├── /cliente/contrataciones
│   └── /cliente/contrataciones/[id]
├── /cliente/calificaciones
├── /cliente/notificaciones
└── /cliente/configuracion
```

Panel inicial sugerido:

- Solicitudes activas.
- Cotizaciones nuevas.
- Próximos servicios.
- Acceso rápido para publicar una necesidad.

## Área de proveedor

```text
/proveedor
├── /proveedor/oportunidades
│   └── /proveedor/oportunidades/[id]
├── /proveedor/cotizaciones
├── /proveedor/trabajos
│   └── /proveedor/trabajos/[id]
├── /proveedor/perfil
├── /proveedor/verificacion
├── /proveedor/notificaciones
└── /proveedor/configuracion
```

Panel inicial sugerido:

- Estado de verificación.
- Disponibilidad actual.
- Oportunidades nuevas.
- Cotizaciones pendientes.
- Trabajos adjudicados.

## Área administrativa

```text
/admin
├── /admin/verificaciones
├── /admin/usuarios
├── /admin/categorias
├── /admin/zonas
├── /admin/solicitudes
├── /admin/contrataciones
├── /admin/reportes
└── /admin/auditoria
```

El panel administrativo no deberá compartir el mismo menú operativo que clientes o proveedores.

## Cambio de modo

Una persona que tenga perfil de cliente y proveedor podrá cambiar de modo desde su cuenta. El cambio modifica navegación y contexto visual, no crea una nueva sesión ni duplica la identidad.

## Principios de experiencia

- Diseño mobile-first.
- Una acción principal visible por pantalla.
- Estados y próximos pasos explicados con lenguaje cotidiano.
- Formularios divididos cuando la cantidad de información lo justifique.
- Confirmación antes de publicar, contratar, cancelar o suspender.
- No depender únicamente del color para comunicar estados.
- Mantener rutas y nombres independientes del nombre comercial definitivo.

## Flujos prioritarios para diseñar antes del estilo visual completo

1. Registro e inicio de sesión.
2. Activación de perfil proveedor.
3. Publicación de solicitud.
4. Envío y comparación de cotizaciones.
5. Aceptación y seguimiento del servicio.
6. Verificación administrativa.
7. Reportes y suspensión.

## Fuera del mapa inicial

Chat en tiempo real, pagos internos, tienda de repuestos, suscripciones y aplicación React Native se incorporarán únicamente en etapas posteriores.
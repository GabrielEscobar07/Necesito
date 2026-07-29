# 14 — Estados y transiciones

## Principio

Los estados representan hechos del negocio. No deberán modificarse libremente desde la interfaz ni aceptarse transiciones inválidas en la API.

## Solicitud de servicio

| Estado | Significado |
|---|---|
| `BORRADOR` | El cliente todavía no publicó. |
| `PUBLICADA` | Puede distribuirse y recibir cotizaciones. |
| `CON_COTIZACIONES` | Tiene al menos una cotización activa. |
| `ADJUDICADA` | Una cotización fue aceptada. |
| `CANCELADA` | El cliente o administrador la canceló. |
| `VENCIDA` | Terminó su período sin adjudicación. |
| `CERRADA` | El flujo asociado terminó. |

Transiciones principales:

```text
BORRADOR → PUBLICADA
PUBLICADA → CON_COTIZACIONES
PUBLICADA → CANCELADA | VENCIDA
CON_COTIZACIONES → ADJUDICADA | CANCELADA | VENCIDA
ADJUDICADA → CERRADA
```

## Cotización

| Estado | Significado |
|---|---|
| `ACTIVA` | Puede ser evaluada por el cliente. |
| `RETIRADA` | El proveedor la retiró antes de aceptación. |
| `ACEPTADA` | Fue seleccionada. |
| `NO_SELECCIONADA` | Otra propuesta fue aceptada. |
| `VENCIDA` | Finalizó su vigencia. |
| `INVALIDADA` | Administración la anuló por una causa documentada. |

Una cotización `ACEPTADA` no regresa a `ACTIVA` mediante una edición ordinaria.

## Verificación de proveedor

| Estado | Significado |
|---|---|
| `NO_INICIADA` | El proveedor todavía no envió información. |
| `BORRADOR` | Está preparando su solicitud. |
| `EN_REVISION` | Fue enviada y espera decisión. |
| `OBSERVADA` | Requiere correcciones o información adicional. |
| `APROBADA` | La revisión fue satisfactoria. |
| `RECHAZADA` | No cumplió requisitos o existen inconsistencias. |
| `VENCIDA` | Requiere renovación. |
| `REVOCADA` | La aprobación fue retirada con motivo registrado. |

## Contratación

| Estado | Significado |
|---|---|
| `CONFIRMADA` | Se creó a partir de una cotización aceptada. |
| `COORDINANDO` | Las partes acuerdan fecha y detalles. |
| `PROGRAMADA` | Existe una fecha acordada. |
| `EN_PROGRESO` | El servicio comenzó. |
| `FINALIZACION_PENDIENTE` | Una parte indicó que terminó. |
| `FINALIZADA` | El servicio quedó cerrado. |
| `CANCELADA_CLIENTE` | Canceló el cliente. |
| `CANCELADA_PROVEEDOR` | Canceló el proveedor. |
| `CANCELADA_ADMIN` | Canceló administración con causa. |
| `EN_DISPUTA` | Existe una incidencia abierta que requiere revisión. |

Flujo esperado:

```text
CONFIRMADA → COORDINANDO → PROGRAMADA → EN_PROGRESO
EN_PROGRESO → FINALIZACION_PENDIENTE → FINALIZADA
```

Las cancelaciones y disputas dependen del punto del flujo y deberán registrar motivo.

## Reporte

| Estado | Significado |
|---|---|
| `ABIERTO` | Fue recibido. |
| `EN_REVISION` | Un administrador lo está analizando. |
| `ESPERANDO_INFORMACION` | Se solicitó información adicional. |
| `RESUELTO` | Se tomó una medida o se cerró con explicación. |
| `DESCARTADO` | No correspondía o no tenía sustento suficiente. |

## Reglas técnicas futuras

- Cada cambio genera un registro de historial.
- La API valida actor, estado anterior y estado destino.
- Las acciones repetidas deben manejarse de forma segura.
- Los nombres internos pueden implementarse como enumeraciones o catálogos según el módulo.
- La interfaz solo mostrará acciones permitidas, pero la seguridad real estará en el backend.
# 04 — Flujo del servicio

## Flujo principal

```text
Cliente publica solicitud
        ↓
Sistema valida y clasifica
        ↓
Proveedores compatibles pueden verla
        ↓
Proveedores envían cotizaciones
        ↓
Cliente compara y acepta una
        ↓
Servicio adjudicado
        ↓
Trabajo realizado
        ↓
Finalización y calificación
```

## Etapa 1: creación de solicitud

El cliente proporciona como mínimo:

- Categoría.
- Descripción del problema.
- Zona o ubicación aproximada.
- Disponibilidad o momento preferido.
- Medio de contacto permitido.

Podrán agregarse fotografías de manera opcional, sujetas a validación de tamaño, formato y seguridad.

## Etapa 2: publicación

La API valida la solicitud y determina si puede publicarse. Una solicitud inválida no debe distribuirse a proveedores.

Estados preliminares:

```text
Borrador → Publicada → En cotización → Adjudicada → En ejecución → Completada
                       └→ Cancelada
                       └→ Expirada
```

Los nombres definitivos se validarán al diseñar el modelo de dominio.

## Etapa 3: cotizaciones

Una cotización debería incluir:

- Precio estimado o modalidad de cálculo.
- Descripción de lo incluido.
- Disponibilidad.
- Vigencia de la propuesta.
- Observaciones.

Debe quedar claro cuándo el precio es estimado y cuándo es definitivo.

## Etapa 4: selección

El cliente compara propuestas y acepta una. Al adjudicar:

- La cotización seleccionada cambia de estado.
- Las demás cotizaciones dejan de estar disponibles para aceptación.
- El proveedor seleccionado recibe confirmación.
- La operación debe ser transaccional para evitar dobles adjudicaciones.

## Etapa 5: ejecución y cierre

Cliente y proveedor registran el avance mínimo necesario. Al finalizar, el cliente puede confirmar el servicio y emitir una calificación.

## Casos que deben definirse después

- Cancelaciones después de aceptar una cotización.
- Proveedor que no se presenta.
- Cliente ausente.
- Cambio de precio durante el servicio.
- Trabajo parcialmente realizado.
- Disputas y evidencia.
- Emergencias y riesgos físicos.

# Cómo consultar y publicar topes de descuento

Define cuánto puede rebajar una persona por venta según su rol. Los cambios se publican como versiones con fecha de vigencia; el historial no se edita.

> **Quién puede hacerlo:** Super Administrador y Administrador consultan; solo el Super Administrador publica. «Consultar topes de descuento» efectivo permite consultar a otros roles.
> **Dónde está:** menú lateral → Ventas → **Topes de descuento**.

## Antes de empezar

**Sin tope** y **0** son distintos: sin tope no limita el monto de la rebaja; 0 no permite descontar. Si no hay una versión vigente, los valores de respaldo son:

| Rol | Tope por defecto |
|---|---|
| Super Administrador / Administrador | Sin tope |
| Administrador de Punto / Vendedor / Bodeguero | $0 |

El sistema considera la rebaja efectiva: bajar el precio de referencia frente al precio publicado del equipo y aplicar el campo Descuento suma para el mismo límite. No basta con revisar únicamente el campo Descuento.

## Cómo consultar el tope vigente y el historial

1. Entra a **Topes de descuento**.
2. Revisa **Vigente por rol**, con **Rol**, **Tope vigente** y **Vigente desde**.
3. Si aparece **Por defecto**, ese rol no tiene una versión vigente y se muestra el respaldo.
4. Revisa **Historial de versiones**, con **Rol**, **Tope**, **Vigente desde** y **Creada**.

La etiqueta **Vigente** identifica la versión aplicable según la fecha usada por la pantalla. Una versión futura no reemplaza todavía la vigente. Para corregir un valor publicado se agrega otra versión; no hay botón para editar o borrar una anterior.

La etiqueta de vigencia usa la fecha del dispositivo; la autorización de la venta usa la fecha del negocio. Cerca del cambio de día, un dispositivo en otra zona horaria puede señalar una versión diferente.

## Cómo publicar una versión

1. Haz clic en **Nueva versión**.
2. En **Rol**, elige a quién aplica.
3. En **Tope**, escribe el máximo permitido, o déjalo vacío para **sin tope**.
4. En **Vigente desde**, elige la fecha desde la que debe regir.
5. Haz clic en **Publicar**.

El formulario abre la fecha de hoy del dispositivo. **Rol** y **Vigente desde** son obligatorios; **Tope** no lo es. No uses un valor negativo. Mientras se envía aparece **Publicando…** y no puedes cerrar el diálogo.

Al terminar se cierra el diálogo y se recarga la configuración. Una fecha futura queda en el historial; no debe interpretarse como el límite autorizado hoy. Las ventas ya registradas conservan la versión del tope utilizada al registrarlas.

## Qué ve cada rol

| Rol | Consulta esta pantalla | Publica |
|---|---|---|
| Super Administrador | Sí | Sí |
| Administrador | Sí | No |
| Administrador de Punto / Vendedor / Bodeguero | Con «Consultar topes de descuento» efectivo | No |

Quien tiene **Registrar ventas** puede consultar su propio tope desde el formulario de venta sin tener acceso a este historial de los demás roles. Crear topes es reservado al Super Administrador.

## Relación con otros módulos

**Necesitas antes:**
- Conocer los [roles y permisos](../general/roles-y-permisos.md) que usa el negocio.
- [Precios del equipo](../inventario/precios.md), base para medir la rebaja.
- Lecturas de apoyo, según la tarea que realices: [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md).

**Esto afecta a:**
- [Nueva venta](nueva-venta.md): el límite se valida al registrar.
- [Solicitudes](solicitudes.md): una modificación se juzga contra el tope de quien aprueba en el momento de aprobar.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Elige el rol y la fecha desde la que rige antes de publicar.» | Falta un dato obligatorio. | Elige Rol y Vigente desde. |
| «El tope de descuento no puede ser negativo (9.8).» | El valor no es válido. | Usa un valor no negativo o vacío para sin tope. |
| No aparece Nueva versión | Puedes consultar, pero no publicar. | Solicita el cambio al Super Administrador. |

Si no llegó confirmación al publicar, revisa el historial antes de repetir el envío. Otra publicación crea otra versión, no edita la anterior.

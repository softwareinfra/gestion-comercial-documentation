# Ficha del equipo

Revisa los datos de una unidad, sus precios y, según tus permisos, corrige datos de compra o consulta sus cambios.

> **Quién puede hacerlo:** los cinco roles consultan los equipos de su alcance; las acciones dependen del permiso.
> **Dónde está:** Inventario → Equipos → icono Ver (`/inventario/equipos/:id`).

## Cómo consultar la ficha

1. Busca el equipo en [Equipos](equipos.md).
2. Pulsa **Ver** en la fila y comprueba el IMEI y el número del título **Equipo …**.
3. Revisa las secciones de la ficha.
4. Para regresar al listado, pulsa **Volver a Equipos**.

| Sección | Contenido |
|---|---|
| Datos del equipo | No. interno, IMEI, referencia, categoría, estado operativo, ubicación, RAM, almacenamiento, color, batería, días en inventario, disponibilidad para venta y notas. |
| Compra | Proveedor si tienes acceso a proveedores; factura, guía, fechas de pedido, ingreso y salida; costo y ganancia si tienes acceso al costo. |
| Precios de venta | Crédito y Contado efectivos. Con acceso al costo se distingue «a mano» y se muestra el sugerido correspondiente cuando el precio fue fijado a mano. |
| Auditoría | Estado del registro, creación, actualización y fechas de deshabilitado o anulado cuando existan. |

**Estado del registro** y **Estado** operativo no son el mismo dato. La ficha no ofrece botones para deshabilitar, activar o anular el registro. **Días en inventario** sigue contando desde el ingreso hasta hoy; no se detiene en la fecha de salida.

Si tienes acceso a Garantías y hay relaciones registradas, aparece **Reemplazo por garantía**: distingue el equipo que salió de una venta por garantía del que entró como reemplazo. El enlace a la venta depende además del permiso para consultar ventas.

## Cómo editar la ficha

Necesitas **Editar la ficha, el costo y los precios del equipo**. No necesitas crear otro ingreso para corregir los campos que este formulario admite.

1. Pulsa **Editar**.
2. Corrige los campos del formulario.
3. Comprueba especialmente Costo y Ganancia. Si cambias la ganancia a un valor distinto, los precios fijados a mano vuelven al sugerido.
4. Pulsa **Guardar**; durante el envío dice **Guardando…**.

Al guardar correctamente se cierra el formulario y se vuelve a cargar la ficha con los datos del servidor. **Cancelar** cierra sin guardar. No hay campos editables para IMEI, referencia, categoría, proveedor, ubicación ni fecha de ingreso o salida en este formulario. Crédito y Contado se fijan desde [la tabla de Equipos](equipos.md#cómo-ajustar-precios-de-uno-o-varios-equipos), no desde esta ficha.

Cambiar Costo modifica el cálculo sugerido, pero no elimina por sí solo los precios a mano. Cambiar la ganancia numéricamente sí elimina esos precios. Revisa [la relación entre precios manuales y sugeridos](precios.md#cómo-se-calculan-los-precios) antes de guardar.

### Qué significa cada campo editable

| Campo | Qué poner | Regla |
|---|---|---|
| Costo | Costo de compra, en pesos. | Cero o más; hasta dos decimales y 12 dígitos en total. |
| Ganancia | Ganancia definida para calcular el sugerido. | Cero o más; hasta dos decimales y 12 dígitos en total. |
| Factura del proveedor | Número de factura asociado a esta unidad. | Obligatorio; hasta 50 caracteres. |
| Guía | Número de guía. | Opcional; hasta 50 caracteres. |
| Fecha de pedido | Fecha del pedido de compra. | Opcional; al dejarla vacía se quita. |
| RAM | Dato de memoria, por ejemplo el texto con su capacidad. | Opcional; hasta 30 caracteres. |
| Almacenamiento | Dato de capacidad. | Opcional; hasta 30 caracteres. |
| Color | Color del equipo. | Opcional; hasta 40 caracteres. |
| Batería (%) | Porcentaje entero de batería. | De 0 a 100; obligatorio para iPhone de categoría Exhibición. |
| Notas | Observaciones de la unidad. | Opcional. |

En Costo y Ganancia escribe el número sin símbolo de moneda ni separadores de miles; para decimales usa un punto. El formulario envía esos textos al servidor sin convertirlos como las celdas monetarias del listado.

## Cómo cambiar el estado operativo

Necesitas **Cambiar el estado de un equipo**. El botón aparece cuando tienes ese permiso y hay destinos disponibles para su estado operativo.

1. Pulsa **Cambiar estado**.
2. En **Nuevo estado**, elige uno de los destinos ofrecidos para el estado actual.
3. Escribe el **Motivo**. Es obligatorio y no sirve dejar solamente espacios.
4. Pulsa **Cambiar estado** dentro del diálogo; durante el envío dice **Enviando…**.

Al guardar se cierra el diálogo y se recarga la ficha. El cambio queda en el historial con su motivo. Los destinos dependen del estado actual, no de todos los estados del catálogo. Consulta [Estados operativos](../administracion/estados-operativos.md) para los recorridos y sus excepciones.

Si eliges **Vendido** y **Fecha de salida** está vacía, el sistema la completa con la fecha local actual del servidor. Si ya tiene una fecha, la conserva. Puedes verla en **Compra** tras recargar la ficha.

Esta acción cambia el estado del equipo: no registra por sí misma una venta, un traslado ni una garantía. Para esos procesos usa sus pantallas. Un equipo Vendido no puede volver manualmente a Disponible; la reversión al anular una venta es un proceso distinto. Un registro anulado no admite cambios aunque un botón siga apareciendo por su estado operativo.

## Cómo consultar el historial

Si tienes **Ver historial del equipo**, debajo de la ficha aparece **Historial**. Usa su paginación para consultar los registros. Muestra Fecha, Usuario, Sucursal, Acción, Qué cambió, Estado, Motivo y Aprobó.

**Qué cambió** muestra el valor anterior y el nuevo cuando corresponde. El historial incluye la creación del equipo desde su ingreso. Sin **Ver costo y ganancia** se ocultan esos valores; sin acceso a proveedores, se ocultan los datos de proveedor protegidos. Si no hay eventos, aparece **«Todavía no hay movimientos registrados.»**.

## Qué ve cada rol

Permisos de base, sin extras:

| Rol | Consultar | Costo, ganancia y proveedor | Editar ficha | Cambiar estado / historial |
|---|---|---|---|---|
| Super Administrador | Global | Sí | Sí | Sí |
| Administrador | Global | Sí | Sí | Sí |
| Administrador de Punto | Su sede | Sí | No | Sí |
| Vendedor | Su sede | No | No | No |
| Bodeguero | Su sede | Sí | No | Sí |

Un permiso extra puede abrir edición, cambio de estado, historial o información protegida, manteniendo el alcance de sede. Editar exige también **Ver costo y ganancia**. Ver el historial no concede automáticamente ese acceso al costo. Consulta [Roles y permisos](../general/roles-y-permisos.md) y [Permisos extra](../administracion/usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra).

## Relación con otros módulos

**Necesitas antes:**

- [Equipos](equipos.md): desde el listado abres esta ficha.
- [Categorías de equipo](../administracion/categorias-de-equipo.md): explican la batería obligatoria para iPhone de Exhibición.
- Lecturas de apoyo, según la tarea que realices: [Estados operativos](../administracion/estados-operativos.md); [Proveedores](../administracion/proveedores.md); [Registrar y consultar ingresos](ingresos.md); [Cómo se calculan los precios](precios.md#cómo-se-calculan-los-precios); [Trasladar equipos entre sedes](traslados.md); [Cómo registrar una venta](../ventas/nueva-venta.md); [Cómo solicitar y resolver cambios de una venta](../ventas/solicitudes.md); [Cómo atender un equipo en garantía](../garantias/equipos-en-garantia.md); [Cómo consultar el tablero de inventario](../dashboard/tablero-de-inventario.md).

**Esto afecta a:**

- [Precios](precios.md): el costo y la ganancia intervienen en los sugeridos.
- [Traslados](traslados.md): son el proceso para mover la ubicación del equipo.
- [Ventas](../ventas/ventas.md) y [Garantías](../garantias/equipos-en-garantia.md): gestionan sus propios procesos; el cambio manual de estado no los sustituye.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| No aparece Editar | Tu permiso no permite corregir la ficha. | Consulta con quien administra los permisos; no crees un equipo duplicado. |
| No aparece Cambiar estado | Falta el permiso o no hay destinos ofrecidos para ese estado. | Revisa tu acceso y el recorrido del estado actual. |
| «La batería debe ser un número entero entre 0 y 100.» | El texto no es un porcentaje entero válido. | Escribe un entero entre 0 y 100. |
| «Elige el nuevo estado.» | No seleccionaste un destino. | Elige una opción de Nuevo estado. |
| «El motivo es obligatorio.» | Falta el motivo del cambio. | Escribe por qué cambias el estado. |
| «El equipo ya está en ese estado.» | Su estado coincide con el destino; pudo cambiar desde que abriste la ficha. | Recarga y revisa el estado actual antes de repetir. |
| «La anulación es terminal: el equipo no cambia más.» | Se intentó modificar un registro anulado. | No reintentes la edición ni el cambio de estado de ese registro. |

Si la ficha no carga o el equipo ya no está en tu alcance, vuelve al listado y verifica el IMEI y la sede. Para otros mensajes, consulta [Qué pasa si hay errores](../general/formularios-y-acciones-comunes.md#qué-pasa-si-hay-errores).

# Equipos

Consulta los equipos de tu alcance, revisa su disponibilidad y, si tienes permiso, ajusta su ganancia y sus precios de venta desde la tabla.

> **Quién puede hacerlo:** los cinco roles consultan. La edición de precios depende del permiso indicado más abajo.
> **Dónde está:** menú lateral → Inventario → Equipos (`/inventario`).

## Antes de empezar

Cada equipo es una unidad identificada por su IMEI. Esta pantalla no tiene un botón para crear equipos: se registran mediante un [ingreso de mercancía](ingresos.md).

El listado también incluye equipos vendidos; no es una lista exclusiva de mercancía disponible. **Días** cuenta desde la fecha de ingreso hasta hoy, incluso después de una venta. **Estado** es el estado operativo del equipo, distinto del estado del registro que aparece en la ficha.

Con los estados de fábrica, Disponible y Reservado pasan el filtro de disponibilidad cuando el registro está Activo. Vendido, En traslado, En garantía, Devuelto por garantía, Inactivo y Dado de baja por nota crédito no pasan ese filtro. La disponibilidad por sí sola no sustituye las validaciones de una venta.

## Cómo consultar y filtrar

1. Abre **Equipos**.
2. En **Filtros de equipos**, despliega **Equipo** o **Producto y ubicación**. En los roles con alcance de sede, el segundo grupo se llama **Producto**.
3. Escribe el IMEI completo en **IMEI** para buscar una coincidencia exacta. No es un buscador por fragmentos ni por nombre de referencia.
4. Si lo necesitas, combina los otros filtros de la tabla.
5. Para empezar de nuevo, usa **Limpiar filtros**.
6. Cambia de página con los controles del listado. Consulta [Listados, filtros y paginación](../general/listados-filtros-y-paginacion.md) para su uso común.

| Filtro | Opciones / alcance |
|---|---|
| Estado | Todos los estados o un estado operativo de Inventario. |
| Disponibilidad | Todos, Disponibles para venta o No disponibles. |
| Tipo de producto | Todos los tipos o uno del catálogo. |
| Marca | Todas las marcas o una del catálogo. |
| Sucursal | Todas las sucursales o una concreta; aparece en los roles de alcance global. |

Al cambiar filtros vuelves a la primera página. El Super Administrador y el Administrador consultan globalmente; Administrador de Punto, Vendedor y Bodeguero ven los equipos cuya ubicación actual es su sede.

## Cómo leer la tabla y abrir una ficha

La tabla muestra **IMEI**, **Referencia**, **Ubicación**, **Estado**, **Días**, **Crédito** y **Contado**. Quien tiene acceso al costo ve además **Costo** y **Ganancia**. Crédito y Contado son los precios efectivos de venta: pueden venir del cálculo sugerido o haberse fijado a mano.

1. Ubica el equipo por su IMEI.
2. En **Acciones**, pulsa el icono **Ver**.
3. Consulta la [ficha del equipo](equipo-detalle.md).

Si tienes cambios de precio pendientes, **Ver** pide confirmar antes de salir. **Abrir la ficha** en ese aviso continúa sin guardar y descarta los cambios pendientes de la tabla.

## Cómo ajustar precios de uno o varios equipos

Necesitas **Editar la ficha, el costo y los precios del equipo**. Super Administrador y Administrador lo tienen por su rol; un permiso extra puede abrirlo a los demás. El costo no se cambia en esta tabla: se corrige en la [ficha](equipo-detalle.md#cómo-editar-la-ficha).

1. Escribe el nuevo valor en **Ganancia**, **Crédito** o **Contado** de la fila.
2. Revisa los indicadores de esa fila: **Antes**, **A mano**, **Se conserva al guardar**, **Se recalcula al guardar** o **Vuelve al sugerido**, según el cambio.
3. Si quieres dejar de fijar un precio a mano, pulsa el icono **Usar el sugerido** de Crédito o Contado. Vaciar el campo y salir de él restaura el valor anterior: no equivale a usar el sugerido.
4. Puedes editar otras filas y cambiar filtros o página. El contador superior cuenta equipos con cambios, no campos; incluye las filas que ya no ves.
5. Pulsa **Guardar cambios**. Mientras se prepara la revisión dice **Revisando…**.
6. En **Confirmar los cambios de precio**, revisa el antes y el después de Ganancia, Crédito y Contado de cada equipo.
7. Pulsa **Confirmar y guardar**. Mientras se envía dice **Guardando…**.

Al guardar correctamente se cierra la revisión, se recarga la tabla y aparece **«Se guardaron los precios de N equipos.»** (para uno, «Se guardaron los precios de 1 equipo.»). El guardado es conjunto: un rechazo de validación impide guardar cualquier fila del lote.

Puedes guardar hasta **100 equipos** en un lote. Si superas ese límite, deshaz cambios de algunas filas y guarda por partes; filtrar para esconderlas no reduce el lote.

Crédito y Contado fijados a mano deben ser positivos, de al menos un peso y sin centavos. Ganancia puede ser cero, no negativa, y admite hasta dos decimales. El sistema valida además el tamaño de los importes.

### Qué cambios se recalculan

Cambiar la ganancia a un valor distinto quita los precios fijados a mano: vuelven al sugerido, salvo que también fijes expresamente esos precios en el mismo lote. Cambiar Crédito afecta al Contado sugerido; un Contado que se conserve a mano no sigue ese recálculo. Cambiar solo Contado no modifica Crédito.

Los importes futuros los calcula el servidor en la revisión, no la tabla mientras escribes. Consulta [Precios y parámetros](precios.md#cómo-se-calculan-los-precios) para las fórmulas. Otro usuario puede cambiar el equipo o los parámetros entre la revisión y el guardado: la vista previa no reserva esos valores.

### Cómo cancelar o deshacer

- **Cancelar** en la revisión la cierra y conserva los cambios pendientes para seguir trabajando.
- El icono **Deshacer** de una fila descarta los cambios de ese equipo.
- **Descartar cambios** abre una confirmación; **Descartar cambios** en ese aviso elimina el lote pendiente.

Los cambios sin guardar viven en la pantalla, no quedan almacenados para la siguiente visita. Cambiar filtros o página los conserva. Salir por el menú o por el botón Atrás puede perderlos sin el aviso propio de **Ver**. Al recargar o cerrar la pestaña, la aplicación solicita al navegador una confirmación de salida; su texto depende del navegador.

## Cómo exportar o imprimir

Con resultados y permiso **Exportar e imprimir el inventario**, al pie de los filtros aparecen **Exportar Excel** e **Imprimir / PDF**. Usan los equipos que coinciden con los filtros de tu alcance, no únicamente la página visible.

1. Ajusta los filtros.
2. Para descargar un archivo de Excel, pulsa **Exportar Excel**. El límite es **20.000 filas**; si lo superas, acota el listado, por ejemplo por Estado.
3. Para una hoja imprimible, pulsa **Imprimir / PDF** y sigue [Imprimir inventario](imprimir-inventario.md). Su límite es **5.000 filas**.

Si hay precios pendientes, **Exportar igual** descarga los valores guardados y conserva tus cambios en la tabla. **Abrir la hoja** imprime sin guardar y descarta los pendientes al salir de esta pantalla. Guarda antes si necesitas que el archivo o la impresión refleje el lote editado.

El Excel incluye datos de identificación, ubicación, estado, fechas y precios. El nombre del proveedor depende del permiso **Consultar proveedores**; costo, ganancia, precios sugeridos y precios manuales dependen de **Ver costo y ganancia**. Un permiso para exportar no abre por sí mismo esos datos.

## Qué ve cada rol

La tabla describe permisos de base, sin extras.

| Rol | Alcance del listado | Costo y ganancia | Editar precios | Exportar / imprimir |
|---|---|---|---|---|
| Super Administrador | Global | Sí | Sí | Sí |
| Administrador | Global | Sí | Sí | Sí |
| Administrador de Punto | Su sede | Sí | No | Sí |
| Vendedor | Su sede | No | No | Sí |
| Bodeguero | Su sede | Sí | No | Sí |

Los permisos extra pueden ampliar acciones, no convierten el alcance de sede en global. Para editar se exige también **Ver costo y ganancia**. Consulta [Permisos extra del usuario](../administracion/usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra).

## Relación con otros módulos

**Necesitas antes:**

- [Ingresos](ingresos.md): registran los equipos que luego consultas aquí.
- [Referencias](../administracion/referencias.md) y [estados operativos](../administracion/estados-operativos.md): explican los catálogos que ves.
- Lecturas de apoyo, según la tarea que realices: [Exportar a Excel e imprimir](../general/exportar-e-imprimir.md); [Listados: buscar, filtrar y pasar de página](../general/listados-filtros-y-paginacion.md); [Menú lateral y navegación](../general/menu-y-navegacion.md); [Categorías de equipo](../administracion/categorias-de-equipo.md); [Marcas](../administracion/marcas.md); [Proveedores](../administracion/proveedores.md); [Sucursales](../administracion/sucursales.md); [Lista completa de permisos extra](../administracion/usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra); [Usuarios](../administracion/usuarios.md); [Cómo se calculan los precios](precios.md#cómo-se-calculan-los-precios).

**Esto afecta a:**

- [Ficha del equipo](equipo-detalle.md): muestra los precios guardados y permite otras correcciones.
- [Nueva venta](../ventas/nueva-venta.md): utiliza los precios y comprueba si el equipo se puede vender.
- [Imprimir inventario](imprimir-inventario.md): consulta los equipos de los filtros seleccionados.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Ningún equipo coincide con el filtro.» | Hay filtros sin coincidencias en tu alcance. | Revisa el IMEI exacto y usa Limpiar filtros. |
| «Todavía no hay equipos.» | El listado sin filtros está vacío para tu alcance. | Revisa la sede y si ya se registró el ingreso. |
| «Ninguno de los cambios modifica los precios de hoy.» | La revisión no detectó cambios efectivos. | Pulsa Cerrar; revisa si necesitas modificar valores. |
| «No se guardó ningún cambio.» o el aviso equivalente que cuenta equipos con errores | El servidor rechazó el lote. | Corrige los mensajes de las filas y vuelve a Guardar cambios. |
| «Mostrar en la tabla» junto a un error | El equipo con error no está en la página visible. | Pulsa ese botón: limpia los otros filtros y busca su IMEI. |
| «Recargar la tabla» | Un equipo cambió de alcance o fue anulado durante el trabajo. | Recarga para revisar la situación; conserva los pendientes, así que corrige o deshaz los de la fila afectada. |
| «Cambiaste precios mientras se preparaba la revisión: vuelve a pulsar Guardar cambios para revisarlos todos.» | Se modificó el lote mientras se preparaba la vista previa. | Vuelve a pulsar Guardar cambios. |

Si no cargan las opciones de filtros, usa **Reintentar** en su aviso; no inventes una opción a partir de un número. Para errores generales de sesión o conexión, consulta [Qué pasa si hay errores](../general/formularios-y-acciones-comunes.md#qué-pasa-si-hay-errores).

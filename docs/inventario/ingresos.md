# Registrar y consultar ingresos

Registra una factura de mercancía y sus equipos en una sede. El ingreso conserva los datos comunes de compra y crea cada unidad en el inventario.

> **Quién puede hacerlo:** Super Administrador, Administrador, Administrador de Punto y Bodeguero. Un Vendedor necesita el permiso extra indicado en «Qué ve cada rol».
> **Dónde está:** menú lateral → Inventario → Ingresos (`/inventario/ingresos`).

## Antes de empezar

Necesitas un proveedor, una sede, las referencias y las categorías de los equipos. Las listas del formulario ofrecen opciones activas. Debe existir una versión vigente de los [parámetros de precio](precios.md), que proporciona la ganancia cuando la de un equipo queda vacía.

Ten a mano el número de factura y los IMEI. Un IMEI no puede repetirse dentro del ingreso ni existir ya en el inventario, aunque el equipo anterior esté anulado. El sistema asigna el **No. de movimiento** y el **No. interno** de cada equipo; no los escribes tú.

En este formulario el IMEI debe tener entre 14 y 16 dígitos. Si el identificador de tu equipo no cumple ese formato, consulta a tu administrador.

El ingreso se guarda completo o no se guarda: si falla una unidad, no quedan registradas las otras del mismo envío. No hay edición ni acción de anular el ingreso en estas pantallas; revisa los datos comunes antes de confirmar.

## Cómo consultar los ingresos

1. Abre **Ingresos**.
2. Revisa **No. de movimiento**, **Proveedor**, **Sucursal**, **Fecha de ingreso**, **Equipos** y **Factura**.
3. Si eres Super Administrador o Administrador, usa **Sucursal** y **Ciudad** en **Filtros de ingresos** para acotar el listado.
4. Usa **Limpiar filtros** para quitar ambos filtros.
5. Cambia de página con los controles del [listado](../general/listados-filtros-y-paginacion.md).
6. Pulsa el icono **Ver** de la fila para abrir el ingreso.

Administrador de Punto y Bodeguero consultan los ingresos registrados en su sede; no tienen esos filtros globales. El alcance del ingreso depende de su sede de registro, no de la ubicación actual de los equipos que nacieron allí. No hay buscador por número de movimiento o factura en este listado.

Cambiar un filtro vuelve a la primera página. Si no hay coincidencias, aparece **«Ningún ingreso coincide con el filtro.»**; sin filtros, **«Todavía no hay ingresos.»**.

## Cómo registrar un ingreso

1. Pulsa **Registrar ingreso**.
2. Elige **Proveedor**.
3. Elige **Sede** si tienes alcance global. Para los roles de sede aparece fija la que tienes asignada.
4. Escribe **Número de factura**.
5. Revisa **Fecha de ingreso**; el formulario comienza con la fecha de hoy de tu dispositivo y permite cambiarla.
6. Completa los datos opcionales de la cabecera si los necesitas.
7. En el primer equipo, escribe **IMEI**.
8. Elige **Referencia**.
9. Elige **Categoría**.
10. Escribe **Costo**.
11. Completa sus datos opcionales; para iPhone de Exhibición incluye la batería.
12. Si la factura incluye otra unidad, pulsa **Agregar equipo** y completa sus campos.
13. Revisa todas las unidades y pulsa **Guardar**. Durante el envío dice **Guardando…**.

Al guardar correctamente se cierra el diálogo y se recarga el listado, conservando los filtros y la página. El ingreso nuevo puede no aparecer en esa vista. Los equipos quedan en la sede indicada, con estado operativo **Disponible**, sus datos de compra y los consecutivos asignados por el sistema.

**Quitar equipo** elimina esa fila antes de registrar, no borra una unidad que ya existe. No puedes quitar la única fila: el ingreso necesita al menos un equipo. **Cancelar** cierra el formulario sin registrar. Durante el guardado se bloquean Guardar, Cancelar, Agregar equipo y Quitar equipo.

### Campos comunes de la factura

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Proveedor | Proveedor de la compra; la lista muestra los activos. | Sí. |
| Sede | Sucursal o bodega donde ingresa la mercancía. Globales eligen una activa; roles de sede usan la propia. | Sí. |
| Número de factura | Número del documento del proveedor, hasta 50 caracteres. | Sí. |
| Número de guía | Número de guía, hasta 50 caracteres. | No. |
| Fecha de pedido | Fecha en que se pidió la mercancía. | No. |
| Fecha de ingreso | Fecha de entrada que se copiará a los equipos. | Sí. |
| Notas | Observaciones generales del ingreso. | No. |

### Campos de cada equipo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| IMEI | De 14 a 16 dígitos, sin puntos ni guiones; distinto de los demás equipos. | Sí. |
| Referencia | Modelo de la unidad, de las referencias activas. | Sí. |
| Categoría | Categoría activa, como Nuevo o Exhibición. | Sí. |
| Costo | Costo de compra en pesos, cero o más. | Sí. |
| Ganancia | Ganancia definida para esta unidad, cero o más. Vacía usa la ganancia por defecto vigente; escribir cero conserva cero. | No. |
| RAM | Dato de memoria, hasta 30 caracteres. | No. |
| Almacenamiento | Dato de capacidad, hasta 30 caracteres. | No. |
| Color | Color, hasta 40 caracteres. | No. |
| Batería (%) | Entero entre 0 y 100. | Sí para iPhone de Exhibición; opcional en los otros casos. |
| Notas del equipo | Observaciones de esta unidad. | No. |

Costo y Ganancia admiten hasta 12 dígitos en total, con hasta dos decimales. Escribe el número sin símbolo de moneda ni separadores de miles; usa punto para los decimales. Estos campos envían el texto que escribes, no tienen la conversión de las celdas de precio del listado.

Si tienes permiso para consultar parámetros, la ayuda de Ganancia puede mostrar el valor por defecto. Aunque no muestre la cifra, dejar Ganancia vacía pide que el servidor aplique la versión vigente.

La cifra de ayuda usa la fecha del dispositivo; el importe aplicado usa la fecha configurada para el sistema (Bogotá por defecto). Cerca de medianoche, si tu dispositivo usa otra zona horaria, las cifras pueden diferir.

## Cómo revisar un ingreso registrado

1. Pulsa **Ver** en el listado.
2. En **Ingreso …**, comprueba **Datos del ingreso**: número de movimiento, proveedor, sede, factura, guía, fechas y notas.
3. Revisa **Auditoría**: estado del registro y fechas de creación y actualización.
4. En **Equipos del ingreso**, revisa No. interno, IMEI, Referencia, Color y Costo cuando tu acceso lo permita.
5. Para abrir la [ficha de una unidad](equipo-detalle.md), pulsa su icono **Ver**.
6. Pulsa **Volver a Ingresos** para regresar.

La tabla de unidades tiene paginación propia, pero pertenece al mismo ingreso. Si un equipo ya se trasladó a otra sede, puedes seguir viendo su vínculo en el ingreso original; abrir su ficha sigue sujeto al alcance de inventario de tu usuario.

No hay un botón Editar ni Anular en el detalle del ingreso. Las correcciones admitidas de costo, ganancia y datos de una unidad se hacen en su [ficha](equipo-detalle.md#cómo-editar-la-ficha), con el permiso correspondiente; no reescriben la cabecera original de la factura. No vuelvas a registrar la misma mercancía para corregirla: sus IMEI ya existen.

## Cómo imprimir el comprobante del ingreso

1. Abre el ingreso registrado.
2. Pulsa **Imprimir**.
3. En **Documento imprimible**, revisa la hoja **Ingreso de mercancía**.
4. Pulsa **Imprimir** para abrir la impresión del navegador.
5. Confirma la impresora o el destino PDF que tu navegador ofrezca.
6. Pulsa **Volver al detalle** para regresar.

La hoja incluye el movimiento completo, no solo la página visible de equipos: número, fecha de ingreso, **Origen** (proveedor), **Destino** (sede), **Elaborado por**, cantidad y lista de unidades con No. interno, IMEI, Marca y Referencia. Incluye las Observaciones generales y espacios **Entregado por** y **Recibido por** para firmar a mano.

No incluye costo ni ganancia, incluso para administradores. No captura firmas digitales ni descarga automáticamente un PDF del servidor. El acceso a esta impresión es el del ingreso; no depende del permiso separado para exportar el listado de Equipos.

## Qué ve cada rol

Permisos de base, sin extras:

| Rol | Consultar / registrar / imprimir | Sede de registro y alcance del listado |
|---|---|---|
| Super Administrador | Sí | Puede elegir sede; consulta global. |
| Administrador | Sí | Puede elegir sede; consulta global. |
| Administrador de Punto | Sí | Su sede asignada. |
| Vendedor | No | No ve Ingresos por su rol. |
| Bodeguero | Sí | Su ubicación asignada. |

El Vendedor puede acceder con **Registrar y consultar ingresos**, que exige **Ver costo y ganancia** y **Consultar proveedores**. El permiso extra no amplía su alcance por sede. Registrar ingresos no concede edición de la ficha ni publicación de parámetros.

Los cuatro roles que entran de base ven costo y proveedor. El comprobante en papel omite costo para cualquiera. Consulta [Permisos extra](../administracion/usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra) para su asignación.

## Relación con otros módulos

**Necesitas antes:**

- [Proveedor](../administracion/proveedores.md): origen de la compra.
- [Sucursal o bodega](../administracion/sucursales.md): sede donde se recibe la mercancía.
- [Referencias](../administracion/referencias.md) y [categorías de equipo](../administracion/categorias-de-equipo.md): opciones de cada unidad.
- [Parámetros de precios](precios.md): versión vigente para la ganancia por defecto.
- Lecturas de apoyo, según la tarea que realices: [Exportar a Excel e imprimir](../general/exportar-e-imprimir.md); [Qué pasa si hay errores](../general/formularios-y-acciones-comunes.md#qué-pasa-si-hay-errores); [Estados operativos](../administracion/estados-operativos.md); [Marcas](../administracion/marcas.md); [Tipos de producto](../administracion/tipos-de-producto.md); [Lista completa de permisos extra](../administracion/usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra); [Usuarios](../administracion/usuarios.md).

**Esto afecta a:**

- [Equipos](equipos.md): el ingreso crea las unidades en la sede y las deja Disponibles.
- [Ficha del equipo](equipo-detalle.md): conserva su origen y permite las correcciones admitidas.
- [Traslados](traslados.md) y [Nueva venta](../ventas/nueva-venta.md): usan los equipos existentes, sin volver a ingresarlos.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Completa el proveedor, la sede y la referencia y categoría de cada equipo antes de guardar.» | Falta una selección obligatoria. | Revisa cabecera y cada grupo de equipo marcado. |
| «El IMEI debe tener entre 14 y 16 dígitos.» | El formato no pasa la validación. | Escribe los dígitos completos sin puntos ni guiones. |
| «El IMEI ya viene en el equipo #N de este mismo ingreso.» | Repetiste una unidad en el formulario; N identifica la primera fila. | Corrige el IMEI o quita la fila duplicada. |
| «Ya existe un equipo registrado con el IMEI …: el IMEI es único (8.10).» | Alguno de los IMEI ya está registrado. | Revisa la unidad en Equipos; no intentes crearla de nuevo. |
| «El porcentaje de batería es obligatorio para un iPhone de exhibición.» | Falta batería en una unidad con esa referencia y categoría. | Revisa los iPhone de Exhibición del lote; el aviso puede aparecer arriba sin señalar una fila. |
| «La batería debe ser un número entero entre 0 y 100.» | El porcentaje escrito no es válido. | Usa un entero del rango permitido. |
| «Solo puedes registrar ingresos en la sucursal que tienes asignada.» | Se intentó registrar en otra sede con alcance local. | Usa tu sede; un permiso extra no cambia ese alcance. |
| «Tu rol todavía no puede consultar proveedores; el registro de ingresos requiere ese permiso.» | La consulta de proveedores fue denegada. | Pide revisar los permisos o el desfase del servidor; ese aviso no ofrece Reintentar. |

Ante un error de validación, corrige sin asumir que las demás filas ya entraron: el lote es conjunto. Si falla un catálogo por conexión, usa **Reintentar** y espera a cargarlo. Para otros errores, consulta [Qué pasa si hay errores](../general/formularios-y-acciones-comunes.md#qué-pasa-si-hay-errores).

# Exportar a Excel e imprimir

Varias pantallas te dejan **bajar un archivo de Excel** con lo que tienes en pantalla o **imprimir** un documento (o guardarlo como PDF). Aquí se explican los patrones comunes y sus excepciones: no todas las pantallas descargan o imprimen el mismo tipo de documento.

> **Quién puede hacerlo:** depende de la pantalla y del permiso. Si no tienes el permiso, el botón no aparece.
> **Dónde está:** en el pie de la tarjeta de filtros (Equipos), en el encabezado de la pantalla (Ventas, fichas de detalle, tableros) o dentro de cada sección de un tablero.

## Antes de empezar

- El archivo de Excel lo **arma el sistema** y se baja a tu computador; tu navegador decide en qué carpeta queda y cómo se llama el archivo lo decide el sistema.
- Exportar los listados de **Ventas** y **Equipos** toma todos los resultados de los filtros, no solo la página visible: si hay 156 resultados en seis páginas, el archivo trae los 156. La hoja de inventario también toma el conjunto filtrado, con su propio tope. Los documentos de una ficha corresponden a ese registro y los tableros imprimen el contenido ya cargado. **El Informe de metas imprime solo la página actual**, con una indicación de página y total. Mira [Listados, filtros y paginación](listados-filtros-y-paginacion.md).
- Los botones para exportar los listados de Ventas y Equipos se ofrecen solo con resultados. El **Imprimir** de los tableros permanece disponible incluso durante la carga o con errores; verifica el contenido antes de usarlo.
- Lo que no puedes ver en pantalla tampoco sale en el archivo: por ejemplo, las columnas de **costo** no existen para quien no ve el costo, y el **proveedor** no sale para quien no ve proveedores. Mira [Roles y permisos](roles-y-permisos.md).
- Para imprimir, el sistema **no genera PDF**: abre la ventana de impresión del navegador. Desde ahí eliges tu impresora o la opción de guardar como PDF.

## Dónde puedes exportar a Excel

| Pantalla | Botón | Qué baja | Permiso que lo abre (roles que lo traen de base) |
|---|---|---|---|
| Ventas → Ventas | **Exportar Excel** (encabezado) | El listado de ventas con los filtros | «Exportar el listado de ventas» (Super Administrador, Administrador, Administrador de Punto, Vendedor) |
| Inventario → Equipos | **Exportar Excel** (pie de la tarjeta de filtros) | Los equipos con los filtros | «Exportar e imprimir el inventario» (los cinco roles) |
| Ventas → Cuadre de caja → ficha de un cuadre | **Exportar Excel** | El cuadre | «Cuadres de caja» (Super Administrador, Administrador, Administrador de Punto) |
| Dashboard e Informes → Ventas | **Exportar Excel** dentro de «Evolución del periodo» (serie) y otro dentro del desglose | La serie o el desglose del tablero | «Tablero de ventas» (Super Administrador, Administrador, Administrador de Punto, Vendedor) |

## Cómo exportar a Excel

1. Pon los filtros que quieres (o déjalos vacíos para bajar todo).
2. Haz clic en **Exportar Excel**.
3. El botón dice «Exportando…» mientras el sistema arma el archivo. **No hagas clic otra vez**: mientras baja, el botón no responde, y las exportaciones del listado de Ventas y del inventario quedan registradas. Las descargas de la serie/desglose del tablero y del cuadre no tienen ese registro de auditoría.
4. Cuando termina, el archivo se descarga solo.

Al terminar verás: el archivo en la carpeta de descargas de tu navegador.

### Reglas que conviene saber

- **Tope de filas de los listados de Ventas y Equipos.** Estos archivos pueden tener hasta **20.000 filas**. Si tu filtro deja más, el sistema no lo baja y te dice cuántas filas hay y cuál es el tope. Acota el rango de fechas o los filtros. En Equipos el aviso te sugiere filtrar por estado, porque el inventario incluye los equipos vendidos.
- El tope de 20.000 filas anterior no es una validación común a todas las descargas: el tablero exporta su serie o desglose, y el cuadre su documento.
- **Límite de velocidad.** El límite por defecto es de 10 descargas por minuto. El límite de tu instalación puede variar; sigue el tiempo de espera que indique el aviso. Si te pasas, el sistema te dice cuánto esperar.
- **Cambios sin guardar (solo Equipos).** Si en la tabla de Equipos editaste precios y no los has guardado, al exportar aparece el diálogo «Exportar sin los cambios»: el archivo lleva los precios guardados y los cambios sin guardar no entran. Elige **Exportar igual** para seguir o **Cancelar**. Tus cambios no se pierden.
- Si cambias un filtro mientras se descarga, un error de la descarga anterior no se te muestra en los filtros nuevos.

## Dónde puedes imprimir

| Pantalla | Botón | Qué imprime |
|---|---|---|
| Inventario → Equipos | **Imprimir / PDF** (pie de la tarjeta de filtros) | La hoja «Inventario para imprimir» con los filtros |
| Inventario → Ingresos → ficha de un ingreso | **Imprimir** | El documento del ingreso (con espacio para firmas) |
| Inventario → Traslados → ficha de un traslado | **Imprimir** | El documento del traslado (con espacio para firmas) |
| Ventas → Ventas (icono de impresora en la fila) y ficha de la venta | **Imprimir** | El comprobante de la venta. Solo aparece si tienes el permiso «Registrar ventas» (Super Administrador, Administrador, Administrador de Punto y Vendedor lo traen de base) |
| Ventas → Cuadre de caja → ficha de un cuadre | **Imprimir** | El cuadre |
| Metas Comerciales → ficha de una meta | **Imprimir** | La meta |
| Dashboard e Informes → cada tablero (Ventas, Inventario, Metas, Financieras) | **Imprimir** (encabezado) | La pantalla tal como está, sin volver a pedir los datos |

## Cómo imprimir un documento

Para las fichas y la hoja de inventario:

1. Abre la ficha (o el listado de Equipos) y haz clic en **Imprimir** (o **Imprimir / PDF**). Se abre la vista del documento, en la misma pestaña.
2. Revisa el documento en pantalla. Arriba hay un enlace para volver («Volver al detalle», «Volver a Equipos») y el botón **Imprimir**.
3. Haz clic en **Imprimir**. Se abre la ventana de impresión de tu navegador.
4. Elige tu impresora o «Guardar como PDF» y confirma.

Para los cuatro tableros, revisa las secciones cargadas y haz clic una vez en **Imprimir**: abre directamente la ventana del navegador, sin una vista intermedia. El Informe de metas imprime solo la página actual.

Al terminar verás: el documento impreso o el PDF guardado. El menú lateral y la barra superior no salen en el papel; tampoco los controles marcados por el sistema para excluirlos. **No se excluyen todos los errores ni todos los botones**: un tablero con secciones que fallaron puede imprimir sus avisos de error. Espera o reintenta antes de imprimir.

### Reglas de las hojas para imprimir

- **Equipos:** la hoja muestra los precios **guardados**. Si tienes cambios sin guardar, el diálogo «Imprimir sin guardar» te avisa que se pierden si abres la hoja. Elige **Abrir la hoja** para continuar o **Cancelar** para conservarlos. El botón **Imprimir** de la hoja aparece cuando hay datos y ya cargaron los nombres de los filtros; mientras tanto ves «Preparando los nombres de los filtros…».
- **Tope para imprimir:** la hoja de inventario admite hasta **5.000 filas**. Si te pasas: «La vista para imprimir tiene N filas y el tope es 5000. Acota los filtros o usa Exportar Excel.».
- **Tableros:** imprimen el contenido ya cargado, sin volver a pedir datos. Si quieres otras cifras, cambia los filtros antes de imprimir. En **Informe de metas**, cambia de página e imprime cada una por separado si necesitas todas: cada hoja identifica la página y el total.
- Los documentos de ingreso, traslado y comprobante de venta traen líneas de firma para firmar a mano.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «La exportación tiene N filas y el tope es 20000. Acota el rango de fechas o los filtros.» | Tu filtro deja demasiadas filas | Acota las fechas o los filtros y vuelve a exportar |
| «La exportación tiene N filas y el tope es 20000. El inventario incluye los equipos vendidos: filtra por estado o acota los demás filtros.» | Lo mismo, en Equipos | Filtra por estado |
| Un mensaje de «Hiciste demasiadas solicitudes seguidas.» con los segundos que faltan | Pediste demasiadas descargas en un minuto | Espera y vuelve a intentar |
| «No se pudo descargar el archivo. Revisa tu conexión e inténtalo de nuevo.» | El archivo no llegó | Revisa tu conexión y repite |
| «El navegador no dejó guardar el archivo. Revisa los permisos de descarga e inténtalo de nuevo.» | El archivo llegó, pero tu navegador lo bloqueó | Permite las descargas de este sitio en tu navegador |
| «La vista para imprimir tiene N filas y el tope es 5000. Acota los filtros o usa Exportar Excel.» | Demasiadas filas para imprimir | Acota los filtros o exporta a Excel |
| «No tienes permiso para acceder a esta sección.» al abrir una hoja | Tu usuario no tiene el permiso de esa hoja | Pide a un administrador que revise tus permisos |

El aviso combina «Hiciste demasiadas solicitudes seguidas.» con «Vuelve a intentarlo en N segundos.»; N es el tiempo que debes esperar.

## Qué ve cada rol

| Rol | Exporta ventas | Exporta e imprime inventario | Cuadre (exportar / imprimir) | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | |
| Administrador | Sí | Sí | Sí | |
| Administrador de Punto | Sí | Sí | Sí | |
| Vendedor | Sí | Sí | No | En el archivo de ventas no existen las columnas de costo |
| Bodeguero | No | Sí | No | En el inventario, el proveedor y el costo salen porque su rol los ve |

## Relación con otros módulos

**Necesitas antes:**
- Tener datos a la vista: [Listados, filtros y paginación](listados-filtros-y-paginacion.md).
- Lecturas de apoyo, según la tarea que realices: [Proveedores](../administracion/proveedores.md).

**Esto afecta a:**
- [Equipos](../inventario/equipos.md) y [Imprimir inventario](../inventario/imprimir-inventario.md).
- [Ventas](../ventas/ventas.md) y [Comprobante de venta](../ventas/comprobante-de-venta.md).
- [Cuadres de caja](../ventas/cuadres-de-caja.md).
- [Ingresos](../inventario/ingresos.md) y [Traslados](../inventario/traslados.md).
- [Metas](../metas/metas.md).
- [Tablero de ventas](../dashboard/tablero-de-ventas.md), [Tablero de inventario](../dashboard/tablero-de-inventario.md), [Informe de metas](../dashboard/informe-de-metas.md) e [Informe de financieras](../dashboard/informe-de-financieras.md).

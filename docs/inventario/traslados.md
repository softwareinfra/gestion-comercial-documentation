# Trasladar equipos entre sedes

Crea un envío de equipos entre sucursales o bodegas, registra su despacho y confirma en destino la recepción o el rechazo.

> **Quién puede hacerlo:** Super Administrador, Administrador, Administrador de Punto y Bodeguero. El Vendedor necesita **Gestionar traslados** como permiso extra.
> **Dónde está:** menú lateral → Inventario → Traslados (`/inventario/traslados`).

## Antes de empezar

El traslado usa equipos ya registrados; no crea unidades nuevas. Necesita origen y destino distintos, un motivo y al menos un equipo en el origen que pueda cambiar a En traslado. El formulario ofrece sedes activas.

Distingue el **estado del traslado** del **estado de sus equipos**. Al crear, el traslado queda **Creado**, pero sus equipos ya quedan **En traslado** y dejan de estar disponibles para venta. Su ubicación sigue siendo el origen hasta la recepción.

Aunque la ayuda mencione el despacho, las unidades quedan bloqueadas **al crear** el traslado. No esperes al despacho para considerarlas bloqueadas.

El traslado no tiene edición de cabecera o de sus equipos después de crearlo. Antes del despacho puedes anularlo con motivo; después, el cierre corresponde a recibir o rechazar en destino.

## Cómo consultar los traslados

1. Abre **Traslados**.
2. Revisa **Código**, **Origen**, **Destino**, **Estado**, **Fecha de creación** y **Equipos**.
3. Si tienes alcance global, usa **Sucursal** o **Ciudad** en **Filtros de traslados**.
4. Usa **Limpiar filtros** para quitar ambos.
5. Cambia de página con los controles del [listado](../general/listados-filtros-y-paginacion.md).
6. Pulsa el icono **Ver** de una fila para abrirla.

El Super Administrador y el Administrador consultan globalmente. Un usuario de sede ve los traslados donde su sede es **origen o destino**, incluso antes de recibirlos. Ver un traslado no permite hacer las acciones de la contraparte.

Los filtros globales también buscan en ambos extremos: Sucursal coincide con origen o destino; Ciudad, con la ciudad de cualquiera de ellos. Si combinas los dos filtros, sus coincidencias pueden estar en extremos distintos del mismo traslado. Cambiar filtros vuelve a la primera página.

No hay buscador por código ni filtro de Estado en este listado. Origen y Destino muestran el nombre y el tipo de sede.

## Cómo crear un traslado

1. Pulsa **Crear traslado**. Se abre una página propia, no un diálogo.
2. Elige **Origen** si eres Super Administrador o Administrador; los usuarios de sede lo tienen fijo en su ubicación asignada.
3. Elige **Destino** entre las otras sedes activas.
4. Escribe **Motivo**, obligatorio y de hasta 500 caracteres.
5. Completa **Observaciones** si las necesitas.
6. En **Equipos a trasladar**, marca la casilla de cada unidad que enviarás.
7. Comprueba el contador y los IMEI seleccionados.
8. Pulsa **Crear traslado** al pie. Durante el envío dice **Creando…**.

Al crear correctamente se abre el detalle del nuevo traslado. El código lo asigna el sistema. El traslado queda Creado; las unidades quedan En traslado, aún ubicadas en el origen. El guardado es conjunto: si una unidad falla, no se crea un traslado parcial.

Para encontrar una unidad, escribe su IMEI completo en **IMEI exacto…** y espera a que se aplique. El selector muestra Seleccionar, No. interno, IMEI y Referencia. Cambiar de página o filtrar por IMEI conserva los equipos seleccionados. Para quitar uno, desmarca su casilla o pulsa su IMEI en la selección (**Quitar de la selección**).

Cambiar Origen vacía la selección anterior y limpia la página y el filtro de IMEI del selector. **Cancelar** regresa al listado sin crear. La selección y los textos no se guardan como un borrador para volver más tarde.

El selector puede ofrecer un equipo **Reservado**, pero ese equipo no puede pasar a **En traslado**. Revisa su estado en la ficha antes de elegirlo; no cambies el estado para eludir una reserva.

## Cómo revisar el detalle

En **Datos del traslado** aparecen Código, Origen, Destino, Estado, Motivo y Observaciones. **Auditoría** muestra el estado del registro, quién lo creó y cuándo, y los datos de despacho, recepción o rechazo cuando existen.

En **Equipos del traslado**, la columna **Equipo** muestra un identificador precedido de #; no es el No. interno de la unidad. IMEI identifica la unidad seleccionada para ese traslado. Pulsa **Ver** para abrir su [ficha](equipo-detalle.md); la ficha sigue su propio alcance de inventario, así que la sede de destino puede ver el traslado antes de tener acceso a la unidad aún ubicada en origen. Usa la paginación de la tabla para otras unidades.

**Volver a Traslados** regresa al listado. Las acciones que aparecen arriba dependen del estado y de si trabajas en origen o destino. Motivo conserva el de creación: el motivo posterior de un rechazo o anulación se registra en la auditoría del proceso, pero no reemplaza ese campo de la ficha. Esta pantalla no ofrece una tabla de historial de eventos como la ficha del equipo.

## Qué cambia en cada paso

Los nombres son los de los estados de fábrica; Administración puede cambiar sus nombres visibles.

| Acción | Estado del traslado al terminar | Estado de equipos | Ubicación de equipos |
|---|---|---|---|
| Crear traslado | Creado | En traslado; no disponibles para venta | Origen |
| Despachar | En tránsito | Siguen En traslado | Sigue origen |
| Recibir | Recibido | Disponible | Cambia a destino |
| Rechazar | Rechazado | Disponible | Sigue origen |
| Anular antes del despacho | Anulado; registro Anulado | Disponible | Sigue origen |

No hay que pasar manualmente por un botón Pendiente de despacho o Despachado. El despacho completa sus pasos internos y deja el traslado En tránsito. Las acciones del destino se ofrecen en En tránsito; Recibido, Rechazado y Anulado no ofrecen otro avance.

La recepción no crea otro equipo ni cambia la fecha de ingreso de la unidad: mueve la existente a destino y registra el cambio. Por eso sus días en inventario no se reinician con el traslado.

## Cómo despachar

> **Quién puede hacerlo:** usuarios con Gestionar traslados de la sede de origen, o Super Administrador y Administrador.

1. Abre el traslado Creado o Pendiente de despacho.
2. Pulsa **Despachar** cuando corresponda registrar la salida.
3. Revisa el aviso y confirma con **Despachar** dentro del diálogo.

Al terminar se cierra el diálogo y se recarga el detalle. El traslado queda En tránsito y se registran **Despachado por** y **Despachado el**. Sus equipos ya estaban bloqueados desde la creación, y siguen contabilizados en el origen hasta recibir.

## Cómo recibir en destino

> **Quién puede hacerlo:** usuarios con Gestionar traslados de la sede de destino, o Super Administrador y Administrador.

1. Abre el traslado En tránsito.
2. Comprueba las unidades recibidas contra los IMEI del traslado.
3. Pulsa **Recibir**.
4. Confirma con **Recibir** dentro del diálogo.

Al terminar se cierra el diálogo y se recarga el detalle. El traslado queda Recibido, con **Recibido por** y **Recibido el**. Las unidades pasan a la ubicación de destino y quedan Disponibles. El movimiento se realiza como un conjunto; no hay recepción parcial por unidad en esta acción.

## Cómo rechazar en destino

> **Quién puede hacerlo:** usuarios con Gestionar traslados de la sede de destino, o Super Administrador y Administrador.

1. Abre el traslado En tránsito.
2. Pulsa **Rechazar**.
3. Escribe **Motivo** para explicar el rechazo.
4. Confirma con **Rechazar el traslado**.

Al terminar se cierra el diálogo y se recarga el detalle. El traslado queda Rechazado, con **Rechazado por** y **Rechazado el**. Los equipos vuelven a Disponible en origen; su ubicación no había cambiado aún. El rechazo es definitivo y no convierte el mismo traslado en otro envío: coordina también la devolución física de mercancía, que este registro no transporta por ti.

No uses Recibir primero si quieres rechazar: una vez Recibido, este traslado no admite rechazo. **Cancelar** en el diálogo cierra sin rechazar.

## Cómo anular antes del despacho

> **Quién puede hacerlo:** usuarios con Gestionar traslados de la sede de origen, o Super Administrador y Administrador.

1. Abre el traslado Creado o Pendiente de despacho.
2. Pulsa **Anular**.
3. Escribe **Motivo**.
4. Revisa que estás anulando el envío correcto.
5. Confirma con **Anular definitivamente**.

Al terminar se cierra el diálogo y se recarga el detalle. El traslado y su registro quedan Anulados; los equipos vuelven a Disponible en origen. Se conserva el traslado, no se borra ni se reactiva para editarlo. **Cancelar** cierra el aviso sin anular.

Una vez despachado, la opción de anular no está disponible: el destino debe recibir o rechazar según lo ocurrido. La anulación de este envío no anula los registros de sus equipos.

## Cómo adjuntar y abrir documentos

1. Abre el detalle del traslado.
2. En **Documentos**, usa **Agregar documento**.
3. Elige un PDF o una imagen JPG, JPEG, PNG o WEBP, de hasta **5 MB**.
4. Espera la carga: se envía al elegir el archivo, sin otro botón Guardar.
5. Comprueba que se actualice la lista.
6. Pulsa **Abrir** junto al documento para consultarlo en otra pestaña.

Puedes adjuntar varios documentos, uno por selección. La lista muestra nombre, tamaño y fecha. No hay una acción para borrar o reemplazar un adjunto en esta pantalla. Se permite adjuntar a un traslado de tu alcance aun cuando ya esté cerrado; adjuntar no cambia su estado.

Si **Abrir** está deshabilitado, el documento no tiene un enlace disponible. Al abrir, la aplicación actualiza la lista para obtener un enlace actual; no conviene conservar un enlace antiguo como acceso permanente. Si el documento no abre, revisa si el navegador bloqueó la nueva pestaña y vuelve a intentar; si sigue fallando, avisa a tu administrador.

## Cómo imprimir el traslado

1. Abre el traslado.
2. Pulsa **Imprimir**.
3. En **Documento imprimible**, revisa la hoja **Traslado entre sedes**.
4. Pulsa **Imprimir** para abrir el diálogo del navegador.
5. Elige la impresora o el destino PDF que ofrezca el navegador.
6. Usa **Volver al detalle** para regresar.

La hoja incluye el traslado completo, no solo los equipos de la página visible: código, **Fecha de creación**, Origen, Destino, Elaborado por, cantidad de equipos, No. interno, IMEI, Marca, Referencia y Observaciones. No incluye costo ni ganancia. Los espacios **Despachado por** y **Recibido por** quedan para firmar a mano; no son una captura de firma digital.

La fecha de la cabecera es la de creación del traslado, no la de despacho ni recepción. Imprimir no despacha ni recibe la mercancía. El acceso es el del traslado; no requiere el permiso separado de exportar el listado de Equipos.

## Qué ve cada rol

| Rol | Consulta / crea / documentos / impresión por su rol | Acciones sobre mercancía |
|---|---|---|
| Super Administrador | Sí; consulta global y elige origen | Puede operar ambos extremos. |
| Administrador | Sí; consulta global y elige origen | Puede operar ambos extremos. |
| Administrador de Punto | Sí; traslados de su sede como origen o destino; crea desde la propia | Despacha/anula si es origen; recibe/rechaza si es destino. |
| Vendedor | No | Necesita Gestionar traslados como extra; conserva las restricciones de sede. |
| Bodeguero | Sí; traslados de su ubicación como origen o destino; crea desde la propia | Despacha/anula si es origen; recibe/rechaza si es destino. |

Las acciones también dependen del estado, como explican los pasos anteriores. La lista de documentos y el comprobante no tienen columnas de costo; el contenido de cada adjunto depende del archivo que subas. Gestionar traslados no abre el dato de costo por sí solo. El permiso extra no cambia el alcance de sede. La lectura de sedes de apoyo permite elegir otros destinos, sin conceder sus operaciones.

## Relación con otros módulos

**Necesitas antes:**

- [Sucursales y bodegas](../administracion/sucursales.md): origen y destino distintos.
- [Ingresos](ingresos.md) y [Equipos](equipos.md): las unidades deben estar registradas en el origen.
- [Permisos extra](../administracion/usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra): cuando tu rol no trae Gestionar traslados.
- Lecturas de apoyo, según la tarea que realices: [Exportar a Excel e imprimir](../general/exportar-e-imprimir.md); [Estados operativos](../administracion/estados-operativos.md); [Usuarios](../administracion/usuarios.md); [Ficha del equipo](equipo-detalle.md).

**Esto afecta a:**

- [Equipos y su ficha](equipo-detalle.md): la creación bloquea su disponibilidad; recibir cambia ubicación y deja Disponible. Los cambios del equipo se registran en su historial.
- [Nueva venta](../ventas/nueva-venta.md): no uses equipos En traslado para vender; deben terminar el recorrido correspondiente.
- [Tablero de inventario](../dashboard/tablero-de-inventario.md): la ubicación de los equipos cambia al recibir, no al crear o despachar.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Ningún traslado coincide con el filtro.» | Los filtros no encontraron registros. | Usa Limpiar filtros. |
| «Todavía no hay traslados.» | El listado sin filtros está vacío en tu alcance. | Revisa la sede y si el traslado ya fue creado. |
| «No hay equipos disponibles en la sede de origen.» | El selector no encontró equipos vendibles allí. | Verifica origen y los estados en Equipos. |
| «Ningún equipo disponible coincide con el filtro.» | No hay coincidencia del IMEI exacto entre los equipos del selector. | Revisa el IMEI o vacía ese filtro. |
| «El destino debe ser distinto del origen (8.8).» | Elegiste la misma sede para ambos extremos. | Elige otra sede activa. |
| «No hay otra sede activa a la que trasladar; un traslado necesita una sede de destino distinta del origen.» | No se ofrecen destinos activos diferentes. | Pide revisar las sedes; Crear traslado permanece deshabilitado. |
| «Tu rol todavía no puede enumerar las sedes de destino; crear un traslado requiere ese permiso.» | El catálogo recibido no incluye otra sede y la pantalla lo interpreta como falta de alcance de lectura. | Pide revisar permisos, catálogo y versión del servidor; también puede haber una sola sede en el negocio. |
| «El traslado ya avanzó de estado: la información se actualizó.» | Otro envío o usuario cambió el estado antes de tu acción. | Revisa la ficha recargada antes de actuar otra vez. |
| «El documento supera el máximo de 5 MB.» | El adjunto excede el tamaño permitido. | Reduce el tamaño y vuelve a seleccionarlo. |
| «Solo se aceptan documentos PDF o imágenes (jpg, jpeg, png, webp).» | El formato del adjunto no es permitido. | Exporta el documento a uno de esos formatos; cambiar solo el nombre no cambia el archivo. |
| «El documento ya no tiene un enlace disponible; la lista se actualizó.» | La nueva consulta no pudo entregar un enlace al adjunto. | Revisa la lista actual y reporta si sigue sin abrir. |

Si el equipo ya no está en origen o dejó de estar disponible desde que lo seleccionaste, el servidor rechaza la creación: revisa su ficha y la selección. Si una acción falla por un estado de equipo modificado, no fuerces el cambio desde otra pantalla; pide revisar el traslado y sus unidades. Para errores generales, consulta [Qué pasa si hay errores](../general/formularios-y-acciones-comunes.md#qué-pasa-si-hay-errores).

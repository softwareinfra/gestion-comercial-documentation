# Cómo consultar ventas y registrar abonos

Busca una venta, abre sus datos y revisa lo que se cobró. Desde la ficha puedes imprimir, pedir cambios y registrar abonos de cartera propia según tus permisos.

> **Quién puede hacerlo:** Super Administrador, Administrador, Administrador de Punto y Vendedor consultan ventas. El Bodeguero necesita «Consultar ventas» efectivo.
> **Dónde está:** menú lateral → Ventas → Ventas.

## Antes de empezar

El listado incluye ventas activas y anuladas. Una anulada permanece para consulta. La modificación y la anulación se tramitan por [solicitud](solicitudes.md); la ficha no tiene edición directa de la venta.

La **Ganancia** es el valor de venta menos el costo conservado al vender el equipo. No incluye el recargo ni el IVA de intermediación. El precio del equipo y los datos del cliente conservados en una venta pueden diferir de sus fichas actuales.

## Cómo consultar y filtrar

1. Entra a **Ventas**.
2. Revisa las columnas **Número**, **Fecha**, **Cliente**, **Equipo**, **Modalidad**, **Valor** y **Estado**. Según tu alcance y permisos aparecen también **Ganancia**, **Sucursal** y **Acciones**.
3. Usa **Búsqueda exacta** para buscar por **Número de venta**, **Documento del cliente**, **IMEI** o **Número de contrato**.
4. Usa **Periodo y estado** para elegir fechas, **Modalidad** y **Estado**.
5. En **Comercial**, filtra por **Financiera**, si tienes su consulta, y **Medio de pago**. Los usuarios de alcance global pueden filtrar además por **Vendedor**, **Ciudad** y **Sucursal**.
6. Haz clic en el **Número** de una venta para abrir su ficha.

Cambiar un filtro vuelve a la primera página. **Limpiar filtros** retira los filtros. La consulta y la página quedan en la dirección del navegador. Para el uso general del listado, consulta [Filtros y paginación](../general/listados-filtros-y-paginacion.md).

## Cómo exportar o imprimir

1. Ajusta los filtros de las ventas que necesitas.
2. Haz clic en **Exportar Excel**, disponible si hay filas y tienes «Exportar el listado de ventas».
3. Abre el archivo descargado y revisa el período y alcance que declara.

La descarga no se limita a la página visible. Aplica los filtros y permisos de la consulta, con una ventana de fechas de hasta 366 días. Sin una ventana completa, el sistema resuelve el período de descarga; consulta el período indicado en el informe. El máximo por descarga es **20.000 filas**. Si el resultado supera ese límite, se rechaza la descarga en vez de entregar una lista cortada: acota más los filtros.

Para el documento de una venta, usa **Imprimir** en su fila o en su ficha. Sigue [Comprobante de venta](comprobante-de-venta.md).

## Cómo leer la ficha

1. Abre el **Número** de la venta.
2. Revisa **Cliente** y **Equipo**: documento, datos de contacto, IMEI, referencia y características del aparato.
3. Revisa **Datos comerciales**: modalidad, precio del equipo, precio de referencia, descuento, valor, financiera y plan de crédito.
4. Revisa **Medios de pago**: medio, valor y referencia de las líneas vigentes.
5. Si es Cartera propia, revisa **Saldo de cartera**.

La ficha muestra **Número de contrato** cuando está informado. En ventas a crédito aparecen las referencias. **Costo congelado**, **Ganancia**, **Movimientos de caja** e historial dependen de permisos. Si tienes consulta de reemplazos y la venta tuvo uno, aparece su relación; la acción **Reemplazar equipo** se explica en [Garantías](../garantias/equipos-en-garantia.md).

Si aparece «Esta venta fue modificada después de su última impresión: vuelve a imprimirla.», abre el [comprobante](comprobante-de-venta.md). La marca puede seguir visible después de imprimir: consultar el documento no la borra.

## Cómo registrar un abono de cartera propia

> **Quién puede hacerlo:** Super Administrador, Administrador y Administrador de Punto, o quien tenga «Registrar abonos de cartera propia» efectivo.

1. Abre una venta activa con modalidad **Cartera propia**.
2. Haz clic en **Registrar abono**.
3. Escribe **Valor del abono** en pesos enteros, sin centavos, mayor que cero y sin exceder el saldo pendiente.
4. Elige **Medio de pago**.
5. Escribe **Referencia** si la necesitas.
6. Haz clic en **Registrar abono**.

Al terminar se cierra el diálogo y se recarga la venta. El abono crea un ingreso de caja y reduce el saldo de cartera. No es una edición de las líneas de pago originales. No hay aquí un calendario de vencimientos ni cálculo de mora.

## Cómo guardar una imagen de soporte

1. En la ficha de una venta activa, busca la sección de imagen.
2. Haz clic en **Subir imagen** o **Reemplazar imagen**, según ya exista una.
3. Elige el archivo en **Imagen**.
4. Revisa la vista previa, el nombre y el tamaño.
5. Confirma con **Subir imagen** o **Reemplazar imagen**.

Admite JPG, JPEG, PNG o WEBP, hasta el tamaño que la pantalla llama **10 MB**. La imagen anterior se conserva al reemplazarla; se muestra la vigente. Usa **Abrir** para verla en una pestaña nueva. Si el navegador la bloquea, permite ventanas emergentes para este sitio. Una venta anulada permite consultar su imagen, pero no subir otra.

Aunque la ayuda diga «Una foto más pesada se reduce antes de subirla», esta pantalla rechaza las imágenes mayores al límite. Reduce el archivo antes de elegirlo.

## Qué ve cada rol

| Rol | Ventas que consulta | Costo y ganancia | Historial / abonos / caja dentro de la venta |
|---|---|---|---|
| Super Administrador / Administrador | Alcance global | Sí | Sí |
| Administrador de Punto | Su sucursal | Sí | Sí |
| Vendedor | Su sucursal, incluidas las ventas de otros asesores del punto | Con «Ver costo y ganancia» | Requiere los permisos extra correspondientes. |
| Bodeguero | Su ubicación con «Consultar ventas» | Por su permiso de costo, si puede consultar ventas | Requiere los permisos extra correspondientes. |

Imprimir y gestionar imágenes usan **Registrar ventas**; consultar ventas por sí solo no abre esas acciones. Pedir modificaciones o anulaciones usa **Solicitar modificaciones y anulaciones**. Los permisos extra conservan el alcance operativo del usuario.

## Relación con otros módulos

**Necesitas antes:**
- [Registrar la venta](nueva-venta.md).
- [Medios de pago](../administracion/medios-de-pago.md) activos para los abonos.
- Lecturas de apoyo, según la tarea que realices: [Exportar a Excel e imprimir](../general/exportar-e-imprimir.md); [Listados: buscar, filtrar y pasar de página](../general/listados-filtros-y-paginacion.md); [Menú lateral y navegación](../general/menu-y-navegacion.md); [Entidades financieras](../administracion/entidades-financieras.md); [Sucursales](../administracion/sucursales.md); [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md); [Ficha del equipo](../inventario/equipo-detalle.md); [Cómo consultar y registrar movimientos de caja](caja.md); [Cómo imprimir el comprobante de venta](comprobante-de-venta.md).

**Esto afecta a:**
- [Caja](caja.md): los abonos crean movimientos de ingreso.
- [Solicitudes](solicitudes.md): corrigen o anulan la venta con aprobación.
- [Garantías](../garantias/equipos-en-garantia.md): el reemplazo se inicia desde esta ficha.
- [Comprobante](comprobante-de-venta.md): imprime los datos actuales de la venta, conservados desde el registro o actualizados con aprobación.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «La venta no está activa (9.12).» | La venta no admite el abono. | Recarga la ficha y revisa su estado. |
| «El abono debe ser un entero mayor que cero.» | El formulario exige pesos enteros positivos. | Escribe el abono sin centavos. |
| «El abono debe ser mayor que cero (9.14).» | El valor no es válido. | Escribe el dinero efectivamente recibido. |
| «La imagen supera el máximo de 10 MB.» | El archivo es muy pesado. | Reduce la imagen antes de elegirla otra vez. |
| «Solo se aceptan imágenes (jpg, jpeg, png, webp).» | El formato no se admite. | Exporta una imagen en un formato permitido. |
| «La venta ya no está en tu alcance.» | La acción no puede operar sobre esta venta. | Vuelve al listado de tu alcance. |

Si el abono supera el saldo, el aviso indica ambos valores: revisa el saldo actualizado. Si falla una acción sin confirmación, comprueba en la ficha si quedó registrada antes de repetirla. Si no encuentras una venta, limpia los filtros y busca por un identificador exacto.

# Cómo imprimir el comprobante de venta

Prepara el documento que firma el cliente al recibir el equipo. Puedes imprimirlo o guardarlo en PDF desde el navegador.

> **Quién puede hacerlo:** Super Administrador, Administrador, Administrador de Punto y Vendedor, o quien tenga «Registrar ventas» efectivo, dentro de su alcance.
> **Dónde está:** Ventas → Ventas → **Imprimir** en la fila o en la ficha.

## Antes de empezar

La venta debe estar registrada. El comprobante usa los datos conservados en ella: cliente, equipo, sucursal, asesor, valores, medios de pago y texto de aceptación. No vuelve a tomar el nombre o las características de las fichas actuales para sustituirlos.

Una modificación aprobada o un reemplazo por garantía puede actualizar los datos de la venta y activar el aviso de reimpresión. Una venta anulada se puede imprimir para archivo, con su estado y fecha de anulación visibles.

## Cómo imprimir o guardar en PDF

1. Busca la venta en [Ventas](ventas.md).
2. Haz clic en **Imprimir**.
3. Espera que cargue **Imprimible de venta**.
4. Revisa el **Comprobante de venta** y su número.
5. Haz clic en **Imprimir** en esta página.
6. En el diálogo del navegador, elige la impresora o la opción de guardar en PDF.
7. Usa **Volver al detalle** para regresar a la venta.

El documento deja espacios en blanco para la **Firma** y la **Huella** del **Cliente**; se completan a mano. El asesor aparece identificado, pero no tiene un espacio de firma en el papel mostrado.

## Qué revisar en el documento

| Bloque | Qué comprobar |
|---|---|
| Venta | Número, ciudad, sucursal, fecha y hora. |
| Cliente | Documento, nombre y datos de contacto. |
| Equipo | IMEI, número interno, marca, referencia y características del aparato entregado. |
| Crédito y valores | Modalidad, precio, descuento, valor, crédito, cuotas y periodicidad. En financiada, recargo e IVA de intermediación cuando correspondan y total a pagar. |
| Referencias / Asesor / Medios de pago | Personas de contacto, quién atendió y distribución del pago. |
| Observaciones / Texto de aceptación | Condiciones y texto conservado al registrar la venta. |

El comprobante no muestra el costo ni la ganancia del negocio. **Número de contrato** se consulta en la ficha; no aparece en este formato imprimible.

## Qué significa Reimpresión

La etiqueta **Reimpresión** significa que el sistema ya había registrado una consulta del comprobante de esa venta. Abrir esta página registra ese hecho, antes de usar el diálogo de impresión del navegador. Cancelar la impresión del navegador no deshace ese registro.

El aviso de la ficha «Esta venta fue modificada después de su última impresión: vuelve a imprimirla.» indica la marca de modificación. Abrir o imprimir el comprobante no borra esa marca en la fuente actual.

## Qué ve cada rol

| Rol | Puede imprimir | Alcance |
|---|---|---|
| Super Administrador / Administrador | Sí | Global. |
| Administrador de Punto / Vendedor | Sí | Ventas de su sucursal. |
| Bodeguero | Con «Registrar ventas» efectivo | Ventas de su ubicación asignada. |

El permiso **Consultar ventas** por sí solo no permite imprimir. El formato de cliente no incorpora costo ni ganancia aunque quien imprime tenga permiso para consultarlos.

## Relación con otros módulos

**Necesitas antes:**
- [Registrar una venta](nueva-venta.md).
- [Texto de aceptación](texto-de-aceptacion.md), cuya versión queda conservada en la venta.
- [Solicitudes](solicitudes.md) y [Garantías](../garantias/equipos-en-garantia.md): los cambios aprobados o un reemplazo pueden requerir otro documento para el cliente.
- Lecturas de apoyo, según la tarea que realices: [Exportar a Excel e imprimir](../general/exportar-e-imprimir.md); [Cómo consultar ventas y registrar abonos](ventas.md).

**Esto afecta a:**
- [Ventas](ventas.md): el historial registra la consulta del comprobante.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «No se encontró la venta.» | El enlace no identifica una venta válida. | Vuelve al listado y abre el documento desde su fila. |
| Error de carga con **Reintentar** | No cargó la venta o el comprobante. | Usa Reintentar en el aviso correspondiente. |
| Sello de venta anulada | Estás imprimiendo una operación que ya no está vigente. | Conserva el documento como archivo de la anulación. |

Si los datos de la venta están mal, no los corrijas alterando el documento descargado. Tramita la [solicitud de modificación](solicitudes.md) y revisa después el comprobante.

# Cómo solicitar y resolver cambios de una venta

Pide una modificación o una anulación de una venta registrada. Enviar la petición no cambia la venta: el cambio se ejecuta cuando un administrador la aprueba.

> **Quién puede hacerlo:** Super Administrador, Administrador, Administrador de Punto y Vendedor solicitan con «Solicitar modificaciones y anulaciones». Super Administrador y Administrador resuelven.
> **Dónde está:** desde la ficha de Ventas; para seguimiento, Ventas → **Solicitudes**.

## Antes de empezar

La venta debe estar activa, ser computable y no tener otra solicitud pendiente, sea de modificación o anulación. Si ya hay una, un Super Administrador o Administrador debe resolverla antes de que presentes otra. Si eres un usuario de sede y la abrió un compañero, puede que no puedas verla. Escribe una **Justificación** que explique por qué hay que cambiarla. La solicitud conserva los valores de partida y los cambios propuestos.

El Administrador no puede aprobar una solicitud propia; debe revisarla otro administrador. El Super Administrador sí puede aprobar la propia. El Administrador puede rechazar su propia petición.

## Cómo solicitar una modificación

1. Abre una venta sin otra solicitud pendiente en [Ventas](ventas.md).
2. Haz clic en **Solicitar modificación**.
3. Revisa los datos que aparecen llenos con los valores actuales de la venta.
4. Cambia los datos comerciales, las referencias, observaciones o medios de pago que necesitas corregir.
5. Si necesitas otro cliente y tienes «Registrar ventas», busca uno existente por su tipo y número de documento.
6. Escribe la **Justificación**.
7. Haz clic en **Enviar solicitud**.

Al confirmar el envío, se cierra el diálogo y aparece la confirmación con **Ver solicitud**. La venta conserva sus datos mientras la petición esté pendiente.

Se pueden proponer precio, descuento, modalidad, entidad financiera, crédito, cuotas, periodicidad, número de contrato, referencias, observaciones, cliente y medios de pago. La solicitud no cambia el asesor, la sucursal ni el IMEI. Para reemplazar un aparato, consulta [Garantías](../garantias/equipos-en-garantia.md).

El cliente se cambia por otro existente: no se crea uno nuevo desde este diálogo. Si no tienes «Registrar ventas», el cliente queda en lectura. Sigue las reglas de campos de [Nueva venta](nueva-venta.md), comprobando el total de la propuesta. El tope propio que se muestra aquí orienta; la rebaja se comprueba contra el tope de quien aprueba al ejecutar el cambio.

Antes de crear la solicitud, el sistema comprueba los pagos de la propuesta: medios, importes, modalidad, financiera, suma contra el total y que Financiación cubra el recargo de intermediación y su IVA. Una propuesta que no cumple estas reglas se rechaza sin crear solicitud. Si propones sustituir pagos y hay abonos de cartera propia sin reversar, tampoco se crea la petición. El plan de crédito, las referencias y el tope del aprobador se comprueban al aprobar.

## Cómo solicitar una anulación

1. Abre la venta activa sin otra solicitud pendiente.
2. Haz clic en **Solicitar anulación**.
3. Escribe el motivo en el diálogo.
4. Confirma con **Solicitar anulación**.
5. Si el envío se confirma, usa **Ver solicitud** para seguir su revisión.

La solicitud de anulación no devuelve todavía el equipo ni el dinero de caja. Si se aprueba, el equipo vuelve al inventario disponible, la venta queda anulada y deja de ser computable; sus movimientos pendientes de reverso reciben contramovimientos.

Un reemplazo por garantía con el aparato retirado todavía en un estado de garantía abierta puede impedir **enviar la solicitud** y también **aprobar una ya existente**. El bloqueo depende del estado actual del aparato retirado, no solo de que la venta haya tenido un reemplazo. Si el envío falla por ese motivo, no se crea una nueva solicitud para seguimiento; revisa el impedimento con quien gestiona [Garantías](../garantias/equipos-en-garantia.md).

Para aprobar, además, el equipo de la venta debe seguir **Vendido**. La aprobación de anulación rechaza una venta que tenga registros de abonos de cartera propia, incluso si fueron reversados: esa comprobación mira la existencia histórica del abono.

## Cómo consultar tus solicitudes

1. Entra a Ventas → **Solicitudes**.
2. Elige **Estado**: Pendiente, Aprobada o Rechazada. La bandeja abre en Pendiente y no ofrece una opción de todos los estados.
3. Si tienes alcance global, puedes filtrar además por **Sucursal** y **Ciudad**.
4. Revisa **Venta**, **Tipo**, **Solicitante**, **Fecha**, **Justificación** y **Estado**.
5. Usa **Ver** en **Acciones** para abrir la solicitud. El enlace del número de venta abre la venta.

En la ficha ves quién solicitó, cuándo, la justificación y los cambios propuestos. Cuando está resuelta, muestra **Resuelta por**, **Fecha de resolución** y **Nota**. Los cambios propuestos se presentan con sus valores de origen y propuesta; no incluyen costo ni ganancia de la venta.

## Cómo aprobar o rechazar

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Abre una solicitud **Pendiente**.
2. Revisa la justificación y los cambios o efectos propuestos.
3. Para ejecutarla, haz clic en **Aprobar**.
4. Confirma con **Aprobar** en el diálogo.

Al terminar se actualiza la solicitud. Una modificación aprobada actualiza la venta y activa su aviso de reimpresión. Si sustituye medios de pago, conserva las líneas anteriores como reemplazadas y contramueve la caja asociada antes de emitir la de las nuevas líneas. Cambiar financiera o entrar a Financiada usa la configuración de intermediación que correspondía a la fecha de la venta; conservar la financiera conserva su configuración congelada.

Para rechazarla:

1. Haz clic en **Rechazar**.
2. Escribe el motivo obligatorio.
3. Confirma con **Rechazar**.

La venta queda como estaba y la solicitud queda rechazada. Una solicitud resuelta no se puede resolver otra vez.

Si la propuesta no cumple el plan, el descuento, las referencias o el cuadre del pago, la aprobación falla. El aprobador no edita la petición desde esta ficha: puede rechazarla con una explicación para que la rehagan. Cambiar medios de pago se bloquea si hay abonos de cartera propia sin reversar; corregir otros datos no tiene ese bloqueo específico. El cuadre de pagos y ese bloqueo por abonos también se comprueban al enviar la propuesta, antes de crear la solicitud.

## Qué ve cada rol

| Rol | Consulta y solicita | Aprueba / rechaza |
|---|---|---|
| Super Administrador | Solicitudes de alcance global | Sí; puede aprobar la propia. |
| Administrador | Solicitudes de alcance global | Sí; no aprueba la propia, sí puede rechazarla. |
| Administrador de Punto / Vendedor | Sus solicitudes en su sucursal, no las de sus compañeros | No. |
| Bodeguero | Sus solicitudes en su ubicación con «Solicitar modificaciones y anulaciones» y sus requisitos efectivos | No. |

El alcance de las solicitudes es más estrecho que el listado de ventas para los roles de sede: ver una venta de un compañero no permite abrir la solicitud que ese compañero creó. «Aprobar o rechazar modificaciones y anulaciones» es reservado, no un permiso extra otorgable.

## Relación con otros módulos

**Necesitas antes:**
- [Venta registrada](ventas.md).
- [Entidades financieras](../administracion/entidades-financieras.md) y [medios de pago](../administracion/medios-de-pago.md) válidos para la propuesta.
- Lecturas de apoyo, según la tarea que realices: [Formularios y acciones comunes: crear, editar, deshabilitar y anular](../general/formularios-y-acciones-comunes.md); [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md); [Cómo consultar y publicar topes de descuento](topes-de-descuento.md); [Cómo consultar créditos y cortes por financiera](../dashboard/informe-de-financieras.md); [Cómo comparar metas en un informe](../dashboard/informe-de-metas.md); [Cómo consultar el tablero de ventas](../dashboard/tablero-de-ventas.md).

**Esto afecta a:**
- [Inventario](../inventario/equipo-detalle.md): la anulación revierte la venta del equipo.
- [Caja](caja.md): los cambios de medios y la anulación generan contramovimientos.
- [Comprobante](comprobante-de-venta.md): una modificación aprobada marca reimpresión.
- [Garantías](../garantias/equipos-en-garantia.md): una garantía abierta puede bloquear la anulación.
- [Metas](../metas/metas.md) y [tablero](../dashboard/tablero-de-ventas.md): una anulada deja de ser computable.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Esta venta ya tiene una solicitud pendiente: resuélvela antes de abrir otra (9.11).» | Ya hay una modificación o anulación pendiente. | Pide a un Super Administrador o Administrador que la resuelva; si la abrió un compañero, puede que no puedas verla. |
| «La justificación es obligatoria (9.11.2).» | Falta explicar la modificación. | Llena Justificación. |
| «Abriste esta solicitud: la aprueba otro administrador.» | Eres el Administrador solicitante. | Deja la aprobación a otro administrador; puedes rechazarla si corresponde. |
| «El rechazo exige un motivo (9.11.5).» | No hay explicación del rechazo. | Escribe el motivo. |
| «Esta solicitud ya fue resuelta: no se puede resolver dos veces (9.11).» | Otro intento ya la cerró. | Recarga y revisa el resultado. |
| «La venta no está activa: no admite solicitudes de cambio (9.12).» | La venta dejó de admitir cambios. | Recarga su ficha. |

Si el envío de una modificación se detiene por pagos que no cubren el total, financiación que no cubre el recargo y su IVA, o sustitución de pagos bloqueada por abonos sin reversar, no queda una solicitud creada. Revisa la propuesta y el impedimento antes de reenviar.

Si el envío de una solicitud de anulación se detiene por garantía abierta del aparato retirado, no queda una nueva petición para seguimiento. Revisa el impedimento con quien gestiona la garantía. Si la aprobación se detiene por garantía o abonos, no se completa la anulación; revisa el impedimento con quien gestiona la garantía o la caja. No supongas que reversar un abono histórico habilita la anulación: esa regla difiere de la que bloquea reemplazar medios de pago.

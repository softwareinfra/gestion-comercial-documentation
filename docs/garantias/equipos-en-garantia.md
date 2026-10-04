# Cómo atender un equipo en garantía

Consulta los equipos que están en garantía, registra su siguiente estado o reemplaza el equipo de una venta. El cambio de estado y el reemplazo son acciones distintas: el reemplazo se hace desde la ficha de la venta.

> **Quién puede hacerlo:** Super Administrador, Administrador, Administrador de Punto y Vendedor consultan el módulo. Por rol, el Vendedor no cambia estados; el reemplazo lo registran Super Administrador y Administrador. Los permisos extra pueden ampliar estas acciones.
> **Dónde está:** menú lateral → Garantías y Devoluciones. Para reemplazar: Ventas → ficha de la venta → **Reemplazar equipo**.

## Antes de empezar

- Identifica el equipo por su IMEI y revisa su [ficha de inventario](../inventario/equipo-detalle.md).
- El seguimiento reúne equipos en **En garantía**, **Devuelto por garantía** y **Dado de baja por nota crédito**. Los nombres salen del catálogo de estados operativos y pueden haberse renombrado.
- Para un reemplazo, necesitas una venta activa sin solicitud de anulación pendiente. El equipo que sale debe estar vendido o en garantía.
- El equipo que entra debe estar activo y **Disponible**, ser de la misma referencia y categoría, estar en la sucursal de la venta y no tener otra venta activa. Un equipo reservado no entra como reemplazo.

## Cómo consultar los equipos

1. Entra a **Garantías y Devoluciones**. Verás **Equipos en garantía**.
2. Elige **Estado**. Al entrar sin un estado válido, se usa **En garantía**.
3. Escribe el IMEI en el filtro si necesitas encontrar un equipo concreto.
4. Si tienes alcance global, elige **Sucursal** para limitar la consulta.
5. Revisa **IMEI**, **Referencia**, **Ubicación** y **Estado**.
6. Haz clic en **Ver** para abrir la ficha del equipo.

La lista tiene paginación; consulta [Listados, filtros y paginación](../general/listados-filtros-y-paginacion.md). Cambiar el filtro puede dejar la lista vacía aunque existan equipos en otro estado o ubicación.

## Cómo cambiar el estado

1. Busca el equipo en la lista.
2. Haz clic en **Cambiar estado** en su fila.
3. Elige **Nuevo estado**.
4. Escribe el **Motivo** del cambio.
5. Haz clic en **Cambiar estado**.

Se cierra el diálogo y se actualiza el listado. Los filtros se conservan: si el equipo dejó el estado consultado, puede desaparecer de esa lista.

| Estado actual | Destinos del recorrido |
|---|---|
| En garantía | Devuelto por garantía o Dado de baja por nota crédito |
| Devuelto por garantía | Disponible, Inactivo o Dado de baja por nota crédito |
| Dado de baja por nota crédito | No tiene un siguiente estado; no aparece el botón |

El diálogo ofrece los destinos presentes en el catálogo. Para iniciar la garantía de un equipo vendido, ve a [Cambiar el estado del equipo](../inventario/equipo-detalle.md). Al guardar, el cambio manual exige motivo, un estado de Inventario, un equipo no anulado y una transición permitida; deja registrado el cambio y su motivo. No comprueba la situación de la venta ni sus solicitudes y no registra un reemplazo. Para sustituir el aparato, sigue el procedimiento de reemplazo de esta página.

## Cómo reemplazar el equipo de una venta

Necesitas **Consultar ventas** efectivo para abrir la ficha, además de **Registrar reemplazos por garantía** y sus requisitos **Ver costo y ganancia** y **Consultar reemplazos por garantía**. Registrar reemplazos no abre automáticamente Ventas. Esto también aplica al Bodeguero con permisos extra.

1. Abre la [ficha de la venta](../ventas/ventas.md).
2. Haz clic en **Reemplazar equipo**.
3. Comprueba el equipo que aparece en **Sale de la venta**.
4. Elige **Equipo de reemplazo**.
5. Revisa la información del equipo elegido.
6. Escribe **Motivo del reemplazo** (obligatorio, máximo 500 caracteres).
7. Haz clic en **Reemplazar equipo**.

El reemplazo se registra directamente; no crea una solicitud de aprobación. El equipo retirado queda en garantía si estaba vendido, el nuevo queda vendido y la venta pasa a identificar el equipo nuevo. Se guarda un registro de reemplazo con consecutivo **GAR-** y la venta queda marcada para reimpresión.

La venta conserva su valor, costo, ganancia, pagos y caja. La diferencia de costo del reemplazo es informativa: costo del equipo que entra menos costo congelado del que sale. El historial de reemplazos de la venta muestra fecha, registro, equipos, diferencia de costo, motivo y quién registró. Para consultarlo en esa ficha necesitas **Consultar ventas**, **Consultar reemplazos por garantía** y su requisito **Ver costo y ganancia** efectivos.

Si la venta es financiada, avísale a la financiera del cambio de IMEI. El sistema muestra el recordatorio, pero no registra ese aviso. Para entregar el comprobante actualizado, consulta [Comprobante de venta](../ventas/comprobante-de-venta.md).

Si no hay candidatos, el formulario permite cancelar; prepara el equipo o su [traslado](../inventario/traslados.md) antes de intentar registrar. Si la conexión falla después del envío, revisa primero la venta y su historial antes de intentar otro reemplazo.

## Qué ve cada rol

| Rol | Consulta el seguimiento | Cambia estados | Registra reemplazo | Consulta historial de reemplazos |
|---|---|---|---|---|
| Super Administrador / Administrador | Todas las sucursales | Sí | Sí | Sí |
| Administrador de Punto | Su sucursal | Sí | Con permiso extra | Sí |
| Vendedor | Su sucursal | Con permiso extra | Con permisos extra | Con permisos extra |
| Bodeguero | Si un permiso extra le abre el módulo | Sí en su alcance | Con Registrar reemplazos y sus requisitos, más Consultar ventas | Con Consultar reemplazos y su requisito de costo, más Consultar ventas |

El seguimiento no tiene columnas de costo ni ganancia. Los permisos **Cambiar el estado de un equipo**, **Consultar reemplazos por garantía** y **Registrar reemplazos por garantía** controlan acciones diferentes. Consultar reemplazos requiere **Ver costo y ganancia**; registrar requiere además consultar reemplazos. Para registrar desde la ficha de la venta o consultar allí sus reemplazos, necesitas también **Consultar ventas**: es el acceso a esa pantalla, no una dependencia automática de los permisos de garantías. Los permisos extra no amplían la sucursal de los roles de sede.

## Relación con otros módulos

**Necesitas antes:**

- [Estados operativos](../administracion/estados-operativos.md): estados del recorrido.
- [Equipos](../inventario/equipos.md) y [traslados](../inventario/traslados.md): equipo de reemplazo disponible en la sucursal de la venta.
- [Ventas](../ventas/ventas.md): venta activa y equipo que se retira.
- [Solicitudes](../ventas/solicitudes.md): resolver una anulación pendiente antes de reemplazar.
- Lecturas de apoyo, según la tarea que realices: [Menú lateral y navegación](../general/menu-y-navegacion.md); [Referencias](../administracion/referencias.md); [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md); [Ficha del equipo](../inventario/equipo-detalle.md).

**Esto afecta a:**

- [Ficha del equipo](../inventario/equipo-detalle.md): estados del retirado y del reemplazo.
- [Comprobante de venta](../ventas/comprobante-de-venta.md): identifica el equipo nuevo y exige reimpresión.
- [Caja](../ventas/caja.md): el reemplazo conserva los pagos y no genera un movimiento de caja por la diferencia de costo.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Ningún equipo coincide con el filtro.» | No hay resultados para esa consulta | Revisa IMEI, estado y sucursal |
| «Elige el nuevo estado.» | Falta el destino | Elige una opción |
| «El motivo es obligatorio.» | Falta justificar el cambio de estado | Escribe el motivo |
| «El motivo del reemplazo es obligatorio (6.4).» | Falta justificar el reemplazo | Completa Motivo del reemplazo |
| «La venta no está activa: no admite reemplazo de equipo (9.12, 10.3).» | La venta no admite esta operación | Revisa su estado en Ventas |
| «La venta tiene una solicitud de anulación pendiente: resuelve la solicitud de anulación antes de reemplazar el equipo (9.12).» | Hay una anulación por resolver | Revisa la solicitud antes de continuar |
| «El equipo de reemplazo tiene que estar disponible en el inventario de la sucursal (8.10).» | El candidato dejó de estar disponible | Consulta inventario y elige otro equipo elegible |
| «La venta ya no tiene el equipo que se quiso retirar: otro reemplazo se registró mientras tanto. Revisa el histórico de la venta antes de volver a registrar (10.3).» | Ya cambió el equipo de la venta | Cierra el formulario y revisa el historial; evita registrar dos veces |

Si falta el estado **En garantía**, la pantalla indica que un administrador debe crearlo en **Estados operativos**. No muestra el inventario completo como sustituto del seguimiento.

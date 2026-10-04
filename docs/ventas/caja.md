# Cómo consultar y registrar movimientos de caja

Consulta ingresos y egresos, registra movimientos manuales y revisa el saldo por medio de pago y categoría. Para comparar el efectivo del día con lo contado, usa [Cuadre de caja](cuadres-de-caja.md).

> **Quién puede hacerlo:** Super Administrador, Administrador y Administrador de Punto. Vendedor y Bodeguero necesitan «Registrar y consultar movimientos de caja» efectivo. Solo Super Administrador y Administrador reversan movimientos manuales.
> **Dónde está:** menú lateral → Ventas → **Caja**.

## Antes de empezar

Los movimientos conservan su valor y datos: no se editan ni se borran desde esta pantalla. Un error en un movimiento manual se corrige con un **contramovimiento**, que deja un nuevo registro de igual valor y sentido contrario.

Las ventas y los abonos pueden generar movimientos automáticamente. No registres de nuevo como ingreso manual un dinero que ya quedó registrado por [Nueva venta](nueva-venta.md) o [Registrar abono](ventas.md#cómo-registrar-un-abono-de-cartera-propia).

Una bodega pura no registra ingresos ni egresos manuales. El tipo ingreso/egreso lo define la categoría que eliges.

## Cómo consultar y filtrar movimientos

1. Entra a **Caja**.
2. Revisa **Número**, **Fecha**, **Tipo**, **Categoría**, **Medio**, **Valor**, **Venta**, **Referencia**, **Notas** y **Estado**.
3. Filtra por **Tipo**, **Categoría**, **Medio de pago** y fechas.
4. Si tienes alcance global, usa además **Sucursal** y **Ciudad**.
5. Usa **Limpiar filtros** para retirar la selección.

La columna Sucursal aparece con alcance global. En Notas puedes leer el motivo y la relación del reverso con el movimiento original. Si tienes consulta de ventas, el número de la venta relacionada abre su ficha. Cambiar filtros vuelve a la primera página; consulta el funcionamiento general en [Filtros y paginación](../general/listados-filtros-y-paginacion.md).

## Cómo registrar un movimiento manual

1. Haz clic en **Nuevo movimiento**.
2. Elige **Sucursal** si tienes alcance global; para un usuario de sede aparece la asignada, en lectura.
3. Elige **Categoría**. Su nombre indica si corresponde a ingreso o egreso.
4. Elige **Medio de pago**.
5. Escribe **Valor**, mayor que cero.
6. Llena **Referencia** si necesitas identificar el pago; admite hasta 120 caracteres.
7. Llena **Notas** si necesitas explicar el movimiento.
8. Haz clic en **Registrar movimiento**.

Sucursal, Categoría, Medio de pago y Valor son obligatorios. Referencia y Notas son opcionales. La lista ofrece categorías activas para registro manual y medios activos; excluye las categorías reservadas que usa el sistema para ventas y abonos. Caja admite valores con hasta dos decimales: no impone la regla de pesos enteros del formulario de venta.

Al terminar se cierra el diálogo, se muestra la confirmación del movimiento y se recargan el listado y el saldo. Los filtros y la página se conservan; el movimiento nuevo puede quedar fuera de la vista actual.

## Cómo leer el saldo

Si eres Super Administrador o Administrador, elige **Sucursal** o **Ciudad** para cargar **Saldo**. Sin ninguno de esos filtros aparece «Elige una sucursal o una ciudad para ver el saldo.»; al limpiar ambos vuelve ese aviso. Para los usuarios de sede se consulta su ubicación sin exigir esa selección.

La sección **Saldo** presenta el saldo por sucursal, medio y categoría, con subtotales. Suma los ingresos y resta los egresos, incluyendo los contramovimientos. Puede haber saldos negativos o con centavos.

El saldo es acumulado. **No se limita por Tipo, Categoría, Medio de pago ni fechas del listado**. Para usuarios de alcance global lo acotan los filtros de Sucursal y Ciudad; para usuarios de sede lo acota su ubicación. Por eso el total visible de una página de movimientos no tiene que coincidir con el saldo.

El [Cuadre de caja](cuadres-de-caja.md) es otra lectura: compara los movimientos de un día con el efectivo contado.

## Cómo reversar un movimiento manual

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Busca el movimiento manual con estado **Registrado**.
2. Haz clic en **Reversar** en su fila.
3. Escribe el motivo obligatorio.
4. Confirma con **Reversar**.

Al terminar el sistema agrega un contramovimiento con el mismo valor, categoría y medio, y con el tipo opuesto. El original se muestra anulado; no desaparece. Se recargan el listado y el saldo, conservando los filtros.

Un movimiento ya reversado no admite otro reverso. Un contramovimiento no se reversa. Tampoco se reversan por separado desde Caja los movimientos ligados a ventas: su corrección pasa por [Solicitudes de venta](solicitudes.md). Esto incluye los abonos vinculados a una venta; no existe aquí un botón para deshacerlos por separado.

## Qué ve cada rol

| Rol | Consulta / registra | Reversa manuales | Alcance |
|---|---|---|---|
| Super Administrador / Administrador | Sí | Sí | Global. |
| Administrador de Punto | Sí | No | Su sucursal. |
| Vendedor / Bodeguero | Con «Registrar y consultar movimientos de caja» efectivo | No | Su sede; una bodega pura no registra movimientos manuales. |

El permiso «Ver la caja dentro de la venta» es distinto: abre esos datos en la ficha de una venta, no sustituye el permiso de esta pantalla. «Reversar movimientos de caja» es reservado a los roles administrativos.

## Relación con otros módulos

**Necesitas antes:**
- [Sucursal](../administracion/sucursales.md) que maneje caja.
- [Categorías de caja](../administracion/categorias-de-caja.md) y [medios de pago](../administracion/medios-de-pago.md) activos.
- Lecturas de apoyo, según la tarea que realices: [Entidades financieras](../administracion/entidades-financieras.md); [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md); [Cómo registrar una venta](nueva-venta.md); [Cómo pedir y resolver una rectificación de cuadre](solicitudes-de-cuadre.md); [Cómo solicitar y resolver cambios de una venta](solicitudes.md); [Cómo registrar un abono de cartera propia](ventas.md#cómo-registrar-un-abono-de-cartera-propia); [Cómo atender un equipo en garantía](../garantias/equipos-en-garantia.md).

**Esto afecta a:**
- [Cuadres de caja](cuadres-de-caja.md): incorporan los movimientos del día; si el cuadre ya estaba cerrado, requieren una rectificación para incorporarlos a una revisión nueva.
- [Ventas](ventas.md): los ingresos automáticos y los abonos se relacionan con su venta.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «El valor debe ser un número mayor que cero.» | Falta un importe válido. | Revisa Valor. |
| «La categoría de caja está inactiva (12.6).» | La categoría ya no admite nuevos movimientos. | Recarga el formulario y elige una activa. |
| «Una bodega no maneja caja: no registra ingresos ni egresos (6.2).» | La ubicación es bodega pura. | Revisa la sucursal de la operación. |
| «Este movimiento ya tiene su contramovimiento registrado (9.14).» | Ya se hizo el reverso. | Recarga el listado y revisa ambos registros. |
| «El motivo del contramovimiento es obligatorio (9.14).» | Falta explicar el reverso. | Escribe el motivo. |

Si falla el envío sin confirmación, comprueba en el listado si el movimiento o su reverso quedaron registrados antes de intentar de nuevo. Si no aparece el resultado, limpia los filtros.

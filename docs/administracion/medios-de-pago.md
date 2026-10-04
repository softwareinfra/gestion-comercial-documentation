# Medios de pago

Aquí administras las formas de cobro con las que se registra una venta (efectivo, transferencia, tarjeta…), y marcas cuáles de ellas **exigen una entidad financiera**. Lo usas cuando el negocio empieza a aceptar una forma de pago nueva, cuando quieres cambiar cómo se llama una existente o cuando una ya no se acepta.

> **Quién puede hacerlo:** Super Administrador y Administrador.
> **Dónde está:** menú lateral → Administración → Medios de pago.

Esta pantalla funciona igual que [Tipos de producto](tipos-de-producto.md) y [Marcas](marcas.md) (buscar, crear, editar, activar y desactivar). Aquí verás solo lo propio de los medios de pago: la casilla «Requiere entidad financiera» y lo que el sistema hace con ella.

## Antes de empezar

- **Medio de pago:** la forma en que el cliente paga una parte o el total de una venta. Una venta puede tener varias líneas de pago, cada una con su medio.
- **Código:** identificador corto que el sistema usa por dentro. Se escribe al crear y **no se puede cambiar**; al editar aparece de solo lectura.
- **Requiere entidad financiera:** si está marcada, una venta que use este medio **debe** llevar una entidad financiera (por ejemplo, un banco o ADDI). Ver [Entidades financieras](entidades-financieras.md).
- **No se borra nada.** Se desactiva con el interruptor **Activo**.

### Los medios que trae el sistema

Vienen de fábrica y están **Protegidos** (no se pueden desactivar, pero sí renombrar y cambiar la casilla):

| Nombre | Código | Requiere entidad financiera |
|---|---|---|
| Efectivo | `efectivo` | No |
| Tarjeta débito | `tarjeta_debito` | No |
| Tarjeta crédito | `tarjeta_credito` | No |
| Datáfono | `datafono` | No |
| Transferencia | `transferencia` | No |
| Cartera propia | `cartera_propia` | No |
| Financiación | `financiacion` | Sí |

## Cómo consultar y buscar

1. Entra a Administración → Medios de pago. Verás el título **Medios de pago** y la frase «Formas de cobro con las que se registra una venta, y cuáles exigen entidad financiera.»
2. La tabla tiene seis columnas: **Nombre**, **Código**, **Requiere entidad financiera** («Sí» o «No»), **Activo** (interruptor), **Protegido** («Sí» o «No») y **Acciones** (el lápiz).
3. La barra «Buscar por nombre o código…» busca en las dos cosas a la vez. El tipo de coincidencia y la paginación funcionan como en [Marcas](marcas.md#cómo-consultar-y-buscar).
4. Sin resultados: «Ningún medio de pago coincide con el filtro.» Sin medios: «Todavía no hay medios de pago.»

## Cómo crear un medio de pago

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Haz clic en **Nuevo medio de pago**.
2. Se abre el panel «Nuevo medio de pago» con la frase «Forma de cobro con la que se registra una venta.»
3. Escribe el **Nombre**.
4. Escribe el **Código**. No podrás cambiarlo después.
5. Marca **Requiere entidad financiera** solo si las ventas que usen este medio siempre deben llevar una entidad financiera. Por defecto viene sin marcar.
6. Haz clic en **Guardar**.

Al terminar se cierra el panel y se actualiza el listado, conservando la búsqueda y la página. La opción se crea activa y no protegida. Si no aparece, limpia la búsqueda y localízala por su nombre.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | El nombre del medio, hasta 100 caracteres. No puede repetir el de otro medio (sin importar mayúsculas). | Sí |
| Código | Solo letras sin tildes ni eñes, números, guiones y guiones bajos. Hasta 40 caracteres. No puede repetir el de otro medio. No se puede cambiar después. | Sí, al crear |
| Requiere entidad financiera | Casilla. Marcada: toda venta con este medio exige entidad financiera. | No (por defecto sin marcar) |

## Cómo editar un medio de pago

1. Haz clic en el lápiz de la fila («Editar: Transferencia», por ejemplo).
2. Se abre el panel «Editar medio de pago». El **Código** se ve pero no se escribe.
3. Cambia el **Nombre** y/o la casilla **Requiere entidad financiera**, y haz clic en **Guardar**. Al guardar viajan el nombre y la casilla.

Dos cosas que debes saber antes de tocar la casilla:

- **Marcarla tiene efecto inmediato en las ventas nuevas.** Cualquier venta que use ese medio pasa a exigir entidad financiera: si falta, el sistema responde «Esta venta exige una entidad financiera (9.8).» En una venta de **contado** el formulario no muestra el campo de la entidad financiera, así que el aviso aparece arriba del formulario y quien vende no tiene dónde corregirlo. Marca la casilla solo en medios que se usan en ventas financiadas.
- **Desmarcarla no quita las exigencias que trae el sistema.** Las ventas financiadas y las que usan el medio «Financiación» seguirán exigiendo entidad financiera aunque apagues la casilla de «Financiación».

## Cómo desactivar o volver a activar un medio de pago

1. Haz clic en el interruptor de la columna **Activo**. Se guarda al instante.
2. Los siete medios de fábrica tienen el interruptor bloqueado; al dejar el mouse encima dice «Las semillas del sistema no se pueden desactivar.»

Un medio desactivado sigue en la tabla, pero:

- **Ya no se ofrece** al registrar una venta, un abono ni un movimiento de caja (solo aparecen los activos).
- Si alguien lo manda de todos modos, el sistema lo rechaza: «El medio de pago «…» está inactivo (12.6).»
- Al modificar una venta que ya tenía ese medio, el medio sigue apareciendo en esa línea, con una insignia de inactivo, para que se vea cuál era.

## Qué ve cada rol

| Rol | Ve la pantalla | Puede crear | Puede editar y activar/desactivar | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | |
| Administrador | Sí | Sí | Sí | |
| Administrador de Punto | No | No | No | «No tienes permiso para acceder a esta sección.» si escribe la dirección. Elige el medio al registrar ventas, abonos y movimientos de caja |
| Vendedor | No | No | No | Igual. Elige el medio al registrar ventas |
| Bodeguero | No | No | No | Igual |

Los cinco roles pueden consultar el catálogo (lectura de apoyo). Ver [Marcas](marcas.md#qué-ve-cada-rol).

## Relación con otros módulos

**Necesitas antes:**
- [Entidades financieras](entidades-financieras.md): si marcas «Requiere entidad financiera», las ventas con ese medio necesitan una entidad activa.

**Esto afecta a:**
- [Registrar una venta](../ventas/nueva-venta.md): cada línea de pago se elige de los medios activos, y la casilla decide si la venta exige entidad financiera.
- [Solicitudes](../ventas/solicitudes.md): el formulario para pedir cambios de una venta también usa estos medios.
- [Caja](../ventas/caja.md): el movimiento de caja registrado a mano y el abono de cartera propia eligen un medio activo.
- [Ventas](../ventas/ventas.md) y [Tablero de ventas](../dashboard/tablero-de-ventas.md): el medio de pago es un filtro y un eje de agrupación.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Ya existe un elemento del catálogo con ese nombre.» | Ya hay un medio con ese nombre. | Usa el existente o cambia el nombre. |
| «Ingresa un código válido: solo letras sin tildes ni eñes, números, guiones y guiones bajos.» | El código tiene espacios, tildes u otros símbolos. | Corrígelo. |
| Un mensaje de «ya existe» bajo el campo **Código** | Ya hay otro medio con ese código. | Usa otro código. Si el aviso usa otro texto, revisa el campo señalado; si no puedes identificar el duplicado, avisa a tu administrador. |
| «El código es obligatorio para este catálogo.» | Falta el código al crear. | Escríbelo. |
| «No tienes permiso para ver esta información.» | Tu usuario no puede hacer esta acción. | Pídele a un Super Administrador que revise tu rol. |
| Un aviso rojo con el botón «Reintentar» | No se pudo cargar la lista. | Haz clic en **Reintentar**. |

## Preguntas frecuentes

**Dejamos de aceptar «Datáfono». ¿Lo desactivo?** No se puede: es un medio de fábrica y está protegido. Si necesitas dejar de usar un medio de fábrica, consulta a tu administrador cómo proceder.

**¿Qué pasa con las ventas viejas si renombro un medio?** El sistema solo cambia el nombre del medio; las ventas ya registradas siguen apuntando al mismo medio. Los comprobantes consultan el nombre que se guardó con cada pago de la venta; renombrar el catálogo no cambia ese nombre guardado.

# Categorías de caja

Aquí administras los **conceptos** con los que se clasifica cada movimiento de caja, y si cada concepto es un **ingreso** (entra plata) o un **egreso** (sale plata). Lo usas cuando necesitas un concepto nuevo, por ejemplo para registrar un gasto que no está en la lista. Cada categoría puede llevar un **código** que se escribe una sola vez, al crearla.

> **Quién puede hacerlo:** Super Administrador y Administrador.
> **Dónde está:** menú lateral → Administración → Categorías de caja.

Esta pantalla funciona igual que [Tipos de producto](tipos-de-producto.md) y [Marcas](marcas.md) (buscar, crear, editar, activar y desactivar). Aquí verás solo lo propio de las categorías de caja: el tipo (Ingreso o Egreso) y las categorías que el sistema usa por su cuenta.

## Antes de empezar

- **Categoría de caja:** el concepto de un movimiento de caja, por ejemplo «Gastos autorizados de sucursal». Quien registra un movimiento en [Caja](../ventas/caja.md) elige una categoría, y de ella sale si el movimiento suma o resta.
- **Tipo:** **Ingreso** o **Egreso**. Es obligatorio. El movimiento toma el sentido de su categoría: no se elige por separado.
- **Código:** identificador corto que el sistema usa por dentro. Se escribe al crear y **no se puede cambiar**; al editar aparece de solo lectura.
- **Nombre:** lo que ven las personas. Sí se puede cambiar. Puede repetirse entre un Ingreso y un Egreso, pero no dentro del mismo tipo (sin importar mayúsculas).
- **No se borra nada.** Se desactiva con el interruptor **Activa**.

### Las categorías que trae el sistema

Las ocho vienen de fábrica y están **Protegidas** (no se pueden desactivar, pero sí renombrar):

| Tipo | Nombre | Código |
|---|---|---|
| Ingreso | Cuotas iniciales | `cuotas_iniciales` |
| Ingreso | Ventas de contado | `ventas_contado` |
| Ingreso | Abonos de cartera propia | `abonos_cartera_propia` |
| Ingreso | Ingresos autorizados | `ingresos_autorizados` |
| Egreso | Gastos autorizados de sucursal | `gastos_sucursal` |
| Egreso | Consignaciones a cuentas de la empresa | `consignaciones` |
| Egreso | Traslados de efectivo | `traslados_efectivo` |
| Egreso | Ajustes autorizados | `ajustes_autorizados` |

**Tres de ellas las usa el sistema solo, y no se ofrecen para registrar a mano:** «Cuotas iniciales», «Ventas de contado» y «Abonos de cartera propia». El sistema las asigna cuando registras una venta de contado, una venta a crédito (cuota inicial) o un abono de cartera propia. Por eso el formulario de movimiento de caja no las muestra. Ver [Registrar una venta](../ventas/nueva-venta.md) y [Caja](../ventas/caja.md).

## Cómo consultar y buscar

1. Entra a Administración → Categorías de caja. Verás el título **Categorías de caja** y la frase «Los conceptos de ingreso y egreso con los que se clasifica cada movimiento de caja.»
2. La tabla tiene seis columnas: **Nombre**, **Código** (muestra «—» si la categoría no tiene código), **Tipo** (una etiqueta «Ingreso» o «Egreso»), **Activa** (interruptor), **Protegida** («Sí» o «No») y **Acciones** (el lápiz).
3. La barra dice «Buscar por nombre…», pero el sistema busca en el nombre **y** en el código. El tipo de coincidencia y la paginación funcionan como en [Marcas](marcas.md#cómo-consultar-y-buscar).
4. Sin resultados: «Ninguna categoría de caja coincide con el filtro.» Sin categorías: «Todavía no hay categorías de caja.»

## Cómo crear una categoría de caja

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Haz clic en **Nueva categoría de caja**.
2. Se abre el panel «Nueva categoría de caja» con la frase «Concepto de ingreso o egreso con el que se clasifica un movimiento de caja.»
3. Escribe el **Nombre**.
4. Escribe el **Código**. No podrás cambiarlo después.
5. En **Tipo** elige «Selecciona un tipo» y escoge **Ingreso** o **Egreso**.
6. Haz clic en **Guardar**.

Al terminar se cierra el panel y se actualiza el listado, conservando la búsqueda y la página. La opción se crea activa y no protegida. Si no aparece, limpia la búsqueda y localízala por su nombre. Si tienes permiso para registrar movimientos de caja, podrás elegirla entre las categorías activas no reservadas.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | El concepto, hasta 100 caracteres. No puede repetir el de otra categoría **del mismo tipo** (sin importar mayúsculas). | Sí |
| Código | Solo letras sin tildes ni eñes, números, guiones y guiones bajos. Hasta 40 caracteres. No puede repetir el de otra categoría. No se puede cambiar después. | Sí, al crear |
| Tipo | **Ingreso** o **Egreso**. | Sí |

## Cómo editar una categoría de caja

1. Haz clic en el lápiz de la fila («Editar: Ajustes autorizados», por ejemplo).
2. Se abre el panel «Editar categoría de caja». El **Código** se ve pero no se escribe.
3. Cambia el **Nombre** y/o el **Tipo**, y haz clic en **Guardar**. Al guardar viajan el nombre y el tipo.

Lo que conviene saber antes de cambiar el **Tipo**:

- **No cambies el tipo de «Cuotas iniciales», «Ventas de contado» ni «Abonos de cartera propia».** Son Ingreso por diseño. Si las pasas a Egreso, el sistema deja de poder registrar esas ventas y abonos, y responde «La categoría «Ventas de contado» es de tipo «egreso» y no puede registrar un movimiento de tipo «ingreso» (9.14).» (con el nombre que tenga la categoría).
- **Los movimientos ya registrados no cambian.** Cada movimiento guarda su propio tipo y el nombre de la categoría del momento; cambiar la categoría después no los altera ni mueve el saldo histórico. Sí afecta a los movimientos **nuevos**.
- Con las categorías que creas tú, cambiar el tipo solo afecta lo que se registre desde ese momento.

## Cómo desactivar o volver a activar una categoría

1. Haz clic en el interruptor de la columna **Activa**. Se guarda al instante.
2. Las ocho de fábrica tienen el interruptor bloqueado; al dejar el mouse encima dice «Las semillas del sistema no se pueden desactivar.»

Una categoría desactivada sigue en la tabla, pero ya no se ofrece al registrar un movimiento de caja. Si alguien intenta usarla, el sistema responde «La categoría de caja está inactiva (12.6).»

## Qué ve cada rol

| Rol | Ve la pantalla | Puede crear | Puede editar y activar/desactivar | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | |
| Administrador | Sí | Sí | Sí | |
| Administrador de Punto | No | No | No | «No tienes permiso para acceder a esta sección.» si escribe la dirección. Registra movimientos de caja de su sucursal |
| Vendedor | No | No | No | Igual. No ve los movimientos de caja |
| Bodeguero | No | No | No | Igual. No ve los movimientos de caja |

Los cinco roles pueden consultar el catálogo (lectura de apoyo); ver los movimientos de caja es otra cosa y depende del rol o del permiso «Registrar y consultar movimientos de caja». Ver [Marcas](marcas.md#qué-ve-cada-rol) y [Roles y permisos](../general/roles-y-permisos.md).

## Relación con otros módulos

**Necesitas antes:**
- Nada.

**Esto afecta a:**
- [Caja](../ventas/caja.md): al registrar un movimiento a mano se elige una categoría activa (sin las tres que usa el sistema solo), y la lista de movimientos se puede filtrar por categoría.
- [Registrar una venta](../ventas/nueva-venta.md): según la modalidad, el sistema registra el ingreso en «Ventas de contado» o en «Cuotas iniciales»; los abonos de cartera propia van a «Abonos de cartera propia».
- [Cuadres de caja](../ventas/cuadres-de-caja.md): se calculan con los movimientos de caja. El cuadre agrupa los movimientos por categoría y medio de pago y conserva sus nombres al cerrar.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Elige el tipo de flujo antes de guardar.» | Dejaste el **Tipo** sin elegir. | Elige Ingreso o Egreso y guarda de nuevo. |
| «Ya existe una categoría de caja con ese nombre para ese tipo de flujo.» | Ya hay una categoría con ese nombre y el mismo tipo. | Usa la existente o cambia el nombre. |
| «Ingresa un código válido: solo letras sin tildes ni eñes, números, guiones y guiones bajos.» | El código tiene espacios, tildes u otros símbolos. | Corrígelo. |
| Un mensaje de «ya existe» sobre el código | Ya hay otra categoría con ese código. | Usa otro código. Si el aviso usa otro texto, revisa el campo señalado; si no puedes identificar el duplicado, avisa a tu administrador. |
| «El código es obligatorio para este catálogo.» | Falta el código al crear. | Escríbelo. |
| «No tienes permiso para ver esta información.» | Tu usuario no puede hacer esta acción. | Pídele a un Super Administrador que revise tu rol. |
| Un aviso rojo con el botón «Reintentar» | No se pudo cargar la lista. | Haz clic en **Reintentar**. |

## Preguntas frecuentes

**Quiero un gasto nuevo, por ejemplo «Papelería». ¿Cómo lo creo?** Crea una categoría de tipo **Egreso** con ese nombre y un código propio (por ejemplo `papeleria`). Luego aparece en el formulario de movimientos de [Caja](../ventas/caja.md).

**¿Por qué «Ventas de contado» no sale cuando registro un movimiento a mano?** Porque la asigna el sistema solo al registrar la venta; ofrecerla a mano mezclaría ingresos manuales con los de las ventas.

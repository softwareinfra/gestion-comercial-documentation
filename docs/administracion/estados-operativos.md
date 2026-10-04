# Estados operativos

Aquí ves y administras los **estados** por los que pasan las cosas del negocio: el estado de un equipo («Disponible», «Vendido»…) y el de un traslado («Despachado», «Recibido»…). Sirve sobre todo para **consultar** qué estados existen y para cambiarles el nombre o el orden en que se muestran. Crear estados nuevos es posible, pero tiene un alcance limitado (ver «Qué hace el sistema con los estados»).

> **Quién puede hacerlo:** Super Administrador y Administrador.
> **Dónde está:** menú lateral → Administración → Estados operativos.

Esta pantalla funciona igual que [Tipos de producto](tipos-de-producto.md) y [Marcas](marcas.md) (buscar, crear, editar, activar y desactivar). Aquí verás solo lo propio de los estados: el dominio, el orden y los que trae el sistema.

## Antes de empezar

- **Estado operativo:** una etapa por la que pasa un equipo o un traslado.
- **Dominio:** a qué tipo de cosa pertenece el estado. Hay cinco en la lista: **Inventario**, **Traslados**, **Garantías**, **Ventas** y **Movimientos de caja**. Es una lista fija del sistema: no puedes agregar dominios nuevos.
- **Orden:** un número que decide en qué orden se muestran los estados de un mismo dominio en las listas (por ejemplo, en el filtro «Estado» de Equipos). El menor sale primero.
- **Código:** identificador corto que el sistema usa por dentro. Se escribe al crear y **no se puede cambiar**; al editar aparece de solo lectura.
- **Nombre:** lo que ven las personas. Sí se puede cambiar.
- **No se borra nada.** Se desactiva con el interruptor **Activo**.

### Los estados que trae el sistema

Vienen de fábrica y están **Protegidos** (no se pueden desactivar, pero sí renombrar):

**Dominio Inventario** (estado de un equipo):

| Orden | Nombre | Código |
|---|---|---|
| 1 | Disponible | `disponible` |
| 2 | Reservado | `reservado` |
| 3 | Vendido | `vendido` |
| 4 | En traslado | `en_traslado` |
| 5 | En garantía | `en_garantia` |
| 6 | Devuelto por garantía | `devuelto_garantia` |
| 7 | Dado de baja por nota crédito | `baja_nota_credito` |
| 8 | Inactivo | `inactivo` |

**Dominio Traslados** (estado de un traslado):

| Orden | Nombre | Código |
|---|---|---|
| 1 | Creado | `creado` |
| 2 | Pendiente de despacho | `pendiente_despacho` |
| 3 | Despachado | `despachado` |
| 4 | En tránsito | `en_transito` |
| 5 | Recibido | `recibido` |
| 6 | Rechazado | `rechazado` |
| 7 | Anulado | `anulado` |

Para los dominios **Garantías**, **Ventas** y **Movimientos de caja** el código no trae estados de fábrica. Consulta el listado para conocer los estados disponibles en tu instalación.

## Cómo consultar y buscar

1. Entra a Administración → Estados operativos. Verás el título **Estados operativos** y la frase «Los estados por los que pasan inventario, traslados, garantías, ventas y movimientos de caja.»
2. La tabla tiene siete columnas: **Nombre**, **Código**, **Dominio** (una etiqueta), **Orden**, **Activo** (interruptor), **Protegido** («Sí» o «No») y **Acciones** (el lápiz).
3. La barra «Buscar por nombre o código…» busca en las dos cosas a la vez. **No busca por dominio**: para ver los de un dominio, busca por un nombre o código que conozcas. El tipo de coincidencia y la paginación funcionan como en [Marcas](marcas.md#cómo-consultar-y-buscar).
4. Sin resultados: «Ningún estado operativo coincide con el filtro.» Sin estados: «Todavía no hay estados operativos.»

## Cómo crear un estado operativo

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Haz clic en **Nuevo estado operativo**.
2. Se abre el panel «Nuevo estado operativo» con la frase «Estado por el que pasan inventario, traslados, garantías, ventas y caja.»
3. Escribe el **Nombre**.
4. Escribe el **Código**. No podrás cambiarlo después.
5. En **Dominio** elige «Selecciona un dominio» y escoge uno de los cinco.
6. Si quieres, escribe el **Orden** (un número de 0 en adelante). Si lo dejas vacío, el sistema le pone 0.
7. Haz clic en **Guardar**.

Al terminar se cierra el panel y se actualiza el listado, conservando la búsqueda y la página. La opción se crea activa y no protegida. Si no aparece, limpia la búsqueda y localízala por su nombre.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | El nombre del estado, hasta 100 caracteres. No puede repetir el de otro estado **del mismo dominio** (sin importar mayúsculas); dominios distintos sí pueden repetir nombre. | Sí |
| Código | Solo letras sin tildes ni eñes, números, guiones y guiones bajos. Hasta 40 caracteres. No puede repetir el de otro estado (de ningún dominio). No se puede cambiar después. | Sí, al crear |
| Dominio | Inventario, Traslados, Garantías, Ventas o Movimientos de caja. | Sí |
| Orden | Número entero de 0 en adelante. Vacío = 0 al crear; al editar, vacío = no cambia. | No |

## Cómo editar un estado operativo

1. Haz clic en el lápiz de la fila («Editar: Disponible», por ejemplo).
2. Se abre el panel «Editar estado operativo». El **Código** se ve pero no se escribe.
3. Cambia el **Nombre**, el **Dominio** o el **Orden**, y haz clic en **Guardar**.

**No cambies el Dominio de los estados de fábrica.** El sistema busca cada estado por su código **y** su dominio: por ejemplo, al registrar un ingreso busca «Disponible» en Inventario, y al confirmar una venta busca «Vendido» en Inventario. Si cambias el dominio de uno de esos estados, el sistema ya no lo encuentra y esas acciones fallan. Si una operación falla después de ese cambio, avisa a tu administrador y menciona el estado cuyo dominio se modificó. Renombrarlos y cambiar su orden sí es seguro.

## Cómo desactivar o volver a activar un estado

1. Haz clic en el interruptor de la columna **Activo**. Se guarda al instante.
2. Los 15 estados de fábrica tienen el interruptor bloqueado; al dejar el mouse encima dice «Las semillas del sistema no se pueden desactivar.»

Un estado que crees tú se puede desactivar; sigue en la tabla.

## Qué hace el sistema con los estados

- **Los estados de un equipo y de un traslado siguen un flujo fijo que está en el sistema, no en esta pantalla.** Por ejemplo, en el **cambio ordinario de estado**, un equipo «Vendido» solo puede pasar a «En garantía» o «Dado de baja por nota crédito». Hay una excepción separada: al **aprobar la anulación de su venta**, el sistema devuelve el equipo vendido a «Disponible». No es una opción para cambiarlo a mano; se hace mediante [Solicitudes de modificación y anulación](../ventas/solicitudes.md). El sistema decide los pasos permitidos por el **código** de cada estado. Un estado que crees aquí **no tiene ningún paso permitido**: no aparece como destino al cambiar el estado de un equipo, y nada del sistema lo asigna solo. Por eso, en la práctica, esta pantalla sirve para **renombrar y reordenar** los estados existentes.
- **Equipos:** el filtro «Estado» y el cambio de estado de un equipo muestran los estados del dominio Inventario, ordenados por **Orden** y luego por nombre. Ver [Equipos](../inventario/equipos.md).
- **Traslados:** cada traslado muestra su estado con el nombre de este catálogo. Ver [Traslados](../inventario/traslados.md).
- **Ventas y garantías:** la ficha de una venta y la pantalla de equipos en garantía leen este catálogo para mostrar los nombres de estado. Ver [Ventas](../ventas/ventas.md) y [Equipos en garantía](../garantias/equipos-en-garantia.md).

## Qué ve cada rol

| Rol | Ve la pantalla | Puede crear | Puede editar y activar/desactivar | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | |
| Administrador | Sí | Sí | Sí | |
| Administrador de Punto | No | No | No | «No tienes permiso para acceder a esta sección.» si escribe la dirección. Ve los nombres de estado en Inventario y Traslados |
| Vendedor | No | No | No | Igual. Ve los nombres de estado en Inventario y Ventas |
| Bodeguero | No | No | No | Igual. Ve los nombres de estado en Inventario y Traslados |

Los cinco roles pueden consultar el catálogo (lectura de apoyo). Ver [Marcas](marcas.md#qué-ve-cada-rol).

## Relación con otros módulos

**Necesitas antes:**
- Nada.

**Esto afecta a:**
- [Equipos](../inventario/equipos.md) y [Detalle de un equipo](../inventario/equipo-detalle.md): los nombres de estado y su orden en filtros y en el cambio de estado.
- [Registrar un ingreso](../inventario/ingresos.md): los equipos nuevos nacen «Disponible».
- [Traslados](../inventario/traslados.md): los nombres de los estados de traslado.
- [Registrar una venta](../ventas/nueva-venta.md): al confirmar, el equipo pasa a «Vendido».
- [Equipos en garantía](../garantias/equipos-en-garantia.md): los estados «En garantía» y «Devuelto por garantía».

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Completa el dominio antes de guardar.» | Dejaste el **Dominio** sin elegir. | Elige uno y guarda de nuevo. |
| «Ya existe un estado con ese nombre en ese dominio.» | Ya hay un estado con ese nombre en el mismo dominio. | Usa el existente o cambia el nombre. |
| «Ingresa un código válido: solo letras sin tildes ni eñes, números, guiones y guiones bajos.» | El código tiene espacios, tildes u otros símbolos. | Corrígelo. |
| Un mensaje de «ya existe» bajo el campo **Código** | Ya hay otro estado con ese código. | Usa otro código. Si el aviso usa otro texto, revisa el campo señalado; si no puedes identificar el duplicado, avisa a tu administrador. |
| «El código es obligatorio para este catálogo.» | Falta el código al crear. | Escríbelo. |
| «No tienes permiso para ver esta información.» | Tu usuario no puede hacer esta acción. | Pídele a un Super Administrador que revise tu rol. |
| Un aviso rojo con el botón «Reintentar» | No se pudo cargar la lista. | Haz clic en **Reintentar**. |

## Preguntas frecuentes

**¿Puedo agregar un estado «En reparación» para los equipos?** Puedes crearlo (dominio Inventario), pero el sistema no lo usará: ningún paso del flujo lleva a ese estado ni sale de él. Si necesitas ese recorrido, consulta a tu administrador antes de crear el estado.

**¿Puedo cambiar el orden en que salen los estados de Inventario?** Sí: cambia el número de **Orden** de cada uno y guarda.

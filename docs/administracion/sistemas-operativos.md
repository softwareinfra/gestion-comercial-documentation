# Sistemas operativos

Aquí administras la lista de sistemas operativos (iOS, Android, etc.) con la que se agrupan los equipos en los informes. Cada referencia tiene uno. Lo usas si aparece un sistema nuevo que quieres poder separar en los informes, o para cambiar cómo se llama uno existente. Cada sistema lleva un **código** que se escribe una sola vez, al crearlo.

> **Quién puede hacerlo:** Super Administrador y Administrador.
> **Dónde está:** menú lateral → Administración → Sistemas operativos.

Esta pantalla funciona igual que [Tipos de producto](tipos-de-producto.md) y [Marcas](marcas.md) (buscar, crear, editar, activar y desactivar). Aquí verás solo lo propio de los sistemas operativos.

## Antes de empezar

- **Sistema operativo:** el eje con el que los informes separan los equipos (por ejemplo iOS contra Android).
- **Código:** identificador corto que el sistema usa por dentro. Se escribe al crear y **no se puede cambiar**; en la edición aparece de solo lectura.
- **Nombre:** lo que ven las personas. Sí se puede cambiar.
- **No se borra nada.** Se desactiva con el interruptor **Activo**.

### Los sistemas que trae el sistema

| Nombre | Código | ¿Protegido? | Para qué sirve |
|---|---|---|---|
| iOS | `ios` | Sí | El que llevan los iPhone. |
| Android | `android` | Sí | El que llevan los celulares Android. |
| Sin clasificar | `sin_clasificar` | Sí | Valor de reserva: lo pone el sistema cuando una referencia no tiene un sistema claro. **No se puede elegir a mano** al crear o editar una referencia. |
| Otro | `otro` | No | Un sistema distinto de iOS y Android. Este sí se puede desactivar. |

Los protegidos no se pueden desactivar (el interruptor sale bloqueado), pero sí renombrar.

## Cómo consultar y buscar

1. Entra a Administración → Sistemas operativos. Verás el título **Sistemas operativos** y la frase «Eje de los informes por sistema operativo; cada uno lleva un código que no cambia.»
2. La tabla tiene cinco columnas: **Nombre**, **Código**, **Activo** (interruptor), **Protegido** («Sí» o «No») y **Acciones** (el lápiz).
3. La barra «Buscar por nombre o código…» busca en las dos cosas a la vez. El tipo de coincidencia y la paginación funcionan como en [Marcas](marcas.md#cómo-consultar-y-buscar).
4. Sin resultados: «Ningún sistema operativo coincide con el filtro.» Sin sistemas: «Todavía no hay sistemas operativos.»

## Cómo crear un sistema operativo

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Haz clic en **Nuevo sistema operativo**.
2. Se abre el panel «Nuevo sistema operativo» con la frase «Eje de los informes; su código se fija al crearlo y no cambia.»
3. Escribe el **Nombre** (por ejemplo, «HarmonyOS»).
4. Escribe el **Código** (por ejemplo, `harmony`). No podrás cambiarlo después.
5. Haz clic en **Guardar**.

Al terminar se cierra el panel y se actualiza el listado, conservando la búsqueda y la página. La opción se crea activa y no protegida. Si no aparece, limpia la búsqueda y localízala por su nombre.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | El nombre del sistema, hasta 100 caracteres. No puede repetir el de otro sistema (sin importar mayúsculas). | Sí |
| Código | Solo letras sin tildes ni eñes, números, guiones y guiones bajos. Hasta 40 caracteres. No puede repetir el de otro sistema. No se puede cambiar después. | Sí, al crear |

## Cómo editar un sistema operativo

1. Haz clic en el lápiz de la fila («Editar: Android», por ejemplo).
2. Se abre el panel «Editar sistema operativo». El **Código** se ve pero no se escribe.
3. Cambia el **Nombre** y haz clic en **Guardar**. Al guardar solo viaja el nombre.

## Cómo desactivar o volver a activar un sistema

1. Haz clic en el interruptor de la columna **Activo**. Se guarda al instante.
2. iOS, Android y Sin clasificar tienen el interruptor bloqueado; al dejar el mouse encima dice «Las semillas del sistema no se pueden desactivar.»

Un sistema desactivado sigue en la tabla, pero deja de ofrecerse en el desplegable **Sistema operativo** al crear o editar referencias. Las referencias que ya lo usan lo conservan. El sistema no revisa si hay referencias que lo usan.

## Qué hace el sistema con los sistemas operativos

- Cada [referencia](referencias.md) tiene uno. **Al crear** una referencia, si dejas «Según el tipo de producto», el sistema pone iOS a los iPhone, Android a los celulares Android y «Sin clasificar» a los demás tipos. **Al editar**, esa opción vuelve a derivar iOS o Android para los tipos correspondientes; con cualquier otro tipo **conserva el sistema operativo actual**, no lo reemplaza por «Sin clasificar». Ver [Cómo decide el sistema el sistema operativo](referencias.md#cómo-decide-el-sistema-el-sistema-operativo).
- Los informes ([Tablero de ventas](../dashboard/tablero-de-ventas.md) y [Tablero de inventario](../dashboard/tablero-de-inventario.md)) permiten filtrar por sistema operativo. El Tablero de ventas además muestra un desglose iOS / Android, que busca esos dos sistemas por sus códigos `ios` y `android`.
- Como el sistema operativo cuelga de la referencia, si cambias el de una referencia las ventas anteriores de ese modelo se reagrupan en los informes.

## Qué ve cada rol

| Rol | Ve la pantalla | Puede crear | Puede editar y activar/desactivar | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | |
| Administrador | Sí | Sí | Sí | |
| Administrador de Punto | No | No | No | «No tienes permiso para acceder a esta sección.» si escribe la dirección |
| Vendedor | No | No | No | Igual |
| Bodeguero | No | No | No | Igual |

Los cinco roles pueden consultar el catálogo (lectura de apoyo). Ver [Marcas](marcas.md#qué-ve-cada-rol).

## Relación con otros módulos

**Necesitas antes:**
- Nada.
- Lecturas de apoyo, según la tarea que realices: [Tipos de producto](tipos-de-producto.md).

**Esto afecta a:**
- [Referencias](referencias.md): el sistema operativo se elige (o se deriva) al crear o editar una referencia.
- [Tablero de ventas](../dashboard/tablero-de-ventas.md) y [Tablero de inventario](../dashboard/tablero-de-inventario.md): filtro y desglose por sistema operativo.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Ya existe un elemento del catálogo con ese nombre.» | Ya hay un sistema con ese nombre. | Usa el existente o cambia el nombre. |
| «Ingresa un código válido: solo letras sin tildes ni eñes, números, guiones y guiones bajos.» | El código tiene espacios, tildes u otros símbolos. | Corrígelo. |
| Un mensaje de «ya existe» bajo el campo **Código** | Ya hay otro sistema con ese código. | Usa otro código. Si el aviso usa otro texto, revisa el campo señalado; si no puedes identificar el duplicado, avisa a tu administrador. |
| «El código es obligatorio para este catálogo.» | Falta el código al crear. | Escríbelo. |
| «No tienes permiso para ver esta información.» | Tu usuario no puede hacer esta acción. | Pídele a un Super Administrador que revise tu rol. |
| Un aviso rojo con el botón «Reintentar» | No se pudo cargar la lista. | Haz clic en **Reintentar**. |

## Preguntas frecuentes

**¿Por qué no puedo elegir «Sin clasificar» en una referencia?** Porque es un valor de reserva que solo pone el sistema. Elige otro, o deja «Según el tipo de producto».

**¿Puedo desactivar «Otro»?** Sí, es el único de fábrica que no está protegido.

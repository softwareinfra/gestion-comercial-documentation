# Categorías de equipo

Aquí administras las categorías con las que clasificas cada equipo del inventario. Hoy el sistema trae dos: **Nuevo** y **Exhibición**. Es la categoría que eliges, equipo por equipo, al registrar un ingreso. Cada categoría lleva un **código** que se escribe una sola vez, al crearla.

> **Quién puede hacerlo:** Super Administrador y Administrador.
> **Dónde está:** menú lateral → Administración → Categorías de equipo.

Esta pantalla funciona igual que [Tipos de producto](tipos-de-producto.md) y [Marcas](marcas.md) (buscar, crear, editar, activar y desactivar). Aquí verás solo lo propio de las categorías de equipo.

## Antes de empezar

- **Categoría de equipo:** una etiqueta del estado comercial del equipo. Se elige por cada equipo al ingresarlo.
- **Código:** identificador corto que el sistema usa por dentro. Se escribe al crear y **no se puede cambiar**; al editar aparece de solo lectura.
- **Nombre:** lo que ven las personas. Sí se puede cambiar.
- **No se borra nada.** Se desactiva con el interruptor **Activa**.

### Las categorías que trae el sistema

Vienen de fábrica y están **Protegidas** (no se pueden desactivar, pero sí renombrar):

| Nombre | Código |
|---|---|
| Nuevo | `nuevo` |
| Exhibición | `exhibicion` |

## Cómo consultar y buscar

1. Entra a Administración → Categorías de equipo. Verás el título **Categorías de equipo** y la frase «Clasificación de los equipos del inventario; su código se fija al crearla y no cambia.»
2. La tabla tiene cinco columnas: **Nombre**, **Código**, **Activa** (interruptor), **Protegida** («Sí» o «No») y **Acciones** (el lápiz).
3. La barra «Buscar por nombre o código…» busca en las dos cosas a la vez. El tipo de coincidencia y la paginación funcionan como en [Marcas](marcas.md#cómo-consultar-y-buscar).
4. Sin resultados: «Ninguna categoría de equipo coincide con el filtro.» Sin categorías: «Todavía no hay categorías de equipo.»

## Cómo crear una categoría de equipo

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Haz clic en **Nueva categoría de equipo**.
2. Se abre el panel «Nueva categoría de equipo» con la frase «Agrupa los equipos del inventario; su código se fija al crearla y no cambia.»
3. Escribe el **Nombre**.
4. Escribe el **Código**. No podrás cambiarlo después.
5. Haz clic en **Guardar**.

Al terminar se cierra el panel y se actualiza el listado, conservando la búsqueda y la página. La opción se crea activa y no protegida. Si no aparece, limpia la búsqueda y localízala por su nombre.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | El nombre de la categoría, hasta 100 caracteres. No puede repetir el de otra categoría (sin importar mayúsculas). | Sí |
| Código | Solo letras sin tildes ni eñes, números, guiones y guiones bajos. Hasta 40 caracteres. No puede repetir el de otra categoría. No se puede cambiar después. | Sí, al crear |

## Cómo editar una categoría de equipo

1. Haz clic en el lápiz de la fila («Editar: Exhibición», por ejemplo).
2. Se abre el panel «Editar categoría de equipo». El **Código** se ve pero no se escribe.
3. Cambia el **Nombre** y haz clic en **Guardar**. Al guardar solo viaja el nombre.

## Cómo desactivar o volver a activar una categoría

1. Haz clic en el interruptor de la columna **Activa**. Se guarda al instante.
2. Nuevo y Exhibición tienen el interruptor bloqueado; al dejar el mouse encima dice «Las semillas del sistema no se pueden desactivar.»

Una categoría desactivada sigue en la tabla, pero deja de ofrecerse al registrar un ingreso (solo aparecen las activas). Los equipos ya registrados con ella la conservan.

## Qué hace el sistema con las categorías (por su código)

- **Batería de los iPhone de exhibición.** Si el equipo que ingresas es de tipo iPhone y su categoría es la de código `exhibicion`, el sistema exige el porcentaje de batería: «El porcentaje de batería es obligatorio para un iPhone de exhibición.» Por eso puedes cambiar el nombre «Exhibición» sin problema, pero no su código. Ver [Tipos de producto](tipos-de-producto.md) y [Registrar un ingreso](../inventario/ingresos.md).

## Qué ve cada rol

| Rol | Ve la pantalla | Puede crear | Puede editar y activar/desactivar | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | |
| Administrador | Sí | Sí | Sí | |
| Administrador de Punto | No | No | No | «No tienes permiso para acceder a esta sección.» si escribe la dirección. Elige la categoría al registrar ingresos |
| Vendedor | No | No | No | Igual |
| Bodeguero | No | No | No | Igual. Elige la categoría al registrar ingresos |

Los cinco roles pueden consultar el catálogo (lectura de apoyo). Ver [Marcas](marcas.md#qué-ve-cada-rol).

## Relación con otros módulos

**Necesitas antes:**
- Nada.

**Esto afecta a:**
- [Registrar un ingreso](../inventario/ingresos.md): cada equipo del ingreso se registra con una categoría activa.
- [Equipos](../inventario/equipos.md): la categoría aparece en la ficha del equipo.
- [Tablero de ventas](../dashboard/tablero-de-ventas.md) y [Tablero de inventario](../dashboard/tablero-de-inventario.md): la categoría es uno de los filtros.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Ya existe un elemento del catálogo con ese nombre.» | Ya hay una categoría con ese nombre. | Usa la existente o cambia el nombre. |
| «Ingresa un código válido: solo letras sin tildes ni eñes, números, guiones y guiones bajos.» | El código tiene espacios, tildes u otros símbolos. | Corrígelo. |
| Un mensaje de «ya existe» bajo el campo **Código** | Ya hay otra categoría con ese código. | Usa otro código. Si el aviso usa otro texto, revisa el campo señalado; si no puedes identificar el duplicado, avisa a tu administrador. |
| «El código es obligatorio para este catálogo.» | Falta el código al crear. | Escríbelo. |
| «No tienes permiso para ver esta información.» | Tu usuario no puede hacer esta acción. | Pídele a un Super Administrador que revise tu rol. |
| Un aviso rojo con el botón «Reintentar» | No se pudo cargar la lista. | Haz clic en **Reintentar**. |

## Preguntas frecuentes

**¿Puedo crear una categoría «Usado»?** Sí: créala con su nombre y un código propio (por ejemplo `usado`). Ojo: el sistema no le aplica ninguna regla especial; solo las categorías con código `exhibicion` activan la exigencia de batería en los iPhone. La categoría también puede elegirse como filtro en los tableros de ventas e inventario.

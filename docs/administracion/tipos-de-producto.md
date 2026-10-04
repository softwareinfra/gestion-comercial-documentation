# Tipos de producto

Aquí administras la clasificación base de lo que vendes: celular Android, iPhone, tablet, computador, smartwatch y accesorio. Cada tipo lleva un **código** que se escribe una sola vez, al crearlo, y nunca cambia. Lo usas cuando necesitas un tipo nuevo o cuando quieres cambiar cómo se llama uno existente.

> **Quién puede hacerlo:** Super Administrador y Administrador.
> **Dónde está:** menú lateral → Administración → Tipos de producto.

Esta pantalla funciona igual que [Marcas](marcas.md) (buscar, crear, editar, activar y desactivar). Aquí verás solo lo propio de los tipos de producto: el código, los tipos que trae el sistema y lo que el sistema hace con ellos.

## Antes de empezar

- **Tipo de producto:** la clasificación de un equipo. Cada referencia pertenece a un tipo (ver [Referencias](referencias.md)).
- **Código:** un identificador corto que el sistema usa por dentro. **Lo escribes al crear el tipo y después no se puede cambiar.** En la edición el campo aparece, pero solo de lectura.
- **Nombre:** lo que ven las personas en las listas. Sí se puede cambiar cuando quieras.
- **El sistema reconoce los tipos por su código, no por su nombre.** Por eso puedes renombrar «iPhone» sin romper nada, pero no puedes cambiarle el código.
- **No se borra nada.** Se desactiva con el interruptor **Activo**.

### Los tipos que trae el sistema

Vienen de fábrica y están marcados como **Protegido** (no se pueden desactivar, pero sí renombrar):

| Nombre | Código |
|---|---|
| Celular Android | `celular_android` |
| iPhone | `iphone` |
| Tablet | `tablet` |
| Computador | `computador` |
| Smartwatch | `smartwatch` |
| Accesorio tecnológico | `accesorio` |

## Cómo consultar y buscar

1. Entra a Administración → Tipos de producto. Verás el título **Tipos de producto** y la frase «Clasificación base del catálogo; cada tipo lleva un código que no cambia.»
2. La tabla tiene cinco columnas: **Nombre**, **Código**, **Activo** (interruptor), **Protegido** («Sí» o «No») y **Acciones** (el lápiz).
3. Para buscar usa la barra «Buscar por nombre o código…». Busca en el nombre y en el código a la vez. El tipo de coincidencia y la paginación funcionan como se explica en [Marcas](marcas.md#cómo-consultar-y-buscar).
4. Si no hay resultados verás «Ningún tipo de producto coincide con el filtro.»; si todavía no hay ninguno, «Todavía no hay tipos de producto.»

## Cómo crear un tipo de producto

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Haz clic en **Nuevo tipo de producto**.
2. Se abre el panel «Nuevo tipo de producto» con la frase «Clasificación base del catálogo; su código se fija al crearlo y no cambia.»
3. Escribe el **Nombre**.
4. Escribe el **Código**. Piénsalo bien: no podrás cambiarlo después.
5. Haz clic en **Guardar**.

Al terminar se cierra el panel y se actualiza el listado, conservando la búsqueda y la página. La opción se crea activa y no protegida. Si no aparece, limpia la búsqueda y localízala por su nombre.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | El nombre del tipo, hasta 100 caracteres. No puede repetir el de otro tipo (sin importar mayúsculas). | Sí |
| Código | Solo letras sin tildes ni eñes, números, guiones y guiones bajos (por ejemplo `tablet` o `equipo-de-sonido`). Hasta 40 caracteres. No puede repetir el de otro tipo. No se puede cambiar después. | Sí, al crear |

## Cómo editar un tipo de producto

1. Haz clic en el lápiz de la fila («Editar: iPhone», por ejemplo).
2. Se abre el panel «Editar tipo de producto». El **Código** se ve pero no se puede escribir en él.
3. Cambia el **Nombre** y haz clic en **Guardar**. Al guardar solo viaja el nombre.

## Cómo desactivar o volver a activar un tipo

1. Haz clic en el interruptor de la columna **Activo** de la fila. Se guarda al instante.
2. Los seis tipos de fábrica tienen el interruptor bloqueado; al dejar el mouse encima dice «Las semillas del sistema no se pueden desactivar.»

Un tipo desactivado sigue en la tabla, pero deja de ofrecerse en el desplegable **Tipo de producto** cuando creas o editas una referencia. El sistema no revisa si hay referencias que lo usan; esas siguen como están.

## Qué hace el sistema con los tipos (por su código)

- **Batería de los iPhone de exhibición.** Al registrar un ingreso, si el equipo es de tipo `iphone` y su categoría es `exhibicion`, el sistema exige el porcentaje de batería: «El porcentaje de batería es obligatorio para un iPhone de exhibición.» Ver [Categorías de equipo](categorias-de-equipo.md) y [Registrar un ingreso](../inventario/ingresos.md).
- **Sistema operativo de la referencia.** Si dejas el sistema operativo de una referencia en «Según el tipo de producto», `iphone` queda en iOS y `celular_android` en Android. Ver [Referencias](referencias.md) y [Sistemas operativos](sistemas-operativos.md).

## Qué ve cada rol

| Rol | Ve la pantalla | Puede crear | Puede editar y activar/desactivar | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | |
| Administrador | Sí | Sí | Sí | |
| Administrador de Punto | No | No | No | «No tienes permiso para acceder a esta sección.» si escribe la dirección |
| Vendedor | No | No | No | Igual |
| Bodeguero | No | No | No | Igual |

Los cinco roles pueden consultar el catálogo para elegir en otros formularios. Ver [Marcas](marcas.md#qué-ve-cada-rol).

## Relación con otros módulos

**Necesitas antes:**
- Nada.

**Esto afecta a:**
- [Referencias](referencias.md): cada referencia se crea con un tipo de producto activo.
- [Registrar un ingreso](../inventario/ingresos.md): la regla de la batería del iPhone de exhibición depende del tipo.
- [Sistemas operativos](sistemas-operativos.md): el sistema operativo por defecto de una referencia sale de su tipo.
- [Tablero de ventas](../dashboard/tablero-de-ventas.md): el tipo de producto es uno de los ejes del tablero.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Ya existe un elemento del catálogo con ese nombre.» | Ya hay un tipo con ese nombre (aunque cambien las mayúsculas). | Usa el existente, o elige otro nombre. |
| «Ingresa un código válido: solo letras sin tildes ni eñes, números, guiones y guiones bajos.» | El código tiene espacios, tildes u otros símbolos. | Escríbelo solo con letras sin tilde, números, guiones o guiones bajos. |
| Un mensaje de «ya existe» bajo el campo **Código** | Ya hay otro tipo con ese código. | Usa otro código. Si el aviso usa otro texto, revisa el campo señalado; si no puedes identificar el duplicado, avisa a tu administrador. |
| «El código es obligatorio para este catálogo.» | Falta el código al crear. | Escríbelo. Normalmente el navegador ya te avisa antes. |
| «Asegúrate de que este campo no tenga más de 40 caracteres.» (o 100 en el nombre) | El texto es demasiado largo. | Acórtalo. |
| «No tienes permiso para ver esta información.» | Tu usuario no puede hacer esta acción. | Pídele a un Super Administrador que revise tu rol. |

## Preguntas frecuentes

**Me equivoqué al escribir el código, ¿cómo lo corrijo?** No se puede editar. Crea un tipo nuevo con el código correcto y desactiva el equivocado con el interruptor (si no es uno de fábrica).

**¿Puedo renombrar «iPhone»?** Sí. El sistema lo reconoce por su código `iphone`, no por el nombre.

# Marcas

Aquí administras la lista de fabricantes (Samsung, Apple, etc.) de los equipos y accesorios que entran al inventario. Las usas cuando aparece una marca nueva que todavía no está en el sistema, o cuando una marca ya no se va a trabajar. Esta es también la página de entrada a los **ocho catálogos** de Administración: aquí se explica con detalle cómo funcionan todos (buscar, crear, editar, activar y desactivar), y en las otras siete páginas solo se cuenta lo propio de cada uno.

> **Quién puede hacerlo:** Super Administrador y Administrador.
> **Dónde está:** menú lateral → Administración → Marcas.

## Antes de empezar

- **Un catálogo es una lista de opciones** que luego eliges en otras pantallas (al registrar un ingreso, una venta o un movimiento de caja). Si una opción no está en el catálogo, no la puedes elegir allá.
- **Marca:** el fabricante del equipo. Cada referencia (el modelo concreto) pertenece a una marca. Ver [Referencias](referencias.md).
- **No se borra nada.** Una marca que ya no usas se **desactiva** con el interruptor de la columna **Activa**; se puede volver a activar cuando quieras. Las marcas no se anulan ni se eliminan.
- **El nombre no se puede repetir.** El sistema compara sin fijarse en mayúsculas: «Samsung» y «samsung» son la misma marca.
- En Marcas no hay opciones de fábrica: el sistema no trae ninguna marca cargada desde el inicio, así que todas las que veas las creó alguien.

### Cómo llegar a los catálogos

1. En el menú lateral haz clic en **Administración**. Se despliega la lista de pantallas del módulo (está en orden alfabético).
2. Elige la pantalla que necesitas. Los ocho catálogos son: **Categorías de caja**, **Categorías de equipo**, **Estados operativos**, **Marcas**, **Medios de pago**, **Referencias**, **Sistemas operativos** y **Tipos de producto**. (Las demás pantallas de la lista, como Ciudades o Usuarios, no son catálogos.)
3. Si abres Administración sin elegir una pantalla (por ejemplo, escribiendo la dirección `/administracion`), el sistema te lleva directo a **Marcas**: Administración no tiene una portada propia.

### Los ocho catálogos de un vistazo

| Catálogo | Para qué sirve en el día a día | Trae opciones de fábrica |
|---|---|---|
| [Marcas](marcas.md) | Fabricante del equipo | No |
| [Tipos de producto](tipos-de-producto.md) | Clasificar: celular Android, iPhone, tablet… | Sí (6) |
| [Referencias](referencias.md) | El modelo concreto de cada marca (lo eliges al ingresar un equipo) | No |
| [Sistemas operativos](sistemas-operativos.md) | iOS / Android para los informes | Sí (4) |
| [Categorías de equipo](categorias-de-equipo.md) | Nuevo o exhibición | Sí (2) |
| [Medios de pago](medios-de-pago.md) | Cómo paga el cliente en una venta | Sí (7) |
| [Categorías de caja](categorias-de-caja.md) | Concepto de cada movimiento de caja (ingreso o egreso) | Sí (8) |
| [Estados operativos](estados-operativos.md) | Estados por los que pasan inventario y traslados | Sí (15: 8 de inventario y 7 de traslados) |

Las opciones «de fábrica» vienen con el sistema y casi todas aparecen marcadas como **Protegida** o **Protegido** (más abajo se explica qué implica). La excepción es «Otro», en Sistemas operativos: viene de fábrica pero no está protegida.

## Cómo consultar y buscar

1. Entra a Administración → Marcas. Verás el título **Marcas** y la frase «Fabricantes de los equipos y accesorios que entran al inventario.»
2. Mira la tabla. Tiene cuatro columnas: **Nombre**, **Activa** (un interruptor), **Protegida** («Sí» o «No») y **Acciones** (el lápiz para editar).
3. La tabla muestra 25 marcas por página, ordenadas por nombre. Incluye las marcas desactivadas (con el interruptor apagado).
4. Para buscar, usa la barra que está encima de la tabla («Buscar por nombre…»). Elige a la izquierda cómo comparar (**Contiene**, **Inicia por**, **Es igual a** o **Termina en**) y escribe. La tabla se actualiza sola un instante después de que dejas de escribir.
5. Si ninguna marca coincide verás «Ninguna marca coincide con el filtro.» Si todavía no hay marcas: «Todavía no hay marcas.»

La búsqueda no distingue mayúsculas de minúsculas, pero **sí distingue tildes**: «samsung» encuentra «Samsung», pero «Perez» no encuentra «Pérez». Cómo funcionan el buscador, la paginación y la dirección de la página está en [Listados: buscar, filtrar y pasar de página](../general/listados-filtros-y-paginacion.md#cómo-buscar-por-texto).

## Cómo crear una marca

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Haz clic en **Nueva marca** (arriba a la derecha).
2. Se abre un panel lateral con el título «Nueva marca» y la frase «Fabricante de los equipos y accesorios que entran al inventario.»
3. Escribe el **Nombre**.
4. Haz clic en **Guardar**. Mientras se envía, el botón dice «Guardando…» y el panel no se puede cerrar.

Al terminar se cierra el panel y se actualiza el listado, conservando la búsqueda y la página. La opción se crea activa. Si no aparece, limpia la búsqueda y localízala por su nombre.

Para salir sin guardar haz clic en **Cancelar**, en la **X** o presiona **Escape**. Hacer clic fuera del panel no lo cierra. Más detalles en [Formularios y acciones comunes](../general/formularios-y-acciones-comunes.md).

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | El nombre de la marca, como quieres verlo en las listas. Hasta 100 caracteres. No puede repetir el de otra marca (sin importar mayúsculas). | Sí |

## Cómo editar una marca

1. En la fila de la marca, haz clic en el lápiz (su nombre es «Editar: Samsung», por ejemplo).
2. Se abre el panel «Editar marca» con el nombre ya escrito.
3. Cambia el **Nombre** y haz clic en **Guardar**.

Al terminar se cierra el panel y se recarga la lista conservando la búsqueda y la página. Si la fila deja de aparecer, busca el nombre nuevo o limpia la búsqueda. Si no cambiaste nada y guardas, el sistema no registra ningún cambio.

## Cómo desactivar o volver a activar una marca

En los catálogos no hay «Deshabilitar» ni «Anular» con motivo: hay un interruptor.

1. En la fila de la marca, haz clic en el interruptor de la columna **Activa**.
2. El cambio se guarda al instante y la tabla se actualiza. Mientras se guarda, ese interruptor no responde.

Qué pasa con una marca desactivada:

- Sigue existiendo y sigue saliendo en la tabla.
- Ya no se ofrece al crear o editar una referencia (el desplegable **Marca** solo muestra las activas).
- El sistema **no revisa** si hay referencias que usan esa marca: esas referencias siguen como están.

Si algo falla al cambiar el interruptor, el mensaje aparece arriba de la tabla.

### Qué es «Protegida»

La columna **Protegida** dice «Sí» para las opciones que vienen de fábrica con el sistema. A esas el interruptor les sale bloqueado, y al dejar el mouse encima dice «Las semillas del sistema no se pueden desactivar.» Sí puedes cambiarles el nombre. En Marcas todas dicen «No», porque no hay marcas de fábrica; y nadie puede crear opciones protegidas desde la pantalla.

## Qué ve cada rol

| Rol | Ve la pantalla | Puede crear | Puede editar y activar/desactivar | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | |
| Administrador | Sí | Sí | Sí | |
| Administrador de Punto | No | No | No | No tiene Administración en su menú. Si escribe la dirección, el sistema responde «No tienes permiso para acceder a esta sección.» |
| Vendedor | No | No | No | Igual que el anterior |
| Bodeguero | No | No | No | Igual que el anterior |

Aunque no vean la pantalla, los cinco roles pueden **consultar** el catálogo de marcas para elegir en los formularios de otros módulos (es una «lectura de apoyo»; ver [Roles y permisos](../general/roles-y-permisos.md)). Crear y editar catálogos es solo de los dos roles administrativos y **no** se puede dar como permiso extra (aparece como «Crear y editar catálogos», reservado; ver [Permisos de un usuario](usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra)).

## Relación con otros módulos

**Necesitas antes:**
- Nada. Es de los primeros catálogos que se llenan.

**Esto afecta a:**
- [Referencias](referencias.md): cada referencia pertenece a una marca; sin la marca creada y activa no puedes crear la referencia.
- [Registrar un ingreso](../inventario/ingresos.md) y [Equipos](../inventario/equipos.md): el equipo se registra con una referencia, y la referencia ya trae su marca.
- [Tablero de ventas](../dashboard/tablero-de-ventas.md): la marca es uno de los ejes para filtrar y agrupar las ventas.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Ya existe un elemento del catálogo con ese nombre.» (arriba del formulario) | Ya hay una marca con ese nombre, aunque esté escrita con otras mayúsculas o esté desactivada. | Busca la marca existente. Si está desactivada, actívala en vez de crear otra. |
| El navegador marca el campo Nombre como obligatorio | Lo dejaste vacío. | Escribe el nombre. |
| «Asegúrate de que este campo no tenga más de 100 caracteres.» | El nombre es demasiado largo. | Acórtalo. |
| «No tienes permiso para ver esta información.» | Tu usuario no puede hacer esta acción (por ejemplo, tus permisos cambiaron mientras tenías la pantalla abierta). | Pídele a un Super Administrador que revise tu rol. |
| Un aviso rojo con el botón «Reintentar» | No se pudo cargar la lista. | Haz clic en **Reintentar**. |

## Preguntas frecuentes

**¿Puedo borrar una marca que creé por error?** No. El sistema no borra registros. Desactívala con el interruptor, o edítala y corrige el nombre.

**¿Por qué no encuentro una marca que sé que existe?** Revisa el tipo de coincidencia (por defecto «Contiene») y las tildes. Borra el texto del buscador con la **X** para ver todas.

# Menú lateral y navegación

El menú lateral es la forma de moverte por el sistema. Aquí ves cómo se organiza, qué pantallas aparecen según tu usuario y qué pasa cuando intentas abrir algo que no te corresponde.

> **Quién puede hacerlo:** todos los roles. Lo que aparece en el menú cambia según el rol y los permisos.
> **Dónde está:** la columna oscura a la izquierda de toda pantalla, después de ingresar.

## Antes de empezar

- El sistema tiene **seis módulos**: Dashboard e Informes, Ventas, Inventario, Metas Comerciales, Garantías y Devoluciones, y Administración. Solo ves los que tu usuario tiene habilitados.
- Dentro de cada módulo hay **pantallas**. El menú solo te ofrece las pantallas que tu usuario puede abrir.
- Lo que ves en el menú es una comodidad: la autorización real la hace el sistema cada vez que pides algo. Mira [Roles y permisos](roles-y-permisos.md).

## Cómo leer el menú lateral

De arriba hacia abajo:

1. **Marca:** el logo y el texto «G5-Service», con «Gestión comercial» debajo.
2. **«Módulos»:** la lista de tus módulos, siempre en este orden: Dashboard e Informes, Ventas, Inventario, Metas Comerciales, Garantías y Devoluciones, Administración (los que no tengas no aparecen).
3. **Tu identidad (abajo):** un círculo con tus iniciales, tu nombre, tu rol y, si tienes sucursal, su nombre. A la derecha está el botón **Cerrar sesión**.

## Cómo moverte por los módulos

El menú funciona como un **acordeón**:

1. Al entrar, todos los módulos están recogidos.
2. Haz clic en el nombre de un módulo que tenga varias pantallas (por ejemplo **Ventas**). Se despliega su lista de pantallas debajo. Este clic **solo abre o cierra la lista**; no cambia de pantalla.
3. Haz clic en la pantalla que quieres (por ejemplo **Caja**). Ahí sí cambia la pantalla.
4. Al abrir otro módulo, el que estaba abierto se cierra. Solo uno queda desplegado a la vez.
5. El menú **no recuerda** qué estaba abierto: cada vez que recargas la página vuelve a mostrarse todo recogido.

Si un módulo te ofrece **una sola pantalla**, no hay lista: el nombre del módulo es un enlace directo a esa pantalla. Les pasa, por ejemplo, a **Garantías y Devoluciones** y a **Metas Comerciales**, y a un Vendedor con **Inventario**.

El módulo donde estás queda resaltado en rojo con texto blanco; la pantalla donde estás queda resaltada en gris dentro de la lista.

Las pantallas de cada módulo aparecen en **orden alfabético**, no en el orden en que se usan.

### Qué pantallas ofrece cada módulo

| Módulo | Pantalla en el menú | Quién la ve (permiso que la abre) | Roles que lo traen de base |
|---|---|---|---|
| Dashboard e Informes | Financieras | «Informe de financieras» | Super Administrador, Administrador |
| | Inventario | «Tablero de inventario» | Super Administrador, Administrador, Administrador de Punto |
| | Metas | «Tablero de metas» | Super Administrador, Administrador, Administrador de Punto, Vendedor |
| | Ventas | «Tablero de ventas» | Super Administrador, Administrador, Administrador de Punto, Vendedor |
| Ventas | Caja | «Registrar y consultar movimientos de caja» | Super Administrador, Administrador, Administrador de Punto |
| | Cuadre de caja | «Cuadres de caja» | Super Administrador, Administrador, Administrador de Punto |
| | Solicitudes | «Solicitar modificaciones y anulaciones» | Super Administrador, Administrador, Administrador de Punto, Vendedor |
| | Texto de aceptación | «Consultar el texto de aceptación» | Super Administrador, Administrador |
| | Topes de descuento | «Consultar topes de descuento» | Super Administrador, Administrador |
| | Ventas | «Consultar ventas» | Super Administrador, Administrador, Administrador de Punto, Vendedor |
| Inventario | Equipos | «Consultar inventario» | Los cinco roles |
| | Ingresos | «Registrar y consultar ingresos» | Super Administrador, Administrador, Administrador de Punto, Bodeguero |
| | Parámetros de precios | «Consultar parámetros de precio» | Super Administrador, Administrador, Administrador de Punto, Bodeguero |
| | Traslados | «Gestionar traslados» | Super Administrador, Administrador, Administrador de Punto, Bodeguero |
| Metas Comerciales | Metas | «Consultar metas» | Super Administrador, Administrador, Administrador de Punto, Vendedor |
| Garantías y Devoluciones | Equipos en garantía | Solo el módulo, sin permiso propio | Quien tenga el módulo: Super Administrador, Administrador, Administrador de Punto, Vendedor |
| Administración | Categorías de caja, Categorías de equipo, Ciudades, Entidades financieras, Estados operativos, Marcas, Medios de pago, Proveedores, Referencias, Sistemas operativos, Sucursales, Tipos de producto, Usuarios | Solo el módulo, sin permiso propio | Super Administrador, Administrador |

Notas sobre la tabla:

- Un permiso extra que te dé el Super Administrador puede hacer que una pantalla aparezca aunque tu rol no la traiga. Un ejemplo: a un Bodeguero con «Registrar y consultar movimientos de caja», el menú le muestra el módulo **Ventas** con solo la pantalla **Caja**. Mira [Permisos de un usuario](../administracion/usuario-detalle-y-permisos.md).
- Si algo no aparece en el menú pero crees que debería, pídele al Super Administrador que revise tus permisos.
- Varias pantallas de detalle (la ficha de un equipo, de una venta, de un usuario) no están en el menú: se abren desde el listado.

## La barra superior (miga de pan)

Arriba de cada pantalla verás dos textos, por ejemplo «Ventas › Caja». Indican dónde estás: primero el módulo y luego la pantalla. **No son enlaces**; para volver usa el menú. Si estás en una ficha de detalle (por ejemplo una venta), la barra muestra la pantalla de la que cuelga esa ficha.

## Moverte solo con el teclado

- Al presionar **Tab** por primera vez en una pantalla, el primer elemento es **Saltar al contenido**. Te lleva directo al contenido principal sin recorrer todo el menú.
- Las listas desplegables de los formularios y filtros se manejan con flechas, Inicio, Fin, Enter, Espacio y Escape. Mira [Formularios y acciones comunes](formularios-y-acciones-comunes.md).

## Qué pasa si abres algo que no te corresponde

| Lo que haces | Lo que ves |
|---|---|
| Escribes o pegas la dirección de una pantalla de un módulo que tu usuario no tiene | «No tienes permiso para acceder a esta sección.» |
| Escribes o pegas la dirección de una pantalla a la que tu usuario no tiene permiso, dentro de un módulo que sí tienes | «No tienes permiso para acceder a esta sección.» |
| Entras a un módulo por su nombre pero no tienes su pantalla principal | El sistema te lleva a la primera pantalla de ese módulo que sí puedes abrir (por ejemplo, un Bodeguero con solo Caja, al abrir Ventas, llega a Caja). Si no tienes ninguna, ves el aviso de arriba. |
| Escribes una dirección que no existe | «Página no encontrada — La dirección que abriste no corresponde a ninguna sección.», con el enlace **Volver al inicio**. |
| Abres Administración sin elegir una pantalla | Llegas a **Marcas**: no hay una portada propia de Administración. |

## Mientras carga una pantalla

- Verás «Cargando la pantalla…» un instante, con el menú y la barra en pie.
- Si el sistema se actualizó mientras tenías la página abierta, puede aparecer «La aplicación se actualizó mientras la tenías abierta. Recarga para seguir.» con el botón **Recargar**. Haz clic en él.
- Si aparece «No se pudo abrir esta pantalla.», haz clic en **Recargar**. Si se repite, avisa al administrador.

## Qué ve cada rol

| Rol | Módulos que abre (de base) | Observaciones |
|---|---|---|
| Super Administrador | Los seis | Todas las pantallas de la tabla de arriba |
| Administrador | Los seis | Todas las pantallas de la tabla de arriba |
| Administrador de Punto | Dashboard e Informes, Ventas, Inventario, Metas Comerciales, Garantías y Devoluciones | Sin Administración. No ve las pantallas de Topes de descuento, Texto de aceptación ni el Informe de financieras |
| Vendedor | Dashboard e Informes, Ventas, Inventario, Metas Comerciales, Garantías y Devoluciones | Sin Administración. En Dashboard solo Metas y Ventas; en Ventas solo Solicitudes y Ventas; en Inventario solo Equipos |
| Bodeguero | Inventario | Equipos, Ingresos, Parámetros de precios y Traslados |

## Relación con otros módulos

**Necesitas antes:**
- Haber ingresado: [Primeros pasos](primeros-pasos.md).
- Lecturas de apoyo, según la tarea que realices: [Roles y permisos](roles-y-permisos.md).

**Esto afecta a:**
- Cada pantalla de cada módulo se abre desde aquí. Las explicaciones de cada una están en su módulo: [Administración](../administracion/usuarios.md), [Inventario](../inventario/equipos.md), [Ventas](../ventas/ventas.md), [Garantías](../garantias/equipos-en-garantia.md), [Metas](../metas/metas.md) y [Dashboard](../dashboard/tablero-de-ventas.md).
- [Roles y permisos](roles-y-permisos.md): explica por qué tu menú es distinto al de otra persona.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «No tienes permiso para acceder a esta sección.» | Tu usuario no tiene ese módulo o esa pantalla. | Usa el menú para ir a otra pantalla. Si la necesitas para tu trabajo, pídele al Super Administrador que revise tus permisos. |
| «Tu usuario no tiene módulos habilitados. Pídele a un administrador que revise tus permisos.» | Tu usuario no tiene ningún módulo. | Avisa a un administrador. |
| «Esta sección todavía no tiene pantallas.» | El sistema reconoce un módulo que aún no tiene pantallas propias. | Avisa al administrador. |
| «Página no encontrada» | La dirección no existe. | Haz clic en **Volver al inicio**. |

# Usuarios

Aquí das de alta a las personas que entran al sistema, las buscas, les asignas su rol y su sucursal, les pones la contraseña y las deshabilitas o anulas cuando ya no deben entrar. Esta página cubre el listado y el alta; lo que haces sobre una persona que ya existe (editar, contraseña, deshabilitar, permisos extra) está en [Detalle de un usuario y sus permisos](usuario-detalle-y-permisos.md).

> **Quién puede hacerlo:** Super Administrador y Administrador.
> **Dónde está:** menú lateral → Administración → Usuarios.

Administrador de Punto, Vendedor y Bodeguero no tienen el módulo Administración en su menú. Si alguno de ellos escribe la dirección de la pantalla a mano, el sistema le responde «No tienes permiso para acceder a esta sección.»

## Antes de empezar

- **Rol:** define qué módulos abre la persona y qué puede hacer en ellos. Son cinco: Super Administrador, Administrador, Administrador de Punto, Vendedor y Bodeguero. Lo que trae cada uno está en [Roles y permisos](../general/roles-y-permisos.md).
- **Sucursal:** es el lugar donde trabaja la persona. Para el Administrador de Punto, el Vendedor y el Bodeguero es **obligatoria**; sus datos operativos se acotan a **su** sucursal, pero pueden consultar catálogos nacionales de apoyo según sus permisos. Para el Bodeguero la pantalla también dice «Sucursal», pero el sistema lo trata como su ubicación asignada (puede ser una bodega o cualquier otro tipo de sede). El Super Administrador y el Administrador pueden quedar «Sin sucursal» y ven todas.
- **Nombre de usuario:** no lo escribes tú. El sistema lo arma solo con el primer nombre y el primer apellido, en minúsculas y sin tildes: «Ana Rojas» queda `ana.rojas`. Si ya existe, agrega un número: `ana.rojas2`, `ana.rojas3`. Si el nombre tiene varias palabras (por ejemplo «María José Pérez Gómez») solo usa la primera de cada campo: `maria.perez`. Una vez creado no se puede cambiar.
- **Contraseña:** tampoco se escribe al crear. La persona no podrá entrar hasta que tú le asignes una, desde su ficha (ver [Asignar una contraseña](usuario-detalle-y-permisos.md#asignar-una-contraseña)).
- **Nada se borra:** a un usuario solo se le deshabilita (se puede reactivar) o se le anula (definitivo). Ver [Deshabilitar, activar o anular](usuario-detalle-y-permisos.md#deshabilitar-activar-o-anular-a-un-usuario).

## Cómo consultar y buscar usuarios

1. Entra a Administración → Usuarios. Verás el título **Usuarios** y la frase «Quiénes entran al sistema, con su rol y la sucursal donde trabajan.»
2. Mira la tabla «Listado de usuarios». Tiene cinco columnas: **Usuario**, **Nombre**, **Rol**, **Sucursal** y **Estado** (Activo, Deshabilitado o Anulado). Si la persona no tiene sucursal, la columna muestra «—».
3. La lista está ordenada por nombre de usuario y muestra 25 personas por página. Incluye a los usuarios deshabilitados y anulados.
4. Para abrir la ficha de alguien, haz clic en su **nombre de usuario** (la primera columna). No hay otro botón para esto.

### Filtros

La tarjeta «Filtros de usuarios» tiene tres campos:

| Campo | Qué hace |
|---|---|
| **Buscar** | Escribe en «Buscar por nombre, usuario o documento…». El botón de criterio al lado te deja elegir **Contiene** (por defecto), **Inicia por**, **Es igual a** o **Termina en**. |
| **Sucursal** | «Todas las sucursales» o una sucursal de la lista. La lista incluye también sucursales deshabilitadas, para que puedas encontrar a quienes trabajaban allí. |
| **Ciudad** | «Todas las ciudades» o una ciudad (la de la sucursal donde trabaja la persona). Incluye ciudades desactivadas. |

Cómo funciona la búsqueda:

- Busca en el nombre de usuario, el nombre, el apellido y el número de documento, cada uno por separado. El texto que escribes se compara entero contra cada campo, sin partirlo por espacios: si escribes «Ana Rojas» (con espacio) no aparece Ana Rojas, porque ningún campo contiene ese texto. Busca por «Ana» o por «Rojas», o por el nombre de usuario (`ana.rojas`).
- Las tildes cuentan: «Perez» no encuentra a «Pérez».
- La búsqueda se aplica unos instantes después de que dejas de escribir.
- Al cambiar cualquier filtro vuelves a la página 1.
- El botón **Limpiar filtros** borra el buscador y las dos listas a la vez. Debajo de los filtros la tarjeta cuenta cuántos usuarios coinciden.
- Si ningún usuario coincide verás «Ningún usuario coincide con los filtros.» Si todavía no hay ninguno: «Todavía no hay usuarios.»

La página, la búsqueda y los filtros quedan en la dirección del navegador: puedes recargar o compartir el enlace y verás lo mismo.

## Cómo crear un usuario

> **Quién puede hacerlo:** el Super Administrador crea usuarios de cualquier rol. El Administrador solo puede crear Administrador de Punto, Vendedor y Bodeguero.

1. Haz clic en **Nuevo usuario** (arriba a la derecha).
2. Se abre el diálogo «Nuevo usuario» («Persona con acceso al sistema, con su rol y su sucursal.»). Arriba te avisa que el nombre de usuario se genera solo y que la contraseña se asigna después.
3. Llena **Nombre**, **Apellido**, **Número de documento** y **Teléfono**. El **Correo electrónico** es opcional.
4. En **Rol** elige «Selecciona el rol» y escoge uno de la lista.
5. En **Sucursal** elige la sede donde trabajará (o deja «Sin sucursal» si el rol la permite).
6. Haz clic en **Guardar**. Mientras se envía el botón dice «Guardando…» y el diálogo no se puede cerrar.

Al terminar se cierra el diálogo y se actualiza el listado, conservando los filtros y la página. El usuario se crea con estado **Activo**, pero puede no aparecer en esa vista: limpia los filtros y busca su nombre de usuario. Todavía **no puede entrar**: falta asignarle la contraseña desde su ficha.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | Nombre de la persona, hasta 150 caracteres. Con él y el apellido se arma el nombre de usuario. | Sí |
| Apellido | Apellido de la persona, hasta 150 caracteres. | Sí |
| Número de documento | Solo números, de 5 a 15 dígitos. No puede repetirse: cada persona tiene un documento distinto. | Sí |
| Teléfono | Celular de 10 dígitos que empiece por 3, por ejemplo 3101234567. Si lo escribes con espacios o guiones («310 123 45 67»), el sistema los quita. | Sí |
| Correo electrónico | Un correo válido. Puedes dejarlo vacío. | No |
| Rol | Uno de los roles que tu propio rol puede asignar (ver arriba). | Sí |
| Sucursal | La sede donde trabaja. Solo aparecen las sucursales **activas**. | Sí para Administrador de Punto, Vendedor y Bodeguero. No para Super Administrador y Administrador |

## Qué ve cada rol

| Rol | Ve la pantalla | Puede crear | Puede editar | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí, todos los usuarios | Usuarios de cualquier rol | A cualquiera; a sí mismo solo nombre, documento, teléfono y correo | Es el único que puede crear y gestionar Administradores y otros Super Administradores |
| Administrador | Sí, todos los usuarios | Solo Administrador de Punto, Vendedor y Bodeguero | Solo a esos tres roles; a los Administradores y Super Administradores (incluido él mismo) solo los puede consultar | En «Rol» solo le aparecen esos tres |
| Administrador de Punto | No | No | No | No tiene Administración en su menú |
| Vendedor | No | No | No | No tiene Administración en su menú |
| Bodeguero | No | No | No | No tiene Administración en su menú |

Ningún permiso extra abre Administración para estos tres roles: los permisos de Administración que sí se pueden otorgar son solo de consulta y no suman el módulo al menú (ver [permisos extra](usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra)).

## Relación con otros módulos

**Necesitas antes:**
- [Crear una sucursal](sucursales.md): las personas con rol Administrador de Punto, Vendedor o Bodeguero necesitan una sucursal activa para poder crearlas.
- [Crear una ciudad](ciudades.md): el filtro «Ciudad» sale de las ciudades, y cada sucursal pertenece a una.
- Lecturas de apoyo, según la tarea que realices: [Menú lateral y navegación](../general/menu-y-navegacion.md).

**Esto afecta a:**
- La sucursal asignada acota los **datos operativos** del Administrador de Punto, el Vendedor y el Bodeguero. No acota los catálogos nacionales de apoyo, como sedes y ciudades; consultarlos no permite ver las operaciones de otra sede ni agrega Administración al menú. El Super Administrador y el Administrador tienen alcance operativo global. Ver [Roles y permisos](../general/roles-y-permisos.md).
- [Equipos](../inventario/equipos.md), [Ingresos](../inventario/ingresos.md) y [Traslados](../inventario/traslados.md): el Bodeguero opera Inventario en su ubicación.
- [Registrar una venta](../ventas/nueva-venta.md): el Vendedor y el Administrador de Punto registran ventas en su sucursal. Una bodega pura no registra ventas: el sistema rechaza con «Una bodega pura no registra ventas: traslada el equipo antes (6.2).» la venta de un equipo que está en una bodega.
- [Metas](../metas/metas.md): el Administrador de Punto y el Vendedor consultan las metas de su alcance.
- Deshabilitar o anular a alguien le quita el acceso: no podrá volver a iniciar sesión (ver [Primeros pasos](../general/primeros-pasos.md)).

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Elige el rol antes de guardar.» | Dejaste el Rol sin elegir. | Elige un rol de la lista y guarda de nuevo. |
| «La sucursal es obligatoria para el rol elegido.» | Elegiste Administrador de Punto, Vendedor o Bodeguero y dejaste «Sin sucursal». | Elige la sucursal. |
| «Los roles Administrador de Punto, Vendedor y Bodeguero requieren una sucursal asignada.» | Lo mismo, pero lo rechaza el sistema al guardar. | Elige la sucursal. |
| «Ya existe un registro con ese valor en «Cédula» (Usuario).» | Otro usuario ya tiene ese número de documento. | Revisa el número; no se pueden crear dos usuarios con el mismo documento. |
| «La cédula debe tener entre 5 y 15 dígitos.» | El número de documento tiene letras, puntos o una cantidad de dígitos fuera de 5 a 15. | Escríbelo solo con números. |
| «El celular debe tener 10 dígitos y empezar por 3 (formato 310XXXXXXX).» | El teléfono no cumple el formato. | Escribe el celular de 10 dígitos que empieza por 3. |
| «Ingresa un correo electrónico válido.» | El correo está mal escrito. | Corrígelo o déjalo vacío. |
| «Este campo es obligatorio.» / «Este campo no puede estar vacío.» | Falta un dato obligatorio (Nombre, Apellido, documento o teléfono). | Llénalo. Antes de enviar, el navegador también marca los campos vacíos con su propio aviso. |
| «No tienes permiso para ver esta información.» | El sistema no te deja hacer esa acción (por ejemplo, si tu rol o tus permisos cambiaron mientras tenías la pantalla abierta, o intentas gestionar a alguien con rol administrativo siendo Administrador). El mensaje dice «ver» aunque lo que fallaba era guardar. | Pídele el cambio a un Super Administrador. |
| «No fue posible generar un nombre de usuario único; reintenta.» | Dos personas se crearon al mismo tiempo con el mismo nombre. | Vuelve a guardar. |
| Un aviso rojo con el botón «Reintentar» | No se pudo cargar la lista (o las sucursales / ciudades). | Haz clic en **Reintentar**. Si las sucursales no cargan, el formulario no se puede llenar hasta que carguen. |

Si el sistema rechaza la longitud de **Nombre** o **Apellido**, acorta el campo a un máximo de 150 caracteres. La pantalla permite escribir más, pero el sistema no lo acepta al guardar.

## Preguntas frecuentes

**¿Por qué la persona que acabo de crear no puede entrar?** Porque el usuario nace sin contraseña. Entra a su ficha y usa **Asignar contraseña**.

**¿Puedo cambiar el nombre de usuario?** No. Se genera al crear y no se puede editar. Si se escribió mal el nombre o el apellido de la persona, corrígelo con **Editar** en su ficha; su nombre de usuario para entrar seguirá igual. **No anules la cuenta para corregir esos datos:** la anulación es definitiva y no libera el documento para crear otra cuenta con él.

**¿Por qué no encuentro a un usuario?** Revisa que los filtros de Sucursal y Ciudad estén en «Todas…» y usa **Limpiar filtros**. Recuerda que la búsqueda distingue tildes y no junta nombre y apellido.

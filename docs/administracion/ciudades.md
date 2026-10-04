# Ciudades

Aquí registras las ciudades (con su departamento) que después eliges al crear una sucursal. Es lo primero que conviene tener listo cuando vas a montar sedes nuevas. Las ciudades no se borran ni se anulan: solo se activan o se desactivan con un interruptor.

> **Quién puede hacerlo:** Super Administrador y Administrador.
> **Dónde está:** menú lateral → Administración → Ciudades.

Administrador de Punto, Vendedor y Bodeguero no tienen el módulo Administración en su menú. Si alguno de ellos escribe la dirección de la pantalla a mano, el sistema le responde «No tienes permiso para acceder a esta sección.» Esos roles sí **usan** las ciudades (por ejemplo, en filtros y formularios de otros módulos), pero no las administran (ver [Qué ve cada rol](#qué-ve-cada-rol)).

## Antes de empezar

- **Ciudad:** se identifica por su **nombre** y su **departamento** juntos. «Armenia» del Quindío y «Armenia» de otro departamento pueden existir las dos; lo que no puede repetirse es la pareja.
- **Activa:** una ciudad puede estar activa o inactiva. No hay «Deshabilitado» ni «Anulado» como en las sucursales o los proveedores; solo el interruptor **Activa**.
- **Nada se borra:** no hay botón para eliminar una ciudad. Las sucursales ya creadas conservan la ciudad que tenían.
- **Dónde se usa:** la ciudad se elige al crear o editar una [sucursal](sucursales.md) y sirve de filtro en varias pantallas (por ejemplo, el listado de [Usuarios](usuarios.md)).

## Cómo consultar y buscar ciudades

1. Entra a Administración → Ciudades. Verás el título **Ciudades** y la frase «Ciudades y departamentos donde ubicar las sucursales y los proveedores.»
2. La tabla «Listado de ciudades» tiene cuatro columnas: **Nombre**, **Departamento**, **Activa** (un interruptor) y **Acciones** (el lápiz para editar).
3. La lista sale ordenada por nombre y luego por departamento, con 25 ciudades por página. Incluye las ciudades inactivas.
4. Para buscar, usa la barra «Buscar por nombre o departamento…». A la izquierda puedes elegir el criterio: **Contiene** (por defecto), **Inicia por**, **Es igual a** o **Termina en**. El funcionamiento general de la búsqueda y la paginación está en [Listados: buscar, filtrar y pasar de página](../general/listados-filtros-y-paginacion.md).
5. Esta pantalla no tiene tarjeta de filtros: solo el buscador.

Cómo funciona la búsqueda aquí:

- Busca en el nombre y en el departamento; coincide si coincide en cualquiera de los dos.
- No distingue mayúsculas de minúsculas, pero **sí distingue tildes**: «Bogota» no encuentra «Bogotá».
- El texto que escribes se compara entero, sin partirlo por espacios.
- Si ninguna ciudad coincide verás «Ninguna ciudad coincide con el filtro.» Si todavía no hay ninguna: «Todavía no hay ciudades.»

## Cómo crear una ciudad

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Haz clic en **Nueva ciudad** (arriba a la derecha).
2. Se abre un panel lateral con el título «Nueva ciudad» y la frase «Se usará para ubicar sucursales y proveedores.»
3. Escribe el **Nombre**.
4. Escribe el **Departamento**.
5. Haz clic en **Guardar**. Mientras se envía, el botón dice «Guardando…» y el panel no se puede cerrar.

Al terminar se cierra el panel y se actualiza el listado, conservando la búsqueda y la página. La ciudad se crea con **Activa** encendido. Si no aparece, limpia la búsqueda y localízala por nombre y departamento.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | El nombre de la ciudad, hasta 100 caracteres. | Sí |
| Departamento | El departamento al que pertenece, hasta 100 caracteres. Es texto libre: lo escribes tú, no se elige de una lista. | Sí |

Dos cuidados al escribir:

- La pareja nombre + departamento **no distingue mayúsculas**: «ARMENIA / quindío» cuenta como repetida si ya existe «Armenia / Quindío».
- Como el departamento es texto libre, escríbelo siempre igual («Quindío», no «Quindio» ni «QUINDIO»): el sistema trata las tildes como letras distintas y te dejaría crear dos ciudades casi iguales.

## Cómo editar una ciudad

1. En la fila de la ciudad, haz clic en el lápiz (**Editar**).
2. Se abre el panel «Editar ciudad» con los datos actuales.
3. Cambia el **Nombre** o el **Departamento** y haz clic en **Guardar**.

Puedes cancelar con **Cancelar**, con la **X** o con la tecla Escape. Hacer clic fuera del panel no lo cierra.

## Cómo activar o desactivar una ciudad

1. En la columna **Activa** de la fila, haz clic en el interruptor.
2. El cambio se guarda al instante: **no pide motivo ni confirmación**, y no hay botón «Guardar».

Mientras el sistema guarda el cambio, el interruptor de esa fila queda bloqueado. Si falla, aparece el mensaje de error encima de la tabla.

Qué cambia al desactivar una ciudad:

- Deja de aparecer en la lista «Ciudad» al **crear o editar una sucursal** (esa lista muestra solo las activas).
- Sigue apareciendo en los **filtros** de ciudad de Usuarios y de Sucursales, para que puedas encontrar lo que ya tenías en ella.
- Las sucursales que ya estaban en esa ciudad no cambian.
- **Metas:** al crear o editar una [meta](../metas/metas.md) cuyo alcance incluya esa ciudad, el sistema responde «La ciudad está inactiva; la meta exige una ciudad activa (11.2).» Las metas que ya existían siguen calculándose.
- Desactivar la ciudad no elimina las sucursales que ya la tienen asignada. Revisa esas sucursales antes de cambiarla.

## Qué ve cada rol

| Rol | Ve la pantalla Ciudades | Puede crear | Puede editar / activar | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | |
| Administrador | Sí | Sí | Sí | |
| Administrador de Punto | No | No | No | No tiene Administración en su menú. El sistema sí le deja **consultar** las ciudades para sus filtros y formularios. |
| Vendedor | No | No | No | Igual: solo consulta de apoyo. |
| Bodeguero | No | No | No | Igual: solo consulta de apoyo. |

El permiso de consultar ciudades se llama «Consultar sedes y ciudades» (las sedes y las ciudades van en un solo permiso). Los cinco roles lo traen de base. El de crear y editar, «Crear y editar sedes y ciudades», está **reservado** a los roles administrativos y no se puede otorgar como permiso extra (ver [Detalle de un usuario y sus permisos](usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra)).

## Relación con otros módulos

**Necesitas antes:**
- Nada. Es el primer paso de la organización: crea las ciudades antes que las sucursales.
- Lecturas de apoyo, según la tarea que realices: [Formularios y acciones comunes: crear, editar, deshabilitar y anular](../general/formularios-y-acciones-comunes.md); [Listados: buscar, filtrar y pasar de página](../general/listados-filtros-y-paginacion.md).

**Esto afecta a:**
- [Sucursales](sucursales.md): cada sucursal pertenece a una ciudad activa, que eliges de esta lista.
- [Usuarios](usuarios.md): el filtro «Ciudad» sale de aquí (la ciudad de la sucursal donde trabaja la persona).
- Otras pantallas que filtran por ciudad, como el [tablero de ventas](../dashboard/tablero-de-ventas.md) y el [tablero de inventario](../dashboard/tablero-de-inventario.md). Qué filtros usa cada una se explica en su página.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Ya existe esa ciudad en ese departamento.» | Ya hay una ciudad con ese nombre y ese departamento (sin importar mayúsculas). | Revisa la lista; si ya existe, úsala. Si es otra ciudad, corrige el nombre o el departamento. |
| «Este campo es obligatorio.» / «Este campo no puede estar vacío.» | Falta el nombre o el departamento. | Llénalo. Antes de enviar, el navegador también marca los campos vacíos con su propio aviso. |
| «Asegúrate de que este campo no tenga más de 100 caracteres.» | El nombre o el departamento es demasiado largo. | Acórtalo. |
| Un aviso rojo con el botón **Reintentar** | No se pudo cargar la lista. | Haz clic en **Reintentar**. |
| «No tienes permiso para ver esta información.» | El sistema no te deja hacer esa acción (por ejemplo, si tu rol cambió mientras tenías la pantalla abierta). | Pídele el cambio a un Super Administrador. |

## Preguntas frecuentes

**¿Puedo borrar una ciudad que me equivoqué al crear?** No, no existe el borrado. Corrígela con **Editar**, o desactívala con el interruptor si ya no la quieres en las listas.

**¿Por qué una ciudad que desactivé sigue saliendo en un filtro?** Es a propósito: los filtros muestran también las ciudades inactivas para que puedas encontrar lo que quedó registrado en ellas.

**¿La ciudad sirve para ubicar proveedores?** La frase de la pantalla lo dice, pero el formulario de [proveedores](proveedores.md) no tiene campo de ciudad. Hoy la ciudad solo se asigna a las sucursales.

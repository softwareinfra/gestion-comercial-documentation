# Roles y permisos

> **Base verificada contra el código.** El detalle de botones de cada pantalla se consolida con las páginas de sus módulos. Donde falta ese detalle está marcado.

Aquí ves qué roles existen, qué módulos abre cada uno, qué permisos trae de base y cómo el Super Administrador puede sumarle permisos extra a una persona.

> **Quién puede hacerlo:** esta página es de consulta para todos. Asignar roles y permisos extra es de los administradores (ver abajo).
> **Dónde está:** el rol se asigna en Administración → Usuarios; los permisos extra, en la ficha del usuario.

## Los cinco roles

| Rol | Sucursal | Qué ve |
|---|---|---|
| Super Administrador | Opcional: ve todas aunque tenga una asignada | Todos los módulos y todo lo otorgable; además es el único que fija ciertas cosas (ver «Solo el Super Administrador») |
| Administrador | Opcional: ve todas aunque tenga una asignada | Todos los módulos |
| Administrador de Punto | Una asignada | Los datos de su sucursal |
| Vendedor | Una asignada | Los datos de su sucursal; en el tablero de ventas, solo sus propias ventas |
| Bodeguero | Una ubicación asignada (puede ser de cualquier tipo) | Inventario de su ubicación |

- **Super Administrador y Administrador** ven todo consolidado, de todas las sucursales. Los otros tres roles consultan los datos operativos de su sucursal o ubicación, con los recortes propios de cada pantalla. Las lecturas de apoyo pueden incluir catálogos nacionales; por ejemplo, otras sedes para elegir un destino de traslado.
- Un **Administrador** puede gestionar usuarios con rol Administrador de Punto, Vendedor o Bodeguero. Los demás roles los gestiona solo el Super Administrador. Consulta [Usuarios](../administracion/usuarios.md) y [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md) para editar sus datos y consultar sus permisos.

## Módulos que abre cada rol (antes de permisos extra)

| Módulo | Super Administrador | Administrador | Administrador de Punto | Vendedor | Bodeguero |
|---|:-:|:-:|:-:|:-:|:-:|
| Dashboard e Informes | Sí | Sí | Sí | Sí (acotado) | No |
| Ventas | Sí | Sí | Sí | Sí | No |
| Inventario | Sí | Sí | Sí | Sí | Sí |
| Metas Comerciales | Sí | Sí | Sí | Sí | No |
| Garantías y Devoluciones | Sí | Sí | Sí | Sí | No |
| Administración | Sí | Sí | No | No | No |

- Un permiso extra puede **abrirle un módulo** a una persona que su rol no trae. Mira «Permisos extra».
- Algunas pantallas de Administración (sedes, ciudades, catálogos, proveedores, entidades financieras) las **leen** otros roles para elegir en sus formularios, aunque el módulo Administración no aparezca en su menú.

## Permisos: qué son

Cada cosa que puedes hacer está descrita por un **permiso** con un nombre en pantalla. Tu lista de permisos es:

> los permisos de tu rol (la **base**) + los **permisos extra** que el Super Administrador te haya dado.

El menú y los botones que ves dependen de esa lista. Aun así, cada vez que haces algo, el sistema vuelve a comprobar que puedes: ocultar un botón no es lo único que te protege.

## Catálogo de permisos y quién lo trae de base

Hay 47 permisos. «Otorgable» significa que el Super Administrador puede dárselo como extra a un Administrador de Punto, Vendedor o Bodeguero. Los **reservados** nunca se otorgan como extra.

**Leyenda:** Sí = lo trae de base; — = no lo trae. SA = Super Administrador, A = Administrador, AP = Administrador de Punto, V = Vendedor, B = Bodeguero.

| Grupo | Permiso | SA | A | AP | V | B | Otorgable | Requiere antes |
|---|---|:-:|:-:|:-:|:-:|:-:|:-:|---|
| Inventario | Consultar inventario | Sí | Sí | Sí | Sí | Sí | Sí | |
| Inventario | Exportar e imprimir el inventario | Sí | Sí | Sí | Sí | Sí | Sí | |
| Inventario | Ver costo y ganancia | Sí | Sí | Sí | — | Sí | Sí | |
| Inventario | Ver historial del equipo | Sí | Sí | Sí | — | Sí | Sí | |
| Inventario | Cambiar el estado de un equipo | Sí | Sí | Sí | — | Sí | Sí | |
| Inventario | Registrar y consultar ingresos | Sí | Sí | Sí | — | Sí | Sí | Ver costo y ganancia; Consultar proveedores |
| Inventario | Gestionar traslados | Sí | Sí | Sí | — | Sí | Sí | |
| Inventario | Consultar parámetros de precio | Sí | Sí | Sí | — | Sí | Sí | Ver costo y ganancia |
| Inventario | Editar la ficha, el costo y los precios del equipo | Sí | Sí | — | — | — | Sí | Ver costo y ganancia |
| Inventario | Crear parámetros de precio | Sí | — | — | — | — | Reservado | |
| Ventas | Consultar ventas | Sí | Sí | Sí | Sí | — | Sí | |
| Ventas | Registrar ventas | Sí | Sí | Sí | Sí | — | Sí | Consultar ventas; Consultar entidades financieras |
| Ventas | Exportar el listado de ventas | Sí | Sí | Sí | Sí | — | Sí | Consultar ventas |
| Ventas | Solicitar modificaciones y anulaciones | Sí | Sí | Sí | Sí | — | Sí | Consultar ventas; Consultar entidades financieras |
| Ventas | Ver historial de la venta | Sí | Sí | Sí | — | — | Sí | Consultar ventas |
| Ventas | Registrar abonos de cartera propia | Sí | Sí | Sí | — | — | Sí | Consultar ventas |
| Ventas | Ver la caja dentro de la venta | Sí | Sí | Sí | — | — | Sí | Ver costo y ganancia; Consultar ventas |
| Ventas | Ficha, corrección e historial de clientes | Sí | Sí | — | — | — | Reservado | |
| Ventas | Consultar topes de descuento | Sí | Sí | — | — | — | Sí | |
| Ventas | Consultar el texto de aceptación | Sí | Sí | — | — | — | Sí | |
| Ventas | Aprobar o rechazar modificaciones y anulaciones | Sí | Sí | — | — | — | Reservado | |
| Ventas | Crear topes de descuento | Sí | — | — | — | — | Reservado | |
| Ventas | Crear el texto de aceptación | Sí | — | — | — | — | Reservado | |
| Caja | Registrar y consultar movimientos de caja | Sí | Sí | Sí | — | — | Sí | |
| Caja | Cuadres de caja | Sí | Sí | Sí | — | — | Sí | |
| Caja | Reversar movimientos de caja | Sí | Sí | — | — | — | Reservado | |
| Caja | Aprobar o rechazar rectificaciones de cuadre | Sí | Sí | — | — | — | Reservado | |
| Garantías | Consultar reemplazos por garantía | Sí | Sí | Sí | — | — | Sí | Ver costo y ganancia |
| Garantías | Registrar reemplazos por garantía | Sí | Sí | — | — | — | Sí | Ver costo y ganancia; Consultar reemplazos por garantía |
| Metas | Consultar metas | Sí | Sí | Sí | Sí | — | Sí | |
| Metas | Crear, editar, deshabilitar y activar metas | Sí | Sí | — | — | — | Reservado | |
| Tablero | Tablero de ventas | Sí | Sí | Sí | Sí | — | Sí | |
| Tablero | Tablero de inventario | Sí | Sí | Sí | — | — | Sí | Ver costo y ganancia |
| Tablero | Tablero de metas | Sí | Sí | Sí | Sí | — | Sí | |
| Tablero | Informe de financieras | Sí | Sí | — | — | — | Reservado | |
| Administración | Consultar sedes y ciudades | Sí | Sí | Sí | Sí | Sí | Sí | |
| Administración | Crear y editar sedes y ciudades | Sí | Sí | — | — | — | Reservado | |
| Administración | Consultar proveedores | Sí | Sí | Sí | — | Sí | Sí | |
| Administración | Crear y editar proveedores | Sí | Sí | — | — | — | Reservado | |
| Administración | Consultar entidades financieras | Sí | Sí | Sí | Sí | — | Sí | |
| Administración | Crear y editar financieras, reglas e intermediación | Sí | Sí | — | — | — | Reservado | |
| Administración | Consultar catálogos | Sí | Sí | Sí | Sí | Sí | Sí | |
| Administración | Crear y editar catálogos | Sí | Sí | — | — | — | Reservado | |
| Administración | Guardar filtros propios | Sí | Sí | Sí | Sí | Sí | Sí | |
| Administración | Gestionar usuarios y ver sus permisos | Sí | Sí | — | — | — | Reservado | |
| Administración | Otorgar permisos extra | Sí | — | — | — | — | Reservado | |
| Administración | Fijar la tasa de intermediación | Sí | — | — | — | — | Reservado | |

### Qué hace cada permiso (en una línea)

La descripción que ve el Super Administrador en la ficha del usuario:

- **Consultar inventario:** ver el listado y la ficha de los equipos de tu alcance.
- **Exportar e imprimir el inventario:** descargar en Excel e imprimir el listado de equipos filtrado.
- **Ver costo y ganancia:** ver el costo y la ganancia en todos los módulos: inventario, ventas, garantías, exportaciones y tablero.
- **Ver historial del equipo:** consultar los cambios registrados de cada equipo de tu alcance. Sin «Ver costo y ganancia», el historial oculta esos valores.
- **Cambiar el estado de un equipo:** cambiar el estado operativo de un equipo de tu alcance, con motivo.
- **Registrar y consultar ingresos:** registrar ingresos de mercancía en tu sede y consultarlos.
- **Gestionar traslados:** crear, despachar, recibir, rechazar y anular los traslados de tu sede, con sus documentos.
- **Consultar parámetros de precio:** consultar los parámetros de precio vigentes y su historial.
- **Editar la ficha, el costo y los precios del equipo:** corregir costo, ganancia definida, factura del proveedor, guía, fecha de pedido, RAM, almacenamiento, color, batería y observaciones, y fijar precios desde la tabla, uno por uno o en masa.
- **Consultar ventas:** ver el listado y el detalle de las ventas de tu alcance.
- **Registrar ventas:** cotizar, imprimir el comprobante, cargar la imagen, buscar y crear clientes y consultar tu tope de descuento.
- **Exportar el listado de ventas:** descargar el listado de ventas filtrado.
- **Solicitar modificaciones y anulaciones:** pedir la modificación o la anulación de una venta, con justificación, y seguir tus solicitudes.
- **Ver historial de la venta:** consultar quién pidió, quién aprobó y qué cambió en cada venta de tu alcance.
- **Registrar abonos de cartera propia:** registrar abonos de las ventas de cartera propia de tu alcance.
- **Ver la caja dentro de la venta:** ver en el detalle de cada venta los movimientos de caja que generó.
- **Consultar topes de descuento / Consultar el texto de aceptación:** ver los topes de todos los roles y su historial / las versiones del texto de aceptación y habeas data del comprobante.
- **Registrar y consultar movimientos de caja:** registrar ingresos y egresos de caja de tu sede, consultarlos y ver el saldo.
- **Cuadres de caja:** hacer, consultar, imprimir y exportar el cuadre diario de tu sede, y pedir su rectificación.
- **Consultar reemplazos por garantía / Registrar reemplazos por garantía:** ver los reemplazos de tu alcance, con sus costos / reemplazar por garantía el equipo de una venta de tu alcance.
- **Consultar metas:** ver e imprimir las metas comerciales de tu alcance.
- **Tablero de ventas / de inventario / de metas:** ver los indicadores de tu alcance (el de ventas permite además descargar su serie y su desglose).
- **Consultar sedes y ciudades, proveedores, entidades financieras y catálogos:** verlos (para elegirlos en los formularios).
- **Guardar filtros propios:** guardar, usar y borrar tus propios filtros de pantalla.

Los permisos **reservados** se describen como «Reservado a los roles administrativos» o «Reservado al Super Administrador» y nunca se otorgan como extra.

## Permisos extra

- **Quién los otorga:** solo el **Super Administrador** (permiso «Otorgar permisos extra»).
- **A quién:** a un Administrador de Punto, un Vendedor o un Bodeguero. El Super Administrador y el Administrador ya traen de base todo lo otorgable.
- **Qué hacen:** suman acciones **dentro de tu alcance**. No amplían el alcance de los datos operativos: un Vendedor con un permiso extra sigue limitado a su sucursal para esos datos. Esto no impide consultar catálogos de apoyo, como la lista de sedes.
- **Pueden abrir un módulo.** Un permiso extra suma al menú el módulo al que pertenece (por ejemplo, «Consultar ventas» le abre Ventas a un Bodeguero). Las lecturas de apoyo (sedes y ciudades, proveedores, entidades financieras, catálogos y filtros guardados) **no** abren módulo.
- **Dependencias.** Algunos permisos exigen que tengas otros (columna «Requiere antes»). Si falta alguno, el permiso extra se guarda pero **no tiene efecto** hasta que tengas lo que exige. Un ejemplo: «Registrar y consultar ingresos» exige «Ver costo y ganancia» y «Consultar proveedores».
- **Si cambias el rol de alguien,** los permisos extra que el nuevo rol ya trae de base se descartan; los demás se conservan guardados. Hacia Super Administrador o Administrador la lista de extras queda vacía.
- **Permisos que no tienes por rol pero sí por extra.** Por ejemplo, a un Bodeguero con «Registrar y consultar movimientos de caja» se le muestra Ventas con la pantalla Caja.

Mira la pantalla donde se administran: [Permisos de un usuario](../administracion/usuario-detalle-y-permisos.md).

## Datos sensibles: quién los ve

Cada dato tiene una regla de visibilidad que se cumple en **todos** los módulos, pantallas, archivos exportados e impresiones:

| Dato | Lo ven por rol | Permiso extra que lo abre |
|---|---|---|
| Costo y ganancia | Super Administrador, Administrador, Administrador de Punto, Bodeguero | «Ver costo y ganancia» |
| Movimientos de caja dentro de la venta | Super Administrador, Administrador, Administrador de Punto | «Ver la caja dentro de la venta» |
| Nombre del proveedor | Super Administrador, Administrador, Administrador de Punto, Bodeguero | «Consultar proveedores» |

El Bodeguero ve el costo aunque no tenga el módulo de Ventas: si un permiso extra le abre Ventas, verá las ventas **con** costo, como el Administrador de Punto.

## Solo el Super Administrador

Algunas cosas las fija únicamente el Super Administrador: publicar nuevos parámetros de precio, los topes de descuento, el texto de aceptación y la tasa de intermediación de una financiera; y otorgar permisos extra.

## Qué ve cada rol

| Rol | Resumen |
|---|---|
| Super Administrador | Todo. Único que otorga permisos extra y publica parámetros de precio, topes, texto de aceptación e intermediación |
| Administrador | Todos los módulos y todo lo reservado a «roles administrativos», menos lo exclusivo del Super Administrador. Puede editar precios de equipos; crear parámetros de precio es otra acción |
| Administrador de Punto | Su sucursal: inventario, ventas, caja, garantías (consulta), metas y tableros de ventas, inventario y metas |
| Vendedor | Su sucursal: ve inventario (equipos), ventas y solicitudes, metas y tableros de ventas y metas; no ve costos ni caja |
| Bodeguero | Inventario de su ubicación, con costo y proveedor; nada más sin permisos extra |

## Relación con otros módulos

**Necesitas antes:**
- Que exista el usuario y su rol: [Usuarios](../administracion/usuarios.md).
- Lecturas de apoyo, según la tarea que realices: [Menú lateral y navegación](menu-y-navegacion.md); [Primeros pasos: ingresar, salir y mantener tu sesión](primeros-pasos.md); [Sucursales](../administracion/sucursales.md).

**Esto afecta a:**
- [Menú y navegación](menu-y-navegacion.md): los módulos y pantallas que ves.
- [Usuarios y permisos](../administracion/usuario-detalle-y-permisos.md): donde se otorgan los permisos extra.
- Cada pantalla de cada módulo muestra u oculta botones y columnas según esta página.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «No tienes permiso para acceder a esta sección.» | Tu usuario no tiene ese módulo o esa pantalla | Pide al Super Administrador que revise tus permisos |
| «No tienes permiso para ver esta información.» | El sistema rechazó un dato o una acción por tu rol | Igual que arriba |
| «Tu sesión llegó sin permisos: el servidor puede estar desactualizado. Avísale al administrador del sistema.» | No se entregó tu lista de permisos | Cierra sesión y avisa al administrador |

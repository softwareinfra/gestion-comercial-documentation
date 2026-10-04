# Detalle de un usuario y sus permisos

La ficha de un usuario es donde cambias sus datos, le pones la contraseña, lo deshabilitas o anulas, y (solo el Super Administrador) le sumas **permisos extra** sobre lo que ya trae su rol. También aquí está la lista completa de esos permisos y las reglas del rol Bodeguero.

> **Quién puede hacerlo:** Super Administrador y Administrador, con límites (ver la tabla «Quién gestiona a quién»). Los permisos extra los otorga **solo** el Super Administrador.
> **Dónde está:** menú lateral → Administración → Usuarios → clic en el nombre de usuario.

## Antes de empezar

- **Rol y permisos:** cada rol trae un conjunto de permisos (lo que puede hacer). Un **permiso extra** es uno más que le sumas a una persona concreta, sin cambiarle el rol. Ver [Roles y permisos](../general/roles-y-permisos.md).
- **Estados de un usuario:** **Activo** (puede entrar), **Deshabilitado** (no puede entrar; se puede volver a activar) y **Anulado** (definitivo: queda solo de lectura, no puede entrar ni recibir otra contraseña y no tiene acciones).
- Para crear un usuario y entender el nombre de usuario, la sucursal y el listado, ve a [Usuarios](usuarios.md).

### Quién gestiona a quién

| Quien está en sesión | Puede editar, asignar contraseña y deshabilitar/anular/activar a… | Sobre sí mismo |
|---|---|---|
| Super Administrador | Cualquier usuario | Puede editar su nombre, documento, teléfono y correo, y asignarse contraseña. **No** puede cambiarse el rol ni la sucursal, ni deshabilitarse o anularse. |
| Administrador | Solo Administrador de Punto, Vendedor y Bodeguero | Solo consulta su ficha. No puede editarse ni cambiarse la contraseña. |

Sobre un Administrador o un Super Administrador, el Administrador ve la ficha pero sin ningún botón de acción y sin la sección «Permisos». Si el sistema lo rechaza de todos modos, dice «Solo un Super Administrador puede gestionar usuarios con rol administrativo.»

## Cómo ver la ficha de un usuario

1. En Administración → Usuarios, haz clic en el nombre de usuario de la persona.
2. Arriba verás el enlace **Volver a Usuarios** y, como título, el nombre y apellido de la persona.
3. La ficha muestra: **Nombre de usuario**, **Documento**, **Teléfono**, **Correo electrónico** (con «—» si no tiene), **Rol**, **Sucursal** (con «—» si no tiene), **Estado**, **Creado el** y **Actualizado el** (en formato día/mes/año). Si la persona fue deshabilitada aparece **Deshabilitado el**; si fue anulada, **Anulado el**.
4. Si la dirección no lleva un número de usuario válido, verás el título «Usuario» y el aviso «No se encontró el usuario.» Si lleva un número que no corresponde a ninguna persona, verás el aviso «No se encontró el registro.» con el botón **Reintentar**.

Los botones de la cabecera cambian según quién eres y a quién miras: **Editar**, **Asignar contraseña**, **Editar permisos** y tres botones con icono (Deshabilitar, Anular, Activar). Si un botón no aparece es porque tu rol no puede hacer esa acción sobre esa persona.

## Cómo editar los datos de un usuario

> **Quién puede hacerlo:** Super Administrador (a cualquiera) y Administrador (a Administrador de Punto, Vendedor y Bodeguero). Un usuario anulado no se edita.

1. En la ficha, haz clic en **Editar**.
2. Se abre el diálogo «Editar usuario». Cambia lo que necesites: **Nombre**, **Apellido**, **Número de documento**, **Teléfono**, **Correo electrónico**, **Rol**, **Sucursal**. Los campos y sus reglas son los mismos del alta (ver [Qué significa cada campo](usuarios.md#qué-significa-cada-campo)).
3. Haz clic en **Guardar**.

Al terminar verás la ficha actualizada. El nombre de usuario **no** cambia aunque cambies el nombre o el apellido.

Cosas que conviene saber:

- Si editas **tu propia** ficha (solo el Super Administrador puede), los campos Rol y Sucursal aparecen bloqueados y el diálogo dice «Tu propio rol y tu propia sucursal no se pueden modificar.»
- Un usuario **deshabilitado** sí se puede editar; uno **anulado** no.
- Si cambias el rol de alguien a Administrador de Punto, Vendedor o Bodeguero, debes elegir su sucursal. Si lo cambias a Administrador o Super Administrador, la sucursal es opcional.
- Si cambias el rol, los **permisos extra** de la persona se ajustan solos (ver [Qué pasa con los permisos extra cuando cambias el rol](#qué-pasa-con-los-permisos-extra-cuando-cambias-el-rol)).
- Si la sucursal de la persona fue deshabilitada, el desplegable **Sucursal** solo ofrece sucursales activas y puede mostrar «Sin sucursal» en vez del nombre de la sede. Si no tocas ese campo, el sistema conserva la sucursal que ya tenía.

## Asignar una contraseña

> **Quién puede hacerlo:** Super Administrador (a cualquiera, incluido él mismo) y Administrador (a Administrador de Punto, Vendedor y Bodeguero; no a sí mismo). A un usuario anulado no se le puede asignar otra contraseña ni permitir el ingreso.

Es lo que tienes que hacer después de crear a alguien, o cuando la persona olvidó su contraseña.

1. En la ficha, haz clic en **Asignar contraseña**.
2. Se abre el diálogo «Asignar contraseña: *nombre de usuario*». Dice: «La contraseña reemplaza de inmediato a la anterior y no vuelve a mostrarse.»
3. Escribe la **Contraseña nueva**. Para comprobar lo que escribiste, mantén presionado el ojo que está al lado («Mantén presionado el ojo para ver la contraseña.»), por ejemplo para dictársela a la persona.
4. Haz clic en **Asignar contraseña**. Mientras se envía el botón dice «Enviando…».

Al terminar verás en la ficha el mensaje «Contraseña asignada correctamente.»

Reglas de la contraseña:

- Máximo 128 caracteres. Los espacios cuentan como parte de la contraseña (no se recortan).
- No puede parecerse demasiado a los datos de la persona (nombre de usuario, nombre, etc.): el sistema dice «La contraseña se parece demasiado a un dato del usuario: …».
- El sistema también rechaza contraseñas demasiado cortas, demasiado comunes o formadas solo por números. Si aparece un aviso de contraseña no válida, revisa lo que señala y usa una contraseña más larga, que no sea común ni esté formada solo por números.

## Deshabilitar, activar o anular a un usuario

> **Quién puede hacerlo:** Super Administrador (a cualquier otro usuario) y Administrador (a Administrador de Punto, Vendedor y Bodeguero). Nadie puede deshabilitarse ni anularse a sí mismo: en tu propia ficha estos botones no aparecen.

Qué botones ves según el estado de la persona (son iconos; al pasar el mouse dicen su nombre):

| Estado actual | Botones |
|---|---|
| Activo | **Deshabilitar** y **Anular** |
| Deshabilitado | **Activar** y **Anular** |
| Anulado | Ninguno: es definitivo |

Pasos:

1. En la ficha, haz clic en el icono de la acción (**Deshabilitar**, **Activar** o **Anular**).
2. Se abre un diálogo con el nombre de la acción y el nombre de usuario, por ejemplo «Deshabilitar: ana.rojas», y una explicación:
   - Deshabilitar: «El registro deja de estar operativo, pero puede activarse de nuevo más adelante.»
   - Activar: «El registro vuelve a estar operativo.»
   - Anular: «La anulación es definitiva: el registro queda de solo lectura y no puede editarse ni reactivarse.»
3. Escribe el **Motivo**. Es obligatorio; sin motivo el sistema dice «El motivo es obligatorio.»
4. Haz clic en el botón de confirmar: **Deshabilitar**, **Activar** o **Anular definitivamente**.

Al terminar verás la ficha con el nuevo **Estado** y la fecha (**Deshabilitado el** o **Anulado el**). Una persona deshabilitada o anulada ya no puede iniciar sesión. Cada cambio queda registrado con su motivo.

Si una acción no se puede hacer, el sistema lo dice en el diálogo:

| Lo que ves | Qué significa |
|---|---|
| «El usuario ya está deshabilitado.» / «El usuario ya está activo.» | Otra persona ya hizo ese cambio; recarga la ficha. |
| «La anulación es terminal: el usuario no cambia más.» | El usuario ya estaba anulado. |
| «La autodesactivación está prohibida.» / «La autoanulación está prohibida.» | Intentaste hacerlo sobre tu propia cuenta. |
| «El sistema no puede quedarse sin Super Administrador activo.» | El sistema protege que siempre haya al menos un Super Administrador activo. |

## Permisos extra por usuario

### Cómo ver los permisos de una persona

> **Quién puede verlos:** Super Administrador y Administrador, pero este último solo los de Administrador de Punto, Vendedor y Bodeguero.

En la ficha, debajo de los datos, está la sección **Permisos**:

- Si miras a un **Administrador de Punto, un Vendedor o un Bodeguero**, verás un resumen con el formato «Incluidos por el rol: N · Extra: M» (si hay permisos que no hacen efecto, se agrega «· Sin efecto: K») y la lista completa agrupada por módulo: Inventario, Ventas, Caja, Garantías, Metas, Tablero y Administración. Cada grupo dice cuántos permisos tiene la persona («X de N»).
- Si eres Super Administrador y miras a otro **Super Administrador o Administrador**, solo verás: «El Super Administrador y el Administrador ya traen todo lo que se puede otorgar.»
- Si eres Administrador, o si la persona está anulada, la lista es solo de lectura y te lo dice: «Solo lectura: no tienes permiso para otorgar permisos extra.» o «La anulación es terminal: el usuario no cambia más.»

Cada fila de la lista está en una de estas clases:

| Cómo se ve | Qué significa |
|---|---|
| Casilla marcada y bloqueada, con la etiqueta **Incluido por el rol** | El rol ya lo trae; no se puede quitar. |
| Casilla marcada, sin etiqueta | Es un permiso extra que tiene la persona. |
| Casilla marcada con la etiqueta **Sin efecto** y una nota «Sin efecto: le falta «…».» | Se le otorgó, pero no funciona porque le falta otro permiso del que depende. Sigue guardado. |
| Un candado y la etiqueta **Reservado** | No se puede otorgar como extra a nadie. |
| Nota «Requiere «…».» bajo el nombre | Para que funcione necesita ese otro permiso. |

### Cómo otorgar o quitar permisos extra

> **Quién puede hacerlo:** solo el Super Administrador, a un Administrador de Punto, un Vendedor o un Bodeguero. Nadie puede otorgarse permisos a sí mismo, y un usuario anulado no cambia más (uno deshabilitado sí).

1. Abre la ficha de la persona.
2. Haz clic en **Editar permisos** (botón de la cabecera).
3. Se abre el diálogo «Editar permisos» («Suma permisos a los que trae el rol. Rigen desde la próxima vez que la persona abra el sistema.»).
4. Marca las casillas de los permisos que quieres sumar. Para quitar un extra, desmárcalo. Los permisos «Incluido por el rol» no se pueden desmarcar y los «Reservado» no tienen casilla.
5. Si el permiso que marcaste necesita otros, el sistema los marca por ti y te avisa: «También se marcó «Ver costo y ganancia»: la requiere «Registrar y consultar ingresos».» Si desmarcas uno del que otros dependen, también desmarca esos: «También se desmarcó «…»: requiere «…».»
6. (Opcional) Escribe el **Motivo (opcional)**: por qué le otorgas esos permisos (hasta 500 caracteres; un contador dice «0 de 500»). Queda en el registro de cambios.
7. Haz clic en **Guardar permisos**. El botón está deshabilitado hasta que cambies algo. Mientras se envía dice «Guardando…».

Al terminar verás el mensaje «Permisos guardados. *Nombre* los verá la próxima vez que abra el sistema.» y la lista actualizada. La persona verá los cambios en su menú y sus pantallas la próxima vez que abra el sistema.

Para quitarle **todos** los extra, desmarca todos y guarda.

Reglas que conviene recordar:

- Lo que se guarda **reemplaza** la lista anterior por la que dejaste marcada.
- Un extra no amplía el alcance de sus **operaciones** a otra sucursal. Puede dar acceso a catálogos nacionales de apoyo (sedes, ciudades, proveedores, financieras o catálogos), sin permitir consultar las operaciones de otra sede.
- Cada extra efectivo suma al menú el módulo que abre. Ejemplo: a un Bodeguero con «Consultar ventas» le aparece Ventas en el menú. Ningún permiso extra abre el módulo **Administración**.
- Un extra de **Ventas**, **Garantías** o **Tablero** dado a un **Bodeguero** le muestra también el costo y la ganancia en esos módulos, porque su rol ya ve el costo.
- Cada cambio queda registrado con quién lo hizo, qué cambió y el motivo. Si haces muchos cambios seguidos, el sistema limita la velocidad (30 por minuto en la configuración de base). El límite de tu instalación puede variar; si aparece un aviso, espera el tiempo indicado antes de repetir.

### Qué pasa con los permisos extra cuando cambias el rol

- Los extra de la persona se **conservan**, menos los que el nuevo rol ya trae.
- Si la pasas a **Administrador o Super Administrador**, se quitan todos (esos roles ya traen todo lo otorgable).
- Un extra que queda sin el permiso del que depende sigue guardado pero queda **Sin efecto** hasta que vuelva a cumplirse.
- Si el cambio de rol prende o apaga extras, el registro del cambio lo deja anotado.

### Avisos que puedes ver en el diálogo

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Estos permisos guardados no se pueden otorgar y no tienen efecto: «…». Se quitan la próxima vez que se guarden los permisos.» | La persona tiene guardado algo que ya no es otorgable. | Se limpian al guardar un cambio autorizado en la selección de permisos otorgables. Si no hay un cambio que hacer, avisa al Super Administrador responsable. |
| ««X» requiere «Y».» | Faltó un permiso del que depende otro. | Marca también «Y». |
| ««X» es un permiso reservado: no se otorga como extra.» | Intentaste otorgar un permiso de la clase **Reservado**. | Quítalo. |
| «Solo el Super Administrador otorga permisos extra.» | Tu rol no puede otorgar. | Pídeselo a un Super Administrador. |
| «Nadie se otorga permisos a sí mismo.» | Intentaste darte permisos. | Pídeselo a otro Super Administrador. |
| «Los permisos extra son para Administradores de Punto, Vendedores y Bodegueros: el Super Administrador y el Administrador ya traen todo lo que se puede otorgar.» | La persona tiene un rol que no recibe extras. | Nada: ya tiene todo. |
| «La anulación es terminal: el usuario no cambia más.» | El usuario está anulado. | Nada. |
| «No se pudo contactar con el servidor. Vuelve a intentarlo: guardar otra vez no duplica nada.» | Se cayó la conexión. | Vuelve a guardar. |
| «No se pudo confirmar si se guardaron los permisos: al cerrar, la ficha se vuelve a leer.» | No se sabe si el cambio se aplicó. | Cierra el diálogo y revisa la ficha. |
| «No se pudieron guardar los permisos. Vuelve a intentarlo.» | Falló el servidor. | Intenta de nuevo. |

**Guardar permisos** permanece deshabilitado si no cambias la selección de permisos otorgables; escribir solo el motivo no lo habilita. No otorgues ni quites permisos arbitrariamente para limpiar el aviso. Si el aviso anuncia que quitará permisos sin efecto al guardar, recuerda que el botón se habilita al cambiar la selección de permisos otorgables; el motivo por sí solo no lo habilita.

## Lista completa de permisos extra

El catálogo tiene **47 permisos**: **31 se pueden otorgar** como extra y **16 son reservados**. Los nombres de abajo son los que ves en la pantalla. Las columnas «Ya lo trae el rol» dicen si el Administrador de Punto (AP), el Vendedor (V) o el Bodeguero (B) lo tienen sin necesidad de extra: en ese caso aparece «Incluido por el rol» y no hay nada que otorgar. El Super Administrador y el Administrador ya traen los 31.

Los textos dicen «tu alcance» o «tu sede»: se refieren al alcance operativo de **esa persona** (su sucursal). Las lecturas nacionales de apoyo son la excepción descrita en el grupo Administración.

### Permisos que se pueden otorgar (31)

**Inventario**

| Permiso | Qué hace | Requiere | AP | V | B |
|---|---|---|:-:|:-:|:-:|
| Consultar inventario | Ver el listado y la ficha de los equipos de su alcance. | — | Sí | Sí | Sí |
| Exportar e imprimir el inventario | Descargar en Excel e imprimir el listado de equipos filtrado. | — | Sí | Sí | Sí |
| Ver costo y ganancia | Ver el costo y la ganancia en todos los módulos: inventario, ventas, garantías, exportaciones y tablero. | — | Sí | No | Sí |
| Ver historial del equipo | Consultar los cambios registrados de cada equipo de su alcance. Sin «Ver costo y ganancia», el historial oculta esos valores. | — | Sí | No | Sí |
| Cambiar el estado de un equipo | Cambiar el estado operativo de un equipo de su alcance, con motivo. | — | Sí | No | Sí |
| Registrar y consultar ingresos | Registrar ingresos de mercancía en su sede y consultarlos. | Ver costo y ganancia; Consultar proveedores | Sí | No | Sí |
| Gestionar traslados | Crear, despachar, recibir, rechazar y anular los traslados de su sede, con sus documentos. | — | Sí | No | Sí |
| Consultar parámetros de precio | Consultar los parámetros de precio vigentes y su historial. | Ver costo y ganancia | Sí | No | Sí |
| Editar la ficha, el costo y los precios del equipo | Corregir el costo, la ganancia definida, el número de factura del proveedor, el número de guía, la fecha de pedido, la RAM, la capacidad de almacenamiento, el color, el porcentaje de batería y las observaciones de los equipos de su alcance, y fijar sus precios desde la tabla, uno por uno o en masa. | Ver costo y ganancia | No | No | No |

**Ventas**

| Permiso | Qué hace | Requiere | AP | V | B |
|---|---|---|:-:|:-:|:-:|
| Consultar ventas | Ver el listado y el detalle de las ventas de su alcance. | — | Sí | Sí | No |
| Registrar ventas | Registrar ventas en su sede: cotizar, imprimir el comprobante, cargar la imagen, buscar y crear clientes y consultar su tope de descuento. | Consultar ventas; Consultar entidades financieras | Sí | Sí | No |
| Exportar el listado de ventas | Descargar el listado de ventas filtrado. | Consultar ventas | Sí | Sí | No |
| Solicitar modificaciones y anulaciones | Pedir la modificación o la anulación de una venta, con justificación, y seguir sus solicitudes. | Consultar ventas; Consultar entidades financieras | Sí | Sí | No |
| Ver historial de la venta | Consultar quién pidió, quién aprobó y qué cambió en cada venta de su alcance. | Consultar ventas | Sí | No | No |
| Registrar abonos de cartera propia | Registrar los abonos de las ventas de cartera propia de su alcance. | Consultar ventas | Sí | No | No |
| Ver la caja dentro de la venta | Ver en el detalle de cada venta los movimientos de caja que generó. | Ver costo y ganancia; Consultar ventas | Sí | No | No |
| Consultar topes de descuento | Ver los topes de descuento de todos los roles y su historial. | — | No | No | No |
| Consultar el texto de aceptación | Ver las versiones del texto de aceptación y habeas data del comprobante. | — | No | No | No |

**Caja**

| Permiso | Qué hace | Requiere | AP | V | B |
|---|---|---|:-:|:-:|:-:|
| Registrar y consultar movimientos de caja | Registrar ingresos y egresos de caja de su sede, consultarlos y ver el saldo. | — | Sí | No | No |
| Cuadres de caja | Hacer, consultar, imprimir y exportar el cuadre diario de caja de su sede, y pedir su rectificación. | — | Sí | No | No |

**Garantías**

| Permiso | Qué hace | Requiere | AP | V | B |
|---|---|---|:-:|:-:|:-:|
| Consultar reemplazos por garantía | Ver los reemplazos por garantía de su alcance, con sus costos. | Ver costo y ganancia | Sí | No | No |
| Registrar reemplazos por garantía | Reemplazar por garantía el equipo de una venta de su alcance. | Ver costo y ganancia; Consultar reemplazos por garantía | No | No | No |

**Metas**

| Permiso | Qué hace | Requiere | AP | V | B |
|---|---|---|:-:|:-:|:-:|
| Consultar metas | Ver e imprimir las metas comerciales de su alcance. | — | Sí | Sí | No |

**Tablero**

| Permiso | Qué hace | Requiere | AP | V | B |
|---|---|---|:-:|:-:|:-:|
| Tablero de ventas | Ver los indicadores de ventas de su alcance y descargar su serie y su desglose. | — | Sí | Sí | No |
| Tablero de inventario | Ver el estado, la distribución y la rotación del inventario de su alcance. | Ver costo y ganancia | Sí | No | No |
| Tablero de metas | Ver el avance de las metas de su alcance. | — | Sí | Sí | No |

**Administración** (son lecturas de apoyo: dejan elegir en los formularios de otros módulos y **no** agregan Administración al menú)

| Permiso | Qué hace | Requiere | AP | V | B |
|---|---|---|:-:|:-:|:-:|
| Consultar sedes y ciudades | Ver el catálogo de sedes y ciudades. | — | Sí | Sí | Sí |
| Consultar proveedores | Ver los proveedores y el nombre del proveedor en el inventario, los ingresos y las exportaciones. | — | Sí | No | Sí |
| Consultar entidades financieras | Ver las entidades financieras para registrar ventas. | — | Sí | Sí | No |
| Consultar catálogos | Ver marcas, tipos de producto, sistemas operativos, referencias, categorías, medios de pago, categorías de caja y estados. | — | Sí | Sí | Sí |
| Guardar filtros propios | Guardar, usar y borrar tus propios filtros de pantalla. | — | Sí | Sí | Sí |

### Permisos reservados (16): no se otorgan como extra

En el diálogo aparecen con un candado y la etiqueta **Reservado**, sin casilla. Los traen por rol el Super Administrador y el Administrador, salvo los cinco marcados «solo Super Administrador».

| Permiso | Qué hace | Quién lo trae por rol |
|---|---|---|
| Crear parámetros de precio | Publicar una versión nueva de los parámetros de precio. | Solo Super Administrador |
| Ficha, corrección e historial de clientes | Consultar la ficha completa de un cliente, corregirla y ver su historial. | Super Administrador y Administrador |
| Aprobar o rechazar modificaciones y anulaciones | Resolver las solicitudes de modificación y de anulación de ventas. | Super Administrador y Administrador |
| Crear topes de descuento | Publicar una versión nueva del tope de descuento de un rol. | Solo Super Administrador |
| Crear el texto de aceptación | Publicar una versión nueva del texto de aceptación. | Solo Super Administrador |
| Reversar movimientos de caja | Corregir un movimiento de caja con un contramovimiento. | Super Administrador y Administrador |
| Aprobar o rechazar rectificaciones de cuadre | Resolver las solicitudes de rectificación de un cuadre de caja. | Super Administrador y Administrador |
| Crear, editar, deshabilitar y activar metas | Gestionar las metas comerciales (valen para cualquier sede, ciudad o la empresa entera). | Super Administrador y Administrador |
| Informe de financieras | Ver créditos y fechas de corte y pago por financiera. | Super Administrador y Administrador |
| Crear y editar sedes y ciudades | Crear, editar, deshabilitar, anular y activar sedes, y crear y editar ciudades. | Super Administrador y Administrador |
| Crear y editar proveedores | Crear, editar, deshabilitar, anular y activar proveedores. | Super Administrador y Administrador |
| Crear y editar financieras, reglas e intermediación | Gestionar las entidades financieras, sus reglas de corte y pago y el historial de su intermediación. | Super Administrador y Administrador |
| Crear y editar catálogos | Crear y editar los catálogos administrables. | Super Administrador y Administrador |
| Gestionar usuarios y ver sus permisos | Crear, editar, deshabilitar, anular y activar usuarios, asignarles la contraseña y ver sus permisos. | Super Administrador y Administrador |
| Otorgar permisos extra | Sumar permisos extra a Administradores de Punto, Vendedores y Bodegueros. | Solo Super Administrador |
| Fijar la tasa de intermediación | Publicar una versión nueva de la intermediación de una financiera. | Solo Super Administrador |

## El rol Bodeguero

El Bodeguero es un rol de sede: sus operaciones se acotan a **una ubicación asignada**; también consulta los catálogos nacionales de apoyo indicados abajo. En pantalla se asigna en el campo **Sucursal**, igual que a los demás roles de sede.

Qué trae por rol (antes de cualquier permiso extra):

- **Módulo:** solo **Inventario**. No ve Ventas, Garantías, Metas ni el Tablero en su menú.
- **Inventario:** consultar inventario, exportar e imprimir, ver costo y ganancia, ver historial del equipo, cambiar el estado de un equipo, registrar y consultar ingresos, gestionar traslados y consultar parámetros de precio. **No** puede editar la ficha, el costo ni los precios del equipo (ese permiso, «Editar la ficha, el costo y los precios del equipo», no lo trae; se le puede otorgar como extra).
- **Lecturas de apoyo:** ve sedes y ciudades, proveedores (incluido el nombre del proveedor), catálogos y guarda sus filtros. **No** ve entidades financieras.
- **Datos sensibles:** ve el **costo y la ganancia** y el **nombre del proveedor**; **no** ve los movimientos de caja.

Reglas de la ubicación asignada:

- La sucursal es **obligatoria** (como para el Administrador de Punto y el Vendedor).
- Puede quedar en cualquier tipo de ubicación, no solo en una bodega: el sistema no valida el tipo.
- Sus datos y acciones operativos se acotan a **su** ubicación. Un permiso extra no amplía ese alcance operativo; las lecturas de apoyo pueden abarcar catálogos nacionales.
- Lo crea, edita, deshabilita y le asigna contraseña un Super Administrador o un Administrador; solo el Super Administrador le otorga permisos extra.

Si le otorgas un extra que lo lleve a **Ventas, Garantías o el Tablero**, verá el costo y la ganancia allí también.

## Qué ve cada rol

| Rol | Ve la ficha | Puede editar | Asignar contraseña | Deshabilitar / anular / activar | Ver sus permisos | Otorgar extras |
|---|---|---|---|---|---|---|
| Super Administrador | Sí, de todos | A cualquiera (a sí mismo, sin rol ni sucursal) | A cualquiera, incluido él mismo | A cualquier otro usuario (no a sí mismo) | Sí | Sí, a Administrador de Punto, Vendedor y Bodeguero (no a sí mismo) |
| Administrador | Sí, de todos | Solo Administrador de Punto, Vendedor y Bodeguero | Solo Administrador de Punto, Vendedor y Bodeguero | Solo Administrador de Punto, Vendedor y Bodeguero | Sí, de Administrador de Punto, Vendedor y Bodeguero (solo lectura) | No |
| Administrador de Punto | No | No | No | No | No | No |
| Vendedor | No | No | No | No | No | No |
| Bodeguero | No | No | No | No | No | No |

Lo que puede **recibir** cada rol como permiso extra: Administrador de Punto, Vendedor y Bodeguero (los 31 otorgables, salvo los que ya traen). Super Administrador y Administrador no reciben extras porque ya los traen todos.

## Relación con otros módulos

**Necesitas antes:**
- [Usuarios](usuarios.md): el usuario tiene que existir.
- [Sucursales](sucursales.md): para los roles de sede, la sucursal asignada tiene que estar creada y activa.
- Saber qué trae cada rol: [Roles y permisos](../general/roles-y-permisos.md).

**Esto afecta a:**
- Todos los módulos: lo que la persona ve y puede hacer depende de su rol, su sucursal y sus extras. Cada extra efectivo que abre un módulo lo suma al menú; las lecturas de apoyo no agregan Administración: [Equipos](../inventario/equipos.md), [Precios](../inventario/precios.md), [Ingresos](../inventario/ingresos.md), [Traslados](../inventario/traslados.md), [Ventas](../ventas/ventas.md), [Registrar una venta](../ventas/nueva-venta.md), [Solicitudes](../ventas/solicitudes.md), [Topes de descuento](../ventas/topes-de-descuento.md), [Texto de aceptación](../ventas/texto-de-aceptacion.md), [Caja](../ventas/caja.md), [Cuadres de caja](../ventas/cuadres-de-caja.md), [Equipos en garantía](../garantias/equipos-en-garantia.md), [Metas](../metas/metas.md), [Tablero de ventas](../dashboard/tablero-de-ventas.md) y [Tablero de inventario](../dashboard/tablero-de-inventario.md).
- [Proveedores](proveedores.md): «Consultar proveedores» decide si la persona ve el nombre del proveedor en inventario, ingresos y exportaciones.
- [Entidades financieras](entidades-financieras.md): «Consultar entidades financieras» es necesaria para registrar ventas y solicitar cambios.
- [Filtros guardados](../general/filtros-guardados.md): «Guardar filtros propios».
- Deshabilitar o anular a alguien le quita el acceso (ver [Primeros pasos](../general/primeros-pasos.md)).

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «No se encontró el usuario.» / «No se encontró el registro.» | La dirección no corresponde a un usuario. | Vuelve a Usuarios y entra desde la lista. |
| «No tienes permiso para ver esta información.» | Tu rol no puede hacer eso sobre esa persona. | Pídeselo a un Super Administrador. |
| Un aviso con el botón **Reintentar** («las sedes», «los permisos») | No cargó un dato de apoyo. | Haz clic en **Reintentar**. |
| «Cargando los permisos…» que no termina | Los permisos no respondieron. | Usa **Reintentar** si aparece, o recarga la página. |
| No aparece el botón **Editar permisos** | No eres Super Administrador, es tu propia ficha, el usuario está anulado, o su rol es Administrador o Super Administrador. | Revisa la tabla «Quién gestiona a quién». |
| «Tu sesión llegó sin permisos: el servidor puede estar desactualizado. Avísale al administrador del sistema.» | El servidor no mandó la lista de permisos de tu sesión. | Avisa al responsable del sistema; puedes cerrar sesión desde ese mismo aviso. |

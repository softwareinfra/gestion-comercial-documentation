# Primeros pasos: ingresar, salir y mantener tu sesión

Aquí aprendes a entrar a G5-Service, a qué pantalla llegas según tu usuario, cómo salir y qué pasa si dejas el sistema quieto un rato.

> **Quién puede hacerlo:** todos los roles (Super Administrador, Administrador, Administrador de Punto, Vendedor y Bodeguero).
> **Dónde está:** la pantalla de ingreso («G5-Service — Ingresa tu usuario y contraseña»). El botón para salir está abajo del menú lateral.

## Antes de empezar

- Necesitas un **usuario** y una **contraseña**. No hay una pantalla para registrarte tú mismo: tu cuenta la crea y la administra un administrador. Para saber quién puede crear usuarios y asignar contraseñas, mira [Usuarios](../administracion/usuarios.md).
- Usa el **nombre de usuario que te asignaron**. El sistema lo genera con el primer nombre y el primer apellido, en minúsculas y sin tildes, separados por un punto; si ya existe, agrega un número desde 2. Si falta uno de los dos, usa el disponible. No puedes cambiarlo. Mira [Usuarios](../administracion/usuarios.md).
- Tu cuenta tiene un **rol** (por ejemplo, Vendedor). El rol y los permisos extra que te haya dado el Super Administrador deciden qué menús ves. Mira [Roles y permisos](roles-y-permisos.md).

## Cómo iniciar sesión

1. Abre la dirección del sistema en tu navegador. Mientras el sistema revisa si ya tenías una sesión abierta, verás «Verificando la sesión…».
2. Si no tenías sesión, te llevará a la pantalla de ingreso, con el título **G5-Service** y el texto «Ingresa tu usuario y contraseña».
3. Escribe tu usuario en el campo **Usuario**.
4. Escribe tu contraseña en el campo **Contraseña**.
5. Haz clic en **Iniciar sesión**. Mientras el sistema verifica, el botón dice «Iniciando sesión…».

Al terminar verás: la primera pantalla de tu menú (mira «A qué pantalla llegas» más abajo).

### Ver lo que escribes en la contraseña

Junto al campo **Contraseña** hay un ojo. Dice «Mantén presionado el ojo para ver la contraseña.». **Mientras lo mantengas presionado** (con el mouse, con el dedo, o con la tecla Espacio o Enter) ves la contraseña; al soltarlo, vuelve a quedar oculta. Un clic rápido no la deja visible. Así nadie que pase detrás de ti la alcanza a leer por descuido.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Usuario | El usuario que te asignó el administrador | Sí |
| Contraseña | Tu contraseña | Sí |

## A qué pantalla llegas

Después de ingresar, el sistema te lleva al **primer módulo** de tu menú, en este orden fijo: Dashboard e Informes, Ventas, Inventario, Metas Comerciales, Garantías y Devoluciones, Administración. Cada módulo abre su primera pantalla disponible. En la práctica:

| Rol | Primer módulo | Pantalla con la que empiezas |
|---|---|---|
| Super Administrador | Dashboard e Informes | Tablero de ventas |
| Administrador | Dashboard e Informes | Tablero de ventas |
| Administrador de Punto | Dashboard e Informes | Tablero de ventas |
| Vendedor | Dashboard e Informes | Tablero de ventas (con tus ventas) |
| Bodeguero | Inventario | Equipos |

Un permiso extra puede cambiar esto: si a un Bodeguero le abren Ventas, por ejemplo, su primer módulo pasa a ser Ventas. Si tu usuario no tiene ningún módulo, ves este aviso: «Tu usuario no tiene módulos habilitados. Pídele a un administrador que revise tus permisos.»

## Cómo cerrar sesión

1. Mira la parte de abajo del menú lateral: verás tu nombre, tu rol y, si tienes sucursal asignada, el nombre de tu sucursal.
2. Haz clic en el botón con el icono de salida, a la derecha de tu nombre. Su nombre es **Cerrar sesión** (aparece al dejar el mouse encima).

Al terminar verás la pantalla de ingreso. Si el sistema no alcanza a confirmar el cierre, de todos modos te saca de la sesión en tu pantalla.

## Cuánto dura tu sesión

- **Por inactividad:** la sesión se cierra al superar el tiempo de inactividad configurado. El valor por defecto es **30 minutos**. El tiempo de tu instalación puede ser distinto; si necesitas conocerlo, consulta a tu administrador.
- **Mientras trabajas:** cada vez que haces clic, escribes o te desplazas por la pantalla, el sistema lo detecta y avisa (como máximo una vez por minuto) que sigues aquí. Por eso puedes llenar un formulario largo sin que se cierre la sesión.
- **Tope máximo:** la sesión tiene un tiempo máximo aunque estés activo. El valor por defecto es **12 horas**. El tiempo de tu instalación puede ser distinto.
- **Al cerrar el navegador:** normalmente la sesión termina, pero depende del navegador (algunos restauran la sesión al reabrir). No cuentes con eso: cierra sesión tú mismo en equipos compartidos.

### Si tu sesión se cierra mientras trabajas

1. Al hacer la siguiente acción, el sistema te lleva a la pantalla de ingreso.
2. Ingresa de nuevo.
3. Llegarás a tu pantalla inicial, **no** a la que estabas. Lo que tenías a medio escribir en un formulario se pierde.

## Qué ve cada rol

| Rol | Puede ingresar | Observaciones |
|---|---|---|
| Super Administrador | Sí | Sucursal opcional: ve todas aunque tenga una asignada |
| Administrador | Sí | Sucursal opcional: ve todas aunque tenga una asignada |
| Administrador de Punto | Sí | El pie del menú muestra su sucursal |
| Vendedor | Sí | El pie del menú muestra su sucursal |
| Bodeguero | Sí | El pie del menú muestra su ubicación asignada |

## Relación con otros módulos

**Necesitas antes:**
- Que un administrador haya creado tu usuario y te haya asignado una contraseña: [Usuarios](../administracion/usuarios.md).
- Para roles con sucursal, que tu usuario tenga sucursal asignada: [Sucursales](../administracion/sucursales.md).
- Lecturas de apoyo, según la tarea que realices: [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md).

**Esto afecta a:**
- [Menú y navegación](menu-y-navegacion.md): los módulos y pantallas que ves dependen de tu rol y permisos.
- [Roles y permisos](roles-y-permisos.md): qué puedes hacer en cada pantalla.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Credenciales inválidas o usuario sin acceso.» | El usuario o la contraseña no coinciden, o tu cuenta está deshabilitada o anulada. El sistema responde igual en todos esos casos, a propósito. | Revisa cómo escribes usuario y contraseña (usa el ojo). Si sigue igual, pídele a un administrador que revise tu cuenta. |
| «Demasiados intentos fallidos. Intenta de nuevo en unos minutos.» | Se alcanzó el límite de fallos con el mismo usuario desde la misma conexión a internet. Los valores por defecto son 6 fallos seguidos y 30 minutos de bloqueo; tu instalación puede usar otros. | Espera y vuelve a intentar. No sigas probando: cada fallo cuenta. |
| «Demasiados intentos. Espera un momento antes de volver a probar.» | Intentaste ingresar muchas veces en un minuto (el límite por defecto es de 10 por minuto; el de tu instalación puede variar). | Espera un momento y vuelve a intentar. |
| «No se pudo contactar con el servidor. Revisa tu conexión.» | Tu equipo no logra comunicarse con el sistema. | Revisa tu conexión a internet y vuelve a intentar. |
| «No se pudo contactar con el servidor.» (en lugar de la pantalla, sin botón) | Al abrir el sistema, no se pudo verificar tu sesión. | Recarga la página. Si sigue, avisa al administrador. |
| «Tu sesión llegó sin permisos: el servidor puede estar desactualizado. Avísale al administrador del sistema.» (con un botón **Cerrar sesión**) | El sistema no entregó tu lista de permisos. | Haz clic en **Cerrar sesión** y avisa al administrador. |
| «Tu usuario no tiene módulos habilitados. Pídele a un administrador que revise tus permisos.» | Tu usuario no tiene ningún módulo. | Pídele a un administrador que revise tu rol y permisos. |
| «Tu sesión expiró. Inicia sesión de nuevo.» | La sesión ya no es válida. Si llegas directamente a la pantalla de ingreso, inicia sesión de nuevo. | Ingresa de nuevo. |

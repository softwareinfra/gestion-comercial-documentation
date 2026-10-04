# Formularios y acciones comunes: crear, editar, deshabilitar y anular

Esta página explica cómo funcionan los formularios y los botones de acción que se repiten en todo el sistema. En las páginas de cada módulo solo se enlaza aquí.

> **Quién puede hacerlo:** depende de cada pantalla. Quien no puede crear o editar no ve el botón, o recibe un aviso de permiso. Mira [Roles y permisos](roles-y-permisos.md).
> **Dónde está:** en cualquier pantalla con un botón de alta (por ejemplo «Nueva ciudad») o con iconos de acción en cada fila.

## Antes de empezar

- Muchos formularios de alta y edición se abren encima de la pantalla, sobre un fondo atenuado, en un **diálogo**. Esta página explica ese patrón. Otros tienen página propia, como [Nueva venta](../ventas/nueva-venta.md) y [Crear traslado](../inventario/traslados.md), o se editan dentro de la tabla, como los precios de [Equipos](../inventario/equipos.md). Las instrucciones de X y Escape solo aplican al diálogo.
- Cuando se usa un diálogo, puede tener dos formas según el tamaño del formulario: un **panel lateral** pegado al borde derecho (formularios cortos, hasta ocho campos) o una **caja centrada** más ancha (formularios grandes).
- **En este sistema no se borra nada.** Lo que ya no se usa se **deshabilita** (se puede volver a activar) o se **anula** (es definitivo). Quedan registrados. La única excepción son los [filtros guardados](filtros-guardados.md).
- Los nombres de botones, campos y mensajes son los que verás en pantalla; cada pantalla tiene los suyos.

## Cómo crear algo (formulario en diálogo)

1. Haz clic en el botón principal del encabezado (por ejemplo **Nueva ciudad**).
2. Se abre el diálogo con un título, una línea que explica para qué sirve y, a la derecha arriba, una **X** (su nombre es «Cerrar»). El cursor ya queda en el primer campo.
3. Llena los campos. Los que son obligatorios no te dejan enviar el formulario vacío.
4. Haz clic en **Guardar**. Mientras se envía, el botón dice «Guardando…».

Al terminar, el diálogo se cierra y se actualiza el listado conservando la búsqueda y la página. El registro nuevo puede no aparecer con esos criterios.

Para **editar**, usa el icono del lápiz en la fila («Editar: nombre»). Se abre el mismo formulario con los datos ya escritos.

### Cómo cerrar un diálogo sin guardar

- Haz clic en **Cancelar**, en la **X**, o presiona **Escape**.
- Hacer clic en el fondo atenuado **no** cierra el diálogo (así no pierdes lo escrito por un clic sin querer).
- Mientras el formulario se está enviando **no se puede cerrar** (la X se apaga y Escape no hace nada). Espera a que termine.
- Con el teclado, **Tab** recorre solo los controles del diálogo; al cerrarlo, el cursor vuelve al botón que lo abrió.

## Qué pasa si hay errores

- Los errores de un campo salen **debajo de ese campo**, en rojo. Los lee en voz alta un lector de pantalla.
- Los errores que no son de un campo salen **arriba del formulario**.
- Los mensajes los escribe el sistema y se muestran tal cual. Si algo ya existe (por ejemplo una ciudad repetida), el mensaje lo dice.
- En el formulario de **nueva venta**, en el de **solicitud de modificación** y en el de **permisos de un usuario**, el sistema además te lleva al primer campo con error. En los demás, corrige mirando los mensajes en rojo.
- Cuando falla por permiso, ves «No tienes permiso para ver esta información.».
- Si se te cerró la sesión por inactividad mientras llenabas el formulario, el sistema te lleva a la pantalla de ingreso y lo escrito se pierde: mira [Primeros pasos](primeros-pasos.md).
- Si haces demasiadas acciones seguidas, el sistema responde «Hiciste demasiadas solicitudes seguidas.» y te dice cuánto esperar. Espera y vuelve a intentar.

### Tipos de campo que verás

| Campo | Cómo se usa |
|---|---|
| Texto | Escríbelo normalmente |
| Lista desplegable | Haz clic para abrirla y elegir. Con el teclado: flechas para moverte, Enter o Espacio para elegir, Escape para cerrarla, Inicio y Fin para ir al primero o al último, y una letra para saltar a la opción que empieza así. No es la lista nativa del navegador. |
| Dinero | En campos de pesos enteros puedes pegar «$ 1.200.000» o «1.200.000»: el sistema limpia los puntos de miles y el signo; al salir muestra separador de miles. No todos los importes son enteros: por ejemplo, Costo y Ganancia en la ficha del equipo admiten hasta dos decimales. Sigue la indicación del campo y la página de su módulo. |
| Fecha | Usa el selector de fecha del navegador |
| Contraseña | Con un ojo: mantén presionado para verla. Mira [Primeros pasos](primeros-pasos.md) |
| Motivo (texto largo) | Un cuadro de texto en los diálogos de deshabilitar, anular y activar |

## Cómo activar o desactivar con el interruptor «Activa»

En varios catálogos (por ejemplo Ciudades) hay una columna **Activa** con un interruptor.

1. Haz clic en el interruptor de la fila.
2. El cambio se guarda al instante y el listado se actualiza. Mientras se guarda, ese interruptor no responde.

Algunos registros vienen de fábrica con el sistema («semillas»): su interruptor queda bloqueado y no se pueden desactivar. Al dejar el mouse encima dice «Las semillas del sistema no se pueden desactivar.».

Si falla, el error aparece arriba de la tabla.

## Cómo deshabilitar, anular o volver a activar (con motivo)

En Proveedores, Sucursales y Entidades financieras, las acciones de ciclo de vida aparecen en la fila según el estado del registro. En [Usuarios](../administracion/usuario-detalle-y-permisos.md), aparecen en la cabecera de la ficha.

**Los tres estados** (se ven como una pastilla de color en la tabla):

| Estado | Qué significa | Acciones disponibles |
|---|---|---|
| Activo | El registro se usa con normalidad | **Deshabilitar** y **Anular** |
| Deshabilitado | Está en pausa. No se borra | **Activar** y **Anular** |
| Anulado | Quedó sin efecto, **de forma definitiva**. Solo se puede leer | Ninguna |

**Pasos:**

1. Haz clic en el icono de la acción en la fila, o en la cabecera de la ficha si es un usuario (su nombre es, por ejemplo, «Deshabilitar: Banco Uno»).
2. Se abre un diálogo con el título de la acción y una explicación:
   - Deshabilitar: «El registro deja de estar operativo, pero puede activarse de nuevo más adelante.»
   - Anular: «La anulación es definitiva: el registro queda de solo lectura y no puede editarse ni reactivarse.»
   - Activar: «El registro vuelve a estar operativo.»
3. Escribe el **Motivo**. Es obligatorio: si lo dejas vacío, el diálogo dice «El motivo es obligatorio.».
4. Haz clic en **Deshabilitar**, **Anular definitivamente** o **Activar**. Mientras se envía, dice «Enviando…».

Al terminar, el diálogo se cierra y se guarda el nuevo estado. Se actualiza el listado o la ficha; en un listado, la fila puede quedar fuera de los filtros actuales.

El sistema guarda quién hizo el cambio, cuándo y con qué motivo.

### Si algo sale mal al cambiar de estado

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «El motivo es obligatorio.» | Dejaste el motivo vacío | Escribe el motivo |
| «La anulación es terminal: el registro no cambia más.» | Ya estaba anulado | No se puede hacer nada más con ese registro |
| «El registro ya está deshabilitado.» / «El registro ya está activo.» | Alguien más ya hizo el cambio, o ya estaba en ese estado | Recarga el listado y revisa |

Cada pantalla puede ofrecer solo algunas de las tres acciones. Por ejemplo, las metas no se pueden anular. Mira la página de cada pantalla.

## Confirmaciones sin motivo

Algunas acciones no piden un motivo pero sí una confirmación, porque no se pueden deshacer (por ejemplo despachar o recibir un traslado). Verás un diálogo con la explicación de las consecuencias y dos botones: **Cancelar** y el que confirma (con el nombre de la acción). Mientras se envía dice «Enviando…».

## Qué ve cada rol

| Rol | Ve el botón de alta o edición | Observaciones |
|---|---|---|
| Super Administrador | En todas las pantallas que administra | |
| Administrador | En casi todas | Crear usuarios y gestionar catálogos es de los roles administrativos. Las tasas y topes que mueven dinero (intermediación, topes de descuento, texto de aceptación) solo los publica el Super Administrador. |
| Administrador de Punto | Según la pantalla | Por ejemplo, registra ingresos y traslados de su sucursal |
| Vendedor | Según la pantalla | Por ejemplo, registra ventas y pide modificaciones o anulaciones |
| Bodeguero | Según la pantalla | Opera Inventario en su ubicación |

Consulta **Qué ve cada rol** en la página de la tarea que vas a realizar y [Roles y permisos](roles-y-permisos.md) para conocer los permisos adicionales.

## Relación con otros módulos

**Necesitas antes:**
- Poder abrir la pantalla: [Menú y navegación](menu-y-navegacion.md).
- Para elegir cosas en una lista desplegable, que ya estén creadas (por ejemplo, una ciudad antes de crear una sucursal). Cada pantalla lo indica.
- Lecturas de apoyo, según la tarea que realices: [Listados: buscar, filtrar y pasar de página](listados-filtros-y-paginacion.md).

**Esto afecta a:**
- Todas las pantallas de alta y edición: [Administración](../administracion/ciudades.md), [Inventario](../inventario/ingresos.md) y [Ventas](../ventas/nueva-venta.md).
- Anular o modificar una venta ya confirmada no se hace con estos botones: pide aprobación. Mira [Solicitudes](../ventas/solicitudes.md).

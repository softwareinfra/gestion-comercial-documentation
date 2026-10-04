# Sucursales

Aquí registras los lugares donde trabaja el negocio: los puntos de venta, las bodegas o los sitios que hacen las dos cosas. Cada persona (salvo Super Administrador y Administrador), cada equipo y cada venta queda ligado a una sucursal, así que es uno de los primeros datos que hay que tener listos. Desde aquí también las deshabilitas o anulas cuando ya no se usan; nada se borra.

> **Quién puede hacerlo:** Super Administrador y Administrador.
> **Dónde está:** menú lateral → Administración → Sucursales.

Administrador de Punto, Vendedor y Bodeguero no tienen el módulo Administración en su menú. Si alguno de ellos escribe la dirección de la pantalla a mano, el sistema le responde «No tienes permiso para acceder a esta sección.»

## Antes de empezar

### Sucursal, punto de venta y bodega: ¿en qué se diferencian?

En el sistema hay **un solo tipo de registro**: la **Sucursal**. Lo que distingue a un punto de venta de una bodega es el campo **Tipo**, que tiene tres opciones exactas:

| Tipo | Qué es | Qué puede hacer |
|---|---|---|
| **Punto de venta** | Un lugar donde se vende. | Registrar ventas, llevar caja y hacer el cuadre de caja. |
| **Bodega** | Un lugar que solo guarda equipos. | **No** registra ventas, **no** maneja caja y **no** tiene cuadre de caja. Sí recibe ingresos y traslados. |
| **Punto de venta y bodega** | Un lugar que hace las dos cosas. | Lo mismo que un punto de venta: vende y maneja caja, además de guardar equipos. |

Lo que el sistema hace cuando el tipo es **Bodega**:

- **Ventas:** si intentas vender un equipo que está en una bodega, el sistema responde «Una bodega pura no registra ventas: traslada el equipo antes (6.2).» Primero hay que [trasladar el equipo](../inventario/traslados.md) a un punto de venta.
- **Caja:** el sistema rechaza un movimiento de caja suelto en una bodega con «Una bodega no maneja caja: no registra ingresos ni egresos (6.2).» y un cuadre de caja con «Una bodega no maneja caja: no tiene cuadre (6.2).» En los formularios de caja y de cuadre, las bodegas ni siquiera aparecen para elegir.
- **Ventas ya hechas:** si una sucursal pasa a ser bodega después de haber vendido, sus ventas anteriores conservan su caja (abonos y modificaciones siguen funcionando).

Las sucursales de tipo «Punto de venta» y «Punto de venta y bodega» se comportan igual en todo lo que encontró el manual; el nombre «y bodega» sirve para que quede claro que también guarda mercancía.

> Las personas que trabajan en una sucursal (Administrador de Punto, Vendedor y Bodeguero) tienen alcance **operativo** de esa sucursal; pueden consultar catálogos nacionales de apoyo según sus permisos. Para el Bodeguero, la pantalla también la llama «Sucursal», aunque el sistema la trata como su ubicación asignada. Mira [Usuarios](usuarios.md).

### Otras cosas que conviene saber

- **Ciudad:** cada sucursal pertenece a una ciudad. Primero [crea la ciudad](ciudades.md).
- **Responsable:** es opcional. Es una de las personas ya registradas en [Usuarios](usuarios.md).
- **Estado:** una sucursal está **Activa**, **Deshabilitada** (se puede volver a activar) o **Anulada** (definitivo). No existe el botón de borrar.

## Cómo consultar y buscar sucursales

1. Entra a Administración → Sucursales. Verás el título **Sucursales** y la frase «Puntos de venta y bodegas, con su ciudad y su responsable.»
2. La tabla «Listado de sucursales» tiene seis columnas: **Nombre**, **Código interno**, **Tipo**, **Ciudad**, **Estado** (Activo, Deshabilitado o Anulado) y **Acciones**.
3. La lista sale ordenada por nombre, con 25 sucursales por página. Incluye las deshabilitadas y las anuladas.

### Filtros

La tarjeta «Filtros de sucursales» tiene dos campos:

| Campo | Qué hace |
|---|---|
| **Buscar** | Escribe en «Buscar por nombre o código interno…». El botón de criterio al lado te deja elegir **Contiene** (por defecto), **Inicia por**, **Es igual a** o **Termina en**. |
| **Ciudad** | «Todas las ciudades» o una ciudad de la lista. La lista incluye también ciudades desactivadas, para que puedas encontrar las sedes que quedaron en ellas. |

Cómo funciona:

- La búsqueda mira el nombre y el código interno. No distingue mayúsculas, pero sí tildes.
- La página, la búsqueda y la ciudad elegida quedan en la dirección del navegador: puedes recargar o compartir el enlace y verás lo mismo. Al cambiar un filtro vuelves a la página 1.
- El pie de la tarjeta dice «Mostrando N sucursales» y cuántos filtros hay aplicados. Cuando hay alguno aparece el botón **Limpiar filtros**, que borra el buscador y la ciudad a la vez.
- Si ningún registro coincide verás «Ninguna sucursal coincide con el filtro.» Si todavía no hay ninguna: «Todavía no hay sucursales.»
- Mientras la lista de ciudades no cargue, el filtro «Ciudad» está bloqueado.

El funcionamiento general de listados y paginación está en [Listados: buscar, filtrar y pasar de página](../general/listados-filtros-y-paginacion.md).

## Cómo crear una sucursal

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Haz clic en **Nueva sucursal** (arriba a la derecha).
2. Se abre un diálogo al centro de la pantalla con el título «Nueva sucursal» y la frase «Punto de venta o bodega, con su ciudad y su responsable.» Si las ciudades o los usuarios todavía están cargando, ves «Cargando catálogos…» hasta que termine.
3. Llena **Nombre**, **Código interno**, **Dirección**.
4. En **Tipo** elige «Selecciona el tipo» y escoge una de las tres opciones.
5. En **Ciudad** elige «Selecciona una ciudad» y escoge una de la lista.
6. Si quieres, llena **Teléfono**, **URL de mapa**, **Responsable**, **Latitud**, **Longitud** y **Notas**.
7. Haz clic en **Guardar**. Mientras se envía el botón dice «Guardando…» y el diálogo no se puede cerrar.

Al terminar se cierra el diálogo y se actualiza el listado, conservando los filtros y la página. La sucursal se crea con estado **Activo**. Si no aparece, usa **Limpiar filtros** y búscala por nombre o código.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | El nombre de la sucursal, hasta 150 caracteres. No puede repetirse con el de otra sucursal. | Sí |
| Código interno | Mayúsculas, números y guiones, de 2 a 20 caracteres (por ejemplo `GEO-01`). No puede repetirse. El sistema **no** lo pasa a mayúsculas por ti. | Sí |
| Tipo | «Punto de venta», «Bodega» o «Punto de venta y bodega». Mira la tabla de arriba. | Sí |
| Ciudad | Una ciudad **activa** de la lista. | Sí |
| Dirección | La dirección, hasta 255 caracteres. | Sí |
| Teléfono | Celular de 10 dígitos que empiece por 3, por ejemplo 3101234567, **sin espacios ni guiones**. | No |
| URL de mapa | El enlace de Google Maps de la sede (una dirección web completa). | No |
| Responsable | «Sin responsable» o una persona activa de la lista (se muestran nombre y apellido). | No |
| Latitud | Número decimal, hasta 9 cifras en total y 6 decimales. Va **junto** con la longitud. | No |
| Longitud | Igual que la latitud. | No |
| Notas | Texto libre. | No |

Reglas que conviene recordar:

- **Latitud y longitud van juntas:** o llenas las dos o dejas las dos vacías. Si llenas solo una, el formulario avisa «Latitud y longitud van juntas: completa ambas o deja ambas vacías.»
- El **Teléfono** de una sucursal debe ser un celular colombiano; un número fijo o con espacios no pasa.

## Cómo editar una sucursal

1. En la fila de la sucursal, haz clic en el lápiz (**Editar**).
2. Se abre el diálogo «Editar sucursal» con los datos actuales.
3. Cambia lo que necesites y haz clic en **Guardar**.

Puedes editar sucursales **Activas** y **Deshabilitadas**. Una sucursal **Anulada** ya no muestra el lápiz: queda de solo lectura. Puedes cancelar con **Cancelar**, con la **X** o con la tecla Escape; hacer clic fuera del diálogo no lo cierra.

## Cómo deshabilitar, activar o anular una sucursal

En la columna **Acciones** hay iconos según el estado actual:

| Estado actual | Iconos que ves | Qué hace cada uno |
|---|---|---|
| Activo | **Deshabilitar**, **Anular** | Deshabilitar: la deja sin uso, pero la puedes volver a activar. Anular: es definitivo. |
| Deshabilitado | **Activar**, **Anular** | Activar: la vuelve a dejar operativa. |
| Anulado | Ninguno | Queda de solo lectura: no se edita ni se reactiva. |

Pasos:

1. Haz clic en el icono de la acción (al pasar el mouse dice su nombre: «Deshabilitar», «Anular» o «Activar»).
2. Se abre un diálogo titulado con la acción y el nombre de la sucursal, por ejemplo «Deshabilitar: Centro». Explica la consecuencia: para deshabilitar, «El registro deja de estar operativo, pero puede activarse de nuevo más adelante.»; para anular, «La anulación es definitiva: el registro queda de solo lectura y no puede editarse ni reactivarse.»
3. Escribe el **Motivo**. Es obligatorio: sin motivo verás «El motivo es obligatorio.»
4. Haz clic en **Deshabilitar**, **Anular definitivamente** o **Activar** (según el caso). Mientras se envía dice «Enviando…».

Al terminar verás el estado nuevo en la columna **Estado**. El motivo y quién lo hizo quedan registrados.

### Qué pasa al deshabilitar o anular (nada se borra)

- **Todo lo que ya existe se conserva.** Las personas, los equipos, los ingresos, las ventas, la caja y las metas ligadas a la sucursal siguen apuntando a ella: el sistema no tiene borrado de sucursales.
- **Deja de ofrecerse en los formularios nuevos.** Una sucursal que no está activa no aparece en las listas para elegir al crear un [ingreso](../inventario/ingresos.md), un [traslado](../inventario/traslados.md), un movimiento o un cuadre de [caja](../ventas/caja.md), o una persona en [Usuarios](usuarios.md). Sí sigue saliendo en los filtros, para que puedas consultar su historia. Esa restricción la aplican las pantallas: por detrás, el sistema no revisa el estado de la sucursal al guardar un ingreso o un traslado.
- **Metas:** al crear o editar una [meta](../metas/metas.md) sobre esa sucursal, el sistema responde «La sucursal está deshabilitada o anulada; la meta exige una sucursal activa (11.2).» Las metas que ya existían siguen calculándose.
- **Las personas asignadas siguen asignadas.** El sistema no les cambia la sucursal. Antes de deshabilitar una sede con personas o equipos, organiza su traslado con tu administrador; deshabilitar no reasigna a las personas.
- **Deshabilitar se deshace; anular no.** Si te equivocaste al deshabilitar, usa **Activar**. Si anulaste, no hay vuelta atrás.

## Qué ve cada rol

| Rol | Ve la pantalla Sucursales | Puede crear | Puede editar / deshabilitar / anular | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | |
| Administrador | Sí | Sí | Sí | |
| Administrador de Punto | No | No | No | No tiene Administración en su menú. El sistema sí le deja **consultar** las sucursales para elegir en sus formularios (por ejemplo, el destino de un traslado), pero solo con datos básicos: nombre, código, tipo, ciudad, dirección, mapa y estado; sin teléfono, responsable ni notas. |
| Vendedor | No | No | No | Igual: solo consulta básica de apoyo. |
| Bodeguero | No | No | No | Igual: solo consulta básica de apoyo. |

El permiso de consulta se llama «Consultar sedes y ciudades» y lo traen los cinco roles. «Crear y editar sedes y ciudades» (que incluye deshabilitar, anular y activar sedes) está **reservado** a los roles administrativos y no se puede otorgar como permiso extra (ver [Detalle de un usuario y sus permisos](usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra)).

## Relación con otros módulos

**Necesitas antes:**
- [Crear una ciudad](ciudades.md): la ciudad de la sucursal se elige de la lista de ciudades activas.
- [Usuarios](usuarios.md) (solo si quieres poner un **Responsable**): la persona debe existir y estar activa. Como las personas de sede necesitan sucursal, suele hacerse en este orden: ciudad → sucursal → usuarios → (opcional) volver a editar la sucursal para asignar responsable.

**Esto afecta a:**
- [Usuarios](usuarios.md): la sucursal asignada acota los datos operativos de Administradores de Punto, Vendedores y Bodegueros. Super Administradores y Administradores mantienen alcance global aunque tengan sucursal asignada. Los catálogos de apoyo (sedes, ciudades y proveedores, según permisos) son nacionales; consultarlos no abre Administración ni permite ver las operaciones de otra sede. Ver [Roles y permisos](../general/roles-y-permisos.md).
- [Equipos](../inventario/equipos.md), [Ingresos](../inventario/ingresos.md) y [Traslados](../inventario/traslados.md): cada equipo está en una sucursal; los formularios de ingresos y traslados ofrecen sucursales activas. Consulta [Qué pasa al deshabilitar o anular](#qué-pasa-al-deshabilitar-o-anular-nada-se-borra) para distinguir esa restricción de pantalla de las comprobaciones al guardar.
- [Registrar una venta](../ventas/nueva-venta.md) y [Ventas](../ventas/ventas.md): la venta pertenece a la sucursal donde está el equipo; en una bodega no se vende.
- [Caja](../ventas/caja.md) y [Cuadres de caja](../ventas/cuadres-de-caja.md): solo los puntos de venta (y «Punto de venta y bodega») llevan caja y cuadre.
- [Metas](../metas/metas.md): una meta puede tener como alcance una sucursal.
- Los tableros y el [Informe de financieras](../dashboard/informe-de-financieras.md) usan las sucursales como filtro.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Completa el tipo y la ciudad antes de guardar.» | Dejaste sin elegir el Tipo o la Ciudad. | Elige ambos y guarda de nuevo. |
| «Latitud y longitud van juntas: completa ambas o deja ambas vacías.» | Llenaste solo una de las dos coordenadas. | Llena la otra o vacía las dos. |
| «La latitud y la longitud van juntas: registra ambas o ninguna.» | Lo mismo, pero lo rechaza el sistema al guardar. | Igual que arriba. |
| «El código interno usa mayúsculas, números y guiones (2 a 20).» | El código tiene minúsculas, espacios, otros símbolos o una longitud fuera de 2 a 20. | Escríbelo en mayúsculas, sin espacios, por ejemplo `CENTRO-1`. |
| «El celular debe tener 10 dígitos y empezar por 3 (formato 310XXXXXXX).» | El teléfono no cumple el formato. | Escribe el celular de 10 dígitos que empieza por 3, sin espacios ni guiones. |
| Un mensaje de que ya existe un registro con ese valor en «Nombre» o «Código interno» | Otra sucursal ya usa ese nombre o ese código. | Elige otro nombre o código. |
| «Este campo es obligatorio.» / «Este campo no puede estar vacío.» | Falta el nombre, el código interno o la dirección. | Llénalo. Antes de enviar, el navegador también marca los campos vacíos con su propio aviso. |
| «Ingresa una URL válida.» | La URL de mapa no es una dirección web completa. | Copia el enlace completo de Google Maps (empieza por `https://`). |
| «El motivo es obligatorio.» | Intentaste deshabilitar, anular o activar sin escribir el motivo. | Escribe el motivo. |
| «El registro ya está deshabilitado.» / «El registro ya está activo.» | Otra persona cambió el estado antes que tú. | Cierra el diálogo y revisa el estado en la tabla. |
| «La anulación es terminal: el registro no cambia más.» | La sucursal ya estaba anulada. | No hay nada más que hacer. |
| «Una bodega pura no registra ventas: traslada el equipo antes (6.2).» | Se intentó vender un equipo que está en una sucursal de tipo Bodega. | [Traslada el equipo](../inventario/traslados.md) a un punto de venta. |
| Un aviso rojo con el botón **Reintentar** | No se pudo cargar la lista, las ciudades o los usuarios. | Haz clic en **Reintentar**. Si las ciudades o los usuarios no cargan, el formulario no se puede llenar. |
| «No tienes permiso para ver esta información.» | El sistema no te deja hacer esa acción (por ejemplo, si tu rol cambió mientras tenías la pantalla abierta). | Pídele el cambio a un Super Administrador. |

## Preguntas frecuentes

**¿Cuál es la diferencia entre «Sucursal», «Punto de venta» y «Bodega»?** Sucursal es el nombre del registro; «Punto de venta», «Bodega» y «Punto de venta y bodega» son los tres valores del campo **Tipo**. Ver la tabla al principio de esta página.

**¿Puedo cambiar el Tipo de una sucursal que ya tiene ventas?** El formulario de edición lo permite. Las ventas anteriores conservan su caja; lo que cambia es lo que se puede hacer de ahí en adelante (por ejemplo, una bodega ya no registra ventas nuevas).

**¿Puedo asignar a un Vendedor a una sucursal de tipo Bodega?** El sistema lo permite al crear la persona; no puedes registrar una [venta](../ventas/nueva-venta.md) de un equipo ubicado en una bodega pura. Primero [traslada el equipo](../inventario/traslados.md) a un punto de venta.

**¿Por qué no puedo elegir una ciudad en el formulario?** Solo aparecen las ciudades activas. Activa la ciudad en [Ciudades](ciudades.md).

**¿Por qué mi Responsable no aparece en la lista?** Solo salen las personas con estado Activo (de cualquier rol). Revisa su estado en [Usuarios](usuarios.md).

# Referencias

Una referencia es el **modelo concreto** de un equipo: «Galaxy A56», «iPhone 15», etc. Cada una pertenece a una marca y a un tipo de producto, y tiene un sistema operativo. Es lo que eliges, equipo por equipo, cuando registras un ingreso de mercancía. Aquí la creas cuando llega un modelo que todavía no está en la lista.

> **Quién puede hacerlo:** Super Administrador y Administrador.
> **Dónde está:** menú lateral → Administración → Referencias.

Esta pantalla funciona como [Marcas](marcas.md) (buscar, crear, editar, activar y desactivar). Aquí verás lo propio de las referencias: los tres datos que las acompañan (marca, tipo de producto y sistema operativo) y las reglas que los relacionan.

## Antes de empezar

- **Necesitas tener creadas** la [marca](marcas.md) y el [tipo de producto](tipos-de-producto.md) de la referencia, y que estén **activas**. Los desplegables solo ofrecen las activas.
- **El nombre de la referencia no es único en todo el sistema**: es único **dentro de una marca y un tipo**. Puedes tener «A56» en Samsung y otro «A56» en otra marca. Dentro de la misma marca y tipo, no se puede repetir (sin importar mayúsculas).
- **Sistema operativo:** cada referencia queda con uno (iOS, Android, Otro o, si no se pudo saber, «Sin clasificar»). Sirve para los informes por sistema operativo. Ver [Sistemas operativos](sistemas-operativos.md).
- **No se borra nada.** Una referencia que ya no vendes se desactiva con el interruptor **Activa**.
- No hay referencias de fábrica: todas las crea alguien.

## Cómo consultar y buscar

1. Entra a Administración → Referencias. Verás el título **Referencias** y la frase «Los modelos concretos de cada marca, agrupados por tipo de producto.»
2. La tabla tiene seis columnas: **Nombre**, **Marca**, **Tipo de producto**, **Sistema operativo**, **Activa** (interruptor) y **Acciones** (el lápiz). Mientras los catálogos de apoyo cargan, las columnas Marca, Tipo de producto y Sistema operativo muestran «…».
3. La barra «Buscar por nombre…» busca **solo en el nombre de la referencia**, no en la marca ni en el tipo. El tipo de coincidencia y la paginación funcionan como en [Marcas](marcas.md#cómo-consultar-y-buscar).
4. Sin resultados: «Ninguna referencia coincide con el filtro.» Sin referencias: «Todavía no hay referencias.»

Esta pantalla **no tiene columna «Protegida»**: ninguna referencia es de fábrica.

## Cómo crear una referencia

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Haz clic en **Nueva referencia**.
2. Se abre el panel «Nueva referencia» con la frase «Modelo concreto dentro de una marca y un tipo de producto.» Si los catálogos todavía están cargando verás «Cargando catálogos…» un instante.
3. Escribe el **Nombre**.
4. En **Marca** elige «Selecciona una marca» y escoge la marca.
5. En **Tipo de producto** elige «Selecciona un tipo» y escoge el tipo.
6. En **Sistema operativo** deja «Según el tipo de producto» (la opción por defecto) o elige uno concreto. Debajo te explica qué pasa: «Si lo dejas según el tipo, iPhone queda en iOS, celular Android en Android y cualquier otro tipo sin clasificar.»
7. Haz clic en **Guardar**.

Al terminar se cierra el panel y se actualiza el listado, conservando la búsqueda y la página. La opción se crea activa. Si no aparece, limpia la búsqueda y localízala por su nombre.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | El modelo, hasta 100 caracteres. Único dentro de la misma marca y tipo. | Sí |
| Marca | Una marca **activa** de [Marcas](marcas.md). | Sí |
| Tipo de producto | Un tipo **activo** de [Tipos de producto](tipos-de-producto.md). | Sí |
| Sistema operativo | «Según el tipo de producto», o uno de la lista de [Sistemas operativos](sistemas-operativos.md). La lista solo trae los activos y **nunca** trae «Sin clasificar». | No (queda «Según el tipo de producto») |

### Cómo decide el sistema el sistema operativo

| Si dejas «Según el tipo de producto» y el tipo es… | La referencia queda en… |
|---|---|
| iPhone | iOS |
| Celular Android | Android |
| Cualquier otro (tablet, computador, smartwatch, accesorio o uno que hayas creado) | Sin clasificar |

- Si quieres que una tablet, por ejemplo, quede como Android o iOS, **elígelo tú** en el desplegable.
- Si eliges un tipo iPhone o Celular Android, el sistema operativo **tiene que ser** el que le corresponde (iOS para iPhone, Android para Celular Android). Con otro, el sistema no deja guardar.
- «Sin clasificar» es el valor que el sistema pone solo cuando no puede saber; **no se puede elegir a mano** al crear.

## Cómo editar una referencia

1. Haz clic en el lápiz de la fila («Editar: Galaxy A56», por ejemplo).
2. Se abre el panel «Editar referencia» con los datos actuales. Puedes cambiar el nombre, la marca, el tipo y el sistema operativo.
3. Haz clic en **Guardar**.

Lo que conviene saber al editar:

- **Si cambias el tipo de producto**, el sistema operativo vuelve solo a «Según el tipo de producto». Si quieres otro, vuelve a elegirlo.
- Al editar, la ayuda dice: «Si lo dejas según el tipo, iPhone y celular Android se rederivan; con cualquier otro tipo se conserva el sistema actual.» Es decir: en una referencia cuyo tipo no es iPhone ni Celular Android, «Según el tipo de producto» **no la cambia**.
- Si la referencia ya está en «Sin clasificar» (porque así quedó), ese valor aparece en la lista para que puedas dejarlo; no lo puedes elegir en otra.
- Si el sistema operativo actual de la referencia está desactivado, también aparece en la lista para que no se cambie sin querer.
- **Cambiar la marca, el tipo o el sistema operativo de una referencia cambia los informes:** los tableros agrupan las ventas por la marca, el tipo y el sistema operativo **actuales** de la referencia, también las ventas anteriores. Ver [Tablero de ventas](../dashboard/tablero-de-ventas.md).
- Si la marca o el tipo de la referencia fueron desactivados, el desplegable correspondiente no los ofrece (solo trae las activas). Si el valor anterior no está entre las opciones, el campo muestra «Selecciona una marca» o «Selecciona un tipo», según corresponda. Revisa la marca y el tipo antes de guardar.

## Cómo desactivar o volver a activar una referencia

1. Haz clic en el interruptor de la columna **Activa**. Se guarda al instante.

Una referencia desactivada sigue en la tabla, pero **no se ofrece** al registrar un ingreso (solo aparecen las activas). Los equipos ya registrados con ella no cambian.

## Si el sistema operativo no carga

Si la lista de sistemas operativos falla, verás dentro del panel un aviso con el botón **Reintentar**, y el campo **Sistema operativo** queda bloqueado con el texto «Sistema operativo no disponible». Aun así puedes guardar la referencia: el sistema decide el sistema operativo por ti. Haz clic en **Reintentar** para recuperar el campo sin perder lo que ya escribiste.

## Qué ve cada rol

| Rol | Ve la pantalla | Puede crear | Puede editar y activar/desactivar | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | |
| Administrador | Sí | Sí | Sí | |
| Administrador de Punto | No | No | No | «No tienes permiso para acceder a esta sección.» si escribe la dirección. Elige referencias al registrar ingresos |
| Vendedor | No | No | No | Igual. Consulta las referencias al registrar una venta |
| Bodeguero | No | No | No | Igual. Elige referencias al registrar ingresos |

Los cinco roles pueden consultar el catálogo (lectura de apoyo). Ver [Marcas](marcas.md#qué-ve-cada-rol).

## Relación con otros módulos

**Necesitas antes:**
- [Marcas](marcas.md): la marca de la referencia, activa.
- [Tipos de producto](tipos-de-producto.md): el tipo, activo.
- [Sistemas operativos](sistemas-operativos.md): solo si quieres elegir uno a mano.

**Esto afecta a:**
- [Registrar un ingreso](../inventario/ingresos.md): cada equipo del ingreso se registra con una referencia activa. Sin la referencia creada, no puedes ingresar ese modelo.
- [Equipos](../inventario/equipos.md): la marca, el tipo y el sistema operativo de un equipo son los de su referencia.
- [Registrar una venta](../ventas/nueva-venta.md) y [Equipos en garantía](../garantias/equipos-en-garantia.md): muestran el modelo del equipo por su referencia.
- [Tablero de ventas](../dashboard/tablero-de-ventas.md) y [Tablero de inventario](../dashboard/tablero-de-inventario.md): filtran y agrupan por referencia, marca, tipo y sistema operativo.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Completa la marca y el tipo de producto antes de guardar.» | Dejaste la marca o el tipo sin elegir. | Elígelos y guarda de nuevo. |
| «Ya existe esa referencia para esa marca y tipo de producto.» | Ya hay una referencia con ese nombre en la misma marca y tipo. | Busca la existente (puede estar desactivada y basta con activarla). |
| «El tipo de producto «iPhone» solo admite el sistema operativo con código «ios».» (o «android» para Celular Android) | Elegiste un sistema operativo que no corresponde al tipo. | Deja «Según el tipo de producto» o elige el correcto. |
| ««Sin clasificar» no es elegible: es el bucket de la migración.» | Intentaste dejar «Sin clasificar» a propósito; ese valor solo lo pone el sistema. (La palabra «bucket» es el nombre interno de ese valor «de reserva».) | Elige otro sistema operativo o «Según el tipo de producto». |
| «No existe un registro con el identificador «…»» bajo un campo | La marca, el tipo o el sistema operativo elegidos ya no existen. | Cierra el panel, recarga la pantalla y vuelve a intentarlo. |
| Un aviso rojo con el botón «Reintentar» dentro del panel | No cargaron las marcas o los tipos (o los sistemas operativos). | Haz clic en **Reintentar**. Sin marcas y tipos no se puede llenar el formulario. |
| «Asegúrate de que este campo no tenga más de 100 caracteres.» | El nombre es demasiado largo. | Acórtalo. |

## Preguntas frecuentes

**No veo la marca que necesito en el desplegable.** Puede estar desactivada, o no existir todavía. Revísala en [Marcas](marcas.md).

**¿Por qué la tablet que creé quedó en «Sin clasificar»?** Porque el tipo Tablet no tiene un sistema operativo asignado por el sistema. Edita la referencia y elige el sistema operativo a mano.

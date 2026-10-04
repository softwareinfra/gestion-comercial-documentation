# Proveedores

Aquí registras a quienes te abastecen de equipos (personas o empresas), con su documento y su contacto. Cada vez que entra mercancía al inventario se elige un proveedor, así que conviene tenerlo creado **antes** de registrar el [ingreso](../inventario/ingresos.md). Los proveedores no se borran: se deshabilitan o se anulan.

> **Quién puede hacerlo:** Super Administrador y Administrador.
> **Dónde está:** menú lateral → Administración → Proveedores.

Administrador de Punto, Vendedor y Bodeguero no tienen el módulo Administración en su menú. Si alguno de ellos escribe la dirección de la pantalla a mano, el sistema le responde «No tienes permiso para acceder a esta sección.» Dos de esos roles sí **eligen** proveedores al registrar ingresos (ver [Qué ve cada rol](#qué-ve-cada-rol)).

## Antes de empezar

- **Tipo de persona y tipo de documento:** son dos datos distintos. El tipo de persona es «Persona natural» o «Persona jurídica»; el tipo de documento es «CC» o «NIT». El sistema no los obliga a coincidir (por ejemplo, no te impide poner «Persona natural» con «NIT»).
- **Un proveedor se identifica por su tipo y su número de documento juntos.** No puede haber dos proveedores con el mismo «CC 1234567» ni con el mismo «NIT 900123456». Un «CC 900123456» y un «NIT 900123456» sí pueden existir a la vez.
- **Estado:** un proveedor está **Activo**, **Deshabilitado** (se puede volver a activar) o **Anulado** (definitivo). No existe el botón de borrar.
- **Es un dato de apoyo:** un proveedor por sí solo no hace nada; se usa al registrar ingresos y aparece en la ficha de los equipos que te vendió.

## Cómo consultar y buscar proveedores

1. Entra a Administración → Proveedores. Verás el título **Proveedores** y la frase «Quiénes abastecen el inventario, con su documento y su contacto.»
2. La tabla «Listado de proveedores» tiene cinco columnas: **Razón social**, **Documento** (se muestra tipo y número, por ejemplo «NIT 900123456»), **Contacto**, **Estado** (Activo, Deshabilitado o Anulado) y **Acciones**.
3. La lista sale ordenada por razón social, con 25 proveedores por página. Incluye los deshabilitados y los anulados.
4. Para buscar, usa la barra «Buscar por razón social o documento…». A la izquierda puedes elegir el criterio: **Contiene** (por defecto), **Inicia por**, **Es igual a** o **Termina en**. Esta pantalla no tiene tarjeta de filtros.

Cómo funciona la búsqueda:

- Busca en la razón social y en el número de documento; coincide si coincide en cualquiera de los dos. No busca por el tipo de documento ni por el contacto.
- No distingue mayúsculas, pero **sí distingue tildes**.
- El texto se compara entero, sin partirlo por espacios: «Distribuidora Norte» encuentra solo lo que contenga esas dos palabras seguidas.
- La página y la búsqueda quedan en la dirección del navegador, así que puedes recargar o compartir el enlace. El funcionamiento general está en [Listados: buscar, filtrar y pasar de página](../general/listados-filtros-y-paginacion.md).
- Si ningún proveedor coincide verás «Ningún proveedor coincide con el filtro.» Si todavía no hay ninguno: «Todavía no hay proveedores.»

## Cómo crear un proveedor

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Haz clic en **Nuevo proveedor** (arriba a la derecha).
2. Se abre un diálogo al centro de la pantalla con el título «Nuevo proveedor» y la frase «Quién abastece el inventario, con su documento y su contacto.»
3. Escribe la **Razón social**.
4. En **Tipo de persona** elige «Selecciona el tipo de persona» y escoge «Persona natural» o «Persona jurídica».
5. En **Tipo de documento** elige «Selecciona el tipo de documento» y escoge «CC» o «NIT».
6. Escribe el **Número de documento**.
7. Si quieres, llena el **Nombre de contacto** y el **Teléfono**.
8. Haz clic en **Guardar**. Mientras se envía el botón dice «Guardando…» y el diálogo no se puede cerrar.

Al terminar se cierra el diálogo y se actualiza el listado, conservando la búsqueda y la página. El proveedor se crea con estado **Activo**. Si no aparece, limpia la búsqueda y búscalo por razón social o documento.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Razón social | El nombre de la empresa o de la persona, hasta 150 caracteres. | Sí |
| Tipo de persona | «Persona natural» o «Persona jurídica». | Sí |
| Tipo de documento | «CC» o «NIT». | Sí |
| Número de documento | El número, hasta 20 caracteres. El sistema **no revisa su formato**: lo guarda tal como lo escribes. | Sí |
| Nombre de contacto | La persona con quien tratas, hasta 150 caracteres. | No |
| Teléfono | Celular de 10 dígitos que empiece por 3, por ejemplo 3101234567, **sin espacios ni guiones**. | No |

Cuidados al escribir:

- Como el número no se revisa, **escríbelo siempre igual**. «900123456» y «900123456-7» cuentan como números distintos y el sistema no te avisaría de que es la misma empresa.
- El teléfono solo acepta celulares. Un número fijo, con espacios o con indicativo no pasa.

## Cómo editar un proveedor

1. En la fila del proveedor, haz clic en el lápiz (**Editar**).
2. Se abre el diálogo «Editar proveedor» con los datos actuales.
3. Cambia lo que necesites y haz clic en **Guardar**.

Puedes editar proveedores **Activos** y **Deshabilitados**. Uno **Anulado** ya no muestra el lápiz: queda de solo lectura. Puedes cancelar con **Cancelar**, con la **X** o con la tecla Escape; hacer clic fuera del diálogo no lo cierra.

## Cómo deshabilitar, activar o anular un proveedor

En la columna **Acciones** hay iconos según el estado actual:

| Estado actual | Iconos que ves | Qué hace cada uno |
|---|---|---|
| Activo | **Deshabilitar**, **Anular** | Deshabilitar: lo deja sin uso, pero lo puedes volver a activar. Anular: es definitivo. |
| Deshabilitado | **Activar**, **Anular** | Activar: lo vuelve a dejar operativo. |
| Anulado | Ninguno | Queda de solo lectura: no se edita ni se reactiva. |

Pasos:

1. Haz clic en el icono de la acción (al pasar el mouse dice su nombre: «Deshabilitar», «Anular» o «Activar»).
2. Se abre un diálogo titulado con la acción y la razón social, por ejemplo «Deshabilitar: Distribuidora Norte». Explica la consecuencia: para deshabilitar, «El registro deja de estar operativo, pero puede activarse de nuevo más adelante.»; para anular, «La anulación es definitiva: el registro queda de solo lectura y no puede editarse ni reactivarse.»
3. Escribe el **Motivo**. Es obligatorio: sin motivo verás «El motivo es obligatorio.»
4. Haz clic en **Deshabilitar**, **Anular definitivamente** o **Activar** (según el caso). Mientras se envía dice «Enviando…».

Al terminar verás el estado nuevo en la columna **Estado**. El motivo y quién lo hizo quedan registrados.

### Qué pasa al deshabilitar o anular (nada se borra)

- **Los ingresos y los equipos que ya compraste a ese proveedor se conservan** y siguen mostrando su nombre: el sistema no permite borrar proveedores y el listado de proveedores incluye también los deshabilitados y anulados justamente para que los ingresos antiguos puedan mostrar el nombre.
- **Deja de ofrecerse en los ingresos nuevos:** en el formulario de [Ingresos](../inventario/ingresos.md) solo aparecen los proveedores **Activos**. Esa restricción la aplica la pantalla: el sistema, por detrás, no revisa el estado del proveedor al guardar un ingreso.
- **Deshabilitar se deshace; anular no.** Si te equivocaste al deshabilitar, usa **Activar**. Si anulaste, no puedes reactivarlo ni crear otro con el mismo tipo y número de documento. La anulación no libera el tipo y número de documento. Si necesitas volver a trabajar con ese proveedor, consulta a tu administrador antes de anularlo.

## Qué ve cada rol

| Rol | Ve la pantalla Proveedores | Puede crear | Puede editar / deshabilitar / anular | Observaciones |
|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | Ve todos los datos del proveedor. |
| Administrador | Sí | Sí | Sí | Ve todos los datos del proveedor. |
| Administrador de Punto | No | No | No | No tiene Administración en su menú, pero puede **consultar** los proveedores para elegirlos en los ingresos. Solo le llegan el nombre (razón social) y el estado: **no** ve documento, contacto ni teléfono. |
| Vendedor | No | No | No | No consulta proveedores y no ve su nombre en el inventario. |
| Bodeguero | No | No | No | Igual que el Administrador de Punto: consulta el nombre y el estado para registrar ingresos. |

- Los permisos de consultar y de gestionar se llaman «Consultar proveedores» y «Crear y editar proveedores». El segundo (que incluye deshabilitar, anular y activar) está **reservado** a los roles administrativos y no se otorga como extra.
- «Consultar proveedores» sí se puede otorgar como **permiso extra** (por ejemplo a un Vendedor). Además de abrir esta consulta, hace que esa persona vea el **nombre del proveedor** en el inventario, los ingresos y las exportaciones. Ver [Detalle de un usuario y sus permisos](usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra).
- El documento y el contacto de un proveedor solo los ven el Super Administrador y el Administrador. Por eso, quien no los ve tampoco puede buscar por documento.

## Relación con otros módulos

**Necesitas antes:**
- Nada. No depende de ciudades ni de sucursales.
- Lecturas de apoyo, según la tarea que realices: [Lista completa de permisos extra](usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra).

**Esto afecta a:**
- [Ingresos](../inventario/ingresos.md): cada ingreso de mercancía empieza por elegir un proveedor activo.
- [Equipos](../inventario/equipos.md) y [la ficha del equipo](../inventario/equipo-detalle.md): cada equipo guarda el proveedor al que se le compró. Quien tiene permiso para verlo lo encuentra en la ficha, en las exportaciones y al imprimir.
- [Exportar e imprimir](../general/exportar-e-imprimir.md): la columna «Proveedor» solo sale para los roles que pueden ver el nombre del proveedor.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Completa el tipo de persona y el tipo de documento antes de guardar.» | Dejaste sin elegir el Tipo de persona o el Tipo de documento. | Elige ambos y guarda de nuevo. |
| Un mensaje de que el tipo y el número de documento ya existen | Ya hay otro proveedor con ese mismo tipo y número. | Búscalo en la lista; si es el mismo, úsalo (o actívalo si está deshabilitado). |
| «El celular debe tener 10 dígitos y empezar por 3 (formato 310XXXXXXX).» | El teléfono no cumple el formato. | Escribe el celular de 10 dígitos que empieza por 3, sin espacios ni guiones. |
| «Este campo es obligatorio.» / «Este campo no puede estar vacío.» | Falta la razón social o el número de documento. | Llénalo. Antes de enviar, el navegador también marca los campos vacíos con su propio aviso. |
| «Asegúrate de que este campo no tenga más de 150 caracteres.» (o 20, en el número de documento) | El texto es demasiado largo. | Acórtalo. |
| «El motivo es obligatorio.» | Intentaste deshabilitar, anular o activar sin escribir el motivo. | Escribe el motivo. |
| «El registro ya está deshabilitado.» / «El registro ya está activo.» | Otra persona cambió el estado antes que tú. | Cierra el diálogo y revisa el estado en la tabla. |
| «La anulación es terminal: el registro no cambia más.» | El proveedor ya estaba anulado. | No hay nada más que hacer. |
| Un aviso rojo con el botón **Reintentar** | No se pudo cargar la lista. | Haz clic en **Reintentar**. |
| «No tienes permiso para ver esta información.» | El sistema no te deja hacer esa acción (por ejemplo, si tu rol cambió mientras tenías la pantalla abierta). | Pídele el cambio a un Super Administrador. |

## Preguntas frecuentes

**¿Por qué el Administrador de Punto no ve el NIT del proveedor?** Porque el sistema solo le entrega el nombre y el estado, para que pueda elegirlo en un ingreso. El documento y el contacto son solo de los roles administrativos.

**¿Puedo corregir el tipo de documento de un proveedor que ya tiene ingresos?** Sí, con **Editar**: los ingresos siguen apuntando al mismo proveedor. Solo cuida que la nueva pareja tipo + número no esté ocupada por otro.

**¿El proveedor tiene ciudad?** No. El formulario no tiene ese campo, aunque la pantalla [Ciudades](ciudades.md) diga que sirve «para ubicar sucursales y proveedores».

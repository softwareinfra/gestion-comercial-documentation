# Entidades financieras

Aquí registras a los bancos, cooperativas y demás empresas que financian las ventas a crédito (por ejemplo ADDI), y configuras tres cosas de cada una: sus datos básicos, sus **fechas de corte y de pago** y su **intermediación** (lo que la financiera descuenta en cada venta financiada). Las entidades no se borran: se deshabilitan o se anulan. Esta página cubre el listado y también la pantalla de **detalle** de cada entidad.

> **Quién puede hacerlo:** Super Administrador y Administrador. La **tasa de intermediación** la fija **solo el Super Administrador**.
> **Dónde está:** menú lateral → Administración → Entidades financieras. El detalle se abre haciendo clic en la razón social de una fila.

Administrador de Punto, Vendedor y Bodeguero no tienen el módulo Administración en su menú. Si alguno de ellos escribe la dirección de la pantalla a mano, el sistema le responde «No tienes permiso para acceder a esta sección.» Administrador de Punto y Vendedor sí **eligen** entidades financieras al registrar una venta (ver [Qué ve cada rol](#qué-ve-cada-rol)).

## Antes de empezar

- **Entidad financiera (o financiera):** la empresa que financia o intermedia en una venta. Se identifica por su **NIT**, que no puede repetirse.
- **Corte y pago:** la financiera agrupa las ventas en **períodos** que se cierran en una fecha (el **corte**) y te paga algún tiempo después (el **pago**). Cada entidad tiene una regla que dice cómo se calculan esas dos fechas. Se explica en [Fechas de corte y de pago](#fechas-de-corte-y-de-pago).
- **Intermediación:** el valor que la financiera cobra (o descuenta) cuando financia una venta. Se define como un **porcentaje del valor de venta** y, si aplica, un **IVA** que se cobra *sobre* esa intermediación. Se explica en [Intermediación](#intermediación).
- **Historial que no se edita:** la regla de corte/pago y la tasa de intermediación se guardan como **versiones** con una fecha desde la que rigen. Una versión ya guardada **no se modifica ni se borra**: para corregir algo se registra una versión nueva. La que rige hoy lleva la etiqueta **Vigente**.
- **Estado:** una entidad está **Activa**, **Deshabilitada** (se puede volver a activar) o **Anulada** (definitivo).

## Cómo consultar y buscar entidades

1. Entra a Administración → Entidades financieras. Verás el título **Entidades financieras** y la frase «Bancos y cooperativas con convenio, cada uno con su regla de corte y pago.»
2. La tabla «Listado de entidades financieras» tiene cuatro columnas: **Razón social** (es un enlace al detalle), **NIT**, **Estado** (Activo, Deshabilitado o Anulado) y **Acciones**.
3. La lista sale ordenada por razón social, con 25 entidades por página. Incluye las deshabilitadas y las anuladas.
4. Para buscar, usa la barra «Buscar por razón social o NIT…». A la izquierda puedes elegir el criterio: **Contiene** (por defecto), **Inicia por**, **Es igual a** o **Termina en**. Esta pantalla no tiene tarjeta de filtros.

Cómo funciona la búsqueda:

- Busca en la razón social y en el NIT; coincide si coincide en cualquiera de los dos.
- No distingue mayúsculas, pero **sí distingue tildes**: «Bogota» no encuentra «Bogotá».
- El texto se compara entero, sin partirlo por espacios. El funcionamiento general está en [Listados: buscar, filtrar y pasar de página](../general/listados-filtros-y-paginacion.md).
- Si ninguna entidad coincide verás «Ninguna entidad financiera coincide con el filtro.» Si todavía no hay ninguna: «Todavía no hay entidades financieras.»

## Cómo crear una entidad financiera

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. Haz clic en **Nueva entidad financiera** (arriba a la derecha).
2. Se abre un panel lateral con el título «Nueva entidad financiera» y la frase «Banco o cooperativa con convenio, con su regla de corte y pago.»
3. Escribe la **Razón social**.
4. Escribe el **NIT**.
5. Haz clic en **Guardar**. Mientras se envía, el botón dice «Guardando…» y el panel no se puede cerrar.

Al terminar se cierra el panel y se actualiza el listado, conservando la búsqueda y la página. La entidad se crea con estado **Activo**. Si no aparece, limpia la búsqueda y búscala por razón social o NIT. **Todavía no tiene regla de corte y pago ni tasa de intermediación:** se cargan desde su detalle (más abajo).

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Razón social | El nombre de la entidad, hasta 150 caracteres. | Sí |
| NIT | El NIT, hasta 20 caracteres. No puede repetirse. El sistema **no revisa su formato**: lo guarda tal como lo escribes. | Sí |

## Cómo editar una entidad

1. En la fila de la entidad, haz clic en el lápiz (**Editar**).
2. Se abre el panel «Editar entidad financiera» con los datos actuales.
3. Cambia la **Razón social** o el **NIT** y haz clic en **Guardar**.

Con esto solo cambian esos dos datos: la regla de corte y pago y la intermediación **no** se editan aquí (ver el detalle). Puedes editar entidades **Activas** y **Deshabilitadas**; una **Anulada** ya no muestra el lápiz. Puedes cancelar con **Cancelar**, con la **X** o con la tecla Escape; hacer clic fuera del panel no lo cierra.

## Cómo deshabilitar, activar o anular una entidad

En la columna **Acciones** hay iconos según el estado actual:

| Estado actual | Iconos que ves | Qué hace cada uno |
|---|---|---|
| Activo | **Deshabilitar**, **Anular** | Deshabilitar: la deja sin uso, pero la puedes volver a activar. Anular: es definitivo. |
| Deshabilitado | **Activar**, **Anular** | Activar: la vuelve a dejar operativa. |
| Anulado | Ninguno | Queda de solo lectura: no se edita ni se reactiva. |

Pasos:

1. Haz clic en el icono de la acción (al pasar el mouse dice su nombre: «Deshabilitar», «Anular» o «Activar»).
2. Se abre un diálogo titulado con la acción y la razón social, por ejemplo «Deshabilitar: ADDI». Explica la consecuencia: para deshabilitar, «El registro deja de estar operativo, pero puede activarse de nuevo más adelante.»; para anular, «La anulación es definitiva: el registro queda de solo lectura y no puede editarse ni reactivarse.»
3. Escribe el **Motivo**. Es obligatorio: sin motivo verás «El motivo es obligatorio.»
4. Haz clic en **Deshabilitar**, **Anular definitivamente** o **Activar** (según el caso). Mientras se envía dice «Enviando…».

Al terminar verás el estado nuevo en la columna **Estado**. El motivo y quién lo hizo quedan registrados.

### Qué pasa al deshabilitar o anular (nada se borra)

- **No se puede vender con ella.** Una entidad que no está activa no aparece para elegir en una venta nueva; si alguien lograra enviarla, el sistema responde «La entidad financiera «nombre» no está activa (12.2).» En [Metas](../metas/metas.md) pasa algo parecido: una meta nueva o editada por entidad exige una entidad activa («La entidad financiera está deshabilitada o anulada; la meta exige una entidad activa (11.2).»), y las metas que ya existían siguen calculándose.
- **Las ventas ya hechas se conservan.** La venta guarda la entidad y la tasa con la que se hizo (ver [Intermediación](#intermediación)); deshabilitar o anular no las toca. Al modificar una venta que ya tenía esa entidad, la entidad sigue mostrándose marcada como inactiva.
- **El historial sigue consultable.** En el detalle se siguen viendo la regla de corte/pago y la tasa, incluso con la entidad anulada.
- **Anulada = no recibe versiones nuevas.** En una entidad anulada el detalle ya no muestra los botones para registrar una versión nueva de regla ni de tasa; el sistema además lo rechazaría. Una entidad **deshabilitada** sí puede recibir versiones nuevas.
- **Deshabilitar se deshace; anular no.** Si te equivocaste al deshabilitar, usa **Activar**.

## El detalle de una entidad

Se abre al hacer clic en la razón social de una fila. La dirección es `/administracion/entidades-financieras/` seguida del número de la entidad. Si entras a una dirección con un número inválido verás «No se encontró la entidad financiera.»; si la entidad no existe, «No se encontró el registro.»

De arriba hacia abajo verás:

1. **«Volver a Entidades financieras»**, un enlace que te regresa al listado.
2. El título con la **razón social** de la entidad y la frase «Ficha de la entidad, las versiones de su regla de corte y pago y su tasa de intermediación.»
3. A la derecha del título, los botones **Nueva tasa de intermediación** (solo para el Super Administrador) y **Nueva versión de regla**. Con la entidad anulada no aparece ninguno.
4. La **ficha** (solo lectura): **NIT**, **Estado**, **Creada el**, **Actualizada el** y, si aplica, **Deshabilitada el** o **Anulada el**.
5. La tabla **«Historial de reglas de corte y pago»**.
6. La tabla **«Historial de intermediación»**.

Desde el detalle no se edita la razón social ni el NIT: eso se hace con el lápiz del listado.

### Fechas de corte y de pago

**Qué es cada cosa.** La regla le dice al sistema, para esa financiera, cuándo se **cierra el período de ventas** (el corte) y cuándo se espera el **pago** de ese período. Las dos se configuran juntas en cada versión. El sistema usa la regla para calcular las fechas que muestra el [Informe de financieras](../dashboard/informe-de-financieras.md): la **fecha de corte** del período calculado tomando hoy como referencia y la **fecha estimada de pago**, que sale de aplicar la regla de pago a esa fecha de corte. La vigencia de la versión es independiente de las fechas iniciales de corte y pago: si la referencia es anterior a la fecha inicial de una recurrencia, se usa su primer período, aunque sea futuro. El valor esperado corresponde a ese período de corte completo. Ese informe lo ven solo los roles administrativos. Si la entidad no tiene ninguna regla que ya esté rigiendo, el informe no puede calcular ni esas fechas ni el valor esperado para esa entidad.

Hay tres formas de definir el corte y tres de definir el pago (son las mismas, se elige cada una por separado):

| Tipo de recurrencia | Qué pide | Cómo se arman los períodos |
|---|---|---|
| **Semanal** | Un **día de la semana** (lunes … domingo). | El período son los 7 días que terminan en ese día. Ejemplo: «Semanal — lunes». |
| **Mensual por posición** | Un **día de la semana** y una **semana del mes** (1.ª a 5.ª). | El período cierra en esa ocurrencia del día dentro de cada mes. Ejemplo: «Mensual — 2.ª semana, miércoles» es el segundo miércoles de cada mes. |
| **Fecha inicial y período** | Una **fecha inicial** y los **días del período** (mínimo 1). | Bloques seguidos del número de días indicado, empezando en la fecha inicial. Ejemplo: «Cada 15 días desde el 01/03/2026». |

**La 5.ª semana.** Si eliges la 5.ª semana y un mes no tiene cinco veces ese día, el cierre cae en la **última** ocurrencia de ese día en el mes (no en el último día del mes). La pantalla lo avisa: «En un mes sin quinta ocurrencia del día elegido, la fecha cae en la última ocurrencia de ese día en el mes.» `Esta información está pendiente de confirmar.`.

### Cómo registrar una versión nueva de la regla

> **Quién puede hacerlo:** Super Administrador y Administrador.

1. En el detalle de la entidad, haz clic en **Nueva versión de regla**.
2. Se abre un diálogo al centro con el título «Nueva versión de regla», la frase «Nueva versión de la regla de corte y pago de la entidad.» y el aviso «El historial no se edita: para corregir una regla se registra una versión nueva.»
3. En **Vigente desde** elige la fecha desde la que empieza a regir esta versión.
4. En el grupo **Regla de corte**, elige el **Tipo de recurrencia del corte** («Selecciona el tipo de recurrencia») y llena los campos que aparecen según el tipo:
   - Semanal: **Día de la semana del corte**.
   - Mensual por posición: **Día de la semana del corte** y **Semana del mes del corte**.
   - Fecha inicial y período: **Fecha inicial del corte** y **Días del período del corte**.
5. En el grupo **Regla de pago**, haz lo mismo con el **Tipo de recurrencia del pago** y sus campos («… del pago»).
6. Haz clic en **Guardar**. Mientras se envía dice «Guardando…».

Al terminar verás el diálogo cerrado y la versión nueva en la tabla «Historial de reglas de corte y pago». Si cambias el tipo de recurrencia, los campos del tipo anterior se borran y desaparecen, para que no viaje ningún dato sobrante.

Reglas que conviene recordar:

- **Todo es obligatorio:** la vigencia y, en corte y en pago, el tipo con todos sus campos. Si falta algo verás «Completa la vigencia y, en corte y pago, el tipo de recurrencia con todos sus campos.»
- **Corregir una regla = registrar otra versión.** Si te equivocaste, registra una nueva con la misma fecha en **Vigente desde**: entre dos versiones con la misma fecha, rige la que se creó después.
- Puedes registrar versiones con una vigencia **futura**: quedan en la tabla, pero no llevan la etiqueta **Vigente** hasta que llegue su fecha.

### Cómo leer el historial de reglas

La tabla «Historial de reglas de corte y pago» tiene cuatro columnas: **Vigente desde** (con la etiqueta **Vigente** en la versión que rige hoy), **Corte**, **Pago** y **Registrada el**. Va ordenada con la fecha de vigencia más reciente arriba. **Corte** y **Pago** se leen como una frase: «Semanal — lunes», «Mensual — 2.ª semana, miércoles» o «Cada 15 días desde el 01/03/2026».

- La etiqueta **Vigente** la pone el sistema con la fecha de Bogotá: es la versión de fecha más reciente que ya haya empezado. **No siempre es la primera fila**: una versión con fecha futura queda arriba sin etiqueta.
- Si todavía no hay ninguna: «Todavía no hay reglas registradas.»

### Intermediación

**Qué es.** Cuando una venta se financia con una entidad, la financiera descuenta una parte. Aquí defines cuánto, como una **fracción del valor de venta** (0.1200 es 12 %) y, si aplica, un **IVA que se cobra sobre esa intermediación** (no sobre el valor de la venta). El cálculo del recargo y de su IVA lo hace el sistema al registrar la venta; aquí solo se guarda la tasa.

Cómo la usa el sistema:

- Solo cuenta en las ventas de modalidad **financiada con una entidad**. En el contado y en la cartera propia no hay intermediación.
- Cada venta usa la versión que regía en **su** fecha, y la **guarda congelada** (tasa, valor del recargo e IVA). Por eso cambiar la tasa después **no modifica las ventas ya hechas**.
- El total que se cobra en la venta suma el valor de venta, el recargo y el IVA del recargo. Ese recargo lo descuenta la financiera al desembolsar, así que va en la línea de **financiación** y no como dinero recibido en caja. Mira [Registrar una venta](../ventas/nueva-venta.md).
- Una entidad que **no tiene ninguna tasa registrada** se trata como si **no cobrara**: es el estado normal mientras no se carguen las tasas reales.

### Cómo registrar una tasa de intermediación nueva

> **Quién puede hacerlo:** solo el Super Administrador (permiso «Fijar la tasa de intermediación»). El Administrador puede **ver** el historial, pero no ve el botón; si lo intentara por otra vía, el sistema se lo rechaza. No se puede otorgar como permiso extra.

1. En el detalle de la entidad, haz clic en **Nueva tasa de intermediación**.
2. Se abre un panel lateral con el título «Nueva tasa de intermediación», la frase «Rige desde la fecha indicada. El historial no se edita.» y el aviso «El historial no se edita: para corregir la tasa se registra una versión nueva.»
3. En **Vigente desde** confirma o cambia la fecha (viene con la de hoy).
4. Deja marcada **Cobra intermediación** si la financiera cobra; desmárcala si **no** cobra (entonces la tasa se bloquea y se vacía).
5. En **Tasa de intermediación** escribe la fracción, con **punto** y menor que 1: `0.1200` es 12 %. Debajo verás la ayuda «Fracción, menor que 1: 0.1200 es 12 %.» y, mientras escribes, el eco «= 12 %».
6. Si la intermediación lleva IVA, marca **Cobra IVA sobre la intermediación** y escribe en **IVA de la intermediación (%)** el porcentaje (de 0 a 100, hasta dos decimales, con coma o punto; por ejemplo `19` o `12,5`). Verás también el eco «= 19 %».
7. Si quieres, escribe **Notas**.
8. Haz clic en **Guardar**.

Al terminar se cierra el panel y se actualiza el «Historial de intermediación». Si enviaste IVA y el sistema devuelve una versión sin él, aparece un aviso junto al historial y la pantalla lo enfoca: la versión **ya se guardó sin IVA**. Avisa al responsable del sistema. Cuando se actualice, registra una **versión nueva con IVA para cada vigencia afectada**; reabrir o cerrar el panel no corrige lo ya guardado. El aviso puede acumular varias fechas. Es una advertencia condicionada: el servidor de estas fuentes sí admite IVA, no se afirma que lo pierda normalmente.

#### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Vigente desde | La fecha desde la que rige esta versión. | Sí |
| Cobra intermediación | Marcada si la financiera cobra; desmarcada si no cobra. Viene marcada. | Sí (siempre tiene un valor) |
| Tasa de intermediación | Fracción menor que 1, con punto y hasta 4 decimales (`0.1200` = 12 %). `0` es «cobra 0 %», que no es lo mismo que «no cobra». Se bloquea si no cobra. | Sí, si cobra |
| Cobra IVA sobre la intermediación | Marcada si se cobra IVA sobre la intermediación. Solo se puede marcar si la financiera cobra. | No |
| IVA de la intermediación (%) | Porcentaje de 0 a 100, hasta dos decimales. Se habilita solo con la casilla de IVA marcada. Se acepta un `%` al final. | Sí, si cobra IVA |
| Notas | Texto libre. | No |

**Ojo con las dos escalas.** La **tasa** se escribe como **fracción** (`0.1200`) y el **IVA** como **porcentaje** (`19`). Por eso el formulario muestra el eco («= 12 %», «= 19 %»): si escribes `0.19` en el IVA verás «= 0,19 %».

**El IVA que ya rige.** Al abrir el panel, si la versión que rige hoy cobra IVA, la casilla de IVA viene **marcada y con ese porcentaje**, y debajo dice «La versión que rige hoy cobra IVA del 19 %: destildar la casilla lo quita en la versión nueva.» Así, corregir solo la tasa no te quita el IVA por accidente. Si cambias la fecha de **Vigente desde** a otra **sin haber tocado la casilla de IVA ni su porcentaje**, la casilla vuelve a verse sin marcar (porque en esa otra fecha podría regir otra versión) y debajo dice «Sin marcarla, si la versión que rige en esa fecha cobra IVA, el servidor pide decidirlo antes de guardar.» Si entonces guardas sin decidir y en esa fecha regía una versión con IVA, el sistema te responde «La intermediación que rige en la fecha de vigencia de esta versión cobra IVA: indica si la nueva lo sigue cobrando (y con qué tasa) o si lo quita.» y te guía: «Para mantener el IVA: tildar la casilla y escribir su porcentaje. Para quitarlo: tildarla y destildarla.»

Si ya tocaste la casilla de IVA o escribiste su porcentaje, esa decisión se conserva al cambiar **Vigente desde**. Revisa la casilla y el porcentaje antes de guardar; el aviso para decidir el IVA no aparece necesariamente en ese caso.

**Corregir una tasa.** Como en las reglas, una tasa mal digitada se corrige registrando otra versión con la misma fecha de **Vigente desde**: rige la que se creó después.

### Cómo leer el historial de intermediación

La tabla «Historial de intermediación» tiene cuatro columnas: **Vigente desde** (con la etiqueta **Vigente** en la versión que rige hoy), **Intermediación**, **Notas** y **Registrada el**. En **Intermediación** verás, por ejemplo, «12 %», «11 % + IVA 19 %» o «No cobra». **Notas** muestra «—» si está vacía. La etiqueta **Vigente** sigue la misma regla que en las reglas de corte y pago. Si todavía no hay ninguna: «Todavía no hay tasas de intermediación registradas.»

## Qué ve cada rol

| Rol | Ve las pantallas | Crea y edita entidades | Deshabilita / anula | Registra versión de regla | Registra tasa de intermediación | Observaciones |
|---|---|---|---|---|---|---|
| Super Administrador | Sí | Sí | Sí | Sí | **Sí** | Es el único que fija la tasa de intermediación. |
| Administrador | Sí | Sí | Sí | Sí | No | Ve el historial de intermediación, pero no el botón. |
| Administrador de Punto | No | No | No | No | No | No tiene Administración en su menú. Sí **consulta** las entidades **activas** para elegirlas en una venta, y solo ve nombre y estado (**no** el NIT). |
| Vendedor | No | No | No | No | No | Igual que el Administrador de Punto. |
| Bodeguero | No | No | No | No | No | No consulta entidades financieras. |

- Los permisos se llaman «Consultar entidades financieras» (se puede otorgar como permiso extra a los roles de sede; sirve para registrar ventas), «Crear y editar financieras, reglas e intermediación» (reservado a los roles administrativos) y «Fijar la tasa de intermediación» (reservado al Super Administrador). Ver [Detalle de un usuario y sus permisos](usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra).
- El [Informe de financieras](../dashboard/informe-de-financieras.md), que usa las reglas de corte y pago, está reservado a los roles administrativos.

## Relación con otros módulos

**Necesitas antes:**
- Nada. La entidad se crea sola. Para que sirva de algo en una venta hay que cargarle, desde su detalle, al menos la **tasa de intermediación** si cobra (sin ella se trata como que no cobra) y, para el informe, una **regla de corte y pago**.
- Lecturas de apoyo, según la tarea que realices: [Lista completa de permisos extra](usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra).

**Esto afecta a:**
- [Registrar una venta](../ventas/nueva-venta.md) y [Ventas](../ventas/ventas.md): una venta financiada exige elegir una entidad **activa**, y su tasa vigente define el recargo y el IVA del recargo que se suman al total. Ver también [Solicitudes](../ventas/solicitudes.md) para cambiar la entidad de una venta ya confirmada.
- [Caja](../ventas/caja.md): la línea de financiación no cuenta como dinero recibido en caja; el recargo lo descuenta la financiera al desembolsar.
- [Informe de financieras](../dashboard/informe-de-financieras.md): usa la regla de corte y pago para mostrar la fecha de corte, la fecha estimada de pago y el valor esperado por entidad.
- [Metas](../metas/metas.md): una meta puede referirse a una entidad financiera.
- [Tablero de ventas](../dashboard/tablero-de-ventas.md): puede filtrar las ventas por entidad financiera Consulta el filtro **Financiera** en [Tablero de ventas](../dashboard/tablero-de-ventas.md); está disponible con **Consultar entidades financieras**.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| Un mensaje de que ya existe un registro con ese valor en «NIT» | Otra entidad ya tiene ese NIT. | Búscala en la lista; si es la misma, úsala (o actívala si está deshabilitada). |
| «Este campo es obligatorio.» / «Este campo no puede estar vacío.» | Falta la razón social o el NIT. | Llénalo. Antes de enviar, el navegador también marca los campos vacíos con su propio aviso. |
| «Asegúrate de que este campo no tenga más de 150 caracteres.» (o 20, en el NIT) | El texto es demasiado largo. | Acórtalo. |
| «Completa la vigencia y, en corte y pago, el tipo de recurrencia con todos sus campos.» | Falta la fecha o algún campo del corte o del pago. | Llena todo lo que pide el tipo de recurrencia elegido, en los dos grupos. |
| «Completa la vigencia y, si la financiera cobra, su tasa.» | Falta la fecha, o marcaste «Cobra intermediación» y no escribiste la tasa. | Escribe la fecha y la tasa, o desmarca «Cobra intermediación». |
| «La tasa va como fracción menor que 1, con hasta 4 decimales: 0.1200 es 12 %.» | Escribiste la tasa como porcentaje (`12`), con coma (`0,12`) o con más de 4 decimales. | Escríbela como fracción con punto: `0.1200`. |
| «Falta el porcentaje de IVA: la casilla dice que la financiera lo cobra.» | Marcaste «Cobra IVA…» y dejaste vacío el porcentaje. | Escribe el porcentaje o desmarca la casilla. |
| «El IVA va como porcentaje de 0 a 100, con hasta dos decimales (por ejemplo, 12,5).» | El IVA no está entre 0 y 100 o tiene más de dos decimales. | Corrígelo. |
| «La intermediación que rige en la fecha de vigencia de esta versión cobra IVA: indica si la nueva lo sigue cobrando (y con qué tasa) o si lo quita.» | No decidiste qué pasa con el IVA de la versión que rige en esa fecha. | Sigue la guía que aparece debajo de la casilla (ver arriba). |
| «La tasa de intermediación debe estar entre 0 y 1 (excluido el 1).» | La tasa es 1 o más, o negativa. | Usa una fracción menor que 1. |
| «La versión que rige desde el [fecha] se guardó, pero sin IVA: el servidor todavía no admite el IVA de la intermediación. Cuando se actualice, hay que registrar una versión nueva con el IVA.» | Se guardó una versión sin el IVA enviado; [fecha] es la vigencia que muestra el aviso. Puede aparecer una variante con varias fechas. | Avisa al responsable para actualizar el sistema y después registra una versión nueva con IVA para cada fecha afectada. |
| «La tasa de IVA debe estar entre 0 y 1 (de 0 % a 100 %).» | El IVA sale de 0 a 100 %. | Corrígelo. |
| «Solo se cobra IVA sobre una intermediación que la financiera cobra.» | Intentaste un IVA sin marcar que la financiera cobra. | Marca «Cobra intermediación» o quita el IVA. |
| «La anulación es terminal: la entidad no recibe reglas nuevas.» / «La anulación es terminal: la entidad no recibe versiones nuevas.» | La entidad está anulada. | No hay forma de registrar versiones nuevas; ya no se ofrecen los botones. |
| «No tienes permiso para ver esta información.» | El sistema no te deja hacer esa acción (por ejemplo, un Administrador que intenta fijar la tasa). | Pídele el cambio a un Super Administrador. |
| «El motivo es obligatorio.» | Intentaste deshabilitar, anular o activar sin escribir el motivo. | Escribe el motivo. |
| «El registro ya está deshabilitado.» / «El registro ya está activo.» | Otra persona cambió el estado antes que tú. | Cierra el diálogo y revisa el estado en la tabla. |
| «La entidad financiera «nombre» no está activa (12.2).» | Se intentó vender con una entidad deshabilitada o anulada. | Elige otra entidad o vuelve a activar esta (si no está anulada). |
| Un aviso rojo con el botón **Reintentar** | No se pudo cargar la lista, la entidad o uno de los historiales. | Haz clic en **Reintentar**. |

## Preguntas frecuentes

**¿Dónde cambio el NIT?** Con el lápiz del listado (no desde el detalle).

**Me equivoqué en una regla de corte o de pago. ¿Cómo la corrijo?** Registra una versión nueva con la misma fecha de **Vigente desde**: la que se creó después es la que rige. La equivocada queda en el historial.

**¿Por qué el Administrador no puede fijar la tasa?** Porque es un parámetro que mueve dinero y el sistema lo reserva al Super Administrador. El Administrador sí ve el historial.

**¿Las ventas viejas cambian si registro una tasa nueva?** No. Cada venta guarda la tasa con la que se hizo.

**¿Qué pasa si la entidad no tiene tasa?** Se trata como si no cobrara intermediación. Carga la tasa real desde el detalle cuando la tengas.

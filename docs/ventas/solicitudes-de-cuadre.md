# Cómo pedir y resolver una rectificación de cuadre

Corrige el contado de un cuadre o incorpora movimientos del mismo día que entraron después de cerrarlo. La aprobación crea otra revisión; conserva intacta la anterior.

> **Quién puede hacerlo:** quienes tienen «Cuadres de caja» piden y consultan dentro de su alcance. Super Administrador y Administrador aprueban o rechazan.
> **Dónde está:** Ventas → Cuadre de caja → ficha del cuadre → **Pedir rectificación**. Para seguimiento: **Rectificaciones de cuadre** en el listado de cuadres.

## Antes de empezar

Necesitas un cuadre cerrado cuya revisión siga vigente. No puede existir otra rectificación pendiente sobre ese cuadre. Si ya fue rectificado, usa la revisión vigente para la próxima petición.

La solicitud no cambia por sí sola el cuadre. Al aprobarla se vuelve a consultar el libro de movimientos del **día del cuadre**, usando el efectivo contado propuesto. No es una reapertura del cierre ni una modificación de los movimientos de caja.

## Cómo pedir la rectificación

1. Abre la revisión vigente desde [Cuadre de caja](cuadres-de-caja.md).
2. Haz clic en **Pedir rectificación**. También puedes iniciar desde **Cuadrar el día** si ese día ya tiene cuadre.
3. Revisa o cambia **Efectivo contado**, en pesos enteros, sin centavos y no negativo. Cero es válido.
4. Escribe la **Justificación** obligatoria.
5. Llena **Observaciones** si las necesitas.
6. Haz clic en **Pedir rectificación**.

Al terminar se cierra el diálogo y aparece la confirmación con **Ver solicitud**. El cuadre mantiene su revisión actual mientras se decide. El contado puede abrir lleno con el valor de la revisión: compruébalo, aunque tu propósito sea incorporar movimientos tardíos.

La sucursal y la fecha no se cambian en el diálogo: vienen del cuadre elegido. En la revisión aprobada, unas Observaciones vacías conservan las observaciones de la revisión anterior.

## Cómo consultar la bandeja y el resultado

1. En **Cuadre de caja**, haz clic en **Rectificaciones de cuadre**.
2. Revisa la bandeja, que abre en **Pendiente**.
3. En **Estado**, elige Pendiente, Aprobada o Rechazada. No hay una opción de todos los estados.
4. Usa **Cuadres desde** y **Cuadres hasta** para filtrar por la fecha del cuadre de origen. Están disponibles también para usuarios de sede.
5. Si tienes alcance global, filtra por **Sucursal** y **Ciudad**.
6. Usa **Ver** en la columna Acciones para abrir una petición.

La tabla presenta **Cuadre**, **Fecha del cuadre**, **Contado pedido**, **Solicitante**, **Fecha**, **Justificación**, **Estado** y **Acciones**; con alcance global añade Sucursal. **Fecha** indica cuándo se pidió la rectificación; los filtros de fechas usan **Fecha del cuadre**. El enlace del Cuadre abre el cierre, no la solicitud. Cambiar filtros vuelve a la primera página.

La ficha **Rectificación** muestra el cuadre, su revisión, sucursal, fecha, solicitante, justificación y observaciones. En una resuelta muestra quién resolvió, cuándo y la nota; una aprobada enlaza su **Revisión resultante**. No hay notificaciones: entra a la bandeja para consultar lo pendiente.

## Cómo aprobar o rechazar

> **Quién puede hacerlo:** Super Administrador y Administrador. El Administrador no aprueba su propia solicitud; el Super Administrador sí puede hacerlo.

1. Abre una rectificación **Pendiente**.
2. Comprueba el cuadre de origen, el contado pedido y la justificación.
3. Haz clic en **Aprobar**.
4. Confirma con **Aprobar** en **Aprobar rectificación**.

Al terminar se resuelve la solicitud y se crea la revisión siguiente, enlazada como **Revisión resultante**. La anterior queda Rectificada. El sistema vuelve a sumar los movimientos existentes del día original al momento de aprobar: el resultado puede incluir movimientos que todavía no estaban cuando se pidió la rectificación. La revisión identifica como quien contó y cerró al solicitante; el aprobador queda identificado en la solicitud y la auditoría.

Aunque la confirmación diga «releyendo el libro de hoy», se relee el día del cuadre elegido, incluso si es una fecha anterior.

Para rechazar:

1. Haz clic en **Rechazar**.
2. Escribe el motivo obligatorio.
3. Confirma con **Rechazar**.

El cuadre queda igual y la solicitud se cierra con el motivo. Una resuelta no admite otra resolución. El Administrador sí puede rechazar su propia petición.

## Qué ve cada rol

| Rol | Consulta y pide | Aprueba / rechaza |
|---|---|---|
| Super Administrador | Alcance global | Sí, incluso aprobar la propia. |
| Administrador | Alcance global | Sí, excepto aprobar la propia. |
| Administrador de Punto | Cuadres y rectificaciones de su sucursal | No. |
| Vendedor / Bodeguero | Su sede con «Cuadres de caja» efectivo | No. |

Esta bandeja **no se limita al solicitante propio** para los usuarios de sede; muestra las rectificaciones de su alcance. Es distinto de [Solicitudes de venta](solicitudes.md). Aprobar rectificaciones es reservado a los roles administrativos y no se otorga como extra.

## Relación con otros módulos

**Necesitas antes:**
- [Cuadre de caja](cuadres-de-caja.md) cerrado y vigente.
- [Caja](caja.md) con los movimientos correctos del día que vas a consolidar.

**Esto afecta a:**
- [Cuadres de caja](cuadres-de-caja.md): añade una revisión que puedes consultar, exportar e imprimir.
- El libro de [Caja](caja.md) se consulta de nuevo, pero aprobar una rectificación no agrega ni borra movimientos de dinero.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Este cuadre ya tiene una solicitud pendiente: resuélvela antes de abrir otra.» | Ya existe una petición abierta. | Abre Ver solicitud o la bandeja Pendiente. |
| «Ese cuadre ya fue rectificado: pide el cambio sobre la revisión vigente.» | El cierre elegido ya tiene sucesor. | Abre la revisión vigente. |
| «Pediste esta rectificación: la aprueba otro administrador.» | Eres el Administrador solicitante. | Deja la aprobación a otro administrador. |
| «Esta solicitud de rectificación ya fue resuelta: no se puede resolver dos veces (cambio 2.5).» | Otro intento ya la resolvió. | Recarga y consulta el resultado. |
| «El efectivo contado tiene que ser un número entero, sin signo.» | Escribiste un negativo o un formato inválido. | Escribe el contado entero no negativo. |

Si no llega confirmación, consulta la bandeja antes de reenviar. Si no aparece Pedir rectificación, comprueba si estás en una revisión anterior o si ya hay una solicitud pendiente. No alteres el cuadre exportado para simular otra revisión.

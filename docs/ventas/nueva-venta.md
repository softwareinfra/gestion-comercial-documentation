# Cómo registrar una venta

Registra el equipo, el cliente y la forma de pago. Al confirmar, el equipo queda vendido y se registran los ingresos de caja que correspondan a los pagos recibidos.

> **Quién puede hacerlo:** Super Administrador, Administrador, Administrador de Punto y Vendedor. Un Bodeguero necesita el permiso extra efectivo «Registrar ventas» y sus requisitos.
> **Dónde está:** menú lateral → Ventas → Ventas → **Nueva venta**.

## Antes de empezar

- Verifica el equipo en [Inventario](../inventario/equipos.md). Debe estar activo, en un estado que permita venderlo y en un punto de venta. Una bodega pura debe [trasladarlo](../inventario/traslados.md) antes.
- Ten el documento del cliente y los datos del pago. Las ventas **Financiada** y **Cartera propia** requieren plan de cuotas y referencias familiar y personal.
- La sucursal sale de la ubicación del equipo. El asesor es quien registra la venta: no eliges otro vendedor ni otra sucursal en el formulario.
- El precio necesita [parámetros de precio](../inventario/precios.md). Los [topes de descuento](topes-de-descuento.md) limitan la rebaja que puedes aplicar.

## Cómo elegir el equipo y el cliente

1. Haz clic en **Nueva venta**. Se abre una página de formulario.
2. Escribe el **IMEI** del aparato.
3. Haz clic en **Buscar equipo**.
4. Comprueba que el equipo encontrado corresponde al que vas a entregar.
5. Elige el **Tipo de documento** del cliente.
6. Escribe su **Número de documento**.
7. Haz clic en **Buscar cliente**.
8. Si el cliente existe, revisa sus datos. Si no existe con ese tipo y número, completa los campos que aparecen.

Cambiar el IMEI o el documento exige hacer de nuevo la búsqueda. El tipo de documento cuenta: un mismo número registrado con otro tipo no es el cliente elegido.

Los datos del cliente existente se muestran para consulta. Este formulario no corrige su ficha. Un cliente nuevo se crea al registrar la venta; buscarlo y llenar sus datos no confirma todavía la operación.

### Datos del cliente

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Tipo de documento | Cédula de ciudadanía, Cédula de extranjería, Tarjeta de identidad, Pasaporte, NIT o Permiso especial de permanencia. | Sí |
| Número de documento | Cédulas y Tarjeta de identidad: 5 a 15 dígitos. Pasaporte y Permiso especial de permanencia: 5 a 20 letras o dígitos, sin guiones. NIT: 9 a 15 dígitos y, si aplica, guion seguido de un dígito de verificación. | Sí |
| Nombres / Apellidos | Hasta 100 caracteres en cada campo. | Sí, para cliente nuevo |
| Celular | Si lo llenas, un celular válido de 10 dígitos que empiece por 3. | No |
| Correo | Un correo válido, si lo llenas. | No |
| Fecha de nacimiento / Fecha de expedición | Fechas que no sean futuras. La expedición no puede ser anterior al nacimiento. | No |
| Dirección | Hasta 255 caracteres. | No |

## Cómo completar Modalidad y valores

1. Elige **Modalidad**: **Contado**, **Financiada** o **Cartera propia**.
2. Revisa el **Precio de referencia** que aparece para el equipo y la modalidad.
3. Ajusta ese precio si corresponde a la venta que acordaste.
4. Escribe el **Descuento**, si vas a aplicarlo.
5. Comprueba el **Valor de venta**: precio de referencia menos descuento.
6. Si vendes a crédito, completa el plan y las referencias indicadas abajo.
7. Escribe **Observaciones**, si las necesitas.

El precio que aparece usa el precio publicado del equipo; si no tiene uno fijado, usa el sugerido por los parámetros. Bajar ese precio también cuenta como descuento: la rebaja efectiva es la reducción frente al precio del equipo más el campo Descuento. Subirlo no compensa el descuento. El sistema compara esa rebaja con tu tope al registrar.

Escribe el dinero en pesos enteros. El precio y el valor de venta deben ser mayores que cero. No confundas el valor de venta con el **Total a pagar** de una financiada: este último puede incluir recargo e IVA de intermediación.

### Campos de crédito y referencias

| Campo | Cuándo y cómo llenarlo |
|---|---|
| Entidad financiera | Obligatoria en Financiada; también puede exigirla el medio de pago elegido. Debe estar activa. |
| Número de contrato (opcional) | En Financiada, el número que entrega la entidad, hasta 60 caracteres; puede quedar vacío si aún no lo ha emitido. |
| Crédito autorizado | El valor del crédito. En Financiada genera una línea de Financiación con ese mismo monto; cámbialo aquí, no en esa fila. |
| Número de cuotas | En Financiada y Cartera propia, al menos 1 cuota. |
| Valor de la cuota | En Financiada y Cartera propia, mayor que cero. |
| Periodicidad | En crédito, elige Semanal, Catorcenal, Quincenal o Mensual. |
| Nombre de la referencia familiar / Teléfono de la referencia familiar | Obligatorios en Financiada y Cartera propia. Nombre hasta 150 caracteres; teléfono hasta 15. |
| Nombre de la referencia personal / Teléfono de la referencia personal | Obligatorios en Financiada y Cartera propia. Nombre hasta 150 caracteres; teléfono hasta 15. |

En **Contado** no aparece la sección Referencias ni se exige el plan de crédito. Cambiar a Contado limpia los campos del plan; revisa los medios antes de registrar. En Cartera propia, el crédito autorizado no crea por sí mismo una fila: completa los medios de pago que correspondan.

## Cómo distribuir el pago y confirmar

1. En **Medios de pago**, elige el medio de la primera línea editable.
2. Escribe el **Valor de la línea**.
3. Llena la **Referencia de la línea** si necesitas identificar el pago; admite hasta 60 caracteres.
4. Usa **Agregar medio de pago** si necesitas repartir el valor entre otros medios.
5. Usa **Quitar** para retirar una fila que no vas a completar.
6. Revisa el resumen: **Completo** indica que las líneas cubren el total; **Faltan** o **Sobran** muestran la diferencia.
7. Haz clic en **Registrar venta**.

La venta exige al menos un medio y admite hasta 20 líneas. Los medios deben estar activos y sus montos deben ser mayores que cero. Contado no admite el medio Financiación. En Financiada, la línea del crédito autorizado se muestra en lectura; al cambiar ese crédito se actualiza su valor.

En Financiada, revisa **Recargo por intermediación**, **IVA de la intermediación** si aplica y **Total a pagar**. El recargo y su IVA deben quedar cubiertos dentro de Financiación; ponerlos únicamente en efectivo u otro medio no cumple esa regla. ADDI se elige como entidad financiera, con su configuración, igual que las otras entidades.

Mientras se envía aparece **Registrando…**. Al terminar se abre la ficha de la venta registrada. El equipo pasa a **Vendido**. Se crean movimientos de caja por los pagos recibidos; las líneas de Financiación y Cartera propia no generan ingreso inicial de dinero. La venta conserva los datos del equipo, cliente, precios y texto de aceptación usados al registrar.

## Qué ve cada rol

| Rol | Puede registrar | Alcance del equipo |
|---|---|---|
| Super Administrador / Administrador | Sí | Sucursales de alcance global; la bodega pura no vende. |
| Administrador de Punto / Vendedor | Sí | Su sucursal. |
| Bodeguero | Con «Registrar ventas» y sus requisitos efectivos | Su ubicación asignada; si es bodega pura, debe trasladar el equipo antes. |

El permiso extra no amplía el alcance. El formulario muestra el precio y el total que paga el cliente; ver el costo y la ganancia es un permiso distinto, explicado en [Ventas](ventas.md).

## Relación con otros módulos

**Necesitas antes:**
- [Equipos disponibles](../inventario/equipos.md) y [precios](../inventario/precios.md).
- [Entidades financieras](../administracion/entidades-financieras.md) y [medios de pago](../administracion/medios-de-pago.md), según la venta.
- [Topes](topes-de-descuento.md) y [texto de aceptación](texto-de-aceptacion.md) configurados para el negocio.
- Lecturas de apoyo, según la tarea que realices: [Formularios y acciones comunes: crear, editar, deshabilitar y anular](../general/formularios-y-acciones-comunes.md); [Categorías de caja](../administracion/categorias-de-caja.md); [Estados operativos](../administracion/estados-operativos.md); [Referencias](../administracion/referencias.md); [Sucursales](../administracion/sucursales.md); [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md); [Usuarios](../administracion/usuarios.md); [Registrar y consultar ingresos](../inventario/ingresos.md); [Trasladar equipos entre sedes](../inventario/traslados.md).

**Esto afecta a:**
- [Detalle del equipo](../inventario/equipo-detalle.md): queda vendido.
- [Caja](caja.md): recibe los movimientos por el dinero cobrado.
- [Comprobante](comprobante-de-venta.md): usa los datos conservados en la venta.
- [Metas](../metas/metas.md): cuentan equipos y suman el valor vendido después del descuento, sin recargo ni IVA de intermediación, de las ventas computables.
- [Tablero de ventas](../dashboard/tablero-de-ventas.md): usa las ventas computables y muestra además la ganancia de venta cuando tu permiso permite verla.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «El equipo pertenece a otra sucursal (6.6).» | El aparato está fuera de tu alcance. | Revisa su ubicación con quien administra Inventario. |
| «El equipo no está activo (8.10).» | No admite la venta en su situación actual. | Revisa su ficha; no intentes vender otro IMEI como sustituto. |
| «Una bodega pura no registra ventas: traslada el equipo antes (6.2).» | El equipo está en una bodega. | Gestiona el traslado al punto que vende. |
| «Esta venta exige una entidad financiera (9.8).» | La modalidad o uno de los medios la necesita. | Elige una entidad activa. |
| «Este campo es obligatorio para esta modalidad (9.4).» | Falta una referencia exigida para crédito. | Completa el campo señalado. |
| «Completa esta línea o quítala.» | Hay una fila de pago sin completar. | Completa medio y valor, o usa Quitar. |
| «No se pudo confirmar si la venta quedó registrada. Revisa el historial de ventas antes de volver a intentar.» | No llegó confirmación de la operación. | Vuelve al listado y busca por IMEI o documento antes de reenviar. |

Si el aviso dice que el equipo ya tiene una venta activa, identifica la venta con el consecutivo indicado y revísala en el listado. Si rechaza el descuento, revisa tanto **Precio de referencia** como **Descuento**. Un error de cuotas, documentos o fechas se corrige en el campo señalado.

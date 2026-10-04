# Cómo cuadrar la caja del día

Compara el efectivo que indica el sistema con el que cuentas físicamente. Al cerrar queda una foto del día, con su desglose, contado y diferencia.

> **Quién puede hacerlo:** Super Administrador, Administrador y Administrador de Punto, o quien tenga «Cuadres de caja» efectivo, dentro de su alcance.
> **Dónde está:** menú lateral → Ventas → **Cuadre de caja** → **Cuadrar el día**.

## Antes de empezar

- Revisa los movimientos en [Caja](caja.md) y registra lo pendiente antes de cerrar.
- Una bodega pura no tiene cuadre.
- La fecha del cuadre debe ser hoy o anterior, dentro de la ventana operativa que el sistema llama **12 meses**; la comprobación admite hasta 366 días hacia atrás desde hoy.
- El día arranca en cero: el efectivo esperado no arrastra el saldo de días anteriores. Puede ser negativo si ese día hubo más egresos netos en efectivo.
- Un día cerrado no se reabre ni se edita; se corrige mediante [rectificación aprobada](solicitudes-de-cuadre.md).

## Cómo consultar cuadres existentes

1. Entra a **Cuadre de caja**.
2. Filtra por fechas.
3. En **Mostrar**, elige **Vigentes** o **Todas las revisiones**.
4. Si tienes alcance global, filtra por **Sucursal** y **Ciudad**.
5. Haz clic en el **Número** del cuadre o en **Ver**.

La tabla muestra **Número**, **Fecha**, **Rev.**, **Esperado**, **Contado**, **Diferencia**, **Estado** y **Acciones**; con alcance global añade Sucursal. Una revisión reemplazada se muestra **Rectificado**; la más reciente, **Vigente**. **Todas las revisiones** conserva el historial. Al cambiar filtros vuelves a la primera página.

## Cómo preparar y cerrar el día

1. Haz clic en **Cuadrar el día**.
2. Elige **Sucursal** si tienes alcance global; con alcance de sede se usa la asignada.
3. Elige la **Fecha del cuadre**.
4. Revisa **Efectivo**: ingresos, egresos y esperado.
5. Revisa **Totales del día** y **Desglose** por categoría y medio de pago.
6. Haz clic en **Cerrar el día** si todavía no está cerrado.
7. Cuenta físicamente el efectivo.
8. Escribe el total en **Efectivo contado**.
9. Llena **Observaciones** si necesitas explicar el cierre.
10. Confirma con **Cerrar el día**.

**Efectivo contado** es obligatorio y debe ser un entero no negativo, sin centavos. Cero es válido para una caja vacía. No escribas el esperado en lugar del dinero contado para forzar que cuadre.

Al terminar se abre la ficha del cuadre cerrado. El sistema vuelve a leer los movimientos del día al confirmar; no congela únicamente las cifras de la vista previa. Calcula **Diferencia = Efectivo contado − Efectivo esperado**: cero es **Cuadra**, negativa es **Faltante** y positiva es **Sobrante**. No exige diferencia cero para cerrar.

Los totales se calculan a partir del neto de cada grupo de categoría y medio: los netos positivos suman a ingresos, los negativos a egresos. Un reverso del mismo grupo puede compensar su importe. El esperado usa los grupos del medio Efectivo. Para el día sin movimientos se puede registrar contado cero y cerrar.

## Cómo interpretar avisos y revisiones

| Aviso o estado | Qué significa | Qué hacer |
|---|---|---|
| El día ya tiene un cuadre | No puedes cerrarlo de nuevo. | Abre el cuadre existente; pide rectificación si hace falta. |
| Movimientos posteriores | Se registraron más movimientos para ese día después de congelar la revisión. | Pide rectificación para incorporarlos. |
| Días con movimientos sin cuadrar | Entre un cuadre anterior y este hay días con movimientos sin su cuadre. | Revisa esos días y registra los cuadres que falten. |
| Rectificado | Existe una revisión que reemplaza esta foto. | Usa **Ver la revisión vigente** cuando esté disponible. |
| Rectificación pendiente | Hay una solicitud sin resolver. | Usa **Ver solicitud**; no envíes otra para el mismo cuadre. |

La revisión cerrada conserva sus cifras aunque entren movimientos después. El aviso de días pendientes no impide cerrar y no afirma que falten todos los días sin actividad. Una revisión posterior enlaza el cuadre anterior y su motivo.

## Cómo imprimir y exportar el cuadre

1. Abre la revisión que necesitas.
2. Para descargarla, haz clic en **Exportar Excel**.
3. Para imprimir, haz clic en **Imprimir**.
4. En **Imprimible del cuadre**, revisa los datos y haz clic en **Imprimir**.
5. Elige impresora o guardar en PDF en el navegador.

La exportación y el documento corresponden a la revisión abierta, no al libro vivo de Caja. Conservan las cifras y el desglose del cuadre, y declaran su estado y rectificación cuando corresponda. Puedes imprimir una revisión anterior para archivo. Usa **Volver al cuadre** para regresar desde el imprimible.

## Qué ve cada rol

| Rol | Consulta, cierra, imprime, exporta y pide rectificación | Alcance |
|---|---|---|
| Super Administrador / Administrador | Sí | Global; elige la sucursal. |
| Administrador de Punto | Sí | Su sucursal. |
| Vendedor / Bodeguero | Con «Cuadres de caja» efectivo | Su ubicación; una bodega pura no tiene cuadre. |

La aprobación de una rectificación es otra acción, reservada al Super Administrador y Administrador. Tener **Cuadres de caja** no permite aprobar.

## Relación con otros módulos

**Necesitas antes:**
- [Caja](caja.md) y sus movimientos del día.
- [Sucursal](../administracion/sucursales.md) que maneje caja, [categorías](../administracion/categorias-de-caja.md) y [medios de pago](../administracion/medios-de-pago.md).
- [Ventas](ventas.md) y sus abonos: los movimientos que generen en la fecha del cuadre participan en el consolidado de ese día.
- Lecturas de apoyo, según la tarea que realices: [Exportar a Excel e imprimir](../general/exportar-e-imprimir.md); [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md); [Cómo pedir y resolver una rectificación de cuadre](solicitudes-de-cuadre.md).

**Esto afecta a:**
- [Rectificaciones de cuadre](solicitudes-de-cuadre.md): una corrección genera otra revisión con aprobación.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Cuenta el efectivo y escribe el total.» | Falta el contado. | Cuenta el dinero y llena Efectivo contado. |
| «El efectivo contado va en pesos enteros, sin centavos.» | El formato del contado no es válido. | Escribe un entero sin decimales. |
| «La fecha del cuadre no puede ser posterior a hoy (cambio 2.5).» | Elegiste una fecha futura para el negocio. | Elige hoy o una fecha anterior. |
| «La fecha del cuadre está fuera de la ventana operativa de 12 meses (§15.2).» | La fecha es demasiado antigua. | Revisa el día que necesitas cuadrar. |
| «Una bodega no maneja caja: no tiene cuadre (6.2).» | La sede es bodega pura. | Usa una sucursal que maneje caja. |

Si otra persona cerró el día mientras contabas, revisa el cuadre que ya existe. Ante una pérdida de confirmación, busca el cuadre por sucursal y fecha antes de volver a cerrar. No fuerces un segundo cierre: pide rectificación sobre el vigente.

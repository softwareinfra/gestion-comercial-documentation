# Cómo consultar créditos y cortes por financiera

Compara créditos colocados, valores de venta y financiación, y consulta el valor esperado y las fechas del corte calculado con la regla vigente de cada financiera.

> **Quién puede hacerlo:** Super Administrador y Administrador. **Informe de financieras** es un permiso reservado; no se otorga como extra a los roles de sede.
> **Dónde está:** menú lateral → Dashboard e Informes → Financieras. Verás **Informe de financieras**.

## Antes de empezar

- Créditos, valor de venta y valor financiado responden al período que consultas.
- Valor esperado, fecha de corte y pago estimado responden al **período de corte completo de la entidad**, calculado tomando hoy como referencia con la regla vigente hoy. Si hoy es anterior a la fecha inicial de la recurrencia de corte, se usa su primer período, aunque sea futuro. No usan como corte el rango del informe.
- La financiación se toma de las líneas de pago vigentes; no equivale al precio de venta ni a efectivo recibido en caja.
- Para tener fechas y valor esperado, la entidad debe tener una [regla de corte y pago](../administracion/entidades-financieras.md) vigente. Sin ella, esas tres columnas muestran «—».

## Cómo elegir la consulta

1. Entra a Dashboard e Informes → **Financieras**.
2. Elige **Periodo**, o **Rango personalizado** con **Desde** y **Hasta**. Periodo automático usa Mes en curso.
3. Elige **Financiera** si necesitas limitar las ventas que alimentan las cifras.
4. Elige **Modalidad** si necesitas ese recorte.
5. Limita por **Sucursal** o **Ciudad** cuando corresponda.
6. Revisa el alcance, período aplicado y fecha de generación en el encabezado.

Puedes consultar Día en curso, Semana en curso, Mes en curso, Trimestre en curso, Año en curso o Mes anterior. La tabla es un resumen por entidad para ese rango, no una serie diaria por entidad. Para evolución temporal, consulta el [Tablero de ventas](tablero-de-ventas.md) con modalidad financiada y la financiera elegida.

La selección **Financiera** limita las operaciones sumadas. Pueden seguir apareciendo otras entidades activas con cifras del período en cero: el informe incluye entidades activas o con operaciones que aportan al resultado y las ordena por valor financiado, hasta 50. No interpretes esas filas como ventas de otra financiera incluidas en tus totales.

Puedes reutilizar criterios con [Filtros guardados](../general/filtros-guardados.md). **Desglosar por** es configuración del informe: no se elimina al limpiar los filtros de la tarjeta.

## Cómo interpretar las columnas

| Columna | Qué significa |
|---|---|
| Entidad | Financiera y estado de su registro |
| Créditos | Cantidad de ventas de modalidad financiada que cuentan en el rango |
| Valor de venta | Suma del valor de venta de esos créditos, después del descuento, sin intermediación ni IVA |
| Valor financiado | Suma de importes de líneas vigentes con el medio de financiación para las operaciones consultadas |
| Valor esperado | Suma de financiación del período de corte calculado completo, conservando el alcance y criterios de operaciones; no es la suma del rango elegido |
| Fecha de corte | Fin del período de corte calculado tomando hoy como referencia con la regla vigente; antes de su fecha inicial, se usa el primer período |
| Pago estimado | Fin del período de pago calculado tomando la fecha de corte como referencia con esa regla; si precede a la fecha inicial del pago, se usa el primer período |

La vigencia de la versión y las fechas iniciales de corte y pago son independientes. Si la referencia es anterior a la fecha inicial de una recurrencia, se usa su primer período. **Valor esperado** suma la financiación de ese período de corte completo, que puede ser futuro; no supone que el período contenga hoy.

Una modificación puede sustituir financiación por efectivo: la venta sigue contando como crédito si conserva su modalidad financiada, pero su financiación vigente puede bajar. El valor esperado puede superar el valor financiado del período porque sus ventanas son distintas.

Este informe no registra pagos recibidos de la financiera ni resta recaudos de una cuenta por cobrar. **Valor esperado** es la proyección calculada desde líneas de financiación, no una confirmación de pago recibido.

## Cómo revisar e imprimir un desglose

1. En **Desglosar por**, elige **Sucursal** o **Ciudad**. **Sin desglose** es la opción inicial.
2. Haz clic en **Ver desglose** junto a la entidad.
3. Revisa Créditos, Valor de venta y Valor financiado de sus grupos.
4. Abre los desgloses que quieras incluir en papel.
5. Haz clic en **Imprimir**.

Los grupos no repiten valor esperado ni fechas: esos datos pertenecen al corte de la entidad. Se imprime la tabla consultada y los desgloses abiertos, con alcance, período, filtros y fecha de generación. Consulta [Exportar e imprimir](../general/exportar-e-imprimir.md) para guardar la impresión en PDF.

## Qué ve cada rol

| Rol | Acceso |
|---|---|
| Super Administrador / Administrador | Consulta e imprime el informe consolidado, con filtros de ubicación |
| Administrador de Punto / Vendedor / Bodeguero | No tienen este informe por rol ni lo reciben como permiso extra |

Consultar entidades financieras como catálogo de apoyo para registrar una venta no da acceso a este informe.

## Relación con otros módulos

**Necesitas antes:**

- [Entidades financieras](../administracion/entidades-financieras.md): entidades y reglas de corte/pago.
- [Nueva venta](../ventas/nueva-venta.md): modalidad, financiera y líneas de pago que alimentan los valores.
- Lecturas de apoyo, según la tarea que realices: [Exportar a Excel e imprimir](../general/exportar-e-imprimir.md); [Filtros guardados y filtros recordados](../general/filtros-guardados.md); [Sucursales](../administracion/sucursales.md).

**Esto afecta a:**

- La consulta e impresión no modifican entidades, ventas ni caja. Una corrección de pagos se tramita mediante [Solicitudes](../ventas/solicitudes.md).
- [Tablero de ventas](tablero-de-ventas.md): permite consultar la serie temporal de una financiera y comparar el valor vendido con su financiación.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «—» en Valor esperado, Fecha de corte y Pago estimado | No hay regla vigente para calcular el corte | Revisa las reglas de la entidad; no lo interpretes como cero por cobrar |
| «Ninguna financiera con créditos en el periodo y con estos filtros.» | La consulta no devuelve filas de entidades | Revisa catálogo, período y criterios |
| «Periodo recortado» | El rango pedido superó los límites aplicados | Revisa el rango efectivo del encabezado |
| Valor esperado mayor que Valor financiado | Se comparan corte completo y período consultado | Compara las ventanas antes de asumir un error |

Si falla la carga, usa la opción de reintento del informe. Que aparezca una financiera activa con cero créditos no es una confirmación de que tiene un pago recibido o pendiente registrado.

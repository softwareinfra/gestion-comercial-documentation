# Cómo consultar el tablero de inventario

Revisa el stock actual, su valor a costo, los equipos con permanencia prolongada y las referencias con mayor o menor rotación.

> **Quién puede hacerlo:** Super Administrador, Administrador y Administrador de Punto. Vendedor y Bodeguero necesitan el permiso extra **Tablero de inventario**, que requiere **Ver costo y ganancia**.
> **Dónde está:** menú lateral → Dashboard e Informes → Inventario. Verás **Tablero de inventario**.

## Antes de empezar

- El resumen y el desglose son una foto del inventario de **hoy**. El período de rotación no los convierte en un inventario histórico.
- Se consultan equipos con registro activo. **Disponibles** incluye los estados Disponible y Reservado; excluye Vendido, En traslado, En garantía, Devuelto por garantía, Baja por nota crédito e Inactivo.
- El rótulo **Baja por nota crédito** corresponde al estado **Dado de baja por nota crédito** del catálogo.
- **Valor del inventario** usa costo de los equipos disponibles para la venta, no precio sugerido de venta.

## Cómo elegir y consultar el stock

1. Entra a **Tablero de inventario**.
2. Filtra por **Marca**, **Tipo de producto**, **Sistema operativo**, **Referencia** o **Categoría**.
3. Si tienes alcance global, limita por **Sucursal** o **Ciudad**.
4. Revisa el encabezado y las tarjetas del stock.
5. Elige **Desglosar por** para comparar los grupos ofrecidos: Sucursal, Ciudad, Marca, Tipo de producto, Sistema operativo, Referencia o Categoría, según tu alcance.

El desglose muestra **hasta 50 grupos**, con unidades disponibles y su valor a costo, ordenados de mayor a menor cantidad de unidades. No incluye una columna de participación. Este límite es fijo y distinto de **Cuántas referencias** en rotación. Para volver a usar una consulta, revisa [Filtros guardados](../general/filtros-guardados.md).

## Cómo leer la permanencia

| Indicador | Qué significa |
|---|---|
| Disponibles | Cantidad de equipos activos disponibles para venta según los estados admitidos |
| Valor del inventario | Suma de costos de esos equipos |
| Días promedio en inventario | Promedio de días en inventario de esos equipos; «—» si no hay equipos para promediar |
| Alertas de permanencia | Equipos disponibles cuya fecha de ingreso alcanza o supera el umbral de días |
| Valor indicado como inmovilizados | Suma del costo de los equipos que generan esas alertas |

En **Días para la alerta de permanencia**, escribe el umbral que quieres revisar. El valor inicial es 60 días. Este control cambia la alerta y el valor inmovilizado; no filtra el desglose ni la rotación. También puedes revisar la distribución por estados del inventario.

## Cómo revisar la rotación

1. Ve a **Top … referencias por rotación**.
2. Elige **Periodo de rotación**, o un rango con **Rotación desde** y **Rotación hasta**.
3. Elige **Orden de rotación**: Más vendidas o Menos vendidas. Por defecto usa Más vendidas.
4. Elige **Cuántas referencias**: 10, 25 o 50.
5. Revisa **Referencia**, **Vendidas**, **Stock de hoy** y **Días para vender**.

**Vendidas** usa ventas computables del período; **Stock de hoy** usa unidades disponibles actuales. Son dos consultas sobre momentos distintos.

Con los permisos extra para entrar, el **Vendedor** compara sus propias ventas de su sucursal contra el stock disponible de esa sucursal. El **Bodeguero** compara las ventas de su ubicación contra su stock disponible; no se limita a ventas registradas por él.

- **Más vendidas:** ordena por ventas del período. Días para vender promedia los días entre ingreso del equipo y venta, excluyendo del promedio ventas con reemplazo por garantía. Esas ventas sí siguen contando como vendidas.
- **Menos vendidas:** parte de referencias con stock disponible hoy y las ordena desde la menor cantidad vendida, incluidas referencias con cero ventas. Días para vender aparece en raya en este recorrido.

El período afecta este bloque, no las tarjetas del stock. Un período automático usa Mes en curso; también puedes elegir Mes anterior o Rango personalizado como en el [Tablero de ventas](tablero-de-ventas.md#cómo-elegir-la-consulta).

## Cómo imprimir

1. Espera a que carguen los bloques.
2. Haz clic en **Imprimir**.
3. Revisa la vista de impresión del navegador.

La hoja identifica el inventario de hoy, alcance, filtros y fecha de generación. La rotación lleva además su propio rango: ventas del período contra el stock de hoy. No cambies la interpretación del stock por ese rango. Consulta [Exportar e imprimir](../general/exportar-e-imprimir.md) para guardar la hoja en PDF.

La impresión conserva el recorte del desglose de stock: **hasta 50 grupos**, ordenados por unidades. El selector de 10, 25 o 50 referencias corresponde al bloque de rotación.

## Qué ve cada rol

| Rol | Acceso al tablero | Alcance |
|---|---|---|
| Super Administrador / Administrador | Incluido por rol | Todas las ubicaciones, con filtros |
| Administrador de Punto | Incluido por rol | Su sucursal |
| Vendedor | Con Tablero de inventario y Ver costo y ganancia efectivos | Stock de su sucursal; rotación de sus propias ventas en esa sucursal |
| Bodeguero | Con Tablero de inventario y Ver costo y ganancia efectivos | Stock y ventas de su ubicación asignada |

Este tablero exige costo y ganancia como requisito de acceso. El permiso extra no amplía la ubicación; no equivale a poder editar precios o equipos.

## Relación con otros módulos

**Necesitas antes:**

- [Ingresos](../inventario/ingresos.md), [equipos](../inventario/equipos.md) y [traslados](../inventario/traslados.md): stock, fechas de ingreso y ubicación actual.
- [Ventas](../ventas/ventas.md): unidades vendidas para rotación.
- [Garantías](../garantias/equipos-en-garantia.md): sus estados excluyen equipos de Disponibles; un reemplazo cambia qué ventas entran en el promedio de días para vender.
- Lecturas de apoyo, según la tarea que realices: [Exportar a Excel e imprimir](../general/exportar-e-imprimir.md); [Filtros guardados y filtros recordados](../general/filtros-guardados.md); [Categorías de equipo](../administracion/categorias-de-equipo.md); [Ciudades](../administracion/ciudades.md); [Referencias](../administracion/referencias.md); [Sistemas operativos](../administracion/sistemas-operativos.md); [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md).

**Esto afecta a:**

- La consulta e impresión no cambian el stock. Para corregir un equipo, abre su [ficha de inventario](../inventario/equipo-detalle.md).

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «No hay equipos en el desglose para estos filtros.» | No hay stock disponible en esos grupos | Revisa filtros y estados en Inventario |
| «No hubo movimiento de referencias en el periodo.» | La rotación no devuelve referencias con esa consulta | Revisa período, orden y filtros |
| «—» en Días promedio en inventario | No hay equipos para promediar | Revisa Disponibles; no lo interpretes como cero días |
| «—» en Días para vender | No se calculó ese promedio; ocurre en Menos vendidas o si no hay ventas elegibles para promediar | Usa Vendidas y Stock de hoy sin asumir que el tiempo fue cero |

Si el tablero no aparece en el menú, revisa **Tablero de inventario** y su requisito **Ver costo y ganancia**.

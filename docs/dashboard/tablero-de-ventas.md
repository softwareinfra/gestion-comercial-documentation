# Cómo consultar el tablero de ventas

Consulta el valor vendido, la cantidad de equipos, la evolución y los grupos que aportan a las ventas. Puedes imprimir el tablero y descargar la serie o el desglose en Excel.

> **Quién puede hacerlo:** Super Administrador, Administrador, Administrador de Punto y Vendedor. El permiso extra **Tablero de ventas** puede abrirlo a otro usuario en su alcance.
> **Dónde está:** menú lateral → Dashboard e Informes → Ventas. Verás **Tablero de ventas**.

## Antes de empezar

- Los indicadores cuentan ventas computables; una anulación retira el aporte de la venta a su período original.
- **Total vendido** es el valor de venta después del descuento, sin sumar intermediación ni su IVA. No representa necesariamente lo recibido en caja.
- El tablero del Vendedor muestra sus propias ventas dentro de su sucursal. El [listado de ventas](../ventas/ventas.md) puede mostrar también las ventas de sus compañeros de sucursal.
- El encabezado indica alcance, período efectivo y fecha de generación. Si aparece **Periodo recortado**, revisa el rango que realmente se consultó.

## Cómo elegir la consulta

1. Entra a **Tablero de ventas**.
2. Elige **Periodo**: Día en curso, Semana en curso, Mes en curso, Trimestre en curso, Año en curso, Mes anterior o Rango personalizado. Sin elección, Periodo automático usa el mes en curso.
3. Si elegiste **Rango personalizado**, completa **Desde** y **Hasta**.
4. Limita por **Marca**, **Tipo de producto**, **Sistema operativo**, **Referencia** o **Categoría** si lo necesitas.
5. Limita por **Financiera**, **Medio de pago** o **Modalidad** cuando corresponda.
6. Con alcance global, puedes elegir **Sucursal**, **Ciudad** y **Trabajador**.

Los períodos en curso comienzan al inicio del día, semana, mes, trimestre o año y llegan hasta hoy; **Mes anterior** es el mes calendario cerrado anterior. Las fechas se interpretan en la zona horaria configurada para el negocio (Bogotá por defecto) e incluyen el día inicial y el final. Los rangos extensos se recortan desde el final pedido: revisa el encabezado antes de comparar.

El filtro **Medio de pago** selecciona ventas que tienen una línea vigente con ese medio. El resumen sigue sumando el valor completo de esas ventas; no calcula el recaudo de ese medio. **Financiera** aparece cuando puedes consultar ese catálogo.

Puedes reutilizar una consulta con [Filtros guardados](../general/filtros-guardados.md). **Limpiar filtros** limpia los criterios de la tarjeta; la granularidad y la configuración del desglose se controlan en sus bloques.

## Cómo leer los resúmenes

Las tarjetas **Día en curso**, **Semana en curso**, **Mes en curso** y **Año en curso** muestran sus propios rangos. No siguen al filtro de período: aunque consultes Mes anterior, esas cuatro tarjetas siguen siendo las actuales.

Haz clic en **Resumen del periodo** para desplegar sus indicadores y la distribución por modalidad.

| Indicador | Qué significa |
|---|---|
| Total vendido | Suma del valor de venta de las operaciones consultadas |
| Equipos | Cantidad de ventas que cuentan |
| Ticket promedio | Total vendido dividido por cantidad; «—» si no hay ventas |
| Costo del periodo | Suma de costos congelados en esas ventas, si puedes ver costo |
| Ganancia del periodo | Suma de ganancias de esas ventas, si puedes ver costo |
| Margen | Ganancia dividida por total vendido, mostrada como porcentaje; sin base para dividir aparece «—» |

Las tarjetas pueden mostrar además iOS y Android si ambos existen en el catálogo y no filtraste un sistema operativo. No uses esos dos grupos como prueba de que incluyen cualquier otro sistema operativo del catálogo.

## Cómo consultar la evolución

1. Abre **Evolución del periodo**.
2. Elige **Granularidad**: Diaria, Semanal, Mensual, Trimestral o Anual, o deja la elección automática.
3. Revisa el gráfico y la tabla de la serie.
4. Para guardar esta serie, haz clic en **Exportar Excel** en ese bloque.

La elección automática usa días para rangos de hasta 31 días, semanas hasta 120 y meses para los mayores. La serie incluye intervalos sin ventas con cero; no los confunde con días omitidos. La descarga usa la misma consulta de la serie y respeta los datos de costo que puedes ver.

## Cómo comparar grupos de ventas

1. Abre el bloque **Desglose por…**.
2. Elige **Desglosar por**: las opciones incluyen Sucursal, Ciudad, Trabajador, Marca, Tipo de producto, Sistema operativo, Referencia, Financiera, Modalidad y Medio de pago, según lo que la pantalla ofrezca en tu alcance.
3. Elige **Ordenar por**: Valor vendido, Equipos o Ganancia cuando tienes permiso para verla.
4. Elige **Cuántas filas**: 10, 25 o 50.
5. Revisa los valores y la **Participación**.
6. Haz clic en **Exportar Excel** en ese bloque si necesitas descargar el desglose.

El desglose es un grupo de primeras filas, no una lista paginada. La participación usa el total del alcance consultado como base; las filas mostradas pueden sumar menos de 100 %.

**Medio de pago tiene otra base:** suma importes de líneas de pago vigentes, no el valor de venta completo. Una venta con dos medios cuenta en los dos grupos; no sumes las cantidades de esos grupos como si fueran ventas distintas. Ese desglose no muestra costo ni ganancia para ningún rol y se ordena por importe.

## Cómo imprimir

1. Espera a que carguen los bloques que vas a revisar.
2. Haz clic en **Imprimir** en la cabecera del tablero.
3. Revisa la vista de impresión del navegador.

La hoja usa los datos ya consultados y agrega alcance, período, filtros y fecha de generación. Las secciones recogidas también se muestran en papel. Los límites del desglose siguen aplicándose a la impresión y a su Excel. Consulta [Exportar e imprimir](../general/exportar-e-imprimir.md) para guardar en PDF.

## Qué ve cada rol

| Rol | Ventas del tablero | Costo, ganancia y margen |
|---|---|---|
| Super Administrador / Administrador | Todas, con filtros de alcance | Sí |
| Administrador de Punto | Su sucursal | Sí |
| Vendedor | Sus propias ventas en su sucursal | Con Ver costo y ganancia |
| Bodeguero con Tablero de ventas | Ventas de su ubicación | Según su permiso efectivo de costo |

El permiso extra **Tablero de ventas** permite consulta y descarga; no amplía la sucursal. Sin **Ver costo y ganancia**, esos datos tampoco se incluyen en el Excel ni se ofrece ordenar por ganancia.

## Relación con otros módulos

**Necesitas antes:**

- [Registrar ventas](../ventas/nueva-venta.md): datos que alimentan los indicadores.
- [Catálogos de referencias](../administracion/referencias.md), [sistemas operativos](../administracion/sistemas-operativos.md) y [medios de pago](../administracion/medios-de-pago.md): clasificación y filtros.
- Lecturas de apoyo, según la tarea que realices: [Exportar a Excel e imprimir](../general/exportar-e-imprimir.md); [Filtros guardados y filtros recordados](../general/filtros-guardados.md); [Menú lateral y navegación](../general/menu-y-navegacion.md); [Categorías de equipo](../administracion/categorias-de-equipo.md); [Ciudades](../administracion/ciudades.md); [Entidades financieras](../administracion/entidades-financieras.md); [Marcas](../administracion/marcas.md); [Tipos de producto](../administracion/tipos-de-producto.md); [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md); [Cómo solicitar y resolver cambios de una venta](../ventas/solicitudes.md); [Cómo consultar créditos y cortes por financiera](informe-de-financieras.md).

**Esto afecta a:**

- La consulta y exportación no modifican ventas ni caja. Para cambiar una operación, usa [Solicitudes](../ventas/solicitudes.md).
- [Metas](../metas/metas.md): comparte la base de ventas computables, con los períodos y alcances de cada meta.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «No hay ventas en el periodo con los filtros activos.» | La evolución no tiene ventas para esa consulta | Revisa el período y los filtros |
| «Ninguna fila en el desglose para este periodo y estos filtros.» | No hay grupos para la consulta | Cambia dimensión o filtros |
| «Periodo recortado» | El rango aplicado es menor o distinto al pedido por sus límites | Usa el período del encabezado para interpretar las cifras |
| «—» en Ticket promedio | No hay cantidad con la cual calcularlo | Revisa cantidad y filtros; no lo interpretes como una venta de valor cero |

Si falla un bloque, usa su opción de reintento. Si falta Financiera, revisa tu permiso de consulta del catálogo; si faltan costo y ganancia, revisa **Ver costo y ganancia**.

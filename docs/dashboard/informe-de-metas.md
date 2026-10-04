# Cómo comparar metas en un informe

Consulta juntas las metas cuyos períodos se cruzan con el rango elegido y compara su avance y cumplimiento.

> **Quién puede hacerlo:** Super Administrador, Administrador, Administrador de Punto y Vendedor. El permiso extra **Tablero de metas** permite la consulta a otro usuario dentro de su alcance.
> **Dónde está:** menú lateral → Dashboard e Informes → Metas. Verás **Informe de metas**.

## Antes de empezar

- El rango selecciona metas cuyo inicio es igual o anterior al fin consultado y cuyo fin es igual o posterior al inicio consultado, incluidas metas que contienen todo el rango. Una consulta mensual puede traer una meta anual.
- El avance se calcula sobre el período **completo de cada meta**, no sobre el fragmento del rango del informe.
- Las fórmulas de equipos, valor, porcentaje y cumplimiento son las mismas explicadas en [Metas](../metas/metas.md#cómo-interpretar-el-avance).

## Cómo consultar y comparar

1. Entra a **Informe de metas**.
2. Elige **Periodo**, o **Rango personalizado** con **Desde** y **Hasta**. Periodo automático usa Mes en curso.
3. Filtra por **Marca** si corresponde a las metas que buscas. **Financiera** aparece si tienes **Consultar entidades financieras** efectivo.
4. Con alcance global, limita por **Sucursal**, **Ciudad** o **Trabajador**.
5. Revisa **Meta**, **Alcance**, **Periodo**, **Avance**, **Cumplimiento** y **Estado**.
6. Cambia de página para revisar otros resultados.

Marca y Financiera se aplican a la definición de la meta. Una meta con «Todas las marcas excepto esa» puede aparecer al filtrar por su marca de referencia; lee **Alcance**. Este informe permite consulta; para crear o editar, entra a [Metas Comerciales](../metas/metas.md).

El permiso **Tablero de metas** por sí solo no habilita el filtro **Financiera**. Si eres Bodeguero, necesitas además **Consultar entidades financieras** efectivo para usarlo.

**Cumplimiento** y **Estado** son distintos: una meta puede seguir Activa y estar No cumplida. Los alcances globales también pueden recibir metas deshabilitadas; los roles de sede consultan activas.

Puedes guardar criterios con [Filtros guardados](../general/filtros-guardados.md). Cambiar filtros vuelve a la primera página; imprimir conserva la página actual.

## Cómo imprimir la página consultada

1. Ve a la página de resultados que necesitas.
2. Haz clic en **Imprimir**.
3. Revisa el número de página y el total en la hoja.

La impresión contiene la página visible, no todas las metas del resultado. La hoja dice **Página … de … — … metas en total** y agrega alcance, período, filtros y fecha de generación. Si necesitas otra página, vuelve al informe, navega hasta ella e imprime de nuevo. Consulta [Exportar e imprimir](../general/exportar-e-imprimir.md) para guardar cada hoja en PDF.

## Qué ve cada rol

| Rol | Metas del informe |
|---|---|
| Super Administrador / Administrador | De los alcances configurados, con filtros; incluye deshabilitadas |
| Administrador de Punto | Activas de su sucursal e individuales de su equipo actual |
| Vendedor | Activas de su sucursal y sus propias individuales |
| Bodeguero con Tablero de metas | Activas de su ubicación y sus propias individuales |

El informe del Vendedor puede incluir el avance de la meta de su sucursal; no se limita a sus ventas individuales como el [Tablero de ventas](tablero-de-ventas.md). Un extra no amplía el alcance. Aquí no se muestran costo ni ganancia.

## Relación con otros módulos

**Necesitas antes:**

- [Metas](../metas/metas.md): configuración de períodos, alcances y objetivos.
- [Ventas](../ventas/ventas.md): aportes al avance.
- Lecturas de apoyo, según la tarea que realices: [Exportar a Excel e imprimir](../general/exportar-e-imprimir.md); [Filtros guardados y filtros recordados](../general/filtros-guardados.md).

**Esto afecta a:**

- La consulta e impresión no modifican metas ni ventas. Para corregir un objetivo usa [Editar una meta](../metas/metas.md#cómo-editar-deshabilitar-o-activar).
- [Solicitudes de venta](../ventas/solicitudes.md): una anulación aprobada cambia el avance que se consulta después.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Ninguna meta coincide con los filtros.» | No hay metas para el rango y criterios dentro de tu alcance | Revisa períodos de metas y filtros |
| «Todavía no hay metas comerciales para informar.» | La consulta sin filtros propios no devuelve metas | Revisa la configuración en Metas Comerciales |
| «Periodo recortado» | El sistema aplicó un rango limitado | Lee el rango efectivo del encabezado |

Si el porcentaje parece corresponder a más días de los que consultaste, compara el **Periodo** de esa meta: su avance usa ese período completo. Si falla la carga, usa la opción de reintento del informe.

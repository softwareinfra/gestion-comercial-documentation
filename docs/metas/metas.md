# Cómo crear y consultar metas comerciales

Define un objetivo de equipos vendidos, de valor vendido o de ambos para un período. Consulta cuánto se ha alcanzado y cuánto falta.

> **Quién puede hacerlo:** Super Administrador y Administrador crean y gestionan metas. Administrador de Punto y Vendedor consultan e imprimen las metas de su alcance. Un permiso extra puede abrir la consulta al Bodeguero.
> **Dónde está:** menú lateral → Metas Comerciales.

## Antes de empezar

- Una meta tiene un período con inicio y fin, incluidos ambos días. Un período de un día es válido.
- Puedes definir una meta para **Toda la empresa**, una **Sucursal**, una **Ciudad** o un **Trabajador**. Combina ese alcance con marca y entidad financiera si lo necesitas.
- Debes definir al menos un objetivo: cantidad de equipos, valor vendido o ambos. La cantidad debe ser un entero de al menos 1; el valor debe superar cero.
- Las metas pueden compartir períodos. Las ventas del período cuentan aunque sean anteriores a la creación de la meta.
- **Activa / Deshabilitada** dice si se usa la meta; **Cumplida / En curso / No cumplida** dice cómo va frente a sus objetivos.

## Cómo buscar y consultar una meta

1. Entra a **Metas Comerciales**.
2. Usa **Buscar** para buscar por nombre.
3. Usa **Vigente el** para encontrar metas cuyo período incluya ese día. Este filtro no significa que la meta esté activa.
4. Filtra por **Marca** si necesitas limitar la lista. **Financiera** aparece si tienes **Consultar entidades financieras** efectivo.
5. Si tienes alcance global, puedes filtrar también por **Estado**, **Sucursal**, **Ciudad** y **Trabajador**.
6. Haz clic en el nombre de la meta para abrir su ficha.

La tabla muestra **Meta**, **Alcance**, **Periodo**, **Avance** y **Cumplimiento**. El alcance global agrega **Estado** y, para quienes gestionan, acciones. En la ficha puedes revisar **Avance**, **Alcance y periodo**, observaciones y fechas de auditoría.

El filtro Marca busca la marca elegida al definir la meta: también puede encontrar una meta que diga «Todas las marcas excepto» esa marca. Revisa el alcance antes de interpretar el resultado.

El permiso **Consultar metas** por sí solo no muestra el filtro **Financiera**. Si eres Bodeguero, necesitas además **Consultar entidades financieras** efectivo para usarlo.

## Cómo crear una meta

1. Haz clic en **Nueva meta**.
2. Escribe el **Nombre**.
3. Elige **Alcance**.
4. Si elegiste Sucursal, Ciudad o Trabajador, elige el registro correspondiente.
5. Elige **Marca** si la meta se limita por marca.
6. Si elegiste una marca, elige **Aplica a**.
7. Elige **Entidad financiera** si la meta corresponde a una financiera.
8. Completa **Inicio del periodo** y **Fin del periodo**.
9. Completa **Objetivo en equipos**, **Objetivo en valor** o ambos.
10. Escribe **Observaciones** si necesitas aclarar el objetivo.
11. Haz clic en **Guardar**.

Se cierra el diálogo y se actualiza el listado conservando la consulta. La nueva meta puede quedar fuera de los filtros o de la página que estabas viendo.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | Nombre reconocible, máximo 150 caracteres | Sí |
| Alcance | Toda la empresa, Sucursal, Ciudad o Trabajador | Sí; inicia en Toda la empresa |
| Sucursal / Ciudad / Trabajador | Registro del alcance elegido; no se combinan esos tres alcances | Si elegiste ese alcance |
| Marca | Marca de referencia; déjala sin selección para no limitar por marca | No |
| Aplica a | Esa marca o Todas las marcas excepto esa | Aparece cuando eliges Marca |
| Entidad financiera | Financiera a la que se limita el objetivo; sin selección no limita por financiera | No |
| Inicio del periodo / Fin del periodo | Fechas del período; fin igual o posterior al inicio | Sí |
| Objetivo en equipos | Entero de al menos 1 | Uno de los dos objetivos, o ambos |
| Objetivo en valor | Valor positivo en pesos | Uno de los dos objetivos, o ambos |
| Observaciones | Aclaraciones de la meta | No |

Los registros de sucursal, ciudad, trabajador, marca o financiera enviados al guardar deben estar activos. Un trabajador activo puede tener meta individual sin que su rol sea Vendedor. «Todas las marcas excepto esa» significa excluir una marca; no selecciona por sistema operativo ni restringe a celulares.

## Cómo interpretar el avance

La cantidad alcanzada cuenta ventas que aportan a la meta; el valor alcanzado suma su valor de venta después del descuento, sin agregar la intermediación ni su IVA. Se usa la fecha de registro de la venta y las dimensiones de la meta: período, alcance, marca y financiera cuando se definieron. Una venta anulada deja de aportar a su período original.

| Indicador | Cómo se calcula |
|---|---|
| Porcentaje | Alcanzado ÷ objetivo × 100, a dos decimales; puede superar 100 % |
| Falta | Objetivo menos alcanzado; si ya se alcanzó, muestra cero |
| Cumplida | Los porcentajes de los objetivos definidos, redondeados a dos decimales, llegan al 100 % o lo superan, aunque el período no haya terminado |
| En curso | No llega a todos los objetivos y el fin del período todavía no pasó; incluye metas futuras |
| No cumplida | El período terminó y no llegó a todos los objetivos |

La barra se llena hasta 100 %, pero el texto conserva el porcentaje superior a 100 %. Si definiste equipos y valor, cumplir uno no basta para que la meta diga **Cumplida**. No se muestra una barra para un objetivo que dejaste sin definir.

Ejemplo: con objetivo de 10 equipos y 12 alcanzados, el porcentaje es 120 % y faltan 0 equipos. Si también definiste un objetivo en valor cuyo porcentaje redondeado sigue por debajo de 100 %, la meta puede seguir **En curso**.

El cumplimiento usa esos porcentajes ya redondeados, mientras **Falta** usa la diferencia de cantidades o importes. Por ejemplo, con un único objetivo de $1.000.000 y $999.999 alcanzados, el porcentaje es 99,9999 % y se redondea a 100,00 %: aparece **Cumplida** y aún falta $1.

## Cómo editar, deshabilitar o activar

Para corregir la configuración:

1. Abre la ficha de la meta.
2. Haz clic en **Editar meta** (también puedes usar **Editar** en el listado).
3. Corrige los campos.
4. Haz clic en **Guardar**.

El diálogo se cierra y se actualiza la ficha o el listado. Corregir período, alcance u objetivos puede cambiar el avance calculado; no modifica las ventas.

Para dejar de usar una meta, haz clic en **Deshabilitar**, escribe el **Motivo** y confirma **Deshabilitar**. Para volver a usarla, haz clic en **Activar**, escribe el motivo y confirma **Activar**. Las acciones actualizan la consulta: una meta deshabilitada deja de estar disponible para los roles de sede y puede salir del listado según sus filtros. No hay acción de anulación de metas.

## Cómo imprimir una meta

1. Abre la ficha de la meta.
2. Haz clic en **Imprimir**.
3. Revisa **Informe de meta**.
4. Haz clic en **Imprimir** para abrir la impresión del navegador.

La hoja muestra nombre, alcance, período, avance y fecha de generación. Agrega el estado del registro cuando la meta está deshabilitada. Es una consulta del avance al generar la hoja; no congela la meta ni las ventas. Para impresión y guardado en PDF, consulta [Exportar e imprimir](../general/exportar-e-imprimir.md). Para comparar varias metas, usa [Informe de metas](../dashboard/informe-de-metas.md).

## Qué ve cada rol

| Rol | Metas que consulta e imprime | Gestiona |
|---|---|---|
| Super Administrador / Administrador | Metas de los alcances configurados, activas y deshabilitadas | Sí |
| Administrador de Punto | Activas de su sucursal e individuales de personas asignadas actualmente a su sucursal | No |
| Vendedor | Activas de su sucursal y sus propias metas individuales | No |
| Bodeguero con Consultar metas | Activas de su ubicación y sus propias metas individuales | No |

Las metas de empresa o ciudad y las de marca o financiera sin sucursal o trabajador de tu alcance no aparecen para los roles de sede. Un permiso extra de consulta no amplía ese alcance. El permiso **Crear, editar, deshabilitar y activar metas** está reservado a los roles administrativos; no se otorga como extra.

El avance muestra cantidad y valor vendido, no costo ni ganancia. **Creada por** se muestra al alcance global; los roles de sede reciben las fechas de creación y actualización sin ese dato.

## Relación con otros módulos

**Necesitas antes:**

- [Sucursales](../administracion/sucursales.md), [ciudades](../administracion/ciudades.md) o [usuarios](../administracion/usuarios.md): según el alcance que vayas a definir.
- [Marcas](../administracion/marcas.md) y [entidades financieras](../administracion/entidades-financieras.md): si limitas la meta por esas dimensiones.
- [Ventas](../ventas/ventas.md): sus registros alimentan el avance; editar una meta conserva esas ventas.
- Lecturas de apoyo, según la tarea que realices: [Exportar a Excel e imprimir](../general/exportar-e-imprimir.md); [Menú lateral y navegación](../general/menu-y-navegacion.md); [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md); [Cómo registrar una venta](../ventas/nueva-venta.md); [Cómo solicitar y resolver cambios de una venta](../ventas/solicitudes.md); [Cómo comparar metas en un informe](../dashboard/informe-de-metas.md); [Cómo consultar el tablero de ventas](../dashboard/tablero-de-ventas.md).

**Esto afecta a:**

- [Informe de metas](../dashboard/informe-de-metas.md): compara la configuración y el avance de las metas.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Define al menos un objetivo: en equipos o en valor.» | Dejaste ambos objetivos vacíos | Completa al menos uno |
| «Elige la sucursal del alcance.» | Elegiste Sucursal sin indicar cuál | Selecciona la sucursal |
| «Elige la ciudad del alcance.» | Elegiste Ciudad sin indicar cuál | Selecciona la ciudad |
| «Elige el trabajador del alcance.» | Elegiste Trabajador sin indicar quién | Selecciona la persona |
| «El fin del periodo no puede ser anterior al inicio; un solo día es un periodo válido (11.2).» | Las fechas están invertidas | Corrige el fin o el inicio |
| «El objetivo en equipos debe ser al menos 1 (11.3).» | La cantidad es cero o inválida | Usa un entero positivo |
| «El objetivo en valor debe ser mayor que cero (11.3).» | El valor no es positivo | Corrige el valor o déjalo vacío si usas equipos |
| «La marca está inactiva; la meta exige una marca activa (11.2).» | La marca elegida dejó de estar activa | Revisa el catálogo y elige una marca activa |

Si no encuentras una meta, revisa los filtros, su estado y tu alcance. Una meta deshabilitada o de otra sucursal puede no estar disponible para tu rol.

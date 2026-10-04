# Filtros guardados y filtros recordados

En los cuatro tableros puedes guardar una combinación de filtros con un nombre y volver a usarla cuando quieras, desde cualquier computador. Además, cada tablero **recuerda solo** los últimos filtros que usaste.

> **Quién puede hacerlo:** cualquier usuario que pueda abrir uno de los cuatro tableros. Los filtros guardados son **personales**: cada quien ve y borra solo los suyos.
> **Dónde está:** en el pie de la tarjeta de filtros de Dashboard e Informes → Ventas, Inventario, Metas y Financieras.

## Antes de empezar

- Solo existen en estas cuatro pantallas: **Tablero de ventas**, **Tablero de inventario**, **Informe de metas** e **Informe de financieras**. Las demás pantallas con filtros no los tienen. Para ver cómo se usan los filtros en general, mira [Listados, filtros y paginación](listados-filtros-y-paginacion.md).
- Hay **dos funciones distintas**:

  | | Filtros guardados | Filtros recordados |
  |---|---|---|
  | Quién los crea | Tú, a mano, con un nombre | El sistema, solos |
  | Cuántos | Hasta 20 por pantalla | Uno por pantalla |
  | Dónde viven | En el sistema: los ves desde cualquier equipo | En el navegador del equipo que usas |
  | Cómo los usas | Los eliges de una lista | Se aplican solos al entrar |

- Cada filtro guardado pertenece a **una pantalla**: uno de Ventas no aparece en Inventario.
- Un filtro guardado no se puede renombrar ni reemplazar. Solo se crea o se borra.

## Cómo guardar una combinación de filtros

1. En el tablero, pon los filtros que quieres guardar (periodo, sucursal, marca, etc.).
2. En el pie de la tarjeta de filtros, haz clic en **Guardar filtros**.
3. Se abre un panel a la derecha con el título «Guardar filtros» y el texto «Ponles un nombre a los filtros que tienes aplicados para volver a usarlos después.».
4. Escribe el **Nombre** (obligatorio, hasta 60 caracteres).
5. Haz clic en **Guardar**. Mientras se guarda, el botón dice «Guardando…».

Al terminar verás: el panel se cierra y el nombre queda en la lista **Filtros guardados**, ya seleccionado.

Puedes guardar «sin filtros» (todo vacío): es un filtro guardado válido.

### Si tus filtros tienen fechas fijas

Si en el tablero elegiste un rango de fechas con **Desde** y **Hasta**, el panel muestra este aviso: «Estos filtros tienen fechas fijas: este favorito va a mostrar siempre ese mismo rango. Si quieres que se mueva con el calendario, elige antes un periodo como «Mes anterior».» El aviso no te impide guardar.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Nombre | Un nombre que te diga qué filtros son (hasta 60 caracteres). No puede repetirse en la misma pantalla, sin importar mayúsculas o minúsculas. | Sí |

## Cómo usar un filtro guardado

1. Abre la lista **Filtros guardados** (está en el pie de la tarjeta de filtros).
2. Elige el nombre que quieres.

Al terminar verás: los filtros del tablero cambian a los del favorito y la lista muestra su nombre. Si usas el botón «atrás» del navegador, vuelves a los filtros que tenías antes.

La lista muestra el nombre del filtro guardado **solo mientras los filtros del tablero son exactamente los suyos**. Si cambias un filtro, la lista vuelve a decir «Filtros guardados».

Mensajes de la lista cuando no hay qué elegir (está apagada):

| Lo que ves | Qué significa |
|---|---|
| «Todavía no hay filtros guardados» | No has guardado ninguno en esta pantalla |
| «No se pudieron cargar los filtros guardados» | Falló la carga de la lista. Junto a ella aparece un botón con el icono de recargar («Volver a cargar los filtros guardados»). El resto del tablero sigue funcionando. |

## Cómo borrar un filtro guardado

1. Elige el filtro en la lista **Filtros guardados**. El botón aparece cuando los filtros actuales coinciden con ese favorito; también puede aparecer si la coincidencia se detecta automáticamente. Es el botón con el icono de papelera («Borrar el filtro guardado: …»).
2. Haz clic en la papelera.
3. Se abre la confirmación «Borrar "nombre"» con el texto «El filtro guardado se borra para siempre. Los filtros que tienes aplicados ahora no cambian.».
4. Haz clic en **Borrar** (o en **Cancelar**).

Al terminar verás: el nombre desaparece de la lista. Los filtros que tenías puestos en el tablero se quedan como estaban.

> **Importante:** este es el **único** lugar del sistema donde algo se borra de verdad y no se puede recuperar. En el resto del sistema se deshabilita o se anula: mira [Formularios y acciones comunes](formularios-y-acciones-comunes.md).

## Cómo funcionan los filtros recordados

- Cada vez que cambias los filtros de un tablero, el sistema los guarda **en el navegador del equipo**, para ti y para esa pantalla.
- Al volver a entrar a ese tablero, **si entras con una dirección sin parámetros**, el sistema vuelve a poner los últimos que usaste.
- Si entras con una dirección que ya trae filtros (por ejemplo un enlace que te pasaron), esos filtros mandan y no se cambian por los recordados.
- Si quitas todos los filtros a propósito, se respeta: no reaparecen solos.
- La **página** de resultados no se recuerda.
- Si tu navegador bloquea el almacenamiento, la función simplemente no hace nada; el tablero funciona igual.
- Son por usuario: si otra persona usa el mismo equipo con su propio usuario, ve los suyos.

## Qué pasa con filtros que ya no te corresponden

Al aplicar un filtro guardado o uno recordado, el sistema descarta sin avisar lo que hoy no puedes usar:

- Los filtros de **Sucursal, Ciudad o Vendedor** guardados cuando tenías un rol que ve todas las sucursales, si ahora tu rol ya no los ve.
- Los filtros que dependen de un permiso que ya no tienes.
- Un periodo o una agrupación que el sistema ya no ofrece.

Por eso a veces un filtro guardado muestra menos filtros de los que recuerdas.

## Qué ve cada rol

La tabla muestra el acceso **de base, antes de permisos extra**. Un Bodeguero con un permiso extra que abra un tablero puede guardar y usar sus filtros allí.

| Rol | Ve los tableros | Puede guardar y usar filtros | Observaciones |
|---|---|---|---|
| Super Administrador | Sí (los cuatro) | Sí | |
| Administrador | Sí (los cuatro) | Sí | |
| Administrador de Punto | Ventas, Inventario y Metas | Sí | No ve el Informe de financieras |
| Vendedor | Ventas y Metas | Sí | Sus filtros guardados son personales. En el [Tablero de ventas](../dashboard/tablero-de-ventas.md) ve sus propias ventas; en el [Informe de metas](../dashboard/informe-de-metas.md), las metas activas de su sucursal y sus individuales |
| Bodeguero | No tiene el módulo Dashboard | No aplica | El permiso existe, pero no hay tablero donde usarlo |

## Relación con otros módulos

**Necesitas antes:**
- Poder abrir el tablero: [Menú y navegación](menu-y-navegacion.md).
- Lecturas de apoyo, según la tarea que realices: [Listados: buscar, filtrar y pasar de página](listados-filtros-y-paginacion.md); [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md).

**Esto afecta a:**
- [Tablero de ventas](../dashboard/tablero-de-ventas.md), [Tablero de inventario](../dashboard/tablero-de-inventario.md), [Informe de metas](../dashboard/informe-de-metas.md) e [Informe de financieras](../dashboard/informe-de-financieras.md): cada uno explica sus propios filtros.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Ya tienes un filtro guardado con ese nombre en esta pantalla.» (bajo el campo Nombre) | Ya hay uno con ese nombre (sin distinguir mayúsculas) | Cambia el nombre |
| «Llegaste al máximo de 20 filtros guardados en esta pantalla. Borra alguno para poder guardar este.» (arriba del formulario) | Ya tienes 20 en esta pantalla | Borra alguno que no uses y vuelve a guardar |
| Un mensaje de error rojo dentro del panel | No se pudo guardar | Revisa tu conexión y vuelve a hacer clic en **Guardar**. Si cancelas, la lista se vuelve a cargar sola para mostrar si el filtro se alcanzó a guardar. |
| «Hiciste demasiadas solicitudes seguidas.» y cuánto esperar | Guardaste o listaste demasiado rápido (el límite por defecto es de 60 por minuto; el de tu instalación puede variar) | Espera y vuelve a intentar |
| El panel no se deja cerrar con Escape ni con la X | Se está guardando | Espera a que termine |

# Listados: buscar, filtrar y pasar de página

Casi todas las pantallas del sistema muestran una tabla con registros (ciudades, ventas, equipos, usuarios…). Muchas comparten el buscador, los filtros y el paginador que se explican aquí; las excepciones se indican en la página de cada módulo. Aquí se explica una sola vez; en las demás páginas solo se enlaza a esta.

> **Quién puede hacerlo:** todos los roles, en las pantallas que su usuario puede abrir.
> **Dónde está:** en cualquier pantalla con tabla, por ejemplo Administración → Ciudades o Ventas → Ventas.

## Antes de empezar

- Los listados paginados muestran **25 registros por página**. Es fijo y no se cambia. No todas las tablas son listados paginados: un documento o un resumen puede tener otra presentación.
- Lo que escribes en los filtros **se aplica al instante**, sin botón «Buscar».
- La página en la que estás, la búsqueda y los filtros quedan guardados en la **dirección de la página** (la barra de direcciones del navegador). Por eso puedes recargar con F5, usar los botones «atrás» y «adelante» del navegador o compartir la dirección con un compañero y ver lo mismo. Ojo: lo que tú ves depende de tu rol; dos personas con la misma dirección pueden ver resultados distintos.
- Los registros de negocio no se borran: se deshabilitan o se anulan; en los catálogos se activan o desactivan con un interruptor. La excepción son los [filtros guardados](filtros-guardados.md), que sí se borran. Mira [Formularios y acciones comunes](formularios-y-acciones-comunes.md).

## Cómo está armada una pantalla con listado

De arriba hacia abajo:

1. **Encabezado:** el título, una frase que explica para qué sirve y las acciones disponibles. En un catálogo, la acción principal (por ejemplo «Nueva ciudad») abre un diálogo. No es una regla para todos los listados: [Nueva venta](../ventas/nueva-venta.md) y [Crear traslado](../inventario/traslados.md) se abren en páginas propias; algunos encabezados también ofrecen exportar o imprimir.
2. **Buscador y/o tarjeta de filtros.**
3. **La tabla** con sus columnas.
4. **El pie de la tabla**, con cuántos registros hay y los botones para cambiar de página.

## Cómo buscar por texto

Las pantallas con buscador muestran una barra con dos partes:

1. A la izquierda, el botón **Filtro:** con el tipo de coincidencia (por defecto **Contiene**). Haz clic para elegir otro:

   | Opción | Qué hace |
   |---|---|
   | Contiene | Coincide en cualquier parte del texto |
   | Inicia por | Debe empezar con el término |
   | Es igual a | Coincidencia exacta y completa |
   | Termina en | Debe finalizar con el término |

2. A la derecha, el campo de texto (con una lupa). Escribe lo que buscas.

Al terminar verás: la tabla se actualiza sola cuando dejas de escribir un momento (un instante después de la última tecla). Si cambias el tipo de coincidencia, se aplica de inmediato.

Para borrar la búsqueda, haz clic en la **X** que aparece dentro del campo («Limpiar búsqueda»).

Cambiar el texto o el tipo de coincidencia te devuelve a la página 1.

## Cómo usar los filtros

Las pantallas más completas (Ventas, Equipos, los tableros) tienen una **tarjeta de filtros**:

1. Cada filtro tiene su **rótulo visible** arriba del campo (por ejemplo «Sucursal», «Desde», «Hasta»).
2. En las pantallas con muchos filtros, están agrupados en **secciones que se pliegan**: haz clic en el título de la sección para abrirla o cerrarla. La primera sección está abierta al entrar. Una sección cerrada se abre sola si aumenta el número de filtros aplicados en ella. Cambiar el valor de un filtro sin aumentar esa cuenta no la abre.
3. Al lado del título de cada sección ves, en gris, los filtros que contiene; y si hay filtros puestos en ella, cuántos («1 filtro aplicado»).
4. Elige o escribe el valor. La tabla cambia sola y vuelves a la página 1.
5. Las fechas se eligen con el selector de fecha del navegador: **Desde** y **Hasta**.

### El pie de la tarjeta de filtros

Abajo de la tarjeta hay una línea de resumen:

- «Mostrando **N** ventas · **N** filtros aplicados» (el sustantivo cambia según la pantalla), o «Sin filtros aplicados».
- Si hay al menos un filtro puesto, aparece el botón **Limpiar filtros**. Quita todos los filtros de esa pantalla a la vez. Cuando no hay ningún filtro, el botón no aparece.
- En algunas pantallas, en este mismo pie están los botones **Exportar Excel** e **Imprimir / PDF**, que actúan sobre todo lo que los filtros dejan, no solo sobre la página visible. Mira [Exportar e imprimir](exportar-e-imprimir.md).
- En los tableros, en este pie están también los [filtros guardados](filtros-guardados.md).

## Cómo cambiar de página

Abajo de la tabla está el paginador:

1. A la izquierda verás, por ejemplo, «Mostrando 26-50 de 156 resultados». Con un solo resultado dice «… 1 resultado»; sin ninguno, «Sin resultados».
2. A la derecha:
   - **Anterior** y **Siguiente** (flechas). «Anterior» está apagado en la página 1 y «Siguiente» en la última.
   - Los **números de página**. La actual está marcada. Si hay más de siete páginas, se muestran la primera, la última, la actual con sus vecinas y puntos suspensivos (…) en los huecos.
3. Haz clic en el número de página al que quieres ir.

Al cambiar de página, el cursor del teclado queda en la tabla, para que puedas seguir con el teclado.

## Estados de una pantalla con listado

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Cargando…» (o «Cargando ciudades…», según la pantalla) con un anillo | El sistema está trayendo los datos | Espera un momento |
| «Todavía no hay ciudades.» (el texto cambia según la pantalla) | No hay registros de este tipo | Crea el primero con la acción principal del encabezado, si tu rol puede |
| «Ninguna ciudad coincide con el filtro.» (el texto cambia según la pantalla) | Hay registros, pero ninguno cumple tu búsqueda o tus filtros | Cambia la búsqueda o usa **Limpiar filtros** |
| «No tienes permiso para ver esta información.» | Tu usuario no puede ver esos datos | Avisa a un administrador si los necesitas |
| «No se encontró el registro.» | El registro que intentaste abrir ya no existe o no es de tu alcance | Vuelve al listado |
| «Tu sesión expiró. Inicia sesión de nuevo.» | Se cerró tu sesión | Ingresa de nuevo: [Primeros pasos](primeros-pasos.md) |
| Otro mensaje con el botón **Reintentar** | La carga falló (por ejemplo, sin conexión) | Haz clic en **Reintentar** |

Cuando una pantalla tiene dos errores a la vez (por ejemplo, la tabla y un filtro), cada **Reintentar** reintenta solo lo suyo.

## Lo que cada rol ve en un listado

Los datos operativos se consultan dentro del alcance de quien los mira. La regla no se aplica de la misma manera a los catálogos de apoyo:

- **Super Administrador y Administrador** ven todas las sucursales (consolidado).
- **Administrador de Punto, Vendedor y Bodeguero** consultan datos operativos de su sucursal o ubicación asignada; algunas pantallas tienen recortes adicionales, como el tablero de ventas del Vendedor.
- En Equipos, el filtro **Sucursal** no se envía para un rol sin alcance global. Cada pantalla define qué filtros de alcance ofrece; no se puede extender esta regla a todos los filtros de todas las pantallas.
- Los catálogos de apoyo pueden incluir otras sedes: por ejemplo, la lista de sucursales sirve para elegir el destino de un traslado. Poder elegir una sede no te autoriza a consultar sus movimientos.

Revisa **Qué ve cada rol** en la página del módulo: allí se explica el alcance del listado que estás consultando.

## Qué ve cada rol

| Rol | Ve el listado | Observaciones |
|---|---|---|
| Super Administrador | Todas las sucursales | |
| Administrador | Todas las sucursales | |
| Administrador de Punto | Datos operativos de su sucursal | Las lecturas de apoyo tienen reglas propias |
| Vendedor | Datos operativos de su sucursal | En el listado de Ventas ve las ventas de su sucursal, incluidas las de sus compañeros. En el tablero de ventas ve solo las propias. Mira [Ventas](../ventas/ventas.md). |
| Bodeguero | Inventario de su ubicación | Puede leer catálogos de apoyo |

## Relación con otros módulos

**Necesitas antes:**
- Poder abrir la pantalla: [Menú y navegación](menu-y-navegacion.md).

**Esto afecta a:**
- [Formularios y acciones comunes](formularios-y-acciones-comunes.md): crear, editar y deshabilitar desde un listado.
- [Filtros guardados](filtros-guardados.md): guardar y reutilizar combinaciones de filtros en los tableros.
- [Exportar e imprimir](exportar-e-imprimir.md): bajar o imprimir lo que muestran los filtros.
- Cada módulo aplica esto a sus propias pantallas: por ejemplo [Ciudades](../administracion/ciudades.md), [Equipos](../inventario/equipos.md) y [Ventas](../ventas/ventas.md).

## Preguntas frecuentes

**¿Puedo cambiar cuántos registros veo por página?** En los listados paginados, no: son 25.

**¿Por qué la tabla de Equipos se desplaza dentro de su tarjeta?** La tabla de Equipos es ancha y larga; su encabezado queda fijo arriba y se desplaza dentro de la tarjeta, con barra horizontal.

**¿Y si la tabla no cabe en mi pantalla?** En pantallas angostas, la tabla se desplaza de lado dentro de su tarjeta.

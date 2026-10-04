# Precios y parámetros

Consulta las versiones de parámetros que usa el sistema para sugerir precios. Para fijar un precio específico por equipo, usa [la tabla de Equipos](equipos.md#cómo-ajustar-precios-de-uno-o-varios-equipos).

> **Quién puede hacerlo:** Super Administrador, Administrador, Administrador de Punto y Bodeguero consultan por su rol. Solo el Super Administrador crea versiones.
> **Dónde está:** menú lateral → Inventario → Parámetros de precios (`/inventario/parametros`).

## Antes de empezar

Los parámetros son versiones con fecha de vigencia. No se edita ni se elimina una versión anterior: para corregir un valor se crea otra versión.

Los precios sugeridos se calculan al consultar usando el costo, la ganancia del equipo y los parámetros vigentes. Los precios fijados a mano tienen prioridad sobre el sugerido correspondiente. La ganancia por defecto propone la ganancia al registrar un ingreso que no la traiga; no reemplaza la ganancia ya definida de cada equipo.

## Cómo consultar las versiones

1. Abre **Parámetros de precios**.
2. Revisa **Vigente desde**, **Recargo de crédito**, **Descuento de contado** y **Ganancia por defecto**.
3. Consulta **Creado por** y **Registrada el** para identificar quién publicó la versión y cuándo.
4. Busca la insignia **Vigente**. Una versión con fecha futura no es necesariamente la que se usa hoy, aunque aparezca primero.

El cálculo usa la versión con fecha de vigencia más reciente que no sea posterior a hoy; con la misma vigencia, gana la registrada después. El historial muestra las versiones, pero no ofrece una acción de editar ni una ficha con sus notas.

La etiqueta **Vigente** usa la fecha del dispositivo. Los precios se calculan con la fecha configurada para el sistema (Bogotá por defecto). Cerca de medianoche, si tu dispositivo usa otra zona horaria, la etiqueta puede señalar otra versión.

## Cómo crear una versión

Solo el Super Administrador tiene **Crear parámetros de precio**; este permiso no se puede otorgar como extra.

1. Pulsa **Nueva versión**.
2. En **Nueva versión de parámetros**, completa los cuatro campos obligatorios.
3. Si lo necesitas, escribe **Notas** para explicar el cambio.
4. Revisa fecha e importes antes de pulsar **Guardar**. Mientras se envía dice **Guardando…**.

Al guardar correctamente se cierra el formulario y se recarga el historial. La nueva fila aparece allí; no se abre una ficha ni se garantiza que quede marcada Vigente si su fecha es futura. **Cancelar** cierra sin guardar.

Para corregir una versión, crea otra con los valores completos que deban aplicar. Una corrección con la misma fecha de vigencia puede desplazar a la anterior porque fue registrada después.

### Qué significa cada campo

| Campo | Qué poner | ¿Obligatorio? |
|---|---|---|
| Vigente desde | Fecha a partir de la cual puede aplicar la versión. | Sí. |
| Recargo de crédito | Fracción entre cero y menos de uno, hasta cuatro decimales: `0.0300` significa 3 %. No escribas `3` ni el signo %. | Sí. |
| Descuento de contado | Monto en pesos que se resta del Crédito efectivo para sugerir Contado. Cero o más, hasta dos decimales. | Sí. |
| Ganancia por defecto | Ganancia propuesta cuando el ingreso no incluye la del equipo. Cero o más, hasta dos decimales. | Sí. |
| Notas | Explicación del cambio. | No. |

Descuento y Ganancia por defecto admiten hasta 12 dígitos en total, incluidos sus dos decimales. Escribe números sin símbolo de moneda ni separadores de miles, y usa punto para decimales. El formulario envía los textos tal como los escribes.

El 3 % es un ejemplo de formato, no una afirmación sobre el parámetro vigente de tu negocio. Consulta tu historial para conocer los valores que aplican.

## Cómo se calculan los precios

El cálculo usa pesos colombianos y redondea al peso entero; medio peso redondea hacia arriba en valores positivos.

- **Crédito sugerido** = (Costo + Ganancia del equipo) ÷ (1 − Recargo de crédito), redondeado al peso.
- **Crédito efectivo** = precio fijado a mano, si existe; de lo contrario, Crédito sugerido.
- **Contado sugerido** = Crédito efectivo − Descuento de contado, redondeado al peso.
- **Contado efectivo** = precio de Contado fijado a mano, si existe; de lo contrario, Contado sugerido.

Si fijas Crédito a mano pero dejas Contado en sugerido, el descuento se resta de ese Crédito manual, no del Crédito sugerido original. Cambiar los parámetros puede cambiar los sugeridos sin reescribir cada equipo. Los importes manuales se conservan, aunque el Contado sugerido puede variar si depende de un Crédito que no es manual.

Si cambias la ganancia del equipo a un valor distinto, sus dos precios manuales se quitan. En un mismo lote de edición puedes además fijarlos expresamente de nuevo. Cambiar solo el costo no quita los precios manuales.

El cálculo no pone un piso de cero al Contado sugerido: un descuento mayor que Crédito puede producir un valor negativo. No interpretes ese resultado como autorización para registrar una venta con valores inconsistentes; revisa los parámetros y el equipo antes de vender.

## Qué ve cada rol

| Rol | Consulta parámetros por su rol | Crea versiones |
|---|---|---|
| Super Administrador | Sí | Sí |
| Administrador | Sí | No |
| Administrador de Punto | Sí | No |
| Vendedor | No | No |
| Bodeguero | Sí | No |

Un Vendedor puede consultar con el permiso extra **Consultar parámetros de precio**, que exige también **Ver costo y ganancia**. Las versiones de parámetros son una configuración compartida; no son versiones separadas por sucursal. Conceder consulta no permite publicar cambios.

## Relación con otros módulos

**Necesitas antes:**

- [Roles y permisos](../general/roles-y-permisos.md) y [permisos extra](../administracion/usuario-detalle-y-permisos.md#lista-completa-de-permisos-extra): determinan consulta y publicación.
- Lecturas de apoyo, según la tarea que realices: [Ficha del equipo](equipo-detalle.md).

**Esto afecta a:**

- [Equipos](equipos.md): muestra y permite revisar los precios de cada unidad.
- [Ficha del equipo](equipo-detalle.md): permite corregir costo y ganancia.
- [Ingresos](ingresos.md): usa la ganancia por defecto cuando no se indica una propia.
- [Nueva venta](../ventas/nueva-venta.md): consulta los precios efectivos del equipo.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Todavía no hay versiones de parámetros.» | El historial está vacío. | Pide al Super Administrador que revise la configuración antes de usar precios sugeridos. |
| No aparece Nueva versión | No tienes el permiso reservado de creación. | Consulta el historial; la publicación corresponde al Super Administrador. |
| «Para guardar hacen falta la vigencia, el recargo de crédito, el descuento de contado y la ganancia por defecto.» | Hay un campo obligatorio vacío. | Completa los cuatro; cero es un valor válido en los campos monetarios. |
| «El porcentaje adicional debe ser menor que 1 (100 %): con 1 el valor de venta a crédito sería infinito.» | El recargo es uno o más. | Escríbelo como fracción menor que uno. |
| «El servidor todavía pide dos tasas que ya no se usan: la versión se podrá guardar cuando el servidor se actualice.» | La aplicación detectó un servidor anterior que exige campos retirados. | Reporta el desfase de versión; no inventes esas tasas ni repitas el envío. |

Si falla la carga, usa **Reintentar**. Los errores de un campo aparecen junto a él; consulta [Qué pasa si hay errores](../general/formularios-y-acciones-comunes.md#qué-pasa-si-hay-errores) para problemas de conexión o sesión.

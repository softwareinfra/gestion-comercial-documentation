# Cómo consultar y publicar el texto de aceptación

Consulta el texto de aceptación y habeas data que se conserva en las nuevas ventas y se imprime en su comprobante. Para cambiarlo se publica una versión nueva.

> **Quién puede hacerlo:** Super Administrador y Administrador consultan; solo el Super Administrador publica. Otros roles consultan con «Consultar el texto de aceptación» efectivo.
> **Dónde está:** menú lateral → Ventas → **Texto de aceptación**.

## Antes de empezar

La venta conserva el texto vigente cuando se registra. Publicar otro texto no reemplaza el de las ventas anteriores. Si no existe una versión vigente, el registro de una venta conserva un texto vacío; no se inventa uno al imprimirla.

## Cómo consultar el texto y sus versiones

1. Entra a **Texto de aceptación**.
2. Revisa **Vigente**: muestra **Vigente desde** y el **Texto** completo con sus saltos de línea.
3. Si aparece **Sin texto vigente**, revisa si existen únicamente versiones futuras o si falta publicarlo.
4. Revisa **Historial de versiones**, con **Vigente desde**, **Creada** e **Inicio del texto**.

El historial muestra el inicio del texto; al pasar el cursor sobre esa celda puedes consultar el texto completo que contiene. La versión vigente también se muestra completa arriba. Las versiones anteriores no tienen acción de edición ni borrado.

La etiqueta **Vigente** usa la fecha del dispositivo; la venta toma el texto según la fecha del negocio. Cerca de medianoche, un dispositivo en otra zona horaria puede señalar otra versión.

## Cómo publicar una versión

1. Haz clic en **Nueva versión**.
2. Escribe el contenido en **Texto**.
3. Elige **Vigente desde**.
4. Haz clic en **Publicar**.

Ambos campos son obligatorios. Un texto que contenga únicamente espacios no permite continuar. La fecha abre con hoy del dispositivo. Mientras se guarda aparece **Publicando…** y el diálogo no se puede cerrar.

Al terminar se cierra el diálogo y se recarga la configuración. Con fecha futura queda programado para esa vigencia; el texto anterior continúa aplicando mientras corresponda. Corregir un texto publicado consiste en publicar otra versión.

## Qué ve cada rol

| Rol | Consulta esta pantalla | Publica |
|---|---|---|
| Super Administrador | Sí | Sí |
| Administrador | Sí | No |
| Administrador de Punto / Vendedor / Bodeguero | Con «Consultar el texto de aceptación» efectivo | No |

El permiso **Registrar ventas** permite imprimir el texto que ya tiene una venta dentro de su comprobante. Esa acción no da acceso por sí misma a esta configuración. Publicar textos es reservado al Super Administrador.

## Relación con otros módulos

**Necesitas antes:**
- Un usuario autorizado según [Roles y permisos](../general/roles-y-permisos.md).
- Lecturas de apoyo, según la tarea que realices: [Detalle de un usuario y sus permisos](../administracion/usuario-detalle-y-permisos.md).

**Esto afecta a:**
- [Nueva venta](nueva-venta.md): conserva el texto vigente al registrar.
- [Comprobante de venta](comprobante-de-venta.md): imprime el texto guardado en esa venta, incluso si luego se publicaron otras versiones.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «Escribe el texto y la fecha desde la que rige antes de publicar.» | Falta texto o fecha. | Completa ambos; no uses únicamente espacios. |
| «Sin texto vigente» | No hay una versión que aplique según la fecha usada por la pantalla. | Revisa las fechas del historial y la fecha del dispositivo. |
| No aparece Nueva versión | Tu permiso permite consultar, no publicar. | Solicita la publicación al Super Administrador. |

Si la venta ya se registró sin texto, publicar uno hoy no añade texto a esa venta anterior. Si el envío falló sin confirmación, revisa el historial antes de repetir **Publicar**.

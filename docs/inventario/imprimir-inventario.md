# Imprimir inventario

Prepara una hoja con los equipos que coinciden con los filtros de Equipos. Desde ella abres la impresión del navegador y, si ofrece esa opción, puedes guardarla como PDF.

> **Quién puede hacerlo:** los cinco roles con **Exportar e imprimir el inventario**.
> **Dónde está:** Inventario → Equipos → Imprimir / PDF (`/inventario/equipos/imprimir`).

## Antes de empezar

La hoja consulta los equipos guardados de tu alcance; no se limita a la página visible y admite hasta **5.000 filas**. Ajusta los filtros en Equipos antes de abrirla. Si necesitas más filas, usa **Exportar Excel**, con límite de 20.000.

Si la tabla tiene precios sin guardar, **Imprimir / PDF** pide confirmación. **Abrir la hoja** continúa sin guardar esos precios y los descarta al salir del listado. Para imprimirlos, cancela y guarda el lote primero.

## Cómo imprimir o guardar como PDF

1. En [Equipos](equipos.md#cómo-consultar-y-filtrar), selecciona los filtros que necesitas.
2. Con resultados, pulsa **Imprimir / PDF**. La hoja se abre en la misma pestaña con esos filtros.
3. Comprueba la cabecera: **Alcance**, **Fecha**, **Filtros**, **Equipos** y **Generado el**.
4. Espera a que estén listos los equipos y los nombres de los filtros. Mientras se resuelven puede aparecer **«Preparando los nombres de los filtros…»**.
5. Pulsa **Imprimir**. Abre el diálogo de impresión del navegador.
6. Elige la impresora y confirma allí. Si el navegador ofrece un destino para guardar PDF, selecciónalo y guarda el archivo.
7. Usa **Volver a Equipos** para regresar con los mismos filtros.

El sistema arma una hoja imprimible; no descarga automáticamente un PDF generado por el servidor. El nombre del destino PDF y los ajustes de papel pertenecen al navegador, no a esta pantalla.

## Qué contiene la hoja

La tabla incluye **Nº interno**, **IMEI**, **Equipo** (marca y referencia, con RAM, almacenamiento y color cuando existen), **Categoría**, **Ubicación**, **Estado**, **Días**, **Crédito** y **Contado**. Con acceso al costo se agregan **Costo** y **Ganancia**.

No incluye la columna de proveedor ni todos los campos del Excel. Crédito y Contado son precios efectivos guardados o calculados, sin las etiquetas «a mano» de la tabla editable. Los equipos vendidos también pueden aparecer si los filtros los incluyen.

## Qué ve cada rol

| Rol | Alcance | Costo y ganancia por su rol |
|---|---|---|
| Super Administrador | Global, recortado por filtros | Sí |
| Administrador | Global, recortado por filtros | Sí |
| Administrador de Punto | Su sede, recortada por filtros | Sí |
| Vendedor | Su sede, recortada por filtros | No |
| Bodeguero | Su sede, recortada por filtros | Sí |

Los cinco roles tienen exportación e impresión de base. **Ver costo y ganancia** puede ampliar las columnas para un usuario con ese extra; el permiso de exportar no las abre por sí solo. El alcance de sede no se convierte en global mediante extras.

## Relación con otros módulos

**Necesitas antes:**

- [Equipos](equipos.md): selecciona los filtros y guarda los precios antes de imprimir.
- Lecturas de apoyo, según la tarea que realices: [Exportar a Excel e imprimir](../general/exportar-e-imprimir.md).

**Esto afecta a:**

- El documento que imprimes o guardas desde el navegador. Consultar esta hoja no modifica los equipos.

## Si algo sale mal

| Lo que ves | Qué significa | Qué hacer |
|---|---|---|
| «La vista para imprimir tiene N filas y el tope es 5000. Acota los filtros o usa Exportar Excel.» | El resultado supera el límite. | Vuelve a Equipos y reduce el conjunto o descarga Excel; reintentar igual no reduce las filas. |
| «Ningún equipo coincide con los filtros.» | La consulta de la hoja no encontró resultados. | Vuelve a Equipos y revisa filtros y alcance. |
| Un aviso de carga de nombres con Reintentar | No se pudieron resolver los nombres de los filtros. | Pulsa Reintentar y espera antes de imprimir. |
| Imprimir no está disponible mientras prepara nombres | La hoja aún no está lista. | Espera a que termine la consulta; revisa el aviso si falla. |

Para errores de conexión o sesión, consulta [Qué pasa si hay errores](../general/formularios-y-acciones-comunes.md#qué-pasa-si-hay-errores). El número N del aviso depende del resultado, no es una cifra fija.

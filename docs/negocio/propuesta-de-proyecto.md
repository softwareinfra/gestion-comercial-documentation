## PROPUESTA DE PROYECTO

SISTEMA DE GESTIÓN COMERCIAL, INVENTARIO, GARANTÍAS, FINANCIACIÓN Y TESORERÍA

Propuesta Técnica y Comercial

Propósito del Documento:

Definir con precisión qué funcionalidades se construirán, cuáles serán opcionales, cuáles no estarán incluidas y qué aspectos

siguen pendientes de validación.

Enfoque de la aplicación:

Aplicación web optimizada para computador, con acceso desde

tablet y celular.


## INTRODUCCIÓN

El presente documento establece formalmente el Alcance Funcional del Sistema de Gestión Comercial, Inventario, Garantías, Financiación y Tesorería. Su principal objetivo es consolidar en un marco técnico y operativo unificado todas las especificaciones, requerimientos, reglas de negocio y restricciones que guiarán el diseño y desarrollo de la plataforma tecnológica comercial.

A través de esta especificación se busca transformar el modelo operativo actual —basado en procesos manuales y hojas de cálculo independientes— hacia una arquitectura centralizada, escalable y segura. Esta transición permitirá modernizar la gestión de múltiples puntos de venta y bodegas, garantizando el control riguroso de dispositivos mediante código IMEI, la trazabilidad de garantías, la integración de alianzas financieras y la consolidación gerencial en tiempo real.

Marco de Referencia Acordado: Este documento servirá como la guía oficial para la fase de construcción de la aplicación web, delimitando de manera transparente las funcionalidades base incluidas, los componentes opcionales cotizables, las restricciones de alcance y las validaciones pendientes.

## 1. ANTECEDENTES

La empresa administra actualmente la información de inventario, ventas, clientes, financiación, metas, movimientos de dinero y reportes mediante archivos de Excel y documentos diligenciados manualmente.

El crecimiento exponencial de la operación en los últimos meses ha generado múltiples dificultades operativas y administrativas de alto impacto, entre las que se destacan de manera prioritaria:

- Duplicidad e inconsistencia de información: Incongruencias frecuentes entre los reportes emitidos por cada tienda y la consolidación central realizada en la sede principal.

- Errores de digitación: Fallas humanas recurrentes en el registro manual de códigos IMEI, valores de venta, nombres de clientes y datos de identificación.

- Dificultad para consultar el inventario disponible por punto: Imposibilidad de verificar existencias en tiempo real de otras sucursales ante una solicitud inmediata de compra.

- Falta de trazabilidad sobre ventas, traslados, garantías, devoluciones y movimientos de dinero: Ausencia de un registro histórico centralizado sobre los cambios de estado y ubicación de los equipos.

- Dependencia de una persona para actualizar los archivos: Cuellos de botella operativos por centralizar la consolidación de planillas en un único usuario administrativo.

- Dificultad para consolidar la información de diferentes sucursales: Procesos manuales lentos que toman días para entregar cifras consolidadas al cierre de mes.

- Riesgo de pérdida o deterioro de documentos físicos: Almacenamiento manual vulnerable a extravíos, daños o fallas en la búsqueda posterior de garantías.

- Dificultad para hacer seguimiento al cumplimiento de metas: Visibilidad limitada del avance diario de ventas en relación con los presupuestos individuales y corporativos.

- Dificultad para proyectar los pagos de las entidades financieras: Falta de un sistema automatizado que calcule fechas de corte y pagos esperados de plataformas aliadas.

La operación cuenta actualmente con aproximadamente 10 tiendas y tiene una proyección de crecimiento hasta cerca de 50 puntos de venta. El volumen actual es cercano a 350 ventas mensuales, con una proyección aproximada de 700 a 1.000 ventas por mes.


## 2. OBJETIVO DEL DESARROLLO

Implementar una aplicación web que centralice y organice la operación de la empresa, con acceso autenticado y controlado por roles, permitiendo gestionar:

- Dashboard e informes gerenciales.

- Inventario de equipos.

- Traslados de mercancía entre sucursales, puntos de venta y bodegas.

- Registro de ventas.

- Ingresos, egresos y movimientos de caja asociados con ventas.

- Formatos imprimibles por cada venta.

- Garantías y devoluciones asociadas con fallas de equipos.

- Metas comerciales.

- Administración de usuarios, sucursales, bodegas, proveedores y entidades financieras.

- Proyección de pagos de las entidades financieras.

- Exportación y archivado de información.

La solución deberá permitir que cada sucursal opere de manera independiente, pero que los administradores puedan consultar la información consolidada de toda la empresa.

## 3. ALCANCE GENERAL DE LA APLICACIÓN

La aplicación incluirá los siguientes módulos principales:

- 1. Dashboard e Informes.

- 2. Inventario.

- 3. Ventas.

- 4. Garantías y Devoluciones.

- 5. Metas Comerciales.

- 6. Administración.

La nueva estructura reemplaza los módulos independientes de:

- Entidades Financieras.

- Usuarios.

- Sucursales, Puntos de Venta y Bodegas.

- Caja y movimientos de dinero.

Las funcionalidades de entidades financieras, usuarios, sucursales, puntos de venta, bodegas y proveedores se gestionarán desde el módulo de Administración.

Las funcionalidades de caja y movimientos de dinero se integrarán dentro del módulo de Ventas, debido a que los ingresos, medios de pago, consignaciones y movimientos relacionados nacen principalmente de las operaciones comerciales.

También se manejarán catálogos administrativos para:

- Marcas.

- Tipos de producto.

- Referencias o modelos.


- Medios de pago.

- Categorías de movimientos.

- Estados requeridos para la operación.

## 4. CLASIFICACIÓN DEL ALCANCE

Las funcionalidades se clasifican de la siguiente manera:

| Clasificación | Significado |
| --- | --- |
| Incluido en el alcance base | Se desarrollará como parte de la fase acordada. |
| Opcional cotizable | Es técnicamente viable, pero requiere tiempo, costo o infraestructura adicional. |
| Pendiente de definición | El requerimiento existe, pero faltan datos o reglas para poder estimarlo y construirlo correctamente. |
| No incluido | No se desarrollará en esta fase. Podrá evaluarse posteriormente mediante una solicitud de cambio. |

## 5. COMPATIBILIDAD CON DISPOSITIVOS

## 5.1 Alcance incluido

La aplicación será web y podrá abrirse desde:

- Computadores de escritorio.

- Computadores portátiles.

- Tablets.

- Celulares.

El diseño será desktop first, lo que significa que la experiencia principal estará optimizada para pantallas de computador.

En tablet y celular:

- Se podrá iniciar sesión.

- Se podrán consultar los módulos autorizados.

- Se podrán registrar operaciones básicas.

- Los formularios se adaptarán de manera básica al ancho de la pantalla.

- Las tablas amplias podrán requerir desplazamiento horizontal.

- Algunos reportes y dashboards se visualizarán mejor desde computador.

- La impresión de documentos estará orientada principalmente al uso desde computador.

## 5.2 Limitaciones aceptadas

La solución no garantiza:

- Una experiencia móvil equivalente a una aplicación nativa.

- Una reorganización especializada de todos los dashboards para celular.

- Uso cómodo de tablas con muchas columnas en pantallas pequeñas.


- Funcionalidades sin conexión a Internet.

- Instalación como aplicación móvil desde App Store o Play Store.

## 5.3 Criterio de aceptación

La aplicación deberá ser accesible desde celular y tablet, pero el criterio principal de diseño, pruebas y aceptación será la visualización desde computador.

## 6. PRINCIPIOS GENERALES DEL SISTEMA

## 6.1 Operación multipunto

Cada sucursal deberá funcionar como una unidad independiente para:

- Inventario.

- Ventas.

- Garantías y devoluciones.

- Caja y movimientos de dinero asociados con ventas.

- Metas.

- Usuarios asignados.

- Reportes.

Los administradores podrán consultar:

- Una sucursal específica.

- Una ciudad.

- Varias sucursales.

- La operación consolidada de toda la empresa.

## 6.2 Sucursales, puntos de venta y bodegas

Las sucursales, puntos de venta y bodegas serán administrados desde un mismo módulo. Cada ubicación podrá configurarse como:

- Punto de venta.

- Bodega.

- Punto de venta y bodega.

Una ubicación configurada únicamente como bodega podrá recibir, almacenar y trasladar equipos, pero no registrar ventas.

## 6.3 Eliminación de información

No se incluirá una opción de eliminación directa para los registros operativos principales. Las acciones permitidas serán:

- Crear.

- Consultar.

- Editar cuando corresponda.

- Deshabilitar.

- Anular.


- Archivar.

Las ventas, garantías, traslados, movimientos de caja, equipos, usuarios y sucursales con historial no se eliminarán directamente desde la interfaz.

## 6.4 Trazabilidad

Cada operación importante deberá registrar:

- Fecha y hora.

- Usuario que realizó la acción.

- Sucursal desde la cual se realizó.

- Tipo de operación.

- Información anterior.

- Información nueva.

- Estado.

- Motivo u observación.

- Usuario que aprobó, cuando corresponda.

## 6.5 Administración independiente

Los administradores de la empresa deberán poder gestionar la operación sin depender del desarrollador para tareas normales como:

- Crear usuarios desde Administración.

- Crear sucursales, puntos de venta y bodegas desde Administración.

- Crear proveedores desde Administración.

- Crear entidades financieras desde Administración.

- Crear marcas y referencias.

- Configurar metas.

- Habilitar o deshabilitar registros.

- Asignar vendedores a sucursales.

## 6.6 Acceso al sistema e inicio de sesión

El inicio de sesión será la puerta de acceso a todas las funcionalidades del sistema, aunque no se manejará como un módulo independiente. Cada colaborador autorizado tendrá:

- Un nombre de usuario.

- Una contraseña.

- Un rol.

- Una sucursal asignada, cuando corresponda.

- Un estado activo o deshabilitado.

## Generación del nombre de usuario

El nombre de usuario se generará mediante la combinación de al menos uno de los nombres y uno de los apellidos del colaborador. Se aplicará una regla uniforme para todos los usuarios. Cuando una combinación ya exista, el sistema deberá generar una variación que permita conservar la unicidad del usuario.


## Reglas de acceso

- Solo los usuarios activos podrán iniciar sesión.

- La contraseña será obligatoria.

- El sistema mostrará únicamente los módulos y acciones autorizados para el rol.

- Los usuarios deshabilitados o anulados no podrán ingresar.

- El inicio de sesión y el cierre de sesión quedarán registrados para auditoría.

- El nombre de usuario no podrá repetirse.

- La administración de credenciales estará disponible únicamente para roles administrativos autorizados.

## 7. MÓDULO DASHBOARD E INFORMES

## 7.1 Objetivo

Presentar información visual y consolidada sobre ventas, inventario, metas, financiación y movimientos de caja.

## 7.2 Vistas incluidas

- Vista general de toda la empresa.

- Vista por ciudad.

- Vista por sucursal o punto de venta.

- Vista por vendedor, cuando el rol tenga autorización.

- Vista por entidad financiera.

- Vista por periodo.

## 7.3 Filtros incluidos

- Día, Semana, Mes, Trimestre, Año, Rango personalizado.

- Sucursal, Ciudad, Vendedor.

- Marca, Tipo de producto, Referencia, Categoría del equipo.

- Entidad financiera, Modalidad de venta, Medio de pago.

## 7.4 Indicadores de ventas

- Ventas del día, semana, mes y año.

- Total vendido, Unidades vendidas, Costo total, Ganancia, Margen, Ticket promedio.

- Ventas por día, sucursal, ciudad, vendedor y entidad financiera.

- Ventas de contado, ventas financiadas, ventas de cartera propia.

- Participación de cada punto en las ventas generales, Ranking de sucursales.

- Equipos más vendidos, Marcas más vendidas, Referencias más vendidas.

## 7.5 Indicadores de inventario

- Unidades disponibles y valor total del inventario.

- Unidades y valor por sucursal y por ciudad.

- Equipos vendidos, equipos en garantía, equipos en traslado.

- Equipos con mayor rotación, equipos con baja rotación.


- Días promedio en inventario, valor del inventario inmovilizado.

- Referencias con mayor cantidad en stock, alertas por permanencia prolongada.

## 7.6 Indicadores de metas

- Meta general por sucursal y por ciudad.

- Meta de Android, Meta de Apple o iPhone.

- Meta por entidad financiera, Meta por ciudad y entidad financiera.

- Valor objetivo, Valor alcanzado, Unidades objetivo, Unidades alcanzadas.

- Porcentaje de cumplimiento, Faltante, Estado de cumplimiento.

## 7.7 Indicadores de financieras

- Ventas financiadas por entidad y valor financiado por entidad.

- Cantidad de créditos, Valor esperado de pago.

- Fecha de corte, Fecha estimada de pago.

- Información diaria, semanal y mensual. Detalle por sucursal y ciudad.

## 7.8 Impresión y exportación

Todos los informes definidos deberán permitir:

- Imprimir desde el navegador.

- Guardar como PDF utilizando las capacidades del navegador.

- Mantener los filtros aplicados.

- Mostrar el periodo consultado, la sucursal o vista general, y la fecha y hora de generación.

La solución no almacenará automáticamente cada PDF generado. El sistema dará formato a la información y permitirá imprimirla o guardarla localmente.

## 7.9 Reglas de acceso

- El administrador podrá consultar toda la empresa.

- El administrador de punto podrá consultar su sucursal.

- El vendedor podrá consultar únicamente la información autorizada.

- Los vendedores no podrán consultar el inventario completo de todas las sucursales.

- Los indicadores de costo y ganancia podrán ocultarse para determinados roles.

## 7.10 Pendiente de validación

El cliente deberá aprobar: Orden definitivo de los indicadores, Gráficos exactos, Fórmulas definitivas, Indicadores visibles para cada rol, Diseño final de la vista general y vista por punto.

## 8. MÓDULO DE INVENTARIO

## 8.1 Objetivo

Registrar y controlar todos los equipos adquiridos, su ubicación, estado, costo, proveedor, movimiento y valores calculados de venta dentro de la empresa.


## 8.2 Campos del inventario

Identificación y ubicación: Número interno, Sucursal/agencia/punto de venta/bodega, IMEI, Estado del equipo.

Información de compra: Proveedor o distribuidor, Número de factura del proveedor, Número de guía, Fecha de pedido, Fecha de ingreso, Costo. (El número de guía y la fecha de pedido estarán disponibles, pero podrán ser opcionales durante el registro).

Clasificación del producto: Tipo de producto, Marca, Referencia o modelo, Categoría, RAM, Capacidad de almacenamiento, Color, Porcentaje de batería (cuando aplique).

Tipos de producto iniciales: Celular Android, iPhone, Tablet, Computador, Smartwatch, Accesorio tecnológico definido posteriormente. El sistema deberá permitir crear nuevos tipos de producto sin requerir intervención del desarrollador.

Categorías iniciales: Nuevo, Exhibición. La categoría de exhibición aplicará principalmente a equipos Apple, pero quedará disponible según las reglas autorizadas.

Batería: El porcentaje de batería será obligatorio para iPhone de exhibición, opcional para iPhone nuevo, no obligatorio para Android y podrá dejarse vacío para productos que no lo requieran.

## 8.3 Campos calculados o automáticos

Entrada de inventario, Existencia, Salida de inventario, Fecha de salida, Ubicación actual, Días en inventario, Estado de disponibilidad, Valor sugerido de venta a crédito, Valor sugerido de venta de contado, Comisión aplicable para ADDI, IVA sobre la comisión de ADDI, Valor total para registrar en ADDI. Estos datos deberán ser calculados o actualizados por el sistema y no depender de fórmulas manuales de Excel.

## 8.4 Estados iniciales

Disponible, Reservado, Vendido, En traslado, En garantía, Devuelto por garantía, Dado de baja por nota crédito, Inactivo.

## 8.5 Consulta y filtros

IMEI, Sucursal, Ciudad, Bodega, Proveedor, Número de factura, Marca, Tipo de producto, Referencia, Categoría, Estado, Fecha de ingreso, Rango de costo, Tiempo en inventario.

## 8.6 Visibilidad del inventario

- El administrador podrá consultar el inventario general.

- El administrador de punto podrá consultar el inventario de su sucursal.

- El vendedor podrá consultar únicamente el inventario de la sucursal asignada (no podrá ver el de otros puntos).

- Los traslados entre puntos deberán ser gestionados o autorizados por usuarios con permisos administrativos.

## 8.7 Ingreso de inventario

El sistema permitirá: Seleccionar proveedor, Seleccionar sucursal o bodega, Registrar datos comunes de la factura, Registrar uno o varios equipos, Validar IMEI duplicados, Guardar el movimiento y Generar un resumen imprimible del ingreso.

## 8.8 Traslados

Se permitirán traslados: Entre sucursales, Entre bodegas, De bodega a punto de venta, De punto de venta a bodega, Entre puntos de venta. Cada movimiento de mercancía deberá quedar identificado de forma única y trazable.


El traslado incluirá: Código o número único de traslado, Fecha y hora de creación, despacho y recepción, Ubicación de origen y destino, Tipo de ubicación de origen y destino, Equipos seleccionados, IMEI de cada equipo, Usuario que crea, despacha y recibe, Motivo, Observaciones, Estado del traslado, Documento soporte asociado.

Los estados iniciales del traslado serán: Creado, Pendiente de despacho, Despachado, En tránsito, Recibido, Rechazado, Anulado.

## 8.9 Documento imprimible

El ingreso o traslado podrá generar un documento con: Número de movimiento, Fecha, Origen, Destino, Usuario, Cantidad de equipos, IMEI, Marca, Referencia, Observaciones y Espacios para firma.

## 8.10 Reglas de negocio

- El IMEI deberá ser único.

- Un equipo vendido no podrá venderse nuevamente.

- Un equipo en traslado no podrá venderse.

- Un equipo en garantía no estará disponible para la venta.

- Cada equipo tendrá una sola ubicación actual.

- Un traslado confirmado no podrá eliminarse.

- Un equipo dado de baja deberá conservar su historial.

- La modificación del costo deberá limitarse a roles autorizados.

## 8.11 Cálculo de valores de venta

A partir del costo del equipo, el sistema deberá calcular los valores sugeridos para venta a crédito, venta de contado y venta mediante ADDI.

## 8.11.1 Datos de configuración

Costo del equipo, Valor definido para la ganancia de la venta a crédito, Porcentaje adicional utilizado en la configuración actual (inicialmente 3%), Diferencia entre valor de crédito y contado (inicialmente 100.000 COP), Comisión de ADDI (inicialmente 11%), IVA aplicado sobre la comisión de ADDI (inicialmente 19%).

## 8.11.2 Fórmulas iniciales

Venta a crédito: Valor de venta a crédito = costo + valor definido para la ganancia + valor calculado por el porcentaje adicional.

Venta de contado: Valor de venta de contado = valor de venta a crédito - 100.000 COP.

Venta mediante ADDI: Comisión ADDI = valor de venta a crédito x 11%. IVA de la comisión = comisión ADDI x 19%. Valor para registrar en ADDI = valor de venta a crédito + comisión ADDI + IVA de la comisión.

## 8.11.3 Reglas

Los valores se calcularán automáticamente. El vendedor no podrá modificar los parámetros generales de cálculo. Los cambios en porcentajes deberán quedar registrados en auditoría. La base exacta del 3% y los valores fijos/ administrables deben ser aprobados por el cliente antes del desarrollo.


## 9. MÓDULO DE VENTAS

## 9.1 Objetivo

Registrar la venta, asociar el equipo con el cliente, calcular valores, actualizar el inventario, administrar los medios de pago, registrar los movimientos de caja relacionados y generar el formato imprimible aprobado por el cliente para todas las ventas.

## 9.2 Datos automáticos

Número de venta, Fecha y hora, Usuario que registra, Nombre del asesor (obligatorio del usuario autenticado), Sucursal, Ciudad, Datos del equipo por IMEI, Costo, Estado del inventario, Ganancia calculada, Fecha de salida del inventario.

## 9.3 Datos del cliente

Nombres y apellidos, Tipo de documento, Número de documento, Número de celular, Correo electrónico, Fecha de nacimiento, Fecha de expedición del documento, Dirección.

## 9.4 Referencias personales

Cuando la modalidad lo requiera: Nombre y teléfono de referencia familiar, Nombre y teléfono de referencia personal.

## 9.5 Datos del equipo

Al digitar o seleccionar el IMEI se cargarán automáticamente: Marca, Tipo de producto, Referencia, RAM, Almacenamiento, Color, Categoría, Porcentaje de batería, Costo, Sucursal actual.

## 9.6 Datos comerciales

Valor de venta, Descuento, Costo, Ganancia, Modalidad, Entidad financiera, Crédito autorizado, Cuota inicial, Valor financiado, Número de cuotas, Valor de la cuota, Periodicidad de pago (Semanal si se aprueba, Catorcenal, Quincenal, Mensual, Contado), Equipo libre (cuando aplique), Observaciones.

Relación con entidades financieras: Menú desplegable alimentado desde Administración. Solo financieras activas. Las ventas históricas conservan la financiera original.

## 9.7 Medios de pago

Una venta podrá utilizar uno o varios medios: Efectivo, Tarjeta débito, Tarjeta crédito, Datáfono, Transferencia, Cartera propia, Financiación.

## 9.8 Validaciones de pago

La suma de medios de pago y valor financiado debe coincidir con el total de la venta. Para contado, valor financiado es cero. Para financiada, financiera, número de cuotas y valor de cuota son obligatorios. Descuento no puede superar el límite del rol.

## 9.9 Actualización del inventario

Al confirmar la venta: el equipo pasa a vendido, se registra fecha de salida, IMEI no puede usarse en otra venta activa, se generan movimientos de caja y alimenta dashboards/metas.


## 9.10 Historial y consulta

Consulta por número de venta, fecha, sucursal, ciudad, vendedor, cliente, documento, IMEI, financiera, modalidad, medio de pago y estado.

## 9.11 Modificación de ventas

Una venta confirmada no podrá ser modificada directamente por vendedores ni por administradores de punto. Flujo de aprobación:

- 1. El usuario solicita la modificación y selecciona los campos a cambiar.

- 2. Registra una justificación obligatoria.

- 3. La solicitud queda en estado pendiente de aprobación.

- 4. Un Super Administrador o Administrador revisa la información original y propuesta.

- 5. El administrador aprueba o rechaza la solicitud. Solo después de la aprobación se aplican los cambios.

- 6. El sistema conserva la venta original, los cambios, la justificación, fecha y usuario aprobador.

## 9.12 Anulación de ventas

Requiere solicitud con motivo obligatorio y aprobación administrativa. La venta original se conserva, el inventario y movimientos de caja se ajustan, y la venta anulada no cuenta para metas.

## 9.13 Formato imprimible por venta

## 9.13.1 Definición del formato antes de aprobar la propuesta

El cliente deberá seleccionar y aprobar el único formato imprimible que se implementará para todas las ventas. El vendedor no podrá elegir entre diferentes formatos al registrar una venta.

## 9.13.2 Información del formato aprobado

Incluirá: Número interno de venta, Ciudad, Sucursal, Fecha y hora, Datos del cliente, Entidad financiera, Datos del equipo e IMEI, Crédito/Financiación, Referencias, Asesor responsable, Medios de pago, Observaciones, Texto de aceptación, Espacios para firma y huella.

## 9.13.3 Firma y huella

Firma y huella se realizarán manualmente sobre el documento impreso. No se capturará firma digital ni huella biométrica en el alcance base.

## 9.13.4 Impresión

Generación desde los datos guardados, impresión directa o guardado en PDF desde el navegador. No se almacena automáticamente copia PDF en servidor.

## 9.14 Ingresos, egresos y caja asociados con ventas

Ingresos iniciales: Cuotas iniciales, Ventas de contado, Abonos de cartera propia, Ingresos autorizados.

Egresos iniciales: Gastos autorizados de sucursal, Consignaciones a cuentas de la empresa, Traslados de efectivo, Ajustes autorizados.

Datos del movimiento: Número único, Fecha/hora, Sucursal, Tipo, Categoría, Valor, Medio de pago, Venta relacionada, Referencia, Usuario responsable, Observaciones, Estado.

Reglas: Todo movimiento se asocia a una sucursal; no se eliminan registros; correcciones por anulación o ajuste.


## 10. MÓDULO DE GARANTÍAS Y DEVOLUCIONES

## 10.1 Objetivo

Gestionar el proceso completo de recepción, validación, recolección, envío, seguimiento, reemplazo, devolución y cierre de una garantía asociada con la falla de un equipo.

## 10.2 Inicio de la garantía

Registro mediante IMEI, consulta de venta, confirmación de datos del cliente, fecha de recepción, descripción de falla, estado físico (caja, cable, rayones/golpes), observaciones, si requiere equipo de reemplazo y dirección de recolección.

## 10.3 Reemplazo del equipo

IMEI del equipo nuevo opcional si no hay reemplazo, obligatorio si se entrega nuevo equipo. Se asocia el nuevo IMEI al cliente, conservando relación con el IMEI original en garantía.

## 10.4 Notificación de cambio de IMEI a la entidad financiera

Para ventas financiadas con reemplazo de equipo, se registra la gestión manual ante la financiera (Entidad, IMEI original/ nuevo, fecha, usuario, canal, referencia, estado de gestión). No se incluye integración automática por API.

## 10.5 Cuando no hay reemplazo

Se registra motivo por el cual no se entrega otro equipo, estado físico que impide reemplazo inmediato y observaciones informadas al cliente.

## 10.6 Proceso de garantía con la marca o proveedor

- 1. Subir la unidad al enlace o plataforma de garantías.

- 2. Registrar la validación del IMEI realizada por el proveedor y solicitud por correo.

- 3. Registrar la guía de recolección generada por el centro de servicios.

- 4. Registrar la transportadora asignada.

- 5. Si no se recolecta en los días hábiles definidos, registrar la autorización de envío contra entrega. Tiempo estimado: 15 a 30 días hábiles.

## 10.7 Datos de seguimiento del proceso

Plataforma/enlace, fecha de carga, validación IMEI, guía recolección, transportadora, fechas programadas/reales, días transcurridos, diagnóstico proveedor, observaciones.

## 10.8 Estados iniciales

Recibido en tienda, Pendiente de carga en garantías, Cargado en plataforma, Pendiente de validación de IMEI, IMEI validado, Recolección solicitada, Guía generada, Pendiente de recolección, Recolectado, Enviado contra entrega, Recibido por el centro de servicios, En revisión, En reparación, Reparado, Rechazado, Pérdida de garantía, Nota crédito, Devuelto a la empresa, Entregado al cliente, Disponible para nueva venta, Cerrado.

## 10.9 Cierre de la garantía o devolución

Registro de resultado, fecha de regreso/entrega, IMEI entregado, destino del equipo (inventario o baja), número de nota crédito y confirmación financiera.


## 10.10 Imprimibles

Formatos para recepción, aceptación de reemplazo, entrega de equipo nuevo/reparado y cierre de garantía.

## 11. MÓDULO DE METAS COMERCIALES

## 11.1 Objetivo

Permitir que los administradores configuren metas y que cada punto conozca su avance en tiempo real.

## 11.2 Tipos de metas

Meta general por punto de venta, Meta por ciudad, Meta Android, Meta Apple/iPhone, Meta por entidad financiera, Meta por ciudad y entidad financiera.

## 11.3 Unidad de meta

Cantidad de equipos, Valor vendido, o Ambas cuando se requiera.

## 11.4 Gestión y visualización

Solo administradores crean/modifican metas. Vendedores consultan avance, porcentaje, faltante y estado. Ventas anuladas no suman para el cumplimiento.

## 12. MÓDULO DE ADMINISTRACIÓN

## 12.1 Objetivo

Centralizar la configuración y gestión de elementos maestros (Usuarios, Roles, Sucursales, Bodegas, Proveedores, Entidades financieras, Marcas, Referencias, Catálogos).

## 12.2 Administración de Entidades Financieras

| Campo | Descripción o formato |
| --- | --- |
| Fecha de creación | DD/MM/AA, generada automáticamente |
| Razón social | Nombre de la financiera |
| Número de identificación | Número del NIT |
| Fecha o regla de inicio del corte de cartera | Fecha inicial de aplicación o día definido para iniciar el periodo |
| Fecha o regla de cierre del corte de cartera | Día de la semana o regla mensual recurrente |
| Fecha o regla de pago | Día de la semana o regla mensual recurrente |

Configuración de cortes y pagos: Recurrencia semanal, mensual por posición de día, o fecha inicial. Modificaciones aplican a nuevos periodos sin alterar históricos.


## 12.3 Administración de Proveedores

| Campo | Descripción o formato |
| --- | --- |
| Fecha de creación | DD/MM/AA, generada automáticamente |
| Razón social o nombre del proveedor | Nombre del proveedor |
| Tipo de persona | Natural o jurídica |
| Tipo de documento | Cédula o NIT |
| Nombre de contacto | Nombre del funcionario |
| Número de celular | 310 XXX XX XX |
| Fecha de anulación | DD/MM/AA, generada al deshabilitar |

## 12.4 Administración de Sucursales, Puntos de Venta y Bodegas

| Campo | Descripción o formato |
| --- | --- |
| Fecha de creación | DD/MM/AA, generada automáticamente |
| Nombre de la sucursal | Nombre de la sucursal |
| Dirección | Dirección de la sucursal |
| Número de celular | 310 XXX XX XX |
| Ubicación | Enlace o geolocalización de Google Maps |

Campos adicionales: Código interno único, Tipo de ubicación (Punto de venta, Bodega, Ambos), Ciudad, Estado, responsable principal, Observaciones. Soporta proyección hasta 50 ubicaciones.

## 12.5 Administración de Colaboradores y Usuarios

| Campo | Descripción o formato |
| --- | --- |
| Fecha de creación | DD/MM/AA, generada automáticamente |
| Nombre del colaborador | Nombres y apellidos |
| Número de identificación | Número de cédula |
| Cargo o rol | Super Administrador, Administrador, Administrador de Punto o Vendedor |
| Número de celular | 310 XXX XX XX |
| Fecha de anulación | DD/MM/AA, generada al deshabilitar |

## Roles iniciales:

- Super Administrador: Acceso completo, administración total de usuarios, roles, aprobaciones, inventario, traslados, metas, financieras y reportes consolidados.

- Administrador: Gestión administrativa autorizada, creación de vendedores/admin punto, aprobación de modificaciones/anulaciones, inventario, traslados, metas, financieras e informes.


- Administrador de Punto: Consulta de su sucursal e inventario de punto, registro de ventas, inicio/seguimiento de garantías, consulta de metas, registro de movimientos autorizados, impresión.

- Vendedor: Consulta de inventario de su punto, registro de ventas, impresión del formato aprobado, inicio de garantías, consulta de metas autorizadas, solicitud de modificaciones.

## 12.6 Catálogos Generales

Gestión de Marcas, Tipos de producto, Referencias/modelos, Categorías de equipo, Medios de pago, Categorías de ingresos/egresos y Estados operativos permitidos.

## 13. OPCIONALES COTIZABLES

## 13.1 Carga de fotografías y documentos adjuntos por venta

Permitirá adjuntar fotografías del cliente, documento, soportes de entrega y PDF/imágenes requeridas por financieras.

## 13.2 Importación de datos desde Excel

Alternativa A: Migración inicial asistida. Alternativa B: Importador permanente para el usuario.


## 14. FUNCIONALIDADES INCLUIDAS, OPCIONALES Y EXCLUIDAS

| Funcionalidad | Estado |
| --- | --- |
| Aplicación web para computador | Incluida |
| Acceso desde tablet y celular | Incluido con adaptación básica |
| Inicio de sesión con usuario y contraseña | Incluido |
| Usuario generado con combinación de nombre y apellido | Incluido |
| Control de acceso por roles | Incluido |
| Optimización especializada para celular | No incluida |
| Aplicación móvil nativa | No incluida |
| Registro de inventario | Incluido |
| Separación por tipo, marca y referencia | Incluida |
| Cálculo de precio a crédito | Incluido, sujeto a validación |
| Cálculo de precio de contado | Incluido, sujeto a validación |
| Cálculo de valor para ADDI | Incluido, sujeto a validación |
| Administración de proveedores | Incluida dentro de Administración |
| Traslados de mercancía trazables | Incluidos |
| Ventas con trazabilidad de asesor | Incluidas |
| Menú desplegable de entidades financieras activas | Incluido |
| Pagos combinados | Incluidos |
| Aprobación administrativa de modificaciones de ventas | Incluida |
| Formato imprimible único aprobado antes de la propuesta | Incluido |
| Elección de formato por parte del vendedor | No incluida |
| Captura digital de firma | No incluida |
| Captura biométrica de huella | No incluida |
| Garantías y devoluciones asociadas con fallas | Incluidas |
| Seguimiento de recolección y envío a centro de servicios | Incluido |
| Imprimibles de garantía | Incluidos, sujetos a aprobación |
| Registro de notificación de cambio de IMEI a financieras | Incluido como seguimiento manual |
| Administración de entidades financieras | Incluida dentro de Administración |
| Reglas semanales y mensuales de corte y pago | Incluidas |
| Proyección de pagos de financieras | Incluida |
| Integración automática por API con financieras | No incluida |


| Funcionalidad | Estado |
| --- | --- |
| Administración de colaboradores, usuarios y sucursales | Incluida dentro de Administración |
| Roles Super Admin, Admin, Admin Punto y Vendedor | Incluidos |
| Geolocalización o enlace de Google Maps para sucursales | Incluido |
| Metas por punto, por financiera, y por ciudad/financiera | Incluidas |
| Dashboards imprimibles | Incluidos |
| Exportación a Excel o CSV | Incluida |
| Fotografías y documentos adjuntos por venta | Opcional cotizable |
| Migración inicial e importador permanente de Excel | Opcional cotizable |
| Almacenamiento automático de PDF de ventas | No incluido |
| Contabilidad completa, conciliación bancaria, Power BI, IA | No incluido |
| Eliminación directa de registros | No incluida |
| Consulta del inventario de todos los puntos por vendedores | No incluida |

## 15. EXPORTACIÓN Y CONSERVACIÓN DE INFORMACIÓN

## 15.1 Exportaciones

Exportación a Excel/CSV de Ventas, Inventario, Traslados, Garantías, Caja, Financieras, Usuarios, Sucursales e Informes.

## 15.2 Política histórica

Ventana operativa móvil de 12 meses. Información previa pasa a archivo histórico de solo consulta conservando trazabilidad.


## 16. CAMPOS NORMALIZADOS A PARTIR DEL EXCEL

## 16.1 Inventario

| Campo actual | Campo propuesto en el sistema |
| --- | --- |
| No. | Número interno |
| Agencia | Sucursal o ubicación |
| No. de guía | Número de guía |
| Fecha de pedido / Fecha de ingreso | Fecha de pedido / Fecha de ingreso |
| Distribuidor / No. factura | Proveedor / Número de factura |
| IMEI / Marca / RAM / Color | IMEI / Tipo, marca, referencia / RAM y almacenamiento / Color |
| Costo / Ganancia crédito | Costo / Valor de ganancia configurado |
| Porcentaje adicional | Cálculo automático según parámetro aprobado |
| Valor crédito / Valor contado | Calculado por el sistema |
| Comisión ADDI / IVA comisión ADDI / Valor ADDI | Calculados por el sistema |
| Entrada / Existencia / Salidas | Generados y calculados por el sistema |

## 16.2 Ventas

| Campo actual | Campo propuesto en el sistema |
| --- | --- |
| No. / Agencia / Fecha / Vendedor | Número de venta / Sucursal / Fecha y hora / Usuario autenticado |
| Nombres y apellidos / Celular / Nacimiento / Documento | Datos del cliente (Nombres, celular, nacimiento, tipo/ número doc) |
| IMEI / Marca / RAM / Color / Costo / Ganancia | Datos del equipo e inventario automáticos y calculados |
| Valor / Entidad financiera / Cuota inicial / Descuento / Financiado / Cuotas | Datos comerciales y de financiación |
| Contado / Efectivo / Cartera propia / Datáfono / Transferencia | Modalidades y medios de pago |

## 17. REQUERIMIENTOS NO FUNCIONALES

Seguridad: Inicio de sesión obligatorio, unicidad de usuario, contraseñas seguras, control de acceso por roles, restricción por sucursal, trazabilidad y copias de seguridad.

Rendimiento: Paginación en tablas, filtros, índices de búsqueda por IMEI, documento, venta y fecha. Preparado para 50 puntos y hasta 1.000 ventas mensuales.

Infraestructura: Aplicación y base de datos administradas, variables de entorno, pipeline de despliegue.


Auditoría: Registro completo de inicios de sesión, cambios, solicitudes, aprobaciones, anulaciones, traslados, garantías, movimientos de caja, metas y parámetros de precios/financieras.

## 18. CRITERIOS GENERALES DE ACEPTACIÓN

La solución se considerará aceptada cuando funcionen adecuadamente todas las características descritas en las secciones anteriores, incluyendo inicio de sesión con unicidad de usuario, gestión multipunto, traslados trazables, ventas autenticadas por asesor, cálculo de fórmulas de precios, formato único de venta, aprobación de modificaciones por roles superiores, módulo completo de garantías con seguimiento de recolección/envío, reglas de financieras por posición mensual/semanal, metas, dashboards, exportaciones, y archivado histórico a 12 meses sin eliminación directa de registros críticos.

## 19. ENTREGABLES

- Documentación: Alcance funcional, reglas de negocio, matriz de roles, matriz de campos, flujos y criterios de aceptación.

- Diseño: Prototipo, navegación, formularios, dashboard y formatos imprimibles.

- Desarrollo: Código fuente, base de datos, migraciones, módulos aprobados, roles y exportaciones.

- Calidad: Pruebas unitarias, funcionales, de seguridad, roles, ventas, inventario, garantías y financieras.

- Despliegue: Aplicación desplegada, pipeline, variables y copias de seguridad.

- Cierre: Manual básico, capacitación, credenciales administrativas y acta de aceptación.

## 20. PUNTOS PENDIENTES PARA CERRAR EL ALCANCE

Aprobación del único formato imprimible de venta, campos definitivos de garantía, plataforma de garantías, base exacta para el porcentaje del 3 %, confirmación de valores fijos/administrables para 100.000 COP y porcentajes de ADDI, reglas iniciales de corte/pago de financieras, jerarquía final Super Admin vs Admin, fórmulas definitivas del Dashboard, canales de notificación de IMEI y decisión final sobre adjuntos e importación de Excel.

## 21. GESTIÓN DE CAMBIOS

Cualquier funcionalidad no incluida explícitamente se manejará como solicitud de cambio evaluando descripción, motivo, impacto funcional, técnico, tiempo, costo y responsable de aprobación.

## 22. APROBACIÓN DEL ALCANCE

La aprobación confirma que las partes comprenden y aceptan los módulos, exclusiones, reglas, entregables y procedimiento de cambios.


## 23. CONDICIONES DE PAGO E INCUMPLIMIENTO

Una vez aceptado y firmado el presente documento, el cliente contará con un plazo máximo de cinco (5) días calendario para realizar el pago correspondiente al veinticinco por ciento (25 %) del valor total acordado. Este pago dará inicio formal a la ejecución del proyecto.

La segunda etapa de pago estará asociada a la primera entrega establecida dentro del desarrollo del proyecto. A partir de la fecha en que dicha entrega sea puesta a disposición del cliente, este contará con un plazo máximo de cinco (5) días calendario para efectuar el pago correspondiente a esta etapa.

La tercera y última etapa de pago estará asociada a la entrega final del proyecto. Una vez la solución final sea puesta a disposición del cliente, este contará con un plazo máximo de cinco (5) días calendario para efectuar el pago correspondiente al saldo restante acordado.

Ante dicho incumplimiento, el proveedor podrá suspender temporalmente el acceso al sistema y retirar la aplicación del entorno de operación hasta que el cliente regularice la totalidad de los valores pendientes. La reactivación del servicio se realizará una vez se confirme el pago correspondiente, sin que esta suspensión implique la eliminación de las demás obligaciones, compromisos o condiciones establecidas en la propuesta.

Responsable del negocio

Responsable del desarrollo

Nombre:

Nombre:

Cargo:

Cargo:

Fecha:

Fecha:

Firma:

Firma:

---
name: contrato-adhesion-minorista-central-compras-mer-0505
description: "Contrato de adhesión de un minorista a una central de compras. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de adhesión de un minorista a una central de compras

> Formulario **MER-0505** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Contrato de suministro por el que se propone la opción más simple en la que la central de compras vende en firme al distribuidor minorista y se plantean como posible alternativa cláusulas que construirían un sistema de distribución selectiva afiliado a la central de compras

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de adhesión de un minorista a una central de compras» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de adhesión de un minorista a una central de compras” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-adhesion-minorista-central-compras-mer-0505`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] DATOS REGISTRALES (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] FECHA (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] ACTIVIDAD
- [ ] DIRECCIÓN
- [ ] LUGAR
- [ ] MOTIVO
- [ ] NOMBRE DE LA INSTITUCIÓN ARBITRAL
- [ ] NOMBRE DE LA MARCA
- [ ] Nº
- [ ] NÚMERO
- [ ] PLAZO
- [ ] PORCENTAJE
- [ ] TELÉFONO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Contrato de suministro por el que se propone la opción más simple en la que la central de compras vende en firme al distribuidor minorista y se plantean como posible alternativa cláusulas que construirían un sistema de distribución selectiva afiliado a la central de compras


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero el «Texto del formulario» (al final de este fichero) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea del «Texto del formulario» y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Texto del formulario

Lo que sigue, hasta el final de este fichero, es el formulario tal cual: desde su primera línea hasta la firma.

En la ciudad de [LOCALIDAD] a [FECHA].

REUNIDOS

De una parte

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI [DNI/NIE] en representación de la sociedad [DENOMINACIÓN SOCIAL] con domicilio en [LOCALIDAD], según consta en el Registro Mercantil de [LOCALIDAD] nº registro [DATOS REGISTRALES] en adelante denominado el SUMINISTRADOR/LA CENTRAL DE COMPRA

y de otra

D./Dña. [NOMBRE Y APELLIDOS] mayor de edad, con DNI nº [DNI/NIE] en su condición de (gerente/administrador/empresario) de la empresa con domicilio en según consta en el Registro Mercantil de [LOCALIDAD] nº registro [DATOS REGISTRALES] en adelante denominado el DISTRIBUIDOR.

Ambos se reconocen capacidad suficiente y legitimación para contratar y

EXPONEN:

- Que [DENOMINACIÓN SOCIAL] es una empresa dedicada a la distribución mayorista de productos multimarca de amplio espectro según se detalla en su catálogo de productos, en adelante el CATÁLOGO general de productos.
- Que D./Dña. [NOMBRE Y APELLIDOS] es titular/gerente de una empresa de distribución minorista dedicada al ramo de [ACTIVIDAD].
- Que ambos manifiestan interés en concluir un contrato de suministro actuando como suministrador y distribuidor respectivamente sometiéndose a las siguientes

ESTIPULACIONES:

1.- Suministro

Suministrador y distribuidor acuerdan la realización de un suministro continuado de los productos establecidos en el catálogo general de la central de compra, que será debidamente actualizado con periodicidad semestral. A tal fin, el suministrador adjudicará un código de cliente al distribuidor con el que se realizarán todas las gestiones con la central de compra.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Para el registro como cliente del distribuidor éste aportará sus datos bancarios al servicio de atención al cliente de la central de compra)

Para el registro como cliente del distribuidor éste aportará sus datos bancarios al servicio de atención al cliente de la central de compra y prestará fianza de [IMPORTE] Euros con carácter previo a la realización del primer pedido)

2.- Catálogo de Productos

El suministrador proporcionará al distribuidor un ejemplar del catálogo de productos, así como de sus sucesivas renovaciones y de las ofertas especiales que realice la central de compra.

El suministrador se compromete a la entrega en el domicilio señalado de cualquiera de los productos incluidos en su catálogo general de productos. Se fija como domicilio de entrega del distribuidor el de [DIRECCIÓN],

El suministrador se reserva la facultad de actualizar el catálogo, descatalogar productos y sustituir los productos del mismo por otros de calidad y características equiparables en atención a las circunstancias del mercado. El compromiso de suministro queda condicionado a las existencias presentes en almacén. El reparto de existencias, caso de existir limitaciones se atenderá por el orden de entrada.

3.- Unidades de pedido

Si existen limitaciones máximas en las cantidades o unidades del pedido, el suministrador las hará constar con carácter previo en el catálogo o las comunicará mediante el pertinente aviso.

Si existen limitaciones mínimas en productos que se distribuyan por lotes, por número o cantidad mínima de pedido se harán constar en el catálogo general.

El catálogo fijará para cada producto o lote mínimo de los mismos su denominación comercial, código de producto, unidades de pedido mínimo, unidades por caja o paquete de embalaje, precio de compra por unidad y precio de venta al público recomendado.

[OPCIONAL — incluir si procede]

3 bis.-

[OPCIONAL — incluir si procede]

El distribuidor se compromete a la realización de una compra mínima inicial de productos del catálogo por importe de [IMPORTE] Euros)

[OPCIONAL — incluir si procede]

El distribuidor recibirá del suministrador una sugerencia de stock mínimo elaborada y justificada conforme a sus estadísticas y estudios de ventas con el fin de facilitar la constitución del stock inicial)

[OPCIONAL — incluir si procede]

El distribuidor compromete la realización de pedidos al suministrador por un importe mínimo de [IMPORTE] Euros por trimestre.

[OPCIONAL — incluir si procede]

El distribuidor contrae la obligación de compra en exclusiva [OTROS DATOS]

1: - de los productos integrados en el catálogo general de productos del suministrador/

2: - de los productos del catálogo marcados con la enseña, marcas y/o signos distintivos del suministrador y [OTROS DATOS].

2 a) - renuncia a vender en su establecimiento productos idénticos o similares de marcas competidoras

2 b) - renuncia a la venta de productos suministrados por empresas alternativas o competidoras en cuantía superior al [PORCENTAJE] % del volumen total de facturación.

4.- Realización de pedidos

Los pedidos del distribuidor podrán realizarse por teléfono, fax o email a cualquiera de las direcciones y números establecidos en el catálogo general, web de la compañía o modelos de pedidos aportados por el suministrador.

5.- Pedidos ordinarios y extraordinarios

Todos los pedidos deberán realizarse siempre antes de las 12 de la mañana del día semanal asignado al distribuidor por el servicio de atención al cliente. Los pedidos realizados en la semana anterior al día semanal asignado se acumularán en la hoja de pedido semanal que se tramitará como pedido único el día asignado.

Todos los pedidos deberán superar el importe mínimo del pedido que se fija inicialmente en 200 euros.

El distribuidor podrá realizar pedidos extraordinarios fuera de esta periodicidad pero en este caso el importe mínimo deberá superar los 600 euros y se añadirá un cargo de 50 euros en concepto de pago de portes.

Los importes de los pedidos mínimos serán revisados anualmente.

6.- Condiciones de entrega

las entregas de los productos solicitados por el distribuidor utilizando los conductos establecidos se realizarán el día semanal asignado por el servicio de atención al cliente para su ruta y en el plazo máximo de una semana a contar desde la solicitud realizada en el día asignado al distribuidor para dicha gestión.

7.- Recepción de entregas

El distribuidor recibirá con la entrega de los pedidos un albarán con indicación de un listado con los bultos entregados, contenido, número y precio, debiendo entregar copia firmada del mismo al transportista.

Es obligación del distribuidor comprobar la lista y número de bultos antes de firmar la copia del albarán. Las reclamaciones que se deseen realizar por falta de bultos deberán consignarse en el propio albarán e irán firmadas por el distribuidor o persona autorizada por el mismo.

Es obligación del distribuidor comprobar el estado general del embalaje y de los bultos. Cualquier reclamación que se desee realizar sobre el estado de los mismos deberá consignarse en el propio albarán e irá firmada por el distribuidor o persona autorizada por el mismo.

Una vez firmado el albarán y entregado sin consignación de incidencias no se aceptarán reclamaciones por esta causa.

Una vez firmado el albarán con aceptación de cajas completas no se admitirán reclamaciones respecto a cajas incompletas. El distribuidor podrá examinar a su contento las cajas antes de firmar el albarán.

Las reclamaciones de los productos señalados como de alto valor en el catálogo general deberán hacer mención expresa a esta circunstancia. Las incidencias sobre los productos de alto valor que superen los [IMPORTE] euros se someterán al arbitraje de [NOMBRE DE LA INSTITUCIÓN ARBITRAL] si no fuera posible el acuerdo amistoso

8.- Incidencias en la entrega

Cualquier otra incidencia en la entrega no señalada en la estipulación anterior se comunicará al transportista y se anotará en el albarán de entrega (mal estado de los productos entregados, productos de caducidad excesivamente corta, productos golpeados, etc.) Las incidencias se comunicarán al servicio de atención al cliente de la central de compra antes de una semana.

9.- Devoluciones

El distribuidor comunicará las devoluciones al servicio de atención al cliente de la central de compra utilizando los conductos de comunicación señalados (teléfono [TELÉFONO], fax, formulario de hoja de devolución) indicando en todo caso, los datos de código del pedido, código de los productos devueltos, descripción de cantidad, número de bultos, número de albarán de entrega y una indicación de la causa de devolución. La hoja de devolución o albarán devuelto deberá ir firmado por el distribuidor o persona autorizada por el mismo.

Las devoluciones se realizarán en los días asignados para las entregas y para ello deberán ser comunicadas al servicio de atención al cliente de la central de compra antes de las 12 horas de la mañana del día asignado para la realización del pedido semanal.

Solo se recogerán las devoluciones notificadas previamente con los datos completos. Se rechazará el embarque de aquellos bultos no consignados en la solicitud de devolución y de aquellos que no hayan sido designados con sus datos completos. No se podrá variar el número de bultos o características de las mercancías cuya solicitud de devolución se haya cursado.

Para la realización de la devolución, el transportista del suministrador acudirá provisto de hojas de recogida/etiquetas identificativas correspondientes a los productos cuya devolución se solicita, que serán firmadas a la entrega por el distribuidor o persona autorizada por el mismo.

Las diferencias de cantidad que se deriven de las devoluciones dependerán de la comprobación final del estado de los artículos en el almacén del suministrador y se compensarán en la factura correspondiente al mes en curso.

Las mercancías que se quieran devolver deberán estar en todos los casos debidamente embaladas y en buen estado, no caducada y sin etiquetas o marcajes ajenos al suministrador. Si no se cumplen estas condiciones el suministrador podrá declarar la devolución improcedente y la mercancía se devolverá al distribuidor en la siguiente entrega.

No se admitirá en ningún caso devoluciones con un plazo superior a [Nº] días desde la entrega.

No se admitirá en ningún caso devoluciones de productos perecederos y de alimentación con manipulación. Cualquier reclamación sobre estos productos se sustanciará mediante compensación de la parte responsable

10.- Plazos de Pago

La facturación será realizada por la Central de compra el último día de cada mes comprendiendo todas las entregas realizadas durante dicho período, incluidas las devoluciones realizadas en firme.

La factura tendrá vencimiento inmediato y se abonará mediante domiciliación bancaria o con aplazamiento a 60 días si se presenta aval bancario.

11.- Terminación del contrato

El contrato se pacta por plazo indefinido, pudiendo ser denunciado por cualquiera de las partes mediante preaviso en el plazo de [PLAZO].

[OPCIONAL — incluir si procede]

Son causas de terminación del contrato sin necesidad de preaviso:

— la no realización de pedidos en plazo superior a dos meses/la no realización de las compras mínimas establecidas en el presente acuerdo.
— la utilización indebida de los rótulos, marcas, embalajes envoltorios y demás signos distintivos o promocionales del suministrador.
— la vulneración de los compromisos de exclusividad establecidos en el presente acuerdo.
— el incumplimiento de los protocolos de solicitud, recepción y/o devolución de las mercancías.
— El impago o el retraso superior a 20 días en la liquidación de los pagos correspondientes a las entregas realizadas y facturadas.

12.- Datos comerciales

El suministrador incorporará los datos correspondientes al distribuidor en sus bases de datos, que serán convenientemente registradas en la Agencia Española de Protección de Datos conforme a lo establecido en la Ley Orgánica de Protección de Datos Personales. El distribuidor consiente en la utilización/cesión de dichos datos para [MOTIVO] Asiste al distribuidor el ejercicio de los derechos de acceso, rectificación y cancelación en los términos establecidos en la ley.

[OPCIONAL — incluir si procede]

El distribuidor consiente en la utilización de los datos correspondientes a sus ventas para la elaboración de estudios de mercado encaminados a la mejor adaptación de los productos que integran el catálogo general de productos, la elaboración de planes de adquisición y la elaboración de ofertas comerciales adaptadas a los niveles reales de consumo.

[OPCIONAL — incluir si procede]

13.- El distribuidor queda autorizado a la comercialización de los productos bajo la enseña,/rótulo [NOMBRE DE LA MARCA] registrada en la agencia española de patentes y marcas con el n.º [NÚMERO] de la que es titular el suministrador, así como a utilizar los envases, bolsas y demás distintivos promocionales registrados del suministrador, siempre en condiciones de no exclusividad y sometido a las condiciones de este contrato.

El distribuidor no podrá alterar, sublicenciar, ceder o manipular los elementos distintivos y promocionales del suministrador.

Finalizado el contrato el distribuidor se obliga a retirar los rótulos, marcas y demás distintivos del suministrador, así como a devolver los envases, bolsas carteles y demás elementos promocionales distintivos del suministrador

Otras Cláusulas opcionales:

* Sometimiento a arbitraje para la resolución de conflictos
* Financiación de los distribuidores, mecanismos de aplazamiento de pagos
* Realización de campañas promocionales o publicitarias conjuntas

Firmado En [LUGAR], a [FECHA].

SUMINISTRADOR/LA CENTRAL DE COMPRA

DISTRIBUIDOR
D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]

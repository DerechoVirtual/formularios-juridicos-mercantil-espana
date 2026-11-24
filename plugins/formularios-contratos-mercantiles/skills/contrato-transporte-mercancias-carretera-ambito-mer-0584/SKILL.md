---
name: contrato-transporte-mercancias-carretera-ambito-mer-0584
description: "Contrato de transporte de mercancías por carretera en ámbito nacional. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de transporte de mercancías por carretera en ámbito nacional

> Formulario **MER-0584** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de transporte de mercancías por carretera en ámbito nacional» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de transporte de mercancías por carretera en ámbito nacional” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-transporte-mercancias-carretera-ambito-mer-0584`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (5 veces)
- [ ] Nº (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] CALLE (3 veces)
- [ ] HORA (3 veces)
- [ ] NÚMERO DE LA CALLE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] CLASE
- [ ] FECHAS
- [ ] LUGAR

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Tras la entrada en vigor de la Ley Concursal, y de conformidad con su artículo 61.3, "Se tendrán por no puestas las cláusulas que establezcan la facultad de resolución o la extinción del contrato por la sola causa de la declaración de concurso de cualquiera de las partes".


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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL REMITENTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL PORTEADOR", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE TRANSPORTE, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que EL REMITENTE es una persona jurídica de derecho privado dedicada a la (fabricación/producción [ELEGIR: fabricación / producción]) de (descripción del producto).

SEGUNDO.- Que EL PORTEADOR es titular de la autorización de la clase [CLASE] núm. (cuando el porteador sea un operador de transporte) y de los siguientes vehículos:

a) Matrícula:

b) Marca:

c) Autorización de Transporte núm. [Nº]

TERCERO.- Que ambas partes de común acuerdo llevan a efecto el presenten contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

EL PORTEADOR se compromete al transporte de las mercancías señaladas en el Anexo I desde (lugar de origen) a (lugar de destino) entre los días [FECHAS] y [DÍA] del mes de [MES] de (año).

[ELEGIR UNA OPCIÓN: Precio, facturación y pago / Precio fijo / Precio variable]

Revisión del precio por alteración del precio del combustible

EL PORTEADOR podrá incrementar en su factura el precio inicialmente pactado en cuantía equivalente a la diferencia existente entre el precio que tenía el litro de gasóleo el día de celebración del contrato y el que tenía en el momento de realizarse el transporte, multiplicada por el número de litros de gasóleo utilizados en su realización.

De la misma manera, el obligado al pago del precio del transporte podrá exigir una reducción equivalente del precio inicialmente pactado cuando el precio del gasóleo se hubiese reducido entre la fecha de celebración del contrato y la de realización efectiva del transporte.

Recogida y entrega de la mercancía

Carga y descarga asumida por EL PORTEADOR

El PORTEADOR se obliga a la recogida y carga de dichas mercancías en los almacenes que EL REMITENTE tiene en (localidad) en la calle [CALLE] núm. [NÚMERO DE LA CALLE] el día [FECHA] de (mes) de (año) entre las [HORA] y las horas.

EL PORTEADOR se obliga a entregar dichas mercancías en el almacén sito en (localidad) en la calle [CALLE] núm. [NÚMERO DE LA CALLE] el día [FECHA] de (mes) de (año) entre las [HORA] y las horas.

Carga y descarga asumida por EL REMITENTE

EL PORTEADOR cumplirá su obligación poniendo a disposición del REMITENTE el vehículo para su carga en el almacén sito en (localidad) en la calle [CALLE] núm. [NÚMERO DE LA CALLE] el día [FECHA] de (mes) de (año) entre las [HORA] y las horas. Transcurrido dicho plazo sin que vehículo haya sido puesto a su disposición, EL REMITENTE podrá, sin perjuicio de exigir la indemnización a que en su caso hubiere lugar, buscar otro PORTEADOR.

El plazo para realizar la carga del envío a bordo del vehículo será de [Nº] horas contadas desde su puesta a disposición por EL PORTEADOR. Cuando EL REMITENTE incumpla los plazos anteriormente señalados podrá EL PORTEADOR exigirle una indemnización en concepto de paralización del vehículo, a menos que pruebe que el retraso se debió a circunstancias de fuerza mayor, caso fortuito o causa imputable al PORTEADOR.

Acondicionamiento, embalaje y señalización del envío de mercancías con riesgo

Las mercancías deberán ser entregadas al PORTEADOR convenientemente acondicionadas y embaladas, y señalizadas mediante marcas o inscripciones que avisen del riesgo que su manipulación pueda entrañar para las personas o para las propias mercancías, de tal forma que éstas puedan soportar sin menoscabo su transporte en condiciones normales y no constituyan causa de peligro para el porteador o su personal dependiente, las demás mercancías transportadas, el vehículo o los terceros.

EL PORTEADOR podrá rechazar los envíos o bultos que se presenten mal acondicionados, embalados o señalizados para su transporte.

Itinerario

Determinado por EL PORTEADOR

El PORTEADOR puede elegir las rutas, medios y demás aspectos del transporte que estime convenientes.

Determinado por EL REMITENTE

EL PORTEADOR no podrá apartarse de la ruta elegida por EL REMITENTE salvo por causa de fuerza mayor.

Si se apartara de la misma sin mediar causa justificada, será responsable de todos los daños que por cualquier circunstancia sobrevengan durante el transporte a las mercancías que integran el envío, además de pagar la suma de [IMPORTE] euros ( €) en concepto de arras penitenciales.

Seguimiento en carretera

Los vehículos utilizados en la ejecución del presente contrato deberán tener instalado un medio de comunicación (describir) que permita al PORTEADOR informar de las siguientes incidencias:

a) Detención de vehículos durante más de una hora

b) Averías

c) Elección de rutas o itinerarios alternos

d) Cualquier otra incidencia que pudiera provocar un retraso en entrega de la mercancía superior a [Nº] horas/días

[ELEGIR UNA OPCIÓN: Daño o avería / Daño o avería en la mercancía / Reservas en el momento de la entrega / Dentro de un plazo desde la entrega]

Nombramiento de peritos

Si se producen dudas y contestaciones entre EL CONSIGNATARIO y EL PORTEADOR sobre el estado en que se hallan las mercancías que componen el envío en el momento en que éste hace entrega de las mismas a aquél, dichas mercancías serán reconocidas por peritos nombrados por las partes, y un tercero en caso de discordia, designado por la Junta Arbitral del Transporte.

Retraso en la entrega

EL PORTEADOR deberá entregar sin demora ni entorpecimiento alguno el envío al CONSIGNATARIO dentro del plazo de tiempo acordado en la Cláusula Primera.

De no hacerlo así en supuesto de incumplimiento del plazo de entrega por parte del transportista, las partes pactan una penalización de [IMPORTE] euros por cada día de retraso en la entrega de la carga, descontándose, en su caso, de la cantidad que quedara pendiente de pago si la misma fuera superior a la derivada de la penalización por retraso pactada, salvo que pruebe que el retraso fue debido a fuerza mayor, caso fortuito o causa imputable al CARGADOR o CONSIGNATARIO.

Responsabilidad del porteador

Alcance de la responsabilidad

Las mercancías se transportarán a riesgo y ventura del remitente.

La responsabilidad del porteador comenzará desde el momento en que las mercancías se encuentren cargadas, colocadas y estibadas en su totalidad a bordo del vehículo que ha de realizar el transporte.

Límites a la responsabilidad del PORTEADOR

La responsabilidad del PORTEADOR por los daños, pérdidas o averías que sufran las mercancías integrantes del envío o por los retrasos en su entrega al consignatario, estará limitada como máximo a la cantidad de [IMPORTE] euros por kilogramo/tonelada

Dicha limitación de responsabilidad no será de aplicación cuando el daño o retraso se hubiese producido mediando dolo del PORTEADOR.

Subcontratación

El transporte de las mercancías deberá ser realizado por EL PORTEADOR con los medios personales y materiales integrantes de su propia organización empresarial, utilizando vehículos de los que disponga en tal concepto.

No obstante, cuando el transporte se lleve a cabo por EL PORTEADOR mediante la colaboración de otro PORTEADOR que cuente con el personal y los vehículos adecuados para realizarlo, no quedará desvirtuada su condición de porteador único frente al REMITENTE.

En todo caso, los vehículos utilizados habrán de reunir las condiciones adecuadas para el transporte del envío de que se trate, así como para el acceso y circulación por los lugares en que haya de realizarse su carga y descarga, cuando tales condiciones le hubiesen sido previamente comunicadas por el REMITENTE.

Derecho de retención

EL PORTEADOR autoriza al REMITENTE a retener hasta el % del precio del porte hasta que se demuestre que las mercancías han sido recibidas en condiciones óptimas para su utilización o, en su caso, hasta que EL PORTEADOR haya respondido de los daños y perjuicios irrogados al remitente.

Seguro

EL PORTEADOR contratará un seguro que resulte satisfactorio para EL REMITENTE y proporcionará a éste, a su solicitud, pruebas de la existencia de dicho seguro. La cobertura incluirá, entre otros aspectos, los daños provocados por incendios, agua, fenómenos naturales y robo.

EL PORTEADOR informará con prontitud al REMITENTE de cualquier peligro asegurable y cualquier suceso extraordinario que afecten a la mercancía transportada y tomará las medidas necesarias para la resolución del problema y la satisfacción de las reclamaciones.

Resolucion del contrato

El Contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2. Por acuerdo de las Partes por escrito.

3. La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

Cláusula penal

En caso de resolución del contrato por causa imputable a cualquiera de las Partes, la parte contraria no estará obligada a la devolución de las mercancias o cantidades entregadas hasta ese momento, fijándose además una cantidad adicional de [IMPORTE] € como indemnización que la parte incumplidora deberá abonar a

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Jurisdicción competente y ley aplicable

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, la competencia de los Tribunales que deban conocer del asunto se determinará de conformidad con los criterios de competencia objetiva, funcional y territorial legalmente aplicables.

El presente contrato tiene carácter mercantil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE TRANSPORTE INTERIOR POR CARRETERA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo. Don [NOMBRE Y APELLIDOS]

(El Porteador)

Fdo. Don [NOMBRE Y APELLIDOS]

(El REMITENTE)

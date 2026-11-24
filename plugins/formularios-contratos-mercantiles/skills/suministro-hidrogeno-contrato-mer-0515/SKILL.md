---
name: suministro-hidrogeno-contrato-mer-0515
description: "Suministro de hidrógeno (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Suministro de hidrógeno (contrato)

> Formulario **MER-0515** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Suministro de hidrógeno (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Suministro de hidrógeno (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:suministro-hidrogeno-contrato-mer-0515`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (14 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (3 veces)
- [ ] PROVINCIA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] INSCRIPCIÓN (2 veces)
- [ ] NIF (2 veces)
- [ ] ACTIVIDAD
- [ ] CONSUMO MÍNIMO
- [ ] INSTITUCIÓN DE MEDIACIÓN
- [ ] NIF/DNI
- [ ] Nº DE CUENTA (IBAN)
- [ ] NÚMERO
- [ ] PLAZO

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

- Ninguna.

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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [FECHA]

REUNIDOS

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NÚMERO],

Y de otra parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NIF/DNI]

INTERVIENEN

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF [NIF], domiciliada en [DOMICILIO] y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA] e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], en adelante LA PROVEEDORA

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF [NIF], domiciliada en [DOMICILIO] y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA] e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], en adelante LA SUMINISTRADA

MANIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE SUMINISTRO, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que la PROVEEDORA es una empresa dedica al almacenamiento, transporte y suministro de hidrógeno con las siguientes características:

II. Que la SUMINISTRADA se dedica a la actividad de [ACTIVIDAD], para lo cual precisa de suministro continuado de hidrógeno de las características comercializadas por la proveedora expresadas anteriormente.

III. Que, conviniendo ambas partes en concertar el suministro de hidrógeno, otorgan a tal fin el presente CONTRATO DE SUMINISTRO, en base a las siguientes

CLÁUSULAS

PRIMERA.- OBJETO DEL CONTRATO

Por medio del presente contrato, la PROVEEDORA se compromete a la prestación del suministro de hidrógeno, que deberá ser entregado en las instalaciones de la SUMINISTRADA sitas en [LOCALIDAD].

El hidrógeno suministrado tendrá los requisitos técnicos y de calidad que se recogen en las prescripciones del Anexo I de este contrato, debiendo ser descargado en los puntos de suministro que se reflejan en el Anexo II.

Para la duración prevista del contrato, se estima un consumo mínimo de hidrógeno de [CONSUMO MÍNIMO] kg/mensuales, y un consumo máximo de [PLAZO] kg/mensuales.

El suministro mínimo mensual será el expresando anteriormente, que la SUMINISTRADA se compromete a adquirir en cada periodo mensual, pero la cantidad estimada que opera como límite máximo es orientativa, quedando subordinada el consumo real a las necesidades finales de la SUMINISTRADA.

SEGUNDA.- PERIODO INICIAL DEL SUMINISTRO Y PRÓRROGAS

El periodo de vigencia inicial de este contrato es de dos años, a contar desde la firma del mismo.

No obstante, las partes podrán prorrogar el contrato por periodos de un año. Al efecto, el contrato se entenderá prorrogado por un año si ninguna de las partes manifiesta su voluntad de no renovarlo antes de la finalización del periodo o de sus sucesivas prórrogas.

En caso de que alguna de las dos partes pretenda finalizar el contrato a la finalización del periodo, deberá comunicarlo con un periodo de preaviso de tres meses.

TERCERA.- FORMA Y LUGAR DE ENTREGA DEL SUMINISTRO

Los pedidos del suministro de hidrógeno se realizarán en función de las necesidades de la SUMINISTRADA para cada periodo mensual, debiendo realizar sus pedidos, como mínimo, con periodicidad quincenal.

Una vez recibido el pedido por la PROVEEDORA, el plazo máximo de entrega será de setenta y dos horas desde la recepción del pedido.

En caso de situaciones de urgencia debidamente justificada por la SUMINISTRADA, se establece un plazo máximo de veinticuatro horas desde la comunicación de la circunstancia que justifica el suministro urgente.

El lugar de entrega de los suministros será las instalaciones de la empresa SUMINISTRADA, sitas en [LOCALIDAD], en los puntos de suministro reflejados en el Anexo II, siendo de cuenta de la PROVEEDORA del transporte y operaciones de descarga a depósitos de la SUMINISTRADA.

CUARTA.- PRECIO DEL SUMINISTRO Y FORMA DE PAGO

El precio del suministro se fija en la cantidad de …. euros por kilogramo suministrado, más IVA.

El pago se hará contra factura mensual que emitirá la PROVEEDORA según el total suministrado en el mes corriente, con el mínimo estipulado en la cláusula primera de este contrato.

El importe de cada factura se hará efectivo en la cuenta [Nº DE CUENTA (IBAN)], titularidad de la PROVEEDORA, dentro de los diez primeros días de cada mes.

QUINTA.- REVISIÓN DE PRECIOS

A la finalización del periodo inicial del contrato, en el caso de prórrogas sucesivas, el precio podrá ser actualizado por la PROVEEDORA, acomodándose a la variación porcentual experimentada por el Índice de Precios al Consumo que fije el Instituto Nacional de Estadística (u Organismo que le sustituya), aplicando sobre el precio inicial pactado el porcentaje que represente la diferencia existente entre los índices que correspondan al período de revisión.

De forma excepcional, si los generales costes de producción del hidrógeno se incrementarán más de un 25%, podrá revisarse el precio para ajustarlo al incremento de costes, lo cual deberá justificar documentalmente la PROVEEDORA. En este caso, la SUMINISTRADA podrá desistir de la prórroga del contrato si no estuviere conforme con dicho incremento.

SEXT A.- OBLIGACIONES DE LA PROVEEDORA

La PROVEEDORA se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, y en especial asume las siguientes obligaciones:

-La PROVEEDORA se obliga a suministrar el hidrógeno en los puntos de suministros que aparecen en el Anexo II en los términos pactados. El suministro será entregado por trasvase del medio de transporte utilizado por la PROVEEDORA al tanque o depósito, desde sus vehículos de transporte, siendo de su cuenta los gastos ocasionados por el transporte y entrega.

- La PROVEEDORA será responsable de realizar el transporte y la descarga del suministro con las debidas garantías de manipulación, seguridad y calidad.

-La PROVEEDORA mantendrá a disposición de la SUMINISTRADA un teléfono, o dirección de correo electrónico de contacto para poder atender al suministro, realizar los pedidos, o atender cualquier consulta o problema que surja.

-La PROVEEDORA responderá de todos aquellos daños o perjuicios que se pudiesen producir por efecto directo de la falta de calidad del producto suministrado imputable al mismo, o a sus empleados en ejecución del suministro.

SÉPTIMA.- OBLIGACIONES DE LA SUMINISTRADA

La SUMINISTRADA se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, y en especial asume las siguientes obligaciones:

-La SUMINISTRADA se obliga al pago puntual del precio del suministro.

-La SUMINISTRADA pondrá a disposición de la PROVEEDORA sus instalaciones y puntos de suministro en óptimas condiciones de descarga, facilitando el inmediato acceso a los puntos de suministro a los efectos de realizar las operaciones de descarga.

- La SUMINISTRADA se obliga a comunicar cualquier incidencia o problema que surja con los suministros, así como a realizar los pedidos de forma continuada con arreglo a los volúmenes y capacidades de transporte de los vehículos utilizados por la PROVEEDORA.

OCTAVA.- CAUSAS DE RESOLUCIÓN ANTICIPADA.No obstante la fecha de extinción del contrato o de sus prórrogas, las partes podrán resolver anticipadamente el contrato en caso de incumplimiento grave de sus obligaciones en los términos pactados en este contrato.

Específicamente, se pactan como causas de resolución la de cese de actividad de la cualquiera de las partes, el haber declarado su disolución o liquidación, o incurrir en causa legal de disolución, o la pérdida de valor de sus activos que represente más de un ….% del valor de su activo inmovilizado según las cuentas anuales, así como la de apertura de la fase de liquidación tras la declaración judicial de concurso de cualquiera de las partes.

NOVENA.- NOTIFICACIONES

Al margen de las comunicaciones telefónicas y por correo electrónico sobre pedidos o incidencias, las demás notificaciones que se efectúen entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

DÉCIMA.- SUMISIÓN A MEDIACIÓN Y/O ARBITRAJE

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación (en su caso se citará la institución) de [INSTITUCIÓN DE MEDIACIÓN], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y (caso de fijar un plazo máximo....) fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

(caso de pacto sucesivo de arbitraje...) A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de la Corte de [LOCALIDAD], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato y sus Anexo I y II, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

Fdo.: Fdo.:

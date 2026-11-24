---
name: contrato-servicios-asesoria-laboral-mer-0561
description: "Contrato de servicios de asesoría laboral. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicios de asesoría laboral

> Formulario **MER-0561** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicios de asesoría laboral» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicios de asesoría laboral” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-servicios-asesoria-laboral-mer-0561`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA PARTE

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

[ELEGIR UNA OPCIÓN: Intervienen / Si intervienen en nombre y representación de alguien / Opción 1: Si intervienen en nombre y representación de alguien / Si intervienen en su propio nombre y derecho / Opción 2: Si intervienen en su propio nombre y derecho]

EXPONEN

I.- Que el ASESOR está especializado en la prestación de servicios de asesoramiento fiscal, económico- financiero, contable, laboral y complementarios.

II.- Que el CLIENTE está interesado en recibir del ASESOR, la prestación del servicio de asesoría fiscal, contable, laboral tal y como se define en el presente documento.

III.- Que ambas partes han acordado realizar el presente contrato de prestación de servicios de acuerdo con los siguientes

CLÁUSULAS

Objeto

El ASESOR prestará al CLIENTE asesoramiento sobre las siguientes materias, lo que se concreta en la realización de los siguientes trabajos o servicios:

1. Asesoramiento e información en materia social y laboral en los aspectos que sean exigidos por la legislación social.

2. Redactar y diligenciar, en su caso, ante los Organismos competentes, los documentos sociales y laborales del CLIENTE.

3. Redactar y tramitar altas y bajas de los trabajadores, confeccionar las nóminas de salarios, liquidaciones en la Seguridad Social, contratos de trabajo generales y especiales con asesoramiento sobre la legislación vigente para cada modalidad. La tramitación podrá realizar por vía telemática, si así se acuerda entre las partes.

4. Previo acuerdo de las partes, el ASESOR y con cargo al CLIENTE podrá facilitar y diligenciar los libros de visita, suscripción de pólizas con Cías Aseguradoras, convenios con Mutuas de Accidentes, programas de Seguridad e Higiene, así como cuantos servicios de carácter social complementarios de los anteriores pueda precisar.

5. Las partes podrán acordar, al margen del precio del presente contrato, la representación y defensa en Actos de Conciliación y Tribunales de lo Social, Inspección de Trabajo, expedientes de crisis y regulación de plantilla, así como la redacción de informes o dictámenes jurídicos en el ámbito social-laboral.

Honorarios

La cuota de honorarios será de [IMPORTE] euros, más el IVA que corresponda legalmente, y será revisable cada año en caso de producirse la prórroga del contrato. De no establecerse pacto en contrario, dichos honorarios se verán incrementados anualmente en el porcentaje del IPC del sector servicios correspondiente al año anterior.

En los citados honorarios no están incluidos aquellos servicios que, por tener determinada entidad, superan el marco de la asesoría continuada sobre cuestiones ordinarias al igual que los trabajos propiamente jurídicos, aunque tengan relación con ellos.

No obstante la cuota fijada, cuando se realicen trabajos de duración extraordinaria y jurídicos, podrá acordarse de que se facturen independientemente según las tarifas de honorarios orientativas del Colegio

Pago

El pago del precio estipulado en el pacto anterior, se realizará por ingreso/transferencia/recibo domiciliado en la cuenta número [NÚMERO] de la entidad [DENOMINACIÓN SOCIAL] cuyo titular es

Dichos ingresos deberán realizarse en los diez primeros días de cada mes/trimestre/año de vigencia del contrato.

La falta de pago de cualquiera de las mensualidades / pagos trimestrales o anuales dará derecho al ASESOR a resolver el contrato y, si lo estimara oportuno, a proceder a su reclamación judicial, aplicándose desde la fecha del incumplimiento el interés de demora establecido en la Ley.

Duración del contrato

Los servicios y funciones descritos en el pacto anterior se prestarán por parte del ASESOR por un plazo inicial de [Nº] meses (desde la firma hasta el 31 de diciembre), que se renovará tácitamente por periodos anuales, de no mediar preaviso, al menos, con un mes de antelación a su término.

En el supuesto de no renovación del contrato, el ASESOR se obliga a la confección y/o presentación de la declaraciones fiscales correspondientes al ejercicio anterior.

Obligaciones del Cliente

Son obligaciones del cliente las siguientes:

1. Facilitar al ASESOR toda la documentación necesaria, en los plazos y periodicidad que, en cada caso se acuerde, para la adecuada prestación de los servicios.

2. Formular las consultas o visitas en las horas establecidas al efecto.

3. Efectuar en plazo el pago de los honorarios.

4. No efectuar gestiones ante los organismos sociales sin previo conocimiento del ASESOR. En especial, ante cualquier requerimiento de la Inspección de Trabajo, se abstendrá de hacer gestión alguna hasta tanto haya contactado con el ASESOR.

5. El CLIENTE no podrá solicitar al ASESOR ni asesoramiento ni colaboración en la realización de acciones u omisiones fraudulentas o tendentes a eludir la declaración y/o pago de sus obligaciones sociales legalmente obligatorias.

Responsabilidades

El CLIENTE responde de la exactitud de los datos que facilite al ASESOR para la realización del servicio contratado, que deberán ser completos y entregados dentro de plazo. De las consecuencias que se deriven por causa de que los datos facilitados por el CLIENTE sean incompletos, insuficientes o se entreguen fuera de plazo no será responsable el ASESOR.

El trabajo a realizar por el ASESOR no debe considerarse como sustitutivo del trabajo habitual del CLIENTE en relación al cumplimiento de sus obligaciones tributarias, ni sobre las decisiones finales en materia tributaria que serán, en todo caso, adoptadas por el CLIENTE.

Confidencialidad

El ASESOR se obliga a tratar confidencialmente todos aquellos datos, documentación y demás información que hayan sido suministrados por el CLIENTE durante la vigencia del presente contrato. Asimismo se compromete a no comunicar esta información a ninguna otra persona o entidad, exceptuando sus propios empleados y sólo en la medida necesaria para la correcta ejecución del contrato.

El acuerdo de confidencialidad establecido en el presente pacto tendrá validez durante la vigencia del contrato y seguirá en vigor, al menos, durante 5 años más después de la extinción, por cualquier causa, del mismo.

Lo contenido en este contrato no obligará a confidencialidad en lo referente a:

• Cualquier información o conocimiento revelado legítimamente por terceros que hayan autorizado su difusión.

• Cuando la información sea requerida por imperativo legal.

Protección de datos

El ASESOR informa al CLIENTE de que los datos personales contenidos en el presente contrato y los generados por la prestación del servicio, todos ellos relativos al CLIENTE, serán incorporados a un fichero cuyo responsable es [NOMBRE DE LA PARTE] con la finalidad de prestar el servicio, entendiendo que la firma del presente contrato implica su consentimiento para llevar a cabo dicho tratamiento.

El CLIENTE tiene la posibilidad de ejercitar los derechos de acceso, rectificación, cancelación y oposición, en relación a sus datos personales, dirigiendo un escrito a la dirección del ASESOR indicada en el encabezamiento del presente contrato.

Respecto de los datos personales a los que el ASESOR tenga acceso como consecuencia de la prestación del servicio, se entenderán facilitados de forma voluntaria por el CLIENTE, y sólo serán utilizados con la finalidad de prestar aquél, siguiendo en todo momento las instrucciones del CLIENTE, comprometiéndose el ASESOR a no aplicarlos ni utilizarlos para finalidad distinta de la pactada y a no comunicarlos a otras personas, así como a destruir los soportes y/o documentos donde se contengan dichos datos al finalizar el presente contrato, salvaguardando en todo caso las pruebas necesarias respecto a las actuaciones realizadas. En todo caso, los papeles de trabajo y el diseño o sistema de análisis serán propiedad del ASESOR.

Asimismo, ambas partes se comprometen a adoptar las necesarias medidas de seguridad para la protección de dichos datos en el nivel que les corresponda de acuerdo a la regulación legal.

Igualmente le informa de que, en ocasiones, el cumplimiento del presente contrato podrá implicar la cesión de datos personales a la Hacienda Pública para la consecución de la prestación del servicio arriba indicado, de acuerdo en todo caso con lo dispuesto en la normativa legal, y de forma específica en la Ley Orgánica 3 / 2018, de 5 de diciembre, de Protección de Datos de Personales y Garantía de los Derechos Digitales y en la Ley General Tributaria.

Si tal cesión se produjera previo requerimiento de la Administración Tributaria, el ASESOR lo comunicará de forma inmediata al CLIENTE.

Compatibilidad

El ASESOR aquí interviniente declara que no se encuentra afectado por ninguna causa legal que le impida asumir el trabajo encomendado.

Autorización para subcontratación

La prestación de servicios deberá ser realizado por EL ASESOR con los medios personales y materiales integrantes de su propia organización empresarial, utilizando vehículos de los que disponga en tal concepto.

No obstante, cuando precise de la colaboración de otro profesional, no quedará desvirtuada su condición de prestador de servicios único frente a EL CLIENTE.

En todo caso, las personas a quienes subcontrate habrán de reunir las condiciones y preparación adecuadas para la prestación de servicios encomendada.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Jurisdicción competente y ley aplicable

El conocimiento de los litigios relativos a que diera lugar la interpretación y/o ejecución del presente contrato corresponderá al Tribunal de Instancia del lugar en que se halle la finca.

El presente contrato tiene carácter civil, se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE PRESTACIÓN DE SERVICIOS DE ASESORÍA LABORAL, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(EL ASESOR)

Fdo. Don [NOMBRE Y APELLIDOS]

(EL CLIENTE)

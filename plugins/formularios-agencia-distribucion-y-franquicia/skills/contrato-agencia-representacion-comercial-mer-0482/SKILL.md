---
name: contrato-agencia-representacion-comercial-mer-0482
description: "Contrato de agencia o representación comercial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de agencia o representación comercial

> Formulario **MER-0482** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de agencia o representación comercial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de agencia o representación comercial” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-agencia-representacion-comercial-mer-0482`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] PROVINCIA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] INSCRIPCIÓN
- [ ] INSTITUCIÓN ARBITRAL
- [ ] INSTITUCIÓN DE MEDIACIÓN
- [ ] MES
- [ ] NÚMERO
- [ ] PRODUCTOS FABRICADOS
- [ ] TELÉFONO
- [ ] ZONA GEOGRÁFICA

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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NÚMERO], dirección de correo electrónico, teléfono móvil

Y de otra parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA] provisto/a del N.I.F, dirección de correo electrónico, teléfono móvil [TELÉFONO].

INTERVIENEN

D./Dª [NOMBRE Y APELLIDOS], interviene en su propio nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], NIF, con los datos expresados anteriormente, en adelante el REPRESENTANTE.

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF, domiciliada en y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], dirección de correo electrónico, teléfono móvil, en adelante la REPRESENTADA.

MANIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE REPRESENTACIÓN COMERCIAL, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que el REPRESENTANTE desempeña la actividad profesional de representación comercial en la zona geográfica de [ZONA GEOGRÁFICA]

II. Que la REPRESENTADA se dedica a la fabricación de [PRODUCTOS FABRICADOS] y desea promover la venta de sus productos y los servicios relacionados con los mismos, en la zona geográfica de desarrollo de la actividad del REPRESENTANTE.

III. Que conviniendo ambas partes en concertar el contrato, otorgan a tal fin el presente CONTRATO DE REPRESENTACIÓN COMERCIAL, en base a las siguientes

CLÁUSULAS

PRIMERA.- OBJETO DEL CONTRATO

El objeto del presente contrato es la promoción y conclusión de actos y operaciones de comercio por parte del REPRESENTANTE, por cuenta y en nombre de la REPRESENTADA, respecto de los bienes y servicios descritos en el expositivo II en la zona geográfica de…………………

El REPRESENTANTE actuara de forma independiente, sin vinculación laboral con la REPRESENTADA, organizando su actividad conforme a sus propios criterios.

El REPRESENTANTE realizará, por sí mismo o por medio de sus dependientes, la promoción y la conclusión de los actos u operaciones de comercio encomendadas, quedando autorizado por la REPRESENTADA para que concluya las operaciones en su nombre.

SEGUNDA.- ÁMBITO TERRITORIAL Y DURACIÓN DEL CONTRATO

El ámbito territorial de este contrato es la zona geográfica de actuación del REPRESENTANTE expresada en el expositivo I.

El contrato se pacta por tiempo indefinido. Ello, no obstante, transcurrido el primer año de vigencia, cualquiera de las partes podrá extinguir el contrato por denuncia unilateral, mediante comunicación escrita y siempre que observe un plazo de preaviso de seis meses.

TERCERA.- RETRIBUCIÓN Y FORMA DE PAGO

El REPRESENTANTE percibirá una retribución fija de [IMPORTE] euros mensuales, más una comisión en función del valor de los actos y operaciones promovidas y concluidas por el REPRESENTANTE.

La comisión será de un % del importe neto total, excluidos impuestos, de los actos y operaciones promovidos por cuenta de la REPRESENTADA, cuando se hayan concluido como consecuencia de la intervención profesional del agente en la zona geográfica objeto de este contrato.

La comisión se devengará en el momento en que la REPRESENTADA ejecute el acto u operación de comercio y se liquidará el último día de cada mes. La comisión se pagará no más tarde del día 10 del mes siguiente al de su devengo.

A efectos informativos, la REPRESENTADA entregará al REPRESENTANTE una relación de las comisiones devengadas por cada acto u operación, el último día del mes siguiente al que se hubieran devengado. En la relación se consignarán los elementos esenciales en base a los que haya sido calculado el importe de las comisiones. Asimismo, la REPRESENTADA se compromete a informar de cuantos datos sean precisos, incluso mediante exhibición de la contabilidad, para verificar todo lo relativo a las comisiones que le correspondan al REPRESENTANTE.

La remuneración pactada satisface todas las obligaciones económicas, de modo que el REPRESENTANTE no tendrá derecho al reembolso de los gastos que le hubiera originado el ejercicio de su actividad profesional.

QUINTA.- OBLIGACIONES DEL REPRESENTANTE

El REPRESENTANTE se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, actuando lealmente y de buena fe en interés de la REPRESENTADA, y en especial asume las siguientes obligaciones:

- Ocuparse con la diligencia de un ordenado comerciante de la promoción y conclusión de los actos u operaciones que se le hubieren encomendado.

- Comunicar a la entidad REPRESENTADA toda la información de que disponga, cuando sea necesaria para la buena gestión de los actos u operaciones cuya promoción y conclusión se le hubiere encomendado, así como, en particular, la relativa a la solvencia de los terceros con los que existan operaciones pendientes de conclusión o ejecución.

- Desarrollar su actividad con arreglo a las instrucciones razonables recibidas del empresario, siempre que no afecten a su independencia.

- Recibir en nombre de la REPRESENTADA cualquier clase de reclamaciones de terceros sobre defectos o vicios de calidad o cantidad de los bienes vendidos y de los servicios prestados como consecuencia de las operaciones promovidas, aunque no las hubiera concluido.

- Llevar una contabilidad independiente de los actos u operaciones relativos a la REPRESENTADA.

-Informar a la REPRESENTADA con periodicidad trimestral del curso de las operaciones en proyecto o realizadas en el ámbito de la representación comercial pactada en este contrato.

SEXT A.- OBLIGACIONES DE LA REPRESENTADA

La REPRESENTADA se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, actuando con lealtad y de buena fe con el REPRESENTANTE y en especial asume las siguientes obligaciones:

- Poner a disposición del REPRESENTANTE, con antelación suficiente y en cantidad apropiada, los muestrarios, catálogos, tarifas y demás documentos necesarios para el ejercicio de su actividad profesional.

- Procurar al REPRESENTANTE todas las informaciones necesarias para la ejecución del contrato.

- Advertir al REPRESENTANTE, desde que tenga noticia de ello, de sus previsiones sobre el volumen de los actos u operaciones encomendados.

- Satisfacer la remuneración pactada.

- Comunicar al REPRESENTANTE en el plazo más breve posible la aceptación o el rechazo de las operaciones comunicadas y del estado de su ejecución.

SÉPTIMA.- PROHIBICIÓN DE COMPETENCIA

El REPRESENTANTE se obliga a no prestar servicios de igual o similar naturaleza a empresas que directa o indirectamente realicen actividades empresariales concurrentes o competidoras durante la vigencia del presente contrato, ni podrá participar directa o indirectamente en empresas que realicen actividades comerciales relacionadas con bienes o servicios de análoga naturaleza al ámbito de este contrato.

Este pacto se extenderá a los dos años siguientes a la extinción del contrato, salvo que fuera resuelto por incumplimiento imputable a la REPRESENTADA, periodo en el cual el REPRESENTANTE no podrá desempeñar actividades de representación comercial en la zona geográfica delimitada en este contrato respecto de la clase de bienes o de servicios objeto del mismo.

OCTAVA.- CAUSAS DE RESOLUCIÓN Y EXTINCIÓN DEL CONTRATO

El incumplimiento por cualquiera de las partes de cualquiera de las obligaciones estipuladas, facultará a la parte contraria a resolver de forma inmediata el presente contrato o exigir su cumplimiento, sin perjuicio de la indemnización de daños y perjuicios que proceda en ambos casos.

En especial, cualquiera de las partes podrá dar por finalizado el contrato en cualquier momento, sin necesidad de preaviso, en los siguientes casos:

Cuando la otra parte hubiere incumplido, total o parcialmente, las obligaciones legal o contractualmente establecidas.
Cuando la otra parte hubiere sido declarada en concurso.

Asimismo, se pacta como causa de extinción la muerte o declaración de fallecimiento del REPRESENTANTE.

NOVENA.- INDEMNIZACIONES POR EXTINCIÓN ANTICIPADA

Cuando se extinga el contrato por causa no imputable al REPRESENTANTE y si éste hubiese aportado nuevos clientes al empresario o incrementado sensiblemente las operaciones con la clientela preexistente, tendrá derecho a una indemnización equivalente al importe medio de dos meses de retribución por cada año de vigencia del contrato, con un máximo de veinticuatro mensualidades.

Este derecho a la indemnización por clientela existe también en el caso de que el contrato se extinga por muerte o declaración de fallecimiento del REPRESENTANTE.

Estas indemnizaciones no procederán cuando la causa de extinción sea la edad, la invalidez o la enfermedad del REPRESENTANTE, por no poder continuar sus actividades

DÉCIMA.- APLICACIÓN DE LOS PRINCIPIOS UNIDROIT (representación comercial internacional)

Ambas partes manifiestan conocer los principios UNIDROIT del Instituto Internacional para la Unificación del Derecho Privado, que regulan las reglas generales referidas a contratos comerciales internacionales, conviniendo su aplicación al presente contrato en todo lo que no esté expresamente estipulado.

UNDÉCIMA.- NOTIFICACIONES

Toda notificación que se efectúe entre las partes se hará preferentemente en las direcciones de correo electrónico que figuran en el encabezamiento, sin perjuicio de que también puedan ser realizadas en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de dirección de correo electrónico y/o de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

NOVENA.- SUMISIÓN A MEDIACIÓN Y/O ARBITRAJE

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación (en su caso se citará la institución) de [INSTITUCIÓN DE MEDIACIÓN], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y (caso de fijar un plazo máximo....) fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

( en su caso, pacto de arbitraje...) A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de [INSTITUCIÓN ARBITRAL], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

Fdo.: Fdo.:

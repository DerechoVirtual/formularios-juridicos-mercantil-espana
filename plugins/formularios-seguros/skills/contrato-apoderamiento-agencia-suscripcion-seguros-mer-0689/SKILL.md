---
name: contrato-apoderamiento-agencia-suscripcion-seguros-mer-0689
description: "Contrato de apoderamiento a una agencia de suscripción de seguros. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de apoderamiento a una agencia de suscripción de seguros

> Formulario **MER-0689** del plugin **Seguros: pólizas, coberturas y reclamaciones** (`formularios-seguros`) · Mercantil › Seguros · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de apoderamiento a una agencia de suscripción de seguros» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de apoderamiento a una agencia de suscripción de seguros” para mi caso». También puedes invocarla directamente con `/formularios-seguros:contrato-apoderamiento-agencia-suscripcion-seguros-mer-0689`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguros:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguros: pólizas, coberturas y reclamaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (11 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (3 veces)
- [ ] PROVINCIA (3 veces)
- [ ] ASEGURADORA (2 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] INSCRIPCIÓN (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] MES
- [ ] PORCENTAJE

## Normas que cita el formulario

- art. 60 Ley 20/2015

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

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NÚMERO],

Y de otra parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NÚMERO],

INTERVIENEN

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la aseguradora [ASEGURADORA], CIF, domiciliada en [DOMICILIO] y constituida en [LOCALIDAD] ante Notario de [LOCALIDAD] D./Dª [NOMBRE Y APELLIDOS], en fecha [FECHA] e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], dirección de correo electrónico [CORREO ELECTRÓNICO], teléfono móvil [TELÉFONO], en adelante la ASEGURADORA.

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la agencia de suscripción de seguros [ASEGURADORA], CIF, domiciliada en [DOMICILIO] y constituida en [LOCALIDAD] ante Notario de [LOCALIDAD] D./Dª [NOMBRE Y APELLIDOS], en fecha [FECHA] e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], dirección de correo electrónico [CORREO ELECTRÓNICO], teléfono móvil [TELÉFONO], en adelante la AGENCIA.

MANIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE APODERAMIENTO DE AGENCIA DE SUSCRIPCIÓN DE SEGUROS, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que la ASEGURADORA actúa en los ramos de actividad de [ACTIVIDAD], estando interesada en contratar con una agencia de suscripción para operar en el mercado español.

II. Que la AGENCIA es una agencia de suscripción de seguros española autorizada por la Dirección General de Seguros y Fondos de Pensiones, que está interesada en actuar como apoderada de la ASEGURADORA para la suscripción de riesgos en su nombre y por su cuenta.

III. El presente contrato se otorga en el ámbito de lo establecido en el art. 60 de la Ley 20/2015, de 14 de julio, de ordenación, supervisión y solvencia de las entidades aseguradoras y reaseguradoras, reuniendo ambas partes todos los requisitos necesarios para el desarrollo de su actividad mercantil y para concertar el presente contrato.

IV. Que, conviniendo ambas partes en concertar el contrato, otorgan a tal fin el presente CONTRATO DE APODERAMIENTO DE AGENCIA DE SUSCRIPCIÓN, en base a las siguientes

CLÁUSULAS

PRIMERA.- OBJETO DEL CONTRATO

El objeto del presente contrato es el de apoderamiento por parte de la ASEGURADORA a la AGENCIA para la suscripción de riesgos en su nombre y por su cuenta en todos los ramos de su actividad.

El apoderamiento otorgado a la AGENCIA para actuar en nombre y representación de la aseguradora alcanza a todas las actuaciones necesarias para concertar contratos de seguro en su nombre y representación, incluyendo las facultades de analizar el riesgo a asegurar, determinación de coberturas, decidir sobre la aceptación y suscripción del riesgo, así como preparar y emitir el contrato de seguro, gestionar el cobro de la prima, la administración del contrato de seguro, así como las facultades para la tramitación, gestión, negociación y liquidación de siniestros cuya cuantía no exceda de [IMPORTE] euros.

SEGUNDA.- ÁMBITO TERRITORIAL Y DURACIÓN DEL CONTRATO

El ámbito territorial del contrato alcanza a todo el territorio español.

El contrato se pacta por tiempo indefinido. Ello no obstante, transcurridos los diez primeros años de vigencia, cualquiera de las partes podrá extinguir el contrato por denuncia unilateral, mediante comunicación escrita y siempre que observe un plazo de preaviso de un año.

En este caso en que se extinga el contrato de forma unilateral, la parte que la efectúe deberá indemnizar a la otra parte en el equivalente al importe medio de un mes de retribución por cada año de vigencia del contrato.

TERCERA.- RETRIBUCIÓN Y FORMA DE PAGO

La remuneración del AGENCIA consistirá en una comisión de [PORCENTAJE] % del importe neto total, excluidos impuestos, de los actos y contratos concertados por cuenta de la ASEGURADORA, que será abonada con cargo a la liquidación que se efectúe mensualmente.

La comisión se devengará en las liquidaciones que se deben realizar mensualmente sobre el neto de las primas percibidas, una vez detraídos los importes satisfechos por la AGENCIA por causas de siniestro.

La AGENCIA remitirá a la ASEGURADORA el día [FECHA] de cada mes, coincidiendo con la fecha de pago, una liquidación de las comisiones devengadas por las operaciones correspondientes a dicho período mensual.

La remuneración pactada satisface todas las obligaciones económicas, de modo que la AGENCIA no tendrá derecho al reembolso de los gastos que le hubiera originado el ejercicio de su actividad profesional.

CUARTA.- OBLIGACIONES DE LA AGENCIA

La AGENCIA se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, actuando lealmente y de buena fe en interés de la ASEGURADORA, y en especial asume las siguientes obligaciones:

- Expresar en toda la documentación mercantil de suscripción de seguros y publicidad, administración del contrato y gestión de riesgos su naturaleza de agencia de suscripción y la ASEGURADORA en nombre de la que se actúa.

- Cumplir las directrices o estándares de servicio fijadas por la ASEGURADORA para sus agencias, e incluir las condiciones de calidad aprobadas por la misma en los contratos que pueda suscribir la AGENCIA con corredores o sociedades de correduría de seguros.

- Informar a la ASEGURADORA de las cuestiones que puedan serle formuladas por la misma, entregar cualquier información que pudiera solicitarle y permitir que examine los documentos pertinentes caso de estimarlo necesario.

- Remitir con la mayor diligencia al departamento de atención al cliente de la ASEGURADORA las quejas o reclamaciones presentadas por cualquier persona en relación con la actuación de la AGENCIA.

- Llevar una contabilidad independiente de los actos u operaciones relativos a la ASEGURADORA.

- A responder frente a la ASEGURADORA por los daños y perjuicios que ésta haya tenido que indemnizar a terceros, como consecuencia de la actuación culpable o negligente de la AGENCIA.

QUINT A.- OBLIGACIONES DE LA ASEGURADORA

La ASEGURADORA se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, actuando con lealtad y de buena fe con la AGENCIA y en especial asume las siguientes obligaciones:

- Asumir directamente las coberturas de los riesgos contratados por la AGENCIA.

- Procurar a la AGENCIA todas las informaciones necesarias para la ejecución del contrato. Especialmente, la ASEGURADORA estará obligada a proporcionar información continua e inmediata sobre los productos y promociones que oferte en el mercado.

- Satisfacer la remuneración pactada.

- Comunicar a la AGENCIA en el plazo más breve posible la resolución de cualesquiera reclamaciones, quejas o incidencias respecto de la actividad objeto de este contrato.

SÉXTA.- DEBER DE CONFIDENCIALIDAD

Ambas partes se obligan a no revelar, ceder o transferir a terceros ninguna información confidencial referente a este contrato o cualquier otro aspecto relacionado con la actividad de las entidades que pueda conocer o haya conocido con motivo de la prestación de servicios prevista en el presente contrato.

SÉPTIMA.- CAUSAS DE RESOLUCIÓN Y EXTINCIÓN DEL CONTRATO

El incumplimiento por cualquiera de las partes de cualquiera de las obligaciones estipuladas facultará a la parte contraria a resolver de forma inmediata el presente contrato o exigir su cumplimiento, sin perjuicio de la indemnización de daños y perjuicios que proceda en ambos casos.

En especial, cualquiera de las partes podrá dar por finalizado el contrato en cualquier momento, sin necesidad de preaviso, en los siguientes casos:

Cuando la otra parte hubiere incumplido gravemente, total o parcialmente, las obligaciones legal o contractualmente establecidas.
Cuando la otra parte hubiere sido declarada en concurso.

OCTAVA.- INDEMNIZACIÓN POR CLIENTELA

A la finalización del presente contrato, la AGENCIA tendrá derecho a percibir una cantidad de tres mensualidades del saldo medio que arrojen las comisiones percibidas a la fecha de extinción en concepto de indemnización por clientela.

No obstante, la AGENCIA perderá su derecho a ser indemnizado en los siguientes supuestos:

1. Cuando el contrato se hubiera resuelto o extinguido por voluntad unilateral de la AGENCIA o para causa que le sea imputable.

2. Cuando con consentimiento de la ASEGURADORA, la AGENCIA hubiese cedido sus derechos contractuales a otra agencia.

NOVENA.- ELEVACIÓN DEL DOCUMENTO A PÚBLICO, COMUNICACIONES E INSCRIPCIONES

Ambas partes convienen la elevación de este documento a escritura pública, a requerimiento de cualquiera de ellas, así como a realizar todas las comunicaciones, inscripciones y demás actuaciones necesarias para la plena eficacia de este contrato, tanto ante la Dirección General de Seguros como ante cualesquiera otros organismos públicos y privados.

DÉCIMA.- NOTIFICACIONES

Toda notificación que se efectúe entre las partes se hará preferentemente en las direcciones de correo electrónico que figuran en el encabezamiento, sin perjuicio de que también puedan ser realizadas en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de dirección de correo electrónico y/o de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo.: Fdo.:

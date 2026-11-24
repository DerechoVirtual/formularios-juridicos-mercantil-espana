---
name: contrato-colaboracion-mercantil-captacion-clientes-mer-0480
description: "Contrato de colaboración mercantil para la captación de clientes potenciales (leads). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de colaboración mercantil para la captación de clientes potenciales (leads)

> Formulario **MER-0480** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de colaboración mercantil para la captación de clientes potenciales (leads)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de colaboración mercantil para la captación de clientes potenciales (leads)” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-colaboracion-mercantil-captacion-clientes-mer-0480`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (11 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (4 veces)
- [ ] PROVINCIA (3 veces)
- [ ] ASEGURADORA (2 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] INSCRIPCIÓN (2 veces)
- [ ] NIF (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] ACTIVIDAD
- [ ] DENOMINACIÓN SOCIAL
- [ ] INSTITUCIÓN ARBITRAL
- [ ] Nº
- [ ] PORCENTAJE
- [ ] SUCURSAL

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

Y de otra parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NÚMERO],

INTERVIENEN

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la aseguradora [ASEGURADORA], CIF [NIF], domiciliada en [DOMICILIO] y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA] e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], dirección de correo electrónico [CORREO ELECTRÓNICO], teléfono móvil [TELÉFONO], en adelante la EMPRESA.

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la aseguradora [ASEGURADORA], CIF [NIF], domiciliada en [DOMICILIO] y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA] e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], dirección de correo electrónico [CORREO ELECTRÓNICO], teléfono móvil [TELÉFONO], en adelante la COLABORADORA.

MANIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE COLABORACIÓN MERCANTIL ENTRE EMPRESAS PARA LA CAPTACIÓN DE LEADS, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que la EMPRESA está dedicada a la actividad empresarial de [ACTIVIDAD], estando interesada en ampliar su línea de negocio.

II. Que la COLABORADORA se dedica profesionalmente al servicio de marketing, para la captación y comercialización con la venta leads (clientes potenciales) a entidades empresariales, profesionales y comerciales.

III. Que ambas partes convienen en concertar el contrato para la prestación de dichos servicios y otorgan a tal fin el presente CONTRATO DE COLABORACIÓN MERCANTIL ENTRE EMPRESAS PARA LA CAPTACIÓN DE LEADS, en base a las siguientes

CLÁUSULAS

PRIMERA.- OBJETO DEL CONTRATO

El objeto del presente contrato es la captación de LEADS (potenciales clientes) para la línea de negocio de la EMPRESA por medio de los servicios de marketing de la COLABORADORA.

Los LEADS serán exclusivos de la EMPRESA, sin que puedan ser suministrados por la COLABORADORA a otros clientes.

Los LEADS se pondrán a disposición de la EMPRESA por parte de la COLABORADORA con periodicidad mínima semanal.

SEGUNDA.- DURACIÓN

El contrato se pacta por tiempo indefinido. Ello no obstante, transcurrido el primer año de vigencia, cualquiera de las partes podrá extinguir el contrato por denuncia unilateral, mediante comunicación escrita y siempre que observe un plazo de preaviso de tres meses.

TERCERA.- RETRIBUCIÓN Y FORMA DE PAGO

La remuneración de la COLABORADORA consistirá en una comisión de [PORCENTAJE] % del importe neto total, excluidos impuestos, de la facturación que se realice por la EMPRESA a los LEADS suministrados por la COLABORADORA y que contraten sus servicios.

La comisión se devengará en las liquidaciones que se deben realizar mensualmente sobre los LEADS captados por la COLABORADORA, y se ingresará en la cuenta corriente núm. [Nº] que la COLABORADORA tiene abierta en la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL]

A este efecto, la EMPRESA se obliga a entregar a la COLABORADORA, el día [FECHA] de cada mes, coincidiendo con la fecha de pago, una relación de las comisiones devengadas por las operaciones correspondientes a dicho período mensual, especificando el porcentaje correspondiente a la comisión sobre la facturación neta de los LEADS.

La remuneración pactada satisface todas las obligaciones económicas derivadas de este contrato, de modo que la COLABORADORA no tendrá derecho al reembolso de los gastos que le hubiera originado el ejercicio de su actividad.

CUARTA.- OBLIGACIONES DE LA COLABORADORA

La COLABORADORA se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, actuando con diligencia, lealmente y de buena fe en interés de la EMPRESA, y en especial asume las siguientes obligaciones:

La COLABORADORA realizará con sus propios medios personales y material y bajo su propio riesgo y coste, la búsqueda y obtención de LEADS (clientes potenciales) para la EMPRESA, poniéndolos a su disposición en los términos pactados, y se responsabiliza del cumplimiento de la normativa sobre protección de datos.

La COLABORADORA correrá con los gastos publicitarios y de cualquier tipo que sean necesarios para su deber de captación del LEADS.
La COLABORADORA se compromete a realizar su trabajo con la mayor calidad posible, acudiendo a las fuentes necesarias de reconocido rigor y seriedad, y aplicando los métodos y conocimientos adecuados para que su trabajo de colaboración resulte del mayor rigor y eficacia según los cánones éticos profesionales más extendidos.
La COLABORADORA se obliga a no utilizar en beneficio propio o de terceros los conocimientos adquiridos sobre la clientela, proyectos, trabajos en ejecución y funcionamiento en general de LA EMPRESA, haciéndose responsable de cualquier perjuicio que el incumplimiento de esta estipulación acarrease a LA EMPRESA.

-La COLABORADORA seguirá su metodología de captación de LEADS, obligándose a prestar sus servicios con arreglo a las instrucciones razonables recibidas de la EMPRESA, siempre que no afecten a su independencia.

QUINT A.- OBLIGACIONES DE LA EMPRESA

La EMPRESA se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, actuando con diligencia, lealtad y de buena fe con la COLABORADORA, y en especial asume las siguientes obligaciones:

- La EMPRESA se obliga a practicar las liquidaciones, incluyendo las cantidades facturadas a los LEADS suministrados por la COLABORADORA conforme a lo pactado en la estipulación tercera, y a satisfacer puntualmente la remuneración pactada.

- La EMPRESA se obliga a no interferir en la estrategia comercial de la COLABORADORA, sin perjuicio del desarrollo de sus propias acciones comerciales respecto de los leads suministrados por la COLABORADORA en prestación de sus servicios, que en cualquier caso serán remunerados conforme a lo pactado en este contrato.

- La EMPRESA procurará a la COLABORADORA todas las informaciones necesarias para la ejecución del contrato.

- La EMPRESA suministrará a la COLABORADORA toda la documentación e información que fuera requerida por ésta para el correcto desarrollo y cumplimiento de los servicios y remuneraciones pactadas, y colaborará en cualquier solicitud de información o aclaración que le fuera requerida para la correcta prestación y liquidación de los servicios.

SEXTA.- DEBER DE CONFIDENCIALIDAD

La EMPRESA y la COLABORADORA se obligan a actuar con toda la discreción y reserva necesarias para mantener el secreto y confidencialidad de los trabajos realizados y relaciones económicas entre ambas, o con cualquiera de sus empresas colaboradoras o marcas comerciales.

Ambas partes manifiestan conocer los graves perjuicios que podrían ocasionarse por la falta de discreción en su trabajo y se comprometen a no revelar, bajo ningún concepto, a ninguna persona o entidad del tipo que fuere, la totalidad o parte de información relativa a los trabajos y relaciones objeto de este contrato.

La parte que infrinja el deber de confidencialidad y secreto será responsable de los perjuicios que la falta de cumplimiento de esta estipulación pudiese acarrear a la otra parte.

SÉPTIMA.- CAUSAS DE RESOLUCIÓN Y EXTINCIÓN DEL CONTRATO

El incumplimiento por cualquiera de las partes de cualquiera de las obligaciones estipuladas, facultará a la parte contraria a resolver de forma inmediata el presente contrato o exigir su cumplimiento, sin perjuicio de la indemnización de daños y perjuicios que proceda en ambos casos.

En especial, cualquiera de las partes podrá dar por finalizado el contrato en cualquier momento, sin necesidad de preaviso, en los siguientes casos:

Cuando la otra parte hubiere incumplido, total o parcialmente, las obligaciones legal o contractualmente establecidas.
Cuando la otra parte hubiere sido declarada en concurso.

OCTAVA.- INDEMNIZACIONES POR EXTINCIÓN ANTICIPADA

Cuando se extinga el contrato por causa no imputable a la COLABORADORA, y si se hubiesen incrementado en más de un 50% las operaciones comerciales como consecuencia de la prestación de sus servicios, tendrá derecho a una indemnización equivalente al importe medio de dos meses de retribución por cada año de vigencia del contrato, con un máximo de veinticuatro mensualidades.

NOVENA.- NOTIFICACIONES Y COMUNICACIONES

Toda notificación, requerimiento y/o comunicación que se efectúe entre las partes se hará preferentemente en las direcciones de correo electrónico que figuran en el encabezamiento, sin perjuicio de que también puedan ser realizadas en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de dirección de correo electrónico y/o de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

DÉCIMA.- SUMISIÓN A MEDIACIÓN Y/O ARBITRAJE

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación (en su caso se citará la institución) de., antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y (caso de fijar un plazo máximo....) fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

( en su caso, pacto de arbitraje...) A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de [INSTITUCIÓN ARBITRAL], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

Fdo.: Fdo.:

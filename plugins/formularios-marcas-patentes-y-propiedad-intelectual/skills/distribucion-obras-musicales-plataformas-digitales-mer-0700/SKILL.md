---
name: distribucion-obras-musicales-plataformas-digitales-mer-0700
description: "Distribución de obras musicales en plataformas digitales (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Distribución de obras musicales en plataformas digitales (contrato)

> Formulario **MER-0700** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Distribución de obras musicales en plataformas digitales (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Distribución de obras musicales en plataformas digitales (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:distribucion-obras-musicales-plataformas-digitales-mer-0700`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] PROVINCIA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] INSCRIPCIÓN
- [ ] INSTITUCIÓN ARBITRAL
- [ ] INSTITUCIÓN DE MEDIACIÓN
- [ ] NÚMERO

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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [DÍA] de del año [AÑO]

REUNIDOS

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NÚMERO], dirección de correo electrónico, teléfono móvil

Y de otra parte D./Dª [NOMBRE Y APELLIDOS]., mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA]. provisto/a del N.I.F..

INTERVIENEN

D./Dª [NOMBRE Y APELLIDOS], interviene en su propio nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], NIF, con los datos expresados anteriormente, en adelante el AUTOR.

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF, domiciliada en y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D./Dª [NOMBRE Y APELLIDOS], en fecha e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], dirección de correo electrónico, teléfono móvil, en adelante LA DISTRIBUIDORA.

MENIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE DISTRIBUCIÓN DE OBRAS MUSICALES EN PLATAFORMAS DIGITALES, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que el AUTOR es titular de todos los derechos de propiedad intelectual de las obras musicales cuyas características se especifican en el Anexo número 1.

II. Que la DISTRIBUIDORA es una sociedad mercantil que tiene como objeto la distribución de música digital, mediante las herramientas tecnológicas idóneas para procesar los archivos musicales y distribuirlos en las plataformas de streaming.

III. Que conviniendo ambas partes en concertar el contrato, otorgan a tal fin el presente CONTRATO DE DISTRIBUCIÓN DE OBRAS MUSICALES EN PLATAFORMAS DIGITALES, en base a las siguientes

CLÁUSULAS

PRIMERA.- OBJETO DEL CONTRATO

El objeto del presente contrato es la cesión no exclusiva por el AUTOR a la DISTRIBUIDORA de los derechos de distribución, reproducción y comunicación pública de las obras relacionadas en el Anexo I, para su comercialización a través de las plataformas digitales de distribución.

El contrato autoriza a la DISTRIBUIDORA a distribuir, en formato digital, las obras objeto de cesión para el listado de plataformas y servicios de internet recogidos en el Anexo II de este contrato.

A estos efectos, el AUTOR autoriza expresamente a la DISTRIBUIDORA a realizar los actos de conversión de la obra a los correspondientes formatos digitales y la incorporación, en su caso, de los necesarios sistemas de protección, en tanto sea necesario para la distribución y divulgación de la obra.

La DISTRIBUIDORA difundirá las obras del autor objeto de este contrato de forma diligente para su comercialización eficaz en las plataformas digitales y servicios de internet. A estos efectos, caso de no poder utilizarse alguna o algunas de las plataformas o servicios por causas ajenas a la voluntad de la DISTRIBUIDORA, se compromete a sustituirla por otra u otras de similar nivel de difusión.

SEGUNDA.- AMPLIACIÓN DEL OBJETO

Ambas partes, de común acuerdo, podrán ampliar el objeto del contrato a nuevas obras del autor.

A dicho efecto, el AUTOR remitirá sus obras a través del sitio web……… de la DISTRIBUIDORA, quien deberá responder en un plazo de quince días sobre la aceptación.

En caso de que la DISTRIBUIDORA no realizara ninguna comunicación, se entenderán aceptadas las obras remitidas, las cuales serán distribuidas con arreglo a lo pactado en este contrato.

TERCERA.- RETRIBUCIÓN Y FORMA DE PAGO

El AUTOR recibirá un porcentaje del .% del importe neto de las ventas de formatos digitales u otros que puedan desarrollarse por la DISTRIBUIDORA en el futuro, cualquiera que sea su naturaleza. Para calcular el importe neto se descontarán los impuestos.

La distribuidora informará con periodicidad trimestral al AUTOR del número de veces en las que la puesta a disposición de sus obras se haya hecho efectiva y del importe devengado. La comunicación se remitirá a la dirección de correo electrónico que figura en el encabezamiento.

El pago de las cantidades se realizará por la DISTRIBUIDORA dentro de los quince días siguientes al de la remisión de dicha comunicación.

El AUTOR tendrá derecho a comprobar los datos que le comunique la DISTRIBUIDORA y, a dicho efecto, ésta le facilitará el acceso a los contadores de las plataformas digitales encargadas de su puesta a disposición del público.

CUARTA.- DURACIÓN

El contrato tendrá una duración de………, el cual se prorrogará por igual plazo si ninguna de las partes manifiesta su voluntad en contrario.

Al efecto, cualquiera de las partes puede oponerse a la prórroga mediante comunicación a la otra parte con una antelación mínima de treinta días a la del vencimiento del contrato o de sus prórrogas.

CUARTA.- ÁMBITO TERRITORIAL

El ámbito territorial de este acuerdo es todo el mundo, llevándose a cabo la comercialización por las plataformas digitales y servicios de internet relacionados en el Anexo II, o los que les sustituyan conforme a lo pactado en este contrato.

QUINTA.- OBLIGACIONES DEL AUTOR

El AUTOR responde ante la DISTRIBUIDORA de la autoría y originalidad de su obra y del ejercicio de los derechos que cede mediante este contrato, se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, y en especial asume las siguientes obligaciones:

- A garantizar la pacífica explotación de los derechos cedidos, manifestando que no contraerá compromisos o gravámenes de ninguna especie que atenten contra la cesión de derechos a la DISTRIBUIDORA.

- A incluir los avisos y advertencias exigidos por la normativamente vigente sobre contenido explícito de las letras y de las obras objeto de gestión.

-A autorizar a la DISTRIBUIDORA al uso del nombre del AUTOR, de su biografía y demás elementos de sus derechos de imagen necesarios para la distribución de la obra.

- A informar a la DISTRIBUIDORA de las actividades del AUTOR que puedan entrar en conflicto con este contrato.

- A autorizar a la DISTRIBUIDORA al ejercicio de las acciones legales contra terceros respecto de las conductas que puedan suponer un perjuicio respecto de la gestión de los derechos cedidos en este contrato.

SEXT A.- OBLIGACIONES DE LA DISTRIBUIDORA

La DISTRIBUIDORA se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, y en especial asume las siguientes obligaciones:

- A gestionar diligentemente la explotación digital de las obras del autor objeto de este contrato y a comercializarlas de forma eficaz en las plataformas digitales y servicios de internet, buscando su más amplia difusión conforme a los usos habituales.

- A sustituir de forma inmediata la plataformas o servicios en los que intermedia por otros de difusión equivalente en caso de interrumpirse, suspenderse o extinguirse el servicio en alguno o algunos de los relacionados en el Anexo II.

- Al empleo de los estándares de calidad en la explotación digital de las obras objeto de este contrato.

- Al estricto respeto a los derechos del AUTOR, especialmente el derecho a la integridad de sus obras.

- A conservar y facilitar toda la información necesaria para la debida comprobación de los datos relativos a la explotación cubierta por este contrato de acuerdo a lo estipulado en la cláusula tercera.

- A no transmitir los derechos de cesión a terceros, sin consentimiento escrito del AUTOR.

SÉPTIMA.- CAUSAS DE RESOLUCIÓN ANTICIPADA

El incumplimiento por cualquiera de las partes de cualquiera de las obligaciones estipuladas, facultará a la parte contraria a resolver de forma inmediata el presente contrato o exigir su cumplimiento, sin perjuicio de la indemnización de daños y perjuicios que proceda en ambos casos.

En especial, se pacta como causa de resolución anticipada del contrato, el incumplimiento de las obligaciones de pago y de información por parte de la DISTRIBUIDORA. Adicionalmente, se producirá una reversión automática de los derechos cedidos en méritos del presente contrato a favor del AUTOR.

Asimismo, el contrato se resolverá anticipadamente por el ejercicio de acciones por terceros sobre la autoría o derechos de cesión de la obra contra el AUTOR que puedan perturbar la explotación de los derechos cedidos.

OCTAVA.- NOTIFICACIONES

Toda notificación que se efectúe entre las partes se hará preferentemente en las direcciones de correo electrónico que figuran en el encabezamiento, sin perjuicio de que también puedan ser realizadas en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de dirección de correo electrónico y/o de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

NOVENA.- SUMISIÓN A MEDIACIÓN Y/O ARBITRAJE

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación (en su caso se citará la institución) de [INSTITUCIÓN DE MEDIACIÓN], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y (caso de fijar un plazo máximo....) fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

( en su caso, pacto de arbitraje...) A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de [INSTITUCIÓN ARBITRAL], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato y sus Anexos I y II, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

Fdo.: Fdo.:

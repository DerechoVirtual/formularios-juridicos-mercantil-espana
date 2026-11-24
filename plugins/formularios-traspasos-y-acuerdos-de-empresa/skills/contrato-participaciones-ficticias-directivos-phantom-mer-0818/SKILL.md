---
name: contrato-participaciones-ficticias-directivos-phantom-mer-0818
description: "Contrato de participaciones ficticias para directivos (phantom shares). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de participaciones ficticias para directivos (phantom shares)

> Formulario **MER-0818** del plugin **Traspasos de negocio, confidencialidad y acuerdos de empresa** (`formularios-traspasos-y-acuerdos-de-empresa`) · Mercantil › Otros documentos mercantiles · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de participaciones ficticias para directivos (phantom shares)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de participaciones ficticias para directivos (phantom shares)” para mi caso». También puedes invocarla directamente con `/formularios-traspasos-y-acuerdos-de-empresa:contrato-participaciones-ficticias-directivos-phantom-mer-0818`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-traspasos-y-acuerdos-de-empresa:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Traspasos de negocio, confidencialidad y acuerdos de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] Nº (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] PROVINCIA (3 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] INSCRIPCIÓN
- [ ] INSTITUCIÓN ARBITRAL
- [ ] INSTITUCIÓN DE MEDIACIÓN
- [ ] NIF/DNI
- [ ] OBJETO SOCIAL
- [ ] PLAZO
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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [FECHA]

REUNIDOS

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA] provisto/a del N.I.F, dirección de correo electrónico, teléfono móvil

Y de otra parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA] provisto/a del N.I.F. [NIF/DNI]

INTERVIENEN

D./Dª [NOMBRE Y APELLIDOS], interviene en su propio nombre, con los datos expresados anteriormente, en adelante el ALTO DIRECTIVO.

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF, domiciliada en…………… y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D./Dª [NOMBRE Y APELLIDOS], en fecha [FECHA] e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], dirección de correo electrónico [CORREO ELECTRÓNICO], teléfono móvil [TELÉFONO], en adelante la EMPRESA.

MANIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE PHATOM SHARE, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que el ALTO DIRECTIVO ostenta el cargo de Director General de la EMPRESA en virtud de contrato de alta dirección de fecha [FECHA]

II. Que la EMPRESA tiene como objeto social [OBJETO SOCIAL] y adopta la forma de sociedad de capital, con un capital social que se compone por un total de [Nº] acciones, cuyo valor nominal es de [IMPORTE] euros cada una.

III. Que ambas partes están interesadas en mantener la permanencia del ALTO DIRECTIVO en el EMPRESA e incentivar la consecución de objetivos, mediante la participación en la marcha económica de la empresa.

IV. Que, conviniendo ambas partes en concertar el contrato, otorgan a tal fin el presente CONTRATO DE PHANTOM SHARE, el cual se incluirá como documento anexo al contrato de alta dirección suscrito entre las partes, formando parte de éste, en base a las siguientes

CLÁUSULAS

PRIMERA.- OBJETO DEL CONTRATO

El objeto del presente contrato es la transmisión por parte de la EMPRESA al ALTO DIRECTIVO de un número de [Nº] acciones phantom share, sujeta al régimen jurídico y condiciones que se establecen a continuación, con la finalidad de incentivar la continuidad y esfuerzo individual del ALTO DIRECTIVO.

La transmisión de las acciones phantom share se realizará en tres fases: la primera en el momento de la firma de este contrato con un número de [Nº] acciones, y la segunda y la tercera en periodos trianuales (….), con un número de [Nº] acciones en cada una de estas dos fases, en todo caso vinculadas a la permanencia del ALTO DIRECTIVO en la empresa y a la consecución de los objetivos que se describen en el Anexo I del presente contrato.

La transmisión de las acciones supone una obligación de pago por parte de la EMPRESA al ALTO DIRECTIVO, con carácter de retribución variable en efectivo en concepto de dividendo, o por incentivos, o ligada al valor de transmisión de la Sociedad, en el caso de que tenga lugar la transmisión de la EMPRESA mediante un “supuesto convencional de transmisión” definido en la cláusula tercera.

SEGUNDA.- RÉGIMEN JURÍDICO DE LAS ACCIONES DEL CONTRATO PHANTOM SHARE

Las Acciones del Phantom Stock Plan, se definen como participaciones virtuales en el capital social de la Sociedad, que confieren los mismos derechos económicos que a los accionistas, cuyo valor efectivo vendrá determinado por el Valor de Transmisión, una vez llegado un “supuesto convencional de transmisión”.

Las Acciones del phantom share son virtuales y representan un derecho a percibir dividendos anuales de forma equivalente a los accionistas y a participar en el Valor de Transmisión de la Sociedad en el caso de que se produzca un “supuesto convencional de transmisión”.

Las acciones phantom share no dan a sus titulares el derecho de adquirir acciones en el capital social de la EMPRESA, ni serán convertibles en acciones en el capital social de la EMPRESA, ni en ningún otro instrumento asimilable a una participación en el capital social de la EMPRESA.

A los efectos de calcular la Remuneración, las acciones phantom share representan una participación en los beneficios y en el valor de transmisión de la EMPRESA cuyo importe efectivo viene determinado por el número de Acciones transmitidas al ALTO DIRECTIVO.

En caso de ampliación de capital, las acciones phantom share se ampliarán en el mismo porcentaje de incremento del capital social.

TERCERA.- REMUNERACIÓN

El ALTO DIRECTIVO percibirá la remuneración en concepto de dividendos por sus acciones phantom share en condiciones idénticas a las de los accionistas, garantizándose por la EMPRESA un dividendo mínimo anual de … euros por cada acción en caso de que se cumplan los objetivos establecidos en el Anexo I del presente contrato.

Asimismo, el ALTO DIRECTIVO participará en el valor de transmisión de la EMPRESA siempre que se produzca uno de los siguientes Eventos de Liquidez:

• La transmisión a título de compraventa o por cualquier otro título de al menos el cincuenta por ciento (50%) del capital social de la EMPRESA, a cualquier persona física o jurídica, sea o no accionista de la EMPRESA, siempre que, en las transmisiones a título distinto del de compraventa, la contraprestación obtenida por los transmitentes consista exclusivamente en dinero y/o acciones cotizadas en un mercado secundario organizado;

• La admisión a cotización en un mercado secundario organizado de al menos el cincuenta y uno por ciento (51%) de las acciones de la EMPRESA.

• La absorción de la EMPRESA por otra sociedad ya existente o de nueva creación en el marco de un proceso de fusión siempre que la contraprestación obtenida por los accionistas de la EMPRESA consista exclusivamente en dinero y/o acciones cotizadas en un mercado secundario organizado;

• La escisión total de la EMPRESA, siempre que la contraprestación obtenida por los accionistas de la EMPRESA consista exclusivamente en dinero y/o acciones cotizadas en un mercado secundario organizado; y

• La escisión parcial de la EMPRESA, siempre que la contraprestación obtenida por los accionistas de la EMPRESA consista exclusivamente en dinero y/o acciones cotizadas en un mercado secundario organizado y el patrimonio escindido constituya al menos el cincuenta por ciento (50%) del patrimonio total de la Sociedad en el momento de la escisión.

CUARTA.- VALOR DE TRANSMISIÓN DE LA EMPRESA

El valor de transmisión de la EMPRESA es la magnitud para determinar el importe de la remuneración cuanto tenga lugar un “supuesto convencional de transmisión” y estará constituido por la diferencia entre el valor actual y el valor de venta.

El valor de venta será fijado sobre la base del valor real de mercado de la EMPRESA en el momento del “supuesto convencional de transmisión”, el cual se determinará partiendo de las cantidades pagadas comprometidas con ocasión de un “supuesto convencional de transmisión” por cualquier persona física o jurídica, ya sean en efectivo o mediante la entrega de acciones cotizadas en un mercado secundario organizado, ponderando todas las circunstancias que sean relevantes para fijar el Valor de Transmisión.

El Valor actual de la EMPRESA es el que figura en el Anexo II del presente contrato, el cual será tomado como referencia, en su caso, para el cálculo de la remuneración correspondiente al valor de transmisión, el cual está constituida por la diferencia entre el valor actual y el valor de venta.

La EMPRESA determinará el valor de transmisión y, en caso de desacuerdo por el ALTO DIRECTIVO, por la EMPRESA se encargará a un auditor o a un experto independiente un dictamen dirimente sobre los aspectos que sean objeto de controversia, el cual será vinculante para ambas partes.

QUINTA.- MANTENIMIENTO DE LA CONDICIÓN DE BENEFICIARIO

Para tener derecho a percibir los beneficios económicos será necesario que, en el momento de cobrar los incentivos correspondientes, el ALTO DIRECTIVO continúe vinculado contractualmente a la Sociedad.

SEXTA.- PERCEPCIÓN DE DERECHOS CONSOLIDADOS

El ALTO DIRECTIVO percibirá los derechos ya adquiridos y consolidados derivados de las acciones phantom share en el momento en que la relación con la EMPRESA se extinga o finalice por fallecimiento, jubilación forzosa o por incapacidad permanente. En caso de fallecimiento, la EMPRESA abonará los derechos ya adquiridos y consolidados a los herederos.

En este caso, el ““supuesto convencional de transmisión”” a efectos del cálculo de la participación en el valor de transmisión se considerará producido el día del hecho causante.

SÉPTIM A.- PÉRDIDA DE LA CONDICIÓN DE BENEFICIARIO

En todo caso, el ALTO DIRECTIVO perderá su condición de beneficiario y, por lo tanto, perderá el derecho a la percepción de cualesquiera derechos económicos derivados del presente contrato en el supuesto de cese voluntario en la prestación de servicios a la EMPRESA, así como en el caso de desistimiento o terminación justificada de la relación a instancias de la EMPRESA.

OCTAVA.- INTRANSMISIBILIDAD DE LOS DERECHOS.

Las acciones phantom share constituyen un derecho personal e intransferible del ALTO DIRECTIVO. En ningún caso podrá ser objeto de enajenación y cesión a terceros.

NOVENA.- REVERSIÓN DE LAS ACCIONES

Transcurridos [Nº] años desde la celebración del contrato, la EMPRESA podrá adquirir todas o parte de las acciones phantom share del ALTO DIRECTIVO por un precio de [IMPORTE] euros por cada una de ellas.

Caso de que la EMPRESA no ejercite la opción de recompra a la finalización del periodo, y si se hubieran cumplido todos los objetivos de permanencia y económicos reflejados en el Anexo I del presente contrato, el ALTO DIRECTIVO tendrá derecho a una remuneración de [IMPORTE] euros por cada acción no revertida a la finalización del periodoaaa.

DÉCIMA.- PROHIBICIÓN DE COMPETENCIA

El ALTO DIRECTIVO no podrá participar en ninguna actividad económica por cuenta propia o ajena que directa o indirectamente suponga una situación de competencia para la EMPRESA en el plazo de [Nº] años desde la finalización de la relación contractual.

En caso de incurrir en prohibición de competencia, además de las consecuencias derivadas de la infracción, el ALTO DIRECTIVO deberá reintegrar todas las cantidades percibidas por derechos derivados de las acciones phantom share pactados en este contrato.

UNDÉCIMA.- CONFIDENCIALIDAD

Ambas partes manifiestan que toda la información recogida en este contrato es confidencial, y se comprometen a no difundirla y no dar acceso a la misma a terceros, salvo en los casos taxativamente establecidos en la Ley.

DUODÉCIMA.- NOTIFICACIONES

Toda notificación formal que se efectúe entre las partes se hará preferentemente en las direcciones de correo electrónico que figuran en el encabezamiento, sin perjuicio de que también puedan ser realizadas en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de dirección de correo electrónico y/o de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

NOVENA.- SUMISIÓN A MEDIACIÓN Y/O ARBITRAJE

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación (en su caso se citará la institución) de [INSTITUCIÓN DE MEDIACIÓN], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y (caso de fijar un plazo máximo [PLAZO]) fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

(en su caso, pacto de arbitraje) A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de [INSTITUCIÓN ARBITRAL], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato y sus Anexos I y II, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

Fdo.: Fdo.:

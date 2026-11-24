---
name: pacto-socios-modelo-mer-0009
description: "Pacto de socios (modelo). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Pacto de socios (modelo)

> Formulario **MER-0009** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Pacto de socios (modelo)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Pacto de socios (modelo)” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:pacto-socios-modelo-mer-0009`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] ACTIVIDAD (4 veces)
- [ ] PROVINCIA (4 veces)
- [ ] CORREO ELECTRÓNICO (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] TELÉFONO (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] FECHA
- [ ] INSTITUCIÓN ARBITRAL
- [ ] INSTITUCIÓN DE MEDIACIÓN
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

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NÚMERO], dirección de correo electrónico [CORREO ELECTRÓNICO], teléfono móvil [TELÉFONO] (en adelante SOCIO 1)

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NÚMERO], dirección de correo electrónico [CORREO ELECTRÓNICO], teléfono móvil [TELÉFONO] (en adelante SOCIO 2)

Y de otra parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NÚMERO], dirección de correo electrónico [CORREO ELECTRÓNICO], teléfono móvil [TELÉFONO] (en adelante SOCIO 3)

INTERVIENEN

Todos ellos intervienen en su propio nombre para pactar las reglas por las que se regulan sus relaciones como SOCIOS de la sociedad [DENOMINACIÓN SOCIAL], en adelante la EMPRESA.

MANIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente PACTO DE SOCIOS, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que los SOCIOS han creado la EMPRESA [DENOMINACIÓN SOCIAL], con participación de un tercio en el capital social cada uno de ellos, en forma de sociedad limitada, para llevar a cabo el siguiente objeto social

II. Que la EMPRESA es fruto de una iniciativa común cuyo objetivo es la de la ampliación de las líneas de negocio a las siguientes actividades [ACTIVIDAD]

III. Que los SOCIOS están interesados en pactar la regulación de aspectos organizativos y de régimen jurídico, entrada de inversores y nuevos socios, transmisión de participaciones y otros relevantes para el funcionamiento de la EMPRESA.

IV. Que, a dichos efectos, los SOCIOS tienen la voluntad de suscribir el presente Pacto con el objeto de establecer los acuerdos y condiciones vinculantes para los SOCIOS en la organización y funcionamiento de la EMPRESA.

V. Que, conviniendo todos los SOCIOS en concertar el contrato, otorgan a tal fin el presente PACTO DE SOCIOS, en base a las siguientes

CLÁUSULAS

PRIMERA.- OBJETO DEL CONTRATO

El objeto del presente contrato es de fijar los acuerdos y condiciones vinculantes para los SOCIOS sobre el funcionamiento de la EMPRESA, en especial relacionadas con la organización de la EMPRESA, entrada de inversores y/o accionistas, transmisión de participaciones sociales y determinación de los derechos y obligaciones de los SOCIOS.

El funcionamiento de la EMPRESA se regirá por el presente PACTO, su escritura de constitución y sus Estatutos Sociales, no existiendo otros acuerdos entre los SOCIOS tendentes a regular la organización y funcionamiento de la EMPRESA.

En el supuesto de que alguno de los acuerdos recogidos en el presente PACTO entre fuera discrepante con los Estatutos de la EMPRESA, prevalecerán las estipulaciones del presente PACTO entre los SOCIOS, quienes renuncian desde este momento, con pleno efecto y con carácter irrevocable, a cuantos derechos y acciones pudiesen corresponderles por razón de lo establecido en los referidos Estatutos en contravención del presente PACTO.

SEGUNDA.- ORGANIZACIÓN Y ADMINISTRACIÓN DE LA EMPRESA

La gestión y dirección de la EMPRESA se dividirá en tres ramas de actividad, cuya administración corresponderá a cada uno de los SOCIOS:

-El SOCIO 1 dirigirá la rama de negocio de [ACTIVIDAD]

-El SOCIO 2 dirigirá la rama de negocio de [ACTIVIDAD]

-El SOCIO 3 dirigirá la rama de negocio de [ACTIVIDAD]

Cada uno de los SOCIOS tendrá atribuido el uso de la firma social, y la representación de la EMPRESA, tanto en juicio como fuera de él para cualquier clase de actos o contratos, en cada una de sus ramas de actividad.

No obstante ser todos los SOCIOS administradores solidarios, deberán consultarse y decidirse de forma mancomunada todos los aspectos que afecten a la organización y funcionamiento global de la EMPRESA o que se refieran a más de una rama de actividad. La toma de decisiones conjunta se realizará de forma consensuada o, en su caso por mayoría, de forma vinculante para el SOCIO discrepante. En todo caso, serán objeto de decisión conjunta todos los aspectos relativos a contratación de personal, cambios de sede y creación de nuevas líneas de negocio, entrada de nuevos socios e inversores, ampliación de capital, transmisión de participaciones, régimen de los SOCIOS y otras análogas que afecten a la marcha de la EMPRESA.

La entrada de nuevos inversores o socios no alterará el régimen de administración, salvo acuerdo unánime de los SOCIOS fundadores.

En caso de fallecimiento, separación o cese por cualquier causa de uno de los SOCIOS, los otros dos SOCIOS ostentarán la administración de la EMPRESA de acuerdo a lo dispuesto en esta cláusula, asumiendo conjunta o individualmente la correspondiente rama de actividad, salvo que de común acuerdo decidan otro régimen de administración.

TERCERA.- ENTRADA DE NUEVOS SOCIOS E INVERSORES

Los SOCIOS fijan de común acuerdo unos objetivos estratégicos en dos horizontes temporales en cuanto a la entrada de nuevos socios e inversores:

1. Horizonte temporal 1: En los tres años siguientes al de la firma de este PACTO se admitirá la entrada de nuevos socios y/o inversores por decisión unánime de los SOCIOS.

En el caso de socios-inversores su participación se materializará mediante ampliación del capital social, con un límite del 30% para todo el periodo, y estará en todo caso condicionada al compromiso de inversión no inferior al 25% del volumen de negocio. Los SOCIOS renuncian al derecho de suscripción y adquisición preferente en este periodo cuando se trate de ampliación de participaciones sociales por la incorporación de socios inversores.

La entrada de nuevos socios requerirá necesariamente que éstos se adhieran en su integridad al presente PACTO.

2. Horizonte temporal 2: A partir del cuarto año de la firma de este PACTO, el régimen de transmisión de participaciones se sujetará a los límites establecidos en la siguiente cláusula, ostentando los socios el derecho de adquisición preferente en el caso de que uno de los SOCIOS pretenda transmitir total o parcialmente sus participaciones en la EMPRESA a un tercero. Asimismo, será efectivo el derecho de acompañamiento de los SOCIOS establecido en la cláusula quinta de este contrato.

En el caso de inversores, la entrada deberá decidirse por el órgano de administración previsto en la cláusula anterior, adoptándose las decisiones por mayoría.

CUARTA.- TRANSMISIÓN DE PARTICIPACIONES SOCIALES: DERECHO DE ADQUISICIÓN PREFERENTE

En el supuesto de que uno de los SOCIOS pretenda transmitir total o parcialmente sus participaciones sociales en la EMPRESA a un tercero, el SOCIO deberá comunicar su intención al órgano de administración, con expresión del precio de transmisión, con un plazo de quince días de antelación a fin de que los demás SOCIOS puedan ejercitar el derecho de acompañamiento o el de adquisición preferente de las participaciones, los cuales se realizarán a prorrata de sus respectivas participaciones en caso de que existan varios interesados.

El SOCIO que pretenda realizar la transmisión deberá obtener, como condición indispensable para su ejecución, el compromiso escrito del tercero adquirente de adherirse íntegramente y sin reservas al presente PACTO.

Comunicada la intención por uno de los SOCIOS de ejercitar el derecho de adquisición preferente, el órgano de administración fijará el valor de la participación si hubiere acuerdo entre transmitente y adquirente. En caso de discrepancia, el valor de la participación se fijará por la valoración de mercado de la EMPRESA, encomendándose el dictamen a un Experto Independiente que deberán emitir su informe en el plazo máximo de treinta días naturales desde la recepción del encargo.

Si la diferencia de la valoración con el precio comunicado es inferior al 10%, por exceso o defecto, quedará fijado como valor de transmisión el precio comunicado. Si la diferencia fuese superior a dicho porcentaje, se encomendará dictamen dirimente a un tercer Experto Independiente, que fijará el valor de la transmisión de forma vinculante. En ningún caso el precio de la transmisión será superior al ofertado por el tercero, según la comunicación realizada por el SOCIO.

QUINTA.- DERECHO DE ACOMPAÑAMIENTO

En el supuesto de que alguno de los SOCIOS recibiera una oferta para adquirir parte o la totalidad de sus acciones por parte de un tercero, los demás SOCIOS, sin perjuicio del derecho a la adquisición preferente, tendrán el derecho a vender conjuntamente al oferente con dicho SOCIO, al mismo precio y condiciones que las ofrecidas a éste y en proporción a sus respectivas participaciones en el capital social.

En caso de que uno o varios SOCIOS opten por el derecho de acompañamiento, la transmisión al SOCIO que ejercite el derecho de adquisición preferente o al tercero oferente deberá serlo de todas las participaciones del SOCIO inicial y acompañante (-s).

El SOCIO o SOCIOS que pretendan realizar la transmisión deberán obtener, como condición indispensable para su ejecución, el compromiso escrito del tercero adquirente de adherirse íntegramente y sin reservas al presente PACTO.

SEXTA .- DERECHOS DE LOS SOCIOS

Los SOCIOS fundadores, por la aportación de su experiencia profesional y por el desempeño de su trabajo a tiempo completo y en régimen de dedicación exclusiva a la EMPRESA, tienen los derechos reconocidos legalmente y los derechos retributivos establecidos en este PACTO. Estos derechos no serán extensibles a los demás SOCIOS que no tengan relación de dedicación exclusiva a la empresa.

En especial, los SOCIOS tendrán derecho:

- A una retribución mensual de [IMPORTE] euros por catorce pagas, más una prima por participación en el órgano de administración de [IMPORTE] euros anuales, que se fraccionara en doce mensualidades.

-En el caso de alcanzar los objetivos estratégicos recogidos en el Plan de EMPRESA, a una prima por objetivos equivalente al 20% de las ganancias.

- En caso de que alguno o algunos de los SOCIOS asuma la dirección de una rama de actividad por cese o separación de otro socio, o de una nueva rama de actividad de la EMPRESA, tendrá derecho a una prima de especial dedicación consistente en un incremento del 50% de la retribución por su participación en el órgano de administración.

SÉPTIMA.- OBLIGACIONES DE LOS SOCIOS

Los SOCIOS fundadores deberán cumplir todas las obligaciones recogidas en el presente PACTO con arreglo a los principios de buena fe y de diligencia, asumiendo libremente las obligaciones de permanencia mínima, dedicación exclusiva, prohibición de competencia y confidencialidad que se desarrollan en las siguientes cláusulas.

El incumplimiento de estas obligaciones determinará que el SOCIO deba indemnizar a la EMPRESA por todos los daños y perjuicios producidos, estableciéndose, como cláusula penal, el importe de 10.000 euros por incumplimiento de cualesquiera de las obligaciones expresadas en el presente PACTO.

Esta cláusula penal se pacta con carácter adicional y no eximirá al SOCIO incumplidor del pago de los daños y perjuicios efectivamente derivados de su incumplimiento.

OCTAVA.- PERMANENCIA MÍNIMA

Los SOCIOS se comprometen a permanecer en la EMPRESA y a no transmitir sus participaciones sociales en el plazo mínimo de un año desde la fecha de la firma de este PACTO.

NOVENA.- DEDICACIÓN EXCLUSIVA

Los SOCIOS se comprometen a desarrollar su actividad profesional de forma exclusiva para la EMPRESA, sin prestar otras actividades retribuidas por cuenta propia o ajena.

DÉCIMA.- PROHIBICIÓN DE COMPETENCIA

Los SOCIOS se comprometen expresamente a no competir con la EMPRESA, ya sea directa o indirectamente, por sí mismos, o a través de terceros, conjunta o individualmente desde la firma de este contrato, y en toda su vigencia. En caso de separación o desvinculación de la EMPRESA, la prohibición de competencia se extenderá durante el plazo de dos años más desde la fecha de desvinculación o separación.

Por tanto, no podrán realizar actividades y/o actuaciones que directa o indirectamente coincidan en el mercado o puedan coincidir con las actividades y/o productos de la empresa, ni por cuenta propia ni ajena, ya sea en calidad de trabajadores, asesores, comerciales, consultores, accionistas, o cualquier otra figura análoga o similar.

UNDÉCIMA.- CONFIDENCIALIDAD

Los SOCIOS se comprometen, tanto durante la vigencia de la sociedad como una vez extinguida, a no transmitir, difundir o revelar a terceras personas información confidencial de la EMPRESA a la que hayan tenido acceso como consecuencia de su actividad, o a utilizar tal información en interés propio. El deber de confidencialidad permanecerá tras la separación o desvinculación de los SOCIOS.

A estos efectos, los SOCIOS expresamente se comprometen a no suministrar, ceder o vender ningún tipo de información respecto del desarrollo y productos de la EMPRESA a otras personas, entidades o sociedades.

DUODÉCIMA.- DURACIÓN

El presente PACTO tiene una duración indefinida desde la fecha de su firma en tanto desarrolle su actividad la EMPRESA, con independencia de las modificaciones en la composición personal de la EMPRESA, en tanto que la adquisición de la condición de socio requiere preceptivamente de la íntegra adhesión al presente PACTO.

DECIMOTERCERA.- MODIFICACIONES

Las modificaciones del presente PACTO requerirán de consentimiento por escrito de todos los SOCIOS y de los eventuales adherentes, cuyos derechos y obligaciones se vieran afectados por la modificación.

DECIMOCUARTA.- NOTIFICACIONES

Toda notificación formal que se efectúe entre las partes se hará preferentemente en las direcciones de correo electrónico que figuran en el encabezamiento, sin perjuicio de que también puedan ser realizadas en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de dirección de correo electrónico y/o de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

DECIMOQUINTA.- SUMISIÓN A MEDIACIÓN Y/O ARBITRAJE

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación (en su caso se citará la institución) de [INSTITUCIÓN DE MEDIACIÓN], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y (caso de fijar un plazo máximo [PLAZO]) fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

( en su caso, pacto de arbitraje...) A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de [INSTITUCIÓN ARBITRAL], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento. Fdo.: Fdo.:

---
name: escritura-constitucion-sociedad-unipersonal-limitada-mer-0259
description: "Escritura de constitución de una sociedad unipersonal, limitada o anónima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de constitución de una sociedad unipersonal, limitada o anónima

> Formulario **MER-0259** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Escritura pública de constitución de una sociedad limitada o anónima unipersonal por un único socio fundador, con estipulaciones sobre denominación, duración, domicilio, objeto, capital y aportaciones, administración y aprobación de estatutos, para su inscripción en el Registro Mercantil.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de constitución de una sociedad unipersonal, limitada o anónima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de constitución de una sociedad unipersonal, limitada o anónima” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-constitucion-sociedad-unipersonal-limitada-mer-0259`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (8 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] ACTIVIDAD
- [ ] CALLE, NÚMERO Y PISO
- [ ] COLEGIO NOTARIAL
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DE LA APORTACIÓN
- [ ] DOMICILIO
- [ ] ENTIDAD DE CRÉDITO
- [ ] FECHA
- [ ] FIRMA DEL OTORGANTE Y DEL NOTARIO
- [ ] NACIONALIDAD
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE PROTOCOLO
- [ ] OBJETO SOCIAL
- [ ] PROFESIÓN
- [ ] REPETIR EL SIGUIENTE PÁRRAFO PARA CADA APORTACIÓN:

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…ón, oposición y portabilidad, en los términos previstos en la normativa vigente.»: el original aludía a los ficheros del protocolo y de administración y organización de la derogada LO 15/1999; adaptar la cláusula informativa al modelo de información de protección de datos que utilice la notaría.
- Junto a «…igir esta responsabilidad prescribirá a los cuatro años de la fecha del informe.»: la Ley 3/2009 está derogada por el Real Decreto-ley 5/2023; el régimen de aportaciones no dinerarias se recoge en el texto refundido de la Ley de Sociedades de Capital. Comprobar los artículos vigentes.
- Junto a «…s mismas circunstancias, en su caso, de los auditores de cuentas de la sociedad.»: comprobar el artículo equivalente en el texto refundido de la Ley de Sociedades de Capital (escritura de constitución).

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

NÚMERO DE PROTOCOLO: [Nº DE PROTOCOLO]

En [LOCALIDAD], a [FECHA].

Ante mí, D./Dña. [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio de [COLEGIO NOTARIAL],

COMPARECE

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero/a / divorciado/a / separado/a judicialmente / viudo/a / casado/a], con profesión [PROFESIÓN], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [Nº DE DOCUMENTO].

INTERVIENE

D./Dña. [NOMBRE Y APELLIDOS] interviene en su propio nombre y derecho.

Tiene, a mi juicio, según interviene, la capacidad legal necesaria para celebrar la presente escritura de constitución de SOCIEDAD [ELEGIR: LIMITADA / ANÓNIMA] UNIPERSONAL, a cuyo fin

EXPONE

PRIMERO.- Que el mismo D./Dña. [NOMBRE Y APELLIDOS] ha decidido constituir una sociedad [ELEGIR: limitada / anónima] unipersonal para la realización de [ACTIVIDAD].

SEGUNDO.- Que, a tales efectos, y en su calidad de único socio fundador, ha decidido otorgar la presente escritura de constitución de SOCIEDAD [ELEGIR: LIMITADA / ANÓNIMA] UNIPERSONAL, que se regirá por las siguientes

ESTIPULACIONES

I.- Constitución y socio único fundador

En el presente acto el compareciente D./Dña. [NOMBRE Y APELLIDOS], como único socio fundador, procede a constituir una sociedad [ELEGIR: limitada / anónima] unipersonal de nacionalidad española, que se regirá por el presente contrato, por los estatutos que en el mismo se aprueban y, en lo en ellos no dispuesto y en cuanto no sean contrarios a la misma, por el texto refundido de la Ley de Sociedades de Capital. Se hace constar expresamente el carácter unipersonal de la sociedad, a los efectos de su constancia en el Registro Mercantil.

II.- Denominación

La sociedad se denomina [DENOMINACIÓN SOCIAL], [ELEGIR: S.L.U. / S.A.U.], denominación que no se halla registrada por ninguna otra sociedad o entidad inscribible en el Registro Mercantil, según consta en la certificación negativa de denominación que el compareciente exhibe y que se halla vigente, la cual procedo a unir, a requerimiento del compareciente, a la matriz de la presente escritura.

III.- Duración

La sociedad tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de la presente escritura, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la sociedad en momentos anteriores al de su inscripción en el Registro Mercantil.

Los ejercicios sociales se computarán por años naturales.

IV.- Domicilio

El domicilio de la sociedad se halla situado en [LOCALIDAD], calle [CALLE, NÚMERO Y PISO].

V.- Objeto social

El objeto social de la sociedad será [OBJETO SOCIAL].

VI.- Capital social

El capital social será de [IMPORTE] euros, dividido en [ELEGIR: participaciones / acciones] de [IMPORTE] euros de valor nominal cada una de ellas, numeradas de manera correlativa con los números 1 a [Nº].

Dicho capital social ha sido totalmente suscrito y desembolsado por el socio único fundador, que ha realizado las aportaciones que se describen:

[REPETIR EL SIGUIENTE PÁRRAFO PARA CADA APORTACIÓN:]

Aportación de [DESCRIPCIÓN DE LA APORTACIÓN], por lo que se le asignan [Nº] [ELEGIR: participaciones / acciones], que son las numeradas [Nº] a [Nº].

La totalidad de dichas aportaciones ha sido realizada a título de propiedad, y se han efectuado en moneda nacional, realidad que se acredita mediante certificación del depósito de las correspondientes cantidades a nombre de la sociedad en la entidad de crédito [ENTIDAD DE CRÉDITO], certificación que se halla vigente según compruebo al observar la fecha del depósito al que hace referencia, y cuyo original se me entrega para ser incorporado a la presente escritura, lo cual procedo a efectuar a requerimiento del compareciente, quedando la misma unida al final de esta matriz.

VII.- Administración y representación de la sociedad

D./Dña. [NOMBRE Y APELLIDOS] asume el cargo de administrador único de la compañía y representación inicial de la sociedad durante el plazo estatutario de [Nº] años, y lo acepta en el presente acto, manifestando no hallarse incurso en ninguno de los supuestos legales ni estatutarios inhabilitantes para el ejercicio del mismo.

Igualmente queda encargado el citado administrador inicial único de la presentación de la presente escritura constitutiva para su inscripción en el Registro Mercantil de [PROVINCIA], quien se compromete a su cumplimiento.

VIII.- Aprobación de los estatutos sociales

Se procede a la aprobación de los estatutos que han de regir el funcionamiento de la sociedad, que el compareciente me otorga en este acto, extendidos en [Nº] folios, aprobados y firmados por él, que ratifica y eleva a escritura pública mediante su incorporación a la presente, que solicita expresamente, lo cual efectúo uniéndolos al final de esta matriz.

IX.- Facultades de subsanación

El compareciente podrá, en su calidad de socio único, proceder a la subsanación o rectificación de la presente escritura y de los estatutos a ella incorporados cuando ello sea preciso para su obligada inscripción en el Registro Mercantil de [PROVINCIA], y siempre que las citadas subsanaciones o rectificaciones se limiten a meros errores materiales o a aceptar las modificaciones procedentes de la calificación registral.

X.- Protección de datos personales

Advierto expresamente al compareciente de que sus datos serán tratados por el Notario, como responsable del tratamiento, conforme al Reglamento (UE) 2016/679 (RGPD) y a la Ley Orgánica 3/2018 (LOPDGDD), con la finalidad de formalizar el presente instrumento público y cumplir las obligaciones legales derivadas de la función notarial, así como de que, en su caso, tales datos pueden ser cedidos a aquellas administraciones públicas que, según una norma con rango de ley, tengan derecho a ello. Le informo de los derechos que le asisten de acceso, rectificación, supresión, limitación, oposición y portabilidad, en los términos previstos en la normativa vigente.

OTORGAMIENTO Y AUTORIZACIÓN NOTARIAL

Le leo, por su elección, esta escritura, advertido de su derecho a leerla por sí, del que no usa y, tras hacerle las oportunas explicaciones verbales para su cabal conocimiento, manifiesta quedar enterado, la acepta, se ratifica y firma.

Yo, el Notario, DOY FE de que el consentimiento ha sido libremente prestado y de que el otorgamiento se adecua a la legalidad y a la voluntad debidamente informada del otorgante.

Queda extendida en un total de [Nº] folios de papel notarial, el primero con el número [Nº] y los demás con los números siguientes en orden correlativo.

Y de su contenido, DOY FE.

[FIRMA DEL OTORGANTE Y DEL NOTARIO]

NOTAS DE USO

1. Denominación (art. 413 del Reglamento del Registro Mercantil): no podrá autorizarse escritura de constitución de sociedades y demás entidades inscribibles, o de modificación de denominación, sin que se presente al Notario la certificación que acredite que no figura registrada la denominación elegida. La denominación habrá de coincidir exactamente con la que conste en la certificación negativa expedida por el Registrador Mercantil Central. La certificación presentada deberá ser la original, estar vigente y haber sido expedida a nombre de un fundador o promotor o, en caso de modificación de la denominación, de la propia sociedad o entidad. Los términos «fundador o promotor» deben interpretarse en sentido jurídico propio; por ello, si se trata de una sociedad de responsabilidad limitada, la certificación deberá haber sido expedida a nombre de cualquiera de quienes, como socios, otorgan la escritura fundacional que expresa su aportación y las participaciones que se les asignan, exigencia que no se cumple cuando la certificación aparece expedida a nombre de quien se limita a intervenir en la escritura no como socio fundador, sino únicamente para manifestar que solicitó la certificación en nombre de uno de los actuales fundadores y que se la cede mediante la renuncia de la reserva hecha a su favor (resolución de la Dirección General de los Registros y del Notariado de 22 de noviembre de 1993).

2. Aportaciones no dinerarias: la Ley 3/2009 introdujo un nuevo régimen de las aportaciones no dinerarias. En relación con el informe del experto: las aportaciones no dinerarias, cualquiera que sea su naturaleza, habrán de ser objeto de un informe elaborado por uno o varios expertos independientes con competencia profesional, designados por el Registrador Mercantil del domicilio social conforme al procedimiento que reglamentariamente se determine. El informe contendrá la descripción de la aportación, con sus datos registrales, si existieran, y la valoración de la aportación, expresando los criterios utilizados y si se corresponde con el valor nominal y, en su caso, con la prima de emisión de las acciones que se emitan como contrapartida. El valor que se dé a la aportación en la escritura social no podrá ser superior a la valoración realizada por los expertos. El experto responderá frente a la sociedad, frente a los accionistas y frente a los acreedores de los daños causados por la valoración, y quedará exonerado si acredita que ha aplicado la diligencia y los estándares propios de la actuación que le haya sido encomendada. La acción para exigir esta responsabilidad prescribirá a los cuatro años de la fecha del informe.

Excepciones a la necesidad de informe del experto. No será necesario: a) cuando la aportación no dineraria consista en valores mobiliarios que coticen en un mercado secundario oficial o en otro mercado regulado o en instrumentos del mercado monetario. Estos bienes se valorarán al precio medio ponderado al que hubieran sido negociados en uno o varios mercados regulados en el último trimestre anterior a la fecha de la realización efectiva de la aportación, de acuerdo con la certificación emitida por la sociedad rectora del mercado secundario oficial o del mercado regulado de que se trate. Si ese precio se hubiera visto afectado por circunstancias excepcionales que hubieran podido modificar significativamente el valor de los bienes en la fecha efectiva de la aportación, los administradores de la sociedad deberán solicitar el nombramiento de experto independiente para que emita informe; b) cuando la aportación consista en bienes distintos de los señalados en la letra anterior cuyo valor razonable se hubiera determinado, dentro de los seis meses anteriores a la fecha de la realización efectiva de la aportación, por experto independiente con competencia profesional no designado por las partes, de conformidad con los principios y las normas de valoración generalmente reconocidos para esos bienes. Si concurrieran nuevas circunstancias que pudieran modificar significativamente el valor razonable de los bienes a la fecha de la aportación, los administradores de la sociedad deberán solicitar el nombramiento de experto independiente para que emita informe. En este caso, si los administradores no hubieran solicitado el nombramiento de experto debiendo hacerlo, el accionista o los accionistas que representen, al menos, el cinco por ciento del capital social el día en que se adopte el acuerdo de aumento del capital podrán solicitar del Registrador Mercantil del domicilio social que, con cargo a la sociedad, nombre un experto para que se efectúe la valoración de los activos. La solicitud podrán hacerla hasta el día de la realización efectiva de la aportación, siempre que en el momento de presentarla continúen representando al menos el cinco por ciento del capital social.

Cuando las aportaciones no dinerarias se efectúen sin informe de expertos independientes designados por el Registro Mercantil, los administradores elaborarán un informe que contendrá: 1) la descripción de la aportación; 2) el valor de la aportación, el origen de esa valoración y, cuando proceda, el método seguido para determinarla (si la aportación hubiera consistido en valores mobiliarios cotizados en mercado secundario oficial o del mercado regulado de que se trate o en instrumentos del mercado monetario, se unirá al informe la certificación emitida por su sociedad rectora); 3) una declaración en la que se precise si el valor obtenido corresponde, como mínimo, al número y al valor nominal y, en su caso, a la prima de emisión de las acciones emitidas como contrapartida; 4) una declaración en la que se indique que no han aparecido circunstancias nuevas que puedan afectar a la valoración inicial.

3. Contenido de la escritura de constitución (art. 8 de la derogada Ley de Sociedades Anónimas, hoy recogido en la Ley de Sociedades de Capital): en la escritura se expresarán: a) los nombres, apellidos y edad de los otorgantes, si éstos fueran personas físicas, o la denominación o razón social, si son personas jurídicas y, en ambos casos, la nacionalidad y el domicilio; b) la voluntad de los otorgantes de fundar una sociedad; c) el metálico, los bienes o derechos que cada socio aporte o se obligue a aportar, indicando el título en que lo haga y el número de acciones o participaciones atribuidas en pago; d) la cuantía total, al menos aproximada, de los gastos de constitución, tanto de los ya satisfechos como de los meramente previstos hasta que aquélla quede constituida; e) los estatutos que han de regir el funcionamiento de la sociedad; f) los nombres, apellidos y edad de las personas que se encarguen inicialmente de la administración y representación social, si fueran personas físicas, o su denominación social si fueran personas jurídicas y, en ambos casos, su nacionalidad y domicilio, así como las mismas circunstancias, en su caso, de los auditores de cuentas de la sociedad.

4. Aportaciones dinerarias: si se efectúa la aportación en moneda extranjera, debe determinarse su equivalencia en [IMPORTE] euros.

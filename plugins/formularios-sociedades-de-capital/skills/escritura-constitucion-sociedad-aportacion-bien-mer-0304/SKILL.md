---
name: escritura-constitucion-sociedad-aportacion-bien-mer-0304
description: "Escritura de constitución de sociedad con aportación de un bien ganancial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de constitución de sociedad con aportación de un bien ganancial

> Formulario **MER-0304** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Escritura pública de constitución de una sociedad mercantil de capital en la que dos cónyuges casados en régimen de gananciales aportan, como contravalor de las participaciones sociales que se les adjudican con carácter ganancial, un inmueble ganancial (aportación no dineraria en el momento de la constitución).

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de constitución de sociedad con aportación de un bien ganancial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de constitución de sociedad con aportación de un bien ganancial” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-constitucion-sociedad-aportacion-bien-mer-0304`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (9 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] IMPORTE (7 veces)
- [ ] AÑO (6 veces)
- [ ] DÍA (6 veces)
- [ ] MES (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] NÚMERO (6 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] NOMBRE DEL NOTARIO (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL PRIMER CÓNYUGE (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL SEGUNDO CÓNYUGE (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] IMPORTE EN LETRA (3 veces)
- [ ] Nº DE FINCA (3 veces)
- [ ] Nº DE INSCRIPCIÓN (3 veces)
- [ ] Nº DE PROTOCOLO (3 veces)
- [ ] DNI/NIE (2 veces)
- [ ] FOLIO (2 veces)
- [ ] LIBRO (2 veces)
- [ ] NIF (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] PLAZO (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] TOMO (2 veces)
- [ ] ARANCEL APLICABLE
- [ ] BASES DE CÁLCULO
- [ ] CLASE DE ESCRITURA
- [ ] COLEGIO NOTARIAL
- [ ] DENOMINACIÓN O NOMBRE DEL GESTOR
- [ ] DESCRIPCIÓN DEL INMUEBLE
- [ ] HOJA
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE
- [ ] Nº DE CERTIFICACIÓN
- [ ] OBJETO SOCIAL
- [ ] SECCIÓN

## Normas que cita el formulario

- art. 6 Ley Orgánica 3/2018

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

- Junto a «…números [Nº] y los [NÚMERO] siguientes, el mismo día de su autorización. DOY FE.»: el original citaba disposiciones fiscales de 2010 y la fórmula arancelaria de la época; comprobar la vigencia del tratamiento fiscal (art. 45.I.B).11 TRLITPAJD), del arancel notarial aplicable y de los plazos y advertencias registrales, así como el cumplimiento de la normativa sobre titularidad real y prevención del blanqueo de capitales en el momento del otorgamiento.

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

NÚMERO [Nº DE PROTOCOLO]

CONSTITUCIÓN DE LA ENTIDAD "[DENOMINACIÓN SOCIAL]" [ELEGIR: SOCIEDAD LIMITADA / SOCIEDAD LIMITADA UNIPERSONAL / SOCIEDAD ANÓNIMA]

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO].

Ante mí, [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio Notarial de [COLEGIO NOTARIAL],

COMPARECEN

Los consortes D./Dña. [NOMBRE Y APELLIDOS DEL PRIMER CÓNYUGE] y D./Dña. [NOMBRE Y APELLIDOS DEL SEGUNDO CÓNYUGE], mayores de edad, vecinos de [LOCALIDAD], con domicilio en [DOMICILIO], y con DNI/NIF [DNI/NIE] y [DNI/NIE], respectivamente.

Declaran que su régimen económico matrimonial es el legal de la sociedad de gananciales.

Les identifico con los documentos reseñados, que compruebo tienen la fotografía y firma coincidentes con las de sus titulares.

Sus datos resultan de la documentación que me exhiben y de sus manifestaciones.

INTERVIENEN en su propio nombre y derecho.

[OPCIONAL — incluir solo si interviene además una persona jurídica en representación de la cual comparece otra persona (por ejemplo, un socio persona jurídica o el mandatario de una entidad)]

Y además, D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTANTE], como [ELEGIR: administrador único / administrador solidario / apoderado], en nombre y representación de la entidad mercantil "[DENOMINACIÓN SOCIAL]", de nacionalidad española y duración indefinida, con domicilio social en [LOCALIDAD], calle [DOMICILIO], número [Nº], y con CIF [NIF]. Su objeto social lo constituye [OBJETO SOCIAL]. Inscrita en el Registro Mercantil de [PROVINCIA], en el tomo [TOMO], libro [LIBRO], folio [FOLIO], sección [SECCIÓN], hoja [HOJA], inscripción [Nº DE INSCRIPCIÓN]. Los datos reseñados resultan de la escritura de [CLASE DE ESCRITURA] autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], el día [DÍA] de [MES] de [AÑO], con el número [Nº DE PROTOCOLO] de protocolo, cuya copia autorizada he tenido a la vista; asimismo resultan de consulta telemática por mí efectuada al Registro Mercantil de [PROVINCIA], de la que testimonio parcial incorporo a la presente, sin que en lo omitido haya nada que desvirtúe lo inserto. Actúa en el ejercicio de su cargo, para el que fue designado/a por tiempo [ELEGIR: indefinido / por el plazo de [PLAZO]], por decisión de [ELEGIR: el socio único, en el ejercicio de las funciones de la Junta General / la Junta General], el día [DÍA] de [MES] de [AÑO], en la que aceptó el nombramiento, elevado a público mediante escritura autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], el día [DÍA] de [MES] de [AÑO], con el número [Nº DE PROTOCOLO] de protocolo, que causó la inscripción [Nº DE INSCRIPCIÓN] de su hoja social. Me asevera la subsistencia de la entidad y la vigencia de su cargo, así como no haber variado ninguno de los particulares de la sociedad antes reseñados y que el acto que aquí se documenta no implica negación del objeto social. A mi juicio, las facultades representativas inherentes a su acreditado cargo son suficientes para el otorgamiento de la presente escritura.

A mi juicio, tienen los comparecientes, en el concepto en el que intervienen, capacidad legal suficiente para otorgar la presente escritura de CONSTITUCIÓN DE SOCIEDAD MERCANTIL, y a tal fin,

EXPONEN

Los consortes D./Dña. [NOMBRE Y APELLIDOS DEL PRIMER CÓNYUGE] y D./Dña. [NOMBRE Y APELLIDOS DEL SEGUNDO CÓNYUGE] son dueños con carácter ganancial de:

DESCRIPCIÓN.- [DESCRIPCIÓN DEL INMUEBLE]

INSCRIPCIÓN.- Inscrita en el Registro de la Propiedad de [LOCALIDAD], al tomo [TOMO], libro [LIBRO], folio [FOLIO], finca número [Nº DE FINCA].

TÍTULO.- Les pertenece a dichos consortes, con carácter ganancial, por el título de [ELEGIR: compraventa / otro título que proceda], formalizada mediante escritura autorizada el día [DÍA] de [MES] de [AÑO] por D./Dña. [NOMBRE DEL NOTARIO], Notario/a de [LOCALIDAD], la cual causó la inscripción [Nº DE INSCRIPCIÓN] de la citada finca registral número [Nº DE FINCA].

REFERENCIA CATASTRAL.- Los comparecientes manifiestan que los datos catastrales referentes a la finca objeto de esta escritura se hallan reflejados en el certificado catastral telemático descriptivo y gráfico, que dejo unido a la presente. A instancia de los exponentes, hago constar yo, el Notario, que dejo incorporado el certificado por mí obtenido por medios telemáticos, en cumplimiento de lo dispuesto en el art. 170 del Reglamento Notarial y en el art. 3.2 del texto refundido de la Ley del Catastro Inmobiliario (Real Decreto Legislativo 1/2004). Habiéndose cumplido la obligación de aportar la referencia catastral, les hago saber que no será preciso hacer la correspondiente declaración de alteración catastral ante el Catastro.

CARGAS Y ARRIENDOS.- Libre de unas y otros, así como al corriente en el pago de los gastos de comunidad.

IMPUESTO SOBRE BIENES INMUEBLES.- A los efectos del art. 64 del texto refundido de la Ley Reguladora de las Haciendas Locales, hacen constar los comparecientes que el inmueble está al corriente del pago del Impuesto sobre Bienes Inmuebles. Advierto a los comparecientes que los bienes inmuebles quedan afectos al pago de toda cuota tributaria pendiente y me eximen de solicitar previa información sobre las deudas pendientes que por tal impuesto afecten al inmueble.

INFORMACIÓN REGISTRAL.- A los efectos del contenido del art. 175 del Reglamento Notarial, yo, el Notario, hago constar que [ELEGIR: he accedido por vía telemática a los asientos registrales de la finca descrita / por imposibilidad técnica no he podido acceder por vía telemática a los asientos registrales de la finca descrita, por lo que, conforme establece el apartado 4.º de dicho art. 175 del Reglamento Notarial, he solicitado del Registro de la Propiedad información registral por otro medio, obtenida de dicho Registro, alusiva a la finca descrita, en la que constan todas las circunstancias de la petición e información adecuadas]. Hago la advertencia expresa a los otorgantes de que prevalece sobre la manifestación de los comparecientes la situación registral existente con anterioridad a la presentación en el Registro de la Propiedad de la copia autorizada o telemática de esta escritura. La descripción del inmueble, su titularidad y situación de cargas, en la forma expresada en los párrafos anteriores, resulta de las manifestaciones de los aportantes, del título de propiedad que me exhiben y de la nota simple del Registro de la Propiedad que yo, el Notario, tengo a la vista e incorporo a la presente como parte integrante de la misma.

VALOR a efectos de la aportación: [IMPORTE EN LETRA] EUROS ([IMPORTE] €).

CONSTITUCIÓN.- Que dichos D./Dña. [NOMBRE Y APELLIDOS DEL PRIMER CÓNYUGE] y D./Dña. [NOMBRE Y APELLIDOS DEL SEGUNDO CÓNYUGE] tienen voluntad de constituir y, mediante la presente, constituyen una SOCIEDAD [ELEGIR: LIMITADA / ANÓNIMA] de nacionalidad española, que se denominará «[DENOMINACIÓN SOCIAL], [ELEGIR: SOCIEDAD LIMITADA / SOCIEDAD ANÓNIMA]», se regirá por el texto refundido de la Ley de Sociedades de Capital, aprobado por Real Decreto Legislativo 1/2010, de 2 de julio, las demás disposiciones legales y reglamentarias aplicables y, en especial, por sus Estatutos, extendidos en [NÚMERO] folios de papel común por ambas caras, que, leídos y aprobados por los socios fundadores y firmados en el último de ellos por los mismos a mi presencia -firmas que en este acto legitimo-, me entregan y uno a esta matriz, formando parte de ésta y adquiriendo el carácter de instrumento público.

DENOMINACIÓN. CERTIFICACIÓN DEL REGISTRO MERCANTIL CENTRAL.- La compañía, como ha quedado dicho, adopta la denominación de «[DENOMINACIÓN SOCIAL], [ELEGIR: SOCIEDAD LIMITADA / SOCIEDAD ANÓNIMA]», no usada por ninguna otra, como se acredita mediante certificación del Registro Mercantil Central de fecha [DÍA] de [MES] de [AÑO], número [Nº DE CERTIFICACIÓN], expedida a nombre de D./Dña. [NOMBRE Y APELLIDOS], que queda protocolizada con esta matriz.

CAPITAL SOCIAL, SUSCRIPCIÓN Y DESEMBOLSO.- Como resulta de los Estatutos, el CAPITAL SOCIAL queda fijado en la cifra de [IMPORTE EN LETRA] EUROS ([IMPORTE] €), dividido en [NÚMERO] [ELEGIR: PARTICIPACIONES SOCIALES / ACCIONES], de [IMPORTE] EURO/S de valor nominal cada una de ellas, numeradas correlativamente, a efectos de identificación, del [Nº] al [Nº], ambos inclusive, capital que es suscrito y desembolsado en su totalidad y en la siguiente forma y proporción: Los consortes D./Dña. [NOMBRE Y APELLIDOS DEL PRIMER CÓNYUGE] y D./Dña. [NOMBRE Y APELLIDOS DEL SEGUNDO CÓNYUGE] aportan el inmueble ganancial descrito anteriormente (registral [Nº DE FINCA]) por su valor neto de [IMPORTE EN LETRA] EUROS ([IMPORTE] €), adjudicándose en contraprestación y con carácter ganancial las [ELEGIR: participaciones / acciones] de la siguiente forma: a) en cuanto a D./Dña. [NOMBRE Y APELLIDOS], las [ELEGIR: participaciones / acciones] números [Nº] al [Nº], ambas inclusive; y b) en cuanto a D./Dña. [NOMBRE Y APELLIDOS], las [ELEGIR: participaciones / acciones] números [Nº] al [Nº], ambas inclusive.

ADVERTENCIA.- Yo, el Notario, hago expresa advertencia de la responsabilidad solidaria de los socios fundadores y de quienes adquieran alguna de las participaciones sociales desembolsadas con aportaciones no dinerarias, conforme al art. 73 del texto refundido de la Ley de Sociedades de Capital, durante el plazo previsto en el art. 75 de la misma Ley, en cuanto a la realidad de las aportaciones y del valor que se les ha atribuido.

ÓRGANO DE ADMINISTRACIÓN.- De conformidad con los Estatutos de la compañía, los socios fundadores deciden optar por la forma de administración [ELEGIR: única / solidaria / mancomunada / Consejo de Administración] y designan como ADMINISTRADOR/ES, por plazo [ELEGIR: INDEFINIDO / DE [PLAZO]], a D./Dña. [NOMBRE Y APELLIDOS], atribuyéndole todas las facultades recogidas en el art. [Nº DE ARTÍCULO] de los Estatutos sociales. El/La nombrado/a administrador/a, cuyas circunstancias personales constan en la comparecencia, acepta el cargo y, hecha la advertencia de la prohibición de ocupar cargos en la Sociedad a las personas declaradas incompatibles en la medida y condiciones fijadas en el texto refundido de la Ley de Sociedades de Capital y demás disposiciones vigentes, o que las sustituyan o complementen, declara expresamente no estar incurso/a en ninguna de las prohibiciones, incapacidades e incompatibilidades establecidas en dicha legislación, tanto de carácter estatal como autonómico.

COMIENZO DE LAS OPERACIONES Y FACULTADES DEL ÓRGANO DE ADMINISTRACIÓN EN LA FASE ANTERIOR A LA INSCRIPCIÓN DE LA SOCIEDAD.- La Sociedad dará comienzo a sus operaciones el día de hoy. Los socios fundadores, aun cuando en su caso fuere reiteración de lo establecido por la vigente legislación de sociedades de capital, acuerdan facultar al órgano de administración nombrado de modo que, durante la fase anterior a la inscripción, pueda ejercitar las mismas facultades que en los presentes Estatutos y en las normas legales se atribuyen a dicho órgano con carácter general, de modo que los actos y contratos celebrados con terceros antes de la inscripción de la sociedad, dentro del ámbito de dichas facultades, quedarán automáticamente aceptados y asumidos por la sociedad por el mero hecho de su inscripción en el Registro Mercantil. Al propio tiempo: a) le facultan para que pueda realizar los actos y contratos que el cumplimiento de la actividad de la empresa que constituye su objeto social haga necesarios, útiles o convenientes, especialmente en el orden interno y organizativo, y el otorgamiento y revocación de poderes de cualquier clase; y b) para la dedicación, por cuenta propia o ajena, al mismo, análogo o complementario género de actividad que constituye el objeto social.

OTROS PACTOS Y CONDICIONES.

A) Inscripción parcial: Se solicita la inscripción, incluso parcial, de este título, a tenor del art. 63 del Reglamento del Registro Mercantil.

B) Utilización de técnicas electrónicas, informáticas y telemáticas: Se hace expresamente constar que los comparecientes renuncian en este acto, de modo formal y expreso, a la comunicación telemática del contenido de la presente escritura a través del sistema de información central del Consejo General del Notariado con el sistema de información corporativo del Colegio de Registradores de la Propiedad y Mercantiles de España.

APODERAMIENTO.- Los otorgantes se apoderan recíprocamente para que cualquiera de ellos, por sí solo, pueda rectificar, aclarar o subsanar esta escritura y los Estatutos protocolizados con ella, según lo que resulte de la calificación verbal o escrita del Registrador Mercantil.

CIF.- Los comparecientes me requieren a mí, el Notario, para solicitar de la Agencia Estatal de Administración Tributaria (AEAT), de conformidad con lo dispuesto en la vigente legislación y mediante el procedimiento telemático establecido para ello, la expedición en soporte electrónico del NÚMERO DE IDENTIFICACIÓN FISCAL; la comunicación acreditativa del mismo que reciba de la AEAT la dejaré unida a esta matriz por testimonio. A los efectos de dicha solicitud, manifiestan los comparecientes que la actividad, de las que constituyen su objeto social, que se especifique en aquélla sea la primera de las relacionadas en el art. [Nº DE ARTÍCULO] de los estatutos sociales.

APODERAMIENTO PARA GESTIONES.- Los comparecientes autorizan y, en lo menester, otorgan mandato expreso a «[DENOMINACIÓN O NOMBRE DEL GESTOR]», con CIF/NIF [NIF] y domicilio a efectos de notificaciones en [LOCALIDAD], calle [DOMICILIO], número [Nº], para que, en su nombre y representación, pueda presentar a la administración la presente escritura y cuantas otras hayan podido formalizarse o se formalicen necesarias para la inscripción de la misma en los Registros correspondientes, así como efectuar las gestiones y declaraciones que como sujetos u obligados tributarios les correspondan en relación con los actos que se contienen en las referidas escrituras, en orden a comunicar a la administración los datos necesarios para la liquidación de los tributos que se devenguen como consecuencia de tales actos, y otros de contenido informativo, encaminados a calificar y cuantificar el importe a ingresar o la cantidad que resulte a compensar o devolver, quedando igualmente facultado dicho autorizado/mandatario para interponer cuantos recursos sean convenientes o dirigir comunicaciones a la administración en orden a proteger los derechos de los otorgantes, así como a recibir de aquélla cuantas comunicaciones y notificaciones sean necesarias dirigidas a los mismos.

DECLARACIONES FISCALES.- Se solicita la exención en la modalidad de operaciones societarias del Impuesto sobre Transmisiones Patrimoniales y Actos Jurídicos Documentados, conforme al art. 45.I.B).11 del texto refundido de la Ley del Impuesto (Real Decreto Legislativo 1/1993, de 24 de septiembre).

PROTECCIÓN DE DATOS.- De conformidad con el art. 6 de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, se entiende por consentimiento del afectado toda manifestación de voluntad libre, específica, informada e inequívoca por la que éste acepta, ya sea mediante una declaración o una clara acción afirmativa, el tratamiento de datos personales que le conciernen. Cuando se pretenda fundar el tratamiento de los datos en el consentimiento del afectado para una pluralidad de finalidades, será preciso que conste de manera específica e inequívoca que dicho consentimiento se otorga para todas ellas. No podrá supeditarse la ejecución del contrato a que el afectado consienta el tratamiento de los datos personales para finalidades que no guarden relación con el mantenimiento, desarrollo o control de la relación contractual.

OTORGAMIENTO

Así lo otorgan los señores comparecientes, a quienes yo, el Notario, leo este documento, advertidos de su derecho a leerlo por sí, que no usan y, enterados de su contenido, adecuado a la legalidad y a su voluntad debidamente informada, lo aprueban libremente y firman conmigo. Hago las reservas y advertencias legales, en especial:

a) Las de carácter fiscal: obligatoriedad de presentar esta escritura a liquidación del impuesto de operaciones societarias en el plazo de treinta días hábiles desde este otorgamiento; exención del pago de dicho impuesto (art. 45.I.B).11 del texto refundido del Impuesto sobre Transmisiones Patrimoniales y Actos Jurídicos Documentados, RDLeg 1/1993, de 24 de septiembre); y sanciones en caso de incumplimiento de deberes fiscales.

b) Las de tipo registral: obligatoriedad de la inscripción en el Registro Mercantil en el plazo de un mes desde este otorgamiento.

c) Advierto del régimen de responsabilidad que afecta durante cinco años a los socios aportantes, frente a la sociedad y frente a los acreedores sociales, por la realidad de las aportaciones y el valor atribuido a las mismas.

d) Respecto a los datos personales recogidos en el presente documento, debe tenerse en cuenta que el tratamiento de los mismos se ajustará al Reglamento (UE) 2016/679, de 27 de abril (RGPD), y a la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, y que el interesado podrá ejercitar sus derechos de acceso, rectificación, supresión, portabilidad, oposición y limitación del tratamiento de los datos en los términos establecidos en los arts. 12 a 23 del citado Reglamento y en los arts. 12 a 18 de la citada Ley Orgánica.

e) Por último, hago constar expresamente que he cumplido con la obligación de identificación del "titular real" que impone la Ley 10/2010, de 28 de abril, de prevención del blanqueo de capitales y de la financiación del terrorismo, cuyo resultado, por manifestación de los socios aportantes, es que ellos mismos son los "titulares reales" de la operación aquí documentada, sin que me conste nada en contra de la anterior manifestación.

AUTORIZACIÓN

De todo lo contenido en este instrumento público, extiendo la presente en [NÚMERO] folios de papel de uso exclusivo para documentos notariales, el presente y los [NÚMERO] anteriores en orden correlativo de numeración y de la misma serie, DOY FE. Están las firmas de los comparecientes y mi sello, signo, firma y rúbrica.

DOCUMENTOS UNIDOS: [RELACIÓN DE DOCUMENTOS UNIDOS: CERTIFICACIÓN DEL REGISTRO MERCANTIL CENTRAL, CERTIFICADO CATASTRAL, NOTA SIMPLE, ESTATUTOS, ETC.]

SIGUEN LAS FIRMAS DE LOS COMPARECIENTES. SIGNADO, RUBRICADO Y FIRMADO POR MÍ. ESTÁ EL SELLO DE MI NOTARÍA.

APLICACIÓN DE ARANCEL. DISPOSICIÓN ADICIONAL 3.ª DE LA LEY 8/1989. BASES DE CÁLCULO: [BASES DE CÁLCULO]

ARANCEL APLICABLE: [ARANCEL APLICABLE]

DERECHOS ARANCELARIOS sin IVA: [IMPORTE] euros; cuota de IVA: [IMPORTE] euros; total factura: [IMPORTE] euros.

ES PRIMERA COPIA LITERAL de su matriz con la que concuerda fielmente y donde queda anotada. La expido a instancias de D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], en [NÚMERO] folios de papel exclusivo para documentos notariales, números [Nº] y los [NÚMERO] siguientes, el mismo día de su autorización. DOY FE.

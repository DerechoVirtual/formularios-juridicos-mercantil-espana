---
name: acta-junta-sl-sobre-cese-nombramiento-administradores-mer-0024
description: "Acta de junta de SL sobre cese y nombramiento de administradores o consejo de administración. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de junta de SL sobre cese y nombramiento de administradores o consejo de administración

> Formulario **MER-0024** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de acta de Junta General ( extraordinaria convocada o universal) de Socios de una Sociedad de Responsabilidad Limitada en la que se acuerda el cese del administrador único, de los administradores solidarios, mancomunados y del Consejo de Administración y se procede al nombramiento de otros, así como el cambio de los estatutos sociales en lo que afecte a tales ceses y nombramientos posteriores.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de junta de SL sobre cese y nombramiento de administradores o consejo de administración» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de junta de SL sobre cese y nombramiento de administradores o consejo de administración” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-junta-sl-sobre-cese-nombramiento-administradores-mer-0024`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (48 veces)
- [ ] Nº (20 veces)
- [ ] LOCALIDAD (14 veces)
- [ ] DENOMINACIÓN SOCIAL (9 veces)
- [ ] NACIONALIDAD (8 veces)
- [ ] NIF (8 veces)
- [ ] PUNTO DEL ORDEN DEL DÍA (8 veces)
- [ ] DIRECCIÓN (7 veces)
- [ ] FECHA (5 veces)
- [ ] CALLE (3 veces)
- [ ] MAYORÍA (2 veces)
- [ ] TEXTO DEL ACUERDO (2 veces)
- [ ] ÓRGANO (2 veces)
- [ ] DNI/NIE
- [ ] LUGAR
- [ ] Nº DE ARTÍCULO

## Normas que cita el formulario

- art. 196 Real Decreto Legislativo 1/2010

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

Modelo de acta de Junta General ( extraordinaria convocada o universal) de Socios de una Sociedad de Responsabilidad Limitada en la que se acuerda el cese del administrador único, de los administradores solidarios, mancomunados y del Consejo de Administración y se procede al nombramiento de otros, así como el cambio de los estatutos sociales en lo que afecte a tales ceses y nombramientos posteriores.


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

ACTA DE LA JUNTA GENERAL DE ‘, S.L.

[OPCIONAL — incluir si procede]

(Junta General Extraordinaria)

En [LOCALIDAD], siendo las [Nº] horas del día [FECHA], se reunió [ELEGIR: en primera convocatoria / en segunda convocatoria], en el domicilio social de ‘[DENOMINACIÓN SOCIAL], S.L.’ sito en [LOCALIDAD] la Junta General Extraordinaria de socios, previa convocatoria al efecto del [ELEGIR: administrador único / administrador solidario / administrador mancomunado / Consejo de Administración] de la citada mercantil realizada mediante

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Comunicación individual]

Que el texto íntegro de la convocatoria fue el siguiente:

CONVOCATORIA

D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

Estimado señor,

Por la presente, le comunicamos la próxima celebración de la junta general de la sociedad [DENOMINACIÓN SOCIAL] SL, de la que usted es socio, y le convocamos de acuerdo con lo previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales.

La junta general de socios se celebrará en la [DIRECCIÓN], de la localidad de [LOCALIDAD], y tendrá lugar, en primera convocatoria, el día [FECHA] a las [Nº] horas y, en segunda convocatoria, el día [FECHA] a las [Nº] horas.

La junta convocada tendrá el siguiente

ORDEN DEL DÍA

[OPCIONAL — incluir si procede]

(Administrador único)

1.- Cesar a D./Dña. [NOMBRE Y APELLIDOS], administrador único de ‘[DENOMINACIÓN SOCIAL], S.L.’ y nombrar nuevo administrador.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

(Administradores solidarios)

1.- Cesar a D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] administradores solidarios de ‘ S.L.’ y nombrar nuevos administradores solidarios.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

Administradores mancomunados

1.- Cesar a D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] administradores mancomunados de ‘[DENOMINACIÓN SOCIAL], S.L.’ y nombrar nuevos administradores mancomunados.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

(Consejo de Administración)

1.- Cesar al Consejo de Administración de ‘[DENOMINACIÓN SOCIAL], S.L.’ formado por D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], adoptando cuantos acuerdos sean necesarios, en concreto, nombrar nuevos miembros del Consejo.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

En su calidad de socio, y de conformidad con lo que dispone el artículo 196 del Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el texto refundido de la Ley de Sociedades de Capital, tiene derecho a solicitar por escrito, con anterioridad a la reunión de la junta general o verbalmente durante la misma, los informes o aclaraciones que estimen precisos acerca de los asuntos comprendidos en el orden del día.

El órgano de administración estará obligado a proporcionárselos, en forma oral o escrita de acuerdo con el momento y la naturaleza de la información solicitada, salvo en los casos en que, a juicio del propio órgano, la publicidad de ésta perjudique el interés social.

No procederá la denegación de la información cuando la solicitud esté apoyada por socios que representen, al menos, el veinticinco por ciento del capital social.

Actúa como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario D./Dña. [NOMBRE Y APELLIDOS], designados ambos por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las participaciones que poseen y/o representan cada uno de ellos:

Socios presentes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones sociales numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Socios representados:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], mayor de edad y con D.N.I [DNI/NIE] asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] participaciones sociales numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [Nº] participaciones sociales, que representan el % del capital social.

Todo el capital social de la compañía tiene derecho a voto.

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Junta.

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por

unanimidad

mayoría de [MAYORÍA] se adoptan los acuerdos cuyo contenido se transcribe a continuación

[OPCIONAL — incluir si procede]

(Junta universal)

En [LOCALIDAD], [DIRECCIÓN] a [FECHA], siendo las [Nº] horas, se hallan reunidos en el domicilio social de ‘[DENOMINACIÓN SOCIAL], S.L.’ la totalidad de sus socios, como consta en la lista de asistentes, que representan la totalidad del capital social, y acuerdan por unanimidad constituirse en Junta General Extraordinaria de carácter Universal, al amparo de lo previsto en el art. 178 de la vigente Ley de Sociedades de Capital y en el art. de los Estatutos Sociales para tratar y deliberar sobre el siguiente orden del día, que es unánimemente aceptado:

ORDEN DEL DÍA

[OPCIONAL — incluir si procede]

(Administrador único)

1.- Cesar a D./Dña. [NOMBRE Y APELLIDOS], administrador único de ‘[DENOMINACIÓN SOCIAL], S.L.’ y nombrar nuevo administrador.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

(Administradores solidarios)

1.- Cesar a D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] administradores solidarios de ‘ S.L.’ y nombrar nuevos administradores solidarios.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

(Administradores mancomunados)

1.- Cesar a D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] administradores mancomunados de ‘[DENOMINACIÓN SOCIAL], S.L.’ y nombrar nuevos administradores mancomunados.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

(Consejo de Administración)

1.- Cesar al Consejo de Administración de ‘[DENOMINACIÓN SOCIAL], S.L.’ formado por D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], adoptando cuantos acuerdos sean necesarios, en concreto, nombrar nuevos miembros del Consejo.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

Actúa como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario D./Dña. [NOMBRE Y APELLIDOS], designados ambos por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las participaciones que poseen y/o representan cada uno de ellos:

Socios presentes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Socios representados:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], mayor de edad y con D./Dña. [NOMBRE Y APELLIDOS] asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] participaciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [Nº] participaciones, que representan el % del capital social.

Todo el capital social de la compañía tiene derecho a voto.

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Junta.

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por

unanimidad

mayoría de [MAYORÍA] se adoptan los acuerdos cuyo contenido se transcribe a continuación

ACUERDOS

[OPCIONAL — incluir si procede]

Primero.- Cese del administrador único D./Dña. [NOMBRE Y APELLIDOS] y nombramiento de nuevo administrador

[ELEGIR UNA OPCIÓN: Caducidad / Acuerdo de Junta / Dimisión / Fallecimiento]

En la presente junta se procede a nombrar nuevo administrador único a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN] con DNI/NIF [NIF], quien, hallándose presente, acepta el cargo y manifiesta no estar incurso en ninguna prohibición, incompatibilidad o incapacidad para el ejercicio del mismo.

[OPCIONAL — incluir si procede]

Primero.- Cese de los administradores solidarios D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], y nombramiento de nuevos administradores solidarios

[ELEGIR UNA OPCIÓN: Dimisión / Caducidad / Fallecimiento / Acuerdo de Junta]

En la presente junta se procede a nombrar como nuevos administradores solidarios de la compañía a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la calle [CALLE] con DNI/NIF [NIF], y a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la calle [CALLE] con DNI/NIF [NIF], quienes, hallándose presentes, aceptan el cargo y manifiestan no hallarse incursos en ninguna prohibición, incompatibilidad o incapacidad para el ejercicio del mismo y en especial en ninguna de las circunstancias previstas en los arts. 229 y 230 Ley de Sociedades de Capital, que prohíben la competencia con las actividades de la sociedad.

[OPCIONAL — incluir si procede]

Primero.- Cese de los administradores mancomunados D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], y nombramiento de nuevos administradores mancomunados

[ELEGIR UNA OPCIÓN: Por acuerdo de la Junta / Dimisión / Caducidad / Fallecimiento]

En la presente junta se procede a nombrar como nuevos administradores mancomunados de la compañía a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino de [LOCALIDAD] con domicilio en la calle [CALLE] con DNI/NIF [NIF], y a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN] con DNI/NIF [NIF], quienes, hallándose presentes, aceptan el cargo y manifiestan no hallarse incursos en ninguna prohibición, incompatibilidad o incapacidad para el ejercicio del mismo y en especial en ninguna de las circunstancias previstas en el art. 229 Ley de Sociedades de Capital, que prohíbe la competencia con las actividades de la sociedad.

[OPCIONAL — incluir si procede]

Primero.- Cese del Consejo de Administración formado por D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] y nombramiento de nuevos consejeros.

[ELEGIR UNA OPCIÓN: Caducidad / Por acuerdo de la Junta / Dimisión / Fallecimiento]

Se procede a nombrar como nuevos administradores que integrarán el Consejo de Administración, por igual plazo de 5 años a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN] con DNI/NIF [NIF], D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN] con DNI/NIF [NIF], y D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino de [LOCALIDAD] con domicilio en la [DIRECCIÓN] con DNI/NIF [NIF], quienes, hallándose presente, aceptan el cargo y manifiesta no hallarse incursos en ninguna prohibición, incompatibilidad o incapacidad para el ejercicio del mismo.

Segundo.- [TEXTO DEL ACUERDO]

Tercero.- [TEXTO DEL ACUERDO]

Cuarto.- Facultad para elevar a público.

Facultar a [NOMBRE Y APELLIDOS] para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando a tales efectos las escrituras públicas correspondientes, incluidas las facultades de subsanación, rectificación o aclaración, así como para realizar cuantas actuaciones sean precisas o convenientes para la eficacia de los susodichos acuerdos.

Tras todo lo cual, redactada y leída que fue el acta por el Secretario, esta es aprobada por la Junta, por unanimidad de los asistentes.

No existiendo más asuntos que tratar, se levanta la sesión.

Secretario

Vº Bº Presidente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

Asistentes

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Firmado: D./Dña. [NOMBRE Y APELLIDOS]

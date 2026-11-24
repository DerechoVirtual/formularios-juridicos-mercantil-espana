---
name: acta-junta-sl-acuerda-reducir-capital-social-mer-0033
description: "Acta de junta de SL que acuerda reducir el capital social. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de junta de SL que acuerda reducir el capital social

> Formulario **MER-0033** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Acta de Junta General (Extraordinaria convocada o Universal) de Socios de una Sociedad de Responsabilidad Limitada en la que se acuerda la reducción de capital mediante la disminución del valor nominal de las participaciones sociales, su amortización o su agrupación, con la finalidad de restablecer el equilibrio entre el capital y el patrimonio neto de la sociedad disminuido por consecuencia de pérdidas, la constitución o el incremento de la reserva legal o de las reservas voluntarias o la devolución del valor de las aportaciones. Incluye también el acuerdo de modificación de los estatutos sociales en lo que afecte a esa reducción de capital. (Art. 317 TRLSC)

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de junta de SL que acuerda reducir el capital social» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de junta de SL que acuerda reducir el capital social” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-junta-sl-acuerda-reducir-capital-social-mer-0033`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (24 veces)
- [ ] NOMBRE Y APELLIDOS (19 veces)
- [ ] LOCALIDAD (11 veces)
- [ ] PUNTO DEL ORDEN DEL DÍA (8 veces)
- [ ] IMPORTE (7 veces)
- [ ] FECHA (5 veces)
- [ ] DIRECCIÓN (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] CALLE (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] NIF (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] ÓRGANO (2 veces)
- [ ] CARGO
- [ ] DNI/NIE
- [ ] FINALIDAD DE LA REDUCCIÓN
- [ ] LUGAR
- [ ] MEDIO DE PAGO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 287 Real Decreto Legislativo 1/2010
- art. 196 TRLSC

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

Acta de Junta General (Extraordinaria convocada o Universal) de Socios de una Sociedad de Responsabilidad Limitada en la que se acuerda la reducción de capital mediante la disminución del valor nominal de las participaciones sociales, su amortización o su agrupación, con la finalidad de restablecer el equilibrio entre el capital y el patrimonio neto de la sociedad disminuido por consecuencia de pérdidas, la constitución o el incremento de la reserva legal o de las reservas voluntarias o la devolución del valor de las aportaciones. Incluye también el acuerdo de modificación de los estatutos sociales en lo que afecte a esa reducción de capital. (Art. 317 TRLSC)


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

En [LOCALIDAD], siendo las [Nº] horas del día [FECHA], se reunió [ELEGIR: en primera convocatoria / en segunda convocatoria], en el domicilio social de ‘[DENOMINACIÓN SOCIAL], S.L.’ sito en [LOCALIDAD] calle [CALLE] de [LOCALIDAD] la Junta General Extraordinaria de socios, previa convocatoria al efecto del [ELEGIR: administrador único / administrador solidario / administrador mancomunado / Consejo de Administración] de la citada mercantil realizada mediante

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Comunicación individual]

El texto íntegro de la convocatoria fue el siguiente:

CONVOCATORIA

D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

Estimado señor,

Por la presente, le comunicamos la próxima celebración de la junta general de la sociedad [DENOMINACIÓN SOCIAL] SL, de la que usted es socio, y le convocamos de acuerdo con lo previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales.

La junta general de socios se celebrará en la [DIRECCIÓN], de la localidad de [LOCALIDAD], y tendrá lugar, en primera convocatoria, el día [FECHA] a las [Nº] horas y, en segunda convocatoria, el día [FECHA] a las [Nº] horas.

La junta convocada tendrá el siguiente

ORDEN DEL DÍA

[OPCIONAL — incluir si procede]

1.- Reducir el capital social para devolver aportaciones a los socios por cualquier procedimiento y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1. Reducir el capital social para compensar pérdidas, por cualquier procedimiento y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1. Reducir el capital social para constituir aumentar la reserva legal- voluntaria, por cualquier procedimiento y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1.- Reducir el capital social por el procedimiento de amortizar participaciones sociales propias y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

En su calidad de socio, y de conformidad con lo que dispone el artículo 287 del Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el texto refundido de la Ley de Sociedades de Capital, tiene derecho a examinar en el domicilio social el texto íntegro de la modificación estatutaria propuesta. En virtud de lo dispuesto en el artículo 196 TRLSC, también tiene derecho a solicitar, con anterioridad a la reunión de la junta o verbalmente durante la misma, los informes o aclaraciones que estime precisos acerca de los asuntos comprendidos en el orden del día.

Actúa como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario D./Dña. [NOMBRE Y APELLIDOS], designados ambos por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las participaciones que poseen y/o representan cada uno de ellos:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios presentes:

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones sociales numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios representados:

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], calle [CALLE], mayor de edad y con D.N.I. asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] participaciones sociales numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [Nº] participaciones sociales, que representan el % del capital social.

Todo el capital social de la compañía tiene derecho a voto.

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Junta.

Seguidamente, por indicación del Presidente, el Secretario da lectura al Orden del día, a continuación de lo cual se pasa al tratamiento de los puntos del mismo, y previa deliberación, se adoptan por unanimidad los siguientes acuerdos:

[OPCIONAL — incluir si procede]

(Junta universal)

En [LOCALIDAD], [DIRECCIÓN] a [FECHA], siendo las [Nº] horas, se hallan reunidos en el domicilio social de ‘[DENOMINACIÓN SOCIAL], S.L.’ la totalidad de sus socios, como consta en la lista de asistentes, que representan la totalidad del capital social, y acuerdan por unanimidad constituirse en Junta General Extraordinaria de carácter Universal, al amparo de lo previsto en el art. 178 de la vigente Ley de Sociedades de Capital y en el art. de los Estatutos Sociales para tratar y deliberar sobre el siguiente orden del día, que es unánimemente aceptado:

ORDEN DEL DÍA

[OPCIONAL — incluir si procede]

1.- Reducir el capital social para devolver aportaciones a los socios por cualquier procedimiento y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

[OPCIONAL — incluir si procede]

1. Reducir el capital social para compensar pérdidas, por cualquier procedimiento y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

[OPCIONAL — incluir si procede]

1. Reducir el capital social para constituir aumentar la reserva legal- voluntaria, por cualquier procedimiento y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

[OPCIONAL — incluir si procede]

1.- Reducir el capital social por el procedimiento de amortizar participaciones sociales propias y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

Actúa como Presidente D./Dña. [NOMBRE Y APELLIDOS] y, como Secretario, D./Dña.. [NOMBRE Y APELLIDOS], designados ambos conforme a los Estatutos Sociales, por acuerdo unánime de los reunidos.

Abierta la sesión por el Sr. Presidente, el Sr. Secretario pasa lista de asistentes, constatándose la concurrencia a la Junta de la totalidad de los socios, que firman a continuación de sus nombres y que representan la totalidad del capital social.

LISTA DE ASISTENTES:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios Presentes

D./Dña. [NOMBRE Y APELLIDOS], asiste personalmente, como titular de las participaciones sociales

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios representados

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], mayor de edad y con D.N.I. asiste en nombre y representación, según acredita mediante [ÓRGANO] de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] participaciones sociales numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

En consecuencia, asisten, entre presentes y representados, el 100% del capital social.

En su virtud, ratificada por todos ellos su decisión de reunirse en Junta General Extraordinaria Universal, el Presidente declara válidamente constituida la misma.

Seguidamente, por indicación del Presidente, el Secretario da lectura al Orden del día, a continuación de lo cual se pasa al tratamiento de los puntos del mismo, y previa deliberación, se adoptan por unanimidad los siguientes

ACUERDOS:

Primero. Reducción de capital social.

a) Cuantía y finalidad de la Reducción

Reducir el capital social de la entidad en la cifra de [IMPORTE] euros, con la finalidad de [FINALIDAD DE LA REDUCCIÓN]
devolver aportaciones a los socios
restablecer el equilibrio entre el capital y el patrimonio contable disminuido por pérdidas
constituir/aumentar la reserva- legal- voluntaria
amortizar participaciones sociales propias

b) Procedimiento

[OPCIONAL — incluir si procede]

Para restitución de aportaciones, compensación de pérdidas y constitución o aumento de reservas legales y voluntarias

[ELEGIR UNA OPCIÓN: Mediante reducción del valor nominal / Mediante amortización de participaciones / Mediante agrupación de participaciones]

[OPCIONAL — incluir si procede]

Para restitución de aportaciones:

- Que los Estatutos sociales reconocen a los acreedores derecho de oposición al acuerdo de reducción.

- Que a efectos del ejercicio del citado derecho

[ELEGIR UNA OPCIÓN: Notificación personal / Acuerdo publicado en el BORME y en la página web de la sociedad]

- Que ningún acreedor ha ejercitado en plazo su derecho de oposición.

[OPCIONAL — incluir si procede]

(Si hay oposición)

- Que únicamente han ejercitado en plazo su derecho de oposición los siguientes acreedores:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD], y DNI [DNI/NIE], titular de un crédito contra la sociedad por importe de [IMPORTE] euros.

A D./Dña. [NOMBRE Y APELLIDOS] se le ha garantizado su crédito a su entera satisfacción

Dicho crédito ha sido abonado por la sociedad, antes de este acto.

La reducción se efectúa restituyendo a los socios un total de [IMPORTE] euros la cual se hará efectiva en la misma proporción en que han sufrido la reducción, de la siguiente forma:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN], y con DNI/NIF [NIF] titular de [Nº] participaciones sociales, números [Nº] a [Nº], ambas inclusive, recibe la cantidad de [IMPORTE] euros en efectivo [MEDIO DE PAGO],

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN], y con DNI/NIF [NIF] titular de [Nº] participaciones sociales, números [Nº] a [Nº], ambas inclusive, recibe como adjudicación no dineraria: que se entrega en pleno dominio, y libre de toda carga, gravamen, o arrendamiento

A los efectos de lo establecido en el art. 332 de la Ley de Sociedades de Capital se acuerda constituir una reserva con cargo a beneficios o reservas libres y por un importe igual al percibido por los socios en concepto de restitución de aportaciones, la cual tendrá carácter de indisponible en los términos legalmente previstos.

[OPCIONAL — incluir si procede]

Para compensación de pérdidas y constitución o aumento de reservas legales y voluntarias

[ELEGIR UNA OPCIÓN: Con balance ad hoc / Con otro balance]

[OPCIONAL — incluir si procede]

Para amortización de participaciones propias

Amortizar las participaciones números a [Nº], con un valor nominal global de [IMPORTE] euros.

[OPCIONAL — incluir si procede]

Adquiridas por la sociedad bajo los supuestos legalmente previstos.

[OPCIONAL — incluir si procede]

Adquiridas por la sociedad dentro de un patrimonio obtenido a título universal.

[OPCIONAL — incluir si procede]

Adquiridas por la sociedad a título gratuito.

[OPCIONAL — incluir si procede]

Adquiridas por la sociedad por adjudicación judicial para pagar un crédito de la sociedad contra su titular.

[OPCIONAL — incluir si procede]

Adquiridas por la sociedad en el caso de adquisición forzosa previsto en el art.109.3 de la Ley de Sociedades de Capital

[OPCIONAL — incluir si procede]

Adquiridas por la sociedad con autorización expresa de la Junta General, con cargo a [ELEGIR: beneficios / reservas de libre disposición] y con la finalidad de:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Obtener las participaciones de un socio separado o excluido

Obtener las participaciones como consecuencia de la aplicación de una cláusula restrictiva de las mismas

Obtener las participaciones transmitidas mortis causa.

Puesto que la amortización no comporta devolución de aportaciones a los socios, se decide dotar la ‘Reserva ‘ por el importe del valor nominal de las participaciones amortizadas, reserva que será indisponible hasta que transcurran 5 años desde la publicación de la reducción, salvo que antes del vencimiento de dicho plazo hayan sido satisfechas todas las deudas sociales contraídas con anterioridad a la fecha en que la reducción sea oponible a terceros.

Segundo. Modificación de Estatutos

Se acuerda por unanimidad modificar el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"Art - El capital de la sociedad es de [IMPORTE] euros y está representado por [ÓRGANO O PERSONA] participaciones, de valor nominal [IMPORTE] euros cada una de ellas, numeradas correlativamente del 1 al [Nº], ambos inclusive. Todas las participaciones confieren los mismos derechos y obligaciones y están totalmente desembolsadas en el 100% de su valor nominal’.

Tercero.- Elevación a público

Se faculta a D./Dña. [NOMBRE Y APELLIDOS], en su calidad de [CARGO] para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando para ello las escrituras correspondientes, incluidas, en su caso, las de subsanación, aclaración o rectificación, así como para realizar cuantas operaciones fueren precisas para la plena eficacia de dichos acuerdos.

Abierto el turno de ruegos y preguntas, no se formula ninguna y siendo las [Nº] horas del mismo día, se levanta la sesión por el Presidente, de la que se extiende la presente acta que, leída por todos los asistentes, se aprueba por unanimidad y es seguidamente firmada por el Secretario, con el Vº bueno del Presidente y por todos los asistentes.

Secretario

Vº Bº Presidente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

Asistentes

Firmado: D./Dña. [NOMBRE Y APELLIDOS]

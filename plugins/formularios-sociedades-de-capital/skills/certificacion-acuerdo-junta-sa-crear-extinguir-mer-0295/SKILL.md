---
name: certificacion-acuerdo-junta-sa-crear-extinguir-mer-0295
description: "Certificación del acuerdo de junta de una SA de crear o extinguir prestaciones accesorias. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación del acuerdo de junta de una SA de crear o extinguir prestaciones accesorias

> Formulario **MER-0295** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de certificado de Acta de Junta General Extraordinaria o Universal de socios de una Sociedad Anónima en el que se certifica el acuerdo sobre la creación o extinción anticipada de determinadas prestaciones accesorias de carácter gratuito o retribuido exigibles a los accionistas, a la vista del informe de los administradores realizado al efecto, así como la adopción de los acuerdos necesarios para la modificación, en su caso, de los estatutos sociales.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación del acuerdo de junta de una SA de crear o extinguir prestaciones accesorias» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación del acuerdo de junta de una SA de crear o extinguir prestaciones accesorias” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdo-junta-sa-crear-extinguir-mer-0295`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (15 veces)
- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] FECHA (6 veces)
- [ ] Nº DE ARTÍCULO (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] DESCRIBIR (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] ACCIONES AFECTADAS (3 veces)
- [ ] ACCIONISTAS AFECTADOS (2 veces)
- [ ] CALLE (2 veces)
- [ ] LUGAR (2 veces)
- [ ] DIRECCIÓN
- [ ] MAYORÍA
- [ ] OBJETO DE LA PRESTACIÓN ACCESORIA
- [ ] PUNTO DEL ORDEN DEL DÍA
- [ ] RETRIBUCIÓN
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 197 Real Decreto Legislativo 1/2010

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

Modelo de certificado de Acta de Junta General Extraordinaria o Universal de socios de una Sociedad Anónima en el que se certifica el acuerdo sobre la creación o extinción anticipada de determinadas prestaciones accesorias de carácter gratuito o retribuido exigibles a los accionistas, a la vista del informe de los administradores realizado al efecto, así como la adopción de los acuerdos necesarios para la modificación, en su caso, de los estatutos sociales.


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

CERTIFICADO DE ACTA DE JUNTA GENERAL DE ‘[DENOMINACIÓN SOCIAL], S.A.’

En [LUGAR], a [FECHA].

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de Secretario del Consejo de Administración de ‘[DENOMINACIÓN SOCIAL], S.A.’ y de su Junta de accionistas reunida el pasado [FECHA]

CERTIFICO

[OPCIONAL — incluir si procede]

(Junta General Extraordinaria)

Que siendo las [Nº] horas del día [FECHA], se reunió en [ELEGIR: primera / segunda] convocatoria, en el domicilio social de ‘[DENOMINACIÓN SOCIAL], S.A.’ sito en [LOCALIDAD] calle [CALLE] de [LOCALIDAD] la Junta General Extraordinaria de socios, previa convocatoria al efecto del [ELEGIR: administrador único / administrador solidario / administrador mancomunado / Consejo de Administración] de la citada mercantil realizada mediante

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Comunicación individual]

Que el texto íntegro de la convocatoria fue el siguiente:

CONVOCATORIA

D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

Estimado señor,

Por la presente, le comunicamos la próxima celebración de la junta general de la sociedad [DENOMINACIÓN SOCIAL] SA, de la que usted es socio, y le convocamos de acuerdo con lo previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales.

La junta general de socios se celebrará en la [DIRECCIÓN], de la localidad de [LOCALIDAD], y tendrá lugar, en primera convocatoria, el día [FECHA] a las [Nº] horas y, en segunda convocatoria, el día [FECHA] a las [Nº] horas.

La junta convocada tendrá el siguiente

ORDEN DEL DÍA

[OPCIONAL — incluir si procede]

1º) Crear prestaciones accesorias consistentes en [DESCRIBIR] para los accionistas [ACCIONISTAS AFECTADOS], y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

[OPCIONAL — incluir si procede]

1º) Extinguir anticipadamente las prestaciones accesorias consistentes en [DESCRIBIR] vigentes para los accionistas [ACCIONISTAS AFECTADOS], y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

2º) [PUNTO DEL ORDEN DEL DÍA]

3º) Ruegos y preguntas.

4º) Aprobación, en su caso, del acta de la Junta.

En su calidad de socio, y de conformidad con lo que dispone el artículo 197 del Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el texto refundido de la Ley de Sociedades de Capital, hasta el séptimo día anterior al previsto para la celebración de la junta, los accionistas podrán solicitar de los administradores las informaciones o aclaraciones que estimen precisas acerca de los asuntos comprendidos en el orden del día, o formular por escrito las preguntas que consideren pertinentes.

Que actuó como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario D./Dña. [NOMBRE Y APELLIDOS], designados ambos por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

Que el Presidente, asistido por el Secretario, procedió a elaborar la lista de asistentes que a continuación se relata, con detalle de las participaciones que poseen y/o representan cada uno de ellos:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios presentes

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios representados

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], calle [CALLE], mayor de edad y con D.N.I. asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

Que, en consecuencia, asistieron, entre presentes y representados, un total de [Nº] socios, titulares de [Nº] acciones, que representan el % del capital social.

No existen en la sociedad titulares de derechos especiales distintos de las acciones.

Todo el capital social de la compañía tiene derecho a voto.

Por lo tanto, por el Presidente se procedió a declarar válidamente constituida la Junta.

Que por indicación del Presidente, el Secretario dio lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por

unanimidad

mayoría de [MAYORÍA] se adoptan los acuerdos cuyo contenido se transcribe a continuación

ACUERDOS

[OPCIONAL — incluir si procede]

Primero.- Creación de prestaciones accesorias

A) Modificación de los estatutos.

A la vista del informe de los administradores al efecto, y de la propuesta de modificación, se acuerda la creación de prestaciones accesorias consistentes en [DESCRIBIR], de carácter [ELEGIR: gratuito / retribuido], y exigibles a los accionistas titulares de las acciones [ACCIONES AFECTADAS], quienes en muestra de su consentimiento individual lo hacen constar de forma separada al final del acta; por lo que, en consecuencia, se acuerda modificar el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo quedará redactado de la siguiente forma:

"Art [Nº DE ARTÍCULO] - Prestaciones accesorias: Consisten en [OBJETO DE LA PRESTACIÓN ACCESORIA], son de carácter [ELEGIR: gratuito / retribuido], y exigibles a los accionistas titulares de las acciones [ACCIONES AFECTADAS].

[ELEGIR UNA OPCIÓN: Si las acciones se representan mediante títulos / Si las acciones se representan por medio de anotaciones en cuenta]

[OPCIONAL — incluir si procede]

Primero.- Extinción anticipada de prestaciones accesorias

A) A la vista del informe de los administradores al efecto, y de la propuesta de modificación, se acuerda la extinción de las prestaciones accesorias consistentes en [DESCRIBIR], de carácter [ELEGIR: gratuito / retribuido]. [RETRIBUCIÓN], y exigibles a los accionistas titulares de las acciones [ACCIONES AFECTADAS], vigentes hasta este momento, quienes en muestra de su consentimiento individual lo hacen constar de forma separada al final del acta; por lo que, en consecuencia, se acuerda modificar el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo quedará redactado de la siguiente forma:

"Art [Nº DE ARTÍCULO] - Prestaciones accesorias: ’

[ELEGIR UNA OPCIÓN: Si las acciones se representan mediante títulos / Si las acciones se representan por medio de anotaciones en cuenta]

Segundo.- Se faculta al Secretario del Consejo de Administración para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando para ello las escrituras correspondientes, incluidas, en su caso, las de subsanación, aclaración o rectificación, así como para realizar cuantas operaciones fueren precisas para la plena eficacia de dichos acuerdos.

Tercero.- Abierto el turno de ruegos y preguntas, no se formula ninguna.

Consentimiento de cada uno de los afectados por el acuerdo de creación de prestaciones accesorias

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Estando presentes en este acto:

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Y dado que el citado acuerdo de creación de prestaciones accesorias afecta a las acciones de su titularidad, estando todos ellos conformes con el citado acuerdo, firman a continuación en muestra de la prestación de su consentimiento individual al mismo.

D./Dña. [NOMBRE Y APELLIDOS]

Y siendo las [Nº] horas del mismo día, se levanta la sesión por el Presidente, de la que se extiende la presente acta que, leída por todos los asistentes, se aprueba por unanimidad y es seguidamente firmada por todos ellos.

Secretario

D./Dña. [NOMBRE Y APELLIDOS]

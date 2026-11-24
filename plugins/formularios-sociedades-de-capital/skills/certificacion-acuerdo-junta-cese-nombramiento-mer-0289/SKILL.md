---
name: certificacion-acuerdo-junta-cese-nombramiento-mer-0289
description: "Certificación del acuerdo de junta de cese y nombramiento de administradores de una sociedad anónima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación del acuerdo de junta de cese y nombramiento de administradores de una sociedad anónima

> Formulario **MER-0289** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de certificado de Acta de Junta General Extraordinaria convocada o universal de Accionistas de una Sociedad Anónima en el que se certifica el acuerdo de cese del administrador único, administradores solidarios, administradores mancomunados y Consejo de Administración de la compañía y el nombramiento de otros, así como la adopción de los acuerdos que sean precisos para proceder a esa renovación.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación del acuerdo de junta de cese y nombramiento de administradores de una sociedad anónima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación del acuerdo de junta de cese y nombramiento de administradores de una sociedad anónima” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdo-junta-cese-nombramiento-mer-0289`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (25 veces)
- [ ] LOCALIDAD (11 veces)
- [ ] Nº (11 veces)
- [ ] NACIONALIDAD (8 veces)
- [ ] NIF (8 veces)
- [ ] DIRECCIÓN (6 veces)
- [ ] FECHA (5 veces)
- [ ] CALLE (4 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] PISO (3 veces)
- [ ] ACUERDO ADOPTADO (2 veces)
- [ ] CARGO
- [ ] DNI/NIE
- [ ] LUGAR
- [ ] MAYORÍA
- [ ] Nº DE ARTÍCULO
- [ ] PUNTO DEL ORDEN DEL DÍA
- [ ] ÓRGANO

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

Modelo de certificado de Acta de Junta General Extraordinaria convocada o universal de Accionistas de una Sociedad Anónima en el que se certifica el acuerdo de cese del administrador único, administradores solidarios, administradores mancomunados y Consejo de Administración de la compañía y el nombramiento de otros, así como la adopción de los acuerdos que sean precisos para proceder a esa renovación.


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

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de [CARGO] de ‘[DENOMINACIÓN SOCIAL], S.A.’ reunida el pasado [FECHA]

CERTIFICO

Que en [LOCALIDAD], siendo las [Nº] horas del día [FECHA], se reunió en el domicilio social de ‘[DENOMINACIÓN SOCIAL], S.A.’ en [ELEGIR: primera / segunda] convocatoria, la Junta General Extraordinaria de Accionistas, previa convocatoria al efecto [ELEGIR: del administrador único / de los administradores solidarios / de los administradores mancomunados / del Consejo de Administración] saliente/es de la citada mercantil realizada mediante:

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Comunicación individual]

Que el texto íntegro de la convocatoria fue el siguiente:

‘CONVOCATORIA DE JUNTA GENERAL DE ‘[DENOMINACIÓN SOCIAL], S.A.’

Se convoca Junta General a celebrar en el domicilio social de la compañía, sito en la calle [CALLE] de [LOCALIDAD] el día [FECHA] a las [Nº] horas en primera convocatoria y en el mismo lugar el día [FECHA] a las [Nº] horas (por lo menos, 24 horas después), con el siguiente ORDEN DEL DÍA:

[ELEGIR UNA OPCIÓN: Administrador único / Administradores solidarios / Administradores mancomunados / Consejo de Administración]

2.- [PUNTO DEL ORDEN DEL DÍA]

3.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la Junta y otorgamiento de facultades para ejecución y elevación a público de los acuerdos adoptados.

Los accionistas tienen derecho a examinar en el domicilio social el texto íntegro de la propuesta y de su informe, así como los documentos que deban ser sometidos a aprobación por la Junta, y de solicitar su entrega o envío gratuito.’

Que según lo previsto en el art [Nº DE ARTÍCULO] de los estatutos sociales de la compañía actuó como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS], y como Secretario yo, D./Dña. [NOMBRE Y APELLIDOS], designados que fuimos ambos por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

Que el Presidente, asistido por mí, el Secretario, procedió a elaborar la lista de asistentes que a continuación se relata, con detalle de las acciones que poseen y/o representaron cada uno de ellos:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Accionistas presentes:

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Accionistas representados:

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], calle [CALLE], mayor de edad y con D.N.I [DNI/NIE] asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Que todas las citadas representaciones se acreditaron de forma legal, a satisfacción de la Junta.

Que, en consecuencia, asistieron, entre presentes y representados, un total de [Nº] accionistas, titulares de [Nº] acciones sociales, que representaron el % del capital social con derecho a voto.

Que todo el capital social de la compañía tiene derecho a voto.

Que por lo tanto, por el Presidente se procedió a declarar válidamente constituida la Junta.

Que sobre las citadas manifestaciones del Presidente ningún asistente protestó ni presentó reserva alguna.

Que por indicación del Presidente, yo, el Secretario di lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por una mayoría de [MAYORÍA] se adoptaron los acuerdos cuyo contenido se transcribe a continuación:

ACUERDOS

[OPCIONAL — incluir si procede]

Primero.- Cese del administrador único D./Dña. [NOMBRE Y APELLIDOS] y nombramiento de nuevo administrador único

[ELEGIR UNA OPCIÓN: Caducidad / Acuerdo de Junta / Dimisión / Fallecimiento]

Se procede a nombrar nuevo administrador único a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino de [LOCALIDAD] con domicilio en la [DIRECCIÓN] con DNI/NIF [NIF], quien, hallándose presente, acepta el cargo y manifiesta no hallarse incurso en ninguna prohibición, incompatibilidad o incapacidad para el ejercicio del mismo.

[OPCIONAL — incluir si procede]

Primero.- Cese de los administradores solidarios D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], y nombramiento de nuevos administradores solidarios

[ELEGIR UNA OPCIÓN: Dimisión / Caducidad / Fallecimiento / Acuerdo de Junta]

Se procede a nombrar como nuevos administradores solidarios de la compañía a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la calle [CALLE] nº [NÚMERO] piso [PISO] con DNI/NIF [NIF], y a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN] con DNI/NIF [NIF], quienes, hallándose presentes, aceptan el cargo y manifiestan no hallarse incursos en ninguna prohibición, incompatibilidad o incapacidad para el ejercicio del mismo.

[OPCIONAL — incluir si procede]

Primero.- Cese de los administradores mancomunados D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], y nombramiento de nuevos administradores mancomunados

[ELEGIR UNA OPCIÓN: Por acuerdo de la Junta / Dimisión / Caducidad / Fallecimiento]

Se procede a nombrar como nuevos administradores mancomunados de la compañía a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la calle [CALLE] nº [NÚMERO] piso [PISO] con DNI/NIF [NIF], y a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN] con DNI/NIF [NIF], quienes, hallándose presentes, aceptan el cargo y manifiestan no hallarse incursos en ninguna prohibición, incompatibilidad o incapacidad para el ejercicio del mismo.

[OPCIONAL — incluir si procede]

Primero.- Cese del Consejo de Administración formado por D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] y nombramiento de nuevos consejeros

[ELEGIR UNA OPCIÓN: Caducidad / Por acuerdo de la Junta / Dimisión / Fallecimiento]

Se procede a nombrar como nuevos administradores que integrarán el Consejo de Administración, por igual plazo de 5 años a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN] nº [NÚMERO] piso [PISO] con DNI/NIF [NIF], D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN] con DNI/NIF [NIF], y D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD] vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN] con DNI/NIF [NIF], quienes, hallándose presente, aceptan el cargo y manifiesta no hallarse incursos en ninguna prohibición, incompatibilidad o incapacidad para el ejercicio del mismo.

Segundo.- [ACUERDO ADOPTADO]

Tercero.- [ACUERDO ADOPTADO]

Cuarto.- Facultad para elevar a público

Facultar a [NOMBRE Y APELLIDOS] para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando a tales efectos las escrituras públicas correspondientes, incluidas las facultades de subsanación, rectificación o aclaración, así como para realizar cuantas actuaciones sean precisas o convenientes para la eficacia de los susodichos acuerdos’.

Tras todo lo cual, redactada y leída que fue el acta por mí, el Secretario, esta fue aprobada por la Junta, por unanimidad de los asistentes.

No existiendo más asuntos que tratar, se levantó la sesión.

Secretario

VºBº Presidente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

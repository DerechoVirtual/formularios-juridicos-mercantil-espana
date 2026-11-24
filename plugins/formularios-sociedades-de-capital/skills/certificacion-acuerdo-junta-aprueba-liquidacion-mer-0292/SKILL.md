---
name: certificacion-acuerdo-junta-aprueba-liquidacion-mer-0292
description: "Certificación del acuerdo de junta que aprueba la liquidación de una sociedad anónima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación del acuerdo de junta que aprueba la liquidación de una sociedad anónima

> Formulario **MER-0292** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Certificado del acta de la Junta General Extraordinaria de accionistas de una sociedad anónima en liquidación, en el que se certifica el acuerdo de aprobar el balance final de liquidación, el informe sobre las operaciones liquidatorias, la cuota de liquidación y su reparto (si queda remanente), con la facultad de elevar a público los acuerdos.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación del acuerdo de junta que aprueba la liquidación de una sociedad anónima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación del acuerdo de junta que aprueba la liquidación de una sociedad anónima” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdo-junta-aprueba-liquidacion-mer-0292`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (10 veces)
- [ ] Nº (10 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] HORA (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] DIRECCIÓN DE LA PÁGINA WEB
- [ ] DNI/NIE
- [ ] DOCUMENTO ACREDITATIVO DE LA REPRESENTACIÓN
- [ ] FORMA DE PAGO O ADJUDICACIÓN
- [ ] IMPORTE
- [ ] INCORPORAR EL BALANCE FINAL DE LIQUIDACIÓN
- [ ] INCORPORAR EL INFORME COMPLETO SOBRE LAS OPERACIONES LIQUIDATORIAS
- [ ] MAYORÍA
- [ ] NOMBRE DEL DIARIO
- [ ] NOMBRE Y APELLIDOS DEL ACCIONISTA REPRESENTADO
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE
- [ ] OTROS PUNTOS DEL ORDEN DEL DÍA, SI LOS HUBIERA
- [ ] REPETIR EL SIGUIENTE PÁRRAFO TANTAS VECES COMO ACCIONISTAS PRESENTES:

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

CERTIFICADO DE ACTA DE JUNTA GENERAL DE [DENOMINACIÓN SOCIAL], S.A., en liquidación

En [LOCALIDAD], a [FECHA].

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de Secretario del Consejo de liquidación de [DENOMINACIÓN SOCIAL], S.A., en liquidación, y de su Junta de accionistas reunida el pasado [FECHA],

CERTIFICO

Que en [LOCALIDAD], siendo las [HORA] horas del día [FECHA], se reunió en el domicilio social de [DENOMINACIÓN SOCIAL], S.A., en [ELEGIR: primera / segunda] convocatoria, la Junta General Extraordinaria de Accionistas, previa convocatoria al efecto del [ELEGIR: administrador único / administradores solidarios / administradores mancomunados / Consejo de Administración] de la citada mercantil, realizada mediante:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Con página web) Anuncio en la página web de la sociedad [DIRECCIÓN DE LA PÁGINA WEB] desde el [FECHA] hasta la fecha de la celebración de la junta, el [FECHA], y alerta telemática a los correos electrónicos correspondientes a cada socio de los anuncios de convocatoria insertados en la web.

— (Sin página web) Anuncio publicado en el Boletín Oficial del Registro Mercantil n.º [Nº], correspondiente al día [FECHA], y en el diario [NOMBRE DEL DIARIO] de [LOCALIDAD] del [FECHA].

— (Comunicación individual) El procedimiento de comunicación individual y escrita previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales, habiendo sido remitido el anuncio al último de los socios con fecha de [FECHA].

Que el texto íntegro de la convocatoria fue el siguiente:

«CONVOCATORIA DE JUNTA GENERAL DE [DENOMINACIÓN SOCIAL], S.A.

Se convoca Junta General a celebrar en el domicilio social de la compañía, sito en la calle [DOMICILIO] de [LOCALIDAD], el día [FECHA], a las [HORA] horas, en primera convocatoria, y en el mismo lugar el día [FECHA], a las [HORA] horas (por lo menos, 24 horas después), en segunda convocatoria, con el siguiente

ORDEN DEL DÍA:

1.º) Liquidar la sociedad, adoptando cuantos acuerdos complementarios sean precisos y, en concreto, procediéndose, en su caso, a la aprobación del balance final de liquidación y a la determinación de la cuota de liquidación y de la propuesta para su reparto.

2.º) [OTROS PUNTOS DEL ORDEN DEL DÍA, SI LOS HUBIERA]

3.º) Ruegos y preguntas.

4.º) Aprobación, en su caso, del acta de la Junta.

Los accionistas tienen derecho a examinar en el domicilio social el texto íntegro de la liquidación propuesta y de su informe, así como los documentos que deban ser sometidos a aprobación por la Junta, y a solicitar su entrega o envío gratuito.»

Que, según lo previsto en el art. [Nº DE ARTÍCULO] de los estatutos sociales de la compañía, actuó como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario yo, D./Dña. [NOMBRE Y APELLIDOS], designados que fuimos ambos por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

Que el Presidente, asistido por mí, el Secretario, procedió a elaborar la lista de asistentes que a continuación se relata, con detalle de las acciones que poseen y/o representaron cada uno de ellos:

Accionistas presentes:

[REPETIR EL SIGUIENTE PÁRRAFO TANTAS VECES COMO ACCIONISTAS PRESENTES:]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE]% del total del capital social con derecho a voto.

Accionistas representados:

[REPETIR EL SIGUIENTE PÁRRAFO TANTAS VECES COMO ACCIONISTAS REPRESENTADOS:]

D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTANTE], vecino/a de [LOCALIDAD], calle [DOMICILIO], mayor de edad y con DNI [DNI/NIE], asiste en nombre y representación, según acredita mediante [DOCUMENTO ACREDITATIVO DE LA REPRESENTACIÓN], de D./Dña. [NOMBRE Y APELLIDOS DEL ACCIONISTA REPRESENTADO], titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE]% del total del capital social con derecho a voto.

Que todas las citadas representaciones se acreditaron de forma legal, a satisfacción de la Junta.

Que, en consecuencia, asistieron, entre presentes y representados, un total de [Nº] accionistas, titulares de [Nº] acciones, que representaron el [PORCENTAJE]% del capital social con derecho a voto.

Que todo el capital social de la compañía tiene derecho a voto.

Que, por lo tanto, por el Presidente se procedió a declarar válidamente constituida la Junta.

Que sobre las citadas manifestaciones del Presidente ningún asistente protestó ni presentó reserva alguna.

Que, por indicación del Presidente, yo, el Secretario, di lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por una mayoría de [MAYORÍA] se adoptaron los acuerdos cuyo contenido se transcribe a continuación:

ACUERDOS

Primero.- Liquidación de la sociedad

La sociedad queda liquidada de conformidad con los siguientes extremos:

1.º) Balance final. Aprobar el balance final de liquidación presentado por los liquidadores, que se une a la presente acta como Anexo I. (El balance debe ser censurado por los interventores, si es que éstos han sido nombrados.)

2.º) Informe sobre las operaciones liquidatorias. Aprobar el informe completo sobre las operaciones liquidatorias presentado por los liquidadores, que se une a la presente acta como Anexo II.

3.º) Cuota de liquidación. Fijar la cuota de liquidación en la suma de [IMPORTE] euros por acción, correspondiente a cada una de las [Nº] acciones que integran el total del capital social de la compañía, las cuales se encuentran todas ellas liberadas.

4.º) Proyecto de división entre los socios del activo resultante. Aprobar la división del remanente social, determinando el abono de la cuota de liquidación correspondiente a cada acción mediante [FORMA DE PAGO O ADJUDICACIÓN].

Segundo.- Facultad para elevar a público

Facultar a todos y cada uno de los miembros del órgano de liquidación para que, indistintamente, puedan comparecer ante Notario y elevar a público los presentes acuerdos, otorgando a tales efectos las escrituras públicas correspondientes, incluidas las facultades de subsanación, rectificación o aclaración, así como para realizar cuantas actuaciones sean precisas o convenientes para la eficacia de los susodichos acuerdos.

Tras todo lo cual, redactada y leída que fue el acta por mí, el Secretario, esta fue aprobada por la Junta, por unanimidad de los asistentes.

No existiendo más asuntos que tratar, se levantó la sesión.

V.º B.º El Presidente | El Secretario

Firmado: D./Dña. [NOMBRE Y APELLIDOS] | Firmado: D./Dña. [NOMBRE Y APELLIDOS]

ANEXO I: BALANCE FINAL

[INCORPORAR EL BALANCE FINAL DE LIQUIDACIÓN]

ANEXO II: INFORME SOBRE LAS OPERACIONES LIQUIDATORIAS

[INCORPORAR EL INFORME COMPLETO SOBRE LAS OPERACIONES LIQUIDATORIAS]

NOTAS DE USO

1. Elevación a público de los acuerdos (art. 107 del Reglamento del Registro Mercantil): la elevación a instrumento público de los acuerdos de la Junta o Asamblea general o especial y de los acuerdos de los órganos colegiados de administración podrá realizarse tomando como base el acta o libro de actas, testimonio notarial de los mismos o certificación de los acuerdos. También podrá realizarse tomando como base la copia autorizada del acta, cuando los acuerdos constaren en acta notarial. En la escritura de elevación a público del acuerdo social deberán consignarse todas las circunstancias del acta que sean necesarias para calificar la validez de aquél. En su caso, el Notario testimoniará en la escritura el anuncio de convocatoria publicado o protocolizará testimonio notarial del mismo.

2. Legitimación para elevar a público (art. 108 del Reglamento del Registro Mercantil): corresponde a la persona que tenga facultad para certificar los acuerdos. Las decisiones del socio único, consignadas en acta bajo su firma o la de su representante, podrán ser ejecutadas y formalizadas por el propio socio o por los administradores de la sociedad. También podrá realizarse por cualquiera de los miembros del órgano de administración con nombramiento vigente e inscrito en el Registro Mercantil, cuando hubieren sido expresamente facultados para ello en la escritura social o en la reunión en que se hayan adoptado los acuerdos. La elevación a instrumento público por cualquier otra persona requerirá el otorgamiento de la oportuna escritura de poder, que podrá ser general para todo tipo de acuerdos, en cuyo caso deberá inscribirse en el Registro Mercantil. Este procedimiento no será aplicable para elevar a públicos los acuerdos sociales cuando se tome como base para ello el acta o testimonio notarial de la misma.

3. Reparto del haber social: es imprescindible su detalle y datos registrales (art. 247.3, párrafo segundo, del Reglamento del Registro Mercantil) y también la comparecencia de los socios beneficiados para que se puedan inscribir a su nombre en el Registro de la Propiedad. Confirma esta tesis la resolución de la Dirección General de los Registros y del Notariado de 13 de octubre de 2004 (BOE de 4 de diciembre de 2004): para la inscripción en el Registro Mercantil sí es suficiente la escritura otorgada por el liquidador, pero para la inscripción en el Registro de la Propiedad no es bastante que el liquidador certifique sobre los referidos acuerdos sociales, toda vez que su certificación no es más que un documento privado, sin el valor ni los importantes efectos que en nuestro Derecho se atribuyen al documento autorizado por un funcionario público.

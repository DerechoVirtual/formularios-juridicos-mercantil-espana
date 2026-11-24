---
name: acta-junta-general-extraordinaria-universal-sl-acuerda-mer-0021
description: "Acta de junta general extraordinaria y universal de SL que acuerda emitir obligaciones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de junta general extraordinaria y universal de SL que acuerda emitir obligaciones

> Formulario **MER-0021** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de acuerdo de una Junta General, extraordinaria convocada o universal, de socios de una Sociedad Limitada, mediante la cual se adopta una acuerdo de emisión de obligaciones, estableciendo en el mismo las condiciones necesarias para su cumplimiento.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de junta general extraordinaria y universal de SL que acuerda emitir obligaciones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de junta general extraordinaria y universal de SL que acuerda emitir obligaciones” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-junta-general-extraordinaria-universal-sl-acuerda-mer-0021`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (22 veces)
- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (6 veces)
- [ ] DIRECCIÓN (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] ÓRGANO (2 veces)
- [ ] LUGAR
- [ ] Nº DE ARTÍCULO
- [ ] PROVINCIA
- [ ] TÉRMINOS DEL SORTEO
- [ ] ÓRGANO O PERSONA

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

Modelo de acuerdo de una Junta General, extraordinaria convocada o universal, de socios de una Sociedad Limitada, mediante la cual se adopta una acuerdo de emisión de obligaciones, estableciendo en el mismo las condiciones necesarias para su cumplimiento.


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

[OPCIONAL — incluir si procede]

(Junta General Extraordinaria)

En [LOCALIDAD], siendo las [Nº] horas del día [FECHA], se reunió [ELEGIR: en primera convocatoria / en segunda convocatoria], en el domicilio social de ‘[DENOMINACIÓN SOCIAL], S.L.’ sito en [LOCALIDAD] de [PROVINCIA] la Junta General Extraordinaria de socios, previa convocatoria al efecto del [ELEGIR: administrador único / administrador solidario / administrador mancomunado / Consejo de Administración] de la citada mercantil realizada mediante

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Comunicación individual]

Que el texto íntegro de la convocatoria fue el siguiente:

CONVOCATORIA

D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

Estimado señor,

Por la presente, le comunicamos la próxima celebración de la junta general de la sociedad [DENOMINACIÓN SOCIAL] SL, de la que usted es socio, y le convocamos de acuerdo con lo previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales.

La junta general de socios se celebrará en la [DIRECCIÓN], de la localidad de [LOCALIDAD], y tendrá lugar, en primera convocatoria, el día [FECHA] a las [Nº] horas y, en segunda convocatoria, el día [FECHA] a las [Nº] horas.

La junta convocada tendrá el siguiente

Orden del día

1.- Emisión de obligaciones.

2.- Concesión de facultades para la ejecución y protocolización de acuerdos.

3.- Aprobación del acta de la reunión.

En su calidad de socio, y de conformidad con lo que dispone el artículo 196 del Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el texto refundido de la Ley de Sociedades de Capital, tiene derecho a solicitar por escrito, con anterioridad a la reunión de la junta general o verbalmente durante la misma, los informes o aclaraciones que estimen precisos acerca de los asuntos comprendidos en el orden del día.

Actúa como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario D./Dña. [NOMBRE Y APELLIDOS], designados ambos por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las participaciones que poseen y/o representan cada uno de ellos:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios presentes:

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios representados:

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], mayor de edad y con D.N.I. asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] participaciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [Nº] participaciones, que representan el % del capital social.

No existen en la sociedad titulares de derechos especiales distintos de las participaciones sociales.

Todo el capital social de la compañía tiene derecho a voto.

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Junta.

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por [ELEGIR: unanimidad / mayoría] se adoptan los acuerdos cuyo contenido se transcribe a continuación

[OPCIONAL — incluir si procede]

(Junta universal)

En [LOCALIDAD], [DIRECCIÓN] a [FECHA], siendo las [Nº] horas, se hallan reunidos en el domicilio social de ‘[DENOMINACIÓN SOCIAL], S.L.’ la totalidad de sus socios, como consta en la lista de asistentes, que representan la totalidad del capital social, y acuerdan por unanimidad constituirse en Junta General Extraordinaria de carácter Universal, al amparo de lo previsto en el art. 178 de la vigente Ley de Sociedades de Capital y en el art. de los Estatutos Sociales para tratar y deliberar sobre el siguiente ORDEN DEL DÍA, que es unánimemente aceptado:

ORDEN DEL DÍA

1.- Emisión de obligaciones.

2.- Concesión de facultades para la ejecución y protocolización de acuerdos.

3.- Aprobación del acta de la reunión.

De conformidad con lo establecido en el art.97.1.4ª del Reglamento del Registro Mercantil, y en prueba de aceptación de todos los asistentes El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las participaciones que poseen y/o representan cada uno de ellos:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios presentes:

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios representados:

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], mayor de edad y con D./Dña. [NOMBRE Y APELLIDOS] asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] participaciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

No existen en la sociedad titulares de derechos especiales distintos de las participaciones sociales.

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [Nº] acciones, que representan el % del capital social.

Todo el capital social de la compañía tiene derecho a voto.

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Junta.

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por [ELEGIR: unanimidad / mayoría] se adoptan los acuerdos cuyo contenido se transcribe a continuación

ACUERDOS

Primero.- Emisión

Emitir un préstamo [IMPORTE] euros de conformidad con los informes emitidos por el Órgano de Administración y los Auditores de Cuentas y conforme a las siguientes condiciones:

Representación: El préstamo estará representado por [ÓRGANO O PERSONA] obligaciones nominativas, de [IMPORTE] euros de valor nominal cada una, de serie única y numeradas correlativamente del [Nº] al [Nº], ambos inclusive.

Emisión: La emisión se realiza a la par y libre de gastos para el suscriptor.

Suscripción: La suscripción se hará en [DIRECCIÓN] en el periodo comprendido desde [FECHA] a .siempre que la escritura de emisión haya sido inscrita en los Registros correspondientes; en otro caso, el Consejo de Administración podrá retrasar los períodos de suscripción para comenzar después de que la inscripción se haya producido.

Intereses: El interés de dichas obligaciones será el [PORCENTAJE] bruto, y [PORCENTAJE] neto.

Amortización: La amortización del préstamo se hará mediante sorteos, en los términos siguientes [TÉRMINOS DEL SORTEO] haciéndose el pago de los intereses y las amortizaciones en [DIRECCIÓN].

Garantía: La emisión quedará garantizada con el activo de la sociedad emisora.

Segundo.- Sindicato de obligacionistas

Constituir el Sindicato de obligacionistas, con domicilio en [LOCALIDAD], el cual se regirá, en sus relaciones jurídicas con la sociedad emisora, por el Reglamento que se reproduce a continuación, a reserva de su ratificación y aprobación por la Asamblea General de obligacionistas

"Reglas de funcionamiento del Sindicato".

Asimismo, se nombra como primer Comisario del mismo a D./Dña. [NOMBRE Y APELLIDOS].

Tercero.- Elevación a público

Facultar a todos y cada uno de los administradores y consejeros para que comparezcan ante el Notario de su elección y eleven a público los anteriores acuerdos, con cumplimiento de todas las formalidades legales, y realicen cuantos actos sean precisos, hasta su inscripción en el Registro Mercantil, con expresas facultades de rectificación y subsanación, para el caso de calificaciones verbales o escritas sobre los citados acuerdos por el Sr. Registrador Mercantil competente.

No habiendo más asuntos que tratar, se da lectura íntegra del acta de la reunión, que previa su aprobación por todos los socios asistentes, que la encuentran conforme a la realidad de lo acordado, y que, como queda dicho, representan la totalidad del capital social, es firmada por todos ellos, así como por el Presidente y el Secretario de la reunión.

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

Firmado: D./Dña. [NOMBRE Y APELLIDOS]

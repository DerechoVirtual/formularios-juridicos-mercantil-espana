---
name: acta-junta-sl-sobre-dividendos-cuenta-reposicion-mer-0019
description: "Acta de junta de SL sobre dividendos a cuenta, reposición de pérdidas y reparto de reservas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de junta de SL sobre dividendos a cuenta, reposición de pérdidas y reparto de reservas

> Formulario **MER-0019** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de junta de SL sobre dividendos a cuenta, reposición de pérdidas y reparto de reservas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de junta de SL sobre dividendos a cuenta, reposición de pérdidas y reparto de reservas” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-junta-sl-sobre-dividendos-cuenta-reposicion-mer-0019`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (20 veces)
- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] FECHA (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] DIRECCIÓN WEB (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] CALLE (4 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] DIRECCIÓN (3 veces)
- [ ] MAYORÍA (3 veces)
- [ ] PLATAFORMA (3 veces)
- [ ] NOMBRE DE LA APLICACIÓN (2 veces)
- [ ] NOMBRE DE LA PLATAFORMA (2 veces)
- [ ] ÓRGANO (2 veces)
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE ARTÍCULO

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

Acta de Junta General Extraordinaria Convocada o Universal, presencial o telemática (en remoto) por la que se acuerda la distribución de dividendos a cuenta, reposición de pérdidas y distribución de reservas de libre disposición

[OPCIONAL — incluir si procede]

(Junta General Extraordinaria)

En [LOCALIDAD], siendo las [Nº] horas del día [FECHA], se reunió [ELEGIR: en primera convocatoria / en segunda convocatoria], de forma telemática en el domicilio social de ‘[DENOMINACIÓN SOCIAL], S.L.’ sito en [LOCALIDAD] calle [CALLE] de [LOCALIDAD] la Junta General Extraordinaria de socios, previa convocatoria al efecto del [ELEGIR: administrador único / administrador solidario / administrador mancomunado / Consejo de Administración] de la citada mercantil realizada mediante

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Comunicación individual]

[OPCIONAL — incluir si procede]

(Junta telemática)

La videoconferencia se celebra utilizando la plataforma informática [PLATAFORMA] disponible en [DIRECCIÓN WEB], actuando la sociedad como organizadora y facilitando la asistencia telemática de todos los socios que lo deseen. Esta plataforma cumple con todos los requisitos legales exigibles de autenticidad y de conexión plurilateral en tiempo real con imagen y sonido.

Para participar en la junta todos los socios fueron informados de la necesidad de disponer de un [ELEGIR: ordenador / teléfono móvil] con cámara web y audio) y de la aplicación o programa [NOMBRE DE LA APLICACIÓN] para conectarse en la fecha y hora prevista a la videoconferencia

Para incorporarse a la videoconferencia se accede a la dirección de internet [DIRECCIÓN WEB] previa descarga en de la aplicación de dicha plataforma [NOMBRE DE LA PLATAFORMA] para invitados o clientes.

Todos los socios manifestaron al órgano de administración, con carácter previo a la convocatoria para la celebración de la junta, que disponen de los medios necesarios para poder conectarse, por el sistema de videoconferencia descrito y asistir a la celebración de la Junta.

Que el texto íntegro de la convocatoria fue el siguiente:

CONVOCATORIA

D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

Estimado señor,

Por la presente, le comunicamos la próxima celebración de la junta general de la sociedad [DENOMINACIÓN SOCIAL] SL, de la que usted es socio, y le convocamos de acuerdo con lo previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales.

La junta general de socios se celebrará de forma telemática en [DIRECCIÓN], de la localidad de [LOCALIDAD], y tendrá lugar, en primera convocatoria, el día [FECHA] a las [Nº] horas y, en segunda convocatoria, el día [FECHA] a las [Nº] horas.

[OPCIONAL — incluir si procede]

(Telemática)

La videoconferencia se celebrará utilizando la plataforma informática [PLATAFORMA] disponible en [DIRECCIÓN WEB], actuando la sociedad como organizadora y facilitando la asistencia telemática de todos los socios que lo deseen. Esta plataforma cumple con todos los requisitos legales exigibles de autenticidad y de conexión plurilateral en tiempo real con imagen y sonido.

Para participar en la junta es necesario disponer de [ELEGIR: ordenador / teléfono móvil] con cámara web y audio y de la aplicación o programa que tienen que tener instalado en su dispositivo para conectarse en la fecha y hora prevista a la videoconferencia que es

Para incorporarse a la videoconferencia deberán acceder a la dirección de internet [DIRECCIÓN WEB] previa descarga en su dispositivo informático de la aplicación de dicha plataforma para invitados o clientes.

La junta convocada tendrá el siguiente

ORDEN DEL DÍA

[OPCIONAL — incluir si procede]

(Distribución de dividendos a cuenta)

1. Aprobación de lal información contable formulada por el órgano de administración social.

2. Aprobación de la distribución de dividendo a cuenta de los resultados del ejercicio en curso.

3. Lectura y, en su caso, aprobación del acta de la Junta.

[OPCIONAL — incluir si procede]

(Reposición de Pérdidas)

1. Reposición de pérdidas.

2. Lectura y, en su caso, aprobación del acta de la Junta.

[OPCIONAL — incluir si procede]

(Distribución de Reservas de libre disposición)

1. Aprobación del estado contable formulado por el órgano de administración social.

2. Aprobación del reparto de reservas de libre disposición.

3. Lectura y, en su caso, aprobación del acta de la Junta.

Actúa como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario D./Dña. [NOMBRE Y APELLIDOS], designados ambos por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las participaciones que poseen y/o representan cada uno de ellos:

Socios presentes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Socios representados:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], calle [CALLE], mayor de edad y con D.N.I. asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] participaciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [Nº] participaciones, que representan el % del capital social.

Todo el capital social de la compañía tiene derecho a voto.

[OPCIONAL — incluir si procede]

(Telemática)

El Secretario manifiesta que el sistema de videoconferencia con imagen y sonido en directo utilizado, le ha permitido la debida identificación física de todos los asistentes al consejo.

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Junta.

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición se adoptan por

unanimidad

mayoría de [MAYORÍA] los acuerdos cuyo contenido se transcribe a continuación se adoptan los acuerdos cuyo contenido se transcribe a continuación

[OPCIONAL — incluir si procede]

(Voto por correo)

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo. Los socios emitieron su voto mediante escrito firmado dejando constancia del mismo para cada uno de los puntos del orden del día, que remitieron desde su dirección de correo electrónico a la dirección de la sociedad [DENOMINACIÓN SOCIAL] en formato PDF y cifrados digitalmente con [Nº] horas de antelación a la celebración de la Junta. Tras el recuento de los mismos se adoptan por

unanimidad

mayoría de los acuerdos cuyo contenido se transcribe a continuación

[OPCIONAL — incluir si procede]

(Junta universal)

En [LOCALIDAD], calle [CALLE] a [FECHA], siendo las [Nº] horas, [ELEGIR: se hallan reunidos en el domicilio social / se hallan conectados por videoconferencia] la totalidad de sus socios, como consta en la lista de asistentes, que representan la totalidad del capital social, y acuerdan por unanimidad constituirse en Junta General Extraordinaria de carácter Universal, al amparo de lo previsto en el art. 178 de la vigente Ley de Sociedades de Capital y en el art. de los Estatutos Sociales para tratar y deliberar sobre el siguiente ORDEN DEL DÍA, que es unánimemente aceptado:

[OPCIONAL — incluir si procede]

(Junta telemática)

La videoconferencia se celebra utilizando la plataforma informática [PLATAFORMA] disponible en [DIRECCIÓN WEB], actuando la sociedad como organizadora y facilitando la asistencia telemática de todos los socios que lo deseen. Esta plataforma cumple con todos los requisitos legales exigibles de autenticidad y de conexión plurilateral en tiempo real con imagen y sonido.

Para participar en la junta todos los socios fueron informados de la necesidad de disponer de un [ELEGIR: ordenador / teléfono móvil] con cámara web y audio) y de la aplicación o programa [NOMBRE DE LA APLICACIÓN] para conectarse en la fecha y hora prevista a la videoconferencia

Para incorporarse a la videoconferencia se accede a la dirección de internet [DIRECCIÓN WEB] previa descarga en de la aplicación de dicha plataforma [NOMBRE DE LA PLATAFORMA] para invitados o clientes.

[OPCIONAL — incluir si procede]

(Distribución de dividendos a cuenta)

1. Aprobación del estado contable formulado por el órgano de administración social.

2. Aprobación de la distribución de dividendo a cuenta de los resultados del ejercicio en curso.

3. Lectura y, en su caso, aprobación del acta de la Junta.

[OPCIONAL — incluir si procede]

(Reposición de Pérdidas)

1. Reposición de pérdidas.

2. Lectura y, en su caso, aprobación del acta de la Junta.

[OPCIONAL — incluir si procede]

(Distribución de Reservas de libre disposición)

1. Aprobación del estado contable formulado por el órgano de administración social.

2. Aprobación del reparto de reservas de libre disposición.

3. Lectura y, en su caso, aprobación del acta de la Junta.

El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las participaciones que poseen y/o representan cada uno de ellos:

Socios presentes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Socios representados:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], calle [CALLE], mayor de edad y con D./Dña. [NOMBRE Y APELLIDOS] asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] participaciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

En consecuencia, asisten, entre presentes y representados la totalidad de socios, titulares del 100% del capital social.

Todo el capital social de la compañía tiene derecho a voto.

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Junta.

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, se adoptan por

unanimidad

mayoría de [MAYORÍA] los acuerdos cuyo contenido se transcribe a continuación

[OPCIONAL — incluir si procede]

(Voto por correo)

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo. Los socios emitieron su voto mediante escrito firmado dejando constancia del mismo para cada uno de los puntos del orden del día, que remitieron desde su dirección de correo electrónico a la dirección de la sociedad [DENOMINACIÓN SOCIAL] en formato PDF y cifrados digitalmente con [Nº] horas de antelación a la celebración de la Junta. Tras el recuento de los mismos se adoptan por

unanimidad

mayoría de [MAYORÍA] los acuerdos cuyo contenido se transcribe a continuación

ACUERDOS

[OPCIONAL — incluir si procede]

(Distribución de dividendos a cuenta)

Primero.- Aprobación de la información contable

Con la finalidad de acordar una distribución de dividendos a cuenta de los resultados del ejercicio en curso, los asistentes convienen tomar como base de dicha distribución la información contable aportada por el órgano de administración el [FECHA], que es aprobado por la unanimidad de los asistentes en este mismo acto. El estado contable aprobado se adjunta a la presente como anexo 1

Segundo.- Aprobación de la distribución de dividendo a cuenta de los resultados del ejercicio en curso

Se aprueba por unanimidad de los asistentes la distribución de un dividendo a cuenta de los resultados del ejercicio social en curso, en los siguientes términos:

– Dividendo bruto: [IMPORTE] euros por participación social.
– Retención fiscal: tipo aplicable%.
– Dividendo líquido: [IMPORTE] euros por participación social.
– El pago se llevará a efecto en [DIRECCIÓN] a partir del día [FECHA]

[OPCIONAL — incluir si procede]

(Reposición de Pérdidas)

Primero Aprobación de la información contable

La información contable aportada por el órgano de administración es aprobada por la unanimidad de los asistentes en este mismo acto. El estado contable aprobado se adjunta a la presente como anexo 1

Segundo.- Reintegro

Reintegrar el patrimonio de la compañía con el propósito de reponer las pérdidas sociales, mediante la incorporación al activo de la sociedad de un total de [IMPORTE] euros, que en estel mismo acto es aportada por los señores socios mediante su ingreso en la caja social, en proporción a su participación en el capital social.

[OPCIONAL — incluir si procede]

(Distribución de Reservas de libre disposición)

Primero.- Aprobación de la información contable

Con la finalidad de acordar el reparto de reservas de libre disposición los asistentes convienen tomar como base de dicho reparto la información contable aportada por el órgano de administración el de [DÍA] de [MES], que es aprobado por la unanimidad de los asistentes en este mismo acto. El estado contable aprobado se adjunta a la presente como anexo 1

Segundo.- Aprobación de la distribución de reservas voluntarias

Se aprueba por unanimidad de los asistentes la distribución de las reservas voluntarias de la sociedad, en los siguientes términos:

– Importe bruto: [IMPORTE] euros por participación.
– Retención fiscal: "tipo aplicable"%.
– Importe líquido: [IMPORTE] euros por acción.
– El pago se efectuará en [DIRECCIÓN] a partir del día [FECHA].

No habiendo más asuntos que tratar, ni más proposiciones, ruegos o preguntas, se redacta la presente acta por el Secretario que, previa su lectura, es aprobada por la propia Junta, por unanimidad de los asistentes, firmándola a continuación el Secretario con el Visto Bueno del Presidente, así como, en prueba de conformidad, los asistentes.

Tras lo cual, se levanta la sesión.

VB Presidente

Secretario

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

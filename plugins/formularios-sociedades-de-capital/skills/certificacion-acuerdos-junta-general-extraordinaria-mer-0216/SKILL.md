---
name: certificacion-acuerdos-junta-general-extraordinaria-mer-0216
description: "Certificación de los acuerdos de la junta general extraordinaria de una sociedad anónima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación de los acuerdos de la junta general extraordinaria de una sociedad anónima

> Formulario **MER-0216** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de certificación expedida por el Secretario del Consejo de Administración de una Sociedad Anónima sobre los acuerdos llevados a cabo en la Junta General Extraordinaria, así como una lista de asistentes a la misma.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación de los acuerdos de la junta general extraordinaria de una sociedad anónima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación de los acuerdos de la junta general extraordinaria de una sociedad anónima” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdos-junta-general-extraordinaria-mer-0216`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (16 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] ASUNTO DEL ORDEN DEL DÍA
- [ ] CALLE
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] IMPORTE
- [ ] LUGAR
- [ ] Nº DE DOCUMENTO
- [ ] OTROS DATOS
- [ ] PORCENTAJE
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

Modelo de certificación expedida por el Secretario del Consejo de Administración de una Sociedad Anónima sobre los acuerdos llevados a cabo en la Junta General Extraordinaria, así como una lista de asistentes a la misma.


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

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de [ELEGIR: Administrador único / Administrador solidario / Administradores mancomunados / Secretario del Consejo de Administración] de ‘[DENOMINACIÓN SOCIAL], S.A.’ [DENOMINACIÓN SOCIAL], con domicilio social en [LOCALIDAD], [DOMICILIO] y N.I.F.

CERTIFICA

Primero.- Que la reunión de la Junta General Extraordinaria de la citada Sociedad celebrada el pasado día [FECHA] en el domicilio social de la misma, fue convocada:

:

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Por comunicación individual]

Con el siguiente contenido: y Orden del Día:

1º.- [ASUNTO DEL ORDEN DEL DÍA]
2º.- Ruegos y preguntas.
3º.- Lectura y, en su caso, aprobación del Acta de la reunión.

Segundo.- Que con posterioridad se procedió a elaborar la siguiente lista de asistentes:

LISTA DE ASISTENTES A LA JUNTA GENERAL EXTRAORDINARIA DE ACCIONISTAS DE ‘[DENOMINACIÓN SOCIAL], S.A.’

En [LOCALIDAD], a [FECHA], a las [Nº] horas, comienza la reunión de la Junta General Extraordinaria de ‘ [DENOMINACIÓN SOCIAL],S.A.’, en [ELEGIR: primera / segunda] convocatoria.

Contando la sociedad con un Capital Social de [IMPORTE] euros, dividido en [Nº] acciones de las cuales [Nº] de ellas tienen derecho a voto, se hallan presentes y representados los accionistas que a continuación se describen, con las acciones y número de votos que se señalan para cada uno de ellos:

Accionistas presentes

Firmado: Nº [Nº] de acciones Acciones Nº [NÚMERO] Nº votos

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE] % del total del capital social con derecho a voto.

Accionistas representados

Firmado: Nº [Nº] de acciones Acciones Nº [NÚMERO] Nº votos [Nº]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], calle [CALLE], mayor de edad y con D.N.I [DNI/NIE] asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Firmas

CON DERECHO A VOTO	SIN DERECHO A VOTO
ACCIONISTAS PRESENTES: %	%	%
ACCTAS. REPRESENTADOS:%	%	%
ACCIONISTAS ASISTENTES:%	%	%
CAPITAL PRESENTE:%	%	%
CAPITAL REPRESENTADO:%	%	%
CAPITAL ASISTENTE:%	%	%

Tercero.- Que de dicha lista de asistentes, que se unió al Acta de la Junta como [Nº DE DOCUMENTO] se desprendía la concurrencia de [Nº] socios con derecho de voto, que suponen un % del capital social, de los cuales [Nº] accionistas concurren personalmente, sumando el % del capital social, y [Nº] accionistas lo hacen debidamente representados, sumando a su vez un % del capital, por lo que se procedió a la declaración por el Presidente de la válida constitución de la Junta en [ELEGIR: primera / segunda] convocatoria, seguido lo cual el Secretario dio paso a la lectura del Orden del Día fijado en la convocatoria.

Cuarto.- Que a continuación se procedió al debate de los asuntos contenidos en el Orden del Día, se aludieron los siguientes aspectos y se produjeron las siguientes intervenciones [OTROS DATOS] (Resumen de los asuntos debatidos y de las intervenciones de las que se haya solicitado constancia)

Y que no solicitándose por ninguno de los accionistas la palabra y no habiendo más asuntos que tratar, el Presidente dio por concluido el debate y suspendió momentáneamente la sesión para la redacción por el Secretario de la correspondiente Acta, en la cual quedó reflejada la adopción de los siguientes acuerdos:

‘I.-

II.-

III.-

.-

Quinto.- Que dichos acuerdos fueron aprobados con el voto favorable del % del capital concurrente con derecho a voto.

Sexto.- Que actuaron como Presidente y Secretario de la Junta quienes ocupan dichos cargos en el Consejo de Administración, cargos que declararon vigentes e inscritos en el Registro Mercantil de

Una vez redactada el Acta, esta fue leída íntegramente por el Secretario, se sometió a la aprobación de los asistentes, que la aprobaron por unanimidad, por encontrarla conforme a lo debatido y acordado, seguido lo cual se levantó la sesión, siendo las [Nº] horas del día señalado y se procedió a la firma de la misma por el Secretario, con el Visto Bueno del Presidente.

Así se certifica, para que conste, en cumplimiento de lo previsto en la Ley de Sociedades de Capital y en el Reglamento del Registro Mercantil, con el Vº.Bº del Presidente

En [LUGAR], a [FECHA].

Administrador único
Administrador solidario
Administradores mancomunados
Secretario del Consejo de Administración

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

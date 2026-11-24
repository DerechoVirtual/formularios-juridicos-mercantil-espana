---
name: certificacion-acuerdos-junta-general-ordinaria-mer-0285
description: "Certificación de los acuerdos de la junta general ordinaria, universal o no, de una sociedad anónima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación de los acuerdos de la junta general ordinaria, universal o no, de una sociedad anónima

> Formulario **MER-0285** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de certificación expedida por el Secretario del Consejo de Administración de una Sociedad Anónima sobre los acuerdos presenciales, o telemáticos (en remoto) llevados a cabo en la Junta General Ordinaria universal o no universal, así como una lista de asistentes a la misma.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación de los acuerdos de la junta general ordinaria, universal o no, de una sociedad anónima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación de los acuerdos de la junta general ordinaria, universal o no, de una sociedad anónima” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdos-junta-general-ordinaria-mer-0285`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (27 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] DIRECCIÓN WEB (4 veces)
- [ ] EJERCICIO (4 veces)
- [ ] Nº DE ACCIONES (4 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE VOTOS (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] AÑO DEL EJERCICIO (2 veces)
- [ ] CALLE (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DE LA PLATAFORMA (2 veces)
- [ ] PLATAFORMA (2 veces)
- [ ] PUNTO DEL ORDEN DEL DÍA (2 veces)
- [ ] ÓRGANO (2 veces)
- [ ] DESTINO DE LOS RESULTADOS
- [ ] LUGAR
- [ ] Nº DE DOCUMENTO

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

Modelo de certificación expedida por el Secretario del Consejo de Administración de una Sociedad Anónima sobre los acuerdos presenciales, o telemáticos (en remoto) llevados a cabo en la Junta General Ordinaria universal o no universal, así como una lista de asistentes a la misma.


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

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de [ELEGIR: Administrador único / Administrador solidario / Administradores mancomunados / Secretario del Consejo de Administración] de ‘[DENOMINACIÓN SOCIAL], S.A.’ con domicilio social en [LOCALIDAD], y N.I.F

CERTIFICA

[OPCIONAL — incluir si procede]

(Junta Ordinaria no universal)

Primero.- Que la reunión de la Junta General Ordinaria de la citada Sociedad celebrada el pasado día [ELEGIR: en el domicilio social de la misma / por videoconferencia], fue convocada:

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Por comunicación individual]

Con el siguiente contenido y Orden del día:

1º.- Examen y, en su caso, aprobación de las Cuentas Anuales y del Informe de gestión correspondientes al ejercicio económico [EJERCICIO], así como de la aplicación de los resultados de dicho ejercicio.
2º.- Censura y, en su caso, aprobación de la gestión realizada por el Consejo de Administración durante el ejercicio social [AÑO DEL EJERCICIO]
3º.- Facultar al Consejo de Administración para que, a través de su Presidente, proceda al depósito de las Cuentas Anuales y del Informe de gestión en el Registro Mercantil de [LOCALIDAD], y a certificar sobre la aprobación de las citadas Cuentas Anuales, Informe de gestión y aplicación de resultados del citado ejercicio.
4º.- [PUNTO DEL ORDEN DEL DÍA]
5º.- Ruegos y preguntas.
6º.- Lectura y, en su caso, aprobación del Acta de la reunión.

[OPCIONAL — incluir si procede]

(Junta telemática)

Que la videoconferencia se celebró utilizando la plataforma informática [PLATAFORMA] disponible en [DIRECCIÓN WEB], actuando la sociedad como organizadora y facilitando la asistencia telemática de todos los socios que lo deseen. Esta plataforma cumple con todos los requisitos legales exigibles de autenticidad y de conexión plurilateral en tiempo real con imagen y sonido.

Que para participar en la junta se debía disponer de [ELEGIR: ordenador / teléfono móvil] con cámara web y audio y de la aplicación o programa para conectarse en la fecha y hora prevista a la videoconferencia

Que para incorporarse a la videoconferencia se debía acceder a la dirección de internet [DIRECCIÓN WEB] previa descarga en su dispositivo informático de la aplicación de dicha plataforma [NOMBRE DE LA PLATAFORMA] para invitados o clientes.

Que todos los socios manifestaron al órgano de administración, con carácter previo a la convocatoria para la celebración de la junta, que disponen de los medios necesarios para poder conectarse, por el sistema de videoconferencia descrito y asistir a la celebración de la Junta.

[OPCIONAL — incluir si procede]

(Junta Ordinaria universal)

Primero.- Que en la reunión de la Junta General Ordinaria Universal de la citada Sociedad celebrada el pasado día [ELEGIR: en el domicilio social de la misma / por videoconferencia] y con la asistencia de todo el capital social, y por lo tanto de todos los accionistas con derecho a voto, se aprobó por unanimidad de dichos asistentes el siguiente Orden del Día:

1º.- Examen y, en su caso, aprobación de las Cuentas Anuales y del Informe de gestión correspondientes al ejercicio económico [EJERCICIO], así como de la aplicación de los resultados de dicho ejercicio.
2º.- Censura y, en su caso, aprobación de la gestión realizada por el Consejo de Administración durante el ejercicio social [AÑO DEL EJERCICIO]
3º.- Facultar al Consejo de Administración para que, a través de su Presidente, proceda al depósito de las Cuentas Anuales y del Informe de gestión en el Registro Mercantil de [LOCALIDAD], y a certificar sobre la aprobación de las citadas Cuentas Anuales, Informe de gestión y aplicación de resultados del citado ejercicio.
4º.- [PUNTO DEL ORDEN DEL DÍA]
5º.- Ruegos y preguntas.
6º.- Lectura y, en su caso, aprobación del Acta de la reunión.

[OPCIONAL — incluir si procede]

(Junta telemática)

Que la videoconferencia se celebró utilizando la plataforma informática [PLATAFORMA] disponible en [DIRECCIÓN WEB], actuando la sociedad como organizadora y facilitando la asistencia telemática de todos los socios que lo deseen. Esta plataforma cumple con todos los requisitos legales exigibles de autenticidad y de conexión plurilateral en tiempo real con imagen y sonido.

Que para participar en la junta se debía disponer de [ELEGIR: ordenador / teléfono móvil] con cámara web y audio y de la aplicación o programa para conectarse en la fecha y hora prevista a la videoconferencia

Que para incorporarse a la videoconferencia se debía acceder a la dirección de internet [DIRECCIÓN WEB] previa descarga en su dispositivo informático de la aplicación de dicha plataforma [NOMBRE DE LA PLATAFORMA] para invitados o clientes.

Que todos los socios manifestaron al órgano de administración, con carácter previo a la convocatoria para la celebración de la junta, que disponen de los medios necesarios para poder conectarse, por el sistema de videoconferencia descrito y asistir a la celebración de la Junta.

[OPCIONAL — incluir si procede]

(Junta ordinaria no universal)

Segundo.- Que con posterioridad se procedió a elaborar la siguiente lista de asistentes:

LISTA DE ASISTENTES A LA JUNTA GENERAL DE ACCIONISTAS DE ‘[DENOMINACIÓN SOCIAL], S.A.’

En [LOCALIDAD], a [FECHA], a las [Nº] horas, comienza la reunión de la Junta General de ‘ [DENOMINACIÓN SOCIAL],S.A.’, en [ELEGIR: primera / segunda] convocatoria.

Contando la sociedad con un Capital Social de [IMPORTE] euros, dividido en [Nº] acciones de las cuales [Nº] de ellas tienen derecho a voto, se hallan presentes y representados los accionistas que a continuación se describen, con las acciones y número de votos que se señalan para cada uno de ellos:

Accionistas presentes

Firmado: Nº [Nº] de acciones [Nº DE ACCIONES] Acciones Nº [NÚMERO] Nº votos [Nº DE VOTOS]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Accionistas representados

Firmado: Nº [Nº] de acciones [Nº DE ACCIONES] Acciones Nº [NÚMERO] Nº votos [Nº DE VOTOS]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], calle [CALLE], mayor de edad y con D.N.I [DNI/NIE] asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

CON DERECHO A VOTO	SIN DERECHO A VOTO
ACCIONISTAS PRESENTES: %	%	%
ACCTAS. REPRESENTADOS:%	%	%
ACCIONISTAS ASISTENTES:%	%	%
CAPITAL PRESENTE:%	%	%
CAPITAL REPRESENTADO:%	%	%
CAPITAL ASISTENTE:%	%	%

Tercero.- Que de dicha lista de asistentes, que se unió al Acta de la Junta como [Nº DE DOCUMENTO] (Anexo [Nº]) se desprendía la concurrencia de [Nº] socios con derecho de voto, que representan un % del capital social, de los cuales [Nº] accionistas concurren personalmente, representando el % del capital social, y [Nº] accionistas lo hacen debidamente representados, representando a su vez un % del capital, por lo que se procedió a la declaración por el Presidente de la válida constitución de la Junta en [ELEGIR: primera / segunda] convocatoria, seguido lo cual el Secretario dio paso a la lectura del Orden del Día fijado en la convocatoria.

[OPCIONAL — incluir si procede]

(Junta ordinaria universal)

Segundo.- Que la totalidad de los accionistas se corresponden con los que constan en la siguiente lista de asistentes:

LISTA DE ASISTENTES A LA JUNTA GENERAL ORDINARIA DE ACCIONISTAS DE ‘[DENOMINACIÓN SOCIAL], S.A.’

En [LOCALIDAD], a [FECHA], a las [Nº] horas, comienza la reunión de la Junta General de ‘ [DENOMINACIÓN SOCIAL],S.A.’.

Contando la sociedad con un Capital Social de [IMPORTE] euros, dividido en [Nº] acciones de las cuales [Nº] de ellas tienen derecho a voto, se hallan presentes y representados los accionistas que a continuación se describen, con las acciones y número de votos que se señalan para cada uno de ellos:

Accionistas presentes

Firmado: Nº [Nº] de acciones [Nº DE ACCIONES] Acciones Nº Nº votos [Nº DE VOTOS]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Accionistas representados

Firmas Firmado: Nº [Nº] de acciones [Nº DE ACCIONES] Acciones Nº [NÚMERO] Nº votos

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

.- Que a continuación se procedió al debate de los asuntos contenidos en el Orden del Día, se aludieron los siguientes aspectos y se produjeron las siguientes intervenciones

[OPCIONAL — incluir si procede]

(Junta ordinaria universal)

Que los citados accionistas procedieron con el carácter de Junta General Ordinaria y Universal a la adopción de los siguientes acuerdos, que fueron adoptados por unanimidad:

Y que no solicitándose por ninguno de los accionistas la palabra y no habiendo más asuntos que tratar, el Presidente dio por concluido el debate y suspendió momentáneamente la sesión para la redacción por el Secretario de la correspondiente Acta, en la cual quedó reflejada la adopción de los siguientes acuerdos:

I.-Aprobar las Cuentas Anuales correspondientes al ejercicio [EJERCICIO]

II.-Aprobar la gestión realizada por el Consejo de Administración durante el ejercicio [EJERCICIO]

III.-Aprobar la aplicación de los resultados obtenidos durante dicho ejercicio, destinando [DESTINO DE LOS RESULTADOS]

IV.-Facultar al Consejo de Administración para que, a través de su Presidente, proceda al depósito de las Cuentas Anuales y del Informe de gestión en el Registro Mercantil de [LOCALIDAD], y a certificar sobre la aprobación de las citadas Cuentas Anuales, Informe de gestión y aplicación de resultados del citado ejercicio.

V.-

[OPCIONAL — incluir si procede]

(Junta ordinaria no universal)

.- Que dichos acuerdos fueron aprobados con el voto favorable del % del capital concurrente con derecho a voto.

.- Que actuaron como Presidente y Secretario de la Junta quienes ocupan dichos cargos en el Consejo de Administración, cargos que declararon vigentes e inscritos en el Registro Mercantil de

Una vez redactada el Acta, esta fue leída íntegramente por el Secretario, se sometió a la aprobación de los asistentes, que lo hicieron por unanimidad, por encontrarla conforme a lo debatido y acordado, seguido lo cual se levantó la sesión, siendo las [Nº] horas del día señalado y se procedió a la firma de la misma por el Secretario, con el Visto Bueno del Presidente.

Así se certifica, para que conste, en cumplimiento de lo previsto en la Ley de Sociedades de Capital y en el Reglamento del Registro Mercantil, con el Vº.Bº del Presidente

En [LUGAR], a [FECHA].

VºBº Presidente

Administrador único
Administrador solidario
Administradores mancomunados
Secretario del Consejo de Administración

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

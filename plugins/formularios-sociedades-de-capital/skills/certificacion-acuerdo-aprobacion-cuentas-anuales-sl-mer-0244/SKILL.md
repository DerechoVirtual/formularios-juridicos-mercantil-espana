---
name: certificacion-acuerdo-aprobacion-cuentas-anuales-sl-mer-0244
description: "Certificación del acuerdo de aprobación de las cuentas anuales de una SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación del acuerdo de aprobación de las cuentas anuales de una SL

> Formulario **MER-0244** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de certificado del acta de Junta General de Socios presencial o telemática (en remoto) de una Sociedad de Responsabilidad Limitada mediante el cual se certifica la aprobación de los puntos que se establecieron como orden del día: las cuentas anuales de la compañía, propuesta de aplicación de los resultados obtenidos y examen y aprobación, en su caso, de la gestión del Consejo de Administración.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación del acuerdo de aprobación de las cuentas anuales de una SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación del acuerdo de aprobación de las cuentas anuales de una SL” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdo-aprobacion-cuentas-anuales-sl-mer-0244`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (9 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] EJERCICIO (3 veces)
- [ ] FECHA (3 veces)
- [ ] LUGAR (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] ASUNTO DEL ORDEN DEL DÍA
- [ ] CALLE
- [ ] DESTINO
- [ ] DNI/NIE
- [ ] LOCALIDAD
- [ ] MAYORÍA
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

Modelo de certificado del acta de Junta General de Socios presencial o telemática (en remoto) de una Sociedad de Responsabilidad Limitada mediante el cual se certifica la aprobación de los puntos que se establecieron como orden del día: las cuentas anuales de la compañía, propuesta de aplicación de los resultados obtenidos y examen y aprobación, en su caso, de la gestión del Consejo de Administración.


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

CERTIFICADO DE ACTA DE JUNTA GENERAL DE ‘[DENOMINACIÓN SOCIAL], S.L.’

En [LUGAR], a [FECHA].

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de Secretario del Consejo de Administración de ‘ S.L.’ y de su Junta de socios reunida el pasado [FECHA]

CERTIFICO

[ELEGIR UNA OPCIÓN: Presencial / Telemática / — y además elegir: Con página web / Sin página web / Comunicación individual]

Que el texto íntegro de la convocatoria fue el siguiente:

CONVOCATORIA

Estimado señor,

Por la presente, le comunicamos la próxima celebración de la junta general de la sociedad SL, de la que usted es socio, y le convocamos de acuerdo con lo previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales

[ELEGIR UNA OPCIÓN: Presencial / Telemática]

La junta convocada tendrá el siguiente

ORDEN DEL DÍA

I.- Examen y aprobación de las cuentas anuales de [DENOMINACIÓN SOCIAL] SL, correspondientes al ejercicio [EJERCICIO].

.- Ruegos y preguntas

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

Que según lo previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales, actuó como Presidente de la junta quien lo es del Consejo de Administración, D./Dña. [NOMBRE Y APELLIDOS], y como Secretario yo, D./Dña.. [NOMBRE Y APELLIDOS]

Que asistieron igualmente los restantes miembros del Consejo de Administración.

Que el Presidente, asistido por mí, el Secretario, procedió a elaborar la lista de asistentes que a continuación se relata, con detalle de las participaciones que poseen y/o representan cada uno de ellos:

Socios presentes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones sociales numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Socios representados:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], calle [CALLE], mayor de edad y con D.N.I [DNI/NIE] asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] participaciones sociales numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Que, en consecuencia, asistieron, entre presentes y representados, un total de [Nº] socios, titulares de [Nº] participaciones sociales, que representaban el % del capital social con derecho a voto.

[OPCIONAL — incluir si procede]

Que el sistema de videoconferencia con imagen y sonido en directo utilizado, ha permitido a este secretario la debida identificación física de todos los asistentes.

Que por el Presidente se procedió a declarar válidamente constituida la Junta, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el ORDEN DEL DÍA de la convocatoria, tras lo cual se adoptaron los siguientes

ACUERDOS

Primero.- Examen y aprobación de las cuentas anuales e Informe de Gestión de ‘[DENOMINACIÓN SOCIAL], S.L.’ correspondiente al ejercicio [EJERCICIO]

El Presidente ordena dar lectura a las cuentas correspondientes a dicho ejercicio [EJERCICIO] tal y como han quedado redactadas. Finalizada su lectura, se informa a los reunidos de todos los pormenores planteados en torno a dichas cuentas manifestando, a los efectos de lo dispuesto en los arts. 257 de la Ley de Sociedades de Capital y 366-2º del Reglamento del Registro Mercantil, que las cuentas se han formulado de acuerdo con [ELEGIR: PGC / PGC PYMES / PGC PYMES con criterios Microempresa] por cumplir la sociedad los requisitos para ello.

[OPCIONAL — incluir si procede]

(Voto por correo)

Los socios emitieron su voto mediante escrito firmado dejando constancia del mismo para cada uno de los puntos del orden del día, y lo remitieron desde su dirección de correo electrónico a la dirección de la sociedad [DENOMINACIÓN SOCIAL] en formato PDF y cifrados digitalmente con al menos [Nº] horas de antelación a la celebración de la Junta.

Una vez finalizada la deliberación y sometida a votación la aprobación de las cuentas presentadas, se acuerda por [ELEGIR: unanimidad / mayoría]

unanimidad

mayoría de [MAYORÍA] la aprobación de las mismas en los términos en que han sido redactadas por el Consejo de Administración.

Se hace constar que la sociedad puede formular balance abreviado y no está obligada a someter las cuentas a verificación de auditor.

Las cuentas anuales y el informe de gestión, firmados ambos por la totalidad de los miembros del Consejo de Administración, quedan unidas al Acta de la Junta como Anexo.

Segundo.- Propuesta de aplicación de los resultados obtenidos.

Por el Presidente se abre este punto informando a los reunidos de la necesidad legal de que la Junta se pronuncie en torno a la aplicación del saldo positivo/negativo obtenido en el ejercicio precedente, comunicando la propuesta que se realiza por el Consejo de Administración al respecto.

Previa su deliberación, se acuerda por [ELEGIR: unanimidad / mayoría]

unanimidad

mayoría [PORCENTAJE] destinar dicho saldo a [DESTINO].

Tercero.- Examen y aprobación, en su caso, de la gestión realizada por el Consejo de Administración.

Por el Presidente se informa a los reunidos sobre el desarrollo de los negocios sociales llevados a cabo a lo largo del ejercicio que se cierra, cuyas cuentas han sido aprobadas.

Previas las oportunas deliberaciones en las que intervienen [NOMBRE Y APELLIDOS], se acuerda por [ELEGIR: unanimidad / mayoría de] hacer constar la plena satisfacción de todos los reunidos por la marcha de los negocios sociales y la forma en que los mismos se han llevado a cabo.

Cuarto.- [ASUNTO DEL ORDEN DEL DÍA]

Quinto.- Ruegos y preguntas.

‘

Doy fe de que las cuentas anuales y el informe de gestión aportado a la Junta por el Consejo de Administración del que soy secretario se encontraban firmados por todos los miembros del dicho Consejo.

Que el acta fue aprobada por la propia Junta, así como firmada por mí, el Secretario, con el Visto Bueno del Presidente, al término de dicha reunión.

Y para que conste y surta los efectos oportunos expido el presente certificado con el Visto Bueno del Presidente, al que se acompañan los Anexos citados en el Acta de la Junta, como Anexos I y II, en [LUGAR], a [FECHA].

D./Dña. [NOMBRE Y APELLIDOS]

Secretario del Consejo de Administración

ANEXO I: CUENTAS ANUALES

ANEXO II: INFORME DE GESTIÓN

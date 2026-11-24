---
name: acta-junta-general-universal-ordinaria-sociedad-anonima-mer-0284
description: "Acta de junta general universal ordinaria de una sociedad anónima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de junta general universal ordinaria de una sociedad anónima

> Formulario **MER-0284** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de acta de Junta General Universal Ordinaria, presencial o telemática (en remoto) de una Sociedad Anónima, con la asistencia de todos los accionistas con derecho de voto, en la que se concreta los puntos que se han tratado en la Junta, tales como examen y aprobación de las cuentas anuales, se censura o aprueba la gestión del Consejo de Administración, y se faculta a ésta para que proceda al depósito de las Cuentas Anuales y del Informe de Gestión en el Registro Mercantil.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de junta general universal ordinaria de una sociedad anónima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de junta general universal ordinaria de una sociedad anónima” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-junta-general-universal-ordinaria-sociedad-anonima-mer-0284`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] EJERCICIO (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DIRECCIÓN WEB (2 veces)
- [ ] AÑO DEL EJERCICIO
- [ ] CALLE
- [ ] DESTINO DE LOS RESULTADOS
- [ ] FECHA
- [ ] INTERVENCIONES DE LOS ASISTENTES
- [ ] Nº DE ARTÍCULO
- [ ] PISO
- [ ] PLATAFORMA
- [ ] PORCENTAJE
- [ ] PUNTO DEL ORDEN DEL DÍA

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

Modelo de acta de Junta General Universal Ordinaria, presencial o telemática (en remoto) de una Sociedad Anónima, con la asistencia de todos los accionistas con derecho de voto, en la que se concreta los puntos que se han tratado en la Junta, tales como examen y aprobación de las cuentas anuales, se censura o aprueba la gestión del Consejo de Administración, y se faculta a ésta para que proceda al depósito de las Cuentas Anuales y del Informe de Gestión en el Registro Mercantil.


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

Acta de la Junta General Ordinaria de accionistas de la Sociedad Anónima [DENOMINACIÓN SOCIAL]

En [LOCALIDAD], a [FECHA], siendo las [Nº] horas y en el domicilio social de la sociedad [DENOMINACIÓN SOCIAL] sito en la calle [CALLE], piso [PISO], municipio [LOCALIDAD]

Se celebra la presente Junta con la asistencia [ELEGIR: personal / telemática] de todos los accionistas con derecho a voto de la sociedad, que a su vez representan el total del capital suscrito y desembolsado y acuerdan por unanimidad constituirse en Junta General Ordinaria Universal de Accionistas, con la asistencia asimismo de la totalidad de los componentes del Consejo de Administración.

[OPCIONAL — incluir si procede]

(Telemática)

La videoconferencia se celebró utilizando la plataforma informática [PLATAFORMA] disponible en [DIRECCIÓN WEB], actuando la sociedad como organizadora y facilitando la asistencia telemática de todos los socios que lo deseen. Esta plataforma cumple con todos los requisitos legales exigibles de autenticidad y de conexión plurilateral en tiempo real con imagen y sonido.

Para participar en la junta era necesario disponer de [ELEGIR: ordenador / teléfono móvil] (con cámara web y audio) y de la aplicación o programa que debieron instalar en su dispositivo para conectarse en la fecha y hora prevista a la videoconferencia.

Para incorporarse a la videoconferencia se accedió a la dirección de internet [DIRECCIÓN WEB] previa descarga en su dispositivo informático de la aplicación de dicha plataforma para invitados o clientes.

Todos los socios han manifestaron al órgano de administración, con carácter previo a la celebración de la junta, que disponen de los medios necesarios para poder conectarse, por el sistema de videoconferencia descrito y asistir a la celebración de la Junta.

Se procede a elaborar la lista de asistentes

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE] % del total del capital social con derecho a voto.

Al hallarse presente el capital citado y aceptarse por unanimidad la celebración de la Junta con carácter de Universal, queda válidamente constituida.

Actúa como Presidente de la Junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario de la misma D./Dña. [NOMBRE Y APELLIDOS], en su calidad de Presidente y Secretario del Consejo de Administración respectivamente, y en ejercicio de las funciones que en tal sentido les atribuye el artículo [Nº DE ARTÍCULO] de los estatutos sociales.

Se procede a la declaración por el Presidente de la válida constitución de la Junta, seguido lo cual el Secretario da paso a la lectura del Orden del Día y que es aceptado por unanimidad por todos los asistentes, cuyo contenido es el siguiente:

1º.- Examen y, en su caso, aprobación de las Cuentas Anuales y del Informe de gestión correspondientes al ejercicio económico [EJERCICIO], así como de la aplicación de los resultados de dicho ejercicio.
2º.- Censura y, en su caso, aprobación de la gestión realizada por el Consejo de Administración durante el ejercicio social [AÑO DEL EJERCICIO]
3º.- Facultar al Consejo de Administración para que, a través de su Presidente, proceda al depósito de las Cuentas Anuales y del Informe de gestión en el Registro Mercantil de [LOCALIDAD], y a certificar sobre la aprobación de las citadas Cuentas Anuales, Informe de gestión y aplicación de resultados del citado ejercicio.
4º.- [PUNTO DEL ORDEN DEL DÍA]
5º.- Ruegos y preguntas.
6º.- Lectura y, en su caso, aprobación del Acta de la reunión.

[OPCIONAL — incluir si procede]

(Telematica)

El secretario y el presidente [ELEGIR: manifiesta / manifiestan] que el sistema de videoconferencia con imagen y sonido en directo utilizado, ha permitido la debida identificación física de todos los asistentes.

A continuación se procede al debate de los asuntos contenidos en el Orden del Día se aluden los siguientes aspectos y se producen las siguientes intervenciones [INTERVENCIONES DE LOS ASISTENTES]

No solicitándose por ninguno de los accionistas la palabra y no habiendo más asuntos que tratar, el Presidente da por concluido el debate y suspende momentáneamente la sesión para la redacción por el Secretario de la presente Acta, en la cual queda reflejada la adopción de los siguientes acuerdos:

Primero.-Aprobar las Cuentas Anuales, así como el Informe de gestión correspondientes al ejercicio [EJERCICIO]

Segundo.-Aprobar la gestión realizada por el Consejo de Administración durante el ejercicio [EJERCICIO]

Tercero.-Aprobar la aplicación de los resultados obtenidos durante dicho ejercicio, destinandos a [DESTINO DE LOS RESULTADOS]

Cuarto.-Facultar al Consejo de Administración para que, a través de su Presidente, proceda al depósito de las Cuentas Anuales y del Informe de gestión en el Registro Mercantil de [LOCALIDAD], y a certificar sobre la aprobación de las citadas Cuentas Anuales, Informe de gestión y aplicación de resultados del citado ejercicio.

Quinto.-

Una vez redactada el Acta y leída íntegramente por el Secretario, se somete a la votación de los asistentes, que la aprueban por unanimidad, por encontrarla conforme a lo debatido y acordado.

Acto seguido, se levanta la sesión, siendo las [Nº] horas del día señalado en el encabezamiento, procediéndose a la firma de la presente por mí, el Secretario, con el Visto Bueno del Presidente.

D./Dña. [NOMBRE Y APELLIDOS]

El Secretario

D./Dña. [NOMBRE Y APELLIDOS]

Vº.Bº, el Presidente

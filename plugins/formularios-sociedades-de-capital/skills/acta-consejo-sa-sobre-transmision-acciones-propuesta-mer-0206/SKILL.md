---
name: acta-consejo-sa-sobre-transmision-acciones-propuesta-mer-0206
description: "Acta del consejo de una SA sobre transmisión de acciones y propuesta de ampliación de capital. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta del consejo de una SA sobre transmisión de acciones y propuesta de ampliación de capital

> Formulario **MER-0206** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Acta del Consejo de Administración de una Sociedad Anónima en la que se informa sobre la recepción de solicitudes de transmisión de acciones, aprobándose por unanimidad el autorizar al Consejero Delegado para que lleve a cabo las actuaciones necesarias para proceder a esa transmisión, así como la aprobación de proceder a la ampliación del capital social. Exposición de los últimos acuerdos aprobados por la sociedad.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta del consejo de una SA sobre transmisión de acciones y propuesta de ampliación de capital» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta del consejo de una SA sobre transmisión de acciones y propuesta de ampliación de capital” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-consejo-sa-sobre-transmision-acciones-propuesta-mer-0206`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº (2 veces)

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

Acta del Consejo de Administración de una Sociedad Anónima en la que se informa sobre la recepción de solicitudes de transmisión de acciones, aprobándose por unanimidad el autorizar al Consejero Delegado para que lleve a cabo las actuaciones necesarias para proceder a esa transmisión, así como la aprobación de proceder a la ampliación del capital social. Exposición de los últimos acuerdos aprobados por la sociedad.


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

CONSEJO DE ADMINISTRACION DE [DENOMINACIÓN SOCIAL]

Presidente

D./Dña. [NOMBRE Y APELLIDOS]

Consejeros

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

Secretario

D./Dña. [NOMBRE Y APELLIDOS]

En [LOCALIDAD], siendo las [Nº] horas del día [FECHA] se reúne el Consejo de Administración de [DENOMINACIÓN SOCIAL], S.A. en el domicilio social, con asistencia de los señores que arriba se expresan, previamente citados por el Secretario, al término de la reunión celebrada por la Junta General Extraordinaria de Accionistas, celebrada con anterioridad en el día de hoy.

Preside la reunión D./Dña. [NOMBRE Y APELLIDOS], y actúa de Secretario del Consejo, D./Dña. [NOMBRE Y APELLIDOS]

Abierto el acto por el Sr. Presidente, éste declara el Consejo válidamente constituido, de conformidad con lo establecido en el art. 247.2 de la Ley de Sociedades de Capital, por encontrarse presentes en la reunión, la totalidad de sus componentes, procediendo a dar lectura al Orden del Día:

ORDEN DEL DIA

1.- Informe sobre recepción de solicitudes de transmisión de acciones a efectos de lo establecido en el art. de los Estatutos Sociales.

2.- Informe y propuesta sobre aumento de capital social.

3.- Exposición de últimos acuerdos con la mercantil [DENOMINACIÓN SOCIAL]

Acto seguido se procede a abordar cada uno de los extremos mencionados por el orden en que han sido relacionados en las citaciones tal como ha quedado expuesto.

1.- Informe sobre recepcion de solicitudes de transmision de acciones a efectos de lo establecido en el art. de los estatutos sociales.

Por el Sr. Presidente se informa de que se ha recibido en la sede social la notificación fehaciente por parte de [NOMBRE Y APELLIDOS] de su intención de proceder a la venta de las acciones que posee de nuestra sociedad, ejercitando con ello el derecho de opción de venta que le fue atribuido mediante acuerdo de Junta General celebrada el [FECHA] y documento firmado al efecto

Con el objetivo de cumplir cuanto exigen los vigentes Estatutos Sociales, y concretamente el mencionado art. se reseñan los datos de la pretendida venta.

Comprador: [DENOMINACIÓN SOCIAL], SA para autocartera.

Precio: [IMPORTE] euros

Numeración:

Se acuerda también por unanimidad dar traslado a todos los socios de las transmisiones anunciadas a los efectos oportunos.

2.- Informe y propuesta sobre aumento de capital social

A continuación se cede la palabra al Consejero Delegado D./Dña. [NOMBRE Y APELLIDOS], quien da lectura a un informe sobre la necesidad de proceder a la ampliación del capital social en la cantidad de [IMPORTE] euros, proponiendo su aprobación por este Consejo a fin de ser expuesto en la Junta General de Accionistas que se celebrará [FECHA].

Tras un examen de las razones expuestas en el informe, se aprueba por unanimidad proceder a la ampliación propuesta, a fin de que sea remitido a la Junta General.

3.- Exposicion de ultimos acuerdos con la mercantil

A continuación por el Sr. Presidente se da lectura a los últimos acuerdos firmados, comentándose por los Sres. Consejeros las ventajas y dificultades que conllevan en armonioso debate.

Se aprueba y ratifica por unanimidad por el Consejo la firma de dichos acuerdos.

Por último se somete a la consideración del Consejo la posible aprobación del Acta por el mismo, y habiéndose decidido así, se procede a la redacción de la presente. Redactado y leído el presente texto, el consejo, por unanimidad de todos los asistentes, acuerda aprobar la presente acta.

Y no habiendo más asuntos que tratar, se levanta la sesión en [LOCALIDAD] a las [Nº] horas del [FECHA]

D./Dña. [NOMBRE Y APELLIDOS]

El secretario:

D./Dña. [NOMBRE Y APELLIDOS]

Vº Bº El Presidente:

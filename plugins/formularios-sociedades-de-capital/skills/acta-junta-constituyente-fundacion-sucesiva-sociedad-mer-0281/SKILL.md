---
name: acta-junta-constituyente-fundacion-sucesiva-sociedad-mer-0281
description: "Acta de la junta constituyente en la fundación sucesiva de una sociedad anónima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de la junta constituyente en la fundación sucesiva de una sociedad anónima

> Formulario **MER-0281** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de acta de Junta constituyente para el supuesto de una fundación sucesiva de una Sociedad Anónima, en la que se procede a elaborar la lista de suscriptores, así como la aprobación de las gestiones de los promotores, de los estatutos sociales, del valor dado de las aportaciones no dinerarias y el nombramiento de los Administradores, entre otras cosas, puntos establecidos en el orden del día.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de la junta constituyente en la fundación sucesiva de una sociedad anónima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de la junta constituyente en la fundación sucesiva de una sociedad anónima” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-junta-constituyente-fundacion-sucesiva-sociedad-mer-0281`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (3 veces)
- [ ] Nº (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] INTERVENCIONES DE LOS ASISTENTES
- [ ] LOCALIDAD
- [ ] PUNTO DEL ORDEN DEL DÍA
- [ ] SUSCRIPTORES ASISTENTES

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

Modelo de acta de Junta constituyente para el supuesto de una fundación sucesiva de una Sociedad Anónima, en la que se procede a elaborar la lista de suscriptores, así como la aprobación de las gestiones de los promotores, de los estatutos sociales, del valor dado de las aportaciones no dinerarias y el nombramiento de los Administradores, entre otras cosas, puntos establecidos en el orden del día.


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

En [LOCALIDAD], a [FECHA], siendo las [Nº] horas y en el domicilio [DOMICILIO]

Se celebra la presente Junta constituyente de [DENOMINACIÓN SOCIAL], Sociedad en formación, cuya convocatoria ha sido efectuada por los promotores mediante carta certificada remitida con la debida antelación [FECHA] y mediante el correspondiente anuncio en el Boletín Oficial del Registro Mercantil de fecha [FECHA].

Actúa como Presidente de la Junta D./Dña. [NOMBRE Y APELLIDOS], en su calidad de promotor que consta como primer firmante del Programa de Fundación, y como Secretario D./Dña. [NOMBRE Y APELLIDOS], elegido al efecto por los suscriptores asistentes.

Se procede a elaborar la lista de suscriptores [SUSCRIPTORES ASISTENTES], y al concurrir un número de suscriptores suficiente, por el Presidente se declara válidamente constituida la Junta.

Seguido lo cual el Secretario da paso a la lectura del Orden del Día fijado en la convocatoria, que es aceptado por unanimidad por todos los asistentes, cuyo contenido es el siguiente:

1º.- Aprobación de las gestiones realizadas hasta la presente Junta por los promotores.
2º.- Aprobación de los Estatutos Sociales.
3º.- Aprobación del valor dado a las aportaciones no dinerarias.
4º.- Aprobación de los beneficios particulares reservados a los promotores.
5º.- Nombramiento de los Administradores de la Sociedad.
6º.- Designación de quienes habrán de otorgar la escritura fundacional de la Sociedad.
7º.- [PUNTO DEL ORDEN DEL DÍA].
8º.- Ruegos y preguntas.
9º.- Lectura y, en su caso, aprobación del Acta de la reunión.

Diligencia del Secretario para hacer constar que tras la constitución de la Junta y lectura y aprobación del Orden del Día, se procede a suscribir la presente Acta por la totalidad de los accionistas presentes en este momento.

A continuación se procede al debate de los asuntos contenidos en el Orden del Día se aluden los siguientes aspectos y se producen las siguientes intervenciones [INTERVENCIONES DE LOS ASISTENTES].

No solicitándose por ninguno de los accionistas la palabra y no habiendo más asuntos que tratar, el Presidente da por concluido el debate y suspende momentáneamente la sesión para la redacción por el Secretario de la presente Acta, en la cual queda reflejada la adopción de los siguientes

ACUERDOS

Primero.-

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Una vez redactada el Acta y leída íntegramente por el Secretario, se somete a la aprobación de los asistentes, que la aprueban por unanimidad, por encontrarla conforme a lo debatido y acordado.

Acto seguido, se levanta la sesión, siendo las [Nº] horas del día señalado en el encabezamiento, procediéndose a la firma de la presente por mí, el Secretario, con el Visto Bueno del Presidente.

Secretario

VºBº Presidente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

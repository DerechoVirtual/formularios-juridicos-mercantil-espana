---
name: acta-junta-sl-sa-designa-auditor-cuentas-mer-0134
description: "Acta de junta de SL o SA que designa al auditor de cuentas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de junta de SL o SA que designa al auditor de cuentas

> Formulario **MER-0134** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de junta de SL o SA que designa al auditor de cuentas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de junta de SL o SA que designa al auditor de cuentas” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-junta-sl-sa-designa-auditor-cuentas-mer-0134`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] Nº (7 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] FECHA (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] DNI/NIE
- [ ] FOLIO
- [ ] HOJA
- [ ] LUGAR DE CELEBRACIÓN
- [ ] Nº DE ARTÍCULO
- [ ] SECCIÓN
- [ ] TOMO
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

La persona que deba ejercer la auditoría de cuentas será nombrada por la junta general antes de que finalice el ejercicio a auditar, por un período de tiempo inicial, que no podrá ser inferior a tres años ni superior a nueve, a contar desde la fecha en que se inicie el primer ejercicio a auditar, sin perjuicio de lo dispuesto en la normativa reguladora de la actividad de auditoría de cuentas respecto a la posibilidad de prórroga y a la duración de los contratos en relación con sociedades calificadas como entidades de interés público.

La junta podrá designar a una o varias personas físicas o jurídicas que actuarán conjuntamente. Cuando los designados sean personas físicas, la junta deberá nombrar tantos suplentes como auditores titulares.

La junta general no podrá revocar al auditor antes de que finalice el periodo inicial para el que fue nombrado, o antes de que finalice cada uno de los trabajos para los que fue contratado una vez finalizado el periodo inicial, a no ser que medie justa causa.


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

ACTA DE JUNTA GENERAL DE ‘
SL
SA

En [LUGAR DE CELEBRACIÓN], siendo las [Nº] horas del día [FECHA], se reúne en el domicilio social de ‘ [ELEGIR: SL / SA] la Junta General de Socios, previa convocatoria al efecto del Consejo de Administración de la citada mercantil realizada

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Por comunicación individual]

El texto íntegro de la convocatoria es el siguiente:

Según lo previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales, actúa como Presidente de la junta quien lo es del Consejo de Administración, D./Dña. [NOMBRE Y APELLIDOS], y como Secretario D./Dña. [NOMBRE Y APELLIDOS].

Asisten igualmente los restantes miembros del Consejo de Administración.

El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las [ELEGIR: participaciones / acciones] que poseen y/o representan cada uno de ellos:

Socios presentes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [ELEGIR: participaciones / acciones] numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Firmado:

Socios representados:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], mayor de edad y con D.N.I [DNI/NIE] asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [ELEGIR: participaciones / acciones] sociales numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Firmado:

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [ELEGIR: participaciones / acciones], que representan el % del capital social con derecho a voto.

Hallándose presente el citado capital, se procede a la declaración por el Presidente de la válida constitución de la Junta en [ELEGIR: primera / segunda] convocatoria, seguido lo cual el Secretario da paso a la lectura del Orden del Día fijado en la convocatoria.

A continuación, se procede al debate de los asuntos contenidos en el Orden del Día se aluden los siguientes aspectos y se producen las siguientes intervenciones

No solicitándose por ninguno de los socios la palabra y no habiendo más asuntos que tratar, el Presidente da por concluido el debate y suspende momentáneamente la sesión para la redacción por el Secretario de la presente Acta, en la cual queda reflejada la adopción de los siguientes:

ACUERDOS:

Primero. Nombramiento de auditores de la sociedad.—

El presidente informa a la junta sobre la conclusión de la vigencia del contrato con los auditores de la sociedad, por lo que la junta debe proceder al nombramiento de nuevos auditores.

Tras ello la junta acuerda por unanimidad nombrar como nuevo auditor a la sociedad “ [ELEGIR: SL / SA], inscrita en el Registro Mercantil número [NÚMERO] de [LOCALIDAD], hoja [HOJA], folio [FOLIO], tomo [TOMO], general [Nº] de la sección [SECCIÓN] del Libro de Sociedades, con domicilio en [LOCALIDAD], calle [CALLE] número [NÚMERO] y NIF número

De acuerdo con los términos que marca la Ley 22/2015, de 20 de julio, de Auditoría de Cuentas, el nombramiento se hace por un período de nueve años a contar desde el primer día del primero de los ejercicios a auditar, es decir, a partir del [FECHA] No obstante, transcurridos los tres primeros años del contrato, ambas partes podrán, con un preaviso de tres meses a la fecha usual de comienzo del trabajo, resolverlo por mutuo acuerdo y siempre que exista una causa razonable para cualquiera de las partes.

Segundo. Otorgamiento de facultades para la ejecución de los acuerdos adoptados.—

Se acuerda por unanimidad facultar solidaria e indistintamente a [NOMBRE Y APELLIDOS] para que comparezcan ante notario, eleven a público los acuerdos adoptados y realicen cuantas aclaraciones y subsanaciones sean necesarias hasta lograr la inscripción de estos acuerdos en el correspondiente Registro Mercantil, pudiendo solicitar, en su caso, la anotación preventiva de los mismos, así como su inscripción parcial.

Tercero. Ruegos y preguntas.—

Abierto el período de ruegos y preguntas ninguno de los asistentes hace uso de la palabra.

[ELEGIR UNA OPCIÓN: Aprobación por unanimidad / Aprobación por mayoría con oposición de socio]

El Secretario

Vº Bº El Presidente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

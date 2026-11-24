---
name: acta-asamblea-cooperativa-acuerda-demandar-consejeros-mer-0436
description: "Acta de asamblea de cooperativa que acuerda demandar a consejeros sin constar en el orden del día. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de asamblea de cooperativa que acuerda demandar a consejeros sin constar en el orden del día

> Formulario **MER-0436** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de acta de Junta General de una sociedad cooperativa en la que se acuerda ejercitar la acción social de responsabilidad contra determinados miembros del Consejo Rector por entender que han causado un perjuicio irreparable, sin que estuviese en los puntos a tratar en el orden del día de la Junta.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de asamblea de cooperativa que acuerda demandar a consejeros sin constar en el orden del día» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de asamblea de cooperativa que acuerda demandar a consejeros sin constar en el orden del día” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:acta-asamblea-cooperativa-acuerda-demandar-consejeros-mer-0436`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] Nº (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] ASUNTO DEL ORDEN DEL DÍA
- [ ] CALLE
- [ ] DIRECCIÓN
- [ ] DNI/NIE
- [ ] EJERCICIO
- [ ] EXPONER LOS HECHOS
- [ ] LUGAR
- [ ] MOTIVO
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

Modelo de acta de Junta General de una sociedad cooperativa en la que se acuerda ejercitar la acción social de responsabilidad contra determinados miembros del Consejo Rector por entender que han causado un perjuicio irreparable, sin que estuviese en los puntos a tratar en el orden del día de la Junta.


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

ACTA DE JUNTA GENERAL DE ‘[DENOMINACIÓN SOCIAL], S.Coop.’

En [LOCALIDAD], siendo las [Nº] horas del día [FECHA], se reúne en el domicilio social de ‘[DENOMINACIÓN SOCIAL], S.Coop.’ en [ELEGIR: primera / segunda] convocatoria, su Junta General Ordinaria, previa convocatoria al efecto del Consejo Rector de la citada cooperativa realizada mediante anuncio expuesto públicamente de forma destacada en dicho domicilio social y en cada uno de los demás centros en que la cooperativa desarrolle su actividad.

A continuación se transcribe el texto íntegro de la convocatoria:

‘CONVOCATORIA DE ASAMBLEA GENERAL ORDINARIA DE ‘[DENOMINACIÓN SOCIAL], S.COOP’

El Consejo Rector de ‘[DENOMINACIÓN SOCIAL], S.Coop.’ convoca a sus socios a la Asamblea General Ordinaria que tendrá lugar en el domicilio social, sito en [LOCALIDAD], en la [DIRECCIÓN], el día [FECHA] a sus [Nº] horas, en primera convocatoria, y si fuere preciso, en el mismo lugar el día [FECHA], a las [Nº] horas en segunda convocatoria.

El Orden del Día es el siguiente:

Primero.- Aprobación o censura de las cuentas anuales, informe de gestión y propuesta de aplicación de resultados del ejercicio [EJERCICIO]

Segundo.- Aprobación o censura de la gestión social.

Tercero.- [ASUNTO DEL ORDEN DEL DÍA]

Cuarto.- Ruegos y preguntas.

Quinto.- Redacción, lectura y, en su caso, aprobación del acta de la reunión.

En [LUGAR], a [FECHA].

El Presidente del Consejo Rector’.

Actúa como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario D./Dña. [NOMBRE Y APELLIDOS], quienes lo son, a su vez, del Consejo Rector.

El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios presentes:

D./Dña. [NOMBRE Y APELLIDOS] Firmado:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios representados:

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], calle [CALLE], mayor de edad y con D.N.I [DNI/NIE] asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS]

Firmado:

Todas las citadas representaciones se acreditan de forma legal, a satisfacción de la Asamblea General.

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [Nº] votos, que representan el [PORCENTAJE] de los votos sociales. [OTROS DATOS].

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Asamblea General.

Sobre las citadas manifestaciones del Presidente ningún asistente protesta ni presenta reserva alguna.

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo a continuación

Se trae a debate, pese a no constar como punto del Orden del Día, la posibilidad de entablar la acción social de responsabilidad contra los miembros del Consejo Rector D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] con motivo de sus siguientes actuaciones [EXPONER LOS HECHOS], tras todo lo cual la Asamblea

ACUERDA:

Primero.-

Segundo.-

Tercero.-

Cuarto.- Ejercitar la acción social de responsabilidad contra los miembros del Consejo Rector D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] por [MOTIVO], que se considera que ha causado un perjuicio irreparable para la sociedad.

Tras todo lo cual, redactada y leída que fue el acta por el Secretario, esta es aprobada por la Junta, por unanimidad de los asistentes.

No existiendo más asuntos que tratar, se levanta la sesión.

Vº Bº Presidente

Secretario

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

Asistentes

Firmado: D./Dña. [NOMBRE Y APELLIDOS]

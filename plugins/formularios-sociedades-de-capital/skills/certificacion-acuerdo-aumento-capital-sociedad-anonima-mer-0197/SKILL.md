---
name: certificacion-acuerdo-aumento-capital-sociedad-anonima-mer-0197
description: "Certificación del acuerdo de aumento de capital de una sociedad anónima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación del acuerdo de aumento de capital de una sociedad anónima

> Formulario **MER-0197** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación del acuerdo de aumento de capital de una sociedad anónima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación del acuerdo de aumento de capital de una sociedad anónima” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdo-aumento-capital-sociedad-anonima-mer-0197`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] CALLE
- [ ] CLASE DE ACCIONES
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE Y APELLIDOS
- [ ] NÚMERO
- [ ] PORCENTAJE
- [ ] TIPO DE JUNTA
- [ ] ÓRGANO
- [ ] ÓRGANO O PERSONA

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

AMPLIACIÓN DE CAPITAL: CERTIFICADO

D./Dña. [NOMBRE Y APELLIDOS], Secretario del Consejo de Administración de [DENOMINACIÓN SOCIAL] S.A., con domicilio social en [LOCALIDAD], calle [CALLE], número [NÚMERO] y N.I.F.

CERTIFICA

CONVOCATORIA Y ORDEN DEL DÍA

Que la Junta General Extraordinaria de la citada mercantil convocada mediante [ÓRGANO] y celebrada el pasado día [DÍA] de [MES] de [AÑO] en el domicilio social de la misma, [TIPO DE JUNTA] tuvo el siguiente Orden del Día:

1º) Aumento de capital en la suma de [IMPORTE] euros por cualquier procedimiento y contravalor, y adopción de cuantos acuerdos complementarios sean necesarios, en especial la consiguiente modificación del artículo [Nº DE ARTÍCULO] de los Estatutos Sociales.

2º) Delegación en el órgano de administración para su ejecución en la forma legal

3º) Los socios tienen derecho a examinar en el domicilio social el texto íntegro de la modificación y del informe sobre la misma y de pedir la entrega o envío gratuito de dichos documentos

4º) Ruegos y preguntas.

5º) Aprobación, en su caso, del acta de la Junta.

LISTA DE ASISTENTES

Que se confeccionó por escrito la lista de asistentes, la cual obra al comienzo del acta.

PRESIDENTE Y SECRETARIO

Que actuaron como Presidente y Secretario de la Junta quienes ocupan dichos cargos en el Consejo de Administración, cargos que declararon vigentes e inscritos en el Registro Mercantil de

INFORME JUSTIFICATIVO

Que el órgano de administración presentó el oportuno informe justificativo de la modificación de fecha [FECHA]

ADOPCIÓN DE ACUERDOS

Que a continuación se procedió al debate de los asuntos contenidos en el Orden del Día, se aludieron los siguientes aspectos y se produjeron las siguientes intervenciones

Que no solicitándose por ninguno de los accionistas la palabra y no habiendo más asuntos que tratar, el Presidente dio por concluido el debate y suspendió momentáneamente la sesión para la redacción por el Secretario de la correspondiente Acta, en la cual quedó reflejada la adopción de los siguientes ACUERDOS:

[ELEGIR UNA OPCIÓN: Ampliación de capital / Mediante la emisión de nuevas acciones con derecho de suscripción preferente / Mediante la emisión de nuevas acciones sin derecho de suscripción preferente / Amplicación de capital mediante aumento del valor nominal de las acciones]

MODIFICACIÓN DE LOS ESTATUTOS SOCIALES

En consecuencia, se acuerda por unanimidad modificar el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"El capital de la sociedad es de [IMPORTE] euros y está representado por [ÓRGANO O PERSONA] acciones [CLASE DE ACCIONES], de valor nominal [IMPORTE] euros cada una de ellas, numeradas correlativamente del 1 al [Nº], ambos inclusive. Todas las acciones son de una sola serie, confieren los mismos derechos y obligaciones y están totalmente desembolsadas en el 100% de su valor nominal".

ELEVACIÓN A ESCRITURA PÚBLICA

Se faculta al Secretario del Consejo de Administración para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando para ello las escrituras correspondientes, incluidas, en su caso, las de subsanación, aclaración o rectificación, así como para realizar cuantas operaciones fueren precisas para la plena eficacia de dichos acuerdos"

Que dichos acuerdos fueron aprobados con el voto favorable del [PORCENTAJE] % del capital concurrente con derecho a voto.

Que una vez redactada el Acta, esta fue leída íntegramente por el Secretario, se sometió a la aprobación de los asistentes, que la aprobaron por unanimidad, por encontrarla conforme a lo debatido y acordado, seguido lo cual se levantó la sesión, siendo las [Nº] horas del día señalado y procediéndose a la firma de la misma por el Secretario, con el Visto Bueno del Presidente.

Así se certifica, para que conste, en cumplimiento de lo previsto en la Ley de Sociedades de Capital y en el Reglamento del Registro Mercantil, con el Vº.Bº del Presidente, en [LUGAR], a [DÍA] de [MES] de [AÑO].

Vº.Bº,el Presidente,	El Secretario,

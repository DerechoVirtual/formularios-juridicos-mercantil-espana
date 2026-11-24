---
name: acta-consejo-rector-cooperativa-nombra-consejero-mer-0440
description: "Acta del consejo rector de una cooperativa que nombra consejero delegado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta del consejo rector de una cooperativa que nombra consejero delegado

> Formulario **MER-0440** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de acta de una reunión llevada a cabo por el Consejo Rector de una sociedad cooperativa, mediante la cual se acepta la dimisión del consejero delegado y se nombra a otro por cinco años, siendo adoptado dicho acuerdo por unanimidad.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta del consejo rector de una cooperativa que nombra consejero delegado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta del consejo rector de una cooperativa que nombra consejero delegado” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:acta-consejo-rector-cooperativa-nombra-consejero-mer-0440`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (16 veces)
- [ ] FECHA (7 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NÚMERO (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] Nº (2 veces)
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] OTROS DATOS
- [ ] PLAZO

## Normas que cita el formulario

- art. 36 Ley 27/1999

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

Modelo de acta de una reunión llevada a cabo por el Consejo Rector de una sociedad cooperativa, mediante la cual se acepta la dimisión del consejero delegado y se nombra a otro por cinco años, siendo adoptado dicho acuerdo por unanimidad.


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

CONSEJO RECTOR DE [DENOMINACIÓN SOCIAL]

Presidente

D./Dña. [NOMBRE Y APELLIDOS]

Consejeros

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

En [LOCALIDAD], siendo las [Nº] horas del día [FECHA] se reúne el Consejo Rector de [DENOMINACIÓN SOCIAL], S.Coop. en el domicilio social [DIRECCIÓN], con asistencia de los señores que arriba se expresan, previamente citados por el Sr. Presidente.

Preside la reunión D./Dña. [NOMBRE Y APELLIDOS], y actúa de Secretario del Consejo D./Dña. [NOMBRE Y APELLIDOS]

Abierto el acto por el Sr. Presidente, éste declara el Consejo válidamente constituido, de conformidad con lo establecido en el art. 36 de la Ley 27/1999, de 16 de julio, de Cooperativas, por encontrarse presentes en la reunión [OTROS DATOS], procediendo a dar lectura al Orden del Día:

ORDEN DEL DIA

1.- Nombramiento de Consejero Delegado

Toma la palabra el secretario D./Dña. [NOMBRE Y APELLIDOS], recordando que en la Asamblea General de carácter Universal celebrada con anterioridad en el día de hoy, se aceptó la dimisión como Consejero de D./Dña. [NOMBRE Y APELLIDOS], quien al mismo tiempo dimitió de su cargo como Consejero-Delegado de la Sociedad.

D./Dña. [NOMBRE Y APELLIDOS] fue designado Consejero-Delegado en la reunión del Consejo Rector celebrada el [FECHA], el cual fue elevado a público el [FECHA], ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], y con el nº [NÚMERO] de su protocolo, e inscrito en el Registro Mercantil de [LOCALIDAD].

Seguidamente el Presidente propone designar como Consejero Delegado y por un plazo de cinco años, a D./Dña. [NOMBRE Y APELLIDOS]

D./Dña. [NOMBRE Y APELLIDOS], presente en la reunión, acepta el nombramiento para el que ha sido propuesto, a la vez que agradece la confianza en él depositada.

El consejo, por unanimidad,

ACUERDA

Primero.- Aceptar la dimisión de D./Dña. [NOMBRE Y APELLIDOS] como Consejero-Delegado, cargo para el que fue designado en el Consejo Rector en su reunión celebrada el [FECHA], el cual fue elevado a público el [FECHA], ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], y con el nº [NÚMERO] de su protocolo, e inscrito en el Registro Mercantil de [LOCALIDAD],

Segundo.- Nombrar como Consejero-Delegado y por un periodo de [PLAZO], al miembro del Consejo, D./Dña. [NOMBRE Y APELLIDOS], de nacionalidad española, nacido el [FECHA], casado/a, economista, vecino/a de [LOCALIDAD], [DOMICILIO] y con D.N.I. nº [NÚMERO], el cual presente en la reunión, acepta el cargo para el que ha sido elegido, manifestando no hallarse incurso en causa alguna de incompatibilidad de las reguladas por la normativa vigente.

Tercero.- Apoderar al Secretario D./Dña. [NOMBRE Y APELLIDOS] para que concurra ante Notario, eleve a públicos estos acuerdos, y siga lo necesario para su inscripción registral, facultándole incluso para corregir, subsanar e interpretar dichos acuerdos a fin de que queden debidamente inscritos.

Por último se somete a la consideración del Consejo la posible aprobación del Acta por el mismo, y habiéndose decidido así, se procede a la redacción de la presente. Redactado y leído el presente texto,

El consejo, por unanimidad de todos los asistentes, acuerda aprobar la presente acta.

Y no habiendo más asuntos que tratar, se levanta la sesión en [LOCALIDAD] a las [Nº] horas del [FECHA]

El Secretario

Vº Bº el Presidente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

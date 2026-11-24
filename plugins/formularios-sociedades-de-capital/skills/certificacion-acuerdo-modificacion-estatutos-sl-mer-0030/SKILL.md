---
name: certificacion-acuerdo-modificacion-estatutos-sl-mer-0030
description: "Certificación del acuerdo de modificación de estatutos de una SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación del acuerdo de modificación de estatutos de una SL

> Formulario **MER-0030** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Certificación de acta de Junta General Extraordinaria convocada o Universal en la que se adopta el acuerdo de modificación de estatutos por traslado de domicilio, modificación o sustitución del objeto social, cambio de denominación, creación y extinción anticipada de prestaciones accesorias, duración de la compañía, y modificación del Régimen de transmisión de participaciones sociales

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación del acuerdo de modificación de estatutos de una SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación del acuerdo de modificación de estatutos de una SL” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdo-modificacion-estatutos-sl-mer-0030`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] FECHA (7 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DESCRIBIR (4 veces)
- [ ] DIRECCIÓN (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] SOCIOS AFECTADOS (4 veces)
- [ ] Nº (3 veces)
- [ ] OBJETO SOCIAL (3 veces)
- [ ] PUNTO DEL ORDEN DEL DÍA (3 veces)
- [ ] LUGAR (2 veces)
- [ ] ÓRGANO (2 veces)
- [ ] CALLE
- [ ] NORMATIVA APLICABLE
- [ ] Nº DE ARTÍCULO
- [ ] PAÍS

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

Certificación de acta de Junta General Extraordinaria convocada o Universal en la que se adopta el acuerdo de modificación de estatutos por traslado de domicilio, modificación o sustitución del objeto social, cambio de denominación, creación y extinción anticipada de prestaciones accesorias, duración de la compañía, y modificación del Régimen de transmisión de participaciones sociales


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

En [LUGAR], a [FECHA].

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de [ELEGIR: administrador único / administrador solidario / administradores mancomunados / Secretario del Consejo de Administración] de ‘[DENOMINACIÓN SOCIAL], S.L.’ y de su Junta de socios reunida el pasado [FECHA].

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de [ELEGIR: liquidador único / liquidador solidario / liquidadores mancomunados / Secretario del Consejo de Liquidación] de ‘[DENOMINACIÓN SOCIAL], S.L.’ y de su Junta de socios reunida el pasado [FECHA].

CERTIFICO

- Que en [LOCALIDAD] calle [CALLE], domicilio social de SL con fecha de dede", se celebró Junta General Universal de socios de la entidad.
- Que en la junta estuvo, presente la totalidad del capital social, todo él con derecho a voto, y
- Que todos los asistentes firmaron en el acta, bajo su nombre respectivo, aceptando la constitución de la Junta con carácter de universal y con el siguiente

ORDEN DEL DÍA

[OPCIONAL — incluir si procede]

Primero. Trasladar el domicilio social de la compañía a la [DIRECCIÓN], de la localidad de [LOCALIDAD], y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

[OPCIONAL — incluir si procede]

Primero. Trasladar el domicilio social de la compañía a [DIRECCIÓN], en [LOCALIDAD] y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

[OPCIONAL — incluir si procede]

Primero. Sustituir el objeto social anterior por el siguiente [OBJETO SOCIAL], y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

[OPCIONAL — incluir si procede]

Primero. Modificar el objeto social de la compañía en el siguiente sentido [OBJETO SOCIAL], y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

[OPCIONAL — incluir si procede]

Primero. Modificar la actual denominación de la sociedad, [DENOMINACIÓN SOCIAL] ‘S.L.’, por ‘ S.L.’ y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

[OPCIONAL — incluir si procede]

Primero.

Prorrogar la duración de la sociedad [DENOMINACIÓN SOCIAL] hasta [FECHA]

Conversión de la duración de la sociedad a tiempo indefinido, y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

[OPCIONAL — incluir si procede]

Primero. Crear prestaciones accesorias consistentes en [DESCRIBIR] para los socios [SOCIOS AFECTADOS], y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

[OPCIONAL — incluir si procede]

Primero. Extinguir anticipadamente las prestaciones accesorias consistentes en [DESCRIBIR] vigentes para los socios [SOCIOS AFECTADOS], y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

[OPCIONAL — incluir si procede]

Primero. Modificar el régimen de transmisión de las participaciones de la compañía, y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

Segundo. [PUNTO DEL ORDEN DEL DÍA].

[PUNTO DEL ORDEN DEL DÍA]

Ruegos y preguntas.

[PUNTO DEL ORDEN DEL DÍA]

Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

- Que, conforme a las disposiciones legales y estatutarias, se designaron los cargos de Presidente y Secretario de la reunión.

- Que se confeccionó por escrito la lista de asistentes, la cual obra al comienzo del acta.

- Que la Junta adoptó, por unanimidad, los acuerdos que se transcriben literalmente a continuación:

ACUERDOS

[OPCIONAL — incluir si procede]

Primero.- Traslado del domicilio social

A la vista de la propuesta de modificación, se acuerda trasladar el domicilio social de la compañía a la [DIRECCIÓN] de la localidad de [LOCALIDAD].

[OPCIONAL — incluir si procede]

Primero.- Traslado del domicilio social al extranjero

A la vista del informe de los administradores, y del proyecto de traslado depositado en el RM y publicado en el BORM, se acuerda trasladar el domicilio social de ‘[DENOMINACIÓN SOCIAL], S.L.’ a [DIRECCIÓN], en [PAÍS], con mantenimiento de su personalidad jurídica, en virtud de lo previsto en [NORMATIVA APLICABLE].

[OPCIONAL — incluir si procede]

Primero.- Sustitución y modificación del objeto social

A la vista de la propuesta de modificación efectuada por el órgano de administración, se acuerda sustituir el objeto social por [OBJETO SOCIAL].

[OPCIONAL — incluir si procede]

Primero.- Cambio de la denominación social

A la vista del informe de los administradores al efecto, de la propuesta de modificación, y del certificado negativo de denominación expedido por el Registro Mercantil Central, según el cual no figura entidad alguna registrada con el nuevo nombre que pretende darse a la sociedad, se acuerda modificar la denominación social, que de ‘[DENOMINACIÓN SOCIAL], S.L.’ pase a ser ‘[DENOMINACIÓN SOCIAL], S.L.’.

[OPCIONAL — incluir si procede]

Primero.- Prórroga de la duración de la sociedad

A la vista la propuesta de modificación, se acuerda prorrogar la duración de la sociedad hasta [FECHA].

[OPCIONAL — incluir si procede]

Primero.- Creación de prestaciones accesorias

A) Modificación de los estatutos.

A la vista de la propuesta de modificación, se acuerda la creación de prestaciones accesorias consistentes en [DESCRIBIR], de carácter [ELEGIR: gratuito / retribuido], y exigibles a los socios titulares de las participaciones [SOCIOS AFECTADOS], quienes en muestra de su consentimiento individual lo hacen constar de forma separada al final del acta

B) La creación de las prestaciones accesorias acordada se hace constar en los títulos representativos de las participaciones que las llevan aparejadas mediante [ÓRGANO].

[OPCIONAL — incluir si procede]

Primero.- Extinción anticipada de prestaciones accesorias

A) A la vista del informe de los administradores al efecto, y de la propuesta de modificación, se acuerda la extinción de las prestaciones accesorias consistentes en [DESCRIBIR], de carácter [ELEGIR: gratuito / retribuido], y exigibles a los socios titulares de las participaciones [SOCIOS AFECTADOS], vigentes hasta este momento, quienes en muestra de su consentimiento individual lo hacen constar de forma separada al final del acta

B) La extinción de las prestaciones accesorias acordada se hace constar en los títulos representativos de las participaciones que las llevan aparejadas mediante [ÓRGANO].

[OPCIONAL — incluir si procede]

Primero.- Modificación del régimen de transmisión de las participaciones de la compañía

A la vista de la propuesta de modificación, se acuerda transformar el régimen de transmisión de las participaciones de la compañía.

Segundo.- Modificación de los Estatutos Sociales

Como consecuencia del acuerdo de [FECHA] suscrito, se conviene por unanimidad modificar el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

Tercero.- Elevación a público

Se faculta al Secretario del Consejo de Administración para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando para ello las escrituras correspondientes, incluidas, en su caso, las de subsanación, aclaración o rectificación, así como para realizar cuantas operaciones fueren precisas para la plena eficacia de dichos acuerdos.

[OPCIONAL — incluir si procede]

Para los casos de modificación y/o sustitución del objeto social; prórroga de la duración de la sociedad, creación de prestaciones accesorias, extinción anticipada de prestaciones accesorias, modificación del régimen de transmisión de participaciones y traslado del domicilio social al extranjero.

Cuarto.- Derecho de separación

Abierto el turno de ruegos y preguntas, no se formula ninguna. Se recuerda a los señores socios que no han votado a favor del presente acuerdo su derecho a separarse de la sociedad, derecho que, en su caso, deberá ejercitarse por escrito dirigido al órgano de administración de la sociedad, y en el plazo de un mes a contar desde la publicación del presente acuerdo en el Boletín Oficial del Registro Mercantil o, en su caso, desde la recepción de su comunicación Quienes ejerciten dicho derecho tendrán igualmente derecho al reembolso del valor de sus participaciones.

[OPCIONAL — incluir si procede]

Para los casos de creación y extinción anticipada de prestaciones accesorias

Quinto.- Consentimiento individual

Consentimiento de cada uno de los afectados por el acuerdo de creación de
prestaciones accesorias
extinción anticipada de prestaciones accesorias

Estando presentes en este acto:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] titular de [Nº] participaciones sociales numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

- Que el acta fue aprobada por la propia Junta, así como firmada por el Secretario con el Visto Bueno del Presidente, todo ello al término de la reunión.

Y, para que conste y surta los oportunos efectos, se expide la presente certificación- con el Visto Bueno del Presidente D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

D./Dña. [NOMBRE Y APELLIDOS]

administrador único
administrador solidario
administradores mancomunados
Secretario del Consejo de Administración

Secretario

Vº Bº Presidente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

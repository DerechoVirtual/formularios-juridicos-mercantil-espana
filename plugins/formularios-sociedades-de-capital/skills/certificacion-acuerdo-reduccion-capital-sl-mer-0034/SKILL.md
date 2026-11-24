---
name: certificacion-acuerdo-reduccion-capital-sl-mer-0034
description: "Certificación del acuerdo de reducción de capital de una SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación del acuerdo de reducción de capital de una SL

> Formulario **MER-0034** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de certificado de acta de Junta General (Extraordinaria o Universal) de Socios de una Sociedad de Responsabilidad Limitada en la que se acuerda la reducción de capital mediante la disminución del valor nominal de las participaciones sociales, su amortización o su agrupación, con la finalidad de restablecer el equilibrio entre el capital y el patrimonio neto de la sociedad disminuido por consecuencia de pérdidas, la constitución o el incremento de la reserva legal o de las reservas voluntarias o la devolución del valor de las aportaciones. Incluye también el acuerdo de modificación de los estatutos sociales en lo que afecte a esa reducción de capital. (Art. 317 TRLSC)

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación del acuerdo de reducción de capital de una SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación del acuerdo de reducción de capital de una SL” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdo-reduccion-capital-sl-mer-0034`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] Nº (9 veces)
- [ ] IMPORTE (7 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] PUNTO DEL ORDEN DEL DÍA (4 veces)
- [ ] DIRECCIÓN (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] LUGAR (2 veces)
- [ ] NIF (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] CARGO
- [ ] DNI/NIE
- [ ] FINALIDAD DE LA REDUCCIÓN
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

Modelo de certificado de acta de Junta General (Extraordinaria o Universal) de Socios de una Sociedad de Responsabilidad Limitada en la que se acuerda la reducción de capital mediante la disminución del valor nominal de las participaciones sociales, su amortización o su agrupación, con la finalidad de restablecer el equilibrio entre el capital y el patrimonio neto de la sociedad disminuido por consecuencia de pérdidas, la constitución o el incremento de la reserva legal o de las reservas voluntarias o la devolución del valor de las aportaciones. Incluye también el acuerdo de modificación de los estatutos sociales en lo que afecte a esa reducción de capital. (Art. 317 TRLSC)


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

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] en mi calidad de [ELEGIR: administrador único / administrador solidario / administradores mancomunados / Secretario del Consejo de Administración] de ‘[DENOMINACIÓN SOCIAL], S.L.’ y de su Junta de socios reunida el pasado

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] en mi calidad de [ELEGIR: liquidador único / liquidador solidario / liquidadores mancomunados / Secretario del Consejo de Liquidación] de ‘[DENOMINACIÓN SOCIAL], S.L.’ y de su Junta de socios reunida el pasado

CERTIFICO

- Que en [DIRECCIÓN], domicilio social de SL con fecha de ", se celebró Junta General Universal de socios de la entidad.
- Que en la junta estuvo, presente la totalidad del capital social, todo él con derecho a voto, y
- Que todos los asistentes firmaron en el acta, bajo su nombre respectivo, aceptando la constitución de la Junta con carácter de universal y con el siguiente

ORDEN DEL DÍA

[OPCIONAL — incluir si procede]

1.- Reducir el capital social para devolver aportaciones a los socios por cualquier procedimiento y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1. Reducir el capital social para compensar pérdidas, por cualquier procedimiento y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1. Reducir el capital social para constituir aumentar la reserva legal- voluntaria, por cualquier procedimiento y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1.- Reducir el capital social por el procedimiento de amortizar participaciones sociales propias y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

- Que, conforme a las disposiciones legales y estatutarias, se designaron los cargos de Presidente y Secretario de la reunión.

- Que se confeccionó por escrito la lista de asistentes, la cual obra al comienzo del acta.

- Que la Junta adoptó, por unanimidad, los acuerdos que se transcriben literalmente a continuación:

ACUERDOS

Primero. Reducción de capital social.

a) Cuantía y finalidad de la Reducción

Reducir el capital social de la entidad en la cifra de [IMPORTE] euros, con la finalidad de [FINALIDAD DE LA REDUCCIÓN]
devolver aportaciones a los socios
restablecer el equilibrio entre el capital y el patrimonio contable disminuido por pérdidas
constituir/aumentar la reserva- legal- voluntaria
amortizar participaciones sociales propias

b) Procedimiento

[OPCIONAL — incluir si procede]

Para restitución de aportaciones, compensación de pérdidas y constitución o aumento de reservas legales y voluntarias

[ELEGIR UNA OPCIÓN: Mediante reducción del valor nominal / Mediante amortización de participaciones / Mediante agrupación de participaciones]

[OPCIONAL — incluir si procede]

(Para restitución de aportaciones)

- Que los Estatutos sociales reconocen a los acreedores derecho de oposición al acuerdo de reducción.

- Que a efectos del ejercicio del citado derecho

[ELEGIR UNA OPCIÓN: Notificación personal / Acuerdo publicado en el BORME y en la página web de la sociedad]

- Que ningún acreedor ha ejercitado en plazo su derecho de oposición.

[OPCIONAL — incluir si procede]

Si hay oposición

- Que únicamente han ejercitado en plazo su derecho de oposición los siguientes acreedores:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD], y DNI [DNI/NIE], titular de un crédito contra la sociedad por importe de [IMPORTE] euros.

A D./Dña. [NOMBRE Y APELLIDOS] se le ha garantizado su crédito a su entera satisfacción

Dicho crédito ha sido abonado por la sociedad, antes de este acto.

- Que la reducción se efectúa restituyendo a los socios un total de [IMPORTE] euros la cual se hará efectiva en la misma proporción en que han sufrido la reducción, de la siguiente forma:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN], y con DNI/NIF [NIF] titular de [Nº] participaciones sociales, números [Nº] a [Nº], ambas inclusive, recibe la cantidad de [IMPORTE] euros en efectivo,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino/a de [LOCALIDAD] con domicilio en la [DIRECCIÓN], y con DNI/NIF [NIF] titular de [Nº] participaciones sociales, números [Nº] a [Nº], ambas inclusive, recibe la adjudicación no dineraria: que se entrega en pleno dominio, y libre de toda carga, gravamen, o arrendamiento

A los efectos de lo establecido en el art. 332 de la Ley de Sociedades de Capital se acuerda constituir una reserva con cargo a beneficios o reservas libres y por un importe igual al percibido por los socios en concepto de restitución de aportaciones, la cual tendrá carácter de indisponible en los términos legalmente previstos.

[OPCIONAL — incluir si procede]

Para compensación de pérdidas y constitución o aumento de reservas legales y voluntarias

[ELEGIR UNA OPCIÓN: Con balance ad hoc / Con otro balance]

[OPCIONAL — incluir si procede]

(Para amortización de participaciones propias)

Amortizar la participaciones números [Nº] a [Nº], con un valor nominal global de [IMPORTE] euros.

[OPCIONAL — incluir si procede]

Adquiridas por la sociedad bajo los supuestos legalmente previstos.

[OPCIONAL — incluir si procede]

Adquiridas por la sociedad dentro de un patrimonio obtenido a título universal.

[OPCIONAL — incluir si procede]

Adquiridas por la sociedad a título gratuito.

[OPCIONAL — incluir si procede]

Adquiridas por la sociedad por adjudicación judicial para pagar un crédito de la sociedad contra su titular.

[OPCIONAL — incluir si procede]

Adquiridas por la sociedad en el caso de adquisición forzosa previsto en el art.109.3 de la Ley de Sociedades de Capital

[OPCIONAL — incluir si procede]

Adquiridas por la sociedad con autorización expresa de la Junta General, con cargo a [ELEGIR: beneficios / reservas de libre disposición] y con la finalidad de:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Obtener las participaciones de un socio separado o excluido

Obtener las participaciones como consecuencia de la aplicación de una cláusula restrictiva de las mismas

Obtener las participaciones transmitidas mortis causa.

Puesto que la amortización no comporta devolución de aportaciones a los socios, se decide dotar la 'Reserva ' por el importe del valor nominal de las participaciones amortizadas, reserva que será indisponible hasta que transcurran 5 años desde la publicación de la reducción, salvo que antes del vencimiento de dicho plazo hayan sido satisfechas todas las deudas sociales contraídas con anterioridad a la fecha en que la reducción sea oponible a terceros.

Segundo. Modificación de Estatutos

Se acuerda por unanimidad modificar el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"Art [Nº DE ARTÍCULO] El capital de la sociedad es de [IMPORTE] euros y está representado por [ÓRGANO O PERSONA] participaciones, de valor nominal [IMPORTE] euros cada una de ellas, numeradas correlativamente del 1 al [Nº], ambos inclusive. Todas las participaciones confieren los mismos derechos y obligaciones y están totalmente desembolsadas en el 100% de su valor nominal’.

Tercero. Elevación a público

Se faculta a D./Dña. [NOMBRE Y APELLIDOS], en su calidad de [CARGO] para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando para ello las escrituras correspondientes, incluidas, en su caso, las de subsanación, aclaración o rectificación, así como para realizar cuantas operaciones fueren precisas para la plena eficacia de dichos acuerdos.

- Que el acta fue aprobada por la propia Junta, así como firmada por el Secretario con el Visto Bueno del Presidente, todo ello al término de la reunión.

Y, para que conste y surta los oportunos efectos, se expide la presente certificación- con el Visto Bueno del Presidente D./Dña. [NOMBRE Y APELLIDOS].

En [LUGAR], a [FECHA].

Secretario

Vº Bº Presidente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

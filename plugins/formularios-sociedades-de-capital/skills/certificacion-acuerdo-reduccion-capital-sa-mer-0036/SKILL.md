---
name: certificacion-acuerdo-reduccion-capital-sa-mer-0036
description: "Certificación del acuerdo de reducción de capital de una SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación del acuerdo de reducción de capital de una SA

> Formulario **MER-0036** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de certificado de acta de Junta General de Socios de una Sociedad Anónima en la que se acuerda la reducción de capital mediante la disminución del valor nominal de las acciones sociales, su amortización o su agrupación, con la finalidad de restablecer el equilibrio entre el capital y el patrimonio neto de la sociedad disminuido por consecuencia de pérdidas, la constitución o el incremento de la reserva legal o de las reservas voluntarias o la devolución del valor de las aportaciones. Incluye también el acuerdo de modificación de los estatutos sociales en lo que afecte a esa reducción de capital. (Art. 317 TRLSC)

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación del acuerdo de reducción de capital de una SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación del acuerdo de reducción de capital de una SA” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdo-reduccion-capital-sa-mer-0036`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (47 veces)
- [ ] Nº (25 veces)
- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] PLAZO (7 veces)
- [ ] PUNTO DEL ORDEN DEL DÍA (6 veces)
- [ ] FECHA (5 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] LUGAR (2 veces)
- [ ] CAUSA
- [ ] DATOS REGISTRALES
- [ ] DIRECCIÓN
- [ ] LOCALIDAD
- [ ] MEDIO DE PAGO
- [ ] Nº DE ACCIONES
- [ ] Nº DE ARTÍCULO
- [ ] OTROS DATOS
- [ ] TIPO DE RESERVA

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

Modelo de certificado de acta de Junta General de Socios de una Sociedad Anónima en la que se acuerda la reducción de capital mediante la disminución del valor nominal de las acciones sociales, su amortización o su agrupación, con la finalidad de restablecer el equilibrio entre el capital y el patrimonio neto de la sociedad disminuido por consecuencia de pérdidas, la constitución o el incremento de la reserva legal o de las reservas voluntarias o la devolución del valor de las aportaciones. Incluye también el acuerdo de modificación de los estatutos sociales en lo que afecte a esa reducción de capital. (Art. 317 TRLSC)


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

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de [ELEGIR: Administrador único / Administrador solidario / Administradores mancomunados / Secretario del Consejo de Administración] de ‘[DENOMINACIÓN SOCIAL], S.A.’ y de su Junta de socios reunida el pasado

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de [ELEGIR: Liquidador único / Liquidador solidario / Liquidadores mancomunados / Secretario del Consejo de Liquidación] de ‘[DENOMINACIÓN SOCIAL], S.A.’ y de su Junta de socios reunida el pasado

CERTIFICO

- Que en [DIRECCIÓN], el domicilio social de [DENOMINACIÓN SOCIAL] SA con fecha de ", se celebró Junta General Universal de accionistas de la entidad.
- Que en la junta estuvo, presente la totalidad del capital social, todo él con derecho a voto, y
- Que todos los asistentes firmaron en el acta, bajo su nombre respectivo, su aceptación a la constitución de la Junta con carácter de universal con el siguiente

ORDEN DEL DÍA

[OPCIONAL — incluir si procede]

1.- Reducir el capital social con la finalidad de devolver aportaciones y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1º) Reducir el capital social con la finalidad de amortizar acciones rescatables y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1.- Reducir el capital social con la finalidad de amortizar las acciones pertenecientes a accionistas morosos en el pago de desembolsos pendientes y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1.- Reducir el capital social con la finalidad de condonar los desembolsos pendientes, por el importe del valor nominal de las acciones pendientes de desembolso y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1.- Reducir el capital social con la finalidad de incrementar las reservas y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1. Reducir el capital social con la finalidad de restablecer el equilibrio entre el capital y el patrimonio neto de la sociedad disminuido por consecuencia de pérdidas y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

- Que conforme a las disposiciones legales y estatutarias, se designaron los cargos de Presidente y Secretario de la reunión.
- Que se confeccionó por escrito la lista de asistentes, la cual obra al comienzo del acta.
- Que la Junta adoptó, por [ELEGIR: unanimidad / mayoría], los acuerdos que se transcriben literalmente a continuación:

ACUERDOS

Primero.- Reducción de capital

[OPCIONAL — incluir si procede]

(Devolución de aportaciones a los socios)

Se reduce el capital en la cantidad de [IMPORTE] euros. Por lo tanto el capital social quedará fijado en [IMPORTE] euros.

Finalidad de la Reducción

Es devolución de aportaciones a los socios

Procedimiento

La reducción se efectúa mediante el procedimiento de disminuir el valor nominal de todas y cada una de las acciones que integran el capital social, en la cantidad de [IMPORTE] euros por acción quedando el valor final de cada acción en [IMPORTE] euros

Pago:

Como consecuencia de la reducción de capital social se abonará a los accionistas la suma global de [IMPORTE] euros

Dicha cantidad se distribuirá entre los accionistas en la misma proporción en que han sufrido la reducción.

Plazo de ejecución y desembolso

El plazo para la ejecución de la reducción del capital social es de [PLAZO] a partir de la adopción del presente acuerdo, mediante el abono a los accionistas de las siguientes cantidades:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

a) D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] acciones, con los números [Nº] a [Nº], ambos inclusive, se le entrega en efectivo de la suma de [IMPORTE] euros, equivalentes a [IMPORTE] euros por acción.

Oferta de compra:

La oferta será publicada en el BORM y en un periódico de gran circulación en la provincia donde radica el domicilio social, manteniéndose hasta el [FECHA]

En caso de no alcanzar las acciones ofrecidas el número mínimo fijado, se entenderá que el capital queda reducido en la cuantía correspondiente a las acciones que efectivamente sean adquiridas

[OPCIONAL — incluir si procede]

(Amortización de acciones rescatables)

Se reduce el capital en la suma de [IMPORTE] euros. Por lo tanto el capital social quedará fijado en [IMPORTE] euros.

Finalidad de la Reducción:

Es la amortización de las acciones rescatables.

Procedimiento:

La reducción del capital se llevará a cabo mediante la amortización de las acciones rescatables y la restitución de aportaciones.

Plazo de ejecución y desembolso:

El plazo para la ejecución de la reducción del capital social es de [PLAZO] a partir de la adopción del presente acuerdo, mediante el abono a los accionistas de las siguientes cantidades:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] acciones, con los números [Nº] a [Nº], ambos inclusive, se le entrega en efectivo de la suma de [IMPORTE] euros, equivalentes a [IMPORTE] euros por acción.

[OPCIONAL — incluir si procede]

(Exclusión de accionista moroso)

Se reduce el capital en la suma de [IMPORTE] euros. Por lo tanto, el capital social quedará fijado en [IMPORTE] euros.

Finalidad de la Reducción::

Es la amortización de las acciones pertenecientes a accionistas morosos en el pago de los desembolsos pendientes.

Procedimiento:

La reducción del capital social tendrá lugar mediante la amortización de las acciones afectadas por la mora.

Plazo de ejecución y desembolso:

El plazo para la ejecución de la reducción del capital social es de [PLAZO] a partir de la adopción del presente acuerdo, afectando a los siguientes accionistas morosos:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], titular [Nº] acciones, con los números [Nº] a [Nº]

Efectuada la amortización de las acciones afectadas por la mora, quedará en beneficio de la sociedad las cantidades recibidas por aquélla a cuenta de la acción.

[OPCIONAL — incluir si procede]

(Condonación de desembolsos pendientes)

Se reduce el capital en la suma de [IMPORTE] euros. Por lo tanto el capital social quedará fijado en [IMPORTE] euros.

Finalidad de la Reducción:

Es la condonación de los desembolsos pendientes, por el importe del valor nominal de las acciones no desembolsadas

Procedimiento:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

La reducción se efectuará mediante la disminución del valor nominal de todas las acciones que lo integran en [IMPORTE] euros por acción, que pasan a tener un valor nominal de [IMPORTE] euros cada una de ellas, amortizándose así la cantidad de [IMPORTE] euros por acción.

La reducción se efectuará mediante la amortización de [Nº] acciones propias, para lo cual se ofrece a todos los accionistas la adquisición de acciones de la sociedad por un precio de [IMPORTE] euros por acción, que se pagarán [MEDIO DE PAGO], realizándose el pago con cargo a [OTROS DATOS] y afectará a todas las acciones por igual.

Oferta de compra:

Será publicada en el BORM y en un periódico de gran circulación en la provincia donde radica el domicilio social, manteniéndose hasta el [FECHA]

En caso de no alcanzar las acciones ofrecidas el número mínimo fijado, se entenderá que el capital queda reducido en la cuantía correspondiente a las acciones que efectivamente sean adquiridas

La reducción se efectuará mediante la agrupación de [Nº] acciones para su canje por [Nº] nuevas acciones de [IMPORTE] euros de valor nominal cada una de ellas.

Oferta de compra

Será publicada en el BORM y en un periódico de gran circulación en la provincia donde radica el domicilio social, manteniéndose hasta el [FECHA]

En caso de no alcanzar las acciones ofrecidas el número mínimo fijado, se entenderá que el capital queda reducido en la cuantía correspondiente a las acciones que efectivamente sean adquiridas

Plazo de ejecución y desembolso:

El plazo para la ejecución de la reducción del capital social es de [PLAZO] a partir de la adopción del presente acuerdo, mediante el abono a los accionistas con acciones íntegramente desembolsadas de las siguientes cantidades:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], titular [Nº] acciones, con los números [Nº] a [Nº], ambos inclusive, se le entrega en efectivo de la suma de [IMPORTE] euros, equivalentes a [IMPORTE] euros por acción.

Y mediante la condonación a los accionistas con acciones no desembolsadas íntegramente de las siguientes cantidades:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], titular [Nº DE ACCIONES], acciones, con los números [Nº] a, ambos inclusive, la entrega en efectivo de la suma de [IMPORTE] euros, equivalentes a [IMPORTE] euros por acción.

[OPCIONAL — incluir si procede]

(Reservas)

Se reduce el capital en la suma de [IMPORTE] euros. Por lo tanto el capital social quedará fijado en [IMPORTE] euros.

Finalidad de la Reducción:

Es el incremento de la reserva [TIPO DE RESERVA]

Procedimiento:

La reducción se efectuará mediante la disminución del valor nominal de todas las acciones que lo integran en [IMPORTE] euros por acción, que pasan a tener un valor nominal de [IMPORTE] euros cada una de ellas, amortizándose así la cantidad de [IMPORTE] euros por acción.

Plazo de ejecución y desembolso:

El plazo para la ejecución de la reducción del capital social es de [PLAZO] a partir de la adopción del presente acuerdo, mediante el abono a los accionistas de las siguientes cantidades:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], titular [Nº] acciones, con los números [Nº] a, ambos inclusive, se le entrega en efectivo de la suma de [IMPORTE] euros, equivalentes a [IMPORTE] euros por acción.

[OPCIONAL — incluir si procede]

(Restablecimiento del equilibrio entre el capital y el patrimonio neto de la sociedad disminuido por consecuencia de pérdidas)

Se reduce el capital en la suma de [IMPORTE] euros. Por lo tanto el capital social quedará fijado en [IMPORTE] euros.

Finalidad de la Reducción:

Es el restablecimiento del equilibrio entre el capital y el patrimonio neto de la sociedad disminuido por consecuencia de pérdidas.

Procedimiento:

La reducción se efectuará mediante la disminución del valor nominal de todas las acciones que lo integran en [IMPORTE] euros por acción, que pasan a tener un valor nominal de [IMPORTE] euros cada una de ellas, amortizándose así la cantidad de [IMPORTE] euros por acción.

Plazo de ejecución y desembolso:

El plazo para la ejecución de la reducción del capital social es de [PLAZO] a partir de la adopción del presente acuerdo, mediante el abono a los accionistas de las siguientes cantidades:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], titular [Nº] acciones, con los números [Nº] a [Nº], ambos inclusive, se le entrega en efectivo de la suma de [IMPORTE] euros, equivalentes a [IMPORTE] euros por acción.

Con aportaciones no dinerarias

[OPCIONAL — incluir si procede]

Se reduce el capital en la suma de [IMPORTE] euros. Por lo tanto, el capital social quedará fijado en [IMPORTE] euros.

Finalidad de la Reducción:

Es la devolución de aportaciones no dinerarias, que tiene su causa en [CAUSA]

Procedimiento:

La reducción se efectuará mediante la disminución del valor nominal de todas las acciones que lo integran en [IMPORTE] euros por acción, que pasan a tener un valor nominal de [IMPORTE] euros cada una de ellas, amortizándose así la cantidad de [IMPORTE] euros por acción.

Concretamente se proyecta la devolución de las siguientes aportaciones.

a) D./Dña. [NOMBRE Y APELLIDOS] del inmueble sito en [LOCALIDAD], cuya descripción registral es [DATOS REGISTRALES], valorada en [IMPORTE] euros ( €), y cuya aportación efectiva se realizó en la Escritura de Constitución. La memoria explicativa e informe técnico sobre la valoración del citado inmueble se hallan a disposición de los accionistas.

Plazo de ejecución y desembolso:

El plazo para la ejecución de la reducción del capital social es de [PLAZO] a partir de la adopción del presente acuerdo, mediante el abono a los accionistas de las siguientes cantidades:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

a) D./Dña. [NOMBRE Y APELLIDOS] titular [Nº] acciones, con los números [Nº] a [Nº], ambos inclusive, se le entrega en efectivo de la suma de [IMPORTE] euros, equivalentes a [IMPORTE] euros por acción.

Segundo.- Modificación de los Estatutos

Como consecuencia del acuerdo de reducción de capital suscrito, se conviene modificar el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"El capital de la sociedad es de [IMPORTE] euros y está representado poracciones nominativas, de valor nominal euros cada una de ellas, numeradas correlativamente del 1 al [Nº], ambos inclusive. Todas las acciones son de una sola serie, confieren los mismos derechos y obligaciones y están totalmente desembolsadas en el 100% de su valor nominal".

Tercero.- Elevación a público

Se facultò a D./Dña. [ELEGIR: Administrador único / Administrador solidario / Administradores mancomunados / Secretario del Consejo de Administración] para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando para ello las escrituras correspondientes, incluidas, en su caso, las de subsanación, aclaración o rectificación, así como para realizar cuantas operaciones fueren precisas para la plena eficacia de dichos acuerdos.

Se hace constar que la aprobación del acuerdo señalado se ha realizado con el voto favorable de todo el capital social con derecho a voto.

- Que el acta fue aprobada por la propia Junta, así como firmada por el Secretario con el Visto Bueno del Presidente, todo ello al término de la reunión.

Y, para que conste y surta los oportunos efectos, se expide la presente certificación- con el Visto Bueno del Presidente D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

Secretario

Vº Bº Presidente Secretario

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

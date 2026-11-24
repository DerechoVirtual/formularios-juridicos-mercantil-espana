---
name: acta-junta-general-sa-acuerda-emitir-obligaciones-mer-0287
description: "Acta de junta general de una SA que acuerda emitir obligaciones convertibles o no convertibles. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de junta general de una SA que acuerda emitir obligaciones convertibles o no convertibles

> Formulario **MER-0287** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de acuerdo de una Junta General de Accionistas de una Sociedad Anónima, ordinaria o extraordinaria, mediante la cuál se adopta un acuerdo de emisión de obligaciones en acciones y no convertibles [OTROS DATOS], determinando en el mismo las condiciones necesarias para su establecimiento y cumplimiento.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de junta general de una SA que acuerda emitir obligaciones convertibles o no convertibles» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de junta general de una SA que acuerda emitir obligaciones convertibles o no convertibles” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-junta-general-sa-acuerda-emitir-obligaciones-mer-0287`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (7 veces)
- [ ] FECHA (6 veces)
- [ ] PORCENTAJE (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] ACCIONISTAS CON DERECHO DE SUSCRIPCIÓN
- [ ] DESCRIPCIÓN DE LA GARANTÍA
- [ ] FORMA Y PLAZO DE AMORTIZACIÓN
- [ ] INTERVENCIONES DE LOS ASISTENTES
- [ ] LUGAR DE PAGO
- [ ] NOMBRE DEL PERIÓDICO
- [ ] Nº DE ARTÍCULO
- [ ] NÚMERO
- [ ] PERIODICIDAD
- [ ] UNANIMIDAD O MAYORÍA

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

Modelo de acuerdo de una Junta General de Accionistas de una Sociedad Anónima, ordinaria o extraordinaria, mediante la cuál se adopta un acuerdo de emisión de obligaciones en acciones y no convertibles [OTROS DATOS], determinando en el mismo las condiciones necesarias para su establecimiento y cumplimiento.


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

Acta de la Junta General de accionistas de la Sociedad Anónima [DENOMINACIÓN SOCIAL]

En [LOCALIDAD], a [FECHA], siendo las [Nº] horas y en el domicilio social de la sociedad [DENOMINACIÓN SOCIAL] sito en [LOCALIDAD]

Se celebra la presente Junta, cuya convocatoria fue efectuada mediante anuncios publicados en el ‘Boletín Oficial del Registro Mercantil’ número [NÚMERO] de fecha [FECHA] y en la página web de la sociedad

[OPCIONAL — incluir si procede]

Supuesto que no haya otro medio

En el periódico diario ‘ [NOMBRE DEL PERIÓDICO] ‘ de [LOCALIDAD] de fecha [FECHA], con el siguiente contenido:

Se procede a elaborar la lista de asistentes

Concurren [Nº] socios con derecho de voto, que representan un [PORCENTAJE] % del capital social, de los cuales [Nº] accionistas asisten personalmente, representando el [PORCENTAJE] % del capital social, y [Nº] accionistas lo hacen debidamente representados, suponiendo a su vez un [PORCENTAJE] % del capital.

Actúa como Presidente de la Junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario de la misma D./Dña. [NOMBRE Y APELLIDOS], en su calidad de Presidente y Secretario del Consejo de Administración respectivamente, y en ejercicio de las funciones que en tal sentido les atribuye el artículo [Nº DE ARTÍCULO] de los estatutos sociales.

Hallándose presente el citado capital, se procede a la declaración por el Presidente de la válida constitución de la Junta en [ELEGIR: primera convocatoria / segunda convocatoria] seguido lo cual el Secretario da paso a la lectura del Orden del Día fijado en la convocatoria.

Se procede al debate de los asuntos contenidos en el Orden del Día y se aluden los siguientes aspectos con las siguientes intervenciones [INTERVENCIONES DE LOS ASISTENTES]

No solicitándose por ninguno de los accionistas la palabra y no habiendo más asuntos que tratar, el Presidente da por concluido el debate y suspende momentáneamente la sesión para la redacción por el Secretario de la presente Acta, en la cual queda reflejada la adocpión de los siguientes ACUERDOS:

Primero.-

Segundo.- Emitir un préstamo por valor de [IMPORTE] euros, con sujeción a lo previsto en las siguientes Condiciones:

I.- El préstamo será materializado por [Nº] obligaciones representadas mediante [ELEGIR: títulos nominativos / títulos al portador / anotaciones en cuenta] convertibles en acciones, de [IMPORTE] euros de valor nominal cada una de ellas, y agrupadas en única serie numerada de manera correlativa del uno al

II.- La suscripción se realizará, una vez inscrita en los Registros correspondientes la oportuna escritura pública de emisión, en el plazo comprendido entre el [FECHA] y el [FECHA], y podrá realizarse en
la entidad financiera
el domicilio social

[OPCIONAL — incluir si procede]

(Obligaciones convertibles)

II.- La suscripción se realizará, una vez inscrita en los Registros correspondientes la oportuna escritura pública de emisión, en el plazo comprendido entre el y el [FECHA] para los accionistas [ACCIONISTAS CON DERECHO DE SUSCRIPCIÓN], en el ejercicio de su derecho de suscripción preferente de [Nº] obligaciones por cada
acción
obligación convertible
  Transcurrido dicho plazo las obligaciones así no suscritas podrán ser ofrecidas en suscripción pública durante el período comprendido entre el y el .En ambos casos la suscripción podrá realizarse en [ELEGIR: la entidad financiera / el domicilio social]

III.- La suscripción se efectuará por el valor nominal de los títulos respectivos [OTROS DATOS].

IV.- Las obligaciones que se suscriban darán derecho a la percepción de un interés del [PORCENTAJE] % anual que se abonarán por [PERIODICIDAD] vencidos.

[OPCIONAL — incluir si procede]

(No convertibles)

V.- La amortización se efectuará [FORMA Y PLAZO DE AMORTIZACIÓN]

.- Los pagos correspondientes a los intereses vencidos y a las amortizaciones de las obligaciones suscritas se realizarán en [LUGAR DE PAGO]

[OPCIONAL — incluir si procede]

En caso de que se trate de emisión garantizada

.- La emisión de obligaciones que se acuerda será garantizada por medio de [DESCRIPCIÓN DE LA GARANTÍA].

[OPCIONAL — incluir si procede]

.- Se reconoce el derecho de los obligacionistas a solicitar la conversión de sus obligaciones en acciones en cualquier momento dentro del plazo máximo de según las siguientes bases de conversión: Dicha conversión dará lugar al aumento del capital social en la cuantía correspondiente a las obligaciones convertidas.

.- La falta de conversión de alguna o algunas de las obligaciones emitidas dará lugar a su amortización, que se efectuará

.- El Consejo de Administración queda encargado de la designación del primer Comisario del Sindicato de Obligacionistas y de la elaboración de las normas provisionales del mismo hasta que ambos sean ratificados, modificados o sustituidos por las decisiones que adopte la Asamblea de Obligacionistas.

.- Igualmente queda encargado el Consejo de Administración del cumplimiento de cuantos actos sean necesarios para la ejecución del presente acuerdo de emisión de obligaciones y de aquellos otros que vengan exigidos por la legislación aplicable, en concreto en lo referente a las normas previstas en la Ley del Mercado de Valores.

El presente acuerdo se aprueba con el voto favorable del [PORCENTAJE] % del capital presente y/o representado. [OTROS DATOS].

Una vez redactada el Acta y leída íntegramente por el Secretario, se somete a la aprobación de los asistentes, que la aprueban por [UNANIMIDAD O MAYORÍA], por encontrarla conforme a lo debatido y acordado.

Acto seguido, se levanta la sesión, siendo las [Nº] horas del día señalado en el encabezamiento, procediéndose a la firma de la presente por mí, el Secretario, con el Visto Bueno del Presidente.

D./Dña. [NOMBRE Y APELLIDOS]

El Secretario:

D./Dña. [NOMBRE Y APELLIDOS]

Vº.Bº, el Presidente,

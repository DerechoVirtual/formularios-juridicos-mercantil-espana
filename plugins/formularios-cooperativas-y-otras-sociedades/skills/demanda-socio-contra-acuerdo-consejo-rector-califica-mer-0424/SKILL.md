---
name: demanda-socio-contra-acuerdo-consejo-rector-califica-mer-0424
description: "Demanda del socio contra el acuerdo del consejo rector que califica su baja en la cooperativa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del socio contra el acuerdo del consejo rector que califica su baja en la cooperativa

> Formulario **MER-0424** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de impugnación del acuerdo del consejo rector de una sociedad cooperativa en el que se establece la calificación y los efectos de la baja voluntaria de un socio cooperativista.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del socio contra el acuerdo del consejo rector que califica su baja en la cooperativa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del socio contra el acuerdo del consejo rector que califica su baja en la cooperativa” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:demanda-socio-contra-acuerdo-consejo-rector-califica-mer-0424`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] MOTIVO (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] EJERCICIO
- [ ] EXPONER LOS HECHOS
- [ ] FUNDAMENTOS
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] SEDE

## Normas que cita el formulario

- art. 52.1.r LEC
- art. 249.1.3 LEC
- art. 18 Ley 27/1999
- art. 51 Ley 27/1999
- art. 253 LEC

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

Modelo de demanda de impugnación del acuerdo del consejo rector de una sociedad cooperativa en el que se establece la calificación y los efectos de la baja voluntaria de un socio cooperativista.


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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según acredito mediante escritura de poder que acompaño para su unión a los autos por copia testimoniada cuya devolución del original desde este momento intereso por precisarlo para otros usos, dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal de instancia comparezco y como mejor proceda en Derecho

DIGO:

Que, en la representación que ostento, interpongo demanda de juicio declarativo ordinario, sobre IMPUGNACIÓN DE ACUERDOS SOCIALES frente a la mercantil ‘[DENOMINACIÓN SOCIAL], S.Coop.’ [DENOMINACIÓN SOCIAL], con domicilio en

A efectos del primer emplazamiento del demandado, para el caso de que no sea hallado en dicho domicilio, se designan los siguientes lugares donde podrá intentarse la comunicación, por el siguiente orden:

Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

Primero.- Mi representado, [NOMBRE Y APELLIDOS] ha venido ostentado la condición de socio de ‘[DENOMINACIÓN SOCIAL], S. Coop.’, según acredito con copia del Libro Registro de Socios de la Cooperativa citada, que acompaño con documento número 1 de los que se unen a la presente demanda.

Segundo.- Con fecha [FECHA], mi mandante solicitó su baja voluntaria ante el Consejo Rector de ‘[DENOMINACIÓN SOCIAL], S.Coop.’, habiendo cumplido con el preceptivo plazo de preaviso previsto en el art. de sus Estatutos Sociales, por el siguiente motivo [MOTIVO]. Acredito dicha circunstancia con el original del burofax por el que se efectuó dicha solicitud. (Documento nº 2)

Tercero.- Con fecha [FECHA] mi representado recibió notificación del Acuerdo del Consejo Rector por el que se aceptaba su baja voluntaria, calificándose ésta como justificada, y posteriormente el [FECHA] otro acuerdo del mismo órgano estableciendo una liquidación que ascendía a la cantidad de [IMPORTE] euros en concepto del derecho al reembolso por sus participaciones sociales calculado según el balance de cierre del ejercicio en el que se causaba la baja. (Documento nº 3)

Cuarto.- Considerando injustificada la citada cantidad, puesto que [MOTIVO], mi defendido formuló en plazo el oportuno RECURSO DE IMPUGNACIÓN del citado Acuerdo del Consejo Rector previsto en el artículo 51.2 en relación con el 17.5 y 18.3.c), todos ellos de la Ley 27/99, de 16 de julio, de Cooperativas, solicitando que dicho recurso fuera admitido y resuelto, acordando un derecho de reembolso de [IMPORTE] euros por sus participaciones en el capital social de de ‘ S.Coop.’ (Documento nº 4)

Quinto.- Dicho recurso ha sido desestimado, según resolución al mismo notificada a mi representado el pasado día [FECHA] (Documento nº 5) [OTROS DATOS].

Sexto.- [EXPONER LOS HECHOS].

A los anteriores hechos, son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA: Corresponde a la Sección de lo Mercantil del Tribunal de Instancia al que me dirijo, en virtud de lo dispuesto en el art. 52.1.regla 10ª de la LEC de 7 de enero de 2000, puesto que la entidad demandada tiene su domicilio social en esta capital.

II.- PROCEDIMIENTO: Corresponde el del Juicio Ordinario según lo previsto en el art. 249.1.3º de la LEC de 7 de enero de 2000 y en el 31.5 de la Ley 27/99, de 16 de julio, de Cooperativas, en relación con el art. 118 de la Ley de Sociedades de Capital, a los que se remite el artículo 18.3 in fine de la Ley 27/199, a su vez aplicable por remisión del artículo 17.6 del mismo cuerpo legal.

III.- LEGITIMACION ACTIVA: Corresponde al demandante en su calidad de socio.

IV.- PLAZO: Se interpone la demanda dentro del plazo de un mes señalado en el apartado 3 del artículo 18 de la Ley 27/1999, de 16 de julio, de Cooperativas ‘ [OTROS DATOS], aplicable por remisión al mismo desde el apartado 6 del artículo 17 del citado texto, según el cual: ‘El socio disconforme con el acuerdo motivado del Consejo Rector, sobre la calificación y efectos de su baja podrá impugnarlo en los términos previstos en el apartado c) del punto 3 del artículo 18 de esta Ley’.

V.- FONDO DEL ASUNTO: El artículo 51 de la Ley 27/1999, de 16 de julio, de Cooperativas, regula el reembolso de las participaciones de los socios cooperativistas estableciendo que

VII.- CUANTÍA: Conforme al art. 253 de la LEC cifro la cuantía de la presente demanda en [IMPORTE], fijación que amparo en el siguiente fundamento [FUNDAMENTOS]

VIII.- COSTAS: Conforme al artículo 394 de la L.E.C., las costas han de imponerse a la demandada.

SUPLICO AL TRIBUNAL DE INSTANCIA. Que habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido en parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente a las personas designadas en el encabezamiento, dé al mismo el curso señalado en la ley y, en su día, dicte sentencia en la que, estimando íntegramente esta demanda de impugnación de acuerdo social:

A) Se califique como justificada a todos los efectos legales la baja de la actora como socio de ‘[DENOMINACIÓN SOCIAL], S.A.’
B) Se declarase mal hecha la propuesta de liquidación formulada por el Consejo Rector de la demandada con fecha [FECHA]
C) Se condene a la demandada a proceder al ajuste contable correcto a efectos de la liquidación y reembolso de las aportaciones de capital social de la actora, y
D) Se condene a la entidad demandada a liquidar y reembolsar las aportaciones de capital social de la actora de conformidad con las normas legales citadas al efecto, según el balance de cierre del ejercicio [EJERCICIO] en que la baja se causó, devengando las cantidades resultantes el interés que legalmente corresponda.
E) Condene a dicha Cooperativa en todas las costas y gastos de este procedimiento.

Es de Justicia que pido en [LUGAR], a [FECHA].

Abogado y número de colegiado:

Procurador

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

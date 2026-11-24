---
name: demanda-reclamacion-aportacion-no-devuelta-socio-tras-mer-0783
description: "Demanda de reclamación de la aportación no devuelta al socio tras reducir capital en una SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reclamación de la aportación no devuelta al socio tras reducir capital en una SL

> Formulario **MER-0783** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda por reclamación de cantidad, a una sociedad que ha acordado la reducción de capital y la devolución de aportaciones, pero no ha cumplido con el pago efectivo de la cantidad acordada a los socios. Esto puede deberse a diversas razones, como falta de liquidez, discrepancias en la valoración de las aportaciones, o incumplimiento de los plazos establecidos.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reclamación de la aportación no devuelta al socio tras reducir capital en una SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reclamación de la aportación no devuelta al socio tras reducir capital en una SL” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-reclamacion-aportacion-no-devuelta-socio-tras-mer-0783`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] FECHA (6 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DOMICILIO
- [ ] MES
- [ ] NIF
- [ ] NOMBRE DE LA PARTE
- [ ] Nº
- [ ] Nº DE PROTOCOLO
- [ ] OBJETO SOCIAL
- [ ] PARTE DEMANDADA
- [ ] SEDE
- [ ] TIPO DE ÓRGANO DE ADMINISTRACIÓN

## Normas que cita el formulario

- art. 51.1 LEC
- art. 6.1.1 LEC
- art. 6.1.3 LEC
- art. 7.1 LEC
- art. 10 LEC
- art. 251.1 LEC
- art. 317.1 TRLSC
- art. 202.3 TRLSC
- art. 576 LEC
- art. 394 LEC

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

Modelo de demanda por reclamación de cantidad, a una sociedad que ha acordado la reducción de capital y la devolución de aportaciones, pero no ha cumplido con el pago efectivo de la cantidad acordada a los socios. Esto puede deberse a diversas razones, como falta de liquidez, discrepancias en la valoración de las aportaciones, o incumplimiento de los plazos establecidos.


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

Don [NOMBRE Y APELLIDOS], provisto de D.N.I. nº [NÚMERO], vecino de [LOCALIDAD], con domicilio en [LOCALIDAD], bajo dirección del Letrado en ejercicio Don [NOMBRE Y APELLIDOS], colegiado del Iltre. Colegio de Abogados de [COLEGIO], y despacho abierto en [LOCALIDAD], ante el Tribunal comparezco y como mejor en Derecho proceda, DIGO:

Que por medio del presente escrito, y en nombre de mi representado, interpongo DEMANDA DE JUICIO VERBAL frente a la mercantil [DENOMINACIÓN SOCIAL], con NIF [NIF], y domicilio social en [LOCALIDAD], en reclamación de cantidad de [IMPORTE] euros, demanda que formulo sobre la base de los siguientes:

HECHOS

PRIMERO.- Mi representado es titular de [Nº] participaciones de la sociedad demandada.

Adjunto certificado de titularidad de las participaciones, como documento nº [Nº DE DOCUMENTO]

SEGUNDO.- La sociedad mercantil demandada [DENOMINACIÓN SOCIAL] fue constituida el [FECHA] de [MES] de [AÑO], mediante escritura autorizada el [FECHA] ante el notario de [LOCALIDAD] D. bajo el número de su protocolo [Nº DE PROTOCOLO]. Se acompaña como documento núm. copia de la misma con sello de registro.

El domicilio social de [DENOMINACIÓN SOCIAL] se encuentra en [DOMICILIO], según resulta de la escritura fundacional, manifestándose también que es el centro de sus intereses principales, dado que las oficinas centrales y desde ellas se administra la sociedad de forma permanente y pública.

El órgano de administración de la compañía es el [TIPO DE ÓRGANO DE ADMINISTRACIÓN].

Su objeto social es [OBJETO SOCIAL]. Se aporta título constitutivo y estatutos de la empresa como documento número [Nº DE DOCUMENTO] y número [NÚMERO].

TERCERO.- Mediante acuerdo adoptado por la Junta General de socios de la citada entidad, reunida el día [FECHA], se aprobó la reducción de capital social en la cuantía de [IMPORTE] euros con la finalidad de devolver parcialmente sus aportaciones a los socios, entre ellos, al demandante. El acuerdo se inscribió en el Registro Mercantil el [FECHA] y se publicó la inscripción en el BORME el día [FECHA].

Acompaño copia del acta de la Junta General en la que se acuerda la devolución de aportaciones a los socios a prorrata de sus participaciones, correspondiendo a mi representado la entrega de una cantidad líquida de dinero que asciende a [IMPORTE] euros (documento nº [Nº DE DOCUMENTO]).

CUARTO.- Aunque se expidió un cheque bancario para devolver al demandante la suma de [IMPORTE] euros, depositado en la Notaría [LOCALIDAD]; cantidad que esta parte reconoce haber recibido en fecha [FECHA] (documentos números [Nº DE DOCUMENTO]), lo cierto es que la deuda no ha sido satisfecha en su totalidad, puesto que la sociedad demandada sigue adeudando a mi representado la cantidad de [IMPORTE] euros y, por consiguiente, a fecha de interposición de esta demanda, la demandada aún no ha procedido a ejecutar la obligación derivada del acuerdo adoptado en la Junta.

QUINTO.- Se han intentado agotar todas las vías extrajudiciales de solución amistosa de la presente controversia, sin que la mercantil demandada haya atendido la reclamación efectuada mediante burofax, tal y como acreditamos acompañando el mismo al presente escrito como documento nº [Nº DE DOCUMENTO], por lo que nos vemos en la necesidad de acudir al auxilio judicial.

A los anteriores hechos le son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA.

El art. 51.1 LEC establece que las personas jurídicas serán demandadas en el lugar de su domicilio, que es esta localidad, en que la sociedad demandada tiene su domicilio social.

II.- PROCEDIMIENTO.

En aplicación de los arts. 248.3 y 250.2 LEC, y en atención a la cuantía del objeto litigioso, este pleito se tramitará por las normas de proceso declarativo llamado Juicio Verbal.

III.- CAPACIDAD.

Conforme al art. 6.1.1º LEC tienen capacidad para ser parte las personas físicas, y las jurídicas, como las sociedades mercantiles, conforme al art. 6.1.3º LEC, y a tenor del art. 7.1 y 4 LEC detentan capacidad de obrar procesal las personas físicas, en tanto que mayores de edad que no precisan medidas de apoyo para el ejercicio de su capacidad jurídica, y las sociedades, a través de quienes legalmente les representen, respectivamente.

IV.- LEGITIMACIÓN.

El art. 10 LEC legitima para comparecer y actuar en juicio a los titulares de la relación jurídica o del objeto litigioso. En el caso de autos, demandante y entidad demandada son los sujetos titulares de los derechos de crédito y correlativas obligaciones derivadas del acuerdo societario de reducción del capital, estando legitimados activamente los socios como titulares del derecho de reintegro de sus aportaciones frente a la sociedad demandada, que por ello se legitima pasivamente.

V.- POSTULACIÓN.

En aplicación de los arts. 23.1 y 31.1 LEC, las partes deberán comparecer representadas por Procurador de los Tribunales y asistidas por Letrado en ejercicio.

VI.- CUANTÍA.

De conformidad con lo dispuesto en el art.251.1ª LEC, la cuantía de la presente demanda se fija en la cantidad de [IMPORTE] euros, suma que se corresponde con la cantidad de dinero reclamada en concepto de principal.

VII.- FONDO DEL ASUNTO.

La reducción del capital social, por parte de la sociedad respectiva, puede ser voluntaria u obligatoria. La de la primera clase es la que tiene lugar cuando la sociedad, sin obligarle a ello ningún precepto legal, acuerda libremente la reducción (supuesto, como es obvio, el cumplimiento de los requisitos legales de convocatoria y constitución de la oportuna Junta con todos los requisitos legalmente exigidos para ello, lo que aquí no se cuestiona) cuando estime que es necesaria o conveniente para el cumplimiento de su objeto social, pudiendo dicha reducción tener por finalidad "la devolución del valor de las aportaciones" (art. 317.1 TRLSC).

Pues bien, producida dicha situación, el art. 202.3 TRLSC establece que los acuerdos sociales podrán ejecutarse a partir de la fecha de la aprobación del acta en la que consten, por lo que es posible exigir a la sociedad que lleve a cabo las obligaciones que se deriven de la adopción de dichos acuerdos.

VIII.- MORA.

La parte demandada ha incurrido en mora en el cumplimiento de su obligación y, por tanto, conforme a lo prevenido en los arts. 1.100, 1.101, 1.108 y 1.109 CC, debe condenarse a la demandada al pago del interés legal de la antedicha cantidad, [IMPORTE] euros, desde la fecha de interpelación judicial; y a partir del dictado de sentencia y hasta su completa satisfacción los intereses serán los que se contemplan en el art. 576 LEC.

IX- COSTAS.

De conformidad con lo dispuesto en el art.394 LEC, las costas de la primera instancia habrán de imponerse a la parte que haya visto rechazadas todas sus pretensiones, en virtud del principio objetivo de vencimiento.

Por lo expuesto,

SUPLICO AL TRIBUNAL: Que, teniendo por presentado este escrito, junto con sus copias y documentos adjuntos, se sirva admitirlos teniéndome por personado y parte en la representación acreditada de [NOMBRE DE LA PARTE] y, por formulada DEMANDA DE JUICIO VERBAL en reclamación de cantidad contra [PARTE DEMANDADA] y, previos los trámites legales, incluido el recibimiento del pleito a prueba que desde este momento dejo interesado, se dicte la correspondiente sentencia por la que estimando la demanda condene a la demandada a abonar al demandante la cantidad de [IMPORTE] euros, más los intereses devengados desde la interposición de la demanda hasta su definitivo pago, y todo ello con expresa imposición de las costas procesales a la parte demandada.

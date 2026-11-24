---
name: demanda-socio-contra-sociedad-ejercicio-accion-regreso-mer-0782
description: "Demanda del socio contra la sociedad en ejercicio de la acción de regreso (art. 331 LSC). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del socio contra la sociedad en ejercicio de la acción de regreso (art. 331 LSC)

> Formulario **MER-0782** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del socio contra la sociedad en ejercicio de la acción de regreso (art. 331 LSC)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del socio contra la sociedad en ejercicio de la acción de regreso (art. 331 LSC)” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-socio-contra-sociedad-ejercicio-accion-regreso-mer-0782`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (18 veces)
- [ ] DENOMINACIÓN SOCIAL (10 veces)
- [ ] IMPORTE (7 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] Nº (6 veces)
- [ ] NOMBRE DE LA PARTE (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] COLEGIO
- [ ] DATOS REGISTRALES
- [ ] FOLIO
- [ ] HOJA
- [ ] LUGAR
- [ ] NIF
- [ ] PORCENTAJE
- [ ] PORCENTAJE O IMPORTE DE LA REDUCCIÓN
- [ ] SEDE
- [ ] TOMO

## Normas que cita el formulario

- art. 331 TRLSC
- art. 331 LSC
- art. 51.1 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 253.1 LEC
- art. 249.2 LEC
- art. 23 LEC
- art. 399 LEC
- art. 332 TRLSC
- art. 333 TRLSC
- art. 1.145 CC
- art. 222 TRLC
- art. 1.145.2 CC
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

Se plantea demanda ejercitando acción de regreso del socio, prevista en el art. 331 TRLSC 2010, sobre el supuesto que puede darse con más frecuencia en la práctica. Consiste en un caso en que el socio reclama el pago de la sociedad, tras haber sido condenado solidariamente con ella (en una acción de reclamación contractual acumulada a la responsabilidad del art. 331 LSC), y haber tenido que pagar todo lo reclamado.

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales y de la entidad [DENOMINACIÓN SOCIAL], como acredito en virtud de escritura de poder que acepto y acompaño, y cuya devolución intereso por ser de carácter general y necesaria para otros usos, bajo la dirección letrada de D/Dña. [NOMBRE Y APELLIDOS], abogado/a ejerciente, n.º [NÚMERO] del Iltre. Colegio de abogados de [COLEGIO], con despacho abierto en [LOCALIDAD], ante el tribunal comparezco y como mejor proceda en Derecho,

DIGO:

Que, por medio del presente escrito procedo a interponer demanda de juicio ordinario, en la que ejercito la acción de regreso o repetición frente a la entidad [DENOMINACIÓN SOCIAL], con domicilio social en [LOCALIDAD].

Todo ello de acuerdo con los siguientes hechos y consideraciones de derecho:

HECHOS

Primero.- Mi mandante es socio, desde un inicio de la mercantil [DENOMINACIÓN SOCIAL], constituida el [FECHA], según consta en la escritura autorizada el día [FECHA] por D./D.ª [NOMBRE Y APELLIDOS], Notario de [LOCALIDAD], con domicilio social en [LOCALIDAD], e inscrita en el Registro Mercantil nº [NÚMERO] de [LOCALIDAD] en el [DATOS REGISTRALES], Tomo [TOMO], Folio [FOLIO], Hoja [HOJA], con CIF [NIF]. Ostentó la titularidad de participaciones sociales con números [Nº], ambos inclusive, con un valor de [IMPORTE] euros cada una, lo que hace un total de [IMPORTE] euros en total. Suma que fue desembolsada en fecha [FECHA].

Acredito estos extremos con el documento nº [Nº] de los que se acompañan a este escrito, consistente en copia simple de la escritura de constitución mencionada, así como con el documento nº [Nº], que recoge la certificación del Registro Mercantil donde constan los datos mencionados. Como documento nº [Nº DE DOCUMENTO] se aporta certificación del libro registro de socios, donde se hace constar la referida titularidad inicial de las participaciones sociales, y como documento nº extracto de la transferencia bancaria mediante la cual mi cliente aportó el valor íntegro de las participaciones que adquiría

Segundo.- En fecha [FECHA], se acordó en junta extraordinaria de socios, aprobada por unanimidad, reducir el capital de [DENOMINACIÓN SOCIAL], en un [PORCENTAJE O IMPORTE DE LA REDUCCIÓN]. El acuerdo fue inscrito en el Registro Mercantil el [FECHA], y publicado en el BOREM en fecha [FECHA], además de en la página web de la citada mercantil.

Como consecuencia de la reducción operada, a todos los socios, entre ellos a mi representado, se les devolvió [PORCENTAJE] de las cantidades inicialmente desembolsadas. En concreto, y por lo que respecta a mi cliente, se le devolvieron [IMPORTE] euros el [FECHA].

Se acompaña copia de escritura pública de reducción de capital como documento nº [Nº], certificación de su inscripción en el Registro Mercantil el [FECHA], como documento nº [Nº], y extracto de la transferencia bancaria de devolución, operada el [FECHA], como documento nº [Nº DE DOCUMENTO].

Tercero.- En fecha [FECHA], la entidad [DENOMINACIÓN SOCIAL] demandó a mi cliente ante el Tribunal de Instancia (Sección de lo Mercantil) nº [NÚMERO] de [LOCALIDAD], ejercitando la acción de responsabilidad de socios de sociedad limitada, prevista en el art. 331 TRLSC 2010, en reclamación de una deuda anterior a la reducción del capital social, que ostentaba contra la entidad [DENOMINACIÓN SOCIAL]. Dicha acción se ejercitaba de manera acumulada a la acción de responsabilidad contractual contra esta última sociedad. Los autos se tramitaron como Juicio Ordinario nº [NÚMERO], y en los mismos recayó sentencia de fecha [FECHA], en la que se estimó íntegramente la demanda y se condenó los demandados, de manera solidaria, a abonar a la actora la cantidad de [IMPORTE] euros. Frente a la misma, todos ellos, interpusieron recurso de apelación ante la Audiencia Provincial de [LOCALIDAD], que fue desestimado mediante sentencia dictada el [FECHA], que no fue recurrida.

Se aportan copias testimoniadas de ambas resoluciones, respectivamente, como documentos nºy. En la primera de ella se hace constar como hecho probado primero que «La entidadcontrató con la mercantil, en el año, la prestación de servicios de limpieza diarios, que se desarrollaron sin objeción por las partes. El coste del servicio contratado fue deeuros en cómputo anual, que se repartía en 12 mensualidades deeuros cada una; de los cualesha abonado la cantidad parcial deeuros».

En fecha [FECHA], mi cliente fue requerido extrajudicialmente de pago por el importe global de la condena, como paso previo a instar contra él la correspondiente demanda ejecutiva. Al día siguiente, el [FECHA], se realizó una transferencia bancaria por el importe reclamado, cuyo extracto se adjunta como documento nº [Nº DE DOCUMENTO].

Cuarto.- El pasado [FECHA], mi representado reclamó mediante correo certificado a la entidad [DENOMINACIÓN SOCIAL], a través del administrador social único, D/Dª. [NOMBRE Y APELLIDOS], la cantidad abonada como consecuencia de la sentencia condenatoria. En la comunicación se indicaba que mi cliente, como mero socio de la aquí demandada, no tuvo participación alguna en la generación de la deuda reclamada por [NOMBRE DE LA PARTE], lo cual resulta íntegramente imputable a aquella, o, en su caso, a su administrador social único. Se adjunta copia de dicho correo como documento nº [Nº], que no ha sido contestado hasta la fecha.

A los presentes hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

En cuanto a la competencia objetiva, se plantea la demanda ante la sección de lo Mercantil del tribunal de instancia que corresponda, como parte de la Jurisdicción Civil. En la presente demanda se ejercita una acción de regreso por parte de quien ha abonado una deuda, como deudor solidario en virtud de lo dispuesto en el art. 331 TRLSC 2010.

Asimismo, el Tribunal al que tengo el honor de dirigirme es competente territorialmente, según arts. 51.1 LEC, pues a su partido judicial corresponde al domicilio social de la entidad demandada.

II.- CAPACIDAD Y LEGITIMACIÓN

Mi mandante es mayor de edad y se encuentra en situación de pleno ejercicio de sus derechos civiles, en virtud de lo dispuesto en los arts. 6.1.1.º y 7.1 LEC. Asimismo, la demandada es persona jurídica, cuya capacidad se reconoce en el art. 6.1.3.º LEC, derivándose su personalidad de su constitución como sociedad de responsabilidad limitada en escritura pública inscrita en el Registro Mercantil, con la necesidad de comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

Corresponde la legitimación activa directa a mi cliente, por cuanto que es socio de la entidad demandada, y que ha respondido de una deuda como deudor solidario con arreglo al art. 331 TRLSC 2010. Razón por la cual ejercita la presente acción de regreso. Asimismo, en cuanto a la legitimación pasiva, corresponde a la entidad [DENOMINACIÓN SOCIAL], por cuanto es la sociedad directamente responsable de la deuda abonada por mi mandante, en el ámbito de los distintos deudores solidarios de la misma.

III.- PROCEDIMIENTO Y CUANTÍA

Cumpliendo la exigencia del art. 253.1 LEC, se cifra la cuantía de la demanda en la cantidad de [IMPORTE] euros de principal a cuya condena de pago se peticiona. Asimismo, de acuerdo con el art. 249.2 LEC, y siendo la cuantía reclamada superior a 15.000 euros, la presente acción se tramitará por el procedimiento ordinario

IV.- POSTULACIÓN Y DEFENSA

Conforme a los arts. 23 y 31 LEC se formula esta demanda a través de Procurador de los Tribunales con poder notarial para pleitos, y con dirección y firma de Letrado habilitado ante el Tribunal. Asimismo, se cumplen los requisitos formales del art. 399 LEC.

V.- FONDO DE LA CUESTIÓN CONTROVERTIDA

1.- De la responsabilidad del art. 331 TRLSC 2010 reclamada a mi cliente

Mi mandante ha sido finalmente condenado a pagar al acreedor de la sociedad de responsabilidad limitada aquí demandada, en virtud de la responsabilidad solidaria que determina el art. 331 TRLSC 2010, en el periodo que va desde que se reduce el capital social de aquella, con devolución de aportaciones a los socios; hasta que la reducción es oponible a terceros, mediante su publicación en el BOREM. Es cierto que mi cliente no estaba de acuerdo con la reclamación en virtud de la cual fue condenado, y que se discutieron, tanto la cuantía reclamada, como las fechas de oponibilidad del acuerdo de reducción social del capital frente a terceros. Si bien, la cuestión se zanjó judicialmente, y a pesar del recurso de apelación, la sentencia dictada en la primera instancia mercantil devino firme.

De esta manera, se le condena al pago de una deuda generada, en la que no tuvo nada que ver, más allá de ser un socio más de la entidad que genera aquella, sin capacidad alguna de influir en su gestión. La deuda se le imputa en virtud del régimen de tutela de acreedores, en sede de reducción de capital social, que se configura legalmente en el citado art. 331 TRLSC 2010, con objeto de crear una responsabilidad temporal, personal, solidaria, de los socios de sociedades de responsabilidad limitada, hasta el importe de las devoluciones de aportaciones, derivadas de dicha reducción.

En el presente caso, [NOMBRE DE LA PARTE] no había activado ninguna de los mecanismos de exclusión o limitación de tal responsabilidad solidaria. Así, no se había dotado de la reserva con cargo a beneficios o reserva libre, prevista en el art. 332 TRLSC 2010, ni se recogía estatutariamente la posibilidad de oposición previa de los acreedores del art. 333 TRLSC 2010.

En consecuencia, la sentencia firme del Tribunal de Instancia (Sección de lo Mercantil), previa a la presente acción, considera que concurren los presupuestos de la responsabilidad solidaria de mi mandante: la deuda reclamada es anterior al acuerdo de reducción del capital social y a su publicidad frente a terceros (con inscripción de la identidad de los socios a quienes se devuelven aportaciones); no se encontraba especialmente garantizada; la cuantía reclamada era inferior al importe de las aportaciones efectivamente restituidas al socio; y las consecuencias de la reducción del capital consistieron específicamente en una devolución efectiva de parte de las aportaciones realizadas para suscribir participaciones sociales, conforme exige la Resolución DGRN de 10 de mayo de 2017.

2.- De la acción de regreso o repetición ejercitada:

A partir de dicha realidad incuestionable, mi mandante ejercita la presente acción de repetición prevista en el art. 1.145 CC, como deudor solidario que es, frente a otro de los codeudores en la parte que le corresponde. Esto es, se reclama íntegramente el pago de la deuda a [NOMBRE DE LA PARTE], al ser la sociedad mercantil que contrató con el acreedor, recibió la prestación de servicios sin objeción por su parte, e impagó parte del precio convenido.

Como se ha dicho, mi mandante se limitaba a ser un socio más de dicha entidad, nunca ha intervenido en su gestión, y es ajeno al hecho de que no hubiera una reserva constituida, ni que los acreedores carecieran de un procedimiento de oposición previo a la reducción.

Por ello se reclama el importe íntegro de lo pagado, cumpliendo con el criterio exigido por la STS nº 712/2016, de 28 de diciembre, de exigir el pago en función de su participación en el daño. Participación que, en el presente caso, es totalmente imputable a la aquí demandada. En este sentido, es posible que en la vía de regreso se diluciden las responsabilidades concretas de los condenados solidariamente en un proceso anterior; e incluso, tal y como permite la STS de 5 de mayo de 2010, Sentencia 274/2010, Rec. 858/2005, reclamar frente a un deudor solidario no condenado en el pleito anterior.

3.- De la cosa Juzgada

En consecuencia, en el presente procedimiento se reclama frente a la sociedad codemandada por el importe íntegro de la deuda abonada, al atribuir toda la responsabilidad de la misma a [NOMBRE DE LA PARTE]. Cuestión que determinará el objeto del pleito que nos ocupa.

Si bien, hay determinadas cuestiones que no se podrán volver a plantear, como son la deuda en sí (se ha trascrito en los hechos de esta demanda uno de los hechos probados de la sentencia condenatoria), su importe, y el pago por parte de mi mandante. Así, entra en juego el instituto de la cosa juzgada del art. 222 TRLConc, interpretado por la Jurisprudencia del Tribunal Supremo.

Ejemplos de dicha Jurisprudencia son la STS de 13 de marzo de 2007 o la nº 106/2004 de 27 de febrero, que indica «la eventual repetición habrá de respetar lo así resuelto o declarado, en una suerte de efecto prejudicial evitatorio de la posible contradicción en las resoluciones o hasta vulneración del "non bis in idem". Extremo íntimamente vinculado a la propia acción de repetición, dado que la posibilidad establecida en el art. 1.145.2 CC está fundamentada en la interdicción del enriquecimiento sin causa y cuyo único presupuesto es la validez y eficacia del pago liberador efectuado por el regresante, cuyo importe se acredita, en este caso, con el extracto de la transferencia. En definitiva, siendo firme y con efectos de cosa juzgada la sentencia dictada en el anterior procedimiento, la responsabilidad solidaria impuesta en su día a mi mandante, es inatacable, por lo que lo único que puede discutirse en el presente procedimiento, es la imputación de la misma a la aquí demandada; lo que se sostiene en el presente escrito.

En consecuencia, a tenor de todo lo expuesto, debe condenarse a la entidad [DENOMINACIÓN SOCIAL], a pagar a mi representado la cantidad de [IMPORTE] euros, con intereses legales desde el [FECHA], fecha de la reclamación extrajudicial.

VI. COSTAS

Conforme al artículo 394 de la LEC, las costas han de imponerse al demandado.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

que teniendo por presentado este escrito de demanda con sus documentos y copias, se sirva admitirlo y acordar de conformidad, teniendo por interpuesta demanda de Juicio Declarativo Ordinario contra la entidad [DENOMINACIÓN SOCIAL], para que en su día, seguidos sean los trámites legales oportunos, se dicte sentencia por la que se condene a la misma al pago a mi mandante de la cantidad de [IMPORTE] euros, intereses legales desde la reclamación extrajudicial de fecha [FECHA] y al pago de las costas causadas.

En [LUGAR], a [FECHA].

Firma del Procurador

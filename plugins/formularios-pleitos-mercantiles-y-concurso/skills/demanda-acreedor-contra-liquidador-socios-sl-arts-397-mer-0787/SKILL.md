---
name: demanda-acreedor-contra-liquidador-socios-sl-arts-397-mer-0787
description: "Demanda del acreedor contra el liquidador y los socios de una SL (arts. 397 y 399 LSC). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del acreedor contra el liquidador y los socios de una SL (arts. 397 y 399 LSC)

> Formulario **MER-0787** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Se ejercita la acción individual de responsabilidad de liquidadores sociales prevista en el art. 397 TRLSC, en relación con el art. 241 TRLSC, por haber dejado impagado un crédito, de manera consciente. Y, asimismo, se acumula la acción de reclamación contra los tres socios codemandados, a partir de lo dispuesto en el art. 399.1 TRLSC, quienes deben responder hasta el límite de lo recibido como cuota de liquidación

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del acreedor contra el liquidador y los socios de una SL (arts. 397 y 399 LSC)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del acreedor contra el liquidador y los socios de una SL (arts. 397 y 399 LSC)” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-acreedor-contra-liquidador-socios-sl-arts-397-mer-0787`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (25 veces)
- [ ] FECHA (8 veces)
- [ ] IMPORTE (8 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] SEDE (3 veces)
- [ ] AÑO
- [ ] FECHA DE LA ESCRITURA
- [ ] LUGAR
- [ ] NIF
- [ ] NOMBRE Y Nº DE COLEGIADO
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] OBJETO DEL SERVICIO
- [ ] TIPO DE SERVICIOS PRESTADOS
- [ ] TOMO

## Normas que cita el formulario

- art. 155 Ley 1/2000
- art. 6.1.1 LEC
- art. 29 Código Civil
- art. 23 LEC
- art. 10 LEC
- art. 397 TRLSC
- art. 399.1 TRLSC
- art. 253.1 LEC
- art. 249.2 LEC
- art. 241 TRLSC
- art. 399.2 TRLSC
- art. 391.2 TRLSC
- art. 241 bis TRLSC
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

Se ejercita la acción individual de responsabilidad de liquidadores sociales prevista en el art. 397 TRLSC, en relación con el art. 241 TRLSC, por haber dejado impagado un crédito, de manera consciente. Y, asimismo, se acumula la acción de reclamación contra los tres socios codemandados, a partir de lo dispuesto en el art. 399.1 TRLSC, quienes deben responder hasta el límite de lo recibido como cuota de liquidación


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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA [SEDE] QPTC

D./Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS] según acredito mediante escritura de Poder que debidamente bastanteada acompaño como documento nº 1 de los que se unen al presente escrito para su unión a los Autos mediante copia, previa su certificación por el Letrado de la Administración de Justicia del Tribunal al que tengo el honor de dirigirme, y cuya devolución intereso por precisarlo para otros usos, dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho,

DIGO:

Que mediante el presente escrito formulo demanda de Juicio Declarativo Ordinario contra

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

[NOMBRE Y APELLIDOS], antiguos socios de la mercantil [DENOMINACIÓN SOCIAL] SL, y contra D./Dña. [NOMBRE Y APELLIDOS], liquidador de la misma, en reclamación de la cantidad de [IMPORTE] euros; designando como su domicilio, a efectos de notificaciones, a tenor del artículo 155 de la Ley 1/2000, de 7 de enero, de Enjuiciamiento Civil (en lo sucesivo, LEC), los siguientes, por su orden respectivo:

1º.- En sus domicilios particulares en:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[NOMBRE Y APELLIDOS], respectivamente.

2º.- En el lugar que presta sus servicios como liquidador D./Dña. [NOMBRE Y APELLIDOS] para la entidad [DENOMINACIÓN SOCIAL] SL, con domicilio social en [LOCALIDAD].

Fundamento mis pretensiones en los siguientes

HECHOS

Primero.- Mi representado es acreedor de la mercantil [DENOMINACIÓN SOCIAL] SL, en la cantidad de [IMPORTE] euros, como consecuencia de la prestación de sus servicios como [TIPO DE SERVICIOS PRESTADOS], para [OBJETO DEL SERVICIO] Los servicios se prestaron, sin queja alguna por parte de la prestataria en [FECHA], y la factura correspondiente, que se adjunta como documento nº 1, no ha sido abonada en ningún momento. La misma fue enviada con acuse de recibo, que se aporta como documento nº 2, en fecha [FECHA], al entonces administrador societario, hoy liquidador y codemandado en el presente escrito.

Segundo.- La sociedad [DENOMINACIÓN SOCIAL] SL fue constituida el [FECHA], según consta en la escritura autorizada el [FECHA DE LA ESCRITURA] por D./Dña. [NOMBRE Y APELLIDOS], Notario de [LOCALIDAD], su domicilio social se halla sito en [LOCALIDAD], y fue inscrita en el Registro Mercantil nº [NÚMERO] de los de [SEDE] el [FECHA], Tomo [TOMO], con NIF [NIF].

Acredito estos extremos con el documento nº 3 de los que se acompañan a este escrito, y consistente en copia simple de la escritura de constitución mencionada, así como con el documento nº 4, que recoge la certificación del Registro Mercantil donde constan los datos mencionados. El objeto social de dicha mercantil consiste en

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

fueron titulares de 5.000 participaciones sociales, cada uno, de la entidad demandada, lo que supone un 33,3 % del capital social en cada caso.

D./Dña. [NOMBRE Y APELLIDOS], anterior administrador único, fue liquidador de la sociedad, desde su nombramiento como tal en junta ordinaria celebrada el [FECHA], en la que se acordó la disolución de la sociedad, tal y como consta en la certificación del Registro Mercantil que se acompaña como documento nº 5.

Tercero.- El [ELEGIR: el codemandado / la codemandada] D./Dña. [NOMBRE Y APELLIDOS], formuló inventario y balance de la sociedad a fecha de disolución, cuyas copias se acompañan como documentos nº 6 y 7, respectivamente, sin que se incluyera el crédito de mi mandante. El [FECHA] el liquidador fue notificado por burofax, aportado como documento nº 8, de tal omisión, sin que hubiese respuesta alguna por su parte. La no inclusión del crédito se mantuvo en el balance final de liquidación, acompañado como documento nº 9, aprobado en la junta general de socios celebrada el pasado día [FECHA]. A dicho balance se acompañó un informe completo sobre las operaciones liquidatorias, que no recogían, evidentemente, el pago del crédito referido, y el proyecto de división entre los socios del activo resultante (documentos nº 10 y 11). Todo ello fue objeto de aprobación tal y como se puede comprobar en la certificación del Registro Mercantil aportada como documento nº 12, sin que fuera impugnado por ningún socio en el plazo legal de dos meses. Como consecuencia de dicho reparto, cada uno de los tres socios codemandados recibió la cantidad de [IMPORTE] euros.

A los presentes hechos les son de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I.- Capacidad de las partes

Todas las partes son mayores de edad y se encuentra en situación de pleno ejercicio de sus derechos civiles, conforme a lo dispuesto en los arts. 6.1.1º y 7 de la LEC en relación a los artículos 29 y 322 del Código Civil.

II.- Postulación y defensa

Conforme a lo previsto en los arts. 23 y 31 LEC, se presenta la demanda por medio de Procurador legalmente habilitado y bajo dirección letrada firmante de la misma.

III.- Legitimación

Ostenta legitimación activa mi poderdante pues su acción nace de su carácter de acreedor de la persona jurídica demandada, y le corresponde su ejercicio en nombre propio a los efectos del artículo 10 de la LEC, en relación a los arts. 397 y 399 del texto refundido de la Ley de Sociedades de Capital, aprobado por el Real Decreto Legislativo 1/2010, de 2 de julio (en lo sucesivo, TRLSC).

Asimismo, están legitimados pasivamente los demandados, D./Dña. [NOMBRE Y APELLIDOS] como liquidador de una Sociedad de Responsabilidad Limitada contra la que se reclama por el perjuicio sufrido por su actuación dolosa, con arreglo al art. 397 TRLSC, y los tres antiguos socios, D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], y D./Dña. [NOMBRE Y APELLIDOS], quienes responden solidariamente hasta su cuota de liquidación (que supera en todos los casos el crédito aquí reclamado), de manera solidaria, en virtud de lo dispuesto el art. 399.1 TRLSC.

IV.- Jurisdicción y Competencia

En cuanto a la competencia objetiva, se plantea la demanda ante la Sección de lo Mercantil del Tribunal de Instancia [SEDE].

Asimismo, el Tribunal al que tengo el honor de dirigirme es competente territorialmente, según 50.1 LEC pues a su partido judicial corresponde al domicilio de los demandados.

V.- Cuantía y Procedimiento

Cumpliendo la exigencia del art. 253.1 LEC, se cifra la cuantía de la demanda en la cantidad de [IMPORTE] euros, principal a cuya condena de pago se peticiona. Asimismo, de acuerdo con el art. 249.2 LEC, y siendo la cuantía reclamada superior a 15.000 euros, la presente acción se tramitará por el procedimiento ordinario.

VI.- Fondo del Asunto

1. De las acciones ejercitadas

En la presente demanda se acumulan dos acciones para reclamar el crédito que la asiste a mi mandante, y que no ha sido cobrado en el marco de la liquidación societaria de la entidad Hermanos Gutiérrez SL, a pesar de haberse procedido a repartir amplias cuotas liquidatorias a los tres codemandados, con las que se habría podido saldar perfectamente la deuda que aquí se reclama.

De esta forma, se ejercita la acción individual de responsabilidad de liquidadores sociales prevista en el art. 397 TRLSC, en relación con el art. 241 TRLSC, dirigiéndose contra liquidador D./Dña. [NOMBRE Y APELLIDOS] por haber dejado impagado aquél, de manera consciente. Y, asimismo, se acumula la acción de reclamación contra los tres socios codemandados, a partir de lo dispuesto en el art. 399.1 TRLSC, quienes responden hasta el límite de lo recibido como cuota de liquidación. Tal acumulación es posible con arreglo a lo dispuesto en el propio art. 399.2 TRLSC, cuando dispone que la responsabilidad de los socios se entiende sin perjuicio de la responsabilidad de los liquidadores.

2. Acción individual de responsabilidad del liquidador social

En consecuencia y en primer lugar, mi cliente, como acreedor perjudicado por la actuación del liquidador, se dirige contra éste, para reclamarle el daño ocasionado, consistente en el impago total de su crédito. En este sentido, D./Dña. [NOMBRE Y APELLIDOS] ha sido administrador único de la mercantil antes indicada, conoce perfectamente los servicios prestados por mi mandante, que fueron encargados por él, y realizados a su entera satisfacción. Asimismo, ha recibido reclamaciones para su cobro, antes y después de ser nombrado liquidador, sin que siquiera haya dado explicación alguna al respecto. Se ha limitado a ignorar todas y cada una de las realizadas, mientras se repartía el patrimonio de la mercantil beneficiada por los servicios impagados. Entre ellos, la sede social, vendida en el marco de la liquidación, tras haber sido sustancialmente reformada y mejorada por la intervención de mi mandante.

Por ello, concurren los requisitos establecidos en los arts. 397 y 241 TRLSC, para poder dirigirse frente al liquidador codemandado, quien, como administrador que es de la sociedad en liquidación, ve equiparada su responsabilidad con la de los administradores, en la línea señalada por la Sentencia del Tribunal Supremo de fecha 27 de noviembre de 2014, recurso [Nº DE PROCEDIMIENTO]/[AÑO]. De esta manera, tal y como interpreta la Sentencia del Tribunal Supremo de 18 de abril de 2011, recurso 289/2008, en un análisis de los preceptos previstos al respecto en la derogada Ley de Sociedades Anónimas, y que son antecedentes de los preceptos legales referidos, concurren los siguientes requisitos:

1) Acción u omisión en fraude o por negligencia grave, excluyéndose los supuestos de simple negligencia. En el presente caso, el demandado ha sido plenamente consciente de la deuda de mi representado, y ha decidido ignorarla, agotando el patrimonio con el cual podría abonarse. Se ha infringido el art. 391.2 TRLSC que obliga al liquidador, a la hora de dividir el patrimonio social, a satisfacer previamente a los acreedores el importe de sus créditos, o, en su caso, consignarlos en una entidad de crédito.
2) Que la acción u omisión se desarrolle por el liquidador o liquidadores precisamente en tal concepto. Tal omisión se ha producido durante todo el proceso liquidatorio, del cual el mismo es el director, incluso teniendo conocimiento de todo ello, mucho antes de que se aperturara aquel.
3) Daño o perjuicio directo o indirecto -"cualquier perjuicio", según el tenor de la norma-. La falta de cobro de los [IMPORTE] euros, constituye el daño originado al patrimonio de mi cliente.
4) Relación de causalidad entre el actuar de los liquidadores y el daño. La cual concurre claramente, puesto que de haber atendido la reclamación de pago, lo que era perfectamente posible, y para lo que venía obligado por lo dispuesto en el precepto legal mencionado; el daño aquí reclamado no se hubiera producido. Tal concurrencia se adapta a lo que la sentencia en análisis exige al respecto, "establecida una relación de causalidad física o fenomenológica entre el agente y el resultado dañoso, debe formularse un juicio mediante el cual se aprecia si las consecuencias dañosas de la actividad son susceptibles de ser atribuidas jurídicamente al agente, aplicando las pautas o criterios extraídos del Ordenamiento jurídico que justifican o descartan dicha imputación cuando se ponen en relación con el alcance del acto dañoso particularmente considerado, con su proximidad al resultado producido, con su idoneidad para producir el daño y con los demás elementos y circunstancias concurrentes".
[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— (Si se considerara aplicable el nuevo plazo de prescripción de la acción individual de responsabilidad, introducido en el actual art. 241 bis TRLSC por la Ley 31/2014, de 3 de diciembre, por la que se modifica la Ley de Sociedades de Capital para la mejora del gobierno corporativo, con entrada en vigor el 24 de diciembre de 2014, y que modifica el diez a quo)
— Si no se considera aplicable el art. 241 bis TRLSC)

3.- Acción de reclamación frente a los antiguos socios por las deudas sociales

En segundo lugar, y según lo argumentado, la acción se dirige contra los tres antiguos socios de la mercantil Hermanos Gutiérrez SL, quienes, en virtud del art. 399.1 TRLSC, responden solidariamente de la deuda social no satisfecha, hasta el límite recibido como cuota de liquidación, que en cada caso ascendió a la cantidad de [IMPORTE] euros.

Esta acción, tal y como es interpretada por la Sentencia del Tribunal Supremo de 22 de diciembre de 2011, recurso 1718/2008, no requiere como requisito de prosperabilidad una reapertura del proceso de liquidación, ni la existencia de fraude, o reproche alguno de culpabilidad. Simplemente exige:

1.- Que se acredite la existencia del crédito, lo que deriva de la documental acompañada, sin que exista ningún tipo de reclamación, protesta o queja alguna respecto a los servicios de arquitecto prestados.
2.- Que se ejercite la acción por el titular del crédito o persona legitimada, y se dirija contra los socios que se han beneficiado del saldo positivo de la liquidación social. Extremos que concurren todos ellos.
3.- Y que la reclamación se ciña al límite de lo recibido como cuota de liquidación, habiendo percibido cada socio la cantidad total de [IMPORTE] euros.

El fundamento de la acción, continúa diciendo la resolución mencionada, se apoya en diversas posturas, con variadas perspectivas jurídicas, "Se habla deasunción por los socios de la posición de la sociedad, asunción de garantía de las deudas sociales pendientes, sucesión del socio en la sociedad extinguida(de modo similar a lo que sucede con las sucesiones hereditarias a beneficio de inventario),subrogación ex lege, enriquecimiento sin causa, y de afectación preferente del patrimonio social al pago de las deudas sociales(que constituye un principio general del régimen de las sociedades mercantiles)".

Finalmente, la acción se ejercita en plazo, pues tratándose de obligación legal para cuya efectividad no hay un plazo especial de prescripción extintiva, como acción personal, queda sujeta al plazo general de cinco años delart. 1964 del Código Civil

VII.- Costas

El total vencimiento de la parte demandada determina, según el artículo 394 de la LEC que ésta deba satisfacer todas las costas del presente procedimiento.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL

Que teniendo por presentado este escrito de demanda con sus documentos y copias, se sirva admitirlo y acordar de conformidad, teniendo por interpuesta demanda de Juicio Declarativo Ordinario contra D./Dña. [NOMBRE Y APELLIDOS] para que en su día, seguidos sean los trámites legales oportunos, se dicte sentencia por la que se condene solidariamente a D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], y D./Dña. [NOMBRE Y APELLIDOS], antiguos socios de la mercantil [DENOMINACIÓN SOCIAL] SL, y a D./Dña. [NOMBRE Y APELLIDOS], Liquidador de la misma, al pago de la cantidad de [IMPORTE] euros, intereses legales desde la presente reclamación y al pago de las costas causadas.

Es Justicia que solicito en [LUGAR], a [FECHA].

Abogado y número de colegiación [NOMBRE Y Nº DE COLEGIADO]

Procurador

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

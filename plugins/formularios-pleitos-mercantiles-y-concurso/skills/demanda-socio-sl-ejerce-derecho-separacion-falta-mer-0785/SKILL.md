---
name: demanda-socio-sl-ejerce-derecho-separacion-falta-mer-0785
description: "Demanda del socio de una SL que ejerce el derecho de separación por falta de reparto de dividendos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda del socio de una SL que ejerce el derecho de separación por falta de reparto de dividendos

> Formulario **MER-0785** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

El art. 348 bis LSC (con entrada en vigor el 1 de enero de 2017, tras levantarse la suspensión provisional de su vigencia), configura un derecho de separación automático y objetivo para los socios cuando la sociedad no reparta un tercio de los beneficios anualmente a partir del quinto ejercicio desde su constitución, con independencia de la concreta situación económica en que se encuentre la compañía. En el presente supuesto, dándose todos los requisitos previstos en dicho precepto, y solicitándose en plazo la disolución, el órgano de administración deniega dicho derecho, y ante dicha negativa se interpone esta demanda.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda del socio de una SL que ejerce el derecho de separación por falta de reparto de dividendos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda del socio de una SL que ejerce el derecho de separación por falta de reparto de dividendos” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-socio-sl-ejerce-derecho-separacion-falta-mer-0785`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (9 veces)
- [ ] FECHA (8 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DATOS REGISTRALES
- [ ] LUGAR
- [ ] NIF
- [ ] NÚMERO
- [ ] OTROS DATOS

## Normas que cita el formulario

- art. 348 bis Real Decreto Legislativo 1/2010
- art. 87 LOPJ
- art. 51.1 LEC
- art. 6.1.3.º LEC
- art. 7.4 LEC
- art. 23 LEC
- art. 399 LEC
- art. 348 bis LSC
- art. 353.1 LSC
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

El art. 348 bis LSC (con entrada en vigor el 1 de enero de 2017, tras levantarse la suspensión provisional de su vigencia), configura un derecho de separación automático y objetivo para los socios cuando la sociedad no reparta un tercio de los beneficios anualmente a partir del quinto ejercicio desde su constitución, con independencia de la concreta situación económica en que se encuentre la compañía. En el presente supuesto, dándose todos los requisitos previstos en dicho precepto, y solicitándose en plazo la disolución, el órgano de administración deniega dicho derecho, y ante dicha negativa se interpone esta demanda.


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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA QUE POR TURNO CORRESPONDA

D./Dña. [NOMBRE Y APELLIDOS], Procurador/Procuradora de los Tribunales y de D./D.ª [NOMBRE Y APELLIDOS] como acredito en virtud de escritura de poder que acepto y acompaño, y cuya devolución intereso por ser de carácter general y necesaria para otros usos, bajo la dirección letrada de D./D.ª [NOMBRE Y APELLIDOS], abogado/a ejerciente, n.º [NÚMERO] del Iltre. Colegio de [LOCALIDAD], con despacho abierto en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho,

DIGO:

Que por medio del presente escrito paso a interponer demanda de juicio ordinario, en la que ejercito la acción de separación frente a la entidad [DENOMINACIÓN SOCIAL], SL, con domicilio social en [LOCALIDAD].

Todo ello de acuerdo con los siguientes hechos y consideraciones de derecho:

HECHOS

Primero.- Mi mandante es socio de la mercantil [DENOMINACIÓN SOCIAL] SL, constituida el [FECHA], según consta en la escritura autorizada el día [FECHA] por D./D.ª [NOMBRE Y APELLIDOS], Notario de [LOCALIDAD], con domicilio social en [LOCALIDAD], e inscrita en el Registro Mercantil nº [Nº] de [LOCALIDAD] el [FECHA], en el [DATOS REGISTRALES], con CIF [NIF]. Ostenta la titularidad de participaciones sociales con números del [Nº] al [Nº], ambos inclusive, con un valor de [IMPORTE] euros cada una, lo que hace un total de [IMPORTE] euros por todas las participaciones.

Acredito estos extremos con el documento nº [Nº] de los que se acompañan a este escrito, consistente en copia simple de la escritura de constitución mencionada, así como con el documento nº [Nº], que recoge la certificación del Registro Mercantil donde constan los datos mencionados. Como documento nº [Nº DE DOCUMENTO] se aporta certificación del libro registro de socios, donde se hace constar la referida titularidad de las participaciones sociales.

Segundo.- Como se ha indicado, la sociedad se inscribió en el Registro Mercantil, en fecha [FECHA], habiendo, por ello, transcurrido el plazo de cinco años desde su puesta en funcionamiento. Durante este tiempo no se ha producido reparto alguno de dividendos. Se acompaña bloque documental nº [Nº], con las actas de las juntas de socios realizadas durante todo este lapso de tiempo, en el cual se puede comprobar tal realidad.

Tercero.- En la Junta celebrada el pasado [FECHA], se propuso un reparto de dividendos con arreglo a los beneficios sociales obtenidos en el ejercicio anterior, consistente en que cada socio recibiera [IMPORTE] euros por participación ostentada, que correspondía exactamente a un tercio de dichos beneficios. Los mismos eran repartibles, cuanto menos en la proporción mínima propuesta, dado que no existían pérdidas, y las reservas legales y estatutarias estaban correctamente dotadas. Así se hizo constar en la convocatoria de la junta, cuya copia se adjunta como documento nº [Nº DE DOCUMENTO]. La propuesta fue votada favorablemente por mi cliente, si bien, no alcanzó la mayoría de capital necesaria para ello, y fue finalmente rechazada por la junta. Extremos que se pueden comprobar en el acta correspondiente, cuya copia se aporta como documento nº [Nº DE DOCUMENTO]. Se aporta también, como bloque documental nº [Nº] las cuentas anuales del pasado ejercicio, de las que se desprende la indicada situación económica que permitía el reparto de beneficios.

Cuarto.- El pasado [FECHA], antes de que transcurriera un mes desde la celebración de la última junta, mediante correo certificado se comunicó por escrito al administrador social único, D./Dña. [NOMBRE Y APELLIDOS], la voluntad de mi mandante de ejercer el derecho de separación que le confiere el art. 348 bis del Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el texto refundido de la Ley de Sociedades de Capital (en lo sucesivo, LSC). La comunicación, cuya copia se acompaña como documento nº [Nº], expresaba el valor individual y global de las participaciones sociales antes expuestas, en orden a su correspondiente reembolso. Se añadía que, para el caso de que no hubiera acuerdo sobre el valor propuesto, debería estarse a lo que dictaminara un auditor nombrado específicamente para ello, por el Registrador Mercantil.

Quinto.- El administrador social único de la sociedad aquí demandada expresó en fecha [FECHA], por el mismo conducto de correo certificado, su negativa a la separación, sin ofrecer argumento alguno al respecto. Se aporta copia de dicha respuesta como documento nº [Nº DE DOCUMENTO]. Asimismo, ha reiterado verbalmente a mi mandante, esa negativa a la separación, bajo el argumento de que la entidad se encuentra en un momento crucial, y que no puede prescindirse de ninguno de los socios.

A los presentes hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA.

En cuanto a la competencia objetiva, se plantea la demanda ante la sección de lo Mercanti del Tribunal de Instancia que corresponda, como parte de la Jurisdicción Civil, en virtud del art. 87 LOPJ, según el cual tales órganos conocerán, asimismo, de cuantas cuestiones sean de la competencia del orden jurisdiccional civil, respecto de "todas aquellas cuestiones que dentro de este orden jurisdiccional se promuevan al amparo de la normativa reguladora de las sociedades mercantiles y cooperativas".

Asimismo, el Tribunal al que tengo el honor de dirigirme es competente territorialmente, según arts. 51.1 LEC, pues a su partido judicial corresponde al domicilio social de la entidad demandada.

II.- CAPACIDAD Y LEGITIMACIÓN.

Mi mandante es mayor de edad y se encuentra en situación de pleno ejercicio de sus derechos civiles, en virtud de lo dispuesto en los arts. 6.1.1.º y 7.1 LEC. Asimismo, la demandada es persona jurídica, cuya capacidad se reconoce en el art. 6.1.3.º LEC, derivándose su personalidad de su constitución como sociedad de responsabilidad limitada en escritura pública inscrita en el Registro Mercantil, con la necesidad de comparecer en juicio por medio de sus representantes legales (art. 7.4 LEC).

Corresponde la legitimación activa directa a mi cliente, por cuanto que es socio de la entidad demandada, ha votado a favor del reparto de dividendos posible, y la mayoría del capital social ha decidido lo contrario. Asimismo, en cuanto a la legitimación pasiva, corresponde a la entidad SL, por cuanto es la sociedad, en cuyo seno se ha decidido no repartir aquello a lo que todos los socios tienen derecho, y cuyo administrador se niega injustificadamente a la separación pretendida.

III.- PROCEDIMIENTO Y CUANTÍA.

Según los artículos 248 y 249.2 de la LEC el presente pleito ha de tramitarse según las reglas del Juicio Ordinario, pues no teniendo materia especial propia del Juicio Verbal, su interés económico resulte imposible de calcular, ni siquiera de modo relativo.

IV.- POSTULACIÓN Y DEFENSA.

Conforme a los arts. 23 y 31 LEC se formula esta demanda a través de Procurador de los Tribunales con poder notarial para pleitos, y con dirección y firma de Letrado habilitado ante el Tribunal. Asimismo se cumplen los requisitos formales del art. 399 LEC.

V.- FONDO DE LA CUESTIÓN CONTROVERTIDA.

1) Del derecho de separación ejercitado:

Los arts. 346 y ss. LSC regulan las causas legales de separación de los socios en las sociedades de capital, en los supuestos en los que alguno de aquellos no esté de acuerdo, y haya votado en contra, de determinadas decisiones de entidad en la vida societaria. De esta forma, se establecen causas legales de separación, y se da cabida a que se añadan otras en los correspondientes estatutos.

Entre las causas legales de separación, se regula expresamente en el art. 348 bis LSC"Transcurrido el quinto ejercicio contado desde la inscripción en el Registro Mercantil de la sociedad, el socio o socia que hubiera hecho constar en el acta su protesta por la insuficiencia de los dividendos reconocidos tendrá derecho de separación en el caso de que la junta general no acordara la distribución como dividendo de [OTROS DATOS], al menos, el veinticinco por ciento de los beneficios obtenidos durante el ejercicio anterior que sean legalmente distribuibles siempre que se hayan obtenido beneficios durante los tres ejercicios anteriores. Sin embargo, aun cuando se produzca la anterior circunstancia, el derecho de sepración no surgirá si el total de los dividendos distribuidos durante los últimos cinco años equivale, por lo menos, al veinticinco por ciento de los beneficios legalmente distribuibles registrados en dicho periodo".

De esta forma, con el precepto legal expuesto se intenta buscar un remedio al abuso de derecho o abuso de poder de la mayoría social, consistente en negar a la minoría el derecho al dividendo. Así lo fue exigiendo una jurisprudencia de la que es ejemplo la Sentencia del Tribunal Supremo, Sala Primera, de lo Civil, 125/2012 de 20 Mar. 2012, Rec. 1699/2008, con cita de Tribunal Supremo, Sala Primera, de lo Civil, Sentencia 873/2011 de 7 Dic. 2011, Rec. 1857/2008, y culminó en la Ley 25/2011, de 1 de agosto, que incorpora el citado art. 348 bis LSC, cuya vigencia se retrasa hasta 2017.

Se otorga, en consecuencia, una salida a aquellas situaciones de opresión o abuso de la mayoría del capital social en la política de distribución de dividendos.

En este caso, y conforme a los hechos expuestos en los antecedentes del presente escrito expositivo, concurren todos los requisitos legalmente exigidos para la separación que aquí se interesa:

1.- Se ha denegado recientemente por la Junta General de Socios el reparto de dividendos mínimo al que se tenía derecho, el veinticinco por ciento de los beneficios propios derivados de la explotación del objeto social, y obtenidos durante el ejercicio anterior. Teniendo en cuenta además, que la empresa demandada ha obtenido beneficios durante los tres ejercicios anteriores al último cerrado. En este sentido, la Audiencia Provincial de Barcelona, Sección 15ª, Sentencia 81/2015 de 26 Mar. 2015, Rec. 175/2014 atiende, siguiendo lo dispuesto en el Plan General de Contabilidad (aprobado por Real Decreto 1514/2007, de 16 de noviembre), al concepto de "beneficio propio de la explotación del objeto social", esto es, los ingresos que deriven de las actividades ordinarias y típicas de la empresa, y que se repitan con frecuencia. Concepto en el que se engloban los beneficios que se pretendían repartir.
2.- Mi mandante votó a favor de tal acuerdo, pero quedó en minoría frente a la mayor parte del capital social y dejó consyancia en acta de su protesta..
3.- La sociedad demandada lleva más de cinco años inscrita en el Registro Mercantil y el total de los dividendos distribuidos durante los últimos cinco años no equivale al veinticinco por ciento de los beneficios legalmente distribuibles registrados en ese periodo
4.- Los beneficios son legalmente repartibles dado que ni existían pérdidas, ni el último ejercicio, ni en los anteriores, y las reservas legales y estatutarias estaban correctamente dotadas; tal y como se puede comprobar con las últimas cuentas anuales aprobadas.
5.- Dentro del plazo de un mes, computado desde la referida Junta General, mi mandante ha instado por escrito al administrador social de la demandada, su separación con una propuesta del valor de sus participaciones sociales, a efectos de su correspondiente desembolso. En tal comunicación escrita mi mandante se mostraba de acuerdo, además, con otra eventual valoración llevada a cabo por un auditor de cuentas nombrado específicamente para ello, por el Registrador Mercantil.
6.- La sociedad demandada, evidentemente, no es una sociedad cotizada.

El recurso a la presente acción judicial viene obligado porque, a pesar de que se han cumplimentado todos los requisitos legales; el administrador social de la demandada, niega sin fundamento razonable alguno, la separación. Ni siquiera discute en su contestación la valoración de las participaciones sociales ofrecida, limitándose a señalar que no se puede prescindir en la coyuntura actual, de ningún socio. En esta línea, se recuerda que el art. 348 bis LSC, que configura este derecho de separación de forma automática y objetiva, obligando a la sociedad repartir un 25% de los beneficios anualmente a partir del quinto ejercicio desde su constitución, con independencia de la concreta situación económica en que se encuentre la compañía.

2.- De la forma de llevarse a cabo la separación:

En consecuencia, ante la negativa injustificada de la entidad demandada y en atención a todo lo expuesto, se interpone la presente demanda, para que judicialmente se acuerde la separación a la que mi cliente tiene derecho. La misma debe conllevar obligatoriamente, y así se solicita que se ordene en la propia sentencia, el reembolso de las [Nº] participaciones titularidad de mi cliente, por el valor razonable de [IMPORTE] euros. Valoración que se desprende de la situación económica de la empresa, y de la documentación aportada.

En el supuesto de que, de contrario, se discuta la misma, mi mandante se muestra de acuerdo en que el valor sea finalmente determinado judicialmente, sobre la base de lo que dictamine un auditor nombrado específicamente para ello, por el Registrador Mercantil, con arreglo a lo dispuesto en el art. 353.1 LSC.

VI. COSTAS

Conforme al artículo 394 de la LEC, las costas han de imponerse al demandado.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito de demanda con sus documentos y copias, se sirva admitirlo y acordar de conformidad, teniendo por interpuesta demanda de Juicio Declarativo Ordinario en ejercicio de la acción de separación de mi mandante frente a la entidad SL, para que en su día, seguidos sean los trámites legales oportunos, se dicte sentencia por la que se declare la separación del demandante, con reembolso de las participaciones sociales por importe de [IMPORTE] euros cada una, o el valor que se determine judicialmente; condenándole al pago de las costas ocasionadas.

Por ser justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado y número de colegiado

Firma del Procurador:

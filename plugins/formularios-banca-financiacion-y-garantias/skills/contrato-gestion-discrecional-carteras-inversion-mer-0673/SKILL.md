---
name: contrato-gestion-discrecional-carteras-inversion-mer-0673
description: "Contrato de gestión discrecional de carteras de inversión. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de gestión discrecional de carteras de inversión

> Formulario **MER-0673** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de gestión discrecional de carteras de inversión» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de gestión discrecional de carteras de inversión” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-gestion-discrecional-carteras-inversion-mer-0673`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] LUGAR
- [ ] MES

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

CONTRATO DE GESTIÓN DE CARTERAS

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO],

De otra:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL CLIENTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA ENTIDAD", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE GESTIÓN DE CARTERAS, de conformidad con las siguientes,

CLÁUSULAS

Objeto del contrato

El presente contrato regula la gestión discrecional e individualizada, por parte de la ENTIDAD, de los valores, efectivo y otros instrumentos financieros del CLIENTE que, en el momento de la firma de este contrato o en cualquier momento, ponga, con esa finalidad, a disposición de la ENTIDAD, así como de los rendimientos generados por aquéllos.

La cartera inicial del CLIENTE es la que se detalla en el Anexo I del presente contrato. La actividad de gestión recaerá exclusivamente y no podrá superar en ningún momento, salvo en los supuestos y límites que establezca la Comisión Nacional del Mercado de Valores, la suma de los dos conceptos siguientes:

a) El patrimonio aportado inicialmente o en sucesivas ocasiones por el CLIENTE.

b) El importe de créditos en su caso obtenidos de una entidad habilitada. La concesión de crédito exigirá, en todo caso, la previa formalización del correspondiente documento contractual de crédito suscrito por el CLIENTE y el acreditante.

La ENTIDAD actuará de acuerdo a las condiciones preliminares y cláusulas de este contrato y sólo podrá desviarse de los criterios generales de inversión pactados cuando el criterio profesional del gestor aconseje dicha desviación o se produzcan incidencias en la contratación. En estos casos, la ENTIDAD, además de registrar las desviaciones, informará con detalle de las mismas al CLIENTE de forma inmediata.

Depósito de los valores, instrumentos financieros y efectivo

La ENTIDAD promoverá el registro o depósito de los activos financieros objeto de este contrato, dando lugar a las correspondientes anotaciones en las cuentas de valores y efectivo afectas de forma exclusiva al presente contrato.

Facultades de la entidad

La ENTIDAD ejercitará su actividad de gestión con las más amplias facultades, pudiendo, en nombre y por cuenta del CLIENTE entre otras operaciones, comprar, suscribir, enajenar, prestar, acudir a las amortizaciones, ejercitar los derechos económicos, realizar los cobros pertinentes, conversiones y canje de los valores y, en general, activos financieros sobre los que recaiga la gestión, desarrollando las actuaciones, comunicaciones e iniciativas exigidas para ello, pudiendo, a tales efectos, suscribir cuantos documentos sean necesarios.

[ELEGIR UNA OPCIÓN: Autorizaciones expresas / Entidades no autorizadas a negociar por cuenta propia / Entidades autorizadas a negociar por cuenta propia / Opción 2: Entidades autorizadas a negociar por cuenta propia]

Obligaciones de información

5.1. Obligación de información general

Trimestralmente con carácter general, o mensualmente cuando la cartera gestionada presentara pérdidas al final del mes con respecto al final del mes anterior y cuando el perfil general de riesgo del CLIENTE sea "arriesgado" o "muy arriesgado", la ENTIDAD remitirá al CLIENTE la siguiente información:

a) Composición detallada de la cartera e información que posibilite su comparación con la situación de la cartera en el momento en que se efectuó la última comunicación.

b) Variaciones en la composición de la cartera habidas durante el período, incluyendo la liquidez, así como detalle de valores nominales y efectivos calculados éstos últimos según los criterios de valoración contenidos en el Anexo III del presente contrato, número de valores e instrumentos financieros comprados, vendidos o prestados, entidades a través de las que se hayan canalizado las operaciones, mercados, garantías depositadas, entidades que actúan de contrapartida en las operaciones OTC, pagos de cupones o de dividendos, fechas de conversión o canje y amortizaciones. La ENTIDAD identificará específicamente y de forma separada las operaciones, inversiones o actuaciones siguientes:

i) La inversión en valores o instrumentos financieros emitidos por la ENTIDAD o entidades de su grupo o en Instituciones de Inversión Colectiva gestionadas por éste.

ii) La suscripción o adquisición de valores o instrumentos financieros en los que la ENTIDAD o alguna entidad de su grupo actúe como asegurador o colocador de la emisión u oferta pública de venta.

iii) Los valores o instrumentos financieros resultantes de la negociación de la ENTIDAD o entidades del grupo con el CLIENTE.

iv) Operaciones entre el CLIENTE y otros clientes de la ENTIDAD.

c) Entidades que tuvieran depositados, administrados o registrados los valores, el efectivo y otros activos financieros, especificando en su caso las cuentas globales (cuentas ómnibus).

d) Detalle de las comisiones y gastos repercutidos directamente al CLIENTE tanto si el beneficiario es la propia ENTIDAD como si lo es un tercero. En todo caso se identificarán las entidades que perciben los correspondientes ingresos y los conceptos por los que se aplican.

Una vez al año, La ENTIDAD remitirá al CLIENTE la siguiente información:

a) Las cantidades totales, directa o indirectamente, percibidas por la ENTIDAD distintas de las directamente repercutidas al CLIENTE, en proporción al patrimonio gestionado al CLIENTE, como resultado de acuerdos alcanzados por la ENTIDAD con intermediarios u otras entidades financieras y que tengan su origen en operaciones realizadas para los clientes de la ENTIDAD en el marco del contrato de gestión de carteras.

b) Datos necesarios para la declaración de los Impuestos, en lo que hace referencia a la cartera gestionada.

5.2. Reducción superior al 25%

Si el valor de la cartera del CLIENTE experimentara una reducción superior al 25% de su valor a la fecha de referencia de la última información remitida al CLIENTE, la ENTIDAD comunicará esta situación al CLIENTE de forma inmediata.

5.3 Derecho de representación

Cuando la ENTIDAD solicite conforme a lo previsto en la normativa vigente, la representación del CLIENTE para el ejercicio de los derechos políticos derivados de las acciones pertenecientes a la cartera gestionada, deberán informar al CLIENTE expresamente de la existencia de cualquier relación o vínculo interesado entre la ENTIDAD y su grupo con alguna de las sociedades a las que se refiere la representación.

5.4 Obligación de información adicional

Siempre que el CLIENTE lo solicite, la ENTIDAD le proporcionará toda la información adicional concerniente a las operaciones realizadas, a las consultas que formule referentes a su cartera de valores y a las entidades a través de las cuales se hubieran canalizado las operaciones.

Actuación de la entidad

6.1. Situaciones de incompatibilidad

Las partes convienen y se hacen responsables de la aplicación al presente contrato de las normas de conducta previstas en la legislación del mercado de valores que resulten de aplicación. El CLIENTE informará a la ENTIDAD cuando surjan situaciones de incompatibilidad o alguna circunstancia que impida la inversión del patrimonio gestionado en determinados valores o instrumentos financieros.

6.2. Operaciones prohibidas

La ENTIDAD no efectuará en ningún caso operaciones prohibidas por la legislación española, ni aquellas que requieran autorizaciones oficiales o expresas del CLIENTE mientras no se obtengan estas autorizaciones.

6.3. Agrupación de operaciones

No obstante el carácter individual de la gestión de carteras, la ENTIDAD, con el objeto de racionalizar las órdenes de compraventa de activos podrá agrupar operaciones de diferentes clientes dentro de los límites establecidos en la normativa vigente. Para evitar un posible conflicto de interés entre los clientes derivado de esta u otras actuaciones, la ENTIDAD dispone de unos criterios objetivos de prorrateo o distribución de operaciones entre clientes en particular, y de resolución de posibles conflictos de interés en general, que se detallan a continuación:

Criterios: En caso de agruparse operaciones de diferentes clientes, el criterio de distribución de activos está definido por las decisiones tomadas en los Comités de Gestión de la mercantil [DENOMINACIÓN SOCIAL], que tienen en cuenta, en cada caso, el tamaño, perfil de riesgo, peso relativo de los valores y liquidez disponible en cada una de las carteras gestionadas. La ENTIDAD se compromete a aplicar en todo caso dichos criterios objetivos que sólo se modificarán previa comunicación y aceptación del CLIENTE.

6.4. Responsabilidad de la ENTIDAD

La ENTIDAD responderá de los perjuicios que pueda causar al cliente por el incumplimiento de las obligaciones asumidas en el presente contrato y por actuaciones dolosas o realizadas con negligencia, en cuyo caso indemnizará al CLIENTE.

Comisiones y régimen económico aplicable

El CLIENTE abonará a la ENTIDAD las tarifas correspondientes por el concepto de gestión de cartera y los gastos de intermediación y otras comisiones de acuerdo con lo previsto en las condiciones económicas incluidas en el Anexo II particular del presente contrato, que, en ningún caso, superan las recogidas en el folleto informativo de tarifas.

Asimismo, la cartera se valorará a esos efectos según lo previsto en el Anexo III del contrato. La ENTIDAD hará efectivas las cantidades debidas con cargo a la cuenta de efectivo del CLIENTE afecta al contrato de gestión.

La ENTIDAD informará al CLIENTE de cualquier modificación que se produzca en las tarifas de comisiones y gastos repercutibles que afecten al presente contrato. El CLIENTE dispondrá de dos meses desde la recepción de la citada información para solicitar la modificación o extinción del contrato, sin que le sean aplicadas las nuevas tarifas hasta que transcurra dicho plazo. Sin embargo, en el caso de que la tarifa sea claramente beneficiosa para el CLIENTE se aplicará inmediatamente.

Duración del contrato

La duración del presente contrato es indefinida, pudiendo cualquiera de las partes unilateralmente dar por finalizado el mismo en cualquier momento de su vigencia, mediante la correspondiente comunicación en la que habrá de señalarse e identificarse la(s) entidad(es) financiera(s) y las cuentas a nombre del cliente correspondientes, en las que éste podrá disponer de los valores, instrumentos financieros y efectivo que integren el patrimonio gestionado cuyo contrato es objeto de resolución.

Cuando la vigencia del contrato se desee interrumpir a voluntad de la ENTIDAD será necesario un preaviso de 15 días.

Efectos de la terminación del contrato

Una vez resuelto el contrato, la ENTIDAD rendirá y dará razón de las cuentas de gestión en un plazo máximo de 15 días.

En el caso de extinción anticipada del contrato, la ENTIDAD sólo tendrá derecho a percibir las comisiones por las operaciones realizadas pendientes de liquidar en el momento de la resolución del contrato y la parte proporcional devengada de las tarifas correspondientes al período iniciado en el momento de finalización del contrato.

La cancelación anticipada del contrato no afectará a la tramitación, liquidación y cancelación de las operaciones en curso que se hubiesen concertado con anterioridad a la comunicación, que seguirán rigiéndose por las condiciones a ellas aplicables, de acuerdo con las estipulaciones del presente contrato.

A partir de la comunicación efectiva de resolución anticipada del contrato, El CLIENTE dispondrá de su patrimonio de forma directa e inmediata en las cuentas de valores, instrumentos financieros y efectivo señaladas al efecto, y la ENTIDAD recabará instrucciones expresas del CLIENTE para cualquier otra operación. No obstante, cuando por el carácter extraordinario o urgente de las circunstancias no pudieran recabarse instrucciones del CLIENTE y fuese imprescindible la actuación de la ENTIDAD para mantener el valor de la cartera del CLIENTE, la ENTIDAD realizará las operaciones necesarias dando cuenta al CLIENTE de forma inmediata.

Modificación

El CLIENTE podrá retirar efectivo o activos de su cuenta, restringir o modificar los activos sobre los que se extienda la gestión de cartera o sustraerlos del régimen de gestión previsto en este contrato, poniéndolo en conocimiento de la ENTIDAD, en su caso, con la antelación suficiente como para que la correspondiente operación pueda realizarse.

Igualmente el CLIENTE comunicará con la suficiente antelación a la ENTIDAD cualquier acto de disposición o gravamen sobre los valores, activos o efectivo de su cartera.

El CLIENTE podrá limitar las facultades de gestión de la ENTIDAD, así como las diversas modalidades de inversión de la cartera, dar instrucciones a la ENTIDAD o modificar las ya existentes previa comunicación a la ENTIDAD.

Las modificaciones indicadas no afectarán a la tramitación, liquidación y cancelación de las operaciones en curso que se hubiesen concertado con anterioridad a la comunicación, que seguirán rigiéndose por las condiciones a ellas aplicables, de acuerdo con las estipulaciones del presente contrato.

Confidencialidad

Los términos de este Contrato así como cualquier información transmitida al amparo de lo previsto en el mismo serán confidenciales y no podrán ser revelados a terceros sin el previo consentimiento escrito de la otra Parte, salvo en caso de que la información sea de dominio público y en los restantes supuestos previstos en la legislación vigente y en el presente Contrato.

Protección de datos

En el caso de que la prestación de los Servicios suponga la necesidad de acceder a datos de carácter personal, las Partes quedan obligadas al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable. LA ENTIDAD responderá, por tanto, de las infracciones en que pudiera incurrir en el caso de que destine los datos personales a otra finalidad, los comunique a un tercero, o en general, los utilice de forma irregular, así como cuando no adopte las medidas correspondientes para el almacenamiento y custodia de los mismos. A tal efecto, se obliga a indemnizar por cualesquiera daños y perjuicios que sufra directamente, o por toda reclamación, acción o procedimiento, que traiga su causa de un incumplimiento o cumplimiento defectuoso por parte de LA ENTIDAD de lo dispuesto tanto en el Contrato como lo dispuesto en la normativa reguladora de la protección de datos de carácter personal.

A los efectos de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales, LA ENTIDAD únicamente tratará los datos de carácter personal a los que tenga acceso conforme a las instrucciones del CLIENTE y no los aplicará o utilizará con un fin distinto al objeto del Contrato, ni los comunicará, ni siquiera para su conservación, a otras personas. En el caso de que LA ENTIDAD destine los datos a otra finalidad, los comunique o los utilice incumpliendo las estipulaciones del Contrato, será considerado también responsable del tratamiento, respondiendo de las infracciones en que hubiera incurrido personalmente.

LA ENTIDAD deberá adoptar las medidas de índole técnica y organizativas necesarias que garanticen la seguridad de los datos de carácter personal y eviten su alteración, pérdida, tratamiento o acceso no autorizado, habida cuenta del estado de la tecnología, la naturaleza de los datos almacenados y los riesgos a que están expuestos, ya provengan de la acción humana o del medio físico o natural. A estos efectos el PROVEEDOR DE LIQUIDEZ deberá aplicar las medidas técnicas y organizativas apropiadas para garantizar un nivel de seguridad adecuado al riesgo, conforme al artículo 32 del Reglamento (UE) 2016/679 (RGPD).

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sin cláusula penal / Sumisión a tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal / Sumisión a tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Sumisión a Arbitraje sin cláusula penal en caso de no ejecución voluntaria del laudo / Con cláusula penal / Sumisión a Arbitraje con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los .. folios del presente CONTRATO DE GESTIÓN DE CARTERAS, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(LA ENTIDAD)

Fdo. Don [NOMBRE Y APELLIDOS]

(EL CLIENTE)

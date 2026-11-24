---
name: custodia-administracion-valores-contrato-mer-0671
description: "Custodia y administración de valores (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Custodia y administración de valores (contrato)

> Formulario **MER-0671** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Custodia y administración de valores (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Custodia y administración de valores (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:custodia-administracion-valores-contrato-mer-0671`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº

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

CONTRATO DE CUSTODIA Y ADMINISTRACIÓN DE VALORES

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

Constituye el objeto de este contrato la custodia y administración de valores e instrumentos financieros representados mediante títulos físicos o mediante anotación en cuenta, que el cliente determine en cada momento.

En el caso de valores e instrumentos financieros representativos de Deuda Pública Española y de valores e instrumentos financieros negociados en el mercado AIAF Renta Fija, su custodia y administración se llevará a través del Registro de Terceros de LA ENTIDAD, en su calidad de Entidad Gestora del Sistema de Deuda Pública en Anotaciones y de Entidad Miembro de AIAF, respectivamente.

Los valores e instrumentos financieros representados mediante anotación en cuenta distintos a la Deuda Pública Española y a los negociados en el Mercado AIAF Renta Fija, serán custodiados y administrados por la CONFEDERACIÓN ESPAÑOLA DE CAJAS DE AHORRO (CECA), a través de su Registro de Terceros. Los títulos físicos, cuando existan, serán custodiados en la Cámara de Valores de CECA.

Para realizar la operativa de liquidación y custodia en los distintos mercados internacionales, CECA usa subcustodios, empleando cuentas globales cuando viene exigido por la operativa habitual de negociación por cuenta ajena en el correspondiente mercado extranjero. Para la designación de estos subcustodios, CECA tiene en cuenta que dichas entidades cumplan rigurosamente los siguientes requisitos y practicas de mercado: a) Ser entidades de reconocido prestigio; b) Contar con experiencia y solvencia a nivel mundial para realizar esta actividad; c) Tener su sede en países con reglamentación y supervisión específica en materia de tenencia y custodia de instrumentos financieros; y d) Contar con elevados volúmenes de custodia en sus mercados de referencia.

Sin perjuicio de lo anterior, se advierte al CLIENTE que la utilización de cuentas globales puede conllevar la restricción temporal en la disponibilidad, deterioro del valor o incluso pérdida de los instrumentos financieros de su propiedad, o de los derechos derivados de los mismos, como consecuencia de riesgos específicos, legales y operacionales. Asimismo, se informa al CLIENTE que en caso de estar la cuenta global abierta en un Estado no miembro de la Unión Europea, sus derechos sobre los valores, instrumentos financieros y fondos pueden ser distintos en materia de propiedad e insolvencia, a los que le corresponderían si estuvieran sujetos a la legislación de un Estado miembro.

En virtud de lo anterior, el CLIENTE autoriza la custodia y administración de sus valores extranjeros mediante la utilización de las citadas cuentas globales. Las entidades en las que se mantienen, a través de CECA, cuentas globales se indican al final de este documento junto a su calidad crediticia (rating) y demás datos que ahí se contienen. Dicha información se mantendrá actualizada a través de la web de LA ENTIDAD www

Obligaciones de la entidad

Son obligaciones de LA ENTIDAD, entre otras, las siguientes:

a) La guarda y custodia de los valores e instrumentos financieros, de los que no podrá hacer uso sino en provecho del CLIENTE;

b) La restitución de los valores e instrumentos financieros custodiados de acuerdo con las normas vigentes, cuando a ello fuese requerido por el CLIENTE.

c) La administración de los valores e instrumentos financieros, entendiéndose comprendidos en tal administración, según proceda atendiendo al tipo de valor de que se trate, las siguientes funciones:

- El cobro de intereses, dividendos y primas por asistencia a Juntas.

- El pago de dividendos pasivos, previa provisión de fondos suficientes por parte del CLIENTE.

- La recogida de acciones entregadas en los casos de ampliación de capital, cuando ello fuera pertinente.

- El cobro de amortizaciones y recogida de títulos canjeados.

- Y, en general, la realización de cuantos actos fueran necesarios o convenientes para la conservación de los derechos que correspondan a los valores e instrumentos financieros custodiados, así como a tener informado al CLIENTE de todo lo referente a los mismos.

d) LA ENTIDAD remitirá al CLIENTE las liquidaciones de las respectivas operaciones, una vez realizadas, por correo, a no ser que las partes acuerden otro medio. Los extractos de Cuenta de Valores serán remitidos por el mismo medio, cada vez que se efectúe un movimiento que altere su saldo anterior y, en cualquier caso, con periodicidad anual.

e) Cualesquiera otras acordadas en este contrato o impuesta por la legislación vigente.

f) LA ENTIDAD mantendrá registros internos que permitan conocer en todo momento y sin demora la posición de valores y operaciones en curso del CLIENTE. Los valores e instrumentos financieros depositados estarán materializados de acuerdo a sus características, quedando autorizada LA ENTIDAD para cambiar dicha materialización cuando así sea necesario para la conservación de los mismos.

Obligaciones del cliente

Son obligaciones del CLIENTE:

a) Abonar a LA ENTIDAD la retribución pactada.

b) Tener una cuenta corriente vinculada a este contrato en la que se recojan cuantos cobros y pagos dimanen de los valores e instrumentos financieros custodiados y del presente contrato.

c) Efectuar las adecuadas provisiones de fondos en la cuenta vinculada para hacer frente a las obligaciones que se derivan del presente contrato.

d) El CLIENTE se compromete a dar conformidad o formular reparos a los extractos y liquidaciones que le envíe LA ENTIDAD, en el plazo de quince días naturales desde la fecha de recepción de aquellos; LA ENTIDAD informa que, en otro caso, podría llegar a entenderse que presta su conformidad a unos y otros.

e) Cualesquiera otras acordada en este contrato o impuesta por la legislación vigente.

Subdepósito

En el caso de que LA ENTIDAD lo estime conveniente para su mejor administración, podrá subdepositar los valores e instrumentos financieros en otra entidad de depósito, para lo que el CLIENTE autoriza expresamente a LA ENTIDAD, comprometiéndose a otorgar los documentos necesarios si ello fuese pertinente. LA ENTIDAD, en caso de que ejercite esta facultad de subdepósito, no quedará en ningún caso exonerada de la responsabilidad que asume con la formalización de este contrato.

Las operaciones, financieras o no, que sean anunciadas por las entidades emisoras de los valores e instrumentos financieros custodiados o administrados que confieran derechos preferentes a su CLIENTE o requieran su conformidad (enajenar derechos de suscripción no ejercitados antes de su decaimiento, atender desembolsos de dividendos pasivos, suscribir ampliaciones de capital liberadas, acudir a las ofertas públicas de adquisición para su exclusión, por ejemplo), serán comunicadas por LA ENTIDAD, por escrito, estableciendo un plazo para su respuesta, cuya amplitud estará en función del determinado por las Entidades Emisoras o las Entidades Agentes designadas por éstas, en las respectivas operaciones. Las instrucciones del CLIENTE serán atendidas, siempre que sean recibidas dentro del plazo fijado por LA ENTIDAD y previa la provisión de fondos, si procediese. En los casos de no recibir respuesta, se tomará la decisión que más convenga a los intereses del CLIENTE, conforme a las normas de la Comisión Nacional del Mercado de Valores.

Responsabilidad

LA ENTIDAD actuará con la diligencia debida para cumplimentar las órdenes del CLIENTE, y conseguir que los valores e instrumentos financieros custodiados en esta cuenta conserven el valor y los derechos que les correspondan, sin que sea responsable por los perjuicios que pudieran originarse debidos a una administración no suficientemente eficiente por causas imputables al CLIENTE, falta de provisión de fondos en los supuestos en que proceda y por causas externas de fuerza mayor.

Comisiones

La custodia, administración o llevanza de los valores e instrumentos financieros, cualquiera que sea su materialización, devengará a favor de LA ENTIDAD las comisiones indicadas en las condiciones particulares, las cuales no exceden de las máximas previstas en el folleto de la Tarifa de Comisiones, Condiciones y Gastos Repercutibles a Clientes que LA ENTIDAD tiene comunicadas tanto al Banco de España como a la Comisión Nacional del Mercado de Valores, y publicadas, haciéndose entrega al CLIENTE en este acto del folleto parcial de tarifas máximas en operaciones y servicios del Mercado de Valores.

LA ENTIDAD podrá modificar dichas comisiones si bien tendrá la obligación de comunicar al CLIENTE las nuevas tarifas, indicando el plazo de su entrada en vigor, que no será inferior a dos meses desde la fecha de su recepción por aquel, a no ser que sean de forma clara más favorables al CLIENTE, en cuyo caso se aplicarán de forma inmediata. Estas modificaciones se efectuarán siguiendo el procedimiento en la Circular del Banco de España 5/2012, de 27 de junio, en la Circular de la Comisión Nacional del Mercado de Valores 7/2011, de 12 de diciembre y normativa concordante.

Pluralidad de titulares

La cuenta de valores podrá abrirse a nombre de uno o varios titulares. Si la cuenta se abre a nombre de varios titulares, estos deberán expresar su carácter de mancomunado o indistinto. Si no se especifica su carácter, la cuenta se entenderá abierta indistintamente.

En el supuesto de que la cuenta tenga carácter mancomunado, se requerirá la firma de todos sus titulares para efectuar cualquier acto, implique o no disposición.

En el supuesto de que la cuenta tenga carácter indistinto, los titulares se autorizan mutuamente para que cualquiera de ellos, mediante su firma, pueda ejercitar por sí solo, todos los derechos dimanantes de este contrato.

Disposiciones de valores e instrumentos financieros

Para vender, constituir derechos reales y en general para cualquier acto que implique disposición de los valores e instrumentos financieros, total o parcialmente, o de los derechos vinculados a los mismos, será necesario cursar la orden por escrito, debidamente firmada por el CLIENTE o por todos los titulares en el caso de que la cuenta esté abierta con carácter mancomunado.

En el caso de que la cuenta esté abierta con carácter indistinto, los titulares en virtud del presente contrato se autorizan recíproca e indistintamente a efectos de que cualquiera de ellos, pueda dar a LA ENTIDAD cualquier orden de compra o de venta de valores e instrumentos financieros en nombre y representación de todos los titulares del contrato, y en general efectuar o dar instrucciones para que se realice cualquier acto de disposición en relación a los valores e instrumentos financieros custodiados o que se custodien en el futuro, quedando obligados frente a LA ENTIDAD, de forma solidaria, al cumplimiento de todas las obligaciones derivadas de las operaciones que se realicen por cualquiera de los titulares.

Fallecimiento del cliente

En caso de fallecimiento del CLIENTE o de alguno de los titulares de la cuenta de valores, los herederos, legatarios o ejecutores testamentarios del fallecido no podrán disponer de los valores, total o parcialmente, mientras no acrediten su derecho a suceder al causante o a disponer de los mismos, una vez cumplidas las disposiciones fiscales..

Descubiertos en cuenta vinculada

Si como consecuencia de las operaciones originadas por la cuenta de valores se produjera descubierto en la cuenta vinculada, LA ENTIDAD, previo aviso al CLIENTE con tres días de antelación, queda autorizada para cargar dicha operación en cualquiera de las cuentas que figuren abiertas a nombre del mismo, con independencia de la moneda en que estén denominadas, lo que incluye cuentas en moneda extranjera previa su conversión, también podrá LA ENTIDAD, previo aviso al CLIENTE, vender los valores e instrumentos financieros custodiados para hacer frente al importe adeudado, siempre que exista equivalencia con el grupo de titularidad e intentando minimizar los perjuicios para el CLIENTE.

Duración del contrato

La duración del presente contrato es indefinida, pudiendo cualquiera de las partes unilateralmente dar por finalizado el mismo en cualquier momento de su vigencia, mediante la correspondiente comunicación en la que habrá de señalarse e identificarse la(s) entidad(es) financiera(s) y las cuentas a nombre del cliente correspondientes, en las que éste podrá disponer de los valores, instrumentos financieros y efectivo que integren el patrimonio gestionado cuyo contrato es objeto de resolución.

Cuando la vigencia del contrato se desee interrumpir a voluntad de la ENTIDAD será necesario un preaviso de 15 días.

Efectos de la terminación del contrato

Una vez resuelto el contrato, la ENTIDAD rendirá y dará razón de las cuentas de gestión en un plazo máximo de 15 días.

En el caso de extinción anticipada del contrato, la ENTIDAD sólo tendrá derecho a percibir las comisiones por las operaciones realizadas pendientes de liquidar en el momento de la resolución del contrato y la parte proporcional devengada de las tarifas correspondientes al período iniciado en el momento de finalización del contrato.

La cancelación anticipada del contrato no afectará a la tramitación, liquidación y cancelación de las operaciones en curso que se hubiesen concertado con anterioridad a la comunicación, que seguirán rigiéndose por las condiciones a ellas aplicables, de acuerdo con las estipulaciones del presente contrato.

A partir de la comunicación efectiva de resolución anticipada del contrato, El CLIENTE dispondrá de su patrimonio de forma directa e inmediata en las cuentas de valores, instrumentos financieros y efectivo señaladas al efecto, y la ENTIDAD recabará instrucciones expresas del CLIENTE para cualquier otra operación. No obstante, cuando por el carácter extraordinario o urgente de las circunstancias no pudieran recabarse instrucciones del CLIENTE y fuese imprescindible la actuación de la ENTIDAD para mantener el valor de la cartera del CLIENTE, la ENTIDAD realizará las operaciones necesarias dando cuenta al CLIENTE de forma inmediata.

Confidencialidad

Los términos de este Contrato así como cualquier información transmitida al amparo de lo previsto en el mismo serán confidenciales y no podrán ser revelados a terceros sin el previo consentimiento escrito de la otra Parte, salvo en caso de que la información sea de dominio público y en los restantes supuestos previstos en la legislación vigente y en el presente Contrato.

Protección de datos

En el caso de que la prestación de los Servicios suponga la necesidad de acceder a datos de carácter personal, las Partes quedan obligadas al cumplimiento de la LO 3/2018, de 5 diciembre de Protección Datos Personales y Garantías de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable. LA ENTIDAD responderá, por tanto, de las infracciones en que pudiera incurrir en el caso de que destine los datos personales a otra finalidad, los comunique a un tercero, o en general, los utilice de forma irregular, así como cuando no adopte las medidas correspondientes para el almacenamiento y custodia de los mismos. A tal efecto, se obliga a indemnizar por cualesquiera daños y perjuicios que sufra directamente, o por toda reclamación, acción o procedimiento, que traiga su causa de un incumplimiento o cumplimiento defectuoso por parte de LA ENTIDAD de lo dispuesto tanto en el Contrato como lo dispuesto en la normativa reguladora de la protección de datos de carácter personal.

A los efectos de la LO 3/2018, LA ENTIDAD únicamente tratará los datos de carácter personal a los que tenga acceso conforme a las instrucciones del CLIENTE y no los aplicará o utilizará con un fin distinto al objeto del Contrato, ni los comunicará, ni siquiera para su conservación, a otras personas. En el caso de que LA ENTIDAD destine los datos a otra finalidad, los comunique o los utilice incumpliendo las estipulaciones del Contrato, será considerado también responsable del tratamiento, respondiendo de las infracciones en que hubiera incurrido personalmente.

LA ENTIDAD deberá adoptar las medidas de índole técnica y organizativas necesarias que garanticen la seguridad de los datos de carácter personal y eviten su alteración, pérdida, tratamiento o acceso no autorizado, habida cuenta del estado de la tecnología, la naturaleza de los datos almacenados y los riesgos a que están expuestos, ya provengan de la acción humana o del medio físico o natural. A estos efectos el PROVEEDOR DE LIQUIDEZ deberá aplicar las medidas técnicas y organizativas apropiadas para garantizar un nivel de seguridad adecuado al riesgo, conforme al artículo 32 del Reglamento (UE) 2016/679 (RGPD).

Procedimiento de reclamaciones

LA ENTIDAD informa de que ante el Departamento de Atención al Cliente sito en [LOCALIDAD] (dirección), el CLIENTE, podrá someter cualquier incidencia surgida en relación con este contrato, y ejercitar los derechos de acceso, rectificación, cancelación y oposición, de sus datos personales incorporados a ficheros titularidad de LA ENTIDAD.

Igualmente el CLIENTE podrá dirigir sus reclamaciones ante la Comisión Nacional del Mercado de Valores.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sin cláusula penal / Sumisión a tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal / Sumisión a tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Sumisión a Arbitraje sin cláusula penal en caso de no ejecución voluntaria del laudo / Con cláusula penal / Sumisión a Arbitraje con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE CUSTODIA Y ADMINISTRACIÓN DE VALORES, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(LA ENTIDAD)

Fdo. Don [NOMBRE Y APELLIDOS]

(EL CLIENTE)

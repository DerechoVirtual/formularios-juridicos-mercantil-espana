---
name: contrato-tipo-deposito-administracion-valores-titulos-mer-0667
description: "Contrato tipo de depósito y administración de valores en títulos o anotaciones en cuenta. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato tipo de depósito y administración de valores en títulos o anotaciones en cuenta

> Formulario **MER-0667** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato tipo de depósito y administración de valores en títulos o anotaciones en cuenta» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato tipo de depósito y administración de valores en títulos o anotaciones en cuenta” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-tipo-deposito-administracion-valores-titulos-mer-0667`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO
- [ ] DÍA
- [ ] LOCALIDAD
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

CONTRATO TIPO DE DEPÓSITO Y ADMINISTRACIÓN DE VALORES REPRESENTADOS EN FORMA DE TÍTULOS O ANOTACIONES EN CUENTA

En [LOCALIDAD] a, [DÍA] de [MES] de 20 [AÑO]

EXPONEN

Ambas partes están interesadas en la apertura de una cuenta de valores por el CLIENTE en la ENTIDAD para el depósito de los valores representados en títulos y para la administración de los valores representados por medio de anotaciones en cuenta.

De conformidad con el art. 76 RD 217/2008, de 15 febrero, sobre régimen jurídico de las empresas de servicios de inversión, así como de la Circular 1/1996, de 27 de marzo, de la Comisión Nacional del Mercado de Valores, sobre normas de actuación, transparencia e identificación de los clientes en las operaciones del Mercado de Valores, y el Texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios (RDLeg 1/2007, de 16 noviembre), es preceptivo, para la prestación de ese servicio, la suscripción entre las partes de un contrato-tipo, previamente comprobado por la Comisión Nacional del Mercado de Valores, puesto que el valor nominal de los valores propiedad del CLIENTE y objeto de la referida cuenta es inferior 120.202 euros y el CLIENTE no tiene la condición de entidad financiera.

A tales efectos, la ENTIDAD ha elaborado el presente contrato-tipo habiéndolo oportunamente comunicado a la Comisión Nacional del Mercado de Valores, la cual, previa comprobación de que se ajusta a la regulación anteriormente indicada, lo ha puesto a disposición del público.

Habiendo concretado las condiciones en que se producirá la apertura de cuenta y el depósito y administración de los valores registrados en la misma, y reconociéndose mutuamente capacidad al efecto, las partes suscriben el presente contrato, de acuerdo con las siguientes

CLÁUSULAS

Objeto del contrato

1.1. El presente contrato regula las condiciones de depósito y administración, por parte de la ENTIDAD, de valores propiedad del CLIENTE que, en la fecha de este contrato o en cualquier momento posterior, éste mantenga en su cuenta abierta en la ENTIDAD.

1.2. La ENTIDAD está obligada a custodiar los valores representados mediante títulos y a mantener, en su caso, la inscripción, previamente practicada, de los valores representados mediante anotaciones en cuenta.

Administración del depósito de valores

2.1. La ENTIDAD realizará todos aquellos actos y operaciones ordenados expresa- mente por el titular en relación con los valores objeto del contrato-tipo de depósito o administración.

2.2. De no recibir con la debida antelación instrucciones escritas en contrario, la ENTIDAD queda autorizada a realizar, por cuenta del titular, todos aquellos actos y operaciones incluidos dentro del funcionamiento habitual de una administración de depósitos de valores, a fin de que los valores depositados o administrados conserven los derechos que les corresponden, de conformidad con las disposiciones legales aplicables. Entre estas operaciones, y a título enunciativo, la ENTIDAD se ocupará:

a) Del cobro de los intereses o dividendos correspondientes, o del principal en caso de reembolso parcial o amortización total, con la presentación o entrega de los títulos, si se trata de valores que adoptan dicha forma de representación y, en su caso, cancelación de la inscripción correspondiente, conforme a la normativa vigente, si se trata de valores representados mediante anotaciones en cuenta.

Las cantidades percibidas serán abonadas en la cuenta asociada que ha sido señalada por el titular en el Apartado II de este contrato-tipo. Dicha cuenta asociada se regulará por las condiciones convenidas en el contrato formalizado para su apertura.

b) De atender las operaciones obligatorias, tales como presentación de títulos a canjes, cambios, estampillados por aumento o disminución de capital, cuando proceda, o pago de los dividendos pasivos correspondientes, previa provisión de fondos a tal fin.

c) De comunicar al titular las operaciones voluntarias o potestativas, como el posible ejercicio de derechos de suscripción preferente, solicitando las instrucciones oportunas, que deberán llegar a poder de la ENTIDAD, como mínimo, con un margen de dos días hábiles de negociación en el mercado donde coticen antes de la finalización de la operación de que se trate, para que ésta pueda ser cumplimentada dentro de los plazos que se señalen; de no ser así, la ENTIDAD queda autorizada para vender los derechos correspondientes a suscripciones de valores con desembolso en efectivo, si fueran negociables y hubiera mercado, o a recoger los nuevos valores procedentes de asignación gratuita, con venta correlativa de los derechos sobrantes, como en el caso anterior.

En relación con todos estos actos, la ENTIDAD no será responsable de cualquier error u omisión que pueda producirse por causa imputable al titular y que no se hiciera subsanar en tiempo oportuno por éste.

2.3. La ENTIDAD asume las obligaciones anteriormente mencionadas, respecto a las operaciones a las que se refiere, siempre que sean hechas públicas de forma oficial por la Entidad emisora, o en forma privada en el caso de valores no negociables.

2.4. Las operaciones específicas que lo requieran, relativas a los valores (orden de compra o venta, suscripción, conversión-canje, traspasos) se instrumentarán por mediación de la Orden de Valores pertinente, la cual, además de servir para cursar las instrucciones, contendrá expresamente las condiciones o características de la operación a que se refiera. Los nuevos valores procedentes de estas operaciones quedarán incluidos, salvo indicación en contrario del titular al dar su orden, en el depósito o administración objeto de este contrato-tipo y se reflejarán en el correspondiente Extracto de la Cuenta de Valores.

Normas de actuación

3.1. La ENTIDAD desarrollará su actividad de depósito y administración procurando, en todo momento, el interés del CLIENTE ejercitando, en nombre y por cuenta del mismo, los derechos económicos que se deduzcan de los valores, realizando los cobros pertinentes, convirtiendo y canjeando los valores y, en general, activos financieros registrados en la cuenta, facilitando al CLIENTE el ejercicio de los derechos políticos de los valores, informándole de las circunstancias que conozca que afecten a los valores, desarrollando las actuaciones, comunicaciones e iniciativas exigidas para ello, pudiendo, a tales efectos, suscribir cuantos documentos sean necesarios. Los derechos económicos que se generen serán abonados por la ENTIDAD en la cuenta corriente vinculada del CLIENTE.

3.2. La ENTIDAD desarrollará las actuaciones a que se refiere el anterior apartado de esta cláusula siguiendo las órdenes dadas por el CLIENTE que se integrarán, en su caso, en el archivo de justificantes de órdenes y en el archivo de operaciones, dando lugar a las correspondientes anotaciones en la cuenta del CLIENTE.

Las órdenes recibidas de viva voz o por vía telefónica no escrita necesitarán la confirmación escrita del ordenante o persona habilitada. Se entenderá confirmada la orden cuando la ENTIDAD comunique al CLIENTE por cualquier medio escrito, incluidos el télex, fax u otros similares, la ejecución y en su caso, la liquidación de la misma según sus instrucciones, y éste no manifieste disconformidad en el plazo de 15 días, desde la recepción de dicha información por el CLIENTE. Las órdenes que se refieran a operaciones a plazo superior a tres meses se confirmarán antes de la fecha valor.

La cuenta de valores registrará cualesquiera valores del CLIENTE que sean susceptibles de llevanza por parte de la ENTIDAD, de acuerdo con la legislación española.

3.3. De no recibir instrucciones expresas del CLIENTE, la ENTIDAD adoptará las decisiones que mejor salvaguarden los intereses del CLIENTE valorando muy especial- mente la naturaleza y características de los valores y de las operaciones en cuestión. En concreto, y entre otras posibles actuaciones, la ENTIDAD enajenará los derechos de suscripción no ejercitados antes del momento de su decaimiento, acudirá a las ofertas públicas de adquisición de valores para su exclusión, atenderá los desembolsos de dividendos pasivos pendientes, con cargo a la cuenta del CLIENTE con límite del saldo de la misma y suscribirá ampliaciones de capital liberadas.

En ningún caso asumirá actuación alguna frente a un emisor en el caso de impago por éste de intereses, dividendos o amortizaciones correspondientes a los valores.

Información que ha de prestar la entidad al titular del presente contrato

4.1. La ENTIDAD suministrará puntualmente por escrito al titular la información concerniente a los valores depositados o administrados, recabando del mismo, cuando proceda, sus instrucciones específicas respecto a dichos valores.

Especialmente, a efectos de la adecuada información respecto a los valores depositados o administrados, la ENTIDAD remitirá al titular Extractos de la Cuenta de Valores detallando de forma clara y concreta las operaciones relativas a los mismos, con expresión de las denominaciones de los valores, movimientos producidos, saldos finales y saldos valorados, así como la situación de los valores. Dicha remisión se realizará inmediatamente después de constituir el depósito o administración a virtud del presente contrato-tipo, así como cada vez que el titular efectúe alguna operación que modifique o altere la composición de los valores depositados o administrados.

En todo caso, la ENTIDAD remitirá al titular, una vez al año, información clara y concreta de la situación de los valores depositados o administrados, así como detalle de las operaciones, saldos y rendimientos de sus valores. La información anual servirá, asimismo, para facilitar al titular el cumplimiento de sus obligaciones fiscales.

No obstante lo anterior, la ENTIDAD proporcionará al titular, siempre que éste lo solicite por escrito, y ello dentro del plazo legal (actualmente de seis años) durante el cual la ENTIDAD ha de conservar la información o documentos de que se trate, toda la información concerniente a las operaciones contratadas por el titular, pues la ENTIDAD llevará, a través de los procedimientos técnicos correspondientes, un registro de las operaciones realizadas y un archivo de justificantes de las órdenes recibidas, que permita al titular conocer la situación de sus valores depositados o administrados conforme a lo antes expresado.

4.2. El Extracto de la Cuenta de Valores constituye para la ENTIDAD un medio acreditativo del registro y del derecho del titular sobre los valores indicados en él, entendiéndose que el último Extracto refleja la realidad vigente en esa fecha, sustituyendo y anulando los Extractos de fechas anteriores.

Dicho Extracto es un documento nominativo e intransferible, no pudiendo ser, por tanto, objeto de transmisión o endoso, y constituye título suficiente para que el titular pueda exigir de la ENTIDAD la restitución de los valores representados mediante títulos físicos, o la transferencia contable de los valores representados mediante anotaciones en cuenta, que se hallen depositados o administrados por la ENTIDAD, aunque la presentación del mismo no sea un requisito indispensable para tal exigencia, pudiendo el titular acreditar su derecho por otros medios.

Obligaciones del cliente

El CLIENTE asume la obligación de poner en conocimiento de la ENTIDAD cualquiera de las siguientes circunstancias:

a) Modificación del domicilio, nacionalidad, estado civil y régimen económico matrimonial.

b) Solicitud o declaración de suspensión de pagos, quiebra, quita y espera y con- curso de acreedores.

c) Cualquier hecho o circunstancia que modifiquen, total o parcialmente, los datos comunicados a la ENTIDAD, por el CLIENTE, en el momento de la firma del presente contrato o con posterioridad.

El CLIENTE abonará a la ENTIDAD las tarifas correspondientes, de acuerdo con lo previsto en la cláusula sexta del presente contrato.

Comisiones y régimen económico aplicable

La ENTIDAD tendrá derecho a percibir las comisiones y a aplicar el régimen económico previsto en el Anexo 1 del presente contrato, que se devengarán en la forma que igualmente se indica en el citado Anexo 1.

La ENTIDAD hace entrega al CLIENTE de una copia de las tarifas máximas de comisiones y gastos repercutibles y normas de valoración y de disposición de fondos y valores aplicables a las operaciones que resultan del presente contrato.

La ENTIDAD hará efectivas las cantidades debidas con cargo a la cuenta corriente del CLIENTE vinculada a la cuenta de valores.

En el caso de no tener liquidez en la citada cuenta, la ENTIDAD lo pondrá en conocimiento del CLIENTE. De no producirse el pago en una semana desde el envío de la comunicación al domicilio del CLIENTE, la ENTIDAD podrá enajenar activos de la cartera para reembolsarse, siguiendo, en defecto de instrucciones del CLIENTE, el orden siguiente: Deuda Pública, renta fija nacional, renta variable, participaciones de Instituciones de Inversión Colectiva, opciones y futuros financieros, valores extranjeros de renta fija y valores extranjeros de renta variable.

Duración y terminación

El presente contrato es de duración indefinida pudiendo cualquiera de las partes dar por finalizado el mismo, en todo momento de su vigencia, con un preaviso de 15días.

Una vez finalizado, la ENTIDAD seguirá las instrucciones del CLIENTE en lo concerniente al traspaso de los valores y efectivo.

Modificación

Cualquier modificación al presente contrato deberá proponerse por escrito y ser aceptada por la otra parte.

La ENTIDAD informará al CLIENTE de cualquier modificación de las tarifas de comisiones y gastos repercutibles que puedan ser de aplicación a la relación contractual. Dicha comunicación deberá ser escrita, pudiendo incorporarse a cualquier información periódica que deba suministrarle. El CLIENTE dispondrá de un plazo de dos meses desde la recepción de la citada información para modificar o cancelar la relación contractual, sin que hasta que transcurra dicho plazo le sean de aplicación las tarifas modificadas. En el supuesto de que tales modificaciones implicaran un beneficio al CLIENTE, le serán aplicadas, inmediatamente, a las operaciones que desde entonces se concierten.

En el caso de otras modificaciones, éstas no afectarán a la tramitación, liquidación y cancelación de las operaciones que se hubiesen concertado con anterioridad a la efectividad de la modificación, que seguirá rigiéndose por las condiciones a ellas aplicables, de acuerdo con las estipulaciones del presente contrato.

Comunicaciones

Las comunicaciones entre las partes se realizarán por escrito dirigido a los domicilios de las partes que figuran en el encabezamiento del presente contrato.

Jurisdicción

Sin perjuicio del eventual ejercicio judicial de acciones, para el que las partes, con renuncia a cualquier otra que pudiera serles de aplicación, se someten a la jurisdicción y competencia de los Tribunales del lugar de otorgamiento del contrato, las partes acuerdan recabar el Informe del protector del Inversor del Mercado que corresponda de acuerdo con sus normas de procedimiento.

Y, en prueba de conformidad, las partes suscriben el presente contrato, por duplicado y en el lugar y fecha indicados en su encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

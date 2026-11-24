---
name: contrato-cuenta-corriente-bancaria-condiciones-mer-0644
description: "Contrato de cuenta corriente bancaria con condiciones generales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cuenta corriente bancaria con condiciones generales

> Formulario **MER-0644** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cuenta corriente bancaria con condiciones generales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cuenta corriente bancaria con condiciones generales” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-cuenta-corriente-bancaria-condiciones-mer-0644`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- El modelo no tiene campos marcados: Claude te preguntará lo que necesite según el caso.

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

Condiciones generales

1. Eficacia de las condiciones generales.

Las presentes condiciones generales serán aplicadas por la entidad a la contratación de las operaciones y servicios financieros que realice con los clientes, cuando así se haga constar en los documentos respectivos en los que se concierten las condiciones particulares aplicables a cada una de esas operaciones y servicios.

2. Titularidad de la cuenta.

Cuando se establezca la titularidad indistinta de la cuenta, todos los derechos y las obligaciones que se deriven de los productos o servicios que se contraten podrán ser ejercitados o, en su caso, podrán ser exigidos a cualquiera de los titulares de forma solidaria, no obstante lo que dispongan las Leyes al respecto. En las cuentas indistintas, la entidad podrá abonar los ingresos realizados por o a favor de cada uno de los titulares de forma individual.

El fallecimiento de alguno de los titulares, ha de ser comunicado inmediatamente a la entidad por sus herederos o por el resto de titulares. Serán de exclusiva responsabilidad del ordenante las órdenes que se hayan realizado desde el momento de la defunción hasta que ésta se haya comunicado a la entidad. Desde el conocimiento del fallecimiento, la entidad puede retener la cantidad necesaria para el cumplimiento de las obligaciones fiscales que se deriven, hasta que quede acreditado de forma suficiente que se ha dado cumplimiento a tales obligaciones.

3. Compensación de cuentas.

La entidad queda autorizada de forma expresa, sin necesidad de requerimiento previo, para compensar los saldos deudores con los acreedores o para retener los saldos acreedores de otras cuentas a la vista o a plazo que los titulares ostenten en la entidad.

También, queda autorizada para detraer las cantidades correspondientes a abonos o adeudos que se hubieran realizado de forma errónea o condicional.

4. Liquidez.

Las partes contratantes acuerdan la liquidez y exigibilidad de la cantidad que resulte de la liquidación efectuada por la entidad en el modo establecido en los respectivos contratos de productos y servicios financieros. El saldo que resulte de la contabilidad de la entidad, siempre que haya sido liquidado en el modo pactado por las partes en cada una de las operaciones, prevalece sobre cualquier otro posible saldo.

5. Intereses, comisiones y gastos.

La entidad ha de entregar a los titulares de la cuenta una copia de estas condiciones generales, de los epígrafes del folleto de las tarifas de comisiones y gastos y, en particular, las relacionadas con los productos y servicios contratados y, de igual modo, las normas de valoración aplicables.

La entidad queda facultada para modificar los tipos de interés que resulten aplicables a las cuentas, los productos y los servicios financieros, así como las comisiones y gastos correspondientes. Dichas modificaciones serán comunicadas a los titulares con antelación razonable a su aplicación. Esta comunicación podrá ser sustituida en los contratos de duración indefinida, mediante su exposición en el tablón de anuncios de todas las oficinas así como en las páginas web de la entidad, no siendo aplicables hasta que no hayan transcurrido dos meses desde su publicación.

En los supuestos en los que se trate de comisiones o gastos relativos a tarjetas o servicios de banca a distancia, la comunicación será previa e individual y las modificaciones no serán aplicables hasta que no hayan transcurrido quince días desde la comunicación. La entidad también podrá incrementar el límite señalado en las condiciones particulares de la tarjeta, en función del uso que se haga de la misma, sin que ello suponga coste alguno para el titular, quien podrá oponerse a dicho incremento.

Si los titulares muestran su desacuerdo con las nuevas condiciones, comunicándolo a la entidad dentro de los plazos establecidos, podrán resolver el contrato, en cuyo caso se aplicarían las últimas condiciones aceptadas hasta la fecha en que se ha comunicado a la entidad la disconformidad. Los titulares tienen la obligación de devolver a la entidad las tarjetas —tanto principales como adicionales— o cualquier otro medio de disposición, y reembolsar a la entidad la totalidad de las cantidades debidas por el uso de los mismos. La entidad, por su parte, devolverá a los titulares de las cuentas asociadas a las tarjetas la parte proporcional de la comisión de expedición/emisión o cuota anual percibida por el tiempo que reste hasta el vencimiento de las tarjetas. Tratándose de operaciones de valores, las modificaciones se comunicarán por escrito y entrarán en vigor una vez transcurridos dos meses desde la notificación.

Las modificaciones relativas a los tipos de interés, comisiones y gastos que supongan un beneficio para el titular, surtirán efecto desde la fecha en que el banco decida su aplicación. Todos los cargos y abonos que se produzcan en relación a las operaciones derivadas de los depósitos o servicios que hayan sido contratados, incluidos los intereses, comisiones y gastos, se contabilizarán en la cuenta corriente asociada a los titulares.

6. Domicilio y comunicaciones.

La entidad enviará con carácter periódico al titular la información a que esté obligada conforme a la normativa vigente, así como cualquier otra que considere de su interés. La entidad realizará estas comunicaciones mediante escrito dirigido al domicilio del titular, que figure en las condiciones particulares o a través de su dirección de correo electrónico, si así lo solicita el cliente, considerándose recibidas sin más requisitos. Cualquier modificación o cambio que se produzca en el domicilio o dirección de correo electrónico proporcionados deberá ser comunicado por escrito a la entidad, quedando ésta liberada de cualquier responsabilidad hasta la realización de la notificación efectiva. En el supuesto de que se produzca el traslado del domicilio al extranjero, los titulares deberán designar a los efectos de los contratos firmados con la entidad un domicilio en España. En defecto de éste, se entenderá como tal el señalado en las condiciones particulares de los contratos o el último que se hubiera comunicado.

La entidad no queda obligada a cumplir órdenes de pago tramitadas por fax. Sí se admiten las órdenes cursadas por vía telefónica o electrónica con clave de autenticidad convenida; la entidad no se hace responsable de los daños y perjuicios derivados de los retrasos o deficiencias de los servicios de comunicaciones implicados o de otras causas de fuerza mayor.

7. Tratamiento de datos de carácter personal.

Los contratantes quedan informados y prestan su consentimiento para que los datos de carácter personal se incorporen a los ficheros de la entidad, autorizándola para el tratamiento de los mismos con el fin de utilizarlos en relación con el desarrollo y ejecución de este contrato. Los contratantes, asimismo, prestan su consentimiento a la entidad para que por cualquier medio de comunicación, incluido el correo electrónico o a través de otro medio de comunicación electrónica equivalente, envíe comunicaciones comerciales, en particular, publicitarias, ofertas promocionales, juegos promocionales o concursos, relativas a otros productos y servicios financieros, de inversión y otros propios de la entidad, autorizando la comunicación de sus datos, para fines idénticos, a la empresas del grupo dedicadas al ámbito financiero, en la forma y con las limitaciones que se contienen en la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y Garantía de Derechos Digitales y en la Ley 34/2002, de 11 de julio, de servicios de la sociedad de la información y del comercio electrónico.

Los contratantes quedan informados de que conforme a la normativa señalada pueden ejercitar en cualquier momento sus derechos de acceso, rectificación, cancelación y oposición de sus datos de carácter personal y de la cesión de estos últimos en los términos y con las finalidades descritas, así como la revocación de la autorización concedida para recibir por cualquier medio, incluida la vía electrónica, información relativa a las comunicaciones comerciales a las que se hace referencia en el anterior párrafo. Se comunica a estos efectos que se designa como responsable del fichero a la entidad. Por su parte, los contratantes declaran que toda la información proporcionada es veraz, autorizando a la entidad para realizar todas las comprobaciones que considere oportunas, así como a solicitar a la central de información de riesgos del Banco de España y a cualquier otro fichero de solvencia patrimonial y crédito, los datos que puedan existir acerca de sus operaciones activas con otras entidades de crédito. Los contratantes autorizan a la entidad para el tratamiento de sus datos con la finalidad de evaluar el riesgo crediticio.

8. Tributos y gastos.

Serán de cuenta de los titulares de forma exclusiva todos los tributos y gastos tanto judiciales como extrajudiciales que se originen como consecuencia de la formalización de los contratos sobre productos o servicios financieros y del surgimiento, cumplimiento o extinción de las obligaciones que se deriven de los mismos, con exigibilidad desde la fecha en que se generen.

9. Apertura de cuenta.

En la cuenta que la entidad proceda a abrir a nombre de los titulares, quedarán acreditadas las cantidades que tanto éstos como terceros entreguen para su abono y se adeudarán las órdenes de cargo que hayan sido aceptadas por la entidad y las disposiciones de fondos realizadas tanto por los titulares personalmente, como a través de cajeros automáticos o por cualquier otro medio acordado entre el titular y la entidad. Quedarán, además, contabilizados los importes relativos a los intereses, comisiones y gastos que se recogen en las condiciones particulares de la cuenta. En el caso de que los titulares entreguen a la entidad documentos en gestión de cobro o descuento, para su abono en cuenta, los titulares autorizan a la entidad en que se encuentra domiciliado el pago de los documentos cedidos para que, actuando por su cuenta e interés, requieran el pago a los obligados que resulten por razón de dichos documentos para el caso de que éstos resulten impagados, permitiendo la solicitud de información sobre solvencia patrimonial y crédito, en relación a los incumplimientos relativos a los documentos cedidos. Los titulares se obligan a comunicar de forma inmediata a la entidad el pago que se haya producido de la deuda por el obligado, asumiendo las responsabilidades que pudieran derivarse del incumplimiento de tal obligación y, en consecuencia del mantenimiento inexacto de datos en los ficheros de los prestadores de servicios que anteriormente se han indicado.

Los titulares podrán igualmente disponer de los fondos a través de reintegros de efectivo, cheques, tarjeta, transferencias o a través de cualquier otro medio autorizado. Los cheques, pagarés y medios de disposición se guardarán en lugar seguro, debiendo su robo o extravío ser denunciado a las autoridades correspondientes e inmediatamente a la entidad.

Los titulares asumen, de forma expresa, la obligación de mantener en todo momento la provisión de fondos necesaria para atender a los cargos correspondientes. En el caso de que el saldo sea insuficiente, la entidad se reserva el derecho a aceptar cargos en la cuenta. En caso de descubierto, éste habrá de ser reintegrado a la entidad de forma inmediata por los titulares sin necesidad de previo requerimiento. Al descubierto producido, se la aplicará el tipo de interés nominal hecho público por la entidad, con carácter periódico y en las fechas señaladas en las condiciones particulares, más la comisión de descubierto indicada en tales condiciones, calculada sobre el mayor saldo descubierto que se haya producido en la cuenta en cada periodo de liquidación.

Las comisiones se harán efectivas en las mismas fechas en que se proceda a la liquidación periódica de la cuenta.

10. Información de la entidad.

La entidad ha de informar periódicamente a los titulares, proporcionándoles un extracto de la cuenta, salvo que aquéllos hayan optado por expedición de libreta. Proporcionará, igualmente, detalle de las liquidaciones realizadas, que serán de la conformidad de los titulares si éstos no reclaman en el plazo de los dos meses posteriores a la notificación de la liquidación.

11. Liquidación de intereses.

Para la liquidación de intereses se utilizará la fórmula del interés simple (i: c.r.t: 36.500) que se calculará sobre los saldos mantenidos (medios o diarios), siendo i= intereses devengados, c = los saldos mantenidos, r = tipo de interés nominal y t = los días de permanencia, salvo los años bisiestos en cuyo caso el divisor será 36.000.

12. Tasa Anual Equivalente (TAE) La Tasa Anual Equivalente se calculará de acuerdo con la Circular 5/2012, de 27 de junio, sobre entidades de crédito y proveedores de servicios de pago, sobre transparencia de los servicios bancarios y responsabilidad en la concesión de préstamos.

13. Duración.

La cuenta tendrá carácter indefinido y podrá ser resuelta unilateralmente por cualquiera de la partes. Si la resolución es por decisión de los titulares no se requiere más que su manifestación en tal sentido. Si por voluntad de la entidad, será necesario un preaviso de ocho días dirigido a cualquiera de los titulares. A partir de la fecha de la cancelación de la cuenta, si resulta un saldo deudor a favor de la entidad, éste se considerará vencido, líquido y exigible debiendo reembolsarse inmediatamente por los titules, sin perjuicio del posible devengo de intereses moratorios. En el caso de que el saldo resultante fuese a favor de los titulares, quedará a su disposición sin generar intereses.

Cualquiera que fuese el motivo de la cancelación de la cuenta, quedan los titularse obligados a devolver a la entidad los cheques, pagarés o libretas no utilizados, así como tarjetas, documentos u otros medios de pago que le hayan sido facilitados.

14. Libreta.

En el supuesto de la que entidad entregue al titular una libreta, ésta será personal e intransferible. Esta deberá custodiarse en lugar seguro y su robo o extravío deberá ser comunicado con la mayor brevedad posible en atención a las circunstancias del titular a la entidad y a las autoridades competentes. Los asientos que se extiendan en la libreta no serán válidos si carecen de la impresión mecánica que los autentique, tienen tachaduras o raspaduras o si carecen de la firma de los apoderados de la entidad.

El/Los TITULARES / ENTIDAD P.P.

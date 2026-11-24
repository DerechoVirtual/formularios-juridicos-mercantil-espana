---
name: escritura-prestamo-garantia-hipotecaria-mer-0624
description: "Escritura de préstamo con garantía hipotecaria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de préstamo con garantía hipotecaria

> Formulario **MER-0624** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de préstamo con garantía hipotecaria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de préstamo con garantía hipotecaria” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:escritura-prestamo-garantia-hipotecaria-mer-0624`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] PORCENTAJE (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] FECHA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] CALLE (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DATO REGISTRAL
- [ ] DOMICILIO
- [ ] DÍA Y MES
- [ ] FOLIO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] OTROS DATOS
- [ ] PLAZO
- [ ] TIPO DE INTERÉS
- [ ] TOMO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 23 Ley 5/2019
- art. 23.8 Ley 5/2019
- art. 6 Real Decreto 309/2019

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

En [LOCALIDAD], a [DÍA Y MES] de 20

Comparecientes

De una parte la ENTIDAD, representada por [ÓRGANO O PERSONA] (detallar), D./D.ª [NOMBRE Y APELLIDOS], constituida en escritura pública otorgada el día [FECHA] ante Notario de [LOCALIDAD] D./D.ª [NOMBRE Y APELLIDOS] e inscrita en el Registro Mercantil de [LOCALIDAD] Libro [DATO REGISTRAL] Tomo [TOMO] Folio [FOLIO] domiciliada en [DOMICILIO] calle [CALLE]. núm [NÚMERO] y con CIF núm

De otra, D./D.ª [NOMBRE Y APELLIDOS], actuando por cuenta propia /actuando en representación de [NOMBRE DEL REPRESENTADO/A] (en adelante el CLIENTE PRESTATARIO), mayor de edad, con domicilio en [LOCALIDAD] calle [CALLE]. núm [NÚMERO] y con CIF núm

Ambas partes se reconocen con carácter mutuo y tienen capacidad legal suficiente para otorgar el presente contrato de préstamo hipotecario, manifestando el PRESTATARIO haber recibido con la debida antelación la ficha de advertencias estandarizadas (FiAE) del anexo II de la Orden EHA/2899/2011, de 28 de octubre, de transparencia y protección del cliente de servicios bancarios, modificada por Orden ECE/482/2019, de 26 de abril, así como haberse cumplido las normas de transparencia del crédito inmobiliario, según consta en el acta extendida por el Notario D…………., en fecha …………, número de protocolo………… de asesoramiento individual del CLIENTE PRESTATARIO, por lo que conciertan el referido contrato, conforme a las siguientes cláusulas:

Cláusulas

1. Importe del préstamo hipotecario. La ENTIDAD concede al CLIENTE PRESTATARIO un préstamo que asciende a / (detallar euros en número [Nº]/[AÑO] letra), que recibe en este momento a su entera satisfacción.

2. Amortización del capital prestado. El CLIENTE PRESTATARIO se obliga a la devolución del principal prestado así como a satisfacer los intereses pactados en la cláusula siguiente, en el plazo de [PLAZO] (detallar) años, a contar desde esta fecha, mediante el pago de las cuotas fijas mensuales establecidas comprensivas de capital e intereses por importe de [IMPORTE] (detallar) € calculadas al tipo previsto y de conformidad con el cuadro de amortización convenido. El primer vencimiento tendrá lugar en la fecha de [FECHA] (detallar) y el último [FECHA] (detallar), con un número total de cuotas de a(detallar).

El CLIENTE PRESTATARIO podrá en cualquier momento anticipar total o parcialmente el pago de la cantidad adeudada y realizar el pago anticipado del capital de las cuotas más lejanas en el tiempo. En el supuesto de ser expresamente solicitado por el CLIENTE PRESTATARIO, se aplicará al capital de las amortizaciones más próximas en el tiempo, conservando el plazo pactado inicialmente, o bien, a la disminución del capital debido, conservando el préstamo el plazo inicialmente previsto, y siendo las cuotas reducidas y calculadas de nuevo en función del importe de la amortización satisfecha anticipadamente.

Para estos supuestos de amortización anticipada, la ENTIDAD podrá aplicar la comisión correspondiente conforme a las condiciones establecidas para los contratos de interés fijo que son: a) en caso de reembolso o amortización anticipada total o parcial del préstamo durante los 10 primeros años de vigencia del contrato de préstamo, se pacta una compensación o comisión a favor del prestamista que no podrá exceder del importe de la pérdida financiera que pudiera sufrir el prestamista, de conformidad con la forma de cálculo prevista en el apartado 8 del art. 23 de la Ley 5/2019, del [PORCENTAJE] ( límite 2%) por ciento del capital reembolsado anticipadamente; y b) en caso de reembolso o amortización anticipada total o parcial del préstamo desde el fin del período señalado en la letra a) hasta el final de la vida del préstamo, se pacta una compensación o comisión a favor del prestamista que no podrá exceder del importe de la pérdida financiera que pudiera sufrir el prestamista, de conformidad con la forma de cálculo prevista en el citado art. 23.8 de la Ley 5/2019, del [PORCENTAJE] (límite 1,5) por ciento del capital reembolsado anticipadamente.

Con carácter previo han de quedar íntegramente satisfechos los posibles intereses pendientes de pago y, en su caso, los de demora por ser dicho pago preferente respecto al capital.

3. Intereses del préstamo. La suma prestada como principal del préstamo hipotecario devengará a favor de la ENTIDAD PRESTAMISTA el interés nominal [TIPO DE INTERÉS] (detallar)% anual y devengable por días, utilizando la fórmula del interés simple (i: c.r.t: 36.500) que se calculará sobre los saldos mantenidos (medios o diarios), siendo i= intereses devengados; c = los saldos mantenidos, r = tipo de interés nominal y t = los días de permanencia.

Intereses de demora. Las cantidades por cuotas comprensivas de capital e intereses que no sean satisfechas por la parte prestataria a su vencimiento, devengarán desde dicho vencimiento, a favor de la ENTIDAD PRESTAMISTA, el interés de demora será el interés remuneratorio más [PORCENTAJE] (límite tres) puntos porcentuales a lo largo del período en el que aquel resulte exigible, sin necesidad de requerimiento alguno y pagadero en su caso al hacerse efectivo cualquier concepto vencido e impagado. Este devengo tendrá preferencia sobre todos los demás.

4. Tasa Anual Equivalente (TAE). La Tasa Anual Equivalente (TAE) se calculará de acuerdo con la fórmula matemática que figura en el Anexo II, epígrafe I de la Ley 5/2019, de 15 de marzo, reguladora de los contratos de crédito inmobiliario.

5. Comisiones. El CLIENTE PRESTATARIO deberá atender a las siguientes comisiones:

Comisión de apertura. (detallar)% respecto del principal prestado que engloba la totalidad de los gastos de estudio, tramitación o concesión del préstamo y otros similares inherentes a la actividad del prestamista ocasionada por la concesión del préstamo [PORCENTAJE]. Se hará efectiva de una sola vez en el momento de realizar la disposición del capital.
Comisión de amortización total o parcial en los términos pactados en la cláusula segunda.
Comisión de subrogación [PORCENTAJE] (detallar)% sobre el principal subrogado.
Comisión por reclamación de recibos vencidos [IMPORTE] (detallar) € por recibo reclamado.
Otras posibles comisiones [OTROS DATOS] (detallar)

6. Gastos y tributos. Los gastos y tributos derivados del contrato se distribuirán del siguiente modo:

Los gastos de tasación del inmueble corresponderán a prestatario y los de gestoría al prestamista.
El prestamista asumirá el coste de los aranceles notariales de la escritura de préstamo hipotecario y los de las copias los asumirá quien las solicite.
Los gastos de inscripción de las garantías en el registro de la propiedad corresponderán al prestamista.
El pago del impuesto de transmisiones patrimoniales y actos jurídicos documentados se realizará de conformidad con lo establecido en la normativa tributaria aplicable.

7. Información durante la vigencia del préstamo. LA ENTIDAD PRESTAMISTA facilitará al CLIENTE, durante la vigencia del préstamo, la información que se establece en los arts. 6 a 10 del Real Decreto 309/2019, de 26 de abril, por el que se desarrolla parcialmente la Ley 5/2019, de 15 de marzo, reguladora de los contratos de crédito inmobiliario y se adoptan otras medidas en materia financiera.

8. Resolución anticipada del contrato. La ENTIDAD PRESTAMISTA podrá proceder a declarar vencida la obligación del CLIENTE y ejecutar la hipoteca de la finca en los siguientes supuestos:

Si el inmueble hipotecado sufriera una depreciación importante de su valor a juicio del perito designado por la ENTIDAD y el CLIENTE PRESTAMISTA no aumentara la garantía a satisfacción de la ENTIDAD.
El vencimiento anticipado del contrato por impago cuando concurran conjuntamente los siguientes requisitos:
Que el prestatario se encuentre en mora en el pago de una parte del capital del préstamo o de los intereses.
Que la cuantía de las cuotas vencidas y no satisfechas equivalgan al menos:
Al tres por ciento de la cuantía del capital concedido, si la mora se produjera dentro de la primera mitad de la duración del préstamo. Se considerará cumplido este requisito cuando las cuotas vencidas y no satisfechas equivalgan al impago de doce plazos mensuales o un número de cuotas tal que suponga que el deudor ha incumplido su obligación por un plazo al menos equivalente a doce meses.
Al siete por ciento de la cuantía del capital concedido, si la mora se produjera dentro de la segunda mitad de la duración del préstamo. Se considerará cumplido este requisito cuando las cuotas vencidas y no satisfechas equivalgan al impago de quince plazos mensuales o un número de cuotas tal que suponga que el deudor ha incumplido su obligación por un plazo al menos equivalente a quince meses.
Que el prestamista haya requerido el pago al prestatario concediéndole un plazo de al menos un mes para su cumplimiento y advirtiéndole de que, de no ser atendido, reclamará el reembolso total adeudado del préstamo.
El impago de cuantas contribuciones, arbitrios, impuestos, tasas, exacciones o gastos de comunidad que afecten a las fincas hipotecadas, cuando de ello pudiere causar cualquier gravamen o afección de rango preferente a la hipoteca constituida en virtud de lo pactado en el presente contrato.
La declaración de concurso, o el embargo de los bienes del CLIENTE por su tercero, incluso la Hacienda Pública o la Seguridad Social.
El incumpliendo de los pactos recogidos en las cláusulas siguientes.
El incumplimiento de los gastos de otorgamiento y formalización y de los tributos correspondientes que conlleve la escritura hasta su inscripción en el registro de la propiedad.

10. Seguros. Durante la vigencia de este contrato, el CLIENTE PRESTATARIO se obliga a tener asegurada la finca hipotecada contra el riesgo de incendio. El CLIENTE se obliga a acreditar el pago de la prima y a no rescindir el contrato de seguro sin autorización expresa de la ENTIDAD, mientras subsista el presente contrato.

11. Reclamación judicial. Una vez que por cualquier causa haya vencido el préstamo hipotecario, para conseguir el cobro de lo que se adeuda, la ENTIDAD podrá ejercitar las acciones que están previstas en la Ley de Enjuiciamiento Civil. A tales efectos, las partes contratantes pactan de forma expresa las siguientes estipulaciones:

el valor de la finca hipotecada que servirá de base a la subasta primera es el que se consigna en la descripción efectuada en la cláusula correspondiente.
el domicilio para el CLIENTE PRESTATARIO a los efectos de notificaciones, citaciones, emplazamientos y requerimientos, será el consignado en este contrato.
el CLIENTE PRESTATARIO autoriza expresamente a la ENTIDAD para que pueda obtener copias, cuando lo precise, incluso parciales, de esta escritura. Presta igualmente su consentimiento para que las segundas copias puedan tener carácter ejecutivo y así se haga constar por el notario autorizante.
La cantidad líquida y vencida exigible por la ENTIDAD será la que se deduzca de su contabilidad, siendo los intereses vencidos por el capital amortizado y no satisfechos a la fecha de la demanda, así como los que posteriormente se generen, reclamables al tipo de demora pactado en la cláusula tercera del contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

La ENTIDAD PRESTAMISTA EL CLIENTE PRESTATARIO

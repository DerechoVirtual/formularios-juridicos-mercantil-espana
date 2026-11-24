---
name: escritura-prestamo-hipotecario-interes-variable-mer-0649
description: "Escritura de préstamo hipotecario a interés variable. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de préstamo hipotecario a interés variable

> Formulario **MER-0649** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de préstamo hipotecario a interés variable» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de préstamo hipotecario a interés variable” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:escritura-prestamo-hipotecario-interes-variable-mer-0649`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] PORCENTAJE (5 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] CALLE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PLAZO (2 veces)
- [ ] TIPO DE INTERÉS (2 veces)
- [ ] CARGAS
- [ ] COLEGIO
- [ ] DOMICILIO
- [ ] FINCA
- [ ] FOLIO
- [ ] INSCRIPCIÓN
- [ ] LIBRO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] OTROS DATOS
- [ ] REFERENCIA CATASTRAL
- [ ] TIPO DE INTERÉS DE REFERENCIA
- [ ] TOMO
- [ ] TÍTULO DE ADQUISICIÓN
- [ ] ÓRGANO
- [ ] ÓRGANO O PERSONA

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

En [LOCALIDAD] a fecha de [FECHA].

Y ante [ÓRGANO], Notario del Ilustre Colegio de [COLEGIO]

Comparecen:

De una parte, la ENTIDAD, representada por [ÓRGANO O PERSONA] (detallar), D/Dª [NOMBRE Y APELLIDOS], constituida en escritura pública otorgada el día ante Notario de [LOCALIDAD] D e inscrita en el Registro Mercantil de Libro [LIBRO] Tomo [TOMO] Folio [FOLIO] domiciliada en [DOMICILIO] calle [CALLE] núm [NÚMERO] y con CIF núm

De otra, D/Dª [NOMBRE Y APELLIDOS], actuando por cuenta propia /actuando en representación de [NOMBRE DEL REPRESENTADO/A] (en adelante el CLIENTE), mayor de edad, con domicilio en [LOCALIDAD] c/ [CALLE] núm [NÚMERO] con DNI/NIF núm

Cláusulas

1. Importe del préstamo hipotecario. La ENTIDAD concede al CLIENTE PRESTATARIO un préstamo que asciende a [IMPORTE] (detallar euros en número y letra), que recibe en este momento a su entera satisfacción.

2. Amortización del capital prestado. El CLIENTE PRESTATARIO se obliga a la devolución del principal prestado así como a satisfacer los intereses pactados en la cláusula siguiente, en el plazo de [PLAZO] (detallar) años, a contar desde esta fecha, mediante el pago de las cuotas fijas mensuales establecidas comprensivas de capital e intereses por importe de [IMPORTE] (detallar) € calculadas al tipo previsto y de conformidad con el cuadro de amortización convenido. El primer vencimiento tendrá lugar en la fecha de [FECHA] (detallar) y el último [FECHA] (detallar), con un número total de cuotas de [Nº] (detallar).

El CLIENTE PRESTATARIO podrá en cualquier momento anticipar total o parcialmente el pago de la cantidad adeudada y realizar el pago anticipado del capital de las cuotas más lejanas en el tiempo. En el supuesto de ser expresamente solicitado por el CLIENTE PRESTATARIO, se aplicará al capital de las amortizaciones más próximas en el tiempo, conservando el plazo pactado inicialmente, o bien, a la disminución del capital debido, conservando el préstamo el plazo inicialmente previsto, y siendo las cuotas reducidas y calculadas de nuevo en función del importe de la amortización satisfecha anticipadamente. Para estos supuestos de amortización anticipada, la ENTIDAD podrá aplicar la comisión correspondiente conforme a lo dispuesto en la cláusula al efecto. Con carácter previo han de quedar íntegramente satisfechos los posibles intereses pendientes de pago y, en su caso, los de demora, por ser dicho pago preferente respecto al capital.

3. Intereses del préstamo. Tipo de interés variable: el/la cliente PRESTATARIO pagará el interés pactado en la cláusula anterior hasta la fecha [FECHA] (detallar). A partir de la misma, el interés a pagar por el/la cliente será revisado para su aumento o disminución tomándose como referencia [TIPO DE INTERÉS DE REFERENCIA] (detallar tipo de referencia). Al tipo de interés resultante se le adicionará un diferencial de [PORCENTAJE] (detallar en números) %.

Será suficiente la simple notificación formal al CLIENTE PRESTATARIO para que tenga efectos la modificación del tipo de interés.

Intereses de demora: las cantidades por cuotas comprensivas de capital e intereses que no sean satisfechas por la parte prestataria a su vencimiento devengarán desde dicho vencimiento, a favor de la ENTIDAD PRESTAMISTA, el interés de demora de [PORCENTAJE] (detallar)% anual, sin necesidad de requerimiento alguno y pagadero, en su caso, al hacerse efectivo cualquier concepto vencido e impagado. Este devengo tendrá preferencia sobre todos los demás. En el supuesto de que el interés de demora resultase inferior al interés ordinario en caso de su revisión, resultará aplicable éste.

4. Tasa Anual Equivalente (T.A.E.): La Tasa Anual Equivalente se calculará de acuerdo con la Circular 5/2012, de 27 de junio, sobre transparencia de los servicios bancarios y responsabilidad en la concesión de préstamos.

5. Comisiones. El/la cliente PRESTATARIO deberá atender a las siguientes comisiones: a. Comisión de apertura [PORCENTAJE] (detallar)% respecto del principal prestado. Se hará efectiva de una sola vez en el momento de realizar la disposición del capital.

b. Comisión de amortización total o parcial [PORCENTAJE] (detallar)% sobre el principal anticipado. Se ha de hacer efectiva en el momento de la amortización.

c. Comisión de subrogación [PORCENTAJE] (detallar)% sobre el principal subrogado.

d. Comisión por reclamación de recibos vencidos [IMPORTE] (detallar) € por recibo reclamado.

e. Otras posibles comisiones [OTROS DATOS] (detallar)

6. Gastos y tributos. El CLIENTE PRESTAMISTA asume cuantos gastos e impuestos graven la finca o puedan generarse durante la vigencia del presente contrato. Asume igualmente los gastos de tasación, los notariales y registrales de constitución, modificación, cancelación de la hipoteca, los derivados de la tramitación de la escritura ante el registro de la propiedad y los tributos generados por éste hasta su total inscripción en el citado registro e, incluso, los que se generen después con carácter complementario. También, serán de su cuenta las primas derivadas de los contratos de seguro contra incendio y, en su caso, de vida. En este supuesto, la ENTIDAD podrá hacer efectivos dichos gastos por cuenta del CLIENTE, garantizándose su reintegro con la suma depositada en la ENTIDAD en cumplimiento de lo dispuesto en la cláusula núm. 9.

Corresponden igualmente al CLIENTE PRESTATARIO los gastos derivados de la cancelación de la hipoteca y todos aquellos que se generen para la ENTIDAD, si para lograr la efectividad del pago de lo adeudado es necesario ejercitar cualquier tipo de acción y procedimiento judicial, incluidos los honorarios de abogado y procurador, aun en el caso de que su intervención no fuera obligatoria, sino voluntaria.

7. Resolución anticipada del contrato. La ENTIDAD PRESTAMISTA podrá proceder a declarar vencida la obligación del CLIENTE y ejecutar la hipoteca de la finca en los siguientes supuestos: 1. Si el inmueble hipotecado sufriera una depreciación importante de su valor a juicio del perito designado por la ENTIDAD y el CLIENTE PRESTAMISTA no aumentara la garantía a satisfacción de la ENTIDAD. 2. La falta de pago a su vencimiento de [Nº] (detallar número) cuotas. 3. La falta de pago por el CLIENTE del impuesto de bienes inmuebles, así como sus recargos, establecidos por el Estado, la Comunidad Autónoma, municipio o provincia, sobre la finca hipotecada o se niegue a declarar por los motivos de la falta de estos pagos o de las primas del seguro. 4. La declaración de concurso, o el embargo de los bienes del CLIENTE por un tercero, incluso la Hacienda Pública o la Seguridad Social. 5. El incumpliendo de los pactos recogidos en las cláusulas siguientes. 6. El incumplimiento de los gastos de otorgamiento y formalización y de los tributos correspondientes que conlleve la escritura hasta su inscripción en el Registro de la Propiedad, aunque la ENTIDAD se haga cargo de dichos gastos.

8. Garantía hipotecaria. Conservación de los bienes. Derecho de inspección de la ENTIDAD PRESTAMISTA. Para garantizar la devolución del capital prestado en la suma de [IMPORTE] (detallar en número y letra) €, más los intereses debidos por los años del contrato [PLAZO] (detallar años), al tipo de interés [TIPO DE INTERÉS] (detallar) %, más la cantidad que se fija como ampliación eventual para costas y gastos [IMPORTE] (detallar), el CLIENTE PRESTATARIO constituye hipoteca a favor de la ENTIDAD sobre la finca [FINCA] (detallar), título [TÍTULO DE ADQUISICIÓN]; cargas [CARGAS]; inscripción [INSCRIPCIÓN]; referencia catastral [REFERENCIA CATASTRAL]; valor a efectos de subsanar [IMPORTE]; valor a efectos de seguro

Conforme a lo que disponen los artículos 110 y 111 de la Ley Hipotecaria, esta hipoteca se extiende a las nuevas construcciones e instalaciones que pueden llevarse a cabo o realizarse en lo sucesivo sobre la finca gravada, salvo que la finca haya pasado a un tercer poseedor y hayan sido costeadas por el nuevo dueño.

El CLIENTE PRESTATARIO se obliga a conservar la finca dada en garantía, actuando diligentemente, y a efectuar en ella las reparaciones necesarias, ordinarias y extraordinarias. También, queda obligado a realizar las comunicaciones a la ENTIDAD de cualquier evento que menoscabe el valor o el estado de la finca hipotecada. La ENTIDAD se reserva el derecho a inspeccionar la finca en cualquier momento a través de perito en la materia, a efectos de comprobar el estado de la finca y el cumplimiento de las obligaciones previstas por esta cláusula para el CLIENTE.

9. Seguros. Durante la vigencia de este contrato, el CLIENTE PRESTATARIO se obliga a tener asegurada la finca hipotecada contra el riesgo de incendio. El CLIENTE se obliga a acreditar el pago de la prima y a no rescindir el contrato de seguro sin autorización expresa de la ENTIDAD, mientras subsista el presente contrato.

10. Reclamación judicial. Una vez que por cualquier causa haya vencido el préstamo hipotecario, para conseguir el cobro de lo que se adeuda, la ENTIDAD podrá ejercitar las acciones que están previstas en la Ley de Enjuiciamiento Civil. A tales efectos, las partes contratantes pactan de forma expresa las siguientes estipulaciones: 1. el valor de la finca hipotecada que servirá de base a la subasta primera es el que se consigna en la descripción efectuada en la cláusula correspondiente. 2. el domicilio para el CLIENTE PRESTATARIO a los efectos de notificaciones, citaciones, emplazamientos y requerimientos, será el consignado en este contrato. 3. el CLIENTE PRESTATARIO autoriza expresamente a la ENTIDAD para que pueda obtener copias, cuando lo precise, incluso parciales, de esta escritura. Presta, igualmente, su consentimiento para que las segundas copias puedan tener carácter ejecutivo y así se haga constar por el notario autorizante. 4. La cantidad líquida y vencida exigible por la ENTIDAD será la que se deduzca de su contabilidad, siendo los intereses vencidos por el capital amortizado y no satisfechos a la fecha de la demanda, así como los que posteriormente se generen, reclamables al tipo de demora de [TIPO DE INTERÉS] (detallar) %.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

La ENTIDAD PRESTAMISTA EL CLIENTE PRESTATARIO

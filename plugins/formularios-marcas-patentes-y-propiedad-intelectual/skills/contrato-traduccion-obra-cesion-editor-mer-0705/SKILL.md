---
name: contrato-traduccion-obra-cesion-editor-mer-0705
description: "Contrato de traducción de una obra con cesión al editor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de traducción de una obra con cesión al editor

> Formulario **MER-0705** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Por el contrato de traducción el traductor o sus derechohabientes ceden al editor, mediante compensación económica, el derecho de reproducir su obra y el de distribuirla. El editor se obliga a realizar estas operaciones por su cuenta y riesgo en las condiciones pactadas y con sujeción a lo dispuesto en el Real Decreto Legislativo 1/1996, de 12 de abril, por el que se aprueba el texto refundido de la Ley de Propiedad Intelectual

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de traducción de una obra con cesión al editor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de traducción de una obra con cesión al editor” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-traduccion-obra-cesion-editor-mer-0705`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (13 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] DNI/NIE (4 veces)
- [ ] LENGUA (4 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] TÍTULO DE LA OBRA (2 veces)
- [ ] ÁMBITO TERRITORIAL (2 veces)
- [ ] IMPORTE
- [ ] LUGAR
- [ ] Nº DE EJEMPLARES
- [ ] PLAZO
- [ ] TIPO DE EDICIÓN

## Normas que cita el formulario

- art. 46 TRLPI
- art. 68.f Real Decreto Legislativo 1/1996

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

Por el contrato de traducción el traductor o sus derechohabientes ceden al editor, mediante compensación económica, el derecho de reproducir su obra y el de distribuirla. El editor se obliga a realizar estas operaciones por su cuenta y riesgo en las condiciones pactadas y con sujeción a lo dispuesto en el Real Decreto Legislativo 1/1996, de 12 de abril, por el que se aprueba el texto refundido de la Ley de Propiedad Intelectual


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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EDITOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, TRADUCTOR.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de traducción y, a tal fin,

MANIFIESTAN

Que el editor posee los derechos de edición en la lengua [LENGUA] de la obra [TÍTULO DE LA OBRA] de la que es autor D./Dña. [NOMBRE Y APELLIDOS] y que el traductor se compromete a llevar a cabo la correspondiente traducción al [LENGUA], por lo cual ambas partes convienen en formalizar este contrato con arreglo a los siguientes:

PACTOS

Primero.- Objeto

El editor encarga al traductor la traducción de la obra [TÍTULO DE LA OBRA] de la que es autor D./Dña. [NOMBRE Y APELLIDOS], y el traductor se obliga a realizar personalmente la traducción del [Nº] al [Nº] ajustada fielmente al original.

El traductor responde ante el editor de la autoría y originalidad de su obra y del ejercicio pacífico de los derechos que cede mediante el presente contrato, manifestando que sobre los mismos no tiene contraídos ni contraerá compromisos o gravámenes de ninguna especie que atenten contra los derechos que al editor o a terceros correspondan, de acuerdo con lo estipulado en el presente instrumento. A este respecto, el traductor se hace responsable frente al editor de todas las cargas pecuniarias que pudieran derivarse para el segundo a favor de tercero como motivo de acciones, reclamaciones o conflicto derivados del incumplimiento de estas obligaciones por parte del traductor.

Segundo.- Entrega del Texto

El texto de la traducción deberá ser entregado al editor antes del [FECHA] En su traducción se seguirán las directrices recibidas del editor.

Tercero.- Contraprestación

El editor pagará al traductor, como anticipo de los derechos que puedan corresponderles por la edición de la obra encargada, la cantidad de [IMPORTE] euros por folio que se liquidarán de acuerdo con los siguientes plazos:

— El % en el momento de la firma de este contrato.
— La cantidad restante cuando el editor dé su conformidad a la traducción.

Dicha conformidad o disconformidad deberá darla el editor en un plazo que no podrá ser superior a [Nº] días, a contar desde la fecha de su recepción.

[OPCIONAL — incluir si procede]

(No conformidad)

Si el editor no diese su conformidad a la traducción encargada y el traductor no realizase las modificaciones propuestas por el editor, éste quedará liberado de la obligación de efectuar el pago del último plazo, deberá devolver la traducción al traductor, y quedará resuelto el presente contrato.

Cuarto.- Reproducción, distribución y venta

Realizada, entregada y aceptada la traducción y pagado el anticipo por el editor, los derechos de reproducción, distribución y venta de la misma en forma de libro se ceden al editor para su explotación comercial en lengua [LENGUA] y para el ámbito territorial de [ÁMBITO TERRITORIAL].

[OPCIONAL — incluir si procede]

(Si es a tanto alzado art. 46 TRLPI)

Realizada, entregada y aceptada la traducción y pagado el tanto alzado por el editor, los derechos de reproducción, distribución y venta de la misma en forma de libro se ceden al editor para su explotación comercial en lengua [LENGUA] y para el ámbito territorial de [ÁMBITO TERRITORIAL].

Quinto.- Exclusividad

La cesión se entiende hecha con carácter no exclusivo, en cualquiera de los posibles sistemas de comercialización, para las siguientes modalidades de edición:

Sexto.- Adquisición preferente

El traductor cede al editor, que lo acepta, un derecho de opción preferente para adquirir los demás derechos de explotación (comunicación pública, transformación y colección) en iguales términos y condiciones que el autor pueda convenir con terceros.

Séptimo.- Cesión

El editor sólo podrá ceder a otro los derechos que se le ceden, con el consentimiento del traductor, expresado por escrito, previo pacto de los términos económicos de esta cesión.

Como remuneración por los derechos de autor, cuya cesión es objeto del presente contrato, el traductor percibirá:

1º. El [PORCENTAJE] % del precio de venta al público, según catálogo y sin IVA, por cada uno de los ejemplares vendidos en edición [TIPO DE EDICIÓN]
2º. Para las restantes modalidades de edición, los porcentajes que se aplicarán para determinar la remuneración del traductor serán los siguientes:

En caso de resolución de este contrato por no publicación de la obra, quedarán definitivamente en poder del traductor las cantidades anticipadas.

Octavo.- Publicación

El editor viene obligado a poner a la venta la obra en un plazo no superior a [Nº] meses a contar desde la fecha de entrega del original.

El editor se obliga a que el nombre del traductor figure, en lugar visible, en la página de créditos, así como la mención del Copyright de la traducción.

Noveno.- Ediciones y Número de ejemplares

Durante la vigencia del presente contrato, el editor podrá efectuar un máximo de [PLAZO] ediciones para cada una de ellas, con las reimpresiones que dentro de dichos totales libremente decida el editor.

[OPCIONAL — incluir si procede]

(A tanto alzado art. 46 TRLPI)

El editor queda facultado para realizar una primera y única edición de la obra que comprenderá un mínimo de [Nº] ejemplares y un máximo de [Nº] ejemplares, con las reimpresiones que dentro de dichos totales libremente decida el editor, buscando asegurar a la obra una explotación continua y una difusión comercial conforme a los usos habituales en el sector profesional al que la obra corresponda.

[OPCIONAL — incluir si procede]

(Clausula limitativa)

a) Si el mínimo es inferior a 10.000 ejemplares, el máximo de ejemplares no podrá ser superior al triple del mínimo previsto.

b) Si el mínimo oscila entre 10.000 y 50.000 ejemplares, el máximo no podrá ser superior al doble del mínimo previsto.

c) Si el mínimo es superior a 50.000 ejemplares, el máximo no podrá ser superior al 150 por 100 del mínimo).

Décimo.- Control de tirada

Antes de la puesta en circulación de los ejemplares impresos de la obra cada una de las ediciones o reimpresiones que realice el editor, éste remitirá al traductor una certificación comprensiva del número de ejemplares de que conste la edición o reimpresión de que se trate, fecha de publicación de la obra y de su precio de venta al público. Esta certificación irá acompañada de una declaración jurada de la persona o entidad responsable de los talleres de impresión y encuadernación de la obra, en la que conste el número de ejemplares fabricados que fueron entregados al editor y fecha de la entrega o entregas efectuadas.

Se considerará que está agotada la edición o reimpresión de la obra cuando el número de ejemplares sin vender sea inferior al [PORCENTAJE] % del total de la edición o reimpresión y, en todo caso, inferior a [Nº DE EJEMPLARES], circunstancia que deberá ser comunicada al traductor; cuando el traductor no haya recibido ninguna liquidación transcurridos [Nº] meses desde la fecha establecida para ello en el artículo decimoquinto, o cuando transcurrido un período de [Nº] años desde la fecha de publicación de la obra, las liquidaciones anuales arrojen una venta inferior a [Nº] ejemplares.

Decimoprimero.- Liquidaciones

El editor se obliga a presentar anualmente al traductor durante el primer trimestre del año correspondiente, un certificado en el que se haga constar las liquidaciones de las ventas de ejemplares de la obra realizadas durante el año natural inmediatamente anterior —aunque el resultado sea negativo—, con expresión del número de ejemplares publicados, vendidos en depósitos, distribuidos y en almacén, así como su precio de venta sin IVA según catálogo. El pago lo realizará el editor dentro de los 30 días siguientes al envío del citado certificado.

Decimosegundo.- Obligaciones fiscales

El traductor faculta expresamente al editor para la detracción, declaración e ingreso en el Tesoro Público de aquellas cantidades que por cualquier concepto impositivo hubiera de satisfacer el autor derivadas de los rendimientos de la propiedad intelectual objeto de este contrato, en todos aquellos impuestos o gravámenes en que el editor tenga, por disposición legal, la condición de sustituto del Traductor-Contribuyente.

Decimotercero.- Duración

El presente contrato tendrá una duración de [Nº] años (15 como máximo) contados desde la fecha en que el traductor ponga a disposición del editor la obra en condiciones de ser reproducida. Extinguido el contrato, el editor gozará de un derecho de opción preferente para suscribir un nuevo contrato de edición sobre la misma obra, en iguales términos y condiciones que el traductor pueda convenir con terceros.

[OPCIONAL — incluir si procede]

(A tanto alzado art. 46 TRLPI)

El presente contrato tendrá una duración [Nº] años (10 como máximo) contados desde la fecha en que el traductor ponga a disposición del editor la obra en condiciones de ser reproducida.

Decimocuarto.- Venta de acciones o participaciones

Las partes declaran que, en caso de encontrarse el editor constituido jurídicamente en forma de sociedad anónima o limitada, la venta de acciones o participaciones sociales por parte de los actuales titulares en favor de terceros, no podrá considerarse que constituye cambio de titularidad de la empresa, en el sentido empleado en el artículo 68.f) del Real Decreto Legislativo 1/1996, de 12 de abril, por el que se aprueba el Texto Refundido de la Ley de Propiedad Intelectual. Asimismo, el editor, en caso de constituir una persona física, podrá ceder los derechos que adquiere en virtud del presente contrato, a una sociedad anónima o limitada que constituya y en la que suscriba más de un 50% del capital social, la cual le sustituirá en todo el contrato como editor.

Decimoquinto.- Distribución

El editor pondrá en conocimiento del traductor la forma de distribución en lo relativo a la explotación de la obra y qué entidad la va a realizar.

Decimosexto.- Ejemplares gratuitos

Estarán exentos de liquidación al traductor, aunque deberán serle notificados, los ejemplares que el editor entregue gratuitamente para fines de promoción y crítica de la obra y reposición de ejemplares defectuosos o estropeados. El máximo de ejemplares de cada edición que podrá destinar el editor a fines de promoción y crítica será de

El traductor recibirá sin cargo alguno un mínimo de [Nº] ejemplares de la primera edición y [Nº] ejemplares por cada una de las nuevas ediciones o reimpresiones de la obra, los cuales no podrán ser destinados al comercio y no devengarán derechos para el traductor. Asimismo, el traductor podrá adquirir al editor, con el descuento de [PORCENTAJE] % los ejemplares que precise para su uso particular o con destino a terceros, sin fines lucrativos.

Decimoséptimo.- Legislación aplicable

El presente contrato de edición se regirá y será interpretado conforme a lo previsto en el Real Decreto Legislativo 1/1996, de 12 de abril, por el que se aprueba el Texto Refundido de la Ley de Propiedad Intelectual y, en general, por las disposiciones legales que le sean de aplicación.

Decimoctavo.- Domicilio

Ambas partes designan como domicilio respectivo a efectos de notificaciones el que hacen constar en la cabecera de este contrato, si bien podrán modificarlo mediante notificación remitida a la otra parte.

Decimonoveno.- Sumisión en conflictos

[ELEGIR UNA OPCIÓN: Arbitraje / Tribunales]

Y en prueba de conformidad en cuanto antecede, suscriben el presente contrato, por duplicado, en el lugar y fecha arriba indicados.

El presente contrato se otorga en dos ejemplares pero a un solo efecto, quedando uno en poder de cada una de las partes contratantes.

EDITOR

TRADUCTOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

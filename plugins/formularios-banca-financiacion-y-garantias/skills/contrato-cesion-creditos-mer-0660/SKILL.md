---
name: contrato-cesion-creditos-mer-0660
description: "Contrato de cesión de créditos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cesión de créditos

> Formulario **MER-0660** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

El contrato por el que una persona (el cedente) transmite a otra (cesionario) la titularidad de los derechos de crédito que ostenta frente a una tercera persona (deudor); es decir, su derecho a recibir el pago de una deuda (o crédito) de parte de la misma. De esta forma, la tercera persona pasa a ser deudora del acreedor cesionario.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cesión de créditos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cesión de créditos” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-cesion-creditos-mer-0660`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] MES (2 veces)
- [ ] ENTIDAD BANCARIA
- [ ] LUGAR
- [ ] Nº DE CHEQUE
- [ ] NÚMERO

## Normas que cita el formulario

- art. 1170.2 Código Civil
- art. 347 Código de Comercio
- art. 1526 Código Civil
- art. 348 Código de Comercio
- art. 1529 Código Civil
- art. 1527 Código Civil

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

El contrato por el que una persona (el cedente) transmite a otra (cesionario) la titularidad de los derechos de crédito que ostenta frente a una tercera persona (deudor); es decir, su derecho a recibir el pago de una deuda (o crédito) de parte de la misma. De esta forma, la tercera persona pasa a ser deudora del acreedor cesionario.


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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

EXPONEN PRIMERO.-Que el cedente es titular del siguiente crédito:

Deudor: [DENOMINACIÓN SOCIAL], SA

Origen del crédito: entrega por el cedente de una partida de sus productos, aceptados a satisfacción de dicho deudor, y como consecuencia de la correspondiente compraventa mercantil.

Precio pactado: [IMPORTE] euros.

Fecha de aplazamiento y de vencimiento del crédito: el precio pactado fue aplazado y será pagadero el día [DÍA] de [MES] de [AÑO]

Garantías ofrecidas por dicho deudor: fianza solidaria prestada en legal forma por todos los miembros del Consejo de Administración de la sociedad deudora.

SEGUNDO.- Que interesa a ambas las partes la cesión por venta de la cedente a la cesionaria del crédito que a su favor ha sido descrito en el expositivo anterior, con todos los efectos que en Derecho sean procedentes y, a tal fin, otorgan el presente contrato de cesión de crédito por venta con sujeción a las siguientes

ESTIPULACIONES

[NOMBRE Y APELLIDOS], SA, debidamente representada por don [NOMBRE Y APELLIDOS], actuando como cedente, VENDE a la mercantil [DENOMINACIÓN SOCIAL], SL, en su calidad de cesionaria y representada en este acto por don [NOMBRE Y APELLIDOS], el crédito descrito en el expositivo primero de este documento. La cesionaria acepta y, en su consecuencia, adquiere la titularidad del crédito cedido, con todos los derechos, accesorios, obligaciones y cargas anejos al mismo.

Por ser de su interés, la cesionaria manifiesta conocer todas las circunstancias relativas al crédito que se transmite así como respecto de la operación comercial que fue origen de dicho crédito, cuyo exacto cumplimiento fue aceptado por el deudor del crédito cedido.

SEGUNDA.- El precio de esta cesión por venta asciende a [IMPORTE] euros., cantidad que, según manifiestan ambas partes, ha sido entregada en su mitad en efectivo a la cedente y la otra mitad mediante el giro de un cheque, por tal importe, con número de referencia [Nº DE CHEQUE], emitido por la cesionaria contra su cuenta corriente número, del Banco [ENTIDAD BANCARIA], sucursal núm [NÚMERO], y en favor de la cedente, quien manifiesta habérsele entregado dicho medio pago, sujetándose su eficacia liberatoria a cuanto dispone el artículo 1170.2º del Código Civil.

TERCERA.- La presente cesión se lleva a cabo de acuerdo con lo previsto en los artículos 347 y 348 del Código de Comercio y supletoriamente de conformidad con lo ordenado en los artículos 1526 y siguientes del Código Civil, SA como cedente, y de conformidad con cuanto dispone el artículo 348 del Código de Comercio, responde ante la cesionaria de la existencia y legitimidad del crédito cedido y de la personalidad con que se efectúa esta cesión, pero no de la solvencia del deudor del crédito cedido y de sus fiadores.

A estos efectos, y para el caso de que fuera aplicable lo dispuesto en el artículo 1529 del Código Civil, la cesionaria declara conocer la situación económica, financiera y patrimonial del deudor del crédito cedido y de sus fiadores solidarios y, de forma particular, su aparente situación de insolvencia derivada de la falta de pago, hasta la fecha, del crédito que se cede, por lo que liberan a la cedente de toda responsabilidad como consecuencia de la mencionada situación, al menos aparente, de insolvencia de los deudores y fiadores.

CUARTA.- La cedente, soportando ella misma los gastos que así se pudieran derivar, asume expresamente la obligación de notificar, mediante requerimiento notarial, la presente cesión al deudor del crédito cedido al igual que a los fiadores, disponiendo de un plazo que no podrá ser superior al de diez días a contar desde la fecha del presente acuerdo.

Todo ello a efectos de lo dispuesto en el artículo 347 del Código de Comercio y artículo 1527 del Código Civil.

QUINTA.- Todos los gastos e impuestos ocasionados con motivo del presente contrato serán de cuenta de la mercantil [DENOMINACIÓN SOCIAL]

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

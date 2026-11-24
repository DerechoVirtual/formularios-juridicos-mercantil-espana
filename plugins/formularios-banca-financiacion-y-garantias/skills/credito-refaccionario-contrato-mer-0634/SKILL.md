---
name: credito-refaccionario-contrato-mer-0634
description: "Crédito refaccionario (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Crédito refaccionario (contrato)

> Formulario **MER-0634** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Crédito refaccionario (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Crédito refaccionario (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:credito-refaccionario-contrato-mer-0634`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] AÑO (2 veces)
- [ ] FOLIO (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] TOMO (2 veces)
- [ ] CALLE
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DÍA
- [ ] DÍA Y MES
- [ ] ENTIDAD MEDIADORA
- [ ] FASE DE LAS OBRAS
- [ ] FUNDAMENTOS
- [ ] MES
- [ ] Nº REGISTRAL
- [ ] NÚMERO
- [ ] PISO
- [ ] PLAZO
- [ ] PUERTA
- [ ] REFERENCIA CATASTRAL

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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [DÍA] de [MES] de [AÑO]

Manifiestan

Que intervienen en su propio nombre, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE CRÉDITO REFACCIONARIO, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que el deudor refaccionario es propietario del inmueble cuya descripción registral es la siguiente:

Vivienda situada en la calle [CALLE], número [NÚMERO], piso [PISO], puerta [PUERTA], de la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], referencia catastral [REFERENCIA CATASTRAL], inscrita en el Registro de la Propiedad de [LOCALIDAD], Tomo [TOMO], Folio [FOLIO], Finca núm

II. Que en la citada finca se han realizado las siguientes obras:

Dichas obras han sido iniciadas por la empresa y se encuentran en este momento en fase de [FASE DE LAS OBRAS], siendo el montante total de las mismas la cantidad de [IMPORTE] euros, desglosada en la cantidad de [IMPORTE] euros ya liquidados mediante certificados de obra y pendientes de pago, y en la cantidad de [IMPORTE] euros presupuestados y pendientes de pago.

III. El deudor refaccionario está interesado en obtener un crédito refaccionario de [IMPORTE] euros para el pago de las obras a realizar en el inmueble y el acreedor refaccionario acepta la concesión de dicho crédito.

IV. Que conviniendo ambas partes en concertar el crédito, otorgan a tal fin el presente CONTRATO DE CRÉDITO REFACCIONARIO sobre la finca registral, descrita en el expositivo I, en base a las siguientes

CLÁUSULAS

Finca objeto de la refacción, cargas y vloración antes del inicio de las obras

Que Don [NOMBRE Y APELLIDOS], deudor refaccionario, es propietario de la vivienda [DESCRIPCIÓN DEL BIEN], que se encuentra inscrita en el Registro de la Propiedad de [LOCALIDAD], Tomo [TOMO], Folio [FOLIO], Finca Registral núm. [Nº REGISTRAL]

Que dicha finca se encuentra libre de cargas y no existe ninguna inscripción de derecho real a favor de persona distinta del propietaria.

Dicha finca tiene un valor de [IMPORTE] euros, antes del inicio de las obras objeto de la refacción, el cual es aceptado por ambas partes.

Obras objeto de la refacción

Las obras objeto de la refacción son las siguientes:

El coste económico de estas obras asciende a [IMPORTE] euros según se ha descrito en el expositivo II de este contrato.

[ELEGIR UNA OPCIÓN: Crédito para la realización de las obras / Concesión, cuantía y entrega / Finalidad]

Duración, vencimiento y amortización

El presente crédito se pacta por una duración de [PLAZO], por lo que el día de [DÍA Y MES] de [AÑO], el capital deberá haber sido íntegramente devuelto al acreedor refaccionario.

El capital y los intereses pactados se devolverán mediante el pago sucesivo de cuotas mensuales, con vencimiento la primera de ellas el día y las sucesivas el mismo día de cada uno de los meses siguientes.

En cualquier momento, el deudor refaccionario puede anticipar la devolución del capital y los intereses pactados.

Intereses

El crédito devengará un interés anual del% que se calculará sobre el capital pendiente de pago.

Intereses de demora

El retraso en el pago de las cantidades debidas, tanto por el principal como por intereses, devengará un interés de demora anual del %, que se computará a partir del día en que debió realizarse el pago, y ello sin necesidad de notificación al deudor refaccionario ni de denuncia de mora.

Causas de resolución anticipada

No obstante el vencimiento pactado, el acreedor refaccionario podrá resolver de pleno derecho el crédito y exigir todas las obligaciones de pago contraídas por el deudor refaccionario en los siguientes supuestos:

A) Alteración del destino pactado para la cantidad prestada.

B) Falta de pago, en la fecha de su vencimiento, de dos cuotas por cualquiera de las cantidades debidas en concepto de principal o intereses.

C) Por no comparecer el deudor refaccionario ante el registrador de la propiedad para que se anote el crédito refaccionario sobre la finca, o cuando la anotación registral se frustre por cualquier causa imputable al deudor.

Lugar de pago

Se designa como lugar de pago de las obligaciones derivadas del presente contrato la cuenta corriente señaladas en este contrato la cuenta corriente abierta por el acreedor refaccionario en la Entidad, Oficina, número, donde deberá realizar el deudor los pagos derivados de este contrato.

Responsabilidad del inmueble

Sin perjuicio de la responsabilidad personal e ilimitada del deudor refaccionario con respecto al acreedor refaccionario, el inmueble descrito en la estipulación primera responderá del crédito refaccionario conforme a lo establecido en la legislación civil e hipotecaria.

A dicho fin, ambas partes se comprometen a solicitar la anotación registral del crédito refaccionario contraído en virtud de este contrato, y a comparecer ante el Registrador de la Propiedad, personalmente o por medio de representante especialmente autorizado, a fin de llevar a cabo la anotación registral del crédito refaccionario.

Gastos

Los gastos derivados del presente contrato, incluidos los de la anotación del crédito refaccionario en el Registro de la Propiedad y que los tributos, correrán a cargo del deudor refaccionario.

NOTIFICACIONES

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Sumisión a mediación y/o arbitraje

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación [ENTIDAD MEDIADORA] de [LOCALIDAD], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y [FUNDAMENTOS] fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de la Corte de [LOCALIDAD], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

Fdo.: Don [NOMBRE Y APELLIDOS]

Acreedor refaccionario

Fdo.: Don [NOMBRE Y APELLIDOS]

Deudor refaccionario

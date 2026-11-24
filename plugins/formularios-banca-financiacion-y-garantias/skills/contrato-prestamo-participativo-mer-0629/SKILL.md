---
name: contrato-prestamo-participativo-mer-0629
description: "Contrato de préstamo participativo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de préstamo participativo

> Formulario **MER-0629** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de préstamo participativo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de préstamo participativo” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-prestamo-participativo-mer-0629`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (11 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] IMPORTE (3 veces)
- [ ] PROVINCIA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DÍA (2 veces)
- [ ] INSCRIPCIÓN (2 veces)
- [ ] MES (2 veces)
- [ ] NIF/DNI (2 veces)
- [ ] AÑO
- [ ] DOMICILIO
- [ ] FECHA
- [ ] NIF
- [ ] PLAZO
- [ ] PORCENTAJE

## Normas que cita el formulario

- art. 20 Ley 7/1996

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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [DÍA] de [MES] del [AÑO]

PARTES

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NIF/DNI]

Y de otra parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA] provisto/a del N.I.F. [NIF/DNI]

INTERVINIENTES

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF, fecha, domiciliada en y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D./Dª [NOMBRE Y APELLIDOS], en fecha e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], en adelante LA PRESTATARIA

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF [NIF], domiciliada en [DOMICILIO] y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D./Dª [NOMBRE Y APELLIDOS], en fecha [FECHA] e inscrita en el Registro Mercantil de inscripción [INSCRIPCIÓN], en adelante LA PRESTAMISTA

MANIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE PRÉSTAMO PARTICIPATIVO, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

OBJETO

I. Que la PRESTATARIA está interesada en contratar un préstamo participativo para el ejercicio de su actividad social por importe de [IMPORTE] euros

II. Que la PRESTAMISTA está dispuesta a conceder el citado préstamo, en las condiciones que se dirán, siendo conocedora de la situación actual de la entidad PRESTATARIA.

III. Que conviniendo ambas partes en concertar el crédito, otorgan a tal fin el presente CONTRATO DE PRÉSTAMO PARTICIPATIVO, en base a las siguientes

CLAUSULAS

PRIMERA.- OBJETO DEL CONTRATO

La PRESTAMISTA concede un préstamo participativo por la cantidad de [IMPORTE] euros, la cual se ingresa en este acto (o en el plazo de … días) por transferencia bancaria en la cuenta núm titularidad de la PRESTATATARIA, que deberán ser devueltas y reintegradas por ésta en las circunstancias y condiciones que se señalan en el presente contrato.

Dicho préstamo se destinará por la PRESTATARIA para la financiación de las actividades de la misma.

Este préstamo participativo se considerará patrimonio contable a los efectos de reducción del capital y liquidación de sociedades previstas en la legislación mercantil.

El presente se regirá por los pactos particulares contenidos en el contrato y por las disposiciones legales aplicables al mismo, en particular por lo dispuesto en el artículo 20 del Real Decreto Ley 7/1996, de 7 de junio.

SEGUNDA.- DURACIÓN

El presente préstamo se pacta por una duración de [PLAZO], por lo que finalizará el día de [DÍA] de [MES]

No obstante, este contrato será susceptible de prórroga por anualidades sucesivas, a contar desde el día de finalización cada periodo, siempre que no medie comunicación en contrario de cualquiera de las partes, notificada a la otra parte con una antelación mínima de treinta días, a la fecha de vencimiento inicial o de sus prórrogas.

TERCERA. AMORTIZACIÓN E INTERESES

El préstamo se amortizará en cuotas anuales con vencimiento el día por importe de [IMPORTE] euros cada una de ellas con más sus intereses.

El presente préstamo devengará un interés fijo del [PORCENTAJE] %, con independencia de la evolución de la actividad, y, además, un interés variable, que por cada año será equivalente al % del resultado antes de impuestos, sin tener en cuenta en el mismo el propio interés del préstamo.

El resultado antes de impuestos se determinará a partir de las cifras que aparezcan en las cuentas anuales aprobadas por la Junta General de la PRESTATARIA correspondientes al último ejercicio cerrado antes de cada uno de los sucesivos vencimientos. Si en el momento de la liquidación no se hubieran aprobado por la Junta General de la PRESTATARIA las cuentas correspondientes al último ejercicio a computar, incluso en el caso de vencimiento anticipado, se tomará como resultado antes de impuestos el correspondiente al ejercicio anterior incrementado en un % por ciento.

CUARTA.- AMORTIZACIÓN ANTICIPADA

La parte PRESTATARIA podrá amortizar anticipadamente el crédito, total o parcialmente, a partir del primer ejercicio, siempre y cuando el préstamo participativo se compense con una ampliación de igual cuantía de sus fondos propios y este aumento no provenga de la revalorización de activos.

Se pacta expresamente una penalización por amortización anticipada del % sobre el total del importe del capital amortizado.

QUINTA.- INTERESES DE DEMORA

El retraso en el pago de las cantidades debidas, tanto por el principal como por intereses, devengará un interés de demora anual del %, que se computará a partir del día en que debió realizarse el pago, y ello sin necesidad de notificación a la PRESTATARIA ni de denuncia de mora.

SEXTA.- CAUSAS DE RESOLUCIÓN ANTICIPADA

No obstante el vencimiento pactado, el PRESTAMISTA podrá resolver de pleno derecho el crédito y exigir todas las obligaciones de pago contraídas por el PRESTATARIO en los siguientes supuestos:

1) Falta de pago, en la fecha de su vencimiento, de la cuota por cualquiera de las cantidades debidas en concepto de principal o intereses.

2) El cese de actividad de la PRESTATARIA, el haber declarado su disolución o liquidación, o incurrir en causa legal de disolución, o la pérdida de valor de sus activos que represente más de un % del valor de su activo inmovilizado según las cuentas anuales.

3) La solicitud de declaración judicial de concurso o situación preconcursal similar.

4) El incumplimiento de obligaciones por la PRESTATARIA con respecto de terceros, o el que se haya decretado embargo sobre sus bienes o derechos.

La PRESTATARIA se obliga expresamente a informar inmediatamente a la PRESTAMISTA de cualquier circunstancia que pueda afectar al cumplimiento del presente contrato o a que se produzca cualquier causa de vencimiento anticipado.

SÉPTIMA.- LUGAR DE PAGO

Se designa como lugar de pago de las obligaciones derivadas del presente contrato la cuenta abierta por la PRESTAMISTA en la Entidad, Oficina, número, donde deberá realizar la PRESTATARIA los pagos derivados de este contrato.

OCTAVO.- PRELACIÓN DEL CRÉDITO

En orden a la prelación de créditos, este préstamo participativo se situará después de los acreedores comunes.

NOVENO.- GASTOS E IMPUESTOS

Los gastos e impuestos derivados del presente contrato serán satisfechos por la parte determinada legalmente y, en otro caso, por mitad.

DECIMO.- NOTIFICACIONES

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

UNDÉCIMO. SUMISIÓN A MEDIACIÓN Y/O ARBITRAJE

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación ( en su caso se citará la institución) de., antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y ( caso de fijar un plazo máximo....) fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

(caso de pacto sucesivo de arbitraje...) A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de la Corte de [LOCALIDAD], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo.: Don ………. Fdo.: Don ……….

PRESTATARIOPRESTAMISTA

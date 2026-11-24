---
name: contrato-prestamo-garantizado-hipoteca-mer-0683
description: "Contrato de préstamo garantizado con hipoteca. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de préstamo garantizado con hipoteca

> Formulario **MER-0683** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de préstamo garantizado con hipoteca» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de préstamo garantizado con hipoteca” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-prestamo-garantizado-hipoteca-mer-0683`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] IMPORTE (6 veces)
- [ ] Nº (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] FECHA (3 veces)
- [ ] AÑO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] ACTIVIDAD
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MOTIVO
- [ ] PLAZO
- [ ] TOMO

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL PRESTAMISTA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL PRESTATARIO", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE PRÉSTAMO CON GARANTÍA HIPOTECARIA, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que EL PRESTATARIO precisa de una cantidad de dinero de la que en la actualidad no dispone para [MOTIVO] (descripción del uso que se pretende dar a la cantidad de dinero prestado).

SEGUNDO.- Que EL PRESTAMISTA es una persona jurídica de derecho privado dedicada a la [ACTIVIDAD] (descripción de la actividad), mostrándose conforme con hacer entrega al PRESTATARIO de la cantidad solicitada.

TERCERA.- Que por todo lo anterior, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

EL PRESTAMISTA entrega en concepto de préstamo al PRESTATARIO, que acepta, la cantidad de [IMPORTE] euros ( €), que deberán ser devueltas y reintegradas por dicho PRESTATARIO en las circunstancias y condiciones que se señalan en el presente contrato.

Duración del préstamo

El presente préstamo se pacta por una duración de [PLAZO], por lo que el día [FECHA] de [MES] (mes) de [AÑO] (año) el capital prestado deberá haber sido íntegramente devuelto al PRESTAMISTA.

[ELEGIR UNA OPCIÓN: Intereses / Préstamo ordinario / Participativo / — y además elegir: Forma de devolución / Mediante pago único / Devolución mediante pago único / Cuotas periódicas / Devolución mediante cuotas periódicas]

Interés de demora

El retraso en cualquiera de los pagos dará derecho al PRESTAMISTA a exigir un interés moratorio del % respecto de cada uno de los pagos no satisfechos puntualmente. Si EL PRESTATARIO se retrasara en el pago de [Nº] plazos o en el pago del último, EL PRESTAMISTA podrá optar entre exigir el pago de los plazos pendientes o resolver el contrato, con abono en ambos caso de las indemnizaciones que puedan corresponder.

Devolución anticipada del préstamo

No obstante la duración pactada, EL PRESTAMISTA podrá considerar vencido de pleno derecho el préstamo y exigibles la totalidad de las obligaciones de pago que tenga contraídas EL PRESTATARIO cuando concurra cualquiera de las circunstancias siguientes:

1. Cuando EL PRESTATARIO incumpliera cualquiera de las obligaciones contraídas en virtud del presente contrato.

2. Cuando los datos del PRESTATARIO o los documentos aportados por él y que sirvieron de base conocer la situación financiera del mismo, determinante a los efectos de la concesión del préstamo, hubieran sido falseados.

3. Cuando EL PRESTATARIO enajene o grave más del % del total de sus bienes, modifique o cambie su objeto social, sus actividades o su naturaleza jurídica, o de cualquier manera que influya negativamente en su solvencia.

4. Cuando EL PRESTATARIO sea declarado en situación legal de concurso.

Amortización anticipada del préstamo

El préstamo concertado podrá ser objeto de amortización anticipada si así lo decidiera EL PRESTATARIO.

Dicha amortización podrá ser total o parcial. Las cantidades anticipadas serán aplicadas, en primer lugar, a la satisfacción de intereses, comisiones y gastos devengados y, en segundo lugar, a la amortización del principal, según el orden natural de las fechas de amortización previstas.

En caso de amortización anticipada a solicitud del PRESTATARIO se percibirá en el momento de la misma una comisión del % anual, sobre la cantidad amortizada.

Compromiso de garantía

Si durante la vigencia del préstamo se produjesen circunstancias que pudieran afectar negativamente a la solvencia del PRESTATARIO, éste se obliga a constituir, a requerimiento del PRESTAMISTA, las garantías reales sobre bienes inmuebles, muebles o derechos que sean necesarias para garantizar la devolución de las cantidades adeudadas.

Esta obligación deberá ser cumplida por EL PRESTATARIO dentro del plazo de [Nº] días/semas/meses siguientes a la fecha en que EL PRESTAMISTA le haya requerido para ello.

Cesión del contrato

Cesión de derechos del PRESTATARIO

EL PRESTATARIO no podrá transmitir sus derechos y obligaciones sobre el préstamo sin el consentimiento previo y por escrito del. Éste no podrá denegar el consentimiento de forma arbitraria.

En caso de una eventual cesión de los derechos, EL PRESTAMISTA podrá adaptar el canon pactado en el presente contrato al que viniera exigiendo a los nuevos prestatarios en esa fecha.

Cesión de derechos del PRESTAMISTA

EL PRESTAMISTA se reserva la facultad de ceder libremente sus derechos y obligaciones derivados del presente contrato, previa comunicación escrita al PRESTATARIO. El cesionario quedará subrogado en todos los derechos y obligaciones contractuales de la cedente.

Garantía hipotecaria

Constitución de la hipoteca

Se constituye hipoteca a favor de LA PRESTAMISTA sobre el inmueble descrito inmueble [DESCRIPCIÓN DEL BIEN] situado en [DIRECCIÓN] número [NÚMERO] de [LOCALIDAD], cuyos datos registrales son los siguientes: Finca número [NÚMERO], inscrita en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], constando una superficie de [Nº] metros cuadrados útiles de dicha vivienda en la inscripción registral, en garantía del pago del saldo resultante de la cuenta de crédito, hasta la cantidad de [IMPORTE] euros, cantidad que se desglosa en la siguiente forma:

1.-Hasta la cantidad de [IMPORTE] euros, en concepto de límite máximo de este crédito.

2.-Hasta la cantidad de [IMPORTE], euros en concepto de intereses ordinarios devengados durante el último año al tipo % establecido en el presente contrato.

3.-Hasta la cantidad de [IMPORTE] euros en concepto de intereses de demora del último año y al tipo pactado.

4.-Hasta la cantidad de [IMPORTE] euros en concepto de costas y gastos tanto judiciales como extrajudiciales y que tengan relación con la conservación y efectividad de la garantía.

Extensión de la garantía

La garantía hipotecaria se extiende a los elementos, bienes y derechos que se enumeran en los arts. 109 y 110 de la Ley Hipotecaria.

Cesión del crédito hipotecario

EL PRESTATARIO renuncia de manera expresa al derecho de notificación en caso de cesión o venta de todo o parte del crédito hipotecario de conformidad con lo dispuesto en la Ley Hipotecaria.

Seguro

EL PRESTATARIO se obliga a formalizar un seguro de daños, que cubra riesgo de pérdida de la finca hipotecada durante toda la vigencia del presente crédito en una entidad aseguradora de conocida solvencia.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de la parte

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE PRÉSTAMO MERCANTIL extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo. Don [NOMBRE Y APELLIDOS]

(El Prestamista)

Fdo. Don [NOMBRE Y APELLIDOS]

(El Prestatario)

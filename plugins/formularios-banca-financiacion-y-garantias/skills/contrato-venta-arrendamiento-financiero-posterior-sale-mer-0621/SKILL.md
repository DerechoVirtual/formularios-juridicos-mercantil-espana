---
name: contrato-venta-arrendamiento-financiero-posterior-sale-mer-0621
description: "Contrato de venta con arrendamiento financiero posterior (sale and lease back). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de venta con arrendamiento financiero posterior (sale and lease back)

> Formulario **MER-0621** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de venta con arrendamiento financiero posterior (sale and lease back)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de venta con arrendamiento financiero posterior (sale and lease back)” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-venta-arrendamiento-financiero-posterior-sale-mer-0621`.
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
- [ ] INSCRIPCIÓN (2 veces)
- [ ] NIF/DNI (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DÍA
- [ ] INSTITUCIÓN DE MEDIACIÓN
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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [DÍA] de [MES] de [AÑO]

Partes

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NIF/DNI]

Y de otra parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de provincia de [PROVINCIA] provisto/a del N.I.F. [NIF/DNI]

Intervinientes

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF, domiciliada en y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], en adelante LA VENDEDORA/ARRENDATARIA

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF, domiciliada en y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], en adelante LA COMPRADORA/ARRENDADORA

MANIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE SALE AND LEASE BACK, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

Exposiciones

I. Que la VENDEDORA/ARRENDATARIA está interesada en vender, y simultáneamente arrendar, el inmueble de su propiedad con la siguiente descripción: (se harían constar los datos del inmueble…)

II. Que la COMPRADORA/ARRENDADORA está dispuesta a adquirir el inmueble con finalidad inmediata de cederlo en arrendamiento en unidad de acto a la VENDEDORA/ARRENDATARIA.

III. Que conviniendo ambas partes en concertar el contrato, otorgan a tal fin el presente CONTRATO DE SALE AND LEASE BACK, en base a las siguientes

Cláusulas

PRIMERA.- OBJETO DEL CONTRATO

Por medio del presente contrato, la VENDEDORA/ARRENDATARIA, en la representación que ostenta, VENDE el inmueble descrito en el antecedente primero a la COMPRADORA/ ARRENDADORA.

La venta se efectúa con cuantos derechos, usos, servicios y servidumbres son inherentes al inmueble, libre de cargas, y con exclusión de los bienes muebles que se encuentran en su interior que son de titularidad de la VENDEDORA/ARRENDATARIA.

El estado del inmueble y el inventario del mobiliario, maquinaria y demás efectos que hay en su interior, de titularidad de la VENDEDORA/ARRENDATARIA, así como las tasaciones, se recoge en el Anexo I de este contrato.

Simultáneamente, en unidad de acto, la COMPRADORA/ARRENDADORA arrienda el citado inmueble a la VENDEDORA/ARRENDATARIA, para que continúe desarrollando la actividad de [ACTIVIDAD] con el mismo mobiliario, maquinaria y demás efectos de su titularidad.

SEGUNDA.- PRECIO DE LA COMPRAVENTA

El precio de la compraventa del inmueble es de [IMPORTE] Euros, impuestos excluidos, que la COMPRADORA entrega a la vendedora en este acto.

TERCERA.- PLAZO INICIAL DE ARRENDAMIENTO Y RENTA

La COMPRADORA/ARRENDADORA arrienda el inmueble adquirido a la VENDEDORA/ARRENDATARIA por un periodo inicial de AÑOS.

La renta anual será de [IMPORTE] EUROS, impuestos excluidos, y se abonará por mensualidades anticipadas en los cinco primeros días del mes.

CUARTA.- PRÓRROGA Y OPCIÓN DE COMPRA

Al finalizar el plazo inicial del arrendamiento, la VENDEDORA-ARRENDATARIA podrá prorrogar el contrato durante un periodo adicional de AÑOS, notificándolo a la COMPRADORA-ARRENDADORA con una antelación mínima de seis meses.

A la finalización del periodo de prórroga, se reconoce a favor de la VENDEDORA-ARRENDATARIA el derecho de opción de compra sobre el inmueble objeto del presente contrato, y a tal efecto la COMPRADORA-ARRENDADORA estará obligada a suscribir documento público de compraventa, cuando concurran las siguientes condiciones:

1.ª Que se ejercite este derecho dentro del plazo de [Nº] meses anteriores a la finalización del plazo de prórroga pactado. Si no se prorroga el contrato o pasado este plazo la VENDEDORA-ARRENDATARIA perderá la opción de compraventa pactada.

2.ª Que la VENDEDORA-ARRENDATARIA ponga a disposición del arrendador el valor residual del inmueble, que se fija de la siguiente manera:

. La cantidad resultante se hará efectiva cuando se suscriba la escritura pública de compraventa.

. Del precio final deberá descontarse la cantidad abonada en concepto de renta que se considerará parte del precio liquidado de forma anticipada, según las previsiones del cuadro de amortización que se adjunta como Anexo II del presente contrato, fijándose el valor residual inicial en [IMPORTE] euros, el cual deberá ser concretado tan pronto se ejercite la opción con arreglo a las rentas efectivamente satisfechas en el periodo de duración inicial y prórroga del contrato, y sus actualizaciones, y una vez actualizado el precio final al IPC, según las fórmulas recogidas en el citado Anexo II del contrato.

- Los gastos e impuestos derivados de la transmisión correrán por cuenta de la VENDEDORA-ARRENDATARIA.

QUINTA.- ACTUALIZACIÓN DE LA RENTA ARRENDATICIA

Al cumplimiento de cada año de vigencia del contrato la renta será actualizada previo requerimiento fehaciente en el mes anterior, expresando el porcentaje de alteración aplicado siendo válida para ello la notificación efectuada por nota en el recibo de la mensualidad del pago precedente.

Las partes contratantes convienen que la renta total que en cada momento satisfaga el arrendatario se acomodará cada año a la variación porcentual experimentada por el Índice de Precios al Consumo que fije el Instituto Nacional de Estadística (u Organismo que le sustituya), aplicando sobre aquella renta el porcentaje que represente la diferencia existente entre los índices que correspondan al período de revisión. Para la aplicación de las sucesivas actualizaciones, se tomará como mes de referencia el del mes de

SEXT A.- OBLIGACIONES DE LA VENDEDORA-ARRENDATARIA

La VENDEDORA-ARRENTARIA se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, y en especial asume las siguientes obligaciones:

Las obras de mantenimiento, mejoras, reparaciones, sustituciones y todas las que sean necesarias para la adecuada conservación del inmueble serán de cuenta de la VENDEDORA-ARRENDATARIA, sin que las mismas generen derecho de indemnización a su favor una vez finalizado el contrato de arrendamiento.
Los impuestos, seguros y demás gastos relativos al inmueble serán íntegramente de cuenta de la VENDEDORA-ARRENDATARIA.
La VENDEDORA-ARRENDATARIA se obliga a concertar un seguro a favor del COMPRADOR-ARRENDADOR que cubra el importe de seis mensualidades de renta, como fianza arrendaticia.

SÉPTIMA.- OBLIGACIONES DE LA COMPRADORA-ARRENDADORA

La COMPRADORA-ARRENDADORA se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, garantizado el uso de la cosa por la arrendataria y, en especial, se obliga a no enajenar ni gravar el inmueble durante el periodo del arrendamiento y su prórroga hasta el momento en que el arrendatario ejercite en su caso la opción de compra pactada en la estipulación cuarta.

SÉPTIMA.- CESIÓN Y SUBARRIENDO

La VENDEDORA-ARRENDATARIA no podrá ceder el contrato ni subarrendar le inmueble sin el consentimiento expreso y por escrito del COMPRADOR-ARRENDADOR.

OCTAVA.- CAUSAS DE RESOLUCIÓN ANTICIPADA

No obstante el vencimiento pactado, la VENDEDORA-ARRENDADORA podrá resolver de pleno derecho el arrendamiento y exigir todas las obligaciones a cargo la VENDEDORA-ARRENDATARIA en los siguientes supuestos:

1) Falta de pago de la renta.

2) El cese de actividad de la VENDEDORA-ARRENDATARIA, el haber declarado su disolución o liquidación, o incurrir en causa legal de disolución, o la pérdida de valor de sus activos que represente más de un ….% del valor de su activo inmovilizado según las cuentas anuales.

3) La apertura de la fase de liquidación tras la declaración judicial de concurso de la VENDEDORA-ARRENDATARIA.

4) El incumplimiento grave de las obligaciones por la VENDEDORA-ARRENDATARIA en los términos pactados en este contrato..

(…)

Ambas partes pactan expresamente que, en caso de terminación anticipada del arrendamiento por causa imputable a la VENDEDORA-ARRENDATARIA, ésta pagará a LA COMPRADORA-ARRENDADORA la totalidad de la renta correspondiente al resto del período de duración del arrendamiento pactado, sin derecho a ejercitar la opción de compra.

NOVENA.- GASTOS E IMPUESTOS

Los gastos e impuestos derivados del presente contrato serán satisfechos por la parte determinada legalmente y, en otro caso, por mitad.

DÉCIMA.- NOTIFICACIONES

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

UNDÉCIMA.- SUMISIÓN A MEDIACIÓN Y/O ARBITRAJE

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación (en su caso se citará la institución) de [INSTITUCIÓN DE MEDIACIÓN], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y (caso de fijar un plazo máximo....) fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

( caso de pacto sucesivo de arbitraje...) A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de la Corte de [LOCALIDAD], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato y sus Anexos I y II, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

Fdo.: Fdo.:

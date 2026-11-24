---
name: garantia-primer-requerimiento-contrato-mer-0657
description: "Garantía a primer requerimiento (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Garantía a primer requerimiento (contrato)

> Formulario **MER-0657** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Garantía a primer requerimiento (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Garantía a primer requerimiento (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:garantia-primer-requerimiento-contrato-mer-0657`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº (4 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] CONCEPTO DE LA GARANTÍA
- [ ] DÍA
- [ ] LUGAR
- [ ] Nº DE EJEMPLARES
- [ ] NÚMERO DE LA CALLE
- [ ] OBJETO DEL CONTRATO

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].de [MES] dos mil [AÑO]

Con intervención del Notario Don [NOMBRE Y APELLIDOS], perteneciente al Colegio Notarial de [LOCALIDAD] Y con residencia en [LOCALIDAD]

MANIFIESTAN

1. Que con fecha de [FECHA] Se formalizó un contrato de construcción de [OBJETO DEL CONTRATO] entre el ORDENANTE DE LA GARANTÍA y el BENEFICIARIO que fue intervenido por el Notario Don [NOMBRE Y APELLIDOS] y cuyo contenido se incorpora en fotocopia como anexo de este contrato.

2. Que, como consecuencia del referido contrato, el ORDENANTE DE LA GARANTÍA se obliga a construir de acuerdo con las instrucciones recibidas y a entregar al BENEFICIARIO de lo convenido en el referido contrato, en el lugar acordado y, en todo caso, antes de la fecha de

3. Que el BENEFICIARIO DE LA GARANTÍA se obliga, en virtud del referido contrato que le vincula con el ORDENANTE a satisfacerle la cantidad de [IMPORTE] € contra la recepción de la mercadería en la cc.

4. Que frente al riesgo de incumplimiento de la obligación de entrega por parte de la entidad ORDENANTE DE LA GARANTÍA, el BENEFICIARIO desea garantizar el cumplimiento del contrato suscrito, mediante la celebración de un contrato autónomo de garantía bajo la modalidad a primera demanda, en el que figure como EMISOR DE LA GARANTÍA una entidad de crédito.

CLÁUSULAS

Objeto del contrato

Que en virtud del presente contrato el EMISOR DE LA GARANTÍA se obliga frente al BENEFICIARIO a garantizar el cumplimiento, en los términos previstos, del contrato de compraventa suscrito entre el ORDENANTE y el BENEFICIARIO DE LA GARANTÍA y del que se da cuenta en las manifestaciones de este contrato y cuya copia se incorpora en el Anexo I.

Extensión de la garantía

La garantía prestada por el EMISOR lo es, exclusivamente, para el cumplimiento de las obligaciones asumidas por el ORDENANTE frente al BENEFICIARIO en el contrato celebrado entre estos últimos con fecha

Cuantía de la garantía prestada

El importe de la garantía prestada por el EMISOR es por [CONCEPTO DE LA GARANTÍA], y hasta, la cantidad de [IMPORTE] €, y en su caso serán reclamados y satisfechos en la sucursal de [LOCALIDAD] del EMISOR, c/ [CALLE], núm. [NÚMERO DE LA CALLE]

Período de duración de la garantía

La duración de la garantía prestada por el EMISOR es de [Nº] días a contar desde el día siguiente en que el ORDENANTE DE LA GARANTÍA hubiera debido cumplir con su obligación de entrega. Esto es, la garantía dejará de producir sus efectos en la fecha de [FECHA] Si la EMISORA DE LA GARANTÍA no fuese requerida de pago fehacientemente por el BENEFICIARIO dentro de los [Nº] días siguientes al incumplimiento del contrato garantizado, y en la sucursal mencionada en la cláusula tercera de este contrato, la entidad EMISORA DE ESTA GARANTÍA quedará completamente liberada de cuantas obligaciones asumió en virtud de este documento y, consiguientemente, quedará extinguida y sin efecto la presente garantía.

Reclamación de la garantía

Durante el período de vigencia de la garantía, tal y como se contempla en la cláusula cuarta de este contrato, el EMISOR DE LA GARANTÍA cumplirá frente al BENEFICIARIO las obligaciones de garantía asumidas en virtud del presente documento, contra el requerimiento fehaciente de pago del BENEFICIARIO en que se notifique a la entidad EMISORA DE LA GARANTÍA el incumplimiento en fecha del contrato garantizado.

Renuncia expresa a los beneficios de la fianza

El EMISOR DE LA GARANTÍA renuncia expresamente a los beneficios de orden, excusión y cualesquiera otros que le pudieran corresponder con fundamento en el contrato celebrado entre el ORDENANTE y el BENEFICIARIO DE LA GARANTÍA. La garantía se configura con carácter autónomo o independiente por lo que el EMISOR DE LA GARANTÍA se compromete a su realización contra requerimiento fehaciente del BENEFICIARIO, recibida en los términos contenidos en este documento, en el que se notifique el incumplimiento del contrato garantizado.

Retribución de la garantía

El EMISOR DE LA GARANTÍA recibe, contra la firma del presente documento, la cantidad de [IMPORTE] € del ORDENANTE. Si la ejecución llegara a realizarse en los términos convenidos en este contrato recibirá, además, la cantidad de [IMPORTE] € del ORDENANTE que le serán cargados, en los quince días siguientes a la ejecución de la garantía, en la c/c núm. [Nº] que la entidad ORDENANTE tiene abierta en la sucursal del EMISOR DE LA GARANTÍA sita en [LOCALIDAD], calle [CALLE], núm. [Nº], de

Gastos de formalización

Todos los gastos, impuestos y correlativos deriva- dos de la formalización, cumplimiento y extinción de las obligaciones consignadas en este contrato serán a cargo del ORDENANTE DE LA GARANTÍA.

Normativa aplicable

En todo lo no previsto en este documento, el régimen jurídico a que quedará sometida la garantía a primer requerimiento prestada en virtud de la firma del presente contrato será el dispuesto por las Reglas Uniformes de Garantías a Primer Requerimiento (Uniform Rules for Demand Guarantees, URDG) de la Cámara de Comercio Internacional de París.

Sometimiento a fuero

Las partes renuncian a su fuero propio, sometiéndose para la resolución de los litigios que pudieran surgir por este contrato a la Jurisdicción española y a los Tribunales de

Fe pública

El presente contrato se formaliza, con intervención de Fedatario Público, especialmente requerido a todos los efectos legales. Las partes manifiestan su conformidad al presente contrato que otorgan y firman con mi intervención en [Nº DE EJEMPLARES], ejemplares igualmente originales y auténticos formalizados a un solo efecto, quedando un original en mi archivo. Y yo, Fedatario Público, hechas las advertencias legales y en particular las de carácter fiscal doy fe de la identidad y capacidad de las partes, de la legitimidad de sus firmas, y de todo lo convenido en el presente documento que firmo y sello en el lugar y fecha arriba indicados.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

EL BENEFICIARIO DE LA	EL ORDENANTE	EL EMISOR GARANTÍA

ANEXO 1

Fotocopia del contrato de compraventa garantizado

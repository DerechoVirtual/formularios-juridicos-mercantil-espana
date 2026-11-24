---
name: solicitud-apertura-credito-documentario-mer-0655
description: "Solicitud de apertura de crédito documentario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de apertura de crédito documentario

> Formulario **MER-0655** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Solicitud que dirige un cliente (ordenante) a su banco para que abra un crédito documentario a favor de un beneficiario extranjero, con las condiciones de la operación (importe, modo de pago, envíos, Incoterms, documentos exigidos) y las condiciones generales que regulan la relación entre banco emisor y solicitante, conforme a las Reglas y Usos Uniformes de la Cámara de Comercio Internacional (UCP 600).

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de apertura de crédito documentario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de apertura de crédito documentario” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:solicitud-apertura-credito-documentario-mer-0655`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (6 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] ESPECIFICAR (2 veces)
- [ ] FIRMA (2 veces)
- [ ] MES (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] CIUDAD
- [ ] DATOS DEL BANCO DEL BENEFICIARIO
- [ ] DATOS DEL BENEFICIARIO
- [ ] DESCRIPCIÓN DE LA MERCANCÍA
- [ ] FECHA
- [ ] FECHA DE VENCIMIENTO
- [ ] IMPORTE
- [ ] INDICACIONES
- [ ] LUGAR DE DESTINO
- [ ] LUGAR DE ORIGEN
- [ ] MEDIO DE TRANSPORTE
- [ ] MONEDA
- [ ] NOMBRE DEL CORRESPONSAL
- [ ] NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL
- [ ] Nº DE CUENTA
- [ ] OTRAS INDICACIONES
- [ ] OTRAS INSTRUCCIONES
- [ ] SUCURSAL

## Normas que cita el formulario

- art. 276 Código de Comercio

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

- Junto a «… en cuanto resulte aplicable a los créditos documentarios, y el Derecho español.»: el original la denominaba "Convención de Viena"; comprobar su denominación y su aplicabilidad al caso.

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

SOLICITUD DE APERTURA DE CRÉDITO DOCUMENTARIO

Sucursal: [SUCURSAL]

Lugar y fecha: [LOCALIDAD], [DÍA] de [MES] de [AÑO]

Solicitante: [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL]

Cuenta a cargo: [Nº DE CUENTA]

Muy señores nuestros:

Rogamos a Vds. se sirvan abrir un Crédito Documentario con las siguientes características:

Beneficiario (nombre, domicilio, ciudad, país): [DATOS DEL BENEFICIARIO]

Banco del beneficiario (nombre, oficina, cuenta, plaza): [DATOS DEL BANCO DEL BENEFICIARIO]

Añadir confirmación: [ELEGIR: Sí / No]

Transferible: [ELEGIR: Sí / No]

Fecha de vencimiento y lugar de utilización: [FECHA DE VENCIMIENTO] / [ELEGIR: en las cajas del Banco emisor / en las cajas del Banco corresponsal [NOMBRE DEL CORRESPONSAL]]

Importe y moneda: [IMPORTE] [MONEDA]

Clase de importe: [ELEGIR: exacto / aproximado, con tolerancia del [PORCENTAJE] %]

Modo de pago: [ELEGIR: a la vista / diferido] ; [ELEGIR: aceptación / negociación]

Envíos parciales: [ELEGIR: autorizados / no autorizados]

Envío desde [LUGAR DE ORIGEN] hasta [LUGAR DE DESTINO] por [MEDIO DE TRANSPORTE]

Transbordos: [ELEGIR: autorizados / no autorizados]

Última fecha de expedición de la mercancía: [FECHA]

Clase de compraventa según INCOTERMS: [ELEGIR: C.I.F. / F.O.B. / C&F / Ex-Works / otra: ESPECIFICAR]

Localidad a la que se refiere: [LOCALIDAD]

Descripción de la mercancía: [DESCRIPCIÓN DE LA MERCANCÍA]

Documentos de transporte (indicar número de ejemplares de cada uno):

[ELEGIR LOS QUE PROCEDAN:] Juego completo de conocimiento de embarque limpio (marítimo): [Nº] ejemplares. / Juego completo de conocimiento de embarque limpio (aéreo): [Nº] ejemplares. / Carta de porte ferroviario o talón de ferrocarril: [Nº] ejemplares. / Otros: [ESPECIFICAR]

Otros documentos (indicar número de ejemplares):

[ELEGIR LOS QUE PROCEDAN:] Factura comercial: [Nº] ejemplares. / Póliza o certificado de seguro: [Nº] ejemplares. / Otros: [ESPECIFICAR]

Indicaciones: [INDICACIONES]

Los documentos de transporte deberán ser presentados dentro de los [Nº] días a partir de la fecha de embarque de la mercancía, pero dentro del plazo de validez del crédito. Otras indicaciones sobre los documentos de transporte: [OTRAS INDICACIONES].

Las comisiones y gastos bancarios que se produzcan fuera de España serán a cargo [ELEGIR: nuestro (del solicitante) / del beneficiario].

Otras instrucciones: [OTRAS INSTRUCCIONES]

Este crédito se abre por nuestra cuenta y riesgo y se regirá por las condiciones especiales y generales de la presente solicitud y por las Reglas y Usos Uniformes relativos a los Créditos Documentarios, publicadas por la Cámara de Comercio Internacional, en su última versión de 2007 (Publicación n.º 600 de la CCI, UCP 600).

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Solicitante: [FIRMA]	Banco emisor (sello y firma p.p.): [FIRMA]

CONDICIONES GENERALES

PRIMERA.— En estas condiciones se entiende por Banco Emisor el Banco que firma la presente póliza, por Solicitante el cliente que ordena la apertura del crédito y por Beneficiario la persona que está legitimada para presentar los documentos y exigir el importe del crédito.

SEGUNDA.— El crédito documentario es completamente independiente de la relación que subyace entre el Solicitante y el Beneficiario. El Banco trabaja con documentos y no con mercancías. La correspondencia de la mercancía con la descripción de la misma que figura en el formulario no incumbe al Banco más allá de lo documentalmente constatable.

TERCERA.— Si la presente solicitud tuviere amparo en un contrato de apertura de crédito, en un contrato de afianzamiento o de garantía para la realización de operaciones de comercio con el exterior o en un contrato de depósito irregular, las condiciones particulares que ahora se reseñan le serán de aplicación únicamente en lo no previsto por aquél.

Las cantidades que pague el Banco Emisor al/los Beneficiario/s de este Crédito se asentarán en la cuenta designada en el anverso (cuenta de cargo) y serán reembolsadas por el Solicitante, en esta ciudad, ante la presentación de los documentos exigidos o, cuando la utilización no sea a la vista, al vencimiento del pago diferido. El saldo deberá satisfacerse en moneda de curso legal, calculando, en su caso, el cambio de la moneda extranjera al tipo de cambio vendedor vigente en el mercado de divisas el día del pago por el Banco Emisor al Beneficiario o, en su caso, el día del reembolso del Banco Emisor a su Corresponsal. Cuando el saldo de la cuenta de cargo designada fuese insuficiente, devengará en favor del Banco Emisor el interés nominal pactado en el contrato de apertura de crédito o, alternativamente, en caso de que la operación no se hiciere a su amparo, el tipo nominal anual del [PORCENTAJE] %, que se liquidará por trimestres vencidos. La fórmula utilizada para obtener el importe absoluto de los intereses devengados al tipo nominal pactado es IA = C x N x r / (365 x 100), siendo IA = importe absoluto de los intereses devengados en cada liquidación al tipo de interés nominal contractual; C = capital sobre el que se devengan; N = número de días naturales correspondientes al período de devengo; r = interés nominal contractual expresado en tantos por ciento. Los intereses se calcularán desde el día del pago por el Banco Emisor al Beneficiario o, en su caso, desde el día del reembolso del Banco Emisor a su Corresponsal hasta el día del reembolso del Solicitante al Banco Emisor.

CUARTA.— El Banco Emisor gozará, a los efectos del art. 276 del Código de Comercio, del derecho de retención sobre mercancías y documentos representativos de las mismas para resarcirse de las cantidades que se le adeudan en virtud de la apertura y puesta en funcionamiento del presente Crédito.

[OPCIONAL — incluir si procede: cláusula adicional de pignoración] Las mercancías y los documentos representativos de las mismas quedarán pignorados en favor del Banco Emisor para la satisfacción de las cantidades adeudadas a éste por la emisión y puesta en funcionamiento del Crédito.

QUINTA.— En el caso de que el presente Crédito tenga como cobertura un depósito irregular, deberá determinarse si los fondos depositados quedan a disposición del Banco Emisor para satisfacer el pago del crédito documentario o bien se pignora su derecho al reembolso del saldo depositado, en garantía de las cantidades adeudadas por la emisión y puesta en funcionamiento del Crédito. En este segundo caso, el Banco Emisor podrá compensar los mencionados saldos con las cantidades adeudadas en virtud del Crédito Documentario.

En el caso en que la apertura del crédito documentario tenga como cobertura una póliza de apertura de crédito y, en general, siempre que el Banco Emisor se haya obligado a anticipar los fondos necesarios para poner en funcionamiento el Crédito, el Solicitante se obliga a constituir prenda sobre las mercancías en favor del Banco Emisor para la satisfacción de las cantidades adeudadas a éste por la emisión y puesta en funcionamiento del Crédito, según las formalidades de la Ley sobre Hipoteca Mobiliaria y Prenda sin Desplazamiento, de manera simultánea a la recepción de manos del Banco Emisor de los documentos exigidos en la presente solicitud.

[OPCIONAL — cláusula alternativa a la inmediatamente anterior:] La entrega al Solicitante se realizará para que éste venda la mercancía y reembolse lo adeudado con cargo al producto obtenido. El Banco podrá exigir la prestación de las garantías oportunas para asegurar este reembolso.

SEXTA.— Para el caso de que el Solicitante no haya reembolsado al Banco Emisor todos los desembolsos, comisiones y gastos relativos a la emisión y puesta en funcionamiento de este Crédito, contabilizados en la cuenta de cargo, en los tres días siguientes al momento de exigibilidad de los mismos, determinado según la cláusula anterior, el Solicitante apodera de manera irrevocable al Banco Emisor para vender la mercancía con libertad de precios, tiempo, pactos y condiciones, aplicando el importe a la satisfacción de los saldos deudores descritos y quedando el resto, si lo hubiere, a disposición del Solicitante. Si el precio obtenido no fuera suficiente para cubrir los anticipos, gastos y comisiones de la operación, el comitente quedará deudor del Banco Emisor por el resto.

SÉPTIMA.— [ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Para todas las cuestiones litigiosas que puedan derivarse de este Crédito, ambas partes renuncian a su propio fuero y se someten a la jurisdicción y competencia de los Tribunales de [CIUDAD].

— Para todas las cuestiones litigiosas que puedan derivarse de este Crédito, ambas partes se someten al arbitraje previo de la Cámara de Comercio Internacional, que resolverá las mencionadas controversias de acuerdo con la interpretación de las estipulaciones de esta póliza, las Reglas y Usos Uniformes para los Créditos Documentarios de la Cámara de Comercio Internacional (revisión de 2007), la Convención de las Naciones Unidas sobre Garantías Independientes y Cartas de Crédito Contingente, en cuanto resulte aplicable a los créditos documentarios, y el Derecho español.

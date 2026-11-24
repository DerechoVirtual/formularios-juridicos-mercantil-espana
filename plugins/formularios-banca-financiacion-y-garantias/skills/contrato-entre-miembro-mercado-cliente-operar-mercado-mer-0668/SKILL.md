---
name: contrato-entre-miembro-mercado-cliente-operar-mercado-mer-0668
description: "Contrato entre miembro del mercado y cliente para operar en el mercado de valores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato entre miembro del mercado y cliente para operar en el mercado de valores

> Formulario **MER-0668** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato entre miembro del mercado y cliente para operar en el mercado de valores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato entre miembro del mercado y cliente para operar en el mercado de valores” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-entre-miembro-mercado-cliente-operar-mercado-mer-0668`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (2 veces)
- [ ] Nº (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] LUGAR
- [ ] MES

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

1. MIEMBRO

RAZÓN SOCIAL [DENOMINACIÓN SOCIAL]

NIF-CIF:

DOMICILIO:

REPRESENTADO POR:

ESCRITURA DE APODERAMIENTO/LUGAR:

FECHA:

Nº [Nº]:

NOTARIO:

2. CLIENTE

NOMBRE O RAZÓN SOCIAL/NAME-COMPANY NAME:

NIF-CIF/TAX NUMBER:

DOMICILIO SOCIAL/ADDRESS:

REPRESENTADO POR/SIGNATORY:

ESCRITURA DE APODERAMIENTO/POWER OF ATTORNEY: LUGAR/PLACE:

FECHA/DATE: Nº [Nº]/[AÑO] NUMBER: NOTARIO/NOTARY:

3. NÚMERO DE CUENTA ASIGNADO AL CLIENTE:

4. CONOCIMIENTO Y ACEPTACIÓN DE LA NORMATIVA APLICABLE:

EL CLIENTE declara conocer y aceptar el Reglamento del mercado, las Condiciones Generales de los Contratos negociables, las Circulares del Mercado y demás normativa aplicable en cada momento, sin restricciones ni reservas, obligándose a respetar- los estrictamente.

Y, en prueba de su conformidad con lo que antecede, firman ambas partes el presente contrato.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

FIRMA MIEMBRO FIRMA CLIENTE:

5. OBLIGACIONES MUTUAS

(Sin perjuicio de las contenidas en el Reglamento)

5.1. EL CLIENTE nombra como comisionista al MIEMBRO, quien acepta intervenir en nombre propio y por cuenta del CLIENTE en el Mercado.

5.2. El MIEMBRO garantiza al CLIENTE la transmisión al Mercado de las Órdenes que reciba del mismo en aplicación del presente contrato y a efectuar cuantos actos fueran necesarios para la realización de las Transacciones.

5.3. El CLIENTE conoce que MEFF SOCIEDAD RECTORA DE PRODUCTOS FINANCIEROS DERIVADOS DE PRODUCTOS FINANCIEROS DE RENTA VARIABLE, SA (en adelante, MEFF) actuará como su contrapartida en las Transacciones que se realicen, siempre que las Ordenes hayan sido adecuadamente transmitidas por el MIEMBRO.

5.4. El CLIENTE se compromete a constituir y ajustar las Garantías que correspondan a los Contratos registrados en su Cuenta.

5.5. EL CLIENTE acepta que, en caso de que no constituyera o ajustase las Garantías precisas en la cuantía y tiempo establecidos, MEFF podrá liquidar por cuenta del Cliente todas sus posiciones en el Mercado ejecutando la garantía previamente constituida si fuese necesario y entregando al Cliente el resultado de dicha liquidación si fuese a favor del Cliente o reclamándosela si fuese a favor de MEFF.

5.6. En aplicación de lo anterior, el CLIENTE da a MEFF orden firme e irrevocable de Cerrar, por cuenta del CLIENTE, todos los Contratos registrados en su Cuenta, en caso que el CLIENTE incumpliera con alguna de sus obligaciones de constitución o ajuste de Garantías, pago de Primas de Opciones, pago de la Liquidación Diaria de Pérdidas y Ganancias, cumplimiento de la liquidación por ejercicio o a vencimiento o pago de comisiones a MEFF.

6. COMISIONES

6.1. Comisiones MEFF. Las comisiones cargadas por MEFF son las recogidas en la tarifa de MEFF que esté vigente en cada momento, de las que se dará conocimiento al Cliente en el momento de firma del contrato.

6.2. Comisiones MIEMBRO. Las comisiones cargadas por el MIEMBRO al CLIENTE son las que éstos han acordado libremente, que se adjuntan como anexo a este contrato firmado por las partes.

7. PAGOS

7.1. El CLIENTE autoriza al MIEMBRO para que realice en su nombre los pagos y cobros que resulten de la participación del CLIENTE en el Mercado.

7.2. El CLIENTE se compromete al pago de comisiones, primas y liquidaciones, incluida la liquidación diaria de pérdidas y ganancias, por las transacciones realizadas por su cuenta en el Mercado.

7.3. El MIEMBRO se compromete al pago al Cliente de las primas y liquidaciones recibidas de MEFF correspondientes a las transacciones realizadas en el Mercado por cuenta del cliente.

8. COMUNICACIÓN E INFORMACIÓN

El Cliente da su consentimiento para que su nombre y número de identificación fiscal, que figuran en el presente contrato, sean comunicados a las autoridades competentes por el miembro o por MEFF, si fuese necesario.

9. EXONERACIÓN DE DAÑOS Y PERJUICIOS

El CLIENTE exonera al MIEMBRO y a MEFF de cualquier daño o perjuicio que pudiera sufrir por causa de fuerza mayor o por suspensión o interrupción del Mercado.

10. RECLAMACIONES

10.1 INTERVENCIÓN PREVIA DE MEFF. Para la resolución de reclamaciones del Cliente contra el MIEMBRO o contra MEFF, previamente a cualquier acción administrativa, arbitral o judicial, el CLIENTE se dirigirá por escrito a MEFF (MEFF RENTA VARIABLE, Torre Picasso, planta 26, 28020-MADRID ó MEFF RENTA FIJA, Vía Laietana, 58, 08003-BARCELONA), identificando, en su caso, al Miembro frente al que tiene la reclamación, y describiendo con detalle ésta y los hechos que la fundamenten.

MEFF, en un plazo no superior a 15 días, tratará que ambas partes lleguen a un acuerdo. Si transcurrido dicho plazo, no se hubiese logrado un acuerdo entre las partes, MEFF lo hará constar por escrito, el cual remitirá a ambas partes y a la Comisión Nacional de Mercado de Valores, haciendo constar, en su caso, si el MIEMBRO ha actuado o no correctamente y proponiendo una solución a la reclamación

10.2 PROCEDIMIENTO ARBITRAL (Cláusula optativa)

El CLIENTE y el MIEMBRO acuerdan someter todas las discrepancias que puedan surgir entre ellos o del CLIENTE con MEFF a un procedimiento de Arbitraje de Derecho en la forma y términos comprendidos en el artículo 9.4 del Reglamento que se da aquí por reproducido a todos los efectos, obligándose a cumplir el laudo arbitral que se dicte.

La operativa en Opciones y Futuros requiere una vigilancia constante de la posición. Estos instrumentos comportan un alto riesgo si no se gestionan adecuadamente. Un beneficio puede convertirse rápidamente en pérfida como consecuencia de variaciones en el precio. Operar con Opciones y Futuros requiere conocimiento y buen juicio.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

FIRMA CLIENTE: FIRMA MIEMBRO:

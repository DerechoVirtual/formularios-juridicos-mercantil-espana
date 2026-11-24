---
name: acuerdo-prenda-sobre-credito-deuda-mer-0654
description: "Acuerdo de prenda sobre un crédito o deuda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acuerdo de prenda sobre un crédito o deuda

> Formulario **MER-0654** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acuerdo de prenda sobre un crédito o deuda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acuerdo de prenda sobre un crédito o deuda” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:acuerdo-prenda-sobre-credito-deuda-mer-0654`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (8 veces)
- [ ] MES (5 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] LUGAR

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].año

INTERVIENEN

D [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A] en lo sucesivo "EL ACREEDOR", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO] en fecha [FECHA] con el número de protocolo [Nº DE PROTOCOLO] poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A] en lo sucesivo "EL DEUDOR", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO] en fecha [FECHA] con el número de protocolo [Nº DE PROTOCOLO] poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente ACUERDO DE PIGNORACIÓN, y a tal efecto, libremente y de común acuerdo,

EXPONEN

I.- Que [DENOMINACIÓN SOCIAL] S.L. es acreedor de la mercantil [DENOMINACIÓN SOCIAL], S.L.U., con base en convenio de fecha [DÍA] de [MES] de [AÑO]

II.- Con arreglo al citado convenio, [DENOMINACIÓN SOCIAL] S.L., adeuda a [DENOMINACIÓN SOCIAL], S.L. la cantidad de [IMPORTE] euros ( €) y con vencimiento al día [FECHA] de [MES] de

III.- Que LA DEUDORA es acreedora de la compañía [DENOMINACIÓN SOCIAL] S.L. (C.I.F. B-) por el concepto de provisión de fondos por la prestación de servicios según consta en contrato de fecha [FECHA] de [MES] de

El importe adeudado por [DENOMINACIÓN SOCIAL], S.L. a LA DEUDORA asciende a la cantidad de [IMPORTE] (,00 €). Esta deuda tiene como vencimiento el propio vencimiento del contrato, el cual se produjo con fecha [DÍA] de [MES] de [AÑO], no siendo aplicable esta provisión de fondos a posteriores prorrogas del contrato, si las mismas se produjeran.

IV.- Que con el fin de garantizar el pago de las cantidades adeudas por LA DEUDORA a LA ACREEDORA, ambas partes,

ACUERDAN

Objeto

LA DEUDORA. con el fin de garantizar las obligaciones de pago tanto de principal, como de intereses u otras responsabilidades accesorias, derivadas de la deuda que se ha generado a favor de LA ACREEDORA afecta y pignora con carácter irrevocable los importes que deba percibir, perciba, o se depositen o consignen, a favor de LA DEUDORA por la deuda que mantiene la compañía [DENOMINACIÓN SOCIAL], S.L., con LA DEUDORA, según se describen en el expositivo III de este convenio, hasta cubrir el importe adeudado a LA ACREEDORA

En consecuencia las cantidades que puedan ser percibidas como consecuencia de los conceptos enunciados, quedarán indisponibles por parte de LA DEUDORA en tanto no quede totalmente cancelado y liquidado a satisfacción de LA ACREEDORA la totalidad de la deuda que pueda existir a la fecha del pago.

Autorización

Desde esta fecha se autoriza de forma irrevocable y sin limitación alguna para que LA ACREEDORA en todo momento pueda cobrar directamente los saldos pendientes de [DENOMINACIÓN SOCIAL], S.L., terceros, hasta cancelar totalmente la deuda, sin necesidad de requerimiento de notificación.

Comunicaciones

Igualmente, LA DEUDORA., se compromete y obliga irrevocablemente a poner en conocimiento de LA ACREEDORA tan pronto se produzca, cualquier notificación y/o comunicación, y/o situación que pudiera afectar o se refiera a las deudas mencionadas.

LA DEUDORA. se obliga a manifestar a todo tercero que pretenda trabar o embargar los importes a percibir por ella, la existencia de la pignoración, exhibiéndole a tal fin copia este convenio, y si, no obstante, la diligencia de embargo se practicara, exigirá que se haga contar en el acta que se extienda, sus manifestaciones y se tome nota en la misma de la pignoración. De todo ello se dará cuenta inmediatamente a LA ACREEDORA para que pueda proceder en defensa de sus derechos.

Ejercicio de acciones

La aceptación por LA ACREEDORA de esta garantía, no empece las acciones de todo tipo que le correspondan, las cuales podrá ejercitar libremente y sin que entablada la acción se entienda dificultado o diferido el ejercicio de las acciones derivadas de esta garantía, quedando LA ACREEDORA facultada para retener o aplicar el importe de los pagos de estas deudas hasta que se pague la totalidad de la deuda que haya podido generarse. Esta garantía podrá ser utilizada por LA ACREEDORA con carácter previo, simultáneo o posterior a cualquier otra que le corresponda ahora y en el futuro sin necesidad de requerimientos y/o notificaciones.

Sumisión a Tribunales

Para la resolución de cualesquiera controversias que surgieran en la interpretación y/o aplicación y cumplimiento del presente contrato, las Partes, con renuncia expresa a cualquier otro fuero que pudiera corresponderles, acuerdan someterse a los Tribunales de

Y en prueba de conformidad, ambas partes suscriben el presente convenio, por duplicado y aun solo efecto, en el lugar y fecha indicados en el encabezamiento.

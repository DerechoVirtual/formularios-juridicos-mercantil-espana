---
name: contrato-compraventa-internacional-entre-importador-mer-0544
description: "Contrato de compraventa internacional entre importador y exportador. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa internacional entre importador y exportador

> Formulario **MER-0544** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa internacional entre importador y exportador» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa internacional entre importador y exportador” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-compraventa-internacional-entre-importador-mer-0544`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] LEGISLACIÓN APLICABLE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] FECHA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] INCOTERM
- [ ] LUGAR
- [ ] NIF
- [ ] Nº
- [ ] PAÍS
- [ ] PLAZO

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

Contrato entre dos partes (importador y exportador) domiciliados en países distintos por el que se comprometen al intercambio de una mercancía por el pago de un precio. En este contrato deben constar datos como el precio, la cantidad, incoterms, la calidad, las especificaciones técnicas, el puerto de destino, etc.

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de VENDEDOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, VENDEDOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del COMPRADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, COMPRADOR.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato y, a tal fin,

MANIFIESTAN

Que han acordado celebrar un contrato mercantil de compraventa internacional de mercaderías con sujeción a las siguientes

CLÁUSULAS

Primera.- Objeto

El objeto de la presente compraventa son las siguientes mercaderías [DESCRIPCIÓN DEL BIEN] que el VENDEDOR transmite al COMPRADOR, quien las acepta con sujeción al resto de cláusulas de este contrato.

[OPCIONAL — incluir si procede]

(Descripción de la mercancía en anexos)

La mercancía que mediante el presente contrato transfiere «el vendedor» al «comprador» es la que figura relacionada en el anexo unido a este documento.

Segunda.- Entrega, Incoterms y riesgos

La venta se efectuará en condiciones [INCOTERM] (FOB [LOCALIDAD], NIF [NIF]) sometiéndose las partes contratantes, en cuanto a la interpretación de dicho término comercial, a las reglas internacionales publicadas por la Cámara de Comercio Internacional (INCOTERMS 2020).

En consecuencia, cada parte deberá cumplir las obligaciones y sufragar los gastos que, según la indicada interpretación, correspondan a cada una de ellas, sometiéndose igualmente a las citadas reglas (INCOTERMS 2020) en lo referente a la transmisión del riesgo.

El «vendedor» deberá haber entregado la mercancía objeto de este contrato al transportista como máximo antes del día [FECHA], no respondiendo de los daños que pudieran ocasionarse al «comprador» como consecuencia de demoras en la llegada de dicha mercancía a destino, salvo que tales demoras se hubiesen motivado por incumplimiento del plazo de entrega indicado y no pudiera acreditar el «vendedor» causa justificada alguna que hubiese ocasionado dicho retraso.

[OPCIONAL — incluir si procede]

(Sanciones por retrasos)

La falta de entrega de las mercancías en la fecha acordada dará derecho al comprador a fijar un plazo suplementario para la entrega de [Nº] días, o bien optar por la resolución del contrato o por exigir al vendedor el pago de una indemnización de [IMPORTE] euros por cada día de demora, siempre que no existiese causa justificada que motivase tal demora

Tercera.- Precio

El precio de la compraventa de las mercancías objeto de este contrato, se fija en [IMPORTE] euros que serán pagados de la siguiente forma:

El % del precio total, es decir [IMPORTE] euros se abonan por el comprador al VENDEDOR en el presente acto mediante [ELEGIR: efectivo / cheque / transferencia bancaria a la cuenta corriente de la que es titular el vendedor], sirviendo este documento de la más eficaz carta de pago.

[ELEGIR UNA OPCIÓN: En plazos / Crédito documentario]

[OPCIONAL — incluir si procede]

(Actualización de Precios)

Queda entendido que el precio pactado se ha calculado de acuerdo con los costes del día de la firma del presente contrato. Consiguientemente, si entre dicha fecha y la pactada para la entrega se modificasen tales costes por causas ajenas a la voluntad del «vendedor», el «comprador» vendrá obligado a soportar, un eventual aumento del precio

Cuarta.- Reserva de dominio

La propiedad de la mercancía no se transmitirá al «comprador» hasta que por éste se haya satisfecho la totalidad del precio pactado, reservándose entretanto el dominio sobre dicha mercancía el «vendedor» quien podrá exigirlo incluso en caso de reventa de la mercancía por parte del «comprador».

Si la ley del país del «comprador» no reconociera como válida la «reserva de dominio» estipulada en este pacto, el «vendedor» gozará de todos los demás derechos sobre la mercancía vendida que dicha Ley le reconozca, quedando obligado el «comprador» a prestar su colaboración al «vendedor» si éste se ve precisado a tomar medidas destinadas a proteger su derecho de propiedad y todos los demás derechos nacidos del presente contrato.

Quinta.- Impagos

Caso de que por el «comprador» dejara de pagarse todo o parte del precio convenido, el «vendedor» podrá optar entre ejercitar la reserva de dominio y recuperar la mercancía vendida, en cuyo caso el «comprador» perdería todo derecho al reintegro de las cantidades que hubiese hasta entonces satisfecho, o exigir judicialmente el cobro del resto de las cantidades que hubiesen podido quedar impagadas.

Sexta.- Garantía

El vendedor se compromete a reponer gratuitamente cualquier pieza defectuosa o a reparar cualquier defecto de funcionamiento, siempre que el «comprador» ponga en conocimiento del «vendedor» dicho defecto en un plazo máximo de [PLAZO] contados a partir de la recepción de la mercancía en destino.

Transcurridos dicho plazo no se admitirán reclamaciones ni devoluciones de ningún tipo. En cualquier caso el «vendedor» podrá comprobar los defectos acusados por el «comprador» mediante los medios que crea oportunos, sin que el «comprador» pueda entorpecer la actuación de las personas encargadas por el «vendedor» para verificar tal comprobación.

Quedan excluidos de este plazo de garantía los defectos o perjuicios ocasionados en la mercancía vendida por causa de negligencia o manejo defectuoso por parte del «comprador», uso de lubricantes no apropiados, accidentes, siniestros, y, en general, cualquier otro tipo de irregularidad ajena al funcionamiento de la mercancía en sí.

Séptima.- Asistencia técnica y mantenimiento.

En caso de que «el comprador» solicite al «vendedor» el montaje en destino de la mercancía objeto de este contrato, deberá cubrir todos los gastos que el mismo lleve consigo, incluidos los gastos de desplazamiento y dietas del personal enviado por el «vendedor» para dicho montaje.

Igualmente correrán de su cargo los gastos que origine cualquier otro desplazamiento de personal técnico requerido para efectuar trabajos de mantenimiento o reparación de la mercancía vendida, sin perjuicio del plazo de garantía estipulado.

Octava.- Impuestos y gastos

Todos los impuestos que graven este contrato en el país del vendedor correrán a cargo de éste y los que se devenguen en el país del comprador serán satisfechos por él. Los derechos de aduana serán a cargo de la parte que le corresponda según el término comercial pactado en la cláusula segunda.

Los demás gastos que se originen por la celebración, cumplimiento o extinción de este contrato, tanto judiciales como extrajudiciales, serán a cargo de la parte que la ley [LEGISLACIÓN APLICABLE] señale.

Novena.- Carácter mercantil y legislación aplicable

El presente contrato es de carácter mercantil y se regirá por la Convención de las Naciones Unidas sobre los Contratos de Compraventa Internacional de Mercaderías adoptada en Viena el 11 de abril de 1980 y por los INCOTERMS 2020 en cuanto a la formación del contrato y los derechos y obligaciones del vendedor y del comprador dimanantes de este contrato [LEGISLACIÓN APLICABLE]; en lo restante se aplicará la ley [LEGISLACIÓN APLICABLE], contenida en el Código de Comercio español, leyes especiales españolas, usos mercantiles y en su defecto al Código Civil español

Décima.- Fuero

Caso de que el «vendedor» tuviese que entablar acción judicial contra el «comprador» por incumplimiento de las obligaciones de pago estipuladas, o cualquier otra obligación por servicios prestados por el «vendedor» que deban ser atendidos por el «comprador», las partes, de común acuerdo, deciden someter la controversia a la competencia de los tribunales del país del «comprador» y concretamente a los de la localidad en donde éste desarrolle sus actividades comerciales o industriales, debiéndose resolver el litigio de acuerdo con la ley del país del comprador.

[OPCIONAL — incluir si procede]

Decimoprimera.- Arbitraje

Independientemente de lo dispuesto, que será de observancia únicamente para las reclamaciones que en su caso pudiera entablar el «vendedor» contra el «comprador» por causa de impago de cantidades adeudadas por cualquier concepto, las dudas o discrepancias que pudieran surgir respecto a la interpretación o traducción del presente contrato o al cumplimiento de cualquier otra obligación aquí estipulada, serán sometidas a procedimiento de arbitraje de acuerdo con el Reglamento de la Cámara de Comercio Internacional obligándose las partes a respetar la decisión del laudo arbitral que se dicte. La ley con arreglo a la que deba resolverse la controversia será la del país del [PAÍS].

Así queda convenido. Y para que conste se extiende y firma el presente documento, por duplicado

COMPRADOR

VENDEDOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

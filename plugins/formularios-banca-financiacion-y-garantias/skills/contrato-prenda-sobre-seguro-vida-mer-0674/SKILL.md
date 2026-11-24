---
name: contrato-prenda-sobre-seguro-vida-mer-0674
description: "Contrato de prenda sobre un seguro de vida. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de prenda sobre un seguro de vida

> Formulario **MER-0674** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de prenda sobre un seguro de vida» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de prenda sobre un seguro de vida” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-prenda-sobre-seguro-vida-mer-0674`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] AÑO
- [ ] CONCEPTO DE LA DEUDA
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
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

PIGNORACIÓN DE SEGURO DE VIDA

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO],

De otra:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL ACREEDOR PIGNORATICIO", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL DEUDOR PIGNORANTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Reconociéndose mutuamente y teniendo a juicio del Fedatario Público que interviene, capacidad legal suficiente para el otorgamiento de la presente garantía, y a tal efecto, libremente y de común acuerdo,

MANIFIESTAN

PRIMERO. Que EL DEUDOR PIGNORANTE es titular de un derecho de crédito derivado de la póliza de seguro de vida cuyos datos a continuación se reflejan:

a) TOMADOR:

b) ENTIDAD ASEGURADORA:

c) BOLETÍN DE ADHESIÓN DE FECHA:

d) PÓLIZA N.º [NÚMERO] DE FECHA [FECHA]

e) BENEFICIARIO CON CARÁCTER REVOCABLE:

SEGUNDO Que EL DEUDOR PIGNORANTE adeuda al ACREEDOR PIGNORATICIO la cantidad de [IMPORTE] en concepto de [CONCEPTO DE LA DEUDA]

TERCERO Que por todo lo anterior, ambas partes de común acuerdo constituir derecho real de PRENDA sobre el derecho de crédito derivado del seguro de vida anteriormente descrito.

CLÁUSULAS

Objeto

La prenda se extiende al derecho del DEUDOR PIGNORANTE a obtener el rescate del seguro contratado por el valor liquidativo que tengan los activos contratados en el momento de verificarse el rescate, con independencia de la circunstancia que lo determine.

Duración del contrato

La presente garantía se mantendrá vigente mientras subsistan las responsabilidades derivadas de la operación asegurada en concepto de principal, intereses, comisiones y otros gastos.

Alcance de la garantía

3.1. Reducción de la deuda

Las eventuales reducciones de la deuda principal no facultan al DEUDOR PIGNORANTE para exigir la liberación parcial o proporcional de la garantía aportada.

3.2. Fallecimiento del DEUDOR PIGNORANTE

La prenda se mantendrá vigente en la hipótesis de fallecimiento del DEUDOR PIGNORANTE titular de la misma si existen aún riesgos garantizados pendientes de abono. Si con anterioridad a la extinción de las obligaciones garantizadas se produce el fallecimiento del asegurado o el vencimiento del seguro, los importes que deba satisfacer la Compañía de Seguros serán ingresados en una cuenta especial abierta a nombre del ACREEDOR PIGNORATICIO con esta fecha y a este efecto, extendiéndose la prenda a los derechos económicos derivados de su saldo.

3.3. Prórroga del crédito

La prórroga del crédito que pudiera producirse en el futuro conllevará automáticamente la prórroga de la vigencia de la garantía y la de los demás pactos establecidos en el presente contrato, sin necesidad de aviso o aprobación del DEUDOR PIGNORANTE, quien presta su consentimiento expreso con la firma del presente contrato.

3.4. Amortización anticipada del crédito

En el supuesto de que el crédito fuera amortizado anticipadamente y fueran liquidadas al ACREEDOR PIGNORATICIO todas las obligaciones accesorias por razón del mismo, los derechos de cobro derivados de los créditos pignorados quedarán libres de la prenda constituida, procediéndose a su devolución al DEUDOR PIGNORANTE.

Incumplimiento de la obligación subyacente

En caso de incumplimiento de la obligación subyacente por parte del DEUDOR PIGNORANTE el ACREEDOR PIGNORATICIO podrá hacer efectivo su derecho ejecutando la prenda en los términos que se exponen a continuación, sin perjuicio de su derecho a ejercitar las acciones derivadas de la obligación subyacente sobre el patrimonio del DEUDOR:

a) EL ACREEDOR PIGNORATI CIO podrá ejercitar directamente los derechos de rescate, aplicando las cantidades por los importes que procedan al pago de la deuda.

b) Las cantidades depositadas en la cuenta especial expuesta en la Cláusula Tercera serán aplicables automática y directamente al pago de la deuda, quedando relevado el ACREEDOR PIGNORATICIO del requisito de subasta pública en atención a su condición de prenda de derechos de cobro inmediato y que por ser un valor líquido no precisan de realización, poniendo el sobrante, si lo hubiera, a disposición del DEUDOR PIGNORANTE.

Revocación del beneficiario

La garantía prestada implica la revocación del beneficiario designado con carácter revocable señalado en el Exponendo Primero.

Notificación a la entidad aseguradora

El DEUDOR PIGNORANTE faculta al ACREEDOR PIGNORATICIO a notificar en su nombre a la entidad aseguradora la pignoración del seguro de vida para que ésta se abstenga de realizar pago alguno al deudor titular o al beneficiario designado.

Las partes acuerdan que la presente garantía pignoraticia podrá ser sustituida o complementada por otros bienes aceptables para EL ACREEDOR PIGNORATICIO, previo otorgamiento del correspondiente contrato de constitución de prenda.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de la parte

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Régimen del contrato

El presente contrato tiene carácter mercantil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en las disposiciones de la Ley de la Ley de Hipoteca Mobiliaria y Prenda sin Desplazamiento, del Código de Comercio, demás leyes especiales y usos mercantiles.

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE PIGNORACIÓN DE SEGURO DE VIDA extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(El ACREEDOR PIGNORATICIO)

Fdo. Don [NOMBRE Y APELLIDOS]

(El DEUDOR PIGNORANTE)

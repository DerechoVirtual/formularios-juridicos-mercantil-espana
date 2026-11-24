---
name: contrato-factoring-creditos-comerciales-mer-0628
description: "Contrato de factoring de créditos comerciales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de factoring de créditos comerciales

> Formulario **MER-0628** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de factoring de créditos comerciales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de factoring de créditos comerciales” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-factoring-creditos-comerciales-mer-0628`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] ACTIVIDAD
- [ ] FECHA
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] PERIODO
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

Operación financiera por la que el cliente, generalmente una empresa cede a un factor (empresa de "factoring") créditos comerciales contra sus clientes, a cambio de un importe convenido.

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del FACTOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, FACTOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del CLIENTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CLIENTE.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de FACTORING y, a tal fin,

MANIFIESTAN

I. Que la empresa [DENOMINACIÓN SOCIAL], se dedica a [ACTIVIDAD] estando interesada en la gestión de cobro y abono de los servicios que presta.

II. Que [DENOMINACIÓN SOCIAL] (factor) tiene por objeto la ejecución por cuenta de cualquier cliente de un conjunto de servicios que comprenden entre otros, la investigación de la solvencia de los compradores o deudores de dichos cedentes, la asignación de un riesgo de insolvencia de los créditos cedidos, la realización del cobro de éstos, el seguimiento del control contable de dichos riesgos y la realización de anticipos financieros sobre ellos. (Factorin sin recursos)

III. Que habiendo llegado las partes a un acuerdo, otorgan el presente contrato que formalizan bajo las siguientes:

CLÁUSULAS

Primera.- Objeto

El FACTOR, previa comunicación por el CLIENTE de sus deudores, se obliga a realizar investigaciones sobre la solvencia de los mismos, clasificándolos mediante el establecimiento de un límite cuantitativo de riesgo económico y por un determinado período de tiempo, que constituirá, a su vez, el límite máximo de asunción de riesgo asumido por el FACTOR para cada uno de ellos.

Tal límite de cobertura será comunicado por el FACTOR al CLIENTE, comportando dicha comunicación la aceptación, por el FACTOR, del DEUDOR investigado y clasificado

Segunda.- Cesión

Los créditos se cederán al FACTOR con todos los accesorios que de ellos deriven o que con ellos se relacionen. en la forma prevista en el presente contrato.

Por la cesión el FACTOR adquiere con exclusividad todos los derechos del CEDENTE contra los DEUDORES de los créditos cedidos.

El nominal de las facturas cedidas por todos los conceptos y pendientes de vencimiento no podrá superar el límite nominal de [IMPORTE] euros.

Si el FACTOR apreciara que los riesgos en curso de los documentos en su poder sumados a los de una nueva remesa que se le presente exceden el límite nominal antedicho, o estimara que ha existido experiencia negativa alguna con algún cliente determinado, quedará facultado para rechazar la remesa o remesas que considere oportuno en la relación con ese CLIENTE.

Tercera.- Aprobación del Factor

EL CLIENTE se obliga a someter a la aprobación del FACTOR cuantas operaciones de venta le sean propuestas por sus compradores.

EL FACTOR tiene derecho a admitir o no dichas ventas, así como las facturas y letras que se produzcan con las ventas aceptadas, en un plazo de [Nº] días contados desde el día de la comunicación por el CLIENTE. Transcurrido dicho plazo sin que el FACTOR devuelva la documentación facilitada por el CLIENTE se entiende que el FACTOR acepta la operación a la que se refiera.

[OPCIONAL — incluir si procede]

(Reserva del cliente)

EL CLIENTE se reserva el derecho a realizar los cobros y gestiones que se refieran a las ventas que no sean aceptadas por el FACTOR así como los relativos a las facturas y letras que no sean admitidos por éste.

Cuarta.- Cláusula de Insolvencia

El FACTOR establecerá límites de clasificación para cada uno de los deudores, y dentro de esos límites asumirá la garantía de insolvencia, según se especifica en el presente contrato, salvo comunicación expresa efectuada al CEDENTE por escrito, dentro de los [Nº] días siguientes hábiles al de la cesión de los créditos.

[OPCIONAL — incluir si procede]

(Retirada y modificación)

Igualmente, el FACTOR ser reserva el derecho de, en todo momento, retirar o modificar las clasificaciones de los deudores.

La aprobación, modificación, o retirada de los límites para los deudores se formalizará con la remisión al CEDENTE de una comunicación escrita específica por cada deudor, debidamente firmada y sellada.

A efectos de este contrato se entiende por insolvencia:

1) La declaración de concurso.
2) El hecho de que el deudor haya establecido con los acreedores un convenio extrajudicial refrendado por el FACTOR que implique una reducción o quita del pasivo.
3) Resultado negativo del auto de embargo, llevado a cabo sobre el patrimonio del deudor, o cuando dicho embargo haya proporcionado una compensación parcial.

La insolvencia existirá efectivamente desde el momento de la declaración de concurso, desde la fecha de refrendo del FACTOR al convenio extrajudicial o desde la fecha en que se haya producido el resultado negativo del autor de embargo.

[OPCIONAL — incluir si procede]

(Riesgos extraordinarios)

No se considerará efectiva la garantía de insolvencia prestada por el FACTOR, sobre los créditos cedidos, en los casos de fuerza mayor, riesgos catastróficos acaecidos a los deudores, moratorias gubernamentales, incautaciones, confiscaciones o expropiaciones, ni ante situaciones de estado de guerra del país o similar (rebeliones, revoluciones, motines u otras hostilidades de naturaleza análoga), desórdenes públicos ni situaciones de huelga o paros laborales que los afecten, ni cuando los créditos no sean admitidos en el pasivo del deudor fallido, o correspondan a contratos nulos, anulados, rescindidos, resueltos, revocados o suspendidos.

Quedarán fuera de la cobertura de insolvencia todos aquellos casos en los que el CEDENTE incumpla las obligaciones previstas en la presente cláusula.

La falta de pago por cualquier otro motivo distinto de la insolvencia será soportada por el CEDENTE, a quien el FACTOR podrá retroceder el crédito

Quinta.- Contraprestación

El cliente entregará el % sobre el nominal de los créditos transmitidos en pago de los servicios prestados por el factor.

Este importe se deducirá por el factor de la cantidad a entregar al cliente en el momento en que se produzcan las liquidaciones pertinentes.

Todos los gastos que ocasione la investigación de la solvencia de los abonados del cliente correrán a cargo del factor, debiendo el cliente facilitar al factor todos los datos que le solicite con referencia a dicho abonado, incluidos los relativos a la propia contabilidad del cliente.

[OPCIONAL — incluir si procede]

(Anticipos)

Previa solicitud, el CLIENTE podrá obtener anticipos sobre los créditos cedidos en los términos señalados en el presente contrato.

Las cantidades anticipadas servirán como garantía frente a las contingencias que puedan surgir en el cobro. El FACTOR podrá adeudar con cargo a este fondo de garantía todos los importes por los que el CEDENTE resulte deudor del FACTOR.

El CEDENTE podrá optar entre las modalidades de anticipo que se indican a continuación:

[ELEGIR UNA OPCIÓN: Modalidad de descuento / Modalidad de crédito]

Sexta.- Duración

La duración del presente contrato es de [PLAZO] a contar desde la fecha de la firma. Finalizado este plazo se entenderá tácitamente prorrogado por un período igual, salvo cuando una de las partes, con al menos treinta días de antelación al vencimiento, comunique a la otra su voluntad contraria a la prórroga. Tal comunicación deberá ser realizada mediante carta certificada con acuse de recibo. Entendiéndose que la extinción será efectiva en relación con las nuevas operaciones a los [Nº] días de la recepción fehaciente de la notificación de la rescisión.

Séptima.- Otras obligaciones del cliente

Por el presente contrato, el CEDENTE asume las siguientes obligaciones:

1) No concederá ni pactará bonificaciones ni variaciones en el valor de los créditos cedidos al FACTOR, salvo con autorización previa y expresa de éste para cada caso particular.
2) En relación con los créditos cedidos, deberá entregar al FACTOR cualquier cantidad recibida de sus deudores, bien sea en pago parcial o total de la suma adeudada.
3) Bajo su responsabilidad, garantiza la vigencia, validez y legitimidad de todos y cada uno de los créditos cedidos, declarando que ha sido realizada la entrega o prestado el servicio y que no existen incidencias relacionadas con una u otro, y que no se debe a los deudores cantidad alguna que pueda ser compensada por éstos, afectando a la cuantía del crédito cedido. También declara que tales créditos no han sido cedidos a ninguna otra entidad y que todos ellos responden a ventas o prestaciones de servicios verdaderos y en ningún caso condicionados, suspendidos en depósito ni sujetos a carga o modo alguno.
4) Transmitir los créditos al FACTOR de modo que éste pueda ejercitar los derechos adquiridos sin impedimento ni defecto en la transmisión.
5) A petición del FACTOR, prestar a éste la asistencia necesaria para ejercer su derecho en caso de litigio, entregándole los documentos y poderes que fuesen necesarios.
6) Responder de la solvencia de los deudores de los créditos cedidos en los casos no cubiertos por el FACTOR, según lo previsto en la cláusula siguiente, de insolvencia.
7) Informar por escrito al FACTOR de todas las incidencias suscitadas por los deudores en relación con los créditos cedidos.
8) Poner a disposición del FACTOR su contabilidad, cuentas y documentos relativos a las operaciones de crédito cedidas.

Octava.- Notificación de la Cesión

El CLIENTE incluirá en todos los contratos que celebre con sus deudores una cláusula por la que éstos se comprometen a pagar su deuda o parte de ella al FACTOR o a quien éste designe.

[OPCIONAL — incluir si procede]

(Por ejemplo)

"El crédito representado por este documento ha sido cedido de forma irrevocable a..., en virtud de contrato de factoring, el único pago liberatorio será el realizado directamente a la citada entidad de factoring".

Asimismo, todas las facturas extendidas por el CLIENTE a cargo de sus deudores deberán incluir un endoso indicativo de que las correspondientes cuentas han sido cedidas al FACTOR, y que son pagaderas a éste o a quien él designe.

Novena.- Cesión

El FACTOR podrá en todo momento transmitir a terceros los créditos que le hayan sido transmitidos por el CLIENTE.

Décima.- Confidencialidad

Tanto el FACTOR como el CLIENTE se comprometen a no divulgar la información y documentación confidencial referente a la otra parte de la que hayan tenido conocimiento por razón de la ejecución del presente contrato, salvo las indispensables para su cumplimiento, y a mantenerla en secreto, incluso después de la finalización del mismo.

Ambas partes acuerdan tomar las medidas necesarias respecto a su personal e incluso terceros que puedan tener acceso a dichas información y documentación, a fin de garantizar la confidencialidad objeto de esta cláusula.

Decimoprimera.- Resolución

Las partes podrán resolver el presente contrato cuando concurra/n alguna/s de las siguientes causas:

- Por el incumplimiento de cualquiera de las obligaciones establecidas en este contrato.

Igualmente, el FACTOR podrá dar por resuelto el presente contrato:

- En cualquiera de los supuestos de disolución, liquidación o cese de actividades del CLIENTE.
- Cuando el porcentaje de impagados (devoluciones sobre créditos vencidos) sea, en [PERIODO], superior al % de la suma de créditos vencidos en igual plazo.
- Cuando el CLIENTE no hiciere anualmente cesión de créditos al FACTOR por importe de [IMPORTE] al menos del % del límite establecido de anticipo de fondos.

Decimosegunda.- Liquidaciones

A la extinción del presente contrato el FACTOR efectuará la liquidación de las cuentas mantenidas con el CLIENTE, según resulte de su contabilidad.

Si la referida liquidación arrojase un saldo favorable al FACTOR, éste será líquido y exigible, estando el CLIENTE obligado a su reintegro en un plazo de... días hábiles a partir de la comunicación que le sea hecha de tal saldo deudor.

Si el CLIENTE no cumpliese con lo establecido en el párrafo anterior, podrá el FACTOR proceder a su reclamación judicial. A estos efectos, se pacta, expresamente, por las partes contratantes, que la liquidación para determinar el saldo que resulte reclamable se practicará por el FACTOR, el cual expedirá la oportuna certificación que recoja el saldo que presente la cuenta del CLIENTE. En su virtud, bastará para el ejercicio de la acción ejecutiva la presentación de este contrato mercantil.

Decimotercera.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Decimocuarta.- Protección de datos personales

LAS PARTES reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

El incumplimiento de cualquiera de LAS PARTES de las obligaciones establecidas en la en la normativa vigente sobre Tratamiento de Datos de Carácter Personal, generará una indemnización en favor de la contraparte de [IMPORTE] euros.

Decimoquinta.- Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE].

Decimosexta.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones del Código de Comercio, de la Ley 10/2014, de 26 de junio, de ordenación, supervisión y solvencia de entidades de crédito, y demás disposiciones legales en vigor.

Decimoséptima.- Fuero competente

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Tribunales de [LOCALIDAD]

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

El FACTOR

________________________________

EL CLIENTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

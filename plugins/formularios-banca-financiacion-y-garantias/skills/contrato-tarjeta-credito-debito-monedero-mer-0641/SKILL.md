---
name: contrato-tarjeta-credito-debito-monedero-mer-0641
description: "Contrato de tarjeta de crédito, débito o monedero. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de tarjeta de crédito, débito o monedero

> Formulario **MER-0641** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de tarjeta de crédito, débito o monedero» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de tarjeta de crédito, débito o monedero” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-tarjeta-credito-debito-monedero-mer-0641`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] FECHA (2 veces)
- [ ] TIPO DE INTERÉS (2 veces)
- [ ] DEPÓSITO VINCULADO
- [ ] DOMICILIO
- [ ] MEDIO DE PAGO
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] Nº DE CUENTA (IBAN)
- [ ] PLAZO
- [ ] TIPO DE TARJETA

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…ratos de crédito al consumo, y en la normativa de transparencia bancaria vigente»: La Ley 7/1995 de crédito al consumo y la Circular 8/1990 están derogadas; la TAE se calcula hoy conforme al anexo I de la Ley 16/2011, de 24 de junio, de contratos de crédito al consumo, y la transparencia bancaria se rige por la Orden EHA/2899/2011 y la Circular 5/2012 del Banco de España. Fuente: BOE-A-2011-10970.
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

Condiciones particulares del contrato:

Tipo de tarjeta [TIPO DE TARJETA] (detallar)

Número de contrato [Nº] (detallar)

Depósito vínculado [DEPÓSITO VINCULADO] (detallar)

Fecha de alta del contrato [FECHA] (detallar)

Caduca final [FECHA] (detallar)

Límite para operaciones a crédito [IMPORTE] (detallar en letra y número €)

Límite para operaciones a débito [IMPORTE] (detallar en letra y número €)

Límite para operaciones con cargo a monedero electrónico [IMPORTE] (detallar en letra y número €)

Tipo de interés aplicable a los pagos aplazados [TIPO DE INTERÉS] (detallar)

T.A.E [PORCENTAJE] (detallar)

Forma de pago [MEDIO DE PAGO] (detallar)

Comisiones de apertura y mantenimiento de la tarjeta [IMPORTE] (detallar € anuales)

Titulares:

Nombre [NOMBRE Y APELLIDOS] (detallar)

N.I.F.: (detallar)

Domicilio [DOMICILIO] (detallar)

Cláusulas

1. Objeto. La tarjeta a la que el presente contrato se refiere es personal e intransferible. El TITULAR designado podrá realizar las operaciones que a continuación se detallan siempre dentro de la red de establecimientos, oficinas y cajeros automáticos integrados en los respectivos sistemas de utilización:

a) Pago de bienes y servicios

b) Obtención de dinero en efectivo, en las propias oficinas de entidades de crédito o a través de cajeros automáticos.

Respecto de las incidencias que puedan surgir entre el TITULAR y terceros, la ENTIDAD queda al margen, sin perjuicio del derecho que le corresponda a interponer las acciones que considere oportunas.

2. Utilización de la tarjeta en establecimientos mercantiles: el TITULAR queda obligado para satisfacer el pago de bienes o servicios, 1. a la presentación de la tarjeta debidamente firmada; 2. a acreditar su identidad en aquellos casos en que le sea solicitado; 3. a la firma del comprobante (factura o nota) que le sea presentado. La firma del comprobante implicará la conformidad de la operación realizada y el compromiso de reembolso de su importe a la ENTIDAD, en el tiempo y forma establecidos.

3. Tarjetas y cajeros automáticos: utilización. Para la correcta utilización de los cajeros automáticos el TITULAR deberá seguir las instrucciones debidamente facilitadas. En todo caso, se operará a través de la introducción de la tarjeta y el pulsado de la clave personal de carácter numérico (número de identificación personal o PIN) que la ENTIDAD haya proporcionado al TITULAR.

4. Tarjeta monedero electrónico: en los supuestos en lo que la tarjeta tenga esta cualidad, se activará mediante recarga a través del adeudo directo y automático de la cuenta asociada a la tarjeta, hasta los límites indicados, en los cajeros automáticos de la ENTIDAD o adheridos o a través de medios on line dispuestos para ello. Se requerirá para la recarga proporcionar el PIN. Para el pago de bienes y servicios deberá procederse a la introducción de la tarjeta en el dispositivo correspondiente y proporcionar la identificación que se solicitase.

En caso de devolución de la tarjeta a la ENTIDAD sin agotar el saldo, ésta procederá a su devolución a la cuenta asociada.

5. Obligación de custodia de la tarjeta. El TITULAR recibe la tarjeta de la ENTIDAD en concepto de comodato. Asume el deber de su custodia, y salvo prueba en contrario, la responsabilidad de su posible uso ilegítimo que pudiera hacerse de la misma hasta el momento en que el TITULAR comunique a la ENTIDAD, sin demora indebida desde que tuvo conocimiento del hecho, la pérdida, sustracción o incidencia ocurrida.

6. Comunicaciones. Modificación del contrato. Conformidad del TITULAR. Cuando la modalidad de la tarjeta sea de crédito (pago diferido o aplazado), y en el caso de que la tarjeta se haya utilizado, la ENTIDAD las comunicará al TITULAR de forma agrupada, en el mes natural en forma de extractos.

En el caso de tarjetas de débito como de crédito, la ENTIDAD, remitirá al menos una vez al año en el mes correspondiente a la fecha de alta del servicio el justificante de adeudo de la cuota anual.

En las comunicaciones a que se hace referencia con anterioridad se notificará al TITULAR las posibles modificaciones del contrato que hayan tenido lugar. La ENTIDAD se reserva el derecho a modificar el tipo de interés y las comisiones establecidas en este contrato si se alteran sustancialmente las condiciones del mercado financiero que motivaron la celebración del presente contrato en las condiciones pactadas. Todas las modificaciones se comunicarán previamente con una antelación de [PLAZO] (detallar) días, que podrá ignorarse si las condiciones son más beneficiosas para el titular.

Los límites de utilización de carácter individual podrán reducirse por parte de la ENTIDAD en caso de concurrencia de cualquiera de las causas expuestas en la cláusula decimotercera.

Todas las modificaciones señaladas en esta cláusula se reconocen sin perjuicio de la facultad de resolución que se reconoce al TITULAR para el caso de que no fuera de su conveniencia el mantenimiento de la vinculación contractual con la ENTIDAD en los nuevos términos contractuales.

7. Modalidades de pago. Se establecen tres posibles modalidades de pago que el TITULAR puede elegir según el tipo de tarjeta utilizado. 1. Débito: adeudo directo y automático en la cuenta asociada. 2. Crédito-pago diferido: adeudo mensual por el total de las cantidades dispuestas. 3. Crédito-pago fraccionado: adeudos mensuales cuyo importe ha de ascender, como mínimo, a [PORCENTAJE] (detallar) parte del saldo deudor de la tarjeta. En este último caso, los cargos periódicos tendrán este mínimo salvo que el saldo dispuesto con al tarjeta sea menor, en cuyo caso, el adeudo se corresponderá con esta cantidad. Si en cualquier momento el saldo dispuesto por mediación de la tarjeta sobrepasa el límite concedido se producirá automáticamente un cargo por el exceso dispuesto.

En todo caso, la cantidad aplazada devengará a favor de la ENTIDAD el tipo de interés nominal [TIPO DE INTERÉS] (detallar)%, que se calculará según la fórmula del interés simple (i: c.r.t: 36.500) siendo i= intereses devengados; c = los saldos mantenidos, r = tipo de interés nominal y t = los días de permanencia.

8. La Tasa Anual Equivalente (T.A.E.) se calculará de acuerdo con la fórmula contemplada en el anexo I de la Ley 16/2011, de 24 de junio, de contratos de crédito al consumo, y en la normativa de transparencia bancaria vigente .

9. Validez y duración. Las tarjetas tendrán un plazo de validez limitado que figurará reflejado en las mismas sin que puedan ser utilizadas con posterioridad a la fecha de caducidad. Las tarjetas se entenderán renovadas por un nuevo periodo de igual duración si un mes antes del vencimiento, ninguna de las partes manifiesta su voluntad en contrario. La ENTIDAD puede, sin embargo, reservarse la facultad de anular o limitar el uso de las tarjetas durante su periodo de vigencia, así como de no renovarlas, perdiendo el TITULAR todos los derechos relativos al uso de las mismas siempre y cuando no se haga un uso inadecuado. Tal anulación deberá ser previamente comunicada al TITULAR y conllevará la de las posibles tarjetas adicionales.

El TITULAR tiene la obligación de devolver las tarjetas cuando renuncie a su uso o la ENTIDAD le comunique su anulación, siendo a su cargo todas las operaciones que se realicen con tales tarjetas hasta la efectiva devolución de las mismas.

Cuando se proceda a renunciar a la utilización de las tarjetas, o la ENTIDAD decida su anulación, conforme a lo que en este contrato se estipula, los titulares de la cuenta asociada y los titulares de las tarjetas quedarán solidariamente obligados a reembolsar la totalidad de la deuda pendiente, más los gastos o cantidades debidas como consecuencia de la anulación, limitación o cese del uso de su tarjeta y, en su caso, de las adicionales, aunque haya optado por el sistema de pago aplazado. El TITULAR de la cuenta asociada y el TITULAR de la tarjeta autoriza expresamente a la ENTIDAD para adeudar en cualquier otra cuenta de su titularidad en la propia ENTIDAD, el importe de su débito derivado de la utilización de la tarjeta. En el supuesto de falta de pago, la ENTIDAD podrá exigir solidariamente a todos los titulares de las cuentas asociadas y a los titulares de las tarjetas, el reintegro de la totalidad de la deuda pendiente, así como los gastos, intereses y demás cantidades que le sean debidas por el uso de las tarjetas. La cantidad líquida exigible por la utilización de las tarjetas será la que se derive de la contabilidad de la ENTIDAD, mediante certificación expedida por ésta, según han convenido las partes.

Con una antelación no inferior a un mes a la caducidad del contrato y de la tarjeta, la ENTIDAD queda autorizada expresamente por el TITULAR para poder remitir a su domicilio, sin necesidad de permiso adicional, una tarjeta sin activar para que reemplace a la tarjeta anterior. Junto a la tarjeta, la ENTIDAD remitirá una propuesta contractual actualizada para sustituir al contrato hasta entonces en vigor así como al folleto de condiciones de valoración y comisiones aplicables. Si restando quince días para la finalización del plazo indicado, el TITULAR no hubiera recibido envío alguno, deberá comunicarlo a la mayor celeridad en cualquier oficina de la ENTIDAD.

La activación de la nueva tarjeta a través de los cajeros automáticos de la ENTIDAD y pulsando el PIN implica la aceptación de la nueva situación contractual. Por el contrario, si transcurrido el tiempo establecido en la propuesta sin que ésta se haya aceptado, caducará totalmente y se tendrá por no emitida.

10. Comisiones. La cuota anual que se pagará por anticipado. Comisión por disposiciones en efectivo tanto en España como en el extranjero diferenciándose si lo son por ventanilla o en cajeros automáticos.

La ENTIDAD cargará en la cuenta asociada la comisión por reclamación de posiciones deudoras que será única y exigible por cada posición deudora, vencida o reclamada.

La comisión por exceso sobre el límite autorizado se calculará tomando como base el límite excedido registrado en cada liquidación, y se liquidará por meses, produciéndose el adeudo en la cuenta asociada.

Todos los pagos y cargos que se efectúen como consecuencia de la utilización, emisión y renovación de las tarjetas, quedan domiciliados en la cuenta asociada, cuyo código [Nº DE CUENTA (IBAN)] (detallar) en la que el TITULAR deberá en todo momento tener saldo suficiente para atender dichos cargos y pagos.

11. Operaciones en el extranjero. Para el adeudo de las sumas derivadas de la utilización de las tarjetas en el extranjero, se aplicará el contravalor en [IMPORTE] € de los $ U.S.A. resultantes de aplicar el tipo de cambio de la divisa en la que se formalizó la operación. Los tipos de cambio serán los vigentes en el momento en que se satisfagan los importes por diferentes centros de compensación. La comisión por cambio de divisas que se aplicará será [PORCENTAJE] (detallar) %, calculándose sobre el contravalor en [IMPORTE] € del importe de la operación.

12. Ingresos en cajeros automáticos de la entidad. Este tipo de operación será posible empleando la tarjeta, pulsando el PIN e introduciendo el dinero en el sobre que facilite el cajero automático en ese momento. El sobre, una vez cerrado, deberá ser colocado en el dispositivo del cajero colocado a tal fin. La máquina emitirá un resguardo de carácter provisional cuya validez estará condicionada al recuento definitivo realizado por la ENTIDAD. El ingreso en la cuenta asociada se producirá el siguiente día hábil bancario y por la cantidad que unilateralmente verifique la ENTIDAD, siendo éste el único procedimiento existente. Si el TITULAR no acepta el método anteriormente descrito y desea estar presente en la apertura del sobre y recuento de su contenido, deberá estar presente en la oficina en la que se encuentre el cajero en el momento en que abra sus puertas al público.

13. Bloqueo de la cuenta asociada y cambio de crédito a débito. La ENTIDAD puede bloquear de forma inmediata el uso de la tarjeta, comunicándoselo previamente al TITULAR, si concurre cualquiera de las circunstancias siguientes: 1. Irregularidades graves o reiteradas del TITULAR en el uso de la tarjeta. 2. Incumplimiento de cualquiera de las obligaciones asumidas por el TITULAR de este contrato. 3. En el caso de fallecimiento del TITULAR, solicitud de concurso voluntario de acreedores o declaración de concurso, o incurriera en alguna causa que disminuya o modifique su capacidad civil. Si la solvencia del TITULAR quedase alterada de forma notoria por incumplimiento de las obligaciones económicas u otras circunstancias que supongan una interrupción de su normal actividad o hagan peligrar su patrimonio. 4. Si el TITULAR se viese en la obligación de reembolsar anticipadamente cualquier crédito obtenido de otras instituciones financieras, sufriera embargo de sus bienes o incurriera en protesto de sus efectos mercantiles. 5. Por falseamiento o inexactitud de la información que el TITULAR ha facilitado a la ENTIDAD. 6. Si se aprecia una reiterada falta de saldo en la cuenta asociada para hacer frente a los pagos derivados del presente contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

El/Los TITULAR/ES ENTIDAD P.P.

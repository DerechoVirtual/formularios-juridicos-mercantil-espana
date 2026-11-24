---
name: poliza-credito-negociacion-descuento-documentos-mer-0661
description: "Póliza de crédito para la negociación o el descuento de documentos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Póliza de crédito para la negociación o el descuento de documentos

> Formulario **MER-0661** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Póliza de crédito para la negociación o el descuento de documentos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Póliza de crédito para la negociación o el descuento de documentos” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:poliza-credito-negociacion-descuento-documentos-mer-0661`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] TIPO DE INTERÉS

## Normas que cita el formulario

- art. 317 Código de Comercio

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

CLÁUSULAS

Este contrato tiene por objeto:

A) Facilitar al ACREDITADO el descuento o la negociación de letras de cambio y/o cualquier otro documento que pueda ser objeto de negociación o descuento.

B) Asegurar al BANCO/CAJA contra los riesgos derivados del descuento y negocia- ción de tales efectos y documentos, bien por falta de pago de los mismos, bien por cualquier otra causa. Asegura el contrato al BANCO/CAJA el buen fin de las letras de cambio y/o cualquier otro documento que tenga descontado o negociado, y descuente o negocie en lo sucesivo, y en los que el acreditado figure como librador, tomador o endosatario, aceptante, endosante o avalista, viniendo el ACREDITADO obligado a satisfacer el importe de tales cambiales o documentos en cuanto por resultar impagados o desatendidos por cualquier otra causa, le fueren presentados al cobro.

La falta de pago de las letras de cambio se acreditará mediante las oportunas actas notariales de protesto, declaración equivalente, o en su defecto, por la mera tenencia por el BANCO/CAJA de las letras de cambio y/o documentos negociados, con posterioridad a la fecha de vencimiento, si la tuviere, y si no la tuviere o fuese a la vista, quince días después de la fecha de descuento.

Sin embargo, el BANCO/CAJA no efectuará el protesto cuando se trate de letras de cambio sobre plazas no bancales, no notariales, cuando contengan la expresión «sin gas- tos» o cuando se trate de letras de cambio defectuosamente extendidas o en las que consten diferentes plazas para pago y protesto.

Se comprenden en este contrato toda clase de letras de cambio y/o cualquier otro documento que sea objeto de negociación o de descuento tomados en firme por el BANCO/ CAJA, cualesquiera que sean las circunstancias del documento o de la negociación, incluyendo el riesgo vigente al día de la fecha, aunque proceda de letras de cambio y/o cualquier otro documento descontado con anterioridad a la misma.

En todo caso, el BANCO/CAJA acepta las letras y/o cualquier otro documento para la negociación o descuento, con las siguientes limitaciones:

a) En aquellos efectos respecto a los que no medien 20 días entre su recepción y vencimiento, la responsabilidad será exclusivamente del cedente si no se efectúa el protesto.

b) El BANCO/CAJA declina toda responsabilidad a que hubiere lugar por falta de datos del librado y, en general, siempre que las letras de cambio adolezcan de algún defecto legal, de cuyas consecuencias responderá exclusivamente el ACREDITADO.

c) El BANCO/CAJA no adquiere responsabilidad de ninguna índole por los daños y perjuicios derivados de los servicios postales de cualquier clase, y en general, en todos de fuerza mayor o caso fortuito.

d) El ACREDITADO manifiesta y responde expresamente de que las letras de cambio y/o cualquier otro documento que se descuente o negocie en virtud de la presente póliza, corresponde a créditos legítimos por razón de operaciones de su actividad, exigibles en su momento y no reclamados o litigiosos, así como que no han sido objeto de traba, embargo o afección alguna.

Asimismo, el ACREDITADO queda responsabilizado de forma única y directa en aquellos supuestos en que se presente al BANCO/CAJA para su negociación o descuento letras de cambio en las que se haya producido, en contra de lo dispuesto por la legislación vigente, un fraccionamiento de la deuda a los efectos de pago del Impuesto sobre Actos Jurídicos Documentados.

El ACREDITADO y los fiadores reconocen adeudar y se obligan a pagar al BANCO/CAJA toda cantidad que resulte cargada en la cuenta especial prevista en la correspondiente cláusula, aun en el supuesto de que sea consecuencia de descuento o negociación de documentos por un importe que sobrepase el límite máximo del crédito concedido.

El descuento de las letras de cambio y/o cualquier otro documento por el ACREDITADO en el BANCO/CAJA, se entenderá siempre hecho «salvo buen fin», y se sujetará a las condiciones ordinarias de esta operación, tanto en la exclusiva facultad del BANCO/CAJA para calificar el papel presentado y para rechazar o admitir la operación, como en lo relativo al tipo de descuento y formas de disposición del líquido. A estos efectos,

el ACREDITADO declara hallarse debidamente informado de las condiciones que rigen la operación de descuento.

Las letras de cambio y/o los documentos descontados o negociados que resultaren total o parcialmente impagados o desatendidos por cualquier otra causa, serán adeudados por el importe no atendido ni compensado en la cuenta especial del BANCO/ CAJA. En la misma cuenta se asentarán cuantos abonos se produzcan por el ACREDITADO para disminuir el saldo deudor.

En el supuesto de que se den las circunstancias previstas en la estipulación séptima, el BANCO/CAJA procederá a cargar en la mencionada cuenta especial las letras, efectos y demás documentos descontados o negociados cuyo vencimiento no se hubiere producido aún, así como los vencidos cuyo resultado de cobro no sea todavía conocido por el BANCO/ CAJA en el momento del cargo.

No obstante, será facultad del BANCO/CAJA exigir el pago inmediato del importe de los mencionados documentos o cargarlos en cualquier otra cuenta, que con saldo acreedor suficiente, tuvieran como titulares tanto el ACREDITADO como los fiadores. La firma de esta póliza por los intervinientes supone un expreso reconocimiento a ese cargo.

A dichos efectos, se entenderá por saldo deudor de dicha cuenta especial, la diferencia entre la suma de los abonos y la suma de los adeudos, más los intereses, comisiones, impuestos y gastos cuyo saldo quedará automáticamente determinado al sentarse en la cuenta cada una de las operaciones que lo integren.

Desde el momento en que la cuenta especial presente un saldo deudor, el ACREDITADO y los fiadores quedarán obligados al reintegro de su total importe.

El saldo negativo de la cuenta a la que se refiere la cláusula anterior devengará a favor del BANCO/CAJA un interés del [TIPO DE INTERÉS] % anual. La liquidación de intereses se realizará trimestralmente, capitalizándose los intereses líquidos y no satisfechos, que como aumento del saldo deudor principal, devengarán nuevos intereses en el trimestre siguiente, conforme a lo que determina el artículo 317 del Código de Comercio.

El ACREDITADO podrá resolver este contrato en cualquier momento. No obstante, deberá pagar el saldo deudor que resulte a su cargo, pero seguirá vigente el contrato hasta la conclusión de las operaciones que hasta entonces se hubieren realizado al amparo de esta póliza, y de las que estuvieren en curso, hasta que todas ellas queden totalmente liquidadas.

El BANCO/CAJA, a su vez, podrá también exigir en cualquier momento el pago del saldo deudor de la cuenta, sin necesidad de notificación o requerimiento alguno. Cerrada la cuenta por el BANCO/CAJA, será exigible su saldo por vía judicial, tanto si el mismo se ha ocasionado por adeudo de efectos impagados y descontados, de sus gastos, comisiones e intereses, como si el citado saldo se ha producido por el vencimiento anticipado de los efectos descontados.

Los fiadores, estipulando expresamente la solidaridad, y renunciando a los beneficios de división, orden y excusión, se obligan solidariamente con el ACREDITADO, viniendo obligados a responder de todas las cantidades que se adeuden al BANCO/CAJA como consecuencia del presente contrato. Para el ejercicio de la acción ejecutiva derivada de esta póliza se conviene expresamente que, de acuerdo con el artículo 520 de la Ley de Enjuiciamiento Civil, será cantidad líquida y exigible la que resulte de certificación expedida por el BANCO/CAJA e intervenida por Notario, acreditativa del saldo que, por todos los conceptos asumidos en la presente póliza, resulten a cargo del ACREDITADO y fiadores, en su caso.

En cualquier caso, será facultad del BANCO/CAJA esperar a que el saldo deudor de la cuenta alcance el límite del crédito concedido.

Será igualmente facultad del BANCO/CAJA la de aplicar, para la cancelación del tal saldo deudor, las cantidades que el ACREDITADO o los fiadores tuvieren a su favor en otras cuentas abiertas en el BANCO/CAJA.

Asimismo, respecto a los valores y activos de todas clases que estén depositados por el ACREDITADO o por cualquiera de los fiadores en el BANCO/CAJA, tanto uno como otro autorizan expresamente a éste para que pueda proceder a su venta y amortice, con el importe de dicha enajenación, las cantidades que resulten adeudadas en virtud del presente contrato.

La firma de esta póliza por los comparecientes supone una expresa aceptación de estos cargos.

Antes de la fecha de su vencimiento, y a los efectos de exigibilidad al ACREDITADO y a los fiadores, el BANCO/CAJA podrá declarar vencidas las letras de cambio y demás documentos descontados, en los siguientes casos:

a) Si el ACREDITADO o cualquiera de los fiadores incumplen sus obligaciones de pago, dejando protestar efectos cambiarios a su cargo o si fuesen requeridos notarial o judicialmente o demandados en reclamación de cantidad.

b) Cuando el ACREDITADO haya presentado al BANCO/CAJA para su descuento efectos cambiarios o cualquier otro documento que se libren contra personas a las que no se haya proveído de fondos.

c) Cuando existan circunstancias objetivas que hagan dudar al BANCO/CAJA del buen fin de los efectos aún pendientes de vencer.

d) El incumplimiento por el ACREDITADO o los fiadores, en su caso, de cualquiera de las obligaciones que se deriven de la presente póliza.

e) Este contrato podrá resolverse por fallecimiento, concurso del ACREDITADO o de cualquiera de los fiadores, solicitud de moratoria, convenio extrajudicial con sus acreedores, liquidación de parte de sus activos, solicitud de concurso o cualquier otra acción o actuación similar, judicial o privada del ACREDITADO o fiadores, o contra ellos, que pueda conducir a idénticos resultados, y también si todos o parte de los bienes de cualquiera de ellos fueran objeto de embargo o sufrieren sensible disminución de su valor. Todos ellos quedan solidariamente obligados a notificar al BANCO/CAJA la producción de cualquiera de los indicados supuestos. Si no lo hicieran, incurrirán en la responsabilidad legalmente establecida.

También podrá resolverse si por cualquier causa el ACREDITADO o fiadores cesaren en la continuidad de su negocio o acordasen su disolución, liquidación, así como fusión o absorción del mismo o el cierre, segregación o escisión de una parte sustancial de sus establecimientos o conjunto de activos patrimoniales, sin recibir a cambio contraprestación equivalente, así como el cambio o modificación del objeto social o de su forma.

Asimismo podrá resolverse cuando sin concurrir las circunstancias previstas en los apartados anteriores, sea presumible una variación en la situación económica del ACREDITADO o fiadores por el impago de efectos a su cargo o la hipoteca, embargo o venta del 20% de su activo patrimonial.

En los casos mencionados, cuando el BANCO/CAJA proceda a aplicar el vencimiento anticipado de las letras de cambio y demás documentos, reintegrará al ACREDITADO, mediante reducción del saldo deudor que aparezca en la cuenta especial prevista en la cláusula de este contrato, el importe de los intereses que el BANCO/CAJA hubiere aplicado en el momento del descuento y que corresponda al período de tiempo existente entre el día de vencimiento anticipado y la fecha de vencimiento que conste en los documentos negociados.

Las letras de cambio y demás documentos que, aun habiendo vencido, fueran carga- dos en la cuenta especial, quedarán retenidos por el BANCO/CAJA como respaldo del saldo que resulte a su favor, hasta que por cualquier medio fuese totalmente liquidada la deuda.

OCTAVA.- Todos los gastos e impuestos de toda clase, presentes y futuros, que origine este contrato serán de cuenta del ACREDITADO, o de los fiadores en su caso, incluidas las costas judiciales y honorarios de Letrado y derechos de Procurador de eventuales procedimientos.

El presente contrato ha sido formalizado con intervención de Notario, a todos los efectos, incluso a los previstos en el número 5 del artículo 517 de la Ley de Enjuiciamiento Civil y el artículo 520 de la misma Ley y demás legislación concordante, sometiéndose las partes a la competencia de los Tribunales de [LOCALIDAD], con renuncia del fuero actual o futuro.

Todos los efectos derivados del presente contrato serán extensivos a las negociaciones y descuentos que se realicen en el BANCO/CAJA por letras o documentos negociables, extendidos a favor de la firma comercial [DENOMINACIÓN SOCIAL], de la que los ACREDITADOS se declaran titulares y responsables únicos.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Las partes manifiestan su conformidad al contenido de la presente póliza, la otorgan y firman, y yo el Notario doy fe de todo lo contenido en esta póliza, de haberse verificado el otorgamiento del presente contrato, así como la identidad y capacidad legal de los contratantes y de la legitimidad de sus firmas.

BANCO/CAJA EL ACREDITADO LOS FIADORES Con mi intervención

El Notario

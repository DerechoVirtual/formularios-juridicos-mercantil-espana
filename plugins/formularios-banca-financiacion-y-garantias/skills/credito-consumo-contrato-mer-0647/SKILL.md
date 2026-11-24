---
name: credito-consumo-contrato-mer-0647
description: "Crédito al consumo (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Crédito al consumo (contrato)

> Formulario **MER-0647** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Crédito al consumo (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Crédito al consumo (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:credito-consumo-contrato-mer-0647`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] PORCENTAJE (3 veces)
- [ ] TIPO DE INTERÉS (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] FECHA
- [ ] IMPORTE
- [ ] LUGAR Y FECHA
- [ ] NOMBRE Y APELLIDOS
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 317 Código de Comercio
- art. 32 Ley 16/2011

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

Condiciones particulares del contrato:

Lugar y fecha de otorgamiento [LUGAR Y FECHA]

CLIENTE/S (en el caso de ser varios CLIENTES PRESTATARIOS, quedan todos ellos obligados solidariamente al cumplimiento de las obligaciones derivadas de este contrato frente a la ENTIDAD PRESTAMISTA. En caso de intervención de personas casadas, éstas quedan comprometidas a no variar su régimen económico matrimonial sin dejar expresamente a salvo las obligación contraídas con la ENTIDAD PRESTAMISTA por razón del contrato a celebrar, incluso aunque la modificación se inscriba en los Registros Civil y Mercantil.)

Avalista/s

Representante de la ENTIDAD [NOMBRE Y APELLIDOS]

Datos del bien a financiar [DESCRIPCIÓN DEL BIEN]

Cláusulas

1. Intereses: el préstamo devengará a favor de la ENTIDAD PRESTAMISTA el tipo de interés [TIPO DE INTERÉS] (detallar) %, efectuándose la liquidación y pago de los intereses de la siguiente forma:

a) Durante el periodo de carencia, el cálculo de los intereses, se efectuará diariamente multiplicando el principal pendiente del préstamo por el interés nominal [TIPO DE INTERÉS]. Establecido en este contrato dividiendo su resultado por 36.000. Los intereses a adeudar al final de cada periodo de liquidación serán la suma aritmética de los devengos producidos en cada uno de los días incluidos en dicho periodo.

b) Durante el periodo de amortización el cálculo de los intereses se efectuará mensualmente multiplicando el principal pendiente del préstamo por el tipo de interés nominal establecido en este contrato por el número de meses comprendido en cada periodo de liquidación y dividiendo el resultado por 1.200.

c) Los intereses serán adeudados en la cuenta del prestatario.

d) Interés de demora: sin perjuicio del derecho de la ENTIDAD PRESTAMISTA a dar por vencido de forma anticipada el préstamo, tal y como más adelante se detalla, las cantidades adeudadas por intereses y amortizaciones de principal, no satisfechas en la fechas previstas, devengarán desde el día siguiente de las mismas, el interés de demora pactado en las condiciones particulares, pudiendo la ENTIDAD considerarlos capital, conforme a lo previsto por el artículo 317 del Código de Comercio.

Para la liquidación de intereses se utilizará la fórmula del interés simple (i: c.r.t: 36.500) que se calculará sobre los saldos mantenidos (medios o diarios), siendo i= intereses devengados; c = los saldos mantenidos, r = tipo de interés nominal y t = los días de permanencia, salvo los años bisiestos en cuyo caso el divisor será 36.000.

2. T.A.E: la Tasa Anual Equivalente (T.A.E.) se calculará de acuerdo con lo dispuesto en el artículo 32 de la Ley 16/2011, de 24 de junio, de contratos de crédito al consumo.

3. Amortización: el presente contrato se amortizará mediante [ÓRGANO] (detallar) número de cuotas sucesivas, comprensivas de capital e intereses [IMPORTE] (detallar) cantidad en número y letra, cada una, devengándose la primera de ella el [FECHA] (detallar) fecha, y la última el día del vencimiento fijado en este contrato. Las cuotas previstas habrán de hacerse efectivas por el CLIENTE PRESTATARIO sin que sea necesario realizar requerimiento alguno en el día del vencimiento señalado para cada una de ellas. El CLIENTE podrá optar por la domiciliación de las precitadas cantidades en el banco o caja de ahorros que designe.

El CLIENTE PRESTATARIO puede proceder a la cancelación anticipada del préstamo, bien de forma total o parcial. En tal caso, el CLIENTE no tendrá derecho a la restitución de la comisión ni de los intereses percibidos por la ENTIDAD. Las citadas entregas anticipadas serán aplicadas, por este orden, al reintegro de las costas y gastos suplidos por la ENTIDAD; al pago de los intereses de demora; al pago de los intereses del principal y por último, a la amortización del capital objeto del préstamo.

En caso de amortización parcial, el CLIENTE puede optar entre la reducción del importe de las cuotas y la reducción del plazo de amortización del préstamo.

En el caso de amortización total anticipada, los intereses devengados desde la fecha de la última liquidación hasta la fecha de la cancelación se calcularán diariamente multiplicando el capital pendiente del préstamo por el tipo de interés nominal establecido y procediendo a su división por 36.000.

4. Comisiones. El presente préstamo devengará a favor de la ENTIDAD una comisión de apertura [PORCENTAJE] (detallar) % que será liquidada y pagada en el mismo momento de la formalización del contrato por el CLIENTE. Se establecen, igualmente, las siguientes comisiones de cancelación parcial [PORCENTAJE] (detallar) % y de cancelación total [PORCENTAJE] (detallar) %, para el supuesto de que el cliente opte por una amortización anticipada.

5. Derechos de la ENTIDAD PRESTAMISTA: No obstante lo previsto en la cláusula número 3, la ENTIDAD PRESTAMISTA podrá considerar el vencimiento del préstamo y exigir la devolución de la suma que por capital, gastos, intereses y comisiones le deba el CLIENTE PRESTATARIO, en el supuesto de que concurra alguna de las siguientes circunstancias: 1. por el incumplimiento de cualquiera de las obligaciones contraídas en este contrato. 2. por la inexactitud comprobada y ocultación de los datos proporcionados a la ENTIDAD PRESTAMISTA con anterioridad a la concesión de este contrato. La citada conducta ha de dar lugar a una valoración del riesgo de la operación incompleta o errónea. 3 por conductas del CLIENTE PRESTATARIO o de cualquiera de sus avalistas que pongan en peligro su solvencia. 4. por la declaración de concurso de acreedores o resolución admitiendo a trámite el concurso que suponga la indisponibilidad o cesión total o parcial de sus bienes por el CLIENTE PRESTATARIO, así como por embargo de los bienes, intervención administrativa o judicial de todos o parte de los bienes del CLIENTE PRESTATARIO. 5. Si concurriera cualquiera de las causas de vencimiento anticipado previstas en la legislación vigente.

Si el préstamo resultare vencido por la llegada de su término o por cualquiera de las causas previstas en este apartado, la ENTIDAD PRESTAMISTA podrá exigir el pago vía ejecutiva en el caso de que el CLIENTE PRESTATARIO no hiciese el pago de la suma adeudada en el mismo día del vencimiento o en el siguiente en atención al calendario, si fuese festivo. Con la intención de proporcionar mayor seguridad jurídica al CLIENTE PRESTATARIO y a efectos meramente procesales, la ENTIDAD PRESTAMISTA practicará la liquidación de intereses y demás conceptos adeudados, sumados al débito por principal prestado, determinando con ello la deuda ejecutivamente exigible. La ENTIDAD practicará la correspondiente certificación que recoja el saldo pendiente el día del cierre. Bastará para el ejercicio de la acción ejecutiva la presentación de este contrato, junto con la certificación prevista en el artículo 517 de la Ley de Enjuiciamiento Civil y legislación concordante, así como la presentación de la documentación señalada en el artículo 573.1 de la Ley de Enjuiciamiento Civil.

6. Avalistas. El/los avalista/s designados garantiza/n solidariamente entre sí y con el CLIENTE PRESTATARIO, en términos idénticos a éste último, cuantas obligaciones se contraen en el presente contrato, incluso aunque no aparezca/n expresamente mencionado/s en algunas de las cláusulas que lo conforman y, en especial, en relación al pago del principal, intereses y comisiones. En el caso de que la ENTIDAD PRESTAMISTA deje las obligaciones derivadas de este contrato vencidas o sin reclamar, no se entenderá como una prórroga a efectos de liberar al/los avalista/s.

7. Gastos e impuestos. Serán de cuenta del CLIENTE PRESTATARIO todos los gastos e impuestos que se deriven del presente préstamo durante su vigencia, incluso los gastos de carácter judicial o extrajudicial, comprendidos los abogados y procuradores, que pudiera generar su ejecución y cobro, los que se satisfagan por la formalización del contrato de este contrato como de los documentos a que se refieren las condiciones que preceden, así como los gastos derivados de medios de comunicación, según las tarifas vigentes.

8. Carácter no exclusivo de la operación. La financiación percibida a través de la realización de este contrato carece de carácter exclusivo permitiéndose al CLIENTE PRESTATARIO realizar el pago de los bienes adquiridos en el comercio al contado, a través de la financiación que procuren otras entidades de crédito o mediante la utilización de tarjetas y otras formas de obtención de crédito. La ENTIDAD PRESTAMISTA no asume ninguna responsabilidad que pueda derivarse de la realización de operaciones comerciales o de los bienes que por medio de este préstamo al consumo sean adquiridos.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

La ENTIDAD PRESTAMISTA EL CLIENTE PRESTATARIO

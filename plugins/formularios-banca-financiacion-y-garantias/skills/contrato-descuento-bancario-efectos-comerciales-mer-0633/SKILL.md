---
name: contrato-descuento-bancario-efectos-comerciales-mer-0633
description: "Contrato de descuento bancario de efectos comerciales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de descuento bancario de efectos comerciales

> Formulario **MER-0633** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de descuento bancario de efectos comerciales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de descuento bancario de efectos comerciales” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-descuento-bancario-efectos-comerciales-mer-0633`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (3 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] ENTIDAD BANCARIA
- [ ] IMPORTE
- [ ] MES
- [ ] NÚMERO
- [ ] PLAZO
- [ ] SUCURSAL
- [ ] TIPO DE INTERÉS

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

En la localidad/ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte, D [NOMBRE Y APELLIDOS], mayor de edad, en representación de la entidad bancaria [ENTIDAD BANCARIA], oficina [SUCURSAL], con domicilio en [LOCALIDAD] y titular del CIF [NIF], en calidad de descontante (en adelante el BANCO),

Y de otra, D [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD] y titular del NIF [NIF], en calidad de descontatario (en adelante el CLIENTE);

MANIFIESTAN

Que reconociéndose mutuamente las partes, según intervienen, la capacidad legal necesaria a los efectos de este CONTRATO DE DESCUENTO, en la representación expresada, siendo responsables de la veracidad de sus manifestaciones, y de forma libre, espontánea y de mutuo acuerdo, convienen formalizar el contrato con arreglo a las siguientes

CLÁUSULAS

Objeto

El BANCO concede una línea de crédito a favor del CLIENTE, con un límite máximo de [IMPORTE] euros, con objeto de facilitar el descuento de los créditos que el CLIENTE ostente contra terceros, que respondan a operaciones comerciales realizadas por el mismo, representados o comunicados al banco en la forma que se establece en el presente contrato.

El CLIENTE asumirá el riesgo crediticio de los deudores de los instrumentos descontados, de manera que la titularidad del crédito será cedida al BANCO salvo buen fin.

Operaciones de descuento

Los instrumentos con contenido crediticio objeto de descuento deben ser de libre disposición del CLIENTE. Las operaciones de descuento no podrán realizarse con instrumentos vencidos.

Los instrumentos pueden ser letras de cambio, facturas conformadas y títulos valores representativos de deuda, así definidos por las leyes y reglamentos de la materia. Dichos instrumentos se transferirán mediante endoso o por cualquier otra forma que permita la transferencia a favor del BANCO, debiendo el CLIENTE comunicar a los deudores la operación de descuento en un plazo no superior a dos días.

La suma de los importes descontados en cada momento por el CLIENTE no excederá del límite señalado en la cláusula anterior.

Abono del descuento, intereses y liquidaciones

El BANCO se reserva el derecho a aceptar o rechazar, total o parcialmente, los créditos que el CLIENTE le presente para su descuento.

En el caso de que los acepte, el BANCO abonará el importe de los créditos en la cuenta núm [NÚMERO], descontando los intereses.

Se pacta un interés del [TIPO DE INTERÉS] % anual, que se calculará desde la fecha del descuento a la del vencimiento del respectivo crédito. Si los créditos no tuvieren fecha de vencimiento, se considerará que son créditos a la vista.

Los intereses devengados se calcularán mediante la aplicación de la siguiente fórmula:

c (nominal del efecto) x r (tipo de interés nominal) x t (días naturales hasta fecha vencimiento)

____________________________________________________________________________

36.000

De acuerdo a lo dispuesto en la Circular 5/2012, de 27 de junio, del Banco de España, el BANCO deberá realizar las correspondientes liquidaciones en las que incluirá en todo caso: a) Nominal;:b) Vencimiento; c) Días de descuento; d) Tipo de descuento contractual aplicado; e) Tipo de interés nominal (anual) equivalente; f) Importe de los intereses que resultan; g) Impuestos liquidados, en su caso, con expresión del tipo y la base de cálculo; h) Comisiones aplicadas, con indicación concreta de su concepto, base y período de devengo, separando claramente cada concepto que haya dado lugar al devengo de comisión; i) Gastos que la entidad pueda haber aplicado con indicación concreta de su concepto, separando claramente cada concepto de gasto, si hubiera varios; j) Los importes anteriores se detallarán en la moneda original del instrumento y en la que vaya a efectuarse la liquidación, si fueran diferentes, añadiendo entonces el tipo de cambio aplicado; y k) Tasa anual equivalente (TAE).

Cobro de los efectos

Los créditos endosados al BANCO serán gestionados para su cobro a la fecha del vencimiento.

A tal fin, el BANCO podrá realizar todos los actos de disposición con relación a los instrumentos descontados, cobrar los títulos a su vencimiento y, en caso de incumplimiento, formular el correspondiente protesto de ser necesario, realizar las gestiones de cobranza extrajudicial y, en su caso, iniciar las acciones judiciales que fueran necesarias.

En cualquier caso los descuentos se entienden efectuados salvo buen fin, por lo que el CLIENTE responde de la solvencia de los deudores, así como de la existencia y legitimidad del crédito.

Si finalmente los créditos descontados resultaren total o parcialmente impagados, el CLIENTE viene obligado a satisfacer su importe, con los intereses y gastos de la operación.

Derechos y obligaciones de las partes

Los derechos y obligaciones de las partes son las que resultan de las anteriores cláusulas, en especial las siguientes:

1) El CLIENTE debe transmitir el crédito descontado al BANCO, comunicándolo al deudor en el plazo estipulado y absteniéndose de realizar cualquier acto tendente a su cobro total o parcial.

2) El CLIENTE está obligado a pagar los intereses y gastos pactados al BANCO a cambio de obtener la liquidez derivada del descuento de los créditos

3) El CLIENTE debe restituir el importe anticipado en caso de impago del deudor.

4) El CLIENTE debe informar al BANCO sobre cualquier circunstancia relevante sobre las operaciones de descuento y utilizar los formularios proporcionados por EL BANCO para la presentación de los efectos sujetos a descuento

5) El BANCO debe entregar al CLIENTE el importe descontado

6) El BANCO ha de presentar el crédito al cobro llegado su vencimiento y realizar diligentemente los actos necesarios para la conservación y cobro del mismo.

7) El BANCO deberá comunicar inmediatamente al CLIENTE las operaciones que no han llegado a buen fin, siendo responsable en otro caso del perjuicio derivado por la demora.

Plazo

El presente contrato tendrá una duración de [PLAZO] y concluirá sin necesidad de aviso previo alguno.

Cualquiera de las partes podrá ponerle término al presente contrato antes de su vencimiento, siempre que se comunique fehacientemente a la otra parte con una antelación mínima de

Resolución del contrato

Sin perjuicio de la facultad de las partes de dar por vencido este contrato voluntariamente, en la forma prevista en la cláusula anterior, el contrato podrá resolverse por incumplimiento de las partes de cualquiera de las obligaciones contraídas en este contrato y, además, por no continuar el CLIENTE en su negocio, por ser declarado en concurso o se produzca merma patrimonial que comprometa la solvencia tenida en cuenta a la hora de conceder este contrato de descuento.

En el caso de resolución del contrato por incumplimiento de una de las partes, la otra parte podrá reclamar la correspondiente indemnización de daños y perjuicios.

En caso de resolución anticipada, el BANCO podrá retener los créditos en concepto de prenda y como garantía del saldo deudor que presente la cuenta, pudiendo gestionar su cobro y aplicarlo a la reducción del saldo impagado hasta su total liquidación.

Gastos e impuestos

Todos los gastos e impuestos que origine el presente contrato, incluidos los de otorgamiento de póliza, aranceles y honorarios serán de cuenta del CLIENTE.

Domicilio a efectos de comunicaciones

A efectos de notificaciones, requerimientos y comunicaciones a que dé lugar el presente contrato, los domicilios del CLIENTE y del BANCO serán los designados en el encabezamiento del presente contrato, a no ser que medie notificación fehaciente de cualquiera de las partes comunicando el cambio de dicho domicilio.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

En prueba de conformidad, una vez leído el contrato, ambas partes firman el presente documento, por duplicado y aun sólo efecto, en el lugar y fecha indicados en el encabezamiento.

EL CLIENTE

Fdo.

EL BANCO

Fdo.

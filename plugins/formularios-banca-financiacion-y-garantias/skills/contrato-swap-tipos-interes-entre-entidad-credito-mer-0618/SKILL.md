---
name: contrato-swap-tipos-interes-entre-entidad-credito-mer-0618
description: "Contrato de swap de tipos de interés entre entidad de crédito y cliente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de swap de tipos de interés entre entidad de crédito y cliente

> Formulario **MER-0618** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de swap de tipos de interés entre entidad de crédito y cliente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de swap de tipos de interés entre entidad de crédito y cliente” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-swap-tipos-interes-entre-entidad-credito-mer-0618`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (3 veces)
- [ ] PROVINCIA (3 veces)
- [ ] NIF/DNI (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FECHA DE CONSTITUCIÓN
- [ ] FECHAS
- [ ] IMPORTE
- [ ] INSCRIPCIÓN
- [ ] MES
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº
- [ ] NÚMERO
- [ ] PERIODICIDAD
- [ ] PORCENTAJE
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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], dirección [DIRECCIÓN] provisto/a del N.I.F. número [NIF/DNI]

de otra parte

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA] provisto/a del N.I.F [NIF/DNI]

INTERVIENEN

D./Dña. [NOMBRE Y APELLIDOS], interviene en nombre y representación de EL BANCO de [DENOMINACIÓN SOCIAL], CIF [NIF], domiciliado en [DOMICILIO] y constituido en [FECHA DE CONSTITUCIÓN] ante el Notario de [LOCALIDAD] D. [NOMBRE DEL NOTARIO], en fecha [FECHA] e inscrito en el Registro Mercantil de [LOCALIDAD], inscripción [INSCRIPCIÓN], en adelante el BANCO.

D./Dña. [NOMBRE Y APELLIDOS], interviene en su propio nombre y representación, en adelante EL CLIENTE.

MANIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE SWAP, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

Que el CLIENTE mantiene con el BANCO determinadas operaciones financieras, entre ellas un préstamo referenciado a tipo de interés variable.

Que el CLIENTE desea cubrir, total o parcialmente, el riesgo de variación del tipo de interés asociado a dichas operaciones.

Que el BANCO está dispuesto a suscribir con el CLIENTE una permuta financiera de tipos de interés (en adelante, el "Contrato de Swap"), operación que queda sujeta a las siguientes

CLÁUSULAS

PRIMERA. – Objeto

Por medio del presente Contrato, las partes convienen en intercambiar entre sí, en las fechas y condiciones aquí previstas, ciertos flujos de intereses calculados sobre un importe nominal de referencia, con el fin de que el CLIENTE limite su exposición al riesgo de variación de tipos de interés.

Este Contrato no supone concesión de un préstamo ni entrega del importe nominal, que tiene carácter meramente teórico o de referencia.

SEGUNDA. – Importe nominal y duración

El importe nominal de referencia será de [IMPORTE] euros.

El Swap comenzará el día [FECHA] y finalizará el día [FECHA]., salvo resolución anticipada conforme a este Contrato.

Las liquidaciones se efectuarán con periodicidad [PERIODICIDAD], tomándose como fechas de liquidación los días [FECHAS] de cada periodo.

TERCERA. – Tipos de interés aplicables

Sobre el importe nominal se calcularán dos tipos de interés:

En cada periodo de liquidación, el CLIENTE deberá pagar a EL BANCO intereses calculados aplicando un tipo de interés fijo del [PORCENTAJE] % anual.

En cada periodo de liquidación, el BANCO deberá pagar al CLIENTE intereses calculados aplicando un tipo de interés variable del [TIPO DE INTERÉS] (Euríbor a 3 meses + [Nº] puntos porcentuales), tomado como valor el publicado dos días hábiles anteriores al inicio de cada periodo de liquidación.

Los intereses se calcularán tomando como base un año de 365 días y el número de días efectivamente transcurridos en cada periodo.

CUARTA. – Liquidación y pagos

4.1. Determinación del importe de cada parte

En cada periodo, se calcularán:

- Intereses correspondientes al tipo fijo (a cargo del CLIENTE).
- Intereses correspondientes al tipo variable (a cargo del BANCO).

4.2. Liquidación por diferencias

En cada Fecha de Liquidación se compensarán ambos importes y:

- Si los intereses fijos son mayores que los variables, el CLIENTE abonará al BANCO la diferencia.
- Si los intereses variables son mayores que los fijos, el BANCO abonará al CLIENTE la diferencia.

4.3. Forma de pago

Los pagos se efectuarán mediante adeudo o abono en la cuenta que tiene abierta el CLIENTE en el BANCO, con número [NÚMERO], que se designa en este acto, efectuándose los pagos con valor en la propia fecha de Liquidación.

No existirán otros flujos de dinero entre las partes distintos de los previstos en esta cláusula y, en su caso, los derivados de la cancelación anticipada.

QUINTA. – Relación con otras operaciones

Este contrato es independiente de cualquier préstamo u operación de financiación que el CLIENTE mantenga con el BANCO, aun cuando se haya celebrado con la finalidad de cubrir el riesgo de tipo de interés de dicha operación.

El incumplimiento o cancelación del préstamo u otra operación subyacente no implica por sí mismo la terminación de este Contrato, salvo pacto expreso en contrario.

SEXTA. – Cancelación anticipada y valoración

6.1. El CLIENTE podrá solicitar en cualquier momento la cancelación anticipada del Contrato, mediante notificación escrita al BANCO con una antelación mínima de treinta días hábiles.

6.2. En caso de cancelación anticipada a petición del CLIENTE, el BANCO valorará el Swap a precio de mercado en la fecha de cancelación, de acuerdo con sus modelos internos de valoración, teniendo en cuenta los tipos de interés vigentes, el plazo restante y demás parámetros relevantes.

6.3. Si el valor de mercado del Contrato resultara favorable al BANCO, el CLIENTE deberá abonar a EL BANCO el importe de dicho valor como compensación por cancelación. Si el valor de mercado resultara favorable al CLIENTE, EL BANCO abonará dicho importe al CLIENTE.

6.4. EL BANCO facilitará al CLIENTE, a solicitud de éste, una explicación razonable del criterio de valoración utilizado.

SÉPTIMA. Información y conocimiento del producto

7.1. El CLIENTE declara que:

a) Ha recibido de EL BANCO información suficiente sobre la naturaleza, características y riesgos del Swap.
b) Comprende que el resultado económico del Contrato depende de la evolución de los tipos de interés, pudiendo ser favorable o desfavorable para él.
c) Es consciente de que la cancelación anticipada puede originar costes

7.2. EL BANCO manifiesta haber cumplido las obligaciones de información y evaluación de conveniencia que le resulten aplicables conforme a la normativa vigente en materia de mercados de instrumentos financieros.

OCTAVA. Incumplimiento

8.1. Se considerará incumplimiento del CLIENTE, entre otros supuestos:

a) La falta de pago de cualquier cantidad debida en virtud de este Contrato.
b) La declaración de concurso, insolvencia o situación similar del CLIENTE.
c) El incumplimiento grave de otras obligaciones financieras frente a EL BANCO.

8.2. En caso de incumplimiento del CLIENTE, EL BANCO podrá:

a) Declarar vencido anticipadamente el Contrato y exigir su liquidación total mediante valoración a precio de mercado, conforme a lo previsto en la cláusula 6.
b) Compensar las cantidades resultantes con cualesquiera saldos que el CLIENTE mantenga en EL BANCO, en la medida en que lo permita la normativa aplicable.

NOVENA. – Impuestos y gastos

Todos los impuestos, tasas o gastos que se deriven de la formalización, ejecución o cancelación del presente Contrato serán de cargo de la parte a quien corresponda legalmente su pago, salvo pacto distinto.

DÉCIMA. – Comunicaciones

Toda comunicación relacionada con este Contrato deberá efectuarse por escrito y se considerará válida si se envía a los domicilios que constan en el encabezamiento, o a aquellos otros que las partes hayan notificado por escrito con posterioridad.

UNDÉCIMA. – Ley aplicable y jurisdicción

11.1. El presente Contrato se regirá e interpretará conforme a la ley española.

11.2. Para cuantas cuestiones litigiosas pudieran derivarse de su interpretación o cumplimiento, las partes se someten, con renuncia expresa a cualquier otro fuero que pudiera corresponderles, a los Juzgados y Tribunales de [ciudad], salvo que por imperativo legal corresponda otro fuero.

Y en prueba de conformidad, las partes firman el presente Contrato, por duplicado ejemplar y a un solo efecto, en el lugar y fecha indicados en el encabezamiento.

EL BANCO

EL CLIENTE

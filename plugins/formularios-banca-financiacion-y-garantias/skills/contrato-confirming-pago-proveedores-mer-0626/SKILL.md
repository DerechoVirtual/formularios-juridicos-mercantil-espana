---
name: contrato-confirming-pago-proveedores-mer-0626
description: "Contrato de confirming de pago a proveedores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de confirming de pago a proveedores

> Formulario **MER-0626** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que una entidad financiera gestiona los pagos de una empresa a sus proveedores, ofertándoles de ordinario a estos últimos la posibilidad de cobrar las facturas con anterioridad a la fecha de vencimiento.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de confirming de pago a proveedores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de confirming de pago a proveedores” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-confirming-pago-proveedores-mer-0626`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] Nº (5 veces)
- [ ] DNI/NIE (4 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] PLAZO (2 veces)
- [ ] LUGAR
- [ ] NÚMERO
- [ ] PERIODICIDAD
- [ ] PORCENTAJE
- [ ] ÓRGANO

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

Contrato por el que una entidad financiera gestiona los pagos de una empresa a sus proveedores, ofertándoles de ordinario a estos últimos la posibilidad de cobrar las facturas con anterioridad a la fecha de vencimiento.

Notas al pie del formulario original:
(1) El Banco Santander tiene registrado el nombre de "confirming" como marca nacional (número 1.749.430 de la clase 36 para "servicios de negocios financieros y monetarios. Servicios administrativo- financieros prestados a empresas en la gestión de pagos a sus proveedores. Servicio de factoring (operaciones de gestión de cobro de créditos y de anticipo de fondos sobre los mismos). Servicios de agencias para el cobro de deudas. Servicios de seguros"), lo que origina polémica sobre la utilización de este término, empleándose otras denominaciones como Pago Certificado, Programa Flexible de Pagos o Servicio de Pago a Proveedores, si bien el Tribunal Supremo, Sala Tercera, en Sentencias de 17 de noviembre de 2004, 25 de octubre del mismo año y 1 de febrero de 2006 expone que tal expresión ha devenido por la propia fuerza de los hechos en una utilización que ha adquirido una gran difusión en el mercado bancario, referida a la prestación de unos servicios determinados por las entidades bancarias, admitiendo como marcas aquellas que combinan tal expresión con otras, normalmente referidas a una entidad bancaria


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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ENTIDAD FINANCIERA.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

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

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de CONFIRMING y, a tal fin,

MANIFIESTAN

I. Que el Cliente ha solicitado a la Entidad que realice en su nombre la gestión de pago a sus proveedores, de las facturas emitidas por éstos y su cargo.

II. Que la Entidad ha aceptado llevar a cabo la gestión de los pagos a que se refiere la manifestación anterior.

III. Que por ello ambas partes acuerdan llevar a efecto el presente contrato de CONFIRMING mediante las siguientes

CONDICIONES

Primera.- Objeto

a) La gestión, administración y pago por la entidad financiera de los créditos que contra el cliente correspondan a sus proveedores a consecuencia de operaciones del tráfico empresarial habitual entre ambos, bien sean anteriores o posteriores a la firma del presente contrato.

b) La proposición de cesión y cesión, en su caso, a favor de la entidad financiera de los créditos que los proveedores del cliente ostenten legítimamente frente a éste derivados de las operaciones de tráfico habitual de la empresa, bien sean anteriores o posteriores a la firma del presente contrato.

c) <la prestación por parte de la entidad financiera de servicios de asesoramiento, control y gestión de los créditos de proveedores al cliente.

Segunda.- Límite de riesgo

La entidad financiera adquirirá créditos de los proveedores hasta un límite máximo global de [IMPORTE] euros.

Tercera.- Remuneración

La entidad financiera percibirá del cliente como remuneración de sus funciones el [Nº] por ciento nominal de los créditos transferidos. El pago se efectuará el [FECHA] en la cuenta corriente núm. [Nº]

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho a la entidad financiera a exigir al cliente un interés moratorio del [PORCENTAJE] % respecto de cada uno de los pagos no satisfechos puntualmente. Si el cliente se retrasara en el pago de [Nº] plazos o en el pago del último, la entidad financiera podrá optar entre exigir el pago de las cantidades pendientes o resolver el contrato, con abono en ambos caso de las indemnizaciones que puedan corresponder.

Las liquidaciones entre la entidad financiera y el cliente serán de carácter [PERIODICIDAD]

Cuarta.- Obligaciones del cliente

El cliente se obliga:

a) a no conceder ni pactar bonificaciones ni variaciones sobre la cuantía de las deudas ni de las fechas de pago de las facturas emitidas por los proveedores. Las modificaciones sólo podrán efectuarse con la expresa autorización de la entidad financiera;
b) a notificar a la entidad financiera, las facturas a su cargo emitidas por los proveedores y conformadas por el propio cliente;
c) a garantizar bajo su responsabilidad la vigencia, validez y legitimidad de los créditos comunicados, declarando que sobre los mismos no existe traba o gravamen;
d) a comunicar los créditos de proveedores a la entidad financiera de forma que ésta pueda realizar los servicios previstos en el contrato;
e) a informar a la entidad financiera de cuantas eventualidades suscitadas por los proveedores o por terceros puedan darse en relación con los créditos transmitidos.

Quinta.- Obligaciones de la Entidad Financiera

La entidad financiera se obliga:

a) a recibir del cliente las relaciones de facturas conformadas y documentos cambiarios aceptados por éste dentro del límite establecido en la cláusula segunda;
b) a contabilizar y controlar los créditos de los proveedores a cargo del cliente cedidos a la entidad financiera por aquellas operaciones comerciales que dichos proveedores hayan realizado con el cliente y hayan sido comunicadas por éste a la entidad financiera;
c) a pagar a los proveedores del cliente los créditos a cargo de éste que legítimamente les correspondan y que se encuentren incluidos en las relaciones que aquél remita a la entidad financiera según lo previsto en la letra a) de esta cláusula;
d) a informar al cliente, en el plazo de días desde que se produzca la cesión, de los créditos a su cargo que la entidad financiera adquiera de los proveedores.

Sexta.- Notificaciones entre las partes

Del cliente a la entidad financiera:

El cliente deberá comunicar a la entidad financiera las facturas a su cargo a las que haya dado su conformidad, quedando igualmente obligado a comunicar los documentos cambiarios aceptados y sus condiciones fundamentales de cantidad y plazo.

Esta comunicación se realizará mediante [ÓRGANO] según el modelo que se acompaña como anexo.

De la entidad financiera a los Proveedores:

Una vez que la entidad financiera reciba la información señalada en la cláusula precedente, detallará por escrito a los proveedores del cliente las facturas que por ellos han sido emitidas y los documentos cambiarios formalizados ofreciéndoles mediante dicho escrito la posibilidad de ceder en firme y sin recurso los créditos a la entidad financiera.

De la entidad financiera al cliente

La entidad financiera notificará al cliente en el plazo de [Nº] días desde cada cesión de los créditos que haya adquirido de los proveedores de éste. Por el presente acto el cliente reconoce expresamente que dicha comunicación le obliga a pagar a la entidad financiera, a su vencimiento, el importe de los citados créditos sin necesidad de ninguna otra notificación, momento desde el cual no se considerará pago legítimo sino el que se hiciere a la entidad financiera.

Séptima.- Cesión de créditos a terceros

El cliente autoriza a la entidad financiera a ceder total o parcial a terceras personas los créditos que ésta ostente contra el cliente como consecuencia del presente contrato. La entidad financiera se obliga a comunicar al cliente dicha cesión a fin de que éste pueda proceder a su legítimo pago al nuevo acreedor.

Octava.- Pago de créditos

El pago por el cliente de los créditos se realizará a su vencimiento por medio de cargo realizado por la entidad financiera en la cuenta corriente número [NÚMERO] de la entidad financiera de la que es titular el cliente.

Novena.- Duración

El presente contrato se concluye por un plazo de [PLAZO] pudiendo prorrogarse, a voluntad de las partes y de común acuerdo por períodos anuales.

Si llegado el vencimiento del plazo inicial o de cualquiera de sus prórrogas, alguna de las partes decidiera dar por finalizado el presente contrato, deberá de comunicar su intención a la otra parte con al menos [PLAZO] de antelación a la fecha del vencimiento a través de un medio que deje constancia de su recepción.

[OPCIONAL — incluir si procede]

(Promesa de Garantía)

Décima.- Garantía

Si durante la vigencia del contrato se produjesen circunstancias que pudieran afectar negativamente a la solvencia del cliente, éste se obliga a constituir, a requerimiento de la entidad financiera, las garantías reales sobre bienes inmuebles, muebles o derechos que sean necesarias para la devolución de las cantidades adeudadas.

Esta obligación deberá ser cumplida por el cliente dentro del plazo de [ELEGIR: días / semanas / meses] siguientes a la fecha en que la entidad financiera le haya requerido para ello.

.- Confidencialidad

Tanto la entidad financiera como el cliente se comprometen a no divulgar la información y documentación confidencial referente a la otra parte de la que hayan tenido conocimiento por razón de la ejecución del presente contrato, salvo las indispensables para su cumplimiento, y a mantenerla en secreto, incluso después de la finalización del mismo.

Ambas partes acuerdan tomar las medidas necesarias respecto a su personal e incluso terceros que puedan tener acceso a dichas información y documentación, a fin de garantizar la confidencialidad objeto de esta cláusula.

.- Protección de datos

La entidad financiera reconoce que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales. A tal efecto, la entidad financiera:

a) únicamente accederá a los datos personales de clientes y demás personas físicas relacionadas con el cliente si tal acceso fuese necesario para cumplir con los servicios objeto del presente contrato.
b) se compromete a:
— utilizar los datos de carácter personal a los que tenga acceso única y exclusivamente para cumplir con sus obligaciones contractuales para con el cliente.
— observar y adoptar cuantas medidas de seguridad sean necesarias para asegurar la confidencialidad, secreto e integridad de los datos de carácter personal a los que tenga acceso, así como a adoptar en el futuro cuantas medidas de seguridad sean exigidas por las leyes y reglamentos destinadas a preservar el secreto, confidencialidad e integridad en el tratamiento automatizado de datos personales.
— a no ceder en ningún caso a terceras personas los datos de carácter personal a los que tenga acceso, ni tan siquiera a efectos de su conservación.

Las obligaciones establecidas para la entidad financiera por la presente cláusula serán también de obligado cumplimiento para sus posibles empleados, colaboradores, tanto externos como internos, y subcontratistas, por lo que la entidad financiera responderá frente al cliente si tales obligaciones son incumplidas por tales empleados, colaboradores y subcontratistas.

El incumplimiento por parte de la entidad financiera de cualesquiera de las obligaciones establecidas en la anterior cláusula de confidencialidad y en ésta de tratamiento de datos de carácter personal, generará una indemnización en favor del cliente de [IMPORTE] euros, sin perjuicio del derecho del cliente a resarcirse de los perjuicios que le sean causados y que superen la cuantía indicada.

La duración de las obligaciones de confidencialidad establecidas en el presente contrato será indefinida, manteniéndose en vigor con posterioridad a la finalización, por cualquier causa, de la relación entre la entidad financiera y el cliente.

.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

.- Impuestos

[ELEGIR UNA OPCIÓN: Sin determinar / A cargo del cliente]

.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en su defecto, por lo dispuesto por la legislación mercantil y civil vigente, tanto española como de la Unión Europea que fuere de aplicación.

.- Fuero competente

[ELEGIR UNA OPCIÓN: Tribunales / Cláusula de arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

Entidad Financiera

________________________________

Cliente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

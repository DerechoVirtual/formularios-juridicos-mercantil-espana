---
name: contrato-forfaiting-creditos-exportacion-mer-0627
description: "Contrato de forfaiting de créditos de exportación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de forfaiting de créditos de exportación

> Formulario **MER-0627** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que el cliente (una empresa exportadora) vende a una empresa de forfaiting ( generalmente una entidad financiera) un documento de pago internacionalmente aceptado, letra o pagaré, que reconoce un derecho de cobro originado en una operación de compra-venta internacional, transfiriendo todos los riesgos y responsabilidades de cobro y recibiendo el pago al contado con las deducciones propias del descuento.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de forfaiting de créditos de exportación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de forfaiting de créditos de exportación” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-forfaiting-creditos-exportacion-mer-0627`.
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
- [ ] IMPORTE (4 veces)
- [ ] Nº (3 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] PLAZO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DIVISA
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] NÚMERO
- [ ] PERIODICIDAD
- [ ] PORCENTAJE

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

Contrato por el que el cliente (una empresa exportadora) vende a una empresa de forfaiting ( generalmente una entidad financiera) un documento de pago internacionalmente aceptado, letra o pagaré, que reconoce un derecho de cobro originado en una operación de compra-venta internacional, transfiriendo todos los riesgos y responsabilidades de cobro y recibiendo el pago al contado con las deducciones propias del descuento.


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

En lo sucesivo, EMPRESA DE FORFAITING.

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

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de FORFAITING y, a tal fin,

MANIFIESTAN

I.- Que LA EMPRESA DE FORFAITING se dedica habitualmente a la prestación de servicios consistente en la realización de operaciones de gestión de cobro de créditos ajenos y/o anticipo de fondos sobre los mismos.

II.- Que EL CLIENTE se dedica a la exportación de en [DESCRIPCIÓN DEL BIEN].

III.- Que estando interesado el CLIENTE en externalizar y encargar a un tercero la gestión del cobro de los efectos que provienen del desarrollo de su actividad de exportación, y LA EMPRESA DE FORFAITING en asumir la gestión de los mismos, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Primera.- Objeto

Constituye el objeto del presente contrato el endoso a la EMPRESA DE FORFAITING de los derechos de crédito que EL CLIENTE ostenta para que sean abonados por aquella con carácter anticipado previo descuento de la comisión que conforme a este contrato resulte procedente.

La EMPRESA DE FORFAITING se obliga a aceptar todas las letras de cambios y pagarés que el cliente le entregue de conformidad con las condiciones que se exponen a continuación.

EL CLIENTE se obliga a documentar todos y cada uno de los créditos cedidos por medio de la correspondiente factura, que deberá ir unida al pagaré, letra de cambio o efecto debidamente endosado y a garantizar, bajo su responsabilidad, la vigencia, legitimidad y validez de todos y cada uno de los efectos cedidos, declarando que sobre los mismos no existe gravamen alguno ni incidencia relacionada con la mercancía exportada.

Segunda.- Endoso y documentos de exportación

EL CLIENTE sólo endosará los documentos cambiarios que no superen la cantidad de [IMPORTE] y se expresen en la siguiente divisa [DIVISA]. Además aportará recibo, carta de porte o embarque o cualquier documento fehaciente que demuestre la remisión efectiva de la exportación junto a los efectos correspondientes para pago de las mismas. Igualmente, deberá aportarse carta de conformidad del importador o justificante de haberse asegurado la mercancía.

Para la realización de los endosos es necesario que:

a) Exista aval o bien garantía suficiente bancaria o de otro tipo a favor del librador del pagaré o del librado de la letra, salvo que la Entidad renuncie expresamente a exigir dichas garantías inicialmente sin que ello implique su renuncia a exigirlas con posterioridad.
b) Los endosos se realicen sin responsabilidad alguna del cedente.

Tercera.- Descuentos

La EMPRESA FORFAITING se compromete a descontar efectos hasta un límite máximo de [IMPORTE] euros nominales, que serán el resultado en cada momento de deducir de la cifra global anticipada y descontada por la EMPRESA FORFAITING el capital recuperado por dicha empresa por la gestión de cobro de los efectos cedidos por el CLIENTE y satisfechos por los correspondientes deudores. A estos efectos se tomará como valor de cambio a [IMPORTE] euros del capital recuperado el de la fecha en que sea efectivamente satisfecho a la EMPRESA FORFAITING.

Cuarta.- Remuneración y Comisiones

La EMPRESA DE FORFAITING percibirá del CLIENTE como remuneración de sus funciones el [Nº] por ciento nominal de los créditos transferidos.

El pago se efectuará el día [FECHA] en la cuenta corriente nº [NÚMERO] que EL CLIENTE tiene suscrita con la entidad [DENOMINACIÓN SOCIAL]

Las liquidaciones entre la EMPRESA FORFAITING y el CLIENTE serán [PERIODICIDAD]. La cifra a ingresar por la EMPRESA FORFAITING será la resultante de deducir a la cifra mensual de créditos cedidos una cantidad igual a la resultante de deducir de la misma el .. por ciento correspondiente a la comisión pactada como remuneración de la EMPRESA FORFAITING.

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho a la parte perjudicada a exigir un interés moratorio del [PORCENTAJE] % respecto de cada uno de los pagos no satisfechos puntualmente.

Quinta.- Duración

La duración del presente contrato será de [PLAZO] desde la fecha de la firma del mismo.

Finalizado este plazo se entenderá tácitamente prorrogado por iguales periodos, salvo que expirado el plazo inicial y con al menos [Nº] días de antelación al vencimiento, cualquiera de las partes comunique a la otra su voluntad contraria a la prórroga por un medio que deje constancia de su recepción.

Sexta.- Acciones derivadas de los efectos cambiarios

EL CLIENTE queda obligado a proporcionar a la EMPRESA FORFAITING toda la documentación referente a la gestión de cobro así como los poderes suficientes para iniciar o seguir cualquier procedimiento judicial o extrajudicial tendente al cobro de las cantidades correspondientes por los impagos que puedan producirse. Igualmente se compromete a ceder cuantas posibles acciones judiciales le asistan frente a las empresas transportistas de las mercancías que se exporten, obligándose a comunicar la presente circunstancia a dichas empresa.

Séptima.- Confidencialidad

Tanto la EMPRESA FORFAITING como el CLIENTE se comprometen a no divulgar la información y documentación confidencial referente a la otra parte de la que hayan tenido conocimiento por razón de la ejecución del presente contrato, salvo las indispensables para su cumplimiento, y a mantenerla en secreto, incluso después de la finalización del mismo.

Ambas partes acuerdan tomar las medidas necesarias respecto a su personal e incluso terceros que puedan tener acceso a dichas información y documentación, a fin de garantizar la confidencialidad objeto de esta cláusula.

Octava.- Protección de datos

La EMPRESA FORFAITING reconoce que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales. A tal efecto, la EMPRESA FORFAITING:

a) Únicamente accederá a los datos personales de clientes y demás personas físicas relacionadas con el CLIENTE si tal acceso fuese necesario para cumplir con los servicios objeto del presente contrato.
b) Se compromete a:
- Utilizar los datos de carácter personal a los que tenga acceso única y exclusivamente para cumplir con sus obligaciones contractuales para con el CLIENTE.
- Observar y adoptar cuantas medidas de seguridad sean necesarias para asegurar la confidencialidad, secreto e integridad de los datos de carácter personal a los que tenga acceso, así como a adoptar en el futuro cuantas medidas de seguridad sean exigidas por las leyes y reglamentos destinadas a preservar el secreto, confidencialidad e integridad en el tratamiento automatizado de datos personales.
- A no ceder en ningún caso a terceras personas los datos de carácter personal a los que tenga acceso, ni tan siquiera a efectos de su conservación.

Las obligaciones establecidas para la EMPRESA FORFAITING por la presente cláusula serán también de obligado cumplimiento para sus posibles empleados, colaboradores, tanto externos como internos, y subcontratistas, por lo que la EMPRESA FORFAITING responderá frente al CLIENTE si tales obligaciones son incumplidas por tales empleados, colaboradores y subcontratistas.

El incumplimiento por parte de la EMPRESA FORFAITING de cualesquiera de las obligaciones establecidas en la anterior cláusula de Confidencialidad y en ésta de Tratamiento de Datos de Carácter Personal, generará una indemnización en favor del CLIENTE de [IMPORTE] euros, sin perjuicio del derecho del CLIENTE a resarcirse de los perjuicios que le sean causados y que superen la cuantía indicada.

La duración de las obligaciones de confidencialidad establecidas en el presente contrato será indefinida, manteniéndose en vigor con posterioridad a la finalización, por cualquier causa, de la relación entre la EMPRESA FORFAITING y el CLIENTE.

Novena.- Terminación y resolución

Son causas de terminación y resolución del presente contrato:

- Su terminación normal, ya sea por:
a) haber llegado el contrato a su vencimiento,
b) haberse cumplido y ejecutado la prestación a la que ambas partes se encuentran obligadas,
c) acuerdo mutuo de las partes.
- Por incumplimiento de cualquiera de las partes de alguna de las cláusulas del presente contrato, sin que dicho incumplimiento fuera subsanado dentro de los [PLAZO] siguientes a la notificación por escrito efectuada por la otra parte solicitando la subsanación del incumplimiento.

Décima.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Decimoprimera.- Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE].

Decimosegunda.- Elevación a escritura pública

El presente contrato se elevará a público a solicitud de cualquiera de las partes, siendo los gastos del notario pagados por la parte que lo solicite.

Decimotercera.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones del Código de Comercio, Leyes especiales, los usos y costumbres mercantiles y, en su defecto, por lo establecido en el Código Civil.

Decimocuarta.- Fuero competente

[ELEGIR UNA OPCIÓN: Si se pacta sometimiento a tribunales / Si se pacta someterse a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

EMPRESA DE FORFAITING

________________________________

EL CLIENTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

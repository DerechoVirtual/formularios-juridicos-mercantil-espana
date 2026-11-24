---
name: contrato-comision-mercantil-sin-garantia-comisionista-mer-0486
description: "Contrato de comisión mercantil con o sin garantía del comisionista. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de comisión mercantil con o sin garantía del comisionista

> Formulario **MER-0486** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que, el comisionista, se obliga a realizar un acto o actividad comercial que le ha sido encargada por otro empresario, el comitente. Cuando el comisionista garantiza el buen resultado económico del negocio celebrado y se obliga a responder frente al comitente del incumplimiento del tercero en iguales plazos y condiciones que éste, se entiende como comisión con garantía.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de comisión mercantil con o sin garantía del comisionista» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de comisión mercantil con o sin garantía del comisionista” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-comision-mercantil-sin-garantia-comisionista-mer-0486`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] Nº (6 veces)
- [ ] DNI/NIE (4 veces)
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE DE LA PARTE (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] PERIODICIDAD (2 veces)
- [ ] PLAZO (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] ÍNDICE DE REVISIÓN (2 veces)
- [ ] DIRECCIÓN
- [ ] LUGAR
- [ ] MARCA
- [ ] OBJETO DEL CONTRATO
- [ ] UNIDAD DE REFERENCIA
- [ ] ZONA GEOGRÁFICA

## Normas que cita el formulario

- art. 272 Código de Comercio

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

Contrato por el que, el comisionista, se obliga a realizar un acto o actividad comercial que le ha sido encargada por otro empresario, el comitente. Cuando el comisionista garantiza el buen resultado económico del negocio celebrado y se obliga a responder frente al comitente del incumplimiento del tercero en iguales plazos y condiciones que éste, se entiende como comisión con garantía.


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

En lo sucesivo, EL COMISIONISTA.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EL COMITENTE.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de COMISIÓN y, a tal fin,

EXPONEN

I.- Que EL COMISIONISTA se dedica a [ACTIVIDAD].

II.- Que EL COMISIONISTA cuenta con experiencia y con organización propia suficiente para el ejercicio de su actividad.

III.- Que ambas partes están interesadas en establecer las relaciones comerciales previstas en el presente contrato y que por ello

ACUERDAN

Llevar a efecto el presente contrato de COMISIÓN, mediante las siguientes

CLAUSULAS

Primera.- Objeto del Contrato

Por el presente contrato el COMITENTE encarga al COMISIONISTA, quien acepta, la [OBJETO DEL CONTRATO] de [DESCRIPCIÓN DEL BIEN] descritos en el Anexo I

[OPCIONAL — incluir si procede]

(Con garantía)

El COMISIONISTA se compromete mensualmente a la [ACTIVIDAD], como mínimo, de las siguientes cantidades de los productos descritos:

En el caso de que no tengan lugar las ventas mínimas garantizadas por el COMISIONISTA, serán de cargo de éste el abono del precio de venta de dichos productos al COMITENTE, de acuerdo con lo establecido en el artículo 272 del Código de Comercio.

Segunda.- Ejecución

El COMISIONISTA actúa por cuenta del COMITENTE en los contratos que formalice con terceros en ejecución del presente convenio y se compromete a llevar a cabo las operaciones que le han sido encomendadas, con la diligencia de un ordenado comerciante, sirviendo al interés del COMITENTE y protegiendo la imagen de

El presente contrato es otorgado atendiendo a las cualidades personales, profesionales y económicas del COMISIONISTA, de modo que los derechos y obligaciones derivados del mismo no podrán cederse ni directa ni indirectamente, sin previa autorización escrita del COMITENTE.

Tercera.- Condiciones de venta

EL COMISIONISTA, en la ejecución de la comisión, deberá sujetarse a las instrucciones que reciba del COMITENTE y, en todo caso, deberá realizar la venta de las mercancías objeto de este contrato bajo las siguientes condiciones:

[OPCIONAL — incluir si procede]

(Si se exime de responsabilidad al comisionista)

El COMISIONISTA estará obligado a consultar al COMITENTE todo lo que no haya sido previsto, quedando exento de responsabilidad si se ajusta a las instrucciones recibidas.

El precio mínimo por el que se autoriza al COMISIONISTA la celebración de contratos es de [IMPORTE], euros [UNIDAD DE REFERENCIA].

El COMISIONISTA se obliga a entregar al COMITENTE las cantidades satisfechas por el comprador con el que contacte el día posterior al de la celebración de dicho contrato, mediante su ingreso en la cuenta corriente número [NÚMERO] que éste tiene contratada con la entidad [DENOMINACIÓN SOCIAL], sucursal [LOCALIDAD] de

[OPCIONAL — incluir si procede]

(En caso de que exista provisión de fondos)

En concepto de provisión de fondos, el COMITENTE entrega al COMISIONISTA [IMPORTE] euros cantidad que el COMISIONISTA declara haber recibido, y que ha de destinarse a cuantos gastos puedan originarse a consecuencia de la gestión.

Cualquier gasto adicional deberá ser comunicado por el COMISIONISTA al COMITENTE, debiendo abonar este último dichas cantidades al COMISIONISTA, hasta un máximo de [IMPORTE] € adicionales. A partir de esa cantidad, el COMITENTE no responderá de los gastos realizados en la gestión de las operaciones encomendadas

Cuarta.- Retribución del Comisionista

El COMITENTE acuerda pagar al COMISIONISTA en compensación por los servicios prestados:

[OPCIONAL — incluir si procede]

(Cuantía fija)

Una remuneración fija de [IMPORTE] euros [ELEGIR: brutos / netos], que deberá ser pagada por EL COMITENTE por meses adelantados, a contar desde la fecha del presente contrato y dentro de los primeros días de cada mes.

Dicha contraprestación será revisada anualmente de acuerdo con [ÍNDICE DE REVISIÓN].

[OPCIONAL — incluir si procede]

(Comisión fija)

Una comisión fija y única del %. Este porcentaje no podrá ser modificado por las partes salvo que se acuerde mutuamente y por escrito.

El importe de la comisión se calculará sobre el valor neto de las ventas, es decir, el precio en factura de los productos vendidos por el COMISIONISTA incluyendo gastos e impuestos

El COMITENTE deberá satisfacer [PERIODICIDAD] la comisión al COMISIONISTA siempre dentro de los [Nº] días siguientes del mes posterior al que finalice el plazo.

[OPCIONAL — incluir si procede]

(Comisión variable por características de producto o número de operaciones)
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Un [PORCENTAJE] % por la venta de [DESCRIPCIÓN DEL BIEN]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Un % a partir de [Nº] operaciones

El COMITENTE deberá satisfacer [PERIODICIDAD] la comisión al COMISIONISTA siempre dentro de los [Nº] días siguientes del mes posterior al que finalice el plazo.

[OPCIONAL — incluir si procede]

(Sistema mixto)

Como contraprestación a la actividad desarrollada como consecuencia del presente contrato, El COMISIONISTA percibirá una remuneración fija de [IMPORTE] euros [ELEGIR: brutos / netos], que deberá ser pagada por EL COMITENTE por meses adelantados, a contar desde la fecha del presente contrato y dentro de los primeros días de cada mes.

Esa cantidad será revisada anualmente de acuerdo con [ÍNDICE DE REVISIÓN].

Además de la retribución fija citada, el COMISIONISTA percibirá como contraprestación al ejercicio de su actividad profesional, una comisión del [PORCENTAJE] de todas las ventas que se realicen en la [ZONA GEOGRÁFICA] sobre la que se extiende el presente contrato, llevándose a cabo la liquidación de las referidas comisiones a [ELEGIR: mes / trimestre / año] vencido y dentro de los quince primeros días del mes siguiente al término de cada [ELEGIR: mes / trimestre / año]. Para ello, el COMISIONISTA recibirá en los primeros [Nº] días del mes siguiente al término del [ELEGIR: mes / trimestre / año], una liquidación de las comisiones devengadas, debiendo remitir en los siguiente [Nº] días factura conforme a la referida liquidación, factura que le será abonada en la cuenta bancaria número [NÚMERO] antes del día [FECHA] del mes siguiente al término de cada [ELEGIR: mes / trimestre / año], y siempre y cuando se haya remitido en la forma que queda expuesta la factura correspondiente.

[OPCIONAL — incluir si procede]

(Información detallada)

A tal efecto, el COMISIONISTA facilitará al COMITENTE, a efectos de control contable, relaciones [ELEGIR: semanales / quincelanes / mensuales / bimestrales / trimestrales / semestrales / anuales] separadas de los movimientos de venta en unidades y valores. Dichas relaciones serán remitidas durante los días de cada [ELEGIR: semana / quincena / mes / trimestre / semestre / año].

[OPCIONAL — incluir si procede]

(Si existe sobre precio)

Además, y para el caso de que el COMISIONISTA obtuviera del eventual comprador un precio superior al señalado en la cláusula .de este contrato, las partes acuerdan una comisión a favor del COMISIONISTA del % de dicho sobreprecio.

Quinta.- Obligaciones de las partes

El COMISIONISTA se compromete a:

1. Llevar a cabo las operaciones que le han sido encomendadas, con la diligencia de un ordenado comerciante, sirviendo al interés del COMITENTE y protegiendo la imagen de [MARCA].

[ELEGIR: Exclusividad]

2. El COMISIONISTA podrá desarrollar su actividad profesional por cuenta de varios COMITENTES en todo el territorio nacional

[OPCIONAL — incluir si procede]

(Si requiere almacenamiento)

3. Guardar y custodiar los bienes objeto de la encomienda desde el día [FECHA]. [FECHA], fecha en la que el COMITENTE le facilitará las llaves del local en el que dichos bienes se hallan almacenados.

4. Transmitir al COMITENTE cualquier queja relacionada con los productos objeto de la actividad de [NOMBRE DE LA PARTE], tan pronto como las reciba, y a cooperar en la resolución de las mismas.

5. Comunicar mediante conducto notarial el éxito de su operación al COMITENTE. Asimismo se obliga a enviarle un Fax semanal con la información referente a los potenciales compradores y estado de la gestión. Igualmente deberá, una vez finalizada la misma, aportar un estado de cuentas detallando los gastos ocasionados, debidamente acreditados.

6. Entregar al COMITENTE las cantidades satisfechas por el comprador con el que contacte el día posterior al de la celebración de dicho contrato, mediante su ingreso en la cuenta corriente número [NÚMERO] que éste tiene contratada con la entidad [DENOMINACIÓN SOCIAL],

[OPCIONAL — incluir si procede]

(Si media provisión de fondos)

7. Reintegrar al COMITENTE de las cantidades percibidas en concepto de provisión de fondos, excepto una cuantía equivalente a un % de dicha cuantía, para satisfacer los gastos que las gestiones le hayan ocasionado cuando no logre el objeto o finalidad de este contrato

El COMITENTE se compromete a:

1. Abstenerse de cerrar operaciones de compraventa respecto a los productos cuya venta se encomienda al COMISIONISTA.
2. Satisfacer al comisionista la comisión y el importe de todos los gastos
3. Responder por todas las reclamaciones que se presenten de terceros concernientes a vicios o defectos de la calidad de los [ELEGIR: productos / servicios / productos y servicios] de las operaciones promovidas, aunque no se hubiesen concluido

Sexta.- Duración

[ELEGIR UNA OPCIÓN: Duración determinada / Duración hasta ejecución plena de las obligaciones / — y además elegir: Renovación automática o caducidad / Extinción al vencimiento]

[OPCIONAL — incluir si procede]

(Si se pacta confidencialidad)

Séptima.- Confidencialidad

El COMISIONISTA asume el interés del COMITENTE en mantener el carácter confidencial y secreto de los procedimientos transmitidos durante la vigencia del presente acuerdo.

[OPCIONAL — incluir si procede]

(Si se pacta contratar un seguro)

.- Seguros

El COMITENTE se compromete a mantener actualizado un seguro de daños sobre los productos almacenados en [DIRECCIÓN] cuya venta se encomienda al COMISIONISTA.

El COMITENTE presentará al COMISIONISTA cuando le sea requerido copia del seguro referido

.- Extinción del contrato

El presente contrato podrá resolverse, además de por las causas legalmente previstas, cuando concurra alguna de las siguientes circunstancias:

- El mutuo acuerdo de las partes expresado por escrito.
- El vencimiento del término de duración pactado.
- El incumplimiento total o parcial de las obligaciones establecidas en el presente contrato.
- La insolvencia o declaración de concurso de cualquiera de las partes contratantes.

[OPCIONAL — incluir si procede]

(Si se pacta devolución)

La extinción o resolución de este contrato supondrá la obligación de devolución por parte del COMISIONISTA de todos los bienes proporcionados por el COMITENTE para el ejercicio de su actividad en el plazo de [PLAZO] desde que sea efectiva la finalización del contrato.

.- Vencimiento anticipado

El COMITENTE y el COMISIONISTA tendrán derecho a finalizar anticipadamente el presente contrato, en caso de reiterado incumplimiento de la otra parte. Con este fin, la parte que se considere afectada por el incumplimiento deberá comunicarlo a la parte infractora, haciendo constar las circunstancias del incumplimiento. La parte infractora, cuando fuere posible, deberá corregir o subsanar dicha infracción en el plazo de [Nº] días desde el envío de la notificación.

En el caso de que la parte infractora no subsanase la infracción en el plazo señalado, o incurriese en nuevos incumplimientos, la parte afectada podrá resolver el contrato con el envío de una nueva notificación fehaciente, dirigida al infractor, en la que conste la falta de subsanación de los incumplimientos, quedando el contrato resuelto, sin perjuicio de la indemnización de daños y perjuicios que en su caso fuera exigible.

[OPCIONAL — incluir si procede]

(Otras consecuencias de la extinción)

Extinguido el contrato de comisión, cualquiera que fuere la causa, el COMISIONISTA dejará de usar la marca o cualquier elemento identificativo del COMITENTE, procediendo a devolver cualquier elemento promocional o publicitario que le haya sido entregado para la explotación del objeto del presente acuerdo.

.- Daños y perjuicios

En el caso de resolución de este contrato de comisión por incumplimiento imputable a alguna de las partes y en orden la liquidación e indemnización de daños y perjuicios, se conviene que:

1. Salvo causa justificada, si fuere por culpa del COMITENTE, el retraso en el pago a favor del COMISIONISTA, devengará un interés de demora del % y si el COMITENTE renunciara al contrato sin justa causa, pagará además de los gastos realizados la suma de [IMPORTE] euros.
2. Salvo causa justificada, si fuere por culpa del COMISIONISTA, el retraso en la devolución de los productos [PLAZO], [NOMBRE DE LA PARTE] pagará la cantidad de [IMPORTE] euros.
3. El tipo de mora, será el mismo que el del comitente.
4. En ambos casos se indemnizarán mutuamente los gastos de celebración del contrato.

.- Gastos e impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE]

.- Legislación aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones del Código de Comercio, leyes especiales y usos mercantiles, y en su defecto por lo previsto en el Código Civil.

.- Jurisdicción competente

[ELEGIR UNA OPCIÓN: Si se pacta someterse a tribunales / Si se pacta someterse a arbitraje]

Y en prueba de conformidad las partes firman el presente contrato, extendido por duplicado ejemplar, y a un solo efecto, en el lugar y fecha indicada en el encabezamiento

_______________________________

COMITENTE

_______________________________

COMISIONISTA

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

Anexo I: lista de productos y precios

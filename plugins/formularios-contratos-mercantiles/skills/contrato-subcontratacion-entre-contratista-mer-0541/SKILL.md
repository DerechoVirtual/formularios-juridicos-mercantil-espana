---
name: contrato-subcontratacion-entre-contratista-mer-0541
description: "Contrato de subcontratación entre contratista y subcontratista. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de subcontratación entre contratista y subcontratista

> Formulario **MER-0541** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de subcontratación entre contratista y subcontratista» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de subcontratación entre contratista y subcontratista” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-subcontratacion-entre-contratista-mer-0541`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] DNI/NIE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] ASEGURADORA (2 veces)
- [ ] FECHA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº DE PÓLIZA (2 veces)
- [ ] CALLE
- [ ] DÍA Y MES
- [ ] LUGAR
- [ ] Nº

## Normas que cita el formulario

- art. 1.591 Código Civil

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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de CONTRATISTA)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CONTRATISTA.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del SUBCONTRATISTA)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, SUBCONTRATISTA.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de SUBCONTRATA y, a tal fin,

EXPONEN

I. Que la sociedad "" ha asumido la ejecución de las obras de un edificio subterráneo sito en [LOCALIDAD], calle [CALLE], según proyecto redactado por el Arquitecto D./Dña. [NOMBRE Y APELLIDOS] quien actuará como Dirección facultativa de las obras o trabajos a que alude este contrato, y a cuyo fin ha solicitado la colaboración de D./Dña. [NOMBRE Y APELLIDOS]

II. Que D./Dña. [NOMBRE Y APELLIDOS] ha presentado presupuesto-oferta con fecha [FECHA], el que se une al presente contrato como anexo número dos, y que se entiende forma parte de su contenido, y habiendo convenido otorgar el presente contrato, lo efectúan conforme a las cláusulas generales que se unen como anexo número uno a este documento y de cuyo contenido se entiende forma parte, y conforme también a las siguientes:

CLÁUSULAS PARTICULARES

Primera.- Objeto del contrato

El contratista encarga al subcontratista, que acepta en el presente acto, la ejecución de los trabajos de desvíos de agua de alcantarillados y jardinería de acuerdo con las especificaciones del proyecto, pliegos de condiciones de las obras que el subcontratista declara conocer, así como de acuerdo con las normas municipales y disposiciones aplicables en la materia.

Segunda.- Aceptación de la propiedad

La validez y efectos de este contrato se supeditan a la aceptación por parte de la propiedad tanto de las obras como de los equipos de trabajo de la subcontratista.

La aceptación se entiende producida si nada en contra se comunica por la contrata a la subcontratista en el plazo de diez días hábiles desde la firma de este documento.

Tercera.- Condiciones de ejecución

El contratista se obliga a suministrar todos los permisos pertinentes y el subcontratista todos los materiales, mano de obra, medios técnicos o auxiliares y equipos que precise.

Cuarta.- Precios unitarios- Presupuesto de la obra

El presupuesto total de la obra es de [IMPORTE] euros y los precios de los trabajos específicos subcontratados son los siguientes: [IMPORTE].

Quinta.- Plazo de ejecución

contados a partir del [DÍA Y MES] del presente año.

Sexta.- Condiciones de pago

Para pagar las cantidades indicadas se establece como plazo el de sesenta días desde la terminación de las obras, en metálico o mediante el libramiento de efectos.

Séptima.- Plazo de garantía

Octava.- Garantías y retenciones

Y en prueba de conformidad, firman el presente documento, por duplicado, en el lugar y fecha al principio indicados, quedando un ejemplar del mismo en poder de cada parte contratante.

CONTRATISTA

SUBCONTRATISTA

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
ANEXO I

CLÁUSULAS GENERALES

Primera.- Objeto del contrato

El objeto de este contrato es la ejecución de los trabajos descritos en las cláusulas particulares, y según el presupuesto-oferta que en las mismas se menciona.

Los trabajos se realizarán de acuerdo tanto con el plan de obra definido por el contratista, como por las normas del pliego general de arquitectura y cualesquiera otra vigentes en los diferentes Ministerios u Organismos competentes que se refieran a edificaciones, instalaciones y construcciones en general.

El subcontratista:

– No podrá subcontratar ninguno de los trabajos sin la previa autorización fehaciente del contratista.
– Cumplirá las órdenes e instrucciones del Jefe de obra, y de la Dirección facultativa y propiedad de las obras.

El contratista se reserva el derecho a ejecutar total o parcialmente las obras objeto de este contrato.

Segunda.- Validez del contrato

La validez y eficacia de este contrato se supedita a la aceptación por la propiedad del subcontratista y sus medios de ejecución, según lo previsto en las cláusulas particulares.

Tercera.- Precios

Los precios aceptados se consideran fijos e inmodificables.

En los precios están incluidos la total ejecución de los trabajos, así como materiales, maquinaria, mano de obra y cuantos medios auxiliares sean necesarios para la ejecución de aquellos.

No obstante, el precio definitivo será el resultado de aplicar a las unidades de obra realizadas, los precios establecidos para cada una en el cuadro de precios del presupuesto y, en su caso, los descuentos correspondientes, así como los que sin figurar incluidos en la oferta-presupuesto, se deriven de lo previsto en el presente contrato. En el caso de instalaciones, serán de cuenta del subcontratista todos los proyectos, permisos, licencias, visados, tasas o cánones necesarios, preceptivos o exigibles para la puesta en marcha de las mismas.

Cuando fuese necesario ejecutar unidades de obra nuevas, será necesaria la autorización y aprobación escrita de la contratista de las mismas y de los precios contradictorios.

Cuarta.- Plazo y forma de ejecución. Penalizaciones por incumplimiento de plazos

El plazo es el fijado en las cláusulas particulares. Si excepcionalmente en las mismas no se indicara, entonces será el deducido del plazo del contrato principal en la parte que corresponda ejecutar al subcontratista.

Si el subcontratista no realizara los trabajos en el plazo o condiciones previstas, el contratista podrá ejecutarlos directamente o por encargo a un tercero, abonando su importe con cargo a la fianza o contra las cantidades que en ese momento adeudare contratista a subcontratista, sin perjuicio de las demás acciones que pudieran corresponder al contratista.

El contratista podrá reformar o reajustar el programa de ejecución si lo estimase oportuno para la buena marcha de las obras. Cualquier reajuste que suponga que los trabajos no puedan comenzar en las fechas previstas o una dilatación en su ejecución, darán derecho al subcontratista a una prórroga de plazo de ejecución igual a la demora.

El retraso en el incumplimiento de los plazos por la subcontratista, dará lugar a la aplicación a la misma de las siguientes penalizaciones:

1ª. Si el incumplimiento fuese de plazos parciales, deberá abonar a la contratista la cantidad de [IMPORTE] euros por día de retraso.
2ª. Si el incumplimiento fuese del plazo final, podrá la contratista pedir la resolución del contrato en los términos que después se dirán en la estipulación decimocuarta.

Quinta.- Obligaciones mensuales

Mensualmente el subcontratista realizará una medición al origen de unidades de obra realmente ejecutadas y terminadas, expresando claramente su localización en la obra, y se someterán a la aprobación de la Dirección facultativa de la obra. No se incluirán acopios.

Mensualmente la subcontratista pasará factura por triplicado de los trabajos realmente realizados y ejecutados desde el origen, deduciendo la retención correspondiente, especificando de forma clara y concisa los datos necesarios para la identificación y localización de las distintas unidades.

El contratista procederá al abono de la factura en metálico o mediante efectos librados con vencimiento a 30 días. Para ello es preciso que la Dirección facultativa, al recibir la factura, no haya rechazado por escrito los trabajos realizados por no ajustarse a la calidad contratada o no responder a las condiciones y especificaciones del proyecto de las obras.

Sexta.- Garantías

La subcontratista garantiza la perfecta ejecución de los trabajos y cumplimiento de los plazos. A tal fin acepta una retención del 10 por 100 a deducir de cada facturación parcial y que le será devuelto un 5 por 100 a la recepción provisional y medición general de las obras, y el otro 5 por 100 a la recepción definitiva, en metálico o mediante el libramiento de efectos con vencimiento a [Nº] días, siempre que los trabajos objeto de este contrato hayan sido terminados a plena satisfacción del contratista y de la Dirección facultativa de la obra.

Séptima.- Deficiencias y desperfectos

Serán de cuenta del subcontratista todos los daños y perjuicios que se causen al contratista o a terceros como consecuencia de la mala ejecución de las obras, o por empleo de materiales calidad inferior a la prevista en el proyecto o por incumplimiento de las órdenes recibidas.

Octava.- Terminación de las obras, recepción y liquidación provisional

El subcontratista comunicará por escrito al contratista la terminación de sus trabajos, dentro de los 10 días siguientes a aquel en que realmente se produzcan, procediendo a su vez, dentro de los 30 días siguientes contados desde la misma fecha a levantar acta de recepción provisional, que firmarán el contratista, subcontratista y Dirección facultativa.

Si la recepción provisional no se produjera en el plazo indicado y ello fuera por causas imputables al contratista, se entenderá igualmente producida la recepción provisional a los quince días siguientes a la certificación de la terminación de las obras.

En el caso de instalaciones, será requisito imprescindible para proceder a la recepción provisional, la entrega por parte del subcontratista de una colección completa de planos con todo detalle sobre la instalación realizada, así como las normas de mantenimiento y conservación.

Novena.- Plazo de garantía

Efectuada la recepción provisional, se iniciará un plazo de garantía hasta la recepción definitiva de las obras por parte de la propiedad, durante el cual el subcontratista se obliga a reparar los defectos de construcción a él imputables, con arreglo a las especificaciones e instrucciones del contratista y Dirección facultativa.

Décima.- Medición general de las obras

Durante los 4 primeros meses del plazo de garantía se procederá de común acuerdo a la medición general de las obras. La medición de las partes ocultas de la obra podrá realizase durante el desarrollo de los trabajos.

Dentro de los 20 días siguientes a la firma del acta de conformidad sobre la medición general efectuada, el subcontratista entregará al contratista una relación valorada de la obra realizada. Desde la citada entrega, el contratista dispondrá igualmente de otro plazo de 20 días, dentro del cual examinará la valoración y comunicará a la subcontratista su conformidad o disconformidad y consiguientes observaciones o reparos.

La parte contratista hará efectiva a la subcontratista el saldo, en su caso, resultante de la relación valorada, una vez efectuada las retenciones correspondientes según lo establecido en la cláusula decimosexta.

Undécima.- Recepción y liquidación definitiva de las obras

El primer día hábil siguiente a la terminación del plazo de garantía, se levantará acta de recepción definitiva, quedando relevada la subcontratista a partir de dicho momento de toda responsabilidad, excepto la establecida en el artículo 1.591 del Código Civil. De no formalizarse tal recepción en la fecha indicada y si ello fuera por causas ajenas al subcontratista, se tendrá por verificada en aquélla la recepción definitiva.

Dentro de los 15 días siguientes a la fecha de recepción definitiva, se valorarán los trabajos efectuados dentro del plazo de garantía, siempre que no fuesen consecuencia de imperfecciones habidas en la ejecución de las obras imputables al subcontratista y se practicará la liquidación definitiva de toda la obra, dentro de los 30 días siguientes a la valoración anterior, abonándose al subcontratista el saldo, en su caso, y con devolución de las retenciones conforme a lo previsto en las cláusulas sexta y séptima.

Duodécima.- Obligaciones sociales y laborales del subcontratista

El subcontratista está obligado al cumplimiento de las disposiciones vigentes en materia laboral, de Seguridad Social, y demás de seguridad e higiene en el trabajo, de acuerdo con la Reglamentación, convenio o norma que le sea de aplicación, y, especialmente, teniendo a todo el personal que participe en las obras objeto de este contrato de alta en Seguridad Social y amparado por póliza de seguro de accidentes de trabajo.

En relación a este apartado se obliga, además:

1º. A justificar documentalmente el cumplimiento de sus obligaciones en materia laboral y de seguridad social. Caso de no hacerlo, el contratista podrá suspender el abono de la facturación de los trabajos hasta tanto no se lleve a efecto tal justificación.
2º. Responder especialmente de las infracciones cometidas por sus operarios en materia de seguridad e higiene.
3º. Mantener en vigor y hasta la terminación de este contrato, un seguro temporal de accidentes y el riesgo de incapacidad permanente y muerte con la entidad aseguradora [ASEGURADORA] con número de póliza [Nº DE PÓLIZA].
4º. Mantener igualmente en vigor y hasta la terminación de este contrato, un seguro que cubra los riesgos de responsabilidad civil y penal, con la entidad aseguradora [ASEGURADORA] con número de póliza [Nº DE PÓLIZA].

Se faculta al contratista a retener de las facturas las cantidades precisas para el abono de las cargas sociales y de los salarios devengados cuando estime que el subcontratista no los ha pagado.

Decimotercera.- Resolución del contrato

Son causas de resolución de este contrato:

1º. El incumplimiento total o parcial de todas o algunas de las cláusulas convenidas en el mismo.
2º. El abandono de la obra sin causa justificada o la negligencia en la ejecución de los trabajos por parte del subcontratista, todo ello a juicio de la Dirección facultativa.
3º. La resolución del contrato principal o de ejecución de obra.
4º. La muerte o, en su caso, la extinción de la personalidad jurídica de cualquiera de las partes contratantes, si los herederos o sucesores no quieren que se continúen las obras.
5º. El concurso de acreedores de cualquiera de las partes contratantes, sin perjuicio de los derechos y acciones que a cada uno pueda corresponder.
6º. El mutuo acuerdo de las partes con los efectos que en el mismo se establezcan.

En caso de resolución del contrato por causa imputable al subcontratista, perderá ésta las retenciones, las que se aplicarán los daños y perjuicios ocasionados al contratista, sin perjuicio de los derechos y acciones que le correspondiesen al contratista.

Decimocuarta.- Paralización de las obras

Tal paralización suspenderá la ejecución de este contrato, salvo que exceda de 4 meses, en cuyo caso se procederá a la liquidación de las obras según lo prevenido.

Decimoquinta.- Finiquito

A la terminación de los trabajos y para el abono resultante de la medición general de las obras, el subcontratista firmará el correspondiente recibo finiquito y acreditará que no queda pendiente de abono alguno de materiales, mano de obra, pago e impuestos, seguros y cargas sociales o reclamaciones laborales respecto del personal empleado en estas obras.

Decimosexta.- Impuestos

Todos los impuestos y tributos, excepto el IVA, que puedan afectar al presente contrato o ejecución de los trabajos a que el mismo se refiere, así como los gastos que en su caso pudieran derivarse de su elevación a escritura pública, serán de cuenta del subcontratista.

Decimoséptima.- Sumisión expresa

Ambas partes, con renuncia expresa al fuero propio, se someten a los Tribunales de [LOCALIDAD].

Y en prueba de conformidad, firman el presente documento anexo, por duplicado, en el lugar y fecha al principio indicados, quedando un ejemplar del mismo en poder de cada parte contratante.

CONTRATISTA

SUBCONTRATISTA

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

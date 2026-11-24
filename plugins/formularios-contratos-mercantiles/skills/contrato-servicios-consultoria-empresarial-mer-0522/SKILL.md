---
name: contrato-servicios-consultoria-empresarial-mer-0522
description: "Contrato de servicios de consultoría empresarial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicios de consultoría empresarial

> Formulario **MER-0522** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato de servicios que utilizan las empresas de consultoría, mediante el que una de las partes («Consultor») establece las condiciones de su propuesta de servicios a la otra parte («Cliente»). Habitualmente estos contratos se realizan para un proyecto concreto en una amplia gama de sectores (estrategia y gestión de empresas, estudios de mercado, recursos humanos, ingeniería, tecnologías de la información, etc.).

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicios de consultoría empresarial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicios de consultoría empresarial” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-servicios-consultoria-empresarial-mer-0522`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] FECHA (3 veces)
- [ ] DESCRIBIR (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] OBJETO DEL CONTRATO (2 veces)
- [ ] PLAZO (2 veces)
- [ ] FINALIDAD DEL ESTUDIO
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] Nº
- [ ] OTROS DATOS
- [ ] ZONA GEOGRÁFICA

## Normas que cita el formulario

- art. 48 Real Decreto Legislativo 1/1996
- art. 1.124 Código Civil

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

Contrato de servicios que utilizan las empresas de consultoría, mediante el que una de las partes («Consultor») establece las condiciones de su propuesta de servicios a la otra parte («Cliente»). Habitualmente estos contratos se realizan para un proyecto concreto en una amplia gama de sectores (estrategia y gestión de empresas, estudios de mercado, recursos humanos, ingeniería, tecnologías de la información, etc.).


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

En lo sucesivo, EMPRESA DE CONSULTORÍA.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EL CLIENTE.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de CONSULTING y, a tal fin,

MANIFIESTAN

I.- Que LA EMPRESA DE CONSULTORÍA se dedica, entre otros, a prestar los servicios de [OBJETO DEL CONTRATO], contando a tal fin con una experiencia demostrada, y con la infraestructura y los medios necesarios para un óptimo desarrollo de dicha actividad, así como con los permisos y licencias legalmente requeridos.

II.- Que EL CLIENTE está interesado en [OBJETO DEL CONTRATO], en lo que está especializada la contraparte

III.- Que ambas partes acuerdan llevar a cabo el presente contrato de consultoría con arreglo a las siguientes:

CLAUSULAS

Primera.- Objeto

La empresa de consultoría se obliga a llevar a efecto y realizar para el cliente un estudio sobre [DESCRIBIR]. consistente en [DESCRIBIR]. y con la finalidad de [FINALIDAD DEL ESTUDIO]., según las siguientes condiciones de: y a presentar, según la periodicidad pactada, sendos informes sobre los trabajos realizados con indicación de [OTROS DATOS].

Segunda.- Condiciones Generales

La prestación de servicios objeto de este contrato se realizará por la empresa consultora con sujeción a la OFERTA presentada por ella misma (que como Anexo se incorpora al presente contrato, formando parte integrante del mismo), y siguiendo, en todo caso, las directrices marcadas por el ciente, que dispone en todo momento de la facultad de determinar el alcance, la forma y el contenido de la prestación del servicio contratado.

Ambas partes reconocen que la oferta elaborada y suscrita por la empresa consultora es parte integrante de este contrato, quedando vinculada a los términos y condiciones descritos en el mismo

El incumplimiento de esta obligación supondrá la imposición sobre la consultora de la penalización consistente en un % sobre la diferencia entre la cantidad máxima establecida en el presente contrato y la cantidad ejecutada hasta dicho momento; la penalización se extraerá de los trabajos devengados y no cobrados. En caso de no existir facturación pendiente de cobro, dicho importe será devuelto al cliente.

Tercera.- Documentación y control

El Cliente se obliga a proporcionar a la empresa de consultoría cuantos datos e informaciones considere precisos para la prestación de los servicios, así como cuantos le sean requeridos por ésta para su realización, facilitándole igualmente el acceso a sus oficinas y centros productivos.

La empresa consultora se obliga, a fin de facilitar el control y seguimiento de la ejecución del contrato, a remitir periódicamente al cliente, la información y documentación acreditativa del estado de las actividades desarrolladas por la consultora en ejecución del mismo.

Además, el cliente se reserva la facultad de exigir a la empresa consultora el envío de cualquier documentación que pudiera necesitar en relación al cumplimiento de la normativa vigente

Cuarta.- Duración

El plazo de ejecución de los trabajos definidos en este contrato se desarrollará entre el [FECHA] y el [FECHA].

No obstante, el contrato podrá ser prorrogado al término del cómputo inicial por nuevos períodos, mediando preaviso de debiendo existir a tal extremo acuerdo expreso de las partes. En caso de existir prórroga expresa por acuerdo de las partes, se podrá incrementar el precio establecido en el presente contrato, en el IPC que proceda publicado por el Instituto Nacional de Estadística.

[OPCIONAL — incluir si procede]

(Resolución unilateral por parte del cliente)

En cualquier caso, el cliente se reserva la facultad de resolver anticipadamente el contrato sin necesidad de alegar justa causa y sin que dicha resolución origine a favor de la empresa consultora derecho a percibir indemnización o compensación de ningún tipo, siempre que dicha circunstancia sea comunicada de forma fehaciente a la consultora, al menos, con una antelación de [PLAZO]. Dicha resolución implicará en cualquier caso, el abono de los trabajos realizados hasta ese momento.

[OPCIONAL — incluir si procede]

(Suspensión unilateral por parte del cliente)

El cliente tendrá la facultad de suspender el presente contrato en cualquier momento, sin más requisitos que la mera comunicación por escrito a la empresa consultora con [PLAZO] de antelación, y sin que el ejercicio de dicha facultad genere a favor del mismo derecho a percibir indemnización o compensación alguna.

En caso de suspensión temporal del Contrato, por causa no imputable a la empresa consultora, las partes de mutuo acuerdo establecerán la prórroga del plazo de ejecución y las condiciones de reanudación de los servicios que forman parte del presente contrato. En todo caso, dicha prórroga no será inferior a la duración de la suspensión temporal. Los gastos y costes derivados de dicha suspensión correrán en todo caso a cargo de

Quinta.- Precio del contrato y abono

El precio de los trabajos objeto del presente contrato asciende a la cantidad de [IMPORTE] euros (€), más la cantidad de (€) en concepto de IVA.

El abono del precio del Contrato quedará condicionado a la correcta ejecución del mismo y al cumplimiento de las obligaciones contractuales de la empresa de consulting,

El precio de los trabajos será pagadero por el cliente en la siguiente forma:

[ELEGIR UNA OPCIÓN: En tres pagos / Mensualmente]

El abono del precio se realizará contra la presentación de las correspondientes facturas emitidas por la empresa de consulting, indicando la referencia del contrato [Nº] y recibidas por el cliente, previo el visto bueno del Responsable del Contrato, reputándose los abonos como recepciones parciales o totales de parte o de la totalidad de las prestaciones del Contrato.

El pago del último de los plazos estipulados, correspondiente a la entrega definitiva del objeto del contrato, se hará depender de la aprobación final del mismo. Dicha aprobación será emitida por el cliente una vez constatada su adecuación a las condiciones y calidades acordadas por las partes, asumiendo el cliente el compromiso de pronunciarse sobre este extremo en el plazo de días contados desde la recepción del trabajo. Aceptados por el cliente los trabajos realizados, la consultora procederá a emitir la última de las facturas comprometidas, rigiendo respecto del pago de la misma lo anteriormente expresado.

Sexta.- Recursos

Para la prestación de los servicios contratados, la empresa consultora utilizará los medios materiales adecuados, así como su propio personal, siempre y cuando:

a) tengan la cualificación y experiencia adecuadas para la realización de los trabajos convenidos.
b) conozcan el contenido de los pactos relativos a propiedad intelectual, confidencialidad, tratamiento de datos de carácter personal y uso de la imagen corporativa y del nombre de FSC Inserta que en virtud del presente contrato se establecen, así como su obligación personal de respetarlos.

La relación entre las partes firmantes de este contrato tiene carácter exclusivamente mercantil, no existiendo vínculo laboral alguno entre FSC Inserta y la consultora o el personal de la misma.

La consultora, en su condición de empleador, se responsabilizará de cuantas obligaciones se deriven de la legislación social y, en especial, de las disposiciones vigentes en materia de Seguridad Social, Seguridad e Higiene en el Trabajo y prevención de riesgos laborales

Séptima.- Propiedad Intelectual

La empresa consultora realiza por medio del presente acto, mediando el pago del precio señalado, una cesión en exclusiva a favor del cliente de los derechos de explotación de los soportes, tanto gráficos como documentales, resultantes del presente Contrato, en el ámbito territorial de [ZONA GEOGRÁFICA], por el periodo de

Dicha cesión de derechos de explotación comprende la capacidad para explotar los soportes, tanto gráficos como documentales, resultantes del presente Contrato bajo cualquier forma y en especial, los derechos de reproducción, distribución, comunicación pública y transformación, así como la capacidad para otorgar autorizaciones no exclusivas a terceros, en virtud de lo establecido por los artículos 17 y siguientes en concordancia con el artículo 48 del Real Decreto Legislativo 1/1996, de 12 de abril, por el que se aprueba el texto refundido de la Ley de Propiedad Intelectual.

La cesión de material informativo, documental, gráfico, histórico o de cualquier tipo por parte del cliente a la empresa de consulting, para el desarrollo de los trabajos objeto del presente Contrato, no otorga ningún tipo de derecho de explotación sobre los mismos, más allá de su utilización en el marco del desarrollo de los trabajos. Su utilización posterior será objeto de violación de los derechos de autor, en los términos y con los efectos previstos en el Real Decreto Legislativo 1/1996, de 12 de abril, por el que se aprueba el texto refundido de la Ley de Propiedad Intelectual y su normativa complementaria y el material cedido deberá ser devuelto al cliente, al momento de entrega de los trabajos.

Octava.- Confidencialidad

La empresa consultora llevará a cabo el servicio encomendado por el cliente con absoluta confidencialidad, con la debida diligencia y secreto profesional.

La empresa consultora responderá frente al cliente del incumplimiento de las obligaciones asumidas en virtud de la presente estipulación, que sea directamente imputable a la consultora o a cualquiera de sus colaboradores, de los cuales deberá responder legalmente incluso aún después de producida la terminación del contrato por cualquier causa.

Novena.- Protección de datos

La consultora reconoce expresamente que los datos de carácter personal, a los que tuviera acceso por razón de la prestación objeto del presente contrato, son de la exclusiva propiedad del cliente, por lo que la empresa consultora no podrá aplicarlos o utilizarlos para un fin distinto al recogido en el presente documento, ni cederlos a otras personas, ni siquiera a efectos de conservación

La consultora se obliga a cumplir diligentemente el deber de guardia y custodia que impone la Ley Orgánica 3/2018, de 5 de diciembre de Protección de Datos y garantía de los derechos digitales. Estos deberes serán exigibles a la consultora durante la vigencia del presente contrato y aún después de producido la terminación por cualquier causa del mismo,

La empresa consultora responderá frente al cliente del incumplimiento de las obligaciones asumidas en virtud de la presente estipulación, que sea directamente imputable a la misma, o a cualquiera de sus colaboradores, de los cuales deberá responder legalmente.

Décima.- Incumplimiento

En el caso de que cualquiera de las partes incumpliera alguna de las obligaciones esenciales del presente contrato, o las cumpliera de forma defectuosa, la parte que a su vez hubiera cumplido con las suyas podrá considerar que ha existido incumplimiento del contrato en los términos establecidos por el artículo 1.124 del Código Civil, quedando facultada para optar entre resolver el contrato o exigir su cumplimiento, reclamando, en ambos casos, la correspondiente indemnización de daños y perjuicios.

Decimoprimera.- Resolución

Será causa de resolución anticipada del contrato el incumplimiento por la consultora de los niveles de calidad y continuidad comprometidos por la misma para la prestación del servicio, en los términos y condiciones que se definen en el presente contrato. Quedando en todo caso excluidos todos aquellos supuestos en los que el incumplimiento de alguna de las partes se deba única y exclusivamente a casos de fuerza mayor.

Constituirán causas de resolución del contrato por causas imputables al contratista las siguientes:

- El abandono por parte de la empresa de consulting del servicio objeto del contrato. Se entenderá producido el abandono la prestación del servicio contratado haya dejado de desarrollarse, con la regularidad adecuada o con los medios humanos o materiales precisos para la normal ejecución del contrato
- Las reiteradas deficiencias en la ejecución del contrato.
- La sustitución de aquel personal cuya presencia en la ejecución del proyecto hubiera constituido una de las causas por las que se hubiera seleccionado al contratista para la ejecución de los trabajos.

[OPCIONAL — incluir si procede]

(Si la empresa consultora es persona física)

El fallecimiento, incapacidad, y cualquier otra causa que le imposibilite a para ejecutar el contrato con la calidad y continuidad a que se compromete en virtud del mismo.

Decimosegunda.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Decimotercera.- Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE]

Decimocuarta.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en su defecto, por lo dispuesto por la legislación mercantil y civil vigente, tanto española como de la Unión Europea que fuere de aplicación.

Decimoquinta.- Fuero competente

[ELEGIR UNA OPCIÓN: Si se pacta someterse a ciertos tribunales / Si se pacta someterse a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

Empresa de Consulting

________________________________

Cliente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

---
name: contrato-estimatorio-mercancias-consignacion-mer-0834
description: "Contrato estimatorio de mercancías en consignación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato estimatorio de mercancías en consignación

> Formulario **MER-0834** del plugin **Traspasos de negocio, confidencialidad y acuerdos de empresa** (`formularios-traspasos-y-acuerdos-de-empresa`) · Mercantil › Otros documentos mercantiles · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que una parte (consignante, proveedor o distribuidor) entrega a otra (consignatario) bienes muebles, con un valor estimado, para que procure su venta dentro de un plazo, obligándose a devolver los no vendidos y a pagar el valor estimado de los vendidos. Es un contrato atípico, asimilable a la comisión de venta, en el que el consignatario asume el riesgo de pérdida o deterioro de los bienes.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato estimatorio de mercancías en consignación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato estimatorio de mercancías en consignación” para mi caso». También puedes invocarla directamente con `/formularios-traspasos-y-acuerdos-de-empresa:contrato-estimatorio-mercancias-consignacion-mer-0834`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-traspasos-y-acuerdos-de-empresa:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Traspasos de negocio, confidencialidad y acuerdos de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº DE ANEXO (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (5 veces)
- [ ] DOMICILIO (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] DNI/PASAPORTE (3 veces)
- [ ] ENTIDAD DE CRÉDITO (3 veces)
- [ ] IBAN (3 veces)
- [ ] NACIONALIDAD (3 veces)
- [ ] DATOS REGISTRALES: FOLIO, TOMO, HOJA (2 veces)
- [ ] DNI/PASAPORTE DEL CÓNYUGE (2 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] BIENES
- [ ] DENOMINACIÓN SOCIAL
- [ ] ELEMENTOS Y HERRAMIENTAS NECESARIOS
- [ ] ESPECIFICAR LOS MEDIOS DE PAGO
- [ ] ESPECIFICAR LOS PRODUCTOS
- [ ] IMPORTE
- [ ] INDEMNIZACIONES
- [ ] LOCALIDAD, CALLE Y NÚMERO
- [ ] MES
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTADO
- [ ] Nº DE ANEXOS
- [ ] Nº DE PROTOCOLO
- [ ] PARTE
- [ ] PARTE QUE LOS ASUME
- [ ] PERIODICIDAD DE LAS PRÓRROGAS
- [ ] PERIODO
- [ ] PLAZO
- [ ] PLAZO DE PREAVISO
- [ ] PRODUCTO RECIBIDO
- [ ] ZONA

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

- Junto a «…dará en poder del Consignatario como contraprestación por su actividad de venta.»: la fijación de precios mínimos de reventa puede ser contraria a la normativa de defensa de la competencia (Ley 15/2007 y Reglamento (UE) 2022/720); comprobar su compatibilidad antes de incluirla.

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

[Nota de uso: en todo el texto se emplea la denominación EL CONSIGNANTE; sustitúyase por la denominación elegida en el apartado de Reunidos (CONSIGNANTE, PROVEEDOR o DISTRIBUIDOR).]

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

DE UNA PARTE,

[Datos del CONSIGNANTE, DISTRIBUIDOR O PROVEEDOR]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y DNI/Pasaporte número [DNI/PASAPORTE].

[OPCIONAL — incluir si procede (estado civil casado/a)]
Casado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con DNI/Pasaporte número [DNI/PASAPORTE DEL CÓNYUGE], en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, [ELEGIR: CONSIGNANTE / PROVEEDOR / DISTRIBUIDOR].

[Si hay más de una persona en esta posición contractual, repetir el párrafo anterior tantas veces como sea necesario.]

Y DE OTRA,

[Datos del CONSIGNATARIO]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y DNI/Pasaporte número [DNI/PASAPORTE].

[OPCIONAL — incluir si procede (estado civil casado/a)]
Casado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con DNI/Pasaporte número [DNI/PASAPORTE DEL CÓNYUGE], en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CONSIGNATARIO.

INTERVIENEN

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Todas las partes en su propio nombre y representación.

— D./Dña. [NOMBRE Y APELLIDOS], en su propio nombre y representación. (Repetir para cada parte que actúe en nombre propio.)

— D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si se trata de persona física) D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTADO], mayor de edad, de nacionalidad [NACIONALIDAD], domiciliado en [DOMICILIO], con DNI/Pasaporte número [DNI/PASAPORTE].

— (Si se trata de persona jurídica) La compañía mercantil denominada [DENOMINACIÓN SOCIAL], domiciliada en [LOCALIDAD, CALLE Y NÚMERO], con NIF núm. [NIF], inscrita en el Registro Mercantil de [PROVINCIA], en [DATOS REGISTRALES: FOLIO, TOMO, HOJA]. Hace uso de las facultades conferidas a su favor en calidad de [ELEGIR: administrador único / administrador solidario / consejero delegado / apoderado] de la sociedad indicada, cargo para el que fue nombrado en escritura otorgada ante el notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO] el [FECHA], con el número [Nº DE PROTOCOLO] de su protocolo, que causó inscripción en el Registro Mercantil de [PROVINCIA] en [DATOS REGISTRALES: FOLIO, TOMO, HOJA].

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato ESTIMATORIO O DE CONSIGNACIÓN y, a tal fin,

EXPONEN

I. Que el [ELEGIR: Consignante / Proveedor / Distribuidor] comercializa [ESPECIFICAR LOS PRODUCTOS] en la zona de [ZONA], teniendo asignada la distribución exclusiva de tales productos, y que se detallan de forma pormenorizada en el Anexo núm. [Nº DE ANEXO] del presente contrato.

II. Que el Consignatario tiene como actividad [ACTIVIDAD], con establecimiento abierto al público autorizado con las oportunas licencias y requerimientos administrativos y con todos los medios materiales y humanos necesarios para tal fin.

III. Que ambas partes están de acuerdo en regular sus relaciones mediante el presente contrato de consignación o estimatorio conforme a las siguientes

CLÁUSULAS

PRIMERA.– Objeto

El [ELEGIR: Consignante / Proveedor / Distribuidor] entrega al consignatario, a título de mero tenedor, a efecto de que procure su venta, [BIENES], cuyo estado, descripción y precio de venta al público pactado figuran en el listado incluido en el anexo [Nº DE ANEXO] del presente contrato.

[OPCIONAL — incluir si procede (modificación del listado de bienes y precios)]
Cualquier modificación de dicho listado deberá ser pactada por las partes formando parte del contrato. La modificación podrá afectar a los precios y a la cantidad de productos en stock.

SEGUNDA.– Entrega

Los Productos objeto del presente contrato serán entregados por el [ELEGIR: consignante / proveedor / distribuidor] al consignatario en su domicilio, considerando a tales efectos el indicado en el encabezamiento del presente documento.

La entrega de los productos detallados y valorados en el Anexo núm. [Nº DE ANEXO] no originará la transmisión de su propiedad a favor del Consignatario, atribuyéndose a éste su posesión y la disponibilidad exclusiva de los mismos para su venta a terceros.

El [ELEGIR: Consignante / Proveedor / Distribuidor] entregará los Productos según el calendario, horarios y cantidades previstas en el Anexo [Nº DE ANEXO] de este contrato.

Los bienes descritos en los Anexos [Nº DE ANEXOS] se estima que tienen el valor señalado en dichos Anexos para cada uno de ellos.

[OPCIONAL — incluir si procede (obligaciones de exposición)]
El Consignatario se obliga a mantener en todo momento la exposición en sus escaparates de [PRODUCTO RECIBIDO].

En el interior de su establecimiento el consignatario se obliga a mantener las mercancías que le son suministradas en lugar accesible al público y en condiciones que las hagan atractivas para su adquisición. Para ello el [ELEGIR: Consignante / Proveedor / Distribuidor] dispondrá de los correspondientes [ELEMENTOS Y HERRAMIENTAS NECESARIOS].

El [ELEGIR: Consignante / Proveedor / Distribuidor] se reserva la facultad de realizar a través de su personal colaborador las correspondientes inspecciones.

[OPCIONAL — incluir si procede (reintegros)]
El Consignatario, a la terminación del plazo estipulado para la venta de los Productos, deberá reintegrar al [ELEGIR: Consignante / Proveedor / Distribuidor] los no vendidos en perfectas condiciones de conservación, si bien en ese momento podrá optar por su adquisición, quedando el Consignatario, en consecuencia, obligado a reembolsar al [ELEGIR: Consignante / Proveedor / Distribuidor] el precio de los mismos en el plazo de los [Nº] días hábiles siguientes a aquél en que hubiera concluido el plazo para su devolución. En el supuesto de retraso en el pago de dicho precio será de aplicación el interés de demora.

TERCERA.– Duración

El presente contrato tendrá una vigencia de [PLAZO] desde el [FECHA] y se entenderá prorrogado tácitamente por periodos [PERIODICIDAD DE LAS PRÓRROGAS], salvo notificación en contrario por alguna de las partes con una antelación de [PLAZO DE PREAVISO].

En el caso de que se acuerde la prórroga del contrato se realizará una nueva relación de los Productos que, siendo propiedad del [ELEGIR: Consignante / Proveedor / Distribuidor] en ese momento, estén en poder del Consignatario, pasando esta nueva relación a ser el Anexo al contrato, previa invalidación de la que de forma original se hizo.

CUARTA.– Contraprestación

El [ELEGIR: Consignante / Proveedor / Distribuidor] procederá al pago de una cuota mensual de [IMPORTE], por meses adelantados, mediante transferencia al número de cuenta [IBAN] del Banco [ENTIDAD DE CRÉDITO]. Dicha transferencia deberá ser efectiva antes del día [DÍA] de cada mes. El consignatario por su parte abonará mensualmente al [ELEGIR: Consignante / Proveedor / Distribuidor] la cantidad recaudada por la venta de sus bienes mediante transferencia al número de cuenta de su titularidad [IBAN] del Banco [ENTIDAD DE CRÉDITO].

QUINTA.– Precio de venta al público

El Consignatario determinará libremente el precio de venta de los Productos a terceros, sin perjuicio de su obligación de reembolsar al [ELEGIR: Consignante / Proveedor / Distribuidor], en cualquier caso, los precios pactados en el Anexo núm. [Nº DE ANEXO] respecto de los Productos efectivamente vendidos.

[OPCIONAL — incluir si procede (precios mínimos)]
Las partes acuerdan como precios mínimos de venta de los Productos a terceros los incluidos en el Anexo [Nº DE ANEXO] del presente contrato, por debajo de los cuales el Consignatario no podrá transmitirlos a terceros.

La diferencia entre el precio pactado en el Anexo [Nº DE ANEXO] y el efectivamente satisfecho por los terceros adquirentes de los Productos quedará en poder del Consignatario como contraprestación por su actividad de venta.

SEXTA.– Transmisión de riesgos

El Consignatario asumirá el buen fin de todas las operaciones que realice, exonerando en este acto expresamente de toda responsabilidad al [ELEGIR: Consignante / Proveedor / Distribuidor] frente a los terceros adquirentes de los Productos objeto del presente contrato, permaneciendo el primero como único responsable por dichas ventas y frente a cualquier eventual reclamación que pudieran interponer tales terceros, si bien todo ello a salvo la responsabilidad que pueda dimanar de los propios Productos.

Igualmente, el Consignatario asume los riesgos derivados de la pérdida de los Productos que se le entregan, incluyendo su robo, pérdida o deterioro por cualquier motivo, incluso los que le sean totalmente ajenos, con la única excepción de los daños provocados por el dolo o negligencia del [ELEGIR: Consignante / Proveedor / Distribuidor].

SÉPTIMA.– Notificación de daños e información

El consignatario deberá notificar al [ELEGIR: Consignante / Proveedor / Distribuidor] cualquier daño, avería o sustracción, etc., que sufriesen los productos consignados dentro del plazo de [Nº] horas de producido el hecho o desde su recepción, procediendo a su baja del listado de productos y precios anexo al presente contrato.

A la finalización de cada [PERIODO] el Consignatario deberá presentar una relación de los Productos vendidos, a la cual el [ELEGIR: Consignante / Proveedor / Distribuidor] dará su conformidad, previas las comprobaciones que estime oportunas, debiendo el Consignatario realizar [ELEGIR: de modo inmediato / en el plazo de [Nº] días hábiles siguientes] el pago correspondiente a los Productos vendidos en [ESPECIFICAR LOS MEDIOS DE PAGO].

OCTAVA.– Garantías y seguros

[OPCIONAL — incluir si procede (por parte del Consignante, Proveedor o Distribuidor)]
Además de la cuota mensual, el [ELEGIR: Consignante / Proveedor / Distribuidor] deberá abonar al consignatario una cantidad equivalente a una mensualidad como depósito en calidad de garantía ante los posibles perjuicios que el consignatario pudiese sufrir por el incumplimiento por parte del [ELEGIR: Consignante / Proveedor / Distribuidor] de las condiciones del presente contrato.

El [ELEGIR: Consignante / Proveedor / Distribuidor] procederá al abono del depósito mediante transferencia bancaria en el momento de la firma del presente contrato al número de cuenta de su titularidad [IBAN] del Banco [ENTIDAD DE CRÉDITO], y éste servirá como eficaz carta de pago.

El depósito se abonará únicamente una vez, aunque el contrato se prorrogue trimestralmente, siendo devuelto íntegramente al [ELEGIR: Consignante / Proveedor / Distribuidor] a la finalización definitiva del contrato y sus prórrogas, si las hubiere. El depósito nunca podrá ser utilizado como pago de una mensualidad.

[OPCIONAL — incluir si procede (por parte del Consignatario)]
El Consignatario se obliga a suscribir un seguro que cubra los eventuales daños por pérdida o deterioro de los Productos que le son entregados en virtud del presente contrato. El Consignatario quedará obligado, durante toda la vigencia del contrato, a hallarse al corriente de los pagos de la prima de tal seguro, pudiendo en cualquier momento el [ELEGIR: Consignante / Proveedor / Distribuidor] requerirle para que proceda a la acreditación de la vigencia del seguro y del pago correspondiente de las primas del mismo.

NOVENA.– Obligaciones del [ELEGIR: Consignante / Proveedor / Distribuidor]

El [ELEGIR: Consignante / Proveedor / Distribuidor] queda obligado en virtud del presente contrato a:

• Responder del saneamiento por evicción y vicios ocultos de los Productos entregados al Consignatario.

• Responder, por sí o por medio del fabricante de los Productos, frente a los compradores, de las garantías legales y comerciales de los Productos.

• No requerir al Consignatario la devolución de los Productos entregados hasta la expiración de los plazos de devolución pactados o hasta la expiración final de la duración del presente contrato o de las prórrogas acordadas por las partes.

DÉCIMA.– Cesión del contrato

Las partes no podrán ceder o transmitir total o parcialmente por ningún medio su posición en el contrato a ningún tercero sin el previo acuerdo de la otra parte.

DECIMOPRIMERA.– Confidencialidad

Ambas Partes se obligan a no revelar ni utilizar, directa o indirectamente, la información y conocimientos adquiridos derivados de la relación contractual acordada. Las Partes se comprometen a tomar las medidas necesarias, tanto respecto a sus empleados como a terceros que pudieran tener alguna relación con el presente Contrato, para asegurar el cumplimiento de lo acordado en esta cláusula.

[OPCIONAL — incluir si procede (destrucción de información)]
Una vez extinguido el presente Contrato, el consignatario destruirá toda información que sobre la presente relación haya almacenado en cualquier soporte o haya reproducido por cualquier procedimiento.

DECIMOSEGUNDA.– Protección de datos

Las partes reconocen que la legislación sobre protección de datos personales (Reglamento (UE) 2016/679 (RGPD) y Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente base jurídica que las legitime.

DECIMOTERCERA.– Resolución

El contrato terminará por cualquiera de las siguientes causas:

• Expiración del término pactado.

• Mutuo acuerdo de las partes.

• Incumplimiento por cualquiera de las partes de una obligación sustancial del contrato.

• Cese de la actividad de cualquiera de las partes por un plazo superior a [Nº] meses.

• Muerte, declaración de fallecimiento, jubilación o inhabilitación del Consignatario cuando fuera persona física.

[OPCIONAL — incluir si procede (notificación)]
En cualquier caso, y como requisito previo a la resolución del Contrato por cualquiera de las Partes, se deberá notificar a la Parte incumplidora el incumplimiento y conceder un plazo de [Nº] días desde la notificación para que subsane dicho incumplimiento. Transcurrido dicho plazo se podrá resolver el Contrato.

La finalización del presente contrato no liberará a las partes de satisfacer los pagos pendientes a la otra parte surgidos durante la vigencia del contrato.

[OPCIONAL — incluir si procede (indemnizaciones)]
La resolución del Contrato por cualquiera de las partes dará derecho a las siguientes indemnizaciones: [INDEMNIZACIONES].

DECIMOCUARTA.– Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[PARTE]: [DOMICILIO]. (Repetir para cada parte.)

DECIMOQUINTA.– Impuestos y gastos

Todos los impuestos y gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [PARTE QUE LOS ASUME].

DECIMOSEXTA.– Naturaleza del contrato

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y, en lo en ellas no previsto, por las disposiciones del Código de Comercio, leyes especiales y usos mercantiles, y en su defecto por lo previsto en el Código Civil.

DECIMOSÉPTIMA.– Fuero competente

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si se pacta acudir a tribunales) Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Tribunales de [LOCALIDAD].

— (Si se pacta acudir a arbitraje) Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD].

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

[ELEGIR: CONSIGNANTE / PROVEEDOR / DISTRIBUIDOR] | CONSIGNATARIO

Firmado: D./Dña. [NOMBRE Y APELLIDOS] | Firmado: D./Dña. [NOMBRE Y APELLIDOS]

ANEXOS

[ANEXO: LISTADO DE BIENES, ESTADO, DESCRIPCIÓN, VALOR ESTIMADO Y PRECIO DE VENTA AL PÚBLICO; CALENDARIO, HORARIOS Y CANTIDADES DE ENTREGA]

NOTAS DE USO

El contrato estimatorio o de consignación es un contrato atípico en virtud del cual una de las partes (el «tradens») entrega a otra (el «accipiens» o consignatario) determinadas cosas muebles, sin transmitirle su propiedad y sin recibir a cambio su importe. Por su parte, el «accipiens» se compromete a procurar la venta de tales cosas dentro de un plazo. Transcurrido éste, el «accipiens» está obligado a devolver al «tradens» las cosas no vendidas y a pagarle el precio estimado en su momento de las vendidas. El «accipiens» asume los riesgos de la destrucción de los bienes, incluso cuando ésta acaezca por caso fortuito. Falta unanimidad en la doctrina en torno a la naturaleza jurídica de este contrato, que se tiende a asimilar a la comisión de venta.

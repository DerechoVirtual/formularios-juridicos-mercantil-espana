---
name: contrato-compraventa-empresa-unidad-productiva-mer-0524
description: "Contrato de compraventa de una empresa o unidad productiva. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de una empresa o unidad productiva

> Formulario **MER-0524** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que el vendedor hace entrega a otra persona física o jurídica (llamada comprador) de una unidad de explotación comercial o industrial en su totalidad (la empresa) o de un conjunto de elementos patrimoniales susceptibles de constituir una unidad económica autónoma, rama de actividad o unidad productiva independiente (capaz de funcionar por sus propios medios) a cambio de un precio.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de una empresa o unidad productiva» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de una empresa o unidad productiva” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-compraventa-empresa-unidad-productiva-mer-0524`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (12 veces)
- [ ] Nº (10 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] MES (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº DE ANEXO (2 veces)
- [ ] PLAZO (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] FECHA
- [ ] FECHAS
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] PORCENTAJE
- [ ] ZONA GEOGRÁFICA
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 11 Ley Orgánica 3/2018
- art. 175 Ley 58/2003

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

Contrato por el que el vendedor hace entrega a otra persona física o jurídica (llamada comprador) de una unidad de explotación comercial o industrial en su totalidad (la empresa) o de un conjunto de elementos patrimoniales susceptibles de constituir una unidad económica autónoma, rama de actividad o unidad productiva independiente (capaz de funcionar por sus propios medios) a cambio de un precio.


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

En lo sucesivo, VENDEDOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, COMPRADOR.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de compraventa [ELEGIR: de empresa / rama de actividad] y, a tal fin,

MANIFIESTAN

I. Que el Vendedor ha venido explotando hasta la fecha la empresa [DENOMINACIÓN SOCIAL] que tiene como objeto social el desarrollo de la siguiente actividad el desarrollo de las siguientes actividades [ACTIVIDAD] con domicilio social en [LOCALIDAD] CIF/NIF núm. [Nº], e inscrita en el Registro Mercantil de

II. Que en la actualidad dicha empresa en funcionamiento tiene un patrimonio social constituido por los bienes y derechos que se relacionan en el inventario suscrito por ambas partes que se adjunta como anexo [Nº DE ANEXO] Todo ello conforme resulta del balance de la sociedad elaborado, a por el Vendedor.

[OPCIONAL — incluir si procede]

(Si en la venta se incluye el local o inmueble)

III. Que uno de los elementos esenciales de la citada empresa es el inmueble, propiedad del vendedor, ubicado en [DIRECCIÓN], que consta de [Nº] metros cuadrados de superficie y que comprende:

IV. Que dicho local se encuentra inscrito en el Registro de la Propiedad de: [LOCALIDAD], con los siguientes datos:

V. Que el vendedor declara bajo su propia responsabilidad que dicho local se encuentra libre de toda carga, gravamen y limitación, y que no existe sobre el mismo contienda judicial ni de cualquier otra índole. Asimismo, en cuanto a la situación arrendaticia, el local se encuentra libre de arrendatarios, ocupantes y precaristas.

. Que el vendedor está interesado en transmitir la titularidad en pleno dominio de la [ELEGIR: empresa / unidad económica independiente] para su explotación, y el comprador está interesado en adquirirla y por el precio y demás condiciones estipuladas en este documento.

. Y que, habiendo llegado las Partes, libre y espontáneamente, a un acuerdo de voluntades, formalizan el presente contrato, conforme a las siguientes:

ESTIPULACIONES

Primera.- Objeto

[ELEGIR UNA OPCIÓN: Empresa / Unidad económica autónoma]

[OPCIONAL — incluir si procede]

(Inmueble)

Las Partes manifiestan que el inmueble descrito en las Manifestaciones [Nº] forma parte de la venta y será, por tanto, transmitido al COMPRADOR mediante este documento.

La presente compraventa lleva implícita además la transmisión de todos los derechos sobre el nombre comercial, así como la titularidad sobre las licencias y autorizaciones necesarias para proseguir con la explotación de la [ELEGIR: empresa / unidad económica autónoma].

La compradora afirma conocer el estado en el que se encuentra los bienes enseres y accesorios descritos en el inventario, así como todas las especificaciones técnicas propias de las mismas y relativas a su correcto funcionamiento y mantenimiento técnico. Reconoce la compradora que los bienes y accesorios inherentes a la empresa adquirida se encuentran en perfectas condiciones de conservación y funcionamiento.

Segundo.- Precio y forma de pago

El precio total de esta venta asciende a [IMPORTE] correspondiendo:

[IMPORTE] euros al pago de instalaciones y mobiliario

[IMPORTE] euros al pago de existencias.

[IMPORTE] euros al pago de licencias, marcas, patentes y nombres comerciales que se transmiten.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

euros

[OPCIONAL — incluir si procede]

(Cuando el pago de la totalidad del precio es anterior)

El vendedor manifiesta haber recibido la totalidad del precio indicado con anterioridad a este acto del comprador, sirviendo el presente documento como carta de pago.

[OPCIONAL — incluir si procede]

(Cuando el pago de la totalidad del precio es simultáneo)
[ELEGIR UNA OPCIÓN: En efectivo / Con cheque / Por transferencia]

[OPCIONAL — incluir si procede]

(Cuando el pago de la totalidad del precio es anterior y simultáneo)

Esta cantidad será satisfecha de la siguiente forma:

a) la cantidad de [IMPORTE], reconoce el vendedor haberla recibido del comprador con anterioridad a este acto.
b) la cantidad de [IMPORTE], es pagada en este acto por el comprador [ELEGIR: en efectivo / mediante cheque bancario nominativo / por transferencia] por valor de [IMPORTE] sirviendo el presente documento como carta de pago.

[OPCIONAL — incluir si procede]

(Cuando media aplazamiento del pago del precio)

Esta cantidad será pagada de la siguiente forma:

a) [IMPORTE] euros se entregan al vendedor en este acto por el comprador mediante [ÓRGANO] sirviendo el presente documento como carta de pago.
b) [IMPORTE] será satisfecha por el comprador en un total de [Nº] pagos, el primero de los cuales tendrá lugar el [DÍA] de [MES] de [AÑO]

Como garantía del abono del precio aplazado se libran - letras de cambio-números [Nº] por importe [IMPORTE] cada una de ellas y con vencimiento los días [FECHAS] de [MES] cada mes. Dichas letras de cambio son aceptadas en este acto por el comprador.

[ELEGIR UNA OPCIÓN: Con condición suspensiva / Con condición resolutoria]

Tercera.- Transmisión de la titularidad

De acuerdo a lo señalado en la manifestación [Nº] de este Contrato, el vendedor transmite al comprador la [ELEGIR: empresa / unidad económica autónoma], con todos los elementos esenciales integrantes de la misma, que figuran en el inventario Anexo al mismo.

La transmisión de la titularidad de la [ELEGIR: empresa / unidad económica autónoma] se produce en la fecha de firma del presente Contrato señalada en el encabezamiento y conlleva, igualmente, la transmisión de todos sus elementos materiales y/o inmateriales, créditos, derechos, obligaciones y contratos esenciales para su actividad económica.

De conformidad con lo establecido en la legislación aplicable y en el presente Contrato, la entrega o traditio de cada elemento se realizará de la siguiente forma:

Bienes muebles

Las Partes acuerdan que mediante este Contrato se transmiten [DESCRIPCIÓN DEL BIEN] y/u otros activos que figuran en el inventario Anexo.

El traspaso de la propiedad de estos bienes se produce en este acto, con su entrega material o puesta a disposición del comprador.

El vendedor declara bajo su responsabilidad que todos estos bienes se encuentran libres de toda carga, gravamen y limitación, y que no existe sobre los mismos contienda judicial de cualquier otra índole.

[OPCIONAL — incluir si procede]

(Evicción)

El vendedor será responsable del saneamiento por evicción y vicios ocultos, siendo el límite temporal de la responsabilidad, por este y otros conceptos derivados del presente Contrato, el establecido por la legislación vigente en cada caso aplicable.

Contratos laborales

De conformidad con lo establecido en el artículo 44 del Estatuto de los Trabajadores, desde la fecha de firma del presente Contrato señalada en el encabezamiento, todos los empleados que presten sus servicios en la Empresa, y que figuran en la relación adjunta como Anexo [Nº DE ANEXO] a este Contrato, con indicación de su categoría, puesto de trabajo, antigüedad, salario anual y beneficios sociales, pasarán a depender del comprador que sucederá al vendedor en todas sus obligaciones y derechos laborales y de Seguridad Social.

[ELEGIR UNA OPCIÓN: Sin pagos pendiente / Con pagos pendientes]

[OPCIONAL — incluir si procede]

(Si no está dado de alta el comprador ni de baja el vendedor)

El comprador se compromete a inscribirse como empresario en los organismos y dependencias laborales, así como en la Seguridad Social en un plazo no superior a [Nº] días y a dar de baja simultáneamente la inscripción del vendedor como empresario respecto a los empleados que figuran en la relación adjunta como Anexo al presente Contrato.

Propiedad intelectual e industrial

[ELEGIR UNA OPCIÓN: Si se transmiten / Si no se transmiten]

[OPCIONAL — incluir si procede]

Bienes inmuebles

Las Partes acuerdan que mediante este Contrato se transmite al comprador el local de negocio de la Empresa descrito en las Manifestaciones [Nº], propiedad del vendedor. El traspaso de la propiedad sobre el mismo se producirá en el momento del otorgamiento de la escritura pública de compraventa.

El Impuesto municipal sobre el Incremento del Valor de los Terrenos devengado, en su caso, como consecuencia de esta transmisión será pagado por el vendedor.

Datos de carácter personal.

Mediante el presente Contrato, se transmiten al comprador los ficheros de datos personales de clientes y proveedores de los que es responsable el vendedor, con la finalidad de desarrollar la actividad económica y las gestiones administrativas necesarias para la [ELEGIR: empresa / unidad económica autónoma], considerándose lícitos los tratamientos de datos necesarios para el buen fin del presente contrato, incluida su comunicación con carácter previo, en la medida en que garantizan la continuidad en la prestación de los servicios objeto del mismo.

De conformidad con lo establecido en el artículo 11 y siguientes de la Ley Orgánica 3/2018, de Protección de Datos Personales y garantía de los derechos digitales, el comprador deberá facilitar a los afectados, de forma expresa, precisa e inequívoca, entre otras, informaciones acerca de: la fecha de la transmisión, su identidad y datos de contacto y el modo en el que podrán ejercer sus derechos de acceso, rectificación, supresión, limitación, portabilidad y oposición. Esta comunicación debe efectuarse a más tardar dentro de a partir de la fecha de firma de este Contrato señalada en el encabezamiento.

Contratos en curso.

El comprador se subrogará en los contratos vigentes que hayan sido celebrados por el vendedor y que sean necesarios o indispensables para la continuidad de la actividad desarrollada por la [ELEGIR: empresa / unidad económica autónoma], a partir de la fecha de firma del presente Contrato señalada en el encabezamiento previa comunicación y autorización de los terceros que hayan celebrado dichos contratos con el vendedor.

El comprador se compromete a respetar los derechos y obligaciones regulados en los contratos de referencia y asume esta subrogación a su cuenta y riesgo, no teniendo derecho a ninguna indemnización en caso de revocación u oposición a la subrogación por parte de los terceros contratantes no conformes.

El vendedor declara que se encuentra al corriente del pago y/o cumplimiento de sus obligaciones derivadas de los contratos en curso transmitidos al comprador.

El listado de los contratos a los cuales resulta de aplicación la presente estipulación figura en el inventario Anexo a este Contrato.

Deudas.

El vendedor declara que ha satisfecho el pago de todas las deudas de la [ELEGIR: empresa / unidad económica autónoma], incluidas las derivadas de sus obligaciones fiscales y laborales.

[OPCIONAL — incluir si procede]

(Si la inexistencia de deudas es elemento esencial)

El comprador declara que la inexistencia de deudas constituye un elemento esencial en virtud del cual celebra el presente Contrato.

Página web y redes

Las Partes acuerdan que mediante el presente Contrato se transmite al comprador la titularidad sobre las siguientes direcciones electrónicas:

La transmisión de la titularidad sobre las mismas se instrumentará respetando la normativa aplicable al tipo de sitio y, en su caso, al tipo de dominio de que se trate

Cuarta.- Obligaciones Fiscales

A partir de la fecha de firma de este Contrato señalada en el encabezamiento, el comprador deberá asumir todas las obligaciones y deudas fiscales derivadas del desarrollo de su actividad económica.

Las partes manifiestan que tras solicitar a la Administración Tributaria la certificación de deudas contemplada en el artículo 175 de la Ley 58/2003, de 17 de diciembre, General Tributaria, la responsabilidad del comprador quedará limitada a las deudas, sanciones y responsabilidades contenidas en la misma.

Quinta.- Procedimientos judiciales

El vendedor declara que, a la fecha de firma de este Contrato, ha cumplido todas sus obligaciones contractuales con terceros, así como aquellas impuestas por la Ley.

Asimismo, manifiesta que no se halla inmerso en litigio alguno ni tiene pendiente ninguna reclamación civil, mercantil, fiscal, administrativa, laboral o de otro tipo en razón de la actividad económica desarrollada por la [ELEGIR: empresa / unidad económica autónoma].

[OPCIONAL — incluir si procede]

(Colaboración posterior)

El vendedor se obliga a colaborar con el comprador en el caso de que, con posterioridad a la firma de este Contrato, aparezcan reclamaciones de terceros en razón de la actividad económica desarrollada por la [ELEGIR: empresa / unidad económica autónoma] con anterioridad a la presente compraventa.

Sexta.- Manifestaciones y garantías

El Vendedor manifiesta:

a) Que la [ELEGIR: empresa / unidad económica autónoma] que es objeto de compraventa goza de todos los permisos y licencias administrativas necesarias para su explotación y funcionamiento, no teniendo pendiente sanción administrativa, o civil de ningún tipo.
b) Que no existe ninguna reclamación judicial o extrajudicial de ningún orden sobre los bienes y derechos que integran el inventario de la [ELEGIR: empresa / unidad económica autónoma] en el momento en el que se efectúa la presente transmisión.
c) Que la [ELEGIR: empresa / unidad económica autónoma] cumple con todas las normas que les son de aplicación, y especialmente con la legislación y demás normativa de orden medioambiental.
d) Que la [ELEGIR: empresa / unidad económica autónoma] se encuentra al corriente de pago de sus obligaciones fiscales y laborales.

El Comprador manifiesta:

a) Que se subroga en la posición del Vendedor en las relaciones laborales que aquella tiene a la fecha de la presente compraventa. De esta manera los trabajadores conservarán su categoría, antigüedad y salario.
b) Que se subroga en la posición del Vendedor en todos aquellos contratos que hubieran sido suscritos en directa relación con la explotación de la [ELEGIR: empresa / unidad económica autónoma]
empresa
unidad económica autónoma
c) Que asume el pasivo de la [ELEGIR: empresa / unidad económica autónoma] comprada que resulta del balance que se incorpora junto a la presente escritura.

[OPCIONAL — incluir si procede]

(Continuidad en la gestión del vendedor)

Asimismo, las Partes acuerdan que en caso que el vendedor siga encargándose de la gestión interna de la [ELEGIR: empresa / unidad económica autónoma] con posterioridad a la fecha de firma de este Contrato, los criterios a aplicar deberán ser coincidentes con los que tradicionalmente venía aplicando. Las medidas extraordinarias necesitarán la autorización expresa del comprador.

[OPCIONAL — incluir si procede]

Séptima.- Depósito

En este acto, el vendedor hace entrega al comprador del documento bancario por el que se acredita el ingreso de [IMPORTE] euros en concepto de depósito de garantía con la finalidad de asegurar el cumplimiento de sus obligaciones legales y contractuales, en una cuenta bancaria de titularidad conjunta de ambas Partes.

El comprador declara en este acto recibir dicha cantidad en la fecha mencionada en el encabezamiento, constituyendo el presente documento la más formal y solemne carta de pago que en derecho corresponda.

Este depósito de garantía será devuelto al vendedor transcurridos [Nº] años desde la fecha de firma del presente Contrato, siempre y cuando se hayan cumplido todas las obligaciones que la Ley y el presente Contrato le imponen.

.- Confidencialidad y reserva

Los términos y condiciones del presente Contrato se mantendrán en la más estricta confidencialidad y únicamente se desvelarán en cumplimiento de un deber legal o judicial.

Toda violación o incumplimiento, por una u otra Parte de la presente estipulación conlleva la obligación, para aquella Parte que cometió dicho incumplimiento, de pagar a la otra Parte una indemnización compensatoria, sin perjuicio, del derecho de la Parte considerada afectada a ejercer o iniciar todas las acciones pertinentes a fin de imponer las sanciones que legalmente procedan.

Esta obligación de confidencialidad deberá respetarse durante un período de: a partir de la fecha de firma de este Contrato señalada en el encabezamiento.

.- Cesión del Contrato

[ELEGIR UNA OPCIÓN: Se permite / Se prohíbe]

.- Prohibición de competencia

El vendedor se obliga a no explotar, en nombre propio o ajeno, directa o indirectamente, una empresa o negocio competidor con un objeto similar al de la [ELEGIR: empresa / unidad económica autónoma] y que, puedan desviar su clientela, en el siguiente ámbito geográfico: [ZONA GEOGRÁFICA], por un plazo de [PLAZO] desde la firma del presente Contrato señalada en el encabezamiento.

La prohibición de competencia dentro el ámbito temporal y territorial indicados conlleva las siguientes prohibiciones:

a) establecer relaciones contractuales, por cuenta propia o ajena, con empresas de la competencia que desarrollen idéntica o similar actividad a la de la [ELEGIR: empresa / unidad económica autónoma];
b) convertirse en propietario, socio, administrador o relacionarse de ninguna otra forma con entidades relacionadas con un negocio que presente servicios o productos similares a los de la [ELEGIR: empresa / unidad económica autónoma] o que de cualquier otra forma compita con la misma;
c) aceptar ningún trabajo ni prestar servicios a cualquier cliente de la [ELEGIR: empresa / unidad económica autónoma] si dicho empleo o servicio, en alguna medida, utiliza de alguna forma las técnicas o métodos empleados o los productos o servicios transmitidos por el presente contrato
d) mantener contactos o comunicarse con cualquier cliente de la Empresa, siempre que dicha comunicación se relacione con a la venta o prestación de algún producto o servicio igual o similar a cualquier producto o servicio prestado por la [ELEGIR: empresa / unidad económica autónoma].

[OPCIONAL — incluir si procede]

(Indemnización)

Toda violación o incumplimiento por el vendedor de lo aquí acordado conlleva su obligación de pagar al comprador una indemnización compensatoria, sin perjuicio, del derecho del comprador a ejercer o iniciar todas las acciones pertinentes a fin de imponer las sanciones que legalmente procedan.

.- Desistimiento y Resolución del contrato

En el caso de que exista una discordancia entre el resultado que se refleja en el balance aportado y la realidad de la empresa, y tales diferencias supongan una disminución en el neto patrimonial superior al [PORCENTAJE] de lo indicado en el balance aportado, el Comprador podrá optar entre reducir la disminución comprobada del precio pendiente de pago o resolver el contrato con la consiguiente restitución de las prestaciones por ambas partes, pactándose que además el Comprador tendrá derecho a una indemnización de daños igual a [IMPORTE] euros.

[OPCIONAL — incluir si procede]

(Si hay transmisión de inmueble)

.- Escritura Pública

En relación con el inmueble transmitido y descrito en las manifestaciones [Nº], en virtud de lo dispuesto en los artículos 1279 y 1280.1° del Código Civil, las Partes se obligan a otorgar escritura pública en un plazo máximo de [PLAZO] desde la fecha de firma de este Contrato, señalada en el encabezamiento. El retraso del comprador en el cumplimiento de esta obligación no supondrá el retraso en el cumplimiento del resto de obligaciones asumidas en el presente Contrato.

.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

.- Protección de datos personales

Las partes reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

.- Gastos e Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta del [NOMBRE DE LA PARTE].

.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones Código de Comercio, leyes especiales y usos mercantiles que le sean aplicables, o en lo no previsto, por las disposiciones del Código Civil.

.- Fuero competente

[ELEGIR UNA OPCIÓN: Si se pacta acudir a los tribunales / Si se pacta acudir a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

EL VENDEDOR

________________________________

EL COMPRADOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

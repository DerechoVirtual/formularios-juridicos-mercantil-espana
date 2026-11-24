---
name: contrato-agencia-sector-artes-graficas-mer-0495
description: "Contrato de agencia en el sector de las artes gráficas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de agencia en el sector de las artes gráficas

> Formulario **MER-0495** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de agencia en el sector de las artes gráficas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de agencia en el sector de las artes gráficas” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-agencia-sector-artes-graficas-mer-0495`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMUNIDAD AUTÓNOMA (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DE LA ZONA (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] PRODUCTOS

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

INTERVIENEN

D [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A] en lo sucesivo "LA FÁBRICA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO] en fecha [FECHA] con el número de protocolo [Nº DE PROTOCOLO] poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A] en lo sucesivo "LA AGENCIA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO] en fecha [FECHA] con el número de protocolo [Nº DE PROTOCOLO] poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE AGENCIA DE INDUSTRIA GRÁFICA, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que LA FÁBRICA es una persona jurídica de derecho privado dedicada a la [ACTIVIDAD] de [PRODUCTOS].

SEGUNDO.- Que LA AGENCIA es una persona jurídica dedicada a la prestación de servicios de intermediación en el sector de las industrias gráficas.

TERCERO.- Que ambas partes de común acuerdo llevan a efecto el presenten contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

La FABRICA, como empresa dedicada al diseño, fabricación y venta de productos de artes gráficas y de publicidad en general, en el ámbito de nacional, encarga a LA AGENCIA, y ésta la acepta, la gestión de comercialización de sus productos y mercancías, efectuando las gestiones de mediación y venta de los mismos con los clientes, así como la captación de nuevos clientes, con sujeción a las instrucciones que se contienen en el ANEXO I de este contrato, que es igualmente firmado por las partes, formando parte integrante del presente.

Las zonas geográficas en que La AGENCIA desarrollará esta actividad comercial serán las siguientes:

a) [NOMBRE DE LA ZONA]: comprendiendo los territorios de las Comunidades Autónomas de [COMUNIDAD AUTÓNOMA] y de [COMUNIDAD AUTÓNOMA] En un futuro cercano se ampliará al norte de Portugal.

b) [NOMBRE DE LA ZONA]: este ámbito incluye los territorios de las Comunidades Autónomas de [COMUNIDAD AUTÓNOMA], [COMUNIDAD AUTÓNOMA] y [COMUNIDAD AUTÓNOMA] En un futuro cercano se ampliará al sur de Francia.

Duración

La duración de este contrato será INDEFINIDA, pudiendo resolverlo unilateralmente cualquiera de las partes previa denuncia o comunicación expresa a la otra parte con un preaviso de DOS MESES. No se establece derecho a indemnización alguna para ninguna de las partes.

Comisión de ventas

Se establece como precio de la gestión una comisión sobre las ventas efectivas que se determinará para cada tipo de trabajo o para cada presupuesto, según las siguientes reglas:

▪ La comisión por ventas que reciba LA AGENCIA será el porcentaje que se determine como de "comisión zona" en el ANEXO I de este contrato, pudiendo consistir en un porcentaje fijo para todos sus clientes o para cada trabajo concreto, previo acuerdo entre las partes.

▪ Respecto de la gestión de comercialización de LA AGENCIA de los productos y mercancías de LA FÁBRICA, captación de clientes, mediación y venta de los productos de LA FÁBRICA, LA AGENCIA será quien decida y establezca el precio o tarifa a facturar al cliente final por el trabajo que se contrate o encargue, que en todo caso no podrá ser inferior al precio o tarifa que tenga establecido LA FÁBRICA. Así, LA AGENCIA comunicará por tanto a LA FABRICA el trabajo concreto y precio o tarifa por el que LA FÁBRICA facturará al cliente final.

▪ La comisión por ventas que reciba LA AGENCIA consistirá en una cantidad igual a la diferencia existente entre la cantidad por la que LA FÁBRICA factura al cliente final, tarifa fijada por LA AGENCIA, y la tarifa que tenga establecida LA FÁBRICA respecto de dicho producto o trabajo concreto.

▪ La liquidación o pago de comisiones a favor de LA AGENCIA se realizara por meses completos de facturación una vez emitidas las facturas a los clientes por LA FÁBRICA a 90 días de la fecha de facturación.

▪ En el caso en que un cliente no abonara a su vencimiento la factura emitida por LA FÁBRICA, y tuviese que intervenir el departamento jurídico para proceder al cobro, únicamente se abonará el pago de la comisión correspondiente a LA AGENCIA si finalmente se consigue el cobro de la factura inicialmente impagada, y el pago de dicha comisión a favor de LA AGENCIA se realizará en el mes en que se produzca el pago por parte del cliente.

▪ LA FÁBRICA enviara listado con las comisiones a facturar para su comprobación y aprobación, y LA AGENCIA una vez aprobado dicho listado de comisiones, emitirá la factura que será abonada por EL FABRICANTE mediante transferencia bancaria por su importe total IVA incluido al nº [Nº] de cta.

▪ LA FÁBRICA se obliga a poner en conocimiento de LA AGENCIA el momento en que se produzcan los pagos por parte de los clientes, así como a remitir los justificantes de dichos pagos si así lo solicitara LA AGENCIA.

▪ Los plazos para el pago por parte del Cliente Final podrán ser aplazados por LA FÁBRICA, a petición del Agente Comercial, siempre que así lo autorice por escrito LA FÁBRICA.

Sobre estas comisiones se aplicarán los impuestos que la normativa tributaria venga a establecer en cada momento, siendo en la actualidad el I.V.A. del tipo del 18%.

Muestrarios y tarifas

LA FÁBRICA entregará a LA AGENCIA los correspondientes muestrarios, tarifas que tenga establecidas y demás elementos materiales para su gestión de promoción, todo lo cual será remitido a su cargo, hasta su destino, comprometiéndose LA AGENCIA a conservarlo con la adecuada diligencia comercial. Al final de los sucesivos ciclos de ventas y, en todo caso, al rescindirse por cualquier causa este contrato, deberán devolverse los muestrarios, tarifas y demás elementos en su poder, en este caso a cargo de LA FÁBRICA.

En anexos, firmados por ambas partes para su unión a este contrato, se relacionarán las tarifas, objetos, instrumentos, productos y mercancías que componen el muestrario.

Medios técnicos

LA AGENCIA aportará sus propios medios técnicos y de transporte, así como su red de agentes comerciales y empleados (sin que ello implique relación laboral alguna del Fabricante con los mismos).

LA FÁBRICA deberá homologar los proveedores y sub-agentes que presten servicios a LA AGENCIA

Derecho de reserva

LA FÁBRICA se reserva el derecho a rechazar cualquier solicitud de presupuesto o pedido de Productos realizado por el comercial o por el cliente final, si tiene facturas pendientes de pago.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal en caso de no ejecución voluntaria de la sentencia]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Y en prueba de conformidad con todo lo expuesto, firman el presente por duplicado y a un solo efecto, en lugar y fecha indicados al encabezamiento.

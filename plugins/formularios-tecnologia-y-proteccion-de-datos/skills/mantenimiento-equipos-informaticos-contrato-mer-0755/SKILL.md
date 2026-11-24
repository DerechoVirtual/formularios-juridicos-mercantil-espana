---
name: mantenimiento-equipos-informaticos-contrato-mer-0755
description: "Mantenimiento de equipos informáticos (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Mantenimiento de equipos informáticos (contrato)

> Formulario **MER-0755** del plugin **Contratos tecnológicos, comercio electrónico y protección de datos** (`formularios-tecnologia-y-proteccion-de-datos`) · Mercantil › Tecnología, comercio electrónico y protección de datos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Mantenimiento de equipos informáticos (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Mantenimiento de equipos informáticos (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-tecnologia-y-proteccion-de-datos:mantenimiento-equipos-informaticos-contrato-mer-0755`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-tecnologia-y-proteccion-de-datos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos tecnológicos, comercio electrónico y protección de datos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] PERIODICIDAD
- [ ] PLAZO

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA EMPRESA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL CLIENTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE MANTENIMIENTO DE EQUIPOS INFORMÁTICOS, y a tal efecto, libremente y de común acuerdo,

EXPONEN

I.El CLIENTE es el propietario de los equipos informáticos designados en el presente contrato y se dedica profesionalmente a [ACTIVIDAD] Para la prestación de sus servicios cuenta con los medios organizativos y técnicos necesarios para su desempeño.

II.Que el CLIENTE está interesado en recibir por parte de LA EMPRESA la prestación de dichos servicios de mantenimiento en los términos y condiciones designados en el presente contrato.

III.Que por todo lo anterior, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

El presente contrato tiene por objeto el mantenimiento todos los sistemas informáticos que se adjuntan como Anexo I siempre que estas den un servicio al CLIENTE, se use o no como puesto de trabajo, incluidos sus periféricos y toma de red.

No se incluirán en el mantenimiento aquellos equipos que no estén dando servicio a la EMPRESA, por mal funcionamiento o por tener unos fines ajenos a la actividad de la empresa, así como aquellos equipos que su sistema sea rechazado por un técnico cualificado antes de la firma de este contrato.

Tampoco se incluirán aquellos periféricos implantados por otras empresas que requieran su propia configuración y mantenimiento especializado, como dispositivos de conexión a Internet (que dependerán de su proveedor de servicios de Internet), sistemas de seguimiento de personas y mercancía, configuraciones de correo, sistemas de seguridad (como antivirus o cortafuegos) o cualquier otro periférico o configuración rechazados por un técnico especialista antes de la firma del presente contrato.

Como aplicaciones, solo se dará soporte y mantenimiento a aquellas aplicaciones incluidas con los sistemas operativos y paquetes de ofimática aceptados por los técnicos, así como otras aplicaciones recomendadas, instaladas o aceptadas por los técnicos de LA EMPRESA, quedando excluidas todas aquellas aplicaciones que requieran conocimientos especializados o mantenimiento de terceras empresas. Bajo ningún concepto, se dará soporte de operativa de las aplicaciones de usuario, como ofimática, diseño gráfico, aplicaciones industriales o cualquier otro tipo de aplicación, dándose a entender que su operativa es responsabilidad de los usuarios y de los conocimientos que estos tengan para desempeñar su puesto de trabajo. No obstante, los técnicos especializados, asignados a su mantenimiento, podrán, voluntariamente, orientar al usuario a un uso correcto de las aplicaciones, siempre que el técnico asegure tener los conocimientos adecuados para desempeñar esta tarea

Precio y facturación

El precio del Contrato es de [IMPORTE] euros, IVA excluido por mes.

El pago de las facturas se realizará mensualmente y por adelantado. El CLIENTE lo hará efectivo mediante transferencia bancaria dentro de los 5 primeros días de cada mes. En la siguiente cuenta corriente titularidad de LA EMPRESA:

El precio total del mantenimiento, incluye soporte telefónico para resolución de dudas y averías por vía telefónica y administración a control remoto por Internet, con el consentimiento previo del CLIENTE para la instalación y configuración de las herramientas necesarias para desempeñar dichas tareas, así como las visitas del técnico en persona, acordadas por ambas partes, para solventar problemas que no puedan resolverse vía telefónica o por Internet y para revisar que el sistema se mantenga estable y evitar futuras averías. Se conocerá como visita la presencia del técnico en las instalaciones del CLIENTE durante un máximo de media jornada, ya sea de mañana o de tarde. Si por cualquier motivo el técnico tuviera que realizar más visitas de las acordadas en el mantenimiento, se deberán abonar 70 euros más por turno en concepto de 'visita extraordinaria'.

Revisión anual de condiciones

Al inicio de cada ejercicio fiscal, LA EMPRESA revisará los importes del mantenimiento, aplicando las diferencias legales acordes con el IPC anual. Además, se revisarán el número de puestos de trabajo y servidores a los que se van a realizar las tareas de mantenimiento, para ajustar el nuevo importe en incremento o decremento acorde a la nueva configuración.

Aumento de equipos

En caso de reparación, ampliación o instalación de puestos de trabajo nuevos, la mano de obra invertida en dichas tareas queda incluida en el mantenimiento, pero las piezas, repuestos o material necesario para dichas tareas serán facturados aparte.

Duración del contrato

El plazo de duración del presente Contrato es de [Nº] meses a partir de la fecha referida en el encabezamiento del Contrato. El Contrato podrá ser prorrogado expresamente y por escrito.

El CLIENTE podrá dar por finalizado este mantenimiento, previo aviso de 30 días naturales, sin compromiso alguno, estando obligado a abonar el total de las facturas pendientes de mantenimientos u otros gastos (apartado 7 del presente contrato), estando libre de abonar cualquier tipo de factura por operaciones o materiales no disfrutados por parte del cliente.

Acuerdo de nivel de servicio

Todos los Servicios prestados por LA EMPRESA se realizarán por personal especializado en cada materia. El personal de LA EMPRESA acudirá previsto de todo el material necesario, adecuado y actualizado, para prestar los Servicios.

Las averías o el mal funcionamiento de los equipos se comunicarán a través de llamada telefónica o envío de fax.

Los problemas se resolverán en un período máximo de [PLAZO]

( Se entiende por incidencia crítica: las incidencias que, en el marco de la prestación de los Servicios, afectan significativamente al CLIENTE.

( Se entiende por incidencia grave: las incidencias que, en el marco de la prestación de los Servicios, afectan moderadamente al CLIENTE.

( Se entiende por incidencia leve: las incidencias que se limitan a entorpecer la prestación de los Servicios.

La reparación se realizará en los siguientes períodos máximos desde el aviso:

( Incidencia crítica

( Incidencia grave

( Incidencia leve

El estado de los equipos se revisará [PERIODICIDAD] por el CLIENTE y LA EMPRESA para comprobar su buen funcionamiento.

Confidencialidad

Todos los documentos, informaciones, acuerdos, contratos y precontratos, quedando incluidos los correos electrónicos y todo tipo de comunicaciones para la realización de este contrato, así como cualquier conocimiento o información que pudiera tenerse sobre cualquiera de las dos partes o sus actividades son información completamente confidencial, por lo que deberá ser tratada con el más absoluto de los secretos, aun extinguida la relación contractual.

Protección de datos

En cumplimiento de lo dispuesto en la Ley Orgánica 3 / 2018, de 5 de diciembre, de Protección de Datos Personales y Garantía de Derechos Digitales, le informamos que sus datos personales quedarán incorporados y serán tratados en los ficheros de ambas partes, con el fin de poder mantener la presente relación contractual. Le informamos de la posibilidad de ejercer sus derechos de acceso, rectificación, cancelación y oposición sobre sus datos de carácter personal solicitándolo por escrito junto a una fotocopia de su DNI en la siguiente dirección indicada en la cabecera del presente contrato.

Resolución del contrato

El incumplimiento por cualquier de las partes de cualquiera de las obligaciones que este contrato impone, facultará a la parte contraria a resolver de forma inmediata el presente contrato o exigir su cumplimiento, sin perjuicio de la indemnización de daños y perjuicios que proceda en ambos casos.

No obstante el presente contrato se extinguirá, además de por las causas generales del Derecho, por las siguientes:

a. Por el incumplimiento de alguna de las cláusulas del presente contrato. En tal caso no será necesario preavisar, y en ningún caso abonar cantidad indemnizatoria alguna por parte de la parte que rescindió el contrato.

b. Por el transcurso de la duración del mismo, o en su caso si se hubiera solicitado la no renovación y siempre que se hubiera cumplido con el plazo de preaviso.

c. Por ser declarados en situación de suspensión de pagos, quiebra o concurso de acreedores cualquiera de las partes.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Jurisdicción competente y ley aplicable / Sumisión a tribunales / Opción 10.1: Sumisión a tribunales / Sumisión a arbitraje / Opción 10.2: Sumisión a arbitraje]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE MANTENIMIENTO DE EQUIPOS INFORMÁTICOS extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(LA EMPRESA)

Fdo. Don [NOMBRE Y APELLIDOS]

(El CLIENTE)

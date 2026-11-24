---
name: contrato-servicios-intermediacion-adopcion-mer-0567
description: "Contrato de servicios de intermediación en adopción internacional. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicios de intermediación en adopción internacional

> Formulario **MER-0567** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicios de intermediación en adopción internacional» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicios de intermediación en adopción internacional” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-servicios-intermediacion-adopcion-mer-0567`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] PAÍS DE ADOPCIÓN (12 veces)
- [ ] IMPORTE (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FECHA
- [ ] IMPORTE EN LETRA
- [ ] LUGAR
- [ ] MES
- [ ] NACIONALIDAD
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] Nº DE CUENTA (IBAN)
- [ ] Nº DE PROTOCOLO

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

De una parte:

D [NOMBRE Y APELLIDOS] mayor de edad, de estado civil [ESTADO CIVIL] vecino de [LOCALIDAD] domiciliado en [DOMICILIO] con documento nacional de identidad número [NÚMERO]

De otra:

D [NOMBRE Y APELLIDOS] mayor de edad, de estado civil [ESTADO CIVIL] vecino de [LOCALIDAD] domiciliado en [DOMICILIO] con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D [NOMBRE Y APELLIDOS] en nombre propio.

D [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A] en lo sucesivo "LA ASOCIACIÓN", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO] en fecha [FECHA] con el número de protocolo [Nº DE PROTOCOLO] poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE PRESTACIÓN DE SERVICIOS DE INTERMEDIACIÓN EN ADOPCIÓN INTERNACIONAL, y a tal efecto, libremente y de común acuerdo,

EXPONEN

Que Don [NOMBRE Y APELLIDOS] y Doña [NOMBRE Y APELLIDOS] han decidido adoptar un menor de nacionalidad [NACIONALIDAD], siendo su deseo tramitar el Expediente de Adopción a través de LA ASOCIACIÓN, llevándose a efecto por ambas partes el presente Contrato, a tenor de las siguientes

CLÁUSULAS

Objeto

a).- ASOCIACIÓN se compromete a tramitar el expediente de Adopción encomendado, que comprende los servicios que se determinan en la cláusula siguiente.

b).- La duración del presente contrato surte efecto desde la firma del mismo y durante el periodo de tiempo necesario para la conclusión de los trámites de adopción objeto del contrato, salvo que por alguna de las partes se proceda a la resolución, lo cual se ha de notificar por escrito.

c).- El contrato dejara de producir efectos por resolución de cualquiera de los contratantes, cuando concurra en el otro causa alguna de incumplimiento, o por el cumplimiento de las actividades en el previstas para la conclusión de la tramitación de la adopción.

SERVICIOS

Con carácter general, ASOCIACIÓN ofrece a los interesados en la adopción de menores [PAÍS DE ADOPCIÓN] los siguientes servicios, siendo el punto cuatro obligación de AIPAME.

EN LA FASE INICIAL DE LA ADOPCIÓN

A) GESTIÓN Y TRAMITACIÓN EN ESPAÑA:

• Recepción y registro de los documentos remitidos por los Organismos españoles. (Certificado de idoneidad, informe psico-social y compromiso de seguimiento).

• Información sobre los documentos exigidos por la Legislación de la Federación Rusa para la tramitación del Expediente de Adopción.

• Comprobación de que el Expediente está completo y todos los documentos perfectamente diligenciados.

• Envío del Expediente de Adopción a su Delegación en Moscú.

B) CURSO DE FORMACIÓN:

ASOCIACIÓN impartirá un Curso de Formación de Padres de acuerdo con el Programa de Trabajo aprobado por el Organismo de la Comunidad Autónoma. El Curso se divide en dos fases, la primera se llevará a efecto en la Fase Inicial de la Adopción y la segunda cuando se produzca aceptación de la Preasignación del menor.

Durante el curso de formación se tratarán los siguientes aspectos de la adopción:

• Información y asesoramiento jurídico sobre los aspectos legales de la adopción en la legislación Española. La adopción internacional.

• La adopción en la legislación [PAÍS DE ADOPCIÓN] Efectos legales de la adopción. Información sobre las características del país de origen del menor. Situación social y económica actual. Situación general de los menores. La vida en los Orfanatos. Funcionamiento de las Instituciones extranjeras.

• Situación de los menores: su historia previa, diferencias culturales, de idioma etc. La familia después de la adopción. Principales problemas que se plantean.

• Conocer la realidad socio-familiar de los adoptantes. Exponer y tratar los problemas que pueden surgir en la integración del menor en el entorno social y familiar. Reflexionar sobre el proceso de crecimiento del niño.

• La importancia de la cultura de origen como parte histórica del niño. El enriquecimiento del grupo familiar en la integración de dos culturas.

• Preparación del viaje a [PAÍS DE ADOPCIÓN]

• Seguimiento y control en los primeros meses de la llegada del hijo. Escolarización del menor. Integración del hijo en la familia y en la sociedad.

Estos temas se trabajarán en pequeños grupos y a través de entrevistas individuales tanto con la Trabajadora Social como con la Psicóloga.

EN LA FASE DE PREASIGNACIÓN:

• Recepción del documento referente a la Preasignación del menor. Informar de la misma a los Organismos Españoles, sometiéndola a su aprobación.

• Informar a los adoptantes de la existencia de la Preasignación, poniendo en su conocimiento todos los datos disponibles sobre el menor y recabando su aceptación para la adopción.

• Remitir a los Organismos extranjeros a través de su Delegación en [PAÍS DE ADOPCIÓN], el informe sobre la Preasignación del menor emitido por los Organismos Españoles y la aceptación o no de los adoptantes.

• Información de los documentos necesarios para la entrada del menor en España y, de los que exige el Consulado Español en [PAÍS DE ADOPCIÓN] para el reconocimiento e inscripción de la adopción.

CONSTITUClÓN DE LA ADOPCIÓN:

• Informar a los adoptantes sobre cuándo pueden trasladarse al país de origen del menor, para ultimar los trámites de la adopción.

• Asistencia y apoyo en todos los trámites Judiciales y Administrativos de la adopción en [PAÍS DE ADOPCIÓN]

• Obtención y diligenciamiento de las certificaciones de nacimiento original y nueva del menor.

• Obtención y diligenciamiento de la certificación de adoptabilidad del menor.

• Legalización y compulsa de la Resolución Judicial constitutiva de la adopción.

• Ayudar a los adoptantes en las gestiones de legalización o cualquiera otras que deban realizar ante las dependencias del Consulado Español en [PAÍS DE ADOPCIÓN]

• Asesorar a los adoptantes sobre la inscripción registral de la adopción.

• Velar para que la familia adoptante realice la inscripción de la adopción en el Registro del Consulado de [LOCALIDAD] en España.

• Comprobar que se dispone de toda la documentación pertinente para el reconocimiento de eficacia en nuestro país de la Resolución emitida por las autoridades extranjeras.

• Comprobar que el menor reúne todos los requisitos y la documentación necesaria para su entrada y residencia en España.

• Comunicar a los Organismos Españoles la constitución de la adopción, mediante copia compulsada de la resolución de la adopción.

• Comunicar al Departamento competente en materia de Servicios Sociales de la Diputación Foral que corresponda y al organismo competente del país de origen del niño, que la resolución de adopción se encuentra inscrita en el Registro Civil Central o Consular correspondiente. A la Diputación Foral se le facilitara una copia de la inscripción registral.

FASE DE SEGUIMIENTO:

• Seguimiento detallado de la evolución del menor en el entorno familiar, con el fin de procurar una adecuada integración.

• Seguimiento del menor en su entorno psico-social.

• Detectar e informar sobre las posibles patologías de adaptación que pudieran surgir en esta fase.

• Elaboración y remisión de informes del seguimiento tanto a los Organismos Españoles como [PAÍS DE ADOPCIÓN], con la periodicidad establecida en la legislación aplicable.

Condiciones

LA ASOCIACIÓN no admitirá la solicitud de adopción internacional de aquellas personas que ya tengan en trámite otra solicitud anterior. Únicamente se procederá a tramitar dicha solicitud, cuando el expediente inicial este finalizado o, hubiera sido cancelado. A estos efectos, los interesados deberán firmar una declaración jurada manifestando que no tienen otro expediente de adopción en trámite y asumiendo toda la responsabilidad al respecto.

PRECIO Y FORMA DE PAGO

Precio

El coste a abonar por los solicitantes a la Entidad, como contraprestación por los servicios prestados es [IMPORTE]

En relación a las presentes cantidades, y como aclaración a las mismas, se hace constar que el precio incluye todos los costes de mantenimiento, infraestructura y personal de la Entidad necesarios para la gestión del expediente, así como de todos aquellos costes que no puedan o sean difícilmente individualizables y los cuatro informes de seguimientos.

Los gastos directos del expediente son los que, con carácter general, son individualizables y atribuibles únicamente a la gestión del concreto, incluso con carácter excepcional, y justificables como tales. La partida en cuestión se liquidará en base a ello al término de la tramitación objeto del contrato. Con cargo a esta partida se podrá liquidar aquellos gastos que se hayan podido producir por variaciones sustanciales en los costes en el país de origen previa notificación de los mismos a los interesados.

Forma de pago

Los adoptantes abonaran a la firma del presente documento la cantidad de [IMPORTE] € mediante transferencia bancaria a la cuenta [Nº DE CUENTA (IBAN)]

Después del viaje de asignación abonaran [IMPORTE] € a la cuenta anteriormente mencionada. Antes de viajar a juicio abonaran la cantidad de [IMPORTE] € en concepto de seguimientos especificados anteriormente en la misma cuenta.

Las cantidades correspondientes a los GASTOS EN [PAÍS DE ADOPCIÓN] se abonarán a la remisión de la documentación, mediante transferencia bancaria [IMPORTE EN LETRA] ( euros) en la cuenta bancaria número

Los costos de la tramitación en [PAÍS DE ADOPCIÓN] incluyen básicamente el mantenimiento, infraestructura, gastos de personal y gestión del expediente (traducción, legalización, etc.).

Gastos en el extranjero no imputables a la ASOCIACIÓN

En ningún caso se entienden incluidos los gastos de viaje, estancia, acompañamiento o intérpretes en [PAÍS DE ADOPCIÓN] Tales gastos serán abonados directamente por las familias en [IMPORTE] € como se indicara en este apartado a continuación.

Asimismo, abonarán a los correspondientes prestatarios de servicios, aquellas cantidades que en el momento de la firma del presente acuerdo se establezcan para la consecución de los servicios complementarios que conlleva el proceso adoptivo y que en ningún caso forman parte del presente contrato por no ser esta entidad la prestataria de estos servicios.

La familia realizará una provisión de fondos a LA ASOCIACIÓN, para que esta liquide en nombre de la familia los suplidos y gastos de traslados, interpretes y traductores oficiales. El importe total de la provisión de fondos será de [IMPORTE] € ( €). Se informa a la familia que se realiza una aportación económica a la institución extranjera que proceda de [IMPORTE] € por cada uno de los menores adoptados.

LA ASOCIACIÓN facilitara a los solicitantes información sobre las tarifas usuales de alojamientos, trasportes, interpretes y demás conceptos para situaciones al margen del proceso adoptivo.

Cambios legislativos

LA ASOCIACIÓN en ningún caso responderá por las consecuencias legales o materiales que se deriven de los cambios legislativos que pudieran producirse en las normativas sobre adopción tanto en [PAÍS DE ADOPCIÓN] como en España.

Retraso en la tramitación

LA ASOCIACIÓN no se responsabiliza de cualesquiera demoras en los trámites administrativos y jurisdiccionales de los expedientes de adopción, siempre que estos retrasos sean por causas no imputables a la actuación de LA ASOCIACIÓN.

Resolución del contrato

En caso de rescisión del presente contrato, las sumas abonadas se atribuirán al pago de los servicios prestados, devolviéndose a la familia o debiendo abonar ésta la diferencia entre la nota de gastos y el importe remitido. LA ASOCIACIÓN se compromete a gestionar dicha liquidación.

[ELEGIR UNA OPCIÓN: Jurisdicción y ley aplicable / Sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal en caso de no ejecución voluntaria de la sentencia]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

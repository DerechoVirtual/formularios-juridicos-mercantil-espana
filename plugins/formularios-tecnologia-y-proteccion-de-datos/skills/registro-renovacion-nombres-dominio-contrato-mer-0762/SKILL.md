---
name: registro-renovacion-nombres-dominio-contrato-mer-0762
description: "Registro y renovación de nombres de dominio (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Registro y renovación de nombres de dominio (contrato)

> Formulario **MER-0762** del plugin **Contratos tecnológicos, comercio electrónico y protección de datos** (`formularios-tecnologia-y-proteccion-de-datos`) · Mercantil › Tecnología, comercio electrónico y protección de datos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Registro y renovación de nombres de dominio (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Registro y renovación de nombres de dominio (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-tecnologia-y-proteccion-de-datos:registro-renovacion-nombres-dominio-contrato-mer-0762`.
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
- [ ] NOMBRE DE DOMINIO (5 veces)
- [ ] Nº (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] EXTENSIÓN DE DOMINIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PLAZO (2 veces)
- [ ] AÑO
- [ ] DIRECCIÓN
- [ ] DIRECCIÓN IP
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL SERVIDOR

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

CONTRATO DE REGISTRO Y RENOVACIÓN DE NOMBRES DE DOMINIO

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS] mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL CLIENTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL AGENTE REGISTRADOR", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE REGISTRO Y RENOVACIÓN DE NOMBRES DE DOMINIO, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO: Que el CLIENTE está interesado en la contratación de los servicios de registro de [NOMBRE DE DOMINIO] (indicar nombre) como nombre de dominio en Internet accediendo al DNS, y en los servicios de renovación del registro de nombre de dominio en Internet.

SEGUNDO: Que el AGENTE REGISTRADOR es una empresa especializada en la intermediación en los procesos de registro y renovación de los nombres de dominio en Internet.

TERCERO: Que las Partes reunidas en la sede social del CLIENTE, acuerdan celebrar el presente contrato de TIENDA VIRTUAL, en adelante el "Contrato", de acuerdo con las siguientes

CLÁUSULAS

Objeto

En virtud del Contrato el AGENTE REGISTRADOR se obliga a registrar a nombre del CLIENTE el nombre [NOMBRE DE DOMINIO] como nombre de dominio en Internet, de segundo nivel bajo [EXTENSIÓN DE DOMINIO] en el Registro competente para ello, así como de realizar las correspondientes renovaciones del registro de [NOMBRE DE DOMINIO] como nombre de dominio en Internet.

Términos y condiciones específicos de la prestación de los servicios

El AGENTE REGISTRADOR prestará los Servicios en los siguientes términos y condiciones específicos:

2.1El AGENTE REGISTRADOR declara que toda la información que consta en este contrato, sobre el registro, es correcta y completa.

2.2El CLIENTE autorizará al AGENTE REGISTRADOR para que pueda actuar en su nombre ante el Registrador o Autoridad de Asignación, para realizar todas las actuaciones necesarias para la asignación y renovación del nombre de dominio, recibir todas las comunicaciones y realizar los pagos por la asignación o renovación del nombre de dominio.

2.3El CLIENTE se obliga a poner en conocimiento del AGENTE REGISTRADOR cualquier modificación en los datos aportados en este contrato y autoriza a éste para cambiar los datos ante el Registro o Autoridad de Asignación. Para este fin el AGENTE REGISTRADOR proporcionará un nombre de usuario y una clave de acceso vía web, para poder acceder y cambiar sus datos excepto el de titular del nombre de dominio.

2.4El AGENTE REGISTRADOR solicitará la disponibilidad del nombre [NOMBRE DE DOMINIO], a través de WHOIS del Registro correspondiente, bajo el "." elegido.

2.5Una vez comprobado que el nombre de dominio está libre. El AGENTE REGISTRADOR realizará la solicitud y las gestiones correspondientes, siempre respetando las normas y plazos establecidos por cada Registro o Autoridad de Asignación, encaminadas al Registro, transferencia y renovación del Nombre de Dominio de segundo nivel bajo [EXTENSIÓN DE DOMINIO] elegido por el CLIENTE.

2.6El CLIENTE reconoce que es el AGENTE REGISTRADOR quien debe efectuar la solicitud correspondiente ante los organismos competentes, pero la concesión, la transferencia o la renovación del nombre de dominio es responsabilidad exclusiva del Registro o Autoridad de Asignación. También reconoce el CLIENTE que no existe ninguna relación contractual entre él y el Registro o Autoridad de Asignación.

2.7El CLIENTE acepta que es el único responsable de la elección de este nombre de dominio y de su posterior mantenimiento.

2.8El CLIENTE declara que el uso del nombre de dominio, que se va registrar, no infringe los derechos de terceras personas y que se utilizará dentro de la legalidad.

2.9El CLIENTE reconoce que la titularidad y responsabilidad última sobre el nombre de dominio recae sobre quien figura como titular del mismo.

2.10El CLIENTE acepta todas las normas y condiciones impuestas por todas las Organizaciones Reguladoras, Registros o Autoridades de Asignación, nacionales e internacionales, de nombres de dominio en Internet.

2.11El AGENTE REGISTRADOR una vez obtenida la concesión del nombre de dominio, comunicará y entregará al CLIENTE la documentación acreditativa de la inscripción. La comunicación de la concesión por parte del Registro o Autoridad de Asignación del nombre de dominio solicitado se efectuará mediante correo electrónico a la dirección del CLIENTE proporcionada en la solicitud. Hasta la recepción de la comunicación el CLIENTE no deberá considerarse titular del nombre de dominio.

2.12El CLIENTE se compromete a realizar y guardar una copia de todos los archivos de su nombre dominio por si fuese necesario reemplazarlos.

2.13El nombre de dominio quedará asignado a la dirección IP [DIRECCIÓN IP] El CLIENTE autoriza al AGENTE REGISTRADOR a dar todos sus datos necesarios al servidor [NOMBRE DEL SERVIDOR], que se encuentra situado en

2.14Si el CLIENTE estuviese interesado en la adjudicación de nombres de subdominios o nombres de dominio de Internet de 3º nivel, partiendo del nombre dominio registrado por este contrato, el AGENTE REGISTRADOR se los proporcionará previo pago del precio según la tarifa vigente.

2.15El AGENTE REGISTRADOR comunicará al CLIENTE la necesidad de renovación del registro del nombre de dominio [NOMBRE DE DOMINIO], quince días antes de su caducidad, para que proceda al pago de la renovación según la tarifa vigente. La renovación se realizará previo pago del precio.

2.16En el supuesto de que el CLIENTE no pagase la renovación del registro, el AGENTE REGISTRADOR no procederá a la renovación del mismo.

2.17Cuando no se produzca la renovación del nombre de dominio, éste pasara a estar en reserva para el titular durante [PLAZO]. Una vez pasado el tiempo de reserva el nombre de dominio pasará a estar libre y a disposición del público en general.

2.18El AGENTE REGISTRADOR podrá bloquear el nombre de dominio para corregir errores en el nombre de dominio, cometidos por él, por el Registrador o por la Autoridad de Asignación.

2.19El CLIENTE como titular del nombre de dominio podrá transmitirlo, si está al corriente de la renovación del mismo, y lo realiza por contrato escrito ante el AGENTE REGISTRADOR.

2.20El AGENTE REGISTRADOR se compromete a contestar a cualquiera petición de cambio de Agente Registrador en 24 horas, siempre y cuando el CLIENTE esté al corriente de todos los pagos.

2.21El CLIENTE se compromete a colaborar con el AGENTE REGISTRADOR para llevar a buen fin el presente contrato y solucionar cualquier incidencia en el plazo más breve posible.

2.22El AGENTE REGISTRADOR ejecutará el Contrato realizando de manera competente y profesional los Servicios, cumpliendo los niveles de calidad exigidos.

Garantías

El AGENTE REGISTRADOR declara que está en posesión de las acreditaciones necesarias para actuar ante los Registros de nombres de dominio.

Responsabilidades

El AGENTE REGISTRADOR no es responsable de aquello que le sea exclusivamente imputable al CLIENTE o titular, ni de aquello que sea imputable a la actuación del Registrador o Autoridad de Asignación, así como de los errores que resulten del proceso de registro.

El AGENTE REGISTRADOR se reserva el derecho de suspender o cancelar el nombre de dominio del CLIENTE o titular, cuando el mismo sea utilizado para enviar publicidad comercial no solicitada, o si el titular usa el nombre de dominio para realizar actividades ilegales.

Si el CLIENTE o titular incumple cualesquiera de las obligaciones contenidas en este contrato, el AGENTE REGISTRADOR se reserva el derecho de suspender o cancelar el nombre de dominio del titular.

El AGENTE REGISTRADOR se reserva el derecho de bloquear, denegar, cancelar o transferir cualquier nombre de dominio siempre que a su juicio, sea necesario para: cumplir con la legislación aplicable, con los requerimientos legales y en el cumplimiento de cualquier procedimiento de resolución de controversias; por incumplimiento de los términos y condiciones de este contrato. Para evitar cualquier responsabilidad civil o criminal del AGENTE REGISTRADOR, del Registrador o de la Agencia de Asignación y de sus empleados.

El AGENTE REGISTRADOR no será responsable de las consecuencias que se puedan producir por la falta de operatividad de la dirección e-mail de contacto del CLIENTE.

El AGENTE REGISTRADOR no garantiza la utilidad de la elección del nombre de dominio para la realización de ninguna actividad en particular.

La responsabilidad del AGENTE REGISTRADOR, del Registro o de la Agencia de Asignación se limitará al importe de la tasa de registro aplicable en el momento de suscitarse la controversia.

Ni el Registro competente, ni la Agencia de Asignación, ni el AGENTE REGISTRADOR serán, en ningún caso, responsables por la vulneración de derechos de propiedad intelectual o industrial, o de cualesquiera otros derechos o intereses legítimos que puedan derivarse del registro o renovación del nombre de dominio solicitado por el CLIENTE.

El CLIENTE es el único responsable frente a cualquier reclamación o acción legal, judicial o extrajudicial, iniciada por terceras personas, en relación con la titularidad del nombre de dominio registrado tanto contra el CLIENTE como contra el AGENTE REGISTRADOR y contra el Registro o Autoridad de Asignación, asumiendo el CLIENTE cuantos gastos, costes e indemnizaciones sean irrogadas a cualesquiera de los anteriores con motivo de tales reclamaciones o acciones legales.

[ELEGIR UNA OPCIÓN: Precio y forma de pago / Pago no aplazado / Pago aplazado]

Calidad de los servicios prestados

El AGENTE REGISTRADOR se obliga a gestionar y obtener, a su cargo, todas las licencias, permisos y autorizaciones administrativas, tanto españolas como internacionales, que pudieren ser necesarias para la realización de los Servicios.

Confidencialidad

El AGENTE REGISTRADOR guardará confidencialidad sobre la información que le facilite el CLIENTE en o para la ejecución del Contrato o que por su propia naturaleza deba ser tratada como tal. Se excluye de la categoría de información confidencial toda aquella información que sea divulgada por el CLIENTE, aquella que haya de ser revelada de acuerdo con las disposiciones de la ICANN, con las leyes, con una resolución judicial o acto de autoridad competente. Este deber se mantendrá durante un plazo de tres años a contar desde la finalización del servicio.

Protección de datos

En este sentido, y por requisito establecido por la ICANN, el titular del nombre de dominio autoriza la publicación de los datos relativos a la titularidad del nombre de dominio en cuestión y de los contactos administrativo, técnico y de pago que según la normativa, deben ser públicos y accesibles desde el WHOIS de los registradores competentes.

En el caso de que la prestación de los Servicios suponga la necesidad de acceder a datos de carácter personal, el AGENTE REGISTRADOR, en los supuestos en que sea encargado del tratamiento, queda obligado al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

El AGENTE REGISTRADOR responderá, por tanto, de las infracciones en que pudiera incurrir en el caso de que destine los datos personales a otra finalidad, los comunique a un tercero, o en general, los utilice de forma irregular, así como cuando no adopte las medidas correspondientes para el almacenamiento y custodia de los mismos. A tal efecto, se obliga a indemnizar al CLIENTE, por cualesquiera daños y perjuicios que sufra directamente, o por toda reclamación, acción o procedimiento, que traiga su causa de un incumplimiento o cumplimiento defectuoso por parte del AGENTE REGISTRADOR de lo dispuesto tanto en el Contrato como lo dispuesto en la normativa reguladora de la protección de datos de carácter personal.

A los efectos de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales, el AGENTE REGISTRADOR únicamente tratará los datos de carácter personal a los que tenga acceso conforme a las instrucciones del CLIENTE y no los aplicará o utilizará con un fin distinto al objeto del Contrato, ni los comunicará, ni siquiera para su conservación, a otras personas. En el caso de que el AGENTE REGISTRADOR destine los datos a otra finalidad, los comunique o los utilice incumpliendo las estipulaciones del Contrato, será considerado también responsable del tratamiento, respondiendo de las infracciones en que hubiera incurrido personalmente.

El AGENTE REGISTRADOR deberá adoptar las medidas de índole técnica y organizativas necesarias que garanticen la seguridad de los datos de carácter personal y eviten su alteración, pérdida, tratamiento o acceso no autorizado, habida cuenta del estado de la tecnología, la naturaleza de los datos almacenados y los riesgos a que están expuestos, ya provengan de la acción humana o del medio físico o natural. A estos efectos el AGENTE REGISTRADOR deberá aplicar las medidas técnicas y organizativas apropiadas para garantizar un nivel de seguridad adecuado al riesgo, conforme al artículo 32 del Reglamento (UE) 2016/679 (RGPD).

El CLIENTE podrá en cualquier momento ejercitar los derechos de acceso, oposición, rectificación y cancelación enviando por carta certificada, la solicitud indicando los motivos y junto con la fotocopia del DNI, a la dirección [DIRECCIÓN] (dirección) del AGENTE REGISTRADOR.

DURACIÓN DEL CONTRATO

El plazo de duración del presente Contrato para realizar el registro es de [PLAZO] a partir de la fecha de recepción de la transferencia bancaria.

La renovación se realizará dentro del plazo estipulado por el Registrador para renovar el nombre de dominio y una vez recibido el pago por transferencia bancaria del CLIENTE.

Las renovaciones del registro del nombre de dominio se obtendrán siempre que el CLIENTE no renuncie o pierda la titularidad del nombre de dominio, o cambie de Agente Registrador.

Pacto de no contratación

El CLIENTE se compromete a no contratar a persona alguna de las que prestan sus servicios para EL AGENTE REGISTRADOR. La presente cláusula extenderá su vigencia incluso con posterioridad a la extinción del presente contrato por un período de [Nº] años.

En caso de incumplimiento del presente acuerdo, EL CLIENTE estará obligado a indemnizar al AGENTE REGISTRADOR con la cantidad de [IMPORTE] euros.

Resolución

El Contrato podrá resolverse por las siguientes causas:

1.Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2.Por acuerdo de las Partes por escrito.

3.La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

Gastos e impuestos

El AGENTE REGISTRADOR se hará cargo de la totalidad de los tributos, cualesquiera que sea su naturaleza y carácter, que se devenguen como consecuencia del Contrato, así como cualesquiera operaciones físicas y jurídicas que conlleve, salvo el Impuesto sobre el Valor Añadido (IVA) o su equivalente, que el AGENTE REGISTRADOR repercutirá al CLIENTE

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sin cláusula penal / Sumisión a tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal / Sumisión a tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Suministro a arbitraje / Sin cláusula penal / Sumisión a Arbitraje sin cláusula penal en caso de no ejecución voluntaria del laudo / Coin cláusula penal / Sumisión a Arbitraje con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE REGISTRO Y RENOVACIÓN DE NOMBRES DE DOMINIO, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(El Cliente)

Fdo. Don [NOMBRE Y APELLIDOS]

(El Agente Registrador)

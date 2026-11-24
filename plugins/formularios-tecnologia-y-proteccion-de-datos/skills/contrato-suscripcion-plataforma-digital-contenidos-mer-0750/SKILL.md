---
name: contrato-suscripcion-plataforma-digital-contenidos-mer-0750
description: "Contrato de suscripción a plataforma digital de contenidos con opción de aportar contenido propio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de suscripción a plataforma digital de contenidos con opción de aportar contenido propio

> Formulario **MER-0750** del plugin **Contratos tecnológicos, comercio electrónico y protección de datos** (`formularios-tecnologia-y-proteccion-de-datos`) · Mercantil › Tecnología, comercio electrónico y protección de datos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de suscripción a plataforma digital de contenidos con opción de aportar contenido propio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de suscripción a plataforma digital de contenidos con opción de aportar contenido propio” para mi caso». También puedes invocarla directamente con `/formularios-tecnologia-y-proteccion-de-datos:contrato-suscripcion-plataforma-digital-contenidos-mer-0750`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-tecnologia-y-proteccion-de-datos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos tecnológicos, comercio electrónico y protección de datos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NOMBRE DE LA PLATAFORMA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] DIRECCIÓN WEB
- [ ] FECHA
- [ ] IMPORTE
- [ ] INSCRIPCIÓN
- [ ] INSTITUCIÓN ARBITRAL
- [ ] INSTITUCIÓN DE MEDIACIÓN
- [ ] NOMBRE DEL NOTARIO
- [ ] PLATAFORMA
- [ ] PLAZO
- [ ] PROVINCIA

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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [FECHA]

INTERVIENEN

D./Dª [NOMBRE Y APELLIDOS], interviene en su propio nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], NIF, dirección de correo electrónico, con los datos expresados anteriormente, en adelante EL/LA CLIENTE.

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF, domiciliada en y constituida en [LOCALIDAD] ante la Notaría de [LOCALIDAD] D.Dª [NOMBRE DEL NOTARIO], en fecha e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], dirección de correo electrónico, teléfono móvil, en adelante LA PLATAFORMA.

MANIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE SUSCRIPCIÓN A LA PLATAFORMA DIGITAL [NOMBRE DE LA PLATAFORMA] CON OPCIÓN DE CREACIÓN DE CANALES E INCLUSIÓN DE CONTENIDOS, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que la PLATAFORMA es titular exclusiva de todos los derechos de explotación que se derivan de la propiedad intelectual de la plataforma digital, como servicio de alta disponibilidad, redundancia y escalabilidad, siendo la única persona autorizada a permitir el acceso a dicha plataforma por los interesados que se lo soliciten.

II. Que la PLATAFORMA ofrece el servicio de acceso ilimitado a sus contenidos mediante suscripción y, en su caso, por servicios premium adicionales o servicios de pago. Opcionalmente, ofrece el programa Creadores para la creación de canales por parte de los suscriptores que pueden incorporar sus propios contenidos.

III. Que EL/LA CLIENTE está interesada en concertar la suscripción a los contenidos de la PLATAFORMA, así como el de optar a la creación de canales con contenidos propios.

IV. Que, conviniendo ambas partes en concertar el contrato, otorgan a tal fin el presente CONTRATO DE SUSCRIPCIÓN A LA PLATAFORMA DIGITAL [NOMBRE DE LA PLATAFORMA] CON OPCIÓN DE CREACIÓN DE CANALES E INCLUSIÓN DE CONTENIDOS, en base a las siguientes

CLAUSULAS

PRIMERA.- OBJETO DEL CONTRATO

El objeto del presente contrato es la prestación por parte de la PLATAFORMA a EL/LA CLIENTE del servicio de acceso a los contenidos de la plataforma digital, así como todos los servicios complementarios al uso de dicha plataforma, tales como actualizaciones de la aplicación y servicio de soporte en horario laboral, de conformidad con lo estipulado en el presente contrato.

La PLATAFORMA ofrece el acceso a ciertas funciones o contenido premium a cambio de tarifas únicas o periódicas, a los servicios de pago, en los términos establecidos en las reglas de uso y tarifas de los servicios de pago que EL/LA CLIENTE manifiesta conocer y que se incorporan como Anexo I de este contrato.

Las opciones y características actualizadas de la plataforma [PLATAFORMA] son las que figuran en la dirección web [DIRECCIÓN WEB]

La prestación del servicio de suscripción no implica ni directa ni indirectamente cesión alguna a EL/LA CLIENTE de derechos de propiedad intelectual de ningún tipo sobre la citada plataforma, que quedan expresamente reservados a su legítimo titular. EL/LA CLIENTE no podrá ceder, traspasar ni subarrendar a terceros los derechos y obligaciones que le corresponden derivados de este contrato, sin el previo consentimiento expreso de la PLATAFORMA.

El servicio de suscripción incorpora, como contenido opcional, el programa CREADORES, mediante el cual el suscriptor puede crear canales a los que puede incorporar sus propios contenidos. De ejercitarse esta opción, la PLATAFORMA se obliga a incluir los canales y contenidos del EL/LA CLIENTE, en los términos y condiciones que se pactan en este contrato.

SEGUNDA.- PRECIO DE LA SUSCRIPCIÓN Y FORMA DE PAGO

El precio del servicio de suscripción al contenido de LA PLATAFORMA es de [IMPORTE] euros/mensuales.

Los servicios adicionales de pago se facturan conforme a las tarifas que se recogen en el Anexo I de este contrato, que son actualizadas periódicamente en la dirección web

Desde el primer día del mes natural siguiente al de la fecha de este contrato, LA PLATAFORMA procederá a facturar por anticipado con cadencia trimestral el precio del servicio de suscripción, el cual será abonado en la cuenta que designa EL/LA CLIENTE con el número, en la entidad bancaria, sucursal, donde se cargarán los recibos trimestrales.

Los servicios adicionales de pago se facturarán por trimestre vencido, siendo abonados de la misma forma.

EL/LA CLIENTE podrá darse de baja en el servicio en cualquier momento, mediante comunicación escrita y fehaciente a LA PLATAFORMA que podrá dirigir a la dirección de correo electrónico, viniendo obligado a pagar únicamente por los meses naturales en los que haya mantenido en vigor su acceso a LA PLATAFORMA, y, en su caso, los servicios adicionales de pago, sin perjuicio de que pueda ejercer su derecho de desistimiento conforme a lo previsto en el Real Decreto Legislativo 1/2007, de 16 de noviembre, por el que se aprueba el texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, notificándolo debidamente por escrito y de forma fehaciente a la citada dirección de correo electrónico dentro del plazo legal.

TERCERA.- CONDICIONES Y MONETIZACIÓN DE LA CREACIÓN DE CANALES Y CONTENIDOS PROPIOS

LA PLATAFORMA ofrece a sus suscriptores la posibilidad de crear canales e incluir contenidos propios a través del programa CREADORES, cuyas condiciones se recogen en la dirección web, así como en el Reglamento de CREADORES de la PLATAFORMA.

A través del programa CREADORES, EL/LA CLIENTE podrá crear canales e incorporar contenidos propios en los términos y condiciones que se recogen en el Reglamento de creadores de LA PLATAFORMA, que EL/LA CLIENTE manifiesta conocer, y que se incorpora como Anexo II de este contrato.

EL/LA CLIENTE podrá monetizar los canales y contenidos de creación propia en el caso de que se supere el número mínimo de suscriptores recogido en el Reglamento Anexo II, en cuyo caso LA PLATAFORMA permitirá habilitar los anuncios publicitarios y, en su caso, incluir su contenido en los servicios Premium adicionales de pago, en los términos y con las condiciones recogidas en el citado Reglamento.

En caso de monetización, LA PLATAFORMA abonará las tarifas establecidas en el Reglamento Anexo II, aplicando el porcentaje correspondiente en función de número de accesos, descargas o visualizaciones que están establecidos en las tarifas.

Los ingresos de EL/LA CLIENTE correspondiente al contenido de creadores, serán abonados en la cuenta asociada al creador abierta conforme a lo establecido en el Reglamento Anexo II.

CUARTA.- DURACIÓN

El contrato tendrá una duración de [PLAZO], el cual se prorrogará por igual plazo si ninguna de las partes manifiesta su voluntad en contrario.

No obstante lo anterior, EL/LA CLIENTE podrá darse de baja en la suscripción en cualquier momento conforme a lo estipulado en la cláusula segunda, en cuyo caso LA PLATAFORMA podrá suprimir los canales y contenidos propios creados por EL/LA CLIENTE.

QUINTA.- OBLIGACIONES DEL CLIENTE

EL/LA CLIENTE se compromete a hacer un uso diligente de la plataforma, así como de sus claves de acceso, obligándose a mantenerlas en secreto, y a no cederlas o facilitarlas a terceras personas.

EL/LA CLIENTE deberá comunicar a LA PLATAFORMA, la pérdida, robo o cualquier incidencia de las claves de acceso a efectos de que LA PLATAFORMA, las desactive e Inhabilite, y proporcionar, en su caso, una nueva clave a EL/LA CLIENTE, todo ello a fin de garantizar el correcto acceso a los datos e impedir accesos no autorizados.

En el caso de que EL/LA CLIENTE se incluya en el programa CREADORES, se obliga a respetar los contenidos, prohibiciones y límites establecidos en el Reglamento Anexo II.

SEXT A.- OBLIGACIONES DE LA DISTRIBUIDORA

La PLATAFORMA se obliga al cumplimiento del contrato con arreglo a las disposiciones legales que lo regulan, y en especial asume la obligación de gestionar diligentemente sus contenidos y ofrecer un servicio de acceso permanente a EL/LA CLIENTE, sustituyendo de forma inmediata los servicios que ofrece en caso de interrumpirse, suspenderse o extinguirse alguno de los servicios ofertados.

En caso de que EL/LA CLIENTE se incorpore al programa CREADORES, LA PLATAFORMA se obliga a gestionar diligentemente la explotación digital de canales y contenidos creados por EL/LA CLIENTE, y a comercializarla de forma eficaz en la plataforma, buscando su más amplia difusión conforme a los usos habituales.

SÉPTIMA.- CAUSAS DE RESOLUCIÓN ANTICIPADA

El incumplimiento por cualquiera de las partes de cualquiera de las obligaciones estipuladas, facultará a la parte contraria a resolver de forma inmediata el presente contrato o exigir su cumplimiento, sin perjuicio de la indemnización de daños y perjuicios que proceda en ambos casos.

Una vez que se produzca la baja de EL/LA CLIENTE en la PLATAFORMA se procederá la inhabilitación de sus claves de acceso, así como al tratamiento de cualquier tipo de Información de EL/LA CLIENTE de acuerdo a lo establecido en la normativa vigente de protección de datos, en los términos que se pactan en este contrato.

En el caso de que EL/LA CLIENTE se incluya en el programa CREADORES, se pacta como causa de resolución del contrato la vulneración de los contenidos, prohibiciones y límites establecidos en el Reglamento Anexo II, así como la infracción de los derechos de la propiedad intelectual o de terceros por parte del creador, lo cual facultará a LA PLATAFORMA a resolver el contrato, con la indemnización de daños y perjuicios que proceda.

OCTAVA.- CONFIDENCIALIDAD

Ambas partes se comprometen a no divulgar la información y documentación confidencial referente a la otra parte de la que hayan tenido conocimiento por razón de la ejecución del presente contrato, salvo las indispensables para su cumplimiento, y a mantenerla en secreto, incluso después de la finalización del mismo.

En especial, LA PLATAFORMA declara que toda la información que EL/LA CLIENTE le proporcione será tratada con la mayor confidencialidad, respetando las medidas de seguridad impuestas por la normativa vigente. Los datos del CLIENTE y los de terceros grabados en su software a los que pueda acceder LA PLATAFORMA, únicamente serán tratados por ésta para asegurar el cumplimiento del servicio contratado, declarando la PLATAFORMA que estos datos son confidenciales a todos los efectos y sujetos al más estricto secreto profesional incluso una vez finalizada la presente relación contractual.

NOVENA.- PROTECCIÓN DE DATOS.

Las partes se obligan a cumplir la normativa vigente en materia de protección de datos, en concreto, lo previsto en el Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016, relativo a la protección de las personas físicas en lo que respecta al tratamiento de datos personales y a la libre circulación de estos datos (Reglamento general de protección de datos) y Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales; o cualquier otra norma que pueda sustituirlas en el futuro; y consienten el tratamiento de sus datos personales por la contraparte para las finalidades relacionadas con el objeto del presente contrato,

En especial, LA PLATAFORMA declara que los datos personales facilitados por EL/LA CLIENTE son los datos de contacto necesarios para la eficacia de la relación contractual que se inicia con la aceptación de este contrato. El tratamiento de dichos datos de contacto se realizará conforme a la normativa vigente, por lo que LA PLATAFORMA, como responsable del tratamiento, gestionará, mediante el fichero “clientes”, los datos personales de contacto facilitados por EL/LA CLIENTE con la finalidad de gestionar los servicios pactados en este contrato.

DÉCIMA.- NOTIFICACIONES

Toda notificación que se efectúe entre las partes se hará preferentemente en las direcciones de correo electrónico que figuran en el encabezamiento, sin perjuicio de que también puedan ser realizadas en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de dirección de correo electrónico y/o de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

UNDÉCIMA.- SUMISIÓN A MEDIACIÓN Y/O ARBITRAJE

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación (en su caso se citará la institución) de [INSTITUCIÓN DE MEDIACIÓN], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y (caso de fijar un plazo máximo....) fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

(en su caso, pacto de arbitraje...) A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de [INSTITUCIÓN ARBITRAL], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato y sus Anexos I y II, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

Fdo.: Fdo.:

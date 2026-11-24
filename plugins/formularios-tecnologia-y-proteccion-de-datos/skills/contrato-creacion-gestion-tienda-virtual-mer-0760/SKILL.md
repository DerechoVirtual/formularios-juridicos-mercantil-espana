---
name: contrato-creacion-gestion-tienda-virtual-mer-0760
description: "Contrato de creación y gestión de tienda virtual. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de creación y gestión de tienda virtual

> Formulario **MER-0760** del plugin **Contratos tecnológicos, comercio electrónico y protección de datos** (`formularios-tecnologia-y-proteccion-de-datos`) · Mercantil › Tecnología, comercio electrónico y protección de datos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de creación y gestión de tienda virtual» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de creación y gestión de tienda virtual” para mi caso». También puedes invocarla directamente con `/formularios-tecnologia-y-proteccion-de-datos:contrato-creacion-gestion-tienda-virtual-mer-0760`.
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
- [ ] FECHA (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] PLAZO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN DEL SERVICIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MEDIOS DE PAGO
- [ ] MES
- [ ] SUCURSAL

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

CONTRATO DE TIENDA VIRTUAL

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS] mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL CLIENTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL PROVEEDOR", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE TIENDA VIRTUAL, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO: Que el CLIENTE está interesado en la contratación de los servicios de tienda virtual para ofrecer sus productos a través de Internet.

SEGUNDO: Que el PROVEEDOR es una empresa especializada en la prestación de servicios web.

TERCERO: Que las Partes reunidas en la sede social del CLIENTE, acuerdan celebrar el presente contrato de TIENDA VIRTUAL, en adelante el "Contrato", de acuerdo con las siguientes

CLÁUSULAS

Objeto

En virtud del Contrato el PROVEEDOR se obliga a prestar al CLIENTE los servicios de Tienda Virtual [DENOMINACIÓN DEL SERVICIO], en adelante "los Servicios", válido para crear y gestionar una tienda virtual en Internet a través de un conjunto de páginas web auto administrables con información gráfica o de texto, con un control exclusivo de quién lo administra, en los términos y condiciones previstos en el Contrato y en todos sus Anexos.

Términos y condiciones específicos de la prestación de los servicios

El PROVEEDOR prestará los Servicios en los siguientes términos y condiciones específicos:

2.1El PROVEEDOR proporcionará al CLIENTE el servicio de tienda virtual en el plazo de [PLAZO] a partir de la firma del presente contrato. Dicho servicio tiene las siguientes características técnicas:

2.2El PROVEEDOR licenciará el uso del servicio al CLIENTE. Dicha licencia es sin exclusiva y sin ceder ningún otro derecho sobre el servicio objeto de este contrato. La cesión del uso se realiza por tiempo determinado, el de vigencia del presente contrato.

2.3El PROVEEDOR podrá licenciar el uso del servicio a cualquier tercero, incluso a un competidor directo del CLIENTE. El PROVEEDOR se reservará el derecho a revocar la licencia de uso en caso de incumplimiento por el CLIENTE de sus obligaciones contractuales.

2.4El PROVEEDOR facilitará las claves y códigos necesarios para acceder al servicio. Dichas claves y códigos permiten la entrada al sistema de creación y gestión de la tienda virtual. El CLIENTE será el único responsable de la custodia de las claves y códigos del programa.

2.5El CLIENTE administrará el servicio y las páginas web del mismo a través de un sistema remoto. El control del sistema remoto lo tendrá el CLIENTE, a través de las claves y códigos suministrados, bajo su exclusiva responsabilidad.

2.6Con la entrega del servicio también se entrega el manual del usuario, que contiene las reglas de utilización del mismo.

2.7El PROVEEDOR realizará un curso de capacitación para que el CLIENTE, o para quién el designe, conozca como utilizar el servicio.

2.8El PROVEEDOR facilitará al CLIENTE un servicio de hosting con un servidor web para el alojamiento de la tienda virtual. El servidor será "seguro" y ofrecerá toda la seguridad necesaria para la transmisión de los datos de la venta on line. El espacio de memoria del alojamiento será suficiente para alojar el programa.

2.9Será por cuenta del CLIENTE la obtención del nombre de dominio y su mantenimiento.

2.10El PROVEEDOR configurará el servicio y lo pondrá en funcionamiento.

2.11El CLIENTE ofrecerá sus productos a los visitantes de la Tienda Virtual y realizará las ventas on line, de esos productos, en su propio nombre, por su cuenta y riesgo, asumiendo todas las obligaciones y responsabilidades que le imponga la legislación aplicable a la venta en general y a la venta on line en especial.

2.12El CLIENTE se obliga a publicar en la tienda virtual las condiciones de contratación de la venta de los productos ofrecidos. De tal forma, que los posibles compradores tengan conocimiento de las mismas antes de realizar la compra on line.

2.13El CLIENTE declara que los Productos ofrecidos en la tienda virtual son de producción, uso y comercialización conforme a la legislación vigente y respetan cualesquiera derechos de terceras personas.

2.14El CLENTE asumirá la garantía de los productos vendidos a través de la tienda virtual.

2.15El CLIENTE determinará los posibles medios de pago respecto a terceros compradores de la tienda virtual. Los medios de pago podrán ser los utilizados usualmente en este tipo de transacciones comerciales, esto es, [MEDIOS DE PAGO]. De los posibles medios de pago el CLIENTE deberá determinar uno, como opción de pago por defecto.

2.16El PROVEEDOR garantiza el servicio por un período de [PLAZO]

2.17El PROVEEDOR comunicará al CLIENTE cambios o implementaciones del servicio, por si fuesen de su interés.

Política de uso

El CLIENTE es el único responsable de determinar si los servicios que constituyen el objeto de este Contrato se ajustan a sus necesidades, por lo que el PROVEEDOR no garantiza que los servicios contratados se ajuste a las necesidades específicas del CLIENTE.

[ELEGIR UNA OPCIÓN: Precio y forma de pago / Pago no aplazado / Pago aplazado]

Calidad de los servicios prestados

El PROVEEDOR responderá de la calidad del trabajo desarrollado con la diligencia exigible a una empresa experta en la realización de los trabajos objeto del Contrato. El PROVEEDOR se obliga a gestionar y obtener, a su cargo, todas las licencias, permisos y autorizaciones administrativas que pudieren ser necesarias para la realización de los Servicios.

Formación

EL PROVEEDOR se obliga a prestar al personal del CLIENTE la formación precisa para la correcta y óptima utilización del programa. La duración del proceso de formación será de

El pago se efectuará el día [FECHA] en la cuenta corriente nº [NÚMERO] que EL PROVEEDOR tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL]

El precio incluye los gastos de desplazamiento que en su caso deba efectuar el personal del PROVEEDOR a las oficinas del CLIENTE así como el valor de los materiales que, en su caso, se les proporcione durante el tiempo que duren las reparaciones.

Confidencialidad

El PROVEEDOR guardará confidencialidad sobre la información que le facilite el CLIENTE en o para la ejecución del Contrato o que por su propia naturaleza deba ser tratada como tal. Se excluye de la categoría de información confidencial toda aquella información que sea divulgada por el CLIENTE, aquella que haya de ser revelada de acuerdo con las leyes o con una resolución judicial o acto de autoridad competente. Este deber se mantendrá durante un plazo de tres años a contar desde la finalización del servicio.

Protección de datos

En el caso de que la prestación de los Servicios suponga la necesidad de acceder a datos de carácter personal, el PROVEEDOR, como encargado del tratamiento, queda obligado al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable. El PROVEEDOR responderá, por tanto, de las infracciones en que pudiera incurrir en el caso de que destine los datos personales a otra finalidad, los comunique a un tercero, o en general, los utilice de forma irregular, así como cuando no adopte las medidas correspondientes para el almacenamiento y custodia de los mismos. A tal efecto, se obliga a indemnizar al CLIENTE, por cualesquiera daños y perjuicios que sufra directamente, o por toda reclamación, acción o procedimiento, que traiga su causa de un incumplimiento o cumplimiento defectuoso por parte del PROVEEDOR de lo dispuesto tanto en el Contrato como lo dispuesto en la normativa reguladora de la protección de datos de carácter personal.

A los efectos de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales, el PROVEEDOR únicamente tratará los datos de carácter personal a los que tenga acceso conforme a las instrucciones del CLIENTE y no los aplicará o utilizará con un fin distinto al objeto del Contrato, ni los comunicará, ni siquiera para su conservación, a otras personas. En el caso de que el PROVEEDOR destine los datos a otra finalidad, los comunique o los utilice incumpliendo las estipulaciones del Contrato, será considerado también responsable del tratamiento, respondiendo de las infracciones en que hubiera incurrido personalmente.

El PROVEEDOR deberá adoptar las medidas de índole técnica y organizativas necesarias que garanticen la seguridad de los datos de carácter personal y eviten su alteración, pérdida, tratamiento o acceso no autorizado, habida cuenta del estado de la tecnología, la naturaleza de los datos almacenados y los riesgos a que están expuestos, ya provengan de la acción humana o del medio físico o natural. A estos efectos el PROVEEDOR deberá aplicar las medidas técnicas y organizativas apropiadas para garantizar un nivel de seguridad adecuado al riesgo, conforme al artículo 32 del Reglamento (UE) 2016/679 (RGPD).

Responsabilidades

El PROVEEDOR responderá de la corrección y precisión de los documentos que aporte al CLIENTE en ejecución del Contrato y avisará sin dilación al CLIENTE cuando detecte un error para que pueda adoptar las medidas y acciones correctoras que estime oportunas.

El PROVEEDOR responderá de los daños y perjuicios que se deriven para el CLIENTE y de las reclamaciones que pueda realizar un tercero, y que tengan su causa directa en errores del PROVEEDOR, o de su personal, en la ejecución del Contrato o que deriven de la falta de diligencia referida anteriormente.

Las obligaciones establecidas para el PROVEEDOR por la presente cláusula serán también de obligado cumplimiento para sus posibles empleados, colaboradores, tanto externos como internos, y subcontratistas, por lo que el PROVEEDOR responderá frente al CLIENTE si tales obligaciones son incumplidas por tales empleados.

Duración del contrato

El plazo de duración del presente Contrato es de [PLAZO] a partir de la fecha referida en el encabezamiento del Contrato. El Contrato podrá ser prorrogado expresamente y por escrito.

[ELEGIR UNA OPCIÓN: Acuerdo de nivel de servicio / Con cláusula penal / Opción 11.1Con cláusula penal / Sin cláusula penal / Opción 11.2Sin cláusula penal]

Pacto de no contratación

El CLIENTE se compromete a no contratar a persona alguna de las que prestan sus servicios para EL PROVEEDOR. La presente cláusula extenderá su vigencia incluso con posterioridad a la extinción del presente contrato por un período de [Nº] años.

En caso de incumplimiento del presente acuerdo, EL CLIENTE estará obligado a indemnizar al PROVEEDOR con la cantidad de [IMPORTE] euros.

Resolución

El Contrato podrá resolverse por las siguientes causas:

1.Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2.Por acuerdo de las Partes por escrito.

3.La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de … días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sin cláusula penal / Sumisión a tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal / Sumisión a tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Suministro a arbitraje / Sin cláusula penal / Sumisión a Arbitraje sin cláusula penal en caso de no ejecución voluntaria del laudo / Coin cláusula penal / Sumisión a Arbitraje con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE TIENDA VIRTUAL, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(El Cliente)

Fdo. Don [NOMBRE Y APELLIDOS]

(El Proveedor)

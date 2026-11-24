---
name: contrato-organizacion-concierto-mer-0612
description: "Contrato de organización de un concierto. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de organización de un concierto

> Formulario **MER-0612** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de organización de un concierto» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de organización de un concierto” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-organizacion-concierto-mer-0612`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL NOTARIO (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE PASES O ENTRADAS

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

D [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A] en lo sucesivo "La Compañía", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS DEL NOTARIO] en fecha [FECHA] con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS] en nombre y representación de en lo sucesivo "La Promotora", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS DEL NOTARIO] en fecha [FECHA] con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE ORGANIZACIÓN DE CONCIERTO, y a tal efecto, libremente y de común acuerdo,

EXPONEN

Que La Compañía es una persona jurídica de derecho privado dedicada a la organización y producción de eventos musicales.

Que La Promotora es una persona jurídica dedicada la promoción internacional de conciertos

Que ambas partes de común acuerdo llevan a efecto el presenten contrato con arreglo a las siguientes:

CLÁUSULAS

Permisos

La Compañía se compromete a obtener cuantas licencias, certificados y permisos sean necesarios para la realización del evento musical.

A tal fin, la Promotora deberá proporcionar a la Compañía la documentación necesaria para la obtención de los permisos.

Objeto

Supuesta la obtención de la licencia, la Compañía deberá dejar disponible aquellas áreas del Estadio necesarias para la preparación y presentación del evento. Y todo ello de conformidad con la planificación horaria que se adjunta como Anexo I.

La Promotora organizará y celebrará el Concierto en el Estadio en las fechas previstas. Esto es, inicialmente el [FECHA] o, en caso de que el evento fuera aplazado, dentro de los márgenes temporales concedidos por la Autoridad que concede la licencia.

Obligaciones de la compañía

Serán de cuenta y cargo de la Compañía:

a) El control de las pantallas y marcadores si así lo requiere la Promotora al final del Estadio, así como la emisión de mensajes de emergencia y/o seguridad. La publicación de cualquier otra información sólo estará permitida cuando no haya actuación alguna en el escenario

b)La limpieza del Estadio.

c)El control de los medios de comunicación local.

d) El acondicionamiento y protección del césped y de todas las zonas de paso.

e) La celebración de los acuerdos de aparcamiento requeridos para la obtención de la licencia.

Obligaciones adicionales de la Compañía

La Compañía proporcionará, si así fuera necesario, y siempre a su propia cuenta y cargo:

a) El uso de los equipos de sonido existentes

b) El personal de taquilla

c) Personal y material de primeros auxilios, servicios de ambulancias, bomberos y los médicos requeridos para la obtención de las licencias

d) Electricistas para la iluminación y el control del sonido del Estadio

e) Suministro de agua y/o calefactores

f) Las modificaciones necesarias en el vallado y zona de acceso

Obligaciones de la Promotora

La Promotora se compromete a producir y presentar el Evento. Esta obligación incluye la asunción de los siguientes costes económicos:

a) El del caché de los Artistas, cuyo pago puntual asume la Promotora

b) El del alojamiento y manutención de los Artistas

c) El del alquiler de la maquinaria necesaria para el montaje y desmontaje del escenario

d) El del personal de seguridad asociado a la producción el evento adicional al mencionado en la estipulación 5.r)

e) El de los consumos de energía necesarios dentro del Estadio

f) El de proporcionar los escenarios y equipamientos necesarios para la celebración del evento

g) El de proporcionar e instalar una mezcladora de sonido Que deberán ser ubicadas en un lugar mutuamente consentido por las Partes, sujeto siempre a la aprobación de las autoridades que conceden las licencias.

h) El de la iluminación y sonidos necesarios para la celebración del evento y que no hayan sido especificado en otros apartados

i) El de los baños y fuentes necesarios de conformidad con la normativa que regula la concesión de las licencias, permisos y certificados

j) El de las oficinas de producción temporales y servicios adicionales de apoyo requeridos por la Promotora

k) El de cualquier servicio adicional a los reflejados en esta estipulación requeridos de conformidad con la normativa de aplicación a la celebración de este tipo de eventos, siempre que la Promotora haya prestado con carácter previo su conformidad con el mismo

l) El de la publicidad del evento

m) El de cualquier canon o impuesto relacionado con la celebración del evento

n) El de los servicios de seguridad ciudadana y policía

o) El de la impresión de las entradas

p) El de los servicios de consultoría acústica mencionados en la estipulación 11

q) El de los derechos de autor exigidos por la S.G.A.E.

r) El de la señalización específicamente empleada para el evento

s) El de cualquier licencia necesaria para la celebración del espectáculo

Obligaciones adicionales de la Promotora

La Promotora igualmente se compromete a:

a) De conformidad con lo preceptuado en la estipulación segunda, asegurar que el espectáculo no finalizará más tarde de la hora estipulada para la concesión de las licencias

b) No vender o entregar entradas o pases que excedan la capacidad de 51.252 personas, o el número máximo de personas estipulado para la concesión de las licencias

c) Entregar a la Compañía [Nº DE PASES O ENTRADAS] pases o entradas gratuitas

d) Adoptar las medidas necesarias para asegurar que el evento cumple con todas las formalidades y condiciones exigidas para la concesión de las licencias

e) No incluir o hacer nada durante el contrato que menoscabe o dañe los intereses o reputación de la Compañía

Cumplimiento de exigencias legales

Así mismo, la Promotora se compromete a observar y cumplir todas las exigencias legales relacionadas con cualquier aspecto de la preparación, producción y celebración del evento.

Introducción de objetos y equipos en el estadio

Todos las propiedades y pertenencias (incluidos los equipos de iluminación adicionales) que la Promotora o cualquier persona autorizada pretenda introducir en el estadio deberán ser previamente autorizadas por la Compañía. En todo caso, esta última se compromete a asegurar que tales pertenencias cumplen con las exigencias y formalidades exigidas por la regulación administrativa aplicable.

La Promotora se compromete a retirar todos los equipos de su propiedad del Estadio antes del [FECHA]

Merchandising

La Compañía se compromete a informar a los Artistas que intervienen en el Concierto, así como a cualquier persona autorizada por ellos para vender los objetos de merchandising pertinentes de los stands habilitados para ello dentro del Estadio, debiendo éstos últimos ajustarse a las directrices proporcionadas por la Compañía.

La Compañía recibirá el 5% de los ingresos obtenidos con la venta de tales objetos, una vez deducidos los impuestos y comisiones aplicadas por las entidades bancarias como consecuencia del uso de tarjetas de crédito.

Los stands introducidos en el Estadio serán construidos y levantados de conformidad con las especificaciones razonada y justificadamente dadas por la Compañía, y deberán cumplir con las exigencias legales y administrativas aplicables.

La venta de bebidas y consumibles en estos stands estará totalmente prohibida.

Publicidad

La publicidad dentro del Estadio o en cualquier elemento propiedad de la Compañía deberá ser previamente autorizada por escrito por ésta. Si la emisión o empleo de cualquier tipo de publicidad supone el desembolso de alguna cantidad por parte de la Compañía, la misma será de cuenta y cargo de la Promotora.

Control de las condiciones impuestas para la concesión de las licencias.

Dado que para la promoción, producción y realización del Evento la Compañía está obligada a cumplir con las condiciones impuestas por la Autoridad concedente de las licencias, la Promotora se compromete a cumplir con todas las especificaciones dadas por la Compañía que tengan por objeto, tanto mantener el orden durante la celebración del Evento, como cumplir con las condiciones exigidas para la concesión y mantenimiento de las licencias.

En este sentido, la Promotora se compromete a realizar todos los esfuerzos necesarios para garantizar que los niveles de sonido se mantienen dentro de los límites autorizados por la licencia. Estos límites podrán elevarse como consecuencia del "sound propagation test" (que toma en consideración las condiciones meteorológicas existentes) realizados por los consultores acústicos de la Compañía en cada uno de los ensayos previos a la realización del Evento.

El nivel de sonido Laeq será controlado desde la posición de mezclado durante la duración de los ensayos y durante la celebración del Evento. Si el límite máximo de sonido fuera sobrepasado, los ingenieros de sonido reducirán los niveles de sonido a los márgenes permitidos. Si a pesar de todo, el nivel máximo de sonido es excedido hasta el punto de generar responsabilidades legales y/o administrativas, la Compañía quedará exenta de toda responsabilidad, siendo de cuenta y cargo de la Promotora el pago de cuantas multas o penas fueran impuestas como consecuencia de su acción y/o omisión negligente, así como los honorarios profesionales que razonablemente se deriven de la misma.

La Promotora se compromete a informar a los Artistas y al personal técnico y de producción de los derechos y obligaciones impuestos por las Autoridades concedentes de las licencias, así como de la necesidad de ajustarse a las exigencias legales y administrativas que vienen impuestas por éstas.

Todo los poderes concedidos para la organización, producción y realización del Evento estarán sujetos a la supervisión de los representantes de la Compañía.

Cesión del personal

La Compañía se compromete a, si la Promotora así lo solicita y siempre y cuando las restantes obligaciones asumidas en el presente contrato se lo permitan, proporcionar a esta ultima los servicios de personal que precise para colaborar en las tareas de montaje y desmontaje, así como de cualquier otro tipo relacionados con la organización, presentación y celebración del Evento.

En este caso, serán de cuenta y cargo de la Promotora los gastos que tales servicios generen, siempre y cuando hayan sido notificados y consentidos por ambas Partes con carácter previo a su realización.

Precio de las entradas

El precio de las entradas para el Evento será fijado por la Promotora y por [DENOMINACIÓN SOCIAL] compañía que presta los servicios de ticketing y promoción.

Zonas exclusivas

Las zonas señaladas en el Anexo II serán de uso exclusivo de la Compañía.

Folletos

La Promotora se compromete a realizar los programas y folletos del Evento que serán vendidos en los stands definidos en la Estipulación Novena, estando sujetos a los mismos términos y condiciones de venta allí expuestos.

Zonas de aparcamiento

La Compañía proporcionará y acondicionará zonas de aparcamiento para las personas que asistan al Evento. Los ingresos que con ello se obtengan pertenecerán a la Compañía, quien de una parte asume toda responsabilidad por este concepto y, de otra, tiene plena libertad para fijar el número de plazas disponible así como el coste de las mismas.

La Promotora tiene derecho a recibir, libre de cargo y coste, el uso de doscientas plazas de aparcamiento para su servicio particular, así como para el de los Artistas.

Bebidas y demás comsumibles

La Compañía proporcionará bebidas y demás consumibles. Todos los beneficios percibidos por este concepto pertenecerán a la Compañía. Esto no obstante, los puntos de venta serán mutuamente acordados por las Partes y deberán cumplir con las exigencias legales y/o administrativas oportunas.

Fotografías

Si se alcanzara un acuerdo o se hubiera recibido el consentimiento de los Artistas para ello, la Compañía tendrá derecho, previa consulta a la Promotora, a tomar fotografías durante el Evento, siempre sujeta a las mismas restricciones impuestas a la Promotora.

Grabación y retransmisión del evento

La grabación y retransmisión radiotelevisiva del Evento, así como la producción de cualquier video u otro tipo de grabación será regulada en un acuerdo separado entre las Partes Relevantes.

Precio

a) La Promotora deberá abonar a la Compañía en concepto de alquiler del Estadio, la cantidad de ( €), I.V.A. no incluido. Esta cantidad será entregada a la Compañía en el momento de la firma del presente contrato.

b) La Promotora deberá concertar una póliza de seguro que cubra el riesgo de cancelación o no producción del Evento, así como la responsabilidad civil derivada de la realización el Evento.

c) Si la Autoridad concedente de las licencias denegare la concesión de las mismas, este contrato se ajustará a lo establecido en el apartado d) de esta Estipulación. Del mismo modo, las Partes renuncian a reclamarse recíprocamente cualquier tipo de daños producidos por este concepto, debiendo la Compañía devolver a la Promotora las cantidades que le hubiesen sido entregadas.

d) Si el Evento no llegara a tener lugar como consecuencia de cualquier incumplimiento doloso o negligente imputable a la Promotora, la Compañía tendrá derecho a recibir de aquélla la suma total estipulada en el apartado 20 a) en concepto de alquiler del Estadio. Este caso, además, serán de cuenta y cargo de la Promotora la totalidad de los gastos en que la Compañía hubiera incurrido.

e) Si el Evento no llegara a concluir en la hora establecida, la Promotora liberará a la Compañía y a su personal de toda responsabilidad legal o administrativa, indemnizándola además por los gastos y honorarios profesionales en que hubiera incurrido como consecuencia de su acción u omisión dolosa o negligente.

Diseño de los folletos publicitarios

Siempre que fuera razonablemente posible, la Promotora presentará a la Compañía el diseño y composición de los programas (incluidos anuncios) así como de todo el material publicitario (incluido el insertado en periódicos y revistas) en que, de alguna manera, se aluda a la Compañía para su previa aprobación, que no podrá ser arbitraria e injustificadamente denegada o retrasada.

La Promotora se compromete igualmente a entregar, junto con los programas, una referencia a los procedimientos de evacuación de emergencia en los términos exigidos por la Autoridad concedente de las licencias. Esta información podrá entregarse en forma de folleto adicional.

Impuestos

El I.V.A. incrementará todas las cantidades que deban ser abonadas por la Promotora a la Compañía, incluidas las sumas estipuladas en el Apartado 20.a).

Régimen de responsabilidades

a) La Promotora liberará a la Compañía de toda responsabilidad por pérdidas y/o daños materiales y/o personales en que hubiera incurrido como consecuencia de la acción u omisión dolosa o negligente de la Promotora, de cualquiera de sus empleados o de cualquiera de los Artistas que participan en el Evento, indemnizándola por los gastos legales y profesionales en que hubiera podido incurrir como consecuencia de ello.

b) La Promotora deberá concertar una póliza de seguro no inferior a [IMPORTE] contra las pérdidas y/o daños materiales y/o personales causados en los bienes, equipo, agentes y/o trabajadores de la Compañía como consecuencia de la acción u omisión dolosa o negligente de la Promotora.

c) La Promotora se compromete a compensar a la Compañía.

d) La Compañía liberará a la Promotora de toda responsabilidad por pérdidas y/o daños materiales y/o personales en que hubiera incurrido como consecuencia de la acción u omisión dolosa o negligente de la Compañía o de cualquiera de sus empleados, indemnizándola por los gastos legales y profesionales en que hubiera podido incurrir como consecuencia de ello.

Causas de exoneración de la responsabilidad

Será causa de exoneración de la responsabilidad de cualquiera de las Partes, el incumplimiento de cualquiera de sus obligaciones como consecuencia de fuerza mayor, incluidas la huelga, guerra civil, terrorismo o interrupción general de los servicios de agua y/o electricidad.

Seguridad e higiene

Ambas Partes reconocen sus respectivas obligaciones impuestas por la legislación vigente en el ámbito de la seguridad e higiene. Para un mejor conocimiento de las mismas, la Compañía a provisto a la Promotora con una copia de las normas aplicables en esta materia.

Obligación legal de retención sobre las percepciones económicas

Si así fuera preciso, la Compañía deberá retener de los ingresos obtenidos por la venta de las entradas las cantidades incluidas en la Schedule Eleven Finance Act 1986.

Elección de ley

Las Partes designan la ley española como aplicable a los conflictos y litigios que eventualmente pudieran surgir como consecuencia de la interpretación y/o aplicación del presente contrato.

Sumisión a arbitraje

Antes de recurrir a procedimientos judiciales, las partes intentarán llegar a un acuerdo que permita resolver sus diferencias.

En cualquier caso, cuando fallen las negociaciones o, en todo caso, 10 días hábiles después de que éstas se han iniciado, las Partes se someterán al arbitraje de Derecho de un profesional designado de común acuerdo por ellas. Si no llegaran a un acuerdo, será el Presidente del Ilustre Colegio de Abogados de la Región el que lo designe. El coste del Experto será asumido por la Parte que el Experto designe. Cada una de ellas será responsable de sus propios gastos. Ambas Partes se reservan el derecho de acudir a los tribunales españoles cuando la vía expuesta anteriormente no sea viable.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

========================================================================

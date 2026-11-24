---
name: contrato-produccion-obra-encargo-mer-0740
description: "Contrato de producción de una obra por encargo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de producción de una obra por encargo

> Formulario **MER-0740** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de producción de una obra por encargo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de producción de una obra por encargo” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-produccion-obra-encargo-mer-0740`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] Nº (5 veces)
- [ ] FECHA (3 veces)
- [ ] AÑO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] TÍTULO DE LA OBRA (2 veces)
- [ ] FORMATO DE IMAGEN
- [ ] FORMATO DE PELÍCULA (MM)
- [ ] IMPORTE
- [ ] IMÁGENES POR SEGUNDO
- [ ] LUGAR
- [ ] TIPO DE CÁMARAS

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

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA PRODUCTORA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL DIRECTOR", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE PRODUCCIÓN DE OBRA, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que LA PRODUCTORA tiene en proyecto la producción bajo su iniciativa de una obra audiovisual (documental) titulada [TÍTULO DE LA OBRA] con una duración aproximada de [Nº] minutos.

SEGUNDO.- Que EL DIRECTOR está interesado en dirigir el proyecto mencionado en el anterior Exponendo.

TERCERO.- Que en vista de lo anterior, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

Constituye el objeto del presente contrato la producción por parte de LA PRODUCTORA de la obra [TÍTULO DE LA OBRA] descrita en el Exponiendo Primero rodada en [FORMATO DE PELÍCULA (MM)] mm color, formato [FORMATO DE IMAGEN] a [IMÁGENES POR SEGUNDO] imágenes por segundo y de acuerdo con las condiciones y especificaciones artísticas y técnicas acordadas en el presente contrato.

[ELEGIR UNA OPCIÓN: Contraprestación / Cantidad fija / Cantidad variable / — y además elegir: Pago / Cantidad fija / Cantidad variable]

Plan de rodaje

El inicio de la grabación de la obra audiovisual comenzará el día [DÍA] de [MES] de [AÑO] calculándose de forma provisional una duración total aproximada de [Nº] semanas/meses.

Coste de producción

El coste de producción, según diseño que se presentará a los organismos oficiales correspondientes, queda fijado en la cantidad de [IMPORTE] euros, incluyendo copias y publicidad de lanzamiento.

El coste de producción se asume íntegramente por LA PRODUCTORA.

Obligaciones de la productora

Remuneración

L A PRODUCTORA se compromete a satisfacer al DIRECTOR la remuneración establecida en la Clausula Segunda.

Material audiovisual

LA PRODUCTORA facilitará al DIRECTOR, con cargo a los gastos directamente imputables a la producción del documental:

- monitores de T.V.

- cámaras tipo [TIPO DE CÁMARAS].

Libertad de creación:

LA PRODUCTORA garantiza al DIRECTOR la más absoluta libertad de creación en el desempeño de su cometido, así como la no introducción de variaciones en la versión definitiva.

Derecho moral:

El PRODUCTOR se compromete a ejercitar los derechos de explotación conforme a los buenos usos y con estricto respecto en todo caso del Derecho moral del DIRECTOR-REALIZADOR.

Publicidad de la obra

LA PRODUCTORA se obliga a citar al DIRECTOR en toda la publicidad que realice de la obra.

Seguros

LA PRODUCTORA contratará con una o varias compañías de seguros las siguientes pólizas:

a) Póliza de seguro de accidentes e invalidez permanente de los protagonistas y el director;

b) Póliza de seguro de responsabilidad civil (que incluya siniestro sobre mobiliario, accesorios, material técnico de rodaje); y

c) Póliza de seguro de buen fin del documental, cuya beneficiaria serán la propia PRODUCTORA.

Los seguros deberán cubrir íntegramente el coste del documental y serán mantenidos en vigor hasta que la copia standard del mismo sea entregada.

Obligaciones del director

Dirección-realización de la obra

El DIRECTOR se compromete a hacerse cargo por sí mismo de la dirección-realización de la obra audiovisual, así como a supervisar y coordinar las aportaciones de los restantes coautores y guionistas, a lo largo de todo el proceso de realización hasta la entrega de la versión definitiva a LA PRODUCTORA.

Respeto de los límites presupuestarios

EL DIRECTOR se compromete a realizar los servicios descritos dentro de los límites presupuestarios establecidos, y a cumplir con los plazos de entrega y de realización establecidos, colaborando con LA PRODUCTORA para lograr el buen fin de la obra audiovisual.

Disponibilidad

EL DIRECTOR se compromete a estar a disposición de LA PRODUCTORA durante el período de preproducción, montaje, edición, y en general a lo largo de toda la producción de la obra audiovisual, y a participar en todos los actos promocionales de la obra, siempre y cuando le sea posible acudir y no obstaculice el desarrollo del desempeño de su puesto de trabajo habitual. No obstante, LA PRODUCTORA deberá comunicar con antelación de [Nº] días toda la información relativa a los actos de que se trate, y a respetar los compromisos y decisiones al respecto que pueda asumir el DIRECTOR.

Entrega de la Obra

EL DIRECTOR se comprometa a entregar a LA PRODUCTORA una copia de la obra audiovisual terminada en formato DVD con caja DVD-Pack, carátula a color y serigrafía de la galleta en el DVD, fijándose como fecha máxima la del día [FECHA] salvo causas de fuerza mayor.

DIRECTOR se encargará de la maquetación de la portada de la caja del DVD, así como de la galleta del DVD y su posterior grabación utilizando para ello los medios necesarios.

Cesión de derechos de propiedad intelectual

EL DIRECTOR cede en exclusiva a LA PRODUCTORA sus derechos de reproducción, distribución y comunicación pública sobre la obra en todo el universo, incluyendo España, por todos los medios, formatos y procedimientos conocidos y por conocer, y con duración de los mencionados derechos de por vida.

Alcance y condiciones con respecto de sistemas de inteligencia artificial

Las Partes acuerdan que las cesiones efectuadas en los anteriores apartados se realizan sin la facultad de emplear los derechos cedidos para el entrenamiento, alimentación o aprendizaje automático de ningún sistema de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robóticos, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología disruptiva relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). De tal manera que, el uso de los derechos cedidos por mor del presente Contrato para los enunciados usos constituirá un incumplimiento sustancial del mismo.

LA PRODUCTORA habrá de respetar el compromiso adquirido en virtud de la anterior Estipulación en los contratos, negocios y relaciones jurídicas que mantenga con terceros, sean personas físicas o jurídicas, adoptando todas las medidas necesarias a tal fin e incluyendo, si fuese necesario, previsiones escritas en los contratos que celebre con estos terceros.

Uso de la imagen del director-realizador

El DIRECTOR autoriza a LA PRODUCTORA el uso de su imagen personal, fotografía, retrato e imagen física, reproducida o generada por cualquier medio, su biografía, así como su expediente profesional, para fines de promoción, explotación y comercialización de la obra a que este contrato se refiere.

Financiación externa

EL DIRECTOR autoriza a LA PRODUCTORA a la presentación de su currículum ante cuantas instancias o instituciones sea necesario para la obtención de financiación de la obra.

Igualmente se obliga a colaborar en la redacción del Proyecto que en su caso se precise como documentación necesaria para la obtención de la citada financiación.

Versiones

La decisión acerca de la versión definitiva de la obra audiovisual será adoptada por LA PRODUCTORA y EL DIRECTOR de mutuo acuerdo, si bien, en caso de desacuerdo, decidirá

Queda expresamente prohibida toda modificación de la versión definitiva de la obra, sin previa autorización escrita del DIRECTOR y de LA PRODUCTORA.

Igualmente en la comunicación pública a través de la radiodifusión, se podrán realizar en la forma de emisión de la obra audiovisual, las modificaciones estrictamente exigidas por el medio de programación del medio de que se trate, sin perjuicio en todo caso del Derecho moral del DIRECTOR.

Uso fragmentario de la obra

El DIRECTOR autoriza la utilización de extractos, secuencias o fragmentos, imágenes, fotografías o elementos sonoros y de interpretación de la obra con fines estrictamente promocionales.

Resolución del contrato

El Contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2. Por acuerdo de las Partes por escrito.

3. La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

La resolución del contrato por esta causa producirá los mismos efectos que el incumplimiento de la obligación de pago en lo que a recuperación de la maquinaria e indemnización de los daños y perjuicios respecta.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de EL DIRECTOR.

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Jurisdicción competente y ley aplicable

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, la competencia de los Tribunales que deban conocer del asunto se determinará de conformidad con los criterios de competencia objetiva, funcional y territorial legalmente aplicables.

El presente contrato tiene carácter mercantil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE PRODUCCIÓN DE OBRA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo. Don [NOMBRE Y APELLIDOS]

(LA PRODUCTORA)

Fdo. Don [NOMBRE Y APELLIDOS]

(EL DIRECTOR)

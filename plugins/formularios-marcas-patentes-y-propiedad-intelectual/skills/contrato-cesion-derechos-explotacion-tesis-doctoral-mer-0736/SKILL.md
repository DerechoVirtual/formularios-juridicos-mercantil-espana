---
name: contrato-cesion-derechos-explotacion-tesis-doctoral-mer-0736
description: "Contrato de cesión de los derechos de explotación de una tesis doctoral. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cesión de los derechos de explotación de una tesis doctoral

> Formulario **MER-0736** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cesión de los derechos de explotación de una tesis doctoral» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cesión de los derechos de explotación de una tesis doctoral” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-cesion-derechos-explotacion-tesis-doctoral-mer-0736`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº

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

CONTRATO DE CESIÓN DE DERECHOS DE TESIS DOCTORAL

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE CESIÓN DE DERECHOS DE TESIS DOCTORAL, y a tal efecto, libremente y de común acuerdo,

EXPONEN

I. Que el AUTOR es el único y exclusivo titular de los derechos de explotación de la Tesis Doctoral denominada "", (a partir de ahora "Tesis Doctoral"), a través de cualquier medio, y en particular, a través de Internet u otro canal o destino de la información que sea susceptible de adscripción en Internet, también a través de la televisión digital, cable o cualquier otra plataforma o forma de transmisión de datos tecnológica (como por ejemplo, ondas hercianas, transmisión telemática o transmisión por fibra óptica).

II. El Autor garantiza que es el titular de los derechos de propiedad intelectual, objeto del presente Contrato, en relación con la Tesis Doctoral y que, en consecuencia, está en plenas facultades para suscribir con la UNIVERSIDAD el presente Contrato, y que lo establecido en este documento no infringe ningún derecho de terceros, sea la propiedad industrial, intelectual, secreto comercial o cualquier otro.

El autor garantiza que en la elaboración de la Obra y en todos los materiales relacionados con la misma, no ha hecho uso, empleado o se ha ayudado de sistemas de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robóticos, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). Dicho compromiso podrá ser levantado previa conformidad de las partes por escrito cuando el uso de dicha tecnología sea testimonial.

III. Ambas partes están interesadas en suscribir un contrato que regulará la cesión por parte del Autor a la UNIVERSIDAD de los derechos de transformación, reproducción, y comunicación pública de la Tesis Doctoral únicamente para los usos que se especifican en el mismo, todo ello de acuerdo con las siguientes:

CLÁUSULAS

Objeto

El Autor cede a la UNIVERSIDAD durante el periodo de vigencia del presente Contrato, con carácter gratuito y con fines exclusivamente de investigación y docencia, los derechos de transformación, reproducción y comunicación pública, de la Tesis Doctoral, únicamente para:

1. Transformar o adaptar la Tesis Doctoral, sea directamente o a travésde terceros, cuando esto se considere necesario para adecuarla al formato, imagen o apariencia de Internet o cualquier otra tecnología susceptible de adscripción en Internet; así como incorporar cualquier otro sistema de seguridad en el formato electrónico de la Tesis Doctoral, correspondiendo al Autor la facultad de supervisar la adaptación a fin de que no se desnaturalice el contenido o sentido de su obra.

2. Reproducir la Tesis Doctoral, de forma total o parcial, en un soporte digital para su incorporación en una base de datos electrónica, comprendido el derecho a almacenar la Tesis Doctoral en centros servidores, así como el derecho a realizar cualquier otra reproducción temporal necesaria para permitir a los usuarios la visualización, reproducción o grabación en el disco duro del PC o en soporte papel de la Tesis Doctoral, para su uso privado y/o con fines de estudio e investigación.

3. La comunicación pública o puesta a disposición, total o parcial, de la Tesis Doctoral, en la modalidad de demanda o a la carta, a través de cualquier canal alámbrico o inalámbrico, o dirigido a cualquier destino de la información que sea susceptible de adscripción en Internet (por ejemplo, la telefonía móvil - protocolo WAP "Wireless Access Protocol"- o UMTS o otros medios análogos, como los medios televisivos y de radiodifusión con la televisión digital o por cable cuando sea difundida a través de Internet).

4. Las Partes acuerdan que las cesiones efectuadas en los anteriores apartados se realizan sin la facultad de emplear los derechos cedidos para el entrenamiento, alimentación o aprendizaje automático de ningún sistema de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robóticos, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología disruptiva relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). De tal manera que, el uso de los derechos cedidos por mor del presente Contrato para los enunciados usos constituirá un incumplimiento sustancial del mismo.

La UNIVERSIDAD habrá de respetar el compromiso adquirido en virtud de la anterior Estipulación en los contratos, negocios y relaciones jurídicas que mantenga con terceros, sean personas físicas o jurídicas, adoptando todas las medidas necesarias a tal fin e incluyendo, si fuese necesario, previsiones escritas en los contratos que celebre con estos terceros.

Para hacer efectiva la cesión de los derechos establecidos en la cláusula 1.1, el Autor entregará a la UNIVERSIDAD, en soporte electrónico o papel, en la forma la siguiente documentación:

1. Un documento en el que consten los datos necesarios para la identificación de la Tesis Doctoral, según el modelo que figura en el Anexo I

2. Un ejemplar completo de la Tesis Doctoral, en formato digital, de acuerdo con las especificaciones técnicas descritas en el Anexo II. El autor se compromete -si fuera necesario- a facilitar una descripción del software y aplicaciones usados para crear el documento digital, incluyendo una lista de los ficheros y el tamaño de los mismos, así como copia de las licencias de uso del software de terceros, que será reproducido, distribuido y usado con la tesis y permiso por escrito para distribuir software de terceros. En el caso de incluir otras aplicaciones (video clip, registros sonoros, videos, aplicaciones multimedia, etc.) el autor garantiza haber obtenido todos los permisos para que la UNIVERSIDAD reproduzca y distribuya cualquier software de terceros necesarios para acceder, visualizar o imprimir dicha tesis. Si los mencionados permisos no están suficientemente garantizados, la UNIVERSIDAD se reserva el derecho de rechazar la publicación de la tesis.

3. Cuando la tesis que se desea incorporar hubiera sido leída y aprobada en un curso académico anterior al de la fecha de la firma de este Contrato, el Autor deberá hacer constar por escrito, bajo su exclusiva responsabilidad, que el ejemplar que se entrega para su publicación digital es copia íntegra y exacta del original que se leyó y aprobó en su fecha para la obtención del grado de doctor.

El Autor autoriza expresamente a la UNIVERSIDAD para ceder, en su caso, los derechos objeto del presente Contrato a las Entidades con la que la Universidad establezca convenio de colaboración para difundir las tesis en línea.

La cesión se efectúa con el carácter de no exclusiva y dada la naturaleza intrínsecamente transfronteriza del medio utilizado por la UNIVERSIDAD para la difusión de su fondo digitalizado, la cesión tendrá eficacia a nivel mundial.

Duración

El contrato entrará en vigor el día de su firma. La cesión posee carácter gratuito y tendrá la duración correspondiente al período legalmente establecido hasta el paso de la obra a dominio público.

Con la finalización del contrato se producirá el cese inmediato en la utilización de los derechos cedidos y la Universidad devolverá al Autor todos los materiales que le hubieran sido entregados por éste. En el caso de finalización de este Contrato por cualquier causa, cada una de las partes cesará inmediatamente en la utilización de los derechos y signos, el uso de los cuales y la explotación les hubiera estado cedida por la otra parte. Así mismo, la UNIVERSIDAD, devolverá de forma inmediata al Autor todos los materiales que le hayan sido entregados por este.

Derechos de autor

La titularidad de los derechos morales y explotación de propiedad intelectual sobre la Tesis Doctoral, pertenece y seguirá perteneciendo al Autor. La UNIVERSIDAD, adquiere únicamente los derechos que específicamente figuren en este Contrato, y en particular los que se especifican en la Cláusula Primera.

Por lo tanto, quedan excluidos de este Contrato y reservados al Autor, cuantos derechos le correspondan con relación a modalidades de uso de la Tesis Doctoral no previstas en la cláusula primera, o que hayan de efectuarse en forma y condiciones distintas a las expresamente indicadas en esta cláusula.

Cada una de las partes informará inmediatamente a la otra de cualquier infracción de los derechos de propiedad intelectual de los que hubiera tenido conocimiento.

Obligaciones del autor

El AUTOR se compromete y obliga a:

a) Proporcionar a la GALERÍA la información que necesite sobre la obra realizada

b) Colaborar en los actos que la GALERÍA realice para promocionar su obra.

c) Intervenir en el asesoramiento para proceder al montaje y desmontaje de la exposición.

El Autor deberá indicar inmediatamente a la UNIVERSIDAD cualquier error o incidencia de la que tenga conocimiento en relación con la Tesis Doctoral con el objeto de que la UNIVERSIDAD, pueda actuar en consecuencia.

Obligaciones de la Universidad

La UNIVERSIDAD, en virtud del presente Contrato, adquiere el derecho, pero no la obligación, de poder difundir la Tesis Doctoral a través de Internet o de los otros medios enumerados en la Cláusula 1 anterior. La difusión, ya sea total o parcial, se realizará haciendo constar siempre el nombre y apellidos del autor de la obra, el título de la misma y la fecha de aprobación así como que la Universidad de Zaragoza ostenta los correspondientes derechos de dicha reproducción y comunicación pública.

La UNIVERSIDAD únicamente pondrá a disposición de sus usuarios la Tesis Doctoral para su uso privado y/o con fines de investigación y educación, pero no garantiza ni asume responsabilidad alguna para la forma y manera en que los usuarios hagan uso posterior de la Tesis Doctoral. Se asegurará en todo caso que el sistema utilizado para la visualización de la obra asegure que el texto podrá ser leído pero no ser modificado.

Las partes reconocen y acuerdan que la UNIVERSIDAD no tiene intención de censurar ni revisar la exactitud y adecuación de la Tesis Doctoral, ni podrá ser obligada a hacerlo, en consecuencia será, en todo caso el Autor el responsable del contenido de la Tesis Doctoral, así como de cualquier supervisión de la adaptación de la misma a través de Internet.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y Ley aplicable / Sin claúsula penal / Sumisión a tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal / Sumisión a tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Sumisión a arbitraje / Arbitraje / Sin cláusula penal / Sumisión a Arbitraje sin cláusula penal en caso de no ejecución voluntaria del laudo / Con cláusula penal / Sumisión a Arbitraje con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE CESIÓN DE DERECHOS DE TESIS DOCTORAL, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(Universidad)

Fdo. Don [NOMBRE Y APELLIDOS]

(El Autor)

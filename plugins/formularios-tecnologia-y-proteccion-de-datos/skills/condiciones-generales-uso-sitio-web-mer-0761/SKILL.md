---
name: condiciones-generales-uso-sitio-web-mer-0761
description: "Condiciones generales de uso de un sitio web. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Condiciones generales de uso de un sitio web

> Formulario **MER-0761** del plugin **Contratos tecnológicos, comercio electrónico y protección de datos** (`formularios-tecnologia-y-proteccion-de-datos`) · Mercantil › Tecnología, comercio electrónico y protección de datos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Condiciones generales de uso de un sitio web» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Condiciones generales de uso de un sitio web” para mi caso». También puedes invocarla directamente con `/formularios-tecnologia-y-proteccion-de-datos:condiciones-generales-uso-sitio-web-mer-0761`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-tecnologia-y-proteccion-de-datos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos tecnológicos, comercio electrónico y protección de datos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DIRECCIÓN WEB

## Normas que cita el formulario

- art. 11 Ley 34/2002

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

CONDICIONES GENERALES DE USO DE PÁGINA WEB

La utilización de esta página web así como las de los subdominios y/o directorios (en adelante conjuntamente denominados el "Sitio") queda sometida tanto a las presentes Condiciones Generales de Uso, como a las condiciones particulares propias (en adelante, las "Condiciones Particulares") que, según los casos, puedan regir la utilización de determinados servicios ofertados en la misma. Por lo tanto, con anterioridad a la utilización de dichos servicios, el Usuario también habrá de leer atentamente tanto este Aviso Legal como, en su caso, las correspondientes Condiciones Particulares. Asimismo, la utilización del Sitio se encuentra sometida igualmente a todos los avisos, reglamentos de uso e instrucciones, que puestos en conocimiento del Usuario por LA EMPRESA sustituyan, completen y/o modifique las presentes Condiciones Generales de Uso. Por el mero uso del Sitio o de cualquiera de los sitios incluidos en la página web el Usuario manifiesta su aceptación sin reservas de las presentes Condiciones Generales de Uso.

Por ello, si las consideraciones detalladas en este Aviso Legal no son de su conformidad, rogamos no haga uso del Sitio, ya que cualquier uso que haga del mismo o de los servicios y contenidos en él implicará la aceptación de los términos legales recogidos en este texto.

LA EMPRESA se reserva el derecho a realizar cambios en el Sitio sin previo aviso, con el objeto de actualizar, corregir, modificar, añadir o eliminar los contenidos del Sitio o de su diseño. Los contenidos y servicios del Sitio se actualizan periódicamente. Debido a que la actualización de la información no es inmediata, le sugerimos que compruebe siempre la vigencia y exactitud de la información, servicios y contenidos recogidos en el Sitio. Asimismo, las condiciones y términos que se recogen en el presente Aviso Legal pueden variar, por lo que le invitamos a que revise estos términos cuando visite de nuevo el Sitio.

El acceso a algunas de las secciones o apartados de esta página web le puede redireccionar a otras páginas de LA EMPRESA, en las que encontrará asimismo las correspondientes Condiciones Generales de Uso y Política de Privacidad, todas ellas en línea con las contenidas en la presente página.

Condición de usuario

La utilización del Sitio atribuye la condición de Usuario del Sitio (en adelante, el "Usuario") e implica la aceptación plena y sin reservas de todas y cada una de las disposiciones incluidas tanto en el presente Aviso Legal como en la Política de Privacidad.

Responsabilidades del usuario

El Usuario se compromete a utilizar los Servicios del Sitio de acuerdo con los términos expresados en el presente Aviso Legal, siendo responsable de su uso correcto. Sin perjuicio de lo que se expone a continuación, el Usuario se obliga a no utilizar el Sitio para la prestación de servicios, la realización de actividades publicitarias o de explotación comercial.

Veracidad de los datos proporcionados por el usuario

Algunos de los servicios ofertados requieren el previo registro del Usuario, para cuya utilización deberá darse de alta como Usuario de la web de LA EMPRESA, debiendo para ello leer y aceptar expresamente, en el momento anterior a efectuar su alta en el servicio, las condiciones de registro y la Política de Privacidad.

Toda la información que facilite el Usuario deberá ser veraz. A estos efectos, el Usuario garantiza la autenticidad de todos aquellos datos que comunique como consecuencia de la cumplimentación de los formularios necesarios para el registro y acceso a determinados servicios. Será asimismo responsabilidad del Usuario mantener toda la información facilitada a LA EMPRESA. permanentemente actualizada de forma que responda, en cada momento, a la situación real del Usuario. En todo caso el Usuario será el único responsable de las manifestaciones falsas o inexactas que realice y de los perjuicios que cause a LA EMPRESA o a terceros por la información que facilite.

Todo aquel que envíe comunicaciones a este sitio web o a sus propietarios será responsable del contenido de éstas, también en lo que se refiere a su veracidad y precisión, no haciéndose, por tanto, responsable LA EMPRESA de la información y contenidos introducidos por terceros.

No obstante y en cumplimiento de lo dispuesto en el art. 11 y 16 de la Ley 34/2002, de Servicios de la Sociedad de la Información y del Comercio Electrónico, LA EMPRESA se pone a disposición de todos los usuarios, autoridades y fuerzas de seguridad para colaborar de forma activa en la retirada o en su caso bloqueo de todos aquellos contenidos que pudieran afectar o contravenir la legislación nacional, o internacional, derechos de terceros o la moral y el orden público. En caso de que el usuario considere que existe en el sitio web algún contenido que pudiera ser susceptible de esta clasificación, se ruega lo notifique de forma inmediata al propietario del sitio web.

Uso de las facilidades de mensajería instantánea (chat)

LA EMPRESA no se hace responsable de los contenidos que, en contravención a las presentes Condiciones Generales de Uso y de cualesquiera otras que regulen o puedan regular cualesquiera de los servicios ofrecidos en la página web de LA EMPRESA las partes pudieran enviarse, siendo el Usuario el único responsable de la veracidad y licitud de los mismos.

LA EMPRESA no se responsabiliza del uso que pueda darse ni de los contenidos que puedan ser enviados y/o visualizados a través del sistema de mensajería instantánea (chat). Ninguna de las informaciones y/o contenidos que puedan ser introducidos y/o visualizados a través de esta facilidad podrá ser entendido como contenido LA EMPRESA ni que LA EMPRESA tenga responsabilidad alguna sobre los mismos. No obstante todo lo anterior, se reserva el derecho de retirar el acceso a esta facilidad en caso de tener conocimientos de un uso indebido de la misma, entendiéndose por tal la introducción de contenidos ilegales o contrarios a la moral y al orden público, así como en caso de hacerse en uso de la misma que sea o pueda ser perjudicial para la imagen de la compañía.

Uso de los contenidos del sitio

El Usuario se obliga a no utilizar el Sitio ni los servicios ofertados en o a través del mismo para la realización de actividades contrarias a las leyes, a la moral, al orden público, lesivas de los derechos e intereses de terceros o que de cualquier otra forma puedan dañar, inutilizar, sobrecargar, deteriorar o impedir la normal utilización del Sitio.

El Usuario que actúe contra la imagen, buen nombre o reputación de LA EMPRESA, así como quien utilice ilícita o fraudulentamente los diseños, logos o contenidos del Sitio y/o viole en cualquier forma los derechos de propiedad intelectual e industrial del Sitio o de los contenidos y servicios de la misma, será responsable frente a LA EMPRESA de su actuación. A los efectos aquí previstos se entenderá por contenidos, sin que esta enumeración tenga carácter limitativo, los textos, fotografías, gráficos, imágenes, iconos, tecnología, software, links y demás contenidos audiovisuales o sonoros, así como su diseño gráfico y códigos fuente En particular, el Usuario se compromete a abstenerse de:

a)Reproducir, copiar, distribuir, poner a disposición o de cualquier otra forma comunicar públicamente, transformar o modificar los Contenidos, a menos que se cuente con la autorización del titular de los correspondientes derechos o ello resulte legalmente permitido;

b)Suprimir, manipular o de cualquier forma alterar el ¨copyright¨ y demás datos identificativos de la reserva de derechos de LA EMPRESA o de sus titulares.

Derechos de propiedad intelectual y de propiedad industrial

Tanto el diseño del Sitio y sus códigos fuente, como los logos, marcas, y demás signos distintivos que aparecen en el mismo, pertenecen a LA EMPRESA o entidades colaboradoras y están protegidos por los correspondientes derechos de propiedad intelectual e industrial. Igualmente están protegidos por los correspondientes derechos de propiedad intelectual e industrial las imágenes, logos y melodías, etc. contenidos en el servidor de LA EMPRESA. En ningún momento podrá entenderse que el uso o acceso al Sitio y/o a los servicios ofertados en el mismo atribuyen al Usuario derecho alguno sobre las citadas marcas, nombres comerciales y/o signos distintivos.

Su uso, reproducción, distribución, comunicación pública, transformación o cualquier otra actividad similar o análoga, queda totalmente prohibida salvo que medie expresa autorización de LA EMPRESA. La licencia de uso de cualquier contenido de este Sitio otorgada al usuario se limita a la descarga por parte del usuario de dicho contenido y el uso profesional del mismo, siempre que los citados contenidos permanezcan íntegros.

LA EMPRESA declara su respeto a los derechos de propiedad intelectual e industrial de terceros; por ello, si considera que este sitio pudiera estar violando sus derechos, rogamos se ponga en contacto con LA EMPRESA en la siguiente dirección de e-mail

Frames

LA EMPRESA prohíbe expresamente la realización de ¨framings¨ o la utilización por parte de terceros de cualesquiera otros mecanismos que alteren el diseño, configuración original o contenidos de su Sitio.

Privacidad

LA EMPRESA cumple con la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y con cualquier otra normativa vigente en la materia, y mantiene una Política de Privacidad sobre los datos personales, en la que se describe, principalmente, el uso que LA EMPRESA hace de los datos de carácter personal, se informa al Usuario detalladamente de las circunstancias esenciales de dicho uso y de las medidas de seguridad que se aplican a sus datos de carácter personal para evitar que terceros no autorizados puedan acceder a ellos.

LA EMPRESA podrá utilizar ¨cookies¨. Las ¨cookies¨ son ficheros de texto que los ordenadores mandan a su disco duro para facilitar a su ordenador un acceso más rápido a la página web seleccionada. La finalidad de las ¨cookies¨ de LA EMPRESA es personalizar los servicios que le ofrecemos, facilitándole información que pueda ser de su interés. Las ¨cookies¨ no extraen información de su ordenador, ni determinan donde se encuentra Ud. Si a pesar de ello, Ud. no desea que se instale en su disco duro una ¨cookie¨, solicitamos configure el navegador de su ordenador para no recibirlas. Sin embargo, le hacemos notar que, en todo caso, la calidad de funcionamiento de la página web puede disminuir

Responsabilidades de la empresa

9.1 Uso incorrecto del Sitio

LA EMPRESA. ha creado el Sitio [DIRECCIÓN WEB] para la difusión de su actividad y para facilitar el acceso a sus servicios, pero no puede controlar la utilización del mismo de forma distinta a la prevista en el presente Aviso Legal; por tanto el acceso al Sitio y el uso correcto de la información contenida en el mismo son responsabilidad de quien realiza estas acciones, no siendo responsable LA EMPRESA por el uso incorrecto, ilícito o negligente que del mismo pudiere hacer el Usuario, ni del conocimiento que puedan tener terceros no autorizados de la clase, condiciones, características y circunstancias del uso que los Usuarios hacen del Sitio y de los servicios. Asimismo, LA EMPRESA tampoco será responsable de los perjuicios de toda naturaleza que puedan deberse a la suplantación de la personalidad de un tercero efectuada por un Usuario en cualquier clase de comunicación realizada a través del Sitio.

9.2Utilización de los contenidos

LA EMPRESA facilita todos los contenidos de su Sitio de buena fe y realizará sus mejores esfuerzos para que los mismos estén permanentemente actualizados y vigentes; no obstante, LA EMPRESA no puede asumir responsabilidad alguna respecto al uso o acceso que realicen los Usuarios fuera del ámbito al que se dirige el Sitio, cuya responsabilidad final recaerá sobre el Usuario.

9.3Virus

LA EMPRESA se compromete a aplicar todas las medidas necesarias para intentar garantizar al Usuario la ausencia de virus, gusanos, caballos de Troya y elementos similares en su Sitio. No obstante, estas medidas no son infalibles y, por ello, no puede asegurar totalmente la ausencia de dichos elementos nocivos. En consecuencia, LA EMPRESA no será responsable de los daños que los mismos pudieran producir al Usuario.

9.4Fallos tecnológicos

LA EMPRESA ha concluido todos los contratos necesarios para la continuidad de su Sitio y realizará sus mejores esfuerzos para que el mismo no sufra interrupciones, pero no puede garantizar la ausencia de fallos tecnológicos, ni la permanente disponibilidad del Sitio y de los servicios contenidos en él y, en consecuencia, no asume responsabilidad alguna por los daños y perjuicios que puedan generarse por la falta de disponibilidad y por los fallos en el acceso ocasionados por desconexiones, averías, sobrecargas o caídas de la red no imputables a LA EMPRESA.

Ley aplicable y jurisdicción

La ley aplicable en caso de disputa o conflicto de interpretación de los términos que conforman este Aviso Legal, así como cualquier cuestión relacionada con los servicios del presente Sitio, será la ley española. Para la resolución de cualquier conflicto que pueda surgir con ocasión de la visita al Sitio o del uso de los servicios que en él se puedan ofertar, LA EMPRESA y el Usuario acuerdan someterse a los Tribunales de domicilio del Usuario, siempre que el mismo esté situado en territorio español.

Links o hiperenlaces

LA EMPRESA le facilita el acceso a otras páginas web que consideramos pueden ser de su interés. El objetivo de dichos enlaces es únicamente facilitarle la búsqueda de los recursos que le puedan interesar a través de Internet. No obstante, algunas de dichas páginas no pertenecen a LA EMPRESA ni se hace una revisión de sus contenidos, por lo que en ningún momento se podrá considerar a LA EMPRESA como responsable de las mismas, del funcionamiento de la página enlazada o de los posibles daños que puedan derivarse del acceso o uso de la misma.

No se permitirá el enlace de ninguna página web o de una dirección de correo electrónico al Sitio, salvo con la autorización expresa por escrito de LA EMPRESA. Adicionalmente, dichos enlaces deberán respetar las siguientes condiciones: (a) únicamente podrán realizarse enlaces con la Home Page o página principal de esta web; (b) el establecimiento del enlace no supondrá ningún tipo de acuerdo, contrato, patrocinio ni recomendación por parte de LA EMPRESA de la página que realiza el enlace salvo que así se derive de la correspondiente relación contractual entre las partes.

En cualquier momento, LA EMPRESA podrá retirar la autorización mencionada en el párrafo anterior, sin necesidad de alegar causa alguna. En tal caso, la página que haya realizado el enlace deberá proceder a su inmediata supresión, tan pronto como reciba la notificación de la revocación de la autorización por parte de LA EMPRESA.

Duración y terminación

La prestación del servicio del Sitio y los demás servicios ofertados en el mismo tiene, en principio, una duración indefinida. LA EMPRESA podrá, no obstante, dar por terminada o suspender la prestación del servicio del Sitio y/o de cualquiera de los servicios en cualquier momento, sin perjuicio de lo que se hubiere dispuesto al respecto en las correspondientes Condiciones Particulares. A tal efecto, LA EMPRESA comunicará dicha circunstancia en la pantalla de acceso al servicio con un preaviso de quince días.

LA EMPRESA se reserva, asimismo, el derecho de modificar unilateralmente, en cualquier momento y sin previo aviso, la presentación y condiciones del Sitio, así como los servicios del mismo y las condiciones requeridas para su utilización.

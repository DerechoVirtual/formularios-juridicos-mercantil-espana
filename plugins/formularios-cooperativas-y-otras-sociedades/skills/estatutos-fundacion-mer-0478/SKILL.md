---
name: estatutos-fundacion-mer-0478
description: "Estatutos de una fundación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Estatutos de una fundación

> Formulario **MER-0478** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Estatutos de una fundación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Estatutos de una fundación” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:estatutos-fundacion-mer-0478`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DIRECCIÓN
- [ ] LOCALIDAD
- [ ] Nº
- [ ] OTROS DATOS
- [ ] PORCENTAJE
- [ ] ÁMBITO TERRITORIAL

## Normas que cita el formulario

- art. 1024 Código Civil
- art. 31 Ley 50/2002

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

DENOMINACIÓN, DURACIÓN, DOMICILIO Y OBJETO
APLICACIÓN DE LOS RECURSOS AL CUMPLIMIENTO DE LOS FINES FUNDACIONALES Y DETERMINACIÓN DE LOS BENEFICIARIOS
RÉGIMEN ECONÓMICO
GOBIERNO DE LA FUNDACIÓN
EXTINCIÓN DE LA FUNDACIÓN

Modelo de estatutos de una Fundación, en los que se establecen las condiciones necesarias para su creación, organización y funcionamiento, tales como su denominación, duración, domicilio, objeto, régimen económico, órganos de gobierno y extinción.

TÍTULO I.- DENOMINACIÓN, DURACIÓN, DOMICILIO Y OBJETO

Artículo 1º.- Denominación

La Fundación se denomina ", Fundación", y se regirá por los presentes estatutos, así como por la Ley 50/2002 y por las disposiciones legales que le sean aplicables en cada momento.

Artículo 2º.- Fines fundacionales

La Fundación tiene como fines fundacionales los siguientes fines de interés general:

Artículo 3º.- Domicilio

El domicilio de la Fundación se halla situado en [DIRECCIÓN], [LOCALIDAD]

El Patronato podrá acordar el cambio de domicilio, debiendo en tal caso comunicarlo al Registro de Fundaciones y al Protectorado.

Artículo 4º.- Ámbito territorial de las actividades

La Fundación desarrollará sus actividades principalmente en [ÁMBITO TERRITORIAL]

Artículo 5º.- Duración

La Fundación tendrá una duración de carácter indefinido.

TÍTULO II.- APLICACIÓN DE LOS RECURSOS AL CUMPLIMIENTO DE LOS FINES FUNDACIONALES Y DETERMINACIÓN DE LOS BENEFICIARIOS

Artículo 6º.- Dotación

La dotación de la Fundación es la consignada en su escritura de constitución, sin perjuicio de las modificaciones de la misma que puedan efectuarse, y que deberán ser inscritas en el Registro de Fundaciones.

Artículo 7º.- Inventario e inscripción

Los bienes y derechos que formen el patrimonio de la fundación deben figurar a su nombre, y hacerse constar en su inventario anual.

El Patronato debe promover, bajo su responsabilidad, la inscripción a nombre de la fundación de los bienes y derechos que integran el patrimonio de ésta, en los Registros públicos correspondientes.

Artículo 8º. - Herencias y donaciones

La aceptación de herencias por las fundaciones se entenderá hecha siempre a beneficio de inventario. Los patronos serán responsables frente a la fundación de la pérdida del beneficio de inventario por los actos a que se refiere el artículo 1024 del Código Civil.

La aceptación de legados con cargas o donaciones onerosas o remuneratorias y la repudiación de herencias, donaciones o legados sin cargas será comunicada por el Patronato al Protectorado en el plazo máximo de los diez días hábiles siguientes, pudiendo éste ejercer las acciones de responsabilidad que correspondan contra los patronos, si los actos del Patronato fueran lesivos para la fundación, en los términos previstos legalmente.

Artículo 9º.- Enajenaciones y gravámenes

La enajenación o gravamen de los bienes y derechos se efectuarán según lo dispuesto en la normativa vigente, previa solicitud de las autorizaciones que sean precisas, o practicándose las comunicaciones que sean necesarias.

Artículo 10º.- Destino de rentas e ingresos

Se efectuará en los términos previstos legalmente.

Artículo 11º.- Beneficiarios de la Fundación

Serán beneficiarios de la Fundación:

El Patronato facilitará información suficiente de los fines y actividades de la fundación, para que éstos sean conocidos por los beneficiarios y demás interesados.

TÍTULO III.- RÉGIMEN ECONÓMICO

Artículo 12º.- Contabilidad, auditoría y plan de actuación

Se regirán por lo previsto legalmente, siendo el Presidente quien formulará las cuentas anuales, que deberán ser aprobadas en el plazo máximo de seis meses desde el cierre del ejercicio por el Patronato de la fundación.

TÍTULO IV.- GOBIERNO DE LA FUNDACIÓN

Artículo 13º.- Patronato

El gobierno y representación de la Fundación corresponde al Patronato, así como el cumplimiento de los fines fundacionales y la administración de los bienes y derechos que integran el patrimonio de la fundación, manteniendo plenamente el rendimiento y utilidad de los mismos.

Igualmente, es el órgano competente para interpretar la voluntad del fundador (o fundadores), los preceptos contenidos en los presentes estatutos y cubrir sus lagunas.

Podrán ser miembros del Patronato las personas físicas que tengan plena capacidad de obrar y no estén inhabilitadas para el ejercicio de cargos públicos. Las personas jurídicas podrán formar parte del Patronato, debiendo designar a una persona física que las represente.

Artículo 14º.- Patronos

El Patronato estará formado por [Nº] patronos que elegirán entre ellos un Presidente.

El cargo de Secretario, podrá recaer en una persona que no sea miembro del Patronato, en cuyo caso tendrá voz pero no voto, a quien corresponde la certificación de los acuerdos del Patronato.

Los patronos entrarán a ejercer sus funciones después de haber aceptado expresamente el cargo en documento público, en documento privado con firma legitimada por notario o mediante comparecencia realizada al efecto en el Registro de Fundaciones. La aceptación se podrá llevar también a cabo ante el Patronato, acreditándose a través de certificación expedida por el Secretario, con firma legitimada notarialmente.

Dicha aceptación se notificará formalmente al Protectorado y se inscribirá en el mencionado Registro.

Los patronos ejercerán su cargo gratuitamente, sin perjuicio del derecho a ser reembolsados de los gastos debidamente justificados que el cargo les ocasione en el ejercicio de su función.

El cargo de patrono, en caso de recaer en persona física, deberá ejercerse personalmente. No obstante, podrá actuar en su nombre y representación otro patrono por él designado. Esta actuación será siempre para actos concretos y deberá ajustarse a las instrucciones que, en su caso, el representado formule por escrito.

Podrá actuar en nombre de quien fuera llamado a ejercer la función de patrono por razón del cargo que ocupare, la persona a quien corresponda su sustitución.

Artículo 15º.- Delegación y apoderamientos

El Patronato podrá delegar sus facultades en uno o más de sus miembros. No son delegables la aprobación de las cuentas y del presupuesto ni aquellos actos que requieran la autorización del Protectorado.

El Patronato podrá nombrar apoderados generales o especiales.

Las delegaciones, los apoderamientos generales y su revocación deberán inscribirse en el Registro de Fundaciones.

Artículo 16º.- Otros órganos

Artículo 17º.- Responsabilidad de los patronos

Los patronos deberán desempeñar el cargo con la diligencia de un empresario eficiente y de un representante leal.

El régimen de su responsabilidad se sujeta a lo previsto legalmente.

Artículo 18º.- Sustitución, cese y suspensión de patronos

La sustitución de los patronos se producirá en la siguiente forma [OTROS DATOS]

El cese se producirá por las causas legalmente previstas.

La suspensión de los patronos podrá ser acordada cautelarmente por el Juez cuando se entable contra ellos la acción de responsabilidad.

La sustitución, cese y suspensión de patronos se inscribirán en el Registro de Fundaciones.

Artículo 19º.- Sesiones

El Patronato se reunirá cuantas veces lo determine su Presidente o Vicepresidente, en su caso, a iniciativa propia o a petición de cualquiera de sus miembros. Será presidido por el Presidente, y en su ausencia, por el Vicepresidente o Secretario, por este orden, y a falta de ambos, por el patrono de mayor edad.

Artículo 20º.- Votaciones y adopción de los acuerdos

Para que los acuerdos del Patronato sean válidos deberán ser adoptados por mayoría de votos, siendo necesaria, al menos, la concurrencia de [PORCENTAJE] de sus miembros.

Artículo 21º.- Atribuciones del Presidente

El Presidente del Patronato tendrá las siguientes atribuciones:

1. Formular las cuentas anuales.
2. Dirigir las tareas del Patronato.
3. Ordenar los pagos acordados válidamente.
4. Representar legalmente a la Fundación por delegación del Patronato.
5. Convocar, presidir y levantar las sesiones que celebre el Patronato, y dirigir sus deliberaciones con voto de calidad, en caso de empate.
6. Proponer el plan de actividades de la Fundación al Patronato.

Artículo 22º.- Atribuciones del secretario

El secretario tiene a su cargo:

- La dirección de los trabajos administrativos de la Fundación.
- La custodia de los documentos oficiales e internos.
- La redacción de las actas de las sesiones, las cuales transcribirá al correspondiente libro, una vez aprobadas, y con el visto bueno del Presidente.

Además, velará especialmente por el cumplimiento de las disposiciones legales vigentes en materia de fundaciones, y cursará al Registro de Fundaciones, al Protectorado y a los demás órganos de la Administración Pública que resulten competentes, cuantas comunicaciones y documentos a que aparezca obligada la Fundación.

Ostenta asimismo la facultad certificante de los acuerdos del Patronato.

TÍTULO V.- EXTINCIÓN DE LA FUNDACIÓN

Artículo 23º.- Causas y acuerdo de extinción

La Fundación se extinguirá por las causas y en las formas previstas en el artículo 31 de la Ley 50/2002, de 26 de diciembre, de Fundaciones.

El acuerdo de extinción o, en su caso, la resolución judicial en que se decida, serán comunicados por el Patronato al Registro de Fundaciones para su inscripción.

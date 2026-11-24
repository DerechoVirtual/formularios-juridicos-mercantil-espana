---
name: acta-junta-general-extraordinaria-sa-acuerda-disolucion-mer-0293
description: "Acta de junta general extraordinaria de una SA que acuerda la disolución. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de junta general extraordinaria de una SA que acuerda la disolución

> Formulario **MER-0293** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Acta de la Junta General Extraordinaria (o universal) de accionistas de una sociedad anónima en la que se acuerda disolver la sociedad, cesar a los administradores y nombrar liquidadores, con facultad para elevar a público los acuerdos.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de junta general extraordinaria de una SA que acuerda la disolución» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de junta general extraordinaria de una SA que acuerda la disolución” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-junta-general-extraordinaria-sa-acuerda-disolucion-mer-0293`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (10 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] Nº (9 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] HORA (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] Nº DE ARTÍCULO (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] CALLE Y NÚMERO
- [ ] DETERMINAR LA MAYORÍA
- [ ] DIRECCIÓN DE LA PÁGINA WEB
- [ ] DNI/NIE
- [ ] DOCUMENTO ACREDITATIVO DE LA REPRESENTACIÓN
- [ ] NOMBRE DEL DIARIO
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE
- [ ] NOMBRE Y APELLIDOS DEL SOCIO
- [ ] NOMBRE Y APELLIDOS DEL SOCIO REPRESENTADO
- [ ] OTROS PUNTOS DEL ORDEN DEL DÍA, SI LOS HUBIERA
- [ ] REPETIR EL SIGUIENTE PÁRRAFO TANTAS VECES COMO SOCIOS PRESENTES:
- [ ] REPETIR EL SIGUIENTE PÁRRAFO TANTAS VECES COMO SOCIOS REPRESENTADOS:

## Normas que cita el formulario

- art. 191 LSC
- art. 193 LSC
- art. 364 LSC
- art. 202 LSC

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

- Junto a «…én por los estatutos o por los accionistas asistentes a la junta (art. 191 LSC).»: el original citaba el art. 202 LSC para esta regla; comprobar el artículo.

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

ACTA DE JUNTA GENERAL DE [DENOMINACIÓN SOCIAL], S.A.

En [LOCALIDAD], siendo las [HORA] horas del día [FECHA], se reunió en [ELEGIR: primera / segunda] convocatoria, en el domicilio social de [DENOMINACIÓN SOCIAL], S.A., sito en calle [DOMICILIO] de [LOCALIDAD], la Junta General Extraordinaria de socios, previa convocatoria al efecto del [ELEGIR: administrador único / administrador solidario / administrador mancomunado / consejo de administración] de la citada mercantil, realizada mediante:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Con página web) Anuncio en la página web de la sociedad [DIRECCIÓN DE LA PÁGINA WEB] desde el [FECHA] hasta la fecha de la celebración de la junta, el [FECHA], y alerta telemática a los correos electrónicos correspondientes a cada socio de los anuncios de convocatoria insertados en la web.

— (Sin página web) Anuncio publicado en el Boletín Oficial del Registro Mercantil n.º [Nº], correspondiente al día [FECHA], y en el diario [NOMBRE DEL DIARIO] de [LOCALIDAD] de [FECHA].

— (Comunicación individual) El procedimiento de comunicación individual y escrita previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales, habiendo sido remitido el anuncio al último de los socios con fecha de [FECHA].

El texto íntegro de la convocatoria fue el siguiente:

CONVOCATORIA

D./Dña. [NOMBRE Y APELLIDOS DEL SOCIO]

En [LOCALIDAD], a [FECHA].

Estimado señor:

Por la presente, le comunicamos la próxima celebración de la junta general de la sociedad [DENOMINACIÓN SOCIAL], S.A., de la que usted es socio, y le convocamos de acuerdo con lo previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales.

La junta general de socios se celebrará en [CALLE Y NÚMERO], de la localidad de [LOCALIDAD], y tendrá lugar, en primera convocatoria, el día [FECHA], a las [HORA] horas y, en segunda convocatoria, el día [FECHA], a las [HORA] horas.

La junta convocada tendrá el siguiente

ORDEN DEL DÍA

1.º) Disolver la sociedad, adoptando cuantos acuerdos complementarios sean precisos y, en concreto, procediéndose al cese de los actuales administradores y correspondiente nombramiento de liquidadores.

2.º) [OTROS PUNTOS DEL ORDEN DEL DÍA, SI LOS HUBIERA]

3.º) Ruegos y preguntas.

4.º) Aprobación, en su caso, del acta de la Junta.

Los accionistas tienen derecho a examinar en el domicilio social el texto íntegro de la disolución propuesta y de su informe, así como los documentos que deban ser sometidos a aprobación por la Junta, y a solicitar su entrega o envío gratuito.

[OPCIONAL — si ha lugar: en caso de junta universal, sustituir el párrafo de convocatoria anterior por el siguiente:] En [LOCALIDAD], calle [DOMICILIO], a [FECHA], siendo las [HORA] horas, se hallan reunidos en el domicilio social de [DENOMINACIÓN SOCIAL], S.A., la totalidad de sus socios, como consta en la lista de asistentes, que representan la totalidad del capital social, y acuerdan por unanimidad constituirse en Junta General Extraordinaria de carácter universal, al amparo de lo previsto en el art. 178 de la Ley de Sociedades de Capital y en el art. [Nº DE ARTÍCULO] de los estatutos sociales, para tratar y deliberar sobre el orden del día antes transcrito, que es unánimemente aceptado.

Actúa como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario D./Dña. [NOMBRE Y APELLIDOS], designados ambos por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las acciones que poseen y/o representan cada uno de ellos:

Socios presentes:

[REPETIR EL SIGUIENTE PÁRRAFO TANTAS VECES COMO SOCIOS PRESENTES:]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE]% del total del capital social con derecho a voto.

Socios representados:

[REPETIR EL SIGUIENTE PÁRRAFO TANTAS VECES COMO SOCIOS REPRESENTADOS:]

D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTANTE], vecino/a de [LOCALIDAD], calle [DOMICILIO], mayor de edad y con DNI [DNI/NIE], asiste en nombre y representación, según acredita mediante [DOCUMENTO ACREDITATIVO DE LA REPRESENTACIÓN], de D./Dña. [NOMBRE Y APELLIDOS DEL SOCIO REPRESENTADO], titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE]% del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [Nº] acciones, que representan el [PORCENTAJE]% del capital social.

Todo el capital social de la compañía tiene derecho a voto.

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Junta.

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por [DETERMINAR LA MAYORÍA] se adoptan los acuerdos cuyo contenido se transcribe a continuación.

[NOTA SOBRE LA MAYORÍA REQUERIDA: salvo previsión estatutaria que establezca otras superiores, en primera convocatoria se necesita la concurrencia de accionistas presentes o representados que posean al menos el 50% del capital suscrito con derecho a voto; en segunda convocatoria es suficiente la concurrencia del 25% de dicho capital, pero si concurren accionistas que representan menos del 50% del capital suscrito con derecho a voto, los acuerdos citados solo pueden adoptarse válidamente con el voto favorable de los dos tercios del capital presente o representado en la junta. Esta mayoría puede ser elevada por los estatutos sociales.]

ACUERDOS

Primero.- Disolución de la sociedad

Disolver la sociedad por la siguiente causa: [DETERMINAR LA CAUSA QUE MOTIVA LA DISOLUCIÓN, ELIGIENDO ENTRE LAS SIGUIENTES:]

a) Por el cese en el ejercicio de la actividad o actividades que constituyan el objeto social. En particular, se entenderá que se ha producido el cese tras un período de inactividad superior a un año.

b) Por la conclusión de la empresa que constituya su objeto.

c) Por la imposibilidad manifiesta de conseguir el fin social.

d) Por la paralización de los órganos sociales de modo que resulte imposible su funcionamiento.

e) Por pérdidas que dejen reducido el patrimonio neto a una cantidad inferior a la mitad del capital social, a no ser que éste se aumente o se reduzca en la medida suficiente, y siempre que no sea procedente solicitar la declaración de concurso.

f) Por reducción del capital social por debajo del mínimo legal, que no sea consecuencia del cumplimiento de una ley.

g) Porque el valor nominal de las participaciones sociales sin voto o de las acciones sin voto excediera de la mitad del capital social desembolsado y no se restableciera la proporción en el plazo de dos años.

h) Por cualquier otra causa establecida en los estatutos.

[Téngase en cuenta que la declaración de concurso no constituye, por sí sola, causa de disolución, pero si en el procedimiento se produce la apertura de la fase de liquidación la sociedad queda automáticamente disuelta.]

Segundo.- Cese de los administradores y nombramiento de liquidadores

Cesar a los administradores sociales, quedando éstos convertidos en liquidadores de [DENOMINACIÓN SOCIAL], S.A., salvo que se hayan designado otros en los estatutos o que, al acordar la disolución, los designe la junta general.

Estando presentes los anteriores administradores y actuales liquidadores D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], aceptan el cargo y se obligan a cumplirlo bien y fielmente, declarando no hallarse incursos en ninguna de las incompatibilidades legales ni estatutarias, especialmente y por analogía en las previstas en la Ley 3/2015, de 30 de marzo.

Tercero.- Facultad para elevar a público

Facultar a todos y cada uno de los miembros del órgano de liquidación para que, indistintamente, puedan comparecer ante Notario y elevar a público los presentes acuerdos, otorgando a tales efectos las escrituras públicas correspondientes, incluidas las facultades de subsanación, rectificación o aclaración, así como para realizar cuantas actuaciones sean precisas o convenientes para la eficacia de los susodichos acuerdos.

Tras todo lo cual, redactada y leída que fue el acta por el Secretario, esta es aprobada por la Junta, por unanimidad de los asistentes.

No existiendo más asuntos que tratar, se levanta la sesión.

V.º B.º El Presidente | El Secretario

Firmado: D./Dña. [NOMBRE Y APELLIDOS] | Firmado: D./Dña. [NOMBRE Y APELLIDOS]

Asistentes

Firmado: D./Dña. [NOMBRE Y APELLIDOS]

NOTAS DE USO

1. Responsabilidad de los administradores (art. 367 de la Ley de Sociedades de Capital): responderán solidariamente de las obligaciones sociales posteriores al acaecimiento de la causa legal de disolución los administradores que incumplan la obligación de convocar en el plazo de dos meses la junta general para que adopte, en su caso, el acuerdo de disolución, así como los administradores que no soliciten la disolución judicial o, si procediere, el concurso de la sociedad en el plazo de dos meses a contar desde la fecha prevista para la celebración de la junta, cuando ésta no se haya constituido, o desde el día de la junta, cuando el acuerdo hubiera sido contrario a la disolución o al concurso.

2. Lista de asistentes (art. 98 del Reglamento del Registro Mercantil): figurará al comienzo de la propia acta o se adjuntará a ella por medio de anejo firmado por el Secretario, con el visto bueno del Presidente. Igualmente podrá formarse mediante fichero o incorporarse a soporte informático; en estos casos se extenderá en la cubierta precintada del fichero o del soporte la oportuna diligencia de identificación firmada por el Secretario, con el visto bueno del Presidente.

3. Presidente y secretario de la junta: la junta general será presidida por la persona que designen los estatutos; en su defecto, por el presidente del Consejo de Administración, y a falta de éste, por el accionista que elijan en cada caso los socios asistentes a la reunión. El presidente estará asistido por un secretario, designado también por los estatutos o por los accionistas asistentes a la junta (art. 191 LSC).

4. Quórum (art. 193 LSC): la junta general de accionistas quedará válidamente constituida en primera convocatoria cuando los accionistas presentes o representados posean, al menos, el veinticinco por ciento del capital suscrito con derecho de voto; los estatutos podrán fijar un quórum superior (art. 193.1). En segunda convocatoria será válida la constitución de la junta cualquiera que sea el capital concurrente, salvo que los estatutos fijen un quórum determinado, el cual necesariamente habrá de ser inferior al que aquéllos hayan establecido o exija la ley para la primera convocatoria (art. 193.2).

5. Mayoría para la disolución (art. 364 LSC): el acuerdo se adoptará con el quórum de constitución y las mayorías establecidas para las sociedades anónimas en los arts. 193 y 201.

6. Acta (art. 202 LSC): podrá ser aprobada por la propia junta a continuación de haberse celebrado ésta y, en su defecto, y dentro del plazo de quince días, por el presidente y dos interventores, uno en representación de la mayoría y otro por la minoría.

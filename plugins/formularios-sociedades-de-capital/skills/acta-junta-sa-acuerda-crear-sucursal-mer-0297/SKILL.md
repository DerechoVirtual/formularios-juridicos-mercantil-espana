---
name: acta-junta-sa-acuerda-crear-sucursal-mer-0297
description: "Acta de junta de una SA que acuerda crear una sucursal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de junta de una SA que acuerda crear una sucursal

> Formulario **MER-0297** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Acta de la Junta General Extraordinaria convocada, o junta universal, de accionistas de una sociedad anónima en la que se acuerda crear una sucursal en una localidad determinada, concretando los datos de identificación, la actividad y los representantes permanentes, con los acuerdos complementarios necesarios.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de junta de una SA que acuerda crear una sucursal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de junta de una SA que acuerda crear una sucursal” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-junta-sa-acuerda-crear-sucursal-mer-0297`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (9 veces)
- [ ] Nº (9 veces)
- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] CALLE, NÚMERO Y LOCALIDAD (5 veces)
- [ ] HORA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº DE ARTÍCULO (4 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] OTROS ACUERDOS, SI LOS HUBIERA (2 veces)
- [ ] OTROS PUNTOS DEL ORDEN DEL DÍA, SI LOS HUBIERA (2 veces)
- [ ] ACTIVIDADES
- [ ] CONTINÚA, EN AMBOS CASOS:
- [ ] DENOMINACIÓN O IDENTIFICACIÓN DE LA SUCURSAL
- [ ] DETERMINAR LA MAYORÍA
- [ ] DIRECCIÓN DE LA PÁGINA WEB
- [ ] DNI/NIE
- [ ] DOCUMENTO ACREDITATIVO DE LA REPRESENTACIÓN
- [ ] NOMBRE DEL DIARIO
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE
- [ ] NOMBRE Y APELLIDOS DEL SOCIO
- [ ] NOMBRE Y APELLIDOS DEL SOCIO REPRESENTADO
- [ ] NOMBRE Y APELLIDOS, DNI/NIE Y FACULTADES
- [ ] REPETIR EL SIGUIENTE PÁRRAFO TANTAS VECES COMO SOCIOS PRESENTES:
- [ ] REPETIR EL SIGUIENTE PÁRRAFO TANTAS VECES COMO SOCIOS REPRESENTADOS:

## Normas que cita el formulario

- art. 191 LSC
- art. 193 LSC
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

ACTA DE JUNTA GENERAL DE [DENOMINACIÓN SOCIAL], S.A.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LA OTRA:]

— JUNTA GENERAL EXTRAORDINARIA CONVOCADA

En [LOCALIDAD], siendo las [HORA] horas del día [FECHA], se reunió en [ELEGIR: primera convocatoria / segunda convocatoria], en el domicilio social de [DENOMINACIÓN SOCIAL], S.A., sito en calle [DOMICILIO] de [LOCALIDAD], la Junta General Extraordinaria de socios, previa convocatoria al efecto del [ELEGIR: administrador único / administrador solidario / administrador mancomunado / Consejo de Administración] de la citada mercantil, realizada mediante:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Con página web) Anuncio en la página web de la sociedad [DIRECCIÓN DE LA PÁGINA WEB] desde el [FECHA] hasta la fecha de la celebración de la junta, el [FECHA], y alerta telemática a los correos electrónicos correspondientes a cada socio de los anuncios de convocatoria insertados en la web.

— (Sin página web) Anuncio publicado en el Boletín Oficial del Registro Mercantil n.º [Nº], correspondiente al día [FECHA], y en el diario [NOMBRE DEL DIARIO].

— (Comunicación individual) El procedimiento de comunicación individual y escrita previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales, habiendo sido remitido el anuncio al último de los socios con fecha de [FECHA].

Que el texto íntegro de la convocatoria fue el siguiente:

CONVOCATORIA

D./Dña. [NOMBRE Y APELLIDOS DEL SOCIO]

En [LOCALIDAD], a [FECHA].

Estimado señor:

Por la presente, le comunicamos la próxima celebración de la junta general de la sociedad [DENOMINACIÓN SOCIAL], S.A., de la que usted es socio, y le convocamos de acuerdo con lo previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales.

La junta general de socios se celebrará en [CALLE, NÚMERO Y LOCALIDAD], y tendrá lugar, en primera convocatoria, el día [FECHA], a las [HORA] horas y, en segunda convocatoria, el día [FECHA], a las [HORA] horas.

La junta convocada tendrá el siguiente

ORDEN DEL DÍA

1.º) Creación de una sucursal de [DENOMINACIÓN SOCIAL], S.A. en [CALLE, NÚMERO Y LOCALIDAD], y adoptar cuantos acuerdos complementarios sean precisos.

2.º) [OTROS PUNTOS DEL ORDEN DEL DÍA, SI LOS HUBIERA]

3.º) Ruegos y preguntas.

4.º) Aprobación, en su caso, del acta de la Junta.

En su calidad de socio, y de conformidad con lo que dispone el artículo 197 del texto refundido de la Ley de Sociedades de Capital, aprobado por Real Decreto Legislativo 1/2010, de 2 de julio, tiene derecho a solicitar, hasta el séptimo día anterior al previsto para la celebración de la junta, de los administradores las informaciones o aclaraciones que estime precisas acerca de los asuntos comprendidos en el orden del día, o formular por escrito las preguntas que considere pertinentes. Los administradores estarán obligados a facilitar la información por escrito hasta el día de la celebración de la junta general.

— JUNTA UNIVERSAL

En [LOCALIDAD], calle [DOMICILIO], a [FECHA], siendo las [HORA] horas, se hallan reunidos en el domicilio social de [DENOMINACIÓN SOCIAL], S.A., la totalidad de sus socios, como consta en la lista de asistentes, que representan la totalidad del capital social, y acuerdan por unanimidad constituirse en Junta General Extraordinaria de carácter universal, al amparo de lo previsto en el art. 178 de la Ley de Sociedades de Capital y en el art. [Nº DE ARTÍCULO] de los estatutos sociales, para tratar y deliberar sobre el siguiente ORDEN DEL DÍA, que es unánimemente aceptado:

1.º) Creación de una sucursal de [DENOMINACIÓN SOCIAL], S.A. en [CALLE, NÚMERO Y LOCALIDAD], y adoptar cuantos acuerdos complementarios sean precisos.

2.º) [OTROS PUNTOS DEL ORDEN DEL DÍA, SI LOS HUBIERA]

3.º) Ruegos y preguntas.

4.º) Aprobación, en su caso, del acta de la Junta.

[CONTINÚA, EN AMBOS CASOS:]

Actúa como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario D./Dña. [NOMBRE Y APELLIDOS], designados ambos por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las acciones que poseen y/o representan cada uno de ellos:

Socios presentes:

[REPETIR EL SIGUIENTE PÁRRAFO TANTAS VECES COMO SOCIOS PRESENTES:]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE]% del total del capital social con derecho a voto.

Socios representados:

[REPETIR EL SIGUIENTE PÁRRAFO TANTAS VECES COMO SOCIOS REPRESENTADOS:]

D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTANTE], vecino/a de [CALLE, NÚMERO Y LOCALIDAD], mayor de edad y con DNI [DNI/NIE], asiste en nombre y representación, según acredita mediante [DOCUMENTO ACREDITATIVO DE LA REPRESENTACIÓN], de D./Dña. [NOMBRE Y APELLIDOS DEL SOCIO REPRESENTADO], titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE]% del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [Nº] acciones, que representan el [PORCENTAJE]% del capital social.

Todo el capital social de la compañía tiene derecho a voto.

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Junta.

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por [DETERMINAR LA MAYORÍA] se adoptan los acuerdos cuyo contenido se transcribe a continuación.

ACUERDOS

Primero.- Creación de la sucursal.

A la vista de la potestad reconocida en el art. [Nº DE ARTÍCULO] de los estatutos sociales, se acuerda la creación de una sucursal de [DENOMINACIÓN SOCIAL], S.A., de conformidad con lo siguiente:

a) Identificación: [DENOMINACIÓN O IDENTIFICACIÓN DE LA SUCURSAL].

b) Domicilio: [CALLE, NÚMERO Y LOCALIDAD].

c) Actividades que se le encomiendan: [ACTIVIDADES].

d) Identidad de los representantes nombrados con carácter permanente para la sucursal, con expresión de sus facultades: [NOMBRE Y APELLIDOS, DNI/NIE Y FACULTADES].

Segundo.- [OTROS ACUERDOS, SI LOS HUBIERA].

Tercero.- [OTROS ACUERDOS, SI LOS HUBIERA].

Cuarto.- Facultad para elevar a público.

Facultar a todos y cada uno de los miembros del Consejo de Administración para que, indistintamente, puedan comparecer ante Notario y elevar a público los presentes acuerdos, otorgando a tales efectos las escrituras públicas correspondientes, incluidas las facultades de subsanación, rectificación o aclaración, así como para realizar cuantas actuaciones sean precisas o convenientes para la eficacia de los susodichos acuerdos.

Tras todo lo cual, redactada y leída que fue el acta por el Secretario, esta es aprobada por la Junta, por unanimidad de los asistentes.

No existiendo más asuntos que tratar, se levanta la sesión.

D./Dña. [NOMBRE Y APELLIDOS], Secretario

D./Dña. [NOMBRE Y APELLIDOS], V.º B.º Presidente

D./Dña. [NOMBRE Y APELLIDOS], Asistentes

NOTAS DE USO

1. Competencia (art. 11 de la Ley de Sociedades de Capital): salvo disposición contraria de los estatutos, el órgano de administración será competente para acordar la creación, la supresión o el traslado de las sucursales. Es decir, el acuerdo de junta solo será necesario cuando así lo prevean los estatutos. La creación de una sucursal no implica la creación de una nueva sociedad o persona jurídica, por lo que no es necesario el cumplimiento de los requisitos que la ley establece para la constitución de nuevas sociedades. Sin embargo, es requisito para su inscripción posterior que la constitución esté reflejada en escritura pública (resolución de la Dirección General de los Registros y del Notariado de 11 de septiembre de 1990).

2. Lista de asistentes (art. 98 del Reglamento del Registro Mercantil): figurará al comienzo de la propia acta o se adjuntará a ella por medio de anejo firmado por el Secretario, con el visto bueno del Presidente. Igualmente podrá formarse mediante fichero o incorporarse a soporte informático; en estos casos se extenderá en la cubierta precintada del fichero o del soporte la oportuna diligencia de identificación firmada por el Secretario, con el visto bueno del Presidente.

3. Presidente y secretario (art. 191 LSC): la junta general será presidida por la persona que designen los estatutos; en su defecto, por el presidente del Consejo de Administración, y a falta de éste, por el accionista que elijan en cada caso los socios asistentes a la reunión. El presidente estará asistido por un secretario, designado también por los estatutos o por los accionistas asistentes a la junta.

4. Quórum (art. 193 LSC): la junta general de accionistas quedará válidamente constituida en primera convocatoria cuando los accionistas presentes o representados posean, al menos, el veinticinco por ciento del capital suscrito con derecho de voto; los estatutos podrán fijar un quórum superior (art. 193.1). En segunda convocatoria será válida la constitución de la junta cualquiera que sea el capital concurrente, salvo que los estatutos fijen un quórum determinado, el cual necesariamente habrá de ser inferior al que aquéllos hayan establecido o exija la ley para la primera convocatoria (art. 193.2).

5. Acta (art. 202 LSC): podrá ser aprobada por la propia junta a continuación de haberse celebrado ésta y, en su defecto, y dentro del plazo de quince días, por el presidente y dos interventores, uno en representación de la mayoría y otro por la minoría. El acta aprobada en cualquiera de estas dos formas tendrá fuerza ejecutiva a partir de la fecha de su aprobación.

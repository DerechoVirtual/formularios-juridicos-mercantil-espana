---
name: escritura-publica-transformacion-sa-sl-mer-0350
description: "Escritura pública de transformación de una SA en SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de transformación de una SA en SL

> Formulario **MER-0350** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de transformación de una SA en SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de transformación de una SA en SL” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:escritura-publica-transformacion-sa-sl-mer-0350`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (7 veces)
- [ ] MES (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] CARGO (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] FECHA
- [ ] IMPORTE
- [ ] LUGAR DE CELEBRACIÓN
- [ ] MEDIO DE IDENTIFICACIÓN
- [ ] NOMBRE DEL PERIÓDICO
- [ ] SERIE
- [ ] VOTOS A FAVOR

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

Además de las menciones exigidas para la constitución de la sociedad cuyo tipo se adopte, la escritura pública de transformación habrá de contener la relación de socios que hubieran quedado automáticamente separados y el capital que representen, así como las participaciones que se atribuyan a cada socio en la sociedad transformada

ANTE MÍ

COMPARECE D./Dña. [NOMBRE Y APELLIDOS], [OTROS DATOS]

INTERVIENE en representación de «[DENOMINACIÓN SOCIAL], S.A.»Ostenta tal representación como [CARGO]

Me aseguro de la identidad del compareciente a quien identifico [MEDIO DE IDENTIFICACIÓN], y teniendo, a mi juicio, capacidad suficiente para el otorgamiento de la presente escritura de transformación,

EXPONE

Convocatoria

Que en la página web de la sociedad [DENOMINACIÓN SOCIAL] fueron publicados sendos anuncios de convocatoria de la Junta General de «[DENOMINACIÓN SOCIAL], S.A.».

Celebración de la Junta General

Que la Junta General se celebró en [LUGAR DE CELEBRACIÓN], el día [DÍA] de [MES] de [AÑO], a las [Nº] horas, en primera [OTROS DATOS] convocatoria, con la concurrencia de [Nº] socios con derecho a voto, que representaban el [PORCENTAJE] % del capital social. Del número de socios concurrentes, -que representaban el [PORCENTAJE] % del capital –asistieron personalmente y – que representaban el [PORCENTAJE] % del capital- asistieron por representación.

En la Junta se aprobaron, con el voto favorable de [VOTOS A FAVOR], los acuerdos siguientes:

1.-Transformar la sociedad en sociedad de responsabilidad limitada, aprobar los estatutos por los que se ha de regir y asignar a cada socio las participaciones sociales que les corresponden en proporción al valor nominal de las acciones poseídas por cada uno de ellos.

2.-Aprobar el balance general de la sociedad cerrado con fecha [DÍA] de [MES] de [AÑO] junto con un informe sobre modificaciones patrimoniales significativas producidas con posterioridad.

3.-Nombrar el órgano de administración de la sociedad de responsabilidad limitada resultante de la transformación.

4.-Encomendar al administrador la publicación de los acuerdos adoptados, la elaboración del balance final y el otorgamiento de la correspondiente escritura de transformación.

Publicación

Que el acuerdo de transformación se publicó en el Boletín Oficial del Registro Mercantil, el día [DÍA] de [MES] de [AÑO]; y en el periódico [NOMBRE DEL PERIÓDICO], el día [FECHA] de [MES] de

Capital social

Se hace constar expresamente, que el capital social se encuentra íntegramente desembolsado y que han sido anulados e inutilizados los títulos representativos de las acciones.

Balance final

Que se ha formulado el correspondiente balance final, cerrado el día de ayer.

Documentos incorporados

Que todo lo expuesto resulta de los documentos correspondientes, que el compareciente me entrega en este acto y que, a su requerimiento, incorporo a la matriz de la presente escritura, que son los siguientes:

-Certificación de los acuerdos sociales.

-Balance de la sociedad cerrado el día [DÍA] de [MES] de [AÑO]

-Balance final de la sociedad cerrado el día anterior al otorgamiento de la presente escritura.

-Copias de todos los anuncios anteriormente expresados, previa verificación por mí de su exacta correspondencia con los originales, que he tenido a la vista.

-Estatutos sociales.

Que en virtud de todo lo expuesto, procede el otorgamiento de la presente escritura de transformación con arreglo a las siguientes,

ESTIPULACIONES

Primera.- Transformación

La sociedad se transforma en sociedad de responsabilidad limitada, denominada «, SR.» que se regirá por las reglas contenidas en los estatutos que el compareciente me entrega en este acto, extendidos en [Nº] folios, y que se incorporan a la presente escritura.

Segunda.- Adjudicación de acciones

Las participaciones sociales se adjudican a los socios, en proporción al valor nominal de las acciones que cada uno de ellos poseía, atribuyéndose a cada socio las participaciones siguientes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], [Nº] participaciones.

Tercera.- Gastos de transformación

Los gastos de transformación se estiman en [IMPORTE]

Cuarta.- Nombramiento del administrador

Se nombra administrador de la sociedad a [NOMBRE Y APELLIDOS] El nombramiento se realiza por el plazo estatutario de [Nº] años.

El nombrado acepta el cargo [CARGO], manifestando no estar incurso en las incompatibilidades establecidas en la legislación vigente.

OTORGAMIENTO Y AUTORIZACIÓN

Hago a los comparecientes las reservas y advertencias legales, especialmente las derivadas de la legislación fiscal, y del Registro Mercantil y de su publicidad.

Leo esta escritura a los comparecientes advirtiéndoles del derecho que tienen a hacerlo personalmente, derecho al que renuncian. Enterados de su contenido, los comparecientes hacen constar libremente su consentimiento al otorgamiento de la escritura y la firman.

Y yo, el Notario, compruebo que el consentimiento ha sido libremente prestado y se adecua a la legalidad, y del contenido de esta escritura, extendida en [Nº] folios de papel exclusivo para documentos notariales, serie [SERIE], números [Nº], DOY FE.

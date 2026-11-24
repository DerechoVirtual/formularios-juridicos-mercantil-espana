---
name: certificacion-acuerdo-transformacion-sa-sl-mer-0360
description: "Certificación del acuerdo de transformación de una SA en SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación del acuerdo de transformación de una SA en SL

> Formulario **MER-0360** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación del acuerdo de transformación de una SA en SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación del acuerdo de transformación de una SA en SL” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:certificacion-acuerdo-transformacion-sa-sl-mer-0360`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (13 veces)
- [ ] Nº (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] COLEGIO
- [ ] FECHA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MEDIO DE PUBLICACIÓN
- [ ] PORCENTAJE

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

D./Dña. [NOMBRE Y APELLIDOS], Secretario del Consejo de Administración de [DENOMINACIÓN SOCIAL], S.A., con domicilio social en [LOCALIDAD], calle [CALLE], número [NÚMERO] y C.I.F.

CERTIFICA

Que en la reunión de la Junta General Extraordinaria de la citada mercantil celebrada el pasado día [DÍA] de [MES] de [AÑO] en el domicilio social de la misma, cuya reunión fue convocada mediante anuncios publicados en el BORM número [NÚMERO] de fecha [FECHA] y [MEDIO DE PUBLICACIÓN], se aprobaron los acuerdos que literalmente dicen así:

Aprobación del balance de transformación

La junta acuerda aprobar el balance de la sociedad cerrado a [DÍA] de [MES] de [AÑO], tal y como ha sido formulado por el órgano de administración.

Examen de la propuesta de transformación de SA en SL

La junta acuerda aprobar el balance de la sociedad cerrado a [DÍA] de [MES] de [AÑO], tal y como ha sido formulado por el órgano de administración.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

○ D./Dña. [NOMBRE Y APELLIDOS], participaciones números 1 a [Nº]

Se hace constar que, en previsión de este acuerdo, se ha solicitado al Señor Registrador Mercantil de [LOCALIDAD] el nombramiento de expertos independientes que elaboren el informe estipulado sobre el patrimonio social no dinerario de la compañía.

Ratificación de órgano de administración

La junta acuerda ratificar a los integrantes del Consejo de Administración en su cargo.

• A D./Dña. [NOMBRE Y APELLIDOS], Presidente del Consejo de Administración
• A D./Dña. [NOMBRE Y APELLIDOS], Secretario
• D./Dña. [NOMBRE Y APELLIDOS], Primer Vocal
• D./Dña. [NOMBRE Y APELLIDOS], Segundo Vocal
• D./Dña. [NOMBRE Y APELLIDOS], Tercer Vocal

Aprobación de los estatutos sociales

Derivado de estos acuerdos, se decide la aprobación de los nuevos estatutos sociales, adecuados a la nueva forma social adoptada, conforme a las exigencias de la Ley de Sociedades de Capital. La redacción de los nuevos estatutos es la que sigue: ESTATUTOS SOCIALES DE "[DENOMINACIÓN SOCIAL], S.L."

Elevación a escritura pública

Se faculta al Secretario del Consejo de Administración para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando para ello las escrituras correspondientes, incluidas, en su caso, las de subsanación, aclaración o rectificación, así como para realizar cuantas operaciones fueren precisas para la plena eficacia de dichos acuerdos.»

Lista de asistentes

Que consta al principio del acta, mediante relación nominal, asistiendo [Nº] accionistas personalmente y [Nº] representados, los cuales son titulares de [Nº] acciones, cuyo nominal, en su conjunto, importa la cantidad de [IMPORTE] euros, lo que equivale al [Nº] por ciento del capital social.

Actuó como Presidente de la Junta General D./Dña. [NOMBRE Y APELLIDOS], y como Secretario D./Dña. [NOMBRE Y APELLIDOS].

Asistieron también los consejeros señores D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] Y D./Dña. [NOMBRE Y APELLIDOS].

Mayorías

Se hace constar que la aprobación del acuerdo (o acuerdos) señalados se ha realizado con el voto favorable del [PORCENTAJE] % del capital concurrente con derecho a voto.

Intervención del notario

Conforme al acuerdo del Consejo de Administración de requerir la presencia de Notario, asistió a la expresada Junta General extraordinaria de accionistas y levantó acta de la reunión el Notario del Ilustre Colegio de [COLEGIO], con residencia en [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS]. Este acta notarial tiene la consideración de acta de la Junta.

Y, para que conste, expido la presente certificación, en [LUGAR], a [DÍA] de [MES] de [AÑO].

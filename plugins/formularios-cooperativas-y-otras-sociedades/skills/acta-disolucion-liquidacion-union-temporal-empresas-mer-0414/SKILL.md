---
name: acta-disolucion-liquidacion-union-temporal-empresas-mer-0414
description: "Acta de disolución y liquidación de una unión temporal de empresas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de disolución y liquidación de una unión temporal de empresas

> Formulario **MER-0414** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de disolución y liquidación de una unión temporal de empresas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de disolución y liquidación de una unión temporal de empresas” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:acta-disolucion-liquidacion-union-temporal-empresas-mer-0414`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] FECHA (5 veces)
- [ ] NOMBRE O DENOMINACIÓN (4 veces)
- [ ] DENOMINACIÓN DE LA UTE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] LUGAR DE CELEBRACIÓN (2 veces)
- [ ] Nº ORDINAL DE LA JUNTA (2 veces)
- [ ] DESCRIPCIÓN DE LA OBRA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NIF
- [ ] NOMBRE DEL REPRESENTADO/A
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

Acuerdos adoptados por las empresas miembros de la UTE sobre ratificación del acuerdo de disolución, aprobación de la gestión y de los balances de disolución y liquidación, así como la distribución del haber social entre los socios partícipes

En [LOCALIDAD] domicilio de la Unión Temporal de Empresas [DENOMINACIÓN DE LA UTE], y siendo las [Nº] horas del día [FECHA], se celebra junta general de miembros de la Unión Temporal de Empresas [DENOMINACIÓN DE LA UTE] (Ley 18/1982) con NIF nº [NIF], estando presentes los representantes de cada una de las empresas miembros de la UTE:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

La empresa [DENOMINACIÓN SOCIAL], representada por su administrador único D./Dña. [NOMBRE Y APELLIDOS]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] en calidad de consejero delegado de [DENOMINACIÓN SOCIAL]

Asiste el gerente de la UTE, D./Dña. [NOMBRE Y APELLIDOS].

Comparecen con el siguiente

ORDEN DEL DÍA:

Primero: Ratificación de la [Nº ORDINAL DE LA JUNTA] junta extraordinaria [LUGAR DE CELEBRACIÓN] celebrada en fecha [FECHA] ante la presencia de todos los miembros de la UTE donde se adoptó la decisión de disolver y liquidar la Unión Temporal «[NOMBRE O DENOMINACIÓN]»

Segundo: Aprobación de la gestión realizada por el Gerente Único de la Unión Temporal

Tercero: Aprobación del Balance de disolución de la Unión Temporal, y la imputación de resultados a los socios.

Cuarto: Aprobación del Balance de liquidación de la Unión Temporal.

Quinto: Distribución del haber entre los socios partícipes.

Sexto: Delegación de facultades para elevar a público los acuerdos de disolución y liquidación.

Séptimo: Lectura y aprobación del acta de la junta.

Como prueba de conformidad tanto con la celebración de la presente junta como con el orden del día de la misma los representantes de cada una de las empresas de la Unión Temporal firman su asistencia:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

Seguidamente, se adoptan los siguientes

ACUERDOS:

Primero.- Ratificación de la [Nº ORDINAL DE LA JUNTA] junta extraordinaria [LUGAR DE CELEBRACIÓN] celebrada en fecha [FECHA] ante la presencia de todos los miembros de la UTE donde se adoptó la decisión de disolver y liquidar la Unión Temporal «[NOMBRE O DENOMINACIÓN]»

Se acuerda por las empresas integrantes proceder a la disolución de «[NOMBRE O DENOMINACIÓN]» UTE, debido a;

— la finalización de la ejecución de la obra de [DESCRIPCIÓN DE LA OBRA] causa por la cual única y exclusivamente se constituyó la citada UTE y
—- la entrega de la obra según se acredita en el acta de recepción expedida por el Ayuntamiento de [LOCALIDAD] en fecha [FECHA] (Se adjunta como Anexo 1 a esta acta)

Segundo.- Aprobación de la gestión realizada por el Gerente Único de la Unión Temporal

La Gestión realizada por D./Dña. [NOMBRE Y APELLIDOS] Gerente único de la UTE y el balance de fin de ejercicio, así como la cuenta de pérdidas y ganancias son aprobadas por las empresas miembro de la «[NOMBRE O DENOMINACIÓN]» UTE

Por la presente D./Dña. [NOMBRE Y APELLIDOS] cesa en el cargo como representante de la Unión Temporal de Empresas.

Tercero.- Aprobación del Balance de disolución de la Unión Temporal, y la imputación de resultados a los socios

Se aprueba por las empresas miembros el balance de disolución, que se adjunta como anexo nº 2 a esta acta, y es firmado por los representantes de las empresas miembros de la UTE.

Cuarto.- Aprobación del Balance de liquidación de la Unión Temporal

Se aprueba por las empresas miembros:

- el balance de liquidación, que se adjunta como anexo nº 3 a este acta, y es firmado por los representantes de las empresas miembros de la UTE así como,
- las operaciones de liquidación realizadas para saldar las deudas y los créditos contraídos con terceros y vender los bienes y derechos de la UTE.
- el remanente obtenido de [IMPORTE] euros

Quinto.- Distribución del haber entre los socios partícipes

Se acuerda por las empresas miembros pagar con cargo a ese remanente los saldos que resulten a favor de cada integrante de la UTE:

Y repartir la cantidad restante entre los integrantes de la UTE en proporción a su participación:

Sexto.- Delegación de facultades para elevar a público los acuerdos de disolución y liquidación

Se aprueba por unanimidad facultar a D./Dña. [NOMBRE Y APELLIDOS] para llevar a cabo todos los trámites administrativos, o de la naturaleza que fuere, precisos para la disolución y liquidación de [DENOMINACIÓN DE LA UTE] UTE, hasta su completa extinción, incluido el otorgamiento de la oportuna escritura de disolución y extinción, asumiendo los integrantes de la UTE los gastos y honorarios precisos para tal extinción en proporción a su participación en la UTE.

Asimismo, se acuerda nombrar a D./Dña. [NOMBRE Y APELLIDOS] como depositario por el plazo de seis años de las escrituras de la Unión Temporal, cuentas anuales, Libros y soportes contables, y documentación administrativa, fiscal, laboral, comercial, financiera, de la correspondencia y de cualquier otra documentación o justificantes del tráfico de la Unión Temporal.

Séptimo.- Lectura y aprobación del acta de la junta

Y una vez suscritos los anteriores acuerdos se procede a la lectura y aprobación de esta acta que es firmada por los representantes de las empresas miembros asistentes a la junta, en [LUGAR], a [FECHA].

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

En nombre y representación de [NOMBRE DEL REPRESENTADO/A]

D./Dña. [NOMBRE Y APELLIDOS]

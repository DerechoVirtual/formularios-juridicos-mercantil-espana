---
name: acta-disolucion-liquidacion-sociedad-limitada-anonima-mer-0003
description: "Acta de disolución y liquidación de sociedad limitada o anónima unipersonal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de disolución y liquidación de sociedad limitada o anónima unipersonal

> Formulario **MER-0003** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de disolución y liquidación de sociedad limitada o anónima unipersonal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de disolución y liquidación de sociedad limitada o anónima unipersonal” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-disolucion-liquidacion-sociedad-limitada-anonima-mer-0003`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] CALLE (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] DNI/NIE
- [ ] DÍA
- [ ] IMPORTE
- [ ] MES
- [ ] NIF
- [ ] Nº
- [ ] Nº DE ACTA
- [ ] NÚMERO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 15 TRLSC

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

El acuerdo de disolución y apertura de la liquidación puede ser adoptado por el socio único, ya que ostenta la totalidad de los derechos de voto en la junta general. Este acuerdo debe constar en acta, formalizarse en escritura pública e inscribirse en el Registro Mercantil, momento a partir del cual la sociedad entra en periodo de liquidación y debe añadir a su denominación la expresión “en liquidación”

Acuerdo de disolución y liquidación: Acta [Nº DE ACTA].

En [LOCALIDAD], a las [Nº] horas del día [DÍA] de [MES] de [AÑO], en el domicilio de la sociedad “ [DENOMINACIÓN SOCIAL], [ELEGIR: SRLU / SAU.”] situado en el señalado municipio, calle [CALLE], número [NÚMERO], D./Dña. [NOMBRE Y APELLIDOS] con DNI [DNI/NIE], actuando personalmente y por sí mismo titular del 100% del capital social y, por tanto, como Socio Único de la [ELEGIR: SRLU / SAU.”], ejerciendo las funciones propias de la Junta General de Socios, adopta las siguientes decisiones:

Decisiones

Primero.- Acuerda la disolución y liquidación de la Sociedad “ [DENOMINACIÓN SOCIAL], [ELEGIR: SRLU / SAU.”].”, la cual durante el tiempo que dure la disolución añadirá a su denominación social la frase "EN LIQUIDACION"

Segundo.- Acuerda el cese como administrador de la compañía de D./Dña. [NOMBRE Y APELLIDOS] relevándolo de su expresado cargo, con agradecimiento por los servicios prestados y con expresa aprobación de su gestión.

Tercero.- Nombra liquidador único de la Sociedad al hasta ahora administrador D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], titular del NIF nº. [NIF], quien presente en este mismo acto manifiesta aceptar el cargo, prometiendo desempeñarlo bien y fielmente, así como no hallarse incurso en causa de incompatibilidad legal o estatutaria alguna.

Cuarto.- La sociedad queda liquidada de conformidad con los siguientes extremos:

1º) Balance final.

Se aprueba el balance final de liquidación presentado por los liquidadores, que se une a la presente acta como Anexo I

2º) Cuota de liquidación

Se fija la cuota de liquidación en la suma de [IMPORTE] euros por [ELEGIR: participación / acción], correspondiente a cada una de las [ELEGIR: participaciónes / acciónes] que integran el total capital social de la compañía, las cuales se encuentran todas ellas liberadas.

3º) Reparto de la cuota de liquidación.

Se aprueba la división del remanente social determinando el abono de la cuota de liquidación correspondiente a cada [ELEGIR: participación / acción] mediante [ÓRGANO]

Quinto.- Se faculta expresamente al liquidador de la Sociedad D./Dña. [NOMBRE Y APELLIDOS] para que eleve a públicos los presentes acuerdos, otorgando cuantos documentos sean necesarios a tal fin; solicite la cancelación registral de la sociedad, así como para que subsane, aclare, complemente o rectifique el contenido de los mismos, de acuerdo con la calificación del Registro Mercantil; proceda al depósito de los libros y la documentación pertinente ante el citado Registro Mercantil, y a la publicación de los diferentes acuerdos en el Boletín Oficial del Registro y los periódicos oportunos.

No habiendo más asuntos que tratar por el Socio Único, las mencionadas decisiones adoptadas se consignan en la presente acta de conformidad con lo dispuesto en el art. 15 TRLSC

Fdo. EL SOCIO ÚNICO

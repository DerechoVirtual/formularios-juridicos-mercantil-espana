---
name: contrato-cesion-derechos-explotacion-obra-autor-mer-0745
description: "Contrato de cesión de derechos de explotación de una obra por su autor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cesión de derechos de explotación de una obra por su autor

> Formulario **MER-0745** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cesión de derechos de explotación de una obra por su autor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cesión de derechos de explotación de una obra por su autor” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-cesion-derechos-explotacion-obra-autor-mer-0745`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NÚMERO (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FOLIO (2 veces)
- [ ] INSCRIPCIÓN (2 veces)
- [ ] MES (2 veces)
- [ ] NIF (2 veces)
- [ ] SECCIÓN (2 veces)
- [ ] TOMO (2 veces)
- [ ] CALLE
- [ ] CARGO
- [ ] FECHA
- [ ] IDIOMA
- [ ] MATERIAL DE LAS TAPAS
- [ ] NIF/DNI
- [ ] NOMBRE DEL NOTARIO
- [ ] PLAZO
- [ ] PROVINCIA
- [ ] TIPO DE LETRA

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

En la ciudad de [LOCALIDAD], a [FECHA]

REUNIDOS

De una parte, don/doña [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], vecindad civil común y provisto de NIF número [NIF], en adelante el AUTOR.

De otra parte, don/doña [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], vecindad civil común y provista de NIF número [NIF], en adelante el EDITOR.

O

Don/doña [NOMBRE Y APELLIDOS], en nombre y representación de la mercantil "" y en calidad de apoderado [CARGO], cuya representación acredita mediante copia de la escritura de poder otorgada el día [DÍA] de [MES] de [AÑO] ante el Notario de [LOCALIDAD], Don [NOMBRE DEL NOTARIO] bajo el número [NÚMERO] de su protocolo, inscritos dichos poderes en el Registro Mercantil Provincial de [PROVINCIA] al tomo [TOMO], folio [FOLIO], sección [SECCIÓN], hoja número [NÚMERO], inscripción [INSCRIPCIÓN]. La mencionada sociedad tiene su domicilio social en [LOCALIDAD] calle [CALLE], número [NÚMERO], e inscrita en el Registro Mercantil de [LOCALIDAD], al tomo [TOMO], folio [FOLIO], sección [SECCIÓN], hoja número [NÚMERO], inscripción [INSCRIPCIÓN] y con C.I.F. [NIF/DNI]

Manifiestan

PRIMERO.- Que don/doña [NOMBRE Y APELLIDOS] es autor y titular de la totalidad de los derechos sobre la obra literaria cuyo título es "".

SEGUNDO.- Que don/doña [NOMBRE Y APELLIDOS] está interesado/a en la adquisición de los derechos de los que es titular el autor sobre la mencionada obra.

Por tal motivo ambas partes en su propio nombre y derecho, libremente y de común acuerdo convienen en otorgar el presente CONTRATO DE CESION DE DERECHOS DE AUTOR con arreglo a las siguientes

ESTIPULACIONES

Que don/doña [NOMBRE Y APELLIDOS] cede a don/doña [NOMBRE Y APELLIDOS] los derechos en exclusiva para la impresión en lengua [IDIOMA] de la mencionada obra.

En este acto el autor hace entrega del original de la obra, que el editor manifiesta conocer encontrándose a su plena satisfacción.

Dicha obra consta de índice, dedicatoria y texto, con una extensión total de [Nº] páginas tamaño folio, mecanografiado a espacio sencillo.

El precio de la cesión es de [IMPORTE] euros, pagaderos en dos plazos:

1º El primero en este acto, mediante la entrega de cheque nominativo por importe de la mitad de la totalidad del precio de la cesión, es decir, [IMPORTE] euros.

2º y el segundo, [IMPORTE] euros en el momento de la publicación y salida a la venta de la obra.

El autor se compromete a efectuar tantas correcciones o pruebas como le fuera requerido por el editor.

La salida a la venta de la obra no será en ningún caso, salvo caso fortuito o fuerza mayor, en fecha posterior al [DÍA] de [MES] de [AÑO], previo visto bueno del autor.

La obra se editará exclusivamente en papel y el número de ejemplares mínimo será de [Nº] y máximo de [PLAZO]. La letra a utilizar será [TIPO DE LETRA]. Los materiales a emplear en los ejemplares serán: para el papel y [MATERIAL DE LAS TAPAS] para las tapas o encuadernación.

La publicación se realizará a riesgo y ventura del editor, corriendo éste con los gastos derivados de impresión, publicidad, distribución, etc. sin que se facture nada por tales conceptos al cedente quien obtendrá el precio de la cesión con independencia del resultado de la comercialización de la edición.

El cedente tendrá derecho a la entrega de [Nº] ejemplares por el editor sin contraprestación. En ningún caso estos ejemplares podrán ser destinados al comercio o venta.

El editor podrá realizar sucesivas ediciones de la obra.

Las Partes acuerdan que las cesiones efectuadas en los anteriores apartados se realizan sin la facultad de emplear los derechos cedidos para el entrenamiento, alimentación o aprendizaje automático de ningún sistema de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robóticos, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología disruptiva relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). De tal manera que, el uso de los derechos cedidos por mor del presente Contrato para los enunciados usos constituirá un incumplimiento sustancial del mismo.

El PRODUCTOR habrá de respetar el compromiso adquirido en virtud de la anterior Estipulación en los contratos, negocios y relaciones jurídicas que mantenga con terceros, sean personas físicas o jurídicas, adoptando todas las medidas necesarias a tal fin e incluyendo, si fuese necesario, previsiones escritas en los contratos que celebre con estos terceros.

El/la autor/a responde frente al Editor/a de la autoría y originalidad de la obra, que son de su exclusividad responsabilidad; en consecuencia, el Editor/a no responde frente a cualquier reclamación efectuada por terceros en relación a las mismas.

Además se compromete a, en la elaboración de la Obra y en todos los materiales relacionados con la misma, no hacer uso, emplear o ayudarse de sistemas de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robóticos, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). Dicho compromiso podrá ser levantado previa conformidad de las partes por escrito cuando el uso de dicha tecnología sea testimonial.

El presente contrato estará sujeto a lo establecido en el mismo y para lo no previsto y con carácter subsidiario a lo dispuesto por el Texto Refundido de la Ley de Propiedad Intelectual aprobado por el Real Decreto Legislativo 1/1996, de 12 abril.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Para la resolución de cualquier conflicto derivado del presente contrato las partes con renuncia expresa a cualquier fuero que pudiera corresponderles, se someterá a los Tribunales de

En prueba de conformidad las personas reseñadas en el encabezamiento firman por duplicado ejemplar, el presente documento y a un solo efecto, en el lugar y fecha consignados al principio de este escrito.

Fdo. El editor	Fdo. El autor

---
name: contrato-cesion-licencia-no-exclusiva-derechos-autor-mer-0719
description: "Contrato de cesión o licencia no exclusiva de derechos de autor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cesión o licencia no exclusiva de derechos de autor

> Formulario **MER-0719** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cesión o licencia no exclusiva de derechos de autor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cesión o licencia no exclusiva de derechos de autor” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-cesion-licencia-no-exclusiva-derechos-autor-mer-0719`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] IMPORTE
- [ ] NIF
- [ ] Nº
- [ ] ÁMBITO TERRITORIAL

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

REUNIDOS

De una parte, D. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE], que actúa en nombre y representación de la entidad mercantil [DENOMINACIÓN SOCIAL], con domicilio social en [LOCALIDAD], CIF [NIF], en adelante mencionada como CESIONARIO, y

De otra parte, D. [NOMBRE Y APELLIDOS], que obra en su propio nombre y derecho, con DNI [DNI/NIE]

[NOMBRE Y APELLIDOS], y domicilio en [LOCALIDAD], en adelante mencionado como CEDENTE.

Ambas partes, reconociéndose mutuamente la capacidad legal necesaria para otorgar el presente contrato,

[ELEGIR UNA OPCIÓN: Manifiestan / Condición de heredero / Entidad titular]

Primera

El CEDENTE garantiza ser el titular legítimo y pleno de todos los derechos de explotación sobre la OBRA objeto de este contrato, y cede al CESIONARIO los derechos de

La cesión tiene carácter no exclusivo y sólo se considera a los efectos indicados en la cláusula anterior, quedando en posesión del autor las facultades morales y patrimoniales para cualquier otra utilización de su obra.

Las Partes acuerdan que las cesiones efectuadas en los anteriores apartados se realizan sin la facultad de emplear los derechos cedidos para el entrenamiento, alimentación o aprendizaje automático de ningún sistema de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robóticos, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología disruptiva relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). De tal manera que, el uso de los derechos cedidos por mor del presente Contrato para los enunciados usos constituirá un incumplimiento sustancial del mismo. E CESIONARIO habrá de respetar el compromiso adquirido en virtud de la anterior Estipulación en los contratos, negocios y relaciones jurídicas que mantenga con terceros, sean personas físicas o jurídicas, adoptando todas las medidas necesarias a tal fin e incluyendo, si fuese necesario, previsiones escritas en los contratos que celebre con estos terceros.

La cesión de los derechos y modalidades de explotación indicados se hace con carácter no exclusivo para la explotación comercial en [ÁMBITO TERRITORIAL]

El CEDENTE entregará al CESIONARIO una copia de la obra en el plazo de un mes a partir de la fecha en que se firme el presente contrato. El CESIONARIO se compromete a reproducir íntegramente la obra según la entregue el CEDENTE en la forma y para los fines convenidos en este contrato.

El CEDENTE responde ante el CESIONARIO de la autoría y originalidad de la OBRA y del ejercicio pacífico de los derechos que cede mediante el presente contrato. A estos efectos, el CEDENTE manifiesta que la OBRA no vulnera derechos de terceros. A este respecto, el CEDENTE se hace responsable frente al CESIONARIO de todas las cargas pecuniarias que pudieran derivarse para el mismo a favor de terceros con motivo de acciones, reclamaciones o conflictos derivados del incumplimiento de este contrato por su parte.

El CESIONARIO se compromete a hacer figurar el nombre del AUTOR de la OBRA (y, en su caso, del CEDENTE, si fuera distinto al autor) de forma destacada en todos los ejemplares de la OBRA, y a incluir la mención internacional de reserva de propiedad intelectual (c) seguida del nombre y apellidos o seudónimo del AUTOR (y, en su caso, del CEDENTE, si fuera distinto del autor) y el año de la publicación.

En concepto de remuneración el CEDENTE percibe la cantidad de [IMPORTE] euros, que se hacen entrega con la firma de este contrato. La remuneración indicada se ha establecido a tanto alzado al amparo de la excepción al principio general de remuneración proporcional prevista en los artículos 46.2.c) y 46.2.d).4º del Texto Refundido de la Ley de Propiedad Intelectual de 1996.

El presente contrato tendrá una duración de [Nº] años, a contar desde su firma por las partes.

El cesionario no podrá ceder los derechos adquiridos sobre la OBRA a terceras personas sin el consentimiento expreso del ilustrador. No será necesario el consentimiento del CEDENTE cuando la transmisión tenga lugar como consecuencia de la disolución o el cambio de titularidad de la empresa cesionaria incluyendo operaciones fusión, escisión total o parcial, operaciones de cesión global de activo y pasivo o de segregación patrimonial.

Estipulación facultativa, en función de la naturaleza del cesionario:

A estos efectos, como quiera que el EDITOR se haya constituido en sociedad anónima (o sociedad de responsabilidad limitada), no se considerará que existe transmisión de empresa cuando los actuales titulares de las acciones (o participaciones sociales) de la entidad CESIONARIA de este contrato transmitan la totalidad de las acciones (o participaciones sociales) a uno o varios terceros por cualquier medio reconocido en Derecho. Tampoco se entenderá producida la transmisión de la empresa si el CESIONARIO decide transformarse en sociedad de responsabilidad limitada (o sociedad anónima) o en cualquier otra entidad con personalidad jurídica reconocida por el Derecho.

El incumplimiento por el CESIONARIO de cualquiera de las obligaciones estipuladas en este contrato, permitirá al CEDENTE instar la resolución del mismo mediante notificación por escrito al CESIONARIO en su domicilio. El CEDENTE hará suyas, en concepto de indemnización, las cantidades que hubiera percibido del CESIONARIO, sin perjuicio de que pueda reclamar indemnizaciones mayores si resultare procedente.

Ambas partes se someten, para cualquier diferencia que pudiera surgir de la interpretación y cumplimiento de presente Contrato, a la jurisdicción y competencia de los Tribunales de [LOCALIDAD], renunciando a su fuero propio, caso de ser otro. No obstante, las partes podrán acordar puntualmente, en documento aparte y para cada posible controversia que pudiera surgir como consecuencia de la interpretación y ejecución del presente contrato, someterse a un arbitraje, de conformidad con la legislación vigente en España en materia de arbitraje, designando de común acuerdo un árbitro único de entre profesionales del sector de la propiedad intelectual.

El presente contrato se extiende por duplicado, quedando una copia en poder del CEDENTE y otra en poder del CESIONARIO.

En prueba de conformidad, y a un solo efecto, los comparecientes firman en el lugar y fecha abajo reseñados.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

EL CEDENTE	EL CESIONARIO

---
name: contrato-cesion-licencia-exclusiva-derechos-autor-mer-0716
description: "Contrato de cesión o licencia exclusiva de derechos de autor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cesión o licencia exclusiva de derechos de autor

> Formulario **MER-0716** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cesión o licencia exclusiva de derechos de autor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cesión o licencia exclusiva de derechos de autor” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-cesion-licencia-exclusiva-derechos-autor-mer-0716`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DESCRIPCIÓN DE LA OBRA (2 veces)
- [ ] MODALIDADES DE EXPLOTACIÓN (2 veces)
- [ ] TÍTULO DE LA OBRA (2 veces)
- [ ] DNI/NIE
- [ ] NIF
- [ ] NIF/DNI
- [ ] NOMBRE DEL CAUSANTE
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

CONTRATO DE CESIÓN O LICENCIA DE EXPLOTACIÓN EXCLUSIVA DE DERECHOS DE AUTOR

REUNIDOS

De una parte, D. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE], que actúa en nombre y representación de la entidad mercantil [DENOMINACIÓN SOCIAL], con domicilio social en [LOCALIDAD], CIF [NIF], en adelante mencionada como CESIONARIO, y

De otra parte, D. [NOMBRE Y APELLIDOS], que obra en su propio nombre y derecho, con DNI [NIF/DNI]

[NOMBRE Y APELLIDOS], y domicilio en [LOCALIDAD], en adelante mencionado como AUTOR o CEDENTE.

Ambas partes, reconociéndose mutuamente la capacidad legal necesaria para otorgar el presente contrato,

MANIFIESTAN Y ACUERDAN

I. Que D. es autor de la obra [DESCRIPCIÓN DE LA OBRA], que lleva por título [TÍTULO DE LA OBRA], en lo sucesivo la OBRA, y titular en pleno dominio de los derechos morales y patrimoniales sobre la misma.

(Alternativa: Que, en su condición de heredero de [NOMBRE DEL CAUSANTE], D. es titular de los derechos de explotación de la obra [DESCRIPCIÓN DE LA OBRA], que lleva por título [TÍTULO DE LA OBRA], (en lo sucesivo la OBRA).

II. Que la entidad [DENOMINACIÓN SOCIAL] se halla interesada en adquirir los derechos de explotación necesarios para [MODALIDADES DE EXPLOTACIÓN] de la OBRA, en las condiciones que se exponen a continuación.

III. Que, en méritos de todo lo anterior, ambas partes, reconociéndose la capacidad legal suficiente, celebran el presente contrato de licencia en exclusiva de acuerdo con las siguientes

CLÁUSULAS

El AUTOR garantiza ser el titular legítimo y pleno de todos los derechos de explotación sobre la OBRA objeto de este contrato, y cede al CESIONARIO los derechos de [MODALIDADES DE EXPLOTACIÓN].

La cesión de los derechos y modalidades de explotación indicados se hace con carácter exclusivo para la explotación comercial en [ÁMBITO TERRITORIAL]

El presente contrato tendrá una duración de [Nº] años, a contar desde su firma por ambas partes.

El AUTOR responde ante el CESIONARIO de la autoría y originalidad de la OBRA y del ejercicio pacífico de los derechos que cede mediante el presente contrato. A estos efectos, el AUTOR manifiesta que la OBRA no vulnera derechos de terceros. Asimismo manifiesta que no tiene contraídos ni contraerá compromisos o gravámenes de ninguna especie que atenten contra los derechos que al CESIONARIO o terceros le correspondan, de acuerdo con lo estipulado en este contrato. A este respecto, el AUTOR se hace responsable frente al CESIONARIO de todas las cargas pecuniarias que pudieran derivarse para el mismo a favor de terceros con motivo de acciones, reclamaciones o conflictos derivados del incumplimiento de este contrato por parte del AUTOR.

Además el AUTOR garantiza que en la elaboración de la Obra y en todos los materiales relacionados con la misma, no ha hecho uso, empleado o se ha ayudado de sistemas de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robóticos, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). Dicho compromiso podrá ser levantado previa conformidad de las partes por escrito cuando el uso de dicha tecnología sea testimonial.

El CESIONARIO se compromete a respetar los derechos morales del AUTOR y a poner en conocimiento de éste cualquier infracción de los mismos que pudiera ser realizada por terceros. En particular, el CESIONARIO se obliga a que figure el nombre del AUTOR de forma destacada en todos los ejemplares de la OBRA que publique por sí mismo o a través de terceros licenciatarios, y a incluir la mención internacional de reserva de propiedad intelectual (c) seguida del nombre y apellidos o seudónimo del AUTOR y el año de la publicación, y a observar, en su caso, las formalidades administrativas requeridas para la circulación de la OBRA; en particular el depósito legal de la OBRA.

Además las Partes acuerdan que las cesiones efectuadas en los anteriores apartados se realizan sin la facultad de emplear los derechos cedidos para el entrenamiento, alimentación o aprendizaje automático de ningún sistema de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robóticos, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología disruptiva relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). De tal manera que, el uso de los derechos cedidos por mor del presente Contrato para los enunciados usos constituirá un incumplimiento sustancial del mismo. El CESIONARIO habrá de respetar el compromiso adquirido en virtud de la anterior Estipulación en los contratos, negocios y relaciones jurídicas que mantenga con terceros, sean personas físicas o jurídicas, adoptando todas las medidas necesarias a tal fin e incluyendo, si fuese necesario, previsiones escritas en los contratos que celebre con estos terceros.

[ELEGIR UNA OPCIÓN: Sexta / Reproducción de ejemplares / Poner la obra a disposición del público / — y además elegir: Séptima / Poner a la venta / Poner la obra a disposición del público]

Con independencia de las facultades del AUTOR para perseguir cualquier vulneración de sus derechos, el CESIONARIO podrá perseguir las infracciones que afecten a las facultades de explotación que le han sido otorgadas por medio del presente contrato. En consecuencia, en los supuestos de infracción podrá llevar a cabo las acciones judiciales y extrajudiciales que tenga por conveniente, comprometiéndose el AUTOR a prestar su colaboración en tales reclamaciones. Los costes derivados de las mismas serán sufragadas por el CESIONARIO.

AUTOR y CESIONARIO podrán acordar el ejercicio conjunto de acciones judiciales en defensa de sus derechos, así como, en su caso, la contratación de asesoramiento jurídico a tales fines. En tales casos, las indemnizaciones que pudieran percibirse con motivo de la infracción de los derechos de explotación cedidos se repartirán al [PORCENTAJE] % entre AUTOR y CESIONARIO. Si las indemnizaciones derivan de infracciones a los derechos morales, corresponderán en exclusiva al AUTOR, salvo pacto en contrario supeditado a la asunción de gastos de asesoramiento y defensa jurídica por el CESIONARIO en la proporción que pudiera pactarse.

[ELEGIR UNA OPCIÓN: Noveva / Porcentaje precio de venta / Porcentaje descarga en línea / — y además elegir: Cláusula facultativa / Remuneración a tanto alzado / Remuneración mixta fija / Remuneración mixta variable / — y además elegir: Décima / Número de ejemplares / Número de descargas]

Durante la vigencia del presente contrato, el AUTOR autoriza al CESIONARIO para ceder a terceros de forma subsidiaria y no exclusiva (sublicencias) los derechos de explotación de la OBRA objeto de este contrato, con vistas a su explotación en la modalidad prevista en cualquiera de los territorios autorizados.

El resultado económico de estos acuerdos de cesión subsidiaria o sublicencias con terceros se distribuirán en la proporción del [PORCENTAJE] % para el CESIONARIO y el [PORCENTAJE] % para el AUTOR. A estos efectos, el CESIONARIO se compromete a enviar una copia del contrato de cesión subsidiaria o sublicencia al AUTOR y a liquidar y abonar los derechos indicados más arriba dentro de los 90 días siguientes a la fecha de cobro de los mismos por el CESIONARIO.

(Alternativa: Si durante la vigencia del presente contrato, el CESIONARIO quisiera autorizar a terceros [sublicencias] para la explotación subsidiaria de los derechos de explotación de la OBRA objeto de este contrato en cualquiera de los territorios autorizados, deberá obtener previamente la autorización expresa y por escrito del AUTOR. AUTOR y CESIONA- RIO se pondrán de acuerdo en cada caso en la remuneración que proceda para el primero, como consecuencia de la explotación efectuada por terceros con la autorización del CESIO- NARIO).

[ELEGIR UNA OPCIÓN: Duodécima / Liquidación de ventas / Liquidación de descargas]

En todas las cantidades que se paguen por anticipos o derechos se efectuarán las retenciones que de conformidad a la normativa fiscal sean aplicables. El AUTOR autoriza al CESIONARIO a recibir -para reintegrársela a aquél- cualquier suma de dinero que deba a ser abonada al AUTOR por un tercero de acuerdo con el presente contrato.

El AUTOR faculta expresamente al CESIONARIO para la detracción, declaración e ingreso en el Tesoro Público de aquellas cantidades que por cualquier concepto impositivo hubiera de satisfacer, derivadas de los rendimientos de la propiedad intelectual objeto de este contrato, en todos aquellos impuestos o gravámenes en que el CESIONARIO tenga, por disposición legal, la condición de sustituto del AUTOR como contribuyente.

El CESIONARIO sólo podrá transmitir plenamente a otra persona física o jurídica los derechos que se le ceden por este contrato para la explotación de la OBRA con el consentimiento expreso del AUTOR expresado por escrito.

No será necesario el consentimiento del AUTOR cuando la transmisión tenga lugar como consecuencia de la disolución o el cambio de titularidad de la empresa cesionaria, incluyendo operaciones de fusión, escisión total o parcial, operaciones de cesión global de activo y pasivo o de segregación patrimonial.

Estipulación facultativa, en función de la naturaleza del cesionario:

A estos efectos, como quiera que el EDITOR se haya constituido en sociedad anónima (o sociedad de responsabilidad limitada), no se considerará que existe transmisión de empresa cuando los actuales titulares de las acciones (o participaciones sociales) de la entidad CESIONARIA de este contrato transmitan la totalidad de las acciones (o participaciones sociales) a uno o varios terceros por cualquier medio reconocido en Derecho. Tampoco se entenderá producida la transmisión de la empresa si el CESIONARIO decide transformarse en sociedad de responsabilidad limitada (o sociedad anónima) o en cualquier otra entidad con personalidad jurídica reconocida por el Derecho.

El incumplimiento por el CESIONARIO de cualquiera de las obligaciones estipuladas en este contrato, permitirá al AUTOR instar la resolución del mismo mediante notificación por escrito al CESIONARIO en su domicilio. El AUTOR hará suyas, en concepto de indemnización, las cantidades que hubiera percibido del CESIONARIO, sin perjuicio de que pueda reclamar indemnizaciones mayores si resultare procedente.

Ambas partes se someten, para cualquier diferencia que pudiera surgir de la interpretación y cumplimiento de presente Contrato, a la jurisdicción y competencia de los Juzgados y Tribunales de [LOCALIDAD], renunciando a su fuero propio, caso de ser otro. No obstante, las partes podrán acordar puntualmente, en documento aparte y para cada posible controversia que pudiera surgir como consecuencia de la interpretación y ejecución del presente contrato, someterse a un arbitraje, de conformidad con la legislación vigente en España en la materia, designando de común acuerdo un árbitro único de entre profesionales del sector de la propiedad intelectual.

El AUTOR y el CESIONARIO podrán compelerse recíprocamente para elevar a escritura pública el presente contrato, corriendo los gastos que se originen al respecto por cuenta de quién lo hubiera solicitado.

No será efectiva ninguna enmienda, modificación, alteración o renuncia a las disposiciones del presente contrato salvo que se realice por escrito y sea firmada por ambas partes o, en su caso, por la parte que renuncie a alguno de sus derechos, haciéndose constar como anexo a este documento. Si el contrato se hubiera elevado a público, también deberá revestir forma pública cualquier enmienda, modificación, alteración o renuncia del mismo, corriendo los gastos por cuenta de quien hubiera promovido la misma.

Este documento y sus posibles anexos representan la única relación contractual completa y válida entre las partes sobre el objeto del mismo, siendo ineficaz cualquier correspondencia previa, carta de intención o acuerdos verbales entre las partes.

El presente contrato se otorga en 2 ejemplares, pero en todo caso a un solo efecto, quedando un ejemplar en poder de cada parte. Las partes podrán, de mutuo acuerdo, expresado por escrito y que conste como anexo a este documento, nombrar a un tercera persona para que actúe como depositario de un tercer ejemplar para los casos de pérdida o conflictos sobre el contenido auténtico del contrato.

Y en prueba de conformidad con cuanto antecede, suscriben el presente contrato, por duplicado, en el lugar y fecha arriba indicados.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

AUTOR [NOMBRE Y APELLIDOS] CESIONARIO

---
name: contrato-representacion-futbolista-profesional-agente-mer-0479
description: "Contrato de representación de un futbolista profesional por su agente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de representación de un futbolista profesional por su agente

> Formulario **MER-0479** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de representación de un futbolista profesional por su agente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de representación de un futbolista profesional por su agente” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-representacion-futbolista-profesional-agente-mer-0479`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] PLAZO (4 veces)
- [ ] DNI/NIE Y DOMICILIO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] IMPORTE
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

Contrato por el que un representante, profesional con conocimiento y experiencia suficiente, es contratado por un deportista para que negocie contratos de patrocinio, promocione su imagen pública, gestione su patrimonio, sus obligaciones fiscales, le asesore y negocie con clubes, y se ocupe de la proyección de su carrera deportiva

En (lugar), a (fecha).

PARTES

De una parte,

[NOMBRE Y APELLIDOS], DNI y domicilio [DNI/NIE Y DOMICILIO] registrado en la Real Federación Española de Fútbol, núm. [Nº]), en adelante AGENTE.

Y de otra parte, D./Dª. [NOMBRE Y APELLIDOS], DNI y domicilio [DNI/NIE Y DOMICILIO], en adelante REPRESENTADO/A

MANIFIESTAN

Que EL/LA AGENTE está dedicado/a, entre otras actividades, a la gestión de la carrera deportiva, el asesoramiento y la representación de jugadores de fútbol.

Que EL REPRESENTADO/A es futbolista profesional, y que declarándose libre de compromisos adquiridos de objeto igual al del presente contrato, desea contratar los servicios profesionales del AGENTE a fin de que le asesore y asista en la gestión de su carrera profesional.

Reconociéndose recíprocamente capacidad legal, consienten en suscribir el presente contrato de representación, por el que se acuerdan las siguientes

ESTIPULACIONES

Primera.- EL/LA REPRESENTADO/A, con la aceptación del AGENTE, manifestada a la firma del presente contrato, nombra a éste como su representante y le encomienda la negociación, búsqueda y gestión de cuantas actividades remuneradas contribuyan al progreso de su carrera deportiva como futbolista profesional, y en particular negociando todo tipo de contratos entre EL/LA REPRESENTADO/A y cualquier entidad deportiva, incluyendo traspasos y renovaciones de cuantos contratos se hayan formalizado con carácter previo a la firma del presente contrato.

Segunda.- EL/LA REPRESENTADO/A otorga al AGENTE, que acepta a la fIrma del presente contrato, el mandato de buscar, negociar y realizar cuantas gestiones sean precisas para ofrecer al REPRESENTADO contratos de patrocinio y/o publicitarios que sean de su interés.

Tercera.- EL/LA AGENTE no contraerá ningún compromiso en nombre del REPRESENTADO/A con terceros, debiendo todos ellos ser previa y expresamente aceptados y firmados por éste.

Cuarta. La duración del presente contrato será de [PLAZO], y entrará en vigor a partir del día de la firma.

El presente contrato se renovará automáticamente por el mismo período si ninguna de las partes comunica a la otra con una antelación mínima de [PLAZO] a la fecha en que finalice su vigencia su intención de no renovar. La misma regla se aplicará a las sucesivas prórrogas.

[ELEGIR: Contraprestación]

Quinta.- El AGENTE percibirá, como contraprestación por los servicios prestados, una comisión equivalente al [PORCENTAJE] % de las cantidades brutas que anualmente perciba el deportista por todos los conceptos que tengan que ver o se relacionen con su carrera deportiva, sean honorarios, salarios, comisiones o retribuciones por los derechos de imagen.

Percibirá asimismo una comisión del [PORCENTAJE] % sobre los incrementos de los ingresos brutos del REPRESENTADO/A, entendiéndose que la comisión se aplicará únicamente sobre la diferencia entre los ingresos iniciales y los ingresos resultantes de la negociación por EL AGENTE del aumento.

(OPCIONAL) Percibirá también EL AGENTE una comisión del % sobre los ingresos procedentes de los contratos de patrocinio y/o publicitarios comerciales que negociados por aquel suscriba el REPRESENTADO/A.

Las comisiones serán pagadas por el REPRESENTADO/A al AGENTE dentro del [PLAZO] siguiente a su cobro, respecto de los ingresos de este en concepto de prima de fichaje y traspasos, y [PLAZO] respecto de los restantes ingresos que el REPRESENTADO perciba de la entidad deportiva en la que preste sus servicios.

Opción B

Sexta.- La representación para la realización de las prestaciones señaladas en la ESTIPULACIÓN Primera se otorga por el REPRESENTADO/A con carácter exclusivo al AGENTE (puede concretarse si para España, Europa, o mundialmente).

Para el supuesto de que el jugador o club con contrato de representación en vigor y exclusividad, utilizara los servicios de otra persona o lo hiciera él mismo, a los efectos de negociar o renegociar un contrato de trabajo o cerrar un acuerdo de transferencia entre dos clubes, distinto al intermediario contratado, durante el período de vigencia de dicho acuerdo, o incumpliera cualesquiera de los acuerdos de este contrato, se establece una cláusula indemnizatoria a favor del intermediario por un importe de [IMPORTE].

Séptima.- Las partes se comprometen a respetar lo establecido en los Estatutos, Reglamentos, Circulares y decisiones de los órganos competentes de la Real Federación Española de Fútbol, de en su caso la Liga Nacional de Fútbol Profesional, así como aquellos de la FIFA, de las confederaciones y demás federaciones nacionales, incluyendo las disposiciones legales de aplicación obligatoria y demás legislación aplicable en el territorio nacional español, así como la legislación internacional y los tratados aplicables.

Octava.- En virtud de lo establecido por La Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos y Garantía de Derechos Digitales, los datos de carácter personal del REPRESENTADO/A van a ser tratados por el AGENTE, con la finalidad de mantener las oportunas relaciones comerciales y promocionales precisas para la ejecución del presente contrato. Sin perjuicio de lo anterior, EL/LA REPRESENTADO/A podrá ejercitar sus derechos dispuestos en la mencionada Ley Orgánica, notificándolo por escrito al AGENTE.

Ambas partes se comprometen a no divulgar la información y documentación confidencial referente a la otra parte de la que hayan tenido conocimiento por razón de la ejecución del presente contrato, salvo las indispensables para su cumplimiento, y a mantenerla en secreto, incluso después de la finalización del mismo, salvo con el previo consentimiento por escrito de la otra parte.

Novena.- (Opcional) Para la resolución de cualquier conflicto o discrepancia relacionada con la aplicación, ejecución e interpretación del presente contrato, las partes acuerdan someterse, con expresa renuncia a cualquier otro fuero que les pudiera corresponder, al arbitraje del Tribunal Arbitral del Fútbol, de la Liga Nacional de Fútbol Profesional, de acuerdo con el Reglamento de dicho Tribunal, por un árbitro nombrado de conformidad a dicho Reglamento, comprometiéndose al cumplimiento del laudo resultante.

(Opcional) Ambas partes, con renuncia de su propio fuero, acuerdan someterse a los efectos de la aplicación, ejecución e interpretación del presente contrato a los Juzgados y Tribunales de la ciudad de

En prueba de conformidad y obligándose al cumplimiento del presente contrato lo firman por triplicado y a un solo efecto en el lugar y fecha indicados en el encabezamiento.

EL AGENTE EL/LA REPRESENTADA

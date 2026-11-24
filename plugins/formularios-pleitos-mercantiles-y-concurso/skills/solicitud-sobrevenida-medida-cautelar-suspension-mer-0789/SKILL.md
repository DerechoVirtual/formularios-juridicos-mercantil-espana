---
name: solicitud-sobrevenida-medida-cautelar-suspension-mer-0789
description: "Solicitud sobrevenida de medida cautelar de suspensión de acuerdo social sin audiencia del demandado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud sobrevenida de medida cautelar de suspensión de acuerdo social sin audiencia del demandado

> Formulario **MER-0789** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud sobrevenida de medida cautelar de suspensión de acuerdo social sin audiencia del demandado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud sobrevenida de medida cautelar de suspensión de acuerdo social sin audiencia del demandado” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:solicitud-sobrevenida-medida-cautelar-suspension-mer-0789`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] DESCRIPCIÓN DEL ACUERDO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] NOMBRE DE LA PARTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] EXPONER LOS HECHOS (2 veces)
- [ ] MOTIVO (2 veces)
- [ ] Nº DE PROCEDIMIENTO (2 veces)
- [ ] ÓRGANO (2 veces)
- [ ] FUNDAMENTOS
- [ ] IMPORTE
- [ ] LUGAR
- [ ] Nº
- [ ] PARTE DEMANDADA
- [ ] PETICIÓN
- [ ] SEDE

## Normas que cita el formulario

- art. 727.1.º LEC
- art. 723.1 LEC
- art. 733.2 LEC
- art. 727 LEC
- art. 734 LEC
- art. 732.2 LEC

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

- Junto a «…A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

DATOS OBJETIVOS

Juicio Ordinario núm. [Nº DE PROCEDIMIENTO]/[AÑO]

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE], PLAZA N.º [Nº]

D. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, interviniendo en nombre de D. [NOMBRE Y APELLIDOS], en virtud de la representación que tengo acreditada en los autos de Juicio Ordinario núm. [Nº DE PROCEDIMIENTO]/[AÑO], seguidos a instancia de mi mandante frente a la sociedad [DENOMINACIÓN SOCIAL] ante el Tribunal comparezco bajo la dirección de la Abogada D.ª [NOMBRE Y APELLIDOS] y como mejor proceda en derecho DIGO:

Que mediante el presente escrito, en nombre de mi representado y al amparo de lo dispuesto en el artículo 733.2 en relación con el artículo 727.1.º, ambos de la LEC, solicito la adopción sin audiencia del demandado de la medida cautelar de SUSPENSIÓN DEL ACUERDO [DESCRIPCIÓN DEL ACUERDO] adoptado en la junta general ordinaria de la sociedad [DENOMINACIÓN SOCIAL] el día [DÍA] de [MES] de [AÑO], petición que dirijo frente a [PARTE DEMANDADA], ya circunstanciada, sobre la base de los siguientes

ANTECEDENTES Y PRESUPUESTOS

Mi representado formuló demanda en el ejercicio de la acción de impugnación de acuerdo social [DESCRIPCIÓN DEL ACUERDO]

Tras la presentación de la demanda ha acaecido [EXPONER LOS HECHOS]

Se da la circunstancia [EXPONER LOS HECHOS]

La apariencia de buen derecho que asiste a mi representado se desprende de [FUNDAMENTOS]

A los hechos antecedentes resultan de aplicación los siguientes

FUNDAMENTOS DE DERECHO

Competencia

Corresponde conocer esta solicitud a la Sección de lo mercantil del Tribunal de Instancia que tramita la demanda principal, en virtud de lo dispuesto en el artículo 723.1 de la LEC.

Legitimación

La legitimación activa corresponde a mi mandante en su calidad de accionista demandante [ÓRGANO] mientras [NOMBRE DE LA PARTE] ostenta la legitimación pasiva en su calidad de demandada en el proceso principal.

Trámite

La tramitación se ajustará a lo dispuesto en el artículo 733.2 de la LEC.

Otros presupuestos y fondo

La medida cautelar de suspensión de acuerdo social que se solicita aparece prevista en el ordinal 10º del artículo 727 de la LEC, por lo que tiene perfecto encaje legal.

Se cumplen los requisitos de concurrencia de apariencia de buen derecho y peligro de mora procesal, y se ofrece la caución que se deja determinada mediante OTROSÍ.

El señalamiento de la comparecencia prevista en el artículo 734 de la LEC para substanciar la tramitación de la medida interesada impediría, con toda probabilidad, la eficacia de la medida, debido a [MOTIVO] Procede, por ello, la adopción inaudita altera parte de la medida interesada, sin perjuicio de la posibilidad de que la sociedad [DENOMINACIÓN SOCIAL] pueda formalizar, si lo estima conveniente, la oposición prevista en los artículos 739 y ss. de la LEC.

Costas

Deberán ser impuestas a la demandada [NOMBRE DE LA PARTE] si se opusiere a la adopción de la medida cautelar propuesta.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL que tenga por presentado este escrito y documentos que acompaño, teniendo por formulada solicitud, posterior a demanda, de adopción sin audiencia del demandado de la medida cautelar de SUSPENSIÓN DEL ACUERDO [DESCRIPCIÓN DEL ACUERDO] adoptado en la junta general ordinaria de la sociedad [DENOMINACIÓN SOCIAL] el día [DÍA] de [MES] de [AÑO], impulsando en debida forma el trámite para su adopción previsto en el artículo 733.2 de la LEC, para [PETICIÓN], en definitiva dictar auto mediante el que se acuerde la adopción de dicha medida, y en su virtud se acuerde la suspensión del expresado acuerdo, con los demás pronunciamientos procedentes, y con imposición de costas a [NOMBRE DE LA PARTE] si se opusiere a la adopción de la medida cautelar propuesta.

Por ser Justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

OTROSÍ PRIMERO DIGO: Que ofrezco la prestación de caución mediante [ÓRGANO] por la suma de [IMPORTE] euros, cantidad que se estima suficiente y proporcionada a la finalidad que persigue, dado que [MOTIVO] Subsidiariamente, ofrezco prestar la caución que por el tribunal se señale.

OTROSÍ SEGUNDO DIGO: Que al amparo de lo dispuesto en el artículo 732.2 de la LEC, y al objeto de acreditar la concurrencia de los supuestos que autorizan la adopción de las medidas cautelares propuestas, propongo la práctica de la siguiente

PRUEBA

1.

NUEVAMENTE SUPLICO AL TRIBUNAL que tenga por ofrecida la caución antecedente, resolviendo lo necesario para su constitución y por propuesta la prueba que se deja reseñada, acordando lo necesario para su práctica. Justicia que reitero en igual lugar y fecha.

Fdº: Fdº:
Abogada	Procurador

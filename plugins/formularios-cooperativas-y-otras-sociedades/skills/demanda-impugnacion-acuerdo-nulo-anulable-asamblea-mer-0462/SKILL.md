---
name: demanda-impugnacion-acuerdo-nulo-anulable-asamblea-mer-0462
description: "Demanda de impugnación de un acuerdo nulo o anulable de la asamblea general de una cooperativa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de impugnación de un acuerdo nulo o anulable de la asamblea general de una cooperativa

> Formulario **MER-0462** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Fundamentos de derecho y súplica de una demanda de juicio ordinario por la que un socio de una cooperativa impugna un acuerdo de la Asamblea General, solicitando su declaración de nulidad o de anulabilidad (por ser contrario a la ley o lesionar el interés de la cooperativa en beneficio de uno o varios socios) y, en su caso, su suspensión.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de impugnación de un acuerdo nulo o anulable de la asamblea general de una cooperativa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de impugnación de un acuerdo nulo o anulable de la asamblea general de una cooperativa” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:demanda-impugnacion-acuerdo-nulo-anulable-asamblea-mer-0462`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] Nº (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL LETRADO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR (2 veces)
- [ ] CIVIL / ÚNICA, DE CIVIL Y DE INSTRUCCIÓN
- [ ] CONTENIDO DEL ACUERDO
- [ ] CONTENIDO DEL ACUERDO IMPUGNADO
- [ ] DENOMINACIÓN DE LA LEY
- [ ] DESCRIBIR EL ACUERDO CUYA SUSPENSIÓN SE SOLICITA
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] DOMICILIO SOCIAL
- [ ] EXPOSICIÓN DE LOS MOTIVOS DE IMPUGNACIÓN
- [ ] IMPORTE O «INDETERMINADA»
- [ ] NIF
- [ ] NOMBRE Y APELLIDOS DEL SOCIO BENEFICIADO
- [ ] NOMBRE Y APELLIDOS DEL SOCIO DEMANDANTE
- [ ] Nº DE ARTÍCULO
- [ ] Nº DE COLEGIADO
- [ ] SEDE
- [ ] UNO O VARIOS SOCIOS / TERCERO

## Normas que cita el formulario

- art. 31.5 Ley 27/1999
- art. 31.4 Ley 27/1999
- art. 253 LEC
- art. 394 LEC

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: el original solo traía los fundamentos de derecho y la súplica; el encabezamiento, la identificación de las partes y los hechos deben redactarse con arreglo al modelo general de demanda. Se incluye un encabezamiento y un bloque de hechos mínimos para que el escrito sea utilizable.
- Junto a «…de Cooperativas, en relación con el art. 207 de la Ley de Sociedades de Capital.»: si la cooperativa se rige por una ley autonómica de cooperativas, citar el precepto equivalente de esa ley.
- Junto a «…DOR] Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.

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

A LA SECCIÓN [CIVIL / ÚNICA, DE CIVIL Y DE INSTRUCCIÓN] DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL SOCIO DEMANDANTE], con DNI [DNI/NIE] y domicilio en [DOMICILIO], según acredito mediante poder que acompaño como documento n.º 1, bajo la dirección del Letrado D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que, por medio del presente escrito, formulo demanda de juicio ordinario de impugnación de acuerdos sociales contra la cooperativa [DENOMINACIÓN SOCIAL], S. Coop., con NIF [NIF] y domicilio social en [DOMICILIO SOCIAL], en base a los siguientes

HECHOS

Primero.- El demandante es socio de la cooperativa demandada desde el [FECHA].

Segundo.- El [FECHA] se celebró Asamblea General Ordinaria de [DENOMINACIÓN SOCIAL], S. Coop., en la que se adoptó el acuerdo n.º [Nº], consistente en [CONTENIDO DEL ACUERDO IMPUGNADO]. El demandante asistió a la Asamblea y [ELEGIR: hizo constar su oposición al acuerdo, según resulta del acta que se acompaña / no asistió a la Asamblea (SOLO PARA ACUERDOS NULOS)]. Se acompaña acta como documento n.º [Nº].

Tercero.- El acuerdo es contrario a la ley y lesiona el interés de la cooperativa en beneficio de [UNO O VARIOS SOCIOS / TERCERO], por los motivos siguientes: [EXPOSICIÓN DE LOS MOTIVOS DE IMPUGNACIÓN].

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA: Corresponde al Tribunal de Instancia al que me dirijo, en virtud de lo dispuesto en el art. 52.1, regla 10.ª de la Ley de Enjuiciamiento Civil, puesto que la entidad demandada tiene su domicilio social en [LOCALIDAD].

II.- PROCEDIMIENTO: Corresponde el del juicio ordinario según lo previsto en el art. 249.1.3.º de la Ley de Enjuiciamiento Civil y en el art. 31.5 de la Ley 27/1999, de 16 de julio, de Cooperativas, en relación con el art. 207 de la Ley de Sociedades de Capital.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Para anulación)

III.- ANULABILIDAD: Se trata de un acuerdo anulable por lesionar, en beneficio del socio [NOMBRE Y APELLIDOS DEL SOCIO BENEFICIADO], los intereses de la cooperativa.

IV.- LEGITIMACIÓN ACTIVA: Corresponde al demandante en su calidad de socio asistente a la Asamblea General Ordinaria de [DENOMINACIÓN SOCIAL], S. Coop., de [LOCALIDAD]. Por parte del demandante se hizo constar su oposición al acuerdo impugnado, según resulta del literal del acta acompañada, requisito exigido por la jurisprudencia para legitimar la posterior acción impugnatoria y por el artículo 31.4 de la Ley 27/1999, de 16 de julio, de Cooperativas (sentencias del Tribunal Supremo, Sala Primera, de lo Civil, de 9 de mayo de 1986, de 30 de abril de 1988 y de 30 de noviembre de 1991).

V.- PLAZO: Se interpone la demanda dentro del plazo de caducidad de los 40 días siguientes a la fecha de [ELEGIR: adopción del acuerdo / inscripción].

— (Para nulidad)

III.- NULIDAD: Se trata de un acuerdo nulo por vulnerar lo dispuesto en el artículo [Nº DE ARTÍCULO] de la Ley [DENOMINACIÓN DE LA LEY].

IV.- LEGITIMACIÓN ACTIVA: Corresponde al demandante en su calidad de [ELEGIR: socio / miembro del consejo rector / interventor / miembro del comité de recursos].

V.- PLAZO: Se interpone la demanda dentro del plazo de caducidad de un año siguiente a la fecha de [ELEGIR: adopción del acuerdo / inscripción].

VI.- FONDO DEL ASUNTO: Por la presente demanda se solicita la declaración de nulidad de los acuerdos tomados con los números [Nº], según el acta de la Asamblea General Ordinaria de fecha [FECHA] (acompañada como documento n.º [Nº] a esta demanda), como contrarios a la ley y porque lesionan el interés de la sociedad en beneficio de uno de sus socios.

VII.- CUANTÍA: Conforme al art. 253 de la LEC cifro la cuantía de la presente demanda en [IMPORTE O «INDETERMINADA»], fijación que amparo en el siguiente fundamento: [JUSTIFICAR LA CUANTÍA, CALCULADA CONFORME A LAS REGLAS LEGALES; DEBERÁN PRESENTARSE LOS DOCUMENTOS O DICTÁMENES QUE ACREDITEN EL VALOR DE LA COSA LITIGIOSA; SI NO ES POSIBLE LA DETERMINACIÓN, AUN EN FORMA RELATIVA, LA DEMANDA SE CONSIDERARÁ DE CUANTÍA INDETERMINADA].

VIII.- COSTAS: Conforme al artículo 394 de la LEC, las costas han de imponerse a la parte demandada.

SUPLICO AL TRIBUNAL DE INSTANCIA, que teniendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido en parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente a las personas designadas en el encabezamiento, dé al mismo el curso señalado en la ley y, en su día, dicte sentencia en la que, estimando íntegramente esta demanda de impugnación de acuerdo social:

a) Declare [ELEGIR: nulo / anulable] el acuerdo de la Asamblea General de [DENOMINACIÓN SOCIAL], S. Coop., tomado el día [FECHA] y consistente en [CONTENIDO DEL ACUERDO].

b) Ordene la suspensión del acuerdo: [DESCRIBIR EL ACUERDO CUYA SUSPENSIÓN SE SOLICITA]. [PARA ELLO SE PRECISA QUE LOS DEMANDANTES SEAN LOS INTERVENTORES O SOCIOS QUE REPRESENTEN, AL MENOS, UN 20% DEL TOTAL DE VOTOS SOCIALES.]

c) Condene a dicha cooperativa en todas las costas y gastos de este procedimiento.

Es de justicia que pido en [LOCALIDAD], a [FECHA].

Abogado y número de colegiado: [NOMBRE Y APELLIDOS DEL LETRADO] — Col. n.º [Nº DE COLEGIADO]

Procurador: [NOMBRE Y APELLIDOS DEL PROCURADOR]

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

---
name: demanda-impugnacion-acuerdos-sl-suspension-anotacion-mer-0801
description: "Demanda de impugnación de acuerdos de una SL con suspensión y anotación preventiva de la demanda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de impugnación de acuerdos de una SL con suspensión y anotación preventiva de la demanda

> Formulario **MER-0801** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio ordinario sobre impugnación de acuerdos sociales de una Sociedad de Responsabilidad Limitada interpuesta ante un Tribunal de Instancia (Sección de lo Mercantil) por un miembro del Consejo de Administración y socio de la misma por medio de la cual se solicita la suspensión de acuerdos aprobados por la Junta General, ordenando la nulidad de la inscripción de los mismo o la cancelación de su inscripción en el Registro Mercantil y la anotación preventiva de la demanda.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de impugnación de acuerdos de una SL con suspensión y anotación preventiva de la demanda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de impugnación de acuerdos de una SL con suspensión y anotación preventiva de la demanda” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-impugnacion-acuerdos-sl-suspension-anotacion-mer-0801`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] Nº (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] EXPONER LOS HECHOS (2 veces)
- [ ] FUNDAMENTOS (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] PETICIÓN (2 veces)
- [ ] LUGAR
- [ ] OTROS DATOS
- [ ] TÍTULO DE ADQUISICIÓN

## Normas que cita el formulario

- art. 253 LEC
- art. 727.10 LEC
- art. 732.2 LEC
- art. 727.5 LEC

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

Modelo de demanda de juicio ordinario sobre impugnación de acuerdos sociales de una Sociedad de Responsabilidad Limitada interpuesta ante un Tribunal de Instancia (Sección de lo Mercantil) por un miembro del Consejo de Administración y socio de la misma por medio de la cual se solicita la suspensión de acuerdos aprobados por la Junta General, ordenando la nulidad de la inscripción de los mismo o la cancelación de su inscripción en el Registro Mercantil y la anotación preventiva de la demanda.


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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTACIA DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], Procurador de los Tribunales, en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], según acredito mediante escritura de poder que acompaño para su unión a los autos por copia testimoniada cuya devolución del original desde este momento intereso por precisarlo para otros usos, dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho

DIGO:

Que, en la representación que ostento, interpongo demanda de juicio declarativo ordinario, sobre IMPUGNACIÓN DE ACUERDOS SOCIALES frente a la mercantil ‘ S.L.’ [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD].

A efectos del primer emplazamiento del demandado, para el caso de que no sea hallado en dicho domicilio, se designan los siguientes lugares donde podrá intentarse la comunicación, por el siguiente orden:

Fundamento la misma en los siguientes hechos y consideraciones jurídicas:

HECHOS

Primero.- El pasado día [FECHA], en su domicilio social, se celebró Junta General de socios de ‘[DENOMINACIÓN SOCIAL], S.L.’, en la que se adoptaron los siguientes acuerdos:

‘Primero:

Segundo:

Tercero: ‘.

[OPCIONAL — incluir si procede]

Por parte de mi representado se hizo constar la oposición expresa a la adopción de los citados acuerdos.

Segundo.- Mi representado ostenta la condición de miembro del consejo de administración de ‘[DENOMINACIÓN SOCIAL], S.L.’ en virtud de su nombramiento y aceptación acaecidos de manera simultánea el pasado [FECHA].

Asimismo, cuenta con la condición de socio de la citada mercantil, como titular de [Nº] participaciones sociales de la misma que se corresponden con las numeradas del [Nº] al [Nº], ambas inclusive, adquiridas en fecha [FECHA] por título [TÍTULO DE ADQUISICIÓN], y que suponen un % con respecto al capital social

Tercero.- [EXPONER LOS HECHOS]

[EXPONER LOS HECHOS]

Cuarto.- Como fundamento de los anteriores hechos se adjuntan a la presente demanda los siguientes DOCUMENTOS:

A) Con relación al HECHO PRIMERO, se adjunta como DOCUMENTO NÚM. [Nº DE DOCUMENTO]
B) En relación al HECHO SEGUNDO, se adjunta como DOCUMENTO NÚM. [Nº DE DOCUMENTO]

A los anteriores hechos, son aplicables los siguientes

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA

Corresponde a la sección de lo mercantil de este Tribunal de Instancia al que me dirijo, en virtud de lo dispuesto en el art. 52.1.regla 10ª de la Ley de Enjuiciamiento Civil (LEC) de 7 de enero de 2000, puesto que la entidad demandada tiene su domicilio social en esta capital.

II.- PROCEDIMIENTO

Corresponde el del Juicio Ordinario según lo previsto en el art. 249.1.3º de la Ley de Enjuiciamiento Civil (LEC) de 7 de enero de 2000 y en el art. 207 de la Ley de Sociedades de Capital (LSC) [FUNDAMENTOS].

III.- IMPUGNACIÓN

Por la presente demanda se solicita la impugnación de los acuerdos tomados con los números [Nº] según el acta de la Junta General de fecha [FECHA] (acompañada como documento [Nº DE DOCUMENTO] a esta demanda), como contrarios a la Ley y porque lesionan el interés de la sociedad en beneficio de uno de sus accionistas (por ejemplo).

IV.- LEGITIMACIÓN ACTIVA

En virtud de lo previsto en el art. 206 Ley de Sociedades de Capital, mi representado ostenta dicha legitimación en su calidad de miembro del consejo de administración y socio de ‘[DENOMINACIÓN SOCIAL], S.L.’.

V.- LEGITIMACIÓN PASIVA

Corresponde a la demandada, en virtud de lo previsto en el art. 206.3 Ley de Sociedades de Capital.

VI.- CUANTÍA

Conforme al art. 253 de la LEC cifro la cuantía de la presente demanda en [IMPORTE], fijación que amparo en el siguiente fundamento [FUNDAMENTOS]

VII.- POSTULACIÓN Y DEFENSA

Conforme a lo previsto en los arts. 23 y 31 de la Ley de Enjuiciamiento Civil, se presenta la demanda por medio de Procurador legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VIII.- FONDO DE LA CUESTIÓN CONTROVERTIDA

(Arts. 205 y ss. Ley de Sociedades de Capital).

En cuanto al cómputo del plazo de caducidad para la interposición de la acción, téngase en cuenta que la acción de impugnación de los acuerdos sociales caducará en el plazo de un año, salvo que tenga por objeto acuerdos que por sus circunstancias, causa o contenido resultaren contrarios al orden público, en cuyo caso la acción no caducará ni prescribirá.

El plazo de caducidad se computará desde la fecha de adopción del acuerdo si hubiera sido adoptado en junta de socios o en reunión del consejo de administración, y desde la fecha de recepción de la copia del acta si el acuerdo hubiera sido adoptado por escrito. Si el acuerdo se hubiera inscrito, el plazo de caducidad se computará desde la fecha de oponibilidad de la inscripción.

IX.- COSTAS

Conforme al artículo 394 de la L.E.C., las costas han de imponerse a la demandada.

Por lo expuesto,

SUPLICO AL TRIBUNAL. Que habiendo por presentado este escrito de demanda con los documentos que lo acompañan y copias de uno y otros, los admita y me tenga por comparecido en parte en la representación que ostento y que acreditada dejo; y por promovido juicio declarativo ordinario frente a las mercantil designada en el encabezamiento, dé al mismo el curso señalado en la ley y, en su día, dicte sentencia en la que, estimando íntegramente la demanda:

a) Declare nulos los acuerdos impugnados.
b) Ordene la inscripción de dicha nulidad en el Registro Mercantil, publicándose en extracto en el Boletín Oficial de dicho Registro.
c) Ordene la cancelación de su inscripción, así como la de los asientos [OTROS DATOS].
d) Condene a [PETICIÓN]

Todo ello con imposición de las costas del juicio a la parte demandada.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO que presentándose con el presente escrito justificación documental suficiente del derecho que se ejercita, formulo la petición de las siguientes medidas cautelares, por cuanto se consideran necesarias para asegurar la efectividad de la tutela judicial que se quiere se otorgue en la sentencia estimatoria que se dicte en este proceso, entendiendo esta representación que de no acordarse, puede verse impedida (o dificultada) por situaciones producidas durante la pendencia del proceso.

1º) SUSPENSIÓN DE LOS ACUERDOS IMPUGNADOS, en base al artículo 727.10ª de la LEC. A tales efectos mi mandante ostenta participaciones sociales que representan un % del capital social, es decir, un porcentaje superior al 5% exigido por el citado precepto de la Ley Rituaria Civil. (En su caso, téngase en cuenta el art. 732.2 LEC).
2ª) ANOTACIÓN PREVENTIVA DE LA DEMANDA EN EL REGISTRO MERCANTIL, según lo previsto en el artículo 727.5ª de la LEC y 155 a 157 del Reglamento del Registro Mercantil.

A los efectos legales procedentes, se ofrece caución por la suma de [IMPORTE] EUROS, cantidad que se considera suficiente para responder, en su caso, de los daños y perjuicios que la adopción de las medidas cautelares que se interesan pudieran causar en el patrimonio del demandado.

Por lo expuesto, y al amparo de lo previsto en los artículos 721 y siguientes, y concordantes, de la LEC,

SUPLICO AL TRIBUNAL que se tengan por hechas las anteriores manifestaciones, y habiendo quedado acreditada cumplidamente la concurrencia de los presupuestos que exige la Ley para la SUSPENSIÓN DE ACUERDOS SOCIALES IMPUGNADOS y la ANOTACIÓN PREVENTIVA de la presente demanda, que desde ahora se interesan, previos los trámites legales, incluida la audiencia de las partes, se sirva dictar resolución en la que, declarando justificada la pretensión, se acuerde la adopción de las medidas interesadas, disponiendo al efecto [PETICIÓN], por ser Justicia que reitero en el mismo lugar y fecha ut supra.

Abogado y número de colegiado:

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

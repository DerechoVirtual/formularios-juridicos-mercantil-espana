---
name: demanda-exclusion-socio-sl-participacion-igual-mer-0794
description: "Demanda de exclusión de un socio de SL con participación igual o superior al 25 por ciento. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de exclusión de un socio de SL con participación igual o superior al 25 por ciento

> Formulario **MER-0794** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda solicitando al Tribunal de Instancia (Sección de lo Mercantil) la ratificación judicial del acuerdo de exclusión como socio del demandado, acordado por la Junta general de la sociedad de responsabilidad limitada y formulando la petición de medida cautelar consistente en la anotación preventiva de la demanda. Ejercitada por la sociedad o por otro socio

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de exclusión de un socio de SL con participación igual o superior al 25 por ciento» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de exclusión de un socio de SL con participación igual o superior al 25 por ciento” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-exclusion-socio-sl-participacion-igual-mer-0794`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] CAUSA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NIF
- [ ] Nº DE ARTÍCULO
- [ ] Nº DE DOCUMENTO
- [ ] OTROS DATOS

## Normas que cita el formulario

- art. 249.1.3 LEC
- art. 249.2 LEC
- art. 352.2 Real Decreto Legislativo 1/2010
- art. 352 TRLSC
- art. 351 TRLSC
- art. 253 LEC
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

Modelo de demanda solicitando al Tribunal de Instancia (Sección de lo Mercantil) la ratificación judicial del acuerdo de exclusión como socio del demandado, acordado por la Junta general de la sociedad de responsabilidad limitada y formulando la petición de medida cautelar consistente en la anotación preventiva de la demanda. Ejercitada por la sociedad o por otro socio


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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA

D./Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de ‘[DENOMINACIÓN SOCIAL], S.L.’, según acredito mediante escritura de Poder que acompaño como documento nº 1 de los que se unen al presente escrito para su unión a los Autos mediante copia, previa su certificación por el Letrado de la Administración de Justicia al que tengo el honor de dirigirme, y cuya devolución intereso por precisarlo para otros usos, dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho,

DIGO:

Que mediante el presente escrito formulo demanda de Juicio Declarativo Ordinario contra D./Dña. [NOMBRE Y APELLIDOS], socio titular del % del capital social de [DENOMINACIÓN SOCIAL], S.L., por la que intereso la RATIFICACIÓN JUDICIAL del acuerdo de expulsión del socio demandado, con NIF [NIF] y domicilio en [LOCALIDAD].

Fundamento mis pretensiones en los siguientes

HECHOS

[ELEGIR UNA OPCIÓN: Sociedad / Socio]

Segundo.- El [FECHA], la mercantil ‘[DENOMINACIÓN SOCIAL], S.L.’ celebró Junta General extraordinaria en cuya convocatoria constaba, como punto 2º del Orden del Día, la exclusión del demandado como socio de la misma, por haber incurrido en la siguiente causa [ELEGIR: legal / estatutaria] de exclusión [CAUSA].

Acredito dicho extremo con copia de los burofax remitidos a los socios, por el que se notificó la convocatoria de Junta, de fecha [FECHA], según lo previsto en el artículo [Nº DE ARTÍCULO] de los Estatutos sociales.

La Junta se celebró en la fecha señalada al efecto, acordándose por mayoría la exclusión mencionada, y oponiéndose a la misma el demandado D./Dña. [NOMBRE Y APELLIDOS], según consta en el certificado del acta de Junta que acompaño como documento [Nº DE DOCUMENTO].

[ELEGIR UNA OPCIÓN: Sociedad / Socios]

A los presentes hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- Jurisdicción y competencia

Es competente la sección de lo Mercantil del Tribunal de Instancia del domicilio del demandado, al que se dirige la presente demanda

II.- Procedimiento

El procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley, en aplicación de lo dispuesto en los arts. 249.1.3º de la LEC, por analogía, dado que se solicita la ratificación judicial de un acuerdo social al que el socio interesado se opone (o puede también considerarse aplicable residualmente el art. 249.2 de la LEC).

III.- Legitimación activa

El art. 352.2 del Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el Texto Refundido de la Ley de Sociedades de Capital, según el cual cualquier socio que haya votado a favor del acuerdo de exclusión de un socio con capital superior al 25% del capital social está legitimado para ejercitar la acción de exclusión en nombre de la sociedad, cuando ésta no lo hubiera hecho en el plazo de un mes desde que se adoptó el acuerdo.

IV.- Legitimación pasiva

Corresponde al socio excluido y disconforme con el acuerdo, según lo previsto en el apartado 2 del art. 352 TRLSC citado.

V.- Causa de exclusión

En virtud de lo previsto en el art. 351 TRLSC, en relación con el art. de los estatutos sociales, la [CAUSA] constituye causa legítima de exclusión del socio.

VI.- Cuantía

Conforme al art. 253 de la LEC, en relación con el 251 regla 12ª del mismo texto legal, cifro la cuantía de la presente demanda en [IMPORTE] euros, que es el importe al que asciende el valor de las participaciones sociales de D./Dña. [NOMBRE Y APELLIDOS].

VII.- Postulación y defensa

Conforme a lo previsto en los arts. 23 y 31 de la Ley de Enjuiciamiento Civil, se presenta la demanda por medio de Procurador legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VIII.- Plazo

Según dispone la Sentencia de 9 de abril de 2003 de la Sala 1ª del Tribunal Supremo (Sr. Gullón Ballesteros, Europea de Derecho nº 2004111709), ‘el art. 99.2 LSRL (actual 352.2 TRLSC) silencia el plazo en que aquellos socios pueden ejercitar la acción si transcurre el del mes sin que lo haya hecho la sociedad. Si se tiene en cuenta que han de actuar por exigencia del susodicho precepto ‘en nombre de la sociedad’, no es razonable sostener que la misma tiene un plazo muy reducido para actuar por sí misma, es decir, por sus propios representantes, pero en cambio, cuando actúa a través de los socios, tiene un plazo más extenso, que sería el del Art. 947 Código de comercio. Lógicamente, el plazo debe ser el mismo. Ahora bien, el dies a quo del cómputo debe ser el día en que los actores han tenido conocimiento de que la sociedad no ha ejercitado la acción de expulsión, por aplicación de la legislación común (Art. 1.969 Cód. civ.).

A este argumento de lógica deben añadirse las atinadas consideraciones de la sentencia de primera instancia, que destaca la impropiedad de fijar un largo plazo que permita que cuestiones fundamentales para la correcta marcha de la sociedad, como la de exclusión de un socio, queden en el régimen de transitoriedad e indefinición, en contraste con la celeridad que exige el tráfico jurídico y con su seguridad. En el fondo, se trata aquí de dar eficacia a un acuerdo social de expulsión de un socio, que debe seguir en cuanto al plazo para lograrlo el mismo espíritu restrictivo que el legislador muestra en la fijación de plazos para impugnar acuerdos sociales’.

Por lo tanto, se interpone la presente demanda en plazo, puesto que no ha transcurrido un mes desde la fecha en que se adoptó el acuerdo de exclusión.

IX.- Costas

Conforme al artículo 394 de la L.E.C., las costas han de imponerse a la demandada.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL, que teniendo por presentado este escrito de demanda con sus documentos y copias, se sirva admitirlo y acordar de conformidad, teniendo por interpuesta demanda de Juicio Declarativo Ordinario contra D./Dña. [NOMBRE Y APELLIDOS], para que en su día, seguidos sean los trámites legales oportunos, se dicte sentencia por la que se decrete, estimando la presente demanda, la ratificación judicial del acuerdo de exclusión como socio del demandado, acordado por la Junta general de ‘[DENOMINACIÓN SOCIAL], S.L.’ con fecha [FECHA], por ser justicia que pido en

OTROSÍ DIGO, que en el presente procedimiento se demanda [OTROS DATOS] formulo la petición de medida cautelar consistente en la anotación preventiva de la presente demanda en la hoja correspondiente a la mercantil demandada en el Registro Mercantil de [LOCALIDAD], por cuanto se considera necesaria para asegurar la efectividad de la tutela judicial que se quiere se otorgue en la sentencia estimatoria que se dicte en este proceso, entendiendo esta representación que de no acordarse, como medida cautelar, puede verse impedida (o dificultada) por situaciones producidas durante la pendencia del proceso.

A los efectos legales procedentes, se ofrece caución por la suma de [IMPORTE] euros, cantidad que se considera suficiente para responder, en su caso, de los daños y perjuicios que la adopción de la medida cautelar que se interesa pudiera causar en el patrimonio del demandado.

Por lo expuesto, y al amparo de lo previsto en los artículos 721 y siguientes, en concreto el art. 727.5º de la LEC,

SUPLICO AL TRIBUNAL que se tengan por hechas las anteriores manifestaciones, y habiendo quedado acreditada cumplidamente la concurrencia de los presupuestos que exige la Ley para la adopción de la medida cautelar de anotación preventiva que desde ahora se interesa, previos los trámites legales, incluida la audiencia de las partes, se sirva dictar resolución en la que, declarando justificada la pretensión, se acuerde la adopción de la medida cautelar interesada, por ser justicia que reitero en el mismo lugar y fecha ut supra.

Abogado y número de colegiado:

Procurador

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

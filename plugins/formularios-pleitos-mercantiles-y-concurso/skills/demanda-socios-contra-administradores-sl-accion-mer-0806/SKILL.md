---
name: demanda-socios-contra-administradores-sl-accion-mer-0806
description: "Demanda de socios contra los administradores de una SL por la acción individual de responsabilidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de socios contra los administradores de una SL por la acción individual de responsabilidad

> Formulario **MER-0806** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de Juicio Declarativo Ordinario en ejercicio de la acción individual de responsabilidad de los administradores de una Sociedad, ejercitada por los accionistas, solicitando se declare la responsabilidad de los codemandados, condenándoles por ello solidariamente al pago de una determinada cantidad de dinero, por los daños causados a los actores.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de socios contra los administradores de una SL por la acción individual de responsabilidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de socios contra los administradores de una SL por la acción individual de responsabilidad” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-socios-contra-administradores-sl-accion-mer-0806`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (18 veces)
- [ ] IMPORTE (6 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] Nº DE DOCUMENTO (4 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] EXPONER LOS HECHOS
- [ ] FECHA DE INSCRIPCIÓN
- [ ] NIF
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] OTROS DATOS
- [ ] TOMO
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 236 LSC
- art. 1089 Código Civil
- art. 225 LSC
- art. 241 LSC
- art. 1911 Código Civil
- art. 1317 Código Civil
- art. 6 Código de Comercio
- art. 252 LEC

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

Modelo de demanda de Juicio Declarativo Ordinario en ejercicio de la acción individual de responsabilidad de los administradores de una Sociedad, ejercitada por los accionistas, solicitando se declare la responsabilidad de los codemandados, condenándoles por ello solidariamente al pago de una determinada cantidad de dinero, por los daños causados a los actores.


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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA [SEDE]

D./Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], según acredito mediante escritura de Poder que acompaño como documento nº 1 de los que se unen al presente escrito para su unión a los Autos mediante copia, previa su certificación por el Letrado de la Administración de Justicia del Tribunal al que tengo el honor de dirigirme, y cuya devolución intereso por precisarlo para otros usos, dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], ante el Tribunal comparezco y como mejor proceda en Derecho,

DIGO:

Que mediante el presente escrito formulo demanda de Juicio Declarativo Ordinario, en la que ejercito la acción INDIVIDUAL de responsabilidad de los administradores de [DENOMINACIÓN SOCIAL], S.L.’, D./Dña. [NOMBRE Y APELLIDOS] con DNI y domicilio en [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS] con DNI y domicilio en [LOCALIDAD] y D./Dña. [NOMBRE Y APELLIDOS] con DNI y domicilio en [LOCALIDAD], y contra sus respectivos cónyuges para el caso de que fueren casados, y a los solos efectos del art. 144 del Reglamento Hipotecario.

Fundamento mis pretensiones en los siguientes

HECHOS

Primero.- Mis representados son todos ellos socios de la mercantil ‘[DENOMINACIÓN SOCIAL], S.L.’, constituida el [FECHA], según consta en la escritura autorizada el [FECHA] por D./Dña. [NOMBRE Y APELLIDOS], Notario de [LOCALIDAD], su domicilio social se halla sito en la localidad de [LOCALIDAD], y fue inscrita en el Registro Mercantil nº [NÚMERO] de los de [SEDE] el [FECHA DE INSCRIPCIÓN], Tomo [TOMO], con NIF [NIF].

Acredito estos extremos con el documento nº [Nº DE DOCUMENTO] de los que se acompañan a este escrito, y consistente en copia simple de la escritura de constitución mencionada, así como con el documento nº [Nº DE DOCUMENTO], que recoge la certificación del Registro Mercantil donde constan los datos mencionados.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones de ‘ S.L.’ de [IMPORTE] euros de valor nominal, lo que supone un % del capital social. Acredito esta circunstancia mediante certificación expedida

En prueba de lo anterior acompaño certificación expedida por el Secretario del Consejo de Administración de ‘[DENOMINACIÓN SOCIAL], S.L.’ del Libro Registro donde constan las mentadas titularidades, como documento

Segundo.-El [FECHA], ‘ S.L.’ celebró junta general de socios, en segunda convocatoria, debidamente convocada, en la que, entre otros acuerdos, se adoptó, como constaba en su Orden del Día, el cese de los administradores que ostentaban el cargo de consejeros hasta esa fecha, renovándose totalmente dicho Consejo de Administración con el nombramiento de D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], LOS DEMANDADOS, quienes aceptaron el cargo. Dicho nombramiento y su aceptación fueron inscritos en el Registro Mercantil a fecha de [FECHA], según consta en la inscripción número [NÚMERO] de la certificación que se adjunta como documento nº [Nº DE DOCUMENTO].

Igualmente acredito dicha circunstancia mediante escritura otorgada ante el Notario D./Dña. [NOMBRE Y APELLIDOS] de [LOCALIDAD], de fecha [FECHA], que se acompaña como documento nº [Nº DE DOCUMENTO] de los que se unen a este escrito de demanda.

Tercero.- Que por los citados administradores se han llevado a cabo las siguientes conductas [EXPONER LOS HECHOS].

Cuarto.- Los hechos descritos en el ordinal Tercero del presente relato fáctico han producido unos daños en el patrimonio de mis representados que asciende a la cifra de [IMPORTE] euros, como se acredita de la documental aportada, y sin perjuicio de las restantes pruebas que habrán de practicarse en el momento procesal oportuno, la apertura de cuyo período intereso ya desde este momento.

A los presentes hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- Jurisdicción y competencia

Es competente la sección de lo Mercantil del tribunal de instancia correspondienta al domicilio del demandado, al que se dirige la presente demanda, por aplicación de lo dispuesto en los arts. 45 y 50 de la L.E.C.

II.- Procedimiento

El procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley, atendiendo a la cantidad reclamada que es de [IMPORTE] euros, en aplicación de lo dispuesto en el art. 249.2 de la L.E.C.

III.- Legitimación activa

El art. 241 del Texto Refundido de la Ley de Sociedades de Capital, aprobado por Real Decreto Legislativo 1/2010, de 2 de julio, según el cual, además de la acción social, quedan a salvo las acciones de indemnización que puedan corresponder a los socios y a terceros por actos de los administradores que lesionen directamente los intereses de aquéllos.

IV.- Requisitos para el ejercicio de la acción individual de responsabilidad

Deben concurrir los requisitos comunes de toda reclamación de responsabilidad, teniendo en cuenta las siguientes precisiones efectuadas por los Tribunales, en una clásica doctrina jurisprudencial fijada por [ÓRGANO JUDICIAL], entre otras, por sentencias del Tribunal Supremo de fecha 22 de marzo de 2006, de 6 de octubre de 2000, rec. 2912/1995, 20 de diciembre de 2002, rec. 1727/1997, 4 de abril de 2003, rec. 2512/1997, 25 de abril de 2.005, rec. 4197/1998, 7 de marzo de 2006, rec. 2264/1999, o 16 de noviembre de 2009 .

* Daño.

Quien sufre el daño en el caso de la acción individual es el titular del interés lesionado, que pueden ser, los socios o los terceros, comprendiendo dentro de estos, tanto a los acreedores perjudicados por los actos de los administradores, como otras personas, pues el concepto de ‘tercero’ dentro de este artículo, ha de entenderse en contraposición al de socio.

* Acto lesivo de los administradores con motivo del ejercicio de su cargo.

Incluye tanto la acción positiva como la omisión, siempre que exista un deber de actuar.

* El acto de los administradores ha de ser ilícito.

La ilicitud del acto puede derivar:

- Del incumplimiento de preceptos legales o estatutarios, o
-De la simple culpa en su actuación por falta de la diligencia general con la que debe desempeñar su cargo.
• Y en este punto entiende que es de aplicación lo previsto en el art. 236 LSC 1/2010.
• En la culpa o negligencia en el actuar de los administradores basta cualquier género de culpa (arts. 1089 y 1902 del Código Civil, aplicable en la materia como expresivos de principios generales de nuestro ordenamiento), viniendo definida la negligencia en este ámbito por conceptos normativos, contenidos en el art. 225 LSC 1/2010, según el cual la diligencia exigible al administrador es la propia de ‘un ordenado empresario’.
* Relación de causalidad entre el acto lícito del administrador y el daño directo sufrido por el socio o el tercero.

La producción del daño en el patrimonio del tercero debe ser consecuencia directa del acto imputado a los administradores.

En la casuística a que esta acción ha dado lugar, se ha considerado a veces que existe la cuestionada relación de causalidad en la lesión sufrida por los actores con el carácter ‘directo’ que exige el art. 241 LSC 1/2010 en casos de decisión de llevar a cabo la liquidación social en forma ‘irregular’, que aunque no determina daño patrimonial alguno para la propia sociedad, sí malogra definitivamente el derecho del acreedor a hacer efectivo su crédito con arreglo al principio de responsabilidad patrimonial universal que consagra el art. 1911 del Código Civil. (AP Lérida 6-2-98)

El plazo de prescripción es de cuatro años a contar desde el día en que hubiera podido ejercitarse [OTROS DATOS].

El art. 144 del Reglamento Hipotecario, en relación con los arts. 1317 y 1365 del Código Civil, así como arts. 6 al 12 del Código de Comercio

VI- Cuantía

Conforme al art. 252 Regla 1ª de la LEC en relación con el art. 253 de ese mismo texto legal cifro la cuantía de la presente demanda en [IMPORTE] euros, que es el importe de la cantidad que se reclama.

VI.- Postulación y defensa

Conforme a lo previsto en los arts. 23 y 31 de la Ley de Enjuiciamiento Civil, se presenta la demanda por medio de Procurador legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VII.- Costas

Conforme al artículo 394 de la L.E.C., las costas han de imponerse a la demandada.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL, que teniendo por presentado este escrito de demanda con sus documentos y copias, se sirva admitirlo y acordar de conformidad, teniendo por interpuesta demanda de Juicio Declarativo de Menor Cuantía en ejercicio de la acción individual de responsabilidad por mi representados, socios de la mercantil ‘[DENOMINACIÓN SOCIAL], S.L.’, contra el órgano de administración formado por los codemandados D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y contra sus cónyuges, en el caso de que fueren casados y a los solos efectos del art. 144 RH 1947 para que en su día, seguidos sean los trámites legales oportunos, se dicte sentencia por la que se declare la responsabilidad de los codemandados, condenándoles por ello solidariamente al pago de [IMPORTE] euros, por los daños causados a mis mandantes, más otros [IMPORTE] euros previstos para intereses y costas, cuya condena a los codemandados igualmente intereso, cantidades todas ellas que habrán de destinarse a indemnizar a los demandantes por los daños sufridos, por ser justicia que pido en

Abogado y número de colegiado [Nº DE COLEGIADO/A]

Procurador

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

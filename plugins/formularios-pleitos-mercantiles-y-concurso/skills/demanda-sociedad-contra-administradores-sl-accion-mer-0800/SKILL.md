---
name: demanda-sociedad-contra-administradores-sl-accion-mer-0800
description: "Demanda de la sociedad contra los administradores de una SL por la acción social de responsabilidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de la sociedad contra los administradores de una SL por la acción social de responsabilidad

> Formulario **MER-0800** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario por la que una sociedad limitada ejercita la acción social de responsabilidad contra los administradores que le han causado un daño patrimonial, previo acuerdo de la junta general, y solicita su condena solidaria al pago de una cantidad.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de la sociedad contra los administradores de una SL por la acción social de responsabilidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de la sociedad contra los administradores de una SL por la acción social de responsabilidad” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-sociedad-contra-administradores-sl-accion-mer-0800`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] FECHA (9 veces)
- [ ] Nº (8 veces)
- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] IMPORTE (5 veces)
- [ ] CITAR NÚMERO DE RECURSO O ECLI (3 veces)
- [ ] DNI/NIE (3 veces)
- [ ] DOMICILIO (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE DEL NOTARIO (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL LETRADO (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR (2 veces)
- [ ] DATOS REGISTRALES: TOMO, FOLIO, HOJA
- [ ] DOMICILIO PROFESIONAL
- [ ] DOMICILIO SOCIAL
- [ ] NIF
- [ ] Nº DE COLEGIADO
- [ ] Nº DE PROTOCOLO
- [ ] PROVINCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 45 LEC
- art. 249.2 LEC
- art. 238 LSC
- art. 236 LSC
- art. 225 LSC
- art. 202.2 LSC
- art. 241 bis LSC
- art. 234 LSC
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

- Junto a «…o por los realizados incumpliendo los deberes inherentes al desempeño del cargo.»: el original citaba el art. 237 LSC para este presupuesto; comprobar la redacción vigente de los arts. 236 y 237 LSC, que regulan, respectivamente, los presupuestos de la responsabilidad y su carácter solidario con las causas de exoneración.
- Junto a «…ligencia, incluso aunque un acuerdo de la junta general lo autorice o ratifique.»: el original remitía al «actual art. 236.2 LSC»; comprobar el artículo equivalente en la LSC vigente.
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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador de los Tribunales y de [DENOMINACIÓN SOCIAL], S.L., según acredito mediante escritura de poder que acompaño como documento n.º 1 de los que se unen al presente escrito, para su unión a los autos mediante copia, previa su certificación por el Letrado de la Administración de Justicia del órgano judicial al que tengo el honor de dirigirme, y cuya devolución intereso por precisarlo para otros usos, dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO], con despacho profesional en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y como mejor proceda en Derecho,

DIGO:

Que mediante el presente escrito formulo demanda de juicio declarativo ordinario, en la que ejercito la acción social de responsabilidad de los administradores de [DENOMINACIÓN SOCIAL], S.L., D./Dña. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE] y domicilio en [DOMICILIO]; D./Dña. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE] y domicilio en [DOMICILIO]; y D./Dña. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE] y domicilio en [DOMICILIO].

Fundamento mis pretensiones en los siguientes

HECHOS

Primero.- Mi representada, [DENOMINACIÓN SOCIAL], S.L., con NIF [NIF], se constituyó el [FECHA], según consta en la escritura autorizada el [FECHA] por [NOMBRE DEL NOTARIO], Notario de [LOCALIDAD]. Su domicilio social se halla sito en [DOMICILIO SOCIAL] y fue inscrita en el Registro Mercantil n.º [Nº] de los de [PROVINCIA] el [FECHA], [DATOS REGISTRALES: TOMO, FOLIO, HOJA].

Acredito estos extremos con el documento n.º 2 de los que se acompañan a este escrito, consistente en copia simple de la escritura de constitución mencionada, así como con el documento n.º 3, que recoge la certificación del Registro Mercantil donde constan los datos mencionados.

Segundo.- El [FECHA], [DENOMINACIÓN SOCIAL], S.L. celebró junta general de socios, en segunda convocatoria, debidamente convocada, en la que, entre otros acuerdos, se adoptó, como constaba en su orden del día, el cese de los administradores que ostentaban el cargo de consejeros hasta esa fecha, renovándose totalmente dicho Consejo de Administración con el nombramiento de D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], LOS DEMANDADOS, quienes aceptaron el cargo. Dicho nombramiento y su aceptación fueron inscritos en el Registro Mercantil con fecha [FECHA], según consta en la inscripción número [Nº] de la certificación que se adjunta como documento n.º [Nº].

Igualmente acredito dicha circunstancia mediante escritura otorgada ante el Notario D./Dña. [NOMBRE DEL NOTARIO], de [LOCALIDAD], de fecha [FECHA], que se acompaña como documento n.º [Nº] de los que se unen a este escrito de demanda.

Tercero.- Que por los citados administradores se han llevado a cabo las siguientes conductas: [ENUMERAR LAS CONDUCTAS QUE HAN DADO LUGAR A LOS RESULTADOS DESENCADENANTES DE LA RESPONSABILIDAD IMPUTADA; DEBE DOCUMENTARSE EN LA MEDIDA EN QUE SE PUEDA O, EN SU CASO, EN EL PERÍODO PROBATORIO, TRATAR DE ACREDITARSE POR EL MEDIO QUE SE CONSIDERE OPORTUNO: TESTIFICALES, PERICIALES, ETC.].

Cuarto.- En fecha [FECHA] se procedió a la celebración de Junta General Extraordinaria de socios de [DENOMINACIÓN SOCIAL], S.L. en la que, hallándose presentes socios que representaban el 100% del capital social de la citada mercantil, se decidió por unanimidad la celebración de dicha junta con el carácter de universal. No siendo preciso, por lo tanto, el cumplimiento de los requisitos de convocatoria, los asistentes fijaron el orden del día, entre cuyos puntos, y en primer lugar, constaba el debate y aprobación del cese y destitución de los miembros del Consejo de Administración, y el ejercicio de la acción social de responsabilidad contra los mismos.

Tras las oportunas deliberaciones se adoptó por mayoría el ejercicio de dicha acción, la destitución de los citados administradores demandados y el nombramiento del nuevo Consejo.

Acredito dichos extremos con el certificado del acta de la junta a que se ha hecho referencia en el párrafo precedente, como documento n.º [Nº], la cual fue elevada a escritura pública ante el Notario D./Dña. [NOMBRE DEL NOTARIO] en fecha [FECHA], con el número [Nº DE PROTOCOLO] de su protocolo, que acompaño como documento n.º [Nº], para la posterior inscripción de las destituciones y nuevos nombramientos del órgano de administración que constan en las inscripciones [Nº] y [Nº] de la certificación del Registro Mercantil señalada precedentemente y que acompaña al presente escrito de demanda.

Quinto.- Los hechos descritos en el ordinal Tercero del presente relato fáctico han producido unos daños en el patrimonio de mi representada, la mercantil [DENOMINACIÓN SOCIAL], S.L., que ascienden a la cifra de [IMPORTE] euros, como se acredita de la documental aportada, y sin perjuicio de las restantes pruebas que habrán de practicarse en el momento procesal oportuno, la apertura de cuyo período intereso ya desde este momento.

A los presentes hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- Jurisdicción y competencia

Es competente la Sección de lo Mercantil del Tribunal de Instancia del domicilio del demandado, al que se dirige la presente demanda, por aplicación de lo dispuesto en los arts. 45 y 50 de la LEC.

II.- Procedimiento

El procedimiento ajustado a Derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la misma Ley, atendiendo a la cantidad reclamada, que es de [IMPORTE] euros, en aplicación de lo dispuesto en el art. 249.2 de la LEC.

III.- Legitimación activa

El art. 238.1 del texto refundido de la Ley de Sociedades de Capital, aprobado por Real Decreto Legislativo 1/2010, de 2 de julio (LSC), establece que la acción (social) de responsabilidad contra los administradores se entablará por la sociedad, previo acuerdo de la junta general, que puede ser adoptado, aunque no conste en el orden del día.

En cuanto a la mayoría exigible en ese acuerdo social, el citado art. 238 LSC señala que los estatutos no pueden establecer, para este caso, una mayoría distinta de la ordinaria.

IV.- Presupuestos constitutivos de la responsabilidad

En virtud de lo previsto en el art. 236 LSC, los administradores responden frente a la sociedad, frente a los socios y frente a los acreedores sociales del daño que causen por actos u omisiones contrarios a la ley o a los estatutos, o por los realizados incumpliendo los deberes inherentes al desempeño del cargo.

Estos deberes se recogen en los arts. 225 a 232 LSC, según los cuales deben desempeñar su cargo con la diligencia de un ordenado empresario y de un representante leal, debiendo informarse cada uno de ellos de manera diligente sobre la marcha de la empresa. Además, están obligados a cumplir con los deberes de fidelidad, lealtad y secreto a los que los citados preceptos les obligan.

Siguiendo la doctrina señalada en la sentencia del Tribunal Supremo, Sala 1.ª, de 20 de julio de 2010 [CITAR NÚMERO DE RECURSO O ECLI], se trata además de una responsabilidad solidaria. Así, responden solidariamente todos los miembros del órgano de administración que realizó el acto o adoptó el acuerdo lesivo, menos los que prueben que, no habiendo intervenido en su adopción y ejecución, desconocían su existencia o, conociéndola, hicieron todo lo conveniente para evitar el daño o, al menos, se opusieron expresamente a aquél. En ningún caso exonera de responsabilidad la circunstancia de que el acto o acuerdo lesivo haya sido adoptado, autorizado o ratificado por la junta general. En este sentido, señala la referida resolución que, pese a que los acuerdos de la junta general vinculan a todos los socios (art. 93.2 de la derogada Ley de Sociedades Anónimas, hoy recogido en el art. 202.2 LSC), el legislador ha reconocido a los administradores, al actuar en el ámbito de su competencia, una independencia o autonomía respecto de ellos, cuando sean antijurídicos y dañosos para la sociedad. Por ello, no quedan exonerados, en la idea de que los administradores no pueden realizar actos ilícitos, contrarios a la ley, a los estatutos o al deber general de diligencia, incluso aunque un acuerdo de la junta general lo autorice o ratifique.

Esta presunción de responsabilidad solidaria de los administradores miembros del órgano de administración implica una presunción iuris tantum de culpa colectiva o conjunta de todos y cada uno de ellos, quienes individualmente solo pueden liberarse de esta presunción mediante la prueba de las causas exonerativas previstas en la LSC.

Fuera de los supuestos de renuncia o transacción, ningún acuerdo que pueda tomarse por la junta general, sea cual sea su contenido, exonera de responsabilidad al administrador o impide la prosperabilidad de la acción entablada por la sociedad. La acción de responsabilidad contra los administradores prescribe a los cuatro años a contar desde el día en que hubiera podido ejercitarse (art. 241 bis LSC, en vigor desde el 24 de diciembre de 2014).

V.- Carga de la prueba

Incumbe a los demandados, puesto que los hechos de los administradores que han dado lugar a la presente reclamación de cantidad son contrarios a la ley y a los estatutos sociales, como indica la sentencia de la Audiencia Provincial de San Sebastián de 18 de julio de 1995 [CITAR NÚMERO DE RECURSO O ECLI].

Sobre si el acto está o no comprendido en el objeto social, es doctrina consagrada por el Tribunal Supremo (sentencias de 18 de diciembre de 2001, 6 de febrero de 2003, 28 de marzo de 2005 y 6 de julio de 2006) y por las resoluciones de la Dirección General de los Registros y del Notariado (hoy Dirección General de Seguridad Jurídica y Fe Pública) de 1 de junio de 1976, 2 de octubre de 1981, 31 de marzo de 1986 y 12 de mayo de 1989, la de que «la inclusión en el ámbito del poder de representación de los administradores, no sólo de los actos de desarrollo o ejecución del objeto social, sea en forma directa o indirecta y los complementarios y auxiliares para ello, sino también los neutros y polivalentes y los aparentemente desconectados con tal objeto social, quedando excluidos tan sólo únicamente los actos claramente contrarios al objeto social, esto es los contradictorios o denegatorios del mismo» y, además, dada la dificultad de establecer a priori si un determinado acto queda o no incluido en el ámbito de las facultades concedidas a los representantes orgánicos de la sociedad, no es posible hacer recaer en el tercero la carga de interpretar la conexión entre el acto que va a realizar y el objeto social redactado unilateralmente por la otra parte contratante.

El propio art. 234 LSC mantiene la responsabilidad de la sociedad, supuesta la buena fe y la actuación diligente del tercero, aun cuando se desprenda de los estatutos inscritos en el Registro Mercantil que el acto no está comprendido en el objeto social. En este sentido, véase la sentencia de la Audiencia Provincial de Pontevedra de 30 de junio de 1996 [CITAR NÚMERO DE RECURSO O ECLI].

VI.- Cuantía

Conforme al art. 253 de la LEC cifro la cuantía de la presente demanda en [IMPORTE] euros, que es el importe de la cantidad que se reclama.

VII.- Postulación y defensa

Conforme a lo previsto en los arts. 23 y 31 de la Ley de Enjuiciamiento Civil, se presenta la demanda por medio de Procurador legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VIII.- Costas

Conforme al artículo 394 de la LEC, las costas han de imponerse a la parte demandada.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL, que teniendo por presentado este escrito de demanda con sus documentos y copias, se sirva admitirlo y acordar de conformidad, teniendo por interpuesta demanda de juicio declarativo ordinario en ejercicio de la acción social de responsabilidad por mi representada, la mercantil [DENOMINACIÓN SOCIAL], S.L., contra el anterior órgano de administración formado por los codemandados D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], para que en su día, seguidos los trámites legales oportunos, se dicte sentencia por la que se declare la responsabilidad de los codemandados, condenándoles por ello solidariamente al pago de [IMPORTE] euros por los daños causados en el patrimonio de mi representada, más otros [IMPORTE] euros previstos para intereses y costas, cuya condena a los codemandados igualmente intereso, cantidades todas ellas que habrán de reintegrar el patrimonio de mi representada, por ser justicia que pido en [LOCALIDAD], a [FECHA].

Abogado y número de colegiado: [NOMBRE Y APELLIDOS DEL LETRADO] — Col. n.º [Nº DE COLEGIADO]

Procurador: [NOMBRE Y APELLIDOS DEL PROCURADOR]

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

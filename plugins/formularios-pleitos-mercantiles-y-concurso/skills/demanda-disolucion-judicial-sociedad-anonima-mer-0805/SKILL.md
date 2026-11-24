---
name: demanda-disolucion-judicial-sociedad-anonima-mer-0805
description: "Demanda de disolución judicial de una sociedad anónima presentada por accionistas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de disolución judicial de una sociedad anónima presentada por accionistas

> Formulario **MER-0805** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Escrito dirigido al Tribunal Mercantil competente por varios accionistas de una Sociedad Anónima sobre disolución judicial de la misma, por considerar que se halla incursa en una causa de disolución establecida legalmente, y tras haber hecho caso omiso el Consejo de Administración de la misma sobre el requerimiento notarial de convocatoria de Junta General. Adaptado a LJV.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de disolución judicial de una sociedad anónima presentada por accionistas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de disolución judicial de una sociedad anónima presentada por accionistas” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-disolucion-judicial-sociedad-anonima-mer-0805`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (13 veces)
- [ ] FECHA (6 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] IMPORTE (5 veces)
- [ ] Nº (5 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] PORCENTAJE (4 veces)
- [ ] CAUSA DE DISOLUCIÓN (3 veces)
- [ ] LUGAR (2 veces)
- [ ] NOMBRE O DENOMINACIÓN (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DESCRIBIR
- [ ] DOCUMENTOS ACREDITATIVOS
- [ ] FECHA DE INSCRIPCIÓN
- [ ] FOLIO
- [ ] FUNDAMENTO DE LA CAUSA DE DISOLUCIÓN
- [ ] HOJA
- [ ] MES
- [ ] NIF
- [ ] NIF/DNI
- [ ] NÚMERO
- [ ] OBJETO PRINCIPAL DE LA SOLICITUD
- [ ] TOMO

## Normas que cita el formulario

- art. 363 TRLSC
- art. 367 TRLSC
- art. 126.1 Ley 15/2015
- art. 125 LJV
- art. 366 TRLSC
- art. 363 LSC
- art. 253 LEC
- art. 126.3 LJV
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

Notas al pie del formulario original:
(1) La disolución judicial puede darse en los siguientes supuestos:

-A solicitud de cualquier interesado, en los siguientes casos:

* Cuando la junta solicitada a los administradores por accionistas que consideren que existe causa legítima al efecto no sea convocada.

* Cuando convocada dicha junta no pueda lograrse el acuerdo o éste sea contrario a la disolución.

-A instancia de los administradores, que están obligados a solicitar dicha disolución judicial de la sociedad cuando el acuerdo social sea contrario a la disolución o no pueda ser logrado.

Esta solicitud de los administradores debe formularse en el plazo de 2 meses a contar: (los requisitos sobre el plazo para instar la disolución judicial se introducen por reforma del art. 262.5 efectuada por LC, aplicable desde 1-9-2004 —actual art. 367 TRLSC—)

- desde la fecha prevista para la celebración de la junta, cuando ésta no se haya constituido, o

- desde el día de la junta, cuando el acuerdo haya sido contrario a la disolución o no se haya adoptado.

Puede practicarse en los términos previstos para la anotación preventiva de la demanda de impugnación de acuerdos sociales.

Los administradores responden solidariamente de las obligaciones sociales posteriores al acaecimiento de la causa legal de disolución ( *) cuando, existiendo alguna de las causas de disolución para las que se precisa acuerdo de la junta, incumplan la obligación de solicitar la disolución judicial o el concurso () de la sociedad en el plazo de 2 meses:

- A contar desde la fecha prevista para la celebración de la junta cuando ésta no se haya constituido.

- Desde el día de la junta, cuando el acuerdo haya sido contrario a la disolución o al concurso ( *), ya que los administradores están obligados a solicitar dicha disolución judicial cuando el acuerdo es contrario a la disolución o cuando no puede ser logrado.

( *) La precisión relativa a que las obligaciones sociales de las que pueden ser responsables los administradores en este supuesto de responsabilidad son sólo aquellas posteriores al acaecimiento de la causa legal de disolución ha sido introducida por la nueva redacción dada al apdo. 5 del art. 262 por Ley 19/2005, de 14 de noviembre, con entrada en vigor el 16-11-2005 —actual art. 367 TRLSC—.

( *) La referencia al concurso se introduce por reforma del art. 262.5 LSA efectuada por LC, aplicable desde 1-9-2004 —actual art. 367 TRLSC—.

En estos casos las obligaciones sociales reclamadas se presumen de fecha posterior al acaecimiento de la causa legal de disolución de la sociedad, salvo que los administradores acrediten que son de fecha anterior.

Esta presunción ha sido introducida por la nueva redacción dada al apdo. 5 del art. 262 por Ley 19/2005, de 14 de noviembre, con entrada en vigor el 16-11-2005 —actual art. 367 LSC—.

La resolución judicial que decrete la disolución de la sociedad debe inscribirse en el Registro Mercantil, para los que se prevén los siguientes aspectos:

- Publicidad:

El Boletín Oficial del Registro Mercantil publicará los datos esenciales de la disolución, facilitando de esta forma una nueva vía de conocimiento de la nueva situación social, y lo que es más importante, determinando (artículo 21 Código de Comercio y 9 RRM 1996) la fecha a partir de la cual dicho acto será oponible a terceros de buena fe. A los efectos de esta publicidad en el BORME, el artículo 369 TRLSC 2010 dispone que el registrador mercantil remitirá de oficio al Registro Mercantil Central, de forma telemática y sin coste adicional alguno, la inscripción de la disolución. La eliminación del coste de la publicación se enmarca en una serie de medidas adoptadas mediante el Real Decreto-ley 13/2010, de 3 de diciembre, para reducir costes de publicidad y de tramitación a las empresas españolas "que suponen trabas muchas veces injustificadas para nuestras empresas" (v. exposición de motivos de esta norma, apartado IV).

-Título inscribible.

La inscripción debe practicarse en virtud de testimonio judicial de la sentencia firme por la que se declare la disolución de la sociedad.

-Circunstancias de la inscripción.

Además de las circunstancias generales deben hacerse constar las siguientes:

*La causa que determina la disolución.

*El cese de los administradores.

*Las personas encargadas de la liquidación.

*Las normas que, en su caso, haya acordado la junta general para la liquidación y división del haber social.

(2) Téngase en cuenta que, a partir del 23-7-2015, fecha de entrada en vigor de la LJV, se trata de un expediente de jurisdicción voluntario de los regulados en los arts. 125 a 128 LJV. Por otro lado, desde la reforma orgánica instaurada por la LO 1/2025, la competencia objetiva y funcional para conocer todas aquellas cuestiones que se promuevan al amparo de la normativa reguladora de las sociedades mercantiles corresponde a las Secciones de lo Mercantil del Tribunal de Instancia [SEDE], según lo previsto en el art. 87.6.a) LPOJ, señalándose asimismo esta competencia en la nueva redacción de la diisp. adic. 8.ª.1 LOPJ, en especial, para los asuntos que tramiten y decidan en primera instancia los procesos civiles sobre impugnación de acuerdos sociales establecidos en el texto refundido de la Ley de Sociedades de Capital (RDLeg 1/2010, de 2 de julio) [NOTA DE REVISIÓN: La Ley de Sociedades Anónimas y la Ley de Sociedades de Responsabilidad Limitada están derogadas; hoy rige el texto refundido de la Ley de Sociedades de Capital (RDLeg 1/2010). Hay que citar el artículo equivalente del TRLSC. Fuente: RDLeg 1/2010, disposición derogatoria única.], el texto refundido de la Ley de Sociedades de Capital (RDLeg 1/2010, de 2 de julio) o Ley de Cooperativas.


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

D/Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], (etc.), según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO]; dirigido por el Letrado abajo firmante don [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito intereso la DISOLUCIÓN JUDICIAL de la mercantil [DENOMINACIÓN SOCIAL], S.A., con NIF [NIF] y domicilio en [LOCALIDAD]

Fundamento mis pretensiones en los siguientes

HECHOS

Primero.- Mis representados son todos ellos accionistas de la mercantil ‘[DENOMINACIÓN SOCIAL]’, constituida el [FECHA] de [MES] de [AÑO], según consta en la escritura autorizada el [FECHA] por D./Dña. [NOMBRE Y APELLIDOS], Notario de [LOCALIDAD], su domicilio social se halla sito en la localidad de [LOCALIDAD] calle [CALLE], y fue inscrita en el Registro Mercantil nº [NÚMERO] de los de [SEDE] el [FECHA DE INSCRIPCIÓN], Tomo [TOMO], Folio [FOLIO], Hoja [HOJA], con CIF [NIF/DNI]

Acredito estos extremos con el documento nº [Nº DE DOCUMENTO] de los que se acompañan a este escrito, y consistente en copia simple de la escritura de constitución mencionada, así como con el documento nº [Nº DE DOCUMENTO], que recoge la certificación del Registro Mercantil donde constan los datos mencionados.

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] acciones nominativas de ‘.’ de [IMPORTE] euros de valor nominal, lo que supone un [PORCENTAJE] % del capital social.

D./Dña. [NOMBRE Y APELLIDOS]. es titular de [Nº] acciones nominativas de ‘[NOMBRE O DENOMINACIÓN]’ de [IMPORTE] euros de valor nominal, lo que supone un [PORCENTAJE] % del capital social.

D./Dña [NOMBRE Y APELLIDOS] es titular de [Nº] acciones nominativas de ‘.’ de [IMPORTE] euros de valor nominal, lo que supone un [PORCENTAJE] % del capital social.

(Etc.)

De lo anterior se deduce que en conjunto, mis mandantes representan un [PORCENTAJE] % (no importa el porcentaje puesto que cualquier interesado puede presentar el escrito solicitando la disolución judicial) del capital social total de la mercantil a la que venimos haciendo referencia. En prueba de lo anterior acompaño certificación expedida por el Secretario del Consejo de Administración de ‘[NOMBRE O DENOMINACIÓN]’ del Libro Registro donde constan las mentadas titularidades, como documento

Segundo.- El [FECHA], mis representados solicitaron al Consejo de Administración de ‘.’ la convocatoria de una junta general de accionistas por considerar que la citada mercantil se hallaba incursa en una causa de disolución consistente en [DESCRIBIR] Dicho órgano de administración se halla compuesto por D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], según consta en las inscripciones números [Nº] correspondientes a los respectivos nombramientos y aceptaciones según consta en la certificación del Registro Mercantil que se acompaña como documento nº [Nº DE DOCUMENTO]

Acredito dicha solicitud de convocatoria de junta mediante copia del requerimiento notarial dirigido a los citados administradores por el Notario D./Dña. [NOMBRE Y APELLIDOS] de [LOCALIDAD], de fecha [FECHA], que se acompaña como documento nº [Nº DE DOCUMENTO] de los que se unen a este escrito.

Tercero.- Que mis mandantes consideran que la sociedad se halla incursa en la siguiente causa que legitima su disolución (son causas de disolución las previstas en los arts. 363 y 368 TRLSC) [CAUSA DE DISOLUCIÓN] puesto que [FUNDAMENTO DE LA CAUSA DE DISOLUCIÓN].

Acredito la causa de disolución que se alega mediante los siguientes documentos [DOCUMENTOS ACREDITATIVOS]

Cuarto.- Que habiendo transcurrido el plazo de [Nº] meses la convocatoria de junta no ha sido llevada a cabo, habiendo sido inútiles cuantas gestiones han realizado mis representados en su intento por ponerse en contacto con los administradores sociales a fin de agilizar los trámites al efecto. (Si el plazo es superior a 2 meses y la causa de disolución efectivamente existe los administradores se hallarán incursos en la responsabilidad que recoge el art. 367 TRLSC).

A los presentes hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- Jurisdicción y competencia

Es competente la Sección de lo Mercantil del Tribunal de Instancia del domicilio de la mercantil [DENOMINACIÓN SOCIAL]. a que se refiere este escrito, por aplicación de lo dispuesto en los arts. 126.1 de la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria (en lo sucesivo, LJV) y 366.1 Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el texto refundido de la Ley de Sociedades de Capital (en lo sucesivo, TRLSC).

II PROCEDIMIENTO

El procedimiento ajustado a derecho será el del expediente de jurisdicción voluntaria regulado en los arts. 125 a 128 LJV, dado que se solicita la disolución judicial de la sociedad que debería haber sido acordada en la junta de accionistas no convocada por los administradores sociales.

III Legitimación activa

El art. 366 TRLSC, según el cual cualquier interesado podrá solicitar la disolución judicial de la sociedad en el caso de que, habiendo sido solicitada a los administradores la convocatoria de junta por cualquier accionista que considere, a su juicio, que existe causa legítima para la disolución de la sociedad.

IV Legitimación pasiva

Corresponde a la sociedad X, S.A., conforme a lo previsto en el apartado 1 del artículo 366 TRLSC.

V Causa de disolución

En virtud de lo previsto en el art. 363 LSC, la [CAUSA DE DISOLUCIÓN] constituye causa legítima de disolución social

VI CUANTIA

Conforme al art. 253 de la LEC, en relación con el 251 regla 12ª del mismo texto legal, cifro la cuantía de la presente demanda en [IMPORTE] euros, que es el importe al que asciende el valor del patrimonio de ‘.

VII Postulación y defensa

Conforme a lo previsto en el art. 126.3 LJV, se presenta este escrito por medio de Procurador legalmente habilitado y bajo dirección de Letrado firmante de la misma.

VIII COSTAS

Por todo lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito con sus documentos y copias, se sirva admitirlo y acordar de conformidad, para que en su día, seguidos sean los trámites legales oportunos, se dicte Auto por el que se declare:

1) la disolución judicial de la citada compañía mercantil, señalando que su causa es [CAUSA DE DISOLUCIÓN]
2) el cese de los administradores sociales,
3) el nombramiento de los liquidadores sociales,

Todo ello sin perjuicio de la eventual responsabilidad en la que hayan podido incurrir los administradores, por ser justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO, que en el presente procedimiento se solicita [OBJETO PRINCIPAL DE LA SOLICITUD] (se especificará el objeto principal de la solicitud) por lo que formulo la petición de medida cautelar consistente en la anotación preventiva de la presente solicitud en la hoja correspondiente a la mercantil [DENOMINACIÓN SOCIAL]. en el Registro Mercantil de [LOCALIDAD], por cuanto se considera necesaria para asegurar la efectividad de la tutela judicial que se quiere se otorgue en el Auto que se dicte en este proceso, entendiendo esta representación que de no acordarse, como medida cautelar, puede verse impedida (o dificultada) por situaciones producidas durante la pendencia del proceso.

A los efectos legales procedentes, se ofrece caución por la suma de [IMPORTE] euros, cantidad que se considera suficiente para responder, en su caso, de los daños y perjuicios que la adopción de la medida cautelar que se interesa pudiera causar en el patrimonio de la mercantil [DENOMINACIÓN SOCIAL].

Por lo expuesto, y al amparo de lo previsto en los artículos 721 y siguientes, en concreto el art. 727.5º de la LEC,

SUPLICO AL TRIBUNAL que se tengan por hechas las anteriores manifestaciones, y habiendo quedado acreditada cumplidamente la concurrencia de los presupuestos que exige la Ley para la adopción de la medida cautelar de anotación preventiva que desde ahora se interesa, previos los trámites legales, incluida la audiencia de las partes, se sirva dictar resolución en la que, declarando justificada la pretensión, se acuerde la adopción de la medida cautelar interesada, por ser justicia que reitero en el mismo lugar y fecha ut supra.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

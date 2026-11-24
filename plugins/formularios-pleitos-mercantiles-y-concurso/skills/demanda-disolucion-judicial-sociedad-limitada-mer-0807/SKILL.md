---
name: demanda-disolucion-judicial-sociedad-limitada-mer-0807
description: "Demanda de disolución judicial de una sociedad limitada presentada por socios. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de disolución judicial de una sociedad limitada presentada por socios

> Formulario **MER-0807** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Modelo de demanda de juicio ordinario interpuesta ante la Sección de lo Mercantil del Tribunal de Instancia por varios socios por medio de la cuál se solicita la disolución judicial de una Sociedad de Responsabilidad Limitada, tras no haberse procedido a celebrar la Junta General en un plazo determinado, requerida notarialmente por los demandantes al considerar que la sociedad está incursa en alguna de las causas de disolución establecidas legalmente.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de disolución judicial de una sociedad limitada presentada por socios» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de disolución judicial de una sociedad limitada presentada por socios” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-disolucion-judicial-sociedad-limitada-mer-0807`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (6 veces)
- [ ] Nº DE DOCUMENTO (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] CAUSA DE DISOLUCIÓN (3 veces)
- [ ] Nº (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] LUGAR (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] SEDE (2 veces)
- [ ] ACTUACIONES REALIZADAS
- [ ] ADMINISTRADORES A CESAR
- [ ] CALLE
- [ ] DESCRIBIR
- [ ] DOCUMENTOS ACREDITATIVOS
- [ ] FECHA DE INSCRIPCIÓN
- [ ] FOLIO
- [ ] FUNDAMENTO DE LA CAUSA DE DISOLUCIÓN
- [ ] HOJA
- [ ] LIQUIDADORES A NOMBRAR
- [ ] MOTIVO
- [ ] NIF
- [ ] NIF/DNI
- [ ] NÚMERO
- [ ] OBJETO PRINCIPAL DE LA SOLICITUD
- [ ] OTROS DATOS
- [ ] TOMO

## Normas que cita el formulario

- art. 126.1 Ley 15/2015
- art. 87.6.a LOPJ
- art. 125 LJV
- art. 366.1 TRLSC
- art. 363 TRLSC
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

D./Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO] de los que se unen al presente escrito para su unión a los Autos mediante copia, previa su certificación por el Letrado de la Administración de Justicia al que tengo el honor de dirigirme, y cuya devolución intereso por precisarlo para otros usos, dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito y al amparo de lo dispuesto en los artículos 125 y siguientes de la Ley de la Jurisdicción Voluntaria (LJV), promuevo EXPEDIENTE DE JURISDICCIÓN VOLUNTARIA SOBRE DISOLUCIÓN JUDICIAL de la mercantil SL, con NIF [NIF] y domicilio en [LOCALIDAD] Fundamento mis pretensiones en los siguientes

HECHOS

Primero.- Mis representados son todos ellos socios de la mercantil ‘ S.L.’, constituida el [FECHA], según consta en la escritura autorizada el [FECHA] por D./Dña. [NOMBRE Y APELLIDOS], Notario de [LOCALIDAD], su domicilio social se halla sito en la localidad de [LOCALIDAD] calle [CALLE], y fue inscrita en el Registro Mercantil nº [NÚMERO] de los de [SEDE] el [FECHA DE INSCRIPCIÓN], Tomo [TOMO], Folio [FOLIO], Hoja [HOJA], con CIF [NIF/DNI]

Acredito estos extremos con el documento nº [Nº DE DOCUMENTO] de los que se acompañan a este escrito, y consistente en copia simple de la escritura de constitución mencionada, así como con el documento nº [Nº DE DOCUMENTO], que recoge la certificación del Registro Mercantil donde constan los datos mencionados.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones de ‘[DENOMINACIÓN SOCIAL], S.L.’ de [IMPORTE] euros de valor nominal, lo que supone un [PORCENTAJE] % del capital social.

De lo anterior se deduce que en conjunto, mis mandantes representan un [PORCENTAJE] % [OTROS DATOS] del capital social total de la mercantil a la que venimos haciendo referencia. En prueba de lo anterior acompaño certificación expedida por el Secretario del Consejo de Administración de ‘[DENOMINACIÓN SOCIAL], S.L.’ del Libro Registro donde constan las mentadas titularidades, como documento

Segundo.- El [FECHA], mis representados solicitaron al Consejo de Administración de ‘[DENOMINACIÓN SOCIAL], S.L.’ la convocatoria de una junta general de socios por considerar que la citada mercantil se hallaba incursa en una causa de disolución consistente en [DESCRIBIR] Dicho órgano de administración se halla compuesto por D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], según consta en las inscripciones números [Nº] correspondientes a los respectivos nombramientos y aceptaciones según consta en la certificación del Registro Mercantil que se acompaña como documento nº [Nº DE DOCUMENTO]

Acredito dicha solicitud de convocatoria de junta mediante copia del requerimiento notarial dirigido a los citados administradores por el Notario D./Dña. [NOMBRE Y APELLIDOS] de [LOCALIDAD], de fecha [FECHA], que se acompaña como documento nº [Nº DE DOCUMENTO] de los que se unen a este escrito.

Tercero.- Que mis mandantes consideran que la sociedad se halla incursa en la siguiente causa que legitima su disolución [CAUSA DE DISOLUCIÓN] puesto que [FUNDAMENTO DE LA CAUSA DE DISOLUCIÓN].

Acredito la causa de disolución que se alega mediante los siguientes documentos [DOCUMENTOS ACREDITATIVOS]

Cuarto.- Que habiendo transcurrido el plazo de [Nº] meses la convocatoria de junta no ha sido llevada a cabo, ni se ha instado el concurso de la sociedad, habiendo sido inútiles cuantas gestiones han realizado mis representados en su intento por ponerse en contacto con los administradores sociales a fin de agilizar los trámites al efecto [ACTUACIONES REALIZADAS].

A los presentes hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- Jurisdicción y competencia

Es competente la Sección de lo Mercantil del Tribunal de Instancia del domicilio de [LOCALIDAD], S.L., al que se dirige el presente escrito, por aplicación de lo dispuesto en los arts. 126.1 de la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria (en lo sucesivo, LJV) y 366.1 Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el texto refundido de la Ley de Sociedades de Capital (en lo sucesivo, TRLSC), en relación con lo dispuesto en el art. 87.6.a) LOPJ.

II.- PROCEDIMIENTO

El procedimiento ajustado a derecho será el del expediente de jurisdicción voluntaria regulado en los arts. 125 a 128 LJV, dado que se solicita la disolución judicial de la sociedad que debería haber sido acordada en la junta de accionistas no convocada por los administradores sociales.

III.- Legitimación activa

El art. 366.1 TRLSC, según el cual cualquier interesado podrá solicitar la disolución judicial de la sociedad en el caso de que, habiendo sido solicitada a los administradores la convocatoria de junta por cualquier socio que considere, a su juicio, que existe causa legítima para la disolución de la sociedad, ésta no haya sido convocada, no se haya celebrado o no se haya adoptado el acuerdo de disolución.

IV.- Legitimación pasiva

Corresponde a la sociedad [DENOMINACIÓN SOCIAL] S.L., según lo previsto en el art. 366.1 in fine TRLSC.

V.- Causa de disolución

En virtud de lo previsto en el art. 363 TRLSC la [CAUSA DE DISOLUCIÓN] constituye causa legítima de disolución social

VI.- Postulación y defensa

Conforme a lo previsto en el art. 126.3 LJV, se presenta este escrito por medio de Procurador legalmente habilitado y bajo dirección de Letrado firmante de la misma.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL,

que teniendo por presentado este escrito con sus documentos y copias, se sirva admitirlo y acordar de conformidad, teniendo por solicitada DISOLUCIÓN JUDICIAL de la mercantil ‘ S.L.’, para que en su día, seguidos sean los trámites legales oportunos, se dicte Auto por el que se declare:

1) la disolución judicial de la citada compañía mercantil, señalando que su causa es [CAUSA DE DISOLUCIÓN]
2) el cese de los administradores sociales, [ADMINISTRADORES A CESAR]
3) el nombramiento de los liquidadores sociales, [LIQUIDADORES A NOMBRAR]

Todo ello sin perjuicio de la eventual responsabilidad en la que hayan podido incurrir los administradores, por ser justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO, que en el presente procedimiento se solicita [OBJETO PRINCIPAL DE LA SOLICITUD] < formulo la petición de medida cautelar consistente en la anotación preventiva de la presente solicitud en la hoja correspondiente a la mercantil en el Registro Mercantil de [LOCALIDAD], por cuanto se considera necesaria para asegurar la efectividad de la tutela judicial que se quiere se otorgue en el Auto que se dicte en este proceso, entendiendo esta representación que de no acordarse, como medida cautelar, puede verse impedida [MOTIVO] por situaciones producidas durante la pendencia del proceso.

A los efectos legales procedentes, se ofrece caución por la suma de [IMPORTE] euros, cantidad que se considera suficiente para responder, en su caso, de los daños y perjuicios que la adopción de la medida cautelar que se interesa pudiera causar en el patrimonio de la mercantil.

Por lo expuesto, y al amparo de lo previsto en los artículos 721 y siguientes, en concreto el art. 727.5º de la LEC,

SUPLICO AL TRIBUNAL que se tengan por hechas las anteriores manifestaciones, y habiendo quedado acreditada cumplidamente la concurrencia de los presupuestos que exige la Ley para la adopción de la medida cautelar de anotación preventiva que desde ahora se interesa, previos los trámites legales, incluida la audiencia de las partes, se sirva dictar resolución en la que, declarando justificada la pretensión, se acuerde la adopción de la medida cautelar interesada, por ser justicia que reitero en el mismo lugar y fecha ut supra.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

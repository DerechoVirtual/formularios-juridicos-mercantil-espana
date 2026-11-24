---
name: estatutos-sociales-sociedad-garantia-reciproca-mer-0427
description: "Estatutos sociales de una sociedad de garantía recíproca. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Estatutos sociales de una sociedad de garantía recíproca

> Formulario **MER-0427** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de estatutos de sociedad de garantía recíproca regulando su denominación, duración, domicilio, objeto social, el capital social y las participaciones, los socios, sus órganos sociales, el ejercicio social y las cuentas anuales, así como la disolución y liquidación, las garantías y el fondo de provisiones técnicas.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Estatutos sociales de una sociedad de garantía recíproca» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Estatutos sociales de una sociedad de garantía recíproca” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:estatutos-sociales-sociedad-garantia-reciproca-mer-0427`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (9 veces)
- [ ] IMPORTE (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN
- [ ] Nº DE ARTÍCULO
- [ ] Nº MÍNIMO DE CONSEJEROS
- [ ] NÚMERO DE SOCIOS

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

Modelo de estatutos de sociedad de garantía recíproca regulando su denominación, duración, domicilio, objeto social, el capital social y las participaciones, los socios, sus órganos sociales, el ejercicio social y las cuentas anuales, así como la disolución y liquidación, las garantías y el fondo de provisiones técnicas.


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

TÍTULO I.- DENOMINACIÓN, DURACIÓN, DOMICILIO Y OBJETO

Artículo 1º.- Denominación

La Sociedad se denominará « [DENOMINACIÓN SOCIAL], S.G.R.», que se regirá por su contrato constitutivo, por los presentes estatutos y en lo en ellos no dispuesto, por la Ley 1/1994 de 11 de Marzo, de Sociedades de Garantía Recíproca o legislación vigente en cada momento.

Artículo 2º.- Duración

La Sociedad tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de su escritura constitutiva, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Sociedad en momentos anteriores al de su inscripción en el Registro Mercantil.

Los ejercicios sociales se computarán por años naturales.

Artículo 3º.- Domicilio

El domicilio de la Sociedad se halla situado en [DIRECCIÓN], calle [CALLE]

Artículo 4º.- Objeto social

El objeto social de la Sociedad será el otorgamiento de garantías personales por aval o por cualquier otro medio admitido en derecho diferente al seguro de caución, a favor de sus socios y para las operaciones que éstos realicen dentro del giro o tráfico de las empresas de que sean titulares.

[OPCIONAL — incluir si procede]

La Sociedad también podrá prestar servicios de asistencia y asesoramiento financiero a sus socios, y una vez cubiertas las reservas y obligaciones legalmente necesarias, podrá participar en sociedades y asociaciones cuyo objeto sean actividades dirigidas a pequeñas y medianas empresas.

La Sociedad no podrá conceder directamente ninguna clase de créditos a sus socios, pero sí que podrá emitir obligaciones con sujeción a las condiciones legalmente establecidas.

TÍTULO II.- CAPITAL SOCIAL Y PARTICIPACIONES

Artículo 5º.- Capital social

El capital social mínimo se fija en [IMPORTE] euros, dividido en [Nº] participaciones sociales de [IMPORTE] euros de valor nominal cada una de ellas, iguales, acumulables e indivisibles, numeradas de manera correlativa con los números 1 a [Nº], y representadas por certificaciones que llevarán dicha numeración, autorizadas por la firma del Presidente del Consejo de Administración.

Dicho capital se halla totalmente suscrito y desembolsado mediante aportaciones dinerarias realizadas por los socios fundadores a título de propiedad.

El capital social será variable entre la cifra mínima citada y el triple de dicha cantidad.

El importe de la cifra de recursos propios computables no podrá ser inferior a 15.000.000 de euros. A los efectos de este apartado la cifra de recursos propios computables se calculará de acuerdo con la definición que fije el Banco de España.

Artículo 6º.- Prohibiciones sobre las participaciones

Las participaciones no tendrán el carácter de valores negociables ni podrán denominarse acciones.

Será nula la creación de participaciones sociales que no responda a una aportación dineraria a la sociedad, y no podrán atribuirse participaciones sociales por un valor inferior a su valor nominal.

Artículo 7º.- Desembolso de las participaciones sociales

En el momento de la suscripción los socios deberán desembolsar en efectivo el 25% de las cuotas que suscriban, siempre que esté desembolsada la cantidad correspondiente a la cifra mínima del capital.

El Consejo de Administración determinará la cuantía, el tiempo y la forma en que deberán realizarse los sucesivos desembolsos.

Deberán estar totalmente desembolsadas las participaciones cuya titularidad exijan los presentes Estatutos para obtener una determinada garantía de la Sociedad, cuando dicha garantía sea otorgada.

La falta de desembolso será causa de exclusión del socio moroso, una vez que éste sea advertido fehacientemente de la sanción en caso de que persista en su incumplimiento.

Artículo 8º.- Libro Registro de Socios

La sociedad llevará un Libro Registro de Socios cuya custodia y llevanza corresponde al órgano de administración. En él se inscribirán los socios con expresión del número de participaciones de que sean titulares y de los sucesivos desembolsos por razón de las mismas. Se harán constar igualmente el nombre, apellidos, estado, razón o denominación social y domicilio del socio, su carácter de socio partícipe o socio protector, fecha de inscripción, motivo de la suscripción o adquisición y, en su caso, empresa de la que sea titular.

Artículo 9º.- Reglas sobre transmisiones de las participaciones sociales

Toda transmisión inter vivos de las participaciones sociales exigirá la autorización previa por parte del Consejo de Administración, quien podrá autorizarlas cuando se trate de transmisiones a favor de personas que cumplan las condiciones previstas en los presentes Estatutos, cuando pidan su admisión en calidad de socio o cuando ya lo sean.

Las participaciones cuya titularidad exijan los presentes Estatutos para la obtención de una garantía otorgada por la Sociedad sólo serán exigibles, mientras la garantía subsista, junto con la empresa del socio.

La adquisición de participaciones sociales por sucesión hereditaria no confiere al heredero o legatario la condición de socio salvo cuando el Consejo de Administración acuerde, a petición de aquel, dicha admisión.

Si el heredero o legatario no adquiere la condición de socio le serán reembolsadas las participaciones sociales una vez extinguidas las deudas que la Sociedad tuviera garantizadas con cargo a las mismas.

La adquisición por cualquier título de participaciones sociales deberá ser comunicada por escrito a la Sociedad, indicando el nombre, apellidos, razón o denominación social y domicilio del nuevo socio, así como de la empresa de la que, en su caso, sea titular. Cuando no se cumpla este requisito el adquirente no podrá ejercitar los derechos que corresponden a los socios.

Artículo 10º.- Aumento y reducción del capital social

El capital podrá ser aumentado por el Consejo de Administración entre la cifra mínima del capital social y el triple de dicha cantidad, mediante la creación y atribución de nuevas participaciones sociales, que en todo caso deberán estar suscritas en su totalidad y desembolsadas en un 25% como mínimo en el momento de su creación, todo ello sin perjuicio de la exigencia del desembolso íntegro de la cantidad correspondiente a la cifra mínima del capital.

También dentro de esos límites, el capital podrá ser reducido por el reembolso y extinción de participaciones sociales, previo acuerdo del Consejo de Administración.

La reducción del capital social por debajo de la cifra mínima del capital social fijada en los Estatutos, o el aumento del mismo por encima del triple de dicha cantidad, requerirán acuerdo de la Junta General por el que se fije nueva cifra mínima de capital social, de modo que éste se mantenga entre dicha cifra y su triple, acuerdo que deberá ser adoptado según las reglas previstas para las modificaciones estatutarias y su ejecución.

Artículo 11º.- Derechos atribuidos por las participaciones sociales

Quienes sean titulares de una participación social ostentarán la condición de socio, correspondiéndole como mínimo los siguientes derechos:

* Derecho a votar en las Juntas Generales.
* Derecho a solicitar el reembolso de la participación social.
* Derecho a participar, en su caso, en los beneficios sociales.
* Derecho a ser informado en los términos previstos legalmente.
* Derecho a solicitar las garantías y asesoramiento de la Sociedad dentro de los límites establecidos en los presentes Estatutos.

[OPCIONAL — incluir si procede]

Los socios partícipes tienen, además, el derecho a solicitar las garantías y el asesoramiento de la sociedad dentro de los límites establecidos en estos estatutos.

Artículo 12º.- Derecho de reembolso de las participaciones sociales

Los socios podrán exigir el reembolso de las participaciones sociales que le pertenezcan y cuya titularidad no le venga exigida por los Estatutos por razón de una garantía otorgada por la Sociedad que permanezca en vigor.

No procederá el reembolso si su realización diese lugar a una cobertura insuficiente del capital social obligatorio, de la reserva legal o de los requisitos de solvencia.

El reembolso deberá ser solicitado al Consejo de Administración con una antelación mínima de [Nº] meses, y su importe no podrá ser superior al valor real de las participaciones reembolsadas, teniendo siempre como límite máximo su valor nominal. En caso de plusvalía, ésta pertenecerá a las reservas de la Sociedad, sobre las cuales no ostentan derecho alguno los socios que obtienen reembolsos.

Los socios que se separen responderán por el importe reembolsado, durante el plazo de 5 años, y en el caso de que el patrimonio social sea insuficiente, de las deudas contraídas por la Sociedad con anterioridad a la fecha de dicho reembolso.

TÍTULO III.- SOCIOS

Artículo 13º.- Clases de socios

Los socios pueden ser:

1º) Partícipes.

Son aquellos a cuyo favor la Sociedad puede prestar garantías.

Las solicitudes de admisión como socio partícipe deben ir dirigidas al Consejo de Administración, acompañada de la firma de [NÚMERO DE SOCIOS]. El Consejo decidirá sobre dicha cuestión.

Para ser socio partícipe deben reunirse los siguientes requisitos:

a) Ser titular de una empresa con un número de trabajadores que no puede exceder de 250 y que esté dedicada a la actividad económica, dentro del ámbito geográfico, definidos en el objeto social de los presentes Estatutos.

En el caso de que la empresa pasase a tener un número de trabajadores superior a 250, no daría lugar a la pérdida de la condición de socio, siempre que 4/5 de los socios partícipes sean titulares de empresas que no sobrepasen dicho límite.

b) No hallarse incurso concurso de acreedores.
c) Suscribir, como mínimo [Nº] participación/es social/es.

2º) Socios protectores. Son aquellos socios que no cumplen el primero de los requisitos exigidos para ser socio partícipe, es decir, ser titulares de empresas con un número de trabajadores que no puede exceder de 250 y que esté dedicada a la actividad económica, dentro del ámbito geográfico, definidos en el objeto social de los presentes Estatutos.

Estos socios no pueden solicitar de la Sociedad garantías para sus operaciones, y su participación en ella no puede exceder del 50% de la cifra mínima fijada para el capital social por los presentes estatutos. A estos efectos, no se computan en dicho porcentaje las participaciones de socios protectores que ostenten la condición de Administraciones públicas, organismos autónomos y demás entidades de derecho público dependientes de las mismas, sociedades mercantiles en cuyo capital participe mayoritariamente cualquiera de las anteriores o entidades que asocien o representen intereses económicos de carácter general o de ámbito sectorial.

Los socios protectores deberán suscribir como mínimo [Nº] participación/es, debiendo dirigir su solicitud de admisión al Consejo de Administración.

Artículo 14º.- Pérdida de la condición de socio

La condición de socio se pierde por las causas siguientes:

1ª) Por transmisión de la totalidad de las participaciones sociales, realizada de conformidad con las previsiones estatutarias establecidas al respecto.
2ª) Por muerte del socio persona física o disolución del socio persona jurídica.
3ª) Por pérdida de la condición de empresario.
4ª) Por desaparición de alguna de las condiciones requeridas para ser socio, salvo el caso de que la empresa que participe llegue a tener más de 250 trabajadores, en los términos previstos en el artículo precedente.
5ª) Por ejercicio del derecho al reembolso de las participaciones, en los términos previstos en los presente Estatutos.

Artículo 15º.- Exclusión

La exclusión de socios es competencia de la Junta General, excepto en el caso de incumplimiento del desembolso de los dividendos pasivos o de las obligaciones garantizadas por la Sociedad.

La decisión de la Junta se adoptará, previa audiencia del interesado, quien deberá ser convocado a la sesión de la Junta en cuyo orden del día figure dicho acuerdo mediante carta certificada y con acuse de recibo remitida con una antelación no inferior a 15 días de la fecha en que haya de tener lugar la reunión.

Son causas de exclusión de los socios las siguientes:

1ª) Incumplimiento del desembolso de los dividendos pasivos o de las obligaciones garantizadas por la Sociedad.

[OPCIONAL — incluir si procede]

En este caso, la causa de exclusión operará una vez que el socio sea advertido fehacientemente de la sanción en caso de que persista en su incumplimiento, y podrá ser acordada por el Consejo de Administración.

2ª) Impago de gastos y comisiones adeudadas a la Sociedad.

3ª) Ejercicio de operaciones que no sean de lícito comercio.

4ª) Incumplimiento de las garantías y obligaciones contraídas frente a la Sociedad.

5ª) Concurso de acreedores del socio.

6ª) Injerencia en las funciones administrativas por socio al que no correspondan las mismas.

7ª) Comisión de fraude en la administración por socio que ostente la cualidad de administrador.

8ª) Falta en el cumplimiento de las obligaciones derivadas de los presentes Estatutos, de los acuerdos sociales y de las decisiones de la Junta o el Consejo de Administración, cuando se relaciones con los fines sociales y con las garantías que, en cumplimiento de sus fines, sean presentadas por ésta.

TÍTULO IV.- ÓRGANOS SOCIALES

Artículo 16º.- Disposiciones generales

Son órganos de la sociedad la Junta General de Socios, como órgano supremo y deliberante que manifiesta la voluntad social por mayoría en los asuntos de su competencia, y el Consejo de Administración, al que le corresponden las funciones de gestión, administración y representación de la sociedad, con las facultades que legalmente tiene atribuidas, así como por las que le son reconocidas en los presentes estatutos.

Sección Primera.- Junta General

Artículo 17º.- Disposición general

Los socios que legal y válidamente se constituyan en Junta General decidirán por mayoría en los asuntos que sean competencia de la Junta.

Todos los socios, incluidos los disidentes y los que no hayan participado en la reunión, quedan sometidos a los acuerdos adoptados por la Junta General, sin perjuicio de su derecho de impugnación de los mismos, en los supuestos previstos legalmente, y cuando concurran los requisitos precisos al efecto.

Artículo 18º.- Competencias de la Junta

Es competencia de la Junta deliberar y adoptar acuerdos sobre los siguientes asuntos:

- Censurar la gestión social, aprobar las cuentas anuales y la aplicación del resultado.
- Nombrar y separar a los administradores, liquidadores y, en su caso, auditores de la sociedad, así como ejercitar la acción social contra cualquiera de ellos.
- Aprobar la exclusión de un socio por alguna de las causas establecidas legal o estatutariamente, salvo cuando la causa de exclusión consista en el incumplimiento por parte del socio del desembolso de los dividendos pasivos o de las obligaciones garantizadas por la sociedad.
- Autorizar a los administradores para el ejercicio por cuenta propia o ajena del mismo, análogo o complementario género de actividad que constituya el objeto social.
- Modificar los estatutos sociales.
- Fijar el límite máximo de deudas a garantizar por la Sociedad dentro de cada ejercicio.
- Aumentar y reducir la cifra mínima del capital social estatutario.
- Acordar la transformación, fusión o escisión de la sociedad.
- Acordar la disolución de la sociedad
- Cualquier otro asunto que determinen la Ley o los Estatutos.

[OPCIONAL — incluir si procede]

Asimismo, es competencia de la Junta el impartir instrucciones a los administradores o someter a autorización la adopción de decisiones o acuerdos por dicho órgano sobre determinados asuntos de gestión.

Artículo 19º.- Clases de Juntas Generales

Las Juntas Generales podrán ser ordinarias o extraordinarias, y deberán ser convocadas por el Consejo de Administración.

La Junta General ordinaria, que deberá haber sido previamente convocada, deberá celebrarse de manera necesaria dentro de los seis primeros meses de cada ejercicio económico con el objeto de fijar el límite máximo de deudas a garantizar por la Sociedad durante cada ejercicio, nombrar auditores de cuentas, censurar la gestión social, aprobar, en su caso, las cuentas del ejercicio anterior, y resolver sobre la aplicación del resultado obtenido, según el balance que sea aprobado al efecto, sin perjuicio de otros asuntos que puedan ser tratados en la misma, de conformidad con lo previsto en el correspondiente Orden del Día.

Todas las Juntas Generales distintas a la Junta General ordinaria se considerarán Juntas Generales Extraordinarias y deberán celebrarse siempre que el Consejo de Administración de la sociedad lo considere oportuno o conveniente para los intereses de la sociedad y, en todo caso, cuando así sea solicitado por un número de socios que representen al menos un 10% del capital social desembolsado, quienes habrán de expresar en su solicitud los asuntos que consideren que deban tratarse en dicha Junta. En este caso, la Junta deberá ser convocada por el Consejo de Administración para su celebración dentro de los 30 días siguientes al del requerimiento notarial a dicho Consejo de Administración, debiendo incluirse en su Orden del Día, por lo menos, los asuntos plasmados en la solicitud de los socios.

Artículo 20º.- Lugar y fecha de celebración de las Juntas

Las Junta Generales se celebrarán en el término municipal donde la sociedad tiene su domicilio, en el lugar, fecha y hora señalados en la convocatoria.

Si en la convocatoria no figurase el lugar de celebración se entenderá que la Junta ha sido convocada para su celebración en el domicilio social.

Artículo 21º.- Junta Universal

La Junta General quedará válidamente constituida para tratar cualquier asunto, sin necesidad de previa convocatoria, siempre que esté presente o representada la totalidad del capital social y que los concurrentes acepten por unanimidad la celebración de la reunión y el orden del día de la misma.

La junta universal podrá reunirse en cualquier lugar del territorio nacional o del extranjero.

Artículo 22º.- Supuestos en que debe convocarse Junta General

El Administrador deberá convocar la Junta General Ordinaria, en todo caso, para su celebración dentro de los 6 primeros meses de cada ejercicio.

Si no fuere así, podrá ser convocada por el Letrado de la Administración de Justicia o registrador mercantil correspondiente al domicilio social a solicitud de cualquier socio, y previa audiencia del Órgano de Administración.

Además, el Órgano de Administración deberá convocar la Junta General siempre que lo consideren necesario o conveniente.

La obligación deberá cumplirse, en todo caso, a solicitud de uno o varios socios que representen al menos el 5% del capital social, expresando en la solicitud los asuntos a tratar en la Junta.

En este supuesto la Junta debe ser convocada para su celebración dentro del mes siguiente a la fecha en que se haya requerido notarialmente al Órgano de Administración para convocarla, y deberán incluirse necesariamente en su orden del día los asuntos que hayan sido objeto de la solicitud.

Si el Órgano de Administración no atiende oportunamente a la solicitud, puede realizarse la convocatoria por el Letrado de la Administración de Justicia o Registrador Mercantil correspondiente al domicilio social si lo solicita uno o varios socios que representen al menos el 5% del capital social y previa audiencia al Órgano de Administración.

El Órgano de Administración está obligados a convocar la junta general en el plazo de 2 meses, para que se adopte el acuerdo de disolución de la sociedad cuando se dé alguna de las causas disolutorias que se contemplan en el Artículo [Nº DE ARTÍCULO] de los presentes estatutos.

En caso de muerte o de cese del Administrador único cualquier socio podrá solicitar al letrado de la administración de justicia o al Registrador Mercantil competente la convocatoria de la Junta General para el nombramiento de nuevo administrador.

En los casos en que proceda el letrado de la administración de justicia deberá resolver sobre la convocatoria en el plazo de un mes desde que le haya sido formulada la solicitud, y si acuerda su celebración, deberá designar libremente al Presidente y Secretario de la Junta. Contra la resolución por la que se acuerde la convocatoria no cabrá recurso alguno, y los gastos de la convocatoria serán de cuenta de la sociedad.

Artículo 23º.- Forma y contenido de la convocatoria

La Junta General deberá ser convocada

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Por comunicación individual]

Entre la convocatoria y la fecha prevista para la celebración de la reunión deberá existir un plazo de al menos 15 días.

[OPCIONAL — incluir si procede]

En los casos de convocatoria individual a cada socio, el plazo se computará a partir de la fecha en que haya sido remitido el anuncio al último de ellos.

El anuncio deberá expresar los siguientes datos:

* Nombre de la sociedad.
* Fecha y hora de la reunión.
* Orden del día, en el que deberán figurar los asuntos a tratar.

[OPCIONAL — incluir si procede]

(Para los casos de anuncio de la convocatoria por medio de comunicación individual y escrita,)

* Nombre de la persona o personas que realizan la comunicación.

Artículo 24º.- Asistencia y representación

Todos los socios tienen derecho a asistir a la Junta General, sin que pueda exigírseles para la asistencia a las reuniones de la junta la titularidad de un número mínimo de participaciones.

Los socios podrán acudir a las juntas personalmente o representados.

La representación se regirá por lo siguiente: los socios podrán ser representados por medio de otro socio, su cónyuge, ascendientes, descendientes, persona que ostente poder general conferido en documento público con facultades para administrar todo el patrimonio que el representado tenga en el territorio nacional, o por otras personas, si así lo autorizan los estatutos.

Ningún socio podrá ostentar más de 10 representaciones ni un número de votos delegados superior al 10% del total.

La representación comprenderá la totalidad de las participaciones de que sea titular el socio representado y deberá conferirse por escrito. Si no consta en documento público, deberá ser especial para cada junta.

La representación siempre es revocable, teniendo el valor de revocación la asistencia personal a la junta del representado.

Artículo 25º.- Derecho de voto

Cada participación atribuye a su titular el derecho a emitir un voto.

No obstante lo anterior, los socios no podrán ejercer el derecho de voto correspondiente a sus participaciones, sino que vendrán obligados a la abstención, cuando en la Junta se vaya a adoptar algún acuerdo que le autorice a transmitir participaciones de las que sea titular, o que le excluya de la sociedad, o que le libere de una obligación o le conceda un derecho, o por el que la sociedad decida anticiparle fondos, concederle créditos o préstamos, o prestar garantías a su favor o facilitarle asistencia financiera, o cuando, siendo administrador, se refiera a la dispensa de la prohibición de competencia o al establecimiento con la sociedad de una relación de prestación de cualquier tipo de obras o servicios.

En esos supuestos, las participaciones del socio que se encuentre en alguno de ellos, se deducirá del capital social para el cómputo de la mayoría de los votos que sea precisa en cada caso.

Ningún socio podrá tener un número de votos superior al 5% del total.

Los socios protectores no podrán tener, en conjunto, un número de votos superior al 50% del total. En caso de que sea necesario, se reducirá proporcionalmente el número de votos que corresponden a cada uno de ellos, sin que se les pueda privar de un voto como mínimo.

Artículo 26º.- Adopción de los acuerdos: Régimen de mayorías

En general los acuerdos sociales se adoptarán, excepto en los supuestos de mayoría reforzada y unanimidad que se contemplan en los párrafos siguientes, por mayoría de los votos válidamente emitidos, siempre que representen al menos 1/3 de los votos correspondientes a las participaciones sociales en que se divide el capital social, sin computar los votos en blanco.

No obstante lo anterior, se precisará las mayorías reforzada consistente en el voto favorable de al menos 2/3 de los votos correspondiente a las participaciones en que se divida el capital, en los siguientes supuestos:

* Aumento o reducción de capital o cualquier otra modificación de los estatutos sociales para la que no se exija mayoría cualificada.
* Transformación fusión o escisión de la sociedad, supresión del derecho de preferencia en los aumentos de capital, exclusión de socios y autorización a los administradores para dedicarse a actividades iguales, análogas o complementarias a las del objeto social.

[OPCIONAL — incluir si procede]

En todo caso se precisará unanimidad para la adopción de los siguientes acuerdos:

* Incorporación a los estatutos de cláusulas que prohíban toda transmisión voluntaria de las participaciones sociales por actos inter vivos.
* Aumento de capital a realizar elevando el valor nominal de las participaciones sociales, excepto cuando se haga íntegramente con cargo a reservas o beneficios de la sociedad.
* Reducción del capital social, cuando no afecte por igual a todas las participaciones.
* Acuerdo de devolución de capital por sistema distinto a la prorrata de las respectivas participaciones sociales, en la reducción de capital por restitución de aportaciones.
* Incorporación, modificación o supresión a los estatutos de causas de separación de los socios.
* Incorporación a los estatutos de causas de exclusión distintas de las legales, o modificación de las estatutarias.
* Acuerdo contrario a percibir la cuota de liquidación en dinero.

Artículo 27º.- Funcionamiento de la Junta

Las Juntas Generales serán presididas por el Presidente del Consejo de Administración o quien haga sus veces o por el socio que por mayoría sea elegido por los socios asistentes a la reunión.

Corresponde al Presidente la dirección de las deliberaciones y la proclamación de los resultados de las votaciones.

El Presidente será asistido por un Secretario, quien será designado en cada caso por el socio que resulte elegido entre los asistentes a la reunión.

Artículo 28º.- Acta de la Junta

Todos los acuerdos sociales serán consignados en acta, que deberá extenderse o consignarse en el correspondiente Libro de Actas.

Las actas incluirán de manera necesaria la lista de los socios asistentes y deberá ser aprobada por la propia Junta al finalizarse su sesión o, en su defecto, dentro del plazo de los 15 días siguientes, por el Presidente de la Junta General y dos socios interventores, representantes cada uno de ellos de la mayoría y de la minoría respectivamente.

El acta tendrá fuerza ejecutiva desde la fecha de su aprobación, y deberá ser firmada por el Secretario, con el Visto Bueno del Presidente.

Podrá requerirse acta notarial, según lo previsto legalmente.

Sección Segunda.- Órgano de Administración

Artículo 29º.- Consejo de Administración

La Sociedad será gestionada, representada y administrada por un Consejo de Administración que actuará colegiadamente y estará compuesto por [Nº] administradores o consejeros, con un mínimo de [Nº MÍNIMO DE CONSEJEROS] y un máximo de

Para ser administrador [ELEGIR: se requiere / no se requiere] la condición de socio.

No podrá ser administrador quien se halle incurso en alguna de las prohibiciones e incompatibilidades establecidas al efecto en la Ley 1/1994, de 11 de marzo, reguladora de las Sociedades de Garantía Recíproca, y demás disposiciones vigentes.

El Consejo nombrará de entre sus miembros a un Presidente y un Vicepresidente. Dicho nombramiento habrá de recaer en administradores que ostenten la condición de socios.

Todos los miembros del Consejo de Administración deberán ser personas de reconocida honorabilidad comercial y profesional, poseer conocimientos y experiencia adecuados para ejercer sus funciones y estar en disposición de ejercer un buen gobierno de la entidad. Los requisitos de honorabilidad y conocimiento y experiencia deberán concurrir también en los directores generales o asimilados, así como en los responsables de las funciones de control interno y en las personas que ocupen puestos claves para el desarrollo diario de la actividad de la entidad.

A estos efectos, la valoración de la idoneidad se ajustará a los criterios y procedimientos de control de la honorabilidad, experiencia y buen gobierno establecidos con carácter general para las entidades de crédito.

Artículo 30º.- Duración del cargo

Los administradores ejercerán su cargo por un período de [Nº] años, pudiendo ser reelegido por la Junta una o más veces por períodos de igual duración máxima.

Artículo 31º.- Nombramiento y separación

El nombramiento y separación de los administradores será competencia de la Junta General, aunque no figure en el correspondiente Orden del Día.

A estos efectos, los votos que voluntariamente se agrupen hasta reunir un número igual o superior al que resulte de dividir el total de los votos por el número de miembros del Consejo, tendrán derecho a designar los que, superando fracciones enteras, se deduzcan de la correspondiente proporción.

La Junta designará las personas que deben integrar el Consejo, sin determinar el cargo que dentro del mismo deba ocupar cada una de ellas.

El Consejo, para cubrir vacantes producidas durante el plazo de nombramiento de un administrador podrá nombrar sólo a personas que sean socias. Dicho nombramiento será eficaz hasta la siguiente reunión de la Junta, ordinaria o extraordinaria, posterior a dicho nombramiento.

Artículo 32º.- Prohibición de competencia

Los administradores no podrán dedicarse, por cuenta propia o ajena, al mismo, análogo o complementario género de actividad que constituya el objeto social, salvo autorización expresa de la sociedad por acuerdo de la Junta General.

Cualquier socio podrá solicitar del Letrado Superior de Justicia o del Registrador Mercantil competente el cese del administrador que infrinja esta prohibición.

Artículo 33º.- Representación de la sociedad

Por los actos de los administradores en representación de la sociedad ésta quedará obligada frente a terceros que hayan obrado de buena fe y sin culpa grave, aun cuando se desprenda de los estatutos inscritos en el Registro Mercantil que el acto no está comprendido en el objeto social.

Artículo 34º.- Retribución

El cargo de consejero será retribuido de la siguiente manera

[OPCIONAL — incluir si procede]

-una asignación fija,

[OPCIONAL — incluir si procede]

-dietas de asistencia,

[OPCIONAL — incluir si procede]

-participación en beneficios,

[OPCIONAL — incluir si procede]

-retribución variable con indicadores o parámetros generales de referencia,

[OPCIONAL — incluir si procede]

-remuneración en acciones o vinculada a su evolución,

[OPCIONAL — incluir si procede]

-indemnizaciones por cese, siempre y cuando el cese no estuviese motivado por el incumplimiento de las funciones de administrador

[OPCIONAL — incluir si procede]

-los sistemas de ahorro o previsión que se consideren oportunos.

El importe máximo de la remuneración anual del conjunto de los administradores en su condición de tales deberá ser aprobado por la junta general y permanecerá vigente en tanto no se apruebe su modificación.

Salvo que la junta general determine otra cosa, la distribución de la retribución entre los distintos administradores se establecerá por acuerdo de éstos y, en el caso del consejo de administración, por decisión del mismo, que deberá tomar en consideración las funciones y responsabilidades atribuidas a cada consejero.

La remuneración de los administradores deberá en todo caso guardar una proporción razonable con la importancia de la sociedad, la situación económica que tuviera en cada momento y los estándares de mercado de empresas comparables. El sistema de remuneración establecido deberá estar orientado a promover la rentabilidad y sostenibilidad a largo plazo de la sociedad e incorporar las cautelas necesarias para evitar la asunción excesiva de riesgos y la recompensa de resultados desfavorables.

Artículo 35º.- Funcionamiento del Consejo

El Consejo de Administración se reunirá cuantas veces lo estime pertinente su Presidente o quien haga sus veces, mediante convocatoria escrita en la que se hará constar la hora, lugar y fecha de la reunión junto con su orden del día.

También habrá de ser convocado cuando lo soliciten [Nº] miembros, caso en el que la reunión deberá celebrarse dentro de los [Nº] días siguientes a la recepción de la petición, indicando la hora, lugar y fecha de la misma, así como el orden del día, entre cuyos asuntos a tratar deberán incluirse necesariamente los propuestos por los solicitantes de dicha convocatoria.

No es precisa la realización de convocatoria alguna en aquellos casos en los que, reunidos la totalidad de los miembros del Consejo, acuerden constituirse en tal.

El Consejo se considerará válidamente constituido cuando concurran en la reunión la mayoría de sus componentes, presentes o representados.

Los acuerdos del Consejo deberán ser adoptados por mayoría absoluta de los miembros concurrentes en la reunión, excepto para los supuestos en que legal o estatutariamente se requiera la mayoría reforzada de las dos terceras partes del Consejo.

Artículo 36º.- Documentación de sus decisiones

Las decisiones adoptadas por el Consejo de Administración podrán ser hechas constar en el correspondiente Libro de Actas, debiendo constar en tales actas la firma del Presidente y la del Secretario.

En materia de ejecución de las actas, de los acuerdos y su ejecución, son aplicables las disposiciones previstas en el Real Decreto Legislativo 1/2010, por el que se aprueba la Ley de Sociedades de Capital.

Artículo 37º.- Delegación de facultades y apoderamientos

El Consejo de Administración podrá designar, de entre sus miembros, una Comisión ejecutiva, así como nombrar uno o más Consejeros delegados, delegando en ellos alguna o varias de las facultades que legalmente sean delegables.

A su vez, la Comisión ejecutiva está facultada para:

TÍTULO IV.- EJERCICIO SOCIAL Y CUENTAS ANUALES

Artículo 38º.- Ejercicio social

Los ejercicios sociales comienzan el 1 de enero y finalizan el 31 de diciembre de cada año natural.

Por excepción, el primer ejercicio social comprende desde el principio de las operaciones de la Sociedad hasta el 31 de diciembre de ese mismo año.

Artículo 39º.- Cuentas Anuales

Las cuentas y el informe de gestión, así como su revisión por auditores de cuentas, deberán ajustarse a las normas legales y reglamentarias vigentes en cada momento.

Cualquier socio tendrá derecho a obtener, en la forma y plazo legalmente previstos, copia inmediata y gratuita de los documentos antes referidos, así como del informe de gestión y, en su caso, del informe de los auditores.

Además, el socio o socios que representen al menos el 5% del capital social, podrán examinar en el domicilio social, por sí o en unión de un experto contable, los documentos que sirvan de soporte y antecedente de las cuentas anuales, sin perjuicio del derecho de la minoría a nombrar un auditor de cuentas con cargo a la Sociedad.

Artículo 40º.- Aplicación del resultado y reserva legal

La aplicación del resultado del ejercicio es competencia de la Junta General, con los límites legales y estatutarios.

La Sociedad deberá detraer, como mínimo, un 50% de los beneficios que obtenga en cada ejercicio, una vez deducido el Impuesto sobre Sociedades, hasta constituir un fondo de reserva legal hasta que alcance un valor igual al triple de la cifra mínima del capital social. Sólo será disponible esta reserva para cubrir, en su caso, el saldo deudor de la Cuenta de Pérdidas y Ganancias, y deberá ser repuesta cuando descienda del citado nivel.

Artículo 41º.- Reparto de beneficios

Los socios tendrán derecho a los beneficios repartibles en proporción a su participación en el capital social.

Sólo podrán ser repartidos entre los socios beneficios realmente obtenidos o reservas expresas de efectivos o de libre disposición, siempre que el valor del activo real menos el pasivo exigible no sea inferior al capital social.

Una vez efectuada dotada la reserva legal en los términos legales, y en la medida que lo permitan los excedentes y las reservas de libre disposición, podrá atribuirse a los socios un beneficio equivalente como máximo al interés legal del dinero incrementado en 2 puntos.

No obstante lo anterior, y a fin de reforzar la solvencia de la Sociedad, no podrán distribuirse beneficios entre los socios hasta que la suma de la reserva legal y las reservas de libre disposición no alcancen un valor igual al doble de la cifra mínima del capital social.

Los beneficios sobrantes de las operaciones citadas habrán de destinarse a la dotación de las reservas de libre disposición.

En todo caso, deberá destinarse a dotar reservas la totalidad de los beneficios generados en el ejercicio si existiera un déficit de recursos propios superior al 20%.

TÍTULO V.- DISOLUCIÓN Y LIQUIDACIÓN DE LA SOCIEDAD

Artículo 42º.- Disolución

La sociedad se disolverá por las causas legalmente establecidas.

Artículo 43º.- Liquidación

La disolución de la sociedad abrirá el período de liquidación, excepto en los supuestos de fusión o escisión total, o en cualquier otro caso de cesión global del activo y del pasivo.

Para la realización de las operaciones liquidatorias deberá constituirse una Comisión liquidatoria, presidida por un representante del Banco de España e integrada por cuatro miembros designados, respectivamente, por los socios partícipes, por los socios protectores, por las entidades de crédito que tuvieran operaciones garantizadas por la Sociedad en ese momento y por la Comunidad Autónoma donde la Sociedad tenga su domicilio social.

Una vez extinguidas las garantías otorgadas por la Sociedad y satisfechos los créditos contra ella, el activo resultante se distribuirá entre los socios en proporción al número de participaciones de las que sean titulares. Se excluye de esta participación en el reparto a los socios que lo hayan sido durante un plazo inferior a 5 años, excepto en el caso de que la Sociedad llegue a disolverse durante los 5 años iniciales de su existencia.

En el caso de que todas las participaciones no hubiesen sido libradas en igual proporción, deberán ser restituidos en primer término los socios que hubiesen liberado mayores cantidades en cuanto al exceso sobre la aportación de los restantes, restituyéndose lo demás con arreglo al criterio de proporcionalidad.

Cuando el activo social no sea suficiente para reembolsar a los socios, las pérdidas se distribuirán en proporción al valor nominal de las participaciones.

TÍTULO VI.- GARANTÍAS

Artículo 44º.- Condiciones generales de concesión

Los socios que pretendan obtener garantías de la Sociedad, mediante aval o por cualquier otro medio admitido en Derecho, para las operaciones que realicen dentro del ámbito de las empresas de las que sean titulares, deberán dirigir la correspondiente solicitud al Presidente del Consejo de Administración. El Consejo establecerá los informes o documentos que deberán acompañarse a las solicitudes, quedando a disposición de los socios partícipes los impresos necesarios.

El límite máximo individual de concesión de garantías por la Sociedad será proporcional al número de participaciones sociales suscritas por cada socio partícipe, no obstante, el Consejo de Administración podrá concretar los porcentajes teniendo en cuenta el límite global de garantías que la Sociedad pueda otorgar.

La aprobación o denegación de las garantías solicitadas es competencia exclusiva del Consejo de Administración.

Una vez que se proceda a la aprobación de la concesión de la garantía, el socio partícipe habrá de cumplir lo siguiente:

1º) Desembolsar la totalidad del valor de un mínimo de participaciones sociales que representen al menos el % del importe de la deuda garantizada por la Sociedad.
2º) Satisfacer a la Sociedad la correspondiente comisión, que no podrá exceder de [PORCENTAJE]; y la comisión de gastos de estudio, que no podrá exceder de [PORCENTAJE]
3º) Aportar las garantías personales o reales que en su caso le sean solicitadas por el Consejo de Administración.
4º) Comprometerse a utilizar el importe del crédito para garantizar el fin específico que causó su solicitud.
5º) Firmar el contrato de aval, con compromiso de cumplimiento de sus condiciones y preceptos estatutarios.

TÍTULO VII.- FONDO DE PROVISIONES TÉCNICAS

Artículo 45º.- Régimen

La Sociedad contará con un Fondo de Provisiones Técnicas que formará parte de su patrimonio, cuya finalidad será la de reforzar la solvencia de la Sociedad.

El Fondo podrá ser integrado, en todo caso, por:

1º) Dotaciones que efectúe la Sociedad con cargo a su Cuenta de Pérdidas y Ganancias, sin limitación, y en concepto de provisiones de insolvencias.
2º) Subvenciones, donaciones u otras aportaciones que no sean reintegrables y se efectúen por Administraciones Públicas, organismos autónomos y demás entidades de derecho público de ellos dependientes, sociedades mercantiles en cuyo capital participe mayoritariamente cualquiera de las anteriores y las entidades que representen o asocien intereses económicos de carácter general o del ámbito sectorial referido estatutariamente.
3º) Cualquier otra aportación de carácter no reintegrable efectuada por personas físicas o jurídicas, o por cualquier clase de entidades.

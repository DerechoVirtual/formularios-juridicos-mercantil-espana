---
name: escritura-constitucion-sociedad-laboral-limitada-mer-0451
description: "Escritura de constitución de una sociedad laboral limitada o anónima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de constitución de una sociedad laboral limitada o anónima

> Formulario **MER-0451** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública de constitución de una sociedad de responsabilidad limitada laboral o Anónima Laboral en la que se concretan las normas para su creación, funcionamiento y organización, tales como su objeto social, denominación, capital social, administración y representación de la misma.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de constitución de una sociedad laboral limitada o anónima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de constitución de una sociedad laboral limitada o anónima” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:escritura-constitucion-sociedad-laboral-limitada-mer-0451`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (12 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] COLEGIO
- [ ] DIRECCIÓN
- [ ] FECHA
- [ ] LUGAR
- [ ] NACIONALIDAD
- [ ] NIF
- [ ] OBJETO SOCIAL
- [ ] PROFESIÓN

## Normas que cita el formulario

- art. 4 Ley 10/2010

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

Modelo de escritura pública de constitución de una sociedad de responsabilidad limitada laboral o Anónima Laboral en la que se concretan las normas para su creación, funcionamiento y organización, tales como su objeto social, denominación, capital social, administración y representación de la misma.


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

NÚMERO DE PROTOCOLO:

En [LUGAR], a [FECHA].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO]

COMPARECEN

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y [ELEGIR: DNI / pasaporte / permiso de residencia] número

INTERVIENEN

Los señores comparecientes intervienen en su propio nombre y derecho.

Hago constar, a los efectos de lo dispuesto en el artículo 4º de la Ley 10/2010, de 28 de abril de Prevención de Blanqueo de Capitales y Financiación del Terrorismo, y el artículo 8º de su Reglamento, R.D.304/2014 de 5 de Mayo, sobre identificación del TITULAR REAL, que los comparecientes manifiestan y aseguran que, respectivamente, intervienen por cuenta e interés propios y no, directa o indirectamente, por los de ninguna otra persona.

Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente escritura de constitución de SOCIEDAD LABORAL DE RESPONSABILIDAD LIMITADA, a cuyo fin

EXPONEN

[OPCIONAL — incluir si procede]

(Sociedad Limitada Laboral)

PRIMERO.- Que los mentados Sres. han convenido constituir una Sociedad de Responsabilidad Limitada para la realización de [ACTIVIDAD]

SEGUNDO.- Que, a tales efectos, y en su calidad de únicos socios fundadores, han decidido otorgar la presente escritura de constitución de SOCIEDAD DE RESPONSABILIDAD LIMITADA LABORAL, que se regirá por las siguientes

[OPCIONAL — incluir si procede]

(Sociedad Anónima Laboral)

PRIMERO.- Que los mentados Sres. han convenido constituir una Sociedad Anónima Laboral por el procedimiento de fundación simultánea y para la realización de [ACTIVIDAD]

SEGUNDO.- Que a tales efectos, y en su calidad de únicos socios fundadores y socios trabajadores que lo serán de la futura compañía, han decidido otorgar la presente escritura de constitución de SOCIEDAD ANÓNIMA LABORAL, que se regirá por las siguientes

ESTIPULACIONES

I.- Constitución y socios fundadores

En el presente acto los comparecientes

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS],

Según intervienen y como socios fundadores y trabajadores, proceden a constituir una Sociedad de Responsabilidad Limitada Laboral de nacionalidad española que se regirá por el presente contrato, por los estatutos que en el mismo se aprueban, y en lo en ellos no dispuesto y en cuanto no sean contrarios a la misma, por la Ley 44/2015, de 14 de octubre, de Sociedades Laborales y Participadas, por el Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el Texto Refundido de la Ley de Sociedades de Capital y demás normas legales y reglamentarias que resulten de aplicación.

Presentes todos los socios y en relación con lo establecido en los Estatutos sociales, designan como cuentas de correo electrónico de cada uno de ellos y a todos los efectos, las siguientes:

II.- Denominación

La Sociedad se denomina «, [ELEGIR: SRLL / SAL] », denominación que no se halla registrada por ninguna otra sociedad o entidad inscribible en el Registro Mercantil, según consta en la certificación negativa de denominación que los comparecientes exhiben y que se halla vigente, la cual procedo a unir, a requerimiento de los comparecientes, a la matriz de la presente escritura.

III.- Duración

La Sociedad tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de la presente escritura, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Sociedad en momentos anteriores al de su inscripción en el Registro Mercantil.

Los ejercicios sociales se computarán por años naturales.

IV.- Domicilio

El domicilio de la Sociedad se halla situado en [DIRECCIÓN], [LOCALIDAD]

V.- Objeto social

El objeto social de la Sociedad será [OBJETO SOCIAL]

VI.- Capital social

[OPCIONAL — incluir si procede]

Sociedad Limitada Laboral

El capital social será de [IMPORTE] euros, dividido en [Nº] participaciones DE CLASE LABORAL, de [IMPORTE] euros de valor nominal cada una de ellas, numeradas de manera correlativa con los números 1 a

Dicho capital social ha sido totalmente suscrito y desembolsado por los socios fundadores, habiendo realizado cada uno de ellos las aportaciones que se describen:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], aporta [DESCRIPCIÓN DEL BIEN] por lo que se le asignan [Nº] participaciones, que son las numeradas [Nº] a [Nº]

Todas las aportaciones han sido realizada a título de propiedad, y se han efectuado en moneda nacional realidad que se acredita mediante certificación del depósito de las correspondientes cantidades a nombre de la sociedad en la entidad de crédito [ENTIDAD BANCARIA], certificación que se halla vigente según compruebo al observar la fecha del depósito al que hace referencia, y cuyo original se me entrega para ser incorporado a la presente escritura, lo cual procedo a efectuar a requerimiento de los comparecientes, quedando la misma unida al final de esta matriz.

[OPCIONAL — incluir si procede]

(Sociedad Anónima Laboral)

El capital social será de [IMPORTE] euros, dividido en [Nº] acciones de clase laboral de [IMPORTE] euros de valor nominal cada una de ellas, numeradas de manera correlativa con los números 1 a [Nº] y representadas mediante títulos nominativos.

Dicho capital social ha sido totalmente suscrito y desembolsado por los socios fundadores, habiendo realizado cada uno de ellos las aportaciones que se describen:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], aporta [DESCRIPCIÓN DEL BIEN] y suscribe [Nº] acciones, que son las numeradas [Nº] a [Nº]

La totalidad de dichas aportaciones ha sido realizada a título de propiedad, y se han efectuado en moneda nacional realidad que se acredita mediante certificación del depósito de las correspondientes cantidades a nombre de la sociedad en la entidad de crédito [ENTIDAD BANCARIA], certificación que se halla vigente según compruebo al observar la fecha del depósito al que hace referencia, y cuyo original se me entrega para ser incorporado a la presente escritura, lo cual procedo a efectuar a requerimiento de los comparecientes, quedando la misma unida al final de esta matriz.

VII.- Administración, representación inicial de la sociedad y WEB corporativa

Inicialmente se encomienda la administración y representación de la Sociedad a D./Dña. [NOMBRE Y APELLIDOS] mayor de edad con NIF [NIF] y domicilio en [LOCALIDAD] en calidad de Administrador único de la misma, por el plazo estatutario de [Nº] años, quien acepta el cargo en el presente acto, manifestando no hallarse incurso en ninguno de los supuestos legales ni estatutarios inhabilitantes para el ejercicio del mismo.

Igualmente se encomienda al citado Administrador inicial único la presentación de esta escritura constitutiva para su inscripción en el Registro Mercantil de [LOCALIDAD], quien se compromete a su cumplimiento.

Se acuerda asimismo por unanimidad la creación de la página WEB corporativa de la Sociedad, de conformidad con los Estatutos Sociales y la Ley de Sociedades de Capital, delegando en el órgano de administración la elección de la dirección URL o sitio en la Web de la web corporativa, que una vez concretada comunicará dicho órgano de administración a todos los socios.

VIII.- Aprobación de los estatutos sociales

Se procede a la aprobación de los Estatutos que han de regir el funcionamiento de la Sociedad, que los comparecientes me otorgan en este acto, extendidos en [Nº] folios, aprobados y firmados por ellos, que ratifican y elevan a escritura pública mediante su incorporación a la presente, que solicitan expresamente, lo cual efectúo uniéndolos al final de esta matriz.

IX.- Facultades de subsanación

Los comparecientes se otorgan poder recíproco para que cualquiera de ellos, por sí o en representación de los demás, pueda proceder a la subsanación o rectificación de la presente escritura y de los Estatutos a ella incorporados siempre que ello sea preciso para su obligada inscripción en el Registro Mercantil de [LOCALIDAD], y siempre que las citadas subsanaciones o rectificaciones se limiten a meros errores materiales, o a aceptar las modificaciones procedentes de la calificación registral.

X.- Comunicación al Registro Mercantil

[ELEGIR UNA OPCIÓN: Presentación telemática / Presentación no telemática]

XI.- Protección de datos personales

Advierto expresamente al compareciente que sus datos van a ser incorporados al fichero del Protocolo y documentación notarial y al fichero de Administración y organización, así como del hecho de que, en su caso, tales datos pueden ser cedidos a aquellas Administraciones públicas que según una norma con rango de ley tengan derecho a ello. Hechas las advertencias de sus derechos al respecto.

XII.- Reservas y advertencias legales

Se han hecho las reservas y advertencias legales, en especial advierto de la necesidad de la inscripción en el Registro Mercantil de los actos formalizados en esta escritura y en particular y a efectos fiscales he advertido a los comparecientes de la obligación de presentación de la documentación a liquidar dentro de plazo y de las obligaciones y responsabilidades tributarias que les incumben en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se derivarían de la inexactitud de sus declaraciones.

OTORGAMIENTO Y AUTORIZACIÓN NOTARIAL

Les leo, por su elección, esta escritura, advertidos de su derecho a leerla por sí, del que no usan y, tras hacerles las oportunas explicaciones verbales para su cabal conocimiento, manifiestan quedar enterados, la aceptan, se ratifican y firman.

Yo, el Notario, Doy fe de que el consentimiento ha sido libremente prestado y de que el otorgamiento se adecua a la legalidad y a la voluntad debidamente informada de los otorgantes.

Queda extendida en un total de [Nº] folios de papel notarial, el primero con el número y los demás con los números siguientes en orden correlativo.

Y de su contenido, DOY FE.

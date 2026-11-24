---
name: escritura-publica-constitucion-cooperativa-mer-0444
description: "Escritura pública de constitución de una cooperativa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de constitución de una cooperativa

> Formulario **MER-0444** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública de constitución de una Cooperativa, en la que se establecen y concretan, entre otras cosas, las pautas y condiciones necesarias para su funcionamiento, denominación, duración, domicilio, objeto y capital social, Primer Consejo Rector o Administrador Único e Interventor, y disolución de la misma.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de constitución de una cooperativa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de constitución de una cooperativa” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:escritura-publica-constitucion-cooperativa-mer-0444`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] Nº (9 veces)
- [ ] NACIONALIDAD (7 veces)
- [ ] IMPORTE (5 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] CLASE DE COOPERATIVA (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] COLEGIO
- [ ] DESCRIBIR
- [ ] DIRECCIÓN
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] ENTIDAD BANCARIA
- [ ] FECHA
- [ ] LUGAR
- [ ] Nº DE ARTÍCULO
- [ ] NÚMERO
- [ ] PROFESIÓN

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

Modelo de escritura pública de constitución de una Cooperativa, en la que se establecen y concretan, entre otras cosas, las pautas y condiciones necesarias para su funcionamiento, denominación, duración, domicilio, objeto y capital social, Primer Consejo Rector o Administrador Único e Interventor, y disolución de la misma.


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

Ante mí, Notario del Ilustre Colegio de [COLEGIO]

COMPARECEN

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO],

INTERVIENEN

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Los señores comparecientes intervienen en su propio nombre y derecho

En nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], domiciliado en [DOMICILIO], con DNI [DNI/NIE]

Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente escritura de constitución de SOCIEDAD COOPERATIVA [DENOMINACIÓN SOCIAL], a cuyo fin

EXPONEN

Primero.- Que los mentados Sres. han convenido constituir una Sociedad Cooperativa [CLASE DE COOPERATIVA] para [ACTIVIDAD]

Segundo.- Que, a tales efectos, y en su calidad de únicos promotores de la misma, manifiestan que reúnen los requisitos necesarios para ser socios que se recogen en el artículo [Nº DE ARTÍCULO] de los Estatutos que acompañan a la presente escritura, y expresan su voluntad de otorgar la presente escritura de constitución de SOCIEDAD COOPERATIVA [DENOMINACIÓN SOCIAL], que se regirá por las siguientes:

ESTIPULACIONES

I.- Constitución y socios promotores

En el presente acto los comparecientes, según intervienen y como socios promotores, proceden a constituir una Sociedad Cooperativa de [CLASE DE COOPERATIVA] de nacionalidad española que se regirá por el presente contrato, por los estatutos que en el mismo se aprueban, y en lo en ellos no dispuesto y en cuanto no sean contrarios a la misma, por la Ley 27/1999, de 16 de julio, de Cooperativas.

II.- Denominación

La Cooperativa se denominará ‘[DENOMINACIÓN SOCIAL], S.Coop.’, denominación que no se halla registrada por ninguna otra sociedad o entidad inscribible en el Registro Mercantil, según consta en la certificación negativa de denominación que los comparecientes exhiben y que se halla vigente, la cual procedo a unir, a su requerimiento, a la matriz de la presente escritura.

III.- Duración

La Cooperativa tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de la presente escritura, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Cooperativa en momentos anteriores al de su inscripción en el Registro de Sociedades Cooperativas.

Los ejercicios sociales se computarán por años naturales.

IV.- Domicilio y web corporativa

El domicilio de la Cooperativa se halla situado en [DIRECCIÓN], [LOCALIDAD]

La Sociedad contará con una web corporativa en la que constarán el domicilio social y los datos identificativos y registrales de la cooperativa, en los términos previstos en el artículo 3 bis de la LCoop.

Las personas socias podrán acceder, a través de la correspondiente clave, a la información contenida en dicha web y a la sede electrónica de la sociedad.

V.- Objeto social

El objeto social de la Cooperativa será [ACTIVIDAD]

VI.- Capital social

El capital social será de [IMPORTE] euros.

Dicho capital social está constituido por las aportaciones de los socios, quienes acreditan haber suscrito, cada uno de ellos, más de [IMPORTE] euros, que es la considerada aportación obligatoria mínima al capital para ser socio, habiendo realizado cada uno de ellos las aportaciones que se describen:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], aporta [IMPORTE] y suscribe [Nº] un total de [IMPORTE] euros.

La totalidad de dichas aportaciones ha sido realizada a título de propiedad, y se han efectuado en moneda nacional, realidad que se acredita mediante certificación del depósito de las correspondientes cantidades a nombre de la cooperativa en la entidad de crédito [ENTIDAD BANCARIA], certificación que se halla vigente según compruebo al observar la fecha del depósito al que hace referencia, y cuyo original se me entrega para ser incorporado a la presente escritura, lo cual procedo a efectuar a requerimiento de los comparecientes, quedando la misma unida al final de esta matriz.

Igualmente compruebo que el importe total de las aportaciones desembolsadas no es inferior al capital social mínimo establecido estatutariamente.

VII.- Gastos de constitución

La cuantía total aproximada de los gastos de constitución e incluidos los ya satisfechos se calcula que alcanzará la cifra de [IMPORTE] euros.

VIII.- Primer Consejo Rector/Administrador único e interventor

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

El primer Consejo Rector de la Cooperativa será el formado por tres personas, quedando designadas al efecto las personas y para los cargos que se dirán:

1. Ocupará la presidencia, D./Dña. [NOMBRE Y APELLIDOS], socio, de nacionalidad [NACIONALIDAD] y domicilio en [LOCALIDAD] por el plazo estatutario de [Nº] años, quien acepta el cargo en el presente acto, manifestando no hallarse incurso en ninguno de los supuestos legales ni estatutarios inhabilitantes para el ejercicio del mismo, quien asume las funciones legales y estatutarias previstas.

2. Ocupará la secretaría, D./Dña. [NOMBRE Y APELLIDOS], socio, de nacionalidad [NACIONALIDAD] y domicilio en [LOCALIDAD] por el plazo estatutario de [Nº] años, quien acepta el cargo en el presente acto, manifestando no hallarse incurso en ninguno de los supuestos legales ni estatutarios inhabilitantes para el ejercicio del mismo, quien asume las funciones legales y estatutarias previstas.

3. Ocupará la vicepresidencia D./Dña. [NOMBRE Y APELLIDOS], socio, de nacionalidad [NACIONALIDAD] y domicilio en [LOCALIDAD] por el plazo estatutario de [Nº] años, quien acepta el cargo en el presente acto, manifestando no hallarse incurso en ninguno de los supuestos legales ni estatutarios inhabilitantes para el ejercicio del mismo, quien asume las funciones legales y estatutarias previstas.

El primer interventor de la Cooperativa será D./Dña. [NOMBRE Y APELLIDOS], de nacionalidad [NACIONALIDAD] y domicilio en [LOCALIDAD], por el plazo estatutario de [Nº] años, quien acepta el cargo en el presente acto, manifestando no hallarse incurso en ninguno de los supuestos legales ni estatutarios inhabilitantes para el ejercicio del mismo.

Igualmente se encomienda al citado administrador inicial, D./Dña. [NOMBRE Y APELLIDOS], la presentación de la presente escritura constitutiva para su inscripción en el Registro de Sociedades Cooperativas de [PROVINCIA], quien se compromete a su cumplimiento en el plazo de 1 mes.

El primer Administrador de la Cooperativa será D./Dña. [NOMBRE Y APELLIDOS], socio, de nacionalidad [NACIONALIDAD] y domicilio en [LOCALIDAD] por el plazo estatutario de [Nº] años, quien acepta el cargo en el presente acto, manifestando no hallarse incurso en ninguno de los supuestos legales ni estatutarios inhabilitantes para el ejercicio del mismo, quien asume las funciones legales y estatutarias previstas para el Consejo Rector, su Presidente y su Secretario.

El primer interventor de la Cooperativa será D./Dña. [NOMBRE Y APELLIDOS], de nacionalidad [NACIONALIDAD] y domicilio en [LOCALIDAD], por el plazo estatutario de [Nº] años, quien acepta el cargo en el presente acto, manifestando no hallarse incurso en ninguno de los supuestos legales ni estatutarios inhabilitantes para el ejercicio del mismo.

Igualmente se encomienda al citado administrador inicial, D./Dña. [NOMBRE Y APELLIDOS], la presentación de la presente escritura constitutiva para su inscripción en el Registro de Sociedades Cooperativas de [PROVINCIA], quien se compromete a su cumplimiento en el plazo de 1 mes.

IX.- Aprobación de los estatutos sociales

Se procede a la aprobación de los Estatutos que han de regir el funcionamiento de la Cooperativa, que los comparecientes me otorgan en este acto, extendidos en [Nº] folios, aprobados y firmados por ellos, que ratifican y elevan a escritura pública mediante su incorporación a la presente, que solicitan expresamente, lo cual efectúo uniéndolos al final de esta matriz.

OTORGAMIENTO Y AUTORIZACIÓN NOTARIAL

Hago las reservas y advertencias legales, en especial:

a) Las referidas a la obligación de inscribir la presente en el Registro en plazo y las consecuencias de su infracción.
b) Las de carácter fiscal, y entre ellas la obligación de presentar la escritura a su liquidación en la oficina competente, en el plazo de treinta días hábiles desde este otorgamiento, y las sanciones y consecuencias que se derivarían de la falta de presentación en dicho plazo.

Leo a los comparecientes, tras advertirles del derecho que tienen a hacerlo por sí, al que renuncian, la presente escritura, prestan su consentimiento y firman conmigo.

De todo lo consignado en este instrumento público, extendido sobre [DESCRIBIR] folios de papel de uso exclusivo notarial, serie y números [Nº] yo, el Notario, doy fe.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS].

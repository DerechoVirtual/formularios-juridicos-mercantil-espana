---
name: escritura-acta-fundacional-sociedad-agraria-mer-0453
description: "Escritura de acta fundacional de una sociedad agraria de transformación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de acta fundacional de una sociedad agraria de transformación

> Formulario **MER-0453** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública de un acta fundacional de una Sociedad Agraria de Transformación, de Responsabilidad Limitada, en la que se establecen y concretan, entre otras cosas, las pautas y condiciones necesarias para su creación y funcionamiento, denominación, duración, domicilio, objeto y capital social.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de acta fundacional de una sociedad agraria de transformación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de acta fundacional de una sociedad agraria de transformación” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:escritura-acta-fundacional-sociedad-agraria-mer-0453`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] Nº (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] COLEGIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DIRECCIÓN
- [ ] LUGAR
- [ ] NACIONALIDAD
- [ ] OBJETO SOCIAL
- [ ] PORCENTAJE
- [ ] PROFESIÓN

## Normas que cita el formulario

- art. 2 Real Decreto 1776/1981

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

Modelo de escritura pública de un acta fundacional de una Sociedad Agraria de Transformación, de Responsabilidad Limitada, en la que se establecen y concretan, entre otras cosas, las pautas y condiciones necesarias para su creación y funcionamiento, denominación, duración, domicilio, objeto y capital social.


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

Los señores comparecientes intervienen en su propio nombre y derecho como PROMOTORES OTORGANTES de la SOCIEDAD AGRARIA DE TRANSFORMACIÓN que pretenden constituir.

Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente escritura de constitución de SOCIEDAD AGRARIA DE TRANSFORMACIÓN (en los sucesivo, SAT), a cuyo fin

EXPONEN

PRIMERO.- Que los mentados Sres. ostentan la condición de titulares de explotaciones agrarias en el término municipal de [LOCALIDAD]

SEGUNDO.- Que es su intención constituir una SAT en virtud de lo previsto en el Real Decreto 1776/1981, de 3 de agosto, por el que se aprueba el Estatuto que regula las Sociedades Agrarias de Transformación, y en la Orden de 14 de septiembre de 1982, por la que se desarrolla dicho Real Decreto.

A tales efectos, y en su calidad de PROMOTORES han decidido otorgar la presente escritura de ACTA FUNDACIONAL de SAT, según las siguientes

ESTIPULACIONES

I.- Constitución

Por el presente acto los comparecientes, según intervienen y como promotores otorgantes proceden a constituir una Sociedad Agraria de Transformación de nacionalidad española que se regirá por el presente contrato, por los estatutos que en el mismo se aprueban, y en lo en ellos no dispuesto y en cuanto no sean contrarios a la misma, por el Real Decreto 1776/1981, de 3 de agosto, por el que se aprueba el Estatuto que regula las Sociedades Agrarias de Transformación, y por la Orden de 14 de septiembre de 1982, por la que se desarrolla dicho Real Decreto.

II.- Denominación

La Sociedad se denomina ‘ [DENOMINACIÓN SOCIAL], S.A.T. de Responsabilidad Limitada’.

III- Duración

La Sociedad tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al de la inscripción de la presente escritura en el Registro de Sociedades Agrarias de Transformación dependiente del Ministerio de Agricultura, Pesca y Alimentación.

IV.- Domicilio

El domicilio de la Sociedad se halla situado en [DIRECCIÓN], [LOCALIDAD]

V.- Objeto social

El objeto social de la Sociedad será [OBJETO SOCIAL]

VI.- Capital social

El capital social será de [IMPORTE] euros, y se halla dividido en [Nº] resguardos nominativos de [IMPORTE] euros de valor nominal cada uno de ellos.

[OPCIONAL — incluir si procede]

Dicho capital social ha sido totalmente suscrito y desembolsado

[OPCIONAL — incluir si procede]

Dicho capital ha sido suscrito y desembolsado en un [PORCENTAJE] comprometiéndose en este acto realizar los desembolsos pendientes no más tarde de [FECHA]

Las aportaciones han sido realizadas de la siguiente forma:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], aporta [DESCRIPCIÓN DEL BIEN] y suscribe [Nº] resguardos nominativos.

VII.- Primeros cargos rectores

La primera Junta Rectora estará formada por:

D./Dña. [NOMBRE Y APELLIDOS], como Presidente

D./Dña. [NOMBRE Y APELLIDOS], como Secretario

y D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] en su calidad de Vocales

Por el plazo estatutario de [Nº] años, quienes aceptan el cargo en el presente acto, manifestando no hallarse incurso en ninguno de los supuestos legales ni estatutarios inhabilitantes para el ejercicio del mismo.

VIII.- Persona facultada para tramitar el expediente de constitución

Se encomienda a D./Dña. [NOMBRE Y APELLIDOS] la tramitación del expediente de constitución de la presente SAT y su inscripción en el Registro correspondiente, así como la realización de cuantas operaciones sean precisas para dicha finalidad, quien acepta dicho encargo.

IX.- Documentos anexos

En cumplimiento de lo previsto en el artículo 2 del Real Decreto 1776/1981, de 3 de agosto, por el que se aprueba el Estatuto que regula las Sociedades Agrarias de Transformación, se formalizan y aprueban, junto con la presente Acta fundacional, los siguientes documentos:

1º) Relación de socios [OTROS DATOS]
2º) Se procede a la aprobación de los Estatutos que han de regir el funcionamiento de la Sociedad, que los comparecientes me otorgan en este acto, extendidos en [Nº] folios, aprobados y firmados por ellos, que ratifican y elevan a escritura pública mediante su incorporación a la presente, que solicitan expresamente, lo cual efectúo uniéndolos al final de esta matriz.
3º) Memoria. [OTROS DATOS].

OTORGAMIENTO Y AUTORIZACIÓN NOTARIAL

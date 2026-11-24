---
name: escritura-constitucion-sociedad-garantia-reciproca-mer-0452
description: "Escritura de constitución de una sociedad de garantía recíproca. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de constitución de una sociedad de garantía recíproca

> Formulario **MER-0452** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de constitución de una sociedad de garantía recíproca» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de constitución de una sociedad de garantía recíproca” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:escritura-constitucion-sociedad-garantia-reciproca-mer-0452`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] Nº (7 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] IMPORTE (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] ACTIVIDAD
- [ ] CLASE
- [ ] COLEGIO
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DIRECCIÓN
- [ ] ENTIDAD BANCARIA
- [ ] FECHA
- [ ] LUGAR
- [ ] NACIONALIDAD
- [ ] NÚMERO
- [ ] PROFESIÓN
- [ ] SERIE

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

Modelo de escritura de constitución de sociedad de garantía recíproca, estando integrada la relación de socios fundadores por socios partícipes y protectores, teniendo una duración de carácter indefinido y cuyo objeto social será el otorgamiento de garantías personales por aval o por cualquier otro medio admitido en derecho diferente al seguro de caución, a favor de sus socios y para las operaciones que éstos realicen dentro del giro o tráfico de las empresas de que sean titulares, pudiendo también prestar servicios de asistencia y asesoramiento financiero a sus socios, y una vez cubiertas las reservas y obligaciones legalmente necesarias, podrá participar en sociedades y asociaciones cuyo objeto sean actividades dirigidas a pequeñas y medianas empresas.


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

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viuda / viudo / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO],

INTERVIENEN

Los señores comparecientes intervienen

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente escritura de constitución de SOCIEDAD DE GARANTÍA RECÍPROCA, a cuyo fin

EXPONEN

PRIMERO.- Que los mentados Sres. han convenido constituir una Sociedad de Garantía Recíproca para la realización de [ACTIVIDAD]

SEGUNDO.- Que, a tales efectos, y en su calidad de socios [OTROS DATOS], han decidido otorgar la presente escritura de constitución de SOCIEDAD DE GARANTÍA RECÍPROCA, que se regirá por las siguientes

ESTIPULACIONES

I.- Constitución y socios fundadores

En el presente acto los comparecientes, proceden a constituir una Sociedad de Garantía Recíproca de nacionalidad española que se regirá por el presente contrato, por los estatutos que en el mismo se aprueban, y en lo en ellos no dispuesto y en cuanto no sean contrarios a la misma, por la Ley 1/1994 de 11 de Marzo, de Sociedades de Garantía Recíproca

El proyecto de la presente escritura y los estatutos que le acompañan han sido objeto de autorización previa por el Ministerio de Economía y Hacienda, según se acredita con la mentada autorización, que dejo incorporada a la matriz de la presente escritura.

La relación de socios fundadores está integrada por los siguientes socios partícipes y protectores:

Socios partícipes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

Todos ellos [OTROS DATOS] manifiestan ser titulares de empresas con un número de trabajadores no superior a 250.

Socios protectores

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

Todos ellos manifiestan reunir los requisitos necesarios para adquirir la condición de la Sociedad, según las normas legales y estatutarias que la rigen.

II.- Denominación

La Sociedad se denomina «, SGR», denominación que no se halla registrada por ninguna otra sociedad o entidad inscribible en el Registro Mercantil, según consta en la certificación negativa de denominación que los comparecientes exhiben y que se halla vigente, la cual procedo a unir, a requerimiento de los comparecientes, a la matriz de la presente escritura.

III.- Duración

La Sociedad tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de la presente escritura, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Sociedad en momentos anteriores al de su inscripción en el Registro Mercantil.

Los ejercicios sociales se computarán por años naturales.

IV.- Domicilio

El domicilio de la Sociedad se halla situado en [DIRECCIÓN], [LOCALIDAD]

V.- Objeto social

El objeto social de la Sociedad será el otorgamiento de garantías personales por aval o por cualquier otro medio admitido en derecho diferente al seguro de caución, a favor de sus socios y para las operaciones que éstos realicen dentro del giro o tráfico de las empresas de que sean titulares.

La Sociedad también podrá prestar servicios de asistencia y asesoramiento financiero a sus socios, y una vez cubiertas las reservas y obligaciones legalmente necesarias, podrá participar en sociedades y asociaciones cuyo objeto sean actividades dirigidas a pequeñas y medianas empresas.

La Sociedad no podrá conceder directamente ninguna clase de créditos a sus socios, pero sí que podrá emitir obligaciones con sujeción a las condiciones legalmente establecidas.

VI.- Capital social fundacional

El capital social fundacional que se constituye es de [IMPORTE], dividido en [Nº] participaciones sociales de [IMPORTE] euros de valor nominal cada una de ellas, representadas por certificados numerados de manera correlativa con los números 1 a

Dicho capital social ha sido totalmente suscrito y desembolsado por los socios fundadores, habiendo realizado cada uno de ellos las aportaciones que se describen:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], aporta [DESCRIPCIÓN DEL BIEN] por lo que se le asignan [Nº] participaciones, que son las numeradas [Nº] a [Nº]

La totalidad de dichas aportaciones ha sido realizadas a título de propiedad, y se han efectuado en moneda nacional, realidad que se acredita mediante certificación del depósito de las correspondientes cantidades a nombre de la sociedad en la entidad de crédito [ENTIDAD BANCARIA], certificación que se halla vigente según compruebo al observar la fecha del depósito al que hace referencia, y cuyo original se me entrega para ser incorporado a la presente escritura, lo cual procedo a efectuar a requerimiento de los comparecientes, quedando la misma unida al final de esta matriz.

VII.- Administración

VIII.- Administración y representación inicial de la sociedad

Inicialmente se encomienda la administración y representación de la Sociedad a D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] en calidad de administradores integrantes de su Consejo de Administración, por el plazo estatutario de [Nº] años, quienes aceptan el cargo en el presente acto, manifestando no hallarse incursos en ninguno de los supuestos legales ni estatutarios inhabilitantes para el ejercicio del mismo.

Los citados consejeros manifiestan ser personas de reconocida honorabilidad comercial y profesional, y poseer conocimientos y experiencia adecuados para el ejercicio de sus funciones, según precisa el art. 43 de la Ley 1/94.

Igualmente se encomienda al citado Consejo de Administración inicial la presentación de la presente escritura constitutiva para su inscripción en el Registro Mercantil de [LOCALIDAD], quien se compromete a su cumplimiento.

IX.- Aprobación de los estatutos sociales

Se procede a la aprobación de los Estatutos que han de regir el funcionamiento de la Sociedad, que los comparecientes me otorgan en este acto, extendidos en [Nº] folios, aprobados y firmados por ellos, que ratifican y elevan a escritura pública mediante su incorporación a la presente, que solicitan expresamente, lo cual efectúo uniéndolos al final de esta matriz.

X.- Facultades de subsanación

Los comparecientes se otorgan poder recíproco para que cualquiera de ellos, por sí o en representación de los demás, pueda proceder a la subsanación o rectificación de la presente escritura y de los Estatutos a ella incorporados siempre que ello sea preciso para su obligada inscripción en el Registro Mercantil de [LOCALIDAD], y siempre que las citadas subsanaciones o rectificaciones se limiten a meros errores materiales, o a aceptar las modificaciones procedentes de la calificación registral.

OTORGAMIENTO Y AUTORIZACIÓN NOTARIAL

Hechas las reservas y advertencias legales, en particular y a efectos fiscales, advierto de las obligaciones y responsabilidades tributarias que incumben a las partes en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se pueden derivar de la eventual inexactitud de sus declaraciones.

Leo a los señores comparecientes la presente escritura, previa su renuncia a su derecho de hacerlo por sí, del que les advierto. La consienten y firman conmigo, el Notario, que doy fe de todo lo precedente consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales, de clase [CLASE], serie [SERIE], números

D./Dña. [NOMBRE Y APELLIDOS]

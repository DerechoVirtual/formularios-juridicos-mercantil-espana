---
name: escritura-constitucion-sociedad-limitada-profesional-mer-0418
description: "Escritura de constitución de una sociedad limitada profesional. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de constitución de una sociedad limitada profesional

> Formulario **MER-0418** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura de constitución de una Sociedad de Responsabilidad Limitada Profesional en la que se establecen las condiciones necesarias para su creación, organización y funcionamiento, tales como su denominación, duración, domicilio, capital social y órganos de administración. SOCIEDAD RESPONSABILIDAD LIMITADA PROFESIONAL: ESCRITURA DE CONSTITUCIÓN

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de constitución de una sociedad limitada profesional» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de constitución de una sociedad limitada profesional” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:escritura-constitucion-sociedad-limitada-profesional-mer-0418`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] COLEGIO
- [ ] CÓDIGO CNAE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] DÍA
- [ ] ESTADO CIVIL
- [ ] FECHA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE PROTOCOLO
- [ ] NÚMERO
- [ ] OBJETO SOCIAL
- [ ] PISO

## Normas que cita el formulario

- art. 20 Ley 14/2013
- art. 11.3 Ley 2/2007

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

Modelo de escritura de constitución de una Sociedad de Responsabilidad Limitada Profesional en la que se establecen las condiciones necesarias para su creación, organización y funcionamiento, tales como su denominación, duración, domicilio, capital social y órganos de administración.

SOCIEDAD RESPONSABILIDAD LIMITADA PROFESIONAL: ESCRITURA DE CONSTITUCIÓN


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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS] Notario del Ilustre Colegio de [COLEGIO]

COMPARECEN

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL] vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número

INTERVIENEN

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente escritura de constitución de SOCIEDAD LIMITADA PROFESIONAL, a cuyo fin

EXPONEN

I.- Que han decidido constituir una Sociedad profesional de nacionalidad española que se denominará [DENOMINACIÓN SOCIAL] Sociedad Limitada Profesional.

II.- Que con esta denominación no existe ninguna otra en el Registro Central de Sociedades, lo que me acreditan con la oportuna certificación del mencionado Registro que me entregan e incorporo a esta matriz, para su trascripción en las copias.

III.- Que los gastos previstos de constitución, a cargo de la sociedad hasta su inscripción en el Registro Mercantil, se estiman aproximadamente en [IMPORTE] euros.

OTORGAN

Primero.- Constitución y socios fundadores

En el presente acto los comparecientes D./Dña. [NOMBRE Y APELLIDOS] según intervienen y como socios fundadores, proceden a constituir una Sociedad de Limitada Profesional de nacionalidad española que se regirá por el presente contrato, por los estatutos que en el mismo se aprueban, y en lo en ellos no dispuesto y en cuanto no sean contrarios a la misma, por la Ley de Sociedades Profesionales.

Segundo.- Denominación

La Sociedad se denomina ", S.L. Profesional", denominación que no se halla registrada por ninguna otra sociedad o entidad inscribible en el Registro Mercantil, según consta en la certificación negativa de denominación que los comparecientes exhiben y que se halla vigente, la cual procedo a unir, a requerimiento de los comparecientes, a la matriz de la presente escritura.

Tercero.- Duración

La Sociedad tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de la presente escritura, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Sociedad en momentos anteriores al de su inscripción en el Registro Mercantil.

Los ejercicios sociales se computarán por años naturales.

La sociedad empezará sus actividades, tal como determinan los Estatutos sociales.

Cuarto.- Domicilio

El domicilio de la Sociedad se halla situado en [DIRECCIÓN] calle [CALLE] número [NÚMERO], piso [PISO]

Quinto.- Objeto social

El objeto social de la Sociedad será [OBJETO SOCIAL]. De conformidad con el art. 20 de la Ley 14/2013, de 27 de septiembre, hacen constar los comparecientes que la Clasificación Nacional de Actividades Económicas (CNAE) que le corresponderá a la entidad constituida es [CÓDIGO CNAE].

Sexto.- Capital social

[ELEGIR UNA OPCIÓN: Capital social, aportaciones y suscripción / Aportaciones dinerarias / Aportaciones no dinerarias]

Séptimo.- Administración

[ELEGIR UNA OPCIÓN: Administradores solidarios / Administradores mancomunados / Consejo de Administración / Administrador único]

Octavo.- Aprobación de los estatutos sociales

Se procede a la aprobación de los Estatutos que han de regir el funcionamiento de la Sociedad, que los comparecientes me otorgan en este acto, extendidos en [Nº] folios, aprobados y firmados por ellos, que ratifican y elevan a escritura pública mediante su incorporación a la presente, que solicitan expresamente, lo cual efectúo uniéndolos al final de esta matriz.

Noveno.- Constitución del seguro

Acreditan la constitución del seguro de responsabilidad, a que se refiere el art. 11.3 de la Ley 2/2007, de 15 de marzo, de sociedades profesionales, exhibiéndome la póliza suscrita, (o certificación) de la que dejo unida fotocopia que testimonio; el seguro concertado cubre la responsabilidad en que la sociedad pueda incurrir en el ejercicio de la actividad que constituyen su objeto.

Décimo.- Comunicación al Registro Mercantil

[ELEGIR UNA OPCIÓN: Presentación telemática / Presentación no telemática]

Undécimo.- Protección de datos personales

Advierto expresamente a los comparecientes que sus datos van a ser incorporados al fichero del Protocolo y documentación notarial y al fichero de Administración y organización, así como del hecho de que, en su caso, tales datos pueden ser cedidos a aquellas Administraciones públicas que según una norma con rango de ley tengan derecho a ello. Hechas las advertencias de sus derechos al respecto.

Reservas y advertencias legales

Se han hecho las reservas y advertencias legales, en especial advierto de la necesidad de la inscripción en el Registro Mercantil de los actos formalizados en esta escritura y en particular y a efectos fiscales he advertido a los comparecientes de la obligación de presentación de la documentación a liquidar dentro de plazo y de las obligaciones y responsabilidades tributarias que les incumben en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se derivarían de la inexactitud de sus declaraciones.

OTORGAMIENTO Y AUTORIZACIÓN

Les leo, por su elección, esta escritura, advertidos de su derecho a leerla por sí, del que no usan y, tras hacerles las oportunas explicaciones verbales para su cabal conocimiento, manifiestan quedar enterados, la aceptan, se ratifican y firman.

Yo, el Notario, Doy fe de que el consentimiento ha sido libremente prestado y de que el otorgamiento se adecua a la legalidad y a la voluntad debidamente informada de los otorgantes.

Queda extendida en un total de [Nº] folios de papel notarial, el primero con el número y los demás con los números siguientes en orden correlativo.

Y de su contenido, DOY FE.

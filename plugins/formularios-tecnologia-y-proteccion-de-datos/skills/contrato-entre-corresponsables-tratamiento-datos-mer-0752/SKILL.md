---
name: contrato-entre-corresponsables-tratamiento-datos-mer-0752
description: "Contrato entre corresponsables del tratamiento de datos personales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato entre corresponsables del tratamiento de datos personales

> Formulario **MER-0752** del plugin **Contratos tecnológicos, comercio electrónico y protección de datos** (`formularios-tecnologia-y-proteccion-de-datos`) · Mercantil › Tecnología, comercio electrónico y protección de datos · normativa revisada el 24-11-2026.

## Qué es

Contrato entre dos o más responsables que determinan conjuntamente los objetivos y los medios de un tratamiento de datos personales (corresponsables, arts. 4.7 y 26 del Reglamento (UE) 2016/679, RGPD), en el que se determinan de modo transparente y de mutuo acuerdo sus respectivas responsabilidades, especialmente respecto al ejercicio de los derechos de los interesados y a sus obligaciones de información.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato entre corresponsables del tratamiento de datos personales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato entre corresponsables del tratamiento de datos personales” para mi caso». También puedes invocarla directamente con `/formularios-tecnologia-y-proteccion-de-datos:contrato-entre-corresponsables-tratamiento-datos-mer-0752`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-tecnologia-y-proteccion-de-datos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos tecnológicos, comercio electrónico y protección de datos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL DEL CORRESPONSABLE 1
- [ ] DENOMINACIÓN SOCIAL DEL CORRESPONSABLE 2
- [ ] DESCRIPCIÓN DE LOS TRATAMIENTOS
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE DEL CORRESPONSABLE 1
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE DEL CORRESPONSABLE 2

## Normas que cita el formulario

- art. 26 RGPD

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

Notas explicativas: cuando dos o más responsables determinan conjuntamente los objetivos y los medios del tratamiento son corresponsables (arts. 4.7 y 26 RGPD). La corresponsabilidad implica, conforme al art. 82.4 RGPD, que cada responsable puede ser declarado responsable de la totalidad de los daños causados por el tratamiento sujeto a corresponsabilidad, con el fin de garantizar que el interesado reciba una compensación. El art. 29 de la LO 3/2018 (LOPDGDD) dispone que la determinación de las responsabilidades del art. 26.1 RGPD se realizará atendiendo a las actividades que efectivamente desarrolle cada uno de los corresponsables. Las entidades corresponsables están obligadas a suscribir un acuerdo que recoja sus respectivas funciones y responsabilidades en el cumplimiento de la normativa de protección de datos, en particular en cuanto al ejercicio de los derechos del interesado (que puede ejercerse frente a cualquiera de ellos) y a sus respectivas obligaciones de suministro de información (considerando 79 RGPD).


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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte, D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTANTE DEL CORRESPONSABLE 1], con DNI/NIE [DNI/NIE], que interviene en representación de [DENOMINACIÓN SOCIAL DEL CORRESPONSABLE 1], con domicilio social en [DOMICILIO] y NIF [NIF], en su calidad de CORRESPONSABLE 1 DEL TRATAMIENTO DE DATOS de esta, en adelante «el CORRESPONSABLE 1».

De otra parte, D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTANTE DEL CORRESPONSABLE 2], con DNI/NIE [DNI/NIE], que interviene en representación de [DENOMINACIÓN SOCIAL DEL CORRESPONSABLE 2], con domicilio social en [DOMICILIO] y NIF [NIF], en su calidad de CORRESPONSABLE 2 DEL TRATAMIENTO DE DATOS de esta, en adelante «el CORRESPONSABLE 2».

Ambos comparecientes se reconocen mutua y recíprocamente suficiente capacidad para obligarse entre sí por medio del presente CONTRATO DE CORRESPONSABILIDAD EN EL TRATAMIENTO DE DATOS PERSONALES, conforme a lo establecido en los artículos 4.7 y 26 del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016, relativo a la protección de las personas físicas en lo que respecta al tratamiento de datos personales y a la libre circulación de estos datos (en adelante, RGPD), y a tal fin,

EXPONEN

A) Que ambas entidades han determinado conjuntamente los objetivos y los medios del tratamiento, por lo que son consideradas corresponsables del tratamiento.

B) Que, en cumplimiento con lo dispuesto en el artículo 26 del RGPD, el tratamiento de datos de carácter personal de los corresponsables requiere la determinación de modo transparente y de mutuo acuerdo de las responsabilidades respectivas, especialmente respecto al ejercicio de los derechos del interesado y sus obligaciones de suministro de información.

De acuerdo con lo anterior, las partes suscriben el presente contrato, que se regirá de conformidad con las siguientes

CLÁUSULAS

PRIMERA.– Definiciones

Responsable del tratamiento: persona física o jurídica, de naturaleza pública o privada, u órgano administrativo, que decida sobre la finalidad, contenido y uso del tratamiento.

Corresponsables del tratamiento: aquellos responsables que determinan conjuntamente los objetivos y los medios del tratamiento.

SEGUNDA.– Objeto y alcance

Las presentes cláusulas tienen por objeto regular las relaciones entre ambos corresponsables del tratamiento de los datos que sean necesarios para los tratamientos siguientes: [DESCRIPCIÓN DE LOS TRATAMIENTOS].

TERCERA.– Confidencialidad

Toda la información de cualquier clase que obtenga o sea expuesta por ambas partes será tratada de forma confidencial, obligándose a proteger esta información del mismo modo que protege la confidencialidad de la información de su propiedad de similar naturaleza y a su no revelación a terceros bajo ningún concepto. Esta obligación de confidencialidad existirá aun después de la conclusión de los servicios objeto de este contrato.

Los firmantes de este contrato se informan recíprocamente de que sus respectivos datos personales recogidos en el mismo serán tratados de acuerdo con la legislación vigente en materia de protección de datos de carácter personal, con la finalidad del desarrollo del presente contrato, sin que sean cedidos a terceros salvo que sea necesario por imposición legal.

Las partes se comprometen a tratar los datos personales de acuerdo con lo dispuesto en el RGPD, en la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, y en la normativa aplicable en la materia.

Las partes se comprometen a informar a los titulares de los datos de los fines para los que se van a tratar sus datos, así como a recabar, en su caso, los consentimientos necesarios para poder tratar legítimamente los datos personales.

Para ejercitar los derechos de acceso, rectificación, supresión u oposición, así como el resto de derechos reconocidos en el RGPD y en la Ley Orgánica 3/2018, los firmantes deberán dirigirse, en su caso, a la dirección de quien, respectivamente, actúa como contraparte y cuya determinación figura en el encabezamiento de este contrato.

CUARTA.– Obligaciones de los corresponsables del tratamiento

Los corresponsables del tratamiento se obligan a:

1. Garantizar a los interesados, ante cualquiera de los corresponsables, el ejercicio de los derechos de acceso, rectificación, supresión y oposición; limitación del tratamiento; portabilidad de datos; y a no ser objeto de decisiones individualizadas automatizadas (incluida la elaboración de perfiles).

2. Resolver dentro del plazo establecido las solicitudes de ejercicio de derechos y comunicar a la otra parte la recepción de la solicitud, a fin de que puedan resolver conjuntamente dichas solicitudes.

3. Facilitar, en el momento de la recogida de los datos, la información relativa a los tratamientos de datos que se van a realizar, incluyendo la identidad de los diversos responsables del tratamiento.

4. Realizar conjuntamente las evaluaciones de impacto relativas a la protección de datos, cuando proceda.

5. Poner mutuamente a su disposición toda la información necesaria para demostrar el cumplimiento de sus obligaciones, así como para la realización de las auditorías o las inspecciones que realicen el corresponsable u otro auditor autorizado por él.

6. Implantar las medidas de seguridad necesarias.

7. Designar un delegado de protección de datos, cuando proceda, y comunicar su identidad y datos de contacto al otro corresponsable.

QUINTA.– Duración y resolución del contrato

El presente contrato se considera accesorio a la condición de las partes de corresponsables del tratamiento, por lo que su duración y extinción quedan supeditadas a la existencia de dicha condición.

SEXTA.– Subcontratación

Las partes se informarán recíprocamente de las subcontrataciones que realicen en el tratamiento de los datos objeto de este contrato.

Si fuera necesario subcontratar algún tratamiento, este hecho se deberá comunicar previamente y por escrito a la otra parte, con una antelación de 15 días, indicando los tratamientos que se pretende subcontratar e identificando de forma clara e inequívoca la empresa subcontratista y sus datos de contacto.

El subcontratista tendrá la condición de encargado del tratamiento y estará obligado igualmente a cumplir las obligaciones establecidas en este documento para el encargado del tratamiento y las instrucciones que dicte su responsable. En el caso de incumplimiento por parte del subencargado, el encargado inicial seguirá siendo plenamente responsable ante el responsable en lo referente al cumplimiento de las obligaciones.

SÉPTIMA.– Notificación de violaciones de la seguridad de los datos objeto de este contrato

Las partes se comunicarán, sin dilación indebida, y a través de métodos que dejen constancia de tal comunicación, las violaciones de la seguridad de los datos personales a su cargo de las que tengan conocimiento, juntamente con toda la información relevante para la documentación y comunicación de la incidencia.

No será necesaria la notificación cuando sea improbable que dicha violación de la seguridad constituya un riesgo para los derechos y las libertades de las personas físicas. Si se dispone de ella, se facilitará, como mínimo, la información siguiente:

• Descripción de la naturaleza de la violación de la seguridad de los datos personales, inclusive, cuando sea posible, las categorías y el número aproximado de interesados afectados, y las categorías y el número aproximado de registros de datos personales afectados.

• Descripción de las posibles consecuencias de la violación de la seguridad de los datos personales.

• Descripción de las medidas adoptadas o propuestas para poner remedio a la violación de la seguridad de los datos personales, incluyendo, si procede, las medidas adoptadas para mitigar los posibles efectos negativos.

Si no es posible facilitar la información simultáneamente, y en la medida en que no lo sea, la información se facilitará de manera gradual sin dilación indebida.

En prueba de conformidad, las partes firman el presente contrato por duplicado y a un solo efecto, en el lugar y fecha indicados en el encabezamiento.

FIRMAS

D./Dña. [NOMBRE Y APELLIDOS] (CORRESPONSABLE 1) D./Dña. [NOMBRE Y APELLIDOS] (CORRESPONSABLE 2)

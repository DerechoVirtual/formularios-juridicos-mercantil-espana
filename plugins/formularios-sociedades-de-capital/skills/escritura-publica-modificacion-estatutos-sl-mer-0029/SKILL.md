---
name: escritura-publica-modificacion-estatutos-sl-mer-0029
description: "Escritura pública de modificación de estatutos de una SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de modificación de estatutos de una SL

> Formulario **MER-0029** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de modificación de estatutos de una SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de modificación de estatutos de una SL” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-publica-modificacion-estatutos-sl-mer-0029`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (20 veces)
- [ ] Nº DE ARTÍCULO (16 veces)
- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] OTROS DATOS (3 veces)
- [ ] SOCIOS AFECTADOS (3 veces)
- [ ] CLASE (2 veces)
- [ ] DATOS REGISTRALES (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] COLEGIO
- [ ] DIRECCIÓN
- [ ] LUGAR
- [ ] MES
- [ ] NACIONALIDAD
- [ ] OBJETO DE LA ESCRITURA
- [ ] PAÍS
- [ ] PROFESIÓN
- [ ] PÁGINA
- [ ] SERIE
- [ ] TEXTO DEL ARTÍCULO ESTATUTARIO

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

Escritura pública por la que se formaliza el acta de Junta General Extraordinaria convocada o Universal en la que se adopta el acuerdo de modificación de estatutos sociales por traslado de domicilio, modificación o sustitución del objeto social, cambio de denominación, creación y extinción anticipada de prestaciones accesorias, duración de la compañía, y modificación del régimen de transmisión de participaciones sociales

NÚMERO DE PROTOCOLO:

En [LUGAR], a [FECHA].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO].

COMPARECEN

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viuda / viudo / casada / casado], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domiciliado en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO],

INTERVIENEN

En nombre y representación de la mercantil ‘[DENOMINACIÓN SOCIAL], S.L.’ domiciliada en [DOMICILIO], constituida por tiempo indefinido mediante escritura pública autorizada por D./Dña. [NOMBRE Y APELLIDOS] Notario de [LOCALIDAD] en fecha [FECHA], con el número [NÚMERO] de los de su protocolo. La presente mercantil se halla inscrita en el Registro Mercantil de [LOCALIDAD], al [DATOS REGISTRALES]; su NIF es

Para el presente acto se encuentra facultado en virtud de su cargo de Secretario del Consejo de Administración, que asegura vigente, para el que fue designado por un plazo de [Nº] años por acuerdo de la Junta General de socios de la citada mercantil celebrada en fecha [FECHA], cuyos acuerdos fueron elevados a públicos en escritura otorgada ante D./Dña. [NOMBRE Y APELLIDOS] Notario de [LOCALIDAD], el día [FECHA], escritura que cuenta con el número [NÚMERO] de las de su protocolo y se halla inscrita en el Registro Mercantil de [LOCALIDAD], en el [DATOS REGISTRALES]. El compareciente se halla especialmente facultado para el presente acto por acuerdo de la Junta General de ‘[DENOMINACIÓN SOCIAL], S.L.’, certificación de la cual, con las firmas que la autorizan y que considero legítimas, incorporo a esta escritura, y acompañará a todas sus copias fotocopia auténtica de la misma.

Le identifico por su [ELEGIR: DNI / pasaporte / permiso de residencia] antes reseñado, y tiene, a mi juicio, según interviene, la capacidad legal necesaria para celebrar la presente escritura de [OBJETO DE LA ESCRITURA], a cuyo fin

OTORGA/N

Primero.- Convocatoria y propuesta de modificación

Que la mercantil ‘[DENOMINACIÓN SOCIAL], S.L.’ fue convocada a Junta por su Consejo de Administración mediante anuncios insertados en la página web de la sociedad [DENOMINACIÓN SOCIAL] y en el Boletín Oficial del Registro Mercantil de [LOCALIDAD] del día [FECHA] de [MES], igualmente del año en curso, a fin de su reunión en Junta General en fecha [FECHA]. El compareciente acredita dichos extremos mediante exhibición de los correspondientes ejemplares, fotocopia de los cuales, previa su solicitud, procedo a unir debidamente testimoniados a la presente escritura.

Que la propuesta de modificación de los estatutos de la compañía fue la que a continuación se transcribe literalmente:

El compareciente manifiesta que el texto íntegro de la modificación propuesta ha estado desde la convocatoria a disposición de los socios en el domicilio social.

Segundo.- Elevación a público

Que en cumplimiento de los acuerdos adoptados en la Junta General de Socios de [FECHA], la mercantil ‘[DENOMINACIÓN SOCIAL], S.L.’ eleva a público dichos acuerdos, los cuales constan en el certificado del acta de la misma expedida por D./Dña. [NOMBRE Y APELLIDOS], en su calidad de Secretario del Consejo y de la Junta, con el Visto Bueno del Presidente, cuyo contenido reproduzco a continuación.

[OPCIONAL — incluir si procede]

Tercero.- Sustitución y modificación del objeto social

A) Queda modificado el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo estará redactado de la siguiente forma:

"Art [Nº DE ARTÍCULO] - El objeto social de la sociedad es ‘.

B) Publicación del acuerdo.

[ELEGIR: Publicación o comunicación]

El compareciente manifiesta que el acuerdo ha sido comunicado en forma escrita a cada uno de los socios que no votaron a favor, con fecha [FECHA], constando la recepción del último de los envíos con fecha [FECHA].

C) Derecho de separación.

Por el compareciente se manifiesta que, existiendo derecho de separación por parte de los señores socios que no votaron a favor del acuerdo que se eleva a público por medio de la presente y que habiendo transcurrido el plazo de un mes a contar [ELEGIR: desde la publicación de dicho acuerdo en el Boletín Oficial del Registro Mercantil / desde la recepción de la comunicación citada en la letra precedente], ninguno de ellos lo ha ejercitado.

[OPCIONAL — incluir si procede]

Tercero.- Traslado del domicilio social a otro término municipal

Queda modificado el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"Art [Nº DE ARTÍCULO] - El domicilio social se halla sito en [LOCALIDAD], calle ‘.

[OPCIONAL — incluir si procede]

Tercero.- Traslado del domicilio social al extranjero

A) Queda modificado el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"Art [Nº DE ARTÍCULO]. - El domicilio social se halla sito en [LOCALIDAD], en [DIRECCIÓN].

El compareciente declara que el presente traslado de domicilio con mantenimiento de la personalidad jurídica de ‘[DENOMINACIÓN SOCIAL], S.L.’ es posible en virtud de lo previsto en el art [Nº DE ARTÍCULO] del Convenio [PAÍS] suscrito entre España y dicho país, de fecha [FECHA].

B) Publicación del acuerdo.

El compareciente manifiesta que el acuerdo ha sido publicado en la página [PÁGINA] del BORM [Nº] de fecha [FECHA]. El compareciente me muestra original de dicho anuncio, fotocopia del cual, a su petición, procedo a unir a la presente escritura.

C) Derecho de separación.

Por el compareciente se manifiesta que, existiendo derecho de separación por parte de los señores socios que no votaron a favor del acuerdo que se eleva a público por medio de la presente y que, habiendo transcurrido el plazo de un mes a contar desde la publicación de dicho acuerdo en el Boletín Oficial del Registro Mercantil, ninguno de ellos lo ha ejercitado.

[OPCIONAL — incluir si procede]

Tercero.- Cambio de la denominación social

A) Queda modificado el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"Art [Nº DE ARTÍCULO] - Denominación social: La sociedad se denomina ‘[DENOMINACIÓN SOCIAL], S.L.’, y se regirá por los presentes estatutos, así como por las disposiciones legales que le sean aplicables en cada momento’.

B) Certificado negativo de denominación.

El compareciente me exhibe y entrega, para su unión a la presente escritura, certificado negativo de denominación expedido por el Registro Mercantil Central con fecha [FECHA] por el que acredita que no existe inscrita ninguna otra entidad con la denominación adoptada por la mercantil a la que representa.

[OPCIONAL — incluir si procede]

Tercero.- Prórroga de la duración de la sociedad

A) Queda modificado el artículo [Nº DE ARTÍCULO]. de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"Art - Duración: ‘.

B) Publicación del acuerdo.

[ELEGIR: Publicación o comunicación]

El compareciente manifiesta que el acuerdo ha sido comunicado en forma escrita a cada uno de los socios que no votaron a favor, con fecha [FECHA], constando la recepción del último de los envíos con fecha [FECHA].

C) Derecho de separación.

Por el compareciente se manifiesta que, existiendo derecho de separación por parte de los señores socios que no votaron a favor del acuerdo que se eleva a público por medio de la presente y que habiendo transcurrido el plazo de un mes a contar [ELEGIR: desde la publicación de dicho acuerdo en el Boletín Oficial del Registro Mercantil / desde la recepción de la comunicación citada en la letra precedente], ninguno de ellos lo ha ejercitado

[OPCIONAL — incluir si procede]

Tercero.- Creación de Prestaciones accesorias

A) Queda modificado el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"Art [Nº DE ARTÍCULO] - Prestaciones accesorias: Consisten en [OTROS DATOS], son de carácter [ELEGIR: gratuito / retribuído], y exigibles a los socios titulares de las participaciones [SOCIOS AFECTADOS].

B) Consentimiento de los interesados.

Puesto que la citada modificación supone la creación de prestaciones accesorias para los titulares de las participaciones [SOCIOS AFECTADOS] de la mercantil, el compareciente manifiesta que el acuerdo ha sido además aceptado por cada uno de los socios afectados, en los términos obrantes en el certificado del acta de la mentada Junta, que se halla unida a la presente.

C) Igualmente manifiesta el declarante que las prestaciones accesorias referidas se han hecho constar en [OTROS DATOS] representativos de las participaciones que las llevan aparejadas.

D) Publicación del acuerdo.

[ELEGIR: Publicación o comunicación]

El compareciente manifiesta que el acuerdo ha sido comunicado en forma escrita a cada uno de los socios que no votaron a favor, con fecha [FECHA], constando la recepción del último de los envíos con fecha [FECHA].

E) Derecho de separación.

Por el compareciente se manifiesta que, existiendo derecho de separación por parte de los señores socios que no votaron a favor del acuerdo que se eleva a público por medio de la presente y que habiendo transcurrido el plazo de un mes a contar [ELEGIR: desde la publicación de dicho acuerdo en el Boletín Oficial del Registro Mercantil / desde la recepción de la comunicación citada en la letra precedente] ninguno de ellos lo ha ejercitado.

[OPCIONAL — incluir si procede]

Tercero.- Extinción anticipada de prestaciones accesoria

A) Queda modificado el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"Art [Nº DE ARTÍCULO] - Prestaciones accesorias:

B) Consentimiento de los interesados.

Puesto que la citada modificación supone la creación de prestaciones accesorias para los titulares de las participaciones [SOCIOS AFECTADOS] de clase [CLASE] de la mercantil, el compareciente manifiesta que el acuerdo ha sido además aceptado por cada uno de los socios afectados, en los términos obrantes en el certificado del acta de la mentada Junta, que se halla unida a la presente.

C) Igualmente manifiesta el declarante que las prestaciones accesorias referidas se han hecho constar en [OTROS DATOS] representativos/as de las participaciones que las llevan aparejadas.

D) Publicación del acuerdo.

[ELEGIR: Publicación o comunicación]

El compareciente manifiesta que el acuerdo ha sido comunicado en forma escrita a cada uno de los socios que no votaron a favor, con fecha [FECHA], constando la recepción del último de los envíos con fecha [FECHA].

E) Derecho de separación.

Por el compareciente se manifiesta que, existiendo derecho de separación por parte de los señores socios que no votaron a favor del acuerdo que se eleva a público por medio de la presente y que habiendo transcurrido el plazo de un mes a contar [ELEGIR: desde la publicación de dicho acuerdo en el Boletín Oficial del Registro Mercantil / desde la recepción de la comunicación citada en la letra precedente] ninguno de ellos lo ha ejercitado.

[OPCIONAL — incluir si procede]

Tercero.- Modificación del régimen de transmisión de las participaciones de la compañía y de los estatutos sociales

A) Queda modificado el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"Art [Nº DE ARTÍCULO] - Régimen de transmisión [TEXTO DEL ARTÍCULO ESTATUTARIO]

B) Publicación del acuerdo.

[ELEGIR: Publicación o comunicación]

El compareciente manifiesta que el acuerdo ha sido comunicado en forma escrita a cada uno de los socios que no votaron a favor, con fecha [FECHA], constando la recepción del último de los envíos con fecha [FECHA].

C) Derecho de separación.

Por el compareciente se manifiesta que, existiendo derecho de separación por parte de los señores socios que no votaron a favor del acuerdo que se eleva a público por medio de la presente y que habiendo transcurrido el plazo de un mes a contar [ELEGIR: desde la publicación de dicho acuerdo en el Boletín Oficial del Registro Mercantil / desde la recepción de la comunicación citada en la letra precedente], ninguno de ellos lo ha ejercitado.

Cuarto.- Se solicita por el compareciente la inscripción de la presente escritura en el Registro Mercantil, incluso parcial para el caso de que por parte del Registrador se detectasen defectos en la misma que impidieren su inscripción total.

Advierto expresamente al compareciente que sus datos van a ser incorporados al fichero del Protocolo y documentación notarial y al fichero de Administración y organización, así como del hecho de que, en su caso, tales datos pueden ser cedidos a aquellas Administraciones públicas que según una norma con rango de ley tengan derecho a ello..

Hechas las reservas y advertencias legales, en particular y a efectos fiscales, advierto de las obligaciones y responsabilidades tributarias que incumben a las partes en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se pueden derivar de la eventual inexactitud de sus declaraciones.

Leo a los señores comparecientes la presente escritura, previa su renuncia a su derecho de hacerlo por sí, del que les advierto. La consienten y firman conmigo, el Notario, que doy fe de todo lo precedente consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales, de clase [CLASE], serie [SERIE], números [Nº].

D./Dña. [NOMBRE Y APELLIDOS]

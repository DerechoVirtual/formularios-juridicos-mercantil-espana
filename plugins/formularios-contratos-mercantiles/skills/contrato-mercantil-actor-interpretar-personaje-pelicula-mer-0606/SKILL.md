---
name: contrato-mercantil-actor-interpretar-personaje-pelicula-mer-0606
description: "Contrato mercantil de un actor para interpretar un personaje en una película. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato mercantil de un actor para interpretar un personaje en una película

> Formulario **MER-0606** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato mercantil de un actor para interpretar un personaje en una película» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato mercantil de un actor para interpretar un personaje en una película” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-mercantil-actor-interpretar-personaje-pelicula-mer-0606`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] FECHA (3 veces)
- [ ] NOMBRE DEL PERSONAJE (3 veces)
- [ ] Nº (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] TÍTULO DE LA PELÍCULA (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LUGAR (2 veces)
- [ ] IMPORTE
- [ ] MEDIO DE PAGO
- [ ] NIF
- [ ] NOMBRE DE LA ENTIDAD DE GESTIÓN
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] PLAZO
- [ ] SEDE
- [ ] ÓRGANO

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

Contrato mercantil de prestación artística del actor como intérprete de un personaje en la película que la productora tiene intención de rodar.

En [LUGAR], a [FECHA].

REUNIDOS

De una parte, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO].

De la otra parte, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO].

INTERVIENEN

D./Dña. [NOMBRE Y APELLIDOS], en lo sucesivo EL ACTOR, en su propio nombre y derecho.

D./Dña. [NOMBRE Y APELLIDOS] en representación de la mercantil [NOMBRE DEL REPRESENTADO/A], con domicilio en [LOCALIDAD] y NIF número [NIF] en uso del poder otorgado ante D./Dña. [NOMBRE Y APELLIDOS], Notario de [LOCALIDAD], el [FECHA], bajo el número [NÚMERO] de los de su protocolo, y por medio del cual se halla facultado para ejercitar, entre otras, las siguientes facultades: (hacer constar aquellas que se precisen para el contrato de prestación artística), en lo sucesivo LA PRODUCTORA.

Se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de PRESTACIÓN ARTÍSTICA y a tal fin,

MANIFIESTAN

I.- Que LA PRODUCTORA tiene la intención de proceder al rodaje de una película cinematográfica que se denominará [TÍTULO DE LA PELÍCULA].

II.- Que por tal motivo LA PRODUCTORA está interesada en contratar al ACTOR para que interprete al personaje [NOMBRE DEL PERSONAJE] de dicha película en la forma y condiciones que se dirán.

Por ello ambas partes acuerdan la celebración del presente contrato que se sujetará a las siguientes

CLÁUSULAS

Primera.- El objeto del presente contrato es la prestación artística del ACTOR como intérprete del personaje [NOMBRE DEL PERSONAJE] en la película [TÍTULO DE LA PELÍCULA] cuya duración se estima que será de aproximadamente [Nº] minutos, previéndose una aparición total en pantalla del ACTOR de [Nº] minutos, de los cuales [Nº] minutos se corresponderán con primeros planos y diálogos en los que intervendrá EL ACTOR.

Segunda.- La prestación artística del ACTOR consistirá en realizar la actividad interpretativa del personaje [NOMBRE DEL PERSONAJE] en la película [TÍTULO DE LA PELÍCULA], de conformidad con el guion redactado para la misma que se une al presente contrato como Anexo I, y sin perjuicio de las posibles modificaciones de las que este pueda ser objeto, siempre que las mismas sean aprobadas por LA PRODUCTORA.

Tercera.- LA PRODUCTORA se obliga a abonar al ACTOR la cantidad de [IMPORTE] euros, importe que incluye la cesión que EL ACTOR efectúa en beneficio de LA PRODUCTORA de sus derechos de explotación. La citada cantidad le será abonada al ACTOR mediante [ÓRGANO] en [MEDIO DE PAGO].

Cuarta.- EL ACTOR cede a LA PRODUCTORA, en virtud del presente contrato, cuantos derechos de explotación le correspondan de su actuación objeto del mismo según lo previsto en el Real Decreto Legislativo 1/1996, de 12 de abril, por el que se aprueba el Texto Refundido de la Ley de Propiedad Intelectual, excepto los que en dicho cuerpo legal se consideran irrenunciables.

Dicha cesión se realiza en exclusiva, de manera perpetua y para todo ámbito geográfico, comprendiendo los siguientes derechos:

a) Sobre sus interpretaciones y grabaciones en la película.
b) Derecho de uso de su nombre propio y artístico así como de su imagen en relación con la explotación de la película que se efectúe según lo previsto en el presente contrato y para y en su promoción y publicidad sin límite temporal o espacial alguno, entendiéndose expresamente comprendida la cesión de los derechos de remake.
c) Derecho de uso de la película y de cualquier fotografía, cartel, o cualquier otro elemento de la misma y especialmente las fotografías, imágenes, registros sonoros y de voz o efectos, así como cualquier toma o actuación del ACTOR en o para la película, incluidos los ensayos. Expresamente reconoce EL ACTOR que cualquier modificación, alteración, variación, traducción, doblaje o subtitulado de la película o sus tomas efectuado por LA PRODUCTORA o los eventuales licenciatarios de ésta no serán considerados deformaciones ni cualquier otra clase de atentado contra la interpretación
d) Distribución, reproducción y comunicación pública por cualquier medio de ámbito nacional, incluidas las televisiones locales, regionales o internacionales; bien sean de titularidad pública o privada; cualquiera que sea el medio utilizado para emitir sus señales; ya sean dichas señales de pago o codificadas o se transmitan libremente, incluida su eventual captación por satélite aun cuando su origen sea de una entidad distinta a la que envía dicha señal.
e) Distribución, reproducción y comunicación pública de la película para su incorporación a formato vídeo doméstico que se destine a su venta, alquiler o préstamo, bien de forma individual o bien formando parte de una colección.
f) Distribución, reproducción, comunicación pública y transformación en fragmentos de la película, respetando en todo caso el derecho moral del ACTOR, para su posterior incorporación a cualquier producción o grabación audiovisual, incluso cuando vayan a destinarse a fines publicitarios.
g) Distribución, reproducción y comunicación pública por cualquier otro medio de explotación que no haya sido citado en los párrafos precedentes.

No obstante todo lo anterior, la cesión de los derechos de explotación que EL ACTOR realiza a favor de LA PRODUCTORA deja a salvo el derecho del ACTOR a la remuneración que le corresponda por sus derechos de alquiler, que será fijada por la entidad de gestión de los derechos de autor [NOMBRE DE LA ENTIDAD DE GESTIÓN] a la que pertenece EL ACTOR.

Quinta.- EL ACTOR se obliga a participar en cuantos eventos sean necesarios para la debida promoción y publicidad de la película, participando, a requerimiento de LA PRODUCTORA, en cuantas sesiones fotográficas, campañas, galas, presentaciones, estrenos, y demás actuaciones promocionales se realicen para tal fin.

Sexta.- EL ACTOR autoriza a LA PRODUCTORA para que tanto su imagen como su voz y su nombre propio y/o artístico sean utilizados a modo de reclamo publicitario de la película en objetos de merchandising y demás productos de publicidad.

Séptima.- LA PRODUCTORA se reserva el derecho a resolver el presente contrato en el caso de que la producción de la película fuera suspendida, o bien en caso de que la calidad de la interpretación del ACTOR no se ajuste a lo deseado, sin derecho a indemnización alguna para EL ACTOR.

Octava.- Todos los gastos de traslado del ACTOR a los lugares de ensayo y/o rodaje de la película, así como los correspondientes a su alojamiento y manutención correrán a cargo de LA PRODUCTORA.

Novena.- LA PRODUCTORA se obliga a anunciar debidamente el nombre real y/o artístico del ACTOR, obligándose, en concreto, a incluir este en los créditos finales (y, en su caso, en los iniciales) de la película (así como en los carteles de publicidad de la misma).

Décima.- EL ACTOR se compromete a seguir las instrucciones del director y/o LA PRODUCTORA así como a presentarse en las sesiones de rodaje y ensayo, mezclas o montaje en las condiciones señaladas por LA PRODUCTORA dentro del plazo previsto de rodaje de [PLAZO], según el calendario que se recoge en el Anexo II que acompaña al presente contrato.

Decimoprimera.- Las partes renuncian expresamente a su propio fuero, señalando como competente, en caso de conflicto surgido en la ejecución de lo dispuesto en el presente contrato, los Tribunales [SEDE].

Decimosegunda.- El presente contrato se regirá por lo dispuesto en el Real Decreto Legislativo 1/1996, de 12 de abril, por el que se aprueba el Texto Refundido de la Ley de Propiedad Intelectual, y demás normas de desarrollo de la misma.

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

En [LUGAR], a [FECHA].

Firma del ACTOR

Firma de LA PRODUCTORA

D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]

---
name: escritura-publica-perdida-unipersonalidad-sl-sa-mer-0229
description: "Escritura pública de pérdida de la unipersonalidad de una SL o SA por transmisión de su capital. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de pérdida de la unipersonalidad de una SL o SA por transmisión de su capital

> Formulario **MER-0229** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública por medio de la cual se da publicidad sobre la pérdida de una Sociedad de Responsabilidad Limitada de su condición de unipersonalidad, tras haberse procedido a la venta de alguna de las participaciones sociales de su único socio a otra persona, ahora también socio de la misma.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de pérdida de la unipersonalidad de una SL o SA por transmisión de su capital» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de pérdida de la unipersonalidad de una SL o SA por transmisión de su capital” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-publica-perdida-unipersonalidad-sl-sa-mer-0229`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DATOS REGISTRALES (2 veces)
- [ ] CLASE
- [ ] COLEGIO
- [ ] DOMICILIO
- [ ] INSCRIPCIÓN
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE PROTOCOLO
- [ ] NÚMERO
- [ ] PROVINCIA
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

Modelo de escritura pública por medio de la cual se da publicidad sobre la pérdida de una Sociedad de Responsabilidad Limitada de su condición de unipersonalidad, tras haberse procedido a la venta de alguna de las participaciones sociales de su único socio a otra persona, ahora también socio de la misma.


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

COMPARECE

D./Dña. [NOMBRE Y APELLIDOS] Administrador y socio único hasta la fecha, de la compañía [ELEGIR: SLU / SA], de estado civil casado/a vecino/a de [LOCALIDAD], domiciliado en [DOMICILIO], con [ELEGIR: DNI / pasaporte / permiso de residencia] número

INTERVIENE

En representación de ‘ [ELEGIR: SLU / SA] ’ constituida en fecha [FECHA] mediante escritura pública otorgada ante notario D./Dña. [NOMBRE Y APELLIDOS] el [FECHA] con el número de orden de su protocolo [Nº DE PROTOCOLO] que causó inscripción en el Registro mercantil de [PROVINCIA] en el [DATOS REGISTRALES].

Interviene en su calidad de apoderado de la sociedad antes mencionada, según consta en escritura de poder otorgada a su favor, ante notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], mediante escritura de [FECHA], con el número [NÚMERO] de orden de su protocolo que causó inscripción [INSCRIPCIÓN] en el Registro Mercantil de [LOCALIDAD] en el [DATOS REGISTRALES].

Tiene, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente escritura pública de publicidad de pérdida de situación de unipersonalidad como consecuencia de haberse transmitido alguna de las participaciones.

MANIFIESTA

Primero- Que la sociedad que representa [ELEGIR: SLU / SA] ha perdido la condición de Sociedad [ELEGIR: de Responsabilidad Limitada / Anónima] Unipersonal, por la adquisición por parte de D./Dña. [NOMBRE Y APELLIDOS] de [ELEGIR: participaciones / acciones] que pertenecían a D./Dña. [NOMBRE Y APELLIDOS], hasta esa fecha socio único de la Sociedad, tal y como se describe en escritura pública de [FECHA] otorgada en [LOCALIDAD] el día [FECHA] ante el Notario de [LOCALIDAD], por lo que el mentado D./Dña. [NOMBRE Y APELLIDOS] ha dejado de ser socio único de dicha Sociedad, según consta en el correspondiente Libro Registro que el compareciente exhibe ante mí.

SegundoSe solicita por el compareciente la inscripción de la presente escritura en el Registro Mercantil, incluso parcial si es que existiere algún defecto que a juicio del Registrador Mercantil impida la total

AUTORIZACIÓN Y OTORGAMIENTO

Hechas las reservas y advertencias legales, en particular y a efectos fiscales, advierto de las obligaciones y responsabilidades tributarias que incumben a las partes en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se pueden derivar de la eventual inexactitud de sus declaraciones.

Leo a los señores comparecientes la presente escritura, previa su renuncia a su derecho de hacerlo por sí, del que les advierto. La consienten y firman conmigo, el Notario, que doy fe de todo lo precedente consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales, de clase [CLASE], serie [SERIE], números

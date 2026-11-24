---
name: requerimiento-notarial-administradores-sa-convoquen-mer-0258
description: "Requerimiento notarial a los administradores de una SA para que convoquen junta extraordinaria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Requerimiento notarial a los administradores de una SA para que convoquen junta extraordinaria

> Formulario **MER-0258** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Acta notarial de requerimiento a los administradores de una sociedad anónima, a instancia de accionistas que representan al menos el 5% del capital social, para que convoquen Junta General Extraordinaria con el orden del día que se indica (art. 168 de la Ley de Sociedades de Capital). Es presupuesto para solicitar después la convocatoria judicial o por el Registro Mercantil si los administradores no atienden el requerimiento.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Requerimiento notarial a los administradores de una SA para que convoquen junta extraordinaria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Requerimiento notarial a los administradores de una SA para que convoquen junta extraordinaria” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:requerimiento-notarial-administradores-sa-convoquen-mer-0258`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] REPETIR EL SIGUIENTE PÁRRAFO PARA CADA COMPARECIENTE: (2 veces)
- [ ] CLASE
- [ ] COLEGIO NOTARIAL
- [ ] DATOS REGISTRALES: TOMO, FOLIO, HOJA E INSCRIPCIÓN
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] DOMICILIO SOCIAL: CALLE, NÚMERO Y PISO, MUNICIPIO Y PROVINCIA
- [ ] FIRMAS DE LOS COMPARECIENTES Y DEL NOTARIO
- [ ] NACIONALIDAD
- [ ] NIF
- [ ] Nº DE DOCUMENTO
- [ ] NÚMEROS
- [ ] OTROS ASUNTOS, SI LOS HUBIERA
- [ ] PORCENTAJE
- [ ] PORCENTAJE: MÍNIMO 5
- [ ] PROFESIÓN
- [ ] PROVINCIA
- [ ] SERIE
- [ ] TÍTULO DE ADQUISICIÓN

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

NÚMERO DE PROTOCOLO: [Nº DE PROTOCOLO]

En [LOCALIDAD], a [FECHA].

Ante mí, D./Dña. [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio de [COLEGIO NOTARIAL],

COMPARECE/N

[REPETIR EL SIGUIENTE PÁRRAFO PARA CADA COMPARECIENTE:]

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero/a / divorciado/a / separado/a judicialmente / viudo/a / casado/a], con profesión [PROFESIÓN], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [Nº DE DOCUMENTO], socio de [DENOMINACIÓN SOCIAL], S.A.

INTERVIENE/N

Todos ellos en su propio nombre y derecho.

Les identifico por sus documentos de identidad antes reseñados, y tienen, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente ACTA DE REQUERIMIENTO, a cuyo fin

EXPONE/N

Primero.- Antecedentes

a) Sociedad a cuyos administradores se requiere.

Que, por los títulos y en los conceptos que a continuación se reseñan, los comparecientes representan el [PORCENTAJE: MÍNIMO 5]% del capital social de la mercantil [DENOMINACIÓN SOCIAL], S.A., cuyos datos son los siguientes:

Su domicilio social se halla sito en [DOMICILIO SOCIAL: CALLE, NÚMERO Y PISO, MUNICIPIO Y PROVINCIA] y fue constituida por [ELEGIR: tiempo indefinido / plazo determinado] mediante escritura autorizada por el Notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO] el [FECHA], bajo el número [Nº DE PROTOCOLO] de los de su protocolo.

La citada sociedad se halla inscrita en el Registro Mercantil de [PROVINCIA], [DATOS REGISTRALES: TOMO, FOLIO, HOJA E INSCRIPCIÓN], y le corresponde el NIF número [NIF].

b) Títulos y porcentajes.

[REPETIR EL SIGUIENTE PÁRRAFO PARA CADA COMPARECIENTE:]

D./Dña. [NOMBRE Y APELLIDOS] manifiesta ser socio de [DENOMINACIÓN SOCIAL], S.A., como propietario y titular de [Nº] acciones, que suponen un [PORCENTAJE] por ciento del capital social, adquiridas por [TÍTULO DE ADQUISICIÓN], según resulta de los títulos que el compareciente me exhibe, sin que en lo omitido en nada amplíe, limite, condicione o contradiga lo expuesto, y en los que no figura nota alguna de transmisión posterior.

Segundo.- Requerimiento

Que los comparecientes, en el ejercicio del derecho que les reconoce el artículo 168 de la Ley de Sociedades de Capital,

Me requieren a mí, el Notario, para que, presentándome en el domicilio social de [DENOMINACIÓN SOCIAL], S.A., REQUIERA a sus administradores sociales a fin de que, en el plazo de los dos meses siguientes a la fecha en que dicho requerimiento se produzca, procedan a convocar Junta General Extraordinaria de [DENOMINACIÓN SOCIAL], S.A., en primera y segunda convocatoria, incluyendo en el orden del día los siguientes asuntos a tratar:

1.º.- [ASUNTO A TRATAR. POR EJEMPLO, AUTORIZACIÓN PARA LA VENTA DE UN ACTIVO ESENCIAL DE LA COMPAÑÍA CONSISTENTE EN EL ESTABLECIMIENTO MERCANTIL SITUADO EN [DIRECCIÓN]].

2.º.- [OTROS ASUNTOS, SI LOS HUBIERA].

Requerimiento que yo, el Notario, ACEPTO, y practicaré mediante diligencia a continuación de la presente.

Leo a los señores comparecientes la presente, previa su renuncia a su derecho de hacerlo por sí, del que les advierto. La consienten y firman conmigo, el Notario, que doy fe de todo lo precedente consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales, de clase [CLASE], serie [SERIE], números [NÚMEROS].

[FIRMAS DE LOS COMPARECIENTES Y DEL NOTARIO]

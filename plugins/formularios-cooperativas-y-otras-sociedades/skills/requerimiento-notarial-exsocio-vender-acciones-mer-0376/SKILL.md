---
name: requerimiento-notarial-exsocio-vender-acciones-mer-0376
description: "Requerimiento notarial al exsocio para vender sus acciones o participaciones laborales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Requerimiento notarial al exsocio para vender sus acciones o participaciones laborales

> Formulario **MER-0376** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Requerimiento notarial a socio con relación laboral extinguida para que proceda a la venta de sus acciones o participaciones bajo ciertas condiciones

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Requerimiento notarial al exsocio para vender sus acciones o participaciones laborales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Requerimiento notarial al exsocio para vender sus acciones o participaciones laborales” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:requerimiento-notarial-exsocio-vender-acciones-mer-0376`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (13 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] FECHA (7 veces)
- [ ] Nº (5 veces)
- [ ] NÚMERO (3 veces)
- [ ] DIRECCIÓN (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LUGAR (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] CALIDAD DE LA PERSONA QUE RECIBE LA CÉDULA
- [ ] CARGO
- [ ] COMUNIDAD AUTÓNOMA
- [ ] CONDICIÓN DEL ADQUIRENTE
- [ ] DENOMINACIÓN SOCIAL
- [ ] LUGAR DE DEPÓSITO
- [ ] NACIONALIDAD
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

Requerimiento notarial a socio con relación laboral extinguida para que proceda a la venta de sus acciones o participaciones bajo ciertas condiciones


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

NÚMERO

ACTA DE REQUERIMIENTO.

En [LUGAR], a [FECHA].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS],Notario de [LOCALIDAD] del Ilustre Colegio Notarial de [LOCALIDAD]

COMPARECE

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD], con N.I.F. número [NÚMERO], vecino/a de [LOCALIDAD],

Interviene en representación de la sociedad «[DENOMINACIÓN SOCIAL]», con N.I.F. número [NÚMERO] y domicilio en la [DIRECCIÓN], de la localidad de [LOCALIDAD], constituida en escritura autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA] número de protocolo [Nº DE PROTOCOLO] e inscrita en el Registro Mercantil de [LOCALIDAD], así como en el Registro Administrativo de Sociedades Laborales de [COMUNIDAD AUTÓNOMA] con el número

Ejerce esta representación como [CARGO] de la sociedad, cargo para el que fue nombrado por acuerdo de la junta general de fecha [FECHA], formalizado en escritura autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA] número de protocolo [Nº DE PROTOCOLO] e inscrito en el Registro Mercantil, hoja citada, inscripción número

Me asegura el señor compareciente la vigencia de su representación y me exhibe copia autorizada de la escritura de constitución de la sociedad así como la documentación acreditativa del nombramiento para el cargo de administrador.

Me aseguro de su identidad por su reseñado documento y le juzgo con capacidad legal suficiente e interés legítimo para el otorgamiento de esta acta.

El señor compareciente

EXPONE

1. Que el día [FECHA] finalizó la relación laboral del D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD] de la localidad de [LOCALIDAD], titular de las [ELEGIR: acciones / participaciones] de clase laboral números [Nº] a [Nº], ambos inclusive.

2. Que, a tenor de lo dispuesto en la Ley 44/2015, de 14 de octubre, de Sociedades Laborales y Participadas, la sociedad ha recibido propuestas de adquisición de estas [ELEGIR: acciones / participaciones] por parte de personas que reúnen los requisitos del artículo 6 de dicha Ley, según la siguiente relación:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD] de la localidad de [LOCALIDAD], que tiene la condición de [CONDICIÓN DEL ADQUIRENTE].

3. Que no habiendo sido ofrecida voluntariamente por el socio la adquisición de sus [ELEGIR: acciones / participaciones] se inicia el procedimiento previsto en la Ley 44/2015, de 14 de octubre, de Sociedades Laborales y Participadas, a los efectos del ejercicio del derecho de adquisición por los sujetos interesados.

Por todo lo cual, y mediante esta acta, el señor compareciente,

MANIFIESTA

Que me requiere a mí, el Notario, para que notifique y requiera fehacientemente al D./Dña. [NOMBRE Y APELLIDOS], cuya relación laboral ha quedado extinguida con la sociedad, para que proceda a formalizar la venta de sus [ELEGIR: acciones / participaciones], con arreglo a las siguientes condiciones:

• 1.ª La venta se efectuará por un precio de [IMPORTE] euros por cada [ELEGIR: acción / participación] según valoración efectuada por experto conforme a la Ley 44/2015, de 14 de octubre, de Sociedades Laborales y Participadas.
• 2.ª La venta se realizará mediante comparecencia ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], en la [DIRECCIÓN], de la localidad de [LOCALIDAD], ante el cual se consigna la cantidad de [IMPORTE] euros a favor del requerido, previo otorgamiento de los documentos de transmisión indicados.
• 3.ª La venta ha de formalizarse en el plazo de un mes desde la recepción del requerimiento notarial.

Con advertencia de que si hace caso omiso de este requerimiento, el órgano de administración de la sociedad procederá a otorgar los documentos de venta correspondientes y a depositar el precio de las participaciones en [LUGAR DE DEPÓSITO].

Acepto el requerimiento.

Hago al señor compareciente las reservas y advertencias legales, entre ellas la incorporación de datos a los ficheros automatizados regulados en la Orden del Ministerio de Justicia 484/2003, de 19 de febrero, y le leo, previa advertencia del derecho que tiene a hacerlo por sí, el contenido de la presente acta. Enterado, según dice, por la lectura que he realizado, el señor compareciente hace constar su aprobación al contenido del acta y la firma.

Yo, el Notario, compruebo que esta acta se adecua a la legalidad y a la voluntad debidamente informada y expresada ante mí, y del contenido de esta acta, extendido en [Nº] folios de papel timbrado notarial de serie [SERIE], números [Nº], DOY FE.

DILIGENCIA DE NOTIFICACIÓN. Referida al acta número [NÚMERO] de mi protocolo general ordinario, que redacto en mi despacho según notas tomadas sobre el lugar.

En [LUGAR], a [FECHA].

A las [Nº] horas de [FECHA] me presento en el domicilio señalado por el requirente y, tras dar a conocer mi condición de Notario y el objeto de mi presencia, entrego cédula con trascripción literal del acta y advertencia del derecho reglamentario a contestar, a la persona más idónea allí encontrada, que resultó quien dijo ser [CALIDAD DE LA PERSONA QUE RECIBE LA CÉDULA], que se hizo cargo de la cédula, sin hacer manifestación alguna.

De todo lo cual, yo, el Notario, DOY FE.

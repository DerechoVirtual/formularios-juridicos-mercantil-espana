---
name: notificacion-notarial-participada-haber-superado-diez-mer-0106
description: "Notificación notarial a la participada de haber superado el diez por ciento de su capital. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Notificación notarial a la participada de haber superado el diez por ciento de su capital

> Formulario **MER-0106** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

La sociedad que, por sí misma o por medio de una sociedad filial, llegue a poseer más del diez por ciento del capital de otra sociedad deberá notificárselo de inmediato, quedando mientras tanto suspendidos los derechos correspondientes a sus participaciones. Dicha notificación habrá de repetirse para cada una de las sucesivas adquisiciones que superen el cinco por ciento del capital (art. 155.1 LSC). Aunque la normativa vigente no impone requisitos formales, es conveniente que la notificación, se efectúe de forma notarial

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Notificación notarial a la participada de haber superado el diez por ciento de su capital» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Notificación notarial a la participada de haber superado el diez por ciento de su capital” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:notificacion-notarial-participada-haber-superado-diez-mer-0106`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] FECHA (5 veces)
- [ ] Nº (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DIRECCIÓN (2 veces)
- [ ] LUGAR (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALIDAD DE LA PERSONA QUE RECIBE LA CÉDULA
- [ ] CARGO
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] ESTADO CIVIL
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

La sociedad que, por sí misma o por medio de una sociedad filial, llegue a poseer más del diez por ciento del capital de otra sociedad deberá notificárselo de inmediato, quedando mientras tanto suspendidos los derechos correspondientes a sus participaciones. Dicha notificación habrá de repetirse para cada una de las sucesivas adquisiciones que superen el cinco por ciento del capital (art. 155.1 LSC). Aunque la normativa vigente no impone requisitos formales, es conveniente que la notificación, se efectúe de forma notarial


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

ACTA DE NOTIFICACIÓN.

En [LUGAR], a [FECHA].

Ante mí, Notario de [LOCALIDAD], del Ilustre Colegio Notarial de [LOCALIDAD]

COMPARECE

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, DNI número [DNI/NIE], de estado civil [ESTADO CIVIL], vecino/a de [LOCALIDAD], [DOMICILIO].

Interviene en representación de «[DENOMINACIÓN SOCIAL], SA», constituida en escritura autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA] (número de protocolo [Nº DE PROTOCOLO]) e inscrita en el Registro Mercantil de [LOCALIDAD], N.I.F. y domicilio en la [DIRECCIÓN], de la localidad de [LOCALIDAD].

Ejerce esta representación como [CARGO] de la sociedad, cargo para el que fue nombrado por acuerdo de la junta general de fecha [FECHA], formalizado en escritura autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA] (número de protocolo [Nº DE PROTOCOLO]) e inscrito en el Registro Mercantil, hoja citada, inscripción número [NÚMERO].

Me afirma el señor compareciente la vigencia de su representación y me exhibe copias autorizadas de la escritura de constitución de la sociedad y de la escritura de nombramiento para el cargo de administrador.

Me aseguro de su identidad por su reseñado documento y le juzgo con capacidad legal suficiente e interés legítimo para el otorgamiento de la presente por la que

EXPONE

Que la sociedad que representa [DENOMINACIÓN SOCIAL] ha llegado a poseer, un [Nº] por ciento del capital de la sociedad «[DENOMINACIÓN SOCIAL]», domiciliada en la [DIRECCIÓN], de la localidad de [LOCALIDAD], y

REQUIERE

De mí, el Notario, para que notifique a la sociedad indicada, en el domicilio reseñado, la posesión del porcentaje de capital referido en la anterior parte expositiva, a los efectos del artículo 155 de la Ley de Sociedades de Capital y ejercicio de los derechos correspondientes a sus [ELEGIR: acciones / participaciones].

Acepto el requerimiento.

Hago al señor compareciente las reservas y advertencias legales y le leo, previa advertencia del derecho que tiene a hacerlo por sí, el contenido de la presente acta. Enterado, el señor compareciente hace constar su aprobación al contenido del acta y la firma.

Del contenido de esta acta, extendida en [Nº] folios de papel timbrado notarial de serie [SERIE], números [Nº], yo, el Notario, DOY FE.

DILIGENCIA DE NOTIFICACIÓN. Referida al acta número [NÚMERO] de mi protocolo general ordinario, que redacto en mi despacho según notas tomadas sobre el lugar.

En [LUGAR], a [FECHA].

A las [Nº] horas de hoy me presento en el domicilio señalado por el requirente y, tras dar a conocer mi condición de Notario y el objeto de mi presencia, entrego cédula con trascripción literal del acta y advertencia del derecho reglamentario a contestar, a la persona más idónea allí encontrada, que resultó quien dijo ser [CALIDAD DE LA PERSONA QUE RECIBE LA CÉDULA], que se hizo cargo de la cédula, sin hacer manifestación alguna.

De todo lo cual, yo, el Notario, DOY FE.

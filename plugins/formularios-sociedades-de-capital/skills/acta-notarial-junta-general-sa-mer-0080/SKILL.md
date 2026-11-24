---
name: acta-notarial-junta-general-sa-mer-0080
description: "Acta notarial de la junta general de una SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta notarial de la junta general de una SA

> Formulario **MER-0080** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Los administradores podrán requerir la presencia de notario para que levante acta de la junta general y estarán obligados a hacerlo siempre que, con cinco días de antelación al previsto para la celebración de la junta, lo soliciten socios que representen, al menos, el uno por ciento del capital social en la sociedad anónima o el cinco por ciento en la sociedad de responsabilidad limitada. En este caso, los acuerdos sólo serán eficaces si constan en acta notarial.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta notarial de la junta general de una SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta notarial de la junta general de una SA” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-notarial-junta-general-sa-mer-0080`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (9 veces)
- [ ] Nº (9 veces)
- [ ] FECHA (8 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] NÚMERO (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] ESTADO CIVIL (3 veces)
- [ ] CARGO (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] CALLE
- [ ] DESCRIPCIÓN DEL DOCUMENTO
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] PÁGINA WEB
- [ ] TOMO

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

Los administradores podrán requerir la presencia de notario para que levante acta de la junta general y estarán obligados a hacerlo siempre que, con cinco días de antelación al previsto para la celebración de la junta, lo soliciten socios que representen, al menos, el uno por ciento del capital social en la sociedad anónima o el cinco por ciento en la sociedad de responsabilidad limitada. En este caso, los acuerdos sólo serán eficaces si constan en acta notarial.


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

NÚMERO [NÚMERO]

ACTA NOTARIAL DE JUNTA GENERAL

En [LOCALIDAD], el día [FECHA]

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario de [LOCALIDAD], del Ilustre Colegio Notarial de [LOCALIDAD],

COMPARECE

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], y vecino/a de [LOCALIDAD], D.N.I.

Interviene en nombre y representación de la sociedad anónima denominada «[DENOMINACIÓN SOCIAL], SA», domiciliada en [DOMICILIO], constituida ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], e inscrita en el Registro Mercantil de [LOCALIDAD], tomo [TOMO], N.I.F.

Ejerce esta representación por ser miembro del órgano de administración de la sociedad, con nombramiento acordado por la junta general de fecha [FECHA] inscrito en el Registro Mercantil de [LOCALIDAD] el día [FECHA]. Me entrega certificación del acuerdo de nombramiento y certificación registral de la inscripción, confirmándome la vigencia del cargo.

Me aseguro de su identidad y tiene, a mi juicio, capacidad legal suficiente para este acto, estando facultado para él por razón de su cargo, y al efecto,

EXPONE

Que la sociedad «[DENOMINACIÓN SOCIAL], SA» ha convocado junta general mediante anuncio publicado el día [FECHA] en su página web [PÁGINA WEB] (o, en su caso) en el BORME de fecha [FECHA] y en el diario

Que el texto íntegro de la convocatoria de la junta general publicado es el siguiente:

D./Dña. [NOMBRE Y APELLIDOS] me entrega sendos ejemplares de las publicaciones citadas con los dos anuncios de convocatoria, que protocolizo con esta matriz

Y esto expuesto, el señor compareciente

MANIFIESTA

Que me requiere a mí, el Notario, para que asista a la celebración de la indicada junta general y levante acta notarial de la reunión a que se refieren los artículos 203 de la Ley de Sociedades de Capital y 101 del Reglamento del Registro Mercantil.

Acepto el requerimiento.

Leo la presente acta a la parte requirente, por renuncia de su derecho a leerla por sí mismo, derecho del que le he informado puntualmente. Enterado por mi lectura y explicaciones de su contenido, el señor compareciente hace contar su aprobación y la firma.

Y yo, el Notario, DOY FE, de todo lo contenido en este instrumento público, extendido en [Nº] folios de papel timbrado números [Nº]

DILIGENCIA DE PRESENCIA

Relativa a la junta general de la sociedad «[DENOMINACIÓN SOCIAL], SA», a celebrar en [DIRECCIÓN], el día [FECHA], a las [Nº] horas.

La extiendo yo, el Notario, para hacer constar las siguientes circunstancias relativas a esta reunión, celebrada con mi presencia.

Actúa como presidente de la junta general el D./Dña. [NOMBRE Y APELLIDOS], con D.N.I. número [NÚMERO], mayor de edad, de estado civil [ESTADO CIVIL], y vecino/a de [LOCALIDAD], en virtud de su cargo de [CARGO] según el artículo [Nº DE ARTÍCULO] de los estatutos sociales. Y actúa como secretario de la junta general el D./Dña. [NOMBRE Y APELLIDOS], con D.N.I. número [NÚMERO], mayor de edad, de estado civil [ESTADO CIVIL], y vecino/a de [LOCALIDAD], calle [CALLE], en virtud de su cargo de [CARGO] según el artículo [Nº DE ARTÍCULO] de los estatutos sociales. Me aseguro de su identidad por los reseñados documentos y me acreditan la vigencia de sus cargos por [DESCRIPCIÓN DEL DOCUMENTO].

La lista de asistentes ha sido redactada por el secretario de la junta señalando como resultado la asistencia personal de [Nº] socios con derecho de voto, que representan el [Nº] por ciento del capital social, y la asistencia por representación de [NOMBRE DEL REPRESENTADO/A] socios con derecho de voto, que representan el [Nº] por ciento del capital social. La asistencia total a la junta es del [Nº] por ciento del capital social y, por ello, el presidente la declara válidamente constituida. El secretario me hace entrega de la lista de asistentes, que uno a esta matriz.

El presidente comunica mi asistencia a la junta en aplicación del artículo 203 de la Ley de Sociedades de Capital con facultades para elaborar el acta de la junta. Yo, el Notario, intervengo en este momento para preguntar a los presentes si existen protestas o reservas de cualquier tipo sobre las manifestaciones del presidente relativas a la lista de asistentes y a la declaración de válida constitución de la junta.

No se produce ninguna protesta ni reserva.

A continuación se inicia el debate en la junta sobre los asuntos que constan en el orden del día de la convocatoria.

En cuanto al punto número [NÚMERO] del orden del día [FECHA]

(a) [ELEGIR: (b) / (c)]

No habiendo nada más que hacer constar, doy por finalizada mi actuación.

Del contenido de la presente diligencia, que redacto en mi estudio de acuerdo con las notas tomadas sobre el terreno, extendida a continuación del acta que la motiva, y en [Nº] folios de papel timbrado números [Nº], yo, el Notario, DOY FE.

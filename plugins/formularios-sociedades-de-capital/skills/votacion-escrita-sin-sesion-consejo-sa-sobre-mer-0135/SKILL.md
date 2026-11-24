---
name: votacion-escrita-sin-sesion-consejo-sa-sobre-mer-0135
description: "Votación escrita y sin sesión del consejo de SA sobre aceptación, nombramientos y reparto de cargos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Votación escrita y sin sesión del consejo de SA sobre aceptación, nombramientos y reparto de cargos

> Formulario **MER-0135** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

La votación por escrito y sin sesión del consejo de administración, es una modalidad que no requiere presencia física o virtual de sus miembros. Para que sea válida, se deben cumplir ciertos requisitos, como la ausencia de oposición expresa de ningun consejero y la garantía de autenticidad de los votos.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Votación escrita y sin sesión del consejo de SA sobre aceptación, nombramientos y reparto de cargos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Votación escrita y sin sesión del consejo de SA sobre aceptación, nombramientos y reparto de cargos” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:votacion-escrita-sin-sesion-consejo-sa-sobre-mer-0135`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] AÑO (3 veces)
- [ ] CALLE (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DNI/NIE
- [ ] NIF
- [ ] Nº DE ARTÍCULO

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

La votación por escrito y sin sesión del consejo de administración, es una modalidad que no requiere presencia física o virtual de sus miembros. Para que sea válida, se deben cumplir ciertos requisitos, como la ausencia de oposición expresa de ningun consejero y la garantía de autenticidad de los votos.


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

ACTA DEL CONSEJO DE ADMINISTRACIÓN SA

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], calle [CALLE], en su calidad de secretario del consejo de administración de la sociedad “[DENOMINACIÓN SOCIAL], S.A.”, con NIF número [NIF] y con domicilio sito en [LOCALIDAD], calle [CALLE], número [NÚMERO].

CERTIFICA

Que el día [DÍA] de [MES] de [AÑO] se ha recibido en el domicilio social de la sociedad una carta firmada por la totalidad de los miembros del consejo de administración señores:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

en la cual, y al amparo de lo dispuesto en el artículo 248.2 del Texto Refundido de la Ley de Sociedades de Capital y del artículo [Nº DE ARTÍCULO] de los estatutos sociales, se adoptaron los siguientes acuerdos y manifestaciones por unanimidad que constituyen, entre otras cosas, votación por escrito y sin sesión del consejo de administración, y sin que ningún miembro del consejo se haya opuesto a este procedimiento

ACUERDOS

1ª Manifestación de conocimiento y conformidad

Manifestar individualmente que conocen el acuerdo de la junta general ordinaria de la sociedad “[DENOMINACIÓN SOCIAL], S.A.”, que se celebró el día [DÍA] de [MES] de [AÑO]. Manifestar individualmente que aceptan el nombramiento como miembros del consejo de administración de la sociedad antedicha y declaran que no se hallan incursos en ninguna incompatibilidad legal para desempeñar los mismos y, en particular, en ninguna de las incompatibilidades de la Ley 3/2015, de 30 de marzo, reguladora del ejercicio del alto cargo de la Administración General del Estado.

Votaciones por escrito y sin sesión del consejo de administración, a continuación.

2ª Cese de secretario

Cesar como secretario no consejero a D./Dña.. [NOMBRE Y APELLIDOS].

3ª Elección de nuevo secretario

Elegir como secretario/a no consejero/a a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, casado, con domicilio en [LOCALIDAD], calle [CALLE], número [NÚMERO], titular del DNI número [DNI/NIE]. El nuevo secretario, abajo firmante, manifiesta que acepta el nombramiento y declara que no se halla incurso en ninguna incompatibilidad legal para desempeñar el mismo y, en particular, en ninguna de las incompatibilidades de la Ley 3/2015, de 30 de marzo, reguladora del ejercicio del alto cargo de la Administración General del Estado.

4º Distribución de cargos

Distribuir los cargos del consejo de administración de la siguiente forma:

Presidente/a, D./Dña. [NOMBRE Y APELLIDOS]

Vicepresidente/a: D./Dña. [NOMBRE Y APELLIDOS]

Vocales: D./Dña. [NOMBRE Y APELLIDOS]

Vocales: D./Dña. [NOMBRE Y APELLIDOS]

Vocales: D./Dña. [NOMBRE Y APELLIDOS]

Secretario/a no consejero/a:D./Dña.. [NOMBRE Y APELLIDOS]

5º Registro

Solicitar al registrador mercantil que, en base al artículo 63 del Reglamento del Registro Mercantil y en caso de apreciar algún defecto, proceda a la inscripción parcial si ello es posible.

6º Autorización

Autorizar, en cuanto fuere menester, a D./Dña. [NOMBRE Y APELLIDOS], en la forma más amplia en derecho, para la ejecución y desarrollo de todos y cada uno de los acuerdos adoptados por el consejo, con las más amplias facultades legales, así como para la subsanación, en su caso, de las omisiones o errores de los referidos acuerdos y su interpretación, y para realizar cuantos actos sean necesarios y otorgar cuantos documentos públicos y/o privados fueran precisos para su plena efectividad hasta lograr la inscripción en el Registro Mercantil.

Se hace constar, a los efectos del artículo 100.3 del Reglamento del Registro Mercantil, que la carta–circular en que constan los acuerdos ha sido remitida por cada uno de los administradores dentro del plazo de diez días contados desde la fecha de recepción de la solicitud de emisión del voto, solicitud que consta en la misma carta-circular.

Y para que así conste, la presente certificación es expedida por el secretario con el visto bueno de la presidenta, sirviendo a todos los efectos como Acta del Consejo de Administración

En [LOCALIDAD], el día [DÍA] de [MES] de [AÑO].

D./Dña. [NOMBRE Y APELLIDOS]

Secretario

D./Dña. [NOMBRE Y APELLIDOS]

Vº Bº Presidente

D./Dña. [NOMBRE Y APELLIDOS]

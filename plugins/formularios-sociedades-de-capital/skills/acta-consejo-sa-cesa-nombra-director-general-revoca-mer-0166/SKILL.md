---
name: acta-consejo-sa-cesa-nombra-director-general-revoca-mer-0166
description: "Acta del consejo de SA que cesa y nombra director general y revoca y otorga poderes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta del consejo de SA que cesa y nombra director general y revoca y otorga poderes

> Formulario **MER-0166** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

El Acta del Consejo de Administración debe reflejar la fecha, hora y lugar de la reunión, los nombres de los asistentes, el orden del día y el seguimiento de la misma. Además, debe incluir la información específica sobre el cese del director general anterior, la aceptación del cargo por el nuevo director general y la descripción detallada de los poderes que se le otorgan o revocan.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta del consejo de SA que cesa y nombra director general y revoca y otorga poderes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta del consejo de SA que cesa y nombra director general y revoca y otorga poderes” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-consejo-sa-cesa-nombra-director-general-revoca-mer-0166`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (17 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] AÑO (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] ESTADO CIVIL
- [ ] NÚMERO

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

El Acta del Consejo de Administración debe reflejar la fecha, hora y lugar de la reunión, los nombres de los asistentes, el orden del día y el seguimiento de la misma. Además, debe incluir la información específica sobre el cese del director general anterior, la aceptación del cargo por el nuevo director general y la descripción detallada de los poderes que se le otorgan o revocan.


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

ACTA DE LA REUNIÓN DEL CONSEJO DE ADMINISTRACIÓN DE LA SOCIEDAD «[DENOMINACIÓN SOCIAL], S.A.»

En [LOCALIDAD], y en el domicilio social de la compañía, sito en [LOCALIDAD], el [DÍA] de [MES] de [AÑO], se celebra reunión del consejo de administración de la sociedad «[DENOMINACIÓN SOCIAL], S.A.», previamente convocado en la forma y plazos legal y estatutariamente previstos.

Asisten personalmente a la reunión todos los miembros del consejo de administración, que a continuación se detallan:

Presidente/a: D./Dña. [NOMBRE Y APELLIDOS]

Vocal: D./Dña. [NOMBRE Y APELLIDOS]

Vocal: D./Dña. [NOMBRE Y APELLIDOS]

Secretario/a no Consejero/a: D./Dña.. [NOMBRE Y APELLIDOS]

Asisten asimismo a la reunión en calidad de invitados D./Dña. [NOMBRE Y APELLIDOS] y D./Dña.. [NOMBRE Y APELLIDOS]

A la finalización de la presente Acta aparecen estampadas las firmas de todos los asistentes.

ORDEN DEL DÍA

Los reunidos acuerdan por unanimidad celebrar reunión del consejo de administración con el siguiente

1. Cese de gerente de la sociedad.

2. Revocación de poderes.

3. Nombramiento de nuevo gerente de la sociedad.

4. Otorgamiento de poderes.

5. Protocolización.

Dicho orden del día aparece aprobado y firmado por todos los asistentes.

Actúan como presidente y secretario de la reunión D./Dña. [NOMBRE Y APELLIDOS]. y D./Dña.. [NOMBRE Y APELLIDOS], respectivamente.

ACUERDOS

1. CESE DE GERENTE DE LA SOCIEDAD.

Se acuerda por unanimidad cesar como gerente de la sociedad con efectos inmediatos a D./Dña. [NOMBRE Y APELLIDOS]

2. REVOCACIÓN DE PODERES.

Se acuerda por unanimidad revocar todas y cada una de las facultades que fueron otorgadas en favor de D./Dña.. [NOMBRE Y APELLIDOS] en virtud de las siguientes escrituras públicas:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Escritura pública otorgada ante el notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS]. el día [DÍA] de [MES] de [AÑO], con el número [NÚMERO] de orden de su protocolo.

3. NOMBRAMIENTO DE NUEVO GERENTE DE LA SOCIEDAD.

Se acuerda por unanimidad nombrar como nuevo gerente de la sociedad a:

• D./Dña. [NOMBRE Y APELLIDOS], de nacionalidad [NACIONALIDAD], estado civil, mayor de edad, con domicilio profesional en [LOCALIDAD], y DNI n.º [DNI/NIE], vigente.

4. OTORGAMIENTO DE PODERES.

Se acuerda por unanimidad otorgar poder a favor de D./Dña.. [NOMBRE Y APELLIDOS], de nacionalidad [NACIONALIDAD], estado civil [ESTADO CIVIL], mayor de edad, con domicilio profesional en [LOCALIDAD] y DNI [DNI/NIE], vigente, para que ejercite, solidariamente, en nombre y representación de la Sociedad «[DENOMINACIÓN SOCIAL], S.A.», las siguientes facultades:

5. PROTOCOLIZACIÓN.

Se acuerda asimismo facultar a [NOMBRE Y APELLIDOS] para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando a tales efectos las escrituras públicas correspondientes, incluidas las facultades de subsanación, rectificación o aclaración, así como para realizar cuantas actuaciones sean precisas o convenientes para la eficacia de los susodichos acuerdos.

Tras todo lo cual, redactada y leída que fue el acta por el Secretario, esta es aprobada por la Junta, por unanimidad de los asistentes.

No existiendo más asuntos que tratar, se levanta la sesión.

D./Dña. [NOMBRE Y APELLIDOS]

Secretario

D./Dña. [NOMBRE Y APELLIDOS]

Vº Bº Presidente

D./Dña. [NOMBRE Y APELLIDOS]

Asistentes

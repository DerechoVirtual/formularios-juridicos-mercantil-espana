---
name: certificacion-acuerdo-consejo-sa-cambiar-domicilio-mer-0151
description: "Certificación del acuerdo del consejo de SA de cambiar el domicilio dentro del mismo municipio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación del acuerdo del consejo de SA de cambiar el domicilio dentro del mismo municipio

> Formulario **MER-0151** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

El órgano de administración es competente para cambiar el domicilio social dentro del territorio nacional, salvo disposición contraria de los estatutos. Se considerará que hay disposición contraria de los estatutos solo cuando los mismos establezcan expresamente que el órgano de administración no ostenta esta competencia.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación del acuerdo del consejo de SA de cambiar el domicilio dentro del mismo municipio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación del acuerdo del consejo de SA de cambiar el domicilio dentro del mismo municipio” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdo-consejo-sa-cambiar-domicilio-mer-0151`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] MES (4 veces)
- [ ] AÑO (3 veces)
- [ ] CALLE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] DÍA (3 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CARGO
- [ ] FECHA
- [ ] FOLIO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NIF
- [ ] SECCIÓN
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

El órgano de administración es competente para cambiar el domicilio social dentro del territorio nacional, salvo disposición contraria de los estatutos. Se considerará que hay disposición contraria de los estatutos solo cuando los mismos establezcan expresamente que el órgano de administración no ostenta esta competencia.


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

D./Dña.. [NOMBRE Y APELLIDOS], [CARGO] de la entidad mercantil «[DENOMINACIÓN SOCIAL], S.A.» con Número de Identificación Fiscal [NIF] e inscrita en el Registro Mercantil de [LOCALIDAD], al Folio [FOLIO] del Tomo [TOMO] General de Sociedades número [NÚMERO], sección [SECCIÓN], hoja número e inscripción 1.ª

CERTIFICA

ACTA DEL CONSEJO DE ADMINISTRACIÓN DE LA ENTIDAD «[DENOMINACIÓN SOCIAL], S.A.» CELEBRADA EL DÍA [FECHA] DE [MES] DE [AÑO]

En el domicilio social, siendo las [Nº] horas del día [DÍA] de [MES] de [AÑO], se reúne el consejo de administración de la compañía, con la asistencia de todos los miembros del mismo:

CARGO	NOMBRE
Presidente
Vicepresidente
Secretario
Vicesecretario

Orden del día

El consejo de administración de la compañía se reúne para tratar del siguiente orden del día:

1.º Cambio del domicilio social de la compañía.

2.º Ruegos y preguntas.

3.º Elevación a público de los acuerdos adoptados.

4.º Aprobación del acta.

Y ya, sin más preámbulo, se entra en la deliberación, discusión y, en su caso, aprobación del citado orden del día.

ACUERDOS

Tras la exposición por el secretario de los temas propuestos a debate, con diversas intervenciones y comentarios, se adoptan por unanimidad, entre otros, los siguientes Acuerdos:

1. Cambio del domicilio social.— Se acuerda por unanimidad el cambio de domicilio social de la Compañía de la calle [CALLE], número, a la calle [CALLE], número, con la correspondiente modificación en los estatutos sociales:

«Artículo —La sociedad tendrá su domicilio social en el número [NÚMERO] de la calle [CALLE] de »

2. Ruegos y preguntas.— Nadie hace uso de la palabra.

3. Elevación a público de acuerdos adoptados.— La junta acuerda por unanimidad delegar solidaria e indistintamente, en cualesquiera de los miembros del órgano de administración, la elevación a público, en su caso, de los acuerdos adoptados, pudiendo realizar cuantas aclaraciones o subsanaciones sean necesarias o convenientes con el fin de obtener la inscripción de los mismos en el Registro Mercantil, solicitando la anotación preventiva o la inscripción parcial del título.

4. Aprobación del acta.— El consejo de administración acuerda por unanimidad, previa redacción y lectura del acta, la aprobación de la misma, siendo las [Nº] horas del [DÍA] de [MES] de

Y yo, D./Dña. [NOMBRE Y APELLIDOS], secretario del consejo de administración de la entidad mercantil «[DENOMINACIÓN SOCIAL], S.A.» expido la presente certificación con el V.º B.º del Sr. presidente del consejo de administración D./Dña. [NOMBRE Y APELLIDOS] en [LUGAR], a [DÍA] de [MES] de [AÑO]., a los efectos de su inscripción en el Registro Mercantil del domicilio social de la entidad.

D./Dña. [NOMBRE Y APELLIDOS]

administrador único
administrador solidario
administradores mancomunados
Secretario del Consejo de Administración

Secretario

Vº Bº Presidente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

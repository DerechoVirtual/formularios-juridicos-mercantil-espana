---
name: acuerdo-consejo-administracion-aprueba-proyecto-mer-0326
description: "Acuerdo del consejo de administración que aprueba el proyecto de escisión. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acuerdo del consejo de administración que aprueba el proyecto de escisión

> Formulario **MER-0326** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acuerdo del consejo de administración que aprueba el proyecto de escisión» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acuerdo del consejo de administración que aprueba el proyecto de escisión” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:acuerdo-consejo-administracion-aprueba-proyecto-mer-0326`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] HORA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] DIRECCIÓN
- [ ] NOMBRE O DENOMINACIÓN
- [ ] NÚMERO
- [ ] ÓRGANO O PERSONA

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

En este formulario se reproduce el contenido del acuerdo del consejo de administración por el que se aprueba el proyecto de escisión (y se adoptan otros acuerdos complementarios), teniendo en cuenta que deberá incluirse en el acta del consejo de administración o, en su caso, en la certificación que se expida para dejar constancia del mismo.

En el domicilio social de [DENOMINACIÓN SOCIAL] sito en [LOCALIDAD], calle, número, piso, y siendo las [HORA] del [FECHA] se reúne el Consejo de Administración de la entidad, que fue convocado de acuerdo a las previsiones estatutarias de la siguiente forma:

[ELEGIR UNA OPCIÓN: Convocatoria expedida a cada Consejero / Convocatoria entregada en mano a cada Consejero]

Se transcribe a continuación el texto íntegro de la convocatoria

"Sociedad."

Se convoca por el presidente D./Dña. [NOMBRE Y APELLIDOS], Consejo de Administración de la sociedad [DENOMINACIÓN SOCIAL] a celebrar en [DIRECCIÓN], el [FECHA], a las [HORA].

Asisten a la reunión los siguientes Consejeros:

Personalmente:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Personalmente y como representante de D./Dña. [NOMBRE Y APELLIDOS]

Todas las representaciones citadas se acreditan en forma legal, a satisfacción del Consejo.

Ejerce la función de Secretario del Consejo D./Dña. [NOMBRE Y APELLIDOS]

Por el Presidente se declara la válida constitución del Consejo, sin que ningún asistente presente protesta o reserva alguna.

Ningún asistente solicita constancia en el acta de su intervención u oposición y previa presentación de las propuestas referentes al proyecto de escisión de [DENOMINACIÓN SOCIAL] el Consejo adopta los siguientes:

ACUERDOS

Punto número [NÚMERO] del orden del día aprobación del proyecto de escisión y del informe sobre la escisión

El consejo ha decidido:

Primero. Aprobar el proyecto de escisión. de la sociedad « a favor de las sociedades «[NOMBRE O DENOMINACIÓN]» y « que supondrá la extinción de la sociedad que se escinde y conllevará el traspaso por sucesión universal de las partes del patrimonio escindidas a las sociedades beneficiarias.

El proyecto de escisión será insertado en la página web de la sociedad publicándose en el Boletín Oficial del Registro Mercantil el hecho mismo de la inserción y la fecha en que se produjo.

[ELEGIR UNA OPCIÓN: Balance ad hoc / Último balance del ejercicio]

Segundo. Aprobar el informe del órgano de administración sobre la escisión en el que, se describe y justifica detalladamente el proyecto de escisión en sus aspectos jurídicos y económicos, con especial referencia al tipo de canje y a las especiales dificultades de valoración, así como se exponen las implicaciones de la escisión para los socios, los acreedores y los trabajadores. Además, según el artículo 67 de aquella norma, el informe indica que han sido emitidos los informes sobre las aportaciones no dinerarias, así como el Registro Mercantil donde se depositarán estos informes.

A los efectos oportunos, se deja constancia de que la sociedad encargó y recibió un informe, de fecha [FECHA], elaborado por [ÓRGANO O PERSONA] experto independiente nombrado por resolución del Registrador Mercantil de [LOCALIDAD], de fecha [FECHA], del que resulta la exactitud del valor asignado a los bienes en el proyecto de escisión, la corrección del tipo de cambio propuesto y de los métodos seguidos para establecerlo, y que el valor del patrimonio que se transmite a las sociedades beneficiarias no es inferior a su aumento de capital.

No habiendo más asuntos que tratar y previa su redacción por el Secretario, el propio Consejo aprueba la presente Acta, firmándola a continuación el Secretario con el Visto Bueno del Presidente, así como, en prueba de conformidad, por los asistentes que desean hacerlo.

Tras lo cual, se levanta la sesión.

El Secretario D./Dña. [NOMBRE Y APELLIDOS]

VºB Del Presidente D./Dña. [NOMBRE Y APELLIDOS]

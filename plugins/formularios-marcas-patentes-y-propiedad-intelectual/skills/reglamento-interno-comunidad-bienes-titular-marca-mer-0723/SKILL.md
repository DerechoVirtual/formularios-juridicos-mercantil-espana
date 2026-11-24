---
name: reglamento-interno-comunidad-bienes-titular-marca-mer-0723
description: "Reglamento interno de la comunidad de bienes titular de una marca. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Reglamento interno de la comunidad de bienes titular de una marca

> Formulario **MER-0723** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Reglamento interno de la comunidad de bienes titular de una marca» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Reglamento interno de la comunidad de bienes titular de una marca” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:reglamento-interno-comunidad-bienes-titular-marca-mer-0723`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FRACCIÓN DE LA CUOTA (6 veces)
- [ ] PORCENTAJE (6 veces)
- [ ] CALLE
- [ ] DENOMINACIÓN DE LA COMUNIDAD
- [ ] DIRECCIÓN
- [ ] MARCA/MODELO
- [ ] NÚMERO
- [ ] PISO
- [ ] PLAZO

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

REGLAMENTO DE USO

Art. 1º.- Denominación

La comunidad de bienes se denomina " [DENOMINACIÓN DE LA COMUNIDAD], C.B."

Art. 2º.- Finalidad

La finalidad de esta comunidad será la realización de actividades principales, auxiliares y complementarias relacionadas con la titularidad de la marca [MARCA/MODELO]

Art. 3º.- Domicilio

El domicilio de la comunidad estará ubicado en [DIRECCIÓN], calle [CALLE] nº [NÚMERO] piso [PISO]

Art. 4º.- Duración

La duración de la presente comunidad de bienes es de 10 años renovables tácitamente por plazos de igual duración, salvo denuncia [PLAZO] de antelación a la expiración de dicho plazo de 10 años.

Art. 5º.- Aportaciones

Las aportaciones de los partícipes a la comunidad son las siguientes:

• D [NOMBRE Y APELLIDOS] aporta [PORCENTAJE] % de la marca, que representa un [FRACCIÓN DE LA CUOTA] de la cuota de la marca.

• D [NOMBRE Y APELLIDOS] aporta [PORCENTAJE] % de la marca, que representa un [FRACCIÓN DE LA CUOTA] de la cuota de la marca.

• D [NOMBRE Y APELLIDOS] aporta [PORCENTAJE] % de la marca, que representa un [FRACCIÓN DE LA CUOTA] de la cuota de la marca.

Art. 6º.- Reparto de beneficios y cargas

El concurso de los partícipes, tanto en los beneficios como en las cargas que genere el objeto de la presente comunidad, será proporcional a sus respectivos intereses o cuotas, que son las siguientes:

• A D [NOMBRE Y APELLIDOS] corresponde un interés o cuota del [PORCENTAJE] % [FRACCIÓN DE LA CUOTA].

• A D [NOMBRE Y APELLIDOS] corresponde un interés o cuota del [PORCENTAJE] % [FRACCIÓN DE LA CUOTA].

• A D [NOMBRE Y APELLIDOS] corresponde un interés o cuota del [PORCENTAJE] % [FRACCIÓN DE LA CUOTA].

Art. 7º.- Uso de la marca

No es posible el uso independiente de la marca por los comuneros, pues tal utilización es incompatible con la función de indicación de origen que debe cumplir la marca. La utilización individual y exclusiva de uno de los cotitulares es un acto de disposición que requerirá el consentimiento expreso y escrito de los demás.

La oposición absoluta e injustificada de un partícipe al uso de la marca de forma que pueda dar lugar a su declaración de caducidad, se considerará a todos los efectos como renuncia a su derecho.

Art. 8º.- Administración de la comunidad

Los acuerdos sobre administración requerirán unanimidad de los partícipes. No habrá mayoría sino cuando el acuerdo esté tomado por los partícipes que representen la mayor cantidad de los intereses que constituyan el objeto de la sociedad.

Si no resultare mayoría, o el acuerdo de ésta fuere gravemente perjudicial a los interesados en la cosa común, la Sección de lo Mercantil del Tribunal de Instancia proveerá, a instancia de parte, lo que corresponda, incluso, en su caso, nombrando un administrador.

A efectos de las relaciones con la Oficina Española de Patentes y Marcas, los comuneros designan como representante de la Comunidad a D. [NOMBRE Y APELLIDOS]

Art. 9º.- Derecho de tanteo y retracto

Cada comunero puede enajenar libremente su cuota. Los partícipes podrán ejercitar el derecho de tanteo en el plazo de un mes a contar desde el momento en que fueran notificados del propósito y condiciones en que se llevaría a cabo la cesión. A falta de aviso previo o si la cesión se hubiere realizado de forma distinta a lo prevenido en aquél, los partícipes podrán ejercitar el derecho de retracto, en igual plazo, desde la publicación de la inscripción de la cesión en el Registro de Marcas

Art. 10º.- Ejercicio de acciones

Cada partícipe podrá por sí solo ejercitar las acciones civiles y criminales en defensa de la marca, pero deberá notificarlo a los demás comuneros, a fin de que éstos puedan sumarse a las mismas y para que contribuyan al pago de los gastos habidos.

Art. 11º.- Extinción de la comunidad de marca

La comunidad se extinguirá por decisión de cualquiera de los comuneros, en cualquier tiempo.

Cuando los comuneros no convengan en que la marca adjudique a uno de ellos indemnizando a los demás, se venderá y repartirá su precio.

Art. 12º.- Elevación a documento público

Cualquiera de los copartícipes podrá instar que este documento se eleve a escritura pública, siendo de su cuenta los gastos que se ocasionen.

---
name: informe-especial-sobre-exclusion-derecho-suscripcion-mer-0161
description: "Informe especial sobre la exclusión del derecho de suscripción preferente en aumento de capital. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Informe especial sobre la exclusión del derecho de suscripción preferente en aumento de capital

> Formulario **MER-0161** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Informe especial sobre la exclusión del derecho de suscripción preferente en aumento de capital» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Informe especial sobre la exclusión del derecho de suscripción preferente en aumento de capital” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:informe-especial-sobre-exclusion-derecho-suscripcion-mer-0161`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] AÑO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MES
- [ ] NIF
- [ ] Nº

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

Para que sea válido el acuerdo de exclusión del derecho de preferencia es necesario que los administradores elaboren un informe en el que especifiquen el valor de las acciones de la sociedad y se justifiquen detalladamente la propuesta y la contraprestación a satisfacer por las nuevas [ELEGIR: acciones / participaciones], con la indicación de las personas a las que hayan de atribuirse, y, en las sociedades anónimas, que un experto independiente, distinto del auditor de las cuentas de la sociedad, nombrado a estos efectos por el Registro Mercantil, elabore otro informe, bajo su responsabilidad, sobre el valor razonable de las acciones de la sociedad, sobre el valor teórico del derecho de preferencia cuyo ejercicio se propone suprimir o limitar y sobre la razonabilidad de los datos contenidos en el informe de los administradores.

A la junta general de accionistas:

A los fines previstos en el artículo 308 del Texto Refundido de la Ley de Sociedades de Capital, y de acuerdo con el encargo recibido de la sociedad, emitimos el presente informe especial sobre el aumento de capital social en [IMPORTE] euros, mediante la emisión de [Nº] acciones ordinarias de [IMPORTE] euros de valor nominal cada una, con exclusión del derecho de suscripción preferente, acompañada del informe adjunto del consejo de administración que se someterá a la aprobación de la junta general extraordinaria de accionistas.

El informe elaborado por el consejo de administración propone que el tipo de emisión de las nuevas acciones para su suscripción por la sociedad «[DENOMINACIÓN SOCIAL]», SA domiciliada en [DOMICILIO], [LOCALIDAD] y con número de identificación fiscal [NIF], sea el %. De este modo se desembolsarán por cada acción [IMPORTE] euros, de las que [IMPORTE] euros corresponden al valor nominal de los títulos y [IMPORTE] euros corresponden a la prima de emisión.

Nuestro trabajo se ha basado en las cuentas del ejercicio cerrado el [DÍA] de [MES] de [AÑO], auditadas por nosotros sin salvedad alguna, y ha incluido los siguientes aspectos:

a) Formulación de preguntas a la dirección de la sociedad sobre acontecimientos importantes que pudieran haber afectado de forma significativa a la sociedad entre la fecha de cierre de las citadas cuentas anuales y la fecha del informe de auditoría.

b) Evaluación de la adecuación de los factores utilizados para la determinación del tipo de emisión propuesto para las acciones y un examen de la documentación que soporta el método de valoración utilizado por la sociedad y las bases de cálculo.

c) Obtención de un escrito de la dirección de la sociedad en el que se nos comunicó que han puesto en nuestro conocimiento todas las hipótesis, datos o informaciones relevantes a efectos de la operación a efectuar.

Teniendo en cuenta todo lo indicado anteriormente, a nuestro juicio profesional, los factores utilizados por el consejo de administración de «[DENOMINACIÓN SOCIAL], S.A.» en la determinación del tipo de emisión de [IMPORTE] euros para las nuevas acciones están adecuadamente expuestos en su informe adjunto y se basan en el método de valoración descrito anteriormente, que consideramos adecuado a las circunstancias presentes, y justifican el tipo de emisión propuesto a la aprobación de la junta general extraordinaria de accionistas.

Este informe especial ha sido preparado únicamente a los fines previstos en el artículo 308 del Texto Refundido de la Ley de Sociedades de Capita, por lo que no debe ser utilizado para ninguna otra finalidad.

«[DENOMINACIÓN SOCIAL], S.A.»

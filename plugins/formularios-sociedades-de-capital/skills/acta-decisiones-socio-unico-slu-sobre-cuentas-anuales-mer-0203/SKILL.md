---
name: acta-decisiones-socio-unico-slu-sobre-cuentas-anuales-mer-0203
description: "Acta de decisiones del socio único de una SLU sobre cuentas anuales, dividendo a cuenta y auditor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de decisiones del socio único de una SLU sobre cuentas anuales, dividendo a cuenta y auditor

> Formulario **MER-0203** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de acta de decisión del socio único de una Sociedad de responsabilidad limitada unipersonal relativo a la aprobación de las cuentas anuales y reparto de dividendos a cuenta

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de decisiones del socio único de una SLU sobre cuentas anuales, dividendo a cuenta y auditor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de decisiones del socio único de una SLU sobre cuentas anuales, dividendo a cuenta y auditor” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-decisiones-socio-unico-slu-sobre-cuentas-anuales-mer-0203`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº (3 veces)
- [ ] FECHA (2 veces)
- [ ] DESTINO DEL RESULTADO
- [ ] EJERCICIO
- [ ] FOLIO
- [ ] HOJA
- [ ] IMPORTE
- [ ] INSCRIPCIÓN
- [ ] LIBRO
- [ ] NIF
- [ ] Nº DE ARTÍCULO
- [ ] NÚMERO
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

Modelo de acta de decisión del socio único de una Sociedad de responsabilidad limitada unipersonal relativo a la aprobación de las cuentas anuales y reparto de dividendos a cuenta


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

ACTA DE DECISIÓN DEL SOCIO ÚNICO DE ‘[DENOMINACIÓN SOCIAL], S.L.’, SOCIEDAD UNIPERSONAL

En [LOCALIDAD], siendo las [Nº] horas del día [FECHA], D./Dña. [NOMBRE Y APELLIDOS], en su calidad de socio único de la mercantil ‘[DENOMINACIÓN SOCIAL], S.L.’ Sociedad Unipersonal, adopta las siguientes

DECISIONES:

Primera.- Examen y aprobación de las cuentas anuales correspondiente al ejercicio [EJERCICIO]

Se aprueban las mismas en los términos en que han sido redactadas por el órgano de administración.

Se hace constar que la sociedad puede formular balance abreviado y no está obligada a someter las cuentas a verificación de auditor.

Las cuentas anuales, firmadas por el órgano de administración, quedan unidas al Acta como Anexo [Nº].

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Segunda.- Aplicación de los resultados obtenidos.

Se decide destinar la cantidad de [IMPORTE] a [DESTINO DEL RESULTADO].

Segunda.- Distribución de cantidades a cuenta de dividendos

Se acuerda aprobar un dividendo a cuenta a pagar al socio único de .euros El dividendo a cuenta será abonado en metálico mediante la correspondiente transferencia bancaria realizada por "" a "

Se hace constar que los resultados obtenidos desde el fin del último ejercicio son superiores a la cantidad aprobada como dividendo a cuenta, No existen pérdidas procedentes de ejercicios anteriores a compensar, la reserva legal alcanza el 20% del capital social y los administradores han formulado un estado contable que pone de manifiesto la existencia de liquidez suficiente para la distribución del dividendo a cuenta. Por tanto, se entienden cumplidos los requisitos que para la distribución entre los socios de cantidades a cuenta de dividendos establece el artículo [Nº DE ARTÍCULO] de los estatutos sociales. El citado dividendo a cuenta a pagar al socio único será exigible con efectos el día [FECHA] de

Tercera.- Examen y aprobación de la gestión realizada por el órgano de administración.

Se deja constancia de la plena satisfacción por la marcha de los negocios sociales y la forma en que los mismos se han llevado a cabo.

Cuarta.- Nombramiento del auditor de cuentas de la sociedad y del grupo consolidado

Se decide nombrar por un término de [Nº] años, como auditor de cuentas de la sociedad y del grupo consolidado, a la compañía [DENOMINACIÓN SOCIAL] con domicilio social en [LOCALIDAD], NIF n.º [NIF] e inscrita en el Registro Mercantil de [LOCALIDAD], al Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Sección [SECCIÓN], Hoja [HOJA], Inscripción [INSCRIPCIÓN], en el REA y en el Registro Oficial de Auditores de Cuentas (ROAC) con el n.º [NÚMERO], todo ello en cumplimiento de lo dispuesto en el artículo 264 del Texto Refundido de la Ley de Sociedades de Capital.

El nombramiento efectuado se presentará para su inscripción en el Registro Mercantil de [LOCALIDAD] junto con la carta de aceptación de los Auditores designados.

Quinta.- Elevación a público

Se acuerda facultar a [NOMBRE Y APELLIDOS], así como a aquellas personas con poderes de protocolización debidamente inscritos para que uno cualquiera de ellos pueda elevar a público las anteriores, compareciendo ante Notario y procediendo, en su caso, a la subsanación, rectificación o aclaración del mismo y/o de la escritura o acta a que todo ello dé lugar.

Y no habiendo más decisiones que consignar, se levanta la presente acta, en cumplimiento de lo previsto en el artículo 15 del Texto Refundido de la Ley de Sociedades de Capital, y en el artículo 97.2 del Reglamento del Registro Mercantil, siendo dicha acta leída y firmada en prueba de conformidad en el lugar y en la fecha citados en el encabezamiento.

SOCIO ÙNICO

D./Dña. [NOMBRE Y APELLIDOS]

---
name: resguardo-deposito-matriz-mer-0572
description: "Resguardo de depósito con su matriz. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Resguardo de depósito con su matriz

> Formulario **MER-0572** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Resguardo de depósito con su matriz» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Resguardo de depósito con su matriz” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:resguardo-deposito-matriz-mer-0572`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (9 veces)
- [ ] MES (9 veces)
- [ ] AÑO (8 veces)
- [ ] IMPORTE (7 veces)
- [ ] DÍA (6 veces)
- [ ] FECHA (5 veces)
- [ ] Nº (5 veces)
- [ ] LUGAR (4 veces)
- [ ] NOMBRE DE LA PARTE (4 veces)
- [ ] ACTO O RESOLUCIÓN (3 veces)
- [ ] ASEGURADORA (3 veces)
- [ ] DESCRIPCIÓN DE LA MERCANCÍA (3 veces)
- [ ] ÓRGANO (3 veces)
- [ ] DATOS DE TRANSCRIPCIÓN DEL RESGUARDO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] MOTIVO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALIDAD DEL DEPOSITANTE
- [ ] LUGAR DE PAGO

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

Matriz

Depósito núm. [Nº] en [LUGAR], a [DÍA] de [MES] dos mil [AÑO]

Silo núm. Almacén [Nº].

Mercancías depositadas [DESCRIPCIÓN DE LA MERCANCÍA], cuyo valor aproximado asciende a [IMPORTE] €/euros, y que han sido aseguradas por esta entidad contra [ACTO O RESOLUCIÓN], hasta la cifra máxima de /euros por kg, en la compañía aseguradora [ASEGURADORA], conforme a las estipulaciones que obran en la póliza núm

Datos del depositante [ÓRGANO], que deposita las mercancías en calidad de [CALIDAD DEL DEPOSITANTE]

Lugar y fecha del contrato de depósito: fue firmado en [LUGAR], a [DÍA] de [MES] dos mil [AÑO] Fecha de finalización del depósito: de [FECHA] dos mil

Datos de transcripción del resguardo de garantía [DATOS DE TRANSCRIPCIÓN DEL RESGUARDO].

Resguardo de Depósito (anverso)

Depósito núm [NÚMERO] en [LUGAR], a [DÍA] de [MES] dos mil [AÑO]

Contra entrega de este RESGUARDO DE DEPÓSITO la sociedad [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD], COMO ENTIDAD DEPOSITARIA, restituirá a [NOMBRE DE LA PARTE], con domicilio en [LOCALIDAD], COMO PARTE DEPOSITANTE, las MERCANCÍAS siguientes: [DESCRIPCIÓN DE LA MERCANCÍA], cuyo valor aproximado asciende a [IMPORTE] €/euros, y que han sido aseguradas por esta entidad contra [ACTO O RESOLUCIÓN], hasta la cifra máxima de [IMPORTE] €/euros por kg, en la compañía aseguradora [ASEGURADORA], conforme a las estipulaciones que obran en la póliza núm. [Nº], y que han sido depositadas en el silo núm. [Nº], del almacén sito en [LOCALIDAD], de la ENTIDAD DEPOSITARIA, en virtud del contrato suscrito por las partes contratantes el día [FECHA] de [MES] de dos mil [AÑO], en [LOCALIDAD] y hasta el día [FECHA] de [MES] de dos mil [AÑO], con unos gastos de almacenaje cifrados en [IMPORTE] €/euros.

LA PARTE DEPOSITANTE	LA ENTIDAD DEPOSITARIA

Cláusulas:

Resguardo de Depósito (reverso)

Restitúyanse las mercancías objeto de este depósito a., con domicilio en [LOCALIDAD], en razón de [MOTIVO].

En [LOCALIDAD], a [DÍA] de [MES] dos mil [AÑO]

Firma del endosante

Nombre y domicilio del endosante [ÓRGANO].

Datos de transcripción del resguardo de garantía [DATOS DE TRANSCRIPCIÓN DEL RESGUARDO].

Resguardo de Garantía (anverso)

Depósito núm. [Nº] en [LUGAR], a [DÍA] de [MES] dos mil [AÑO]

Vencimiento [FECHA].

En virtud del presente RESGUARDO DE GARANTÍA, se garantiza el cumplimiento del PRÉSTAMO de la cantidad de [IMPORTE] recibido por [NOMBRE DE LA PARTE], como PARTE PRESTATARIA, de [NOMBRE DE LA PARTE], como PARTE PRESTAMISTA, pagadero en [LUGAR DE PAGO], y que vence el día [FECHA] de [MES] de

Al pago de dicha garantía quedan afectas las MERCANCÍAS siguientes: [DESCRIPCIÓN DE LA MERCANCÍA], cuyo valor aproximado asciende a [IMPORTE] €/euros, y que han sido depositadas en el silo núm [NÚMERO], del almacén sito en [LOCALIDAD], de la sociedad [DENOMINACIÓN SOCIAL], en virtud del contrato reproducido en el Resguardo de Depósito concordante con el presente documento y en el que se halla transcrita la presente pignoración, y que han sido aseguradas por la entidad depositaria contra [ACTO O RESOLUCIÓN], hasta la cifra máxima de [IMPORTE] €/euros por kg, en la compañía aseguradora [ASEGURADORA], conforme a las estipulaciones que obran en la póliza núm

LA PARTE PRESTAMISTA	LA ENTIDAD PRESTATARIA

Cláusulas:

Resguardo de Garantía (reverso)

Satisfágase esta garantía a [NOMBRE DE LA PARTE], con domicilio en [LOCALIDAD], en razón de [MOTIVO].

En [LOCALIDAD], a [DÍA] de [MES] dos mil [AÑO]

Firma del endosante.

Nombre y domicilio del endosante [ÓRGANO].

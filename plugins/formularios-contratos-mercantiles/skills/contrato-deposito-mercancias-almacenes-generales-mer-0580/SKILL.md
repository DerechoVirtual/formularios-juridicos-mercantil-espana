---
name: contrato-deposito-mercancias-almacenes-generales-mer-0580
description: "Contrato de depósito de mercancías en almacenes generales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de depósito de mercancías en almacenes generales

> Formulario **MER-0580** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de depósito de mercancías en almacenes generales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de depósito de mercancías en almacenes generales” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-deposito-mercancias-almacenes-generales-mer-0580`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] FECHA (2 veces)
- [ ] MES (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] ASEGURADORA
- [ ] CALIDAD DEL DEPOSITANTE
- [ ] DESCRIPCIÓN DE LAS MERCANCÍAS
- [ ] DÍA
- [ ] Nº DE SILOS
- [ ] NÚMERO

## Normas que cita el formulario

- art. 1780 Código Civil

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

CONTRATO DE DEPÓSITO EN ALMACENES GENERALES

En [LOCALIDAD] a [DÍA] de [MES] dos mil

ESTIPULACIONES

Que la parte depositante, en calidad de [CALIDAD DEL DEPOSITANTE] de las mercancías siguientes [DESCRIPCIÓN DE LAS MERCANCÍAS], cuyo valor aproximado asciende a [IMPORTE] €/euros, procede al depósito de las mismas en los silos núms [Nº DE SILOS], de los almacenes de la entidad depositaria sitos en [LOCALIDAD], con fecha [FECHA] de de dos mil

Que la entidad depositaria se compromete a mantener almacenadas las referidas mercancías hasta la fecha [FECHA] de [MES] dos mil, y declara tener conocimiento de sus obligaciones respecto a la conservación, guarda y custodia de tales mercancías.

La entidad depositaria se compromete a asegurar las repetidas mercancías contra [ACTO O RESOLUCIÓN], hasta la cifra máxima de [IMPORTE] €/euros por kg, en la compañía aseguradora [ASEGURADORA], conforme a las estipulaciones que obran en la póliza núm [NÚMERO], cuya copia obra adjunta al presente contrato.

La entidad depositaria no podrá llevar a cabo cambio, traslado ni con mixtión alguna, ni en general ningún acto de disposición sobre las mercancías que le son entregadas por la parte depositante, sin autorización expresa y fehaciente de la parte depositante.

La entidad depositaria sólo podrá proceder a emitir los correspondientes resguardos de depósito y de garantía sobre las mercancías depositadas a expreso requerimiento para ello de la parte depositante, siempre en un momento anterior a la fecha de finalización del depósito objeto del presente contrato, que obra en la estipulación segunda del mismo.

La parte depositante se compromete a satisfacer a la entidad depositaria la cantidad de [IMPORTE] €/euros, en concepto de gastos de almacenaje y justa contraprestación sus servicios de depósito y custodia de las mercancías depositadas. En caso de mora o incumplimiento de esta obligación, la entidad depositaria tendrá derecho a retener en prenda tales mercancías hasta la completa satisfacción de tal obligación, según lo dispuesto en el artículo 1780 del Código Civil.

La parte depositante se compromete a avisar de forma fehaciente y con antelación suficiente a la entidad depositaria de cualquier cuestión que pueda sobrevenir respecto a la propiedad, posesión o pignoración de las mercancías depositadas, y en general de todo lo que pueda afectar a la titularidad y disposición sobre las mismas.

Las partes intervinientes acuerdan libre y voluntariamente someter todo litigio, discrepancia o cuestión relacionadas con la aplicación, ejecución o interpretación del presente contrato a la (jurisdicción de los tribunales de la localidad de que se trate, renunciando a su propio fuero/ a su resolución mediante laudo, en equidad, o en Derecho, dictado por el Tribunal/la Corte de Arbitraje de la Cámara de Comercio e Industria de [LOCALIDAD], y hacen constar asimismo su compromiso expreso de cumplir el laudo arbitral que se dicte).

Y en prueba de conformidad, las partes intervinientes otorgan y firman el presente contrato por duplicado y a un solo efecto en el lugar y fecha que obran en el encabezamiento.

LA PARTE DEPOSITANTE Fdo.:

LA ENTIDAD DEPOSITARIA Fdo.:

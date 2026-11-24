---
name: contrato-deposito-bancario-plazo-fijo-mer-0645
description: "Contrato de depósito bancario a plazo fijo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de depósito bancario a plazo fijo

> Formulario **MER-0645** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de depósito bancario a plazo fijo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de depósito bancario a plazo fijo” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-deposito-bancario-plazo-fijo-mer-0645`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- El modelo no tiene campos marcados: Claude te preguntará lo que necesite según el caso.

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

CONTRATO DE DEPÓSITO BANCARIO A PLAZO

Condiciones generales del depósito a plazo

Son aplicables a este contrato las condiciones generales del contrato de apertura de cuenta

1. Eficacia de las condiciones generales.

Las presentes condiciones generales a modo de contrato marco, regirán todas las imposiciones que los titulares realicen en la cuenta, que se regirán, además, por las que consten en cada uno de los documentos que los titulares y la entidad deberán suscribir en la contratación de las sucesivas imposiciones que se formalicen al amparo de estas condiciones generales, así como por las condiciones del contrato de cuenta corriente, siempre que no se opongan o contradigan lo que aquí se dispone o lo dispuesto en los contratos adicionales.

En todas las ocasiones en que los titulares quieran realizar una nueva imposición, deberán suscribir un contrato adicional en el que se exprese el importe, el plazo y el periodo de liquidación, el tipo de interés y las demás condiciones que vayan a regir esa imposición de forma concreta.

Los titulares del contrato marco necesariamente deberán corresponderse con los titulares de cada uno de los contratos adicionales que queden suscritos al amparo de aquel contrato marco.

2. Duración del contrato.

Los titulares no podrán retirar las imposiciones que se realicen en este tipo de cuentas hasta que no transcurra el plazo formal establecido, que será aquél que figure en el contrato adicional para cada una de las imposiciones en concreto.

La entidad procederá a la prórroga por igual periodo y en las mismas condiciones si antes del vencimiento de cada imposición o de cualquiera de la prórrogas establecidas, no se hubiera recibido notificación alguna por parte de los titulares para retirar su importe. Esta regla también será aplicable a cada vencimiento habido con posterioridad y a las prórrogas sucesivas. En caso de prórroga, los intereses vencidos de la imposición quedarán abonados en la cuenta asociada.

Si por parte de la entidad se procede a la modificación del tipo de interés y de las prórrogas, así como de la periodicidad con que han de producirse las liquidaciones, procederá a su comunicación a los titulares en modo personalizado, indicando el tipo de interés nominal, el TAE a que está dispuesto a prorrogarla por igual plazo y la periodicidad con que se efectuarán las liquidaciones, con la suficiente antelación a su aplicación. La falta de comunicación en contra a la entidad por parte de los titulares antes del vencimiento de la imposición, se entiende como la aceptación de la prórroga con las nuevas condiciones. Si hay rechazo de las nuevas condiciones por parte de los titulares antes del vencimiento, cuando el mismo se produzca, podrán libremente proceder a la retirada del importe de la imposición.

3. Intereses.

Para liquidar los intereses correspondientes a esta operación, se procederá a utilizar la fórmula interés simple (i: c.r.t: 36.000, siendo i= intereses devengados; c = los saldos mantenidos, r = tipo de interés nominal y t = los días de permanencia), si se considera que cada mes del año tiene 30 días, con excepción de aquellos depósitos contratados por un plazo inferior a un mes en cuyo caso se tendrán en cuenta los días naturales realmente transcurridos y se utilizará como divisor 36.500.

El/LOS TITULAR/ES La ENTIDAD P.P.

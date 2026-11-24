---
name: carta-garantia-bancaria-primer-requerimiento-modelo-mer-0656
description: "Carta de garantía bancaria a primer requerimiento (modelo). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Carta de garantía bancaria a primer requerimiento (modelo)

> Formulario **MER-0656** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Carta de garantía bancaria autónoma, irrevocable y exigible a primer requerimiento, emitida por un banco, a solicitud de un ordenante, a favor de un beneficiario (p. ej. proveedor) para garantizar el pago del precio de unos suministros, con importe máximo, vigencia, renuncia a los beneficios de excusión, orden y división, sometimiento a las Reglas Uniformes de la CCI y fuero.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Carta de garantía bancaria a primer requerimiento (modelo)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Carta de garantía bancaria a primer requerimiento (modelo)” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:carta-garantia-bancaria-primer-requerimiento-modelo-mer-0656`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (18 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] FECHA (5 veces)
- [ ] DOMICILIO (4 veces)
- [ ] NOMBRE DEL NOTARIO (3 veces)
- [ ] PROVINCIA (3 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE (2 veces)
- [ ] AÑO
- [ ] CIUDAD
- [ ] DENOMINACIÓN SOCIAL DEL BANCO
- [ ] DENOMINACIÓN SOCIAL DEL BENEFICIARIO
- [ ] DENOMINACIÓN SOCIAL DEL ORDENANTE
- [ ] DESCRIPCIÓN DE LOS SUMINISTROS
- [ ] DNI/NIF
- [ ] DOCUMENTO ACREDITATIVO
- [ ] DÍA
- [ ] FIRMA
- [ ] IMPORTE
- [ ] MES
- [ ] Nº DE DOCUMENTO
- [ ] PAÍS O LOCALIDAD

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

GARANTÍA BANCARIA A PRIMER REQUERIMIENTO

PARTES

El Banco [DENOMINACIÓN SOCIAL DEL BANCO], S.A., constituido en escritura pública de fecha [FECHA], otorgada ante el Notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], e inscrita en el Registro Mercantil de [PROVINCIA], tomo [Nº], folio [Nº], hoja [Nº], sección [Nº], inscripción [Nº], con domicilio social en [LOCALIDAD], calle [DOMICILIO], núm. [Nº], con NIF núm. [NIF], representada por [NOMBRE Y APELLIDOS DEL REPRESENTANTE], mayor de edad, [ESTADO CIVIL], con domicilio en [LOCALIDAD], calle [DOMICILIO], núm. [Nº], con DNI/NIF núm. [DNI/NIF], cuyas facultades representativas, que declara no han sido revocadas o limitadas, resultan de lo previsto en la escritura pública de fecha [FECHA], otorgada ante el Notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], e inscrita en el Registro Mercantil de [PROVINCIA], tomo [Nº], hoja [Nº], folio [Nº], inscripción [Nº], en adelante BANCO GARANTE,

por el presente documento y a solicitud de la sociedad mercantil [DENOMINACIÓN SOCIAL DEL ORDENANTE], constituida en [PAÍS O LOCALIDAD], representada por [NOMBRE Y APELLIDOS DEL REPRESENTANTE], mayor de edad, [ESTADO CIVIL], con domicilio en [LOCALIDAD], calle [DOMICILIO], núm. [Nº], con [ELEGIR: DNI/NIF / pasaporte] [Nº DE DOCUMENTO], cuyas facultades representativas, que declara no han sido revocadas o limitadas, resultan de lo previsto en el documento que se adjunta ([DOCUMENTO ACREDITATIVO]), en adelante ORDENANTE DE LA GARANTÍA,

presta a favor de la sociedad mercantil española [DENOMINACIÓN SOCIAL DEL BENEFICIARIO], S.A., constituida en escritura pública de fecha [FECHA], otorgada ante el Notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], e inscrita en el Registro Mercantil de [PROVINCIA], tomo [Nº], folio [Nº], hoja [Nº], sección [Nº], inscripción [Nº], con domicilio social en [LOCALIDAD], calle [DOMICILIO], núm. [Nº], con NIF núm. [NIF], en adelante BENEFICIARIO DE LA GARANTÍA,

una garantía bancaria autónoma e irrevocable, exigible al simple requerimiento del BENEFICIARIO, para garantizar el exacto y puntual cumplimiento de todas y cada una de las obligaciones que resulten para el ORDENANTE del pago del precio de los suministros de [DESCRIPCIÓN DE LOS SUMINISTROS], realizados por el BENEFICIARIO, en los términos siguientes:

IMPORTE DE LA GARANTÍA

La garantía se constituye por un importe total de [IMPORTE] euros.

OBLIGACIONES DEL GARANTE

1. El BANCO GARANTE se obliga a entregar inmediatamente al BENEFICIARIO DE LA GARANTÍA, y a su requerimiento escrito, todas las cuantías que el mismo le exigiera al amparo de esta garantía y hasta el límite fijado en el apartado precedente. La procedencia del requerimiento se deja al criterio del BENEFICIARIO DE LA GARANTÍA y es independiente de decisión judicial alguna.

RENUNCIA A LOS BENEFICIOS

2. El BANCO renuncia expresamente a los beneficios de excusión, orden y división y cualesquiera otros que le puedan corresponder en relación con el pago de cualquier cuantía que le sea exigida por el BENEFICIARIO, dentro de los límites de la garantía prestada.

DURACIÓN DE LA GARANTÍA

3. La presente garantía es válida desde el [FECHA] hasta el [FECHA], debiendo el BENEFICIARIO presentar al BANCO GARANTE sus requerimientos de pago en el referido período temporal. Para cancelar la garantía antes del término final arriba señalado, el ORDENANTE deberá comunicar fehacientemente al BANCO que han quedado canceladas todas las deudas derivadas de dichas operaciones. Transcurrido el período por el que se ha pactado la garantía, con independencia de que el BANCO hubiera abonado cantidad alguna en este concepto al BENEFICIARIO, se entiende que la garantía prestada ha caducado.

NORMATIVA APLICABLE

4. En todo lo no previsto en este documento, la garantía a primer requerimiento prestada por el BANCO GARANTE se regirá por las Reglas Uniformes de Garantías a Primer Requerimiento (Uniform Rules for Demand Guarantees, URDG) de la Cámara de Comercio Internacional de París, en su revisión vigente.

FUERO

5. En todo lo relativo a la interpretación y ejecución de esta garantía, el BANCO GARANTE, el ORDENANTE y el BENEFICIARIO, con renuncia a su fuero propio, se someten a los Jueces y Tribunales de [CIUDAD].

PROTECCIÓN DE DATOS

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento del Reglamento (UE) 2016/679 (RGPD), de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, y demás normativa aplicable.

Fecha y lugar: [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del representante de la entidad bancaria, legitimada notarialmente: [FIRMA]

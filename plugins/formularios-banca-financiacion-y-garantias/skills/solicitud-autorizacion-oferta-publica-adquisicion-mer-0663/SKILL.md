---
name: solicitud-autorizacion-oferta-publica-adquisicion-mer-0663
description: "Solicitud de autorización de una oferta pública de adquisición de valores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de autorización de una oferta pública de adquisición de valores

> Formulario **MER-0663** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Escrito dirigido a la Comisión Nacional del Mercado de Valores (CNMV) para solicitar la autorización de una oferta pública de adquisición de valores (OPA), voluntaria u obligatoria, conforme al Real Decreto 1066/2007, de 27 de julio, sobre el régimen de las ofertas públicas de adquisición de valores. Lo presenta el oferente, junto con el folleto explicativo y la documentación acreditativa.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de autorización de una oferta pública de adquisición de valores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de autorización de una oferta pública de adquisición de valores” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:solicitud-autorizacion-oferta-publica-adquisicion-mer-0663`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL DE LA SOCIEDAD AFECTADA
- [ ] DESCRIPCIÓN DE LA REPRESENTACIÓN QUE OSTENTA
- [ ] DÍA
- [ ] FIRMA
- [ ] LOCALIDAD
- [ ] MEDIO PREFERENTE O LUGAR DE NOTIFICACIONES
- [ ] MES
- [ ] NIF O EQUIVALENTE
- [ ] NOMBRE Y APELLIDOS
- [ ] PERSONA U ÓRGANO COMPETENTE
- [ ] VARIACIONES PRODUCIDAS, O INDICACIÓN DE QUE NO HAN EXISTIDO

## Normas que cita el formulario

- art. 17 Real Decreto 1066/2007

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: comprobar la vigencia del Real Decreto 1066/2007 y de la Circular de la CNMV que aprueba los modelos de solicitud, folleto y anuncio (a la que remite el original con las expresiones «Formulario I» y «Norma Primera»), y su adaptación a la Ley 6/2023, de los Mercados de Valores y de los Servicios de Inversión.

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

A LA COMISIÓN NACIONAL DEL MERCADO DE VALORES

SOLICITUD DE AUTORIZACIÓN DE OFERTA PÚBLICA DE ADQUISICIÓN DE VALORES

1. La presente solicitud de autorización se hace pública en virtud de lo previsto en el artículo 17 del Real Decreto 1066/2007, de 27 de julio, y se refiere a una oferta que está sujeta a la preceptiva autorización de la Comisión Nacional del Mercado de Valores.

Los términos y características detallados de la oferta estarán contenidos en el folleto explicativo que se publicará tras la obtención de la referida autorización.

2. IDENTIFICACIÓN DEL SOLICITANTE

[NOMBRE Y APELLIDOS Y DNI/NIE O EQUIVALENTE; EN CASO DE PERSONA JURÍDICA, DENOMINACIÓN SOCIAL, DOMICILIO SOCIAL Y NIF O EQUIVALENTE], así como identificación del medio preferente o del lugar que se señale a efectos de notificaciones: [MEDIO PREFERENTE O LUGAR DE NOTIFICACIONES].

EXPONE

[OPCIONAL — incluir solo en caso de oferta obligatoria] OFERTAS OBLIGATORIAS: Se declara que se ha producido el supuesto que, en virtud de lo previsto en la normativa vigente, obliga a la formulación de una oferta pública de adquisición de valores, a saber: [DESCRIPCIÓN DEL HECHO O CIRCUNSTANCIA QUE SUPONE LA OBLIGACIÓN DE FORMULAR LA OFERTA].

DECISIÓN DE FORMULAR UNA OFERTA PÚBLICA DE ADQUISICIÓN DE VALORES: Se declara la decisión de formular una oferta pública de adquisición de valores de [DENOMINACIÓN SOCIAL DE LA SOCIEDAD AFECTADA], en los términos y condiciones que se describen en el presente escrito de solicitud y en el folleto explicativo adjunto, decisión adoptada por [PERSONA U ÓRGANO COMPETENTE] con fecha [FECHA].

DECLARACIÓN SOBRE LA GARANTÍA DE LA OFERTA: La garantía de la oferta [ELEGIR: se presenta junto con la solicitud de autorización / será presentada en el plazo máximo previsto en el artículo 17 del Real Decreto 1066/2007, de 27 de julio].

CARACTERÍSTICAS DE LA OFERTA: [DESCRIPCIÓN DE LAS PRINCIPALES CARACTERÍSTICAS DE LA OFERTA, INCORPORANDO LAS INFORMACIONES SEÑALADAS EN EL FORMULARIO I DE LA CIRCULAR DE LA CNMV, EXCEPTO LAS PREVISTAS EN SUS APARTADOS 1 Y 2].

DATOS DEL ANUNCIO DE LA OFERTA: [OPCIONAL — si ha lugar] El anuncio de la oferta fue publicado con fecha [FECHA], y se confirman las informaciones y características de la oferta en él contenidas, con las siguientes variaciones: [VARIACIONES PRODUCIDAS, O INDICACIÓN DE QUE NO HAN EXISTIDO].

[OPCIONAL — incluir si el anuncio de la oferta y la solicitud de autorización se producen simultáneamente] Este escrito de solicitud tiene la consideración de anuncio de la oferta a todos los efectos.

SOLICITA

A la Comisión Nacional del Mercado de Valores que tenga por presentado el escrito, junto con el folleto explicativo de la oferta y demás documentación que se acompañe, por realizadas las manifestaciones contenidas en su cuerpo y se sirva admitirlos a trámite y autorizar la formulación de la oferta.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Firma del solicitante o persona apoderada: [FIRMA]

[OPCIONAL — si firma un apoderado] Identificación del apoderado: [NOMBRE Y APELLIDOS], [NIF O EQUIVALENTE], en su condición de [DESCRIPCIÓN DE LA REPRESENTACIÓN QUE OSTENTA], acompañando la documentación acreditativa de dicha representación.

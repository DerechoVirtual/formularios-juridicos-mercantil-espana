---
name: anuncio-previo-oferta-publica-adquisicion-valores-mer-0664
description: "Anuncio previo de una oferta pública de adquisición de valores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Anuncio previo de una oferta pública de adquisición de valores

> Formulario **MER-0664** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Anuncio previo de una oferta pública de adquisición de valores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Anuncio previo de una oferta pública de adquisición de valores” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:anuncio-previo-oferta-publica-adquisicion-valores-mer-0664`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] ACUERDOS RELATIVOS A LA OFERTA
- [ ] AUTORIZACIONES Y DEFENSA DE LA COMPETENCIA
- [ ] CONDICIONES DE EFICACIA DE LA OFERTA
- [ ] CONTRAPRESTACIÓN
- [ ] DECISIÓN DE FORMULAR LA OFERTA
- [ ] IDENTIFICACIÓN DEL OFERENTE
- [ ] INFORMACIÓN SOBRE LA SOCIEDAD AFECTADA
- [ ] INICIATIVAS EN MATERIA BURSÁTIL
- [ ] OTRAS INFORMACIONES
- [ ] PARTICIPACIÓN DEL OFERENTE
- [ ] PRESENTACIÓN DE LA OFERTA
- [ ] TIPO DE OFERTA
- [ ] VALORES Y MERCADOS DE LA OFERTA

## Normas que cita el formulario

- art. 30.6 Real Decreto 1362/2007

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

El presente anuncio se hace público en virtud de lo previsto en el Real Decreto
INFORMACIONES

1. El presente anuncio se hace público en virtud de lo previsto en el Real Decreto

1066/2007, de 27 julio, sobre el régimen de las ofertas públicas de adquisición de valores y contiene las principales características de la oferta, que está sujeta a la preceptiva autorización de la Comisión Nacional del Mercado de Valores.

Los términos y características detallados de la oferta estarán contenidos en el folleto explicativo que se publicará tras la obtención de la referida autorización.

INFORMACIONES

2.1. Identificación del oferente.- [IDENTIFICACIÓN DEL OFERENTE].

2.2 Decisión de formular la oferta.- [DECISIÓN DE FORMULAR LA OFERTA].

2.3. Presentación de la oferta.- [PRESENTACIÓN DE LA OFERTA]

2.4. Tipo de oferta.- [TIPO DE OFERTA]

2.5. Participación del oferente en la sociedad afectada.- [PARTICIPACIÓN DEL OFERENTE]

2.6. Información sobre la sociedad afectada.- [INFORMACIÓN SOBRE LA SOCIEDAD AFECTADA]

2.7. Valores y mercados a los que se dirige la oferta.- [VALORES Y MERCADOS DE LA OFERTA].

2.8. Contraprestación.- [CONTRAPRESTACIÓN]

2.9. Condiciones para la eficacia de la oferta.- [CONDICIONES DE EFICACIA DE LA OFERTA].

2.10. Defensa de la competencia y autorizaciones de otros organismos supervisores.- [AUTORIZACIONES Y DEFENSA DE LA COMPETENCIA].

2.11. Acuerdos relativos a la oferta.- [ACUERDOS RELATIVOS A LA OFERTA].

2.12. Iniciativas en materia bursátil.- [INICIATIVAS EN MATERIA BURSÁTIL].

2.13. Otras informaciones.- [OTRAS INFORMACIONES].

2.14. Lugar, fecha y firma.

3..

4. De acuerdo con lo establecido en el artículo 30.6 del Real Decreto 1362/2007, de 19 octubre, a partir de la fecha del presente anuncio, aquellos accionistas de (denominación social de la sociedad afectada) que adquieran valores que atribuyan derechos de voto deberán notificar a la Comisión Nacional del Mercado de Valores dicha adquisición cuando la proporción de derechos de voto en su poder alcance o supere el 1%. Asimismo, los accionistas que ya tuvieran el 3% de los derechos de voto notificarán cualquier operación que implique una variación posterior en dicho porcentaje.

En aplicación de lo dispuesto en el apartado 2.b) de la Norma quinta de la Circular

1/2017, de 26 abril, de la Comisión Nacional del Mercado de Valores, a partir de la fecha del presente anuncio deberá suspenderse la operativa del contrato de liquidez de la sociedad afectada en el caso de que exista.

---
name: poliza-seguro-transporte-terrestre-mercancias-modelo-mer-0691
description: "Póliza de seguro de transporte terrestre de mercancías (modelo). Lo redacta con los datos del caso y comprueba las normas con Jurisprudenciator."
---

# Póliza de seguro de transporte terrestre de mercancías (modelo)

> Formulario **MER-0691** del plugin **Seguros: pólizas, coberturas y reclamaciones** (`formularios-seguros`) · Mercantil › Seguros · normativa revisada el 24-11-2026.

## Qué es

Póliza de seguro de transporte terrestre de mercancías (póliza flotante para una agencia de transportes), con condiciones generales, condiciones particulares y condiciones especiales, conforme a la Ley 50/1980, de 8 de octubre, de Contrato de Seguro (LCS). Se usa para asegurar los daños materiales que sufran las mercancías con ocasión o a consecuencia de su transporte por carretera o ferrocarril.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Póliza de seguro de transporte terrestre de mercancías (modelo)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Póliza de seguro de transporte terrestre de mercancías (modelo)” para mi caso». También puedes invocarla directamente con `/formularios-seguros:poliza-seguro-transporte-terrestre-mercancias-modelo-mer-0691`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguros:indice`.

## Qué contiene esta skill

- `formulario.md`: el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `marco.md`: la guía del tema (Seguros: pólizas, coberturas y reclamaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (17 veces)
- [ ] DENOMINACIÓN SOCIAL DE LA AGENCIA DE TRANSPORTE (2 veces)
- [ ] FECHA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] AÑO
- [ ] DESTINATARIO Y DATOS DE CONTACTO DE LA ASEGURADORA
- [ ] DÍA
- [ ] IMPORTE O PORCENTAJE
- [ ] LOCALIDAD
- [ ] MATRÍCULA
- [ ] MES
- [ ] NOMBRE DEL AGENTE
- [ ] Nº DE ARTÍCULOS
- [ ] Nº DE ARTÍCULOS LIMITATIVOS
- [ ] Nº DE AÑOS
- [ ] Nº DE PÓLIZA
- [ ] Nº DE VIAJES
- [ ] REFERENCIA DE LAS CONDICIONES ESPECIALES
- [ ] SUCURSAL

## Normas que cita el formulario

- art. 367 Código de Comercio
- art. 22 LCS
- art. 4 LCS
- art. 25 LCS
- art. 31 LCS
- art. 57 LCS
- art. 18 LCS
- art. 38 LCS
- art. 20 LCS
- art. 40 LCS

---

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…2 LCS. Es un contrato consensual, bilateral, oneroso, nominado, típico y formal.»: el artículo 33 de las condiciones generales (letras d y e) reproduce un incremento de la indemnización del 20% anual por mora; comprobar su adecuación a la redacción vigente del artículo 20 LCS.
- Junto a «…gada de la mercancía al lugar de destino, salvo prórrogas que puedan convenirse.»: el original aparecía truncado en este punto; se ha completado el inicio del segundo párrafo con la regla habitual para el transporte con medios propios. Comprobar su redacción.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTA EXPLICATIVA

El artículo 54 LCS define el seguro de transporte terrestre: por él, el asegurador se obliga, dentro de los límites establecidos por la Ley y en el contrato, a indemnizar los daños materiales que puedan sufrir con ocasión o consecuencia del transporte las mercancías porteadas, el medio utilizado u otros objetos asegurados. Al tratarse de un seguro de daños, debe respetar las disposiciones generales de este tipo de seguros (artículos 25 a 44 LCS), así como los artículos 1 a 22 LCS, aplicables al contrato de seguro cualquiera que sea su modalidad. Su regulación específica se contiene en los artículos 54 a 62 LCS. Es un contrato consensual, bilateral, oneroso, nominado, típico y formal.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee `formulario.md` entero y la parte de `marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

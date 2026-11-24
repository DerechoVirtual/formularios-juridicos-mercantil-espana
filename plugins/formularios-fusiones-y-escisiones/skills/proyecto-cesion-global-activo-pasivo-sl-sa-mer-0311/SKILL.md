---
name: proyecto-cesion-global-activo-pasivo-sl-sa-mer-0311
description: "Proyecto de cesión global de activo y pasivo de una SL o SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Proyecto de cesión global de activo y pasivo de una SL o SA

> Formulario **MER-0311** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Proyecto de cesión global de activo y pasivo de una SL o SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Proyecto de cesión global de activo y pasivo de una SL o SA” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:proyecto-cesion-global-activo-pasivo-sl-sa-mer-0311`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] BENEFICIARIO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] FECHA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NORMATIVA APLICABLE

## Normas que cita el formulario

- art. 74 Real Decreto-ley 5/2023

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

Los administradores de la sociedad habrán de redactar y suscribir un proyecto de cesión global, que contendrá, al menos, las siguientes menciones: la denominación, el tipo social y el domicilio de la sociedad y los datos de identificación del cesionario o cesionarios; La fecha a partir de la cual la cesión tendrá efectos contables de acuerdo con lo dispuesto en el Plan General de Contabilidad; la información sobre la valoración del activo y pasivo del patrimonio, la designación y, en su caso, el reparto preciso de los elementos del activo y del pasivo que han de transmitirse a cada cesionario; la contraprestación que hayan de recibir la sociedad o los socios. Cuando la contraprestación se atribuya a los socios, se especificará el criterio en que se funde el reparto; las posibles consecuencias de la cesión global sobre el empleo y la acreditación de encontrarse al corriente en el cumplimiento de las obligaciones tributarias y frente a la Seguridad Social.

I. De conformidad con lo establecido en el art. 74 del Real Decreto-ley 5/2023 los administradores de [DENOMINACIÓN SOCIAL] (en adelante sociedad cedente) han redactado y aprobado el presente Proyecto de cesión global de activo y pasivo a favor de [BENEFICIARIO] (en adelante cesionario).

Como consecuencia de la cesión global el cesionario adquirirá en bloque el patrimonio de la sociedad cedente, por sucesión universal en sus derechos y obligaciones.

II. Se redacta con sujeción a todo lo dispuesto en el [NORMATIVA APLICABLE].

En cumplimiento de las previsiones contenidas en el art.74 del RD-ley 5/2023, se redacta a continuación el presente Proyecto de cesión global de activo y pasivo con las menciones exigidas por el mismo:

1. Datos identificativos del cedente y del cesionario/s

Sociedad cedente:

Denominación social:

Domicilio social:

Datos registrales:

N.I.F.:

Cesionario/s:

La cesión global de activo y pasivo se efectúa a favor de [BENEFICIARIO]:

[OPCIONAL — incluir si procede]

(Persona Física)

Nombre y apellidos:

Domicilio:

N.I.F.:

[OPCIONAL — incluir si procede]

(Persona jurídica)

Denominación social:

Domicilio social:

Datos registrales:

N.I.F.:

2. Fecha de efectividad de la cesión global a efectos contables

A efectos contables, se fija como fecha a partir de la cual las operaciones de la sociedad cedente han de considerarse realizadas por el cesionario [DENOMINACIÓN SOCIAL].

3. Valoración de activo y pasivo- y reparto entre los cesionarios

Valoración del activo:.

Valoración del pasivo:.

[OPCIONAL — incluir si procede]

En caso de reparto entre cesionarios

La totalidad de los activos y pasivos de la sociedad cedente será atribuida a los cesionarios sin que quede sin designar y repartir ningún activo o pasivo de la sociedad que se escinde.

A continuación, se designan los activos y pasivos trasmitidos a cada uno de los cesionarios:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

A D./Dña. [NOMBRE Y APELLIDOS], se le transmiten los siguientes elementos del activo y del pasivo: [DESCRIPCIÓN DEL BIEN].

4. Contraprestación

A cambio del patrimonio transmitido, la sociedad cedente recibirá del cesionario una contraprestación de [IMPORTE].

5. Efectos de la cesión global sobre el empleo.

Como consecuencia de la cesión global no se extinguirán las relaciones laborales existentes en la sociedad cedente. En su lugar, el cesionario se subrogará en los derechos y obligaciones laborales y de Seguridad Social de la sociedad cedente, incluyendo los compromisos por pensiones y, en general, las obligaciones adquiridas en materia de protección social complementaria.

6. Cumplimiento de las obligaciones fiscales y laborales

Las sociedades participantes en la Modificación estructural están al corriente en el cumplimiento de sus obligaciones fiscales y con la seguridad social, tal y como queda acreditado en

Otras menciones

En [LUGAR], a [FECHA].

CEDENTE

CESIONARIO

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

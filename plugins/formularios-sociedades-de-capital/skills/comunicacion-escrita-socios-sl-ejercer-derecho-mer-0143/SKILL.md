---
name: comunicacion-escrita-socios-sl-ejercer-derecho-mer-0143
description: "Comunicación escrita a los socios de una SL para ejercer el derecho de preferencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Comunicación escrita a los socios de una SL para ejercer el derecho de preferencia

> Formulario **MER-0143** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Comunicación escrita a los socios de una SL para ejercer el derecho de preferencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Comunicación escrita a los socios de una SL para ejercer el derecho de preferencia” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:comunicacion-escrita-socios-sl-ejercer-derecho-mer-0143`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (4 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHA
- [ ] MES

## Normas que cita el formulario

- art. 305.3 LSC
- art. 304 TRLSC
- art. 307 TRLSC

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

A pesar de que el procedimiento habitual es que el acuerdo de aumento de capital social que otorgue derecho de preferencia a los socios se publique en el BORME, se permite que el órgano de administración sustituya tal publicación por una comunicación escrita a cada socio y, en su caso, a los usufructuarios inscritos en el libro registro (artículo 305.3 LSC).

S. L. (Denominación de la Sociedad)

(Domicilio de la Sociedad)

(Nombre o denominación del socio)

(Domicilio)

Estimado Sr./Sra. [NOMBRE Y APELLIDOS]:

Mediante la presente le comunico que la junta general de la sociedad [DENOMINACIÓN SOCIAL] S.L., celebrada el [FECHA] de [MES] de [AÑO], adoptó el acuerdo de aumentar el capital social en [IMPORTE] Euros, en las condiciones que se explican seguidamente:

1.—El aumento del capital se realizará mediante la emisión de (numero y letra) nuevas participaciones sociales de [IMPORTE] (numero y letra) Euros de valor nominal cada una.

2.—Los actuales socios podrán ejercitar el derecho de asunción preferente respecto de [Nº] (numero y letra) participaciones nuevas por cada una de las antiguas de las que fueran titulares (artículo 304 TRLSC).

3.—El plazo para el ejercicio de ese derecho será de un mes desde la fecha del envio de esta comunicación, expresada más abajo.

4.—Trascurrido dicho plazo, las participaciones que no hayan sido efectivamente asumidas e íntegramente desembolsadas, podrán serlo por los restantes socios. Para ello habrán de haber comunicado, al asumir las nuevas participaciones, su deseo de suscribir el número de participaciones sobrantes (artículo 307 TRLSC).

5.—Al finalizar el plazo fijado en el apartado 3, el órgano de administración comunicará a cada socio interesado, en el plazo de los [Nº] días siguientes, la asignación de las participaciones sobrantes de acuerdo con las solicitudes recibidas. Si existiesen varios socios interesados en asumir las participaciones ofrecidas, éstas se adjudicarán en proporción a las que cada uno de ellos ya tuviere en la sociedad, incluyendo las asumidas y desembolsadas en la ampliación dentro del plazo inicial. Los socios deberán desembolsar el importe correspondiente a la asignación resultante dentro del plazo de [Nº] días [ELEGIR: naturales / hábiles] siguientes desde la recepción de la comunicación realizada al efecto por el órgano de administración.

6.—Si quedaran participaciones sobrantes, el órgano de administración, en los quince días siguientes, podrá adjudicarlas a personas extrañas a la sociedad que deseen asumirlas.

7.—Las cantidades que cada socio deba desembolsar como consecuencia de la ampliación deberán hacerse mediante entrega en metálico, cheque, o justificante de transferencia bancaria a la cuenta de la sociedad n.º [Nº]

Todo lo cual se le comunica a Usted de conformidad y a los efectos previstos en los artículos 304 y ss. del Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el Texto Refundido de la Ley de Sociedades de Capital

Atentamente le saluda,

D./Dña. [NOMBRE Y APELLIDOS]

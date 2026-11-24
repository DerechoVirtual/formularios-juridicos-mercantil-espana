---
name: solicitud-judicial-interventores-convocar-asamblea-mer-0472
description: "Solicitud judicial de interventores para convocar la asamblea ordinaria de la cooperativa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud judicial de interventores para convocar la asamblea ordinaria de la cooperativa

> Formulario **MER-0472** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de solicitud ante órgano judicial por parte, bien de los interventores,o bien de los socios, de una sociedad cooperativa, mediante el cual se solicita la celebración de Asamblea General Ordinaria al haber transcurrido más de seis meses desde la fecha del ejercicio económico sin que se haya procedido a su convocatoria y tras haber instado su celebración al Consejo Rector, sin haber obtenido respuesta.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud judicial de interventores para convocar la asamblea ordinaria de la cooperativa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud judicial de interventores para convocar la asamblea ordinaria de la cooperativa” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:solicitud-judicial-interventores-convocar-asamblea-mer-0472`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (10 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] DNI/NIE (4 veces)
- [ ] FECHA (3 veces)
- [ ] CALLE (2 veces)
- [ ] DOCUMENTOS ACREDITATIVOS (2 veces)
- [ ] AÑO
- [ ] LUGAR
- [ ] SEDE
- [ ] ÓRGANO

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

Modelo de solicitud ante órgano judicial por parte, bien de los interventores,o bien de los socios, de una sociedad cooperativa, mediante el cual se solicita la celebración de Asamblea General Ordinaria al haber transcurrido más de seis meses desde la fecha del ejercicio económico sin que se haya procedido a su convocatoria y tras haber instado su celebración al Consejo Rector, sin haber obtenido respuesta.


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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

[OPCIONAL — incluir si procede]

(Por Interventores)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD] y DNI número [DNI/NIE] y D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD] y DNI número [DNI/NIE] en su calidad de Interventores de ‘[DENOMINACIÓN SOCIAL], S. Coop.’, con domicilio en [LOCALIDAD], calle [CALLE], como acreditan con [DOCUMENTOS ACREDITATIVOS], ante el Tribunal de Instancia comparecen y como mejor proceda en Derecho DICEN:

[OPCIONAL — incluir si procede]

(Por socios)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD] y DNI número [DNI/NIE] y D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD] y DNI número [DNI/NIE] en su calidad de socios de ‘[DENOMINACIÓN SOCIAL], S. Coop.’, con domicilio en [LOCALIDAD], calle [CALLE], como acreditan con [DOCUMENTOS ACREDITATIVOS], ante el Tribunal de Instancia comparecen y como mejor proceda en Derecho DICEN:

Primero.- Que el día [FECHA] se cerró el ejercicio económico correspondiente al año [AÑO] de ‘[DENOMINACIÓN SOCIAL], S.Coop.’, por lo que ha transcurrido con creces el plazo de seis meses desde dicha fecha, tal y como establece el artículo 23.1 de la Ley 27/99, de 16 de julio, de Cooperativas, sin que haya sido convocada la Asamblea General Ordinaria que dicho precepto cita.

Segundo.- Que, por ese motivo, y en cumplimiento del derecho y deber que a quienes suscriben el presente escrito, en su calidad de [ELEGIR: Interventores / socios] de ‘[DENOMINACIÓN SOCIAL], S.Coop.’ otorga e impone el apartado 2 del precepto citado en el ordinal precedente, fue requerido el Consejo Rector de la sociedad el pasado día [FECHA] como se acredita con la copia fechada y sellada que acompaña al presente escrito como documento número

Tercero.- Que ha transcurrido el plazo de quince días que el artículo 23 de la Ley de Cooperativas establece al efecto sin que el Consejo Rector haya convocado la Asamblea General Ordinaria.

Cuarto.- Que quienes suscriben este escrito proponen como Presidente y Secretario de la Asamblea a celebrar a D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] y como Orden del Día el siguiente:

Por lo expuesto,

SUPLICAMOS AL TRIBUNAL DE INSTANCIA se digne dictar resolución por la que se convoque la Asamblea General Ordinaria de ‘ S.Coop.’ en el domicilio social de la misma, designando las personas que habrán de ocupar los cargos de Presidente y Secretario de dicha Asamblea, la fecha, lugar y hora de reunión tanto en primera como en segunda convocatoria, así como los asuntos señalados en el Orden del Día propuesto en el ordinal Cuarto, ordenándose asimismo su correspondiente publicidad mediante [ÓRGANO], por ser justicia que pedimos en [LUGAR], a [FECHA].

PARTE 1

PARTE 2

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

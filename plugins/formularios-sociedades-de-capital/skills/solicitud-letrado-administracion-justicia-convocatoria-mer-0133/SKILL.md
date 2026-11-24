---
name: solicitud-letrado-administracion-justicia-convocatoria-mer-0133
description: "Solicitud al letrado de la Administración de Justicia de convocatoria de junta extraordinaria de SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud al letrado de la Administración de Justicia de convocatoria de junta extraordinaria de SA

> Formulario **MER-0133** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Los administradores deberán convocar la junta general cuando lo soliciten uno o varios socios que representen, al menos, el cinco por ciento del capital social, expresando en la solicitud los asuntos a tratar. Si los administradores no atienden oportunamente la solicitud de convocatoria efectuada por la minoría, podrá realizarse, previa audiencia de los administradores, por el Letrado de la Administración de Justicia o por el Registrador mercantil del domicilio social.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud al letrado de la Administración de Justicia de convocatoria de junta extraordinaria de SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud al letrado de la Administración de Justicia de convocatoria de junta extraordinaria de SA” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:solicitud-letrado-administracion-justicia-convocatoria-mer-0133`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] Nº DE ARTÍCULO (3 veces)
- [ ] CALLE (2 veces)
- [ ] FECHA (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DNI/NIE
- [ ] LUGAR
- [ ] NIF
- [ ] NOMBRE Y APELLIDOS
- [ ] NÚMERO
- [ ] SEDE

## Normas que cita el formulario

- art. 168.2 TRLSC
- art. 169.2 TRLSC
- art. 363.1.c TRLSC

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

Los administradores deberán convocar la junta general cuando lo soliciten uno o varios socios que representen, al menos, el cinco por ciento del capital social, expresando en la solicitud los asuntos a tratar. Si los administradores no atienden oportunamente la solicitud de convocatoria efectuada por la minoría, podrá realizarse, previa audiencia de los administradores, por el Letrado de la Administración de Justicia o por el Registrador mercantil del domicilio social.


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

AL LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA DE LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA [SEDE]

D./Dª. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE] y domicilio a efecto de estas actuaciones en calle [CALLE], número, en su condición de accionista y presidente del consejo de administración de la sociedad «[DENOMINACIÓN SOCIAL], S.A.», con NIF número [NIF] y domicilio en calle [CALLE], número [NÚMERO], ante ese tribunal comparezco y respetuosamente

EXPONGO

1. Que el día [FECHA] recibí notarialmente una solicitud proveniente de accionistas que representan más del 5% del capital social desembolsado, exigiendo que se convocara junta general extraordinaria de accionistas (se adjunta como documento número 1 fotocopia de la diligencia notarial).

2. Que los estatutos sociales obligan a efectuar la convocatoria de la junta «cuando se lo pida un número de accionistas que representen por lo menos un 5% del capital social» (artículo [Nº DE ARTÍCULO] de los estatutos del que se adjunta fotocopia como documento número 2).

Tal mandato refleja lo dispuesto en el artículo 168 del Texto Refundido de la Ley de Sociedades de Capital, a cuyo tenor:

«Los administradores deberán convocar la junta general cuando lo soliciten uno o varios socios que representen, al menos, el cinco por ciento del capital social, expresando en la solicitud los asuntos a tratar.

En este caso, la junta general deberá ser convocada para su celebración dentro del mes siguiente a la fecha en que se hubiere requerido notarialmente a los administradores para convocarla, debiendo incluirse necesariamente en el orden del día los asuntos que hubiesen sido objeto de solicitud.»

3. Que el consejo de administración está formado por (seis) consejeros. Tres de los consejeros representan a un grupo de accionistas y otros tres a otro grupo. Las decisiones del consejo se toman por la mayoría de consejeros presentes o representados. Para que el consejo tome decisiones se requiere que estén presentes o representados la mitad más uno de sus miembros. Debido a lo anterior tres, de los consejeros pueden paralizar la actuación del consejo simplemente no asistiendo a las reuniones del consejo. (Se adjunta fotocopia del artículo [Nº DE ARTÍCULO] de los estatutos como documento número 3).

4. Por otra parte, se convocó al consejo de administración para el día [DÍA] de [MES] de [AÑO]. La convocatoria se hizo de acuerdo con el artículo [Nº DE ARTÍCULO] de los estatutos (documento número 3) enviando carta certificada el día [DÍA] de [MES] de [AÑO] (se adjunta fotocopia justificante como documento número 4).

El mismo día [FECHA] se adelantó este aviso mediante comunicación por fax (se adjunta fotocopia como documento número 5).

5. El día [DÍA] de [MES] de [AÑO] el consejo de administración no se pudo celebrar al faltar tres de los consejeros. Esta es la prueba más evidente de la inoperatividad del consejo.

Se adjunta fotocopia del documento en que se justificaba la no presencia de esos consejeros y que fue entregado en presencia de un notario. Es el documento número 6.

6. Al no haberse podido reunir el consejo, no se ha podido convocar la junta para su celebración en el mes siguiente (artículo 168.2 TRLSC y se cumple el presupuesto que según el artículo 169.2 TRLSC permite la solicitud de convocatoria especial.

7. Que en mi persona se reúnen las cualidades de presidente del consejo y accionista titular de más del 5% del capital (lo que se justifica con fotocopia legitimada notarialmente de los títulos, documento número 7), y me permite solicitar la convocatoria especial en base al artículo 169.2 del TRLSC.

8. A la vista de la paralización del consejo de administración por la actuación de una parte del mismo, por encima de lo dispuesto en la Ley, y teniendo en cuenta que de persistir esta actitud pudiera incurrirse en causa de disolución de la sociedad [artículo 363.1.c) TRLSC], es por lo que, ante el Tribunal comparezco y

SOLICITO

Que al amparo del artículo 169.2 del Texto Refundido de la Ley de Sociedades de Capital, se proceda a la convocatoria judicial de la junta.

Es justicia que pido en [LUGAR], a [DÍA] de [MES] de [AÑO].

Firma.

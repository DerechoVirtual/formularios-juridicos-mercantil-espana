---
name: auto-acuerda-acumular-juicio-declarativo-civil-mer-0811
description: "Auto que acuerda acumular el juicio declarativo civil al procedimiento concursal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Auto que acuerda acumular el juicio declarativo civil al procedimiento concursal

> Formulario **MER-0811** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

TRIBUNAL DE INSTANCIA DE , SECCIÓN DE LO MERCANTIL, PLAZA JUDICIAL N.º AUTO ANTECEDENTES DE HECHO RAZONAMIENTOS JURÍDICOS PARTE DISPOSITIVA Firmas Auto acordando la acumulación al procedimiento concursal del juicio ordinario que se tramita en otra Sección de lo Mercantil del Tribunal de Instancia.

Es un modelo de tipo **resoluciones judiciales (autos, decretos, providencias, diligencias)**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Auto que acuerda acumular el juicio declarativo civil al procedimiento concursal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Auto que acuerda acumular el juicio declarativo civil al procedimiento concursal” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:auto-acuerda-acumular-juicio-declarativo-civil-mer-0811`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NÚMERO (8 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] AÑO (3 veces)
- [ ] FECHA (3 veces)
- [ ] LUGAR (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] SEDE (2 veces)
- [ ] LOCALIDAD
- [ ] Nº DE FAX
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 451 LEC

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

- Junto a «…a Sección de lo Mercantil del Tribunal de Instancia, plaza n.º [NÚMERO], de esta»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

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

TRIBUNAL DE INSTANCIA DE [SEDE], SECCIÓN DE LO MERCANTIL, PLAZA JUDICIAL N.º [NÚMERO]

Tfno [TELÉFONO]

Fax [Nº DE FAX]

Concurso n.º [NÚMERO]/[AÑO]

Deudor:

Abogado [NOMBRE Y APELLIDOS] Procurador/a [NOMBRE Y APELLIDOS]

Acreedores: [NOMBRE DE LA PARTE].

Abogado [NOMBRE Y APELLIDOS] Procurador/a [NOMBRE Y APELLIDOS]

AUTO

D./Dña. [NOMBRE Y APELLIDOS], Magistrado-Juez de la Sección de lo Mercantil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO]

En [LUGAR], a [FECHA].

ANTECEDENTES DE HECHO

PRIMERO

Por la Administración Concursal se ha solicitado la acumulación a este procedimiento concursal del siguiente juicio declarativo que se tramita en la otra Sección de lo Mercantil del Tribunal de Instancia, n.º [NÚMERO], de esta Villa: Juicio Ordinario n.º [NÚMERO]/[AÑO], siendo parte demandante D./Dña. [NOMBRE Y APELLIDOS] y parte demandada [NOMBRE DE LA PARTE], sobre disolución de sociedad, iniciado con fecha [FECHA], y que se encuentra en trámite de celebración del acto del juicio.

SEGUNDO

Se alega la inviabilidad de que en el concurso se debata la aceptación de un convenio, cuando en el juicio identificado se tiene demandada la disolución de la sociedad por inoperancia de los órganos sociales.

TERCERO

Este procedimiento concursal se encuentra en trámite de emisión del informe de la Administrador Concursal.

RAZONAMIENTOS JURÍDICOS

PRIMERO

La regla general del art. 137 LC consiste en que los juicios declarativos que se estuvieran tramitando al declararse el concurso en los que fuera parte el concursado, continúen hasta la firmeza de la sentencia, se entiende que en el Tribunal que estuviera conociendo.

Sin embargo, se admite en la misma norma la salvedad de que dichos juicios pertenezcan a una de las categorías especiales de la ley que obligan a mudarlos al juzgado del concurso (acumulación) o a congelarlos por completo (suspensión).

SEGUNDO

Se concitan en el presente supuesto los requisitos para activar la excepción de legitimación, tempestividad, y condición procesal del juicio civil puesto de manifiesto.

En cuanto al presupuesto material, se considera que no es ya de trascendencia sustancial para la formación de las masas, sino impracticable para ello de cara a una solución del concurso, que uno de los administradores sociales de la concursada pretenda la disolución de la mercantil por la paralización de los órganos sociales que impiden el funcionamiento de la empresa, y el otro se encuentre impulsando la aceptación de un convenio, con la intervención de la Administración Concursal. El riesgo de una resolución que se dicte en proceso ajeno al concursal, y que atienda al estado de disfuncionamiento de la sociedad anterior a la apertura del concurso, pudiendo conllevar un fallo que abocaría a una liquidación, aconsejan extremar la ‘vis attractiva’ de este procedimiento derivada de la insolvencia, y concentrar la resolución de este conflicto en el único procedimiento universal.

TERCERO

Lógicamente, no hay obstáculo para la acumulación solicitada por cuanto el juicio acumulable se conozca en otra Sección de lo Mercantil del Tribunal de Instancia, como si conociera este mismo, bien que no como Tribunal concursal, y así, procede acceder a la acumulación, interesándose la remisión de lo actuado para la continuación y resolución del proceso en el seno de este procedimiento de concurso.

PARTE DISPOSITIVA

SE ACUERDA LA ACUMULACIÓN a este procedimiento concursal del juicio ordinario que se tramita bajo número [NÚMERO]/[AÑO] en la Sección de lo Mercantil del Tribunal de Instancia, plaza n.º [NÚMERO], de esta Villa, al que se dirigirá oficio, junto con testimonio de esta resolución, interesando la remisión de las actuaciones, en la que emplazará a las partes personadas para que comparezcan en este Tribunal en el plazo de diez días.

Así lo acuerdo, mando y firmo

Es justicia de hacerse en [LUGAR], a [FECHA].

Firma del Juez/a

Contra esta resolución cabe recurso de reposición, que puede interponerse ante el mismo Tribunal, sin efectos suspensivos, por escrito en el plazo de cinco días hábiles contados desde el siguiente a la notificación, debiéndose expresar la infracción cometida a juicio del recurrente (art. 546 LC, y arts. 451 y 452 LEC).

Para interponer el recurso será necesario la constitución de un depósito de 25 euros, sin cuyo requisito no será admitido a trámite. El depósito se constituirá consignando dicho importe en la Cuenta de Depósitos y Consignaciones que este Tribunal tiene abierta en [LOCALIDAD] con el número [NÚMERO], indicando en el campo concepto del resguardo de ingreso que se trata de un "Recurso" código 00-Reposición. La consignación deberá ser acreditada al interponer el recurso (disp. adic. 15.ª de la LOPJ).

Están exentos de constituir el depósito para recurrir los incluidos en el apartado 5 de la disposición citada y quienes tengan reconocido el derecho a la asistencia jurídica gratuita.

========================================================================

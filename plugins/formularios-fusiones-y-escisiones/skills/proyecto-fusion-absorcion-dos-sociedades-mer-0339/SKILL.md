---
name: proyecto-fusion-absorcion-dos-sociedades-mer-0339
description: "Proyecto de fusión por absorción de dos sociedades. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Proyecto de fusión por absorción de dos sociedades

> Formulario **MER-0339** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Proyecto de fusión por absorción de dos sociedades» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Proyecto de fusión por absorción de dos sociedades” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:proyecto-fusion-absorcion-dos-sociedades-mer-0339`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE O DENOMINACIÓN (14 veces)
- [ ] DENOMINACIÓN SOCIAL (11 veces)
- [ ] IMPORTE (8 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] Nº (6 veces)
- [ ] FECHA (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº DE TÍTULOS (4 veces)
- [ ] NIF (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] Nº DE PARTICIPACIONES O ACCIONES (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CAUSA
- [ ] HORA
- [ ] LUGAR
- [ ] OTRAS MODIFICACIONES ESTATUTARIAS
- [ ] OTROS DATOS
- [ ] TEXTO DEL ARTÍCULO

## Normas que cita el formulario

- art. 40 Real Decreto-ley 5/2023

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

PROYECTO DE FUSIÓN POR ABSORCIÓN DE LAS SOCIEDADES «[NOMBRE O DENOMINACIÓN]» (ABSORBENTE) y «[NOMBRE O DENOMINACIÓN]» (ABSORBIDA)
Firmas

Los administradores de cada una de las sociedades que participen en la fusión por absorción habrán de redactar y suscribir un proyecto común de fusión con el contenido establecido en el art. 40 del Real Decreto-ley 5/2023. Si falta la firma de alguno de ellos, se señalará al final del proyecto, con indicación de la causa.

PROYECTO DE FUSIÓN POR ABSORCIÓN DE LAS SOCIEDADES «[NOMBRE O DENOMINACIÓN]» (ABSORBENTE) y «[NOMBRE O DENOMINACIÓN]» (ABSORBIDA)

Conforme a lo exigido en los artículos 39.1 y 40 del RD-ley 5/2023, los administradores de las sociedades «[NOMBRE O DENOMINACIÓN]» y «[NOMBRE O DENOMINACIÓN]» en el presente documento redactan el pertinente proyecto de fusión por absorción de [DENOMINACIÓN SOCIAL] por [DENOMINACIÓN SOCIAL], con el objeto de ser sometido a las respectivas juntas generales.

Primero.- Identificación de las sociedades participantes

• Sociedad absorbente: «[NOMBRE O DENOMINACIÓN]», NIF [NIF], con domicilio social en [LOCALIDAD], población [LOCALIDAD], constituida mediante escritura pública autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], con el número [NÚMERO] de su protocolo, e inscrita en el Registro Mercantil de [LOCALIDAD],

• Sociedad absorbida: «[NOMBRE O DENOMINACIÓN]», NIF [NIF], con domicilio social en [LOCALIDAD], población [LOCALIDAD] constituida mediante escritura pública autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], con el número [NÚMERO] de su protocolo, e inscrita en el Registro Mercantil de [LOCALIDAD],

Segundo.- Tipo y procedimiento de canje

A) Tipo de canje

La sociedad absorbente «[DENOMINACIÓN SOCIAL]» posee en la actualidad un capital social de [IMPORTE] euros divididos en [Nº DE PARTICIPACIONES O ACCIONES] de [IMPORTE] euros de valor nominal cada una, números 1 a [Nº] ambos inclusive. Esta sociedad procede a aumentar su capital en la cantidad de [IMPORTE] euros creando un total de [Nº] nuevas [ELEGIR: participaciones / acciones] de [IMPORTE] euros de valor nominal cada una, números [Nº] a [Nº] ambos incluidos.

Las nuevas [ELEGIR: participaciones / acciones] se asignarán a los socios de la sociedad absorbida «[DENOMINACIÓN SOCIAL]» en la siguiente proporción de [Nº DE TÍTULOS] de «[NOMBRE O DENOMINACIÓN]» por cada [Nº DE TÍTULOS] de «[NOMBRE O DENOMINACIÓN]».

Por otra parte, los socios de «[NOMBRE O DENOMINACIÓN]» recibirán una compensación dineraria de [IMPORTE] euros por cada [ELEGIR: participación / acción] preexistente, mientras que la compensación dineraria de los socios de «[NOMBRE O DENOMINACIÓN]» será de [IMPORTE] euros por cada [ELEGIR: participación / acción] asignada

El tipo de canje se ha determinado teniendo en cuenta el valor real de los patrimonios sociales, tal y como exige el artículo 36.1 del RD-ley 5/2023.

Con esta finalidad, se ha atribuido a los socios de cada sociedad la parte correspondiente a las [HORA] propias o recíprocas poseídas por la propia sociedad y que son [Nº DE TÍTULOS] en «[NOMBRE O DENOMINACIÓN]» y [Nº DE TÍTULOS] en «[NOMBRE O DENOMINACIÓN]».

B) Procedimiento de canje.

El canje de las [ELEGIR: participaciones / acciones] de la sociedad absorbida «[DENOMINACIÓN SOCIAL]» se realizará en el domicilio social, bien personalmente o por correo, a partir de la firma de la escritura de fusión.

Las [ELEGIR: participaciones / acciones] de la sociedad absorbida «[DENOMINACIÓN SOCIAL]» se amortizarán y serán sustituidas por la asignación de las [ELEGIR: participaciones / acciones] realizada en la escritura de fusión.

Las [ELEGIR: participaciones / acciones] de la sociedad absorbida «[DENOMINACIÓN SOCIAL]» se amortizarán y serán sustituidas por [ELEGIR: participaciones / acciones] que podrán pedirse en el domicilio social, personalmente o por correo, a partir de la firma de la escritura de fusión.

Al no intervenir en la operación ninguna sociedad por acciones, no procede el canje sino que la asignación de las [ELEGIR: participaciones / acciones] se hará en la escritura de fusión.

Tercero.- Aportaciones de industria o prestaciones accesorias

En las sociedades que participan en el presente proceso de fusión no existen aportaciones de industria ni prestaciones accesorias [OTROS DATOS].

Cuarto.- Derechos o títulos especiales

En las sociedades que participan en el presente proceso de fusión no existen titulares de derechos especiales distintos de las [ELEGIR: participaciones / acciones]

Quinto.- Ventajas de expertos y administradores

En el presente proceso de fusión no se concederán ventajas especiales a favor de los expertos independientes ni a favor de los administradores participantes..

Sexto.- Fecha de inicio de participación en las ganancias

Las nuevas [ELEGIR: participaciones / acciones] darán derecho a participar en las ganancias sociales desde ..

Séptimo.- Fecha de inicio de efectos contables

Las operaciones de la sociedad absorbida se considerarán realizadas a efectos contables por cuenta de la sociedad absorbente a partir de [FECHA].

Octavo.- Modificaciones de los estatutos de la sociedad absorbente

Las modificaciones de los estatutos que la fusión provocará en la sociedad absorbente «[DENOMINACIÓN SOCIAL]» se describen a continuación:

• La sociedad absorbente [DENOMINACIÓN SOCIAL] procede al aumento de su capital social en la cantidad de [IMPORTE] euros mediante creación de [Nº DE PARTICIPACIONES O ACCIONES] nuevas [ELEGIR: participaciones / acciones], de [IMPORTE] euros de valor nominal cada una, números [Nº] al [Nº] ambos incluidos.

Como consecuencia del aumento de capital descrito el artículo [Nº DE ARTÍCULO] de los estatutos, relativo a la cifra del capital social, quedará redactado de la siguiente forma: [TEXTO DEL ARTÍCULO].

• [OTRAS MODIFICACIONES ESTATUTARIAS].

Noveno.- Valoración de los activos y pasivos de las sociedades que se fusionan.

Décimo.- Cuentas tenidas en cuenta para establecer las condiciones de la fusión.

Las cuentas de las sociedades que se fusionan utilizadas para establecer las circunstancias y condiciones en que se realiza la fusión han sido cerradas a fecha [FECHA]

Decimoprimero.- Efectos de la fusión sobre el empleo, de impacto de género y en la responsabilidad social de la empresa

A) Consecuencias de la fusión sobre el empleo..

B) Impacto de género en los órganos de administración.

C) Incidencia en la responsabilidad social de la empresa.

Decimosegundo.- Otros efectos

Cambios en el órgano de administración de la sociedad absorbente.

Amortización depropias o recíprocas.

Las [ELEGIR: participaciones / acciones] de las sociedades que se fusionan, que estuvieran en poder de cualquiera de ellas o en el de otras personas que actuasen por cuenta de esas sociedades, no podrán canjearse por [ELEGIR: participaciones / acciones] de la sociedad resultante de la fusión debiendo ser amortizadas o extinguidas.

Su valor en el patrimonio de la sociedad ha sido tenido en cuenta para calcular la relación o tipo de canje.

Régimen fiscal especial.

• 1.º La fusión tiene como finalidad [CAUSA].

• 2.º La operación de fusión puede acogerse, de este modo, al régimen especial establecido en [Nº DE ARTÍCULO], por la Ley 27/2014 del Impuesto sobre Sociedades.

Decimotercero.- Lugar y fecha.

Este proyecto de fusión es suscrito en [LUGAR], a [FECHA].

Decimocuarto.- Firma de los administradores de las sociedades que se fusionan.

A continuación, se incluye la firma de todos los administradores de las sociedades que se fusionan.

1.º Firmas de los administradores de la sociedad «[DENOMINACIÓN SOCIAL]»

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

2.º Firmas de los administradores de la sociedad «[DENOMINACIÓN SOCIAL]»

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

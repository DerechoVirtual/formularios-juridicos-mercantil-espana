---
name: sociedad-mercantil-irregular-contrato-mer-0131
description: "Sociedad mercantil irregular (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Sociedad mercantil irregular (contrato)

> Formulario **MER-0131** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Sociedad mercantil irregular (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Sociedad mercantil irregular (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:sociedad-mercantil-irregular-contrato-mer-0131`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] CALLE
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE O DENOMINACIÓN
- [ ] NÚMERO
- [ ] OBJETO SOCIAL

## Normas que cita el formulario

- art. 136 Código de Comercio

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

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS:

D [NOMBRE Y APELLIDOS]

Se reconoce mutuamente la capacidad legal necesaria para la celebración del presente contrato, y en tal sentido,

EXPONEN

Que los comparecientes, por convenir así a los intereses de todos, tienen el propósito de establecer una situación de sociedad entre ellos para la explotación de un negocio de [ACTIVIDAD], que se regirá por las estipulaciones del presente contrato, y en lo no previsto en ellas, a efectos puramente internos entre las partes, por las disposiciones contenidas en el Código de Comercio relativas a la sociedad colectiva y demás disposiciones legalmente aplicables.

ESTIPULACIONES

La sociedad actuará en el tráfico bajo la denominación de «[NOMBRE O DENOMINACIÓN]», tendrá duración indefinida y da comienzo a sus operaciones en el día de hoy. Los ejercicios sociales se computarán por años naturales, excepto el primero, que comenzará en esta fecha y terminará el día 31 de diciembre del presente año.

El objeto social será [OBJETO SOCIAL]

El domicilio de la sociedad estará situado en [DIRECCIÓN] calle [CALLE], número [NÚMERO]

El capital social se fija en [IMPORTE] euros, cuyo importe ha sido puesto en común e ingresado en la caja social en este acto por cada uno de los socios, en la cuantía siguiente:

Todos los socios reconocen la realidad y efectividad de las aportaciones realizadas, manifiestan su acuerdo en cuanto a su valoración y liberan plenamente a cada uno de los demás en cuanto al cumplimiento de esta obligación inicial.

Las cuotas que corresponden a los socios en la sociedad son las siguientes:

D [PORCENTAJE] % del total

D [PORCENTAJE] % del total

La alteración de estas cuotas exigirá el acuerdo unánime de los socios.

Se establece que la administración y representación de la sociedad se encomienda a los socios D [NOMBRE Y APELLIDOS] y D. [NOMBRE Y APELLIDOS], que actuarán con carácter solidario, y que aceptan el cargo en este mismo documento.

Los gestores representarán a la sociedad en todo lo referente al giro o tráfico de la misma, tanto judicial como extrajudicialmente. Sin embargo, para disponer, gravar o enajenar por cualquier título bienes inmuebles o establecimientos mercantiles, contraer obligaciones por un importe superior al treinta por cien del capital social, o afianzar obligaciones de terceras personas o de los propios socios, necesitarán el acuerdo unánime de todos éstos.

Ninguno de los socios podrá desempeñar, por su cuenta, actividades ajenas a la sociedad, sino en los términos establecidos en los artículos 136 y 137 del Código de Comercio.

Ningún socio podrá enajenar, gravar ni ceder su participación en la sociedad sin el consentimiento de todos los demás, dejando a salvo lo que se establece en este contrato para caso de muerte de alguno de ellos.

Los acuerdos, salvo los casos en que en este contrato se exige la unanimidad, se adoptarán mediante el voto favorable de [PORCENTAJE]. No obstante, será necesario el voto unánime favorable de todos los socios cuando se trate de acuerdos que impliquen la modificación del contenido de este contrato, la admisión de nuevos socios, la transmisión de la condición de socio, la destitución de todos o alguno de los administradores, la transformación y la fusión o escisión de la sociedad.

La participación en las ganancias y pérdidas de la sociedad se determinará en proporción a la cuota que cada socio posea. La cuantía de las ganancias a distribuir entre los socios se fijará, a propuesta de los gestores, dentro de los dos meses siguientes a la finalización de cada ejercicio social.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

La sociedad se disolverá por las causas establecidas en el Código de Comercio para las sociedades colectivas, y se procederá a su liquidación conforme a las reglas contenidas en el mismo. Se regirán asimismo por las normas del citado Código los supuestos de separación y exclusión de socios. En el caso de muerte de alguno de los socios, podrá pactarse la continuación de la sociedad con los herederos del fallecido, siempre que medie el acuerdo unánime de los demás. De no producirse este acuerdo, se procederá a la liquidación que hubiera correspondido al socio fallecido de haberse disuelto la sociedad en la fecha de su fallecimiento, y continuará la sociedad entre los restantes.

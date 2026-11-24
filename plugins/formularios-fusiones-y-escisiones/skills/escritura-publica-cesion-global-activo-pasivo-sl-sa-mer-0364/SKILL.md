---
name: escritura-publica-cesion-global-activo-pasivo-sl-sa-mer-0364
description: "Escritura pública de cesión global de activo y pasivo de una SL o SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de cesión global de activo y pasivo de una SL o SA

> Formulario **MER-0364** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de cesión global de activo y pasivo de una SL o SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de cesión global de activo y pasivo de una SL o SA” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:escritura-publica-cesion-global-activo-pasivo-sl-sa-mer-0364`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] MES (11 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] AÑO (8 veces)
- [ ] DÍA (8 veces)
- [ ] FECHA (5 veces)
- [ ] Nº (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] NOMBRE DEL DIARIO (4 veces)
- [ ] PÁGINA (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] COLEGIO
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NÚMERO
- [ ] OTRAS CONDICIONES

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

NÚMERO DE PROTOCOLO:

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS]. Notario del Ilustre Colegio de [COLEGIO]

COMPARECE/N

D/Dña. [NOMBRE Y APELLIDOS]

INTERVIENEN

[ELEGIR UNA OPCIÓN: Facultades derivadas del cargo de Administrador / Facultades derivadas de los acuerdos de la Junta]

EXPONEN

I.- Que mediante acuerdo adoptado el día [FECHA] de [MES] del año en curso, la Junta General de [ELEGIR: SL / SA]. acordó la cesión global de su activo y pasivo a favor del CESIONARIO, según consta en la certificación expedida por D/Dña. [NOMBRE Y APELLIDOS], y cuya firma reconozco y considero legítima. A petición de los comparecientes, procedo a unir dicha certificación, con sus documentos anexos, a la presente

II.- Que las cifras a las que ascienden el total del activo y del pasivo citados en el ordinal precedente son las descritas en el Anexo I que acompaña a la certificación aludida en el expositivo anterior.

Expuesto lo anterior, los comparecientes

OTORGAN

CONVOCATORIA

Que la mercantil [ELEGIR: SL / SA]. fue convocada por su Consejo de Administración mediante anuncios insertados en el diario [NOMBRE DEL DIARIO], del día [FECHA] de [MES] del año en curso, y en el Boletín Oficial del Registro Mercantil de [LOCALIDAD] del día [FECHA] de [MES], igualmente del año en curso, a fin de su reunión en Junta General [ELEGIR: ordinaria / extraordinaria] en fecha [DÍA] de [MES] de [AÑO] EL CEDENTE acredita dichos extremos mediante exhibición de los correspondientes ejemplares.

Elevación a público de los Acuerdos sociales

El compareciente, según interviene, eleva a público los acuerdos adoptados por la Junta General [ELEGIR: ordinaria / extraordinaria] de la mercantil [DENOMINACIÓN SOCIAL], [ELEGIR: SL / SA]. celebrada el pasado día [DÍA] de [MES] de [AÑO], tal y como constan en la certificación literal de la que me hace entrega, y a cuya solicitud procedo a unir a la presente, dándose así por reproducidos.

Dicha certificación fue expedida por el mismo compareciente, en su calidad de Secretario de tal Junta, con el Visto Bueno de su Presidente, cuyas firmas reconozco y considero legítimas, quedando acreditada la facultad certificante del compareciente.

Cesión global del activo y pasivo con plazo sin oposición

Publicación del acuerdo de cesión:

El citado acuerdo de cesión fue publicado en el Boletín Oficial del Registro Mercantil de fecha [DÍA] de [MES] de [AÑO], página [PÁGINA], y en el diario [NOMBRE DEL DIARIO], que es una de los de gran circulación en el lugar del domicilio social, el día [FECHA], página [PÁGINA], expresándose en ambos la identidad del CESIONARIO y el derecho de los acreedores de la sociedad cedente y de los acreedores del CESIONARIO a obtener el texto íntegro del texto de la cesión y a oponerse a la cesión.

Se me hace entrega de sendas copias de dichos anuncios, los cuales, a petición de D/Dña. [NOMBRE Y APELLIDOS]. procedo a unir a la matriz de la presente escritura.

Plazo: Transcurso del plazo sin oposición

Que ha transcurrido el plazo de 1 mes desde el día [DÍA] de [MES] de [AÑO], fecha del último de los anuncios citados, sin que ningún acreedor del CESIONARIO ni del CEDENTE haya ejercitado derecho de oposición contra el acuerdo de cesión.

Cesión global:

EL CEDENTE cede globalmente el activo y el pasivo de la sociedad al CESIONARIO, quien entregará a [ELEGIR: SL / SA] en pago de dicha cesión [IMPORTE] euros.

Cesión global del activo y pasivo con plazo con oposición

Publicación del acuerdo de cesión:

El citado acuerdo de cesión fue publicado en el Boletín Oficial del Registro Mercantil de fecha [DÍA] de [MES] de [AÑO], página [PÁGINA], y en el diario [NOMBRE DEL DIARIO], que es uno de los de gran circulación en el lugar del domicilio social, el día [FECHA], página [PÁGINA], expresándose en ambos la identidad del CESIONARIO y el derecho de los acreedores de la sociedad cedente y de los acreedores del CESIONARIO a obtener el texto íntegro del texto de la cesión y a oponerse a la cesión.

Se me hace entrega de sendas copias de dichos anuncios, los cuales, a petición de D/Dña. [NOMBRE Y APELLIDOS] procedo a unir a la matriz de la presente escritura.

Plazo: Transcurso del plazo con oposición

Que ha transcurrido el plazo de 1 mes desde el día [DÍA] de [MES] de [AÑO], fecha del último de los anuncios citados, sin que ningún acreedor del CESIONARIO ni del CEDENTE haya ejercitado derecho de oposición contra el acuerdo de cesión.

Cesión global:

EL CEDENTE cede globalmente el activo y el pasivo de la sociedad al CESIONARIO, en los términos del Proyecto de cesión global elaborado por el órgano de Administración que se incorpora como Anexo I.

Liquidación y extinción de la sociedad

Queda por lo tanto disuelta la sociedad, manifestándose por el compareciente:

Aprobación y publicación del balance final

Que el citado balance final fue aprobado por la Junta de socios, tal y como queda acreditado en la certificación unida a la presente, a la cual acompaña igualmente, como Anexo I, copia original del mismo.

Que el citado balance final ha sido publicado en el Boletín Oficial del Registro Mercantil el día [DÍA] de [MES] de [AÑO] y en el diario [NOMBRE DEL DIARIO], siendo este uno de los de mayor circulación en el lugar del domicilio social de [DENOMINACIÓN SOCIAL], [ELEGIR: SL / SA] como me acredita el compareciente mediante la exhibición de sendos ejemplares.

[ELEGIR UNA OPCIÓN: Plazo para impugnar el balance final / Sin reclamaciones / Con reclamaciones / — y además elegir: Satisfacción de los acreedores o aseguramiento de sus créditos / Satisfacción / Satisfacción de los acreedores / Aseguramiento / Aseguramiento de créditos]

Reparto del haber social entre los socios y relación de socios

Que, siendo la cuota de reparto de [IMPORTE] euros por [ELEGIR: participación / acción] social, se ha procedido al reparto entre los socios del haber social existente de conformidad con lo siguiente:

a) D/Dña.. [NOMBRE Y APELLIDOS] titular de [ELEGIR: participaciones / acciones] numeradas del [Nº] al [Nº], ambos inclusive, recibe [IMPORTE] euros por el total de sus [ELEGIR: participaciones / acciones].

b) D/Dña.. [NOMBRE Y APELLIDOS], titular de [ELEGIR: participaciones / acciones] numeradas del [Nº] al [Nº], ambos inclusive, recibe [IMPORTE] euros por el total de sus [ELEGIR: participaciones / acciones].

c) [OTRAS CONDICIONES]

Documentación

El compareciente D/Dña.. [NOMBRE Y APELLIDOS]. manifiesta su propósito de depositar en el Registro Mercantil los libros de comercio, la correspondencia, la documentación y los justificantes concernientes al tráfico de la mercantil [DENOMINACIÓN SOCIAL], [ELEGIR: SL / SA] siguientes:

Inscripción

Se solicita por D/Dña.. [NOMBRE Y APELLIDOS] en la representación que ostenta, la inscripción de la presente escritura en el Registro Mercantil, y en particular se solicita del Registrador Mercantil la práctica de cuantos asientos deriven de la presente y, en concreto, la cancelación de todos los asientos referentes a la sociedad.

Advertencia registral

Informo al compareciente que, para poder inscribir los actos formalizados en la presente escritura, se precisa que la sociedad haya realizado el pertinente depósito de las cuentas anuales en el Registro Mercantil (art. 378 Reglamento del Registro Mercantil).

[ELEGIR UNA OPCIÓN: Comunicación al registro mercantil / Presentación telemática / No telemática / Presentación no telemática]

Protección de datos personales

Advierto expresamente al compareciente que sus datos van a ser incorporados al fichero del Protocolo y documentación notarial y al fichero de Administración y organización, así como del hecho de que, en su caso, tales datos pueden ser cedidos a aquellas Administraciones públicas que según una norma con rango de ley tengan derecho a ello. Hechas las advertencias de sus derechos al respecto.

Otorgamiento y autorización

Se han hecho las reservas y advertencias legales, en especial advierto de la necesidad de la inscripción en el Registro Mercantil de los actos formalizados en esta escritura y en particular y a efectos fiscales he advertido a los comparecientes de la obligación de presentación de la documentación a liquidar dentro de plazo y de las obligaciones y responsabilidades tributarias que les incumben en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se derivarían de la inexactitud de sus declaraciones.

Les leo, por su elección, esta escritura, advertidos de su derecho a leerla por sí, del que no usan y, tras hacerles las oportunas explicaciones verbales para su cabal conocimiento, manifiestan quedar enterados, la aceptan, se ratifican y firman.

Yo, el Notario, Doy fe de que el consentimiento ha sido libremente prestado y de que el otorgamiento se adecua a la legalidad y a la voluntad debidamente informada de los otorgantes.

Queda extendida en un total de [Nº] folios de papel notarial, el primero con el número [NÚMERO]. y los demás con los números siguientes en orden correlativo.

Y de su contenido, DOY FE.

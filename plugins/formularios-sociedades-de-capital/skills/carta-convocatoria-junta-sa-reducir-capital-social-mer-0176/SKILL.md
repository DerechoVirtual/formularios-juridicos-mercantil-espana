---
name: carta-convocatoria-junta-sa-reducir-capital-social-mer-0176
description: "Carta de convocatoria de junta de SA para reducir el capital social. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Carta de convocatoria de junta de SA para reducir el capital social

> Formulario **MER-0176** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Carta de convocatoria de junta de SA para reducir el capital social» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Carta de convocatoria de junta de SA para reducir el capital social” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:carta-convocatoria-junta-sa-reducir-capital-social-mer-0176`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] PUNTO DEL ORDEN DEL DÍA (6 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] FECHA (3 veces)
- [ ] MES (3 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE ARTÍCULO (3 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] LUGAR DE CELEBRACIÓN
- [ ] NOMBRE Y APELLIDOS
- [ ] TELÉFONO

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

D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

Estimado señor,

Por la presente, le comunicamos la próxima celebración de la junta general de la sociedad [DENOMINACIÓN SOCIAL] SA, de la que usted es socio, y le convocamos de acuerdo con lo previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales.

La junta general de socios se celebrará en la [LUGAR DE CELEBRACIÓN], de la localidad de [LOCALIDAD], y tendrá lugar, en primera convocatoria, el día [FECHA] a las [Nº] horas y, en segunda convocatoria, el día [FECHA] a las [Nº] horas.

La junta convocada tendrá el siguiente

ORDEN DEL DIA

[OPCIONAL — incluir si procede]

1.- Reducir el capital social con la finalidad de devolver aportaciones. La necesidad de devolver aportaciones tiene su causa en la escisión de la sociedad, y adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1.- Reducir el capital social con la finalidad de amortizar acciones rescatables y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1.- Reducir el capital social con la finalidad de amortizar las acciones pertenecientes a accionistas morosos en el pago de desembolsos pendientes y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1.- Reducir el capital social con la finalidad de condonar los desembolsos pendientes, por el importe del valor nominal de las acciones pendientes de desembolso y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1.Reducir el capital social con la finalidad de incrementar las reservas y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

[OPCIONAL — incluir si procede]

1.- Reducir el capital social con la finalidad de restablecer el equilibrio entre el capital y el patrimonio neto de la sociedad disminuido por consecuencia de pérdidas y modificación del artículo correspondiente de los estatutos sociales.

2.- [PUNTO DEL ORDEN DEL DÍA]

.- Ruegos y preguntas.

.- Lectura y aprobación del acta de la junta o designación de interventores para su aprobación.

DERECHO DE ASISTENCIA

Podrán asistir a la Junta General todos los accionistas que, a título individual o en agrupación, sean titulares de, al menos, [Nº] acciones, inscritas en el correspondiente registro contable de anotaciones en cuenta con cinco días de antelación a la fecha de celebración de la Junta, de conformidad con lo previsto en el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales y en el artículo 179 de la Ley de Sociedades de Capital.

DERECHO DE REPRESENTACIÓN

Todo accionista que tenga derecho de asistencia podrá otorgar su representación a otra persona para asistir a la Junta General, cumpliendo los requisitos y formalidades exigidos por el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales y por la Ley.

La representación se hará constar en la tarjeta de asistencia o mediante carta, en todo caso, firmadas con firma autógrafa. El documento en el que conste la representación deberá contener o llevar anejo el Orden del Día, así como la solicitud de instrucciones para el ejercicio del voto y la indicación del sentido en que deberá votar el representante en el caso de que no se impartan instrucciones precisas. En caso de ausencia de instrucciones para el ejercicio del derecho de voto por parte del accionista que la confiera, se entenderá que éste vota a favor de las propuestas que formula el Consejo de Administración.

La representación también podrá conferirse por medios electrónicos de comunicación a distancia a través de la página web de la Sociedad, a partir del día [DÍA] de [MES] de [AÑO], y el documento electrónico que remita el accionista deberá de incorporar una firma electrónica reconocida o avanzada, de cualquiera de los prestadores de servicios de certificación referidos en el siguiente apartado sobre voto a distancia. La representación ejercida a través de medios electrónicos de comunicación a distancia, deberá de obrar en poder de la Sociedad, en su sede social, con al menos 24 horas de antelación a la hora prevista para la celebración de la Junta General en primera convocatoria.

VOTO A DISTANCIA

El accionista puede emitir su voto a distancia, cumpliendo los requisitos y formalidades exigidos por el artículo de los Estatutos Sociales y por la Ley. Para la emisión del voto por correo postal, los accionistas deberán cumplimentar y remitir a la Sociedad un formulario normalizado que facilite la Sociedad a estos efectos, que incluirá la información necesaria para acreditar la condición de accionista, debiendo la firma del accionista legitimarse notarialmente. Si se tratara de personas jurídicas, el formulario deberá ir acompañado por el correspondiente documento que acredite suficientemente la representación con que actúa el firmante.

El voto se podrá emitir por medios electrónicos de comunicación a distancia, a través de la página web de la Sociedad, a partir del día [DÍA] de [MES] de [AÑO], y el documento electrónico que remita el accionista deberá de incorporar una firma electrónica reconocida o avanzada, de cualquiera de los siguientes prestadores de servicios de certificación: Asimismo se podrá utilizar el Documento Nacional de Identidad electrónico (DNIe) emitido por la Dirección General de la Policía, del Ministerio del Interior español.

El voto a distancia deberá de obrar en poder de la Sociedad en su sede social, con al menos 24 horas de antelación a la hora prevista para la celebración de la Junta General en primera convocatoria. En caso contrario, el voto se tendrá por no emitido.

DERECHO DE INFORMACIÓN

A partir de la publicación de esta convocatoria y en cumplimiento de lo establecido en los artículos 286, 287, 296, 297.1.a), 300 y 528 de la Ley de Sociedades de Capital los accionistas podrán examinar en el domicilio social de la Sociedad, consultar en la página web de la Sociedad (www) y solicitar la entrega o envío gratuito (a través de la Oficina de Atención al Accionista, de 9.30 a 14.00 y de 16.30 a 19.00 horas, en días laborables, teléfono [TELÉFONO], y dirección de correo electrónico [CORREO ELECTRÓNICO]), de los siguientes documentos:

- En relación con el punto primero del Orden del Día: Texto íntegro de la propuesta de acuerdo e Informe de los Administradores a los efectos previstos en los artículos 286 y 297.1.a) de la Ley de Sociedades de Capital.

- En relación con el punto segundo del Orden del Día: Texto íntegro de la propuesta de acuerdo e Informe de los Administradores a los efectos previstos en el artículo 286 de la Ley de Sociedades de Capital.

- Formularios y condiciones para el ejercicio de los derechos de información, delegación y voto a distancia.

Hasta el séptimo día anterior previsto para la celebración de la Junta, los accionistas, mediante comunicación escrita, podrán solicitar de los administradores, informaciones o aclaraciones, o formular preguntas acerca de los asuntos comprendidos en el Orden del Día y sobre la información accesible al público que se hubiera facilitado por la Sociedad a la Comisión Nacional del Mercado de Valores desde la celebración de la última Junta General, de acuerdo con lo dispuesto en el artículo 527 de la Ley de Sociedades de Capital.

El solicitante deberá acreditar su identidad, en el caso de solicitud de información por escrito, mediante fotocopia de su Documento Nacional de Identidad o Pasaporte y, si se tratara de personas jurídicas, documento de acreditación suficiente de su representación. Adicionalmente, el solicitante deberá acreditar su condición de accionista o proporcionar los datos suficientes (número de acciones, entidad depositaria, etc.), para que puedan ser verificados por la Sociedad.

El derecho de información mediante medios electrónicos de comunicación a distancia podrá ejercerse a través de la página web de la Sociedad a partir del día [DÍA] de [MES] de [AÑO], y el documento electrónico que remita el accionista deberá de incorporar una firma electrónica reconocida o avanzada de cualquiera de los prestadores de servicios de certificación referidos en el apartado anterior sobre voto a distancia.

Asimismo y con el fin de dar cumplimiento al artículo 528.2 de la Ley de Sociedades de Capital, a partir de la publicación de esta convocatoria se habilita un Foro Electrónico de Accionistas en la página web de la Sociedad. Las normas de funcionamiento del Foro, así como el formulario que hay que cumplimentar para participar en el mismo, se encuentran disponibles en la página web de la Sociedad.

PRESENCIA DE NOTARIO

El Consejo de Administración ha acordado la presencia de Notario en la Junta, de conformidad con lo previsto en el artículo 203 de la Ley de Sociedades de Capital.

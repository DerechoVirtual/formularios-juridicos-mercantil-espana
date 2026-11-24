---
name: convocatoria-junta-transformar-sa-sl-mer-0361
description: "Convocatoria de junta para transformar una SA en SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convocatoria de junta para transformar una SA en SL

> Formulario **MER-0361** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convocatoria de junta para transformar una SA en SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convocatoria de junta para transformar una SA en SL” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:convocatoria-junta-transformar-sa-sl-mer-0361`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DÍA (8 veces)
- [ ] MES (8 veces)
- [ ] AÑO (7 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE ARTÍCULO (3 veces)
- [ ] FECHA
- [ ] LUGAR DE CELEBRACIÓN
- [ ] MEDIO DE PUBLICACIÓN
- [ ] NÚMERO

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

Por acuerdo del Consejo de Administración de [DENOMINACIÓN SOCIAL], en cumplimiento de lo dispuesto en los Estatutos Sociales y en el Reglamento de la Junta General de la Sociedad y de conformidad con la vigente Ley de Sociedades de Capital, se convoca a los señores accionistas a la Junta General Ordinaria que se celebrará a las [Nº] horas del día [DÍA] de [MES] de [AÑO], en [LUGAR DE CELEBRACIÓN] en primera convocatoria, y en el mismo lugar y hora el día [DÍA] de [MES] de [AÑO], en segunda convocatoria.

Los asuntos a tratar en la Junta serán los que se contienen en el siguiente,

Se celebra la presente Junta, cuya convocatoria fue realizada mediante anuncios publicados en el BORM número [NÚMERO] de fecha [FECHA] y en [MEDIO DE PUBLICACIÓN], con el siguiente contenido:

ORDEN DEL DÍA

- Lectura y aprobación del acta de la sesión anterior.

- Examen y aprobación, si procede, de las Cuentas Anuales (Balance, Cuenta de Pérdidas y Ganancias, Estado de cambios en el Patrimonio Neto y Memoria) de [DENOMINACIÓN SOCIAL], S.A., correspondientes al ejercicio económico comprendido entre el [DÍA] de [MES] de [AÑO] y el [DÍA] de [MES] de [AÑO], así como de la propuesta de aplicación de resultados (dicho balance ha sido aprobado por los Auditores).

- Renovación por tres años, como auditores externos de la Sociedad, a la entidad a tenor de lo establecido en el artículo 264 de la Ley de Sociedades de Capital, al haber transcurrido el plazo inicial para los que habían sido designados. Esta auditora [DENOMINACIÓN SOCIAL], en virtud de esta relección, verificará el ejercicio social que comienza el [DÍA] de [MES] de [AÑO] y finaliza el [DÍA] de [MES] del año

- Transformación de Sociedad Anónima a Sociedad Limitada, con aprobación, si procede, de los acuerdos complementarios precisos:

▪ Balance de la Sociedad, presentado para su transformación, con las modificaciones que, en su caso, resulten procedentes.

▪ Propuesta de nuevos Estatutos de la Sociedad.

▪ Informe de los Administradores que explica y justifica los aspectos jurídicos y económicos de la transformación.

▪ Canje de acciones por cuotas o participaciones sociales, determinación de los Socios y anulación de los títulos representativos.

▪ Adquisición por parte de la Sociedad de las acciones propias en poder de los Socios que ejerciten el derecho de separación.

▪ Cese del Órgano de Administración de la Sociedad Anónima

▪ Nombramiento del nuevo Órgano de Administración de la Sociedad de Responsabilidad Limitada; integrado por Presidente, Consejero Delegado, Vocales en número de tres y Secretario.

- Otorgamiento de facultades para la formalización, elevación a público y ejecución de los acuerdos que se adopten; con especial incidencia en los necesarios hasta conseguir la inscripción de la nueva Sociedad en el Registro Mercantil.

- Ruegos y preguntas

DERECHO DE ASISTENCIA

Podrán asistir a la Junta General todos los accionistas que, a título individual o en agrupación, sean titulares de [Nº], al menos, [Nº] acciones, inscritas en el correspondiente registro contable de anotaciones en cuenta con cinco días de antelación a la fecha de celebración de la Junta, de conformidad con lo previsto en el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales y en el artículo 179 de la Ley de Sociedades de Capital.

DERECHO DE REPRESENTACIÓN

Todo accionista que tenga derecho de asistencia podrá otorgar su representación a otra persona para asistir a la Junta General, cumpliendo los requisitos y formalidades exigidos por el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales y por la Ley.

La representación se hará constar en la tarjeta de asistencia o mediante carta firmadas. El documento en el que conste la representación deberá contener o llevar anejo el Orden del Día, así como la solicitud de instrucciones para el ejercicio del voto y la indicación del sentido en que deberá votar el representante en el caso de que no se impartan instrucciones precisas. En caso de ausencia de instrucciones para el ejercicio del derecho de voto por parte del accionista que la confiera, se entenderá que éste vota a favor de las propuestas que formula el Consejo de Administración.

La representación también podrá conferirse por medios electrónicos de comunicación a distancia a través de la página web de la Sociedad, a partir del día [DÍA] de [MES] de [AÑO], y el documento electrónico que remita el accionista deberá de incorporar una firma electrónica reconocida o avanzada, de cualquiera de los prestadores de servicios de certificación referidos en el siguiente apartado sobre voto a distancia. La representación ejercida a través de medios electrónicos de comunicación a distancia, deberá de obrar en poder de la Sociedad, en su sede social, con al menos 24 horas de antelación a la hora prevista para la celebración de la Junta General en primera convocatoria.

VOTO A DISTANCIA

El accionista puede emitir su voto a distancia, cumpliendo los requisitos y formalidades exigidos por el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales y por la Ley. Para la emisión del voto por correo postal, los accionistas deberán cumplimentar y remitir a la Sociedad un formulario normalizado que facilite la Sociedad a estos efectos, que incluirá la información necesaria para acreditar la condición de accionista, debiendo la firma del accionista legitimarse notarialmente. Si se tratara de personas jurídicas, el formulario deberá ir acompañado por el correspondiente documento que acredite suficientemente la representación con que actúa el firmante.

El voto se podrá emitir por medios electrónicos de comunicación a distancia, a través de la página web de la Sociedad, a partir del día [DÍA] de [MES] de [AÑO], y el documento electrónico que remita el accionista deberá de incorporar una firma electrónica reconocida o avanzada, de cualquiera de los siguientes prestadores de servicios de certificación: Asimismo se podrá utilizar el Documento Nacional de Identidad electrónico (DNIe) emitido por la Dirección General de la Policía, del Ministerio del Interior español.

El voto a distancia deberá de obrar en poder de la Sociedad en su sede social, con al menos 24 horas de antelación a la hora prevista para la celebración de la Junta General en primera convocatoria. En caso contrario, el voto se tendrá por no emitido.

DERECHO DE INFORMACIÓN

Cualquier accionista podrá obtener de la Sociedad, previa solicitud por escrito, para su examen, los documentos que se someten a la aprobación de la Junta, mediante su entrega o envío gratuito, en el propio domicilio Social o incluso por medios electrónicos. En concreto, de conformidad con el artículo 13 del RDLey 5/2023, los siguientes documentos:

- El informe de los Administradores, que explica y justifica los aspectos jurídicos y económicos de la transformación; e indica, asimismo, las consecuencias que tendrá para los Socios, así como su eventual impacto de género en los órganos de administración e incidencia en la responsabilidad social de la empresa.

- El balance de la Sociedad a transformar, cerrado dentro de los seis meses anteriores a la fecha prevista para la reunión, junto con un informe sobre las modificaciones patrimoniales.

- El informe del Auditor de Cuentas sobre el balance presentado.

- El proyecto de escritura social o estatutos de la sociedad que resulte de la transformación.

- La acreditación de encontrarse al corriente en el cumplimiento de las obligaciones tributarias y frente a la Seguridad Social, mediante la aportación de los correspondientes certificados, válidos y emitidos por el órgano competente.

PRESENCIA DE NOTARIO

El Consejo de Administración ha acordado la presencia de Notario en la Junta, de conformidad con lo previsto en el artículo 203 de la Ley de Sociedades de Capital.

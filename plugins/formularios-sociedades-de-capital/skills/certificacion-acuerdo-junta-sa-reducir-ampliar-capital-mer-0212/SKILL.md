---
name: certificacion-acuerdo-junta-sa-reducir-ampliar-capital-mer-0212
description: "Certificación del acuerdo de junta de una SA de reducir y ampliar capital a la vez (acordeón). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación del acuerdo de junta de una SA de reducir y ampliar capital a la vez (acordeón)

> Formulario **MER-0212** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de certificado, expedido por el Secretario con el Visto Bueno del Presidente, del acta de la Junta General Extraordinaria de una sociedad anónima que acordó reducir el capital social y aumentarlo simultáneamente (operación acordeón) y modificar los estatutos. Es el documento que se incorpora a la escritura pública de elevación a público de los acuerdos para su inscripción registral.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación del acuerdo de junta de una SA de reducir y ampliar capital a la vez (acordeón)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación del acuerdo de junta de una SA de reducir y ampliar capital a la vez (acordeón)” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdo-junta-sa-reducir-ampliar-capital-mer-0212`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (20 veces)
- [ ] IMPORTE (14 veces)
- [ ] FECHA (8 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] DENOMINACIÓN SOCIAL (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] HORA (4 veces)
- [ ] Nº DE ARTÍCULO (4 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] DIRECCIÓN DE LA PÁGINA WEB
- [ ] DNI
- [ ] DOCUMENTO DE REPRESENTACIÓN
- [ ] ENTIDAD DE CRÉDITO
- [ ] FINALIDAD
- [ ] IBAN
- [ ] IMPORTE DE LA PRIMA
- [ ] INCORPORAR EL BALANCE
- [ ] MAYORÍA O UNANIMIDAD
- [ ] NOMBRE DEL DIARIO
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTADO
- [ ] PLAZO DE EJECUCIÓN
- [ ] PROVINCIA

## Normas que cita el formulario

- art. 194 LSC
- art. 201 LSC

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

CERTIFICADO DE ACTA DE JUNTA GENERAL DE [DENOMINACIÓN SOCIAL], S.A.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de Secretario de la Junta General de [DENOMINACIÓN SOCIAL], S.A., reunida el pasado [DÍA] de [MES] de [AÑO] en [LOCALIDAD],

CERTIFICO

Que en [LOCALIDAD], siendo las [HORA] horas del día [FECHA], se reunió en el domicilio social de [DENOMINACIÓN SOCIAL], S.A., en [ELEGIR: primera / segunda] convocatoria, la Junta General Extraordinaria de Accionistas, previa convocatoria al efecto del [ELEGIR: Administrador único / administradores solidarios / administradores mancomunados / Consejo de Administración] de la citada mercantil, realizada mediante:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Con página web) Anuncio en la página web de la sociedad [DIRECCIÓN DE LA PÁGINA WEB] desde el [FECHA] hasta la fecha de la celebración de la junta el [FECHA], y alerta telemática a los correos electrónicos correspondientes a cada socio de los anuncios de convocatoria insertados en la web.

— (Sin página web) Anuncio publicado en el Boletín Oficial del Registro Mercantil número [Nº] correspondiente al día [FECHA], y en el diario [NOMBRE DEL DIARIO] de [PROVINCIA] del [FECHA].

— (Comunicación individual) El procedimiento de comunicación individual y escrita previsto en el artículo [Nº DE ARTÍCULO] de los Estatutos sociales, habiendo sido remitido el anuncio al último de los socios con fecha de [FECHA].

Que el texto íntegro de la convocatoria fue el siguiente:

"CONVOCATORIA DE JUNTA GENERAL DE [DENOMINACIÓN SOCIAL], S.A.

El órgano de administración de [DENOMINACIÓN SOCIAL], S.A. convoca Junta General de dicha sociedad a celebrar en el domicilio social, sito en la calle [CALLE] de [LOCALIDAD], el día [FECHA] a las [HORA] horas en primera convocatoria y en el mismo lugar el día [FECHA] a las [HORA] horas en segunda convocatoria, con el siguiente

ORDEN DEL DÍA:

1º) Reducir el capital social en la cantidad de [IMPORTE] euros para [ELEGIR: devolución de aportaciones a los socios / condonación de desembolsos pendientes / constitución o incremento de la reserva legal o de reservas voluntarias / restablecimiento del equilibrio entre el capital y el patrimonio de la sociedad disminuido por consecuencia de pérdidas], mediante la disminución del valor nominal de las acciones, que quedará fijado en [IMPORTE] euros por acción.

2º) Aumentar, de manera simultánea, el capital social de [DENOMINACIÓN SOCIAL], S.A. en [IMPORTE] euros mediante la emisión de [Nº] nuevas acciones de [IMPORTE] euros de valor nominal cada una de ellas, que se numerarán del [Nº] al [Nº], ambos inclusive.

3º) Adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.

4º) Ruegos y preguntas.

5º) Aprobación, en su caso, del acta de la Junta.

Se informa a los señores accionistas de su derecho a examinar en el domicilio social el texto íntegro de la operación propuesta y de su informe, los documentos que deban ser sometidos a aprobación por la Junta, y a solicitar su entrega o envío gratuito."

Que, según lo previsto en el art. [Nº DE ARTÍCULO] de los estatutos sociales de la compañía, actuó como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario yo, D./Dña. [NOMBRE Y APELLIDOS], designados por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

Que el Presidente, asistido por mí, el Secretario, procedió a elaborar la lista de asistentes que a continuación se relata, con detalle de las acciones que poseen y/o representaron cada uno de ellos:

Accionistas presentes:

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE] % del total del capital social con derecho a voto. (Repetir para cada accionista presente.)

Accionistas representados:

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], calle [CALLE], mayor de edad y con DNI [DNI], asiste en nombre y representación, según acredita mediante [DOCUMENTO DE REPRESENTACIÓN], de D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTADO], titular de [Nº] acciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE] % del total del capital social con derecho a voto. (Repetir para cada accionista representado.)

Que todas las citadas representaciones se acreditaron de forma legal, a satisfacción de la Junta.

Que, en consecuencia, asistieron, entre presentes y representados, un total de [Nº] accionistas, titulares de [Nº] acciones sociales, que representaron el [PORCENTAJE] % del capital social con derecho a voto.

Que todo el capital social de la compañía tiene derecho a voto.

Que, por lo tanto, por el Presidente se procedió a declarar válidamente constituida la Junta.

Que sobre las citadas manifestaciones del Presidente ningún asistente protestó ni presentó reserva alguna.

Que, por indicación del Presidente, yo, el Secretario, di lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en la misma, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por una mayoría de [MAYORÍA O UNANIMIDAD] se adoptaron los acuerdos cuyo contenido se transcribe a continuación:

ACUERDOS

PRIMERO.– Aprobación del balance y reducción del capital social

Se acuerda reducir el capital social conforme a los siguientes extremos:

A) Balance. Aprobar el balance que sirve de base a la presente operación, el cual ha sido verificado por los auditores de cuentas de la sociedad y que se incorpora como ANEXO I a la presente certificación.

B) Cifra de reducción. Reducir el capital en la suma de [IMPORTE] euros. Por lo tanto, el capital social quedará fijado en [IMPORTE] euros.

C) Finalidad de la reducción. La finalidad de la reducción del capital es [FINALIDAD].

D) Procedimiento. La reducción se efectúa mediante la disminución del valor nominal de todas las acciones que lo integran en [IMPORTE] euros por acción, que pasan a tener un valor nominal de [IMPORTE] euros cada una de ellas. Así, se amortiza la cantidad de [IMPORTE] euros por acción, circunstancia que se hace constar en los títulos acreditativos de las mismas mediante su estampillado. La presente operación afecta por igual a todos los accionistas.

E) Plazo de ejecución. La reducción del capital social se efectúa en [PLAZO DE EJECUCIÓN].

SEGUNDO.– Ampliación simultánea del capital social

Aumentar el capital social en la suma de [IMPORTE] euros, mediante la emisión y puesta en circulación de [Nº] nuevas acciones, de la misma serie de las hoy existentes, representadas por [ELEGIR: títulos nominativos / títulos al portador / anotaciones en cuenta], numeradas correlativamente del [Nº] al [Nº], ambos inclusive, por valor nominal de [IMPORTE] euros cada una de ellas. [En caso de que las nuevas acciones se emitan con prima de emisión, hacer constar su cuantía por cada acción que se emita: [IMPORTE DE LA PRIMA].]

Las nuevas acciones serán íntegramente desembolsadas en metálico en el momento de la suscripción.

Se reconoce a todos los socios el derecho a suscribir un número de las nuevas acciones proporcional al valor nominal de las que poseen, no obstante lo cual y ante la propia Junta se renuncia expresamente al ejercicio de tal derecho por parte de todos y cada uno de los asistentes, lo cual la Junta acepta, no procediéndose, por tanto, al establecimiento de las condiciones de ejercicio del mismo.

Todas las acciones representativas del aumento de capital son suscritas y desembolsadas en este mismo acto, en los siguientes términos:

D./Dña. [NOMBRE Y APELLIDOS] suscribe [Nº] nuevas acciones, nº [Nº] a [Nº], ambos inclusive, por su valor nominal total de [IMPORTE] euros, cuyo desembolso acredita mediante certificado bancario de la entidad [ENTIDAD DE CRÉDITO] donde consta el ingreso de las citadas cantidades en la cuenta [IBAN] de la que es titular la compañía. (Repetir para cada suscriptor.)

TERCERO.– Modificación de los estatutos

Se acuerda modificar el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales, que en lo sucesivo queda redactado de la siguiente forma:

"Artículo [Nº DE ARTÍCULO].– El capital de la sociedad es de [IMPORTE] euros y está representado por [Nº] acciones nominativas, de valor nominal [IMPORTE] euros cada una de ellas, numeradas correlativamente del 1 al [Nº], ambos inclusive. Todas las acciones son de una sola serie, confieren los mismos derechos y obligaciones y están totalmente desembolsadas en el 100% de su valor nominal."

Se faculta al [ELEGIR: Secretario del Consejo de Administración / Secretario de la Junta / administrador] para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando para ello las escrituras correspondientes, incluidas, en su caso, las de subsanación, aclaración o rectificación, así como para realizar cuantas operaciones fueren precisas para la plena eficacia de dichos acuerdos.

Abierto el turno de ruegos y preguntas, no se formula ninguna y, siendo las [HORA] horas del mismo día, se levanta la sesión por el Presidente, de la que se extiende la presente acta que, leída por todos los asistentes, se aprueba por unanimidad y es seguidamente firmada por todos ellos.

Que, tras todo ello, redactada y leída que fue el acta por mí, el Secretario, ésta fue aprobada por la Junta, por unanimidad de los asistentes, con el Visto Bueno del Presidente.

Que, no existiendo más asuntos que tratar, se levantó la sesión.

SECRETARIO | Vº Bº PRESIDENTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] | Firmado: D./Dña. [NOMBRE Y APELLIDOS]

ANEXO I: Balance verificado por auditor de cuentas

[INCORPORAR EL BALANCE]

NOTAS DE USO

Presidente y secretario (art. 191 del texto refundido de la Ley de Sociedades de Capital, en adelante LSC): la junta general será presidida por la persona que designen los estatutos; en su defecto, por el presidente del Consejo de Administración, y a falta de éste, por el accionista que elijan en cada caso los socios asistentes a la reunión. El presidente estará asistido por un secretario, designado también por los estatutos o por los accionistas asistentes a la junta.

Quórum (art. 194 LSC): la modificación estatutaria debe ser adoptada con el quórum reforzado previsto para las modificaciones estatutarias. Salvo previsión estatutaria que establezca otros superiores, en primera convocatoria se necesita la concurrencia de accionistas presentes o representados que posean al menos el 50% del capital suscrito con derecho a voto y, en segunda convocatoria, es suficiente la concurrencia del 25% de dicho capital.

Mayoría (art. 201 LSC): el acuerdo se adoptará por mayoría ordinaria de los votos de los accionistas presentes o representados, pero si concurren accionistas que representan menos del 50% del capital suscrito con derecho a voto, los acuerdos citados sólo pueden adoptarse válidamente con el voto favorable de los dos tercios del capital presente o representado en la junta. Esta mayoría puede ser elevada por los estatutos sociales.

Las certificaciones de acuerdos sociales deben ser expedidas por quien tenga facultad para certificar, con el Visto Bueno del Presidente, y sus firmas habrán de legitimarse notarialmente o constar en la escritura de elevación a público (arts. 108 y concordantes del Reglamento del Registro Mercantil).

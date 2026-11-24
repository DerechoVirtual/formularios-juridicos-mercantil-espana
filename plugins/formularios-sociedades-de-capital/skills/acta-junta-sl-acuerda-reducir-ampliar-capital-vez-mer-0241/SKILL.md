---
name: acta-junta-sl-acuerda-reducir-ampliar-capital-vez-mer-0241
description: "Acta de junta de una SL que acuerda reducir y ampliar capital a la vez (operación acordeón). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta de junta de una SL que acuerda reducir y ampliar capital a la vez (operación acordeón)

> Formulario **MER-0241** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de acta de Junta General Extraordinaria de carácter Universal de una Sociedad de Responsabilidad Limitada en el que se adopta el acuerdo de reducción del capital social mediante la disminución del valor nominal de las participaciones, y ampliación simultánea del mismo (llamado "Operación Acordeón") mediante la creación de nuevas participaciones.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de junta de una SL que acuerda reducir y ampliar capital a la vez (operación acordeón)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de junta de una SL que acuerda reducir y ampliar capital a la vez (operación acordeón)” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-junta-sl-acuerda-reducir-ampliar-capital-vez-mer-0241`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (20 veces)
- [ ] IMPORTE (16 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] DENOMINACIÓN SOCIAL (8 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] CLASE DE TÍTULOS
- [ ] DIRECCIÓN
- [ ] Nº DE ARTÍCULO
- [ ] Nº DE CUENTA (IBAN)
- [ ] PORCENTAJE
- [ ] ÓRGANO
- [ ] ÓRGANO O PERSONA

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

Modelo de acta de Junta General Extraordinaria de carácter Universal de una Sociedad de Responsabilidad Limitada en el que se adopta el acuerdo de reducción del capital social mediante la disminución del valor nominal de las participaciones, y ampliación simultánea del mismo (llamado "Operación Acordeón") mediante la creación de nuevas participaciones.


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

ACTA DE JUNTA GENERAL DE ‘[DENOMINACIÓN SOCIAL], S.L.’

En [LOCALIDAD], siendo las [Nº] horas del día [FECHA], se reúne en el domicilio social de ‘[DENOMINACIÓN SOCIAL], S.L.’ la Junta General de Socios, previa convocatoria al efecto del Consejo de Administración de la citada mercantil realizada mediante:

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Comunicación individual]

A continuación, se transcribe el texto íntegro de la convocatoria:

‘CONVOCATORIA DE JUNTA GENERAL DE ‘[DENOMINACIÓN SOCIAL], S.L.’

El órgano de administración de ‘[DENOMINACIÓN SOCIAL], S.L.’ convoca Junta General de dicha compañía a celebrar en el domicilio social de la compañía, sito en la [DIRECCIÓN] de [LOCALIDAD] el día [FECHA] a las [Nº] horas, con el siguiente

ORDEN DEL DÍA:

1º) Reducir el capital social en la cantidad de [IMPORTE] euros mediante la disminución del valor nominal de las participaciones, que quedará fijado en [IMPORTE] euros por participación.
2º) Aumentar, de manera simultánea, el capital social de ‘[DENOMINACIÓN SOCIAL], S.L.’ en [IMPORTE] euros mediante la creación de [Nº] nuevas participaciones de [IMPORTE] euros de valor nominal cada una de ellas, que se numerarán del [Nº] al [Nº], ambos inclusive.
3º) Adoptar cuantos acuerdos complementarios sean precisos, en concreto, la modificación de los estatutos sociales.
4º) Ruegos y preguntas.
5º) Aprobación, en su caso, del acta de la Junta.

Se informa a los señores socios de su derecho a solicitar los informes o aclaraciones que estimen precisos sobre los asuntos comprendidos en el orden del día, por escrito, cuando así lo soliciten con anterioridad a la reunión de la junta general, o verbalmente, durante dicha junta. Igualmente se pone en su conocimiento que el texto íntegro de la modificación propuesta está a disposición de los socios en el domicilio social.’

Actúa como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS], quien también lo es del Consejo de Administración, y como Secretario D./Dña. [NOMBRE Y APELLIDOS], igualmente Secretario de dicho órgano, designados ambos por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las participaciones que poseen y/o representan cada uno de ellos:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios presentes:

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones sociales numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE] % del total del capital social con derecho a voto.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
Socios representados:

D./Dña. [NOMBRE Y APELLIDOS], vecino/a de [LOCALIDAD], mayor de edad y con D.N.I. asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] participaciones numeradas del [Nº] al [Nº], ambos inclusive, que representan el % del total del capital social con derecho a voto.

Todas las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [Nº] participaciones, que representan el % del capital social con derecho a voto.

Todo el capital social de la compañía tiene derecho a voto.

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Junta.

Sobre las citadas manifestaciones del Presidente ningún asistente protesta ni presenta reserva alguna.

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por [ELEGIR: unanimidad / mayoría] se adoptan los acuerdos cuyo contenido se transcribe a continuación:

ACUERDOS

Primero.- Aprobación del balance y reducción del capital social

Se acuerda reducir el capital social conforme a los siguientes extremos:

A) Balance

Para el cálculo de la base de la presente operación se ha utilizado el balance aprobado por la Junta celebrada el pasado [FECHA] (dentro de los 6 meses inmediatamente anteriores al acuerdo de aumento de capital), balance que ha sido objeto de verificación por los auditores de cuentas de la sociedad [DENOMINACIÓN SOCIAL].

De dicho balance se desprende la carencia de reservas por parte de ‘[DENOMINACIÓN SOCIAL], S.L.’

Tanto el balance como su verificación se acompañan como Anexos I y II respectivamente.

B) Cifra de reducción.

Reducir el capital en la suma de [IMPORTE] euros. Por lo tanto, el capital social quedará fijado en [IMPORTE] euros.

C) Finalidad de la reducción.

La finalidad de la reducción del capital es la de proceder al restablecimiento del equilibrio entre el capital y el patrimonio de la sociedad disminuido por consecuencia de pérdidas [IMPORTE].

D) Procedimiento.

La reducción se efectúa mediante la disminución del valor nominal de todas las participaciones que lo integran en [IMPORTE] euros por participación, que pasan a tener un valor nominal de [IMPORTE] euros cada una de ellas. Así, se amortiza la cantidad de [IMPORTE] euros por participación. Del nuevo valor de las participaciones se toma oportuna nota en el Libro Registro de Socios de la entidad, que libra nuevos títulos de las citadas participaciones, en los que se deja constancia del nuevo valor nominal, quedando anulados los anteriores.

La presente operación afecta por igual a todos los socios.

E) Plazo de ejecución.

La reducción del capital social se efectúa en el presente acto.

Segundo.- Ampliación simultánea del capital social

Aumentar el capital social en la suma de [IMPORTE] euros, mediante la creación y puesta en circulación de [Nº] nuevas participaciones, de la misma serie de las hoy existentes, representadas por títulos [CLASE DE TÍTULOS], numerados correlativamente del [Nº] al [Nº], ambos inclusive, por valor nominal de [IMPORTE] euros cada una de ellas. Con una prima de emisión, por cada participación que se emite de [IMPORTE] euros

Las nuevas participaciones serán íntegramente desembolsadas en metálico en el momento de la suscripción.

Se reconoce a todos los socios el derecho a suscribir un número de las nuevas participaciones proporcional al valor nominal de las que poseen.

Así, todas las participaciones representativas del aumento de capital son suscritas y desembolsadas en este mismo acto por los socios en los siguientes términos:.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] suscribe [Nº] nuevas participaciones, nºs. a [Nº], ambos inclusive, por su valor nominal total de [IMPORTE] euros, cuyo desembolso acredita mediante certificado bancario de la entidad [DENOMINACIÓN SOCIAL] donde consta el ingreso de las citadas cantidades en la cuenta [Nº DE CUENTA (IBAN)] de la que es titular la compañía.

Tercero.- Modificación de los estatutos

Como consecuencia de las nuevas participaciones y de las primas de emisión que quedan totalmente suscritas y desembolsadas se acuerda modificar el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"Art .- El capital de la sociedad es de [IMPORTE] EUROS y está representado por [ÓRGANO O PERSONA] participaciones, de valor nominal [IMPORTE] EUROS cada una de ellas, numeradas correlativamente del 1 al [Nº], ambos inclusive. Todas las participaciones son de una sola serie, confieren los mismos derechos y obligaciones y están totalmente desembolsadas en el 100% de su valor nominal’.

Cuarto.- Se faculta al Secretario del Consejo de Administración para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando para ello las escrituras correspondientes, incluidas, en su caso, las de subsanación, aclaración o rectificación, así como para realizar cuantas operaciones fueren precisas para la plena eficacia de dichos acuerdos.

Quinto.- Abierto el turno de ruegos y preguntas, no se formula ninguna y siendo las [Nº] horas del mismo día, se levanta la sesión por el Presidente, de la que se extiende la presente acta que, leída por todos los asistentes, se aprueba por unanimidad y es seguidamente firmada por todos ellos.

Secretario

Vº Bº Presidente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

Asistentes

Firmado: D./Dña. [NOMBRE Y APELLIDOS]

ANEXO I: Balance verificado por auditor de cuentas

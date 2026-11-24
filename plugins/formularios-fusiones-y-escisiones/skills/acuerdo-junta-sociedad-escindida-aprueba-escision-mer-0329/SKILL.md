---
name: acuerdo-junta-sociedad-escindida-aprueba-escision-mer-0329
description: "Acuerdo de junta de la sociedad escindida que aprueba la escisión total o parcial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acuerdo de junta de la sociedad escindida que aprueba la escisión total o parcial

> Formulario **MER-0329** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

La escisión total o parcial habrá de ser acordada necesariamente por la junta de socios de las sociedad escindida, ajustándose estrictamente al proyecto común de escisión, con los requisitos y formalidades establecidos en el régimen de las sociedades que se escinden. Cualquier acuerdo de una sociedad que modifique el proyecto de escisión equivaldrá al rechazo de la propuesta. Este acuerdo deberá incluirse en el acta de la junta general o, en su caso, en la certificación que se expida para dejar constancia del mismo.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acuerdo de junta de la sociedad escindida que aprueba la escisión total o parcial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acuerdo de junta de la sociedad escindida que aprueba la escisión total o parcial” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:acuerdo-junta-sociedad-escindida-aprueba-escision-mer-0329`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (23 veces)
- [ ] NOMBRE Y APELLIDOS (21 veces)
- [ ] LOCALIDAD (18 veces)
- [ ] FECHA (13 veces)
- [ ] DENOMINACIÓN SOCIAL (8 veces)
- [ ] IMPORTE (7 veces)
- [ ] NOMBRE O DENOMINACIÓN (7 veces)
- [ ] PORCENTAJE (6 veces)
- [ ] CALLE (5 veces)
- [ ] NIF (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] Nº DE ACCIONES/PARTICIPACIONES (3 veces)
- [ ] Nº DE ARTÍCULO (3 veces)
- [ ] ÓRGANO (3 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº DE PARTICIPACIONES (2 veces)
- [ ] DATOS DE IDENTIFICACIÓN
- [ ] DNI/NIE
- [ ] LUGAR
- [ ] MEDIO DE PAGO
- [ ] Nº DE ANEXO

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

La escisión total o parcial habrá de ser acordada necesariamente por la junta de socios de las sociedad escindida, ajustándose estrictamente al proyecto común de escisión, con los requisitos y formalidades establecidos en el régimen de las sociedades que se escinden. Cualquier acuerdo de una sociedad que modifique el proyecto de escisión equivaldrá al rechazo de la propuesta. Este acuerdo deberá incluirse en el acta de la junta general o, en su caso, en la certificación que se expida para dejar constancia del mismo.


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

ACUERDO DE ESCISIÓN DE LA SOCIEDAD «[NOMBRE O DENOMINACIÓN]»

[OPCIONAL — incluir si procede]

Junta General Extraordinaria

En [LOCALIDAD], siendo las [Nº] horas del día [FECHA], se reunió [ELEGIR: en primera convocatoria / en segunda convocatoria], en el domicilio social de ‘[NOMBRE O DENOMINACIÓN]’ sito en [LOCALIDAD] calle [CALLE] de [LOCALIDAD] la Junta General Extraordinaria de socios, previa convocatoria al efecto del [ELEGIR: administrador único / administrador solidario / administrador mancomunado / Consejo de Administración] de la citada mercantil realizada mediante

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Comunicación individual]

Que el texto íntegro de la convocatoria fue el siguiente:

CONVOCATORIA

D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

Estimado señor,

Por la presente, le comunicamos la próxima celebración de la junta general de la sociedad [DENOMINACIÓN SOCIAL], de la que usted es socio, y le convocamos de acuerdo con lo previsto en el artículo [Nº DE ARTÍCULO] de los estatutos sociales.

La junta general de socios se celebrará en la calle [CALLE], número [NÚMERO], de la localidad de [LOCALIDAD], y tendrá lugar, en primera convocatoria, el día [FECHA] a las [Nº] horas y, en segunda convocatoria, el día [FECHA] a las [Nº] horas.

La junta convocada tendrá el siguiente

ORDEN DEL DÍA

I. Aprobación de la escisión [ELEGIR: parcial / total] de la sociedad « [DENOMINACIÓN SOCIAL] »

II. Aprobación del balance de escisión.

[OPCIONAL — incluir si procede]

Solo para escisión parcial

III. Reducción de Capital

. Nombramiento de administradores

. Elevación a Público

En su calidad de socio, y de conformidad con lo que dispone el artículo [Nº DE ARTÍCULO]
196
197
 del Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el texto refundido de la Ley de Sociedades de Capital, tiene derecho a solicitar por escrito, con anterioridad a la reunión de la junta general o verbalmente durante la misma, los informes o aclaraciones que estimen precisos acerca de los asuntos comprendidos en el orden del día.

Actúa como Presidente de la junta D./Dña. [NOMBRE Y APELLIDOS] y como Secretario D./Dña. [NOMBRE Y APELLIDOS], designados ambos por la Junta conforme a los estatutos sociales y por acuerdo unánime de los reunidos.

El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las [ELEGIR: acciones / participaciones] que poseen y/o representan cada uno de ellos:

Socios presentes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE] % del total del capital social con derecho a voto.

Socios representados:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], vecino de [LOCALIDAD], calle [CALLE], mayor de edad y con D.N.I [DNI/NIE] asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE] % del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [Nº DE PARTICIPACIONES], que representan el [PORCENTAJE] % del capital social.

No existen en la sociedad titulares de derechos especiales distintos de las [ELEGIR: acciones / participaciones]

Todo el capital social de la compañía tiene derecho a voto.

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Junta.

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por se adoptan los acuerdos cuyo contenido se transcribe a continuación

[OPCIONAL — incluir si procede]

Junta universal

En [LOCALIDAD], calle [CALLE] a [FECHA], siendo las [Nº] horas, se hallan reunidos en el domicilio social de ‘[NOMBRE O DENOMINACIÓN]’ la totalidad de sus socios, como consta en la lista de asistentes, que representan la totalidad del capital social, y acuerdan por unanimidad constituirse en Junta General Extraordinaria de carácter Universal, al amparo de lo previsto en el art. 178 de la vigente Ley de Sociedades de Capital y en el art. de los Estatutos Sociales para tratar y deliberar sobre el siguiente ORDEN DEL DÍA, que es unánimemente aceptado:

I. Aprobación de la escisión [ELEGIR: parcial / total] de la sociedad « [DENOMINACIÓN SOCIAL] »
II. Aprobación del balance de escisión.

[OPCIONAL — incluir si procede]

Solo para escisión parcial

III. Reducción de Capital

. Nombramiento de administradores

. Elevación a Público

De conformidad con lo establecido en el art.97.1.4ª del Reglamento del Registro Mercantil, y en prueba de aceptación de todos los asistentes El Presidente, asistido por el Secretario, procede a elaborar la lista de asistentes que a continuación se relata, con detalle de las [ELEGIR: acciones / participaciones] que poseen y/o representan cada uno de ellos:

Socios presentes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE] % del total del capital social con derecho a voto.

Socios representados:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], vecino de [LOCALIDAD], calle [CALLE], mayor de edad y con D./Dña. [NOMBRE Y APELLIDOS] asiste en nombre y representación, según acredita mediante [ÓRGANO], de D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] numeradas del [Nº] al [Nº], ambos inclusive, que representan el [PORCENTAJE] % del total del capital social con derecho a voto.

Las citadas representaciones se acreditan de forma legal, a satisfacción de la Junta.

No existen en la sociedad titulares de derechos especiales distintos de las [ELEGIR: acciones / participaciones].

En consecuencia, asisten, entre presentes y representados, un total de [Nº] socios, titulares de [Nº DE PARTICIPACIONES], que representan el [PORCENTAJE] % del capital social.

Todo el capital social de la compañía tiene derecho a voto.

Por lo tanto, por el Presidente se procede a declarar válidamente constituida la Junta.

Por indicación del Presidente, el Secretario da lectura al ORDEN DEL DÍA establecido en la convocatoria, pasándose a continuación al estudio y deliberación de los asuntos contenidos en el mismo, tras lo cual, no deseando los asistentes iniciar debate alguno sobre los mencionados puntos ni solicitar constancia en acta de ninguna intervención u oposición, por se adoptan los acuerdos cuyo contenido se transcribe a continuación

ACUERDOS ADOPTADOS

Primero. Escisión

Se acuerda por el proyecto de escisión [ELEGIR: parcial / total] suscrito por los administradores de la sociedad escindida «[DENOMINACIÓN SOCIAL]» y de [ELEGIR: la sociedad beneficiaria / las sociedades beneficiarias] «[NOMBRE O DENOMINACIÓN]», de fecha [FECHA], insertado en la página web de la sociedad el día [FECHA] y publicado este hecho en el BORME el día [FECHA]

Se incorpora un ejemplar del proyecto a esta acta como anexo [Nº DE ANEXO]

[ELEGIR UNA OPCIÓN: Parcial / Total]

Igualmente, se aceptan las valoraciones atribuidas al patrimonio de las sociedades participantes en la escisión, efectuadas por los auditores:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] mayor de edad, de estado civil [ESTADO CIVIL], con DNI/NIF [NIF], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD]

Las circunstancias y condiciones del proyecto de escisión son:

1) Datos identificativos de las sociedades participantes en la escisión.

Sociedad escindida. «[NOMBRE O DENOMINACIÓN]», NIF [NIF], con domicilio social en [LOCALIDAD], constituida mediante escritura pública autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], con el número [NÚMERO] de su protocolo, e inscrita en el Registro Mercantil de [LOCALIDAD],

Sociedad beneficiaria. «[NOMBRE O DENOMINACIÓN]», NIF [NIF], con domicilio social en [LOCALIDAD], constituida mediante escritura pública autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], con el número [NÚMERO] de su protocolo, e inscrita en el Registro Mercantil de [LOCALIDAD],

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[OPCIONAL — incluir si procede]

Para el caso de escisión total

Sociedad beneficiaria. «[NOMBRE O DENOMINACIÓN]», NIF [NIF], con domicilio social en [LOCALIDAD], constituida mediante escritura pública autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], con el número [NÚMERO] de su protocolo, e inscrita en el Registro Mercantil de [LOCALIDAD],

2) Tipo de canje.

[OPCIONAL — incluir si procede]

Escisión total

La sociedad escindida se extingue como consecuencia de la escisión

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

La sociedad «[DENOMINACIÓN SOCIAL]» beneficiaria procederá a ampliar su capital en la cuantía de [IMPORTE] euros, mediante la creación de [Nº DE ACCIONES/PARTICIPACIONES] nuevas [ELEGIR: acciones / participaciones] con un valor nominal de [IMPORTE] euros cada una, números [Nº] al [Nº], ambos inclusive.

Las nuevas [ELEGIR: acciones / participaciones] de la sociedad beneficiaria se entregan a los socios de la sociedad escindida, en la proporción de [Nº DE ACCIONES/PARTICIPACIONES] de la sociedad beneficiaria «[DENOMINACIÓN SOCIAL]» por cada [Nº DE ACCIONES/PARTICIPACIONES] de [ELEGIR: acciones / participaciones] de la sociedad escindida «[DENOMINACIÓN SOCIAL]».

Igualmente, los socios de [DENOMINACIÓN SOCIAL] reciben una compensación dineraria de [IMPORTE] euros por cada [ELEGIR: acción / participación] asignada. La compensación será pagada [MEDIO DE PAGO]

3) Procedimiento de canje.

El canje se efectuará en el plazo de [Nº] días desde la fecha de celebración de la junta general que apruebe la escisión mediante [ÓRGANO]

4) Elementos patrimoniales atribuidos.

Los elementos patrimoniales de la sociedad escindida que serán atribuidos a [ELEGIR: la sociedad beneficiaria / las sociedades beneficiarias], constan en el inventario detallado que se acompaña como anexo número [NÚMERO].

5) Participación en las ganancias sociales.

Las [ELEGIR: acciones / participaciones] creadas como consecuencia de la escisión darán derecho a participar en los beneficios sociales de la sociedad beneficiaria a partir del día [FECHA], y en las mismas condiciones que el resto de las [ELEGIR: acciones / participaciones] sociedad/es beneficiaria/s.

6) Efectos contables de la escisión.

[ELEGIR UNA OPCIÓN: Parcial / Total]

7) Acreditación del cumplimiento de las obligaciones fiscales y frente a la Seguridad Social.

8) Derechos especiales derivados de la escisión.

No se otorgan derechos especiales de ningún tipo, así como tampoco se atribuyen ventajas de ninguna clase ni a los administradores sociales de las sociedades que participan en la escisión, ni al experto independiente que ha redactado el informe de escisión.

9) Fecha de las cuentas de las sociedades que participan en la escisión.

Las cuentas de las sociedades que participan en la escisión utilizadas para establecer las condiciones en que se realiza la operación han sido cerradas a fecha [FECHA]

10) Régimen fiscal de la escisión.

La presente escisión se somete al régimen fiscal especial que para estas operaciones regula la Ley 27/2014, de 27 de noviembre del Impuesto sobre sociedades.

[OPCIONAL — incluir si procede]

Escisión parcial

10) Administración de la sociedad.

[ELEGIR UNA OPCIÓN: Con nombramiento / Sin Modificación]

Segundo. Balance de Escisión

[ELEGIR UNA OPCIÓN: Balance ad hoc / Último Balance del Ejercicio]

[OPCIONAL — incluir si procede]

Escisión parcial

Tercero. Reducción del Capital Social

Se apruebareducir el capital social en el importe de [IMPORTE] euros, mediante la reducción del valor nominal de las [ELEGIR: acciones / participaciones], que pasará de ser de [IMPORTE] euros a [IMPORTE] euros cada una. El capital social después de la reducción es de [IMPORTE] euros.

Se da nueva redacción al artículo [Nº DE ARTÍCULO] de los estatutos, relativo al capital social:

Cuarto. Administradores

Se aprueba por [ELEGIR: unanimidad / mayoría] nombrar como nuevos administradores de la sociedad escindida, por el plazo estatutario de [Nº] años, a:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], con DNI/NIF [NIF], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS] presentes en la junta, aceptan el cargo para el cual han sido nombrados prometen cumplirlo bien y fielmente y manifiestan no estar incursos en causa alguna de incapacidad, prohibición o incompatibilidad

. Elevación a Público

Se acuerda por unanimidad facultar al administrador de la sociedad D./Dña. [NOMBRE Y APELLIDOS] para que pueda llevar a cabo la elevación a público de los acuerdos y realizar las gestiones precisas hasta su inscripción en el Registro Mercantil, y para subsanar, corregir o aclarar los documentos que otorgaren a los efectos referidos.

Particularmente, esta persona procederá a la publicación del acuerdo de escisión o, en su caso, a la publicidad sustitutiva

Acta

Finalizado el tratamiento de los puntos del orden del día de carácter sustantivo, se confecciona el acta que, una vez leída, es aprobada por unanimidad, y firmada por el secretario de la junta con el visto bueno del presidente de la junta

Tras lo cual, se levanta la sesión a las [Nº] horas del día y en el lugar que figuran en el encabezamiento.

Secretario D./Dña. [NOMBRE Y APELLIDOS], [DATOS DE IDENTIFICACIÓN]

VºBº Presidente D./Dña. [NOMBRE Y APELLIDOS],

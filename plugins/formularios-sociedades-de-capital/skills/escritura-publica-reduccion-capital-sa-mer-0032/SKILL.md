---
name: escritura-publica-reduccion-capital-sa-mer-0032
description: "Escritura pública de reducción del capital de una SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de reducción del capital de una SA

> Formulario **MER-0032** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura mediante la cual se eleva a público el acuerdo de Junta General de Socios de una Sociedad Anónima sobre la reducción de capital mediante la disminución del valor nominal de las acciones, su amortización o su agrupación, con la finalidad de restablecer el equilibrio entre el capital y el patrimonio neto de la sociedad disminuido por consecuencia de pérdidas, la constitución o el incremento de la reserva legal o de las reservas voluntarias o la devolución del valor de las aportaciones. Incluye también el acuerdo de modificación de los estatutos sociales en lo que afecte a esa reducción de capital. (Art. 317 TRLSC)

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de reducción del capital de una SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de reducción del capital de una SA” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-publica-reduccion-capital-sa-mer-0032`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (7 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] COLEGIO
- [ ] CÓDIGO CNAE
- [ ] DATOS REGISTRALES
- [ ] DESCRIBIR
- [ ] DOMICILIO
- [ ] ESTADO CIVIL
- [ ] LUGAR
- [ ] NIF
- [ ] Nº
- [ ] Nº DE SERIE
- [ ] OBJETO SOCIAL
- [ ] PLAZO
- [ ] PROFESIÓN

## Normas que cita el formulario

- art. 20 Ley 14/2013
- art. 4 Ley 10/2010

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

Modelo de escritura mediante la cual se eleva a público el acuerdo de Junta General de Socios de una Sociedad Anónima sobre la reducción de capital mediante la disminución del valor nominal de las acciones, su amortización o su agrupación, con la finalidad de restablecer el equilibrio entre el capital y el patrimonio neto de la sociedad disminuido por consecuencia de pérdidas, la constitución o el incremento de la reserva legal o de las reservas voluntarias o la devolución del valor de las aportaciones. Incluye también el acuerdo de modificación de los estatutos sociales en lo que afecte a esa reducción de capital. (Art. 317 TRLSC)


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

En [LUGAR], a [FECHA].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO]

COMPARECEN

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD].

Con [ELEGIR: DNI / pasaporte / permiso de residencia]

INTERVIENEN

Los señores comparecientes intervienen en su calidad de [ELEGIR: Administrador único / Administrador solidario / Administradores mancomunados / Consejero / Secretario del Consejo de Administración] de la citada empresa, domiciliada en [DOMICILIO], [DATOS REGISTRALES]; NIF [NIF] con el siguiente objeto social [OBJETO SOCIAL]. De conformidad con el art.20 de la Ley 14/2013, de 27 de septiembre, hacen constar los comparecientes que la Clasificación Nacional de Actividades Económicas (CNAE) que le corresponde es [CÓDIGO CNAE] cargo para el que fueron nombrados, por plazo de [PLAZO] por acuerdo de la Junta General de [FECHA], elevado a público en escritura autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS] ", el [FECHA], número [NÚMERO] de su Protocolo, la cual obra inscrita en el Registro Mercantil.

Lo expuesto resulta de las escrituras citadas, cuyas copias autorizadas tengo a la vista sin que en lo omitido por innecesario haya nada que limite, condicione, contradiga o amplíe lo inserto, asegurando el compareciente la subsistencia de su representación, así como no haber variado la capacidad de la entidad representada, y no haberse modificado el objeto social.

Asimismo hago constar que a los efectos del art.4 de la Ley 10/2010, de 28 de abril, de prevención del blanqueo de capitales y de la financiación del terrorismo, el compareciente, manifiesta que los titulares reales del capital social de la persona jurídica por él representada, son:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] quien ostenta más de veinticinco por ciento del capital social del capital social de la entidad en la presente escritura representada.

Les identifico por su citado [ELEGIR: DNI / pasaporte / Permiso de residencia] número [NÚMERO]. Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para otorgar la presente escritura elevación a público de los acuerdos sociales de reducción del capital de ', S.A.' y correspondiente modificación de los estatutos de la citada mercantil

EXPONEN

Primero.- Que los mentados Sres. celebraron el pasado día [FECHA] Junta universal de socios de la citada compañía ‘[DENOMINACIÓN SOCIAL], S.A.’, en la cual adoptaron, por unanimidad, el acuerdo de reducir el capital social de la citada sociedad.

Segundo.- Que, a tales efectos, y debido al acuerdo de reducción del capital de la Sociedad indicado anteriormente, los socios han convenido igualmente modificar el artículo [Nº DE ARTÍCULO] de sus Estatutos, referente a la cifra de capital social y a las acciones que lo constituyen.

Tercero.- Que los anteriores acuerdos constan en la certificación que me entregan, emitida por D./Dña. [NOMBRE Y APELLIDOS], secretario de dicha Junta, y con el visto bueno de D./Dña. [NOMBRE Y APELLIDOS] Presidente de la misma, quienes fueron elegidos para tales cargos por voto unánime de los socios, cuyas firmas legítimo, procediendo a la unión de dicha certificación a la matriz de la presente escritura formando parte integrante de la misma a cuyo fin

OTORGAN

Primero.- Elevación a público

El compareciente, conforme interviene, eleva a público los acuerdos adoptados por la Junta General de la sociedad [DENOMINACIÓN SOCIAL] S. A.", en su reunión de [FECHA], los cuales obran en la certificación que exhibe, dándose aquí por reproducidos.

Segundo.- Reducción de capital social

I. Reducción del Capital Social

Queda REDUCIDO EL CAPITAL SOCIAL de la entidad en la cifra de [IMPORTE] euros, mediante el procedimiento de [ELEGIR: disminución del valor nominal de las acciones que lo integran / amortización de acciones / agrupación y canje de acciones].

II. Publicaciones.

[ELEGIR UNA OPCIÓN: Con página web / Sin página web]

III. Acreedores.

[ELEGIR UNA OPCIÓN: Sin derecho de oposición / Con derecho de oposición no ejercitado / Con derecho de oposición sí ejercitado]

[OPCIONAL — incluir si procede]

(Cuando la reducción se realiza para devolver aportaciones a los socios)

IV. Pago a los socios:

El compareciente deja constancia de que con anterioridad a este acto se ha reembolsado a los accionistas afectados las cantidades correspondientes salvo la suma de [IMPORTE] euros, correspondiente a socios que no han comparecido Dicha cantidad ha sido consignada en depósito, a disposición de sus legítimos dueños.

[OPCIONAL — incluir si procede]

(Cuando la reducción se realiza para reducir pérdidas, o constituir o incrementar la reserva legal o voluntaria)

IV. Balance y certificación de Auditoría:

El compareciente entrega, para su unión a la presente, como hago, los siguientes documentos:

1. Balance cerrado a [FECHA], y aprobado por la Junta, que ha servido de base para el aumento de capital objeto de la presente reducción.
2. Certificado del auditor de cuentas de la sociedad D./Dña. [NOMBRE Y APELLIDOS] de fecha [FECHA].

Tercero.- Modificación de Estatutos

Debido a la reducción del capital social, los otorgantes han acordado la modificación del artículo [Nº DE ARTÍCULO] de los Estatutos de la Sociedad, el cual quedará redactado de la siguiente manera:

‘Artículo.- Capital social

El capital social será de [IMPORTE] euros, dividido en [Nº] acciones de [IMPORTE] euros de valor nominal cada una de ellas, numeradas de manera correlativa con los números 1 a

Dicho capital se halla totalmente suscrito y desembolsado mediante aportaciones realizadas por los socios a título de propiedad’.

Cuarto.- Solicitud de inscripción en el Registro Mercantil de [LOCALIDAD]

Los otorgantes solicitan al señor Registrador Mercantil de [LOCALIDAD] la inscripción de la presente escritura y la correspondiente modificación de los estatutos de la sociedad en la hoja registral correspondiente a la citada mercantil.

ADVERTENCIAS LEGALES, OTORGAMIENTO Y AUTORIZACIÓN NOTARIAL

Hice las reservas y advertencias legales, especialmente las prevenidas en la legislación fiscal, y las referentes a la obligación de presentar esta escritura en el Registro Mercantil.

Leo a los comparecientes, tras advertirles del derecho que tienen a hacerlo por sí, al que renuncian, la presente escritura, prestan su consentimiento y firman conmigo.

De todo lo consignado en este instrumento público, extendido sobre [DESCRIBIR] folios de papel de uso exclusivo notarial, serie y números, [Nº DE SERIE] yo, el Notario, doy fe.

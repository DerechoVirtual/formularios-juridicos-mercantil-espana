---
name: acta-notarial-junta-universal-sl-mer-0023
description: "Acta notarial de una junta universal de SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acta notarial de una junta universal de SL

> Formulario **MER-0023** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Los administradores podrán requerir la presencia de notario para que levante acta de la junta general y estarán obligados a hacerlo siempre que, con cinco días de antelación al previsto para la celebración de la junta, lo soliciten socios que representen, al menos, el cinco por ciento en la sociedad de responsabilidad limitada. En este caso, los acuerdos sólo serán eficaces si constan en acta notarial.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta notarial de una junta universal de SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta notarial de una junta universal de SL” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-notarial-junta-universal-sl-mer-0023`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (15 veces)
- [ ] FECHA (9 veces)
- [ ] Nº (9 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] HORA (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] CÓDIGO CNAE
- [ ] DATOS REGISTRALES
- [ ] DESCRIBIR
- [ ] DIRECCIÓN
- [ ] DNI/NIE
- [ ] DÍA
- [ ] INSCRIPCIÓN
- [ ] LUGAR
- [ ] MES
- [ ] NACIONALIDAD
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº DE FOLIOS
- [ ] OBJETO DE LA ESCRITURA
- [ ] OTROS DATOS
- [ ] PROFESIÓN
- [ ] SERIE

## Normas que cita el formulario

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

Los administradores podrán requerir la presencia de notario para que levante acta de la junta general y estarán obligados a hacerlo siempre que, con cinco días de antelación al previsto para la celebración de la junta, lo soliciten socios que representen, al menos, el cinco por ciento en la sociedad de responsabilidad limitada. En este caso, los acuerdos sólo serán eficaces si constan en acta notarial.


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

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domiciliado en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO],

En nombre y representación de la mercantil, S.L.’ domiciliada en [DOMICILIO], con la Clasificación Nacional de Actividades Económicas (CNAE) [CÓDIGO CNAE]. Constituida por tiempo indefinido mediante escritura pública autorizada por D./Dña. [NOMBRE Y APELLIDOS] Notario de [LOCALIDAD] en fecha [FECHA], con el número [NÚMERO] de los de su protocolo. La presente mercantil se halla inscrita en el Registro Mercantil de [LOCALIDAD], al [DATOS REGISTRALES]; su NIF es [NIF].

Para el presente acto se encuentra facultado en virtud de su cargo de Secretario del Consejo de Administración, que asegura vigente, para el que fue designado por un plazo de [Nº] años por acuerdo de la Junta General de socios de la citada sociedad celebrada en fecha [FECHA], cuyos acuerdos fueron elevados a públicos en escritura otorgada ante D./Dña. [NOMBRE Y APELLIDOS] Notario de [LOCALIDAD], el día [FECHA], escritura que cuenta con el número [NÚMERO] de las de su protocolo y se halla inscrita en el Registro Mercantil de [LOCALIDAD], en el Tomo y Folios, inscripción [INSCRIPCIÓN]. El compareciente se halla especialmente facultado para el presente acto por acuerdo de la Junta General de ‘[DENOMINACIÓN SOCIAL], S.L.’, certificación de la cual, con las firmas que la autorizan y que considero legítimas, incorporo a esta escritura, y acompañará a todas sus copias fotocopia auténtica de la misma.

Asimismo, hago constar que a los efectos del art. 4 de la Ley 10/2010, de 28 de abril, de prevención del blanqueo de capitales y de la financiación del terrorismo, el compareciente, manifiesta que la persona jurídica representada ha identificado los titulares reales de su capital social por acta notarial de manifestaciones autorizada por el Notario de

D./Dña. [NOMBRE Y APELLIDOS] el día [FECHA], con el número de protocolo.

Le identifico por su [ELEGIR: DNI / pasaporte / permiso de residencia] antes reseñado, y tiene, a mi juicio, según interviene, la capacidad legal necesaria para celebrar la presente escritura de [OBJETO DE LA ESCRITURA], a cuyo fin

EXPONEN

Primero.- Antecedentes

a) Proyecto de Junta Universal

Que los socios de la entidad se proponen celebrar Junta General Universal en [DIRECCIÓN], calle", a las [HORA] del día [FECHA].

b) Previsiones estatutarias

Que me exhibe los Estatutos de la entidad, incorporados a la escritura de constitución, a fin de que transcriba, como hago, los particulares siguientes: [OTROS DATOS].

c) Manifestaciones

Manifiestan los comparecientes:

Que, en la actualidad, el Presidente y Secretario del Consejo de Administración de la entidad son D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], con DNI [DNI/NIE] y que no existen Vicepresidente o Vicesecretario del Consejo, extremos todos ellos que acredita con la escritura ya mencionada en la intervención.

Segundo.- Requerimiento

Expuesto lo cual, los comparecientes, conforme intervienen,

Me requieren

A mí, el Notario, para que personándome en el lugar y hora indicados constate el acuerdo de celebrar la prevista Junta Universal y, en su caso, levante acta de la reunión, todo ello conforme a lo establecido por el art. 178 y 203 de la Ley de Sociedades de Capital y art. 101 s. y concordantes, del Reglamento del Registro Mercantil.

Acepto el requerimiento que practicaré mediante diligencia a continuación de la presente.

Otorgamiento

Leo a los comparecientes, tras advertirles del derecho que tienen a hacerlo por sí, al que renuncian el presente acta, prestan su consentimiento y firman conmigo.

Autorización

Y yo, el Notario, doy fe del presente documento extendido en [Nº DE FOLIOS] de folios de papel notarial del Timbre del Estado, serie y números [Nº].

Diligencia de presencia

A) JUNTA UNIVERSAL

a) Asistentes

A las [HORA] del [FECHA], me constituyo yo, el Notario, en el domicilio fijado en el requerimiento, donde constato la presencia de las personas que se mencionarán, quienes, tras las advertencias pertinentes sobre mi condición de Notario y el carácter de mi intervención, consienten expresamente la práctica de la diligencia y efectúan las siguientes manifestaciones:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Quien dice llamarse [NOMBRE Y APELLIDOS], el cual:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Manifiesta representar [Nº] participaciones sociales de las que integran el capital social de la entidad, y asistir en su carácter de socio titular de las citadas participaciones sociales.

Manifiesta representar [Nº] participaciones sociales de las que integran el capital social de la entidad, y asistir en su carácter de representante del socio, titular de las citadas participaciones sociales.

- Se identifica mediante la exhibición de su Documento Nacional de Identidad, número [NÚMERO].

- Exhibe los siguientes documentos, fotocopia de los cuales, concordantes con sus originales, incorporo a la presente.

[OPCIONAL — incluir si procede]

(Libro registro de socios)

Certificación del Libro Registro de socios, de [FECHA], y suscrita por D./Dña. [NOMBRE Y APELLIDOS].

[OPCIONAL — incluir si procede]

(Escritura de constitución)

Escritura pública autorizada por el Notario D./Dña. [NOMBRE DEL NOTARIO]; de [LOCALIDAD] el [DÍA] de [MES] de [AÑO], acreditativa de la propiedad de las participaciones sociales reseñadas, y en las que no figura nota alguna de transmisión posterior.

D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], quienes manifiestan ser administradores de la Sociedad, acreditando sus cargos, que declaran subsistentes, e identificándose, mediante la exhibición de las copias autorizadas de las escrituras y de los Documentos Nacionales de Identidad, ya reseñados en el requerimiento.

Tales Administradores, en uso de su facultad certificante, aseveran que las manifestaciones efectuadas por los asistentes se corresponden con los asientos extendidos en el Libro Registro de Socios de la entidad los cuales no han sufrido variación respecto a los reseñados en el requerimiento y que, por tanto, está presente la totalidad del capital social de la entidad.

Tras examinar los que desean hacerlo la documentación reseñada, manifiestan todos los asistentes que está presente o representada la totalidad del capital social de la entidad, sin que ninguno desee hacer manifestaciones u oposiciones al respecto.

b) Acuerdo de celebrar Junta Universal

D./Dña. [NOMBRE Y APELLIDOS] propone a los presentes la celebración de junta general universal de la entidad con el siguiente ORDEN DEL DÍA:

Constato yo, el Notario, como todos y cada uno de los asistentes prestan su expresa conformidad a la propuesta, como consecuencia de lo cual se celebra la Junta General de socios de la entidad [DENOMINACIÓN SOCIAL] SL

B) DESARROLLO DE LA JUNTA

De acuerdo con las previsiones legales y estatutarias, actúan de presidente y secretario de la Junta los que lo son del Consejo de Administración quienes me acreditan sus cargos (que declaran subsistentes), y se identifican, mediante la exhibición de las copias autorizadas de escrituras y de los Documentos Nacionales de Identidad - ya reseñados en el requerimiento.

D./Dña. [NOMBRE Y APELLIDOS] se declara nombrado Presidente de la Junta y D./Dña. [NOMBRE Y APELLIDOS], designado como Secretario por unanimidad de los votos correspondientes al capital social.

Advertidos los asistentes por mí, el Notario, sobre si desean dejar constancia en acta de cualesquiera manifestaciones, intervenciones u oposiciones, en relación a la propuesta y acuerdo citados ninguno ejerce tal derecho

Identifico yo, el Notario, al Presidente y Secretario nombrados a través de sus respectivos Documentos Nacionales de Identidad, números [Nº] y [Nº], que, a tal fin me exhiben.

Declara el Presidente de la Junta que la misma está válidamente constituida, y que a la sesión concurren, presentes o representados, [Nº] socios, titulares de las [Nº] participaciones sociales que integran la totalidad del capital social de la entidad. Cada una de las participaciones sociales atribuye derecho a emitir un voto.

Advertidos por mí, el Notario, en tal sentido, ninguno de los asistentes formula protesta o reserva alguna sobre la citadas declaraciones del Presidente y Secretario

Punto primero del Orden del día

Tras declarar el Presidente la procedencia de entrar a examinar el punto primero del Orden del día, su debate, propuesta y acuerdo se desarrollan en los términos siguientes:

Se aprueba en su integridad y por unanimidad la propuesta reseñada

Y, siendo las [HORA] del mismo día, el Presidente declara concluida la Junta y levanta la sesión, sin que ninguno de los asistentes desee formular cualesquiera otras manifestaciones.

Con lo cual concluyo la presente diligencia que, por referencia a las notas tomadas en el momento de practicarla, extiendo en mi despacho cuando son las [HORA] del [FECHA].

Doy fe de todo el contenido de la presente, que extiendo sobre [DESCRIBIR] folios serie [SERIE] y números [Nº].

D./Dña. [NOMBRE Y APELLIDOS]

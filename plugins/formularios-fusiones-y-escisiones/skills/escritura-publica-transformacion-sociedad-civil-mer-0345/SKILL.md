---
name: escritura-publica-transformacion-sociedad-civil-mer-0345
description: "Escritura pública de transformación de una sociedad civil en sociedad limitada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de transformación de una sociedad civil en sociedad limitada

> Formulario **MER-0345** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura Pública por la que se acuerda la transformación de una sociedad Civil en sociedad de Responsabilidad Limitada con expresión de la aprobación del balance de la sociedad presentado para la transformación, con las modificaciones que en su caso resulten procedentes, así como de las menciones exigidas para la constitución de la sociedad cuyo tipo se adopte y la continuidad de la responsabilidad por las deudas sociales durante 5 años.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de transformación de una sociedad civil en sociedad limitada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de transformación de una sociedad civil en sociedad limitada” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:escritura-publica-transformacion-sociedad-civil-mer-0345`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] Nº (9 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] NACIONALIDAD (3 veces)
- [ ] CAPITAL SOCIAL (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] ACTIVIDAD
- [ ] CALLE
- [ ] CARGO
- [ ] COLEGIO
- [ ] DNI/NIE
- [ ] EJERCICIO
- [ ] ESTADO CIVIL
- [ ] FOLIO Y HOJA
- [ ] LUGAR
- [ ] NIF
- [ ] Nº DE PROTOCOLO
- [ ] OBJETO SOCIAL
- [ ] PLAZO
- [ ] SERIE
- [ ] TOMO

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

Modelo de escritura Pública por la que se acuerda la transformación de una sociedad Civil en sociedad de Responsabilidad Limitada con expresión de la aprobación del balance de la sociedad presentado para la transformación, con las modificaciones que en su caso resulten procedentes, así como de las menciones exigidas para la constitución de la sociedad cuyo tipo se adopte y la continuidad de la responsabilidad por las deudas sociales durante 5 años.


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

NÚMERO

ELEVACIÓN A PÚBLICO DE ACUERDOS SOCIALES

En [LUGAR], a [FECHA].

Ante mí, Notario del Ilustre Colegio de [COLEGIO],

COMPARECEN

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO],

INTERVIENEN

[OPCIONAL — incluir si procede]

(En nombre propio)

En nombre y derecho propio como únicos socios de la sociedad civil denominada [DENOMINACIÓN SOCIAL] con NIF número [NIF], domiciliada en [DOMICILIO], calle [CALLE], con actividad principal de

[OPCIONAL — incluir si procede]

(En representación)

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[OPCIONAL — incluir si procede]

(Si se trata de persona física)

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO],

[OPCIONAL — incluir si procede]

(Si se trata de una persona jurídica)

Compañía mercantil de nacionalidad española denominada [DENOMINACIÓN SOCIAL], [ELEGIR: SL / SA], domiciliada en [DOMICILIO], calle, con NIF núm. Inscrita en el Registro Mercantil de [LOCALIDAD], en [TOMO] el [FOLIO Y HOJA]. Su capital social es de [CAPITAL SOCIAL], dividido en [Nº], [ELEGIR: participaciones / acciones / cuotas] de [IMPORTE] euro de valor nominal cada una de ellas, numeradas correlativamente del 1 al [Nº] ambos inclusive, estando totalmente suscritas e íntegramente desembolsadas.

Dicha Sociedad tiene por objeto social [OBJETO SOCIAL]

Hace uso de las facultades conferidas a su favor en calidad de:

[ELEGIR UNA OPCIÓN: Cargo social / Apoderado]

Y el representante de la sociedad [DENOMINACIÓN SOCIAL], según interviene, hace constar, conforme a lo establecido en la Ley 10/2010 de 28 de abril, que el titular real de la sociedad ha sido identificado en acta de manifestaciones autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS] el día [FECHA], con el número de su protocolo [Nº DE PROTOCOLO], manifestando no haberse modificado el contenido de la misma, y por tanto no ha habido modificación en la titularidad real reflejada.

Identifico a los comparecientes por la documentación que muestran y les juzgo con la capacidad legal necesaria para el otorgamiento de la escritura de transformación de Sociedad Civil en Sociedad de Responsabilidad Limitada y a tal efecto

EXPONEN

1. Que con fecha [FECHA] los comparecientes D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS] constituyeron una sociedad civil por tiempo indefinido.

2. Que la sociedad civil se está domiciliada en [DOMICILIO], siendo su actividad principal [ACTIVIDAD].

3. Que el capital social de la sociedad civil se fijó en [CAPITAL SOCIAL], aportados por los socios a partes iguales en metálico.

Me entregan en este acto, a mí, el Notario, el contrato de constitución de la sociedad civil, con liquidación de impuestos incluida, que protocolizo con esta matriz.

4. Que debido a que quieren transformar la sociedad civil en sociedad de responsabilidad limitada, los socios comparecientes se constituyen en este acto en junta general universal y por unanimidad: y a tal efecto

ACUERDAN

Primero. Transformar la sociedad civil en sociedad de responsabilidad limitada, con la denominación de «[DENOMINACIÓN SOCIAL], SL».

Con dicho fin los comparecientes me entregan certificación negativa de denominación social vigente expedida por el Registro Mercantil Central. La certificación queda protocolizada con esta matriz.

Igualmente, me entregan los estatutos de la sociedad limitada, aprobados unánimemente y firmados por todos ellos, que protocolizo con esta matriz.

Segundo. Aprobar por unanimidad el balance de la sociedad, cerrado el día [FECHA], anterior al día de la adopción de este acuerdo, conforme al artículo 218 del Reglamento del Registro Mercantil. El balance queda asimismo protocolizado con esta matriz.

Tercero. Aportar y desembolsar todo el patrimonio de la sociedad civil a la nueva sociedad de responsabilidad limitada, manifestando bajo su responsabilidad que el patrimonio cubre el capital social.

Cuarto. Establecer el capital social de la sociedad limitada en [IMPORTE] euros, dividido en [Nº] participaciones de [IMPORTE] euros de valor nominal cada una, numeradas del 1 al [Nº], ambos inclusive, que quedan atribuidas a los socios de la siguiente manera:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Al socio D./Dña. [NOMBRE Y APELLIDOS] se les atribuyen [Nº] participaciones sociales, números [Nº] a [Nº], inclusive, con un valor nominal en conjunto de [IMPORTE] euros.

Quinto. Reconocer que la sociedad resultante mantiene la personalidad jurídica, así como, el patrimonio y los derechos y obligaciones que correspondían a la sociedad civil que se transforma.

Sexto. Asumir la obligación descrita en el artículo 32.2 del RD-ley 5/2023 de modificaciones estructurales de las sociedades mercantiles, relativa a la subsistencia durante cinco años, a contar desde la publicación de la transformación en el BORME, de su responsabilidad personal por las deudas sociales contraídas con anterioridad a la transformación de la sociedad.

Séptimo. Nombrar [CARGO] a:

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL] mayor de edad, de nacionalidad [NACIONALIDAD], vecino/a de [LOCALIDAD], y con DNI número [DNI/NIE] como [ELEGIR: administrador único / administrador solidario / consejero / administrador mancomunado]

El nombramiento se efectúa por el plazo de [PLAZO]

Presente en el acto, D./Dña. [NOMBRE Y APELLIDOS] acepta el cargo conferido, promete cumplirlo con diligencia y manifiesta no estar incurso en causa alguna de incapacidad, incompatibilidad o prohibición legal para su ejercicio [EJERCICIO]. en especial las de la Ley 3/2015, de 30 de marzo, reguladora del ejercicio del alto cargo de la Administración General del Estado, ni las de las demás disposiciones legales, estatales o autonómicas aplicables, lo que ratificaron todos los asistentes.

OTORGAMIENTO Y AUTORIZACIÓN

Hago a los comparecientes las reservas y advertencias legales, especialmente las derivadas de la legislación fiscal, y del Registro Mercantil y de su publicidad.

Leo esta escritura a los comparecientes advirtiéndoles del derecho que tienen a hacerlo personalmente, derecho al que renuncian. Enterados de su contenido, los comparecientes hacen constar libremente su consentimiento al otorgamiento de la escritura y la firman.

Y yo, el Notario, compruebo que el consentimiento ha sido libremente prestado y se adecua a la legalidad, y del contenido de esta escritura, extendida en [Nº] folios de papel exclusivo para documentos notariales, serie [SERIE], números [Nº], DOY FE.

Notario

Otorgantes

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

---
name: escritura-publica-constitucion-sociedad-comanditaria-mer-0459
description: "Escritura pública de constitución de una sociedad comanditaria por acciones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de constitución de una sociedad comanditaria por acciones

> Formulario **MER-0459** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública de constitución de una Sociedad Comanditaria por Acciones, en la que se establecen y concretan, entre otras cosas, las pautas y condiciones necesarias para su creación y funcionamiento, denominación, duración, domicilio, objeto y capital social.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de constitución de una sociedad comanditaria por acciones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de constitución de una sociedad comanditaria por acciones” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:escritura-publica-constitucion-sociedad-comanditaria-mer-0459`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] Nº (11 veces)
- [ ] IMPORTE (7 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (3 veces)
- [ ] CALLE (2 veces)
- [ ] DATOS REGISTRALES (2 veces)
- [ ] ACTIVIDAD
- [ ] COLEGIO
- [ ] CÓDIGO CNAE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] ENTIDAD ENCARGADA DEL REGISTRO CONTABLE
- [ ] INSCRIPCIÓN
- [ ] LUGAR
- [ ] Nº DE PROTOCOLO
- [ ] NÚMERO
- [ ] OBJETO SOCIAL

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

Modelo de escritura pública de constitución de una Sociedad Comanditaria por Acciones, en la que se establecen y concretan, entre otras cosas, las pautas y condiciones necesarias para su creación y funcionamiento, denominación, duración, domicilio, objeto y capital social.


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

Ante mí, Notario del Ilustre Colegio de [COLEGIO]

COMPARECEN

[OPCIONAL — incluir si procede]

(Si fuera una persona física)
[ELEGIR UNA OPCIÓN: En caso de estado civil no casado / En caso de estado civil casado]

[OPCIONAL — incluir si procede]

(Si fuera una persona jurídica)

La compañía mercantil de nacionalidad española denominada [DENOMINACIÓN SOCIAL], [ELEGIR: SL / SA], domiciliada en [DOMICILIO], calle [CALLE], con NIF núm. Inscrita en el Registro Mercantil de [LOCALIDAD], en [DATOS REGISTRALES] el

INTERVIENEN

Los señores comparecientes intervienen en su propio nombre y derecho.

[OPCIONAL — incluir si procede]

(Cuando se trate de representantes)

D./Dña. [NOMBRE Y APELLIDOS] hace uso de las facultades conferidas a su favor en calidad de:

[OPCIONAL — incluir si procede]

(Cargo social)

administrador único [ELEGIR: administrador solidario / administrador mancomunado / Secretario del Consejo de Administración] de la sociedad indicada, cargo para el que fue nombrado en escritura otorgada ante notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS] el [FECHA] con el número de orden de su protocolo [Nº DE PROTOCOLO] que causó inscripción en el Registro Mercantil de [LOCALIDAD] en el

[OPCIONAL — incluir si procede]

(Apoderado)

apoderado de la sociedad antes mencionada, según consta en escritura de poder otorgada a su favor, ante notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], mediante escritura de [FECHA] con el número [NÚMERO] de orden de su protocolo que causó inscripción [INSCRIPCIÓN] en el Registro Mercantil de [LOCALIDAD] en el [DATOS REGISTRALES].

Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente escritura de constitución de SOCIEDAD COMANDITARIA POR ACCIONES, a cuyo fin

EXPONEN

I.- Que los mentados Sres. han convenido realizar de manera conjunta [ACTIVIDAD].

II.- Que, a tales efectos, y en su calidad de únicos socios fundadores, han decidido otorgar la presente escritura de constitución deSOCIEDAD COMANDITARIA POR ACCIONES, que se regirá por lo previsto en la presente escritura, a cuyos efectos

OTORGAN

Primero.- Constitución.

Los comparecientes:

Como socios colectivos:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS],

Como socios comanditarios,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS],

proceden a constituir una Sociedad Comanditaria por acciones.

Segundo.- Régimen legal

La mercantil ‘ S.Com.por A’ se regirá por lo dispuesto en el presente contrato y los estatutos que a él se incorporan, por las disposiciones correspondientes del Texto Refundido de la Ley de Sociedades de Capital, Código de Comercio y demás disposiciones que resulten aplicables.

Tal y como establece el art.20 de la L 14/2013, de 27 de septiembre los comparecientes dejan constancia de que la Clasificación Nacional de Actividades Económicas (CNAE) que le corresponderá a la entidad constituida es la siguiente: [CÓDIGO CNAE].

Tercero.- Denominación.

[ELEGIR UNA OPCIÓN: Con aportación de certificación negativa / Con solicitud telemática por el notario]

Cuarto.- Duración.

La Sociedad tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de la presente escritura, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Sociedad en momentos anteriores al de su inscripción en el Registro Mercantil.

Los ejercicios sociales se computarán por años naturales.

Quinto.- Domicilio.

El domicilio de la Sociedad se halla situado en [DIRECCIÓN], calle [CALLE]

Sexto.- Objeto social.

El objeto social de la Sociedad será [OBJETO SOCIAL].

Séptimo.- Capital social.

El capital social será de [IMPORTE], dividido en [Nº] acciones de [IMPORTE] euros de valor nominal cada una de ellas, numeradas de manera correlativa con los números 1 a [Nº] y representadas mediante [ELEGIR: títulos al portador / títulos nominativos / anotaciones en cuenta]

[OPCIONAL — incluir si procede]

(En caso de estar representadas por anotaciones en cuenta)

La entidad encargada de llevar dicho registro contable es [ENTIDAD ENCARGADA DEL REGISTRO CONTABLE].

Dicho capital social ha sido totalmente suscrito y desembolsado por los socios fundadores, habiendo realizado cada uno de ellos las aportaciones que se describen a continuación:

[OPCIONAL — incluir si procede]

(Si se trata de aportaciones dinerarias)
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], aporta en efectivo por su valor nominal conjunto [IMPORTE] y suscribe [Nº] acciones, que son las numeradas [Nº] a [Nº]

[ELEGIR UNA OPCIÓN: Cuando exista ingreso previo / Cuando la entrega del efectivo se hace directamente al notario]

[OPCIONAL — incluir si procede]

(Si se trata de aportaciones no dinerarias)

D./Dña. [NOMBRE Y APELLIDOS] aporta a la sociedad, con el consentimiento de su cónyuge, (el bien que corresponda o la mitad indivisa), valorado en ", equivalente al valor nominal de las acciones númerosde laa.

La totalidad de estas aportaciones ha sido realizada a título de propiedad, en pleno dominio, con todos sus derechos inherentes y accesorios y libres de toda carga y gravamen, arrendamientos, responsabilidad u otras afecciones.

En prueba de todo ello los comparecientes me entregan para unir a la presente documentación, a lo cual procedo, los correspondientes informes emitidos por el/los experto/s independiente/s nombrados a tal fin por el Registrador Mercantil de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], en los que se describen y valoran las citadas aportaciones no dinerarias

[OPCIONAL — incluir si procede]

(Si se trata de aportaciones mixtas)

D./Dña. [NOMBRE Y APELLIDOS] - con el consentimiento de su cónyuge, efectúa las siguientes aportaciones a la sociedad:

a). Dineraria: [IMPORTE] euros en efectivo metálico, correspondiente al valor nominal de las acciones números " de a [Nº].

b). No dineraria " (el bien que corresponda o la mitad indivisa), por su valor de [IMPORTE] correspondiente al valor nominal- de las acciones números [Nº] de [Nº] a [Nº]. Esta aportación no dineraria ha sido realizada a título de propiedad, en pleno dominio, con todos sus derechos inherentes y accesorios y libres de toda carga y gravamen, arrendamientos, responsabilidad u otras afecciones. Se anexa a la presente escritura el informe sobre la valoración de esta aportación.

Octavo.- Gastos de constitución

La cuantía total aproximada de los gastos de constitución incluidos los ya satisfechos se calcula que alcanzará la cifra de [IMPORTE] euros.

Noveno.- Administración.

La administración se encomienda por los comparecientes a D./Dña. [NOMBRE Y APELLIDOS], en su calidad de socio colectivo, quien ejercerá sus funciones como administrador único por un período de [Nº] años, percibiendo por ello una retribución anual bruta de [IMPORTE] euros.

D./Dña. [NOMBRE Y APELLIDOS] acepta el cargo y toma posesión del mismo, manifestando no hallarse incurso en ninguna de las causas que inhabilitan para el ejercicio de dicho cargo.

Décimo.- Aprobación de los estatutos sociales.

Se procede a la aprobación de los Estatutos que han de regir el funcionamiento de la Sociedad, que los comparecientes me otorgan en este acto, extendidos en [Nº] folios, aprobados y firmados por ellos, que ratifican y elevan a escritura pública mediante su incorporación a la presente, que solicitan expresamente, lo cual efectúo uniéndolos al final de esta matriz.

OTORGAMIENTO Y AUTORIZACIÓN NOTARIAL

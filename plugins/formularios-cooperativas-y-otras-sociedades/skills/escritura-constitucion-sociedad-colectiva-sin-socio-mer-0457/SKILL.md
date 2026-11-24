---
name: escritura-constitucion-sociedad-colectiva-sin-socio-mer-0457
description: "Escritura de constitución de una sociedad colectiva, con o sin socio industrial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de constitución de una sociedad colectiva, con o sin socio industrial

> Formulario **MER-0457** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública de constitución de una Sociedad Colectiva, en la que se establecen y concretan las pautas y condiciones necesarias para su creación y funcionamiento, denominación, duración, domicilio, objeto, capital social y socios industriales.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de constitución de una sociedad colectiva, con o sin socio industrial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de constitución de una sociedad colectiva, con o sin socio industrial” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:escritura-constitucion-sociedad-colectiva-sin-socio-mer-0457`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] IMPORTE (4 veces)
- [ ] DATOS REGISTRALES (3 veces)
- [ ] FECHA (3 veces)
- [ ] Nº (3 veces)
- [ ] CALLE (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] ACTIVIDAD
- [ ] COLEGIO
- [ ] CRITERIO DE REVISIÓN
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DIRECCIÓN
- [ ] DOMICILIO
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

Modelo de escritura pública de constitución de una Sociedad Colectiva, en la que se establecen y concretan las pautas y condiciones necesarias para su creación y funcionamiento, denominación, duración, domicilio, objeto, capital social y socios industriales.


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

[OPCIONAL — incluir si procede]

(Si fuera una persona física)
[ELEGIR UNA OPCIÓN: En caso de estado civil no casado / En caso de estado civil casado]

[OPCIONAL — incluir si procede]

(Si fuera una persona jurídica)

La compañía mercantil de nacionalidad española denominada [DENOMINACIÓN SOCIAL], [ELEGIR: SL / SA], domiciliada en [DOMICILIO], calle [CALLE], con NIF núm. Inscrita en el Registro Mercantil de [LOCALIDAD], en [DATOS REGISTRALES] el [DATOS REGISTRALES].

INTERVIENEN

Los señores comparecientes intervienen en su propio nombre y derecho.

[OPCIONAL — incluir si procede]

(Cuando se trate de representantes)

D./Dña. [NOMBRE Y APELLIDOS] hace uso de las facultades conferidas a su favor en calidad de:

[OPCIONAL — incluir si procede]

(Cargo social)

[ELEGIR: administrador único / administrador solidario]de la sociedad indicada, cargo para el que fue nombrado en escritura otorgada ante notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS] el [FECHA] con el número de orden de su protocolo [Nº DE PROTOCOLO] que causó inscripción en el Registro Mercantil de [LOCALIDAD] en el

[OPCIONAL — incluir si procede]

(Apoderado)

apoderado de la sociedad antes mencionada, según consta en escritura de poder otorgada a su favor, ante notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], mediante escritura de [FECHA] con el número [NÚMERO] de orden de su protocolo que causó inscripción [INSCRIPCIÓN] en el Registro Mercantil de [LOCALIDAD] en el [DATOS REGISTRALES].

Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente escritura de constitución deSOCIEDAD COLECTIVA, a cuyo fin

EXPONEN

PRIMERO.- Que los mentados Sres. han convenido realizar de manera conjunta actividad que vaya a ser objeto de la explotación común.

SEGUNDO.- Que, a tales efectos, y en su calidad de únicos socios fundadores, han decidido otorgar la presente escritura de constitución de SOCIEDAD COLECTIVA, que se regirá por las siguientes

ESTIPULACIONES

I.- Constitución.

En el presente acto los comparecientes proceden a constituir una Sociedad Colectiva que se regirá por el presente contrato, por los estatutos que en el mismo se aprueban, y en lo en ellos no dispuesto, por el Código de Comercio, así como por cuantas disposiciones resulten de aplicación.

II.- Denominación.

[ELEGIR UNA OPCIÓN: Con aportación de certificación negativa / Con solicitud telemática por el notario]

III.- Capital social

El capital social se cifra en [IMPORTE] euros, importe que ha sido desembolsado de la siguiente forma:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
[ELEGIR UNA OPCIÓN: Entrega en efectivo / Mediante ingreso en cuenta bancaria]

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(En caso de aportaciones no dinerarias)

D./Dña. [NOMBRE Y APELLIDOS] aporta, con el consentimiento de su cónyuge si se trata de un bien ganancial [DESCRIPCIÓN DEL BIEN] valorado en [IMPORTE] euros

En prueba de todo ello los comparecientes me entregan para unir a la presente matriz, a lo cual procedo, los correspondientes informes emitidos por el experto independiente en los que se describen y valoran las citadas aportaciones no dinerarias.

Todas las aportaciones se realizan a título de propiedad

[OPCIONAL — incluir si procede]

(Cuando existan socios industriales)
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] sólo aportará a la sociedad [DENOMINACIÓN SOCIAL] servicios, trabajo o actividad, consistente en la realización de las siguientes actividades [ACTIVIDAD], por lo que asume la condición de socio industrial, percibiendo con carácter mensual una cantidad de [IMPORTE] euros revisables por períodos anuales según [CRITERIO DE REVISIÓN] criterio de revisión.

IV- Duración.

La Sociedad tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de la presente escritura, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Sociedad en momentos anteriores al de su inscripción en el Registro Mercantil.

Los ejercicios sociales se computarán por años naturales.

V.- Domicilio.

El domicilio de la Sociedad se halla situado en [DIRECCIÓN], calle [CALLE], por ser éste el lugar en el que radican su efectiva dirección y administración.

VI.- Objeto social.

El objeto social de la Sociedad será [OBJETO SOCIAL].

VII.- Socio gestor.

La administración y representación de la Sociedad se encomienda a un socio gestor, quien tendrá el uso de la firma social.

El gestor representará a la sociedad en cuantos aspectos sean referentes a su giro o tráfico, tanto judicial como extrajudicialmente.

Se procede a nombrar, en este mismo acto, a D./Dña. [NOMBRE Y APELLIDOS] como socio gestor de la Sociedad, quien acepta, y manifiesta no hallarse incurso en ninguna de las causas que inhabilitan para el ejercicio de dicho cargo.

ISe encomienda al socio gestor la presentación de la presente escritura constitutiva para su inscripción en el Registro Mercantil de [LOCALIDAD] quien se compromete a su cumplimiento.

VIII.- Cantidades que se asignan al socio gestor anualmente para sus gastos particulares.

Se acuerda como cantidad anual a asignar a cada socio gestor, a fin de que pueda ser destinada a sus gastos particulares, [IMPORTE] euros, revisables cada [Nº] años según

IX.- Aprobación de los estatutos sociales.

Se procede a la aprobación de los Estatutos que han de regir el funcionamiento de la Sociedad, que los comparecientes me otorgan en este acto, extendidos en [Nº] folios, aprobados y firmados por ellos, que ratifican y elevan a escritura pública mediante su incorporación a la presente, que solicitan expresamente, lo cual efectúo uniéndolos al final de esta matriz.

X.- Inscripción en el Registro Mercantil

Advierto yo, el Notario, a los señores comparecientes, a los efectos y de conformidad con lo establecido en el artículo 82 del Reglamento del Registro Mercantil, acerca de la obligatoriedad de la inscripción de la presente escritura en dicho Registro, y, a efectos fiscales, les hago las reservas y advertencias relativas a las obligaciones y responsabilidades tributarias que incumben a las partes en su aspecto material, formal y sancionador.

[ELEGIR UNA OPCIÓN: Comunicación al Registro mercantil / Opción 1: Presentación telemática / Opción 2: Presentación no telemática]

XI Protección de datos personales

Advierto expresamente al compareciente que sus datos van a ser incorporados al fichero del Protocolo y documentación notarial y al fichero de Administración y organización, así como del hecho de que, en su caso, tales datos pueden ser cedidos a aquellas Administraciones públicas que según una norma con rango de ley tengan derecho a ello. Hechas las advertencias de sus derechos al respecto.

OTORGAMIENTO Y AUTORIZACIÓN

Les leo, por su elección, esta escritura, advertidos de su derecho a leerla por sí, del que no usan y, tras hacerles las oportunas explicaciones verbales para su cabal conocimiento, manifiestan quedar enterados, la aceptan, se ratifican y firman.

Yo, el Notario, Doy fe de que el consentimiento ha sido libremente prestado y de que el otorgamiento se adecua a la legalidad y a la voluntad debidamente informada de los otorgantes.

Queda extendida en un total de [Nº] folios de papel notarial, el primero con el número y los demás con los números siguientes en orden correlativo.

Y de su contenido, DOY FE.

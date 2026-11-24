---
name: escritura-publica-constitucion-agrupacion-interes-mer-0454
description: "Escritura pública de constitución de una agrupación de interés económico. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de constitución de una agrupación de interés económico

> Formulario **MER-0454** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública de constitución de una agrupación de interés económico, en la que se establecen y concretan, entre otras cosas, las pautas y condiciones necesarias para su funcionamiento, denominación, duración, domicilio, objeto y capital social y disolución.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de constitución de una agrupación de interés económico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de constitución de una agrupación de interés económico” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:escritura-publica-constitucion-agrupacion-interes-mer-0454`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] CLASE
- [ ] COLEGIO
- [ ] DIRECCIÓN
- [ ] FECHA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MEDIO DE COMUNICACIÓN
- [ ] NACIONALIDAD
- [ ] Nº
- [ ] NÚMERO
- [ ] PROFESIÓN
- [ ] SERIE

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

Modelo de escritura pública de constitución de una agrupación de interés económico, en la que se establecen y concretan, entre otras cosas, las pautas y condiciones necesarias para su funcionamiento, denominación, duración, domicilio, objeto y capital social y disolución.


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

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO],

INTERVIENEN

Los señores comparecientes intervienen en su propio nombre y derecho.

Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente escritura de constitución de una AGRUPACIÓN DE INTERÉS ECONÓMICO, a cuyo fin

EXPONEN

PRIMERO.- Que los mentados Sres. son todos ellos [OTROS DATOS] dedicados [ACTIVIDAD], por lo que reúnen los requisitos legales precisos para ser socios de una Agrupación de Interés Económico.

SEGUNDO.- Que es voluntad de los mismos constituir la Agrupación de Interés Económico ‘, A.I.E.’, denominación que no consta registrada por ninguna sociedad ni ninguna otra entidad inscribible en el Registro Mercantil Central, según consta en la certificación negativa de denominaciones que a tal efecto me exhiben y a cuyo requerimiento procedo a incorporar a la matriz de la presente escritura.

TERCERO.- Que a tales efectos proceden al otorgamiento de la presente escritura de constitución de la Agrupación de Interés Económico ‘, A.I.E.’, que se regirá por las siguientes

ESTIPULACIONES

I.- Constitución

Los otorgantes proceden a constituir una Agrupación de Interés Económico que se regirá por el presente contrato y por la Ley 12/1991, de 29 de Abril, reguladora de las Agrupaciones de Interés Económico, así como por cuantas disposiciones legales y reglamentarias que resulten de aplicación.

II.- Socios y responsabilidad

Son socios de la misma los otorgantes

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS],

Quienes responderán personal y solidariamente entre sí, y subsidiariamente con respecto a la Agrupación, de las deudas contraídas por la misma.

III.- Denominación

La Agrupación se denomina ‘, A.I.E.’.

IV.- Duración

La Agrupación tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de la presente escritura, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Agrupación en momentos anteriores al de su inscripción en el Registro Mercantil.

V.- Domicilio

El domicilio de la Agrupación se halla situado en [DIRECCIÓN], por ser éste el lugar en el que radican su efectiva dirección y administración.

VI.- Objeto social

El objeto social de la Agrupación es [ACTIVIDAD]

VII.- Capital social

El capital social se cifra en [IMPORTE] euros, en cuya composición han participado los socios en las siguientes proporciones [OTROS DATOS]

VIII.- Adopción de acuerdos

Los acuerdos de la Agrupación serán adoptados:

* En Asamblea de socios, por correspondencia escrita o electrónica o por cualquier otro medio que permita tener constancia escrita de la consulta y del voto emitido por los socios.
* Se atribuye un voto a cada socio.
* Se requiere que el acuerdo de disolución sea adoptado por la mayoría de los socios
- Por conclusión de la actividad que constituye su objeto o por imposibilidad de realizarlo.
- Por paralización de los órganos sociales de modo que resulte imposible su funcionamiento.
* Los demás acuerdos precisarán unanimidad de los socios, en concreto en los siguientes supuestos referentes a la modificación de la presente escritura:
- Objeto de la Agrupación.
- Número de votos atribuidos a cada socio.
- Requisitos para la adopción de los acuerdos.
- Duración prevista para la Agrupación.
- Cuota de contribución de cada uno de los socios o de algunos de ellos a la financiación de la Agrupación.

IX.- Convocatoria de la Asamblea de socios

La Asamblea de los socios deberá ser convocada por el Administrador por propia iniciativa o a instancia de cualquier socio.

En este caso, la convocatoria debe realizarse en el plazo máximo de 30 días.

La convocatoria se comunicará a los socios por medio de [MEDIO DE COMUNICACIÓN] con acuse de recibo con al menos 15 días de antelación a la fecha fijada para la reunión, en la que deberá expresarse con claridad los asuntos que pretendan tratarse en la misma, y el lugar, fecha y hora de la reunión.

X.- Admisión, separación y exclusión de socios

La admisión de nuevos socios precisa en todo caso acuerdo unánime de los miembros de la Asamblea, en escritura pública que, inscrita en el Registro Mercantil,

Cualquier socio tendrá derecho a separarse de la Agrupación por los siguientes motivos:

* Cuando concurra justa causa.
* Cuando medie el consentimiento de los demás socios.

La separación de algún socio por mediar justa causa:

* Deberá hacerse constar en escritura pública otorgada por el propio interesado, en la que deben constar la causa alegada y la notificación fehaciente a la Agrupación.
* Deberá inscribirse en el Registro Mercantil, inscripción que no se extenderá hasta transcurridos 15 días desde la fecha de la notificación, siempre que no exista oposición por parte de la Agrupación.

Si existe tal oposición, deberá suspenderse la inscripción hasta que decidan los Tribunales. Mientras tanto, puede tomarse anotación preventiva por el plazo de 1 año.

La pérdida de la condición de socio podrá producirse en los siguientes casos:

* Cuando dejen de concurrir en el socio los requisitos exigidos por la Ley y por la presente escritura para ser socio de la Agrupación.
* Cuando se declare el concurso, del socio
* Por exclusión del socio por alguna de las siguientes causas:

Dicha exclusión:

- Deberá hacerse constar en escritura pública otorgada por el administrador facultado por acuerdo unánime del resto de los socios en la que deben expresarse los siguientes aspectos:
• Causa alegada, y
• Notificación fehaciente al excluido.
- Deberá ser inscrita en el Registro Mercantil, sin que la inscripción pueda extenderse hasta que haya transcurrido un mes desde la fecha de la notificación al socio excluido.
• Si dentro de ese plazo se acreditase la impugnación judicial del acuerdo de exclusión, se suspenderá la inscripción hasta que recaiga sentencia firme.
• No obstante, si la exclusión se debiera a la muerte o declaración judicial de fallecimiento del socio o al transcurso del plazo establecido, puede practicarse la inscripción en virtud de instancia en la que se consigne la causa de exclusión y a la que debe acompañarse, en su caso, certificación del Registro Civil.

El socio cesante tendrá derecho a la liquidación de su participación de acuerdo con las reglas establecidas en la presente escritura, y en su defecto, según lo previsto en el Código de Comercio.

XI.- Administración de la Agrupación

La Agrupación será gestionada, administrada y representada en juicio o fuera de él y en todos los actos comprendidos en el objeto social por un Administrador Único, que podrá ostentar (o no) la condición de socio.

El cargo de Administrador tendrá una duración de cinco años, y podrá ser reelegido por la Asamblea de socios una o más veces por períodos de igual duración máxima.

El Administrador responderá de los daños causados a la Agrupación, salvo cuando pruebe haber actuado conforme a la diligencia exigida.

Se procede al nombramiento, en el presente acto, de D./Dña. [NOMBRE Y APELLIDOS] como Administrador Único inicial de la Agrupación, quien acepta el cargo y manifiesta no hallarse incurso en ninguna de las causas que inhabilitan para el ejercicio del mismo.

XII.- Participación en los resultados económicos

Los resultados económicos positivos y las pérdidas procedentes de las actividades de la Agrupación serán considerados como beneficios o pérdidas de los socios y repartidos entre ellos en la siguiente proporción

XIII.- Disolución

La sociedad quedará disuelta en los casos y con los requisitos establecidos en la Ley.

OTORGAMIENTO Y AUTORIZACIÓN NOTARIAL

Hechas las reservas y advertencias legales, en particular y a efectos fiscales, advierto de las obligaciones y responsabilidades tributarias que incumben a las partes en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se pueden derivar de la eventual inexactitud de sus declaraciones.

Leo a los señores comparecientes la presente escritura, previa su renuncia a su derecho de hacerlo por sí, del que les advierto. La consienten y firman conmigo, el Notario, que doy fe de todo lo precedente consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales, de clase [CLASE], serie [SERIE], números

D./Dña. [NOMBRE Y APELLIDOS]

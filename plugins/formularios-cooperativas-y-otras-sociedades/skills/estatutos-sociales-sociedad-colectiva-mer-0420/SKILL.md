---
name: estatutos-sociales-sociedad-colectiva-mer-0420
description: "Estatutos sociales de una sociedad colectiva. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Estatutos sociales de una sociedad colectiva

> Formulario **MER-0420** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo genérico de creación de estatutos sociales para una Sociedad Colectiva, en los que se concretan las bases de organización y funcionamiento de la sociedad, tales como la duración, domicilio, objeto y capital social, socio industrial, participación de los socios y disolución de la misma. SOCIEDAD COLECTIVA: ESTATUTOS

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Estatutos sociales de una sociedad colectiva» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Estatutos sociales de una sociedad colectiva” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:estatutos-sociales-sociedad-colectiva-mer-0420`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN
- [ ] Nº
- [ ] NÚMERO
- [ ] OBJETO SOCIAL
- [ ] PISO
- [ ] PORCENTAJE

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

Modelo genérico de creación de estatutos sociales para una Sociedad Colectiva, en los que se concretan las bases de organización y funcionamiento de la sociedad, tales como la duración, domicilio, objeto y capital social, socio industrial, participación de los socios y disolución de la misma.

SOCIEDAD COLECTIVA: ESTATUTOS


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

TÍTULO I.- DENOMINACIÓN, DURACIÓN, DOMICILIO Y OBJETO

Artículo 1º.- Denominación

La sociedad se denomina [DENOMINACIÓN SOCIAL] SOCIEDAD COLECTIVA, y se regirá por los presentes estatutos, así como por las disposiciones legales que le sean aplicables en cada momento.

Artículo 2º.- Duración

La sociedad tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día en que se otorgue su escritura de constitución, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la sociedad en momentos anteriores al de su inscripción en el Registro Mercantil.

Artículo 3º.- Domicilio social

El domicilio social se halla situado en [DIRECCIÓN], calle [CALLE], número [NÚMERO], piso [PISO], por ser éste el lugar en el que radican su efectiva dirección y administración.

El órgano de administración podrá decidir la creación, supresión y traslado de sucursales.

Artículo 4º.- Objeto social

La Sociedad tendrá como objeto social [OBJETO SOCIAL]

TÍTULO II.- CAPITAL SOCIAL Y LOS SOCIOS

Artículo 5º.- Capital social

[ELEGIR UNA OPCIÓN: Aportaciones dinerarias / Aportaciones no dinerarias]

Artículo 6º.- Derechos y obligaciones de los socios

Cada uno de los socios colectivos tiene los mismos derechos y obligaciones, correspondiendo a cada uno un voto y respondiendo ilimitadamente con todos sus bienes en la forma que determina el Código de Comercio.

Los socios colectivos percibirán, con carácter de remuneración directa de su trabajo personal y con independencia de los beneficios sociales que puedan devengar sus participaciones sociales, unos sueldos fijos cuya cuantía será fijada por la Asamblea de Socios, atendiendo a la marcha económica de la sociedad y a la intensidad y continuidad de los servicios prestados.

Todos los socios contraen la prohibición de concurrencia por sí o por persona interpuesta en negocios similares o conexos a los que desarrolle la sociedad.

Los socios participarán en las ganancias sociales de acuerdo a los siguientes porcentajes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D. participará en un [PORCENTAJE] %

Los socios participarán en las pérdidas de acuerdo a los mismos porcentajes previstos en el artículo anterior para su participación en las pérdidas.

No obstante lo anterior, los socios industriales no responderán de las pérdidas más allá de los límites de las aportaciones realizadas al capital social.

TÍTULO III.- ÓRGANOS SOCIALES

Artículo 7º.- Disposiciones generales

[ELEGIR UNA OPCIÓN: Con dos administradores solidarios / Con dos administradores mancomunados / Con administrador único]

Sección 1ª.- Asamblea de Socios

Artículo 8º.- Asamblea de Socios

Todos los socios colectivos reunidos, previa citación, forman la junta de socios, en cuyo órgano radica toda la soberanía social.

Todos los socios, incluidos los disidentes y los que no hayan participado en la reunión, quedan sometidos a los acuerdos adoptados por la Asamblea, sin perjuicio de su derecho de impugnación, en los supuestos previstos legalmente, y cuando concurran los requisitos precisos al efecto.

Cualquiera de los socios podrá pedir la reunión de la Asamblea, solicitándolo al socio gestor con al menos [Nº] días de antelación, y señalando la hora y día de su celebración y los asuntos a tratar en la misma. El socio gestor debe realizar la convocatoria de los socios mediante citación por escrito entregada personalmente o enviada a sus respectivos domicilios por correo certificado con al menos días de antelación a la fecha de la celebración de la reunión.

Artículo 9º.- Votaciones y adopción de los acuerdos

Cada uno de los puntos que formen parte del Orden del Día deberán ser objeto de votación separada.

Los acuerdos de la asamblea ordinaria se tomarán por mayoría de los socios que asistan a ella y, si hubiere empate, lo decidirá la mayoría de capital.

Será necesario el consentimiento unánime de los socios:

1. Para autorizar la cesión de las participaciones sociales.
2. Para la modificación de los estatutos.
3. Para la transformación o disolución de la sociedad.

Sección Segunda.- Socios gestores

[ELEGIR UNA OPCIÓN: Órgano de Administración / Gestores solidarios / Socios gestores mancomunados / Socio gestor único]

TÍTULO IV.- EJERCICIO SOCIAL Y CUENTAS ANUALES

Artículo 14º.- Ejercicio social

Los ejercicios sociales comenzarán el 1 de enero y finalizarán el 31 de diciembre de cada año natural.

El primer ejercicio social, por excepción, comenzará el día en que la sociedad inicie sus operaciones y terminará el 31 de diciembre de ese mismo año.

Artículo 15º.- Cuentas anuales

En el plazo máximo de tres meses contados a partir del cierre de cada ejercicio económico el órgano de administración deberá formular las Cuentas Anuales, incluyendo en las mismas el Balance, la Cuenta de Pérdidas y Ganancias y la Memoria explicativa, el informe de gestión y la propuesta de aplicación de los resultados, según los criterios de valoración y con la estructura legal y reglamentariamente exigidos, y en su caso, deberán asimismo redactarse las cuentas y el informe de gestión consolidados, que deberán ir firmados por todos los administradores, expresándose en defecto de firma cuál sea la causa de su falta.

Artículo 16º.- Depósito y publicidad de las Cuentas Anuales

Cuando las Cuentas Anuales sean aprobadas por la Asamblea de socios éstas serán presentadas para su depósito, con la certificación del acuerdo de la Asamblea, en el Registro Mercantil correspondiente, en el plazo y forma legales y reglamentarios.

Artículo 17º.- Aplicación del resultado

La aplicación del resultado del ejercicio es competencia de la Asamblea de Socios, con los límites legales y estatutarios vigentes.

De los beneficios obtenidos en cada ejercicio, una vez cubierta la dotación para reserva legal, y demás atenciones legalmente establecidas, la Junta podrá aplicar lo que estime conveniente para reserva voluntaria, fondo de previsión para inversiones y cualquier otra atención legalmente permitida. El resto, en su caso, se distribuirá como dividendos entre los socios en proporción al capital desembolsado por cada acción.

TÍTULO V.- DISOLUCIÓN Y LIQUIDACIÓN DE LA SOCIEDAD

Artículo 18º.- Disolución

La sociedad se disolverá:

a) Por vencimiento del término de su duración, si antes no fuere prorrogado válidamente; b) Por la imposibilidad de desarrollar la empresa social, por la terminación de la misma o por la extinción de la cosa o cosas cuya explotación constituye su objeto; c) Por disminución del número de socios a menos de dos; d) Por la iniciación del trámite de liquidación obligatoria de la sociedad; e) Por decisión de la Asamblea de Socios adoptada conforme a las reglas dadas para las reformas estatutarias y a las prescripciones de la ley; f) Por decisión de autoridad competente en los casos expresamente previstos en la ley; g) Por muerte de alguno de los socios; h) Por incapacidad sobreviniente a alguno de los socios; i) Por la iniciación del trámite de liquidación obligatoria de alguno de los socios, si los demás no adquieren su interés social o no aceptan la cesión a un extraño, una vez requeridos por el liquidador, dentro de los treinta días hábiles siguientes; j) Por enajenación forzada del interés de alguno de los socios en favor de un extraño, si los demás asociados no se avienen dentro de los treinta días hábiles siguientes a continuar la sociedad con el adquirente; k) Por renuncia o retiro justificado de alguno de los socios si los demás no adquieren su interés en la sociedad o no aceptan su cesión a un tercero.

Artículo 19º.- Forma de liquidación

La Asamblea de Socios que acuerde la disolución de la sociedad acordará igualmente el nombramiento de los liquidadores, que podrá recaer en los propios miembros del órgano de administración.

El número de liquidadores será siempre impar.

Artículo 20º.- Normas liquidatorias

En la liquidación de la sociedad se observarán las normas establecidas en la Ley y las que, en complemento a éstas y respetando los límites legales, hayan sido acordadas por la Asamblea de Socios que haya adoptado el acuerdo de disolución.

TÍTULO VI.- RÉGIMEN SUPLETORIO

Artículo 21º.- Régimen supletorio

En todo lo no previsto en los artículos anteriores de los presentes estatutos se aplicarán las normas del Código de Comercio y del Reglamento del Registro Mercantil.

Artículo 22º.- Resolución de controversias

[ELEGIR UNA OPCIÓN: Resolución de controversias / Sumisión a Tribunales / Arbitraje]

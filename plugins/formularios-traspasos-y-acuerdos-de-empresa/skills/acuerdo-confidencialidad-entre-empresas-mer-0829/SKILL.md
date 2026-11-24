---
name: acuerdo-confidencialidad-entre-empresas-mer-0829
description: "Acuerdo de confidencialidad entre empresas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acuerdo de confidencialidad entre empresas

> Formulario **MER-0829** del plugin **Traspasos de negocio, confidencialidad y acuerdos de empresa** (`formularios-traspasos-y-acuerdos-de-empresa`) · Mercantil › Otros documentos mercantiles · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acuerdo de confidencialidad entre empresas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acuerdo de confidencialidad entre empresas” para mi caso». También puedes invocarla directamente con `/formularios-traspasos-y-acuerdos-de-empresa:acuerdo-confidencialidad-entre-empresas-mer-0829`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-traspasos-y-acuerdos-de-empresa:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Traspasos de negocio, confidencialidad y acuerdos de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE DE LA PARTE (9 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] ESTADO CIVIL
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL NOTARIO

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS] mayor de edad, de estado civil vecino de [LOCALIDAD] domiciliado en [DOMICILIO] con documento nacional de identidad número [NÚMERO]

De otra:

D [NOMBRE Y APELLIDOS] mayor de edad, de estado civil [ESTADO CIVIL] vecino de [LOCALIDAD] domiciliado en [DOMICILIO] con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A] en lo sucesivo "LA EMPRESA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO] en fecha [FECHA] con el número de protocolo [Nº DE PROTOCOLO] poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A] en lo sucesivo "", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D en fecha [FECHA] con el número de protocolo [Nº DE PROTOCOLO] poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente ACUERDO DE CONFIDENCIALIDAD, de conformidad con las siguientes,

ESTIPULACIONES

Objeto

El presente acuerdo se refiere a la información que [NOMBRE DE LA PARTE] proporcione a la mercantil [DENOMINACIÓN SOCIAL] ya sea de forma oral, gráfica o escrita y, en estos dos últimos casos, ya esté contenida en el "Plan de Negocios" o en cualquier otro tipo de documento, con ocasión de las negociaciones que se están desarrollando acerca de la posibilidad de que [NOMBRE DE LA PARTE] adquiera participaciones de

Confidencialidad

1. únicamente utilizará la información facilitada por LA EMPRESA para el fin mencionado en la estipulación anterior, comprometiéndose a mantener la más estricta confidencialidad respecto de dicha información, advirtiendo de dicho deber de confidencialidad y secreto a sus empleados, asociados y a cualquier persona que, por su relación con [NOMBRE DE LA PARTE] deba tener acceso a dicha información.

2. o las personas mencionadas en el párrafo anterior no podrán reproducir, modificar, hacer pública o divulgar a terceros la información objeto del presente acuerdo, sin previa autorización escrita y expresa de LA EMPRESA

3. De igual forma, [NOMBRE DE LA PARTE] adoptará respecto de la información objeto de este acuerdo las mismas medidas de seguridad que adoptaría normalmente respecto a la información confidencial de su propia Empresa, evitando su pérdida, robo o sustracción.

Límites a la confidencialidad

Sin perjuicio de lo estipulado en el presente acuerdo, ambas partes aceptan que la obligación de confidencialidad no se aplicará en los siguientes casos:

a) Cuando la información se encontrara en el dominio público en el momento de su suministro a [NOMBRE DE LA PARTE] o, una vez suministrada la información, ésta acceda al dominio público sin infracción de ninguna de las estipulaciones del presente acuerdo.

b) Cuando la legislación vigente o un mandato judicial exija su divulgación. En ese caso, [NOMBRE DE LA PARTE] notificará a LA EMPRESA tal eventualidad, y hará todo lo posible por garantizar que se dé un tratamiento confidencial a la información.

c) En caso de que [NOMBRE DE LA PARTE] pueda probar que la información fue desarrollada o recibida legítimamente de terceros, de forma totalmente independiente a su relación con LA EMPRESA

Derecho de propiedad

Los derechos de propiedad intelectual de la información objeto de este acuerdo pertenecen a LA EMPRESA, y el hecho de revelarla a [NOMBRE DE LA PARTE] para el fin mencionado en la estipulación primera, no cambiará tal situación.

En caso de que la información resulte revelada o divulgada o utilizada por [NOMBRE DE LA PARTE] de cualquier forma distinta al objeto de este acuerdo, ya sea de forma dolosa o por mera negligencia, habrá de indemnizar a LA EMPRESA los daños y perjuicios ocasionados, quien se reserva el ejercicio de las acciones civiles o penales que puedan corresponderle por dicho motivo.

A tal fin, y como indemnización mínima, que no excluye la reclamación de otros daños que pudiera ocasionar la revelación de la información prestada por LA EMPRESA, se establece la cantidad de [IMPORTE] euros.

Duración

El presente acuerdo entrará en vigor en el momento de la firma del mismo por ambas partes, extendiéndose su vigencia hasta un plazo de [Nº] años después de la finalización de las negociaciones para la compra de participaciones de LA EMPRESA

se obliga a devolver a LA EMPRESA, de manera inmediata, cualquier documentación que ésta haya facilitado, en cualquier tipo de soporte y, en su caso, las copias obtenidas de los mismos, que constituyan información amparada por el deber de confidencialidad objeto del presente acuerdo, en el supuesto de que se den por finalizadas las negociaciones para la compra de participaciones de LA EMPRESA

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal en caso de no ejecución voluntaria de la sentencia]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente ACUERDO, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Y en prueba de conformidad con todo lo expuesto, firman el presente por duplicado y a un solo efecto, en lugar y fecha indicados al encabezamiento.

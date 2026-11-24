---
name: convenio-colaboracion-entre-despachos-abogados-mer-0509
description: "Convenio de colaboración entre despachos de abogados. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convenio de colaboración entre despachos de abogados

> Formulario **MER-0509** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Modelo de acuerdo de colaboración entre despachos de abogados, mediante el cual se comprometen, entre otras cosas, a no quebrantar el secreto profesional y a colaborar en la difusión de su colaboración por medios adecuados. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del acuerdo, así como los derechos y obligaciones de cada una de las partes.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convenio de colaboración entre despachos de abogados» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convenio de colaboración entre despachos de abogados” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:convenio-colaboracion-entre-despachos-abogados-mer-0509`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE DE LA PARTE (5 veces)
- [ ] DENOMINACIÓN ABREVIADA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] OBLIGACIONES DE LA PARTE (2 veces)
- [ ] CLÁUSULA ADICIONAL
- [ ] COLEGIO
- [ ] FECHA
- [ ] FINALIDAD DE LA COLABORACIÓN
- [ ] IMPORTE
- [ ] INSTITUCIÓN ARBITRAL
- [ ] LUGAR
- [ ] OBJETO DEL CONTRATO
- [ ] PLAZO
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

Modelo de acuerdo de colaboración entre despachos de abogados, mediante el cual se comprometen, entre otras cosas, a no quebrantar el secreto profesional y a colaborar en la difusión de su colaboración por medios adecuados. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del acuerdo, así como los derechos y obligaciones de cada una de las partes.


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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

(Datos del Firmante Uno)

[ELEGIR UNA OPCIÓN: si el despacho es una sociedad / si se trata de un abogado autónomo]

En lo sucesivo, [DENOMINACIÓN ABREVIADA].

Y DE OTRA,

(Datos del Firmante Dos)

[ELEGIR UNA OPCIÓN: si el despacho es una sociedad / si se trata de un abogado autónomo]

En lo sucesivo, [DENOMINACIÓN ABREVIADA].

INTERVIENEN

Ambas partes se reconocen mutua y recíprocamente capacidad y legitimación suficientes para suscribir este ACUERDO DE COLABORACIÓN, asegurando cada parte que los poderes con que respectivamente actúan no han sido revocados ni limitados, y que son bastantes para obligar a sus representadas en virtud de este acto, y, en esa representación,

EXPONEN

I.- Que [NOMBRE DE LA PARTE] es [ELEGIR: una empresa / profesional] que se dedica a la prestación de servicios jurídicos y desarrolla su actividad bajo la marca [MARCA/MODELO], con sede en [LOCALIDAD] y oficinas abiertas en las localidades que se mencionan en el Anexo I, con el personal adscrito que se señala en el mismo para cada uno de dichos centros de operaciones, ofreciendo a sus clientes un servicio de asesoría integral y defensa judicial y extrajudicial.

II.- Que [NOMBRE DE LA PARTE] es asimismo, [ELEGIR: una empresa / profesional] que se dedica a la prestación de servicios jurídicos y desarrolla su actividad bajo la marca [MARCA/MODELO], con sede en [LOCALIDAD] y oficinas abiertas en las localidades que se mencionan en el Anexo, con el personal adscrito que se señala en el mismo para cada uno de dichos centros de operaciones, ofreciendo a sus clientes un servicio de asesoría integral y defensa judicial y extrajudicial.

III.- Que ambas partes están interesadas en establecer una colaboración para [OBJETO DEL CONTRATO] y, por ello, convienen obligarse de acuerdo con las siguientes

ESTIPULACIONES

Primera.- Objeto del Convenio

El presente contrato tiene por objeto regular los términos de la colaboración entre [NOMBRE DE LA PARTE] e [NOMBRE DE LA PARTE], colaboración que tiene por finalidad [FINALIDAD DE LA COLABORACIÓN].

Segunda.- Obligaciones de las partes

1. Por el presente contrato, [NOMBRE DE LA PARTE] se obliga a: [OBLIGACIONES DE LA PARTE].

2. Por el presente contrato, se obliga a: [OBLIGACIONES DE LA PARTE].

Tercera.- Reglas comunes de colaboración

Las partes contratantes aceptan las siguientes normas que regularán el funcionamiento profesional, financiero, ético y de relación entre los abogados de los despachos colaboradores:

(Pueden pactarse, por ejemplo, las siguientes:)

[OPCIONAL — incluir si procede]

a) No quebrantar y salvaguardar el secreto profesional.

[OPCIONAL — incluir si procede]

b) Colaborar en la difusión de la existencia de su colaboración por medios adecuados que no perjudiquen su imagen y prestigio.

Para fomentar la cohesión, las partes contratantes podrán utilizar la imagen corporativa resultante de su colaboración en los términos y condiciones que se establecen en el Anexo II, relativo a las normas de uso y reproducción gráfica del logotipo y demás componentes de la imagen corporativa para su incorporación a la correspondencia y demás elementos de publicidad.

[OPCIONAL — incluir si procede]

c) Colaborar en la buena relación entre los abogados de los despachos asociados así como en la celebración de congresos y reuniones entre ellos.

[OPCIONAL — incluir si procede]

d) Relación profesional entre asociados.

La colaboración se asienta en el principio básico de facilitar que cada despacho pueda prestar servicios a sus clientes fuera de su jurisdicción, valiéndose de otro despacho que realizará el trabajo encomendado, dentro de unos mismos niveles de calidad y precio, compartiendo utilidades en función del trabajo de cada una de las partes.

El despacho de origen se responsabiliza del pago de los honorarios del despacho de destino.

Al inicio de cualquier asunto, el despacho de origen deberá disponer, como mínimo, de una provisión de fondos del [PORCENTAJE] % del presupuesto en los términos que se regulan en el Anexo III de los que se incorporan al presente Acuerdo.

Los compañeros de los despachos colaboradores se dispensarán entre sí el mismo respeto, amistad y confianza que si se tratase de un compañero del propio despacho.

[OPCIONAL — incluir si procede]

e) Reparto de honorarios.

Los beneficios o utilidades que genere cada asunto (honorarios) se repartirán entre las partes contratantes según las siguientes normas:

General:

i.- % para la parte que genere el asunto.
ii.- % para la parte que resuelva el asunto.

Normas especiales:

i.- Acuerdos especiales por escrito en el que se regule que la retribución se repartirá en función de los trabajos y ayudas que desarrolle la parte que genera el asunto (despacho de origen) y la que lo desarrolla (despacho de destino).
ii.- Cuando la consulta la efectúe un despacho profesional, éste deberá pactar con el despacho asociado de destino el reparto de honorarios en función del trabajo de cada despacho.

f) Confidencialidad. Los distintos profesionales que intervengan en un asunto deberán guardar absoluto secreto de las informaciones que conozcan con ocasión de la colaboración con otro profesional.

g) Custodia de documentos. Los documentos originales o sus fotocopias de los que se haya servido para realizar su trabajo deberán ser custodiados con la máxima diligencia para evitar su reproducción y, por consiguiente, el quebranto de la confidencialidad.

Los documentos originales, una vez examinados, deberán ser devueltos al profesional que los haya entregado en custodia. Como norma general, cada profesional acusará recibo de los documentos que le entregue otro profesional (originales o fotocopias) para ser utilizados en su trabajo, identificándolos individualmente.

No obstante todo lo anterior, quedan a salvo las normas de conducta de cada profesión y a las que cada profesional pueda estar sujeto.

Cuarta.- Condiciones económicas y forma de pago

Quinta.- Confidencialidad y protección de datos personales

Ambas partes se comprometen a no divulgar la información confidencial referente a la otra parte o sus clientes de la que hayan tenido conocimiento por razón de la ejecución del presente contrato y a mantenerla en secreto, incluso después de la finalización del mismo.

Ambas partes acuerdan tomar las medidas necesarias respecto a su personal e incluso terceros que puedan tener acceso a dichas información y documentación, a fin de garantizar la confidencialidad objeto de esta cláusula.

Ambas partes reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos de personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales. A tal efecto, cada [ELEGIR: despacho / profesional]:

a) Únicamente accederá a los datos personales de clientes y demás personas físicas relacionadas con el otro despacho si tal acceso fuese necesario para cumplir con los servicios objeto del presente contrato.
b) Se compromete a:
- Utilizar los datos de carácter personal a los que tenga acceso única y exclusivamente para cumplir con sus obligaciones contractuales para con el otro despacho.
- Observar y adoptar cuantas medidas de seguridad sean necesarias para asegurar la confidencialidad, secreto e integridad de los datos de carácter personal a los que tenga acceso, así como a adoptar en el futuro cuantas medidas de seguridad sean exigidas por las leyes y reglamentos destinadas a preservar el secreto, confidencialidad e integridad en el tratamiento automatizado de datos personales.
- A no ceder en ningún caso a terceras personas los datos de carácter personal a los que tenga acceso, ni tan siquiera a efectos de su conservación.

Las obligaciones establecidas para cada despacho por la presente cláusula serán también de obligado cumplimiento para sus posibles empleados, colaboradores, tanto externos como internos, y subcontratistas, por lo que cada despacho responderá si tales obligaciones son incumplidas por sus empleados, colaboradores y subcontratistas.

El incumplimiento por parte de alguno de los despachos de cualesquiera de las obligaciones establecidas de Confidencialidad y Tratamiento de Datos de Carácter Personal, generará una indemnización en favor del otro de [IMPORTE] euros, sin perjuicio del derecho de éste a resarcirse de los perjuicios que le sean causados y que superen la cuantía indicada.

La duración de las obligaciones de confidencialidad establecidas en el presente contrato será indefinida, manteniéndose en vigor con posterioridad a la finalización, por cualquier causa, de la relación entre los despachos.

Sexta.- Duración de la colaboración

El presente acuerdo tendrá una duración inicial de [PLAZO], prorrogable por períodos anuales cuando así lo manifiesten expresamente las partes mediante acuerdo por escrito que se incorporará al presente, a más tardar el 31 de diciembre de cada ejercicio.

Séptima.- Propiedad intelectual e industrial

(Pueden incorporarse sendas licencias de marca para que cada parte pueda utilizar la de la otra en los términos que se detallen al efecto; o bien puede pactarse dicha licencia con carácter unilateral, así como cualquier otra cesión de derechos de propiedad intelectual o industrial).

[CLÁUSULA ADICIONAL]

Octava.- Exclusividad

[ELEGIR UNA OPCIÓN: Se pacta exclusividad / No se pacta exclusividad]

Novena.- Resolución

Sin perjuicio de la extinción que corresponda por mutuo acuerdo o cumplimiento del plazo pactado, ambas partes podrán denunciar el presente acuerdo, por incumplimiento grave de las condiciones esenciales pactadas en el mismo.

La existencia del incumplimiento grave será comunicada fehacientemente por la parte denunciante, mediante comunicación escrita. La parte infractora tendrá el plazo de un mes para subsanar la causa del incumplimiento. Al final de este plazo si la causa de incumplimiento no hubiera sido subsanada el acuerdo quedará resuelto automáticamente si así lo requiriese la parte perjudicada.

Las partes se comprometen a intentar resolver de buena fe y de manera amistosa cualquier desacuerdo que pueda surgir en el desarrollo del presente Convenio previo a acudir a la jurisdicción contemplada en la estipulación siguiente.

Décima.- Ley y Jurisdicción aplicables

El presente Convenio de Colaboración se regirá por la Ley española.

Las partes acuerdan que todo tipo de litigio, discrepancia, cuestión o reclamación resultantes de la ejecución o interpretación del presente Acuerdo se resolverán definitivamente mediante arbitraje en el marco de [INSTITUCIÓN ARBITRAL] (por ejemplo, Colegio de Abogados de [COLEGIO]) a quien se encomienda la Administración del arbitraje y la designación de los árbitros de acuerdo con su Reglamento y Estatutos. Igualmente, las partes hacen constar expresamente su compromiso de cumplir el laudo arbitral que se dicte.

Y en prueba de conformidad se firma el presente acuerdo, por duplicado ejemplar, en el lugar y fecha arriba indicados.

Firmado: Firmado:

Firmado: Firmado:

ANEXO I: INFORMACIÓN DETALLADA DE LOS DESPACHOS EN COLABORACIÓN

(Sedes, abogados, personal laboral, etc.)

ANEXO II: REGLAS DE USO DEL LOGOTIPO Y DEMÁS SIGNOS IDENTIFICATIVOS DE LA IMAGEN CORPORATIVA RESULTANTE DEL ACUERDO.

ANEXO III: NORMAS COMUNES PARA EL CÁLCULO DE HONORARIOS Y PRESUPUESTOS.

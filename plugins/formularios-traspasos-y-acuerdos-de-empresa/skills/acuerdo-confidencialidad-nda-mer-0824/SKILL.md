---
name: acuerdo-confidencialidad-nda-mer-0824
description: "Acuerdo de confidencialidad (NDA). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acuerdo de confidencialidad (NDA)

> Formulario **MER-0824** del plugin **Traspasos de negocio, confidencialidad y acuerdos de empresa** (`formularios-traspasos-y-acuerdos-de-empresa`) · Mercantil › Otros documentos mercantiles · normativa revisada el 24-11-2026.

## Qué es

El acuerdo de confidencialidad, también conocido como NDA (por las siglas en inglés de Non-Disclosure Agreement) es un contrato que tiene como objetivo comprometer legalmente a las partes a no revelar información que se intercambia entre las mismas para un objetivo o fin determinado, pero que no está o no debe alcanzar el domino público.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acuerdo de confidencialidad (NDA)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acuerdo de confidencialidad (NDA)” para mi caso». También puedes invocarla directamente con `/formularios-traspasos-y-acuerdos-de-empresa:acuerdo-confidencialidad-nda-mer-0824`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-traspasos-y-acuerdos-de-empresa:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Traspasos de negocio, confidencialidad y acuerdos de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] CORREO ELECTRÓNICO
- [ ] FECHA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NOMBRE DEL PROYECTO
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE CLÁUSULA

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

El acuerdo de confidencialidad, también conocido como NDA (por las siglas en inglés de Non-Disclosure Agreement) es un contrato que tiene como objetivo comprometer legalmente a las partes a no revelar información que se intercambia entre las mismas para un objetivo o fin determinado, pero que no está o no debe alcanzar el domino público.


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

[ELEGIR UNA OPCIÓN: Si es persona física / Si es persona jurídica]

Y DE OTRA,

[ELEGIR UNA OPCIÓN: Si es persona física / Si es persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para obligarse y otorgar este acuerdo de confidencialidad (en adelante, El acuerdo) y, a tal efecto,

EXPONEN

I. Que las partes colaboran conjuntamente a fin de desarrollar el proyecto [NOMBRE DEL PROYECTO].

II. Que este acuerdo se establece para garantizar, en el desarrollo del proyecto descrito anteriormente un máximo nivel de confianza entre ambas partes y para implantar las condiciones bajo las que el divulgador acuerda revelar cierta información confidencial, que es de su propiedad, al receptor.

III. Que el acuerdo regirá la custodia y no transmisión a terceros de la información distribuida entre las partes, así como los derechos, obligaciones y responsabilidades que les incumben en su condición de divulgador y receptor de la información indicada.

IV. Que, a fin de completar el proyecto referido en el precedente I, las partes reconocen que el receptor podría llegar a suministrar información confidencial propia al divulgador, motivo por el que le serían de aplicación a este último los términos y las condiciones previstas en este acuerdo para el receptor.

Por todo lo expuesto, las partes han alcanzado este acuerdo que se regirá por las siguientes

CLÁUSULAS

Primera.- Definiciones

Información confidencial – toda aquella susceptible de revelación por escrito, de palabra o por cualquier otro medio o soporte, tangible o intangible, actualmente conocido o que posibilite el estado de la técnica en el futuro, intercambiada como consecuencia de este acuerdo.

La información confidencial puede incluir —pero no se limita a— descubrimientos, conceptos, ideas, conocimientos, técnicas, know-how, software, planes de negocio, prototipos, diseños y dibujos, resultados de pruebas, borradores, diagramas, textos, modelos, muestras, bases de datos de cualquier tipo, aplicaciones, programas, marcas, logotipos, cualquier tipo de información industrial, financiera publicitaria, técnica, personal, comercial que las partes se intercambien o revelen por cualquier vía.

Divulgador – cualquiera de las partes cuando, en los términos recogidos en este acuerdo, suministre a la otra parte información considerada confidencial.

Receptor – cualquiera de las partes cuando, en los términos recogidos en este acuerdo, reciba de la otra parte información considerada confidencial. El receptor queda obligado a mantener la información en secreto y a emplearla únicamente para los fines que se establezcan en este acuerdo.

Segunda.- Objeto del acuerdo

El objeto de este acuerdo es determinar en qué términos y condiciones las partes van a comunicarse y a mantener en secreto los datos y la información que se intercambien entre sí.

Tercera.- Deber de confidencialidad

Las partes reconocen que la información que compartan o se transmitan en el desarrollo del proyecto referido en el expositivo I tiene carácter confidencial. Se considera específicamente confidencial la información detallada en el Anexo de este acuerdo.

Cada una de las partes se obliga a dar un trato confidencial a la información definida como tal en este acuerdo y que reciba de la otra en el ámbito del proyecto referido anteriormente, comprometiéndose a no divulgarla y a mantener su confidencialidad, poniéndola en conocimiento sólo de las personas que, para el desarrollo del proyecto señalado en el expositivo I, sea imprescindible.

Las partes se comprometen a emplear la información divulgada única y exclusivamente en orden a desarrollar el proyecto descrito en el expositivo I.

Cada una de las partes advertirá del carácter confidencial de la citada información a sus empleados, colaboradores y cualquier otra persona que, por su relación con el receptor, tenga acceso a aquélla, así como del deber de confidencialidad que les atañe.

Cada parte, en cuanto receptora de información confidencial, es responsable del uso indebido que de la información confidencial puedan hacer sus empleados, colaboradores y cualquier otra persona que, por su relación con ella, tenga acceso a dicha información.

Las partes están obligadas a poner los medios necesarios para evitar que la información pueda divulgarse, cederse, sustraerse etc. adoptando, a tal efecto, las medidas de seguridad que aplicarían a la información confidencial de su propiedad. En concreto, las partes custodiarán la información confidencial

Cuarta.- Excepciones

Se excluye la confidencialidad de la información en los siguientes supuestos:

1. Si el divulgador autorizara su divulgación, expresamente y por escrito.
2. Si la información revelada al receptor fuera de dominio público.
3. Si la información revelada al receptor deviniera de dominio público con posterioridad sin que aquél violara este acuerdo.
4. Si el receptor ya conociera la información con carácter previo a la firma de este acuerdo, al no tener todavía obligación de guardar confidencialidad.
5. Si el receptor estuviera obligado a revelar la información por mandato legal u orden judicial.

Quinta.- Propiedad

La información revelada bajo el ámbito de este acuerdo es propiedad exclusiva de la parte divulgadora, aunque se transmita al receptor para el desarrollo del proyecto reseñado en el expositivo I.

Ninguna de las partes, en cuanto receptora de información confidencial, podrá utilizar ésta salvo para el desarrollo del proyecto reseñado en el expositivo I.

La revelación de información confidencial al receptor no implica, en ningún caso, que el divulgador le esté otorgando licencia alguna sobre cualquier derecho de propiedad intelectual que integre, en todo o en parte, la información confidencial a que se refiere este acuerdo.

Sexta.- Duración del acuerdo

[ELEGIR UNA OPCIÓN: Por un plazo determinado / De carácter indefinido]

Séptima.- Devolución y/o destrucción de la información confidencial revelada

A la finalización del acuerdo, independientemente de la causa de ésta, cada parte en cuanto receptora queda obligada a devolver toda la información que haya recibido de la otra parte y sus copias o a destruirla, según lo exija la naturaleza de la información o soporte en que se haya transmitido.

Cada parte en cuanto divulgadora habrá de certificar que dicha devolución o destrucción de información confidencial se ha llevado a término correctamente, previa acreditación de esta circunstancia por la parte receptora.

Octava.- Estándar de Cuidado

El receptor protegerá la Información confidencial de la divulgación a cualquier persona que no sea sus directivos, empleados, fuentes de financiación, afiliados y agentes, utilizando un grado de atención razonable y similar al que el mismo utiliza para proteger su propia información confidencial. Igualmente, el receptor requerirá a sus empleados para que acepten las obligaciones de confidencialidad que se estipulan en el presente y será el principal responsable de cualquier incumplimiento de tales obligaciones por parte de los mismos.

Novena.- Sin transferencia de derechos

Ninguna de las partes adquirirá ningún derecho de propiedad intelectual en virtud del presente Acuerdo.

Décima.- Aviso de incumplimiento

El receptor notificará al divulgador inmediatamente tras el descubrimiento de cualquier uso o divulgación no autorizada de la Información confidencial, o cualquier otro incumplimiento de este Acuerdo, y cooperará razonablemente con el divulgador para recuperar la posesión de la Información confidencial y evitar un uso no autorizado.

Decimoprimera.- Incumplimiento

El incumplimiento de las obligaciones establecidas en la cláusula tercera y en la cláusula [Nº DE CLÁUSULA] generará una indemnización en favor de la parte no incumplidora de [IMPORTE] euros, sin perjuicio del derecho de esta última a ejercitar las acciones que estime oportuno, por la vía que corresponda, para resarcirse de cualesquiera daños y perjuicios que se le hayan causado.

[OPCIONAL — incluir si procede]

(Renuncia)

La renuncia al ejercicio de este derecho, o la no exigencia de una obligación o la subsanación de un incumplimiento, no constituirá una renuncia a su ejercicio posterior.

Decimosegunda.- Domicilio a efectos de notificaciones

Las notificaciones que las partes deban realizarse por motivo de este acuerdo se efectuarán en los siguientes domicilios, por escrito y de forma fehaciente.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[NOMBRE Y APELLIDOS], domicilio en [LOCALIDAD] y correo electrónico [CORREO ELECTRÓNICO]

Cada parte queda obligada a notificar a la otra cualquier cambio que se produzca en el domicilio de notificaciones.

Decimotercera.- Protección de datos

Las partes declaran conocer las obligaciones que la legislación sobre protección de datos exige en cuanto a tratamiento de datos de carácter personal.

Con la suscripción de este acuerdo, cada una de las partes consiente que sus datos personales, recogidos en este documento, así como los que hayan de facilitarse entre sí en el desarrollo del proyecto reseñado en el expositivo I, sean incorporados a los correspondientes ficheros de la otra parte.

[OPCIONAL — incluir si procede]

(Pacto de no cesión de datos a terceros)

Las partes no cederán a terceros, en ningún caso, los datos personales recogidos como consecuencia de la suscripción de este acuerdo y del desarrollo del citado proyecto, salvo que medie consentimiento expreso y escrito de la parte titular de esos datos de carácter personal.

Cada parte utilizará los datos de carácter personal a los que tenga acceso única y exclusivamente para dar cumplimiento de las obligaciones asumidas en este acuerdo y para desarrollar el proyecto indicado en el expositivo I.

Las partes adoptarán las medidas de seguridad que sean necesarias para mantener la confidencialidad, secreto e integridad de los datos de carácter personal a los que tengan acceso.

Las obligaciones que establece la presente cláusula se extienden a los empleados de las partes, colaboradores y cuantas personas tengan acceso a datos de carácter personal, tanto externos como internos, y subcontratistas, por lo que las partes responderán frente a la otra parte si tales obligaciones son incumplidas por tales empleados, colaboradores y subcontratistas.

Decimocuarta.- Legislación aplicable y fuero

[ELEGIR UNA OPCIÓN: En caso de no sometimiento a arbitraje / En caso de sometimiento a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

________________________________

Firmado: Firmado:

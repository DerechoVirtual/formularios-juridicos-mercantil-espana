---
name: contrato-joint-venture-entre-empresas-mer-0483
description: "Contrato de joint venture entre empresas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de joint venture entre empresas

> Formulario **MER-0483** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de joint venture entre empresas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de joint venture entre empresas” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-joint-venture-entre-empresas-mer-0483`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] ACTIVIDAD (5 veces)
- [ ] DNI/NIE (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] PAÍS (4 veces)
- [ ] SECTOR DE ACTIVIDAD (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NACIONALIDAD (3 veces)
- [ ] Nº (3 veces)
- [ ] NORMATIVA APLICABLE (2 veces)
- [ ] PLAZO (2 veces)
- [ ] ZONA GEOGRÁFICA (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHA
- [ ] FORMA SOCIETARIA
- [ ] IDIOMA
- [ ] IDIOMAS
- [ ] INSTITUCIÓN ARBITRAL
- [ ] LUGAR
- [ ] OBJETO SOCIAL
- [ ] ÓRGANO DE ADMINISTRACIÓN
- [ ] ÓRGANO O PERSONA

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

Asociación de empresas (nacionales o extrajeras) que mantienen su individualidad e independencia jurídica pero que actúan unidas bajo una misma dirección y normas, para llevar a cabo una operación comercial concreta, en la que se distribuyen las inversiones, el control, responsabilidades, personal, riesgos, gastos y beneficios

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de LA EMPRESA A)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EMPRESA A.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de LA EMPRESA B)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EMPRESA B.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de JOINT VENTURE y, a tal fin,

MANIFIESTAN

I. Que la Empresa A es una sociedad de nacionalidad española, presente en [ZONA GEOGRÁFICA], que cuenta con amplia experiencia en el sector de [SECTOR DE ACTIVIDAD] y con capacidad legal de acuerdo con normativa vigente [NORMATIVA APLICABLE], para participar, tanto en España, como en el extranjero, con otros socios nacionales o extranjeros, ya sean personas naturales o jurídicas, públicas o privadas, en el desarrollo de proyectos en sector de [SECTOR DE ACTIVIDAD], por medio, entre otras modalidades, de la constitución de una empresa conjunta.

II. Que la Empresa B es una sociedad de nacionalidad española, presente en [ZONA GEOGRÁFICA], que cuenta con amplia experiencia en el sector de [SECTOR DE ACTIVIDAD] y con capacidad legal de acuerdo con normativa vigente [NORMATIVA APLICABLE], para participar, tanto en España, como en el extranjero, con otros socios nacionales o extranjeros, ya sean personas naturales o jurídicas, públicas o privadas, en el desarrollo de proyectos en sector de [SECTOR DE ACTIVIDAD], por medio, entre otras modalidades, de la constitución de una empresa conjunta.

III. Que las partes, como consecuencia de la convergencia de intereses y con el objeto de ampliar mercados, desean poner esfuerzos comunes con el objeto de realizar la actividad de [ACTIVIDAD].

IV.- Que el objeto de este contrato es regular las condiciones por las que se regirán las partes en la cooperación para el desarrollo de la actividad de [ACTIVIDAD] bajo las siguientes:

CLÁUSULAS

Primera.- Objeto

Las partes se asocian, con carácter permanente y por tiempo indefinido, para desarrollar, a través de la forma societaria [FORMA SOCIETARIA], una empresa en común, dedicada a [ACTIVIDAD].

Segunda.- Características y forma de operar de la sociedad conjunta

Las partes convienen en constituir una sociedad de nacionalidad [NACIONALIDAD], que iniciará sus actividades el día de su constitución, bajo la denominación de [DENOMINACIÓN SOCIAL] y con el siguiente objeto social [OBJETO SOCIAL].

La sociedad se constituirá con un capital social de [IMPORTE] euros, representado por [ÓRGANO O PERSONA] de [IMPORTE] euros, de valor nominal cada una de ellas, numeradas del al [Nº], inclusive. Las [ELEGIR: participaciones / acciones] serán suscritas por la empresa A en un por 100, por la empresa B en un por 100. Todos los derechos, beneficios y obligaciones que se deriven serán aplicables a los porcentajes reseñados.

El desembolso de las [ELEGIR: participaciones / acciones] se efectuará en su totalidad por los suscriptores mediante aportaciones por valor de [IMPORTE] euros, mediante aportación dineraria el día del otorgamiento de la escritura pública de constitución.

La sociedad será administrada y gobernada por [ÓRGANO DE ADMINISTRACIÓN] que será/n nombrado/s a tal efecto.

[OPCIONAL — incluir si procede]

(Pacto de sindicación de acciones)

Los estatutos contendrán una cláusula de sindicación de acciones que impidan su transmisión a terceros sin ser ofrecidas antes a las otras partes intervinientes en este contrato.

Las partes deciden que la joint venture societaria constituida tenga su centro administrativo y de comercialización en las propias oficinas en las que en la actualidad desarrolla su actividad la empresa A o B, pudiendo las partes, de común acuerdo, trasladarse a otro emplazamiento, si lo consideran conveniente a sus intereses.

Tercera.- Obligaciones de las partes

La empresa A asume la obligación de colaborar en el desarrollo del objetivo común mediante la actuación activa y pasiva para la que sea requerida respecto a la [ACTIVIDAD], captación de clientes y todo aquello que redunde en el beneficio de la nueva entidad.

La empresa B asume la obligación de llevar de manera directa la gestión de [ACTIVIDAD] y de proporcionar a la nueva sociedad todos los medios materiales y humanos necesarios para llevar a cabo la actividad.

Ambas partes convienen que, para llevar a término eficazmente esta asociación, pondrán sus mejores recursos y esfuerzos y cooperarán de común acuerdo, en cuanto sea necesario, para lograr un beneficio racional, justo y equitativo para ambas, quedando prohibida, en todo caso, el ejercicio individual de su actividad, entrando en competencia directa con la Sociedad formada por ambas.

Las partes pueden, de común acuerdo, modificar el presente contrato adoptando como forma de colaboración cualquier otra forma asociativa admitida legalmente y aplicar en la misma las reglas previstas en este contrato en cuanto sea posible su adaptación. El presente contrato de cooperación finalizará a los [PLAZO] desde su firma.

Las partes garantizan la veracidad y validez de la información suministrada y se obligan a no revelar ni divulgar la información confidencial manejada como consecuencia del ejercicio de su actividad, a ninguna persona física o jurídica, sin el consentimiento previo y por escrito de la otra parte.

Cuarta.- Régimen fiscal y arancelario

Las partes se comprometen a solicitar para la joint venture de las Autoridades Competentes de [PAÍS] las exenciones tributarias y arancelarias que estén contempladas por la Ley.

Quinta.- Seguros

Las partes adoptarán las medidas necesarias para que la Joint Venture asegure y mantenga asegurados durante toda su duración todos los activos, existencias, bienes y filiales con una compañía de seguros de reputación internacional de manera que la propia Empresa y, si fuere necesario, cada miembro esté adecuadamente cubierto por sus responsabilidades:

• Contra accidentes, pérdidas, daños, perjuicios, responsabilidad frente a terceros, pérdidas de beneficio y otros riesgos normalmente asegurados de acuerdo con criterios internacionalmente aceptados por entidades que lleven a cabo negocios similares a los de la Empresa Conjunta;
• En cantidades que representen su reposición íntegra o el pago de su valor en [IMPORTE] Euros o en cualquier otra moneda libremente convertible;
• En relación con cualquier cobertura que requiera cualquier persona o entidad que pueda otorgar financiación a la Empresa Conjunta

Sexta.- Rescisión contractual

Cualquiera de las partes podrá exigir la rescisión del contrato siempre que concurran las siguientes circunstancias:

a) Que exista una situación de incumplimiento por una de las partes en las obligaciones que asume por el presente contrato.
b) Por contravenir cualquiera de los pactos que se estipulan en el presente contrato.

[OPCIONAL — incluir si procede]

(Sanción)

La rescisión contractual provocará el efecto de obligar a la parte declarada incumplidora a poner a disposición de la otra la participación que ostente en la joint venture sin recibir contraprestación alguna y dejando a salvo el derecho de la otra parte de reclamar daños y perjuicios.

Séptima.- Fuerza mayor

Ninguna de las partes responderá por el incumplimiento, suspensión o retraso en la ejecución de las obligaciones derivadas del presente contrato, ni estará obligada a indemnizar a la otra por los perjuicios causados, cuando el incumplimiento, la suspensión o retraso sea producido por fuerza mayor debidamente probada.

La prueba de la fuerza mayor corresponderá a quien la alega, presentado como prueba suficiente del suceso. Queda expresamente convenido que tal parte deberá dar notificación por escrito a la otra de los detalles del caso de fuerza mayor dentro de los [Nº] días naturales siguientes a que se haya producido el acontecimiento determinante de dicha fuerza mayor.

La parte afectada por la fuerza mayor está obligada a reanudar el cumplimiento de sus obligaciones tan pronto hayan cesado los efectos de la fuerza mayor. Las obligaciones no afectadas por la fuerza mayor serán cumplidas según las estipulaciones de este Acuerdo.

Octava.- Terminación de la joint venture

Sin perjuicio de las causas señaladas para el supuesto de rescisión contractual, la joint venture terminará:

a) Por vencimiento del plazo señalado anteriormente.
b) Por mutuo acuerdo de las partes.

Novena.- Salvaguardia

Las condiciones del presente contrato podrán revisarse de común acuerdo en caso de que surja un acontecimiento imprevisible y ajeno a la voluntad de las partes que tenga como efecto que una de ellas obtenga ventajas desproporcionadas con respecto a sus obligaciones.

[OPCIONAL — incluir si procede]

(Nombramiento de expertos)

En tales supuestos, se conviene que cada una de las partes designará un experto, y éstos se reunirán para determinar si las condiciones del contrato han sufrido modificaciones fundamentales.

Décima.- Transmisión del contrato

Este contrato de joint venture no podrá cederse ni transferirse sin el consentimiento escrito de la otra parte.

[OPCIONAL — incluir si procede]

(Participación preferente)

En el caso de que una de las partes decida constituir otra sociedad en un campo conexo, concederá a la otra un derecho preferente de participar en dicha sociedad.

Decimoprimera.- Subsistencia de las obligaciones

La rescisión o terminación de este contrato no afecta de manera alguna a la validez y exigibilidad de las obligaciones contraídas con anterioridad, o de aquellas que, por su naturaleza o disposición de la ley, o por voluntad de las partes, deban diferirse a fecha posterior, en consecuencia, las partes podrán exigir, aun con posterioridad a la rescisión o terminación del contrato, el cumplimiento de estas obligaciones.

[OPCIONAL — incluir si procede]

(Extinción por insolvencia)

Decimosegunda.- Insolvencia patrimonial

Ambas partes podrán dar por terminado el presente contrato, en forma anticipada y sin necesidad de declaración judicial previa, en caso de que una de ellas incurra en concurso de acreedores o cualquier otro tipo de insolvencia patrimonial.

. Resolución de controversias

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Las partes, de común acuerdo, deciden someter sus controversias a la competencia de los tribunales del país del [PAÍS] y concretamente a los de la localidad donde éste desarrolle su actividad.

Todos los litigios que puedan plantearse en relación con el presente contrato serán resueltos de forma definitiva según las reglas de conciliación y arbitraje de [INSTITUCIÓN ARBITRAL], por uno o varios árbitros designados de acuerdo con dichas reglas.

.- Legislación aplicable

Este contrato tiene carácter mercantil y se regirá por sus propias cláusulas y, en su defecto, por la ley vigente en [PAÍS].

.- Gastos e impuestos

Cuantos gastos se deriven para la formalización de los actos jurídicos previstos en el presente contrato serán satisfechos por la joint venture.

Los impuestos que se devenguen como consecuencia de todos aquellos actos precisos para la constitución de la joint venture serán de cargo de la misma.

[OPCIONAL — incluir si procede]

(En caso de socios extranjeros)

.- Idioma

El texto íntegro del contrato, así como la documentación que se deriva del mismo, han sido redactados en los idiomas [IDIOMAS], considerándose ambas versiones como oficiales, fijándose como prioritaria para su interpretación la versión en idioma [IDIOMA].

.- Notificaciones

Cualquier notificación que deba enviarse en virtud del presente contrato deberá hacerse en la dirección de las partes que figura en el mismo. No obstante, las partes podrán variar el lugar de recepción de las notificaciones por medio de la notificación fehaciente con [PLAZO] de antelación a que se produzca tal cambio.

Las notificaciones deberán serlo por cualquier medio que deje constancia del contenido de la comunicación y de su recepción.

.- Condiciones suspensivas

Las partes acuerdan, como condición esencial para la puesta en marcha de esta joint venture:

Que la joint venture reciba de las autoridades competentes de [PAÍS]. las licencias, permisos y/o autorizaciones para todas aquellas actividades de su objeto social que así lo requieran de conformidad con la legislación vigente.

Y en prueba de conformidad con todo lo establecido en el presente contrato, ambas partes lo firman en [Nº] ejemplares, en [LOCALIDAD].

EMPRESA A

EMPRESA B

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

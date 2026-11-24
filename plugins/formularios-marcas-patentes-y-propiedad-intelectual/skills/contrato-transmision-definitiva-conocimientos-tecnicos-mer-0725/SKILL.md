---
name: contrato-transmision-definitiva-conocimientos-tecnicos-mer-0725
description: "Contrato de transmisión definitiva de conocimientos técnicos (know how). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de transmisión definitiva de conocimientos técnicos (know how)

> Formulario **MER-0725** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de transmisión definitiva de conocimientos técnicos (know how)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de transmisión definitiva de conocimientos técnicos (know how)” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-transmision-definitiva-conocimientos-tecnicos-mer-0725`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] Nº (5 veces)
- [ ] TIPO DE APARATOS (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PRODUCTOS (2 veces)
- [ ] PRODUCTOS O SERVICIOS (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE EXPERTOS
- [ ] TIPO DE APARATO
- [ ] TIPO DE OPERACIONES
- [ ] ÁMBITO DE ACTIVIDAD

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

CONTRATO DE CESIÓN DE KNOW HOW

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA CEDENTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL CESIONARIO", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE CESIÓN DE KNOW HOW, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO Que la CEDENTE fabrica/presta servicios de [PRODUCTOS O SERVICIOS] desde hace [Nº] años en el ámbito de [ÁMBITO DE ACTIVIDAD] y ha adquirido una importante experiencia y renombre en este dominio. El éxito en la fabricación/prestación de servicios de [PRODUCTOS O SERVICIOS] es particularmente debido a la utilización y conocimientos sobre el funcionamiento del aparato [TIPO DE APARATO] que permite operaciones de [TIPO DE OPERACIONES] según una técnica novedosa.

SEGUNDO Que EL CESIONARIO desea incorporar los conocimientos técnicos y la tecnología utilizada por la CEDENTE a la fabricación de sus productos/ prestación de sus servicios, siendo una mercantil cualificada para fabricar y utilizar los aparatos [TIPO DE APARATOS] de manera satisfactoria.

TERCERO Que en vista de lo anterior, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

Por el presente contrato, La CEDENTE se obliga a suministrar al CESIONARIO toda información sobre los aparatos [TIPO DE APARATOS], su experiencia y los métodos que ella misma emplea, incluidos los procedimientos o secretos de fabricación, de tal manera que un técnico cualificado pueda realizarlos tras un periodo de adaptación razonable. Y le autoriza para hacer uso de todo ello en las condiciones más adelante especificadas.

Precio

El precio de la cesión del know how descrito en el Exponendo primero se concreta en la cantidad de [IMPORTE] euros ( €) más el Impuesto sobre el Valor Añadido correspondiente, esto es, [IMPORTE] € ( euros) adicionales.

[ELEGIR UNA OPCIÓN: Pago del precio / Fijo / Precio fijo / Variable / Precio variable / — y además elegir: Alcance de la cesión / Cesión exclusiva / No exclusiva / Cesión no exclusiva]

Asesoramiento técnico

LA CEDENTE está obligado a poner a disposición del CESIONARIO los conocimientos técnicos que posean y que resulten necesarios para poder proceder a una adecuada explotación de la invención.

A petición del CESIONARIO, la CEDENTE se compromete a poner a su disposición en sus establecimientos en [Nº DE EXPERTOS] (número) expertos técnicos a fin de ayudarla para realizar los ajustes necesarios para la fabricación de los productos/prestación de los servicios conforme a la tecnología y conocimientos licenciados. Los gastos de dicho asesoramiento correrán a cargo del

Medios

La CEDENTE suministrará al CESIONARIO, en el plazo de [Nº] días toda la documentación técnica que se enumera en el Anexo I. En particular, un ejemplar de todos los esquemas, planos y dibujos que permitan la ejecución del material que actualmente se utiliza para la fabricación/prestación de servicios. Y un informe técnico que comprenderá:

• las notas de cálculo,

• los resultados de los ensayos,

• las especificaciones de los materiales a utilizar

• las indicaciones relativas a los incorporaciones y aplicaciones a utilizar

• las indicaciones necesarias para el control de las piezas.

Garantías

La obligación de la CEDENTE se limita al cumplimiento de su prestación de comunicar al CESIONARIO la totalidad de los conocimientos de que dispone para la fabricación de [PRODUCTOS] y prestación de servicios. La CEDENTE no asume responsabilidad por los riesgos inherentes a la realización técnica, a cargo del CESIONARIO. Éste declara conocer los aparatos [TIPO DE APARATOS] y se obliga a fabricar [PRODUCTOS] y prestar los servicios de forma correcta técnicamente conforme al know how cedido.

La CEDENTE no garantiza la explotación comercial del know how cedido. Los riesgos de la misma son a cargo exclusivo del CESIONARIO.

La CEDENTE declara que no ha patentado en ningún país los aparatos [TIPO DE APARATOS], ni partes de los mismos. Asimismo declara no conocer de la existencia de ninguna patente o derecho exclusivo válido perteneciente a terceros que cubra total o parcialmente estos aparatos afectando la posibilidad de su utilización por el CESIONARIO. Si el CESIONARIO fuese demandado, informará a la CEDENTE quien podrá intervenir en el procedimiento.

Mejoras y garantías

La CEDENTE se obliga a comunicar al CESIONARIO toda modificación que aporte ulteriormente al objeto de know-how, de manera que perfeccione la fabricación o prestación de servicios o reduzca los costes. Esta comunicación será obligatoria desde que la modificación llegue a estar disponible para su uso empresarial y queda sometida a las mismas prescripciones impuestas para el know how inicial. La misma obligación incumbe al CESIONARIO.

Deber de confidencialidad

Las Partes se obligan a no revelar, ceder o transferir a terceros ninguna información referente a los negocios, clientes, operaciones, instalaciones, procedimientos, métodos, transacciones, "know-how", o cualquier otro aspecto relacionado con la actividad de la contraparte que pudieran conocer o hayan conocido con motivo de la celebración del presente contrato.

Alcance en cuanto a sistemas de inteligencia artificial

Las Partes acuerdan que las cesiones efectuadas en los anteriores apartados se realizan sin la facultad de emplear los derechos cedidos para el entrenamiento, alimentación o aprendizaje automático de ningún sistema de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robóticos, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología disruptiva relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). De tal manera que, el uso de los derechos cedidos por mor del presente Contrato para los enunciados usos constituirá un incumplimiento sustancial del mismo. El CESIONARIO habrá de respetar el compromiso adquirido en virtud de la anterior Estipulación en los contratos, negocios y relaciones jurídicas que mantenga con terceros, sean personas físicas o jurídicas, adoptando todas las medidas necesarias a tal fin e incluyendo, si fuese necesario, previsiones escritas en los contratos que celebre con estos terceros.

Distribución de los productos

EL CESIONARIO fabricará los productos y prestará los servicios para los que el know how es concedido en el territorio pactado. EL CESIONARIO se obliga a no realizar una política activa de ventas de dichos productos en los territorios que no han sido objeto de la presente licencia. En particular, no realizará en dichos territorios campañas publicitarias dirigidas a la distribución del producto, y no mantendrá almacenes o sucursales para dicha venta.

Obligación de suministro

EL CESIONARIO contratará los servicios y adquirirá los productos de las empresas designadas por la CEDENTE y adquirirá las piezas o sustancias elaborados por la CEDENTE que se especifican en el Anexo II. Sin embargo, siempre que no se altere la calidad y características de los productos o servicios resultantes EL CESIONARIO podrá suministrarse con productos o servicios de empresas distintas

Rendición de cuentas

EL CESIONARIO pondrá en conocimiento de LA CEDENTE de forma detallada los datos relevantes para el cómputo de los cánones pactados como contraprestación. La documentación se remitirá antes del vencimiento del plazo previsto para efectuar dicho pago. Y la CEDENTE podrá examinar la contabilidad del CESIONARIO para comprobar la exactitud de la liquidación realizada. E incluso si fuese necesario para los fines de control del adecuado pago de los cánones pactados podrá controlar, a su costa, y personalmente o por persona expresamente autorizada al efecto la producción del CESEIONARIO.

Resolución del contrato

El Contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2. Por acuerdo de las Partes por escrito.

3. La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

A la finalización del contrato EL CESINARIO no podrá seguir haciendo uso del know how concedido por sí misma o por terceros. Se obliga, desde la expiración del plazo a restituir en un plazo de [Nº] días la documentación recibida del CESIONARIO, sin poder conservar reproducciones, o copias de ningún tipo.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sumisión a tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Sumisión a tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Arbitraje / Sumisión a Arbitraje sin cláusula penal en caso de no ejecución voluntaria del laudo / Sumisión a arbitraje con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE CESIÓN DE KNOW HOW, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La CEDENTE)

Fdo. Don [NOMBRE Y APELLIDOS]

(El CESIONARIO)

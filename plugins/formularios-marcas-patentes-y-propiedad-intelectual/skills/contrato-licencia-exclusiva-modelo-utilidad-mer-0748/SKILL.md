---
name: contrato-licencia-exclusiva-modelo-utilidad-mer-0748
description: "Contrato de licencia exclusiva de un modelo de utilidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de licencia exclusiva de un modelo de utilidad

> Formulario **MER-0748** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de licencia exclusiva de un modelo de utilidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de licencia exclusiva de un modelo de utilidad” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-licencia-exclusiva-modelo-utilidad-mer-0748`.
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
- [ ] Nº (4 veces)
- [ ] AÑO (2 veces)
- [ ] DENOMINACIÓN DEL MODELO DE UTILIDAD (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ACTIVIDAD
- [ ] LUGAR
- [ ] Nº DE REGISTRO
- [ ] ÁMBITO TERRITORIAL

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

Contrato otorgando licencia exclusiva sobre modelo de utilidad reconocido en España

LICENCIA DE MODELO DE UTILIDAD

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA LICENCIANTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL LICENCIATARIO", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar la presente LICENCIA DE MODELO DE UTILIDAD y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO Que LA LICENCIANTE es titular de la patente [DENOMINACIÓN DEL MODELO DE UTILIDAD] inscrita en la Oficina Española de Patentes y Marcas como [Nº DE REGISTRO] el día [DÍA] de [MES] de [AÑO], según justifica mediante certificación del registro que se adjunta al presente como Anexo nº I.

SEGUNDO Que dicha modelo de utilidad se halla libre de cargas y gravámenes.

TERCERO Que el LICENCIATARIO es una sociedad mercantil que tiene por objeto social la [ACTIVIDAD] y está interesado en adquirir el derecho sobre el uso del modelo de utilidad supra mencionada.

CUARTO Que en vista de lo anterior, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

Por el presente contrato, LA LICENCIANTE cede al LICENCIATARIO un derecho de uso sobre el modelo de utilidad [DENOMINACIÓN DEL MODELO DE UTILIDAD] en los términos y condiciones que se detallan en el presente contrato.

[ELEGIR UNA OPCIÓN: Canon / Canon fijo / Canon variable]

Condiciones de uso

EL LICENCIATARIO se obliga a seguir las condiciones e instrucciones de fabricación de los productos fabricados bajo la modelo de utilidad objeto de Licencia especificadas en el Anexo II del presente contrato.

EL LICENCIATARIO está obligado a realizar campañas publicitarias de promoción de los productos fabricados bajo el modelo de utilidad objeto de licencia por un importe mensual/anual de [IMPORTE] euros ( €).

El incumplimiento del LICENCIATARIO de las condiciones de uso de la licencia dará lugar a la inmediata resolución del contrato y al abono de una indemnización por daños y perjuicios LA LICENCIANTE de [IMPORTE] euros.

Declaraciones y garantías

Sobre la titularidad

LA LICENCIANTE declara ser la titular registral del modelo de utilidad y garantiza que ninguna otra persona física o jurídica o entidad de cualquier otra índole ostenta derecho alguno sobre la misma.

Obligación de saneamiento

La LICENCIANTE responderá de cualquier perjuicio que sufra el LICENCIATARIO si por sentencia firme resultare privada de los derechos exclusivos cedidos por el mejor derecho de un tercero, o si se declarase la nulidad o caducidad del modelo de utilidad, o si no se concediese el modelo de utilidad solicitado, o si se malograse de cualquier otra forma la titularidad de la LICENCIANTE sobre el mismo. Pero dicha responsabilidad sólo surgirá si la pérdida del modelo de utilidad o de la solicitud de modelo de utilidad se basase en hechos o circunstancias anteriores a la firma del presente contrato y que la LICENCIANTE conocía o debía haber conocido de haber actuado con una diligencia adecuada, o en el incumplimiento de las obligaciones que conforme al presente contrato se establecen a cargo de la LICENCIANTE.

Por el contrario, la LICENCIANTE no responde de la pérdida del modelo de utilidad, o de la no concesión de la misma cuando resulte de causas desconocidas para él y cuyo desconocimiento no implica negligencia por su parte. O de hechos o circunstancias revelados a la LICENCIATARIO antes de la firma del presente contrato.

Sobre el pago de las cuotas de mantenimiento

LA LICENCIANTE garantiza encontrarse al corriente del pago de las cuotas de mantenimiento del modelo de utilidad.

LA LICENCIANTE se hace responsable de los daños o perjuicios que le ocasione al LICENCIATARIO los eventuales incumplimientos o excepciones a las manifestaciones y garantías vertidas en los párrafos precedentes.

Transmisión de know-how

LA LICENCIANTE está obligado a poner a disposición del LICENCIATARIO los conocimientos técnicos que posean y que resulten necesarios para poder proceder a una adecuada explotación de la invención.

EL LICENCIATARIO a quien se comuniquen conocimientos secretos estará obligado a adoptar las medidas necesarias.

Zona geográfica

En virtud del presente contrato EL LICENCIATARIO adquiere el derecho a utilizar el modelo de utilidad descrita en el Exponendo Primero en la zona geográfica de [ÁMBITO TERRITORIAL]

Prohibición de sublicencias

Esta licencia de uso no supone cesión definitiva del modelo de utilidad ni de ninguno de los derechos que LA LICENCIANTE ostenta sobre el mismo, por lo que el LICENCIATARIO no podrá cederlos, transferirlo a terceros o realizar acto de disposición alguno sobre los mismos sin el consentimiento previo, expreso y por escrito de LA LICENCIANTE.

Exclusividad

Exclusividad de LA LICENCIANTE

LA LICENCIANTE se compromete a no conceder el derecho de utilización del modelo de utilidad a terceros. En este sentido la licencia de uso se concede en exclusiva al LICENCIATARIO.

No obstante, LA LICENCIANTE se reserva el derecho seguir utilizando la modelo de utilidad durante la vigencia del presente Contrato.

Exclusividad del LICENCIARIO

Por su parte, EL LICENCIATARIO se obliga a no comercializar, por sí ni a través de terceros, productos o servicios que de cualquier modo pudieran ser competencia directa o indirecta de los que fabrica o presta LA LICENCIANTE.

Deber de confidencialidad

Las Partes se obligan a no revelar, ceder o transferir a terceros ninguna información referente a los negocios, clientes, operaciones, instalaciones, procedimientos, métodos, transacciones, "know-how", o cualquier otro aspecto relacionado con la actividad de la contraparte que pudieran conocer o hayan conocido con motivo de la celebración del presente contrato.

Alcance en cuanto a sistemas de inteligencia artificial

Las Partes acuerdan que las cesiones efectuadas en los anteriores apartados se realizan sin la facultad de emplear los derechos cedidos para el entrenamiento, alimentación o aprendizaje automático de ningún sistema de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robóticos, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología disruptiva relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). De tal manera que, el uso de los derechos cedidos por mor del presente Contrato para los enunciados usos constituirá un incumplimiento sustancial del mismo. El LICENCIATARIO habrá de respetar el compromiso adquirido en virtud de la anterior Estipulación en los contratos, negocios y relaciones jurídicas que mantenga con terceros, sean personas físicas o jurídicas, adoptando todas las medidas necesarias a tal fin e incluyendo, si fuese necesario, previsiones escritas en los contratos que celebre con estos terceros.

Duración del contrato

El presente contrato se concluye por un plazo de [Nº] años pudiendo prorrogarse, a voluntad de las partes y de común acuerdo por períodos anuales.

Si llegado el vencimiento del plazo inicial o de cualquiera de sus prórrogas, alguna de las partes decidiera dar por finalizado el presente contrato, deberá de comunicar su intención a la otra parte con al menos dos meses de antelación a la fecha del vencimiento a través de un medio que deje constancia de su recepción.

Responsabilidad frente a terceros

Sin perjuicio de las acciones que pudiera corresponderle entre ellas, La LICENCIANTE responderá solidariamente con el LICENCIATARIO de los daños y perjuicios ocasionados a terceras personas por defectos inherentes a la invención objeto del modelo de utilidad.

Cláusula del licenciatario más favorecido

LA LICENCIANTE se obliga a conceder al LICENCIATARIO en el futuro y durante un plazo de [Nº] años desde la extinción del presente contrato cualquier condición más favorable que pueda reconocer a otro licenciatario.

Resolución del contrato

El Contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2. Por acuerdo de las Partes por escrito.

3. La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sumisión a tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Sumisión a tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Arbitraje / Sumisión a Arbitraje sin cláusula penal en caso de no ejecución voluntaria del laudo / Sumisión a Arbitraje con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente LICENCIA DE MODELO DE UTILIDAD, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La Licenciante)

Fdo. Don [NOMBRE Y APELLIDOS]

========================================================================

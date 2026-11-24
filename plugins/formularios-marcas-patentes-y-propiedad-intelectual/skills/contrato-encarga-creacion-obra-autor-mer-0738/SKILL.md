---
name: contrato-encarga-creacion-obra-autor-mer-0738
description: "Contrato por el que se encarga la creación de una obra a su autor. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato por el que se encarga la creación de una obra a su autor

> Formulario **MER-0738** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato por el que se encarga la creación de una obra a su autor» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato por el que se encarga la creación de una obra a su autor” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-encarga-creacion-obra-autor-mer-0738`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DESCRIBIR
- [ ] DÍA
- [ ] ENTIDAD BANCARIA
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] OBJETO DEL ENCARGO
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

CONTRATO DE ENCARGO DE OBRA

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE ENCARGO DE OBRA, y a tal efecto, libremente y de común acuerdo,

EXPONEN

I. Que el AUTOR, crea y realiza obras de arte consistentes en [DESCRIBIR]

II. Que el COMITENTE es una entidad interesada en [OBJETO DEL ENCARGO]

III. Que el COMITENTE conoce la producción artística del AUTOR, así como su calidad y características, estando interesado en encargar una obra al AUTOR que entrará a formar parte del fondo artístico del COMITENTE. de conformidad con lo establecido en este documento., todo ello de acuerdo con las siguientes:

CLÁUSULAS

Objeto

Objeto

El COMITENTE encarga al AUTOR quien acepta, la realización de una obra con las siguientes características:

Condiciones de aceptación de la obra

La realización de la obra, pactada en el párrafo anterior, queda supeditada a la aprobación por parte del COMITENTE del proyecto que el AUTOR le presente, así como del presupuesto necesario para la producción de la misma.

De no ser admitido, por cualquier motivo, por el COMITENTE el proyecto referido, éste deberá abonar al artista la cantidad de [IMPORTE] euros como pago del citado proyecto, resolviéndose el presente contrato, sin que las partes nada puedan reclamarse.

Prohibición de uso de Inteligencia Artificial

El/La AUTOR/A se compromete a, en la elaboración de la Obra y en todos los materiales relacionados con la misma, no hacer uso, emplear o ayudarse de sistemas de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robóticos, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). Dicho compromiso podrá ser levantado previa conformidad de las partes por escrito cuando el uso de dicha tecnología sea testimonial.

Plazo de entrega

El AUTOR se compromete a finalizar la obra y a ponerla a disposición del COMITENTE en el plazo máximo de [PLAZO] a partir de la fecha de la firma del presente documento, es decir por todo el próximo día

En el supuesto de circunstancias especiales, ajenas al AUTOR, que hagan imposible la finalización de la obra antes del plazo previsto, como pudieran ser enfermedad, inclemencias del tiempo, la falta de materiales, éste lo deberá comunicar con quince días de antelación al COMITENTE quien deberá consentir prorrogar el plazo de entrega hasta que las circunstancias especiales hayan desaparecido.

Contraprestación económica

El precio señalado para la realización de la obra es de [IMPORTE] euros, que deberá abonarse de la siguiente forma:

• 40% a la aprobación del proyecto;

• 40% al inicio de la obra; y

• 20% restante en el momento de finalización del encargo.

Además de la cantidad pactada, irán a cuenta del COMITENTE los gastos de transporte, comida y alojamiento que se devenguen por razón de la ejecución de la obra, y que el AUTOR acredite documentalmente. De no poderse acreditar el importe del gasto, pero sí la realización del mismo se establecen los siguientes módulos:

• [IMPORTE] Euros/Km;

• [IMPORTE] Euros/por comida; y

• [IMPORTE] Euros/por día de alojamiento.

Todas las cantidades serán abonadas por medio de transferencia o ingreso bancario en la cuenta corriente titularidad del AUTOR de la que éste es titular en la entidad financiera [ENTIDAD BANCARIA] con el número

Producción de la obra

A partir de que el AUTOR lo requiera, el COMITENTE deberá proveer al AUTOR de cuanto material precise para el cumplimiento de lo pactado. Las partes acuerdan que los proveedores y profesionales que deban intervenir en la producción de la obra serán de la confianza del COMITENTE y escogidos por éste.

Derechos de autor

Con el encargo de la obra realizado en este documento no se entienden cedidos los derechos del autor sobre la misma. A efectos de lo dispuesto en el artículo 56.2 de la Ley de Propiedad Intelectual, el AUTOR manifiesta que queda excluido expresamente de la presente compraventa la transmisión del derecho de exposición pública de la obra.

Para cualquier tipo de exhibición, reproducción, comunicación pública o cesión de la obra, así como para realizar cualquier otra modalidad de explotación de la misma, el COMITENTE recabará la autorización expresa y por escrito del AUTOR o de sus representantes.

El COMITENTE se compromete a respetar escrupulosamente los derechos del autor sobre su obra, reconociendo en todo momento su autoría, obligándose a informar, cuando así sea requerido por el AUTOR, sobre la situación en la que se encuentre la obra, su localización, así como en su caso, la comunicación de la venta de la obra a los efectos legalmente previstos.

Uso de la imagen del autor

El AUTOR autoriza al COMITENTE el uso de su imagen personal, fotografía, retrato e imagen física, reproducida o generada por cualquier medio, su biografía, así como su expediente profesional, para fines de promoción, explotación y comercialización¡ de la obra a que este Contrato se refiere.

Merchandising

El AUTOR participará en los eventuales beneficios que se obtengan por las explotaciones derivadas de la obra, entendiendo por tales, cualquier elemento accesorio explotado para favorecer la comercialización y promoción de la obra audiovisual, tales como objetos de artes plásticas o aplicadas, juegos, y en general todas las aplicaciones genéricamente denominadas productos derivados, comprometiéndose las partes a suscribir un acuerdo en el que se fijen las condiciones de participación del AUTOR en los citados beneficios, que en ningún caso podrá ser inferior a [PORCENTAJE] %.

Resolución del contrato

Incumplimiento del AUTOR

Si vencido el plazo o la prórroga prevista en el pacto anterior, el AUTOR no ha realizado la obra, el COMITENTE podrá optar por rescindir el contrato y exigir la devolución de lo abonado, a excepción del primer pago realizado por el proyecto de la obra, o reclamar la finalización inmediata del encargo.

Incumplimiento del COMITENTE

Si durante la vigencia del contrato, al COMITENTE no le interesase la finalización del encargo, éste deberá abonar el total de las prestaciones económicas acordadas en el presente Contrato.

Cuando el encargo se haya acabado y el AUTOR haya puesto a disposición del COMITENTE la obra encargada y éste no ha abonado el precio pendiente de abono, podrá exigir además del pago del precio total, los intereses legales del dinero devengados desde la fecha en la que se puso a disposición del COMITENTE la citada obra y éste no procedió a abonarla.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sin cláusula penal / Sumisión a tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal / Sumisión a tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Sumisión a arbitraje / Arbitraje / Sin cláusula penal / Sumisión a Arbitraje sin cláusula penal en caso de no ejecución voluntaria del laudo / Con cláusula penal / Sumisión a Arbitraje con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE ENCARGO DE OBRA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(El Autor)

Fdo. Don [NOMBRE Y APELLIDOS]

(El Comitente)

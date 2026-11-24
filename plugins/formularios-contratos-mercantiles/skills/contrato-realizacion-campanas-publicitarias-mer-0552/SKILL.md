---
name: contrato-realizacion-campanas-publicitarias-mer-0552
description: "Contrato de realización de campañas publicitarias. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de realización de campañas publicitarias

> Formulario **MER-0552** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de realización de campañas publicitarias» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de realización de campañas publicitarias” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-realizacion-campanas-publicitarias-mer-0552`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE DE LA PARTE (17 veces)
- [ ] NÚMERO (8 veces)
- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] PRODUCTO (6 veces)
- [ ] CALLE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº (4 veces)
- [ ] PISO (4 veces)
- [ ] CARGO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] MOTIVO
- [ ] OTROS DATOS
- [ ] PERIODICIDAD
- [ ] PLAZO
- [ ] ÓRGANO
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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS:

De una parte, D [NOMBRE Y APELLIDOS], mayor de edad, provisto de D.N.I. y N. I. F. número [NÚMERO], domiciliado en Calle [CALLE], número [NÚMERO], piso [PISO], de [LOCALIDAD], que interviene en nombre y representación de la sociedad [DENOMINACIÓN SOCIAL] como [CARGO] de dicha sociedad, provista de C.I.F. número [NÚMERO] y domiciliada en Calle [CALLE], número [NÚMERO], piso [PISO], de [LOCALIDAD], que podrá ser designado a los efectos de este contrato como ANUNCIANTE,

y de otra parte, D [NOMBRE Y APELLIDOS], mayor de edad, provisto de D.N.I. y N. I. F. número [NÚMERO], domiciliado en Calle [CALLE], número [NÚMERO], piso [PISO], de [LOCALIDAD], que interviene en nombre y representación de la sociedad [DENOMINACIÓN SOCIAL] como [CARGO] de dicha sociedad, provista de C.I.F. número [NÚMERO] y domiciliada en Calle [CALLE], número [NÚMERO], piso [PISO], de [LOCALIDAD], que podrá ser designada en lo sucesivo como EMPRESA PUBLICISTA.

Ambas partes se reconocen capacidad suficiente para contratar y obligarse mediante la firma de este contrato, que prometen no impugnar, y, de común acuerdo,

EXPONEN

La empresa [DENOMINACIÓN SOCIAL] se dedica a la actividad mercantil de fabricación de [PRODUCTO], y a tal efecto ha elaborado un producto [PRODUCTO] que desea comercializar bajo la denominación

La empresa [DENOMINACIÓN SOCIAL] ejerce actividad como empresa especializada en el desarrollo de campañas de publicidad para apoyar la comercialización de [PRODUCTO]

está interesado en el desarrollo de una campaña publicitaria para la promoción de su producto [PRODUCTO] e [DENOMINACIÓN SOCIAL] tiene, asimismo, interés en hacerse cargo de dicha campaña, y a tal efecto suscriben el presente contrato de realización de publicidad, que se regirá por la legislación de general y particular aplicación, y por las siguientes

ESTIPULACIONES

encarga a [DENOMINACIÓN SOCIAL] la realización de una campaña publicitaria para la promoción del producto [PRODUCTO] que aquella fabrica, con sujeción a las siguientes directrices:

La campaña publicitaria será supervisada por [NOMBRE DE LA PARTE], quien podrá realizar las observaciones que estime pertinentes sobre aspectos circunstanciales de la misma y sin alterar el núcleo central de la creación publicitaria que desarrolle [NOMBRE DE LA PARTE], a quien incumbirá exclusivamente la aportación de las ideas publicitarias y el desarrollo de las mismas.

La campaña publicitaria tiene por objeto la inserción de anuncios en televisión/radio/vallas publicitarias/ que apoyen la comercialización del producto [PRODUCTO]

Opciones:

a.- En caso de prestación única:

La realización del producto publicitario/de la campaña se hará efectiva en un plazo no superior a [PLAZO]

b.- En caso de campaña continuada:

La duración de este contrato será de [Nº] meses/años, contados a partir de la fecha del mismo. Durante este periodo, [NOMBRE DE LA PARTE] desarrollará [Nº] un anuncio/producto con periodicidad [PERIODICIDAD] de modo que pueda emitirse/publicarse al menos una vez por

La contraprestación por la realización de la campaña publicitaria se fija en [IMPORTE] euros, que [NOMBRE DE LA PARTE] deberá pagar a [NOMBRE DE LA PARTE] del siguiente modo:

La contraprestación pactada incluye la retribución que pueda corresponder a [NOMBRE DE LA PARTE] como creador del anuncio en concepto de propiedad intelectual. De este modo, tanto la idea como su desarrollo, elementos publicitarios, eslóganes, melodías y demás rasgos identificativos de la campaña -y en consecuencia del producto publicitario- quedarán de la completa titularidad de [NOMBRE DE LA PARTE], quien podrá hacer uso de los mismos en futuras campañas, aun cuando fueren realizadas por empresa publicitaria diferente a

La creación publicitaria quedará de la íntegra y exclusiva propiedad del anunciante, sin que la empresa publicista pueda utilizar, ni en todo ni en parte, ni el resultado final ni ninguno de los componentes de la campaña, ya sean eslóganes, melodías, o cualesquiera otros componentes o elementos de la campaña, que se elaborará, en cuanto a la totalidad de su contenido, para el único y exclusivo uso de

La empresa publicitaria podrá (o, en su caso: no podrá) reseñar su autoría sobre la campaña publicitaria con estas condiciones:

Todos los gastos que genere la creación publicitaria (en su caso: incluidas retribuciones de actores o figurantes) serán de cuenta de [NOMBRE DE LA PARTE], que aportará todos los medios personales y materiales precisos hasta la completa creación del producto publicitario final, en condiciones para su publicación o emisión.

Los costes y gastos que se deriven de la inserción de los anuncios en los medios publicitarios serán satisfechos por [NOMBRE DE LA PARTE]

La creación publicitaria que ha de desarrollar [NOMBRE DE LA PARTE] se ajustará estrictamente a las disposiciones de la Ley 34/1988, de 11 de noviembre, General de Publicidad.

colaborará con la empresa encargada de la realización publicitaria, facilitando tanto información sobre cualidades del producto publicitado, como [Nº] ejemplares de dichos productos para que puedan ser empleados en la confección de los anuncios/folletos/etc.

no podrá divulgar de ninguna manera las informaciones que reciba, que deberá mantener en estricto secreto, conforme a un criterio de lealtad contractual, tanto durante la vigencia del contrato como tras la finalización del mismo. Este pacto sobre confidencialidad se extiende a cualesquiera informaciones sobre los productos o sobre las personas -incluidas las ajenas a la empresa anunciante- que [NOMBRE DE LA PARTE] pueda proporcionar a [NOMBRE DE LA PARTE] en el desarrollo de los contactos que mantengan para la prestación de información útil para la elaboración de los productos publicitarios.

El encargo de creación publicitaria que realiza [NOMBRE DE LA PARTE] a [NOMBRE DE LA PARTE] se confiere en calidad de "en exclusiva", de modo que durante la vigencia del contrato el anunciante no podrá encomendar a otras empresas publicistas la elaboración de anuncios sobre el mismo producto a que se refiere este contrato.

El presente contrato se concierta en virtud de la confianza que [NOMBRE DE LA PARTE] manifiesta tener en la capacidad creativa y en los medios materiales y personales de que dispone [NOMBRE DE LA PARTE] de modo que será esta última quien deberá hacerse cargo directamente de la elaboración de los productos publicitarios, sin subcontratar los mismos con terceros ajenos a su propia y directa organización empresarial.

se reserva el derecho de decisión final sobre el resultado de la campaña, de modo que si aquel no resulta satisfactorio podrá [OTROS DATOS]

Si [NOMBRE DE LA PARTE] decide introducir modificaciones en los productos elaborados por [ÓRGANO O PERSONA], deberá correr con todos los gastos y desembolsos que tales variaciones acarreen.

Este contrato podrá resolverse, además de por las causas generales legalmente previstas, por los siguientes motivos:

A instancia del anunciante [ÓRGANO]:

A instancia de la empresa publicista [MOTIVO]:

Se establecen las siguientes pautas indemnizatorias para el supuesto de resolución contractual:

Las partes manifiestan, y mutuamente reconocen, su condición de comerciantes, y que la contratación guarda relación con la actividad mercantil de ambos contratantes. En consecuencia, resultarán de aplicación a la interpretación y aplicación de este concreto las normas que regulan la contratación mercantil, y en particular, las del Código de Comercio y la Ley 3/2004 por la que se establecen medidas de lucha contra la morosidad en las operaciones comerciales.

Controversias

Para dirimir cualquier cuestión sobre interpretación o aplicación de este contrato las partes se someten, con renuncia a cualquier fuero especial que pudiera corresponderles, a los tribunales de la ciudad de

Y en prueba de conformidad con cuantas manifestaciones y estipulaciones se contienen en el presente documento que consta de [Nº] hojas por una sola cara, las partes lo firman en todas dichas hojas, por duplicado ejemplar y a un solo efecto, en el lugar y fecha de su encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdº: Por Fdº: Por [DENOMINACIÓN SOCIAL]
Administrador Único	Administrador Único

---
name: contrato-venta-rama-actividad-mer-0815
description: "Contrato de venta de una rama de actividad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de venta de una rama de actividad

> Formulario **MER-0815** del plugin **Traspasos de negocio, confidencialidad y acuerdos de empresa** (`formularios-traspasos-y-acuerdos-de-empresa`) · Mercantil › Otros documentos mercantiles · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de venta de una rama de actividad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de venta de una rama de actividad” para mi caso». También puedes invocarla directamente con `/formularios-traspasos-y-acuerdos-de-empresa:contrato-venta-rama-actividad-mer-0815`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-traspasos-y-acuerdos-de-empresa:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Traspasos de negocio, confidencialidad y acuerdos de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] PROVINCIA (3 veces)
- [ ] NIF/DNI (2 veces)
- [ ] NOMBRE DE LA RAMA DE ACTIVIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] ENTIDAD BANCARIA
- [ ] Nº
- [ ] NÚMERO

## Normas que cita el formulario

- art. 11 Ley Orgánica 3/2018

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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NIF/DNI]

Y de otra parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NIF/DNI]

INTERVIENEN

MANIFIESTAN

Que intervienen en la indicada representación, se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE COMPRAVENTA DE LA RAMA DE ACTIVIDAD [NOMBRE DE LA RAMA DE ACTIVIDAD] DE LA EMPRESA VENDEDORA, asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que la VENDEDORA es una empresa dedicada a las siguientes actividades: (.)

II. Que, dentro de las actividades empresariales que desarrolla, se encuentra la rama de actividad, la cual se ejerce de forma separada por la empresa, de modo que constituye una unidad económica autónoma, capaz de funcionar por sus propios medios.

III. Que la parte COMPRADORA está interesada en adquirir la citada rama de actividad, constituida por los bienes, derechos y elementos patrimoniales que se describen de forma extensa en el inventario Anexo I que se incorpora como parte integrante en el presente contrato.

IV. Que, estando interesadas ambas partes en el negocio de compraventa, encomendaron a la empresa auditora la realización de una Due Dilligence, cuyo resultado se recoge en el informe sobre el estado actual de la rama de actividad que se incorpora como Anexo II de este contrato.

V. Que, conviniendo ambas partes en concertar el contrato, otorgan a tal fin el presente CONTRATO DE COMPRAVENTA DE LA RAMA DE LA ACTIVIDAD [NOMBRE DE LA RAMA DE ACTIVIDAD] DE LA VENDEDORA, en base a las siguientes

CLÁUSULAS

PRIMERA.- OBJETO DEL CONTRATO

Por medio del presente contrato, la VENDEDORA vende a la COMPRADORA la rama de actividad de de su empresa con los bienes, derechos y elementos que constan en el inventario incorporado como Anexo I de este contrato, que la adquiere, con todos y cada uno de los elementos que la integran tales como locales, maquinaria, y marcas y patentes asociadas a su actividad, con expresión de los derechos y cargas recogidos en el citado inventario.

La venta incluye la subrogación de la COMPRADORA en los contratos en curso relativos a la rama de actividad, así como en los de seguro, los cuales se relacionan en el Anexo III que se incorpora como parte integrante de este contrato, quedando la COMPRADORA subrogada en todos los derechos y obligaciones derivados de dichos contratos.

La venta incluye asimismo la cesión de los créditos de los que la VENDEDORA es titular en esta rama de actividad, así como la asunción de las deudas derivadas de dicha rama por parte de la COMPRADORA, los cuales se relacionan en el Anexo IV que se incorpora como parte integrante de este contrato.

La COMPRADORA se subroga asimismo en la totalidad de los contratos de trabajo del personal de la rama de la actividad de la empresa, los cuales se relacionan en el Anexo V que se incorpora como parte integrante de este contrato.

Ambas partes se comprometen a realizar las gestiones, así como a otorgar los documentos públicos, oficiales y privados necesarios para materializar la venta de la rama de actividad.

SEGUNDA.- PRECIO DE LA COMPRAVENTA

El precio total de esta compraventa es de [IMPORTE] euros, más IVA.

TERCERA.- FORMA DE PAGO

El precio pactado de compraventa lo abonará la COMPRADORA de la siguiente forma:

- A la fecha de la firma del presente contrato euros, más IVA.

- El día de [DÍA] de [MES], la COMPRADORA pagará la cantidad de [IMPORTE] euros, más IVA.

- El día de [DÍA] de [MES], la COMPRADORA pagará la cantidad de [IMPORTE] euros, más IVA.

Como medio de pago, se acuerda entre las partes el uso de transferencia bancaria a la cuenta número [NÚMERO] del banco [ENTIDAD BANCARIA] de la VENDEDORA.

Por el cumplimiento de los plazos y pagos descritos, no se devengará interés alguno.

En caso de incumplimiento de los plazos de obligación de pago, se devengará un interés de demora del %, sin perjuicio de la facultad de la parte VENDEDORA de resolver el contrato.

CUARTA.- TRANSMISIÓN DE LA TITULARIDAD

La VENDEDORA, a la firma de este documento, le hace entrega material a la COMPRADORA de la unidad productiva de rama de actividad objeto de este contrato, por lo que éste declara que la ha recibido a satisfacción.

La VENDEDORA declara que la venta de la unidad productiva de rama de actividad se hace como unidad económica y que se encuentra libre de embargos, arrendamientos, prendas sin tenencia y cualquier otra limitación al derecho de dominio por parte de la VENDEDORA, tal como resulta reflejado en los ANEXOS I a V de este contrato.

La VENDEDORA se obliga a realizar las gestiones necesarias para el cambio de titularidad y la COMPRADORA se compromete, en un término de días a partir del otorgamiento de este contrato, a gestionar en su nombre todas las cuentas de servicios donde opera el negocio, las licencias, patentes, y todos los demás permisos que sean necesarios para la operación del negocio.

QUINTA.- GARANTÍA Y RESPONSABILIDAD DE LA VENDEDORA

LA VENDEDORA garantiza el pleno funcionamiento de las instalaciones, así como de la maquinaria, bienes y accesorios inventariados en el Anexo I y necesarios para el desempeño de la actividad descrita durante un periodo máximo de [Nº] meses, dentro de los cuales deberá costear aquellas reparaciones que sean necesarias para el correcto ejercicio de la actividad. No obstante lo anterior, no se considerará cubierta por la presente cláusula de garantía los supuestos de negligencia de LA COMPRADORA en la utilización, manejo y conservación de local, maquinarias, bienes y accesorios anteriormente referidos.

La VENDEDORA responderá, conforme a las reglas legales aplicables, tanto por evicción, como por vicios o defectos ocultos de los bienes, derechos y elementos transmitidos a la COMPRADORA.

SEXTA.- SUBROGACIÓN EN LOS CONTRATOS DE TRABAJO

La COMPRADORA se subroga de manera expresa respecto a las relaciones contractuales de carácter laboral del personal de la VENDEDORA, según la relación del Anexo V, con el mecanismo de sucesión de empresa, previsto en el artículo 44 del Texto Refundido del Estatuto de los Trabajadores.

En consecuencia, la COMPRADORA queda subrogada en los derechos y obligaciones laborales y de la Seguridad Social de la VENDEDORA, incluyendo los compromisos de pensiones y, en general, cuantas obligaciones en materia de protección social complementaria hubiera adquirido

SÉPTIMA.- FICHEROS DE DATOS PERSONALES

Por el presente contrato se transmiten a la COMPRADORA los ficheros de datos personales de clientes y proveedores de los que es responsable la VENDEDORA con la finalidad de continuar la actividad económica y realizar las gestiones necesarias a este efecto. De conformidad a lo dispuesto en el art. 14 del Reglamento (UE) 2016/679, de 27 de abril de 2016, y art. 11 de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, la COMPRADORA deberá facilitar la información prevista en los citados preceptos para los supuestos en que los datos personales no se hayan obtenido del interesado

OCTAVA.- PACTO DE CONDICIÓN RESOLUTORIA

Ambas partes pactan expresamente que, para el supuesto de falta de pago de todo o una parte del precio aplazado por parte de la COMPRADORA, la VENDEDORA podrá resolver el contrato y recuperar la rama de actividad, siempre y cuando haya requerido previamente a la COMPRADORA, mediante un acta notarial, para que, en un plazo de veinte días, efectúe el pago, con la advertencia de que, si no lo hace, se resolverá la compraventa.

Para que se aplique la condición resolutoria, la parte impagada del precio aplazado debe superar el 10 % del precio íntegro más los intereses. A estos efectos, la VENDEDORA podrá retener las cantidades pagadas por la COMPRADORA, con un máximo de la mitad de la cantidad total que haya debido percibir, de acuerdo con el contrato, hasta la fecha de la resolución

NOVENA.- OTRAS CAUSAS DE RESOLUCIÓN Y CLÁUSULA PENAL

Serán causas de resolución de la compraventa el incumplimiento grave y culpable de cualquiera de las partes de las obligaciones de este contrato.

En el caso de incumplimiento por la COMPRADORA por falta de pago, en los plazos pactados, de cualquiera de las cantidades que se han aplazado hasta el otorgamiento de la escritura, la VENDEDORA podrá optar por resolver el contrato, previo requerimiento de pago de dichas cantidades conforme al pacto recogido en la cláusula octava, o por el cumplimiento.

En este caso, si la VENDEDORA decidiera resolver la compraventa, tendrá derecho a retener como propias las cantidades entregadas hasta la fecha por la COMPRADORA, hasta el límite del diez por ciento (10%) del precio de la compraventa, en concepto de cláusula penal que sustituye a la indemnización de daños y perjuicios.

Si la VENDEDORA optara por exigir el estricto cumplimiento del contrato, tendrá derecho a una indemnización consistente en la cantidad que resulte de aplicar al importe adeudado el interés de demora del 8% sobre las cantidades impagadas en concepto de cláusula penal que sustituye a indemnización de daños y perjuicios.

En el caso de incumplimiento por la VENDEDORA de sus obligaciones relativas a la entrega de la rama de actividad, incluida la prohibición de competencia, la COMPRADORA podrá optar por la resolución del contrato o por el cumplimiento.

Si la COMPRADORA opta por la resolución del contrato, la VENDEDORA, además de devolver las cantidades entregadas por la COMPRADORA, le indemnizará con una cantidad equivalente al cinco por ciento del precio de la compraventa, en concepto de cláusula penal que sustituye a la indemnización de daños y perjuicios.

Si la COMPRADORA opta el cumplimiento, la VENDEDORA le indemnizará con la suma de [IMPORTE] euros diarios desde la fecha pactada hasta el día de la entrega efectiva de la finca, en concepto de cláusula penal que sustituye a indemnización de daños y perjuicios, tal como se conviene en la cláusula cuarta de este contrato.

DÉCIMA.- PROHIBICIÓN DE COMPETENCIA

La VENDEDORA se compromete expresamente a no competir con la COMPRADORA en la rama de actividad objeto de este contrato, ya sea directa o indirectamente, por sí mismos, o a través de terceros, conjunta o individualmente desde la firma de este contrato, durante un plazo de diez años.

Ambas partes manifiestan que la prohibición de competencia es una obligación esencial en aras a que la COMPRADORA pueda consolidar la clientela y fondo de comercio transmitido en este negocio en la rama de actividad objeto de este contrato.

Por tanto, la VENDEDORA no podrá realizar actividades y/o actuaciones que directa o indirectamente coincidan en el mercado o puedan coincidir con las actividades y/o productos de la rama de actividad objeto de este contrato, ni por cuenta propia ni ajena, ya sea de forma directa, como de forma indirecta, en calidad de asesoramiento, consultoría, suministro, ni cualquier otra figura análoga o similar.

UNDÉCIMA.- CONFIDENCIALIDAD

Ambas partes se comprometen a no divulgar la información y documentación confidencial referente a la otra parte de la que hayan tenido conocimiento por razón del presente contrato, salvo las indispensables para su cumplimiento, y a mantenerla en secreto.

A estos efectos, ambas partes expresamente se comprometen a no suministrar, ceder o vender ningún tipo de información respecto del desarrollo y productos de la actividad de la otra parte.

DUODÉCIMA.- ELEVACIÓN DEL DOCUMENTO A PÚBLICO, COMUNICACIONES E INSCRIPCIONES

Ambas partes convienen la elevación de este documento a escritura pública, a requerimiento de cualquiera de ellas, así como a realizar todas las comunicaciones, inscripciones y demás actuaciones necesarias para la plena eficacia de este contrato, ante cualesquiera organismos y empresas, públicas y privadas, así como ante las personas trabajadoras y la clientela.

DÉCIMOTERCERA.- OBLIGACIONES FISCALES, GASTOS E IMPUESTOS

A partir del momento de la firma de este contrato, la COMPRADORA asume todas las obligaciones fiscales derivadas del desarrollo de la actividad económica de la rama objeto de este contrato.

Los gastos e impuestos derivados de este contrato serán satisfechos por cada una de las partes conforme a las normas aplicables en la legislación mercantil, civil y tributaria.

DÉCIMOCUARTA.- NOTIFICACIONES

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato y sus Anexos I, II, III, IV y V, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

Fdo.: Fdo.:

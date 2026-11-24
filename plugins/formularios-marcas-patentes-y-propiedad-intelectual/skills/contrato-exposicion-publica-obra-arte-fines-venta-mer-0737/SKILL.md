---
name: contrato-exposicion-publica-obra-arte-fines-venta-mer-0737
description: "Contrato de exposición pública de una obra de arte con fines de venta. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de exposición pública de una obra de arte con fines de venta

> Formulario **MER-0737** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de exposición pública de una obra de arte con fines de venta» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de exposición pública de una obra de arte con fines de venta” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-exposicion-publica-obra-arte-fines-venta-mer-0737`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FECHA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] PLAZO
- [ ] TIPO DE OBRAS
- [ ] TIPO DE SEGURO

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

CONTRATO DE EXHIBICIÓN PÚBLICA DE OBRA PARA VENTA

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE EXHIBICIÓN PÚBLICA, y a tal efecto, libremente y de común acuerdo,

EXPONEN

I. Que el AUTOR crea y realiza obras de [TIPO DE OBRAS], la calidad y las características de las cuales son bien conocidas por la GALERÍA)

II. Que la GALERÍA está interesada en proceder a la exhibición y venta de la obra que se dirá durante el plazo de [PLAZO], a la que el AUTOR presta su autorización de conformidad con lo establecido en este documento., todo ello de acuerdo con las siguientes:

CLÁUSULAS

Objeto

El AUTOR entrega en este acto a la GALERÍA, que las recibe, las piezas que figuran en el Anexo I, comprometiéndose ésta a cuidarlas con la debida diligencia, manteniéndolas en perfecto estado de conservación y lugar adecuado para su exhibición.

Las referidas piezas las recibe la GALERÍA para ser exhibidas públicamente en la exposición que se celebrará en el espacio que ésta tiene destinado al efecto, sito en [LOCALIDAD] durante los días

El AUTOR autoriza, expresamente, a la GALERÍA para que ésta pueda vender las obras objeto de exhibición según el precio estipulado en el Anexo II del presente Contrato.

Duración

La duración del presente contrato será desde la fecha del mismo hasta el próximo día [FECHA], fecha en la que la GALERÍA deberá entregar en el lugar que el AUTOR indique las piezas que no hayan sido vendidas.

En ningún caso podrá entenderse prorrogado el contrato, salvo autorización expresa y por escrito del AUTOR.

Llegado el día pactado para la devolución de las obras sin que la GALERÍA las haya devuelto al AUTOR, éste podrá optar entre exigir a la GALERÍA su devolución inmediata o el pago de las obras no devueltas al precio acordado en el Anexo II de este contrato.

Contraprestación

El AUTOR y la GALERÍA han fijado de común acuerdo el precio mínimo por el cual la GALERÍA ha de ofertar cada una de las obras, excluido el I.V.A. Los precios de las piezas pactados son inamovibles, salvo autorización expresa y por escrito de la AUTOR.

Sin perjuicio de lo señalado en el párrafo anterior, el AUTOR autoriza a la GALERÍA a ofrecer un descuento de hasta un [PORCENTAJE] % sobre los precios mínimos, en las ventas que puedan hacerse a museos o a otras galerías.

Una vez la GALERÍA ha realizado y cobrado la venta, podrá quedarse en concepto de comisión, un % sobre el precio de venta, (sin incluir el IVA) y seguidamente, en el plazo de [Nº] días abonará al AUTOR el % restante

Obligaciones del autor

El AUTOR se compromete y obliga a:

a) Proporcionar a la GALERÍA la información que necesite sobre la obra realizada

b) Colaborar en los actos que la GALERÍA realice para promocionar su obra.

c) Intervenir en el asesoramiento para proceder al montaje y desmontaje de la exposición.

Obligaciones de la galería

La GALERÍA se compromete y obliga a:

a) Recoger la obra entregada en este mismo acto y conservarla en perfecto estado de conservación.

b) Abonar los gastos de embalaje, traslado, transporte y montaje de la obra, así como los de desmontaje de la obra y su posterior embalaje y transporte al lugar en el que artista haya designado para proceder a su devolución.

c) Realizar las gestiones más idóneas para conseguir como más ventas mejor, y obtener la cotización más alta de la obra. Los gastos de todo tipo que comporte la actividad de la GALERÍA irán a su cargo, sin que en ningún caso pueda repercutirlos al AUTOR.

d) Realizar la venta de las obras.

e) Hacerse responsable de cualquier tipo de desperfecto, sustracción o desaparición que pueda sufrir la obra, incluso por caso de fuerza mayor, y asimismo en el caso que no hubiera culpa ni negligencia por su parte. Para ello, deberá abonar una prima anual de seguro que cubra tales contingencias por el valor de las obras pactadas con el AUTOR, designando a este como beneficiario.

f) Proporcionar en todo momento al AUTOR información sobre las gestiones para la venta y promoción de las obras. El AUTOR se reserva el derecho a exigir de la GALERÍA, que estas gestiones se planteen y enfoquen con su colaboración y consentimiento previo.

g) Proporcionar en todo momento al AUTOR información sobre la localización de las obras y sobre las transacciones que se hayan realizado o se tenga intención de realizar.

h) Liquidar en el plazo de [Nº] días desde la venta de la obra las comisiones al AUTOR, así como el I.V.A que por las mismas se devengue.

i) Utilizar los proveedores habituales del AUTOR en todo aquello que afecte físicamente, directamente, a la obra (enmarcado, iluminación, montaje) para su exposición.

Derechos de autor

El AUTOR no cede ningún derecho de autor sobre la obra objeto del presente contrato, salvo los que expresamente se transmiten en este documento que son la exhibición física de la obra en el espacio de arte señalado en el Pacto Primero de este documento y la venta de la misma en las condiciones pactadas en este contrato.

Para cualquier otro tipo de exhibición, reproducción, comunicación pública o cesión de la obra, así como para realizar cualquier otra modalidad de explotación de la misma, la GALERÍA deberá recabar la autorización expresa y por escrito del AUTOR o de sus representantes.

La GALERÍA se compromete a respetar, escrupulosamente, los derechos de autor sobre la obra objeto de este contrato, reconociendo, en todo momento, su autoría, obligándose a informar, cuando así sea requerido por el AUTOR sobre la situación en la que se encuentre la obra, su localización, así como en su caso, la comunicación de la venta de la obra a los efectos legalmente previstos.

Seguros

El GALERISTA asumirá el pago del seguro [TIPO DE SEGURO] para cubrir la rotura, pérdida de la pieza o cualquier otro siniestro que se produzca una vez salga la pieza del taller del AUTOR.

La pieza se asegurará por el valor de venta de la obra y el beneficiario será en todo caso el AUTOR.

Transporte

El transporte de la obra a la Galería correrá a cargo del GALERISTA.

Catálogos e invitaciones

Catálogos

El contenido del catálogo promocional de a exposición deberá pactarse entre la GALERÍA y el AUTOR. Los costes de diseño, maquetación, fotocomposición e impresión irán a cargo de la GALERÍA.

El AUTOR tendrá derecho a quedarse gratuitamente un número no inferior al % de los catálogos publicados por motivo de la exposición en caso de que sea una exposición individual y un mínimo de [Nº] ejemplares, si se trata de una exposición o un acontecimiento colectivo. La GALERÍA está obligada a hacer la difusión y distribución adecuada de los catálogos de la exposición..

Invitaciones

El diseño y el contenido de las invitaciones será pactado por ambas partes, si bien el AUTOR respetará el diseño o estilo determinado de la GALERÍA.

El AUTOR proporcionará a la GALERÍA la lista de sus clientes o personas que desea invitar, así como la autorización para que las direcciones puedan pasar a formar parte de la base de datos de la galería, siempre, lógicamente, cumpliendo escrupulosamente, la Ley de Protección de Datos.

Marcos y dispositivos de montaje

Los gastos de enmarcado de la obra, así como los originados por otro dispositivo de exposición (peanas, vitrinas, cajas de luz, iluminación, proyectores) y en general todos los gastos de montaje que se originen con motivo de una exposición o de cualquier otra forma de exhibición de la obra del artista, irán a cargo de la GALERÍA.

Uso de la imagen del autor

El AUTOR autoriza a la GALERÍA el uso de su imagen personal, fotografía, retrato e imagen física, reproducida o generada por cualquier medio, su biografía, así como su expediente profesional, para fines de promoción, explotación y comercialización¡ de la obra a que este Contrato se refiere.

Opción de compra

El AUTOR reconoce a la GALERÍA, por el plazo de [Nº] meses a contar desde la firma del presente contrato, el derecho de opción de compra de la obra objeto de cesión, fijando el precio de la misma en el importe de [IMPORTE] Euros.

Para proceder al ejercicio de tal opción, la GALERÍA deberá comunicar expresamente y por escrito al AUTOR su voluntad de compra de la obra objeto de este contrato, procediendo a entregar al AUTOR el importe fijado en el párrafo anterior.

Transcurridos el plazo fijado quedará extinguido el derecho de opción de compra a favor de la GALERÍA.

Merchandising

El AUTOR participará en los eventuales beneficios que se obtengan por las explotaciones derivadas de la obra, entendiendo por tales, cualquier elemento accesorio explotado para favorecer la comercialización y promoción de la obra audiovisual, tales como objetos de artes plásticas o aplicadas, juegos, y en general todas las aplicaciones genéricamente denominadas productos derivados, comprometiéndose las partes a suscribir un acuerdo en el que se fijen las condiciones de participación del AUTOR en los citados beneficios, que en ningún caso podrá ser inferior a [PORCENTAJE] %.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sin cláusula penal / Sumisión a tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal / Sumisión a tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Sumisión a arbitraje / Arbitraje / Sin cláusula penal / Sumisión a Arbitraje sin cláusula penal en caso de no ejecución voluntaria del laudo / Con claúsula penal / Sumisión a Arbitraje con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE EXHIBICIÓN PÚBLICA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(El Autor)

Fdo. Don [NOMBRE Y APELLIDOS]

(El Galerista)

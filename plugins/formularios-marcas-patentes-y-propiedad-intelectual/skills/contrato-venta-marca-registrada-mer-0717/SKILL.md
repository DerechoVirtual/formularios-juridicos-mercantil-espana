---
name: contrato-venta-marca-registrada-mer-0717
description: "Contrato de venta de una marca registrada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de venta de una marca registrada

> Formulario **MER-0717** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de venta de una marca registrada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de venta de una marca registrada” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-venta-marca-registrada-mer-0717`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] Nº (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] AÑO
- [ ] CLASE
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] ÓRGANO ARBITRAL

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

II. MANIFIESTAN

1. Que el Vendedor es único propietario y legítimo titular de la marca núm. [Nº], registrada para la clase [CLASE] del Nomenclátor Internacional, concedida por la OEPM el día [FECHA] y de la solicitud de marca núm. [Nº], presentada para productos o servicios de la clase 4ª del Nomenclátor el día [FECHA]

2. Que el Vendedor está interesado en formalizar la venta de la marca y de la solicitud de marca al Comprador, en los términos y condiciones que figuran en este contrato.

3. Que el Comprador está interesado, y así lo tiene convenido con el Vendedor, en adquirir la marca y la solicitud de marca en los términos y condiciones previstos en este contrato.

4. Que ambas partes se reconocen capacidad legal suficiente para obligarse mutuamente y convienen la celebración del presente Contrato de Compraventa de Marca de conformidad con las condiciones que se recogen en las siguientes:

CLÁUSULAS

Objeto y consentimiento

El Vendedor vende y transmite al Comprador la marca y la solicitud de marca descritas (o que figuran en el Anexo 1 de este Contrato). El Comprador adquiere la titularidad de las mismas a través del otorgamiento de este contrato.

Precio

1. El precio de la presente compraventa es, en conjunto y para la totalidad de las marcas, de [IMPORTE] A este precio hay que añadir el IVA correspondiente.

2. El pago del precio se efectuará del siguiente modo:

A) En el momento de la formalización del presente Contrato se pagará un importe de [IMPORTE], mediante transferencia bancaria o cualquier otro medio acordado por las Partes.

B) La parte del precio restante se pagará el día [FECHA]

3. La Parte del precio que queda aplazada devengará, a partir del día [FECHA], un interés anual calculado al tipo del [Nº] por ciento. El cálculo de intereses se verificará anual- mente sobre la base del precio pendiente de pago, y dichos intereses serán satisfechos en los mismos plazos y condiciones previstos para el pago del precio en el apartado anterior.

4. No obstante lo dispuesto en el párrafo 2, el Comprador podrá en todo momento y si así lo estima conveniente pagar anticipadamente el precio, total y parcialmente.

Formalización

El presente Contrato de cesión será formalizado mediante escritura pública, otorgada ante Notario elegido de común acuerdo entre las Partes, y en un plazo máximo de quince días naturales a contar desde la fecha indicada en el encabezamiento.

(El presente Contrato de cesión será formalizado en documento privado, comprometiéndose las Partes contratantes a realizar cuantos trámites fueran necesarios para lograr la inscripción de la cesión en la Oficina Española de Patentes y Marcas).

Gastos

Todos los gastos, derechos e impuestos, etc., que se ocasionen con motivo del otorgamiento de este contrato serán satisfechos por las partes según Ley.

Garantías

El Vendedor manifiesta y garantiza:

1. Respecto a la marca inscrita:

A) Que en el momento de la firma del presente Contrato es el legítimo titular y único propietario, sin restricción alguna, de la marca descrita, y que así figura en la sección de marcas de la OEPM.

B) Que en el momento de la firma del presente Contrato la marca se encuentra libre de todo tipo de trabas, embargos, cargas, gravámenes, retenciones y cualesquiera derechos a favor de terceros.

C) Que en la fecha de firma del presente Contrato el Vendedor no ha otorgado ninguna licencia o derecho de uso a favor de tercero sobre la marca.

D) Que la marca se encuentra plenamente en vigor, es plenamente eficaz y oponible frente a terceros y se encuentra al corriente de los pagos de impuestos, tasas y, en general, cualesquiera pagos previstos por la legislación vigente, no debiéndose cantidad alguna por tales conceptos.

E) Que no tiene conocimiento de que a la firma de este Contrato existan oposición, reclamación judicial o extrajudicial o, en general, procedimiento alguno que afecte a la marca y que tampoco tiene conocimiento de que la explotación de dicha marca por parte del Comprador pueda infringir o infrinja alguna marca, patente, secreto empresarial o cualquier otro derecho de un tercero.

2. Respecto a la solicitud de marca:

A) El Vendedor garantiza que ha sido debidamente presentada para su tramitación, a su nombre, en la OEPM.

B) Que está libre de toda carga, que no ha sido objeto de cesión o licencia y que no le consta que infrinja o pueda infringir los derechos correspondientes a un tercero.

C) El Vendedor no otorga ninguna otra garantía al Comprador y, en particular, éste no podrá exigir el reembolso de cantidad alguna en el caso de que dicha solicitud de marca no prosperara por causas que no fueran conocidas por el Vendedor o que hubieran sido reveladas al Comprador antes de la firma de este Contrato.

3. Indemnización.

El Vendedor se obliga frente al Comprador a defenderle y a indemnizarle íntegramente de y frente a todos los daños y perjuicios, pérdidas, gastos, costes, reclamaciones, procedimientos y acciones que se produzcan como consecuencia de cualquier inexactitud o incumplimiento de alguna de las garantías u obligaciones que se sostienen en los apartados anteriores o, en general, en este Contrato, o que se produzcan como consecuencia de reclamaciones fundamentadas en hechos o circunstancias anteriores a la firma de este Contrato.

Obligaciones

1. A partir de la firma del presente Contrato, el Vendedor se abstendrá de otorgar cualesquiera derechos, reales o personales, licencias o contratos sobre la marca y la solicitud de marca a favor de cualquier tercero, así como de usar personalmente la marca transmitida. No renunciará a la solicitud de marca. Y, en general, no llevará a cabo ninguna acción que impida o perjudique la plena eficacia de la transmisión de la propiedad de la marca y de la solicitud de marca a que se refiere este Contrato.

2. El Vendedor se compromete a defender en juicio y fuera de él la marca hasta que no sea inscrito el Comprador como titular registral en la OEPM.

3. El Comprador se obliga a pagar todos los gastos que genere el mantenimiento de la marca desde la fecha del otorgamiento del presente contrato, aun cuando no figure como titular registral de la misma.

Ley aplicable y jurisdicción

Este Contrato se regirá y será interpretado de conformidad con la legislación española. Las partes acuerdan que todo litigio, conflicto, cuestión o reclamación que resulte de la ejecución o interpretación del presente Contrato o esté directa o indirectamente relacionada con el mismo se resolverá definitivamente mediante arbitraje, siendo competente [ÓRGANO ARBITRAL], y encomendando al mismo la designación de árbitros y la administración del arbitraje. Asimismo las partes hacen constar expresamente su compromiso de cumplir el laudo arbitral que se dicte.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y EN PRUEBA DE CONFORMIDAD, las partes, después de leer detenidamente el documento lo ratifican y firman por duplicado, ambos con idéntica fuerza en la ciudad y fecha indicadas al inicio.

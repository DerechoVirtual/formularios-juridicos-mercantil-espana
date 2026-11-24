---
name: condiciones-generales-venta-empresa-mer-0592
description: "Condiciones generales de venta de una empresa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Condiciones generales de venta de una empresa

> Formulario **MER-0592** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Condiciones generales de venta de una empresa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Condiciones generales de venta de una empresa” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:condiciones-generales-venta-empresa-mer-0592`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº

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

Ámbito de aplicación

Las presentes condiciones generales de venta serán aplicables a cualquier contrato de venta o entrega entre las partes, salvo que éstas hayan acordado otra cosa por escrito.

Las ofertas y presupuestos realizados por LA VENDEDORA no serán vinculantes para la misma, entendiéndose perfeccionado el contrato de compraventa únicamente cuando LA VENDEDORA confirme por escrito un pedido.

Las presentes condiciones de venta sólo podrán ser modificadas por acuerdo escrito entre las partes, por lo que serán inválidas en este sentido las cláusulas o condiciones que figuren impresas o manuscritas, en los pedidos, cartas u otros documentos emitidos por LA COMPRADORA.

La modificación por LA VENDEDORA de las presentes condiciones de venta no afectará a contratos ya perfeccionados.

Todas las compras futuras de mercancías de LA VENDEDORA, en ausencia de un acuerdo expreso en sentido contrario, estarán sujetas a los presentes términos y condiciones generales.

Lugar

Salvo que LA VENDEDORA aceptase otro en la confirmación de pedido, el lugar de realización de todas las obligaciones contractuales será [LUGAR] (lugar), y la entrega de las mercancías se realizará en el almacén de LA VENDEDORA.

Plazo de entrega

El plazo de entrega empezará a computarse tan pronto como el pedido sea confirmado por LA VENDEDORA. El plazo de entrega se considerará completado cuando la entrega esté lista para despachar en el lugar acordado.

El plazo de entrega será razonablemente ampliado si por motivos ajenos a la voluntad y control de LA VENDEDORA se impiden el cumplimiento con la fecha de entrega.

Igualmente, el plazo de entrega será ampliado si LA COMPRADORA cambia el pedido original o se retrasa en sus obligaciones contractuales, especialmente si LA COMPRADORA ha retrasado la entrega de los documentos necesarios o ha retrasado los pagos acordados.

Precio

Todos los precios deberán ser considerados como netos, en [IMPORTE] euros, sin ninguna deducción de cualquier tipo, salvo pacto en contrario.

Los precios podrán ser modificados, teniendo LA COMPRADORA la facultad de desistir del contrato si aquél no le conviniera en un plazo de 7 días siguientes a la notificación de las nuevas tarifas.

Los precios no incluyen impuestos, tasas u otras cargas, tanto de naturaleza general como especial, que serán a cargo de LA COMPRADORA a menos que se pacte otra cosa por escrito, teniendo en cuenta los Incoterms que en su caso sean de aplicación y/o las condiciones de entrega de las mercancías.

Forma de pago

Salvo pacto escrito en contrario, cada pedido se pagará al contado, sin ningún descuento y sin que se permita deducción, compensación o retención de pagos por parte de LA COMPRADORA.

Las fechas de pago acordadas deberán ser cumplidas por LA COMPRADORA incluso si el transporte o la entrega se demorasen debido a razones más allá del control de LA VENDEDORA.

Si LA VENDEDORA lo considera oportuno por la posición financiera de LA COMPRADORA, podrá solicitar las garantías que considere necesarias para asegurar el debido cumplimiento de las obligaciones contractuales de LA COMPRADORA, pudiendo entretanto suspender las entregas.

Caso de exigirse algún aval de garantía, el texto del mismo deberá acomodarse al modelo que a tal efecto facilitará LA VENDEDORA.

Intereses

Con efectos desde la fecha de pago acordada, LA COMPRADORA deberá pagar intereses sobre el valor de la cantidad debida a un % sobre [Nº] meses.

Aceptación de mercancía

LA COMPRADORA revisará y llevará a cabo el reconocimiento de las remesas, en cuanto a calidad y cantidad, en el acto mismo de la entrega. Una vez revisadas y practicado el reconocimiento de las remesas, éstas se considerarán aceptadas por LA COMPRADORA, renunciando ésta a cualquier reclamación.

Asimismo, LA COMPRADORA dispondrá de un plazo de 30 días para denunciar cuantos vicios o defectos ocultos se presenten en las remesas, transcurrido el cual perderá toda acción y derecho a reclamar por esta causa en contra de LA VENDEDORA.

Con respecto a las reclamaciones relativas al uso, venta o distribución de los productos vendidos o entregados, individualmente o en combinación con otros productos, ingredientes o embalajes, o cualquier otra queja relativa al contrato, los derechos de LA COMPRADORA y la responsabilidad de LA VENDEDORA se limitarán al cambio de tales productos o a la devolución del precio de venta, según elija LA VENDEDORA. LA COMPRADORA nunca tendrá derecho a devolver los productos aceptados o cuyo plazo para denunciar defectos haya transcurrido. La responsabilidad de LA VENDODORA nunca excederá el valor de las mercancías afectadas en el momento de la venta.

Reserva de dominio

LA VENDEDORA conservará la propiedad de las mercancías suministradas hasta la recepción completa de los pagos acordados. LA COMPRADORA autoriza a LA VENDEDORA a inscribir su reserva de propiedad en registros públicos o archivos, y estará obligado a dar cualquier firma para ello requerida.

Embalajes

LA COMPRADORA adquirirá la titularidad de los materiales de embalaje a menos que:

a) En el material de embalaje se indique que LA VENDEDORA o un tercero reclama la reserva de dominio del mismo; o

b) La hoja de pedido o los documentos que la acompañen incorporen una reserva de dominio a favor de LA VENDEDORA o un tercero.

En tales casos, se estará a lo previsto en la Condición anterior ("Reserva de dominio").

Garantía

LA VENDEDORA garantiza exclusivamente que en la fecha de entrega los productos estarán en conformidad con las especificaciones convenidas.

Los productos se venden sin posteriores garantías y sin ningún tipo de promesa por parte de LA VENDEDORA respectos a sus posibilidades de procesamiento, aplicaciones potenciales y comerciabilidad.

LA VENDEDORA será responsable de reparar o reemplazar cualquier mercancía que, antes de expirar el periodo de garantía, se pruebe que sea inutilizable debido a malos materiales, diseño defectuoso o pobre elaboración.

Si un suministro se mantiene defectuoso a pesar de su reparación o sustitución, LA VENDEDORA queda autorizada a llevarse la mercancía defectuosa contra el reembolso de los pagos recibidos.

Quedan excluidas de la garantía y responsabilidad de LA VENDODORA todas las deficiencias fuera de su control, especialmente si es como resultado del desgaste normal, falsa información de LA COMPRADORA, mantenimiento inadecuado, fallos en la observancia de las instrucciones de funcionamiento, uso de cualquier material inapropiado, influencia de una acción química o electrolítica, etc.

Si LA COMPRADORA alega que una garantía de acuerdo con las especificaciones técnicas de la mercancía no es alcanzada, la garantía sólo será válida si LA VENDEDORA tiene la oportunidad de comprobar que los parámetros garantizados no son alcanzados.

La garantía por LA VENDEDORA está sujeta al oportuno cumplimiento de las condiciones de pago acordadas con LA COMPRADORA.

Daños

Las reclamaciones de garantía y responsabilidad del cliente están exhaustivamente cubiertas por estas condiciones. Mientras no haya leyes obligatorias específicas en contrario, en ningún caso estará LA COMPRADORA autorizada a reclamaciones contractuales o extracontractuales por daños resultantes, pero no limitados a, pérdida de producción, pérdida de uso, de pedidos, de beneficio y cualquier otro daño directo, indirecto o consecuencial.

LA VENDEDORA sólo es responsable de compensar al cliente por los costes de remediar los defectos en el propio suministro.

Límite de responsabilidad

Los precios de LA VENDEDORA son elaborados y negociados sobre la base de que su responsabilidad legal máxima estará limitada. Los clientes tienen sus propios medios de limitación de riesgo, y duplicarlos sería superfluo.

LA VENDEDORA está dispuesta a negociar unos límites de responsabilidad más altos, sujetos al correspondiente incremento proporcional del precio.

Salvo acuerdo en contrario, la responsabilidad de LA VENDEDORA nunca excederá del valor de las mercancías afectadas en el momento de la venta.

LA VENDEDORA queda liberada de toda responsabilidad por encima de ese máximo, incluso si ha sido causado por su propia negligencia o incumplimiento de obligaciones, salvo en caso de fraude por parte del Vendedor.

Patentes

La venta de mercancía por LA VENDEDORA no transmitirá en ningún caso licencia alguna bajo ninguna patente relativa a los productos o a su composición, y LA COMPRADORA asume expresamente todos los riesgos de infracción de patente por razón de su uso o venta de producción, individualmente o en combinación con otros materiales o en alguna operación de elaboración en algún proceso.

Seguros

El beneficio y riesgo de los suministros pasará a LA COMPRADORA una vez estén listos para despacho en las condiciones pactadas.

En caso de que el despacho de la mercancía se retrasase por razones más allá del control de LA VENDEDORA, los suministros serán almacenados y asegurados a costa y riesgo de LA COMPRADORA. El transporte será ejecutado a coste y riesgo de LA COMPRADORA.

LA COMPRADORA será responsable de suscribir un seguro para los suministros contra cualquier tipo de riesgo.

LA VENDEDORA podrá solicitar a LA COMPRADORA fotocopia del último recibo satisfecho justificando el pago puntual de las primas correspondientes a tales seguros. Los seguros a los que se hace referencia deberán tener una duración mínima igual a la duración prevista para la ejecución del pedido.

Incumplimiento de la compradora

En caso de incumplimiento o falta de cumplimiento puntual o adecuado de cualquiera de las obligaciones de LA COMPRADORA, así como en caso de declaración de concurso de acreedores, liquidación o disolución de su empresa, LA VENDEDORA tendrá derecho a notificar la rescisión total o parcial del contrato o la suspensión de su ejecución en todo o en parte. Ello se realizará mediante notificación fehaciente, sin necesidad de ulterior advertencia de incumplimiento o intervención judicial, y sin que LA VENDEDORA deba responder por los daños, sin perjuicio de cuantos otros derechos asistan a LA VENDEDORA.

Tan pronto como se produzca cualquiera de las circunstancias antes mencionadas, todas las reclamaciones que LA VENDEDORA tenga frente a LA COMPRADORA se convertirán en pagaderas inmediatamente.

Si LA COMPRADORA no realiza el pago puntualmente o en su totalidad, al primer requerimiento de LA VENDEDORA deberá devolver los productos no pagados.

En caso de no ser devueltos dichos productos por LA COMPRADORA, LA VENDEDORA, sin perjuicio de sus demás derechos y acciones, estará legitimado para recuperar los productos vendidos sin necesidad de nuevo requerimiento, notificación o intervención judicial.

Fuerza mayor

"Fuerza Mayor" significa a los efectos del presente contrato la existencia de cualquier contingencia, circunstancia o causa que esté más allá del control de la parte que la invoca, incluyendo, pero no limitándolo a las siguientes circunstancias: imposición o sumisión a una ley, regulación, decreto, orden o solicitud de cualquier autoridad (nacional, estatal, autonómica, provincial o municipal), confiscación, motín, guerra, disturbios, incendios, inundaciones, terremotos, tormentas, explosiones, huelgas, cierres, parada de maquinaria o de fábrica, imposibilidad de conseguir materias primas, equipos, gasóleo o transporte.

Si por Fuerza Mayor cualquiera de las Partes no puede cumplir alguna obligación del presente Contrato distinta a la de pago del precio, dicha Parte queda exonerada de su cumplimiento, siempre que notifique a la otra parte indicando el comienzo y la naturaleza de la situación de Fuerza Mayor. La Parte que invoque la Fuerza Mayor deberá enviar notificación inmediata tras la finalización de la causa que motive la Fuerza Mayor.

LA VENDEDORA no será responsable frente a LA COMPRADORA por ninguna pérdida o daño derivado del incumplimiento o de la falta de cumplimiento puntual o total de sus obligaciones por causa de fuerza mayor.

Esta cláusula es aplicable a LA VENDEDORA y a LA COMPRADORA. No obstante los anteriores apartados de este artículo, si a LA COMPRADORA le afecta la Fuerza Mayor no será relevada de ninguna de sus obligaciones de aceptar y pagar los envíos hechos con anterioridad al recibo por parte de l Vendedor de la notificación por escrito de LA COMPRADORA de la situación de Fuerza Mayor; tampoco LA COMPRADORA podrá invocar la causa de Fuerza Mayor para retrasar el pago de la cantidades adeudadas.

Si concurre causa de Fuerza Mayor, LA VENDEDORA tendrá derecho a distribuir, en la forma que considere razonable, las cantidades de productos útiles entre sus clientes y sus propios requerimientos.

Compensación

LA VENDEDORA, así como todas las compañías que forman parte del mismo grupo que ella, tiene derecho a compensar cualquier suma que le adeude LA COMPRADORA o cualquiera de las compañías que forman parte del mismo grupo que ella, contra cualquier suma pagadera a LA COMPRADORA.

Cesión

Ninguna de las partes cederá el contrato sin el consentimiento escrito de la otra parte, con la sola excepción de que LA VENDEDORA puede ceder el contrato, en todo o en parte, a cualquiera de las compañías que formen parte de su mismo grupo empresarial.

Catálogos y documentos

Los datos contenidos en los catálogos y documentos técnicos serán vinculantes sólo si está explícitamente estipulado como tal en los mismos.

Todos los documentos facilitados por LA VENDEDORA a LA COMPRADORA deberán ser considerados como propiedad exclusiva del primero, debiendo ser considerados confidenciales y no pudiendo ser cedidos, bajo ningún concepto ni por ningún título a terceros, ni copiados ni usados sin el previo consentimiento y por escrito del Vendedor.

Si no se realiza el pedido, todos los catálogos y demás documentos entregados deberán ser devueltos inmediatamente al Vendedor.

Confidencialidad y Protección de datos

En cumplimiento de los dispuesto en la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garnatía de los Derechos Digitales y el Real Decreto-ley 5/2018, de 27 de julio, los datos de carácter personal facilitados por LA COMPRADORA formarán parte del fichero de clientes de LA VENDEDORA, cuyos fines son el mantenimiento de la relación contractual, el control y gestión de las ventas y sus correspondientes cobros. LA VENDEDORA tratará dichos datos con la máxima confidencialidad, y se compromete a no utilizarlos con un fin distinto a aquel para el que han sido recabados, así como a conservarlos con las debidas medidas que garanticen su seguridad y eviten su alteración, pérdida, tratamiento o acceso no autorizados.

LA VENDEDORA se compromete a guardar secreto profesional respecto de los referidos datos personales, incluso una vez finalizada la relación contractual.

LA COMPRADORA autoriza a LA VENDEDORA a conservar sus datos durante un periodo de cinco años una vez cumplida la prestación contractual.

LA COMPRADORA tiene la posibilidad de ejercitar los derechos de acceso, rectificación, cancelación y oposición dirigiendo una comunicación por escrito a la atención del Responsable de Protección de Datos de [DENOMINACIÓN SOCIAL] (nombre de la empresa), [DIRECCIÓN] (dirección).

Separabilidad

Las presentes condiciones se considerarán separables, y si alguna de ellas fuera inválida por cualquier razón, el resto conservará su validez con toda su fuerza y efecto.

Idioma

En caso de discrepancia entre textos en castellano y textos en cualquier otra lengua relacionados con la venta de la mercancía, prevalecerá el texto en castellano.

Fuero

La presente relación se regirá por la legislación española. Las partes renuncian expresamente a cualquier otro foro o jurisdicción a los que pudiesen tener derecho y acuerdan someter a los tribunales de [LOCALIDAD] cualquier diferencia o litigio derivados de la validez, interpretación, cumplimiento o ejecución de las Condiciones Generales de Venta, así como de los actos o transacciones contempladas en las mismas.

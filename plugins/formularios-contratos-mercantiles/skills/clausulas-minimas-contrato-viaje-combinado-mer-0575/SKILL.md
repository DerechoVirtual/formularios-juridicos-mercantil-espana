---
name: clausulas-minimas-contrato-viaje-combinado-mer-0575
description: "Cláusulas mínimas del contrato de viaje combinado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Cláusulas mínimas del contrato de viaje combinado

> Formulario **MER-0575** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato de viaje combinado entre el consumidor o viajero y la agencia organizadora o minorista, con las cláusulas mínimas que deben figurar en él conforme al texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios (TRLGDCU, Real Decreto Legislativo 1/2007), libro cuarto, título IV. Se usa cada vez que una agencia contrata un viaje que combina al menos dos tipos de servicios de viaje (transporte, alojamiento, etc.).

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Cláusulas mínimas del contrato de viaje combinado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Cláusulas mínimas del contrato de viaje combinado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:clausulas-minimas-contrato-viaje-combinado-mer-0575`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MES (2 veces)
- [ ] AUTORIDAD COMPETENTE Y DATOS DE CONTACTO
- [ ] CONDICIONES DE LA FINANCIACIÓN
- [ ] DOMICILIO Y DATOS DE CONTACTO DE LA ENTIDAD GARANTE
- [ ] ENTIDAD GARANTE
- [ ] ITINERARIO DEL VIAJE CONTRATADO
- [ ] NOMBRE DEL PROGRAMA O FOLLETO DEL ORGANIZADOR, PÁGINA Y REFERENCIA
- [ ] SOLICITUDES ESPECIALES
- [ ] TELÉFONO DE URGENCIA

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

- Al principio del formulario: el original citaba el artículo 151.4.b) y c) de la «LGDU/2007»; se entiende referido al TRLGDCU (RDLeg 1/2007). Comprobar el apartado exacto del artículo 151 TRLGDCU en la redacción vigente.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS SOBRE EL CONCEPTO DE VIAJE COMBINADO

El artículo 151 TRLGDCU define el viaje combinado como la combinación de, al menos, dos tipos de servicios de viaje a efectos del mismo viaje o vacación, si esos servicios:

1. Son combinados por un solo empresario, incluso a petición o según la selección del viajero, antes de que se celebre un único contrato por la totalidad de los servicios, o

2. Con independencia de la celebración de contratos distintos con diferentes prestadores de servicios de viaje, esos servicios:

i. son contratados en un único punto de venta y seleccionados antes de que el viajero acepte pagar,

ii. son ofrecidos, vendidos o facturados a un precio a tanto alzado o global,

iii. son anunciados o vendidos como «viaje combinado» o bajo una denominación similar,

iv. son combinados después de la celebración de un contrato en virtud del cual el empresario permite al viajero elegir entre una selección de distintos tipos de servicios de viaje, o

v. son contratados con distintos empresarios a través de procesos de reserva en línea conectados en los que el nombre del viajero, sus datos de pago y su dirección de correo electrónico son transmitidos por el empresario con el que se celebra el primer contrato a otro u otros empresarios con quienes se celebra otro contrato, a más tardar veinticuatro horas después de la confirmación de la reserva del primer servicio de viaje.

No se considerará viaje combinado si los servicios turísticos no representan una proporción igual o superior al veinticinco por ciento del valor de la combinación y no se anuncian o no constituyen por alguna otra razón una característica esencial de la combinación, o si solo han sido seleccionados y contratados después de que se haya iniciado la ejecución de un servicio de viaje.

El contrato de viaje combinado es el que versa sobre el conjunto del viaje combinado o, si dicho viaje se realiza con arreglo a contratos distintos, todos los contratos que regulen los servicios de viaje incluidos en él.


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

CONTRATO DE VIAJE COMBINADO

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

[IDENTIFICACIÓN DE LAS PARTES QUE SUSCRIBEN EL CONTRATO: NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL, DNI/NIE/NIF, DOMICILIO, CONDICIÓN EN LA QUE INTERVIENEN (AGENCIA ORGANIZADORA, AGENCIA MINORISTA, VIAJERO O CONSUMIDOR) Y, EN SU CASO, DATOS DE LA REPRESENTACIÓN]

HAN CONVENIDO la realización del viaje contenido en el programa o folleto [NOMBRE DEL PROGRAMA O FOLLETO DEL ORGANIZADOR, PÁGINA Y REFERENCIA] en los términos de la oferta en él especificada, con las condiciones generales que figuran asimismo en el programa o folleto y que se incorporan al presente contrato firmadas por las partes contratantes, y las condiciones particulares que a continuación se detallan.

CONDICIONES PARTICULARES

DESTINO DEL VIAJE: El destino o destinos y, en caso de fraccionamiento de la estancia, los distintos períodos y sus fechas son los que constan en la documentación definitiva del viaje que se entrega en este acto al consumidor.

MEDIO DE TRANSPORTE: El tipo de transporte (avión, tren, etc.), sus características y categoría son los que constan en la documentación del viaje que se entrega en este acto al consumidor.

FECHA DE SALIDA: En la hora y lugar que constan en la documentación del viaje que se entrega en este acto al consumidor.

FECHA DE REGRESO: En la hora y lugar que constan en la documentación del viaje que se entrega en este acto al consumidor.

ALOJAMIENTO: En el establecimiento que figura en la documentación definitiva que se entrega en este acto al consumidor, en la que, asimismo, se identifica su situación y categoría, en habitación [ELEGIR: individual / doble / triple], en régimen de [ELEGIR: sólo alojamiento / alojamiento y desayuno / media pensión (indicar si la comida cubierta es el almuerzo o la cena, y si existe posibilidad de opción) / pensión completa], indicándose [ELEGIR: que están incluidas las bebidas / que no están incluidas las bebidas] en el régimen contratado.

MÍNIMO DE PERSONAS: En la fecha de la firma del presente contrato, la realización del presente viaje combinado no está supeditada a la inscripción de un mínimo de personas.

ITINERARIO: El que consta en la oferta contenida en el programa a que se hace referencia en el encabezamiento de este contrato. (En el caso de que el itinerario del programa o folleto haya sufrido alguna modificación en los términos legalmente previstos, deberá detallarse expresamente el itinerario del viaje contratado: [ITINERARIO DEL VIAJE CONTRATADO].)

OTROS SERVICIOS INCLUIDOS EN EL PRECIO DEL VIAJE: Los especificados en la oferta contenida en el programa a que se hace referencia en el encabezamiento de este contrato y, en su caso, los incluidos en la documentación definitiva que se entrega en este acto al consumidor.

SOLICITUDES ESPECIALES REALIZADAS POR EL CONSUMIDOR Y ACEPTADAS POR LA AGENCIA ORGANIZADORA O MINORISTA: [SOLICITUDES ESPECIALES]

PRECIO, SUPLEMENTOS Y PRECIO TOTAL: Precio base: [IMPORTE]. Suplementos: [IMPORTE]. Precio total: [IMPORTE].

Estos precios han sido calculados en base a los tipos de cambio, tarifas de transporte, coste del carburante y tasas e impuestos aplicables en esta fecha. Cualquier variación del precio de los citados elementos podrá dar lugar a la revisión del precio final del viaje, tanto al alza como a la baja, en los importes estrictos de las variaciones de precio aludidas. Estas modificaciones serán notificadas por escrito al consumidor. En ningún caso se revisará, al alza, el precio del viaje en los 20 días inmediatamente anteriores a la fecha de salida.

EL PAGO DEL PRECIO total del presente viaje combinado se ha realizado en la agencia minorista contra la entrega de los bonos y documentación final del viaje, a la firma del presente contrato. [OPCIONAL — si ha lugar] (En el supuesto de existir financiación del precio, deberán hacerse constar sus condiciones: [CONDICIONES DE LA FINANCIACIÓN].)

OBLIGACIÓN DE COMUNICAR TODO INCUMPLIMIENTO EN LA EJECUCIÓN DEL CONTRATO: El consumidor está obligado a comunicar todo incumplimiento en la ejecución del contrato, preferentemente «in situ» o, en otro caso, a la mayor brevedad posible, por escrito o en cualquier otra forma en que quede constancia, al organizador o al minorista y, en su caso, al prestador del servicio de que se trate.

Si no se subsanaran en un plazo razonable establecido por el viajero, éste podría hacerlo y solicitar el reembolso de los gastos necesarios asumidos. Este reembolso deberá ser abonado en un plazo no superior a 14 días naturales después de poner fin al contrato.

PRESCRIPCIÓN DE ACCIONES: El plazo para reclamar por el incumplimiento o cumplimiento defectuoso del presente contrato prescribe a los dos años desde el momento en que la acción pudo ser ejercitada. Se informa al consumidor de la conveniencia de que conserve en su poder el programa o folleto al que se hace referencia en este contrato, el presente contrato y la documentación facilitada por la agencia, a efectos de prueba, ante la eventualidad de ulteriores reclamaciones.

CONFIRMACIÓN DE LAS RESERVAS: A la firma del presente contrato se ha producido la confirmación de las reservas del viaje.

CESIÓN DE VIAJE: El viajero podrá ceder el viaje a otra persona, pero esto deberá ser comunicado con una antelación de al menos siete días naturales al inicio del viaje combinado y la persona a la que lo ceda deberá reunir todas las condiciones previstas para este contrato. El cedente del contrato y el cesionario responderán solidariamente de la cantidad pendiente de pago del precio acordado, así como de cualquier comisión, recargo u otros costes adicionales derivados de la cesión. El organizador o, en su caso, el minorista informará al cedente acerca de los costes efectivos de la cesión.

DERECHO DE RESCISIÓN DEL CONTRATO: El viajero podrá resolver el contrato antes del inicio del viaje. En este caso, el empresario podrá establecer una penalización y la recuperación de los costes que haya asumido, y sean justificables, durante el proceso de contratación y por las reservas anuladas.

En circunstancias excepcionales, si en el lugar de destino o sus inmediaciones existen graves problemas de seguridad que puedan afectar al viaje, los viajeros podrán poner fin al contrato antes de su inicio sin pagar ninguna penalización.

Ante cambios sustanciales en algunas de las características principales de los servicios o necesidades especiales contratadas, el viajero podrá decidir si acepta los cambios o resuelve el contrato de viaje sin penalización. Si la ejecución del viaje se ve afectada sustancialmente por la no prestación de servicios, el consumidor también podrá poner fin al contrato sin penalización. Si el empresario incrementa el precio más de un 8%, el viajero podrá poner fin al contrato sin penalización. Si el número de personas inscritas fuera inferior al mínimo especificado en el contrato, el organizador o minorista podrá cancelar el contrato reembolsando al viajero la totalidad de los pagos realizados y notificándoselo de acuerdo con los plazos estipulados.

DERECHO DE DESISTIMIENTO: El viajero dispone de un plazo de 14 días naturales para ejercer su derecho de desistimiento sin necesidad de justificación cuando se haya contratado el viaje fuera del establecimiento mercantil, por ejemplo, si se ha realizado en línea. En tal caso tiene derecho a que se le devuelvan las cantidades que haya pagado en un plazo máximo de 14 días naturales.

GARANTÍA: Los organizadores y minoristas deberán constituir una garantía que se activará gratuitamente con el fin de responder con carácter general al disfrute del viaje combinado y los servicios de viaje vinculados; especialmente para el reembolso de los pagos anticipados, el traslado de vuelta de los viajeros a su lugar de salida u otro punto acordado y, en caso necesario, para la financiación del alojamiento previo a la repatriación.

INFORMACIÓN ADICIONAL

REPRESENTANTE LOCAL DEL ORGANIZADOR O MINORISTA U ORGANISMOS LOCALES QUE PUEDEN PRESTAR AYUDA AL CONSUMIDOR EN CASO DE DIFICULTADES: Nombre, dirección y teléfono que figuran en la documentación definitiva que se entrega al consumidor en este acto. En su caso, número de teléfono de urgencia: [TELÉFONO DE URGENCIA].

GARANTÍA EN CASO DE INSOLVENCIA: Nombre de la entidad garante del cumplimiento de la ejecución del contrato de viaje combinado: [ENTIDAD GARANTE]. Datos de contacto, incluida su dirección completa: [DOMICILIO Y DATOS DE CONTACTO DE LA ENTIDAD GARANTE]. Cuando proceda, nombre de la autoridad competente designada a tal fin y sus datos de contacto: [AUTORIDAD COMPETENTE Y DATOS DE CONTACTO].

[OPCIONAL — incluir si procede] VIAJES Y ESTANCIAS DE MENORES EN EL EXTRANJERO: El nombre, dirección y teléfono en el que se puede establecer un contacto directo con el menor desplazado o los responsables de su estancia «in situ» figuran en la documentación definitiva que se entrega al consumidor en este acto.

SEGUROS: El consumidor podrá suscribir un contrato de seguro, a su exclusivo cargo, que cubra los gastos de cancelación o anulación por el consumidor, o un contrato de asistencia que cubra los gastos de repatriación o traslado al lugar de origen, en caso de accidente, enfermedad o fallecimiento.

ZONAS GEOGRÁFICAS DE RIESGO: Además de la información que facilita, en su caso, la agencia, se informa al consumidor de que el Ministerio de Asuntos Exteriores proporciona información sobre recomendaciones específicas según destino a través de Internet (sitio web oficial del Ministerio) o por cualquier otro medio.

CLÁUSULAS OPCIONALES QUE PUEDEN INCORPORARSE AL CONTRATO

[OPCIONAL — incluir si procede] Las partes renuncian expresamente a someterse a los Tribunales de Arbitraje de Transporte.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Firma de la agencia: [FIRMA]

Firma del consumidor o viajero: [FIRMA]

---
name: informacion-normalizada-previa-contratos-productos-mer-0551
description: "Información normalizada previa para contratos de productos vacacionales de larga duración. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Información normalizada previa para contratos de productos vacacionales de larga duración

> Formulario **MER-0551** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Información normalizada previa para contratos de productos vacacionales de larga duración» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Información normalizada previa para contratos de productos vacacionales de larga duración” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:informacion-normalizada-previa-contratos-productos-mer-0551`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- El modelo no tiene campos marcados: Claude te preguntará lo que necesite según el caso.

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

Parte 1:

Identidad, domicilio y estatuto jurídico del comerciante o comerciantes que serán parte en el contrato:

Breve descripción del producto:

Naturaleza y contenido exactos del derecho o derechos:

Período exacto durante el cual podrá ejercerse el derecho objeto del contrato y, si es necesario, su duración:

Fecha a partir de la cual el consumidor podrá ejercer el derecho objeto del contrato:

Precio que deberá pagar el consumidor por la adquisición del derecho o derechos, incluido todo coste recurrente que previsiblemente vaya a soportar el consumidor como consecuencia de su derecho a disfrutar del alojamiento, del viaje y de cualesquiera productos y servicios conexos que se especifican:

Calendario de pago escalonado en el que se fijan plazos de igual cuantía para cada año de duración del contrato y fechas en que deben pagarse los plazos:

Después del primer año, los importes posteriores podrán ajustarse para garantizar que se mantiene el valor real de dichos plazos, por ejemplo para tener en cuenta la inflación.

Reseña de los costes obligatorios adicionales impuestos en virtud del contrato; tipo de costes e indicación de los importes respectivos (por ejemplo, cotizaciones anuales):

Resumen de los principales servicios de que puede disfrutar el consumidor (por ejemplo, estancias en hotel y vuelos con descuento):

¿Están incluidos en los costes indicados anteriormente?

En caso negativo, especifíquese lo que está incluido y lo que debe pagarse aparte (por ejemplo: estancia de tres noches incluida en la cotización anual, cualquier otro alojamiento deberá pagarse por separado):

¿Se ha adherido el comerciante a uno o más códigos de conducta y, en caso afirmativo, dónde puede o pueden localizarse?:

Parte 2:

Información general:

— El consumidor tiene derecho a desistir del presente contrato, sin necesidad de justificación alguna, en un plazo de catorce días naturales a partir de la fecha de celebración del contrato o de cualquier contrato preliminar vinculante, o a partir de la fecha de su recepción si éste es posterior.

— Durante ese plazo de desistimiento, se prohíbe todo pago de anticipos por el consumidor. La prohibición afecta a cualquier contrapartida, incluido el pago, la constitución de garantías, la reserva de dinero en cuentas, el reconocimiento explícito de deuda, etc. Incluye no sólo los pagos al comerciante, sino también a terceros.

— El consumidor tiene derecho a poner término al contrato, sin incurrir en penalización alguna, notificándolo al comerciante en un plazo de catorce días naturales a partir de la recepción de la solicitud de pago correspondiente a cada plazo anual.

— El consumidor no soportará costes ni obligaciones distintos de los que se especifican en el contrato.

— De conformidad con el Derecho internacional privado, el contrato podrá regirse por una legislación distinta de la del Estado miembro en que el consumidor tenga su residencia o domicilio habitual y los posibles litigios podrán remitirse a órganos jurisdiccionales distintos de los del Estado miembro en que el consumidor tenga su residencia o domicilio habitual.

Firma del consumidor:

Parte 3:

Información adicional a la que tiene derecho el consumidor y lugar concreto en que puede obtenerse (por ejemplo, la sección correspondiente de un folleto general) si no se facilita a continuación:

1) INFORMACIÓN SOBRE LOS DERECHOS ADQUIRIDOS

— una descripción adecuada y correcta de los descuentos existentes para futuras reservas, ilustrada con una serie de ejemplos de ofertas recientes,

— información sobre las restricciones a que está sometida la capacidad del consumidor de utilizar los derechos, como la disponibilidad limitada de las ofertas que se adjudican al primer cliente o los límites de tiempo en que están vigentes los descuentos especiales o debidos a promociones específicas.

2) INFORMACIÓN SOBRE LA RESCISIÓN DEL CONTRATO

— cuando proceda, información sobre las modalidades de rescisión de contratos accesorios y consecuencias de dicha rescisión,

— condiciones de rescisión del contrato, consecuencias de la misma e información sobre la responsabilidad del consumidor por todo coste que pueda derivarse de dicha rescisión.

3) INFORMACIÓN ADICIONAL

— indicación de la lengua o lenguas que podrán utilizarse para la comunicación con el comerciante relativa al contrato, por ejemplo en relación con el tratamiento de las solicitudes de información y las reclamaciones,

— cuando proceda, la posibilidad de recurrir a un medio de resolución extrajudicial de litigios.

Acuse de recibo de la información:

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Firma del consumidor:

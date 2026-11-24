---
name: informacion-normalizada-previa-contratos-mer-0549
description: "Información normalizada previa para contratos de aprovechamiento por turno de uso turístico. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Información normalizada previa para contratos de aprovechamiento por turno de uso turístico

> Formulario **MER-0549** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Información normalizada previa para contratos de aprovechamiento por turno de uso turístico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Información normalizada previa para contratos de aprovechamiento por turno de uso turístico” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:informacion-normalizada-previa-contratos-mer-0549`.
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

Breve descripción del producto (por ejemplo, descripción del bien inmueble):

Naturaleza y contenido exactos del derecho o derechos:

Período exacto durante el cual podrá ejercerse el derecho objeto del contrato y, si es necesario, su duración:

Fecha a partir de la cual el consumidor podrá ejercer el derecho objeto del contrato:

Si el contrato se refiere a un bien específico que se halla en construcción, fecha en que el alojamiento y los servicios/las instalaciones estarán terminados/disponibles:

Precio que deberá pagar el consumidor por la adquisición del derecho o derechos:

Reseña de los costes obligatorios adicionales impuestos en virtud del contrato; tipo de costes e indicación de los importes respectivos (por ejemplo, contribuciones anuales, otras contribuciones recurrentes, impuestos especiales, impuestos locales):

Resumen de los principales servicios de los que puede disfrutar el consumidor (por ejemplo, electricidad, agua, mantenimiento, recogida de basuras) e indicación de los importes que deberá pagar por dichos servicios:

Resumen de las instalaciones de las que puede disfrutar el consumidor (por ejemplo, piscina o sauna):

¿Están incluidas en los costes indicados anteriormente?

En caso negativo, especifíquese lo que está incluido y lo que debe pagarse aparte:

¿Es posible afiliarse a un sistema de intercambio?

En caso afirmativo, indíquese el nombre del sistema de intercambio:

Indicación de los costes derivados de la afiliación o del intercambio:

¿Se ha adherido el comerciante a uno o más códigos de conducta y, en caso afirmativo, dónde puede o pueden localizarse?:

Parte 2:

Información general:

— El consumidor tiene derecho a desistir del presente contrato, sin necesidad de justificación alguna, en un plazo de catorce días naturales a partir de la fecha de celebración del contrato o de cualquier contrato preliminar vinculante, o a partir de la fecha de la recepción de dichos contratos si ésta es posterior.

— Durante ese plazo de desistimiento, se prohíbe todo pago de anticipos por el consumidor. La prohibición afecta a cualquier contrapartida, incluido el pago, la constitución de garantías, la reserva de dinero en cuentas, el reconocimiento explícito de deuda, etc. Incluye no sólo los pagos al comerciante, sino también a terceros.

— El consumidor no soportará costes ni obligaciones distintos de los que se especifican en el contrato.

— De conformidad con el Derecho internacional privado, el contrato podrá regirse por una legislación distinta de la del Estado miembro en que el consumidor tenga su residencia o domicilio habitual y los posibles litigios podrán remitirse a órganos jurisdiccionales distintos de los del Estado miembro en que el consumidor tenga su residencia o domicilio habitual.

Firma del consumidor:

Parte 3:

Información adicional a la que tiene derecho el consumidor y lugar concreto en que puede obtenerse (por ejemplo, la sección correspondiente de un folleto general) si no se facilita a continuación:

1) INFORMACIÓN SOBRE LOS DERECHOS ADQUIRIDOS

— condiciones que rigen el ejercicio del derecho objeto del contrato en el territorio del Estado o Estados miembros en los que estén situados el bien o los bienes de que se trata e información sobre si se han cumplido esas condiciones o, en caso contrario, las condiciones que quedan por cumplir,

— en caso de que el contrato prevea derechos de ocupación de un alojamiento seleccionado de entre un conjunto de alojamientos, información sobre las restricciones a que está sometida la capacidad del consumidor de utilizar cualquier alojamiento de dicho conjunto en cualquier momento.

2) INFORMACIÓN SOBRE LOS BIENES

— en caso de que el contrato se refiera a un bien inmueble específico, una descripción precisa y detallada del bien y de su ubicación; en caso de que el contrato se refiera a varios bienes (complejos turísticos), una descripción apropiada de los bienes y de su ubicación; en caso de que el contrato se refiera a un alojamiento que no sea un bien inmueble, una descripción apropiada del alojamiento y de sus instalaciones,

— los servicios (por ejemplo, electricidad, agua, mantenimiento, recogida de basuras) de los que puede o podrá disfrutar el consumidor, y las condiciones de tal disfrute,

— cuando proceda, las instalaciones comunes, como piscinas, saunas, etc., a las que el consumidor tiene o podría tener acceso en su momento y las condiciones de este acceso.

3) REQUISITOS ADICIONALES PARA LOS ALOJAMIENTOS EN CONSTRUCCIÓN (si procede)

— el estado de terminación del alojamiento y de los servicios que lo hacen completamente operativo (conexiones de gas, electricidad, agua y teléfono) y cualesquiera instalaciones de que podrá disfrutar el consumidor,

— plazo para la terminación del alojamiento y de los servicios que lo hacen completamente operativo (conexiones de gas, electricidad, agua y teléfono) y una estimación razonable del plazo para la terminación de cualesquiera instalaciones de que podrá disfrutar el consumidor,

— el número del permiso de construcción y el nombre y la dirección completa de la autoridad o autoridades competentes,

— una garantía relativa a la terminación del alojamiento o una garantía relativa al reembolso de cualquier pago efectuado en caso de que no se termine y, si procede, las condiciones que rigen el funcionamiento de tales garantías.

4) INFORMACIÓN SOBRE LOS COSTES

— una descripción precisa y adecuada de todos los costes asociados al contrato de aprovechamiento por turno de bienes de uso turístico; la forma en que los costes se asignarán a los consumidores y cómo y cuándo podrán incrementarse dichos costes; el método para el cálculo de la suma correspondiente a las cargas relativas a la ocupación del bien, las cargas legales obligatorias (por ejemplo, impuestos y contribuciones) y los gastos generales de carácter administrativo (por ejemplo, gestión, mantenimiento y reparaciones),

— cuando proceda, información sobre la existencia de cargas, hipotecas, gravámenes o cualquier otra anotación registral que grave el derecho al alojamiento.

5) INFORMACIÓN SOBRE LA RESCISIÓN DEL CONTRATO

— cuando proceda, información sobre las modalidades de rescisión de contratos accesorios y consecuencias de dicha rescisión,

— condiciones de rescisión del contrato, consecuencias de la misma e información sobre la responsabilidad del consumidor por todo coste que pueda derivarse de dicha rescisión.

6) INFORMACIÓN ADICIONAL

— información sobre la forma en que se organizan el mantenimiento y las reparaciones del bien, así como su administración y gestión, incluida la posibilidad de que el consumidor influya y participe en las decisiones relativas a estas cuestiones y las modalidades de esta participación,

— información sobre si es posible o no afiliarse a un sistema de reventa de los derechos contractuales, información sobre el sistema pertinente e indicación de los costes relacionados con la reventa por medio de dicho sistema,

— indicación de la lengua o lenguas que podrán utilizarse para la comunicación con el comerciante relativa al contrato, por ejemplo en relación con las decisiones de gestión, el incremento de los costes y el tratamiento de las solicitudes de información y las reclamaciones,

— cuando proceda, la posibilidad de recurrir a un medio de resolución extrajudicial de litigios.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Acuse de recibo de la información:

Firma del consumidor:

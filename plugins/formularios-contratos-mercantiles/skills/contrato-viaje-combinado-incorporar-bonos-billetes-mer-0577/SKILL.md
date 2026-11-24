---
name: contrato-viaje-combinado-incorporar-bonos-billetes-mer-0577
description: "Contrato de viaje combinado para incorporar a los bonos o billetes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de viaje combinado para incorporar a los bonos o billetes

> Formulario **MER-0577** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de viaje combinado para incorporar a los bonos o billetes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de viaje combinado para incorporar a los bonos o billetes” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-viaje-combinado-incorporar-bonos-billetes-mer-0577`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (3 veces)
- [ ] DATOS DEL VIAJE
- [ ] DENOMINACIÓN DEL VIAJE
- [ ] OTRAS CONDICIONES
- [ ] PETICIONES ESPECIALES

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

Las partes abajo firmantes convienen en la realización del viaje [DENOMINACIÓN DEL VIAJE] contenido en el programa/folleto que se identifica al final de este contrato, en los términos de la oferta en él especificada, con las condiciones generales que figuran, asimismo, en el programa/ folleto y que se incorporan al presente contrato firmadas por las partes contratantes, y las condiciones particulares que a continuación se detallan.

El presente contrato de viaje combinado está integrado por este documento, suscrito por las partes contratantes y los bonos-billetes adjuntos, cuyos números se reflejan al final de este contrato, de los que se entregan al consumidor dos ejemplares, uno de los cuales queda en poder del consumidor al concluir el viaje.

CONDICIONES PARTICULARES

1ª [DATOS DEL VIAJE].

2ª El resto de los servicios contratados son los especificados en la oferta

contenida en el programa/folleto que se referencia al pie y, en su caso, los incluidos en los bono-billetes adjuntos. El itinerario es el que consta en dicha oferta.

3ª La fecha de salida, hora y lugar y la fecha de regreso, hora y lugar figuran, asimismo, en dichos bono-billetes.

4ª Solicitudes especiales realizadas por el consumidor y aceptadas por la agencia organizadora o minorista son las siguientes [PETICIONES ESPECIALES]

5ª La realización del presente viaje combinado no está supeditada a la inscripción de un mínimo de personas.

6ª Precio [IMPORTE], suplementos [IMPORTE], precio total [IMPORTE] El precio ha sido abonado en su totalidad a la firma del presente contrato, estando, asimismo, confirmadas las reservas. Estos precios han sido calculados en base a los tipos de cambio, tarifas de transporte, coste del carburante y tasas e impuestos aplicables en esta fecha. Cualquier variación del precio de los citados elementos podrá dar lugar a la revisión del precio final del viaje, tanto al alza como a la baja, en los importes estrictos de las variaciones de precios aludidas. En ningún caso se revisará, al alza, el precio del viaje en los 20 días inmediatamente anteriores a la fecha de salida.

7ª El consumidor está obligado a comunicar todo incumplimiento en la ejecución del contrato -preferentemente «in situ» o, en otro caso, a la mayor brevedad posible- por escrito o en cualquier otra forma en que quede constancia, al organizador o al minorista y, en su caso, al prestador del servicio de que se trate.

En el caso de que las soluciones arbitradas por la Agencia -Organizador o minorista- no sean satisfactorias para el consumidor, éste dispondrá del plazo de un mes para reclamar ante la Agencia minorista o el organizador, siempre a través de aquélla. La Agencia minorista o el organizador dispondrán de cuarenta y cinco días naturales para dar respuesta a la reclamación planteada por el consumidor, plazo que comenzará a contarse a partir del día siguiente a la presentación de la reclamación ante la Agencia minorista.

8ª El plazo para reclamar por el incumplimiento o cumplimiento defectuoso del presente contrato prescribe a los dos años desde el momento en que la acción pudo ser ejercitada. Se informa al consumidor de la conveniencia de que conserve en su poder el programa/folleto al que se hace referencia en este contrato, el presente contrato y la documentación facilitada por la Agencia, a efectos de prueba, ante la eventualidad de ulteriores reclamaciones.

9ª El Nombre, dirección y teléfono del representante local del organizador o minorista o organismos locales que pueden prestar ayuda al consumidor en caso de dificultades, figuran en la contraportada de los bono-billetes adjuntos, así como, en su caso, el número de teléfono de urgencia. Asimismo, en el caso de estancias de menores en el extranjero el nombre, dirección y teléfono en el que se puede establecer un contacto directo con el menor desplazado o los responsables de su estancia «in situ», figuran en dichos bonos.

El consumidor podrá suscribir un contrato de seguro, a su exclusivo cargo, que cubra los gastos de cancelación o anulación por el consumidor o un contrato de asistencia que cubra los gastos de repatriación o traslado al lugar de origen, en caso de accidente, enfermedad o fallecimiento.

10ª Zonas geográficas de riesgo: Además de la información que facilita la Agencia, en su caso, se informa al consumidor que el Ministerio de Asuntos Exteriores facilita información sobre recomendaciones específicas según destino a través de Internet (http:// www.mae.es) o por cualquier otro medio.

11ª [OTRAS CONDICIONES].

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

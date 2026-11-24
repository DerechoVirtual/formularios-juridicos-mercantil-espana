---
name: transporte-viajeros-carretera-contrato-mer-0573
description: "Transporte de viajeros por carretera (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Transporte de viajeros por carretera (contrato)

> Formulario **MER-0573** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Transporte de viajeros por carretera (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Transporte de viajeros por carretera (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:transporte-viajeros-carretera-contrato-mer-0573`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MES (3 veces)
- [ ] ÓRGANO O PERSONA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LUGAR (2 veces)
- [ ] ACTO O RESOLUCIÓN
- [ ] LUGAR DE DESTINO
- [ ] LUGAR DE ORIGEN
- [ ] MATRÍCULA
- [ ] NOMBRE DEL NOTARIO
- [ ] NÚMERO
- [ ] ÓRGANO ADMINISTRATIVO

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

REUNIDOS

De una parte la [DENOMINACIÓN SOCIAL] con domicilio en [LOCALIDAD] representada por [ÓRGANO O PERSONA]

Y de otra, la Empresa de Transportes [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD], que en lo sucesivo se denominará el Transportista, representada por [ÓRGANO O PERSONA], debidamente autorizado por dicha sociedad según poder otorgado ante el Notario D [NOMBRE DEL NOTARIO], con fecha

Ambas partes, con capacidad jurídica bastante, y sus representantes con poderes suficientes y adecuados para obligar a sus representados, otorgan y convienen este contrato de transporte discrecional de viajeros con arreglo a las siguientes

ESTIPULACIONES

Objeto del contrato

Por el presente contrato el Transportista se compromete y obliga frente a [ACTO O RESOLUCIÓN], al alquiler de su vehículo matrícula [MATRÍCULA], con capacidad para 50 pasajeros sentados, sin incluir el conductor, con tarjeta de transporte núm [NÚMERO], expedida por [ÓRGANO O PERSONA], para la realización de un viaje desde [LUGAR DE ORIGEN] a [LUGAR DE DESTINO], el día [DÍA] de [MES] de [AÑO], con regreso al día siguiente al punto de partida.

Reglamentación del transporte

2.1. Los servicios prestados por el transportista están sometidos a las disposiciones contenidas en el presente contrato y, en su defecto, a las normas del Código de comercio (arts. 349 y ss.) y cualesquiera otra ley que le sea aplicable.

Precio

3.1. El precio objeto de este contrato se determinará de acuerdo con las tarifas aprobadas al efecto por [ÓRGANO ADMINISTRATIVO] y que se unen como Anexo a este documento.

Condiciones de pago

4.1.

Ejecución del transporte

5.1. El transportista se compromete a ejecutar el transporte con la diligencie razona- ble, sin que se determinen horas precisas para el comienzo o terminación del mismo.

5.2. Los pasajeros deberán presentarse en el lugar designado y a la hora preestable- cida por el transportista, y si no se hubiese fijado hora con antelación suficiente a la hora de salida del autobús que les permita cumplimentar los trámites de la misma. El transportista no es responsable de las pérdidas o gastos que se ocasionen al pasajero por su falta de cumplimiento de esta disposición.

Responsabilidad del transportista

6.1. Por daños a los pasajeros en sus personas: El Transportista no responderá de los daños sufridos por los pasajeros en sus personas cuando los mismos procedan de caso fortuito, fuerza mayor o culpa exclusiva de la propia víctima.

6.2. Por daños a los equipajes transportados: El transportista no responderá por los daños sufridos por los equipajes transportados a menos que el pasajero a quien deba hacerse la entrega le presente la oportuna reclamación inmediatamente después de descubrirse el daño y, lo más tarde, dentro de los siete días siguientes a la fecha de la entrega. Toda reclamación deberá formularse por escrito y cursarse dentro de los plazos antedichos.

Prescripción de acciones

7.1. Todo derecho de acción contra el transportista por daños prescribirá a menos que se ejercite dentro del plazo de dos años, contados desde la fecha de llegada a destino, desde la fecha en que el autobús debiera haber llegado o desde la fecha en que se interrumpió el transporte.

Tribunales competentes

8.1. Ambas partes, con expresa renuncia al fuero que pudiera corresponderles, acuerdan someterse a los Tribunales de Justicia de [LOCALIDAD] respecto a cualquier discrepancia que pudiera surgir en la interpretación y cumplimiento del presente contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

El presente contrato se extiende y firma por duplicado en [LUGAR], a [DÍA], de [MES], de [AÑO].

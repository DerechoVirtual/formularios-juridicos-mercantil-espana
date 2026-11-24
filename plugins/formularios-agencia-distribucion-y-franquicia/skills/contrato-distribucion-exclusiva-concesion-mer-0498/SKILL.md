---
name: contrato-distribucion-exclusiva-concesion-mer-0498
description: "Contrato de distribución en exclusiva o concesión. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de distribución en exclusiva o concesión

> Formulario **MER-0498** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato mercantil de distribución de bienes en exclusiva, mediante el cual la empresa fabricante de los mismos concede a la distribuidora los derechos de distribución en exclusiva de esos productos. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del contrato, así como los derechos y obligaciones de cada una de las partes.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de distribución en exclusiva o concesión» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de distribución en exclusiva o concesión” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-distribucion-exclusiva-concesion-mer-0498`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] CANTIDAD DE EXISTENCIAS
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] MARCA/MODELO
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº
- [ ] PRODUCTOS

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

Modelo de contrato mercantil de distribución de bienes en exclusiva, mediante el cual la empresa fabricante de los mismos concede a la distribuidora los derechos de distribución en exclusiva de esos productos. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del contrato, así como los derechos y obligaciones de cada una de las partes.


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

En Madrid a [DÍA] de [MES] de [AÑO]

INTERVIENEN

El primero en nombre y representación de la Cía. Mercantil [DENOMINACIÓN SOCIAL], en su calidad de Consejero Delegado de la misma, cargo para el que fue designado por la Junta general de [FECHA], protocolizada ante el Notario de Madrid don [NOMBRE DEL NOTARIO] el [DÍA] de [MES] de 20 [AÑO] con el número [NÚMERO] de su protocolo, haciéndolo el segundo en su propio nombre y derecho.

Ambas partes con plena capacidad que dicen tener y mutuamente se reconocen, en el concepto en que intervienen, necesaria para el otorgamiento del presente documento y libre y espontáneamente

EXPONEN

PRIMERO.- Que la Cía. Mercantil [DENOMINACIÓN SOCIAL] (en adelante el Concedente) se dedica a la fabricación de [PRODUCTOS], que se comercializan bajo la marca [MARCA/MODELO]

SEGUNDO.- Don [NOMBRE Y APELLIDOS] (en adelante el Concesionario) dispone de la organización comercial suficiente y necesaria para comercializar y distribuir los productos del Concedente.

TERCERO.- Ambas partes han convenido un contrato de distribución exclusiva o concesión que vienen a formalizar por medio del presente documento y con sujeción a las siguientes,

ESTIPULACIONES

Objeto del contrato

Don [NOMBRE Y APELLIDOS], en la representación en que actúa de la Cía [DENOMINACIÓN SOCIAL] concede a don [NOMBRE Y APELLIDOS], que acepta, la exclusiva de venta a partir de esta fecha de los productos a que se ha hecho referencia en el exponendo primero del presente documento, en la zona de

El CONCESIONARIO, por su parte, se compromete, dentro de la zona que le ha sido asignada, a realizar la reventa de los productos del concedente, prestar los servicios postventa y de asistencia técnica de los mismos.

Duración

La duración del presente contrato será de [Nº] años, prorrogables tácitamente por períodos iguales sin necesidad de nuevo convenio entre las partes.

Si cualquiera de las partes no deseara la prórroga del contrato deberá notificarlo así a la otra en forma fehaciente con, cuando menos, tres meses de antelación a la fecha de su vencimiento.

Obligaciones del Concesionario

El concesionario se obliga a:

1. Realizar un mínimo de compras anuales del importe que por el concedente se fije para la zona que le ha sido señalada, teniendo en cuenta las circunstancias del mercado en la citada zona.

2. A llevar a cabo las ventas que realice en las condiciones establecidas por el concedente sin que, salvo autorización expresa de éste, pueda el concesionario concertar otras diferentes.

3. Mantener unas existencias medias en almacén de [CANTIDAD DE EXISTENCIAS]

4. Habilitar y mantener locales para la exposición, almacenaje y servicio técnico en la calle [CALLE] núm [NÚMERO] de [LOCALIDAD]

Los citados locales deberán reunir las condiciones que figuran en los planos y memoria que se acompañan como anexo núm. 1.

El concedente podrá inspeccionar y visitar los locales de exposición y almacén cuantas veces lo estime conveniente o necesario.

Todos los gastos e impuestos que conlleve la puesta en funcionamiento y explotación de los locales serán de cuenta y cargo del concesionario.

5. A no divulgar a terceros los conocimientos comerciales o técnicos que le fueran suministrados por el concedente.

6. No realizar dentro de la zona de su concesión, por cuenta propia o de terceros, operaciones o gestiones de cualquier tipo referidas a la venta de productos de la misma clase que aquellos que son objeto del presente contrato.

Obligaciones del concedente

El concedente se obliga a:

1. Vender al concesionario por los precios que para los mismos se establecen en las tarifas fijadas al efecto los productos a que se hace referencia en el exponendo I del presente contrato, así como las piezas de repuesto necesarias para su reparación, todo ello en la medida en que le sea solicitado por el concesionario.

2. A no realizar directamente ni a través de terceros venta alguna de los productos

señalados en el exponendo I del presente documento, dentro de la zona asignada al concesionario.

3. Auxiliar al concesionario en los aspectos técnico y comercial.

Subcontratación de minoristas

El concedente autoriza expresamente al concesionario para contratar con minoristas la distribución del producto dentro de la provincia que le ha sido asignada. Sin embargo, el concedente deberá conocer y autorizar expresamente cualquier subcontratación antes de ser llevada a cabo por el concesionario.

Utilización del nombre y la marca

El concedente autoriza expresamente al concesionario para utilizar el nombre y la marca que le corresponden, si bien tan sólo en relación con los productos que el mismo le suministre.

El concesionario someterá para su aprobación al concedente cualquier utilización que vaya a llevar a cabo del nombre y la marca de este último, ya sea en el establecimiento comercial, en los papeles, documentos, materiales de promoción, publicidad, etc., previamente a su utilización.

Vinculación entre las partes

Este contrato no supone creación de una Sociedad, asociación, joint-venture, agencia, sucursal o representación, o cualquier otro tipo similar de vinculación entre las partes.

Concedente y concesionario se mantienen jurídicamente independientes y toda acción, derecho u obligación de cada una de las partes que no estén contempladas en este contrato serán de la única y exclusiva competencia de la parte correspondiente, sin que ello afecte en forma alguna a la otra parte.

Rescisión

Procederá la rescisión del presente contrato antes del transcurso del plazo pactado en los siguientes supuestos:

1. Incumplimiento por cualquiera de las partes de las obligaciones que le corresponden en virtud de lo establecido en el presente contrato.

2. Por consecuencia de la declaración en estado de concurso de cualquiera de los intervinientes.

Notificaciones

A los efectos de oír notificaciones las partes señalan los siguientes domicilios:

Sumisión a arbitraje

Las partes intervinientes con renuncia expresa de su fuero propio o del que pudiera corresponderles, en cuantas cuestiones o litigios se susciten, con motivo de la interpretación, aplicación o cumplimiento del presente contrato, se someten para su resolución a arbitraje de la Cámara de Arbitraje de la Sociedad Española de Arbitraje, que tendrá lugar de acuerdo con su reglamento y estatutos, comprometiéndose al cumplimiento de la decisión que recaiga en el mismo.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad dejan redactado el presente documento en el contenido del cual se afirman y ratifican firmándolo por triplicado y a un solo efecto en lugar y fecha indicados en el encabezamiento.

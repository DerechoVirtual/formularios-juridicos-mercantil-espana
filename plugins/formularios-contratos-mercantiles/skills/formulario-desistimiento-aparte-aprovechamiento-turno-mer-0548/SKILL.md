---
name: formulario-desistimiento-aparte-aprovechamiento-turno-mer-0548
description: "Formulario de desistimiento aparte para aprovechamiento por turno y productos vacacionales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Formulario de desistimiento aparte para aprovechamiento por turno y productos vacacionales

> Formulario **MER-0548** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Formulario normalizado de desistimiento, en documento aparte, que el comerciante debe incluir en los contratos de aprovechamiento por turno de bienes de uso turístico, de adquisición de productos vacacionales de larga duración, de reventa y de intercambio (Ley 4/2012, de 6 de julio). Recoge la información sobre el derecho de desistimiento, la prohibición de anticipos y el modelo de notificación de desistimiento.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Formulario de desistimiento aparte para aprovechamiento por turno y productos vacacionales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Formulario de desistimiento aparte para aprovechamiento por turno y productos vacacionales” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:formulario-desistimiento-aparte-aprovechamiento-turno-mer-0548`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] FIRMA (2 veces)
- [ ] DOMICILIO
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y DIRECCIÓN DEL COMERCIANTE

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

NOTAS DE AYUDA

El artículo 12 de la Ley 4/2012, de 6 de julio, regula el derecho de desistimiento por el consumidor de los diferentes contratos regulados en esa Ley, un derecho que podrá ejercitarse sin justificación alguna y que dejará sin efecto el contrato.

El artículo 10 de la misma Ley, titulado "Advertencia sobre el derecho de desistimiento y prohibición de pago de anticipos", dispone que, antes de la celebración del contrato, en la forma prevista en el artículo 9, el empresario pondrá explícitamente en conocimiento del consumidor la existencia del derecho de desistimiento y la duración del plazo para ejercerlo, así como la prohibición del pago de anticipos durante dicho plazo, contemplada en el artículo 13.

El artículo 11, relativo a la forma y el contenido del contrato, dispone en su apartado 4 que las cláusulas contractuales correspondientes al derecho de desistimiento y a la prohibición del pago de anticipos serán firmadas aparte por el consumidor, y que el contrato incluirá, asimismo, un formulario normalizado de desistimiento en documento aparte, según figura en el anexo V de la Ley.


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

FORMULARIO NORMALIZADO DE DESISTIMIENTO

DERECHO DE DESISTIMIENTO

El consumidor tiene derecho a desistir del presente contrato en un plazo de catorce días naturales sin necesidad de justificación.

El derecho de desistimiento comienza el [FECHA] (a cumplimentar por el comerciante antes de entregar el formulario al consumidor).

Si el consumidor no ha recibido el presente formulario, el plazo de desistimiento comenzará a contar cuando el consumidor haya recibido el formulario, pero vencerá en cualquier caso transcurrido un año y catorce días naturales a contar desde el de la celebración del contrato o de cualquier contrato preliminar vinculante o el de la recepción posterior del documento contractual.

Si el consumidor no ha recibido toda la información exigida, el plazo de desistimiento comenzará a contar cuando el consumidor haya recibido dicha información, pero vencerá en cualquier caso transcurridos tres meses y catorce días naturales a contar desde el de la celebración del contrato o de cualquier contrato preliminar vinculante si en ese momento el consumidor recibió el documento contractual, o el de la recepción posterior de dicho documento.

Para ejercer el derecho de desistimiento, el consumidor lo notificará al comerciante mediante un soporte duradero (por ejemplo, una carta enviada por correo postal o un correo electrónico), al nombre y la dirección que se indican a continuación. El consumidor podrá utilizar el presente formulario, aunque no es obligatorio.

Si el consumidor se acoge al derecho de desistimiento, no podrá imputársele coste alguno.

PROHIBICIÓN DEL PAGO DE ANTICIPOS

Durante el plazo de desistimiento se prohíbe todo pago de anticipos por el consumidor. La prohibición afecta a cualquier contrapartida, incluido el pago, la constitución de garantías, la reserva de dinero en cuentas, el reconocimiento explícito de deuda, etc.

Incluye no solo los pagos al comerciante, sino también a terceros.

NOTIFICACIÓN DE DESISTIMIENTO

Destinatario (nombre y dirección del comerciante): [NOMBRE Y DIRECCIÓN DEL COMERCIANTE]

Por la presente le notifico/notificamos que decido/decidimos desistir del contrato [ELEGIR: de aprovechamiento por turno de bienes de uso turístico / de adquisición de producto vacacional de larga duración / de reventa / de intercambio] (táchese lo que no proceda).

Fecha de celebración del contrato (a cumplimentar por el comerciante antes de entregar el formulario al consumidor): [FECHA]

Nombre del consumidor o consumidores (a cumplimentar por el consumidor o consumidores en caso de desistimiento mediante el presente formulario): [NOMBRE Y APELLIDOS]

Dirección del consumidor o consumidores (a cumplimentar por el consumidor o consumidores en caso de desistimiento mediante el presente formulario): [DOMICILIO]

Firma del consumidor o consumidores (únicamente si este formulario se notifica en papel): [FIRMA]

Fecha: [FECHA]

Acuse de recibo de la información:

Firma del consumidor: [FIRMA]

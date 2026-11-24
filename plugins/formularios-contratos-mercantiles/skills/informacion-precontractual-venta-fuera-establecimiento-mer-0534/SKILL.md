---
name: informacion-precontractual-venta-fuera-establecimiento-mer-0534
description: "Información precontractual en la venta fuera del establecimiento mercantil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Información precontractual en la venta fuera del establecimiento mercantil

> Formulario **MER-0534** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Información precontractual en la venta fuera del establecimiento mercantil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Información precontractual en la venta fuera del establecimiento mercantil” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:informacion-precontractual-venta-fuera-establecimiento-mer-0534`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] ENTIDAD BANCARIA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE COMERCIAL
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE FAX
- [ ] PRODUCTO
- [ ] PÁGINA WEB
- [ ] TELÉFONO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 103 TRLGDCU

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

INFORMACIÓN PRECONTRACTUAL PARA LA VENTA DE [PRODUCTO]

En cumplimiento de lo dispuesto en el art. 97 del Texto Refundido de la Ley General de Defensa de Consumidores y Usuarios, en su redacción por Ley 3/2014, de 27 de marzo, se informa al consumidor y usuario (en adelante, el CLIENTE) antes de la celebración del contrato fuera del establecimiento de los siguientes extremos en relación a su objeto:

IDENTIDAD DEL EMPRESARIO Y DATOS PERSONALES

El empresario ofertante es [NOMBRE Y APELLIDOS], que gira con el nombre comercial [NOMBRE COMERCIAL] ( en adelante, el VENDEDOR).

La dirección de su establecimiento comercial es [DIRECCIÓN], número de teléfono [TELÉFONO], número de fax [Nº DE FAX], correo electrónico [CORREO ELECTRÓNICO], pudiendo ponerse en contacto el cliente en cualquiera de las citadas direcciones.

DESCRIPCIÓN DE LAS CARACTERÍSTICAS PRINCIPALES DEL PRODUCTO Y PRECIO TOTAL DE LOS BIENES OFERTADOS

Las características principales del producto ofertado son las siguientes:

(Se describiría el producto; marca, modelo, etc.)

El precio total es de [IMPORTE] euros, que incluye impuestos, tasas y gastos de transporte, o entrega postal.

El precio final no incluye los gastos de financiación.

PROCEDIMIENTO DE PAGO

El pago se realizará a la entrega del producto, admitiéndose el pago en efectivo, por talón conformado o por tarjeta de crédito o débito.

El precio del producto puede ser financiado por la entidad financiera [ENTIDAD BANCARIA], colaboradora de la empresa vendedora. En este caso, el contrato de financiación se formalizará directamente entre el consumidor y usuario y la entidad financiera, entregando ésta previamente al consumidor y usuario la información normalizada europea del contrato de crédito al consumo, y una vez celebrado el contrato, copia del mismo.

PROCEDIMIENTO ENTREGA Y EJECUCIÓN

El empresario vendedor realizará la entrega del producto en un plazo máximo de 30 días desde la formalización del contrato de compraventa. El empresario vendedor recabará del cliente un justificante de entrega del producto en el que constará la fecha de la misma.

La entrega se realizará directamente al cliente o en el domicilio que éste designe, siendo de cuenta del vendedor los gastos de transporte.

DERECHO DE DESISTIMIENTO

El cliente tiene derecho a desistir del contrato durante un periodo de 14 días naturales desde el día de la entrega, sin necesidad de indicar el motivo.

Para ejercer el derecho de desistimiento, el cliente deberá comunicar al vendedor su decisión de desistir del contrato a través de una declaración inequívoca (por ejemplo, una carta enviada por correo postal, fax o correo electrónico).

Para cumplir el plazo de desistimiento, basta con que la comunicación relativa al ejercicio por parte del cliente de este derecho sea enviada antes de que venza el plazo correspondiente.

En caso de desistimiento, el vendedor devolverá todos los pagos recibidos del cliente, sin ninguna demora indebida y, en todo caso, a más tardar 14 días naturales a partir de la fecha en la que sea informado por el cliente de su decisión de desistir del contrato. El cliente se hará cargo de los gastos de devolución, salvo que la realice por correo.

(Cuando con arreglo al artículo 103 TRLGDCU no proceda el derecho de desistimiento, debe indicarse al consumidor y usuario que no le asiste, o las circunstancias en las que lo perderá cuando le corresponda).

GARANTÍA Y SERVICIO DE POSVENTA

El producto ofertado tiene la garantía comercial del fabricante en los términos legalmente establecidos, durante un periodo de dos años a partir de la fecha de entrega.

Las garantías no incluyen las deficiencias ocasionadas por negligencias, golpes, uso o manipulaciones indebidas, conexión a la red eléctrica diferente a la indicada en los manuales de uso, instalación incorrecta no efectuada por el servicio técnico autorizado cuando proceda, ni materiales sometidos a desgaste por su uso normal.

El fabricante [ÓRGANO] ofrece un servicio de posventa a través de sus servicios técnicos, cuyas condiciones pueden consultarse en la página web [PÁGINA WEB]

En [LUGAR], a [DÍA] de [MES] de [AÑO].

EL VENDEDOR

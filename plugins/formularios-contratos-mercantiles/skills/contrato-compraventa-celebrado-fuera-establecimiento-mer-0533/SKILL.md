---
name: contrato-compraventa-celebrado-fuera-establecimiento-mer-0533
description: "Contrato de compraventa celebrado fuera del establecimiento mercantil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa celebrado fuera del establecimiento mercantil

> Formulario **MER-0533** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa celebrado fuera del establecimiento mercantil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa celebrado fuera del establecimiento mercantil” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-compraventa-celebrado-fuera-establecimiento-mer-0533`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NIF (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] PRODUCTOS QUE SE VENDEN
- [ ] ÓRGANO

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

En la localidad/ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte, D [NOMBRE Y APELLIDOS], mayor de edad, que interviene en representación de la mercantil [NOMBRE DEL REPRESENTADO/A], con domicilio en [LOCALIDAD] y titular del CIF [NIF], en calidad de VENDEDOR;

Y de otra, D [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD] y titular del NIF [NIF], en calidad de COMPRADOR;

MANIFIESTAN

Que reconociéndose mutuamente las partes, según intervienen en la representación expresada, la capacidad legal necesaria a los efectos de este CONTRATO DE COMPRAVENTA, celebrado en [LOCALIDAD], FUERA DEL ESTABLECIMIENTO MERCANTIL DEL VENDEDOR, y de forma libre, espontánea y de mutuo acuerdo

EXPONEN

I. El VENDEDOR se dedica a la venta de [PRODUCTOS QUE SE VENDEN], comercializando el siguiente producto ()

II. El COMPRADOR está interesado en su compra, habiendo sido informado previamente por el VENDEDOR de las condiciones de adquisición del citado producto, según información precontractual que se anexa al presente contrato, manifestando el COMPRADOR quedar enterado de su contenido.

III. Y estando interesados en formalizar la compraventa del referido producto, la convienen de acuerdo con las siguientes

CLÁUSULAS

Objeto del contrato

D. [NOMBRE Y APELLIDOS], en la representación que ostenta, VENDE a D. [NOMBRE Y APELLIDOS], que COMPRA el producto reseñado en el expositivo primero.

Precio

El precio convenido es de [IMPORTE] euros, en cuyo importe quedan incluidos el IVA y los gastos de entrega.

El pago del precio se realiza por el comprador al vendedor mediante [ÓRGANO] en este acto, expidiéndose por el VENDEDOR el documento acreditativo correspondiente.

Entrega

El VENDEDOR, en este acto, hace entrega al COMPRADOR del producto (o el vendedor entregará el producto en el domicilio del comprador que figura en el encabezamiento en un plazo no superior a días).

Derecho de desistimiento del comprador

El COMPRADOR tiene derecho a desistir del contrato durante un periodo de 14 días naturales desde el día de la entrega, sin necesidad de indicar el motivo.

Para ejercer el derecho de desistimiento, el COMPRADOR deberá comunicar al vendedor su decisión de desistir del contrato a través de una declaración inequívoca (por ejemplo, una carta enviada por correo postal, fax o correo electrónico), pudiendo utilizar el modelo de formulario que se anexa a este contrato.

Para cumplir el plazo de desistimiento, basta con que la comunicación relativa al ejercicio por parte del COMPRADOR de este derecho sea enviada antes de que venza el plazo correspondiente.

En caso de desistimiento, el VENDEDOR devolverá todos los pagos recibidos del cliente, sin ninguna demora indebida y, en todo caso, a más tardar 14 días naturales a partir de la fecha en la que sea informado por el cliente de su decisión de desistir del contrato.

Garantía por falta de conformidad

El plazo de garantía por falta de conformidad es de dos años a partir de la fecha de la entrega del producto. El VENDEDOR responderá ante el COMPRADOR, de la falta de conformidad que se manifieste en el plazo de garantía en los términos del Texto Refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras Leyes complementarias.

No habrá lugar a responsabilidad por las faltas de conformidad que el comprador conociera o no hubiera podido fundadamente ignorar en el momento de la celebración del contrato.

En caso de falta de conformidad, el COMPRADOR tendrá derecho, a su elección, a la reparación o sustitución del producto. La rebaja del precio y la resolución del contrato, procederán, a elección del COMPRADOR, cuando este no pudiera exigir la reparación o la sustitución y en los casos en que no se hubieran llevado a cabo en plazo razonable o sin mayores inconvenientes para el consumidor. La resolución no procederá cuando la falta de conformidad sea de escasa importancia.

A este efecto, deberá comunicar al VENDEDOR garante, la falta de conformidad apreciada, a la mayor brevedad posible, y en todo caso, y como máximo, en el plazo legal de DOS MESES, desde que tuviera conocimiento de la misma. Salvo prueba en contrario, se entenderá que la comunicación del consumidor ha tenido lugar dentro del plazo establecido. El incumplimiento de dicho plazo, no supondrá la pérdida del derecho del consumidor, pero éste será responsable de los daños que se ocasionen en el bien por el retraso en la comunicación.

Garantía comercial y servicio de posventa

El producto ofertado tiene la garantía comercial del fabricante en los términos legalmente establecidos, durante un periodo de dos años a partir de la fecha de entrega.

Las garantías no incluyen las deficiencias ocasionadas por negligencias, golpes, uso o manipulaciones indebidas, conexión a la red eléctrica diferente a la indicada en los manuales de uso, instalación incorrecta no efectuada por el servicio técnico autorizado cuando proceda, ni materiales sometidos a desgaste por su uso normal.

El fabricante ofrece un servicio de posventa a través de sus servicios técnicos, cuyas condiciones pueden consultarse en la página web

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

En prueba de conformidad, una vez leído el contrato y sus anexos, que forma parte integrante e inseparable del mismo, ambas partes firman el presente documento, por duplicado y aun sólo efecto, quedando en poder del comprador una de las copias del contrato, en el lugar y fecha indicados en el encabezamiento.

EL VENDEDOR

Fdo.

EL COMPRADOR

Fdo.

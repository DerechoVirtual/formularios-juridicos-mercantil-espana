---
name: compraventa-acciones-sociedad-contrato-mer-0046
description: "Compraventa de acciones de una sociedad (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Compraventa de acciones de una sociedad (contrato)

> Formulario **MER-0046** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Compraventa de acciones de una sociedad (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Compraventa de acciones de una sociedad (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:compraventa-acciones-sociedad-contrato-mer-0046`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] NIF (3 veces)
- [ ] Nº (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] ENTIDAD BANCARIA
- [ ] FOLIO
- [ ] HOJA
- [ ] INSCRIPCIÓN
- [ ] MEDIO DE PAGO
- [ ] MOMENTO DEL PAGO
- [ ] NACIONALIDAD
- [ ] NOMBRE DEL NOTARIO
- [ ] TOMO
- [ ] TÍTULO DEL APARTADO

## Normas que cita el formulario

- art. 545 Código de Comercio
- art. 338 Ley 6/2023
- art. 338 LM

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

De una parte, D. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD] y titular del NIF [NIF], en calidad de VENDEDOR;

Y de otra, D. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD] y titular del NIF [NIF], en calidad de COMPRADOR;

MANIFIESTAN

Que reconociéndose mutuamente las partes, según intervienen en la representación expresada, la capacidad legal necesaria a los efectos de este CONTRATO DE COMPRAVENTA DE ACCIONES de la sociedad mercantil [DENOMINACIÓN SOCIAL], y de forma libre, espontánea y de mutuo acuerdo

EXPONEN

El VENDEDOR es dueño, en pleno dominio, de [Nº] acciones de la entidad mercantil [DENOMINACIÓN SOCIAL], entidad de nacionalidad [NACIONALIDAD] con domicilio social en [LOCALIDAD], número [NÚMERO] y provista de Número de Identificación Fiscal [NIF]. Constituida mediante escritura pública autorizada por el Notario de [LOCALIDAD] Don [NOMBRE DEL NOTARIO] el [DÍA] de [MES] de [AÑO], bajo el número [NÚMERO] de su protocolo, e inscrita el [DÍA] de [MES] de [AÑO] en el Registro Mercantil de [LOCALIDAD], en el tomo [TOMO], folio [FOLIO], hoja [HOJA], inscripción [INSCRIPCIÓN] en adelante, la SOCIEDAD.

Las acciones de la SOCIEDAD titularidad del VENDEDOR se corresponden con las números [Nº] a [Nº], por un valor nominal total de [IMPORTE] euros, que están totalmente desembolsadas, libres de toda carga, gravamen, responsabilidad o afección, y que representan el [PORCENTAJE] % del capital social de la SOCIEDAD.

El COMPRADOR está interesado en la compra de las acciones descritas anteriormente titularidad del VENDEDOR

Y estando interesados en formalizar la compraventa de las referidas acciones, la convienen de acuerdo con las siguientes

CLÁUSULAS

Objeto del contrato

D. [NOMBRE Y APELLIDOS], VENDE a D. [NOMBRE Y APELLIDOS], que COMPRA las acciones reseñadas en el expositivo primero y segundo.

Precio

El precio total convenido es de [IMPORTE] euros, que incluye todos los conceptos.

El pago se realiza en este acto [MEDIO DE PAGO].

El pago se efectúa [MOMENTO DEL PAGO] mediante transferencia bancaria a la cuenta número [NÚMERO] del banco [ENTIDAD BANCARIA] del VENDEDOR, manifestando el deudor haberlo recibido y sirviendo la firma del presente de eficaz carta de pago.

Entrega

El VENDEDOR, en este acto, hace entrega al COMPRADOR de las acciones al portador objeto de transmisión.

(en su caso, El VENDEDOR entregará las acciones objeto de la compraventa tan pronto se realice el pago, en la forma prevista en el art. 120 del TR Ley de Sociedades de Capital.)

( en su caso, debe tenerse en cuenta lo dispuesto en el art. 120 TR Ley Sociedades Capital: i) si no se han impreso y entregado los títulos, la transmisión de acciones procederá de acuerdo con las normas sobre la cesión de créditos y demás derechos incorporales. Tratándose de acciones nominativas, los administradores, una vez que resulte acreditada la transmisión, la inscribirán de inmediato en el libro-registro de acciones nominativas.

ii) Una vez impresos y entregados los títulos, la transmisión de las acciones al portador se sujetará a lo dispuesto en el artículo 545 del Código de Comercio. Las acciones nominativas también podrán transmitirse mediante endoso, en cuyo caso serán de aplicación, en la medida en que sean compatibles con la naturaleza del título, los artículos 15, 16, 19 y 20 de la Ley Cambiaria y del Cheque. La transmisión habrá de acreditarse frente a la sociedad mediante la exhibición del título. Los administradores, una vez comprobada la regularidad de la cadena de endosos, inscribirán la transmisión en el libro-registro de acciones nominativas).

Obligaciones y garantías del vendedor

El VENDEDOR asume la responsabilidad por vicios ocultos y al saneamiento por evicción. Asimismo se obliga a comunicar, en el plazo máximo de tres días a la sociedad la presente transmisión, indicando su fecha, la identidad de las partes y el objeto transmitido, así como los demás datos exigibles conforme a las normas legales o estatutarias aplicables. [TÍTULO DEL APARTADO]:

El VENDEDOR garantiza a) que se han cumplido todos los requisitos previstos en los Estatutos Sociales en orden a la transmisión de las acciones anteriormente mencionadas; b) que las acciones objeto del presente Contrato le pertenecen en pleno dominio por justos y legítimos títulos, c) que no existen cargas ni gravámenes de naturaleza real sobre dichas acciones; y d) que las acciones de la SOCIEDAD representan el [PORCENTAJE] % del capital de dicha sociedad a la fecha del presente Contrato.

Otorgamiento de escritura

El presente contrato será elevado a escritura pública a requerimiento de cualquiera de las partes, designándose la Notaría de [LOCALIDAD].

Los gastos de otorgamiento serán de cuenta de [NOMBRE DE LA PARTE].

Exención del ITP y AJD

Ambas partes manifiestan que la presente compraventa está exenta del Impuesto de Transmisiones Patrimoniales y Actos Jurídicos Documentados, según lo previsto en el artículo 338 de la Ley 6/2023, de 17 marzo, del Mercado de Valores y Servicios de Inversión, comprometiéndose a llevar a cabo las actuaciones necesarias para materializar dicha exención.

El VENDEDOR manifiesta que los valores de la SOCIEDAD no se incluyen en ninguno de los supuestos de sujeción contemplados en el citado art. 338 LMV/2023.

Otros gastos e impuestos

Los demás gastos e impuestos derivados de esta compraventa serán de cuenta de [NOMBRE DE LA PARTE].

Notificaciones

Todas las notificaciones, requerimiento, peticiones y otras comunicaciones que hayan de efectuarse por las Partes en relación con el presente Contrato, deberán realizarse por escrito y se entenderá que han sido debidamente realizadas cuando hayan sido entregadas en mano o bien remitidas por correo certificado al domicilio de la otra Parte que conste en el encabezamiento del presente Contrato, o bien a cualquier otro domicilio que a estos efectos cada Parte pueda indicar a la otra.

Régimen jurídico

Este contrato reviste carácter mercantil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por el Texto Refundido de Ley de Sociedades de Capital, y en su defecto por el Código de Comercio, usos mercantiles, Leyes especiales y por lo previsto en el Código Civil.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

En prueba de conformidad, una vez leído el contrato, ambas partes firman el presente documento, por duplicado y aun sólo efecto, en el lugar y fecha indicados en el encabezamiento.

EL VENDEDOR EL COMPRADOR

Fdo. Fdo.

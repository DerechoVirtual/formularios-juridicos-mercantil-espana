---
name: contrato-internacional-suministro-regimen-exclusividad-mer-0611
description: "Contrato internacional de suministro en régimen de exclusividad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato internacional de suministro en régimen de exclusividad

> Formulario **MER-0611** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato internacional de suministro en régimen de exclusividad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato internacional de suministro en régimen de exclusividad” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-internacional-suministro-regimen-exclusividad-mer-0611`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (5 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] MES (2 veces)
- [ ] PLAZO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº DE CUENTA (IBAN)
- [ ] PRODUCTOS
- [ ] REGIÓN O PAÍS DE ORIGEN
- [ ] TIPO DE GASTRONOMÍA

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

EXPONEN

I. Que LA SUMINISTRADORA se dedica habitualmente a la fabricación y venta de [PRODUCTOS]

II. Que LA EMPRESA es un restaurante especializado en gastronomía [TIPO DE GASTRONOMÍA] que ofrece a sus clientes la posibilidad de degustar productos típicos de [REGIÓN O PAÍS DE ORIGEN]

III. Que compartiendo ambas el objetivo de promover y difundir la cultura gastronómica alemana, acuerdan concertar el presente CONTRATO INTERNACIONAL DE SUMINISTRO CON CLÁUSULA DE EXCLUSIVIDAD con arreglo a las siguientes,

ESTIPULACIONES

Objeto del contrato

I.LA EMPRESA concede a LA SUMINISTRADORA los derechos de suministro en exclusiva de los productos que aparecen relacionados en el listado que se acompaña al presente contrato como Anexo I

II. Esto no obstante, quedan incluidos en la misma todos aquellos productos que, pese a no figurar en el anexo, sean fabricados y comercializados por LA SUMINISTRADORA, y que LA EMPRESA pudiera en algún momento necesitar.

Exclusividad del contrato

I. La exclusividad del presente contrato se regirá por lo dispuesto en los párrafos siguientes.

II. Durante la vigencia del presente contrato LA SUMINISTRADORA se obliga a no suministrar, vender o comercializar sus productos a aquellas personas, físicas o jurídicas, que fueran competidoras directas de LA EMPRESA en el mercado en un radio de dos manzanas de edificios a la redonda, salvo autorización expresa de esta última.

III.LA EMPRESA se obliga a utilizar exclusivamente los productos fabricados o comercializados por LA SUMINISTRADORA en la preparación y/o venta de los menús y productos ofertados o degustados en sus locales, no comprando estos productos a ningún otro proveedor.

Además, a efectos de control contable, deberá facilitar a LA SUMINISTRADORA relaciones trimestrales, debidamente firmadas por una persona representativa de la sociedad, de los movimientos de venta en unidades y valores, así como del stock de los productos aún existentes en sus dependencias.

Igualmente, LA EMPRESA se compromete a no adquirir participación ni derecho alguno en negocios o empresas que se dediquen a la comercialización de productos competidores.

IV. El incumplimiento, por cualquiera de las partes, de las obligaciones reguladas en este apartado dará derecho a la parte contraria a una indemnización equivalente a [IMPORTE] euros anuales.

Precio

I.LA SUMINISTRADORA venderá los productos a LA EMPRESA ajustándose, durante el primer año de vigencia del contrato, a las tarifas que se acompañan como Anexo II del presente acuerdo.

II. En tal precio se hallan comprendidas, a excepción de los portes, cuantas actividades sean precisas para la entrega de los pedidos en el domicilio de LA EMPRESA, lugar donde deberán ser entregados los productos.

III. Para los años subsiguientes, las partes fijarán anualmente, de común acuerdo y por escrito el precio de los productos vigente durante la próxima anualidad. En ausencia de acuerdo, se entenderán incrementados en un porcentaje equivalente al IPC interanual.

Pedidos

I. Todos los pedidos serán formalizados por LA EMPRESA, por escrito, en el domicilio de LA SUMINISTRADORA con una antelación mínima de [Nº] días respecto a la fecha de su efectivo libramiento.

II. En todo caso, las partes pactan un pedido mínimo, de forma que LA EMPRESA adquiera productos de LA SUMINISTRADORA por un importe superior a [IMPORTE] euros anuales ( €).

Pagos

Los productos suministrados por LA SUMINISTRADORA a LA EMPRESA se pagarán en el número de cuenta corriente [Nº DE CUENTA (IBAN)] abierta en la entidad [DENOMINACIÓN SOCIAL] en el plazo de [PLAZO] a contar desde la fecha de recepción de los productos. A tal fin, LA SUMINISTRADORA expedirá en cada caso la factura correspondiente.

Duración del contrato

I. El presente contrato tiene una duración de [Nº] años, expirando en consecuencia el día [DÍA] de [MES] de [AÑO]

II. No obstante, podrá renovarse por tácita reconducción por períodos sucesivos de [PLAZO], salvo que alguna de las partes notifique a la otra por cualquier medio que dejara constancia de su recepción, y con [Nº] mes de antelación al término del período inicial o de cualquiera de los sucesivos, su deseo de dar por terminado el contrato.

Calidad de los productos

I.LA SUMINISTRADORA controlará el estado óptimo y calidad de los productos antes de que salgan de sus instalaciones.

II. En caso de que LA EMPRESA recibiere un producto en mal estado, tendrá derecho a optar entre la devolución del mismo con la consiguiente anulación del pedido; o a solicitar de LA SUMINISTRADORA la entrega de un nuevo pedido de las mismas características en buenas condiciones.

Resolución por incumplimiento

I. Cualquiera de las partes podrá resolver el presente contrato en caso de que la otra lo incumpliere.

II. El perjudicado podrá optar entre exigir el cumplimiento o la resolución del contrato, con el resarcimiento de daños y abono de intereses en ambos casos. También podrá pedir la resolución, aún después de haber optado por el cumplimiento, cuando éste resultase imposible.

III. Previamente al ejercicio de la facultad de optar entre este cumplimiento o la resolución contractual, el perjudicado deberá requerir, de forma fehaciente, a la otra parte, señalándole sus incumplimientos y dándole un plazo de [Nº] días a contar desde la recepción de dicha comunicación para que pueda subsanarlos. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

IV. En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de [Nº] días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

Notificaciones

Las partes señalan como respectivos domicilios, a efectos de notificaciones, los reseñados en el encabezamiento del presente contrato.

Legislación aplicable y jurisdicción

I. El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas; en lo en ellas no previsto, por la Legislación Española. En concreto por las disposiciones del Código de Comercio, leyes especiales y usos mercantiles; y en su defecto, por el Código Civil.

II. Ambas partes renuncian expresamente a su fuero y acuerdan someterse a los Tribunales de [LOCALIDAD] para la resolución de todas las cuestiones litigiosas que se suscitaran entre ellas con ocasión de la interpretación o ejecución del presente contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes suscriben por duplicado y a un solo efecto cada una de las hojas de que se compone el presente CONTRATO INTERNACIONAL DE SUMINISTRO CON CLÁUSULA DE EXCLUSIVIDAD en el lugar y fecha indicados en el encabezamiento.

Firmas:

========================================================================

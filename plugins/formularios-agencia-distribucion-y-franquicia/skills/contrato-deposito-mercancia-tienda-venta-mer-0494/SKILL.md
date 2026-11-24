---
name: contrato-deposito-mercancia-tienda-venta-mer-0494
description: "Contrato de depósito de mercancía en una tienda para su venta. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de depósito de mercancía en una tienda para su venta

> Formulario **MER-0494** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de depósito de mercancía en una tienda para su venta» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de depósito de mercancía en una tienda para su venta” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-deposito-mercancia-tienda-venta-mer-0494`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] Nº (6 veces)
- [ ] NOMBRE DE LA PARTE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ÁMBITO TERRITORIAL (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] PLAZO
- [ ] PRODUCTOS
- [ ] PRODUCTOS QUE VENDE
- [ ] PROVINCIA

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

CONTRATO DE DEPÓSITO DE MERCANCÍA EN TIENDA

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS] mayor de edad, de estado civil [ESTADO CIVIL] vecino de [LOCALIDAD] domiciliado en [DOMICILIO] con documento nacional de identidad número [NÚMERO]

De otra:

D [NOMBRE Y APELLIDOS] mayor de edad, de estado civil [ESTADO CIVIL] vecino de [LOCALIDAD] domiciliado en [DOMICILIO] con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D. [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA DEPOSITANTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS] en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA DEPOSITARIA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS] en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE DEPÓSITO DE MERCANCÍA PARA VENTA, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO Que LA DEPOSITANTE es una persona jurídica de derecho privado dedicada a la [ACTIVIDAD] de [PRODUCTOS].

SEGUNDO Que LA DEPOSITARIA, por su parte, se dedica a la venta de [PRODUCTOS QUE VENDE]

TERCERO Que por ello, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

LA DEPOSITARIA encargará periódicamente y LA DEPOSITANTE suministrará periódicamente las cantidades del Producto de acuerdo con las condiciones del presente contrato.

Las calidades y características de dichos bienes se detallan en el Anexo I que se acompaña al presente documento.

[ELEGIR UNA OPCIÓN: Precio, facturación y pago / Precio fijo / Precio actualizable / — y además elegir: Entrega / Cantidades fijas / Cantidades variables en función del consumo / — y además elegir: Almacenamiento / Almacenamiento a cargo de la depositaria / Almacenamiento a cargo de la Depositante]

Duración

El presente contrato tendrá una duración de [PLAZO] y podrá ser prorrogado mediante acuerdo celebrado por escrito entre las partes por un plazo igual, siempre y cuando esto se realice con [Nº] días de antelación al vencimiento del plazo inicialmente pactado.

Saneamiento

Inmediatamente después de la entrega, LA DEPOSITARIA inspeccionará sin demora el Producto en cuanto a tipo, cantidad y problemas manifiestos de calidad y notificará a LA DEPOSITANTE las posibles objeciones, incluidas las reclamaciones por falta de entrega o daños. Esta notificación deberá hacerse en el plazo de [Nº] días laborables siguientes a la entrega o, de lo contrario, se estimará que el Producto se ha entregado en su totalidad y en condiciones satisfactorias.

Si las mercancías no coincidiesen con las calidades, forma y tamaño descritos en el Exponendo Primero, quien las hubiera recibido dispondrá de un plazo de [Nº] días a partir de esa fecha para la solicitud de sustitución de las mercancías que resulten defectuosas o que no se ajusten a dichas características.

El plazo de sustitución de la mercancía no será superior a [Nº] días. En caso de que [NOMBRE DE LA PARTE] no proceda a la sustitución dentro de ese plazo, [NOMBRE DE LA PARTE] podrá proceder a exigir el cumplimiento o la resolución del contrato, con abono en ambos casos de los daños y perjuicios que se le hayan irrogado.

GARANTÍAS

Reserva de dominio

La propiedad del Producto no pasará a LA DEPOSITARIA hasta la recepción de la totalidad del pago por el Producto por LA DEPOSITANTE.

Seguro

LA DEPOSITARIA contratará un seguro para el Producto almacenado en las Instalaciones que resulte satisfactorio para LA DEPOSITANTE y proporcionará a éste, a su solicitud, pruebas de la existencia de dicho seguro. La cobertura incluirá, entre otros aspectos, los daños provocados por incendios, agua, fenómenos naturales y robo. LA DEPOSITARIA informará con prontitud a LA DEPOSITANTE de cualquier peligro asegurable y cualquier suceso extraordinario que afecten al Producto y tomará las medidas necesarias para la resolución del problema y la satisfacción de las reclamaciones.

CLÁUSULA DE EXCLUSIVIDAD

Exclusividad de la DEPOSITANTE

Durante la vigencia del presente contrato [NOMBRE DE LA PARTE] se obliga a no suministrar, vender o comercializar sus productos a aquellas personas, físicas o jurídicas, que fueran competidoras directas de LA DEPOSITARIA en [ÁMBITO TERRITORIAL] salvo autorización expresa de esta última.

Exclusividad de la DEPOSITARIA

se obliga a utilizar exclusivamente los productos fabricados o comercializados por LA DEPOSITANTE en la [ÁMBITO TERRITORIAL], no comprando estos productos a ningún otro proveedor. Además, a efectos de control contable, deberá facilitar a LA DEPOSITANTE relaciones trimestrales, debidamente firmadas por una persona representativa de la sociedad, de los movimientos de venta en unidades y valores, así como del stock de los productos aún existentes en sus dependencias. Igualmente, LA DEPOSITARIA se compromete a no adquirir participación ni derecho alguno en negocios o empresas que se dediquen a la comercialización de productos competidores.

El incumplimiento, por cualquiera de las partes, de las obligaciones reguladas en este apartado dará derecho a la parte contraria a una indemnización equivalente a [IMPORTE] euros anuales.

Resolución del contrato

El Contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2. Por acuerdo de las Partes por escrito.

3. La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

Producida la resolución del contrato, LA DEPOSITANTE podrá auditar la cantidad de Producto remanente y, a su discreción, retirarlo a costa de LA DEPOSITARIA o facturar a ésta el precio en vigor en la fecha de rescisión. LA SUMISTRADA pagará la cantidad facturada de acuerdo con las condiciones de pago acordadas.

Cláusula penal

En caso de resolución del contrato por causa imputable a cualquiera de las Partes, la parte contraria no estará obligada a la devolución de las mercancias o cantidades entregadas hasta ese momento, fijándose además una cantidad adicional de [IMPORTE] € como indemnización que la parte incumplidora deberá abonar a

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Jurisdicción competente y ley aplicable

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los Tribunales de [LOCALIDAD], en [PROVINCIA], renunciando expresamente a su fuero propio si lo tuvieran.

El presente contrato tiene carácter mercantil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE DEPÓSITO DE MERCANCÍA EN TIENDA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La DEPOSITANTE)

Fdo. Don [NOMBRE Y APELLIDOS]

(La DEPOSITARIA)

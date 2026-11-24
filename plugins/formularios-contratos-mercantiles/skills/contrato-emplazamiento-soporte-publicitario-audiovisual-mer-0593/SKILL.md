---
name: contrato-emplazamiento-soporte-publicitario-audiovisual-mer-0593
description: "Contrato de emplazamiento de un soporte publicitario audiovisual. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de emplazamiento de un soporte publicitario audiovisual

> Formulario **MER-0593** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de emplazamiento de un soporte publicitario audiovisual» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de emplazamiento de un soporte publicitario audiovisual” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-emplazamiento-soporte-publicitario-audiovisual-mer-0593`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] Nº (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHAS
- [ ] LUGAR
- [ ] MES
- [ ] SUCURSAL

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

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA AGENCIA DE PUBLICIDAD", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL ARRENDADOR", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE ALOJAMIENTO DE SOPORTE PUBLICITARIO AUDIOVISUAL, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que LA AGENCIA DE PUBLICIDAD es una mercantil que tiene por objeto social la difusión de publicidad a través de distintos medios instalados y gestionados directamente por ella, así como la producción de los contenidos emitidos en dichos medios.

SEGUNDO.- Que EL ARRENDADOR es una mercantil que se dedica a [ACTIVIDAD] (descripción de la actividad).

TERCERO.- Que ambas partes están interesadas en suscribir el presente contrato de alojamiento de [DESCRIPCIÓN DEL BIEN] con fines de difusión comercial y, a tal efecto, de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

EL ARRENDADOR se obliga indefectiblemente a alojar [DESCRIPCIÓN DEL BIEN] (soportes publicitarios, tales como pantallas) manteniéndolas operativas durante los horarios en que permanezca abierto al público.

EL ARRENDADOR no podrá utilizar las pantallas y accesorios anteriormente descritos para propósitos o fines distintos de los señalados en el presente contrato, siendo responsable de los daños que tal incumplimiento pudiera generar. Todo ello sin perjuicio de las responsabilidades penales en que pueda incurrir por su utilización indebida, así como del deber de restitución inmediata de los referidos elementos si así lo precisara la propietaria de los mismos.

[ELEGIR UNA OPCIÓN: Precio / Retribución fija / Variable>]

Pago

El pago de las diferentes mensualidades se efectuará entre los días [FECHAS] y [DÍA] de cada mes en la cuenta corriente nº [NÚMERO] que EL ARRENDADOR tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL].

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho al ARRENDADOR a exigir a LA AGENCIA DE PUBLICIDAD un interés moratorio del % respecto de cada uno de los pagos no satisfechos puntualmente.

Duración del contrato

El presente contrato se concluye por un plazo de [Nº] años pudiendo prorrogarse, a voluntad de las partes y de común acuerdo por períodos anuales.

Si llegado el vencimiento del plazo inicial o de cualquiera de sus prórrogas, alguna de las partes decidiera dar por finalizado el presente contrato, deberá de comunicar su intención a la otra parte con al menos dos meses de antelación a la fecha del vencimiento a través de un medio que deje constancia de su recepción.

Contenidos publicitarios

LA AGENCIA DE PUBLICIDAD asumirá la gestión y desarrollo de la programación de las pantallas alojadas en las instalaciones del ARRENDADOR, programación consistente en una combinación discrecional de publicidad, noticias locales, agendas culturales, ocio y entretenimiento o cualquier otro contenido que esta mercantil juzgue de interés, asumiendo frente a terceros las responsabilidades que por derechos de propiedad intelectual se puedan derivar.

No obstante lo anterior, las partes trazarán y plasmarán por escrito las directrices generales a que deben ajustarse los contenidos publicitarios. Además, habrá revisiones periódicas de los contenidos emitidos.

Exclusividad

Durante la vigencia del presente contrato, y dentro del paquete publicitario que se emitirá en las pantallas instaladas en las dependencias del ARRENDADOR, no se realizarán inserciones publicitarias que, de cualquier manera, pudieran promocionar o favorecer a los competidores directos de éste en el mercado.

Autopromoción del arrendador

LA AGENCIA DE PUBLICIDAD destinará un minuto de cada hora en que las pantallas estén operativas a la emisión de inserciones publicitarias dedicadas a la autopromoción del ARRENDADOR.

Instalación y mantenimiento del soporte audiovisual

LA AGENCIA DE PUBLICIDAD se encargará de la instalación, gestión y mantenimiento de las pantallas que están alojadas en el centro comercial del ARRENDADOR, siendo de su cuenta y cargo todos los gastos que por tales conceptos se generen, y comprometiéndose a conservarlos en buen estado y en disposición de ser utilizados para los fines descritos. Con tal fin, se facilitará en todo momento el acceso a las instalaciones del centro comercial al personal técnico de LA AGENCIA DE PUBLICIDAD.

Esto no obstante, serán del exclusivo cargo y responsabilidad del ARRENDADOR los derivados de cualquier eventualidad o incidencia no imputable a LA AGENCIA DE PUBLICIDAD, tales como reformas del centro o labores de mantenimiento del mismo que deriven en la suspensión temporal del servicio. Esta interrupción temporal implicará la reducción de la retribución de carácter fijo y variable en proporción al tiempo en que el soporte audiovisual permanezca fuera de servicio.

EL ARRENDADOR se obliga a respetar y dejar expedito el campo de visión del soporte audiovisual de cualquier tipo de instalación de carácter temporal o permanente que pudiera dificultar su visionado.

De cara al buen funcionamiento del sistema, LA AGENCIA DE PUBLICIDAD realizará revisiones mensuales de las pantallas para mantenerlas en óptimas condiciones. Igualmente, LA AGENCIA DE PUBLICIDAD se compromete a disponer de un servicio de mantenimiento que cubra todo el periodo de emisión y de un equipo de reposición dispuesto a ser instalado con la menor dilación posible en caso de avería grave.

Publicidad no autorizada

EL ARRENDADOR podrá negarse a que se emita aquella publicidad que, por su forma de presentación, por su contenido o difusión provoque el descrédito, denigración o menosprecio directo o indirecto de una persona, empresa o de sus productos, servicios o actividades.

Resolución del contrato

El Contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2. Por acuerdo de las Partes por escrito.

3. La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE ALOJAMIENTO DE SOPORTE PUBLICITARIO AUDIOVISUAL, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo. Don [NOMBRE Y APELLIDOS]

(La AGENCIA DE PUBLICIDAD)

Fdo. Don [NOMBRE Y APELLIDOS]

(El ARRENDADOR)

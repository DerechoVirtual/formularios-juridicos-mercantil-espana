---
name: contrato-arrendamiento-financiero-opcion-compra-leasing-mer-0681
description: "Contrato de arrendamiento financiero con opción de compra (leasing). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento financiero con opción de compra (leasing)

> Formulario **MER-0681** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que el arrendatario toma en leasing un bien propiedad del arrendador financiero, quien podrá optar entre devolver el bien, ejercitar su derecho de opción de compra o solicitar la prórroga del contrato. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del contrato, así como los derechos y obligaciones de cada una de las partes.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento financiero con opción de compra (leasing)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento financiero con opción de compra (leasing)” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-arrendamiento-financiero-opcion-compra-leasing-mer-0681`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] Nº (5 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] FECHAS
- [ ] LUGAR
- [ ] LUGAR DE ENTREGA
- [ ] MES
- [ ] PORCENTAJE
- [ ] SUCURSAL
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 1.851 Código Civil

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

Contrato por el que el arrendatario toma en leasing un bien propiedad del arrendador financiero, quien podrá optar entre devolver el bien, ejercitar su derecho de opción de compra o solicitar la prórroga del contrato. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del contrato, así como los derechos y obligaciones de cada una de las partes.


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

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA ARRENDADORA FINANCIERA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA EMPRESA USUARIA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE ARRENDAMIENTO FINANCIERO, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que LA ARRENDADORA FINANCIERA es una persona jurídica de derecho privado dedicada a la [ACTIVIDAD] (descripción de la actividad).

SEGUNDO.- Que LA ARRENDADORA FINANCIERA es propietaria en régimen de plena propiedad y dominio de [DESCRIPCIÓN DEL BIEN] (descripción del bien).

TERCERA.- Que LA EMPRESA USUARIA se encuentra interesada en adquirir el derecho de uso sobre el bien descrito en el Exponendo Segundo.

CUARTA.- Que por todo lo anterior, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

LA ARRENDADORA FINANCIERA, como propietaria de los bienes objeto del presente contrato, cede el uso de los mismos a LA EMPRESA USUARIA.

Entrega

Los gastos derivados de la entrega del bien, instalación y montaje necesarios para la puesta en funcionamiento del mismo serán de cuenta de [ELEGIR: la arrendadora financiera / la empresa usuaria]

Cuotas periódicas

Importe de las cuotas

El importe total de las cuotas de arrendamiento asciende a [IMPORTE] euros ( €)().

Este importe se pagará mediante [ÓRGANO] cuotas, cuya composición y vencimiento se detallan en el cuadro de amortización que se adjunta como Anexo I.

Pago de las cuotas

El pago se efectuará entre los días [FECHAS] y [DÍA] de cada mes en la cuenta corriente nº [NÚMERO] que LA ARRENDADORA FINANCIERA tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL].

Retraso en el pago

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho a LA ARRENDADORA FINANCIERA a exigir a LA EMPRESA USUARIA un interés moratorio del % respecto de cada uno de los pagos no satisfechos puntualmente. Si LA EMPREAS USUARIA se retrasara en el pago de dos mensualidades, LA ARRENDADORA FINANCIERA podrá optar entre exigir el pago de los plazos pendientes o resolver el contrato, con abono en ambos caso de las indemnizaciones que puedan corresponder.

Duración

El presente contrato tendrá una duración de [Nº] meses dando comienzo en la fecha de la firma del mismo y finalizando [FECHA] (fecha).

Propiedad del bien

LA EMPRESA USUARIA reconoce que la propiedad del bien corresponde a LA ARRENDADORA FINANCIERA.

LA EMPRESA USUARIA se obliga a proclamar la pertenencia del bien a LA ARRENDADORA FINANCIERA frente a cualquier tercero y, en particular, en los supuestos de embargo del bien por un tercero, de insolvencia de LA EMPRESA USUARIA con inclusión del bien en la masa activa o cualesquiera otros de naturaleza análoga. Así mismo, LA EMPRESA USUARIA se compromete a poner en conocimiento de LA ARRENDADORA FINANCIERA cualquier evento que pueda poner en peligro la titularidad que este ostenta sobre el bien.

Condiciones de uso

Conservación y mantenimiento

LA EMPRESA USUARIA se obliga a destinar el bien objeto del contrato a [ACTIVIDAD] (descripción de la actividad) y a utilizarlo con la debida diligencia en atención a sus características y destino, debiendo mantenerlo en buen estado de uso y conservación, siendo de su cuenta las reparaciones o cambios de piezas deteriorados, debiendo utilizar a tal efecto el material adecuado, sustituyendo las piezas por otras de la misma clase y calidad.

Las piezas incorporadas al bien pasarán automáticamente a ser propiedad de LA ARRENDADORA FINANCIERA sin que proceda derecho de compensación alguna a favor de LA EMPRESA USUARIA.

Obras de mejora

Será necesario el consentimiento expreso de LA ARRENDADORA FINANCIERA para alterar o modificar los bienes. LA EMPRESA USUARIA deberá procurar que el bien sea identificable manteniendo perfectamente legibles la señales o inscripciones del bien a tal efecto.

Deterioro y daños del bien arrendado

Los riesgos de deterioro, daño y pérdida total o parcial del bien, incluidos los supuestos de caso fortuito y fuerza mayor serán de cuenta de [ELEGIR: la arrendadora financiera / la empresa usuaria]

Responsabilidad civil

Serán de cuenta exclusiva de LA EMPRESA USUARIA los daños y perjuicios ocasionados a terceros como consecuencia de la utilización del bien.

EVICCIÓN Y SANEAMIENTO

LA EMPRESA USUARIA exonera a LA ARRENDADORA FINANCIERA de la responsabilidad por la idoneidad, el funcionamiento, el estado o cualquier otra circunstancia o condición referida al bien objeto del contrato.

No obstante, en orden a evitar la indefensión del usuario, LA ARRENDADORA FINANCIERA, en su condición de adquirente del bien, cede a LA EMPRESA USUARIA todos los derechos y acciones que puedan corresponderle frente al fabricante y el proveedor de los bienes. Por tal motivo, cualquier defecto que exista en los bienes objeto del presente contrato deberá ser reclamado directamente por LA EMPRESA USUARIA al fabricante o proveedor, o a quien haya sido comprados o resulten responsables de la venta del mismo, sin que exista por parte de LA ARRENDADORA FINANCIERA obligación alguna mas que otorgar a LA EMPRESA USUARIA la representación necesaria para que este en condiciones de exigir la garantía o los daños y perjuicios que se ocasionen por los defectos y/o vicios que tenga los bienes en contra del proveedor vendedor o responsable de éste.

Opciones de la empresa usuaria

Finalizado el plazo de vigencia del contrato LA EMPRESA USUARIA estará obligada a entregar el bien a LA ARRENDADORA FINANCIERA en [LUGAR DE ENTREGA] (punto de entrega) y en el plazo de [Nº] días, debiendo abonar [IMPORTE] euros por cada día de retraso.

El bien deberá ser entregado a LA ARRENDADORA FINANCIERA en perfecto estado, sin más desgaste que el derivado de un uso normal. Serán de cuenta de LA EMPRESA USUARIA los gastos que ocasione la entrega del bien a LA ARRENDADORA FINANCIERA.

No obstante, LA EMPRESA USUARIA no estará obligado a la devolución del bien una vez finalizado el plazo contractual si ejercitara alguna de las opciones siguientes:

1. Celebrar un nuevo contrato de arrendamiento financiero sobre el mismo bien sirviendo como base para el cálculo de las cuotas el valor residual del bien.

2. Adquirir la propiedad del bien ejercitando la opción de compra por el valor residual del bien. A tal efecto las partes convienen en que el valor residual del bien será de [IMPORTE] euros ( €).

LA EMPRESA USUARIA deberá manifestar su intención de ejercitar una de estas opciones en el plazo de [Nº] días antes de la finalización del término contractual notificándolo fehacientemente a LA ARRENDADORA FINANCIERA.

Cuando LA EMPRESA USUARIA se comprometa así formalmente o garantice el ejercicio de la opción de compra quedará obligada a abonar a LA ARRENDADORA FINANCIERA. el IVA correspondiente a las cuotas pendientes de pago en la forma prevista en la legislación correspondiente.

En cualquier caso, para poder optar por la celebración de un nuevo contrato o por la compra del bien será necesario que LA EMPRESA USUARIA se encuentre el corriente de las obligaciones derivadas del mismo, incluidas las obligaciones fiscales.

Cesión del contrato

Cesión de derechos de LA EMPRESA USUARIA

LA EMPRESA USUARIA no podrá transmitir sus derechos sobre el leasing sin el consentimiento previo y por escrito de LA ARRENDADORA FINANCIERA. Ésta no podrá denegar el consentimiento de forma arbitraria.

En caso de una eventual cesión de los derechos, LA ARRENDADORA FINANCIERA podrá adaptar el canon pactado en el presente contrato al que viniera exigiendo a los nuevos clientes en esa fecha.

Cesión de derechos de LA ARRENDADORA FINANCIERA

LA ARRENDADORA FINANCIERA se reserva la facultad de ceder libremente sus derechos y obligaciones derivados del presente contrato, previa comunicación escrita a LA EMPRESA USUARIA. El cesionario quedará subrogado en todos los derechos y obligaciones contractuales de la cedente.

Seguro

LA EMPRESA USUARIA contratará un seguro que resulte satisfactorio para LA ARRENDADORA FINANCIERA y que cubra tanto la responsabilidad civil en que se pudiera incurrir en el desempeño de la actividad, como el riesgo de daños o pérdida que pueda sufrir el bien arrendado durante todo el periodo de vigencia del presente contrato.

LA EMPRESA USUARIA proporcionará a LA ARRENDADORA FINANCIERA, a su solicitud, pruebas de la existencia de dicho seguro. La cobertura incluirá, entre otros aspectos, los daños provocados por incendios, agua, fenómenos naturales y robo.

En caso de impago el arrendador financiero podrá satisfacer directamente el pago a la compañía asegurador y reclamar el importe abonado al usuario incrementado en un [PORCENTAJE] % en concepto de penalización.

Resolución del contrato

El Contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2. Por acuerdo de las Partes por escrito.

3. La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

Obligado solidario

Con el fin de responder a la totalidad en las obligaciones contraídas por LA EMPRESA USUARIA frente a LA ARRENDADORA FINANCIERA en el presente contrato, se constituye OBLIGADO SOLIDARIO con la primera y en favor de LA ARRENDADORA FINANCIERA a D.. [NOMBRE Y APELLIDOS]

El Obligado Solidario garantiza solidariamente con LA EMPRESA USUARIA todas las obligaciones contraídas por este último resultantes del presente contrato, con renuncia expresa a los beneficios de orden, excusión y división y con especial renuncia a lo dispuesto en el artículo 1.851 del Código Civil en cuanto a la no extinción de la fianza por la prórroga o prórrogas concedidas al prestatario/s, haciendo extensiva esta fianza a cualesquiera prórrogas, renovaciones, novaciones o modificaciones de cualquier tipo, expresas o tácitas, que pudieran producirse en las obligaciones de esta póliza hasta la total extinción de las mismas.

El Obligado Solidario deja afecto al buen fin del presente contrato todos sus bienes presentes o futuros.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de la parte

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los … folios del presente CONTRATO DE ARRENDAMIENTO FINANCIERO extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo. Don [NOMBRE Y APELLIDOS]

(La Arrendadora Financiera)

Fdo. Don [NOMBRE Y APELLIDOS]

(La Empresa Usuaria)

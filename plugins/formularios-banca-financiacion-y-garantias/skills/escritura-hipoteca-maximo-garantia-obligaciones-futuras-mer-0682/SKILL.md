---
name: escritura-hipoteca-maximo-garantia-obligaciones-futuras-mer-0682
description: "Escritura de hipoteca de máximo en garantía de obligaciones futuras. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de hipoteca de máximo en garantía de obligaciones futuras

> Formulario **MER-0682** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de hipoteca de máximo en garantía de obligaciones futuras» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de hipoteca de máximo en garantía de obligaciones futuras” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:escritura-hipoteca-maximo-garantia-obligaciones-futuras-mer-0682`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] NÚMERO (5 veces)
- [ ] FECHA (3 veces)
- [ ] Nº DE PROTOCOLO (3 veces)
- [ ] AÑO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE CLÁUSULA
- [ ] TOMO
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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL ACREEDOR HIPOTECARIO", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL DEUDOR HIPOTECARIO", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para la constitución de la presente HIPOTECA, y a tal efecto, libremente y de común acuerdo,

MANIFIESTAN

PRIMERO Que la mercantil [DENOMINACIÓN SOCIAL], en lo sucesivo, La deudora hipotecaria, es titular en pleno dominio del inmueble sito en el municipio de [LOCALIDAD] ubicada en el número [NÚMERO] de la Calle [CALLE] que a continuación se describe:

• inmueble [DESCRIPCIÓN DEL BIEN] situado en [DIRECCIÓN] número [NÚMERO] de [LOCALIDAD], cuyos datos registrales son los siguientes: Finca número [NÚMERO], inscrita en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], constando una superficie de [Nº] metros cuadrados útiles de dicha vivienda en la inscripción registral.

Corresponde a LA DEUDORA HIPOTECARIA el 100% del pleno dominio de la totalidad de la finca.

SEGUNDO Que el inmueble descrito en el Exponendo I de este documento se halla libre de cargas, al corriente de impuestos y de toda clase de pagos a la comunidad de propietarios, según manifiesta la VENDEDORA.

TERCERO Que dicha mercantil decidió financiarse mediante [ÓRGANO] (descripción de la forma de financiación, préstamo, emisión de obligaciones, acciones) según consta en la escritura pública efectuada ante D [NOMBRE Y APELLIDOS], Notario, el día [FECHA] de [MES] (mes) de [AÑO] (año), con el número de protocolo [Nº DE PROTOCOLO] que se adjunta como Anexo I, y en cumplimiento del compromiso señalado en la Cláusula [Nº DE CLÁUSULA] de la misma, procede a la constitución de hipoteca para garantizar aquellas obligaciones, con sujeción a las siguientes,

CLÁUSULAS

Constitución de hipoteca

Sin perjuicio de la responsabilidad personal, ilimitada y solidaria de la parte prestataria y de cualquier otra garantía, personal o real que pueda concurrir, el presente contrato tiene por objeto la constitución de hipoteca, de acuerdo con lo dispuesto en el artículo 217 del Reglamento Hipotecario, a favor del ACREEDOR sobre la finca descrita en el Exponiendo Primero.

[ELEGIR UNA OPCIÓN: Alcance / Alcance de la hipoteca / Una finca / Varias fincas]

Extensión de la garantía

La garantía hipotecaria se extiende a los elementos, bienes y derechos que se enumeran en los arts. 109 y 110 de la Ley Hipotecaria.

También se pacta de forma expresa, que la hipoteca se extiende a las nuevas construcciones existentes en la/s fincas hipotecada/s, aunque no se haya hecho inscripción de obra nueva, así como también se extenderá dicha hipoteca a las edificaciones que en el futuro pudieran construirse sobre dicha/s finca/s, siempre y cuando no hayan sido costeadas por un tercer adquirente.

Cesión del crédito hipotecario

EL DEUDOR HIPOTECARIO renuncia de manera expresa al derecho de notificación en caso de cesión o venta de todo o parte del crédito hipotecario de conformidad con lo dispuesto en la Ley Hipotecaria.

Conservación de la garantía

Mantenimiento y conservación

El DEUDOR HIPOTECARIO queda obligado a la buena conservación de la/s finca/s hipotecada/s, para que no disminuya su valor actual, y a poner en conocimiento del ACREEDOR HIPOTECARIO cualquier novedad dañosa que afecte a la/s misma/s.

Pago de tributos

Igualmente, el DEUDOR HIPOTECARIO queda obligado a pagar a su debido tiempo los tributos y demás gastos legítimos que deba satisfacer por razón de la/s finca/s hipotecada/s que tengan preferencia legal de cobro sobre el ACREEDOR HIPOTECARIO, exhibiendo los recibos que se libren por tales conceptos, a dicho Banco, si al mismo así le interesa

Notificación de procedimientos de expropiación forzosa

El DEUDOR HIPOTECARIO deberá notificar al ACREEDOR HIPOTECARIO cualquier procedimiento de expropiación forzosa que afecte a cualquiera de las fincas hipotecadas, iniciado o que se inicie en el futuro. En este mismo acto los propietarios de la/s fincas ceden en favor del ACREEDOR HIPOTECARIO cuantos derechos les pudieran corresponder con causa en dichos procedimientos expropiatorios de la/s finca/s hipotecadas.

Anticipos por el acreedor hipotecario

EL ACREEDOR HIPOTECARIO queda autorizado para pagar, por cuenta del DEUDOR HIPOTECARIO, tanto las primas de los seguros, como los tributos, gastos de comunidad y cualesquiera otros gastos y conceptos que afecten a la/s finca/s hipotecada/s.

Sin perjuicio de ello, las cantidades satisfechas por EL ACREEDOR HIPOTECARIO de acuerdo con la presente cláusula, serán exigibles por EL ACREEDOR HIPOTECARIO al DEUDOR HIPOTECARIO desde el mismo día en que se realice su pago y, en caso contrario, los importes satisfechos devengaran a favor del Banco intereses al tipo moratorio señalado en esta escritura.

Seguro

EL DEUDOR HIPOTECARIO se obliga a formalizar un seguro de daños, que cubra riesgo de pérdida de la finca hipotecada durante toda la vigencia del presente crédito en una entidad aseguradora de conocida solvencia.

Procedimiento judicial

Si llegara el caso de que EL ACREEDOR HIPOTECARIO tuviera que hacer efectiva la totalidad o parte del capital, intereses y gastos por la vía judicial, podrá ejercitar, a su plena elección, la acción declarativa, la acción ejecutiva o el procedimiento especial que establece el artículo 681 de la Ley de Enjuiciamiento Civil.

Los valores en que se tasan las fincas hipotecadas para que sirvan de tipo en la subasta serán de [IMPORTE] euros ( €).

Asimismo, tanto a los efectos previstos en el artículo 682 de la Ley de Enjuiciamiento Civil como para cualesquiera otros que se derivan de esta escritura, EL DEUDOR HIPOTECARIO señala como domicilio legal para la practica de los requerimientos, notificaciones y citaciones a que haya lugar el de la finca que se hipoteca en esta escritura.

Procedimiento extrajudicial

Para el caso de que la ejecución de la hipoteca tenga lugar por el procedimiento extrajudicial a que se refieren los artículos 129 de la Ley Hipotecaria y 234 y siguientes del Reglamento Hipotecario, las Partes, además de pactar de modo expreso la sujeción a dicho procedimiento, hacen constar lo siguiente:

1º.- Los valores en que se tasan las fincas hipotecadas para que sirvan de tipo en la subasta serán de [IMPORTE] euros ( €).

2º.- EL DEUDOR HIPOTECARIO designa al ACREEDOR HIPOTECARIO por medio de sus representantes legales, como persona que en su día haya de otorgar la escritura de venta de las fincas hipotecadas en su representación.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción de la presente hipoteca serán de cargo de la parte [ELEGIR: acreedora / deudora]

[ELEGIR UNA OPCIÓN: Jurisdicción competente / Jurisdicción competente y ley aplicable / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de esta escritura.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente acuerdo anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del mismo fuere declarada nula o inaplicable, dicha cláusula se considerará excluida, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este acuerdo.

Las comparecientes aceptan el contenido de la presente escritura.

Hechas las advertencias legales y pertinentes, en particular las de carácter fiscal, así como en forma expresa las relacionadas con la inexcusable obligación de depositar en el Registro de la Propiedad el duplicado de la matriz del título hipotecario que por la presente escritura se emite, así lo otorga, leído por mí, el autorizante, íntegramente y en voz alta, en su presencia, este instrumento público, previa advertencia del derecho que le asiste de leerlo por sí mismo, del que no ha querido usar.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo. Don [NOMBRE Y APELLIDOS]

(El Fiador)

Fdo. Don [NOMBRE Y APELLIDOS]

(El Afianzado)

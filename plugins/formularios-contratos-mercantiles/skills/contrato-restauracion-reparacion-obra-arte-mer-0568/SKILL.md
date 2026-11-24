---
name: contrato-restauracion-reparacion-obra-arte-mer-0568
description: "Contrato de restauración o reparación de una obra de arte. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de restauración o reparación de una obra de arte

> Formulario **MER-0568** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de restauración o reparación de una obra de arte» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de restauración o reparación de una obra de arte” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-restauracion-reparacion-obra-arte-mer-0568`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA OBRA

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

-EXPONEN-

I. Que FUNDACIÓN MUSEO es propietaria de la [NOMBRE DE LA OBRA], obra de arte que integra la Exposición Permanente del Museo (en lo sucesivo, "LA OBRA DE ARTE").

II. Que D. [NOMBRE Y APELLIDOS], de profesión electricista, se dedica habitualmente a las labores de reparación y mantenimiento de instalaciones eléctricas.

III. Que habiéndose apreciado deficiencias en la estructura mecánica y en la instalación eléctrica de la obra de arte, supra mencionada, ambas partes están interesadas en suscribir el presente CONTRATO DE DE REPARACIÓN, y a tal efecto, libremente y de común acuerdo, conciertan el contrato con arreglo a las siguientes,

ESTIPULACIONES

Objeto del contrato

I. D. llevará a cabo la reparación de la OBRA DE ARTE, tanto en su vertiente mecánica como eléctrica, siempre bajo la supervisión y las órdenes de FUNDACIÓN MUSEO (en las personas de [NOMBRE Y APELLIDOS] y/o [NOMBRE Y APELLIDOS]), quien asume toda responsabilidad, directa o indirecta, que por la misma se pueda derivar.

II. La reparación de la instalación eléctrica consistirá en la sustitución de todos aquellos elementos indicados por [NOMBRE Y APELLIDOS] y/o [NOMBRE Y APELLIDOS] por unos nuevos de características y calidades similares.

III. Por lo que a la vertiente mecánica de la reparación respecta, ésta se circunscribirá al cambio de cadenas, piñones y demás elementos de uso común que se relacionan en el Anexo I de este contrato. Cualquier otra reparación no prevista en el mismo precisará del consentimiento expreso y por escrito de las partes contratantes.

Precio

I. El precio pactado se fija en [IMPORTE] euros ( €) más I.V.A., conforme al presupuesto aceptado por las partes que se adjunta como Anexo II de este contrato.

II. Esta cantidad será abonable mediante una entrega inicial del 40% más I.V.A. antes del comienzo de las tareas de reparación. El 60% más I.V.A. restante se abonará en el plazo máximo de 30 días a partir de la entrega de la factura.

Cláusula de reserva de dominio

Hasta el momento en que la totalidad de las cantidades adeudadas le sean satisfechas, D. conserva el pleno dominio y propiedad de los materiales y demás componentes empleados en la reparación de la OBRA DE ARTE. Por ello, podrá retirarlos por falta de pago en cualquier momento aunque su venta y/o montaje haya sido efectuado por terceras personas.

Plazo de ejecución

I. El plazo para la realización de la reparación se pacta en [Nº] días, contabilizados a partir del momento de la firma del presente contrato.

II. D. se compromete a tener a disposición de FUNDACIÓN MUSEO aquellos piñones, cadenas o cualesquiera otro elementos de uso común que sean necesarios para la reparación de LA OBRA DE ARTE en el plazo máximo de [Nº] días hábiles contados a partir del momento en que le hayan sido solicitados. Para el resto de componentes, se estará a lo dispuesto por el proveedor de los mismos.

Modificación del contrato

En el supuesto de incidencias surgidas durante la ejecución de las tareas de reparación que determinen la imposibilidad de ejecución del contrato con arreglo a lo estrictamente estipulado, las partes podrán convenir un nuevo acuerdo que modifique o complemente lo dispuesto en este anterior.

Incumplimiento o ejecución defectuosa del contrato

I. El incumplimiento de la obligación de pago faculta al D. a suspender la ejecución del contrato, dando por vencidos y sin efecto los acuerdos concertados mientras dure la situación de mora; o bien, a resolver el presente acuerdo con reserva de todos los derechos que pudieran corresponderle.

II. Cualquier otro incumplimiento contractual por cualquiera de las partes dará derecho a la resolución del contrato con abono, en todo caso, de los daños y perjuicios que hubiera generado.

Plazo de garantía

En relación con lo anterior, y sin perjuicio de la obligación del contratista de realizar la obra en las debidas condiciones, de lo que debe responder en los términos legalmente establecidos, se pacta una garantía adicional de meses durante los cuales atenderá cualquier reparación sin cargo alguno por sustitución de piezas defectuosas, y mano de obra y desplazamientos, siempre y cuando las averías no se deban a manipulaciones ajenas a su servicio técnico, inadecuado funcionamiento o causas imprevisibles como fallos en el suministro de energía eléctrica, incendios, inundaciones, etc.

Retención de cantidades

EL COMITENTE retendrá el % del precio final de la obra hasta transcurrido el plazo de días/meses desde la recepción definitiva como garantía por posibles vicios ocultos o demora en la entrega de la obra.

Resolución del contrato

En caso de resolución del presente contrato, habrá lugar a una comprobación y liquidación de las obras realizadas con arreglo al proyecto, fijando los saldos pertinentes a favor o en contra del contratista.

Jurisdicción competente y ley aplicable

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, la competencia de los Tribunales que deban conocer del asunto se determinará de conformidad con los criterios de competencia objetiva, funcional y territorial legalmente aplicables.

El presente contrato tiene exclusivamente carácter civil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código Civil y, demás leyes especiales.

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los folios del presente CONTRATO DE REPARACIÓN DE OBRA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

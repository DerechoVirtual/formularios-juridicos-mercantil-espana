---
name: contrato-subcontratacion-obras-mer-0615
description: "Contrato de subcontratación de obras. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de subcontratación de obras

> Formulario **MER-0615** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de subcontratación de obras» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de subcontratación de obras” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-subcontratacion-obras-mer-0615`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (16 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DÍA (4 veces)
- [ ] NÚMERO (4 veces)
- [ ] AÑO (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] MES (3 veces)
- [ ] OBJETO DE LA OBRA (3 veces)
- [ ] CALLE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] PLAZO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIBIR
- [ ] DESTINO DEL EDIFICIO
- [ ] FECHAS
- [ ] LUGAR
- [ ] Nº DE DÍAS
- [ ] Nº DE EXPEDIENTE
- [ ] OTROS DATOS
- [ ] PISO

## Normas que cita el formulario

- art. 17 Ley 38/1999
- art. 4 Ley 32/2006
- art. 8 Ley 32/2006

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

[ELEGIR UNA OPCIÓN: Intervienen / En representación / Nombre propio]

Exponen

PRIMERO.- Que al Contratista se le ha adjudicado la construcción del edificio sito en [LOCALIDAD] en la calle [CALLE], número [NÚMERO], destinado a [DESTINO DEL EDIFICIO].

SEGUNDO.- Que interesa a las Partes concertar el presente contrato de ejecución de la obra consistente en [DESCRIBIR] en la construcción citada.

TERCERA.- Recibe el Subcontratista los siguientes documentos que forman parte de este contrato para su información y como descriptivos de la obra a realizar:

1º Copia de la Licencia de Obras, otorgada por el Ayuntamiento de [LOCALIDAD] el día [DÍA] de [MES] de [AÑO], expediente número [Nº DE EXPEDIENTE] (Anexo I)

2º Proyecto de Obras firmado por D. junto con la Memoria (Anexo II).

3º Cuadro de precios unitarios y presupuesto de [OBJETO DE LA OBRA] (Anexo III)

4º Plan de desarrollo de [OBJETO DE LA OBRA] (Anexo IV)

5º Planos de [OBJETO DE LA OBRA] (Anexo V)

6º Pliego de Condiciones Técnicas y de calidades de los materiales que se emplearán en la obra con el detalle de las características técnicas de cada elemento a instalar o ejecutar (Anexo VI).

7º Plan de Seguridad y Salud que se encuentra debidamente visado con fecha [DÍA] de [MES] de [AÑO] por el Colegio Oficial de Arquitectos Técnicos o Aparejadores. (Anexo VII).

8º Formará también parte del presente contrato, el Acta que las partes levanten como comprobación del replanteo de las obras (Anexo VIII)

CUARTA.- Que para una mayor concreción, se entiende por:

1. Dirección Facultativa: La dirección facultativa estará integrada por el Arquitecto Superior D. e intervendrá como Arquitecto Técnico D. [NOMBRE Y APELLIDOS], quienes desarrollarán las funciones que la Ley establece.

2. Propiedad titular de la obra: D./ la mercantil [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD], en la calle [CALLE], número [NÚMERO], piso [PISO], N.I.F, Tfno. y Fax

QUINTA.- Que interesando a ambas partes, suscriben el presente contrato de conformidad con las siguientes,

ESTIPULACIONES

Objeto

El objeto de este contrato lo constituye la ejecución por EL SUBCONTRATISTA de los trabajos de edificación conforme al proyecto descrito en el expositivo segundo.

[ELEGIR UNA OPCIÓN: Precio / Cerrado / Por unidad de medida]

Plazo

El plazo para la realización de la obra se pacta en [Nº] días, contabilizados a partir del momento en que se concedan las licencias municipales oportunas.

Si llegado dicho término la obra no se hubiese terminado, salvo causas de fuerza mayor no imputables al SUBCONTRATISTA, se establece una cláusula penal consistente en una indemnización de [IMPORTE] euros ( €) por día, descontándose de esta forma del precio total que quede por pagar por parte de D. [NOMBRE Y APELLIDOS]

Un retraso superior a [Nº] meses podrá ser considerado por EL CONTRATISTA como incumplimiento definitivo a los efectos de la resolución del contrato, y le dará derecho a realizar directamente o contratar la ejecución con un tercero, abonando su importe con cargo a las cantidades que en aquel momento adeudase EL CONTRATISTA al SUBCONTRATISTA, sin perjuicio de las demás acciones que cualquiera de las partes pudiera ejercitar para reclamar lo que creyese que le corresponde, mediante Arbitraje, o en su caso ante los Tribunales.

No se considerará fuerza mayor todos los fenómenos atmosféricos que acaezcan durante la realización de la obra. Sin embargo, son casos de fuerza mayor los incendios causados por la electricidad atmosférica; los fenómenos naturales de efectos catastróficos, como maremotos, terremotos, inundaciones u otros semejantes; y los destrozos ocasionados por robos tumultuosos o alteraciones graves del orden público. En estos supuestos, y siempre que no exista actuación imprudente por parte del SUBCONTRATISTA, éste tendrá derecho a una indemnización por los daños y perjuicios que se le hubieren producido.

Mediciones

Entre los días [FECHAS] y [DÍA] de cada mes, EL SUBCONTRATISTA efectuará la medición a origen y valoración de las obras realizadas en el mes anterior.

Las mediciones valoradas de acuerdo con los precios fijados en el Anexo III y con los criterios establecidos en este contrato, constituirán la Certificación de la obra del mes, que deberá firmarse por la Dirección Facultativa para su aprobación o reparos y presentación a la Propiedad.

Si existiesen discrepancias en la medición o en la valoración de alguna partida, se recurrirá a la intervención de un perito imparcial designado por el Colegio de Arquitectos Superiores de [LOCALIDAD] ajeno a las partes y cuyos honorarios correrán a cargo de la parte que más se aleje de la valoración imparcial.

Las certificaciones expedidas de acuerdo con lo antes estipulado, se presentarán a la Propiedad, que dispondrá de [Nº] días naturales para formular su conformidad o reparos que serán resueltas al siguiente día de su manifestación por el adjudicatario y la dirección facultativa. En caso de no tener contestación se da por hecho su conformidad.

Facturación

Dentro de los [Nº DE DÍAS] primeros días de cada mes EL SUBCONTRATISTA entregará al CONTRATISTA en el domicilio consignado en este contrato factura original y [Nº] copias de los trabajos realizados y terminados a origen, haciendo constar los datos necesarios para poder comprobar la obra realizada y la identificación y localización de las distintas unidades, de tal manera que puedan ser verificadas incluso sin desplazarse a la obra.

Las certificaciones serán pagadas en el plazo de [Nº] días desde su aprobación.

El importe de la última certificación se pagará al tiempo de la recepción final de la obra que se consignará en el acta.

Las facturas, excepto la de liquidación, se consideran como pagos a cuenta, por lo que los pagos sucesivos de las mismas no implicarán conformidad ni renuncia del Contratista al derecho de formular reclamaciones.

Derecho de retención

Del importe de cada certificación, sin incluir el IVA ni los Gastos generales y el Beneficio industrial, EL CONTRATISTA retendrá un 5% en concepto de garantía de la correcta ejecución de la obra durante el plazo de un año desde la fecha del certificado de fin de obra.

Con carácter potestativo por parte del SUBCONTRATISTA, la retención podrá ser sustituida por un aval bancario, siendo los gastos que pueda originar dicho aval por cuenta exclusiva del SUBCONTRATISTA.

Aportación de materiales propios

EL CONTRATISTA podrá aportar elementos o materiales cuya adquisición pueda haber gestionado directamente, con la condición de advertir previamente al SUBCONTRATISTA, con una anticipación de [Nº] días/meses sobre la fecha prevista en el calendario de trabajo para la introducción o colocación de dichos materiales en la obra.

En ningún caso esta aportación de materiales por EL CONTRATISTA podrá superar el 20% del presupuesto y conllevará una reducción proporcional del presupuesto. La valoración de las posibles aportaciones por EL CONTRATISTA se realizará por la Dirección Facultativa

Obligaciones del contratista

Seguro

EL SUBCONTRATISTA se compromete a correr con todos los gastos derivados de la contratación de los seguros multirriesgos, debiendo no obstante tener como valor inicial asegurado al menos el de [IMPORTE] euros ( €) durante los primeros [Nº] meses, y siendo suficiente el valor de [IMPORTE] euros ( €) el resto del tiempo que reste por cumplir.

Sujeción a proyecto y presupuesto

Las obras se ejecutarán con estricta sujeción al contenido del proyecto y al presupuesto estipulado que sirve de base al contrato y conforme a las instrucciones que en interpretación técnica de éste diere al contratista el director técnico de la obra.

EL SUBCONTRATISTA cumplirá las órdenes que le sean dadas por el Jefe de Obra, encaminadas a la mejor ejecución de las obras según las instrucciones del Director de Obra. Antes de proceder a la ejecución de cada una de las partidas o trabajos de este contrato, EL SUBCONTRATISTA deberá obtener la conformidad del CONTRATISTA, quien le indicará el orden de preferencia a seguir y siempre respetando el Plan de desarrollo de la obra. No obstante, el proyecto podrá ser variado por EL CONTRATISTA, mediante notificación AL SUBCONTRATISTA, si fuera necesario para la buena marcha de la obra y sin perjuicio de las reclamaciones económicas que procediesen por las pérdidas que a éste le pudiera ocasionar la nueva programación.

EL SUBCONTRATISTA presentará en obra, con anterioridad a la colocación, una muestra de todos los elementos a instalar con los correspondientes accesorios para su aprobación por la Dirección de Obra y EL CONTRATISTA. No podrá instalar EL SUBCONTRATISTA elemento alguno no aprobado. El retraso en la presentación, será de su única responsabilidad.

Trabajos mal ejecutados

EL SUBCONTRATISTA tendrá que corregir a su cargo, o demoler y rehacer, cuantos trabajos haya ejecutado deficientemente a juicio del CONTRATISTA o del Director de Obra. Igualmente deberá reparar los desperfectos que cause en la obra y demoler la obra ejecutada no prevista en este contrato.

Daños al CONTRATISTA y/o a terceros

Serán de cuenta del SUBCONTRATISTA todos los daños que se causen al CONTRATISTA o a terceros como consecuencia de la mala ejecución de las obras, o por el empleo de materiales de inferior calidad a lo pactado en este contrato.

Vicios y defectos constructivos

Aun recibida definitivamente la obra y transcurrido el término de garantía, EL SUBCONTRATISTA responderá de los vicios ocultos de la construcción si los mismos aparecen en el plazo de diez años contados desde que concluyó la construcción.

Igualmente, en el Acta de recepción de la obra EL SUBCONTRATISTA se obliga a entregar al CONTRATISTA un seguro con la prima abonada que garantice al CONTRATISTA de los defectos o vicios de las instalaciones u obras llevadas a cabo por EL SUBCONTRATISTA en los términos del artículo 17 de la Ley 38/1999, de Ordenación de la Edificación.

Igualmente hará entrega al CONTRATISTA de la relación de suministradores de productos empleados en la obra y de las instrucciones para el uso y mantenimiento de los productos incorporados a la obra y las garantías de calidad de los mismos.

En el supuesto de incidencias surgidas en la ejecución del contrato de obras que puedan determinar, si no son resueltas, la imposibilidad de continuar la ejecución, podrá modificarse el presente contrato, a voluntad del contratista, y mediante la propuesta del director técnico de la obra.

Plazo de garantía

En relación con lo anterior, y sin perjuicio de la obligación del CONTRATISTA de realizar la obra en las debidas condiciones, de lo que debe responder en los términos legalmente establecidos, se pacta una garantía adicional de [Nº] meses durante los cuales atenderá cualquier reparación sin cargo alguno por sustitución de piezas defectuosas, y mano de obra y desplazamientos, siempre y cuando las averías no se deban a manipulaciones ajenas a su servicio técnico, inadecuado funcionamiento o causas imprevisibles como fallos en el suministro de energía eléctrica, incendios, inundaciones, etc.

El cómputo de los plazos de responsabilidad y garantía comenzará desde la fecha en que se suscriba el acta de recepción, o cuando se entienda tácitamente realizada si transcurren treinta días desde que se notifique a la propiedad la terminación mediante el certificado final de obra sin que ponga de manifiesto reservas o rechazo.

Prohibición de subcontratación

EL SUBCONTRATISTA no podrá subcontratar ninguna de las partidas sin la previa autorización del CONTRATISTA y siempre responderá solidariamente de lo que ejecutare la persona con quien hubiere subcontratado, tenga o no autorización del Contratista.

Recepción provisional de la obra

EL SUBCONTRATISTA comunicará por escrito en los [Nº] días siguientes a la terminación al CONTRATISTA la finalización de sus trabajos, procediéndose a su vez, dentro de los [Nº] días siguientes contados desde la misma fecha de la notificación, a levantar acta de recepción provisional de la obra o instalación con relación del importe total a que hayan ascendido los trabajos objeto de este contrato, y que firmarán EL CONTRATISTA y EL SUBCONTRATISTA y el Director de Obra.

La recepción provisional se suspenderá, haciendo constar en el acta las deficiencias si existieran.

En este supuesto EL SUBCONTRATISTA tendrá un plazo no superior a [Nº] días, para a su costa subsanar las deficiencias, las cuales se detallarán en el acta en la que se inicia la recepción provisional. En este momento EL SUBCONTRATISTA entregará una colección completa de planos en los que queden claramente reflejados todos los detalles de la instalación realizada, así como las normas de entretenimiento y conservación y se comprobará el funcionamiento de la misma.

Si la recepción provisional no se efectúa en el plazo indicado por causa del CONTRATISTA, se considerará verificada tal recepción a los [Nº] días de la fecha de notificación de la terminación de las obras.

Recepción definitiva de la obra

En el acta de recepción definitiva deberán estar presentes y firmarla, EL CONTRATISTA, EL SUBCONTRATISTA y el Director de Obra.

Obligaciones Laborales y de Seguridad Social

En todo lo relacionado con la contratación del personal se estará a lo que establezca la legislación laboral y sindical en vigor y será responsable civil y penalmente EL SUBCONTRATISTA del incumplimiento de dichas obligaciones y las sanciones que por dicho incumplimiento se derivaran.

En todo caso viene obligado a notificar al CONTRATISTA en el momento del pago de las certificaciones mensuales que se halla al corriente en el pago de los seguros sociales y cuantos otros pagos procedan en relación con el personal que exista en la obra, debiendo respetar también en cuanto a contratación de personal las normas laborales relativas sobre el particular.

Normas sobre seguridad e higiene en el trabajo

EL SUBCONTRATISTA viene obligado a cumplir y hacer cumplir todas y cada una de las Normas de Seguridad y Salud y además el Plan de Seguridad y Salud de la obra, del que se le entrega un ejemplar en este acto, siendo responsable EL SUBCONTRATISTA de que la totalidad de las instalaciones que use o instale en la obra se encuentren en correcto estado y no puedan producir perjuicio alguno a los trabajadores de la misma.

En el supuesto que el Director de Obra estimara conveniente la modificación del Plan de Seguridad e Higiene, deberá poner inmediatamente EL SUBCONTRATISTA los medios necesarios para la acomodación de la obra al plan modificado.

Resolución del contrato

Causas de resolución

Son causas de resolución del contrato:

1. La declaración de quiebra o suspensión de pagos del SUBCONTRATISTA.

2. El embargo de los enseres y materiales propiedad del SUBCONTRATISTA existentes en la obra, sean o no necesarios para la terminación de la misma.

4. El incumplimiento en la ejecución del contrato en un plazo superior a [PLAZO] (días/meses) [OTROS DATOS] por culpa del SUBCONTRATISTA.

5. El incumplimiento por parte del SUBCONTRATISTA en los plazos parciales que hagan prever racionalmente el que la obra no podrá terminarse en el plazo establecido ni con [PLAZO] (días/meses) de retraso con posterioridad a la fecha prevista como de finalización de obras.

6. La ejecución de la obra con deficiencias técnicas, calificadas de graves por el Director de Obra que se hayan puesto de manifiesto en los análisis de calidad, origen y resistencia de materiales empleados.

7. El incumplimiento reincidente por parte del Subcontratista debidamente advertido por EL CONTRATISTA o la Propiedad, de las Normas de Seguridad y Salud en el trabajo.

8. La falta de pago de una certificación de obra en los plazos establecidos en el presente contrato, siempre que el retraso sea superior a [Nº] días a partir de la fecha en que debiera haberse hecho efectivo.

9. La suspensión de las obras por resolución administrativa de los Tribunales o por decisión de la Propiedad o del CONTRATISTA por un plazo superior a meses o indefinida.

Resolución por causas imputables al SUBCONTRATISTA

La resolución del contrato por causas imputables al SUBCONTRATISTA se llevará a cabo por la Propiedad mediante documento del que quede constancia o requerimiento notarial a entregar en el domicilio del mismo, en el cual se expresará las circunstancias por las que se declara extinguido el contrato.

En este caso EL SUBCONTRATISTA vendrá obligado a abandonar la obra en un plazo de [Nº] días y, una vez abandonada la obra o en el mismo día que efectúe la retirada de los últimos materiales, se procederá a levantar el acta de la obra que esté ejecutada, suscribiendo la misma los representantes del CONTRATISTA y del SUBCONTRATISTA. Transcurrido el plazo de [Nº] días sin que EL SUBCONTRATISTA haya abandonado la obra, podrá EL CONTRATISTA, y así expresamente se pacta, proceder a ocupar la misma y continuar la realización de las obras previo levantamiento de acta notarial en el que quede constancia gráfica del estado en que se encuentra la misma y de las manifestaciones que estime oportuno hacer el Director de Obra.

Si EL SUBCONTRATISTA no retirase las instalaciones que tenga en la obra podrá seguirlas utilizando el nuevo SUBCONTRATISTA con abono, una vez finalizada la obra, del alquiler que corresponda.

Los materiales existentes en la obra se certificarán por el Director de Obra bajo su responsabilidad civil y penal y los mismos podrán ser utilizados en la terminación de la misma, abonándoseles al SUBCONTRATISTA si justifica que han sido abonados al proveedor o caso contrario directamente a éste en cuyo caso le serán descontados al SUBCONTRATISTA los importes pagados por los mismos.

Levantada acta por parte del CONTRATISTA y del SUBCONTRATISTA se procederá a hacer el abono de la obra ejecutada desde la última certificación en la forma establecida en el presente contrato y hará efectivos, con cargo a las retenciones, los daños y perjuicios que hubiere causado la resolución del contrato, sin perjuicio de que pueda EL CONTRATISTA reclamar los mayores daños o perjuicios que la resolución del contrato le ocasionare no cubiertos con las garantías.

Resolución por causas imputables al CONTRATISTA

Si la resolución del contrato se produjera por culpa del CONTRATISTA, deberá éste abonar al SUBCONTRATISTA el importe del % de las obras que faltarán por ejecutar, así como retornarle la totalidad del importe de las retenciones.

Recibidas las cantidades que se han establecido, EL SUBCONTRATISTA dejará la obra a disposición del CONTRATISTA, libre de todos los enseres. EL CONTRATISTA no podrá tomar posesión de la obra sin haber cumplido con los pagos y devoluciones establecidos.

Formalidades legales

EL CONTRATISTA y EL SUBCONTRATISTA declaran conocer la L. 32/2006 de 18 de octubre sobre subcontratación en el sector de la construcción, así como el R.D. 1108/2007 de 24 de agosto por el que se desarrolla la citada Ley, por lo que manifiestan:

1. Que cumplen los requisitos del artículo 4 de la Ley 32/2006

2. Que cada contratista dispondrá del libro de subcontratación que deberá permanecer en la obra, y en el que se reflejarán todas y cada una de las subcontrataciones, así como la documentación exigida en el artículo 8 de la Ley 32/2006

3. Que ambas empresas están inscritas en el Registro de Empresas Acreditadas

4. Que ambas empresas velarán para que todos los trabajadores que presten servicios en la obra tengan la formación necesaria y adecuada y cumplan la normativa de seguridad en la obra.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE SUBCONTRATACIÓN DE OBRA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(EL CONTRATISTA)

Fdo. Don [NOMBRE Y APELLIDOS]

(EL SUBCONTRATISTA)

========================================================================

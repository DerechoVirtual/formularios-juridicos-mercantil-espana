---
name: contrato-liquidez-sobre-acciones-propias-mer-0675
description: "Contrato de liquidez sobre acciones propias. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de liquidez sobre acciones propias

> Formulario **MER-0675** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de liquidez sobre acciones propias» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de liquidez sobre acciones propias” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-liquidez-sobre-acciones-propias-mer-0675`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] Nº

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

CONTRATO DE LIQUIDEZ

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO],

De otra:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EMISOR/ACCIONISTA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL PROVEEDOR DE LIQUIDEZ", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE LIQUIDEZ, de conformidad con las siguientes,

CLÁUSULAS

Objeto

El objeto del presente Contrato es establecer los términos y condiciones en virtud de los cuales el EMISOR/ACCIONISTA encomienda al PROVEEDOR DE LIQUIDEZ la ejecución de operaciones de compraventa de acciones de la Sociedad en el Mercado Alternativo Bursátil de acuerdo con el régimen previsto al respecto por las Circulares del Mercado Alternativo Bursátil 3/2008, de 22 de enero, 1/2009 de 9 de julio, sus Instrucciones Operativas de desarrollo y las normas que, eventualmente, sustituyan o modifiquen a las anteriores.

Actuación del proveedor de liquidez

El PROVEEDOR DE LIQUIDEZ tomará por sí sólo las decisiones operativas en relación con el mejor modo de conseguir los objetivos, señalados en el Expositivo Primero, de mantener una regularidad suficiente en la negociación de esas acciones y reducir las variaciones en el precio cuya causa no sea la tendencia del mercado Las operaciones que se realicen en ejecución del objeto del presente Contrato deberán llevarse a cabo en el Mercado Alternativo Bursátil, de acuerdo con sus normas de contratación y dentro de sus horarios ordinarios de negociación. El PROVEEDOR DE LIQUIDEZ no efectuará las operaciones de compraventa previstas en el presente Contrato a través de las modalidades de contratación de bloques ni de operaciones especiales, tal y como se definen en la normativa del Mercado Alternativo Bursátil. El PROVEEDOR DE LIQUIDEZ ejecutará las operaciones a través de un miembro del Mercado, o directamente si el PROVEEDOR DE LIQUIDEZ reviste esa condición.

Independencia del proveedor de liquidez

El PROVEEDOR DE LIQUIDEZ deberá mantener una estructura organizativa interna que garantice la independencia de actuación de los empleados encargados de gestionar el presente Contrato respecto a la Sociedad.

El PROVEEDOR DE LIQUIDEZ se compromete a no solicitar o recibir de la otra Parte ni de la Sociedad instrucción alguna sobre el momento, precio o demás condiciones de las órdenes que formule ni de las operaciones que ejecute en su actividad de PROVEEDOR DE LIQUIDEZ en virtud del presente Contrato. Tampoco podrá solicitar ni recibir información relevante de la Sociedad que no sea pública. En el supuesto de que el PROVEEDOR DE LIQUIDEZ actúe simultáneamente como Asesor Registrado, se adjuntará al presente contrato la descripción que haya presentado al Mercado en relación con los procedimientos y mecanismos que aplique en relación con la prevención y tratamiento de los eventuales conflictos de interés.

Disponibilidad de valores y efectivo

El EMISOR/ACCIONISTA en cuyo nombre y por cuya cuenta actúe el PROVEEDOR DE LIQUIDEZ pondrá a disposición del PROVEEDOR DE LIQUIDEZ el efectivo y/o las acciones que se indican a continuación para que éste pueda hacer frente a los compromisos que adquiera en ejecución del presente Contrato.

4.1 Cuenta de liquidez

El EMISOR/ACCIONISTA abrirá una cuenta de valores que llevará asociada una cuenta de efectivo, (a la que se aludirá como la "Cuenta de Liquidez"), en la que se practicarán los asientos derivados de las transacciones efectuadas y que se dotará inicialmente con las siguientes cantidades:

- acciones de la Sociedad

- [IMPORTE] €

4.2 Equilibrio de la Cuenta de Liquidez

Las Partes deberán asegurarse de que el volumen de acciones y el efectivo de la Cuenta de Liquidez sean adecuados a los parámetros de actuación del PROVEEDOR DE LIQUIDEZ exigidos por la regulación del Mercado Alternativo Bursátil. En caso de un desequilibrio entre el saldo de efectivo y de acciones de la Cuenta de Liquidez que determinara la imposibilidad de asegurar la continuidad de la operativa del Proveedor de Liquidez, de acuerdo con la aludida regulación, éste podrá comprar o vender acciones para equilibrar los saldos de efectivo y acciones disponibles. Estas operaciones no estarán sujetas a la finalidad prevista en el Expositivo Primero ni a los requisitos de actuación de la Cláusula Segunda del presente Contrato, y se realizarán con la mínima perturbación de las condiciones de mercado.

4.3 Sucesiva aportación o retirada de efectivo o acciones de la Cuenta de Liquidez

Si el PROVEEDOR DE LIQUIDEZ estimara que el efectivo o las acciones a su disposición en la Cuenta de Liquidez resultaran demasiado limitadas para asegurar la continuidad de su operativa o excesivas para ello, de acuerdo con la referida regulación del Mercado Alternativo Bursátil, lo pondrá en conocimiento del Emisor /Accionista. El EMISOR/ACCIONISTA podrá, en su caso, llevar a cabo nuevas aportaciones o retiradas de efectivo y/o acciones. El EMISOR/ACCIONISTA no podrá retirar acciones en número superior a las inicialmente aportadas debiendo, en ese caso, procederse a su venta en el mercado a través del Proveedor de Liquidez, sin que esas ejecuciones deban cumplir la finalidad prevista en el Expositivo Primero ni los requisitos de actuación de la Cláusula Segunda del presente Contrato.

Normativa sobre autocartera

Las Partes conocen que el presente Contrato deberá cumplir en todo momento los requisitos y límites establecidos para la adquisición de acciones propias en la normativa vigente en cada momento, en la medida en que ésta sea de aplicación. En esa medida, el EMISOR/ACCIONISTA deberá advertir de los límites precisos al PROVEEDOR DE LIQUIDEZ quién a su vez deberá mantener informado al EMISOR/ACCIONISTA a los efectos de su control.

Obligaciones informativas entre las partes

Las partes se transmitirán recíprocamente la información necesaria sobre la ejecución del contrato para que, en su caso, cada uno pueda dar cumplimiento a sus respectivas obligaciones legales.

Remuneración

El Proveedor de Liquidez, por la realización de la operativa regulada en el presente Contrato percibirá [detallar entre otros conceptos: el tipo de remuneración y la frecuencia de los pagos, teniendo en cuenta que el sistema de remuneración no aliente al PROVEEDOR DE LIQUIDEZ a influir artificialmente en el precio o volumen de cotización mediante la realización de operaciones.

Publicidad

Las Partes convienen en dar al presente Contrato la publicidad que venga determinada por la normativa aplicable al Mercado Alternativo Bursátil y, en su caso, a incluir información detallada del presente Contrato en la información relativa a la incorporación de las acciones de la Sociedad al referido Mercado.

Duración del contrato

El presente Contrato entrará en vigor el día en que comiencen a negociarse en el Mercado Alternativo Bursátil las acciones de la Sociedad y tendrá una duración indefinida. No obstante, ambas Partes tendrán la facultad de resolver anticipadamente el presente Contrato mediante una comunicación por escrito a la otra Parte, realizada con una antelación mínima de 60 días.

Resolución anticipada

El Contrato podrá ser resuelto unilateralmente, a instancia de una de las Partes, por incumplimiento de la otra Parte de cualquiera de las obligaciones asumidas en virtud del presente Contrato.

Efectos de la terminación

La terminación del Contrato determinará el vencimiento automático y la inmediata liquidez y exigibilidad de cuantas cantidades se deban recíprocamente las Partes. La terminación del Contrato dará lugar a la puesta a disposición del nuevo PROVEEDOR DE LIQUIDEZ que, en su caso, designe el Emisor/ Accionista, de las acciones de la Cuenta de Liquidez. En defecto de designación de Proveedor de Liquidez, las acciones serán puestas a disposición del EMISOR/ACCIONISTA, siempre respetando lo establecido en el tercer párrafo de la Cláusula 4.3.

Confidencialidad

Los términos de este Contrato así como cualquier información transmitida al amparo de lo previsto en el mismo serán confidenciales y no podrán ser revelados a terceros sin el previo consentimiento escrito de la otra Parte, salvo en caso de que la información sea de dominio público y en los restantes supuestos previstos en la legislación vigente y en el presente Contrato.

Protección de datos

En el caso de que la prestación de los Servicios suponga la necesidad de acceder a datos de carácter personal, las Partes quedan obligadas al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garnatía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable. El PROVEEDOR DE LIQUIDEZ responderá, por tanto, de las infracciones en que pudiera incurrir en el caso de que destine los datos personales a otra finalidad, los comunique a un tercero, o en general, los utilice de forma irregular, así como cuando no adopte las medidas correspondientes para el almacenamiento y custodia de los mismos. A tal efecto, se obliga a indemnizar por cualesquiera daños y perjuicios que sufra directamente, o por toda reclamación, acción o procedimiento, que traiga su causa de un incumplimiento o cumplimiento defectuoso por parte del PROVEEDOR DE LIQUIDEZ de lo dispuesto tanto en el Contrato como lo dispuesto en la normativa reguladora de la protección de datos de carácter personal.

A los efectos de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garnatía de los Derechos Digitales, el PROVEEDOR DE LIQUIDEZ únicamente tratará los datos de carácter personal a los que tenga acceso conforme a las instrucciones del EMISOR/ACCIONISTA y no los aplicará o utilizará con un fin distinto al objeto del Contrato, ni los comunicará, ni siquiera para su conservación, a otras personas. En el caso de que el PROVEEDOR DE LIQUIDEZ destine los datos a otra finalidad, los comunique o los utilice incumpliendo las estipulaciones del Contrato, será considerado también responsable del tratamiento, respondiendo de las infracciones en que hubiera incurrido personalmente.

El PROVEEDOR DE LIQUIDEZ deberá adoptar las medidas de índole técnica y organizativas necesarias que garanticen la seguridad de los datos de carácter personal y eviten su alteración, pérdida, tratamiento o acceso no autorizado, habida cuenta del estado de la tecnología, la naturaleza de los datos almacenados y los riesgos a que están expuestos, ya provengan de la acción humana o del medio físico o natural. A estos efectos el PROVEEDOR DE LIQUIDEZ deberá aplicar las medidas técnicas y organizativas apropiadas para garantizar un nivel de seguridad adecuado al riesgo, conforme al artículo 32 del Reglamento (UE) 2016/679 (RGPD).

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sin cláusula penal / Sumisión a tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal / Sumisión a tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Sumisión a arbitraje / Sumisión a Arbitraje sin cláusula penal en caso de no ejecución voluntaria del laudo / Con cláusula penal / Sumisión a Arbitraje con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE LIQUIDEZ, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(EL ACCIONISTA/EMISOR)

Fdo. Don [NOMBRE Y APELLIDOS]

(EL PROVEEDOR DE LIQUIDEZ)

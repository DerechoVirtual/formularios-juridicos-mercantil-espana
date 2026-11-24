---
name: contrato-servicios-integracion-sistemas-informaticos-mer-0774
description: "Contrato de servicios de integración de sistemas informáticos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicios de integración de sistemas informáticos

> Formulario **MER-0774** del plugin **Contratos tecnológicos, comercio electrónico y protección de datos** (`formularios-tecnologia-y-proteccion-de-datos`) · Mercantil › Tecnología, comercio electrónico y protección de datos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicios de integración de sistemas informáticos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicios de integración de sistemas informáticos” para mi caso». También puedes invocarla directamente con `/formularios-tecnologia-y-proteccion-de-datos:contrato-servicios-integracion-sistemas-informaticos-mer-0774`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-tecnologia-y-proteccion-de-datos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos tecnológicos, comercio electrónico y protección de datos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (10 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (5 veces)
- [ ] Nº (5 veces)
- [ ] AÑO (3 veces)
- [ ] DÍA (3 veces)
- [ ] MES (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] PLAZO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] ACTIVIDAD
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIBIR
- [ ] FECHAS
- [ ] IMPORTE EN LETRA
- [ ] LUGAR
- [ ] Nº DE REFERENCIA
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

CONTRATO DE INTEGRACIÓN DE SISTEMAS

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS] mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA EMPRESA INFORMÁTICA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL CLIENTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE INTEGRACIÓN DE SISTEMAS, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO Que LA EMPRESA INFORMÁTICA es una mercantil que tiene por objeto social la creación, desarrollo, integración, mantenimiento y comercialización de programas y equipos informáticos.

SEGUNDO Que el CLIENTE es una sociedad mercantil que tiene por objeto social la [ACTIVIDAD] y desea contratar con LA EMPRESA INFORMÁTICA los Servicios Profesionales relacionados con el Desarrollo, Integración y Mantenimiento de un programa informático, en adelante el "Proyecto", conforme a la oferta que LA EMPRESA INFORMÁTICA presentó el [FECHA] con numero de referencia [Nº DE REFERENCIA], en adelante la " Propuesta".

TERCERO Que ambas partes están interesadas en que la EMPRESA INFORMÁTICA desarrolle una aplicación informática que se ajuste a las necesidades del CLIENTE, por lo que ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

El objeto de este contrato es la ejecución del Proyecto consistente en [DESCRIBIR] en los términos y condiciones establecidos en las Propuesta de LA EMPRESA INFORMÁTICA de fecha [FECHA] presentada al Cliente y que queda incorporada al presente contrato como Anexo I, formando parte integrante del mismo a todos los efectos.

Precio

El precio de los servicios descritos en la cláusula primera se concreta en la cantidad de [IMPORTE] euros ( €) más el Impuesto sobre el Valor Añadido correspondiente, esto es, [IMPORTE] euros ( €) adicionales. El precio total de la operación asciende a la cantidad [IMPORTE] euros ( €).

[ELEGIR UNA OPCIÓN: Forma de pago / Pago no aplazado / Opción 3.1:Pago no aplazado / Pago aplazado / Opción 3.2:Pago aplazado]

Pago a tercero

El precio total de la operación asciende a la cantidad [IMPORTE] euros ( €), de los cuales en este acto EL CLIENTE entrega a LA EMPRESA INFORMÁTICA [IMPORTE] euros ( €). Los restantes [IMPORTE] euros ( €) las retendrá EL CLIENTE en su poder para satisfacer con ella la deuda de [IMPORTE] euros ( €) por orden de LA EMPRESA INFORMÁTICA, sin que por ello asuma responsabilidad personal alguna.

Plazos de desarrollo e instalación del sistema

El desarrollo e instalación del sistema objeto del presente contrato se ajustará a las siguientes fases:

Fase de Pruebas

En ella la EMPRESA INFORMÁTICA realizará todas las pruebas necesarias para la comprobación del buen funcionamiento y compatibilidad del sistema desarrollado con el sistema informático del CLIENTE.

Esta fase se iniciará entre los días [FECHAS] y [DÍA] del mes de [MES] de [AÑO] el plazo de [Nº] días desde la firma del presente contrato.

Fase de modificaciones

En el caso de que durante la fase de pruebas surja la necesidad de llevar a cabo una serie de modificaciones en el sistema desarrollado, LA EMPRESA INFORMÁTICA realizará las modificaciones que sean oportunas durante un plazo máximo de [Nº] días a contar desde la finalización de la fase anterior.

Fase de instalación definitiva

La instalación definitiva del sistema se efectuará antes del día [DÍA] de [MES] de [AÑO].

En este momento la EMPRESA INFORMÁTICA hará entrega de toda la documentación para el desarrollo y uso del sistema informático instalado, incluido el manual de instrucciones.

Retraso en la entrega

Para el caso de incumplimiento del plazo final de entrega establecido en la Cláusula anterior, las Partes acuerdan una penalización de [IMPORTE] euros por día de retraso, siempre que éste sea imputable a la EMPRESA INFORMÁTICA.

El retraso en más de [PLAZO] dará derecho al CLIENTE a reclamar la penalización por retraso prevista o a pedir la resolución del contrato, con abono en ambos casos de la indemnización por los daños y perjuicios causados.

Propiedad intelectual

Todos los derechos de propiedad industrial y/o intelectual propiedad del CLIENTE sobre productos, documentos, información, especificaciones etc. que sea necesario utilizar para la prestación de los servicios objeto del presente proyecto, seguirán siendo propiedad de ésta, sin que LA EMPRESA INFORMÁTICA adquiera ningún derecho sobre los mismos.

Los derechos de autor y otros derechos de propiedad intelectual sobre cualesquiera materiales, productos y/o programas de ordenador o software (ya sean en formato impreso o formato máquina) creados por o licenciados a LA EMPRESA INFORMÁTICA con anterioridad al presente Contrato o fuera de él, así como sobre cualesquiera modificaciones subsiguientes de los mismos (en adelante "Trabajos Preexistentes") continuarán siendo de la propiedad del LA EMPRESA INFORMÁTICA (o de su licenciador). Ni el CLIENTE ni LA EMPRESA INFORMÁTICA podrán verse restringidas o limitadas en forma alguna, en virtud del presente Contrato, para el desarrollo y o uso en el futuro de cualesquiera técnicas, ideas, conceptos, información o Know-how relativos a métodos o procesos de aplicación general, incluidos aquellos en el campo de la tecnología de la información y los procesos de negocio.

Asimismo, será propiedad del CLIENTE todo producto resultado de la prestación de servicios objeto del presente proyecto, no pudiendo LA EMPRESA INFORMÁTICA utilizarlo para con otros clientes sin la previa autorización por escrito del CLIENTE. LA EMPRESA INFORMÁTICA entregará al CLIENTE toda la información generada para poder efectuar, si procede, el registro en la Propiedad Intelectual. El CLIENTE será el titular de la propiedad y de los derechos de distribución de los productos generados.

Cesión de derechos

LA EMPRESA INFORMÁTICA cede de manera exclusiva al CLIENTE, que los acepta, sus derechos de reproducción, explotación y/o comercialización tanto sobre el sistema desarrollado, como sobre todos los datos, listados, diagramas y esquemas elaborados en la fase de análisis, el manual de instrucciones o los restantes materiales de apoyo, los símbolos de identificación en todo el mundo, incluyendo España, por todos los medios, formatos y procedimientos conocidos y por conocer, y con duración de los mencionados derechos de por vida.

Garantía

LA EMPRESA INFORMÁTICA garantiza el buen funcionamiento del sistema durante un periodo máximo de [PLAZO], dentro de los cuales deberá costear aquellas reparaciones que sean necesarias para corregir los errores que el software pudiera presentar.

No obstante lo anterior, no se considerará cubierta por la presente cláusula de garantía los supuestos de negligencia en el manejo del programa. Para determinar los supuestos en que ha existido negligencia habrá de estarse a lo dispuesto en las instrucciones de LA EMPRESA INFORMÁTICA fabricante

[ELEGIR UNA OPCIÓN: Responsabilidad / Exoneración de responsabilidad de la empresa informática / Opción 1:Exoneración de responsabilidad de la empresa informática / Responsabilidad de la empresa informática / Opción 2:Responsabilidad de la empresa informática]

Mantenimiento

LA EMPRESA INFORMÁTICA se obliga a prestar al CLIENTE la asistencia técnica necesaria para prevenir, evitar y corregir errores y, en su caso, realizar adaptaciones y mejoras en el sistema desarrollado.

El servicio de mantenimiento incluirá las siguientes prestaciones por parte de LA EMPRESA INFORMÁTICA:

a) Mantenimiento correctivo, formado por todas aquellas operaciones que LA EMPRESA INFORMÁTICA se obliga a realizar para corregir o reparar los fallos del sistema. Estas labores de mantenimiento se realizarán después de haberse presentado el fallo y tendrán como finalidad el funcionamiento correcto del mismo.

b) Mantenimiento preventivo, formado por todas aquellas operaciones que LA EMPRESA INFORMÁTICA se obliga a realizar a intervalos regulares de [Nº] días/semanas/meses, y durante todo el tiempo de duración del contrato que se fija en [PLAZO] Este mantenimiento tendrá por finalidad conservar el sistema en condiciones adecuadas de funcionamiento, evitando la presencia de fallos en el mismo.

El precio convenido a pagar por EL CLIENTE en concepto de servicio de mantenimiento es de [IMPORTE] € [IMPORTE EN LETRA]

El precio incluye los gastos de desplazamiento que en su caso deba efectuar el personal de LA EMPRESA INFORMÁTICA a las oficinas del CLIENTE así como el valor de los materiales que, en su caso, se les proporcione durante el tiempo que duren las reparaciones

Formación

LA EMPRESA INFORMÁTICA se obliga a prestar al personal del CLIENTE la formación precisa para la correcta y óptima utilización del sistema. La duración del proceso de formación será de

El pago se efectuará el día [FECHA] en la cuenta corriente nº [NÚMERO] que LA EMPRESA INFORMÁTICA tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL]

El precio incluye los gastos de desplazamiento que en su caso deba efectuar el personal de LA EMPRESA INFORMÁTICA a las oficinas del CLIENTE así como el valor de los materiales que, en su caso, se les proporcione durante el tiempo que duren las reparaciones.

Pacto de no contratación

El CLIENTE se compromete a no contratar a persona alguna de las que prestan sus servicios para la EMPRESA INFORMÁTICA. La presente cláusula extenderá su vigencia incluso con posterioridad a la extinción del presente contrato por un período de [Nº] años.

En caso de incumplimiento del presente acuerdo, EL CLIENTE estará obligado a indemnizar a la EMPRESA INFORMÁTICA con la cantidad de [IMPORTE] euros.

Resolución del contrato

El Contrato podrá resolverse por las siguientes causas:

1.Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2.Por acuerdo de las Partes por escrito.

3.La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de … días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sin cláusula penal / Sumisión a tribunales sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal / Sumisión a tribunales con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Sumisión a Arbitraje sin cláusula penal en caso de no ejecución voluntaria del laudo / Con cláusula penal / Sumisión a Arbitraje con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE INTEGRACIÓN DE SISTEMAS, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(El Cliente)

Fdo. Don [NOMBRE Y APELLIDOS]

(La empresa informática)

---
name: contrato-arrendamiento-negocio-industria-funcionamiento-mer-0831
description: "Contrato de arrendamiento de un negocio o industria en funcionamiento. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de arrendamiento de un negocio o industria en funcionamiento

> Formulario **MER-0831** del plugin **Traspasos de negocio, confidencialidad y acuerdos de empresa** (`formularios-traspasos-y-acuerdos-de-empresa`) · Mercantil › Otros documentos mercantiles · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de arrendamiento de un negocio o industria en funcionamiento» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de arrendamiento de un negocio o industria en funcionamiento” para mi caso». También puedes invocarla directamente con `/formularios-traspasos-y-acuerdos-de-empresa:contrato-arrendamiento-negocio-industria-funcionamiento-mer-0831`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-traspasos-y-acuerdos-de-empresa:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Traspasos de negocio, confidencialidad y acuerdos de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] Nº (5 veces)
- [ ] NÚMERO (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DOCUMENTO ACREDITATIVO
- [ ] DÍA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MEDIO DE PAGO
- [ ] MES
- [ ] Nº DE FINCA
- [ ] TOMO

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

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA ARRENDADORA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA ARRENDATARIA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE ARRENDAMIENTO DE INDUSTRIA, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que LA ARRENDADORA es propietaria en régimen de plena propiedad y dominio del local sito en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de [Nº] metros cuadrados inscrito en el Registro de la Propiedad de [LOCALIDAD] en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca [Nº DE FINCA] e inscripción número [NÚMERO], en el que se desarrolla la actividad de

Que en el mencionado local se ubican la maquinaria y accesorios que figuran en el Anexo I, todos ellos afectos al desarrollo de la actividad anteriormente y sobre los que no versa carga ni gravamen alguno.

Que LA ARRENDADORA es titular del citado negocio, según se desprende de [DOCUMENTO ACREDITATIVO] (alta en actividades económicas, cámaras de comercio, colegios profesionales).

Que el mencionado local se encuentra libre de cargas y gravámenes y al corriente en el pago de impuestos.

SEGUNDO.- Que LA ARRENDATARIA se encuentra interesada en el arrendamiento de la industria titularidad de LA ARRENDADORA para continuar ejerciendo en ella la actividad industrial/comercial/profesional que hasta ahora se venía realizando.

TERCERA.- Como quiera que ambas partes se encuentran interesadas en el arrendamiento de la industria supra referida, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

Constituye el objeto del presente contrato el arrendamiento de la Industria descrita en el Exponendo Primero.

[ELEGIR UNA OPCIÓN: Traspaso / En el momento de la firma / Con posterioridad / — y además elegir: Renta / Renta fija / Renta variable]

Actualización de la renta

Transcurrido el primer año de vigencia del presente contrato, la renta pactada será actualizada anualmente en función de la evolución anual experimentada por el Índice General de Precios al Consumo del Instituto Nacional de Estadística.

La renta actualizada será exigible a LA ARRENDATARIA a partir del mes siguiente a aquél en que LA ARRENDADORA se lo notifique por escrito y expresando el porcentaje de alteración aplicado. Se considerará valida la notificación hecha mediante anotación en el recibo de la mensualidad precedente.

Duración del contrato

El presente contrato se concluye por un plazo de [Nº] años pudiendo prorrogarse, a voluntad de las partes y de común acuerdo por períodos anuales.

Si llegado el vencimiento del plazo inicial o de cualquiera de sus prórrogas, alguna de las partes decidiera dar por finalizado el presente contrato, deberá de comunicar su intención a la otra parte con al menos dos meses de antelación a la fecha del vencimiento a través de un medio que deje constancia de su recepción.

Cesión de trabajadores

LA ARRENDATARIA queda subrogada en los derechos y obligaciones laborales y de la Seguridad Social de LA ARRENDADORA, incluyendo los compromisos de pensiones y, en general, cuantas obligaciones en materia de protección social complementaria hubiera adquirido LA ARRENDADORA.

Garantía

LA ARRENDADORA garantiza el pleno funcionamiento de las instalaciones, así como de la maquinaria, bienes y accesorios inventariados en el Anexo I y necesarios para el desempeño de la actividad descrita en el Exponendo I durante un periodo máximo de [Nº] meses, dentro de los cuales deberá costear aquellas reparaciones que sean necesarias para el correcto ejercicio de la actividad.

No obstante lo anterior, no se considerará cubierta por la presente cláusula de garantía los supuestos de negligencia de LA ARRENDATARIA en la utilización, manejo y conservación de local, maquinarias, bienes y accesorios anteriormente referidos.

LA ARRENDATARIA deberá permitir el acceso al local de negocio a LA ARRENDADORA y a los operarios o industriales mandados por ésta para la realización, inspección y comprobación de cualquier clase de obras o reparaciones que afecten al inmueble.

Régimen de responsabilidad

Sin perjuicio de las acciones que pudieran corresponderle frente a terceros, LA ARRENDATARIA es directa y exclusivamente responsable de los daños que pudieran irrogarse a las personas o cosas que deriven, directa o indirectamente, del ejercicio de la actividad traspasada.

Licencias, permisos y autorizaciones

LA ARRENDATARIA gestionará y sufragará a su exclusiva cuenta y cargo, todas las licencias, permisos, autorizaciones, obras de adecuación, etc., que la actividad descrita en el Exponendo Primero requiera, con independencia de que sean exigidos por la Administración Central, Autonómica o Local y cumplirá con todas aquellas disposiciones, ordenanzas o exigencias de cualquier autoridad y organismo competente que a tal fin le sean requeridos.

Conservación y mantenimiento

Durante el periodo de vigencia del presente contrato, los gastos de mantenimiento del local e instalaciones, reposición de elementos averiados, etc. serán de cargo exclusivo de LA ARRENDATARIA, quien deberá mantener el local e instalaciones en las condiciones óptimas de conservación y uso para el desempeño de la actividad.

LA ARRENDATARIA deberá permitir el acceso al local de negocio a LA ARRENDADORA y a los operarios o industriales mandados por ésta para la inspección y comprobación del estado del inmueble.

Obras que no sean de conservación o mantenimiento no autorizadas

LA ARRENDATARIA no podrá realizar sin el consentimiento escrito de LA ARRENDADORA obras de ninguna clase que no sean las de mera conservación y mantenimiento.

Obras que no sean de conservación o mantenimiento autorizadas

Se autoriza a LA ARRENDATARIA para realizar las obras de acondicionamiento del local con el fin de adaptarlo a las necesidades de su comercio. Tales obras deberán quedar ultimadas en el plazo de [Nº] meses contados desde la fecha de este contrato y quedarán en beneficio del local sin que por ello LA ARRENDATARIA tenga derecho a percibir indemnización de ninguna clase.

Fianza

LA ARRENDATARIA entrega a LA ARRENDADORA la cantidad de [IMPORTE] euros ( €) en concepto de fianza y garantía adicional. Esta fianza deberá ser restituida en su integridad, o descontando la cantidad que sea necesaria para reponer el local e instalaciones en las condiciones óptimas para el desempeño de la actividad descrita en el Exponendo Primero.

La existencia de esta fianza no será obstáculo para que LA ARRENDADORA pueda instar el desahucio por falta de pago. La fianza no devengará interés a favor de LA ARRENDATARIA.

Prohibición de cesión, subarriendo o traspaso

Se prohíbe a LA ARRENDATARIA a ceder, subrogar, traspasar o subarrendar total o parcialmente el negocio objeto de este contrato.

Seguro

LA ARRENDATARIA contratará un seguro que resulte satisfactorio para LA ARRENDADORA y que cubra el riesgo de daños o pérdida que pueda sufrir el local, maquinaria y bienes afectos al ejercicio de la actividad durante todo el periodo de vigencia del presente contrato.

LA ARRENDATARIA proporcinará a LA ARRENDADORA, a su solicitud, pruebas de la existencia de dicho seguro. La cobertura incluirá, entre otros aspectos, los daños provocados por incendios, agua, fenómenos naturales y robo.

[ELEGIR UNA OPCIÓN: Pacto de no concurrencia / De la arrendadora / Exclusividad]

Confidencialidad

LA ARRENDATARIA se obliga a no revelar, ceder o transferir a terceros ninguna información referente a los negocios, clientes, operaciones, instalaciones, cuentas o finanzas de LA ARRENDADORA, ni sus procedimientos, métodos, transacciones, "know-how", o cualquier otro aspecto relacionado con la actividad de dicha entidad que pueda conocer o haya conocido con motivo de la prestación de servicios prevista en el presente contrato.

LA ARRENDATARIA se responsabilizará de que las personas que están a su cargo se sujeten a las limitaciones establecidas en esta cláusula.

Se entiende que cualquiera de las partes podrá revelar la información confidencial a sus asesores, contables y abogados siempre que se enmarque en el asesoramiento sobre asuntos relacionados con este acuerdo.

El incumplimiento de este compromiso conllevará la obligación de indemnizar los daños y perjuicios causados.

Resolución del contrato

El incumplimiento de las obligaciones que resulten del presente contrato facultará a la parte que cumpla los suyos a exigir a la otra su cumplimiento, o, a su elección, a resolver el contrato, con abono en ambos casos de la indemnización por daños y perjuicios que proceda.

Opción de compra

LA ARRENDADORA concede gratuitamente a LA ARRENDATARIA durante la vigencia de este contrato un derecho de opción de compra del negocio arrendado por un precio de [IMPORTE] euros ( €), del cual se deducirán las cantidades abonadas en concepto de renta por LA ARRENDATARIA hasta el momento en que haga uso de la opción de compra.

Dicho precio se abonará en [MEDIO DE PAGO] (medio de pago) en el momento de hacer uso de la opción y el negocio se transmitirá libre de cargas y gravámenes y al corriente en el pago de impuestos.

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

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE ARRENDAMIENTO DE INDUSTRIA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo. Don [NOMBRE Y APELLIDOS]

(La Arrendadora)

Fdo. Don [NOMBRE Y APELLIDOS]

(La Arrendataria)

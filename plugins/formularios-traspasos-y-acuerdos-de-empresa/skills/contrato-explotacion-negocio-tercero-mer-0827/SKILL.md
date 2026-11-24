---
name: contrato-explotacion-negocio-tercero-mer-0827
description: "Contrato de explotación de un negocio por tercero. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de explotación de un negocio por tercero

> Formulario **MER-0827** del plugin **Traspasos de negocio, confidencialidad y acuerdos de empresa** (`formularios-traspasos-y-acuerdos-de-empresa`) · Mercantil › Otros documentos mercantiles · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de explotación de un negocio por tercero» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de explotación de un negocio por tercero” para mi caso». También puedes invocarla directamente con `/formularios-traspasos-y-acuerdos-de-empresa:contrato-explotacion-negocio-tercero-mer-0827`.
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
- [ ] Nº (8 veces)
- [ ] NÚMERO (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DÍA
- [ ] ESCALERA
- [ ] FOLIO
- [ ] LIBRO
- [ ] LUGAR
- [ ] MEDIO DE PAGO
- [ ] MES
- [ ] NORMATIVA SUPLETORIA
- [ ] Nº DE FINCA
- [ ] PLAZO
- [ ] TIPO DE NEGOCIO
- [ ] TOMO
- [ ] TÍTULO ACREDITATIVO DE LA TITULARIDAD

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

CONTRATO DE EXPLOTACIÓN DE NEGOCIO

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS] mayor de edad, de estado civil [ESTADO CIVIL] vecino de [LOCALIDAD] domiciliado en [DOMICILIO] con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS] mayor de edad, de estado civil [ESTADO CIVIL] vecino de [LOCALIDAD] domiciliado en [DOMICILIO] con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D. [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA ARRENDADORA en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS] en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA ARRENDATARIA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS] en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE EXPLOTACIÓN DE NEGOCIO, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO Que LA ARRENDADORA es propietaria en régimen de plena propiedad y dominio del local sito en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de [Nº] metros cuadrados inscrito en el Registro de la Propiedad de [LOCALIDAD] en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca [Nº DE FINCA] e inscripción número [NÚMERO], en el que se desarrolla la actividad de

Que LA ARRENDADORA es titular del citado negocio, según se desprende de [TÍTULO ACREDITATIVO DE LA TITULARIDAD]

Que el mencionado local se encuentra libre de cargas y gravámenes y al corriente en el pago de impuestos.

SEGUNDO. Que el objeto de arrendamiento es el negocio de [TIPO DE NEGOCIO] que en el local se ha establecido, de tal manera que el objeto del contrato es una unidad patrimonial con vida propia, susceptible de ser inmediatamente explotada.

TERCERA Como quiera que ambas partes se encuentran interesadas en la explotación del negocio supra referido, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

Constituye el objeto del presente contrato la explotación del negocio descrito en el Exponendo Primero.

Traspaso

Las partes manifiestan que lo arrendado es el negocio que en el local se ha establecido, de tal manera que el objeto del contrato es una unidad patrimonial con vida propia, susceptible de ser inmediatamente explotada.

Además, como explotación de negocio, comprende y se hace entrega de una serie de elementos materiales aptos para el ejercicio de la actividad a la que se va a dedicar, contemplados en el Anexo I.

El arrendatario declara recibir el local, el uso del negocio ya instalado, con los elementos precisos y coordinados para su puesta en marcha inmediata y en perfecto estado de conservación.

[ELEGIR UNA OPCIÓN: Renta / Renta fija / Renta variable]

Actualización de renta

Ambas partes acuerdan que la renta se actualizará cada año según el Índice General Nacional del Sistema de Índices de Precios de Consumo en un período de doce meses inmediatamente anteriores a la fecha de cada actualización, tomando como mes de referencia para la primera actualización el que corresponda al último índice publicado en la fecha de celebración del contrato, y en las sucesivas el que corresponda al último aplicado.

La renta actualizada será exigible a LA ARRENDATARIA a partir del mes siguiente a aquél en que LA ARRENDADORA se lo notifique por escrito y expresando el porcentaje de alteración aplicado. Se considerará valida la notificación hecha mediante anotación en el recibo de la mensualidad precedente.

Duración del contrato

El plazo por el que se arrienda la explotación del negocio será de [Nº] meses/años, a partir de la firma del presente contrato. Llegada la fecha de vencimiento del contrato, LA ARRENDATARIA podrá prorrogar el contrato a su voluntad, por períodos anuales sucesivos hasta un máximo de [PLAZO] anualidades. El presente contrato se concluye por un plazo de [Nº] años pudiendo prorrogarse, a voluntad de las partes y de común acuerdo por períodos anuales.

No obstante, transcurridos los primeros [Nº] meses, cuyo plazo es de duración obligatoria para LA ARRENDATARIA, ésta podrá rescindir el contrato anticipadamente, sin esperar a su finalización, siempre y cuando lo notifique fehacientemente a LA ARRENDADORA con un preaviso mínimo de [Nº] meses de antelación a la fecha de desalojo, viniendo obligado a abonar el recibo de alquiler hasta la fecha de desalojo y entrega de llaves.

Cesión de trabajadores

LA ARRENDATARIA queda subrogada en los derechos y obligaciones laborales y de la Seguridad Social de LA ARRENDADORA, incluyendo los compromisos de pensiones y, en general, cuantas obligaciones en materia de protección social complementaria hubiera adquirido LA ARRENDADORA.

Garantía

LA ARRENDADORA garantiza el pleno funcionamiento de las instalaciones, así como de la maquinaria, bienes y accesorios inventariados en el Anexo I y necesarios para el desempeño de la actividad descrita en el Exponendo I durante un periodo máximo de [Nº] meses, dentro de los cuales deberá costear aquellas reparaciones que sean necesarias para el correcto ejercicio de la actividad.

No obstante lo anterior, no se considerará cubierta por la presente cláusula de garantía los supuestos de negligencia de LA ARRENDATARIA en la utilización, manejo y conservación de local, maquinarias, bienes y accesorios anteriormente referidos.

LA ARRENDATARIA deberá permitir el acceso al local de negocio a LA ARRENDADORA y a los operarios o industriales mandados por ésta para la realización, inspección y comprobación de cualquier clase de obras o reparaciones que afecten al inmueble.

Régimen de responsabilidad

LA ARRENDATARIA se hace directa y exclusivamente responsable de cuantos daños puedan ocasionarse a terceras personas o cosas, y sean consecuencia directa o indirecta del negocio instalado, del mal uso del mismo, y de la actuación de sus empleados, eximiendo de toda responsabilidad al arrendador y al administrador por dichas causas..

Licencias, permisos y autorizaciones

LA ARRENDATARIA gestionará y sufragará a su exclusiva cuenta y cargo, todas las licencias, permisos, autorizaciones, obras de adecuación, etc., que la actividad descrita en el Exponendo Primero requiera, con independencia de que sean exigidos por la Administración Central, Autonómica o Local y cumplirá con todas aquellas disposiciones, ordenanzas o exigencias de cualquier autoridad y organismo competente que a tal fin le sean requeridos.

Gastos

Serán de cuenta de la parte arrendataria los gastos generales que se produzcan a partir del día de hoy en los servicios de (aire acondicionado, luz, teléfono escalera [ESCALERA]). El importe de dichos gastos será repercutido a LA ARRENDATARIA en el recibo del alquiler según se vayan produciendo.

Los gastos generales para el adecuado sostenimiento del inmueble, sus servicios, tributos, cargas y responsabilidades serán a cargo de LA ARRENDATARIA; se exceptúa la parte correspondiente a los gastos extraordinarios o por instalaciones que no deban considerarse consecuencia del uso, reparación ordinaria o entretenimiento de los elementos y servicios comunes. Los gastos se revalorizarán anualmente en la misma proporción que la renta.

[ELEGIR UNA OPCIÓN: Conservación y mantenimiento / Con autorización para obras extraordinarias / Sin autorización para obras extraordinarias]

Fianza

LA ARRENDATARIA entrega a LA ARRENDADORA la cantidad de [IMPORTE] euros ( €) en concepto de fianza y garantía adicional. Esta fianza deberá ser restituida en su integridad, o descontando la cantidad que sea necesaria para reponer el local e instalaciones en las condiciones óptimas para el desempeño de la actividad descrita en el Exponendo Primero.

Cada vez que el arrendamiento se prorrogue, LA ARRENDADORA podrá exigir que la fianza sea incrementada, o LA ARRENDATARIA que disminuya, hasta hacerse igual a una mensualidad de la renta vigente al tiempo de la prórroga..

Prohibición de cesión, subarriendo o traspaso

Se prohíbe a LA ARRENDATARIA a ceder, subrogar, traspasar o subarrendar total o parcialmente el negocio objeto de este contrato.

PACTO DE NO CONCURRENCIA

No concurrencia de LA ARRENDADORA

LA ARRENDADORA se compromete a no realizar durante la vigencia del presente contrato actividades por cuenta propia o ajena que de algún modo pudieran suponer competencia para LA ARRENDATARIA.

Del mismo modo, durante la vigencia del presente contrato LA ARRENDADORA no podrá adquirir participación ni derecho alguno en negocios o empresas que desarrollen una actividad concurrente con la de LA ARRENDATARIA, ni participar, activa o pasivamente, en ningún tipo de gestión conducente al desarrollo de este tipo de actividades.

El incumplimiento de este compromiso conllevará la obligación de indemnizar los daños y perjuicios causados.

No concurrencia de LA ARRENDATARIA

Durante un periodo de [Nº] años a contar desde la extinción del presente contrato, LA ARRENDATARIA se compromete a no realizar durante actividades por cuenta propia o ajena que de algún modo pudieran suponer competencia para LA ARRENDADORA.

Del mismo modo, durante la vigencia del presente contrato LA ARRENDATARIA no podrá adquirir participación ni derecho alguno en negocios o empresas que desarrollen una actividad concurrente con la de LA ARRENDADORA, ni participar, activa o pasivamente, en ningún tipo de gestión conducente al desarrollo de este tipo de actividades.

El incumplimiento de este compromiso conllevará la obligación de indemnizar los daños y perjuicios causados.

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

Jurisdicción competente y ley aplicable

Las partes se someten a los Juzgados y Tribunales del lugar donde radica el negocio o empresa.

El presente contrato se regirá por lo aquí pactado y en su defecto [NORMATIVA SUPLETORIA], en cuanto no se oponga al contenido del presente, por lo dispuesto en la Ley 29/1994 de 24 de noviembre de Arrendamientos Urbanos.

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE EXPLOTACIÓN DE NEGOCIO, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La Arrendadora)

Fdo. Don [NOMBRE Y APELLIDOS]

(La Arrendataria)

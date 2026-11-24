---
name: contrato-venta-negocio-industria-mer-0832
description: "Contrato de venta de un negocio o industria. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de venta de un negocio o industria

> Formulario **MER-0832** del plugin **Traspasos de negocio, confidencialidad y acuerdos de empresa** (`formularios-traspasos-y-acuerdos-de-empresa`) · Mercantil › Otros documentos mercantiles · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de venta de un negocio o industria» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de venta de un negocio o industria” para mi caso». También puedes invocarla directamente con `/formularios-traspasos-y-acuerdos-de-empresa:contrato-venta-negocio-industria-mer-0832`.
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
- [ ] NÚMERO (4 veces)
- [ ] FECHA (3 veces)
- [ ] Nº (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DOCUMENTO ACREDITATIVO
- [ ] DÍA
- [ ] FOLIO
- [ ] IMPORTE
- [ ] LIBRO
- [ ] LUGAR
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

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA VENDEDORA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA COMPRADORA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE COMPRAVENTA DE INDUSTRIA, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que LA VENDEDORA es propietaria en régimen de plena propiedad y dominio del local sito en [LOCALIDAD], calle [CALLE] número [NÚMERO] con una superficie de [Nº] metros cuadrados inscrito en el Registro de la Propiedad de [LOCALIDAD] en el Tomo [TOMO], Libro [LIBRO], Folio [FOLIO], Finca [Nº DE FINCA] e inscripción número [NÚMERO], en el que se desarrolla la actividad de

Que en el mencionado local se ubican la maquinaria y accesorios que figuran en el Anexo I, todos ellos afectos al desarrollo de la actividad anteriormente y sobre los que no versa carga ni gravamen alguno.

Que LA VENDEDORA es titular del citado negocio, según se desprende de [DOCUMENTO ACREDITATIVO] (alta en actividades económicas, cámaras de comercio, colegios profesionales).

Que el mencionado local se encuentra libre de cargas y gravámenes y al corriente en el pago de impuestos.

SEGUNDO.- Que LA COMPRADORA se encuentra interesada en adquirir la titularidad de la industria de LA VENDEDORA para continuar ejerciendo en ella la actividad industrial/comercial/profesional que hasta ahora se venía realizando.

TERCERA.- Como quiera que ambas partes se encuentran interesadas en la compraventa de la industria supra referida, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

Constituye el objeto del presente contrato la compraventa de la Industria descrita en el Exponendo Primero.

[ELEGIR UNA OPCIÓN: Traspaso / En el momento de la firma / Con posterioridad]

Precio

El precio de la venta de la industria descrita en el exponendo primero se concreta en la cantidad de [IMPORTE] euros ( €).

[ELEGIR UNA OPCIÓN: Pago / Forma de pago / No aplazado / Aplazado]

Cláusula de reserva de dominio

La venta se entiende hecha con reserva de dominio a favor de la VENDEDORA, hasta el momento en que el importe total del presente contrato de compraventa haya sido satisfecho, esto es, hasta el día [FECHA]

En el supuesto de que por cualquier otra causa, como por ejemplo el robo, la COMPRADORA fuera privada del bien objeto de este contrato, ésta deberá ponerlo en conocimiento inmediato de la VENDEDORA con el fin de que pueda adoptar las acciones que estime oportunas al respecto, sin que por ello se vea liberada de la obligación del pago íntegro del precio. En el supuesto de que la parte COMPRADORA omitiera esta obligación, se entenderá que existe responsabilidad por su parte en el destino final del bien y mala fe en su comportamiento.

Asimismo, la COMPRADORA responderá de los daños y perjuicios que sobrevinieran al negocio traspasado, incluso por caso fortuito, durante el periodo de vigencia de la obligación suspensiva.

La cláusula de reserva de dominio a favor de la parte VENDEDORA quedará automáticamente extinguida en el momento en que la COMPRADORA haya pagado la totalidad del precio pactado. De esta forma, el negocio vendido pasará a ser de plena propiedad de la COMPRADORA sin limitación alguna.

Por el contrario, si llegado el vencimiento de cualquiera de los pagos éste no se hubiera verificado, la COMPRADORA deberá devolver el negocio adquirido en virtud del presente contrato de forma inmediata, encontrándose un representante de la mercantil VENDEDORA plenamente legitimado para recuperar el objeto de este contrato a su voluntad sin necesidad de procedimiento especial alguno, ya que para tal fin le faculta la misma desde el momento de la suscripción de este contrato.

La enajenación o la realización de cualquier otro acto de disposición en tanto no se haya verificado efectivamente el pago requerirá la autorización previa y por escrito de la VENDEDORA.

Cesión de trabajadores

LA COMPRADORA queda subrogada en los derechos y obligaciones laborales y de la Seguridad Social de LA VENDEDORA, incluyendo los compromisos de pensiones y, en general, cuantas obligaciones en materia de protección social complementaria hubiera adquirido LA VENDEDORA.

Garantía

LA VENDEDORA garantiza el pleno funcionamiento de las instalaciones, así como de la maquinaria, bienes y accesorios inventariados en el Anexo I y necesarios para el desempeño de la actividad descrita en el Exponendo I durante un periodo máximo de [Nº] meses, dentro de los cuales deberá costear aquellas reparaciones que sean necesarias para el correcto ejercicio de la actividad.

No obstante lo anterior, no se considerará cubierta por la presente cláusula de garantía los supuestos de negligencia de LA COMPRADORA en la utilización, manejo y conservación de local, maquinarias, bienes y accesorios anteriormente referidos.

LA COMPRADORA deberá permitir el acceso al local de negocio a LA VENDEDORA y a los operarios o industriales mandados por ésta para la realización, inspección y comprobación de cualquier clase de obras o reparaciones que afecten al inmueble.

Licencias, permisos y autorizaciones

LA COMPRADORA gestionará y sufragará a su exclusiva cuenta y cargo, todas las licencias, permisos, autorizaciones, obras de adecuación, etc., que la actividad descrita en el Exponendo Primero requiera, con independencia de que sean exigidos por la Administración Central, Autonómica o Local y cumplirá con todas aquellas disposiciones, ordenanzas o exigencias de cualquier autoridad y organismo competente que a tal fin le sean requeridos.

Pacto de no concurrencia

LA VENDEDORA se compromete a no realizar durante la vigencia del presente contrato actividades por cuenta propia o ajena que de algún modo pudieran suponer competencia para LA COMPRADORA.

Del mismo modo, durante la vigencia del presente contrato LA VENDEDORA no podrá adquirir participación ni derecho alguno en negocios o empresas que desarrollen una actividad concurrente con la de LA COMPRADORA, ni participar, activa o pasivamente, en ningún tipo de gestión conducente al desarrollo de este tipo de actividades.

El incumplimiento de este compromiso conllevará la obligación de indemnizar los daños y perjuicios causados.

Confidencialidad

LA VENDEDORA se obliga a no revelar, ceder o transferir a terceros ninguna información referente a los negocios, clientes, operaciones, instalaciones, cuentas o finanzas de LA COMPRADORA, ni sus procedimientos, métodos, transacciones, "know-how", o cualquier otro aspecto relacionado con la actividad de dicha entidad que pueda conocer o haya conocido con motivo de la prestación de servicios prevista en el presente contrato.

El incumplimiento de este compromiso conllevará la obligación de indemnizar los daños y perjuicios causados.

Evicción (Contienda pendiente)

LA COMPRADORA conoce que LA VENDEDORA ha tenido que sustanciar un procedimiento judicial contrata un tercero que pretendía reclamar [DESCRIPCIÓN DEL BIEN], que es objeto de este contrato.

LA VENDEDORA responderá solamente de la posesión legal pero no de la posesión pacífica. LA COMPRADORA acepta la limitación establecida por LA VENDEDORA a su derecho de saneamiento.

Resolución del contrato

El incumplimiento de las obligaciones que resulten del presente contrato facultará a la parte que cumpla los suyos a exigir a la otra su cumplimiento, o, a su elección, a resolver el contrato, con abono en ambos casos de la indemnización por daños y perjuicios que proceda.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de la parte

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE COMPRAVENTA DE INDUSTRIA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La VENDEDORA)

Fdo. Don [NOMBRE Y APELLIDOS]

(La COMPRADORA)

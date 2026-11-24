---
name: contrato-transporte-mercancias-ejecucion-continuada-mer-0514
description: "Contrato de transporte de mercancías de ejecución continuada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de transporte de mercancías de ejecución continuada

> Formulario **MER-0514** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de transporte de mercancías de ejecución continuada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de transporte de mercancías de ejecución continuada” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-transporte-mercancias-ejecucion-continuada-mer-0514`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] FECHA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº (3 veces)
- [ ] DNI/NIE (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DE LA MERCANCÍA
- [ ] DÍA
- [ ] LOCALIDAD DE DESTINO
- [ ] LOCALIDAD DE ORIGEN
- [ ] LUGAR
- [ ] MES
- [ ] NIF
- [ ] NÚMERO
- [ ] SEDE
- [ ] SI EL CARGADOR FUERA UN AUTÓNOMO RELLENAR SEGÚN LO INDICADO
- [ ] SI EL PORTEADOR FUERA UN AUTÓNOMO RELLENAR SEGÚN LO INDICADO
- [ ] TIPO DE AUTORIZACIÓN DE TRANSPORTE
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 16 Ley 15/2009
- art. 22.3 Ley 15/2009
- art. 38 Ley 15/2009
- art. 1.124 Código Civil
- art. 25 Ley 12/1992

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

DE UNA PARTE, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI número [DNI/NIE], en nombre y representación de [ con domicilio en [LOCALIDAD], con CIF número, en virtud de poder otorgado ante Notario el día [FECHA] que asevera vigente. En adelante PORTEADOR

[SI EL PORTEADOR FUERA UN AUTÓNOMO RELLENAR SEGÚN LO INDICADO] De una parte, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, [estado civil], con domicilio en [LOCALIDAD], que cuenta con NIF número [NIF]. En adelante PORTEADOR.

DE OTRA PARTE, D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI número [DNI/NIE], en nombre y representación de [ con domicilio en [LOCALIDAD], con CIF número, en virtud de poder otorgado ante Notario el día [FECHA] que asevera vigente. En adelante CARGADOR.

[SI EL CARGADOR FUERA UN AUTÓNOMO RELLENAR SEGÚN LO INDICADO] De otra parte, D./Dña. [], mayor de edad, [estado civil], con domicilio en [], que cuenta con NIF número []. En adelante CARGADOR.

Ambas partes se reconocen capacidad suficiente para otorgar este CONTRATO DE TRANSPORTE CONTINUADO DE MERCANCÍAS y

EXPONEN

I. Que el PORTEADOR cuenta con una flota adecuada de vehículos y que tiene capacidad suficiente según manifiesta, para prestar servicios en materia de transporte de mercancías por carretera. Además, es titular de la autorización administrativa necesaria para prestar servicios de transporte público de mercancías por carretera de conformidad con el ordenamiento vigente, encontrándose dado de alta en el Impuesto de Actividades Económicas, disponiendo de los medios personales y materiales y está interesado en realizar el transporte de mercancías (si es preciso indicar el tipo de mercancía) con los vehículos adscritos a su autorización.

II. Que el CARGADOR se dedica, entre otras actividades, al transporte de mercancías, actividad que es sabida por el PORTEADOR (ya que ha venido prestando el servicio de transporte objeto del presente contrato, desde hace más de [Nº] años, procediéndose en este momento a la formalización escrita del presente contrato ya pactado anteriormente entre ambas partes, de conformidad con la obligación contenida en el Real Decreto-Ley 14/2022 de 1 de agosto por el que se modifica el artículo 16 de la Ley 15/2009.

Asimismo, está interesado en que el PORTEADOR le preste los servicios de transporte de mercancías que este le encomiende, mediante los vehículos adscritos a la autorización mencionada en el punto I.

III. Que el PORTEADOR manifiesta su interés en realizar el transporte, la distribución y entrega de las mercancías con los vehículos adscritos a su autorización de [TIPO DE AUTORIZACIÓN DE TRANSPORTE] desde [LOCALIDAD DE ORIGEN], hasta [LOCALIDAD DE DESTINO], (o indicar transporte nacional y/o internacional) y, por ello, capacitado para tal actividad, además está interesado en contratar los servicios de transporte ofrecidos por [DENOMINACIÓN SOCIAL].

IV. Y que, habiendo llegado las partes a un acuerdo libre y espontaneo de sus voluntades, formalizan el presente CONTRATO DE TRANSPORTE CONTINUADO, en adelante “el Contrato”, al objeto de constituir y regular su acuerdo, el cual se regirá por lo previsto en la Ley de Ordenación de Transportes Terrestres y el Reglamento que la desarrolla; la Ley 15/2009, de 11 de noviembre, de Contrato de Transporte Terrestre de Mercancías; y la Orden FOM/1882/2012, de 1 de agosto, por la que se aprueban las condiciones generales de contratación de los transportes de mercancías por carretera aprobadas por el Ministerio de Fomento. Asimismo, el contrato se regirá de conformidad con las condiciones y pactos que se establecen en las siguientes

ESTIPULACIONES

PRIMERA. - OBJETO

Por medio del presente contrato, el PORTEADOR se obliga frente al CARGADOR a realizar por su propia cuenta, riesgo y ventura el transporte por carretera de las mercancías descritas en la estipulación siguiente, en los términos y condiciones fijadas por las Partes en este Contrato, desde diferentes puntos de origen y destino.

El ámbito territorial en el que el PORTADOR prestará sus servicios será el correspondiente al continente europeo (si es internacional también indicarlo).

En ningún caso la firma del presente contrato, ni de los ANEXOS al mismo, supone el compromiso ni la obligación para el CARGADOR de solicitar al PORTEADOR un número o volumen mínimo de transportes diarios, semanales, mensuales o anuales, ni confiere a el PORTEADR derecho de exclusiva alguno.

El PORTEADOR se compromete a utilizar un vehículo adecuado para las mercancías del CARGADOR, siempre y cuando el CARGADOR haya notificado, previamente de la puesta a disposición del vehículo, de la naturaleza de dichas mercancías.

Se permite/No se permite que, la realización de este servicio de transporte sea subcontratado total o parcialmente a un porteador distinto al designado en este contrato.[EN EL CASO DE PERMITIRSE, AÑADIR y SI NO LO AUTORIZA INDICAR QUE NO].Si el PORTEADOR subcontratase el total o parte del transporte informará al CARGADOR de este hecho.

La empresa cargadora comunicará periódicamente al porteador por los medios habituales (correo electrónico, WhatsApp...) las características del servicio que fueran necesarias para su prestación, al menos con la antelación de 24 horas.

SEGUNDA. - MERCANCÍAS OBJETO DEL TRANSPORTE

El PORTEADOR se obliga a realizar el transporte de la siguiente mercancía descrita en la carta de porte nº / albarán nº [NÚMERO], de [DESCRIPCIÓN DE LA MERCANCÍA] que se une a este contrato formando parte de este. Las Partes acuerdan que el CARGADOR deberá acondicionar, embalar y señalizar la mercancía descrita para su transporte, y responderá ante el PORTEADOR de los daños a personas, al material de transporte o a otras mercancías, así como de los gastos ocasionados por defectos en el acondicionamiento, embalaje o señalización. Salvo que tales defectos sean manifiestos o conocidos por el PORTEADOR en el momento de hacerse cargo de las mercancías y no haya hecho las oportunas reservas.

Asimismo, el CARGADOR deberá poner a disposición del PORTEADOR la documentación relativa a la mercancía que sea necesaria para la realización del transporte y de todos aquellos trámites que el PORTEADOR deba efectuar antes de proceder a la entrega de la mercancía en el lugar de destino indicado. El PORTEADOR solo podrá utilizar dicha documentación para los citados fines, siendo responsable de la pérdida o mala utilización de esta.

Los soportes utilizados para el transporte de las mercancías (paletas, cajas, envases, etc.) aportados por el CARGADOR o el expedidor forman parte integrante del envío no podrá exigirse el establecimiento o depósito de garantía alguna en relación con ellos al porteador. El transporte de retorno de los mencionados soportes vacíos constituirá, en todo caso, objeto de un envío de transporte distinto.

EN EL CASO DE UTILIZAR DOCUMENTACIÓN ELECTRÓNICA se podría añadir lo siguiente:

Las Partes se comprometen que esta documentación se genere en formato electrónico.

TERCERA. - LUGAR DE CARGA Y LUGAR DE ENTREGA DE LAS MERCANCÍAS

El CARGADOR se compromete a poner la mercancía a disposición del PORTEADOR en el lugar de carga que resulte de la Carta deporte/ Orden de carga.

El PORTEADOR transportará la mercancía objeto del transporte: desde el lugar de carga hasta el de entrega en destino que resulte de la carta de porte, siguiendo la ruta más adecuada teniendo en cuenta las circunstancias de la operación y las características de la mercancía y la pondrá a disposición de destinatario el día y hora previstos en la Carta de Porte.

CUARTA. - REALIZACIÓN DE LAS LABORES DE CARGA Y DESCARGA

[DEBE TENERSE EN CUENTA LO SANCIONADO POR EL REAL DECRETO-LEY 3/2022 EN CUANTO A LA PROHIBICIÓN DE REALIZAR LA CARGA Y LA DESCARGA POR PARTE DEL CONDUCTOR]

El CARGADOR se compromete a realizar las labores de carga y/o descarga de la mercancía en el lugar de recepción/entrega de estas mencionado en el apartado anterior de la manera más eficiente y rápida, cumpliendo con las previsiones y prohibiciones legales en esta materia, en particular las previstas en la LOTT, Ley 15/2009 del contrato de transporte y Prevención de Riesgos Laborales.

Como excepción a esta regla, cabe establecer una excepción basada en estas 2 circunstancias:

Si hay un pacto contrario por escrito con el transportista previo al inicio del servicio de transporte y además se le abona al transportista una remuneración específica por la ejecución de la carga o descarga. Esta debe figurar en una línea separada en la factura y debe ser acordada directamente con el transportista (la reforma de Ley del Transporte operada en 2022 no establece ninguna cifra en concreto para este concepto).
Existe el caso particular de los vehículos con capacidad superior a las 7,5 toneladas de MMA. Para este tipo de vehículos, queda prohibido que realicen la carga y descarga salvo en el caso de transportes de mudanzas y guardamuebles, vehículos cisterna, áridos o vehículos con grúa, portavehiculos, paquetería o bultos fácilmente manipulables y transporte de animales vivos. Esta medida entrará en vigor 6 meses después de la publicación, es decir, a partir del 2 de septiembre de 2022, fecha en que los conductores de este tipo de vehículos solo podrán ejecutar la carga y descarga en las excepciones marcadas.

Cuando el vehículo haya de esperar un plazo superior a una hora hasta que se concluya su carga o descarga, el PORTEADOR podrá exigir al CARGADOR una indemnización en concepto de PARALIZACIÓN. Dicho plazo se contará desde la puesta a disposición del vehículo para su carga o descarga. El importe de la indemnización por paralización será el estipulado en el artículo 22.3 de la Ley 15/2009, de 11 de noviembre, del contrato de transporte terrestre de mercancías.

QUINTA. - DURACIÓN DEL TRANSPORTE

Las Partes acuerdan que el servicio de transporte objeto de este contrato tiene una duración de [Nº] semanas/meses/años y será renovado automáticamente si ninguna de las partes pone en conocimiento, con al menos UN MES de antelación a la fecha de su vencimiento, de la otra su voluntad de modificar lo pactado aquí o la extinción del Contrato en los [Nº] días/semanas/meses, antes de que concluya la duración de éste o cualquiera de sus prórrogas.

SEXTA. - AUTONOMÍA DEL PORTADOR

El PORTEADOR gozará de plena autonomía en el ejercicio de su actividad empresarial, organizando y ejecutando libremente su actividad de transporte por cuenta propia, con medios materiales y personales propios, con las técnicas y procedimientos propios y fuera del ámbito organizativo y de dirección de la Parte CARGADORA.

El PORTEADOR garantiza al CARGADOR su total indemnidad frente a la responsabilidad que pueda derivarse de las relaciones de aquél con las personas físicas o jurídicas vinculadas a la ejecución del objeto de este contrato.

SÉPTIMA. – SEGUROS Y DOCUMENTACIÓN

[ESTE PUNTO DEBERÁ EXISTIR EN CASO DE QUE EXISTA ALGÚN TIPO DE SEGURO SOBRE LAS MERCANCÍAS]

El conjunto de las mercancías objeto del transporte previsto en este Contrato se encuentra asegurado mediante un seguro de la siguiente clase: en la compañía aseguradora:

Las Partes declaran estar al corriente en la información de la suscripción de las pólizas de los seguros citados anteriormente.

En cualquier momento de la vigencia de este contrato, el CARGADOR podrá solicitar al PORTEADOR los documentos justificativos del cumplimiento de las obligaciones descritas anteriormente (copia de habilitaciones administrativas necesarias para el ejercicio de la actividad, de empresa, conductores y vehículos; seguros obligatorios de circulación y pago de primas; certificaciones de estar al corriente de pagos con Agencia Tributaria y Seguridad Social; copia, en su caso, de seguros de RC y mercancías y pago de primas.

OCTAVA. - PRECIO DEL TRANSPORTE Y FORMA DE PAGO

(EN ESTE APARTADO SE ACONSEJA CONTAR CON UN ANEXO EN EL QUE SE ESPECIFIQUEN CON CLARIDAD LAS TARIFAS A TENER EN CUENTA PARA CADA TIPO DE TRANSPORTE QUE SE LLEVE A CABO, UTILIZÁNDOSE VARIOS PARÁMETROS COMO KM RECORRIDOS, TONELADAS, PRECIO FIJO, O CUALQUIER OTRO CONCEPTO QUE LAS PARTES CONVENGAN).

El CARGADOR se compromete a pagar al transportista el precio del transporte fijado en este contrato y acordado en fecha (indicar la fecha en que se ha tomado para revisión de precio y, en su caso, si proviene de un contrato previo), que se encuentra en vigor actualmente, sometido a lo pactado de la siguiente manera:

(Imprescindible que se detalle expresamente o poner que consta en el ANEXO I del presente contrato especificando que es parte integrante del mismo.)

El precio podrá ser objeto de revisión cuando se alcance el 5% o más de variación en el precio del combustible desde que se fijó el precio del trasporte y que lo fue en fecha [FECHA] y en todo caso de forma trimestral, conforme a la previsión contenida en el artículo 38 de la Ley 15/2009, de 11 de noviembre, del contrato de transporte terrestre de mercancías. En este caso se aplicará la variación acumulada desde el inicio del trimestre hasta el final de éste.

Para calcular la variación del precio del combustible se tomará en cuenta la publicación llevada a cabo por el Ministerio de Transportes, Movilidad y Agenda Urbana, dentro de la Sección “Transporte Terrestre”. A continuación, accederemos a la Sección “Servicios al transportista” y dentro de esta pestaña, entraremos en el apartado incrementos de “Precios del gasóleo”.

En caso de proceder a la revisión se procederá de conformidad a la fórmula contenida en las condiciones generales de contratación del transporte de mercancías por carretera indicada a continuación pudiendo variar dependiendo del peso del vehículo utilizado para el transporte:

-Vehículos con una masa máxima autorizada igual o superior a 20.000 kilogramos:

ΔP=G×P×0,4 / 100

- Vehículos con una masa máxima autorizada superior a 3.500 kilogramos e inferior a 20.000 kilogramos:

ΔP=G×P×0,3 / 100

-Vehículos con una masa máxima autorizada igual o inferior a 3.500 kilogramos:

ΔP=G×P×0,2 / 100

Teniendo en cuenta que:

a) ΔP: significa la cantidad que el porteador deberá incrementar o disminuir el precio contratado.

b) G: supone el índice de variación del precio medio del combustible (gasóleo, gas...) hecho público por la Administración (tal y como se ha indicado anteriormente obtenido de la publicación del MITMA) entre el momento en que se fijó el precio del transporte y aquél en que se realizó efectivamente. La fecha de fijación del precio en el presente contrato formalizado por escrito lo fue en fecha:

c) P: es el precio del transporte establecido al contratar.

La variación de precio en la factura deberá aparecer de manera desglosada, haciendo constar expresamente y de forma diferenciada “variación del precio de combustible”.

El precio, se pagará mensualmente por parte de la CARGADORA mediante [ÓRGANO], previa presentación por el transportista de la factura correspondiente, en la que se hará constar los servicios realizados mensualmente, y en su caso la variación del precio conforme a lo establecido en la estipulación anterior, y en el caso de estar permitidas las operaciones de carga y descarga el desglose del precio por realizar dichas operaciones, pago que se efectuará dentro de los quince días siguientes al mes facturado.

Todos los gastos de consumo de gasoil, seguros de vehículos, reparaciones y cualquier otro de mantenimiento del vehículo correrá a cargo del PORTEADOR.

El PORTEADOR desempeñará su cometido con los elementos - todo ello de su propiedad- de transporte, maquinaria y personal, necesarios, a su riesgo y ventura. Asimismo, podrá contratar, en su nombre, el personal que estime oportuno para el desarrollo y cumplimiento de los trabajos encomendados y asumidos en este contrato, personal que no tendrá relación ni vínculo laboral alguno con la sociedad contratante. En consecuencia, asume el compromiso de cumplir y sufragar cuantas obligaciones laborales y de Seguridad Social se le atribuyan en consonancia con las normas legales en vigor.

Ambas Partes se comprometen a que el precio del transporte no podrá, en ningún caso, resultar inferior a la cifra resultante de los costes efectivos en los que recaiga el transportista al realizar los servicios de transporte.

NOVENA. - RESPONSABILIDAD DE LAS PARTES. FUERZA MAYOR

La responsabilidad de las Partes se regirá por lo previsto en la Ley 15/2009, de 11 de noviembre, del contrato de transporte terrestre de mercancías, la LOTT, las Condiciones Generales de Contratación y normas de desarrollo y complementarias.

A los efectos de este contrato los retrasos derivados de un accidente de circulación, pinchazo o reventón de una rueda, impedimentos a la libre circulación (como manifestaciones, cortes de tráfico, etc.), tendrán la consideración de fuerza mayor y deberán de ser comunicados a la mayor brevedad al cargador.

DECIMA. – COMUNICACIONES

Todas las comunicaciones que en virtud de este contrato deban o debieran ser enviadas, lo serán por un medio fehaciente que deje constancia del momento en que ha sido enviada, el medio por el que ha sido enviada y el momento de su recepción por la otra Parte, y se interpretarán como correctamente enviadas al PORTEADOR o al CARGADOR, si se dirigieran a las direcciones postales de estos que figuran en este Contrato. Cada una de las Partes puede, por medio de notificación escrita enviada a la otra Parte, cambiar la dirección a la que deban dirigirse estas comunicaciones.

Serán válidas a efectos de este contrato las comunicaciones realizadas a los correos electrónicos de las partes, que se consignan a continuación, siempre que se acredite el momento en que se ha enviado, la dirección a la que se envió y el momento de recepción.

E-mail CARGADOR:

E-mail PORTEADOR:

Del mismo modo, podrá hacerse por cualquier medio que pruebe tanto su contenido como su recepción por el destinatario indicado. Toda notificación realizada de este modo surtirá efecto desde la fecha de su recepción, y lo será en los domicilios respectivos indicados en el encabezamiento.

DECIMOPRIMERA. - INTEGRIDAD DEL CONTRATO Y ANULABILIDAD

Este Contrato deja sin efecto todo acuerdo, compromiso y/o negociación que se hubiese celebrado previamente entre las Partes respecto del transporte objeto de este contrato.

DECIMOSEGUNDA. - LEGISLACIÓN APLICABLE

Las Partes se obligan por el presente Contrato, que tiene carácter mercantil -y, por tanto, no le será aplicable el derecho laboral, en cuanto se quiera mantener una interpretación extensiva del mismo-así como sus correspondientes Anexos comprometiéndose a su cumplimiento e interpretación de buena fe.

Las partes dan por reproducidas y aceptan las condiciones generales de contratación de los transportes de mercancías por carretera publicadas por la Orden FOM/1882/2012, de 1 de agosto, por la que se aprueban las condiciones generales de contratación de los transportes de mercancías por carretera aprobadas el Ministerio de Fomento en materia de transporte y demás disposiciones que estuvieren vigentes al tiempo de su celebración y hasta su terminación, que junto con la Ley de Transporte Terrestre de Mercancías de 15/2009, de 11 de noviembre, de Contrato de Transporte Terrestre de Mercancías, con las modificaciones introducidas en el artículo 38 por el Real Decreto-Ley 3/2022 que incorpora la aplicación de la cláusula de Revisión del Precio del Transporte en su artículo 2 apartado 3 y en la disposición transitoria primera y la Ley de Ordenación del Transporte Terrestre junto al Reglamento que la desarrolla se aplicarán en todo lo no previsto en el presente contrato.

DECIMOTERCERA. - RESOLUCIÓN DEL CONTRATO

Se permite la posibilidad de que el presente Contrato pueda ser resuelto por el mutuo acuerdo de las Partes, con los efectos determinados por las Partes. De igual modo, podrá ser resuelto en cualquier momento por cada una de las Partes, a su elección, sin necesidad de intervención judicial y sin perjuicio de la responsabilidad en la que incurra la otra Parte por su incumplimiento contractual por “causa justificada”, descrita aquí como:

El incumplimiento total o parcial por la otra Parte de alguna de las condiciones u obligaciones esenciales de este Contrato que no sea corregido en el plazo de diez días a partir de la notificación escrita y fehaciente enviada para que así se haga; o
Las demás establecidas en este Contrato y por la Ley.

El incumplimiento por cualquiera de las Partes de las obligaciones que emanan del presente Contrato otorgará derecho a la Parte que hubiera procedido correctamente a exigir el cumplimiento de la obligación o a promover la resolución del Contrato de acuerdo con lo dispuesto en el artículo 1.124 del Código Civil.

En todo caso, las causas de resolución citadas anteriormente, indistintamente si una u otra, dará derecho a la otra Parte que no hubiera incurrido en ella o no la hubiera provocado, a la indemnización de daños y perjuicios derivados de la misma.

El hecho de que cualquiera de las partes no utilice una de las causas previstas en esta estipulación para resolver el Contrato no se entenderá como renuncia a sus derechos derivados del incumplimiento de la otra Parte y, por ende, no perjudicará su posición jurídica para hacerle cumplir las obligaciones derivadas del presente Contrato.

En casos de resolución unilateral injustificada y sin preaviso, ante la falta de regulación expresa sobre los daños y perjuicios causados por la falta de preaviso, cabe aplicar analógicamente lo previsto en el art. 25 de la Ley 12/1992, de 27 mayo, del Contrato de Agencia.

La falta de preaviso, que permitiera al transportista reorientar su actividad comercial, supone una infracción de los deberes de lealtad y buena fe en el desarrollo de una relación contractual como la presente, sin que concurra ninguna circunstancia que justifique su omisión.

DECIMOCUARTA. - CONFIDENCIALIDAD Y DATOS DE CARÁCTER PERSONAL

Las Partes se obligan a que toda la información que reciban como consecuencia de la ejecución del presente contrato, bien se refieran a la otra parte contratante o a terceros, haya sido o no notificada con el carácter de confidencial, será manejada con carácter estrictamente confidencial y solamente estará destinada para la correcta aplicación del presente contrato.

Las Partes también se obligan a que en el momento de extinción del presente contrato o si la otra parte lo solicita en cualquier momento, a devolver y entregar a su legítimo titular todo documento o información que pudiera haber recibido u obtenido en ejecución del presente contrato. Toda divulgación de información no autorizada o consentida por su legítimo titular de la que las partes hayan tenido conocimiento o constancia será sancionada conforme a la legislación aplicable.

Cada una de las Partes autoriza que aquellos datos de carácter personal que pudieran haber facilitado a la otra con ocasión de la celebración y ejecución del presente contrato, podrán ser incorporados a ficheros automatizados de datos de carácter personal de gestión de clientes o proveedores, titularidad del TRANSPORTISTA o del CARGADOR. Ambas Partes señalan los domicilios que aparecen en el encabezamiento del presente documento a los efectos del ejercicio de los derechos de acceso, oposición, rectificación y cancelación establecidos por la normativa en materia de protección de datos de carácter personal.

El PORTEADOR reconoce que las informaciones son estrictamente confidenciales, comprometiéndose a no utilizarlos fuera del marco de dichas negociaciones o relaciones y, por ello, será responsable de los perjuicios que sufra el CARGADOR motivados por el incumplimiento de esta obligación.

DECIMOQUINTA. - SUMISIÓN A ARBITRAJE Y RENUNCIA DE FUERO

Las Partes con renuncia al fuero que pudiera corresponderles se someten expresamente, para cuantas cuestiones se deriven del presente contrato, a la Jurisdicción de los Tribunales de [LOCALIDAD].

En caso de controversia, diferencia, conflicto o reclamación en cuanto al Contrato, o en relación con o derivado de la interpretación o ejecución de este, las Partes acuerdan que se someterán a la jurisdicción de las Juntas Arbitrales de [SEDE]. Y en prueba de conformidad y aceptación de todo lo establecido, ambas Partes firman en el lugar y fechas señalados en el encabezamiento, a un solo efecto, todas las hojas de este Contrato en dos ejemplares, uno para cada Parte.

Y en prueba de conformidad y aceptación de todo lo establecido, ambas Partes firman en el lugar y fechas señalados en el encabezamiento, a un solo efecto, todas las hojas de este Contrato en dos ejemplares, uno para cada Parte.

EL PORTEADOREL CARGADOR

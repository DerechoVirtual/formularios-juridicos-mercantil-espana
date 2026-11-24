---
name: contrato-agencia-sin-exclusiva-asuncion-riesgo-agente-mer-0491
description: "Contrato de agencia sin exclusiva con asunción del riesgo por el agente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de agencia sin exclusiva con asunción del riesgo por el agente

> Formulario **MER-0491** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de agencia sin exclusiva con asunción del riesgo por el agente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de agencia sin exclusiva con asunción del riesgo por el agente” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-agencia-sin-exclusiva-asuncion-riesgo-agente-mer-0491`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] CALLE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] NIF (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PLAZO (2 veces)
- [ ] ACTIVIDAD
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FECHA
- [ ] FOLIO
- [ ] LIBRO
- [ ] MES
- [ ] OTROS DATOS
- [ ] PORCENTAJE
- [ ] TOMO
- [ ] ÁMBITO TERRITORIAL
- [ ] ÓRGANO O PERSONA

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

En [LOCALIDAD] a [DÍA] de [MES] 20 .

Comparecen:

De una parte, [DENOMINACIÓN SOCIAL] constituida en escritura pública otorgada el día [FECHA] ante Notario de [LOCALIDAD] D. e inscrita en el Registro Mercantil de [LOCALIDAD] Libro [LIBRO] Tomo [TOMO] Folio [FOLIO] domiciliada en [DOMICILIO] calle [CALLE] núm [NÚMERO] y con CIF núm [NIF] representada por [ÓRGANO O PERSONA], mayor de edad, con domicilio en [LOCALIDAD] c/ [CALLE] núm [NÚMERO] con DNI/NIF núm [NIF] cuyas facultades derivan del poder otorgado por el notario D [NOMBRE Y APELLIDOS], debidamente inscrito, que es declarado vigente y sin modificación alguna (en adelante LA EMPRESA);

De otra parte, D [NOMBRE Y APELLIDOS] mayor de edad, casado, con domicilio en [LOCALIDAD] c/ [CALLE] núm. con DNI/NIF núm [NIF] (en adelante EL AGENTE).

Ambas partes se reconocen con carácter mutuo y tienen capacidad legal suficiente para otorgar el presente contrato de agencia, para convenir la actividad con AGENTE de [ACTIVIDAD] con carácter mercantil, excluyéndose, en consecuencia, la relación laboral, tanto desde un punto de vista formal como sustantivo, para realizar de forma continuada y estable la promoción de actos u operaciones por cuenta de la EMPRESA, en la forma que a continuación se establece y conforme a lo establecido por la Ley 12/1992, de 27 de mayo, sobre régimen jurídico del contrato de agencia y, en particular, conforme a las siguientes:

CLÁUSULAS:

1. Objeto del contrato.

Por el presente contrato, la EMPRESA [DENOMINACIÓN SOCIAL] nombra AGENTE a para que como tal preste los servicios que se detallarán a continuación por cuenta y en nombre de LA EMPRESA, tras la expresa aceptación del AGENTE

La EMPRESA [DENOMINACIÓN SOCIAL] entregará al AGENTE [OTROS DATOS] los productos de consumo (especificar productos) [DESCRIPCIÓN DEL BIEN] con la finalidad de promover su comercialización y venta, exceptuando las actividades de mantenimiento y conservación de dichos productos que será llevado a cabo por la propia EMPRESA.

2. No exclusividad y asunción del riesgo.

El agente asumirá la cuenta y riesgo de la totalidad de las operaciones de comercio a cambio de las contraprestaciones establecidas en el presente contrato.

3. Ámbito geográfico del contrato.

La actividad del AGENTE queda limitada a la siguiente zona geográfica [ÁMBITO TERRITORIAL] (especificar zona).

Fuera de la misma, EL AGENTE no podrá realizar actividades de promoción de ventas por cuenta de la EMPRESA.

4. Obligaciones del AGENTE.

— El AGENTE realizará personalmente las actividades de promoción y conclusión de las ventas con lealtad y buena fe sobre los productos citados, así como la realización de los actos que faciliten la comercialización por la EMPRESA.

— El AGENTE aplicará las condiciones de venta, comprometiéndose a negociar sus operaciones mercantiles por cuenta de la EMPRESA, ya sea directamente o a través de las diversas campañas de marketing y publicitarias sobre artículos y precios en las que se haga partícipe al AGENTE. El AGENTE tiene libertad de elección para determinar la política empresarial de ventas.

— Obligación de comunicar ofertas y pedidos: el AGENTE asume la obligación de comunicar a la EMPRESA las ofertas y pedidos que reciba firmados de posibles clientes en el plazo más breve posible desde su recepción. La comunicación se realizará por [ELEGIR: fax / e-mail / teléfono / correo urgente] (fax, e-mail, teléfono, correo urgente….). El AGENTE se obliga a comunicar a la EMPRESA toda la información de que disponga, cuando sea necesaria para la buena gestión de los actos u operaciones cuya promoción y conclusión se le encomienda en el presente contrato, así como, en particular, la relativa a la solvencia de los terceros con los que existan operaciones pendientes de conclusión o ejecución.

— Obligación de custodia de los productos e información sobre los stocks: el AGENTE se constituirá en depositario de los productos enviados por la EMPRESA a solicitud de los clientes y se encargará de su custodia y entrega al adquirente, por cuenta de la EMPRESA, corriendo con los gastos de custodia y conservación de los productos así como con los riesgos de su pérdida.

— El AGENTE asume la obligación con carácter periódico (especificar plazo) de enviar la relación de existencias, muestrarios, así como el estado de las operaciones en trámite, cuyo detalle, en todo caso, podrá ser reclamado por la EMPRESA al AGENTE, con el objeto de prever pedidos y cumplimentarlos.

— Información y recepción de reclamaciones: el AGENTE se obliga a recibir en nombre de la EMPRESA toda clase de reclamaciones de terceros sobre defectos o vicios de calidad o cantidad de los bienes vendidos y de los servicios prestados como consecuencia de las operaciones promovidas, aunque no se hubiesen concluido.

— Asunción de gastos: el AGENTE no tendrá derecho al reembolso de los gastos que el ejercicio de su actividad profesional le haya ocasionado. Serán de cuenta del AGENTE todos los gastos de viaje, desplazamientos, comunicaciones así como los propios de su actividad.

— Prohibición de competencia: el agente no podrá desarrollar su actividad profesional por cuenta de varios empresarios durante la vigencia del presente contrato. Una vez extinguido el presente contrato, el AGENTE deberá respetar dicho pacto, al menos, durante un periodo de [PLAZO] (especificar plazo).

5. Obligaciones de la EMPRESA.

— Información al AGENTE: la EMPRESA facilitará en todo momento de forma escrita al AGENTE las condiciones de venta en que deben desenvolverse sus gestiones. Las variaciones que se realicen en las condiciones ya entregadas deberán igualmente ser comunicadas por escrito para que puedan ser exigibles al AGENTE.

La EMPRESA facilitará igualmente al AGENTE la relación completa de los productos y precios de venta, mediante los catálogos, muestras y material necesarios o convenientes para la negociación y demostración a los clientes. Asimismo, la EMPRESA informará al AGENTE de las posibles campañas de promoción de sus productos que se lleven a efecto con carácter previo al lanzamiento de las mismas, así como de la comercialización de nuevos productos, proporcionándole de forma puntual los muestrarios nuevos necesarios para el desarrollo de su actividad. Igualmente informará respecto de la retirada del mercado o de las previsiones sobre aumentos o disminuciones en las ventas de los mismos.

— Retribución del AGENTE: el AGENTE percibirá una cantidad fija mensual de [IMPORTE] € por el desempeño de las funciones encomendadas, más una cantidad fija mensual de [IMPORTE] € en concepto de gastos de representación, gestión y mediación. Estas cantidades se revisarán anualmente en función del incremento del IPC. El AGENTE también percibirá un [PORCENTAJE] % del total de las ventas promovidas por él en concepto de comisión. Estas cantidades serán abonadas con carácter mensual una vez realizada la liquidación de los productos efectivamente vendidos y entregados a los compradores y reintegrado a la EMPRESA el producto de dichas ventas, reteniendo para sí la comisión pactada.

— Aceptación o rechazo de las operaciones propuestas: la EMPRESA se compromete a comunicar al AGENTE la aceptación o rechazo de cada operación en un plazo máximo de [PLAZO] (máximo de 15 días, según establece la Ley 12/1992. El plazo puede reducirse), desde que a través del agente se reciba la preceptiva propuesta. La negación de la misma será motivada señalando la falta de requisitos que la concreta operación no cumple. En caso de aceptación, es suficiente con que la EMPRESA remita al AGENTE copia de la aceptación que ha sido directamente enviada al cliente.

— Envío de productos: La EMPRESA suministrará al AGENTE sus productos en las cantidades que éste le solicite (especificar plazo) hasta un límite (especificar límite) quedando aquéllos en depósito del AGENTE hasta que se proceda a su venta. Cuando el agente necesite, para atender la petición de un cliente, una cantidad de productos de la que no disponga en depósito, la solicitará de la EMPRESA, remitiendo la correspondiente nota de pedido. La EMPRESA deberá poner el pedidio a disposición del AGENTE en el plazo máximo de (especificar plazo). En caso de incumplimiento de dicho plazo imputable a la EMPRESA, el AGENTE tendrá derecho a percibir la comisión que le corresponda por dicha operación, haya tenido lugar o no.

6. Régimen del contrato.

— Duración: este contrato se pacta por una duración indefinida. Para su resolución será necesario que cualquiera de las partes que desee ejercitar esta facultad notifique su decisión a la otra por escrito y de forma fehaciente con un plazo de preaviso de al menos (especificar plazo).

— Extinción: el presente contrato se extinguirá por muerte o declaración de fallecimiento del agente. El contrato también se extinguirá sin necesidad de preaviso en las siguientes circunstancias:

a) Cuando la otra parte incumpla, total o parcialmente, las obligaciones legal o contractualmente establecidas.

b) Cuando la otra parte hubiera sido declarada en concurso o admitida a trámite la solicitud.

En tales casos, se entiende que el contrato queda extinguido a la recepción de la notificación escrita en la que conste la voluntad de darlo por extinguido y la causa de la extinción.

— Comisiones futuras: por las operaciones concluidas una vez extinguido el contrato, el AGENTE tendrá derecho a percibir la comisión correspondiente cuando concurra alguna de las circunstancias siguientes:

a) Que el acto u operación se deba principalmente, a la actividad desarrollada por el AGENTE durante la vigencia del contrato, siempre que se hubiera concluido dentro de (especificar plazo) a partir de la extinción del contrato.

b) Que la EMPRESA o el AGENTE hayan recibido el encargo o pedido antes de la extinción del contrato de agencia, siempre que el AGENTE hubiera tenido derecho a percibir la comisión de haberse concluido el acto u operación durante la vigencia del contrato.

— Indemnización por clientela: A la extinción del presente contrato de agencia, si el agente hubiera aportado nuevos clientes a la empresa o incrementado sensiblemente las operaciones con la clientela preexistente, tendrá derecho a una indemnización si su actividad anterior puede continuar produciendo ventajas sustanciales a la empresa y resulta equitativo según las circunstancias concurrentes, sin que pueda la indemnización exceder del importe medio anual de las remuneraciones percibidas por el agente durante el periodo de duración del contrato.

El AGENTE no tendrá derecho a la indemnización por clientela en los siguientes supuestos:

a) Cuando la EMPRESA hubiese extinguido el contrato por causa de incumplimiento de las obligaciones contractuales o legales establecidas para el agente.

b) Cuado el AGENTE hubiera denunciado el contrato, salvo que la denuncia tuviera como causa circunstancias imputables a la EMPRESA o se fundara en la edad, la invalidez o la enfermedad del AGENTE y no pudiera exigírsele razonablemente la continuidad de sus actividades.

c) Cuando con el consentimiento de la EMPRESA, el AGENTE hubiese cedido a un tercero los derechos y las obligaciones de que era titular en virtud del presente contrato.

La acción para reclamar la indemnización por clientela prescribe al año desde la extinción del presente contrato.

— Indemnización por daños y perjuicios: sin perjuicio de la indemnización por clientela, si la EMPRESA denuncia unilateralmente el contrato vendrá obligado a indemnizar los daños y perjuicios que, en su caso, la extinción anticipada haya causado al AGENTE siempre que dicha extinción no permita la amortización de los en gastos que éste haya incurrido para la ejecución del contrato.

— Tribunal competente: las partes se someten al tribunal competente del domicilio del AGENTE en caso de discrepancia sobre el cumplimiento del contrato y de las acciones derivadas del mismo.

7. Cláusulas opcionales.

— Poder de representación del AGENTE: para el cumplimiento de las obligaciones especificadas en este contrato, el AGENTE queda expresamente facultado para concluir en nombre y representación de LA EMPRESA los actos u operaciones de comercialización de los productos.

— Subagentes: La actuación por medio de subagentes requerirá autorización expresa por parte de la EMPRESA. Los subagentes quedarán bajo el cargo y la responsabilidad del AGENTE. La EMPRESA no asume ninguna responsabilidad respecto a aquéllos.

EL AGENTE LA EMPRESA

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

---
name: contrato-distribucion-comercial-mer-0503
description: "Contrato de distribución comercial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de distribución comercial

> Formulario **MER-0503** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de distribución comercial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de distribución comercial” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-distribucion-comercial-mer-0503`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] Nº (5 veces)
- [ ] FECHA (3 veces)
- [ ] PERIODICIDAD (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PLAZO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] INCOTERM
- [ ] LUGAR
- [ ] MES
- [ ] TIPO DE PRODUCTOS

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

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA EMPRESA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA DISTRIBUIDORA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE DISTRIBUCIÓN, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que La EMPRESA se dedica, entre otras actividades, a la fabricación y comercialización de [TIPO DE PRODUCTOS]

SEGUNDO.- Que LA DISTRIBUIDORA es una empresa independiente que cuenta con los medios económicos, humanos y, en general, con una organización y una red de distribución suficientes, y desea obtener la distribución en exclusiva (o no exclusiva) de los productos de LA EMPRESA indicados en el Anexo l.

TERCERO.- Que estando ambas Partes interesadas en que LA DISTRIBUIDORA distribuya y comercialice en exclusiva (o no exclusiva) los productos de LA EMPRESA, ambas partes de común acuerdo llevan a efecto el presenten contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

LA EMPRESA concede a LA DISTRIBUIDORA, que los adquiere, los derechos de distribución en exclusiva (o no exclusiva) de los Productos que aparecen relacionados en el listado que acompaña al presente contrato como Anexo nº I.

Quedan expresamente excluidos del presente contrato todos los productos que no figuren en la misma, así como cuantos pueda lanzar al mercado LA EMPRESA durante el plazo de duración del presente contrato.

[ELEGIR UNA OPCIÓN: Zona Geográfica / En exclusiva / No / — y además elegir: Precio, facturación y pago / Fijo / Actualizable]

Pedidos

Todos los pedidos serán formalizados por LA DISTRIBUIDORA, por escrito, en el domicilio de LA EMPRESA con una antelación mínima de [PLAZO] (días, semanas) respecto a la fecha de su efectivo libramiento.

En el supuesto de que LA EMPRESA retire de su catálogo uno o más de los Productos, LA DISTRIBUIDORA no tendrá derecho a indemnización ni compensación de clase alguna siempre que la retirada obedezca a razones técnicas o a defectos.

Entrega

LA EMPRESA se obliga a entregar y poner a plena disposición de LA DISTRIBUIDORA el Producto objeto del presente contrato el día [FECHA] de cada [PERIODICIDAD] (semana, mes, etc.).

Los Productos se entregarán en las Instalaciones [INCOTERM] (INCOTERM adecuado).

LA DISTRIBUIDORA se compromete a aceptar las mercancías una vez hayan sido entregadas si coinciden con las calidades, forma y tamaño descritos en el Exponendo Primero.

Obligaciones de la distribuidora

LA DISTRIBUIDORA se obliga a:

1. Pagar el Producto suministrado por LA EMPRESA de conformidad con lo estipulado en el presente contrato.

2. Comprar anualmente las cantidades mínimas que se reseñan en el Anexo II del presente contrato.

3. Ocuparse con la diligencia de un ordenado comerciante del desarrollo de la actividad de distribución prevista en el presente contrato. Con esta finalidad, se encargará, a su sólo cargo, de la promoción adecuada del Producto entre los clientes radicados en la zona geográfica que tiene asignado, debiendo contar en todo caso con la autorización previa de LA EMPRESA.

4. Comercializar los productos en locales previamente aprobados por LA EMPRESA y que se establecen en el Anexo III del presente documento, locales que deberán mantenerse en condiciones adecuadas para la venta de Los Productos.

5. Asegurar la máxima satisfacción a los clientes radicados en la zona geográfica que tiene asignada, prestándoles la asistencia necesaria, antes y después de la adquisición de los Productos.

6. Mantener en el territorio de la distribución una red de ventas de los productos suficiente y apropiada para la adecuada distribución de los mismos, así como a disponer del personal necesario para la correcta atención de los clientes.

7. Procurar anualmente un informe relativo a los productos vendidos en el territorio que tiene asignado.

8. Atender todas las reclamaciones que se presenten por terceros concernientes a vicios o defectos de la calidad de los Productos, comunicando dicha información con la mayor brevedad a LA EMPRESA.

9. Facilitar a LA EMPRESA, a efectos de control contable, relaciones [PERIODICIDAD] (mensuales, trimestrales, etc.), debidamente firmadas por una persona representativa de la sociedad, de los movimientos de venta en unidades y valores, así como el stock de los Productos. Dichas relaciones serán remitidas durante los [Nº] días siguientes a cada [PERIODICIDAD] (mes, trimestre, etc.) natural.

Obligaciones de la empresa

LA EMPRESA se obliga a:

1. Atender con prontitud los pedidos de productos realizados por LA DISTRIBUIDORA, siempre y cuando ésta se halle al corriente en el pago de sus obligaciones y las existencias del producto en los almacenes de LA EMPRESA así lo permitan.

2. Remitir a LA DISTRIBUIDORA los artículos promocionales que estime por conveniente para la mayor difusión comercial de los productos.

Cesión de derechos de propiedad intelectual e industrial

LA DISTRIBUIDORA reconoce que LA EMPRESA es la legítima titular de las marcas, nombres comerciales y demás denominaciones o signos distintivos de los Productos que se relacionan con sus correspondientes datos de inscripción en la relación que acompaña al presente contrato como Anexo IV.

LA EMPRESA cede a LA DISTRIBUIDORA que acepta, el uso de su marca o cualquier signo distintivo de LA EMPRESA mientras se mantenga vigente el presente contrato o alguna de sus prórrogas.

Igualmente, LA DISTRIBUIDORA se obliga a comunicar a La Empresa cualquier incidencia que afecte a los Derechos de la Propiedad Industrial e Intelectual inherentes a los Productos.

Duración

El presente contrato tendrá una duración de [PLAZO] (meses, años) y podrá ser prorrogado mediante acuerdo celebrado por escrito entre las partes por un plazo igual, siempre y cuando esto se realice con [Nº] días de antelación al vencimiento del plazo inicialmente pactado.

A la terminación del presente contrato, LA DISTRIBUIDORA deberá enviar a LA EMPRESA, dentro de los siguientes [Nº] días siguientes, los catálogos, rótulos y en general cualquier otro material promocional entregado por LA EMPRESA.

A la fecha de terminación de este contrato, LA DISTRIBUIDORA deberá cesar de inmediato de usar la marca o cualquier signo distintivo de LA EMPRESA.

Garantía de los productos

Los Productos están sujetos a la garantía de LA EMPRESA fabricante que se adjunta como Anexo V al presente documento.

Responsabilidad frente a terceros

Las partes pactan expresamente que LA EMPRESA responderá de cualquier daño y perjuicio que se pueda causar a los Clientes por razón de defecto, pérdidas y/o menoscabos en los Productos, que no puedan ser atribuibles a una actitud negligente de LA DISTRIBUIDORA.

En el supuesto de que dichos clientes reclamasen también a LA DISTRIBUIDORA, y por razón de dicha reclamación ésta viniera obligada a indemnizar o compensar a dichos Clientes, LA DISTRIBUIDORA tendrá derecho a solicitar a LA EMPRESA, que vendrá obligada, el abono inmediato de las cantidades pagadas por LA DISTRIBUIDORA a dichos terceros.

A tal fin, LA DISTRIBUIDORA informará inmediatamente a LA EMPRESA por escrito de todas las reclamaciones por parte de los Clientes y de todas las reclamaciones o acciones interpuestas o que vayan a interponerse respecto a cualquier Producto de las que pueda tener conocimiento. A solicitud de LA EMPRESA, LA DISTRIBUIDORA prestará toda la asistencia razonable en la defensa de tal reclamación o acción interpuesta o que se vaya a interponer con respecto a los Productos, si bien LA EMPRESA, a su arbitrio, tendrá el exclusivo control sobre la defensa y transacción de la reclamación o acción.

Si la reclamación o acción estuviera basada en la negligencia, engaño, fraude, falsedad o incumplimiento de este contrato por parte de LA DISTRIBUIDORA, ésta tendrá el derecho a mantener su propia defensa en cuanto a, y limitada a, dicha negligencia, engaño, fraude, falsedad o incumplimiento de este contrato por parte de LA DISTRIBUIDORA.

Cláusula de exclusividad

Exclusividad de la Distribuidora

LA DISTRIBUIDORA se compromete a no fabricar, representar, distribuir, vender o comercializar, ni por sí ni a través de tercero ni de otras sociedades participadas, ningún tipo de producto igual, parecido o que, en algún modo sea competidor de los relacionados en el documento unido como Anexo I.

Del mismo modo, durante la vigencia del presente contrato LA DISTRIBUIDORA no podrá adquirir participación ni derecho alguno en negocios o empresas que se dediquen a la comercialización con productos competidores de los que son objeto del presente contrato, ni participar, activa o pasivamente, en ningún tipo de gestión conducente a la venta de los productos objeto del presente contrato fuera del territorio al que se circunscribe el presente acuerdo.

Exclusividad de la empresa

Por su parte, durante el término de vigencia del presente contrato, LA EMPRESA se obliga a no conceder la distribución, venta y/o comercialización de los Productos, respecto del territorio descrito en la cláusula segunda, a ninguna persona física o jurídica distinta de LA DISTRIBUIDORA. Asimismo se abstendrá de gestionar otras ventas de LOS PRODUCTOS en dicho territorio, distintas a las que efectuará LA DISTRIBUIDORA.

El incumplimiento, por cualquiera de las partes, de las obligaciones reguladas en este apartado dará derecho a la parte contraria a una indemnización equivalente a [IMPORTE] euros anuales.

Deber de confidencialidad

LA DISTRIBUIDORA se obliga a no revelar, ceder o transferir a terceros ninguna información referente a los negocios, clientes, operaciones, instalaciones, cuentas o finanzas de LA EMPRESA, ni sus procedimientos, métodos, transacciones, "know-how", o cualquier otro aspecto relacionado con la actividad de dicha entidad que pueda conocer o haya conocido con motivo de la prestación de servicios prevista en el presente contrato.

Del mismo modo, LA DISTRIBUIDORA se obliga a actuar con la mayor diligencia para evitar la publicación o revelación de cualquier información confidencial referente a esas materias.

Resolucion del contrato

El Contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2. Por acuerdo de las Partes por escrito.

3. La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

Cláusula penal

En caso de resolución del contrato por causa imputable a cualquiera de las Partes, la parte contraria no estará obligada a la devolución de las mercancias o cantidades entregadas hasta ese momento, fijándose además una cantidad adicional de [IMPORTE] € como indemnización que la parte incumplidora deberá abonar a

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE DISTRIBUCIÓN, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo. Don [NOMBRE Y APELLIDOS]

(La Distribuidora)

Fdo. Don [NOMBRE Y APELLIDOS]

(La Empresa)

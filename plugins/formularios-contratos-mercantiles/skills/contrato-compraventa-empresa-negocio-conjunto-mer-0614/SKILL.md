---
name: contrato-compraventa-empresa-negocio-conjunto-mer-0614
description: "Contrato de compraventa de una empresa o negocio en su conjunto. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de una empresa o negocio en su conjunto

> Formulario **MER-0614** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato de compraventa en el que el objeto es un negocio o una empresa en su globalidad

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de una empresa o negocio en su conjunto» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de una empresa o negocio en su conjunto” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-compraventa-empresa-negocio-conjunto-mer-0614`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (4 veces)
- [ ] CALLE (3 veces)
- [ ] NOMBRE DEL NEGOCIO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] PLAZO (2 veces)
- [ ] ACTIVIDAD
- [ ] DATOS REGISTRALES
- [ ] ESTADO CIVIL
- [ ] LUGAR
- [ ] NOMBRE DE LA CORTE ARBITRAL
- [ ] Nº DE PROCEDIMIENTO

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

En [LUGAR], a [FECHA].

REUNIDOS

DE UNA PARTE:

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, estado civil [ESTADO CIVIL], con domicilio en [LOCALIDAD], calle [CALLE] y con N.I.F. nº [Nº]: [OTROS DATOS], en lo sucesivo EL VENDEDOR.

Y DE OTRA:

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, estado civil, con domicilio en [LOCALIDAD], calle [CALLE], y con N.I.F. nº [Nº]: [OTROS DATOS], en lo sucesivo EL COMPRADOR.

Intervienen ambos en su propio nombre y derecho, reconociéndose la mutua capacidad legal necesaria para otorgar el presente contrato de COMPRAVENTA DE INDUSTRIA/NEGOCIO/EMPRESA, a cuyo efecto, libre y de común acuerdo:

EXPONEN

I.- Que el VENDEDOR es propietario del negocio [NOMBRE DEL NEGOCIO], el cual se desarrolla en el local sito en [LOCALIDAD], Calle [CALLE], con una superficie de [Nº] metros cuadrados, lindando a la izquierda con la finca propiedad de D./Dña. [NOMBRE Y APELLIDOS], a la derecha con la finca propiedad de D./Dña. [NOMBRE Y APELLIDOS], e inscrito en el Registro de la Propiedad de [LOCALIDAD] al [DATOS REGISTRALES], estando libre de cargas y gravámenes y al corriente en el pago de impuestos, según declara el arrendador en este acto.

II.- Que los elementos que constituyen el negocio [NOMBRE DEL NEGOCIO] son los comprendidos en el inventario que figura unido al presente contrato como ANEXO I.

III.- Que el VENDEDOR es titular del citado negocio, según consta en (alta en actividades económicas, cámaras, etc.).

IV.- Que el VENDEDOR es asimismo titular de los bienes muebles y maquinarias comprendidos en el inventario que figura unido al presente contrato como ANEXO II.

V.- Que el COMPRADOR está interesado en adquirir el negocio (y en su caso, arrendar el local) descrito(s) precedentemente, para continuar ejerciendo en ella la actividad industrial/comercial/profesional que hasta ahora aquél venía realizando así como en comprar los bienes muebles, maquinarias y accesorio enumerados en el ANEXO II, por lo que estando el VENDEDOR conforme, llevan a efecto el presente contrato de conformidad con las siguientes

CLÁUSULAS

Primera.- Objeto del contrato

El objeto del presente contrato lo constituye la industria/negocio/empresa descrito en el Exponente I y detallado en el Anexo I del presente contrato.

Segunda.- Traspaso

Al momento de la suscripción del presente contrato, EL COMPRADOR reconoce haber recibido la industria/negocio/empresa en perfecto estado de conservación, al corriente de las Licencias e Impuestos pertinentes y a su plena conformidad.

Asimismo, EL COMPRADOR manifiesta conocer el estado en el que se encuentran los bienes muebles, maquinarias y accesorios descritos en el Anexo II, así como todas las especificaciones técnicas propias de las mismas y relativas a su correcto funcionamiento y mantenimiento técnico. El COMPRADOR afirma que todos ellos los muebles, maquinaria y accesorios inherentes a la industria/negocio/empresa adquirida se encuentran en perfectas condiciones de conservación y funcionamiento sin que exista deterioro alguno en la misma, por encima de los lógicos de la antigüedad. Igualmente manifiesta que su funcionamiento es óptimo para el desempeño de la labor que tiene asignada, habiendo comprobado con anterioridad a la suscripción del presente contrato su correcto funcionamiento y mostrando plena satisfacción al respecto.

Tercera.- Precio

[ELEGIR UNA OPCIÓN: Pago al contado / Único pago aplazado / Pago a plazos]

[OPCIONAL — incluir si procede]

(Para caso de precio aplazado)

Cuarta.- Cláusula de reserva de dominio

La venta se entiende hecha con reserva de dominio a favor del VENDEDOR, hasta el momento en que el importe total del presente contrato de compraventa haya sido satisfecho, esto es, hasta el día [FECHA].

En el supuesto de que por cualquier otra causa, como por ejemplo el robo, el COMPRADOR fuera privado del bien objeto de este contrato, éste deberá ponerlo en conocimiento inmediato del VENDEDOR con el fin de que pueda adoptar las acciones que estime oportunas al respecto, sin que por ello se vea liberada de la obligación del pago íntegro del precio. En el supuesto de que el COMPRADOR omitiera esta obligación, se entenderá que existe responsabilidad por su parte en el destino final del bien y mala fe en su comportamiento.

Asimismo, el COMPRADOR responderá de los daños y perjuicios que sobrevinieran a la industria/negocio/empresa traspasada, incluso por caso fortuito, durante el periodo de vigencia de la obligación suspensiva.

La cláusula de reserva de dominio a favor del VENDEDOR quedará automáticamente extinguida en el momento en que el COMPRADOR haya pagado la totalidad del precio pactado. De esta forma, la industria/negocio/empresa pasará a ser de plena propiedad del COMPRADOR sin limitación alguna.

Por el contrario, si llegado el vencimiento de cualquiera de los pagos éste no se hubiera verificado, el COMPRADOR deberá devolver la industria/ negocio/empresa adquirida en virtud del presente contrato de forma inmediata, encontrándose un representante del VENDEDOR plenamente legitimado para recuperar el objeto de este contrato a su voluntad sin necesidad de procedimiento especial alguno, ya que para tal fin le faculta la misma desde el momento de la suscripción de este contrato.

La enajenación o la realización de cualquier otro acto de disposición en tanto no se haya verificado efectivamente el pago requerirá la autorización previa y por escrito del VENDEDOR.

.- Garantía del vendedor

El VENDEDOR garantiza al COMPRADOR el pleno funcionamiento de las instalaciones, así como de la maquinaria, bienes y accesorios inventariados en los Anexos I y II, necesarios para el desempeño de la actividad descrita en el Exponente I durante un periodo máximo de [Nº] meses, dentro de los cuales deberá costear aquellas reparaciones que sean necesarias para el correcto ejercicio de la actividad.

No obstante lo anterior, no se considerará cubierta por la presente cláusula de garantía los supuestos de negligencia del COMPRADOR en la utilización, manejo y conservación de local, maquinarias, bienes y accesorios anteriormente referidos.

El COMPRADOR deberá permitir el acceso al local de negocio al VENDEDOR y a los operarios o industriales mandados por ésta para la realización, inspección y comprobación de cualquier clase de obras o reparaciones que afecten al inmueble.

.- Cesión de trabajadores

El COMPRADOR queda subrogado en todos los derechos y obligaciones laborales y de la Seguridad Social del VENDEDOR, incluyendo los compromisos de pensiones y, en general, cuantas obligaciones en materia de protección social complementaria hubiera adquirido EL VENDEDOR.

.- Otros gastos y cumplimiento de normas

Serán de cuenta exclusiva del COMPRADOR los impuestos, tasas, precios públicos y licencias, tanto municipales como estatales o autonómicos, que recaigan sobre la industria/negocio/empresa [NOMBRE DEL NEGOCIO],

Asimismo, el COMPRADOR gestionará y sufragará a su exclusiva cuenta y cargo, todas las licencias, permisos, autorizaciones, obras de adecuación, etc., que la actividad de [ACTIVIDAD] requiera, ya sean exigidos por la Administración Central, Local o Autonómica y cumplirán todas las disposiciones, Ordenanzas, y exigencias de cualquier autoridad y Organismo competente.

.- Confidencialidad

Tanto el COMPRADOR como el VENDEDOR se comprometen a no divulgar la información confidencial referente a la otra parte de la que hayan tenido conocimiento por razón de la ejecución del presente contrato y a mantenerla en secreto, incluso después de su firma.

El incumplimiento de este compromiso conllevará la obligación de indemnizar los daños y perjuicios causados.

.- Pacto de no concurrencia

El VENDEDOR se obliga a no tomar a su cargo la venta de productos de clase similar o que puedan ser objeto de competencia con el COMPRADOR o dificulten el mercado de cualquier manera de las ACTIVIDADES descritas en el Anexo I durante un plazo de [PLAZO] y para la zona geográfica de

La obligación de NO COMPENTENCIA que se pacta en esta cláusula desplegará sus efectos incluso en el caso de extinción del presente contrato, por un período máximo de [PLAZO] contado a partir del día siguiente a aquél en que, en su caso, se produzca dicha extinción, y para la zona geográfica de

.- Arbitraje

En caso de cualquier controversia o divergencia que pueda surgir entre las partes en relación con el presente contrato, y en particular sobre su interpretación, validez, eficacia, cumplimiento, resolución o rescisión, ambas partes se someten expresamente, y con renuncia a su fuero propio, a la decisión del asunto o litigio planteado, mediante el arbitraje institucional de (por ejemplo, Cámara de Comercio/Colegio de Abogados/etc. de [LOCALIDAD]), a la cual encomiendan la administración del arbitraje y la designación de los árbitros.

a) El arbitraje se realizará conforme al procedimiento [Nº DE PROCEDIMIENTO] (establecido en el Reglamento Arbitral de [NOMBRE DE LA CORTE ARBITRAL]) y en la Ley de Arbitraje.

b) El laudo arbitral deberá dictarse durante los noventa días siguientes a la aceptación del cargo por parte de los árbitros designados, obligándose ambas partes a aceptar y cumplir la decisión contenida en él.

c) Para el caso de que el arbitraje no llegara a realizarse por mutuo acuerdo o fuese declarado nulo, ambas partes se someten a los Tribunales de [LOCALIDAD] con renuncia a su propio fuero, si éste fuese otro.

.- Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de la parte [NOMBRE DE LA PARTE].

Asimismo, serán de cuenta del [NOMBRE DE LA PARTE] todos los gastos y costas judiciales, así como los honorarios de Abogado y derechos de Procurador, aunque la intervención de los mismos no sea preceptiva, que se originen como consecuencia del incumplimiento del presente contrato.

.- Actualización

En el caso de que alguna o algunas de las cláusulas del contrato pasen a ser inválidas, ilegales o inejecutables en virtud de alguna norma jurídica, se considerarán ineficaces en la medida que corresponda, pero en lo demás, este contrato conservará su validez. Las partes contratantes acuerdan sustituir la cláusula o cláusulas afectadas por otra u otras que tengan los efectos económicos más semejantes a los de las sustituidas.

.- Carácter mercantil de la relación contractual

El presente contrato tiene exclusivamente carácter mercantil y se regirá por sus propias cláusulas y Anexos, y en lo en ellos no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

.- Domicilios a efectos de notificaciones

Se señalan los siguientes:

Para el ARRENDADOR [DOMICILIO].

Para el ARRENDATARIO [DOMICILIO].

Y leído el presente documento, ambas partes lo firman en prueba de su conformidad, a un solo efecto y por duplicado, en el lugar y fecha ut supra.

ARRENDADOR

ARRENDATARIO
D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]

ANEXO I: ELEMENTOS QUE CONSTITUYEN EL NEGOCIO (Por ejemplo marcas, nombres comerciales, know how, franquicias, etc.).

ANEXO II: BIENES MUEBLES Y MAQUINARIAS QUE SE TRANSMITEN

Téngase en cuenta la posibilidad de combinar la cláusula arbitral con otras (cláusulas híbridas arbitraje/jurisdicción), como las de mediación o las de sumisión a determinada jurisdicción, bien permitiendo la elección a una de las partes, o a la demandante, o delimitando qué tipo de contiendas irían a una u otra vía, como señala el AAP Madrid 18 de octubre de 2013, rec. 66/2013.

========================================================================

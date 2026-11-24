---
name: contrato-compraventa-nombre-dominio-mer-0758
description: "Contrato de compraventa de un nombre de dominio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de un nombre de dominio

> Formulario **MER-0758** del plugin **Contratos tecnológicos, comercio electrónico y protección de datos** (`formularios-tecnologia-y-proteccion-de-datos`) · Mercantil › Tecnología, comercio electrónico y protección de datos · normativa revisada el 24-11-2026.

## Qué es

Contrato de compraventa de un nombre de dominio de Internet entre el titular actual (vendedor) y el adquirente (comprador), con garantías de titularidad, transferencia registral ante el registrador, confidencialidad, protección de datos y alternativas de pago y de resolución de conflictos (tribunales o arbitraje, con o sin cláusula penal).

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de un nombre de dominio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de un nombre de dominio” para mi caso». También puedes invocarla directamente con `/formularios-tecnologia-y-proteccion-de-datos:contrato-compraventa-nombre-dominio-mer-0758`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-tecnologia-y-proteccion-de-datos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos tecnológicos, comercio electrónico y protección de datos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE EN CIFRA (8 veces)
- [ ] IMPORTE EN LETRA (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] FECHA (4 veces)
- [ ] PROVINCIA (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] NOMBRE, CORREO ELECTRÓNICO Y TELÉFONO (3 veces)
- [ ] Nº (3 veces)
- [ ] ABREVIATURA DE LA INSTITUCIÓN (2 veces)
- [ ] CORTE ARBITRAL (2 veces)
- [ ] CÓDIGO SWIFT/BIC (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DÍA (2 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] IBAN (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] SUCURSAL (2 veces)
- [ ] ÁMBITO TERRITORIAL (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DIRECCIÓN DEL VENDEDOR
- [ ] DOMINIO
- [ ] DOMINIO DE PRIMER NIVEL
- [ ] DOMINIO DE SEGUNDO NIVEL
- [ ] IMPORTE
- [ ] MES
- [ ] NIF
- [ ] NOMBRE DE LA EMPRESA REGISTRADORA DONDE FIGURA EL DOMINIO
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL
- [ ] Nº DE FOLIOS
- [ ] Nº DE PLAZOS

## Normas que cita el formulario

- art. 32 RGPD
- art. 34 Ley 60/2003

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

NOTAS EXPLICATIVAS

Intervinientes: si se trata de una persona física que interviene en su propio nombre y derecho, es preciso hacer constar tal extremo. Lo mismo sucede si interviene en representación de otra persona física; en este caso será necesario describir la fuente de la que dimana su representación, ya sea legal o convencional. En el mismo sentido, si se trata de una persona física que actúa en beneficio de una sociedad de gananciales, de una sociedad civil irregular o de una comunidad de bienes, puesto que en estos casos no existe una personalidad jurídica diferente de la de los miembros que la integran.

Estado civil: en el supuesto de que el estado civil fuera el de casado, sería conveniente expresar el régimen económico matrimonial y el nombre y apellidos del cónyuge, puesto que el Código Civil contempla la posibilidad de comprometer los bienes comunes o gananciales (artículo 1365 del Código Civil).

Morosidad: la Ley 3/2004, de 29 de diciembre, por la que se establecen medidas de lucha contra la morosidad en las operaciones comerciales, establece la aplicación automática de un tipo de interés de demora, sin necesidad de aviso de vencimiento ni de intimación alguna por parte del acreedor. No obstante, el acreedor sólo podrá exigir el pago de los intereses de demora cuando haya cumplido con las obligaciones contractuales y legales que le incumbían y cuando el retraso en el pago no sea imputable a su conducta. Si se dan estas condiciones, se devengará el interés de demora contractual o el fijado legalmente.

ICANN: Internet Corporation for Assigned Names and Numbers, corporación formada para asumir, entre otras funciones, la responsabilidad sobre la localización de las direcciones IP, la asignación de protocolo, la dirección de sistemas de nombres de dominio y de servidores. Asegura el funcionamiento y estabilidad en la red.

WHOIS: instrumento interactivo de acceso público en Internet que facilita información sobre la titularidad, datos de contacto y disponibilidad de un nombre de dominio en Internet o una dirección IP.


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

CONTRATO DE COMPRAVENTA DE DOMINIO

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte: D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL] (si fuera casado, indicar régimen económico matrimonial y nombre y apellidos del cónyuge), vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [DNI/NIE].

De otra: D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [DNI/NIE].

[OPCIONAL — si las partes actúan mediante representante o son personas jurídicas, sustituir o completar lo anterior con lo siguiente]

INTERVIENEN

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [DENOMINACIÓN SOCIAL], en lo sucesivo «EL COMPRADOR», en virtud de poder otorgado a su favor ante el notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [PROVINCIA] y vigente, según manifiesta.

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [DENOMINACIÓN SOCIAL], en lo sucesivo «EL VENDEDOR», en virtud de poder otorgado a su favor ante el notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [PROVINCIA] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE COMPRAVENTA DE DOMINIO y, a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.– Que el VENDEDOR es titular del dominio de segundo nivel [DOMINIO DE SEGUNDO NIVEL] registrado bajo el nombre de dominio de primer nivel [DOMINIO DE PRIMER NIVEL], en adelante «el Dominio», actualmente registrado a su nombre ante [NOMBRE DE LA EMPRESA REGISTRADORA DONDE FIGURA EL DOMINIO], como se desprende de los datos obtenidos de la base de datos WHOIS del registrador, y se encuentra al corriente del pago de las cuotas de mantenimiento.

SEGUNDO.– Que el COMPRADOR es una empresa especializada en [ACTIVIDAD] y está interesada en adquirir por compra la titularidad del Dominio referido en el expositivo anterior.

TERCERO.– Que las partes, reunidas en la sede social del COMPRADOR, acuerdan celebrar el presente contrato de COMPRAVENTA DE DOMINIO WEB, en adelante el «Contrato», de acuerdo con las siguientes

CLÁUSULAS

PRIMERA.– Objeto

EL VENDEDOR transmite al COMPRADOR el derecho de uso exclusivo del Dominio [DOMINIO] por el precio y en los términos y condiciones que se señalan en el presente Contrato.

SEGUNDA.– Precio y forma de pago

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Pago no aplazado

El precio se concreta en la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE EN CIFRA] €) más el Impuesto sobre el Valor Añadido correspondiente, esto es, [IMPORTE EN LETRA] euros ([IMPORTE EN CIFRA] €) adicionales. El precio total de la operación asciende a la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE EN CIFRA] €).

El pago se efectuará el día [FECHA] en la cuenta corriente nº [IBAN] que EL VENDEDOR tiene suscrita con la entidad [ENTIDAD BANCARIA], en su sucursal [SUCURSAL]. (En el caso de que se trate de una transferencia internacional será preciso conocer el código SWIFT o BIC, de 8 u 11 dígitos alfanuméricos, que contiene la identificación del nombre y oficina del banco y el país donde se encuentra: [CÓDIGO SWIFT/BIC].)

— Pago aplazado

El precio se concreta en la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE EN CIFRA] €) más el Impuesto sobre el Valor Añadido correspondiente, esto es, [IMPORTE EN LETRA] euros ([IMPORTE EN CIFRA] €) adicionales. El precio total de la operación asciende a la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE EN CIFRA] €).

El pago del precio se efectuará en [Nº DE PLAZOS] plazos sucesivos de [IMPORTE] euros cada uno de ellos (IVA incluido), a contar desde [FECHA], pudiendo EL COMPRADOR en cualquier momento anticipar el pago de los plazos pendientes con una reducción del [PORCENTAJE] % sobre cada uno de ellos.

El pago se efectuará el día [DÍA] de cada mes en la cuenta corriente nº [IBAN] que EL VENDEDOR tiene suscrita con la entidad [ENTIDAD BANCARIA], en su sucursal [SUCURSAL]. (En el caso de que se trate de una transferencia internacional será preciso conocer el código SWIFT o BIC, de 8 u 11 dígitos alfanuméricos, que contiene la identificación del nombre y oficina del banco y el país donde se encuentra: [CÓDIGO SWIFT/BIC].)

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho al VENDEDOR a exigir a EL COMPRADOR un interés moratorio del [PORCENTAJE] % respecto de cada uno de los pagos no satisfechos puntualmente. Si EL COMPRADOR se retrasara en el pago de dos plazos o en el pago del último, EL VENDEDOR podrá optar entre exigir el pago de los plazos pendientes o resolver el contrato, con abono en ambos casos de las indemnizaciones que puedan corresponder.

TERCERA.– Garantías

A los efectos de la presente compraventa, EL VENDEDOR declara ser el propietario del Dominio y titular registral del mismo y garantiza frente al COMPRADOR hallarse al corriente del pago de las cuotas de mantenimiento del Dominio frente al registrador.

EL VENDEDOR garantiza que ninguna otra parte tiene ningún derecho sobre el Dominio y que únicamente él es el legítimo propietario del Dominio.

EL VENDEDOR renuncia de forma permanente a cualquier derecho sobre el Dominio, así como sobre la utilización de correo electrónico bajo el mismo (cualquier nombre seguido de la denominación indicada), y manifiesta que no reclamará indemnización alguna por el uso que EL COMPRADOR haga del Dominio en el futuro.

Desde la firma del presente Contrato, EL VENDEDOR garantiza que no utilizará el Dominio objeto de transmisión, ni tampoco correo electrónico bajo el mismo, en su documentación, publicidad o en cualquier otro elemento.

CUARTA.– Transmisión de la titularidad

Convienen las partes que la transmisión, en favor del COMPRADOR, de la titularidad sobre el derecho de uso del Dominio tendrá lugar en el momento de la firma del presente Contrato, aunque no se haya realizado la transferencia registral del citado Dominio ante el registrador a favor del COMPRADOR.

QUINTA.– Transferencia del dominio

EL VENDEDOR se compromete a llevar a cabo las gestiones necesarias para realizar la transferencia del Dominio frente al registrador. En este sentido, EL VENDEDOR firmará el «Domain Name Transfer Agreement», lo presentará ante el registrador y dará las instrucciones oportunas para que procedan a solicitar la transferencia, colaborando en todas las acciones que el propio registrador establezca para llevar a cabo la transferencia.

EL VENDEDOR asumirá los gastos que se deriven de las gestiones de transferencia del Dominio ante el registrador.

A los efectos de formalizar la transferencia del Dominio, este deberá aparecer registrado a nombre del COMPRADOR frente al registrador con los datos recogidos en el Anexo I.

SEXTA.– Calidad de los servicios prestados

EL VENDEDOR se abstendrá de usar el Dominio desde la firma del presente Contrato, tanto directa como indirectamente, y asume y expresamente renuncia a cualquier indemnización o compensación que pueda surgir del uso o propósito del COMPRADOR en cuanto al Dominio.

EL VENDEDOR no reclamará al COMPRADOR, ni a cualquiera designado por éste, por el uso del Dominio, por la transgresión o el uso de copyrights, marcas, patentes, invenciones o cualquier otro elemento referente a la propiedad industrial o intelectual que pueda utilizarse por el uso del Dominio.

SÉPTIMA.– Confidencialidad

EL VENDEDOR guardará confidencialidad sobre la información que le facilite el COMPRADOR en o para la ejecución del Contrato o que por su propia naturaleza deba ser tratada como tal. Se excluye de la categoría de información confidencial toda aquella información que sea divulgada por el COMPRADOR, aquella que haya de ser revelada de acuerdo con las disposiciones de la ICANN, con las leyes, con una resolución judicial o acto de autoridad competente. Este deber se mantendrá durante un plazo de tres años a contar desde la finalización del servicio.

OCTAVA.– Protección de datos

Por requisito establecido por la ICANN, el titular del nombre de dominio autoriza la publicación de los datos relativos a la titularidad del nombre de dominio en cuestión y de los contactos administrativo, técnico y de pago que, según la normativa, deben ser públicos y accesibles desde el WHOIS de los registradores competentes.

En el caso de que la prestación de los servicios suponga la necesidad de acceder a datos de carácter personal, el VENDEDOR, en los supuestos en que sea encargado del tratamiento, queda obligado al cumplimiento del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD), de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales (LOPDGDD), y demás normativa aplicable.

El VENDEDOR responderá, por tanto, de las infracciones en que pudiera incurrir en el caso de que destine los datos personales a otra finalidad, los comunique a un tercero o, en general, los utilice de forma irregular, así como cuando no adopte las medidas correspondientes para el almacenamiento y custodia de los mismos. A tal efecto, se obliga a indemnizar al COMPRADOR por cualesquiera daños y perjuicios que sufra directamente, o por toda reclamación, acción o procedimiento que traiga su causa de un incumplimiento o cumplimiento defectuoso por parte del VENDEDOR de lo dispuesto tanto en el Contrato como en la normativa reguladora de la protección de datos de carácter personal.

A los efectos del RGPD y de la LOPDGDD, el VENDEDOR únicamente tratará los datos de carácter personal a los que tenga acceso conforme a las instrucciones del COMPRADOR y no los aplicará o utilizará con un fin distinto al objeto del Contrato, ni los comunicará, ni siquiera para su conservación, a otras personas. En el caso de que el VENDEDOR destine los datos a otra finalidad, los comunique o los utilice incumpliendo las estipulaciones del Contrato, será considerado también responsable del tratamiento, respondiendo de las infracciones en que hubiera incurrido personalmente.

El VENDEDOR deberá adoptar las medidas de índole técnica y organizativas necesarias que garanticen la seguridad de los datos de carácter personal y eviten su alteración, pérdida, tratamiento o acceso no autorizado, habida cuenta del estado de la tecnología, la naturaleza de los datos almacenados y los riesgos a que están expuestos, ya provengan de la acción humana o del medio físico o natural, de conformidad con el artículo 32 del RGPD.

El COMPRADOR podrá en cualquier momento ejercitar los derechos de acceso, rectificación, supresión, oposición, limitación del tratamiento y portabilidad, enviando por carta certificada la solicitud, indicando los motivos y junto con la fotocopia del DNI, a la dirección [DIRECCIÓN DEL VENDEDOR].

NOVENA.– Gastos e impuestos

[ELEGIR: EL COMPRADOR / EL VENDEDOR / AMBAS PARTES POR MITAD] se hará cargo de la totalidad de los tributos, cualquiera que sea su naturaleza y carácter, que se devenguen como consecuencia del Contrato, así como de cualesquiera operaciones físicas y jurídicas que conlleve, salvo el Impuesto sobre el Valor Añadido (IVA) o su equivalente.

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del procurador y abogado aunque sus intervenciones no fueran preceptivas.

DÉCIMA.– Jurisdicción competente y ley aplicable

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Sumisión a tribunales, sin cláusula penal

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los tribunales de [LOCALIDAD], en [PROVINCIA], renunciando expresamente a su fuero propio si lo tuvieran.

El presente contrato tiene exclusivamente carácter mercantil, no existiendo vínculo laboral alguno entre el COMPRADOR y el VENDEDOR, y se regirá por sus propias cláusulas y, en lo no dispuesto en ellas, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

— Sumisión a tribunales, con cláusula penal en caso de no ejecución voluntaria de la sentencia

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los tribunales de [LOCALIDAD], en [PROVINCIA], renunciando expresamente a su fuero propio si lo tuvieran.

En el caso de que la parte o partes que hubieran resultado condenadas en el fallo de la sentencia no cumplieran voluntariamente con el fallo de la sentencia en el plazo de [Nº] días, deberán abonar a quien le hubiera vencido en el pleito la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE EN CIFRA] €), sin perjuicio de la indemnización por daños y perjuicios que pudiera corresponderles.

El presente contrato tiene exclusivamente carácter mercantil, no existiendo vínculo laboral alguno entre el COMPRADOR y el VENDEDOR, y se regirá por sus propias cláusulas y, en lo no dispuesto en ellas, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

— Sumisión a arbitraje, sin cláusula penal

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al arbitraje de [ELEGIR: Derecho / equidad] de [INSTITUCIÓN ARBITRAL, DE ÁMBITO TERRITORIAL [ÁMBITO TERRITORIAL]], en adelante [ABREVIATURA DE LA INSTITUCIÓN], a la cual encomiendan la administración del arbitraje y la designación de los árbitros. El arbitraje se realizará de acuerdo con el procedimiento establecido en el reglamento de la [CORTE ARBITRAL]. Según el artículo 34 de la Ley 60/2003, de 23 de diciembre, de Arbitraje, los árbitros sólo decidirán en equidad si las partes les han autorizado expresamente para ello y, en aquello que no esté previsto, se estará a la Ley 60/2003. Ambas partes se obligan a aceptar y cumplir la decisión contenida en el laudo arbitral, dictado según lo que se establece en el mencionado reglamento.

El presente contrato tiene exclusivamente carácter mercantil, no existiendo vínculo laboral alguno entre el COMPRADOR y el VENDEDOR, y se regirá por sus propias cláusulas y, en lo no dispuesto en ellas, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

— Sumisión a arbitraje, con cláusula penal en caso de no ejecución voluntaria del laudo

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al arbitraje de [ELEGIR: Derecho / equidad] de [INSTITUCIÓN ARBITRAL, DE ÁMBITO TERRITORIAL [ÁMBITO TERRITORIAL]], en adelante [ABREVIATURA DE LA INSTITUCIÓN], a la cual encomiendan la administración del arbitraje y la designación de los árbitros. El arbitraje se realizará de acuerdo con el procedimiento establecido en el reglamento de la [CORTE ARBITRAL]. Según el artículo 34 de la Ley 60/2003, de 23 de diciembre, de Arbitraje, los árbitros sólo decidirán en equidad si las partes les han autorizado expresamente para ello y, en aquello que no esté previsto, se estará a la Ley 60/2003. Ambas partes se obligan a aceptar y cumplir la decisión contenida en el laudo arbitral, dictado según lo que se establece en el mencionado reglamento.

En el caso de que la parte o partes que hubieran resultado condenadas en el laudo no cumplieran voluntariamente con el fallo del mismo en el plazo de [Nº] días, deberán abonar a quien le hubiera vencido en el procedimiento la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE EN CIFRA] €), sin perjuicio de la indemnización por daños y perjuicios que pudiera corresponderles.

El presente contrato tiene exclusivamente carácter mercantil, no existiendo vínculo laboral alguno entre el COMPRADOR y el VENDEDOR, y se regirá por sus propias cláusulas y, en lo no dispuesto en ellas, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

UNDÉCIMA.– Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

DUODÉCIMA.– Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso, las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº DE FOLIOS] folios del presente CONTRATO DE COMPRAVENTA DE DOMINIO, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo.: D./Dña. [NOMBRE Y APELLIDOS] (El Comprador)

Fdo.: D./Dña. [NOMBRE Y APELLIDOS] (El Vendedor)

ANEXO I. DATOS DE REGISTRO DEL DOMINIO A NOMBRE DEL COMPRADOR

Nombre o denominación social del titular: [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL]

NIF: [NIF]

Domicilio: [DOMICILIO]

Contacto administrativo: [NOMBRE, CORREO ELECTRÓNICO Y TELÉFONO]

Contacto técnico: [NOMBRE, CORREO ELECTRÓNICO Y TELÉFONO]

Contacto de pago: [NOMBRE, CORREO ELECTRÓNICO Y TELÉFONO]

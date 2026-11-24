---
name: contrato-mercantil-obra-servicios-prestados-regimen-mer-0607
description: "Contrato mercantil de obra o servicios prestados en régimen de teletrabajo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato mercantil de obra o servicios prestados en régimen de teletrabajo

> Formulario **MER-0607** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato mercantil de arrendamiento de obra o servicios a través de teletrabajo, mediante el cual el teletrabajador realizará las actividades para las que se le contrata en el local en el que desarrolla su actividad profesional. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del contrato, así como los derechos y obligaciones de cada una de las partes.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato mercantil de obra o servicios prestados en régimen de teletrabajo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato mercantil de obra o servicios prestados en régimen de teletrabajo” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-mercantil-obra-servicios-prestados-regimen-mer-0607`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] ACTIVIDAD (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DENOMINACIÓN ABREVIADA (2 veces)
- [ ] INSTITUCIÓN ARBITRAL (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE FAX O CORREO ELECTRÓNICO (2 veces)
- [ ] ÓRGANO (2 veces)
- [ ] ENTIDAD BANCARIA
- [ ] EQUIPOS INFORMÁTICOS
- [ ] FECHA
- [ ] LUGAR
- [ ] NECESIDAD DE LA EMPRESA
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE ARTÍCULO
- [ ] NÚMERO
- [ ] OBJETO DEL CONTRATO
- [ ] OBJETO SOCIAL
- [ ] OTROS DATOS
- [ ] PERIODICIDAD
- [ ] PLAZO
- [ ] SOPORTE DE LA ENTREGA
- [ ] TITULACIÓN

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

Modelo de contrato mercantil de arrendamiento de obra o servicios a través de teletrabajo, mediante el cual el teletrabajador realizará las actividades para las que se le contrata en el local en el que desarrolla su actividad profesional. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del contrato, así como los derechos y obligaciones de cada una de las partes.

Notas al pie del formulario original:
(1) Téngase en cuenta la posibilidad de combinar la cláusula arbitral con otras (cláusulas híbridas arbitraje/jurisdicción), como las de mediación o las de sumisión a determinada jurisdicción, bien permitiendo la elección a una de las partes, o a la demandante, o delimitando qué tipo de contiendas irían a una u otra vía, como señala el AAP Madrid 18-10-2013, ref. La Ley 172387/2013).


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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

(Datos de una parte)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, [DENOMINACIÓN ABREVIADA].

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

(Datos de otra parte)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, [DENOMINACIÓN ABREVIADA].

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de arrendamiento de obra o servicios en la modalidad de teletrabajo y, a tal fin,

MANIFIESTAN

I.- Que la EMPRESA es una sociedad mercantil cuyo objeto social consiste en [OBJETO SOCIAL], según consta en el artículo [Nº DE ARTÍCULO] de sus Estatutos Sociales, debidamente inscritos.

II.- Que entre las necesidades de la EMPRESA está la de [NECESIDAD DE LA EMPRESA].

III.- Que el TELETRABAJADOR es Licenciado en [TITULACIÓN] y cuenta con una experiencia de [Nº] años en la realización de [ACTIVIDAD] en las empresas [NOMBRE DE LA PARTE], por lo que dispone de la titulación, conocimientos y medios suficientes para realizar trabajos de [ACTIVIDAD] (los ajustados a las necesidades de la EMPRESA señalados en la manifestación precedente), por lo que

ACUERDAN

Celebrar el presente CONTRATO DE ARRENDAMIENTO DE OBRA/SERVICIOS, que libre y espontáneamente sujetan a las siguientes:

CLÁUSULAS

Primera.- Objeto del contrato

Por el presente contrato la EMPRESA contrata al TELETRABAJADOR para que realice, en régimen de arrendamiento de obra/servicios, los trabajos de [ACTIVIDAD] que la EMPRESA le encomiende, de acuerdo con los términos del presente contrato.

Las actividades descritas se desarrollarán en el local que el TELETRABAJADOR utiliza para su actividad profesional, mediante sistema de prestación de servicios a distancia, comúnmente conocido como TELETRABAJO, por conexión por vía telemática de los equipos informáticos de la EMPRESA y del TELETRABAJADOR.

La relación entre las partes tiene carácter exclusivamente mercantil. El TELETRABAJADOR no está sujeto a horario ni lugar de trabajo, desempeñando su función con organización propia y en las horas más idóneas para su cumplimiento, no teniendo ningún tipo de dependencia laboral con la EMPRESA.

A tales efectos, el TELETRABAJADOR manifiesta que está dado de alta en el régimen especial de trabajadores autónomos, exhibiendo documentación acreditativa de tales circunstancias. (Respecto a la Licencia Fiscal, ha desaparecido la cuantía del impuesto de actividades económicas, no obstante las partes pueden señalar como requisito el alta en el mismo -a efectos censales-; también pueden precisarse otras altas específicas, por ejemplo en algún colegio profesional)

Segunda.- Prestación de los servicios/realización de la obra

2.1.- [OBJETO DEL CONTRATO]

2.2.- Además, en caso de que la EMPRESA requiriera los servicios del TELETRABAJADOR para funciones distintas de las descritas, le remitirá una SOLICITUD DE SERVICIO, en la que, en la medida de lo posible, se detallarán los siguientes extremos:

- Descripción, lo más detallada posible, de las labores a realizar por el TELETRABAJADOR.
- Plazo de máximo de entrega [PLAZO].

Dichas solicitudes de servicio quedarán sujetas a los términos del presente contrato, incorporándose al mismo como Anexos.

Las solicitudes de servicio podrán realizarse vía fax o por correo electrónico, debiendo dirigirse, según la modalidad elegida, a:

- [Nº DE FAX O CORREO ELECTRÓNICO]
- [Nº DE FAX O CORREO ELECTRÓNICO]

Cualquier cambio en los datos particulares del TELETRABAJADOR contenidos en la presente cláusula, deberán ser comunicados por escrito y con la máxima urgencia a la EMPRESA por parte del TELETRABAJADOR.

El TELETRABAJADOR quedará obligado a la realización de los servicios solicitados desde el momento de la recepción de cada solicitud de servicio. La realización de dichos servicios quedará sujeta a los términos y condiciones del presente contrato.

2.3.- Tanto para el desempeño de las funciones genéricas descritas en el apartado 2.1 de la presente cláusula como para el cumplimiento de los servicios solicitados por la EMPRESA según lo expuesto en el apartado 2.2 precedente, el TELETRABAJADOR podrá solicitar a la EMPRESA cuanta información adicional le sea precisa.

Una vez recibida dicha información, el TELETRABAJADOR podrá solicitar la modificación de los eventuales plazos de entrega, si concurren causas justificadas al efecto. La modificación en el plazo de entrega deberá ser aceptada por ambas partes expresamente y por escrito.

2.4.- La EMPRESA entregará con la mayor brevedad posible al TELETRABAJADOR la información necesaria para la prestación de sus servicios. La entrega se efectuará en [SOPORTE DE LA ENTREGA] mediante [ÓRGANO].

2.5.- El TELETRABAJADOR dispondrá, en sus instalaciones, de un entorno de desarrollo propio, con los equipos hardware [EQUIPOS INFORMÁTICOS] necesarios para trabajar en conexión con el equipo central de proceso de datos de la EMPRESA. No obstante, el entorno de desarrollo propio que el TELETRABAJADOR destine a su conexión con el equipo central de proceso de datos de la EMPRESA, se hallará aislado, sin conexión a otros equipos, tanto de terceros, como con otros equipos o sistemas informáticos que el TELETRABAJADOR tenga instalados en sus dependencias.

La EMPRESA / El TELETRABAJADOR asumirá el coste de la(s) línea(s) de conexión de voz y datos (principal y de seguridad o ‘back-up’) entre los equipos de la EMPRESA y las instalaciones del TELETRABAJADOR.

Con el fin de garantizar la confidencialidad en las comunicaciones que tengan lugar entre los equipos informáticos de la EMPRESA y el entorno de desarrollo del TELETRABAJADOR, ambas partes procurarán que la línea de conexión entre ambos sea directa. Caso de no ser posible establecer este tipo de línea, el TELETRABAJADOR será responsable de establecer cuantas medidas sean necesarias para garantizar dicha confidencialidad (tales como sistemas de cifrado de datos, etc.).

El acceso a los diferentes entornos y sistemas informáticos de la EMPRESA (desarrollo y pruebas) será efectuado siempre y en todo momento bajo el control y la responsabilidad de la EMPRESA y siguiendo los procedimiento establecidos por la EMPRESA, procedimientos que serán comunicados al TELETRABAJADOR con la suficiente antelación. En cualquier caso, el TELETRABAJADOR será responsable del cumplimiento de tales procedimientos.

2.6.- El incumplimiento de cualquiera de los plazos de entrega por parte del TELETRABAJADOR dará lugar a una indemnización de [IMPORTE] euros por día de retraso, siempre que el mismo no sea directamente imputable a la EMPRESA.

2.7.- En caso de que la EMPRESA detecte algún error o punto oscuro en las labores realizadas por el TELETRABAJADOR, éste procederá a la inmediata subsanación de los defectos detectados y/o a la aclaración de las dudas suscitadas.

2.8.- Además, el TELETRABAJADOR se obliga a acudir con una frecuencia [PERIODICIDAD] a las oficinas de la EMPRESA para exponer la evolución de su trabajo ante el [ÓRGANO]. A tal fin, la EMPRESA se compromete a convocar las oportunas reuniones, comunicando al TELETRABAJADOR la fecha y hora con una antelación mínima de [Nº] días naturales.

Tercera.- Precio y forma de pago

Como contraprestación a los servicios que el TELETRABAJADOR desarrolle, se establece un precio de [IMPORTE] euros al mes, impuestos excluidos [OTROS DATOS].

A tales efectos el TELETRABAJADOR emitirá una factura mensual correspondiente a dicho importe, que la EMPRESA le abonará mediante transferencia bancaria de tal cantidad a la cuenta de la que es titular, número [NÚMERO], de la entidad bancaria [ENTIDAD BANCARIA].

Cuarta.- Confidencialidad y tratamiento de datos de carácter personal

4. 1.- Confidencialidad.

El TELETRABAJADOR se compromete a guardar la máxima reserva y confidencialidad sobre el resultado de cada uno de los trabajos que la EMPRESA le encomiende.

Se considerará información confidencial cualquier información relacionada con los trabajos encomendados al TELETRABAJADOR en virtud del presente contrato (y, en su caso, en especial, los programas de ordenador, los manuales de aplicación, los análisis funcionales y orgánicos, y cualquier otra documentación, dato o material de apoyo derivado de las labores encomendadas al TELETRABAJADOR, así como la información propia de la EMPRESA a la que haya accedido durante la realización de sus funciones).

El TELETRABAJADOR se compromete a no divulgar dicha información confidencial, así como a no publicarla ni de cualquier otro modo, bien directamente, bien a través de terceras personas o empresas, ponerla a disposición de terceros sin el previo consentimiento por escrito de la EMPRESA.

4. 2.- Tratamiento automatizado de datos de carácter personal.

El TELETRABAJADOR reconoce que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales. A tal efecto, el TELETRABAJADOR

a) Únicamente accederá a los datos personales de clientes y demás personas físicas relacionadas con la EMPRESA si tal acceso fuese necesario para cumplir con las obligaciones establecidas para el TELETRABAJADOR en el presente Contrato.

b) Se compromete a:

- Utilizar los datos de carácter personal a los que tenga acceso única y exclusivamente para cumplir con sus obligaciones contractuales para con la EMPRESA
- Observar y adoptar cuantas medidas de seguridad sean necesarias para asegurar la confidencialidad, secreto e integridad de los datos de carácter personal a los que tenga acceso, en especial las indicadas en la cláusula 2.5, así como a adoptar en el futuro cuantas medidas de seguridad sean exigidas por las leyes y reglamentos destinadas a preservar el secreto, confidencialidad e integridad en el tratamiento automatizado de datos personales.
- A no ceder en ningún caso a terceras personas los datos de carácter personal a los que tenga acceso, ni tan siquiera a efectos de su conservación.

4. 3.-

Las obligaciones establecidas para el TELETRABAJADOR en la presente cláusula serán también de obligado cumplimiento para sus posibles empleados, colaboradores, tanto externos como internos, y subcontratistas, por lo que el TELETRABAJADOR responderá frente a la EMPRESA si tales obligaciones son incumplidas por tales empleados, colaboradores y subcontratistas.

4. 4.-

El incumplimiento por parte del TELETRABAJADOR de cualesquiera de las obligaciones de establecidas en la presente cláusula de Confidencialidad y Tratamiento de Datos de Carácter Personal, generará una indemnización en favor de la EMPRESA de [IMPORTE] euros, sin perjuicio del derecho de la EMPRESA de resarcirse de los perjuicios que le sean causados y que superen la cuantía indicada.

4. 5.-

La duración de las obligaciones de confidencialidad establecidas en el presente contrato tendrán una duración indefinida, manteniéndose en vigor con posterioridad a la finalización, por cualquier causa, de la relación entre la EMPRESA y el TELETRABAJADOR.

Quinta.- Arbitraje y competencia jurisdiccional

Para cualquier divergencia surgida del presente contrato, ambas partes se someten expresamente, y con renuncia a su fuero propio, a la decisión del asunto o litigio planteado, mediante el arbitraje institucional de [INSTITUCIÓN ARBITRAL], a la cual encomiendan la administración del arbitraje y la designación de los árbitros.

a) El arbitraje se realizará conforme al procedimiento establecido en el Reglamento Arbitral de [INSTITUCIÓN ARBITRAL] y en la Ley de Arbitraje Ley 60/2003, de 23 de diciembre).
b) El laudo arbitral deberá dictarse durante los noventa días siguientes a la aceptación del cargo por parte de los árbitros designados, obligándose ambas partes a aceptar y cumplir la decisión contenida en él.
c) Para el caso de que el arbitraje no llegara a realizarse por mutuo acuerdo o fuese declarado nulo, ambas partes se someten a los Tribunales de [LOCALIDAD] con renuncia a su propio fuero, si éste fuese otro.

Sexta.- Vigencia y extinción

El presente contrato tendrá una duración de un año, y se renovará de forma automática por períodos de igual duración, salvo que medie preaviso de cualquiera de las partes con un mes de antelación.

La concurrencia de preaviso de extinción por parte del TELETRABAJADOR de acuerdo con lo anterior, no le exonerará de sus obligaciones y responsabilidades por la finalización de tareas en curso o en ejecución en el momento de producirse tal preaviso.

Este contrato se extinguirá por las causas generales establecidas en la Ley y en especial, por incumplimiento de las obligaciones dimanantes de este escrito.

Séptima.- Actualización

En el caso de que alguna o algunas de las cláusulas del contrato pasen a ser inválidas, ilegales o inejecutables en virtud de alguna norma jurídica, se considerarán ineficaces en la medida que corresponda, pero en lo demás, este contrato conservará su validez. Las partes contratantes acuerdan sustituir la cláusula o cláusulas afectadas por otra u otras que tengan los efectos económicos más semejantes a los de las sustituidas.

Y para que así conste, y en prueba de conformidad y aceptación al contenido de este escrito, ambas partes lo firman por duplicado y a un sólo efecto en la fecha y lugar indicados en el encabezamiento.

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

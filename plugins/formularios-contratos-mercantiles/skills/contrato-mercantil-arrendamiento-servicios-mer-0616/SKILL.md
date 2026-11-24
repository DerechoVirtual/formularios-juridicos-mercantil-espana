---
name: contrato-mercantil-arrendamiento-servicios-mer-0616
description: "Contrato mercantil de arrendamiento de servicios profesionales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato mercantil de arrendamiento de servicios profesionales

> Formulario **MER-0616** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato mercantil de arrendamiento o prestación de servicios por el que el cliente contrata los servicios profesionales del prestador, que se compromete a no divulgar la información confidencial; regula objeto, duración, precio, modificaciones, protección de datos, resolución y jurisdicción.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato mercantil de arrendamiento de servicios profesionales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato mercantil de arrendamiento de servicios profesionales” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-mercantil-arrendamiento-servicios-mer-0616`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] IMPORTE (6 veces)
- [ ] DNI/NIE/PASAPORTE (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] NACIONALIDAD (3 veces)
- [ ] NOMBRE (3 veces)
- [ ] Nº (3 veces)
- [ ] Nº DE CUENTA (3 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DATOS REGISTRALES: FOLIO, TOMO GENERAL DEL LIBRO DE SOCIEDADES, HOJA (2 veces)
- [ ] DÍA (2 veces)
- [ ] INSTITUCIÓN ARBITRAL (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (2 veces)
- [ ] ACTIVIDAD DEL CLIENTE
- [ ] ACTIVIDAD DEL PRESTADOR
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DE LOS SERVICIOS
- [ ] FECHA
- [ ] LOCALIDAD, CALLE Y NÚMERO
- [ ] MES
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] Nº DE PROTOCOLO
- [ ] OTRAS CAUSAS DE RESOLUCIÓN.
- [ ] PLAZO
- [ ] SEDE

## Normas que cita el formulario

- art. 5 LOPDGDD
- art. 1124 Código Civil

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

- Junto a «…ioridad a la finalización, por cualquier causa, de la relación entre las partes.»: si el prestador accede a datos personales de los que el cliente es responsable, debe formalizarse además el contrato de encargado del tratamiento previsto en el art. 28 RGPD.

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

DE UNA PARTE, (Datos del PRESTADOR DE SERVICIOS)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero/a / casado/a / divorciado/a / separado/a / viudo/a], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y DNI/Pasaporte número [DNI/NIE/PASAPORTE].

[OPCIONAL — incluir si procede (estado civil casado/a)]

Casado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con DNI/Pasaporte número [DNI/NIE/PASAPORTE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, PRESTADOR DE SERVICIOS.

[Si hay varios prestadores, repetir el párrafo anterior por cada uno.]

Y DE OTRA, (Datos del CLIENTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero/a / casado/a / divorciado/a / separado/a / viudo/a], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y DNI/Pasaporte número [DNI/NIE/PASAPORTE].

[OPCIONAL — incluir si procede (estado civil casado/a)]

Casado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con DNI/Pasaporte número [DNI/NIE/PASAPORTE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CLIENTE.

INTERVIENEN

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Todas las partes en su propio nombre y representación.

— D./Dña. [NOMBRE Y APELLIDOS], en su propio nombre y representación. [Repetir por cada parte que actúe en nombre propio.]

— D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de: [ELEGIR UNA DE LAS DOS SIGUIENTES:]

— (Si se trata de persona física) D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad [NACIONALIDAD], domiciliado/a en [DOMICILIO], con DNI/Pasaporte número [DNI/NIE/PASAPORTE].

— (Si se trata de persona jurídica) La compañía mercantil denominada [DENOMINACIÓN SOCIAL], domiciliada en [LOCALIDAD, CALLE Y NÚMERO], con NIF núm. [NIF], inscrita en el Registro Mercantil de [LOCALIDAD], [DATOS REGISTRALES: FOLIO, TOMO GENERAL DEL LIBRO DE SOCIEDADES, HOJA]. Hace uso de las facultades conferidas a su favor en calidad de [ELEGIR: administrador único / administrador solidario / consejero delegado / apoderado] de la sociedad indicada, cargo para el que fue nombrado en escritura otorgada ante notario de [LOCALIDAD], D./Dña. [NOMBRE DEL NOTARIO], el [FECHA], con el número [Nº DE PROTOCOLO] de su protocolo, que causó inscripción en el Registro Mercantil de [LOCALIDAD], [DATOS REGISTRALES: FOLIO, TOMO GENERAL DEL LIBRO DE SOCIEDADES, HOJA].

Intervienen ambos en su propio nombre y derecho, reconociéndose la mutua capacidad legal necesaria para otorgar el presente contrato de arrendamiento de servicios, y a tal fin

MANIFIESTAN

I. Que el CLIENTE se dedica a [ACTIVIDAD DEL CLIENTE] y está interesado en contratar los servicios del PRESTADOR DE SERVICIOS.

II. Que el PRESTADOR DE SERVICIOS tiene como actividad principal [ACTIVIDAD DEL PRESTADOR] y dispone de las instalaciones y conocimientos necesarios para prestar los servicios objeto del presente contrato, en lo sucesivo, los Servicios.

III. Que por todo ello, ambas partes han acordado la celebración del presente contrato de arrendamiento de servicios, en lo sucesivo EL CONTRATO, en los términos que se estipulan en las siguientes

CLÁUSULAS

Primera.- Objeto

EL PRESTADOR DE SERVICIOS se compromete a realizar los Servicios siguientes, conforme a los términos y condiciones previstos en las cláusulas siguientes: [DESCRIPCIÓN DE LOS SERVICIOS].

Segunda.- Duración

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si se pacta un plazo máximo antes del cual el servicio contratado debe estar realizado) El plazo máximo para la realización de los Servicios será el de [Nº] [ELEGIR: días / meses / años] contados a partir del día siguiente a la firma del presente contrato, pudiendo prorrogarse, a voluntad de las partes y de común acuerdo, con una antelación de [PLAZO].

— (Si se pacta un período durante el cual se va a prestar el servicio) El PRESTADOR DE SERVICIOS realizará los Servicios objeto del presente contrato durante un período de [Nº] [ELEGIR: días / meses / años] contados a partir del día siguiente a la firma del presente contrato.

Una vez finalizado dicho plazo sin que ninguna de las partes haya manifestado lo contrario por escrito mediante [MEDIO DE NOTIFICACIÓN: puede pactarse burofax u otro medio fehaciente], el contrato se entenderá renovado de manera tácita por iguales períodos.

Tercera.- Precio

El precio que el CLIENTE debe abonar al PRESTADOR DE SERVICIOS por los Servicios objeto del presente contrato es de [IMPORTE] euros, no incluyendo los impuestos indirectos aplicables, y sin perjuicio de lo previsto en la cláusula siguiente relativa a las modificaciones que puedan producirse en los Servicios. La forma de abono del citado precio será:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (En caso de pago único) El CLIENTE pagará el precio en el momento en que EL PRESTADOR DE SERVICIOS haya finalizado completamente la prestación de los Servicios mediante [ELEGIR: abono por transferencia bancaria a la cuenta corriente [Nº DE CUENTA] / pago en metálico / cheque girado a nombre de [NOMBRE]].

— (En caso de pago parcial al firmar el contrato y pago del resto del precio al final) EL CLIENTE abona [IMPORTE] euros en el momento de la firma del presente contrato. El precio restante, consistente en [IMPORTE] euros, se pagará en el momento en que EL PRESTADOR DE SERVICIOS haya finalizado completamente la prestación de los Servicios mediante [ELEGIR: abono por transferencia bancaria a la cuenta corriente [Nº DE CUENTA] / pago en metálico / cheque girado a nombre de [NOMBRE]].

— (En caso de pagos periódicos) EL CLIENTE abonará [IMPORTE] euros [ELEGIR: el día [DÍA] de cada mes / dentro de los 5 últimos días de cada mes / dentro de los 5 primeros días de cada mes], importe de la correspondiente factura emitida por el PRESTADOR DE SERVICIOS, mediante [ELEGIR: abono por transferencia bancaria a la cuenta corriente [Nº DE CUENTA] / pago en metálico / cheque girado a nombre de [NOMBRE]].

Cuarta.- Modificaciones de los Servicios

Las partes podrán modificar de mutuo acuerdo los Servicios objeto del presente contrato durante la vigencia del mismo, cuando así lo consideren oportuno.

A tal efecto, la parte que considere necesaria la revisión de los Servicios o su precio o cualquiera otra de las estipulaciones del presente contrato, enviará propuesta por escrito a la otra parte, a fin de comenzar las negociaciones.

Las modificaciones resultantes de dicho acuerdo deberán hacerse constar por escrito.

Quinta.- Confidencialidad

Tanto el CLIENTE como el PRESTADOR DE SERVICIOS se comprometen a no divulgar la información y documentación confidencial referente a la otra parte de la que hayan tenido conocimiento por razón de la ejecución del presente contrato, salvo las indispensables para su cumplimiento, y a mantenerla en secreto, incluso después de la finalización del mismo.

Ambas partes acuerdan tomar las medidas necesarias respecto a su personal e incluso terceros que puedan tener acceso a dicha información y documentación, a fin de garantizar la confidencialidad objeto de esta cláusula.

Sexta.- Protección de datos personales

El PRESTADOR DE SERVICIOS reconoce que la legislación sobre protección de datos personales, constituida por el Reglamento (UE) 2016/679 (RGPD) y la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales (LOPDGDD), establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales. A tal efecto, el PRESTADOR DE SERVICIOS:

a) Únicamente accederá a los datos personales de clientes y demás personas físicas relacionadas con el CLIENTE si tal acceso fuese necesario para cumplir con los servicios objeto del presente contrato.

b) Se compromete a:

- Utilizar los datos de carácter personal a los que tenga acceso única y exclusivamente para cumplir con sus obligaciones contractuales para con el CLIENTE.

- Observar y adoptar cuantas medidas de seguridad sean necesarias para asegurar la confidencialidad, secreto e integridad de los datos de carácter personal a los que tenga acceso, así como adoptar en el futuro cuantas medidas de seguridad sean exigidas por las leyes y reglamentos destinadas a preservar el secreto, confidencialidad e integridad en el tratamiento automatizado de datos personales (arts. 5 y 6 LOPDGDD).

- No ceder en ningún caso a terceras personas los datos de carácter personal a los que tenga acceso, ni tan siquiera a efectos de su conservación.

Las obligaciones establecidas para el PRESTADOR DE SERVICIOS por la presente cláusula serán también de obligado cumplimiento para sus posibles empleados, colaboradores, tanto externos como internos, y subcontratistas, por lo que el PRESTADOR DE SERVICIOS responderá frente al CLIENTE si tales obligaciones son incumplidas por tales empleados, colaboradores y subcontratistas.

El incumplimiento por parte del PRESTADOR DE SERVICIOS de cualesquiera de las obligaciones establecidas en la anterior cláusula de Confidencialidad y en ésta de Protección de datos personales, generará una indemnización en favor del CLIENTE de [IMPORTE] euros, sin perjuicio del derecho del CLIENTE a resarcirse de los perjuicios que le sean causados y que superen la cuantía indicada.

La duración de las obligaciones de confidencialidad establecidas en el presente contrato será indefinida, manteniéndose en vigor con posterioridad a la finalización, por cualquier causa, de la relación entre las partes.

Séptima.- Resolución del contrato (véase art. 1124 del Código Civil)

Serán causa de resolución del contrato, las siguientes:

- La voluntad de cualquiera de las partes, que acuerdan un preaviso por escrito con una antelación de [Nº] [ELEGIR: días / meses]. Si el CLIENTE no cumple el preaviso descrito deberá abonar al PRESTADOR DE SERVICIOS una cantidad de [IMPORTE] euros; si es el PRESTADOR DE SERVICIOS quien incumple dicho plazo, dejará de recibir dicha cantidad del pago pendiente.

- La voluntad de cualquiera de las partes por incumplimiento grave por parte de la otra parte con respecto a las obligaciones pactadas. Se considerará en todo caso que es incumplimiento grave [SUPUESTOS: por ejemplo, el impago o el pago con retraso durante más de 2 mensualidades].

- [OTRAS CAUSAS DE RESOLUCIÓN.]

Octava.- Ley aplicable y jurisdicción competente. Inexistencia de relación laboral

Al presente contrato se aplica la normativa española sobre contratos de arrendamiento de servicios prevista en el Código Civil y cualquier litigio sobre el mismo se resolverá [ELEGIR: en los Tribunales de Instancia de [SEDE] / por arbitraje de derecho ante [INSTITUCIÓN ARBITRAL] / por arbitraje de equidad ante [INSTITUCIÓN ARBITRAL]].

En ningún caso se considerará que la relación del PRESTADOR DE SERVICIOS y el CLIENTE es de naturaleza laboral.

Novena.- Comunicaciones y notificaciones

En general, las comunicaciones entre las partes de asuntos relacionados con el presente contrato se realizarán por escrito mediante [ELEGIR: correo postal / correo electrónico con acuse de recibo / correo certificado] y se entenderán debidamente realizadas cuando por ejemplo se obtenga el correspondiente acuse de recibo.

[OPCIONAL — incluir si procede]

A tal efecto, se designan las siguientes personas y sus respectivos correos electrónicos como interlocutores de cada una de las partes para las finalidades que en cada caso se describen:

Por el PRESTADOR DE SERVICIOS: D./Dña. [NOMBRE Y APELLIDOS], con correo electrónico [CORREO ELECTRÓNICO], para asuntos relacionados con [MATERIA: compras, facturación, etc.]. [Repetir por cada interlocutor.]

Por el CLIENTE: D./Dña. [NOMBRE Y APELLIDOS], con correo electrónico [CORREO ELECTRÓNICO], para asuntos relacionados con [MATERIA: compras, facturación, etc.]. [Repetir por cada interlocutor.]

Décima.- Gastos e impuestos

Serán de cuenta [ELEGIR: del CLIENTE / del PRESTADOR DE SERVICIOS] todos los gastos y costas judiciales, así como los honorarios de Abogado y derechos de Procurador, aunque la intervención de los mismos no sea preceptiva, que se originen como consecuencia del incumplimiento de su prestación profesional pactada en el presente contrato.

Y leído el presente documento, ambas partes lo firman en prueba de su conformidad, a un solo efecto y por duplicado, en el lugar y fecha ut supra.

PRESTADOR DE SERVICIOS: Firmado: D./Dña. [NOMBRE Y APELLIDOS]

CLIENTE: Firmado: D./Dña. [NOMBRE Y APELLIDOS]

---
name: contrato-prestacion-servicios-entre-empresas-mer-0601
description: "Contrato de prestación de servicios entre empresas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de prestación de servicios entre empresas

> Formulario **MER-0601** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato mercantil de arrendamiento o prestación de servicios entre empresas (con ejemplo de descripción de servicios de asesoría jurídica), que fija objeto, duración, precio, resolución anticipada, confidencialidad, protección de datos y jurisdicción.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de prestación de servicios entre empresas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de prestación de servicios entre empresas” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-prestacion-servicios-entre-empresas-mer-0601`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] IMPORTE (5 veces)
- [ ] DOMICILIO (4 veces)
- [ ] CORREO ELECTRÓNICO (3 veces)
- [ ] DNI/PASAPORTE (3 veces)
- [ ] IBAN (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NACIONALIDAD (3 veces)
- [ ] NOMBRE DEL BENEFICIARIO (3 veces)
- [ ] Nº (3 veces)
- [ ] ASUNTOS: COMPRAS, FACTURACIÓN, ETC. (2 veces)
- [ ] DATOS REGISTRALES: FOLIO, TOMO, HOJA (2 veces)
- [ ] DESCRIPCIÓN (2 veces)
- [ ] DNI/PASAPORTE DEL CÓNYUGE (2 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] INSTITUCIÓN ARBITRAL (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] ACTIVIDAD DE LA EMPRESA
- [ ] ACTIVIDAD DEL CLIENTE
- [ ] ACTIVIDAD PROFESIONAL
- [ ] ASUNTOS
- [ ] AÑO
- [ ] CORREOS ELECTRÓNICOS
- [ ] DEDICACIÓN
- [ ] DENOMINACIÓN DEL SERVICIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DE LOS SERVICIOS
- [ ] DOMICILIO SOCIAL
- [ ] ESPECIFICAR SU MODO DE DETERMINACIÓN
- [ ] FINALIDAD DE LA CONTRATACIÓN
- [ ] INDICADOR
- [ ] JURÍDICOS
- [ ] LOCALIDAD, CALLE Y NÚMERO
- [ ] MATERIA
- [ ] MES
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTADO
- [ ] … y 4 datos más que aparecen una vez en el modelo

## Normas que cita el formulario

- art. 1124 Código Civil
- art. 1262 Código Civil

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…IBAN] / pago en metálico / cheque girado a nombre de [NOMBRE DEL BENEFICIARIO]].»: si se opta por pago en metálico, comprobar los límites legales a los pagos en efectivo.
- Junto a «…finalización, por cualquier causa, de la relación entre LA EMPRESA y el CLIENTE.»: si LA EMPRESA trata datos personales por cuenta del CLIENTE, formalizar además el contrato de encargado del tratamiento con el contenido mínimo del art. 28 RGPD.

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

DE UNA PARTE,

[Datos de LA EMPRESA]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y DNI/Pasaporte número [DNI/PASAPORTE].

[OPCIONAL — incluir si procede (estado civil casado/a)]
Casado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con DNI/Pasaporte número [DNI/PASAPORTE DEL CÓNYUGE], en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, LA EMPRESA.

[Si hay más de una persona en esta posición contractual, repetir el párrafo anterior tantas veces como sea necesario.]

Y DE OTRA,

[Datos del CLIENTE]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y DNI/Pasaporte número [DNI/PASAPORTE].

[OPCIONAL — incluir si procede (estado civil casado/a)]
Casado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con DNI/Pasaporte número [DNI/PASAPORTE DEL CÓNYUGE], en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CLIENTE.

INTERVIENEN

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Todas las partes en su propio nombre y representación.

— D./Dña. [NOMBRE Y APELLIDOS], en su propio nombre y representación. (Repetir para cada parte que actúe en nombre propio.)

— D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si se trata de persona física) D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTADO], mayor de edad, de nacionalidad [NACIONALIDAD], domiciliado en [DOMICILIO], con DNI/Pasaporte número [DNI/PASAPORTE].

— (Si se trata de persona jurídica) La compañía mercantil denominada [DENOMINACIÓN SOCIAL], domiciliada en [LOCALIDAD, CALLE Y NÚMERO], con NIF núm. [NIF], inscrita en el Registro Mercantil de [PROVINCIA], en [DATOS REGISTRALES: FOLIO, TOMO, HOJA]. Hace uso de las facultades conferidas a su favor en calidad de [ELEGIR: administrador único / administrador solidario / consejero delegado / apoderado] de la sociedad indicada, cargo para el que fue nombrado en escritura otorgada ante el notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO] el [FECHA], con el número [Nº DE PROTOCOLO] de su protocolo, que causó inscripción en el Registro Mercantil de [PROVINCIA] en [DATOS REGISTRALES: FOLIO, TOMO, HOJA].

MANIFIESTAN

I.- Que LA EMPRESA se dedica a [ACTIVIDAD DE LA EMPRESA], con sede social en [DOMICILIO SOCIAL].

II.- Que EL CLIENTE se dedica a [ACTIVIDAD DEL CLIENTE] y está interesado en contratar los servicios de LA EMPRESA para [FINALIDAD DE LA CONTRATACIÓN].

En su virtud han decidido celebrar el presente CONTRATO DE PRESTACIÓN DE SERVICIOS [DENOMINACIÓN DEL SERVICIO], que se sujetará a las siguientes

CLÁUSULAS

PRIMERA.– Objeto del contrato

EL CLIENTE contrata los servicios ofrecidos por LA EMPRESA, en su calidad de profesional de la actividad de [ACTIVIDAD PROFESIONAL], quien acepta prestarlos, y consistentes en las siguientes actividades: [DESCRIPCIÓN DE LOS SERVICIOS].

[OPCIONAL — incluir si procede (ejemplo de descripción de servicios de asesoría jurídica)]
a) Asesoramiento sobre [MATERIA].

b) Tramitación de [ASUNTOS].

c) Transacciones [DESCRIPCIÓN].

d) Dirección letrada [DESCRIPCIÓN].

LA EMPRESA prestará su asesoramiento con arreglo a la mayor buena fe y diligencia, de acuerdo con su leal saber y entender, y de acuerdo con las siguientes condiciones:

a) Dedicación: [DEDICACIÓN].

b) Lugar de prestación del servicio: oficinas de LA EMPRESA, sitas en [DOMICILIO].

c) Informes: LA EMPRESA elaborará con periodicidad mensual un informe detallado de las actuaciones correspondientes a ese plazo de tiempo, que deberá remitir al CLIENTE vía correo electrónico, en las siguientes direcciones: [CORREOS ELECTRÓNICOS].

d) [OTRAS CONDICIONES].

SEGUNDA.– Duración

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Para el caso de que se pacte un plazo máximo antes del cual el servicio contratado debe estar realizado) El plazo máximo para la realización de los Servicios será el de [Nº] [ELEGIR: días / meses / años] contados a partir del día siguiente a la firma del presente contrato, pudiendo prorrogarse, a voluntad de las partes y de común acuerdo, con una antelación de [PLAZO].

— (Para el caso de que se pacte un periodo durante el cual se va a prestar el servicio) EL PRESTADOR DE SERVICIOS realizará los Servicios objeto del presente contrato durante un periodo de [Nº] [ELEGIR: días / meses / años] contados a partir del día siguiente a la firma del presente contrato.

Una vez finalizado dicho plazo sin que ninguna de las partes haya manifestado por escrito mediante [MEDIO DE NOTIFICACIÓN: puede pactarse burofax u otro medio fehaciente] lo contrario, el contrato se entenderá renovado de manera tácita por iguales periodos.

TERCERA.– Precio

Mediante este contrato de prestación de servicios [JURÍDICOS], el CLIENTE se compromete a abonar a LA EMPRESA las siguientes cantidades:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (En caso de pago único) El CLIENTE pagará el precio en el momento en que EL PRESTADOR DE SERVICIOS haya finalizado completamente la prestación de los Servicios, mediante [ELEGIR: abono por transferencia bancaria a la cuenta corriente [IBAN] / pago en metálico / cheque girado a nombre de [NOMBRE DEL BENEFICIARIO]].

— (En caso de pago parcial al firmar el contrato y pago del resto del precio al final) EL CLIENTE abona [IMPORTE] euros en el momento de la firma del presente contrato. El precio restante, consistente en [IMPORTE] euros, se pagará en el momento en que EL PRESTADOR DE SERVICIOS haya finalizado completamente la prestación de los Servicios, mediante [ELEGIR: abono por transferencia bancaria a la cuenta corriente [IBAN] / pago en metálico / cheque girado a nombre de [NOMBRE DEL BENEFICIARIO]].

— (En caso de pagos periódicos) Pago mensual de la factura girada por LA EMPRESA por [IMPORTE] EUROS, incrementados con [ELEGIR: el IVA correspondiente en cada momento / el tributo que lo sustituyera], que serán abonados, por meses vencidos, [ELEGIR: el día [DÍA] de cada mes / dentro de los 5 últimos días de cada mes / dentro de los 5 primeros días de cada mes], mediante [ELEGIR: abono por transferencia bancaria a la cuenta corriente [IBAN] / pago en metálico / cheque girado a nombre de [NOMBRE DEL BENEFICIARIO]]. El primer pago se efectuará el día [FECHA].

[OPCIONAL — incluir si procede]
En caso de prórroga del contrato, dicho precio se verá incrementado automáticamente el 1 de enero de cada ejercicio económico en la cuantía correspondiente al [ELEGIR: IPC / otro indicador: [INDICADOR]] acumulado del ejercicio anterior.

[OPCIONAL — incluir si procede]
En su caso, parte variable: [ESPECIFICAR SU MODO DE DETERMINACIÓN].

CUARTA.– Resolución anticipada (ver art. 1124 del Código Civil)

No obstante lo previsto en la Cláusula Segunda, y dado que el presente contrato está basado en la confianza, cualquiera de las partes podrá resolverlo unilateralmente, antes de la fecha pactada para su vencimiento, en cuyo caso habrá de comunicárselo a la otra parte, al menos con [Nº] [ELEGIR: meses / días] de anticipación.

Si la resolución se produjera por decisión del CLIENTE, LA EMPRESA tendrá derecho a percibir una indemnización de [IMPORTE] EUROS [OPCIONAL: determinar los parámetros para su cálculo].

QUINTA.– Suministro de datos y secreto profesional

El CLIENTE facilitará a LA EMPRESA cuantos datos, informes o material estime ésta necesario para poder llevar a cabo la prestación del servicio para el que se le contrata.

Por su parte, LA EMPRESA se compromete a prestar sus servicios bajo deber de confidencialidad respecto de los datos personales suministrados por el CLIENTE. Por ello no serán difundidos ni compartidos, salvo que medie consentimiento expreso del cliente.

SEXTA.– Protección de datos personales

[OPCIONAL — incluir si procede]
El CLIENTE da su permiso para que su dirección postal y electrónica sean tratadas y, además, utilizadas para enviar comunicaciones comerciales de promoción y publicidad de los servicios y productos ofrecidos por LA EMPRESA. LA EMPRESA pone a disposición de sus clientes la dirección de correo electrónico [CORREO ELECTRÓNICO] y el teléfono [TELÉFONO], para que estos revoquen el consentimiento prestado.

LA EMPRESA reconoce que la legislación sobre protección de datos personales (Reglamento (UE) 2016/679 (RGPD) y Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente base jurídica que las legitime. A tal efecto, LA EMPRESA:

a) Únicamente accederá a los datos personales de clientes y demás personas físicas relacionadas con el CLIENTE si tal acceso fuese necesario para cumplir con los servicios objeto del presente contrato.

b) Se compromete a:

– Utilizar los datos de carácter personal a los que tenga acceso única y exclusivamente para cumplir con sus obligaciones contractuales para con el CLIENTE.

– Observar y adoptar cuantas medidas de seguridad sean necesarias para asegurar la confidencialidad, secreto e integridad de los datos de carácter personal a los que tenga acceso, así como adoptar en el futuro cuantas medidas de seguridad sean exigidas por las leyes y reglamentos destinadas a preservar el secreto, confidencialidad e integridad en el tratamiento de datos personales.

– No ceder en ningún caso a terceras personas los datos de carácter personal a los que tenga acceso, ni tan siquiera a efectos de su conservación.

Las obligaciones establecidas para LA EMPRESA por la presente cláusula serán también de obligado cumplimiento para sus posibles empleados, colaboradores, tanto externos como internos, y subcontratistas, por lo que LA EMPRESA responderá frente al CLIENTE si tales obligaciones son incumplidas por tales empleados, colaboradores y subcontratistas.

El incumplimiento por parte de LA EMPRESA de cualesquiera de las obligaciones establecidas en la anterior cláusula de confidencialidad y en ésta de protección de datos personales, generará una indemnización en favor del CLIENTE de [IMPORTE] euros, sin perjuicio del derecho del CLIENTE a resarcirse de los perjuicios que le sean causados y que superen la cuantía indicada.

La duración de las obligaciones de confidencialidad establecidas en el presente contrato será indefinida, manteniéndose en vigor con posterioridad a la finalización, por cualquier causa, de la relación entre LA EMPRESA y el CLIENTE.

SÉPTIMA.– Legislación aplicable y jurisdicción

Las partes reconocen que la legislación aplicable al presente contrato, y a todas las relaciones jurídicas dimanantes del mismo, será la española, por expresa aplicación de lo dispuesto en el art. 1262 del Código Civil.

Las partes acuerdan someterse para la resolución de cualquier controversia, conflicto o reclamación derivada del presente contrato, a [ELEGIR: los Tribunales de [LOCALIDAD] / arbitraje de derecho ante [INSTITUCIÓN ARBITRAL] / arbitraje de equidad ante [INSTITUCIÓN ARBITRAL]], por ser éste el lugar de celebración del contrato, con renuncia expresa a cualquier otro fuero que pudiera corresponderles.

OCTAVA.– Comunicaciones y notificaciones

En general, las comunicaciones entre las partes de asuntos relacionados con el presente contrato se realizarán por escrito mediante [ELEGIR: correo postal / correo electrónico con acuse de recibo / correo certificado] y se entenderán debidamente realizadas cuando, por ejemplo, se obtenga el correspondiente acuse de recibo.

[OPCIONAL — incluir si procede]
A tal efecto, se designan las siguientes personas y sus respectivos correos electrónicos como interlocutores de cada una de las partes para las finalidades que en cada caso se describen:

Por LA EMPRESA: D./Dña. [NOMBRE Y APELLIDOS], con correo electrónico [CORREO ELECTRÓNICO], para asuntos relacionados con [ASUNTOS: COMPRAS, FACTURACIÓN, ETC.]. (Añadir más interlocutores si procede.)

Por EL CLIENTE: D./Dña. [NOMBRE Y APELLIDOS], con correo electrónico [CORREO ELECTRÓNICO], para asuntos relacionados con [ASUNTOS: COMPRAS, FACTURACIÓN, ETC.]. (Añadir más interlocutores si procede.)

NOVENA.– Gastos e impuestos

Serán de cuenta de [ELEGIR: EL CLIENTE / LA EMPRESA] todos los gastos y costas judiciales, así como los honorarios de Abogado y derechos de Procurador, aunque la intervención de los mismos no sea preceptiva, que se originen como consecuencia del incumplimiento de su prestación profesional pactada en el presente contrato.

Y leído el presente documento, ambas partes lo firman en prueba de su conformidad, a un solo efecto y por duplicado, en el lugar y fecha arriba indicados.

LA EMPRESA | EL CLIENTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] | Firmado: D./Dña. [NOMBRE Y APELLIDOS]

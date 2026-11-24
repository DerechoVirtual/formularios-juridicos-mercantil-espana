---
name: contrato-servicios-asesoria-juridica-empresa-mer-0599
description: "Contrato de servicios de asesoría jurídica para una empresa. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicios de asesoría jurídica para una empresa

> Formulario **MER-0599** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato mercantil de arrendamiento o prestación de servicios de asesoría jurídica para una empresa.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicios de asesoría jurídica para una empresa» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicios de asesoría jurídica para una empresa” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-servicios-asesoria-juridica-empresa-mer-0599`.
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
- [ ] LOCALIDAD (4 veces)
- [ ] CORREO ELECTRÓNICO (3 veces)
- [ ] DESCRIPCIÓN DEL SERVICIO (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] FECHA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] ACTIVIDAD
- [ ] CALLE
- [ ] COLEGIO
- [ ] DESCRIBIR
- [ ] LUGAR
- [ ] Nº DE COLEGIADO/A
- [ ] OBJETO DEL CONTRATO
- [ ] OTROS DATOS
- [ ] TELÉFONO

## Normas que cita el formulario

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Modelo de contrato mercantil de arrendamiento o prestación de servicios de asesoría jurídica para una empresa.

Notas al pie del formulario original:
(1) Téngase en cuenta la posibilidad de combinarcláusulas híbridas arbitraje/jurisdicción, como las de mediación o las de sumisión a determinada jurisdicción, bien permitiendo la elección a una de las partes, o a la demandante, o delimitando qué tipo de contiendas irían a una u otra vía, como señala elAAP Madrid 18-10-2013, [OTROS DATOS].


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
(Datos de LA EMPRESA)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, LA EMPRESA.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del ASESOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EL ASESOR.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

MANIFIESTAN

I.- Que EL ASESOR es un profesional [OTROS DATOS] dedicado al asesoramiento jurídico así como a la defensa de los intereses de sus clientes ante Tribunales, arbitrajes, etc., con despacho profesional sito en la calle [CALLE] y colegiado con el número [Nº DE COLEGIADO/A] de los pertenecientes al Colegio de Abogados de [COLEGIO].

II.- Que LA EMPRESA se dedica a [ACTIVIDAD] y está interesada en contratar los servicios del ASESOR para que atienda y resuelva los aspectos jurídicos relacionados con el objeto de su negocio, y éste a prestarlos a favor de LA EMPRESA.

En su virtud han decidido celebrar el presente CONTRATO DE ARRENDAMIENTO DE PRESTACIÓN DE SERVICIOS JURÍDICOS, que se sujetará a las siguientes

CLÁUSULAS

Primera.- Objeto del contrato

LA EMPRESA contrata los servicios ofrecidos por EL ASESOR, en su calidad de profesional de la actividad de ASESORAMIENTO LEGAL, quien acepta prestarlos, y consistentes en las siguientes actividades de asesoría jurídica y/o dirección letrada: [OBJETO DEL CONTRATO].

Ejemplo de descripción de servicios:

a) Asesoramiento sobre [DESCRIBIR].
b) Tramitación de [DESCRIPCIÓN DEL SERVICIO].
c) Transacciones [DESCRIPCIÓN DEL SERVICIO].
d) Dirección letrada [DESCRIPCIÓN DEL SERVICIO].

EL ASESOR prestará su asesoramiento con arreglo a la mayor buena fe y diligencia, de acuerdo con su leal saber y entender, y de acuerdo a las siguientes condiciones:

a) Dedicación: será la que estime precisa para el buen fin de su actividad, determinándose en función de las necesidades del servicio, y sin sujeción a horario (o, en su caso, determinarlo).
b) Lugar de prestación del servicio: oficinas de la EMPRESA, sitas en [LOCALIDAD],
c) Informes: el ASESOR elaborará con periodicidad mensual un informe detallado de las actuaciones correspondientes a ese plazo de tiempo, que deberá remitir a LA EMPRESA vía correo electrónico, en las siguientes direcciones [CORREO ELECTRÓNICO],
d) [CORREO ELECTRÓNICO],

Segunda.- Duración

El presente contrato tendrá una duración de SEIS MESES contados a partir del día siguiente a la firma del presente contrato, prorrogándose, a voluntad de las partes, y de común acuerdo, por idénticos períodos sucesivos de tiempo en el supuesto de que ninguno ellas muestren su expreso deseo de no renovarlo con un mes de antelación a la finalización del contrato o de cualquiera de sus prórrogas.

Tercera.- Precio

Mediante este contrato de arrendamiento o prestación de servicios jurídicos, la EMPRESA se compromete a abonar al ASESOR las siguientes cantidades:

a) Pago mensual de [IMPORTE] EUROS, incrementados con el I.V.A. correspondiente en cada momento (o con el tributo que lo sustituyera) que serán abonados, por meses vencidos, del 1 al 7 de cada mes, en la cuenta bancaria que señale EL ASESOR. El primer pago se efectuará el día [FECHA].

En caso de prórroga del contrato, dicho precio se verá incrementado automáticamente el 1 de enero de cada ejercicio económico en la cuantía correspondiente al IPC acumulado del ejercicio anterior.

b) En su caso, parte variable, especificando su modo de determinación.

Cuarta.- Resolución anticipada

No obstante, lo previsto en la Cláusula Segunda, y dado que el presente contrato está basado en la confianza, cualquiera de las partes podrá resolverlo unilateralmente, antes de la fecha pactada para su vencimiento, en cuyo caso, habrá de comunicárselo a la otra parte, al menos con DOS MESES de anticipación.

Si la resolución se produjera por decisión de LA EMPRESA, EL ASESOR tendrá derecho a percibir una indemnización de [IMPORTE] EUROS (en su caso, determinar los parámetros para su cálculo).

Quinta.- Suministro de datos y secreto profesional

LA EMPRESA facilitará al ASESOR cuantos datos, informes o material estime éste necesario para poder llevar a cabo la prestación del servicio para el que se le contrata. La EMPRESA será responsable de la veracidad y calidad de los datos suministrados así como de las consecuencias que la falta de dicha veracidad pueda acarrear.

Por su parte, EL ASESOR se compromete a prestar sus servicios bajo deber de confidencialidad respecto de los datos personales suministrados por LA EMPRESA. Por ello no serán difundidos ni compartidos, salvo que medie consentimiento expreso del cliente.

Sexta.- Protección de datos personales

LA EMPRESA da su permiso para que su dirección postal y electrónica sean tratadas y además, utilizadas para enviar comunicaciones comerciales de promoción y publicidad de los servicios y productos ofrecidos por EL ASESOR. EL ASESOR pone a disposición de sus clientes la dirección de correo electrónico [CORREO ELECTRÓNICO] y el teléfono [TELÉFONO], para que estos revoquen el consentimiento prestado.

EL ASESOR reconoce que la legislación sobre protección de datos personales (Ley Orgánica 3/2018 de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales. A tal efecto, el ASESOR:

a) Únicamente accederá a los datos personales de clientes y demás personas físicas relacionadas con la EMPRESA si tal acceso fuese necesario para cumplir con los servicios objeto del presente contrato.
b) Se compromete a:
— Utilizar los datos de carácter personal a los que tenga acceso única y exclusivamente para cumplir con sus obligaciones contractuales para con la EMPRESA.
— Observar y adoptar cuantas medidas de seguridad sean necesarias para asegurar la confidencialidad, secreto e integridad de los datos de carácter personal a los que tenga acceso, así como a adoptar en el futuro cuantas medidas de seguridad sean exigidas por las leyes y reglamentos destinadas a preservar el secreto, confidencialidad e integridad en el tratamiento automatizado de datos personales.
— A no ceder en ningún caso a terceras personas los datos de carácter personal a los que tenga acceso, ni tan siquiera a efectos de su conservación.

Las obligaciones establecidas para el ASESOR por la presente cláusula serán también de obligado cumplimiento para sus posibles empleados, colaboradores, tanto externos como internos, y subcontratistas, por lo que el ASESOR responderá frente a la EMPRESA si tales obligaciones son incumplidas por tales empleados, colaboradores y subcontratistas.

El incumplimiento por parte del ASESOR de cualesquiera de las obligaciones establecidas en la anterior cláusula de Confidencialidad y en ésta de Tratamiento de Datos de Carácter Personal, generará una indemnización en favor de la EMPRESA de [IMPORTE] euros, sin perjuicio del derecho de la EMPRESA a resarcirse de los perjuicios que le sean causados y que superen la cuantía indicada.

La duración de las obligaciones de confidencialidad establecidas en el presente contrato será indefinida, manteniéndose en vigor con posterioridad a la finalización, por cualquier causa, de la relación entre el ASESOR y la EMPRESA.

Séptima.- Legislación aplicable y jurisdicción

Las partes reconocen que la legislación aplicable al presente contrato, y a todas las relaciones jurídicas dimanantes del mismo, será la española, por expresa aplicación de lo dispuesto en el art.1262 del Código Civil.

Las partes acuerdan someterse para la resolución de cualquier controversia, conflicto o reclamación derivada del presente contrato, a los Tribunales de [LOCALIDAD], por ser éste el lugar de celebración del contrato, con renuncia expresa a cualquier otro fuero que pudiera corresponderles.

LA EMPRESA

EL ASESOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

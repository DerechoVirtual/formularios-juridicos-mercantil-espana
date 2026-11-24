---
name: contrato-renting-bienes-muebles-mer-0625
description: "Contrato de renting de bienes muebles. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de renting de bienes muebles

> Formulario **MER-0625** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Contrato de arrendamiento empresarial en virtud del cual la empresa de renting se obliga a ceder al arrendatario, el uso de un bien mueble ( por ejemplo un automóvil), por tiempo determinado, y contra el pago de un precio, normalmente fraccionado en cuotas, quedando a cargo del arrendador las prestaciones propias del mantenimiento del bien cuyo uso se cede.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de renting de bienes muebles» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de renting de bienes muebles” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-renting-bienes-muebles-mer-0625`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DESCRIPCIÓN DEL BIEN (18 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE ANEXO (2 veces)
- [ ] PLAZO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESTINO DEL BIEN
- [ ] DÍA
- [ ] FECHA
- [ ] FECHAS
- [ ] LUGAR
- [ ] NÚMERO
- [ ] PORCENTAJE

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

Contrato de arrendamiento empresarial en virtud del cual la empresa de renting se obliga a ceder al arrendatario, el uso de un bien mueble ( por ejemplo un automóvil), por tiempo determinado, y contra el pago de un precio, normalmente fraccionado en cuotas, quedando a cargo del arrendador las prestaciones propias del mantenimiento del bien cuyo uso se cede.


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

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EMPRESA DE RENTING.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ARRENDATARIO.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de RENTING y, a tal fin,

MANIFIESTAN

I. Que la empresa de renting es el propietaria de [DESCRIPCIÓN DEL BIEN] designados en el Anexo [Nº DE ANEXO] del presente contrato y se dedica profesionalmente al arrendamiento de los mismos. Para la prestación de sus servicios cuenta con los medios organizativos y técnicos necesarios para su desempeño.

II. Que el arrendatario está interesado:

-en alquilar [DESCRIPCIÓN DEL BIEN] descritos en el Anexo [Nº DE ANEXO], con la opción de compra de los mismos una vez finalizada la vigencia del presente contrato, abonado su valor residual, y
-disfrutar igualmente del servicio de mantenimiento y atención al cliente durante el arrendamiento

III. Que ambas partes han acordado realizar este CONTRATO DE RENTING sometiéndose a las siguientes:

CONDICIONES GENERALES

Primera.- Objeto

La empresa de renting, cede en arrendamiento al arrendatario, que acepta, y toma en arrendamiento, los [DESCRIPCIÓN DEL BIEN] que serán destinados a [DESTINO DEL BIEN].

Segunda.- Recepción y garantía del fabricante

El [DESCRIPCIÓN DEL BIEN] es recibido por el arrendatario en nombre de la empresa de renting., directamente del fabricante. Dicho [DESCRIPCIÓN DEL BIEN] está cubierto única y exclusivamente por la garantía otorgada por el citado fabricante, por lo que no podrá exigirse a la empresa de renting. ninguna garantía o responsabilidad distinta, ni daños o perjuicios o lucro cesante aunque sea por vicios ocultos del [DESCRIPCIÓN DEL BIEN], susceptibles de afectar a su funcionamiento. Para dichos casos la empresa de renting, autoriza al arrendatario a ejercitar frente al fabricante la totalidad de los derechos relacionados con la garantía indicada, excepto la acción de resolución de compraventa.

La recepción de [DESCRIPCIÓN DEL BIEN] por el arrendatario supone su conformidad con las características y estado de éste.

Tercera.- Duración

La duración del arrendamiento se establece por [PLAZO], y se iniciará en la fecha en que [DESCRIPCIÓN DEL BIEN] esté a disposición del Cliente. Para el caso de que el arrendatario esté interesado en la prórroga del presente contrato, deberá cursar solicitud a la compañía de renting con al menos [Nº] días de antelación a la fecha de vencimiento del presente contrato. ..

[ELEGIR UNA OPCIÓN: Cambio de Precio / Continuidad del precio]

Cuarta.- Precio

Durante el periodo de arrendamiento el arrendatario abonará a la empresa de renting una renta mensual de [IMPORTE]

Esta renta incluye el alquiler de [DESCRIPCIÓN DEL BIEN], el mantenimiento en los términos previstos y cuando sea aplicable, el Impuesto Municipal de circulación y la asistencia en carretera y seguro.

El pago se efectuará entre los días [FECHAS] y [DÍA] de cada mes en la cuenta corriente nº [NÚMERO]

que la empresa de renting tiene suscrita con la entidad [DENOMINACIÓN SOCIAL]

[OPCIONAL — incluir si procede]

(Retraso en el pago)

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho la empresa de renting a exigir al arrendatario un interés moratorio del [PORCENTAJE] % respecto de cada uno de los pagos no satisfechos puntualmente.

Quinta.- Fianza

El arrendatario entrega en este acto a la empresa de renting. la cantidad [IMPORTE] euros en concepto de fianza y garantía del fiel cumplimiento de las obligaciones contratadas, sin que en ningún caso pueda aplicarse al pago de cualquiera de las rentas y sin que implique dicha fianza limitación alguna de las responsabilidades del arrendatario, siempre que no exista ninguna obligación pendiente a su cargo y que el se devuelva en perfecto estado.

Este depósito, que no devengará intereses a favor del arrendatario, se le devolverá dentro de los días siguientes a la finalización del arrendamiento, siempre que el arrendatario no tenga ningún pago pendiente con la empresa de renting.

Sexta.- Uso

El [DESCRIPCIÓN DEL BIEN] arrendado deberá ser utilizado por el arrendatario con arreglo a su naturaleza y destino, quedando excluido cualquier uso que entrañe deterioro o riesgo especial para el propio [DESCRIPCIÓN DEL BIEN], quienes lo utilicen o terceros. El arrendatario queda expresamente obligado a observar las instrucciones de uso del [DESCRIPCIÓN DEL BIEN] arrendado en relación a las revisiones, utilización, conservación, reparaciones y, en general, para mantenerlo en buen estado de funcionamiento. Para todo ello el arrendatario debe dirigirse exclusivamente al fabricante, sus servicios, sus establecimientos autorizados, siendo de su cuenta la responsabilidad derivada de intervenciones de personas o servicios de cualquier clase ajenos a los indicados.

El [DESCRIPCIÓN DEL BIEN] sólo podrá ser utilizado por aquellas personas autorizadas que han quedado reseñadas en las condiciones particulares del presente contrato, y que deben estar debidamente autorizadas y con todos los permisos en regla.

En ningún caso la empresa de renting. será responsable del robo, pérdida o destrucción de cualquier objeto que se encuentre [DESCRIPCIÓN DEL BIEN].

El arrendatario se obliga a utilizar el arrendado de conformidad con las leyes, decretos, ordenanzas, reglamentos y otras disposiciones que regulen su uso, y asumirá toda responsabilidad e indemnizará a .la empresa de renting. por la pérdida, gastos, incautación, trabas, confiscación, costes, etc. incluidos honorarios de profesionales, expedientes, o procedimientos incoados por contravención de las leyes o normas reglamentarias infracción de disposiciones, reglamentos u ordenanzas emanadas de la autoridad pública.

[OPCIONAL — incluir si procede]

(Para el caso de que sea renting de vehículos)

El arrendatario garantiza a la empresa de renting. contra los resultados de toda acción de responsabilidad intentada por algún conductor, pasajero u otra persona transportada en el vehículo con autorización o consentimiento de la empresa de renting. A tales efectos, se compromete a no promover o instar acciones judiciales de responsabilidad contra la empresa de renting. por daños causados a tales personas o a su patrimonio, a terceros y otros daños, gastos, incidentes, retrasos y otros hechos resultantes o relacionados con cualquier defecto del vehículo arrendado por avería o accidente sobrevenido al mismo.

[OPCIONAL — incluir si procede]

(Uso en el extranjero)

El vehículo podrá ser utilizado fuera del territorio nacional y dentro de la Unión Europea durante un periodo máximo de [PLAZO]. Cualquier otra utilización en el extranjero requerirá autorización expresa de la Entidad. La cobertura del seguro sólo se extiende a los países de la Unión Europea.

En caso de que un vehículo sea abandonado en el extranjero, el arrendatario será responsable de su repatriación y de todos los gastos incurridos, pudiendo, en su caso, la empresa de renting, repatriar el vehículo por cuenta del Cliente.

[OPCIONAL — incluir si procede]

(Siniestro total)

El siniestro total de vehículo declarado por la compañía de seguros, dará lugar a la extinción del presente contrato, quedando el arrendatario relevado de la obligación de pago de las rentas pendientes de vencimiento, si bien vendrá obligado a abonar a la Entidad el importe del seguro pendiente de facturar.

Ante el evento de una gran reparación no imputable a negligencia del Cliente, la Entidad se reserva el derecho a cancelar anticipadamente el contrato sin penalización alguna para el

Se entenderá por gran reparación aquella cuyo importe supere el % de la suma de las rentas pendientes de vencimiento.

Séptima.- Cesión o subrogación

El arrendatario no podrá transmitir ni ceder sus derechos y obligaciones, ni subarrendar el [DESCRIPCIÓN DEL BIEN] arrendado sin previo permiso escrito de la empresa de renting.

En el caso de que se otorgue la autorización, el arrendatario garantizará de forma conjunta y solidaria con el cesionario las obligaciones asumidas en el presente contrato.

[OPCIONAL — incluir si procede]

(Cuando se especifica a los cesionarios o subrogados)

El sólo podrá ser utilizado por aquellas personas autorizadas reseñadas en las condiciones particulares del presente contrato.

Octava.- Seguros

El arrendatario asume todos los riesgos de daños o pérdidas, total o parcial, del [DESCRIPCIÓN DEL BIEN] arrendado cualquiera que sea la causa a la que corresponda, incluido el caso fortuito.

[ELEGIR UNA OPCIÓN: Contratación por cuenta del arrendatario / Contratación por cuente de la empresa de renting]

Novena.- Mantenimiento

1). La empresa de renting. garantiza cualquier tipo de prestación necesaria para el buen funcionamiento del [DESCRIPCIÓN DEL BIEN] que sea precisa para su mantenimiento, incluyendo el coste de las piezas de recambio y mano de obra. Para ello, el arrendatario se compromete a efectuar el mantenimiento y servicio de cada [DESCRIPCIÓN DEL BIEN] contratado de acuerdo con el programa de mantenimiento previsto por el fabricante y siguiendo las instrucciones expuestas en el manual del mismo. El mantenimiento no abarca los daños que se produzcan como consecuencia de accidente, que serán, en todo caso, cubiertos por la compañía de seguros por lo que en caso de cualquier siniestro, ambas partes se someten al criterio único de los peritos de la citada compañía de seguros.

[OPCIONAL — incluir si procede]

(En caso de automóviles)

El arrendatario atenderá en todo momento que los neumáticos de cada vehículo contratado se encuentren en estado adecuado y cumplan las normas de seguridad previstas en la legislación vigente. En el supuesto de haber contratado la sustitución de neumáticos, vendrá reflejado en el anexo de mantenimiento de cada vehículo el número de neumáticos a sustituir en función de kilometraje contratado, debiendo el arrendatario informar a la empresa de renting de cualquier cambio de neumáticos durante el período contractual.

La empresa de renting. dirigirá al arrendatario, intentando respetar su localidad de residencia, al proveedor más próximo a elección de la misma.

2) Serán por cuenta de la empresa arrendataria. todos los importes facturados por las operaciones de mantenimiento periódicas recomendadas por el fabricante.

3) Cualquier tipo de reparación o mantenimiento, cuyo importe exceda de [IMPORTE] euros se realizará únicamente previa autorización de la empresa de renting.,.

4) En el caso de que el arrendatario haya tenido que adelantar el importe de una intervención no superior a [IMPORTE] euros, la empresa de renting se compromete a reembolsar dicho importe contra presentación de la factura y correspondiente recibo extendido a nombre de la empresa de renting., con indicación del NIF de ésta y del emisor de la factura.

Exclusiones

No se incluyen entre los servicios prestados a través del presente contrato los siguientes:

[ELEGIR UNA OPCIÓN: Solo para renting de automóviles / Si no es renting de automóviles]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

Empresa de Renting

________________________________

Arrendatario

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

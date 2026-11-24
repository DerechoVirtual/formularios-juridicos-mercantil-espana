---
name: transferencia-tecnologia-know-how-secretos-mer-0703
description: "Transferencia de tecnología, Know-How o Secretos empresariales (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Transferencia de tecnología, Know-How o Secretos empresariales (contrato)

> Formulario **MER-0703** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que su titular de un know how, secreto empresarial o tecnología concede a un tercero derechos de explotación (licencia), o bien le cede la titularidad de dicha tecnología (transferencia). En ambos casos, se debe regular la prestación de asistencia técnica por parte del licenciante o transmitente para asegurar una correcta aplicación de la tecnología cedida o licenciada. Asimismo, conviene establecer los mecanismos para determinar la titularidad y, en su caso, el registro, de las mejoras y los desarrollos futuros de dicha tecnología, e incluir en cualquier caso cláusulas de confidencialidad.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Transferencia de tecnología, Know-How o Secretos empresariales (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Transferencia de tecnología, Know-How o Secretos empresariales (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:transferencia-tecnologia-know-how-secretos-mer-0703`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] NOMBRE DE LA PARTE (7 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DESCRIPCIÓN DEL BIEN (4 veces)
- [ ] DNI/NIE (4 veces)
- [ ] ACTIVIDAD (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] PLAZO (3 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] OBJETO DEL CONTRATO (2 veces)
- [ ] PERIODICIDAD (2 veces)
- [ ] ZONA GEOGRÁFICA (2 veces)
- [ ] DESCRIBIR
- [ ] ENTIDAD BANCARIA
- [ ] FECHA
- [ ] IDIOMA
- [ ] LUGAR
- [ ] NOMBRE DEL REGISTRO
- [ ] Nº DE ANEXO
- [ ] Nº DE REGISTRO
- [ ] NÚMERO
- [ ] PARTE QUE ASUME LOS GASTOS
- [ ] TECNOLOGÍA O PROCESO
- [ ] TÍTULOS DE PROPIEDAD INDUSTRIAL
- [ ] ÁMBITO DEL SABER HACER

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

Contrato por el que su titular de un know how, secreto empresarial o tecnología concede a un tercero derechos de explotación (licencia), o bien le cede la titularidad de dicha tecnología (transferencia). En ambos casos, se debe regular la prestación de asistencia técnica por parte del licenciante o transmitente para asegurar una correcta aplicación de la tecnología cedida o licenciada. Asimismo, conviene establecer los mecanismos para determinar la titularidad y, en su caso, el registro, de las mejoras y los desarrollos futuros de dicha tecnología, e incluir en cualquier caso cláusulas de confidencialidad.


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

En lo sucesivo, [ELEGIR: CEDENTE / LICENCIANTE].

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, [ELEGIR: CESIONARIO / LICENCIATARIO].

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de [ELEGIR: Transferencia / Cesión / Licencia de Tecnología / Know how / Secretos Empresariales] y, a tal fin,

MANIFIESTAN

I. Que el [ELEGIR: Cedente / Licenciante] se dedicada a [ACTIVIDAD] con implantación en [ZONA GEOGRÁFICA], desarrollando una importante actividad [ACTIVIDAD], fruto de la cual ha obtenido [TÍTULOS DE PROPIEDAD INDUSTRIAL] que se describen en el Anexo [Nº DE ANEXO] de este contrato, que tiene registrados a su nombre en [NOMBRE DEL REGISTRO], con el número de registro [Nº DE REGISTRO] y fecha que constan en dicho Anexo.

II. El [ELEGIR: Cedente / Licenciante] está en posesión de dicho know-how o secreto empresarial, así como de la información técnica necesaria para la aplicación de [TECNOLOGÍA O PROCESO].

III. El [ELEGIR: Cesionario / Licenciatario] está interesado en que le sea transmitido dicho know-how o Secreto, así como en beneficiarse de la asistencia técnica necesaria para su correcto aprovechamiento.

IV. El [ELEGIR: Cesionario / Licenciatario] y [ELEGIR: Cedente / Licenciante] han alcanzado un acuerdo en virtud del cual este último se compromete a transmitir el know-how mencionado y prestarle la asistencia técnica necesaria para su correcto aprovechamiento, pactando para su ejecución el presente contrato de know-how, transferencia de tecnología y asistencia técnica, con arreglo a las siguientes:

CLAUSULAS

Primera.- Objeto

Por el presente contrato, [ELEGIR: Cedente / Licenciante] se obliga a suministrar al [ELEGIR: Cesionario / Licenciatario] toda información sobre [DESCRIBIR], su experiencia y los métodos que ella misma emplea, incluidos los procedimientos o secretos de [ÁMBITO DEL SABER HACER], de tal manera que pueda realizarlos tras un periodo de adaptación razonable. Y le autoriza para hacer uso de todo ello en las condiciones más adelante especificadas.

Segunda.- Condiciones Generales

El [ELEGIR: Cedente / Licenciante] suministrará al adquirente todas las especificaciones, dibujos y datos técnicos u otros, en el idioma [IDIOMA] que sean necesarios para que el adquirente pueda

2.2. El [ELEGIR: Cedente / Licenciante] y el [ELEGIR: Cesionario / Licenciatario] se intercambiarán periódicamente y al menos una vez al [PERIODICIDAD] toda la información que sea necesaria para la continuación del proyecto de [OBJETO DEL CONTRATO] objeto de [ELEGIR: licencia / transferencia].

2.3. El [ELEGIR: Cedente / Licenciante] y [ELEGIR: Cesionario / Licenciatario] se facilitarán copias de todas las notas de alteraciones.

[OPCIONAL — incluir si procede]

(Comités Técnicos)

2.4. Se creará un comité técnico conjunto, que se reunirá periódicamente con el fin de supervisar el cumplimiento de las obligaciones de las partes.

[OPCIONAL — incluir si procede]

(Recursos)

2.. El [ELEGIR: Cedente / Licenciante] y [ELEGIR: Cesionario / Licenciatario] establecerán un presupuesto de recursos, que tendrá en cuenta las peticiones de prueba y/o los ensayos técnicos de los componentes.

Dicho presupuesto será objeto de revisión [PERIODICIDAD] por parte del [ELEGIR: Cedente / Licenciante] y [ELEGIR: Cesionario / Licenciatario] quien también podrá solicitar ensayos especiales no previstos en el presupuesto.

Los gastos realizados dentro del presupuesto acordado correrán a cargo del [ELEGIR: Cedente / Licenciante] y los que excedan a dicho presupuesto, correrán a cargo [ELEGIR: Cesionario / Licenciatario].

[OPCIONAL — incluir si procede]

(Inspección)

2.. En la medida de lo posible el [ELEGIR: Cedente / Licenciante] dispondrá lo necesario para que su personal técnico visite al adquirente, periódicamente para inspeccionar [DESCRIPCIÓN DEL BIEN] objeto de [ELEGIR: cesión / licencia] y la fabricación de piezas para los mismos. Los gastos de viaje y estancia del personal correrán a cargo de

[OPCIONAL — incluir si procede]

(Formación)

2.. El [ELEGIR: Cedente / Licenciante] sin cargo alguno para el adquirente preparará a los técnicos del [ELEGIR: Cesionario / Licenciatario] en sus fábricas de [LOCALIDAD], pero [NOMBRE DE LA PARTE] deberá facilitar los intérpretes necesarios y correr con todos los gastos de viaje, estancia y demás, así como los sueldos de dichos técnicos e intérpretes.

Tercera.- Licencias y autorizaciones

El Cedente concede al Cesionario todas las licencias y autorizaciones relacionadas con las marcas registradas, nombres comerciales o derechos de diseño de su propiedad.

[OPCIONAL — incluir si procede]

(Cuando se trate de licencia)

El uso de la tecnología transmitida en virtud del presente contrato, queda restringido al ámbito geográfico de [ZONA GEOGRÁFICA], quedando prohibida al Licenciatario la transmisión a terceros de la tecnología transmitida, toda vez que la cesión se hace en exclusiva.

El Licenciatario queda obligado al pago de todas las tasas y derechos que resulten necesarios para el mantenimiento de la tecnología transmitida.

Cuarta.- Secreto

El [ELEGIR: Cesionario / Licenciatario] asume el compromiso de guardar el secreto del know-how que le ha sido cedido, estándole absolutamente prohibido vender o transmitir el mismo a cualquier tercero, ni hacer un uso distinto del mismo al permitido en el presente contrato sin la autorización del [ELEGIR: Cedente / Licenciante]. En concreto, el Licenciatario se obliga a:

1. No proceder a la divulgación o comunicación de la información técnica que le ha sido transmitida con el presente contrato.
2. Restringir, en la medida de lo posible, el acceso a dicha información a sus empleados.
3. Controlar que sus empleados mantengan la presente obligación de secreto.
4. Mantener la obligación de secreto incluso una vez expirado el presente contrato, hasta que la misma pase al dominio público.
5. Impedir cualquier tipo de copia de dicha información por parte de terceros.

Quinta.- Asistencia Técnica

[ELEGIR UNA OPCIÓN: Licencia / Cesión venta]

Sexta.- Precio

El [ELEGIR: Cesionario / Licenciatario] abonará al [ELEGIR: Cedente / Licenciante] por la cesión de [IMPORTE], [IMPORTE] euros; por asistencia técnica durante todo el período de vigencia del contrato [IMPORTE]: euros. El pago del precio se realizará mediante en la cuenta corriente núm. [NÚMERO], en el Banco [ENTIDAD BANCARIA] a nombre del [ELEGIR: Cedente / Licenciante], de la siguiente forma:

- [IMPORTE] euros a la firma del presente contrato, que tiene valor de carta de pago por dicha cantidad a todos los efectos.
- % una vez que la tecnología transmitida haya sido completamente implantada.
- % transcurridos [Nº] meses desde la implantación de la tecnología.
[ELEGIR UNA OPCIÓN: Pago cuando no haya ventas o sean inferiores a cierta cifra / Carencia por el tiempo en que no haya ventas]

[OPCIONAL — incluir si procede]

(Comisiones)

Al margen del precio pactado, el [ELEGIR: Cesionario / Licenciatario] deberá abonar al [ELEGIR: Cedente / Licenciante], durante el plazo de vigencia del contrato, las siguientes comisiones:

— Por la cesión de patentes [IMPORTE].
— Por la asistencia técnica [IMPORTE].
— Por razón de la formación del personal los gastos de desplazamiento y dietas [PARTE QUE ASUME LOS GASTOS]

Para el cumplimiento de estas obligaciones el [ELEGIR: Cesionario / Licenciatario] estará obligado a facilitar al Licenciante los estados de cuentas y toda la documentación contable que éste requiera para efectuar las correspondientes liquidaciones de comisiones.

Séptima.- Garantías

La obligación del [ELEGIR: Cedente / Licenciante] se limita al cumplimiento de su prestación de comunicar al [ELEGIR: Cesionario / Licenciatario] la totalidad de los conocimientos de que dispone para [ACTIVIDAD] y prestación de servicios. El [ELEGIR: Cedente / Licenciante] no asume responsabilidad por los riesgos inherentes a la realización técnica, a cargo del [ELEGIR: Cesionario / Licenciatario]. Éste declara conocer [DESCRIPCIÓN DEL BIEN] y se obliga a fabricar [DESCRIPCIÓN DEL BIEN] y prestar los servicios de forma correcta técnicamente conforme al know how o secreto cedido.

El [ELEGIR: Cedente / Licenciante] no garantiza la explotación comercial del know how cedido. Los riesgos de la misma son a cargo exclusivo del [ELEGIR: Cesionario / Licenciatario].

[OPCIONAL — incluir si procede]

(No se conocen patentes o derechos exclusivos)

[ELEGIR: El Cedente / Licenciante]dice no conocer de la existencia de ninguna patente o derecho exclusivo válido perteneciente a terceros que cubra total o parcialmente [DESCRIPCIÓN DEL BIEN] afectando la posibilidad de su utilización

Octava.- Mejoras

El [ELEGIR: Cedente / Licenciante] se obliga a comunicar al [ELEGIR: Cesionario / Licenciatario] toda modificación que aporte ulteriormente al objeto de know-how, de manera que perfeccione la fabricación o prestación de servicios o reduzca los costes. Esta comunicación será obligatoria desde que la modificación llegue a estar disponible para su uso empresarial y queda sometida a las mismas prescripciones impuestas para el know how inicial. La misma obligación incumbe al [ELEGIR: Cesionario / Licenciatario].

Novena.- Duración y resolución

El presente contrato tendrá una duración de [PLAZO], transcurridos los cuales, podrá ser renovado por iguales periodos, renovándose automáticamente si ninguna de las partes denuncia el mismo con un preaviso mínimo de [PLAZO] antes de su finalización en cualquiera de los siguientes casos:

— Cuando lleve un retraso de más de [Nº] días a partir de la fecha de vencimiento en el pago de cualesquiera cantidades adeudadas este contrato, sin que exista motivo razonable para esta demora.
— Cuando [ELEGIR: Cesionario / Licenciatario] sea culpable de fallos graves en la fabricación, venta o servicio posventa
— Cuando [NOMBRE DE LA PARTE] haya cometido una violación grave de cualquiera de sus obligaciones derivadas de este contrato que hubiera continuado sin ser subsanada durante un plazo de [PLAZO], a contar desde la notificación de la denuncia de este contrato: quedando entendido que en caso de subsanarse esta violación antes del final del plazo de la notificación, ésta quedará sin efecto.
— Cuando [NOMBRE DE LA PARTE] fuere objeto de liquidación, o quedare insolvente o cesare en su negocio.

[OPCIONAL — incluir si procede]

(Persona jurídica)

— Cuando se hubiese llevado a cabo un cambio importante en el accionariado de [NOMBRE DE LA PARTE] del que resulte el control de [NOMBRE DE LA PARTE] por un accionista, o grupo de accionistas que, a juicio de [NOMBRE DE LA PARTE] suponga un perjuicio para sus intereses.

[OPCIONAL — incluir si procede]

Décima.- Cancelación por inviabilidad comercial

Si una vez finalizado el desarrollo de objeto de este contrato, las dos partes apreciaran la inviabilidad comercial de [OBJETO DEL CONTRATO], de común acuerdo negociarían la cancelación de éste.

.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

.- Protección de datos personales

LAS PARTES reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

El incumplimiento de cualquiera de LAS PARTES de las obligaciones establecidas en la en la normativa vigente sobre Tratamiento de Datos de Carácter Personal, generará una indemnización en favor de la contraparte de [IMPORTE] euros.

.- Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE].

.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por la Ley 1/2019, de 20 de febrero, de Secretos Empresariales, y demás disposiciones legales en vigor.

.- Fuero competente

[ELEGIR UNA OPCIÓN: Tribunales / Cláusula de arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

Cedente
Licenciante

Cesionario
Licenciatario

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

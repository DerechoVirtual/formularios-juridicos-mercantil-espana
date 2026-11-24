---
name: contrato-ingenieria-engineering-puesta-marcha-mer-0521
description: "Contrato de ingeniería (engineering) para la puesta en marcha de un establecimiento u obra. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de ingeniería (engineering) para la puesta en marcha de un establecimiento u obra

> Formulario **MER-0521** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que el cliente encarga a una empresa ejecutante la puesta en marcha de un establecimiento, obra, desde la elaboración del proyecto hasta la ejecución del mismo, aportando los materiales, maquinaria, etc. Incluso, la asistencia técnica posterior y, en su caso, la transferencia de tecnología y la cesión de derechos de propiedad industrial.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de ingeniería (engineering) para la puesta en marcha de un establecimiento u obra» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de ingeniería (engineering) para la puesta en marcha de un establecimiento u obra” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-ingenieria-engineering-puesta-marcha-mer-0521`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] DNI/NIE (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] ACTIVIDAD (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº DE ANEXO (3 veces)
- [ ] PLAZO (3 veces)
- [ ] FECHA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] PERIODICIDAD (2 veces)
- [ ] BIENES Y SERVICIOS
- [ ] DESCRIBIR
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE CUENTA (IBAN)
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

Contrato por el que el cliente encarga a una empresa ejecutante la puesta en marcha de un establecimiento, obra, desde la elaboración del proyecto hasta la ejecución del mismo, aportando los materiales, maquinaria, etc. Incluso, la asistencia técnica posterior y, en su caso, la transferencia de tecnología y la cesión de derechos de propiedad industrial.


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

En lo sucesivo, Empresa de ingeniería o ejecutante.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CLIENTE.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de INGENIERÍA O ENGINEERING y, a tal fin,

MANIFIESTAN

I. Que el la empresa de Ingeniería ejecutante, es una sociedad especializada en [ACTIVIDAD].

II. Que el Cliente, es una sociedad cuya actividad principal es [ACTIVIDAD].

III. El Cliente y la empresa de ingeniería ejecutante han alcanzado un acuerdo en virtud del cual la ejecutante se compromete a realizar un completo estudio técnico-económico sobre [DESCRIBIR], aportando los materiales, maquinaria etc pactando para su ejecución el presente contrato, con arreglo a las siguientes:

CLÁUSULAS

Primera.- Objeto

La empresa de ingeniería ejecutante se obliga en virtud del presente contrato a la construcción y puesta en marcha de del Cliente dedicado a [ACTIVIDAD], así como a su mantenimiento posterior en las condiciones que se detallan en el Anexo [Nº DE ANEXO], y con arreglo al presupuesto que se adjunta como Anexo [Nº DE ANEXO], aportando todos los materiales y maquinaria necesarios para la realización de la obra, y obligándose al suministro y transferencia de la tecnología, así como a la cesión de patentes y otros derechos de propiedad industrial que sean necesarios para la ejecución de la obra proyectada y su mantenimiento.

[OPCIONAL — incluir si procede]

(Si se contrata también el proyecto o estudio)

La empresa de ingeniería ejecutante, se compromete a la realización del proyecto y estudio técnico económico de dicha obra, conforme a lo establecido en el pliego de condiciones que se adjunta como Anexo [Nº DE ANEXO], y que presentarán al Cliente para su aprobación previa homologación del proyecto por el Colegio de Ingenieros de [LOCALIDAD], en un plazo máximo de [PLAZO].

Segunda.- Precio

El precio que se establece para las operaciones objeto del presente contrato es de:

[IMPORTE] euros (€) para LA OBRA.

[IMPORTE] euros [ELEGIR: mensuales / trimestrales / semestrales]. (€) para el servicio de mantenimiento, cantidad que se incrementará según las subidas del Índice de Precios al Consumo

[OPCIONAL — incluir si procede]

(Vinculación al presupuesto)

La empresa de ingeniería ejecutante no podrá modificar las obras respecto del presupuesto, salvo acuerdo con el Cliente, con los debidos ajustes presupuestarios.

[OPCIONAL — incluir si procede]

(Garantía)

Del importe de todas y cada una de las certificaciones presentadas el Cliente retendrá un en concepto de garantía que será devuelta por el Cliente a la empresa de ingeniería una vez finalizada la obra.

El pago del precio señalado se efectuará en las siguientes fechas:

• Con respecto a LA OBRA, el cliente entrega a la empresa de ingeniería ejecutante que acepta a cuenta, euros en metálico.
• El resto, euros, se abonarán por el cliente en pagos periódicos [PERIODICIDAD], previa la presentación por la empresa de ingeniería de las correspondientes certificaciones de obra, de [IMPORTE] euros cada uno de ellos, en la cuenta corriente [Nº DE CUENTA (IBAN)].
• En cuanto al servicio de mantenimiento, en caso de aceptación de LA OBRA por el cliente, se efectuará con periodicidad [PERIODICIDAD] los días de cada mes, en la cuenta corriente

[OPCIONAL — incluir si procede]

(Falta de pago)

La falta de pago en los plazos señalados así como el incumplimiento por el cliente de cualquier obligación inherente a este contrato facultará a la empresa de ingeniería a rescindirlo, pactándose a tales efectos un interés de demora del por ciento.

Tercera.- Duración

El plazo máximo para la realización de LA OBRA es de.
meses
años
[NOMBRE Y APELLIDOS], por lo que la empresa de ingeniería ejecutante se compromete a poner a disposición del cliente antes del [FECHA]

En el plazo fijado se incluye la completa puesta en marcha de la planta industrial encargada.

[OPCIONAL — incluir si procede]

(Interrupción por impago de certificación de obra)

El plazo de ejecución de la obra quedará interrumpido en todo caso por el impago de cualquiera de las certificaciones de obra, hasta que la misma no sea abonada.

[OPCIONAL — incluir si procede]

(Penalización por retrasos)

En el caso de retraso en el plazo pactado. El Ejecutante transcurrido un plazo de (de gracia) sin haberla terminado, pagará como penalización al Cliente por cada de retraso un [PORCENTAJE] % del presupuesto. De la penalización se deducirán, en todo caso, las cantidades que tenga pendientes de cobro el Ejecutante

A estos efectos, no se consideran supuestos de causa injustificada aquellos en los que el retraso se produzca por motivo del común acuerdo entre las partes o por fuerza mayor o caso fortuito.

El servicio de mantenimiento a prestar por la empresa de ingeniería se condiciona a la entrega de LA OBRA y a su visto bueno por los responsables del Departamento de del cliente

La duración de la prestación de dicho servicio de mantenimiento, para el caso de aceptación de LA OBRA, se pacta por un período [PLAZO] a contar desde el momento de dicha aceptación, y renovable tácitamente por períodos salvo denuncia expresa de cualquiera de las partes comunicada a la otra por escrito con un preaviso de [ELEGIR: días / meses]

Cuarta.- Visitas

La empresa de ingeniería ejecutante responde de la calidad en la ejecución de la obra objeto de este contrato, así como de la de los materiales que se empleen en la ejecución de la misma.

El Cliente podrá visitar e inspeccionar la obra cuantas veces considere oportuno sin previo aviso.

El derecho de visita no atribuye al Cliente la posibilidad de dar órdenes o directrices a la empresa de ingeniería ejecutante.

Quinta.- Seguros

La empresa de ingeniería ejecutante está obligada a concertar por todo el tiempo que dure la obra un seguro que cubra todos los posibles riesgos de la construcción hasta el importe del presupuesto de la misma.

Sexta.- Subcontratación

La empresa de ingeniería ejecutante bajo su exclusiva responsabilidad podrá llevar a cabo subcontrataciones para la ejecución de la obra. Por ejemplo, podrá contratar con terceros la adquisición de títulos de propiedad industrial, equipos, suministros y en general [BIENES Y SERVICIOS].

Séptima.- Confidencialidad

Tanto la empresa de ingeniería ejecutante como el cliente se comprometen a no divulgar la información y documentación confidencial referente a la otra parte de la que hayan tenido conocimiento por razón de la ejecución del presente contrato, salvo las indispensables para su cumplimiento, y a mantenerla en secreto, incluso después de la finalización del mismo.

Ambas partes acuerdan tomar las medidas necesarias respecto a su personal e incluso terceros que puedan tener acceso a dichas información y documentación, a fin de garantizar la confidencialidad objeto de esta cláusula.

Octava.- Protección de datos

La empresa de ingeniería ejecutante reconoce que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular. A tal efecto, la empresa de ingeniería:

a) Únicamente accederá a los datos personales de clientes y demás personas físicas relacionadas con el cliente si tal acceso fuese necesario para cumplir con los servicios objeto del presente contrato.
b) Se compromete a:
- Utilizar los datos de carácter personal a los que tenga acceso única y exclusivamente para cumplir con sus obligaciones contractuales para con el cliente.
- Observar y adoptar cuantas medidas de seguridad sean necesarias para asegurar la confidencialidad, secreto e integridad de los datos de carácter personal a los que tenga acceso, así como a adoptar en el futuro cuantas medidas de seguridad sean exigidas por las leyes y reglamentos destinadas a preservar el secreto, confidencialidad e integridad en el tratamiento automatizado de datos personales.
- A no ceder en ningún caso a terceras personas los datos de carácter personal a los que tenga acceso, ni tan siquiera a efectos de su conservación.

Las obligaciones establecidas para la empresa de ingeniería por la presente cláusula serán también de obligado cumplimiento para sus posibles empleados, colaboradores, tanto externos como internos, y subcontratistas, por lo que la empresa de ingeniería responderá frente al cliente si tales obligaciones son incumplidas

[OPCIONAL — incluir si procede]

(Incumplimientos e indemnizaciones)

El incumplimiento por parte de la empresa de ingeniería de cualesquiera de las obligaciones establecidas en la anterior cláusula de Confidencialidad y en ésta de Tratamiento de Datos de Carácter Personal, generará una indemnización en favor del cliente de [IMPORTE] euros, sin perjuicio del derecho del cliente a resarcirse de los perjuicios que le sean causados y que superen la cuantía indicada.

La duración de las obligaciones de confidencialidad establecidas en el presente contrato será indefinida, manteniéndose en vigor con posterioridad a la finalización, por cualquier causa, de la relación entre la empresa de ingeniería y el cliente.

Novena.- Terminación y resolución

Son causas de terminación y resolución del presente contrato:

- Su terminación normal, ya sea por:
a) haber llegado el contrato a su vencimiento,
b) haberse cumplido y ejecutado la prestación a la que ambas partes se encuentran obligadas,
c) acuerdo mutuo de las partes.
- Por incumplimiento de cualquiera de las partes de alguna de las cláusulas del presente contrato, sin que dicho incumplimiento fuera subsanado dentro de los [PLAZO] siguientes a la notificación por escrito efectuada por la otra parte solicitando la subsanación del incumplimiento.

Décima.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Decimoprimera.- Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE].

Decimosegunda.- Elevación a escritura pública

El presente contrato se elevará a público a solicitud de cualquiera de las partes, siendo los gastos del notario pagados por la parte que lo solicite.

Decimotercera.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones del Código de Comercio, Leyes especiales, los usos y costumbres mercantiles y, en su defecto, por lo establecido en el Código Civil.

Decimocuarta.- Fuero competente

[ELEGIR UNA OPCIÓN: Si se pacta someterse a tribunales / Si se pacta someterse a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

EMPRESA DE INGENIERÍA EJECUTANTE

________________________________

EL CLIENTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

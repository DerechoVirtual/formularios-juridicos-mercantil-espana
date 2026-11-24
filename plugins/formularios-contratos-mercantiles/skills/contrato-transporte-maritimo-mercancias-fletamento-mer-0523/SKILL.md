---
name: contrato-transporte-maritimo-mercancias-fletamento-mer-0523
description: "Contrato de transporte marítimo de mercancías por fletamento o conocimiento de embarque. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de transporte marítimo de mercancías por fletamento o conocimiento de embarque

> Formulario **MER-0523** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato de transporte de mercancías bajo las modalidades de fletamento y/o conocimiento de embarque por el que el porteador se obliga, a cambio del pago de una contraprestación, a transportar por mar mercancías y entregarlas al destinatario en el puerto o lugar de destino nacional o internacional.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de transporte marítimo de mercancías por fletamento o conocimiento de embarque» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de transporte marítimo de mercancías por fletamento o conocimiento de embarque” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-transporte-maritimo-mercancias-fletamento-mer-0523`.
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
- [ ] LOCALIDAD (4 veces)
- [ ] Nº (4 veces)
- [ ] FECHA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] PLAZO (2 veces)
- [ ] BANDERA
- [ ] DATOS DE PERSONA ADICIONAL
- [ ] DATOS REGISTRALES
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DE LA MERCANCÍA
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] ESTADO DEL BUQUE
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MATRÍCULA
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE DEL BUQUE
- [ ] Nº DE ANEXO
- [ ] OTROS DATOS
- [ ] PAÍS
- [ ] PUERTO DE DESTINO
- [ ] RIESGOS CUBIERTOS
- [ ] SUCURSAL

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

Contrato de transporte de mercancías bajo las modalidades de fletamento y/o conocimiento de embarque por el que el porteador se obliga, a cambio del pago de una contraprestación, a transportar por mar mercancías y entregarlas al destinatario en el puerto o lugar de destino nacional o internacional.


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
(Datos de FLETADOR/TRANSITARIO/PORTEADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, [ELEGIR: FLETADOR / TRANSITARIO / PORTEADOR].

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del FLETANTE/CARGADOR/CLIENTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, [ELEGIR: FLETANTE / CARGADOR / CLIENTE].

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de TRANSPORTE MARÍTIMO DE MERCANCÍAS y, a tal fin,

MANIFIESTAN

I.- Que el [ELEGIR: Fletador / Transitario / Porteador] es propietario del buque [NOMBRE DEL BUQUE] matrícula [MATRÍCULA] con bandera de [BANDERA], estado de [ESTADO DEL BUQUE], registrado en [DATOS REGISTRALES], buque de carga general y con las siguientes características: [DESCRIPCIÓN DEL BIEN].

II.- Que el [ELEGIR: Fletante / Cargador / Cliente] está interesado en celebrar un contrato de transporte marítimo de mercancías para transportar [DESCRIPCIÓN DE LA MERCANCÍA] al puerto de [PUERTO DE DESTINO].

III.- Que ambas partes de común acuerdo llevan a efecto el presenten contrato con arreglo a las siguientes:

CLÁUSULAS

Primera.- Objeto

[ELEGIR UNA OPCIÓN: Transporte nacional o internacional de mercancías con conocimiento de embarque / Fletamento]

Segunda.- Duración

El presente contrato tendrá una duración de [PLAZO].

El [ELEGIR: Fletador / Transitario / Porteador] podrá prorrogar el plazo de fletamento notificándoselo al [ELEGIR: Fletante / Cargador / Cliente] con [Nº] días de antelación, devengando la misma contraprestación que se abonará al contado y por adelantado.

Tercera.- Contraprestación

En contraprestación a sus obligaciones [ELEGIR: Fletador / Transitario / Porteador] percibirá una remuneración de [IMPORTE] euros (€).

Los gastos adicionales que se produzcan como consecuencia de hechos o circunstancias posteriores a la fecha de contratación o, en su caso, a la fecha de emisión de expedición, serán de cuenta y cargo del [ELEGIR: Fletante / Cargador / Cliente], siempre que estén debidamente justificados y no se deba a culpa o negligencia del [ELEGIR: Fletador / Transitario / Porteador].

El pago del % del precio se efectuará el día [FECHA] en la cuenta corriente núm. [Nº] que [ELEGIR: Fletador / Transitario / Porteador] tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL].

El % restante del precio del transporte lo recibirá [ELEGIR: Fletador / Transitario / Porteador] en el plazo de [PLAZO] desde el día siguiente a la entrega de las mercancías en el lugar de destino con aceptación por el destinatario.

[OPCIONAL — incluir si procede]

(Retrasos)

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho al [ELEGIR: Fletador / Transitario / Porteador] a exigir al [ELEGIR: Fletante / Cargador / Cliente] un interés moratorio del % respecto de cada uno de los pagos no satisfechos puntualmente.

[OPCIONAL — incluir si procede]

(Precio del combustible)

EL [ELEGIR: Fletador / Transitario / Porteador] podrá incrementar en su factura el precio inicialmente pactado en cuantía equivalente a la diferencia existente entre el precio que tenía la gasolina el día de celebración del contrato y el que tenga en el momento de realizarse el transporte, multiplicada por el número de litros utilizados en su realización.

Cuarta.- Conocimiento de embarque

Es preceptiva la utilización del conocimiento de embarque en cualquiera de sus modalidades

[OPCIONAL — incluir si procede]

B/L Recibido para el Embarque: implica que la mercancía ha sido recibida por el transporte en la fecha indicada, pero no se ha embarcado. Normalmente se utiliza en las entregas con transporte multimodal, confirmando la fecha en que el contenedor ha llegado a la terminal del primer transportista. No es recomendable en operaciones ligadas con la forma de crédito documentario pues el importador no solicita este documento ya que no le sirve para confirmar el embarque de la mercancía.

[OPCIONAL — incluir si procede]

B/L Nominativo: emitido a nombre de una persona o empresa determinada, que podrá recoger la mercancía previa identificación y presentación de [OTROS DATOS], al menos, un original del B/L. En caso de tramitación por parte del transitario o agente designado para la recogida de la mercancía debe ser entregado a éste endosado (firmado en su reverso por quien esta nominativo) a efectos de cesión de derechos para dicha operativa, si bien no le confiere cesión para su negociación, por lo que en operativas de compraventa en tránsito no resulta operativo, al no poder negociarse libremente.

[OPCIONAL — incluir si procede]

B/L a la orden: en este modelo el propietario de la mercancía es el poseedor de la documentación original que puede transmitir la propiedad a otro mediante endoso convirtiéndolo en nominativo o simplemente endosando el documento como "al portador". Este es uno de tipos de conocimiento de embarque más utilizados por los créditos documentarios con intervención bancaria en el que es el banco quien aparece como consignatario de la mercancía, endosando a posteriori dicha documentación a su cliente, que es el importador.

[OPCIONAL — incluir si procede]

B/L a la orden: en este modelo el propietario de la mercancía es el poseedor de la documentación original que puede transmitir la propiedad a otro mediante endoso convirtiéndolo en nominativo o simplemente endosando el documento como "al portador". Este es uno de tipos de conocimiento de embarque más utilizados por los créditos documentarios con intervención bancaria en el que es el banco quien aparece como consignatario de la mercancía, endosando a posteriori dicha documentación a su cliente, que es el importador.

[OPCIONAL — incluir si procede]

B/L al portador: se emite como "al portador", es decir, sin identificar al propietario de la mercancía que será el que posea la documentación original. No es muy aconsejable ya que la pérdida del documento puede ocasionar graves problemas por lo que importadores y bancos no aceptan entregas con este tipo de B/L, que no es común en operaciones internacionales.

[OPCIONAL — incluir si procede]

B/L House: es un documento emitido por el agente transitario y negociable. Aceptable en operaciones bancarias. Normalmente se acepta en envíos en los que bien el exportador o el importador asumen toda la operativa de la operación internacional.

Quinta.- Recogida, itinerario y entrega de la mercancía

[ELEGIR UNA OPCIÓN: Carga y descarga. Porteador / Carga y descarga. Cargador]

[OPCIONAL — incluir si procede]

(Embalaje y señalización)

Las mercancías deberán ser entregadas al porteador convenientemente acondicionadas y embaladas, y señalizadas mediante marcas o inscripciones que avisen del riesgo que su manipulación pueda entrañar para las personas o para las propias mercancías, de tal forma que éstas puedan soportar sin menoscabo su transporte en condiciones normales y no constituyan causa de peligro para el porteador o su personal dependiente, las demás mercancías transportadas, el vehículo o los terceros.

El cargador, estará obligado a informar previamente al porteador acerca de la naturaleza peligrosa de las mercancías objeto de transporte, almacenaje o manipulación, así como de las precauciones excepcionales que, en su caso, deban adoptarse. En caso de omisión o insuficiente información, el cargador será responsable de los daños y gastos producidos.

[OPCIONAL — incluir si procede]

(Itinerario)
[ELEGIR UNA OPCIÓN: Determinado por el porteador / Determinado por el remitente]

[OPCIONAL — incluir si procede]

(Reclamaciones)

En el momento de la entrega de las mercancías, los destinatarios deberán verificar las condiciones en que se encuentran las mismas, así como que la cantidad, número y peso de los bultos se corresponden con los datos consignados en la documentación referente al transporte, debiendo informar inmediatamente al porteador sobre cualquier defecto o pérdida aparente en cualquier pieza.

En el caso de que alguna irregularidad o pérdida no sea observada inmediatamente por el receptor de las mercancías, éste deberá hacer constar sus reservas por escrito dentro de las [Nº] horas siguientes a la entrega de las mercancías o en los términos y condiciones señalados en el conocimientos de embarque etc., o en su defecto, en los términos y condiciones establecidos en los Convenios Internacionales que regulan la modalidad de transporte de que se trate. De lo contrario perderá el derecho a hacer cualquier reclamación contra el porteador.

[OPCIONAL — incluir si procede]

(Contrato de fletamento)

Sexta.- Entrega del Buque y tripulación

[ELEGIR UNA OPCIÓN: En el puerto de origen / En el puerto de destino]

[OPCIONAL — incluir si procede]

(Tripulación)

El capitán, D. [NOMBRE Y APELLIDOS], así como la tripulación del buque estarán sujetos a las órdenes del fletador, y cumplirán la normativa nacional de la marina mercante de [PAÍS].

.- Seguros

Fletador [ELEGIR: Transitario / Porteador] contratará un seguro que resulte satisfactorio para [ELEGIR: Fletante / Cargador / Cliente] y proporcionará a éste, a su solicitud, pruebas de la existencia de dicho seguro. La cobertura incluirá, entre otros [RIESGOS CUBIERTOS]. El [ELEGIR: Fletador / Transitario / Porteador] informará con prontitud al [ELEGIR: Fletante / Cargador / Cliente] de cualquier peligro asegurable y cualquier suceso extraordinario que afecten a la mercancía y al buque fletado, tomando las medidas necesarias para la resolución del problema y la satisfacción de las reclamaciones.

.- Subcontratación

El transporte de las mercancías deberá ser realizado por el porteador con los medios personales y materiales integrantes de su propia organización empresarial.

No obstante, cuando el transporte se lleve a cabo por el porteador mediante la colaboración de otro porteador que cuente con el personal y las nave adecuada para realizarlo, no quedará desvirtuada su condición de porteador único frente al cargador.

En todo caso, la nave utilizada habrán de reunir las condiciones adecuadas para el transporte del envío de que se trate, así como para el acceso y circulación por los lugares en que haya de realizarse su carga y descarga, cuando tales condiciones le hubiesen sido previamente comunicadas por el cargador.

.- Retención

El porteador autoriza al cargador a retener hasta el % del precio del porte hasta que se demuestre que las mercancías han sido recibidas en condiciones óptimas para su utilización o, en su caso, hasta que el porteador haya respondido de los daños y perjuicios irrogados al cargador.

[OPCIONAL — incluir si procede]

(Fletamento)

El fletante autoriza al fletador a retener hasta el % del flete hasta que los gastos y responsabilidades que son de cuenta y cargo del fletante no hayan sido íntegramente satisfechos.

[OPCIONAL — incluir si procede]

(Transporte internacional)

.- Trámites Aduaneros

Corresponderá al porteador el cumplimiento de las formalidades aduaneras durante el transporte conforme a las instrucciones del cargador que se recogen en [Nº DE ANEXO], siendo los gastos y derechos aduaneros devengados con tal motivo de cuenta y cargo de

.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[DATOS DE PERSONA ADICIONAL]

.- Protección de datos personales

Las partes reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

.- Gastos e Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE].

.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones de la Ley 15/2009, de 11 de noviembre, del contrato de transporte terrestre de mercancías y demás disposiciones concordantes, leyes especiales y usos mercantiles que le sean aplicables.

.- Fuero competente

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Tribunales de [LOCALIDAD].

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD].

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

FLETADOR
TRANSITARIO
PORTEADOR

FLETANTE
CARGADOR
CLIENTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

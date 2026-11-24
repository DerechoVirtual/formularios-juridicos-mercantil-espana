---
name: contrato-suministro-alimentos-servicio-catering-mer-0603
description: "Contrato de suministro de alimentos y servicio de catering. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de suministro de alimentos y servicio de catering

> Formulario **MER-0603** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que el suministrador se obliga a entregar al suministrado los bienes o alimentos objeto del contrato con una determinada periodicidad y durante un plazo determinado de tiempo. Se incluyen los derechos y obligaciones de cada una de las partes, así como las condiciones y estipulaciones necesarias para el cumplimiento del mismo.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de suministro de alimentos y servicio de catering» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de suministro de alimentos y servicio de catering” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-suministro-alimentos-servicio-catering-mer-0603`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] OTROS DATOS (7 veces)
- [ ] TIPO DE PRODUCTOS (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] Nº (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] DIRECCIÓN (2 veces)
- [ ] FECHA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] REFERENCIA DEL PRODUCTO (2 veces)
- [ ] ACTIVIDAD
- [ ] CAUSA
- [ ] CLASE DE PRODUCTO
- [ ] DENOMINACIÓN SOCIAL
- [ ] HORA
- [ ] LUGAR
- [ ] MEDIO DE COMUNICACIÓN
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE ANEXO
- [ ] NÚMERO
- [ ] PLAZO
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

Contrato por el que el suministrador se obliga a entregar al suministrado los bienes o alimentos objeto del contrato con una determinada periodicidad y durante un plazo determinado de tiempo. Se incluyen los derechos y obligaciones de cada una de las partes, así como las condiciones y estipulaciones necesarias para el cumplimiento del mismo.


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
(Datos de SUMINISTRADOR O EMPRESA DE CATERING)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, [ELEGIR: SUMINISTRADOR / EMPRESA DE CATERING].

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del SUMINISTRADO)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, SUMINISTRADO.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de [ELEGIR: Suministro / Catering] y, a tal fin,

EXPONEN

I. Que, se dedica a la fabricación de [TIPO DE PRODUCTOS] y [TIPO DE PRODUCTOS].

[OPCIONAL — incluir si procede]

(Catering)

I. Que la empresa de catering tiene como objeto social el suministro de comidas cocinadas y/o precocinadas para el servicio de [OTROS DATOS], etc..

II. Que, desea recibir entregas sucesivas y periódicas de los siguientes productos [TIPO DE PRODUCTOS].

[OPCIONAL — incluir si procede]

(Descripción de los bienes)

Cantidad [IMPORTE].

Clase [CLASE DE PRODUCTO].

Referencia [REFERENCIA DEL PRODUCTO].

Referencia [REFERENCIA DEL PRODUCTO].

[OPCIONAL — incluir si procede]

II. Que el suministrado, por su parte, se dedica a [ACTIVIDAD] del [OTROS DATOS], necesitando para su proceso los [TIPO DE PRODUCTOS] elaborados por la empresa de catering, por lo que tiene interés en que ésta le suministre dichos [TIPO DE PRODUCTOS].

III. Que ambas partes convienen formalizar un contrato de [ELEGIR: suministro / catering] sobre los indicados productos o mercancías, en base a las siguientes:

CLÁUSULAS

Primera.- Objeto

Que la entidad el suministrador se obliga mediante el presente contrato a abastecer al suministrado, los productos indicados en el expositivo II, de acuerdo con los pactos y condiciones aquí detalladas, y con arreglo a lo dispuesto en el Código de Comercio, usos mercantiles y legislación complementaria aplicable.

[OPCIONAL — incluir si procede]

La empresa de catering se compromete a suministrar. el servicio de alimentación para el suministrado en las condiciones y pactos establecidos en el presente contrato.

Diariamente el suministrado informará por [MEDIO DE COMUNICACIÓN] a la empresa de catering antes de las horas de cuántos son los menús que se precisan para ese día según el número de [OTROS DATOS].

La empresa de catering se compromete a utilizar ingredientes de primera calidad y en perfecto estado de conservación para la elaboración de los menús. Igualmente, se compromete a no utilizar en ningún caso aditivos, conservantes o colorantes no aptos para el consumo humano. En este sentido, la empresa de catering responderá civil e incluso penalmente si vulnera las normativa vigente relativa a los servicios alimentarios.

Segunda.- Precio

Los precios, durante el primer año de vigencia de este contrato de cada uno de los tipos de [TIPO DE PRODUCTOS] se ajustarán a los que figuran en el anexo I que las partes suscriben y que desde este momento forma parte integrante del mismo.

El precio comprende [OTROS DATOS], (a excepción de los portes), cuantas actividades sean precisas para el abastecimiento de [OTROS DATOS] en [LOCALIDAD].

[ELEGIR UNA OPCIÓN: Con suspensión del suministro y aceptación expresa / Simple comunicación]

[OPCIONAL — incluir si procede]

Los precios a aplicar para el suministro alimentario son [IMPORTE] euros por menú suministrado y transportado más el impuesto correspondiente.

Tercera.- Forma de pago

El suministrado se obliga a realizar el pagos de los bienes suministrados el día [FECHA]. de cada mes, contra factura recibida, y efectuando los abonos en la cuenta corriente nº [NÚMERO]. que el suministrador tiene contratada en la entidad [DENOMINACIÓN SOCIAL], sucursal de [LOCALIDAD].

Las facturas deberán detallar el número de [TIPO DE PRODUCTOS]. suministrados, la fecha de la entrega, el precio de cada [OTROS DATOS] el precio total [IMPORTE], y se expedirá por duplicado ejemplar.

[OPCIONAL — incluir si procede]

(Retrasos)

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho al suministrador a exigir al suministrado un interés del [PORCENTAJE] % respecto de cada uno de los pagos no satisfechos puntualmente.

Cuarta.- Duración

El presente contrato tendrá una duración de [PLAZO] desde la fecha de su celebración, quedando automáticamente prorrogado por anualidades sucesivas en el caso de que ninguna de las partes proceda a la denuncia del mismo con al menos [Nº] días naturales de antelación a la fecha de su vencimiento.

Quinta.- Entrega

El Suministrador se compromete a abastecer al Suministrado en la periodicidad y cuantía que el mismo le requiera, por cualquier medio que deje constancia de su recepción, comprometiéndose a la entrega en el plazo máximo de [Nº] días naturales desde aquel en el que se reciba la solicitud.

Los Productos se entregarán en las Instalaciones [DIRECCIÓN].

El Suministrado se compromete a aceptar las mercancías una vez hayan sido entregadas si coinciden con las calidades, forma y tamaño descritos en [Nº DE ANEXO].

[OPCIONAL — incluir si procede]

La empresa de catering se compromete a abastecer al Suministrado en [DIRECCIÓN] diariamente, entre las [HORA] y las [Nº] horas, las raciones individualizadas de comidas correspondientes a los menús pactados que se recogen en el Anexo I de este contrato. Dichos menús comprenden un primer plato, un segundo plato y postre. Las citadas raciones individualizadas irán envasadas al vacío en recipiente adecuado de tal forma que mantengan la temperatura usual en cada caso para su ingestión.

La empresa de catering se compromete a transportar diariamente las comidas contratadas y a depositarlas en los comedores del suministrado en el horario señalado en la Cláusula Segunda del presente contrato

[ELEGIR UNA OPCIÓN: No recepción y sustitución / Saneamiento y sustitución]

En el caso de discrepancia entre las partes sobre el estado y/o calidad de los bienes, las partes se someten a la decisión última de D./Dña. [NOMBRE Y APELLIDOS] experto en

[OPCIONAL — incluir si procede]

(Caso fortuito u fuerza mayor)

El suministrador no responderá frente al suministrado ni ninguna otra persona que pudiera resultar afectada, por la pérdida o deterioro total o parcial de las mercaderías suministradas, ni por el retraso en la entrega de la mismas, siempre que esta pérdida o retraso en la entrega sea motivada por circunstancias que no pudieron preverse o que resulten inevitables, es decir, caso fortuito o fuerza mayor. En estos supuestos el suministrador quedará exento de las consecuencias de su incumplimiento, así como del pago de daños y perjuicios.

Sexta. Inspección

[ELEGIR: El suministrador / la empresa de catering]autoriza la inspección de sus instalaciones en cualquier momento por parte del SUMINISTRADO y a la designación por éste de una persona que pruebe los nuevos menús y preste su conformidad a los mismos.

[OPCIONAL — incluir si procede]

.- Almacenamiento

El suministrado garantiza el almacenamiento del producto en sus Instalaciones, con indicación clara de su pertenencia al suministrador. El Producto no se almacenará en lugar distinto de las Instalaciones, a menos que el suministrador lo autorice previamente por escrito.

El suministrado garantiza que las Instalaciones estarán en todo momento debidamente acondicionadas para la recepción y almacenamiento del Producto, de modo que pueda asegurarse la integridad del mismo.

El suministrado se hará cargo de los costes de almacenamiento del Producto.

El suministrado garantiza por el presente contrato que cumplirá con todas las licencias, y permisos exigidos por la normativa vigente.

[OPCIONAL — incluir si procede]

.- Exclusividad

[OPCIONAL — incluir si procede]

(Del suministrador)

Durante la vigencia del presente contrato [NOMBRE DE LA PARTE] se obliga a no abastecer, suministrar o comercializar sus productos a aquellas personas, físicas o jurídicas, que fueran competidoras directas del suministrado en salvo autorización expresa de esta última..

[OPCIONAL — incluir si procede]

(Del suministrado)

El presente contrato tiene carácter de exclusiva, por lo que el Suministrado se compromete mientras se mantenga la vigencia del mismo a no adquirir de ninguna otra empresa o profesional los bienes que constituyen el objeto del presente contrato de suministro.

[OPCIONAL — incluir si procede]

(Información)

Además, a efectos de logística, deberá facilitar al suministrador relaciones trimestrales, debidamente firmadas de los movimientos de venta en unidades y valores, así como del stock de los productos aún existentes en sus dependencias.

[OPCIONAL — incluir si procede]

.- Reserva de dominio

La propiedad de los bienes suministrados no pasará al suministrado hasta la totalidad de su pago. En el período comprendido entre la entrega y el abono el suministrado tendrá el Producto en calidad de comodatario del suministrador.

.- Seguros

El suministrado contratará un seguro cuya cobertura incluirá, entre otros aspectos, los daños provocados por [CAUSA]

.- Resolución

El Contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.
2. Por acuerdo de las Partes por escrito.

[OTROS DATOS]

.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[NOMBRE Y APELLIDOS]

.- Impuestos y gastos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [ELEGIR: suministrador / suministrado].

.- Protección de datos personales

Las partes reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización de su titular

.- Naturaleza del contrato

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones del Código de Comercio, leyes especiales y usos mercantiles, y en su defecto por lo previsto en el Código Civil.

.- Fuero competente

[ELEGIR UNA OPCIÓN: Si pactan someterse a tribunales / Si pactan someterse a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

SUMINISTRADOR

SUMINISTRADO

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

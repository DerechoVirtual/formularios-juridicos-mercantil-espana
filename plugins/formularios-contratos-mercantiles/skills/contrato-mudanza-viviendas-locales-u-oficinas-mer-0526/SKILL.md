---
name: contrato-mudanza-viviendas-locales-u-oficinas-mer-0526
description: "Contrato de mudanza de viviendas, locales u oficinas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de mudanza de viviendas, locales u oficinas

> Formulario **MER-0526** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que el transportista se encarga del traslado, entre viviendas, locales, u oficinas, de mobiliario, sus complementos, ajuar doméstico y otros enseres incluyendo todas o parte de las operaciones de preparación, montaje y desmontaje, embalaje y demás actividades que requiere este tipo especial de transporte a cambio de una contraprestación. El servicio no se entenderá cumplido hasta la entrega de los muebles y enseres objeto de la mudanza en el domicilio de destino, en las condiciones pactadas.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de mudanza de viviendas, locales u oficinas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de mudanza de viviendas, locales u oficinas” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-mudanza-viviendas-locales-u-oficinas-mer-0526`.
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
- [ ] IMPORTE (3 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] DIRECCIÓN
- [ ] FECHA
- [ ] LUGAR
- [ ] Nº DE ANEXO
- [ ] Nº DE DÍAS
- [ ] OTROS DATOS
- [ ] PLAZO
- [ ] PORCENTAJE

## Normas que cita el formulario

- art. 1.101 Código Civil

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

Contrato por el que el transportista se encarga del traslado, entre viviendas, locales, u oficinas, de mobiliario, sus complementos, ajuar doméstico y otros enseres incluyendo todas o parte de las operaciones de preparación, montaje y desmontaje, embalaje y demás actividades que requiere este tipo especial de transporte a cambio de una contraprestación. El servicio no se entenderá cumplido hasta la entrega de los muebles y enseres objeto de la mudanza en el domicilio de destino, en las condiciones pactadas.


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
(Datos del TRANSPORTISTA)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, TRANSPORTISTA.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del CLIENTE)

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

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de MUDANZA y, a tal fin,

MANIFIESTAN

I. Que el cliente desea realizar una mudanza de muebles y enseres.

Desde: Domicilio de recogida: [DIRECCIÓN].

Hasta: Domicilio de entrega:.

II. Que la empresa transportista tiene interés en realizar dicha mudanza, por lo que ambas partes acuerdan el presente contrato, con arreglo a las siguientes

CLÁUSULAS

Primera.- Objeto

El presente acuerdo se refiere al traslado del mobiliario descrito en el Inventario incluido como Anexo [Nº DE ANEXO] del presente contrato bajo la siguiente modalidad:

[OPCIONAL — incluir si procede]

(Carga, descarga, desmontaje y montaje a cargo del transportista)

Carga, descarga, desmontaje, montaje de muebles de tornillo, embalajes, cristalería, menaje diverso, ropas, libros, legajos, carpetas, discos, adornos y/u otros objetos frágiles, utilizando materiales de embalaje y envases
recuperables propiedad del transportista y sin mediar intervención de oficios ajenos
no recuperables

[OPCIONAL — incluir si procede]

(Desmontaje y montaje a cargo del cliente)

Desmontaje y montaje, tanto en origen como en destino por cuenta del cliente [ELEGIR: utilizando materiales y envases de la empresa de mudanzas / siendo a su cargo los materiales, cubiertos y toda clase de medios y envases utilizados] El transportista llevará a cabo la carga, transporte, descarga y entrega de los bultos y objetos desde y hasta el interior del domicilio o local de recogida y entrega.

Segunda.- Precio y forma de pago

En contraprestación a sus obligaciones el transportista percibirá del cliente una remuneración de [IMPORTE] euros, conforme al presupuesto inicialmente facilitado, de las que percibe el % en el presente acto, en concepto de anticipo a cuenta, que acepta, sirviendo el presente documento de carta de pago.

El % restante del precio del transporte lo recibirá el transportista en el plazo de [PLAZO] desde la entrega del mobiliario en el lugar pactado.

El pago no implicará la conformidad del cliente con el servicio prestado, quedando siempre a salvo la posibilidad de reclamar contra la empresa transportista por la deficiente prestación del servicio.

El transportista entregará al cliente, recibo de las cantidades percibidas, y finalizada la mudanza emitirá factura, en los términos previstos en el Real Decreto 1619/2012, de 30 noviembre por el que se aprueba el Reglamento por el que se regulan las obligaciones de facturación.

Tercera.- Inventario

[ELEGIR UNA OPCIÓN: Hecho por el transportista / Hecho por el cliente]

[OPCIONAL — incluir si procede]

(Indicación de valores)

El cliente hará una declaración del valor global del mobiliario y enseres, así como una declaración detallada de los objetos que puedan tener un valor particular, en la que deben identificarse claramente los bienes de carácter artístico, histórico o de colección y aquellos cuyo valor unitario supere la cantidad de [IMPORTE].

[OPCIONAL — incluir si procede]

(Posibles deterioros)

Cuando a juicio de la empresa transportista exista la posibilidad de deterioro de los bienes objeto de la mudanza, bien por encontrarse en mal estado o porque deban ser sometidos a manipulaciones que puedan entrañar peligro, se expresará claramente esta circunstancia en el inventario, con declinación, en su caso, de responsabilidad por parte de la empresa transportista.

[OPCIONAL — incluir si procede]

Cuarta.- Exclusiones

No será objeto del contrato de mudanza el transporte de armas de fuego, de mercancías perecederas o peligrosas, ni de animales.

Tampoco será objeto del contrato de mudanza el transporte de dinero en metálico, joyas, piedras preciosas, valores al portador, objetos de plata, obras de arte, objetos antiguos o de colección, etc.

El servicio de mudanza no incluye, salvo pacto expreso, el transporte y manipulación de objetos de gran volumen o peso.

.- Información

A requerimiento del transportista, el cliente deberá informarle de todas las circunstancias relevantes para el desarrollo de la mudanza, así por ejemplo de las condiciones de acceso a los locales o viviendas para el personal y los vehículos [OTROS DATOS].

.- Seguros

El transportista se compromete a asegurar los muebles y enseres objeto del transporte relacionados en el inventario, según el valor que en el mismo se les haya asignado, informando al cliente del nombre de la compañía aseguradora con la que se haya suscrito el seguro, del número de póliza y de cualquier otra circunstancia que pueda tener interés para el cliente, particularmente la existencia de franquicia.

En todo caso, el aseguramiento de la mercancía, no afecta a la responsabilidad contractual del transportista como consecuencia del incumplimiento del contrato de mudanza.

.- Formalidades administrativas

Correrá de cuenta del transportista la gestión de las eventuales formalidades administrativas necesarias para ejecutar la mudanza.

El pago de toda clase de tasas, derechos de aduanas y demás tributos, certificados de origen o de traslado de residencia, gastos consulares, transbordos, etc., necesarios para la ejecución de la mudanza, no están incluidos en el precio del contrato y deberán sumarse a este.

El transportista estará obligado a justificar documentalmente estos gastos al cliente.

.- Entrega y recepción de la mudanza

Concluida la mudanza, el cliente, deberá firmar al transportista copia del inventario, a los efectos de dar su conformidad sobre la recepción de la totalidad de muebles, enseres y cajas. En caso contrario, el cliente podrá dejar constancia de los daños en muebles y enseres.

La firma de dicho documento no podrá ser más tarde de las [Nº] horas contadas desde la finalización de los trabajos de mudanza.

[OPCIONAL — incluir si procede]

(Plazo extra para reclamar daños)

Además, una vez concluida la mudanza, el consumidor dispondrá de un plazo de días hábiles, para reclamar a la empresa transportista los daños en muebles y enseres que haya podido constatar. Transcurrido dicho plazo no se admitirá reclamación alguna por pérdida o avería.

.- Responsabilidad del transportista

El mobiliario y demás efectos objeto del servicio de mudanza se transportan a riesgo y ventura del cliente. Por ello serán de su cuenta todos los daños y menoscabos que puedan sufrir aquellos durante el transporte de conformidad con lo previsto en el artículo 76 de la Ley del contrato de transporte terrestre de mercancías.

El porteador no responderá de los daños, retrasos o pérdidas que se produzcan por fuerza mayor o caso fortuito, como incendio, rayo, inundaciones, etc; por causas políticas o sociales, como sabotajes, huelga, motines, fuerzas o medidas militares, incluso en tiempo de paz, guerras, etc.; deterioro de los muebles subidos o bajados por balcones o escaleras dificultosas, los ocasiona dos por la estrechez de las puertas o pasillos y en muebles que, con anterioridad al servicio, se encuentren encolados o restaurados; Los desperfectos producidos por derrames de líquidos, sustancias o ácidos contenidos en recipientes, combustión espontánea, influencia de la temperatura, fermentación, etc., roturas de mármoles de color, lunas y espejos sin marco; los debidos a naturaleza o vicio propio de las cosas o a cualquier otra causa semejante.

.- Indemnizaciones

[OPCIONAL — incluir si procede]

(Por anulación o aplazamiento)

La anulación del contrato o aplazamiento del servicio por indicación del cliente o por decisión del transportista, dará lugar a una indemnización a favor de la parte perjudicada. Dicha indemnización se fija en [PORCENTAJE] del importe de la mudanza, si la parte contraria es notificada con más de [Nº] días y menos de [Nº DE DÍAS] antes de la fecha de ejecución del servicio.

[OPCIONAL — incluir si procede]

(Daños)

Fuera de los casos previstos en los apartados anteriores, el transportista responde de los daños y averías debidos a dolo, culpa o negligencia grave, en los términos de los artículos 1.101 y concordantes del Código Civil, en relación con lo dispuesto en el artículo 76 de la Ley del contrato de transporte terrestre de mercancías.

[ELEGIR: Retrasos]

Los retrasos que pudieran producirse en el servicio darán derecho a reclamaciones por parte del cliente de [IMPORTE].

.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

.- Protección de datos personales

Las partes reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

.- Gastos e Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta [ELEGIR: de la empresa transportista / del cliente].

.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones de la Ley 15/2009, de 11 de noviembre, del contrato de transporte terrestre de mercancías y demás disposiciones concordantes, leyes especiales y usos mercantiles que le sean aplicables

.- Fuero competente

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Tribunales de [LOCALIDAD].

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD].

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

EL TRANSPORTISTA

D./Dña. [NOMBRE Y APELLIDOS]

EL CLIENTE

D./Dña. [NOMBRE Y APELLIDOS]

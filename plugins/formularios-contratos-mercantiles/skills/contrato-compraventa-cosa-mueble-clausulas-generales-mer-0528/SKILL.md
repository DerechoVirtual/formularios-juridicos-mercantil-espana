---
name: contrato-compraventa-cosa-mueble-clausulas-generales-mer-0528
description: "Contrato de compraventa de cosa mueble con cláusulas generales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de cosa mueble con cláusulas generales

> Formulario **MER-0528** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que el vendedor se obliga a entregar una cosa, a cambio del pago de un precio por el comprador. Se incluyen cláusulas referidas a distintos tipos de bienes, pactos y lugares: sobre muestras, de bienes futuros, a ensayo o prueba, con pacto de retro, reserva de dominio, tienda, almacén, mercado o feria, sin responsabilidad por evicción

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de cosa mueble con cláusulas generales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de cosa mueble con cláusulas generales” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-compraventa-cosa-mueble-clausulas-generales-mer-0528`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (11 veces)
- [ ] IMPORTE (8 veces)
- [ ] Nº (7 veces)
- [ ] DESCRIPCIÓN DEL BIEN (4 veces)
- [ ] DNI/NIE (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] PLAZO (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] LUGAR DE ENTREGA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº DE ANEXO (2 veces)
- [ ] AÑO
- [ ] CIRCUNSTANCIAS DE LOS BIENES
- [ ] DOMICILIO A EFECTOS DE NOTIFICACIONES
- [ ] DÍA
- [ ] HORA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE CLÁUSULA
- [ ] Nº DE EJEMPLARES
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 345 Código de Comercio
- art. 327 Código de Comercio

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

Contrato por el que el vendedor se obliga a entregar una cosa, a cambio del pago de un precio por el comprador. Se incluyen cláusulas referidas a distintos tipos de bienes, pactos y lugares: sobre muestras, de bienes futuros, a ensayo o prueba, con pacto de retro, reserva de dominio, tienda, almacén, mercado o feria, sin responsabilidad por evicción


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

En lo sucesivo, EL COMPRADOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EL VENDEDOR.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de COMPRAVENTA y, a tal fin,

EXPONEN

I. Que el vendedor es propietario de [DESCRIPCIÓN DEL BIEN], por título de [ELEGIR: compraventa / donación / fabricación propia]) estando interesado en su venta.

[OPCIONAL — incluir si procede]

(Para compraventa de bienes futuros)

I. Que el vendedor será propietario de [DESCRIPCIÓN DEL BIEN] como consecuencia de y que entrará en posesión de la misma en [FECHA].

II. Que el comprador está interesado en la compra de los bienes descritos en la manifestación anterior. Y es conocedor [CIRCUNSTANCIAS DE LOS BIENES]

[OPCIONAL — incluir si procede]

(En los casos de compraventa de bienes a prueba o ensayo o salvo aprobación)

Siempre y cuando, una vez llevadas a cabo todas aquellas pruebas que estime convenientes para determinar la utilidad de las mismas, considere que son de su agrado.

III. Expuesto cuanto antecede, las partes convienen el otorgamiento del presente contrato de compraventa conforme a los pactos y cláusulas que se determinan a continuación:

CLAUSULAS

Primera.- Objeto

El objeto del presente contrato es la compraventa de en la feria de en el mercado [DESCRIPCIÓN DEL BIEN] señalados en [Nº DE ANEXO] de este contrato, en la cantidad y calidad detalladas en el mismo.

[OPCIONAL — incluir si procede]

(Cuando se trate de Compraventa sobre muestras)

El producto que se vende en el presente contrato se realiza sobre las muestras de las mercaderías entregadas por el vendedor al comprador.

Segunda.- Precio

El precio de la presente compraventa es de [IMPORTE] euros.

[OPCIONAL — incluir si procede]

(Cuando el pago de la totalidad del precio es anterior)

El vendedor manifiesta haber recibido la totalidad del precio indicado con anterioridad a este acto del comprador, sirviendo el presente documento como carta de pago.

[OPCIONAL — incluir si procede]

(Cuando el pago de la totalidad del precio es simultaneo)
[ELEGIR UNA OPCIÓN: En efectivo / Con cheque / Por transferencia]

[OPCIONAL — incluir si procede]

(Cuando el pago de la totalidad del precio es anterior y simultaneo)

Esta cantidad será satisfecha de la siguiente forma:

a) la cantidad de [IMPORTE], reconoce el vendedor haberla recibido del comprador con anterioridad a este acto.
b) la cantidad de [IMPORTE], es pagada en este acto por el comprador en efectivo (o mediante cheque bancario nominativo o transferencia) por valor de [IMPORTE] sirviendo el presente documento como carta de pago.

[OPCIONAL — incluir si procede]

(Cuando media aplazamiento del pago del precio)

Esta cantidad será pagada de la siguiente forma:

a) [IMPORTE] euros se entregan al vendedor en este acto por el comprador mediante [ÓRGANO] sirviendo el presente documento como carta de pago.
b) [IMPORTE] será satisfecha por el comprador en un total de [Nº] pagos, el primero de los cuales tendrá lugar el [DÍA] de [MES] de [AÑO]

Como garantía del abono del precio aplazado se libran - letras de cambio-números [Nº] por importe [IMPORTE] cada una de ellas y con vencimiento los díasde cada mes. Dichas letras de cambio son aceptadas en este acto por el comprador.

[ELEGIR UNA OPCIÓN: Con condición suspensiva / Con condición resolutoria]

Tercera.- Entrega de los bienes

Las mercancías y bienes objeto del presente contrato de compraventa que se relacionan y describen en [Nº DE ANEXO] deberán ser entregadas en [LUGAR DE ENTREGA] en un plazo máximo de [PLAZO].

[OPCIONAL — incluir si procede]

(En tienda o Almacén)

El bien objeto del contrato se entrega en este acto, en el establecimiento, causando prescripción de derecho a favor del comprador, sin perjuicio de las acciones legales que puedan corresponder al propietario.

[OPCIONAL — incluir si procede]

(Si se establece reserva de dominio:)

El vendedor se reserva el dominio de los bienes que constituyen el objeto de la presente compraventa hasta el pago definitivo del precio aplazado. El impago de cualquiera de los plazos indicados anteriormente dejará sin efecto la obligación del vendedor de transmitirlos facultándole para optar entre el cumplimiento del contrato o la resolución del mismo. Una vez verificado el pago íntegro de las entregas descritas en se entenderá transmitido el dominio de los bienes

En el supuesto de que por cualquier otra causa, el comprador fuera privado del bien objeto de este contrato, éste deberá ponerlo en conocimiento inmediato del vendedor con el fin de que pueda adoptar las acciones que estime oportunas al respecto, sin que por ello se vea liberada de la obligación del pago íntegro del precio. En el supuesto de que el comprador omitiera esta obligación, se entenderá que existe responsabilidad por su parte en el destino final del bien y mala fe en su comportamiento.

La enajenación o la realización de cualquier otro acto de disposición en tanto no se haya verificado efectivamente el pago requerirá la autorización previa y por escrito del vendedor

[OPCIONAL — incluir si procede]

(Cuando se trate de Compraventa sobre muestras)

El vendedor se compromete a entregar los objetos vendidos con igual calidad, forma y tamaño que los del muestrario puesto a disposición del comprador, y que sustancialmente se corresponde con la siguiente descripción:

Los bienes objeto del contrato se entregarán en [LUGAR DE ENTREGA]. el [FECHA]. del corriente año, entre sus [HORA]. y sus [Nº]. horas, corriendo a cargo de la parte vendedora los gastos de dicho transporte.

[OPCIONAL — incluir si procede]

(Si se establece pacto de retro)

El vendedor se reserva el derecho de recuperar el objeto de esta compraventa en el plazo de [Nº] meses, a partir de la fecha de este contrato. Transcurrido dicho plazo el vendedor perderá su derecho

El objeto de este contrato no podrá ser enajenado, gravado, ni dispuesto bajo ningún concepto por el comprador hasta que se cumpla el plazo pactado en la cláusula [Nº DE CLÁUSULA], o encuentre un comprador dispuesto a pagar por el objeto de este contrato la cantidad de [IMPORTE] euros, en cuyo caso, el vendedor autoriza al comprador inicial para vender el objeto de este contrato antes del vencimiento del plazo pactado, distribuyendo el exceso del precio de este contrato en relación con el que obtenga del último comprador, en la proporción del % para el vendedor y por el [PORCENTAJE] para el comprador

[OPCIONAL — incluir si procede]

.- Conformidad con el objeto del contrato

EL comprador manifiesta conocer el estado en el que se encuentran los bienes objeto de esta compraventa, y afirma que todos ellos se encuentran en perfectas condiciones de conservación y funcionamiento sin que exista deterioro alguno en los mismos, por encima de los lógicos de la antigüedad. Igualmente manifiesta que su funcionamiento es óptimo para el desempeño de la labor que tiene asignada y libera al vendedor de las obligaciones dispuestas en el art.345 del Código de Comercio.

[OPCIONAL — incluir si procede]

(Si existen conflictos previos sobre el bien [DESCRIPCIÓN DEL BIEN])

El comprador, manifiesta conocer la situación jurídica o litigiosa en la que se encuentra el vendedor con respecto al bien mueble objeto de este contrato, y acepta su compra en las condiciones que se establecen en el presente contrato.

Igualmente, través del presente contrato el comprador se compromete a no transmitir la propiedad del bien mueble, entregándolo a la persona que sobre él tuviere mejor derecho en el caso de que posteriores resoluciones judiciales fallaran que esa persona fuera otra distinta a la que él compró.

[ELEGIR UNA OPCIÓN: Con responsabilidad por evicción / Sin responsabilidad por evicción]

[OPCIONAL — incluir si procede]

(Cuando se trate de compraventa sobre muestras)

Una vez entregadas las mercancías el comprador se compromete a aceptarlas si coinciden con las calidades descritas en el muestrario según lo previsto en la Cláusula del presente documento.

En caso contrario dispondrá de un plazo de [Nº] días a partir de esa fecha para la solicitud de sustitución de las piezas defectuosas o no ajustadas a dichas calidades.

El plazo de sustitución de las piezas no puede ser superior a días. En caso de que el vendedor no proceda a dicha sustitución dentro de ese plazo, el comprador podrá proceder a la íntegra resolución del contrato.

A efectos de lo previsto en el artículo 327 del Código de Comercio las partes nombran de común acuerdo a D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS] como Peritos encargados de decidir, en su caso, si los géneros han de considerarse o no de recibo.

[OPCIONAL — incluir si procede]

(Cuando se trate de compraventa a prueba o ensayo y/o salvo aprobación)

.- Pruebas o ensayos

El comprador asume el derecho y la obligación de realizar todas las pruebas que estime necesarias para comprobar la utilidad de los bienes adquiridos en el plazo máximo de [Nº] días naturales contados a partir de la fecha su entrega.

[ELEGIR UNA OPCIÓN: Si se trata de compraventa a prueba / Si se trata de compraventa salvo aprobación]

.- Daños y perjuicios

Si el comprador devolviera los bienes con desperfectos tales que hiciesen imposible su uso o destino, el vendedor podrá exigir el cumplimiento íntegro del contrato, no estando obligado a devolver las cantidades recibidas a cuenta del precio. Si los bienes estuvieran deteriorados, pero no hasta el punto de resultar inútiles para el uso o destino habitual de los mismos, el comprador deberá soportar el coste de su reparación y restituirlos en el mismo estado en el que se encontraban cuando fueron entregados. Cuando no exista acuerdo sobre el coste efectivo de la restitución o reparación de los bienes, ambas partes se someten a D./Dña. [NOMBRE Y APELLIDOS] que actuará en este caso como árbitro, comprometiéndose a asumir y respetar la solución que el mismo determine. Todo ello, sin olvidar que, desde que se acuerde la cantidad efectiva que deba satisfacerse conforme a lo previsto en la presente cláusula, la misma devengará un interés diario igual al legal del dinero incrementado en [Nº] puntos.

Los honorarios ocasionados por la actuación del árbitro designado habrá de ser soportados por ambas partes al [PORCENTAJE] %.

[OPCIONAL — incluir si procede]

Cuando se trate de compraventa con pacto de retro

.- Devolución

En caso de que el vendedor ejercitara su derecho de retracto devolverá al comprador el precio recibido por este contrato, incrementado con el [PORCENTAJE] % de intereses devengados por dicha cantidad desde esta fecha y todos los gastos e impuestos que pueda ocasionar el presente contrato.

[OPCIONAL — incluir si procede]

(Para compraventas de bienes futuros)

.- Resolución

En el supuesto caso de que el vendedor no pudiera llegar a ser propietario del bien futuro que aquí transmite en el plazo de [PLAZO], contado a partir de la fecha del presente contrato, devolverá la cantidad percibida en el plazo de [PLAZO], en un solo acto y en efectivo, quedando el contrato sin valor alguno.

.- Notificaciones

Las partes convienen los siguientes domicilios para la práctica de las notificaciones necesarias para la ejecución del presente contrato:

El vendedor

El comprador: [DOMICILIO A EFECTOS DE NOTIFICACIONES].

.- Naturaleza mercantil

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto, por las disposiciones del Código de Comercio, leyes especiales, usos mercantiles, y en su defecto, por el Código Civil.

.- Gastos e Impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo del comprador.

.- Fuero

Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Tribunales de [LOCALIDAD]

Y en prueba de conformidad con todo ello firman el presente contrato por [Nº DE EJEMPLARES] ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

_______________________________

EL COMPRADOR

_______________________________

EL VENDEDOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

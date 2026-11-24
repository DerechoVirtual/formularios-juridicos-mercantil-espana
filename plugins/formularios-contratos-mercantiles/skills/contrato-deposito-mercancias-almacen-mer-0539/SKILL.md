---
name: contrato-deposito-mercancias-almacen-mer-0539
description: "Contrato de depósito de mercancías en almacén. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de depósito de mercancías en almacén

> Formulario **MER-0539** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato mediante el cual el que lo suscribe deposita bienes de su propiedad en los almacenes del depositario durante un período de tiempo. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del acuerdo, así como los derechos y obligaciones de cada una de las partes.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de depósito de mercancías en almacén» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de depósito de mercancías en almacén” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-deposito-mercancias-almacen-mer-0539`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] DESCRIPCIÓN DEL BIEN (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] PLAZO (3 veces)
- [ ] FECHA (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] DÍA
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE

## Normas que cita el formulario

- art. 1.770 Código Civil
- art. 306 Código de Comercio
- art. 1.779 Código Civil

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

Contrato mediante el cual el que lo suscribe deposita bienes de su propiedad en los almacenes del depositario durante un período de tiempo. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del acuerdo, así como los derechos y obligaciones de cada una de las partes.


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
(Datos del DEPOSITARIO)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, DEPOSITARIO.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del DEPOSITANTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, DEPOSITANTE.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de DEPÓSITO MERCANTIL y, a tal fin,

MANIFIESTAN

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

I. Que el Depositario de forma no habitual asume la guarda y custodia de bienes muebles, no siendo su principal actividad económica. Para ello dispone de un espacio adecuado, localizado en

I. Que el Depositario es un profesional dedicado a la guardia y custodia de bienes y mercancías en depósito, siendo ésta su actividad económica principal. Para el desarrollo de su actividad cuenta con un almacén sito en [LOCALIDAD].

II. Que el Depositante dispone, en su condición de [ELEGIR: propietario / arrendatario / usufructuario] de [DESCRIPCIÓN DEL BIEN], en concreto, del siguiente tipo: [DESCRIPCIÓN DEL BIEN], marca [MARCA/MODELO], modelo [MARCA/MODELO] y tiene interés en depositarlo en los almacenes descritos en la manifestación precedente

III. Que el Bien Depositado se valora en la cantidad total de [IMPORTE]

IV. Que ambas partes acuerdan llevar a efecto el presente contrato de depósito mediante las siguientes:

CLÁUSULAS

Primera.- Objeto

Mediante el presente Contrato, el Depositante hace entrega en este acto del [DESCRIPCIÓN DEL BIEN], el cual posee de forma legítima, en favor del Depositario para su guarda y custodia comprometiéndose a su restitución en la fecha fijada en el presente Contrato.

La restitución del Bien Depositado tendrá lugar en el plazo señalado, en las mismas condiciones en las que fue entregado, incluyendo sus correspondientes accesorios, sus productos y accesiones, siguiendo lo dispuesto en el artículo 1.770 del Código Civil.

[ELEGIR UNA OPCIÓN: Con precio / Gratuito]

[OPCIONAL — incluir si procede]

Segunda.- Precio

El depositante se obliga a pagar por este depósito mercantil la cantidad de [IMPORTE] euros, sin incluir los impuestos que pudieran derivarse de esta operación.

[OPCIONAL — incluir si procede]

(Cuando el pago de la totalidad del precio es simultaneo)
[ELEGIR UNA OPCIÓN: En efectivo / Con cheque / Por transferencia]

[OPCIONAL — incluir si procede]

(Cuando el pago de la totalidad del precio es anterior y simultáneo)

Esta cantidad será satisfecha de la siguiente forma:

a) la cantidad de [IMPORTE], reconoce el depositante haberla recibido del depositario con anterioridad a este acto.
b) la cantidad de [IMPORTE], es pagada en este acto por el depositante [ELEGIR: en efectivo / mediante cheque bancario nominativo / por transferencia] por valor de [IMPORTE] sirviendo el presente documento como carta de pago.

[OPCIONAL — incluir si procede]

(Cuando media aplazamiento del pago del precio)

Esta cantidad [IMPORTE] será satisfecha por el depositante en un total de [Nº] pagos, el primero de los cuales tendrá lugar el [FECHA].

Como garantía del abono del precio aplazado se libran - letras de cambio-números [Nº] por importe [IMPORTE] cada una de ellas y con vencimiento los días de [DÍA] cada mes. Dichas letras de cambio son aceptadas en este acto por el CLIENTE.

[ELEGIR UNA OPCIÓN: Con condición suspensiva / Con condición resolutoria]

.- Duración

[ELEGIR UNA OPCIÓN: Sin prórrogas / Con prórrogas]

En todo caso, el Depositario deberá restituir el Bien Depositado al Depositante con anterioridad a la fecha señalada de finalización siempre que así lo demanden por escrito, tal y como establece el artículo 306 del Código de Comercio.

La finalización del Contrato como consecuencia de la llegada a término de su periodo de duración inicial, o de cualquiera de sus prórrogas, no generará ningún derecho de indemnización o compensación a favor de ninguna de las Partes.

.- Obligaciones y responsabilidad del depositario

El depositario, una vez puestas a su disposición las mercaderías, que en depósito se le consignen, deberá cuidar de ellas con la diligencia conveniente, siendo responsable de cualquier daño o merma que, por cualquier causa, pudieran sufrir las mercaderías depositadas. Deberá guardarlas y conservarlas en los almacenes descritos anteriormente sin que pueda trasladarlas del lugar sin autorización del depositante

En este sentido, el Depositario será considerado como el único responsable del Depósito y asumirá su responsabilidad, tal y como se recoge en los artículos 1.101 y ss. del Código Civil, sin que le puedan imputar los daños causados por caso fortuito, fuerza mayor o acciones ilícitas de terceros que no se hubieran podido prever. Dichos daños deberán ser notificados por el Depositario a los Depositantes tan pronto como se produzcan.

[OPCIONAL — incluir si procede]

(Seguros)

Con la finalidad de cubrir la responsabilidad de las circunstancias descritas, el Depositario cuenta con una póliza de seguros que cubrirá el valor del Bien Depositado durante la vigencia de este Contrato.

[OPCIONAL — incluir si procede]

(Fuerza mayor)

Se entenderá como Fuerza Mayor, entre otras: inundación, incendio, explosión, cierre patronal, huelga, disturbio civil, bloqueo, embargo, mandato, ley, orden, regulación, ordenanza, demanda o petición del gobierno, o cualquier otra causa que se encuentre fuera de control de la Parte involucrada, sin que pueda entenderse que la falta de fondos constituye una causa de Fuerza Mayor.

La Parte afectada por la Fuerza Mayor hará todo lo posible por eliminar su causa. La exigibilidad de la obligación cuyo cumplimiento se haya visto afectado por la situación de Fuerza Mayor se suspenderá hasta [PLAZO] después de que la situación de Fuerza Mayor deje de impedir o retrasar el cumplimiento. Si la causa de Fuerza Mayor no desaparece tras treinta [PLAZO], o un plazo inferior que justifique la imposibilidad de ejecutar la obligación, las Partes podrán acordar la modificación del Contrato o su resolución

.- Inspección

Se reconoce expresamente el derecho del depositante a efectuar cuantos reconocimientos de las mercancías objeto del presente contrato considere precisos a fin de asegurarse de su buen estado

.- Confidencialidad

Las Partes se comprometen a adoptar todas las medidas necesarias para mantener en secreto toda las información que le haya sido comunicada como tal por la otra Parte durante la vigencia del presente Contrato. Salvo cuando se trate de:

a. información que sea de dominio público;
b. información que dispusieran la Parte antes de haberles sido facilitada por la otra Parte; y,
c. información legalmente adquirida por las Partes de fuentes distintas a las derivadas del presente Contrato.

.- Gastos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE]

Se incluyen, entre otros, los gastos de conservación y mantenimiento del Bien Depositado, los costes de almacenaje, los pagos realizados para la adaptación de las instalaciones al Bien Depositado y todos los perjuicios que le pueda provocar el Depósito, según lo dispuesto en el artículo 1.779 del Código Civil.

.- Prohibición de transmisión de derechos

La cesión o transmisión, independientemente de la forma o negocio jurídico utilizado al efecto, de los derechos y obligaciones asumidos por cualquiera de las Partes, no estará permitida sin la previa autorización expresa y por escrito de la otra Parte

.- Resolución

El presente Contrato podrá ser resuelto en cualquier momento por cada una de las Partes, a su elección, sin necesidad de intervención judicial, y sin perjuicio de la responsabilidad en la que incurra la otra Parte por su incumplimiento contractual, siempre que existan "causas justificadas", tal y como se expone a continuación:

El incumplimiento total o parcial por la otra Parte de alguna de las condiciones u obligaciones esenciales de este Contrato que no sea corregido en el plazo de [PLAZO] a partir de la notificación escrita y fehaciente; y,

II. las demás establecidas en el articulado del presente Contrato o las que se recojan en la ley, y en concreto, en el Código Civil y el Código de Comercio.

.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

.- Protección de datos personales

Las Partes reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos sin la correspondiente autorización del titular de los datos personales.

.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones del Código de Comercio, especialmente por sus artículos 193 a 198 y 303 a 310, usos mercantiles que le sean aplicables, o en lo no previsto, por las disposiciones del Código Civil.

.- Impuestos

Todos los gastos judiciales o extrajudiciales, que se originen como consecuencia de la formalización de este contrato o del nacimiento, cumplimiento o extinción del mismo, serán de cuenta de la parte contratante que la ley establezca

.- Fuero competente

[ELEGIR UNA OPCIÓN: Sometimiento a fuero judicial / Sometimiento a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

DEPOSITARIO

DEPOSITANTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

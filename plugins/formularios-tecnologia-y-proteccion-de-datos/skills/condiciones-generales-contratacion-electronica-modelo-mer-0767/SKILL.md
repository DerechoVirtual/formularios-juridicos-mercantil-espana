---
name: condiciones-generales-contratacion-electronica-modelo-mer-0767
description: "Condiciones generales de contratación electrónica (modelo). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Condiciones generales de contratación electrónica (modelo)

> Formulario **MER-0767** del plugin **Contratos tecnológicos, comercio electrónico y protección de datos** (`formularios-tecnologia-y-proteccion-de-datos`) · Mercantil › Tecnología, comercio electrónico y protección de datos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Condiciones generales de contratación electrónica (modelo)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Condiciones generales de contratación electrónica (modelo)” para mi caso». También puedes invocarla directamente con `/formularios-tecnologia-y-proteccion-de-datos:condiciones-generales-contratacion-electronica-modelo-mer-0767`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-tecnologia-y-proteccion-de-datos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos tecnológicos, comercio electrónico y protección de datos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DIRECCIÓN WEB (3 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 27 Ley 34/2002

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

PREVIO

Las presentes condiciones generales resultarán de aplicación a las adquisiciones de productos y/o servicios realizadas a través de esta página de Internet.

Han sido elaboradas de conformidad con lo establecido en la Ley 3/2014, de 27 de marzo, por el que se modificó la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, la Ley 34/2002, de Servicios de la Sociedad de la Información y Comercio Electrónico y la Ley 7/1998 sobre Condiciones Generales de Contratación, y cuantas disposiciones legales autonómicas o estatales resulten de aplicación.

El contrato se formalizará en lengua castellana.

A continuación se presenta el documento contractual que regulará la contratación de los productos y servicios adquiridos en la página web …… cuya propiedad pertenece a la empresa [DENOMINACIÓN SOCIAL] S.L. (en adelante, el VENDEDOR)

La aceptación del presente documento implica que el adquirente manifiesta:

a.

Que es una persona con capacidad suficiente para contratar.

b.

Que ha leído, entiende y comprende las condiciones de contratación que aquí se detallan.

c.

Que acepta las obligaciones aquí establecidas.

El VENDEDOR se reserva el derecho de modificar unilateralmente las presentes condiciones, sin que ello implique afectar a las adquisiciones de bienes y/o servicios efectuados con anterioridad a la modificación.

OBJETO DEL CONTRATO

El presente acuerdo contractual tiene por objeto la regulación de las condiciones contractuales de compraventa entre el VENDEDOR y el USUARIO en el momento en que este último acepta durante el proceso de contratación on line la casilla correspondiente.

La compra de los productos ofrecidos en la página de internet [DIRECCIÓN WEB] conlleva la entrega por parte del VENDEDOR, obligándose el USUARIO a abonar el precio del producto públicamente expuesto a través del señalado sitio web, y a hacer un uso del mismo conforme a la ley y a las presentes condiciones.

PROCEDIMIENTO DE CONTRATACIÓN

El USUARIO deberá, para poder adquirir un producto durante su primer pedido, abrir una cuenta de cliente y proporcionar y cumplimentar los campos obligatorios señalados por el VENDEDOR.

El USUARIO seleccionará un nombre de usuario y una contraseña, asumiendo un compromiso de hacer un uso diligente de los mismos.

Una vez creada la cuenta de usuario, se informa que de conformidad con lo dispuesto en el artículo 27 de la Ley 34/2002 de Servicios de la Sociedad de la Información y del Comercio Electrónico, el procedimiento de contratación seguirá los siguientes pasos:

(Explicar de acuerdo al procedimiento de contratación utilizado)

1.

2.

3.

4.

5.

En cualquier caso, se informará por correo electrónico al USUARIO por parte del VENDEDOR, una vez cerrado el procedimiento de contratación, de las características, precio, formas de transporte, fecha de contratación y estimación de entrega del producto adquirido.

FORMA, GASTOS Y PLAZO DE ENVÍO

El USUARIO podrá escoger la forma de envío de entre las posibles para su zona.

Los plazos de entrega y el coste serán diferentes según la forma de transporte elegida.

La entrega de los productos adquiridos se realizarán en el domicilio designado por el USUARIO, no asumiendo el VENDEDOR ninguna responsabilidad cuando la entrega del producto no llegue a realizarse como consecuencia de que los datos suministrados por el USUARIO sean falsos, inexactos o incompletos o cuando la entrega no pueda efectuarse por causas ajenas a la empresa de envíos, como lo es la ausencia del destinatario.

La entrega de los productos adquiridos se realizará en el plazo de diez días, no pudiendo superar en ningún caso los treinta días naturales a contar desde la celebración del contrato.

El USUARIO podrá consultar en todo momento el estado de su pedido, solicitando información en el número de teléfono [TELÉFONO] o bien a través del correo electrónico atención.al.cliente@empresa.com.

Cuando el VENDEDOR no realice la entrega en el plazo acordado, el USUARIO tendrá derecho a resolver el contrato, y en tal situación, el VENDEDOR deberá entregar sin demora todas las cantidades abonadas por el consumidor. En el caso de que el VENDEDOR no proceda al abono, el USUARIO tendrá derecho a reclamar que se le pague el doble de la suma adeudada, sin perjuicio de su derecho a ser indemnizado por los daños y perjuicios sufridos en los que excedan de dicha cantidad.

PRECIO E IMPUESTOS

El precio de los productos ofertados en la página de Internet [DIRECCIÓN WEB] están señalados en [IMPORTE] euros (€), incluyendo el Impuesto sobre el Valor Añadido (IVA) que, en su caso, sea procedente aplicar.

Las transacciones que vayan a ser entregadas dentro del territorio de los estados miembros de la Unión Europea estarán sujetas a IVA.

Las compras que deban ser entregadas en territorios de Estados no miembros de la Unión Europea, o en Canarias, Ceuta o Melilla estarán exentos de IVA.

FACTURACIÓN Y FORMA DE PAGO

Todo pago efectuado al VENDEDOR conllevará la emisión de una factura a nombre del USUARIO registrado en la página web.

La factura será automáticamente enviada a la dirección de correo electrónico facilitada por el USUARIO y será también enviada junto al producto adquirido.

El pago del producto adquirido se podrá realizar mediante tarjeta de crédito (Visa, MasteCard y American Express, cargándose el importe en el mismo momento de celebrada la transacción). También podrá efectuarse el pago contra reembolso.

El VENDEDOR manifiesta que la página de Internet [DIRECCIÓN WEB] utiliza tecnología de cifrado certificada, para proteger los datos del USUARIO del acceso no autorizado de terceras personas. Los datos de la tarjeta de crédito y del pedido se transmiten cifrados, con procedimientos 3D y SSL (Secure Socket Layer). Toda la información personal se trata de forma confidencial.

GARANTÍAS

Todos los productos aquí ofertados tienen una garantía de dos años, conforme a lo establecido en el Real Decreto Legislativo 1/2007, de 16 de noviembre, por el que se aprueba el texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias.

DERECHO DE DESISTIMIENTO

El USUARIO dispondrá de un plazo de desistimiento de catorce días naturales a contar de la fecha de recepción del producto para la devolución del mismo. En cualquier caso, el producto deberá ser devuelto en su embalaje original y en perfecto estado.

En tal caso, el VENDEDOR deberá devolver las cantidades abonadas por el USUARIO, en el plazo de catorce días naturales desde la fecha en que se haya informado de la decisión de desistimiento.

LEGISLACIÓN APLICABLE Y COMPETENCIA JUDICIAL

Las presentes condiciones generales se regirán conforme a la legislación española en aquello que no esté expresamente establecido. El VENDEDOR y el USUARIO, acuerdan someter cualquier controversia que pudiera originarse de la transacción objeto de estas condiciones, a los Tribunales del domicilio del USUARIO.

En el supuesto de que el USUARIO tenga su domicilio fuera de España, el VENDEDOR y el USUARIO renuncian expresamente a cualquier otra jurisdicción, sometiéndose a los Tribunales de la ciudad de [LOCALIDAD] (España)

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

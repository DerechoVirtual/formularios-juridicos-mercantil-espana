---
name: contrato-venta-cartera-clientes-mer-0833
description: "Contrato de venta de una cartera de clientes. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de venta de una cartera de clientes

> Formulario **MER-0833** del plugin **Traspasos de negocio, confidencialidad y acuerdos de empresa** (`formularios-traspasos-y-acuerdos-de-empresa`) · Mercantil › Otros documentos mercantiles · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que una empresa o profesional transmite a otra el conjunto de clientes adquirido a lo largo de los años en que ejerció su actividad, con cesión de los créditos, migración de clientes y pacto de no competencia. Se utiliza generalmente entre empresas dedicadas a la misma actividad.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de venta de una cartera de clientes» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de venta de una cartera de clientes” para mi caso». También puedes invocarla directamente con `/formularios-traspasos-y-acuerdos-de-empresa:contrato-venta-cartera-clientes-mer-0833`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-traspasos-y-acuerdos-de-empresa:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Traspasos de negocio, confidencialidad y acuerdos de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (10 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DNI/PASAPORTE (3 veces)
- [ ] DOMICILIO (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NACIONALIDAD (3 veces)
- [ ] TIPO DE IVA (3 veces)
- [ ] DATOS REGISTRALES: FOLIO, TOMO, HOJA (2 veces)
- [ ] DESCRIPCIÓN DE LA ACTIVIDAD (2 veces)
- [ ] DNI/PASAPORTE DEL CÓNYUGE (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL CÓNYUGE (2 veces)
- [ ] Nº (2 veces)
- [ ] PLAZO (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] ZONA GEOGRÁFICA (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DENOMINACIÓN SOCIAL DEL COMPRADOR
- [ ] DESCRIPCIÓN DEL PROCEDIMIENTO
- [ ] DESCRIPCIÓN DETALLADA DE LAS ACTIVIDADES Y SERVICIOS
- [ ] DÍA
- [ ] ENTIDAD DE CRÉDITO
- [ ] IBAN
- [ ] IMPORTE
- [ ] LOCALIDAD, CALLE Y NÚMERO
- [ ] MECANISMO Y PLAZO DE NOTIFICACIÓN
- [ ] MEDIO DE PAGO: METÁLICO, CHEQUE, ETC.
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTADO
- [ ] Nº DE PROTOCOLO
- [ ] SERVICIOS

## Normas que cita el formulario

- art. 347 Código de Comercio

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

- Junto a «…ciembre, de Protección de Datos Personales y garantía de los derechos digitales.»: la cesión de datos personales de los clientes al comprador exige analizar la base jurídica del tratamiento (art. 6 RGPD) y el deber de información a los clientes cedidos (arts. 13 y 14 RGPD).

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

DE UNA PARTE,

[Datos del VENDEDOR]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y DNI/Pasaporte número [DNI/PASAPORTE].

[OPCIONAL — incluir si procede (estado civil casado/a)]
Casado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con DNI/Pasaporte número [DNI/PASAPORTE DEL CÓNYUGE], en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, VENDEDOR.

[Si hay más de una persona en esta posición contractual, repetir el párrafo anterior tantas veces como sea necesario.]

Y DE OTRA,

[Datos del COMPRADOR]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y DNI/Pasaporte número [DNI/PASAPORTE].

[OPCIONAL — incluir si procede (estado civil casado/a)]
Casado/a con D./Dña. [NOMBRE Y APELLIDOS DEL CÓNYUGE], mayor de edad, con DNI/Pasaporte número [DNI/PASAPORTE DEL CÓNYUGE], en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, COMPRADOR.

INTERVIENEN

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Todas las partes en su propio nombre y representación.

— D./Dña. [NOMBRE Y APELLIDOS], en su propio nombre y representación. (Repetir para cada parte que actúe en nombre propio.)

— D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si se trata de persona física) D./Dña. [NOMBRE Y APELLIDOS DEL REPRESENTADO], mayor de edad, de nacionalidad [NACIONALIDAD], domiciliado en [DOMICILIO], con DNI/Pasaporte número [DNI/PASAPORTE].

— (Si se trata de persona jurídica) La compañía mercantil denominada [DENOMINACIÓN SOCIAL], domiciliada en [LOCALIDAD, CALLE Y NÚMERO], con NIF núm. [NIF], inscrita en el Registro Mercantil de [PROVINCIA], en [DATOS REGISTRALES: FOLIO, TOMO, HOJA]. Hace uso de las facultades conferidas a su favor en calidad de [ELEGIR: administrador único / administrador solidario / consejero delegado / apoderado] de la sociedad indicada, cargo para el que fue nombrado en escritura otorgada ante el notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO] el [FECHA], con el número [Nº DE PROTOCOLO] de su protocolo, que causó inscripción en el Registro Mercantil de [PROVINCIA] en [DATOS REGISTRALES: FOLIO, TOMO, HOJA].

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato y, a tal fin,

MANIFIESTAN

I.- Que el VENDEDOR es una entidad dedicada, entre otras actividades, a [DESCRIPCIÓN DE LA ACTIVIDAD], habiendo generado en la realización de la misma una cartera de clientes a los que viene prestando los citados servicios, y que se detalla en el Anexo I del presente contrato.

II.- Que el VENDEDOR ha decidido finalizar el ejercicio de la actividad citada de [ACTIVIDAD], por lo que está interesado en transmitir la titularidad sobre la cartera de clientes mencionada respecto a dicha actividad, descrita en el Anexo II.

III.- Que el COMPRADOR es una entidad dedicada, entre otras actividades, a [DESCRIPCIÓN DE LA ACTIVIDAD], por lo que está interesado en la adquisición de la cartera de clientes descrita en los apartados precedentes.

IV.- Que por ello ambas partes acuerdan llevar a efecto el presente contrato de COMPRAVENTA DE CARTERA DE CLIENTES con sujeción a las siguientes

CLÁUSULAS

PRIMERA.– Objeto

Mediante el presente contrato el VENDEDOR vende al COMPRADOR, quien adquiere, la cartera de clientes descrita en el Exponente I y detallada en el Anexo I, en relación con los servicios citados de [SERVICIOS], según se definen en el Anexo II.

La transmisión de la titularidad sobre la cartera de clientes objeto del presente contrato se produce con su firma e implica igualmente la transmisión de todos los derechos y obligaciones sobre la misma.

SEGUNDA.– Precio

El precio del objeto de la compraventa es de [IMPORTE] EUROS, más IVA, de conformidad para ambas partes, habiéndose determinado éste con arreglo a [CRITERIO DE DETERMINACIÓN: FACTURACIÓN INICIAL, FACTURACIÓN FINAL O VALORACIÓN PERICIAL (DESCRIBIR MÉTODO)].

TERCERA.– Pago

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (De la totalidad a la firma) El pago se efectúa en el presente acto mediante [MEDIO DE PAGO: METÁLICO, CHEQUE, ETC.], cantidad que el vendedor declara haber recibido a su entera satisfacción, sirviendo el presente documento como carta de pago.

— (Aplazado y por renovaciones) Las Partes acuerdan que el Precio, incrementado con el [TIPO DE IVA] % de IVA aplicable, se abonará por el Comprador al Vendedor de la siguiente forma: cuotas mensuales. El Vendedor facturará [Nº] mensualidades al Comprador en función de las renovaciones de las suscripciones de los Clientes de la siguiente forma:

• Durante el primer año el Vendedor facturará al Comprador el [PORCENTAJE] % (más el [TIPO DE IVA] % en concepto de IVA) del importe cobrado por los Servicios prestados por el Comprador a los Clientes, del [FECHA] al [FECHA].

• Durante el segundo año el Vendedor facturará al Comprador el [PORCENTAJE] % (más el [TIPO DE IVA] % en concepto de IVA) del importe cobrado por los Servicios prestados por el Comprador a los Clientes, del [FECHA] al [FECHA].

— (Posterior y por ingreso) El pago se efectuará mediante [ELEGIR: ingreso / transferencia] el día [FECHA] en la cuenta corriente n.º [IBAN] que EL VENDEDOR tiene suscrita con la entidad [ENTIDAD DE CRÉDITO].

CUARTA.– Procedimiento de migración

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Procedimiento genérico) Las partes acuerdan que el proceso migratorio de los servicios prestados hasta la fecha por el VENDEDOR al COMPRADOR se efectuará ajustándose a lo siguiente: [DESCRIPCIÓN DEL PROCEDIMIENTO]. A tales efectos, los clientes que forman parte de la cartera cedida serán notificados de dicha subrogación por el siguiente mecanismo y en el siguiente plazo: [MECANISMO Y PLAZO DE NOTIFICACIÓN].

— (Si se establece un calendario)

Día [FECHA]: el vendedor notificará a los clientes sobre el cambio del prestador de los servicios.

Día [FECHA]: el vendedor facilitará los detalles de facturación y cobro para que el comprador pueda tramitar el cambio administrativo en sus proveedores.

Día [FECHA]: el vendedor entregará al comprador las claves de acceso a los servidores donde se alojan las cuentas.

Día [FECHA]: el vendedor emitirá la primera factura correspondiente al mes de [MES].

QUINTA.– Transmisión de titularidad

La transmisión de la titularidad de la cartera de clientes se realiza en el momento de la firma del presente Contrato e implica, asimismo, la transmisión de todos los derechos y obligaciones de la misma.

Desde la firma del presente contrato, cualquier acuerdo que se formalice entre EL VENDEDOR y cualquiera de los clientes que integran la Cartera de Clientes se celebrará en nombre y por cuenta del COMPRADOR.

SEXTA.– Cesión de créditos

EL VENDEDOR cede al COMPRADOR todos los créditos que ostenta frente a los clientes que integran la Cartera nacidos con anterioridad a la firma del presente contrato. A efectos de este contrato, se entiende por cesión de créditos la transmisión por EL VENDEDOR al COMPRADOR de la titularidad de aquellos que detente frente a sus clientes y que provengan de su actividad comercial.

La cesión de créditos se realizará mediante la entrega, por EL VENDEDOR al COMPRADOR, de cuantos documentos los representen. Los documentos de crédito deberán incorporar, inexcusablemente, en sus originales y copias, la cláusula de cesión siguiente: "El crédito representado por este documento ha sido cedido de forma irrevocable a [DENOMINACIÓN SOCIAL DEL COMPRADOR], en virtud de contrato de compraventa de cartera de clientes, por lo que, de conformidad con el artículo 347 del Código de Comercio, el único pago liberatorio será el realizado directamente a la citada mercantil".

EL VENDEDOR queda obligado a proporcionar al COMPRADOR toda la documentación correspondiente a cada operación, facilitándole asimismo toda la información referente a la gestión del cobro, y otorgándole poderes suficientes a favor de los Letrados y Procuradores de los Tribunales que éste le indique para iniciar o seguir cualquier procedimiento judicial o extrajudicial tendente al cobro de las cantidades correspondientes por los impagados que puedan producirse.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Sin intervención del vendedor) EL VENDEDOR se compromete a no intervenir en las gestiones que realice EL COMPRADOR para el cobro de los créditos cedidos, salvo aquellas que le sean solicitadas por éste.

— (Con intervención del vendedor) EL VENDEDOR gestionará el cobro de las cantidades adeudadas por aquellos clientes integrantes de la Cartera de Clientes que hayan sido cedidos. EL VENDEDOR facilitará copia del expediente de cada uno de los clientes integrantes de la Cartera de Clientes cuyos créditos hayan sido cedidos.

SÉPTIMA.– Confidencialidad

Tanto el VENDEDOR como el COMPRADOR se comprometen a no divulgar la información confidencial referente a la otra parte de la que hayan tenido conocimiento por razón de las negociaciones que han precedido a la firma del presente contrato y a mantenerla en secreto, incluso después de su firma.

OCTAVA.– Pacto de no concurrencia

EL VENDEDOR se obliga a no tomar a su cargo la venta de productos de clase similar o que puedan ser objeto de competencia con el COMPRADOR o dificulten el mercado de cualquier manera de las ACTIVIDADES descritas en el Anexo II durante un plazo de [PLAZO] y para la zona geográfica de [ZONA GEOGRÁFICA].

La obligación de NO COMPETENCIA que se pacta en esta cláusula desplegará sus efectos incluso en el caso de extinción del presente contrato, por un período máximo de [PLAZO] contado a partir del día siguiente a aquél en que, en su caso, se produzca dicha extinción, y para la zona geográfica de [ZONA GEOGRÁFICA].

NOVENA.– Resolución

El Contrato podrá resolverse por las siguientes causas:

• Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas. En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento.

• Por acuerdo de las Partes por escrito.

DÉCIMA.– Gastos e impuestos

En su caso, todos los gastos de elevación a público y/o impuestos indirectos derivados del otorgamiento del presente Contrato serán soportados por las Partes según Ley.

DECIMOPRIMERA.– Carácter mercantil y legislación aplicable

El presente contrato tiene exclusivamente carácter mercantil. El contrato se regirá por las estipulaciones pactadas por las partes, por los anexos (si los hay) y, en su defecto, por la legislación aplicable y vigente en la materia recogida en el Código de Comercio y, subsidiariamente, en el Código Civil.

DECIMOSEGUNDA.– Protección de datos

Ambas partes deberán cumplir con lo establecido por la normativa relativa a la protección de datos, especialmente con lo establecido por el Reglamento (UE) 2016/679 (RGPD) y por la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales.

DECIMOTERCERA.– Notificaciones

Todas las notificaciones, requerimientos, peticiones y otras comunicaciones que hayan de efectuarse por las Partes en relación con el presente Contrato deberán realizarse por escrito y se entenderá que han sido debidamente realizadas cuando hayan sido entregadas en mano o bien remitidas por correo certificado al domicilio de la otra Parte que conste en el encabezamiento del presente Contrato, o bien a cualquier otro domicilio que a estos efectos cada Parte pueda indicar a la otra.

DECIMOCUARTA.– Tribunales

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los Juzgados y Tribunales de [LOCALIDAD], renunciando expresamente a su fuero propio si lo tuvieran.

El presente Contrato reemplaza y sustituye cualesquiera contratos, cartas o instrumentos anteriores entre las partes relativos al objeto convenido en el presente.

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

COMPRADOR | VENDEDOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] | Firmado: D./Dña. [NOMBRE Y APELLIDOS]

ANEXO I. Cartera de clientes transmitida

[RELACIÓN DE CLIENTES: NOMBRE O RAZÓN SOCIAL Y NIF DE CADA UNO, CON LOS CONCEPTOS E IMPORTES FACTURADOS EN LOS 12 MESES ANTERIORES A LA FIRMA DEL CONTRATO]

ANEXO II. Descripción de las actividades y servicios a que se refiere la cartera

[DESCRIPCIÓN DETALLADA DE LAS ACTIVIDADES Y SERVICIOS]

NOTAS DE USO

El contrato de compraventa de cartera de clientes es aquel mediante el cual una parte vende a otra una cartera de clientes a los cuales les está prestando un servicio o proveyendo de bienes o mercancías.

En cuanto a los intervinientes, si se trata de una persona física que interviene en su propio nombre y derecho es preciso hacer constar tal extremo. Lo mismo sucede si interviene en representación de otra persona física; en este caso será necesario describir la fuente de la que dimana su representación, ya sea legal o convencional. En el mismo sentido, si se trata de una persona física que actúa en beneficio de una sociedad de gananciales, de una sociedad civil irregular o de una comunidad de bienes, puesto que en estos casos no existe una personalidad jurídica diferente de la de los miembros que la integran.

En cuanto al objeto, téngase en cuenta que en el anexo deberá figurar el nombre o razón social, así como el NIF, de los clientes que integran la cartera transmitida. Igualmente, deberán constar los conceptos e importes facturados correspondientes a los 12 meses anteriores a la firma del contrato.

Respecto a los pagos no satisfechos puntualmente por el comprador, recuérdese que la Ley 3/2004, de 29 de diciembre, por la que se establecen medidas de lucha contra la morosidad en las operaciones comerciales, establece la aplicación automática de un tipo de interés de demora, sin necesidad de aviso de vencimiento ni de intimación alguna por parte del acreedor. No obstante, el acreedor sólo podrá exigir el pago de los intereses de demora cuando haya cumplido con las obligaciones contractuales y legales que le incumbían y cuando el retraso en el pago no sea imputable a su conducta. Si se dan estas condiciones se devengará el interés de demora contractual o el fijado legalmente conforme a dicha Ley.

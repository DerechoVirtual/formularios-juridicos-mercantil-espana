---
name: contrato-colaboracion-entre-empresa-productora-otra-mer-0512
description: "Contrato de colaboración entre una empresa productora y otra que vende sus productos por internet. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de colaboración entre una empresa productora y otra que vende sus productos por internet

> Formulario **MER-0512** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de colaboración entre una empresa productora y otra que vende sus productos por internet» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de colaboración entre una empresa productora y otra que vende sus productos por internet” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-colaboracion-entre-empresa-productora-otra-mer-0512`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DESCRIPCIÓN DEL PRODUCTO (2 veces)
- [ ] LUGAR (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] PLAZO (2 veces)
- [ ] CANTIDAD MÍNIMA DE STOCK
- [ ] DESCRIBIR
- [ ] IMPORTE
- [ ] MEDIO DE ENVÍO
- [ ] Nº
- [ ] Nº DE CUENTA (IBAN)
- [ ] PERIODICIDAD
- [ ] REGISTRO DE INSCRIPCIÓN
- [ ] SIGNOS DISTINTIVOS
- [ ] TÍTULO DE PROPIEDAD
- [ ] URL
- [ ] ÓRGANO

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

Acuerdo de colaboración suscrito entre una empresa productora de bienes y servicios con otra que se va a dedicar a la venta on line de dichos bienes y servicios: el fabricante cede el uso de los signos distintivos de su propiedad y su "Know How" a la comercializadora sin una zona geográfica determinada para la comercialización en exclusiva de sus productos, a cambio de un canon inicial y un porcentaje de su facturación mensual.

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de LA COMERCIALIZADORA)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, COMERCIALIZADORA.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del FABRICANTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, FABRICANTE.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de colaboración para venta on line de productos y servicios y, a tal fin,

MANIFIESTAN

I.- Que EL FABRICANTE es propietario por título de [TÍTULO DE PROPIEDAD] del PRODUCTO/SERVICIO [DESCRIPCIÓN DEL PRODUCTO] y del ’Know How‘ preciso para la comercialización de dicho PRODUCTO/SERVICIO. Inscrito en la Oficina Española de Patentes y Marcas con el nº [NÚMERO].

II.- Que LA COMERCIALIZADORA ON LINE ha sido seleccionado por EL FABRICANTE para pasar a formar parte de su red de comercialización on line en la forma y condiciones que se dirán, y que por ello ambas partes

ACUERDAN

Llevar a efecto el presente CONTRATO DE COLABORACIÓN PARA VENTA ON LINE DE PRODUCTOS Y SERVICIOS mediante las siguientes

CLÁUSULAS

Primera.- Objeto

EL FABRICANTE nombra a [NOMBRE DE LA PARTE] como su COMERCIALIZADORA ON LINE, para lo cual le cede el uso de los signos distintivos de su propiedad [SIGNOS DISTINTIVOS]. inscritos con el número [NÚMERO] en [REGISTRO DE INSCRIPCIÓN] y su "Know How" consistente en [DESCRIBIR], con la finalidad de que sean utilizados de manera exclusiva en la comercialización de [DESCRIPCIÓN DEL PRODUCTO].

Segunda.- Precio

En contraprestación EL FABRICANTE paga en el presente acto a LA COMERCIALIZADORA ON LINE la cantidad de [IMPORTE] EUROS en concepto de entrada o canon inicial, cantidad que éste manifiesta haber recibido a su entera satisfacción, surtiendo el presente documento efectos de carta de pago. Asimismo, LA COMERCIALIZADORA ON LINE se obliga a pagar al FABRICANTE el [ÓRGANO] por ciento de su facturación mensual, cantidades que se entregarán el día [FECHA] de cada mes siguiente al del vencimiento en la cuenta corriente [Nº DE CUENTA (IBAN)] y previo envío por [MEDIO DE ENVÍO] por LA COMERCIALIZADORA ON LINE de la documentación justificativa del volumen de las ventas.

Tercera.- Duración

El presente contrato tendrá una duración de [Nº] años a contar desde la fecha de la firma, pero a la llegada del término se entenderá prorrogado tácitamente por períodos anuales salvo denuncia expresa en contrario por cualquiera de las partes con un preaviso de [PLAZO].

Cuarta.- Uso de signos distintivos

LA COMERCIALIZADORA ON LINE se obliga a proceder al uso comercial de los signos distintivos citados una vez obtenidos los permisos correspondientes, así como las autorizaciones o licencias que legalmente se establezcan de acuerdo a las siguientes instrucciones [OTROS DATOS].

Quinta.- URL

LA COMERCIALIZADORA ON LINE sólo puede explotar el negocio ON LINE en la URL [URL] que cumple los requerimientos gráficos y de seguridad del sitio on line especificados en el Anexo I. Cualquier cambio en los requerimientos citados deberá ser efectuado con el consentimiento del FABRICANTE.

Sexta.- Obligaciones de la comercializadora

- LA COMERCIALIZADORA ON LINE se compromete a:
-No desarrollar un negocio idéntico ni de características análogas al que es objeto del presente acuerdo durante toda la vigencia del mismo, así como durante un plazo de [PLAZO] con posterioridad a su extinción.
- Aprovisionarse exclusivamente del FABRICANTE o de los proveedores que éste le indique para la puesta en marcha y funcionamiento de su entorno comercial on line durante toda la vigencia del presente contrato, manteniendo siempre un mínimo stock de [CANTIDAD MÍNIMA DE STOCK].
- Seguir de buen grado las instrucciones del FABRICANTE en cuanto al uso de los signos distintivos así como en cuanto a la gestión comercial de su negocio on line, en todo aquello que forme parte del "Know How" descrito en la Cláusula Primera del presente contrato.
- Mantener el secreto de cuanta información sobre el "Know How"’ le sea transmitida por el FABRICANTE.
- Desarrollar su actividad con la diligencia de un buen comerciante, en el intento de mantener las cifras de ventas y alcanzar al menos, para cada periodo, las especificadas en el Anexo I;

[OPCIONAL — incluir si procede]

(Solo también cuando se negocie mejorar en posicionamiento en buscadores)

- Alcanzar las cifras de posicionamiento de la marca en los términos pactados con el FABRICANTE en el Anexo I, las cuales serán revisadas [PERIODICIDAD]

- Disponer de los medios de seguridad en el pago y de seguridad en el tratamiento de los datos especificados en el Anexo I.
- Cumplir los requisitos de comercio electrónico, en particular en lo referente a las obligaciones previas a la contratación y a la información posterior a la celebración del contrato, así como en cuanto al derecho de desistimiento que rige para el comercio minorista.
- Respetar cuantos otros aspectos puedan afectar a la imagen de la marca de los productos y servicios del FABRICANTE.

Séptima.- Obligaciones del Fabricante

EL FABRICANTE se compromete a:

- Prestar la asistencia que precise LA COMERCIALIZADORA ON LINE, tanto en el momento de instalación del negocio como durante el resto de la vigencia del contrato.
- Respetar la exclusividad a LA COMERCIALIZADORA ON LINE [OTROS DATOS].
- Realizar la publicidad de los productos y servicios a los que se refiere el presente contrato.
- Mantener la marca, nombre comercial, rótulo de establecimiento, etc. cuyo uso cede a LA COMERCIALIZADORA ON LINE.
- Aprovisionar a LA COMERCIALIZADORA ON LINE con los productos de temporada (o de temporadas pasadas en caso de outlet on line), en cantidad suficiente y en plazo adecuado, según los pedidos que le sean realizados por éste.
- Respetar la independencia comercial de LA COMERCIALIZADORA ON LINE, sin perjuicio de las obligaciones a las que éste se compromete por virtud del presente contrato.

Octava.- Legislación aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones de la Ley 34/2002, de 11 de julio, de servicios de la sociedad de la información y de comercio electrónico; en lo en ella no previsto, por el Código de Comercio y demás disposiciones aplicables y, en su defecto, por lo dispuesto en el Código Civil.

Novena.- Gastos e impuestos

Todos los gastos, impuestos, tasas, arbitrios y corretajes que puedan derivarse de la formalización, trámite, cumplimiento o extinción del presente contrato serán de cuenta de [NOMBRE DE LA PARTE].

Décima.- Juzgados y tribunales

Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Tribunales de [LOCALIDAD].

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

Es justicia que pido en [LUGAR], a [FECHA].

FABRICANTE

COMERCIALIZADORA
D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]
ANEXO I.- Requerimientos gráficos y de seguridad del sitio on line y cifras de posicionamiento y ventas

En este documento conviene especificar aspectos como los siguientes:

1. Requerimientos mínimos y características técnicas y de programación informática para la comercialización así como especificaciones mínimas de la herramienta a través de la cual los usuarios de internet podrán acceder al negocio de comercio electrónico en Internet.
2. Parámetros para delimitar el posicionamiento que se quiere alcanzar y cifras de ventas que se pretenden conseguir.
3. Detallar si EL FABRICANTE va a tener o no acceso a la herramienta informática que permite controlar y gestionar los servicios contratados, la facturación de los mismos, así como efectuar altas, bajas y modificaciones de los productos, acceder al panel de control y realizar consultas de forma autenticada.
4. Detallar el cumplimiento por parte de LA COMERCIALIZADORA al respeto de los requisitos legales establecidos, entre otras, por las siguientes normas:
a) En materia de comercio electrónico, en concreto los arts. 23 y ss. Ley 34/2002, de 11 de julio, de servicios de la sociedad de la información y comercio electrónico
b) En materia de comercio minorista, en particular el derecho de desistimiento de los clientes de los arts. 68 y ss. TRLGDCU;
c) Cumplimiento en general de la normativa en materia de consumidores y usuarios, en particular lo relativo a condiciones generales y cláusulas abusivas (arts. 80 y ss. TRLGDCU) y garantía de bienes de consumo (arts. 114 y ss. TRLGDCU).
d) En materia de protección de datos de los clientes. En su caso, si EL FABRICANTE va a acceder a los mismos, deberá establecerse el nivel de medidas también para EL FABRICANTE. Y puesto que Internet opera en un entorno global, detallar que LA COMERCIALIZADORA ON LINE va a respetar la normativa de protección de datos también en cuanto a la transferencia internacional de datos (se producirá en todo caso cuando se hagan pagos desde el extranjero) (Ley Orgánica 3/2018, de 5de diciembre, de protección de datos personales y garantía de derechos digitales).

========================================================================

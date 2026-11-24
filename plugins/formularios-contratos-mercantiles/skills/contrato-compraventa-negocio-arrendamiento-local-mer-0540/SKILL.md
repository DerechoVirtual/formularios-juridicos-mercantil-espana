---
name: contrato-compraventa-negocio-arrendamiento-local-mer-0540
description: "Contrato de compraventa de negocio con arrendamiento del local. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa de negocio con arrendamiento del local

> Formulario **MER-0540** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa de negocio con arrendamiento del local» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa de negocio con arrendamiento del local” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-compraventa-negocio-arrendamiento-local-mer-0540`.
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
- [ ] LOCALIDAD (5 veces)
- [ ] DNI/NIE (4 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] SUPERFICIE (2 veces)
- [ ] CALLE
- [ ] ENTIDAD BANCARIA
- [ ] FECHA
- [ ] NOMBRE COMERCIAL
- [ ] SERVICIOS

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

Notas al pie del formulario original:
(1) Téngase en cuenta que el 1 de enero de 2015 se cumplieron 20 años de la entrada en vigor de la vigente Ley de Arrendamientos Urbanos, lo que ha supuesto la extinción automática de muchos contratos de arrendamiento. En esta fecha expiró la moratoria que estableció la Disposición transitoria tercera de la Ley de Arrendamientos urbanos para los contratos de arrendamiento de local de negocio otorgados antes del 9 de mayo de 1985, bajo el régimen legal de prórroga forzosa.


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

En [LOCALIDAD]

REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de VENDEDOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, VENDEDOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del COMPRADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, COMPRADOR.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de COMPRAVENTA DE NEGOCIO y, a tal fin,

EXPONEN

I. Que D./Dña. [NOMBRE Y APELLIDOS] es propietario en pleno dominio de un establecimiento mercantil sito en la calle [CALLE], denominado [NOMBRE COMERCIAL] como nombre comercial registrado.

II. Que para ampliar su propio negocio D./Dña. [NOMBRE Y APELLIDOS] está interesado en la compra del citado negocio en funcionamiento y del alquiler del local en el que se ejerce el negocio.

III. Que han decidido realizar un contrato de compraventa de negocio, de conformidad con las siguientes

CLÁUSULAS

Primera

D./Dña. [NOMBRE Y APELLIDOS] vende a D./Dña. [NOMBRE Y APELLIDOS] quien compra el negocio de [ACTIVIDAD] comprendiendo en esta venta los bienes, derechos y créditos que se señalan en el anexo I del contrato.

Segunda

El precio de la compraventa del negocio mercantil se fija en [IMPORTE] euros ( €).

Tercera

El Vendedor hace la entrega al comprador del establecimiento para continuar la actividad mercantil de [ACTIVIDAD]. El establecimiento mercantil se entrega a plena satisfacción del comprador.

Cuarta

El comprador pagará el precio pactado en la cláusula segunda en la siguiente forma:

a) Haciéndose cargo del pasivo existente señalado en el anexo I, que alcanza la cifra de [IMPORTE] euros ( €).
b) Mediante la entrega al contado de parte precio por importe de [IMPORTE] euros, que entrega el comprador y recibe el vendedor en forma de cheque bancario conformado de la entidad bancaria [ENTIDAD BANCARIA] número [NÚMERO], sirviendo este documento como la más eficaz carta de pago.
c) El importe restante, es decir [IMPORTE] euros se abonará mensualmente a razón de [IMPORTE] euros, los 5 primeros días de cada mes. El vendedor podrá girar letras de cambio por el importe de las cantidades pendientes de pago que el comprador se obliga a aceptar sin que ello altere la naturaleza del presente contrato.

Quinta

Todos los pagos se realizarán, excepto los cambiarios, en el domicilio del vendedor.

Sexta

El vendedor que es propietario del local en el que se ejerce el negocio según consta en la escritura de propiedad de fecha [FECHA] inscrita en el Registro de la Propiedad de [LOCALIDAD] y que está libre de cargas según consta y declara el mismo, arrienda el local cuyas características se indican en el anexo II al comprador por un precio de [IMPORTE] euros mensuales pagaderos por anticipado los cinco primeros días de cada mes, mediante transferencia bancaria en la cuenta nº [NÚMERO] de la entidad bancaria

El arrendatario-comprador se compromete a no subarrendar o traspasar el local objeto del contrato, salvo que tenga autorización escrita del vendedor-arrendador.

Séptima

El comprador entrega la cantidad de [IMPORTE] euros en concepto de fianza, para responder en su caso de los daños que pueda realizar al inmueble.

Octava

Los bienes relacionados con los números [Nº] al [Nº] del anexo deberán ser devueltos, repuestos o bien sustituidos por dinero efectivo, en caso de rescisión del contrato o finalización del mismo.

Novena

El impago del precio de venta dará lugar a la rescisión de la venta y del arrendamiento concertado.

Décima

Los contratos de compraventa y de arrendamiento tienen efectos desde la firma del presente contrato, el de arrendamiento tendrá una duración de un año renovable por tácita reconducción, salvo denuncia de alguna de las partes por carta certificada con acuse de recibo enviada con dos meses de antelación.

Al tratarse de un negocio en funcionamiento el comprador se subroga en los contratos laborales que se compromete a mantener así como en los contratos de suministro, y de seguro notificando ambas partes a los suministradores y compañías de seguro el nombre del nuevo titular del negocio y que estos últimos acepten la subrogación.

Undécima

El vendedor se compromete bajo penalidad de [IMPORTE] euros, a no abrir nuevo establecimiento mercantil dedicado a la misma actividad que la del presente contrato en la misma ciudad donde radica éste durante un plazo de cinco años.

Duodécima

Todos los gastos, impuestos, que se deriven de la formalización, cumplimiento o extinción del presente contrato, serán a cargo del comprador.

Decimotercera

Las partes renunciando a su fuero propio, para toda reclamación concerniente al cumplimiento o interpretación del presente contrato se someten a arbitraje de la Cámara de Comercio de [LOCALIDAD] aceptando en este momento el reglamento de arbitraje de dicha cámara y comprometiéndose a aceptar el laudo que se emita.

Las partes manifiestan su conformidad al presente contrato, que otorgan y firman en dos ejemplares igualmente originales y auténticos formalizados a un solo efecto, en el lugar y fecha indicados en el encabezamiento.

VENDEDOR

COMPRADOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
ANEXO I
ACTIVO	PASIVO
1. Mobiliario	Acreedor valor
2. Maquinaria
3. Existencias

TOTAL	TOTAL
Diferencia: ACTIVO - PASIVO = precio venta.
El comprador	El vendedor
ANEXO II

Características del local:

Superficie:

Unidades: Sala Superficie [SUPERFICIE]

Servicios [SERVICIOS]

Patio [SUPERFICIE]

Inscripción en el registro de la propiedad libre de cargas.

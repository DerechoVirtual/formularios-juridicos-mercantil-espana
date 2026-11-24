---
name: contrato-mediacion-compraventa-inmuebles-mer-0490
description: "Contrato de mediación en la compraventa de inmuebles. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de mediación en la compraventa de inmuebles

> Formulario **MER-0490** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que una persona (mandante) encarga a otra (mediador), la compra o la venta ( en exclusiva) de un inmueble, finca o solar, comprometiéndose a cambio de ello a satisfacerle una retribución en el supuesto de que dicho contrato llegue a perfeccionarse.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de mediación en la compraventa de inmuebles» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de mediación en la compraventa de inmuebles” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-mediacion-compraventa-inmuebles-mer-0490`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DNI/NIE (4 veces)
- [ ] Nº (4 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] ACTIVIDAD
- [ ] COLEGIO PROFESIONAL
- [ ] FECHA
- [ ] LUGAR
- [ ] NOMBRE O DENOMINACIÓN
- [ ] OTROS DATOS
- [ ] SUPERFICIE
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

Contrato por el que una persona (mandante) encarga a otra (mediador), la compra o la venta ( en exclusiva) de un inmueble, finca o solar, comprometiéndose a cambio de ello a satisfacerle una retribución en el supuesto de que dicho contrato llegue a perfeccionarse.


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
(Datos del MANDANTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, MANDANTE.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del MEDIADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, MEDIADIOR.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de MEDIACIÓN INMOBILIARIA y, a tal fin,

EXPONEN

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

I. Que el Mandante, está interesado en la adquisición de una finca de [SUPERFICIE]. en la zona de [LOCALIDAD], donde tiene previsto instalar [ACTIVIDAD]

I. El mandante conviene con el mediador un contrato de mediación inmobiliaria, con el fin de que gestione y proporcione un cliente interesado en la venta de una finca propiedad del mandante, con las siguientes características [DESCRIPCIÓN DEL BIEN] en la zona de

II. Que el Mediador, se encuentra colegiado en [COLEGIO PROFESIONAL] de [LOCALIDAD], con el núm. «[NOMBRE O DENOMINACIÓN]» de Agente de la Propiedad Inmobiliaria, con despacho profesional abierto en la zona.

III. Que ambas partes han alcanzado un acuerdo en virtud del cual el Mediador se compromete a llevar a cabo las gestiones necesarias para la [ELEGIR: adquisición / venta] por parte del Mandante de la finca descrita, pactando para su ejecución el presente contrato de mediación, con arreglo a las siguientes:

ESTIPULACIONES

Primera.- Objeto

En virtud del presente contrato el Mediador se compromete a llevar a cabo todas las gestiones necesarias para que el Mandante [ELEGIR: adquiera / venda] un solar en la zona de [LOCALIDAD] de las características expuestas en el expositivo I.

[OPCIONAL — incluir si procede]

(Solo cuando se trate de compra)

Entre tales gestiones se encuentran:

• la localización del solar,
• la investigación de su situación jurídica y registral,
• la negociación con su propietario de las condiciones de venta, elaboración del correspondiente contrato de compraventa privado, etc.

En ningún caso, el Mediador podrá concluir por sí mismo la operación que le ha sido encargada formalizando el correspondiente contrato de compraventa, pues carece de poder de representación del Mandante.

Segunda.- Condiciones de [ELEGIR: compra / venta]

Las condiciones en que el mandante está interesado en suscribir la [ELEGIR: compra / venta] son:

- Precio de [ELEGIR: venta / compra]: euros.
- Plazo de pago: contado [Nº] meses [Nº] años
- [ELEGIR: El comprador / El mandante] se subrogará en la hipoteca.
- Las arras serán de un mínimo de [IMPORTE] euros.

[OTROS DATOS]

Tercera.- Corretaje

El Mediador percibirá [IMPORTE] euros por el desarrollo de las funciones que tiene encomendadas, (Optionally: más una bonificación adicional si el precio de [ELEGIR: compra es inferior / venta es superior] al fijado en la cláusula anterior

El Mediador sólo tendrá derecho a percibir la remuneración pactada en el caso de que sus gestiones finalmente concluyan en [ELEGIR: la adquisición / la venta] por parte del Mandante de [DESCRIPCIÓN DEL BIEN]. No teniendo derecho a remuneración alguna en caso contrario, con independencia de cuál sea la causa que frustre la operación.

Cuarta.- Firma del contrato

Cuando el mediador encuentre la persona física o jurídica que esté interesada en el contrato de [ELEGIR: compra / venta] notificará por escrito mediante [ÓRGANO] o cualquier otro medio del que quede constancia al mandante para que proceda a firmar el correspondiente contrato

El Mediador estará presente en el momento en que su Mandante y [ELEGIR: el Vendedor / el Comprador] concierten el contrato de [ELEGIR: compra / venta] objeto de su mediación, percibiendo la remuneración pactada en dicho acto.

Quinta.- Subcontratación

Si el mediador hace uso o colaboración de otros profesionales, cualquiera que sea su trabajo, correrán de cargo del mismo cuantos honorarios y gastos devenguen, salvo pacto expreso y escrito.

Sexta.- Duración

[ELEGIR UNA OPCIÓN: Sin prórrogas / Con prórrogas]

[OPCIONAL — incluir si procede]

(Adquisiciones posteriores a la finalización)

Si en los [Nº] meses siguientes a la finalización del contrato, el Mandante lleva a cabo la [ELEGIR: adquisición / venta] en condiciones similares a las propuestas por el mandante tendrá derecho a percibir su remuneración como si el contrato hubiese estado en vigor.

[OPCIONAL — incluir si procede]

(Habitualmente, solo para mandato de venta)

Séptima.- Exclusividad

El mandante manifiesta no tener encomendada la venta del inmueble objeto de este contrato a ningún otro intermediario inmobiliario, y se obliga a no encargar la gestión a ninguno otro distinto al mediador durante la vigencia del presente encargo, ni hacer gestiones tendentes a la venta del inmueble al margen del mediador.

Dado el carácter de exclusiva del presente contrato y los servicios que presta el mediador, si durante el período de vigencia del presente contrato el mandante vendiera el inmueble por su cuenta o a través de tercero, vendrá obligado a abonar al mediador en concepto de indemnización el importe equivalente a los honorarios pactados.

.- Cargas y gravámenes

El mandante se compromete a transmitir el inmueble objeto de este contrato, libre de arrendamientos, cargas y gravámenes.

.- Resolución

Son causas de terminación y resolución del presente contrato las siguientes:

• Vencimiento de la duración pactada
• Acuerdo mutuo de las partes
• Cumplimiento y ejecución de la prestación convenida
• Incumplimiento de cualquiera de las partes de alguna de las cláusulas del presente contrato, sin que dicho incumplimiento fuera subsanado dentro de [Nº] días siguientes a la notificación por escrito efectuada por la otra parte solicitando la subsanación del incumplimiento.

[OPCIONAL — incluir si procede]

(Permanencia de otras indemnizaciones)

La resolución del presente contrato no excluye las reparaciones legales o judiciales que cualquiera de las partes estime oportuno obtener

.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

.- Protección de datos personales

Las partes reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

.- Gastos e Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta del [ELEGIR: mandante / mediador].

.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones Código de Comercio, leyes especiales y usos mercantiles que le sean aplicables, o en lo no previsto, por las disposiciones del Código Civil.

.- Fuero competente

[ELEGIR UNA OPCIÓN: Sometimiento a tribunales / Sometimiento a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

MANDANTE

________________________________

MEDIADOR

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

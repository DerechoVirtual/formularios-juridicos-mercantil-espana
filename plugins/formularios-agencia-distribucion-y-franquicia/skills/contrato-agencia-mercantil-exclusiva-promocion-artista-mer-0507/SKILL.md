---
name: contrato-agencia-mercantil-exclusiva-promocion-artista-mer-0507
description: "Contrato de agencia mercantil con exclusiva para la promoción de un artista. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de agencia mercantil con exclusiva para la promoción de un artista

> Formulario **MER-0507** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato mercantil de agencia con pactos en exclusiva de promoción artística, mediante el cual el artista encarga al agente y promotor, entre otras, su representación, concertación de entrevistas, apariciones públicas, gestiones ante el Registro de la Propiedad Intelectual, firma de actuaciones y campañas de publicidad.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de agencia mercantil con exclusiva para la promoción de un artista» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de agencia mercantil con exclusiva para la promoción de un artista” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-agencia-mercantil-exclusiva-promocion-artista-mer-0507`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] DNI/NIE (4 veces)
- [ ] OTROS DATOS (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº (3 veces)
- [ ] PLAZO (3 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PERIODICIDAD (2 veces)
- [ ] ÁMBITO TERRITORIAL (2 veces)
- [ ] ACTIVIDAD
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIBIR
- [ ] FECHA
- [ ] FECHAS
- [ ] HECHO QUE DEVENGA LA COMISIÓN
- [ ] LUGAR
- [ ] PROVINCIA

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

Modelo de contrato mercantil de agencia con pactos en exclusiva de promoción artística, mediante el cual el artista encarga al agente y promotor, entre otras, su representación, concertación de entrevistas, apariciones públicas, gestiones ante el Registro de la Propiedad Intelectual, firma de actuaciones y campañas de publicidad.


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

(Datos del ARTISTA)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EL ARTISTA.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

(Datos del AGENTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EL AGENTE.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato y, a tal fin,

MANIFIESTAN

I.- Que EL ARTISTA se dedica a [ACTIVIDAD] en el ámbito [ÁMBITO TERRITORIAL]

II.- Que EL AGENTE cuenta con experiencia en la representación en dicho sector y con organización propia suficiente para el ejercicio de su actividad y se halla colegiado en el Colegio de Agentes de Comercio de [PROVINCIA] con el número [NÚMERO].

III.- Que EL ARTISTA está interesado en introducirse en de residencia del AGENTE, y que por ello ambas partes

ACUERDAN

Llevar a efecto el presente contrato de AGENCIA y PROMOCIÓN ARTÍSTICA, mediante las siguientes:

CLÁUSULAS

Primera.- Objeto

EL ARTISTA nombra a D./Dña. [NOMBRE Y APELLIDOS] como su AGENTE Y PROMOTOR para que con la diligencia y buena fe con que en dicha calidad actúa le represente EN EXCLUSIVA en su promoción en

Asimismo EL ARTISTA encarga al AGENTE, quien acepta, la prestación de los siguientes servicios consistentes en las siguientes actividades: dentro del ámbito señalado en el párrafo precedente:

a) Representación del artista ante terceros, especialmente ante los medios de comunicación: radiodifusión, televisiones públicas y privadas, etc.

b) Concertación de entrevistas, apariciones públicas, reportajes gráficos, ruedas de prensa en nombre del artista con dichos medios de comunicación, con sujeción especial a lo previsto en el clausulado del presente contrato.

c) Representación del artista ante el Registro de la Propiedad Intelectual (u organismo internacional competente) español para la realización de cuantas gestiones fueren precisas ante dicho organismo, y en especial para cuantas se deriven de los derechos de propiedad intelectual derivados de la actividad del artista.

d) Suscripción de contratos en nombre del artista para la celebración de actuaciones, con sujeción especial a lo acordado en el presente contrato.

e) Suscripción de contratos de publicidad en nombre del artista que se ajustará en todo caso a las siguientes características [OTROS DATOS].

[OPCIONAL — incluir si procede]

(Si se permite la delegación)

f) Delegación a favor de terceras personas de las anteriores facultades.

g) [OTROS DATOS].

Segunda.- Duración

[ELEGIR UNA OPCIÓN: Indefinido / Determinado]

Tercera.- Precios

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

El precio mínimo por el que el AGENTE está autorizado para realizar las ofertas y cerrar los contratos sobre:

[OPCIONAL — incluir si procede]

Actuaciones

[OPCIONAL — incluir si procede]

Galas

[OPCIONAL — incluir si procede]

Apariciones públicas

[OPCIONAL — incluir si procede]

Entrevistas

[OPCIONAL — incluir si procede]

Reportajes gráficos

[OTROS DATOS]

Es de [IMPORTE].

(Cuando el precio no se determina)

El ARTISTA se compromete a estar a disposición del AGENTE para la ejecución de los contratos suscritos por éste en su nombre.

Cuarta.- Remuneración del Agente

El ARTISTA se obliga a pagar al AGENTE:

a) Una CANTIDAD MENSUAL FIJA de [IMPORTE] euros.
b) Y una COMISIÓN del [Nº] por ciento por cada contrato suscrito por el AGENTE en nombre del ARTISTA. Esta cuantía se revisará cada [PERIODICIDAD].

[OPCIONAL — incluir si procede]

(Devengo de la comisión)

Las comisiones se devengarán en el momento en que EL ARTISTA [HECHO QUE DEVENGA LA COMISIÓN] (Por ejemplo: ejecute su actuación, o conceda una entrevista. Especificar, según el objeto del contrato), tanto si los contratos se han cerrado por dicho AGENTE como si han sido solicitados directamente por los clientes al ARTISTA.

[OPCIONAL — incluir si procede]

(Periodicidad y forma de pago)

Los pagos de las comisiones debidas por EL ARTISTA al AGENTE se efectuarán por liquidaciones periódicas mensuales los días [FECHAS] de cada mes en la cuenta corriente número [NÚMERO] que el AGENTE tiene abierta en la entidad [DENOMINACIÓN SOCIAL].

[OPCIONAL — incluir si procede]

(Detalle)

A tal fin, la EL ARTISTA se obliga a entregar en cada fecha de pago al AGENTE una relación de las comisiones devengadas por las operaciones correspondientes a dicho período, detallando el porcentaje correspondiente a la comisión sobre el precio de los contratos suscritos en su nombre.

c) En todo caso EL ARTISTA satisfará los GASTOS Y SUPLIDOS que los servicios objeto del presente contrato ocasionen al AGENTE, previa la acreditación de los mismos, que se efectuará con una periodicidad [PERIODICIDAD] mediante la presentación de las correspondientes facturas.

Quinta.- Comunicaciones

El AGENTE se compromete a informar inmediatamente al ARTISTA de las propuestas de contratos sobre [DESCRIBIR] que le sean solicitadas por terceros, indicando el nombre del posible cliente, su domicilio, la fecha y el lugar del evento, el precio por el que se ha pactado, la fecha y lugar de pago, [OTROS DATOS].

Las propuestas deberán ser comunicadas por EL AGENTE al ARTISTA con una antelación mínima de [PLAZO] a la celebración del evento, por medio de [ELEGIR: mail / fax / mensajero]

El ARTISTA comunicará su conformidad en el plazo de los [Nº] días siguientes a la recepción de las propuestas, por ese mismo medio.

En caso de ausencia de confirmación, EL AGENTE entenderá que no han sido aceptadas por el ARTISTA las propuestas y condiciones anunciadas.

Las órdenes que sean rechazadas por cualquier causa por el ARTISTA no generarán derecho remuneratorio alguno para el AGENTE, pero sí derecho al reintegro de los gastos que las gestiones realizadas al efecto le hayan ocasionado.

[OPCIONAL — incluir si procede]

Sexta- Derechos de Imagen

EL ARTISTA, cede a LA AGENCIA la utilización de sus derechos de imagen, nombre y/o voz durante la vigencia del presente contrato, a cambio del % del valor de los mismos, a través de cualesquiera medios publicitarios o de comunicación, con el fin de que LA AGENCIA pueda efectuar la promoción de su representado, así como a efectos promocionales y/o comerciales de la propia AGENCIA..

Séptima.- Indemnizaciones

El incumplimiento sin justa causa por parte del ARTISTA de cualquiera de los contratos suscritos en su nombre por el AGENTE, habiendo sido estos debidamente aceptados dará lugar a una indemnización a favor del AGENTE del [Nº] por ciento de la cantidad que éste habría recibido en caso de haberse celebrado el evento.

[OPCIONAL — incluir si procede]

(Indemnización por clientela)

Las partes acuerdan una indemnización por clientela, para los supuestos legalmente previstos, del importe medio anual de las remuneraciones globales que el AGENTE haya recibido durante los últimos [PLAZO].

Octava.- Exclusividad y no competencia

[ELEGIR UNA OPCIÓN: Exclusividad del Agente / Sin exclusividad]

Novena.- Resultados y rescisión

El AGENTE se compromete a conseguir para el ARTISTA un volumen de ingresos mínimo anual de [IMPORTE] euros en el territorio de [ÁMBITO TERRITORIAL].

El incumplimiento de dicha obligación por parte del AGENTE dará derecho al ARTISTA a dar por finalizado el contrato sin necesidad de preaviso, entendiéndose que el contrato finaliza a la recepción de la notificación escrita en la que conste la voluntad del ARTISTA de darlo por extinguido y la causa de la extinción.

[OPCIONAL — incluir si procede]

(Si se tienen en cuenta las proposiciones no aceptadas)

A los efectos de esta posibilidad de rescisión contractual por falta de ingresos mínimos el cómputo de dichos ingresos mínimos se efectuará tomando en consideración las proposiciones de contratos efectuadas por el AGENTE y no aceptadas por EL ARTISTA en el período de [PLAZO].

Décima.- Protección de datos

De conformidad con la Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos de personales y garantía de derechos digitales, EL ARTISTA autoriza a LA AGENCIA a incluir los datos personales indicados en el presente documento en un fichero con las finalidades que se desprenden de forma directa de la relación contractual establecida con LA AGENCIA y a cederlos y transmitirlos a quienes estén interesados en su contratación. Asimismo, se informa de la posibilidad de ejercitar los derechos de acceso, rectificación, cancelación y oposición.

Decimoprimera.- Impuestos y gastos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [ELEGIR: el agente / la empresa].

Decimosegunda.- Naturaleza del contrato

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones de la Ley sobre Contrato de Agencia, Ley 12/92, de 27 de Mayo, y en su defecto por lo previsto en el Código de Comercio, leyes especiales y usos mercantiles, y en su defecto por lo previsto en el Código Civil.

Decimotercera.- Fuero competente

La competencia para el conocimiento de cuantas acciones derive del presente contrato corresponde a los Tribunales de [LOCALIDAD], domicilio del AGENTE, en cumplimiento de lo previsto en la Disposición Adicional Segunda de la Ley 12/92, de 27 de mayo, que regula el contrato de agencia.

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

LA EMPRESA

EL AGENTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

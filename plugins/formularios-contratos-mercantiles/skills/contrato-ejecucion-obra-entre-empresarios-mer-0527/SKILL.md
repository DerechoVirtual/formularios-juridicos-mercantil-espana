---
name: contrato-ejecucion-obra-entre-empresarios-mer-0527
description: "Contrato de ejecución de obra entre empresarios. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de ejecución de obra entre empresarios

> Formulario **MER-0527** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato de realización de obra entre el arrendador o contratista y el arrendatario o comitente, incluyendo las estipulaciones, pactos y circunstancias necesarias para llevar a cabo la obra, así como los derechos y obligaciones de las partes. Todas las referencias a Juzgados contenidas en este documento se entenderán sustituidas por Tribunales de Instancia cuando estos se constituyan, conforme al régimen transitorio que prevé la DT 1ª LO 1/2025

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de ejecución de obra entre empresarios» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de ejecución de obra entre empresarios” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-ejecucion-obra-entre-empresarios-mer-0527`.
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
- [ ] PLAZO (4 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] Nº (2 veces)
- [ ] ACTUACIÓN A REALIZAR
- [ ] CALIDAD DEL COMITENTE
- [ ] CAUSA
- [ ] DESCRIBIR
- [ ] DIRECCIÓN
- [ ] FECHA
- [ ] LUGAR
- [ ] Nº DE ANEXO
- [ ] Nº DE CUENTA (IBAN)
- [ ] OTROS DATOS

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

Contrato de realización de obra entre el arrendador o contratista y el arrendatario o comitente, incluyendo las estipulaciones, pactos y circunstancias necesarias para llevar a cabo la obra, así como los derechos y obligaciones de las partes.

Todas las referencias a Juzgados contenidas en este documento se entenderán sustituidas por Tribunales de Instancia cuando estos se constituyan, conforme al régimen transitorio que prevé la DT 1ª LO 1/2025


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

En lo sucesivo, ARRENDADOR O CONTRATISTA.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ARRENDATARIO O COMITENTE.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de ARRENDAMIENTO DE OBRA y, a tal fin,

EXPONEN

I. Que el comitente es [CALIDAD DEL COMITENTE] de [DESCRIPCIÓN DEL BIEN].

II. Que el contratista conoce dicho [DESCRIPCIÓN DEL BIEN] así como su estado, características y condiciones.

III. Que, sobre el bien descrito anteriormente, el comitente tiene previsto realizar una obra consistente en [DESCRIBIR].

IV. Que el contratista está interesado en llevar a cabo la ejecución de la obra descrita en el expositivo precedente.

V. Que es de interés de las partes formalizar este contrato de arrendamiento de obra que se regirá por las siguientes

CLÁUSULAS

Primera.- Objeto

Mediante este contrato, el comitente encarga al contratista la ejecución de la siguiente obra, [ELEGIR: con suministro / sin suministro] de materiales por el primero, ejecución que el contratista acepta.

[OPCIONAL — incluir si procede]

(En caso de que se haya elaborado presupuesto previo)

La obra se ejecutará de acuerdo con el presupuesto que se adjunta como Anexo [Nº DE ANEXO] en el que se detallan las características de la obra y estimación de su precio, presupuesto que ambas partes aceptan.

Segunda.- Lugar de ejecución de la obra

La ejecución de la obra se desarrollará en [DIRECCIÓN].

Tercera.- Plazo

[ELEGIR UNA OPCIÓN: En caso de pacto de fecha inicial y entrega final / En caso de pacto de calendario y entregas parciales]

Cuarta.- Precio y forma de pago

El precio de la obra se fija en [IMPORTE] euros (IVA no incluido) [ELEGIR: como importe global / por hora de trabajo / por día de trabajo].

[OPCIONAL — incluir si procede]

(En caso de arrendamiento de obra sin suministro de materiales)

En el precio citado se incluye el pago por el contratista de todas las facturas por suministro de materiales.

El pago del precio se realizará, mediante transferencia bancaria, en la cuenta que designa el comitente [Nº DE CUENTA (IBAN)] o en la que pueda designar en el futuro, previa notificación fehaciente al contratista.

El contratista queda obligado a emitir las facturas que correspondan de conformidad con la legislación vigente.

[OPCIONAL — incluir si procede]

(En caso de que así se haya pactado, en especial en el arrendamiento de obra sin suministro de materiales)

Quinta.- Gastos

El contratista se hará cargo de todos los gastos que se devenguen como consecuencia de la ejecución de la obra objeto de este contrato: materiales, otros bienes o servicios que resulten necesarios para el correcto desarrollo de los trabajos, tasas e impuestos que se devenguen por la ejecución de la obra, etc.

Sexta.- Obligaciones del contratista

El contratista ejecutará la obra de acuerdo con las previsiones de este contrato, ajustándose al presupuesto y a los plazos acordados por las partes y adquiriendo y aportando los materiales necesarios para su correcto desarrollocon la supervisión del comitente.

El contratista mantendrá debidamente informado al comitente de la marcha de las obras así como de todas las incidencias que se produzcan, sean o no imputables al primero.

El contratista entregará la obra al comitente al término de su ejecución, en el/los plazo/s previsto/s.

El contratista se obliga a respetar las previsiones de este contrato así como la legislación vigente que le es de aplicación, especialmente en materia laboral y de Seguridad Social y [OTROS DATOS].

Séptima.- Incumplimiento por el contratista

Si el contratista no respetara los plazos previstos en la cláusula tercera y en el plan adjunto como Anexo 2 quedará obligado a pagar, en concepto de penalización por cada día de retraso, la cantidad de [IMPORTE] euros / día.

Octava.- Obligaciones del comitente

El comitente queda obligado a satisfacer el/los pago/s previstos en el contrato en los plazos establecidos.

El comitente queda obligado a colaborar con el contratista para la correcta ejecución de la obra y a facilitarle toda la información útil y relevante de que disponga para el mejor desarrollo de los trabajos así como sobre las necesidades que precisa en cuanto a la obra contratada.

Novena.- Incumplimiento por el comitente

Si el comitente se retrasara en el pago de la obra, éste se verá incrementado en un [Nº] por ciento, en concepto de interés de demora.

Si el comitente no facilitara al contratista información relevante para el desarrollo de la obra, este último podrá notificar fehacientemente al comitente la imposibilidad de cumplir con los plazos establecidos para la ejecución de la obra.

Décima.- Recepción y entrega de la obra

[ELEGIR UNA OPCIÓN: En caso de entrega única / En caso de entregas parciales]

Undécima.- Garantía

El contratista se compromete a [Nº] meses de garantía, tanto de la obra propia como de los trabajos subcontratados, y durante este período todos los defectos de la construcción, así como los daños a terceros que pudieran aparecer motivados por la misma, serán inmediatamente reparados por cuenta de éste.

La garantía no será de aplicación si el comitente no abonara el precio al contratista o si aquél resolviera el contrato por cualquier causa.

Duodécima.- Resolución

El contrato podrá resolverse por mutuo acuerdo de las partes o si concurre alguna de las siguientes circunstancias:

Si cualquiera de las partes incumpliera, total o parcialmente, alguna de las obligaciones esenciales del contrato, la parte afectada por tal incumplimiento le requerirá fehacientemente para su subsanación. Transcurrido el plazo de [PLAZO] desde dicho requerimiento sin que se haya corregido la causa del incumplimiento, la parte afectada por éste podrá resolver el contrato.

Si en el plazo de [PLAZO] desde la firma del presente el contratista apreciara que el cumplimiento del contrato fuera imposible por [CAUSA], se lo notificará fehacientemente al comitente, quedando resuelto el contrato sin que el comitente tenga derecho a reclamar indemnización alguna.

Decimotercera.- Fuerza mayor

No se considerará retraso en el cumplimiento del contrato ni incumplimiento de la ejecución por las partes si concurrieran causas de fuerza mayor. En todo caso, la parte incumplidora por este motivo habrá de notificárselo inmediata y fehacientemente a la parte afectada por el incumplimiento.

Se entiende que concurre fuerza mayor en los siguientes supuestos: fenómenos meteorológicos que impidan el desarrollo de los trabajos, inundación, incendio, huelga, requerimiento de la Administración Pública o cualquier otro que, quedando fuera de la esfera de control de la parte afectada, impida el cumplimiento de las obligaciones pactadas en este contrato.

En cualquier caso, la parte afectada por la fuerza mayor queda obligada a hacer todo lo posible por evitarla, superarla o eliminarla. Una vez finalizada la causa de fuerza mayor que determine la imposibilidad de desarrollar los trabajos, la parte afectada por aquélla dispondrá de [PLAZO] para [ACTUACIÓN A REALIZAR].

Decimocuarta.- Responsabilidad

El contratista ejecutará la obra de acuerdo con la diligencia que le es exigible y con la legislación vigente en cada momento; en particular, las normas civiles, laborales, de Seguridad Social y de construcción.

El contratista será responsable de los daños causados al comitente y/o a terceros como consecuencia de sus infracciones en la ejecución de la obra, sin que pueda considerarse responsabilidad del contratista los perjuicios que sufra el comitente por utilización de la obra no conforme con su finalidad o con las instrucciones o recomendaciones del contratista.

[OPCIONAL — incluir si procede]

(La confidencialidad es un pacto opcional de este contrato)

Decimoquinta.- Confidencialidad

Las partes se comprometen a mantener confidencial toda la información que conozcan, compartan y se comuniquen en relación con la obra, durante la ejecución de ésta y, una vez finalizada, durante un plazo de [PLAZO].

A la finalización de la obra, las partes se devolverán o destruirán la información que hayan percibido de la otra.

No se considera información confidencial aquélla que sea de dominio público o la que las partes tuvieran antes de haberle sido facilitada por la otra parte.

Decimosexta.- Domicilio a efectos de notificaciones

Las comunicaciones que las partes hayan de remitirse en virtud de este contrato se realizarán por cualquier medio fehaciente admitido en Derecho a las siguientes direcciones que comitente y contratista dejan designadas a tal efecto:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Contratista [NOMBRE DE LA PARTE], con domicilio en [LOCALIDAD] y mail [CORREO ELECTRÓNICO]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Comitente [NOMBRE DE LA PARTE], con domicilio en [LOCALIDAD] y mail [CORREO ELECTRÓNICO]

Las partes pueden modificar los domicilios señalados advirtiéndoselo fehacientemente a la otra y facilitándole los nuevos datos.

Decimoséptima.- Legislación aplicable y fuero

Este contrato se rige por las cláusulas recogidas en el presente y, en lo no previsto por él, se atenderá a las previsiones del Código Civil.

[ELEGIR UNA OPCIÓN: En caso de no sometimiento a arbitraje / En caso de sometimiento a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

Arrendador o contratista

________________________________

Arrendatario o comitente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

Anexo 1. Presupuesto

Anexo 2. Calendario de plazos y entregas

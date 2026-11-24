---
name: arrendamiento-empresa-negocio-industria-contrato-mer-0823
description: "Arrendamiento de empresa, negocio o industria (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Arrendamiento de empresa, negocio o industria (contrato)

> Formulario **MER-0823** del plugin **Traspasos de negocio, confidencialidad y acuerdos de empresa** (`formularios-traspasos-y-acuerdos-de-empresa`) · Mercantil › Otros documentos mercantiles · normativa revisada el 24-11-2026.

## Qué es

Por el contrato de arrendamiento de empresa (también denominado industria o negocio), el titular cede a otra empresa o empresario el uso o explotación de su empresa por tiempo determinado y mediante el abono de una contraprestación monetaria.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Arrendamiento de empresa, negocio o industria (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Arrendamiento de empresa, negocio o industria (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-traspasos-y-acuerdos-de-empresa:arrendamiento-empresa-negocio-industria-contrato-mer-0823`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-traspasos-y-acuerdos-de-empresa:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Traspasos de negocio, confidencialidad y acuerdos de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] Nº (8 veces)
- [ ] DNI/NIE (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] PLAZO (2 veces)
- [ ] DIRECCIÓN
- [ ] ENTIDAD BANCARIA
- [ ] FECHA
- [ ] LUGAR
- [ ] NOMBRE DEL NEGOCIO
- [ ] Nº DE ANEXO
- [ ] Nº DE CUENTA (IBAN)
- [ ] PORCENTAJE

## Normas que cita el formulario

- art. 32.4 LAU

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

Por el contrato de arrendamiento de empresa (también denominado industria o negocio), el titular cede a otra empresa o empresario el uso o explotación de su empresa por tiempo determinado y mediante el abono de una contraprestación monetaria.


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

En lo sucesivo, ARRENDADOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ARRENDATARIO.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de arrendamiento de empresa, negocio o industria y, a tal fin,

MANIFIESTAN

I. Que el arrendador [NOMBRE DE LA PARTE] dice ser propietaria de un negocio de [ACTIVIDAD] denominado [NOMBRE DEL NEGOCIO], que se desarrolla en un local comercial situado en [DIRECCIÓN]

II. Que dicho negocio está integrado por el inmueble mencionado en el apartado anterior, así como por [DESCRIPCIÓN DEL BIEN] mencionados en el inventario que los contratantes han elaborado de mutuo acuerdo en documento que se adjunta al presente como Anexo [Nº DE ANEXO],

III. Que el Arrendatario está interesado en llevar a cabo la explotación de dicho negocio.

IV. Que el Arrendador y el Arrendatario han alcanzado un acuerdo en virtud del cual se someten a las siguientes

CLÁSULAS

Primera.- Objeto

El arrendador arrienda al arrendatario por este contrato el negocio, industria o empresa, recibiéndola éste en perfectas condiciones y a su entera satisfacción

[OPCIONAL — incluir si procede]

(Si el negocio o industria estuviese ubicado en un local arrendado)

El arrendador asume la obligación de notificar fehacientemente al arrendador del local donde se halla instalada la industria el presente contrato a los efectos del art. 32.4 LAU

[ELEGIR UNA OPCIÓN: Compra de mercancías / Cesión o arrendamiento de mercancías]

Segunda.- Renta

El precio del arrendamiento descrito en la cláusula primera se concreta en la cantidad de [IMPORTE] euros más el Impuesto sobre el Valor Añadido correspondiente al %, esto es, ( euros) adicionales. Más una parte variable que consistirá en el % del volumen de facturación mensual neta. El precio total de la operación asciende a la cantidad de [IMPORTE] € ( euros).

Dicha cantidad no incluye (Salvo el IVA) los impuestos, tasas, precios públicos y licencias, tanto municipales como estatales o autonómicas que recaigan sobre la actividad, ni los consumos de gas, electricidad, teléfono, agua así como cualquier otro impuesto, suministro o servicio necesarios para el ejercicio de la misma. Los consumos que fueren abonados por los anteriores conceptos por el arrendador serán pasados al cobro al arrendatario junto con la renta mensual.

La renta deberá ser satisfecha anticipadamente por el arrendatario durante los [Nº] primeros días de cada mes en la cuenta [Nº DE CUENTA (IBAN)], de la que es titular el arrendador en banco [ENTIDAD BANCARIA], ubicad en

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho al arrendador a exigir al arrendatario un interés moratorio del [PORCENTAJE] % respecto de cada uno de los pagos no satisfechos puntualmente. Si el arrendatario se retrasara en el pago de [Nº] mensualidades, la arrendadora podrá optar entre exigir el pago de los plazos pendientes o resolver el contrato, con abono en ambos casos de las indemnizaciones que puedan corresponder.

[OPCIONAL — incluir si procede]

(Actualización)

La renta se actualizará por el Arrendador anualmente, de acuerdo con las variaciones que experimente durante el año precedente, IPC. La renta actualizada será exigible a la arrendataria a partir del mes siguiente a aquél en que la arrendadora se lo notifique por escrito y expresando el porcentaje de alteración aplicado. Se considerará valida la notificación hecha mediante anotación en el recibo de la mensualidad precedente.

Tercera.- Fianza

El arrendatario entrega al arrendador la cantidad de [IMPORTE] euros ( €) en concepto de fianza. Esta fianza deberá ser restituida en su integridad, o descontando la cantidad que sea necesaria para reponer [DESCRIPCIÓN DEL BIEN] en las condiciones óptimas para el desempeño de la actividad descrita.

[OPCIONAL — incluir si procede]

(Cuando el arrendador es propietario del local)

El arrendatario entrega al arrendador la cantidad de [IMPORTE] euros, equivalente a mensualidades de la renta correspondiente al local, en concepto de fianza para responder del cumplimiento de la renta, así como de los deterioros o perjuicios que se hubieran producido en la finca por su culpa o la de las personas que trabajen en la empresa. El presente contrato sirve de recibo acreditativo de dicha entrega.

[OPCIONAL — incluir si procede]

(Fiador solidario)

Por el cumplimiento de las obligaciones del presente contrato responde D./Dña. [NOMBRE Y APELLIDOS] solidariamente con el arrendadorio, como fiador, incluso tras las sucesivas prórrogas del contrato.

[OPCIONAL — incluir si procede]

(Aval)

Para responder del pago de las rentas, el Arrendatario entrega al Arrendador, en el momento de la firma del presente contrato, aval bancario a primer requerimiento sin derecho a los beneficios de excusión o división, por el importe de meses de renta, incluido el I.V.A. correspondiente. Dicho aval estará vigente por el tiempo que dure el presente contrato.

Cuarta.- Duración

El presente contrato entrará en vigor el y se concierta por un período de [Nº] años. Llegado el vencimiento el Contrato se entenderá tácitamente prorrogado por tácita reconducción, por períodos de [PLAZO], si no hubiera mediado requerimiento escrito por cualquiera de las partes al menos con [Nº] días de anticipación respecto del vencimiento del plazo inicialmente pactado o de la correspondiente prórroga.

[OPCIONAL — incluir si procede]

(Si se pacta duración mínima)

No obstante, transcurridos los primeros [Nº] meses, cuyo plazo es de duración obligatoria para el arrendatario, éste podrá rescindir el contrato anticipadamente, sin esperar a su finalización, siempre y cuando lo notifique fehacientemente al arrendador con un preaviso mínimo de [Nº] meses de antelación a la fecha de desalojo, viniendo obligado a abonar el recibo de alquiler hasta la fecha de desalojo y entrega de llaves.

Quinta.- Gastos de mantenimiento

El Arrendador se obliga a llevar a cabo todas las reparaciones que sean necesarias para mantener el establecimiento mercantil en perfecto funcionamiento, incluidas las que deban hacerse en el local donde éste está ubicado.

Serán de cuenta del arrendatario todas las contribuciones, impuestos y arbitrios estatales o municipales que graven el negocio o industria instalado en ella. Los que graven el inmueble serán de cuenta del arrendador.

[OPCIONAL — incluir si procede]

(Propiedad horizontal)

También serán de cuenta del arrendatario el pago de los gastos comunes del edificio en régimen de propiedad horizontal donde se hallase ubicado el local del negocio arrendado.

Sexta.- Suministros

El Arrendatario será responsable del abono de los servicios de abastecimiento y consumo de agua, electricidad, teléfono, gas o de cualquier otro servicio que se pudiera medir por contador, con los que cuenta la empresa o pueda contar en el futuro el establecimiento mercantil arrendado, debiendo llevar a cabo los correspondientes cambios de titularidad de aquéllos durante el tiempo que dure el contrato, y siendo de su cargo los gastos que origine dicho cambio

Séptima.- Cesión de trabajadores

El arrendatario queda subrogado en los derechos y obligaciones laborales y de la seguridad social del arrendador, incluyendo los compromisos de pensiones y, en general, cuantas obligaciones en materia de protección social complementaria hubiera adquirido el arrendador.

Octava.- Destino del negocio u empresa

El negocio objeto de este contrato será destinado a [ACTIVIDAD], sin que pueda el arrendatario variar o ampliar dicha actividad sin contar con el consentimiento expreso y escrito del arrendador.

Dicho consentimiento deberá ser requerido con [PLAZO] de antelación a las modificaciones, quedando a cuenta del arrendatario los gastos para el acondicionamiento del local, así como la obtención de los permisos necesarios para el cambio o ampliación de la actividad siempre que lo permitan los estatutos de la Comunidad de Propietarios del edificio donde se hallara ubicado el local del negocio arrendado.

[OPCIONAL — incluir si procede]

(Si se trata de una empresa)

El Arrendatario no podrá modificar el objeto de la empresa arrendada, que deberá dedicarse a la actividad que se describe durante todo el tiempo en que esté vigente el presente contrato.

Novena.- No competencia

[OPCIONAL — incluir si procede]

(Por parte del arrendador)

El arrendador se compromete a no realizar durante la vigencia del presente contrato actividades por cuenta propia o ajena que de algún modo pudieran suponer competencia para el arrendatario.

Del mismo modo, durante la vigencia del presente contrato el arrendador no podrá adquirir participación ni derecho alguno en negocios o empresas que desarrollen una actividad concurrente con la del arrendatario, ni participar, activa o pasivamente, en ningún tipo de gestión conducente al desarrollo de este tipo de actividades.

El incumplimiento de este compromiso conllevará la obligación de indemnizar los daños y perjuicios causados.

[OPCIONAL — incluir si procede]

(Por parte del arrendatario)

Durante un periodo de [Nº] años a contar desde la extinción del presente contrato, el arrendatario se compromete a no realizar actividades por cuenta propia o ajena que de algún modo pudieran suponer competencia para el arrendador.

Del mismo modo, durante la vigencia del presente contrato el arrendatario no podrá adquirir participación ni derecho alguno en negocios o empresas que desarrollen una actividad concurrente con la del arrendador, ni participar, activa o pasivamente, en ningún tipo de gestión conducente al desarrollo de este tipo de actividades.

El incumplimiento de este compromiso conllevará la obligación de indemnizar los daños y perjuicios causados.

Décima.- Cesión o subarriendo

El arrendatario renuncia de forma expresa a su derecho de subrogar, ceder o subarrendar (total o parcialmente) la empresa objeto de este contrato.

Decimoprimera.- Confidencialidad

El arrendatario se obliga a no revelar, ceder o transferir a terceros ninguna información referente a los negocios, clientes, operaciones, instalaciones, cuentas o finanzas del a arrendador, ni sus procedimientos, métodos, transacciones, "know-how", o cualquier otro aspecto relacionado con la actividad de dicha entidad que pueda conocer o haya conocido con motivo de la prestación de servicios prevista en el presente contrato.

El arrendatario se responsabilizará de que las personas que están a su cargo se sujeten a las limitaciones establecidas en esta cláusula.

El incumplimiento de este compromiso conllevará la obligación de indemnizar los daños y perjuicios causados.

Decimosegunda.- Obras

La realización de cualquier obra en el establecimiento mercantil queda supeditada a la autorización previa y expresa del Arrendador. Quedan excluidas aquéllas obras de reparación cuya realización no admita demora sin perjuicio para el establecimiento mercantil arrendado. En todo caso, cuantas obras se realicen con la debida autorización quedarán en beneficio del establecimiento mercantil sin desembolso alguno por parte del Arrendador.

Decimpotercera.- Formalización

Cualquiera de las partes podrá elevar a escritura pública este contrato e inscribirlo en el Registro de la Propiedad siendo los gastos, que esta elevación a público e inscripción conlleve, asumidos por la Parte que lo promueva.

Decimocuarta.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Decimoquinta.- Protección de datos personales

Las Partes de este Contrato conocen y se obligan a cumplir la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales y consienten la incorporación de sus datos personales en el fichero automatizado de la contraparte.

1Decimosexta- Gastos e Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta del [NOMBRE DE LA PARTE].

Decimoséptima.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones Código de Comercio, leyes especiales y usos mercantiles que le sean aplicables, o en lo no previsto, por las disposiciones del Código Civil.

Decimoctava.- Fuero competente

[ELEGIR UNA OPCIÓN: Si se pacta acudir a tribunales / Si se pacta acudir a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

EL ARRENDADOR

________________________________

EL ARRENDATARIO

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

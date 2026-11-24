---
name: contrato-servicios-handling-mer-0532
description: "Contrato de servicios de handling. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicios de handling

> Formulario **MER-0532** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicios de handling» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicios de handling” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-servicios-handling-mer-0532`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (11 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] PROVINCIA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] INSCRIPCIÓN (2 veces)
- [ ] NIF (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] AEROPUERTO
- [ ] AÑO
- [ ] DÍA
- [ ] MES
- [ ] Nº
- [ ] Nº DE AERONAVES
- [ ] NÚMERO

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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NÚMERO].

Y de otra parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA] provisto/a del N.I.F..

INTERVIENEN

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF [NIF], domiciliada en [DOMICILIO] y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA] e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], en adelante el USUARIO

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF [NIF], domiciliada en [DOMICILIO] y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA] e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], en adelante el OPERADOR

MANIFIESTAN

Que intervienen en la representación expresada y se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE ASISTENCIA EN TIERRA ( HANDLING), asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que el USUARIO es una entidad que ostenta la titularidad de [Nº DE AERONAVES] aeronaves, estando interesada un servicio de handling para el normal desarrollo de las actividades aéreas de sus aeronaves cuando operen desde el aeropuerto de

II. Que el OPERADOR es una persona jurídica que brinda servicios de handling a terceros; los cuales incluyen a actividades tales como la atención que se presta a las aeronaves en tierra referidas a la carga, descarga, manipulación, estiba de equipajes y mercaderías, servicios de limpieza exterior e interior, suministro corriente eléctrica, refrigeración y calefacción para puesta en servicio aeronave, provisión de agua, catering a bordo, eliminación de basura y aguas negras.

III. Que estando interesadas ambas partes convienen la celebración de un contrato de hangling, con sujeción a las siguientes

CLÁUSULAS

Objeto del contrato

El OPERADOR prestará los servicios de handling para la flota de aeronaves del USUARIO en el aeropuerto de [AEROPUERTO], comprendiendo los siguientes servicios:

– Suministro corriente eléctrica, refrigeración y calefacción para puesta en servicio aeronave.

– Limpieza exterior e interior del avión para puesta en servicio aeronave.

– “Catering a bordo de avión” - Suministro alimento a bordo de avión

– Servicios de apoyo a la tripulación: Traslado de tripulación desde plataforma aeroportuaria hasta lugar de alojamiento.

– Trabajos de carga y descarga de cualquier material transportado a bordo.

()

El programa de trabajo estimado, conteniendo las tareas y frecuencias a realizar, así como las actividades, se incluye como Anexo I de este contrato.

Duración

El plazo de duración del contrato será de años computados desde la firma del presente documento.

El contrato podrá ser prorrogado por mutuo acuerdo de las partes por iguales periodos.

La prórroga se entenderá tácita si ninguna de las partes manifiesta su voluntad en contra, a cuyo efecto deberá formular un preaviso con [Nº] meses de antelación al de la fecha de vencimiento del contrato.

Precio

Como contraprestación se fija un precio estimado anual de [IMPORTE] euros más el [PORCENTAJE] % de I.V.A. (un total de [IMPORTE] euros).

El OPERADOR tiene derecho al abono de los trabajos o servicios efectivamente realizados y formalmente recibidos por el USUARIO con arreglo a las tablas de precios que se recogen en el Anexo II de este contrato en el que se desglosa el precio unitario de cada trabajo o servicio contratados.

El USUARIO abonará al OPERADOR el precio por meses vencidos y contra factura girada por éste, en la que se incluirá el correspondiente IVA.

En caso que la facturación anual no alcanzará el [PORCENTAJE] % del precio estimado, el USUARIO abonará la diferencia hasta alcanzar dicha cantidad en concepto de mínimo anual.

Obligaciones del operador

El OPERADOR se compromete y obliga a cumplir el contrato de forma diligente, y especialmente a:

– A realizar los trabajos, prestaciones y servicios con la calidad técnica exigible, respondiendo de los perjuicios que se deduzcan para el USUARIO o para terceros, derivados de las omisiones, errores, métodos inadecuados o conclusiones incorrectas producidas en la ejecución del contrato.

– A ajustarse a las instrucciones del USUARIO para la calidad de los trabajos, con sujeción a las facultades de inspección y control inherentes al USUARIO.

– A obtener las autorizaciones y licencias necesarias para prestar los servicios de asistencia en tierra contratados en instalaciones aeroportuarias.

– A cumplir las obligaciones laborales, sociales y de prevención de riesgos del personal a su servicio.

– A suscribir las pólizas de seguro necesarios que cubran los daños derivados de la ejecución de los trabajos correspondientes a los servicios contratados.

Obligaciones del usuario

El USUARIO se compromete y obliga asimismo a cumplir el contrato de forma diligente, y especialmente a:

– Al pago del precio convenido en los términos pactados.

– A facilitar el acceso del OPERADOR a sus instalaciones y aeronaves a los efectos de la correcta ejecución de los trabajos.

– A dar detallada información detallada al OPERADOR sobre los pormenores de sus operaciones en las instalaciones aeroportuarias y mantenerle al día de las modificaciones

– A comunicar cualquier circunstancia imprevista, modificativa o impeditiva con relevancia en la ejecución del contrato.

Modificaciones contractuales

Ambas partes podrán modificar de mutuo acuerdo las condiciones pactadas.

Asimismo, podrán acordarse suspensiones en la ejecución, de carácter temporal, total o parcial, cuando ambas partes así lo convenga.

Extinción y resolución del contrato

El contrato se extinguirá por el transcurso del plazo o de cualquiera de sus prórrogas.

El contrato se resolverá anticipadamente por incumplimiento grave de las obligaciones de las partes, imposibilidad sobrevenida de cumplimiento, o por la suspensión, rescisión o revocación de las licencias o autorizaciones del OPERADOR para la prestación de servicios de asistencia en tierra en instalaciones aeroportuarias.

En el caso de resolución anticipada imputable a una de las partes, la parte incumplidora deberá indemnizar a la contraparte por los daños y perjuicios derivados de la resolución.

Comunicaciones y notificaciones

El OPERADOR proporciona como dirección para recibir cualquier demanda de servicio o de apoyo operacional la siguiente:

()

El OPERADOR se compromete a atender las peticiones del USUARIO durante las 24 horas en el teléfono móvil y dirección de correo electrónico

El USUARIO designa como domicilio para notificaciones el indicado en el encabezamiento de este contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Cláusula de sumisión

(pacto de sumisión expresa) Las partes, con renuncia expresa al fuero que pudiera corresponderles, se someten para todas las cuestiones dimanantes del presente contrato a los Tribunales de la localidad de

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato al que se incorporan los anexos expresados como parte integrante de su contenido, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

EL USUARIO

Fdo.

EL OPERADOR

Fdo.

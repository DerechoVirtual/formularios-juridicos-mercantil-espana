---
name: mantenimiento-instalaciones-frigorificas-contrato-mer-0556
description: "Mantenimiento de instalaciones frigoríficas (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Mantenimiento de instalaciones frigoríficas (contrato)

> Formulario **MER-0556** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Mantenimiento de instalaciones frigoríficas (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Mantenimiento de instalaciones frigoríficas (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:mantenimiento-instalaciones-frigorificas-contrato-mer-0556`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PLAZO (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] PORCENTAJE

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

[ELEGIR UNA OPCIÓN: Intervienen / Si intervienen en nombre y representación de alguien / Opción 1: Si intervienen en nombre y representación de alguien / Si intervienen en su propio nombre y derecho / Opción 2: Si intervienen en su propio nombre y derecho]

EXPONEN

Que ambas partes se encuentran interesadas en el mantenimiento de las Instalaciones supra referidas, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

El CLIENTE contrata con el PROVEEDOR el servicio de mantenimiento de las instalaciones de refrigeración descritas en el Anexo 1 de este mismo contrato, conforme a las especificaciones técnicas solicitadas por el CLIENTE y la propuesta del PROVEEDOR.

El servicio de mantenimiento incluye:

1. Mantenimiento preventivo programado: Este servicio está basado en las necesidades específicas de cada máquina, equipo y dispositivo en particular, según lo determinado en la hoja técnica señalada en el Anexo 2. El mantenimiento preventivo programado será ejecutado durante los períodos seleccionados de común acuerdo entre las dos partes

2. Mantenimiento no programado "correctivo": Hecho sobre la base de llamadas, incluye: ajustes, reparaciones, cambio de elementos y piezas inservibles y/o deterioradas. Todas las actuaciones no programadas serán facturadas según las tarifas vigentes del PROVEEDOR, tanto les piezas y materiales, como la mano de obra y los desplazamientos.

El servicio de mantenimiento no incluye:

1. Trabajos eléctricos externos a las máquinas o mantenimiento de accesorios, dispositivos u otros no suministrados por el PROVEEDOR.

2. Reparación de daños o incremento de tiempos de servicio causado por: accidentes, transporte, negligencia o mal uso, alteraciones, incluyendo entre otros: desviaciones del diseño estructural o de circuitos, instalación o desmontaje de dispositivos o cualquier otra modificación que no esté autorizada por el PROVEEDOR.

3. Reparación de daño o incrementos de tiempos de servicio causados por variaciones en el suministro de la energía eléctrica.

4. Suministro de piezas susceptibles a desgaste por el uso, pintura o retocado de las máquinas o el suministro de materiales para estas operaciones; hacer cambios de especificaciones o servicios relacionados con la reubicación de las máquinas o añadir y/o sacar accesorios, anexos y otros dispositivos.

5. Cualquier servicio donde los técnicos del PROVEEDOR se encuentre imposibilitados de realizar, por causa de alteraciones en las máquinas, accesos o su conexión por medios eléctricos o mecánicos a otras máquinas.

Precio

El pago se efectuará de acuerdo a lo convenido con el PROVEEDOR. El precio puede ser reajustado por PROVEEDOR previo aviso escrito con [Nº] días de antelación, a la facturación con la nueva tarifa.

Los pagos que cubren los servicios realizados fuera de los períodos de servicio previstos en este contrato así como aquellos que no son el objeto de este contrato serán facturados separadamente en base a las tarifas vigentes del PROVEEDOR.

Los gastos de transporte así como todos los gastos ocasionados por desplazamientos excepcionales y que no están incluidos en los servicios del presente contrato, serán facturados al CLIENTE separadamente.

Comienzo del contrato

Antes de la firma de este contrato, el PROVEEDOR efectuará una revisión preventiva a los equipos frigoríficos de propiedad del CLIENTE, a fin de determinar los servicios a prestar

Si de esta revisión se determina una actuación en los equipos que se han de mantener en este contrato, la faena se realizará antes de la contratación de este servicio.

Tanto la revisión inicial, como la faena para la adecuación de los equipos, se facturarán a parte, según la tarifa vigente del PROVEEDOR.

Condiciones del servicio

El cliente puede solicitar la prestación de los servicios previstos en el presente contrato des de la firma del mismo. Así mismo puede hacer un pedido de prestación de servicios complementarios, añadir o suprimir los productos que son el objeto del presente contrato.

Las solicitudes para realizar el mantenimiento correctivo no programado a los equipos frigoríficos se harán una vez que el CLIENTE indique la avería al PROVEEDOR, mediante el teléfono de servicio, fax o e-mail, indicando perfectamente el tipo avería, la máquina afectada y la urgencia en el tiempo.

Si pasa algún desperfecto en los equipos objeto del contrato, el CLIENTE lo comunicará inmediatamente al PROVEEDOR y le facilitará acceso pleno y libre a los Equipos Frigoríficos bajo las condiciones de seguridad establecidas por el CLIENTE. El PROVEEDOR tendrá que acatar y cumplir en su faena las normas de seguridad industrial del CLIENTE.

Condiciones de funcionamiento

V.1.Condiciones Ambientales y Eléctricas:

Las condiciones ambientales se ajustarán estrictamente a las especificaciones subministradas por el PROVEEDOR y señaladas en las placas de características de cada máquina, tanto en temperatura y humedad como en especificaciones de tolerancias eléctricas. El uso de los Equipos Frigoríficos bajo condiciones diferentes a las especificadas, puede ser motivo de suspensión de este contrato en tanto no sean corregidas. Después de una inspección de los equipos, la corrección de los problemas ocasionado por estas causas, serán facturados en base de tiempos y materiales antes de reiniciar el contrato de mantenimiento, según la tarifa vigente del PROVEEDOR.

V.2 Modificaciones estructurales:

Sin tocar ninguna máquina se pueden hacer modificaciones estructurales, tanto en el lugar de los servicios frigoríficos como en la sala de máquinas. Estas modificaciones, aun que parezcan que no son estrictamente frigoríficas, pueden ocasionar malfuncionamientos o desperfectos en la seguridad de la instalación. Cualquier modificación estructural que se haga en el local se ha de informar al PROVEEDOR para su examen.

V.3 Acceso a las máquinas:

El personal técnico del PROVEEDOR tendrá libre y completo acceso a los lugares donde se encuentres ubicadas las máquinas y dispositivos de acuerdo a las normas de seguridad establecidas por el CLIENTE para proveer los servicios contemplados en este contrato.

Igualmente, el CLIENTE, facilitará los medios necesarios para el acceso a sus equipos. Los medios (escaleras, elevadores, etc.) serán totalmente homologados y de acuerdo con la normativa vigente de seguridad.

Duración del contrato

La duración de este contrato será de [PLAZO] y cesará automáticamente llegada la fecha de su finalización, siempre que al menos una de las partes así lo manifestare con una antelación mínima de

Si no se produjese tal preaviso, se entenderá prorrogado por un período de [PLAZO]

Resolución del contrato

El incumplimiento de las obligaciones que resulten del presente contrato facultará a la parte que cumpla los suyos a exigir a la otra su cumplimiento, o, a su elección, a resolver el contrato, con abono en ambos casos de la indemnización por daños y perjuicios que proceda.

Honorarios del mediador

En este arrendamiento ha intervenido como mediador la entidad [DENOMINACIÓN SOCIAL]

Mediante el presente contrato se fijan los honorarios por la intervención de la referida entidad en el [PORCENTAJE] % de la renta de un año.

El precio fijado se pagará por la parte EMPRESA DE MANTENIMIENTO y por la CONTRATISTA por mitad e iguales partes.

Jurisdicción competente y ley aplicable

El conocimiento de los litigios relativos a que diera lugar la interpretación y/o ejecución del presente contrato corresponderá al Tribunal de Instancia del lugar en que se halle la finca.

El presente contrato tiene carácter civil, se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código Civil y demás leyes especiales.

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE MANTENIMIENTO DE INSTALACIONES FRIGORÍFICAS, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La EMPRESA DE MANTENIMIENTO)

Fdo. Don [NOMBRE Y APELLIDOS]

(La CONTRATISTA)

---
name: contrato-ensenanza-conduccion-autoescuela-mer-0562
description: "Contrato de enseñanza de conducción con autoescuela. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de enseñanza de conducción con autoescuela

> Formulario **MER-0562** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de enseñanza de conducción con autoescuela» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de enseñanza de conducción con autoescuela” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-ensenanza-conduccion-autoescuela-mer-0562`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE MINUTOS
- [ ] TIPO DE PERMISO

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

[ELEGIR UNA OPCIÓN: Intervienen / SI intervienen en nombre y representación de alguien / Opción 1: Si intervienen en nombre y representación de alguien / Si intervienen en su propio nombre y derecho / Opción 2: Si intervienen en su propio nombre y derecho]

EXPONEN

Que LA AUTOESCUELA se dedica a [ACTIVIDAD]

Que EL ALUMNO se encuentra interesado en contratar los servicios de la AUTOESCUELA de cara a la obtención del permiso de conducir tipo [TIPO DE PERMISO] por lo que ambas partes de común acuerdo llevan a efecto el presente CONTRATO DE ENSEÑANZA PARA LA FORMACIÓN Y ADIESTRAMIENTO EN LA CONDUCCIÓN DE AUTOMÓVILES, para los que es necesario el permiso de la clase indicada a continuación:con arreglo a las siguientes:

CLÁUSULAS

Objeto

La Escuela impartirá las enseñanzas necesarias para la obtención del permiso de conducción reseñado, con la máxima dedicación y eficacia, y con el profesorado que cumpla todos los requisitos exigidos en el Reglamento de Escuelas Particulares de Conductores. Real Decreto 1295/2003 de 17 de octubre. (B.O.E. 28/10/2003)

Precio

Las condiciones económicas del presente contratos son las siguientes:

a) EXAMEN PRÁCTICO DE MANIOBRAS [IMPORTE]: euros más I.V.A.

b)CLASES TEÓRICAS: [IMPORTE] euros más I.V.A. por cada módulo de [Nº] minutos

c)Tasa de Tráfico vigente a la firma del contrato: [IMPORTE] euros

d)EXAMEN PRÁCTICO DE CIRCULACIÓN: [IMPORTE] euros más I.V.A.

e)CLASES PRÁCTICAS DE CIRCULACIÓN: [IMPORTE] euros más I.V.A. por cada módulo de [Nº DE MINUTOS] Gminutos

Los gastos de tramitación por el segundo expediente y sucesivos, si hubiera lugar, serán de [IMPORTE] euros (más I.V.A.)

Los gastos de inscripción en la Escuela se abonarán por una sola vez, independientemente del número de convocatorias necesarias para la obtención del permiso solicitado.

El alumno abonará a la Autoescuela, anticipadamente, los importes de todos los servicios recibidos antes del examen.

Gestión de documentos

La gestión en los Centros oficiales de cuantos documentos interesen dichos centros para obtener el permiso de conducción será realizada por la autoescuela o el alumno (según autorización).

Siendo el importe de los mismos los señalados en el apartado de condiciones económicas de este contrato. Real Decreto 1295/2003 de 17 de Octubre, artículo 1.3.

Clases

El alumno deberá asistir a las clases prácticas a la hora convenida. Si no asiste vendrá obligado a preavisar con 24 horas de antelación, salvo causa de fuerza mayor. La ausencia a dos clases prácticas consecutivas, salvo en casos de fuerza mayor justificada, puede llevar consigo la supresión del Profesor y el vehículo asignados.

La Autoescuela deberá avisar al alumno con 24h de antelación sobre la supresión de la clase en el caso de que el profesor no pueda acudir a la cita, salvo que concurra caso de fuerza mayor, facilitando la recuperación de la clase suprimida a la mayor brevedad posible.

Examen

Salvo casos debidamente justificados y autorizados por la Jefatura de Tráfico, el alumno será acompañado durante la prueba de circulación por el Profesor que le haya impartido la enseñanza práctica, que se responsabilizará del doble mando.

Las fechas de convocatoria de examen del alumno serán fijadas por la Jefatura Provincial de Tráfico a petición del interesado en función de la capacidad de examen de esta.

Cambio de profesor o vehículo

La Autoescuela se reserva el derecho de cambio de profesor o vehículo por causa de fuerza mayor.

Renuncia del contrato

Si el alumno renunciase a la obtención del permiso de conducción contratado abonará todo lo adeudado hasta entonces, excepción hecha de las TASAS OFICIALES siempre que éstas no hubiesen sido desembolsadas en su nombre ante el Organismo correspondiente.

Terminación del contrato

El contrato terminará por las siguientes causas:

a) Obtención del permiso para cuyo fin se contrató la enseñanza.

b) No inicio o suspensión de la enseñanza por un plazo de dos meses, seguidos o tres meses alternos, salvo causa de fuerza mayor debidamente justificada.

c) Por incumplimiento de las obligaciones por parte del alumno: (Falta de pago o no aportación de documentos).

d) Por mutuo acuerdo de las partes. Estableciendose las condiciones económicas resultantes de la ruptura de dicho contrato.

e) Transcurridos [Nº] meses de la fecha del presente contrato y el alumno no hubiera obtenido el permiso de conducción pretendido por causas ajenas a la Autoescuela. En el caso de caducidad del contrato el alumno no volverá a pagar, en ningún caso, el importe de inscripción en la Autoescuela. En todo caso, se abonará el resto de servicios que se hubieran prestado.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia del evento, así como la obtención de las licencias y permisos necesarios para su celebración serán de cargo de la parte arrendataria.

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

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

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE ENSEÑANZA PARA LA FORMACIÓN Y ADIESTRAMIENTO EN LA CONDUCCIÓN DE AUTOMÓVILES, y a tal efecto, libremente y de común acuerdo, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La AUTOESCUELA)

Fdo. Don [NOMBRE Y APELLIDOS]

(EL ALUMNO)

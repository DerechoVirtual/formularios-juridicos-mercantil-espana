---
name: contrato-gestion-hotel-operador-hotelero-mer-0513
description: "Contrato de gestión de un hotel por operador hotelero. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de gestión de un hotel por operador hotelero

> Formulario **MER-0513** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de gestión de un hotel por operador hotelero» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de gestión de un hotel por operador hotelero” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-gestion-hotel-operador-hotelero-mer-0513`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DÍA
- [ ] FECHA
- [ ] INSTITUCIÓN ARBITRAL
- [ ] INSTITUCIÓN DE MEDIACIÓN
- [ ] MARCA/MODELO
- [ ] MES
- [ ] NOMBRE DEL HOTEL
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] NORMAS APLICABLES A LA MEDIACIÓN
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

De una parte

D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], y N.I.F (en adelante, el PROPIETARIO), con correo electrónico [CORREO ELECTRÓNICO]

Y

de otra

D./Dª [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], y N.I.F. [NIF], que interviene en nombre y representación de [NOMBRE DEL REPRESENTADO/A], con CIF [NIF], y domicilio social en [LOCALIDAD] (en adelante, la GESTORA), con correo electrónico

INTERVIENEN

Ambas partes intervienen en la representación indicada y se reconocen mutua y plena capacidad para contratar y obligarse, a cuyo efecto

EXPONEN

I. Que el PROPIETARIO es titular del inmueble y/o de la empresa de explotación del establecimiento hotelero denominado [NOMBRE DEL HOTEL] sito en [LOCALIDAD], y que el mismo reúne (o reunirá en la fecha prevista para su apertura el día [FECHA]) los requisitos técnico-administrativos exigibles para su apertura y funcionamiento.

II. Que la GESTORA es una entidad profesional especializada en la gestión hotelera, dotada de los medios personales y materiales adecuados para asumir la dirección, administración y explotación del establecimiento, y declara conocer normativa sectorial aplicables y todos los demás requisitos para el ejercicio de la actividad.

III. Que las partes desean convenir una relación de gestión hotelera en la que la GESTORIA actuará en nombre y por cuenta del PROPIETARIO en la explotación del negocio, sin que exista arrendamiento de industria, cesión de empresa ni relación societaria entre ellas.

IV. Y conviniendo ambas partes en concertar el contrato, otorgan a tal fin el presente CONTRATO DE GESTIÓN HOTELERA, en base a las siguientes

CLÁUSULAS

PRIMERA. - OBJETO Y NATURALEZA

El PROPIETARIO encomienda a la GESTORA, con carácter exclusivo, la dirección, administración y explotación del hotel identificado en la Exposición precedente (el HOTEL), incluyendo sus dependencias, instalaciones y servicios accesorios, así como el mobiliario, maquinaria y equipamiento, todo lo que se recoge en el Inventario que se incorpora como Anexo I (inventario), manifestando ambas partes que todos los elementos se encuentran en perfecto estado para su funcionamiento.

La relación que se pacta es de gestión con representación: la GESTORA actuará en nombre y por cuenta del PROPIETARIO, sin adquirir derecho alguno de arrendamiento o posesión distinto del que sea necesario para la ejecución.

SEGUNDA. - ALCANCE DE LA GESTIÓN

La gestión comprenderá todas las actividades necesarias para el funcionamiento y explotación del negocio, entre las cuales se encuentran, sin carácter limitativo, las siguientes: (i) operaciones de alojamiento, F&B, MICE y wellness; (ii) ventas, marketing y distribución (incluida presencia online y canales de terceros), (iii) revenue management y pricing; (iv) compras y contratación de suministros; (v) contabilidad, tesorería y facturación; (vi) mantenimiento preventivo y correctivo y CAPEX operativo; (vii) cumplimiento normativo, seguridad, accesibilidad y sanidad; y (viii) reporting financiero y operativo.

La GESTORA ejercerá sus facultades conforme a las políticas y manuales operativos vigentes. Las materias estratégicas, umbrales económicos y decisiones reservadas al PROPIETARIO se recogen en el Anexo II (Materias Reservadas al Propietario).

TERCERA. - VIGENCIA, PRÓRROGA Y DESISTIMIENTO

El plazo del contrato es de [Nº] AÑOS desde la fecha de su firma.

El contrato se renovará tácitamente, por periodos de [Nº] AÑOS, de no mediar preaviso en contrario de una de las partes, con una antelación mínima de [Nº] MESES.

Sin perjuicio de otras causas previstas, el PROPIETARIO podrá desistir del contrato una vez transcurrido el primer año, con preaviso de [Nº] meses y abono de una compensación equivalente a [Nº] meses de la Tarifa Base promedio de los últimos [Nº] meses.

CUARTA. - REMUNERACIÓN

La GESTORA percibirá una remuneración por la prestación de servicios que se desglosa del siguiente modo: 1) una Tarifa Base que consistirá en un porcentaje de los ingresos totales derivados de la explotación del HOTEL, pactándose un ----- por ciento de los ingresos totales; y 2) una Tarifa de Incentivo del ----- por ciento de las ganancias obtenidas en la explotación hotelera, calculadas y liquidadas, con facturación y pago conforme al calendario del Anexo II.

Los servicios centrales (marketing, CRS, loyalty, tecnología) se repercutirán a la PROPIETARIA según criterios objetivos y verificables. No se aplicarán recargos sobre servicios subcontratados.

QUINTA. - ORGANIZACIÓN DEL SERVICIO Y RÉGIMEN DE FUNCIONAMIENTO

La GESTORA designará los puestos directivos de Director General, Gerente y Director Financiero, que deberán ser aprobados por el PROPIETARIO. La GESTORA contratará por cuenta del PROPIETARIO el resto de personal necesario para la explotación del HOTEL, respetando el convenio colectivo y la normativa de prevención de riesgos laborales.

La GESTORA organizará turnos, protocolos y formación, respondiendo disciplinariamente dentro del marco legal aplicable.

El Hotel operará bajo la marca [MARCA/MODELO], conforme a los manuales operativos del Gestor.

Las modificaciones sustanciales que impliquen CAPEX incremental requerirán aprobación previa del PROPIETARIO.

SEXTA. - RÉGIMEN FINANCIERO

Todos los gastos de explotación, incluidos los salariales, se imputarán a las cuentas operativas a nombre del PROPIETARIO, con el régimen de firmas y límites de disposición definidos en el Anexo IV (Tesorería).

Antes del inicio de cada ejercicio, la GESTORA presentará el Presupuesto Anual (operativo y CAPEX) para su aprobación.

La GESTORA remitirá al PROPIETARIO informes mensuales (caja), trimestrales (revisión de estrategia) y anuales (cuentas auditadas).

El PROPIETARIO podrá auditar las cuentas en cualquier momento con un preaviso de diez días.

SÉPTIMA. - LICENCIAS, CUMPLIMIENTO Y PROTECCIÓN DE CONSUMIDORES

El PROPIETARIO mantendrá la titularidad y vigencia de las licencias estructurales. La GESTORA explotará el HOTEL cumpliendo la normativa turística, sanitaria, de accesibilidad, seguridad y consumo aplicable, con hojas de reclamaciones, cartelería y atención a requerimientos de las autoridades.

Se implantarán programas de compliance penal, anticorrupción y competencia. En seguridad alimentaria, se cumplirán los APPCC y controles pertinentes.

OCTAVA. - PROTECCIÓN DE DATOS Y REGISTRO DE HUÉSPEDES

Las partes actuarán como corresponsables o como responsable/encargado según el Acuerdo de Tratamiento del Anexo V, cumpliendo RGPD y LOPDGDD. La GESTORA notificará brechas de seguridad, mantendrá registros de actividades y designará DPO cuando proceda.

El HOTEL cumplirá las obligaciones de registro documental e información a autoridades respecto de huéspedes y acompañantes, con conservación y remisión telemática en los términos legalmente exigidos.

NOVENA. - RESOLUCIÓN DEL CONTRATO Y EFECTOS

Si en dos ejercicios consecutivos el RevPAR del Hotel resultase inferior al % del promedio del conjunto competitivo aprobado en el presupuesto anual y, simultáneamente, el beneficio real fuese inferior al %, el PROPIETARIO podrá resolver sin penalidad, salvo que la GESTORA, dentro del plazo de treinta días, compense la diferencia hasta el umbral o presente y ejecute un plan de mejora aprobado. Se excluyen supuestos de fuerza mayor, reformas significativas, cierres ordenados y eventos imputables al Propietario.

Con independencia de lo anterior, el contrato podrá resolverse por incumplimiento esencial no subsanado en treinta días desde requerimiento fehaciente, o por fuerza mayor que impida la explotación por más de ciento ochenta días, o por desistimiento del PROPIETARIO en los términos de la cláusula tercera.

A la terminación, las partes procederán a la liquidación de cuentas, entrega de documentación, y traspaso de instalaciones, personal, material, accesos tecnológicos y dominios, siguiendo el Protocolo que se describe en el Anexo VI.

DÉCIMA. - SEGUROS

El PROPIETARIO mantendrá pólizas de todo riesgo daños y responsabilidad civil del inmueble, en tanto que la GESTORA debe mantener las pólizas de responsabilidad civil de la explotación y las demás propias del funcionamiento del negocio.

Cuando proceda, ambas partes se designarán recíprocamente como asegurados adicionales.

DECIMOPRIMERA. - LEGISLACIÓN APLICABLE

El presente Contrato tiene naturaleza mercantil, por lo que se rige por sus propias cláusulas, y en lo en ellas no previsto, por las disposiciones contenidas en el Código de Comercio, y en su defecto por las disposiciones del Código Civil.

DECIMOSEGUNDA. - CONFIDENCIALIDAD

Ambas partes se comprometen a no divulgar la información y documentación confidencial referente a la otra parte de la que hayan tenido conocimiento por razón de la ejecución del presente contrato, salvo las indispensables para su cumplimiento, y a mantenerla en secreto, incluso después de la finalización del mismo. Este deber subsistirá por cinco años tras la terminación. La infracción dará lugar a responsabilidad por los daños causados.

DECIMOTERCERA. - NOTIFICACIONES Y RESOLUCIÓN DE CONTROVERSIAS

Toda notificación se practicará preferentemente por correo electrónico a las direcciones indicadas en el encabezamiento, sin perjuicio de su remisión a los domicilios contractuales. Los cambios de dirección o correo deberán notificarse fehacientemente a la otra parte.

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación de [INSTITUCIÓN DE MEDIACIÓN], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y [NORMAS APLICABLES A LA MEDIACIÓN] fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de [INSTITUCIÓN ARBITRAL], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato, con sus Anexos I, II, III,IV, V y VI que forman parte integrante del mismo, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

El PROPIETARIO

LA GESTORA

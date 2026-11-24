---
name: contrato-auditoria-cuentas-anuales-sociedad-mercantil-mer-0565
description: "Contrato de auditoría de las cuentas anuales de una sociedad mercantil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de auditoría de las cuentas anuales de una sociedad mercantil

> Formulario **MER-0565** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de auditoría de las cuentas anuales de una sociedad mercantil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de auditoría de las cuentas anuales de una sociedad mercantil” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-auditoria-cuentas-anuales-sociedad-mercantil-mer-0565`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] Nº (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)

## Normas que cita el formulario

- art. 263 LSC

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

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO].

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO].

INTERVIENEN

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA MERCANTIL", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA AUDITORA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE AUDITORÍA, y a tal efecto, libremente y de común acuerdo,

EXPONEN

Que la Sociedad desea celebrar un contrato de auditoría de cuentas para dar cumplimiento a lo dispuesto en el artículo 263 LSC y en la Disposición Adicional 1ª de la Ley de Auditoría de Cuentas, habiendo sido designados los auditores anteriormente citados para desempeñar esta función en virtud de acuerdo adoptado en la Junta General de fecha

Que la Sociedad de auditoria que acepta el encargo está inscrita en el Registro Oficial de Auditores de Cuentas con el número [NÚMERO].

III.Que a los fines indicados, ambas partes suscriben el presente CONTRATO DE AUDITORIA DE CUENTAS, que se regirá por las siguientes,

CLÁUSULAS

Objeto

Los auditores realizarán la auditoria de las cuentas anuales de LA SOCIEDAD. Al completar la auditoria, emitirán un informe que contendrá su opinión técnica sobre las cuentas anuales examinadas y sobre la información contable contemplada en el informe de gestión.

Adicionalmente, los auditores informarán a los Administradores sobre las debilidades significativas que, en su caso, hubieran identificado en la evaluación del control interno.

El presente contrato tiene por objeto exclusivo la realización de la auditoria de las cuentas anuales de la Sociedad en los términos previstos en la legislación vigente, quedando excluido del mismo cualquier otra actuación profesional que se encomiende por la Sociedad a los auditores.

Responsabilidad de los auditores

Los auditores realizarán su trabajo de acuerdo con las disposiciones legales vigentes, así como con las normas de auditoria generalmente aceptadas publicadas por el Instituto de Contabilidad y Auditoria de Cuentas. En consecuencia, en bases selectivas, obtendrán la evidencia justificativa de la información incluida en las cuentas anuales, evaluarán los principios contables aplicados, las estimaciones significativas realizadas por los Administradores y la presentación global de las citadas cuentas anuales. Igualmente comprobarán la concordancia de la información contable que contiene el informe de gestión con las cuentas anuales.

Limitaciones de la auditoría

Como parte de la auditoria, y únicamente a efectos de determinar la naturaleza, oportunidad y amplitud de los procedimientos de auditoria, los auditores tendrán en cuenta la estructura de control interno de la Sociedad. Sin embargo, dicha consideración no será suficiente para permitirles expresar una opinión específica sobre la eficacia de la estructura de control interno en lo que se refiere a la información financiera.

El objetivo del trabajo de los auditores es obtener una seguridad razonable de que las cuentas anuales estén libres de errores o irregularidades significativos. Aunque una estructura efectiva de control interno reduce la probabilidad de que puedan existir riesgos de errores o irregularidades y de que no sean detectados, no elimina tal posibilidad. Por dicha razón y dado que el examen de los auditores está basado principalmente en pruebas selectivas, éstos no pueden garantizar que se detecten todo tipo de errores o irregularidades, en caso de existir.

Confidencialidad

Los papeles de trabajo preparados en relación con la auditoria son propiedad de los auditores, constituyen información confidencial, y éstos los mantendrán en su poder de acuerdo con las exigencias de la Ley de Auditoria de Cuentas. Asimismo, y de acuerdo con el deber de secreto establecido en dicha normativa, los auditores se comprometen a mantener estricta confidencialidad sobre la información de la entidad obtenida en la realización del trabajo de auditoría.

Por otra parte, los auditores en la realización de su trabajo mantendrán siempre una situación de independencia y objetividad, tal y como exige la normativa de auditoría de cuentas a este respecto.

Responsabilidad de los administradores

Los Administradores de la sociedad son responsables de la formulación de las cuentas anuales a las que se ha hecho referencia anteriormente, así como de entregarlas a los auditores, debidamente firmadas, dentro del plazo que para su aprobación establece la Ley. En este sentido, los Administradores son responsables del adecuado registro de las operaciones en los libros de contabilidad y del mantenimiento de una estructura de control interno que sea suficiente para permitir la elaboración de unas cuentas anuales fiables. Los Administradores son también responsables de proporcionar a los auditores, cuando éstos así lo soliciten, todos los registros contables de la Sociedad y la información relativa a los mismos así como de indicarles el personal de la Sociedad a quien puedan dirigir sus consultas.

Deber de colaboración de la sociedad

Adicionalmente, la Sociedad prestará a los auditores la máxima colaboración en la preparación de ciertos trabajos, tales como análisis de cuentas, conciliaciones de diferencias de saldos, búsqueda de comprobantes y registros, etc. Estos trabajos así como las cartas de solicitud de confirmación que soliciten los auditores serán puestos a su disposición en el plazo que la Sociedad y los auditores fijen de común acuerdo.

De acuerdo con normas de auditoria generalmente aceptadas, los auditores harán consultas específicas a los Administradores y a otras personas sobre la información contenida en las cuentas anuales y sobre la eficacia de la estructura de control interno. Asimismo, tales normas exigen que los auditores obtengan de los Administradores una carta de manifestaciones sobre las cuentas anuales. Los resultados de las pruebas de auditoria, las respuestas a las consultas de los auditores y la carta de manifestaciones constituyen la evidencia en la que los auditores pretenden basarse para formarse una opinión sobre las cuentas anuales.

Publicidad del informe

Si la sociedad tuviera la intención de publicar las cuentas anuales junto con el informe de auditoria en un documento que contenga otra información, se compromete a proporcionar a los auditores un borrador del documento para su lectura, y a obtener el consentimiento de la Audiotra para la inclusión en él del informe de auditoria, antes de que dicho documento se publique y distribuya.

Duración del contrato

La duración del presente contrato será de [Nº] años a contar desde la conclusión del presente contrato.

Honorarios profesionales

Los honorarios profesionales que habrán de percibir los auditores por el desempeño de su función durante el primer ejercicio de vigencia del presente contrato serán de [IMPORTE] euros, importe fijado tomando como base [Nº] horas de trabajo. Este importe no incluye gastos y suplidos ni el IVA correspondiente a los servicios prestados.

Si durante la realización del trabajo observaran los auditores cambios en las circunstancias en base a las cuales se ha realizado el presente contrato, tales como fusiones, absorciones, cambios del objeto social, modificación del volumen de negocio o de la cifra patrimonial, modificación en los criterios de contabilización, errores en aquellos detalles que hubieran solicitado, modificaciones del sistema contable u otros similares, se lo notificarán a la Sociedad, explicando los motivos que les obligan a modificar los honorarios estimados, en base al número de horas a realizar en virtud de los cambios operados.

Forma de pago

Los honorarios profesionales a percibir por los auditores durante cada ejercicio, serán abonados por la Sociedad de la forma siguiente:

- % a la firma del presente contrato.

- % en [Nº] mensualidades de [IMPORTE] euros cada una durante los meses [MES] a [MES].

- % a la entrega del informe final.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Sumisión a tribunales / Con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Sumisión a arbitraje / Sin cláusula penal en caso de no ejecución voluntaria del laudo / Sumisión a arbitraje / Con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE AUDITORÍA DE CUENTAS, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

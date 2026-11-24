---
name: carta-encargo-trabajo-auditoria-cuentas-mer-0566
description: "Carta de encargo de un trabajo de auditoría de cuentas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Carta de encargo de un trabajo de auditoría de cuentas

> Formulario **MER-0566** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Carta de encargo de un trabajo de auditoría de cuentas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Carta de encargo de un trabajo de auditoría de cuentas” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:carta-encargo-trabajo-auditoria-cuentas-mer-0566`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NIA-ES 706 R (2 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] EJERCICIOS ECONÓMICOS
- [ ] IMPORTE
- [ ] MES
- [ ] NIA-ES 570 R
- [ ] NIA-ES 701
- [ ] NIA-ES 720 R
- [ ] Nº
- [ ] Nº DE LA ÚLTIMA PÁGINA
- [ ] Nº DE PÁGINAS
- [ ] TÍTULO DE LA CLÁUSULA

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

I. Objetivo y limitaciones de la auditoría

Realizaremos nuestro trabajo de acuerdo con las Normas Internacionales de Auditoría adaptadas para su aplicación en España (NIA-ES).

De acuerdo con la legislación vigente en España, las cuentas anuales deberán ser formuladas por el órgano de administración de la sociedad siguiendo el Marco de Información Financiera (MIFA) que resulta de aplicación en España: Código de Comercio, Ley de Sociedades de Capital, Plan General de Contabilidad y adaptaciones sectoriales, como más relevantes.

Como parte de nuestra auditoría, y únicamente a efectos de determinar la naturaleza, oportunidad y amplitud de nuestros procedimientos, efectuaremos un estudio y evaluación de la estructura de control interno de la Sociedad. Sin embargo, ello no será suficiente para permitirnos expresar una opinión específica sobre la eficacia de la estructura de control interno en lo que se refiere a la información financiera. El objetivo de nuestro trabajo, en relación al estudio y evaluación del sistema de control interno, es obtener una seguridad razonable de que las cuentas anuales estén libres de errores o irregularidades significativos. Aunque una estructura efectiva de control interno reduce la probabilidad de que puedan existir riesgos de errores o irregularidades y de que no sean detectados, no elimina tal posibilidad. Por dicha razón y dado que nuestro examen está basado principalmente en pruebas selectivas, no podemos garantizar que se detecten todo tipo de errores o irregularidades, en caso de existir.

La opinión técnica del auditor de cuentas proporciona un mayor grado de fiabilidad a las cuentas anuales, pero no incluye la predicción de sucesos futuros, por lo tanto, la emisión de un informe sin salvedades sobre las cuentas anuales no constituye una garantía sobre la viabilidad futura de una entidad. No obstante, el auditor de cuentas debe prestar atención a aquellas situaciones o circunstancias que le puedan hacer dudar de la continuidad de la actividad normal de la entidad a lo Largo del próximo ejercicio económico, para decidir si las mismas han de influir en su opinión.

Los papeles de trabajo preparados en relación con la auditoría son propiedad del auditor, constituyen información confidencial, y los mantendremos en nuestro poder de acuerdo con las exigencias de la Normativa sobre Auditoría de Cuentas. Asimismo, y de acuerdo con el deber de secreto establecido en dicha normativa, nos comprometemos a mantener estricta confidencialidad sobre la información de la entidad obtenida en la realización del trabajo de auditoría.

Por otra parte, en la realización de nuestro trabajo mantendremos siempre una situación de independencia y objetividad, tal y como exige la normativa de auditoría de cuentas a este respecto.

II. Responsabilidad y manifestaciones de los administradores

II.1. Responsabilidad

La formulación de las cuentas anuales a las que se ha hecho referencia anteriormente es responsabilidad de los Administradores de la sociedad.

Igualmente, el registro de las operaciones en los libros de contabilidad y del mantenimiento de una estructura de control interno que sea suficiente para permitir la elaboración de unas cuentas anuales fiables es responsabilidad de los Administradores, así como proporcionar, cuando sean solicitados, los registros contables de la Sociedad y la información relativa a los mismos.

II.2. Comunicaciones

Con objeto de facilitar una comunicación más efectiva, la sociedad designará el personal de ésta a quienes el auditor deba dirigir las consultas necesarias para realizar su trabajo.

Las Normas Técnicas de Auditoria exigen que obtengamos de los Administradores una carta de manifestaciones sobre las cuentas anuales. Los resultados de nuestras pruebas de auditoría, las respuestas a nuestras consultas y la carta de manifestaciones constituyen la evidencia para emitir una opinión sobre las cuentas anuales. En consecuencia, los administradores deberán entregar firmada la "Carta de manifestaciones de la Dirección" que le soliciten los auditores en los términos previstos en la Norma Técnica de Auditoría al respecto.

II.3. Publicidad del informe de auditoría

Si ustedes tuvieran la intención de publicar las cuentas anuales junto con nuestro informe de auditoria en un documento que contenga otra información, se comprometen a proporcionarnos un borrador del documento para su lectura, y a obtener nuestro consentimiento para la inclusión en él de nuestro informe de auditoría, antes de que dicho documento se publique y distribuya.

III. Informe

De acuerdo con el artículo 5 de la LAC 22/2015, la estructura del informe de auditoría de cuentas anuales emitido por un auditor independiente presentará el siguiente contenido:

i. Informe sobre las cuentas anuales
a) Opinión (o, en su caso, opinión con salvedades, desfavorable o denegada)
b) Fundamento de la opinión
c) Incertidumbre material relacionada con la empresa en funcionamiento, en su caso [NIA-ES 570 R]
d) Aspectos más relevantes de la auditoría o Cuestiones clave de la auditoría [NIA-ES 701]
e) Párrafo de énfasis, en su caso [NIA-ES 706 R]
f) Párrafo sobre otras cuestiones, en su caso [NIA-ES 706 R]
g) Otra información: informe de gestión [NIA-ES 720 R]
h) Responsabilidad de los administradores
i) Responsabilidad del auditor
ii. Informe sobre otros requerimientos legales y reglamentarios «en el caso de EIP»
a) Informe adicional para la comisión de auditoría
b) Periodo de contratación
c) Servicios prestados

III. 1. Riesgos significativos y otros hallazgos

III.2. Ajustes

IV. Honorarios y facturación

De acuerdo con lo establecido en el artículo 24 de la LAC 22/2015, nuestros honorarios por los servicios de auditoría de cuentas anuales se fijan en función del tiempo empleado en la realización del trabajo y de las tarifas horarias de auditoría en vigor cada año, por categorías profesionales.

Nuestros honorarios por el examen de las cuentas correspondientes al ejercicio cerrado el [DÍA] de [MES] de [AÑO] ascienden a [IMPORTE] euros, equivalentes a [Nº] horas de trabajo de nuestro personal profesional. Este importe no incluye gastos y suplidos ni el IVA correspondiente a los servicios prestados.

Si durante la realización del informe de auditoria se observaran cambios en las circunstancias tomadas en consideración para la conclusión del presente acuerdo (fusiones, absorciones, cambios de objeto social, modificación de volumen de negocio o de la cifra patrimonial, modificación en los criterios de contabilización, errores en aquellos detalles que les hubiéramos solicitado, modificación del sistema contable y otros similares, etc.) se lo notificaríamos explicándoles los motivos que nos obligan a variar los honorarios estimados, basándonos en el número de horas a realizar en virtud de los cambios operados.

V. Modificación de carta de encargo

Tal y como se establece en la normativa de auditoría en vigor, sólo se pueden aceptar modificaciones en los términos del encargo de auditoría si existe una justificación razonable para ello.

En tal caso haremos constar los nuevos términos en una nueva carta de encargo.

VI. Protección de datos

De acuerdo con la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales, derecho amparado por el art. 18.4 de la Constitución y lo regulado por el Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016, relativo a la protección de las personas físicas en lo que respecta al tratamiento de datos personales y a la libre circulación de estos datos, al objeto de salvaguardar el interés público y cumplir con sus obligaciones y con la regulación normativa de la legislación contra el blanqueo de capitales, por medio de la presente la Sociedad da el consentimiento al auditor para que pueda acceder a los datos de carácter personal contemplados en el Reglamento General de Protección de Datos (RGPD), no pudiendo ser utilizados los mismos más allá del propósito de la realización del trabajo de auditoría.

El auditor se compromete a tratar los datos de cualquier operación realizada sobre datos personales del cliente y su organización de acuerdo con el RGPD, especialmente en relación con la identidad y acceso a datos personales relevantes de sus empleados y a tener implementados unos procedimientos adecuados que garanticen el adecuado tratamiento, uso y distribución de la información proporcionada por el cliente, en relación con su recogida, registro, estructuración, conservación, adaptación, consulta, utilización, comunicación, supresión y destrucción.

VI.1. Confidencialidad

Todos los datos recogidos cuentan con el compromiso de confidencialidad, con las medidas de seguridad establecidas legalmente, y bajo ningún concepto serán cedidos o tratados por terceras personas, físicas o jurídicas, sin su previo consentimiento, salvo en aquellos casos en los que fuere imprescindible para la correcta prestación de nuestros servicios profesionales de auditoría.

VII. [TÍTULO DE LA CLÁUSULA]. Régimen jurídico aplicable

La prestación de los servicios de auditoria objeto del presente acuerdo se regirá en todo caso por las disposiciones legales vigentes en cada momento y cualquier discrepancia en torno al mismo se someterá al fuero de los tribunales españoles.

VIII. Documento único

Este documento, extendido en [Nº DE PÁGINAS] páginas, numeradas correlativamente del número 1 al [Nº DE LA ÚLTIMA PÁGINA] constituye el único contrato o carta de encargo entre ambas partes, en relación con la realización de la auditoría de las cuentas anuales de [DENOMINACIÓN SOCIAL] para los ejercicios económicos [EJERCICIOS ECONÓMICOS], por lo que el mismo constituye el documento que, a todos efectos, tiene fuerza legal. En consecuencia, cualquier variación en los términos de este contrato o carta de encargo deberá ser realizada por escrito y no será efectiva sin la firma del auditor y de un representante debidamente autorizado de "la Sociedad".

Les agradeceríamos que, como prueba de conformidad y aceptación de los términos aquí expuestos responsabilidades, nos remitan una copia debidamente firmada de este documento, el cual se extiende por duplicado.

Atentamente,

Por la firma de auditoría

Recibido y conforme por la sociedad auditada

Socio-Auditor de cuentas	Representante legal de la entidad
	Fecha:

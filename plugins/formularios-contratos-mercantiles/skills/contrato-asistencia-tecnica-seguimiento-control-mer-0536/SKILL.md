---
name: contrato-asistencia-tecnica-seguimiento-control-mer-0536
description: "Contrato de asistencia técnica para el seguimiento y control del proyecto (project monitoring). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de asistencia técnica para el seguimiento y control del proyecto (project monitoring)

> Formulario **MER-0536** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de asistencia técnica para el seguimiento y control del proyecto (project monitoring)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de asistencia técnica para el seguimiento y control del proyecto (project monitoring)” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-asistencia-tecnica-seguimiento-control-mer-0536`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (16 veces)
- [ ] NÚMERO (7 veces)
- [ ] AÑO (4 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] DÍA (4 veces)
- [ ] FOLIO (4 veces)
- [ ] INSCRIPCIÓN (4 veces)
- [ ] MES (4 veces)
- [ ] NIF (4 veces)
- [ ] TOMO (4 veces)
- [ ] HOJA (3 veces)
- [ ] NOMBRE DEL NOTARIO (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] SECCIÓN (3 veces)
- [ ] COMUNIDAD AUTÓNOMA
- [ ] LIBRO
- [ ] LUGAR
- [ ] NOMBRE COMERCIAL
- [ ] Nº
- [ ] PROVINCIA

## Normas que cita el formulario

- art. 1124 Código Civil

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

DE UNA PARTE, D. [NOMBRE Y APELLIDOS], mayor de edad, vecino de [LOCALIDAD], con NIF [NIF], con domicilio profesional en [LOCALIDAD];

DE OTRA PARTE, D. [NOMBRE Y APELLIDOS], mayor de edad, vecino de [LOCALIDAD], con NIF [NIF], con domicilio profesional en [LOCALIDAD];

DE OTRA PARTE, D. [NOMBRE Y APELLIDOS], mayor de edad, vecino de [LOCALIDAD], con NIF [NIF], con domicilio profesional en [LOCALIDAD];

INTERVIENEN

El primero en nombre y representación de la sociedad de nacionalidad española [DENOMINACIÓN SOCIAL], S.L. (en adelante, el "PROMOTOR"), con domicilio en [LOCALIDAD], y C.I.F. número: [NIF], constituida por tiempo indefinido mediante escritura de fecha [DÍA] de [MES] de [AÑO], autorizada por el Sr. Notario de [LOCALIDAD], Don [NOMBRE DEL NOTARIO], bajo el número [NÚMERO] de su protocolo. Consta inscrita en el Registro Mercantil de [LOCALIDAD], en el Tomo [TOMO], folio [FOLIO], Sección [SECCIÓN], hoja [HOJA], inscripción [INSCRIPCIÓN], en su condición de apoderado de dicha entidad, domiciliada en

El segundo en nombre y representación de la sociedad [DENOMINACIÓN SOCIAL] (en adelante, el "FINANCIERO"), constituida por tiempo indefinido mediante escritura de fecha [DÍA] de [MES] de [AÑO], autorizada por el Sr. Notario de [LOCALIDAD], Don [NOMBRE DEL NOTARIO], bajo el número [NÚMERO] de su protocolo. Consta inscrita en el Registro Mercantil de [LOCALIDAD], en el Tomo [TOMO], folio [FOLIO], Sección [SECCIÓN], hoja [HOJA], inscripción [INSCRIPCIÓN] Es la citada CAJA una Institución benéfico social con sede central en [LOCALIDAD], con C.I.F., e inscrita en el Registro del Banco de España, con el número [NÚMERO], en el de Caja de Ahorros de la Comunidad [COMUNIDAD AUTÓNOMA], con el número [NÚMERO], y en el Registro Mercantil de la Provincia de [PROVINCIA], al tomo [TOMO] general, Libro [LIBRO], folio [FOLIO], hoja número [NÚMERO], inscripción [INSCRIPCIÓN] Se halla especialmente facultado para la firma de este contrato en virtud de su cargo de Apoderado, que manifiesta vigente así como la capacidad jurídica de la Entidad que representa.

El tercero en nombre y representación de la sociedad [DENOMINACIÓN SOCIAL], S.L., cuya división de consultoría opera bajo el nombre comercial de "" (en adelante, el "CONTROLER"), en su condición de Apoderado de dicha entidad, con domicilio en [LOCALIDAD], y C.I.F. número [NÚMERO], constituida por tiempo indefinido mediante escritura de fecha [DÍA] de [MES] de [AÑO], autorizada por el Sr. Notario de [LOCALIDAD], Don [NOMBRE DEL NOTARIO], bajo el número [NÚMERO] de su protocolo. Consta inscrita en el Registro Mercantil de [LOCALIDAD], en el Tomo [TOMO], folio [FOLIO], Sección [SECCIÓN], hoja [HOJA], inscripción [INSCRIPCIÓN], en su condición de apoderado de dicha entidad, domiciliada en

Las partes se reconocen mutuamente la capacidad y facultades necesarias para la celebración del presente Contrato, y manifiestan que éstas no les han sido modificadas, revocadas ni suspendidas, por lo que libre y voluntariamente

EXPONEN

1. Que el PROMOTOR ha decidido continuar con el desarrollo del proyecto "Urbanización " (en lo sucesivo, el "PROYECTO").

2. Que el PROMOTOR mantiene la gestión del PROYECTO directamente (en lo sucesivo, también denominado el "GESTOR"), siendo responsable de la dirección y la gestión de los proyectos y obras relacionados con la continuación del PROYECTO.

3. Que el PROMOTOR ha solicitado financiación al FINANCIERO para llevar a buen fin el desarrollo del PROYECTO.

4. Que el FINANCIERO está interesado en optimizar su capacidad de análisis, seguimiento y control de la marcha del PROYECTO, para lo que ha decidido solicitar al PROMOTOR la contratación de los servicios de la asistencia técnica independiente del CONTROLER, con el fin de disponer tanto de una información como de una asesoría técnica profesional e independiente adecuada para el mejor control y seguimiento de la ejecución del PROYECTO, que reporte directamente al FINANCIERO.

5. Que [NOMBRE COMERCIAL] es el nombre comercial de la sociedad [DENOMINACIÓN SOCIAL], S.L. dedicada a la prestación de servicios de consultoría y asesoramiento sobre dirección y gestión empresarial, así como todo tipo de servicios relacionados con la gestión integral de proyectos inmobiliarios y la revisión, asistencia técnica y control de proyectos en desarrollo. Por ello, dispone de los recursos técnicos, materiales y humanos cualificados para la adecuada prestación de los servicios requeridos por el PROMOTOR y el FINANCIERO.

6. Que, de acuerdo con lo anteriormente expuesto, las partes acuerdan suscribir al presente CONTRATO DE ARRENDAMIENTO DE SERVICIOS DE ASISTENCIA TÉCNICA PARA EL SEGUIMIENTO Y APOYO EN EL CONTROL DEL PROYECTO (PROJECT MONITORING), que se regirán de acuerdo con las siguientes,

ESTIPULACIONES

Objeto del contrato

Es objeto del presente contrato la aportación por parte del CONTROLER, durante la vigencia del presente contrato, al FINANCIERO de ciertos recursos técnicos para auxiliar al FINANCIERO en el control, seguimiento y acceso a la información adecuada sobre la marcha del PROYECTO.

Alcance de los servicios

Con dicha finalidad el CONTROLER prestará en favor del FINANCIERO, a lo largo de la duración del Contrato, los servicios que se relacionan en la Propuesta de Colaboración que se adjunta como Anexo A.

El CONTROLER realizará estas funciones como agente del FINANCIERO, para informarle en el seguimiento de la marcha del PROYECTO, y en la obtención de la información necesaria que posibilite el mejor control del mismo e introducción de mejoras y ahorros en el PROYECTO, a través de la presentación de los servicios descritos en el Anexo A.

Durante la vigencia del presente contrato el CONTROLER mantendrá al FINANCIERO informado de la situación del PROYECTO, ocupándose en su nombre de los factores relacionados con el PROYECTO bajo su responsabilidad, de acuerdo al alcance de los servicios descritos en el Anexo A y proponiendo aquellas actividades o decisiones que considere recomendables para la reducción del riesgo general del PROYECTO, sin perjuicio de la responsabilidad última del GESTOR como auténtico responsable en la conducción y control en términos de plaza, coste y calidad del PROYECTO.

Plazos y duración

Se estima que la duración del presente contrato será de [Nº] meses a partir del día de hoy. El contrato quedará tácitamente prorrogado por sucesivos periodos de un mes, salvo que se produzca su denuncia par cualquiera de las partes, formulada con una antelación de un mes al vencimiento del contrato o de cualquiera de sus prórrogas.

Relaciones laborales

Para la prestación de los servicios objeto del presente Contrato el CONTROLER destinará durante el periodo de duración del mismo el personal con Ia cualificación técnica y profesional adecuada para su ejecución que se relacionan en el Anexo A que se acompaña al presente Contrato.

Por indicación del CONTROLER, y con la previa comunicación al FINANCIERO, se podrá realizar la sustitución de los profesionales indicados por otros profesionales, los cuales serán de similar categoría y experiencia.

Ninguna de las partes, a lo largo del periodo de duración del presente Contrato y dentro de los dos años siguientes a su resolución o vencimiento, realizará una oferta de trabajo directa o indirectamente ni contratará a ningún miembro del personal de la otra parte que haya participado en la prestación o recepción de los servicios objeto del presente Contrato, o que esté de cualquier modo relacionado con el mismo, sin el consentimiento de dicha parte.

Durante el plazo contractual y para desarrollar el objeto contractual el PROMOTOR faculta al CONTROLER para dirigirse al GESTOR y solicitarle, en nombre del FINANCIERO, la información que el CONTROLER estime oportuna para el mejor fin de su labor, así como facultándole para acceder al lugar de las obras y a aquellas reuniones en donde se estime conveniente su presencia, al objeto de facilitar el cumplimiento del objetivo contractual, siempre dentro de las directrices marcadas por el FINANCIERO, y en calidad de CONTROLER del PROYECTO.

Asimismo, el PROMOTOR dará instrucciones al GESTOR y se obliga, objetivamente, a que la información requerida por el CONTROLER sea entregada por el GESTOR.

Honorarios y forma de pago

Los honorarios a percibir por el CONTROLER por los servicios expresados en la estipulación segunda del presente Contrato serán conforme a la Propuesta de Colaboración pactada que se adjunta como Anexo A. Dichos honorarios son aceptados por el PROMOTOR y serán pagados al CONTROLER en los plazos acordados.

Previa aceptación del FINANCIERO, el CONTROLER presentará dentro de los primeros cinco días de cada mes la factura correspondiente al importe indicado para ese mes en la Propuesta de Colaboración adjunta, y el PROMOTOR abonará al CONTROLER dicho importe mediante transferencia bancaria dentro de los cinco días desde su fecha de emisión.

Junto a la primera factura al inicio de la prestación de servicios del 2º Ciclo, el CONTROLER presentará una factura correspondiente a la provisión de fondos de los servicios a prestar en los 3 meses siguientes, que se abonará junto a ese primer pago al 2º Ciclo y quedará saldada a la finalización del PROYECTO.

Nombramiento de representantes

Cada una de las partes designará una persona que actuará como su representante frente a la otra parte. Los representantes tendrán facultad plena para actuar en nombre de su representado y decidir sobre todas las cuestiones que surjan en relación con la ejecución del presente Contrato.

Cada una de las partes podrá sustituir a su representante durante la ejecución de la obra, previa notificación a la otra.

Obligaciones del controler

El CONTROLER desempeñará las actividades objeto del Contrato, relacionadas en el Anexo A consistentes, básicamente, en la verificación del grado de avance de la edificación y su valoración así como la asignación de los recursos económicos y humanos dentro de la obra en curso, con arreglo a los siguientes principios: a) Poniendo a disposición del FINANCIERO su máxima diligencia, cuidado y profesionalidad, y; b) Utilizando su experiencia, competencia y capacidad en la dirección y administración de proyectos.

Obligaciones del promotor

El PROMOTOR facilitará la realización de los trabajos contratados al CONTROLER con arreglo a los siguientes principios:

a) El PROMOTOR prestará su máxima colaboración al CONTROLER en el cumplimiento de los servicios estipulados y para el desarrollo eficiente de los mismos.

b) El PROMOTOR se obliga a pagar al CONTROLER y en los plazos establecidos los Honorarios y Gastos indicados en la estipulación Quinta.

c) El PROMOTOR autorizará a todo el personal del CONTROLER el acceso a la obra, a las reuniones con el GESTOR consultores y proyectistas, prestando todo tipo de facilidades para ello.

d) El PROMOTOR, por sí mismo o a través del GESTOR, entregará al CONTROLER sin cargo alguno y dentro de las diversas fases todos los documentos, diseños y otros elementos necesarios para que el CONTROLER pueda desempeñar el objeto del presente Contrato y con cuantas copias le sean razonablemente solicitadas por este último.

e) El PROMOTOR dará instrucciones al GESTOR y se obliga, objetivamente, a que La información y colaboración requerida por el CONTROLER sea entregada y prestada por el GESTOR.

f) Previa asesoramiento, supervisión, recomendación y aceptación del CONTROLER, el PROMOTOR se obliga a atender, de manera directa o inmediata y bajo su entera responsabilidad, La totalidad de los pagos del PROYECTO, emitiendo en los 15 primeros días de cada mes las peticiones de disposición con orden irrevocable de transferencias bancarias directamente a favor de los intervinientes en la ejecución de la obra, visadas por el CONTROLER.

Obligaciones del financiero

Conforme a las peticiones mensuales de disposición con orden irrevocable de transferencias bancarias subyacentes que presente el PROMOTOR visadas con la aprobación del CONTROLER y en la forma notarial pactada en la escritura de préstamo hipotecario, el FINANCIERO abonará dichas disposiciones entre los días 25 y 30 de cada mes, dentro de los límites de importes, plazos y demás condiciones del préstamo acordado al PROYECTO, en la cuenta abierta por el PROMOTOR en la misma entidad del FINANCIERO a petición del mismo, y simultáneamente, procederá a realizar las transferencias bancarias subyacentes, correspondientes a los pagos aprobados por el CONTROLER al contratista y sub-contratistas intervinientes en el avance de la promoción.

Capacidad con la que actúa el controler

El PROMOTOR y el FINANCIERO declaran que el CONTROLER no es responsable de los errores que pueda haber en el proyecto redactado por los proyectistas, ni asume las responsabilidades que le son propias del GESTOR, Dirección Facultativa, Coordinador de Seguridad o Contratistas, entendiéndose que el CONTROLER no actúa como gerente del proyecto, director de obra, arquitecto, ingeniero, proyectista, dirección facultativa ni como constructor del PROYECTO, sino como mero analista de riesgos del PROYECTO y, en su caso, asesor del FINANCIERO y el PROMOTOR.

El CONTROLER, en el desarrollo del presente Contrato, no asume los compromisos, derechos y obligaciones que sean propios o haya adquirido o adquiera en un futuro el PROMOTOR frente a terceros en relación con el PROYECTO, ya que su función se limita al cumplimiento del objeto del presente Contrato como asesor profesional independiente.

Transferencia de obligaciones contractuales

Ninguna de las partes podrá, sin la previa conformidad por escrito de la otra, transferir a otra persona la totalidad o parte de los derechos u obligaciones objeto del presente Contrato.

No obstante lo anterior, el PROMOTOR y el FINANCIERO autorizan, en este mismo acto, al CONTROLER a que la prestación de servicios que contiene el presente contrato sea realizada por una entidad participada por el CONTROLER. Dicha entidad se subrogará en la posición del CONTROLER en todas las obligaciones y derechos dimanantes del presente contrato.

Modificación de la prestación de servicios

Si las circunstancias así lo exigieran, el FINANCIERO podrá, en cualquier momento, y previa autorización del PROMOTOR, acordar la modificación del alcance de servicios pactados, ya sea ampliándolos o reduciéndolos, debiendo someter tales modificaciones a un acuerdo adicional al presente.

Documentación y confidencialidad

a) En todo momento las partes tendrán acceso libre y completo a cualquier documento o información que elabore la otra parte y afecte o pueda afectar al objeto del presente Contrato, de manera que ambas partes contribuyan a que la gestión sea eficaz y transparente.

b) Las partes se comprometen expresamente a mantener la más estricta confidencialidad respecto de los materiales, informaciones y documentos que de la otra parte contratante puedan tener conocimiento como consecuencia de la presente relación contractual, y a no permitir el acceso a ellos a terceras personas o entidades sin mediar consentimiento previo por la otra parte, excepción hecha de los empleados o agentes de ambas partes, y siempre en la medida estrictamente necesaria para la adecuada prestación de los servicios objeto del presente Contrato, siendo responsable cada una de las partes de los daños y perjuicios que pudieran derivarse de la violación de este deber de confidencialidad por dichos empleados o agentes.

c) Asimismo, se comprometen las partes a no utilizar con fines comerciales, en su propio beneficia o en el de terceros, información alguna obtenida de la otra parte en el marco de la preparación o ejecución del presente Contrato.

Comunicaciones

Para llevar a cabo cualesquiera de las comunicaciones se atenderá a las direcciones que aparecen como domicilio social de las partes al inicio de este contrato.

Suspensión y resolución

a) El FINANCIERO tiene el derecho de suspender temporalmente el presente Contrato en cualquier momento por razones no contempladas en el mismo y notificará par escrito al PROMOTOR y al CONTROLER la fecha de comienzo de dicha suspensión con una antelación superior a 45 días naturales previo al comienzo de la suspensión.

Dicha suspensión no podrá ser superior a tres meses contados a partir del día natural posterior a la comunicación referida en el párrafo anterior. Durante la suspensión, no se devengaran los honorarios establecidos en este contrato para el CONTROLER.

El FINANCIERO deberá comunicar, con 45 días naturales de antelación, la fecha de reanudación de los servicios.

b) De acuerdo con lo establecido en el art. 1124 del vigente Código Civil, el presente contrato se resolverá por incumplimiento, por cualquiera de las partes, de las obligaciones en él contenidas. El que sufra el incumplimiento, podrá escoger entre exigir el cumplimiento o la resolución del contrato, con resarcimiento de daños y abono de intereses, en ambos casos.

A título enunciativo y no limitativo, el CONTROLER tendrá derecho a resolver el Contrato, con las consecuencias antes referidas, en cualquiera de los siguientes casos:

• Por retraso mayor de treinta días en el abono de los honorarios respecto de las condiciones acordadas.

• Por incumplimiento de cualquiera de las obligaciones asumidas en este contrato por el PROMOTOR, y éste no subsanase dicha situación dentro de los treinta días de haber sido requerido fehacientemente para ella.

• En el caso de que la suspensión del Contrato dure más de tres meses.

En el caso de suspensión por más de tres meses o resolución por parte del FINANCIERO por razones no imputables al CONTROLER, el PROMOTOR se compromete a pagar los honorarios e indemnizaciones siguientes:

i. Los honorarios correspondientes hasta el momento de la rescisión.

ii. Una indemnización equivalente al 33% de los honorarios restantes durante el tiempo que falte hasta la expiración del presente contrato o de cualquiera de sus prórrogas, como cláusula penal liquidativa.

A título enunciativo y no limitativo, el PROMOTOR y el FINANCIERO tendrán derecho a resolver el Contrato, con las consecuencias antes referidas, en cualquiera de los siguientes casos:

i. En el caso de que el CONTROLER no cumplimentara de forma repetida y manifiesta en tiempo o en forma los requerimientos que el FINANCIERO le haya notificado por escrito, y si dicho incumplimiento afectará substancialmente a la buena marcha del PROYECTO.

ii. Si el CONTROLER no cumpliera cualquiera de las obligaciones asumidas en este Contrato y no subsanase dicha situación dentro de los 30 días de haber sido requerido fehacientemente para ella.

Publicidad

El CONTROLER podrá, con la previa autorización del PROMOTOR y el FINANCIERO, dar razonable y adecuada publicidad a la adjudicación y ejecución de este encargo, preservando la debida confidencialidad sobre aquellos aspectos o datos que de acuerdo al presente contrato así lo requieran.

Asimismo, con la previa autorización del FINANCIERO y del PROMOTOR, el CONTROLER podrá exhibir en forma razonable su nombre en el Lugar de las obras, debiendo coordinar con el PROMOTOR, la ubicación y tamaño de dichos carteles.

Legislación y arbitraje

El presente contrato se regirá conforme a la legislación española.

Las partes se someten al arbitraje de equidad del Tribunal Arbitral de [LOCALIDAD] con arreglo a las normas institucionales a realizar por un solo árbitro y cuyo laudo se obligan a cumplir.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad las partes, en la representación en la que actúan, firman el presente contrato por triplicado ejemplar en todas y cada una de sus hojas en el lugar y fecha indicados.

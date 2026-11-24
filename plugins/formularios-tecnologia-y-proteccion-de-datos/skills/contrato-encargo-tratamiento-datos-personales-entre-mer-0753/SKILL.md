---
name: contrato-encargo-tratamiento-datos-personales-entre-mer-0753
description: "Contrato de encargo del tratamiento de datos personales entre responsable y encargado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de encargo del tratamiento de datos personales entre responsable y encargado

> Formulario **MER-0753** del plugin **Contratos tecnológicos, comercio electrónico y protección de datos** (`formularios-tecnologia-y-proteccion-de-datos`) · Mercantil › Tecnología, comercio electrónico y protección de datos · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de encargo del tratamiento de datos personales entre responsable y encargado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de encargo del tratamiento de datos personales entre responsable y encargado” para mi caso». También puedes invocarla directamente con `/formularios-tecnologia-y-proteccion-de-datos:contrato-encargo-tratamiento-datos-personales-entre-mer-0753`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-tecnologia-y-proteccion-de-datos:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos tecnológicos, comercio electrónico y protección de datos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] OBJETO DEL CONTRATO (2 veces)
- [ ] AÑO
- [ ] CATEGORÍAS DE INTERESADOS
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NIF

## Normas que cita el formulario

- art. 28 Ley Orgánica 3/2018
- art. 28.2 RGPD
- art. 33 RGPD
- art. 35 RGPD

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

DECLARAN

I.- Que el responsable del tratamiento ha encargado la prestación de un servicio que consistirá, en esencia, en [OBJETO DEL CONTRATO], exigiendo la prestación contratada el tratamiento de datos personales del RESPONSABLE por el prestador que posee la condición de ENCARGADO. En virtud de ello, en aplicación de lo dispuesto en el artículo 28 del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo de 27 de abril de 2016 relativo a la protección de las personas físicas en lo que respecta al tratamiento de datos personales y a la libre circulación de estos datos, –en adelante RGPD o Reglamento (UE) 2016/679–, y del artículo 28 y siguientes de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, ambas partes suscriben el presente contrato.

La prestación del servicio no comporta coste alguno entre responsable y encargado.

II.- El Responsable del Tratamiento AUTORIZA expresamente y de forma previa la habilitación para realizar una subcontratación de los servicios detallados, del RESPONSABLE del Tratamiento a la entidad [DENOMINACIÓN SOCIAL], S.A. que ostentará la condición de SUBENCARGADO del Tratamiento, conforme establece el art. 28.2 y 4 del RGPD.

La prestación a desarrollar por el ENCARGADO implicará un acceso remoto a datos personales para la realización del estudio, directamente del RESPONSABLE del Tratamiento al SUBENCARGADO.

III.- Que el ENCARGADO del tratamiento garantiza condiciones de confiabilidad y proactividad en el cumplimiento de sus obligaciones derivadas del RGPD y de las obligaciones específicamente establecidas por este contrato y para ello el ENCARGADO DEL TRATAMIENTO es responsable de que el SUBENCARGADO DEL TRATAMIENTO de cumplida respuesta, y con un alto grado de satisfacción, al cuestionario de Evaluación de Riesgos de Proveedores (Supplier Risk Evaluation), que se adjunta como ANEXO II.

Y en virtud de ello,

Acuerdo

Cláusula Primera. -Seguimiento de las instrucciones por el RESPONSABLE

El ENCARGADO tratará los datos personales únicamente siguiendo instrucciones del RESPONSABLE contenidas en este contrato y sus anexos. Cuando, en virtud del cumplimiento de obligaciones legales de naturaleza imperativa el ENCARGADO deba realizar algún tratamiento adicional lo notificará al RESPONSABLE.

En particular, y salvo obligación legal de secreto, se notificará al RESPONSABLE los tratamientos que deriven del deber de colaboración con las Fuerzas y Cuerpos de Seguridad, jueces y tribunales, y autoridades públicas.

Será causa de resolución de este contrato, y del contrato principal, sin indemnización alguna tanto aquellos casos en los que el ENCARGADO no notificase previamente los tratamientos descritos en el párrafo anterior, como en aquellos casos en los que por tratarse de la jurisdicción de un país tercero el responsable del tratamiento considerase que se afecta al derecho fundamental a la protección de datos de los interesados, siempre que el ENCARGADO no tuviera obligación de actuar de dicha manera.

Asimismo, y como se desarrolla en la cláusula décima del presente contrato, el RESPONSABLE podrá exigir responsabilidades al ENCARGADO por aquellos daños que eventualmente pudieran causar por el incumplimiento de lo establecido en la presente cláusula.

Cláusula segunda. -Transferencias internacionales de datos.

Se prohíben aquellos tratamientos que constituyan una transferencia internacional de datos personales a efectos del Reglamento (UE) 2016/679. Únicamente se autoriza al ENCARGADO a realizar los tratamientos en países ubicados en el ESPACIO ECONÓMICO EUROPEO.

Clausula tercera. -Confidencialidad y formación del personal.

El ENCARGADO garantizará que las personas autorizadas para tratar datos personales se hayan comprometido a respetar la confidencialidad o estén sujetas a una obligación de confidencialidad de naturaleza estatutaria. En particular, si es requerido por el RESPONSABLE acreditará la existencia de un compromiso contractual de confidencialidad del personal y/o la formación adecuada del mismo.

Cláusula cuarta. -Características de los sistemas de información del ENCARGADO.

En relación con los tratamientos realizados en las instalaciones, medios y soportes del ENCARGADO, éste garantizará la interoperabilidad de sus sistemas y en todo caso la portabilidad de los datos objeto de tratamiento.

Cláusula quinta. -Medidas de seguridad.

1.-El ENCARGADO para garantizar el cumplimiento de los objetivos de confidencialidad, integridad, disponibilidad y resiliencia de la información adoptará las siguientes medidas de seguridad:

a. Garantiza que ha realizado un análisis de riesgos para la seguridad de sus sistemas y, si procediera, una evaluación de impacto relativa a la protección de datos.

b. Garantiza que posee la capacidad de restaurar la disponibilidad y el acceso a los datos personales de forma rápida en caso de incidente físico o técnico.

c. Con carácter periódico realiza procesos singulares de verificación, evaluación y valoración regulares de la eficacia de las medidas técnicas y organizativas para garantizar la seguridad del tratamiento.

d. Adicionalmente adopta medidas de seguridad consistentes en la seudonimización y/o el cifrado de datos personales

2.-El ENCARGADO se compromete a notificar al RESPONSABLE cualquier incidente de seguridad susceptible de ser considerado violación de la seguridad de los datos personales conforme a lo dispuesto por los artículos 33 y 34 RGPD. Para ello se seguirá el procedimiento descrito en Anexo III de este contrato.

En este sentido, en el Anexo III del presente Contrato de Encargo se desarrollarán las obligaciones específicas en materia de seguridad.

Cláusula sexta. -Colaboración con el RESPONSABLE.

Si resultare necesario, el ENCARGADO cooperará lealmente con el RESPONSABLE cuando fuera necesario llevar a cabo la evaluación de impacto relativa a la protección de datos prevista por el artículo 35 RGPD.

Asimismo, el ENCARGADO asistirá al RESPONSABLE, teniendo en cuenta la naturaleza del tratamiento, a través de medidas técnicas y organizativas apropiadas, siempre que sea posible, para que este pueda cumplir con su obligación de responder a las solicitudes que tengan por objeto el ejercicio de los derechos de los interesados establecidos en el capítulo III del Reglamento (UE) 2016/679. Será causa de resolución de este contrato, y del contrato principal, sin indemnización alguna aquellos casos en los que transcurridos diez días naturales después de haberse requerido, el ENCARGADO no colaborase debidamente.

Asimismo, y como se desarrolla en la cláusula décima del presente contrato, el RESPONSABLE podrá exigir responsabilidades al ENCARGADO por aquellos daños que eventualmente pudieran causar por el incumplimiento de las obligaciones establecidas en esta cláusula.

Cláusula séptima. -Prueba del cumplimiento.

El ENCARGADO pondrá a disposición del RESPONSABLE toda la información necesaria para demostrar el cumplimiento de las obligaciones establecidas en el presente contrato.

Cuando las prestaciones se realicen íntegramente en instalaciones del ENCARGADO, este reconoce el derecho al RESPONSABLE a auditar la actividad del ENCARGADO incluidas las inspecciones a los terminales y medios del personal del ENCARGADO. Es obligación de este último levantar toda expectativa de privacidad de su personal, cuyo acceso no será autorizado de no garantizarse los poderes del RESPONSABLE establecidos en este contrato.

Cláusula octava. -Facultades del RESPONSABLE.

El ENCARGADO informará inmediatamente al RESPONSABLE si, en su opinión, una instrucción infringe el presente Reglamento u otras disposiciones en materia de protección de datos de la Unión o de los Estados miembros.

El ENCARGADO garantizará la adecuada llevanza del Registro de Actividades del tratamiento regulado por el artículo 30.2 y en particular asegurará la debida documentación de las medidas técnicas y organizativas de seguridad.

Cláusula novena. -Subcontratación.

No se autoriza a la subcontratación por el ENCARGADO de los servicios objeto de la prestación, más allá de lo indicado en la Declaración II.

Cláusula décima. -Responsabilidad del RESPONSABLE e indemnizaciones.

Si el ENCARGADO del tratamiento infringe el RGPD al determinar los fines y medios del tratamiento, será considerado responsable del tratamiento. A efectos de este contrato el ENCARGADO también será considerado responsable cuando comunique datos sin autorización o los utilice incumpliendo las estipulaciones de este contrato, respondiendo de las infracciones en que hubiera incurrido personalmente.

Ello sin perjuicio de la exigencia de responsabilidad por los daños que eventualmente se pudieran causar, incluidos aquellos reputacionales que menoscaben el honor corporativo y la imagen pública del RESPONSABLE y, en consecuencia, del RESPONSABLE DEL TRATAMIENTO.

Cláusula undécima. -Finalización de la prestación.

EL ENCARGADO, previa elección del responsable comunicada por él mismo o por el RESPONSABLE, suprimirá o devolverá todos los datos personales una vez finalice la prestación de los servicios de tratamiento, y suprimirá las copias existentes a menos que se requiera la conservación de los datos personales en virtud del Derecho de la Unión o de los Estados miembros. En este último caso, lo hará constar expresamente con indicación específica del plazo de conservación y la norma de la que deriva su obligación.

En caso de que el ENCARGADO tuviera un deber de conservación de los datos conforme a la cláusula novena se le prohíbe cualquier tratamiento distinto de esta conservación.

El procedimiento de devolución se ajustará a lo descrito en el Anexo I a este Contrato.

Cláusula duodécima. -Vigencia.

La vigencia de este Contrato se vincula a la realización de [OBJETO DEL CONTRATO] que deberá realizarse en un plazo de SEIS MESES, desde la suscripción del presente acuerdo. No obstante, no se considerará extinguido hasta la completa devolución o destrucción de los datos. En caso de que el ENCARGADO tuviera un deber de conservación de los datos conforme a la cláusula novena subsistirán todas las obligaciones previstas en este contrato que garantizan la seguridad de los datos sin coste adicional alguno para el RESPONSABLE, o del RESPONSABLE DEL TRATAMIENTO.

Cláusula Decimotercera. -Legislación aplicable y jurisdicción.

El presente contrato se regirá por la normativa española y europea en materia de Protección de Datos de Carácter Personal.

En caso de controversia entre las partes surgida con motivo de la aplicación de este contrato, ambas partes, con renuncia expresa a su propio fuero se someten a la jurisdicción de los Tribunales de

Y para que así conste, y en prueba de conformidad y aceptación de todo cuanto antecede, las partes firman el presente Contrato por duplicado ejemplar y a un sólo efecto en la fecha y lugar indicados en el encabezamiento.

Anexos

ANEXO I – DESCRIPCIÓN DETALLADA DE LOS TRATAMIENTOS.

Objeto de la prestación.
Datos que se facilitan o a los que accede el encargado del tratamiento.

Los tratamientos de datos previstos a realizar, relacionados con el desarrollo de los servicios objeto de la prestación, son, en síntesis, los siguientes: Estructuración, interconexión, extracción.

Para la ejecución de las actividades derivadas de la prestación de servicios, el RESPONSABLE tratará la información que se describe a continuación:

• Nombre y apellidos

• Correo electrónico

• Edad

• Teléfono.

• NIF [NIF]

En cuanto a las categorías de interesados que se verán afectadas por los tratamientos de datos realizados por el RESPONSABLE son las siguientes:

- [CATEGORÍAS DE INTERESADOS]

c) Modo de entrega o acceso a los datos.

La entrega de la información al ENCARGADO se realiza por parte del RESPONSABLE DEL TRATAMIENTO, mediante la entrega de un fichero encriptado con la información debiendo el ENCARGADO aplicar las medidas de seguridad ya sea aplicando el Estándar comprometido en el presente contrato.

En todo caso, tanto el RESPONSABLE como el ENCARGADO en el tratamiento y envío de información personal por medios lógicos o físicos, establecen las siguientes medidas técnicas y organizativas de seguridad idóneas para evitar el acceso no autorizado, la pérdida, la sustracción o la modificación de la información tratada, protegiendo así la confidencialidad, integridad, disponibilidad y resiliencia de los sistemas y la información objeto de tratamiento.

Ejercicio de derechos por parte de los afectados.

En el supuesto de que cualesquiera afectados o interesados ejerzan un derecho en materia de protección de datos de los contemplados en el Capítulo III del RGPD, entre ellos, de acceso, rectificación, supresión y portabilidad de sus datos, de limitación y oposición, así como a no ser objeto de decisiones basadas únicamente en el tratamiento automatizado de datos; el ENCARGADO DEL TRATAMIENTO, lo debe notificar al RESPONSABLE DEL TRATAMIENTO sin demora, y en todo caso, en el plazo máximo de 24 horas desde tener constancia del ejercicio del derecho.

f) Devolución de los datos.

Una vez cumplida la prestación de los servicios:

El ENCARGADO devolverá al RESPONSABLE DEL TRATAMIENTO los datos de carácter personal y, si procede, los soportes donde consten. Asimismo, suprimirá todos los datos y copias existentes en los equipos informativos, pudiendo conservar una copia, con los datos debidamente bloqueados, mientras puedan derivarse responsabilidades de la ejecución de la prestación.

Así, en un plazo de 10 días hábiles tras la finalización de la prestación de servicios, el ENCARGADO DEL TRATAMIENTO deberá aportar un certificado acreditativo de la supresión de la información. En el caso que sea necesaria su conservación, porque así lo regula la legislación aplicable, se deberá indicar en el mismo.

1.- Es imprescindible, para verificar el grado de cumplimiento normativo en protección de datos, con base en la diligencia debida del responsable del tratamiento en la elección de sus RESPONSABLES, que éstos den cumplida respuesta, y con un alto grado de satisfacción, al siguiente cuestionario que deberá ser analizado, una vez cumplimentado por parte del ENCARGADO DEL TRATAMIENTO.

2.- El ENCARGADO DEL TRATAMIENTO debe cumplimentar y remitir en el plazo de SIETE días previamente a la ejecución del contrato, al RESPONSABLE DEL TRATAMIENTO Y AL RESPONSABLE DEL MISMO, el siguiente cuestionario, adjuntando las EVIDENCIAS DOCUMENTALES, que demuestren el cumplimiento normativo.

3.- De no verificarse, o de resultar insuficiente desde el punto de vista de protección de datos y seguridad de la información, a criterio del RESPONSABLE DEL TRATAMIENTO, éste puede rescindir unilateralmente el contrato de la prestación del servicio principal, sin ningún tipo de penalización o compensación por ello.

Fecha: ___/_____/20____
1.- Certificación RGPD	Respuesta
Importante:En caso de disponer de la certificación RGPD no será necesario completar el resto del cuestionario.
1.1 ¿Se han adoptado las medidas técnicas y organizativas exigibles por la normativa de protección de datos? (Serán evaluadas y vinculantes por el cuestionario)
2.- Cuestiones generales
2.1 ¿Dispone de una política en materia de protección de datos adaptada a RGPD?, En caso afirmativa, debe ser adjuntada.
2.2 ¿Se imparte formación en materia de protección de datos a sus empleados? En caso afirmativo, adjuntar evidencia.
2.3 Los empleados que vayan a acceder a los datos personales del cliente, ¿firman cláusulas de confidencialidad en materia de protección de datos? En caso afirmativo, adjuntar evidencia.
2.4 ¿Dispone de un procedimiento para gestionar solicitudes de ejercicio de derechos de interesados y/o comunicar las mismas al responsable (cliente)? En caso afirmativo, debe ser adjuntada.
2.5 ¿Se ha designado un Delegado de Protección de Datos (DPO) o un responsable de protección de datos? En caso afirmativo, adjuntar designación formal o evidencia de designación formal.
3.- Transferencias internacionales de datos

3.1 ¿El servicio almacena y procesará los datos (incluso las copias de seguridad) en países del Espacio Económico Europeo * o en alguno de los siguientes países (Andorra, Argentina, Canadá, Suiza, Islas Feroe, Guernsey, Israel, Isla de Man, Jersey, Nueva Zelanda, Japón y Uruguay)?

(*EEE lo componen los países miembros de la UE + Islandia, Liechtenstein y Noruega)

3.2 Responda afirmativamente si cumple alguno de los siguientes casos:

En el caso de que el tratamiento de los datos vaya a ser realizado por un proveedor establecido en EE.UU., Este se encuentra el mismo adherido a los Acuerdos de Privacy Shield (En caso afirmativo adjuntar evidencia de la adherencia al Privacy Shield).

La transferencia internacional de datos está legitimada por el establecimiento de Binding Corporate Rules o Normas Corporativas Vinculantes entre empresas del Grupo del proveedor aprobadas por alguna Autoridad de Control (En caso afirmativo adjuntar evidencia de autorización por parte de la autoridad de control)

La transferencia internacional de datos está legitimada por medio de garantías adecuadas y los interesados cuentan con derechos exigibles y acciones legales efectivas.

4.- Incidentes de seguridad
4.1 ¿Dispone de procedimientos de actuación, de cara a informar al responsable sin dilación indebida, en caso de que se produzca un incidente de seguridad que afecte a los datos de carácter personal? En caso afirmativo, adjuntar procedimiento.
4.2 Dentro del procedimiento de comunicación de incidentes de seguridad al responsable (cliente), ¿se describe la naturaleza de la incidencia, el número aproximado y categorías de datos, la información de contacto del DPO, la descripción de las medidas propuestas para remediar o mitigar la incidencia, así como las posibles consecuencias de dicha incidencia?
4.3 En caso de un incidente de seguridad, ¿el proveedor dispone de un protocolo de mitigación? En caso afirmativo, adjuntar el protocolo correspondiente.
5.- Evaluaciones de impacto (PIA)
5.1 ¿Dispone de una metodología para la realización de evaluaciones de impacto (DPIAs) relativa a la protección de datos? En caso afirmativo, adjuntar la metodología utilizada.
5.2 En caso de que exista la obligación de tener designado un Delegado de Protección de Datos, ¿la realización de las evaluaciones de impacto cuenta con el asesoramiento del DPO o el responsable de protección de datos? En caso afirmativo, adjuntar evidencia del asesoramiento del DPO o responsable de protección de datos.

ANEXO III.-OBLIGACIONES ESPECÍFICAS EN MATERIA DE SEGURIDAD.

a) Notificación de violaciones de seguridad.

El ENCARGADO notificará al RESPONSABLE DEL TRATAMIENTO, sin dilación indebida, y en un plazo máximo de 24 horas desde su conocimiento, junto con toda la información relevante para documentar y comunicar la incidencia en el email: [CORREO ELECTRÓNICO]

La información que se debe incorporar en la notificación, si se conoce, es la siguiente:

a. Descripción de la naturaleza de la violación de la seguridad de los datos personales, inclusive, cuando sea posible, las categorías y el número aproximado de interesados afectados, y las categorías y el número aproximado de registros de datos personales afectados.

b. El nombre y los datos de contacto del delegado de protección de datos o de otro punto de contacto en el que pueda obtenerse más información.

c. Descripción de las posibles consecuencias de la violación de la seguridad de los datos personales.

d. Descripción de las medidas adoptadas o propuestas para poner remedio a la violación de la seguridad de los datos personales, incluyendo, si procede, las medidas adoptadas para mitigar los posibles efectos negativos.

Si no es posible facilitar la información simultáneamente, y en la medida en que no lo sea, la información se facilitará de manera gradual sin dilación indebida.

Además, el ENCARGADO deberá cumplir con las instrucciones que el RESPONSABLE DEL TRATAMIENTO le dirija en cada momento relativas a la notificación y documentación asociada a posibles incidentes de seguridad, en coherencia con los protocolos o procedimientos que se hayan adoptado.

b) Obligaciones de seguridad del personal del ENCARGADO del tratamiento.

El ENCARGADO DEL TRATAMIENTO debe informar, a requerimiento del RESPONSABLE DEL TRATAMIENTO acerca de:

• Las funciones de los usuarios o perfiles de usuarios con acceso a los datos de carácter personal y a los sistemas de información que interviene en la concreta prestación del servicio;

• Las funciones de control o autorizaciones delegadas;

• La formación del personal para que conozca de una forma comprensible las normas de seguridad que afecten al desarrollo de sus funciones, así como las consecuencias en que pudiera incurrir en caso de incumplimiento.

c) Medidas de seguridad adoptadas.

Se detallan en el ANEXO IV, que acompaña al presente contrato.

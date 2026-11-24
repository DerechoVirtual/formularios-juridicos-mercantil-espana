---
name: contrato-servicios-profesionales-arquitectura-mer-0553
description: "Contrato de servicios profesionales de arquitectura. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicios profesionales de arquitectura

> Formulario **MER-0553** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicios profesionales de arquitectura» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicios profesionales de arquitectura” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-servicios-profesionales-arquitectura-mer-0553`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DESCRIPCIÓN DEL PROYECTO
- [ ] DIRECCIÓN
- [ ] DOMICILIO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE COLEGIADO/A
- [ ] NÚMERO
- [ ] OBJETO DEL CONTRATO
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

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], con número de colegiado [Nº DE COLEGIADO/A], Arquitecto perteneciente al Colegio Oficial de Arquitectos Vasco Navarro y estudio profesional en [DIRECCIÓN], con documento nacional de identidad número

[ELEGIR UNA OPCIÓN: Intervienen / Si intervienen en nombre y representación de alguien / Opción 1: Si intervienen en nombre y representación de alguien / Si intervienen en su propio nombre y derecho / Opción 2: Si intervienen en su propio nombre y derecho]

EXPONEN

PRIMERO.- Que EL ARQUITECTO se dedica habitualmente a la prestación de servicios de [ACTIVIDAD]

SEGUNDO.- Que EL CLIENTE precisa de los servicios de EL ARQUITECTO para [OBJETO DEL CONTRATO]

TERCERO.- Que ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

EL CLIENTE encarga al ARQUITECTO que acepta el encargo de redacción del proyecto [DESCRIPCIÓN DEL PROYECTO]

El Presupuesto estimado asciende a [IMPORTE] euros.

Honorarios y forma de pago

Los honorarios del Arquitecto por la redacción del proyecto, dirección y liquidación de la obra, serán la cifra resultante de la aplicación del [PORCENTAJE] % al presupuesto de ejecución material de la fase correspondiente del trabajo.

Todos los pagos deberán efectuarse en la sede en [LOCALIDAD] del Colegio Oficial de Arquitectos [LOCALIDAD], según las normas de la citada entidad.

Los porcentajes de los honorarios a abonar a la entrega de cada fase del trabajo realizado serán: Anteproyecto 25%, Proyecto Básico 40%, Proyecto de Ejecución 70%, Dirección 100%. Se descontarán los importes abonados en una fase anterior del trabajo.

Durante la ejecución de las obras, y en concepto de cantidad a cuenta de sus honorarios, el Cliente abonará al Arquitecto las certificaciones parciales de la obra ejecutada, en proporción a su importe. Se realizarán un mínimo de una certificación anual.

Los pagos a que se refieren las cláusulas anteriores habrán de hacerse efectivos dentro de los [Nº] meses de haberse exigido su pago. Transcurrido dicho plazo sin haberse efectuado, el importe de la cantidad insatisfecha devengará, sin necesidad de requerimiento ni intimación previos, el interés aplicado por el Banco Central Europeo más siete puntos.

Anticipos a cuenta

En este acto, y en concepto de provisión de fondos, el Cliente entrega al Arquitecto la suma de [IMPORTE] euros. Al hacerse la liquidación final de honorarios, se procederá a liquidar la provisión de fondos recibida.

Visado

El cliente expresamente solicita el visado del trabajo profesional encargado cuyo importe será abonado por [NOMBRE DE LA PARTE]

Cuando se haya efectuado el pago, el Colegio pondrá a disposición del Cliente (o persona autorizada por escrito por él), [Nº] ejemplares del proyecto visado, para que proceda a solicitar la licencia de obras y las ofertas de los posibles contratistas. Si el Cliente deseara obtener otras copias del proyecto, serán de su cuenta los gastos necesarios para la obtención de las mismas.

Gastos

El cliente, con conocimiento de que el Arquitecto tiene su residencia fuera del término municipal en que radican las obras, acepta el abono de [IMPORTE] euros por cada visita de obra en concepto de gastos ocasionados al Arquitecto por desplazamientos.

Compatibilidad

El Arquitecto aquí interviniente declara que no se encuentra afectado por ninguna causa legal que le impida asumir el trabajo encomendado.

Mejoras o modificaciones

Cuando en el curso de la realización de las obras se introdujeran en las mismas, por decisión del Cliente, alteraciones que implicasen modificaciones de las determinaciones del proyecto, o cuando habiendo el Arquitecto puesto en conocimiento del Cliente la desobediencia del constructor a sus órdenes escritas, no se adoptaran por aquél las medidas necesarias para la inmediata corrección de esta conducta, podrá el Arquitecto resolver el contrato con derecho al cobro de los trabajos hasta el momento realizados y a la indemnización prevista en la cláusula siguiente.

Resolución del encargo

El desistimiento a proseguir los trabajos encargados por cualquiera de las dos partes, no surtirá efecto hasta que no se comunique por escrito a la otra parte tal resolución. En caso de desistimiento unilateral del Cliente, éste deberá abonar al Arquitecto el importe de los trabajos realizados hasta el momento, e indemnizarle con un 30 % de los honorarios o percepciones que le quedasen por percibir por aquellas fases encargadas que ya no podrá llevar a cabo como consecuencia de esa resolución. Esta última cantidad tendrá el concepto de indemnización por daños y perjuicios voluntariamente convenida.

Retraso

Si las obras no se iniciaran durante un plazo de [Nº] meses o, una vez iniciadas, permanecieren paralizadas por causas no imputables al Arquitecto durante un plazo de [Nº] meses, el Arquitecto podrá resolver el presente contrato, dando por terminada su intervención tras certificar el estado en que las obras se encuentran y notificarlo al Cliente y a la Administración otorgante de la licencia, procediéndose a la oportuna liquidación de los suplidos y honorarios devengados. En tal supuesto será de aplicación lo previsto en la cláusula anterior.

Exclusividad

Salvo autorización escrita del Arquitecto, el proyecto por él redactado, o partes del mismo, no podrá ser utilizado más que para la edificación en la parcela a que el presente contrato se refiere, únicos derechos inherentes a la propiedad intelectual del Arquitecto que pueden entenderse cedidos en virtud del presente contrato.

Normativa urbanística

En el cumplimiento de su prestación, el Arquitecto se atendrá a lo dispuesto en la normativa de ordenación urbanística aplicable por razón del emplazamiento del solar y a la Normativa Técnica de obligado cumplimiento y demás disposiciones técnicas de obligado cumplimiento, observando, además, los preceptos de la legislación reguladora de su ejercicio profesional.

Autorización para subcontratación

La prestación de servicios deberá ser realizado por EL ARQUITECTO con los medios personales y materiales integrantes de su propia organización empresarial, utilizando vehículos de los que disponga en tal concepto.

No obstante, cuando precise de la colaboración de otro profesional, no quedará desvirtuada su condición de prestador de servicios único frente a EL CLIENTE.

En todo caso, las personas a quienes subcontrate habrán de reunir las condiciones y preparación adecuadas para la prestación de servicios encomendada.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

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

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE PRESTACIÓN DE SERVICIOS DE ARQUITECTURA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(EL ARQUITECTO)

Fdo. Don [NOMBRE Y APELLIDOS]

(EL CLIENTE)

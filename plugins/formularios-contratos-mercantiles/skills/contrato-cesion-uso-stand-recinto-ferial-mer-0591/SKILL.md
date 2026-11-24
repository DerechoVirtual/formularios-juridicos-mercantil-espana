---
name: contrato-cesion-uso-stand-recinto-ferial-mer-0591
description: "Contrato de cesión de uso de un stand en un recinto ferial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cesión de uso de un stand en un recinto ferial

> Formulario **MER-0591** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que quien explota unas instalaciones feriales (LA ARRENDADORA) cede a otra persona (LA ARRENDATARIA) un espacio, y su stand, para promocionar sus productos o servicios durante la celebración de un certamen, a cambio de un precio.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cesión de uso de un stand en un recinto ferial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cesión de uso de un stand en un recinto ferial” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-cesion-uso-stand-recinto-ferial-mer-0591`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DÍA (8 veces)
- [ ] IMPORTE (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] MES (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] NÚMERO (6 veces)
- [ ] AÑO (5 veces)
- [ ] PROVINCIA (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE EN LETRA (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] SEDE (2 veces)
- [ ] DESCRIPCIÓN DEL ESPACIO, CON UBICACIÓN Y SUPERFICIE ÚTIL
- [ ] DIRECCIÓN
- [ ] ENTIDAD BANCARIA
- [ ] EXPOSICIÓN COMERCIAL DE QUE SE TRATE
- [ ] IBAN
- [ ] NOMBRE DEL CERTAMEN
- [ ] NOMBRE DEL RECINTO
- [ ] NORMAS DE MONTAJE
- [ ] PORCENTAJE
- [ ] SUCURSAL
- [ ] TIPO DE IVA

## Normas que cita el formulario

- art. 1365 Código Civil
- art. 34 Ley 60/2003

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…ato por la sola causa de la declaración de concurso de cualquiera de las partes.»: el original citaba el art. 61.3 de la derogada Ley 22/2003, Concursal; comprobar el artículo equivalente en el texto refundido vigente (RDLeg 1/2020).
- Junto a «…bienes de alguna de ellas, a menos que se garantice de cualquier forma la deuda.»: el original incluía como causa la suspensión de pagos, la quiebra o el concurso; la resolución por la sola declaración de concurso se tiene por no puesta (art. 156 del texto refundido de la Ley Concursal, véanse las notas de ayuda).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE AYUDA

El contrato de arrendamiento de stand es un contrato mediante el cual una persona física o jurídica que explota las instalaciones feriales, el arrendador, alquila a otra, el arrendatario, un espacio para promocionar sus productos o servicios, así como un stand apropiado, a cambio de un precio.

En cuanto a los intervinientes, si se trata de una persona física que interviene en su propio nombre y derecho es preciso hacer constar tal extremo. Lo mismo sucede si interviene en representación de otra persona física; en este caso será necesario describir la fuente de la que dimana su representación, ya sea esta legal o convencional. En el mismo sentido, si se trata de una persona física que actúa en beneficio de una sociedad de gananciales, de una sociedad civil irregular o de una comunidad de bienes, puesto que en estos casos no existe una personalidad jurídica diferente de la de los miembros que la integran.

De conformidad con el artículo 156 del texto refundido de la Ley Concursal, se tendrán por no puestas las cláusulas que establezcan la facultad de resolución o la extinción del contrato por la sola causa de la declaración de concurso de cualquiera de las partes.

En cuanto al retraso en el pago, recuérdese que la Ley 3/2004, de 29 de diciembre, por la que se establecen medidas de lucha contra la morosidad en las operaciones comerciales, establece la aplicación automática de un tipo de interés de demora, sin necesidad de aviso de vencimiento ni de intimación alguna por parte del acreedor. No obstante, el acreedor solo podrá exigir el pago de los intereses de demora cuando haya cumplido con las obligaciones contractuales y legales que le incumbían y cuando el retraso en el pago no sea imputable a su conducta. Si se dan estas condiciones, se devengará el interés de demora contractual o el fijado legalmente conforme a dicha ley.


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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte:

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL] (si fuera casado/a, conviene expresar el régimen económico matrimonial y el nombre y apellidos del cónyuge, puesto que el Código Civil contempla la posibilidad de comprometer los bienes comunes o gananciales, art. 1365 del Código Civil), vecino/a de [LOCALIDAD], domiciliado/a en [DOMICILIO], con documento nacional de identidad número [DNI/NIE].

De otra:

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL] (si fuera casado/a, conviene expresar el régimen económico matrimonial y el nombre y apellidos del cónyuge, art. 1365 del Código Civil), vecino/a de [LOCALIDAD], domiciliado/a en [DOMICILIO], con documento nacional de identidad número [DNI/NIE].

INTERVIENEN

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [DENOMINACIÓN SOCIAL], en lo sucesivo «LA ARRENDADORA», en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [PROVINCIA] y vigente, según manifiesta.

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [DENOMINACIÓN SOCIAL], en lo sucesivo «LA ARRENDATARIA», en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [PROVINCIA] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE ARRENDAMIENTO DE STAND y, a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que LA ARRENDADORA tiene como actividad principal la organización y gestión de ferias y exposiciones comerciales en el recinto ferial [NOMBRE DEL RECINTO], sito en [DIRECCIÓN].

SEGUNDO.- Que, en el marco de su actividad profesional, LA ARRENDADORA organiza el certamen [NOMBRE DEL CERTAMEN], que se celebrará entre los días [DÍA] y [DÍA] de [MES] de [AÑO] en sus instalaciones.

TERCERO.- Que LA ARRENDATARIA desea arrendar el siguiente espacio a fin de promocionar sus productos/servicios: [DESCRIPCIÓN DEL ESPACIO, CON UBICACIÓN Y SUPERFICIE ÚTIL].

CUARTO.- Que, en virtud de las consideraciones precedentes, ambas partes, de común acuerdo, llevan a efecto el presente CONTRATO DE ARRENDAMIENTO DE STAND con arreglo a las siguientes

CLÁUSULAS

PRIMERA.- Objeto

LA ARRENDADORA cede el uso del espacio descrito en el Exponendo Tercero a LA ARRENDATARIA para la promoción de sus productos/servicios.

SEGUNDA.- Precio

Importe del alquiler

El precio del arrendamiento del stand descrito en el Exponendo Tercero se concreta en la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €), más el Impuesto sobre el Valor Añadido correspondiente al [TIPO DE IVA] %, esto es, [IMPORTE EN LETRA] euros ([IMPORTE] €) adicionales.

Pago del alquiler

El pago se efectuará entre los días [DÍA] y [DÍA] de [MES] en la cuenta corriente núm. [IBAN] que LA ARRENDADORA tiene suscrita con la entidad [ENTIDAD BANCARIA] en su sucursal [SUCURSAL]. [Si se trata de una transferencia internacional será preciso conocer el código SWIFT o BIC (8 u 11 dígitos alfanuméricos que contienen la identificación del nombre y oficina del banco y el país donde se encuentra).]

Retraso en el pago

El retraso en más de [NÚMERO] días en cualquiera de los pagos dará derecho a LA ARRENDADORA a exigir a LA ARRENDATARIA un interés moratorio del [PORCENTAJE] %.

TERCERA.- Duración del contrato

La duración del presente contrato es la comprendida entre el [DÍA] de [MES] de [AÑO] y el [DÍA] de [MES] de [AÑO], coincidiendo con la celebración del certamen. Si por exigencias de las autoridades se aplazara la celebración del certamen, este contrato se entenderá prorrogado tácitamente a las fechas en que se concrete la realización del certamen.

CUARTA.- Instalación del stand

LA ARRENDATARIA, una vez abonado el pago del espacio cedido, podrá comenzar la instalación del stand sobre el espacio asignado a partir del [DÍA] de [MES] de [AÑO], previo pago del canon de montaje, que asciende a [IMPORTE] euros ([IMPORTE] €), y retirada de la autorización de montaje y pases de trabajo.

La instalación del stand se llevará a cabo de conformidad con las normas de montaje fijadas por LA ARRENDADORA, que se adjuntan como Anexo I.

QUINTA.- Obligaciones de la arrendadora

LA ARRENDADORA se obliga a:

1. Poner a disposición de LA ARRENDATARIA el espacio cedido para la instalación de un stand promocional de las características descritas en el Exponendo Tercero.

2. Mantener el horario de apertura y cierre del certamen.

3. Poner a disposición de LA ARRENDATARIA la documentación oficial de [EXPOSICIÓN COMERCIAL DE QUE SE TRATE].

4. Mantener en perfectas condiciones de limpieza las zonas de acceso y los locales y zonas comunes del recinto ferial.

5. Suministrar la iluminación y climatización propias del pabellón y abonar los gastos correspondientes, sin cargo alguno para LA ARRENDATARIA.

SEXTA.- Obligaciones de la arrendataria

LA ARRENDATARIA se obliga a:

1. Instalar y decorar el espacio cedido, por su cuenta y a su cargo.

2. No exponer productos inflamables, peligrosos, en mal estado o que de cualquier otra manera supusieran o pudieran suponer riesgo o amenaza para la integridad o salud de las personas físicas.

3. Desmontar el stand en el plazo de [NÚMERO] días desde la finalización del certamen, así como retirar los productos en él expuestos. En caso contrario, LA ARRENDADORA llevará a cabo esta operación a cargo de LA ARRENDATARIA.

4. No disponer del espacio cedido por el presente contrato vendiéndolo, subarrendándolo ni subrogando a persona alguna en sus derechos y obligaciones, salvo autorización por escrito de LA ARRENDADORA.

5. Responder de la actuación de sus empleados y personal subcontratado.

6. Atender el stand durante el horario de apertura del certamen y no abandonarlo mientras los visitantes del evento no hayan desalojado el recinto.

SÉPTIMA.- Reducción del espacio

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— A instancia de la arrendadora: LA ARRENDADORA se reserva el derecho a reducir la superficie arrendada a LA ARRENDATARIA, comprometiéndose en tal caso a restituir la parte proporcional del precio, sin derecho a compensación alguna por parte de LA ARRENDATARIA y excluyéndose cualquier otra reclamación por parte de esta.

— A instancia de la arrendataria: Si LA ARRENDATARIA solicitara a LA ARRENDADORA una reducción de espacio, perderá el espacio asignado, pudiendo LA ARRENDADORA reubicarlo en los espacios que queden libres.

OCTAVA.- Seguro

LA ARRENDADORA contratará un seguro que cubra el riesgo de daños o pérdida provocados por incendios, agua, fenómenos naturales y robo que puedan sufrir las muestras, mercancías o cualesquiera otros bienes que LA ARRENDATARIA tuviera en el recinto ferial durante la celebración del certamen.

LA ARRENDATARIA proporcionará a LA ARRENDADORA, a su solicitud, pruebas de la existencia de dicho seguro.

NOVENA.- Resolución del contrato

El contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las partes cuando medie incumplimiento grave de las obligaciones pactadas.

2. Por acuerdo de las partes por escrito.

3. La extinción de la personalidad jurídica de cualquiera de las partes o el embargo de bienes de alguna de ellas, a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la parte que pretenda resolver el presente contrato alegando incumplimiento de la contraparte deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [NÚMERO] días a la parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad de opción, sin necesidad de remitir previamente el antedicho requerimiento.

La resolución del contrato por esta causa producirá los mismos efectos que el incumplimiento de la obligación de pago en lo que a recuperación del espacio e indemnización de los daños y perjuicios respecta.

DÉCIMA.- Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de [ELEGIR: LA ARRENDADORA / LA ARRENDATARIA / ambas partes por mitad].

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios de Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

UNDÉCIMA.- Sumisión

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Sumisión a tribunales, sin cláusula penal: Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los Juzgados y Tribunales de [SEDE], en [PROVINCIA], renunciando expresamente a su fuero propio si lo tuvieran. El presente contrato tiene carácter mercantil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

— Sumisión a tribunales, con cláusula penal: Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los Juzgados y Tribunales de [SEDE], en [PROVINCIA], renunciando expresamente a su fuero propio si lo tuvieran. En el caso de que la parte o partes que hubieran resultado condenadas en el fallo de la sentencia no cumplieran voluntariamente con el fallo en el plazo de [NÚMERO] días, deberán abonar a quien le hubiera vencido en el pleito la cantidad de [IMPORTE] euros ([IMPORTE] €), sin perjuicio de la indemnización por daños y perjuicios que pudiera corresponderles. El presente contrato tiene carácter mercantil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

— Sumisión a arbitraje, sin cláusula penal: Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD]. Según el artículo 34 de la Ley 60/2003, de 23 de diciembre, de Arbitraje, los árbitros solo decidirán en equidad si las partes les han autorizado expresamente para ello. El presente contrato tiene carácter mercantil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

— Sumisión a arbitraje, con cláusula penal: Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD]. Según el artículo 34 de la Ley 60/2003, de 23 de diciembre, de Arbitraje, los árbitros solo decidirán en equidad si las partes les han autorizado expresamente para ello. En el caso de que la parte o partes que hubieran resultado condenadas en el laudo no cumplieran voluntariamente con el fallo del mismo en el plazo de [NÚMERO] días, deberán abonar a quien le hubiera vencido en el procedimiento la cantidad de [IMPORTE] euros ([IMPORTE] €), sin perjuicio de la indemnización por daños y perjuicios que pudiera corresponderles. El presente contrato tiene carácter mercantil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

DUODÉCIMA.- Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada, en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

DECIMOTERCERA.- Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y solo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso, las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son solo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este contrato.

DECIMOCUARTA.- Protección de datos

En el caso de que el cumplimiento de este contrato suponga la necesidad de acceder a datos de carácter personal, las partes, como encargadas del tratamiento, quedan obligadas al cumplimiento del Reglamento (UE) 2016/679 (RGPD), de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [NÚMERO] folios del presente CONTRATO DE ARRENDAMIENTO DE STAND, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. D./Dña. [NOMBRE Y APELLIDOS] (LA ARRENDADORA)

Fdo. D./Dña. [NOMBRE Y APELLIDOS] (LA ARRENDATARIA)

ANEXO I.- Normas de montaje fijadas por LA ARRENDADORA: [NORMAS DE MONTAJE]

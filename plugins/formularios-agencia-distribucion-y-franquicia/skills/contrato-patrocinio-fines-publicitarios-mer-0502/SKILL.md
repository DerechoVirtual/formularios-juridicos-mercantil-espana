---
name: contrato-patrocinio-fines-publicitarios-mer-0502
description: "Contrato de patrocinio con fines publicitarios. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de patrocinio con fines publicitarios

> Formulario **MER-0502** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Contrato de patrocinio publicitario por el que el patrocinado (persona física o jurídica) se compromete a colaborar en la publicidad del patrocinador a cambio de una ayuda económica para la realización de su actividad deportiva, benéfica, cultural, científica o de cualquier otra índole (art. 22 de la Ley 34/1988, General de Publicidad).

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de patrocinio con fines publicitarios» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de patrocinio con fines publicitarios” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-patrocinio-fines-publicitarios-mer-0502`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DÍA (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] NÚMERO (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] MES (4 veces)
- [ ] PORCENTAJE (4 veces)
- [ ] PROVINCIA (4 veces)
- [ ] ENTIDAD BANCARIA (3 veces)
- [ ] IBAN (3 veces)
- [ ] SUCURSAL (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] MEDIO ESCRITO (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] PERSONA FÍSICA O JURÍDICA O ENTIDAD QUE RECIBE LA DONACIÓN (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] CALENDARIO
- [ ] CANALES DE TELEVISIÓN, CON FRECUENCIA Y FRANJA HORARIA
- [ ] DESCRIPCIÓN DE LA ACTIVIDAD
- [ ] DESCRIPCIÓN DE LOS ACTOS PÚBLICOS QUE LLEVA A CABO
- [ ] EMISORAS DE RADIO, CON FRECUENCIA Y FRANJA HORARIA
- [ ] IMPORTE DE LA CONTRAPRESTACIÓN
- [ ] IMPORTE EN LETRA
- [ ] LUGAR
- [ ] MÓDULO
- [ ] OBJETO SOCIAL
- [ ] OBRA, ACTIVIDAD O EVENTO
- [ ] TIPO DE ACTOS
- [ ] UBICACIÓN PERIÓDICA

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…bienes de alguna de ellas, a menos que se garantice de cualquier forma la deuda.»: el original incluía como causa la suspensión de pagos, la quiebra o el concurso; la resolución por la sola declaración de concurso se tiene por no puesta (véanse las notas de ayuda).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE AYUDA

El contrato de patrocinio publicitario es un contrato mediante el cual una persona física o jurídica, el patrocinado, se compromete a colaborar en la publicidad de otra, el patrocinador, a cambio de una ayuda económica para la realización de su actividad deportiva, benéfica, cultural, científica o de cualquier otra índole. Está regulado principalmente en el artículo 22 de la Ley 34/1988, de 11 de noviembre, General de Publicidad.

Si se trata de una persona física que interviene en su propio nombre y derecho, es preciso hacer constar tal extremo. Lo mismo sucede si interviene en representación de otra persona física; en este caso será necesario describir la fuente de la que dimana su representación, ya sea esta legal o convencional. En el mismo sentido, si se trata de una persona física que actúa en beneficio de una sociedad de gananciales, de una sociedad civil irregular o de una comunidad de bienes, puesto que en estos casos no existe una personalidad jurídica diferente de la de los miembros que la integran.

Para que dé derecho a la resolución del contrato, tiene que ser un incumplimiento de entidad suficiente. En este sentido, como dicen la sentencia de la Audiencia Provincial de Tarragona de 28 de mayo de 2002 y la sentencia de la Audiencia Provincial de Baleares de 16 de junio de 2003, «los errores habidos en el anuncio carecen de la entidad necesaria para entender incumplida la obligación asumida por la actora y ajustado a derecho el incumplimiento del pago del precio, pues no se está ante un supuesto de aliud pro alio o ante una falta de identidad de la prestación», pues, como indica la última de las resoluciones mencionadas, «los potenciales clientes de la empresa demandada pudieron llegar a conocer la empresa demandada y sus productos aunque el error sufrido pudiera dificultar, que no anular, el hipotético contacto con ella». En el mismo sentido, la sentencia de la Audiencia Provincial de Navarra (Sección 3ª) de 14 de diciembre de 2004.

De conformidad con el texto refundido de la Ley Concursal (arts. 156 a 158), se tienen por no puestas las cláusulas que establezcan la facultad de resolución o la extinción del contrato por la sola causa de la declaración de concurso de cualquiera de las partes.

La conceptuación de las arras penales por el artículo 1152 del Código Civil conduce a afirmar que, salvo que las partes acuerden lo contrario, la satisfacción de la pena sustituye a la indemnización de daños y abono de intereses en caso de falta de cumplimiento, desempeñando así una función propiamente liquidatoria. En el mismo sentido, la sentencia del Tribunal Supremo (Sala de lo Civil, Sección 1ª) de 27 de junio de 2007.


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

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [DENOMINACIÓN SOCIAL], en lo sucesivo «LA PATROCINADORA», en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [PROVINCIA] y vigente, según manifiesta.

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [DENOMINACIÓN SOCIAL], en lo sucesivo «EL PATROCINADO», en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [PROVINCIA] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE PATROCINIO PUBLICITARIO y, a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que LA PATROCINADORA es una mercantil que tiene por objeto social [OBJETO SOCIAL].

SEGUNDO.- Que EL PATROCINADO es una mercantil que se dedica a [DESCRIPCIÓN DE LA ACTIVIDAD] y organiza habitualmente actos de [DESCRIPCIÓN DE LOS ACTOS PÚBLICOS QUE LLEVA A CABO], estando interesado en hacer publicidad, durante tales actos públicos, de los productos de LA PATROCINADORA a cambio de una contraprestación económica.

TERCERO.- Que, en vista de lo anterior, ambas partes, de común acuerdo, llevan a efecto el presente contrato con arreglo a las siguientes

CLÁUSULAS

PRIMERA.- Objeto

EL PATROCINADO se compromete a hacer publicidad de los productos de LA PATROCINADORA en cuantos actos públicos [ELEGIR: deportivos / culturales / benéficos / OTROS] comparezca, sean estos [TIPO DE ACTOS], ruedas de prensa, comparecencias oficiales o cualquier otro que se efectúe en nombre de EL PATROCINADO.

SEGUNDA.- Contraprestación

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Pago de una cantidad.

Cuantía: LA PATROCINADORA se compromete a aportar la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE] €).

Pago de la contraprestación: El pago se efectuará entre los días [DÍA] y [DÍA] de [MES] en la cuenta corriente nº [IBAN] que EL PATROCINADO tiene suscrita con la entidad [ENTIDAD BANCARIA] en su sucursal [SUCURSAL]. [Si se trata de una transferencia internacional será preciso conocer el código SWIFT o BIC (8 u 11 dígitos alfanuméricos que contienen la identificación del nombre y oficina del banco y el país donde se encuentra).]

Retraso en el pago: El retraso en más de [NÚMERO] días en cualquiera de los pagos dará derecho a EL PATROCINADO a exigir a LA PATROCINADORA un interés moratorio del [PORCENTAJE] % respecto de cada uno de los pagos no satisfechos puntualmente.

— Asunción de gastos.

Contraprestación: LA PATROCINADORA sufragará el [PORCENTAJE] % del coste de [OBRA, ACTIVIDAD O EVENTO] según presupuesto que se adjunta en el Anexo I del presente contrato. EL PATROCINADO se compromete a entregar recibo por las cantidades percibidas, en el que se especificará además el destino de las mismas.

Pago de la contraprestación: El abono de los importes adelantados por EL PATROCINADO se efectuará entre los días [DÍA] y [DÍA] de [MES] en la cuenta corriente nº [IBAN] que EL PATROCINADO tiene suscrita con la entidad [ENTIDAD BANCARIA] en su sucursal [SUCURSAL]. [Si se trata de una transferencia internacional será preciso conocer el código SWIFT o BIC.]

Retraso en el pago: El retraso en más de [NÚMERO] días en cualquiera de los pagos dará derecho a EL PATROCINADO a exigir a LA PATROCINADORA un interés moratorio del [PORCENTAJE] % respecto de cada uno de los pagos no satisfechos puntualmente.

— Donación de la contraprestación: EL PATROCINADO donará la contraprestación abonada por LA PATROCINADORA a favor de [PERSONA FÍSICA O JURÍDICA O ENTIDAD QUE RECIBE LA DONACIÓN], por lo que LA PATROCINADORA abonará a esta, mediante liquidaciones [ELEGIR: mensuales / trimestrales / semestrales / anuales], el [PORCENTAJE] % de [IMPORTE DE LA CONTRAPRESTACIÓN]. El pago se efectuará entre los días [DÍA] y [DÍA] de cada mes en la cuenta corriente nº [IBAN] que [PERSONA FÍSICA O JURÍDICA O ENTIDAD QUE RECIBE LA DONACIÓN] tiene suscrita con la entidad [ENTIDAD BANCARIA] en su sucursal [SUCURSAL]. [Si se trata de una transferencia internacional será preciso conocer el código SWIFT o BIC.]

TERCERA.- Condiciones de la publicidad

Medios audiovisuales

La publicidad de los productos de LA PATROCINADORA deberá efectuarse en los siguientes medios, durante el tiempo que se especifica y con las siguientes frecuencias, franjas horarias y ubicación periódica:

— [EMISORAS DE RADIO, CON FRECUENCIA Y FRANJA HORARIA]

— [CANALES DE TELEVISIÓN, CON FRECUENCIA Y FRANJA HORARIA]

Además, EL PATROCINADO se obliga a mencionar en las entrevistas, ruedas de prensa y demás apariciones ante el público o los medios de comunicación el patrocinio del evento.

Medios escritos

La publicidad de los productos de LA PATROCINADORA deberá efectuarse en los siguientes medios, durante [CALENDARIO], en la sección [UBICACIÓN PERIÓDICA] y en módulos de tamaño [MÓDULO]:

— [MEDIO ESCRITO]

— [MEDIO ESCRITO]

A tal efecto, LA PATROCINADORA proporcionará a EL PATROCINADO, o a quien este indique, el material técnico necesario para la reproducción de sus marcas y anagramas.

Folletos y camisetas

LA PATROCINADORA se obliga a entregar a EL PATROCINADO los folletos y camisetas cuyos diseños y características se especifican en el Anexo I, el día [DÍA] de [MES] en [LUGAR].

CUARTA.- Duración del contrato

El presente contrato se concluye por un plazo de [NÚMERO] años, pudiendo prorrogarse, a voluntad de las partes y de común acuerdo, por períodos anuales.

Si, llegado el vencimiento del plazo inicial o de cualquiera de sus prórrogas, alguna de las partes decidiera dar por finalizado el presente contrato, deberá comunicar su intención a la otra parte con al menos dos meses de antelación a la fecha del vencimiento, a través de un medio que deje constancia de su recepción.

QUINTA.- Exclusividad

Exclusividad de EL PATROCINADO: durante tales actos, EL PATROCINADO no podrá hacer publicidad por sí mismo, ni autorizar a terceros, de productos que de cualquier forma entraran en competencia directa o indirecta con los productos de LA PATROCINADORA.

Exclusividad de LA PATROCINADORA: LA PATROCINADORA no podrá, por sí misma ni a través de terceros, patrocinar o financiar de cualquier forma actos o eventos que supusieran o pudieran suponer competencia directa o indirecta con los de EL PATROCINADO.

SEXTA.- Resolución del contrato

El contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las partes cuando medie incumplimiento grave de las obligaciones pactadas.

2. Por acuerdo de las partes por escrito.

3. La extinción de la personalidad jurídica de cualquiera de las partes o el embargo de bienes de alguna de ellas, a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la parte que pretenda resolver el presente contrato alegando incumplimiento de la contraparte deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [NÚMERO] días a la parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad de opción, sin necesidad de remitir previamente el antedicho requerimiento.

SÉPTIMA.- Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de [ELEGIR: LA PATROCINADORA / EL PATROCINADO / ambas partes por mitad].

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios de Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

OCTAVA.- Sumisión

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— Sumisión a tribunales, sin cláusula penal: Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los Tribunales de [SEDE], en [PROVINCIA], renunciando expresamente a su fuero propio si lo tuvieran. El presente contrato tiene exclusivamente carácter mercantil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

— Sumisión a tribunales, con cláusula penal: Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los Tribunales de [SEDE], en [PROVINCIA], renunciando expresamente a su fuero propio si lo tuvieran. En el caso de que la parte o partes que hubieran resultado condenadas en el fallo de la sentencia no cumplieran voluntariamente con el fallo en el plazo de [NÚMERO] días, deberán abonar a quien le hubiera vencido en el pleito la cantidad de [IMPORTE] euros ([IMPORTE] €), sin perjuicio de la indemnización por daños y perjuicios que pudiera corresponderles. El presente contrato tiene exclusivamente carácter mercantil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

— Sumisión a arbitraje, sin cláusula penal: Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD]. Según el artículo 34 de la Ley 60/2003, de 23 de diciembre, de Arbitraje, los árbitros solo decidirán en equidad si las partes les han autorizado expresamente para ello. El presente contrato tiene exclusivamente carácter mercantil, no existiendo vínculo laboral alguno entre EL PATROCINADO y el personal de LA PATROCINADORA, y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

— Sumisión a arbitraje, con cláusula penal: Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD]. Según el artículo 34 de la Ley 60/2003, de 23 de diciembre, de Arbitraje, los árbitros solo decidirán en equidad si las partes les han autorizado expresamente para ello. En el caso de que la parte o partes que hubieran resultado condenadas en el laudo no cumplieran voluntariamente con el fallo del mismo en el plazo de [NÚMERO] días, deberán abonar a quien le hubiera vencido en el procedimiento la cantidad de [IMPORTE] euros ([IMPORTE] €), sin perjuicio de la indemnización por daños y perjuicios que pudiera corresponderles. El presente contrato tiene exclusivamente carácter mercantil y se regirá por sus propias cláusulas y, en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

NOVENA.- Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada, en los respectivos domicilios indicados en el encabezamiento de este contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

DÉCIMA.- Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y solo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso, las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son solo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este contrato.

UNDÉCIMA.- Protección de datos

En el caso de que el cumplimiento de este contrato suponga la necesidad de acceder a datos de carácter personal, las partes, como encargadas del tratamiento, quedan obligadas al cumplimiento del Reglamento (UE) 2016/679 (RGPD), de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [NÚMERO] folios del presente CONTRATO DE PATROCINIO PUBLICITARIO, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. D./Dña. [NOMBRE Y APELLIDOS] (LA PATROCINADORA)

Fdo. D./Dña. [NOMBRE Y APELLIDOS] (EL PATROCINADO)

ANEXO I.- [PRESUPUESTO, DISEÑOS Y CARACTERÍSTICAS DE FOLLETOS Y CAMISETAS, SEGÚN PROCEDA]

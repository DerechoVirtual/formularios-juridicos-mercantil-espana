---
name: estatutos-union-temporal-empresas-ute-mer-0428
description: "Estatutos de una unión temporal de empresas (UTE). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Estatutos de una unión temporal de empresas (UTE)

> Formulario **MER-0428** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Estatutos de una unión temporal de empresas (UTE)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Estatutos de una unión temporal de empresas (UTE)” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:estatutos-union-temporal-empresas-ute-mer-0428`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (7 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ABREVIATURA DE LA DENOMINACIÓN
- [ ] DENOMINACIÓN SOCIAL
- [ ] ESTADO CIVIL
- [ ] FECHA
- [ ] NACIONALIDAD
- [ ] NIF
- [ ] NOMBRE DE LA PARTE
- [ ] NÚMERO
- [ ] OBJETO DEL CONTRATO

## Normas que cita el formulario

- art. 8 Ley 18/1982
- art. 8 d) Ley 18/1982

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

DENOMINACIÓN, OBJETO, DOMICILIO, COMIENZO Y DURACIÓN DE LA UTE
ÓRGANOS DE LA UTE
RESPONSABILIDAD DE LAS EMPRESAS MIEMBROS
RÉGIMEN ECONÓMICO FINANCIERO
INCUMPLIMIENTO, EXTINCIÓN Y LIQUIDACIÓN DE LA UTE
JURISDICCIÓN

Modelo de estatutos de una unión temporal de empresas en los que se concretan las bases de su organización y funcionamiento: duración, domicilio, objeto y capital social, competencias del gerente único y participación en la distribución de resultados, entre otras.

TÍTULO I.- DENOMINACIÓN, OBJETO, DOMICILIO, COMIENZO Y DURACIÓN DE LA UTE

Artículo 1.- Constitución y denominación

Se constituye una "Unión Temporal de Empresas" que figurará en el tráfico con la denominación [DENOMINACIÓN SOCIAL], UNION TEMPORAL DE EMPRESAS, Ley 18/1982, de 26 de mayo, abreviadamente [ABREVIATURA DE LA DENOMINACIÓN] UTE (que en lo sucesivo y a los solos efectos de los presentes Estatutos se denominará "la Unión" o la "UTE" indistintamente) y se regirá por lo estipulado en estos Estatutos y por las normas de la Ley 18/1982 de 26 de mayo, y las demás disposiciones aplicables.

Artículo 2.- Objeto

Constituye el objeto de esta UTE la ejecución de [OBJETO DEL CONTRATO].

[OPCIONAL — incluir si procede]

El citado objeto se desarrolla en la Memoria que se ha incorporado como anexo a la escritura de constitución de la UTE.

[OPCIONAL — incluir si procede]

Asimismo, se acompaña como anexo a estos Estatutos el Acuerdo de constitución de UTE firmado en fecha [FECHA] por:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

SL
SA
[NOMBRE DE LA PARTE]

Dicho Anexo se considera a todos los efectos como parte integrante de los presentes Estatutos.

Artículo 3.- Domicilio fiscal y legal

El domicilio fiscal y oficina principal de la UTE se establece en [DOMICILIO], [LOCALIDAD].

Todas las comunicaciones relativas al contrato objeto de la UTE, se efectuarán al domicilio arriba indicado o en su caso al que se designe expresamente para cada circunstancia.

Artículo 4.- Duración y vigencia

La UTE dará comienzo a sus operaciones en el momento del otorgamiento de su escritura de constitución, coincidente con la firma del presente documento.

La UTE se mantendrá vigente hasta la total prestación de los servicios que constituyen su objeto. En todo caso la duración de la UTE quedará sujeta a lo dispuesto en el apartado c) del artículo 8 de la Ley 18/1982 de 26 de Mayo.

TÍTULO II.- ÓRGANOS DE LA UTE

Artículo 5.- Órganos de gobierno de la UTE

La UTE tendrá los siguientes órganos de gestión y representación:

a) Un Consejo de la Unión, que será el órgano supremo de dirección de la UTE.
b) Un Gerente Único.

Artículo 6.- Competencias del Consejo de la Unión

La UTE será gobernada por un Consejo de la Unión que tendrá encomendada la alta dirección, gestión y gobierno de la ejecución del Contrato que constituye su objeto. El Consejo de la Unión tendrá todas las facultades necesarias para el cumplimiento del objeto de la UTE, enumerándose seguidamente sin carácter limitativo las siguientes:

1. Elaborar las directrices generales de la actuación de las Empresas Miembros y sus cometidos en todo lo que concierne a la ejecución del Contrato. Nombrar y revocar, en su caso, al Gerente Único. Asimismo, inspeccionar, controlar y establecer las directrices de la actuación del Gerente Único. Igualmente, el Consejo tendrá la facultad de decidir sobre todos los actos que los miembros de la UTE consideren conveniente llevar a cabo en forma solidaria y conjunta.
2. Establecer y dirigir las relaciones con los posibles proveedores, organismos, sociedades o personas, en el caso de que existan relaciones con estos terceros llevadas a cabo directamente por la UTE, y no por las Empresas Miembros que la forman.
3. Aprobar el presupuesto, balance y cuentas de la UTE, lo que deberá hacer con la periodicidad que el propio Consejo establezca, que en ningún caso será posterior a una anualidad, debiendo producirse la aprobación en los tres meses siguientes al cierre del ejercicio. Los mencionados documentos deberán ser firmados por todos los miembros del Consejo de la Unión y por el Gerente Único.
4. Establecer el importe de las aportaciones que, en su caso, hayan de efectuar las Empresas Miembros para sufragar los gastos generales de la Unión, y la forma y tiempo de efectuarlas. Aprobar el reembolso de los gastos realizados por cualquiera de las Empresas Miembros, así como los anticipos que, en su caso, soliciten éstas a cuenta de las facturaciones pendientes y su distribución.
5. Establecer la forma, tiempo y condiciones en las que las Empresas Miembros podrán facturar a la Unión el precio de las prestaciones realizadas y la forma y tiempo de su percepción. Aprobar todas las subcontrataciones que deberá realizar la Unión.
6. En general, controlar la marcha y ejecución del Contrato, en todos los aspectos técnicos y financieros relevantes, resolviendo sobre las distintas incidencias que pudieran surgir.
7. En particular, deliberar y resolver sobre los siguientes asuntos:
7.1. Decidir sobre aquellas cuestiones del Contrato, que no se encuentren suficientemente desarrolladas.
7.2. Decidir sobre soluciones técnicas diferentes a las previstas en el Contrato, así como sobre cualesquiera ampliaciones o modificaciones del mismo que sean necesarias.
7.3. Aprobar las repercusiones económicas sobre las Empresas Miembros de las variaciones técnicas, ampliaciones o modificaciones, adoptadas en el desarrollo de la ejecución del Contrato, entendiendo como cuestiones técnicas las referidas tanto a los recursos materiales como los recursos humanos.
8. Establecer la estrategia de la UTE frente al Cliente y frente a terceros en la ejecución del Contrato y su seguimiento.
9. Aclarar las dudas de interpretación de cualquier disposición de estos Estatutos o del Contrato objeto de la UTE.

Las facultades anteriormente señaladas, se entienden referidas exclusivamente para aquellos actos que competen conjunta y solidariamente a las Empresas Miembros, entendiéndose excluidos de dichas facultades aquellos actos que corresponde ejecutar exclusivamente a cada una de las Empresas Miembros.

Artículo 7.- Composición y funcionamiento del Consejo de la Unión

El Consejo de la Unión estará constituido por [Nº] vocales, correspondiendo a cada Empresa Miembro la designación de [Nº] vocales.

Los componentes designados por las partes inicialmente son:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Por [ELEGIR: SL / SA]:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] (NIF. [NIF])

Los miembros del Consejo de la Unión y el Gerente Único no tendrán asignada retribución alguna de la UTE, por percibir sus sueldos de las empresas respectivas.

Los nombramientos se efectuarán por tiempo indefinido, sin perjuicio de la facultad de las Empresas Miembros de la UTE de sustituir en cualquier momento, durante la vigencia de la UTE, a las personas por ellas designadas y mediante la comunicación fehaciente a la otra Empresa Miembro y al Gerente Único de la UTE con una antelación mínima de [Nº] días naturales.

El Consejo de la Unión designará de entre sus miembros un Presidente que dirigirá las reuniones e impulsará de modo general la actuación de este órgano. También designará de entre sus miembros un Secretario que levantará las actas de las sesiones que se celebren, y que certificará con el Vº Bº del Presidente.

El Consejo de la Unión se reunirá en la forma periódica que por el mismo se acuerde, y como mínimo, una vez cada [Nº] meses, y en las ocasiones extraordinarias que se consideren necesarias a convocatoria de su Presidente, a iniciativa propia o previa petición justificada formulada por escrito por cualquiera de las Empresas Miembros o por el Gerente Único.

La notificación de la convocatoria deberá realizarse con una antelación mínima de [Nº] días a la fecha prevista para la reunión, haciendo constar el lugar, día y hora de la sesión, así como el Orden del Día de la misma. La notificación deberá ser por escrito, siendo válidos el telefax, el fax u otro medio electrónico del que quede constancia escrita.

De cada reunión se levantará Acta en la que se reflejarán sucintamente los acuerdos adoptados y que será sometida a la aprobación de todos los miembros del Consejo dentro del mes siguiente a la reunión y, en todo caso, antes de la convocatoria de la reunión siguiente al mismo, mediante el envío de un borrador para su conformidad o reparos. El Acta deberá ser firmada por todos los asistentes. El Gerente de la UTE asistirá a las reuniones del Consejo de la Unión, con voz pero sin voto. En casos especiales los miembros del Consejo podrán asistir a las reuniones acompañados de algún asesor, el cual podrá emitir su opinión en la materia de su especialidad.

El Consejo de la Unión quedará válidamente constituido cuando asistan al mismo, presentes o representados, al menos uno de los representantes designados por cada Empresa Miembro. Cada vocal podrá hacerse representar por otro mediante simple delegación escrita.

El Consejo quedará también válidamente constituido, sin necesidad de convocatoria previa cuando estén presentes la totalidad de sus miembros y acepten por unanimidad la convocatoria de la sesión.

Los acuerdos se adoptarán por unanimidad de las Empresas Miembros. El sentido del voto de cada Empresa Miembro será el que manifieste la mayoría de sus representantes presentes o representados en la reunión.

[OPCIONAL — incluir si procede]

Los acuerdos del Consejo de la Unión podrán también adoptarse por escrito y sin sesión, siempre que el Acta correspondiente sea suscrita por todos los miembros que lo integran.

Artículo 8.- Gerencia. Designación y facultades

A los efectos de lo dispuesto en el artículo 8º d) apartado 6 de la Ley 18/1982 de 26 de Mayo, se nombra Gerente Único de la UTE a D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], de nacionalidad [NACIONALIDAD] y D.N.I. nº [NÚMERO] y con domicilio a estos efectos en [DOMICILIO],

El Gerente Único será responsable de la UTE ante el Consejo de la Unión y tendrá, a los efectos de lo dispuesto en el artículo 8 d) de la Ley 18/1982 de 26 de Mayo, todos los poderes suficientes para representar a la UTE ante la Administración española y ante terceros, y para ejercitar los derechos y asumir las obligaciones necesarias para la consecución de los fines que constituyen el objeto de la UTE, haciendo constar que actúa en nombre de ella en los actos y contratos que suscriba en representación de la misma, que ha de suscribirse al ámbito de su objeto exclusivo.

El Gerente Único tendrá una relación laboral o estatutaria con una de las dos empresas participantes en la UTE.

En consecuencia de lo anterior, el Gerente Único tendrá las siguientes facultades:

1. Firmar en nombre de la UTE el Contrato cuya ejecución es objeto de la misma, así como cuantas ampliaciones o modificaciones sean acordadas.
2. Ejercitar todos los derechos y contraer todas las obligaciones que correspondan a la Unión, haciendo constar que actúa en nombre de ella en todos los actos y contratos que suscriba en representación de la misma.
3. Representar a la UTE ante el órgano de contratación y ante cualesquiera órganos o entes de las Administraciones Públicas, personas físicas, jurídicas, privadas nacionales o extranjeras.
4. Ostentar igualmente la representación en juicio de la UTE, pudiendo comparecer ante Tribunales de cualquier orden o grado, absolver posiciones, ejercitar acciones y desistir de ellas, allanarse y transigir. A los efectos de la representación judicial podrá otorgar poderes a favor de Letrados y Procuradores de su elección.
5. Coordinar y controlar la ejecución individual por cada una de las Empresas Miembros de las prestaciones atribuidas a cada una de ellas, así como dirigir y administrar las actividades de la UTE, dando cuenta al Consejo de la Unión del uso que haga de estas facultades.
6. Llevar la contabilidad y formular, para su posterior aprobación por el Consejo de la Unión, el presupuesto, balance y cuenta de gastos e ingresos de la UTE.
7. Realizar cuantos actos y negocios jurídicos se precisen para las actividades de la Unión, firmando contratos y otorgando documentos públicos o privados.
8. Efectuar cobros, solicitar, consignar y retirar fianzas y depósitos, protestar letras de cambio, percibir o cobrar fondos y bienes de la Unión y reclamarlos tanto de particulares, como de Oficinas Públicas.
9. Abrir, disponer, seguir y cancelar cuentas corrientes de créditos y de ahorro en cualquier Entidad Bancaria o Crediticia, realizando todo cuanto permite la normativa y prácticas bancarias.
10. Efectuar pagos, librar, aceptar, pagar y negociar letras de cambio, disponer de los fondos y bienes de la Unión, constituir depósitos donde a los intereses de la UTE convenga, y cualquier otro acto de disposición.

Por lo que respecta a los aspectos internos de la UTE, el Gerente Único actuará como ejecutor de las resoluciones y directrices del Consejo de la Unión y responderá por las obligaciones y compromisos que contraiga, directamente él mismo ante las Empresas Miembros que forman la presente UTE.

TÍTULO III.- RESPONSABILIDAD DE LAS EMPRESAS MIEMBROS

Artículo 9.- Cuotas de participación y aportaciones

La participación de cada una de las Empresas Miembros en todos los derechos y obligaciones, así como los resultados o ingresos o gastos de la UTE se fijan en proporción a sus respectivas cuotas, sin perjuicio de lo dispuesto en el artículo siguiente.

La participación o cuota de cada una de las Empresas Miembros de la UTE se fija, salvo acuerdo posterior entre las Empresas Miembros, en los siguientes porcentajes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

SL
SA
 %

Las citadas Empresas Miembros constituirán un fondo operativo por un monto de.- euros ( €) para atender a los gastos iniciales comunes, que será aportado por cada una de ellas en proporción a sus respectivas cuotas de participación.

Las nuevas aportaciones para los gastos comunes que requiera la Unión serán las que específicamente sean aprobadas por el Consejo de la Unión.

Artículo 10.- Responsabilidad

Las Empresas Miembros de la UTE responderán solidaria e ilimitadamente frente a terceros por los actos y operaciones en beneficio común, sin perjuicio del derecho de repetición inherente a cada una de ellas y de los pactos que libremente se establezcan en los presentes Estatutos, en orden a una depurada responsabilidad y garantía entre las partes para con terceros.

En consideración a lo anterior, y sin perjuicio de la responsabilidad solidaria de los miembros de la UTE frente a la Administración contratante, las partes desean establecer el principio de responsabilidad mancomunada en las relaciones internas de la UTE. Consiguientemente, cada Empresa Miembro de la UTE será exclusivamente responsable respecto de las penalizaciones e indemnizaciones de cualquier tipo que se impongan a la UTE como consecuencia de los retrasos, daños o ejecuciones defectuosas que le sean imputables, y mantendrá indemne a la otra parte, compensándolas por los daños y perjuicios que por tal causa puedan derivarse para la otra parte.

En el caso de responsabilidad conjunta o concurrencia de causas en la generación de la responsabilidad de la UTE por parte de sus Empresas Miembros, se procurará guardar la debida proporcionalidad en la atribución de responsabilidades.

[OPCIONAL — incluir si procede]

Las posibles reclamaciones internas entre los miembros no incluirán, en ningún caso, la recuperación de daños y perjuicios indirectos.

TÍTULO IV.- RÉGIMEN ECONÓMICO FINANCIERO

Artículo 11.- Régimen contable

Se designa una dirección administrativa de la Unión que corresponderá a [ELEGIR: SL / SA]., por lo que ésta asumirá la llevanza de la contabilidad y gestión administrativa de la UTE, siendo competencia del Consejo de la Unión la determinación de los cargos que, en su caso, por tal concepto se facturarán a la UTE.

La Unión queda sometida al Régimen Especial de Agrupaciones de interés económico, españolas y europeas, y de Uniones Temporales de Empresas regulado en el Capítulo I del Título III del Real Decreto 634/2015, de 10 de julio, por el que se aprueba el Reglamento del Impuesto sobre Sociedades

El ejercicio económico será anual y coincidirá con el año natural, a excepción del primero, que comenzará el día de constitución de la UTE y terminará el día 31 de diciembre.

La contabilidad de la Unión será independiente de la que llevan las Empresas Miembros, a fin de permitir conocer en todo momento la situación económico-financiera de la misma.

Las Empresas Miembros llevarán en su contabilidad cuentas perfectamente diferenciadas, que reflejen sus relaciones con la Unión.

Los asientos contables y los pagos, no podrán hacerse más que sobre la base de documentos justificativos, que deberán ser revisados y firmados por el Gerente Único.

Cada una de las Empresas Miembros podrá examinar por sí misma a través de las personas naturales o físicas que designe, la contabilidad y documentación de la Unión.

Artículo 12.- Movimiento de fondos

Los pagos, transferencias e ingresos de la Unión se efectuarán a nombre de la misma en la cuenta corriente abierta en bancos escogidos de común acuerdo. Los fondos podrán ser retirados de dichas cuentas por cheques, órdenes o transferencias en base a un documento justificativo que ha de ser revisado por el Gerente Único, en su caso.

Las peticiones de fondos a ingresar en la cuenta corriente de la Unión serán hechas por ésta a las Empresas Miembros con un preaviso mínimo de [Nº] días, para permitirle las operaciones bancarias necesarias que serán de cuenta y riesgo de cada una de ellas. Salvo acuerdo en contrario entre las partes, los ingresos de fondos, así como los reembolsos obtenidos, se harán siempre simultáneamente a las partes en la proporción fijada en el art. 9 de estos Estatutos.

En las peticiones de fondos indicadas en el párrafo anterior, deberán incluirse el importe de las cantidades a que sean acreedoras las respectivas Empresas, por suplidos pendientes previamente autorizados por el Consejo de la Unión, quienes en tales supuestos podrán a su vez, descontar de las cantidades a ingresar los expresados importes a su favor, extinguiéndose dichas deudas por compensación de crédito.

En general, se procurará que las obras se financien con el fondo operativo y el cobro de certificaciones, no recurriendo a solicitar aportaciones de fondos complementarias de las Empresas Miembros más que en caso de que no se puedan cubrir las necesidades de tesorería con los medios anteriores.

Artículo 13.- Determinación e imputación de resultados

Los beneficios o pérdidas, así como los ingresos y gastos que obtenga o en que incurra la UTE, serán imputados a las Empresas Miembros en proporción a su respectiva cuota de participación,

imputándose las bases imponibles a las Empresas Miembros en el ejercicio en que se hayan devengado.

Los beneficios serán determinados provisionalmente en el momento en que el Consejo apruebe las Cuentas, y sólo serán definitivos cuando se haya procedido a la ejecución total de los trabajos objeto de la UTE y la liquidación total del Contrato, así como las obligaciones derivadas del mismo, tanto frente al Cliente como ante terceros. Hasta entonces, toda cantidad que hubiese sido distribuida por tal concepto será considerada anticipo o entrega a cuenta, quedando la Empresa Miembro respectiva obligada a las devoluciones a que hubiese lugar.

TÍTULO V.- INCUMPLIMIENTO, EXTINCIÓN Y LIQUIDACIÓN DE LA UTE

Artículo 14.- Incumplimiento

En caso de declaración de concurso, liquidación judicial o amistosa de cualquiera de las Empresas Miembros, así como en al caso de que cualquiera de las Empresas deje de cumplir de forma grave las obligaciones asumidas en los presentes Estatutos o en las actividades subcontratadas por la Unión y no remedie tal incumplimiento dentro de los [Nº] días naturales siguientes a aquél en que la otra Empresa Miembro le requiera a ello por escrito, la Empresa Miembro cumplidora tendrá derecho a excluir de la UTE a aquélla, y proseguir la ejecución del Contrato bien a solas o mediante subcontratación, sin tener posibilidad de obtener retribución alguna la Empresa Miembro apartada desde el momento de tales circunstancias.

La Empresa Miembro excluida en virtud del párrafo anterior estará obligada a indemnizar a la otra Empresa por los daños y perjuicios que ocasione su exclusión.

Queda entendido que el hecho de la exclusión no exime a la Empresa Miembro excluida de la responsabilidad solidaria e ilimitada frente al Cliente y terceros, hasta la total liquidación y pago de las obligaciones contraídas con motivo de la UTE.

No obstante lo anterior, en el supuesto de que el Cliente rescindiera el Contrato en caso de declaración de concurso, liquidación judicial o extrajudicial de cualquiera de las Empresas Miembros, así como en el caso de que cualquiera de las Empresas deje de cumplir de forma grave las obligaciones asumidas en los presentes Estatutos o en las actividades subcontratadas por la Unión, la Empresa que hubiera provocado la resolución y consecuente extinción de la UTE quedará automáticamente excluida del Consejo de la Unión, sin tener derecho a percibir cantidad alguna a cuenta de los resultados que pudieran producirse, hasta la completa liquidación de la UTE; ello sin perjuicio de continuar subsistente su responsabilidad frente a la Empresa cumplidora por la parte proporcional de las pérdidas que pudieran resultar de la misma.

Lo anterior se entenderá sin perjuicio de la responsabilidad conjunta, solidaria e ilimitada de las Empresas Miembros en sus relaciones con el Cliente y terceros y hasta la total liquidación y pago de las obligaciones contraídas con motivo de la UTE.

Artículo 15.- Causas de extinción

La UTE se extinguirá por la imposibilidad física o jurídica de realizar el Contrato para el cual fue constituida, o por haber finalizado en su totalidad los trabajos objeto del citado Contrato, siempre y cuando se hubieren liquidado definitivamente y sin reserva alguna, todas las cuestiones, diferencias o litigios entre las Empresas Miembros y las obligaciones con el Cliente o con terceros. La extinción de la UTE no afectará por tanto a la responsabilidad solidaria de los miembros de la misma hasta la total liquidación de los derechos y obligaciones con terceros, incluyendo, en su caso, los servicios que corresponda prestar durante el período de garantía del Contrato.

Artículo 16.- Liquidación

La liquidación se llevará a efecto por el Consejo de la Unión, y si la UTE se hubiese disuelto por culpa o incumplimiento de una de las Empresas Miembros, la Empresa que hubiese permanecido en la ejecución del Contrato realizará las funciones de liquidación, dando en su momento el debido conocimiento a la otra parte, para la efectividad de la liquidación.

Corresponden al Consejo de la Unión durante el período de liquidación, las siguientes funciones:

1. Llevar y custodiar los libros correspondientes en la UTE y velar por la integridad de su patrimonio.
2. Realizar las operaciones comerciales pendientes y las nuevas que sean necesarias para la liquidación de la UTE.
3. Percibir los créditos y demás derechos pendientes al tiempo de iniciarse la liquidación.
4. Enajenar los bienes de la UTE, de acuerdo con el procedimiento que se establezca por el propio Consejo de la Unión.
5. Pagar a las Empresas Miembros de la UTE su cuota de participación en el patrimonio líquido.
6. Ostentar la representación de la UTE para el cumplimiento de las funciones precedentes.

El Consejo de la Unión quedará automáticamente disuelto una vez realizada la liquidación de la UTE.

Artículo 17.- Beneficios fiscales

La UTE se acoge al régimen tributario establecido en la Ley 18/1982 de 26 de Mayo, la Ley 12/1991 de 29 de abril y la Ley 27/2014, de 27 de diciembre, por el tiempo que dure la ejecución de los trabajos que constituyen su objeto, procediendo a tal efecto a su inscripción en el Registro Especial de Uniones Temporales de Empresas del Ministerio de Hacienda.

TÍTULO VI.- JURISDICCIÓN

Artículo 18.- Jurisdicción

Las Empresas Miembros acuerdan que todo litigio, discrepancia, cuestión o reclamación que se suscite entre las mismas en relación con el Contrato objeto de la UTE o con los presentes Estatutos, o relacionados directa o indirectamente con los mismos, se someterá a los Tribunales de [LOCALIDAD], con renuncia expresa a cualquier fuero que pudiera corresponderles.

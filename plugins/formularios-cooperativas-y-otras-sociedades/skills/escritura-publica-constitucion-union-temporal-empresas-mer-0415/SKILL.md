---
name: escritura-publica-constitucion-union-temporal-empresas-mer-0415
description: "Escritura pública de constitución de una unión temporal de empresas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de constitución de una unión temporal de empresas

> Formulario **MER-0415** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública de constitución de una unión temporal de empresas entre Sociedades [TIPO DE SOCIEDADES], en la que se establecen y concretan, entre otras cosas, las pautas y condiciones necesarias para su funcionamiento, denominación, duración, domicilio, objeto y capital social. UNIÓN TEMPORAL DE EMPRESAS: ESCRITURA DE CONSTITUCION

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de constitución de una unión temporal de empresas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de constitución de una unión temporal de empresas” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:escritura-publica-constitucion-union-temporal-empresas-mer-0415`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (3 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (3 veces)
- [ ] Nº (3 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] AÑO
- [ ] COLEGIO
- [ ] DENOMINACIÓN DE LA UTE
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] NÚMERO
- [ ] OBJETO DEL CONTRATO
- [ ] PARTICIPACIONES DE LAS EMPRESAS MIEMBROS
- [ ] TIPO DE INTERÉS
- [ ] ÓRGANO ARBITRAL

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

Modelo de escritura pública de constitución de una unión temporal de empresas entre Sociedades [TIPO DE SOCIEDADES], en la que se establecen y concretan, entre otras cosas, las pautas y condiciones necesarias para su funcionamiento, denominación, duración, domicilio, objeto y capital social.

UNIÓN TEMPORAL DE EMPRESAS: ESCRITURA DE CONSTITUCION


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

NÚMERO DE PROTOCOLO:

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS] Notario del Ilustre Colegio de [COLEGIO]

COMPARECEN

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número

INTERVIENEN

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente escritura de constitución de UNIÓN TEMPORAL DE EMPRESAS, a cuyo fin

EXPONEN

I.- Que la mercantil [DENOMINACIÓN SOCIAL] se dedica a [ACTIVIDAD]; y que la mercantil [DENOMINACIÓN SOCIAL], a [ACTIVIDAD]

II.- Que es voluntad de los mismos constituir una Unión Temporal de sus Empresas.

III.- Que a tales efectos proceden al otorgamiento de la presente escritura de constitución de ", U.T.E.", y

OTORGAMIENTO

Constitución y denominación

Los otorgantes proceden a constituir una Unión Temporal de Empresas sin personalidad jurídica, que se regirá por el presente contrato y por la Ley 18/1982, de 26 de Mayo, así como por cuantas disposiciones legales y reglamentarias resulten de aplicación.

La Unión se denomina [DENOMINACIÓN DE LA UTE], UNIÓN TEMPORAL DE EMPRESAS.

Duración y comienzo de las operaciones

La Unión Temporal tendrá duración por todo el tiempo que transcurra desde el inicio de sus actividades hasta que, por haber quedado total y definitivamente ejecutados los trabajos necesarios para la conclusión de la obra contratada, y su plazo de garantía, se liquiden definitivamente y sin reserva alguna todas las cuestiones, diferencias y litigios entre la Administración contratante y la Unión Temporal, ante otros terceros y entre las Empresas Unidas.

Sus operaciones comenzarán el día [FECHA]

Objeto

Constituye el objeto de esta Unión Temporal la ejecución de los trabajos comprendidos en el contrato "" que debe realizarse para [OBJETO DEL CONTRATO], así como todos los trabajos complementarios o accesorios a dicho contrato de

En la Memoria adjunta se expresa con más detalle el indicado objeto, con determinación de las actividades y medios que habrán de utilizarse para su realización.

Domicilio fiscal

[ELEGIR UNA OPCIÓN: Sin agencias delegaciones o sucursales / Con agencias delegaciones o sucursales]

Fondo operativo

Las actividades comunes se financiarán con cargo al fondo operativo común, constituido por las empresas miembros con las siguientes participaciones: [PARTICIPACIONES DE LAS EMPRESAS MIEMBROS].

Participación en la distribución de resultados

Las empresas miembros participarán en la distribución de resultados y en los ingresos o gastos de la Unión de acuerdo a la siguiente proporción:

Responsabilidad

Todas las empresas miembros de la Unión responderán solidaria e ilimitadamente, frente a terceros, por los actos y operaciones realizados por la Unión en beneficio común.

Cesión de participaciones

Ningún miembro de la Unión puede transmitir su participación en la misma a terceros o a otro miembro si no es con el consentimiento unánime de todos los demás.

Movimiento de fondos

Los pagos, transferencias e ingresos de la Unión Temporal se efectuarán a nombre de la misma a la orden conjunta de las Empresas Agrupadas, en las cuentas corrientes abiertas en Bancos escogidos de común acuerdo. Los fondos podrán ser retirados de dichas cuentas por cheques, órdenes o transferencias mediante las firmas conjuntas de, al menos, dos personas autorizadas pertenecientes a distintas Empresas.

Las remesas de fondos las deben efectuar las Empresas Agrupadas de forma que lleguen a su debido tiempo y por las cantidades demandadas por la Unión, en cuyo caso dichas remesas no devengarán interés alguno. Si alguna de las empresas no efectuase la aportación a que viniere obligada, incurrirá en morosidad, y deberá abonar a la Unión un interés del [TIPO DE INTERÉS] %, o el interés preferencial que esté vigente en los principales Bancos, incrementado en [Nº] puntos, eligiéndose de entre las dos fórmulas la que resulte la cantidad mayor. Cuando una de las Empresas no morosas consintiera voluntariamente en cubrir algún déficit por demora en el ingreso que le correspondiera, la morosa abonará, directamente a la Empresa que hubiera cubierto dicho déficit, o a través de la propia Unión, los intereses devengados por las diferencias cubiertas, de acuerdo con los tipos que se han indicado en este mismo párrafo.

Las peticiones de fondos a ingresar en la cuenta corriente de la Unión serán hechas por ésta a las Empresas con un preaviso mínimo de quince días para permitirles las operaciones bancarias necesarias, que serán de cuenta y riesgo de cada una de ellas. Salvo acuerdo en contrario entre las partes, los ingresos de fondos, así como los reembolsos de éstos, o de eventuales anticipos sobre los beneficios obtenidos, se harán siempre simultáneamente a las partes en la proporción fijada en el artículo 5 de estos Estatutos.

En las peticiones de fondos indicadas en el párrafo anterior, deberán incluirse los importes de las cantidades a que sean acreedoras por suplidos pendientes, las respectivas Empresas, quienes, en tal supuesto podrán, a su vez, descontar de las cantidades a ingresar los expresados importes a su favor, extinguiendo por compensación su crédito.

Se considera que en todo momento cada una de las Empresas es propietaria de la parte correspondiente de estos fondos circulantes, según la proporción en que la ha aportado y que se especifica en el artículo 5, si bien se usufructúan en común por la Unión Temporal.

Maquinaria y equipos

En principio, y salvo acuerdo en contrario de las Empresas Agrupadas, no se prevé que sea necesaria la adquisición, por parte de la Unión Temporal de maquinaria o equipos de ninguna clase, usándose los medios propios de cada una de las Empresas, recurriéndose, en todo caso al alquiler de los que se consideraran necesarios.

Para el primer supuesto (aportación de maquinaria propia de las empresas unidas), el Comité de Gerencia establecerá la compensación que ha de recibir la Empresa propietaria, fijándose un alquiler mensual para la misma según baremos que a tal efecto establezcan. Dicho alquiler se facturará, salvo acuerdo en contrario, mensualmente, pudiendo compensarse su importe con otras deudas que tuviere la Empresa propietaria con la U.T.E. en cada momento. Por su parte, la Unión deberá inventariar la maquinaria aportada, contabilizándola a su precio real, indicando la sociedad propietaria de la misma. Asimismo, se compromete a conservarla en buen estado durante el tiempo en que se halle a su disposición.

Órganos de la Unión Temporal

[ELEGIR UNA OPCIÓN: Gerente Único sin Comité de Gerencia / Gerente Único con Comité de Gerencia]

Obligaciones financieras

Las empresas atenderán, de acuerdo con los porcentajes que se establecen en el artículo 5 de estos Estatutos, todas las obligaciones financieras estrictamente relacionadas con la ejecución del contrato, compartiendo los riesgos de cualquier clase derivados del mismo, incluidos los de terceros que garanticen mediante fianza prestada la ejecución del contrato objeto de la Unión.

La Unión soportará los gastos y cargas de toda naturaleza ocasionados por los trabajos, con la sola excepción de los impuestos que graven directa o individualmente a las Entidades que la componen.

Los gastos originados en la elaboración de la oferta serán de cuenta de cada una de las Empresas que los hubiera realizado, salvo aquellos para los que previamente se hubiera acordado lo contrario.

Determinación de beneficios

Los beneficios serán determinados provisionalmente en el momento en que las partes, por unanimidad, convengan, pero sólo serán definitivos cuando se haya procedido a la liquidación total del contrato y de las obligaciones derivadas del mismo. Hasta ese momento, toda cantidad que se hubiera distribuido por tal concepto se entenderá realizada a título provisional, en calidad de anticipo, quedando las empresas que los hubieren recibido obligadas a las devoluciones o compensaciones a que hubiere lugar.

Obligaciones contables

La Unión establecerá un sistema contable totalmente independiente del que llevan las Empresas Unidas, de modo que pueda ser conocida en todo momento la situación económico-financiera de la misma.

El plan contable tendrá las necesarias cuentas representativas, las cuales comprenderán las contribuciones que hicieren las Empresas agrupadas, dinerarias o en bienes o servicios (suplidos), al fondo de operaciones para hacer frente a los gastos correspondientes.

Las empresas llevarán en sus contabilidades las cuentas perfectamente diferenciadas, que reflejen sus relaciones con la Unión y los gastos y resultados que se deriven de la operación que constituye el fin de la misma. Cada una de las Empresas podrá examinar, por sí misma o por las personas físicas o jurídicas que designen, la Contabilidad y todos los documentos de la Unión.

Los asientos contables y los pagos no podrán hacerse más que sobre la base de documentos justificativos. Estos últimos, al igual que todos los demás libros y documentos contables de la Unión, radicarán en el domicilio de la U.T.E., o, en su caso, donde se acordare por el Comité de Gerencia, siendo visados por el Jefe Administrativo, si lo hubiere, y en cualquier caso por el Gerente.

Se formulará un balance trimestral, con los detalles informativos que estime necesarios el Comité de Gerencia, y del que se remitirá inmediatamente copia a los miembros del mismo, así como a las personas que éstos designen.

Extinción de la Unión Temporal

La Unión Temporal se extinguirá por las siguientes causas:

a) Por la terminación del suministro, en todos sus aspectos, para el que fue constituida la Unión Temporal.
b) Por la resolución del Contrato objeto de la Unión Temporal.
c) Por imposibilidad, física o jurídica, de realizar el objeto de la misma.
d) Por el concurso y liquidación judicial o amistosa de una de las Empresas miembros de la Unión.
e) Por incumplimiento, por cualquiera de las empresas unidas, de las normas previstas en estos Estatutos y, particularmente, la falta de aportación de dinero, equipos u otros bienes a que estuvieran obligadas las Empresas, cuando, siendo requeridas para ello, dejaran de hacerlo.

En cualquiera de los dos últimos casos, las Empresas no afectadas por las mencionadas situaciones podrán optar por continuar la Unión Temporal, excluyendo de ellas a las que hubieren incumplido y subrogándose en las obligaciones de las mismas.

Efectos de la extinción

Cuando la Unión se extinga por las causas indicadas en los apartados d) y e) del artículo anterior, la parte excluida responderá de la parte proporcional de pérdida que se produjera en la Unión, tanto de la originada hasta el momento en que se produjo el hecho de la expulsión, como hasta la total extinción de la Unión.

En estos mismos casos, concluido o resuelto el contrato, y comenzado el período de liquidación, la Empresa o Empresas que hubieran asumido los derechos y obligaciones de la Unión hasta el momento de dicha extinción deberán realizar todos los cobros que correspondan a la Unión y abonar a la empresa excluida una cantidad igual a la aportación hecha por ésta, deducida la parte proporcional de pérdida que le corresponda, conforme a lo expuesto más arriba.

Si dicha pérdida fuera superior a lo aportado, la Empresa excluida deberá abonar la diferencia, en un plazo de [Nº] días, a las que hubieran continuado en la ejecución del contrato. Sólo estas tendrán derecho a los beneficios, si los hubiere, desde el momento en que quedó excluida la Empresa incumplidora.

La extinción de la Unión Temporal no afectará a la responsabilidad solidaria de sus miembros hasta la total liquidación de los derechos y obligaciones frente a terceros.

Liquidación de la Unión Temporal

La liquidación se llevará a efecto por el Comité de Gerencia y si la UTE se hubiese disuelto por culpa o incumplimiento de una de las empresas miembro, la empresa que hubiese permanecido en la ejecución de las obras realizará las funciones de liquidación, dando en su momento el debido conocimiento a la otra parte.

Corresponde al Comité de Gerencia, durante el período de liquidación, las siguientes funciones:

1) Llevar la administración y velar por el patrimonio, asignando en su caso, a cada empresa miembro, las gestiones que sean necesarias.
2) Realizar las actividades necesarias para la liquidación de la UTE.
3) Efectuar los cobros, sin limitación alguna.
4) Enajenar los bienes de la Unión Temporal de Empresas
5) Liquidar a los miembros su cuota de participación.
6) Ostentar ante toda clase de Autoridades, Tribunales, Organismos, Entidades, Sociedades o Personas físicas, la representación de la UTE para el cumplimiento de las funciones necesarias para la liquidación.

Liquidación de activos

Si la U.T.E. hubiera adquirido cualesquiera bienes (maquinaria, mobiliario, etc.), una vez finalizado su empleo en las obras, se procederá a su reparto entre los miembros de la Unión, o a su venta a terceros, según las siguientes reglas:

1º) La jefatura de Obra o la Administrativa pondrán en conocimiento del Comité de Gerencia, semestralmente, la relación de aquellos bienes, que, según razonables previsiones, no serán necesarios para los fines de la Unión, en la cual figurará el valor residual por el que figuren en el Balance de la misma, y su historial de empleo en obra.
2º) Los miembros del Comité trasladarán a sus respectivas Empresas tal relación, a fin de que, previas las comprobaciones que las mismas estimen oportunas, puedan ofertar por la adquisición de las mismas. A tal efecto, se fijará una reunión específica, en el que las Empresas Unidas formularán, en sobre cerrado, su puja por cada elemento, pudiendo hacerlo por uno, varios, todos o ninguno.
3º) Abiertos y leídos los sobres por el Secretario del Comité, se obrará de la siguiente forma:
a) Si hay un solo socio interesado en un bien, se le adjudicará por el valor que haya ofertado.
b) Si hay más de una oferta por un bien en concreto, se adjudicará al socio que ofrezca mayor importe.
c) Si no hubiere ningún socio interesado, se ofrecerá a la venta a terceros, con el valor residual como precio mínimo.
4º) En el plazo de tres meses, una vez terminadas las obras objeto del contrato, y efectuada su recepción, y si aun quedaran bienes pendientes de adjudicar por el anterior sistema, la Gerencia, auxiliada por los Jefes de Obra y Administración, formará con ellos lotes de valores residuales semejantes, que se adjudicarán a los socios mediante sorteo, compensándose las pequeñas diferencias que pudiera haber con los saldos de su participación en los resultados de la U.T.E.
5º) Tanto en un supuesto como en otro, el socio adjudicatario deberá retirar a su costa el bien que le haya correspondido del lugar donde se hallare, siendo de su cargo todos los gastos que con tal motivo se originen.
6º) En cualquier caso, y para los supuestos en los que, por la naturaleza o el valor

residual de los bienes no pudieran ser aplicadas las anteriores reglas, se estará a lo que acuerde, por unanimidad, el Comité de Gerencia.

Archivo de la documentación

Serán de cargo de la Unión, y su importe deberá ser aprobado por el Comité de Gerencia, los gastos que se originen con motivo de la ubicación y atención del archivo de la documentación de la misma, una vez disuelta, hasta que, de acuerdo con la normativa legal aplicable, sea posible su destrucción, e incluso antes de la citada disolución. Tales servicios pueden comprender el personal mas idóneo que los atienda.

Sumisión a arbitraje

En caso de discrepancia entre los miembros, estas se resolverán de acuerdo con el Arbitraje de [ÓRGANO ARBITRAL], según la Ley de Arbitraje de 23 de diciembre de 2003, renunciando expresamente las partes firmantes a acudir a los Tribunales y comprometiéndose expresamente también a estar y pasar y cumplir los términos del laudo arbitral.

Inscripción en el Registro Especial del Ministerio de Economía y Hacienda

Se solicita la inscripción de la presente escritura, con sus estatutos, en el Registro Especial del Ministerio de Economía y Hacienda, a efectos de la obtención de los beneficios fiscales correspondientes.

Protección de datos personales

Advierto expresamente al compareciente que sus datos van a ser incorporados al fichero del Protocolo y documentación notarial y al fichero de Administración y organización, así como del hecho de que, en su caso, tales datos pueden ser cedidos a aquellas Administraciones públicas que según una norma con rango de ley tengan derecho a ello. Hechas las advertencias de sus derechos al respecto.

Les leo, por su elección, esta escritura, advertidos de su derecho a leerla por sí, del que no usan y, tras hacerles las oportunas explicaciones verbales para su cabal conocimiento, manifiestan quedar enterados, la aceptan, se ratifican y firman.

Yo, el Notario, Doy fe de que el consentimiento ha sido libremente prestado y de que el otorgamiento se adecua a la legalidad y a la voluntad debidamente informada de los otorgantes.

Queda extendida en un total de [Nº] folios de papel notarial, el primero con el número [NÚMERO] y los demás con los números siguientes en orden correlativo.

Y de su contenido, DOY FE.

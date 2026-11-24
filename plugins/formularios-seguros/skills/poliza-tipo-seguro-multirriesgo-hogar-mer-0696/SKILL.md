---
name: poliza-tipo-seguro-multirriesgo-hogar-mer-0696
description: "Póliza tipo de seguro multirriesgo del hogar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Póliza tipo de seguro multirriesgo del hogar

> Formulario **MER-0696** del plugin **Seguros: pólizas, coberturas y reclamaciones** (`formularios-seguros`) · Mercantil › Seguros · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Póliza tipo de seguro multirriesgo del hogar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Póliza tipo de seguro multirriesgo del hogar” para mi caso». También puedes invocarla directamente con `/formularios-seguros:poliza-tipo-seguro-multirriesgo-hogar-mer-0696`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguros:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguros: pólizas, coberturas y reclamaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] PLAZO

## Normas que cita el formulario

- art. 1902 Código Civil

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

ELEMENTOS PERSONALES:
BIENES ASEGURADOS CONTINENTE:
VALOR DE LOS BIENES ASEGURADOS
GARANTÍAS
EXCLUSIONES COMUNES A TODAS LAS GARANTÍAS
Perfección, toma de efecto y duración del seguro
PAGO DE LA PRIMA
DECLARACIONES
LA TRANSMISIÓN DE LOS BIENES ASEGURADOS
LA TRAMITACIÓN DE SINIESTROS
La tasación de los daños
LA DETERMINACIÓN DE LA INDEMNIZACIÓN
EL PAGO DE LA INDEMNIZACIÓN
NORMAS DE TIPO GENERAL COMUNICACIONES:
REVALORIZACIÓN AUTOMÁTICA ANUAL DE LOS CAPITALES ASEGURADOS DE LA PRIMA
Cláusula de indemnización de las pérdidas derivadas de acontecimientos extraordinarios acaecidos en España
Protección de datos

1. ELEMENTOS PERSONALES:

ASEGURADOR:

MEDIADOR:

TOMADOR:

ASEGURADO:

BENEFICIARIO:

ACREEDOR HIPOTECARIO:

2. BIENES ASEGURADOS CONTINENTE:

Elementos de construcción (cimientos, paredes, tabiques, suelos, techos, etc.).

- Instalaciones fijas del edificio garantizado (calefacción, gas, agua, electricidad, etc.).

- Elementos de decoración adheridos permanentemente a paredes, techos y suelo del edificio (falsos techos, moquetas, maderas, etc.).

- Toldos, persianas embutidas en su carril, contraventanas y cualquier otro elemento de cierre instalado en el edificio.

- Dependencias anexas, instalaciones deportivas, garajes y trasteros.

- Vallas, cercas, muros de cerramiento y contención, aceras y viales cuando pertenezcan al edificio.

- Antenas fijas receptoras de radio y televisión.

Si el asegurado es propietario de un inmueble en régimen de propiedad horizontal, se incluye la parte indivisa de las partes comunes del edificio, caso de resultar inexistente o insuficiente el seguro establecido por cuenta común.

Exclusiones:

- Las plantas, árboles y la jardinería en general. CONTENIDO:

- Todos los muebles y objetos de uso personal que se encuentran en la vivienda o en dependencias anexas a la misma, siempre que sean objetos de propiedad del asegurado, de sus familiares, de personas que convivan con el asegurado o de su personal doméstico.

Mobiliario especial:

- Objetos de especial valor (prendas de piel, obras de arte, colecciones numismáticas y filatélicas, etc.).

- Joyas.

No se incluyen en el contenido:

- Vehículos terrestres, aéreos o náuticos y sus remolques.

- Los animales vivos.

- La moneda de curso legal, títulos mobiliarios y efectos de comercio.

3. VALOR DE LOS BIENES ASEGURADOS

CONTINENTE: el precio de su valor de reconstrucción a nuevo, sin aplicar descuento por su antigüedad.

CONTENIDO: su valor de reposición en el mercado sin aplicar descuento por uso o antigüedad, salvo en los aparatos de imagen, sonido, ordenadores personales y sus accesorios, cuando su antigüedad sea superior a tres años. Para este último tipo de bienes, el valor asegurado será su valor real, es decir, el valor de nuevo en el mercado en el momento de la suscripción de la póliza, deduciendo su vetustez por uso o antigüedad.

CAPITALES ASEGURADOS: si el día del siniestro resulta que de las estimaciones realizadas, dichos valores exceden de la suma garantizada, será de aplicación, salvo para las garantías suscritas a primer riesgo, la regla proporcional que se enuncia en la cláusula sobre la DETERMINACIÓN DE LA INDEMNIZACIÓN.

Los bienes están asegurados contra los daños causados por los eventos enumerados anteriormente, hasta el límite por siniestro de la suma asegurada para cada una de las garantías.

4. GARANTÍAS

INCENDIO Y EXTENSIVOS

INCENDIO: combustión y abrasamiento con llama, capaz de propagarse, de un objeto u objetos que no estaban destinados a ser quemados en el lugar y momento en que se produce.

Consecuencias inevitables del incendio:

- Daños causados al intentar impedir, cortar o extinguir el incendio;

- Gastos que ocasione el transporte de los efectos asegurados o cualquier otra medida adoptada para salvarlos del incendio;

- Menoscabos que sufran los objetos salvados por las circunstancias anteriores;

- Objetos desaparecidos, cuando el asegurado pruebe su preexistencia y salvo que el asegurador pruebe que fueron robados.

Exclusiones:

- Daños causados por la sola acción del calor, por contacto directo o indirecto con aparatos que generen calor.

- Accidentes del fumador cuando no se produzca llama o cuando los objetos caigan aisladamente al fuego.

EXPLOSIÓN: acción súbita y violenta de la presión o de la depresión de gases o vapores.

CAÍDA DEL RAYO: la descarga violenta producida por una perturbación en el campo eléctrico de la atmósfera.

DAÑOS ELÉCTRICOS: daños causados en instalaciones y aparatos eléctricos, electrónicos y sus accesorios ocasionados por cortocircuito, propia combustión o corrientes anormales.

HUMO: daños causados por escapes o fugas accidentales, repentinos y anormales, tanto internos como externos a la vivienda.

CHOQUE O IMPACTO DE VEHÍCULOS TERRESTRES: daños directos producidos por el choque o impacto de vehículos terrestres.

Se excluyen los daños causados por vehículos contratados, estén en posesión o sean de propiedad del asegurado o de las personas que de él dependan.

CAÍDA DE AERONAVES: daños directos producidos por la caída de aeronaves, astro- naves o de los objetos que caigan de las mismas.

ONDAS SÓNICAS: daños ocasionados por ondas sónicas producidas por aeronaves o astronaves.

DERRAME O ESCAPE DE LAS INSTALACIONES DE EXTINCIÓN: los daños materia- les directos producidos como consecuencia de la falta de estanquidad, escape, derrame, fuga, rotura, caída, derrumbamiento o fallo general de cualquiera de los elementos de dicha instalación que utilice agua o cualquier otro agente extintor.

Quedan excluidos los daños producidos:

a) En el propio sistema extintor por el derrame o escape.

b) Por la utilización de las instalaciones para fines distintos al de la extinción automá- tica de incendios.

c) Por conducciones subterráneas o instalaciones situadas fuera del recinto del riesgo asegurado, o por el agua embalsada para este fin.

ACTOS DE VANDALISMO O MALINTENCIONADOS: los daños causados por actos de vandalismo o malintencionados, individual o colectivamente por personas distintas al asegurado o personas de las que el asegurado deba responder y los daños producidos en el curso de reuniones y manifestaciones efectuadas conforme a lo dispuesto en la Ley Orgánica 9/1983 de 15 de julio, así como durante el transcurso de huelgas legales.

Quedan excluidos los daños ocasionados como consecuencia de pintadas, inscripciones, pegado de carteles y hechos análogos.

LLUVIA, VIENTO, PEDRISCO Y NIEVE: los daños derivados de la lluvia, siempre que la precipitación sea superior a 40 litros por metro cuadrado y hora; del viento, siempre que la velocidad del mismo supere los 96 km/h; y el pedrisco y la nieve, cualquiera que sea su intensidad.

La medición de estos fenómenos se acreditará fundamentalmente con los informes expedidos por los organismos competentes más cercanos o, en su defecto, mediante aportación de pruebas convincentes.

Exclusiones:

- Los daños producidos por nieve, agua, arena o polvo, que penetre por huecos o aberturas que hayan quedado sin cerrar, o cuyo cierre fuera defectuoso, así como daños al aire libre o en el interior de construcciones abiertas.

- Los daños producidos por heladas, frío, olas o mareas, incluso cuando estos fenómenos hayan sido causados por el viento.

- Que se deriven de defectos o falta de mantenimiento y conservación de los bienes asegurados.

- Las goteras, filtraciones, humedades, u oxidaciones, producidas de forma paulatina, debidas a otras causas distintas de las garantizadas.

INUNDACIÓN: los daños materiales por inundación siempre que no sean consecuencia de hechos o fenómenos que correspondan a riesgos amparados por el Consorcio de Compensación de Seguros, a consecuencia de:

- Desbordamiento o desviación del curso normal de lagos sin salida natural, canales, acequias y otros cursos o cauces de agua en superficie construidos por el hombre.

- El reventón, rotura o avería de alcantarillados, colectores y otros cauces subterráneos.

- Desbordamiento o rotura de presas o diques de contención. DAÑOS POR AGUA

DAÑOS POR AGUA: los daños materiales directos producidos por el agua sobre los bienes asegurados cualquiera que sea la causa que las origine ya sean provenientes de bienes propios o ajenos, debidos a:

* Fugas, roturas o desbordamientos:

- De cañerías, de conducciones de distribución, de evacuación o de depósitos de aguas residuales.

- De canalones o bajadas de agua.

- De las instalaciones de calefacción central o individual.

- De los aparatos que utilizan el agua, comprendiendo máquinas de lavar la vajilla y la ropa.

- De los recipientes o depósitos.

- Consecutivos a la omisión del cierre de llaves o grifos de agua.

* Filtraciones

* Los gastos de la localización y la propia reparación de la avería. Exclusiones:

- Daños originados por un hecho de la naturaleza.

- Daños que tengan su origen en las redes de saneamiento subterráneas, tales como fosas sépticas, arquetas, cloacas, alcantarillados y similares.

- Daños que resulten de una falta de reparación o mantenimiento.

- Daños debidos a la humedad y condensación.

- Daños resultantes de heladas.

- Daños ocasionados por trabajos de construcción o reparación del continente de la vivienda.

ROBO, EXPOLIACIÓN Y HURTO:

Algunas definiciones que han de ser precisadas en el contrato:

ROBO: sustracción o apoderamiento ilegítimo de los bienes designados en la póliza, en contra de la voluntad del asegurado mediante escalo o actos que impliquen fuerza o violencia en las cosas o introduciéndose el autor o autores en la vivienda asegurada y/o sus anexos mediante ganzúa u otros instrumentos no destinados a abrir puertas.

EXPOLIACIÓN (ATRACO): la sustracción o apoderamiento ilegítimo de los bienes designados en la póliza contra la voluntad del asegurado, mediante actos de intimación o violencia realizados sobre las personas que los custodian o vigilan.

HURTO: la sustracción de los bienes designados en la póliza contra la voluntad del asegurado, sin empleo de la fuerza o violencia en las cosas ni intimidación ejercida sobre las personas.

* Quedan garantizados los daños materiales directos por la destrucción, desaparición y deterioro de los objetos asegurados producidos a consecuencia o intento de ROBO o ATRACO en el interior de la vivienda o en sus dependencias anexas.

No se incluyen:

- Los objetos que se hallen fuera de la vivienda asegurada, en dependencias que carezcan de las protecciones declaradas en las condiciones particulares o terrazas, patios, jardines u otras construcciones abiertas.

Igualmente cuando los huecos de entrada a la vivienda no tuviesen activados los sistemas de cierre declarados y habitualmente empleados.

- Las joyas y objetos especiales que se encuentren en garajes y trasteros u otras dependencias que no sean de uso exclusivo.

* Quedan garantizados con los límites siguientes, el robo y la expoliación:

- Del dinero en efectivo hasta el 5% de la suma asegurada en contenido, con un máximo de 300 peuross.

- Las joyas se indemnizarán en su conjunto, hasta 600 euros, salvo que dichas joyas se hayan asegurado expresamente por un importe superior y se haya satisfecho la correspondiente prima.

- Los objetos de especial valor siempre que figuren detallados expresamente por su importe en las condiciones particulares. En caso de no encontrarse detallados, el valor máximo de cada objeto será de 6.000 de euros.

No se incluyen:

- El robo de joyas declaradas en caja fuerte o empotrada cuando éstas no se hallen debidamente cerradas.

- Las joyas cuando la vivienda haya permanecido deshabitada más de4 días consecutivos salvo que estén depositadas en caja de caudales.

* Se garantiza el HURTO cometido en el interior de la vivienda por terceras personas hasta el 5% del contenido.

No se incluyen los objetos de valor especial, las joyas y dinero en efectivo o cualquier documento que represente una garantía en dinero, aunque se hubiera pactado expresa- mente su inclusión en la póliza.

DAÑOS POR ROBO AL CONTINENTE: los daños y desperfectos que sufra la vivienda, el garaje o los trasteros causados por el robo o su tentativa.

SUSTRACCIÓN DE LLAVES: los gastos de compra y sustitución de las cerraduras y llaves de la vivienda, cuando después de haber sufrido un acto de intimidación o violencia tanto en el interior como en el exterior de la vivienda, sean sustituidas, como medida de precaución que pueda evitar un fácil acceso a la vivienda.

USO FRAUDULENTO DE TARJETAS: las pérdidas económicas sufridas por el asegurado o de las personas que convivan con él a consecuencia de robo, expoliación, hurto o extravío de tarjetas.

Para que sea efectiva la cobertura debe realizarse la correspondiente denuncia ante la autoridad competente y el siniestro se tiene que haber producido dentro de las 48 horas anteriores o posteriores al día en que se hubiera comunicado de forma fehaciente a la entidad emisora, la desaparición de los documentos objeto de cobertura.

Quedan excluidas las pérdidas económicas que sean cubiertas por la entidad emisora de la tarjeta.

ATRACO FUERA DEL HOGAR: las pérdidas materiales que el asegurado o las personas que conviven habitualmente con él sufran como consecuencia de una expoliación o atraco fuera de la vivienda asegurada.

ROTURA DE LUNAS, CRISTALES, LOZA SANITARIA, MÁRMOLES, GRANITOS Y VITROCERÁMICA DE COCINA: la reposición y colocación, incluidos los gastos de traslados, originados por la rotura accidental de lunas, cristales, espejos, muebles de metacrilato, loza sanitaria, mármoles, granitos y la rotura de las placas vitrocerámicas de la cocina.

Quedan excluidos los daños producidos por:

a) Las roturas de lámparas y bombillas de todas clases, cristalerías, objetos de uso personal, elementos decorativos no fijos, lentes de cualquier clase, radios televisores y demás aparatos de visión y sonido.

b) Las roturas derivadas de realizarse trabajos de construcción o reparación del continente.

c) Los simples arañazos, raspaduras, desconchados o deterioros superficiales. d) Los mármoles y granitos que recubran paredes, suelos y techos.

VEHÍCULOS Y/O EMBARCACIONES EN GARAJE: los daños que pueda sufrir el vehículo y/o embarcación designado en la póliza únicamente en estado de reposo, cuando se encuentren estacionados en las plazas de garaje o aparcamiento, a consecuencia de un siniestro por caída del rayo, incendio o explosión, de origen externo al vehículo o embarcación.

Dicho vehículo y/o embarcación deberá valorarse como nuevo, siendo su suma asegurada independiente de la fijada para contenido.

TRASLADO TEMPORAL DE BIENES: las coberturas contratadas en la póliza se ex- tienden a los objetos transportados por el asegurado o por las personas que conviven habitualmente con el asegurado en el curso de un viaje desde su residencia habitual al lugar de estancia o viceversa o durante su estancia fuera de su vivienda cuando dichos bienes se encuentren en viviendas, apartamentos y habitaciones de hotel o pensión.

Exclusiones:

- El contenido de una vivienda secundaria propiedad del asegurado que no esté

asegurada con la aseguradora del multirriesgo.

- La estancia del contenido en un edificio destinado a vivienda, ocupado por el asegurado o sus familiares, por un período superior a 3 meses.

GASTOS COMUNES

GASTOS DE SALVAMENTO: el asegurador tomará a su cargo, con un máximo del 25% de las sumas aseguradas de los capitales de continente y contenido, los gastos efectuados por el asegurado para aminorar las consecuencias de un siniestro.

El asegurado tendrá derecho a esta indemnización aunque las medidas adoptadas no hayan tenido éxito, siempre y cuando dichas medidas no sean inoportunas o desproporcionadas a los bienes salvados.

GASTOS POR EXTINCIÓN DE INCENDIOS: los gastos en los que incurra el asegurado, a consecuencia de un siniestro cubierto por la póliza por aplicación de las medidas necesarias adoptadas por el asegurado o por la autoridad con el fin de cortar o impedir la propagación del incendio. La aseguradora también asumirá la tasa municipal de bomberos.

GASTOS DE DEMOLICIÓN Y DESESCOMBRO: los gastos en los que el asegurado, a consecuencia de un siniestro cubierto por la póliza, incurra por la demolición y el desescombro de la vivienda siniestrada, incluyendo los producidos por el traslado de los escombros hasta el lugar más próximo en el que sea oportuno depositarlos

DESALOJAMIENTO FORZOSO: gastos originados por el desalojamiento provisional de la vivienda. Comprenden:

- Si el asegurado es inquilino, la diferencia de precio de alquiler que el asegurado tenga que pagar por una vivienda de características similares a la que ocupaba.

- Si el asegurado es propietario, el precio del alquiler que el asegurado tenga que pagar, de una vivienda de características similares a la que ocupaba.

TRASLADO DE LOS OBJETOS SALVADOS: gastos causados por el traslado necesario de los objetos asegurados mientras dure el desalojo de la vivienda siniestrada.

REPOSICIÓN DE DOCUMENTACIÓN DESTRUIDA: los gastos de reconstrucción de documentos o expedición de duplicados.

LIMPIEZA Y EXTRACCIÓN DE LODOS: los gastos que ocasione la extracción de barros y lodos.

RESTAURACIÓN ESTÉTICA: los gastos necesarios para restablecer la composición estética existente antes del siniestro, en cualquier estancia de la vivienda asegurada afectada por éste, con independencia de los daños directos, cuya reparación se realizará utilizando materiales de características y calidad similares a los originales.

Quedan excluidos los sanitarios con su correspondiente grifería.

ALIMENTOS REFRIGERADOS: la pérdida o el deterioro de alimentos depositados en frigoríficos o equipos de refrigeración como consecuencia de la paralización de la instalación frigorífica por avería de la misma o por un paro accidental.

RESPONSABILIDAD CIVIL: el pago de las indemnizaciones pecuniarias que el asegurado deba satisfacer como civilmente responsable de los daños corporales y/o materiales involuntariamente causados a terceros, por hechos de su vida privada (extra profesional) con arreglo a los artículos 1902 y siguientes del Código Civil.

Si el asegurado es copropietario del edificio donde se encuentra la vivienda asegurada, la garantía se extiende a la cuota-parte que le corresponda por responsabilidades de la comunidad de propietarios del inmueble, por los artículos antes mencionados.

Independientemente del número de perjudicados, consideraremos como un solo y mismo siniestro, todos los daños corporales y/o materiales que provengan de una misma causa.

Expresamente se incluyen:

- La responsabilidad por actos de la vida privada de las personas de las cuales el asegurado tenga que responder.

- La responsabilidad de los demás familiares que convivan habitualmente con el asegurado por sus propios actos dentro de la vida privada.

- Uso de bicicletas o de cualquier otro medio de locomoción no motorizado.

- Uso de aparatos domésticos, dentro de la vivienda asegurada.

- Uso y guía de caballos u otros animales de silla.

- La posesión de animales domésticos.

- La propiedad, tenencia y uso de armas de fuego, para defensa, hallándose en posesión de las guías y licencias requeridas.

- El ejercicio realizado como aficionado de actividades deportivas en general.

- La intoxicación o envenenamiento causado por alimentos o bebidas consumidos en su casa.

Quedan excluidos:

- Obligaciones contractuales.

- La responsabilidad por el incumplimiento de disposiciones oficiales. En ningún caso el asegurador responderá del pago de multas o de las consecuencias de su impago.

- Los daños causados por el ejercicio de un oficio, profesión, servicio, cargo o actividad, retribuido o no.

- Instalaciones industriales y comerciales así como de su explotación.

- Responsabilidades que deban ser objeto de cobertura por un seguro obligatorio.

- Los daños derivados del uso de vehículos a motor o de embarcaciones de cualquier tipo, acuáticas o aéreas.

- La propiedad, uso y tenencia de armas de fuego para prácticas deportivas de tiro o caza.

RESPONSABILIDAD CIVIL LOCATIVA: si el asegurado es el inquilino el asegurador garantiza los daños que la vivienda sufra y de los que el asegurado deba responder frente al propietario.

RESPONSABILIDAD CIVIL INMOBILIARIA: la responsabilidad civil como propietario o copropietario de la vivienda designada en la póliza. En el caso de ser copropietario la garantía será la parte proporcional que le corresponda por responsabilidad de la comunidad de propietarios del inmueble.

También los daños ocasionados a los elementos comunes en caso de ser copropietario.

Quedan no obstante excluidos la parte proporcional que como propietario de los elementos comunes le corresponda.

Expresamente se incluyen:

- Daños por los trabajos realizados en la vivienda objeto del seguro.

- La caída de antenas receptoras individuales de radio y televisión, instaladas en el edificio vivienda de su propiedad.

- Daños por agua ocasionados por las instalaciones de la vivienda asegurada.

DEFENSA JUDICIAL: en cualquier procedimiento judicial que se derive de un siniestro amparado por la póliza el asegurador asumirá la defensa jurídica frente a las reclamaciones del perjudicado, designando los letrados y procuradores que le defenderán y representarán en las actuaciones judiciales que se le siguieren por la reclamación de responsabilidades civiles cubiertas por esta póliza, aun cuando dichas reclamaciones fueran infundadas.

El asegurado deberá prestar la colaboración necesaria a la defensa, comprometiéndose a otorgar los poderes y la asistencia personal que fueren precisos.

Independientemente del resultado del procedimiento judicial, nos reservamos la decisión de ejercitar los recursos legales que procedieran contra dicho resultado o el conformarnos con el mismo.

Si se produce algún conflicto entre el asegurado y el asegurador, por tener que sustentar intereses diferentes, lo pondremos en su conocimiento, sin perjuicio de realizar aquellas diligencias, que por su carácter urgente, sean necesarias para la defensa. En este caso, el asegurado podrá optar entre el mantenimiento de la dirección jurídica por cuenta del asegurador, o en confiar su defensa a otra persona. En este último caso le abonaremos los gastos de tal dirección jurídica hasta el 1% de la suma asegurada para la garantía de responsabilidad civil.

CONSTITUCIÓN DE FIANZAS: abonaremos las fianzas que al asegurado le impongan como garantía exclusiva de responsabilidades civiles o para la obtención de la libertad provisional en procedimientos penales, a causa de siniestros amparados por esta póliza.

ASISTENCIA EN EL HOGAR

SUJETOS: a los efectos de esta garantía, se entenderá por asegurado la persona física titular de la póliza, su cónyuge, hijos, familiares y demás personas, siempre que su domicilio legal sea la vivienda garantizada.

OBJETO DEL SERVICIO: facilitar al asegurado la realización de los trabajos

- De reparación de su vivienda, dañada por un siniestro cubierto por el seguro.

- De reforma, decoración o modificación que desee efectuar en su vivienda, aunque no haya ocurrido un siniestro.

- Precisos para resolver las situaciones de emergencia consideradas como PRESTACIONES COMPLEMENTARIAS. Cuando se trate de resolver cualquiera de estas situaciones de emergencia, se estará a lo dispuesto en el correspondiente apartado para cada una de las prestaciones.

RELACIÓN DE TRABAJOS: albañilería, antenista, ATS, barnizadores, carpintería, car- pintería metálica, cerrajería, cristaleros, deshollinadores, electricistas, electrodomésticos, empapeladores, enfermeras, enmoquetadores, entarimadores, escayolistas, fontaneros, jardineros, limpiacristales, limpiezas generales, mensajeros, mudanzas, niñeras, parquetistas, persianas, pintores, porteros automáticos, sintasol, tapiceros, televisores y vídeos (reparación y alquiler), vigilantes.

GARANTÍA: todos los trabajos están avalados durante tres meses por la aseguradora.

PAGO DE LOS TRABAJOS:

- El asegurado no abonará cantidad alguna por:

* Gastos de desplazamiento de profesionales.

* Reparación de daños causados por siniestros cubiertos por su póliza. Sólo abonará

en este caso la franquicia, cuando exista.

* Recargos en concepto de urgencia o de realizar el trabajo en días festivos.

- El asegurado abonará el importe de la mano de obra y los materiales empleados, al terminar cada trabajo, cuando se trate de reforma, decoración o modificación que desee efectuar en su vivienda, aunque no haya ocurrido un siniestro.

- Cuando se trate de resolver cualquiera de las situaciones de emergencia previstas en el apartado de PRESTACIONES COMPLEMENTARIAS, se estará a lo dispuesto en dicho apartado para cada una de las prestaciones.

SOLICITUD DE SERVICIO: lo puede pedir el asegurado en cualquier momento del día o de la noche, laborales o festivos, mediante llamada al teléfono señalado en estas condiciones generales e indicando el número de póliza, datos personales y trabajo a realizar.

FUNCIONAMIENTO DEL SERVICIO: el servicio de reparaciones urgentes trabaja las 24 horas. Los servicios normales se ejecutan en menos de 24 horas desde el momento de su solicitud, si ésta se realiza en día laborable entre las 9 y las 18 horas.

PRESTACIÓN DEL SERVICIO: esta garantía se presta por medio de la sociedad XXXX.

PRESTACIONES COMPLEMENTARIAS:

- Servicio de cerrajería urgente

En caso de que no se pueda abrir la puerta de la vivienda asegurada por:

* Pérdida, extravío o robo de las llaves.

* Inutilización de la cerradura.

* Cualquier otro hecho accidental.

- Reposición de televisión y vídeo

Se facilitará al asegurado el uso de un aparato de televisión o vídeo cuando no pueda disponer de los suyos debido a robo u otra clase de siniestro cubierto por la póliza.

Este servicio será gratuito para el asegurado, durará mientras lo necesite, con un máximo de 15 días, y los aparatos serán de características similares a los siniestrados.

- Personal de seguridad. Cuando a consecuencia de robo o inhabitabilidad de la vivienda, ésta sea fácilmente accesible desde el exterior, se le enviará a cargo de la aseguradora personal de seguridad cualificado durante un máximo de 96 horas, contadas a partir de la llegada de éstos a la vivienda afectada, dando por finalizado este servicio desde el momento en que el hecho accidental sea subsanado.

- Búsqueda de hotel: Cuando, a consecuencia de un siniestro, se produjera la inhabitabilidad de la vivienda asegurada, nos encargaremos de buscarle un hotel y tomaremos a nuestro cargo el pago del mismo.

- Retorno del asegurado a su domicilio a consecuencia de un siniestro grave. Si cuando el asegurado se encuentra de viaje se produjera en su vivienda un siniestro garantizado por la póliza que diera lugar a la inhabitabilidad de la misma o aconteciera la hospitalización y/o fallecimiento de alguno de los asegurados a consecuencia de un accidente ocurrido en el hogar, se pondrá a su disposición un billete de tren (primera clase) o de avión (clase turista) para volver al domicilio desde donde se encontrara, y otro billete para volver al lugar donde estuviera; o dos billetes hasta su domicilio siempre que el acompañante tuviera la condición de asegurado.

Respecto a los gastos de desplazamiento de las personas aseguradas, solamente nos haremos cargo del exceso sobre los previstos normalmente por el asegurado (billetes de tren, avión, travesías marítimas, peajes, carburantes por vehículo, etc.) reservándose el derecho a exigir al asegurado la devolución de los billetes de pasaje no utilizados.

- Accidente de algún asegurado ocurrido en el hogar: En el supuesto de que por la causa señalada anteriormente existiera prescripción médica de guardar cama sin necesidad de hospitalización, organizaremos y tomaremos a nuestro cargo las siguientes prestaciones:

- Envío de una enfermera que asista al accidentado hasta un máximo de 96 horas.

- Envío de una niñera cuando la persona accidentada tuviere a su cargo habitualmente el cuidado de los menores de 14 años. El plazo máximo de otorgamiento de la garantía es 96 horas.

- Envío de medicamentos prescritos al domicilio. El coste de los medicamentos será siempre por cuenta del asegurado.

- Si, a consecuencia del accidente ocurrido en el hogar existe prescripción médica de hospitalización, organizaremos y tomaremos a nuestro cargo el traslado en ambulancia hasta el hospital más próximo que determine el médico.

- Transmisión de mensajes urgentes: nosotros nos encargaremos, a requerimiento del asegurado, de transmitir a sus familiares, cualquier mensaje urgente cuya necesidad venga determinada por un siniestro cubierto por la póliza.

CONDICIÓN ADICIONAL: el asegurador no es responsable de los retrasos o incumplimientos que sean debidos a fuerza mayor.

5. EXCLUSIONES COMUNES A TODAS LAS GARANTÍAS

1. Los daños resultantes del ejercicio de una actividad comercial, industrial o profesional.

2. Los daños derivados de fermentación, oxidación, vicio propio y defecto de fabricación de las instalaciones y bienes garantizados, así como los debidos al uso o desgaste normal de los bienes asegurados.

3. Los daños producidos cuando el siniestro se origine por dolo, culpa grave o complicidad del asegurado o sus familiares.

4. Los daños ocasionados directamente por los efectos mecánicos, térmicos y radiactivos, debidos a reacciones o transmutaciones nucleares, cualquiera que sea la causa que los produzca.

5. Los daños ocasionados por eventos amparados por el Consorcio de Compensación de Seguros, según la legislación vigente, tal como quedan incluidas en la CLÁUSULA DE INDEMNIZACIÓN DE LAS PÉRDIDAS DERIVADAS DE ACONTECIMIENTOS EX- TRAORDINARIOS ACAECIDOS EN ESPAÑA.

6. Los daños a consecuencia de guerra civil o internacional, levantamientos popula- res o militares, insurrección, rebelión, revolución u operaciones bélicas de cualquier clase y terrorismo.

7. Eventos calificados por el Gobierno de la nación como catástrofe o calamidad nacional.

8. Producidos por hechos o fenómenos de la naturaleza que, estando cubiertos por el Consorcio de Compensación de Seguros, este Organismo no admita la efectividad del derecho de los asegurados por incumplimiento de alguna de las normas establecidas en el Reglamento y Disposiciones Complementarias vigentes en la fecha de su ocurrencia.

9. Las diferencias entre los daños producidos y las cantidades indemnizadas por el Consorcio de Compensación de Seguros en razón de la aplicación de franquicias, retracciones o aplicación de reglas proporcionales u otras limitaciones.

10. Las sanciones administrativas y/o judiciales.

11. Las penalizaciones contractuales.

6. PERFECCIÓN, TOMA DE EFECTO Y DURACIÓN DEL SEGURO

- Las garantías del contrato entran en vigor en el día y horas indicadas en las condiciones particulares, una vez haya sido perfeccionado el mismo y satisfecho el pago de la prima.

En caso de demora en la suscripción de la póliza o en el caso del recibo de prima, las obligaciones del asegurador comenzarán a las 24 horas del día en que el tomador haya cumplimentado los dos requisitos.

- A la expiración del período indicado en las condiciones particulares de la póliza, el contrato se entenderá prorrogado por el plazo de un año y así sucesivamente a la expiración de cada anualidad.

Las partes pueden oponerse a la prórroga del contrato mediante una notificación escrita a la otra parte, efectuada con un plazo de [PLAZO], al menos, un mes de anticipación a la conclusión del período del seguro en curso cuando quien se oponga a la prórroga sea el tomador, y de dos meses cuando sea el asegurador.

7. PAGO DE LA PRIMA

- El tomador está obligado al pago de la prima en las condiciones estipuladas en la póliza. Si se han pactado primas periódicas, la primera de ellas será exigible desde el día y la fecha acordados para la toma y efecto del contrato. Las primas sucesivas se deberán hacer efectivas en los correspondientes vencimientos.

Si en las condiciones particulares no se determinan ningún lugar para el pago de la prima, se entenderá que éste ha de hacerse en el domicilio del asegurador.

En el caso de que la póliza no deba de entrar en vigor, el tomador podrá demorar el pago de la prima hasta el momento en que aquélla deba tomar efecto.

- Para el pago de cada prima, con excepción de la primera, tiene un plazo de gracia de un mes a contar desde el día siguiente a la fecha de vencimiento.

- Si por culpa del tomador la primera prima no ha sido pagada, o la prima única no lo ha sido a su vencimiento tendremos derecho a resolver el contrato o a exigir el pago de la prima debida en vía ejecutiva con base en la póliza. Salvo pacto en contrario en las condiciones particulares, si la prima no ha sido pagada antes de que se produzca el siniestro, el asegurador quedará liberado de la obligación de indemnizar.

En el caso de falta de pago de una de las primas siguientes, la cobertura queda suspendida un mes después del día del vencimiento. Si el asegurador no reclama el pago dentro de los seis meses siguientes al vencimiento de la prima, se entenderá que el contrato queda extinguido.

En cualquier caso, el asegurador, cuando el contrato esté en suspenso, sólo podremos exigir el pago de la prima del período en curso.

Si el contrato no hubiere sido resuelto o extinguido conforme a los números anteriores, la cobertura vuelve a tener efecto a las 24 horas del día en que el tomador pagó su prima.

DOMICILIACIÓN BANCARIA: si se determina en las condiciones particulares la domiciliación bancaria de los recibos de la prima, se aplicarán las siguientes normas:

1) El tomador entregará al asegurador una carta dirigida al Banco o Caja de Ahorros dando la orden oportuna al efecto.

2) La prima se entenderá satisfecha a su vencimiento salvo que, intentado el cobro dentro del plazo de un mes, no existiesen fondos suficientes en la cuenta corriente desig- nada por el tomador.

3) Si el asegurador dejase transcurrir el plazo de un mes sin presentar el recibo al cobro, y al hacerlo no existiesen fondos suficientes en la cuenta por el tomador designada, se lo notificaremos por carta certificada u otro medio indubitado, concediéndole un nuevo plazo de un mes para que nos comunique la forma en que hará efectivo su importe. Este plazo se computará desde la recepción de la expresada carta o notificación en el último domicilio que nos haya comunicado.

PAGO FRACCIONADO DE LA PRIMA: la prima del seguro es anual, si bien el asegurador podrá acceder, a petición del tomador, y siempre que el recibo de prima haya sido domiciliado, a fraccionarla por trimestres o semestres, en cuyo caso el impago de cualquiera de los fraccionamientos dejaría en suspenso la cobertura.

En caso de siniestro, el asegurador podrá deducir de la indemnización a su cargo las fracciones pendientes de cobro de la anualidad en curso.

Si la póliza se anulase por causas ajenas al asegurador, antes de terminar cualquier anualidad del seguro, el tomador deberá satisfacer las fracciones de prima que falten para completar el importe de la prima anual.

8. DECLARACIONES

La presente póliza ha sido concertada sobre la base de las declaraciones formuladas por el tomador/asegurado y las contenidas en la solicitud-cuestionario facilitado por el asegurador conteniendo aquellas que puedan influir en la valoración del riesgo (descripción de la vivienda, clase de edificación, ubicación, régimen, metros cuadrados, construcción, elementos de seguridad, etc.) y que han motivado por nuestra parte la aceptación del riesgo, la asunción de las obligaciones derivadas del contrato y la fijación de la prima.

Si el cuestionario de la póliza difiere de la solicitud-cuestionario o de las cláusulas acordadas, el tomador del seguro podrá reclamar al asegurador, en el plazo de un mes a contar desde la entrega de la póliza, para que subsane la divergencia existente. Transcurrido dicho plazo sin efectuarse reclamación, se estará a lo dispuesto en la póliza.

DEBERES DE DECLARACIÓN ANTERIORES A LA SUSCRIPCIÓN DEL SEGURO:

- Comunicar la existencia de otras pólizas contratadas con otros aseguradores cubriendo los efectos que un mismo riesgo puede producir sobre los mismos bienes asegurados.

- Permitir la entrada en el lugar del riesgo a las personas que al efecto designe la aseguradora y a proporcionarles los datos que les interesen.

- Declarar todas las circunstancias conocidas que permitan al asegurado valorar el riesgo y, muy especialmente, las que figuran en las preguntas cuestionario.

- El asegurador puede rescindir el contrato, mediante declaración dirigida al tomador, en el plazo de un mes a partir del conocimiento de la reserva o inexactitud por parte del tomador del seguro. En este caso el asegurador hará suyas las primas correspondientes al período en curso, salvo que exista dolo o culpa grave por parte del asegurador.

- Si sobreviene un siniestro antes de que el asegurador haga la declaración a la que se refiere el párrafo anterior, la indemnización se reducirá proporcionalmente a la diferencia entre la prima convenida en la póliza y la que correspondería de haberse conocido la verdadera entidad del riesgo.

- Cuando la reserva o inexactitud se produzca por dolo o culpa grave del tomador del seguro, el asegurador quedará liberado del pago de la indemnización.

DEBERES DE DECLARACIÓN DURANTE LA VIDA DEL SEGURO:

- Deberá comunicar al asegurador tan pronto como sea posible todas las circunstancias que agraven el riesgo y que sean de tal naturaleza que si hubieran sido conocidas por el asegurador en el momento de la perfección del contrato, no lo habría celebrado o lo habría celebrado en condiciones más gravosas.

- Si durante la vigencia de la póliza fuese comunicada al asegurador una agravación del riesgo, el asegurador podrá proponer una modificación de las condiciones del contrato en un plazo de dos meses a contar desde el día en que la agravación le haya sido declarada. En tal caso, el tomador dispone de quince días, a contar desde la recepción de esa proposición, para aceptarla o rechazarla. En caso de rechazo o de silencio, el asegurador puede, transcurrido dicho plazo, rescindirle el contrato previa advertencia, dándole para que conteste, un nuevo plazo de quince días, transcurridos los cuales, y dentro de los ocho siguientes, le comunicarán al tomador la rescisión definitiva.

- El asegurador puede, igualmente, rescindir el contrato comunicándoselo por escrito dentro de un mes, a partir del día en que tuvo conocimiento de la agravación del riesgo.

- Si sobreviniere un siniestro sin haberse autorizado declaración de agravación del riesgo, el asegurador quedará liberado de la prestación, si el tomador o el asegurado ha actuado de mala fe. En otro caso, la prestación se reducirá proporcionalmente a la diferencia entre la prima convenida y la que se hubiera aplicado de haberse conocido la verdadera entidad del riesgo.

- Cualquier variación de las circunstancias deberá ser comunicada tan pronto como sea posible.

- Cualquier transmisión de la propiedad del o de los objetos asegurados, debiéndolo hacer por escrito en el plazo de 15 días una vez verificada la transmisión.

- Los nombres y direcciones de los demás aseguradores, si otro u otros contratos de seguro cubren los riesgos que garantiza el asegurador.

9. LA TRANSMISIÓN DE LOS BIENES ASEGURADOS

- Desde el momento de la enajenación del objeto asegurado, el adquiriente se subroga en los derechos y obligaciones que le correspondía en la póliza al titular de esta póliza.

- Serán solidariamente responsables del pago de las primas vencidas en el momento de la transmisión el adquiriente y el titular de esta póliza, o en caso de que hubiera fallecido, sus herederos. Es decir, que el asegurador puede reclamar el pago del mismo indiferentemente al titular de esta póliza o al nuevo propietario del bien.

- El asegurado deberá declarar por escrito al asegurador la operación correspondiente dentro de los quince días siguientes a la misma.

- Comunicar también por escrito al nuevo adquiriente la existencia del contrato de seguro de la cosa transmitida.

- El asegurador podrá dar fin al contrato dentro de los quince días siguientes al que tenga conocimiento de la transmisión verificada.

- Una vez la aseguradora ha ejercitado su derecho, lo notificaremos por escrito al nuevo propietario y no estará obligado por el contrato al cabo del mes de esta notificación, devolviéndole la parte de prima que corresponda al período de seguro por el que como consecuencia de la rescisión, no hayamos soportado el riesgo.

- O el asegurador podrá seguir con el contrato, lo cual quedará patente si no ha efectuado ninguna notificación dentro de los quince días siguientes a aquel en que tenga conocimiento de la transmisión verificada.

- El adquiriente puede seguir con el contrato haciendo efectivo el pago de la prima del período en curso, o haciéndolo al titular de esta póliza según el acuerdo que hayan podido tomar.

- El adquiriente puede dar fin al contrato comunicándoselo por escrito al asegurador dentro de los 15 días contados desde que conoció la existencia del mismo. En este caso, queda a favor del asegurador la prima correspondiente al período que hubiera comenzado a correr cuando se produce la rescisión.

- Todas las normas señaladas regirán también para los casos de muerte, suspensión de pago, quita y espera, quiebra o concurso.

10. LA TRAMITACIÓN DE SINIESTROS

- El tomador/asegurado debe adoptar cuantas medidas estén a su alcance para limitar o disminuir las pérdidas y/o reclamaciones de responsabilidad y evitar que se pierda cual- quier indicio del delito o de sus autores. También debe facilitar el acceso a la aseguradora el acceso al lugar donde haya ocurrido el siniestro, con el fin de adoptar cuantas medidas sean razonables para aminorar el mismo.

El incumplimiento del deber de salvamento establecido en la póliza da derecho al asegurador a reducir la prestación en la proporción oportuna, e incluso a liberar totalmente al asegurador, si el incumplimiento se produce con la manifiesta intención de perjudicar o engañar al asegurador.

- Comunicar al asegurador la ocurrencia del siniestro dentro del plazo máximo de siete días, contados a partir de la fecha en que conoció su acaecimiento, teniendo el asegurador la posibilidad de exigirle al asegurado los daños y perjuicios causados por la falta de esta declaración.

En el supuesto de existir varios aseguradores, esta comunicación deberá hacerse a cada uno de ellos, con indicación del nombre de los demás.

- En el plazo de cinco días después de la notificación, debe el asegurado indicar al asegurador:

* Número de póliza.

* Fecha, hora y lugar del siniestro.

* Causas conocidas y presumidas.

* Medios adoptados para aminorar las consecuencias.

* Circunstancias del siniestro.

* Detalle de los daños causados por el siniestro, clase de objetos siniestrados y cuantía de los daños derivados.

* En general, toda clase de informaciones sobre las circunstancias y consecuencias del siniestro.

En caso de violación de este deber, se producirá la pérdida del derecho a la indemni- zación, en el supuesto de que exista dolo o culpa grave.

- El asegurado debe conservar los restos y vestigios del siniestro hasta terminada la tasación de daños, salvo en caso de imposibilidad material justificada. Esta obligaciónno puede, en ningún caso, dar lugar a indemnización especial.

- Incumbe al asegurado probar la preexistencia de los objetos. El contenido de la póliza no representará más que una presunción a su favor, cuando razonablemente no puedan presentarse pruebas más eficaces.

- En caso de siniestro de robo, expoliación, hurto y/o actos de vandalismo, inmediata- mente de que tenga conocimiento del siniestro, debe denunciar el hecho ante la autoridad local de policía, indicándoles el nombre del asegurador.

- En caso de siniestro que dé lugar a responsabilidad civil:

* El tomador o el asegurado están obligados a adoptar todas las medidas necesarias para su defensa frente a posibles reclamaciones de responsabilidad civil, debiendo mos- trarse tan diligente en su cumplimiento como si no existiera seguro.

* Se deberá comunicar al asegurador inmediatamente su recepción y, en el plazo de siete días, cualquier notificación judicial o administrativa que llegue a su conocimiento y esté relacionada con el siniestro.

* El tomador o el asegurado deberá prestar la colaboración necesaria para su defensa, puesto que el asegurador actuará en su nombre, y otorgarnos los poderes y la asistencia personal que fueren precisos.

* No aceptar, negociar admitir o rechazar, sin autorización del asegurador, ninguna reclamación relativa a siniestros cubiertos por la presente póliza.

11. LA TASACIÓN DE LOS DAÑOS

- El asegurado debe facilitar al asegurador, o a sus representantes, el acceso a las propiedades en que haya ocurrido el siniestro, para poder verificar y valorar el origen, extensión y consecuencias del mismo.

- El asegurador se personará, a la mayor brevedad posible, en el lugar del siniestro para comenzar las oportunas operaciones de comprobación de las causas y forma de ocurrencia del siniestro, de las declaraciones contenidas en la póliza y de las pérdidas sufridas por los objetos asegurados.

VALORACIÓN DE LOS BIENES:

- El CONTINENTE, incluidos los cimientos pero sin comprender el valor del solar:

* Al precio de su valor de reconstrucción a nuevo en el momento inmediato anterior al siniestro:

- Siempre que su reconstrucción se haga en los dos años siguientes a partir de la fecha del siniestro, sin realizar ninguna modificación importante en su destino final.

- Por imperativo de disposiciones legales, la reconstrucción se realice en un emplazamiento distinto.

- El tomador no haya renunciado a la revalorización automática de capitales asegura- dos y de la prima.

* A valor real:

- Si no se reconstruye.

- El CONTINENTE

* Los muebles y objetos de uso doméstico y personal, a valor de reposición a nuevo. En caso de no existir en el mercado, se tomarán como base de valoración otros objetos de similares características y rendimiento a los siniestrados.

* Los aparatos de imagen, sonido, ordenadores personales y sus accesorios, a valor real, cuando su antigüedad sea superior a tres años.

* La moneda de curso legal, por su valor nominal.

* Los objetos de especial valor y joyas serán valorados por el importe real y verdadero en el momento anterior al siniestro.

- El continente y/o contenido a valor real si hubiere renunciado a la revalorización automática de capitales asegurados y de la prima.

- Las lunas, cristales, espejos, mármoles, granitos, placas vitrocerámicas y loza sanitaria, serán valoradas por el importe de reposición incluidos los gastos de instalación.

- Los vehículos a motor si el siniestro es parcial se repararán sin tener en cuenta la depreciación del mismo. Si es total, se indemnizará por el valor real del vehículo. En caso de que el coste de la reparación fuere igual o superior al 80% del valor del vehículo inmediatamente antes de ocurrir el siniestro, podremos considerarlo como siniestro total.

DESACUERDO EN LA TASACIÓN:

- Si no se lograse un acuerdo sobre el importe y la forma de la indemnización, en el plazo de cuarenta días a partir de la recepción de la declaración del siniestro, cada parte designará un perito, debiendo constar por escrito la aceptación de éstos.

Si alguno de los dos no hubiera hecho esta designación, el otro podrá requerirle en este sentido, debiendo nombrar el perito correspondiente dentro de los ocho días siguientes al requerimiento, a falta de lo cual se entenderá que acepta el dictamen del perito de la otra parte, quedando vinculado por el mismo.

- Si los dos peritos así nombrados llegan a un acuerdo, se reflejará en un acta conjunta en la que se harán constar las causas del siniestro, la valoración de los daños, las demás circunstancias que influyan en la determinación de la indemnización según las circunstancias que influyan en la determinación de la indemnización, según la naturaleza del seguro de que se trate, y la propuesta del importe líquido de la indemnización.

- Cuando no haya acuerdo entre los peritos, ambas partes designarán un tercer perito de conformidad. De no existir esta, se podrá promover expediente en la forma prevista en la Ley de la Jurisdicción Voluntaria o en la legislación notarial. En estos casos, el dictamen pericial se emitirá en el plazo señalado por las partes o, en su defecto, en el de treinta días a partir de la aceptación de su nombramiento por el perito tercero.

- El dictamen de los peritos, por unanimidad o mayoría, se notificará tanto al asegurado como al asegurador de manera inmediata y de forma indubitada, y vinculará a los dos salvo que intervenga una impugnación judicial:

* Dentro del plazo de 180 días a partir de la fecha de dicha notificación, si el asegurado es quien efectúe dicha impugnación.

* Dentro del plazo de 30 días, si es el asegurador.

Si no se impugna en estos plazos el dictamen será inatacable.

GASTOS DE PERITOS: Cada parte satisfará los honorarios de su perito y la mitad de los del perito tercero, así como los demás gastos, incluso los de desescombro, que ocasione la tasación pericial. No obstante, si alguna de las partes hubiera hecho necesaria la peritación por haber mantenido una valoración del daño manifiestamente desproporcionada será el único responsable de dichos gastos.

12. LA DETERMINACIÓN DE LA INDEMNIZACIÓN

- La suma asegurada constituye el límite máximo de la indemnización que el asegurador pagará, por todos los conceptos, en caso de siniestro.

- El seguro no puede ser objeto de enriquecimiento injusto para el asegurado.

- Para la determinación del daño se atenderá al valor del interés asegurado en el momento inmediatamente anterior a la ocurrencia del siniestro.

Una vez efectuada la tasación de los daños, la indemnización se determinará en base a lo siguiente:

- Si en el momento del siniestro la suma asegurada es inferior al valor del interés asegurado, el asegurador indemnizará el daño en la misma proporción en la que la suma asegurada cubre el interés asegurado.

Esta regla proporcional no será de aplicación:

1) Cuando la diferencia entre el valor de interés asegurado y la suma asegurada no excede del 15%.

2) Cuando el importe de los siniestros sea inferior a 600 euros.

En el caso de que exista en esta póliza eventos garantizados a primer riesgo, el asegurador indemnizará los mismos sin tener en cuenta la regla proporcional establecida en el párrafo anterior.

- Si, en cambio, la suma asegurada es superior al valor del interés, la indemnización no podrá nunca superar el daño efectivamente causado.

- Si existen varios seguros sobre los mismos objetos y riesgos, declarados conforme a lo estipulado en la cláusula sobre la TRAMITACIÓN DEL SINIESTRO, el asegurador contribuirá a la indemnización y a los gastos de tasación a prorrata de la suma que asegure.

Si por dolo se hubiera omitido esta declaración, el asegurador no estará obligado al pago de la indemnización.

13. EL PAGO DE LA INDEMNIZACIÓN

- Si la fijación de los daños se hizo por arreglo amistoso, el asegurador debe pagar la suma convenida en el plazo máximo de cinco días desde que se firmó el acuerdo.

- Si la fijación de los daños se hizo por acuerdo de los peritos, el asegurador debe abonar el importe señalado por aquéllos en un plazo de cinco días a partir del momento en que ambas partes hayan consentido y aceptado el acuerdo pericial, con lo que el mismo devendrá inatacable.

- En cualquier supuesto el asegurador deberá efectuar dentro de los cuarenta días, a partir de la recepción de la declaración del siniestro el pago del importe mínimo de lo que el asegurador pueda deber, según las circunstancias por el asegurador conocidas.

- Si el dictamen de los peritos fuese impugnado, le abonaremos, dentro de los cinco días siguientes a la impugnación, el importe mínimo anteriormente indicado.

- Si en el plazo de tres meses desde la producción del siniestro no hubiéramos satisfecho la indemnización, mediante pago o por la reparación o reposición del objeto siniestrado, o si en el plazo de cuarenta días, desde la recepción del siniestro, no hubiéramos procedido al pago del importe mínimo, por causa no justificada o que fuere imputable al asegurador, la indemnización o el importe mínimo se incrementará con el pago de un interés anual igual al del interés legal del dinero vigente en el momento en que se devengue, incrementado en el 50%.

No obstante, transcurridos dos años desde la producción del siniestro, el interés anual no podrá ser inferior al 20%.

Podremos exigirle, antes de proceder al pago de la indemnización, certificación acreditativa de la libertad de cargas de los bienes siniestrados.

14. NORMAS DE TIPO GENERAL COMUNICACIONES:

- Las comunicaciones que el tomador deba hacer al asegurador se realizarán por escrito y en el domicilio social señalado en la póliza.

- Las comunicaciones que el asegurador deba hacer al tomador, se realizarán en su domicilio que aparece recogido en la póliza, salvo que haya notificado a la aseguradora el cambio del mismo.

- Las comunicaciones que el tomador o el asegurado efectúe con el agente de seguros, que medie o haya mediado en el contrato, surtirán los mismos efectos que si se hubieren realizado directamente ante la aseguradora. Asimismo, el pago de los recibos de prima realizados al referido agente de seguros se entenderan realizados al asegurador.

- Las comunicaciones que efectúe en nombre del tomador un corredor de seguros surtirán los mismos efectos que si las realizara el mismo tomador. El pago de la prima efectuado por el tomador al corredor de seguros no se entenderá realizado al asegurador, salvo que, a cambio, el corredor le entregue el recibo de prima emitido por el asegurador.

SOLUCIÓN DE CONFLICTOS ENTRE LAS PARTES:

- Las partes podrán someter conjuntamente sus discrepancias al juicio de árbitros según la legislación vigente.

PRESCRIPCIÓN: las acciones derivadas del contrato prescriben a los dos años a contar desde el día en que pudieron ejercitarse.

SUBROGACIÓN:

- Una vez pagada la indemnización, y sin que haya necesidad de ninguna otra cesión, traslado, título o mandato, quedamos subrogados en todos los derechos, recursos y acciones que al asegurado le correspondan contra todos los autores o responsables del siniestro, y aun contra otros aseguradores, si los hubiere, hasta el límite de la indemnización, siendo el asegurado responsable de los perjuicios que con actos u omisiones pueda causar al asegurador en su derecho de subrogación. El asegurador no puede ejercitar en perjuicio del asegurado en que el asegurador se haya subrogado.

- El asegurador no tendrá derecho a la subrogación contra ninguna de las personas cuyos actos u omisiones dé origen a la responsabilidad del asegurado, ni contra el causante del siniestro que sea, respecto del asegurado, pariente en línea directa colateral dentro del tercer grado civil de consanguinidad, padre adoptivo o hijo adoptivo que convivan con el asegurado, salvo que la responsabilidad del siniestro provenga de una actuación dolosa de ellos.

- En caso de concurrir el asegurado y el asegurador frente a tercero responsable, el recobro obtenido se repartirá entre ambos en proporción a su respectivo interés.

EXTINCIÓN Y NULIDAD DEL CONTRATO:

- Si durante la vigencia del seguro se produjera la desaparición del interés o del bien asegurado, desde ese momento el contrato quedará extinguido y el asegurador tendrá derecho a hacer suya la parte de prima no consumida.

- El contrato será nulo salvo en los casos previstos por la Ley, si en el momento de su conclusión no existía el riesgo, había ocurrido el siniestro, o no existiese interés a la indemnización del daño.

15. REVALORIZACIÓN AUTOMÁTICA ANUAL DE LOS CAPITALES ASEGURADOS DE LA PRIMA

Salvo pacto en contrario y con el fin de que el valor del interés asegurado declarado por el tomador y/o asegurado y la suma asegurada que le cubre, mantengan en lo posible la adecuación durante la vigencia del contrato, queda convenido que los capitales asegurados se modificarán automáticamente de la forma siguiente:

- Se aplicará el valor del interés declarado y la prima anual de origen, en la misma proporción, la variación que experimente el índice ponderado de precios al consumo, establecido y publicado por el Instituto Nacional de Estadística u organismo oficial que le pueda sustituir, y cuyo índice de base, considerado como cien en la fecha de efecto, se indica en las condiciones particulares de la póliza, o en último apéndice de declaración de valor asegurado, en su caso.

- Los efectos de la revalorización son de aplicación únicamente para las sumas aseguradas, y, en consecuencia, no son de aplicación a las cantidades fijas establecidas como límite de cobertura ni a los límites porcentuales.

El tomador podrá en los términos señalados en las condiciones generales de la póliza, solicitar la modificación de los capitales asegurados, así como renunciar a los beneficios de esta garantía en cada vencimiento anual, mediante carta certificada dirigida al asegurador con dos meses de antelación al citado vencimiento.

COMPENSACIÓN DE CAPITALES: si en el momento del siniestro existiese un exceso de la suma asegurada en CONTINENTE o en CONTENIDO, tal exceso podrá aplicarse al concepto que resultase insuficientemente asegurado, siempre que la prima resultante no exceda de la satisfecha en la anualidad en curso.

16. CLÁUSULA DE INDEMNIZACIÓN DE LAS PÉRDIDAS DERIVADAS DE ACONTECIMIENTOS EXTRAORDINARIOS ACAECIDOS EN ESPAÑA

De conformidad con lo establecido en el texto refundido del Estatuto legal del Consorcio de Compensación de Seguros, aprobado por el Real Decreto Legislativo 7/2004, de 29 de octubre, y modificado por la Ley 12/2006, de 16 de mayo, el tomador de un contrato de seguro de los que deben obligatoriamente incorporar recargo a favor de la citada entidad pública empresarial tiene la facultad de convenir la cobertura de los riesgos extraordinarios con cualquier entidad aseguradora que reúna las condiciones exigidas por la legislación vigente.

Las indemnizaciones derivadas de siniestros producidos por acontecimientos extraordinarios acaecidos en España y que afecten a riesgos en ella situados serán pagadas por el Consorcio de Compensación de Seguros cuando el tomador hubiese satisfecho los correspondientes recargos a su favor y se produjera alguna de las siguientes situaciones:

a) Que el riesgo extraordinario cubierto por el Consorcio de Compensación de Seguros no esté amparado por la póliza de seguro contratada con la entidad aseguradora.

b) Que, aun estando amparado por dicha póliza de seguro, las obligaciones de la entidad aseguradora no pudieran ser cumplidas por haber sido declarada judicialmente en concurso o por estar sujeta a un procedimiento de liquidación intervenida o asumida por el Consorcio de Compensación de Seguros.

El Consorcio de Compensación de Seguros ajustará su actuación a lo dispuesto en el mencionado Estatuto legal, en la Ley 50/1980, de 8 de octubre, de Contrato de Seguro, en el Reglamento del seguro de riesgos extraordinarios, aprobado por el Real Decreto 300/2004, de 20 de febrero, y en las disposiciones complementarias.

Resumen de las normas legales

1. Acontecimientos extraordinarios cubiertos

a) Los siguientes fenómenos de la naturaleza: terremotos y maremotos, inundaciones extraordinarias (incluyendo los embates de mar), erupciones volcánicas, tempestad ciclónica atípica (incluyendo los vientos extraordinarios de rachas superiores a 135 km/h y los tornados) y caídas de meteoritos.

b) Los ocasionados violentamente como consecuencia de terrorismo, rebelión, sedición, motín y tumulto popular.

c) Hechos o actuaciones de las Fuerzas Armadas o de las Fuerzas y Cuerpos de Seguridad en tiempo de paz.

2. Riesgos excluidos

a) Los que no den lugar a indemnización según la Ley de Contrato de Seguro.

b) Los ocasionados en bienes asegurados por contrato de seguro distinto a aquellos en que es obligatorio el recargo a favor del Consorcio de Compensación de Seguros.

c) Los debidos a vicio o defecto propio de la cosa asegurada, o a su manifiesta falta de mantenimiento.

d) Los producidos por conflictos armados, aunque no haya precedido la declaración oficial de guerra.

e) Los derivados de la energía nuclear, sin perjuicio de lo establecido en la Ley 25/1964, de 29 de abril, sobre energía nuclear. No obstante lo anterior, sí se entenderán incluidos todos los daños directos ocasionados en una instalación nuclear asegurada, cuando sean consecuencia de un acontecimiento extraordinario que afecte a la propia instalación.

f) Los debidos a la mera acción del tiempo, y en el caso de bienes total o parcialmente sumergidos de forma permanente, los imputables a la mera acción del oleaje o corrientes ordinarios.

g) Los producidos por fenómenos de la naturaleza distintos a los señalados en el artículo 1 del Reglamento del seguro de riesgos extraordinarios, y en particular, los producidos por elevación del nivel freático, movimiento de laderas, deslizamiento o asentamiento de terrenos, desprendimiento de rocas y fenómenos similares, salvo que éstos fueran ocasionados manifiestamente por la acción del agua de lluvia que, a su vez, hubiera provocado en la zona una situación de inundación extraordinaria y se produjeran con carácter simultáneo a dicha inundación.

h) Los causados por actuaciones tumultuarias producidas en el curso de reuniones y manifestaciones llevadas a cabo conforme a lo dispuesto en la Ley Orgánica 9/1983, de 15 de julio, reguladora del derecho de reunión, así como durante el transcurso de huelgas legales, salvo que las citadas actuaciones pudieran ser calificadas como acontecimientos extraordinarios conforme al artículo 1 del Reglamento del seguro de riesgos extraordinarios.

i) Los causados por mala fe del asegurado.

j) Los derivados de siniestros cuya ocurrencia haya tenido lugar en el plazo de carencia establecido en el artículo 8 del Reglamento del seguro de riesgos extraordinarios.

k) Los correspondientes a siniestros producidos antes del pago de la primera prima o cuando, de conformidad con lo establecido en la Ley de Contrato de Seguro, la cobertura del Consorcio de Compensación de Seguros se halle suspendida o el seguro quede extinguido por falta de pago de las primas.

l) Los indirectos o pérdidas derivadas de daños directos o indirectos, distintos de la pérdida de beneficios delimitada en el Reglamento del seguro de riesgos extraordinarios. En particular, no quedan comprendidos en esta cobertura los daños o pérdidas sufridas como consecuencia de corte o alteración en el suministro exterior de energía eléctrica, gases combustibles, fuel-oil, gas-oil, u otros fluidos, ni cualesquiera otros daños o pérdidas indirectas distintas de las citadas en el párrafo anterior, aunque estas alteraciones se deriven de una causa incluida en la cobertura de riesgos extraordinarios.

m) Los siniestros que por su magnitud y gravedad sean calificados por el Gobierno de la Nación como de «catástrofe o calamidad nacional».

3. Franquicia

En el caso de daños directos (excepto automóviles y viviendas y sus comunidades), la franquicia a cargo del asegurado será de un 7 por ciento de la cuantía de los daños indemnizables producidos por el siniestro.

En el caso de la cobertura de pérdida de beneficios, la franquicia a cargo del asegurado será la prevista en la póliza para pérdida de beneficios en siniestros ordinarios.

4. Extensión de la cobertura

La cobertura de los riesgos extraordinarios alcanzará a los mismos bienes y sumas aseguradas que se hayan establecido en la póliza a efectos de los riesgos ordinarios. No obstante, en las pólizas que cubran daños propios a los vehículos a motor, el Consorcio garantiza la totalidad del interés asegurable aunque la póliza sólo lo haga parcialmente.

Procedimiento de actuación en caso de siniestro indemnizable por el consorcio de compensación de seguros

En caso de siniestro, el asegurado, tomador, beneficiario, o sus respectivos representantes legales, directamente o a través de la entidad aseguradora o del mediador de seguros, deberá comunicar, dentro del plazo de siete días de haberlo conocido, la ocurrencia del siniestro, en la delegación regional del Consorcio que corresponda, según el lugar donde se produjo el siniestro. La comunicación se formulará en el modelo establecido al efecto, que está disponible en la página «web» del Consorcio (www.consorseguros.es), o en las oficinas de éste o de la entidad aseguradora, al que deberá adjuntarse la documentación que, según la naturaleza de los daños, se requiera.

Asimismo, se deberán conservar restos y vestigios del siniestro para la actuación pericial y, en caso de imposibilidad absoluta, presentar documentación probatoria de los daños, tales como fotografías, actas notariales, vídeos o certificados oficiales. Igualmente, se conservarán las facturas correspondientes a los bienes siniestrados cuya destrucción no pudiera demorarse.

Se deberán adoptar cuantas medidas sean necesarias para aminorar los daños.

La valoración de las pérdidas derivadas de los acontecimientos extraordinarios se realizará por el Consorcio de Compensación de Seguros, sin que éste quede vinculado por las valoraciones que, en su caso, hubiese realizado la entidad aseguradora que cubriese los riesgos ordinarios.

Para aclarar cualquier duda que pudiera surgir sobre el procedimiento a seguir, el Consorcio de Compensación de Seguros dispone del siguiente teléfono de atención al asegurado: 902 222 665.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

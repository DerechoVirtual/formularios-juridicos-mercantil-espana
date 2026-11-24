---
name: contrato-servicios-jardineria-mer-0564
description: "Contrato de servicios de jardinería. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicios de jardinería

> Formulario **MER-0564** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicios de jardinería» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicios de jardinería” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-servicios-jardineria-mer-0564`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (11 veces)
- [ ] IMPORTE (7 veces)
- [ ] MES (6 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DÍA
- [ ] OBJETO DEL CONTRATO
- [ ] OTROS DATOS

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

En [LOCALIDAD], a [DÍA] día de [Nº] mes de [MES] año

REUNIDOS

De una parte:

D, mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D D, mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

[ELEGIR UNA OPCIÓN: INTERVIENEN / Si intervienen en nombre y representación de alguien / Si intervienen en su propio nombre y derecho]

EXPONEN

Que LA EMPRESA se dedica habitualmente a la prestación de servicios de jardinería.

Que LA COMITENTE precisa de los servicios de LA EMPRESA para [OBJETO DEL CONTRATO].

Que ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

OBJETO

I.1Mantenimiento de cesped

Que LA COMITENTE contrata los servicios profesionales de LA EMPRESA en su calidad de profesional de la actividad de jardinería

LA EMPRESA se compromete a realizar los servicios siguientes:

A. Siega, rebordeado y poda

LA EMPRESA segará el césped de acuerdo a la necesidad en concordancia con el crecimiento por la estación. No mas de 1/3 del follaje podrá ser cortado en cada siega. La altura del corte deberá estar en concordancia con el tipo y variedad de hierba.

Las hojas cortadas se dejarán sobre el césped siempre que estas no sean visibles a las [Nº] horas después de la siega. De otra manera, los hojas cortadas deberán ser colectadas y recogidas por LA EMPRESA.

LA EMPRESA deberá limpiar todas las hojas cortadas de las aceras, bordes y vías inmediatamente después de segadas o rebordeadas. Las hojas cortadas no se pueden barrer, soplar o ser echadas de ninguna manera en los drenajes. Los aros alrededor de las plantas y árboles, las aceras, cercas, entradas de garajes, áreas de parqueo y cualquier otra área rodeada de hierba debe ser rebordeada cada dos siegas. El césped alrededor de las cabezas de riego debe ser recortado o tratado con un herbicida no-selectivo de manera que no interfiera con la salida del agua.

B. Fertilización:

LA EMPRESA garantizará que todas las áreas de césped serán fertilizadas dos veces al año, después del rebrote de primavera y luego al final de octubre, con el tipo y cantidades de fertilizante apropiadas.

C. Control de plagas:

LA EMPRESA inspeccionará las áreas de césped en cada visita para encontrar indicios de problemas de plagas y avisará a LA COMITENTE o su representante de cada problema encontrado.

Si se confirma que un problema requiere tratamiento, los pesticidas se aplicarán según la necesidad, solo en las manchas básicas que requieren tratamiento, y siempre que sea posible, usando el pesticida efectivo menos tóxico. Todos los servicios de control de plagas son en adición a los cargos básicos del contrato. El monto del cargo será por el trabajo ejecutado basado en el costo de los materiales y la mano de obra. El costo debe ser acordado entre LA COMITENTE y LA EMPRESA antes de que el referido servicio sea realizado.

I.2Matenimiento a los Jardines: Árboles, Palmas, Arbustos y Canteros

A. Fertilizacion:

LA EMPRESA garantizará que los arbustos ornamentales Y árboles con menos de [Nº] años de plantados deben ser fertilizados [Nº] veces al año. Las aplicaciones se harán durante los meses de [MES], [MES], y [MES] Los arbustos y árboles con mas de [Nº] años en el jardín serán fertilizados [Nº] veces al año en [MES], y

B. Control de plagas:

LA EMPRESA deberá controlar los insectos, enfermedades, y malas hierbas. Esto incluirá el chequeo frecuente y el tratamiento de las manchas que sean necesarias usando los métodos menos tóxicos.

C. Poda:

Los arbustos de flores deben ser podados con utensilios manuales de acuerdo a la necesidad, para proveerlo de una forma irregular, rellena y florecida. Los arbustos sembrados para ser podados con forma deben ser podados según la necesidad para proveerlos de una forma regular y rellena.

La poda de los árboles se hará [Nº] vez al año y estará limitada a las ramas por encima de los 6 metros de altura así como las ramas decadentes. La poda de las palmeras se limitara a las hojas secas y decadentes. Las hojas verdes de las palmeras no serán cortadas.

Todos los restos resultado de las podas, deberán ser recogidos por LA EMPRESA sin cargo adicional A LA COMITENTE.

Ningún árbol que esté debajo de las líneas utilitarias será podado. Las ramas de los árboles, arbustos y hojas de las palmeras deben ser podadas exactamente en el collar.

I.3Cubierta protectora del terreno:

Todas las áreas del terreno cubiertas con fragmentos deben ser reacolchonadas una vez al año durante los meses de invierno. El colchón de fragmentos debe ser establecido con un espesor de [Nº] centímetros.

I.4Flores anuales:

El reemplazo de las plantas anuales existentes se hará [Nº] veces por año en el mes de [MES]

I.5Sistemas de riego:

LA EMPRESA inspeccionará y probará todos los componentes y zonas de riego del sistema mensualmente y reestablecerá los tiempos por zonas de acuerdo a los cambios de evaporación de la estación. Los ajustes menores y reparaciones tales como la limpieza o cambio de las cabezas [OTROS DATOS], la limpieza de filtros, las pequeñas fugas de agua y los ajustes menores de los temporizadores deben ser hechos por LA EMPRESA, las piezas necesarias serán pagadas por LA COMITENTE.

PRECIO

El precio de los servicios descritos en la cláusula primera se concreta en la cantidad de [IMPORTE] euros (€) más el Impuesto sobre el Valor Añadido correspondiente, esto es, [IMPORTE] euros (€) adicionales. El precio total de la operación asciende a la cantidad [IMPORTE] euros (€).

El precio incluye los gastos de desplazamiento que en su caso deba efectuar LA EMPRESA a las oficinas de LA COMITENTE.

[ELEGIR UNA OPCIÓN: Forma de pago / Pagos periódicos / Opción 3.1:Pagos periódicos / Pago único / Opción 3.2:Pago único]

PAGO A TERCERO

El precio total de la operación asciende a la cantidad [IMPORTE] euros (€), de los cuales en este acto LA COMITENTE entrega a LA EMPRESA [IMPORTE] euros ( €). Los restantes [IMPORTE] euros ( €) las retendrá LA COMITENTE en su poder para satisfacer con ella la deuda de [IMPORTE] euros ( €) por orden de LA EMPRESA, sin que por ello asuma responsabilidad personal alguna

RESPONSABILIDADES

LA EMPRESA es responsable por:

1. Cualquier daño que realice a la propiedad del Cliente durante la operación de sus equipos en la realización del contrato.

2. Cumplir con todas las leyes pertinentes a la protección de especies de plantas.

3. Daños a plantas debido a prácticas de horticultura impropias.

4. Daños ocasionados por la instalación impropia de los componentes de reemplazo de los sistemas de riego.

5. Daños a organismos ajenos a los previstos en la aplicación de pesticidas.

LA EMPRESA no es responsable por:

1. Muerte o declinación de plantas debido a la impropia selección, emplazamiento, plantado, o mantenimiento después del tiempo de este contrato.

2. Daños producidos por componentes impropios del sistema de irrigación no escogidos por él durante el tiempo de ejecución de este contrato

3. Cables, alambres o líneas de las cabezas de riego expuestas y que normalmente deben estar soterradas debajo de la superficie del césped.

4. Muerte o daños al césped o plantas de jardines por excesiva irrigación o falta de agua por componentes del sistema de irrigación operando impropiamente y que hayan sido reportados a LA COMITENTE, o restricciones de riego impuestas por las autoridades civiles.

5. Daños causados por cualquier elemento escondido en el terreno y que no esté claramente marcado o protegido.

6. Daños debido al vandalismo.

AUTORIZACIÓN PARA SUBCONTRATACIÓN

La prestación de servicios deberá ser realizado por LA EMPRESA con los medios personales y materiales integrantes de su propia organización empresarial, utilizando vehículos de los que disponga en tal concepto.

No obstante, cuando precise de la colaboración de otro profesional, no quedará desvirtuada su condición de EMPRESA único frente a LA COMITENTE.

En todo caso, las personas a quienes subcontrate habrán de reunir las condiciones y preparación adecuadas para la prestación de servicios encomendada.

RESOLUCIÓN DEL CONTRATO

El Contrato podrá resolverse por las siguientes causas:

1.Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.

2.Por acuerdo de las Partes por escrito.

3.La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

GASTOS E IMPUESTOS

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sumisión a tribunales / Opción 9.1: Sumisión a tribunales / Sumisión a arbitraje / Opción 9.2:Sumisión a arbitraje]

NOTIFICACIONES

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

GENERALIDADES

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE PRESTACIÓN DE SERVICIOS DE JARDINERÍA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. Don [NOMBRE Y APELLIDOS]

(La EMPRESA)

Fdo. Don [NOMBRE Y APELLIDOS]

(La COMITENTE)

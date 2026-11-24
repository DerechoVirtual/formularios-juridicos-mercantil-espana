---
name: seguro-vida-temporal-fallecimiento-garantias-mer-0695
description: "Seguro de vida temporal de fallecimiento con garantías complementarias. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Seguro de vida temporal de fallecimiento con garantías complementarias

> Formulario **MER-0695** del plugin **Seguros: pólizas, coberturas y reclamaciones** (`formularios-seguros`) · Mercantil › Seguros · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Seguro de vida temporal de fallecimiento con garantías complementarias» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Seguro de vida temporal de fallecimiento con garantías complementarias” para mi caso». También puedes invocarla directamente con `/formularios-seguros:seguro-vida-temporal-fallecimiento-garantias-mer-0695`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguros:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguros: pólizas, coberturas y reclamaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (7 veces)
- [ ] IMPORTE (6 veces)
- [ ] AÑO
- [ ] MES
- [ ] Nº DE ANEXO

## Normas que cita el formulario

- art. 98 LCS

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

SEGURO DE VIDA TEMPORAL PARA CASO DE MUERTE CON GARANTÍAS COMPLEMENTARIAS

CONDICIONES PARTICULARES

Plan del seguro:

Modalidad: Seguro de vida temporal mixto de muerte y supervivencia

(indicar la concreta denominación comercial de la modalidad)

Duración: años desde la fecha de inicio de la cobertura Fecha de inicio de la cobertura

/ [MES] / [AÑO]

Importe total de la prima única (si la forma de vencimiento es anual): [IMPORTE] €

Importe total de la primera prima y de las primas sucesivas: [IMPORTE] €

Forma de vencimiento:□ mensual□ trimestral□ semestral□ anual

Garantías contratadas:

Garantía principal por fallecimiento por cualquier causa Primera persona asegurada [IMPORTE] € Segunda persona asegurada [IMPORTE] €

Forma de percepción: □ Montante único □ Rentas periódicas Porcentaje de revalorización de las rentas periódicas: % Garantías complementarias (optativas)

% (a elegir el 25%, 50%, 75% o 100% de la garantía principal)

Capital adicional por incapacidad permanente absoluta o total causada por infarto de miocardio

Primera persona asegurada

Segunda persona asegurada□ Sí

□ Sí %

%

Capital adicional por incapacidad permanente absoluta

Primera persona asegurada

Segunda persona asegurada□ Sí

□ Sí %

%

Capital adicional por incapacidad permanente total

Primera persona asegurada□ Sí %

Segunda persona asegurada□ Sí %

Indemnización diaria por hospitalización

Primera persona asegurada

Segunda persona asegurada□ Sí

□ Sí, [IMPORTE] € día [IMPORTE], € día

Cobertura de gastos y servicios de sepelio Primera persona asegurada □ Sí

Segunda persona asegurada □ Sí

CONDICIONES GENERALES

ARTÍCULO 1: SUJETO Y OBJETO DEL SEGURO: GARANTÍAS ESTIPULADAS.

Conforme a las condiciones estipuladas en la presente póliza, la garantía principal objeto de este contrato consiste en la obligación del Asegurador de pagar al Beneficiario o Beneficiarios designados por el Tomador del seguro el capital garantizado en caso de fallecimiento del Asegurado durante el período de cobertura de este seguro.

Conforme a las condiciones estipuladas en la presente póliza, las garantías complementarias de este seguro consisten en la obligación del Asegurador de pagar al Beneficiario o Beneficiarios designados por el Tomador del seguro las cantidades porcentuales calculadas según lo dispuesto en las condiciones particulares de la póliza sobre el capital garantizado en caso de fallecimiento del Asegurado para los supuestos de hospitalización, de infarto de miocardio, o de incapacidad, así como la cobertura de los gastos y servicios de sepelio, en función de las coberturas estipuladas en las reiteradas condiciones particulares, y de la delimitación de tales coberturas que resulta de las presentes condiciones generales, en particular el artículo siguiente.

Tanto la garantía principal como las garantías complementarias se extienden sobre la persona o personas del Asegurado o Asegurados, conforme a su consignación en las condiciones particulares de la presente póliza.

ARTÍCULO 2: DEFINICIONES.

En el presente contrato se entiende por:

- Asegurador: la Entidad Aseguradora, que asume la cobertura de los riesgos contractualmente pactados.

- Asegurado: la persona o personas físicas sobre las cuales se establece el seguro y que figuran como tal en las condiciones particulares.

- Tomador del seguro: la persona física o jurídica que, junto con el Asegurador, sus- cribe el contrato y al que corresponden los derechos y obligaciones que de él se derivan, salvo los que por su naturaleza deban de ser cumplidos por el Asegurado.

- Beneficiario: la persona o personas designadas por el Tomador para percibir las prestaciones aseguradas.

- Póliza: el documento que contiene las condiciones reguladoras del seguro, integrado por las presentes condiciones generales, las especiales, las particulares que individualizan el riesgo, la descripción de los servicios y los suplementos o apéndices que se emitan a la misma para complementarla o modificarla.

- Bases técnicas: conjunto de tablas de valores, de mortalidad y de morbilidad, y de directrices de gestión y de cálculo utilizados por el Asegurador para los cálculos actuariales propios de este seguro, y en particular para la determinación concreta y revalorización de los emolumentos y cuantías de las prestaciones a satisfacer por ambas partes.

- Prima: el precio del seguro. El recibo de la prima contendrá, además, los recargos e impuestos legalmente repercutibles.

- Prima de riesgo: Importe de la prima del seguro que se destina exclusivamente a la cobertura del riesgo asegurado, y cuya cuantía se determina deduciendo del importe total de la prima los recargos destinados a cubrir los gastos de gestión del Asegurador, establecidos conforme a lo previsto en las bases técnicas del seguro.

- Suma asegurada o capital garantizado: el límite máximo de prestación del Asegurador en caso de siniestro.

- Garantías cubiertas: las prestaciones de carácter principal o de carácter complementario objeto del seguro, a las que se obliga el Asegurador en caso de siniestro, según hayan sido contratadas por el Tomador del seguro en las condiciones particulares de la póliza y con los porcentajes del capital garantizado consignados en las mismas.

- Valor de la póliza: Fondo constituido por las aportaciones del Tomador del seguro a través de las primas, revalorizadas conforme a los tipos de interés técnico trimestral establecidos en las bases técnicas de este seguro, y que nunca podrá ser negativo, y una vez deducidos los gastos y penalizaciones que sean de aplicación conforme a dichas bases técnicas.

- Tipo de interés técnico variable: el que utiliza el Asegurador para actualizar el valor de la póliza al inicio de cada trimestre natural, que figura en las bases técnicas y del que se informa al Tomador del seguro conforme a las condiciones establecidas en las presentes condiciones generales.

- Crecimiento aritmético: incremento anual de una cantidad en un tanto por ciento fijo de su valor en el momento de suscripción del seguro.

- Crecimiento geométrico: incremento anual de una cantidad en un tanto por ciento fijo de su valor al inicio de la anualidad inmediatamente anterior.

- Siniestro: el acaecimiento de cualquier acontecimiento que dé lugar a la satisfacción por parte del Asegurador de las prestaciones contratadas por el Tomador del seguro a través de la presente póliza como garantía principal o, en su caso, como garantías complementarias, de conformidad con lo estipulado en las condiciones generales, especiales y particulares de la misma, y que incluye los hechos siguientes:

- Fallecimiento: muerte efectiva del Asegurado, en sentido médico y biológico, equipa- rada a la declaración judicial regulada en los artículos 193 y ss. del Código Civil.

- Accidente: lesión corporal derivada de una causa violenta, súbita, externa y ajena a la intencionalidad del Asegurado, que produzca incapacidad temporal o permanente o muerte, siempre que no sea objeto de alguna de las exclusiones de cobertura de este seguro establecidas en las presentes condiciones generales.

- Enfermedad grave: cualquier dolencia o lesión física o psíquica que altere la salud del Asegurado, incluido el infarto de miocardio, hasta el punto de impedirle temporalmente el normal desarrollo de sus ocupaciones o actividades habituales durante un período mínimo de tres meses, y que requiera tratamiento hospitalario o intervención clínica o quirúrgica de cirugía mayor, siempre que no generen la percepción por parte del Asegurado de una prestación por incapacidad permanente absoluta o total conforme al régimen de la Seguridad Social, y que no sean objeto de alguna de las exclusiones de cobertura de este seguro establecidas en las presentes condiciones generales.

- Infarto de miocardio: la muerte biológica de una parte del músculo del miocardio como resultado de una insuficiencia de aporte sanguíneo, y cuyo diagnóstico se basa en un historial previo de dolor precordial típico y prolongado, en cambios específicos del electrocardiograma del Asegurado (aparición de la onda «Q»), y en la elevación en sangre de los valores normales de enzimas musculares cardiacas.

- Incapacidad permanente absoluta: la situación física o psíquica del Asegurado de carácter permanente, como consecuencia de enfermedad o accidente, determinante de su ineptitud total para el ejercicio de cualquier actividad profesional.

- Incapacidad permanente total: la situación física o psíquica del Asegurado de carácter permanente, como consecuencia de enfermedad o accidente, determinante de su ineptitud total para el ejercicio de su actividad profesional habitual.

- Hospitalización: el ingreso del Asegurado como paciente de un hospital durante un período mínimo superior a 24 horas.

ARTÍCULO 3: BASES DEL SEGURO.

El Asegurador asume la cobertura del riesgo y la satisfacción de las prestaciones estipuladas en la presente póliza en las condiciones y dentro de los límites establecidos en la misma cuando se produzca el siniestro tal y como aparece delimitado en el artículo anterior, siempre que no sea objeto de alguna de las exclusiones de cobertura de este seguro establecidas en las presentes condiciones generales.

El Tomador del seguro y el Asegurado tienen el deber de declarar al Asegurador, de acuerdo con los documentos utilizados para la delimitación del riesgo durante la tramitación previa a la suscripción de la póliza, en particular los cuestionarios médicos, y, en su caso, con los resultados de las pruebas y reconocimientos médicos a los que debió someterse el Asegurado a instancia del Asegurador. El Tomador del seguro y el Asegurado quedarán exonerados de tal deber si el Asegurador no les presenta tales documentos ni somete al Asegurado a prueba o reconocimiento alguno o cuando, aun sometiéndoselo, se trate de circunstancias que puedan influir en la valoración del riesgo y que no estén comprendidas en tales documentos, pruebas o reconocimientos, excepto cuanto el Tomador del seguro o el Asegurado tengan conocimiento de la influencia de tales circunstancias en la valoración del riesgo por otros medios.

El seguro se emite sobre la base de las declaraciones del Tomador del seguro y del Asegurado contenidas en los documentos utilizados para la delimitación del riesgo durante la tramitación previa a la suscripción de la póliza, en particular los cuestionarios médicos, y, en su caso, los resultados de las pruebas y reconocimientos médicos a los que debió someterse el Asegurado a instancia del Asegurador. Tales declaraciones han motivado la aceptación del riesgo por el Asegurador así como la fijación de la prima, por lo que constituyen un todo unitario junto con la presente póliza como base de este seguro.

El contrato se perfecciona por el consentimiento manifestado por las partes contratantes mediante la suscripción de la póliza.

Si el contenido de la póliza difiere en todo o en partes de las cláusulas efectivamente acordadas entre los contratantes o de la proposición inicial del Asegurador, el Tomador del seguro podrá reclamar al Asegurador en el plazo de un mes a contar desde la fecha en que el Asegurador le entregue la póliza para que se lleve a cabo la oportuna subsanación de la divergencia existente. Transcurrido dicho plazo sin que se hubiere efectuado reclama- ción alguna, los contratantes deberán estar a lo dispuesto en la póliza.

ARTÍCULO 4: FACULTAD DE RESOLUCIÓN UNILATERAL DEL TOMADOR DEL SEGURO.

El Tomador del seguro tendrá la facultad libérrima de resolver el presente contrato de seguro en el plazo de treinta días naturales a contar desde la fecha en que el Asegurador le entregue la póliza o, en su caso, el documento de cobertura provisional, sin que sea necesario indicar los motivos y sin penalización alguna.

Esta facultad deberá ejercitarse por escrito firmado por el propio Tomador del seguro y presentado en el domicilio del Asegurador, o en alguna de sus delegaciones o sucursales, o bien a través del agente o corredor interviniente en el contrato conforme a las condiciones particulares de la póliza, y producirá todos sus efectos desde el mismo día de su expedición. En particular, a partir de esta fecha cesará la cobertura de los riesgos objeto del seguro por parte del Asegurador, y el Tomador del seguro tendrá derecho a la devolución de la prima que hubiese pagado, salvo la parte proporcional correspondiente al período de tiempo durante el que se hubiese mantenido la cobertura objeto del seguro. El Asegurador dispondrá para ello de un plazo de treinta días naturales a contar desde la recepción de la comunicación de resolución unilateral del tomador del seguro.

ARTÍCULO 5: EDAD DEL ASEGURADO.

Salvo pacto en contrario, expresamente consignado en las condiciones particulares de la póliza, no podrá ser Asegurado la persona que, en la fecha de suscripción del seguro, tenga menos de [Nº] años de edad, o más de [Nº] años de edad, o que en la fecha de conclusión del período de cobertura del seguro tenga más de [Nº] años de edad. A tales

efectos, la referida cobertura cesará de forma automática a las 24,00 horas del día 31 de diciembre del año dentro del cual el Asegurado cumpla [Nº] años de edad.

En el supuesto de indicación inexacta de la edad del Asegurado, el Asegurador sólo podrá impugnar este contrato si la verdadera edad del Asegurado excediese por defecto o por exceso en la fecha de suscripción del seguro los límites de admisión mínimo y máximo establecidos en el párrafo precedente.

En cualesquiera otros casos, si como consecuencia de una declaración inexacta de la edad del Asegurado, la prima pagada es inferior a la que correspondería pagar con arreglo a las bases técnicas, la prestación objeto de este contrato se reducirá en proporción a la prima efectivamente percibida. Si, por el contrario, la prima pagada es superior a la que debiera haberse abonado conforme a los mismos criterios, el Asegurador restituirá sin intereses el exceso en las primas de riesgo efectivamente percibidas.

A los efectos del presente seguro se considerará edad del Asegurado la que éste tuviere en la fecha de cumpleaños más próxima al día en que la póliza comienza a tener efecto y en cada aniversario de la misma.

ARTÍCULO 6: EXCLUSIONES DE LA COBERTURA DEL SEGURO.

Quedan excluidas de la cobertura del seguro con carácter general para cualesquiera de las garantías objeto del mismo, principal o complementarias, los siniestros que hayan sido debidos a alguna de las causas siguientes:

- Enfermedades, accidentes, lesiones o cualesquiera otras alteraciones o trastornos de la salud del Asegurado preexistentes a la fecha de suscripción de la póliza, que hubiesen dado síntomas evidentes e inequívocos de su existencia, o que fuesen conocidas por el Asegurado, pero que no hubiesen sido declaradas por éste al Asegurador durante la tramitación previa a tal suscripción, ni en los documentos utilizados para la delimitación del riesgo, en particular los cuestionarios médicos, ni, en su caso, en las pruebas y reconocimientos médicos, ni de ninguna otra forma.

- Siniestros causados voluntariamente por el propio Asegurado, o que le sobrevengan por un acto propio realizado con dolo o mala fe, con imprudencia temeraria, o con negligencia grave, judicialmente declarados, así como los siniestros derivados de la participación de Asegurado en hechos delictivos, duelos o riñas, siempre que no hubiese actuado en legítima defensa propia o de terceros o en salvamento o tentativa de salvamento de personas o bienes.

- Siniestros causados intencionadamente por el Beneficiario, en cuyo caso el capital garantizado se integrará en el patrimonio del Tomador del seguro. Si existieren varios Beneficiarios, conservarán sus derechos como tales los no intervinientes en el siniestro.

- Siniestros consistentes en el fallecimiento del Asegurado por suicidio durante el primer año de vigencia del contrato desde la fecha de suscripción de la póliza.

- Siniestros que sobrevengan al Asegurado por causa de alcoholismo agudo o crónico, o por el uso de drogas, estupefacientes o cualesquiera otras sustancias psicotrópicas no prescritos médicamente.

- Siniestros que sobrevengan al Asegurado como consecuencia de riesgos extraordinarios, entendiendo como tales los derivados de inundaciones extraordinarias, erupciones volcánicas, tempestades ciclónicas atípicas (incluyendo los vientos extraordinarios de rachas superiores a 135 km/h. y los tornados), caídas de cuerpos siderales y aerolitos, actos de terrorismo, rebelión, sedición, insurrección, motín y tumulto popular, conflicto armado (declarado o no, de carácter civil o internacional), y hechos o actuaciones de las Fuerzas Armadas o de las Fuerzas y Cuerpos de Seguridad en tiempo de paz.

- Siniestros que sobrevengan al Asegurado como consecuencia directa o indirecta de energía, reacción o radiación nucleares o contaminación radiactiva, salvo las producidas con ocasión de un tratamiento médico prescrito por un facultativo.

Quedan excluidas de la cobertura del seguro con carácter específico para las garantías complementarias de cualquier clase de invalidez los siniestros que hayan sido debidos a alguna de las causas siguientes:

- Los accidentes ocasionados por la conducción de motocicletas o ciclomotores por parte del Asegurado.

- Los accidentes ocasionados por la práctica de deportes considerados de alto riesgo conforme a la enumeración de los mismos contenida en el Anexo [Nº DE ANEXO] de la presente póliza.

- Los accidentes de aviación (incluidos los que sean consecuencia de efectuar descensos en paracaídas) cuando el Asegurado haya hecho del vuelo su profesión y ocupe una aeronave como integrante de su tripulación por imperativo de las funciones que se le asignen en virtud de tal integración. En todos los demás supuestos, la cobertura del seguro para las garantías complementarias de cualquier clase de invalidez requerirán que el Asegurado realice el vuelo como simple pasajero en líneas comerciales regulares, vuelos «chárter» y siempre en aparatos civiles provistos de un certificado de navegabilidad debidamente autorizado y conducidos por personas provistas de un título de piloto válido para el tipo y modelo de aparato autorizado.

- Los accidentes de navegación submarina, incluyendo los que se produzcan durante inmersiones de buceo con escafandra autónoma.

- Los accidentes producidos durante viajes de exploración.

- Los infartos de miocardio sufridos por el Asegurado no se consideran accidente a los efectos de las garantías complementarias de cualquier clase de invalidez, por lo que no son objeto de cobertura de las mismas.

Quedan excluidos de la cobertura del seguro con carácter específico para la garantía complementaria de incapacidad permanente absoluta o total causada por infarto de miocardio los siniestros sufridos por el Asegurado cuando, con anterioridad a la suscripción y firma de la póliza, hubiese sufrido ya algún infarto previo, o padeciese cualesquiera dolencias de tipo cardiovascular.

(las exclusiones de cobertura se consideran cláusulas limitativas de los derechos del Asegurado, que requieren ser especialmente destacadas en hoja separada adjunta a la póliza y ser específicamente firmadas por el Tomador del seguro y el Asegurado).

ARTÍCULO 7: MODIFICACIÓN DEL RIESGO CUBIERTO MEDIANTE EL SEGURO.

El Tomador del seguro o el Asegurado deberán declarar al Asegurador durante el curso del contrato y lo antes posible, cualesquiera variaciones y modificaciones en los datos y circunstancias declarados durante la tramitación previa a la suscripción del seguro, excepto los estrictamente médicos, a fin de que el Asegurador pueda proponer las oportunas modificaciones de sus condiciones iniciales. En particular, esta declaración deberá compren- der los cambios de residencia y de profesión del Asegurado, así como la práctica de actividades consideradas de riesgo, enumeradas en el Anexo núm. [Nº] de la presente póliza.

Si el siniestro sobreviniere antes de que existiese la citada comunicación, la prestación se reducirá proporcionalmente a la diferencia entre la prima convenida y la que hubiere resultado de haberse conocido por parte del Asegurador las nuevas circunstancias, salvo que mediase dolo o culpa grave del Tomador del seguro o el Asegurado en cuyo caso el Asegurador podrá resolver unilateralmente el contrato conforme a lo establecido en las presentes condiciones generales y quedará liberado de su obligación.

En caso de aceptar expresamente el Asegurador la agravación del riesgo, el Tomador del seguro quedará obligado al pago de la prorrata de la prima correspondiente. La cobertura de los nuevos riesgos declarados no tendrá efecto hasta las 00,00 horas del día siguiente a aquel en el que el Tomador pagó la referida prorrata.

Asimismo el Tomador del seguro o el Asegurado podrán poner en conocimiento del Asegurador cualesquiera circunstancias que disminuyan el riesgo cubierto, lo que obligará al Asegurador a reducir el importe de la prima siguiente a la del período en curso en la cuantía que corresponda.

ARTÍCULO 8: VALORES DE RESCATE.

Sin contenido.

(esta estipulación carece de sentido en los seguros de vida temporales dado que su corta duración impide que se generen reservas matemáticas y de ahí su exclusión del ámbito de aplicación de estos seguros, ex art. 98 LCS, si bien se permite en ese mismo precepto que le sean reconocidos al Tomador del seguro estos derechos mediante pacto expreso en la póliza, aunque no suele ser frecuente)

ARTÍCULO 9: DURACIÓN MÍNIMA Y MÁXIMA DEL SEGURO Y EFECTO DE LA COBERTURA.

La duración del seguro será la estipulada en las condiciones particulares de la póliza, pero nunca por un tiempo inferior a un año natural, y se entenderá automáticamente renovada por períodos de igual duración, sin perjuicio de las oportunas revalorizaciones de las primas en los términos establecidos en las presentes condiciones generales, salvo oposición expresa de cualquiera de los contratantes notificada por escrito con una antelación mínima de dos meses antes de la conclusión del período en curso. La renovación automática del seguro podrá tener lugar de la forma expresada hasta la anualidad inmediatamente anterior a aquélla en la que el Asegurado alcance los [Nº] años de edad para la garantía principal y [Nº] años de edad para las garantías complementarias.

La cobertura del seguro tomará efecto desde las 00,00 horas del primer día del mes siguiente a aquel en el que tuvo lugar la suscripción y firma de la póliza, siempre que el Tomador del seguro haya pagado la primera prima con anterioridad, y hasta las 24,00 horas del día de conclusión del período de duración del seguro establecido en tales condiciones particulares.

En caso de demora por parte del Tomador del seguro o, en su caso, del Asegurado o Asegurados en la suscripción y firma de la póliza, o del Tomador del seguro en el pago de la primera prima, o en ambos supuestos, la cobertura del seguro tomará efecto desde las 00,00 horas del primer día siguiente a aquel en el que hayan tenido lugar la suscripción y firma de la póliza o el pago de la primera prima, o desde las 00,00 horas del primer día siguiente a aquel en el que se hubieren visto satisfechos ambos requisitos, si la demora hubiese afectado simultáneamente al cumplimiento de ambos.

ARTÍCULO 10: TRAMITACIÓN DEL SINIESTRO.

Una vez producido el siniestro, el Tomador, el Asegurado o, en su caso, el Beneficia- rio, deberán comunicarlo al Asegurador a la mayor brevedad posible, en un plazo máximo de siete días naturales desde que lo hubieren conocido, así como facilitarle toda la información necesaria para su comprobación, determinación de sus causas, y valoración. En relación con las garantías complementarias de cualquier clase de invalidez y de indemnización diaria por hospitalización, el Tomador o el Asegurado deberán permitir el reconocimiento médico de este último por los facultativos que designe el Asegurador, así como levantar el secreto profesional del médico tratante de este último para informar sobre su estado de salud al Asegurador; el Asegurador se reserva asimismo la potestad de efectuar o solicitar cuantos informes, pruebas diagnósticas e informaciones resulten pertinentes para evaluar, en su caso, la situación de invalidez o el estado de salud del Asegurado o para realizar el oportuno seguimiento de los mismos.

ARTÍCULO 12: ACREDITACIÓN DE LA PRODUCCIÓN EFECTIVA DEL SINIESTRO.

Producido el siniestro, el Asegurador se obliga a satisfacer al Beneficiario o Beneficiarios del seguro las prestaciones contratadas en la presente póliza de conformidad con las mismas y con lo que se halla previsto en los párrafos siguientes.

Para el pago de las prestaciones estipuladas en el supuesto de fallecimiento del Asegurado, y de los correspondientes gastos y servicios de sepelio en caso de haberse contratado esta garantía complementaria, el Beneficiario o Beneficiarios del seguro para este concreto siniestro conforme a las condiciones particulares de la póliza deberán presen- tar al Asegurador los documentos siguientes:

- Certificado de nacimiento y de defunción o, en su caso, declaración judicial de fallecimiento del Asegurado.

- Certificado médico oficial del facultativo que haya asistido al Asegurado, indicando el origen, evolución y naturaleza de la enfermedad que le causó la muerte o, en su caso, testimonio de las diligencias judiciales o documentos que acrediten el fallecimiento por accidente.

- DNI o pasaporte del Asegurado y del beneficiario o beneficiarios.

- Certificado del Registro de Actos de Últimas Voluntades, copia del último testamento del Asegurado o, en su caso, auto judicial de declaración de herederos.

- Carta de pago del impuesto de sucesiones y donaciones.

- En su caso, facturas acreditativas de los gastos y servicios del sepelio del Asegurado.

Para el pago de las prestaciones estipuladas en el supuesto de cualquier clase de invalidez del Asegurado, incluida la invalidez causada por infarto de miocardio en caso de haberse contratado esta garantía complementaria, el Beneficiario o Beneficiarios del seguro para este concreto siniestro conforme a las condiciones particulares de la póliza deberán presentar al Asegurador los documentos siguientes:

- Certificado de nacimiento del Asegurado.

- Certificado médico oficial del facultativo que haya asistido al Asegurado, indicando la fecha, el origen, las causas, evolución y naturaleza de la dolencia o lesión corporal que han provocado la enfermedad grave o la invalidez del Asegurado o, en su caso, testimonio de las diligencias judiciales o documentos que acrediten el acaecimiento por accidente de dicha invalidez.

- DNI o pasaporte del Asegurado y del beneficiario o beneficiarios.

- Carta de pago del impuesto de sucesiones y donaciones.

- En su caso, la Resolución firme administrativa o judicial de las instancias competentes en la que se declare la situación y grado de invalidez del Asegurado.

Para el pago de las prestaciones estipuladas en el supuesto de indemnización diaria por hospitalización del Asegurado, el Beneficiario o Beneficiarios del seguro para este concreto siniestro conforme a las condiciones particulares de la póliza deberán presentar al Asegurador los documentos siguientes:

- Certificado de nacimiento del Asegurado.

- Certificado médico oficial del facultativo que haya asistido al Asegurado, indicando la fecha, el origen, las causas, evolución y naturaleza de la dolencia o lesión corporal que han provocado la hospitalización del Asegurado, así como los días durante los cuales ha permanecido el Asegurado ingresado en la institución hospitalaria correspondiente.

- Fotocopia de los documentos de ingreso y de alta del Asegurado en la institución hospitalaria correspondiente.

- DNI o pasaporte del Asegurado y del beneficiario o beneficiarios.

ARTÍCULO 14: PAGO DE LAS PRIMAS.

Los recibos de la prima deberán hacerse efectivos por el Tomador del seguro por el importe y períodos y en los plazos, vencimientos y condiciones estipulados en las condiciones particulares.

La primera prima será exigible desde las 00,00 horas del día siguiente al de la suscripción y firma de la póliza. Si no hubiere sido pagada por culpa del Tomador, el Asegurador tendrá la facultad de resolver unilateralmente el contrato conforme a lo dispuesto en las presentes condiciones generales, o bien de exigir el pago conforme a los medios reconocidos en Derecho sobre la base de la póliza. El Asegurador quedará exento de la cobertura estipulada en este seguro si el siniestro se hubiese producido antes de que la primera prima hubiere sido pagada.

Las primas sucesivas deberán de ser pagadas en su fecha de vencimiento conforme a lo estipulado en las condiciones particulares, entendiendo que dicha fecha es el primer día hábil del mes correspondiente en función del período establecido para el desembolso de tales primas.

En caso de impago de alguna de las primas sucesivas, la cobertura quedará suspendida a las 00,00 horas del día después de haber transcurrido un mes desde la referida fecha de vencimiento. Si el Asegurador no reclama su importe en los seis meses siguientes a la fecha de vencimiento de la prima impagada, el seguro se considerará extinguido. Durante dicho plazo, el Asegurador queda exento de toda cobertura y sólo podrá exigir el pago de la prima del período en curso. Si el contrato no hubiere sido resuelto o extinguido conforme a tales requisitos, la cobertura vuelve a tener efecto a las 00,00 horas del día siguiente a aquel en el que el Tomador pagó la prima.

ARTÍCULO 18: REVALORIZACIÓN DE LAS PRIMAS DEL SEGURO.

Las primas del seguro serán objeto de revalorización, en su caso, en cada renovación anual del seguro, teniendo en cuenta la edad y el sexo del Asegurado o Asegurados, conforme a las tablas de las bases técnicas, siendo la tasa creciente conforme aumenta la edad del Asegurado.

El Asegurador se reserva el derecho a adaptar el importe de las primas sucesivas ante una decisión legislativa o administrativa que dé lugar a la modificación de las obligaciones del Asegurador.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

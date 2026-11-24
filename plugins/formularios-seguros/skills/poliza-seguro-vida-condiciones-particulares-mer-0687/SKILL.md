---
name: poliza-seguro-vida-condiciones-particulares-mer-0687
description: "Póliza de seguro de vida con condiciones particulares. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Póliza de seguro de vida con condiciones particulares

> Formulario **MER-0687** del plugin **Seguros: pólizas, coberturas y reclamaciones** (`formularios-seguros`) · Mercantil › Seguros · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Póliza de seguro de vida con condiciones particulares» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Póliza de seguro de vida con condiciones particulares” para mi caso». También puedes invocarla directamente con `/formularios-seguros:poliza-seguro-vida-condiciones-particulares-mer-0687`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguros:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguros: pólizas, coberturas y reclamaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (9 veces)
- [ ] MARCAR (X) SI VARÓN (3 veces)
- [ ] MES (3 veces)
- [ ] ASEGURADORA (2 veces)
- [ ] AÑO (2 veces)
- [ ] MARCAR (X) SI MUJER (2 veces)
- [ ] DNI/NIE
- [ ] LOCALIDAD
- [ ] MARCAR (X) SI CHEQUE NOMINATIVO
- [ ] MARCAR (X) SI EFECTIVO

## Normas que cita el formulario

- art. 3 Ley 50/1980

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

SEGURO DE VIDA

CONDICIONES PARTICULARES

Datos de la entidad aseguradora: [ASEGURADORA]. Sucursal núm. [Nº]

Agente núm. [Nº]

Corredor:

Datos de la póliza:

Póliza núm. □ De emisión□De modificación

Datos del tomador del seguro:

PERSONA FÍSICA:

Apellidos: Nombre: DNI: NIF: Fecha de nacimiento: / [MES] / [AÑO] Sexo: V [MARCAR (X) SI VARÓN] / M Estado civil: Nacionalidad: Idioma/s: Profesión:

PERSONA JURÍDICA:

Razón social: Objeto social/actividad: CIF:

Nacionalidad: Idioma/s: Sucursal/es:

Domicilio: Nº [Nº]: Bloque: Piso: Esc.: Pta.: Localidad: Provincia: Código Postal: País: Télefono: Fax: E-mail:

Pago de la primera prima: Efectivo [MARCAR (X) SI EFECTIVO] Cheque nominativo Domiliación bancaria

Pago de las primas sucesivas: Efectivo Cheque nominativo [MARCAR (X) SI CHEQUE NOMINATIVO] Domiliación bancaria

Datos de la domiciliación bancaria de recibos.

Entidad bancaria:Oficina:Localidad: Provincia:

ccc:

Datos de la persona asegurada:

Cumplimentar este apartado sólo cuando la persona sea distinta del Tomador.

Apellidos: Nombre: DNI: NIF: Fecha de nacimiento: / / [MES] Sexo: V [MARCAR (X) SI VARÓN] / M [MARCAR (X) SI MUJER]

Estado civil: Nacionalidad: Idioma/s: Profesión:

Domicilio: Nº [Nº]: Bloque: Piso: Esc.: Pta.: Localidad: Provincia: Código Postal: País: Télefono: Fax: E-mail:

Relación con el Tomador:

Datos de la segunda persona asegurada:

Cumplimentar este apartado opcionalmente, si hubiere esta segunda persona asegurada. Apellidos: Nombre: DNI: NIF: Fecha de nacimiento: / [MES] / [AÑO] Sexo: V [MARCAR (X) SI VARÓN] / M [MARCAR (X) SI MUJER] Estado civil: Nacionalidad: Idioma/s: Profesión:

Datos del beneficiario:

El Tomador Otros beneficiarios

El cónyuge del Asegurado, en su defecto los hijos del Asegurado, en su defecto los Padres del Asegurado, y en su defecto los herederos del Asegurado

En caso de haber designado «Otros beneficiarios», se ruega cumplimentar los datos que a continuación se requieren.

Apellidos: Nombre: DNI: NIF: Domicilio: Nº [DNI/NIE]: Bloque: Piso: Esc.: Pta.: Localidad: Provincia: Código Postal: País:

Teléfono: Fax: E-mail: Relación con el Tomador: Relación con el Asegurado:

Hecho en [LOCALIDAD]

Leído y aceptado

EL TOMADOR DEL SEGURO LA 1ª PERSONA ASEGURADA LA 2ª PERSONA ASEGURADA

LA ENTIDAD ASEGURADORA [ASEGURADORA]

ARTÍCULO PRELIMINAR.

CONDICIONES GENERALES

El presente contrato se halla sometido a la Ley 50/1980, de Contrato de Seguro, y a cuantas normas pudieren resultarle de aplicación, así como a las condiciones generales y particulares estipuladas en la presente póliza, sin que tengan validez las cláusulas limitativas de los derechos de los asegurados que no sean específicamente aceptadas por ellos como pacto adicional a las condiciones generales, de conformidad con el artículo 3 de la referida Ley 50/1980.

ARTÍCULO 1: SUJETO Y OBJETO DEL SEGURO: GARANTÍAS ESTIPULADAS.

Conforme a las condiciones estipuladas en la presente póliza, la garantía principal de este seguro consiste en la obligación del Asegurador de pagar al Beneficiario o Beneficiarios designados por el Tomador del seguro el capital garantizado en caso de fallecimiento del Asegurado.

Conforme a las condiciones estipuladas en la presente póliza, las garantías complementarias de este seguro consisten en la obligación del Asegurador de pagar al Beneficiario o Beneficiarios designados por el Tomador del seguro las cantidades porcentuales calculadas según lo dispuesto en las condiciones particulares de la póliza sobre el capital garantizado en caso de fallecimiento.

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

- Rescate total: Importe que percibe el Tomador del seguro como consecuencia de ejercitar su derecho de resolución del contrato, y que se calcula sobre el valor de la póliza una vez deducidos del mismo los gastos y penalizaciones que sean de aplicación conforme a las bases técnicas de este seguro.

- Rescate parcial: Importe que percibe el Tomador del seguro como consecuencia de ejercitar su derecho de retirar cantidades parciales del valor de la póliza, según sus indicaciones en la correspondiente solicitud al Asegurador, y que se calcula sobre el referido valor de la póliza una vez deducidos del mismo los gastos y penalizaciones que sean de aplicación conforme a las bases técnicas de este seguro.

- Período de carencia: lapso ininterrumpido de tiempo, contado desde la fecha de suscripción del seguro, durante el cual no surten efecto las garantías estipuladas en la presente póliza en caso de producirse el siniestro.

(El período de carencia se considera una cláusula limitativa de los derechos del Asegurado, que requiere ser especialmente destacada en hoja separada adjunta a la póliza y ser específicamente firmada por el Tomador del seguro y el Asegurado)

- Siniestro: el acaecimiento de cualquier acontecimiento que dé lugar a la satisfacción por parte del Asegurador de las prestaciones contratadas por el Tomador del seguro a través de la presente póliza como garantía principal o, en su caso, como garantías complementarias, de conformidad con lo estipulado en las condiciones generales, especiales y particulares de la misma, y que incluye los hechos siguientes:

- Fallecimiento: muerte efectiva del Asegurado, en sentido médico y biológico, equipa- rada a la declaración judicial regulada en los artículos 193 y ss. del Código Civil.

ARTÍCULO 3: BASES DEL SEGURO.

El Asegurador asume la cobertura del riesgo y la satisfacción de las prestaciones estipuladas en la presente póliza en las condiciones y dentro de los límites establecidos en la misma cuando se produzca el siniestro tal y como aparece delimitado en el artículo anterior, siempre que no sea objeto de alguna de las exclusiones de cobertura de este seguro establecidas en las presentes condiciones generales.

El Tomador del seguro y el Asegurado tienen el deber de declarar al Asegurador, de acuerdo con los documentos utilizados para la delimitación del riesgo durante la tramitación previa a la suscripción de la póliza, en particular los cuestionarios médicos, y, en su caso, con los resultados de las pruebas y reconocimientos médicos a los que debió someterse el Asegurado a instancia del Asegurador. El Tomador del seguro y el Asegurado quedarán exonerados de tal deber si el Asegurador no les presenta tales documentos ni somete al Asegurado a prueba o reconocimiento alguno o cuando, aun sometiéndoselo, se trate de circunstancias que puedan influir en la valoración del riesgo y que no estén comprendidas en tales documentos, pruebas o reconocimientos, excepto cuanto el Tomador del seguro o el Asegurado tengan conocimiento de la influencia de tales circunstancias en la valoración del riesgo por otros medios.

El seguro se emite sobre la base de las declaraciones del Tomador del seguro y del Asegurado contenidas en los documentos utilizados para la delimitación del riesgo durante la tramitación previa a la suscripción de la póliza, en particular los cuestionarios médicos, y, en su caso, los resultados de las pruebas y reconocimientos médicos a los que debió someterse el Asegurado a instancia del Asegurador. Tales declaraciones han motivado la aceptación del riesgo por el Asegurador así como la fijación de la prima, por lo que constituyen un todo unitario junto con la presente póliza como base de este seguro.

El contrato se perfecciona por el consentimiento manifestado por las partes contratantes mediante la suscripción de la póliza.

Si el contenido de la póliza difiere en todo o en partes de las cláusulas efectivamente acordadas entre los contratantes o de la proposición inicial del Asegurador, el Tomador del seguro podrá reclamar al Asegurador en el plazo de un mes a contar desde la fecha en que el Asegurador le entregue la póliza para que se lleve a cabo la oportuna subsanación de la divergencia existente. Transcurrido dicho plazo sin que se hubiere efectuado reclamación alguna, los contratantes deberán estar a lo dispuesto en la póliza.

ARTÍCULO 4: FACULTAD DE RESOLUCIÓN UNILATERAL DEL TOMADOR DEL SEGURO.

El Tomador del seguro tendrá la facultad libérrima de resolver el presente contrato de seguro en el plazo de treinta días naturales a contar desde la fecha en que el Asegurador le entregue la póliza o, en su caso, el documento de cobertura provisional, sin que sea necesario indicar los motivos y sin penalización alguna.

Esta facultad deberá ejercitarse por escrito firmado por el propio Tomador del seguro y presentado en el domicilio del Asegurador, o en alguna de sus delegaciones o sucursales, o bien a través del agente o corredor interviniente en el contrato conforme a las condiciones particulares de la póliza, y producirá todos sus efectos desde el mismo día de su expedición. En particular, a partir de esta fecha cesará la cobertura de los riesgos objeto del seguro por parte del Asegurador, y el Tomador del seguro tendrá derecho a la devolución de la prima que hubiese pagado, salvo la parte proporcional correspondiente al período de tiempo durante el que se hubiese mantenido la cobertura objeto del seguro. El Asegurador dispondrá para ello de un plazo de treinta días naturales a contar desde la recepción de la comunicación de resolución unilateral del tomador del seguro.

ARTÍCULO 5: EDAD DEL ASEGURADO.

Salvo pacto en contrario, expresamente consignado en las condiciones particulares de la póliza, no podrá ser Asegurado la persona que, en la fecha de suscripción del seguro, tenga menos de [Nº] años de edad, o más de [Nº] años de edad, o que en la fecha de

conclusión del período de cobertura del seguro tenga más de [Nº] años de edad. A tales efectos, la referida cobertura cesará de forma automática a las 24,00 horas del día 31 de diciembre del año dentro del cual el Asegurado cumpla [Nº] años de edad.

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

Quedan excluidos de la cobertura del seguro con carácter específico para las garantías complementarias de cualquier clase de invalidez los siniestros que hayan sido debidos a alguna de las causas siguientes:

- Los accidentes ocasionados por la conducción de motocicletas o ciclomotores por parte del Asegurado.

- Los accidentes ocasionados por la práctica de deportes considerados de alto riesgo conforme a la enumeración de los mismos contenida en el Anexo de la presente póliza.

- Los accidentes de aviación (incluidos los que sean consecuencia de efectuar descensos en paracaídas) cuando el Asegurado haya hecho del vuelo su profesión y ocupe una aeronave como integrante de su tripulación por imperativo de las funciones que se le asignen en virtud de tal integración.

- Los accidentes de navegación submarina, incluyendo los que se produzcan durante inmersiones de buceo con escafandra autónoma.

- Los accidentes producidos durante viajes de exploración.

- Los infartos de miocardio sufridos por el Asegurado no se consideran accidente a los efectos de las garantías complementarias de cualquier clase de invalidez, por lo que no son objeto de cobertura de las mismas.

(las exclusiones de cobertura se consideran cláusulas limitativas de los derechos del Asegurado, que requieren ser especialmente destacadas en hoja separada adjunta a la póliza y ser específicamente firmadas por el Tomador del seguro y el Asegurado)

ARTÍCULO 7: MODIFICACIÓN DEL RIESGO CUBIERTO MEDIANTE EL SEGURO.

El Tomador del seguro o el Asegurado deberán declarar al Asegurador durante el curso del contrato y lo antes posible, cualesquiera variaciones y modificaciones en los datos y circunstancias declarados durante la tramitación previa a la suscripción del seguro, excepto los estrictamente médicos, a fin de que el Asegurador pueda proponer las oportunas modificaciones de sus condiciones iniciales. En particular, esta declaración deberá comprender los cambios de residencia y de profesión del Asegurado, así como la práctica de actividades consideradas de riesgo, enumeradas en el Anexo núm. [Nº] de la presente póliza.

Si el siniestro sobreviniere antes de que existiese la citada comunicación, la prestación se reducirá proporcionalmente a la diferencia entre la prima convenida y la que hubiere resultado de haberse conocido por parte del Asegurador las nuevas circunstancias, salvo que mediase dolo o culpa grave del Tomador del seguro o el Asegurado en cuyo caso el Asegurador podrá resolver unilateralmente el contrato conforme a lo establecido en las presentes condiciones generales y quedará liberado de su obligación.

En caso de aceptar expresamente el Asegurador la agravación del riesgo, el Tomador del seguro quedará obligado al pago de la prorrata de la prima correspondiente. La cobertura de los nuevos riesgos declarados no tendrá efecto hasta las 00,00 horas del día siguiente a aquel en el que el Tomador pagó la referida prorrata.

Asimismo el Tomador del seguro o el Asegurado podrán poner en conocimiento del Asegurador cualesquiera circunstancias que disminuyan el riesgo cubierto, lo que obligará al Asegurador a reducir el importe de la prima siguiente a la del período en curso en la cuantía que corresponda.

ARTÍCULO 8: VALORES DE RESCATE.

Mientras no se haya producido el fallecimiento del Asegurado, y a partir del pago de las primas correspondientes al primer año desde la suscripción del seguro, el Tomador tendrá la facultad de efectuar el rescate total del valor de la póliza, en los términos establecidos en las presentes condiciones generales, y que implicará la resolución del contrato por la propia voluntad del Tomador del seguro y la consiguiente extinción de las coberturas objeto del mismo.

Mientras no se haya producido el fallecimiento del Asegurado, el Tomador tendrá la facultad de retirar cantidades parciales del valor de la póliza en los términos establecidos en las presentes condiciones generales para el rescate parcial.

El ejercicio de los derechos de rescate total o parcial por parte del Tomador del seguro requerirá comunicación por escrito al Asegurador en tal sentido dirigida de modo indubitado al domicilio de este último, o en alguna de sus delegaciones o sucursales, o bien a través del agente o corredor interviniente en el contrato conforme a las condiciones particulares de la póliza. El Asegurador dispondrá de un plazo de treinta días naturales desde la fecha de remisión de dicha comunicación para entregar el importe del rescate al Tomador del seguro en la forma y condiciones indicadas en la reiterada comunicación.

El importe del rescate, así como los gastos que se repercuten por la operación de rescate total o parcial, se recogen en las bases técnicas del seguro.

ARTÍCULO 9: EFECTO DE LA COBERTURA DEL SEGURO.

La cobertura del seguro tomará efecto desde las 00,00 horas del día siguiente al día de conclusión del período de carencia estipulado en las condiciones particulares, y hasta las 24,00 horas del día de conclusión del período de duración del seguro establecido en tales condiciones particulares.

ARTÍCULO 10: TRAMITACIÓN DEL SINIESTRO.

Una vez producido el siniestro, el Tomador, el Asegurado o, en su caso, el Beneficiario, deberán comunicarlo al Asegurador a la mayor brevedad posible, en un plazo máximo de siete días naturales desde que lo hubieren conocido, así como facilitarle toda la información necesaria para su comprobación, determinación de sus causas, y valoración.

ARTÍCULO 11: ACREDITACIÓN DE LA PRODUCCIÓN EFECTIVA DEL SINIESTRO.

Para el pago de las prestaciones estipuladas en el supuesto de fallecimiento del Asegurado, y de los correspondientes gastos y servicios de sepelio en caso de haberse contratado esta garantía complementaria, el Beneficiario o Beneficiarios del seguro para este concreto siniestro conforme a las condiciones particulares de la póliza deberán presentar al Asegurador los documentos siguientes:

- Certificado de nacimiento y de defunción o, en su caso, declaración judicial de fallecimiento del Asegurado.

- Certificado médico oficial del facultativo que haya asistido al Asegurado, indicando el origen, evolución y naturaleza de la enfermedad que le causó la muerte o, en su caso, testimonio de las diligencias judiciales o documentos que acrediten el fallecimiento por accidente.

- DNI, NIF o pasaporte del Asegurado y del Beneficiario o Beneficiarios.

- Certificado del Registro de Actos de Últimas Voluntades, copia del último testamento del Asegurado o, en su caso, auto judicial de declaración de herederos.

- Carta de pago del impuesto de sucesiones y donaciones.

- En su caso, facturas acreditativas de los gastos y servicios del sepelio del Asegurado.

ARTÍCULO 13: PAGO DE LAS INDEMNIZACIONES.

Una vez recibidos los documentos acreditativos de la producción efectiva del siniestro por parte del Asegurador, este último estará obligado a pagar o, en su caso, consignar la prestación o prestaciones garantizadas en las condiciones particulares de esta póliza en el plazo máximo de cinco días hábiles y, en cualquier caso, dentro de los cuarenta días naturales a partir de la recepción de la comunicación del siniestro.

Si en el plazo máximo de tres meses desde la producción del siniestro el Asegurador no hubiere abonado al Beneficiario o, en su caso, Beneficiarios, las prestaciones garantizadas correspondientes, sin que mediare causa justificada o que no le fuere imputable al Asegurador, el importe de las mismas se incrementará con un interés anual igual al del interés legal del dinero vigente en el momento en que se devengue, incrementado en un 50%, sin que dicho interés anual pueda ser inferior al 20% a partir del transcurso de dos años desde la referida producción del siniestro.

ARTÍCULO 14: PAGO DE LAS PRIMAS.

Los recibos de la prima deberán hacerse efectivos por el Tomador del seguro por el importe y períodos y en los plazos, vencimientos y condiciones estipulados en las condiciones particulares.

La primera prima será exigible desde las 00,00 horas del día siguiente al de la suscripción y firma de la póliza. Si no hubiere sido pagada por culpa del Tomador, el Asegurador tendrá la facultad de resolver unilateralmente el contrato conforme a lo dispuesto en las presentes condiciones generales, o bien de exigir el pago conforme a los medios reconocidos en Derecho sobre la base de la póliza. El Asegurador quedará exento de la cobertura estipulada en este seguro si el siniestro se hubiese producido antes de que la primera prima hubiere sido pagada.

Las primas sucesivas deberán de ser pagadas en su fecha de vencimiento conforme a lo estipulado en las condiciones particulares, entendiendo que dicha fecha es el primer día hábil del mes correspondiente en función del período establecido para el desembolso de tales primas.

En caso de impago de alguna de las primas sucesivas durante los dos primeros años desde la fecha de inicio de la cobertura del seguro, dicha cobertura quedará suspendida a las 00,00 horas del día después de haber transcurrido un mes desde la referida fecha de vencimiento. Si el Asegurador no reclama su importe en los seis meses siguientes a la fecha de vencimiento de la prima impagada, el seguro se considerará extinguido. Durante dicho plazo, el Asegurador queda exento de toda cobertura y sólo podrá exigir el pago de la prima del período en curso. Si el contrato no hubiere sido resuelto o extinguido conforme a tales requisitos, la cobertura vuelve a tener efecto a las 00,00 horas del día siguiente a aquel en el que el Tomador pagó la prima.

En caso de impago de alguna de las primas sucesivas transcurridos dos años desde la fecha de inicio de la cobertura del seguro, se producirá de forma automática la reducción del capital garantizado de acuerdo a lo establecido en las bases técnicas. No obstante, el Tomador del seguro podrá rehabilitar el capital garantizado inicial en función de lo previsto en dichas bases técnicas previo pago de las primas atrasadas actualizadas incrementadas en el interés legal del dinero vigente en el momento del pago, siempre que todavía no haya tenido lugar el siniestro cubierto por el seguro, y que el riesgo objeto del mismo no haya sufrido alteraciones significativas desde el momento en que se produjo el impago de las primas.

ARTÍCULO 15: DOMICILIACIÓN BANCARIA DEL PAGO DE LAS PRIMAS.

Si se determina en las condiciones particulares de la presente póliza la domiciliación bancaria de los recibos correspondientes a las primas, el cobro de las mismas se realizará conforme a las normas siguientes:

- Como obligado al pago de la prima, el Tomador del seguro entregará al Asegurador carta dirigida a la entidad de crédito correspondiente dando la oportuna orden de domiciliación de los recibos de las primas, con todos los datos necesarios a tales efectos.

- La prima se entenderá satisfecha a su vencimiento, salvo que intentado el cobro dentro del plazo de un mes después de la fecha de vencimiento no existiesen fondos suficientes en la cuenta corriente indicada por el Tomador del seguro para la domiciliación de los recibos de las primas. En este caso, deberá satisfacerse la prima en el domicilio del Asegurador, o en alguna de sus delegaciones o sucursales, o bien a través del agente o corredor interviniente en el contrato conforme a las condiciones particulares de la póliza.

- Si el Asegurador dejare transcurrir el plazo de un mes desde la fecha de vencimiento de la prima sin presentar el recibo al cobro y al hacerlo no existieren fondos suficientes en la cuenta corriente indicada por el Tomador del seguro para la domiciliación de los recibos de las primas, el Asegurador deberá notificar este hecho al Tomador por carta certificada u otro medio indubitado dirigidos al último domicilio de aquél comunicado al Asegurador, y se concederá entonces un nuevo plazo de treinta días naturales desde la recepción de la carta certificada por parte del Tomador para que se pueda satisfacer el importe de la prima impagada en el domicilio del Asegurador, o en alguna de sus delegaciones o sucursales, o bien a través del agente o corredor interviniente en el contrato conforme a las condiciones particulares de la póliza.

ARTÍCULO 16: INFORMACIÓN AL TOMADOR DEL SEGURO.

El Asegurador deberá facilitar al Tomador del seguro con carácter trimestral al inicio de cada trimestre natural la situación actual de la póliza en dicho período, indicando al menos el valor de la póliza al final del período de referencia y el tipo de interés técnico aplicable al próximo trimestre natural.

El Tomador del seguro podrá solicitar en cualquier momento del Asegurador cuales quiera otras informaciones adicionales sobre este seguro, en particular sobre sus bases técnicas, quedando obligado el Asegurador a facilitárselas en soporte duradero en el plazo máximo de quince días hábiles desde la recepción de la solicitud.

ARTÍCULO 17: COMUNICACIONES.

Las comunicaciones del Asegurador al Tomador del seguro, al Asegurado o, en su caso, al Beneficiario o Beneficiarios, se dirigirán a las direcciones consignadas en las condiciones particulares de la póliza, o en sus posteriores modificaciones. A tales efectos, en caso de cambio de domicilio o de los restantes datos sobre los medios de localización del Tomador del seguro, Asegurado o Beneficiario o Beneficiarios, dichos cambios deberán ser comunicados por escrito y de forma indubitada al Asegurador a la mayor brevedad posible. Tales comunicaciones escritas pasarán a integrarse en las condiciones particulares de la póliza. Si el Tomador del seguro, Asegurado o Beneficiario o Beneficiarios omitieren esta comunicación, el Asegurador procederá a efectuar las notificaciones y comunicaciones que procedan en sus últimos domicilios conocidos, quedando exento de cualquier responsabilidad.

Las comunicaciones del Tomador del Seguro o del Asegurado deberán ser dirigidas al Asegurador en su domicilio, o en alguna de sus delegaciones o sucursales, o bien a través del agente o corredor interviniente en el contrato conforme a las condiciones particulares de la póliza, y se podrán realizar por cualquier medio indubitado, salvo en aquellas para las que se requiera expresamente la forma escrita en las presentes condiciones generales.

Las comunicaciones y cualesquiera otras actuaciones, en particular el pago de las primas, realizadas por el Tomador, el Asegurado o, en su caso, por el beneficiario o beneficiarios del seguro a través del Agente interviniente en su tramitación e identificado como tal en las condiciones particulares de la póliza o, en su caso, en su posterior modificación, surtirán los mismos efectos que si se hubiesen realizado directamente frente al Asegurador.

Las comunicaciones y cualesquiera otras actuaciones, en particular el pago de las primas, realizadas por el Tomador, el Asegurado o, en su caso, por el beneficiario o beneficiarios del seguro a través del Corredor interviniente en su tramitación e identificado como tal en las condiciones particulares de la póliza o, en su caso, en su posterior modificación, surtirán los mismos efectos que si se hubiesen realizado directamente frente al Asegurador, salvo indicación en contrario de quién haya efectuado la comunicación o actuación.

ARTÍCULO 18: REVALORIZACIÓN DEL IMPORTE DEL CAPITAL GARANTIZADO Y DE LAS PRIMAS DEL SEGURO.

Tanto el capital garantizado como las primas sucesivas de las distintas prestaciones incluidas en este seguro se revalorizarán anualmente en el tanto por ciento estipulado en las condiciones particulares de la póliza. Este primer incremento por revalorización será constante y de carácter aritmético, por lo que su importe se obtendrá por aplicación del porcentaje sobre el importe inicial consignado en las condiciones particulares para las diversas garantías cubiertas. Se producirá asimismo un crecimiento geométrico en dicha revalorización como resultado de aplicar trimestralmente el tipo de interés técnico variable consignado en las bases técnicas sobre el importe que tuviesen en el trimestre inmediatamente anterior las diversas garantías cubiertas conforme a las condiciones particulares de la póliza

Los importes de las prestaciones a satisfacer por el Asegurador se calcularán tomando como base el capital garantizado revalorizado en el momento de producción del siniestro, de conformidad con las bases técnicas del seguro.

El Asegurador se reserva el derecho a adaptar el importe del capital garantizado y de las primas sucesivas ante una decisión legislativa o administrativa que dé lugar a la modificación de las obligaciones del Asegurador.

Asimismo, el Tomador del Seguro tendrá la facultad libérrima de variar el importe de las primas periódicas inicialmente previstas mediante la pertinente comunicación por escrito y de forma indubitada al Asegurador en su domicilio, o en alguna de sus delegaciones o sucursales, o bien a través del agente o corredor interviniente en el contrato conforme a las condiciones particulares de la póliza, con una antelación mínima de dos meses antes de su entrada en vigor en el próximo vencimiento previsto conforme a tales condiciones particulares. Esta comunicación escrita pasará a integrarse en dichas condiciones como modificación de las mismas. Para llevar a cabo esta modificación, será preciso que la póliza se halle en el momento de la comunicación al corriente del pago de primas.

El Tomador del seguro también podrá realizar en cualquier momento aportaciones extraordinarias a prima única por un importe mínimo igual al establecido en las normas de contratación contenidas en las bases técnicas del seguro.

ARTÍCULO 19: DESIGNACIÓN Y CAMBIO DE BENEFICIARIOS.

En cualquier momento durante la vigencia del contrato, el Tomador del seguro goza de la facultad libérrima de designar al Beneficiario o Beneficiarios de la garantía contratada, y asimismo de revocar o modificar dicha designación sin necesidad de consentimiento del Asegurador, salvo que haya renunciado expresamente y por escrito a esta Facultad.

Tanto la designación como la revocación de Beneficiario o Beneficiarios se podrán realizar en la solicitud del seguro, en las propias condiciones particulares de la póliza, o en posterior declaración escrita comunicada al Asegurador por medio indubitado, o bien mediante testamento.

Si los Beneficiarios han sido designados de forma genérica y sucesiva como cónyuge, hijos, padres o herederos, dicha designación será interpretada de la manera siguiente:

- Cónyuge: persona que lo sea en el momento del fallecimiento del Asegurado, o, en su caso, que sea legalmente considerada como pareja de hecho, de conformidad con la normativa aplicable al supuesto.

- Hijos: cualesquiera descendientes directos con derecho a herencia.

- Padres: los dos ascendientes directos.

- Herederos: los que ostenten tal condición en el momento de fallecer el Asegurado. En todos los casos recién enumerados deberá hacerse constar en las condiciones particulares o, en su caso, en sus modificaciones, o en el documento o testamento en el que se establezca su designación como Beneficiarios, si el cónyuge, hijos, padres o herederos lo son del Tomador del seguro, del Asegurado o de un tercero. No obstante, de no haberse especificado, se considerará que lo son del Tomador del seguro.

Si la designación se hace a favor de varios Beneficiarios sin especificar la forma de distribución, la prestación convenida se distribuirá a partes iguales entre ellos o, en su caso, en proporción a su cuota hereditaria, si se tratase de una designación en favor de los herederos.

La parte no adquirida por un beneficiario acrecerá a los demás.

Si en el momento de fallecimiento del Asegurado no hubiere beneficiario designado ni reglas para su determinación la garantía convenida pasará a formar parte del patrimonio del Tomador del seguro.

ARTÍCULO 20: CESIÓN Y PIGNORACIÓN DE LA PÓLIZA.

El Tomador del seguro podrá en todo momento ceder o pignorar la póliza, siempre que no haya sido designado Beneficiario o Beneficiarios con carácter irrevocable.

La cesión o pignoración de la póliza implica la revocación del Beneficiario o Beneficiarios.

El Tomador del seguro deberá comunicar la cesión o pignoración de la póliza de forma fehaciente y por escrito al Asegurador en su domicilio, o en alguna de sus delegaciones o sucursales, o bien a través del agente o corredor interviniente en el contrato conforme a las condiciones particulares de la póliza.

ARTÍCULO 21: RESOLUCIÓN DEL SEGURO.

El Asegurador se reserva la facultad de resolver unilateralmente el contrato, quedando sin efecto la cobertura estipulada en el mismo, en los supuestos siguientes:

- Reserva o inexactitud del Tomador del seguro o del Asegurado en sus declaraciones al cumplimentar los documentos y cuestionarios médicos entregados al efecto por el Asegurado, o en su caso, al someterse a los reconocimientos médicos requeridos por el Asegurador con carácter previo a la suscripción de la póliza, en los términos establecidos en las bases del seguro recogidas en las presentes condiciones generales, si medió dolo o culpa grave del Asegurado.

- Omisión del deber de comunicación al Asegurador de la agravación de los riesgos cubiertos por el seguro, en los términos establecidos en las presentes condiciones generales, si medió dolo o mala fe del Tomador del seguro, o del Asegurado.

- Si el siniestro se produce antes de haberse pagado la primera prima, en los términos establecidos en las presentes condiciones generales.

La facultad de resolución unilateral del Asegurador en los referidos supuestos será ejercitada mediante declaración dirigida por medio indubitado dirigido al Tomador del seguro en su último domicilio declarado al Asegurador en el plazo de treinta días naturales a contar del conocimiento por parte del Asegurador de la concurrencia del motivo de resolución correspondiente.

Las primas relativas al período en curso en el que el Asegurador ejercite esta facultad de resolución del contrato corresponderán al Asegurador.

ARTÍCULO 22: INDISPUTABILIDAD.

El Asegurador no podrá impugnar el contrato una vez transcurrido un año a contar desde la fecha de suscripción de la póliza, excepto en los supuestos en los que el Tomador del seguro o, en su caso, el Asegurado hayan actuado con dolo, o en el supuesto de indicación inexacta de la edad del Asegurado, si su verdadera edad en el momento de entrada en vigor de la cobertura objeto del contrato excede de los límites de admisión establecidos en las condiciones generales del mismo.

ARTÍCULO 23: TRATAMIENTO AUTOMATIZADO DE LOS DATOS DE CARÁCTER PERSONAL.

A efectos de lo dispuesto en la LO 3/2018, de Protección de Datos Personales y Garantía de los Derechos Digitales, se pone en conocimiento del Tomador del seguro o del Asegurado, las informaciones siguientes:

- Los datos de carácter personal facilitados al Asegurador a través de la presente póliza y de toda la documentación anexa a la misma, así como los que puedan facilitarse con ocasión de cualesquiera comunicaciones al Asegurador o, en su caso, de la tramitación del siniestro, serán incorporados y tratados en los ficheros automatizados de que es titular el Asegurador, en tanto que destinatario de los mismos, por ser elementos indispensables en la valoración del riesgo y en el mantenimiento de la relación contractual.

- El Tomador del seguro o el Asegurado podrán ejercitar los derechos de acceso, rectificación y cancelación de los referidos datos de carácter personal, en la forma prevista y de conformidad con la legislación vigente, en particular la Ley Orgánica 3/2018, en el domicilio del Asegurador, o en alguna de sus delegaciones o sucursales, o bien a través del agente o corredor interviniente en el contrato conforme a las condiciones particulares de la póliza.

- El Asegurador se obliga a mantener el deber de reserva y confidencialidad sobre los referidos datos de carácter personal de conformidad con la legislación vigente, en particular la Ley Orgánica 3/2018, y hasta los límites establecidos en la misma.

- El Tomador del seguro y el Asegurado otorgan su consentimiento expreso para que los referidos datos de carácter personal, en la forma y con las limitaciones establecidas en la Ley Orgánica 3/2018, puedan ser cedidos a otras entidades aseguradoras u organismos públicos o privados relacionados con el sector asegurador con fines estadísticos y de lucha contra el fraude, así como por razones de coaseguro o reaseguro, en particular a las sociedades del grupo al que pertenece el Asegurador.

(los contenidos de este artículo de las condiciones generales se consideran cláusulas limitativas de los derechos del Asegurado, que requieren ser especialmente destacadas en hoja separada adjunta a la póliza y ser específicamente firmadas por el Tomador del seguro y el Asegurado)

ARTÍCULO 24: GASTOS IMPUTABLES A LA PÓLIZA DEL SEGURO.

El Asegurador garantiza que los gastos que se expresan en términos porcentuales se mantendrán a lo largo de la vigencia de la póliza, mientras que los gastos que se expresan en términos monetarios serán incrementados con efecto desde el 1 de febrero de cada año según la variación experimentada por el Índice de Precios al Consumo (o índice que en el futuro le sustituya, en su caso) en el conjunto nacional en el ejercicio natural inmediata- mente anterior.

El Asegurador se reserva la facultad de cargar una serie de gastos el primer día de cada mes sobre el valor de la póliza calculado al último día del mes precedente, calculados conforme a las bases técnicas, con miras a cubrir los gastos de administración y gestión de la póliza.

El Asegurador también podrá deducir adicionalmente del valor de la póliza, y de la misma forma que la expresada en el párrafo anterior, el coste correspondiente a la cobertura de riesgo de fallecimiento, calculado conforme a las bases técnicas, en particular a su tabla de tarifas detallada por edad.

Para el período existente entre la fecha de efecto de la cobertura y el primer día del mes siguiente, el Asegurador cargará un gasto proporcional al número de días efectivamente transcurridos.

ARTÍCULO 25: IMPUESTOS, TASAS Y RECARGOS.

Los impuestos, tasas y recargos legalmente repercutibles de conformidad con la normativa vigente que se deban satisfacer en razón de este contrato, así como las retenciones a cuenta de los impuestos que resulten aplicables correrán a cargo del Tomador del seguro, del Asegurado o, en su caso, del Beneficiario o Beneficiarios, según proceda.

ARTÍCULO 26: JURISDICCIÓN Y COMPETENCIA.

Será competente para el conocimiento de las acciones derivadas de este contrato el tribunal del domicilio del Asegurado.

ARTÍCULO 27: PRESCRIPCIÓN DE ACCIONES.

Las acciones derivadas de este contrato prescriben a los cinco años contados desde el día siguiente a aquel en el que pudieron ejercitarse, pudiendo interrumpirse este plazo por alguno de los medios siguientes:

- Por su ejercicio ante las instancias judiciales competentes.

- Por reclamación extrajudicial del acreedor al deudor.

- Por cualquier acto de reconocimiento de la deuda por parte del deudor.

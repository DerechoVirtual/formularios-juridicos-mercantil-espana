---
name: poliza-seguro-responsabilidad-civil-corredores-seguros-mer-0690
description: "Póliza de seguro de responsabilidad civil de corredores de seguros. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Póliza de seguro de responsabilidad civil de corredores de seguros

> Formulario **MER-0690** del plugin **Seguros: pólizas, coberturas y reclamaciones** (`formularios-seguros`) · Mercantil › Seguros · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Póliza de seguro de responsabilidad civil de corredores de seguros» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Póliza de seguro de responsabilidad civil de corredores de seguros” para mi caso». También puedes invocarla directamente con `/formularios-seguros:poliza-seguro-responsabilidad-civil-corredores-seguros-mer-0690`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguros:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguros: pólizas, coberturas y reclamaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (3 veces)
- [ ] CALLE (2 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] LUGAR (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] MES (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] C.P.
- [ ] IMPORTE
- [ ] Nº
- [ ] Nº DE AÑOS
- [ ] Nº DE ÁRBITROS

## Normas que cita el formulario

- art. 3 Ley 50/1980
- art. 128.1 Real Decreto-ley 3/2020
- art. 33 Ley 50/1980

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

CONDICIONES PARTICULARES PÓLIZA Nº [NÚMERO] SUPLEMENTO NÚM. [Nº]

SUSTITUYE O REE MPLAZA A LA PÓLIZA NÚM. TOMADOR DEL SEGURO/ASEGURADO: Nombre/Razón Social: NIF:

Domicilio: c/ [CALLE]

CP: Población: Provincia: DOMICILIACIÓN DE RECIBOS:

Banco/Caja de Ahorros: Sucursal:

Domicilio: C/ [CALLE]

CP [C.P.] Población: Provincia: Clase de Cta: c/c Núm [NÚMERO]

FECH A DE EFECTO: (A las 00 horas)

FECHA DE VENCIMIENTO: (A las 24 horas)

DURACIÓN DEL SEGURO PARA PERÍODOS SIGUIENTES: AÑOS PRORROGABLES

Desde el [FECHA] a las 00 horas al [FECHA] a las 24 horas

FORMA DE PAGO: ANUAL

SUMA ASEGURADA POR SINIESTRO Y AÑO DE SEGURO: [IMPORTE] euros. LÍMITE MÁXIMO DE FRANQUICIA: % de la indemnización máximo euros.

EL TOMADOR DEL SEGURO/ASEGURADO POR LA ASEGURADORA

DETALLE DEL PRIMER RECIBO:

────────────────────

*PERÍODO PRIMA NETA
IPS IMPTOS. PRIMA
TOTAL

CLÁUSULAS

- Los datos contenidos en la Solicitud Cuestionario cumplimentada por el Asegurado y los Certificados aportados en Entidades Aseguradoras, han servido de base para el cálculo de la prima del presente contrato.

- El Asegurado se obliga a facilitar al Asegurador, cuando sea requerido por éste y en el plazo máximo indicado por él mismo, una nueva actualización de información, donde se reflejarán los datos de la nueva situación del Asegurado, a los efectos de determinar las posibles modificaciones de las Condiciones del Seguro.

- DELIMITACIÓN TEMPORAL: De acuerdo con lo establecido en el artículo 3, punto

2 de las Condiciones Generales de esta póliza, el Asegurado elige expresamente como período máximo en que puede formularse la reclamación del perjudicado, una vez terminada

la última de las prórrogas del contrato o, en su defecto, el período de duración de aquél, el de [Nº DE AÑOS] año/s ( AÑOS).

Hemos por triplicado, en [LUGAR], a [DÍA] de [MES] de [AÑO].

EL TOMADOR DEL SEGURO/ASEGURADO	ENTIDAD ASEGURADORA

PACTO EXPRESO

A los efectos de lo dispuesto en el artículo 3 de la Ley 50/1980 de Contrato de Seguro, el abajo firmante, como Asegurado y profesional de Seguro, declara haber leído, entendido y comprendido, en todos sus términos, las Condiciones Generales (Modelo [MARCA/MODELO]), Especiales (Modelo [MARCA/MODELO]) y Particulares que forman parte de esta póliza, de las que recibe un ejemplar, y en prueba de aceptación expresa de las mismas y, en especial, de las cláusulas limitativas que se hallan destacadas en las mismas.

EL TOMADOR DEL SEGURO/ASEGURADO	ENTIDAD ASEGURADORA

De conformidad con lo regulado en la Ley Orgánica 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales, el/los abajo firmante/s declara/n que los datos indicados son ciertos y otorga/n su consentimiento expreso para que puedan ser tratados automatizadamente con el fin de suscribir el seguro. esta información podrá ser cedida, en su totalidad o en parte, a otras entidades aseguradoras con el objeto de facilitar la tramitación de los siniestros, a otras instituciones colaboradoras con el sector asegurador con fines estadísticos y de lucha contra el fraude, así como por razones de coaseguro o reaseguro. asimismo, podrá hacerse uso de esta información para ofrecer al asegurado otros productos o servicios de la entidad.

PÓLIZA DE SEGURO DE RESPONSABILIDAD CIVIL PROFESIONAL PARA CORREDORES DE SEGUROS

CONDICIONADO DE PÓLIZA SEGURO DE RESPONSABILIDAD CIVIL PROFESIONAL

-CORREDORES DE SEGUROS-

El presente contrato de seguro se rige por lo dispuesto en la Ley 50/1980, de 8de octubre, de Contrato de Seguro y por lo convenido en las condiciones generales y particulares de este contrato, sin que tengan validez las cláusulas limitativas de los derechos de los asegurados que no sean especialmente aceptadas por los mismos. No requerirán dicha aceptación las meras transcripciones o referencias a preceptos legales imperativos.

Los términos y condiciones del presente contrato así como el contenido de la documentación precontractual, quedan afectos a la confidencialidad establecida en la Ley Orgánica 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales.

Las cláusulas que delimitan el compromiso asumido por el Asegurador han sido aceptadas por las partes en razón al equilibrio contractual entre el alcance de la cobertura otorgada y la prima correspondiente.

Si las partes hubieran pretendido estipular un contenido distinto al marco contractual objeto del seguro, bien la póliza no hubiera sido suscita o se habrían pactado condiciones económicas diferentes.

ARTÍCULO PRELIMINAR.-DEFINICIONES.

A los efectos de este contrato se entiende por:

1. ASEGURADOR: La Entidad que, mediante el cobro de la prima, asume la cobertura de los riesgos objeto de este contrato con arreglo a las condiciones de la póliza.

2. TOMADOR DEL SEGURO: Persona que suscribe este contrato con el Asegurador y a quien corresponden las obligaciones que se deriven del mismo, salvo aquellas que correspondan expresamente al asegurado.

3. ASEGURADO: Dentro de los límites cuantitativos y contractuales de la póliza tendrán tal condición:

* El Corredor, persona física o jurídica, titular del interés objeto del seguro. El Asegurado El asegurador

* El personal laboral dependiente del Corredor o Correduría, incluido en la nómina de éstos y en el Ejercicio de las funciones especiales que constituyen la actividad de mediación objeto de este seguro.

* En el caso de Corredurías de Seguros, los Administradores y personal directivo que actúen en interés de la misma y dentro de las competencias que legal y estatutariamente tienen atribuidas.

4. PÓLIZA: Documento que contiene las Condiciones Generales de este contrato y las Particulares que identifican el riesgo, así como las modificaciones que se produzcan durante la vigencia del seguro.

5. PRIMA: Precio del seguro en cuyo recibo se incluirán, además, los recargos y tributos repercutibles.

6. SUMA ASEGURADA: Cantidad establecida en las Condiciones Particulares de la póliza, que representa el límite máximo de la indemnización por cada siniestro y período de seguro.

7. SINIESTRO: Todo hecho que pudiera poner en juego las garantías de la póliza del que puedan derivarse eventuales responsabilidades para el Asegurado, pero siempre que queden comprendidas en el marco de cobertura del presente seguro.

8. RECLAMACIÓN: Procedimiento judicial o administrativo o bien un requerimiento formal y por escrito contra el Asegurado, como presunto responsable de uno de los riesgos cubiertos por la póliza, o bien contra el Asegurador en ejercicio de las acciones legales que corresponden.

Así mismo, se entiende como reclamación cualquier hecho o circunstancia concreta conocida por vez primera por el Asegurado y que conste notificación de forma inequívoca por éste a la Entidad Aseguradora, que pueda razonablemente determinar la ulterior formulación de una petición de resarcimiento, o hacer entrar en juego las coberturas de la póliza.

9. DAÑO CUBIERTO: La pérdida económica que sea consecuencia directa de la actividad negligente del Asegurado y siempre que la responsabilidad derivase de un hecho cubierto por esta póliza.

10. FRANQUICIA: La cantidad o porcentaje, expresamente pactados, que se deducirá de la indemnización que corresponda satisfacer por el Asegurador en cada siniestro.

11. TERCERO: Cualquier persona física o jurídica distinta de:

a) El Tomador del Seguro y el Asegurado.

b) Los cónyuges, ascendientes y descendientes del Tomador del Seguro y el Asegurado.

c) Los familiares del Tomador del Seguro y del Asegurado que convivan con ellos. d) Los socios, directivos, asalariados y personas que, de hecho o de derecho, dependan del Tomador del Seguro o del Asegurado, mientras actúen en el ámbito de dicha dependencia.

12. PERÍODO DEL SEGURO: El tiempo transcurrido entre la fecha del efecto de la póliza y la del vencimiento, tal y como se recoge en las Condiciones Particulares, o bien, entre la fecha de efecto y la de rescisión, resolución o extinción del contrato, si fueran anteriores.

13. MEDIADOR DE SEGUROS PRIVADOS: La actividad mercantil definida en el artículo 128.1 del Real Decreto-ley 3/2020, de 4 de febrero.

14. CORREDOR DE SEGUROS: Las personas físicas o jurídicas que realizan la actividad mercantil de mediación de seguros privados sin mantener vínculos que supongan afección con entidades aseguradoras o pérdida de independencia respecto a éstas y ofreciendo asesoramiento profesional imparcial a quienes demandan la cobertura de los riesgos a que se encuentran expuestos sus personas, sus patrimonios, sus intereses o responsabilidades.

OBJETO Y EXTINCIÓN DEL SEGURO

ARTICULO 1.-RIESGOS CUBIERTOS.

En los términos y condiciones consignados en la póliza, el Asegurador toma a su cargo la Responsabilidad Civil que pueda derivarse para el Asegurado, de acuerdo con la normativa legal vigente, como consecuencia de sus acciones u omisiones negligentes en el ejercicio de la actividad mercantil de Mediación de Seguros Privados en la modalidad de «Correduría de Seguros» en las condiciones previstas en la Ley.

Dentro siempre de los límites fijados en la Condiciones Particulares, correrán por cuenta del Asegurador

- El abono a los perjudicados o a sus derechohabientes de las indemnizaciones a que diera lugar la responsabilidad civil del Asegurado.

- El pago de las costas y gastos judiciales o extrajudiciales inherentes al siniestro, que se abonará en la misma proporción existente entre la indemnización que deba satisfacer el Asegurador, de acuerdo con lo previsto en la póliza, y el importe total de la responsabilidad del Asegurado en el siniestro.

- La constitución de las fianzas judiciales exigidas al Asegurado para garantizar su responsabilidad civil.

ARTÍCULO 2.- EXCLUSIONES

Queda excluida de las garantías del seguro cualquier reclamación:

1. De la que el Tomador del Seguro o Asegurado hubiera tenido conocimiento en el momento de formalizar el contrato.

2. Por daños sufridos por los bienes que por cualquier motivo (depósito, uso, manipulación, transporte u otro), se hallen en poder del Asegurado o de personas de quien éste sea responsable, excepto lo referido a daños, pérdida o extravío de la documentación en poder del Asegurado para el desarrollo de la gestión encomendada.

3. Por daños y perjuicios que sean el resultado de actividades profesionales distintas a la de Corredor de Seguros, así como aquellos que tengan su origen en los inmuebles, sus partes integrantes, pertenencias, bienes, muebles e instalaciones en posesión del Asegurado.

4. Realizada por personas físicas o jurídicas que tengan vínculo estrecho o participación significativa en la Sociedad Mediadora, asignada en los términos previstos en el Real Decreto-ley 3/2020, de 4 de febrero.

5. A consecuencia de pactos especiales o promesas que vayan más allá del ámbito de la responsabilidad civil legal.

6. Por faltas en caja o errores en cobros o pagos, así como pérdidas o extravío de dinero y otros valores pecuniarios, valores emitidos al portador, o a la orden, o endosados.

7. Derivada del pago de multas o sanciones económicas impuestas por los tribunales y demás autoridades.

8. Derivada de la declaración de insolvencia o liquidación de las Entidades Aseguradoras o del propio Asegurado.

9. Por los daños a terceros debidos a la actuación maliciosa del Asegurado. Así mismo, no queda cubierto por las garantías del seguro el porcentaje del 20 por 100 de la indemnización, que se establece como franquicia deducible a cargo del Asegurado en cada siniestro, en los términos que se establezcan en las Condiciones Particulares.

ARTÍCULO 3.-DELIMITACIÓN TEMPORAL.

1. La cobertura del presente contrato ampara el nacimiento a cargo del asegurado, durante el período de vigencia de la póliza, de la obligación de indemnizar a un tercero los daños causados por un hecho previsto en el artículo 1 de estas Condiciones.

2. No obstante lo dispuesto en esta cláusula, la cobertura del Asegurador no comprenderá los siniestros en los que, aun habiendo nacido a cargo del Asegurado la obligación de indemnizar durante la vigencia de la póliza, no se hubiera formulado la correspondiente reclamación por el perjudicado, dentro de un período de tiempo, pactado entre las partes, subsiguiente a la terminaciónde la última de las prórrogas del contrato o, en su defecto, del período de duración.

Este período, queda a elección del Asegurado y, podrá ser de uno, dos o cinco años, haciéndose constar expresamente en las Condiciones Particulares.

Dicho período será en todo caso de CINCO AÑOS en los supuestos en que la terminación de los efectos del contrato, se deba al fallecimiento del Corredor o al cese o renuncia de la actividad de Correduría, pero siempre que el nacimiento de la obligación a indemnizar haya tenido lugar durante la vigencia de la Póliza.

ARTÍCULO 4.-UNIDAD DE SINIESTRO.

1. A los efectos de este seguro, se considerará como un solo y único siniestro.

a) El conjunto de reclamaciones que se deriven de un mismo hecho siniestral, acción u omisión de carácter profesional, cualesquiera que sea el número de reclamantes.

b) Todas las reclamaciones que tengan su origen en una misma causa, aunque se trate de hechos aislados, sucesivos, repetidos o continuados, aun cuando eventualmente puedan realizarse en forma interrumpida.

c) El conjunto de consecuencias resultantes de varias acciones u omisiones atribuidos a un mismo hecho.

2. Se considerará como fecha de siniestro la del momento en que se haya realizado el hecho generador, acción u omisión lesiva, del que el Asegurado pudiera resultar responsable civil.

Todas las reclamaciones derivadas del mismo hecho, tal y como se definen en el punto anterior, se reconducirán a la fecha de siniestro expresada en el párrafo precedente.

3. Solamente en el caso de que no fuera posible identificar el momento en el que se hubiera incurrido en la acción u omisión lesiva, se considerará como fecha del siniestro la de la recepción por el Asegurador de la primera reclamación o notificación fehaciente del Asegurado o del perjudicado de cualquier hecho o circunstancia de la que pudieran traducirse responsabilidades civiles a título de resarcimiento.

ARTÍCULO 5.-LÍMITE POR PERÍODO DE SEGURO.

1. La responsabilidad máxima del Asegurador no sobrepasará la cuantía de la suma asegurada fijada en las Condiciones Particulares para el conjunto de todos y cada uno de los siniestros que sean objeto de cobertura dentro del mismo período de seguro.

2. El hecho de que varias reclamaciones resultantes de una misma actuación profesional se desarrollen a lo largo de diferentes períodos de seguro, no supondrá en modo alguno la acumulación de las sumas aseguradas por el período respectivo, de forma que la responsabilidad máxima del Asegurador nunca sobrepasará la cuan- tía fijada por siniestro y período de seguro.

ARTÍCULO 6.-ÁMBITO GEOGRÁFICO Y JURISDICCIÓN.

Son objeto de la presente cobertura, las actividades de mediación, realizadas en territorio español y sometidas a la normativa española en vigor reguladora de las operaciones de seguro.

Las reclamaciones judiciales formuladas por el perjudicado por actividades de mediación negligentes productoras de daños, sólo serán admisibles a los efectos de esta póliza, si fuesen reclamadas procesalmente ante los Tribunales de Justicia españoles, o bien se tratase de resoluciones reconocidas por éstos, provenientes de Tribunales de los Estados Miembros de la Unión Europea.

ARTÍCULO 7.- BASES DEL CONTRATO

La solicitud y el cuestionado cumplimentados por el Tomador del Seguro, así como la proposición del Asegurador, en su caso, en unión de esta póliza, constituyen un todo unitario, fundamento del seguro, que sólo alcanza, dentro de los límites pactados, a los bienes y riesgos especificados en la misma. Si el contenido de la póliza difiere de la proposición de seguro o de las cláusulas acordadas, el Tomador del Seguro podrá reclamar al Asegurador, en el plazo de un mes a contar desde la entrega de la póliza, para que subsane la divergencia existente. Transcurrido dicho plazo sin efectuar la reclamación, se estará a lo dispuesto en la póliza.

DECLARACIONES SOBRE EL RIESGO

ARTÍCULO 8.-AL EFECTUAR EL SEGURO Y DURANTE SU VIGENCIA.

1. La presente póliza ha sido concertada sobre la base de las declaraciones formula- das por el Tomador del Seguro en el cuestionado que le ha sometido el Asegurador, que han motivado la aceptación del riesgo por el Asegurador, la asunción por su parte de las obligaciones para él derivadas del contrato y la fijación de la prima.

El Tomador del seguro o Asegurado quedarán exonerados de tal deber si el Asegurador no le somete cuestionario o cuando, aun sometiéndoselo, se trate de circunstancias que puedan influir en la valoración del riesgo y que no estén comprendidas en él.

2. El Tomador del seguro o el Asegurado deberán, durante el curso del contrato, comunicar al Asegurador, tan pronto como le sea posible, las circunstancias que agraven el riesgo, así como el acontecimiento de cualquier hecho, conocido por aquéllos, que pueda agravarlo o variarlo, y sean de tal naturaleza que si hubieran sido conocidas por éste en el momento de la perfección del contrato no lo habría celebrado o lo habría concluido en condiciones más gravosas.

ARTÍCULO 9.-DEBER DE COMUNICAR LA EXISTENCIA DE OTRAS PÓLIZAS.

El Tomador del Seguro o el Asegurado quedan obligados, salvo pacto en contrario, a comunicar anticipadamente al Asegurador la existencia de otras pólizas, contratadas con distintos Aseguradores, cubriendo los efectos que un mismo riesgo puede producir sobre el mismo interés y durante idéntico.

ARTÍCULO 10.-FACULTADES DEL ASEGURADOR EN CASO DE AGRAVACIÓN DEL RIESGO.

1. En caso de que durante la vigencia de la póliza le fuese comunicado al Asegurador una agravación del riesgo, éste puede proponer una modificación de las condiciones del contrato en un plazo de dos meses a contar desde el día en que la agravación le haya sido declarada. En tal caso, el Tomador del Seguro dispone de quince días, a contar desde la recepción de esta proposición, para ser aceptada o rechazada. En caso de rechazo, o de silencio, el Asegurador puede, transcurrido dicho plazo, rescindir el contrato previa advertencia al Tomador del Seguro, dándole para que conteste, un nuevo plazo de quince días, transcurridos los cuales y dentro de los ocho siguientes, comunicará al Tomador del Seguro la rescisión definitiva.

2. El Asegurador podrá, igualmente, rescindir el contrato comunicándolo por escrito al Asegurado dentro de un mes, a partir del día en que tuvo conocimiento de la agravación del riesgo.

3. Si sobreviniera un siniestro sin haberse realizado declaración de agravación del riesgo, el Asegurador queda liberado de su prestación, si el Tomador o el Asegurado ha actuado con mala fe. En otro caso, la prestación del Asegurado se reducirá proporcionalmente a la diferencia entre la prima convenida y la que se hubiera aplicado de haberse conocido la verdadera entidad del riesgo.

4. En el caso de agravación del riesgo durante el tiempo del seguro que dé lugar a un aumento de prima, cuando por esta causa queda rescindido el contrato, si la agravación es imputable al Asegurado, el Asegurador hará suya en su totalidad la prima cobrada. Siempre que dicha agravación se hubiera producido por causas ajenas a la voluntad del

Asegurado, éste tendrá derecho a ser reembolsado de la parte de la prima satisfecha correspondiente al período que falte por transcurrir de la anualidad en curso.

ARTÍCULO 11.-CONSECUENCIAS DE LA RESERVA O INEXACTITUD DE LAS DECLARACIONES.

1. El Asegurador podrá rescindir el contrato mediante declaración dirigida al Tomador del Seguro, en el plazo de un mes, a contar del conocimiento de la reserva o inexactitud del Tomador del Seguro. Desde el momento mismo en que el Asegurador haga esta declaración, quedarán de su propiedad las primas correspondientes al período en curso, salvo que concurra dolo o culpa grave por su parte.

2. Si el siniestro sobreviniese antes de que el Asegurador hubiese hecho la declaración a que se refiere el número anterior, la prestación de éste se reducirá en la misma proporción existente entre la prima convenida en la póliza y la que corresponda de acuerdo con la verdadera entidad del riesgo. Cuando la reserva o inexactitud se hubiese producido mediante dolo o culpa grave del Tomador del Seguro, el Asegurador quedará liberado del pago de la prestación.

ARTÍCULO 12.-EN CASO DE DISMINUCIÓN DEL RIESGO.

1. El Tomador del seguro o el Asegurado podrán, durante el curso del contrato, poner en conocimiento del Asegurador todas las circunstancias que disminuyan el riesgo y sean de tal naturaleza que si hubieran sido conocidas por éste en el momento de la perfección del contrato, lo habría concluido en condiciones más favorables para el Tomador del Seguro.

2. En tal caso, al finalizar el período en curso cubierto por la prima, el Asegurador deberá reducir el importe de la prima futura en la proporción correspondiente, teniendo derecho el Tomador del Seguro, en caso contrario, a la resolución del contrato y a la devolución de la diferencia entre la prima satisfecha y la que le hubiera correspondido pagar, desde el momento de la puesta en conocimiento de la disminución del riesgo.

PERFECCIÓN, EFECTOS DEL CONTRATO Y DURACIÓN DEL SEGURO

ARTÍCULO 13.-PERFECCIÓN.

El contrato se perfecciona por el consentimiento, manifestado por la suscripción de la póliza o del documento provisional de cobertura por las partes contratantes. La cobertura contratada y sus modificaciones o adiciones no tomarán efecto, mientras no haya sido satisfecho el recibo de prima, salvo pacto en contrario en Condición Particular.

En caso de demora en el cumplimiento de ambos requisitos, las obligaciones del Asegurador comenzarán a las veinticuatro horas del día en que hayan sido completados.

ARTÍCULO 14.-EFECTO DEL CONTRATO.

Las garantías de la póliza entran en vigor en la hora y fecha indicadas en las Condiciones Particulares.

ARTÍCULO 15.-DURACIÓN DEL SEGURO.

La duración del contrato será la establecida en las Condiciones Particulares.

A la expiración del período indicado en las Condiciones Particulares de esta póliza, se entenderá prorrogada por el plazo de un año, y así sucesivamente a la expiración de cada anualidad.

Las partes podrán oponerse a la prórroga del contrato mediante una notificación escrita a la otra parte, efectuada con un plazo de dos meses de anticipación a la conclusión del período de seguro en curso.

ARTÍCULO 16.-EXTINCIÓN DEL SEGURO.

Si durante la vigencia del seguro se produjera la desaparición del interés asegurado, desde este momento el contrato del seguro quedará extinguido y el Asegurador tiene el derecho de hacer suya la prima no consumida.

PAGO DE LA PRIMA

ARTÍCULO 17.-TIEMPO DE PAGO.

El Tomador del Seguro está obligado al pago de la primera prima o de la prima

única en el momento de la perfección del contrato. Las sucesivas primas se deberán hacer efectivas en los correspondientes vencimientos.

ARTÍCULO 18.-LUGAR DE PAGO.

Cuando en las Condiciones Particulares se pacta la domiciliación bancada, se aplicarán las siguientes normas:

1. El obligado al pago de la prima entregará al Asegurador carta dirigida al Establecimiento bancado o caja de ahorros, dando la orden oportuna al efecto.

2. La prima se entenderá satisfecha a su vencimiento, salvo que intentado el cobro dentro del plazo de gracia de un mes, no existiesen fondos suficientes en la cuenta del obligado a pagarla. En este caso el Asegurador notificará al tomador o al Asegurado que tiene el recibo a su disposición en el domicilio de dicha Entidad aseguradora, y aquél vendrá obligado a satisfacer la prima en dicho domicilio. Transcurrido el plazo de un mes desde el Vencimiento sin haberse efectuado el pago, el seguro quedará en suspenso.

3. Si el Asegurador dejase transcurrir el plazo de gracia sin presentar el recibo al cobro y, al hacerlo después, no existiesen fondos suficientes en la cuenta, deberá notificar tal hecho al obligado a pagar la prima, por carta certificada o un medio indubitado, concediéndole un nuevo plazo de un mes para que pueda satisfacer su importe en el domicilio, sucursal o agencia del Asegurador, computándose el plazo desde la recepción de la expresada carta o notificación en el último domicilio comunicado a la Compañía. Transcurrido el plazo de un mes desde la indicada fecha sin haberse efectuado el pago, el seguro quedará en suspenso.

ARTÍCULO 19.-CONSECUENCIAS DEL IMPAGO DE PRIMAS.

1. Si, por culpa del Tomador del Seguro, la primera prima no ha sido pagada, o la prima única no lo ha sido a su vencimiento, el Asegurador tiene derecho a resolver el contrato o a exigir el pago de la prima debida en vía ejecutiva con base en la póliza. En todo caso, y salvo pacto en contrario en Condición Particular, si la prima no ha sido pagada antes de que se produzca el siniestro, el Asegurador quedará liberado de su obligación.

2. En caso de falta de pago de una de las primas siguientes, la cobertura del Asegurador queda suspendida un mes después del día de su Vencimiento. Si el Asegurador no reclama el pago dentro de los seis meses siguientes al vencimiento de la prima, se entenderá que el contrato queda extinguido. El impago de la prima y la subsiguiente extinción del contrato no modificará lo establecido en el artículo 30 de la presente Póliza. Se considerará como fecha de vencimiento de las primas que procedan de las liquidaciones que practiquen en su caso, el día en que le sea presentado el correspondiente recibo de la prima al Tomador del seguro.

3. En cualquier caso, el Asegurador, cuando el contrato esté en suspenso, sólo podrá exigir el pago de la prima del período en curso.

4. Si el contrato no hubiere sido resuelto o extinguido conforme a los párrafos anteriores, la cobertura vuelve a tener efecto a las veinticuatro horas del día en que el Tomador pagó su prima.

SINIESTROS-TRAMITACIÓN

ARTÍCULO 20.-OBLIGACIÓN DE COMUNICAR EL SINIESTRO.

1. El Tomador del Seguro o el Asegurado deberá comunicar al Asegurador el acaecimiento del siniestro dentro del plazo máximo de siete días de haberlo conocido, salvo que se haya fijado en la póliza un plazo más amplio. En caso de incumplimiento, el Asegurador podrá reclamar los daños y perjuicios causados por la falta o retraso en la tramitación.

2. En caso de existir varios Aseguradores, esta comunicación deberá hacerse a cada uno de ellos, con indicación del nombre de los demás.

ARTÍCULO 21.-DEBER DE INDICAR CIRCUNSTANCIAS Y CONSECUENCIAS DEL SINIESTRO.

El Tomador del Seguro o el Asegurado deberá, además, dar al Asegurador toda clase de informaciones sobre las circunstancias y consecuencias del siniestro. En caso de violación de este deber el rehúse del siniestro sólo se producirá en el supuesto de que hubiese concurrido dolo o culpa grave.

ARTÍCULO 22.-DEBER DE AMINORAR LAS CONSECUENCIAS.

1. El Asegurado y el Tomador del Seguro vendrán obligados a adoptar todas las medidas que favorezcan su defensa frente a las reclamaciones de responsabilidad, debiendo mostrarse tan diligente en su cumplimiento como si no existiera seguro. Comunicará al Asegurador inmediatamente de su recepción cualquier notificación judicial o administrativa que llegue a su conocimiento y que pueda estar relacionada con el siniestro.

2. El incumplimiento de estos deberes facultará al Asegurador para reducir la prestación haciendo partícipe al Asegurado en el siniestro, en la medida en que con su comporta- miento haya agravado las consecuencias económicas del siniestro, o en su caso, a recla-marle daños y perjuicios.

3. Si el incumplimiento del Tomador del seguro o del Asegurado se produjera con la manifiesta intención de perjudicar o de engañar al Asegurador o si obrasen dolosamente en connivencia con los reclamantes o con los damnificados, el Asegurador quedará liberado de toda prestación derivada del siniestro.

ARTÍCULO 23.-DEFENSA DEL ASEGURADO.

1. Salvo pacto en contrario, en cualquier procedimiento judicial que se deduce de un siniestro amparado por la póliza, el Asegurador asumirá, a sus expensas, la dirección jurídica frente a la reclamación del perjudicado, designando los letrados y procuradores que defenderán y representarán al Asegurado en las actuaciones judiciales que se le siguiesen en reclamación de responsabilidades civiles cubiertas por esta póliza, y ello aun cuando dichas reclamaciones fuesen infundadas.

2. El Asegurado deberá prestar la colaboración necesaria a dicha defensa, compro- metiéndose a otorgar los poderes y la asistencia personal que fuesen precisos.

3. La prestación de defensa y representación en causas criminales será potestativa del Asegurador, salvo que, en la póliza se haya pactado lo contrario.

4. Sea cual fuere el fallo o resultado del procedimiento judicial, el Asegurador se reserva la decisión de ejercitar los recursos legales que procedieren contra dicho fallo o resultado, o el conformarse con el mismo.

5. Si el Asegurador estima improcedente el recurso, lo comunicará al Asegurado, quedando éste en libertad para interponerlo por su exclusiva cuenta y aquél obligado a reembolsarle los gastos judiciales y los de abogado y procurador, en el supuesto de que dicho recurso prosperase.

6. Cuando se produjera algún conflicto entre el Asegurado y el Asegurador motivado por tener que sustentar éste en el siniestro intereses contrarios a la defensa del Asegurado, el Asegurador lo pondrá en conocimiento del Asegurado, sin perjuicio de realizar aquellas diligencias que, por su carácter urgente, sean necesarias para la defensa. En este caso, el Asegurado podrá optar entre el mantenimiento de la dirección jurídica por el Asegurador o confiar su propia defensa a otra persona. En este último caso, el Asegurador quedará obligado a abonar los gastos de tal dirección jurídica hasta el límite pactado en la póliza.

SINIESTROS-PAGO DE LA INDEMNIZACIÓN

ARTÍCULO 24.-PAGO DE LA INDEMNIZACIÓN.

El Asegurador, dentro de los límites y condiciones de la póliza, abonará la indemnización, en el plazo máximo de 5 días a partir de la fecha en que el importe de dicha indemnización haya sido fijada por sentencia firme o haya sido determinada por reconocimiento de responsabilidad hecho por el Asegurador.

ARTÍCULO 25.-CONCURRENCIA DE SEGUROS.

1. Si existen varios seguros el Asegurador contribuirá al abono de la indemnización en proporción a la propia suma asegurada, sin que pueda superarse la cuantía del daño. Dentro de este límite el Asegurado puede pedir a cada Asegurador la indemnización debida, según el respectivo contrato.

2. Si por dolo se hubiera omitido esta declaración, el Asegurador no está obligado al pago de la indemnización.

ARTÍCULO 26.-SUBROGACIÓN.

1. Una vez pagada la indemnización y sin que haya necesidad de ninguna otra cesión, traslado, título o mandato, el Asegurador queda subrogado en todos los derechos, recursos y acciones del Asegurado, contra todos los autores o responsables del siniestro, y aun contra otros aseguradores, si los hubiese, hasta el límite de la indemnización, siendo el Asegurado responsable de los perjuicios que con sus actos u omisiones pueda causar al Asegurador en su derecho a subrogarse. No podrá en cambio el Asegurador ejercitar en perjuicio del Asegurado los derechos en que se haya subrogado.

2. El Asegurador no tendrá derecho a la subrogación contra ninguna de las personas cuyos actos u omisiones den origen a responsabilidad del Asegurado, de acuerdo con la Ley, ni contra el causante del siniestro que sea, respecto del Asegurado, pariente en línea directa o colateral dentro del tercer grado civil de consanguinidad, padre adoptante o hijo adoptivo que convivan con el Asegurado. Pero esta norma no tendrá efecto si la responsabilidad proviene de dolo o si la responsabilidad de los mismos está amparada por un contrato de seguro. En este ultimo supuesto, la subrogación estará limitada en su alcance de acuerdo con los términos de dicho contrato.

3. En caso de concurrencia del Asegurador y Asegurado frente a tercer responsable, el recobro obtenido se repartirá entre ambos, en proporción a su respectivo interés.

ARTÍCULO 27.-REPETICIÓN DEL ASEGURADOR CONTRA EL ASEGURADO.

El Asegurador podrá repetir contra el Asegurado por el importe de las indemnizaciones que haya debido satisfacer como consecuencia del ejercicio de la acción directa por el perjudicado o sus derechohabientes cuando el daño o perjuicio causado a tercero sea debido a conducta dolosa del Asegurado.

ARTÍCULO 28.-RECLAMACIÓN DE DAÑOS Y PERJUICIOS AL ASEGURADO O AL TOMADOR DEL SEGURO.

El Asegurador podrá igualmente reclamar los daños y perjuicios que le hubiese causado el Asegurado o el Tomador del Seguro en los casos y situaciones previstos en la póliza, y/o exigirle el reintegro de las indemnizaciones que hubiese tenido que satisfacer a terceros perjudicados por siniestros no amparados por el seguro.

ARTÍCULO 29.-PRESCRIPCIÓN.

Las acciones derivadas del contrato prescriben a los dos años a contar desde el día en que pudieron ejercitarse.

ARTÍCULO 30.-ARBITRAJE.

Si las dos partes estuviesen de acuerdo, podrán someter sus diferencias al juicio de [Nº DE ÁRBITROS]

árbitros de conformidad con la legislación vigente.

ARTÍCULO 31.-COMPETENCIA.

Será tribunal competente para el conocimiento de las acciones derivadas del contrato de seguro el del domicilio de Asegurado, siendo nulo cualquier otro pacto en contrario.

ARTÍCULO 32.-DOMICILIO A EFECTO DE LAS COMUNICACIONES.

1. Las comunicaciones dirigidas al Asegurador se realizarán en el domicilio social del mismo o en el de la delegación señalado en la póliza, o a través del agente de aquél.

2. Las comunicaciones del Asegurador al Tomador del Seguro y, en su caso, al Asegurado se realizarán en el domicilio de éstos recogidos en la póliza, salvo que los mismos hayan notificado fehacientemente al Asegurador el cambio de su domicilio.

ARTÍCULO 33.-CLÁUSULA DE COASEGURO.

El presente contrato de seguro se establece en régimen de coaseguro, en los términos previstos en el párrafo 10 del artículo 33 de la Ley 50/1980, de 8 de octubre, de Contrato de Seguro, sin que exista vínculo alguno de solidaridad, respondiendo cada coasegurador por sí y no por los demás, en proporción a la cuota que a cada uno corresponda y que figura al final de la presente cláusula.

La Entidad abridora de la póliza extenderá un único recibo de prima por la totalidad de las participaciones, delegando en la Agrupación de Interés Económico AGRUPACIÓN DEL CONVENIO, RC CORREDORES, AIE la gestión de su cobro y teniendo su pago plenos efectos liberatorios para el Tomador del Seguro.

Con objeto de facilitar y simplificar las relaciones del Tomador del Seguro con las coaseguradoras, la entidad abridora de la póliza representará al resto de éstas en sus relaciones con aquél. En consecuencia, el Tomador del Seguro podrá dirigir sus declaraciones y reclamaciones exclusivamente a esa entidad, pero sin que ello suponga, en modo alguno, la posibilidad de que le sean exigibles las responsabilidades que a las demás coaseguradoras correspondan por sus respectivas participaciones.

La tramitación y liquidación de siniestros se llevará a cabo por la citada Agrupación de Interés Económico, que administra los intereses de los suscriptores del Convenio de Suscripción de Riesgos de Responsabilidad Civil de Corredores de Seguros, quien queda facultada para la eventual anulación de la póliza. A tal efecto, la entidad abridora notificará a la Agrupación la ocurrencia del siniestro y le dará traslado, a la mayor brevedad, de la documentación necesaria para ello, prestando su colaboración en la referida tramitación y liquidación.

CUADRO DE COASEGURO AÑO [AÑO]

Entidad AseguradoraParticipación %

AZX UNIÓN ASEGURADORA

AGY SEGUROS

TOTAL 100%

El abajo firmante, como Asegurado y profesional del Seguro, declara haber leído, entendido y comprendido en todos sus términos las presentes Condiciones, de las que recibe un ejemplar y, en prueba de aceptación expresa de las mismas, y en particular de las cláusulas limitativas que se hallan destacadas, firma ésta y las páginas anteriores.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo

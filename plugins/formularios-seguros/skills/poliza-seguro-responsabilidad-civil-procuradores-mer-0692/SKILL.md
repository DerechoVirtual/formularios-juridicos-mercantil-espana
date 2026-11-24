---
name: poliza-seguro-responsabilidad-civil-procuradores-mer-0692
description: "Póliza de seguro de responsabilidad civil de procuradores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Póliza de seguro de responsabilidad civil de procuradores

> Formulario **MER-0692** del plugin **Seguros: pólizas, coberturas y reclamaciones** (`formularios-seguros`) · Mercantil › Seguros · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Póliza de seguro de responsabilidad civil de procuradores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Póliza de seguro de responsabilidad civil de procuradores” para mi caso». También puedes invocarla directamente con `/formularios-seguros:poliza-seguro-responsabilidad-civil-procuradores-mer-0692`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguros:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguros: pólizas, coberturas y reclamaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (6 veces)
- [ ] IMPORTE (4 veces)
- [ ] CALLE (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] SUPUESTOS CUBIERTOS

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

Ramo: 07 R. CIVIL

CONDICIONES PARTICULARES

Modalidad: DAÑOS PATRIMONIALES PÓLIZA NÚM. Agente:

Localidad: Fecha Emisión:

Tomador del seguro. Nombre:

Domicilio: C/ [CALLE], NÚM [NÚMERO] CP: Localidad: NIF:

Asegurado.

Nombre:

Domicilio: C/ [CALLE], NUM [Nº] CP.: Localidad:

Fecha de efecto: a las 00 horas.

Fecha de vencimiento: a las 00 horas. Duración del seguro: AÑOS PRORROGABLES Forma de Pago: ANUAL

Recibo de prima emitido por el período del [Nº] al [Nº]

*PRIMA NETA FNGConsorcioIMPUESTOSREC. EXTERNOTotal recibo

Recibos sucesivos por una prima neta de [IMPORTE] euros, más los impuestos y los recargos vigentes en cada momento.

DESCRIPCIÓN DEL RIESGO

Responsabilidad Civil del Tomador del Seguro, en el ejercicio libre de su Profesión como PROCURADOR.

SITUACIÓN DEL RIES GO

C/ [CALLE], NÚM [NÚMERO]

DELIMITACIÓN GEOGRÁFICA DE LA COBERTURA Territorio Nacional

────────────────────

PÓLIZA NÚM. [Nº]

CONDICIONES ESPECIALES PARA DAÑOS PATRIMONIALES PRIMARIOS INCLUIDO

Responsabilidad profesional que pueda derivarse para el Asegurado, de acuerdo con las leyes vigentes, por daños patrimoniales primarios causados involuntariamente a clientes o terceros por hechos que derivan de errores profesionales en que pueda incurrir el Asegurado en el ejercicio libre de su actividad profesional, tal como dicha profesión venga regulada en los estatutos, disposiciones y reglamentos vigentes.

Se entiende por daños patrimoniales primarios aquellos menoscabos o perjuicios patrimoniales que sufran clientes o terceros como consecuencia de los mencionados errores profesionales y que no sean reducibles a un daño personal, material o consecuencias de éstos.

Además:

- Daños materiales, pérdidas o extravío que puedan sufrir los expedientes o documentos que se encuentran en poder del Asegurado para el desarrollo de la gestión encomendada.

- Responsabilidad por actos del personal a su servicio.

- Responsabilidad directamente exigible al personal del Asegurado en el ejercicio de los cometidos encomendados por el mismo dentro del ámbito de su profesión.

EXCLUIDO

- Reclamaciones derivadas de daños personales.

- Reclamaciones derivadas de daños materiales, a excepción de los daños a expedientes y documentos especificados más arriba.

- Pérdida o extravío, de dinero, signos pecuniarios, y en general, valores y efectos al portador o a la orden endosados en blanco.

- Reclamaciones derivadas de daños morales que no trasciendan a la esfera patrimonial del perjudicado.

- Reclamaciones presentadas ante Tribunales extranjeros; las derivadas de infracción o inobservancia del Derecho extranjero; las derivadas de una actividad profesional realizada en el extranjero.

- Reclamaciones que, en base a promesas o pactos especiales, vayan más allá del mbito de la responsabilidad civil legal.

- Reclamaciones derivadas de sobrepasar presupuestos a créditos; mediación o recomendación, tanto a título oneroso como gratuito, de negocios pecuniarios, de inmuebles o de otras transacciones comerciales.

- Reclamaciones por faltas en caja, errores en pagos, infidelidad de los propios empleados del Asegurado.

- Reclamaciones por quebrantamiento del secreto profesional.

- Reclamaciones por calumnia o injuria.

- Reclamaciones por haber ocasionado el daño a consecuencia de haberse desviado a sabiendas de la ley, disposiciones, instrucciones o condiciones de los clientes o de personas autorizadas por ellos o por cualquier infracción del deber profesional hecha a sabiendas.

- Reclamaciones de socios, empleados y familiares del Asegurado, considerando como familiares del mismo al cónyuge, a los parientes por línea directa, ascendente o descendente, colaterales o afines hasta el segundo grado.

- Reclamaciones derivadas de la actividad del Asegurado como director, consejero o ejecutivo de empresas privadas, asociaciones o clubs, o como síndico o administrador de empresas.

- Responsabilidad de aquellas personas que no tengan con el asegurado relación de dependencia laboral, aun cuando actúen para y por cuanta de él.

Delimitación temporal de la cobertura

Daños ocurridos durante el período de vigencia del seguro por errores profesionales cometidos durante ese mismo período cuyas consecuencias sean reclamadas al Asegurado o a la Compañía, de manera fehaciente durante la vigencia de la póliza en el plazo máximo de dos años naturales, contados a partir de la terminación de la misma.

Suma asegurada y siniestros en serie

La suma asegurada representa la cantidad máxima que el Asegurador se compromete a satisfacer por SINIESTRO Y ANUALIDAD de seguro.

Para daños a expedientes y documentos, el límite máximo de prestación por el Asegurador quedará limitado a [IMPORTE] euros ( euros) por siniestro y anualidad de seguro.

Siniestros en serie: A efectos del Seguro, se considerarán como un mismo siniestro: El conjunto de reclamaciones originadas por una misma causa o evento siniestral, cualquiera que sea el número de reclamantes independientemente de que la reclamación se dirija exclusivamente contra el Asegurado o, conjunta a separadamente con él, contra las personas de las que tenga que responder.

El conjunto de las consecuencias de varios errores profesionales cometidos en un mismo acto.

El conjunto de las consecuencias de varias acciones derivadas de la misma o de igual fuente de error si los asuntos tratados profesionalmente por el Asegurado guardaren entre sí una dependencia jurídica o económica.

Defensa civil y fianzas

Se garantiza el pago de los gastos judiciales ocasionados con motivo de la celebración de procesos seguidos contra el asegurado o sus empleados en el ejercicio de su actividad profesional. La cobertura queda limitada a gastos derivados de:

- La defensa del Asegurado o de sus empleados por los Abogados y Procuradores.

- Las restantes costas procesales.

- La constitución de las fianzas que les fueran exigidas para asegurar sus posibles responsabilidades civiles declaradas en el posterior juicio.

- El límite máximo de estos gastos judiciales está representado por las sumas máximas de cobertura concertadas para la garantía principal del presente contrato.

Propiedad y/o usufructo bufete-despacho

Responsabilidad como ocupante o propietario del local en la parte en que está destinada a despacho o bufete del Asegurado, así como la que resulte del funcionamiento de sus instalaciones o máquinas. Cuando exista propiedad horizontal, se incluye asimismo, la prorrata que corresponda a estos locales en la responsabilidad civil de la comunidad de propietarios de la que formen parte, haciéndose extensiva a los daños producidos por incendio, explosión y/o agua cuando estos riesgos tengan su origen en el domicilio en que se encuentra el despacho o bufete.

PÓLIZA NÚM. [Nº]

INCLUIDO

CONDICIONES ESPECIALES PARA PROCURADORES

En general

Responsabilidad en que puede incurrir el profesional en el ejercicio libre e independiente de la Procuraduría encargándose mediante apoderamiento conferido de representar los derechos e intereses de su poderdante ante los Tribunales de Justicia.

EN PARTICULAR por [SUPUESTOS CUBIERTOS]

- Transmitir el Abogado elegido por su cliente o por ellos mismos los documentos, antecedentes e instrucciones que les remitan, o que ellos mismos puedan adquirir.

- Pagar los gastos que se causaren a su instancia.

- Tener el cliente y al letrado al corriente del curso del negocio que se les hubiera confiado.

- Firmar las pretensiones que se presenten a nombre del cliente.

- Oír y firmar los emplazamientos, citaciones y notificaciones de cualquier clase, incluidas de sentencias.

- Asistir a las diligencias y actos para los que las Leyes lo prevengan.

- Dar a sus clientes cuentas documentadas de los gastos judiciales a inversión de las cantidades recibidas.

- La llevanza del libro registro de conocimiento de asuntos. Además:

- Pérdida o extravío de dinero recibido de sus clientes a cuenta de los gastos judiciales u otros que se causaren con motivo del mandato recibido.

EXCLUIDO

- Anuncio o difusión de servicios profesionales, directamente o a través de cualquier medio publicitario.

- Responsabilidad derivada de escritos firmados por Letrados.

- Ejercicio de la función judicial a fiscal, así como el desempeño del LAJ de los

Tribunales, o función auxiliar o subalterna en los mismos

- Ejercicio de la Abogacía, salvo en los casos de habilitación previstos en el Estatuto.

- Ejercicio de la profesión de Agente de Negocios o Gestor Administrativo y Agente de la Propiedad Inmobiliaria, o cualquiera otra profesión que hubiera sido declarada incompatible con el ejercicio de la Procuraduría.

- Cualquier empleo en los Colegios de Procuradores y Abogados.

- Otras funciones o empleos de la Administración legalmente incompatibles con la

Procuraduría.

- Pérdida de la fianza constituida por el Asegurado en garantía a su actividad profesional cuando ésta se refiera a descubiertos fiscales que graven su trabajo personal, cuotas o cargas colegiales, multas y similares.

- Errores profesionales cometidos traspasando los límites del mandato, o bien por no arreglarse a las instrucciones del mandante (salvo que, al no haber instrucciones o ser éstas insuficientes, hubiese actuado de acuerdo a la naturaleza o índole del negocio).

TOMO II

Garantías complementarias aseguradas

INCLUIDO

Defensa de la responsabilidad criminal

- La defensa del Asegurado por los abogados y procuradores designados o autorizados por el Asegurador en los procesos criminales que se le siguieran con ocasión del desarrollo de las actividades descritas en la póliza, aun después de liquidadas las responsabilidades civiles.

- La constitución de fianzas que en causa criminal le fueran exigidas para asegurar su libertad provisional.

- El pago de los gastos judiciales. EXCLUIDO

- El pago de sanciones o multas.

- La defensa en procesos seguidos fuera del territorio nacional.

Los pagos que daba realizar el Asegurador en virtud de esta cobertura, sumados al resto de las cantidades que daba satisfacer por el mismo siniestro, no podrán sobrepasar el límite de garantía establecido en la póliza.

PÓLIZA NÚM. [Nº]

CLÁUSULAS

Franquicia de daños patrimoniales primarios

De conformidad con el apartado 1.2 del artículo primero de las Condiciones Generales de la Póliza, se establecen las siguientes franquicias:

En cada siniestro, el [PORCENTAJE] % de su importe, mínimo de [IMPORTE] euros y máximo de [IMPORTE] euros

En el supuesto de producirse daños a expedientes o documentos, asumirá el Asegurado el [PORCENTAJE] % del importe del siniestro.

La aplicación de las franquicias establecidas en los apartados anteriores se efectuará sobre la cantidad resultante de deducir, del importe de la reclamación, una suma equivalente al monto de los honorarios que correspondan a la realización de la actividad profesional en que se produjo el error origen del daño. Dicho deducción se efectuará aun cuando en el importe de la reclamación no estuviesen comprendidos los honorarios mencionados.

El Asegurado no podrá llevar a cabo, sin consentimiento expreso del Asegurador, ningún tipo de acción cuya finalidad sea conseguir que la sea condonada, reducida o devuelta total o parcialmente la franquicia. El incumplimiento de esta obligación dará lugar a la reducción de la indemnización en la cantidad correspondiente.

El Asegurado se compromete a no cubrir la franquicia establecida en los apartados anteriores por ningún otro seguro. El incumplimiento de esta obligación dará lugar a la rescisión del contrato, así como la pérdida de los derechos que del mismo se derivan.

Cláusula para la regularización de prima

La Prima Neta de la presente póliza tiene carácter de prima mínima provisional, comprometiéndose el Tomador del Seguro a facilitar al Asegurador la cifra real de:

- Honorarios.

Para regularizar en base a aplicar sobre dicha cifra la TASA DE REGULARIZACIÓN indicada en póliza y, en su caso, proceder el cobro del exceso de prima que pudiera corresponder.

- TASA DE REGULARIZACIÓN: ……%.

Las presentes Condiciones Particulares y Generales, junto con la Solicitud-Cuestionario, formen en su conjunto el contrato de Seguro.

EL TOMADOR DEL SEGURO HACE CONSTAR:

QUE RECIBE Y CONOCE LAS CONDICIONES GENERALES DE LA PÓLIZA DE SEGURO DE RESPONSABILIDAD CIVIL POR DAÑOS CAUSADOS A TERCEROS MO- DELO A3243N.

EN LAS QUE FIGURAN DESTACADAS LAS CLÁUSULAS LIMITATIVAS DE LOS DERECHOS DEL ASEGURADO Y CON LA FIRMA DEL PRESENTE DOCUMENTO MUES- TRA SU CONFORMIDAD Y ACEPTACIÓN.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Hecho en PALENCIA en la fecha de emisión que se indica anteriormente

EL TOMADOR DEL SEGURO/ASEGURADO	EL ASEGURADOR

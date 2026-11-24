---
name: demanda-accion-social-responsabilidad-administrador-mer-0809
description: "Demanda de acción social de responsabilidad de un administrador-socio contra otro administrador. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de acción social de responsabilidad de un administrador-socio contra otro administrador

> Formulario **MER-0809** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario en la que un socio y administrador solidario ejercita la acción social de responsabilidad (arts. 236, 238 y 239 TRLSC) contra otro administrador, cuando la junta convocada al efecto no ha aprobado ejercitar la acción por el voto contrario del propio demandado y el demandante ostenta más del 5 % del capital.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de acción social de responsabilidad de un administrador-socio contra otro administrador» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de acción social de responsabilidad de un administrador-socio contra otro administrador” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-accion-social-responsabilidad-administrador-mer-0809`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] IMPORTE (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (3 veces)
- [ ] PORCENTAJE DE CAPITAL (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] COLEGIO DE ABOGADOS
- [ ] DATOS REGISTRALES
- [ ] DENOMINACIÓN SOCIAL DE LA CONTRAPARTE
- [ ] DENOMINACIÓN SOCIAL DEL BENEFICIARIO DE LOS PAGOS
- [ ] DESCRIPCIÓN DEL ENCARGO
- [ ] DESTINO DE LOS FONDOS
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] DOMICILIO PROFESIONAL
- [ ] DOMICILIO SOCIAL
- [ ] ENTIDAD BANCARIA
- [ ] IMPORTE DEL CONTRATO
- [ ] IMPORTE DEL DAÑO EMERGENTE
- [ ] IMPORTE EN LETRA
- [ ] IMPORTE TOTAL
- [ ] NIF
- [ ] NOMBRE DEL PROCURADOR/A
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR/A
- [ ] NOMBRE Y Nº DE COLEGIADO
- [ ] Nº
- [ ] Nº DE COLEGIADO
- [ ] Nº DE CUENTA
- [ ] O DEL DOMICILIO SOCIAL, SEGÚN EL CASO
- [ ] OBJETO DEL CONTRATO
- [ ] OBJETO SOCIAL
- [ ] PERIODICIDAD
- [ ] PERIODO
- [ ] PLAZO
- [ ] … y 2 datos más que aparecen una vez en el modelo

## Normas que cita el formulario

- art. 239 TRLSC
- art. 1106 Código Civil
- art. 1100 Código Civil
- art. 1108 Código Civil

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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…licación de lo dispuesto en los arts. 45 y 50 de la Ley de Enjuiciamiento Civil.»: comprobar el fuero aplicable (art. 50 LEC o, en su caso, art. 52.1.14.º LEC en materia de sociedades) y la competencia objetiva de la Sección de lo Mercantil conforme al art. 86 ter LOPJ vigente.
- Junto a «…acción de responsabilidad, contra el Consejero o contra el Administrador (...)".»: el original citaba preceptos derogados (LSA 1989, LSRL 1995) al transcribir estas sentencias; se han sustituido por la referencia al texto refundido de la Ley de Sociedades de Capital. Comprobar la cita literal de las sentencias y los números de recurso antes de presentar.
- Junto a «…o de colegiado: [NOMBRE Y Nº DE COLEGIADO] Procurador: [NOMBRE DEL PROCURADOR/A]»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.

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

[NOTA PARA EL PROFESIONAL, A SUPRIMIR ANTES DE PRESENTAR: el administrador no puede ejercitar por sí solo la acción social si no está facultado por la junta de socios. En el supuesto de dos administradores solidarios que son también socios al 50 %, la junta convocada para decidir la acción queda bloqueada, por lo que la demanda se plantea con la legitimación subsidiaria del socio con más del 5 % del capital, tras no aprobarse la propuesta en junta (art. 239 TRLSC).]

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE] QUE POR TURNO CORRESPONDA

D./Dª [NOMBRE Y APELLIDOS DEL PROCURADOR/A], Procurador/a de los Tribunales y de D./Dª [NOMBRE Y APELLIDOS DEL DEMANDANTE], como acredito en virtud de escritura de poder que acepto y acompaño, y cuya devolución intereso por ser de carácter general y necesaria para otros usos, bajo la dirección letrada de D./Dª [NOMBRE Y APELLIDOS DEL LETRADO], abogado/a ejerciente, n.º [Nº DE COLEGIADO] del Ilustre Colegio de [COLEGIO DE ABOGADOS], con despacho abierto en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y, como mejor proceda en Derecho,

DIGO:

Que por medio del presente escrito paso a interponer demanda de juicio ordinario, en la que ejercito la acción social de responsabilidad de administrador social frente a D./Dª [NOMBRE Y APELLIDOS DEL DEMANDADO], con DNI/NIE [DNI/NIE] y domicilio en [DOMICILIO].

Todo ello de acuerdo con los siguientes hechos y consideraciones de derecho:

HECHOS

PRIMERO.- Mi mandante y el demandado son administradores solidarios y socios fundadores, con el [PORCENTAJE DE CAPITAL]% cada uno, de la mercantil [DENOMINACIÓN SOCIAL], constituida el [DÍA] de [MES] de [AÑO], según consta en la escritura autorizada el día [FECHA] por D./Dª [NOMBRE DEL NOTARIO], Notario de [LOCALIDAD], con domicilio social en [DOMICILIO SOCIAL], e inscrita en el Registro Mercantil de [PROVINCIA], [DATOS REGISTRALES], con NIF [NIF].

Acredito estos extremos con el documento nº 1 de los que se acompañan a este escrito, consistente en copia simple de la escritura de constitución mencionada, así como con el documento nº 2, que recoge la certificación del Registro Mercantil donde constan los datos mencionados.

SEGUNDO.- La sociedad, constituida y gestionada por ambas partes, ha tenido por objeto social [OBJETO SOCIAL], desarrollando su actividad con distintas empresas que contrataban sus servicios. Desde su inicio hasta hace aproximadamente [PERIODO] el funcionamiento de la misma era correcto y los dos administradores sociales se dedicaban por entero a su actividad de forma cordial y colaboradora. Si bien, desde el momento indicado, por causas que mi cliente desconoce, la paz social se fue degradando, siendo cada vez más complicado poder tomar decisiones de manera conjunta, tal y como se había venido haciendo con normalidad desde un principio, independientemente del carácter solidario formal del órgano de administración conformado por ambos.

En este complicado escenario, mi cliente se apercibió de que los saldos de la cuenta corriente nº [Nº DE CUENTA] que la sociedad tiene abierta en la entidad [ENTIDAD BANCARIA], en la cual tienen firma ambos administradores, descendían de manera irregular. Tras requerir a la entidad un extracto completo de todos los movimientos realizados, se pudo comprobar que desde [FECHA], y con una frecuencia [PERIODICIDAD], se cargaba en la misma la cantidad de [IMPORTE] euros a favor de la sociedad [DENOMINACIÓN SOCIAL DEL BENEFICIARIO DE LOS PAGOS]. Se acompaña, como documento nº 3, copia del extracto bancario en el que se resaltan los movimientos por el referido importe, en los primeros días de cada uno de los últimos [Nº] meses, por un importe global de [IMPORTE TOTAL] euros. El gasto no corresponde a ninguna actividad desarrollada por [DENOMINACIÓN SOCIAL], y mi mandante ha tenido conocimiento de que las citadas cantidades se destinan a abonar [DESTINO PERSONAL DE LOS FONDOS: p. ej., el alquiler de la vivienda habitual del demandado].

TERCERO.- Asimismo, el pasado [FECHA], D./Dª [NOMBRE Y APELLIDOS DEL DEMANDADO], de motu propio y sin ningún tipo de consulta previa con mi cliente, resolvió en nombre de [DENOMINACIÓN SOCIAL] un contrato de [OBJETO DEL CONTRATO] firmado el [FECHA] con la sociedad [DENOMINACIÓN SOCIAL DE LA CONTRAPARTE], a pesar de que su suscripción había respondido al único acuerdo adoptado por ambos administradores en el presente año. Se adjuntan como documentos nº 4 y 5 el contrato firmado por el demandado al respecto y la comunicación enviada por la citada mercantil el [FECHA], en la que solicitaba la devolución de la documentación entregada, como consecuencia de la resolución contractual pactada.

El encargo consistía en [DESCRIPCIÓN DEL ENCARGO] en el plazo de [PLAZO], por un precio de [IMPORTE] euros, con perspectivas de ampliar la colaboración por otro periodo si la relación comercial era satisfactoria para ambas partes.

CUARTO.- Ante estos hechos mi mandante, como administrador solidario y socio con [PORCENTAJE DE CAPITAL]% del capital social, convocó junta extraordinaria de socios para debatir sobre la conveniencia de ejercer acción de responsabilidad contra el aquí demandado por los perjuicios ocasionados a la sociedad con las conductas indicadas. La junta, debidamente convocada, se celebró con presencia de ambos socios, no pudiendo ser aprobado el único punto del orden del día, dado que el demandado, con el [PORCENTAJE DE CAPITAL]% del capital social, votó en contra del mismo. Se aporta como documento nº 6 acta de la referida junta, elaborada por el Notario D./Dª [NOMBRE DEL NOTARIO], de [LOCALIDAD], quien asistió a la misma a petición de mi cliente.

A los presentes hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- JURISDICCIÓN Y COMPETENCIA

Es competente la Sección de lo Mercantil del Tribunal de Instancia del domicilio del demandado [O DEL DOMICILIO SOCIAL, SEGÚN EL CASO], al que se dirige la presente demanda, por aplicación de lo dispuesto en los arts. 45 y 50 de la Ley de Enjuiciamiento Civil.

II.- CAPACIDAD Y LEGITIMACIÓN

Tanto el demandante como el demandado son mayores de edad y se encuentran en situación de pleno ejercicio de sus derechos civiles, en virtud de lo dispuesto en los arts. 6.1.1.º y 7.1 de la Ley de Enjuiciamiento Civil.

Asimismo, mi mandante se encuentra legitimado para interponer la presente demanda en su condición de socio con más del 5 % del capital social, tras haberse convocado junta de socios para decidir al respecto y no haberse aprobado la propuesta realizada, con el voto en contra del propio demandado. En este sentido, el art. 239 del texto refundido de la Ley de Sociedades de Capital, aprobado por Real Decreto Legislativo 1/2010, de 2 de julio, configura esta legitimación subsidiaria cuando no se convoca la junta, cuando la sociedad no interpone la demanda tras la aprobación en junta o, como es el caso que nos ocupa, cuando el acuerdo de la junta convocada al respecto sea contrario a la exigencia de responsabilidad.

En este mismo sentido, el demandado, como administrador social cuya responsabilidad se pretende declarar, está legitimado pasivamente.

III.- PROCEDIMIENTO Y CUANTÍA

El procedimiento ajustado a derecho será el del juicio declarativo ordinario regulado en los arts. 399 a 436 de la Ley de Enjuiciamiento Civil, atendiendo a la cantidad reclamada, que es de [IMPORTE EN LETRA] euros ([IMPORTE] euros), en aplicación de lo dispuesto en el art. 249.2 de la Ley de Enjuiciamiento Civil, y que se señala conforme a la exigencia del art. 253.1 de la misma Ley.

IV.- POSTULACIÓN Y DEFENSA

Conforme a los arts. 23 y 31 de la Ley de Enjuiciamiento Civil se formula esta demanda a través de Procurador de los Tribunales con poder notarial para pleitos, y con dirección y firma de Letrado habilitado ante el Tribunal. Asimismo se cumplen los requisitos formales del art. 399 de la Ley de Enjuiciamiento Civil.

V.- FONDO DE LA CUESTIÓN CONTROVERTIDA

1) De las acciones de responsabilidad de administradores sociales:

El texto refundido de la Ley de Sociedades de Capital regula la responsabilidad de los administradores, aplicable a las sociedades de responsabilidad limitada y a las anónimas, en una triple vertiente:

A) La acción en exigencia de la responsabilidad por la realidad y valoración de las aportaciones no dinerarias, recogida actualmente en el art. 73.3 de la Ley de Sociedades de Capital.

B) La acción exigiendo la responsabilidad por sanción, regulada en el art. 367 de la Ley de Sociedades de Capital, que configura lo que se ha venido a denominar responsabilidad cuasi objetiva.

C) La acción exigiendo la responsabilidad por daño o acción aquiliana, regulada en los arts. 236 y siguientes de la Ley de Sociedades de Capital. En su marco se distingue la acción individual de responsabilidad, cuando el daño se produce a una persona concreta (socio o acreedor), y la acción social de responsabilidad, que aquí se ejercita, cuando el daño se produce a la sociedad mercantil en cuestión. Al respecto, las sentencias del Tribunal Supremo de 29 de diciembre de 2000 y de 30 de enero de 2001 distinguen indicando que "lo que caracteriza a la acción social, es que el daño se produce a la sociedad, eso en un aspecto propedéutico, sirve para distinguirla de la acción individual, en la cual, ese daño se produce al individuo, al interés personal, daños primarios o directos; es, pues, una dualidad perfectamente diferenciada, ya que la acción social procederá cuando una conducta transgresora del Consejero o del Administrador, por alguna de esas causas, daña a los intereses sociales; luego la ley desarrolla la legitimación activa, esto es, ante este daño de interés social, puede ejercitar la acción correspondiente: 1) Quien se considere dañado o perjudicado, el ente social, porque es justamente el receptor del daño, ente social que precisa un acuerdo en Junta con una mayoría ordinaria o simple, en donde se decida ejercitar la acción de responsabilidad, contra el Consejero o contra el Administrador (...)".

2.- De la acción social de responsabilidad ejercitada:

De esta forma, el ejercicio de la acción social se fundamenta en el art. 238.1 de la Ley de Sociedades de Capital, en el que se especifica que los administradores de derecho o de hecho, como tales, responderán frente a la sociedad del daño que causen por actos u omisiones contrarios a la ley o a los estatutos o por los realizados incumpliendo los deberes inherentes al desempeño del cargo. La acción se articula en beneficio de la sociedad y tiene por objeto restablecer el patrimonio de la sociedad, fundándose en la ejecución por el administrador o administradores de una conducta, positiva u omisiva, en el ejercicio de su cargo que comporte una lesión para el patrimonio social y tenga carácter antijurídico, por ser contraria a la ley o a los estatutos o consistir en el incumplimiento de los deberes impuestos legalmente a los administradores (tal y como señala la sentencia del Tribunal Supremo de 23 de enero de 2009, rec. 2018/2004, con cita de la sentencia del mismo Tribunal de 22 de marzo de 2006, rec. 2254/1999).

En consecuencia, se exige la concurrencia de un daño a la sociedad, que se produzca un acto ilícito de los administradores y que exista una relación de causalidad entre éste y aquél:

1.- El acto ilícito, en primer lugar, debe ser contrario a la Ley o a los estatutos, o estar realizado sin la diligencia debida. En el presente caso se imputa un acto contrario a la ley, al haber incumplido el demandado una de las principales obligaciones del administrador social, consistente en desempeñar el cargo con la diligencia de un ordenado empresario y representante leal, según el art. 225.1 de la Ley de Sociedades de Capital. Al respecto, la sentencia de la Audiencia Provincial de Valencia de 2 de octubre de 2009, rec. 364/2009, interpreta tal deber señalando que se trata de una "mera trasposición del tradicional comportamiento del buen padre de familia a que se refiere nuestro Código Civil, cuestión ésta que no cabe confundir con la eventual oportunidad —o falta de oportunidad— que pueda haber concurrido en la adopción de determinadas decisiones por parte del Administrador". Es decir, se trata de decisiones claramente contrarias a un patrón normal de diligencia, no de decisiones tomadas en un determinado momento que, posteriormente, tienen un resultado negativo. En esta misma línea, las sentencias de la Audiencia Provincial de Baleares de 18 de octubre de 2004, rec. 391/2004; de la Audiencia Provincial de Burgos de 31 de julio de 2001, rec. 250/2001; de la Audiencia Provincial de Guipúzcoa de 17 de mayo de 2001, rec. 2045/2001; y de la Audiencia Provincial de Alicante de 24 de octubre de 2002, rec. 818/2000, indican que "el fundamento de la responsabilidad de los administradores no deriva sin más de actos que sean lesivos a la sociedad, ya que pueden producirse pérdidas importantes en el patrimonio social debidas a la gestión de los administradores de las que no serán responsables, porque una cosa es el riesgo de empresa, que necesariamente ha de asumir la sociedad, aunque tenga como resultado pérdidas cuantiosas, y otra el riesgo de una gestión negligente de los administradores, los cuales, por incumplir con sus obligaciones legales y estatutarias, pueden ocasionar daños a la sociedad de los que los administradores deben responder".

Extremo evidentemente encuadrable, por un lado, en la disposición unilateral que el aquí demandado ha hecho de fondos de la sociedad para abonar gastos personales, sin ninguna suerte de autorización al respecto; y, por otro, en el hecho de dar por finalizada una relación contractual beneficiosa para aquella por su cuenta y riesgo, contraviniendo el acuerdo expreso adoptado para la continuación de la sociedad, con la única finalidad de bloquear la actividad de la misma. Conductas realizadas, de manera indudable, conscientemente por el demandado y que le son imputables a título de dolo, tal y como reconoce la sentencia del Tribunal Supremo de 24 de noviembre de 2011, rec. 1851/2007, en un caso similar: "siendo administrador pagó deudas particulares con cargo a la sociedad, lo que, si se tiene en cuenta los importes satisfechos, nada más puede imputarse a grave negligencia o dolo".

2.- En cuanto al daño, es necesario que sea la propia sociedad la que haya sufrido el daño por el acto de los administradores. Por ello la indemnización que se obtenga de su ejercicio debe ingresar necesariamente en el patrimonio de la sociedad, restituyendo aquel. En el presente caso, el daño generado por las dos actuaciones responde a las dos vertientes del mismo, recogidas en el artículo 1106 del Código Civil. Así, la sociedad ha sufrido un daño emergente al verse privada de la cantidad de [IMPORTE DEL DAÑO EMERGENTE] euros, destinados a abonar [DESTINO DE LOS FONDOS], sin ninguna relación con el objeto social de aquella. Y ha sufrido también un lucro cesante, por la ganancia dejada de obtener por el contrato unilateralmente resuelto, el cual preveía un precio de [IMPORTE DEL CONTRATO] euros.

3.- Por último, se precisa una clara relación de causalidad entre el acto ilícito de los administradores y el daño sufrido por la sociedad. Al respecto, la sentencia del Tribunal Supremo de 7 de julio de 2005, rec. 166/1999, considera "causa suficiente del resultado aquella que, aun concurriendo con otras, prepare, condicione o complete la acción de la causa última y, también, que la causalidad adecuada requiere valorar si el acto anterior tiene virtualidad suficiente para que del mismo se derive, como consecuencia necesaria, el efecto lesivo producido". Asimismo, en su sentencia de 12 de junio de 2000 dispone que "En cuanto a la existencia de nexo causal que, en este caso, niega la recurrente, esta Sala se basa en la doctrina jurisprudencial de la causalidad adecuada o eficiente para determinar la existencia de relación o enlace entre la acción u omisión y el daño o perjuicio resultante, pero optando por criterios y soluciones que le permitan valorar en cada caso si el acto antecedente que se presenta como causa tiene virtualidad suficiente para que del mismo se derive, como consecuencia necesaria, el efecto dañoso producido, y que la determinación del nexo causal debe inspirarse en las condiciones o circunstancias que el buen sentido señale en cada caso como índice de responsabilidad, dentro del infinito encadenamiento de causas y efectos". En el supuesto en que se fundamenta la acción de responsabilidad aquí ejercitada, la actuación del demandado, realizada y decidida únicamente por él, es la causa indudable del daño producido, puesto que el haber social se reduce al disponer fraudulentamente de los fondos sociales, y el precio del contrato se disipa y no entra en el patrimonio de la sociedad con la resolución contractual operada.

3.- De la procedencia de la indemnización de daños y perjuicios:

Conforme a la sentencia del Tribunal Supremo, Sala 1.ª, de 4 de julio de 2011, en interpretación de los arts. 1100 y siguientes del Código Civil: "Con la indemnización de daños mediante un pago en dinero se trata de restablecer al perjudicado, en la medida que sea posible, en la posición que hubiera tenido si el acto lesivo no se hubiera producido. Al ser patrimonial, el daño resarcible se identifica con la disminución de un patrimonio causada por el acto dañoso, lo que comprende tanto el valor de la pérdida sufrida, como la ganancia dejada de obtener", resarcimiento a que se refiere precisamente el art. 238 de la Ley de Sociedades de Capital, y que debe llevar a que el demandado reintegre a la sociedad aquello de lo que se apropió indebidamente y aquello que hizo perder a la misma con su dolosa actuación.

Por ello, se reclama que se condene al demandado a abonar la cantidad de [IMPORTE] euros, con intereses legales desde la presentación de la demanda, de conformidad con el artículo 1108 del Código Civil, interpretado por la sentencia de la Audiencia Provincial de Madrid de 4 de marzo de 2011. La misma indica que "La jurisprudencia, superando planteamientos anteriores, ha admitido la aplicación del interés moratorio también para las deudas derivadas de responsabilidad extracontractual (sentencia del TS de 21 de mayo de 1998, rec. 1350/1998) y asimismo ha desplazado, salvo en supuestos excepcionales que lo justificasen, el principio "in illiquidis non fit mora" por el de la restitución al acreedor del rendimiento que haya podido generar la suma adeudada desde que fue judicialmente reclamada (sentencias de la Sala 1.ª del TS de 5 de marzo de 1992, 18 de febrero de 1994, 13 de octubre de 1997, rec. 2650/1993, y de 15 de abril de 2005, 25 de marzo, rec. 624/2005, y 16 de octubre de 2009, rec. 1409/2005, y de 22 de febrero, rec. 2152/2005, 5 de mayo y 13 de octubre de 2010, rec. 1788/2006), que debe el demandante percibir, incluso en caso de estimación parcial, en aras a la completa satisfacción de sus derechos (pues se vería perjudicado por la tardía satisfacción de su crédito), sin que se justifique que se beneficie de aquél el deudor. Por lo tanto, reclamado a la parte demandada el pago de una suma de dinero, procede, en caso de condena al pago de la misma, incluso si la causa de pedir lo fuese la responsabilidad extracontractual, el pago de intereses moratorios desde que le fue judicialmente exigida".

VI.- COSTAS

Conforme al artículo 394 de la Ley de Enjuiciamiento Civil, las costas han de imponerse al demandado.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL: Que, teniendo por presentado este escrito de demanda con sus documentos y copias, se sirva admitirlo y acordar de conformidad, teniendo por interpuesta demanda de juicio declarativo ordinario en ejercicio de la acción social de responsabilidad por mi representado, para que en su día, seguidos los trámites legales oportunos, se dicte sentencia por la que se declare la responsabilidad del demandado D./Dª [NOMBRE Y APELLIDOS DEL DEMANDADO], condenándole al pago de [IMPORTE] euros a favor de la sociedad [DENOMINACIÓN SOCIAL], más intereses desde la presente interpelación judicial, así como al pago de las costas ocasionadas.

Por ser justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Abogado y número de colegiado: [NOMBRE Y Nº DE COLEGIADO]

Procurador: [NOMBRE DEL PROCURADOR/A]

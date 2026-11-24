---
name: licencia-patente-contrato-mer-0709
description: "Licencia de patente (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Licencia de patente (contrato)

> Formulario **MER-0709** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Contrato de licencia exclusiva de una patente española para todo el territorio nacional, con canon fijo anual y regalía sobre ventas, control de instalaciones, prohibición de cesión y sublicencia, cláusula de exclusión de uso para sistemas de inteligencia artificial, duración renovable y sumisión a tribunales.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Licencia de patente (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Licencia de patente (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:licencia-patente-contrato-mer-0709`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (4 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] LOCALIDAD, CALLE, NÚMERO (3 veces)
- [ ] FIRMA (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL (2 veces)
- [ ] Nº DE PATENTE (2 veces)
- [ ] PRODUCTO O INVENCIÓN (2 veces)
- [ ] AÑO
- [ ] CIUDAD
- [ ] DATOS REGISTRALES: LIBRO, TOMO, FOLIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DNI/NIF
- [ ] DÍA
- [ ] ESTADO CIVIL
- [ ] IMPORTE EN LETRA
- [ ] IMPORTE EN NÚMERO
- [ ] MES
- [ ] NACIONALIDAD
- [ ] NIF
- [ ] NOMBRE DEL AUDITOR O DE LA FIRMA DE AUDITORÍA
- [ ] NOMBRE O DENOMINACIÓN DEL LICENCIANTE
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE
- [ ] PORCENTAJE
- [ ] PROVINCIA

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

NOTAS DE AYUDA

La patente puede ser objeto de licencia en su totalidad o en alguna de las facultades que integran el derecho de exclusiva, para todo el territorio nacional o para una parte del mismo. Las licencias pueden ser exclusivas o no exclusivas. Se entiende que, salvo pacto en contrario, la licencia no es exclusiva y que el licenciante podrá conceder licencias a otras personas y explotar por sí mismo la invención. La licencia exclusiva impide el otorgamiento de otras licencias y el licenciante solo podrá explotar la invención si en el contrato se hubiera reservado expresamente ese derecho. Los titulares de licencias contractuales no podrán cederlas a terceros ni conceder sublicencias, a no ser que se hubiere convenido lo contrario.

Según dispone el artículo 86 de la Ley 24/2015, de Patentes, el licenciante y el licenciatario responderán solidariamente de las indemnizaciones a las que hubiere lugar como consecuencia de los daños y perjuicios ocasionados a terceras personas por defectos inherentes a la invención objeto de la patente. El licenciante que hubiera debido hacer frente a la responsabilidad mencionada podrá reclamar al licenciatario las cantidades abonadas, a no ser que se hubiese pactado lo contrario, que hubiere procedido de mala fe o que, dadas las circunstancias del caso y por razones de equidad, deba ser el licenciante quien soporte en todo o en parte la indemnización establecida a favor de terceros.

Según dispone el artículo 117 de la Ley de Patentes, el licenciatario podrá ejercitar en su propio nombre todas las acciones que en la Ley de Patentes se reconocen al licenciante frente a los terceros que infrinjan su derecho. No se podrán ejercitar si se trata de una licencia no exclusiva. El licenciatario que por ello no esté legitimado para ejercitar las acciones por violación de la patente podrá requerir notarialmente al titular de la misma para que entable la acción judicial correspondiente.

Se incluye cláusula sobre sistemas de inteligencia artificial.


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

CONTRATO

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

COMPARECEN

De una parte, [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL], como LICENCIANTE.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Persona física) [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL] [en su caso, especificar el régimen económico matrimonial], de nacionalidad [NACIONALIDAD], con [ELEGIR: DNI/NIF número [Nº] (si es español) / tarjeta de residencia número [Nº] o pasaporte número [Nº], expedido el [FECHA] y vigente hasta el [FECHA] (si es extranjero)], con domicilio en [LOCALIDAD, CALLE, NÚMERO].

— (Persona jurídica) Sociedad mercantil [DENOMINACIÓN SOCIAL], constituida en escritura pública otorgada el día [FECHA] ante el Notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], e inscrita en el Registro Mercantil de [PROVINCIA], [DATOS REGISTRALES: LIBRO, TOMO, FOLIO], domiciliada en [LOCALIDAD, CALLE, NÚMERO] y con NIF núm. [NIF], representada por [NOMBRE Y APELLIDOS DEL REPRESENTANTE], mayor de edad, con domicilio en [LOCALIDAD, CALLE, NÚMERO], con DNI/NIF núm. [DNI/NIF], cuyas facultades derivan del poder otorgado por el Notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], poder debidamente inscrito, que es declarado vigente y sin modificación alguna.

De otra parte, [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL], como LICENCIATARIO (persona física o jurídica; reiterar las anteriores circunstancias en función del supuesto concreto).

Ambas partes, quienes se reconocen con carácter mutuo capacidad legal suficiente para otorgar el presente contrato de licencia de patente, y

EXPONEN

1) Que el LICENCIANTE es titular de la patente española número [Nº DE PATENTE], relativa a [PRODUCTO O INVENCIÓN].

2) Que dicha patente se halla plenamente en vigor y al corriente del pago de las tasas.

3) Que sobre la misma no pende ningún procedimiento judicial que discuta su validez.

4) Que el LICENCIATARIO está interesado en obtener una licencia exclusiva de dicha patente para todo el territorio español.

Por ello, las partes acuerdan el siguiente contrato de licencia de patente, que se regirá por las siguientes

CLÁUSULAS

PRIMERA.— El LICENCIANTE autoriza al LICENCIATARIO a realizar todos los actos que integran la explotación de la invención patentada, en todas sus aplicaciones, en todo el territorio nacional y durante toda la duración de la patente, en relación con la patente española número [Nº DE PATENTE], relativa a [PRODUCTO O INVENCIÓN].

SEGUNDA.— La licencia de patente será exclusiva.

TERCERA.— El LICENCIANTE habrá de poner a disposición del LICENCIATARIO los conocimientos técnicos que posea y que resulten necesarios para poder proceder a una adecuada explotación de la invención. Por su parte, el LICENCIATARIO estará obligado a adoptar las medidas necesarias para evitar la divulgación de los conocimientos secretos que se le comuniquen.

CUARTA.— El LICENCIANTE se reserva el derecho de control de las instalaciones del LICENCIATARIO para controlar el proceso de fabricación. Ese control comprenderá el de la contabilidad. Los costes de la fiscalización de las instalaciones, contabilidad incluida, serán de cuenta del LICENCIANTE, salvo que de la misma se deriven anomalías graves, caso en el cual los costes del control corresponderán al LICENCIATARIO.

QUINTA.— En todo producto manufacturado, así como en las etiquetas y material promocional, aparecerá la indicación "Bajo licencia de [NOMBRE O DENOMINACIÓN DEL LICENCIANTE]".

SEXTA.— El LICENCIATARIO pagará en contraprestación por el uso de la patente una cantidad fija anual de [IMPORTE EN LETRA] euros ([IMPORTE EN NÚMERO] euros) y una regalía sobre el total de ventas de un [PORCENTAJE] %. En caso de discrepancias en cuanto a la fijación del canon que debe pagar el LICENCIATARIO, esta cantidad será determinada por el auditor de cuentas [NOMBRE DEL AUDITOR O DE LA FIRMA DE AUDITORÍA].

SÉPTIMA.— El LICENCIATARIO no podrá ceder la licencia a terceros ni conceder sublicencias.

OCTAVA.— Las Partes acuerdan que las autorizaciones y derechos concedidos en las anteriores cláusulas se otorgan sin la facultad de emplear los derechos licenciados para el entrenamiento, alimentación o aprendizaje automático de ningún sistema de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robótica, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología disruptiva relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). De tal manera que el uso de los derechos licenciados por mor del presente Contrato para los enunciados usos constituirá un incumplimiento sustancial del mismo.

El LICENCIATARIO habrá de respetar el compromiso adquirido en virtud de la anterior estipulación en los contratos, negocios y relaciones jurídicas que mantenga con terceros, sean personas físicas o jurídicas, adoptando todas las medidas necesarias a tal fin e incluyendo, si fuese necesario, previsiones escritas en los contratos que celebre con estos terceros.

NOVENA.— El LICENCIATARIO se compromete a usar la patente en España, resarciendo al LICENCIANTE de los daños y perjuicios que el incumplimiento de esta obligación pudiera ocasionarle.

DÉCIMA.— El LICENCIANTE y el LICENCIATARIO responderán solidariamente de las indemnizaciones a las que hubiere lugar como consecuencia de los daños y perjuicios ocasionados a terceras personas por defectos inherentes a la invención objeto de la patente. El LICENCIANTE que hubiera debido hacer frente a la responsabilidad mencionada en esta cláusula podrá reclamar al LICENCIATARIO las cantidades abonadas.

UNDÉCIMA.— El LICENCIATARIO podrá ejercitar en su propio nombre todas las acciones que en la Ley de Patentes se reconocen al LICENCIANTE frente a los terceros que infrinjan su derecho. El LICENCIATARIO que en tal caso ejercite una acción deberá notificárselo inmediatamente al LICENCIANTE, el cual podrá personarse e intervenir en el procedimiento.

DUODÉCIMA.— El presente contrato tiene una duración de [Nº] años a contar desde la fecha de suscripción del presente contrato. Podrá ser renovado, siempre dentro del periodo de duración legal de la invención, por periodos iguales de tiempo, siempre que ninguna de las partes manifieste su voluntad contraria a la renovación en el plazo de dos meses anteriores al vencimiento del plazo de duración previsto.

DECIMOTERCERA.— El LICENCIANTE responde de la titularidad de la patente y manifiesta que no existen litigios sobre la validez de la patente que se licencia ni acciones reivindicatorias sobre la misma. Caso de existir, el LICENCIANTE se compromete a indemnizar los daños y perjuicios que por dichas causas se originen al LICENCIATARIO. Todo ello sin perjuicio de la responsabilidad por evicción prevista en la ley.

DECIMOCUARTA.— Las partes se someten a la jurisdicción de los Tribunales de [CIUDAD], con renuncia del fuero que pudiera corresponderles.

PROTECCIÓN DE DATOS

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento del Reglamento (UE) 2016/679 (RGPD), de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, y demás normativa aplicable.

Ambas partes firman el presente contrato, que se extiende en dos ejemplares, igualmente originales, en el lugar y fecha indicados en su encabezamiento, como prueba de conformidad.

EL LICENCIANTE: [FIRMA]	EL LICENCIATARIO: [FIRMA]

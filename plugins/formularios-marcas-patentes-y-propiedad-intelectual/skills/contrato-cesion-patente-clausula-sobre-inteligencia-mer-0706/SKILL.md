---
name: contrato-cesion-patente-clausula-sobre-inteligencia-mer-0706
description: "Contrato de cesión de patente con cláusula sobre inteligencia artificial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cesión de patente con cláusula sobre inteligencia artificial

> Formulario **MER-0706** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Contrato de cesión (transmisión) de una patente de invención inscrita en la Oficina Española de Patentes y Marcas, libre de cargas y de derechos de terceros, a cambio de un precio. Adaptado a la Ley 24/2015, de 24 de julio, de Patentes (vigente desde el 1 de abril de 2017). Incluye una cláusula que excluye el uso de los derechos cedidos para el entrenamiento de sistemas de inteligencia artificial.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cesión de patente con cláusula sobre inteligencia artificial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cesión de patente con cláusula sobre inteligencia artificial” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-cesion-patente-clausula-sobre-inteligencia-mer-0706`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] LOCALIDAD, CALLE, NÚMERO (3 veces)
- [ ] Nº (3 veces)
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
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE
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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

COMPARECEN

De una parte, [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL], como CEDENTE.

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Persona física) [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL] [en su caso, especificar el régimen económico matrimonial], de nacionalidad [NACIONALIDAD], con [ELEGIR: DNI/NIF número [Nº] (si es español) / tarjeta de residencia número [Nº] o pasaporte número [Nº], expedido el [FECHA] y vigente hasta el [FECHA] (si es extranjero)], con domicilio en [LOCALIDAD, CALLE, NÚMERO].

— (Persona jurídica) Sociedad mercantil [DENOMINACIÓN SOCIAL], constituida en escritura pública otorgada el día [FECHA] ante el Notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], e inscrita en el Registro Mercantil de [PROVINCIA], [DATOS REGISTRALES: LIBRO, TOMO, FOLIO], domiciliada en [LOCALIDAD, CALLE, NÚMERO] y con NIF núm. [NIF], representada por [NOMBRE Y APELLIDOS DEL REPRESENTANTE], mayor de edad, con domicilio en [LOCALIDAD, CALLE, NÚMERO], con DNI/NIF núm. [DNI/NIF], cuyas facultades derivan del poder otorgado ante el Notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], poder debidamente inscrito, que es declarado vigente y sin modificación alguna.

De otra parte, [NOMBRE Y APELLIDOS / DENOMINACIÓN SOCIAL], como CESIONARIO (persona física o jurídica; reiterar las anteriores circunstancias en función del supuesto concreto).

Ambas partes, quienes se reconocen con carácter mutuo capacidad legal suficiente para otorgar el presente contrato de cesión de patente, y

EXPONEN

1) Que el CEDENTE es titular de la patente española número [Nº DE PATENTE], relativa a [PRODUCTO O INVENCIÓN].

2) Que dicha patente se halla plenamente en vigor y al corriente del pago de las tasas.

3) Que sobre la misma no pende ningún procedimiento judicial que discuta su validez.

4) Que el CESIONARIO está interesado en la adquisición de dicha patente.

CLÁUSULAS

PRIMERA.— El CEDENTE cede al CESIONARIO el pleno dominio y titularidad de la patente española número [Nº DE PATENTE], relativa a [PRODUCTO O INVENCIÓN].

SEGUNDA.— El CESIONARIO adquiere dicho dominio y abona como contraprestación la cantidad de [IMPORTE EN LETRA] euros ([IMPORTE EN NÚMERO] euros), cantidad que se confiesa recibida por parte del CEDENTE.

TERCERA.— El CEDENTE se obliga a poner a disposición del CESIONARIO los conocimientos técnicos que posea y que resulten necesarios para poder proceder a una adecuada explotación de la patente. El CESIONARIO, a quien se comuniquen conocimientos secretos, estará obligado a adoptar las medidas necesarias para evitar su divulgación.

CUARTA.— Las Partes acuerdan que las cesiones efectuadas en los anteriores apartados se realizan sin la facultad de emplear los derechos cedidos para el entrenamiento, alimentación o aprendizaje automático de ningún sistema de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robótica, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología disruptiva relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). De tal manera que el uso de los derechos cedidos por mor del presente Contrato para los enunciados usos constituirá un incumplimiento sustancial del mismo.

El CESIONARIO habrá de respetar el compromiso adquirido en virtud de la anterior estipulación en los contratos, negocios y relaciones jurídicas que mantenga con terceros, sean personas físicas o jurídicas, adoptando todas las medidas necesarias a tal fin e incluyendo, si fuese necesario, previsiones escritas en los contratos que celebre con estos terceros.

QUINTA.— El CEDENTE responde de la titularidad de la patente.

SEXTA.— El CEDENTE y el CESIONARIO responderán solidariamente de las indemnizaciones a las que hubiere lugar como consecuencia de los daños y perjuicios ocasionados a terceras personas por defectos inherentes a la invención objeto de la patente. El CEDENTE que hubiera debido hacer frente a la responsabilidad mencionada en esta cláusula podrá reclamar al CESIONARIO las cantidades abonadas.

SÉPTIMA.— El CEDENTE manifiesta que no existen litigios sobre la validez de la patente que se transmite ni acciones reivindicatorias sobre la misma. Caso de existir, el CEDENTE se compromete a indemnizar los daños y perjuicios que por dichas causas se originen al CESIONARIO. Todo ello sin perjuicio de la responsabilidad por evicción prevista en la ley.

OCTAVA.— Las partes se someten a la jurisdicción de los Tribunales de [CIUDAD], con renuncia del fuero que pudiera corresponderles.

PROTECCIÓN DE DATOS

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento del Reglamento (UE) 2016/679 (RGPD), de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, y demás normativa aplicable.

Ambas partes firman el presente contrato, que se extiende en dos ejemplares, igualmente originales, en el lugar y fecha indicados en su encabezamiento, como prueba de conformidad.

EL CEDENTE: [FIRMA]	EL CESIONARIO: [FIRMA]

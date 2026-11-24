---
name: escritura-publica-transformacion-sociedad-colectiva-sa-mer-0351
description: "Escritura pública de transformación de una sociedad colectiva en SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de transformación de una sociedad colectiva en SA

> Formulario **MER-0351** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Escritura pública por la que los socios de una sociedad colectiva la transforman en sociedad anónima, aprobando el balance, los estatutos, la adjudicación de acciones, el capital y el primer Consejo de Administración. La escritura debe contener, además de las menciones exigidas para la constitución de una sociedad anónima, la relación de socios que hubieran hecho uso del derecho de separación y el capital que representen, así como las acciones que se atribuyan a cada socio en la sociedad transformada.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de transformación de una sociedad colectiva en SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de transformación de una sociedad colectiva en SA” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:escritura-publica-transformacion-sociedad-colectiva-sa-mer-0351`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (8 veces)
- [ ] AÑO (7 veces)
- [ ] DÍA (7 veces)
- [ ] MES (7 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] IMPORTE (5 veces)
- [ ] NOMBRE DEL NOTARIO (4 veces)
- [ ] Nº DE PROTOCOLO (4 veces)
- [ ] DOMICILIO (3 veces)
- [ ] PROVINCIA (3 veces)
- [ ] CONCEPTO (2 veces)
- [ ] DATOS REGISTRALES: TOMO, HOJA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NIF (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] ACTIVIDAD
- [ ] CALLE Y NÚMERO
- [ ] CERTIFICACIÓN REGISTRAL / COPIA DE LA ESCRITURA / OTRO DOCUMENTO
- [ ] COLEGIO NOTARIAL
- [ ] DATOS REGISTRALES: FOLIO, TOMO, LIBRO DE SOCIEDADES, HOJA
- [ ] ENTIDAD BANCARIA
- [ ] ESTADO CIVIL
- [ ] FIRMA - NOMBRE DEL NOTARIO
- [ ] FIRMA - NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL EXPERTO
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTADO
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE
- [ ] NOMBRE Y APELLIDOS DEL SOCIO
- [ ] NOMBRE Y APELLIDOS, EDAD, NACIONALIDAD Y DOMICILIO DEL CONSEJERO
- [ ] NOMBRES Y APELLIDOS
- [ ] NUMERACIÓN
- [ ] Nº DE CUENTA
- [ ] NÚMEROS
- [ ] OBJETO SOCIAL
- [ ] SERIE
- [ ] SUCURSAL

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

- Al principio del formulario: la transformación de sociedades mercantiles se regula actualmente en el Real Decreto-ley 5/2023, de 28 de junio (libro primero, que sustituye a la Ley 3/2009 sobre modificaciones estructurales), y la constitución de la sociedad anónima en el texto refundido de la Ley de Sociedades de Capital (RDLeg 1/2010). Comprobar en esas normas los requisitos vigentes (proyecto, informes, balance, derecho de separación, publicidad, capital mínimo y desembolso) antes de otorgar la escritura.

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

NÚMERO [Nº DE PROTOCOLO]

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Ante mí, [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio de [COLEGIO NOTARIAL],

COMPARECEN

(repetir el párrafo por cada compareciente)

[NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero/a / divorciado/a / separado/a judicialmente / viudo/a / casado/a], con profesión [PROFESIÓN], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [Nº DE DOCUMENTO],

INTERVIENEN

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (En nombre propio) En nombre y derecho propio, como únicos socios de la sociedad colectiva denominada [DENOMINACIÓN SOCIAL], con NIF número [NIF], domiciliada en [LOCALIDAD], calle [DOMICILIO], con actividad principal de [ACTIVIDAD].

— (En representación) [NOMBRE Y APELLIDOS DEL REPRESENTANTE], en nombre y representación de:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si se trata de persona física) [NOMBRE Y APELLIDOS DEL REPRESENTADO], de estado civil [ESTADO CIVIL], con profesión [PROFESIÓN], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [Nº DE DOCUMENTO],

— (Si se trata de una persona jurídica) Compañía mercantil de nacionalidad española denominada [DENOMINACIÓN SOCIAL], [ELEGIR: S.L. / S.A.], domiciliada en [LOCALIDAD], calle [CALLE Y NÚMERO], con NIF núm. [NIF], inscrita en el Registro Mercantil de [PROVINCIA], [DATOS REGISTRALES: FOLIO, TOMO, LIBRO DE SOCIEDADES, HOJA]. Su capital social es de [IMPORTE] euros, dividido en [Nº] [ELEGIR: participaciones / acciones / cuotas] de [IMPORTE] euros de valor nominal cada una de ellas, numeradas correlativamente del 1 al [Nº], ambos inclusive, estando totalmente suscritas e íntegramente desembolsadas.

Dicha sociedad tiene por objeto social [OBJETO SOCIAL].

Hace uso de las facultades conferidas a su favor en calidad de:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Cargo social) [ELEGIR: Administrador único / administrador solidario / consejero delegado] de la sociedad indicada, cargo para el que fue nombrado en escritura otorgada ante el notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], el [DÍA] de [MES] de [AÑO], con el número de orden de su protocolo [Nº DE PROTOCOLO], que causó inscripción en el Registro Mercantil de [PROVINCIA] [DATOS REGISTRALES: TOMO, HOJA].

— (Apoderado) Apoderado de la sociedad antes mencionada, según consta en escritura de poder otorgada a su favor ante el notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], el [DÍA] de [MES] de [AÑO], con el número de orden de su protocolo [Nº DE PROTOCOLO], que causó inscripción en el Registro Mercantil de [PROVINCIA] [DATOS REGISTRALES: TOMO, HOJA].

Y el representante de la sociedad [DENOMINACIÓN SOCIAL], según interviene, hace constar, conforme a lo establecido en la Ley 10/2010, de 28 de abril, de prevención del blanqueo de capitales y de la financiación del terrorismo, que el titular real de la sociedad ha sido identificado en acta de manifestaciones autorizada por el Notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], el día [DÍA] de [MES] de [AÑO], con el número [Nº DE PROTOCOLO] de su protocolo, manifestando no haberse modificado el contenido de la misma y, por tanto, no haber habido modificación en la titularidad real reflejada.

Identifico a los comparecientes por la documentación que muestran y les juzgo con la capacidad legal necesaria para el otorgamiento de esta escritura.

EXPONEN

I. Que los Sres. [NOMBRES Y APELLIDOS] son los únicos socios de «[DENOMINACIÓN SOCIAL], Sociedad Colectiva» [DATOS IDENTIFICADORES DE LA SOCIEDAD: ESCRITURA DE CONSTITUCIÓN, NOTARIO AUTORIZANTE, DATOS DE INSCRIPCIÓN EN EL REGISTRO MERCANTIL, DURACIÓN, OBJETO, NIF].

Acreditan su titularidad mediante [CERTIFICACIÓN REGISTRAL / COPIA DE LA ESCRITURA / OTRO DOCUMENTO].

II. Que es voluntad de los socios transformar la referida Sociedad Colectiva en Sociedad Anónima.

III. Que los socios aprueban el balance general de la sociedad cerrado con fecha [DÍA] de [MES] de [AÑO] (con una antelación máxima de seis meses), que, junto con un informe sobre modificaciones patrimoniales significativas producidas con posterioridad, me entregan en este acto, extendido en [Nº] folios, que, a su requerimiento, incorporo a la matriz de la presente escritura.

IV. Que el patrimonio de la sociedad cubre el capital social [OPCIONAL — incluir si procede: o, por lo menos, el 25 % del capital de la sociedad anónima resultante de la transformación].

Acreditan la realidad del patrimonio dinerario que aparece en el balance mediante la exhibición y entrega de los correspondientes resguardos de depósito a nombre de la sociedad en el Banco/s [ENTIDAD BANCARIA], sucursal [SUCURSAL], cuenta núm. [Nº DE CUENTA], que quedan unidos a esta escritura matriz.

El patrimonio social no dinerario ha sido objeto de informe pericial de fecha [DÍA] de [MES] de [AÑO], elaborado por [NOMBRE Y APELLIDOS DEL EXPERTO], como experto independiente nombrado por el Registrador mercantil en resolución de fecha [DÍA] de [MES] de [AÑO], del que resulta la correcta valoración de los bienes que constan en el balance. El informe está extendido en [Nº] folios y queda incorporado a esta matriz.

V. Que proceden al otorgamiento de la presente escritura de transformación con arreglo a las siguientes

ESTIPULACIONES

PRIMERA.- Transformación de la sociedad.

Los socios transforman la sociedad colectiva en una sociedad anónima, que se denominará «[DENOMINACIÓN SOCIAL], S.A.».

[OPCIONAL — incluir si procede: si se cambia la denominación social, aportar y protocolizar la certificación del Registro Mercantil Central relativa a la nueva denominación social adoptada.]

SEGUNDA.- Estatutos.

La Sociedad se regirá por los estatutos que los socios me entregan en este acto, extendidos en [Nº] folios, aprobados y firmados por ellos, que ratifican y elevan a escritura pública mediante su incorporación a la presente.

TERCERA.- Adjudicación de las acciones.

Las acciones de la sociedad se adjudican a los socios en proporción a su participación en la sociedad colectiva, atribuyéndose a cada uno de ellos las acciones siguientes (repetir por cada socio):

[NOMBRE Y APELLIDOS DEL SOCIO], [Nº] acciones, números [NUMERACIÓN] [en su caso, especificar también clase y serie].

CUARTA.- Capital social.

El capital social queda cubierto en su integridad con el patrimonio de la sociedad transformada. [OPCIONAL — incluir si procede: si no queda cubierto en su integridad, concretar la proporción que queda pendiente de desembolso, así como la forma y plazo máximo en que hayan de satisfacerse los dividendos pasivos.]

Gastos de transformación.- La cuantía total de los gastos de transformación se calcula en [IMPORTE] euros, de los que ya han sido satisfechos [IMPORTE] euros en concepto de [CONCEPTO], quedando pendientes [IMPORTE] euros en concepto de [CONCEPTO].

QUINTA.- Consejo de Administración.

El primer Consejo de Administración de la Sociedad estará constituido por los Consejeros siguientes (repetir por cada consejero):

[NOMBRE Y APELLIDOS, EDAD, NACIONALIDAD Y DOMICILIO DEL CONSEJERO]

Los nombramientos se realizan por el plazo estatutario de [Nº] años.

Los nombrados aceptan el cargo y manifiestan que no están incursos en incompatibilidades legales.

Los Consejeros designados constituyen en este acto el Consejo de Administración de la sociedad, nombrando Presidente a [NOMBRE Y APELLIDOS], Vicepresidente a [NOMBRE Y APELLIDOS], Secretario a [NOMBRE Y APELLIDOS] y Vocales a [NOMBRE Y APELLIDOS] y [NOMBRE Y APELLIDOS].

[OPCIONAL — si ha lugar: nombramiento del administrador único o del número de administradores que corresponda según los Estatutos, en lugar del Consejo de Administración.]

OTORGAMIENTO Y AUTORIZACIÓN

Hago a los comparecientes las reservas y advertencias legales, especialmente las derivadas de la legislación fiscal, y del Registro Mercantil y de su publicidad.

Leo esta escritura a los comparecientes advirtiéndoles del derecho que tienen a hacerlo personalmente, derecho al que renuncian. Enterados de su contenido, los comparecientes hacen constar libremente su consentimiento al otorgamiento de la escritura y la firman.

Y yo, el Notario, compruebo que el consentimiento ha sido libremente prestado y se adecua a la legalidad, y del contenido de esta escritura, extendida en [Nº] folios de papel exclusivo para documentos notariales, serie [SERIE], números [NÚMEROS], DOY FE.

Notario: [FIRMA - NOMBRE DEL NOTARIO]

Otorgantes (repetir por cada otorgante): [FIRMA - NOMBRE Y APELLIDOS]

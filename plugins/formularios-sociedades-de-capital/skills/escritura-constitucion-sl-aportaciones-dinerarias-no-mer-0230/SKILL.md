---
name: escritura-constitucion-sl-aportaciones-dinerarias-no-mer-0230
description: "Escritura de constitución de una SL con aportaciones dinerarias, no dinerarias o mixtas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de constitución de una SL con aportaciones dinerarias, no dinerarias o mixtas

> Formulario **MER-0230** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública de constitución de una Sociedad de Responsabilidad Limitada, en la que se establecen las condiciones y estipulaciones necesarias para su creación, funcionamiento y organización, tales como su denominación, duración, domicilio, objeto, capital social, aportaciones dinerarias, no dinerarias o mixtas, web corporativa y órganos de administración.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de constitución de una SL con aportaciones dinerarias, no dinerarias o mixtas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de constitución de una SL con aportaciones dinerarias, no dinerarias o mixtas” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-constitucion-sl-aportaciones-dinerarias-no-mer-0230`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (19 veces)
- [ ] NOMBRE Y APELLIDOS (18 veces)
- [ ] IMPORTE (8 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] PLAZO (4 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] DOCUMENTO ACREDITATIVO (2 veces)
- [ ] COLEGIO
- [ ] CÓDIGO CNAE
- [ ] DESCRIBIR
- [ ] DIRECCIÓN
- [ ] ENTIDAD BANCARIA
- [ ] FECHA
- [ ] LUGAR
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] OBJETO SOCIAL

## Normas que cita el formulario

- art. 15 Ley 14/2013
- art. 20 Ley 14/2013

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

Modelo de escritura pública de constitución de una Sociedad de Responsabilidad Limitada, en la que se establecen las condiciones y estipulaciones necesarias para su creación, funcionamiento y organización, tales como su denominación, duración, domicilio, objeto, capital social, aportaciones dinerarias, no dinerarias o mixtas, web corporativa y órganos de administración.


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

NÚMERO DE PROTOCOLO:

En [LUGAR], a [FECHA].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO].

COMPARECEN

[ELEGIR UNA OPCIÓN: En caso de estado civil no casado / En caso de estado civil casado]

[OPCIONAL — incluir si procede]

(Si se trata de una persona jurídica)

La entidad [DENOMINACIÓN SOCIAL] constituida en escritura pública ante el notario D./Dña. [NOMBRE DEL NOTARIO], con domicilio en [LOCALIDAD], objeto social [ACTIVIDAD]. Inscrita en el Registro Mercantil de [LOCALIDAD] y NIF [NIF].

INTERVIENEN

Los señores comparecientes intervienen en su propio nombre y derecho.

Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente escritura de constitución de SOCIEDAD DE RESPONSABILIDAD LIMITADA, a cuyo fin

EXPONEN

PRIMERO. Que los mentados Sres. han convenido constituir una Sociedad de Responsabilidad Limitada para la realización de [ACTIVIDAD].

SEGUNDO. Que han sido informados por mí el Notario, sobre el procedimiento de constitución telemática regulado en los art. 15 y 16 de la de la Ley 14/2013, de 27 de septiembre, y me indican expresamente su voluntad de no acogerse al mismo.

TERCERO. Que, a tales efectos, y en su calidad de únicos socios fundadores, han decidido otorgar la presente escritura de constitución de SOCIEDAD DE RESPONSABILIDAD LIMITADA, que se regirá por las siguientes

ESTIPULACIONES

I.- Constitución y socios fundadores

En el presente acto los comparecientes como únicos socios fundadores, proceden a constituir una Sociedad de Responsabilidad Limitada de nacionalidad española que se regirá por el presente contrato, por los estatutos que en el mismo se aprueban, y en lo en ellos no dispuesto y en cuanto no sean contrarios a la misma, por el Real Decreto Legislativo 1/2010, de 2 de julio, por el que se aprueba el Texto Refundido de la Ley de Sociedades de Capital.

Presentes todos los socios y en relación con lo establecido en los Estatutos sociales, establecen como cuenta de correo electrónico de cada uno de ellos y a todos los efectos, las siguientes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[NOMBRE Y APELLIDOS]

II.- Denominación

[ELEGIR UNA OPCIÓN: Con certificación negativa / Con certificación negativa telemática]

III- Duración

La Sociedad tendrá una duración [PLAZO], dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de la presente escritura, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Sociedad en momentos anteriores al de su inscripción en el Registro Mercantil.

Los ejercicios sociales se computarán por años naturales.

IV.- Domicilio

El domicilio de la Sociedad se halla situado en [DIRECCIÓN], [LOCALIDAD].

V.- Objeto social

El objeto social de la Sociedad será [OBJETO SOCIAL].

De conformidad con el art.20 de la Ley 14/2013, de 27 de septiembre, hacen constar los comparecientes que la Clasificación Nacional de Actividades Económicas (CNAE) que le corresponderá a la entidad constituida es [CÓDIGO CNAE].

VI.- Capital social

El capital social será de [IMPORTE] euros, dividido en [Nº] participaciones de [IMPORTE] euros de valor nominal cada una de ellas, numeradas de manera correlativa con los números 1 a [Nº].

Dicho capital social ha sido totalmente suscrito y desembolsado por los socios fundadores, habiendo realizado cada uno de ellos las aportaciones que se describen a continuación:

[OPCIONAL — incluir si procede]

(Aportaciones dinerarias)
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], aporta [IMPORTE] euros por lo que se le asignan [Nº] participaciones, que son las numeradas [Nº] a [Nº].

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

La totalidad de dichas aportaciones han sido realizadas, con el consentimiento de su cónyuge [ELEGIR: en efectivo / por cheque / por transferencia] a título de propiedad, y se han efectuado en moneda nacional. Los fundadores manifiestan que responderán solidariamente frente a la sociedad y frente a los acreedores sociales de la realidad de las mismas, por lo que no es necesaria ninguna acreditación tal y como se establece en el art. 62 de la Ley de Sociedades Capitales.

La totalidad de dichas aportaciones han sido realizadas, con el consentimiento de su cónyuge [ELEGIR: en efectivo / por cheque / por transferencia] a título de propiedad, y se han efectuado en moneda nacional, realidad que se acredita mediante certificación del depósito de las correspondientes cantidades a nombre de la sociedad en la entidad de crédito [ENTIDAD BANCARIA], certificación que se halla vigente según compruebo al observar la fecha del depósito al que hace referencia, y cuyo original se me entrega para ser incorporado a la presente escritura, lo cual procedo a efectuar a requerimiento de los comparecientes, quedando la misma unida al final de esta matriz.

[OPCIONAL — incluir si procede]

(Aportaciones no dinerarias)
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] suscribe [Nº] participaciones sociales, números [Nº] a [Nº] ambas inclusive, por su valor nominal de [IMPORTE] euros. En pago de las mismas:

[OPCIONAL — incluir si procede]

(Si el bien es privativo)

Aporta a la sociedad [DENOMINACIÓN SOCIAL] bien privativo tal y como se deduce de [DOCUMENTO ACREDITATIVO].

[OPCIONAL — incluir si procede]

(Si el bien es ganancial)

Aporta a la sociedad [DENOMINACIÓN SOCIAL] con el consentimiento de su cónyuge [NOMBRE Y APELLIDOS] la mitad indivisa de [DESCRIPCIÓN DEL BIEN] por su valor de [IMPORTE] euros, equivalente al valor nominal de las participaciones sociales adjudicadas.

Todas las aportaciones no dinerarias se efectúan en pleno dominio, con todos sus derechos inherentes y accesorios, y en concepto de libres de toda carga, gravamen o arrendamiento, responsabilidad o afección.

[ELEGIR UNA OPCIÓN: Con informe de experto independiente / Sin informe de experto independiente]

[OPCIONAL — incluir si procede]

(Con aportaciones mixtas)
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] suscribe [Nº] participaciones sociales, números [Nº] a [Nº] ambas inclusive, por su valor nominal de [IMPORTE] euros.

En pago de las mismas efectúa las siguientes aportaciones a la sociedad:

La suma de [IMPORTE] euros, [ELEGIR: en efectivo / por cheque / por transferencia], correspondiente al valor nominal de las participaciones sociales números [Nº] a [Nº].

[OPCIONAL — incluir si procede]

(Si el bien es privativo)

bien privativo tal y como se deduce de [DOCUMENTO ACREDITATIVO]. En relación a esta aportación no dineraria se aporta el informe de valoración confeccionado por el experto independiente D./Dña. [NOMBRE Y APELLIDOS].

[OPCIONAL — incluir si procede]

(Si el bien es ganancial)

con el consentimiento de su cónyuge [NOMBRE Y APELLIDOS] la mitad indivisa de [DESCRIPCIÓN DEL BIEN] por su valor de [IMPORTE] euros, equivalente al valor nominal de las participaciones sociales adjudicadas. En relación a esta aportación no dineraria se aporta el informe de valoración confeccionado por el experto independiente D./Dña. [NOMBRE Y APELLIDOS].

VII.- Administración de la sociedad

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Los socios fundadores, encomiendan la administración y representación de la Sociedad a D./Dña. [NOMBRE Y APELLIDOS] en calidad de Administrador único de la misma, por el plazo de [Nº] años.

Los socios fundadores, al amparo de lo previsto en los Estatutos sociales (Anexo [Nº]), encomiendan la administración y representación de la Sociedad como administradores solidarios, por el plazo estatutario de [PLAZO], a las siguientes personas:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS].

Los socios fundadores, al amparo de lo previsto en los Estatutos sociales /Anexo [Nº]), encomiendan la administración y representación de la Sociedad como administradores mancomunados, por el plazo estatutario de [PLAZO], a las siguientes personas:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS].

Los socios fundadores nombran inicialmente, como miembros del Consejo de Administración, por el plazo estatutario de [PLAZO], a las siguientes personas:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS].

Dichos señores, reunidos en Consejo de Administración, adoptan por unanimidad los siguientes acuerdos:

1. Distribuir los cargos del Consejo de la siguiente forma:

Presidente D./Dña. [NOMBRE Y APELLIDOS].

Secretario D./Dña. [NOMBRE Y APELLIDOS].

Vocales D./Dña. [NOMBRE Y APELLIDOS].

2. Nombrar Consejero Delegado, a D./Dña. [NOMBRE Y APELLIDOS], quien ejercerá todas las facultades que corresponden al Consejo, y que legal y estatutariamente sean delegables.

Todos los nombrados aceptan sus cargos y manifiestan no estar incursos en ninguna incapacidad o incompatibilidad para su ejercicio, en especial de las fijadas para los altos cargos en la Ley 3/2015, de 30 de marzo, y en disposiciones específicas de las Comunidades Autónomas.

Igualmente se encomienda a los citados Administradores la presentación de la presente escritura constitutiva para su inscripción en el Registro Mercantil de [LOCALIDAD].

VIII.- Web Corporativa

Se acuerda asimismo por unanimidad la creación de la página WEB corporativa de la Sociedad, de conformidad con los Estatutos Sociales y la Ley de Sociedades de Capital, delegando en el órgano de administración la elección de la dirección URL o sitio en la Web de la web corporativa, que una vez concretada se comunicará por dicho órgano de administración a todos los socios.

IX.- Aprobación de los estatutos sociales

Se procede a la aprobación de los Estatutos que han de regir el funcionamiento de la Sociedad, que los comparecientes me otorgan en este acto, extendidos en [Nº] folios, aprobados y firmados por ellos, que ratifican y elevan a escritura pública mediante su incorporación a la presente, que solicitan expresamente, lo cual efectúo uniéndolos al final de esta matriz. (Anexo [Nº])

X.- Facultades de subsanación

Los comparecientes se otorgan poder recíproco para que cualquiera de ellos, por sí o en representación de los demás, pueda proceder a la subsanación o rectificación de la presente escritura y de los Estatutos a ella incorporados siempre que ello sea preciso para su obligada inscripción en el Registro Mercantil de [LOCALIDAD], y siempre que las citadas subsanaciones o rectificaciones se limiten a meros errores materiales, o a aceptar las modificaciones procedentes de la calificación registral.

OTORGAMIENTO

Hago las reservas y advertencias legales, en especial:

a) Las referidas a la obligación de inscribir la presente en el Registro Mercantil del domicilio social en el plazo de dos meses y las consecuencias de su infracción.
b) Las de carácter fiscal, y entre ellas la obligación de presentar la escritura a su liquidación en la oficina competente, en el plazo de treinta días hábiles desde este otorgamiento, y las sanciones y consecuencias que se derivarían de la falta de presentación en dicho plazo.

Leo a los comparecientes, tras advertirles del derecho que tienen a hacerlo por sí,al que renuncian, la presente escritura, prestan su consentimiento y firman conmigo.

AUTORIZACIÓN

De todo lo consignado en este instrumento público, extendido sobre [DESCRIBIR] folios de papel de uso exclusivo notarial, serie y números [Nº] yo, el Notario, doy fe.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS].

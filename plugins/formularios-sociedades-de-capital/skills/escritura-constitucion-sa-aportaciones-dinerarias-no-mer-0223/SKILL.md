---
name: escritura-constitucion-sa-aportaciones-dinerarias-no-mer-0223
description: "Escritura de constitución de una SA con aportaciones dinerarias y no dinerarias. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de constitución de una SA con aportaciones dinerarias y no dinerarias

> Formulario **MER-0223** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública de constitución de una sociedad anónima, en la que se establecen las condiciones y estipulaciones necesarias para su creación, así como las aportaciones dinerarias y no dinerarias de cada uno de los socios.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de constitución de una SA con aportaciones dinerarias y no dinerarias» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de constitución de una SA con aportaciones dinerarias y no dinerarias” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-constitucion-sa-aportaciones-dinerarias-no-mer-0223`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (13 veces)
- [ ] IMPORTE (8 veces)
- [ ] Nº (8 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] ACTIVIDAD (3 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] CÓDIGO CNAE (2 veces)
- [ ] DATOS REGISTRALES (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] SERIE (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] CLASE
- [ ] COLEGIO
- [ ] CORREO ELECTRÓNICO
- [ ] DESCRIBIR
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DIRECCIÓN
- [ ] DOCUMENTO ACREDITATIVO
- [ ] DÍA
- [ ] FINCA
- [ ] LUGAR
- [ ] MES
- [ ] NACIONALIDAD
- [ ] NOMBRE DE LA MARCA
- [ ] Nº DE BASTIDOR
- [ ] Nº DE CILINDROS
- [ ] Nº DE MOTOR
- [ ] Nº DE PROTOCOLO
- [ ] OBJETO SOCIAL
- [ ] PISO
- [ ] PROFESIÓN
- [ ] SERIE DE ACCIONES
- [ ] TIPO DE PERMISO
- [ ] TOMO
- [ ] ÓRGANO ADMINISTRATIVO

## Normas que cita el formulario

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

Modelo de escritura pública de constitución de una sociedad anónima, en la que se establecen las condiciones y estipulaciones necesarias para su creación, así como las aportaciones dinerarias y no dinerarias de cada uno de los socios.


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

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO]

COMPARECEN

[OPCIONAL — incluir si procede]

Persona física

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domiciliado en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO],

[OPCIONAL — incluir si procede]

Persona jurídica

D./Dña. [NOMBRE Y APELLIDOS] en nombre y representación de la compañía mercantil de nacionalidad española denominada [DENOMINACIÓN SOCIAL], [ELEGIR: SL / SA], domiciliada en [DOMICILIO], calle, núm. [NÚMERO], con NIF núm. Inscrita en el Registro Mercantil de [LOCALIDAD], en [DATOS REGISTRALES] el

Hace uso de las facultades conferidas a su favor en calidad de [ELEGIR: administrador único / administrador solidadario / consejero delegado] de la sociedad indicada, cargo para el que fue nombrado en escritura otorgada ante notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS] el [DÍA] de [MES] de [AÑO] con el número de orden de su protocolo [Nº DE PROTOCOLO] que causó inscripción en el Registro mercantil de [PROVINCIA] en el tomo [TOMO] hoja

INTERVIENEN

Los señores comparecientes intervienen en su propio nombre y derecho.

Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para celebrar la presente escritura de constitución de SOCIEDAD ANÓNIMA, a cuyo fin

EXPONEN

PRIMERO.- Que los comparecientes han convenido constituir una Sociedad Anónima por el procedimiento de fundación simultánea y para la realización de [ACTIVIDAD]

SEGUNDO.- Que a tales efectos, y en su calidad de únicos socios fundadores, han decidido otorgar la presente escritura de constitución de SOCIEDAD ANÓNIMA, que se regirá por las siguientes

ESTIPULACIONES

I.- Constitución y socios fundadores

En el presente acto los comparecientes D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS],y D./Dña. [NOMBRE Y APELLIDOS], según intervienen y como socios fundadores, proceden a constituir una Sociedad de Anónima de nacionalidad española que se regirá por el presente contrato, por los estatutos que en el mismo se aprueban, y en lo en ellos no dispuesto y en cuanto no sean contrarios a la misma, por el Texto Refundido de la Ley de Sociedades de Capital.

De conformidad con el art.20 de la Ley 14/2013, de 27 de septiembre, hacen constar los comparecientes que la Clasificación Nacional de Actividades Económicas (CNAE) que le corresponderá a la entidad constituida es la siguiente [CÓDIGO CNAE].

Presentes todos los socios y en relación con lo establecido en los Estatutos sociales, designan como cuentas de correo electrónico de cada uno de ellos y a todos los efectos, las siguientes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] Dirección de correo electrónico [CORREO ELECTRÓNICO]

II.- Denominación

La Sociedad se denomina ‘ [DENOMINACIÓN SOCIAL], S.A. ‘, denominación que no se halla registrada por ninguna otra entidad inscribible en el Registro Mercantil, según consta en la certificación negativa de denominación que los comparecientes exhiben y que se halla vigente, la cual procedo a unir, a requerimiento de los comparecientes, a la matriz de la presente escritura.

III- Duración

La Sociedad tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de la presente escritura, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Sociedad en momentos anteriores al de su inscripción en el Registro Mercantil.

Los ejercicios sociales se computarán por años naturales.

IV.- Domicilio

El domicilio de la Sociedad se halla situado en [DIRECCIÓN], calle [CALLE] número [NÚMERO] piso [PISO]

V.- Objeto social

El objeto social de la Sociedad será [OBJETO SOCIAL]. De conformidad con el art. 20 de la Ley 14/2013, de 27 de septiembre, hacen constar los comparecientes que la Clasificación Nacional de Actividades Económicas (CNAE) que le corresponderá a la entidad constituida es [CÓDIGO CNAE].

VI.- Capital social, aportaciones y suscripción

[OPCIONAL — incluir si procede]

(Con aportaciones dinerarias)

El capital social será de [IMPORTE] dividido en [Nº] acciones de [IMPORTE] euros de valor nominal cada una de ellas, numeradas de manera correlativa con los números 1 a [Nº] y representadas mediante títulos [ELEGIR: al portador / nominativos]

I. Suscripción y desembolso

[ELEGIR UNA OPCIÓN: Desembolso total / Desembolso parcial]

II. Justificación de aportaciones

[ELEGIR UNA OPCIÓN: Entrega del efectivo al notario / Depósito previo]

[OPCIONAL — incluir si procede]

(Con aportaciones no dinerarias)

El capital social será de [IMPORTE], dividido en [Nº] acciones de [IMPORTE] euros de valor nominal cada una de ellas, numeradas de manera correlativa con los números 1 a [Nº] y representadas mediante títulos [ELEGIR: al portador / nominativos]

Dicho capital social ha sido totalmente suscrito y desembolsado por los socios habiendo realizado cada uno de ellos las aportaciones que se describen a continuación

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] suscribe acciones, números [Nº] a ", ambas inclusive de la [SERIE DE ACCIONES], clase [CLASE] y/o serie, [SERIE] por su valor nominal total de [IMPORTE].

En pago de las mismas D./Dña. [NOMBRE Y APELLIDOS] aporta a la sociedad - con el consentimiento de su cónyuge, "el bien [DESCRIPCIÓN DEL BIEN], por su valor de [IMPORTE] euros",

[OPCIONAL — incluir si procede]

Vehículos

Tractor [ELEGIR: Automóvil / Motocicleta] marca [MARCA/MODELO] modelo matrícula con número de bastidor [Nº DE BASTIDOR], y de motor [Nº DE MOTOR]; cilindros" [Nº DE CILINDROS] Tiene un permiso de circulación de tipo [TIPO DE PERMISO], expedido [ÓRGANO ADMINISTRATIVO] el

[OPCIONAL — incluir si procede]

Propiedad industrial

Los siguientes derechos de propiedad industrial:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Marca

Derechos derivados de MARCA denominada [NOMBRE DE LA MARCA], Ámbito de actividad [ACTIVIDAD] Número de Inscripción en la OEPM [Nº]

Patente

Patente denominada y cuyo objeto es "", número [NÚMERO] de la clase cuya concesión publicada en el Boletín Oficial de la Propiedad Industrial de [FECHA].

Inscrita en el Registro de la Propiedad Industrial a nombre del aportante, con fecha [FECHA] y número [NÚMERO]

[OPCIONAL — incluir si procede]

Empresa

La Empresa denominada [DENOMINACIÓN SOCIAL], con domicilio dedicada a [ACTIVIDAD].

Los comparecientes me entregan su balance de situación de fecha para que lo una, como hago, a la presente escritura.

Bienes: Dicha empresa se integra por las existencias, mercaderías, utillaje, instrumentos de trabajo, mobiliario y demás bienes y derechos cuya descripción obra en el inventario que, extendido sobre el anverso de " " folios de papel común, que me entregan los comparecientes, tras firmarlos en mi presencia, para que lo una como hago a la presente.

Valoración: Se valora el conjunto de la empresa, según el balance incorporado en [DOCUMENTO ACREDITATIVO].

TÍTULO: Les pertenece, según lo manifiestan habiendo adquirido los bienes por los siguientes:

CARGAS Y ARRENDAMIENTOS: Se deja constancia de que los bienes integrantes de la empresa están libres de toda carga, gravamen, arrendamiento o responsabilidad y que no se encuentran hipotecados, pignorados o embargados, así como que su precio de adquisición está íntegramente satisfecho.

[OPCIONAL — incluir si procede]

Inmueble

Inscrito en el Registro de la Propiedad de [LOCALIDAD], al [DATOS REGISTRALES].

Le pertenece por Compra formalizada mediante escritura autorizada por el Notario D./Dña. [NOMBRE Y APELLIDOS] de [LOCALIDAD] el [FECHA], número de Protocolo.

Referencia y certificación catastral:", según resulta de la certificación catastral descriptiva y gráfica de la finca, dando fe, yo el Notario, de que la descripción contenida en la certificación catastral aportada e incorporada a la presente se corresponde con la realidad física de la finca.

Cargas y situación posesoria: Manifiesta el aportante, que la finca [FINCA] se encuentra libre de cargas y de arrendamientos.

Valor: Se valora en [IMPORTE] euros.

Se hace constar que, en cumplimiento de lo establecido en el artículo 67 de la Ley de Sociedades de Capital, los bienes descritos han sido objeto de informe pericial elaborado por D./Dña. [NOMBRE Y APELLIDOS] como experto independiente nombrado por el Registrador mercantil de [PROVINCIA], en resolución de fecha [FECHA], y que de ese informe resulta la correcta valoración atribuida a los bienes aportados.

[OPCIONAL — incluir si procede]

Maquinaria Industrial

La Máquina modelo, marca [MARCA/MODELO] serie [SERIE] "determinar número y serie

Le pertenece, según manifiesta, por haberlo adquirido - por compraventa a en el según manifiesta sin acreditarlo documentalmente.

Manifiesta el compareciente, en el concepto en que interviene, que la maquinaria reseñada está libre de toda carga, gravamen, arrendamiento o responsabilidad y que no se encuentra hipotecada, pignorada o embargada, así como que su precio de adquisición está íntegramente satisfecho.

La totalidad de dichas aportaciones ha sido realizada a título de propiedad, en pleno dominio, con todos sus derechos inherentes y accesorios y libres de toda carga y gravamen, arrendamientos, responsabilidad u otras afecciones.

En prueba de todo ello los comparecientes me entregan para unir a la presente matriz, a lo cual procedo, los correspondientes informes emitidos por el experto independiente nombrados a tal fin por el Registrador Mercantil de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], en los que se describen y valoran las citadas aportaciones no dinerarias.

VII.- Gastos de constitución

La cuantía total aproximada de los gastos de constitución e incluidos los ya satisfechos se calcula que alcanzará la cifra de [IMPORTE] euros.

VIII.- Administración, representación inicial de la sociedad y WEB corporativa

[ELEGIR UNA OPCIÓN: Administrador único / Administradores solidarios / Administradores mancomunados / Consejo de Administración]

Igualmente se encomienda a los citados administradores iniciales la presentación de la presente escritura constitutiva para su inscripción en el Registro Mercantil de [LOCALIDAD], quien se compromete a su cumplimiento.

Se acuerda asimismo por unanimidad la creación de la página WEB corporativa de la Sociedad, de conformidad con los Estatutos Sociales y la Ley de Sociedades de Capital, delegando en el órgano de administración la elección de la dirección URL que deberá ser comunicado a todos los socios.

IX.- Aprobación de los estatutos sociales

Se procede a la aprobación de los Estatutos que han de regir el funcionamiento de la Sociedad, que los comparecientes me otorgan en este acto, extendidos en [Nº] folios, aprobados y firmados por ellos, que ratifican y elevan a escritura pública mediante su incorporación a la presente, que solicitan expresamente, lo cual efectúo uniéndolos al final de esta matriz.

Otorgamiento

Hago las reservas y advertencias legales, en especial:

a) Las relativas a la obligación de inscribir la presente en el Registro Mercantil del domicilio social en el plazo de dos meses y las consecuencias de su infracción.
b) Las de carácter fiscal, y entre ellas las relativas a la exención en el Impuesto sobre Transmisiones Patrimoniales y Actos Jurídicos Documentados, cuya aplicación expresamente solicitan los comparecientes, y la obligación de presentar la presente escritura a su liquidación en la oficina competente, en el plazo de treinta días hábiles desde este otorgamiento, y las sanciones y consecuencias que se derivarían de la falta de presentación en dicho plazo.

Leo a los comparecientes, tras advertirles del derecho que tienen a hacerlo por sí, - al que renuncian- del que hacen uso la presente escritura, prestan su consentimiento y firman conmigo.

Autorización

De todo lo consignado en este instrumento público, extendido sobre [DESCRIBIR] folios de papel de uso exclusivo notarial, serie y números [Nº], yo, el Notario, doy fe.

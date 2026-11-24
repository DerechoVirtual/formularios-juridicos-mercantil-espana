---
name: escritura-publica-aumento-capital-sl-mer-0039
description: "Escritura pública de aumento de capital de una SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de aumento de capital de una SL

> Formulario **MER-0039** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de aumento de capital de una SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de aumento de capital de una SL” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-publica-aumento-capital-sl-mer-0039`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] FECHA (7 veces)
- [ ] Nº (6 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NÚMERO (3 veces)
- [ ] CARGO (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] COLEGIO
- [ ] DOMICILIO
- [ ] ENTIDAD BANCARIA
- [ ] LIBRO
- [ ] LUGAR
- [ ] NACIONALIDAD
- [ ] NIF
- [ ] PROFESIÓN

## Normas que cita el formulario

- art. 295 TRLSC

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

COMPARECEN
INTERVIENEN
EXPONEN
OTORGAN
Elevación a público
Aumento de capital
Modificación de Estatutos.
Solicitud de inscripción en el Registro Mercantil de [LOCALIDAD]
ADVERTENCIAS LEGALES, OTORGAMIENTO Y AUTORIZACIÓN NOTARIAL

Modelo de escritura mediante la cual se eleva a público el acuerdo de Junta General de Socios de una Sociedad de Responsabilidad Limitada sobre el aumento del capital social por elevación del valor nominal de las participaciones o por creación de nuevas con cargo a: aportaciones dinerarias o no dinerarias, incluida la aportación de créditos contra la sociedad; beneficios o reservas que ya figurasen en el último balance aprobado y, en segundo lugar, se eleva a público a la modificación de los estatutos sociales en lo que afecte a ese aumento de capital (art.295 TRLSC)

NÚMERO DE PROTOCOLO:

En [LUGAR], a [FECHA].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO]

COMPARECEN

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente viudo / viudo / viuda / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domiciliado en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO],

INTERVIENEN

Los señores comparecientes intervienen en su calidad de [CARGO] de ‘ [DENOMINACIÓN SOCIAL], S.L.’, con domicilio en [LOCALIDAD], NIF [NIF], que fue constituida por tiempo indefinido, ante mí, D./Dña. [NOMBRE Y APELLIDOS] notario de esta ilustre villa, el día [FECHA], según consta en el número [NÚMERO] de mi protocolo, y que fue inscrita en el Registro Mercantil de [LOCALIDAD] al Libro [LIBRO] de Sociedades,

Les identifico por su citado [ELEGIR: DNI / pasaporte / permiso de residencia]. Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para otorgar la presente escritura de ampliación del capital social de ‘ [DENOMINACIÓN SOCIAL], S.L.’ y correspondiente modificación de los estatutos de la citada mercantil, según consta en la escritura constitutiva de la sociedad, cuya copia autorizada tengo a la vista sin que en lo omitido por innecesario haya nada que limite, condicione, contradiga o amplíe lo anterior, asegurando los comparecientes la titularidad de sus respectivas participaciones, a cuyo fin

EXPONEN

Primero. Que los mentados Sres. celebraron el pasado día [FECHA] Junta universal de socios de la citada compañía ‘ [DENOMINACIÓN SOCIAL], S.L.’, en la cual adoptaron, por unanimidad, el acuerdo de aumentar el capital social de la citada sociedad.

Segundo.- Que, a tales efectos, y debido al acuerdo de aumento del capital de la Sociedad indicado anteriormente, los socios han convenido modificar el artículo [Nº DE ARTÍCULO] de sus Estatutos, referente a la cifra de capital social y a las participaciones que lo constituyen.

Tercero.- Que los anteriores acuerdos constan en la certificación de la que me hacen entrega, emitida por D./Dña. [NOMBRE Y APELLIDOS], secretario de dicha Junta, y con el visto bueno de D./Dña. [NOMBRE Y APELLIDOS] Presidente de la misma, quienes fueron elegidos para tales cargos por voto unánime de los socios, cuyas firmas legítimo, procediendo a la unión de dicha certificación a la matriz de la presente escritura formando parte integrante de la misma y a cuyo fin

OTORGAN

Primero. Elevación a público

D./Dña. [NOMBRE Y APELLIDOS], conforme interviene, eleva a público los acuerdos adoptados por la Junta General de la sociedad, en su reunión de [FECHA] los cuales obran en la certificación que exhibe, dándose aquí por reproducidos.

La referida certificación, expedida por D./Dña. [NOMBRE Y APELLIDOS], en su calidad de [CARGO] cuya firma conozco y considero legítima, me entrega el compareciente para que una, como hago, a la presente.

Segundo. Aumento de capital

a) Cuantía

Por el mencionado acuerdo queda aumentado el capital social de ‘ [DENOMINACIÓN SOCIAL], S.L.’ en la cantidad de [IMPORTE] euros, por lo que éste pasa a tener la cuantía de [IMPORTE] euros.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

b) Elevación del valor nominal de las participaciones sociales

La citada ampliación de capital social se realiza mediante la elevación del valor nominal de las participaciones sociales en [IMPORTE] euros para cada una de ellas.

b) Creación de nuevas participaciones

La citada ampliación de capital social se realiza mediante la creación de [Nº] nuevas participaciones sociales, de [IMPORTE] euros de valor nominal cada una de ellas y, en su caso, una prima de asunción global de [IMPORTE] euros, lo que supone una prima de [IMPORTE] euros por participación las cuales otorgan iguales derechos a sus titulares.

Que, a efectos del ejercicio del derecho de preferencia, la oferta de asunción de las nuevas participaciones fue comunicada en forma escrita a todos y cada uno de los socios y usufructuarios inscritos en el Libro Registro de socios, habiéndose efectuado el último envío con fecha [FECHA].

Los comparecientes suscribieron las nuevas participaciones sociales a prorrata de su porcentaje de participación en el capital social:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] suscribe [Nº] participaciones numeradas del [Nº] al [Nº], ambos inclusive.

De las nuevas participaciones y sobre su titularidad se ha tomado oportuna nota en el Libro Registro de Socios de la entidad.

c) Desembolso

[OPCIONAL — incluir si procede]

(Aportaciones dinerarias)

Los comparecientes manifiestan que el importe correspondiente al aumento de capital en [IMPORTE] euros ha sido ingresado con fecha [FECHA] en la cuenta abierta a nombre de la sociedad en la entidad de crédito [ENTIDAD BANCARIA], cuenta número [NÚMERO], lo que acredita con certificación del depósito de las correspondientes cantidades expedida por dicha entidad, que me entregan para unir, a la presente escritura, comprobando yo, el notario, que la fecha del citado depósito no es anterior en más de dos meses a la de la presente escritura.

[OPCIONAL — incluir si procede]

(Aportaciones no dinerarias)

La descripción de las aportaciones no dinerarias, así como la identidad de quienes las efectuaron y la numeración de las participaciones sociales a que corresponden son los que constan en la certificación que se adjunta a la presente escritura formando parte integrante de la misma.

El acuerdo de la Junta se adoptó a la vista del informe de los Administradores previsto en el art. 300.1 de la Ley de Sociedades de Capital en el que se describen con detalle las aportaciones proyectadas, su valoración, las personas que las efectúan, el número y valor nominal de las participaciones sociales que hayan de crearse o emitirse, la cuantía del aumento del capital social y las garantías adoptadas para la efectividad del aumento según la naturaleza de los bienes en que la aportación consista.

[OPCIONAL — incluir si procede]

(Por compensación de créditos)

Declara el compareciente que, asumidas todas las participaciones sociales, el aumento de capital ha sido íntegramente desembolsado mediante compensación de créditos, todo ello con sujeción al acuerdo y a las previsiones legales.

A tal fin, hace constar:

Que, a efectos de lo dispuesto en los art. 301 de la Ley de Sociedades de Capital se ha redactado un informe por los administradores donde se describe la naturaleza y características de los créditos a compensar, la identidad de los aportantes, el número de participaciones sociales o de acciones que hayan de crearse o emitirse y la cuantía del aumento, en el que expresamente se hará constar la concordancia de los datos relativos a los créditos con la contabilidad social.

El compareciente declara que los datos que constan en dicho informe se corresponden con los obrantes en la contabilidad de la sociedad.

Queda, por lo tanto, totalmente suscrito y desembolsado el capital de ‘[DENOMINACIÓN SOCIAL], S.L.’

Puesto que el desembolso del total del aumento del capital social se realizó por compensación de los créditos aportados, la Junta hizo constar la total extinción de los mismos.

[OPCIONAL — incluir si procede]

(Con cargo a reservas)

El compareciente declara que, hallándose totalmente suscrita y desembolsada la cifra anterior del capital social, el aumento ha sido desembolsado con cargo a la cuenta ‘Reservas voluntarias’ por traspaso contable del importe de la ampliación de dicha cuenta a la cuenta de capital social.

Declara igualmente que, para el cálculo de la base de la presente operación se ha utilizado el balance aprobado por la Junta celebrada el pasado [FECHA] verificado por [NOMBRE Y APELLIDOS].

Queda, por lo tanto, totalmente suscrito y desembolsado el capital social de ‘ S.L.’

Tercero. Modificación de Estatutos.

Debido al aumento del capital social, los otorgantes han acordado la modificación del artículo [Nº DE ARTÍCULO] de los Estatutos de la Sociedad, el cual quedará redactado de la siguiente manera:

‘Artículo-Capital social

El capital social será de [IMPORTE] euros, dividido en [Nº] participaciones de [IMPORTE] euros de valor nominal cada una de ellas, numeradas de manera correlativa con los números 1 a [Nº].

Dicho capital se halla totalmente suscrito y desembolsado mediante aportaciones realizadas por los socios a título de propiedad’.

Cuarto. Solicitud de inscripción en el Registro Mercantil de [LOCALIDAD]

Los otorgantes solicitan al señor Registrador Mercantil de [LOCALIDAD] la inscripción de la presente escritura y la correspondiente modificación de los estatutos de la sociedad en la hoja registral correspondiente a la citada mercantil.

ADVERTENCIAS LEGALES, OTORGAMIENTO Y AUTORIZACIÓN NOTARIAL

---
name: estatutos-sociales-sociedad-limitada-laboral-mer-0450
description: "Estatutos sociales de una sociedad limitada laboral. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Estatutos sociales de una sociedad limitada laboral

> Formulario **MER-0450** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Estatutos sociales de una sociedad limitada laboral» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Estatutos sociales de una sociedad limitada laboral” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:estatutos-sociales-sociedad-limitada-laboral-mer-0450`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (5 veces)
- [ ] IMPORTE (2 veces)
- [ ] CLASE O SERIE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN
- [ ] LOCALIDAD
- [ ] OBJETO SOCIAL
- [ ] OTROS DATOS
- [ ] PLAZO
- [ ] ÓRGANO O PERSONA

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

DENOMINACIÓN, DURACIÓN, DOMICILIO, NACIONALIDAD, WEB CORPORATIVA Y OBJETO
CAPITAL SOCIAL Y PARTICIPACIONES
ÓRGANOS SOCIALES
EJERCICIO SOCIAL Y CUENTAS ANUALES
SEPARACIÓN Y EXCLUSIÓN DE SOCIOS
DISOLUCIÓN Y LIQUIDACIÓN DE LA SOCIEDAD

Modelo de estatutos de una sociedad de responsabilidad limitada laboral, en el que se concretan las pautas a seguir para su correcto funcionamiento, creación y organización, tales como su objeto social, denominación, derechos y obligaciones de los socios, capital social, administración y representación de la misma.

TÍTULO I.- DENOMINACIÓN, DURACIÓN, DOMICILIO, NACIONALIDAD, WEB CORPORATIVA Y OBJETO

Artículo 1º.- Denominación

La Sociedad se denominará «, [DENOMINACIÓN SOCIAL]
S.L.L.
S.R.L.L.
 » y se regirá por los presentes estatutos, así como por las disposiciones legales que le sean aplicables en cada momento.

Artículo 2º.- Duración

La Sociedad tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de su escritura constitutiva, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Sociedad en momentos anteriores al de su inscripción en el Registro Mercantil.

Los ejercicios sociales se computarán por años naturales.

Artículo 3º.- Domicilio, nacionalidad y WEB corporativa

La Sociedad tiene nacionalidad española, con domicilio situado en [DIRECCIÓN], [LOCALIDAD]

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

El órgano de administración podrá crear, suprimir o trasladar sucursales, así como cambiar el domicilio social dentro del territorio nacional.

El órgano de administración podrá crear, suprimir o trasladar sucursales. Los administradores no ostentan la competencia para cambiar el domicilio social, siendo este acuerdo de exclusiva competencia de la Junta de socios

Por acuerdo de la Junta General, la Sociedad podrá tener una página WEB corporativa, de conformidad con lo dispuesto en el art. 11 bis de la Ley de Sociedades de Capital. La Junta General podrá delegar en el órgano de administración la elección de la dirección URL o sitio en la Web de la web corporativa, que una vez concretada comunicará dicho órgano de administración a todos los socios. Será competencia del órgano de administración la modificación, el traslado o la supresión de la página web.

Artículo 4º.- Objeto social

El objeto social de la Sociedad será [OBJETO SOCIAL]

Estas Actividades también podrán ser desarrolladas, de modo indirecto, mediante la participación en sociedades con análogo objeto.

Cuando para realizar alguna actividad integrante del objeto social fuera precisa la obtención de licencia o autorización administrativa especial, la Sociedad no podrá iniciar su desarrollo hasta que aquélla no se haya concedido.

TÍTULO II.- CAPITAL SOCIAL Y PARTICIPACIONES

Artículo 5º.- Capital Social

El capital social será de [IMPORTE] euros ( Euros), representado por [ÓRGANO O PERSONA] participaciones sociales, acumulables e indivisibles, de [IMPORTE] de valor nominal cada una, de [CLASE O SERIE] numeradas correlativamente del [Nº] al [Nº], ambos inclusive, que confieren a sus titulares los mismos derechos económicos.

Las participaciones sociales podrán ser de dos clases: LABORAL Y GENERAL.

Las participaciones sociales de la clase laboral, serán las numeradas del uno a [Nº] inclusive, deberán, en todo caso, representar al menos la mayoría del capital social y pertenecer necesariamente a personas que reúnan las condiciones legales para ser consideradas trabajadores de la sociedad con relación laboral por tiempo indefinido.

Las restantes participaciones sociales serán de la clase general, numeradas de [Nº]. al [Nº], inclusive, y estarán reservadas, en principio, a quienes no reúnan las condiciones personales anteriormente indicadas.

La transmisión de participaciones sociales que implique un cambio de clase por razón de su propietario facultará al Órgano de Administración, con independencia de que la Junta General haya o no tomado el correspondiente acuerdo, para formalizar dicho cambio, pudiendo, al efecto, otorgar la documentación pertinente.

Artículo 6º.- Límites de titularidad

Ningún socio, salvo que se trate de las entidades a las que se refiere el artículo 1.2. apartado b de la Ley 44/2015 de 14 de octubre de Sociedades Laborales y Participadas, podrá ser titular de participaciones que representen más de la tercera parte del capital social. Sin perjuicio de lo anterior, ningún socio podrá ser titular de participaciones que representen el cincuenta por ciento o más del capital social.

Artículo 7º.- Prohibición

La Sociedad no podrá contratar trabajadores con relación laboral por tiempo indefinido que no sean socios si con ello el número de horas-año trabajadas por estos supera el cuarenta y nueve por ciento (49%) del cómputo global de horas-año trabajadas por el conjunto de los socios trabajadores, con las excepciones legalmente previstas.

Artículo 8º.- Libro Registro de Socios

La Sociedad llevará un Libro Registro de Socios, que custodiará y llevará el Órgano de Administración, en el que deberán inscribirse la titularidad dominical de las participaciones sociales, haciendo constar el nombre, apellidos, nacionalidad y domicilio de los socios, las sucesivas trasmisiones que se efectúen, así como la constitución, modificación y cancelación de cualquier carga o derecho real que las grave.

Artículo 9º.- Indivisibilidad

Toda participación social es indivisible y la Sociedad no reconoce más que un titular por cada participación. Quedan obligados los copartícipes en una o varias participaciones pro indivisas a designar a una sola persona que las represente ante la Sociedad.

Artículo 10º.- Transmisión

La transmisión de participaciones sociales se regirá por las siguientes normas:

Será enteramente libre, sin más requisitos que su comunicación al Órgano de Administración y el de su toma de razón en el Libro Registro de Socios, la transmisión de participaciones de la CLASE LABORAL que se realice entre personas que tengan, de conformidad con la Ley, la condición de trabajadores de la sociedad con contrato por tiempo indefinido, sean o no socios. En cualquier otro supuesto, el socio que pretenda transmitir todas o cualquiera de sus participaciones sociales, deberá comunicar su oferta por escrito, el cual reunirá los requisitos establecidos en el artículo 6 de la Ley de Sociedades Laborales y Participadas, remitiéndola, por correo certificado con acuse de recibo o por cualquier otro medio que asegure y acredite su recepción, al Órgano de Administración. Este lo notificará, dentro de los diez días siguientes a su recepción y también por escrito, a todos los posibles interesados, los cuales, a estos efectos, deberán haber indicado un domicilio para notificaciones, y, en todo caso, mediante anuncio fijado en el tablón de anuncios del domicilio social. Los notificados, cumpliendo los requisitos y respetando el orden de preferencia que establece el artículo 6 de la Ley de Sociedades Laborales y Participadas, podrán optar a su compra, dentro de los veinte días siguientes a la fecha del recibo de dicha notificación.

En el caso de que ninguno de los interesados, incluida la Sociedad, adquiriera las participaciones ofertadas, su titular podrá transmitirlas libremente en el plazo de dos meses, transcurridos los cuales se deberán iniciar nuevamente los trámites establecidos.

En el supuesto de que se ejecute el derecho de preferente adquisición, el precio de transmisión de las participaciones sociales se determinará en la forma que se establece en la Ley de Sociedades Laborales y Participadas.

Artículo 11º.- Transmisión Mortis causa

Las trasmisiones mortis causa de cualquier clase de participaciones será enteramente libre, sin perjuicio, no obstante, de la preferencia que establece en el artículo 10 de la Ley de Sociedades Laborales y Participadas.

Artículo 12º.- Obligatoriedad

Las transmisiones de participaciones que no se ajusten a lo dispuesto en estos estatutos y en la legislación vigente, no producirán efecto alguno frente a la sociedad.

Artículo 13º.- Derechos

Además de los reconocidos por la legislación vigente, son derechos fundamentales de los socios:

a) Tomar parte en las Juntas Generales con voz y voto, e impugnar los acuerdos.
b) Poder ser elegidos y reelegidos en su caso para los cargos sociales, si personalmente no tienen limitaciones que impidan desempeñarlos.
c) Solicitar del Órgano de Administración las aclaraciones o informes que consideren necesarios sobre el estado de la Administración y la Contabilidad de la Sociedad.
• El derecho de información establecido en el párrafo anterior se ejercitará en los términos que establecen las leyes.
• Es obligación de los socios, mantener absoluto secreto de los datos que hubieran conocido como consecuencia de la información recibida.
d) Suscribir preferentemente las participaciones en el caso de nuevas emisiones.
e) Participar en la distribución de las ganancias y en el haber social en el supuesto de liquidación.

TÍTULO III.- ÓRGANOS SOCIALES

Artículo 14º.- Disposición general

El gobierno y administración de la Sociedad corresponde a la Junta General y al Órgano de Administración, dentro de sus respectivas competencias.

Artículo 15º.- Junta General. Funcionamiento

Las Juntas Generales, que podrán ser ordinarias y extraordinarias, se regirán con sujeción estricta a las normas que les sean aplicables del Título V de la Ley de Sociedades de Capital, que se observarán, asimismo, en todo lo relativo a su competencia, solicitud de convocatoria, asistencia y derecho de voto, constitución, derecho de información e impugnación, forma de deliberar y tomar acuerdos y en todo cuanto no esté previsto en estos Estatutos.

El Órgano de Administración convocará las Juntas publicando el correspondiente anuncio en la página web de la sociedad o, en el caso de que no exista, publicando el correspondiente anuncio en el Tablón de Anuncios del domicilio social y comunicándoselo a cada socio por medio de escrito, que remitirá por correo certificado con acuse de recibo, dirigido al domicilio que, para notificaciones y requerimientos, conste en el Libro Registro de Socios, y que deberá estar fijado en territorio nacional. El escrito de convocatoria deberá reunir los requisitos legales y practicarse con la antelación necesaria.

También se considerará válidamente constituida la Junta para resolver sobre cualquier asunto, sin necesidad de previa convocatoria, cuando hallándose reunidos o debidamente representados la totalidad de los socios que representen el capital social, los asistentes, decidan, por unanimidad, celebrarla en aquel mismo lugar y acto.

Actuarán como Presidente y Secretario las personas que ejerzan, a su vez, algún cargo dentro del Órgano de Administración y sean designados, por mayoría simple, por los socios presentes o representados, quienes, en todo caso y con carácter preferente, decidirán sobre y elegirán a las personas que deban desempeñar dicha función.

Cada participación social da derecho a un voto y el socio se podrá hacer representar, además por las personas relacionas en el artículo 183 de la Ley de Sociedades de Capital, por cualquier otra, sea o no socio. Las certificaciones de sus acuerdos serán expedidas por el Órgano de Administración.

Artículo 16º.- La Junta General Ordinaria

Se reunirá, necesariamente, dentro de los seis primeros meses de cada ejercicio, para aprobar, si procede, la gestión social y las cuentas del último ejercicio y resolver sobre la aplicación de los resultados.

Artículo 17º.- Gestión y representación de la sociedad

La gestión y representación de la Sociedad corresponderá, a elección de la Junta General de Socios, que necesitará para adoptar el acuerdo la mayoría de los votos reforzada que establece el artículo 199. b), de la Ley de Sociedades de Capital, a:

1. Un Consejo de Administración que actuará colegiadamente, se compondrá de un número de Consejeros no inferior a tres ni superior a cinco y se organizará y funcionará del modo que se establece en los Artículos 22 y 23 de estos mismos Estatutos.

La Junta General nombrará los miembros del Consejo de Administración y determinará el cargo que cada uno de los elegidos deberá desempeñar. No obstante, si la Junta no lo hubiera hecho, el propio Consejo podrá designar los cargos.

2. Un Administrador Único.
3. Entre un mínimo de dos y hasta un máximo de tres administradores con facultades solidarias.
4. Entre un mínimo de dos y hasta un máximo de tres Administradores mancomunados, de los que al menos dos actuarán de forma conjunta.

Sólo con la mayoría reforzada, establecida en el artículo 199. b), de la Ley de Sociedades de Capital, podrá ser designado Administrador quien no sea socio.

En ningún caso podrá ocupar cargo alguno en el Órgano de Administración de la Sociedad las personas a que les afecten las prohibiciones e incompatibilidades que establece la legislación vigente.

Artículo 18º.- Duración y retribución

El cargo de administrador tiene una duración de [PLAZO], sin perjuicio de la facultad que tiene la Junta de revocar en cualquier momento su nombramiento.

El cargo de administrador será gratuito sin perjuicio de las remuneraciones que los administradores pudieran percibir por la prestación de servicios bajo una relación laboral, común o especial, o a través de un contrato de prestación de servicios profesionales, cuyas funciones sean distintas de las inherentes al cargo de administrador.

Artículo 19º.- Representación de la sociedad

La representación de la Sociedad en juicio y fuera de él corresponde al Órgano de Administración, que ejercitará, sin limitación alguna, todas las facultades que, para el desarrollo del objeto social y dentro del giro y tráfico de la empresa, que no estén reservadas a la Junta General de Socios por la Ley o los Estatutos.

En consecuencia, podrá realizar toda clase de actos, negocios jurídicos y contratos de administración, disposición, gravamen y riguroso dominio con relación a toda clase de bienes.

Artículo 20º.- Consejo de Administración

Para el supuesto de que el sistema de Administración elegido por la Junta General sea el de Organismo Colegiado, se establece:

El Consejo deberá reunirse, por lo menos, una vez al trimestre.

La reunión será convocada por el Presidente, por propia iniciativa, o a petición, formulada por escrito, de al menos un tercio de los miembros que lo integran. Bastará que el anuncio de convocatoria se publique, con una antelación mínima de siete días hábiles a la fecha de su celebración, en el lugar destinado al efecto en el domicilio social.

Actuarán de Presidente y Secretario los que lo sean de dicho Órgano y, en su defecto, los Consejeros que resulten elegidos por mayoría simple de los presentes.

Quedará válidamente constituido cuando acudan a la reunión, presentes o representados, la mayoría de sus componentes y sus acuerdos, salvo aquéllos para los que legalmente se exija una mayoría específica, se tomaran por mayoría absoluta de los asistentes o representados, siendo el voto del Presidente, en caso de empate, dirimente o de calidad.

No obstante lo dispuesto anteriormente serán válidos los acuerdos que se adopten en la forma que prescribe el artículo 248. 2. de la Ley de Sociedades de Capital.

Los acuerdos se transcribirán en un libro de Actas del que el Secretario expedirá, con el Visto Bueno del Presidente, las Certificaciones oportunas.

En todo lo no previsto el Consejo regulara, como por bien tuviere y con el carácter de normas de régimen interno, su propio funcionamiento, dictando las que considere necesarias al efecto. Estas reglas, que deberán estarlo por escrito, podrán ser conocidas por cualquier socio.

Artículo 21º.- Delegación de facultades

El nombramiento de una Comisión Ejecutiva o de uno o varios Consejeros Delegados y la determinación de la extensión, contenido y límites de las facultades que se les deleguen, se realizará por el propio Consejo que, sin embargo, no podrá delegar, aquellas facultades que sean indelegables con arreglo a la Ley. La delegación permanente de alguna facultad requerirá el voto cualificado de las dos terceras partes de los miembros del Consejo.

Los Administradores deberán cumplir estrictamente todos y cada uno de los deberes regulados en el Capítulo III, del Título VI, de la Ley de Sociedades de Capital.

TÍTULO IV.- EJERCICIO SOCIAL Y CUENTAS ANUALES

Artículo 22º.- Ejercicio social

Los ejercicios sociales comienzan el 1 de enero y finalizan el 31 de diciembre de cada año natural.

Por excepción, el primer ejercicio social comprende desde el principio de las operaciones de la Sociedad hasta el 31 de diciembre de ese mismo año.

Artículo 23º.- Cuentas Anuales

Las cuentas y el informe de gestión, así como, en su caso, su revisión por auditores de cuentas, deberán ajustarse a las normas legales y reglamentarias vigentes en cada momento.

El Órgano de Administración está obligado a formular, en el plazo máximo de tres meses, contados a partir del cierre de cada ejercicio social, las cuentas anuales, el informe de gestión y la propuesta de aplicación del resultado, así como, en su caso, las cuentas y el informe de gestión consolidados, en la forma prevista por el Texto Refundido de la Ley de Sociedades de Capital y demás normativa aplicable.

Cualquier socio tendrá derecho a obtener, en la forma y plazo legalmente previstos (15 días antes de la Junta), copia inmediata y gratuita de los documentos antes referidos, así como del informe de gestión y, en su caso, del informe de los auditores.

Además, el socio o socios que representen al menos el 5% del capital social, podrán examinar en el domicilio social, por sí o en unión de un experto contable, los documentos que sirvan de soporte y antecedente de las cuentas anuales, sin perjuicio del derecho de la minoría a nombrar un auditor de cuentas con cargo a la Sociedad.

Artículo 24º.- Aplicación del resultado y Fondo de Reserva Especial

La aplicación del resultado del ejercicio es competencia de la Junta General, con los límites legales y estatutarios.

La Sociedad está obligada a constituir un Fondo de Reserva Especial que se dotará con el 10% del beneficio líquido de cada ejercicio, hasta que alcance al menos una cifra superior al doble del capital social.

El Fondo Especial de Reserva sólo podrá destinarse a la compensación de pérdidas en el caso de que no existan otras reservas disponibles suficientes para este fin y/o a la adquisición de sus propias participaciones sociales, que deberán ser enajenadas a favor de los trabajadores de la sociedad con contrato por tiempo indefinido, de acuerdo con lo dispuesto en el artículo 12 de la Ley de sociedades laborales y participadas.

Artículo 25º.- Reparto de beneficios

Los socios tendrán derecho a los beneficios repartibles en proporción a su participación en el capital social.

TÍTULO V.- SEPARACIÓN Y EXCLUSIÓN DE SOCIOS

Artículo 26º.- Separación de socios

Tendrán derecho a separarse de la Sociedad los socios que no voten a favor de los siguientes acuerdos:

* Sustitución del objeto social.
* Traslado del domicilio social al extranjero, cuando exista un Convenio internacional vigente en España que lo permita con mantenimiento de la misma personalidad jurídica de la sociedad.
* Modificación del régimen de transmisión de las participaciones sociales.
* Prórroga o reactivación de la sociedad.
* Transformación en sociedad anónima, sociedad civil, cooperativa, colectiva o comanditaria, simple o por acciones, así como en agrupación de interés económico.
* Creación, modificación o extinción anticipada de la obligación de realizar prestaciones accesorias, salvo disposición contraria de los estatutos.

Los socios que lo ejerciten tendrán derecho al reembolso de sus participaciones sociales.

Para ello se exigirá que el acuerdo que haya dado lugar al derecho de separación se haya publicado en el Boletín Oficial del Registro Mercantil, o bien, cuando así lo acuerde el Administrador, esa publicidad puede ser sustituida por una comunicación escrita a cada uno de los socios que no hayan votado a favor del acuerdo de que se trate.

El derecho de separación podrá ejercitarse en tanto no transcurra el plazo de 1 mes contado desde la publicación del acuerdo o desde la recepción de la comunicación

Artículo 27º.- Exclusión de socios

Podrán ser excluidos los socios incumplan la obligación de realizar prestaciones accesorias o, si además cuentan con la condición de administradores, cuando infrinjan la prohibición de competencia, o hayan sido condena dos por sentencia firme a indemnizar a la sociedad los daños y perjuicios causados por actos contrarios a la Ley de Sociedades de Capital o a los estatutos o realizados sin la debida diligencia.

La exclusión de uno o varios socios deberá ser acordada por la Junta General, debiendo hacerse constar en el acta de la reunión la identidad de los socios que hayan votado a favor del acuerdo.

Salvo en caso de condena al socio administrador a indemnizar a la sociedad, la exclusión del socio con participación igual o superior al 25% en el capital social requerirá además del acuerdo de la junta, resolución judicial firme, siempre que el socio no se conforme con la exclusión acordada.

Cualquier socio que haya votado a favor del acuerdo estará legitimado para ejercitar la acción de exclusión en nombre de la sociedad si ésta no lo efectúa en el plazo de un mes desde la fecha de adopción del citado acuerdo.

TÍTULO VI.- DISOLUCIÓN Y LIQUIDACIÓN DE LA SOCIEDAD

Artículo 28º.- Disolución

La sociedad se disolverá por las causas legalmente establecidas.

[OTROS DATOS]

Artículo 29º.- Liquidación

La disolución de la sociedad abrirá el período de liquidación, quedando convertido en liquidador quien ostentare en tal momento la condición de Administrador único, salvo en caso de que la Junta General acuerde la designación de otro u otros liquidadores.

Para la liquidación de la sociedad se estará a lo previsto en la Ley de Sociedades de Capital.

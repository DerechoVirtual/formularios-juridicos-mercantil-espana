---
name: escritura-publica-escision-parcial-sl-sa-mer-0328
description: "Escritura pública de escisión parcial de una SL o SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de escisión parcial de una SL o SA

> Formulario **MER-0328** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de escisión parcial de una SL o SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de escisión parcial de una SL o SA” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:escritura-publica-escision-parcial-sl-sa-mer-0328`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (26 veces)
- [ ] IMPORTE (15 veces)
- [ ] NOMBRE O DENOMINACIÓN (15 veces)
- [ ] FECHA (14 veces)
- [ ] Nº (14 veces)
- [ ] LOCALIDAD (10 veces)
- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] Nº DE ACCIONES/PARTICIPACIONES (9 veces)
- [ ] ESTADO CIVIL (3 veces)
- [ ] NACIONALIDAD (3 veces)
- [ ] ACUERDO ADOPTADO (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] MAYORÍA (2 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE DEL DIARIO (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] TEXTO DE LA CONVOCATORIA (2 veces)
- [ ] TEXTO DEL ARTÍCULO (2 veces)
- [ ] ÓRGANO O PERSONA (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] DESCRIPCIÓN DEL DOCUMENTO
- [ ] LUGAR
- [ ] MOTIVO
- [ ] OBLIGACIONES Y DEUDAS
- [ ] PLAZO
- [ ] PROCEDIMIENTO DE REDUCCIÓN DE CAPITAL
- [ ] RELACIÓN DE ACCIONES/PARTICIPACIONES PROPIAS
- [ ] SERIE
- [ ] SISTEMA DE ADMINISTRACIÓN
- [ ] TOMO

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

Escritura pública por la que se formaliza el traspaso en bloque por sucesión universal de una o varias partes del patrimonio de una sociedad, cada una de las cuales forme una unidad económica, a una o varias sociedades de nueva creación o ya existentes, recibiendo los socios de la sociedad que se escinde un número de acciones, participaciones o cuotas sociales de las sociedades beneficiarias de la escisión proporcional a su respectiva participación en la sociedad que se escinde y reduciendo ésta el capital social en la cuantía necesaria.

NÚMERO

ESCRITURA DE ESCISIÓN PARCIAL

SOCIEDAD ESCINDIDA «[NOMBRE O DENOMINACIÓN]»

SOCIEDAD(ES) BENEFICIARIA(S) «[NOMBRE O DENOMINACIÓN]» y «[NOMBRE O DENOMINACIÓN]»

En [LUGAR], a [FECHA].

Ante mí, Notario de [LOCALIDAD], del Ilustre Colegio Notarial de [LOCALIDAD],

COMPARECEN

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI núm. [DNI/NIE], de nacionalidad [NACIONALIDAD], de estado civil [ESTADO CIVIL], vecino/a de la localidad de [LOCALIDAD], con domicilio en la

Actúa en nombre y representación de la sociedad «[DENOMINACIÓN SOCIAL]», constituida mediante escritura otorgada en fecha [FECHA] ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS]. La sociedad tiene el número de NIF [NIF] y está inscrita en el Registro Mercantil de [LOCALIDAD], tomo [TOMO]. La Sociedad tiene un capital social de [IMPORTE], dividido en de [ELEGIR: acciones / participaciones], de [IMPORTE] euros de valor nominal cada una de ellas, numeradas correlativamente del 1 al [Nº] ambos inclusive, estando totalmente suscritas e íntegramente desembolsadas.

Dicha Sociedad tiene por objeto social:

[ELEGIR UNA OPCIÓN: Cargo / Acuerdo del Consejo]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI núm. [DNI/NIE], de nacionalidad [NACIONALIDAD], de estado civil [ESTADO CIVIL], vecino/a de la localidad de [LOCALIDAD], con domicilio en la

Interviene en su propio nombre.

Me aseguro de la identidad de todos los comparecientes por sus reseñados documentos y considero que tienen capacidad y legitimación suficientes para otorgar esta escritura y, al efecto,

EXPONEN

1) Que los órganos de administración de las sociedades «[NOMBRE O DENOMINACIÓN]» y «[NOMBRE O DENOMINACIÓN]» redactaron aprobaron y suscribieron un proyecto de escisión con fecha [FECHA], con el contenido y requisitos aplicables y que al efecto establecen los art. 39 y 40 del RD-ley 5/2023 sobre modificaciones estructurales de las sociedades mercantiles.

[OPCIONAL — incluir si procede]

(Con página web)

El citado proyecto ha quedado insertado en la página web de cada una de las sociedades que participan en la escisión.

La inserción en la web del proyecto y la fecha de la misma se acredita mediante la certificación del contenido de aquélla publicado en el 'Boletín Oficial del Registro Mercantil.

[OPCIONAL — incluir si procede]

(Sin página web)

Un ejemplar del citado proyecto ha sido depositado en el Registro Mercantil de [LOCALIDAD] el día [FECHA]. El depósito fue publicado en el Boletín Oficial del Registro Mercantil de fecha [FECHA].

El depósito y la publicación del mismo se acredita mediante la certificación [DESCRIPCIÓN DEL DOCUMENTO]

[OPCIONAL — incluir si procede]

(Cuando no requiere publicación ni depósito)

El citado proyecto de escisión no ha sido objeto ni de publicación, ni de depósito al haber sido aprobado por unanimidad de todos los socios en Junta Universal. Queda unido a la presente con la firma de los administradores que legítimo.

2) Los órganos de administración de cada una de las sociedades elaboraron sus respectivos informes sobre el proyecto de escisión con fecha [FECHA].

[ELEGIR UNA OPCIÓN: Con informe de experto independiente / Sin informe de experto independiente]

4) Los órganos de administración de cada una de las sociedades confeccionaron sus respectivos balances de escisión, que fueron cerrados a fecha [FECHA] aprobados el .Estos balances no fueron auditados por no existir obligación legal de hacerlo.

4) Las sociedades que participan en la escisión utilizaron como balance de escisión el último balance anual aprobado, cerrado el día [FECHA]

Los comparecientes hacen constar que no se han producido modificaciones importantes en el Activo y Pasivo de las respectivas sociedades desde la fecha del Proyecto hasta la fecha de la aprobación de la escisión.

Un ejemplar de dichos balances firmados por sus administradores se unen a esta matriz, siendo dichas firmas por mi legitimadas por coincidir con la de su DNI o pasaporte.

5) Convocatoria de las juntas.

A) Convocatoria de junta de la sociedad que se escinde «[DENOMINACIÓN SOCIAL]».

La sociedad «[DENOMINACIÓN SOCIAL]» publicó anuncio de convocatoria en [NOMBRE DEL DIARIO] el día [FECHA]. El contenido de dicha convocatoria es el siguiente: [TEXTO DE LA CONVOCATORIA].

B) Convocatoria de junta de las sociedades beneficiarias de la escisión «[NOMBRE O DENOMINACIÓN]».

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

La sociedad «[DENOMINACIÓN SOCIAL]» publicó anuncio de convocatoria en [NOMBRE DEL DIARIO] el día [FECHA]. El contenido de dicha convocatoria es el siguiente: [TEXTO DE LA CONVOCATORIA].

6) Acuerdos de las juntas.

-A) Junta de la sociedad escindida «[DENOMINACIÓN SOCIAL]».

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

La junta general se celebró en el domicilio social sito en [LOCALIDAD] el día [FECHA],antes de la finalización del transcurso de los seis meses siguientes a la fecha del Proyecto y

por unanimidad

con el voto favorable de [MAYORÍA] fueron adoptados los siguientes acuerdos: [ACUERDO ADOPTADO].

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

-B) Junta de la sociedad beneficiaria «[DENOMINACIÓN SOCIAL]».

La junta general se celebró el día [FECHA] y con el voto favorable de [MAYORÍA] fueron adoptados los siguientes acuerdos: [ACUERDO ADOPTADO].

[ELEGIR UNA OPCIÓN: Publicados / Comunicados]

8) Durante el plazo legal de un mes, contado desde la fecha del último de los anuncios, ningún acreedor de las sociedades que participan en la operación se opuso a la escisión.

8) Durante el plazo legal de un mes, contado desde la fecha del último de los anuncios, se han opuesto a la escisión los siguientes acreedores de las sociedades participantes en la operación:

9) Los comparecientes entregan los siguientes documentos, que extendidos en [Nº] folios son prueba de lo que se ha expuesto y que incorporo a esta matriz:

1.º Proyecto de escisión, con las firmas legitimadas de todos los administradores.
2.º Informes de los administradores sobre el proyecto de escisión.
3.º Informe de experto independiente sobre el proyecto de escisión.
4.º Balances de escisión y informes de auditoría.
5.º Relación de elementos del activo y del pasivo que se transmiten en bloque a cada una de las sociedades beneficiarias de la escisión.
6.º Copia de los anuncios de convocatoria y del acuerdo de escisión, cuya correspondencia con el original compruebo por exhibición de sendos ejemplares de las publicaciones citadas.
7.º Estatutos sociales de la nueva sociedad creada como consecuencia de la escisión.
8.º Certificación negativa del Registro Mercantil Central de que no se encuentra registrada la denominación de la nueva sociedad creada como consecuencia de la escisión.
9.º Certificación social de la sociedad escindida «[DENOMINACIÓN SOCIAL]», expedida por [ÓRGANO O PERSONA], con firma legitimada.
10.º Certificación social de la sociedad beneficiaria «[DENOMINACIÓN SOCIAL]», expedida por [ÓRGANO O PERSONA], con firma legitimada.

ESTIPULACIONES

Primera.- Escisión

La sociedad «[DENOMINACIÓN SOCIAL]» se escinde parcialmente y transfiere uno de los bloques patrimoniales que se escinde a la sociedad «[DENOMINACIÓN SOCIAL]» ya preexistente y el otro bloque patrimonial que se escinde a la sociedad «[DENOMINACIÓN SOCIAL]» de nueva creación y que se regirá por los estatutos incorporados a esta escritura.

La escisión implica el traspaso por sucesión universal de cada uno de los bloques patrimoniales que se escinde, que forman una unidad económica, a cada una de las sociedades beneficiarias de la escisión, recibiendo los socios de la sociedad que se escinde un número de acciones, participaciones o cuotas de las sociedades beneficiarias proporcional a su respectiva participación en la sociedad que se escinde y reduciendo ésta el capital social en la cuantía de [IMPORTE] euros.

[OPCIONAL — incluir si procede]

(Si se constituye la nueva sociedad)

Se constituye en este acto la sociedad «[DENOMINACIÓN SOCIAL]», con domicilio en [LOCALIDAD] y que tendrá un capital de [IMPORTE] euros, dividido en [Nº] de [IMPORTE] euros de valor nominal cada una, números [Nº] a [Nº]. Esta sociedad se regirá por los estatutos que se incorporan a esta escritura. Me entregan certificación del Registro Mercantil Central, original y vigente, con la que acreditan que no figura registrada la denominación elegida. Protocolizo la certificación que me es entregada en esta matriz.

Según el proyecto de escisión aprobado, a partir de [FECHA] las operaciones de las sociedades respecto de los bloques patrimoniales que se traspasan se consideran realizadas a efectos contables como independientes.

Segunda.- Transmisión patrimonial

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

La parte del patrimonio de la sociedad escindida «[DENOMINACIÓN SOCIAL]» que ha de transmitirse a «[NOMBRE O DENOMINACIÓN]» forma una unidad económica y está compuesta por los siguientes elementos del activo y del pasivo:

Bienes y derechos: [DESCRIPCIÓN DEL BIEN].

Obligaciones y deudas: [OBLIGACIONES Y DEUDAS].

El valor del patrimonio que se escinde asciende a [IMPORTE] euros.

Tercera. - Asignación de [ELEGIR: acciones / participaciones]

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

1. Los socios de la sociedad que se escinde participan en todas y cada una de las sociedades beneficiarias de la escisión y, además, siguen siendo socios de la sociedad que se escinde parcialmente.

2. Las [ELEGIR: acciones / participaciones] de las sociedades beneficiarias se asignan a los socios de la sociedad que se escinde, según se establece en el proyecto de escisión, en la proporción de [Nº DE ACCIONES/PARTICIPACIONES] de « [DENOMINACIÓN SOCIAL] » por cada [Nº DE ACCIONES/PARTICIPACIONES] de «[NOMBRE O DENOMINACIÓN]» [DENOMINACIÓN SOCIAL], y de [Nº DE ACCIONES/PARTICIPACIONES] de «[NOMBRE O DENOMINACIÓN]» por cada [Nº DE ACCIONES/PARTICIPACIONES] de «[NOMBRE O DENOMINACIÓN]» [DENOMINACIÓN SOCIAL].

[OPCIONAL — incluir si procede]

(Si procede compensación en metálico)

Además, los socios de «[NOMBRE O DENOMINACIÓN]» reciben una compensación dineraria de [IMPORTE] euros por cada [ELEGIR: acción / participación] asignada. La compensación será pagada.

Las nuevas [ELEGIR: acciones / participaciones] darán derecho a participar en las ganancias sociales desde [FECHA].

3 La asignación concreta a los socios se realiza dela siguiente forma:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] de la sociedad escindida «[DENOMINACIÓN SOCIAL]», con un valor nominal de [IMPORTE] euros, se le asignan [Nº DE ACCIONES/PARTICIPACIONES] de la sociedad «[DENOMINACIÓN SOCIAL]» [DENOMINACIÓN SOCIAL], con un valor nominal total de [IMPORTE] euros, números [Nº] a

4 Las [ELEGIR: acciones / participaciones] de las sociedades participantes en la escisión y que están en poder de cualquiera de ellas quedan extinguidas. Estas [ELEGIR: acciones / participaciones] ascienden a un total de [IMPORTE] euros y son las siguientes: [RELACIÓN DE ACCIONES/PARTICIPACIONES PROPIAS].

1 No todos los socios de la sociedad que se escinde permanecen en esta sociedad ni reciben [ELEGIR: acciones / participaciones] de todas las sociedades beneficiarias, habiéndose obtenido el consentimiento individual de los afectados exigido en el artículo 66 del RD-ley 5/2023, de modificaciones estructurales de las sociedades mercantiles.

2 Relación de canje. Las [ELEGIR: acciones / participaciones] de las sociedades beneficiarias se asignan a los socios de la sociedad que se escinde que prestaron su consentimiento individual a tal asignación, según se prevé en el proyecto de escisión, en la proporción de [Nº DE ACCIONES/PARTICIPACIONES] de «[NOMBRE O DENOMINACIÓN]» por cada [Nº DE ACCIONES/PARTICIPACIONES] de «[NOMBRE O DENOMINACIÓN]» [DENOMINACIÓN SOCIAL], y de [Nº DE ACCIONES/PARTICIPACIONES] de «[NOMBRE O DENOMINACIÓN]» por cada [Nº DE ACCIONES/PARTICIPACIONES] de «[NOMBRE O DENOMINACIÓN]» [DENOMINACIÓN SOCIAL].

3. Asignación concreta. La asignación concreta a los socios se realiza del siguiente modo:

A) Socios de la sociedad escindida «[DENOMINACIÓN SOCIAL]».

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]: núm. [Nº] a [Nº], de [IMPORTE] euros de valor nominal cada una.

B) Socios de la sociedad beneficiaria «[DENOMINACIÓN SOCIAL]».

C) Socios de la sociedad beneficiaria «[DENOMINACIÓN SOCIAL]».

4.º Extinción de las participaciones propias y recíprocas. Las [ELEGIR: acciones / participaciones] de las sociedades participantes en la escisión y que están en poder de cualquiera de ellas quedan extinguidas. Estas [ELEGIR: acciones / participaciones] ascienden a un total de [IMPORTE] euros y son las siguientes:

Cuarta.- Modificaciones de estatutos

Como consecuencia de la escisión, la sociedad escindida «[DENOMINACIÓN SOCIAL]» reduce su capital social en la cantidad de [IMPORTE] euros, por medio del siguiente procedimiento: [PROCEDIMIENTO DE REDUCCIÓN DE CAPITAL]. Se produce la consiguiente modificación del artículo [Nº DE ARTÍCULO] estatutos sociales, que queda redactado del siguiente modo: [TEXTO DEL ARTÍCULO].

La sociedad beneficiaria «[DENOMINACIÓN SOCIAL]» aumenta su capital en la cantidad de [IMPORTE] euros, dividido en [Nº], de [IMPORTE] euros de valor nominal cada una, numeradas del [Nº] al [Nº] En consecuencia, se modifica el artículo [Nº DE ARTÍCULO] de los estatutos sociales, relativo al capital social, que queda redactado del siguiente tenor: [TEXTO DEL ARTÍCULO].

Quinta.- Nombramiento de cargos sociales

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

La organización inicial de la administración de la nueva sociedad que se crea será por el sistema de [SISTEMA DE ADMINISTRACIÓN].

Y se nombran como administradores de esta nueva sociedad a las siguientes personas:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], con DNI/NIF [NIF], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD]

Los nombramientos se hacen por un período de [PLAZO]

[NOMBRE Y APELLIDOS], aceptan el cargo para el cual han sido nombrados, prometen cumplirlo bien y fielmente y manifiestan no estar incurso en causa alguna de incapacidad, prohibición o incompatibilidad.

Las personas nombradas constituyen el consejo de administración y nombran presidente y secretario, que igualmente aceptan este cargo, de forma que el consejo queda constituido del siguiente modo: Presidente D./Dña. [NOMBRE Y APELLIDOS], Secretario D./Dña. [NOMBRE Y APELLIDOS], Vocal D./Dña. [NOMBRE Y APELLIDOS], etc.

Sexta.- Régimen fiscal

Según el proyecto de escisión, el motivo económico de la operación es [MOTIVO], lo que le permite acogerse al régimen especial establecido en el Capítulo VII del Título VII Ley 27/2014, de 27 de noviembre, por la que se aprueba la Ley del Impuesto sobre Sociedades.

OTORGAMIENTO Y AUTORIZACIÓN

Hago a los comparecientes las reservas y advertencias legales, especialmente las derivadas de la legislación fiscal, y del Registro Mercantil y de su publicidad.

Leo esta escritura a los comparecientes advirtiéndoles del derecho que tienen a hacerlo personalmente, derecho al que renuncian. Enterados de su contenido, los comparecientes hacen constar libremente su consentimiento al contenido de la escritura y la firman.

Yo, el Notario, compruebo que este otorgamiento se ajusta a la legalidad y a la voluntad de las partes expresada ante mí, y de todo lo consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales de serie [SERIE], números [Nº], DOY FE.

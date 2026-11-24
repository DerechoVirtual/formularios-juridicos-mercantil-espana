---
name: escritura-publica-fusion-absorcion-sl-sa-mer-0332
description: "Escritura pública de fusión por absorción de SL o SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de fusión por absorción de SL o SA

> Formulario **MER-0332** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Las sociedades que se fusionan elevarán el acuerdo de fusión adoptado a escritura pública, a la cual se incorporará el balance de fusión de aquéllas o, en el caso de fusión de sociedades cotizadas, el informe financiero semestral por el que el balance se hubiera sustituido. Si se realizara por absorción, la escritura contendrá las modificaciones estatutarias que se hubieran acordado por la sociedad absorbente con motivo de la fusión y el número, clase y serie de las acciones o las participaciones o cuotas que hayan de ser atribuidas, en cada caso, a cada uno de los nuevos socios.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de fusión por absorción de SL o SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de fusión por absorción de SL o SA” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:escritura-publica-fusion-absorcion-sl-sa-mer-0332`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (20 veces)
- [ ] Nº (12 veces)
- [ ] IMPORTE (10 veces)
- [ ] FECHA (9 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] DOMICILIO (4 veces)
- [ ] NACIONALIDAD (3 veces)
- [ ] NOMBRE O DENOMINACIÓN (3 veces)
- [ ] Nº DE PARTICIPACIONES O ACCIONES (3 veces)
- [ ] ÓRGANO O PERSONA (3 veces)
- [ ] CAPITAL SOCIAL (2 veces)
- [ ] MEDIO DE PUBLICACIÓN (2 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE TÍTULOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] OBJETO SOCIAL (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] TIPO DE ÓRGANO DE ADMINISTRACIÓN (2 veces)
- [ ] TOMO (2 veces)
- [ ] VOTOS A FAVOR (2 veces)
- [ ] CAUSA
- [ ] ESTADO CIVIL
- [ ] FOLIO
- [ ] FOLIO Y HOJA
- [ ] FORMA Y FECHA DE PAGO
- [ ] LUGAR
- [ ] MOTIVO
- [ ] Nº DE ARTÍCULO
- [ ] OTROS DATOS
- [ ] RELACIÓN DE PARTICIPACIONES PROPIAS
- [ ] SERIE

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

Las sociedades que se fusionan elevarán el acuerdo de fusión adoptado a escritura pública, a la cual se incorporará el balance de fusión de aquéllas o, en el caso de fusión de sociedades cotizadas, el informe financiero semestral por el que el balance se hubiera sustituido. Si se realizara por absorción, la escritura contendrá las modificaciones estatutarias que se hubieran acordado por la sociedad absorbente con motivo de la fusión y el número, clase y serie de las acciones o las participaciones o cuotas que hayan de ser atribuidas, en cada caso, a cada uno de los nuevos socios.


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

NÚMERO

ABSORCIÓN DE LA SOCIEDAD «[NOMBRE O DENOMINACIÓN]» POR «[NOMBRE O DENOMINACIÓN]»

En [LUGAR], a [FECHA].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario de [LOCALIDAD], del Ilustre Colegio Notarial de [LOCALIDAD]

COMPARECEN

DE UNA PARTE

[OPCIONAL — incluir si procede]

(En caso de estado civil no casado)

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domiciliado en [DOMICILIO], y [ELEGIR: DNI / pasaporte] número [NÚMERO],

[OPCIONAL — incluir si procede]

(En caso de estado civil casado)
[ELEGIR UNA OPCIÓN: Con régimen económico matrimonial de gananciales / Cuando el régimen económico matrimonial no fuera el de gananciales]

Actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A]

Compañía mercantil de nacionalidad española denominada [DENOMINACIÓN SOCIAL], [ELEGIR: SL / SA], domiciliada en [DOMICILIO], con NIF núm. [NIF]. Inscrita en el Registro Mercantil de [LOCALIDAD], en [TOMO] el Folio [FOLIO]. Su capital social es de [CAPITAL SOCIAL], dividido en [Nº], [ELEGIR: participaciones / acciones / cuotas] de [IMPORTE] EURO de valor nominal cada una de ellas, numeradas correlativamente del 1 al [Nº] ambos inclusive, estando totalmente suscritas e íntegramente desembolsadas.

Dicha Sociedad tiene por objeto social [OBJETO SOCIAL]

Hace uso de las facultades conferidas a su favor

[ELEGIR UNA OPCIÓN: Cargo / Nombrado por el Consejo]

El representante de la citada Sociedad manifiesta expresamente que no han variado las circunstancias sociales antes indicadas de denominación, forma, objeto y domicilio respecto a los que aparecen en esta escritura; y que de conformidad con el art.20 de la Ley 14/2013, de 27 de septiembre hace consta la Clasificación Nacional de Actividades Económicas (CNAE) que le corresponde

DE OTRA

[OPCIONAL — incluir si procede]

(En caso de estado civil no casado)

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domiciliado en [DOMICILIO], y [ELEGIR: DNI / pasaporte] número [NÚMERO],

[OPCIONAL — incluir si procede]

[ELEGIR UNA OPCIÓN: Casado / Cuando el régimen económico matrimonial no fuera el de gananciales]

Actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A]

Compañía mercantil de nacionalidad española denominada [DENOMINACIÓN SOCIAL], [ELEGIR: SL / SA], domiciliada en [DOMICILIO], calle, con NIF núm. Inscrita en el Registro Mercantil de [LOCALIDAD], en [TOMO] el [FOLIO Y HOJA]. Su capital social es de [CAPITAL SOCIAL], dividido en [Nº], de [IMPORTE] euros de valor nominal cada una de ellas, numeradas correlativamente del 1 al [Nº] ambos inclusive, estando totalmente suscritas e íntegramente desembolsadas.

Dicha Sociedad tiene por objeto social [OBJETO SOCIAL]

Hace uso de las facultades conferidas a su favor

[ELEGIR UNA OPCIÓN: Cargo / Nombramiento]

El representante de la citada Sociedad manifiesta expresamente que no han variado las circunstancias sociales antes indicadas de denominación, forma, objeto y domicilio respecto a los que aparecen en esta escritura; y que de conformidad con el art.20 de la Ley 14/2013, de 27 de septiembre hace consta la Clasificación Nacional de Actividades Económicas (CNAE) que le corresponde

Me aseguro de la identidad de todos los comparecientes por los documentos reseñados y considero que tienen capacidad y legitimación suficientes para otorgar la presente escritura y, al efecto,

EXPONEN

I.- OBJETO

Que la presente escritura tiene por objeto la formalización de la fusión operada entre la Sociedad [DENOMINACIÓN SOCIAL] y la sociedad [DENOMINACIÓN SOCIAL]

II.- Datos del proyecto de fusión

[ELEGIR UNA OPCIÓN: Con página web / Sin página web]

III.- Informe de los administradores

Que los órganos de administración de cada una de las sociedades elaboraron sus respectivos informes sobre el proyecto de fusión con fecha [FECHA], con el contenido legalmente exigido.

IV.- Informe de expertos independientes

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

El proyecto de fusión fue objeto de un único informe de fecha [FECHA], elaborado por [ÓRGANO O PERSONA] como experto independiente nombrado por el Registrador Mercantil de [LOCALIDAD] mediante resolución de fecha

No se elaborado informe de expertos independientes sobre el proyecto de fusión, al no ser legalmente obligatorio por [MOTIVO]

V.- Balance de fusión

[ELEGIR UNA OPCIÓN: Cualquier balance cerrado con no más de 6 meses de antelación / Último Balance anual]

Manifiestan los comparecientes que no se han producido modificaciones importantes en el Activo y Pasivo de las respectivas sociedades desde la fecha del Proyecto hasta la fecha de la aprobación de la fusión.

Un Ejemplar de dichos balances firmados por sus administradores se unen a esta matriz, siendo dichas firmas por mi legitimadas

VI.- Convocatoria de las juntas

Convocatoria de junta de la sociedad absorbente «[DENOMINACIÓN SOCIAL]». La sociedad «[DENOMINACIÓN SOCIAL]» publicó anuncio de convocatoria en [MEDIO DE PUBLICACIÓN] el día [FECHA]. El tenor literal de dicha convocatoria es el siguiente:

Convocatoria de junta de la sociedad absorbida «[DENOMINACIÓN SOCIAL]». La sociedad «[DENOMINACIÓN SOCIAL]» publicó anuncio de convocatoria en [MEDIO DE PUBLICACIÓN] el día [FECHA]. El tenor literal de dicha convocatoria es el siguiente:

VII.- Acuerdos de las juntas

Junta de la sociedad absorbente «[DENOMINACIÓN SOCIAL]». La junta general se celebró el día [FECHA] y con el voto favorable de [VOTOS A FAVOR] fueron adoptados los siguientes acuerdos:

Junta de la sociedad absorbida «[DENOMINACIÓN SOCIAL]». La junta general se celebró el día [FECHA] y con el voto favorable de [VOTOS A FAVOR] fueron adoptados los siguientes acuerdos:

VIII.- Publicación de los acuerdos

[ELEGIR UNA OPCIÓN: Publicación en el BORME / Comunicación]

IX.- Oposición de los acreedores

[ELEGIR UNA OPCIÓN: Sin oposición / Con oposición]

Los comparecientes me entregan los siguientes documentos, que extendidos en [Nº] folios son prueba de lo expuesto quedando incorporados a esta matriz:

1.º Proyecto de fusión, con las firmas legitimadas de todos los administradores.
2.º Informes de los administradores sobre el proyecto de fusión.
3.º Informe de experto independiente sobre el proyecto de fusión.
4.º Balances de fusión e informes de auditoría.
5.º Copia de los anuncios de convocatoria y del acuerdo de fusión, cuya correspondencia con el original compruebo por exhibición de sendos ejemplares de las publicaciones citadas.
6.º Certificación social de la sociedad «[DENOMINACIÓN SOCIAL]», expedida por [ÓRGANO O PERSONA], con firma legitimada.
7.º Certificación social de la sociedad «[DENOMINACIÓN SOCIAL]», expedida por [ÓRGANO O PERSONA], con firma legitimada.

ESTIPULACIONES

Primera.- Fusión

La sociedad «[DENOMINACIÓN SOCIAL]» absorbe a la sociedad «[DENOMINACIÓN SOCIAL]», con aumento de su capital en la cantidad de [IMPORTE] euros, mediante la creación de [Nº DE PARTICIPACIONES O ACCIONES] nuevas [ELEGIR: participaciones / acciones] con un valor nominal de [IMPORTE] euros cada una, numeradas del [Nº] al [Nº], ambos inclusive.

La fusión conlleva la extinción de la sociedad absorbida y la transmisión en bloque de su patrimonio social a la sociedad absorbente, que adquiere por sucesión universal los derechos y obligaciones de la primera.

Según el proyecto de fusión aprobado, a partir de [FECHA] las operaciones de la sociedad absorbida se consideran realizadas a efectos contables por cuenta de la sociedad absorbente.

Segunda.- Asignación de participaciones

• 1.º Las nuevas [ELEGIR: participaciones / acciones] de la sociedad absorbente se asignan a los socios de la sociedad absorbida, según se indica en el proyecto de fusión, en la proporción de [Nº DE TÍTULOS] de la sociedad absorbente «[DENOMINACIÓN SOCIAL]» por cada [Nº DE TÍTULOS] de la sociedad absorbida «[DENOMINACIÓN SOCIAL]» [OTROS DATOS].

Igualmente, los socios de «[NOMBRE O DENOMINACIÓN]» reciben una compensación dineraria de [IMPORTE] euros por cada [ELEGIR: participación / acción] asignada. La compensación será pagada [FORMA Y FECHA DE PAGO].

Las nuevas [ELEGIR: participaciones / acciones] darán derecho a participar en las ganancias sociales desde [FECHA].

• 2.º La asignación concreta a los socios de la sociedad absorbida se realiza de la siguiente forma:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

A D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] de la sociedad absorbida «[DENOMINACIÓN SOCIAL]», con un valor nominal de [IMPORTE] euros, se le atribuyen [Nº DE PARTICIPACIONES O ACCIONES] de la sociedad absorbente «[DENOMINACIÓN SOCIAL]», con un valor nominal total de [IMPORTE] euros.

[OPCIONAL — incluir si procede]

(Si existen participaciones o acciones propias y recíprocas)

• 3.º Las [ELEGIR: participaciones / acciones] las participaciones propias y recíprocas de las dos sociedades que se fusionan y que estén en poder de cualquiera de ellas quedan extinguidas. Estas [ELEGIR: participaciones / acciones] ascienden a un total de [IMPORTE] euros y son las siguientes: [RELACIÓN DE PARTICIPACIONES PROPIAS].

Tercera.- Modificación de estatutos de la sociedad absorbente

La sociedad absorbente «[DENOMINACIÓN SOCIAL]» aumenta su capital social en la cantidad de [IMPORTE] euros, mediante la creación de [Nº DE PARTICIPACIONES O ACCIONES] con una valor nominal de [IMPORTE] euros cada una, números [Nº] a [Nº], ambos inclusive.

Por esta causa, se modifica el artículo [Nº DE ARTÍCULO] de los estatutos sociales, relativo al capital social, que queda redactado del siguiente modo:

Además, la sociedad absorbente «[DENOMINACIÓN SOCIAL]» modifica los siguientes artículos de sus estatutos sociales:

Cuarta.- Modificación del órgano de administración de la sociedad absorbente

La sociedad absorbente modifica la estructura del órgano de administración, que de [TIPO DE ÓRGANO DE ADMINISTRACIÓN] pasa a ser [TIPO DE ÓRGANO DE ADMINISTRACIÓN].

Cesan como administradores de la sociedad absorbente:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], con DNI/NIF [NIF], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[ELEGIR UNA OPCIÓN: Administradores solidarios o mancomunados / Consejo de administración]

Quinta.- Régimen fiscal

Según el proyecto de fusión, la causa económica de la operación es [CAUSA], lo que se considera válido para que pueda acogerse al régimen especial establecido en el Capítulo VII del Título VII de la Ley 27/2014, de 27 de noviembre, por la que se aprueba la Ley del Impuesto sobre Sociedades.

[OPCIONAL — incluir si procede]

Sexta.- Presentación telemática

Los compareciente me requieren de forma expresa la presentación telemática de la presente escritura, (art.196 y 249.2 del Reglamento Notarial).

Los datos personales de la/s persona/s compareciente/s quedan incorporados a los ficheros automatizados existentes en la Notaría a mi cargo, y se conservarán en la misma con carácter confidencial, sin perjuicio de las remisiones de obligado cumplimiento impuestas por la legislación vigente (Ley Orgánica 3/2018, de Protección de Datos y Garantía de Derechos Digitales).

OTORGAMIENTO Y AUTORIZACIÓN

Así lo otorgan los comparecientes cuyo consentimiento, libremente prestado, se adecua a la legalidad y a su voluntad debidamente informada Hago a los comparecientes las reservas y advertencias legales, especialmente las derivadas de la legislación fiscal, y del Registro Mercantil y de su publicidad.

Leo esta escritura a los comparecientes advirtiéndoles del derecho que tienen a hacerlo personalmente, derecho al que renuncian. Enterados de su contenido, los comparecientes hacen constar libremente su consentimiento al contenido de la escritura y la firman.

Yo, el Notario, compruebo que este otorgamiento se ajusta a la legalidad y a la voluntad de las partes expresada ante mí, y de todo lo consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales de serie [SERIE], números [Nº], DOY FE.

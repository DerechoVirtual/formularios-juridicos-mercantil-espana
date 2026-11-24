---
name: escritura-publica-fusion-mediante-constitucion-nueva-mer-0333
description: "Escritura pública de fusión mediante constitución de una nueva sociedad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de fusión mediante constitución de una nueva sociedad

> Formulario **MER-0333** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Las sociedades que se fusionan elevarán el acuerdo de fusión adoptado a escritura pública, a la cual se incorporará el balance de fusión de aquéllas o, en el caso de fusión de sociedades cotizadas, el informe financiero semestral por el que el balance se hubiera sustituido. Si la fusión se realizara mediante la creación de una nueva sociedad, la escritura deberá contener, además, las menciones legalmente exigidas para la constitución de la misma en atención al tipo elegido.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de fusión mediante constitución de una nueva sociedad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de fusión mediante constitución de una nueva sociedad” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:escritura-publica-fusion-mediante-constitucion-nueva-mer-0333`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (18 veces)
- [ ] IMPORTE (9 veces)
- [ ] Nº (8 veces)
- [ ] FECHA (6 veces)
- [ ] NOMBRE O DENOMINACIÓN (6 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] DOMICILIO (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] OTROS DATOS (3 veces)
- [ ] CAPITAL SOCIAL (2 veces)
- [ ] FOLIO Y HOJA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº DE TÍTULOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] OBJETO SOCIAL (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] TOMO (2 veces)
- [ ] ÓRGANO O PERSONA (2 veces)
- [ ] CAUSA
- [ ] CNAE
- [ ] FORMA Y FECHA DE PAGO
- [ ] LUGAR
- [ ] MEDIO DE PUBLICACIÓN
- [ ] MOTIVO
- [ ] SERIE
- [ ] VOTOS A FAVOR

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

Las sociedades que se fusionan elevarán el acuerdo de fusión adoptado a escritura pública, a la cual se incorporará el balance de fusión de aquéllas o, en el caso de fusión de sociedades cotizadas, el informe financiero semestral por el que el balance se hubiera sustituido. Si la fusión se realizara mediante la creación de una nueva sociedad, la escritura deberá contener, además, las menciones legalmente exigidas para la constitución de la misma en atención al tipo elegido.


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

ESCRITURA DE FUSIÓN DEy

En [LUGAR], a [FECHA].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario de [LOCALIDAD], del Ilustre Colegio Notarial de [LOCALIDAD],

COMPARECEN

DE UNA PARTE

[OPCIONAL — incluir si procede]

(En caso de estado civil no casado)
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domiciliado en [DOMICILIO], y [ELEGIR: DNI / pasaporte] número [NÚMERO],

[OPCIONAL — incluir si procede]

(En caso de estado civil casado)
[ELEGIR UNA OPCIÓN: Con régimen económico matrimonial de gananciales / Cuando el régimen económico matrimonial no fuera el de gananciales]

Actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A]

Compañía mercantil de nacionalidad española denominada [DENOMINACIÓN SOCIAL], [ELEGIR: SL / SA], domiciliada en [DOMICILIO], con NIF núm. Inscrita en el Registro Mercantil de [LOCALIDAD], en [TOMO] el [FOLIO Y HOJA]. Su capital social es de [CAPITAL SOCIAL], dividido en [ELEGIR: participaciones / acciones / cuotas] de [IMPORTE] EURO de valor nominal cada una de ellas, numeradas correlativamente del 1 al [Nº] ambos inclusive, estando totalmente suscritas e íntegramente desembolsadas.

Dicha Sociedad tiene por objeto social [OBJETO SOCIAL]

Hace uso de las facultades conferidas a su favor

[ELEGIR UNA OPCIÓN: Cargo / Nombrado por el Consejo]

El representante de la citada Sociedad manifiesta expresamente que no han variado las circunstancias sociales antes indicadas -de denominación, forma, objeto y domicilio- respecto a los que aparecen en esta escritura; y que de conformidad con el art.20 de la Ley 14/2013, de 27 de septiembre hace constar la Clasificación Nacional de Actividades Económicas (CNAE) que le corresponde

DE OTRA

[OPCIONAL — incluir si procede]

(En caso de estado civil no casado)

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domiciliado en [DOMICILIO], y [ELEGIR: DNI / pasaporte] número [NÚMERO],

[OPCIONAL — incluir si procede]

(Casado)
[ELEGIR UNA OPCIÓN: Con régimen económico matrimonial de gananciales / Cuando el régimen económico matrimonial no fuera el de gananciales]

Actúa en nombre y representación de [NOMBRE DEL REPRESENTADO/A]

Compañía mercantil de nacionalidad española denominada [DENOMINACIÓN SOCIAL], [ELEGIR: SL / SA], domiciliada en [DOMICILIO], con NIF núm. Inscrita en el Registro Mercantil de [LOCALIDAD], en [TOMO] el [FOLIO Y HOJA]. Su capital social es de [CAPITAL SOCIAL], dividido en [Nº], de [IMPORTE] EURO de valor nominal cada una de ellas, numeradas correlativamente del 1 al [Nº] ambos inclusive, estando totalmente suscritas e íntegramente desembolsadas.

Dicha Sociedad tiene por objeto social [OBJETO SOCIAL]

Hace uso de las facultades conferidas a su favor

[ELEGIR UNA OPCIÓN: Cargo / Nombramiento]

El representante de la citada Sociedad manifiesta expresamente que no han variado las circunstancias sociales antes indicadas de denominación, forma, objeto y domicilio respecto a los que aparecen en esta escritura; y que de conformidad con el art.20 de la Ley 14/2013, de 27 de septiembre hace constar la Clasificación Nacional de Actividades Económicas (CNAE) que le corresponde [CNAE].

Me aseguro de la identidad de todos los comparecientes y considero que tienen capacidad y legitimación suficientes para otorgar esta escritura y, al efecto,

EXPONEN

I.- OBJETO

Que la presente escritura tiene por objeto la formalización de la fusión operada entre la Sociedad [DENOMINACIÓN SOCIAL] y la sociedad [DENOMINACIÓN SOCIAL] mediante la creación de la entidad [DENOMINACIÓN SOCIAL].

II.- DATOS DEL PROYECTO DE FUSIÓN

[ELEGIR UNA OPCIÓN: Sin página web / Con página web]

III.- INFORME DE LOS ADMINISTRADORES

Que los órganos de administración de cada una de las sociedades elaboraron sus respectivos informes sobre el proyecto de fusión con fecha [FECHA], con el contenido legalmente exigido.

IV.- INFORME DE EXPERTOS INDEPENDIENTES

[ELEGIR: En caso de sociedad anónima o comanditaria por acciones]

No se ha elaborado informe de expertos independientes sobre el proyecto de fusión, al no ser legalmente obligatorio por [MOTIVO]

V.- BALANCE DE FUSIÓN

[ELEGIR UNA OPCIÓN: Cualquier balance cerrado con no más de 6 meses de antelación / Último Balance anual]

Manifiestan los comparecientes que no se han producido modificaciones importantes en el Activo y Pasivo de las respectivas sociedades desde la fecha del Proyecto hasta la fecha de la aprobación de la fusión.

Un Ejemplar de dichos balances firmados por sus administradores se unen a esta matriz, siendo dichas firmas por mi legitimadas

VI.- JUNTA GENERAL

a) Convocatoria de las juntas.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Convocatoria)

Que la sociedad «[DENOMINACIÓN SOCIAL]» publicó anuncio de convocatoria en [MEDIO DE PUBLICACIÓN] el día [FECHA]. El contenido y redacción de dicha convocatoria fue el siguiente:

b) Acuerdos de las juntas.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Junta de la sociedad «[DENOMINACIÓN SOCIAL]».

Que en la junta general que se celebró el día [FECHA] con el voto favorable de [VOTOS A FAVOR] fueron adoptados los siguientes acuerdos: la fusión de las entidades [DENOMINACIÓN SOCIAL] y [DENOMINACIÓN SOCIAL] el sentido que consta en las certificaciones firmadas por los comparecientes, lo que legítimo, que se protocolizan, dándose por reproducidas.

c) Publicación de los acuerdos.

[ELEGIR UNA OPCIÓN: En BORME / Comunicación Individual]

[OPCIONAL — incluir si procede]

VII.- OPOSICIÓN DE LOS ACREEDORES

[ELEGIR UNA OPCIÓN: Sin oposición / Con oposición]

Los comparecientes me entregan los siguientes documentos, que extendidos en [Nº] folios dan fe de todo lo expuesto, dejándolos incorporados a esta matriz como parte integrante de la misma:

1.º Proyecto de fusión, con las firmas legitimadas de todos los administradores.
2.º Informes de los administradores sobre el proyecto de fusión.
3.º Informe de experto independiente sobre el proyecto de fusión.
4.º Copia de los anuncios de convocatoria y del acuerdo de fusión, cuya correspondencia con el original compruebo por exhibición de sendos ejemplares de las publicaciones citadas.
5.º Balances de fusión e informes de auditoría.
6.º Estatutos sociales de la nueva sociedad resultante de la fusión.
7.º Certificación del Registro Mercantil Central de que no se encuentra registrada la denominación de la nueva sociedad resultante de la fusión.
8.º Certificación social de la sociedad «[DENOMINACIÓN SOCIAL]», expedida por [ÓRGANO O PERSONA], con firma legitimada.
9.º Certificación social de la sociedad «[DENOMINACIÓN SOCIAL]», expedida por [ÓRGANO O PERSONA], con firma legitimada.

ESTIPULACIONES

Primera.- Fusión

La sociedad «[DENOMINACIÓN SOCIAL]» y la sociedad «[DENOMINACIÓN SOCIAL]» se fusionan para constituir la nueva sociedad «[DENOMINACIÓN SOCIAL]», que se regirá por los estatutos incorporados a esta escritura.

La fusión implica la extinción de cada una de las sociedades que intervienen en el proceso y la transmisión en bloque de los respectivos patrimonios sociales a la nueva entidad, que adquiere por sucesión universal los derechos y obligaciones de aquéllas.

Según el proyecto de fusión aprobado, a partir de [FECHA] las operaciones de las sociedades que se fusionan se consideran realizadas a efectos contables por cuenta de la nueva sociedad.

Me entregan certificación del Registro Mercantil Central, original y vigente, por la que acreditan que no figura registrada la denominación elegida. Protocolizo la certificación que me es entregada en esta matriz.

Segunda.- Régimen Jurídico

La entidad creada se regirá por la ley de Sociedades de Capital y por los Estatutos que extendidos en de folios". firmados por los comparecientes, se incorporan a la presente escritura.

Tercera.- Capital social y Asignación de Participaciones o acciones

Asignación

1.ºLasde la nueva sociedad se atribuyen a los socios de las sociedades, según se prevé en el proyecto de fusión, en la proporción dede «[NOMBRE O DENOMINACIÓN]» por cadade «[NOMBRE O DENOMINACIÓN]» [OTROS DATOS], y dede «[NOMBRE O DENOMINACIÓN]» por cadade «[NOMBRE O DENOMINACIÓN]» [OTROS DATOS].

Igualmente, los socios de «[NOMBRE O DENOMINACIÓN]» reciben una compensación dineraria de [IMPORTE] euros por cada [ELEGIR: participación / acción] asignada, mientras que la compensación dineraria de los socios de «[NOMBRE O DENOMINACIÓN]» es de [IMPORTE] euros por cada [ELEGIR: participación / acción] asignada. La compensación será pagada [FORMA Y FECHA DE PAGO].

Las nuevas [ELEGIR: participaciones / acciones] darán derecho a participar en las ganancias sociales a partir de [FECHA].

• 2.º La asignación concreta a los socios se realiza de la siguiente forma:

A D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] de la sociedad «[DENOMINACIÓN SOCIAL]», con un valor nominal de [IMPORTE] euros, se le asignan [Nº DE TÍTULOS] de la sociedad «[DENOMINACIÓN SOCIAL]» [OTROS DATOS], con un valor nominal total de [IMPORTE] euros.

D./Dña. [NOMBRE Y APELLIDOS], titular de [Nº] de la sociedad «[DENOMINACIÓN SOCIAL]», con un valor nominal de [IMPORTE] euros, se le asignan [Nº DE TÍTULOS] de la sociedad «[DENOMINACIÓN SOCIAL]», con un valor nominal total de [IMPORTE] euros.

• 3.º Las [ELEGIR: participaciones / acciones] de las dos sociedades que se fusionan y que están en poder de cualquiera de ellas quedan extinguidas. Estas [ELEGIR: participaciones / acciones] ascienden a un total de [IMPORTE] euros y son las siguientes:

Cuarto.- Nombramiento de cargos sociales

[ELEGIR UNA OPCIÓN: Administradores / Consejo]

Quinto.- Régimen fiscal

Según el proyecto de fusión, la causa económica de la operación es [CAUSA], por lo que se considera válido para que pueda acogerse al régimen especial establecido en el Capítulo VII del Título VII Ley 27/2014, de 27 de noviembre, por la que se aprueba la Ley del Impuesto sobre Sociedades.

Sexto.- Bienes de la entidad absorbida

[OPCIONAL — incluir si procede]

Séptimo.- Presentación telemática

Los compareciente me requieren de forma expresa la presentación telemática de la presente escritura, (art.196 y 249.2 del Reglamento Notarial).

Los datos personales de la/s persona/s compareciente/s quedan incorporados a los ficheros automatizados existentes en la Notaría a mi cargo, y se conservarán en la misma con carácter confidencial, sin perjuicio de las remisiones de obligado cumplimiento impuestas por la legislación vigente (Ley Orgánica 3/2018 de Protección de Datos Personales y garantía de derechos digitales).

OTORGAMIENTO Y AUTORIZACIÓN

Así lo otorgan los comparecientes cuyo consentimiento, libremente prestado, se adecua a la legalidad y a su voluntad debidamente informada.

Hago a los comparecientes las reservas y advertencias legales, especialmente las derivadas de la legislación fiscal, y del Registro Mercantil y de su publicidad.

Leo esta escritura a los comparecientes advirtiéndoles del derecho que tienen a hacerlo personalmente, derecho al que renuncian. Enterados de su contenido, los comparecientes hacen constar libremente su consentimiento al contenido de la escritura y la firman.

Yo, el Notario, constato que este otorgamiento se ajusta a la legalidad y a la voluntad de las partes expresada ante mí, y de todo lo consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales de serie [SERIE], números [Nº], DOY FE.

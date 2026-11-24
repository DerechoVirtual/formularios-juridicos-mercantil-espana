---
name: solicitud-legalizacion-telematica-libros-contables-sl-mer-0049
description: "Solicitud de legalización telemática de libros contables de SL o SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de legalización telemática de libros contables de SL o SA

> Formulario **MER-0049** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de legalización telemática de libros contables de SL o SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de legalización telemática de libros contables de SL o SA” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:solicitud-legalizacion-telematica-libros-contables-sl-mer-0049`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] OTROS DATOS

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

La Dirección General de los Registros y del Notariado (DGRN), en la Instrucción de 12 de febrero de 2015, proporciona criterios procedimentales únicos y uniformes para la legalización de los libros de todas clases que obligatoriamente deben llevar los empresarios, así como, un nuevo formato que recoge los archivos que conforman la legalización de los libros en un archivo comprimido, aportando una mayor simplicidad, ahorro de tamaño y disminución del tiempo de proceso en la tramitación telemática.

En el soporte electrónico de que se trate deberán constar obligatoriamente los ficheros que a continuación se detallan.

A) Libros legalizados:

Libros legalizados que se corresponderán con la siguiente tabla:

Nombre del libro
Diario
Inventario y Cuentas Anuales
Balances de comprobación (sumas y saldos)
Inventario
Balances
Memoria
Mayor
Libro de Pérdidas y Ganancias
IVA
Facturas Emitidas
Facturas Recibidas
Detalle del Diario
Registro de Acciones Nominativas
Registro de Socios
Libro de Actas
Libro de Detalle de Actas
Libro de Actas del Consejo
Libro de Detalle de Actas del Consejo
Libro-Registro de Contratos del Socio Único con la Sociedad Unipersonal
Otros

B) Archivo NOMBRES.TXT:

Fichero ASCII que contiene los nombres de los ficheros correspondientes a cada uno de los libros cuya legalización se pretenda. Los nombres de dichos ficheros y sus extensiones deberán ajustarse a los requisitos que se detallan a continuación. Cada línea de texto, separada con Intro, indicará el nombre de cada uno de los libros legalizados.

Solamente se permitirá la presentación de un máximo de nueve libros correlativos por cada tipo (por ejemplo, del libro de DIARIO podrá presentar hasta nueve libros). El nombre de dichos ficheros deberá ser el correspondiente al tipo de libro, DIARIO en este caso, concatenado con _NNN (NNN el n.º correspondiente a cada uno de los libros presentados de dicho tipo). En caso de presentarse tipos de libros que no correspondan a ningún nombre de la tabla anterior, sus ficheros correspondientes se nombrarán todos como OTROS_ al que se le concatenará un número correlativo X (del 1 al 9) que los distinga.

Los nombres de los ficheros se ajustarán a la siguiente tabla:

Nombre del libro	Nombre del fichero en el archivo NOMBRE.TXT
Diario	DIARIO_NNN.<extension>
Inventario y cuentas anuales	INV_CUEN_NNN.<extension>
Balances de comprobación (sumas y saldos)	BAL_SUMS_NNN.<extension>
Inventario	INVENTAR_NNN.<extension>
Balances	BALANCES_NNN.<extension>
Memoria	MEMORIA_NNN.<extension>
Mayor	MAYOR_NNN.<extension>
Libro de Pérdidas y Ganancias	PER_GAN_NNN.<extension>
IVA	IVA_NNN.<extension>
Facturas Emitidas	FAC_EMIT_NNN.<extension>
Facturas Recibidas	FAC_RECI_NNN.<extension>
Detalle del Diario	DET_DIA_NNN.<extension>
Registro de Acciones Nominativas	ACCIONES_NNN.<extension>
Registro de Socios	SOCIOS_NNN.<extension>
Libro de Actas	ACTASCON_NNN.<extension>
Libro de Detalle de Actas	ACTASDET_NNN.<extension>
Libro de Actas del Consejo	ACTALCON_NNN.<extension>
Libro de Detalle de Actas del Consejo	ACTACODE_NNN.<extension>
Libro-registro de Contratos del Socio Único con la Sociedad Unipersonal	SOCUNICO_NNN.<extension>
Otros	OTROS_NNN.<extensión>

Las extensiones de los ficheros se ajustarán a la siguiente tabla:

Formato	Extensiones válidas
Excel	XLS o XLSX
QuatroPro	WQ1
Lotus	WK1
Word	DOC o DOCX
Rich Text Format	RTF
Acrobat Reader	PDF
Open Office	ODS y ODT

C) Archivo DATOS.TXT:

Fichero de datos [OTROS DATOS] correspondientes a la solicitud y a la certificación, ajustándose a la estructura siguiente:

Código de campo	Formato	Longitud	Contenido del campo
101	Alfanumérico	8	Fecha de la solicitud (ddmmaaaa)
102	Alfanumérico	100	Nombre o Denominación Social del empresario
103	Alfanumérico	32	Primer apellido
104	Alfanumérico	32	Segundo apellido
105	Alfanumérico	9	NIF
106	Alfanumérico	32	Domicilio
107	Alfanumérico	32	Ciudad
108	Numérico	5	Código Postal
109	Numérico	2	Código de la Provincia
110	Alfanumérico	10	Fax
111	Alfanumérico	10	Teléfono
112	Numérico	5	Código de Registro
201	Alfanumérico	6	Tomo (Datos Registrales)
202	Alfanumérico	6	Libro (Datos Registrales)
203	Alfanumérico	6	Sección (Datos Registrales)
204	Alfanumérico	6	Folio (Datos Registrales)
205	Alfanumérico	32	Tipo de Registro Público
206	Alfanumérico	6	Hoja (Datos Registrales)
207	Alfanumérico	32	Otros (Datos Regístrales)
301	Alfanumérico	100	Nombre o Denominación Social del presentante
302	Alfanumérico	32	Primer apellido presentante
303	Alfanumérico	32	Segundo apellido presentante
304	Alfanumérico	9	DNI presentante
305	Alfanumérico	32	Domicilio presentante
306	Alfanumérico	32	Ciudad presentante
307	Alfanumérico	5	Código postal presentante
308	Alfanumérico	32	Provincia del presentante
309	Alfanumérico	10	Fax presentante
310	Alfanumérico	10	Teléfono presentante
311	Alfanumérico	60	Correo electrónico presentante
401	Alfanumérico	2	Solicita retención (SI/NO)
501	Numérico	3	Número total de libros presentados

Y para cada uno de los libros, en conjunto de seis registros:

Código de campo	Formato	Longitud	Contenido del campo
xxx01	Alfanumérico	100	Descripción del libro
xxx02	Numérico	3	Número del libro
xxx03	Alfanumérico	8	Fecha de apertura del libro (ddmmaaaa)
xxx04	Alfanumérico	8	Fecha de cierre del libro (ddmmaaaa)
xxx05	Alfanumérico	8	Fecha último cierre (ddmmaaaa)
xxx06	Alfanumérico	64	Huella digital del libro

Donde xxx cambiará para cada libro, y por lo tanto para cada grupo de esos cuatro registros, yendo desde el 001 para el primer grupo (el primer libro), hasta el 180 en caso de presentarse el máximo número posible de libros para cada uno de los 20 tipos posibles de dichos libros. El valor xxx ha de coincidir con el orden de líneas del fichero NOMBRES.TXT

D) Rutina cálculo huella digital:

Para generar la huella digital correspondiente a cada libro, se aplicará al fichero de dicho libro el algoritmo estándar SHA256 (RFC 6234) el cual producirá un hash de 256 bits (32 bytes), dicho conjunto de bits a su vez se codificará para su conversión en texto según el estándar base64 (RFC 4648).

Formato ZIP:

Todos los ficheros que componen la legalización se encontrarán comprimidos en un archivo con extensión.ZIP. La tecnología de compresión para conseguir el fichero.ZIP será la de la versión 2.0 o anteriores. Todos los ficheros incluidos en el.ZIP penderán directamente de la raíz (sin estructurarlos en directorios). El algoritmo de compresión será el Deflate estándar (no el Deflate 64) y no se usarán cifrados ni signaturas.

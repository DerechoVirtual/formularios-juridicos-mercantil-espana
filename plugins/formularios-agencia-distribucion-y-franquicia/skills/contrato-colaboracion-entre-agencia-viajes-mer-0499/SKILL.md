---
name: contrato-colaboracion-entre-agencia-viajes-mer-0499
description: "Contrato de colaboración entre agencia de viajes y establecimiento hotelero. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de colaboración entre agencia de viajes y establecimiento hotelero

> Formulario **MER-0499** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de colaboración entre agencia de viajes y establecimiento hotelero» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de colaboración entre agencia de viajes y establecimiento hotelero” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-colaboracion-entre-agencia-viajes-mer-0499`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] MES (3 veces)
- [ ] Nº (3 veces)
- [ ] AÑO (2 veces)
- [ ] CARGO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] NOMBRE DEL HOTEL (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] C.P.
- [ ] CADENA HOTELERA
- [ ] CATEGORÍA OFICIAL
- [ ] FECHA
- [ ] LUGAR
- [ ] NIF
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] OTROS SERVICIOS
- [ ] PAÍS
- [ ] TIPO DE CONTRATO
- [ ] ZONA
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

CONTRATO DE COLABORACIÓN DE LA AGENCIA [DENOMINACIÓN SOCIAL] CON El Hotel [NOMBRE DEL HOTEL] Zona [ZONA] domicilio [DOMICILIO] categoría oficial de [CATEGORÍA OFICIAL] tel., tx., CP [C.P.] País [PAÍS] Cadena [CADENA HOTELERA] En la ciudad de

REUNIDOS

De una parte, D. [NOMBRE Y APELLIDOS], mayor de edad, provisto de DNI núm. actuando en nombre y representación de la Agencia [DENOMINACIÓN SOCIAL], domiciliada en [DOMICILIO], en su calidad de [CARGO] de la misma y a los solos efectos de representación.

Y de otra parte, D. [NOMBRE Y APELLIDOS]. también mayor de edad, con DNI núm. [Nº], actuando en su calidad de [CARGO] en nombre y representación de [NOMBRE DEL REPRESENTADO/A], titular del Hotel [NOMBRE DEL HOTEL] sito en [LOCALIDAD] provisto de NI [NIF] otorgan el presente contrato de colaboración que se regirá con arreglo a las siguientes

CLÁUSULAS

Este contrato entrará en vigor el día [FECHA] de [MES] de 20 y hasta el día [DÍA] de [MES] de [AÑO], fecha ésta en la que se extinguirá sin necesidad de preaviso alguno.

Durante la vigencia del contrato, el Hotel se obliga a tener a disposición de la agencia, de los clientes de ésta o de un tercero, que la misma designe, [Nº] de camas en base a las características, tipo de habitaciones, servicios y condiciones que a continuación se detallan:

El cupo estará a disposición de la agencia hasta [Nº] días antes de la llegada.

Los precios arriban mencionados se entienden netos, en [IMPORTE] euros, por plaza y día, con los impuestos incluidos a los tipos vigentes durante la duración del contrato.

Por un servicio de almuerzo o cena no prestado a los clientes el día de salida o de entrada, el Hotel descontará la cantidad de [IMPORTE] por persona.

El Hotel proporcionará a los guías de la Agencia, con carácter gratuito, una zona de recepción para comunicarse con los clientes de su Agencia y [OTROS SERVICIOS]

Las plazas reservadas a favor de la Agencia en el presente contrato lo son carácter exclusivo para los períodos que se determinen en el mismo.

Si por alguna circunstancia ajena a la Agencia, el Hotel incumpliera la obligación de tener dispuestas las habitaciones contratadas y/o confirmadas en las condiciones y precios pactados, éste se obliga a facilitar alojamiento en Hoteles de igual o superior categoría y características, siendo las diferencias de precio, los gastos de traslado de los clientes y demás cargos ocasionados por el cambio de cuenta del Hotel a quien la Agencia se limitará a pagar los gastos estipulados en este contrato.

De igual forma el Hotel se hará responsable de las implicaciones legales (multas, sanciones, indemnizaciones, etc.,) que, con carácter oficial, o privado, puedan derivarse de esta circunstancia, debiendo expedir a solicitud de la Agencia un certificada acreditativo de la existencia de la reserva y la causa de su incumplimiento.

Las habitaciones no ocupadas serán devueltas al Hotel sin pago de indemnización alguna con la antelación fijada en los releases anteriormente especificados, sin tener la Agencia compromiso alguno sobre las mismas.

Las habitaciones reservadas extra cupo serán a los mismos precios que figuran en este contrato.

El importe de las facturas objeto de este contrato serán remitidas a la Agencia, acompañadas del correspondiente bono; una vez finalizada la estancia de que se trate; serán pagadas con la fórmula que a continuación se indica:

Cualquiera que sea la fórmula elegida será necesaria la conformidad de la Agencia con la facturación presentada para proceder al pago.

Si se hubiera constituido un depósito previo, sólo podrán debitarse las facturas que se vayan produciendo con cargo al mismo cuando lo consienta expresamente la Agencia a solicitud del Hotel y previa conformidad con la facturación presentada.

El Hotel garantiza la calidad de los servicios a prestar, de acuerdo con su categoría oficial, y se hace responsable de todas las reclamaciones que puedan presentarse como consecuencia de las deficiencias probadas en sus servicios, así como de los reembol- sos, sanciones y demás pagos que tenga que hacer la Agencia como consecuencia de reclamaciones de clientes o de sanciones del Ministerio y/o Comunidades Autónomas com- petentes al respecto, al igual que las reclamaciones e indemnizaciones que por las expresa- das causas puedan producirse ante la Jurisdicción Ordinaria Civil u otra especial.

A todos los efectos legales, se hace constar que el establecimiento es propiedad de [NOMBRE DE LA PARTE] y que la explotación del mismo pertenece a [NOMBRE DE LA PARTE] en virtud de contrato de [TIPO DE CONTRATO] por una duración de

La propiedad, representada por [ÓRGANO O PERSONA] expresa su consentimiento para la celebración del presente contrato y garantiza su continuidad para el caso de que quedase subrogada en la explotación, comprometiéndolo así bajo su firma.

Si el establecimiento fuese vendido, arrendado o cedido en cualquier forma a un tercero, los cedentes se comprometen a que el mismo contrato sea respetado y cumplido por los adquirentes, quienes asimismo reconocerán los anticipos o depósitos que acaso existan a favor de la agencia.

Las partes contratantes, con renuncia a su propio fuero y derecho, se someten expresa y voluntariamente a la jurisdicción y competencia de los Tribunales de [LOCALIDAD] y a la aplicación del derecho común de dicho lugar.

CLÁUSULAS ANEXAS:

El Hotel se obliga a que ninguno de sus empleados haga venta de excursiones a clientes de la Agencia, haciéndose responsable del importe de la venta que efectúen contraviniendo este acuerdo.

El Hotel se obliga a no contratar con Tour-Operadores y Agencias de viajes nacionales a precios inferiores a los del presente contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad y aceptación de todas las cláusulas, ambas partes firman en [LUGAR], a [DÍA] de [MES] de [AÑO].

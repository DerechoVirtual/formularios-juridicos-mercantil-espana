---
name: contrato-edicion-obra-colectiva-mer-0741
description: "Contrato de edición de una obra colectiva. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de edición de una obra colectiva

> Formulario **MER-0741** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de edición de una obra colectiva» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de edición de una obra colectiva” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-edicion-obra-colectiva-mer-0741`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (17 veces)
- [ ] Nº (13 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] DÍA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] FECHAS (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PLAZO (2 veces)
- [ ] SUCURSAL (2 veces)
- [ ] AÑO
- [ ] IDIOMA
- [ ] LUGAR
- [ ] MES
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE EJEMPLARES
- [ ] TÍTULO DE LA OBRA

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA EDITORIAL", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS], en nombre y representación de D. [NOMBRE Y APELLIDOS], D. [NOMBRE Y APELLIDOS], D. [NOMBRE Y APELLIDOS], en lo sucesivo "LOS AUTORES", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE EDICIÓN DE OBRA COLECTIVA, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que LA EDITORIAL es una mercantil que tiene por objeto social la creación, desarrollo, mantenimiento y comercialización de programas y equipos informáticos.

SEGUNDO.- Que LOS AUTORES han realizado (descripción de la obra), en lo sucesivo, "La Obra" con título [TÍTULO DE LA OBRA]. Que cada uno de ellos ha intervenido en condición de:

-D. [NOMBRE Y APELLIDOS], en calidad de coordinador.

-D. [NOMBRE Y APELLIDOS], en calidad de autor.

-D. [NOMBRE Y APELLIDOS], en calidad de autor.

TERCERO.- Que ambas partes están interesadas en que LA EDITORIAL reproduzca, publique y distribuya la Obra de LOS AUTORES, por lo que ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

[ELEGIR UNA OPCIÓN: Objeto / Cesión en exclusiva / No en exclusiva]

Contraprestación

Onerosa

Las partes acuerdan una contraprestación por la cesión de derechos objeto del presente contrato del % sobre el precio de venta público (con IVA/sin IVA) por ejemplar vendido de la Obra.

El pago se efectuará entre los días [FECHAS] y [DÍA] de (mes) en la cuenta corriente núm. [Nº] que LOS AUTORES tienen suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL], correspondiéndoles a cada uno un porcentaje en función de su intervención. Así, D [NOMBRE Y APELLIDOS], en su calidad de coordinador, percibirá el % de la contraprestación total; D [NOMBRE Y APELLIDOS], en su condición de autor, el %; D [NOMBRE Y APELLIDOS], en su misma condición de autor, el %;

El retraso en más de [Nº] días en el pago de los derechos dará derecho a LOS AUTORES a exigir a LA EDITORIAL un interés moratorio del %.

Gratuita

LOS AUTORES renuncian a los derechos de autor sobre la Obra

Donación de derechos

LOS AUTORES donan la remuneración de los derechos de autor a favor de (persona física o jurídica o entidad que patrocina la publicación) y LA EDITORIAL abonará a ésta, mediante liquidaciones mensuales/trimestrales/semestrales/anuales el % sobre el precio de venta al público (con IVA/sin IVA) de los ejemplares efectivamente vendidos.

El pago se efectuará entre los días [FECHAS] y [DÍA] de cada mes en la cuenta corriente núm. [Nº] que (persona física o jurídica o entidad que patrocina la publicación) tiene suscrita con la entidad [DENOMINACIÓN SOCIAL] en su sucursal [SUCURSAL].

El retraso en más de [Nº] días en cualquiera de los pagos dará derecho a LA EDITORIAL a exigir al AUTOR un interés moratorio del % respecto de cada uno de los pagos no satisfechos puntualmente.

Obligaciones de los autores

LOS AUTORES se comprometen a:

a) Entregar a LA EDITORIAL un duplicado fiel y completo del original de la Obra. Si éste resultara destruido o extraviado involuntariamente antes de su edición

b) Corregir las pruebas de imprenta previas a la publicación de las OBRA que le sean proporcionadas por la EDITORIAL en un plazo máximo de [Nº] días desde sus respectivas entregas.

c) Revisar las incidencias que en los índices, notas a pie de página, etc. puedan ocasionar las nuevas paginaciones de las sucesivas pruebas de imprenta.

c) No contraer obligación alguna que grave de cualquier modo la cesión de derechos objeto del presente contrato

Obligaciones del original

LA EDITORIAL se compromete a:

a) Publicar la Obra en un plazo de [Nº] meses/años;

b) Sufragar cuantos gastos sean precisos para la publicación, promoción y distribución de la Obra;

c) No introducir en la Obra ninguna clase de alteración, modificación, adición o supresión sin autorización expresa del AUTOR

Condiciones de la edición

Apariencia física

El nombre de LOS AUTORES figurará en la cubierta y en la portada de cada uno de los ejemplares de la Obra.

Título definitivo

El título definitivo será el que decida la EDITORIAL a propuesta de LOS AUTORES.

Tirada

La tirada de la primera edición constará con un mínimo de [Nº] ejemplares y un máximo de [Nº] ejemplares.

Determinación del precio de venta

La determinación del precio de venta, así como la presentación material y la promoción, difusión y explotación comercial de la Obra serán de exclusiva competencia de LA EDITORIAL.

Lengua

La Obra se publicará en lengua [IDIOMA]

Ulteriores ediciones

En el momento en que los ejemplares de la Obra en stock sean inferiores a [Nº DE EJEMPLARES],la EDITORIAL comunicará dicha circunstancia al AUTOR en el plazo de [PLAZO] y mediante comunicación escrita que deje constancia de su recepción.

Si LOS AUTORES no efectúan comunicación en contrario en un plazo de [PLAZO] desde el siguiente a la fecha de conocimiento de la situación del stock, LA EDITORIAL podrá proceder, si lo estima necesario o conveniente para sus intereses, a la publicación de ulteriores ediciones con un mínimo de [Nº] ejemplares y un máximo de

LOS AUTORES se comprometen a corregir las pruebas de imprenta previas a la publicación de la Obra que le sean proporcionadas por la EDITORIAL y actualizar su contenido en un plazo máximo de [Nº] días/semanas desde las respectivas entregas.

Ejemplares de autor

LA EDITORIAL entregará a LOS AUTORES gratuitamente [Nº] ejemplares de cada una de las ediciones o reimpresiones, y le facturará además cuantos ejemplares desee adquirir, que no podrán ser destinados al comercio, con el % de descuento.

Responsabilidad

LOS AUTORES serán los únicos responsable por las reclamaciones que puedan ser formuladas por terceros, incluida la Administración Pública, sobre el contenido y la propiedad de la Obra, así como por los daños y perjuicios que puedan irrogarse por los mismos motivos a LA EDITORIAL, a quien faculta expresamente para el ejercicio de las acciones que la Ley otorga para la defensa de sus derechos en relación con la Obra.

Duración del contrato

Este contrato quedará extinguido a los [Nº] años de la publicación de la última edición o reimpresión.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

Jurisdicción competente y ley aplicable

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, la competencia de los Tribunales que deban conocer del asunto se determinará de conformidad con los criterios de competencia objetiva, funcional y territorial legalmente aplicables.

El presente contrato tiene carácter mercantil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE EDICIÓN DE OBRA COLECTIVA, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo. Don [NOMBRE Y APELLIDOS]

(La Editorial)

Fdo. Don [NOMBRE Y APELLIDOS]

(El Autor)

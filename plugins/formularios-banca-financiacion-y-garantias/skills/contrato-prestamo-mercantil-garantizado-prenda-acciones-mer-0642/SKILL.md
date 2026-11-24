---
name: contrato-prestamo-mercantil-garantizado-prenda-acciones-mer-0642
description: "Contrato de préstamo mercantil garantizado con prenda de acciones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de préstamo mercantil garantizado con prenda de acciones

> Formulario **MER-0642** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Contrato de préstamo mercantil entre dos sociedades, con interés anual, amortización en un plazo, vencimiento anticipado por impago o concurso, y garantía mediante prenda sobre acciones (u otros valores) representadas por anotaciones en cuenta.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de préstamo mercantil garantizado con prenda de acciones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de préstamo mercantil garantizado con prenda de acciones” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-prestamo-mercantil-garantizado-prenda-acciones-mer-0642`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] Nº (5 veces)
- [ ] DOMICILIO (4 veces)
- [ ] NOMBRE DEL NOTARIO (4 veces)
- [ ] AÑO (2 veces)
- [ ] DATOS REGISTRALES: LIBRO, TOMO, FOLIO (2 veces)
- [ ] DNI/NIF (2 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] MES (2 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] CIUDAD
- [ ] DENOMINACIÓN SOCIAL DEL PRESTAMISTA
- [ ] DENOMINACIÓN SOCIAL DEL PRESTATARIO
- [ ] PARTE QUE ASUME LOS IMPUESTOS Y GASTOS
- [ ] PORCENTAJE

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

- Junto a «…e o, en su caso, se disminuyese el interés básico fijado por el Banco de España.»: comprobar que sigue existiendo el tipo oficial de referencia citado o sustituirlo por un índice vigente (p. ej. Euríbor) y respetar, en su caso, la normativa sobre usura y transparencia.

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

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

COMPARECEN

De una parte, [DENOMINACIÓN SOCIAL DEL PRESTAMISTA], constituida en escritura pública otorgada el día [FECHA] ante el Notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], e inscrita en el Registro Mercantil de [PROVINCIA], [DATOS REGISTRALES: LIBRO, TOMO, FOLIO], domiciliada en [LOCALIDAD], calle [DOMICILIO], núm. [Nº], y con NIF núm. [NIF], representada por [NOMBRE Y APELLIDOS DEL REPRESENTANTE], mayor de edad, con domicilio en [DOMICILIO], con DNI/NIF núm. [DNI/NIF], cuyas facultades derivan del poder otorgado por el Notario [NOMBRE DEL NOTARIO], debidamente inscrito, que es declarado vigente y sin modificación alguna (en adelante, el PRESTAMISTA);

De otra parte, [DENOMINACIÓN SOCIAL DEL PRESTATARIO], constituida en escritura pública otorgada el día [FECHA] ante el Notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], e inscrita en el Registro Mercantil de [PROVINCIA], [DATOS REGISTRALES: LIBRO, TOMO, FOLIO], domiciliada en [LOCALIDAD], calle [DOMICILIO], núm. [Nº], y con NIF núm. [NIF], representada por [NOMBRE Y APELLIDOS DEL REPRESENTANTE], mayor de edad, con domicilio en [DOMICILIO], con DNI/NIF núm. [DNI/NIF], cuyas facultades derivan del poder otorgado por el Notario [NOMBRE DEL NOTARIO], debidamente inscrito, que es declarado vigente y sin modificación alguna (en adelante, el PRESTATARIO).

CLÁUSULAS

PRIMERA.— Importe del préstamo.

La entidad PRESTAMISTA entrega en este acto la cantidad de [IMPORTE] euros, importe del capital del préstamo que se formaliza en el presente contrato. La entidad PRESTATARIA recibe la cantidad señalada, reconociendo su deuda al PRESTAMISTA.

SEGUNDA.— Intereses.

El préstamo convenido devengará un interés del [PORCENTAJE] % anual, que se hará efectivo por anualidades vencidas. El interés pactado quedará modificado en sentido y cuantía, sin necesidad de comunicación previa, si por disposición oficial se incrementase o, en su caso, se disminuyese el interés básico fijado por el Banco de España.

TERCERA.— Pago de intereses y devolución del capital.

La PRESTATARIA queda obligada al pago de intereses y a la devolución del capital prestado del modo en que se expone a continuación:

— Desde la fecha de la firma del presente contrato hasta el día de la cancelación, deberá abonar al PRESTAMISTA el interés establecido al tipo correspondiente en la cláusula segunda y por anualidades vencidas.

— La amortización del capital del préstamo se efectuará en el plazo establecido de [Nº] años desde el día de la firma del contrato, con vencimiento el día [DÍA] de [MES] de [AÑO].

La PRESTATARIA podrá realizar reembolsos parciales, que se computarán en las liquidaciones anuales de intereses.

CUARTA.— Garantía.

La PRESTATARIA, en garantía de la cantidad que recibe y de los intereses que la citada cantidad genere durante la duración de la relación de préstamo, constituye prenda a favor del PRESTAMISTA sobre las [ELEGIR: acciones / obligaciones / otros valores: ESPECIFICAR], señalados con los números del [Nº] al [Nº], de [IMPORTE] euros nominales, representados por anotaciones en cuenta, en el registro contable correspondiente.

QUINTA.— Vencimiento.

La entidad PRESTAMISTA podrá considerar vencido el préstamo, procediendo a la notificación de la PRESTATARIA, si se produce alguno de los supuestos que a continuación se mencionan:

— Si la PRESTATARIA deja de pagar los intereses a su vencimiento.

— Si la PRESTATARIA es declarada en concurso o deja de pagar sus obligaciones dinerarias.

SEXTA.— Impuestos y gastos.

Los impuestos y gastos judiciales o extrajudiciales que se deriven de la celebración de este contrato serán de cargo de [PARTE QUE ASUME LOS IMPUESTOS Y GASTOS].

SÉPTIMA.— Tribunal competente.

Las partes renuncian a su fuero propio y se someten a los tribunales de [CIUDAD].

OCTAVA.— Norma aplicable.

Este contrato tiene carácter mercantil y se regirá por sus propias cláusulas y por las disposiciones del Código de Comercio, Código Civil y usos mercantiles, en lo que no estuviere previsto por sus disposiciones.

PROTECCIÓN DE DATOS

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento del Reglamento (UE) 2016/679 (RGPD), de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, y demás normativa aplicable.

EL PRESTAMISTA: [FIRMA]	EL PRESTATARIO: [FIRMA]

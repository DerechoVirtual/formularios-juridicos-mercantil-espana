---
name: contrato-venta-plazos-bienes-muebles-mer-0579
description: "Contrato de venta a plazos de bienes muebles. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de venta a plazos de bienes muebles

> Formulario **MER-0579** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de venta a plazos de bienes muebles» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de venta a plazos de bienes muebles” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-venta-plazos-bienes-muebles-mer-0579`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] LOCALIDAD Y FECHA (5 veces)
- [ ] Nº DE HOJAS (5 veces)
- [ ] Nº (3 veces)
- [ ] FECHA (2 veces)
- [ ] FOLIO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] AÑO
- [ ] CLÁUSULA SOBRE EL DOMINIO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FÓRMULA DE CÁLCULO
- [ ] MES
- [ ] Nº DE ASIENTO
- [ ] Nº DE BIEN
- [ ] Nº DE DIARIO
- [ ] Nº DE PLAZOS
- [ ] OTROS DATOS

## Normas que cita el formulario

- art. 10 Ley 28/1998
- art. 6.1 Ley 28/1998

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

Contrato de venta a plazos

CONTRATO DE VENTA A PLAZOS DE BIENES MUEBLES

Modelo aprobado por Resolución de la Dirección General de los Registros y del Notariado de 18/02/2000

COMPRADOR

APELLIDO 1º	APELLIDO 2º	NOMBRE	N.I.F./C.I.F.

Domicilio

Inscrita

Y en su nombre y representación

APELLIDO 1º	APELLIDO 2º	NOMBRE	N.I.F./C.I.F.

Domicilio

Inscrita

Y en su nombre y representación

FIADOR

APELLIDO 1º	APELLIDO 2º	NOMBRE	N.I.F./C.I.F.

Domicilio

Inscrita

Y en su nombre y representación

VENDEDOR N.I.F./C.I.F.

Domicilio

Inscrita

Y en su nombre y representación

OBJETO

Modelo

Cuya entrega queda hecha al comprador

Marca
Nº FABRICACIÓN O CHASIS	MATRÍCULA (en su caso)

Unidad de cuenta. Euros

PRECIO DE LA COMPRAVENTA (Valor al contado) [IMPORTE]

Desembolso inicial (si lo hubiera) [IMPORTE]

Cantidad aplazada [IMPORTE]

Interés por aplazamiento [Nº] meses al [PORCENTAJE] % [IMPORTE]

SUMA LO ADEUDADO

IMPORTE TOTAL A PLAZOS

RECONOCIMIENTO DE DEUDA.-El comprador reconoce deber al vendedor la cantidad de [IMPORTE] que se pagarán en [Nº DE PLAZOS] plazos conforma al plan de amortización que figura en hoja anexa, señalándose como domicilio de pago [DOMICILIO]. Por consiguiente, con fecha [FECHA] deberá quedar terminado el pago. T.A.E.

DERECHO DE DESISTIMIENTO.-

DOMINIO.- El objeto vendido se halla libre de gravámenes, y el dominio [CLÁUSULA SOBRE EL DOMINIO]

En prueba de conformidad, firman las partes el presente contrato en [Nº DE HOJAS] hojas numeradas correlativamente y en tantos ejemplares como partes intervienen.

COMPRADOR/ES	FIADOR/ES	VENDEDOR
En En En [LOCALIDAD Y FECHA]

CONTRATO DE VENTA A PLAZOS DE BIENES MUEBLES CONDICIONES GENERALES

1. COMPRADOR.-En caso de intervenir varios compradores, se obligan con carácter [ELEGIR: solidario / mancomunado] al cumplimiento de las obligaciones dimanantes del presente contrato.

2. FIADOR.-El/los fiador/es afianza/n.

3. PROHIBICIÓN DEL DISPONER.-El comprador no podrá realizar ningún acto de disposición o gravamen, sin autorización escrita del vendedor.

4. MORA EN EL PAGO.-A partir de cada vencimiento no satisfecho, el vendedor podrá exigir al comprador el pago de [Nº] por ciento sobre el mismo, aplicándose para su cálculo la fórmula [FÓRMULA DE CÁLCULO], sin perjuicio de que la falta de pago de dos de los plazos o el último de ellos pueda dar lugar al vencimiento de lo adeudado o a la resolución del contrato, con los efectos del artículo 10 de la Ley 28/1998.

5. PAGO ANTICIPADO.-El comprador podrá pagar anticipadamente.

6. CESIÓN DE DERECHOS.-

7. TASACIÓN..-El valor de tasación del/los objetos del presente contrato se fijará de la siguiente forma:

8. CÁLCULO DEL T.A.E..-La fórmula utilizada para el cálculo del T.A.E. es la recogida en el anexo de la Ley 16/2011, de 24 de junio de Contratos de Crédito al consumo.

9. NOTIFICACIONES.-Se señalan como domicilios a efectos de notificaciones, requerimientos y emplazamientos.

10. ENTREGA DEL EJEMPLAR DEL CONTRATO.-En cumplimiento de lo establecido en el art. 6.1 de la Ley 28/1998, cada una de las partes intervinientes deberá recibir un ejemplar del presente contrato, debidamente firmado.

11. PLURALIDAD DE OBJETOS.-En estos casos se entenderá distribuido el importe total a plazos proporcionalmente al valor [OTROS DATOS] al contrato de cada bien, salvo pacto en contrario.

OTRAS CLÁUSULAS.

En prueba de conformidad, firman las partes el presente contrato en [Nº DE HOJAS] hojas numeradas correlativamente y en tantos ejemplares como partes intervienen.

COMPRADOR/ES	FIADOR/ES	VENDEDOR
En En En [LOCALIDAD Y FECHA]

LEGITIMACIÓN DE FIRMAS (Opcional)

DILIGENCIA.-CESIÓN A TERCERO: Por haber reintegrado la parte aplazada del precio al acreedor [NOMBRE Y APELLIDOS], queda subrogado en el crédito y derechos dimanantes de este contrato, D. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD] a quien se cede el crédito indicado.

El vendedor cedente responde al financiador de la existencia y legitimidad del crédito; afianza solidariamente el cumplimiento de las obligaciones de pago asumidas por el comprador.

En

EL CEDENTE (Vendedor)	EL CESIONARIO (Financiador)

ANEXO I AL CONTRATO DE VENTA A PLAZOS DE BIENES MUEBLES

CUADRO DE AMORTIZACIÓN

VENCIMIENTO	IMPORTE PLAZO	AMORT. CAPITAL	INTERESES	CAPITAL PENDIENTE

En prueba de conformidad, firman las partes el presente contrato en [Nº DE HOJAS] hojas numeradas correlativamente y en tantos ejemplares como partes intervienen.

COMPRADOR/ES	FIADOR/ES	VENDEDOR
En En En [LOCALIDAD Y FECHA]

ANEXO II AL CONTRATO DE VENTA A PLAZOS DE BIENES MUEBLES

COMPRADOR

APELLIDO 1º	APELLIDO 2º	NOMBRE	N.I.F./C.I.F.

Domicilio

Inscrita

Y en su nombre y representación

APELLIDO 1º	APELLIDO 2º	NOMBRE	N.I.F./C.I.F.

Domicilio

Inscrita

Y en su nombre y representación

FIADOR

APELLIDO 1º	APELLIDO 2º	NOMBRE	N.I.F./C.I.F.

Domicilio

Inscrita

Y en su nombre y representación

OBJETO	Marca	Modelo
Nº FABRICACIÓN O CHASIS	MATRÍCULA (en su caso)	VALOR AL CONTADO

OBJETO	Marca	Modelo
Nº FABRICACIÓN O CHASIS	MATRÍCULA (en su caso)	VALOR AL CONTADO

OBJETO	Marca	Modelo
Nº FABRICACIÓN O CHASIS	MATRÍCULA (en su caso)	VALOR AL CONTADO

OBJETO	Marca	Modelo
Nº FABRICACIÓN O CHASIS	MATRÍCULA (en su caso)	VALOR AL CONTADO

Objetos no principales y accesorios.

En prueba de conformidad, firman las partes el presente contrato en [Nº DE HOJAS] hojas numeradas correlativamente y en tantos ejemplares como partes intervienen.

COMPRADOR/ES	FIADOR/ES	VENDEDOR
En En En [LOCALIDAD Y FECHA]

ANEXO III AL CONTRATO DE VENTA A PLAZOS DE BIENES MUEBLES

CLÁUSULAS DE INDEXACIÓN O REVISIÓN DE LAS CONDICIONES ECONÓMICAS

- Cláusula de revisión.

- Tipo de interés de referencia (índice de referencia objetivo).

- Tipo sustitutivo.

- Fórmula interés nominal (operaciones pactadas a tipo de interés variable):

A efectos de variación de interés en perjuicio de tercero se fija como tope máximo de interés el [PORCENTAJE] % nominal anual.

En prueba de conformidad, firman las partes el presente contrato en [Nº DE HOJAS] hojas numeradas correlativamente y en tantos ejemplares como partes intervienen.

COMPRADOR/ES	FIADOR/ES	VENDEDOR
En En En [LOCALIDAD Y FECHA]

CANCELACIÓN DE CONTRATO DE COMPRAVENTA A PLAZOS Modelo aprobado por Resolución de la Dirección General de los Registros y del Notariado de 18/02/2000

SOLICITUD DE CANCELACIÓN DE LA INSCRIPCIÓN DEL BIEN INSCRITO EN EL REGISTRO DE BIENES MUEBLES DE [LOCALIDAD]

A SOLICITUD DE [FECHA]

Y en su nombre y representación

DATOS DE PRESENTACIÓN: Diario [Nº DE DIARIO] Folio [FOLIO] Asiento [Nº DE ASIENTO]

DATOS DE INSCRIPCIÓN: Nº [Nº] de bien [Nº DE BIEN] Folio [FOLIO]

MOTIVO DE LA CANCELACIÓN

LA PARTE QUE FIGURA COMO ACREEDORA EN LA INSCRIPCIÓN REGISTRAL SOLICITA SEA CANCELADA LA RESERVA DE DOMINIO Y LA PROHIBICIÓN DE DISPONER, QUEDANDO EL COMPRADOR COMO TITULAR DEL PLENO DOMINIO DEL BIEN DE REFERENCIA

a [DÍA] de [MES] de [AÑO]

El vendedor (firma y sello)	Legitimación, Ratificación o Reconocimiento de firmas. (Obligatoria)

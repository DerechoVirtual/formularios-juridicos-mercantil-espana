---
name: contrato-prestamo-vendedor-financiar-comprador-bienes-mer-0662
description: "Contrato de préstamo del vendedor para financiar al comprador de bienes muebles. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de préstamo del vendedor para financiar al comprador de bienes muebles

> Formulario **MER-0662** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato de préstamo de financiación a comprador de bienes muebles, con condiciones generales, cuadro de amortización, anexos y solicitud de cancelación de la reserva de dominio en el Registro de Bienes Muebles. Se usa cuando el vendedor (o un financiador) concede crédito al comprador para pagar a plazos un bien mueble, en el marco de la Ley 28/1998, de Venta a Plazos de Bienes Muebles.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de préstamo del vendedor para financiar al comprador de bienes muebles» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de préstamo del vendedor para financiar al comprador de bienes muebles” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-prestamo-vendedor-financiar-comprador-bienes-mer-0662`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (17 veces)
- [ ] LOCALIDAD (16 veces)
- [ ] FIRMA (15 veces)
- [ ] IMPORTE (15 veces)
- [ ] Nº (9 veces)
- [ ] DOMICILIO (7 veces)
- [ ] MARCA (5 veces)
- [ ] MATRÍCULA (5 veces)
- [ ] MODELO (5 veces)
- [ ] Nº DE HOJAS (5 veces)
- [ ] NIF (4 veces)
- [ ] PORCENTAJE (4 veces)
- [ ] DATOS REGISTRALES (3 veces)
- [ ] PRIMER APELLIDO, SEGUNDO APELLIDO, NOMBRE, NIF, DOMICILIO (3 veces)
- [ ] NOMBRE (2 veces)
- [ ] PRIMER APELLIDO (2 veces)
- [ ] SEGUNDO APELLIDO (2 veces)
- [ ] AÑO
- [ ] CLÁUSULA DE REVISIÓN
- [ ] CONDICIONES DEL PAGO ANTICIPADO, EN SU CASO
- [ ] DENOMINACIÓN O NOMBRE Y APELLIDOS DEL VENDEDOR
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN
- [ ] DOMICILIO DE PAGO
- [ ] DÍA
- [ ] ELEMENTOS DEL COSTE DE ADQUISICIÓN
- [ ] FIRMA Y SELLO
- [ ] FORMA DE FIJACIÓN DEL VALOR DE TASACIÓN
- [ ] FÓRMULA
- [ ] FÓRMULA DE CÁLCULO
- [ ] LEGITIMACIÓN, RATIFICACIÓN O RECONOCIMIENTO DE FIRMAS
- [ ] MES
- [ ] MOTIVO, P. EJ., PAGO ÍNTEGRO DEL PRECIO APLAZADO
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL
- [ ] NOMBRE Y APELLIDOS, NIF, DOMICILIO Y TÍTULO DE LA REPRESENTACIÓN
- [ ] Nº DE FABRICACIÓN O CHASIS
- [ ] Nº DE MESES
- [ ] Nº DE PLAZOS
- [ ] OTRAS CLÁUSULAS PACTADAS
- [ ] REGISTRO DE BIENES MUEBLES COMPETENTE
- [ ] … y 4 datos más que aparecen una vez en el modelo

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: modelo aprobado originalmente por Resolución de la Dirección General de los Registros y del Notariado de 18/02/2000 (hoy, Dirección General de Seguridad Jurídica y Fe Pública). Comprobar el modelo oficial vigente. Si el comprador es consumidor, comprobar además la transposición de la Directiva (UE) 2023/2225 sobre contratos de crédito al consumo y la normativa vigente en la materia.

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

CONTRATO DE PRÉSTAMO DE FINANCIACIÓN A COMPRADOR DE BIENES MUEBLES

COMPRADOR

Primer apellido: [PRIMER APELLIDO]

Segundo apellido: [SEGUNDO APELLIDO]

Nombre: [NOMBRE]

NIF/CIF: [NIF]

Domicilio: [DOMICILIO]

[OPCIONAL — si el comprador es persona jurídica] Inscrita en: [DATOS REGISTRALES]

[OPCIONAL — si el comprador es persona jurídica] Y en su nombre y representación: [PRIMER APELLIDO, SEGUNDO APELLIDO, NOMBRE, NIF, DOMICILIO]

[OPCIONAL — si hay más de un comprador, repetir el bloque anterior]

FIADOR

Primer apellido: [PRIMER APELLIDO]

Segundo apellido: [SEGUNDO APELLIDO]

Nombre: [NOMBRE]

NIF/CIF: [NIF]

Domicilio: [DOMICILIO]

[OPCIONAL — si el fiador es persona jurídica] Inscrita en: [DATOS REGISTRALES]

[OPCIONAL — si el fiador es persona jurídica] Y en su nombre y representación: [PRIMER APELLIDO, SEGUNDO APELLIDO, NOMBRE, NIF, DOMICILIO]

[OPCIONAL — si no hay fiador, suprimir este bloque]

FINANCIADOR

Denominación: [DENOMINACIÓN SOCIAL]

CIF: [NIF]

Domicilio: [DOMICILIO]

Inscrita en: [DATOS REGISTRALES]

Y en su nombre y representación: [PRIMER APELLIDO, SEGUNDO APELLIDO, NOMBRE, NIF, DOMICILIO]

VENDEDOR: [DENOMINACIÓN O NOMBRE Y APELLIDOS DEL VENDEDOR], quien no interviene en este acto.

OBJETO

Modelo: [MODELO]

Marca: [MARCA]

Número de fabricación o chasis: [Nº DE FABRICACIÓN O CHASIS]

Matrícula (en su caso): [MATRÍCULA]

Unidad de cuenta: [IMPORTE] euros

Precio de la compraventa (valor al contado): [IMPORTE]

Coste de adquisición del bien: [IMPORTE]

Desembolso inicial (si lo hubiera): [IMPORTE]

Préstamo de financiación. Capital del préstamo: [IMPORTE]

Interés por aplazamiento: [Nº DE MESES] meses al [PORCENTAJE] %

Importe total del préstamo: [IMPORTE]

T.A.E.: [PORCENTAJE] %

RECONOCIMIENTO DE DEUDA.– El comprador reconoce deber al financiador la cantidad de [IMPORTE], que se pagará en [Nº DE PLAZOS] plazos conforme al plan de amortización que figura en hoja anexa, señalándose como domicilio de pago [DOMICILIO DE PAGO]. Por consiguiente, con fecha [FECHA] deberá quedar terminado el pago.

DERECHO DE DESISTIMIENTO.– [DESCRIPCIÓN DEL DERECHO DE DESISTIMIENTO DEL COMPRADOR, EN LOS TÉRMINOS Y PLAZOS LEGALMENTE PREVISTOS]

DOMINIO.– El objeto vendido se halla libre de gravámenes, y el dominio [ELEGIR: queda reservado al vendedor o financiador hasta el pago total del precio / se transmite al comprador en este acto].

En prueba de conformidad, firman las partes el presente contrato en [Nº DE HOJAS] hojas numeradas correlativamente y en tantos ejemplares como partes intervienen.

COMPRADOR/ES: En [LOCALIDAD], a [FECHA]. [FIRMA]

FIADOR/ES: En [LOCALIDAD], a [FECHA]. [FIRMA]

FINANCIADOR: En [LOCALIDAD], a [FECHA]. [FIRMA]

CONDICIONES GENERALES

1. COMPRADORES.– En caso de intervenir varios compradores, se obligan con carácter [ELEGIR: solidario / mancomunado] al cumplimiento de las obligaciones dimanantes del presente contrato.

2. FIADOR.– El o los fiadores afianzan [ELEGIR: solidariamente, con renuncia a los beneficios de excusión, orden y división / en los términos siguientes: [TÉRMINOS DE LA FIANZA]] el cumplimiento de las obligaciones del comprador derivadas de este contrato.

3. PROHIBICIÓN DE DISPONER.– El comprador no podrá realizar ningún acto de disposición o gravamen sin autorización escrita del financiador.

4. MORA EN EL PAGO.– A partir de cada vencimiento no satisfecho, el financiador podrá exigir al comprador el pago de [PORCENTAJE] por ciento sobre el mismo, aplicándose para su cálculo la fórmula [FÓRMULA DE CÁLCULO], sin perjuicio de que la falta de pago de dos de los plazos o del último de ellos pueda dar lugar al vencimiento de lo adeudado o a la resolución del contrato, con los efectos del artículo 10 de la Ley 28/1998.

5. PAGO ANTICIPADO.– El comprador podrá pagar anticipadamente [CONDICIONES DEL PAGO ANTICIPADO, EN SU CASO].

6. CESIÓN DE DERECHOS.– [CONDICIONES EN LAS QUE EL FINANCIADOR PUEDE CEDER SUS DERECHOS DERIVADOS DEL CONTRATO]

7. TASACIÓN.– El valor de tasación del objeto del presente contrato se fijará de la siguiente forma: [FORMA DE FIJACIÓN DEL VALOR DE TASACIÓN].

8. COSTE DE ADQUISICIÓN.– Los elementos que componen el coste de adquisición que figura en la hoja 1 de este contrato son: [ELEMENTOS DEL COSTE DE ADQUISICIÓN].

9. CÁLCULO DEL T.A.E.– La fórmula utilizada para el cálculo del T.A.E. es la recogida en el anexo I de la Ley 16/2011, de 24 de junio, de Contratos de Crédito al Consumo.

10. NOTIFICACIONES.– Se señalan como domicilios a efectos de notificaciones, requerimientos y emplazamientos los siguientes: Comprador: [DOMICILIO]. Fiador: [DOMICILIO]. Financiador: [DOMICILIO].

11. ENTREGA DEL EJEMPLAR DEL CONTRATO.– En cumplimiento de lo establecido en el artículo 6.1 de la Ley 28/1998, cada una de las partes intervinientes deberá recibir un ejemplar del presente contrato, debidamente firmado.

12. PLURALIDAD DE OBJETOS.– En estos casos se entenderá distribuido el importe total del préstamo proporcionalmente al valor al contado de cada bien, salvo pacto en contrario.

13. CONSUMACIÓN DE LA COMPRA.– El comprador se obliga a satisfacer al contado el precio de la compra con el importe del presente préstamo de financiación.

OTRAS CLÁUSULAS.– [OTRAS CLÁUSULAS PACTADAS]

En prueba de conformidad, firman las partes el presente contrato en [Nº DE HOJAS] hojas numeradas correlativamente y en tantos ejemplares como partes intervienen.

COMPRADOR/ES: En [LOCALIDAD], a [FECHA]. [FIRMA]

FIADOR/ES: En [LOCALIDAD], a [FECHA]. [FIRMA]

FINANCIADOR: En [LOCALIDAD], a [FECHA]. [FIRMA]

ANEXO I. CUADRO DE AMORTIZACIÓN

Vencimiento | Importe del plazo | Amortización de capital | Intereses | Capital pendiente

[FECHA] | [IMPORTE] | [IMPORTE] | [IMPORTE] | [IMPORTE]

[REPETIR UNA LÍNEA POR CADA PLAZO]

En prueba de conformidad, firman las partes el presente contrato en [Nº DE HOJAS] hojas numeradas correlativamente y en tantos ejemplares como partes intervienen.

COMPRADOR/ES: En [LOCALIDAD], a [FECHA]. [FIRMA]

FIADOR/ES: En [LOCALIDAD], a [FECHA]. [FIRMA]

FINANCIADOR: En [LOCALIDAD], a [FECHA]. [FIRMA]

ANEXO II. PLURALIDAD DE OBJETOS

COMPRADOR: [PRIMER APELLIDO, SEGUNDO APELLIDO, NOMBRE, NIF/CIF, DOMICILIO; SI ES PERSONA JURÍDICA: DATOS DE INSCRIPCIÓN Y DE REPRESENTACIÓN]

FIADOR: [PRIMER APELLIDO, SEGUNDO APELLIDO, NOMBRE, NIF/CIF, DOMICILIO; SI ES PERSONA JURÍDICA: DATOS DE INSCRIPCIÓN Y DE REPRESENTACIÓN]

Objeto 1: Marca: [MARCA]. Modelo: [MODELO]. Nº de fabricación o chasis: [Nº]. Matrícula (en su caso): [MATRÍCULA]. Valor al contado: [IMPORTE].

Objeto 2: Marca: [MARCA]. Modelo: [MODELO]. Nº de fabricación o chasis: [Nº]. Matrícula (en su caso): [MATRÍCULA]. Valor al contado: [IMPORTE].

Objeto 3: Marca: [MARCA]. Modelo: [MODELO]. Nº de fabricación o chasis: [Nº]. Matrícula (en su caso): [MATRÍCULA]. Valor al contado: [IMPORTE].

Objeto 4: Marca: [MARCA]. Modelo: [MODELO]. Nº de fabricación o chasis: [Nº]. Matrícula (en su caso): [MATRÍCULA]. Valor al contado: [IMPORTE].

Objetos no principales y accesorios: [DESCRIPCIÓN]

En prueba de conformidad, firman las partes el presente contrato en [Nº DE HOJAS] hojas numeradas correlativamente y en tantos ejemplares como partes intervienen.

COMPRADOR/ES: En [LOCALIDAD], a [FECHA]. [FIRMA]

FIADOR/ES: En [LOCALIDAD], a [FECHA]. [FIRMA]

FINANCIADOR: En [LOCALIDAD], a [FECHA]. [FIRMA]

ANEXO III. CLÁUSULAS DE INDEXACIÓN O REVISIÓN DE LAS CONDICIONES ECONÓMICAS

Cláusula de revisión: [CLÁUSULA DE REVISIÓN]

Tipo de interés de referencia (índice de referencia objetivo): [ÍNDICE DE REFERENCIA]

Tipo sustitutivo: [TIPO SUSTITUTIVO]

Fórmula de interés nominal (operaciones pactadas a tipo de interés variable): [FÓRMULA]

A efectos de variación de interés en perjuicio de tercero se fija como tope máximo de interés el [PORCENTAJE] % nominal anual.

En prueba de conformidad, firman las partes el presente contrato en [Nº DE HOJAS] hojas numeradas correlativamente y en tantos ejemplares como partes intervienen.

COMPRADOR/ES: En [LOCALIDAD], a [FECHA]. [FIRMA]

FIADOR/ES: En [LOCALIDAD], a [FECHA]. [FIRMA]

FINANCIADOR: En [LOCALIDAD], a [FECHA]. [FIRMA]

CANCELACIÓN DE CONTRATO DE COMPRAVENTA A PLAZOS

SOLICITUD DE CANCELACIÓN DE LA INSCRIPCIÓN DEL BIEN INSCRITO EN EL REGISTRO DE BIENES MUEBLES

A [REGISTRO DE BIENES MUEBLES COMPETENTE]

SOLICITANTE: [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL], [NIF], con domicilio en [DOMICILIO]

Y en su nombre y representación: [NOMBRE Y APELLIDOS, NIF, DOMICILIO Y TÍTULO DE LA REPRESENTACIÓN]

DATOS DE PRESENTACIÓN: Diario [Nº]. Folio [Nº]. Asiento [Nº].

DATOS DE INSCRIPCIÓN: Nº de bien [Nº]. Folio [Nº].

MOTIVO DE LA CANCELACIÓN: [MOTIVO, P. EJ., PAGO ÍNTEGRO DEL PRECIO APLAZADO]

LA PARTE QUE FIGURA COMO ACREEDORA EN LA INSCRIPCIÓN REGISTRAL SOLICITA SEA CANCELADA LA RESERVA DE DOMINIO Y LA PROHIBICIÓN DE DISPONER, QUEDANDO EL COMPRADOR COMO TITULAR DEL PLENO DOMINIO DEL BIEN DE REFERENCIA.

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

El vendedor (firma y sello): [FIRMA Y SELLO]

Legitimación, ratificación o reconocimiento de firmas (obligatoria): [LEGITIMACIÓN, RATIFICACIÓN O RECONOCIMIENTO DE FIRMAS]

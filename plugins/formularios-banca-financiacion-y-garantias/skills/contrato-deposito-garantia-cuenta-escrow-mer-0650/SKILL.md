---
name: contrato-deposito-garantia-cuenta-escrow-mer-0650
description: "Contrato de depósito en garantía o cuenta escrow. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de depósito en garantía o cuenta escrow

> Formulario **MER-0650** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de depósito en garantía o cuenta escrow» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de depósito en garantía o cuenta escrow” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-deposito-garantia-cuenta-escrow-mer-0650`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] FECHA (6 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] DNI/NIE (3 veces)
- [ ] Nº DE PROTOCOLO (3 veces)
- [ ] AÑO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] DÍA
- [ ] ENTIDAD MEDIADORA
- [ ] FUNDAMENTOS
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] Nº DE CLÁUSULA

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte, D. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD] y titular del DNI [DNI/NIE]

De otra parte, D. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD] y titular del DNI [DNI/NIE]

Y, de otra, D. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD] y titular del DNI [DNI/NIE]

INTERVIENEN

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL FIDEICOMITENTE", en virtud de poder otorgado a su favor ante el Notario de D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD], y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL BENEFICIARIO", en virtud de poder otorgado a su favor ante el Notario de D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD], y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de la entidad [DENOMINACIÓN SOCIAL], en lo sucesivo "LA FIDUCIARIA", en virtud de poder otorgado a su favor ante el Notario de D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD], y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE FIDEICOMISO DE DEPÓSITO CONDICIONADO, y a tal efecto, libremente y de común acuerdo

EXPONEN

PRIMERO.- Que EL FIDEICOMITENTE y EL BENEFICIARIO han concertado en fecha [FECHA], un contrato de compraventa del 100% de las acciones de la sociedad [DENOMINACIÓN SOCIAL], copia del cual se adjunta al presente documento como Anexo I.

SEGUNDO.- Que en la cláusula [Nº DE CLÁUSULA] del citado contrato se estipula que EL FIDEICOMITENTE está obligado a pagar al BENEFICIARIO en el término de quince días desde la aprobación de las cuentas anuales de los ejercicios sociales de los años [AÑO] la cantidad negativa resultante en caso de pérdidas y en concepto de minoración de precio.

TERCERO.- Que EL FIDEICOMITENTE y EL BENEFICIARIO convienen en constituir un depósito en garantía (escrow account) con LA FIDUCIARIA, quien tendrá la obligación de recibir, custodiar y desembolsar los fondos depositados con arreglo a las estipulaciones de este contrato.

CUARTO.- Que por ello, las partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Depósito

Las partes convienen constituir un depósito en la entidad FIDUCIARIA por importe de [IMPORTE] euros en la cuenta número [NÚMERO], el cual se realiza en este acto mediante transferencia bancaria ordenada por el FIDEICOMITENTE cuyo resguardo se adjunta como Anexo II.

Disposición de fondos a favor del beneficiario

Los fondos depositados la citada cuenta serán entregados por la entidad FIDUCIARIA al BENEFICIARIO por el importe que resulte de las pérdidas sufridas en cada uno de los ejercicios sociales por la sociedad [DENOMINACIÓN SOCIAL] contra la entrega de la siguiente documentación:

- Cuentas anuales aprobadas.

- Informe de auditoría de las cuentas.

- Notificación previa al FIDEICOMITENTE de las cuentas e informe de auditoría.

La solicitud del BENEFICIARIO deberá realizarse dentro de los tres meses siguientes al cierre del ejercicio social.

Transcurrido dicho periodo sin haberse formulado solicitud ante la FIDUCIARIA, caducará el derecho del BENEFICIARIO, no pudiendo entregarse cantidad alguna correspondiente al ejercicio social vencido.

Las partes pactan expresamente que podrán modificar esta cláusula mediante nuevo acuerdo entre FIDEICOMITENTE Y BENEFICIARIO que será comunicado fehacientemente a LA FIDUCIARIA.

Disposición de fondos a favor del fideicomitente

Transcurridos tres meses desde la finalización del último de los ejercicios sociales referidos en el contrato incorporado como Anexo I, es decir, el día [FECHA], sin estar pendiente ninguna solicitud de entrega del BENEFICIARIO, la cantidad depositada o su remanente quedará a disposición del FIDEICOMITENTE, debiendo ser entregada por la FIDUCIARIA tan pronto sea requerida para ello.

Duración

El presente contrato estará vigente hasta el día [FECHA], y podrá ser prorrogado mediante acuerdo celebrado por escrito entre las partes, siempre y cuando esto se realice con [Nº] días de antelación al vencimiento del plazo inicialmente pactado.

Intereses

El depósito generará un interés del [PORCENTAJE] % que quedará a favor y a la libre disposición del FIDEICOMITENTE, debiendo ser ingresado por LA FIDUCIARIA en la cuenta número [NÚMERO], titularidad de aquel y abierta en esta entidad.

Retribución

La FIDUCIARIA percibirá en concepto honorarios por la prestación de sus servicios una comisión del [PORCENTAJE] % sobre los fondos depositados en concepto de comisión de apertura de cuenta, y una cantidad anual de [IMPORTE] euros durante el período de duración del depósito.

Dichas cantidades serán satisfechas por EL FIDEICOMITENTE.

EL BENEFICIARIO será responsable solidario del pago en caso de que no lo hiciera EL FIDEICOMITENTE, pudiendo dirigirse LA FIDUCIARIA indistintamente contra uno u otro responsable en caso de impago.

Responsabilidad de la fiduciaria

LA FIDUCIARIA se obliga a custodiar y desembolsar los fondos en la forma pactada en este contrato. Será responsable de los incumplimientos derivados de la disposición de los fondos o de la falta de entrega de los mismos con contravención de lo pactado, en cuyo caso deberá indemnizar todos los daños y perjuicios que hayan sufrido cualquiera de las partes.

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo del FIDEICOMITENTE.

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Resolución de conflictos: sumisión a mediación y arbitraje

Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, se resolverán a través de la Mediación [ENTIDAD MEDIADORA], de [LOCALIDAD], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y [FUNDAMENTOS] fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de la Corte de [LOCALIDAD], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

Y en prueba de conformidad y aceptación de cuanto antecede, las partes firman los folios del presente CONTRATO DE FIDEICOMISO DE DEPÓSITO CONDICIONADO, extendido por triplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

Fdo. (EL FIDEICOMITENTE) (EL BENEFICIARIO) (LA FIDUCIARIA)

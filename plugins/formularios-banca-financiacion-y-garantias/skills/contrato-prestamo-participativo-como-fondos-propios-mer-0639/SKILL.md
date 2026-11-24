---
name: contrato-prestamo-participativo-como-fondos-propios-mer-0639
description: "Contrato de préstamo participativo como fondos propios del prestatario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de préstamo participativo como fondos propios del prestatario

> Formulario **MER-0639** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de préstamo participativo como fondos propios del prestatario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de préstamo participativo como fondos propios del prestatario” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-prestamo-participativo-como-fondos-propios-mer-0639`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] PLAZO (3 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DE LA OPERACIÓN
- [ ] FECHA
- [ ] LUGAR
- [ ] Nº
- [ ] PORCENTAJE
- [ ] TIPO DE INTERÉS

## Normas que cita el formulario

- art. 20 Ley 7/1996
- art. 311 Código de Comercio

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

Instrumento financiero concebido como un préstamo a largo plazo computado como fondos propios de la empresa prestataria. Normalmente, el tipo de interés a pagar varía en función de los resultados de la compañía prestataria, aunque puede pactarse uno fijo.

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

(Datos del PRESTAMISTA)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, PRESTAMISTA.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

(Datos del PRESTATARIO)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, PRESTATARIO.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de PRÉSTAMO PARTICIPATIVO y, a tal fin,

MANIFIESTAN

I. Que EL PRESTAMISTA se dedica a [ACTIVIDAD]

II. Que EL PRESTATARIO se dedica a [ACTIVIDAD], y pretende realizar la siguiente negocio [DESCRIPCIÓN DE LA OPERACIÓN], en lo sucesivo OPERACIÓN, para lo cual precisa efectuar una inversión de [IMPORTE] euros, y careciendo de liquidez ha decidido dirigirse al PRESTAMISTA, y que por ello ambas partes.

ACUERDAN

Llevar a efecto el presente contrato de PRÉSTAMO PARTICIPATIVO mediante las siguientes:

CLÁUSULAS

Primera.- Objeto

EL PRESTAMISTA entrega en concepto de préstamo al prestatario, que acepta, la cantidad de [IMPORTE] euros, que deberán ser devueltos y reintegrados por dicho prestatario en las circunstancias y condiciones que se señalan en el presente contrato.

El Préstamo se concede al Prestatario para la financiación de las actividades que constituyen y son propias de su objeto social, obligándose ésta a destinar a tal fin el total importe prestado en función de sus necesidades.

Segunda.- Devolución

El prestatario se compromete a reintegrar al prestamista la cantidad percibida en el plazo de [PLAZO] contados desde la fecha de hoy y en [Nº] pagos, mediante ingresos en la cuenta corriente que dicho prestatario tiene abierta a su nombre en la entidad [DENOMINACIÓN SOCIAL] con número .Para el caso de que el prestatario no cumpliera su obligación de reintegro en las fechas expresadas, las partes acuerdan un interés de demora del [TIPO DE INTERÉS] %

[OPCIONAL — incluir si procede]

(Prórrogas)

Las partes, podrán de común acuerdo prorrogar la vigencia del Préstamo por periodos sucesivos de [PLAZO], siempre que, con un [PLAZO] de antelación al vencimiento del contrato, el Prestamista y el Prestatario, manifestaren por escrito firmado por personas debidamente autorizadas al efecto, su postura a favor de la prórroga del mismo y por la cantidad a convenir por las partes.

Tercera.- Amortización anticipada

El Prestatario podrá amortizar anticipadamente, de forma total o parcial, el Préstamo siempre que el importe de la amortización sea de un mínimo de [IMPORTE]. Por excepción, en el supuesto de que la cuantía total pendiente de amortización sea inferior a dicha cifra, la amortización anticipada podrá realizarse por dicha cuantía mínima.

[OPCIONAL — incluir si procede]

(Penalización)

En caso de amortización anticipada, el Prestatario vendrá obligado a pagar una penalización equivalente al % del principal amortizado.

Cuarta.- Intereses

El interés de este préstamo es de carácter participativo, fijándose por lo tanto un interés del [PORCENTAJE] % del beneficio neto del negocio, pagadero, en igual momento y lugar que la cantidad principal.

Se considerará beneficio social el resultado después de impuestos, estimándose a estos efectos el beneficio por resultados ordinarios o extraordinarios y sea cual sea la aplicación que se haya decidido del mismo, determinados conforme a los principios contables establecidos en la normativa contables española, pero sin incluir los propios intereses derivados de este préstamo.

En el caso de que el negocio no produjera beneficios, el préstamo presente no devengará interés alguno

Quinta.- Formalización

El presente contrato podrá ser elevado a escritura pública a petición de cualquiera de las partes, corriendo los gastos en que con ello se incurra a cargo de quien interese dicho acto.

Sexta.- Protección de datos personales

Las partes reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

Séptima.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Octava.- Gastos e Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta del [ELEGIR: prestamista / el prestatario].

Novena.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por el artículo 20 del Real Decreto Ley 7/1996, de 7 de junio, artículos 311 y siguientes del Código de Comercio de 1885, leyes especiales y usos mercantiles que le sean aplicables, o en lo no previsto, por las disposiciones del Código Civil de 1889..

Décima.- Fuero competente

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Tribunales de [LOCALIDAD]

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

PRESTAMISTA

________________________________

PRESTATARIO

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

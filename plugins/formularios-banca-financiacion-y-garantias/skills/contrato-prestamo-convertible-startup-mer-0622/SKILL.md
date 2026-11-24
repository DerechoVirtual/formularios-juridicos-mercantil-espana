---
name: contrato-prestamo-convertible-startup-mer-0622
description: "Contrato de préstamo convertible a una startup. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de préstamo convertible a una startup

> Formulario **MER-0622** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Se trata de un préstamo a corto plazo mediante el cual el inversor inyecta capital en una startup a cambio no de la recuperación del mismo más intereses, sino de la adquisición de acciones preferentes. Una nota convertible es un tipo de financiamiento híbrido que comienza como una deuda a corto plazo y termina en acciones en una fecha posterior.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de préstamo convertible a una startup» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de préstamo convertible a una startup” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-prestamo-convertible-startup-mer-0622`.
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
- [ ] FECHA (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] PLAZO (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] DATOS DE PERSONA ADICIONAL
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL PROYECTO
- [ ] ENTIDAD BANCARIA
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] NÚMERO
- [ ] OBJETO DE LA FINANCIACIÓN
- [ ] OTROS DATOS
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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Se trata de un préstamo a corto plazo mediante el cual el inversor inyecta capital en una startup a cambio no de la recuperación del mismo más intereses, sino de la adquisición de acciones preferentes. Una nota convertible es un tipo de financiamiento híbrido que comienza como una deuda a corto plazo y termina en acciones en una fecha posterior.


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

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de PRÉSTAMO O NOTA CONVERTIBLE y, a tal fin,

MANIFIESTAN

I. Que la PRESTATARIO, [ELEGIR: se dedica a / tiene por objeto social el desarrollo de].

II. Que el PRESTAMISTA debidamente informado, desea impulsar la actividad del PRESTATARIO mediante la financiación de [OBJETO DE LA FINANCIACIÓN], en las condiciones que se indican en las cláusulas de este contrato.

ACUERDAN

Llevar a efecto el presente contrato de PRÉSTAMO o NOTA CONVERTIBLE de acuerdo con las siguientes:

CLÁUSULAS

Primera.- Objeto

El PRESTAMISTA concede a la PRESTATARIA, quien acepta, un préstamo por un importe total de (€), que se destinará a dotar a [NOMBRE DE LA PARTE] de fondos necesarios para financiar el proyecto de [DESCRIPCIÓN DEL PROYECTO].

El importe indicado se abonará y será satisfecho con carácter inmediato tras la firma del presente contrato, no más tarde de [FECHA] mediante abono en la cuenta abierta a nombre del PRESTATARIO, número [NÚMERO], Banco [ENTIDAD BANCARIA].

Segunda.- Duración

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

El PRESTAMO se concede por un plazo de [PLAZO] con finalización el [FECHA] no siendo posible su prórroga.

El PRESTAMO se concede por un plazo de [PLAZO] con finalización el [FECHA] prorrogable [ELEGIR: por iguales plazos / por el plazo máximo y único de desde la citada fecha de vencimiento] salvo en caso de que medie denuncia expresa por alguna de las partes con una antelación mínima de [PLAZO] a la fecha de vencimiento.

Tercera.- Intereses

El PRÉSTAMO devengará un interés del [PORCENTAJE] anual a favor de la PRESTAMISTA, desde la fecha de la firma del presente contrato hasta la fecha de vencimiento.

Los intereses que devengue el PRÉSTAMO se calcularán sobre el saldo del principal vivo no vencido.

Los intereses se liquidarán en a la fecha de vencimiento o, en su caso, serán capitalizados en su totalidad junto con el principal.

[OPCIONAL — incluir si procede]

(Carencia)

Las Partes acuerdan una carencia en el devengo de los intereses descritos hasta la conversión del préstamo en [ELEGIR: participaciones sociales / acciones].

Cuarta.- Conversión

LA PRESTATARIA deberá en cualquier momento antes de la fecha de vencimiento o de la correspondiente prórroga, convertir el PRÉSTAMO en [ELEGIR: participaciones / acciones] del capital social de [ELEGIR: SL / SA]

A estos efectos, se tomará como base mínima la valoración pre-money de [IMPORTE] para la primera fase de la primera ronda de financiación [OTROS DATOS], de [IMPORTE] euros (€).

Quinta.- Ejercicio de la Opción

comunicará por escrito al PRESTAMISTA su voluntad de convertir la totalidad del PRINCIPAL del PRÉSTAMO en [ELEGIR: participaciones sociales / acciones], solicitando a su vez el inicio de los trámites legales correspondientes a la conversión descrita en capital social de [DENOMINACIÓN SOCIAL].

Para ello será necesario que medie un acuerdo de ampliación de capital por compensación de créditos de la Junta General de Socios de y, en su caso desembolso dinerario.

[OPCIONAL — incluir si procede]

(Plazo)

Dicha Junta General deberá celebrarse dentro de a la recepción de la comunicación de la PRESTATARIA descrita.

Sexta.- Protección de datos personales

Las partes de este contrato conocen y se obligan a cumplir el Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016, relativo a la protección de las personas físicas en lo que respecta al tratamiento de datos personales y a la libre circulación de estos datos (RGPD), así como la Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales y su normativa de desarrollo, y/o aquellas que las pudieran sustituir o actualizar en el futuro, donde se establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

Séptima.- Notificaciones

Las partes señalan como correos electrónicos para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[DATOS DE PERSONA ADICIONAL]

Octava.- Conservación y modificación

Si cualquiera de las cláusulas del contrato fuera nula o anulable, dicha declaración no invalidará el resto del Contrato, que mantendrá su vigencia y eficacia. En tal caso, la cláusula o cláusulas nulas deberán sustituirse por otras que, siendo conformes a la ley, respondan al espíritu y finalidad de las iniciales.

Novena.- Gastos e Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta del [ELEGIR: prestamista / el prestatario].

Décima.- Formalización

El presente contrato podrá ser elevado a escritura pública a petición de cualquiera de las partes, corriendo los gastos en que con ello se incurra a cargo de quien interese dicho acto.

Decimoprimera.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por la normativa española.

Decimosegunda.- Fuero competente

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Tribunales de [LOCALIDAD].

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD].

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

PRESTAMISTA

PRESTATARIO
D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]

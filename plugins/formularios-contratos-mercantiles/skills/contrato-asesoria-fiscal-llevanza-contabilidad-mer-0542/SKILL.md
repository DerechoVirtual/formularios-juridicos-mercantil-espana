---
name: contrato-asesoria-fiscal-llevanza-contabilidad-mer-0542
description: "Contrato de asesoría fiscal y llevanza de contabilidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de asesoría fiscal y llevanza de contabilidad

> Formulario **MER-0542** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de asesoría fiscal y llevanza de contabilidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de asesoría fiscal y llevanza de contabilidad” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-asesoria-fiscal-llevanza-contabilidad-mer-0542`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] TIPO DE SOCIEDAD (2 veces)
- [ ] ENTIDAD BANCARIA
- [ ] FECHA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NOMBRE O DENOMINACIÓN
- [ ] Nº
- [ ] OBJETO SOCIAL

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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de ARRENDADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ARRENDADOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del CLIENTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CLIENTE.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de PRESTACIÓN DE SERVICIOS CONTINUADOS y, a tal fin,

EXPONEN

I. Que el Arrendador es una [TIPO DE SOCIEDAD] cuya actividad es la asesoría fiscal y contable.

II. Que el Cliente, es una [TIPO DE SOCIEDAD] cuyo objeto social es [OBJETO SOCIAL].

III. Que el Cliente tiene la intención de concertar un servicio de asesoramiento fiscal y contable.

IV. Que ambas partes han alcanzado un acuerdo en virtud del cual el Arrendador se compromete a llevar a cabo un servicio de asesoramiento fiscal y llevanza de contabilidad al Cliente, otorgando el presente contrato de arrendamiento de servicios con arreglo a las siguientes:

ESTIPULACIONES

Primera.- Objeto

El objeto del presente contrato es el desarrollo por parte del Arrendador de los servicios profesionales de asesoramiento fiscal y llevanza de contabilidad del Cliente. En concreto, el Arrendador se obliga:

1.1. A llevar la contabilidad del Cliente con arreglo al Plan General Contable.
1.2. A preparar y entregar al Cliente, mensualmente, un balance de la situación y de saldos, análisis económico y financiero; trimestralmente, sus balances y cuenta de pérdidas y ganancias; y, anualmente, la memoria, balance y cuenta de resultados, análisis económico y financiero.
1.3. A llevar a cabo las gestiones necesarias para que tenga lugar el correspondiente depósito de cuentas en el Registro Mercantil.
1.4. A llevar a cabo un servicio de asesoramiento fiscal permanente, dentro del cual se entienden incluidos tanto la respuesta oral o escrita a cualquier consulta de esta índole que le sea efectuada, como el cumplimiento de todas y cada una de las obligaciones fiscales del Cliente, incluida la elaboración y presentación de las liquidaciones de todos los impuestos y, en su caso, la elaboración y presentación de los recursos administrativos que el Cliente considere oportuno presentar frente a las resoluciones de la Agencia Tributaria.
1.5. A representar al Cliente en todas las gestiones, actos, inspecciones y comparecencias que deba efectuar ante la Administración Tributaria.

Segunda.- Servicios excluidos

Quedan expresamente excluidas del presente contrato la defensa o actuación jurídica en favor del Cliente, que se produzcan ante la jurisdicción ordinaria.

Tercera.- Duración

El presente contrato tendrá una duración anual, prorrogable automáticamente si a la finalización del mismo no es denunciado por ninguna de las partes, con al menos 30 días de antelación.

Cuarta.- Precio

El Arrendador recibirá la cantidad de [IMPORTE] euros ( €) brutos mensuales, pagaderos en los 5 primeros días de cada mes, que se abonarán por el Cliente, mediante cheque o ingreso en la cuenta corriente núm. «[NOMBRE O DENOMINACIÓN]», en el Banco/Caja [ENTIDAD BANCARIA], sucursal de [LOCALIDAD], a nombre del Arrendador.

Quinta.- Deber de información

Con el objeto de que el Arrendador pueda desarrollar satisfactoriamente la actividad que le ha sido encomendada, el Cliente deberá poner a disposición de aquél todos los datos necesarios acompañándose los mismos de los correspondientes justificantes documentales.

Sexta.- Confidencialidad

El Arrendador asume el compromiso de mantener la más absoluta confidencialidad sobre los datos e informaciones que le suministre el Cliente o de los que tenga conocimiento como consecuencia de las funciones que tiene encomendadas en virtud de este contrato.

Séptima.- Incumplimiento de obligaciones fiscales

En el caso de que, como consecuencia de la prestación de servicios que lleva a cabo el Arrendador, tenga lugar el incumplimiento de las obligaciones fiscales o contables del Cliente, el Arrendador vendrá obligado a hacer frente a las posibles sanciones o multas impuestas a aquél, que serán deducidas del precio a abonar por éste hasta donde alcance. Quedando además facultada en tal caso para la resolución del presente contrato con una indemnización por daños y perjuicios equivalente a la sanción pecuniaria impuesta que deberá ser abonada por el Arrendador.

Octava.- Terminación y resolución del contrato

Son causas de terminación y resolución del presente contrato las siguientes:

a) Su vencimiento, bien por cumplimiento o por acuerdo mutuo de las partes.
b) Por incumplimiento de cualquiera de las partes de alguna de las cláusulas del presente contrato, sin que dicho incumplimiento fuera subsanado dentro de los [Nº] días siguientes a la notificación por escrito efectuada por la otra parte solicitando la subsanación del incumplimiento.
c) La declaración de concurso o la interposición en contra de cualquiera de las partes de juicios ejecutivos o embargos preventivos u otras medidas cautelares que impliquen la disminución de la solvencia económica de las mismas.

Novena.- Gastos del contrato

Queda expresamente convenido que todos los gastos, impuestos, contribuciones, tasas o arbitrios, presentes o futuros, que origine este contrato serán satisfechos por el arrendador.

Décima.- Sometimiento a arbitraje

Con renuncia expresa al ejercicio de cualquier acción ante los tribunales, las partes se comprometen expresamente a instituir, en su día, un arbitraje, con arreglo a la legislación vigente, para resolver cuantas dudas o divergencias pudieran surgir entre ellas como consecuencia de la interpretación o cumplimiento de este contrato.

Undécima.- Normativa aplicable al contrato

El presente contrato tiene carácter de mercantil y se regirá, en primer término, por las estipulaciones contenidas en el mismo, y, en lo en ellas no previsto, por las disposiciones del Código de Comercio, leyes especiales, los usos y costumbres mercantiles.

Conformes las partes con el contenido del presente contrato lo firman por duplicado en el lugar y fecha arriba indicados.

ARRENDADOR

CLIENTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

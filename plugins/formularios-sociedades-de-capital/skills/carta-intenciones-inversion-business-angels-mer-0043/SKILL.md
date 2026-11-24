---
name: carta-intenciones-inversion-business-angels-mer-0043
description: "Carta de intenciones de inversión con business angels. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Carta de intenciones de inversión con business angels

> Formulario **MER-0043** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Carta de intenciones de inversión con business angels» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Carta de intenciones de inversión con business angels” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:carta-intenciones-inversion-business-angels-mer-0043`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE DEL PROYECTO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] CALENDARIO DE ACTUACIONES
- [ ] DENOMINACIÓN SOCIAL
- [ ] FECHA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE EJERCICIOS
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

Objeto del Proyecto
Suscripción de capital. Precio, porcentaje de participación y forma de pago
Calendario de actuaciones
Naturaleza no vinculante
Contenido vinculante

Declaración de intenciones del Business Angel no vinculante sobre la toma de participación y la inversión en un Proyecto desarrollado por una empresa

En [LUGAR], a [FECHA].

D./Dña. [NOMBRE Y APELLIDOS], en nombre propio (en adelante BA), y D./Dña. [NOMBRE Y APELLIDOS], en representación de [NOMBRE DEL REPRESENTADO/A] SL (En adelante PROMOTOR) han mantenido conversaciones preliminares sobre el interés del BA en participar en el proyecto [NOMBRE DEL PROYECTO] mediante la inversión en la compañía [DENOMINACIÓN SOCIAL] SL (en adelante la SOCIEDAD).

Objeto del Proyecto

El interés de las Partes se concreta en la toma de participación y la inversión del BA en el Proyecto [NOMBRE DEL PROYECTO]

Dicha toma de participación se canalizará mediante la suscripción del BA de un porcentaje de participación de la SOCIEDAD, con la posibilidad de que se prevea una ampliación del capital de la misma.

Suscripción de capital. Precio, porcentaje de participación y forma de pago

El BA podrá adquirir, mediante el aumento de capital en la SOCIEDAD correspondiente, una participación monetaria valorada en [IMPORTE] euros, que supone una adquisición del % del capital de la SOCIEDAD. No obstante, el BA acuerda ofrecer a los actuales socios de la SOCIEDAD un ratchet del %, de tal forma que según el grado de consecución —de acuerdo con lo que se establece en el Pacto de Socios— del EBITDA previsto en el Plan de Negocio de la SOCIEDAD, el [PORCENTAJE] del capital en posesión del BA podrá ser adquirido por los socios actuales de la SOCIEDAD durante el periodo de permanencia del BA como socio de la SOCIEDAD.

Las Partes celebrarán un Contrato entre Socios, que regulará los términos y las condiciones en los que el BA adquirirá una participación en el capital social de la SOCIEDAD, como también el gobierno y la dirección de la SOCIEDAD, a partir de la toma de participación del BA y de las relaciones entre todos los socios.

Sin perjuicio de la ulterior definición del contenido, el Pacto de Socios incorporará las siguientes disposiciones:

La participación del BA en el capital social de la SOCIEDAD tendría carácter temporal. A tal efecto, transcurrido un periodo de [Nº DE EJERCICIOS] ejercicios desde la realización de la inversión, si el BA todavía fuera socio de la SOCIEDAD, los socios de la SOCIEDAD se comprometerían a facilitar la desinversión del BA en la SOCIEDAD, de tal forma que las participaciones del BA las comprarían sus socios en los términos establecidos en el Pacto de Socios.

El valor de la desinversión se basará en un múltiplo del EBITDA medio anual de la SOCIEDAD.

Calendario de actuaciones

Las Partes fijan como calendario de actuaciones en el que establecerán las distintas operaciones que tendrán que realizar el siguiente:

[CALENDARIO DE ACTUACIONES]

Naturaleza no vinculante

Esta carta constituye una declaración de intenciones del BA y no establece compromisos vinculantes, excepto lo que se dirá en el siguiente pacto. Por consiguiente, la intención de las Partes requerirá, para que sea vinculante, la celebración de los respectivos acuerdos y contratos mencionados anteriormente. Por este motivo, ninguna de las Partes incurrirá en ninguna responsabilidad ante la otra en el caso de que no se llegue a un acuerdo final sobre el contenido de los acuerdos y contratos mencionados.

Contenido vinculante

No obstante, lo indicado, las partes declaran el carácter vinculante exigible de los compromisos y las obligaciones que asumen, de acuerdo con lo que disponen los apartados siguientes:

• Buena fe [ELEGIR: • Periodo de vigencia / • Confidencialidad / • Exclusividad / • Jurisdicción]

Si los términos aquí contenidos merecen su conformidad, se ruega firmen los dos ejemplares originales de esta carta como muestra de aceptación y que devuelvan un original

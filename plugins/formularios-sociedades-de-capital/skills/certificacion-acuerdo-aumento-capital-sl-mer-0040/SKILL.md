---
name: certificacion-acuerdo-aumento-capital-sl-mer-0040
description: "Certificación del acuerdo de aumento de capital de una SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Certificación del acuerdo de aumento de capital de una SL

> Formulario **MER-0040** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de certificado de acta de Junta General Extraordinaria Convocada o Universal de Socios de una Sociedad de Responsabilidad Limitada en la que, en primer lugar, se acuerda el aumento del capital social por elevación del valor nominal de las participaciones o por creación de nuevas con cargo a: aportaciones dinerarias o no dinerarias, incluida la aportación de créditos contra la sociedad; beneficios o reservas que ya figurasen en el último balance aprobado y, en segundo lugar, se procede a la modificación de los estatutos sociales en lo que afecte a ese aumento de capital (art.295 TRLSC)

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Certificación del acuerdo de aumento de capital de una SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Certificación del acuerdo de aumento de capital de una SL” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:certificacion-acuerdo-aumento-capital-sl-mer-0040`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (4 veces)
- [ ] Nº DE ARTÍCULO (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] FECHA (2 veces)
- [ ] LUGAR (2 veces)
- [ ] DIRECCIÓN
- [ ] LOCALIDAD
- [ ] PLAZO
- [ ] PUNTO DEL ORDEN DEL DÍA
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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Modelo de certificado de acta de Junta General Extraordinaria Convocada o Universal de Socios de una Sociedad de Responsabilidad Limitada en la que, en primer lugar, se acuerda el aumento del capital social por elevación del valor nominal de las participaciones o por creación de nuevas con cargo a: aportaciones dinerarias o no dinerarias, incluida la aportación de créditos contra la sociedad; beneficios o reservas que ya figurasen en el último balance aprobado y, en segundo lugar, se procede a la modificación de los estatutos sociales en lo que afecte a ese aumento de capital (art.295 TRLSC)


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

En [LUGAR], a [FECHA].

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de [ELEGIR: administrador único / administrador solidario / administradores mancomunados / Secretario del Consejo de Administración] de ‘[DENOMINACIÓN SOCIAL], S.L.’ y de su Junta de socios reunida el pasado

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en mi calidad de [ELEGIR: liquidador único / liquidador solidario / liquidadores mancomunados / Secretario del Consejo de Liquidación] de ‘[DENOMINACIÓN SOCIAL], S.L.’ y de su Junta de socios reunida el pasado

CERTIFICA

- Que en [LOCALIDAD] en la [DIRECCIÓN], el domicilio social de SL con fecha de ", se celebró Junta General Universal de socios de la entidad.
- Que en la junta estuvo, presente la totalidad del capital social, todo él con derecho a voto, y
- Que todos los asistentes firmaron en el acta, bajo su nombre respectivo, aceptando la constitución de la Junta con carácter de universal y con el siguiente

Orden del día

Primero. Aumento del capital social de la sociedad en la cantidad de [IMPORTE] euros y modificación del artículo [Nº DE ARTÍCULO] de los estatutos sociales.

Segundo. [PUNTO DEL ORDEN DEL DÍA].

Ruegos y preguntas.

Lectura y aprobación del acta

- Que, conforme a las disposiciones legales y estatutarias, se designaron los cargos de Presidente y Secretario de la reunión.
- Que se confeccionó por escrito la lista de asistentes, la cual obra al comienzo del acta.
- Que la Junta adoptó, por unanimidad, los acuerdos que se transcriben literalmente a continuación:

ACUERDOS

Primero. Aumento del capital social.

[OPCIONAL — incluir si procede]

(Por elevación del valor nominal de las participaciones sociales)

Aumentar el capital social de la sociedad en la cantidad de [IMPORTE] euros mediante la elevación del valor nominal de todas las participaciones sociales existentes en [IMPORTE] euros cada una, siendo el valor nominal final de cada participación social de [IMPORTE] euros.

[ELEGIR UNA OPCIÓN: Con aportaciones dinerarias / Con aportaciones no dinerarias y mixtas / Por compensación de créditos / Mediante transformación de reservas y beneficios]

Se declara íntegramente suscrito y desembolsado en un 100% el aumento de capital a razón de [IMPORTE] euros por participación.

[OPCIONAL — incluir si procede]

(Por creación de nuevas participaciones)

Aumentar el capital social de la sociedad en la cifra de [IMPORTE] euros mediante la creación de [Nº] nuevas participaciones sociales de igual valor nominal y contenido de derechos que las anteriores, y numeradas correlativamente del [Nº] a [Nº], ambos inclusive.

[ELEGIR UNA OPCIÓN: Sin prima de asunción / Con prima de asunción]

[OPCIONAL — incluir si procede]

(Con derecho de suscripción preferente)

Se reconoce a los socios el derecho a asumir un número de las nuevas participaciones sociales proporcional al valor nominal de las que poseen con arreglo a las siguientes normas:

- La relación de cambio será la siguiente:

participaciones sociales nuevas por cada una antigua.

- El plazo del que se dispone para el ejercicio del derecho de suscripción es de [PLAZO]
desde la publicación en el BORME del anuncio del aumento
desde el envío de la comunicación escrita
- Respecto a las participaciones sociales no asumidas en ejercicio del derecho de preferente asunción, serán ofrecidas por el órgano de administración en los términos previstos en [ELEGIR: la Ley / los Estatutos Sociales].

En caso de desembolso incompleto dentro del plazo fijado para ello, el aumento de capital quedará sin efecto.

[OPCIONAL — incluir si procede]

(Sin derecho de suscripción preferente)

A pesar de que se reconoce a los socios el derecho a asumir un número de las nuevas participaciones sociales proporcional al valor nominal de las que poseen, renuncian de forma expresa a este derecho de suscripción preferente ante la propia Junta, obviándose, por tanto, el establecimiento las condiciones de ejercicio del mismo.

Por parte del órgano de administración y de conformidad con el art.308 de la Ley de Sociedades de Capital se hace constar:

I. Que los administradores han elaborado un informe detallado del valor de las participaciones, así como de la contraprestación a pagar por las nuevas y la indicación de las personas a las que hayan de atribuirse.
II. Que en la convocatoria de la junta se indicó la supresión del derecho de suscripción preferente, el tipo de creación de las nuevas participaciones sociales y el derecho de los socios a examinar en el domicilio social el informe de los administradores, así como pedir la entrega o el envío gratuito de estos documentos.
III. Que el valor nominal de las nuevas participaciones, se corresponde con el valor real atribuido a las participaciones en el informe de los administradores.
[ELEGIR UNA OPCIÓN: Con aportaciones dinerarias / Con aportaciones no dinerarias y mixtas / Por compensación de créditos / Por transformación de reservas y beneficios]

Segundo. Modificación de Estatutos

Se acuerda por unanimidad modificar el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo queda redactado de la siguiente forma:

"Art [Nº DE ARTÍCULO] - El capital de la sociedad es de [IMPORTE] euros y está representado por [ÓRGANO O PERSONA] participaciones, de valor nominal [IMPORTE] euros cada una de ellas, numeradas correlativamente del 1 al [Nº], ambos inclusive. Todas las participaciones confieren los mismos derechos y obligaciones y están totalmente desembolsadas en el 100% de su valor nominal’.

Tercero.- Elevación a Público

Se faculta al Secretario del Consejo de Administración para que pueda comparecer ante Notario y elevar a público los presentes acuerdos, otorgando para ello las escrituras correspondientes, incluidas, en su caso, las de subsanación, aclaración o rectificación, así como para realizar cuantas operaciones fueren precisas para la plena eficacia de dichos acuerdos.

- Que el acta fue aprobada por la propia Junta, así como firmada por el Secretario con el Visto Bueno del Presidente, todo ello al término de la reunión.

Y, para que conste y surta los oportunos efectos, se expide la presente certificación- con el Visto Bueno del Presidente D./Dña. [NOMBRE Y APELLIDOS]

En [LUGAR], a [FECHA].

Secretario

Vº Bº Presidente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

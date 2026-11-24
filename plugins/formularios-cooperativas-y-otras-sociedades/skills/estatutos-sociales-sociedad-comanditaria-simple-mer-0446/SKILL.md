---
name: estatutos-sociales-sociedad-comanditaria-simple-mer-0446
description: "Estatutos sociales de una sociedad comanditaria simple. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Estatutos sociales de una sociedad comanditaria simple

> Formulario **MER-0446** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Estatutos sociales de una sociedad comanditaria simple» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Estatutos sociales de una sociedad comanditaria simple” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:estatutos-sociales-sociedad-comanditaria-simple-mer-0446`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] IMPORTE (5 veces)
- [ ] Nº (5 veces)
- [ ] NOMBRE DE LOS SOCIOS (3 veces)
- [ ] DESCRIPCIÓN DEL BIEN (2 veces)
- [ ] CALLE
- [ ] DIRECCIÓN
- [ ] NÚMERO
- [ ] OBJETO SOCIAL
- [ ] PISO

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

Artículo 1º.- Constitución.
- Denominación.
- Duración.
- Domicilio.
- Objeto social.
- Capital social.
- Socio gestor.
- Cantidades que se asignan al socio gestor anualmente para sus gastos particulares.
- Asamblea de socios.
- Adopción de los acuerdos sociales.
- Participación en las ganancias.
- Participación en las pérdidas.
- Modificaciones estatutarias.
- Disolución.

Modelo para la creación de estatutos sociales de una Sociedad Comanditaria Simple, en los que se concretan las bases de organización y funcionamiento de la sociedad, tales como la duración, domicilio, objeto y capital social, socio gestor, participación de los socios y disolución de la misma.

Artículo 1º.- Constitución.

Como socios colectivos:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

Como socios comanditarios:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

constituyen una Sociedad Comanditaria Simple que se regirá por su correspondiente contrato constitutivo, por los presentes estatutos, y en lo en ellos no dispuesto, por el Código de Comercio, así como por cuantas disposiciones resulten de aplicación.

Artículo 2º. - Denominación.

La Sociedad se denomina ‘ [NOMBRE DE LOS SOCIOS], [NOMBRE DE LOS SOCIOS] y [NOMBRE DE LOS SOCIOS], S.Com.

Artículo 3º. - Duración.

La Sociedad tendrá una duración de carácter indefinido, dándose comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de la presente escritura, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Sociedad en momentos anteriores al de su inscripción en el Registro Mercantil.

Los ejercicios sociales se computarán por años naturales.

Artículo 4º. - Domicilio.

El domicilio de la Sociedad se halla situado en [DIRECCIÓN], calle [CALLE] número [NÚMERO] piso [PISO]

Artículo 5º. - Objeto social.

El objeto social de la Sociedad será [OBJETO SOCIAL].

Artículo 6º. - Capital social.

El capital social se cifra en [IMPORTE] euros, importe que ha sido íntegramente suscrito y desembolsado por los socios en el acto de otorgamiento de la escritura de constitución de la Sociedad, con arreglo a las siguientes aportaciones:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], socio colectivo, aporta [DESCRIPCIÓN DEL BIEN].

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], socio comanditario, aporta, en efectivo metálico, la suma de [IMPORTE] euros [IMPORTE] euros.

[OPCIONAL — incluir si procede]

(En caso de aportaciones no dinerarias)
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] socios [ELEGIR: colectivo / comanditario] aporta, con el consentimiento de su cónyuge [DESCRIPCIÓN DEL BIEN] valorado en [IMPORTE] euros

Todas las aportaciones se realizan a título de propiedad.

Artículo 7º. - Socio gestor.

La administración y representación de la Sociedad se encomienda a un socio gestor, quien tendrá el uso de la firma social. Y será D./Dña. [NOMBRE Y APELLIDOS].

El gestor representará a la sociedad en cuantos aspectos sean referentes a su giro o tráfico, tanto judicial como extrajudicialmente.

Se procede a nombrar, en este mismo acto, a D./Dña. [NOMBRE Y APELLIDOS] como socio gestor de la Sociedad, quien acepta, y manifiesta no hallarse incurso en ninguna de las causas que inhabilitan para el ejercicio de dicho cargo.

Artículo 8º. - Cantidades que se asignan al socio gestor anualmente para sus gastos particulares.

Se acuerda asignar a cada socio gestor, en concepto de gastos de representación y gestión debidamente justificados, la cantidad anual de [IMPORTE] euros, revisables cada [Nº] años según

Artículo 9º. - Asamblea de socios.

Cualquiera de los socios podrá pedir la reunión de la Asamblea de los socios. solicitándolo al socio gestor con al menos [Nº] días de antelación, y señalando la hora y día de su celebración y los asuntos a tratar en la misma.

El socio gestor debe realizar la convocatoria de los socios mediante citación por escrito entregada personalmente a los mismos o enviada a sus respectivos domicilios por correo certificado con al menos [Nº] días de antelación a la fecha de la celebración de la reunión.

Artículo 10º. - Adopción de los acuerdos sociales.

Cada socio tiene derecho a un voto.

Los acuerdos sociales se adoptarán por mayoría de los socios presentes en la reunión, debidamente convocada, siempre que al menos conste el voto a favor de [Nº] socios, al menos [Nº] de los cuales deberán ser socios colectivos.

Se exceptúan de lo anterior los casos en los que por disposición normativa o estatutaria se exija unanimidad

Artículo 11º. - Participación en las ganancias.

Los socios participarán en las ganancias sociales de acuerdo a los siguientes porcentajes:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] participará en un %.

Artículo 12º. - Participación en las pérdidas.

Los socios participarán en las pérdidas de acuerdo a los mismos porcentajes previstos en el artículo anterior para su participación en las ganancias

No obstante, lo anterior, los socios comanditarios no responderán de las pérdidas más allá del límites de las aportaciones realizadas al capital social.

Artículo 13º. -

Ningún socio podrá enajenar, gravar ni ceder su participación en la sociedad sin el consentimiento de todos los demás.

En caso de fallecimiento de alguno de los socios colectivos, podrá pactarse la continuidad de la sociedad con los herederos del fallecido, siempre que medie acuerdo unánime al respecto de los socios supervivientes. De no producirse dicho acuerdo, la sociedad continuará entre dichos socios sobrevivientes, rescindiéndose parcialmente en cuanto al socio fallecido.

En caso de fallecimiento de alguno de los socios comanditarios, podrá pactarse la continuidad de la sociedad con los herederos del fallecido, siempre que medie acuerdo de los socios adoptado con la mayoría prevista en el artículo 10º de los presentes estatutos. Si no se produjere este acuerdo, la sociedad continuará entre los socios sobrevivientes, rescindiéndose parcialmente en cuanto al socio fallecido.

Artículo 14º. - Modificaciones estatutarias.

Cualquier modificación estatutaria o del contrato constitutivo requerirá acuerdo unánime de los socios.

Igualmente se precisará unanimidad de los socios para la adopción de los acuerdos de transformación, fusión o escisión de la sociedad.

Artículo 15º. - Disolución.

La sociedad se disolverá por las causas establecidas en el Código de Comercio para las sociedades comanditarias simples, y se procederá a su liquidación de conformidad con las reglas contenidas en dicho Cuerpo Legal.

El activo resultante después de satisfacer los créditos que existan contra la sociedad se repartirá entre los socios en la proporción que tiene atribuida cada uno de ellos como de participación en las ganancias. En esa misma proporción sufrirán las eventuales pérdidas, quedando siempre a salvo lo dispuesto en el Artículo 12º de los presentes estatutos respecto del límite de imputación de la responsabilidad por pérdidas de los socios comanditarios.

Los supuestos de separación y exclusión de los socios se rigen asimismo por las reglas previstas en el Código de Comercio.

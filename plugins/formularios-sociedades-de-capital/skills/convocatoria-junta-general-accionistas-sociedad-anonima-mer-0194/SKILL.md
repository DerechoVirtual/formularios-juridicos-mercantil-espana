---
name: convocatoria-junta-general-accionistas-sociedad-anonima-mer-0194
description: "Convocatoria de junta general de accionistas de una sociedad anónima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Convocatoria de junta general de accionistas de una sociedad anónima

> Formulario **MER-0194** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Escrito de convocatoria de Junta General Ordinaria o Extraordinaria de accionistas presencial o telemática (en remoto), en el que se establece el orden del día: designación de Presidente y Secretario de la Junta, aprobación o censura de cuentas anuales [EJERCICIO], aprobación o censura de la gestión social o modificación de los estatutos sociales.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Convocatoria de junta general de accionistas de una sociedad anónima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Convocatoria de junta general de accionistas de una sociedad anónima” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:convocatoria-junta-general-accionistas-sociedad-anonima-mer-0194`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] MES (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] ENTIDAD ENCARGADA DEL REGISTRO CONTABLE
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR

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

Escrito de convocatoria de Junta General Ordinaria o Extraordinaria de accionistas presencial o telemática (en remoto), en el que se establece el orden del día: designación de Presidente y Secretario de la Junta, aprobación o censura de cuentas anuales [EJERCICIO], aprobación o censura de la gestión social o modificación de los estatutos sociales.


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

CONVOCATORIA DE JUNTA GENERAL DE ACCIONISTAS

[ELEGIR UNA OPCIÓN: Encabezamiento / I. ENCABEZAMIENTO / Junta General Extraordinaria / Junta General Ordinaria / — y además elegir: Orden del día / II. ORDEN DEL DÍA / Junta General Extraordinaria / Junta General Ordinaria]

III. DERECHO A LA INCLUSIÓN DE ASUNTOS EN EL ORDEN DEL DÍA

Los accionistas que representen, al menos, el cinco por ciento del capital social, podrán solicitar que se publique un complemento a la convocatoria de la Junta General de Accionistas incluyendo uno o más puntos en el Orden del Día. El ejercicio de este derecho deberá hacerse mediante notificación fehaciente que habrá de recibirse en el domicilio social dentro de los cinco días siguientes a la publicación de la presente convocatoria.

En el escrito de notificación se hará constar el nombre o denominación social del accionista o accionistas solicitantes, y se acompañará la oportuna documentación -copia de la tarjeta de asistencia o certificado de legitimación- que acredite su condición de accionistas.

El complemento de la convocatoria se publicará con quince días de antelación, como mínimo, a la fecha señalada para la celebración de la Junta en primera convocatoria.

IV. DERECHO DE INFORMACIÓN

Se hace constar el derecho de los accionistas a solicitar por escrito los informes y aclaraciones que estimen precisos sobre los asuntos comprendidos en el Orden del Día.

V. DERECHO DE ASISTENCIA

Podrán asistir a la Junta General y tomar parte en sus deliberaciones, con derecho a voz y voto, el accionista que con cinco días de antelación a aquél en que haya de celebrarse la Junta tenga inscrita la titularidad de acciones a su nombre en el correspondiente registro de anotaciones en cuenta, debiendo acreditar esta circunstancia por medio de la oportuna tarjeta de asistencia, certificado de legitimación expedido por la entidad o entidades encargadas de la llevanza del registro de anotaciones en cuenta, o en cualquier otra forma admitida por la legislación vigente.

A los efectos de acreditar la identidad de los accionistas, o de quien válidamente les represente, a la entrada del local donde se celebre la Junta General se podrá solicitar a los asistentes, junto a la presentación de la tarjeta de asistencia, la acreditación de su identidad mediante la presentación del Documento Nacional de Identidad o de cualquier otro documento oficial generalmente aceptado a estos efectos.

[ELEGIR UNA OPCIÓN: Derecho de representación / VI. DERECHO DE REPRESENTACIÓN / Mediante correspondencia postal / Mediante comunicación electrónica / — y además elegir: Emisión de voto / VII. EMISIÓN DE VOTO / Mediante correspondencia postal / POR MEDIO DE COMUNICACIÓN A DISTANCIA / Mediante comunicación electrónica / POR MEDIO DE COMUNICACIÓN ELECTRÓNICA]

VIII. DISPOSICIONES COMUNES A LA DELEGACIÓN Y AL VOTO A DISTANCIA

1.-REGLAS DE PREFERENCIA

Prioridades entre representación, voto a distancia y asistencia física

La asistencia personal a la Junta del accionista que hubiera otorgado su representación a un tercero o votado a distancia previamente, sea cual fuere el medio utilizado para su emisión, dejará sin efecto dicha representación o voto.

Asimismo, el voto a distancia, sea cual fuere el medio utilizado para su emisión, hará ineficaz cualquier representación electrónica o mediante tarjeta impresa en papel, ya sea anterior, que se tendrá por revocada, o posterior, que se tendrá por no efectuada.

Prioridades entre representaciones

En el caso de que un accionista confiera válidamente varias representaciones, prevalecerá la última recibida por la Sociedad, con independencia de cuál sea el medio por el que se ha concedido.

Prioridades entre votos a distancia

El accionista podrá votar válidamente a distancia una sola vez en relación con cada posición de valores. En el caso de que un accionista efectúe varios votos a distancia respecto de las mismas acciones, sea por vía electrónica o mediante correo postal, prevalecerá el voto que primero haya sido recibido por la Sociedad, quedando invalidados los recibidos en fecha posterior.

2.-OTRAS PREVISIONES

Tanto la representación como el voto emitido a distancia quedarán sin efecto por la enajenación de las acciones que confieren el derecho de asistencia de que tenga conocimiento la Sociedad.

El accionista que confiera su representación mediante correspondencia postal o comunicación electrónica y no hiciera constar marca en alguna o ninguna de las casillas destinadas a dar instrucciones de voto respecto de los puntos del Orden del Día, se entenderá que desea votar a favor de las respectivas propuestas formuladas por el Consejo de Administración.

De la misma forma, el accionista que emita su voto mediante correspondencia postal o comunicación electrónica y no hiciera constar marca en alguna o ninguna de las casillas destinadas a señalar el voto respecto de los puntos del Orden del Día, se entenderá que desea votar a favor de las respectivas propuestas formuladas por el Consejo de Administración.

Asimismo, la validez de la representación conferida y del voto emitido mediante

comunicación a distancia está sujeta a la comprobación de la condición de accionista. En caso de divergencia entre el número de acciones comunicado por el accionista que confiere la representación o emite su voto mediante comunicación a distancia y el que conste en los registros de anotaciones en cuenta que comunique [ENTIDAD ENCARGADA DEL REGISTRO CONTABLE], se considerará válido, a efectos de quórum y votación, y salvo prueba en contrario, el número de acciones facilitado por esta última entidad.

Es responsabilidad exclusiva del accionista la custodia de su firma electrónica para votar o conferir la representación de forma electrónica.

La Sociedad se reserva el derecho a modificar, suspender, cancelar o restringir los mecanismos de voto y representación electrónicos cuando razones técnicas o de seguridad así lo demanden.

La Sociedad no será responsable de los perjuicios que pudieran ocasionarse al accionista derivados de averías, sobrecargas, caídas de líneas, fallos en la conexión, mal funcionamiento del servicio de correos o cualquier otra eventualidad de igual o similar índole, ajenas a la voluntad de la Sociedad, que impidan la utilización de los mecanismos de voto y representación a distancia.

3.-INICIO

Tanto la representación como el voto emitido a distancia se podrán realizar por medios electrónicos de comunicación a distancia, a través de la página web de la Sociedad a partir del día [FECHA] de [MES] de

IX. INTERVENCIÓN DE NOTARIO EN LA JUNTA

De conformidad con lo establecido en el artículo 203 de la Ley de Sociedades de Capital, el Consejo de Administración requerirá la presencia de un Notario del Ilustre Colegio Notarial de [LOCALIDAD], para que levante Acta de la Junta.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo. El Secretario del Consejo de Administración

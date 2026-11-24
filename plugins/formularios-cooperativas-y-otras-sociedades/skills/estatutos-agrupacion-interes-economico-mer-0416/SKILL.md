---
name: estatutos-agrupacion-interes-economico-mer-0416
description: "Estatutos de una agrupación de interés económico. Lo redacta con los datos del caso y comprueba las normas con Jurisprudenciator."
---

# Estatutos de una agrupación de interés económico

> Formulario **MER-0416** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de estatutos de una Agrupación de Interés Económico (A.I.E.), sociedad mercantil que tiene por objeto una actividad económica auxiliar de la desarrollada por sus socios (empresarios, agricultores, artesanos, profesionales liberales y entidades no lucrativas de investigación), regulada por la Ley 12/1991, de 29 de abril, de Agrupaciones de Interés Económico.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Estatutos de una agrupación de interés económico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Estatutos de una agrupación de interés económico” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:estatutos-agrupacion-interes-economico-mer-0416`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- `formulario.md`: el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `marco.md`: la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD O TERRITORIO (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] Nº
- [ ] NÚMERO MÁXIMO
- [ ] NÚMERO MÍNIMO
- [ ] PORCENTAJE

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

---

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…sona jurídica de derecho privado no comerciante; o por una medida de incapacidad»: sustituir la referencia a «incapacidad» por la situación de persona con discapacidad con medidas de apoyo judiciales que proceda conforme a la Ley 8/2021
- Junto a «…ncargada del control de cuentas, que será ejercido por un interventor de cuentas»: comprobar si la Agrupación está obligada a auditoría conforme a la Ley 22/2015, de Auditoría de Cuentas, y, en su caso, nombrar auditor de cuentas

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE AYUDA

La Agrupación de Interés Económico es una sociedad mercantil que tiene por objeto una actividad económica auxiliar a la desarrollada por sus socios, personas físicas o jurídicas que realizan actividades empresariales, agrícolas o artesanales, entidades no lucrativas dedicadas a la investigación y quienes ejerzan profesiones liberales.

La normativa sustantiva que regula la A.I.E. es: a) la Ley 12/1991, de Agrupaciones de Interés Económico; b) el Reglamento (CEE) 2137/85 del Consejo, regulador de las Agrupaciones Europeas de Interés Económico; y c) los artículos 264 a 269 del Reglamento del Registro Mercantil. Con carácter supletorio se rigen por las normas de la sociedad colectiva compatibles con la naturaleza específica de la A.I.E., es decir, el Reglamento del Registro Mercantil (denominación, publicidad, etc.), el texto refundido de la Ley de Sociedades de Capital (administradores) y el Código de Comercio (sociedades colectivas).

Sobre la personalidad, en relación con la reclamación de obligaciones nacidas de contratos suscritos por sociedades posteriormente agrupadas para el cumplimiento de sus fines, véase la sentencia del Tribunal Supremo (Sala de lo Civil, Sección 1ª) núm. 162/2007, de 8 de febrero. Respecto de la excepción de falta de litisconsorcio pasivo necesario, no concurren los presupuestos para su apreciación al no existir razón jurídico-material para que la demanda se dirigiera al tiempo contra una entidad que era ajena por completo al conflicto y a la relación contractual, y que en consecuencia no debía ser afectada en su patrimonio por el contenido del fallo. Cuando la parte recurrente defiende que la A.I.E. debía haber sido demandada porque considera que a la fecha de la demanda era el único deudor, basa su argumento en la supuesta subrogación o sucesión universal y automática de la nueva persona jurídica en el conjunto de relaciones jurídicas de que eran titulares sus miembros al tiempo de la constitución; pero esta sucesión no solo carece de cobertura legal, al no establecerla la Ley 12/1991, sino que, en lo referente a su vertiente pasiva, esto es, a las deudas, ni siquiera admite una aplicación analógica de la figura de la asunción de deudas para presentar a la A.I.E. como único sujeto pasivo obligado, con correlativa liberación de los deudores anteriores, dado que, en primer lugar, es condición indispensable para la eficacia de la misma el cambio subjetivo en la persona del deudor (cambio que no se ha producido porque, tras constituirse la A.I.E., continuaron siendo deudores frente a la parte actora quienes originariamente suscribieron el contrato origen de la deuda, al no existir pacto al respecto ni norma imperativa que operara dicha modificación y porque mantuvieron su personalidad jurídica pese al nacimiento de la Agrupación) y, en segundo lugar, porque, aun de haberse producido ese cambio subjetivo, no habría resultado suficiente para ser oponible frente al acreedor, al ser necesario también el consentimiento expreso o tácito del acreedor (no basta su conocimiento). Conviene recordar, con relación a los presupuestos de eficacia de la asunción de deudas, la doctrina de la sentencia del Tribunal Supremo de 20 de mayo de 1997, que cita otras muchas: la sustitución de la persona del deudor en las relaciones contractuales o asunción de deuda, tanto en la modalidad del convenio entre los deudores como en la de expromisión (convenio entre el acreedor y el nuevo deudor que libere al primitivo), exige en todo caso para su eficacia, no el conocimiento, sino el consentimiento expreso o tácito del acreedor, conforme al artículo 1205 del Código Civil, sin cuya concurrencia no puede producirse la liberación del primitivo deudor. La novación nunca se presume ni puede inferirse de meras deducciones o conjeturas, sino que la voluntad de novar debe constar siempre de modo inequívoco, bien por manifestarse con claridad de forma expresa, bien por inducirse de actos de significación concluyente, sin que de ningún modo sea suficiente el simple conocimiento de la sustitución (sentencias del Tribunal Supremo de 10 de mayo de 1979, 23 de mayo de 1980, 16 de febrero de 1983, 28 de marzo de 1985, 10 de julio de 1986 y 17 de febrero de 1987).

Sobre el régimen de responsabilidad, en relación con la responsabilidad del socio por deudas de la agrupación (pagarés emitidos tras su baja pero antes de la inscripción y la publicación de la misma en el Boletín Oficial del Registro Mercantil), la sentencia del Tribunal Supremo (Sala de lo Civil, Sección 1ª) núm. 424/2006, de 4 de mayo, establece, en relación con una cláusula estatutaria según la cual «los socios responderán personal, solidaria e ilimitadamente de las deudas de cualquier clase contraídas por la Agrupación, en la proporción que corresponda por su participación», que la interpretación de la recurrente (responder solo en el porcentaje de su participación) es insostenible: primero, porque entonces carecería de sentido la solidaridad que inequívocamente establece el propio artículo de los estatutos; y segundo, porque la referencia proporcional a la participación de cada socio tiene que entenderse hecha a la relación interna entre estos, para el caso de que uno o varios acabasen pagando la deuda por entero y formularan contra los demás la reclamación que contempla el párrafo segundo del art. 1145 del Código Civil, teniendo pleno sentido la precisión estatutaria a la vista de lo que sobre distribución de pérdidas y ganancias establece el art. 21 de la Ley 12/1991 (reparto en la proporción prevista en la escritura o, en su defecto, por partes iguales), así como la jurisprudencia que, distinguiendo en la obligación solidaria las relaciones externas con el acreedor de las relaciones internas entre codeudores, combina el párrafo segundo del art. 1145 con el art. 1138 del Código Civil para presumir que la deuda se divide entre los deudores por partes iguales salvo que resulte claramente otra cosa (SSTS de 26 de octubre de 2002, 11 de marzo de 2002, 16 de julio de 2001 y 4 de enero de 1999, entre otras). Dicha proporción es aplicable solo a las relaciones internas entre los socios, no oponible al acreedor, y es plenamente compatible con el régimen de responsabilidad establecido en el art. 5 de la Ley 12/1991.

En cuanto al capital social, puede constituirse una A.I.E. sin capital social, pero se trata de una posibilidad improbable puesto que siempre existen gastos de notaría, registro, impuestos, etc., en el acto constitutivo que implican la existencia de un capital social necesario. No obstante, cabe la posibilidad de que los socios realicen aportaciones a la agrupación a fin de dotarla de fondos suficientes, sin que tales entregas tengan la consideración de capital social, o bien que sea la propia A.I.E. quien solicite un crédito para obtener un capital social garantizado con la responsabilidad de los socios o la prestación de una fianza por los mismos.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee `formulario.md` entero y la parte de `marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

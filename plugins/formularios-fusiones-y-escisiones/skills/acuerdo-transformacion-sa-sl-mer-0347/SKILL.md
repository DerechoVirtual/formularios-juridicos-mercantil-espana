---
name: acuerdo-transformacion-sa-sl-mer-0347
description: "Acuerdo de transformación de una SA en SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acuerdo de transformación de una SA en SL

> Formulario **MER-0347** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Modelo de acta de Junta General (Extraordinaria convocada o Universal) de Socios de una Sociedad Anónima en la que se acuerda su transformación en sociedad de Responsabilidad Limitada con expresión de la aprobación del balance de la sociedad presentado para la transformación, con las modificaciones que en su caso resulten procedentes, así como de las menciones exigidas para la constitución de la sociedad cuyo tipo se adopte.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acuerdo de transformación de una SA en SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acuerdo de transformación de una SA en SL” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:acuerdo-transformacion-sa-sl-mer-0347`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (4 veces)
- [ ] OTROS DATOS (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] FECHA

## Normas que cita el formulario

- art. 24 Real Decreto-ley 5/2023

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

Modelo de acta de Junta General (Extraordinaria convocada o Universal) de Socios de una Sociedad Anónima en la que se acuerda su transformación en sociedad de Responsabilidad Limitada con expresión de la aprobación del balance de la sociedad presentado para la transformación, con las modificaciones que en su caso resulten procedentes, así como de las menciones exigidas para la constitución de la sociedad cuyo tipo se adopte.


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

ACUERDO DE TRANSFORMACIÓN DE «[DENOMINACIÓN SOCIAL], SA» EN SOCIEDAD DE RESPONSABILIDAD LIMITADA

[ELEGIR UNA OPCIÓN: Junta General Extraordinaria / Junta universal]

ACUERDOS

Primero.- Transformación

Se acuerda por [ELEGIR: unanimidad / mayoría] transformar la sociedad « [DENOMINACIÓN SOCIAL], SA», con efectos a partir del día [FECHA] en una sociedad de responsabilidad limitada, con la denominación de « [DENOMINACIÓN SOCIAL], SL».

Las circunstancias y condiciones que rigen el proceso de transformación son las siguientes:

1) La sociedad resultante « [DENOMINACIÓN SOCIAL], SL» mantiene la personalidad jurídica así como su patrimonio y los derechos y obligaciones que correspondían a la sociedad anónima de la que trae causa el proceso de transformación.

2) Debido a que la sociedad anónima que se transforma cuenta con un patrimonio que además de cubrir el capital social está totalmente desembolsado, se acuerda que la sociedad de responsabilidad limitada resultante del proceso tendrá un capital social de [IMPORTE] euros, distribuido en [Nº] participaciones sociales de [IMPORTE] euros de valor nominal cada una, numeradas correlativamente del número 1 al

3) La participación social de los socios no se modifica por el presente acuerdo de transformación. Por lo que, las participaciones sociales de la sociedad de responsabilidad limitada resultante (totalmente suscritas y desembolsadas), se adjudican a los socios en la misma proporción que la que tenían en el capital social de la sociedad anónima transformada, esto es:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

A D./Dña. [NOMBRE Y APELLIDOS], se le adjudican las participaciones números [Nº] al [Nº]

4) Los títulos y resguardos provisionales representativos de las acciones quedan anulados e inutilizados.

5) Conforme al artículo 24 del Real Decreto-ley 5/2023, los socios y los titulares de acciones sin voto que no hayan votado a favor del acuerdo tienen derecho enajenar sus acciones a la sociedad o a los socios o terceros que esta proponga a cambio de una compensación en efectivo adecuada.

6) La sociedad [DENOMINACIÓN SOCIAL] SA que se transforma no tiene obligacionistas ni titulares de derechos especiales distintos de las acciones.

7) Se deja constancia del cumplimiento de la obligación de información a los socios.

Segundo.- Balances

[ELEGIR UNA OPCIÓN: Ad hoc / Último balance anual]

Tercero.- Estatutos

Los estatutos de la sociedad de responsabilidad limitada resultante, son aprobados por [ELEGIR: unanimidad / mayoría] y unidos a la escritura pública de transformación. Un ejemplar de los mismos se adjunta como anexo número 2.

Cuarto.- Administradores

[ELEGIR UNA OPCIÓN: Cese / Mantenimiento]

Quinto.- Elevación a Público

Por unanimidad se acuerda facultar expresamente al administrador de la sociedad D./Dña. [NOMBRE Y APELLIDOS], para que, en nombre y representación de la misma, comparezca ante Notario de su elección con objeto de elevar a público los acuerdos y hacer las gestiones precisas tanto para su inscripción en el Registro Mercantil, como para [OTROS DATOS], en su caso, subsanar, corregir o aclarar cualquier error u omisión que pudiera advertirse.

En particular, D./Dña. [NOMBRE Y APELLIDOS], administrador de la sociedad, deberá proceder a la publicación del acuerdo de transformación o, en su caso, a la publicidad sustitutiva prevista en la regulación vigente.

Sexto.- Acta

Una vez tratados los puntos del orden del día de carácter sustantivo, se confecciona el acta que, una vez leída, es aprobada inmediatamente por unanimidad, y firmada por el secretario de la junta con el visto bueno del presidente [OTROS DATOS].

Tras lo cual, se levanta la sesión a las [Nº] horas del día y en el lugar que figuran en el encabezamiento.

Secretario D./Dña. [NOMBRE Y APELLIDOS], [OTROS DATOS]

VºBº Presidente D./Dña. [NOMBRE Y APELLIDOS],

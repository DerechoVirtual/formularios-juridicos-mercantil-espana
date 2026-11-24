---
name: acta-junta-sl-acuerda-exclusion-socio-mer-0072
description: "Acta de junta de SL que acuerda la exclusión de un socio. Lo redacta con los datos del caso y comprueba las normas con Jurisprudenciator."
---

# Acta de junta de SL que acuerda la exclusión de un socio

> Formulario **MER-0072** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Acta de Junta General de una Sociedad Limitada (extraordinaria convocada o universal) en la que se acuerda la exclusión de un socio (arts. 350 y ss. de la Ley de Sociedades de Capital), fijando el procedimiento de valoración y reembolso de sus participaciones. Si el socio excluido tiene el 25 % o más del capital y no se conforma, además del acuerdo se necesita resolución judicial firme.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acta de junta de SL que acuerda la exclusión de un socio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acta de junta de SL que acuerda la exclusión de un socio” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:acta-junta-sl-acuerda-exclusion-socio-mer-0072`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- `formulario.md`: el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `marco.md`: la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (20 veces)
- [ ] AÑO (11 veces)
- [ ] DÍA (11 veces)
- [ ] MES (11 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] PORCENTAJE (7 veces)
- [ ] DOMICILIO (5 veces)
- [ ] HORA (5 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] NOMBRE Y APELLIDOS DEL SOCIO EXCLUIDO (4 veces)
- [ ] Nº DE ARTÍCULO (4 veces)
- [ ] FIRMA - NOMBRE Y APELLIDOS (3 veces)
- [ ] NOMBRE Y APELLIDOS DEL SOCIO (3 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOCUMENTO ACREDITATIVO DE LA REPRESENTACIÓN (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL NUEVO ADMINISTRADOR (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL SOCIO REPRESENTADO (2 veces)
- [ ] OTROS ASUNTOS, EN SU CASO (2 veces)
- [ ] CALLE Y NÚMERO
- [ ] CAUSAS DE LA EXCLUSIÓN
- [ ] ESTADO CIVIL
- [ ] INDICAR VOTOS EN CONTRA, ABSTENCIONES Y SOCIOS QUE HAN VOTADO A FAVOR
- [ ] MANIFESTACIONES DEL SOCIO AFECTADO
- [ ] NACIONALIDAD
- [ ] NIF
- [ ] NOMBRE DEL DIARIO
- [ ] NOMBRE Y APELLIDOS DEL ADMINISTRADOR CESADO
- [ ] NOMBRE Y APELLIDOS DEL PRESIDENTE
- [ ] NOMBRE Y APELLIDOS DEL SECRETARIO/A
- [ ] PLAZO
- [ ] PROCEDIMIENTO DE VALORACIÓN Y REEMBOLSO

## Normas que cita el formulario

- art. 196 Real Decreto Legislativo 1/2010
- art. 350 Real Decreto Legislativo 1/2010
- art. 190 LSC
- art. 353 Real Decreto Legislativo 1/2010

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE AYUDA

0. Aspectos generales. La sociedad de responsabilidad limitada podrá excluir al socio que incumpla voluntariamente la obligación de realizar prestaciones accesorias, así como al socio administrador que infrinja la prohibición de competencia o hubiera sido condenado por sentencia firme a indemnizar a la sociedad los daños y perjuicios causados por actos contrarios a la ley o a los estatutos o realizados sin la debida diligencia. En las sociedades de capital, con el consentimiento de todos los socios, podrán incorporarse a los estatutos causas determinadas de exclusión o modificarse o suprimirse las que figurasen en ellos con anterioridad.

La exclusión requerirá acuerdo de la junta general. En el acta de la reunión o en anejo se hará constar la identidad de los socios que hayan votado a favor del acuerdo.

Salvo en el caso de condena del socio administrador a indemnizar a la sociedad, la exclusión de un socio con participación igual o superior al veinticinco por ciento en el capital social requerirá, además del acuerdo de la junta general, resolución judicial firme, siempre que el socio no se conforme con la exclusión acordada.

Cualquier socio que hubiera votado a favor del acuerdo estará legitimado para ejercitar la acción de exclusión en nombre de la sociedad cuando ésta no lo hubiera hecho en el plazo de un mes a contar desde la fecha de adopción del acuerdo de exclusión.

2. Lista de asistentes. Según el artículo 98 del Reglamento del Registro Mercantil (RRM), la lista de asistentes figurará al comienzo de la propia acta o se adjuntará a ella por medio de anejo firmado por el Secretario, con el Visto Bueno del Presidente. Igualmente, la lista de asistentes podrá formarse mediante fichero o incorporarse a soporte informático; en estos casos se extenderá en la cubierta precintada del fichero o del soporte la oportuna diligencia de identificación firmada por el Secretario, con el Visto Bueno del Presidente.

3. Presidencia de la Junta. Según el artículo 191 de la Ley de Sociedades de Capital (LSC), la junta general será presidida por la persona que designen los estatutos; en su defecto, por el presidente del Consejo de Administración, y a falta de éste, por el socio que elijan en cada caso los socios asistentes a la reunión. El presidente estará asistido por un secretario, designado también por los estatutos o por los socios asistentes a la junta.

4. Facultad de certificar. El art. 109 RRM indica que la facultad de certificar corresponde, estando el cargo vigente e inscrito: a) si hay Consejo, al Secretario (o Vicesecretario) del Consejo, sea o no administrador, con el Visto Bueno del Presidente (o, en su caso, Vicepresidente); b) si no hay Consejo, al Administrador único, a cualquiera de los solidarios o a los mancomunados que tengan poder de representación; c) en caso de sociedad en liquidación, se aplican a los liquidadores las mismas reglas que para los administradores; d) en caso de socio único, puede certificar el socio o el/los administrador/es nombrados, aplicando las reglas anteriores. En el supuesto de cargo vigente no inscrito, el sistema actual exige la notificación fehaciente del nombramiento al anterior titular, con cargo inscrito, en el domicilio que conste en el Registro, o que se acredite el consentimiento del anterior titular, compareciendo en la escritura o con su firma legitimada notarialmente en la misma certificación o en documento separado (art. 111 RRM).

5. Aprobación del acta de la Junta. Según el artículo 202 LSC, el acta de la junta podrá ser aprobada por la propia junta a continuación de haberse celebrado ésta y, en su defecto, y dentro del plazo de quince días, por el presidente y dos interventores, uno en representación de la mayoría y otro por la minoría. El acta aprobada en cualquiera de estas dos formas tendrá fuerza ejecutiva a partir de la fecha de su aprobación.


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

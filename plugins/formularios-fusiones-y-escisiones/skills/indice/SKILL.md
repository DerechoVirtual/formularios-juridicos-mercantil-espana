---
name: indice
description: "Índice de los 55 formularios de Fusiones, escisiones y transformaciones de sociedades. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Fusiones, escisiones y transformaciones de sociedades: índice de formularios

> Plugin `formularios-fusiones-y-escisiones` · 55 formularios · normativa revisada el 25-11-2026.

## Qué es

Para las modificaciones estructurales del Real Decreto-ley 5/2023: proyectos comunes de fusión y escisión, acuerdos de junta, anuncios, informes a socios y trabajadores, escrituras de fusión, escisión, transformación y cesión global, y la defensa de acreedores y socios.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Proyecto común de fusión por absorción de una SL íntegramente participada»
- «Escritura de escisión parcial con creación de nueva sociedad»
- «Acuerdo de transformación de una SL en SA»

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

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-fusiones-y-escisiones:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Contratos, pactos y cláusulas (13)

| Código | Formulario | Skill |
|---|---|---|
| MER-0313 | Acuerdo de transformación de SL en SA con patrimonio dinerario y no dinerario | `acuerdo-transformacion-sl-sa-patrimonio-dinerario-no-mer-0313` |
| MER-0315 | Acuerdo unánime de escisión parcial de una SL con creación de nueva SL con la parte escindida | `acuerdo-unanime-escision-parcial-sl-creacion-nueva-sl-mer-0315` |
| MER-0322 | Acuerdo de junta de la sociedad beneficiaria que aprueba la escisión | `acuerdo-junta-sociedad-beneficiaria-aprueba-escision-mer-0322` |
| MER-0324 | Acuerdo de escisión parcial de SL con nueva SL beneficiaria y aprobación del proyecto | `acuerdo-escision-parcial-sl-nueva-sl-beneficiaria-mer-0324` |
| MER-0326 | Acuerdo del consejo de administración que aprueba el proyecto de escisión | `acuerdo-consejo-administracion-aprueba-proyecto-mer-0326` |
| MER-0329 | Acuerdo de junta de la sociedad escindida que aprueba la escisión total o parcial | `acuerdo-junta-sociedad-escindida-aprueba-escision-mer-0329` |
| MER-0331 | Acuerdo del consejo de administración que aprueba el proyecto de fusión por absorción | `acuerdo-consejo-administracion-aprueba-proyecto-fusion-mer-0331` |
| MER-0341 | Acuerdo de junta de la sociedad absorbente que aprueba la fusión | `acuerdo-junta-sociedad-absorbente-aprueba-fusion-mer-0341` |
| MER-0342 | Acuerdo de junta de la sociedad absorbida que aprueba la fusión | `acuerdo-junta-sociedad-absorbida-aprueba-fusion-mer-0342` |
| MER-0346 | Acuerdo de transformación de una SL en agrupación de interés económico | `acuerdo-transformacion-sl-agrupacion-interes-economico-mer-0346` |
| MER-0347 | Acuerdo de transformación de una SA en SL | `acuerdo-transformacion-sa-sl-mer-0347` |
| MER-0348 | Acuerdo de transformación de una SL en sociedad colectiva o comanditaria | `acuerdo-transformacion-sl-sociedad-colectiva-mer-0348` |
| MER-0349 | Acuerdo de transformación de una SL en sociedad cooperativa | `acuerdo-transformacion-sl-sociedad-cooperativa-mer-0349` |

### Estatutos, actas, certificaciones y escrituras (31)

| Código | Formulario | Skill |
|---|---|---|
| MER-0311 | Proyecto de cesión global de activo y pasivo de una SL o SA | `proyecto-cesion-global-activo-pasivo-sl-sa-mer-0311` |
| MER-0312 | Acta de junta universal que acuerda la cesión global de activo y pasivo de una SL o SA | `acta-junta-universal-acuerda-cesion-global-activo-mer-0312` |
| MER-0314 | Proyecto de escisión parcial con traspaso a una sociedad ya existente (escisión-absorción) | `proyecto-escision-parcial-traspaso-sociedad-ya-mer-0314` |
| MER-0316 | Proyecto de segregación a favor de una sociedad ya existente | `proyecto-segregacion-favor-sociedad-ya-existente-mer-0316` |
| MER-0317 | Proyecto de escisión parcial de una SL con creación de una nueva SA | `proyecto-escision-parcial-sl-creacion-nueva-sa-mer-0317` |
| MER-0319 | Proyecto de segregación a favor de una sociedad de nueva creación | `proyecto-segregacion-favor-sociedad-nueva-creacion-mer-0319` |
| MER-0320 | Proyecto de escisión total de una SL o SA | `proyecto-escision-total-sl-sa-mer-0320` |
| MER-0321 | Proyecto de escisión parcial con constitución de una nueva sociedad | `proyecto-escision-parcial-constitucion-nueva-sociedad-mer-0321` |
| MER-0323 | Anuncio de publicación del acuerdo de escisión | `anuncio-publicacion-acuerdo-escision-mer-0323` |
| MER-0325 | Escritura pública de escisión total de una SL o SA | `escritura-publica-escision-total-sl-sa-mer-0325` |
| MER-0327 | Anuncio de convocatoria de junta general para acordar la escisión | `anuncio-convocatoria-junta-general-acordar-escision-mer-0327` |
| MER-0328 | Escritura pública de escisión parcial de una SL o SA | `escritura-publica-escision-parcial-sl-sa-mer-0328` |
| MER-0332 | Escritura pública de fusión por absorción de SL o SA | `escritura-publica-fusion-absorcion-sl-sa-mer-0332` |
| MER-0333 | Escritura pública de fusión mediante constitución de una nueva sociedad | `escritura-publica-fusion-mediante-constitucion-nueva-mer-0333` |
| MER-0334 | Anuncio de publicación del acuerdo de fusión | `anuncio-publicacion-acuerdo-fusion-mer-0334` |
| MER-0335 | Anuncio de convocatoria de junta general para acordar la fusión | `anuncio-convocatoria-junta-general-acordar-fusion-mer-0335` |
| MER-0336 | Proyecto de fusión mediante constitución de una nueva sociedad | `proyecto-fusion-mediante-constitucion-nueva-sociedad-mer-0336` |
| MER-0338 | Informe de los administradores sobre el proyecto de fusión | `informe-administradores-sobre-proyecto-fusion-mer-0338` |
| MER-0339 | Proyecto de fusión por absorción de dos sociedades | `proyecto-fusion-absorcion-dos-sociedades-mer-0339` |
| MER-0344 | Anuncio o comunicación individual del acuerdo de transformación de la sociedad | `anuncio-comunicacion-individual-acuerdo-transformacion-mer-0344` |
| MER-0345 | Escritura pública de transformación de una sociedad civil en sociedad limitada | `escritura-publica-transformacion-sociedad-civil-mer-0345` |
| MER-0350 | Escritura pública de transformación de una SA en SL | `escritura-publica-transformacion-sa-sl-mer-0350` |
| MER-0351 | Escritura pública de transformación de una sociedad colectiva en SA | `escritura-publica-transformacion-sociedad-colectiva-sa-mer-0351` |
| MER-0352 | Escritura pública de transformación de una SL en SA | `escritura-publica-transformacion-sl-sa-mer-0352` |
| MER-0358 | Anuncio del acuerdo de fusión especial de sociedad anónima íntegramente participada | `anuncio-acuerdo-fusion-especial-sociedad-anonima-mer-0358` |
| MER-0360 | Certificación del acuerdo de transformación de una SA en SL | `certificacion-acuerdo-transformacion-sa-sl-mer-0360` |
| MER-0361 | Convocatoria de junta para transformar una SA en SL | `convocatoria-junta-transformar-sa-sl-mer-0361` |
| MER-0362 | Anuncio de reducción de capital y transformación de una SA en SL | `anuncio-reduccion-capital-transformacion-sa-sl-mer-0362` |
| MER-0363 | Certificación de reducción de capital de una SA como consecuencia de una escisión | `certificacion-reduccion-capital-sa-como-consecuencia-mer-0363` |
| MER-0364 | Escritura pública de cesión global de activo y pasivo de una SL o SA | `escritura-publica-cesion-global-activo-pasivo-sl-sa-mer-0364` |
| MER-0365 | Certificación del acuerdo de junta sobre cesión global de activo y pasivo de una SL o SA | `certificacion-acuerdo-junta-sobre-cesion-global-activo-mer-0365` |

### Comunicaciones, requerimientos y cartas (7)

| Código | Formulario | Skill |
|---|---|---|
| MER-0318 | Solicitud de depósito del proyecto de escisión en el Registro Mercantil | `solicitud-deposito-proyecto-escision-registro-mercantil-mer-0318` |
| MER-0330 | Solicitud de experto que fije la compensación al socio perjudicado por el tipo de canje en la fusión | `solicitud-experto-fije-compensacion-socio-perjudicado-mer-0330` |
| MER-0337 | Solicitud de expertos independientes para informar sobre el proyecto de fusión de una SA | `solicitud-expertos-independientes-informar-sobre-mer-0337` |
| MER-0340 | Solicitud de depósito del proyecto de fusión en el Registro Mercantil | `solicitud-deposito-proyecto-fusion-registro-mercantil-mer-0340` |
| MER-0353 | Solicitud de experto único por los administradores de la sociedad que se escinde | `solicitud-experto-unico-administradores-sociedad-mer-0353` |
| MER-0357 | Comunicación a los trabajadores del acuerdo de fusión por absorción | `comunicacion-trabajadores-acuerdo-fusion-absorcion-mer-0357` |
| MER-0359 | Carta del consejo de administración que convoca junta para transformar una SL en SA | `carta-consejo-administracion-convoca-junta-transformar-mer-0359` |

### Escritos de trámite y otros (4)

| Código | Formulario | Skill |
|---|---|---|
| MER-0343 | Escrito de adhesión al acuerdo de transformación por socios que asumen responsabilidad personal | `escrito-adhesion-acuerdo-transformacion-socios-asumen-mer-0343` |
| MER-0354 | Instancia al Registro Mercantil de experto independiente para la transformación de SL en SA | `instancia-registro-mercantil-experto-independiente-mer-0354` |
| MER-0355 | Escrito de adhesión de socios a la transformación de una SA en sociedad colectiva o comanditaria | `escrito-adhesion-socios-transformacion-sa-sociedad-mer-0355` |
| MER-0356 | Instancia al Registro Mercantil para depositar el proyecto de fusión de una SA | `instancia-registro-mercantil-depositar-proyecto-fusion-mer-0356` |

---
name: indice
description: "Índice de los 34 formularios de Agencia, distribución, franquicia y colaboración entre empresas. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Agencia, distribución, franquicia y colaboración entre empresas: índice de formularios

> Plugin `formularios-agencia-distribucion-y-franquicia` · 34 formularios · normativa revisada el 25-11-2026.

## Qué es

Para los contratos de colaboración comercial: agencia (Ley 12/1992), distribución exclusiva y selectiva, concesión, franquicia, comisión, patrocinio, alianzas y joint ventures, y las reclamaciones por indemnización de clientela o por resolución.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Contrato de agencia con exclusiva por zona»
- «Contrato de franquicia con canon de entrada y royalties»
- «Reclamación de la indemnización por clientela al terminar la agencia»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-agencia-distribucion-y-franquicia:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Contratos, pactos y cláusulas (32)

| Código | Formulario | Skill |
|---|---|---|
| MER-0479 | Contrato de representación de un futbolista profesional por su agente | `contrato-representacion-futbolista-profesional-agente-mer-0479` |
| MER-0480 | Contrato de colaboración mercantil para la captación de clientes potenciales (leads) | `contrato-colaboracion-mercantil-captacion-clientes-mer-0480` |
| MER-0482 | Contrato de agencia o representación comercial | `contrato-agencia-representacion-comercial-mer-0482` |
| MER-0483 | Contrato de joint venture entre empresas | `contrato-joint-venture-entre-empresas-mer-0483` |
| MER-0484 | Contrato de comercialización de marca o merchandising | `contrato-comercializacion-marca-merchandising-mer-0484` |
| MER-0485 | Contrato de cesión de una cartera de clientes | `contrato-cesion-cartera-clientes-mer-0485` |
| MER-0486 | Contrato de comisión mercantil con o sin garantía del comisionista | `contrato-comision-mercantil-sin-garantia-comisionista-mer-0486` |
| MER-0487 | Cláusulas específicas para el contrato de mediación en la venta | `clausulas-especificas-contrato-mediacion-venta-mer-0487` |
| MER-0488 | Cláusulas específicas para el contrato de mediación inmobiliaria | `clausulas-especificas-contrato-mediacion-inmobiliaria-mer-0488` |
| MER-0490 | Contrato de mediación en la compraventa de inmuebles | `contrato-mediacion-compraventa-inmuebles-mer-0490` |
| MER-0491 | Contrato de agencia sin exclusiva con asunción del riesgo por el agente | `contrato-agencia-sin-exclusiva-asuncion-riesgo-agente-mer-0491` |
| MER-0492 | Contrato de agencia con exclusiva | `contrato-agencia-exclusiva-mer-0492` |
| MER-0493 | Contrato de encargo de comercialización de una vivienda | `contrato-encargo-comercializacion-vivienda-mer-0493` |
| MER-0494 | Contrato de depósito de mercancía en una tienda para su venta | `contrato-deposito-mercancia-tienda-venta-mer-0494` |
| MER-0495 | Contrato de agencia en el sector de las artes gráficas | `contrato-agencia-sector-artes-graficas-mer-0495` |
| MER-0496 | Contrato de patrocinio de un acontecimiento cultural | `contrato-patrocinio-acontecimiento-cultural-mer-0496` |
| MER-0497 | Contrato de patrocinio de un acontecimiento deportivo | `contrato-patrocinio-acontecimiento-deportivo-mer-0497` |
| MER-0498 | Contrato de distribución en exclusiva o concesión | `contrato-distribucion-exclusiva-concesion-mer-0498` |
| MER-0499 | Contrato de colaboración entre agencia de viajes y establecimiento hotelero | `contrato-colaboracion-entre-agencia-viajes-mer-0499` |
| MER-0500 | Contrato de representación de un artista | `contrato-representacion-artista-mer-0500` |
| MER-0501 | Contrato mercantil de comisión | `contrato-mercantil-comision-mer-0501` |
| MER-0502 | Contrato de patrocinio con fines publicitarios | `contrato-patrocinio-fines-publicitarios-mer-0502` |
| MER-0503 | Contrato de distribución comercial | `contrato-distribucion-comercial-mer-0503` |
| MER-0504 | Contrato de franquicia entre franquiciador y franquiciado | `contrato-franquicia-entre-franquiciador-franquiciado-mer-0504` |
| MER-0505 | Contrato de adhesión de un minorista a una central de compras | `contrato-adhesion-minorista-central-compras-mer-0505` |
| MER-0506 | Contrato de agencia mercantil | `contrato-agencia-mercantil-mer-0506` |
| MER-0507 | Contrato de agencia mercantil con exclusiva para la promoción de un artista | `contrato-agencia-mercantil-exclusiva-promocion-artista-mer-0507` |
| MER-0508 | Contrato de patrocinio (sponsoring) en que el patrocinado publicita los productos del patrocinador | `contrato-patrocinio-sponsoring-patrocinado-publicita-mer-0508` |
| MER-0509 | Convenio de colaboración entre despachos de abogados | `convenio-colaboracion-entre-despachos-abogados-mer-0509` |
| MER-0510 | Contrato de cuentas en participación | `contrato-cuentas-participacion-mer-0510` |
| MER-0511 | Contrato de concesión con distribución exclusiva de marcas | `contrato-concesion-distribucion-exclusiva-marcas-mer-0511` |
| MER-0512 | Contrato de colaboración entre una empresa productora y otra que vende sus productos por internet | `contrato-colaboracion-entre-empresa-productora-otra-mer-0512` |

### Escritos de trámite y otros (2)

| Código | Formulario | Skill |
|---|---|---|
| MER-0481 | Alianza estratégica entre una “startup” tecnológica y una empresa (contrato) | `alianza-estrategica-entre-startup-tecnologica-empresa-mer-0481` |
| MER-0489 | Franquicia de producción, distribución y servicios (contrato) | `franquicia-produccion-distribucion-servicios-contrato-mer-0489` |

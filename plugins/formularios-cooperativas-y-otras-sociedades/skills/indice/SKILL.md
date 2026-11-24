---
name: indice
description: "Índice de los 113 formularios de Cooperativas, sociedades laborales y otras formas de empresa. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre."
---

# Cooperativas, sociedades laborales y otras formas de empresa: índice de formularios

> Plugin `formularios-cooperativas-y-otras-sociedades` · 113 formularios · normativa revisada el 24-11-2026.

## Qué es

Para las formas societarias especiales: cooperativas (estatutos, asambleas, consejo rector, altas y bajas de socios, reembolsos), sociedades laborales y participadas, sociedades agrarias de transformación, de garantía recíproca, agrupaciones de interés económico, comanditarias y colectivas, sociedades profesionales y protocolo familiar.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Estatutos de una cooperativa de trabajo asociado»
- «Solicitud de baja voluntaria de un socio cooperativista»
- «Estatutos de una agrupación de interés económico»

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

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-cooperativas-y-otras-sociedades:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado, con su `formulario.md` y su `marco.md`.

### Demandas, peticiones y solicitudes iniciales (2)

| Código | Formulario | Skill |
|---|---|---|
| MER-0424 | Demanda del socio contra el acuerdo del consejo rector que califica su baja en la cooperativa | `demanda-socio-contra-acuerdo-consejo-rector-califica-mer-0424` |
| MER-0462 | Demanda de impugnación de un acuerdo nulo o anulable de la asamblea general de una cooperativa | `demanda-impugnacion-acuerdo-nulo-anulable-asamblea-mer-0462` |

### Contratos, pactos y cláusulas (6)

| Código | Formulario | Skill |
|---|---|---|
| MER-0366 | Acuerdo de reembolso de aportaciones al socio que causa baja en una cooperativa | `acuerdo-reembolso-aportaciones-socio-causa-baja-mer-0366` |
| MER-0367 | Acuerdo de constitución de una unión temporal de empresas (UTE) | `acuerdo-constitucion-union-temporal-empresas-ute-mer-0367` |
| MER-0368 | Acuerdo del consejo rector de una cooperativa sobre la admisión o denegación de un socio | `acuerdo-consejo-rector-cooperativa-sobre-admision-mer-0368` |
| MER-0369 | Protocolo de empresa familiar | `protocolo-empresa-familiar-mer-0369` |
| MER-0374 | Acuerdo de la junta general de adoptar la calificación de sociedad laboral | `acuerdo-junta-general-adoptar-calificacion-sociedad-mer-0374` |
| MER-0426 | Contrato de venta de aportaciones al capital de una cooperativa a un tercero no socio | `contrato-venta-aportaciones-capital-cooperativa-mer-0426` |

### Estatutos, actas, certificaciones y escrituras (44)

| Código | Formulario | Skill |
|---|---|---|
| MER-0384 | Convocatoria del consejo rector por consejeros ante la inacción del presidente | `convocatoria-consejo-rector-consejeros-ante-inaccion-mer-0384` |
| MER-0386 | Certificación de los acuerdos del consejo rector de una cooperativa | `certificacion-acuerdos-consejo-rector-cooperativa-mer-0386` |
| MER-0402 | Convocatoria de la asamblea constituyente de una cooperativa | `convocatoria-asamblea-constituyente-cooperativa-mer-0402` |
| MER-0403 | Anuncio de convocatoria de asamblea general ordinaria o extraordinaria de una cooperativa | `anuncio-convocatoria-asamblea-general-ordinaria-mer-0403` |
| MER-0410 | Anuncio del acuerdo de disolución de una cooperativa | `anuncio-acuerdo-disolucion-cooperativa-mer-0410` |
| MER-0412 | Acta de asamblea general ordinaria de una cooperativa | `acta-asamblea-general-ordinaria-cooperativa-mer-0412` |
| MER-0413 | Acta de asamblea general universal de una cooperativa | `acta-asamblea-general-universal-cooperativa-mer-0413` |
| MER-0414 | Acta de disolución y liquidación de una unión temporal de empresas | `acta-disolucion-liquidacion-union-temporal-empresas-mer-0414` |
| MER-0415 | Escritura pública de constitución de una unión temporal de empresas | `escritura-publica-constitucion-union-temporal-empresas-mer-0415` |
| MER-0416 | Estatutos de una agrupación de interés económico | `estatutos-agrupacion-interes-economico-mer-0416` |
| MER-0417 | Escritura pública de constitución de una agrupación europea de interés económico | `escritura-publica-constitucion-agrupacion-europea-mer-0417` |
| MER-0418 | Escritura de constitución de una sociedad limitada profesional | `escritura-constitucion-sociedad-limitada-profesional-mer-0418` |
| MER-0419 | Estatutos sociales de una sociedad limitada profesional | `estatutos-sociales-sociedad-limitada-profesional-mer-0419` |
| MER-0420 | Estatutos sociales de una sociedad colectiva | `estatutos-sociales-sociedad-colectiva-mer-0420` |
| MER-0421 | Certificación de alta de un socio en una SAT, con o sin ampliación de capital | `certificacion-alta-socio-sat-sin-ampliacion-capital-mer-0421` |
| MER-0422 | Certificación del nombramiento de una nueva junta rectora de una SAT | `certificacion-nombramiento-nueva-junta-rectora-sat-mer-0422` |
| MER-0423 | Certificación de baja de un socio de una SAT, con o sin reducción de capital | `certificacion-baja-socio-sat-sin-reduccion-capital-mer-0423` |
| MER-0427 | Estatutos sociales de una sociedad de garantía recíproca | `estatutos-sociales-sociedad-garantia-reciproca-mer-0427` |
| MER-0428 | Estatutos de una unión temporal de empresas (UTE) | `estatutos-union-temporal-empresas-ute-mer-0428` |
| MER-0429 | Estatutos sociales de una sociedad anónima laboral | `estatutos-sociales-sociedad-anonima-laboral-mer-0429` |
| MER-0436 | Acta de asamblea de cooperativa que acuerda demandar a consejeros sin constar en el orden del día | `acta-asamblea-cooperativa-acuerda-demandar-consejeros-mer-0436` |
| MER-0437 | Acta de asamblea de cooperativa que acuerda disolver, liquidar o reactivar la sociedad | `acta-asamblea-cooperativa-acuerda-disolver-liquidar-mer-0437` |
| MER-0439 | Acta de una reunión del consejo rector de una cooperativa | `acta-reunion-consejo-rector-cooperativa-mer-0439` |
| MER-0440 | Acta del consejo rector de una cooperativa que nombra consejero delegado | `acta-consejo-rector-cooperativa-nombra-consejero-mer-0440` |
| MER-0441 | Convocatoria de reunión del consejo rector de una cooperativa | `convocatoria-reunion-consejo-rector-cooperativa-mer-0441` |
| MER-0442 | Convocatoria de asamblea general ordinaria o extraordinaria de una cooperativa | `convocatoria-asamblea-general-ordinaria-extraordinaria-mer-0442` |
| MER-0443 | Estatutos sociales de una cooperativa | `estatutos-sociales-cooperativa-mer-0443` |
| MER-0444 | Escritura pública de constitución de una cooperativa | `escritura-publica-constitucion-cooperativa-mer-0444` |
| MER-0446 | Estatutos sociales de una sociedad comanditaria simple | `estatutos-sociales-sociedad-comanditaria-simple-mer-0446` |
| MER-0447 | Escritura pública de constitución de una sociedad comanditaria simple | `escritura-publica-constitucion-sociedad-comanditaria-mer-0447` |
| MER-0450 | Estatutos sociales de una sociedad limitada laboral | `estatutos-sociales-sociedad-limitada-laboral-mer-0450` |
| MER-0451 | Escritura de constitución de una sociedad laboral limitada o anónima | `escritura-constitucion-sociedad-laboral-limitada-mer-0451` |
| MER-0452 | Escritura de constitución de una sociedad de garantía recíproca | `escritura-constitucion-sociedad-garantia-reciproca-mer-0452` |
| MER-0453 | Escritura de acta fundacional de una sociedad agraria de transformación | `escritura-acta-fundacional-sociedad-agraria-mer-0453` |
| MER-0454 | Escritura pública de constitución de una agrupación de interés económico | `escritura-publica-constitucion-agrupacion-interes-mer-0454` |
| MER-0455 | Estatutos sociales de una sociedad comanditaria por acciones | `estatutos-sociales-sociedad-comanditaria-acciones-mer-0455` |
| MER-0456 | Estatutos sociales de una sociedad agraria de transformación | `estatutos-sociales-sociedad-agraria-transformacion-mer-0456` |
| MER-0457 | Escritura de constitución de una sociedad colectiva, con o sin socio industrial | `escritura-constitucion-sociedad-colectiva-sin-socio-mer-0457` |
| MER-0458 | Convocatoria de asamblea general de una cooperativa con notificación individual a cada socio | `convocatoria-asamblea-general-cooperativa-notificacion-mer-0458` |
| MER-0459 | Escritura pública de constitución de una sociedad comanditaria por acciones | `escritura-publica-constitucion-sociedad-comanditaria-mer-0459` |
| MER-0464 | Acta de asamblea de cooperativa sobre aportaciones no dinerarias y nuevas aportaciones de socios | `acta-asamblea-cooperativa-sobre-aportaciones-no-mer-0464` |
| MER-0467 | Acta del consejo rector de una cooperativa que nombra y cesa al gerente | `acta-consejo-rector-cooperativa-nombra-cesa-gerente-mer-0467` |
| MER-0469 | Acta del consejo rector de una cooperativa que acuerda la baja obligatoria y expulsión de un socio | `acta-consejo-rector-cooperativa-acuerda-baja-mer-0469` |
| MER-0478 | Estatutos de una fundación | `estatutos-fundacion-mer-0478` |

### Comunicaciones, requerimientos y cartas (44)

| Código | Formulario | Skill |
|---|---|---|
| MER-0370 | Comunicación de intención de transmitir acciones o participaciones laborales a no trabajador fijo | `comunicacion-intencion-transmitir-acciones-mer-0370` |
| MER-0371 | Solicitud del socio cooperativista de información sobre derechos económicos y orden del día | `solicitud-socio-cooperativista-informacion-sobre-mer-0371` |
| MER-0372 | Notificación de la administración de una SL laboral sobre transmisión de participaciones laborales | `notificacion-administracion-sl-laboral-sobre-mer-0372` |
| MER-0373 | Comunicación al Registro de la transmisión de acciones o participaciones de una sociedad laboral | `comunicacion-registro-transmision-acciones-mer-0373` |
| MER-0375 | Solicitud de autorización para superar el límite de horas-año de no socios en sociedad laboral | `solicitud-autorizacion-superar-limite-horas-ano-no-mer-0375` |
| MER-0376 | Requerimiento notarial al exsocio para vender sus acciones o participaciones laborales | `requerimiento-notarial-exsocio-vender-acciones-mer-0376` |
| MER-0377 | Solicitud de calificación e inscripción de una sociedad laboral nueva o preexistente | `solicitud-calificacion-e-inscripcion-sociedad-laboral-mer-0377` |
| MER-0378 | Solicitud de reembolso de las aportaciones de un socio cooperativista fallecido | `solicitud-reembolso-aportaciones-socio-cooperativista-mer-0378` |
| MER-0379 | Solicitud de prórroga del plazo para convocar la asamblea general ordinaria de una cooperativa | `solicitud-prorroga-plazo-convocar-asamblea-general-mer-0379` |
| MER-0380 | Solicitud judicial de asamblea extraordinaria de cooperativa por interventores y socios | `solicitud-judicial-asamblea-extraordinaria-cooperativa-mer-0380` |
| MER-0381 | Solicitud judicial de convocatoria de asamblea ordinaria por interventores y socios de cooperativa | `solicitud-judicial-convocatoria-asamblea-ordinaria-mer-0381` |
| MER-0382 | Solicitud de nuevos puntos del orden del día de la asamblea por interventores y minoría de socios | `solicitud-nuevos-puntos-orden-dia-asamblea-mer-0382` |
| MER-0383 | Notificación al socio del acuerdo de expulsión de una cooperativa | `notificacion-socio-acuerdo-expulsion-cooperativa-mer-0383` |
| MER-0388 | Solicitud al Tribunal de Instancia de interventor que fiscalice la liquidación de una cooperativa | `solicitud-tribunal-instancia-interventor-fiscalice-mer-0388` |
| MER-0389 | Comunicación de puesta a disposición del fondo de educación y promoción al liquidar una cooperativa | `comunicacion-puesta-disposicion-fondo-educacion-mer-0389` |
| MER-0390 | Solicitud de auditoría de cuentas de una cooperativa por una minoría de socios | `solicitud-auditoria-cuentas-cooperativa-minoria-socios-mer-0390` |
| MER-0392 | Aviso al socio del vencimiento del plazo de la aportación obligatoria pendiente en cooperativa | `aviso-socio-vencimiento-plazo-aportacion-obligatoria-mer-0392` |
| MER-0393 | Solicitud de autorización a una cooperativa para superar el límite de operaciones con terceros | `solicitud-autorizacion-cooperativa-superar-limite-mer-0393` |
| MER-0394 | Requerimiento al presidente para que convoque el consejo rector de una cooperativa | `requerimiento-presidente-convoque-consejo-rector-mer-0394` |
| MER-0397 | Solicitud de autorización a la cooperativa para operar con terceros no socios | `solicitud-autorizacion-cooperativa-operar-terceros-no-mer-0397` |
| MER-0398 | Comunicación del socio que ejerce la acción de responsabilidad contra el consejo rector | `comunicacion-socio-ejerce-accion-responsabilidad-mer-0398` |
| MER-0399 | Solicitud del socio de ser liberado de participar en las actividades cooperativizadas | `solicitud-socio-ser-liberado-participar-actividades-mer-0399` |
| MER-0400 | Solicitud de copia certificada de los acuerdos de las asambleas generales de una cooperativa | `solicitud-copia-certificada-acuerdos-asambleas-mer-0400` |
| MER-0404 | Solicitud del socio al consejo rector de convocar asamblea para disolver la cooperativa | `solicitud-socio-consejo-rector-convocar-asamblea-mer-0404` |
| MER-0405 | Solicitud del socio de forma de imputación de las pérdidas de la cooperativa | `solicitud-socio-forma-imputacion-perdidas-cooperativa-mer-0405` |
| MER-0406 | Requerimiento de los interventores al consejo rector para convocar la asamblea general ordinaria | `requerimiento-interventores-consejo-rector-convocar-mer-0406` |
| MER-0407 | Requerimiento de interventores y socios al consejo rector para convocar asamblea extraordinaria | `requerimiento-interventores-socios-consejo-rector-mer-0407` |
| MER-0408 | Solicitud de certificación al Registro de Cooperativas | `solicitud-certificacion-registro-cooperativas-mer-0408` |
| MER-0409 | Solicitud del socio de autorización para realizar actividades competitivas con la cooperativa | `solicitud-socio-autorizacion-realizar-actividades-mer-0409` |
| MER-0411 | Solicitud del socio de una sociedad colectiva para operar por cuenta propia | `solicitud-socio-sociedad-colectiva-operar-cuenta-propia-mer-0411` |
| MER-0430 | Solicitud de un socio al consejo rector de copia certificada de sus acuerdos que le afecten | `solicitud-socio-consejo-rector-copia-certificada-mer-0430` |
| MER-0431 | Solicitud de socios al consejo rector para examinar la documentación económica de la cooperativa | `solicitud-socios-consejo-rector-examinar-documentacion-mer-0431` |
| MER-0434 | Solicitud de baja voluntaria de un socio cooperativista disconforme con un acuerdo de la asamblea | `solicitud-baja-voluntaria-socio-cooperativista-mer-0434` |
| MER-0435 | Solicitud del propio socio de su baja obligatoria en la cooperativa | `solicitud-propio-socio-baja-obligatoria-cooperativa-mer-0435` |
| MER-0445 | Solicitud de un socio al consejo rector de copia certificada de los acuerdos de la asamblea general | `solicitud-socio-consejo-rector-copia-certificada-mer-0445` |
| MER-0448 | Solicitud de calificación previa del proyecto de estatutos de una cooperativa | `solicitud-calificacion-previa-proyecto-estatutos-mer-0448` |
| MER-0449 | Solicitud de inscripción de la escritura de constitución de una cooperativa en su Registro | `solicitud-inscripcion-escritura-constitucion-mer-0449` |
| MER-0460 | Carta del gerente de la cooperativa reclamando al socio el desembolso pendiente de su aportación | `carta-gerente-cooperativa-reclamando-socio-desembolso-mer-0460` |
| MER-0465 | Carta de la cooperativa reclamando a un antiguo socio su parte de las pérdidas | `carta-cooperativa-reclamando-antiguo-socio-parte-mer-0465` |
| MER-0472 | Solicitud judicial de interventores para convocar la asamblea ordinaria de la cooperativa | `solicitud-judicial-interventores-convocar-asamblea-mer-0472` |
| MER-0474 | Comunicación del consejo rector al solicitante de su admisión como socio de la cooperativa | `comunicacion-consejo-rector-solicitante-admision-como-mer-0474` |
| MER-0475 | Solicitud de ingreso como socio en una cooperativa | `solicitud-ingreso-como-socio-cooperativa-mer-0475` |
| MER-0476 | Comunicación del socio al consejo rector de su baja voluntaria en la cooperativa | `comunicacion-socio-consejo-rector-baja-voluntaria-mer-0476` |
| MER-0477 | Solicitud de socios al consejo rector para convocar asamblea general extraordinaria de cooperativa | `solicitud-socios-consejo-rector-convocar-asamblea-mer-0477` |

### Escritos de trámite y otros (17)

| Código | Formulario | Skill |
|---|---|---|
| MER-0385 | Separación del socio de la cooperativa por cambio de clase, transformación, fusión o escisión | `separacion-socio-cooperativa-cambio-clase-mer-0385` |
| MER-0387 | Lista de asistentes a la asamblea general de una cooperativa | `lista-asistentes-asamblea-general-cooperativa-mer-0387` |
| MER-0391 | Preaviso al consejo rector de baja voluntaria del socio de una cooperativa | `preaviso-consejo-rector-baja-voluntaria-socio-mer-0391` |
| MER-0395 | Escrito de delegación de representación en otro socio para la asamblea general de una cooperativa | `escrito-delegacion-representacion-otro-socio-asamblea-mer-0395` |
| MER-0396 | Escrito del socio que se separa de la cooperativa por obligaciones gravemente onerosas | `escrito-socio-separa-cooperativa-obligaciones-mer-0396` |
| MER-0401 | Recibo de cobro de retornos cooperativos por el socio | `recibo-cobro-retornos-cooperativos-socio-mer-0401` |
| MER-0425 | Relación de socios de una sociedad agraria de transformación | `relacion-socios-sociedad-agraria-transformacion-mer-0425` |
| MER-0432 | Escrito del socio impugnando el acuerdo del consejo rector que le deniega la baja voluntaria | `escrito-socio-impugnando-acuerdo-consejo-rector-le-mer-0432` |
| MER-0433 | Impugnación del acuerdo del consejo rector que impone al socio la baja obligatoria o expulsión | `impugnacion-acuerdo-consejo-rector-impone-socio-baja-mer-0433` |
| MER-0438 | Impugnación del importe del reembolso fijado por el consejo rector tras la baja voluntaria | `impugnacion-importe-reembolso-fijado-consejo-rector-mer-0438` |
| MER-0461 | Impugnación del acuerdo del consejo rector que rechaza admitir un nuevo socio de la cooperativa | `impugnacion-acuerdo-consejo-rector-rechaza-admitir-mer-0461` |
| MER-0463 | Comparecencia del socio ante el secretario del consejo rector para delegar su voto | `comparecencia-socio-ante-secretario-consejo-rector-mer-0463` |
| MER-0466 | Propuesta del comité de empresa de un trabajador como vocal del consejo rector de la cooperativa | `propuesta-comite-empresa-trabajador-como-vocal-consejo-mer-0466` |
| MER-0468 | Escrito de un socio pidiendo la destitución de un consejero de cooperativa por incompatibilidad | `escrito-socio-pidiendo-destitucion-consejero-mer-0468` |
| MER-0470 | Impugnación por socios del acuerdo del consejo rector que admite a un nuevo socio de la cooperativa | `impugnacion-socios-acuerdo-consejo-rector-admite-nuevo-mer-0470` |
| MER-0471 | Propuesta de interventores y del 10 por ciento de socios para el orden del día de la asamblea | `propuesta-interventores-10-ciento-socios-orden-dia-mer-0471` |
| MER-0473 | Escrito manuscrito de delegación de voto de un socio de cooperativa en la asamblea | `escrito-manuscrito-delegacion-voto-socio-cooperativa-mer-0473` |

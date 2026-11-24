---
name: indice
description: "Índice de los 68 formularios de Banca, financiación, valores y garantías. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Banca, financiación, valores y garantías: índice de formularios

> Plugin `formularios-banca-financiacion-y-garantias` · 68 formularios · normativa revisada el 24-11-2026.

## Qué es

Para la financiación empresarial y los productos bancarios: préstamos y créditos, préstamo participativo, leasing, renting, factoring y confirming, avales y garantías a primer requerimiento, prendas e hipotecas mobiliarias, swaps, depósitos y custodia de valores, FEIN y reclamaciones al banco.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Contrato de préstamo participativo a una SL»
- «Garantía a primer requerimiento»
- «Contrato de leasing de maquinaria»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-banca-financiacion-y-garantias:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado, con su `formulario.md` y su `marco.md`.

### Contratos, pactos y cláusulas (45)

| Código | Formulario | Skill |
|---|---|---|
| MER-0618 | Contrato de swap de tipos de interés entre entidad de crédito y cliente | `contrato-swap-tipos-interes-entre-entidad-credito-mer-0618` |
| MER-0619 | Contrato de aval bancario entre banco y cliente | `contrato-aval-bancario-entre-banco-cliente-mer-0619` |
| MER-0621 | Contrato de venta con arrendamiento financiero posterior (sale and lease back) | `contrato-venta-arrendamiento-financiero-posterior-sale-mer-0621` |
| MER-0622 | Contrato de préstamo convertible a una startup | `contrato-prestamo-convertible-startup-mer-0622` |
| MER-0625 | Contrato de renting de bienes muebles | `contrato-renting-bienes-muebles-mer-0625` |
| MER-0626 | Contrato de confirming de pago a proveedores | `contrato-confirming-pago-proveedores-mer-0626` |
| MER-0627 | Contrato de forfaiting de créditos de exportación | `contrato-forfaiting-creditos-exportacion-mer-0627` |
| MER-0628 | Contrato de factoring de créditos comerciales | `contrato-factoring-creditos-comerciales-mer-0628` |
| MER-0629 | Contrato de préstamo participativo | `contrato-prestamo-participativo-mer-0629` |
| MER-0630 | Contrato de préstamo de dinero | `contrato-prestamo-dinero-mer-0630` |
| MER-0632 | Contrato de servicio de asesoramiento financiero | `contrato-servicio-asesoramiento-financiero-mer-0632` |
| MER-0633 | Contrato de descuento bancario de efectos comerciales | `contrato-descuento-bancario-efectos-comerciales-mer-0633` |
| MER-0636 | Contrato de prenda sobre mercancías y acciones | `contrato-prenda-sobre-mercancias-acciones-mer-0636` |
| MER-0637 | Contrato de línea de avales bancarios | `contrato-linea-avales-bancarios-mer-0637` |
| MER-0638 | Contrato de contraaval entre la entidad avalista y el avalado | `contrato-contraaval-entre-entidad-avalista-avalado-mer-0638` |
| MER-0639 | Contrato de préstamo participativo como fondos propios del prestatario | `contrato-prestamo-participativo-como-fondos-propios-mer-0639` |
| MER-0640 | Contrato de alquiler de cajas de seguridad bancarias | `contrato-alquiler-cajas-seguridad-bancarias-mer-0640` |
| MER-0641 | Contrato de tarjeta de crédito, débito o monedero | `contrato-tarjeta-credito-debito-monedero-mer-0641` |
| MER-0642 | Contrato de préstamo mercantil garantizado con prenda de acciones | `contrato-prestamo-mercantil-garantizado-prenda-acciones-mer-0642` |
| MER-0644 | Contrato de cuenta corriente bancaria con condiciones generales | `contrato-cuenta-corriente-bancaria-condiciones-mer-0644` |
| MER-0645 | Contrato de depósito bancario a plazo fijo | `contrato-deposito-bancario-plazo-fijo-mer-0645` |
| MER-0648 | Contrato de préstamo de valores | `contrato-prestamo-valores-mer-0648` |
| MER-0650 | Contrato de depósito en garantía o cuenta escrow | `contrato-deposito-garantia-cuenta-escrow-mer-0650` |
| MER-0652 | Contrato de renting de bienes (modelo general) | `contrato-renting-bienes-modelo-general-mer-0652` |
| MER-0653 | Contrato de intermediación para obtener o modificar créditos, préstamos y servicios financieros | `contrato-intermediacion-obtener-modificar-creditos-mer-0653` |
| MER-0654 | Acuerdo de prenda sobre un crédito o deuda | `acuerdo-prenda-sobre-credito-deuda-mer-0654` |
| MER-0658 | Contrato de afianzamiento de un préstamo | `contrato-afianzamiento-prestamo-mer-0658` |
| MER-0660 | Contrato de cesión de créditos | `contrato-cesion-creditos-mer-0660` |
| MER-0661 | Póliza de crédito para la negociación o el descuento de documentos | `poliza-credito-negociacion-descuento-documentos-mer-0661` |
| MER-0662 | Contrato de préstamo del vendedor para financiar al comprador de bienes muebles | `contrato-prestamo-vendedor-financiar-comprador-bienes-mer-0662` |
| MER-0665 | Contrato de crédito en cuenta corriente con reconocimiento de deuda | `contrato-credito-cuenta-corriente-reconocimiento-deuda-mer-0665` |
| MER-0667 | Contrato tipo de depósito y administración de valores en títulos o anotaciones en cuenta | `contrato-tipo-deposito-administracion-valores-titulos-mer-0667` |
| MER-0668 | Contrato entre miembro del mercado y cliente para operar en el mercado de valores | `contrato-entre-miembro-mercado-cliente-operar-mercado-mer-0668` |
| MER-0669 | Contrato mercantil de cuenta corriente | `contrato-mercantil-cuenta-corriente-mer-0669` |
| MER-0670 | Contrato mercantil de depósito bancario | `contrato-mercantil-deposito-bancario-mer-0670` |
| MER-0673 | Contrato de gestión discrecional de carteras de inversión | `contrato-gestion-discrecional-carteras-inversion-mer-0673` |
| MER-0674 | Contrato de prenda sobre un seguro de vida | `contrato-prenda-sobre-seguro-vida-mer-0674` |
| MER-0675 | Contrato de liquidez sobre acciones propias | `contrato-liquidez-sobre-acciones-propias-mer-0675` |
| MER-0678 | Contrato de prenda con entrega de la posesión al acreedor | `contrato-prenda-entrega-posesion-acreedor-mer-0678` |
| MER-0679 | Contrato de fianza en garantía de una deuda | `contrato-fianza-garantia-deuda-mer-0679` |
| MER-0680 | Contrato de préstamo entre empresarios | `contrato-prestamo-entre-empresarios-mer-0680` |
| MER-0681 | Contrato de arrendamiento financiero con opción de compra (leasing) | `contrato-arrendamiento-financiero-opcion-compra-leasing-mer-0681` |
| MER-0683 | Contrato de préstamo garantizado con hipoteca | `contrato-prestamo-garantizado-hipoteca-mer-0683` |
| MER-0684 | Contrato de prenda sin desplazamiento de la posesión | `contrato-prenda-sin-desplazamiento-posesion-mer-0684` |
| MER-0685 | Contrato de constitución de una garantía pignoraticia | `contrato-constitucion-garantia-pignoraticia-mer-0685` |

### Estatutos, actas, certificaciones y escrituras (10)

| Código | Formulario | Skill |
|---|---|---|
| MER-0624 | Escritura de préstamo con garantía hipotecaria | `escritura-prestamo-garantia-hipotecaria-mer-0624` |
| MER-0631 | Escritura de reconocimiento de deuda y prenda sobre participaciones sociales de una SL | `escritura-reconocimiento-deuda-prenda-sobre-mer-0631` |
| MER-0635 | Escritura de prenda sobre acciones de una sociedad anónima | `escritura-prenda-sobre-acciones-sociedad-anonima-mer-0635` |
| MER-0643 | Escritura de hipoteca naval | `escritura-hipoteca-naval-mer-0643` |
| MER-0649 | Escritura de préstamo hipotecario a interés variable | `escritura-prestamo-hipotecario-interes-variable-mer-0649` |
| MER-0659 | Escritura de hipoteca mobiliaria sobre un establecimiento mercantil | `escritura-hipoteca-mobiliaria-sobre-establecimiento-mer-0659` |
| MER-0664 | Anuncio previo de una oferta pública de adquisición de valores | `anuncio-previo-oferta-publica-adquisicion-valores-mer-0664` |
| MER-0676 | Escritura de hipoteca mobiliaria sobre una patente | `escritura-hipoteca-mobiliaria-sobre-patente-mer-0676` |
| MER-0677 | Escritura de hipoteca mobiliaria sobre derechos de propiedad intelectual | `escritura-hipoteca-mobiliaria-sobre-derechos-propiedad-mer-0677` |
| MER-0682 | Escritura de hipoteca de máximo en garantía de obligaciones futuras | `escritura-hipoteca-maximo-garantia-obligaciones-futuras-mer-0682` |

### Comunicaciones, requerimientos y cartas (6)

| Código | Formulario | Skill |
|---|---|---|
| MER-0620 | Reclamación al banco del importe de un aval a primer requerimiento | `reclamacion-banco-importe-aval-primer-requerimiento-mer-0620` |
| MER-0646 | Comunicación al banco del uso indebido de una tarjeta por un tercero no autorizado | `comunicacion-banco-uso-indebido-tarjeta-tercero-no-mer-0646` |
| MER-0655 | Solicitud de apertura de crédito documentario | `solicitud-apertura-credito-documentario-mer-0655` |
| MER-0656 | Carta de garantía bancaria a primer requerimiento (modelo) | `carta-garantia-bancaria-primer-requerimiento-modelo-mer-0656` |
| MER-0663 | Solicitud de autorización de una oferta pública de adquisición de valores | `solicitud-autorizacion-oferta-publica-adquisicion-mer-0663` |
| MER-0672 | Carta de patrocinio o confort letter a favor de una filial | `carta-patrocinio-confort-letter-favor-filial-mer-0672` |

### Escritos de trámite y otros (7)

| Código | Formulario | Skill |
|---|---|---|
| MER-0623 | Ficha Europea de Información Normalizada (FEIN) de préstamo hipotecario | `ficha-europea-informacion-normalizada-fein-prestamo-mer-0623` |
| MER-0634 | Crédito refaccionario (contrato) | `credito-refaccionario-contrato-mer-0634` |
| MER-0647 | Crédito al consumo (contrato) | `credito-consumo-contrato-mer-0647` |
| MER-0651 | Leasing de equipos informáticos (contrato) | `leasing-equipos-informaticos-contrato-mer-0651` |
| MER-0657 | Garantía a primer requerimiento (contrato) | `garantia-primer-requerimiento-contrato-mer-0657` |
| MER-0666 | Contenido del folleto informativo de una oferta de venta de acciones | `contenido-folleto-informativo-oferta-venta-acciones-mer-0666` |
| MER-0671 | Custodia y administración de valores (contrato) | `custodia-administracion-valores-contrato-mer-0671` |

# Banca, financiación, valores y garantías

> Plugin de Claude Code `formularios-banca-financiacion-y-garantias` · **68 formularios** · Mercantil · normativa revisada el 24-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para la financiación empresarial y los productos bancarios: préstamos y créditos, préstamo participativo, leasing, renting, factoring y confirming, avales y garantías a primer requerimiento, prendas e hipotecas mobiliarias, swaps, depósitos y custodia de valores, FEIN y reclamaciones al banco.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 68 está al final):

- **Contratos, pactos y cláusulas** (45). Por ejemplo: Contrato de swap de tipos de interés entre entidad de crédito y cliente; Contrato de aval bancario entre banco y cliente; Contrato de venta con arrendamiento financiero posterior (sale and lease back).
- **Estatutos, actas, certificaciones y escrituras** (10). Por ejemplo: Escritura de préstamo con garantía hipotecaria; Escritura de reconocimiento de deuda y prenda sobre participaciones sociales de una SL; Escritura de prenda sobre acciones de una sociedad anónima.
- **Comunicaciones, requerimientos y cartas** (6). Por ejemplo: Reclamación al banco del importe de un aval a primer requerimiento; Comunicación al banco del uso indebido de una tarjeta por un tercero no autorizado; Solicitud de apertura de crédito documentario.
- **Escritos de trámite y otros** (7). Por ejemplo: Ficha Europea de Información Normalizada (FEIN) de préstamo hipotecario; Crédito refaccionario (contrato); Crédito al consumo (contrato).

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Contrato de préstamo participativo a una SL»
   - «Garantía a primer requerimiento»
   - «Contrato de leasing de maquinaria»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-banca-financiacion-y-garantias:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-banca-financiacion-y-garantias:contrato-swap-tipos-interes-entre-entidad-credito-mer-0618`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 24-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 3.676 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-banca-financiacion-y-garantias@formularios-juridicos-mercantil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-mercantil-espana
/plugin install formularios-banca-financiacion-y-garantias@formularios-juridicos-mercantil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-banca-financiacion-y-garantias.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (68)

| Código | Formulario | Skill |
|---|---|---|
| MER-0618 | Contrato de swap de tipos de interés entre entidad de crédito y cliente | `contrato-swap-tipos-interes-entre-entidad-credito-mer-0618` |
| MER-0619 | Contrato de aval bancario entre banco y cliente | `contrato-aval-bancario-entre-banco-cliente-mer-0619` |
| MER-0620 | Reclamación al banco del importe de un aval a primer requerimiento | `reclamacion-banco-importe-aval-primer-requerimiento-mer-0620` |
| MER-0621 | Contrato de venta con arrendamiento financiero posterior (sale and lease back) | `contrato-venta-arrendamiento-financiero-posterior-sale-mer-0621` |
| MER-0622 | Contrato de préstamo convertible a una startup | `contrato-prestamo-convertible-startup-mer-0622` |
| MER-0623 | Ficha Europea de Información Normalizada (FEIN) de préstamo hipotecario | `ficha-europea-informacion-normalizada-fein-prestamo-mer-0623` |
| MER-0624 | Escritura de préstamo con garantía hipotecaria | `escritura-prestamo-garantia-hipotecaria-mer-0624` |
| MER-0625 | Contrato de renting de bienes muebles | `contrato-renting-bienes-muebles-mer-0625` |
| MER-0626 | Contrato de confirming de pago a proveedores | `contrato-confirming-pago-proveedores-mer-0626` |
| MER-0627 | Contrato de forfaiting de créditos de exportación | `contrato-forfaiting-creditos-exportacion-mer-0627` |
| MER-0628 | Contrato de factoring de créditos comerciales | `contrato-factoring-creditos-comerciales-mer-0628` |
| MER-0629 | Contrato de préstamo participativo | `contrato-prestamo-participativo-mer-0629` |
| MER-0630 | Contrato de préstamo de dinero | `contrato-prestamo-dinero-mer-0630` |
| MER-0631 | Escritura de reconocimiento de deuda y prenda sobre participaciones sociales de una SL | `escritura-reconocimiento-deuda-prenda-sobre-mer-0631` |
| MER-0632 | Contrato de servicio de asesoramiento financiero | `contrato-servicio-asesoramiento-financiero-mer-0632` |
| MER-0633 | Contrato de descuento bancario de efectos comerciales | `contrato-descuento-bancario-efectos-comerciales-mer-0633` |
| MER-0634 | Crédito refaccionario (contrato) | `credito-refaccionario-contrato-mer-0634` |
| MER-0635 | Escritura de prenda sobre acciones de una sociedad anónima | `escritura-prenda-sobre-acciones-sociedad-anonima-mer-0635` |
| MER-0636 | Contrato de prenda sobre mercancías y acciones | `contrato-prenda-sobre-mercancias-acciones-mer-0636` |
| MER-0637 | Contrato de línea de avales bancarios | `contrato-linea-avales-bancarios-mer-0637` |
| MER-0638 | Contrato de contraaval entre la entidad avalista y el avalado | `contrato-contraaval-entre-entidad-avalista-avalado-mer-0638` |
| MER-0639 | Contrato de préstamo participativo como fondos propios del prestatario | `contrato-prestamo-participativo-como-fondos-propios-mer-0639` |
| MER-0640 | Contrato de alquiler de cajas de seguridad bancarias | `contrato-alquiler-cajas-seguridad-bancarias-mer-0640` |
| MER-0641 | Contrato de tarjeta de crédito, débito o monedero | `contrato-tarjeta-credito-debito-monedero-mer-0641` |
| MER-0642 | Contrato de préstamo mercantil garantizado con prenda de acciones | `contrato-prestamo-mercantil-garantizado-prenda-acciones-mer-0642` |
| MER-0643 | Escritura de hipoteca naval | `escritura-hipoteca-naval-mer-0643` |
| MER-0644 | Contrato de cuenta corriente bancaria con condiciones generales | `contrato-cuenta-corriente-bancaria-condiciones-mer-0644` |
| MER-0645 | Contrato de depósito bancario a plazo fijo | `contrato-deposito-bancario-plazo-fijo-mer-0645` |
| MER-0646 | Comunicación al banco del uso indebido de una tarjeta por un tercero no autorizado | `comunicacion-banco-uso-indebido-tarjeta-tercero-no-mer-0646` |
| MER-0647 | Crédito al consumo (contrato) | `credito-consumo-contrato-mer-0647` |
| MER-0648 | Contrato de préstamo de valores | `contrato-prestamo-valores-mer-0648` |
| MER-0649 | Escritura de préstamo hipotecario a interés variable | `escritura-prestamo-hipotecario-interes-variable-mer-0649` |
| MER-0650 | Contrato de depósito en garantía o cuenta escrow | `contrato-deposito-garantia-cuenta-escrow-mer-0650` |
| MER-0651 | Leasing de equipos informáticos (contrato) | `leasing-equipos-informaticos-contrato-mer-0651` |
| MER-0652 | Contrato de renting de bienes (modelo general) | `contrato-renting-bienes-modelo-general-mer-0652` |
| MER-0653 | Contrato de intermediación para obtener o modificar créditos, préstamos y servicios financieros | `contrato-intermediacion-obtener-modificar-creditos-mer-0653` |
| MER-0654 | Acuerdo de prenda sobre un crédito o deuda | `acuerdo-prenda-sobre-credito-deuda-mer-0654` |
| MER-0655 | Solicitud de apertura de crédito documentario | `solicitud-apertura-credito-documentario-mer-0655` |
| MER-0656 | Carta de garantía bancaria a primer requerimiento (modelo) | `carta-garantia-bancaria-primer-requerimiento-modelo-mer-0656` |
| MER-0657 | Garantía a primer requerimiento (contrato) | `garantia-primer-requerimiento-contrato-mer-0657` |
| MER-0658 | Contrato de afianzamiento de un préstamo | `contrato-afianzamiento-prestamo-mer-0658` |
| MER-0659 | Escritura de hipoteca mobiliaria sobre un establecimiento mercantil | `escritura-hipoteca-mobiliaria-sobre-establecimiento-mer-0659` |
| MER-0660 | Contrato de cesión de créditos | `contrato-cesion-creditos-mer-0660` |
| MER-0661 | Póliza de crédito para la negociación o el descuento de documentos | `poliza-credito-negociacion-descuento-documentos-mer-0661` |
| MER-0662 | Contrato de préstamo del vendedor para financiar al comprador de bienes muebles | `contrato-prestamo-vendedor-financiar-comprador-bienes-mer-0662` |
| MER-0663 | Solicitud de autorización de una oferta pública de adquisición de valores | `solicitud-autorizacion-oferta-publica-adquisicion-mer-0663` |
| MER-0664 | Anuncio previo de una oferta pública de adquisición de valores | `anuncio-previo-oferta-publica-adquisicion-valores-mer-0664` |
| MER-0665 | Contrato de crédito en cuenta corriente con reconocimiento de deuda | `contrato-credito-cuenta-corriente-reconocimiento-deuda-mer-0665` |
| MER-0666 | Contenido del folleto informativo de una oferta de venta de acciones | `contenido-folleto-informativo-oferta-venta-acciones-mer-0666` |
| MER-0667 | Contrato tipo de depósito y administración de valores en títulos o anotaciones en cuenta | `contrato-tipo-deposito-administracion-valores-titulos-mer-0667` |
| MER-0668 | Contrato entre miembro del mercado y cliente para operar en el mercado de valores | `contrato-entre-miembro-mercado-cliente-operar-mercado-mer-0668` |
| MER-0669 | Contrato mercantil de cuenta corriente | `contrato-mercantil-cuenta-corriente-mer-0669` |
| MER-0670 | Contrato mercantil de depósito bancario | `contrato-mercantil-deposito-bancario-mer-0670` |
| MER-0671 | Custodia y administración de valores (contrato) | `custodia-administracion-valores-contrato-mer-0671` |
| MER-0672 | Carta de patrocinio o confort letter a favor de una filial | `carta-patrocinio-confort-letter-favor-filial-mer-0672` |
| MER-0673 | Contrato de gestión discrecional de carteras de inversión | `contrato-gestion-discrecional-carteras-inversion-mer-0673` |
| MER-0674 | Contrato de prenda sobre un seguro de vida | `contrato-prenda-sobre-seguro-vida-mer-0674` |
| MER-0675 | Contrato de liquidez sobre acciones propias | `contrato-liquidez-sobre-acciones-propias-mer-0675` |
| MER-0676 | Escritura de hipoteca mobiliaria sobre una patente | `escritura-hipoteca-mobiliaria-sobre-patente-mer-0676` |
| MER-0677 | Escritura de hipoteca mobiliaria sobre derechos de propiedad intelectual | `escritura-hipoteca-mobiliaria-sobre-derechos-propiedad-mer-0677` |
| MER-0678 | Contrato de prenda con entrega de la posesión al acreedor | `contrato-prenda-entrega-posesion-acreedor-mer-0678` |
| MER-0679 | Contrato de fianza en garantía de una deuda | `contrato-fianza-garantia-deuda-mer-0679` |
| MER-0680 | Contrato de préstamo entre empresarios | `contrato-prestamo-entre-empresarios-mer-0680` |
| MER-0681 | Contrato de arrendamiento financiero con opción de compra (leasing) | `contrato-arrendamiento-financiero-opcion-compra-leasing-mer-0681` |
| MER-0682 | Escritura de hipoteca de máximo en garantía de obligaciones futuras | `escritura-hipoteca-maximo-garantia-obligaciones-futuras-mer-0682` |
| MER-0683 | Contrato de préstamo garantizado con hipoteca | `contrato-prestamo-garantizado-hipoteca-mer-0683` |
| MER-0684 | Contrato de prenda sin desplazamiento de la posesión | `contrato-prenda-sin-desplazamiento-posesion-mer-0684` |
| MER-0685 | Contrato de constitución de una garantía pignoraticia | `contrato-constitucion-garantia-pignoraticia-mer-0685` |

## Privacidad

Ver `PRIVACY.md`.

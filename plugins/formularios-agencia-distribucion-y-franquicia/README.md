# Agencia, distribución, franquicia y colaboración entre empresas

> Plugin de Claude Code `formularios-agencia-distribucion-y-franquicia` · **34 formularios** · Mercantil · normativa revisada el 24-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para los contratos de colaboración comercial: agencia (Ley 12/1992), distribución exclusiva y selectiva, concesión, franquicia, comisión, patrocinio, alianzas y joint ventures, y las reclamaciones por indemnización de clientela o por resolución.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 34 está al final):

- **Contratos, pactos y cláusulas** (32). Por ejemplo: Contrato de representación de un futbolista profesional por su agente; Contrato de colaboración mercantil para la captación de clientes potenciales (leads); Contrato de agencia o representación comercial.
- **Escritos de trámite y otros** (2). Por ejemplo: Alianza estratégica entre una “startup” tecnológica y una empresa (contrato); Franquicia de producción, distribución y servicios (contrato).

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Contrato de agencia con exclusiva por zona»
   - «Contrato de franquicia con canon de entrada y royalties»
   - «Reclamación de la indemnización por clientela al terminar la agencia»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-agencia-distribucion-y-franquicia:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-agencia-distribucion-y-franquicia:contrato-representacion-futbolista-profesional-agente-mer-0479`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 1.911 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-agencia-distribucion-y-franquicia@formularios-juridicos-mercantil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-mercantil-espana
/plugin install formularios-agencia-distribucion-y-franquicia@formularios-juridicos-mercantil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-agencia-distribucion-y-franquicia.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (34)

| Código | Formulario | Skill |
|---|---|---|
| MER-0479 | Contrato de representación de un futbolista profesional por su agente | `contrato-representacion-futbolista-profesional-agente-mer-0479` |
| MER-0480 | Contrato de colaboración mercantil para la captación de clientes potenciales (leads) | `contrato-colaboracion-mercantil-captacion-clientes-mer-0480` |
| MER-0481 | Alianza estratégica entre una “startup” tecnológica y una empresa (contrato) | `alianza-estrategica-entre-startup-tecnologica-empresa-mer-0481` |
| MER-0482 | Contrato de agencia o representación comercial | `contrato-agencia-representacion-comercial-mer-0482` |
| MER-0483 | Contrato de joint venture entre empresas | `contrato-joint-venture-entre-empresas-mer-0483` |
| MER-0484 | Contrato de comercialización de marca o merchandising | `contrato-comercializacion-marca-merchandising-mer-0484` |
| MER-0485 | Contrato de cesión de una cartera de clientes | `contrato-cesion-cartera-clientes-mer-0485` |
| MER-0486 | Contrato de comisión mercantil con o sin garantía del comisionista | `contrato-comision-mercantil-sin-garantia-comisionista-mer-0486` |
| MER-0487 | Cláusulas específicas para el contrato de mediación en la venta | `clausulas-especificas-contrato-mediacion-venta-mer-0487` |
| MER-0488 | Cláusulas específicas para el contrato de mediación inmobiliaria | `clausulas-especificas-contrato-mediacion-inmobiliaria-mer-0488` |
| MER-0489 | Franquicia de producción, distribución y servicios (contrato) | `franquicia-produccion-distribucion-servicios-contrato-mer-0489` |
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

## Privacidad

Ver `PRIVACY.md`.

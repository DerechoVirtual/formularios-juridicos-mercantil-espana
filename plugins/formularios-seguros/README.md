# Seguros: pólizas, coberturas y reclamaciones

> Plugin de Claude Code `formularios-seguros` · **11 formularios** · Mercantil · normativa revisada el 24-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para el contrato de seguro: pólizas (vida, responsabilidad civil, defensa jurídica…), declaraciones del asegurado, comunicación del siniestro y reclamaciones a la aseguradora conforme a la Ley de Contrato de Seguro.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 11 está al final):

- **Contratos, pactos y cláusulas** (9). Por ejemplo: Póliza de seguro de transporte marítimo de mercancías; Póliza de seguro de vida con condiciones particulares; Póliza de seguro de responsabilidad civil con condiciones particulares.
- **Escritos de trámite y otros** (2). Por ejemplo: Seguro de vida entera mixto de fallecimiento y supervivencia con garantías complementarias; Seguro de vida temporal de fallecimiento con garantías complementarias.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Póliza de seguro de responsabilidad civil profesional»
   - «Comunicación del siniestro a la aseguradora»
   - «Reclamación a la aseguradora por rechazo del siniestro»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-seguros:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-seguros:poliza-seguro-transporte-maritimo-mercancias-mer-0686`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 681 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-seguros@formularios-juridicos-mercantil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-mercantil-espana
/plugin install formularios-seguros@formularios-juridicos-mercantil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-seguros.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (11)

| Código | Formulario | Skill |
|---|---|---|
| MER-0686 | Póliza de seguro de transporte marítimo de mercancías | `poliza-seguro-transporte-maritimo-mercancias-mer-0686` |
| MER-0687 | Póliza de seguro de vida con condiciones particulares | `poliza-seguro-vida-condiciones-particulares-mer-0687` |
| MER-0688 | Póliza de seguro de responsabilidad civil con condiciones particulares | `poliza-seguro-responsabilidad-civil-condiciones-mer-0688` |
| MER-0689 | Contrato de apoderamiento a una agencia de suscripción de seguros | `contrato-apoderamiento-agencia-suscripcion-seguros-mer-0689` |
| MER-0690 | Póliza de seguro de responsabilidad civil de corredores de seguros | `poliza-seguro-responsabilidad-civil-corredores-seguros-mer-0690` |
| MER-0691 | Póliza de seguro de transporte terrestre de mercancías (modelo) | `poliza-seguro-transporte-terrestre-mercancias-modelo-mer-0691` |
| MER-0692 | Póliza de seguro de responsabilidad civil de procuradores | `poliza-seguro-responsabilidad-civil-procuradores-mer-0692` |
| MER-0693 | Seguro de vida entera mixto de fallecimiento y supervivencia con garantías complementarias | `seguro-vida-entera-mixto-fallecimiento-supervivencia-mer-0693` |
| MER-0694 | Condiciones generales del seguro de accidentes | `condiciones-generales-seguro-accidentes-mer-0694` |
| MER-0695 | Seguro de vida temporal de fallecimiento con garantías complementarias | `seguro-vida-temporal-fallecimiento-garantias-mer-0695` |
| MER-0696 | Póliza tipo de seguro multirriesgo del hogar | `poliza-tipo-seguro-multirriesgo-hogar-mer-0696` |

## Privacidad

Ver `PRIVACY.md`.

# Fusiones, escisiones y transformaciones de sociedades

> Plugin de Claude Code `formularios-fusiones-y-escisiones` · **55 formularios** · Mercantil · normativa revisada el 24-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para las modificaciones estructurales del Real Decreto-ley 5/2023: proyectos comunes de fusión y escisión, acuerdos de junta, anuncios, informes a socios y trabajadores, escrituras de fusión, escisión, transformación y cesión global, y la defensa de acreedores y socios.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 55 está al final):

- **Contratos, pactos y cláusulas** (13). Por ejemplo: Acuerdo de transformación de SL en SA con patrimonio dinerario y no dinerario; Acuerdo unánime de escisión parcial de una SL con creación de nueva SL con la parte escindida; Acuerdo de junta de la sociedad beneficiaria que aprueba la escisión.
- **Estatutos, actas, certificaciones y escrituras** (31). Por ejemplo: Proyecto de cesión global de activo y pasivo de una SL o SA; Acta de junta universal que acuerda la cesión global de activo y pasivo de una SL o SA; Proyecto de escisión parcial con traspaso a una sociedad ya existente (escisión-absorción).
- **Comunicaciones, requerimientos y cartas** (7). Por ejemplo: Solicitud de depósito del proyecto de escisión en el Registro Mercantil; Solicitud de experto que fije la compensación al socio perjudicado por el tipo de canje en la fusión; Solicitud de expertos independientes para informar sobre el proyecto de fusión de una SA.
- **Escritos de trámite y otros** (4). Por ejemplo: Escrito de adhesión al acuerdo de transformación por socios que asumen responsabilidad personal; Instancia al Registro Mercantil de experto independiente para la transformación de SL en SA; Escrito de adhesión de socios a la transformación de una SA en sociedad colectiva o comanditaria.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Proyecto común de fusión por absorción de una SL íntegramente participada»
   - «Escritura de escisión parcial con creación de nueva sociedad»
   - «Acuerdo de transformación de una SL en SA»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-fusiones-y-escisiones:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-fusiones-y-escisiones:proyecto-cesion-global-activo-pasivo-sl-sa-mer-0311`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 2.978 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-fusiones-y-escisiones@formularios-juridicos-mercantil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-mercantil-espana
/plugin install formularios-fusiones-y-escisiones@formularios-juridicos-mercantil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-fusiones-y-escisiones.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (55)

| Código | Formulario | Skill |
|---|---|---|
| MER-0311 | Proyecto de cesión global de activo y pasivo de una SL o SA | `proyecto-cesion-global-activo-pasivo-sl-sa-mer-0311` |
| MER-0312 | Acta de junta universal que acuerda la cesión global de activo y pasivo de una SL o SA | `acta-junta-universal-acuerda-cesion-global-activo-mer-0312` |
| MER-0313 | Acuerdo de transformación de SL en SA con patrimonio dinerario y no dinerario | `acuerdo-transformacion-sl-sa-patrimonio-dinerario-no-mer-0313` |
| MER-0314 | Proyecto de escisión parcial con traspaso a una sociedad ya existente (escisión-absorción) | `proyecto-escision-parcial-traspaso-sociedad-ya-mer-0314` |
| MER-0315 | Acuerdo unánime de escisión parcial de una SL con creación de nueva SL con la parte escindida | `acuerdo-unanime-escision-parcial-sl-creacion-nueva-sl-mer-0315` |
| MER-0316 | Proyecto de segregación a favor de una sociedad ya existente | `proyecto-segregacion-favor-sociedad-ya-existente-mer-0316` |
| MER-0317 | Proyecto de escisión parcial de una SL con creación de una nueva SA | `proyecto-escision-parcial-sl-creacion-nueva-sa-mer-0317` |
| MER-0318 | Solicitud de depósito del proyecto de escisión en el Registro Mercantil | `solicitud-deposito-proyecto-escision-registro-mercantil-mer-0318` |
| MER-0319 | Proyecto de segregación a favor de una sociedad de nueva creación | `proyecto-segregacion-favor-sociedad-nueva-creacion-mer-0319` |
| MER-0320 | Proyecto de escisión total de una SL o SA | `proyecto-escision-total-sl-sa-mer-0320` |
| MER-0321 | Proyecto de escisión parcial con constitución de una nueva sociedad | `proyecto-escision-parcial-constitucion-nueva-sociedad-mer-0321` |
| MER-0322 | Acuerdo de junta de la sociedad beneficiaria que aprueba la escisión | `acuerdo-junta-sociedad-beneficiaria-aprueba-escision-mer-0322` |
| MER-0323 | Anuncio de publicación del acuerdo de escisión | `anuncio-publicacion-acuerdo-escision-mer-0323` |
| MER-0324 | Acuerdo de escisión parcial de SL con nueva SL beneficiaria y aprobación del proyecto | `acuerdo-escision-parcial-sl-nueva-sl-beneficiaria-mer-0324` |
| MER-0325 | Escritura pública de escisión total de una SL o SA | `escritura-publica-escision-total-sl-sa-mer-0325` |
| MER-0326 | Acuerdo del consejo de administración que aprueba el proyecto de escisión | `acuerdo-consejo-administracion-aprueba-proyecto-mer-0326` |
| MER-0327 | Anuncio de convocatoria de junta general para acordar la escisión | `anuncio-convocatoria-junta-general-acordar-escision-mer-0327` |
| MER-0328 | Escritura pública de escisión parcial de una SL o SA | `escritura-publica-escision-parcial-sl-sa-mer-0328` |
| MER-0329 | Acuerdo de junta de la sociedad escindida que aprueba la escisión total o parcial | `acuerdo-junta-sociedad-escindida-aprueba-escision-mer-0329` |
| MER-0330 | Solicitud de experto que fije la compensación al socio perjudicado por el tipo de canje en la fusión | `solicitud-experto-fije-compensacion-socio-perjudicado-mer-0330` |
| MER-0331 | Acuerdo del consejo de administración que aprueba el proyecto de fusión por absorción | `acuerdo-consejo-administracion-aprueba-proyecto-fusion-mer-0331` |
| MER-0332 | Escritura pública de fusión por absorción de SL o SA | `escritura-publica-fusion-absorcion-sl-sa-mer-0332` |
| MER-0333 | Escritura pública de fusión mediante constitución de una nueva sociedad | `escritura-publica-fusion-mediante-constitucion-nueva-mer-0333` |
| MER-0334 | Anuncio de publicación del acuerdo de fusión | `anuncio-publicacion-acuerdo-fusion-mer-0334` |
| MER-0335 | Anuncio de convocatoria de junta general para acordar la fusión | `anuncio-convocatoria-junta-general-acordar-fusion-mer-0335` |
| MER-0336 | Proyecto de fusión mediante constitución de una nueva sociedad | `proyecto-fusion-mediante-constitucion-nueva-sociedad-mer-0336` |
| MER-0337 | Solicitud de expertos independientes para informar sobre el proyecto de fusión de una SA | `solicitud-expertos-independientes-informar-sobre-mer-0337` |
| MER-0338 | Informe de los administradores sobre el proyecto de fusión | `informe-administradores-sobre-proyecto-fusion-mer-0338` |
| MER-0339 | Proyecto de fusión por absorción de dos sociedades | `proyecto-fusion-absorcion-dos-sociedades-mer-0339` |
| MER-0340 | Solicitud de depósito del proyecto de fusión en el Registro Mercantil | `solicitud-deposito-proyecto-fusion-registro-mercantil-mer-0340` |
| MER-0341 | Acuerdo de junta de la sociedad absorbente que aprueba la fusión | `acuerdo-junta-sociedad-absorbente-aprueba-fusion-mer-0341` |
| MER-0342 | Acuerdo de junta de la sociedad absorbida que aprueba la fusión | `acuerdo-junta-sociedad-absorbida-aprueba-fusion-mer-0342` |
| MER-0343 | Escrito de adhesión al acuerdo de transformación por socios que asumen responsabilidad personal | `escrito-adhesion-acuerdo-transformacion-socios-asumen-mer-0343` |
| MER-0344 | Anuncio o comunicación individual del acuerdo de transformación de la sociedad | `anuncio-comunicacion-individual-acuerdo-transformacion-mer-0344` |
| MER-0345 | Escritura pública de transformación de una sociedad civil en sociedad limitada | `escritura-publica-transformacion-sociedad-civil-mer-0345` |
| MER-0346 | Acuerdo de transformación de una SL en agrupación de interés económico | `acuerdo-transformacion-sl-agrupacion-interes-economico-mer-0346` |
| MER-0347 | Acuerdo de transformación de una SA en SL | `acuerdo-transformacion-sa-sl-mer-0347` |
| MER-0348 | Acuerdo de transformación de una SL en sociedad colectiva o comanditaria | `acuerdo-transformacion-sl-sociedad-colectiva-mer-0348` |
| MER-0349 | Acuerdo de transformación de una SL en sociedad cooperativa | `acuerdo-transformacion-sl-sociedad-cooperativa-mer-0349` |
| MER-0350 | Escritura pública de transformación de una SA en SL | `escritura-publica-transformacion-sa-sl-mer-0350` |
| MER-0351 | Escritura pública de transformación de una sociedad colectiva en SA | `escritura-publica-transformacion-sociedad-colectiva-sa-mer-0351` |
| MER-0352 | Escritura pública de transformación de una SL en SA | `escritura-publica-transformacion-sl-sa-mer-0352` |
| MER-0353 | Solicitud de experto único por los administradores de la sociedad que se escinde | `solicitud-experto-unico-administradores-sociedad-mer-0353` |
| MER-0354 | Instancia al Registro Mercantil de experto independiente para la transformación de SL en SA | `instancia-registro-mercantil-experto-independiente-mer-0354` |
| MER-0355 | Escrito de adhesión de socios a la transformación de una SA en sociedad colectiva o comanditaria | `escrito-adhesion-socios-transformacion-sa-sociedad-mer-0355` |
| MER-0356 | Instancia al Registro Mercantil para depositar el proyecto de fusión de una SA | `instancia-registro-mercantil-depositar-proyecto-fusion-mer-0356` |
| MER-0357 | Comunicación a los trabajadores del acuerdo de fusión por absorción | `comunicacion-trabajadores-acuerdo-fusion-absorcion-mer-0357` |
| MER-0358 | Anuncio del acuerdo de fusión especial de sociedad anónima íntegramente participada | `anuncio-acuerdo-fusion-especial-sociedad-anonima-mer-0358` |
| MER-0359 | Carta del consejo de administración que convoca junta para transformar una SL en SA | `carta-consejo-administracion-convoca-junta-transformar-mer-0359` |
| MER-0360 | Certificación del acuerdo de transformación de una SA en SL | `certificacion-acuerdo-transformacion-sa-sl-mer-0360` |
| MER-0361 | Convocatoria de junta para transformar una SA en SL | `convocatoria-junta-transformar-sa-sl-mer-0361` |
| MER-0362 | Anuncio de reducción de capital y transformación de una SA en SL | `anuncio-reduccion-capital-transformacion-sa-sl-mer-0362` |
| MER-0363 | Certificación de reducción de capital de una SA como consecuencia de una escisión | `certificacion-reduccion-capital-sa-como-consecuencia-mer-0363` |
| MER-0364 | Escritura pública de cesión global de activo y pasivo de una SL o SA | `escritura-publica-cesion-global-activo-pasivo-sl-sa-mer-0364` |
| MER-0365 | Certificación del acuerdo de junta sobre cesión global de activo y pasivo de una SL o SA | `certificacion-acuerdo-junta-sobre-cesion-global-activo-mer-0365` |

## Privacidad

Ver `PRIVACY.md`.

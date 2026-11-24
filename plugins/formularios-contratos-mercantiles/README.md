# Contratos mercantiles: compraventa, suministro, transporte y servicios

> Plugin de Claude Code `formularios-contratos-mercantiles` · **105 formularios** · Mercantil · normativa revisada el 24-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para los contratos entre empresas del día a día: compraventa mercantil e internacional, suministro, transporte terrestre, marítimo y aéreo, logística, obra y servicios profesionales, consultoría, publicidad, eventos y turismo, condiciones generales de venta y cláusulas especiales.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 105 está al final):

- **Contratos, pactos y cláusulas** (90). Por ejemplo: Contrato de gestión de un hotel por operador hotelero; Contrato de transporte de mercancías de ejecución continuada; Contrato de reserva de alojamiento turístico.
- **Comunicaciones, requerimientos y cartas** (2). Por ejemplo: Declaración sobre prestación de servicios a terceros; Carta de encargo de un trabajo de auditoría de cuentas.
- **Escritos de trámite y otros** (13). Por ejemplo: Suministro de hidrógeno (contrato); Información precontractual normalizada para contratos de viaje combinado; Información precontractual en la venta fuera del establecimiento mercantil.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Contrato de suministro de mercancías con precio revisable»
   - «Contrato de transporte de mercancías por carretera»
   - «Condiciones generales de venta de una empresa»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-contratos-mercantiles:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-contratos-mercantiles:contrato-gestion-hotel-operador-hotelero-mer-0513`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 5.757 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-contratos-mercantiles@formularios-juridicos-mercantil-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-mercantil-espana
/plugin install formularios-contratos-mercantiles@formularios-juridicos-mercantil-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana/releases/latest/download/formularios-contratos-mercantiles.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (105)

| Código | Formulario | Skill |
|---|---|---|
| MER-0513 | Contrato de gestión de un hotel por operador hotelero | `contrato-gestion-hotel-operador-hotelero-mer-0513` |
| MER-0514 | Contrato de transporte de mercancías de ejecución continuada | `contrato-transporte-mercancias-ejecucion-continuada-mer-0514` |
| MER-0515 | Suministro de hidrógeno (contrato) | `suministro-hidrogeno-contrato-mer-0515` |
| MER-0516 | Contrato de reserva de alojamiento turístico | `contrato-reserva-alojamiento-turistico-mer-0516` |
| MER-0517 | Contrato de dirección integrada de proyecto (project management) en construcción | `contrato-direccion-integrada-proyecto-project-mer-0517` |
| MER-0518 | Contrato de arrendamiento de servicios entre empresarios | `contrato-arrendamiento-servicios-entre-empresarios-mer-0518` |
| MER-0519 | Declaración sobre prestación de servicios a terceros | `declaracion-sobre-prestacion-servicios-terceros-mer-0519` |
| MER-0520 | Información precontractual normalizada para contratos de viaje combinado | `informacion-precontractual-normalizada-contratos-viaje-mer-0520` |
| MER-0521 | Contrato de ingeniería (engineering) para la puesta en marcha de un establecimiento u obra | `contrato-ingenieria-engineering-puesta-marcha-mer-0521` |
| MER-0522 | Contrato de servicios de consultoría empresarial | `contrato-servicios-consultoria-empresarial-mer-0522` |
| MER-0523 | Contrato de transporte marítimo de mercancías por fletamento o conocimiento de embarque | `contrato-transporte-maritimo-mercancias-fletamento-mer-0523` |
| MER-0524 | Contrato de compraventa de una empresa o unidad productiva | `contrato-compraventa-empresa-unidad-productiva-mer-0524` |
| MER-0525 | Contrato de transporte terrestre de mercancías por carretera | `contrato-transporte-terrestre-mercancias-carretera-mer-0525` |
| MER-0526 | Contrato de mudanza de viviendas, locales u oficinas | `contrato-mudanza-viviendas-locales-u-oficinas-mer-0526` |
| MER-0527 | Contrato de ejecución de obra entre empresarios | `contrato-ejecucion-obra-entre-empresarios-mer-0527` |
| MER-0528 | Contrato de compraventa de cosa mueble con cláusulas generales | `contrato-compraventa-cosa-mueble-clausulas-generales-mer-0528` |
| MER-0529 | Contrato de compraventa internacional con consumidores | `contrato-compraventa-internacional-consumidores-mer-0529` |
| MER-0530 | Contrato de servicio de catering o restauración | `contrato-servicio-catering-restauracion-mer-0530` |
| MER-0531 | Contrato de reserva de alojamiento en agroturismo | `contrato-reserva-alojamiento-agroturismo-mer-0531` |
| MER-0532 | Contrato de servicios de handling | `contrato-servicios-handling-mer-0532` |
| MER-0533 | Contrato de compraventa celebrado fuera del establecimiento mercantil | `contrato-compraventa-celebrado-fuera-establecimiento-mer-0533` |
| MER-0534 | Información precontractual en la venta fuera del establecimiento mercantil | `informacion-precontractual-venta-fuera-establecimiento-mer-0534` |
| MER-0535 | Contrato de servicio de banquetes | `contrato-servicio-banquetes-mer-0535` |
| MER-0536 | Contrato de asistencia técnica para el seguimiento y control del proyecto (project monitoring) | `contrato-asistencia-tecnica-seguimiento-control-mer-0536` |
| MER-0537 | Contrato de fletamento parcial de aeronave no regular (split charter) | `contrato-fletamento-parcial-aeronave-no-regular-split-mer-0537` |
| MER-0538 | Contrato de compraventa de cosa futura | `contrato-compraventa-cosa-futura-mer-0538` |
| MER-0539 | Contrato de depósito de mercancías en almacén | `contrato-deposito-mercancias-almacen-mer-0539` |
| MER-0540 | Contrato de compraventa de negocio con arrendamiento del local | `contrato-compraventa-negocio-arrendamiento-local-mer-0540` |
| MER-0541 | Contrato de subcontratación entre contratista y subcontratista | `contrato-subcontratacion-entre-contratista-mer-0541` |
| MER-0542 | Contrato de asesoría fiscal y llevanza de contabilidad | `contrato-asesoria-fiscal-llevanza-contabilidad-mer-0542` |
| MER-0543 | Contrato de prestación de servicios de formación | `contrato-prestacion-servicios-formacion-mer-0543` |
| MER-0544 | Contrato de compraventa internacional entre importador y exportador | `contrato-compraventa-internacional-entre-importador-mer-0544` |
| MER-0545 | Contrato de externalización de servicios (outsourcing) entre empresas | `contrato-externalizacion-servicios-outsourcing-entre-mer-0545` |
| MER-0546 | Contrato de ingeniería operativa entre cliente y empresa ejecutante | `contrato-ingenieria-operativa-entre-cliente-empresa-mer-0546` |
| MER-0547 | Contrato de compraventa mercantil con entrega y pago aplazados (versión abreviada) | `contrato-compraventa-mercantil-entrega-pago-aplazados-mer-0547` |
| MER-0548 | Formulario de desistimiento aparte para aprovechamiento por turno y productos vacacionales | `formulario-desistimiento-aparte-aprovechamiento-turno-mer-0548` |
| MER-0549 | Información normalizada previa para contratos de aprovechamiento por turno de uso turístico | `informacion-normalizada-previa-contratos-mer-0549` |
| MER-0550 | Compraventa mercantil (al contado versión abreviada) (contrato) | `compraventa-mercantil-contado-version-abreviada-mer-0550` |
| MER-0551 | Información normalizada previa para contratos de productos vacacionales de larga duración | `informacion-normalizada-previa-contratos-productos-mer-0551` |
| MER-0552 | Contrato de realización de campañas publicitarias | `contrato-realizacion-campanas-publicitarias-mer-0552` |
| MER-0553 | Contrato de servicios profesionales de arquitectura | `contrato-servicios-profesionales-arquitectura-mer-0553` |
| MER-0554 | Mantenimiento de piscinas (contrato) | `mantenimiento-piscinas-contrato-mer-0554` |
| MER-0555 | Contrato de servicios de asesoría fiscal y contable | `contrato-servicios-asesoria-fiscal-contable-mer-0555` |
| MER-0556 | Mantenimiento de instalaciones frigoríficas (contrato) | `mantenimiento-instalaciones-frigorificas-contrato-mer-0556` |
| MER-0557 | Contrato de suministro de productos alimentarios | `contrato-suministro-productos-alimentarios-mer-0557` |
| MER-0558 | Contrato de servicios de limpieza | `contrato-servicios-limpieza-mer-0558` |
| MER-0559 | Suministro de agua potable (contrato) | `suministro-agua-potable-contrato-mer-0559` |
| MER-0560 | Contrato de suministro de gasóleo | `contrato-suministro-gasoleo-mer-0560` |
| MER-0561 | Contrato de servicios de asesoría laboral | `contrato-servicios-asesoria-laboral-mer-0561` |
| MER-0562 | Contrato de enseñanza de conducción con autoescuela | `contrato-ensenanza-conduccion-autoescuela-mer-0562` |
| MER-0563 | Enseñanza no reglada (contrato) | `ensenanza-no-reglada-contrato-mer-0563` |
| MER-0564 | Contrato de servicios de jardinería | `contrato-servicios-jardineria-mer-0564` |
| MER-0565 | Contrato de auditoría de las cuentas anuales de una sociedad mercantil | `contrato-auditoria-cuentas-anuales-sociedad-mercantil-mer-0565` |
| MER-0566 | Carta de encargo de un trabajo de auditoría de cuentas | `carta-encargo-trabajo-auditoria-cuentas-mer-0566` |
| MER-0567 | Contrato de servicios de intermediación en adopción internacional | `contrato-servicios-intermediacion-adopcion-mer-0567` |
| MER-0568 | Contrato de restauración o reparación de una obra de arte | `contrato-restauracion-reparacion-obra-arte-mer-0568` |
| MER-0569 | Condiciones del contrato de pasaje marítimo | `condiciones-contrato-pasaje-maritimo-mer-0569` |
| MER-0570 | Cláusulas especiales de compraventa sobre pago, garantías, representación y compra a prueba | `clausulas-especiales-compraventa-sobre-pago-garantias-mer-0570` |
| MER-0571 | Contrato de compraventa con expedición de la mercancía (versión abreviada) | `contrato-compraventa-expedicion-mercancia-version-mer-0571` |
| MER-0572 | Resguardo de depósito con su matriz | `resguardo-deposito-matriz-mer-0572` |
| MER-0573 | Transporte de viajeros por carretera (contrato) | `transporte-viajeros-carretera-contrato-mer-0573` |
| MER-0574 | Cláusulas habituales de los contratos de transporte marítimo de mercancías | `clausulas-habituales-contratos-transporte-maritimo-mer-0574` |
| MER-0575 | Cláusulas mínimas del contrato de viaje combinado | `clausulas-minimas-contrato-viaje-combinado-mer-0575` |
| MER-0576 | Condiciones del contrato de pasaje aéreo | `condiciones-contrato-pasaje-aereo-mer-0576` |
| MER-0577 | Contrato de viaje combinado para incorporar a los bonos o billetes | `contrato-viaje-combinado-incorporar-bonos-billetes-mer-0577` |
| MER-0578 | Transmisión de derechos de aprovechamiento por turno de bienes inmuebles (contrato) | `transmision-derechos-aprovechamiento-turno-bienes-mer-0578` |
| MER-0579 | Contrato de venta a plazos de bienes muebles | `contrato-venta-plazos-bienes-muebles-mer-0579` |
| MER-0580 | Contrato de depósito de mercancías en almacenes generales | `contrato-deposito-mercancias-almacenes-generales-mer-0580` |
| MER-0581 | Contrato de transporte marítimo internacional de mercancías | `contrato-transporte-maritimo-internacional-mercancias-mer-0581` |
| MER-0582 | Contrato internacional de permuta de bienes | `contrato-internacional-permuta-bienes-mer-0582` |
| MER-0583 | Contrato de transporte de mercancías por carretera en ámbito internacional | `contrato-transporte-mercancias-carretera-ambito-mer-0583` |
| MER-0584 | Contrato de transporte de mercancías por carretera en ámbito nacional | `contrato-transporte-mercancias-carretera-ambito-mer-0584` |
| MER-0585 | Contrato de fletamento de buque | `contrato-fletamento-buque-mer-0585` |
| MER-0586 | Contrato de cesión de espacios publicitarios en un medio de difusión | `contrato-cesion-espacios-publicitarios-medio-difusion-mer-0586` |
| MER-0587 | Contrato de compraventa sujeta a prueba o ensayo previo | `contrato-compraventa-sujeta-prueba-ensayo-previo-mer-0587` |
| MER-0588 | Contrato de venta de un buque | `contrato-venta-buque-mer-0588` |
| MER-0589 | Contrato de encargo de una campaña publicitaria a una agencia creativa | `contrato-encargo-campana-publicitaria-agencia-creativa-mer-0589` |
| MER-0590 | Contrato de compraventa mercantil sobre muestras o calidad conocida | `contrato-compraventa-mercantil-sobre-muestras-calidad-mer-0590` |
| MER-0591 | Contrato de cesión de uso de un stand en un recinto ferial | `contrato-cesion-uso-stand-recinto-ferial-mer-0591` |
| MER-0592 | Condiciones generales de venta de una empresa | `condiciones-generales-venta-empresa-mer-0592` |
| MER-0593 | Contrato de emplazamiento de un soporte publicitario audiovisual | `contrato-emplazamiento-soporte-publicitario-audiovisual-mer-0593` |
| MER-0594 | Contrato de alquiler de un soporte publicitario | `contrato-alquiler-soporte-publicitario-mer-0594` |
| MER-0595 | Contrato de venta de maquinaria industrial | `contrato-venta-maquinaria-industrial-mer-0595` |
| MER-0596 | Contrato general de compraventa mercantil | `contrato-general-compraventa-mercantil-mer-0596` |
| MER-0597 | Contrato de suministro periódico de bienes | `contrato-suministro-periodico-bienes-mer-0597` |
| MER-0598 | Contrato de venta internacional de mercaderías | `contrato-venta-internacional-mercaderias-mer-0598` |
| MER-0599 | Contrato de servicios de asesoría jurídica para una empresa | `contrato-servicios-asesoria-juridica-empresa-mer-0599` |
| MER-0600 | Contrato de externalización de procesos de negocio entre empresas | `contrato-externalizacion-procesos-negocio-entre-mer-0600` |
| MER-0601 | Contrato de prestación de servicios entre empresas | `contrato-prestacion-servicios-entre-empresas-mer-0601` |
| MER-0602 | Contrato de subcontratación de una obra | `contrato-subcontratacion-obra-mer-0602` |
| MER-0603 | Contrato de suministro de alimentos y servicio de catering | `contrato-suministro-alimentos-servicio-catering-mer-0603` |
| MER-0604 | Contrato de creación y difusión de una campaña publicitaria con una agencia | `contrato-creacion-difusion-campana-publicitaria-agencia-mer-0604` |
| MER-0605 | Cláusulas de reparto de responsabilidades laborales y sociales en obra o servicios con subcontrata | `clausulas-reparto-responsabilidades-laborales-sociales-mer-0605` |
| MER-0606 | Contrato mercantil de un actor para interpretar un personaje en una película | `contrato-mercantil-actor-interpretar-personaje-pelicula-mer-0606` |
| MER-0607 | Contrato mercantil de obra o servicios prestados en régimen de teletrabajo | `contrato-mercantil-obra-servicios-prestados-regimen-mer-0607` |
| MER-0608 | Contrato de calificación crediticia (rating) de una emisión de renta fija | `contrato-calificacion-crediticia-rating-emision-renta-mer-0608` |
| MER-0609 | Contrato internacional para fabricar y suministrar materiales y equipos | `contrato-internacional-fabricar-suministrar-materiales-mer-0609` |
| MER-0610 | Contrato internacional para transportar mercancías por ferrocarril | `contrato-internacional-transportar-mercancias-mer-0610` |
| MER-0611 | Contrato internacional de suministro en régimen de exclusividad | `contrato-internacional-suministro-regimen-exclusividad-mer-0611` |
| MER-0612 | Contrato de organización de un concierto | `contrato-organizacion-concierto-mer-0612` |
| MER-0613 | Contrato internacional de servicios logísticos para transporte por carretera | `contrato-internacional-servicios-logisticos-transporte-mer-0613` |
| MER-0614 | Contrato de compraventa de una empresa o negocio en su conjunto | `contrato-compraventa-empresa-negocio-conjunto-mer-0614` |
| MER-0615 | Contrato de subcontratación de obras | `contrato-subcontratacion-obras-mer-0615` |
| MER-0616 | Contrato mercantil de arrendamiento de servicios profesionales | `contrato-mercantil-arrendamiento-servicios-mer-0616` |
| MER-0617 | Contrato de permuta mercantil de bienes muebles | `contrato-permuta-mercantil-bienes-muebles-mer-0617` |

## Privacidad

Ver `PRIVACY.md`.

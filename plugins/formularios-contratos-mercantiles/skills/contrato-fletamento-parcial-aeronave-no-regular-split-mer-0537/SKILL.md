---
name: contrato-fletamento-parcial-aeronave-no-regular-split-mer-0537
description: "Contrato de fletamento parcial de aeronave no regular (split charter). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de fletamento parcial de aeronave no regular (split charter)

> Formulario **MER-0537** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de fletamento parcial de aeronave no regular (split charter)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de fletamento parcial de aeronave no regular (split charter)” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-fletamento-parcial-aeronave-no-regular-split-mer-0537`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (8 veces)
- [ ] NOMBRE DE LA PARTE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AUTORIDAD AERONÁUTICA
- [ ] DIRECCIÓN
- [ ] LEGISLACIÓN APLICABLE
- [ ] PESO MÁXIMO
- [ ] SEDE
- [ ] TAMAÑO / VOLUMEN MÁXIMO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

Se trata del contrato entre el cargador y el exportador para el flete de un avión que no sigue rutas regulares, sino que solo va a destinos donde tienen mercancía para cargar, y cuya carga es completa.

Es un contrato por el cual el propietario de un avión(Fletante)y el propietario de una carga(Fletador)establecen sus obligaciones y responsabilidades respecto a la utilización del avión completo por parte del fletador para realizar su transporte.

La empresa fletante se obliga a proporcionar a la otra parte(Fletadores)un tipo determinado de aeronave situada en el aeropuerto de salida con su propia tripulación, equipada y con combustible, y a mantenerla en perfectas condiciones de navegabilidad durante toda la vigencia del contrato. El fletante no pierde, en ningún momento, la posesión de la aeronave y el personal de operaciones permanece bajo su exclusivo control. Los fletadores tendrán la obligación de pagar el precio del charter y los gastos que se pacten.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero el «Texto del formulario» (al final de este fichero) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea del «Texto del formulario» y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Texto del formulario

Lo que sigue, hasta el final de este fichero, es el formulario tal cual: desde su primera línea hasta la firma.

AIRCRAFT CHARTER AGREEMENT

This CHARTER AGREEMENT entered into by and between [NOMBRE DE LA PARTE] hereinafter known as the "CARRIER";

and

[NOMBRE Y APELLIDOS], in this act represented by [NOMBRE Y APELLIDOS] with office address at [DIRECCIÓN], hereinafter known as the "CHARTERER",

WITNESSETH THAT;

The CARRIER hereby renders under charter, and CHARTERER hereby accepts under charter, one aircraft of the former, under following terms and conditions:

1.Pupose of the Flight:

A. To Carry Cargo
B. Description/Weight of Cargo
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

C. Maximum allowable size/weight

The cargo may not exceed [TAMAÑO / VOLUMEN MÁXIMO] size/volume

The cargo may not exceed [PESO MÁXIMO] weight

2. Date and time charter will be operated:

A. Type of Aircraft:
B. Pilot(s)/Co-Pilot:
C. Destination & Route of Flight:
D. ETD:

Date From ETD to ETA

3. Computation of Estimated Charter Cost

Cost of Flying time per hour [IMPORTE]

Cost of Waiting time per hour [IMPORTE]

Cost of Overnight Fee [IMPORTE]

Pilot Accommodation & Meals [IMPORTE]

Landing Fee [IMPORTE]

Carrier’s Fee [IMPORTE]

Fuel Differential Charge [IMPORTE]

EFT:

EWT:

Total:

3.1 The estimated charter cost shall be paid upon signing of this Aircraft Charter Agreement.

TERMS AND CONDITIONS

1. Basic Agreement.

Charterer and Carrier agree that the following terms and conditions shall be exclusively applicable to this charter and to the cargo, from the point at which Carrier has received the cargo for shipment until the cargo is tendered or made available to the Consignee for delivery, except as otherwise noted herein.

2. Definitions.

In this charter: the term "Carrier" means [NOMBRE DE LA PARTE]; the term "Charterer" means the party identified as such on the face as well as the owner, shipper, Consignee and anyone with right of claim to or through the cargo; the term "Consignee" means the party identified as such by Charterer on the face; the term "cargo" means those items tendered by Charterer to Carrier for transportation which are described on the face and/or on the air waybill.

3. Charter Price.

Charges and Related Provisions.

A. Price. Charterer shall pay Carrier the charter price which is set forth on the face, which shall be deemed irrevocably earned unless transportation hereunder is canceled, in which event the provisions of subsection 4.D., below, shall apply.

B. Layover and Demurrage. The parties shall allow a maximum of two hours layover at the points of origin and destination, and one hour layover at any scheduled stop, for loading and unloading, customs clearance and similar matters, without any additional charge. Layovers in excess of the foregoing and all other delays caused by Charterer and/or the cargo shall be charged to Charterer at the demurrage rate set forth on the face. Such delay shall include, without limitation, unavailability of cargo for loading at the time specified, inadequate or unacceptable packaging, delay in receipt of operational permits, inadequate customs documentation, delay caused by inadequate paperwork, delay in customs clearance (for any reason) and delay during loading or unloading caused by Charterer and/or the cargo.

C. Expenses, Charges and Advances. All fuel, oil, crew salary, crew expense, aircraft maintenance and aircraft landing and handling fees shall be paid by Carrier. All other expenses, charges and costs, including, without limitation, transportation taxes, foreign taxes, levies, non-objection fees, duties, royalties, special or accessorial services (storage, surface transportation, dunnage, bracing, etc.) requested by Charterer or necessary for the cargo, and all other costs in connection with the cargo and/or this charter, shall be paid for by Charterer; any advances or disbursements made by Carrier for Charterer or the cargo shall be promptly reimbursed by Charterer.

D. Payment and Interest. Charterer shall pay Carrier the charter price prior to flight departure. Carrier shall invoice Charterer for all other charges, expenses and advances, with payment due upon presentation of invoice. All payments shall be made without deduction or setoff. Amounts which are due but unpaid shall accrue interest at a rate of one and one-half percent (l1/2%) per month or the highest rate allowed by law, whichever is less, until paid in full.

E. Collection. Lien and Related Rights. Charterer shall remain responsible for all sums due hereunder until fully paid. Carrier shall have a lien which shall survive delivery upon all cargo to secure full payment of amounts due under this charter. In the event any such amounts are not paid, Carrier may enforce its lien and at any time dispose of or sell the cargo or any portion thereof, publicly or privately and without notice to Charterer, and may collect sums due from the proceeds. Charterer shall pay for or reimburse Carrier for its costs related to any efforts to collect amounts due hereunder, including legal fees and costs. Charterer additionally grants Carrier a consensual lien on all cargo subsequently carried by Carrier for Charterer to secure payment of sums due under this charter.

4. Carrier’s Rights and Responsibilities.

A. Exclusive Control and Performance. Carrier shall have exclusive direction and control over the aircraft, its crew and all cargo on board. Carrier agrees to undertake to provide the transportation services with due diligence but does not guarantee any speed, route, departure or arrival time or date. Carrier shall be entitled to subcontract the whole or any part of the transportation services, and each such subcontractor shall be entitled to all rights, benefits, defenses, limitations and/or immunities available to Carrier pursuant to this charter.

B. Liberties. Carrier shall be at liberty to: make interim stops for fuel, supplies, repairs and to receive and discharge cargo for others; utilize the payload on positioning and depositioning flights and any available payload not utilized by Charterer, and the revenue generated from the transportation of such items, shall be retained by Carrier and shall not reduce or offset the charter price; take whatever steps and do whatever actions it deems necessary for the protection of itself, the aircraft, pilots and passengers, including, without limitation, the substitution of another aircraft, making collect communications, disposing of cargo without instruction and/or tendering transportation of the cargo to other carrier(s). Carrier shall also be excused from delay or inability to perform caused by circumstances beyond its reasonable control.

C. Right of Refusal. Carrier may refuse carriage of cargo which, in its sole discretion: is improperly packaged; is not suitable for carriage; is hazardous/dangerous; exceeds the operational capacity of the aircraft; cannot be loaded within the allotted space; cannot be transported in accordance with applicable laws and regulations; or, has an aggregated value in excess of [IMPORTE] with no prior special arrangements having been made.

D. Cancellation. Transportation shall be canceled if Charterer fails to deliver the cargo to the aircraft at the point of departure within three hours of the scheduled flight departure time. If transportation is canceled pursuant to this subsection, Charterer shall pay the following amount to Carrier: if canceled 16 or more days in advance, 20% of the charter price; if canceled between 8 and 15 days in advance, 50% of the charter price; if canceled 7 days or less in advance, 90% of the charter price. The date of intended flight departure shall be used for calculating how long in advance cancellation occurred. Said amount is not to be deemed a penalty, but rather shall be paid to Carrier for Carrier’s actual expense and damage caused by cancellation.

E. Termination. Carrier may terminate this charter without notice if Charterer breaches any provision hereof or if Carrier, in its sole discretion, determines that the transportation of the cargo would be unsafe or in violation of any applicable law, rule or regulation. In the event of cancellation pursuant to this subsection, the cargo shall be returned to Charterer, its agent or assign, at Charterer’s sole cost and expense, at the point of receipt by Carrier.

5. Charterer’s Rights and Responsibilities.

A. Air Waybill and Disclosure. Prior to flight departure, Charterer is required to complete and deliver to Carrier an air waybill setting forth: the date/place of completion; places of departure/interim stops/destination; name/address of consignee; precise nature of the cargo; number of packages; method of packing; particular marks/numbers used; weight/quantity/volume/dimensions of cargo; actual condition of cargo and its packaging at time of tender for shipment; and, any special circumstances/conditions/handling information. Charterer warrants the completeness and accuracy of the foregoing information; Carrier shall not be responsible for checking or confirming Charterer’s disclosures, and shall be entitled to rely upon the completeness and accuracy thereof. The air waybill shall be considered a receipt only and not the contract for transportation of the cargo. In the event of any conflict between this charter and the air waybill, this charter shall prevail.

B. Hazardous Cargo. Charterer shall not tender to Carrier any cargo which is hazardous or dangerous without prior notification to and the assent of Carrier, verbal or otherwise, with Charterer to be responsible for a full disclosure of the nature of the cargo, any hazards/dangers associated therewith, special handling/packing/ packaging, and compliance with all regulatory requirements. Notwithstanding acceptance of such cargo by Carrier for shipment, Charterer shall remain responsible for all loss and damage resulting from the hazardous/dangerous character of said cargo, whether to Carrier and/or its employees and property or to other persons or property.

C. Preparation and Delivery of Cargo. Charterer shall deliver the cargo to Carrier at the time and place indicated on the face, properly prepared, labeled, securely packaged, loaded and ready for transportation by aircraft. Upon request by Carrier, Charterer shall also provide skids or bases to reduce the floor-bearing weight of individual pieces, and such skids/bases shall be included in Charterer’s disclosure to Carrier as to the weight of cargo to be transported.

D. Couriers. Upon approval by Carrier (which approval shall not be reasonably withheld), couriers may accompany cargo for the safety and protection thereof in accordance with [AUTORIDAD AERONÁUTICA] regulations and limitations relating to couriers.

E. Other Responsibilities. Charterer shall be responsible for loss or damage to the aircraft or other property aboard the aircraft, including expense, claim, liability and/or suit associated therewith, caused by or attributable to Charterer, its employees and/or the cargo. Charterer shall also be responsible for any other matter allocated to it pursuant to this charter, including loss, damage, expense, claim, liability and/or suit associated therewith, to include all matters not specifically allocated to Carrier. Charterer agrees to indemnify and hold harmless (including legal fees and costs) Carrier of and from the foregoing responsibilities.

6. Liability and Indemnity.

Carrier’s liability with respect to the goods, Charterer, Consignee and/or any other party claiming with respect to the goods and whether for loss, damage, delay, shortage, misdelivery, failure to delivery or otherwise, shall be only as follows:

A. Exceptions. Carrier shall not be liable for loss, damage, delay or other result caused by:
1. perils of the air, fire, acts of war, public enemies, public authorities acting with actual or apparent authority in the premises, authority of law, quarantine, riots, unavailability in whole or part of aircraft fuel, hijacking, sabotage, strikes, civil commotion, hazards or dangers incident to war or nuclear risk or any other circumstance beyond the actual control of Carrier;
2. the act or default of Charterer or Consignee;
3. the nature of the cargo or any defect, characteristic or inherent vice thereof;
4. violation by Charterer or Consignee of any term or condition contained in or incorporated into this charter, including, without limitation, improper packing, securing, marking or addressing, and/or failure to observe any of the terms or conditions relating to shipments not acceptable for transportation or acceptable only under certain conditions;
5. compliance with the delivery provisions from Charterer or noncompliance with special instructions not authorized herein; or
6. shortage of cargo loaded and sealed in containers or other packages by Charterer providing the seal is unbroken at time of delivery and the container or other package retains its basic integrity.
B. Consequential Damages. Carrier shall not be liable for any consequential or special damages of any type howsoever arising, whether loss of income or profits or otherwise and whether or not Carrier had or should have had knowledge that such might occur.
C. Limitation of Liability. Charterer agrees that unless a higher value is declared on the face hereof Carrier’s liability for loss, damage or otherwise with respect to the cargo is limited to fifty cents ($.50) per pound actual weight of the cargo so lost or damaged or actual loss or damage with respect to said cargo, whichever is less.
D. Higher Value. Charterer may declare a higher value for the cargo than the foregoing, in which event such declaration must be inserted by Charterer on the face hereof and Charterer must pay to Carrier seventy five cents ($.75) for each one hundred dollars (D.00) or fraction thereof value declared. In the event of such declaration of higher value and loss, damage or other failure to deliver such cargo, Carrier’s liability for such loss or damage shall be limited to the declared value or the actual loss or damage with respect to said cargo, whichever is less.
E. Delivery in Good Condition. Receipt by the Consignee of the cargo without written notification of damage on the delivery receipt shall be prima facie evidence that the cargo has been delivered to Consignee in the same good condition, count and order as when received by Carrier.
F. Claims. As a condition precedent to recovery against Carrier:
1. The cargo must be carefully inspected at delivery and any loss or damage then evident must be noted on Carrier’s copy of the air waybill.
2. In the event of loss or damage not ascertainable at delivery, written notice thereof must be given to Carrier within fifteen days following delivery, after which time it shall be conclusively presumed the cargo was delivered in the same condition and count as when received by Carrier.
3. In the event of cargo which has been lost or otherwise not delivered, Carrier must be given written notice of said loss or failure to deliver within 15 days from the date upon which the cargo should have been delivered.
4. Carrier shall have a reasonable opportunity to inspect the cargo, packing and packaging in the same condition as received by Charterer and/or Consignee and before alteration or destruction.
5. Written claim for loss or damage specifying the particulars thereof must be filed with Carrier within nine months of the date of delivery or date by which the cargo should be been delivered.
6. Suit against Carrier must be filed two years following date of delivery of the cargo or date by which the cargo should have been delivered.
7. There shall be no recovery against Carrier until the charter price and all other sums due Carrier pursuant to this charter have been paid in full.
8. International Flights. In the event of an international shipment, the transportation of the cargo and Carrier’s liability hereunder shall be subject to international laws and protocols; any provision hereof contrary to laws and protocols shall be deemed superseded and amended by the applicable provision(s) of said convention, but all remaining terms and conditions shall continue to be applicable.
9. Law, Jurisdiction and Legal Fees. This charter shall be governed by the laws of [LEGISLACIÓN APLICABLE], and any dispute arising out of or in connection with this charter and/or the transportation of the cargo hereunder shall be brought in court located in [SEDE], with the substantially prevailing party to recover its reasonable legal fees and costs.
10. Integration and Headings. This document, the air waybill and any agreed attachments hereto constitute the entire agreement between the parties with respect to the transportation of the cargo, superseding and negating all prior or contemporaneous agreements, written and oral. This agreement may not be modified or amended except by a writing signed by both parties. The headings used herein are for convenience only, are not substantive and may not be used to interpret the agreement between the parties.

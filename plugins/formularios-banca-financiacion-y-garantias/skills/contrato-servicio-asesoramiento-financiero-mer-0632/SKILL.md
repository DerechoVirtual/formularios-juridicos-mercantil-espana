---
name: contrato-servicio-asesoramiento-financiero-mer-0632
description: "Contrato de servicio de asesoramiento financiero. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicio de asesoramiento financiero

> Formulario **MER-0632** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicio de asesoramiento financiero» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicio de asesoramiento financiero” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-servicio-asesoramiento-financiero-mer-0632`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] PORCENTAJE (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] MES
- [ ] Nº
- [ ] NÚMERO
- [ ] PROVINCIA

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

- Ninguna.

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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [DÍA] de [MES] de [AÑO]

REUNIDOS

EXPONEN

I. Que la ASESORA es una empresa de asesoramiento financiero inscrita en el correspondiente registro de la Comisión Nacional del Mercado de Valores con el número

Que el CLIENTE está interesado en suscribir el presente contrato con la ASESORA para optimizar sus inversiones financieras, a cuyo efecto ha abierto la cuenta de valores asociada núm [NÚMERO], con la relación de activos que se describen en el Anexo, y la cuenta corriente asociada núm

Que reconociéndose mutuamente las partes, según intervienen, la capacidad legal necesaria a los efectos de este CONTRATO DE ASESORAMIENTO FINANCIERO, en la representación expresada, siendo responsables de la veracidad de sus manifestaciones, y de forma libre, espontánea y de mutuo acuerdo, convienen formalizar el contrato con arreglo a las siguientes

CLAÚSULAS

Objeto

La ASESORA prestará al CLIENTE el servicio de asesoramiento en materia de inversión mediante recomendaciones personalizadas, sea a petición del CLIENTE o por iniciativa de la ASESORA, con respecto a una o más operaciones relativas a instrumentos financieros.

A tal efecto, la ASESORA, ponderando las circunstancias de mercado, asesorará al CLIENTE sobre las decisiones de inversión (operaciones de compra, venta, suscripción o reembolso de valores), tanto nacionales como internacionales, y sobre la aparición de nuevos productos financieros que puedan ser de su interés, con el fin de conseguir la mayor rentabilidad del conjunto de instrumentos financieros del CLIENTE.

El asesoramiento objeto de este contrato se limitará exclusivamente a los valores e instrumentos financieros que integran la cartera del CLIENTE en la cuenta de valores descrita en el expositivo II.

Retribución

La ASESORA tendrá derecho a percibir, como contraprestación por sus servicios una comisión fija del [PORCENTAJE] anual del efectivo de la cartera asesorada con un mínimo de [IMPORTE] euros anuales.

Asimismo tendrá derecho a percibir una comisión variable anual sobre la revalorización de la cartera asesorada del [PORCENTAJE] % de los resultados netos obtenidos en el año precedente.

La comisión fija establecida sobre el efectivo de la cartera asesorada se liquidará y cobrará por trimestres. Si el periodo a liquidar se corresponde con un periodo de tiempo inferior al señalado, la comisión aplicable será la proporción que resulte de la tarifa general atendiendo al número de días asesorados. La base para el cálculo de la comisión se fijará sobre el saldo medio diario de la cartera valorada a precios de mercado en el cómputo trimestral.

La comisión variable establecida sobre la revalorización de la cartera asesorada se liquidará y se cobrará por anualidades. La base para el cálculo de la comisión será el incremento del valor efectivo de la cartera al final de cada año, sobre el valor efectivo de la cartera al final del año precedente, restando las aportaciones y sumando las detracciones efectuadas en el período. Si se extingue la relación contractual antes de la expiración del periodo en curso, se tomará como valor de la cartera a efectos de calcular si hay diferencia positiva el de la cartera a la fecha de la extinción.

El CLIENTE deberá abonar tanto la comisión fija como variable derivada del asesoramiento prestado, aceptando el cargo que le realizará la ASESORA en la cuenta corriente asociada descrita en el expositivo II.

Normas de conducta

A fin de determinar los productos que se adaptan al perfil del CLIENTE, la ASESORA ha evaluado la idoneidad del CLIENTE.

El CLIENTE reconoce que con carácter previo a la formalización del presente contrato, ha completado el correspondiente Test de Idoneidad que le ha facilitado la ASESORA, a fin de llevar a cabo la evaluación de idoneidad pertinente, que resulta exigida en consideración a la categoría del CLIENTE, a la naturaleza y grado de los servicios y productos de inversión prestados, de acuerdo con las normas de conducta aplicables a quienes presten servicios de inversión en cada momento.

Para recomendar la compra o suscripción de un producto concreto, la ASESORA recabará información adicional con carácter previo a la recomendación, de cara a evaluar la experiencia y conocimientos del cliente para comprender la naturaleza y riesgos asociados al producto y determinar la conveniencia de dicha inversión.

La ASESORA ha facilitado al CLIENTE, con anterioridad a la firma del presente Contrato, un documento en el que se contiene una descripción de su política de conflicto de intereses que el CLIENTE acepta expresamente.

Responsabilidad

La ASESORA se obliga a actuar con diligencia y transparencia, en el mejor interés del CLIENTE, observando los principios establecidos en las normas de conducta para la prestación de servicios de inversión a clientes, pero no está sometida a obligación alguna en términos de resultado de las inversiones que el CLIENTE realice en base al asesoramiento.

El CLIENTE realiza las inversiones que decida formalizar como resultado de las recomendaciones personalizadas que reciba de la ASESORA por su cuenta y riesgo.

Duración

El presente Contrato tiene una duración indefinida desde la fecha de su firma. No obstante, cualquiera de las partes podrá resolver el presente contrato en cualquier momento de su vigencia mediante comunicación por escrito a la otra con una antelación mínima de [Nº] días naturales.

Resolución del contrato

El contrato se resolverá, además de por la decisión de cualquiera de las partes conforme a la cláusula anterior y por las demás causas de extinción de las obligaciones, por el incumplimiento grave de una de las partes a instancia de la contraparte.

A estos efectos, la ASESORA podrá resolver el contrato en caso de impago de las comisiones, incumplimiento de la normativa aplicable al blanqueo de capitales o de abuso de mercado por parte del CLIENTE.

Gastos e impuestos

Cuantos gastos e impuestos pudieran derivarse del cumplimiento y aplicación del presente contrato, por las contraprestaciones económicas derivadas del mismo, serán satisfechos con arreglo a la legislación vigente.

Comunicaciones

Cualquier comunicación a efectuar a tenor del presente contrato podrá hacerse por carta con acuse de recibo, correo electrónico con acuse de recibo o fax con acuse de recibo. A estos efectos, las direcciones del CLIENTE y de la ASESORA serán los designados en el encabezamiento del presente contrato, a no ser que medie notificación fehaciente de cualquiera de las partes comunicando el cambio de dicho domicilio.

Confidencialidad y protección de datos

Toda la información del CLIENTE a la que tenga acceso la ASESORA será tratada con total confidencialidad.

La ASESORA se abstendrá de revelar a terceros o usar los datos y la información del CLIENTE, salvo que sea necesario para cumplir las obligaciones que le corresponden en virtud del presente contrato o que el CLIENTE lo haya autorizado por escrito a desvelar la información.

De conformidad con lo dispuesto en la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y Garantía de derecho Digitales, el CLIENTE conoce y acepta que sus datos de carácter personal serán almacenados en un fichero titularidad de la ASESORA con el fin de llevar a cabo la gestión de esta relación contractual y cumplir con lo previsto en el presente contrato.

En prueba de conformidad, una vez leído el contrato, ambas partes firman el presente documento en el que se integra el Anexo expresado, por duplicado y aun sólo efecto, en el lugar y fecha indicados en el encabezamiento.

EL CLIENTE	LA ASESORA
Fdo. Fdo.

---
name: informacion-precontractual-normalizada-contratos-viaje-mer-0520
description: "Información precontractual normalizada para contratos de viaje combinado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Información precontractual normalizada para contratos de viaje combinado

> Formulario **MER-0520** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Información precontractual normalizada para contratos de viaje combinado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Información precontractual normalizada para contratos de viaje combinado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:informacion-precontractual-normalizada-contratos-viaje-mer-0520`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL

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

La combinación de servicios de viaje que se le ofrece es un viaje combinado en el sentido del texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, aprobado por Real Decreto Legislativo 1/2007, de 16 de noviembre.

Por lo tanto, usted gozará de todos los derechos que se aplican en el marco de la UE a los viajes combinados. La(s) empresa(s) [DENOMINACIÓN SOCIAL] será(n) plenamente responsable(s) de la correcta ejecución del viaje combinado en su conjunto.

Además, como exige la legislación, la(s) empresa(s) está(n) cubierta(s) por una garantía para reembolsarle los pagos realizados y, si el transporte está incluido en el viaje, asegurar su repatriación en caso de que incurra(n) en insolvencia.

Más información sobre sus principales derechos con arreglo al texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, aprobado por Real Decreto Legislativo 1/2007, de 16 de noviembre.

Información obligatoria

El viajero recibirá la siguiente información:

Principales derechos en virtud del texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios y otras leyes complementarias, aprobado por Real Decreto Legislativo 1/2007, de 16 de noviembre:

- Los viajeros recibirán toda la información esencial sobre el viaje combinado antes de celebrar el contrato.

- Siempre habrá como mínimo un empresario responsable de la correcta ejecución de todos los servicios de viaje incluidos en el contrato.

- Se proporcionará a los viajeros un número de teléfono de emergencia o los datos de un punto de contacto donde puedan contactar con el organizador o el minorista.

- Los viajeros podrán ceder el viaje combinado a otra persona, con un preaviso razonable y, en su caso, con sujeción al pago de gastos adicionales.

- El precio del viaje combinado solo se podrá aumentar si se producen gastos específicos (por ejemplo, en los precios de combustible) y está expresamente estipulado en el contrato, y en ningún caso en los últimos veinte días anteriores al inicio del viaje combinado. Si el aumento de precio excede del ocho por ciento del precio del viaje combinado, el viajero podrá poner fin al contrato. Si el organizador se reserva el derecho de aumentar el precio, el viajero tendrá derecho a una reducción del precio si disminuyen los gastos correspondientes.

- Los viajeros podrán poner fin al contrato sin pagar ninguna penalización y obtener el reembolso completo de todos los pagos realizados si se modifica significativamente alguno de los elementos esenciales del viaje combinado que no sea el precio. Si el empresario responsable del viaje combinado lo cancela antes de su inicio, los viajeros tendrán derecho al reembolso de los pagos realizados y, cuando proceda, a una compensación.

- En circunstancias excepcionales, por ejemplo en caso de que en el lugar de destino existan graves problemas de seguridad que puedan afectar al viaje combinado, los viajeros podrán poner fin al contrato antes del inicio del viaje combinado sin pagar ninguna penalización.

- Además, los viajeros podrán poner fin al contrato en cualquier momento antes del inicio del viaje combinado mediante el pago de una penalización por terminación, que sea adecuada y justificable.

- Si, después del inicio del viaje combinado, no pueden prestarse elementos significativos de este, deberán ofrecerse al viajero fórmulas alternativas adecuadas, sin coste adicional. Los viajeros podrán poner fin al contrato sin pagar ninguna penalización en caso de no ejecución de los servicios cuando ello afecte sustancialmente a la ejecución del viaje combinado y el organizador o, en su caso, el minorista no consigan solucionar el problema.

- Los viajeros también tendrán derecho a una reducción del precio y/o a una indemnización por daños y perjuicios en caso de no ejecución o ejecución incorrecta de los servicios de viaje.

- El organizador y el minorista deberán proporcionar asistencia al viajero en caso de que este se encuentre en dificultades.

- Si el organizador o el minorista incurren en insolvencia se procederá al reembolso de los pagos. En caso de que el organizador o, en su caso, el minorista incurran en insolvencia después del inicio del viaje combinado y este incluya el transporte, se garantizará la repatriación de los viajeros. La agencia ha suscrito una garantía de protección frente a la insolvencia con la empresa. Si se deniegan servicios debido a la insolvencia de la agencia, los viajeros podrán ponerse en contacto con dicha entidad o, en su caso, con la autoridad competente (datos de contacto, entre otros, nombre, dirección completa, correo electrónico y número de teléfono).

Se proporcionará mediante un hiperenlace.

La entidad garante en caso de insolvencia, por ejemplo, un fondo de garantía o una compañía de seguros.

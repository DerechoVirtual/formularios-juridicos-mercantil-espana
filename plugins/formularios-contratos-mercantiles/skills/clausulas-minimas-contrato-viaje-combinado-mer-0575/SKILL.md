---
name: clausulas-minimas-contrato-viaje-combinado-mer-0575
description: "Cláusulas mínimas del contrato de viaje combinado. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Cláusulas mínimas del contrato de viaje combinado

> Formulario **MER-0575** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 25-11-2026.

## Qué es

Contrato de viaje combinado entre el consumidor o viajero y la agencia organizadora o minorista, con las cláusulas mínimas que deben figurar en él conforme al texto refundido de la Ley General para la Defensa de los Consumidores y Usuarios (TRLGDCU, Real Decreto Legislativo 1/2007), libro cuarto, título IV. Se usa cada vez que una agencia contrata un viaje que combina al menos dos tipos de servicios de viaje (transporte, alojamiento, etc.).

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Cláusulas mínimas del contrato de viaje combinado» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Cláusulas mínimas del contrato de viaje combinado” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:clausulas-minimas-contrato-viaje-combinado-mer-0575`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (3 veces)
- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] FIRMA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MES (2 veces)
- [ ] AUTORIDAD COMPETENTE Y DATOS DE CONTACTO
- [ ] CONDICIONES DE LA FINANCIACIÓN
- [ ] DOMICILIO Y DATOS DE CONTACTO DE LA ENTIDAD GARANTE
- [ ] ENTIDAD GARANTE
- [ ] ITINERARIO DEL VIAJE CONTRATADO
- [ ] NOMBRE DEL PROGRAMA O FOLLETO DEL ORGANIZADOR, PÁGINA Y REFERENCIA
- [ ] SOLICITUDES ESPECIALES
- [ ] TELÉFONO DE URGENCIA

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: el original citaba el artículo 151.4.b) y c) de la «LGDU/2007»; se entiende referido al TRLGDCU (RDLeg 1/2007). Comprobar el apartado exacto del artículo 151 TRLGDCU en la redacción vigente.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS SOBRE EL CONCEPTO DE VIAJE COMBINADO

El artículo 151 TRLGDCU define el viaje combinado como la combinación de, al menos, dos tipos de servicios de viaje a efectos del mismo viaje o vacación, si esos servicios:

1. Son combinados por un solo empresario, incluso a petición o según la selección del viajero, antes de que se celebre un único contrato por la totalidad de los servicios, o

2. Con independencia de la celebración de contratos distintos con diferentes prestadores de servicios de viaje, esos servicios:

i. son contratados en un único punto de venta y seleccionados antes de que el viajero acepte pagar,

ii. son ofrecidos, vendidos o facturados a un precio a tanto alzado o global,

iii. son anunciados o vendidos como «viaje combinado» o bajo una denominación similar,

iv. son combinados después de la celebración de un contrato en virtud del cual el empresario permite al viajero elegir entre una selección de distintos tipos de servicios de viaje, o

v. son contratados con distintos empresarios a través de procesos de reserva en línea conectados en los que el nombre del viajero, sus datos de pago y su dirección de correo electrónico son transmitidos por el empresario con el que se celebra el primer contrato a otro u otros empresarios con quienes se celebra otro contrato, a más tardar veinticuatro horas después de la confirmación de la reserva del primer servicio de viaje.

No se considerará viaje combinado si los servicios turísticos no representan una proporción igual o superior al veinticinco por ciento del valor de la combinación y no se anuncian o no constituyen por alguna otra razón una característica esencial de la combinación, o si solo han sido seleccionados y contratados después de que se haya iniciado la ejecución de un servicio de viaje.

El contrato de viaje combinado es el que versa sobre el conjunto del viaje combinado o, si dicho viaje se realiza con arreglo a contratos distintos, todos los contratos que regulen los servicios de viaje incluidos en él.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

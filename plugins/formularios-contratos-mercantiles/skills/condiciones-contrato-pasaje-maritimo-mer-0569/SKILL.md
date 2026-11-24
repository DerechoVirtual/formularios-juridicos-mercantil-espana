---
name: condiciones-contrato-pasaje-maritimo-mer-0569
description: "Condiciones del contrato de pasaje marítimo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Condiciones del contrato de pasaje marítimo

> Formulario **MER-0569** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Condiciones del contrato de pasaje marítimo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Condiciones del contrato de pasaje marítimo” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:condiciones-contrato-pasaje-maritimo-mer-0569`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- El modelo no tiene campos marcados: Claude te preguntará lo que necesite según el caso.

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

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

PRIMERA Documentos

El billete es personal e intransferible. El pasajero responde de la veracidad de los datos aportados para la obtención del billete. Sólo embarcarán las personas provistas de billete y tarjeta de embarque.

Las tarjetas de embarque se pueden retirar con antelación en el puerto de salida o en las oficinas de la Compañía. El cliente también puede recibir en su correo electrónico una tarjeta de embarque on line.

El pasajero deberá disponer de la documentación exigida por la normativa vigente (DNI, pasaporte, tarjeta de residente), cuya exhibición podrá serle requerida por el personal de la Compañía a efectos de verificar el cumplimiento de dicha normativa.

Todo pasajero queda sujeto al Reglamento de policía y buen orden establecido a bordo a cargo del Capitán.

SEGUNDA Horario

Los horarios e itinerarios podrán sufrir variaciones por caso fortuito o fuerza mayor. En tales casos, la Compañía adoptará las medidas razonables bajo su control para poner dichas variaciones en conocimiento de los pasajeros afectados.

En caso de necesidad el transportista puede hacerse sustituir por otro transportista o utilizar otros buques.

TERCERA Hora límite de aceptación al embarque

La hora límite de aceptación de pasajeros al embarque es de 30 minutos, a excepción de las embarcaciones rápidas que es de 15 minutos.

En el caso de los vehículos, la hora límite de aceptación al embarque es de 60 minutos, y en las embarcaciones rápidas es de 30 minutos. La hora límite de aceptación al embarque es el tiempo mínimo de antelación necesario a la hora oficial programada de salida indicada en el billete, antes de cuyo límite el pasajero y/o vehículo debe haber sido admitido al embarque, tener facturado su equipaje y estar en posesión de la tarjeta de embarque. Pasado este tiempo límite, el embarque quedará cerrado. El transportista no incurre en responsabilidad alguna por no aceptar al pasajero y/o vehículo cuando éste se presente a un embarque cerrado.

CUARTA Equipaje

El pasajero de cabina tiene derecho al transporte gratuito de un máximo de 40 kg. de equipaje de uso personal y el de butaca 20 kg., pesos a partir de los cuales deberá hacer efectivo un importe extra, hasta un máximo de 75 Kg. en cabina y 30 Kg. en butaca.

La Compañía no se hace responsable de las joyas, alhajas, dinero u objetos de valor propiedad de los pasajeros, que no hubieran sido confiadas previamente al Capitán para su custodia. Queda prohibido llevar a bordo géneros de ilícito comercio y mercancías peli- grosas.

El transporte de los vehículos amparados por este billete se realiza de conformidad con la normativa vigente sobre la materia y por los Convenios internacionales suscritos por España, sin que los mismos figuren en la masa de la avería gruesa en caso de producirse la misma. El embarque y desembarque de los vehículos en régimen de equipaje es riesgo del propietario y la Compañía no responde de las averías que puedan producirse en dichas operaciones.

QUINTA Reembolso de billete

Para el reembolso de un billete emitido por una oficina del porteador, el interesado deberá dirigirse a cualquiera de las oficinas de la Compañía. Los billetes emitidos por Agencias de Viajes serán reembolsados por éstas.

El reembolso, en uno u otro caso, se efectuará en función de la forma de pago del billete.

SEXTA Artículos peligrosos

Por medidas de seguridad, el transporte en el equipaje de mano, facturado y dentro de los vehículos, de los siguientes artículos está prohibido:

- Carteras o maletines de seguridad provistos de sistemas de alarma.

- Explosivos, municiones, artículos de pirotecnia o bengalas.

- Gases (inflamables, no inflamables, intensamente refrigerados o venenosos), como gas para camping, oxígeno, propano y butano.

- Líquidos inflamables, como combustibles, pinturas o disolventes.

- Sólidos inflamables, como artículos de fácil ignición, sustancias sujetas a combustión espontánea, sustancias que emiten gases inflamables al contacto con el agua.

- Sustancias oxidantes, como sosa o peróxidos.

- Materiales radioactivos.

- Ciertas restricciones son también de aplicación a medicinas, artículos de aseo, nieve carbónica, botellas de oxigeno o de anhídrido carbónico para uso médico, o la munición para armas de caza.

SÉPTIMA Controles de seguridad

En los puertos pueden llevarse a cabo controles de seguridad del pasaje, su equipaje y su vehículo antes de proceder al embarque, con la consiguiente retirada de los objetos cortantes o de cualquier naturaleza que pudieran considerarse como objetos peligrosos.

Para evitar los posibles inconvenientes se aconseja no transportar dichos objetos.

OCTAVA Prohibición de fumar

De conformidad con las disposiciones legales queda expresamente prohibido fumar fuera de las zonas reservadas a tal efecto a bordo del buque, sancionándose su incumplimiento con arreglo a lo establecido en dichas disposiciones.

NOVENA.-Derechos del pasajero

El transportista tiene concertada póliza de seguro que ampara el transporte, sujeta a las condiciones del Seguro Obligatorio de Viajeros.

Para formalizar una reclamación, la Compañía exigirá que se acompañe con el corres- pondiente billete de pasaje utilizado por el pasajero.

Las reclamaciones por daños o pérdida de equipajes que hubieran sido facturados deberán formalizarse por escrito ante la Compañía o su Agente en el momento de su entrega o en el que ésta debiera haberse realizado.

El servicio de Atención al Cliente atenderá todas sus consultas.

DÉCIMA Responsabilidad del transportista

Cualquier exclusión o limitación de responsabilidad del transportista se aplicará y beneficiará a sus agentes, empleados y representantes y a cualquier persona o entidad cuyo buque utilice el transportista para el transporte y a sus agentes, empleados y representantes.

Ningún empleado, agente o representante del transportista podrá modificar o hacer renuncia de cualquiera de las condiciones de este contrato.

Para el ejercicio de las acciones derivadas del contrato de transporte marítimo en líneas internacionales, se estará a la jurisdicción de los Tribunales que resulte de la aplicación del Convenio de Atenas de 1974 y/o de los instrumentos que lo modifiquen y en líneas de navegación de cabotaje nacional, se estará a la jurisdicción que resulte de aplicar la Ley de Enjuiciamiento Civil en vigor.

UNDÉCIMA.-Anulación de reservas y billetes.

La anulación o aplazamiento por parte del pasajero de reservas y billetes, emitidos para una fecha determinada, está condicionada a las siguientes circunstancias:

- En Embarcaciones Rápidas tendrá una penalidad del 10% del importe del billete, si la anulación se efectúa entre los 30 días y las 48 horas precedentes a la salida del buque, y del 20% dentro de las 48 horas anteriores a la salida del mismo hasta 2 horas antes de la misma.

- En Servicios Convencionales tendrá una penalidad del 10% del importe del billete, si la anulación se efectúa entre los 30 días y los 10 días precedentes a la salida del buque, y del 20% entre los 9 días y los 2 días anteriores a la salida del mismo.

La anulación de los billetes pasados los plazos anteriormente señalados comportará la aplicación de una penalidad por el total de su importe.

Si el pasajero decide adelantar la salida, se le podrá anular el billete emitido, sin gastos, debiendo obtener su nueva plaza en la misma acomodación o superior a la que tenía anteriormente, abonando en su caso la diferencia.

DUODÉCIMA.-Billetes Open y Tarifas Especiales.

- El cambio de un billete CERRADO a un billete OPEN se considerará una anulación de salida.

- El cambio de un billete OPEN a un billete CERRADO se considerará un adelanta- miento de salida.

- La anulación del billete emitido OPEN no comportará penalidad alguna.

Los billetes emitidos OPEN tienen una validez de un año desde la fecha de emisión, estando supeditada su utilización a la reserva previa de plaza.

Existen tarifas especiales sujetas a condiciones específicas. En estos casos, la penalidad por anulación se ajustará a las condiciones de la tarifa aplicada que, en algunos casos, alcanza la pérdida total del importe del billete.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

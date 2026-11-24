---
name: contrato-permuta-mercantil-bienes-muebles-mer-0617
description: "Contrato de permuta mercantil de bienes muebles. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de permuta mercantil de bienes muebles

> Formulario **MER-0617** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato de permuta mercantil, mediante el cual cada una de las partes contratantes adquiere la propiedad de los bienes previa valoración de los mismos, con y sin sobreprecio. Se incluyen los derechos y obligaciones de éstas, así como las condiciones y estipulaciones necesarias para el cumplimiento del contrato.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de permuta mercantil de bienes muebles» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de permuta mercantil de bienes muebles” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-permuta-mercantil-bienes-muebles-mer-0617`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (20 veces)
- [ ] DNI/NIE (4 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] DESCRIPCIÓN DE LOS BIENES MUEBLES (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] PLAZO (2 veces)
- [ ] DATOS DE LA PERSONA ADICIONAL
- [ ] DOCUMENTO O ANEXO DE DESCRIPCIÓN
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] Nº
- [ ] PLAZO DE ENTREGA

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

Modelo de contrato de permuta mercantil, mediante el cual cada una de las partes contratantes adquiere la propiedad de los bienes previa valoración de los mismos, con y sin sobreprecio. Se incluyen los derechos y obligaciones de éstas, así como las condiciones y estipulaciones necesarias para el cumplimiento del contrato.


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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de UNA PARTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de LA OTRA PARTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de PERMUTA DE BIENES MUEBLES y, a tal fin,

EXPONEN

I.- Que D./Dña. [NOMBRE Y APELLIDOS] es [ELEGIR: propietario / propietaria] en pleno dominio de [DESCRIPCIÓN DE LOS BIENES MUEBLES], por título de [ELEGIR: compraventa / fabricación propia, donación].

Que el producto se encuentra libre de toda carga o gravamen y no existe sobre el mismo disputa judicial o de cualquier otra índole.

II.- Que D./Dña. [NOMBRE Y APELLIDOS] es [ELEGIR: propietario / propietaria] en pleno dominio de [DESCRIPCIÓN DE LOS BIENES MUEBLES], por título de [ELEGIR: compraventa / fabricación propia, donación].

Que el producto se encuentra libre de toda carga o gravamen y no existe sobre el mismo contienda judicial o de cualquier otra índole.

III.- Que ambas partes se hallan interesadas en los bienes propiedad de la contraparte, y por ello,

ACUERDAN

Llevar a efecto el presente contrato de PERMUTA MERCANTIL DE BIENES MUEBLES, mediante las siguientes:

CLÁUSULAS

Primera.- Objeto

El objeto del presente contrato es la permuta de los bienes descritos en los Exponentes I y II del presente contrato, adquiriendo cada una de las partes contratantes la propiedad de los bienes del otro.

Segunda.- Valoración

[ELEGIR UNA OPCIÓN: Si no existe diferencia de valor / Si existe diferencia de valor]

Tercera.- Entrega

Los bienes que constituyen el objeto de la presente permuta y que se relacionan en los expositivos I y II, deberán ser objeto de entrega entre las partes [PLAZO DE ENTREGA].

[OPCIONAL — incluir si procede]

(En el domicilio señalado para las notificaciones)

En los domicilios que se señalan a efectos de notificaciones, por un plazo máximo que expira el [FECHA] (plazo máximo de entrega de los bienes permutados).

[OPCIONAL — incluir si procede]

(Gastos de transportes y seguros)

Cada una de las partes asume el coste que represente el transporte y entrega de los bienes permutados hasta el domicilio antes indicado, así como la constitución del seguro correspondiente para garantizar el transporte de las mercancías.

Cuarta.- Indemnizaciones

La falta de entrega de las mercancías en el plazo señalado en el párrafo anterior que no se deba a caso fortuito, fuerza mayor dará derecho a la otra parte a optar entre resolver el contrato o exigir al incumplidor la entrega efectiva de los bienes y una indemnización igual a [IMPORTE], por la falta de entrega de los bienes y [IMPORTE] euros por cada día de retraso.

Quinta.- Evicción y saneamiento

Si las mercancías no coincidiesen con las calidades, forma y tamaño descritos en [DOCUMENTO O ANEXO DE DESCRIPCIÓN], D./Dña. [NOMBRE Y APELLIDOS] quien las hubiera recibido dispondrá de un plazo de [PLAZO] a partir del día de su recepción para solicitar la sustitución de las mercancías que resulten defectuosas o que no se ajusten a dichas características.

El plazo de sustitución de la mercancía no será superior a [Nº] días. En caso de que D./Dña. [NOMBRE Y APELLIDOS] no proceda a la sustitución dentro de ese plazo, D./Dña. [NOMBRE Y APELLIDOS] podrá proceder a exigir el cumplimiento o la resolución del contrato, con abono en ambos casos de los daños y perjuicios que se le hayan irrogado.

Sexta.- Reserva de Dominio

La permuta se entiende hecha con reserva de dominio a favor de D./Dña. [NOMBRE Y APELLIDOS] hasta el momento de la contraprestación total de la misma, esto es, hasta el día [FECHA].

[OPCIONAL — incluir si procede]

(En caso de embargos, robos ...)

D./Dña. [NOMBRE Y APELLIDOS] (parte obligada al pago de las cantidades aplazadas) está obligada a hacer constar debidamente ante cualquier pretensión de embargo el carácter de depósito con el que las mercancías se encuentra en su poder y si a pesar de todo fueran embargadas por resolución judicial, lo comunicará a D./Dña. [NOMBRE Y APELLIDOS] en las [PLAZO] a que tal hecho tuviera lugar.

De la misma forma, en el supuesto de que por cualquier otra causa, (por ejemplo el robo), D./Dña. [NOMBRE Y APELLIDOS] (parte obligada al pago de las cantidades aplazadas) fuera privada de los bienes objeto de este contrato, ésta deberá ponerlo en conocimiento inmediato de D./Dña. [NOMBRE Y APELLIDOS] con el fin de que pueda adoptar las acciones que estime oportunas al respecto, sin que por ello se vea liberada de la obligación del pago íntegro del precio de la mercancía.

[OPCIONAL — incluir si procede]

(Responsabilidad por daños y perjuicios)

Asimismo, (parte obligada al pago de las cantidades aplazadas) responderá de los daños y perjuicios que sobrevinieran a la misma, incluso por caso fortuito, durante el período de vigencia de la obligación suspensiva.

La cláusula de reserva de dominio a favor de D./Dña. [NOMBRE Y APELLIDOS] quedará automáticamente extinguida en el momento en que D./Dña. [NOMBRE Y APELLIDOS] parte obligada al pago de las cantidades aplazadas haya satisfecho la totalidad de la contraprestación a la que estaba obligada. De esta forma, el bien permutado pasará a ser de plena propiedad de D./Dña. [NOMBRE Y APELLIDOS] sin limitación alguna.

Séptima.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[DATOS DE LA PERSONA ADICIONAL]

Octava.- Protección de Datos Personales

LAS PARTES reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

El incumplimiento de cualquiera de LAS PARTES de las obligaciones establecidas en la en la normativa vigente sobre Tratamiento de Datos de Carácter Personal, generará una indemnización en favor de la contraparte de [IMPORTE] euros.

Novena.- Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE].

.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones del Código de Comercio, leyes especiales y usos mercantiles que le sean aplicables, o en lo no previsto, por las disposiciones del Código Civil.

.- Fuero competente

[ELEGIR UNA OPCIÓN: Tribunales / Cláusula de arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

========================================================================

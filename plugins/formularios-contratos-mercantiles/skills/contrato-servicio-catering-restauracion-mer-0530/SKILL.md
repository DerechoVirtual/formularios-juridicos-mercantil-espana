---
name: contrato-servicio-catering-restauracion-mer-0530
description: "Contrato de servicio de catering o restauración. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicio de catering o restauración

> Formulario **MER-0530** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicio de catering o restauración» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicio de catering o restauración” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-servicio-catering-restauracion-mer-0530`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (13 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] Nº (4 veces)
- [ ] PROVINCIA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] INSCRIPCIÓN (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] HORA
- [ ] IMPORTE
- [ ] MES
- [ ] NIF
- [ ] NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN
- [ ] Nº DE TRABAJADORES
- [ ] NÚMERO
- [ ] PLAZO

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

En la ciudad/localidad de [LOCALIDAD], provincia de [PROVINCIA], a [DÍA] de [MES] de [AÑO]

REUNIDOS

De una parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA], provisto/a del N.I.F. número [NÚMERO].

Y de otra parte D./Dª [NOMBRE Y APELLIDOS], mayor de edad, vecino/a de [LOCALIDAD], con domicilio en la localidad/ciudad de [LOCALIDAD], provincia de [PROVINCIA] provisto/a del N.I.F. [NIF].

INTERVIENEN

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF, domiciliada en y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], en adelante LA EMPRESA DE CATERING

D./Dª [NOMBRE Y APELLIDOS], interviene en nombre y representación de la mercantil de [DENOMINACIÓN SOCIAL], CIF, domiciliada en y constituida en [LOCALIDAD] ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha e inscrita en el Registro Mercantil de [LOCALIDAD] inscripción [INSCRIPCIÓN], en adelante el CLIENTE

MANIFIESTAN

Que intervienen en la representación expresada y se reconocen mutua y plena capacidad legal de obrar y de obligarse para este acto, otorgando de forma libre y espontánea y a su tenor el presente CONTRATO DE CATERING asumiendo la responsabilidad que corresponda en función de la veracidad de sus manifestaciones, y, de mutuo acuerdo,

EXPONEN

I. Que la EMPRESA DE CATERING es una mercantil dedicada a la prestación de servicios de catering y dispone de los medios, y autorizaciones administrativas necesarias para prestar dichos servicios. La oferta de restauración se recoge en el folleto que se incorpora como Anexo de este contrato.

II. Que el CLIENTE es una mercantil con [Nº DE TRABAJADORES] trabajadores, interesada en contratar los servicios de catering para elaborar y servir la comida de mediodía de sus trabajadores en el comedor de la empresa.

III.- Que siendo interés de ambas partes, convienen la celebración de un contrato de catering, con sujeción a las siguientes

CLÁUSULAS

Objeto

Constituye el objeto del contrato la prestación del servicio de Catering para el CLIENTE en el comedor de su centro de trabajo sito en [LOCALIDAD], donde actualmente están empleados un número de trabajadores, para la comida de mediodía que se desarrollará entre las [HORA] y las [Nº] horas durante los días laborables.

La EMPRESA DE CATERING debe prestar el servicio en barquetas individuales por comensal, con un menú consistente en ensalada, primer plato, segundo plato, postre, pan, bebida y café.

Los platos que integran el menú serán seleccionados por EL CLIENTE en función de los ofertados en el Anexo por la EMPRESA DE CATERING.

De no aprobarse alguna de las combinaciones propuestas, EL CLIENTE podrá proponer otros platos, los que se incluirán en el menú.

Al efecto, la EMPRESA DE CATERING pasará al CLIENTE el listado mensual de las comidas para el mes siguiente con una antelación mínima de [Nº] días.

El día 25 de cada mes el CLIENTE procederá a enviar a la EMPRESA DE CATERING dicho listado, en su caso, con los cambios correspondientes.

Duración

El plazo de duración del contrato es de [Nº] años, que se prorrogará de forma automática por periodos de [PLAZO], salvo que alguna de las partes se oponga a cuyo efecto deberá remitir un preaviso por escrito con una antelación mínima de meses.

Precio

El CLIENTE abonará a la EMPRESA DE CATERING la cantidad de [IMPORTE] euros por menú, impuestos incluidos, con un mínimo de [Nº] menús/día.

El precio se hará efectivo contra factura debidamente desglosada en la forma siguiente:

-Un% sobre el mínimo de menús contratados en los cinco primeros días de cada mes.

-El resto del precio sobre los menús efectivamente realizados en el mes siguiente al de la prestación.

Obligaciones de la empresa de catering

La empresa de CATERING se compromete a cumplir las obligaciones derivadas del contrato y en especial:

– A elaborar las comidas con las características, la calidad, y la cantidad ofrecidas por la empresa en el Anexo, y sobre la base de los menús acordados.

– A servir las comidas por personal adecuado.

– A realizar el transporte y entregar la comida en el tiempo y lugar convenido.

– A cumplir las condiciones higiénico-sanitarias de los establecimientos del sector de la restauración en cuanto a la elaboración, envasado, almacenamiento, transporte y servicio de comidas, así como desarrollar unas prácticas correctas de manipulación de los alimentos e higiene alimentaria.

– A mantener en condiciones higiénicas y de limpieza el comedor donde se sirven las comidas, así como los utensilios, e incluyendo las desinfecciones.

– A informar periódicamente de la planificación de los menús en los términos convenidos.

Obligacionese del cliente

El CLIENTE se compromete a cumplir las obligaciones derivadas del contrato y en especial a:

– A pagar el precio del servicio en el plazo convenido.

– A colaborar con la EMPRESA DE CATERING, poniendo a su disposición el local de comedor y facilitando el acceso del personal de dicha empresa debidamente acreditado a los efectos de la prestación del servicio de restauración.

– A advertir a la EMPRESA DE CATERING de cualquier vicisitud que pueda influir en el normal desarrollo del servicio de comedores dentro de un plazo mínimo de diez días.

Terminación y resolución

El contrato finaliza por el transcurso del plazo pactado o de sus prórrogas, sin que ninguna de las partes pueda pedir indemnización en este caso.

El contrato se resolverá en caso de incumplimiento de las obligaciones de alguna de las partes, a instancia de la parte que no ha incumplido el contrato. En este caso, la parte incumplidora deberá resarcir a la otra parte de todos los daños y perjuicios que le haya causado.

Claúsula de sumisión

(mediación y/o arbitraje) Las partes contratantes acuerdan libre y voluntariamente que todas las desavenencias, divergencias o cuestiones litigiosas que deriven de este contrato, incluso cuando la controversia verse sobre la validez o existencia del presente contrato, se resolverán a través de la Mediación (en su caso se citará la institución) de [NOMBRE DE LA INSTITUCIÓN DE MEDIACIÓN], antes de acudir a la jurisdicción o a otra solución extrajudicial de conflictos, sometiéndose a la regulación establecida en la Ley 5/2012, de 6 de julio, y (caso de fijar un plazo máximo) fijando un plazo máximo de duración del procedimiento de sesenta días desde la solicitud de iniciación por cualquiera de las partes.

(caso de pacto sucesivo de arbitraje) A falta de resolución de la controversia en el procedimiento de mediación, la misma será definitivamente resuelta mediante Arbitraje de la Corte de [LOCALIDAD], a la que se encomienda la administración del arbitraje y la designación de los árbitros, de acuerdo con su reglamento.

(pcto de sumisión expresa) Las partes, con renuncia expresa al fuero que pudiera corresponderles, se someten para todas las cuestiones dimanantes del presente contrato a los Tribunales de la localidad de

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad de cuanto antecede, las partes firman y rubrican el presente contrato al que se incorpora como parte integrane el Anexo expresado, a un solo efecto y por duplicado ejemplar, en todas sus hojas, en el lugar y fecha del encabezamiento.

LA EMPRESA DE CATERING

Fdo. Don [NOMBRE Y APELLIDOS]

EL CLIENTE

Fdo.

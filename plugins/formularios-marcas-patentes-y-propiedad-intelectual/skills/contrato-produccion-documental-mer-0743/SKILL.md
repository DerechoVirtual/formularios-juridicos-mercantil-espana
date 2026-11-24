---
name: contrato-produccion-documental-mer-0743
description: "Contrato de producción de un documental. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de producción de un documental

> Formulario **MER-0743** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato de producción de un documental sobre una determinada materia.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de producción de un documental» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de producción de un documental” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-produccion-documental-mer-0743`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] DNI/NIE (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº (3 veces)
- [ ] PLAZO (3 veces)
- [ ] FECHA (2 veces)
- [ ] IDIOMA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] TÍTULO DE LA OBRA (2 veces)
- [ ] CARGO
- [ ] FORMATO DE IMAGEN
- [ ] FORMATO DE PELÍCULA (MM)
- [ ] IMÁGENES POR SEGUNDO
- [ ] LUGAR
- [ ] LUGAR DE POSTPRODUCCIÓN
- [ ] LUGAR DE RODAJE
- [ ] OBJETO DEL CONTRATO
- [ ] ORDEN DE LOS CRÉDITOS
- [ ] REGLAS DE REMUNERACIÓN
- [ ] TIPO DE OBRA AUDIOVISUAL

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

Modelo de contrato de producción de un documental sobre una determinada materia.


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
(Datos de LA PRODUCTORA)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, LA PRODUCTORA.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del DIRECTOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EL DIRECTOR.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de PRODUCCIÓN DE OBRA AUDIOVISUAL y, a tal fin,

MANIFIESTAN

I.- Que LA PRODUCTORA tiene en proyecto la producción de una obra audiovisual [TIPO DE OBRA AUDIOVISUAL]. titulada provisionalmente [TÍTULO DE LA OBRA], con una duración aproximada de [PLAZO].

II.- Que LA PRODUCTORA está interesada en contratar a D./Dña. [NOMBRE Y APELLIDOS] en calidad de [CARGO] de la citada obra audiovisual, por lo que ambas partes convienen en celebrar el presente contrato, con arreglo a las siguientes:

ESTIPULACIONES

Primera.- Objeto del contrato

El presente contrato tiene por objeto la producción por parte de LA PRODUCTORA del documental " [TÍTULO DE LA OBRA] ", con duración prevista no superior a [Nº] minutos, rodado en [FORMATO DE PELÍCULA (MM)] mm color, formato [FORMATO DE IMAGEN] a [IMÁGENES POR SEGUNDO] imágenes por segundo, de acuerdo con las condiciones artísticas y técnicas acordadas de mutuo acuerdo por las partes aquí contratantes.

El documental se rodará en [LUGAR DE RODAJE], y la postproducción se efectuará en [LUGAR DE POSTPRODUCCIÓN].

Segunda.- Dirección del documental y trabajos específicos

La dirección del documental irá a cargo de EL DIRECTOR, señalándose como labores propias del mismo, en colaboración con LA PRODUCTORA, las siguientes:

a) Aportación de nuevos elementos narrativos del guion, en su caso.
b) Supervisión y aceptación del plan de trabajo.
c) Selección y propuesta de actores, presentadores y voces en off.
d) Propuesta y dirección de localizaciones.
e) Dirección de pruebas de vestuario, maquillaje, peluquería y decorados.
f) Dirección de todos los elementos artísticos, creativos y técnicos del rodaje.
g) Dirección de montaje del documental.
h) Dirección del doblaje si lo hubiere y sonorización del documental hasta la obtención de la copia standard.
i) Propuesta de títulos de crédito y efectos de imagen.
j) Participación activa en la promoción, lanzamiento y presentación del documental en el estreno de las principales capitales (hasta un total de [Nº] en el ámbito nacional), en los principales festivales a los que asistiese el documental a concurso y en los medios de comunicación.

Se determinan como labores propias de LA PRODUCTORA en la creación y elaboración del documental las siguientes:

a) Diseño de producción, incluyendo el presupuesto y el plan de trabajo y presentación ante los organismos oficiales.
b) Selección y contratación de localizaciones.
c) Selección y contratación de actores, presentadores y voces en off.
d) Selección y contratación del equipo técnico.
e) Selección de los efectos visuales del documental.
f) Contratación de empresas proveedoras y servicios en España y otros países, en su caso.
g) Consecución de la financiación necesaria para la realización del documental.
h) Aprobación del vestuario, maquillaje peluquería, decorados y labores creativas de la puesta en escena.
i) Supervisión y aceptación del montaje y premezclas y mezclas de sonido.
j) Supervisión y aprobación de los créditos, efectos visuales y de la copia 0.
k) Diseño de la campaña de promoción, lanzamiento e imagen del documental; dirección del spot y del tráiler de la misma, con la colaboración del propio Director/Coproductor.

Tercera.- Cesión de derechos de propiedad intelectual

Como consecuencia de lo señalado en la cláusula precedente, EL DIRECTOR cede de manera exclusiva a LA PRODUCTORA, que los acepta, sus derechos de reproducción, distribución y comunicación pública sobre el documental, en todo el universo, incluyendo España, por todos los medios, formatos y procedimientos conocidos y por conocer, y con duración de los mencionados derechos de por vida.

Cuarta.- Coste de producción

El coste de producción, según diseño que se presentará a los organismos oficiales correspondientes, queda fijado en la cantidad de [IMPORTE] euros, incluyendo copias y publicidad de lanzamiento.

El coste de producción se asume íntegramente por LA PRODUCTORA.

Quinta.- Contraprestación

Como remuneración por la [OBJETO DEL CONTRATO] objeto del presente contrato, y por los derechos cedidos, LA PRODUCTORA abonará a las siguientes cantidades:

1.- En concepto de la prestación de servicios, una cantidad a tanto alzado de [IMPORTE] euros ( €).

De dicha cantidad habrá que detraer la cantidad que LA PRODUCTORA haya de retener e ingresar en concepto de IRPF conforme a la normativa fiscal aplicable
2.- Por la cesión de derechos de propiedad intelectual, se establece una remuneración conforme a las siguientes reglas: [REGLAS DE REMUNERACIÓN].

Sexta.- Versiones

El documental podrá tener versión [IDIOMA], versión [IDIOMA] y las versiones internacionales que sean necesarias.

Séptima.- Financiación externa previa a la finalización del documental

EL DIRECTOR autoriza a LA PRODUCTORA a la presentación de su currículum ante cuantas instancias sea necesario para la obtención de financiación del documental.

Igualmente se obliga a colaborar en la redacción del Proyecto que en su caso se precise como documentación necesaria para la obtención de la citada financiación.

Octava.- Preparación, rodaje y postproducción

La preparación del documental se iniciará durante [PLAZO], dando comienzo a continuación el rodaje del mismo con una duración de [Nº] semanas.

La postproducción del documental finalizará [FECHA].

Novena.- Créditos

En los títulos de crédito, piezas publicitarias, prensa y apariciones de imagen, LA PRODUCTORA y EL DIRECTOR aparecerán de la siguiente forma y orden: [ORDEN DE LOS CRÉDITOS].

Décima.- Derechos Morales

Queda reservado el derecho moral del AUTOR, en los términos establecidos por la Ley de Propiedad Intelectual.

Decimoprimera.- Contratación de equipo técnico y artístico. Funciones del equipo de producción

La contratación de equipo técnico y artístico será efectuada por LA PRODUCTORA y EL DIRECTOR. En aquellos casos en que se trate de los jefes de equipo del documental (decorador, montador, director de fotografía, director de producción, ayudante de dirección, maquillador, ingeniero de sonido, jefe de vestuario y peluquero), LA PRODUCTORA, de común acuerdo con EL DIRECTOR, elegirán a los profesionales más adecuados.

El trabajo específico de la dirección de producción contratada, con carácter enunciativo y no limitativo, bajo la supervisión de los productores ejecutivos, será:

— Diseño de producción.
— Confección de los desgloses de producción, plan de trabajo, presupuesto y memoria de producción.
— Confección de la documentación de producción necesaria para la preparación y rodaje del documental.
— Confección del plan de tesorería y calendario de pagos.
— Selección y adecuación de localizaciones.
— Control y cotejo semanal informatizado del presupuesto. Realización contable y su presentación a LA PRODUCTORA y al DIRECTOR.
— Altas y Bajas de Seguridad Social. Retenciones. Presentación de documentación.
— Realización de la preparación y rodaje del documental, con alquiler incluido de las oficinas e instalaciones necesarias en [LOCALIDAD].
— Contratación del equipo técnico y artístico (salvo grandes protagonistas).
— Devolución de los materiales alquilados a las empresas proveedoras.

Decimosegunda.- Seguros

LA PRODUCTORA contratará con una o varias compañías de seguros las siguientes pólizas:

a) póliza de seguro de negativo;
b) póliza de seguro de accidentes e invalidez permanente de los protagonistas y el director.
c) póliza de seguro de responsabilidad civil (que incluya siniestro sobre mobiliario, accesorios, material técnico de rodaje); y
d) póliza de seguro de buen fin del documental, cuya beneficiaria serán la propia PRODUCTORA.

Los seguros deberán cubrir íntegramente el coste del documental y serán mantenidos en vigor hasta que la copia standard del mismo sea entregada, o se contratará una duración suplementaria convenida entre las partes que se considere acaso necesaria para la distribución o explotación del documental.

Decimotercera.- Cesión a terceros

LA PRODUCTORA podrá ceder a terceros los derechos y obligaciones dimanantes del presente contrato, con las limitaciones establecidas por la legislación vigente en materia de cesiones a coproductores internacionales.

Decimocuarta.- Confidencialidad

Ninguna de las partes podrá hacer del conocimiento de un tercero el contenido total o parcial de este contrato, sin el consentimiento previo y por escrito de la otra.

[OPCIONAL — incluir si procede]

(Si se pacta el derecho de opción preferente sobre las secuelas, remakes u Spin Off)

Decimoquinta.- Secuela, Remake y Spin Off

La PRODUCTORA tendrá un derecho de opción preferente sobre la secuelas, remakes u Spin Off que se pretendan realizar de la obra audiovisual objeto de este Contrato. Cuando lo que se pretenda por la PRODUCTORA sea la realización de secuelas, remakes u Spin Off utilizando los personajes o elementos originales y creativos de la obra audiovisual objeto del presente contrato se deberá remitir por escrito al autor la información sobre secuelas, remakes u Spin Off y abonarle la suma de [IMPORTE] EUROS ( €). De dicha cantidad habrá que detraer la cantidad que LA PRODUCTORA haya de retener e ingresar en concepto de IRPF conforme a la normativa fiscal aplicable. Para el abono de la citada cantidad habrá de presentarse por el AUTOR la correspondiente factura, que será abonada por la PRODUCTORA en el plazo de [PLAZO]. Los términos relativos a la cesión de los derechos de Autor sobre las secuelas, los remakes o los spin off serán negociados expresamente con el autor.

.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

.- Protección de datos personales

LAS PARTES reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

El incumplimiento de cualquiera de LAS PARTES de las obligaciones establecidas en la en la normativa vigente sobre Tratamiento de Datos de Carácter Personal, generará una indemnización en favor de la contraparte de [IMPORTE] euros.

.- Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [ELEGIR: la productora / el director].

.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones del Real Decreto Legislativo 1/1996, de 12 de abril, por el que se aprueba el Texto Refundido de la Ley de Propiedad Intelectual, y demás disposiciones legales en vigor.

.- Fuero competente

[ELEGIR UNA OPCIÓN: Si se pacta someterse a tribunales / Si se pacta someterse a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

PRODUCTORA	DIRECTOR/ GUIONISTA

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

---
name: contrato-patrocinio-sponsoring-patrocinado-publicita-mer-0508
description: "Contrato de patrocinio (sponsoring) en que el patrocinado publicita los productos del patrocinador. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de patrocinio (sponsoring) en que el patrocinado publicita los productos del patrocinador

> Formulario **MER-0508** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de patrocinio (sponsoring) en que el patrocinado publicita los productos del patrocinador» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de patrocinio (sponsoring) en que el patrocinado publicita los productos del patrocinador” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-patrocinio-sponsoring-patrocinado-publicita-mer-0508`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] DNI/NIE (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] PLAZO (4 veces)
- [ ] FECHA (3 veces)
- [ ] Nº (3 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] TIPO DE ACTOS (2 veces)
- [ ] BENEFICIARIO
- [ ] LUGAR
- [ ] LUGAR DE ENTREGA
- [ ] MES
- [ ] Nº DE CUENTA (IBAN)
- [ ] OTROS DATOS
- [ ] TAMAÑO DEL MÓDULO

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

Contrato mercantil de patrocinio publicitario o sponsoring, por el que el patrocinado se obliga a hacer publicidad de los productos del patrocinador a cambio de una contraprestación económica. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del contrato, así como los derechos y obligaciones de cada una de las partes.

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del PATROCINADOR)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, PATROCINADOR.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del PATROCINADO)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, PATROCINADO.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de PATROCINIO y, a tal fin,

MANIFIESTAN

I.- Que EL PATROCINADOR se dedica a [ACTIVIDAD]

II.- Que EL PATROCINADO se dedica a [ACTIVIDAD] y organiza habitualmente actos de [TIPO DE ACTOS], estando interesado en hacer publicidad durante tales actos públicos de los productos de EL PATROCINADOR a cambio de una contraprestación económica y que por ello ambas partes:

ACUERDAN

Llevar a efecto el presente contrato de PATROCINIO PUBLICITARIO O SPONSORING mediante las siguientes:

CLÁUSULAS

Primera.- Objeto

EL PATROCINADO se compromete a hacer publicidad de los productos de la PATROCINADORA en cuantos actos públicos comparezca, sean éstos, [TIPO DE ACTOS] o cualquier otra que se efectúe en nombre del PATROCINADO

Segunda.- Ejecución

La publicidad de los productos que el PATROCINADOR encomienda al PATROCINADO se realizará de la siguiente forma:

[OPCIONAL — incluir si procede]

(Medios Audiovisuales)

en los siguientes medios, durante el tiempo que se especifica y con la siguientes frecuencias y franjas horarias [OTROS DATOS]

Además, EL PATROCINADO deberá a describir en las entrevistas, ruedas de prensa y demás apariciones públicas o televisadas el patrocinio del evento.

[OPCIONAL — incluir si procede]

(Medios escritos)

en los siguientes medios, durante [PLAZO], en la sección y en módulos de tamaño [TAMAÑO DEL MÓDULO]:

A tal efecto, el PATROCINADOR proporcionará al PATROCINADO o a quien este indique el material necesario para la reproducción de sus marcas y anagramas.

[OPCIONAL — incluir si procede]

(Folletos, pegatinas pins, camisetas)

El PATROCINADOR se obliga a entregar al PATROCINADO el [FECHA] los folletos, pegatinas, pins camisetas [LUGAR DE ENTREGA] cuyos diseños y características se especifican en el Anexo I.

Tercera.- Remuneración

La contraprestación que se establece es de [IMPORTE] euros, de las que EL PATROCINADOR entrega en el presente acto [IMPORTE] euros en metálico en pago de la primera mensualidad correspondiente al mes de [MES], cantidad que el PATROCINADO recibe manifestando su conformidad, y sirviendo el presente documento como carta de pago.

El resto de los pagos (en total [Nº]) se efectuarán el día [FECHA] de cada mes abonándose mediante ingreso en la cuenta corriente [Nº DE CUENTA (IBAN)] del [ELEGIR: PATROCINADO / Beneficiario de la Donación].

[OPCIONAL — incluir si procede]

(Retrasos)

El retraso en más de [Nº] días en cualquiera de los pagos previstos concederá el derecho a LA PATROCINADA a exigir a LA PATROCINADORA un interés moratorio del % respecto de cada uno de los pagos retrasados.

[OPCIONAL — incluir si procede]

(Cumplimiento defectuoso)

El incumplimiento por parte del PATROCINADO de la difusión publicitaria pactada o su realización en condiciones diversas a las señaladas sin causa justificada dará lugar al descuento proporcional en la remuneración a satisfacer por el PATROCINADOR en la mensualidad correspondiente

Cuarta.- Donación de contraprestación

EL PATROCINADO donará la contraprestación abonada por LA PATROCINADORA a favor de [BENEFICIARIO], por lo que LA PATROCINADORA abonará a ésta, la cantidad de [IMPORTE] %.

Quinta.- Obligaciones del Patrocinador

De acuerdo con el presente contrato, EL PATROCINADOR quedará obligado a:

- El pago de la remuneración pactada al Patrocinado.
- Asumir las consecuencias que se puedan derivar para el Patrocinado por el incumplimiento de la legislación en materia de publicidad.
- La entrega de soporte que contengan los signos distintivos objeto de patrocinio en condiciones tales que permitan su tratamiento posterior sin requerir más operación que las necesarias para fijar los signos distintivos en los objetos o elementos del Patrocinado.
- Gestionar y contratar cuantos seguros sean necesarios para cubrir los riesgos derivados de daños a cosas o personas que puedan causarse
- Recabar cuantas autorizaciones, administrativas o particulares, sean precisas para la ejecución de lo acordado en el presente contrato.

e) Responder por el deterioro de los signos distintivos en el caso de que éstos se hubiesen perdido, deteriorado o dañado por un uso indebido

Sexta.- Obligaciones del Patrocinado

De acuerdo con el presente contrato, EL PATROCINADO estará obligado a:

-Revisar los soportes o elementos a los cuales el Patrocinado hubiere fijado los signos distintivos del Patrocinador, a fin de comprobar que en todo momento los mismos se hallan en condiciones de cumplir con lo dispuesto y acordado en este contrato.
-Comunicar al Patrocinador cualquier desperfecto, deterioro o anomalía sobre los soportes o elementos a los que el Patrocinado hubiere incorporado los signos distintivos
-Repetir la publicidad en aquellos casos en los que no hubiese sido posible por cualquier causa su difusión, según los usos del sector, del mensaje de patrocinio. La nueva difusión se hará en las mismas condiciones de todo tipo pactadas inicialmente para la difusión de los signos distintivos del Patrocinador.

Séptima.- Duración

EL presente contrato tendrá una duración de [PLAZO], renovable tácitamente a su vencimiento por períodos [PLAZO], salvo denuncia expresa por alguna de las partes contratantes con [PLAZO] de preaviso

[OPCIONAL — incluir si procede]

(Renovación tácita)

La renovación tácita del contrato implicará una actualización de las remuneraciones mensuales pactadas en un [Nº] por ciento para cada año de prórroga.

Octava.- Exclusividad

[OPCIONAL — incluir si procede]

(Del patrocinado)

Durante la vigencia del presente contrato EL PATROCINADO no podrá hacer publicidad por sí mismo, ni autorizar a terceros de productos que de cualquier forma entraran en competencia directa o indirecta con los productos del PATROCINADOR.

[OPCIONAL — incluir si procede]

(Del patrocinador)

EL PATROCINADOR no podrá, por sí mismo, ni a través de terceros, patrocinar o financiar de cualquier otra forma actos o eventos que supusieran o pudieran suponer competencia directa o indirecta con los del PATROCINADO.

.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

.- Protección de datos personales

LAS PARTES reconocen que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

El incumplimiento de cualquiera de LAS PARTES de las obligaciones establecidas en la en la normativa vigente sobre Tratamiento de Datos de Carácter Personal, generará una indemnización en favor de la contraparte de [IMPORTE] euros.

.- Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [ELEGIR: patrocinador / patrocinado].

.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones de la Ley 34/1988 de 11 de Noviembre, Ley General de Publicidad, reformada por la Ley 29/2009, de 30 de diciembre, por la que se modifica el régimen legal de la competencia desleal y de la publicidad para la mejora de la protección de los consumidores y usuarios; y en su defecto por lo previsto en el Código de Comercio, leyes especiales y usos mercantiles que le sean aplicables, o en lo no previsto, por las disposiciones del Código Civil.

.- Fuero competente

[ELEGIR UNA OPCIÓN: Si se pacta someterse a tribunales / Si se pacta someterse a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

PATROCINADOR

PATROCINADO

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

---
name: contrato-cuentas-participacion-mer-0510
description: "Contrato de cuentas en participación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cuentas en participación

> Formulario **MER-0510** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Contrato de colaboración entre personas, físicas o jurídicas, empresas, por el cual uno de ellos, el partícipe, aporta bienes, dinero o derechos a otro, el gestor, teniendo el gestor que aplicar dicha aportación a la actividad empresarial pactada

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cuentas en participación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cuentas en participación” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-cuentas-participacion-mer-0510`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] ACTIVIDAD
- [ ] IMPORTE
- [ ] MEDIO DE PAGO
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE CLÁUSULA
- [ ] OTROS DATOS
- [ ] PLAZO

## Normas que cita el formulario

- art. 239 Código de Comercio

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

Contrato de colaboración entre personas, físicas o jurídicas, empresas, por el cual uno de ellos, el partícipe, aporta bienes, dinero o derechos a otro, el gestor, teniendo el gestor que aplicar dicha aportación a la actividad empresarial pactada


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

En [LOCALIDAD].

REUNIDOS

DE UNA PARTE,

[ELEGIR UNA OPCIÓN: Persona física / Empresa]

En lo sucesivo, GESTOR.

Y DE OTRA,

[ELEGIR UNA OPCIÓN: Persona física / Empresa]

En lo sucesivo, PARTÍCIPE.

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de CUENTAS EN PARTICIPACIÓN y, a tal fin,

MANIFIESTAN

I.- Que EL GESTOR se dedica, entre otras actividades, a [ACTIVIDAD]

II.- Que EL PARTÍCIPE está interesado en contribuir económicamente en la citada actividad del GESTOR, intención ésta compartida por dicho GESTOR, haciéndose así partícipe de sus resultados prósperos o adversos en la proporción que se señala en el presente contrato.

III.- Que por todo ello ambas partes se someten a las siguientes

CLÁUSULAS

Primera.- Naturaleza

Que las partes acuerdan celebrar, por el presente acto, un contrato de CUENTAS EN PARTICIPACIÓN que se regirá por lo previsto en el presente documento, y en su defecto, por las disposiciones contenidas en los artículos 239 y siguientes del Código de Comercio, así como por las restantes normas que resulten de aplicación.

Segunda.- Objeto

El objeto del presente contrato lo constituye la participación en los resultados, prósperos o adversos, de la actividad desarrollada por el GESTOR descrita en la Manifestación I.

Tercera.- Aportaciones

A tal fin, EL PARTÍCIPE aporta al negocio del GESTOR [IMPORTE] euros, cantidad que entrega en el presente acto, y que EL GESTOR declara recibir [MEDIO DE PAGO].

Cuarta.- Duración

La duración del presente contrato [PLAZO], sin perjuicio de las causas de extinción previstas en la cláusula [Nº DE CLÁUSULA] será:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

De [ELEGIR: meses / años], duración que coincide con la del negocio al que se vincula la aportación del partícipe

Indefinida

Quinta.- Participación

Debido a la entrega referida en la cláusula Tercera, el PARTÍCIPE pasa a serlo en la proporción de un [PORCENTAJE] por 100 de los resultados prósperos o adversos del negocio al que se vincula el presente contrato.

En todo caso, la cuantía máxima de las pérdidas imputables al PARTÍCIPE queda limitada a su aportación.

Sexta.- Liquidación

La liquidación se efectuará:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Cuando finalice el negocio o acto mercantil vinculado a este contrato, previa oportuna rendición de cuentas

Al final de cada ejercicio económico, el GESTOR abonará al PARTÍCIPE el [PORCENTAJE] por 100 de las ganancias que le correspondan, en el plazo de los [Nº] meses siguientes al cierre de dichos ejercicios, previa la oportuna rendición de cuentas referente a ese período.

Séptima.- Rendición de cuentas

El GESTOR rendirá cuentas justificadas de la marcha del negocio en el momento de la extinción del contrato, además de en el plazo de [Nº] meses tras el cierre de cada ejercicio económico. En aras a la comprobación de dichas rendiciones, el PARTÍCIPE podrá examinar, en el plazo de los [Nº] meses siguientes a la extinción del contrato o al cierre de cada ejercicio, la contabilidad del GESTOR, en el domicilio de éste.

Octava.- Gestión

El GESTOR se compromete a la llevanza y dirección de su negocio según la diligencia de un ordenado empresario y un representante leal, comprometiéndose por su parte, el PARTÍCIPE, a no interferir en dicha labor.

Novena.- Extinción

Serán causas de extinción del presente contrato:

a) La voluntad de los contratantes.
b) El incumplimiento de cualquiera de las condiciones estipuladas.
c) La muerte o concurso del GESTOR.
d) Otras [OTROS DATOS]

Décima.- Confidencialidad

Las partes se comprometen a no divulgar la información y documentación confidencial referente a la otra parte de la que hayan tenido conocimiento por razón de la ejecución del presente contrato, salvo las indispensables para su cumplimiento, y a mantenerla en secreto, incluso después de la finalización del mismo.

Ambas partes acuerdan tomar las medidas necesarias respecto a su personal e incluso terceros que puedan tener acceso a dichas información y documentación, a fin de garantizar la confidencialidad objeto de esta cláusula.

Decimoprimera.- Protección de datos

Las partes reconocen que la legislación sobre protección de datos personales (ley orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales.

Decimosegunda.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Decimotercera.- Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE]

Decimocuarta.- Fuero competente

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Ambas partes contratantes renuncian expresamente a su fuero sometiéndose a los Juzgados y Tribunales de [LOCALIDAD]

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

EL GESTOR

EL PARTÍCIPE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

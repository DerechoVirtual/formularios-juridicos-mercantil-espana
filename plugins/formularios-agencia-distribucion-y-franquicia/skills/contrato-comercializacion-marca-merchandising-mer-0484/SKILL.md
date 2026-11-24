---
name: contrato-comercializacion-marca-merchandising-mer-0484
description: "Contrato de comercialización de marca o merchandising. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de comercialización de marca o merchandising

> Formulario **MER-0484** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Por el contrato de comercialización o merchandising, una parte (generalmente una Empresa) colabora con otra (el cliente) para hacer que los productos de esta última sean más competitivos a cambio de un precio. Por ejemplo, redactar informes de mercado; explotar una creación intelectual como imagen; usar marcas en sectores no competitivos; abrir mercados. etc

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de comercialización de marca o merchandising» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de comercialización de marca o merchandising” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-comercializacion-marca-merchandising-mer-0484`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] IMPORTE (5 veces)
- [ ] DNI/NIE (4 veces)
- [ ] PORCENTAJE (4 veces)
- [ ] DESCRIBIR (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] PLAZO (2 veces)
- [ ] CONDICIONES
- [ ] FINALIDAD DEL ESTUDIO
- [ ] LUGAR
- [ ] MARCA/MODELO
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE CUENTA (IBAN)
- [ ] PRODUCTOS

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

Por el contrato de comercialización o merchandising, una parte (generalmente una Empresa) colabora con otra (el cliente) para hacer que los productos de esta última sean más competitivos a cambio de un precio. Por ejemplo, redactar informes de mercado; explotar una creación intelectual como imagen; usar marcas en sectores no competitivos; abrir mercados. etc


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

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EMPRESA DE MERCHANDISING.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CLIENTE.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de MERCHANDISING y, a tal fin,

MANIFIESTAN

I. Que la Empresa de merchandising está dedicada en exclusiva a la investigación y estudio de mercados, así como a la promoción de productos.

II. Que el Cliente tiene como intención el incremento de las ventas de los siguientes productos: [PRODUCTOS],

IV. Que el Cliente y la Empresa de merchandising han alcanzado un acuerdo en virtud del cual esta última se compromete a llevar a cabo la promoción de los productos indicados, pactando para su ejecución el presente contrato, con arreglo a las siguientes:

CLAUSULAS

Primera.- Objeto

La empresa de merchandising se obliga a llevar a efecto y realizar para el cliente un estudio sobre [DESCRIBIR]. consistente en [DESCRIBIR]. y con la finalidad de .. [FINALIDAD DEL ESTUDIO], según las siguientes condiciones de. [CONDICIONES], en lo sucesivo el estudio de mercado.

Segunda.- Duración

El plazo máximo para la realización del estudio de mercado es de [PLAZO] por lo que la empresa de merchandising se compromete a ponerlo a disposición del cliente antes del [FECHA].

Tercera.- Licencias y Cesiones

[ELEGIR UNA OPCIÓN: Marcas / Propiedad intelectual]

Cuarta.- Precio

El precio que se establece para el estudio de mercado objeto del presente contrato es de [IMPORTE] euros; por la cesión de los derechos de reproducción y transformación de [IMPORTE] euros; por la obtención de la licencia de la marca euros; por la campaña de publicidad [IMPORTE] euros.

En pago de los servicios descritos el cliente entrega en el presente acto [IMPORTE]. euros en concepto de anticipo a cuenta, cantidad que la empresa de merchandising recibe manifestando su conformidad, y sirviendo el presente documento como carta de pago.

El pago de la cantidad restante se efectuará en el momento de la entrega del estudio de mercado por la empresa de merchandising al cliente en las fechas previstas, abonándose mediante ingreso en la cuenta corriente [Nº DE CUENTA (IBAN)].

[OPCIONAL — incluir si procede]

(Si media cesión de marcas y campañas de publicidad)

Dichas cantidades se abonarán del siguiente modo:

- Un [PORCENTAJE] % a la firma del presente contrato.
- Un [PORCENTAJE] % una vez presentados el estudio.
- Un [PORCENTAJE] % una vez obtenida la licencia de la marca [MARCA/MODELO]
- Un [PORCENTAJE] % una vez finalizada la campaña publicitaria.

Quinta.- Exclusividad

La Empresa de merchandising se compromete a no contratar prestaciones iguales o semejantes con otra empresa del sector de la del cliente durante [PLAZO]

Sexta.- Subcontratación

Para la celebración de este contrato, se ha tenido en cuenta la experiencia y buen hacer de la Empresa merchandasing por lo que se prohíbe la subcontratación de los servicios que tiene encomendados.

Séptima.- Confidencialidad

Las partes se obligan a guardar secreto y sigilo profesional sobre cuantos datos tenga acceso por razón del presente contrato, comprometiéndose a no revelar ni facilitar ninguna información. Esta obligación permanecerá aún después de extinguido de este contrato.

Las partes responderán del deber de secreto y confidencialidad por parte de sus empleados

Octava.- Protección de datos

La empresa de merchandising reconoce que la legislación sobre protección de datos personales (Ley Orgánica 3/2018, de 5 de diciembre, de protección de datos personales y garantía de derechos digitales) establece una serie de obligaciones en el tratamiento de datos de carácter personal, entre las que destaca la prohibición de realizar cesiones de datos de carácter personal sin la correspondiente autorización del titular de los datos personales. A tal efecto, la empresa de merchandising:

a) Únicamente accederá a los datos personales de clientes y demás personas físicas relacionadas con el cliente si tal acceso fuese necesario para cumplir con los servicios objeto del presente contrato.
b) Se compromete a:
- Utilizar los datos de carácter personal a los que tenga acceso única y exclusivamente para cumplir con sus obligaciones contractuales para con el cliente.
- Observar y adoptar cuantas medidas de seguridad sean necesarias para asegurar la confidencialidad, secreto e integridad de los datos de carácter personal a los que tenga acceso, así como a adoptar en el futuro cuantas medidas de seguridad sean exigidas por las leyes y reglamentos destinadas a preservar el secreto, confidencialidad e integridad en el tratamiento automatizado de datos personales.
- A no ceder en ningún caso a terceras personas los datos de carácter personal a los que tenga acceso, ni tan siquiera a efectos de su conservación.

Las obligaciones establecidas para la empresa de merchandising por la presente cláusula serán también de obligado cumplimiento para sus posibles empleados, colaboradores, tanto externos como internos, y subcontratistas, por lo que la empresa de merchandising responderá frente al cliente si tales obligaciones son incumplidas por tales empleados, colaboradores y subcontratistas.

El incumplimiento por parte de la empresa de merchandising de cualesquiera de las obligaciones establecidas en la anterior cláusula de Confidencialidad y en ésta de Tratamiento de Datos de Carácter Personal, generará una indemnización en favor del cliente de [IMPORTE]. euros, sin perjuicio del derecho del cliente a resarcirse de los perjuicios que le sean causados y que superen la cuantía indicada.

Novena.- Notificaciones

Las partes señalan como domicilios para la práctica de las notificaciones necesarias en la ejecución del presente contrato:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

Décima.- Impuestos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta de [NOMBRE DE LA PARTE]

Decimoprimera.- Naturaleza del contrato y normativa aplicable

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en su defecto, por lo dispuesto por la legislación mercantil y civil vigente, tanto española como de la Unión Europea que fuere de aplicación.

Decimosegunda.- Fuero competente

[ELEGIR UNA OPCIÓN: Si pacta sometimiento a tribunales / Si pacta someterse a arbitraje]

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

________________________________

Empresa de Mercandising

________________________________

Cliente

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

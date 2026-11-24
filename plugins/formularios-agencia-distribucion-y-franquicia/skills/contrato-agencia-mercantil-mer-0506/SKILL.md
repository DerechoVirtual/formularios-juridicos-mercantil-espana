---
name: contrato-agencia-mercantil-mer-0506
description: "Contrato de agencia mercantil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de agencia mercantil

> Formulario **MER-0506** del plugin **Agencia, distribución, franquicia y colaboración entre empresas** (`formularios-agencia-distribucion-y-franquicia`) · Mercantil › Agencia, distribución, franquicia y colaboración empresarial · normativa revisada el 24-11-2026.

## Qué es

Modelo de contrato de agencia mercantil, mediante el cual una empresa encarga a un agente que actúe en su representación para la promoción y venta de sus productos con o sin exclusiva. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del contrato, así como los derechos y obligaciones de cada una de las partes.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de agencia mercantil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de agencia mercantil” para mi caso». También puedes invocarla directamente con `/formularios-agencia-distribucion-y-franquicia:contrato-agencia-mercantil-mer-0506`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-agencia-distribucion-y-franquicia:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Agencia, distribución, franquicia y colaboración entre empresas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (10 veces)
- [ ] DNI/NIE (4 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] PLAZO (3 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] ÁMBITO TERRITORIAL (2 veces)
- [ ] DESCRIPCIÓN DE PRODUCTOS O SERVICIOS
- [ ] FECHA
- [ ] LISTADO DE CLIENTES
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] NÚMERO
- [ ] OTROS DATOS
- [ ] PROVINCIA

## Normas que cita el formulario

- art. 1.1 Ley 12/1992

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

Modelo de contrato de agencia mercantil, mediante el cual una empresa encarga a un agente que actúe en su representación para la promoción y venta de sus productos con o sin exclusiva. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento del contrato, así como los derechos y obligaciones de cada una de las partes.

Notas al pie del formulario original:
(1) El art. 1.1 de la Ley 12/1992, de 27 de mayo, sobre Contrato de Agencia (en lo sucesivo, LCAg.) regula única y exclusivamente los agentes que merecen el calificativo de intermediarios independientes.

A los efectos de ser considerados trabajadores autónomos económicamente dependientes, a estos agentes comerciales no les será de aplicación el requisito de asumir el riesgo y ventura de tales operaciones, contemplado en el artículo 11, apartado 2, letra e) de la Ley 20/2007, de 11 de julio, sobre el Estatuto del trabajador autónomo, vigente desde el 12 de octubre de 2007.

(2) El contrato de agencia puede pactarse por tiempo determinado o indefinido. Si no se fija una duración determinada, se entiende que el contrato ha sido pactado por tiempo indefinido. (art. 23 LCAg.)

Téngase en cuenta que, según el art. 26.1.b) LCAg., cada una de las partes de un contrato de agencia pactado por tiempo determinado o indefinido puede dar por finalizado el contrato en cualquier momento, sin necesidad de preaviso, cuando la otra parte haya sido declarada en concurso.

En caso de duración indefinida, se extingue por la denuncia unilateral de cualquiera de las partes mediante preaviso por escrito. El plazo de preaviso es de un mes para cada año de vigencia del contrato, con un máximo de 6 meses. Si el contrato de agencia ha estado vigente por tiempo inferior a un año, el plazo de preaviso será de un mes. Las partes pueden pactar mayores plazos de preaviso, sin que el plazo para el preaviso del agente pueda ser inferior, en ningún caso, al establecido para el preaviso del empresario. Y Salvo pacto en contrario, el final del plazo de preaviso coincidirá con el último día del mes. (art. 25 LCAg.)

(3) Si el agente tiene la exclusiva para una zona geográfica o para un grupo determinado de personas, tendrá derecho a la comisión siempre que el acto u operación de comercio se concluyan durante la vigencia del contrato de agencia con persona perteneciente a dicha zona o grupo, aunque el acto u operación no hayan sido promovidos ni concluidos por el propio agente. (art. 12.2 LCAg.)


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
(Datos del AGENTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, AGENTE.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de la EMPRESA)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, EMPRESA.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de AGENCIA y, a tal fin,

MANIFIESTAN

I.- Que LA EMPRESA se dedica a [ACTIVIDAD].

II.- Que EL AGENTE cuenta con experiencia en la representación comercial de dicho sector y con organización propia suficiente para el ejercicio de su actividad y se halla colegiado en el Colegio de Agentes de Comercio de [PROVINCIA] con el número [NÚMERO].

III.- Que ambas partes están interesadas en establecer relaciones comerciales

por las que el AGENTE colabore en introducir los productos o servicios en [ÁMBITO TERRITORIAL]

para las actividades que precise LA EMPRESA, y que por ello

ACUERDAN

Llevar a efecto el presente contrato de AGENCIA, mediante las siguientes:

CLÁUSULAS

Primera.- Objeto del contrato

La EMPRESA nombra a D./Dña. [NOMBRE Y APELLIDOS] AGENTE de la misma para que con la diligencia y buena fe con que en dicha calidad actúa le represente como intermediario independiente (El art. 1.1 de la Ley 12/1992, de 27 de mayo, sobre Contrato de Agencia regula única y exclusivamente los agentes que merecen el calificativo de intermediarios independientes) en la promoción y venta de los [ELEGIR: productos / servicios / productos y servicios] que se indican en el Anexo y en el ámbito geográfico que se señala en este contrato asumiendo el riesgo y ventura de las operaciones promovidas en la zona acordada y durante toda la vigencia del contrato.

Segunda.- [ELEGIR: Productos / Servicios / Productos y servicios]

Durante la vigencia del contrato, la EMPRESA queda facultada para la inclusión o exclusión de los [ELEGIR: productos / servicios / productos y servicios] que se recogen en el Anexo citado, previo aviso al AGENTE con una antelación mínima de [ELEGIR: días / semanas / meses] a la fecha de su efectividad, que será indicada en el documento enviado al AGENTE por [ELEGIR: carta / carta certificada / mail con firma electrónica / burofax]. Las citadas modificaciones tendrán eficacia a partir de la fecha indicada siempre que el AGENTE no comunique de manera fehaciente a la EMPRESA su decisión de rescindir el contrato por ese motivo, en cuyo caso no tendrá el AGENTE derecho a solicitar de la EMPRESA indemnización alguna en concepto de [ELEGIR: clientela / daños y perjuicios / clientela y daños y perjuicios].

Tercera.- Duración

[ELEGIR UNA OPCIÓN: Duración indefinida / Duración determinada]

[OPCIONAL — incluir si procede]

(Devolución a la empresa en caso de extinción)

La extinción o resolución del presente contrato supondrá la obligación de devolución por parte del AGENTE de todos los bienes proporcionados por la EMPRESA para el ejercicio de su actividad derivada del mismo en el plazo de [PLAZO] desde que sea efectiva la finalización del contrato.

Cuarta.- Ámbito geográfico y clientes y exclusividad

La actividad del AGENTE se realizará en [ÁMBITO TERRITORIAL]
la localidad
la provincia
el país
otra delimitación geográfica
[NOMBRE Y APELLIDOS], [ELEGIR: de manera exclusiva / no exclusiva], siendo por lo tanto el único AGENTE de LA EMPRESA en las zonas citadas.

Los clientes de la zona atribuida al AGENTE aportados por LA EMPRESA se describen en el Anexo II de este contrato. Previa justificación de su causa, LA EMPRESA queda expresamente facultada para ampliar o reducir dicho listado relación con los siguientes límites y consecuencias [OTROS DATOS].

[ELEGIR UNA OPCIÓN: Con exclusividad / Sin exclusividad]

Quinta.- Subagentes (La actuación por medio de subagentes requiere autorización expresa del empresario. Cuando el agente designe la persona del subagente, responderá de su gestión, art. 5.2 LCAg.)

El AGENTE podrá actuar a través de subagentes, designando para ello a:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS].

EL AGENTE será responsable de las actividades de sus subagentes, en las mismas condiciones que si las hubiese realizado él mismo.

Sexta.- Retribución del AGENTE (La remuneración del agente puede consistir en una cantidad fija, en una comisión o en una combinación de los dos sistemas anteriores. Art. 11.1 LCAg.)

[ELEGIR UNA OPCIÓN: Caso de retribución variable / Caso de retribución fija / Caso de retribución fija con variable]

Séptima.- Obligaciones del AGENTE

EL AGENTE se obliga a:

1. Ocuparse con la diligencia de un ordenado comerciante de la promoción y venta de los [ELEGIR: productos / servicios / productos y servicios] de LA EMPRESA especificados en el Anexo del presente contrato. Para ello, se encargará de la promoción adecuada de los [ELEGIR: productos / servicios / productos y servicios] entre los clientes radicados en la zona geográfica que tiene asignada.
[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— (Caso de instrucciones dadas por LA EMPRESA)
— (Caso de libertad del AGENTE en la política de ventas)
— 3. Asegurar la máxima satisfacción a los clientes radicados en la zona geográfica que tiene asignada, prestándoles la asistencia necesaria, antes y después de la adquisición de los [ELEGIR: productos / servicios / productos y servicios].
— (Caso de información periódica)
— (Caso de información bajo petición)
— 5. Mantener en la zona geográfica que tiene asignada una infraestructura económica, humana y adecuada en general para la promoción y venta de los [ELEGIR: productos / servicios / productos y servicios] especificados en el Anexo.
— 6. Recibir y atender en nombre de LA EMPRESA todas las reclamaciones que se presenten por terceros concernientes a vicios o defectos de la calidad de los [ELEGIR: productos / servicios / productos y servicios] de las operaciones promovidas, aunque no se hubiesen concluido, comunicando dicha información con la mayor brevedad a LA EMPRESA.

[OPCIONAL — incluir si procede]

7. Pacto de volumen mínimo de ventas

Las partes acuerdan fijar para la duración inicial del contrato un volumen mínimo de ventas en la zona geográfica acordada de [IMPORTE] euros. En caso de renovación del presente contrato por iguales periodos, la EMPRESA se compromete a establecer y notificar al AGENTE el objetivo de ventas para el nuevo periodo de vigencia del presente contrato. La falta de acuerdo por las partes con respecto a este extremo será causa de resolución automática del mismo, incluso aunque se haya iniciado ya el periodo de prórroga, sin que exista en este caso derecho por ninguna de las partes a reclamarse cantidad ninguna.

[OPCIONAL — incluir si procede]

Limitación de competencia

Tras la extinción del presente contrato EL AGENTE se abstendrá de intermediar a favor de otras empresas dedicadas a [ACTIVIDAD], ni promoverá operaciones de este tipo para mercantiles durante en

Octava.- Otras obligaciones de la EMPRESA diferentes a la retribución

[OPCIONAL — incluir si procede]

1. Formación

LA EMPRESA estará obligada a proporcionar y EL AGENTE a recibir con pleno aprovechamiento un curso de formación inicial sobre los [ELEGIR: productos / servicios / productos y servicios] de la EMPRESA incluidos en el Anexo I las concretas características, usos y especificaciones técnicas de los productos cuya promoción y venta tiene encomendada.

El curso tendrá una duración de [ELEGIR: días / semanas / meses] y se desarrollará íntegramente en las instalaciones de [NOMBRE DE LA PARTE] en [LOCALIDAD].

En caso de que el AGENTE no supere la formación proporcionada por LA EMPRESA o por la persona por ella designada expresamente, se entenderá automáticamente resuelto el presente contrato, sin que el AGENTE pueda solicitar a la EMPRESA ninguna cantidad en concepto de comisiones, retribución fija, indemnización por clientela o indemnización por daños y perjuicio, asumiendo además EL AGENTE la obligación de restituir el material de estudio que se le hubiese proporcionado.

Si el contrato se resolviera o finalizara antes de expirada la duración inicial del mismo por causa imputable al AGENTE, éste se verá obligado a devolver las cantidades abonadas por LA EMPRESA como gastos relativos al curso de formación en una proporción equivalente al tiempo que restase para completar el período inicial de vigencia del contrato.

. Información

La EMPRESA informará por escrito al AGENTE de las condiciones de venta de los [ELEGIR: productos / servicios / productos y servicios] que se mencionan en la Cláusula Segunda y Anexo de este contrato, así como cualquier variación que se produzca en las misma para que puedan ser exigibles al AGENTE.

La EMPRESA facilitará igualmente al AGENTE la relación completa de los [ELEGIR: productos / servicios / productos y servicios] y precios de venta, mediante los catálogos, muestras y material necesarios o convenientes para la negociación y demostración a los clientes.

[OPCIONAL — incluir si procede]

(De campañas y nuevos productos)

La EMPRESA informará al AGENTE de las posibles campañas de promoción de sus productos que se lleven a efecto con carácter previo al lanzamiento de las mismas, así como de la comercialización de nuevos [ELEGIR: productos / servicios / productos y servicios], proporcionándole de forma puntual los muestrarios nuevos necesarios para el desarrollo de su actividad. Igualmente, informará respecto de la retirada del mercado o de las previsiones sobre aumentos o disminuciones en las ventas de los mismos.

. Aceptación o rechazo de las operaciones propuestas [PLAZO]: la EMPRESA se compromete a comunicar al AGENTE la aceptación o rechazo de cada operación en una plazo máximo de [PLAZO], desde que a través del agente se reciba la preceptiva propuesta. La negación de la misma, será motivada señalando la falta de requisitos que la concreta operación no cumple. En caso de aceptación, es suficiente con que la EMPRESA remita al AGENTE copia de la aceptación que ha sido directamente enviada al cliente.

. Envío de [ELEGIR: productos / servicios / productos y servicios]

[ELEGIR UNA OPCIÓN: Con penalización en caso de no aprovisionamiento / General]

Novena.- Indemnización por clientela

Las partes acuerdan una indemnización por clientela, para los supuestos legalmente previstos, de [IMPORTE].

Décima.- Impuestos y gastos

Todos los impuestos, gastos judiciales o extrajudiciales originados a consecuencia de la celebración del presente contrato serán de cuenta [ELEGIR: del agente / de la empresa].

Decimoprimera.- Naturaleza del contrato

El presente contrato tiene naturaleza mercantil, rigiéndose por lo dispuesto en sus propias cláusulas y en lo en ellas no previsto por las disposiciones de la Ley sobre Contrato de Agencia, Ley 12/92, de 27 de Mayo, y en su defecto por lo previsto en el Código de Comercio, leyes especiales y usos mercantiles, y en su defecto por lo previsto en el Código Civil.

Decimosegunda.- Fuero competente

La competencia para el conocimiento de cuantas acciones derive del presente contrato corresponde a los Juzgados y Tribunales de [LOCALIDAD], domicilio del AGENTE, en cumplimiento de lo previsto en la Disposición Adicional Segunda de la Ley 12/92, de 27 de mayo, que regula el contrato de agencia.

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

LA EMPRESA

EL AGENTE

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]
Anexo I: descripción de productos o servicios de LA EMPRESA

[DESCRIPCIÓN DE PRODUCTOS O SERVICIOS]

Anexo II: listado de clientes de la EMPRESA cuyas cuentas gestionará el AGENTE (de modo exclusivo o no, según pacto).

[LISTADO DE CLIENTES]

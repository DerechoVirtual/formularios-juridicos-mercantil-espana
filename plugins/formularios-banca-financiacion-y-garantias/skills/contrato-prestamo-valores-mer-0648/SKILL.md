---
name: contrato-prestamo-valores-mer-0648
description: "Contrato de préstamo de valores. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de préstamo de valores

> Formulario **MER-0648** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Contrato marco por el que un cliente pone a disposición de su entidad financiera, para que los tome en préstamo, los valores depositados en su cuenta de valores, a cambio de un rendimiento. Regula los requisitos de los valores prestables, la perfección de cada préstamo, el régimen económico, el reintegro, los gastos y tributos y la duración indefinida del contrato.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de préstamo de valores» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de préstamo de valores” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-prestamo-valores-mer-0648`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FIRMA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE CUENTA (2 veces)
- [ ] DATOS REGISTRALES: LIBRO, TOMO, FOLIO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DNI/NIF
- [ ] FECHA
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS DEL CLIENTE
- [ ] NOMBRE Y APELLIDOS DEL REPRESENTANTE Y DATOS DE SU REPRESENTACIÓN
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL REPRESENTADO
- [ ] PROVINCIA

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

- Junto a «…encia de los servicios bancarios y responsabilidad en la concesión de préstamos.»: comprobar la vigencia y el texto actualizado de la circular citada.

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

COMPARECEN

De una parte, la ENTIDAD [DENOMINACIÓN SOCIAL], representada por [NOMBRE Y APELLIDOS DEL REPRESENTANTE Y DATOS DE SU REPRESENTACIÓN], constituida en escritura pública otorgada el día [FECHA] ante el Notario de [LOCALIDAD], [NOMBRE DEL NOTARIO], e inscrita en el Registro Mercantil de [PROVINCIA], [DATOS REGISTRALES: LIBRO, TOMO, FOLIO], domiciliada en [LOCALIDAD], calle [DOMICILIO], núm. [Nº], y con NIF núm. [NIF].

De otra, [NOMBRE Y APELLIDOS DEL CLIENTE], [ELEGIR: actuando por cuenta propia / actuando en representación de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL REPRESENTADO]] (en adelante, el/la CLIENTE), mayor de edad, con domicilio en [DOMICILIO], con DNI/NIF núm. [DNI/NIF].

El/la CLIENTE mantiene con LA ENTIDAD la cuenta de valores y la cuenta corriente de efectivo asociadas.

La ENTIDAD, en su condición de entidad participante de los sistemas de registro, compensación y liquidación de los mercados donde se negocien los valores propiedad del/de la CLIENTE, y que ahora o en el futuro estén depositados en la cuenta de valores mencionada, está facultada para tomarlos en préstamo.

Rendimiento nominal anual: [PORCENTAJE] %.

Tasa Anual Equivalente (T.A.E.): [PORCENTAJE] %.

Cuenta de valores asociada: [Nº DE CUENTA]

Cuenta corriente de efectivo asociada: [Nº DE CUENTA]

CLÁUSULAS

1. OBJETO DEL CONTRATO.

Mediante el presente contrato, el/la CLIENTE se compromete a poner a disposición de la ENTIDAD valores que, ahora o en el futuro, se encuentren depositados en su cuenta de valores, debidamente identificada, con la finalidad de que sean tomados en préstamo por la ENTIDAD, en las condiciones que aquí se pactan.

El/la CLIENTE deberá cumplir los siguientes requisitos para la puesta a disposición de los valores:

a) El/la CLIENTE cursará instrucciones (órdenes) a la ENTIDAD con la identificación concreta de los valores depositados en su cuenta, que el/la CLIENTE pone a disposición de la ENTIDAD para la finalidad de préstamo. El/la CLIENTE podrá ampliar o revocar, total o parcialmente, dichas órdenes en cualquier momento durante la vigencia de este contrato, sin otra condición que la de que el número de unidades de cada valor que el/la CLIENTE mantenga a disposición de la ENTIDAD en todo momento no sea inferior al mínimo determinado por ésta.

b) A su vez, los valores que el/la CLIENTE ponga a disposición de la ENTIDAD han de cumplir los siguientes requisitos: pertenecer al CLIENTE, por la realización de operaciones que ya están liquidadas. Deberán, además, encontrarse libres de toda carga y gravamen, limitación, restricción o suspensión; estar incluidos en la relación de valores objeto de préstamo que determine el respectivo órgano rector del mercado secundario donde se negocien; estar incluidos, también, en la relación de valores susceptibles de ser prestados a la ENTIDAD que ésta tenga establecida en cada momento y que el/la CLIENTE podrá consultar en sus sucursales.

Los valores que reúnan los requisitos anteriormente mencionados recibirán la denominación de valores prestables, tomándose nota de ello en la cuenta de valores del/de la CLIENTE.

Los valores prestables continúan perteneciendo al/a la CLIENTE, correspondiéndole, en consecuencia, todos los derechos políticos y económicos derivados de tales valores. Cualquier orden de transmisión, constitución de derechos reales o de traspaso de dichos valores a otra entidad participante exigirá una orden previa del/de la CLIENTE a la ENTIDAD revocando la condición de prestables.

La relación de valores prestables a su favor puede ser revocada en cualquier momento por la ENTIDAD. Ello implicará la pérdida inmediata de esta condición, a todos sus efectos, surgiendo para la ENTIDAD la única obligación de comunicar esta decisión al/a la CLIENTE.

El/la CLIENTE queda obligado/a a comunicar de forma inmediata y por escrito el fallecimiento, el concurso, la adopción de medidas judiciales de apoyo por situación de discapacidad o cualquier otra situación que pueda afectar a la libre disposición de los valores prestables en relación con cualquiera de los titulares de la cuenta de valores, implicando la pérdida inmediata de su condición de valores prestables.

2. EFICACIA DE LA OPERACIÓN DE PRÉSTAMO DE VALORES.

La ENTIDAD podrá, de forma total o parcial en función de sus necesidades, tomar en préstamo los valores prestables del/de la CLIENTE. Cada uno de estos préstamos quedará perfeccionado a medida que se efectúe la entrega de los valores a la ENTIDAD. Se consideran entregados los valores a la ENTIDAD en el momento de la asignación, a través del sistema de compensación y liquidación correspondiente, de las correspondientes referencias de registro a cada operación de préstamo. El/la CLIENTE, desde ese mismo momento, no puede disponer de esos valores y, mientras los tenga prestados a la ENTIDAD, no tendrá que hacer efectiva la comisión de depósito y administración de valores.

El/la CLIENTE recibirá periódicamente de la ENTIDAD el correspondiente extracto de la cuenta de valores, en el que se reflejarán las sucesivas operaciones de préstamo a favor de la ENTIDAD, con indicación expresa de sus condiciones de plazo y de base de cálculo del rendimiento pactado en la siguiente cláusula. La ENTIDAD comunicará estas operaciones al organismo rector del mercado. La ENTIDAD abrirá a nombre del/de la CLIENTE una cuenta de préstamo de valores. En ella quedarán reflejadas las sucesivas operaciones de préstamos que se celebren bajo el presente contrato, además de permitir conocer en todo momento los datos de la posición global del/de la CLIENTE y la ENTIDAD.

3. RÉGIMEN ECONÓMICO.

A las operaciones que se realicen al amparo del presente contrato se les aplicará el siguiente régimen económico: los préstamos devengarán un rendimiento a favor del/de la CLIENTE al tipo nominal [PORCENTAJE] %, desde el día de la entrega a la ENTIDAD de los valores hasta la fecha de amortización de cada préstamo. El rendimiento se liquidará en efectivo por la ENTIDAD el último día de cada trimestre natural, realizándose una liquidación con carácter final en la fecha de vencimiento del último préstamo vigente entre las partes. La base para el cálculo de este rendimiento será el precio medio ponderado de cada uno de los valores prestados existente al cierre del día en que se perfeccione cada operación de préstamo, conforme a los datos proporcionados por la sociedad rectora del mercado correspondiente o, en su caso, la sociedad de bolsas. A este rendimiento le corresponde, además, la Tasa Anual Equivalente (TAE), calculada conforme a lo que dispone la Circular del Banco de España 5/2012, de 27 de junio, a entidades de crédito y proveedores de servicios de pago, sobre transparencia de los servicios bancarios y responsabilidad en la concesión de préstamos.

Como consecuencia del carácter de este contrato, con duración indefinida y otorgando la facultad de cancelación anticipada a cualquiera de las partes, por su decisión y sin penalización alguna, la ENTIDAD podrá modificar el rendimiento de estos préstamos respecto de las operaciones de préstamo que se perfeccionen en el futuro. La ENTIDAD ha de comunicar las modificaciones realizadas al/a la CLIENTE con una antelación de [Nº] días, aunque las modificaciones que supongan un beneficio para el/la cliente surtirán efecto desde la fecha en que la ENTIDAD decida su aplicación. En el caso de que el/la CLIENTE no estuviera de acuerdo con la modificación prevista y lo comunicara a la ENTIDAD con una antelación de [Nº] días desde la fecha de la aplicación, podrá resolver la presente relación, de igual modo que los préstamos de valores vigentes a esa fecha, en cuyo caso se aplicarán las que se consideren como últimas condiciones aceptadas por el/la CLIENTE hasta que haya hecho constar su disconformidad a la ENTIDAD.

La ENTIDAD, además, abonará al/a la CLIENTE, en la fecha en que lo haga el emisor de los valores prestados, el importe correspondiente a los frutos y derechos económicos derivados de los mismos, incluida la devolución de aportaciones con ocasión de reducciones de capital y las primas de asistencia a juntas generales de accionistas, que se devenguen durante la vigencia de cada operación de préstamo. También se pondrá a disposición del/de la CLIENTE por parte de la ENTIDAD, el primer día correspondiente al periodo de suscripción, el importe correspondiente a los derechos de asignación gratuita y de suscripción preferente de las nuevas acciones que se creen durante la vigencia de las operaciones de préstamo, procediéndose a valorar estos derechos por el valor teórico que pudieren tener a la fecha de cierre del día inmediato anterior al inicio de la negociación de tales derechos en el mercado organizado correspondiente. Todas las cantidades que se generen a favor del/de la CLIENTE y que deban ser abonadas por la ENTIDAD lo serán en la cuenta de efectivo correspondiente.

4. CONDICIONES APLICABLES A LAS OPERACIONES DE PRÉSTAMO DE VALORES.

4.1. Los derechos políticos derivados de los valores prestados corresponden a la ENTIDAD, dejando el/la CLIENTE de ser su titular.

4.2. Se estima una duración máxima de un año para cada una de las operaciones de préstamo perfeccionadas bajo la cobertura del presente contrato. Este plazo se contará a partir de la fecha de la perfección y la ENTIDAD deberá informar al/a la CLIENTE de la duración concreta que se asigne a cada operación. Tanto el/la CLIENTE como la ENTIDAD podrán proceder a la cancelación total o parcial de forma anticipada y sin penalización.

4.3. La ENTIDAD deberá reintegrar al/a la CLIENTE otros valores de la misma clase y con idénticas condiciones que los prestados, al vencimiento previsto o anticipado de cada una de las operaciones de préstamo. Tales valores quedarán depositados en la cuenta de valores del/de la CLIENTE.

4.4. Los valores reintegrados por la ENTIDAD al vencimiento de las operaciones de préstamo que cumplan los requisitos previstos en la cláusula 1 de este contrato quedarán de forma automática en situación de valores prestables, salvo en el supuesto de que el vencimiento de la operación de préstamo se haya producido de forma anticipada por voluntad del/de la CLIENTE, en cuyo caso será preciso que se curse expresamente orden por su parte en los términos que se exponen en dicha cláusula para que los valores vuelvan a adquirir la condición de prestables. El/la CLIENTE queda obligado/a, respecto de dichos valores y como titular de los mismos, a hacer efectiva a la ENTIDAD la comisión de depósito y administración de valores a partir del momento en que los valores sean reintegrados a la ENTIDAD.

4.5. Se aplicarán las reglas siguientes, en caso de que se procediera a la ejecución material de algunas de las operaciones societarias que a continuación se señalan, para el cumplimiento por parte de la ENTIDAD de su obligación de reintegro de los valores que son objeto del préstamo:

a) Cuando la operación llevada a cabo sea la modificación del valor unitario de los valores prestados por una causa diferente del aumento o reducción del capital social del emisor, o si los valores prestados han sido objeto de conversión o canje a consecuencia de una fusión u otra operación estructural distinta de las señaladas a continuación, la ENTIDAD reintegrará al/a la CLIENTE, al vencimiento del préstamo, un número equivalente de nuevos valores resultantes de dichas operaciones societarias y, en su caso, el importe en metálico de la compensación económica que se tuviese que hacer efectiva a consecuencia de estas operaciones.

b) En caso de amortización por el emisor de los valores prestados, la ENTIDAD abonará al/a la CLIENTE el importe de dicha amortización al vencimiento del préstamo.

c) En caso de suspensión de la cotización de los valores a la fecha de vencimiento del préstamo, o si fuera día inhábil en el mercado secundario en que éstos sean objeto de negociación, o no existiera liquidez en el mercado de estos valores, se entenderá prorrogado el vencimiento del préstamo hasta la fecha en que se reanude la negociación efectiva del valor, y queda la ENTIDAD obligada a reintegrar al/a la CLIENTE en dicha fecha los valores objeto del préstamo.

d) Si los valores hubieran sido excluidos de la cotización en la fecha del vencimiento del préstamo, la ENTIDAD hará efectivo al/a la CLIENTE, a modo de sustitución de la prestación inicialmente pactada, el importe en dinero satisfecho por el emisor como contraprestación en la correspondiente oferta pública de adquisición de acciones.

5. GASTOS Y TRIBUTOS.

Cada una de las partes del presente contrato satisfará los gastos y tributos que le corresponda satisfacer legalmente como consecuencia de la realización de las operaciones de préstamo de valores que se formalicen por este contrato. La ENTIDAD retendrá la cantidad correspondiente a los rendimientos de capital mobiliario, o la que proceda de acuerdo con la normativa fiscal vigente, sobre las cantidades abonadas al/a la CLIENTE por los distintos conceptos.

6. DURACIÓN DEL CONTRATO.

Este contrato tiene una duración indefinida, con independencia de la duración de las operaciones particulares que cabe realizar a su amparo. Cualquiera de las partes puede darlo por finalizado en cualquier momento, ejercitando su facultad de resolución a través de comunicación escrita dirigida a la otra parte. Dicha resolución supondrá la pérdida de la condición de prestables de los valores que el/la CLIENTE tiene a disposición de la ENTIDAD en el momento de su ejercicio, impidiendo, eso sí, la cancelación anticipada de las operaciones de préstamo de valores ya perfeccionadas en esa fecha, según lo previsto en este contrato.

PROTECCIÓN DE DATOS

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento del Reglamento (UE) 2016/679 (RGPD), de la Ley Orgánica 3/2018, de 5 de diciembre, de Protección de Datos Personales y garantía de los derechos digitales, y demás normativa aplicable.

EL/LA CLIENTE: [FIRMA]	P.P. LA ENTIDAD: [FIRMA]

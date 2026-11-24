---
name: contrato-credito-cuenta-corriente-reconocimiento-deuda-mer-0665
description: "Contrato de crédito en cuenta corriente con reconocimiento de deuda. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de crédito en cuenta corriente con reconocimiento de deuda

> Formulario **MER-0665** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de crédito en cuenta corriente con reconocimiento de deuda» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de crédito en cuenta corriente con reconocimiento de deuda” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-credito-cuenta-corriente-reconocimiento-deuda-mer-0665`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] NIF (3 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] CLAVE DE OFICINA
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº
- [ ] PERIODICIDAD
- [ ] SUCURSAL
- [ ] TIPO DE INTERÉS

## Normas que cita el formulario

- art. 11 Código de Comercio

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

DECLARACIÓN Y RECONOCIMIENTO DE CRÉDITO

Número del crédito Oficina Importe Oficina [SUCURSAL] clave [CLAVE DE OFICINA] número lugar [LOCALIDAD]

En [LUGAR], a [DÍA] de [MES] de [AÑO].

El Banco [ENTIDAD BANCARIA] (en adelante Banco) por la presente póliza concede una operación de crédito en cuenta corriente en las condiciones y con las garantías que se indican:

Acreditados y Fiadores [NOMBRE Y APELLIDOS]

Para la extracción de fondos de esta cuenta de crédito y ordenar cargos en la misma quedan autorizados:

Don [NOMBRE Y APELLIDOS] NIF [NIF]

Don [NOMBRE Y APELLIDOS] NIF [NIF]

Don [NOMBRE Y APELLIDOS] NIF [NIF]

CARACTERÍSTICAS DEL CRÉDITO

- Límite

- Tipo de interés nominal anual.

- Comisión de apertura.

- % intereses sobre excesos.

- Cuenta asociada.

- Reducciones parciales.

- Primer vencimiento.

- Vencimiento final.

- Tasa anual equivalente (no incluye corretaje ni la comisión de disponibilidad).

- Carencia para las reducciones.

- Primer vencimiento de intereses en el período de carencia.

CLÁUSULAS Y CONDICIONES

El BANCO [ENTIDAD BANCARIA] concede a los ACREDITADOS, solidariamente, una cuenta corriente de crédito mercantil por el importe límite expresado y con el resto de características que se indican en el presente contrato.

La parte acreditada se obliga a la devolución del crédito solidariamente.

Asimismo, la parte acreditada que concierta esta operación, declara que la finalidad de la misma es la atención de necesidades distintas de las de consumo.

Los firmantes, con renuncia a su propio fuero, se someten expresamente a los Tribunales de [LOCALIDAD] para cuantas incidencias se deriven de lo pactado.

En la cuenta corriente de crédito se adeudarán las cantidades de que disponga la parte acreditada así como los intereses, comisiones y gastos motivados por la operación, y se abonarán las cantidades que se reintegren y los intereses correspondientes a los saldos favorables a la parte acreditada.

Los saldos deudores que se produzcan en la cuenta corriente de crédito devengarán a favor del Banco el interés al tipo nominal pactado.

Si por cualquier motivo el saldo deudor del crédito excediera del límite vigente en cada momento, el Banco podrá aplicar sobre la parte excedida el tipo sobre excesos pre- visto, este último tipo también se podrá aplicar por parte del Banco, sobre la totalidad del saldo deudor del crédito, si la operación hubiera llegado al vencimiento pactado.

Los saldos a favor de la parte acreditada devengarán el tipo de interés nominal del [TIPO DE INTERÉS]

0,10 por 100 anual.

Para el cálculo de los intereses se utilizará la siguiente fórmula: I = Intereses del período de liquidación.

i = Saldos; Di = Días permanencia; In = Tasa de interés nominal. I = E Si. di.in / 36.000

La liquidación de intereses se realizará por el Banco trimestralmente.

Se pactan las siguientes comisiones, a abonar al Banco por la parte acreditada, cuya cuantía es la que figura en el cuadro de características y cuyo concepto, base de cálculo y devengo son los que seguidamente se expresan:

a) Comisión de apertura, a percibir en este mismo acto, por una sola vez, cuya base de cálculo es el límite de la cuenta corriente de crédito.

b) Comisión de disponibilidad, que se devengará y liquidará trimestralmente (junto con los intereses) sobre el saldo medio no dispuesto del límite vigente.

El vencimiento final del crédito se pacta sin perjuicio de las reducciones parciales del límite convenidas, que deben producirse con la cadencia y en las mismas fechas de los vencimientos de intereses y por los importes convenidos, determinando así el límite vigente en cada momento.

No obstante el vencimiento final pactado, el Banco podrá anticiparlo dando por resuelto el presente contrato, sin necesidad de cumplir otro requisito, en los siguientes supuestos:

a) Incumplimiento de cualquiera de las obligaciones asumidas por cualquiera de los ACREDITADOS o FIADORES en este contrato y en especial la de no superar el límite vigente y la de no efectuar las reducciones del límite pactadas.

b) En caso de que cualquiera de los ACREDITADOS o FIADORES falleciera, solicitase o fuera declarado en estado de insolvencia temporal o definitiva (suspensión de pagos,

quiebra o concurso de acreedores) o incurriera en alguna causa que disminuya o modifique su capacidad civil.

c) Si a juicio razonable del Banco se alterase notoriamente la solvencia de cual- quiera de los ACREDITADOS o FIADORES por incumplimiento de obligaciones económicas u otras circunstancias que supongan la interrupción de su normal actividad o hagan peligrar su unidad patrimonial.

d) Si cualquiera de los ACREDITADOS o FIADORES se viese en la obligación de reembolsar anticipadamente cualquier crédito obtenido de otras instituciones financieras, sufriera embargo de sus bienes o incurriera en protesto de efectos mercantiles.

e) Falseamiento o inexactitud de la información facilitada por cualquiera de los

ACREDITADOS o FIADORES al Banco.

En los casos anteriores el Banco podrá exigir de los ACREDITADOS y FIADORES la cancelación anticipada del crédito y la devolución total e inmediata de las cantidades adeudadas.

Igualmente, el Banco podrá suspender la disponibilidad de cantidades con cargo al crédito, en cualquiera de los casos antes enumerados v siempre que, a juicio del Banco, la operación no resultase suficientemente garantizada y en tanto no lo sea a su satisfacción, de acuerdo con los parámetros económicos que se tuvieron en cuenta en el momento de la concesión.

Por su parte, cualquiera de los ACREDITADOS o FIADORES podrá resolver este contrato en cualquier momento, previo pago y reembolso al Banco de todas las cantidades adeudadas.

La liquidación del crédito practicada por el Banco hará fe en juicio, considerándose líquida la cantidad que de ella resulte.

Todos los impuestos y gastos, incluso los de intervención, que hoy gravan o en lo sucesivo graven esta clase de operaciones, serán de cuenta y cargo de la parte acreditada. Asimismo, estarán a su cargo los gastos y costas de la reclamación judicial de este crédito o su preparación con diligencias preparatorias, incluso honorarios del letrado, procurador y de otras personas intervinientes, aunque la misma fuese potestativa.

La parte fiadora se declara enterada del contenido del presente contrato, respondiendo solidariamente entre sí y con la parte acreditada de las obligaciones asumidas por ésta, renunciando expresamente a los beneficios de excusión, división y orden, así como cualquier notificación en caso de incumplimiento o resolución contractual, respondiendo en la misma forma, tiempo y condiciones que la parte acreditada, aunque el Banco prorrogue la operación y no exija a su vencimiento la cantidad prestada.

La parte acreditada y la parte fiadora se obligan a facilitar anualmente al Banco los oportunos estados contables actualizados que permitan el análisis económico- financiero de su empresa o negocio.

Igualmente, todos los ACREDITADOS y FIADORES se obligan a comunicar al Banco, con carácter inmediato, todo cambio de régimen económica matrimonial y, de ser comerciante, los actos de oposición y revocación a que alude el artículo 11 del Código de Comercio.

El Banco facilitará a la parte acreditada información de los movimientos contables, de [PERIODICIDAD]

las liquidaciones trimestrales de intereses y comisiones y de las modificaciones de las condiciones de la operación que se produzcan.

Como lugar de cumplimiento del presente contrato se señala por las partes la Oficina Principal del Banco sita en Zaragoza, plaza del General Depié, [Nº] No obstante el Banco podrá autorizar a las partes ACREDITADA y FIADORA para que utilicen los servicios del Banco de cualquiera de sus oficinas.

A los efectos de notificaciones se tendrá como domicilio de ACREDITADOS y FIADO- RES el que se hace constar en el presente contrato. ACREDITADOS y FIADORES quedan obligados a notificar por escrito al Banco el cambio de su domicilio; en todo caso, el nuevo domicilio para notificaciones que se designe deberá estar comprendido dentro de los límites del territorio nacional.

Para el caso de que el límite de la cuenta corriente de crédito sea rebasado (bien sea por exceso o bien por vencimiento de la operación), la parte acreditada se obliga a mantener en la cuenta asociada saldo suficiente para hacer efectivos íntegra- mente dichos excesos mediante adeudo en aquélla, sin que el Banco quede obligado a realizar aplicaciones parciales.

Sin perjuicio de lo pactado en el párrafo anterior, el Banco queda autorizado irrevocablemente para aplicar, con destino al reintegro de las cantidades adeudadas, cualquier saldo o depósito del que cualquiera de los ACREDITADOS o FIADORES puedan ser titulares en el Banco, bien en numerario o en valores de cualquier clase. La presente no podrá ser revocada hasta el completo pago de todas las cantidades adeudadas.

Tratamiento automatizado de datos (Ley Orgánica 3/2018). ACREDITADOS y FIADORES declaran conocer la existencia de un fichero automatizado de datos de carácter personal, los cuales han sido recogidos para poder concertar y desarrollar la relación contractual con el Banco destinatario de la información. ACREDITADOS y FIADORES declaran conocer los derechos que les asisten de acceso, rectificación y cancelación de los datos del fichero ubicado en la Oficina Principal del Banco en Zaragoza.

Las partes intervinientes, en prueba de conformidad con su contenido, otorgan y firman el presente contrato en los ejemplares necesarios para su entrega a cada una de las partes, reconociendo las partes recibir uno de ellos a su formalización. Y yo, el fedatario público que interviene, doy fe de la identidad y capacidad de las partes, de la legitimidad de sus firmas y de lo convenido en el presente contrato, que firmo y sello en el lugar y fecha indicados a su comienzo.

Los Prestatarios,	Los Fiadores,
El Banco Con mi intervención

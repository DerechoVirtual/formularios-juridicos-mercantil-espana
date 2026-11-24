---
name: contrato-mercantil-cuenta-corriente-mer-0669
description: "Contrato mercantil de cuenta corriente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato mercantil de cuenta corriente

> Formulario **MER-0669** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato mercantil de cuenta corriente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato mercantil de cuenta corriente” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-mercantil-cuenta-corriente-mer-0669`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] TIPO DE INTERÉS (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE CHEQUES

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

PÓLIZA DE CONTRATO MERCANTIL DE CUENTA CORRIENTE

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL BANCO", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "EL CLIENTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE DEL NOTARIO], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente y teniendo a juicio del Corredor Público interviniente la capacidad legal en Derecho necesaria para concertar la presente PÓLIZA DE CONTRATO MERCANTIL DE CUENTA CORRIENTE, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO Que EL CLIENTE es una persona jurídica de derecho privado dedicada a la [ACTIVIDAD]

SEGUNDO Que EL BANCO es una persona jurídica de derecho privado dedicada a la [ACTIVIDAD]

TERCERA Que por todo lo anterior, ambas partes de común acuerdo llevan a efecto el presente contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

EL BANCO admite entregas del TITULAR para la apertura de cuenta corriente desde la cantidad de [IMPORTE] euros.

Los criterios de valoración de apuntes practicados e la cuenta son los derivados de las tarifas que, en su momento, mantenga el BANCO, registradas en el Banco de España de conformidad con las normas de transparencia bancaria.

Órdenes de pago

EL BANCO resultará obligado por las órdenes de pago del CLIENTE siempre que exista en cuenta provisión suficiente de fondos para la atención de los pagos.

EL BANCO sólo cumplirá órdenes de pago remitidas por teléfono, télex, telefax, banca electrónica o Internet si incluyen la clave convenida garantizadora de autenticidad.

Intereses y comisiones

3.1 Comisiones

EL BANCO podrá aplicar una comisión semestral de mantenimiento de la cuenta de [IMPORTE] euros.

3.2 Intereses de saldos acreedores

El saldo acreedor de la cuenta devengará un interés del [TIPO DE INTERÉS] % nominal anual, capitalizable mensualmente. La fórmula aplicada para liquidar interese será:

I= (saldos por valoración x días de permanencia en la cuenta de depósito x tipo de interés nominal pactado) / 36.000

3.3 Intereses de saldos deudores

Los saldos deudores de la cuenta corriente devengarán un interés de demora del [TIPO DE INTERÉS] % nominal anual.

Cheques y talonarios

EL BANCO proporcionará a EL CLIENTE los talonarios de cheques, cuyo costo será pagado por EL CLIENTE al momento de su recepción o mediante cargo a su cuenta. EL CLIENTE, podrá adicionalmente disponer de los fondos de su cuenta corriente mediante órdenes impartidas por escrito a EL BANCO.

EL BANCO no será responsable de los perjuicios que pudiera experimentar EL CLIENTE por la pérdida o la sustracción de cheques o por la falsificación de su firma o de otros datos consignados en el cheque. EL BANCO no será responsable del pago de los cheques girados contra la cuenta de EL CLIENTE, salvo que hubiera a simple vista, diferencias notorias entre la firma consignada en el cheque y la firma de EL CLIENTE registrada en EL BANCO, y/o borrones o enmendaduras que induzcan a EL BANCO a suponer que pudiera haber sido falsificado o adulterado el cheque en todas o algunas de sus partes.

La orden de revocación comunicada a EL BANCO después de efectuado el pago, no generará responsabilidad alguna para este último.

EL BANCO rechazará el pago de los cheques girados sin fondos disponibles en la cuenta corriente. EL BANCO cerrará las cuentas corrientes de EL CLIENTE, en caso este último gire [Nº DE CHEQUES] cheques sin tener fondos disponibles, durante seis meses computados desde la fecha del primer rechazo, en las cuentas que mantenga en EL BANCO. Para tales efectos, se incluyen las cuentas corrientes de las cuales EL CLIENTE sea cotitular. Sin perjuicio de lo anterior, EL BANCO podrá a su elección autorizar el sobregiro en cuenta.

Información

El Banco enviará todos los meses a EL CLIENTE, el estado de su cuenta corriente al domicilio que haya indicado al producirse la apertura de la misma, salvo indicaciones especiales aceptadas por EL BANCO.

En el improbable caso que EL CLIENTE no recibiera por algún motivo su estado de cuenta, dentro de los 10 primeros días del mes siguiente podrá recabarlo en la oficina de EL BANCO en la que hubiera abierto la misma dentro de los 10 días posteriores. En caso así no lo hiciera, se entenderá para todos los efectos del presente contrato que EL CLIENTE ha recibido en su domicilio, el estado de cuenta, conforme a lo previsto en el párrafo anterior.

EL CLIENTE se obliga a revisar los estados mensuales de su cuenta, y en su caso, notificar directamente a EL BANCO si advirtiera algún error u omisión, indicando el detalle del mismo.

Retenciones

EL BANCO no se responsabiliza por los perjuicios que pudieran producirse por retenciones de saldos en la cuenta de EL CLIENTE, en cumplimiento de mandatos legales, judiciales y del pago de los importes retenidos, en los términos ordenados a EL BANCO por las autoridades que los hubieran expedido.

Cierre de la cuenta corriente

7.1 Cierre a instancia de EL CLIENTE

EL CLIENTE podrá solicitar el cierre de su cuenta en cualquier momento, dando aviso por escrito a EL BANCO con diez días de anticipación. EL BANCO podrá negarse a la solicitud que le formule EL CLIENTE para el cierre de su cuenta corriente, en el caso que la misma arroje saldo deudor o que EL CLIENTE mantuviese obligaciones pendientes de pago con EL BANCO.

7.2 Cierre a instancia de EL BANCO

Por su parte, y además de las causales indicadas en el presente contrato, EL BANCO podrá cerrar la cuenta corriente en cualquier momento, previo aviso a EL CLIENTE, descargando su responsabilidad sobre la misma, mediante el envío a EL CLIENTE de un cheque o giro, pagadero a su orden, por el saldo que hubiere a su favor, o reclamando el pago en la forma establecida por la Ley, si el saldo resulta deudor.

7.3 Fallecimiento del titular

EL BANCO cerrará la cuenta corriente tan pronto tenga conocimiento del fallecimiento, de EL CLIENTE. En estos casos, los saldos luego de cubiertas las obligaciones con EL BANCO, serán puestos a disposición de los herederos, tribunales o curador, según sea el caso. EL BANCO no se responsabiliza de las operaciones que se hubiesen producido antes de tomar conocimiento del respectivo hecho, de recibir la comunicación pertinente o de ser notificado con el mandato judicial respectivo.

7.4 Efectos del cierre de la cuenta corriente

EL CLIENTE, se obliga a devolver en un plazo máximo de tres días calendario, todos los cheques que no hubieren sido girados hasta el momento del cierre de la cuenta corriente.

Producido el cierre de la cuenta corriente, EL BANCO tiene expedito su derecho para exigir de EL CLIENTE el pago del saldo deudor de la misma, en su caso, más los intereses compensatorios, moratorios y comisiones que se hubieren devengado hasta el cierre de la cuenta, así como los que se devenguen a partir del cierre y los gastos de cobro en que incurra EL BANCO, hasta su total cancelación.

Producido el cierre de la cuenta corriente, EL BANCO tiene expedito su derecho para exigir de EL CLIENTE el pago del saldo deudor de la misma, en su caso, más los intereses compensatorios, moratorios y comisiones que se hubieren devengado hasta el cierre de la cuenta, así como los que se devenguen a partir del cierre y los gastos de cobro en que incurra EL BANCO, hasta su total cancelación.

Cuenta mancomunada

Son aplicables específicamente a las cuentas mancomunadas además de las otras disposiciones contenidas en el presente contrato en lo que no se contradigan, las siguientes:

a) Todos los titulares de las mismas son responsables en forma solidaria ante EL BANCO, de cualquier saldo deudor u operación de crédito que se hubiere convenido bajo la cuenta corriente.

b) EL BANCO sólo pagará cheques girados o ejecutará órdenes escritas impartidas conjuntamente por todos los titulares o en su caso por los representantes cuyas firmas se encuentren debidamente registradas en EL BANCO.

c) Los titulares en forma conjunta podrán solicitar el cierre de la cuenta, con una anticipación no menor de [Nº] días. En este caso, los saldos que resultaren a favor de los titulares, luego de cerrada la cuenta y cubiertas las obligaciones para con EL BANCO, serán entregados al conjunto de los titulares, salvo instrucciones en contrario al momento de dar aviso de cierre.

d) EL BANCO queda autorizado para efectuar retenciones hasta por el saldo de la cuenta, en cumplimiento de mandatos legales, judiciales o de ejecutores coactivos, dirigidos contra uno o varios de los titulares de la cuenta.

e) Al producirse el fallecimiento, quiebra o interdicción de uno cualesquiera de los titulares de la cuenta, EL BANCO cerrará la cuenta y pondrá los saldos a disposición de los demás titulares y de los herederos, tribunal o curador, según sea el caso, previa verificación de su condición por parte de EL BANCO, en proporción al número de titulares de la cuenta, salvo que al momento de la apertura de la cuenta se haya indicado una proporción distinta.

f) Los titulares en forma conjunta podrán dar instrucciones para que EL BANCO pague cheques girados o ejecute órdenes escritas impartidas en forma indistinta por uno cualesquiera de ellos. Si tal fuera el caso, los titulares declaran que tales actos se consideran para todos los efectos legales, como actos de pura administración, para los que los titulares conceden por el mérito de tal instrucción a EL BANCO, un mandato recíproco, por lo que no requiere su validez o eficacia frente a EL BANCO, de formalidad adicional alguna.

Procedimiento ejecutivo

En el supuesto de descubiertos en cuenta corriente, a los efectos del procedimiento ejecutivo, se tendrá por cantidad exigible la especificada por EL BANCO, que se tendrá por líquida siempre que conste en documento intervenido por Fedatario Público que acredite haberse practicado la liquidación en la forma pactada por las partes en esta póliza y que el saldo coincide con el que aparece en la cuenta corriente abierta AL CLIENTE, a los efectos prevenidos en la Ley de Enjuiciamiento Civil.

[ELEGIR UNA OPCIÓN: Sumisión a Tribunales / Jurisdicción competente y ley aplicable / Sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal en caso de no ejecución voluntaria de la sentencia / — y además elegir: Sumisión a arbitraje / Sin cláusula penal en caso de no ejecución voluntaria del laudo / Con cláusula penal en caso de no ejecución voluntaria del laudo]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fe pública

El presente contrato se formaliza con intervención de Fedatario Público especialmente requerido a todos los efectos legales. Las partes manifiestan su conformidad con el presente contrato que otorgan y firman con mi intervención en [Nº] ejemplares igualmente originales y auténticos formalizados a un solo efecto, quedando un original en mi archivo. Y yo, Fedatario Público, hechas las advertencias legales y en particular las de carácter fiscal, doy fe de la identidad y capacidad de las partes, de la legitimidad de su firma y de todo lo convenido en la presente póliza que firmo y sello en el lugar y fecha al principio indicados.

Fdo. Don [NOMBRE Y APELLIDOS]

(El BANCO)

Fdo. Don [NOMBRE Y APELLIDOS]

(El CLIENTE)

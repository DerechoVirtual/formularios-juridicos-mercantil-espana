---
name: contrato-general-compraventa-mercantil-mer-0596
description: "Contrato general de compraventa mercantil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato general de compraventa mercantil

> Formulario **MER-0596** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato general de compraventa mercantil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato general de compraventa mercantil” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-general-compraventa-mercantil-mer-0596`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (13 veces)
- [ ] LOCALIDAD (9 veces)
- [ ] NÚMERO (9 veces)
- [ ] IMPORTE (8 veces)
- [ ] FECHA (5 veces)
- [ ] Nº (5 veces)
- [ ] FOLIO (4 veces)
- [ ] INSCRIPCIÓN (4 veces)
- [ ] SECCIÓN (4 veces)
- [ ] TOMO (4 veces)
- [ ] MES (3 veces)
- [ ] AÑO (2 veces)
- [ ] CALLE (2 veces)
- [ ] CARGO (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DÍA (2 veces)
- [ ] NIF (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] SEDE (2 veces)
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] HORA
- [ ] LUGAR
- [ ] LUGAR DE ENTREGA
- [ ] SUCURSAL
- [ ] TÍTULO DE ADQUISICIÓN

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

En [LUGAR], a [FECHA].

Reunidos

DE UNA PARTE

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Persona física)

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], vecindad civil común y provisto de NIF número [NIF], como COMPRADORA.

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Persona jurídica)

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de la mercantil «[DENOMINACIÓN SOCIAL]» y en calidad de [CARGO], cuya representación acredita mediante copia de la escritura de poder otorgada el día [DÍA] de [MES] de [AÑO] ante el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS] bajo el número [NÚMERO] de su protocolo, inscritos dichos poderes en el Registro Mercantil Provincial de al tomo [TOMO], folio [FOLIO], sección [SECCIÓN], hoja número [NÚMERO], inscripción [INSCRIPCIÓN] La mencionada sociedad tiene su domicilio social en calle [CALLE], número [NÚMERO], e inscrita en el Registro Mercantil de [LOCALIDAD], al tomo [TOMO], folio [FOLIO], sección [SECCIÓN], hoja número [NÚMERO], inscripción [INSCRIPCIÓN] y con C.I.F., denominado en lo sucesivo el COMPRADORA.

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Persona representada)

D./Dña. [NOMBRE Y APELLIDOS], en condición de tutor de su hermano incapaz D./Dña. [NOMBRE Y APELLIDOS] según auto dictado por el Tribunal de Instancia de [SEDE].

Y

DE OTRA PARTE

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Persona física)

De otra parte, D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD], vecindad civil común y provista de NIF número [NIF], como VENDEDORA

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Persona jurídica)

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de la mercantil «[DENOMINACIÓN SOCIAL]» y en calidad de [CARGO], cuya representación acredita mediante copia de la escritura de poder otorgada el día [DÍA] de [MES] de [AÑO] ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS] bajo el número [NÚMERO] de su protocolo, inscritos dichos poderes en el Registro Mercantil Provincial de [PROVINCIA] al tomo [TOMO], folio [FOLIO], sección [SECCIÓN], hoja número [NÚMERO], inscripción [INSCRIPCIÓN] La mencionada sociedad tiene su domicilio social en [LOCALIDAD], calle [CALLE], número [NÚMERO], e inscrita en el Registro Mercantil de [LOCALIDAD], al tomo [TOMO], folio [FOLIO], sección [SECCIÓN], hoja número [NÚMERO], inscripción [INSCRIPCIÓN] y con C.I.F., denominado en lo sucesivo el VENDEDORA.

[OPCIONAL — incluir si procede]

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Persona representada)

D./Dña. [NOMBRE Y APELLIDOS], en condición de Defensor Judicial del incapaz D./Dña. [NOMBRE Y APELLIDOS], designado el día [FECHA] según auto dictado por el Tribunal de Instancia de [SEDE].

Intervienen

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes con capacidad jurídica y de obrar suficiente y que mutuamente se reconocen, libremente y de común acuerdo convienen en otorgar el presente CONTRATO DE COMPRAVENTA MERCANTIL

Exponen

Primero.– Que la VENDEDORA es propietaria en régimen de plena propiedad y dominio de [DESCRIPCIÓN DEL BIEN], por título de [TÍTULO DE ADQUISICIÓN], en lo sucesivo, "Los Mercancías".

Segundo.– Que los Mercancías se encuentra libre de toda carga o gravamen y no existe sobre los mismos contienda judicial o de cualquier otra índole.

Tercero.– Que interesando a la COMPRADORA la adquisición de los Mercancías, y a la VENDEDORA la enajenación de los mismos, ambas partes de común acuerdo llevan a efecto la presente compraventa con arreglo a las siguientes:

Cláusulas

Objeto.–

Constituye el objeto del presente contrato la compraventa de los bienes descritos en la parte expositiva del presente contrato.

Precio.–

El precio de los bienes descritos en la cláusula primera se concreta en la cantidad de [IMPORTE] euros ( €) más el Impuesto sobre el Valor Añadido correspondiente, esto es, [IMPORTE] euros ( €) adicionales. El precio total de la operación asciende a la cantidad [IMPORTE] euros ( €).

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Forma de pago.–

No aplazado

El pago se efectuará el día [FECHA] en la cuenta corriente nº [NÚMERO] que la VENDEDORA tiene suscrita con la entidad en su sucursal [SUCURSAL].

Aplazado

Pago a tercero.–

El precio total de la operación asciende a la cantidad [IMPORTE] euros (€), de los cuales en este acto LA COMPRADORA entrega a LA VENDEDORA [IMPORTE] euros ( €). Los restantes [IMPORTE] euros ( €) las retendrá LA COMPRADORA en su poder para satisfacer con ella la deuda de [IMPORTE] euros ( €) por orden de LA VENDEDORA, sin que por ello asuma responsabilidad personal alguna.

Cláusula de reserva de dominio.–

La venta se entiende hecha con reserva de dominio a favor de LA VENDEDORA, hasta el momento en que el importe total del presente contrato de compraventa haya sido satisfecho, esto es, hasta el día [FECHA]

LA COMPRADORA está obligada a hacer constar debidamente ante cualquier pretensión de embargo el carácter de depósito con el que los Mercancías se encuentran en su poder y, si a pesar de todo, fuera embargada por resolución judicial, lo comunicará a LA VENDEDORA en las cuarenta y ocho horas inmediatas a que tal hecho tuviera lugar.

De la misma forma, en el supuesto de que por cualquier otra causa, como por ejemplo el robo, LA COMPRADORA fuera privada del bien objeto de este contrato, ésta deberá ponerlo en conocimiento inmediato de LA VENDEDORA con el fin de que pueda adoptar las acciones que estime oportunas al respecto, sin que por ello se vea liberada de la obligación del pago íntegro del precio de la mercancía. En el supuesto de que la parte compradora omitiera esta obligación, se entenderá que existe responsabilidad por su parte en el destino final del bien y mala fe en su comportamiento.

Asimismo, LA COMPRADORA responderá de los daños y perjuicios que sobrevinieran a la misma, incluso por caso fortuito, durante el periodo de vigencia de la obligación suspensiva.

La cláusula de reserva de dominio a favor de la parte vendedora quedará automáticamente extinguida en el momento en que LA COMPRADORA haya pagado la totalidad del precio pactado. De esta forma, la mercancía vendida pasará a ser de plena propiedad de LA COMPRADORA sin limitación alguna.

Por el contrario, si llegado el vencimiento de cualquiera de los pagos éste no se hubiera verificado, LA COMPRADORA deberá devolver los Mercancías adquiridos en virtud del presente contrato de forma inmediata, encontrándose un representante de la mercantil vendedora plenamente legitimado para acudir a las dependencias de LA COMPRADORA y recoger el objeto de este contrato a su voluntad sin necesidad de procedimiento especial alguno, ya que para tal fin le faculta la misma desde el momento de la suscripción de este contrato.

La enajenación o la realización de cualquier otro acto de disposición en tanto no se haya verificado efectivamente el pago requerirá la autorización previa y por escrito de la vendedora.

Entrega.–

Los Mercancías objeto del presente contrato se entregarán en [LUGAR DE ENTREGA] el día [FECHA] de [MES] del año en curso, entre las [HORA] y las [Nº] horas. Los gastos de dicho transporte correrán a cargo de la parte

La COMPRADORA se compromete a aceptar las mercancías una vez hayan sido entregadas si coinciden con las calidades, forma y tamaño descritos en el Exponendo Primero.

En caso contrario dispondrá de un plazo de [Nº] días a partir de esa fecha para la solicitud de sustitución de las mercancías que resulten defectuosas o que no se ajusten a dichas características.

El plazo de sustitución de las piezas no será superior a [Nº] días. En caso de que la VENDEDORA no proceda a la sustitución dentro de ese plazo, la COMPRADORA podrá proceder a exigir el cumplimiento o la resolución del contrato, con abono en ambos casos de los daños y perjuicios que se le hayan irrogado.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Transmisión del riesgo.–

En dependencias de la vendedora

LA COMPRADORA asumirá el riesgo por el menoscabo o los daños que los bienes vendidos pudieran sufrir desde el momento en que se hubieran individualizado y hubiesen sido puestos formalmente a su disposición en las dependencias de LA VENDEDORA.

En dependencias de la compradora

Resolución del contrato.–

El Contrato podrá resolverse por las siguientes causas:

1. Por voluntad de cualquiera de las Partes cuando medie incumplimiento grave de las obligaciones pactadas.
2. Por acuerdo de las Partes por escrito.
3. La extinción de la personalidad jurídica de cualquiera de las Partes o la suspensión de pagos, quiebra, concurso o embargo de bienes de alguna de ellas a menos que se garantice de cualquier forma la deuda.

En cualquier caso, la Parte que pretenda resolver el presente Contrato alegando incumplimiento de la contraparte, deberá requerirle al cumplimiento de la obligación de forma fehaciente, otorgándole un plazo de [Nº] días a la Parte incumplidora para que pueda subsanar dicho incumplimiento. Transcurrido dicho plazo sin que los incumplimientos hubiesen sido subsanados, el perjudicado podrá ejercitar la mencionada facultad.

En el supuesto de que los incumplimientos fueren de imposible subsanación en el plazo de 30 días, el perjudicado podrá ejercitar directamente la facultad opción, sin necesidad de remitir, previamente, el antedicho requerimiento.

La resolución del contrato por esta causa producirá los mismos efectos que el incumplimiento de la obligación de pago en lo que a recuperación de las mercancías e indemnización de los daños y perjuicios respecta.

Cláusula penal.–

En caso de resolución del contrato por causa imputable a la COMPRADORA, la VENDEDORA no estará obligada a la devolución de las cantidades satisfechas hasta ese momento, cantidades que se considerarán indemnización por daños y perjuicios, fijándose además una cantidad adicional de [IMPORTE] € como indemnización que la COMPRADORA deberá abonar a la VENDEDORA.

La resolución del contrato legitimará a la VENDEDORA a tomar plena posesión de las Mercancías por sus propios medios, sin necesidad de previa declaración judicial, ni de autoridad alguna, renunciando la COMPRADORA de modo expreso a oponerse de modo alguno a la actuación en este sentido de la VENDEDORA, quien podrá libremente disponer de dichos bienes.

Gastos e impuestos.–

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Sumisión a tribunales.–

Sin cláusula penal

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse a los Tribunales de [LOCALIDAD], en [PROVINCIA], renunciando expresamente a su fuero propio si lo tuvieran.

El presente contrato tiene carácter mercantil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

Con cláusula penal

Sumisión a arbitraje.–

Sin cláusula penal

Para cuantas cuestiones o divergencias pudieran suscitarse en relación con el presente contrato, ambas partes establecen someterse al Arbitraje de Derecho de la Cámara de Comercio de [LOCALIDAD].

El presente contrato tiene carácter mercantil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por lo previsto en el Código de Comercio, demás leyes especiales y usos mercantiles.

Con cláusula penal

Notificaciones.–

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Generalidades.–

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE COMPRAVENTA MERCANTIL, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

PARTE VENDEDORA	PARTE COMPRADORA

Fdo. D./Dña. [NOMBRE Y APELLIDOS]: Fdo. D./Dña. [NOMBRE Y APELLIDOS]:

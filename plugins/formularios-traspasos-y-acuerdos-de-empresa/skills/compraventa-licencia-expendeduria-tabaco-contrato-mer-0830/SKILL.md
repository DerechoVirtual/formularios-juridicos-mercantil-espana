---
name: compraventa-licencia-expendeduria-tabaco-contrato-mer-0830
description: "Compraventa de licencia de expendeduría de tabaco (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Compraventa de licencia de expendeduría de tabaco (contrato)

> Formulario **MER-0830** del plugin **Traspasos de negocio, confidencialidad y acuerdos de empresa** (`formularios-traspasos-y-acuerdos-de-empresa`) · Mercantil › Otros documentos mercantiles · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Compraventa de licencia de expendeduría de tabaco (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Compraventa de licencia de expendeduría de tabaco (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-traspasos-y-acuerdos-de-empresa:compraventa-licencia-expendeduria-tabaco-contrato-mer-0830`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-traspasos-y-acuerdos-de-empresa:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Traspasos de negocio, confidencialidad y acuerdos de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (5 veces)
- [ ] IMPORTE (5 veces)
- [ ] Nº (5 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] CALLE
- [ ] ENSERES TRANSMITIDOS
- [ ] FINCA
- [ ] FOLIO
- [ ] LUGAR
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE ESTANCIAS
- [ ] Nº DE PROTOCOLO
- [ ] NÚMERO
- [ ] TOMO
- [ ] ÓRGANO
- [ ] ÓRGANO ADMINISTRATIVO

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].dos mil [AÑO]

MANIFIESTAN

I.- Que el vendedor es titular de una licencia de estanco - expenduría de tabaco y timbre -, concedida el [DÍA] de [MES] de [AÑO], por [ÓRGANO ADMINISTRATIVO], mediante concurso público, por plazo de 25 años, tal y como se acredita con el documento que se acompaña como Anexo I.

Que el vendedor manifiesta que la referida licencia se encuentra en vigor, y que no está incurso en ningún procedimiento que ponga en peligro la validez de la misma.

II.- Que a raíz de la nueva normativa que regula el sector, entrada en vigor el [DÍA] de [MES] de [AÑO], el vendedor ostenta la facultad de vender dicha licencia a terceras personas, siempre que éstas no se encuentren incursas en causa que les inhabilite a tal efecto.

Que en cumplimiento de la referida normativa, las partes deben presentar la documentación requerida por el Comisionado para el Mercado de Tabaco, perteneciente al Ministerio de Economía y Hacienda, para que apruebe la transmisión, motivo por el cual se acompaña al presente contrato la misma, como Anexo II, debidamente cumplimentada, para ser remitida al citado Organismo.

III.- Que el vendedor es igualmente propietario mediante escritura de compraventa otorgada ante el Notario D [NOMBRE DEL NOTARIO], el [DÍA] de [MES] de [AÑO], con número de protocolo [Nº DE PROTOCOLO] del local donde desarrolla la actividad relacionada con la licencia de estanco, considerado apto por los Organismos competentes, que se encuentra en la calle [CALLE], número [NÚMERO], de [LOCALIDAD].

El referido local se encuentra libre de arrendamientos y cargas, y tiene una superficie de [Nº] m2, divididos en [Nº DE ESTANCIAS] estancias, y está inscrito con número de finca [FINCA], en el Registro de la Propiedad de [LOCALIDAD], al tomo [TOMO], folio [FOLIO], inscripción

Se encuentran dentro del local, y resultan objeto, así mismo, de la presente transmisión, la siguiente maquinaria, enseres, [ENSERES TRANSMITIDOS].

IV.- Que interesando al comprador la obtención de la licencia que ha sido comentada, así como la adquisición del local que igualmente ha sido descrito, para el desarrollo de la referida actividad, las partes convienen en celebrar el presente contrato de compraventa de licencia de estanco, y de local de negocio, el cual se regirá por las siguientes

CLÁUSULAS

Objeto del contrato

El vendedor acuerda con el comprador la compraventa de la licencia de estanco que ha sido descrita, y del local de negocio donde la misma se explota, junto con sus existencias.

Condiciones de la licencia

El comprador manifiesta que conoce las condiciones de la licencia, así como las obligaciones que adquiere, una vez sea titular de la misma, en lo referente a la normativa administrativa que regula la actividad objeto de contrato.

Precio

El vendedor establece los siguientes precios sobre sus bienes:

1º Licencia: se fija un precio de [IMPORTE] Euros.

2º Local de negocio: se fija un precio de [IMPORTE] euros.

Forma de pago

Las partes acuerdan abonar las cantidades que han sido descritas en la anterior cláusula de la siguiente manera:

1º Pago inicial: [IMPORTE] euros, a la firma del contrato, mediante (transferencia/talón/), sirviendo el presente documento como formal carta de pago.

2º Pago aplazado: [IMPORTE] euros, a la firma de la escritura pública de compraventa, mediante [ÓRGANO].

Condición suspensiva

Como quiera que resulta necesario que el Comisionado para el Mercado de Tabaco apruebe la transmisión de la licencia de expenduría de tabaco y timbre, las partes se obligan a presentar la misma, al día siguiente a la firma del presente documento, junto con el contrato de compraventa, al objeto de que el referido Organismo pueda estudiar la operación, y resolver sobre la misma.

La venta objeto del presente contrato se verifica con la condición suspensiva de que se cumplan los siguientes extremos:

1º Que el comprador cumpla con los requisitos exigidos en la legislación vigente para ser concesionario.

2º Que el vendedor obtenga la autorización del Comisionado para el Mercado de Tabaco, para proceder a la venta.

El vendedor se obliga a justificar el extremo contenido en el apartado 2º anterior, por la autorización del Comisionado para el Mercado de Tabacos a esta transmisión, en el plazo de [Nº] días posteriores a la resolución que se obtenga del referido Organismo.

El incumplimiento de dicha obligación permitirá al comprador a resolver este contrato, quedando liberado, en este supuesto de resolución, del pago del precio convenido, y debiendo abonarle el vendedor, [IMPORTE] euros como penalización por el citado incumplimiento.

Escritura de compraventa

Las partes se comprometen a otorgar la correspondiente escritura de compraventa, ante el Notario D. [NOMBRE Y APELLIDOS], en un plazo máximo de [Nº] días, a partir de la recepción de la autorización del Comisionado para el Mercado de Tabaco, obligándose el comprador a notificar fehacientemente con [Nº] días de antelación a la firma, la fecha y hora de la misma, al vendedor.

Sólo a partir de la fecha en que se otorgue la escritura de compraventa que ha sido mencionada, accederá a la titularidad de la licencia el comprador, manteniéndose hasta entonces como propietario, el vendedor, quien deberá explotar el negocio de la misma manera que hasta el momento.

Condiciones económicas del estanco

El vendedor acompaña al presente contrato, como Anexos IV y VI, balance de pérdidas y ganancias de los tres últimos años, relativos a la explotación del negocio, y declaraciones fiscales que acreditan la realidad de los referidos resultados.

En el supuesto de que, una vez iniciada la actividad por el comprador, apareciese una deuda o pasivo oculto que no figurase en el balance, el comprador deberá avisar en un plazo de [Nº] días al vendedor, quien deberá liquidar la misma, de manera íntegra, incluyendo aquellos gastos o intereses que se hubieran podido haber generado por el mero transcurso del tiempo, o la falta de pago de la misma.

En el supuesto de que el vendedor considerara no debida dicha cantidad, deberá poner a disposición del comprador toda aquella documentación que así lo acredite, al objeto de justificar el impago, y eludir la liquidación exigida.

Incumplimiento del contrato

En el supuesto de incumplimiento del contrato en lo referente al otorgamiento de la escritura pública de compraventa, las partes acuerdan las siguientes repercusiones:

1º Si incumpliera el vendedor, negándose a firmar la escritura de compraventa a la fecha en que se hubiera establecido con los requisitos formales del presente contrato, sin causa que lo justifique, el comprador tendrá derecho a escoger entre obligar al vendedor a transmitirle los bienes objeto del presente contrato, en las condiciones pactadas, o resolver el mismo, penalizando al vendedor con el pago de una indemnización que ascendería al duplo de lo abonado hasta el momento por el comprador.

2º Si incumpliera el comprador, negándose a firmar la escritura de compraventa a la fecha en que se hubiera establecido con los requisitos formales del presente contrato, sin causa que lo justifique, el vendedor tendrá derecho a escoger entre obligar al comprador a adquirir los bienes objeto del presente contrato, en las condiciones pactadas, o resolver el mismo, penalizando al comprador con la pérdida de las cantidades abonadas hasta el momento.

Eficacia del contrato

En el supuesto de que alguna de las clausulas fuera declarada ineficaz, de manera originaria o sobrevenida, las partes acuerdan que el resto del contrato mantenga su validez.

Gastos e impuestos

Todos los gastos de elevación a público del contrato y, en su caso, impuestos indirectos derivados del otorgamiento del mismo serán soportados por el comprador, a salvo de la plusvalía municipal, que será liquidada por el vendedor.

Sumisión expresa

Las partes se someten a los Tribunales de [LOCALIDAD], con renuncia expresa de su fuero, o del que les pudiera corresponder, para resolver cualquier cuestión que pudiera surgir de la interpretación o aplicación del presente contrato.

Domicilios de las partes

Las partes designan como domicilios a efectos de notificaciones, los recogidos al inicio del presente contrato.

Si por cualquier causa hubieran de modificar los mismos, habrán de notificar fehacientemente a la contraparte el domicilio donde poder realizarse las correspondientes notificaciones.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de su conformidad, firman las partes el presente documento y sus anexos en el lugar y fecha señalados ut supra.

Firmas

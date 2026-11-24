---
name: compraventa-acciones-nominativas-entre-personas-mer-0145
description: "Compraventa de acciones nominativas entre personas físicas (contrato). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Compraventa de acciones nominativas entre personas físicas (contrato)

> Formulario **MER-0145** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Compraventa de acciones nominativas entre personas físicas (contrato)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Compraventa de acciones nominativas entre personas físicas (contrato)” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:compraventa-acciones-nominativas-entre-personas-mer-0145`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (17 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] AÑO (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] MES (4 veces)
- [ ] DÍA (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] FECHA (2 veces)
- [ ] FOLIO (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] TOMO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] ENTIDAD BANCARIA
- [ ] FECHAS
- [ ] HOJA
- [ ] INSCRIPCIÓN
- [ ] LEGISLACIÓN APLICABLE
- [ ] LIBRO
- [ ] NACIONALIDAD
- [ ] NIF
- [ ] OTROS DATOS

## Normas que cita el formulario

- art. 120.1 TRLSC
- art. 120.2 TRLSC

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

En [LOCALIDAD], a [DÍA], de [MES], [AÑO]

MANIFIESTAN

I. Que el Vendedor es accionista de la entidad mercantil [DENOMINACIÓN SOCIAL], entidad de nacionalidad [NACIONALIDAD] con domicilio social en [LOCALIDAD], número [NÚMERO] y provista de Número de Identificación Fiscal [NIF]. Constituida mediante escritura pública autorizada por el Notario de [LOCALIDAD] Don [NOMBRE DEL NOTARIO] el [DÍA] de [MES] de [AÑO], bajo el número [NÚMERO] de su protocolo, e inscrita el [DÍA] de [MES] de [AÑO] en el Registro Mercantil de [LOCALIDAD], en el tomo [TOMO], folio [FOLIO], hoja [HOJA], inscripción [INSCRIPCIÓN] en adelante, «la Compañía».

II. Que el actual capital social de la Compañía se cifra en la suma de [IMPORTE] euros, dividido en [Nº] acciones de [IMPORTE] euros de valor nominal cada una de ellas.

III. Que el Vendedor es titular de [Nº] acciones nominativas de la Compañía, números [Nº] a la [Nº] y números [Nº] a la [Nº], [OTROS DATOS] todas ellas inclusives, por un valor nominal total de [IMPORTE] euros, que están totalmente desembolsadas y que representan el [PORCENTAJE] % del capital social de la Compañía y que está interesado en vender dichas acciones al Comprador.

IV. Que el Comprador está interesado en adquirir las acciones descritas en el III Manifestando.

V. Que, en virtud de las consideraciones precedentes, las Partes, libre y voluntariamente, han acordado otorgar el presente Contrato de compraventa de acciones con sujeción a las siguientes

Cláusulas

1. Objeto

El Vendedor vende al Comprador, que compra las acciones descritas en el apartado III Manifestando por el precio y en los términos y condiciones que se señalan en el presente Contrato.

Título: El Vendedor acredita la titularidad de tales acciones en virtud de sendos títulos: En cuanto a las acciones [Nº] al [Nº] y las números [Nº] a la [Nº], todas ellas inclusive derivan de las dos escrituras públicas autorizadas por el Notario de [LOCALIDAD], Don [NOMBRE DEL NOTARIO], los días [FECHAS] y día [FECHA], números [Nº] y [Nº] de su protocolo, las cuales son la primera de ellas las de la propia constitución de la Compañía, y la otra correspondiente a una ampliación de capital social, respectivamente (En el supuesto se supone que no se han impreso ni entregado los títulos, por lo que, según indica el art. 120.1 TRLSC, se habrá de proceder conforme a las normas sobre la cesión de créditos y demás derechos incorporales; es decir, arts. 347 y 348 Cco. y 1526-1536 CC. Si las acciones estuvieran impresas, se haría constar los datos y legitimidad de los títulos).

Inscripción: En el Registro Mercantil de [LOCALIDAD], tomo [TOMO], libro [LIBRO], folio [FOLIO].

Cargas: Libre de cualquier carga y gravamen.

2. Precio

El Vendedor vende y transmite al Comprador las [Nº] acciones números [Nº] a la [Nº], y números [Nº] y [Nº] todas ellas inclusive, que le corresponden en la Compañía, por el precio total de [IMPORTE] euros.

El pago deberá efectuarse durante todo el día [FECHA] del mes de [MES] de [AÑO].

El medio de pago del Comprador del precio de las acciones se realizará mediante transferencia bancaria a la cuenta número [NÚMERO] del banco [ENTIDAD BANCARIA] del Vendedor.

[Cláusula optativa:

El pago se realizará del siguiente modo:

a) Un primer pago inicial:

b) Un segundo pago: ]

3. Transmisión de la titularidad

La transmisión de las acciones descritas en el Manifestando III, implicará asimismo, la transmisión de todos los derechos políticos y económicos inherentes a ellas (Si las acciones que se trasmiten estuvieran impresas documentalmente la transmisión se podrá cumplimentar mediante endoso (vid. art. 120.2 II TRLSC)).

4. Obligaciones del Vendedor

El Vendedor se compromete a la transmisión de las acciones descritas en el III Manifestando, asumiendo la responsabilidad por vicios ocultos y al saneamiento por evicción.

5. Obligaciones del Comprador

El Comprador se compromete a satisfacer puntualmente el precio convenido en el presente Contrato.

6. Manifestaciones y Garantías

El Vendedor garantiza, en su calidad de accionista de la Compañía, que:

a) Se han cumplido todos los requisitos previstos en los Estatutos Sociales en orden a la transmisión de las acciones anteriormente mencionadas.

b) Que las acciones objeto del presente Contrato le pertenecen en pleno dominio por justos y legítimos títulos.

c) Que no existen cargas ni gravámenes de naturaleza real sobre dichas acciones.

d) Que las acciones de la Compañía representan el [PORCENTAJE] % del capital de dicha sociedad a la fecha del presente Contrato.

7. Régimen

El presente Contrato se rige en lo no previsto expresamente, por la legislación mercantil y supletoriamente, por las disposiciones del Código Civil.

8. Notificaciones

a) Todas las notificaciones, requerimiento, peticiones y otras comunicaciones que hayan de efectuarse por las Partes en relación con el presente Contrato, deberán realizarse por escrito y se entenderá que han sido debidamente realizadas cuando hayan sido entregadas en mano o bien remitidas por correo certificado al domicilio de la otra Parte que conste en el encabezamiento del presente Contrato, o bien a cualquier otro domicilio que a estos efectos cada Parte pueda indicar a la otra.

b) El vendedor comunicará en el plazo máximo de tres días a la sociedad la presente transmisión, indicando su fecha, la identidad de las partes y el objeto transmitido, así como los demás datos exigibles conforme a las normas legales o estatutarias aplicables.

9. Gastos e impuestos

Todos los gastos e impuestos que se deriven de la presente compraventa serán de cuenta y cargo del comprador.

10. Ley aplicable y jurisdicción competente

El presente Contrato se regirá e interpretará de acuerdo con las Leyes de [LEGISLACIÓN APLICABLE] y se someterá a la jurisdicción de los Tribunales de [LOCALIDAD].

11. Arbitraje (opción alternativa a la cláusula 10)

Para la solución de cualquier cuestión litigiosa derivada del presente Contrato, las Partes se someten al arbitraje institucional del Tribunal Arbitral de [LOCALIDAD], al que se le encarga la designa del árbitro o árbitros y la administración del arbitraje, obligándose desde ahora al cumplimiento de la decisión arbitral.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Las Partes manifiestan su conformidad con el presente Contrato, que otorgan y firman en dos ejemplares igualmente originales, en el lugar y fecha arriba indicados.

El Vendedor El Comprador

Don/Doña [NOMBRE Y APELLIDOS] Don/Doña [NOMBRE Y APELLIDOS]

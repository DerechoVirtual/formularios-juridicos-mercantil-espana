---
name: contrato-compraventa-mercantil-sobre-muestras-calidad-mer-0590
description: "Contrato de compraventa mercantil sobre muestras o calidad conocida. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de compraventa mercantil sobre muestras o calidad conocida

> Formulario **MER-0590** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 25-11-2026.

## Qué es

Contrato mercantil de compraventa de mercancías sobre muestras (art. 327 del Código de Comercio), con precio al contado o aplazado, reserva de dominio, entrega, peritos para decidir si los géneros son de recibo, resolución, cláusula penal opcional y sumisión a tribunales o a arbitraje.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de compraventa mercantil sobre muestras o calidad conocida» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de compraventa mercantil sobre muestras o calidad conocida” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-compraventa-mercantil-sobre-muestras-calidad-mer-0590`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (9 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] NÚMERO (8 veces)
- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (5 veces)
- [ ] PROVINCIA (4 veces)
- [ ] IMPORTE EN LETRA (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] DNI/NIE (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] ENTIDAD BANCARIA (2 veces)
- [ ] ESTADO CIVIL (2 veces)
- [ ] HORA (2 veces)
- [ ] IBAN (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] SEDE (2 veces)
- [ ] SUCURSAL (2 veces)
- [ ] AÑO
- [ ] COLEGIO PROFESIONAL MATERIAL Y TERRITORIALMENTE COMPETENTE
- [ ] DESCRIPCIÓN DE LAS CARACTERÍSTICAS DE LAS MUESTRAS
- [ ] DESCRIPCIÓN DE LAS MERCANCÍAS
- [ ] LUGAR DE ENTREGA
- [ ] MES
- [ ] TIPO DE IVA

## Normas que cita el formulario

- art. 1365 Código Civil
- art. 327 Código de Comercio
- art. 338 Código de Comercio
- art. 34 Ley 60/2003

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

- Junto a «…bienes de alguna de ellas, a menos que se garantice de cualquier forma la deuda.»: la causa 3 puede resultar ineficaz en caso de concurso (art. 156 del texto refundido de la Ley Concursal, citado en las notas de ayuda); valorar su redacción.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE AYUDA

Este contrato, de conformidad con el artículo 327 del Código de Comercio, es el que se realiza sobre muestras o determinando calidad conocida en el comercio.

En cuanto a los intervinientes, si se trata de una persona física que interviene en su propio nombre y derecho es preciso hacer constar tal extremo. Lo mismo sucede si interviene en representación de otra persona física; en este caso será necesario describir la fuente de la que dimana su representación, ya sea esta legal o convencional. En el mismo sentido, si se trata de una persona física que actúa en beneficio de una sociedad de gananciales, de una sociedad civil irregular o de una comunidad de bienes, puesto que en estos casos no existe una personalidad jurídica diferente de la de los miembros que la integran.

Respecto de los pagos no satisfechos puntualmente por el comprador, recuérdese que la Ley 3/2004, de 29 de diciembre, por la que se establecen medidas de lucha contra la morosidad en las operaciones comerciales, establece la aplicación automática de un tipo de interés de demora, sin necesidad de aviso de vencimiento ni de intimación alguna por parte del acreedor. No obstante, el acreedor solo podrá exigir el pago de los intereses de demora cuando haya cumplido con las obligaciones contractuales y legales que le incumbían y cuando el retraso en el pago no sea imputable a su conducta. Si se dan estas condiciones, se devengará el interés de demora contractual o el fijado legalmente conforme a dicha ley.

Para la entrega de las mercancías habrá que tener en cuenta las siguientes apreciaciones. En el caso de que el comprador se niegue a recibir el producto, el artículo 332 del Código de Comercio establece que «Si el comprador rehusare sin justa causa el recibo de los efectos comprados, podrá el vendedor pedir el cumplimiento o rescisión del contrato, depositando judicialmente en el primer caso las mercaderías». No obstante, mediante sentencia núm. 1043/2007, de 1 de octubre de 2007, la jurisprudencia del Tribunal Supremo ha proclamado la inaplicación de la exigencia de depósito judicial que el artículo 332 del Código de Comercio impone al vendedor, en supuestos de rescisión voluntaria unilateral del contrato por el comprador. Así, recuerda la sentencia de 21 de noviembre de 2001, con cita de la de 28 de marzo de 1928, que «el vendedor que ha cumplido con todas sus obligaciones, incluso la entrega de mercancías, por la tradición ficta admitida en nuestro derecho, tenía el arbitrio y la opción para entablar un pleito de indemnización de daños y perjuicios por la rescisión injusta del contrato efectuada por el comprador». Ya la sentencia de 25 de febrero de 1948 consideraba que «no es aplicable el artículo 332 en los casos de tradición ficta».

De conformidad con el artículo 342 del Código de Comercio, «El comprador que no haya hecho reclamación alguna fundada en los vicios internos de la cosa vendida, dentro de los treinta días siguientes a su entrega, perderá toda acción y derecho a repetir por esta causa contra el vendedor». No obstante, se trata de un plazo para reclamar los defectos y diferencias existentes entre lo efectivamente entregado al comprador y lo realmente contratado (excepción non adimpleti contractus). En el caso de que lo entregado sea algo diferente a lo contratado, resultando inhábil para la finalidad para la que fue adquirido (caso de aliud pro alio), los plazos para ejercitar las acciones no son los del artículo 342 del Código de Comercio. En estos casos, la sentencia del Tribunal Supremo de 30 de diciembre de 2003 considera que entra en juego la doctrina del «aliud pro alio» y, por ende, es de aplicación el artículo 1124 del Código Civil en los casos de entrega de cosa inservible, con independencia de que la venta sea civil o mercantil (sentencias de 29 de febrero de 1988, 24 de mayo y 30 de octubre de 1989, 29 de abril y 10 de noviembre de 1994 y 1 de diciembre de 1997). En definitiva, los compradores no solo tienen las acciones protectoras de los vicios ocultos, sino también las que nacen del incumplimiento o anómalo cumplimiento del contrato (sentencias del Tribunal Supremo de 1 de junio de 1982, 10 de junio de 1983, 20 de febrero y 19 de diciembre de 1984, 6 de marzo de 1985, 15 de junio de 1987 y 3 de abril de 2002, entre otras).

En relación con la efectividad de la cláusula de reserva de dominio y su oponibilidad a terceros, hay que tener en cuenta lo dispuesto en el artículo 15 de la Ley 28/1998, de 13 de julio, de Venta a Plazos de Bienes Muebles.

Téngase en cuenta que el texto refundido de la Ley Concursal, en su artículo 156, establece que «se tendrán por no puestas las cláusulas que establezcan la facultad de la otra parte de suspender o de modificar las obligaciones o los efectos del contrato, así como la facultad de resolución o la de extinción del contrato por la declaración de concurso de cualquiera de ellas o por la apertura de la fase de liquidación de la masa activa».

En caso de resolución del contrato por causa imputable a la compradora, tener en cuenta que la conceptuación de las arras penales por el artículo 1152 del Código Civil conduce a afirmar que, salvo que las partes acuerden lo contrario, la satisfacción de la pena sustituye a la indemnización de daños y abono de intereses en caso de falta de cumplimiento, desempeñando así una función propiamente liquidatoria. En el mismo sentido, la sentencia del Tribunal Supremo (Sala de lo Civil, Sección 1ª) de 27 de junio de 2007.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

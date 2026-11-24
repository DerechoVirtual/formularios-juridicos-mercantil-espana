---
name: contrato-intermediacion-obtener-modificar-creditos-mer-0653
description: "Contrato de intermediación para obtener o modificar créditos, préstamos y servicios financieros. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de intermediación para obtener o modificar créditos, préstamos y servicios financieros

> Formulario **MER-0653** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de intermediación para obtener o modificar créditos, préstamos y servicios financieros» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de intermediación para obtener o modificar créditos, préstamos y servicios financieros” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-intermediacion-obtener-modificar-creditos-mer-0653`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (2 veces)
- [ ] DÍA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] MES (2 veces)
- [ ] FECHA
- [ ] GESTIONES ENCOMENDADAS
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] NÚMERO
- [ ] PORCENTAJE

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

MANIFIESTAN:

1) LA EMPRESA es una entidad mercantil que opera dentro del mercado financiero español, ejerciendo actuaciones de intermediación.

2) EL CLIENTE está interesado en contratar la prestación de servicios de intermediación financiera por LA EMPRESA.

3) Estando interesadas ambas partes, por medio del presente formalizan CONTRATO PRIVADO DE INTERMEDIACIÓN de acuerdo con las siguientes

ESTIPULACIONES

EL CLIENTE encarga a LA EMPRESA la intermediación financiera, comercial o bancaria, que consistirá en la realización de cuantas gestiones o trámites sean preciso para llevar a cabo para la (en cada caso se haría constar las gestiones encomendadas [GESTIONES ENCOMENDADAS]) concesión de un préstamo por un importe aproximado de [IMPORTE] Euros.

LA EMPRESA se compromete a elegir entre los productos que existen en el mercado, los que se adapten de mejor forma a las necesidades del CLIENTE, según la información facilitada por el mismo, presentándole al menos tres ofertas vinculantes de las entidades crediticias, y asesorándole sobre las condiciones económicas y jurídicas. En el caso de imposibilidad de obtener tres ofertas vinculantes por no aceptarlas las entidades crediticias, el CLIENTE podrá optar entre desistir del contrato sin coste económico alguno o aceptar alguna de las ofertas que se propongan en los términos indicados en las cláusulas del contrato.

EL CLIENTE abonará a la EMPRESA la cantidad de [IMPORTE] euros más IVA (o un [PORCENTAJE] % sobre el montante total de la operación) en concepto de honorarios como precio total por el servicio prestado, incluyendo cargas y comisiones, minutándose aparte otros impuestos o gastos que no se paguen a través de la EMPRESA o que no los facture ella misma como son los gastos derivados de la operación contratada consistentes en notaría, impuestos, gestorías, etc., así como los demás productos y servicios que puedan ser necesarios para la solicitud y concesión de la operación como por ejemplo seguros correspondientes que solicite la entidad y tasación.

Los honorarios que abone EL CLIENTE se liquidarán en el momento de la firma de la operación, mediante cheque bancario, ingreso en la cuenta que se le indique a tal efecto. Serán abonados anticipadamente los honorarios en los supuestos de encomendar gestiones diferentes a la solicitud de crédito-préstamo como consultoría, asesoramiento, revisiones de escrituras, etc.

El CLIENTE debe abonar los honorarios siempre que la EMPRESA, haya conseguido la aceptación de la entidad bancaria o financiera respecto a la oferta del producto encargado por el cliente, aunque la contratación final no se produzca por causas imputables exclusivamente al CLIENTE.

De acuerdo con la normativa de la Ley 2/2009, de 31 de Marzo, que regula la contratación de créditos-préstamos y los servicios de intermediación de los mismos, el CLIENTE podrá desistir del contrato de intermediación, sin alegación de causa alguna y sin penalización, en los catorce días naturales siguientes a la formalización del contrato. EL CLIENTE deberá desistir mediante escrito dirigido a LA EMPRESA en el domicilio social que figura en el encabezamiento del contrato.

El contrato finalizará cuando, además de las causas legalmente establecidas, concurra alguna de las siguientes: a) Mutuo acuerdo de las partes. b) Resolución por incumplimiento de alguna de las partes de las obligaciones derivadas del Contrato. Si la resolución del contrato se debiere al incumplimiento de EL CLIENTE, la EMPRESA se reserva el derecho a terminar de forma anticipada el presente contrato y, por lo tanto, a ejecutar las acciones legales que le correspondan contra EL CLIENTE sin previo aviso y sin que el cliente tenga derecho a indemnización ni a devolución de cantidad alguna. c) Cese de la prestación del servicio.

En el supuesto que LA EMPRESA no obtenga la operación solicitada en el mercado que se ajuste a las exigencias del CLIENTE, podrá resolver el contrato notificándoselo por escrito en la dirección que figura en el encabezamiento del contrato.

EL CLIENTE autoriza a la EMPRESA a la cesión de sus datos de carácter personal necesarios para analizar su operación a bancos, cajas de ahorro, entidades colaboradoras, organismos públicos y privados necesarios, así como para informarles en un futuro de nuevos productos y servicios financieros que pudieran ser de interés para EL CLIENTE. Dicha comunicación e información podrá ser transmitida incluso por vía electrónica hasta que el CILENTE comunique lo contrario.

En cumplimiento de los dispuesto en la LO 3/2018, de 5 diciembre de Protección Datos Personales y Garantías de los Derechos Digitales y en el Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) por el que se aprueba el Reglamento de desarrollo de la LOPDGDD/1999 y de cualesquiera otras normas vigentes o que en el futuro vengan a sustituir y/o a modificar a éstas, los datos de carácter personal facilitados por EL CLIENTE quedarán registrados en el fichero de la EMPRESA, inscrito en el Registro General de Protección de Datos con el número [NÚMERO] Estos datos solo serán accesibles al personal de esta empresa que deberá conocerlos y serán cedidos única y exclusivamente a las entidades con las que la EMPRESA colabora, a los únicos y exclusivos efectos de analizar y tramitar la operación de financiación objeto de la intermediación financiera contratada.

En cualquier momento, el CLIENTE podrán ejercer su derecho de acceso, rectificación, oposición y cancelación de los datos que ha facilitado a la EMPRESA, mediante comunicación escrita dirigida al domicilio que consta en el encabezamiento.

El CLIENTE manifiesta expresamente que las cláusulas de este contrato se corresponden exactamente con la información previa incluida en el folleto explicativo editado en lengua castellana de fecha [FECHA] suministrada por la EMPRESA y publicado en la página web que figura en el encabezamiento.

El presente contrato se sujeta a las prescripciones de la Ley 2/2009, de 31 de marzo, por la que se regula la contratación con los consumidores de préstamos o créditos hipotecarios y de servicios de intermediación para la celebración de contratos de préstamo o crédito. Los honorarios derivados de los contratos de intermediación en operaciones financieras exentas se encuentran exentos de IVA (ley 37/1992 de la ley del impuesto sobre el valor añadido, de 28 de diciembre de 1992, artículo 20.1, apartado 18º). a dichos honorarios les resulta de aplicación el régimen general del Impuesto de Sociedades, según lo establecido en la Ley 27/2014, de 27 de noviembre, que aprueba la Ley del Impuesto de Sociedades

Para cualquier duda, interpretación o ejecución del contrato de intermediación ambas partes se someten, a efectos de determinar el Tribunal competente, a lo dispuesto en la Ley de Enjuiciamiento Civil.

Y en prueba de conformidad ambas partes firman el presente contrato por duplicado en la ciudad de [LOCALIDAD], a [DÍA] de [MES] de [AÑO], quedando en poder un ejemplar debidamente firmado por cada una de ellas

EL CLIENTE LA EMPRESA

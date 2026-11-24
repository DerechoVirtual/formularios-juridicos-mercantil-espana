---
name: propuesta-acuerdo-reduccion-aumento-simultaneo-capital-mer-0157
description: "Propuesta de acuerdo de reducción y aumento simultáneo de capital de una SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Propuesta de acuerdo de reducción y aumento simultáneo de capital de una SA

> Formulario **MER-0157** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Propuesta de acuerdo de reducción y aumento simultáneo de capital de una SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Propuesta de acuerdo de reducción y aumento simultáneo de capital de una SA” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:propuesta-acuerdo-reduccion-aumento-simultaneo-capital-mer-0157`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] Nº (5 veces)
- [ ] AÑO (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] DÍA
- [ ] FECHA
- [ ] LUGAR
- [ ] MES
- [ ] ÓRGANO O PERSONA

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

La propuesta de acuerdo que debe someterse a la junta general debe incluir:

• La reducción del capital social, especificando la cifra de reducción, la finalidad (normalmente compensar pérdidas), el procedimiento (disminución del valor nominal, amortización de acciones, etc.), el plazo de ejecución y, en su caso, la suma a devolver a los socios.
• El aumento de capital social, indicando la cifra del aumento, la forma de ejecución (nuevas aportaciones dinerarias, compensación de créditos, etc.), el derecho de suscripción o asunción preferente de los socios y el plazo para su ejercicio.
• La simultaneidad y condicionamiento recíproco de ambos acuerdos, de modo que la reducción solo será eficaz si se ejecuta el aumento y viceversa.
• La presentación de un balance auditado que justifique la existencia de pérdidas, aprobado por la junta general y verificado por auditor si la sociedad está obligada a auditar sus cuentas

Primero.— Reducción

Reducción del capital social a cero euros, con la finalidad de restablecer el equilibrio entre aquél y el patrimonio de la sociedad disminuido por consecuencia de pérdidas, mediante la amortización de la totalidad de las acciones representativas de dicho capital.

Segundo.— Aumento

Simultáneo aumento del capital social hasta la cifra de [IMPORTE] euros, mediante la emisión de [Nº] nuevas acciones consistiendo su contravalor en aportaciones dinerarias.

Tercero.— Condiciones

Las condiciones concretas de la reducción y aumento de capital simultáneos serán las siguientes:

1. El capital se reduce en su cifra total, es decir, en [IMPORTE] euros, con la expresada finalidad de restablecer, en combinación con el simultáneo aumento, el equilibrio patrimonial.

2. La reducción se efectúa mediante la amortización de las acciones actuales de la sociedad, es decir, de las acciones números 1 al [Nº] Dichas acciones quedarán amortizadas de pleno derecho y sus títulos representativos quedarán carentes de su valor de tales en el momento en que culmine la ejecución del simultáneo acuerdo de aumento de capital, sin que proceda abonar suma alguna a los accionistas.

3. El aumento de capital se realiza mediante la emisión de [Nº] nuevas acciones ordinarias, numeradas del 1 al [Nº], ambos inclusive, siendo su valor nominal de [IMPORTE] euros y perteneciendo todas ellas a una misma clase y serie.

4. La emisión de las nuevas acciones se hará a la par.

5. El contravalor de las acciones nuevas se hará efectivo mediante aportación dineraria.

6. Las nuevas acciones deberán ser desembolsadas en un 25% en el momento de la suscripción, su importe deberá ser satisfecho en metálico o mediante cheque conformado nominativo a nombre de la sociedad. El 75% restante deberá ser desembolsado en la forma y tiempo que determine el consejo de administración, dentro del plazo máximo de un año desde la adopción del presente acuerdo.

7. Los actuales accionistas son titulares del derecho de suscripción preferente que la Ley les reconoce, y podrán ejercitarlo en el plazo de un mes desde el anuncio de la oferta de suscripción en el Boletín Oficial del Registro Mercantil. Si transcurrido este plazo la ampliación no hubiera quedado suscrita en su totalidad, podrán los accionistas suscribir las acciones no suscritas en el plazo de cinco días. Si transcurrido este último plazo no fueran suscritas todas las acciones emitidas, la ampliación se llevará a efecto únicamente en el importe suscrito. Si este importe fuera inferior a sesenta mil euros, quedarán sin efecto tanto la reducción como la ampliación acordadas.

8. Para el ejercicio del derecho de suscripción preferente se establece, como relación de cambio, la de [IMPORTE] euros en el nuevo capital social por cada [IMPORTE] euros en el antiguo. Para ejercitar el derecho será necesario figurar como titular de las acciones antiguas en el libro registro de acciones nominativas.

Cuarto.— Modificación de estatutos

El artículo [Nº DE ARTÍCULO] de los estatutos sociales quedará redactado en los términos siguientes:

“Artículo [Nº DE ARTÍCULO] "Capital social.—El capital social es de [IMPORTE] euros, representado por [ÓRGANO O PERSONA] acciones nominativas, numeradas correlativamente del 1 al [Nº], ambos inclusive, suscrito en un 25%, debiendo satisfacerse los desembolsos pendientes en la forma y tiempo que determine el consejo de administración, dentro del plazo máximo de un año.

El valor nominal de cada una de las acciones es de [IMPORTE] euros.

Las acciones estarán representadas por títulos numerados correlativamente y extendidos en libros talonarios que podrán incorporar una o más acciones de la misma serie y contendrán, como mínimo, las menciones señaladas en el artículo 114 del Texto Refundido de la Ley de Sociedades de Capital.”

En relación con los acuerdos propuestos, el consejo de administración informa a los señores accionistas lo siguiente:

Las cuentas cerradas a 31 de diciembre de [AÑO] reflejan que la situación patrimonial de la compañía es grave, hasta el punto de ser su neto patrimonial inferior a cero, lo que obliga a adoptar medidas de restablecimiento del equilibrio patrimonial, tanto por consideraciones legales como económicas.

Se impone, por tanto, pedir un esfuerzo a los socios, para que asuman la pérdida patrimonial sufrida e inyecten capital en la Compañía, confiando en que los proyectos empresariales en curso permitan rentabilizar la nueva inversión.

Se considera necesario que la cifra de incremento sea significativa, al objeto de evitar que eventuales pérdidas fuercen a una nueva operación de la índole de la que ahora se propone. euros es una cantidad adecuada. Se intenta dulcificar el esfuerzo que se pide a los accionistas demorando hasta [FECHA] el desembolso del 75%.

En [LUGAR], a [DÍA] de [MES] de [AÑO].

El consejo de administración.

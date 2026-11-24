---
name: publicacion-propuesta-compra-acciones-propias-reducir-mer-0137
description: "Publicación de la propuesta de compra de acciones propias para reducir capital de una SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Publicación de la propuesta de compra de acciones propias para reducir capital de una SA

> Formulario **MER-0137** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Publicación de la propuesta de compra de acciones propias para reducir capital de una SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Publicación de la propuesta de compra de acciones propias para reducir capital de una SA” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:publicacion-propuesta-compra-acciones-propias-reducir-mer-0137`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] MES (6 veces)
- [ ] AÑO (5 veces)
- [ ] DÍA (4 veces)
- [ ] CALLE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº DE ACCIONES (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] FECHA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] NOMBRE Y APELLIDOS
- [ ] OTROS DATOS

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

En las sociedad anónimas, la propuesta de adquisición deberá ser publicada en el Boletín Oficial del Registro Mercantil y en un periódico de gran circulación en la provincia en que la sociedad tenga su domicilio, habrá de mantenerse, al menos, durante un mes, incluirá todas las menciones que sean razonablemente necesarias para la información de los accionistas que deseen enajenar y, en su caso, expresará las consecuencias que se deriven de no alcanzar las acciones ofrecidas el número fijado en el acuerdo

En cumplimiento del acuerdo de la junta general celebrada el día [DÍA] de [MES] de [AÑO] con el carácter de extraordinaria, el consejo de administración de la sociedad, en su reunión de [DÍA] de [MES] de [AÑO], aprobó la propuesta de compra de acciones propias para su posterior amortización de acuerdo con las siguientes condiciones:

— Número de acciones que interesa comprar:

— Precio a satisfacer por acción: [IMPORTE] euros.

— Plazo para la presentación de las ofertas de venta por parte de los accionistas interesados: desde la publicación del anuncio de la presente oferta hasta el [FECHA] de [MES] de

— Lugar de presentación de las ofertas de venta: en el domicilio social sito en [LOCALIDAD], calle [CALLE], número [NÚMERO]

— Información que deberá facilitarse por parte de los accionistas vendedores en el momento de presentar las ofertas de venta:

• Número de acciones que desean vender.

• Número de acciones de que son titulares, aportando documentación justificativa de tal titularidad.

• Datos personales relevantes para la venta.

• Domicilio para posteriores notificaciones.

• La fecha concreta dentro del mes de [MES] de [AÑO] en que deseen formalizar la transmisión de los títulos. En caso de tener dificultades para la determinación de la fecha en el momento mismo de presentación de la oferta, aquélla podrá ser notificada con posterioridad mediante escrito dirigido a la sociedad que deberá recibirse en el domicilio social de ésta con anterioridad al [DÍA] de [MES] de [AÑO], quedando en otro caso sin eficacia la correspondiente oferta de venta.

— Dentro de los quince días siguientes a la finalización del plazo de presentación de ofertas la sociedad remitirá a cada uno de los interesados carta certificada por la que les notificará el número de acciones que, finalmente, desea comprarles la sociedad en atención al número de ofertas de venta recibidas.

— La transmisión de las acciones se efectuará ante el notario de [LOCALIDAD] don [NOMBRE Y APELLIDOS], con domicilio en la calle [CALLE], número [NÚMERO]

— El precio resultante será satisfecho en el momento de formalización de la transmisión mediante cheque nominativo en favor del accionista vendedor.

— Si alguno de los accionistas no compareciera para formalizar la transmisión quedará sin eficacia su oferta de venta. En el supuesto de que se hubiera procedido al prorrateo de las acciones ofrecidas por exceder de [Nº DE ACCIONES], se realizará un nuevo prorrateo sin considerar las ofertas que devengan ineficaces de acuerdo con lo anterior, notificándose el nuevo resultado a los restantes accionistas interesados con el objeto de [OTROS DATOS], si así lo desearan, establecer con ellos las condiciones para la transmisión del correspondiente número adicional de acciones.

— La compra de las acciones se llevará a efecto en todo caso sobre las acciones ofrecidas incluso si el número de éstas no alcanza el número de [Nº DE ACCIONES]

En [LUGAR], a [DÍA] de [MES] de [AÑO].

El consejo de administración.

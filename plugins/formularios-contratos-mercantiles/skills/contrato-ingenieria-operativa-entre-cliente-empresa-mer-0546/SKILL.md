---
name: contrato-ingenieria-operativa-entre-cliente-empresa-mer-0546
description: "Contrato de ingeniería operativa entre cliente y empresa ejecutante. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de ingeniería operativa entre cliente y empresa ejecutante

> Formulario **MER-0546** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de ingeniería operativa entre cliente y empresa ejecutante» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de ingeniería operativa entre cliente y empresa ejecutante” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-ingenieria-operativa-entre-cliente-empresa-mer-0546`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] PLAZO (7 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] CALLE (2 veces)
- [ ] NIF (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FECHA
- [ ] FOLIO
- [ ] LIBRO
- [ ] MES
- [ ] PORCENTAJE
- [ ] SUPERFICIE
- [ ] TOMO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 158 TRLC

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

En [LOCALIDAD], a [DÍA] de [MES] 20 [AÑO]

Comparecen:

De una parte [NOMBRE Y APELLIDOS], como EMPRESA EJECUTANTE (persona jurídica):

(Persona jurídica: constituída en escritura pública otorgada el día [FECHA] ante Notario de [LOCALIDAD] D./Dª [NOMBRE Y APELLIDOS]. e inscrita en el Registro Mercantil de [LOCALIDAD] Libro [LIBRO] Tomo [TOMO] Folio [FOLIO] domiciliada en [DOMICILIO] calle [CALLE] núm [NÚMERO] y con CIF núm [NIF] representada por [ÓRGANO O PERSONA], mayor de edad, con domicilio en [LOCALIDAD] c/ [CALLE] núm [NÚMERO] con DNI/NIF núm [NIF] cuyas facultades derivan del poder otorgando por el notario D./Dª. [NOMBRE Y APELLIDOS], debidamente inscrito, que es declarado vigente y sin modificación alguna)

De otra parte, como CLIENTE (persona jurídica)

Ambas partes se reconocen con carácter mutuo y tienen capacidad legal suficiente para otorgar el presente contrato mercantil de engineering operativo.

Convienen

1. Disposiciones generales: a) La EMPRESA EJECUTANTE es una sociedad de ingeniería especializada en [ACTIVIDAD] (detallar actividad); b) el CLIENTE quiere poner en marcha el establecimiento industrial que se detalla en los documentos anexos, sobre el terreno de su propiedad sito en [LOCALIDAD] (detallar lugar y provincia), con una superficie de [SUPERFICIE] (detallar metros cuadrados), e inscrito en el Registro de la Propiedad de [LOCALIDAD] (detallar tomo, libro, folio, número de finca e inscripción). La finca descrita está libre en la actualidad de todo tipo de cargas. c) La EMPRESA EJECUTANTE ha presentado el presupuesto correspondiente que se detalla en los documentos anexos y que ha sido aprobado por el CLIENTE.

2. Documentos anexos al contrato. Como partes integrantes del correspondiente contrato se acompañan los siguientes documentos anexos: a) Pliego de características específicas del establecimiento industrial a instalar. b) Pliego de garantía y fijación de los plazos de ejecución de cada una de las diversas fases de la operación. c) Pliego de condiciones generales. d) Presupuesto de ejecución.

3. Objeto del contrato. Puesta a disposición del terreno de construcción. Por el presente contrato, la EMPRESA EJECUTANTE se obliga a la construcción y puesta en marcha del establecimiento mercantil del CLIENTE y a su mantenimiento posterior de acuerdo con las condiciones generales predispuestas en los documentos anexos, obligándose a la realización de todas las actuaciones conducentes para la ejecución de la obra proyectada y a su mantenimiento. El proyecto de obra se presentará al CLIENTE para su aprobación, previa homologación del proyecto por el colegio de ingenieros de [LOCALIDAD] (detallar lugar).

El CLIENTE se compromete a la entrega a la EMPRESA EJECUTANTE del terreno en el que se procederá a levantar la planta industrial descrita en el anexo correspondiente y en las condiciones y con las características en él recogidas. La citada obligación incluye la obtención de todos los permisos administrativos y licencias necesarios para que se pueda realizar la edificación e instalación. La entrega se realizará en el plazo de [PLAZO] (detallar días) a partir de la aprobación del proyecto.

En el caso de el retraso no supere [PLAZO] (detallar días), la EMPRESA EJECUTANTE podrá optar entre prolongar el plazo de ejecución en los mismos día de demora de la entrega, o mantener el plazo de ejecución y obtener una compensación de [IMPORTE] (detallar euros) por día de retraso en la entrega del terreno libre de cargas.

Si el retraso es superior a [PLAZO] (detallar días), la EMPRESA EJECUTANTE podrá, además de las opciones contempladas en el párrafo anterior, proceder a la resolución del contrato solicitando la correspondiente indemnización por daños y perjuicios en función de los días de retraso.

4. Precio. Modificaciones. El precio a percibir por la EMPRESA EJECUTANTE será el establecido en el presupuesto recogido en la documentación anexa y que asciendo a la cantidad de [IMPORTE] (detallar euros).

El precio de la obra se hará efectivo mediante certificaciones mensuales de obra ejecutada. Conformada la certificación, el CLIENTE procederá a su abono a la EMPRESA EJECUTANTE en el plazo máximo de [PLAZO] (detallar días) desde su emisión.

Salvo acuerdo expreso con el CLIENTE, la EMPRESA EJECUTANTE no podrá modificar el presupuesto ni las obras respecto a éste. En este último caso deberán realizarse los ajustes presupuestos que se requieran.

5. Garantías. El CLIENTE retendrá un porcentaje de [PORCENTAJE] (detallar %) en concepto de garantía respecto del importe de todas y cada una de las certificaciones de obra presentadas.

La cantidad retenida será devuelta a la EMPRESA EJECUTANTE una vez finalizado el contrato.

5. Obra: calidad y control por el CLIENTE. Subcontratación. La EMPRESA EJECUTANTE responde de la calidad de la obra en su ejecución, así como de los materiales que se empleen en la misma.

El CLIENTE podrá visitar e inspeccionar la obra sin previo aviso cuantas veces considere oportuno. Esta facultad, sin embargo, no implica la posibilidad de impartir órdenes o directrices a la EMPRESA EJECUTANTE.

La EMPRESA EJECUTANTE puede llevar celebrar subcontrataciones para la ejecución de la obra, bajo su exclusiva responsabilidad y sin que las relaciones celebradas por aquella afecten al CLIENTE en modo alguno.

6. Plazo de ejecución. Retraso y penalización. El plazo de ejecución previsto para la realización de la obra es de [PLAZO] (detallar) meses. Dicho plazo comenzará a partir de la puesta a disposición del terreno en el que se ubicará la planta industrial en las condiciones establecidas. En dicho plazo se incluye la puesta en marcha de la planta industrial en su totalidad.

El plazo de ejecución previsto se interrumpirá en el supuesto de impago de cualquiera de las certificaciones de obra hasta el abono de la misma.

En caso de que la EMPRESA EJECUTANTE incumpliera el plazo de ejecución previsto en el anexo correspondiente, y trascurrido el periodo de gracia de [PLAZO] (detallar plazo) quedará obligada a abonar la cantidad de [IMPORTE] (detallar euros) por cada mes de retraso en la ejecución. De la citada penalización se deducirán las cantidades que la EMPRESA EJECUTANTE tenga pendientes de cobro.

7. Seguro. La EMPRESA EJECUTANTE queda obligada a celebrar un contrato de seguro cuya cobertura se extienda a toda la duración de la obra, y que cubra todos los posibles riesgos de la construcción hasta, al menos, el importe del presupuesto de la misma.

8. Terminación y resolución del contrato. Se consideran causas de resolución de este contrato: a) la terminación normal de la relación, bien por haber llegado el contrato a su vencimiento, por haberse ejecutado completamente su objeto o por acuerdo de las partes; b) por incumplimiento de cualquiera de las cláusulas del contrato sin subsanación por parte del incumplidor en el periodo de [PLAZO] (detallar días) desde que le fuera notificado por escrito dicho incumplimiento.

La declaración de concurso de cualquiera de las partes obliga a solicitar a la parte afectada la resolución del contrato de acuerdo con el artículo 158 TRLConc.

La resolución de este contrato de ingeniería, así como cualquiera de las licencias concedidas en su ejecución, no excluya la posibilidad de su reparación legal o judicial que cualquiera de las partes considere oportuno obtener.

9. Gastos. Todos los gastos, impuestos, contribuciones, tasas arbitrios, presentes o futuros, originados por el presente contrato, serán satisfechos a partes iguales por ambas partes.

10. Arbitraje. Las partes se comprometen a acudir a un arbitraje de Derecho privado, conforme a la legislación vigente, para dirimir todos los posibles conflictos que entre ellas pudiera surgir, en particular, como consecuencia de la interpretación o incumplimiento del presente contrato. Las partes renuncian expresamente al ejercicio de cualesquier acción ante tribunales.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

EMPRESA EJECUTANTE CLIENTE

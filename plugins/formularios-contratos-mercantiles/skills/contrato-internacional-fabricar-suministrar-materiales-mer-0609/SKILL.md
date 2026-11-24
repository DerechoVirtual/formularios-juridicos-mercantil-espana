---
name: contrato-internacional-fabricar-suministrar-materiales-mer-0609
description: "Contrato internacional para fabricar y suministrar materiales y equipos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato internacional para fabricar y suministrar materiales y equipos

> Formulario **MER-0609** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato internacional para fabricar y suministrar materiales y equipos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato internacional para fabricar y suministrar materiales y equipos” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-internacional-fabricar-suministrar-materiales-mer-0609`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] MES (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] LUGAR

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

INTERVIENEN

D [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A] en lo sucesivo "EL CLIENTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS] en fecha [FECHA] con el número de protocolo [Nº DE PROTOCOLO] poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D [NOMBRE Y APELLIDOS] en nombre y representación de [NOMBRE DEL REPRESENTADO/A] en lo sucesivo "EL FABRICANTE", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D [NOMBRE Y APELLIDOS] en fecha [FECHA] con el número de protocolo [Nº DE PROTOCOLO] poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE FABRICACIÓN DE MATERIALES Y EQUIPOS, y a tal efecto, libremente y de común acuerdo,

Ambas partes en el respectivo carácter con el que intervienen, se reconocen mutuamente capacidad legal necesaria para suscribir el presente CONTRATO DE SUMINISTRO Y FABRICACIÓN DE MATERIALES Y EQUIPOS, y a tal efecto y de común acuerdo,

EXPONEN

I.- Que EL CLIENTE encargó a EL FABRICANTE la realización de presupuestos en relación con una serie de trabajos de suministro de materiales y fabricación de equipos para la planta de EL CLIENTE en

II.- Que habiéndose aceptado dichos presupuestos EL CLIENTE encarga a EL FABRICANTE los trabajos que más adelante se harán referencia y que se dividen en dos fases de ejecución.

De conformidad con lo anterior, ambas partes consienten en el otorgamiento del presente CONTRATO DE SUMINISTRO Y FABRICACIÓN DE MATERIALES Y EQUIPOS, de acuerdo con las siguientes

CLÁUSULAS

Objeto

El presente contrato tiene por objeto la adquisición por parte de EL CLIENTE para su planta sita en [LOCALIDAD] y el suministro, construcción y entrega por parte de EL FABRICANTE de las siguientes partidas según sus planos y especificaciones técnicas y con sus correspondientes precios (IVA no incluido, se cargará en factura):

Duración

El plazo máximo de ejecución, entrega y montaje de los anteriores materiales e instalaciones por parte de EL FABRICANTE en la planta de EL CLIENTE en será el día [FECHA] de [MES] de

En el caso que se diese un retraso en el cumplimiento de dicho plazo de entrega imputable a EL FABRICANTE ésta mercantil deberá hacerse cargo del pago de una penalización por el referido retraso a EL CLIENTE en cuantía del [PORCENTAJE] % del importe total de los trabajos por cada día de retraso, con un máximo del [PORCENTAJE] %.

Pago

EL CLIENTE se compromete y obliga al abono del importe total de los trabajos a EL FABRICANTE según los precios anteriormente expuestos en la estipulación primera, debiendo abonar la cantidad de [IMPORTE] € además de otros -€ en concepto de [PORCENTAJE] % de IVA, resultando la cantidad total de -€ ( EUROS).

EL FABRICANTE se compromete y obliga a emitir y entregar a EL CLIENTE la correspondiente factura una vez hayan sido totalmente ejecutados los trabajos descritos

Las condiciones de pago para EL CLIENTE son las siguientes:

- [IMPORTE] € (50% del importe total de los trabajos) a 60 días de la fecha de la factura, mediante la entrega de Pagaré conformado por el banco con fecha de vencimiento a 60 días de la fecha de la factura.

- [IMPORTE] € (50% del importe total de los trabajos) a 90 días de la fecha de la factura, mediante la entrega de Pagaré conformado por el banco con fecha de vencimiento a 90 días de la fecha de la factura.

En todo caso, dichos pagos únicamente podrán ser aplazados por el descubrimiento de algún defecto del material o de alguna de las partidas que hicieran necesaria su reparación o sustitución y en la cuantía específica a esa partida concreta.

Ejecución y supervisión de trabajos

EL FABRICANTE., se hace responsable de la ejecución y supervisión de los trabajos contratados, así como de su transporte e instalación en la planta EL CLIENTE.

Todos los trabajos anteriormente detallados podrán ser inspeccionados por parte de EL CLIENTE durante la ejecución de los mismos en los locales de EL FABRICANTE., previo aviso por parte de EL CLIENTE con una antelación mínima de [Nº] días.

Legislación medioambiental y de seguridad e higiene en el trabajo

EL CLIENTE deberá entregar a EL FABRICANTE los requisitos de seguridad, administrativos y medioambientales que deban cumplirse en todos los trabajos a realizar.

En cumplimiento de la legislación vigente en materia de Prevención de Riesgos Laborales, EL CLIENTE adjuntará a este contrato los riesgos analizados y sus causas, y a su vez EL FABRICANTE adjuntará igualmente su protocolo específico de actuación en el que se incluirán las medidas de prevención de la operativa de trabajo teniendo en cuenta los riesgos expuestos por parte de EL CLIENTE Toda esta información deberá ser leída por la totalidad del personal que EL FABRICANTE envíe a las instalaciones de EL CLIENTE a realizar los trabajos contratados.

La totalidad de las partes, así como el conjunto de la instalación, deberán cumplir las normas de seguridad e higiene de la legislación comunitaria.

Documentación

EL FABRICANTE se compromete y obliga a la entrega a EL CLIENTE de toda la documentación acreditativa de que todo el personal afectado por el presente contrato está dado de alta y al corriente de los pagos a la Seguridad Social. En consecuencia, EL CLIENTE queda totalmente exenta de cualquier responsabilidad en virtud del incumplimiento por parte de EL FABRICANTE de sus obligaciones con el personal contratado por esta para la ejecución de los trabajos convenidos.

EL FABRICANTE se hace responsable en cuanto a los operarios contratados para la ejecución de los trabajos pactados, en todo lo referente a las obligaciones salariales, colocación, Seguridad Social, accidentes de trabajo, utilización de herramientas y prendas de seguridad y daños a las instalaciones de EL CLIENTE imputables a dichos trabajadores.

EL CLIENTE impedirá la entrada al trabajo en sus instalaciones, y en su caso expulsará a cualquier miembro del personal de EL FABRICANTE que no esté al corriente en los pagos a la Seguridad Social, o no haya presentado la documentación acreditativa con anterioridad, o no observe las normas legales de seguridad e higiene y las demás previstas en el presente contrato.

EL FABRICANTE se compromete a cumplir las disposiciones señaladas en el Reglamento de Seguridad e Higiene en el trabajo que se encuentre en vigor a la fecha de ejecución de los trabajos.

EL FABRICANTE deberá facilitar por escrito a EL CLIENTE el nombre de la persona responsable a pie de obra durante todo el tiempo que duren los trabajos contratados.

Recepción de los trabajos

EL CLIENTE dará el visto bueno provisional de los trabajos realizados durante los 5 días siguientes a la finalización, entrega e instalación de los mismos, en el supuesto que todo funcione en las condiciones normales de explotación, en función de las especificaciones técnicas de capacidad y rendimiento.

EL CLIENTE dará el visto bueno definitivo después de transcurridos 12 meses a partir del visto bueno provisional, siempre que no exista un deterioro de importancia en los trabajos o instalaciones imputable a defectos de las mismas.

El plazo de garantía de todos los trabajos ejecutados será de 12 meses a partir del visto bueno provisional de EL CLIENTE y cubrirá la totalidad de los costes que se originen como consecuencia de la reparación de las incidencias producidas por defectos de fabricación o ejecución imputables a EL FABRICANTE., tanto en concepto de mano de obra, como de materiales, desplazamientos, etc.

EL FABRICANTE ostentará la propiedad industrial de las partidas objeto del presente contrato, y EL CLIENTE reconocerá a EL FABRICANTE como propietario de dichas instalaciones y trabajos ejecutados hasta la fecha en la que se efectúe el último pago por los trabajos ejecutados y acordados en virtud del presente contrato.

Seguros

EL FABRICANTE deberá tener contratado con carácter previo a la ejecución del presente contrato, con una compañía de seguros las pólizas que fueran necesarias al objeto de cubrir los riesgos de las responsabilidades pecuniarias derivadas del incumplimiento o cumplimiento defectuoso de las obligaciones contraídas en virtud del presente contrato, así como las derivadas de los eventos dañosos que con respecto a sus empleados, así como respecto de los trabajadores, bienes e instalaciones de EL CLIENTE se pudieran producir durante la ejecución de los trabajos objeto del presente contrato, y que fueran imputables a EL FABRICANTE.

Y en prueba de conformidad y aceptación con cuanto antecede expuesto y estipulado, en cuyo contenido se afirman y ratifican, ambas partes suscriben por duplicado y a un solo efecto el presente contrato en el lugar y fecha indicados en su encabezamiento.

[ELEGIR UNA OPCIÓN: Jurisdicción competente y ley aplicable / Sin cláusula penal en caso de no ejecución voluntaria de la sentencia / Con cláusula penal en caso de no ejecución voluntaria de la sentencia]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE FABRICACIÓN DE MATERIALES Y EQUIPOS, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

========================================================================

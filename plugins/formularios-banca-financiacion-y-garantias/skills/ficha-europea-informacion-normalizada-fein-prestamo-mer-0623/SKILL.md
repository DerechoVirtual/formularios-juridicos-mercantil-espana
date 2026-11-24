---
name: ficha-europea-informacion-normalizada-fein-prestamo-mer-0623
description: "Ficha Europea de Información Normalizada (FEIN) de préstamo hipotecario. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Ficha Europea de Información Normalizada (FEIN) de préstamo hipotecario

> Formulario **MER-0623** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Ficha Europea de Información Normalizada (FEIN), creada por la Ley 5/2019, reguladora de los contratos de crédito inmobiliario. Es el documento que el prestamista debe entregar al prestatario con la oferta final, con toda la información personalizada necesaria para que pueda tomar una decisión consciente y fundada sobre las consecuencias de firmar el préstamo.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Ficha Europea de Información Normalizada (FEIN) de préstamo hipotecario» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Ficha Europea de Información Normalizada (FEIN) de préstamo hipotecario” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:ficha-europea-informacion-normalizada-fein-prestamo-mer-0623`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (7 veces)
- [ ] MONEDA NACIONAL DEL PRESTATARIO (7 veces)
- [ ] Nº DE COLUMNA (5 veces)
- [ ] FECHA (4 veces)
- [ ] IMPORTE EN MONEDA NACIONAL DEL PRESTATARIO (4 veces)
- [ ] PERIODICIDAD (4 veces)
- [ ] MONEDA DEL CRÉDITO (3 veces)
- [ ] PERIODO (3 veces)
- [ ] CORREO ELECTRÓNICO (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DURACIÓN DEL PERÍODO DE REFLEXIÓN (2 veces)
- [ ] FAX (2 veces)
- [ ] IMPORTE DEL PRÉSTAMO DE SOLO INTERESES (2 veces)
- [ ] IMPORTE MÁXIMO EN MONEDA NACIONAL DEL PRESTATARIO (2 veces)
- [ ] IMPORTE Y CONCEPTO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL (2 veces)
- [ ] PÁGINA WEB (2 veces)
- [ ] SITUACIÓN DESCRITA EN LA PARTE B DEL ANEXO (2 veces)
- [ ] TELÉFONO (2 veces)
- [ ] CLASE DE INTERÉS APLICABLE
- [ ] CONDICIONES
- [ ] CONDICIONES APLICABLES
- [ ] CONDICIONES DEL REEMBOLSO ANTICIPADO
- [ ] CONSECUENCIAS
- [ ] CONSECUENCIAS FINANCIERAS Y/O JURÍDICAS
- [ ] DURACIÓN
- [ ] DURACIÓN DEL PERÍODO DE DESISTIMIENTO
- [ ] FECHA DE VALIDEZ
- [ ] GARANTÍA
- [ ] GASTOS
- [ ] IMPORTE DE LA CUOTA CORRESPONDIENTE A ESA SITUACIÓN
- [ ] IMPORTE O PORCENTAJE
- [ ] IMPORTE O, SI NO ES POSIBLE, MÉTODO DE CÁLCULO
- [ ] IMPORTE TOTAL A REEMBOLSAR
- [ ] IMPORTE Y MONEDA
- [ ] INDICACIONES
- [ ] INDICACIÓN DE LA LEGISLACIÓN APLICABLE
- [ ] INICIO DEL PERÍODO DE DISPOSICIÓN DEL CRÉDITO
- [ ] LENGUA
- [ ] … y 22 datos más que aparecen una vez en el modelo

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

- Junto a «… que el prestatario quede vinculado por cualquier contrato u oferta de préstamo.»: las instrucciones entre paréntesis («Si ha lugar») indican los párrafos que solo se incluyen cuando proceden. Comprobar el contenido y el formato de la FEIN en el anexo de la Orden ECO/482/2023 (o norma vigente de desarrollo) y en la Ley 5/2019 y su normativa de desarrollo.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

La FEIN se entrega al prestatario sin demora injustificada, una vez que este haya facilitado la información necesaria sobre sus necesidades, situación financiera y preferencias, y con suficiente antelación, que nunca será inferior a diez días naturales respecto del momento en que el prestatario quede vinculado por cualquier contrato u oferta de préstamo.


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

INTRODUCCIÓN

El presente documento se extiende para D./Dña. [NOMBRE Y APELLIDOS DEL PRESTATARIO] (prestatario), a [FECHA].

Se ha elaborado basándose en la información que usted ha facilitado hasta la fecha, así como en las actuales condiciones del mercado financiero.

[OPCIONAL — si ha lugar]
La información que figura a continuación es válida hasta el [FECHA DE VALIDEZ], a excepción del tipo de interés y otros gastos. Después de esa fecha, puede variar con arreglo a las condiciones del mercado.

[OPCIONAL — si ha lugar]
El presente documento no conlleva para [NOMBRE Y APELLIDOS O DENOMINACIÓN DEL PRESTAMISTA] (prestamista) la obligación de concederle un préstamo.

1. PRESTAMISTA

Prestamista: [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL]
Número de teléfono: [TELÉFONO]
Domicilio: [DOMICILIO]
Correo electrónico: [CORREO ELECTRÓNICO]
Número de fax: [FAX]
Dirección de página web: [PÁGINA WEB]
Persona o punto de contacto: D./Dña. [NOMBRE Y APELLIDOS]

[OPCIONAL — si ha lugar: información que indique si se están prestando o no servicios de asesoramiento]
[ELEGIR: Tras analizar sus necesidades y circunstancias, recomendamos que suscriba este crédito / No le recomendamos ningún crédito en concreto. Sin embargo, basándonos en sus respuestas a algunas de las preguntas, le damos información sobre este crédito para que pueda tomar su propia decisión.]

2. INTERMEDIARIO DE CRÉDITO

[OPCIONAL — si ha lugar]
Intermediario de crédito: [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL]
Número de teléfono: [TELÉFONO]
Domicilio: [DOMICILIO]
Correo electrónico: [CORREO ELECTRÓNICO]
Número de fax: [FAX]
Dirección de página web: [PÁGINA WEB]
Persona o punto de contacto: D./Dña. [NOMBRE Y APELLIDOS]

[OPCIONAL — si ha lugar: información que indique si se están prestando o no servicios de asesoramiento]
[ELEGIR: Tras analizar sus necesidades y circunstancias, recomendamos que suscriba este crédito / No le recomendamos ningún crédito en concreto. Sin embargo, basándonos en sus respuestas a algunas de las preguntas, le proporcionamos información sobre este crédito para que pueda tomar su propia decisión.]

Remuneración: [REMUNERACIÓN DEL INTERMEDIARIO]

3. CARACTERÍSTICAS PRINCIPALES DEL PRÉSTAMO

Importe y moneda del préstamo por conceder: [IMPORTE Y MONEDA].

[OPCIONAL — si ha lugar]
El presente préstamo no se expresa en [MONEDA NACIONAL DEL PRESTATARIO].

[OPCIONAL — si ha lugar]
El valor de su préstamo en [MONEDA NACIONAL DEL PRESTATARIO] puede variar.

[OPCIONAL — si ha lugar]
Por ejemplo, si el valor de [MONEDA NACIONAL DEL PRESTATARIO] disminuyera en un 20 % con respecto a [MONEDA DEL CRÉDITO], el valor de su préstamo aumentaría a [IMPORTE EN MONEDA NACIONAL DEL PRESTATARIO]. El incremento podría ser incluso superior si el valor de [MONEDA NACIONAL DEL PRESTATARIO] disminuye en más del 20 %.

[OPCIONAL — si ha lugar]
El valor máximo de su préstamo será [IMPORTE MÁXIMO EN MONEDA NACIONAL DEL PRESTATARIO].

[OPCIONAL — si ha lugar]
Recibirá una advertencia si el importe del crédito alcanza [IMPORTE EN MONEDA NACIONAL DEL PRESTATARIO].

[OPCIONAL — si ha lugar]
Tendrá usted ocasión de ejercer su [ELEGIR: derecho a renegociar el préstamo en moneda extranjera / derecho a convertir el préstamo en [MONEDA CORRESPONDIENTE]], en las siguientes condiciones: [CONDICIONES APLICABLES].

Duración del préstamo: [DURACIÓN].

Tipo de préstamo: [TIPO DE PRÉSTAMO].

Clase de interés aplicable: [CLASE DE INTERÉS APLICABLE].

Importe total a reembolsar: [IMPORTE TOTAL A REEMBOLSAR].

Esto significa que, por cada [UNIDAD MONETARIA DE DENOMINACIÓN DEL PRÉSTAMO] que tome en préstamo, reembolsará usted [IMPORTE].

[OPCIONAL — si ha lugar]
[ELEGIR: Este préstamo / Una parte de este préstamo] es un préstamo de solo intereses. Al finalizar la vigencia del crédito, seguirá adeudando [IMPORTE DEL PRÉSTAMO DE SOLO INTERESES].

[OPCIONAL — si ha lugar]
Valor del bien inmueble que se ha tomado como hipótesis para preparar esta ficha de información: [VALOR DEL INMUEBLE].

[OPCIONAL — si ha lugar]
Importe máximo de préstamo disponible en relación con el valor del bien inmueble: [IMPORTE O PORCENTAJE], o valor mínimo del bien inmueble exigido para prestar el importe indicado: [VALOR MÍNIMO].

[OPCIONAL — si ha lugar]
Garantía: [GARANTÍA].

4. TIPO DE INTERÉS Y OTROS GASTOS

La tasa anual equivalente (TAE) es el coste total del préstamo expresado en forma de porcentaje anual. La TAE sirve para ayudarle a comparar las diferentes ofertas.

La TAE aplicable a su préstamo es [TAE].

Comprende:

El tipo de interés: [TIPO DE INTERÉS].

Otros componentes de la TAE: [OTROS COMPONENTES DE LA TAE].

Costes que deben abonarse una sola vez: [IMPORTE Y CONCEPTO].

[OPCIONAL — si ha lugar]
Tendrá que pagar una tasa por registrar la hipoteca: [IMPORTE].

Costes que deben abonarse periódicamente: [IMPORTE Y CONCEPTO].

[OPCIONAL — si ha lugar]
Esta TAE se calcula a partir de hipótesis sobre el tipo de interés.

[OPCIONAL — si ha lugar]
Dado que [parte de] su préstamo es un préstamo a tipo de interés variable, la TAE efectiva podría diferir de la TAE indicada si el tipo de interés de su préstamo cambia. Por ejemplo, si el tipo de interés aumentase a [SITUACIÓN DESCRITA EN LA PARTE B DEL ANEXO], la TAE podría aumentar a [TAE ILUSTRATIVA CORRESPONDIENTE A ESA SITUACIÓN].

[OPCIONAL — si ha lugar]
Tenga en cuenta que esta TAE se calcula partiendo del supuesto de que el tipo de interés se mantiene durante toda la vigencia del contrato en el nivel fijado para el período inicial.

[OPCIONAL — si ha lugar]
Los siguientes gastos son desconocidos para el prestamista y no se incluyen por tanto en la TAE: [GASTOS].

[OPCIONAL — si ha lugar]
Tendrá que pagar una tasa por registrar la hipoteca.

Asegúrese de que tiene conocimiento de todos los demás tributos y costes conexos al préstamo.

5. PERIODICIDAD Y NÚMERO DE PAGOS

Periodicidad de reembolso: [PERIODICIDAD].

Número de pagos: [NÚMERO DE PAGOS].

6. IMPORTE DE CADA CUOTA

Importe de cada cuota: [IMPORTE EN MONEDA NACIONAL DEL PRESTATARIO].

Sus ingresos pueden variar. Considere si, en caso de que disminuyan sus ingresos, seguirá pudiendo hacer frente al reembolso de sus cuotas [PERIODICIDAD].

[OPCIONAL — si ha lugar]
Dado que [este préstamo / una parte de este préstamo] es un préstamo de solo intereses, tendrá que tomar disposiciones específicas para reembolsar la cantidad de [IMPORTE DEL PRÉSTAMO DE SOLO INTERESES] que adeudará al finalizar la vigencia del crédito. No olvide añadir a la cuota indicada cualesquiera pagos extraordinarios que deba realizar.

[OPCIONAL — si ha lugar]
El tipo de interés de [una parte de] este préstamo es variable. Esto significa que el importe de sus cuotas puede aumentar o disminuir. Por ejemplo, si el tipo de interés aumentase a [SITUACIÓN DESCRITA EN LA PARTE B DEL ANEXO], sus cuotas podrían aumentar a [IMPORTE DE LA CUOTA CORRESPONDIENTE A ESA SITUACIÓN].

[OPCIONAL — si ha lugar]
El valor del importe que tiene que reembolsar en [MONEDA NACIONAL DEL PRESTATARIO] cada [PERIODICIDAD DE LAS CUOTAS] puede variar.

[OPCIONAL — si ha lugar]
Sus pagos podrían incrementarse hasta [IMPORTE MÁXIMO EN MONEDA NACIONAL DEL PRESTATARIO] cada [PERIODO].

[OPCIONAL — si ha lugar]
Por ejemplo, si el valor de [MONEDA NACIONAL DEL PRESTATARIO] disminuyera en un 20 % con respecto a [MONEDA DEL CRÉDITO], tendría usted que pagar [IMPORTE EN MONEDA NACIONAL DEL PRESTATARIO] adicionales cada [PERIODO]. Sus pagos podrían incrementarse en una cantidad muy superior a esta.

[OPCIONAL — si ha lugar]
El tipo de cambio utilizado para la conversión del reembolso en [MONEDA DEL CRÉDITO] a [MONEDA NACIONAL DEL PRESTATARIO] será el publicado por [ORGANISMO ENCARGADO DE LA PUBLICACIÓN DEL TIPO DE CAMBIO] el [FECHA], o se calculará el [FECHA] utilizando [VALOR DE REFERENCIA O MÉTODO DE CÁLCULO].

[OPCIONAL — si ha lugar]
Indicaciones sobre productos de ahorro vinculados y préstamos con intereses diferidos: [INDICACIONES].

7. TABLA ILUSTRATIVA DE REEMBOLSO

[OPCIONAL — si ha lugar]
La siguiente tabla muestra el importe que ha de pagarse cada [PERIODICIDAD].

Las cuotas (columna [Nº DE COLUMNA]) son iguales a la suma de los intereses adeudados (columna [Nº DE COLUMNA]), si ha lugar, el capital adeudado (columna [Nº DE COLUMNA]) y, si ha lugar, otros costes (columna [Nº DE COLUMNA]). [OPCIONAL — si ha lugar: Los costes de la columna «otros costes» corresponden a [LISTA DE COSTES].] El capital pendiente (columna [Nº DE COLUMNA]) es igual al importe del préstamo que queda por reembolsar después de cada cuota.

Tabla de reembolso:
Periodo | Cuota | Intereses | Capital | Otros costes | Capital pendiente
[PERIODO] | [IMPORTE] | [IMPORTE] | [IMPORTE] | [IMPORTE] | [IMPORTE]

8. OTRAS OBLIGACIONES

Si desea beneficiarse de las condiciones de préstamo descritas en el presente documento, el prestatario debe cumplir las obligaciones que a continuación se indican.

Obligaciones: [OBLIGACIONES DEL PRESTATARIO].

[OPCIONAL — si ha lugar]
Observe que las condiciones de préstamo descritas en el presente documento (incluido el tipo de interés) pueden variar en caso de incumplimiento de las citadas obligaciones.

[OPCIONAL — si ha lugar]
Tenga en cuenta las consecuencias que puede tener el poner término más adelante a cualquiera de los servicios accesorios conexos al préstamo: [CONSECUENCIAS].

9. REEMBOLSO ANTICIPADO

Este préstamo puede reembolsarse anticipadamente, íntegra o parcialmente.

[OPCIONAL — si ha lugar]
Condiciones: [CONDICIONES DEL REEMBOLSO ANTICIPADO].

[OPCIONAL — si ha lugar]
Comisión de reembolso anticipado: [IMPORTE O, SI NO ES POSIBLE, MÉTODO DE CÁLCULO].

[OPCIONAL — si ha lugar]
Si decide reembolsar el préstamo anticipadamente, consúltenos a fin de determinar el nivel exacto de la comisión de reembolso anticipado en ese momento.

10. ELEMENTOS DE FLEXIBILIDAD

[OPCIONAL — si ha lugar: información sobre portabilidad o subrogación]
Tiene usted la posibilidad de transferir este préstamo a otro [ELEGIR: prestamista / bien inmueble / prestamista o bien inmueble], en las siguientes condiciones: [CONDICIONES].

[OPCIONAL — si ha lugar]
Este préstamo no puede ser transferido a otro [ELEGIR: prestamista / bien inmueble / prestamista o bien inmueble].

[OPCIONAL — si ha lugar]
Otras prestaciones: [EXPLICACIÓN DE LAS PRESTACIONES ADICIONALES Y, FACULTATIVAMENTE, DE CUALESQUIERA OTRAS PRESTACIONES OFRECIDAS POR EL PRESTAMISTA COMO PARTE DEL CONTRATO DE CRÉDITO QUE NO SE HAYAN MENCIONADO EN LAS SECCIONES ANTERIORES].

11. OTROS DERECHOS DEL PRESTATARIO

[OPCIONAL — si ha lugar]
Dispone usted de un período de reflexión de [DURACIÓN DEL PERÍODO DE REFLEXIÓN] a partir del [FECHA] para reflexionar antes de comprometerse a suscribir este préstamo.

[OPCIONAL — si ha lugar]
No puede usted aceptar el contrato de crédito hasta que haya transcurrido un período de [DURACIÓN DEL PERÍODO DE REFLEXIÓN] a partir del momento en que el prestamista le entregue el contrato.

[OPCIONAL — si ha lugar]
Durante un período de [DURACIÓN DEL PERÍODO DE DESISTIMIENTO] a partir de [INICIO DEL PERÍODO DE DISPOSICIÓN DEL CRÉDITO], el prestatario puede ejercer su derecho a cancelar el contrato de crédito. Condiciones y procedimiento: [PROCEDIMIENTO].

[OPCIONAL — si ha lugar]
Si durante ese período compra o vende usted una propiedad relacionada con el presente contrato de crédito, podría perder su derecho a cancelar el contrato.

[OPCIONAL — si ha lugar]
Si decide usted ejercitar su derecho de desistimiento [del contrato de crédito], no olvide comprobar si quedará o no vinculado por las demás obligaciones que ha contraído en relación con el préstamo [incluidos los servicios accesorios asociados al préstamo, contemplados en la sección 8].

12. RECLAMACIONES

Si tiene una reclamación, diríjase a [DATOS DEL PUNTO DE CONTACTO INTERNO Y FUENTE DE INFORMACIÓN SOBRE EL PROCEDIMIENTO].

[OPCIONAL — si ha lugar]
Plazo máximo para la tramitación de la reclamación: [PERIODO DE TIEMPO].

[OPCIONAL — si ha lugar]
[Si no resolvemos internamente la reclamación a su entera satisfacción,] puede usted dirigirse a: [NOMBRE DEL ORGANISMO EXTERNO QUE SE OCUPE DE LAS RECLAMACIONES Y RECURSOS EXTRAJUDICIALES] [OPCIONAL: o ponerse en contacto con la red FIN-NET para obtener las señas del organismo equivalente en su país].

13. INCUMPLIMIENTO DE LOS COMPROMISOS VINCULADOS AL PRÉSTAMO: CONSECUENCIAS PARA EL PRESTATARIO

Tipos de incumplimiento: [TIPOS DE INCUMPLIMIENTO].

Consecuencias financieras y/o jurídicas: [CONSECUENCIAS FINANCIERAS Y/O JURÍDICAS].

Si tiene dificultades para efectuar sus pagos [PERIODICIDAD], póngase en contacto con nosotros enseguida para estudiar posibles soluciones.

[OPCIONAL — si ha lugar]
En última instancia, puede ser desposeído de su vivienda si no efectúa sus pagos puntualmente.

14. INFORMACIÓN ADICIONAL

[OPCIONAL — si ha lugar]
Legislación aplicable al contrato de crédito: [INDICACIÓN DE LA LEGISLACIÓN APLICABLE].

[OPCIONAL — si el prestamista se propone utilizar una lengua distinta de la lengua de la FEIN]
La información y la documentación contractual se facilitarán en [LENGUA]. Con su consentimiento, durante la vigencia del contrato de crédito, nos comunicaremos con usted en [LENGUA O LENGUAS].

[DECLARACIÓN SOBRE EL DERECHO DEL PRESTATARIO A QUE SE LE PROPORCIONE U OFREZCA, SEGÚN EL CASO, UN PROYECTO DEL CONTRATO DE CRÉDITO].

15. SUPERVISOR

El supervisor de este prestamista es [DENOMINACIÓN Y DIRECCIÓN ELECTRÓNICA DE LA AUTORIDAD O AUTORIDADES SUPERVISORAS].

[OPCIONAL — si ha lugar]
El supervisor de este intermediario de crédito es [DENOMINACIÓN Y DIRECCIÓN ELECTRÓNICA DE LA AUTORIDAD O AUTORIDADES SUPERVISORAS].

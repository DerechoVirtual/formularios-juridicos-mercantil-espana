---
name: contrato-prenda-sobre-mercancias-acciones-mer-0636
description: "Contrato de prenda sobre mercancías y acciones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de prenda sobre mercancías y acciones

> Formulario **MER-0636** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de prenda sobre mercancías y acciones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de prenda sobre mercancías y acciones” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contrato-prenda-sobre-mercancias-acciones-mer-0636`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] IMPORTE (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DNI/NIE (4 veces)
- [ ] FECHA (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] DESCRIBIR
- [ ] DESCRIPCIÓN DEL BIEN
- [ ] LUGAR
- [ ] LUGAR Y FECHA
- [ ] OTROS DATOS
- [ ] PLAZO

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

Derecho real de prenda de bienes muebles (mercancías) y acciones con y sin desplazamiento, por el que el deudor pignorante garantiza el cumplimiento de su obligación al acreedor pignoraticio. Se establecen las condiciones y estipulaciones necesarias para el cumplimiento de la operación, así como los derechos y obligaciones de cada una de las partes

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

(Datos del ACREEDOR PIGNORATICIO)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, ACREEDOR PIGNORATICIO.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

(Datos del DEUDOR PIGNORANTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, DEUDOR PIGNORANTE.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

Ambas partes se reconocen mutuamente con capacidad suficiente para otorgar el presente contrato de PRENDA y, a tal fin,

EXPONEN

I. Que el Acreedor pignoraticio tiene concedido al Deudor pignorante un préstamo de [IMPORTE], euros

II. Que el Deudor pignorante es titular, con plena disponibilidad, de las siguientes mercancías [DESCRIPCIÓN DEL BIEN] libres de cargas y gravámenes.

[OPCIONAL — incluir si procede]

(Prenda de acciones)

II. Que el deudor pignorante es titular de las acciones señaladas con los números [Nº] a [Nº] de la Sociedad [DENOMINACIÓN SOCIAL] con un valor nominal de [IMPORTE] que representan el [PORCENTAJE] % de su capital social y que todas ellas están totalmente desembolsadas

Las acciones indicadas le pertenecen por:

[OPCIONAL — incluir si procede]

(Suscripción en la constitución)

Suscripción en el acto de constitución de la sociedad, que tuvo lugar en virtud de escritura pública autorizada por el notario D./Dña. [NOMBRE Y APELLIDOS] de [LOCALIDAD] el con el número de su protocolo.

[OPCIONAL — incluir si procede]

(Suscripción en aumento de capital)

Suscripción en la escritura de aumento de capital autorizada el [FECHA] por el notario D./Dña. [NOMBRE Y APELLIDOS] de [LOCALIDAD] número de su protocolo, la cual está debidamente inscrita en el Registro Mercantil.

[OPCIONAL — incluir si procede]

(Otro título): [OTROS DATOS].

III. Que estando interesado en el aplazamiento de la deuda citada, el deudor pignorante ha decidido constituir garantía prendaria sobre [DESCRIBIR] a favor del acreedor pignoraticio en garantía de su cumplimiento con arreglo a las siguientes:

CLÁUSULAS

Primera.- Objeto

El deudor pignorante reconoce deber al acreedor pignoraticio la cantidad de [IMPORTE] euros, y careciendo en este momento de liquidez se compromete a proceder a su pago el [FECHA], incrementada en un [PORCENTAJE]. % sobre su cuantía, en concepto de intereses de demora, es decir, un total de [IMPORTE] euros.

En garantía de la suma citada el deudor pignorante, sin perjuicio de su responsabilidad personal e ilimitada, constituye a favor del acreedor pignoraticio prenda sobre los [ELEGIR: bienes / acciones] detallados en la exposición segunda manifestando que dichos [ELEGIR: bienes / acciones] son de su propiedad en pleno dominio, que se encuentran libres de cargas y gravámenes, que su precio de adquisición ha sido íntegramente satisfecho y que son susceptibles de libre enajenación.

[OPCIONAL — incluir si procede]

(Solo para prenda de acciones)

Las acciones pignoradas se considerarán como un objeto unitario a los efectos de este derecho real de garantía, de manera que sólo podrá solicitarse la cancelación de la garantía en el momento en que la deuda garantizada haya sido completamente satisfecha.

La prenda se extiende a cualesquiera derechos, bienes, acciones o indemnizaciones que correspondan al titular de las acciones pignoradas por razón de ser el propietario de las mismas.

Segunda.- Duración

[OPCIONAL — incluir si procede]

(Indefinida)

La presente garantía tendrá una duración indefinida, vinculada a la vigencia de las obligaciones cuyo cumplimiento garantiza

[OPCIONAL — incluir si procede]

(Determinada)

La presente garantía tendrá una duración de [PLAZO], con independencia de que se haya cancelado o no la obligación cuyo cumplimiento garantiza.

Tercera.- Depósito [ELEGIR: con / sin] Desplazamiento Posesorio

[OPCIONAL — incluir si procede]

(Con desplazamiento Posesorio)

El acreedor pignoraticio asume a todos los efectos la condición de depositario del bien pignorado y se compromete a cuidarlo con la diligencia de un ordenado empresario y un representante leal.

Los gastos de conservación del bien pignorado son de cuenta del deudor pignorante, sin embargo queda obligado el acreedor pignoraticio a llevar a cabo los actos necesarios e imprescindibles para la conservación del bien pignorado y a abonar los gastos que de los mismos se derive, pudiendo posteriormente reclamar del deudor su importe.

El acreedor pignoraticio podrá ejercitar cuantas acciones competan al deudor del bien pignorado para reclamarlo o defenderla contra terceros.

[OPCIONAL — incluir si procede]

(Almacén o depósito)

De común acuerdo ambas partes manifiestan que las mercaderías descritas quedan depositadas en el almacén de D./Dña. [NOMBRE Y APELLIDOS], sito en [LOCALIDAD]. D./Dña. [NOMBRE Y APELLIDOS] queda como depositario y manifiesta haber recibido la mercancía en correcto estado de conservación, asumiendo todas las obligaciones que se derivan del depósito.

[OPCIONAL — incluir si procede]

(Sin desplazamiento Posesorio)

El deudor pignorante asume a todos los efectos la condición de depositario del bien pignorado y se compromete a cuidarlo con la diligencia de un ordenado empresario.

Sin perjuicio de su derecho a usar el bien sin menoscabo de su valor, el Deudor pignorante tendrá la obligación de conservarlo y tenerlo a disposición del Acreedor pignoraticio, para que éste pueda, en cualquier momento, inspeccionarlo y comprobar la existencia y estado del mismo.

El acreedor pignoraticio podrá ejercitar cuantas acciones competan al deudor del bien pignorado para reclamarlo o defenderla contra terceros.

[OPCIONAL — incluir si procede]

(Prenda de acciones)

El Deudor pignorante indica que los títulos representativos de las acciones pignoradas se encuentran depositados en la entidad [DENOMINACIÓN SOCIAL], y que por el otorgamiento del presente contrato pone las acciones en posesión del Acreedor pignoraticio [NOMBRE Y APELLIDOS], que acepta la entrega, a cuyo favor se entiende efectuado el depósito. En consecuencia, el Deudor pignorante apodera al Acreedor pignoraticio a fin de que por sí pueda obtener el cambio de titularidad del depósito a su favor en la condición de Acreedor pignoraticio

Cuarta.- Prohibición de disponer

[ELEGIR UNA OPCIÓN: Si hay desplazamiento posesorio / Si NO hay desplazamiento posesorio]

[OPCIONAL — incluir si procede]

(Prenda de acciones)

El Deudor pignorante no podrá disponer de las acciones pignoradas en tanto en cuanto se encuentre pendiente el cumplimiento de cualquiera de las obligaciones que se derivan del

[OPCIONAL — incluir si procede]

(Solo para prenda de bienes muebles)

.- Seguros y depreciación

El deudor pignorante se obliga a asegurar el bien objeto de la garantía prendaria de todos los riesgos que normalmente les afecta ante la compañía designando como beneficiario al acreedor pignoraticio y a sus herederos.

Para el caso de depreciación del objeto de la garantía, el acreedor pignoraticio podrá exigir que se añada la cuantía suficiente de garantía para equiparar su valor a la de la deuda. En su caso podrá sustituirse por otra clase de garantía.

[OPCIONAL — incluir si procede]

(Solo para prenda de acciones)

.- Derechos del acreedor pignoraticio

EL acreedor pignoraticio queda facultado para realizar los actos de gestión y percepción de todo lo que corresponda o sustituya a las acciones gravadas, incluida la percepción de dividendos que habrá de imputar al pago de los intereses de la deuda garantizada y, una vez satisfechos éstos, a la amortización del capital.

Corresponde igualmente al acreedor pignoraticio el ejercicio de los derechos propios del accionista en tanto subsista la prenda. En el caso de ampliación de capital de la sociedad emitente de las acciones objeto de la prenda, acreedor pignoraticio está obligado a acudir a la suscripción y realizar el desembolso necesario con el fin de conservar el valor de los bienes que se le han dado en prenda. En orden a satisfacer este desembolso el deudor pignorante habrá de entregar en depósito al acreedor pignoraticio la cantidad necesaria en el término de días del plazo para el ejercicio del derecho de suscripción preferente.

.- Ejecución y liberación de la prenda

[OPCIONAL — incluir si procede]

(Incumplimiento)

Una vez se haya producido el incumplimiento, ya sea este total o parcial, de las obligaciones derivadas del presente contrato las partes acuerdan que el Acreedor pignoraticio podrá proceder a la venta de las [ELEGIR: mercaderías / acciones] pignoradas en la condición o cantidad que estime pertinente. El Acreedor pignoraticio podrá entonces reintegrarse con el producto de la venta, quedando el resto a disposición del deudor pignorante, en el caso de que no resten obligaciones pendientes de cumplimiento, ya que en este último caso las cantidades restantes quedarán siendo objeto de derecho real de prenda hasta la extinción de las obligaciones.

[OPCIONAL — incluir si procede]

(Para el caso de ejecución judicial)

Se fija por las partes como tope para el caso de subasta del bien pignorado la cantidad de [IMPORTE] euros, más otros. euros que se señalan para costas y gastos como cantidad alzada.

[OPCIONAL — incluir si procede]

(Liberación)

El Deudor pignorante podrá en cualquier tiempo liberar la prenda constituida, previo pago de la deuda con autorización del Acreedor pignoraticio.

.- Gastos e impuestos

Todos los gastos, tributos y honorarios que se originen por el otorgamiento del presente contrato así como los que en un futuro puedan derivarse de cualquier reclamación posterior en ejecución del mismo, serán de cuenta y cargo del deudor pignorante.

.- Notificaciones

Las partes convienen los siguientes domicilios para la práctica de las notificaciones necesarias para la ejecución del presente contrato:

El Acreedor-pignoraticio:

El Deudor-pignorante:

.- Naturaleza del contrato

Los comparecientes, en la representación en que intervienen, manifiestan que el presente contrato tiene carácter de mercantil y se regirá en primer término por las estipulaciones contenidas en el mismo y en lo que en ellas no estuviere previsto por las disposiciones del Código de Comercio, leyes especiales, los usos y costumbres mercantiles y, en su defecto, por lo establecido en el Código Civil.

.- Fuero competente

Para la solución de cualquier cuestión litigiosa que, en su caso, pueda derivarse del presente contrato las partes, con renuncia al fuero aplicable, se someten a la jurisdicción de los jueces y tribunales de

Y en prueba de conformidad con todo ello firman el presente documento por duplicado ejemplar y a un solo efecto en el lugar y fecha expresados en el encabezamiento.

DEUDOR PIGNORANTE

ACREEDOR PIGNORATICIO

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

[LUGAR Y FECHA]

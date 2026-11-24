---
name: escritura-publica-donacion-participaciones-sl-mer-0237
description: "Escritura pública de donación de participaciones de una SL a un descendiente. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de donación de participaciones de una SL a un descendiente

> Formulario **MER-0237** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública mediante la cual se procede a la donación de las participaciones sociales, de titularidad de uno de los socios de una Sociedad de Responsabilidad Limitada, al donatario, sin existir derechos de adquisición preferente del resto de los socios.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de donación de participaciones de una SL a un descendiente» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de donación de participaciones de una SL a un descendiente” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-publica-donacion-participaciones-sl-mer-0237`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (8 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] CLASE
- [ ] COLEGIO
- [ ] LUGAR
- [ ] NIF
- [ ] NOMBRE DE LOS FUNDADORES
- [ ] PROVINCIA
- [ ] SERIE
- [ ] TOMO
- [ ] TÍTULO DE ADQUISICIÓN

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

Modelo de escritura pública mediante la cual se procede a la donación de las participaciones sociales, de titularidad de uno de los socios de una Sociedad de Responsabilidad Limitada, al donatario, sin existir derechos de adquisición preferente del resto de los socios.


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

NÚMERO DE PROTOCOLO:

En [LUGAR], a [FECHA].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO].

COMPARECEN

De una parte,

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente viudo / viuda casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domiciliado en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO].

En lo sucesivo EL DONANTE.

De la otra parte,

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente viudo / viuda casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domiciliado en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO].

En lo sucesivo EL ACEPTANTE.

Les identifico por sus respectivos [ELEGIR: DNI / pasaporte / permiso de residencia], antes reseñados, y tienen, a mi juicio, según intervienen, la capacidad legal necesaria para otorgar la presente escritura de DONACIÓN DE PARTICIPACIONES SOCIALES DE ‘ [DENOMINACIÓN SOCIAL], S.L.’, a cuyo fin

MANIFIESTAN

I.- Que EL DONANTE es dueño, en pleno dominio, de [Nº] participaciones números [Nº] al [Nº], ambos inclusive, de la mercantil ‘[DENOMINACIÓN SOCIAL], S.L.’, cuyos datos son los siguientes: su domicilio social se halla sito en [LOCALIDAD], de [PROVINCIA] y fue constituida por [NOMBRE DE LOS FUNDADORES] mediante escritura autorizada por el Notario de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS] el [FECHA], bajo el número [NÚMERO] de los de su protocolo.

La citada sociedad se halla inscrita en el Registro Mercantil de [LOCALIDAD] al Tomo [TOMO], tiene un capital social de [IMPORTE] euros, dividido en [Nº] participaciones de [IMPORTE] euros de valor nominal de cada una de ellas el cual se halla totalmente desembolsado, y le corresponde el CIF número [NIF].

Título.- El DONANTE manifiesta ser socio de ‘[DENOMINACIÓN SOCIAL], S.L.’ como propietario y titular de [Nº] participaciones, que suponen un [Nº] por ciento del capital social, adquiridas por [TÍTULO DE ADQUISICIÓN], según resulta certificado emitido por el órgano de administración de la citada mercantil que el compareciente me exhibe, sin que en lo omitido en nada amplíe, limite, condicione o contradiga lo expuesto.

Cargas.-Manifiesta asimismo el DONANTE que las citadas participaciones se hallan libres de toda carga, gravamen, responsabilidad o afección, manifestándose por la parte transmitente que se hallan totalmente desembolsadas y que no existe ninguna restricción legal ni estatutaria a su transmisión.

Derechos de adquisición preferente y autorización de venta.-El DONANTE manifiesta que no existen restricciones al objeto de la presente donación por efectuarse ésta a favor de descendiente, tal y como consta en el artículo [Nº DE ARTÍCULO] de los Estatutos de ‘[DENOMINACIÓN SOCIAL], S.L.’.

Valor.-Las participaciones objeto de la presente donación están valoradas en [IMPORTE] euros.

II.- Expuesto lo que antecede, los comparecientes

ACUERDAN

Llevar a efecto la presente DONACIÓN DE PARTICIPACIONES SOCIALES, que se regirá por las siguientes

CLÁUSULAS

Primera. Donación

D./Dña. [NOMBRE Y APELLIDOS], el DONANTE, hace donación, en pleno dominio imponiendo al donatario la prohibición de disponer de las mismas; de forma que no podrá ni venderlas ni gravarlas, salvo autorización expresa del donante, a D./Dña. [NOMBRE Y APELLIDOS], el ACEPTANTE, de las participaciones descritas en la Manifestación I de la presente escritura.

Segunda.- Aceptación

El DONATARIO acepta la donación efectuada en los términos expresados.

Tercera. Gastos

Todos los gastos originados por el presente contrato correrán por cuenta del [ELEGIR: donante / donatario].

Cuarta. Exención impositiva

Se solicita por los comparecientes la exención del Impuesto de Sucesiones y Donaciones prevista en [Nº DE ARTÍCULO].

Quinta. Régimen legal

Este contrato reviste carácter mercantil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por la Ley de Sociedades de Capitales en su defecto por el Código de Comercio, usos mercantiles, Leyes especiales y por lo previsto en el Código Civil.

Sexta Protección de datos personales

Advierto expresamente al compareciente que sus datos van a ser incorporados al fichero del Protocolo y documentación notarial y al fichero de Administración y organización, así como del hecho de que, en su caso, tales datos pueden ser cedidos a aquellas Administraciones públicas que según una norma con rango de ley tengan derecho a ello.

ADVERTENCIAS LEGALES, OTORGAMIENTO Y AUTORIZACIÓN NOTARIAL

Hechas las reservas y advertencias legales, en particular y a efectos fiscales, advierto de las obligaciones y responsabilidades tributarias que incumben a las partes en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se pueden derivar de la eventual inexactitud de sus declaraciones.

Leo a los señores comparecientes la presente escritura, previa su renuncia a su derecho de hacerlo por sí, del que les advierto. La consienten y firman conmigo, el Notario, que doy fe de todo lo precedente consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales, de clase [CLASE], serie [SERIE], números [Nº].

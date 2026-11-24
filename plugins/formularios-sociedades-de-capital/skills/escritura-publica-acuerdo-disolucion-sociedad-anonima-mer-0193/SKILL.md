---
name: escritura-publica-acuerdo-disolucion-sociedad-anonima-mer-0193
description: "Escritura pública del acuerdo de disolución de una sociedad anónima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública del acuerdo de disolución de una sociedad anónima

> Formulario **MER-0193** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública mediante la cual se eleva a público el acuerdo de Junta General Extraordinaria o Universal de Accionistas de una Sociedad Anónima sobre disolución de la sociedad.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública del acuerdo de disolución de una sociedad anónima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública del acuerdo de disolución de una sociedad anónima” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-publica-acuerdo-disolucion-sociedad-anonima-mer-0193`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] COLEGIO
- [ ] DOMICILIO
- [ ] FECHA
- [ ] FOLIO
- [ ] INSCRIPCIÓN
- [ ] LUGAR
- [ ] NIF
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] TOMO
- [ ] ÓRGANO DE DESIGNACIÓN

## Normas que cita el formulario

- art. 378 RRM

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

Modelo de escritura pública mediante la cual se eleva a público el acuerdo de Junta General Extraordinaria o Universal de Accionistas de una Sociedad Anónima sobre disolución de la sociedad.


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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS] Notario del Ilustre Colegio de [COLEGIO]

COMPARECE/N

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D/Dña. [NOMBRE Y APELLIDOS]

INTERVIENE/N

En nombre y representación de la mercantil ", S.A. EN LIQUIDACIÓN" con NIF [NIF] domiciliada en [DOMICILIO], constituida por tiempo indefinido mediante escritura pública autorizada por D. Notario de [LOCALIDAD] en fecha [DÍA] de [MES] de [AÑO]. La presente mercantil se halla inscrita en el Registro Mercantil de [LOCALIDAD], al Tomo [TOMO], Folio [FOLIO], Hoja número [NÚMERO], inscripción [INSCRIPCIÓN] Tiene N.I.F. número B

Sus facultades resultan de su cargo de Liquidador de la sociedad, antes Administrador con cargo vigente e inscrito, y cuya firma legitimo.

MANIFIESTA/N

Manifiesta el compareciente que sus facultades para este acto no le han sido revocadas, restringidas ni limitadas y que se hallan en íntegra vigencia. Y yo, el Notario, considero suficientes las referidas facultades para elevar a públicos acuerdos sociales.

Le identifico por su documento de identidad; tiene, a mi juicio, según interviene, capacidad legal y legitimación para otorgar esta escritura de ACUERDO DE DISOLUCIÓN y DICE que, elevando a públicos los acuerdos de la referida Junta General, en representación de [NOMBRE DEL REPRESENTADO/A], S.A.

OTORGA/N

ELEVACIÓN A PÚBLICO DE LOS ACUERDOS SOCIALES

Los comparecientes, según interviene, eleva a público los acuerdos adoptados por la Junta General [ELEGIR: ordinaria / extraordinaria / universal], de la mercantil [DENOMINACIÓN SOCIAL],S.A. celebrada el pasado día [DÍA] de [MES] de [AÑO], tal y como constan en la certificación literal de la que me hace entrega, y a cuya solicitud procedo a unir a la presente, dándose así por reproducidos.

ACUERDO DE DISOLUCIÓN

Queda disuelta la Sociedad [DENOMINACIÓN SOCIAL] añadiendo a su denominación "en disolución".

Causa de la disolución

Que la causa de la disolución ha sido la voluntad unánime de los socios.

Cese de los Administradores

Que se ha declarado el cese de los Administradores de la Compañía, aprobando su gestión, aclarándose que el único Administrador es el señor compareciente, y que fue designado por [ÓRGANO DE DESIGNACIÓN] en la escritura de fecha [FECHA]; por tanto se da por notificado de su cese, el cual aprueba.

Designación de liquidador

Que ha sido designado Liquidador el propio señor compareciente, que aceptó el cargo y manifestó no estar incurso en incompatibilidad legal alguna.

Normas para la liquidación y división del haber social

Publicación del acuerdo

El compareciente justifica la publicación del cambio de denominación exhibiéndome un ejemplar del Diario de [LOCALIDAD] del día [DÍA] de [MES] de [AÑO] Incorporo a esta matriz fotocopia de la correspondiente página.

El compareciente me muestra original de dicho anuncio, fotocopia del cual, a su petición, procedo a unir a la presente escritura.

ADVERTENCIA REGISTRAL

Informo al compareciente que, para poder inscribir los actos formalizados en la presente escritura, se precisa que la sociedad haya realizado el pertinente depósito de las cuentas anuales en el Registro Mercantil (art. 378 del RRM).

[ELEGIR UNA OPCIÓN: Comunicación al Registro mercantil / Presentación telemática / No telemática / Presentación no telemática]

PROTECCIÓN DE DATOS PERSONALES

Advierto expresamente al compareciente que sus datos van a ser incorporados al fichero del Protocolo y documentación notarial y al fichero de Administración y organización, así como del hecho de que, en su caso, tales datos pueden ser cedidos a aquellas Administraciones públicas que según una norma con rango de ley tengan derecho a ello. Hechas las advertencias de sus derechos al respecto.

OTORGAMIENTO Y AUTORIZACIÓN

Se han hecho las reservas y advertencias legales, en especial advierto de la necesidad de la inscripción en el Registro Mercantil de los actos formalizados en esta escritura y en particular y a efectos fiscales he advertido a los comparecientes de la obligación de presentación de la documentación a liquidar dentro de plazo y de las obligaciones y responsabilidades tributarias que les incumben en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se derivarían de la inexactitud de sus declaraciones.

Les leo, por su elección, esta escritura, advertidos de su derecho a leerla por sí, del que no usan y, tras hacerles las oportunas explicaciones verbales para su cabal conocimiento, manifiestan quedar enterados, la aceptan, se ratifican y firman.

Yo, el Notario, Doy fe de que el consentimiento ha sido libremente prestado y de que el otorgamiento se adecua a la legalidad y a la voluntad debidamente informada de los otorgantes.

Queda extendida en un total de [Nº] folios de papel notarial, el primero con el número [NÚMERO]. y los demás con los números siguientes en orden correlativo.

Y de su contenido, DOY FE.

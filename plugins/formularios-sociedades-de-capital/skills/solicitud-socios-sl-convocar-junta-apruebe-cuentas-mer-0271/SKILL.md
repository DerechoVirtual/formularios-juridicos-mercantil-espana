---
name: solicitud-socios-sl-convocar-junta-apruebe-cuentas-mer-0271
description: "Solicitud de socios de una SL para convocar junta que apruebe las cuentas anuales. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de socios de una SL para convocar junta que apruebe las cuentas anuales

> Formulario **MER-0271** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Receptor HECHOS FUNDAMENTOS DE DERECHO SOLICITO AL LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA DE ESE TRIBUNAL, Firmas Modelo de demanda de jurisdicción voluntaria interpuesta por varios socios por medio de la cual se solicita la celebración de Junta General para proceder a adoptar las cuentas anuales y la gestión social, tras haber transcurrido seis meses sin que se haya procedido por parte de los administradores a convocarla.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de socios de una SL para convocar junta que apruebe las cuentas anuales» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de socios de una SL para convocar junta que apruebe las cuentas anuales” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:solicitud-socios-sl-convocar-junta-apruebe-cuentas-mer-0271`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] SEDE (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] FECHA DE INSCRIPCIÓN
- [ ] FOLIO
- [ ] HOJA
- [ ] IMPORTE
- [ ] LUGAR
- [ ] MES
- [ ] NIF
- [ ] NIF/DNI
- [ ] NOMBRE O DENOMINACIÓN
- [ ] Nº
- [ ] NÚMERO
- [ ] OTROS DATOS
- [ ] PUNTO DEL ORDEN DEL DÍA
- [ ] TOMO

## Normas que cita el formulario

- art. 169.1 TRLSC
- art. 118.1 Ley 15/2015
- art. 87.6.a LOPJ
- art. 117 LJV
- art. 169 TRLSC
- art. 170.3 TRLSC

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

Notas al pie del formulario original:
(1) Téngase en cuenta que a partir del 23-7-2015, fecha de entrada en vigor de la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria, la solicitud de convocatoria de junta puede presentarse ante el Letrado de la Administración de Justicia (antes Secretario) ex arts. 117 a 119 LJV o ante el Registrador Mercantil (arts. 169 a 171 y 377.1 TRLSC). En el presente formulario planteamos el supuesto de presentación ante el Letrado de la Administración de Justicia, siendo competente la Sección de lo Mercantil del TI del domicilio de la sociedad y precisándose la intervención de Abogado y Procurador. Hasta esa fecha el órgano competente era el Juez Mercantil.

Este escrito solicitando la convocatoria de la junta debe hacer constar la concurrencia de los requisitos exigidos legalmente en el art. 169.1 TRLSC al que hace referencia, es decir: a) como se trata de junta ordinaria, la solicitud debe fundamentarse en que no se ha reunido dentro de los plazos legalmente establecido; b) si la junta solicitada fuera estatutaria, se expresarán los motivos de la solicitud y el orden del día que se solicita. En todo caso deben acompañarse los estatutos, los documentos que justifiquen la legitimación y el cumplimiento de dichos requisitos.

También se puede solicitar en el escrito que se designe un presidente y secretario para la junta distintos de los que corresponda estatutariamente.

(2) Téngase en cuenta que desde la entrada en vigor de la reforma orgánica de la LO 1/2025 la competencia objetiva y funcional para conocer todas aquellas cuestiones que se promuevan al amparo de la normativa reguladora de las sociedades mercantiles corresponde a las secciones de lo mercantil de los tribunales de instancia.


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

A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D/Dña. [NOMBRE Y APELLIDOS] Procurador de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS], (etc.) según acredito mediante certificación del Registro Electrónico de Apoderamientos Judiciales que acompaño como documento nº [Nº DE DOCUMENTO], dirigido por el Letrado abajo firmante D./Dña. [NOMBRE Y APELLIDOS], con despacho profesional en [LOCALIDAD], ante el Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito solicito inicio de expediente de JURISDICCIÓN VOLUNTARIA por el que intereso la CONVOCATORIA JUDICIAL DE JUNTA GENERAL de ‘[NOMBRE O DENOMINACIÓN]’, con NIF [NIF] y domicilio en

Fundamento mis pretensiones en los siguientes

HECHOS

Primero.- Mis representados son todos ellos socios de la mercantil ‘.’, constituida el [FECHA] de [MES] de [AÑO], según consta en la escritura autorizada el [FECHA] por D./Dña. [NOMBRE Y APELLIDOS], Notario de [LOCALIDAD], su domicilio social se halla sito en la localidad de [LOCALIDAD] calle [CALLE], y fue inscrita en el Registro Mercantil nº [NÚMERO] de los de [SEDE] el [FECHA DE INSCRIPCIÓN], Tomo [TOMO], Folio [FOLIO], Hoja [HOJA], con CIF [NIF/DNI]

Acredito estos extremos con el documento nº [Nº DE DOCUMENTO] de los que se acompañan a este escrito, y consistente en copia simple de la escritura de constitución mencionada, así como con el documento nº [Nº DE DOCUMENTO], que recoge la certificación del Registro Mercantil donde constan los datos mencionados.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] es titular de [Nº] participaciones de ‘.’ de [IMPORTE] euros de valor nominal, lo que supone un [PORCENTAJE] % del capital social.

De lo anterior se deduce que en conjunto, mis mandantes representan un [PORCENTAJE] % [OTROS DATOS] del capital social total de la mercantil a la que venimos haciendo referencia. En prueba de lo anterior acompaño certificación expedida por el Secretario del Consejo de Administración de ‘.’ del Libro Registro donde constan las mentadas titularidades, como documento

Segundo.- Que ha transcurrido el plazo de 6 meses sin que los administradores hayan procedido a efectuar la convocatoria de la Junta que debía aprobar las cuentas anuales y la gestión social

A los presentes hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- Jurisdicción y competencia

Es competente el Letrado de la Administración de Justicia de la Sección de lo Mercantil del Tribunal de Instancia del domicilio social, según lo previsto en el art. 169.1 TRLSC en relación con el art. 118.1 de la Ley 15/2015, de 2 de julio, de la Jurisdicción Voluntaria (en lo sucesivo, LJV), y el art. 87.6.a) LOPJ.

II PROCEDIMIENTO

El procedimiento ajustado a derecho será el de los arts. 117 a 119 LJV, vigente a estos efectos desde el 23 de julio de 2015.

III Legitimación activa

Corresponde a mis representados según lo previsto en el apartado 1 del art. 169 TRLSC, según el cual cualquier socio puede interesar la convocatoria judicial de Junta General ordinaria o juntas generales previstas en los estatutos y no convocadas en el plazo de los seis primeros meses de cada ejercicio o en el estatutariamente establecido, con audiencia de los administradores, por el Letrado de la Administración de Justicia de la Sección de lo Mercantil del TI del domicilio social, quien además designará libremente a su presidente y secretario.

IV Audiencia de los administradores

Debe efectuarse en virtud de lo previsto en el reiterado art. 169 TRLSC.

V Gastos

Los gastos de la convocatoria serán de cuenta de la sociedad (art. 170.3 TRLSC).

Por todo lo expuesto,

SOLICITO AL LETRADO DE LA ADMINISTRACIÓN DE JUSTICIA DE ESE TRIBUNAL,

que teniendo por presentado este escrito con sus documentos y copias, se sirva admitirlo y acordar de conformidad, teniendo por iniciado expediente de jurisdicción voluntaria y por solicitada convocatoria de Junta General de ‘.’, para que en su día, seguidos sean los trámites legales oportunos, se dicte Decreto por el que se proceda a dicha convocatoria con el siguiente Orden del Día ( [PUNTO DEL ORDEN DEL DÍA]), y ordenando su debida publicidad, Todo ello sin perjuicio de la eventual responsabilidad en la que hayan podido incurrir los administradores,

Por ser de Justicia que pido en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

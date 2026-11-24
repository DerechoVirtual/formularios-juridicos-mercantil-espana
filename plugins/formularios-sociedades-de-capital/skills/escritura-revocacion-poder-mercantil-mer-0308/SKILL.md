---
name: escritura-revocacion-poder-mercantil-mer-0308
description: "Escritura de revocación de poder mercantil. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de revocación de poder mercantil

> Formulario **MER-0308** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Escritura notarial por la que el poderdante revoca un poder anterior, con requerimiento notarial al apoderado para que se dé por notificado y devuelva las copias, y otorga en el mismo acto un nuevo poder para vender y administrar un piso, con facultades de representación procesal.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de revocación de poder mercantil» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de revocación de poder mercantil” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-revocacion-poder-mercantil-mer-0308`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (8 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] MES (4 veces)
- [ ] CALLE (3 veces)
- [ ] DNI/NIE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LETRA (2 veces)
- [ ] NOMBRE DEL NOTARIO (2 veces)
- [ ] Nº (2 veces)
- [ ] PISO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] CARGO
- [ ] COLEGIO NOTARIAL
- [ ] DATOS REGISTRALES
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN DEL PODER
- [ ] DOMICILIO DEL PISO
- [ ] ESTADO CIVIL
- [ ] FECHA
- [ ] NOMBRE Y APELLIDOS DEL APODERADO
- [ ] NOMBRE Y APELLIDOS DEL NUEVO APODERADO
- [ ] NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL PODERDANTE
- [ ] Nº DE FINCA
- [ ] Nº DE FOLIOS
- [ ] Nº DE PROTOCOLO
- [ ] NÚMEROS
- [ ] REGISTRO
- [ ] SERIE

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

- Al principio del formulario: el título original de este formulario («revocación de poder mercantil») no se corresponde con el texto, que revoca un poder anterior y otorga uno nuevo para vender y administrar un piso; se ha reconstruido el texto original.

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

En [LOCALIDAD], mi residencia, a [DÍA] de [MES] de [AÑO].

Ante mí, [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio Notarial de [COLEGIO NOTARIAL], y al efecto de otorgar escritura de poder.

COMPARECE/N:

Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, [ELEGIR: casado/a / soltero/a], vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD], en la calle [CALLE], número [Nº], piso [PISO], letra [LETRA], con DNI/NIE número [DNI/NIE].

[OPCIONAL — incluir si hay más de un compareciente]
Don/Doña [NOMBRE Y APELLIDOS], mayor de edad, [ELEGIR: casado/a / soltero/a], vecino/a de [LOCALIDAD], con domicilio en [LOCALIDAD], en la calle [CALLE], número [Nº], piso [PISO], letra [LETRA], con DNI/NIE número [DNI/NIE].

INTERVIENE/N

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— En nombre propio: [ELEGIR: Interviene en su propio nombre y derecho. / Intervienen ambos en su propio nombre y derecho.]

— En representación: Don/Doña [NOMBRE Y APELLIDOS], en nombre y representación de [DENOMINACIÓN SOCIAL], constituida el [DÍA] de [MES] de [AÑO], ejerce esta representación como [CARGO], estando facultado/a para este otorgamiento por acuerdo de fecha [DÍA] de [MES] de [AÑO], según resulta de la certificación o escritura de poder que se incorpora a esta matriz. Me asegura el/la compareciente la vigencia de esta representación.

TIENE/N, a mi juicio, la capacidad legal necesaria para formalizar esta escritura de REVOCACIÓN DE PODER ANTERIOR Y OTORGAMIENTO DE NUEVO PODER, y a tal efecto,

EXPONEN

ANTECEDENTES

En fecha [DÍA] de [MES] de [AÑO] los comparecientes otorgaron la escritura de poder que a continuación se indica y a favor del apoderado/a que también se menciona:

— Escritura de fecha [FECHA], autorizada por el Notario de [LOCALIDAD], Don/Doña [NOMBRE DEL NOTARIO], con el número [Nº DE PROTOCOLO] de su protocolo, de poder de [DESCRIPCIÓN DEL PODER].

— Apoderado/a: Don/Doña [NOMBRE Y APELLIDOS DEL APODERADO], mayor de edad, de estado civil [ESTADO CIVIL], de profesión [PROFESIÓN], vecino/a de [LOCALIDAD], domiciliado/a en [DOMICILIO].

REVOCACIÓN DEL PODER ANTERIOR

En este acto el/la compareciente REVOCA íntegramente la escritura de poder citada, requiriéndome a mí, el Notario, para que notifique al apoderado la revocación a todos los efectos legales, en el domicilio del mismo antes mencionado, y le requiera a su vez para que me entregue la copia o copias que de dicha escritura de poder disponga el apoderado.

OTORGAMIENTO DE NUEVO PODER

Que por medio del presente instrumento público confiere/n poder, tan amplio como fuere necesario en Derecho, a favor de Don/Doña [NOMBRE Y APELLIDOS DEL NUEVO APODERADO], mayor de edad, de profesión [PROFESIÓN], vecino/a de [LOCALIDAD], domiciliado/a en [DOMICILIO], calle [CALLE], con DNI/NIE número [DNI/NIE], para que, en nombre y representación del/de la compareciente, pueda realizar los actos siguientes con plenitud de competencias, atribuciones y facultades, y con libertad para fijar pactos, cláusulas, disposiciones, determinaciones y declaraciones, de suerte que el/la apoderado/a ostente la plena representación del/de la poderdante sin traba, limitación ni excepción alguna, respecto del piso sito en [DOMICILIO DEL PISO], inscrito en el Registro de la Propiedad de [REGISTRO], finca número [Nº DE FINCA] [DATOS REGISTRALES] (en adelante, «el piso»).

FACULTADES

FACULTADES DE DISPOSICIÓN

Vender a la persona o personas naturales o jurídicas, ya públicas o privadas, que libremente concierte, el piso antes descrito, por el precio y condiciones que estipulen, y cuyo precio podrá o podrán percibir al contado, confesar haberlo percibido con anterioridad, o aplazarlo en todo o en parte, pudiendo incluso garantizar dicho precio aplazado con hipoteca o condición resolutoria o cualquier otra garantía, la que podrán cancelar en su día. Y al efecto otorgar y firmar cuantos documentos públicos o privados fueren precisos.

FACULTADES DE REPRESENTACIÓN PROCESAL

A todos los expresados fines, comparecer ante jueces, tribunales y autoridades competentes, de cualquier clase, grado y jurisdicción, incluso el Tribunal Supremo, en actos, asuntos y juicios civiles, criminales, administrativos, contencioso-administrativos, laborales o de cualquier otra clase, siguiéndolos en todas sus incidencias y recursos, incluso de casación, hasta obtener sentencia o resolución firme y su ejecución. Presentar escritos y ratificarlos. Transigir diferencias. Desistir de los procedimientos iniciados. Ejecutar cuanto fuere necesario o conveniente para la defensa judicial de sus intereses, pudiendo nombrar abogados y procuradores y dar a su favor poderes generales para pleitos.

COPIAS DE PODER

Pedir y retirar copias de este poder.

FACULTADES DE ADMINISTRACIÓN

Administrar en los más amplios términos expresados, pudiendo llevar a cabo, cumplir y ejercitar toda clase de derechos y obligaciones; rendir, exigir y aprobar cuentas; constituir, modificar, resolver o extinguir todo tipo de contratos, muy especialmente de arrendamiento y sin limitación alguna, y contratar contratos de seguro de cualquier clase; promover todo tipo de reclamaciones y procesos o procedimientos, ya extrajudiciales ya judiciales, especialmente de desahucio de arrendatarios, precaristas y cualquier otro tipo de ocupantes; aceptar, pagar y cobrar deudas y créditos por capital, intereses, dividendos y amortizaciones, y con relación a cualquier persona o entidad pública o privada, incluido el Estado, la Comunidad Autónoma, la provincia o el municipio, y que se refieran directa o indirectamente al expresado piso o sus dependencias; firmando recibos, saldos, facturas, conformidades y resguardos; asistir con voz y voto a las juntas de propietarios; aceptar arbitrajes en relación con todo tipo de actos relativos al piso; constituir, reconocer, aceptar, ejecutar, transmitir, dividir, modificar, extinguir y cancelar total o parcialmente usufructos, servidumbres, prendas, hipotecas, anticresis, comunidades de toda clase, propiedades horizontales y, en general, otorgar y firmar cuantos documentos crea necesarios o estime convenientes a los fines de este apoderamiento, pudiendo, en caso de enajenación, transmisión o venta del piso, otorgar escrituras de adición, rectificación, subsanación o aclaración; incluso poderes generales o especiales de representación procesal y a favor de Procuradores y Letrados de su libre elección.

FACULTAD PARA FORMULAR DECLARACIONES

Especialmente se les faculta para que puedan formular declaraciones en nombre de [NOMBRE Y APELLIDOS O DENOMINACIÓN SOCIAL DEL PODERDANTE].

Así lo dice y otorga el/la compareciente (o los comparecientes), quien/es, enterado/s de su derecho a leer por sí este documento, procedo por su elección a la lectura del mismo, en cuyo contenido se ratifica/n y firma/n.

Y yo, el Notario, DOY FE de identificar a los comparecientes por medio de sus documentos nacionales de identidad y de todo lo demás contenido en este instrumento público, extendido en [Nº DE FOLIOS] folios de papel timbrado de uso exclusivamente notarial, de la serie [SERIE], números [NÚMEROS].

Firmas de los comparecientes y firma y signo del Notario.

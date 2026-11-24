---
name: escritura-apoderamiento-mercantil-otorgada-sociedad-mer-0236
description: "Escritura de apoderamiento mercantil otorgada por una sociedad anónima a favor de un tercero. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de apoderamiento mercantil otorgada por una sociedad anónima a favor de un tercero

> Formulario **MER-0236** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de poder notarial otorgado por una Sociedad Anónima a un tercero para que ejercite en nombre y representación de la Sociedad una serie de facultades, como puede ser, entre otros, la representación de la misma ante la Administración Pública, Juzgados y Tribunales, administración de sus bienes o celebración de todo tipo de contratos.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de apoderamiento mercantil otorgada por una sociedad anónima a favor de un tercero» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de apoderamiento mercantil otorgada por una sociedad anónima a favor de un tercero” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-apoderamiento-mercantil-otorgada-sociedad-mer-0236`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] FECHA (6 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] DOMICILIO (2 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] CLASE
- [ ] DATOS REGISTRALES
- [ ] DENOMINACIÓN SOCIAL
- [ ] INSCRIPCIÓN
- [ ] LUGAR
- [ ] NACIONALIDAD
- [ ] NIF
- [ ] PROFESIÓN
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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Modelo de poder notarial otorgado por una Sociedad Anónima a un tercero para que ejercite en nombre y representación de la Sociedad una serie de facultades, como puede ser, entre otros, la representación de la misma ante la Administración Pública, Juzgados y Tribunales, administración de sus bienes o celebración de todo tipo de contratos.


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

Nº DE PROTOCOLO

En [LUGAR], a [FECHA].

Ante mi, D./Dña. [NOMBRE Y APELLIDOS], por oposición Notario de esta villa y de su Ilustre Colegio

COMPARECE

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente viudo / viudo / viuda / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domicilo en [DOMICILIO], [ELEGIR: DNI / Pasaporte / Permiso de Residencia],

Representa a ‘S.A.’ domiciliada en [DOMICILIO], constituida por tiempo indefinido mediante escritura pública autorizada por D./Dña. [NOMBRE Y APELLIDOS] Notario de [LOCALIDAD] en fecha [FECHA], La presente mercantil se halla inscrita en el Registro Mercantil de [LOCALIDAD], al [DATOS REGISTRALES]; su NIF es

Para el presente acto se encuentra facultado en virtud de su cargo de Secretario del Consejo de Administración, que asegura vigente, para el que fue designado por un plazo de [Nº] años por acuerdo de la Junta General de accionistas de la citada mercantil celebrada en fecha [FECHA], cuyos acuerdos fueron elevados a públicos en escritura otorgada ante D./Dña. [NOMBRE Y APELLIDOS] Notario de [LOCALIDAD], el día [FECHA], escritura que cuenta con el número [NÚMERO] de las de su protocolo y se halla inscrita en el Registro Mercantil de [LOCALIDAD], en el Tomo y Folios precedentemente señalados, inscripción [INSCRIPCIÓN] El compareciente se halla especialmente facultado para el presente acto por acuerdo de la Junta General Extraordinaria y Universal de ‘[DENOMINACIÓN SOCIAL], S.A.’, certificación de la cual, con las firmas que la autorizan y que considero legítimas, incorporo a esta escritura, y acompañará a todas sus copias fotocopia auténtica de la misma.

Ejecuta acuerdos de la Junta General Extraordinaria de la Sociedad y del Consejo de Administración de la misma, celebrados en idéntica fecha del día [FECHA], que acredita con certificación incorporada a esta escritura expedida el día [FECHA] del mismo mes, por el mismo, en su calidad de Secretario, y con el Visto Bueno del Presidente D./Dña. [NOMBRE Y APELLIDOS], cuyas firmas están debidamente legitimadas.

Le identifico por su D.N.I. antes reseñado, y tiene, a mi juicio, según interviene, la capacidad legal necesaria para esta escritura de otorgamiento de PODER GENERAL, a cuyo fin

MANIFIESTA

Que confiere poder mercantil a favor de D./Dña. [NOMBRE Y APELLIDOS], mayor de edad con domicilio en [LOCALIDAD], calle [CALLE], nº [NÚMERO] y con DNI/ NIF [NIF] para que ejercite en nombre y representación de la Sociedad poderdante citada las siguientes

FACULTADES

a) Representar a la Sociedad ante toda clase de Juzgados y Tribunales de cualquier grado y jurisdicción, Ministerios y sus Direcciones Generales y Delegaciones Provinciales, Organizaciones Sindicales, Organismos y funcionarios de la Administración Europea, Central, Provincial o Municipal o de las Comunidades Autónomas, y, ante ellos, promover y seguir reclamaciones, expedientes, juicios y causas, por todos sus trámites e incidencias, consintiendo resoluciones, desistiendo de instancias, presentando recursos y apelaciones y pidiendo la ejecución de sentencia y, en general, realizando ante dichos Organismos todas las gestiones que estime convenientes para la Sociedad.

b) Administrar en los más amplios términos toda clase de bienes.

Vender, comprar, dar o recibir en pago o compensación total o parcial, ceder, permutar, extinguir condominios y, por cualquier otro medio oneroso, adquirir y enajenar bienes muebles e inmuebles y derechos de todas clases por los precios, plazos y condiciones que libremente convenga, aceptando y ofreciendo garantías del precio aplazado, incluso hipotecas y condiciones resolutorias expresas, las que podrá cancelar en su día.

Constituir, modificar o extinguir, toda clase de gravámenes o derechos reales o personales, sobre cualesquiera bienes o valores.

c) Celebrar y suscribir toda clase de contratos, rectificarlos, prorrogarlos o renovarlos, rescindirlos o anularlos.

Afianzar y avalar a terceros.

Participar en otras sociedades, suscribiendo o comprando sus acciones o participaciones, aportando bienes muebles o inmuebles y ejercitando cuantos derechos surjan a favor de la Sociedad en su condición de accionistas o socios.

d) Realizar segregaciones, agrupaciones y divisiones, divisiones horizontales, describir los nuevos predios con las características procedentes, realizar declaraciones de obra nueva, redactar, establecer y aceptar Reglamentos y Normas de Comunidad.

e) Concertar toda clase de préstamos, especialmente los de naturaleza hipotecaria, con la garantía de los bienes inmuebles y derechos reales de la Sociedad. Percibir cantidades en efectivo metálico por razón de los préstamos que obtenga. Estipular plazos, intereses, formas de pago y cualesquiera pactos comunes y especiales; pagar sumas por cualquier concepto; contraer las respectivas obligaciones aisladamente o en la forma que permite el artículo 217 del Reglamento Hipotecario; fijar valores, responsabilidades, domicilios y sumisión a determinados Tribunales, aceptar liquidaciones y saldos por cualquier concepto, y ejecutar, en suma, cuanto proceda en relación con los contratos aludidos.

f) Operar con Bancos y Cajas y cualesquiera entidades de depósito, y en ellas abrir, seguir y cancelar cuentas y libretas de ahorro, de crédito, cuentas corrientes y cajas de seguridad, firmando y suscribiendo cheques, recibos y resguardos y cuantos documentos se precisen a los fines indicados; ingresando y retirando cantidades de las mismas, constituyendo depósitos o prendas de valores y retirando todo o parte de ellos, percibir intereses y cantidades en metálicos y, en suma, realizar todo lo permitido por la legislación y práctica bancaria.

g) Librar, girar, aceptar, avalar, negociar, endosar, intervenir, cobrar y protestar toda clase de letras de cambio, pagarés y cheques y demás documentos de giro y crédito bancario.

h) Intervenir en concursos, subastas y licitaciones, haciendo proposiciones y pujar; aceptar adjudicaciones y cederlas, endosarlas y traspasarlas cuando las leyes lo consientan; constituir y cancelar depósitos y fianzas retirando los que hubiera constituido; pedir y consentir liquidaciones parciales y definitivas de obras y servicios y cobrar cantidades a las personas o entidades contratantes.

i) Nombrar y despedir personal técnico y administrativo y laboral, fijando facultades, deberes, sueldos y retribuciones.

Otorgar poderes que comprendan todas o parte de las facultades anteriormente relacionadas a favor de las personas que estime convenientes, incluso Abogados y Procuradores, y revocarlos.

k) Operar con Bancos, Cajas y en ellas abrir, seguir y cancelar cuentas corrientes, firmando y suscribiendo cheques, recibos y resguardos y cuantos documentos se precisen a los fines indicados, ingresando y retirando cantidades de las mismas.

l) Contratar y anular contratos de alquiler para delegaciones y oficinas, así como contratar con todos los organismos, tanto públicos como privados, la instalación de luz, agua, teléfono, etc. en estos locales.

Hechas las reservas y advertencias legales, en particular y a efectos fiscales, advierto de las obligaciones y responsabilidades tributarias que incumben a las partes en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se pueden derivar de la eventual inexactitud de sus declaraciones.

Leo a los señores comparecientes la presente escritura, previa su renuncia a su derecho de hacerlo por sí, del que les advierto. La consienten y firman conmigo, el Notario, que doy fe de todo lo precedente consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales, de clase [CLASE], serie [SERIE], números

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

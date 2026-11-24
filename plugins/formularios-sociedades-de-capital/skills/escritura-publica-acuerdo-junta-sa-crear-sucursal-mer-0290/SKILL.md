---
name: escritura-publica-acuerdo-junta-sa-crear-sucursal-mer-0290
description: "Escritura pública del acuerdo de junta de una SA de crear una sucursal. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública del acuerdo de junta de una SA de crear una sucursal

> Formulario **MER-0290** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública mediante la cual se eleva a público el acuerdo de Junta General Extraordinaria de Accionistas de una Sociedad Anónima sobre creación de una sucursal de la compañía, así como la adopción de los acuerdos que sean precisos.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública del acuerdo de junta de una SA de crear una sucursal» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública del acuerdo de junta de una SA de crear una sucursal” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-publica-acuerdo-junta-sa-crear-sucursal-mer-0290`.
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
- [ ] LOCALIDAD (6 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] CALLE
- [ ] CLASE
- [ ] COLEGIO
- [ ] DATOS REGISTRALES
- [ ] DOCUMENTOS ACREDITATIVOS
- [ ] DOMICILIO
- [ ] INSCRIPCIÓN
- [ ] LUGAR
- [ ] NACIONALIDAD
- [ ] NIF
- [ ] Nº
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

Modelo de escritura pública mediante la cual se eleva a público el acuerdo de Junta General Extraordinaria de Accionistas de una Sociedad Anónima sobre creación de una sucursal de la compañía, así como la adopción de los acuerdos que sean precisos.


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

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO]

COMPARECE/N

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y [ELEGIR: DNI / Pasaporte / Permiso de residencia] número

INTERVIENE/N

En nombre y representación de la mercantil ‘ S.A.’ con NIF [NIF], domiciliada en [DOMICILIO], constituida por tiempo indefinido mediante escritura pública autorizada por D./Dña. [NOMBRE Y APELLIDOS] Notario de [LOCALIDAD] en fecha [FECHA], La presente mercantil se halla inscrita en el Registro Mercantil de [LOCALIDAD], al [DATOS REGISTRALES] y su NIF es

Para el presente acto se encuentra facultado en virtud de su cargo de Secretario del Consejo de Administración, que asegura vigente, para el que fue designado por acuerdo de la Junta General de accionistas de la citada mercantil celebrada en fecha [FECHA], y cuyos acuerdos fueron elevados a públicos en escritura otorgada ante D./Dña. [NOMBRE Y APELLIDOS] Notario de [LOCALIDAD], el día [FECHA], escritura que cuenta con el número [NÚMERO] de las de su protocolo y se halla inscrita en el Registro Mercantil de [LOCALIDAD], en el Tomo y Folios precedentemente señalados, inscripción [INSCRIPCIÓN] El compareciente se halla especialmente facultado para el presente acto por acuerdo de dicha Junta General Extraordinaria de ‘[DENOMINACIÓN SOCIAL], S.A.’, certificación de la cual, con las firmas que la autorizan y que considero legítimas, incorporo a esta escritura, y acompañará a todas sus copias fotocopia auténtica de la misma.

Le identifico por su [ELEGIR: DNI / Pasaporte / Permiso de residencia]. antes reseñado, y tiene, a mi juicio, según interviene, la capacidad legal necesaria para celebrar la presente escritura de ELEVACIÓN A PÚBLICO DE ACUERDOS SOCIALES, a cuyo fin

OTORGA/N

Primero.- Convocatoria

Que la mercantil ‘[DENOMINACIÓN SOCIAL], S.A.’ fue convocada a fin de su reunión en Junta General Extraordinaria en fecha [FECHA] mediante

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Comunicación individual]

El compareciente acredita dichos extremos mediante exhibición de [DOCUMENTOS ACREDITATIVOS].

Segundo.- Elevación a público de los acuerdos sociales

El compareciente, según interviene, eleva a público los acuerdos adoptados por la Junta General Extraordinaria de Accionistas de la mercantil ‘ S.A.’ celebrada el pasado día [FECHA], tal y como constan en la certificación literal de la que me hace entrega, y a cuya solicitud procedo a unir a la presente, dándose así por reproducidos.

Dicha certificación fue expedida por el mismo compareciente, en su calidad de Secretario del Consejo de Administración, con el Visto Bueno de su Presidente, cuyas firmas reconozco y considero legítimas, quedando acreditada la facultad certificante del compareciente.

Tercero.- Creación de la sucursal

A la vista de la potestad reconocida en el art. de los Estatutos Sociales, se acuerda la creación de una sucursal de [DENOMINACIÓN SOCIAL], S.A. de conformidad con lo siguiente:

a) Identificación:

b) Domicilio: Calle [CALLE], nº [NÚMERO] localidad de [LOCALIDAD]

c) Actividades a desarrollar:

d) Representante/s: se designan como representantes permanentes de la sucursal a [NOMBRE Y APELLIDOS], quienes tendrán las siguientes facultades:

(i) Representar a la sucursal ante toda clase de Organismos y funcionarios de la Administración Central, Provincial o Municipal o de las Comunidades Autónomas, Ministerios y sus Direcciones Generales y Delegaciones Provinciales promover y seguir reclamaciones, expedientes, solicitudes, consintiendo resoluciones, desistiendo de instancias, presentando recursos y, en general, realizar ante dichos Organismos todas las gestiones que estime convenientes para el buen funcionamiento de la sucursal.

(ii) Representar a la sucursal ante toda clase de Juzgados y Tribunales de cualquier grado y jurisdicción, y, ante ellos, promover y seguir reclamaciones, expedientes, juicios y causas, por todos sus trámites e incidencias, consintiendo resoluciones, desistiendo de instancias, presentando recursos y apelaciones y pidiendo la ejecución de sentencias, y, en general, realizando ante dichos Organismos todas las gestiones que estime convenientes para la buena marcha de la sucursal, pudiendo absolver posiciones en confesión judicial.

(iii) Administrar toda clase de bienes y derechos de cualquier clase, y disponer de los mismos realizando actos y/o celebrando contratos con libertad para determinar cesiones y/o traspasos de derechos y/o obligaciones fijar precio, rentas, y demás condiciones, esenciales, naturales o accidentales. Celebrar y suscribir toda clase de contratos, de administración, disposición o riguroso dominio, ratificarlos, prorrogarlos o renovarlos, rescindirlos o anularlos.

(iv) Adquirir y/o enajenar bienes muebles e inmuebles y derechos de todas clases por los precios, pactos y condiciones que libremente convenga, aceptando y ofreciendo garantías del precio aplazado, incluso hipotecas y condiciones resolutorias expresas, las que podrá cancelar en su día, con todo tipo de pactos y condiciones.

Constituir, modificar o extinguir, toda clase de gravámenes o derechos reales o personales, sobre cualesquiera bienes o valores.

(v) Constituir, modificar, extinguir, liquidar y ejecutar todo tipo de contratos; usar y disponer de los derechos de tanteo, retracto, adquisición preferente u otros especiales; concurrir a concursos y subastas de obras, servicios y suministros de entidades públicas o privadas y celebrar los contratos correspondientes; contratar suministros, en especial servicios de agua, gas, electricidad, teléfono y otros suministros por tubería o cable; celebrar contratos de trabajo, colectivos y/o individuales; acordar despidos con o sin indemnización; ejercitar y cumplir cuantos derechos y obligaciones deriven de los referidos contratos.

(vi) Participar en otras sociedades de objeto social idéntico o análogo, suscribiendo o comprando sus participaciones o acciones, aportando bienes muebles o inmuebles y/o ejercitando cuantos derechos surjan a favor de la Sociedad en su condición de Socio.

(vii) Concertar toda clase de préstamos o créditos, especialmente los de naturaleza hipotecaria, con la garantía de los bienes inmuebles y derechos reales de la Sociedad. Percibir cantidades en efectivo metálico por razón de los préstamos que obtenga. Convenir plazos, intereses, formas de pago y cualesquiera pactos comunes y especiales; pagar sumas por cualquier concepto;

(viii) Avalar y afianzar a terceros sin limitación.

(ix) Operar con cualesquier entidad de financiación y en ellas, abrir, seguir y cancelar cuentas y libretas de ahorro, de crédito, cuentas corrientes y cajas de seguridad, firmando y suscribiendo cheques, recibos y resguardos, y cuantos documentos se precise, ingresando y retirando cantidades de las mismas, constituyendo depósitos o prendas de valores. Librar, girar, aceptar, avalar, negociar, endosar, intervenir, cobrar y protestar toda clase de letras de cambio, pagarés, cheques y demás documentos de giro y crédito bancario.

(x) Intervenir en concursos, subastas y licitaciones, haciendo proposiciones y pujas, incluso con la Administración Pública; aceptar adjudicaciones y cederlas, endosarlas y traspasarlas cuanto las leyes lo consientan; constituir y cancelar depósitos y fianzas retirando los que hubiera constituido; pedir y consentir liquidaciones parciales y definitivas de obras y servicios, y cobrar cantidades a las personas o entidades contratantes.

(xi) Nombrar y despedir al personal, fijando facultades, deberes, sueldos y retribuciones.

(xii) Otorgar y revocar poderes que comprendan todas o parte de las facultades anteriormente mencionadas a favor de las personas que estime conveniente.

Y en general, ejercitar todo cuanto esté comprendido dentro de las actividades de la sucursal, siendo la precedente relación meramente enunciativa.

Cuarto.-Se solicita por el señor compareciente la inscripción de la presente escritura en el Registro Mercantil, y en particular se solicita del Registrador Mercantil la práctica de cuantos asientos deriven de la presente. Informo al compareciente que, para poder inscribir los actos formalizados en la presente escritura, se precisa que la sociedad haya realizado el pertinente depósito de las cuentas anuales en el Registro Mercantil (art. 282 de la Ley de Sociedades de Capital y 378 del RRM).

Advierto expresamente al compareciente que sus datos van a ser incorporados al fichero del Protocolo y documentación notarial y al fichero de Administración y organización, así como del hecho de que, en su caso, tales datos pueden ser cedidos a aquellas Administraciones públicas que según una norma con rango de ley tengan derecho a ello. Hechas las advertencias de sus derechos al respecto.

A efectos fiscales, advierto de las obligaciones y responsabilidades tributarias que incumben a las partes en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se pueden derivar de la eventual inexactitud de sus declaraciones.

Hechas las reservas y advertencias legales indicadas, leo a los señores comparecientes la presente escritura, previa su renuncia a su derecho de hacerlo por sí, del que les advierto. La consienten y firman conmigo, el Notario, que doy fe de todo lo precedente consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales, de clase [CLASE], serie [SERIE], números

D./Dña. [NOMBRE Y APELLIDOS]

D./Dña. [NOMBRE Y APELLIDOS]

Notario

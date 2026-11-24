---
name: escritura-publica-reduccion-ampliacion-simultanea-mer-0211
description: "Escritura pública de reducción y ampliación simultánea de capital de una SA (operación acordeón). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de reducción y ampliación simultánea de capital de una SA (operación acordeón)

> Formulario **MER-0211** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública mediante la cual se eleva a público el acuerdo de Junta General Extraordinaria de socios de una Sociedad Anónima sobre reducción del capital de la misma para alguna finalidad en concreto, como puede ser por devolución de aportaciones a los socios, o condonación de dividendos pasivos, y el aumento simultáneo de capital (llamada" Operación Acordeón") mediante la emisión de nuevas acciones, así como la adopción de los acuerdos necesarios para la modificación, en su caso, de los estatutos sociales.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de reducción y ampliación simultánea de capital de una SA (operación acordeón)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de reducción y ampliación simultánea de capital de una SA (operación acordeón)” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-publica-reduccion-ampliacion-simultanea-mer-0211`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (10 veces)
- [ ] IMPORTE (9 veces)
- [ ] Nº (8 veces)
- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] NOMBRE Y APELLIDOS (7 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NÚMERO (3 veces)
- [ ] PÁGINA (3 veces)
- [ ] NOMBRE DEL PERIÓDICO (2 veces)
- [ ] CLASE
- [ ] COLEGIO
- [ ] DATOS REGISTRALES
- [ ] DOCUMENTO ACREDITATIVO
- [ ] DOMICILIO
- [ ] INSCRIPCIÓN
- [ ] LUGAR
- [ ] NACIONALIDAD
- [ ] Nº DE ARTÍCULO
- [ ] Nº DE CUENTA (IBAN)
- [ ] PROFESIÓN
- [ ] SERIE
- [ ] ÓRGANO O PERSONA

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

Modelo de escritura pública mediante la cual se eleva a público el acuerdo de Junta General Extraordinaria de socios de una Sociedad Anónima sobre reducción del capital de la misma para alguna finalidad en concreto, como puede ser por devolución de aportaciones a los socios, o condonación de dividendos pasivos, y el aumento simultáneo de capital (llamada" Operación Acordeón") mediante la emisión de nuevas acciones, así como la adopción de los acuerdos necesarios para la modificación, en su caso, de los estatutos sociales.


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

Ante mí, Notario del Ilustre Colegio de [COLEGIO]

COMPARECE/N

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y [ELEGIR: DNI / Pasaporte / Permiso de residencia] número [NÚMERO],

INTERVIENE/N

En nombre y representación de la mercantil ‘[DENOMINACIÓN SOCIAL], S.A.’ domiciliada en [DOMICILIO], constituida por tiempo indefinido mediante escritura pública autorizada por D./Dña. [NOMBRE Y APELLIDOS] Notario de [LOCALIDAD] en fecha [FECHA]. La presente mercantil se halla inscrita en el Registro Mercantil de [LOCALIDAD], al [DATOS REGISTRALES]; su NIF es

Para este acto se encuentra facultado en virtud de su cargo de Secretario del Consejo de Administración, que asegura vigente, para el que fue designado por un plazo de [Nº] años por acuerdo de la Junta General de accionistas de la citada mercantil celebrada en fecha [FECHA], cuyos acuerdos fueron elevados a públicos en escritura otorgada ante D./Dña. [NOMBRE Y APELLIDOS] Notario de [LOCALIDAD], el día [FECHA], escritura que cuenta con el número [NÚMERO] de las de su protocolo y se halla inscrita en el Registro Mercantil de [LOCALIDAD], en el Tomo y Folios precedentemente señalados, inscripción [INSCRIPCIÓN]. El compareciente se halla especialmente facultado para el presente acto por acuerdo de la Junta General Extraordinaria de ‘[DENOMINACIÓN SOCIAL], S.A.’, certificación de la cual, con las firmas que la autorizan y que considero legítimas, incorporo a esta escritura, y acompañará a todas sus copias fotocopia auténtica de la misma.

Le identifico por su [ELEGIR: DNI / Pasaporte / Permiso de residencia]. antes reseñado, y tiene, a mi juicio, según interviene, la capacidad legal necesaria para celebrar la presente escritura de ELEVACIÓN A PÚBLICO DE ACUERDOS SOCIALES, a cuyo fin

OTORGA/N

Primero.- Convocatoria

Que la mercantil ‘[DENOMINACIÓN SOCIAL], S.A.’ fue convocada a fin de su reunión en Junta General Extraordinaria en fecha [FECHA] mediante

[ELEGIR UNA OPCIÓN: Con página web / Sin página web / Comunicación individual]

El compareciente acredita dichos extremos mediante exhibición de [DOCUMENTO ACREDITATIVO].

Igualmente, el compareciente manifiesta que con fecha [FECHA], por el Consejo de Administración de ‘[DENOMINACIÓN SOCIAL], S.A.’ se emitió el preceptivo informe de justificación de la modificación propuesta.

Que en cumplimiento de los acuerdos adoptados en la Junta General de Accionistas de [FECHA], la mercantil ‘[DENOMINACIÓN SOCIAL], S.A.’ eleva a público dichos acuerdos, los cuales constan en el certificado del acta de la misma expedida por D./Dña. [NOMBRE Y APELLIDOS], en su calidad de Secretario del Consejo y de la Junta, con el Visto Bueno del Presidente, y cuyo original se da por reproducido e incorporo a la matriz de la presente escritura.

Segundo.- Reducción del capital social

A) Balance

Me entrega el compareciente el balance aprobado por la Junta de ‘[DENOMINACIÓN SOCIAL], S.A.’ que sirve de base a la presente operación, el cual ha sido verificado por los auditores de cuentas de la sociedad, según acredita con certificado de verificación del mismo, los cuales, a solicitud del compareciente, incorporo a la presente.

B) Cifra de reducción.

Queda reducido el capital en la suma de [IMPORTE] euros.

C) Finalidad de la reducción.

La reducción del capital tiene como finalidad restablecer el equilibrio entre el capital y el patrimonio de la sociedad disminuido por consecuencia de pérdidas.

D) Procedimiento.

La reducción se ha efectuado mediante la disminución del valor nominal de todas las acciones que lo integran en [IMPORTE] euros por acción, que pasan a tener un valor nominal de [IMPORTE] euros cada una de ellas. Así, se amortiza la cantidad de [IMPORTE] euros por acción, circunstancia que se ha hecho constar en los títulos acreditativos de las mismas mediante su estampillado.

La presente operación ha afectado por igual a todos los accionistas.

E) Plazo de ejecución.

La reducción del capital social se efectuó en el acto de la Junta.

F) Publicación del acuerdo.

El compareciente manifiesta que el acuerdo ha sido publicado en la página [PÁGINA] del Boletín Oficial del Registro Mercantil de fecha [FECHA], así como en la página [PÁGINA] del diario [NOMBRE DEL PERIÓDICO] de fecha [FECHA] y en la página [PÁGINA] del diario [NOMBRE DEL PERIÓDICO] de fecha [FECHA]. El compareciente me muestra los originales de dichos anuncios, fotocopia de los cuales, a su petición, procedo a unir a la presente escritura.

G) Derecho de oposición.

Por el compareciente se manifiesta que, tratándose de una reducción del capital social por causa de pérdidas y para restablecer el equilibrio patrimonial de la sociedad, no existe derecho de oposición por parte de los acreedores.

Tercero.- Ampliación simultánea del capital social

Queda aumentado el capital social en la suma de [IMPORTE] euros, declarando el compareciente que:

A) La ampliación se ha efectuado mediante la emisión y puesta en circulación de [Nº] nuevas acciones, de la misma serie de las hasta entonces existentes, representadas por títulos, numerados correlativamente del [Nº] al [Nº], ambos inclusive, por valor nominal de [IMPORTE] euros cada una de ellas.
B) Que las nuevas acciones son íntegramente desembolsadas en metálico en el momento de la suscripción.
C) Que se reconoció a todos los socios el derecho a suscribir un número de las nuevas acciones proporcional al valor nominal de las que poseen, no obstante lo cual y ante la propia Junta se renunció expresamente al ejercicio de tal derecho por parte de todos y cada uno de los asistentes, lo cual la Junta aceptó, no procediéndose, por tanto, al establecimiento de las condiciones de ejercicio del mismo.
D) Que todas las acciones representativas del aumento de capital fueron suscritas y desembolsadas en este mismo acto, en los siguientes términos:.
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] suscribió [Nº] nuevas acciones, nº [NÚMERO] a [Nº], ambos inclusive, por su valor nominal total de [IMPORTE] euros, cuyo desembolso acredita mediante certificado bancario de la entidad [DENOMINACIÓN SOCIAL] donde consta el ingreso de las citadas cantidades en la cuenta [Nº DE CUENTA (IBAN)] de la que es titular la compañía.

Que en consecuencia, las nuevas acciones y las primas de emisión quedan totalmente suscritas y desembolsadas.

Cuarto.- Modificación de los estatutos

Queda modificado el artículo [Nº DE ARTÍCULO] de los Estatutos Sociales que en lo sucesivo tendrá el siguiente contenido:

"Art .- El capital de la sociedad es de [IMPORTE] euros y está representado por [ÓRGANO O PERSONA] acciones nominativas, de valor nominal [IMPORTE] euros cada una de ellas, numeradas correlativamente del 1 al [Nº], ambos inclusive. Todas las acciones son de una sola serie, confieren los mismos derechos y obligaciones y están totalmente desembolsadas en el 100% de su valor nominal’.

Quinto.- Inscripción

Se solicita por el compareciente la inscripción de la presente escritura en el Registro Mercantil, incluso parcial para el caso de que por el Registrador existieren defectos en la misma que impidieren su inscripción total.

Hechas las reservas y advertencias legales, en particular y a efectos fiscales, advierto de las obligaciones y responsabilidades tributarias que incumben a las partes en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se pueden derivar de la eventual inexactitud de sus declaraciones.

Leo a los señores comparecientes la presente escritura, previa renuncia a su derecho de hacerlo por sí, del que les advierto. La consienten y firman conmigo, el Notario, que doy fe de todo lo precedente consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales, de clase [CLASE], serie [SERIE], números

Notario

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

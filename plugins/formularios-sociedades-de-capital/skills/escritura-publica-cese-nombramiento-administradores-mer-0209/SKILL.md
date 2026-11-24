---
name: escritura-publica-cese-nombramiento-administradores-mer-0209
description: "Escritura pública de cese y nombramiento de administradores de una sociedad anónima. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de cese y nombramiento de administradores de una sociedad anónima

> Formulario **MER-0209** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Modelo de escritura pública por la que se eleva a público el acuerdo de la Junta General Extraordinaria de Accionistas de una sociedad anónima sobre el cese del administrador único, administradores solidarios, administradores mancomunados o Consejo de Administración y el nombramiento de los nuevos, para su inscripción en el Registro Mercantil.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de cese y nombramiento de administradores de una sociedad anónima» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de cese y nombramiento de administradores de una sociedad anónima” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-publica-cese-nombramiento-administradores-mer-0209`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (10 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] Nº (6 veces)
- [ ] DENOMINACIÓN SOCIAL (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE DEL NOTARIO (3 veces)
- [ ] PROVINCIA (3 veces)
- [ ] Nº DE PROTOCOLO (2 veces)
- [ ] AÑO
- [ ] CLASE
- [ ] COLEGIO NOTARIAL
- [ ] DATOS REGISTRALES: TOMO, FOLIO, HOJA E INSCRIPCIÓN
- [ ] DIRECCIÓN DE LA PÁGINA WEB
- [ ] DOCUMENTOS EXHIBIDOS
- [ ] DOMICILIO
- [ ] DOMICILIO SOCIAL
- [ ] DÍA
- [ ] MES
- [ ] NACIONALIDAD
- [ ] NIF
- [ ] NOMBRE DEL DIARIO
- [ ] Nº DE ARTÍCULO
- [ ] Nº DE DOCUMENTO
- [ ] Nº DE INSCRIPCIÓN
- [ ] NÚMEROS
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

- Junto a «…reciente acredita dichos extremos mediante exhibición de [DOCUMENTOS EXHIBIDOS].»: comprobar que la forma de convocatoria utilizada es la prevista en los estatutos y en el texto refundido de la Ley de Sociedades de Capital (RDLeg 1/2010), arts. 173 y concordantes, en su redacción vigente.

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

NÚMERO DE PROTOCOLO: [Nº DE PROTOCOLO]

En [LOCALIDAD], a [DÍA] de [MES] de [AÑO]

Ante mí, D./Dña. [NOMBRE DEL NOTARIO], Notario del Ilustre Colegio de [COLEGIO NOTARIAL],

COMPARECE/N

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda / casado / casada], de nacionalidad [NACIONALIDAD], con domicilio en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [Nº DE DOCUMENTO].

[Si comparece más de una persona, repetir el párrafo anterior.]

INTERVIENE/N

En nombre y representación de la mercantil [DENOMINACIÓN SOCIAL], S.A., con NIF [NIF], domiciliada en [DOMICILIO SOCIAL], constituida por tiempo indefinido mediante escritura pública autorizada por el Notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO] en fecha [FECHA]. La presente mercantil se halla inscrita en el Registro Mercantil de [PROVINCIA], al [DATOS REGISTRALES: TOMO, FOLIO, HOJA E INSCRIPCIÓN].

Para el presente acto se encuentra facultado en virtud de su cargo de Secretario de la Junta de accionistas, para el que fue designado por acuerdo de la Junta de la citada mercantil celebrada en fecha [FECHA], y cuyos acuerdos fueron elevados a públicos en escritura otorgada ante el Notario de [LOCALIDAD] D./Dña. [NOMBRE DEL NOTARIO], el día [FECHA], escritura que cuenta con el número [Nº DE PROTOCOLO] de las de su protocolo y se halla inscrita en el Registro Mercantil de [PROVINCIA], en el Tomo y Folios precedentemente señalados, inscripción [Nº DE INSCRIPCIÓN].

Le identifico por su [ELEGIR: DNI / pasaporte / permiso de residencia] antes reseñado, y tiene, a mi juicio, según interviene, la capacidad legal necesaria para celebrar la presente escritura de ELEVACIÓN A PÚBLICO DE ACUERDOS SOCIALES, a cuyo fin

OTORGA/N

PRIMERO.– Convocatoria

Que la mercantil [DENOMINACIÓN SOCIAL], S.A. fue convocada mediante:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Con página web) Anuncio en la página web de la sociedad [DIRECCIÓN DE LA PÁGINA WEB] desde el [FECHA] hasta la fecha de la celebración de la junta el [FECHA], y alerta telemática a los correos electrónicos correspondientes a cada socio de los anuncios de convocatoria insertados en la web.

— (Sin página web) Anuncio publicado en el Boletín Oficial del Registro Mercantil número [Nº] correspondiente al día [FECHA], y en el diario [NOMBRE DEL DIARIO] de [PROVINCIA] del [FECHA].

— (Comunicación individual) El procedimiento de comunicación individual y escrita previsto en el artículo [Nº DE ARTÍCULO] de los Estatutos sociales, habiendo sido remitido el anuncio al último de los socios con fecha de [FECHA].

A fin de su reunión en Junta General Extraordinaria en fecha [FECHA]. El compareciente acredita dichos extremos mediante exhibición de [DOCUMENTOS EXHIBIDOS].

SEGUNDO.– Elevación a público de los acuerdos sociales

El compareciente, según interviene, eleva a público los acuerdos adoptados por la Junta General Extraordinaria de Accionistas de la mercantil [DENOMINACIÓN SOCIAL], S.A. celebrada el pasado día [FECHA], tal y como constan en la certificación literal de la que me hace entrega, y a cuya solicitud procedo a unir a la presente, dándose así por reproducidos.

Dicha certificación fue expedida por el mismo compareciente, en su calidad de Secretario de tal Junta, con el Visto Bueno de su Presidente, cuyas firmas reconozco y considero legítimas, quedando acreditada la facultad certificante del compareciente.

[ELEGIR UNA O VARIAS DE LAS SIGUIENTES ALTERNATIVAS DE LA CLÁUSULA TERCERA, SEGÚN EL ÓRGANO DE ADMINISTRACIÓN, Y SUPRIMIR LAS DEMÁS. RENUMERAR LAS CLÁUSULAS SIGUIENTES SI PROCEDE:]

[OPCIONAL — incluir si procede]
TERCERO.– Cese y nombramiento de administrador único

Que, previo cese del anterior administrador, se nombra como administrador único a D./Dña. [NOMBRE Y APELLIDOS], por el plazo estatutario de [Nº] años, y con los datos personales y circunstancias de aceptación, y declaración de no hallarse incurso en ninguna prohibición, incompatibilidad o incapacidad para el ejercicio del mismo que constan en la mentada certificación.

[OPCIONAL — incluir si procede]
TERCERO.– Cese y nombramiento de administradores mancomunados

Quedan, previo cese por acuerdo de la Junta General de Accionistas de separación de los anteriores administradores mancomunados, nombrados como nuevos administradores mancomunados D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], por el plazo estatutario de [Nº] años, y con los datos personales y circunstancias de aceptación, y declaración de no hallarse incursos en ninguna prohibición, incompatibilidad o incapacidad para el ejercicio del mismo que constan en la mentada certificación.

[OPCIONAL — incluir si procede]
TERCERO.– Cese y nombramiento de administradores solidarios

Quedan, previo cese por dimisión de los anteriores administradores solidarios, nombrados como nuevos administradores solidarios D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], por el plazo estatutario de [Nº] años, y con los datos personales y circunstancias de aceptación, y declaración de no hallarse incursos en ninguna prohibición, incompatibilidad o incapacidad para el ejercicio del mismo que constan en la mentada certificación.

[OPCIONAL — incluir si procede]
TERCERO.– Cese y nombramiento de consejeros

Quedan, previa declaración del cese por caducidad de los anteriores administradores integrantes del Consejo, nombrados como nuevos administradores que pasan a integrar dicho Consejo D./Dña. [NOMBRE Y APELLIDOS], D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], por el plazo estatutario de [Nº] años, y con los datos personales y circunstancias de aceptación, y declaración de no hallarse incursos en ninguna prohibición, incompatibilidad o incapacidad para el ejercicio del mismo que constan en la mentada certificación.

CUARTO.– Inscripción

Se solicita por el señor compareciente la inscripción de la presente escritura en el Registro Mercantil, y en particular se solicita del Registrador Mercantil la práctica de cuantos asientos deriven de la presente.

Hechas las reservas y advertencias legales, en particular y a efectos fiscales, advierto de las obligaciones y responsabilidades tributarias que incumben a las partes en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se pueden derivar de la eventual inexactitud de sus declaraciones.

Leo a los señores comparecientes la presente escritura, previa su renuncia a su derecho de hacerlo por sí, del que les advierto. La consienten y firman conmigo, el Notario, que doy fe de todo lo precedente consignado en este instrumento público, extendido en [Nº] folios de papel timbrado para documentos notariales, de clase [CLASE], serie [SERIE], números [NÚMEROS].

NOTAS DE USO

De conformidad con el artículo 108 del Reglamento del Registro Mercantil (Real Decreto 1784/1996, de 19 de julio), la elevación a instrumento público de los acuerdos sociales corresponde a la persona que tenga facultad para certificarlos. Las decisiones del socio único, consignadas en acta bajo su firma o la de su representante, podrán ser ejecutadas y formalizadas por el propio socio o por los administradores de la sociedad. También podrá realizarse por cualquiera de los miembros del órgano de administración con nombramiento vigente e inscrito en el Registro Mercantil, cuando hubieren sido expresamente facultados para ello en la escritura social o en la reunión en que se hayan adoptado los acuerdos. La elevación a instrumento público por cualquier otra persona requerirá el otorgamiento de la oportuna escritura de poder, que podrá ser general para todo tipo de acuerdos, en cuyo caso deberá inscribirse en el Registro Mercantil. Este procedimiento no será aplicable para elevar a públicos los acuerdos sociales cuando se tome como base para ello el acta o testimonio notarial de la misma.

---
name: anuncio-convocatoria-junta-general-acordar-fusion-mer-0335
description: "Anuncio de convocatoria de junta general para acordar la fusión. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Anuncio de convocatoria de junta general para acordar la fusión

> Formulario **MER-0335** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Anuncio de convocatoria de junta general para acordar la fusión» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Anuncio de convocatoria de junta general para acordar la fusión” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:anuncio-convocatoria-junta-general-acordar-fusion-mer-0335`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE O DENOMINACIÓN (2 veces)
- [ ] CALLE
- [ ] LUGAR
- [ ] LUGAR DE CELEBRACIÓN
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº
- [ ] NÚMERO

## Normas que cita el formulario

- art. 175 LSC

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

La convocatoria de la junta debe realizarse de la forma prevista para cada tipo de sociedad participante en el proceso de fusión. La publicidad habrá de realizarse con un mes de antelación, como mínimo, a la fecha prevista para la celebración de la junta debiendo incluir las menciones mínimas del proyecto de fusión legalmente exigidas, la fecha de inserción en la página web de la sociedad y si ésta no tuviera página web la constancia del derecho que corresponde a todos los socios, obligacionistas y titulares de derechos especiales a examinar en el domicilio social los documentos indicados en este formulario, así como el derecho a obtener la entrega o envío gratuitos del texto íntegro de los mismos


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

CONVOCATORIA DE JUNTA GENERAL DE LA SOCIEDAD

Se convoca a los socios de la sociedad «[DENOMINACIÓN SOCIAL]» a la junta general que tendrá lugar el día [FECHA] a las [Nº] horas y se celebrará en [LUGAR DE CELEBRACIÓN], número [NÚMERO], de la calle [CALLE] de la localidad de [LOCALIDAD], con el siguiente:

ORDEN DEL DÍA

Primero.- Aprobación

Aprobación de la fusión entre las sociedades «[NOMBRE O DENOMINACIÓN]» y «[NOMBRE O DENOMINACIÓN]», mediante absorción de la primera por la segunda, de acuerdo con el proyecto de fusión de fecha [FECHA] aprobado por los órganos de administración de ambas sociedades insertado en sus páginas web y depositado en el Registro Mercantil de [LOCALIDAD] en fecha [FECHA]. De conformidad con lo dispuesto en el artículo 47.2 del RD-ley 5/2023. A continuación se reproducen las menciones mínimas del proyecto de fusión:

• 1. Identificación de las sociedades:

• 2. Tipo y procedimiento de canje de [ELEGIR: participaciones / acciones]:

• 3. Aportaciones de industria o prestaciones accesorias:

• 4. Derechos o títulos especiales:

• 5. Ventajas de expertos y administradores:

• 6. Participación en las ganancias:

• 7. Fecha de efectos contables:

• 8. Modificación de estatutos de la sociedad absorbente [DENOMINACIÓN SOCIAL]:

• 9. Información sobre la valoración de activos y pasivos:

• 10. Fechas de las cuentas en el proyecto:

• 11. Consecuencias de la fusión sobre el empleo, el impacto de género en los órganos de administración y la incidencia en la responsabilidad social de la empresa:

Segundo.- Aprobación del balance de fusión

Tercero.- Adopción y aprobación de las modificaciones estatutarias de la sociedad absorbente

Cuarto.- Nombramiento de administradores de la sociedad resultante del proceso de fusión

Quinto.- Ruegos y preguntas

Sexto.- Lectura y aprobación del acta de la junta

Se deja constancia del derecho de los socios, obligacionistas y titulares de derechos especiales, así como también de los representantes de los trabajadores, de examinar en el domicilio social, o, en su caso, de obtener la entrega o envío gratuitos del texto íntegro de los siguientes documentos:

• A. El proyecto común de fusión.
• B. Los informes de los administradores de cada una de las sociedades sobre el proyecto de fusión.
• C. Los informes de los expertos independientes sobre el proyecto de fusión.
• D. Las cuentas anuales y los informes de gestión de los tres últimos ejercicios, así como los correspondientes informes de los auditores de cuentas de las sociedades.
• E. El balance de fusión de cada una de las sociedades, acompañado del informe del auditor de cuentas de la sociedad.
• F. Los estatutos sociales por los que se rigen las sociedades participantes y los pactos relevantes que vayan a constar en documento público.
• G. El texto íntegro de los estatutos de la sociedad absorbente, incluyendo las modificaciones introducidas.
• H. La identidad de los administradores de las sociedades que participan en la fusión, la fecha desde la que desempeñan sus cargos y la identidad, en su caso, de quienes sean propuestos como nuevos administradores a resultas del proceso de fusión.

En [LUGAR], a [FECHA].

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

Presidente del consejo de administración
administrador único,
administrador solidario
administradores mancomunados
liquidador

La convocatoria de la junta debe realizarse de la forma prevista para cada tipo de sociedad participante en el proceso de fusión. La publicidad habrá de realizarse con un mes de antelación, como mínimo, a la fecha prevista para la celebración de la junta debiendo incluir las menciones mínimas del proyecto de fusión legalmente exigidas, la fecha de inserción en la página web de la sociedad y si ésta no tuviera página web la constancia del derecho que corresponde a todos los socios, obligacionistas y titulares de derechos especiales a examinar en el domicilio social los documentos indicados en el apartado sexto de este formulario, así como el derecho a obtener la entrega o envío gratuitos del texto íntegro de los mismos (art. 47.2 RD-ley 5/2023).

La publicación de la convocatoria debe hacerse al menos con un mes de antelación respecto a la fecha de celebración de la junta (art. 47.2 RD-ley 5/2023).

Se debe detallar la dirección completa: localidad, calle (avenida, plaza, etc.), número y, en su caso, piso y puerta u otros datos que permitan identificar sin dar lugar a dudas la localización de la reunión. En este sentido, no debemos olvidar que, salvo disposición contraria de los estatutos, la junta general de la sociedad limitada se celebrará en el término municipal donde la sociedad tenga su domicilio. (art. 175 LSC).

El proyecto de fusión puede quedar sin efecto si no hubiera sido aprobado por las juntas de socios de todas las sociedades que participen en la fusión dentro de los seis meses siguientes a su fecha (art. 39.3 RD-ley 5/2023).

Este punto del orden del día no es necesario, aunque si conveniente, para atender las cuestiones y quejas que puedan formular los socios

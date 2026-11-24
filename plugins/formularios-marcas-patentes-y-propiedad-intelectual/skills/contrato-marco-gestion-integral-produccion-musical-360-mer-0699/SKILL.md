---
name: contrato-marco-gestion-integral-produccion-musical-360-mer-0699
description: "Contrato marco de gestión integral de la producción musical (360 grados). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato marco de gestión integral de la producción musical (360 grados)

> Formulario **MER-0699** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato marco de gestión integral de la producción musical (360 grados)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato marco de gestión integral de la producción musical (360 grados)” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-marco-gestion-integral-produccion-musical-360-mer-0699`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LUGAR (2 veces)
- [ ] DIRECCIÓN
- [ ] DNI/NIE
- [ ] LOCALIDAD
- [ ] NIF
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº

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

- Junto a «…UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD)»: La LO 15/1999 y su Reglamento (RD 1720/2007) fueron sustituidos por el Reglamento (UE) 2016/679 (RGPD) y la LO 3/2018, de 5 de diciembre (LOPDGDD). Fuente: LO 3/2018, disposición derogatoria única.

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

En [LUGAR], a [FECHA].

REUNIDOS

De una parte, D/Dña. [NOMBRE Y APELLIDOS], mayor de edad, en representación de [NOMBRE DEL REPRESENTADO/A], con CIF [NIF] fecha, y dirección postal [DIRECCIÓN] (productor/promotor)

De otra parte, D/Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI [DNI/NIE], y domicilio en [LOCALIDAD]

ACTUANDO

D/Dña. [NOMBRE Y APELLIDOS], como representante (administrador único/administrador del delgado) de la mercantil prestadora de servicios de promoción y producción musical y de gestión integral de la explotación comercial de obras musicales y fonogramas (a partir de ahora PRODUCTORA/PROMOTORA)

D/Dña. [NOMBRE Y APELLIDOS], en su propio nombre (pero puede actuar en representación de otras personas, en cuyo caso sería “en representación de…” y convendría tener un contrato de mandato o poder notarial) a partir de ahora AUTOR Y/OARTISTA INTÉRPRETE)

Ambas partes se reconocen capacidad jurídica suficiente para contratar y obligarse, y especialmente para formalizar el presente contrato de gestión integral o 360 grados musical

Manifiestan

I.-. Que la sociedad nombre de la mercantil, tiene entre su objeto social y así consta en sus estatutos la prestación de servicios de gestión integral de la música y servicios conexos a dicha prestación (los llamados contratos de 360 grados), que presta, a través de personal cualificado, servicios profesionales orientados a la promoción y producción musical y a la gestión integral de la explotación comercial de obras musicales y fonogramas.

II.- Que el AUTOR/ARTISTA INTÉRPRETE quiere contratar dichos servicios especializados.

III.- Que ambas partes se reconocen capacidad jurídica suficiente para contratar y para obligarse en virtud del presente contrato, resultando de aplicación al mismo, supletoriamente, la normativa nacional, comunitaria e internacional en materia de propiedad intelectual, protección de datos y de sociedad de la información y comercio electrónico.

En consecuencia, deciden, de común acuerdo, formalizar el presente contrato de “gestión integral de la propiedad intelectual de la música 360 grados” con base en las siguientes

CLÁUSULAS

Primera.- Cesión de derechos de imagen y propiedad intelectual.

En virtud del presente contrato el AUTOR/ARTISTA INTÉRPRETE se compromete a componer “x” número de canciones (o discos/LP), originales, cuyos derechos de explotación de dichas obras musicales se ceden en exclusiva en favor del PROMOTOR/PRODUCTOR, que se obliga a realizar de forma integral la explotación comercial y la explotación de los derechos de imagen, marca y merchandising del AUTOR/ARTISTA INTÉRPRETE durante la vigencia del presente contrato.

Segunda.- Derecho y obligaciones del PRODUCTOR/PROMOTOR.

El PROMOTOR/PRODUCTOR gozará de los derechos en exclusiva de propiedad intelectual y de imagen cedidos en virtud del presente contrato en atención a la cláusula anterior y se compromete, en beneficio de ambas partes, a optimizar la explotación de derechos de propiedad intelectual y de imagen en Internet y redes sociales, así como a realizar la gestión integral de la explotación comercial en giras, conciertos y demás interpretaciones que se realicen en los medios de comunicación, especialmente radio y televisión, así como a través de Internet y redes sociales.

En consecuencia, tendrá la exclusiva para gestionar por sí mimo, o a través de empresas de su propio de grupo o de terceros, los siguientes actos de explotaciones y prestaciones<. (enumerar, a continuación, todos los actos que se van a gestionar en este contrato)

Planificar y preparar la estrategia de marketing integral, incluido el marketing digital en Internet y redes sociales de cada concreta obra musical de las que integran el presente contrato.
Producir y explotar comercial los videoclips de cada obra musical.
Explotar comercialmente en Internet y en diferentes cadenas de televisión la difusión de las obras y sus videoclips.
Explotar a través de plataformas especializadas de música en Internet (Spotify, I-tunes…) cada una de las obras musicales.
Planificar e implementar de forma integral el Merchandising del AUTOR/ARTISTA INTÉRPETES.
Promover y contratar conciertos y actuaciones individuales
Planificar las actuaciones del AUTOR/ARTISTA INTÉRPETES en eventos y festivales musicales organizados por terceros.
Diseñar y gestionar la página web del grupo.
Diseñar y gestionar las redes sociales.
Defender los derechos de propiedad intelectual y de imagen derivados del presente contrato….

Tercera.- Derechos y obligaciones del AUTOR/ARTISTA INTÉRPRETE.

El AUTOR/ARTISTA INTÉRPRETE tiene derecho a las remuneraciones y retribuciones que se fijan en la cláusula cuarta del presente contrato y se compromete a componer e interpretar las obras musicales previstas en el desarrollo del presente contrato, conforme a las exigencias de la buena fe, y respondiendo en todo caso de la originalidad y autenticidad de sus creaciones e interpretaciones.

Asimismo, se compromete a preservar su imagen personal conforme a las exigencias del presente contrato.

Cuarta.- Retribución e impago.

(fijar la duración del contrato en la forma que se estime pertinente. Puede ser una retribución fija, una retribución que consista en un porcentaje, P.e. 10 por ciento o una retribución mixta, que contemple una parte fija u otra variable o a porcentaje)

Se fija una retribución mensual de [IMPORTE] euros, que se pagarán por el CLIENTE el día 27 de cada mes.

El impago de dos mensualidades sin justa causa por el CLIENTE conllevará la resolución del contrato y el pago de [IMPORTE] euros en favor de LA MERCANTIL/EL PROFESIONAL PRESTADOR/A DEL SERVICIO en concepto de cláusula penal.

Además, cada disco o fonograma y cada actuación devengarán en favor del AUTOR/ARTISTA INTÉRPRETE un [Nº] por ciento de los ingresos (o de los beneficios) obtenidos.

Y en relación con los derechos de imagen, el 15 por ciento de los beneficios derivados de la explotación de la imagen y del merchandising del AUTOR/ARTISTA INTÉRPRETE.

Quinta.- Duración.

(fijar la duración del contrato en la forma que se estime pertinente, que puede ser temporal o mientras dure la explotación comercial de uno o varios discos o fonogramas)

El presente contrato tendrá la duración de diez años a contar desde la firma del mismo, prorrogable manera indefinida, salvo que, transcurrido el primer año, cualquiera de las partes comunique a la otra, con un preaviso de dos meses, su voluntad de extinguir el presente contrato.

En dicho período, se deberá crear por parte del AUTOR/ARTISTA INTÉRPRETE al menos… (p.e. tres Long Play/Discos de 10 canciones originales).

Sexta.- Responsabilidad.

(delimitar la responsabilidad en la forma que se estime conveniente)

El PRODUCTOR/PROMOTOR asume del deber de realizar la prestación contratada con la diligencia de un buen profesional y asume la responsabilidad de los daños que pueda causar al AUTOR/ARTISTA INTÉRPRETE como consecuencia de actuaciones negligentes directamente relacionadas con la prestación de los servicios contratado.

El AUTOR/ARTISTA INTÉRPRETE responderá de la autoría y originalidad de las cancines que produzca en favor del PRODUCTOR/PROMOTOR durante la vigencia del presente contrato y de la exclusividad en la cesión de los derechos de imagen.

Séptima.- Modificación del contrato.

Las partes podrán modificar de mutuo acuerdo cualquiera de las cláusulas contenidas en el presente contrato.

Octava.- Desistimiento y resolución del contrato.

Cualquier incumplimiento de las obligaciones contenidas en el presente contrato y de los servicios contratados, permitirá a ambas partes extinguir automáticamente el contrato, a través de comunicación fehaciente, en la que se especificará el motivo de la resolución, sin perjuicio de las responsabilidades que pudieran derivarse de dicho incumplimiento de conformidad con la cláusula sexta.

En caso de incumplimiento o una vez extinguido el presente contrato, se dejan de realizar las acciones de promoción y marketing que se derivan del presente contrato.

Novena.- Contratos conexos.

Ambas partes podrán formalizar contratos conexos, derivados del presente contrato marco, para concretos actos de explotación o difusión de las obras musicales o de representaciones, actuaciones o giras específicas, con la propia PROMOTORA/PRODUCTORA o con otras empresas de su grupo o vinculadas a ella.

Décima.- Resolución de controversias.

(fijar mediación, arbitraje o tribunales competente [ELEGIR: mediación / arbitraje / tribunales])

Para resolver cualquier tipo de controversia derivada de la interpretación y aplicación del presente contrato, ambas partes intentarán con carácter preferente y previo una mediación profesional.

En todo caso serán competentes para conocer de las controversias que se derivan del presente contrato las plazas de las Secciones de lo Mercantil del Tribunal de Instancia de XXXXXXX.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Contrato que se firma en [LUGAR], a [FECHA].

FIRMA FIRMA

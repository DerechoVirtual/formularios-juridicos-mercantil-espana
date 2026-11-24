---
name: contrato-servicios-gestion-redes-sociales-social-media-mer-0820
description: "Contrato de servicios de gestión de redes sociales (social media manager). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de servicios de gestión de redes sociales (social media manager)

> Formulario **MER-0820** del plugin **Traspasos de negocio, confidencialidad y acuerdos de empresa** (`formularios-traspasos-y-acuerdos-de-empresa`) · Mercantil › Otros documentos mercantiles · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de servicios de gestión de redes sociales (social media manager)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de servicios de gestión de redes sociales (social media manager)” para mi caso». También puedes invocarla directamente con `/formularios-traspasos-y-acuerdos-de-empresa:contrato-servicios-gestion-redes-sociales-social-media-mer-0820`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-traspasos-y-acuerdos-de-empresa:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Traspasos de negocio, confidencialidad y acuerdos de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] FECHA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LUGAR (2 veces)
- [ ] NIF (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIRECCIÓN
- [ ] LOCALIDAD
- [ ] NOMBRE DEL REPRESENTADO/A

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

De una parte, D/Dña. [NOMBRE Y APELLIDOS], mayor de edad, en representación de (El “social media manager” puede ser persona física, en cuyo caso se identificaría con nombre y DNI. Y además puede ser un contrato de externalización del servicio de “social media manager”, o puede ser un contrato laboral o trabajador por cuenta ajena. En este último caso, sería mejor hablar de “CONTRATANTE” o “COMITENTE” en ven de “CLIENTE), con CIF [NIF], y dirección postal

De otra parte, D/Dña. [NOMBRE Y APELLIDOS], mayor de edad, en representación de [NOMBRE DEL REPRESENTADO/A], con CIF [NIF],y dirección postal [DIRECCIÓN]. (comitente y CLIENTE)

ACTUANDO

D/Dña. [NOMBRE Y APELLIDOS], como representante (Administrador único/administrador del delgado) de la mercantil prestadora de servicios de social media mánager.

D/Dña. [NOMBRE Y APELLIDOS], como representante (O, si es persona física, “en su propio nombre y representación como social media manager”) de la mercantil comitente y destinataria o beneficiaria de los servicios contratados.

Ambas partes se reconocen capacidad jurídica suficiente para contratar y obligarse, y especialmente para formalizar el presente contrato de social media mánager o administrador de redes sociales

MANIFIESTAN

I.-. Que la sociedad [DENOMINACIÓN SOCIAL] (Si es persona física: que D/Dña. [NOMBRE Y APELLIDOS], servicios profesionales orientados a la planificación y gestión de redes sociales. En el contrato nos referiremos a esta parte como “LA MERCANTIL/EL PROFESIONAL PRESTADOR/A DEL SERVICIO”), tiene entre su objeto social y así consta en sus estatutos la prestación de servicios de “social media manager” y servicios conexos a dicha prestación, que presta, a través de personal cualificado, servicios profesionales orientados a la planificación y diseño de marketing digital y gestión de redes sociales.

II.- Que el CLIENTE quiere contratar dichos servicios especializados.

CLÁUSULAS

Primera.- Objeto del contrato

LA MERCANTIL/EL PROFESIONAL PRESTADOR/A DEL SERVICIO se obliga, con carácter general, a prestar los siguientes servicios:

Planificar y preparar la estrategia en Internet y redes sociales de la empresa y la/s marca/s del CLIENTE.
Definir los objetivos que el CLIENTE pretende lograr con sus acciones de social media de la manera más precisa posible.
Mejora el posicionamiento en Internet y garantizar una presencia constante y adecuada del CLIENTE en Internet y Redes Sociales.
Monitorizar las acciones en este ámbito, comprobando si se están cumpliendo los objetivos previstos y si el retorno de la inversión es el correcto.
Analizar la evolución de los principales competidores del CLIENTE.
Conocer la situación dentro del mercado y las necesidades de los clientes de la empresa comitente (CLIENTE).
Mantener una relación fluida con el Community Manager, ayudándole a planificar su trabajo, dándole las indicaciones pertinentes y manteniéndole al día de todas las novedades.
Analizar e interpretar los datos de fuentes externas e internas, en especial los que le llegan del Community Manager.
Gestionar con responsabilidad la estrategia en Internet y redes sociales, evitando actuaciones que puedan causar daño al buen nombre y reputación del CLIENTE.
Eliminar a la mayor brevedad toda información o datos del CLIENTE que aparezcan en redes sociales e Internet y que sean falsos, inexactos o queden desactualizados (derecho la olvido).

Segunda.- Servicios específicos

En concreto, se prestarán los siguientes servicios (Indicar los servicios específicos; esto son meros ejemplos):

En primer lugar, creación de perfiles en Redes Sociales (Generalmente Facebook, Twitter, Instagram y Google +, con posibilidad de otras a solicitud expresa del CLIENTE). Si el CLIENTE, ya tuviera un perfil en RRSS, los servicios consistirán en la mejorar en cuanto a la información, número de seguidores, imágenes de perfil y portada…, es decir, darle un mejor orden a su red social.
Creación de contenido en RRSS, con realización de al menos 2 post semanales, pudiendo incrementar la cantidad bajo acuerdo expreso con el CLIENTE. El contenido es creado por LA MERCANTIL/EL PROFESIONAL PRESTADOR/A DEL SERVICIO en base a información buscada en periódicos, revistas, u otros blogs relacionados con el sector de la empresa, o es enviado por el CLIENTE (imágenes, enlaces, noticias…) con posterior revisión, momento a partir del cual se aplica el formato correcto a dicho contenido y se publica en las redes sociales.
Si el CLIENTE dispone de Blog propio, se determinará si LA MERCANTIL/El PROFESIONAL PRESTADOR/A DEL SERVICIO se pudiera encargar de la elaboración dicho contenido (En la frecuencia que determine el propio CLIENTE), basándonos en las últimas tendencias, últimas noticias, eventos importantes, etc., y compartiendo a su vez el post en las redes sociales.
A final de cada mes, el CLIENTE recibirá un informe con las estadísticas de cada una de sus redes sociales, así como de las campañas de email marketing (Incrementos del número de seguidores, los «likes/me gusta», el alcance y la interacción de sus posts). Este informe podrá incluir aquellas recomendaciones y mejoras para el posicionamiento web.
servicio consistente en posicionar la web del CLIENTE en primera página de los buscadores a través de campañas y actuaciones tecnológicas, creación de la campaña, búsqueda y selección de las mejores palabras claves, datos de información… Los importes relativos al coste de la campaña correrán a cuenta del CLIENTE

Tercera.- Obligaciones del Cliente.

El CLIENTE se obliga a cumplir con todas aquellas obligaciones que se deriven del presente contrato conforme a las exigencias de la buena fe, y aquellas derivadas del encargo realizado, así como cuantas resulten de aplicación a las actividades a desarrollar, especialmente las referidas al cumplimiento de la normativa servicios de sociedad de la información y privacidad.

En concreto, el CLIENTE se obliga a facilitar toda la información y los datos para la adecuada prestación del servicio y a pagar en el tiempo y forma convenidos a continuación.

Cuarta.- Retribución e impago

Se fija una retribución mensual de [IMPORTE] euros, que se pagará por el CLIENTE el día 27 de cada mes (Fijar la duración del contrato en la forma que se estime pertinente).

El impago de dos mensualidades sin justa causa por parte del CLIENTE conllevará la resolución del contrato y el pago de [IMPORTE] euros en favor de LA MERCANTIL/EL PROFESIONAL PRESTADOR/A DEL SERVICIO en concepto de cláusula penal.

Quinta.- Duración

El presente contrato tendrá la duración de un año a contar desde la firma del mismo, prorrogable manera indefinida (Fijar la duración del contrato en la forma que se estime pertinente), salvo que, transcurrido el primer año, cualquiera de las partes comunique a la otra, con un preaviso de dos meses, su voluntad de extinguir el presente contrato.

Sexta.- Responsabilidad

LA MERCANTIL/EL PROFESIONAL PRESTADOR/A DEL SERVICIO asume el deber (Delimitar la responsabilidad en la forma que se estime conveniente) de realizar la prestación contratada con la diligencia de un buen profesional y asume la responsabilidad de los daños que pueda causar al CLIENTE como consecuencia de actuaciones negligentes directamente relacionadas con la prestación de los servicios contratados, pero no asumirá la responsabilidad que pudiera derivarse de los incumplimientos o conductas negligentes de terceros en la prestación de sus servicios, para lo que el CLIENTE tendrá acción directa frente a los mismos en virtud de la legislación vigente aplicable.

La citada responsabilidad que pudiera derivarse de este contrato quedará garantizada con un seguro de responsabilidad civil.

Séptima.- Modificación del contrato.

Las partes podrán modificar de mutuo acuerdo cualquiera de las cláusulas contenidas en el presente contrato.

Octava.- Desistimiento y resolución del contrato

El CLIENTE podrá desistir el presente contrato sin penalización alguna dentro del mes siguiente a la celebración del mismo. En caso de que se supere dicho plazo ya no podrá desistir, quedando el CLIENTE obligado a pagar la cuantía estipulada en la cláusula cuarta del presente contrato.

Cualquier incumplimiento de LA MERCANTIL/EL PROFESIONAL PRESTADOR/A DEL SERVICIO de los servicios contratados, permitirá al CLIENTE extinguir automáticamente el contrato, a través de comunicación fehaciente, en la que se especificará el motivo de la resolución, sin perjuicio de las responsabilidades que pudieran derivarse de dicho incumplimiento de conformidad con la cláusula sexta.

Novena.- Confidencialidad y protección de datos

LA MERCANTIL/EL PROFESIONAL PRESTADOR/A DEL SERVICIO se obliga a guardar la debida confidencialidad y a proteger los datos personales titularidad del CLIENTE a los que pudiera tener acceso o gestionar como “encargado del tratamiento”, obligándose a cumplir con la normativa de protección de datos nacional y comunitaria.

Décima.- Know-how y propiedad intelectual

El Know-How específico y propio de LA MERCANTIL/EL PROFESIONAL PRESTADOR/A DEL SERVICIO no podrá ser utilizado por el CLIENTE o por cualquier otro prestados de servicios de social media manager contratado por el Cliente.

En caso de incumplimiento por el CLIENTE o una vez extinguido el presente contrato, se prohíbe el uso del know-How suministrado por LA MERCANTIL/El PROFESIONAL PRESTADOR/A DEL SERVICIO en la prestación de los servicios contratados.

Cada una de las Partes reconoce la titularidad de la otra y de cualesquiera otros terceros respecto de todos sus derechos de propiedad intelectual, industrial y cualesquiera otros análogos sobre textos, imágenes, fotografías, tecnologías, marcas, logos, nombres de dominio, y cualesquiera otros elementos, creaciones, invenciones o signos distintivos de su propiedad.

Las marcas, logotipos, nombres comerciales, signos distintivos, y demás elementos de propiedad industrial incorporados son titularidad de los respectivos titulares.

Asimismo, todos los derechos de propiedad industrial y/o intelectual sobre las Marcas, así como de cualesquiera ampliación, mejora o modificación de las mismas, son de propiedad exclusiva de cada una de las Partes actualmente propietarias, por lo que las Partes se abstendrán de utilizar o registrar a su nombre cualesquiera otras marcas u otros signos distintivos de la otra Parte sea titular y no podrá modificar, reproducir, distribuir ni comunicar públicamente o poner a disposición de terceros las Marcas, salvo en caso de consentimiento expreso y escrito de la otra Parte.

Todos los derechos de propiedad industrial y/o intelectual sobre los Productos, sin incluir en los mismos las Marcas propiedad de las Partes, así como de cualesquiera ampliación, mejora o modificación de las mismas, serán de propiedad exclusiva de la Parte productora, por lo que, una vez finalizado el Acuerdo las Partes se abstendrán de utilizar o registrar a su nombre cualesquiera Marcas o signos distintivos relativos y/o relacionados con los Productos y no podrá modificar, reproducir, distribuir ni comunicar públicamente o poner a disposición de terceros la propiedad industrial/intelectual.

Las Partes se obligan a informar a la otra, de manera rápida y eficaz, de toda infracción o fundado temor de infracción por parte de clientes, usuarios o de terceros de las Marcas o de desarrollos de las mismas que pudiera afectar a los legítimos intereses de la otra Parte, según corresponda.

Undécima.- Resolución de controversias

Para resolver cualquier tipo de controversia derivada de la interpretación y aplicación del presente contrato, ambas partes intentarán con carácter preferente y previo una mediación profesional.

En todo caso serán competentes para conocer de las controversias que se derivan del presente contrato los tribunales de [LOCALIDAD].

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Contrato que se firma en [LUGAR], a [FECHA].

Firma Firma

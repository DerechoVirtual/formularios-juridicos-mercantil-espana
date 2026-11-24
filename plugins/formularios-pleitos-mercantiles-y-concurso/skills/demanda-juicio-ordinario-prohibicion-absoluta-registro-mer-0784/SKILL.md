---
name: demanda-juicio-ordinario-prohibicion-absoluta-registro-mer-0784
description: "Demanda de juicio ordinario por prohibición absoluta de registro de marca. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de juicio ordinario por prohibición absoluta de registro de marca

> Formulario **MER-0784** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de juicio ordinario por prohibición absoluta de registro de marca» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de juicio ordinario por prohibición absoluta de registro de marca” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-juicio-ordinario-prohibicion-absoluta-registro-mer-0784`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (9 veces)
- [ ] CLASES DEL NOMENCLÁTOR (3 veces)
- [ ] DENOMINACIÓN O SIGNO (2 veces)
- [ ] MARCA/MODELO (2 veces)
- [ ] OBJETO DEL OTROSÍ (2 veces)
- [ ] CLASE
- [ ] DENOMINACIÓN SOCIAL
- [ ] LUGAR
- [ ] Nº
- [ ] Nº DE FOLIOS
- [ ] Nº DE PROCEDIMIENTO
- [ ] NÚMERO
- [ ] PRODUCTOS O SERVICIOS
- [ ] TÉRMINO DE LA MARCA
- [ ] ÓRGANO
- [ ] ÓRGANO ADMINISTRATIVO

## Normas que cita el formulario

- art. 52 LJCA
- art. 1 LJCA
- art. 2.e LJCA
- art. 14.1 LJCA
- art. 19.1.a LJCA
- art. 23 LJCA
- art. 5 Ley 17/2001
- art. 11.1 f) Ley 32/1988
- art. 139.1 LJCA

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

- Junto a «… respetuosamente en [LUGAR], a [FECHA]. Firma de Abogado/a Firma de Procurador/a»: requisito de procedibilidad del art. 5 LO 1/2025 — antes de presentar la demanda hay que intentar un medio adecuado de solución de controversias (MASC) y acreditarlo con la demanda (arts. 264.4.º y 399.3 LEC), salvo las materias excluidas del art. 5.2. Fuente: LO 1/2025, arts. 5 a 7 (BOE-A-2025-76).

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

RECURSO Nº [Nº DE PROCEDIMIENTO]

SECCIÓN Nº [NÚMERO]

Que, en cumplimiento de lo dispuesto en la resolución de fecha [FECHA], paso, en tiempo y forma, a formalizar Demanda en el Recurso Contencioso Administrativo referenciado, al amparo del art. 52 y demás concordantes de la LJCA, contra la resolución de [FECHA] de fecha [FECHA], dictada por la Oficina de Patentes y Marcas (OEPM), en base a los siguientes

HECHOS

PRIMERO.- En fecha [FECHA] mi representada presentó ante la Oficina Española de Patentes y Marcas (OEPM) solicitud de registro de la marca [MARCA/MODELO] (mixta) para productos comprendidos en las clases [CLASES DEL NOMENCLÁTOR] del Nomenclátor Internacional.

SEGUNDO.- Tras seguirse los trámites procedimentales, en los que compareció como la entidad [DENOMINACIÓN SOCIAL] como opositora, el Jefe de la Oficina dictó resolución de fecha [FECHA] considerando que la solicitud se hallaba incursa en la prohibición del artículo 5.1.g) de la Ley de Marcas en relación con los productos comprendidos en las clases [CLASES DEL NOMENCLÁTOR], al incluir indicaciones geográficas no idóneas para distinguir el concreto tipo de productos o servicios [PRODUCTOS O SERVICIOS],por inducir a error a los consumidores medios destinatarios de los productos reivindicados sobre el verdadero origen geográfico de dichos productos o servicios

TERCERO.- En fecha [FECHA], mi representada presentó recurso de alzada ante la Directora de la OEPM, en el cual alegaba que la denegación se basaba en una interpretación errónea de los requisitos necesarios para aplicar de forma debida el artículo 5.1.g) de la Ley de Marcas y el artículo 5.2 del referido Cuerpo legal y no ajustada a Derecho, pues el consumidor no puede confundir el signo con ninguna de las características de los productos a que se refiere la marca, no solo por la propia naturaleza y estructura de aquel, sino, además, por el uso y arraigo que el mismo tiene, existiendo varias marcas de composición muy similar a la solicitada registradas en la OPEM.

CUARTO.- El recurso de alzada fue desestimado mediante resolución de [FECHA], objeto de impugnación en este proceso, que funda su pronunciamiento en un FJ único, donde se reiteran los fundamentos de la resolución denegatoria del registro, contra la cual fue interpuesto el presente recurso contencioso-administrativo cuya demanda ahora se formaliza.

A estos hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- PROCESALES

PRIMERO.- JURISDICCION: Corresponde a esa Jurisdicción Contenciosa Administrativa conocer del asunto que le es sometido, en virtud de lo dispuesto en el art. 1 de la LJCA, por ser ésta pretensión deducida en relación con actos de la Administración Pública, sujetos al Derecho Administrativo y estar expresamente incluido en el art. 2.e) de la citada LJCA.

SEGUNDO.- COMPETENCIA: Es competente la Sala de lo Contencioso Administrativo, a la que me dirijo, de conformidad con el art. 10.1.i) de la mentada Ley, ostentando asimismo la competencia territorial conforme al art. 14.1 regla segunda de la LJCA.

TERCERO.- CAPACIDAD PROCESAL; Se da la misma en mi mandante, conforme a la legislación aplicable.

CUARTO.- LEGITIMACIÓN: Mi principal tiene legitimación activa, conforme al art. 19.1.a) de la LJCA, en su condición de interesado en la inscripción de la marca, en tanto la legitimación pasiva corresponde a la OEPM que dictó la resolución denegatoria.

QUINTO.- REPRESENTACIÓN Y DEFENSA: Son cumplimentados los requisitos establecidos por el art. 23 de la LJCA, el presente supuesto, al comparecer con Procurador y Abogado.

II.- DE FONDO

PRIMERO.- Infracción del art. 5.1.g) de la Ley de Marcas: la marca solicitada no incurre en la prohibición absoluta establecida en el precepto ni puede inducir a error a los consumidores.

El recurso se presenta por infracción del art. 5.1.g) de la Ley de Marcas por cuanto que la marca no incurre en la prohibición absoluta establecida en dicho precepto ni puede inducir en ningún caso a error sobre la calidad o procedencia geográfica de los productos comprendidos en la marca.

La Oficina de Patentes y Marcas deniega la inscripción por aplicación del art. 5.1.g) de la Ley de Marcas, que establece una prohibición absoluta de registro de los signos que puedan inducir al público a error, por ejemplo sobre la naturaleza, la calidad o la procedencia geográfica del producto o servicio. En efecto, el artículo 5 de la Ley 17/2001, de 7 de diciembre, de Marcas, al regular las «prohibiciones absolutas», establece:

«1. No podrán registrarse como marca los signos siguientes: a) (...). g) Los que puedan inducir al público a error, por ejemplo sobre la naturaleza, la calidad o la procedencia geográfica del producto o servicio (...).»

En interpretación de esta prohibición, la jurisprudencia ha reiterado que, para apreciar el carácter distintivo de una marca, se debe atender primero a los productos o servicios reivindicados que tiene la marca y después a la percepción que se presume produce en los consumidores o usuarios de los sectores interesados, respecto de la fuerza individualizadora del signo marcario, a los efectos de determinar si la marca es intrínsecamente idónea para identificar el producto o servicio en cuestión sin producir error en los consumidores sobre su procedencia empresarial.

En este caso, la marca solicitada no tiene relevancia para confundir a los consumidores, pues ninguna duda ofrece sobre su procedencia empresarial desde la perspectiva de un consumidor medio. Como indican las SSTS de 18 de mayo de 2009 y 25 de marzo de 2010, la prohibición de registro prevista en el artículo 11.1 f) de la Ley 32/1988, de 10 de noviembre, de Marcas, que resulta plenamente aplicable a la prohibición contemplada en el artículo 5.1 g) de la vigente Ley de Marcas de 2011, tiene por objeto impedir «el registro de signos distintivos que incluyan indicaciones geográficas que no sean idóneas para distinguir un concreto tipo de productos o servicios por inducir a error a los consumidores medios destinatarios de los productos reivindicados sobre el verdadero origen geográfico de dichos productos o servicios, con la finalidad de asegurar unas condiciones de leal competencia entre los fabricantes y distribuidores de productos que lleven ese tipo de indicaciones y de garantizar el derecho de los consumidores a la correcta elección de los productos que pretenden adquirir».

Pues bien, en este caso no se da el riego de confusión, no siendo aceptable que la prohibición se aplique por la mera inclusión de la denominación geográfica, puesto que la jurisprudencia en ningún momento ha afirmado que las denominaciones de origen o de ciudades, que pueden aparecer en las composiciones marcarias, tengan vedado su registro por aplicación de esta prohibición absoluta, pues lo relevante para la prohibición es la posibilidad de inducir a error al consumidor o usuario en relación con las características de la entidad de cuyo origen proceden los productos o servicios.

La marca aspirante [ÓRGANO] en ningún caso puede inducir a error a los consumidores o usuarios, puesto que se refiere a productos de la clase [CLASE], desligados de cualquier carácter oficial o de procedencia del producto en relación con alguna de las denominaciones de origen, por lo que no puede aplicarse el art. 5.1.g) de la Ley de Marcas, el cual resulta por ello infringido, debiendo procederse al registro de la marca.

SEGUNDO.- El requisito de autorización del consejo regulador excede de la prohibición absoluta del art. 5.1.g) de la Ley de Marcas.

En la resolución impugnada se razona que para poder registrar una marca que incluya un nombre protegido por una denominación de origen es necesaria la autorización del consejo regulador, lo cual infringe el art. 5.1.g) de la Ley de Marcas exceder de los términos de la prohibición recogida en el citado precepto.

La doctrina jurisprudencial expuesta reitera que el art. 5.1.g) de la Ley de Marcas no prohíbe absolutamente la utilización de la denominación marcaria de la procedencia geográfica de un producto, sino lo que impide es su empleo acompañado de otros elementos cuya apreciación conjunta permita vincular la marca con el distintivo de calidad de que se trate, y que este precepto ha de ser aplicado con carácter restrictivo en cuanto que norma prohibitiva. La jurisprudencia circunscribe los supuestos prohibidos a los que el solicitante hace uso de un signo distintivo confundible con una Denominación de Origen, que puede producir error en los consumidores, pero que no identifica productos amparados por tal denominación de origen, lo cual no sucede en este caso donde no concurren los presupuestos aplicativos de las prohibiciones del art. 5.1 de la Ley de Marcas.

La Sala de lo Contencioso-Administrativo del Tribunal Supremo ha reiterado, en relación con la protección jurídica de las marcas que designan productos amparados en el reconocimiento de Denominaciones de Origen, que dicha protección tiene como exclusiva finalidad la de preservar efectivamente los derechos de los consumidores a una adecuada elección del producto ofrecido, en aras de impedir que se produzca confusión, respecto de la procedencia geográfica de un determinado producto, impidiendo que salgan al mercado con posible engaño del consumidor, lo cual no sucede en este caso donde la combinación de términos de la marca solicitada y la clase de productos a que se dirige descarta cualquier tipo de confusión desde la perspectiva del consumidor medio, quedando totalmente identificado su origen o procedencia empresarial, por lo que en modo algun puede entenderse concurrente la prohibición absoluta de registro del artículo 5.1 de la Ley de Marcas.

TERCERO.- Infracción del principio de igualdad y seguridad jurídica: inscripción de otras marcas con el término

La decisión combatida infringe los principios de igualdad y de seguridad jurídica, por ser contraria a previas decisiones sobre la inscripción de marcas con el término «[DENOMINACIÓN O SIGNO]» para las clases [CLASES DEL NOMENCLÁTOR], siendo incomprensible que, ante las mismas situaciones de hecho y de derecho que se plantean en este caso, la Oficina Española de Patentes y Marcas cambie de criterio sin motivación alguna, generando una abrumadora inseguridad jurídica para el titular marcario.

Tal como consta en la documentación aportada por esta parte obrante en los folios [Nº DE FOLIOS] del expediente administrativo, existen hasta un número de [Nº] marcas registradas, denominativas y mixtas, con el término «[DENOMINACIÓN O SIGNO]», idénticas a la que aquí nos interesa y registradas para los mismos productos y servicios que ahora se solicitan, de modo que si la OEPM ha inscrito todas estas marcas es por entender que el término en cuestión no resultaba afectado la prohibición absoluta del art. 5.1.g) de la Ley de Marcas, por lo que la decisión ahora impugnada contraviene el principio de igualdad y seguridad jurídica, así como los propios actos de la Administración al apartarse de forma inmotivada de los precedentes administrativos.

Por todos estos motivos, se solicita que se declare la nulidad de la resolución impugnada, reconociendo el derecho de mi representada a la inscripción de la marca.

CUARTO.- Costas procesales.

En cuanto a las costas, es de aplicación el art. 139.1 de la LJCA debiendo imponerse a la Administración demandada, siendo que el caso no presenta dudas de hecho ni de derecho.

En su virtud,

SUPLICO A LA SALA que, habiendo por presentado este escrito con sus copias, se sirva admitirlos y, teniendo por evacuado, en tiempo y forma, el trámite conferido para formalización de la demanda, con devolución del expediente, y disponga la sustanciación del recurso, tras los trámites pertinentes, a fin de que en su día, sea dictada Sentencia, por la que se reconozca y declare:

Primero: que la resolución de la OEPM de fecha [FECHA] objeto de impugnación, no es conforme a Derecho, declarando su anulación, reconociendo el derecho de mi representada a la inscripción de la marca [MARCA/MODELO].

Segundo: que se condene en costas a la Administración Pública demandada.

[OPCIONAL — incluir si procede]

OTROSI I [OBJETO DEL OTROSÍ]: Se solicita el recibimiento a prueba con el fin de poder acreditar la realidad de las alegaciones de la demanda y que versará exclusivamente sobre (se fijarían los puntos de hecho): 1) ausencia de elementos de confusión en los consumidores derivados de la denominación marcaria; y 2) registro de otras marcas con la indicación [TÉRMINO DE LA MARCA] por la OEPM.

(Proposición de prueba): Para acreditar tales hechos, y sin perjuicio de lo que resulte de la contestación a la demanda, esta parte PROPONE de los siguientes medios de prueba:

I. DOCUMENTAL: Por reproducido el expediente administrativo.
II. MÁS DOCUMENTAL: Que se expida oficio a [ÓRGANO ADMINISTRATIVO].

Por lo que SUPLICO A LA SALA acuerde de conformidad en el momento procesal correspondiente, admitiendo los medios de prueba propuestos por esta parte.

[OPCIONAL — incluir si procede]

OTROSI II [OBJETO DEL OTROSÍ]: Que a los efectos del art. 40 y ss. de la LJCA, señalo la cuantía del presente recurso como indeterminada.

Por lo que SUPLICO A LA SALA tenga por señalada la cuantía del recurso como indeterminada.

Es justicia que pido respetuosamente en [LUGAR], a [FECHA].

Firma de Abogado/a	Firma de Procurador/a

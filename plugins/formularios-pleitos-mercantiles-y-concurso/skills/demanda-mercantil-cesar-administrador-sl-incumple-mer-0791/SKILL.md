---
name: demanda-mercantil-cesar-administrador-sl-incumple-mer-0791
description: "Demanda mercantil para cesar al administrador de una SL que incumple la prohibición de competencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda mercantil para cesar al administrador de una SL que incumple la prohibición de competencia

> Formulario **MER-0791** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Demanda de juicio ordinario que formula un socio de una sociedad limitada contra uno de sus administradores por infringir la prohibición de competencia (arts. 229.1 y 230.3 TRLSC), solicitando su cese judicial, con solicitud de medida cautelar de suspensión en el cargo.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda mercantil para cesar al administrador de una SL que incumple la prohibición de competencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda mercantil para cesar al administrador de una SL que incumple la prohibición de competencia” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:demanda-mercantil-cesar-administrador-sl-incumple-mer-0791`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (8 veces)
- [ ] FECHA (6 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDADO (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] PORCENTAJE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DOMICILIO SOCIAL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE (2 veces)
- [ ] PERSONA VINCULADA (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] ACTIVIDAD
- [ ] ACTIVIDAD DE LA SOCIEDAD ADMINISTRADA
- [ ] ACTIVIDAD DE LA SOCIEDAD COMPETIDORA
- [ ] ACTIVIDADES CONCRETAS DE COMPETENCIA
- [ ] DATOS REGISTRALES
- [ ] DENOMINACIÓN SOCIAL DE LA SOCIEDAD COMPETIDORA
- [ ] DOCUMENTOS CUYA EXHIBICIÓN SE INTERESA
- [ ] DOMICILIO PROFESIONAL
- [ ] NIF
- [ ] NOMBRE DEL NOTARIO
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL LETRADO
- [ ] NOMBRE Y APELLIDOS DEL OTRO ADMINISTRADOR
- [ ] NOMBRE Y APELLIDOS DEL PERITO
- [ ] NOMBRE Y APELLIDOS DEL PROCURADOR
- [ ] NOMBRE Y APELLIDOS DEL TESTIGO
- [ ] Nº
- [ ] Nº DE
- [ ] OBJETO SOCIAL
- [ ] OPERACIONES O ACTIVIDADES CONCRETAS DE COMPETENCIA
- [ ] SEDE

## Normas que cita el formulario

- art. 155 LEC
- art. 6 LEC
- art. 29 Código Civil
- art. 23 LEC
- art. 10 LEC
- art. 229.1 TRLSC
- art. 230.3 TRLSC
- art. 1.720 Código Civil
- art. 313 Código de Comercio
- art. 267 Código de Comercio
- art. 228 TRLSC
- art. 394 LEC
- art. 727 LEC
- art. 723.1 LEC
- art. 728 LEC
- art. 732.2 LEC
- art. 735.2 LEC

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…el domicilio social de la compañía mercantil cuyo administrador es el demandado.»: tras la LO 1/2025 la atribución de competencia a las Secciones de lo Mercantil y la regla de competencia territorial deben comprobarse en el art. 86 ter LOPJ y en los arts. 50 y ss. LEC vigentes; se conservan aquí los preceptos del original.
- Junto a «…e recibimiento a prueba del pleito, o suprimir la numeración si no se utilizan.]»: requisito de procedibilidad (art. 5 LO 1/2025): antes de demandar hay que intentar un medio adecuado de solución de controversias y acreditarlo con la demanda, salvo las materias excluidas del art. 5.2.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTA DE AYUDA: los administradores deben desempeñar el cargo con la lealtad de un fiel representante, obrando de buena fe y en el mejor interés de la sociedad. La infracción del deber de lealtad determina no solo la obligación de indemnizar el daño causado al patrimonio social, sino también la de devolver a la sociedad el enriquecimiento injusto obtenido por el administrador. Este modelo se refiere al incumplimiento de la prohibición de competencia (arts. 229.1 y 230.3 TRLSC).


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

D./Dña. [NOMBRE Y APELLIDOS DEL PROCURADOR], Procurador de los Tribunales y de D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], según acredito mediante escritura de poder que acompaño como documento nº 1 de los que se unen al presente escrito, para su unión a los autos mediante copia, previa su certificación por el Letrado de la Administración de Justicia al que tengo el honor de dirigirme, y cuya devolución intereso por precisarlo para otros usos, dirigido por el/la Letrado/a abajo firmante D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO], con despacho profesional en [DOMICILIO PROFESIONAL], ante el Tribunal comparezco y, como mejor proceda en Derecho,

DIGO:

Que mediante el presente escrito formulo demanda de juicio declarativo ordinario contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], administrador solidario de la mercantil [DENOMINACIÓN SOCIAL], S.L., por la que intereso el CESE JUDICIAL DEL ADMINISTRADOR SOCIAL que ha incurrido en prohibición de competencia, designando como su domicilio, a efectos de notificaciones, a tenor del artículo 155 de la LEC, los siguientes, por su orden respectivo:

1º.- En su domicilio particular, sito en [DOMICILIO], de [LOCALIDAD].

2º.- En el lugar donde presta sus servicios como administrador de la entidad [DENOMINACIÓN SOCIAL], S.L., con domicilio social en [DOMICILIO SOCIAL], de [LOCALIDAD].

Fundamento mis pretensiones en los siguientes

HECHOS

PRIMERO.- Mi representado es socio de la mercantil [DENOMINACIÓN SOCIAL], S.L., constituida el [FECHA], según consta en la escritura autorizada el [FECHA] por D./Dña. [NOMBRE DEL NOTARIO], Notario de [LOCALIDAD], cuyo domicilio social se halla sito en la localidad de [LOCALIDAD], [DOMICILIO SOCIAL], y que fue inscrita en el Registro Mercantil de [PROVINCIA], [DATOS REGISTRALES], el [FECHA], con NIF [NIF].

Acredito estos extremos con el documento nº 1 de los que se acompañan a este escrito, consistente en copia simple de la escritura de constitución mencionada, así como con el documento nº 2, que recoge la certificación del Registro Mercantil donde constan los datos mencionados. El objeto social de dicha mercantil consiste en [OBJETO SOCIAL].

D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE] es titular de [Nº DE] participaciones sociales de la entidad, lo que supone un [PORCENTAJE] % del capital social.

SEGUNDO.- El demandado, D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], conforma junto a D./Dña. [NOMBRE Y APELLIDOS DEL OTRO ADMINISTRADOR] el órgano de administración de la citada mercantil, desde su nombramiento en junta [ELEGIR: ordinaria / extraordinaria] celebrada el [FECHA], con el carácter de solidario, tal y como consta en la certificación del Registro Mercantil que se acompaña como documento nº 3.

TERCERO.- Recientemente se ha tenido conocimiento de que, desde el [FECHA], el demandado D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO] constituyó con su [ELEGIR: cónyuge / pareja / otra persona vinculada] D./Dña. [NOMBRE Y APELLIDOS] la entidad [DENOMINACIÓN SOCIAL DE LA SOCIEDAD COMPETIDORA], S.L., dedicada a [ACTIVIDAD], suscribiendo un [PORCENTAJE] % de las participaciones sociales de la misma, perteneciendo la otra parte a la citada persona, quien es además su administradora única. Se acompaña certificación al respecto del Registro Mercantil, como documento nº 4.

La referida sociedad limitada ha intervenido recientemente en [OPERACIONES O ACTIVIDADES CONCRETAS DE COMPETENCIA].

CUARTO.- Que en junta de socios de [DENOMINACIÓN SOCIAL], S.L., celebrada en fecha [FECHA], el demandado negó los hechos que aquí se le imputan, recordándose en intervención de mi mandante que no se había tratado en ninguna junta de socios propuesta alguna dirigida a la autorización expresa, por parte de dicho órgano social, para el ejercicio de actividades análogas a las realizadas por la propia mercantil administrada por el demandado. Se acompaña, como documento nº 5, copia del acta en que se reflejan estos extremos y, como documento nº 6, certificado negativo del Registro Mercantil en tal sentido.

A los presentes hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I. Capacidad de las partes

Ambas partes son plenamente capaces conforme a lo dispuesto en el art. 6 de la LEC, en relación con los artículos 29 y 322 del Código Civil, pues se trata de dos personas en el pleno ejercicio de sus derechos civiles.

II. Postulación y defensa

Conforme a lo previsto en los artículos 23 y 31 LEC, se presenta la demanda por medio de Procurador legalmente habilitado y bajo la dirección del Letrado firmante de la misma.

III. Legitimación

Ostenta legitimación activa mi poderdante, pues su acción nace de su carácter de socio de una sociedad de responsabilidad limitada y le corresponde su ejercicio en nombre propio a los efectos del art. 10 LEC, en relación con el artículo 229.1 del texto refundido de la Ley de Sociedades de Capital, aprobado por el Real Decreto Legislativo 1/2010, de 2 de julio.

Asimismo, está legitimado pasivamente el demandado como administrador social de una sociedad de responsabilidad limitada que ha incurrido en prohibición de competencia, con arreglo al precepto legal citado.

IV. Jurisdicción y competencia

Se plantea la demanda ante la Sección de lo Mercantil del Tribunal de Instancia que corresponda, como parte de la jurisdicción civil, en virtud del art. 87 de la Ley Orgánica del Poder Judicial.

Asimismo, el Tribunal al que tengo el honor de dirigirme es competente territorialmente, según el artículo 229.1 TRLSC, pues a su partido judicial corresponde el domicilio social de la compañía mercantil cuyo administrador es el demandado.

V. Procedimiento

Según los artículos 248 y 249.2 de la LEC el presente pleito ha de tramitarse por las reglas del juicio ordinario, pues, no teniendo materia especial propia del juicio verbal, su interés económico resulta imposible de calcular, ni siquiera de modo relativo.

VI. Fondo del asunto

1) Del marco general normativo:

El artículo 229.1 TRLSC prohíbe a los administradores sociales desarrollar actividades por cuenta propia o cuenta ajena que entrañen una competencia efectiva, sea actual o potencial, con la sociedad o que, de cualquier otro modo, le sitúen en un conflicto permanente con los intereses sociales, salvo autorización expresa de la sociedad mediante acuerdo de la junta general (art. 230.3 TRLSC).

De esta forma, los artículos expuestos reproducen en la actual legislación la tradicional prohibición contenida en el artículo 65 de la derogada Ley de Sociedades de Responsabilidad Limitada, y la facultad de cualquier socio, independientemente de su cuota de capital social, para solicitar el cese judicial de aquel administrador que la contravenga. Precepto legal que, a su vez, entronca con la tradicional regulación del contrato de mandato y de sociedad, sobre la base de la buena fe y lealtad contractual que se exigen al mandatario o administrador. En esta línea, el artículo 1.720 del Código Civil («Todo mandatario está obligado a dar cuenta de sus operaciones y a abonar al mandante cuanto haya recibido en virtud del mandato, aun cuando lo recibido no se debiera al segundo»); el artículo 1.666 del mismo texto legal («La sociedad debe tener un objeto lícito, y establecerse en interés común de los socios»), y el artículo 1.684, según el cual «Cuando un socio autorizado para administrar cobra una cantidad exigible, que le era debida en su propio nombre, de una persona que debía a la sociedad otra cantidad también exigible, debe imputarse lo cobrado en los dos créditos a proporción de su importe, aunque hubiese dado el recibo por cuenta de sólo su haber; pero, si lo hubiere dado por cuenta del haber social, se imputará todo en éste». Igualmente, el artículo 313 del Código de Comercio de 1829 contenía una prohibición similar a la prevista en el artículo 267 del Código de Comercio de 1885, que impone que «Ningún comisionista comprará para sí ni para otro lo que se le haya mandado vender, ni venderá lo que se le haya encargado comprar, sin licencia del comitente».

2) Fundamento y naturaleza de la prohibición:

El objetivo de la norma es tratar de impedir que los administradores sociales, valiéndose de los conocimientos adquiridos en la gestión y representación social, obtengan una ventaja indebida en el mercado, haciendo prevalecer su interés personal sobre el propio de la sociedad. Así, la sentencia del Tribunal Supremo de 5 de diciembre de 2008, rec. 1353/2003, con referencia a otra sentencia anterior de 9 de septiembre de 1998 (en interpretación del derogado artículo 65 LSRL), señala que tal prohibición se encuentra fundada en la existencia de una incompatibilidad y tiene su fundamento en el sustrato ético que debe presidir las relaciones económicas, por lo que se impone una interpretación rigurosa del precepto, pues la Ley ha querido revestir de un especial rigor a esta prohibición, de manera que su infracción autoriza la expulsión del socio-administrador. En la misma línea, el mismo Tribunal señala en su sentencia de 6 de marzo de 1992, rec. 181/1990, que «No debe olvidarse que, mediante la sociedad, varias personas aúnan sus esfuerzos para la consecución de un fin común, normalmente a través de la cooperación duradera, y en los casos de conflicto entre el interés individual extrasocial del socio y el interés social común a todos, aquel interés particular ha de respetar el interés social, libremente asumido por el socio, y ha de estar limitado por la subordinación del interés personal del socio al interés social, que debe ser preferido».

3) Requisitos de la acción:

a) Ejercicio del mismo, análogo o complementario género de actividad que constituya el objeto social de la entidad administrada por el demandado. El legislador pretende, como ya se ha adelantado, evitar un perjuicio actual o potencial, sin que sea necesario que tal perjuicio esté concretado (sentencia del Tribunal Supremo de 26 de enero de 2006), ni se tenga que demostrar un beneficio efectivo en otras empresas o en otras personas (sentencia del Tribunal Supremo de 12 de junio de 2008, rec. 1136/2001), debiendo tratarse de un daño real y consistente originado por una contraposición de intereses, valorada a tenor de las circunstancias del caso (sentencia del Tribunal Supremo de 28 de junio de 1982). Para ello se exige que concurran las siguientes circunstancias:

— Conflicto de intereses, puesto que el administrador social está sujeto, según los artículos 228 y 229 TRLSC, a los deberes de diligencia (llevando a cabo cuantas acciones se precisen para la consecución del interés social), lealtad (lo que implica no anteponer sus intereses individuales a los de la sociedad administrada) y secreto o confidencialidad (guardar secreto de las informaciones, datos, informes o antecedentes que conozca como consecuencia del ejercicio del cargo, sin que las mismas puedan ser comunicadas a terceros). Obligaciones, todas ellas, vulneradas por el demandado al dedicarse, mediante otra sociedad, a un objeto social muy similar, aprovechando el conocimiento del mercado, proveedores, profesionales, etc., que ha ido obteniendo durante estos últimos meses en el desempeño de su cargo como administrador social, y que, potencialmente, puede estar utilizando en el desarrollo de la actividad de la nueva entidad, que ya se ha concretado en [ACTIVIDADES CONCRETAS DE COMPETENCIA].

— La participación del administrador en la actividad competidora y la habitualidad o estabilidad de la misma. Extremo que concurre atendiendo al hecho de que el demandado ostenta [PORCENTAJE] % de las participaciones sociales de la mercantil competidora, mientras que [PERSONA VINCULADA] ostenta el resto, además de ser la administradora única. De esta manera, existen indicios suficientes para suponer que dicha entidad está controlada y dirigida de hecho por el demandado, y que la misma seguirá ocupándose en el futuro de otras operaciones análogas.

— El grado de coincidencia, similitud o proximidad de la actividad desarrollada por el administrador con la de la propia sociedad. Similitud que, en este caso, raya en la plena coincidencia, toda vez que la nueva sociedad se dedica a un objeto análogo, [ACTIVIDAD DE LA SOCIEDAD COMPETIDORA], cuando la actividad a la que se viene dedicando desde hace mucho tiempo la entidad administrada por el demandado es [ACTIVIDAD DE LA SOCIEDAD ADMINISTRADA].

b) Que dicha actividad no se encuentre autorizada expresamente por la entidad administrada, mediante acuerdo de la junta general. Sin que tal excepción concurra cuando el administrador o administradores realicen el comportamiento prohibido con el conocimiento de alguno o algunos socios o, incluso, con su autorización tácita o resultante de actos concluyentes. Debe rechazarse, en este sentido, la posibilidad de considerar eficaz el consentimiento tácito de la sociedad, tal y como señala la sentencia de la Audiencia Provincial de Lleida de 23 de marzo de 2005, rec. 493/2004. En el presente caso, no se ha tratado en ningún orden del día de junta de socios solicitud alguna en tal sentido por parte de este administrador o por parte de otro, y no se tiene constancia de consentimiento tácito otorgado por mi mandante u otros integrantes de aquella.

4) Sanción por el incumplimiento

La infracción de la prohibición de competencia lleva aparejadas unas sanciones específicas en todo caso; concretamente, el cese del administrador, que puede ser decretado directamente por el Juez a petición de cualquier socio, según lo dispuesto en la jurisprudencia que ha venido interpretando su antecedente en la derogada Ley de Sociedades de Responsabilidad Limitada, de la que es ejemplo la sentencia del Tribunal Supremo de 26 de enero de 2006, rec. 2230/1999.

VII. Costas

El total vencimiento de la parte demandada, unido a su temeridad y mala fe, determina, según el artículo 394 LEC, que esta deba satisfacer todas las costas del presente procedimiento.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL, que teniendo por presentado este escrito de demanda con sus documentos y copias, se sirva admitirlo y acordar de conformidad, teniendo por interpuesta demanda de juicio declarativo ordinario contra D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], para que en su día, seguidos los trámites legales oportunos, se dicte sentencia por la que se declare el cese del demandado como administrador solidario de «[DENOMINACIÓN SOCIAL], S.L.» por causa de infracción de la prohibición de dedicarse, por cuenta propia o ajena, al mismo, análogo o complementario género de actividad que constituya el objeto social, condenándole al pago de las costas causadas.

OTROSÍ DIGO III, que, con el fin de asegurar el buen resultado del presente pleito, conforme a lo previsto en los apartados 6 y 11 del artículo 727 de la LEC, SOLICITO LA ADOPCIÓN DE LA MEDIDA CAUTELAR de SUSPENSIÓN DEL CARGO DE ADMINISTRADOR SOLIDARIO de «[DENOMINACIÓN SOCIAL], S.L.» que ostenta el demandado, hasta que recaiga sentencia, con suspensión de todas sus facultades administrativas y representativas inherentes a dicho cargo, SIN AUDIENCIA DE LA PARTE CONTRARIA.

Todo ello con base en los siguientes

HECHOS

I.- Periculum in mora

La presente demanda tiene por objeto evitar la competencia ilícita por parte de uno de sus dos administradores solidarios, quien, en dicha calidad, tiene las más amplias facultades de gestión de la sociedad en cuestión. Por ello, el conocimiento de la acción principal ejercitada por parte del demandado podrá provocar una reacción negativa que le lleve a intensificar su gestión desleal (ya iniciada con la prohibición vulnerada) o a acelerar el proceso de favorecimiento a la entidad que, entendemos, administra de hecho. Y así, una eventual sentencia estimatoria podría resultar estéril, pues el bien jurídico y fin protegido, el interés prevalente de [DENOMINACIÓN SOCIAL], S.L., habría desaparecido con la propia concreción del perjuicio que se quiere evitar durante el desarrollo del procedimiento principal.

II.- Fumus boni iuris

De los documentos acompañados a la demanda se acredita el objeto social idéntico o análogo de ambas entidades, la condición de administrador social de [PERSONA VINCULADA] y el control de todas las participaciones sociales de la entidad competidora por parte del demandado y dicha persona, así como la inexistencia de autorización alguna para el ejercicio de tal actividad concurrencial.

III.- Caución que se propone

Se propone una caución de [IMPORTE] euros, justificada en que la medida instada no puede causar perjuicio alguno al demandado, pero la LEC exige que se preste la misma.

IV.- Adopción de la medida inaudita parte

Puesto que la deslealtad puesta de manifiesto por el demandado permite sospechar que, en el lapso de tiempo que medie entre la notificación de la demanda y la adopción de la medida cautelar, puede hacer un uso irregular de sus facultades como administrador social y agravar la actual situación de perjuicio potencial para la entidad administrada.

FUNDAMENTOS DE DERECHO

I.- El artículo 723.1 LEC atribuye competencia para conocer de las solicitudes de medidas cautelares al Tribunal que esté conociendo del asunto en primera instancia o, en su caso, al que sea competente para conocer de la demanda principal.

II.- Mi mandante está legitimado activamente para hacer la petición por las razones aducidas en los antecedentes de esta solicitud de medida cautelar, y el demandado lo está pasivamente conforme al hecho segundo de este escrito, por las razones aducidas en el fundamento de derecho III de la demanda.

III.- Se cumplen los requisitos exigidos por el artículo 728 LEC para la adopción de la medida cautelar referida, acompañándose los documentos que previene el artículo 732 del mismo texto legal a tal fin.

IV.- Se ofrece la prestación de caución por importe de [IMPORTE] euros, justificando que no hay perjuicio que se pueda causar al demandado en caso de que no sea estimada la presente demanda.

Por lo expuesto,

SUPLICO AL TRIBUNAL que, formando pieza separada de medidas cautelares, se sirva adoptar la medida cautelar de suspender, hasta que recaiga sentencia, en su cargo de administrador de «[DENOMINACIÓN SOCIAL], S.L.» al demandado, D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDADO], con suspensión de todas sus facultades, tanto administrativas o internas dentro de aquella como representativas o frente a terceros, librando al efecto el correspondiente oficio al Registro Mercantil de [PROVINCIA].

OTROSÍ DIGO II, a los efectos del artículo 732.2 LEC, y para el caso de que se opte por la convocatoria de una comparecencia previa a la adopción de la medida, solicito la práctica de los siguientes medios de prueba en la vista para la audiencia de las partes, caso de celebrarse, en relación con las presentes medidas cautelares:

1º.- Interrogatorio del demandado.

2º.- Documental, consistente en los documentos acompañados al presente escrito.

3º.- Exhibición documental por la parte demandada, consistente en: [DOCUMENTOS CUYA EXHIBICIÓN SE INTERESA].

4º.- Pericial, a fin de que el perito D./Dña. [NOMBRE Y APELLIDOS DEL PERITO] se afirme y ratifique en el informe que se acompaña como documento nº [Nº].

5º.- Testifical, de D./Dña. [NOMBRE Y APELLIDOS DEL TESTIGO], con domicilio en [DOMICILIO].

[OTROSÍ DIGO I: completar con los demás otrosíes que procedan, por ejemplo la solicitud de recibimiento a prueba del pleito, o suprimir la numeración si no se utilizan.]

NOTAS DE AYUDA

(1) Se incluye una medida cautelar de suspensión de las funciones del administrador demandado, pues la pretensión se producirá en el marco de una sociedad convulsa, y el administrador demandado será un peligro (por lo amplio de sus facultades) desde el momento en que reciba el emplazamiento con copia de la demanda.

(2) En la solicitud de medida cautelar se incluye una proposición de prueba para el caso de que no se adopte la medida sin audiencia del demandado. Es este un error habitual en algunos letrados, pues confían en que se dicte el auto de medida cautelar sin más y se encuentran con que el juez no lo ve claro y les convoca a comparecencia. Y en este caso, con la norma del art. 735.2 LEC, puede dejarse sin prueba a quien no la haya pedido con la demanda.

---
name: estatutos-agrupacion-interes-economico-mer-0416
description: "Estatutos de una agrupación de interés económico. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Estatutos de una agrupación de interés económico

> Formulario **MER-0416** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo de estatutos de una Agrupación de Interés Económico (A.I.E.), sociedad mercantil que tiene por objeto una actividad económica auxiliar de la desarrollada por sus socios (empresarios, agricultores, artesanos, profesionales liberales y entidades no lucrativas de investigación), regulada por la Ley 12/1991, de 29 de abril, de Agrupaciones de Interés Económico.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Estatutos de una agrupación de interés económico» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Estatutos de una agrupación de interés económico” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:estatutos-agrupacion-interes-economico-mer-0416`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD O TERRITORIO (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] Nº
- [ ] NÚMERO MÁXIMO
- [ ] NÚMERO MÍNIMO
- [ ] PORCENTAJE

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «…sona jurídica de derecho privado no comerciante; o por una medida de incapacidad»: sustituir la referencia a «incapacidad» por la situación de persona con discapacidad con medidas de apoyo judiciales que proceda conforme a la Ley 8/2021
- Junto a «…ncargada del control de cuentas, que será ejercido por un interventor de cuentas»: comprobar si la Agrupación está obligada a auditoría conforme a la Ley 22/2015, de Auditoría de Cuentas, y, en su caso, nombrar auditor de cuentas

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE AYUDA

La Agrupación de Interés Económico es una sociedad mercantil que tiene por objeto una actividad económica auxiliar a la desarrollada por sus socios, personas físicas o jurídicas que realizan actividades empresariales, agrícolas o artesanales, entidades no lucrativas dedicadas a la investigación y quienes ejerzan profesiones liberales.

La normativa sustantiva que regula la A.I.E. es: a) la Ley 12/1991, de Agrupaciones de Interés Económico; b) el Reglamento (CEE) 2137/85 del Consejo, regulador de las Agrupaciones Europeas de Interés Económico; y c) los artículos 264 a 269 del Reglamento del Registro Mercantil. Con carácter supletorio se rigen por las normas de la sociedad colectiva compatibles con la naturaleza específica de la A.I.E., es decir, el Reglamento del Registro Mercantil (denominación, publicidad, etc.), el texto refundido de la Ley de Sociedades de Capital (administradores) y el Código de Comercio (sociedades colectivas).

Sobre la personalidad, en relación con la reclamación de obligaciones nacidas de contratos suscritos por sociedades posteriormente agrupadas para el cumplimiento de sus fines, véase la sentencia del Tribunal Supremo (Sala de lo Civil, Sección 1ª) núm. 162/2007, de 8 de febrero. Respecto de la excepción de falta de litisconsorcio pasivo necesario, no concurren los presupuestos para su apreciación al no existir razón jurídico-material para que la demanda se dirigiera al tiempo contra una entidad que era ajena por completo al conflicto y a la relación contractual, y que en consecuencia no debía ser afectada en su patrimonio por el contenido del fallo. Cuando la parte recurrente defiende que la A.I.E. debía haber sido demandada porque considera que a la fecha de la demanda era el único deudor, basa su argumento en la supuesta subrogación o sucesión universal y automática de la nueva persona jurídica en el conjunto de relaciones jurídicas de que eran titulares sus miembros al tiempo de la constitución; pero esta sucesión no solo carece de cobertura legal, al no establecerla la Ley 12/1991, sino que, en lo referente a su vertiente pasiva, esto es, a las deudas, ni siquiera admite una aplicación analógica de la figura de la asunción de deudas para presentar a la A.I.E. como único sujeto pasivo obligado, con correlativa liberación de los deudores anteriores, dado que, en primer lugar, es condición indispensable para la eficacia de la misma el cambio subjetivo en la persona del deudor (cambio que no se ha producido porque, tras constituirse la A.I.E., continuaron siendo deudores frente a la parte actora quienes originariamente suscribieron el contrato origen de la deuda, al no existir pacto al respecto ni norma imperativa que operara dicha modificación y porque mantuvieron su personalidad jurídica pese al nacimiento de la Agrupación) y, en segundo lugar, porque, aun de haberse producido ese cambio subjetivo, no habría resultado suficiente para ser oponible frente al acreedor, al ser necesario también el consentimiento expreso o tácito del acreedor (no basta su conocimiento). Conviene recordar, con relación a los presupuestos de eficacia de la asunción de deudas, la doctrina de la sentencia del Tribunal Supremo de 20 de mayo de 1997, que cita otras muchas: la sustitución de la persona del deudor en las relaciones contractuales o asunción de deuda, tanto en la modalidad del convenio entre los deudores como en la de expromisión (convenio entre el acreedor y el nuevo deudor que libere al primitivo), exige en todo caso para su eficacia, no el conocimiento, sino el consentimiento expreso o tácito del acreedor, conforme al artículo 1205 del Código Civil, sin cuya concurrencia no puede producirse la liberación del primitivo deudor. La novación nunca se presume ni puede inferirse de meras deducciones o conjeturas, sino que la voluntad de novar debe constar siempre de modo inequívoco, bien por manifestarse con claridad de forma expresa, bien por inducirse de actos de significación concluyente, sin que de ningún modo sea suficiente el simple conocimiento de la sustitución (sentencias del Tribunal Supremo de 10 de mayo de 1979, 23 de mayo de 1980, 16 de febrero de 1983, 28 de marzo de 1985, 10 de julio de 1986 y 17 de febrero de 1987).

Sobre el régimen de responsabilidad, en relación con la responsabilidad del socio por deudas de la agrupación (pagarés emitidos tras su baja pero antes de la inscripción y la publicación de la misma en el Boletín Oficial del Registro Mercantil), la sentencia del Tribunal Supremo (Sala de lo Civil, Sección 1ª) núm. 424/2006, de 4 de mayo, establece, en relación con una cláusula estatutaria según la cual «los socios responderán personal, solidaria e ilimitadamente de las deudas de cualquier clase contraídas por la Agrupación, en la proporción que corresponda por su participación», que la interpretación de la recurrente (responder solo en el porcentaje de su participación) es insostenible: primero, porque entonces carecería de sentido la solidaridad que inequívocamente establece el propio artículo de los estatutos; y segundo, porque la referencia proporcional a la participación de cada socio tiene que entenderse hecha a la relación interna entre estos, para el caso de que uno o varios acabasen pagando la deuda por entero y formularan contra los demás la reclamación que contempla el párrafo segundo del art. 1145 del Código Civil, teniendo pleno sentido la precisión estatutaria a la vista de lo que sobre distribución de pérdidas y ganancias establece el art. 21 de la Ley 12/1991 (reparto en la proporción prevista en la escritura o, en su defecto, por partes iguales), así como la jurisprudencia que, distinguiendo en la obligación solidaria las relaciones externas con el acreedor de las relaciones internas entre codeudores, combina el párrafo segundo del art. 1145 con el art. 1138 del Código Civil para presumir que la deuda se divide entre los deudores por partes iguales salvo que resulte claramente otra cosa (SSTS de 26 de octubre de 2002, 11 de marzo de 2002, 16 de julio de 2001 y 4 de enero de 1999, entre otras). Dicha proporción es aplicable solo a las relaciones internas entre los socios, no oponible al acreedor, y es plenamente compatible con el régimen de responsabilidad establecido en el art. 5 de la Ley 12/1991.

En cuanto al capital social, puede constituirse una A.I.E. sin capital social, pero se trata de una posibilidad improbable puesto que siempre existen gastos de notaría, registro, impuestos, etc., en el acto constitutivo que implican la existencia de un capital social necesario. No obstante, cabe la posibilidad de que los socios realicen aportaciones a la agrupación a fin de dotarla de fondos suficientes, sin que tales entregas tengan la consideración de capital social, o bien que sea la propia A.I.E. quien solicite un crédito para obtener un capital social garantizado con la responsabilidad de los socios o la prestación de una fianza por los mismos.


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

ESTATUTOS

TÍTULO I: CONSTITUCIÓN, PERSONALIDAD, DOMICILIO, DURACIÓN, OBJETO Y FINES

Artículo 1.- Constitución

La Agrupación se constituye al amparo de la Ley 12/1991, de 29 de abril, con la denominación «[DENOMINACIÓN SOCIAL], A.I.E.». Se regirá, además de por dicha ley, por los presentes estatutos y por todas aquellas disposiciones legales o reglamentarias que resulten aplicables.

Artículo 2.- Personalidad

La Agrupación goza de personalidad jurídica y carácter mercantil para el cumplimiento de sus fines, con arreglo a la ley por la que se rige.

Artículo 3.- Domicilio

El domicilio de la Agrupación se halla situado en [LOCALIDAD], calle [DOMICILIO], número [Nº], por ser este el lugar en el que radican su efectiva dirección y administración.

Artículo 4.- Duración

La Agrupación tendrá una duración de carácter indefinido, dándose comienzo a sus operaciones el día siguiente al del otorgamiento de la escritura de constitución, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Agrupación en momentos anteriores al de su inscripción en el Registro Mercantil.

Su disolución se regulará por los presentes estatutos y la ley vigente.

Artículo 5.- Objeto

La Agrupación no tiene ánimo de lucro para sí misma, planteándose como objetivo de base facilitar el desarrollo y mejorar los resultados de sus socios, mediante el desarrollo de los fines para los que se constituye.

Artículo 6.- Fines

Los fines generales de la Agrupación de Interés Económico son:

a) Mejorar la competitividad empresarial y contribuir al desarrollo económico y social de [LOCALIDAD O TERRITORIO], mejorando los resultados e imagen de nuestras empresas y fomentando a la vez el respeto y progreso de nuestro entorno y de nuestra comunidad.

b) Generar sinergias y favorecer la colaboración entre las empresas y entidades de la Agrupación a través del fomento de la relación y el conocimiento mutuo entre los socios.

c) Facilitar la convergencia de las acciones de los agentes económicos, sociales y entidades locales en la coordinación y gestión de iniciativas comunitarias o programas estatales y/o autonómicos.

d) Representar a la industria de [LOCALIDAD O TERRITORIO] en aquellos proyectos en los que se precise una cohesión para la consecución de objetivos precisos.

e) Acercar el mundo empresarial a las instituciones y a los ciudadanos de [LOCALIDAD O TERRITORIO], con el fin de recoger las diferentes inquietudes que le surjan en el desarrollo de su actividad.

f) Fomentar la mejora de la gestión de la calidad de las empresas asociadas.

g) Fomentar el uso y la transferencia de las nuevas tecnologías y los medios de comunicación y promocionar los productos y servicios basados en las TIC en sus aspectos de desarrollo tecnológico, económico, comercial, formativo, de colaboración mutua y de cooperación.

h) Crear, promocionar y promover una imagen de marca colectiva.

i) Establecer relaciones de colaboración con entidades oficiales y privadas nacionales y extranjeras inspiradas en finalidades similares a las de la Agrupación.

j) Fomentar entre las empresas asociadas el concepto de Responsabilidad Social Corporativa, siendo este un término más amplio que constituye un compromiso continuo de la empresa con la ética en su actuación y en su contribución al desarrollo económico, enfocado hacia el respeto y el progreso de su propio personal, su comunidad y de la sociedad en general.

k) Organizar encuentros empresariales, seminarios y conferencias de muy diversa índole, pudiendo distinguirse encuentros sectoriales, dirigidos al público empresarial en general, y otros.

l) En general, la realización de cuantas funciones se consideren necesarias o convenientes y redunden en beneficio de sus miembros, subordinando en todo momento los intereses particulares a los comunes y generales.

TÍTULO II: DE LOS MIEMBROS DE LA AGRUPACIÓN DE INTERÉS ECONÓMICO

Artículo 7.- Asociados

Podrán pertenecer de pleno derecho a la A.I.E. aquellas personas físicas o jurídicas que lo soliciten y desempeñen actividades empresariales, agrícolas o artesanales, así como quienes ejerzan profesiones liberales, con domicilio social en el municipio de [LOCALIDAD].

Artículo 8.- Régimen de responsabilidad

Los miembros de la Agrupación responderán solidaria e ilimitadamente por las deudas de aquella, salvo que, con carácter interno, haya un acuerdo con un tercero que excluya a uno o varios miembros de una deuda determinada y sin perjuicio de los acuerdos internos que se adopten.

La responsabilidad de los miembros es subsidiaria de la de la Agrupación, adquiriendo valor en el caso en que, tras haber reclamado el o los acreedores el pago correspondiente a la Agrupación, esta no responda. En este sentido, los miembros acuerdan que las deudas de las que hubiere respondido solidariamente uno o varios de ellos serán repetidas y asumidas por el conjunto de los socios, en proporción a la participación de cada uno de ellos en el capital social.

No obstante, un nuevo miembro, cualquiera que sea la causa de su ingreso en la Agrupación, puede ser exonerado de las deudas contraídas anteriormente a su admisión por una cláusula en el contrato o por el mismo acuerdo de su admisión. Para que sea oponible a terceros, esta cláusula debe ser publicada en el registro pertinente.

Hasta la finalización de la liquidación de la Agrupación, los acreedores no pueden pretender el pago de las deudas de la Agrupación por uno de sus miembros hasta pasado un mes desde el requerimiento de pago dirigido a esta por acto extrajudicial y sin ejecución durante dicho plazo.

Los miembros de la Agrupación contribuirán al pago de la diferencia entre gastos e ingresos, en su caso, en proporción a su participación en el capital social.

Artículo 9.- Derechos y obligaciones de los miembros

Los miembros asumen desde un primer momento los resultados positivos o negativos de la Agrupación, lo mismo que el saldo de la liquidación.

La titularidad de una cuota social concede a los miembros la condición de tales y les atribuye los correspondientes derechos reconocidos en estos estatutos, entre otros:

a) Derecho a formar parte de la Asamblea de la Agrupación y a disponer de voto.

b) Derecho a proponer un representante, persona física, para ocupar el cargo de administrador, en la forma colegiada o individual que acuerde constituir la Agrupación.

c) Instar la realización de la consulta de los miembros para adoptar cualquier decisión.

d) Obtener de los administradores información sobre los asuntos de la Agrupación.

e) Conocer y examinar el estado de la administración y de la contabilidad y formular las reclamaciones u observaciones que creyeren convenientes al interés común.

f) Asistir y participar en cuantas reuniones sean legalmente convocadas, emitiendo su voto libremente.

g) Disfrutar de la asistencia y los servicios de la Agrupación.

h) Participar en el reparto de los beneficios que se obtengan, en proporción a su participación en el capital social.

i) Cesar o dimitir como miembro de la Agrupación.

Artículo 10.- Intransmisibilidad de los derechos

Ningún socio podrá transmitir a otra persona, ni siquiera aunque esta ya sea socio, el interés o cuota de participación que tenga en la A.I.E.

Artículo 11.- Ingreso de nuevos miembros

La Agrupación puede admitir nuevos miembros, siempre y cuando reúnan las condiciones exigidas en los presentes estatutos. A estos efectos, los nuevos miembros deberán acreditar documentalmente el cumplimiento de dichas condiciones.

La decisión de admitir nuevos miembros será adoptada por la unanimidad de los miembros de la Agrupación. En el caso de ser rechazado el ingreso, este no tiene por qué ser fundado o motivado.

El ingreso de un nuevo miembro estará subordinado al pago de un canon de entrada fijado en su admisión.

Los nuevos miembros podrán ser exonerados del pago de las deudas originadas con anterioridad a su entrada, si así se establece en el acuerdo de admisión.

Artículo 12.- Dimisión y retiro

Cualquier miembro, mediante un aviso por carta certificada con acuse de recibo dirigido a los administradores con al menos tres meses de antelación, puede dimitir y retirarse de la Agrupación en cualquier momento, con el acuerdo por mayoría de la Asamblea General y con la condición de haber cumplido todas sus obligaciones.

La dimisión entrará en vigor a partir de su inscripción en el registro pertinente, quedando comprometido de manera ilimitada y solidaria con respecto a terceros sobre las deudas originadas por la Agrupación antes de la publicación de su dimisión, durante el plazo de cinco años, dentro de los cuales los acreedores podrán ejercitar las acciones correspondientes contra su persona, salvo que haya un convenio con los acreedores según las condiciones previstas en los presentes estatutos. Todo ello sin perjuicio del derecho de repetición y de la obligación solidaria de los miembros de reembolsarle la suma que hubiera pagado por las deudas contraídas después de la fecha en la que surte efecto su dimisión y antes de la publicación de su dimisión en el registro pertinente.

El miembro dimisionario tiene derecho al reembolso de la proporción de sus participaciones en el excedente del activo neto de la Agrupación.

El valor de los derechos correspondientes al miembro dimisionario o de las obligaciones que le conciernen será determinado sobre la base del patrimonio de la Agrupación existente el día en el cual surta efecto su dimisión. Se fijará de común acuerdo entre las partes y, en su defecto, se designará un experto según las condiciones previstas por la ley.

No obstante, en el caso en el que el desembolso pudiera cargar de deudas la tesorería de la Agrupación, este podrá ser aplazado mediante el pago de un interés al tipo oficial, según las condiciones fijadas por los administradores, sin que este aplazamiento pueda exceder de un período de dos años.

Artículo 13.- Pérdida de la cualidad de miembro

Cualquier miembro puede dejar de formar parte y es considerado dimisionario de oficio:

a) Desde su fallecimiento o disolución.

b) Por cese en el ejercicio de la actividad económica a la cual se vincula la practicada por la Agrupación en el marco de su objeto.

c) Por la declaración de concurso o la apertura de su liquidación; por el cese total o parcial de la actividad de la empresa; por la prohibición de ejercer una profesión de comerciante; por la prohibición de dirigir, administrar o controlar una empresa comercial, sin importar la forma de esta, o una persona jurídica de derecho privado no comerciante; o por una medida de incapacidad .

En caso de disolución de una persona jurídica, los sucesores de esta pueden solicitar su admisión en calidad de nuevos miembros. En este caso, esta nueva personalidad se subroga en los derechos y obligaciones de la antigua.

Desde el momento en el que un miembro deja de formar parte de la Agrupación, el Consejo de Administración debe notificar esta situación a los otros miembros y constatarla por decisión del órgano colegiado de miembros, adoptada por medio de acuerdo mayoritario simple.

Artículo 14.- Exclusión de miembros

Se reputan causas de exclusión de uno o varios miembros las siguientes:

a) El incumplimiento grave y reiterado de sus obligaciones tras un plazo de tres meses concedido mediante un aviso, por carta certificada con acuse de recibo, enviado por el Consejo de Administración para el cumplimiento de las obligaciones incumplidas.

b) La provocación de graves perturbaciones en el funcionamiento de la Agrupación.

c) Si se trata de una sociedad, en el caso en el que nuevos accionistas o asociados tuvieran o consiguieran en un futuro tener una participación superior al 50 % del capital o de los derechos de voto, sin que el Consejo de Administración hubiese sido previamente informado y sin que los demás miembros de la Agrupación hubiesen dado su consentimiento unánime.

El miembro excluido sigue comprometido al igual que el miembro dimisionario. Tiene derecho al reembolso de las mismas cantidades y está sujeto a las mismas obligaciones.

No obstante, si el miembro ha sido excluido por incumplir sus deberes, deberá indemnizar a la Agrupación del perjuicio causado por sus faltas, y la indemnización se compensará en el importe adeudado con la cantidad a reembolsar a la que pueda tener derecho.

La exclusión deberá ser adoptada por acuerdo unánime del resto de miembros. Si no se lograse dicho acuerdo y se considerase que existe causa de exclusión justificada, a petición conjunta de la mayoría de dos tercios de los demás miembros acordada en Asamblea General y formalizada mediante demanda judicial ante el Tribunal competente, este deberá dictar resolución judicial estimatoria o desestimatoria sobre la pretensión de exclusión.

Artículo 15.- Continuación de la Agrupación

La Agrupación subsistirá plenamente entre los miembros restantes a pesar de la dimisión, la exclusión o la pérdida de la condición de miembro de algún miembro, siempre y cuando ello no presente una circunstancia de disolución de la Agrupación.

TÍTULO III: RÉGIMEN ECONÓMICO

Artículo 16.- Capital social

La A.I.E. se constituye con un capital social de [IMPORTE] euros, dividido en [NÚMERO] cuotas iguales de [IMPORTE] euros cada una de ellas.

Artículo 17.- Aportaciones

La Agrupación obtendrá los fondos para cubrir sus gastos por medio de aportaciones fijas en forma de cuotas periódicas idénticas.

Se establecerá un canon de entrada para nuevos miembros que entren a formar parte de la A.I.E. El órgano de administración realizará una revisión periódica para establecer el canon para los nuevos socios.

Artículo 18.- Recursos

Constituyen recursos económicos de la Agrupación:

a) La aportación inicial de los miembros.

b) Los productos de bienes y derechos que posea la Agrupación.

c) Las cuotas anuales establecidas.

d) Los ingresos obtenidos por la realización de las actividades propias.

e) Los ingresos obtenidos como consecuencia de la gestión de programas de colaboración con los poderes públicos y organismos internacionales.

f) Las subvenciones y donaciones y cualquier tipo de aportación que se conceda a la Agrupación por las Administraciones Públicas, entidades o particulares.

g) Los frutos de los bienes y derechos que por cualquier título adquiera la Agrupación.

La Agrupación no persigue ni perseguirá en ningún momento fines lucrativos para sí misma, planteándose como objetivo de base facilitar el desarrollo y mejorar los resultados de sus socios, mediante el desarrollo del objeto para el que se constituye.

Artículo 19.- Ejercicio social

El ejercicio social se computará por años naturales.

Por excepción, el primer ejercicio de la Agrupación se iniciará en la fecha de la firma del contrato de constitución y concluirá el treinta y uno de diciembre del mismo año.

Artículo 20.- Presupuesto de la Agrupación

En el momento de la elaboración del presupuesto, el Consejo de Administración lo someterá a la Asamblea. El presupuesto deberá ser aprobado por la mayoría de los miembros de la Asamblea.

Artículo 21.- Inventarios, balances y cuentas anuales

Todo lo relativo a inventarios, balances, contabilidad y cuentas anuales se ajustará a las prescripciones del derecho mercantil vigente.

Al cierre de cada ejercicio, las cuentas anuales serán formuladas por el Consejo de Administración, explicando el conjunto de gastos e ingresos decididos por la A.I.E.

Las cuentas anuales serán sometidas a la Asamblea General durante los seis meses siguientes al cierre del ejercicio. La aprobación de las cuentas por la Asamblea General deberá hacerse por unanimidad.

El Consejo de Administración llevará una contabilidad regular, conforme a la ley, y constantemente puesta al día en cuanto a los ingresos y gastos de la Agrupación.

Al cierre de cada ejercicio, el Consejo de Administración redactará el inventario, la cuenta de resultados y el balance de la Agrupación.

Artículo 22.- Distribución de pérdidas y beneficios

Los beneficios y pérdidas procedentes de las actividades de la Agrupación serán considerados como beneficios o pérdidas de los miembros y repartidos entre ellos, en su caso, en proporción a sus respectivas cuotas sociales, sin perjuicio de lo establecido en el artículo siguiente.

Artículo 23.- Reservas

La Asamblea de la Agrupación podrá acordar anualmente la dotación de reservas voluntarias derivadas de los resultados del ejercicio, en la cuantía y proporción que estime, para poder desarrollar el objeto social y sus actividades, aumentar el capital social o cubrir los gastos no amortizados.

Artículo 24.- Control de cuentas

El Consejo de Administración podrá nombrar una persona física o jurídica independiente encargada del control de cuentas, que será ejercido por un interventor de cuentas .

Tendrá la misión de verificar todas las cuentas de la Agrupación y puede, con este fin, en todo momento del año, operar las verificaciones o controles que juzgue oportunos.

Establecerá, para cada ejercicio, un informe en el que rendirá cuentas del cumplimiento de su mandato.

En ningún caso los auditores y expertos designados podrán ejercer funciones de gestión y control en el seno de una Agrupación concurrente.

TÍTULO IV: DE LA ADMINISTRACIÓN DE LA A.I.E.

Artículo 25.- Órganos de la Agrupación

La Agrupación será regida y gobernada por la Asamblea General de miembros y representada por un Consejo de Administración, con funciones de dirección y administración.

Artículo 26.- Asamblea General

La Asamblea General de la Agrupación estará constituida por el total de los miembros adherentes a la misma, que ostentarán el número de votos derivados del número de participaciones sociales que hayan suscrito. Los miembros estarán representados por sus representantes legales o por los mandatarios o apoderados específicamente designados a los efectos por medio del título necesario y suficiente.

Los miembros, constituidos en Asamblea debidamente convocada, decidirán, con los quórum de asistencia y votación que procedan, todos los asuntos propios de la competencia de aquella. Todos los miembros, incluso los disidentes y los que no hayan asistido, quedarán sometidos a los acuerdos de la Asamblea, sin perjuicio de lo previsto para el supuesto de separación de alguno de ellos.

Nombramiento de cargos

La Asamblea de miembros nombrará en su primera reunión un Presidente y un Vicepresidente de la Agrupación, quienes ostentarán asimismo estas funciones en el Consejo de Administración. Serán funciones del Presidente, y del Vicepresidente cuando actúe en su ausencia, las siguientes:

a) Formar la lista de asistentes y, a la vista del quórum existente, declarar, si procede, la constitución de la Asamblea, en los casos en que esta se reúna.

b) Autorizar la asistencia de determinadas personas a la reunión.

c) Dirigir los debates.

d) Aprobar el acta.

e) Levantar la sesión.

Los cargos de Presidente y Vicepresidente de la Asamblea General se establecen para una duración de tres años, renovables en su caso.

El secretario de la Asamblea General será designado por el Presidente en el propio acto de esta.

Competencias de la Asamblea

La Asamblea General es el órgano de máxima decisión.

Está capacitada para adoptar cualquier decisión en relación con la realización del objeto de la Agrupación y, particularmente, aprueba las cuentas, el presupuesto, la memoria y el programa de actuación anual. Además, establece las reglas de funcionamiento.

Convocatoria

Los miembros podrán deliberar sobre los asuntos de la Agrupación en Asamblea General presencial.

La Asamblea de miembros deberá ser convocada por el Consejo de Administración de la Agrupación, por propia iniciativa o a instancia de un número de miembros que representen al menos un 10 % del capital social de la Agrupación. En este último caso, la convocatoria habrá de practicarse en el plazo de treinta días.

La convocatoria se realizará por medio de carta certificada con acuse de recibo enviada por el Presidente de la Agrupación a los miembros con al menos quince días de antelación a la fecha fijada para la reunión, expresándose en la notificación de la convocatoria la fecha, lugar y hora de la reunión y todos los asuntos que se han de tratar. La Asamblea quedará válidamente constituida cuando los socios, presentes o representados, representen [PORCENTAJE] % del capital social.

No obstante, para la adopción de los acuerdos que necesiten la adopción del acuerdo por unanimidad y que estén así reflejados en los presentes estatutos y, especialmente, en su artículo 27, se requerirá la concurrencia de la totalidad de los socios.

No obstante, la Asamblea estará convocada y quedará válidamente constituida para tratar cualquier asunto de su competencia, siempre que estén presentes, o debidamente representados, todos los miembros y los asistentes acepten por unanimidad la celebración de la Asamblea.

Los miembros deben deliberar al menos una vez al año en sesión ordinaria, en los seis meses siguientes al cierre del ejercicio, para aprobar o rechazar las cuentas de este ejercicio. Además, los miembros pueden adoptar otras decisiones colegiales en cualquier época del año, en sesiones extraordinarias, mediando las reglas de convocatoria anteriormente señaladas.

La Asamblea se celebrará en la localidad donde la Agrupación tenga su domicilio. Esto no obstante, y tratándose de Asambleas Universales, serán válidos los acuerdos tomados, cualquiera que sea el lugar en el que la Asamblea se haya celebrado.

Artículo 27.- Adopción de acuerdos

Todas las decisiones que excedan de los poderes del Consejo de Administración serán tomadas por la mayoría de los miembros de la Asamblea General, sin perjuicio de lo establecido en el presente artículo y del supuesto regulado en el artículo 14 de los presentes estatutos.

Deberán aprobarse por unanimidad de todos los miembros de la Agrupación los acuerdos de modificación del contrato de constitución que se refieran a las siguientes materias:

a) Objeto de la Agrupación.

b) Número de votos atribuidos a cada miembro.

c) Condiciones para la adopción de acuerdos.

d) Duración prevista para la Agrupación.

e) Cuota de contribución de cada uno de los miembros o de alguno de ellos a la financiación de la Agrupación.

f) Modificar cualquier otra obligación de un miembro, si en los presentes estatutos no se ha establecido otra cosa.

Asimismo, será necesario el acuerdo unánime de todos los miembros para la admisión de nuevos miembros, la transmisión de participaciones sociales, el traslado del domicilio, la disolución y la transformación de la Agrupación, la aprobación de las cuentas anuales, así como para los demás supuestos exigidos por el Reglamento (CEE) 2137/85 que no hayan sido reflejados en los presentes estatutos y los supuestos específicamente regulados en estos estatutos que no se encuentren reflejados en el presente artículo.

Las decisiones colegiales serán extendidas en actas y recogidas en un libro.

Las actas de las sesiones serán firmadas por el Presidente de la sesión y por la Secretaría.

Las actas de las decisiones resultantes de las contestaciones escritas serán firmadas por el Presidente del Consejo de Administración y la Secretaría del Consejo y deben mencionar el uso de este procedimiento. Además, en cada acta se adjuntará la respuesta de cada uno de los miembros.

Las copias o extractos de estas actas serán firmados por el Presidente o por el liquidador, si la Agrupación se encuentra en liquidación.

Artículo 28.- Consejo de Administración

Se crea un Consejo de Administración, como órgano colegiado encargado de gestionar o administrar la Agrupación, formado por un mínimo de [NÚMERO MÍNIMO] y un máximo de [NÚMERO MÁXIMO] miembros.

El Consejo de Administración y sus miembros deberán ejercitar su cargo con la diligencia de un ordenado empresario y de un representante leal y guardarán secreto sobre los datos confidenciales de la Agrupación, aun después de cesar en sus funciones.

Los miembros del Consejo de Administración responderán solidariamente de los daños causados a la Agrupación, salvo que prueben haber actuado conforme a la diligencia exigida en el apartado anterior.

Remuneración

El ejercicio del mandato de los miembros del Consejo de Administración no da lugar a remuneración, salvo acuerdo en contrario adoptado por la Asamblea General de la Agrupación.

Los miembros del Consejo de Administración son nombrados por la Asamblea General por un plazo de tres años, pudiendo ser reelegidos una o más veces por períodos de igual duración máxima, y podrán asimismo ser revocados por acuerdo de la misma. Del mismo modo, podrán dimitir de sus funciones, mediando aviso al Consejo de Administración con una antelación de tres meses acerca de esta decisión.

Atribuciones y competencias del Consejo de Administración

El Consejo de Administración ejercerá los actos de administración y dominio relativos a los negocios y bienes sociales de la Agrupación y todos los de dirección y gobierno necesarios para su marcha y desarrollo, exceptuándose únicamente aquellos expresamente reservados por los estatutos a la Asamblea de miembros. Por consiguiente, estará revestido de las más amplias facultades, sin limitación ni reserva alguna, para actuar en nombre de la Agrupación y representarla, tanto contractual como extracontractualmente, en el orden judicial y extrajudicial y frente a toda clase de personas y entidades públicas y privadas, autoridades, organismos, funcionarios y tribunales de toda índole, así como para otorgar los documentos públicos y privados que sean precisos y, en general, realizar cuanto sea útil y conveniente a la Agrupación.

En el desarrollo de sus funciones deberá siempre velar por el respeto de las normas de funcionamiento establecidas en estos estatutos y tener como objetivo el cumplimiento de los objetivos de la Agrupación.

El Consejo de Administración compromete a la Agrupación ante terceros cuando actúa en nombre de esta, aun cuando sus actos no estén en relación con el objeto social de la Agrupación, a menos que la Agrupación pruebe que el tercero sabía que el acto excedía los límites del objeto social de la Agrupación, o no podía ignorarlo, teniendo en cuenta las circunstancias, y excluyendo que la simple publicación de dicho objeto baste para constituir esta prueba.

Nombramiento de cargos

Corresponden al Presidente y Vicepresidente de la Asamblea de la Agrupación los cargos de Presidente y Vicepresidente del Consejo de Administración, asumiendo las siguientes funciones y competencias:

a) Convocatoria del Consejo.

b) Gestión de las reuniones del Consejo.

c) Actuar en nombre y representación del Consejo y poseer el uso de la firma social para ejecutar los acuerdos del Consejo.

d) Dar el visto bueno a las certificaciones de los acuerdos que hayan de emitirse.

e) Facilitar el ejercicio del derecho de información por parte de los socios.

f) Coordinar la actividad de los miembros del Consejo.

Acuerdos y reuniones del Consejo de Administración

Los acuerdos del Consejo de Administración de la Agrupación deberán ser adoptados por mayoría absoluta de los miembros concurrentes a sus reuniones, resultando necesaria la presencia o la debida representación de la mitad más uno de los miembros del Consejo para su válida constitución. A estos efectos, cada miembro del Consejo de Administración poseerá un voto para la adopción de acuerdos.

El Consejo deberá ser convocado por su Presidente, por propia iniciativa o a instancia de cualquier miembro del Consejo de Administración o de un número de miembros que represente al menos el 10 % del capital social de la Agrupación. En este último caso, la convocatoria habrá de practicarse en el plazo de quince días.

La convocatoria se realizará por medio de carta certificada con acuse de recibo enviada por el Presidente del Consejo a los miembros del Consejo con al menos siete días de antelación a la fecha fijada para la reunión, expresándose en la notificación de la convocatoria la fecha, lugar y hora de la reunión y todos los asuntos que se han de tratar.

No obstante, el Consejo estará convocado y quedará válidamente constituido para tratar cualquier asunto de su competencia, siempre que estén presentes, o debidamente representados, todos sus miembros y los asistentes acepten por unanimidad la celebración del Consejo.

El Consejo realizará reuniones ordinarias cada [NÚMERO] meses y las sesiones extraordinarias que considere oportunas, atendiendo a los requisitos de convocatoria anteriormente establecidos. De todos los acuerdos adoptados se elevarán las oportunas actas, firmadas por el Presidente del Consejo y por quien desarrolle las funciones de Secretaría en el Consejo, que será nombrado por el mismo Consejo para dichas funciones entre sus miembros, y serán recogidas en un libro de actas. Se facilitará asimismo a los miembros de la Agrupación, con antelación a las reuniones del Consejo de Administración, la convocatoria correspondiente por si quisieran asistir a las mismas y posteriormente se les dará cuenta del resultado de los acuerdos adoptados.

TÍTULO V: DISOLUCIÓN Y LIQUIDACIÓN

Artículo 29.- Disolución

La Asamblea General de la Agrupación puede disolver la Agrupación por medio de acuerdo unánime de sus miembros.

Puede igualmente pronunciar la disolución por justo motivo.

Artículo 30.- Liquidación

La Agrupación está en liquidación desde el momento en que su disolución ha sido pronunciada o constatada, cualquiera que sea la causa.

Todos los actos y documentos destinados a terceros deben indicar legiblemente, con todas las menciones obligatorias, que la Agrupación se encuentra en liquidación, según las condiciones previstas por el reglamento.

La personalidad jurídica de la Agrupación subsiste durante el proceso de la liquidación.

La liquidación será efectuada por el Consejo de Administración, a menos que la Asamblea General, que conserva todos sus poderes, prefiera confiar esta misión a uno o varios liquidadores. En el curso de la liquidación, la Agrupación puede nombrar o revocar un nuevo auditor. Ella fija la remuneración de los interesados, así como la duración de sus funciones.

Después de la extinción del pasivo, el producto neto de la liquidación se repartirá entre los miembros en proporción a sus respectivas cuotas sociales.

En caso de insuficiencia del activo para cubrir la integridad del pasivo, el déficit será saldado por los miembros en la misma proporción.

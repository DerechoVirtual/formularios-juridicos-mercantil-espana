---
name: contenido-folleto-informativo-oferta-venta-acciones-mer-0666
description: "Contenido del folleto informativo de una oferta de venta de acciones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contenido del folleto informativo de una oferta de venta de acciones

> Formulario **MER-0666** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contenido del folleto informativo de una oferta de venta de acciones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contenido del folleto informativo de una oferta de venta de acciones” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:contenido-folleto-informativo-oferta-venta-acciones-mer-0666`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- El modelo no tiene campos marcados: Claude te preguntará lo que necesite según el caso.

## Normas que cita el formulario

- art. 1 Real Decreto 1066/2007
- art. 29 Real Decreto 1066/2007
- art. 47 Real Decreto 1066/2007
- art. 26 Real Decreto 1066/2007

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

CONTENIDO DEL FOLLETO

Índice y relación de documentos complementarios

Introducción y advertencias si la operación lo requiere

CAPÍTULO I-PERSONAS RESPONSABLES DEL FOLLETO

a) Nombre y cargo de las personas responsables del folleto y en su caso, de las partes concretas sobre las que asumen la responsabilidad.

b) Declaración de los responsables asegurando que los datos e informaciones comprendidos en el folleto son verídicos, no se incluyen datos o informaciones que puedan inducir a error y no existen omisiones susceptibles de alterar su contenido.

Acuerdos, ámbito y legislación aplicables.

a) Acuerdos y decisiones del oferente para la formulación de la oferta y apoderamiento a las personas responsables del folleto.

b) Ámbito de la oferta, legislación aplicable y autoridad competente con indicación detallada de las normas aplicables en función de lo dispuesto en el artículo 1 del Real Decreto 1066/2007, de 27 de julio.

c) Mercados en los que se formulará la oferta.

d) Indicación de la legislación nacional que regirá los contratos celebrados entre el oferente y los titulares de valores de la sociedad afectada como consecuencia de la oferta, y de los órganos jurisdiccionales competentes.

Información sobre la sociedad afectada.

a) Denominación social y comercial. Domicilio social y dirección.

b) Composición del capital social. Otros valores que puedan dar derecho a la adquisición o suscripción de acciones. Derechos de voto de los valores. Mercados en los que se encuentran admitidas a negociación las acciones y los demás valores cotizados.

c) Estructura de los órganos de administración, dirección y control con indicación de sus respectivos cargos y de las acciones y los demás valores de la sociedad afectada pertenecientes a los miembros de dichos órganos.

d) Estructura accionarial de la sociedad afectada y pactos para sociales.

e) Limitaciones al derecho de voto y restricciones de acceso a los órganos de administración contempladas en los estatutos sociales.

f) Acuerdos relativos a la aplicación de las medidas de neutralización y compensaciones previstas por la sociedad afectada.

Información sobre el oferente y su grupo.

a) Personalidad jurídica, denominación social y comercial, domicilio social, dirección, fecha de constitución, período de actividad y objeto social. Si se trata de una persona física, nombre y domicilio.

b) Composición del capital social. Otros valores que puedan dar derecho a la adquisición o suscripción de acciones. Derechos de voto de los valores. Mercados en los que se encuentran admitidas a negociación, en su caso, las acciones y los demás valores cotizados.

c) Estructura de los órganos de administración, dirección y control con indicación de sus respectivos cargos y de las acciones y los demás valores de la sociedad oferente pertenecientes a los miembros de dichos órganos.

d) Identidad de los principales accionistas o socios del oferente con indicación de los valores, derechos de voto y personas que ejercen el control individualmente o de forma concertada. Cuando el oferente no esté controlado por ninguna persona, se indicará expresamente.

e) Identidad de las personas físicas o jurídicas que actúen en concierto con el oferente y descripción de los pactos u otras relaciones que originan la actuación concertada. Si no existe ninguna persona que actúe concertadamente con el oferente, se indicará expresamente.

f) Limitaciones al derecho de voto y restricciones de acceso a los órganos de administración contempladas en los estatutos sociales.

g) Acuerdos relativos a la aplicación de las medidas de neutralización o equivalentes y compensaciones previstas por la sociedad oferente.

h) Entidades que pertenezcan al mismo grupo que el oferente, con indicación de la estructura del grupo. En su defecto, declaración negativa.

Acuerdos sobre la oferta y la sociedad afectada.

a) Descripción completa de todos los acuerdos o pactos de cualquier naturaleza entre el oferente y los accionistas y miembros de los órganos de administración, dirección y control de la sociedad afectada, y ventajas reservadas por el oferente a dichos miembros. En su defecto, declaración negativa.

Si la declaración del párrafo anterior no fuese negativa, valores y derechos de voto de la sociedad oferente pertenecientes a los miembros de los órganos de administración, dirección y control de la sociedad afectada y a los accionistas integrantes del acuerdo.

b) Miembros pertenecientes a los órganos de administración, dirección y control de la sociedad afectada y de la sociedad oferente simultáneamente.

c) Acciones y otros valores que puedan dar derecho a su adquisición o suscripción de la sociedad oferente pertenecientes, directa o indirectamente, a la sociedad afectada, con indicación de los derechos de voto y declaración negativa en su defecto.

Valores de la sociedad afectada pertenecientes al oferente.

a) Acciones y otros valores que den derecho a su suscripción o adquisición de la sociedad afectada que pertenezcan, directa o indirectamente, al oferente, a sus administradores, a los administradores de las sociedades controladas pertenecientes a su grupo, a sus accionistas o socios de control, y a otras personas que actúen por cuenta del oferente o concertadamente con él, con indicación de los derechos de voto correspondientes.

b) Autocartera de la sociedad afectada. Operaciones con valores de la sociedad afectada.

a) Tipo, fecha y precio o contraprestación de las operaciones, al contado o a plazo, realizadas por el oferente y quienes actúen concertadamente con él durante los últimos 12 meses anteriores al anuncio previo de la oferta.

Con idéntico detalle, se informará de las operaciones referidas al período transcurrido desde el anuncio previo de la oferta hasta su presentación y de las realizadas posteriormente, hasta la autorización.

Si existiera algún acuerdo sobre la oferta o la sociedad afectada con sus accionistas o administradores, la información de este apartado se extenderá a todas las personas integrantes del acuerdo.

Si no existiera ninguna operación, se indicará expresamente.

b) De existir algún acuerdo con la sociedad afectada, se indicarán también las operaciones de auto cartera de esta última en el período señalado en la letra a) anterior.

Actividad y situación económico-financiera del oferente.

a) Información sobre la actividad y situación económico-financiera de la sociedad oferente correspondiente al último ejercicio cerrado y auditado, con identificación de su patrimonio, cifra de negocios, activos totales, endeudamiento financiero neto y resultados, y referencia expresa a cualquier salvedad o indicación relevante que conste en los informes de auditoría.

Cuando la sociedad oferente forme parte de un grupo, la citada información deberá referirse no sólo a la sociedad oferente, sino también a los estados financieros del grupo consolidado.

En el caso de que la sociedad oferente no tenga actividad o haya sido creada para la realización de la oferta, las informaciones de este párrafo deberán referirse a sus accionistas o socios de control.

b) Se incluirán también los datos anteriormente señalados, referidos al período posterior al cierre de las últimas cuentas anuales en la medida que se hayan hecho públicos.

CAPÍTULO II-VALORES A LOS QUE SE DIRIGE LA OFERTA

a) Número y descripción de los valores o clases de valores a los que se dirige la oferta y derechos de voto correspondientes.

b) Número y descripción de los valores o clases de valores que hayan sido inmovilizados con el fin de impedir su transmisión por cualquier medio durante la oferta, derechos de voto correspondientes e identidad de sus titulares.

c) Número y descripción de los valores o clases de valores a los que se extiende de modo efectivo la oferta una vez deducidos los que hubieran sido inmovilizados y derechos de voto correspondientes, indicando, en su caso, el porcentaje o número máximo y mínimo de valores que el oferente se compromete a adquirir.

d) Distribución de los valores y respectivos derechos de voto entre los distintos oferentes, en su caso.

Contraprestación ofrecida.

a) Contraprestación ofrecida por cada valor o clase de valores y forma en que se hará efectiva.

Si la sociedad afectada ha anunciado algún dividendo cuyo pago se va a producir durante el plazo de aceptación de la oferta, deberá indicarse si el importe bruto de dicho dividendo será deducido o no de la contraprestación ofrecida.

b) Justificación de la contraprestación y método de valoración utilizado para determinar el precio equitativo cuando proceda.

c) Cuando la contraprestación consista total o parcialmente en canje por otros valores, se incluirá, además:

Información sobre las proporciones en que haya de producirse el canje.

Precio equivalente en efectivo que resulta de aplicar a la ecuación de canje la cotización media ponderada de los valores ofrecidos, correspondiente al trimestre anterior al anuncio previo de la oferta.

Informe de experto independiente que determine el precio en dinero de los valores ofrecidos en canje cuando se trate de valores a emitir por la propia sociedad oferente y su capital no esté total o parcialmente admitido a negociación en un mercado oficial español o en un mercado regulado de algún Estado miembro de la Unión Europea, o cuando se ofrezcan valores no admitidos a negociación en dichos mercados.

d) Compensación ofrecida a cambio de las medidas de neutralización que puedan resultar ineficaces como consecuencia de lo establecido en el artículo 29 del Real Decreto 1066/2007, de 27 de julio, especificando la forma en que se abonará la compensación y el método empleado para determinarla.

Condiciones a las que está sujeta la oferta.

a) Descripción de las condiciones a las que esté sujeta la oferta o declaración negativa si no existiera ninguna.

b) Limitaciones o restricciones, reglamentarias, propias o impuestas por terceros, que el oferente pueda tener para una posible renuncia a dichas condiciones en caso de que no se cumplieran.

c) Previsiones del oferente sobre la posible renuncia a las condiciones e impacto de dicha renuncia en la oferta, en su finalidad y en las demás previsiones contenidas en el folleto.

Garantías y financiación de la oferta.

a) Tipo de garantías constituidas por el oferente para la liquidación de la oferta, identidad de las entidades financieras con las que hayan sido constituidas e importe.

b) Fuentes de financiación de la oferta y principales características y condiciones de dicha financiación, incluyendo en caso de financiación ajena la identidad de los acreedores financieros y la previsión del oferente para atender el servicio financiero de la deuda.

c) Efectos de la financiación sobre la sociedad afectada. Si el oferente prevé que el pago de los intereses de la financiación de la oferta, su refinanciación o sus garantías dependerán del negocio de la sociedad afectada, deberá indicarse expresamente e incluirse una descripción detallada de los acuerdos de financiación. De lo contrario, deberá hacerse una declaración negativa.

CAPÍTULO III-PROCEDIMIENTO DE ACEPTACIÓN Y LIQUIDACIÓN

a) Plazo de aceptación de la oferta.

b) Formalidades que deben cumplir los destinatarios de la oferta para manifestar su aceptación, así como la forma y plazo en el que recibirán la contraprestación.

c) Gastos de aceptación y liquidación de la oferta que sean de cuenta de los destinatarios, o distribución de los mismos entre el oferente y aquéllos.

d) Plazos para la renuncia a las condiciones a las que, en su caso, esté sujeta la eficacia de la oferta.

e) Designación de las entidades o intermediarios financieros que actúen por cuenta del oferente en el procedimiento de aceptación y liquidación.

f) Formalidades que deben cumplir los titulares de los valores para solicitar la compra forzosa de los valores afectados por la oferta y elegir, en su caso, la naturaleza de la contraprestación en el caso de que se den las condiciones indicadas en el artículo 47 del Real Decreto 1066/2007, de 27 de julio.

CAPÍTULO IV -FINALIDAD DE LA OPERACIÓN

a) Finalidad perseguida con la adquisición.

b) Planes estratégicos e intenciones sobre las actividades futuras y la localización de los centros de actividad de la sociedad afectada y su grupo para un horizonte temporal mínimo de 12 meses.

c) Planes estratégicos e intenciones respecto al mantenimiento de los puestos de trabajo del personal y directivos de la sociedad afectada y su grupo, incluyendo cualquier cambio importante en las condiciones de trabajo para un horizonte temporal mínimo de 12 meses.

d) Planes relativos a la utilización o disposición de activos de la sociedad afectada;

variaciones previstas en su endeudamiento financiero neto.

e) Planes relativos a la emisión de valores de cualquier clase por la sociedad afectada y su grupo.

f) Reestructuraciones societarias de cualquier naturaleza previstas. g) Política de dividendos.

h) Planes sobre la estructura, composición y funcionamiento de los órganos de administración, dirección y control de la sociedad afectada y su grupo. Previsiones sobre la designación de miembros en dichos órganos por el oferente.

i) Previsiones relativas al mantenimiento o modificación de los estatutos de la sociedad afectada o de las entidades de su grupo.

j) Intenciones con respecto al mantenimiento de la cotización de los valores de la sociedad afectada o, en su caso, la exclusión y compromisos para la adopción, en los 6 meses siguientes a la liquidación de la oferta, de las medidas que permitan el mantenimiento o la exclusión en bolsa, en función de las intenciones manifestadas.

k) Intención de aplicar o no el derecho de venta forzosa previsto en el artículo 47 de este Real Decreto.

l) Intenciones relativas a la transmisión de valores de la sociedad afectada, indicando si existe algún acuerdo a este respecto con otras personas y los valores de la sociedad afectada que pertenecen, en su caso, a dichas personas.

m) En la medida en que la sociedad oferente se vea afectada por la oferta, deberán incluirse las informaciones a que se refieren los párrafos anteriores de este Capítulo referidas a la propia sociedad oferente y su grupo.

n) Cuando el oferente sea una sociedad cotizada deberá indicarse el impacto de la oferta y su financiación sobre sus principales magnitudes financieras.

CAPÍTULO V. AUTORIZACIONES Y OTRAS INFORMACIONES O DOCUMENTOS

a) Posibilidad o no de que el resultado de la oferta quede afectado por la Ley 15/2007, de Defensa de la Competencia, por el Reglamento (CE) núm. 139/2004 del Consejo de las Comunidades Europeas o por otras normas de defensa de la competencia y, en su caso, eventuales actuaciones que pretenda o deba iniciar el oferente, con indicación de sus posibles consecuencias de acuerdo con lo dispuesto en los artículos 26 y 33 del Real Decreto 1066/2007, de 27 de julio.

b) Detalle de las autorizaciones o verificaciones administrativas, distintas de la correspondiente a la Comisión Nacional del Mercado de Valores, obtenidas con carácter previo a la formulación de la oferta.

Si como consecuencia de la adquisición o transmisión de la titularidad o el control de los valores resultantes de la oferta, el oferente requiriese alguna autorización o verificación administrativa, que se encuentra pendiente de obtención o de solicitud, se informará de esta circunstancia, de las actuaciones que pretenda o deba iniciar y de los efectos previstos para el supuesto de incumplimiento o falta de obtención.

c) En las ofertas formuladas como permuta, el folleto de la oferta deberá contener información adicional equivalente a la del folleto informativo previsto en el Real Decreto 1310/2005, de 4 noviembre salvo que exista un documento de registro o folleto informativo del emisor de los valores entregados en canje, válido según lo dispuesto en los artículos 27, 30 y 31 de dicho Real Decreto.

d) Lugares donde podrá consultarse el folleto y los documentos que lo acompañan.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

---
name: contrato-venta-participaciones-sociedad-limitada-mer-0199
description: "Contrato de venta de participaciones de una sociedad limitada. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de venta de participaciones de una sociedad limitada

> Formulario **MER-0199** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de venta de participaciones de una sociedad limitada» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de venta de participaciones de una sociedad limitada” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:contrato-venta-participaciones-sociedad-limitada-mer-0199`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (10 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] Nº (7 veces)
- [ ] FECHA (5 veces)
- [ ] MES (4 veces)
- [ ] AÑO (3 veces)
- [ ] Nº DE PROTOCOLO (3 veces)
- [ ] NÚMERO (3 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] DÍA (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE DEL REPRESENTADO/A (2 veces)
- [ ] PLAZO (2 veces)
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] FOLIO
- [ ] HOJA
- [ ] LUGAR
- [ ] NIF
- [ ] Nº DE PARTICIPACIONES
- [ ] OTROS DATOS
- [ ] TOMO

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

En [LUGAR], a [DÍA] de [MES] de [AÑO].

REUNIDOS

De una parte:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

De otra:

D. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil, vecino de [LOCALIDAD], domiciliado en [DOMICILIO], con documento nacional de identidad número [NÚMERO]

INTERVIENEN

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA VENDEDORA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

D. [NOMBRE Y APELLIDOS], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], en lo sucesivo "LA COMPRADORA", en virtud de poder otorgado a su favor ante el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], poder que se halla debidamente inscrito en el Registro Mercantil de [LOCALIDAD] y vigente, según manifiesta.

Todas las partes, en el respectivo carácter con el que intervienen, se reconocen mutuamente la capacidad legal en Derecho necesaria para concertar el presente CONTRATO DE COMPRAVENTA DE PARTICIPACIONES, y a tal efecto, libremente y de común acuerdo,

EXPONEN

PRIMERO.- Que LA VENDEDORA es partícipe de la mercantil [DENOMINACIÓN SOCIAL] (nombre de la sociedad), sociedad de responsabilidad limitada con domicilio social en [LOCALIDAD], en la calle [CALLE], número [NÚMERO] (ciudad), (calle/avenida/plaza), número (número) y Número de Identificación Fiscal [NIF] (en lo sucesivo, "La Compañía").

Que LA COMPAÑÍA fue constituida mediante escritura pública autorizada por el Notario de [LOCALIDAD] D. [NOMBRE Y APELLIDOS], en fecha [FECHA], con el número de protocolo [Nº DE PROTOCOLO], inscrita en el Registro Mercantil de [LOCALIDAD] el [DÍA] (día) de [MES] (mes) de (año) en el tomo [TOMO], folio [FOLIO], hoja [HOJA], inscripción

Que LA VENDEDORA está interesada en vender las participaciones de la Compañía de las que es titular.

SEGUNDO.- Que LA COMPRADORA está interesada en comprar las participaciones de las cual es titular LA VENDEDORA.

TERCERO.- Que en virtud de las consideraciones precedentes, las Partes, libremente y de común acuerdo llevan a efecto el presenten contrato con arreglo a las siguientes:

CLÁUSULAS

Objeto

LA VENDEDORA vende y transmite a LA COMPRADORA, que compra y adquiere libres de cargas y gravámenes las participaciones de las que la primera es titular, esto es, [Nº DE PARTICIPACIONES] (número) participaciones, las señaladas con los números [Nº] (número) a la [Nº] (número), y números [Nº] (número) a la [Nº] (número), todas ellas inclusive, que están totalmente desembolsadas y que representan el % del capital social de la Compañía (en lo sucesivo, "Las Participaciones").

[ELEGIR UNA OPCIÓN: Precio y pago / Antes de la firma del contrato / No aplazado y efecutado después / Aplazado y efectuado después]

Transmisión de la titularidad

La transmisión de la titularidad de las Participaciones se efectuará en el momento de la firma del presente Contrato y conlleva la transmisión de todos los derechos políticos y económicos inherentes a las mismas.

Declaraciones y garantías

El capital social de La Compañía es de [IMPORTE] euros ( €) y está dividido en [Nº] (número de participaciones) participaciones de [IMPORTE] euros de valor nominal cada una, por lo que las Participaciones que se transmiten representan el % del capital de la Compañía a la fecha de la firma del presente Contrato.

LA VENDEDORA declara, en su calidad de partícipe de la Compañía, que se han cumplido todos los requisitos legales y aquellos previstos en los Estatutos Sociales en orden a la transmisión de las Participaciones.

Igualmente, LA VENDEDORA declara que no existen ningún litigio, procedimiento judicial, reclamación o inspección administrativa pendiente, y que no hay visos de contienda civil, mercantil, fiscal, administrativa, laboral o de cualquier otra índele.

Además, LA VENDEDORA manifiesta que las Participaciones objeto del presente Contrato le pertenecen en pleno dominio por justo y legítimo título y que las mismas libres y exentas de cualesquiera opciones, gravámenes, convenios, compromisos, reclamaciones, embargos, afectaciones o gravámenes, no existiendo deuda alguna en relación con las mismas que afecte a LA VENDEDORA, o que de cualquier forma pudieran influenciar o condicionar los derechos que LA COMPRADORA adquiere.

LA VENDEDORA se hace responsable de los daños o perjuicios que le ocasione a LA COMPRADORA los eventuales incumplimientos o excepciones a las manifestaciones y garantías vertidas en los párrafos precedentes.

Situación de la compañía

LA VENDEDORA declara que la Compañía está debidamente constituida y registrada de conformidad con la legislación aplicable.

La Compañía no se encuentra en situación legal de insolvencia y en el momento actual no existe indicio alguno que sostenga una eventual declaración de insolvencia.

La Compañía tiene capacidad para desarrollar su actual actividad, para ser propietaria y gestionar sus bienes, derechos y obligaciones. Los estatutos sociales actuales de la Compañía son los aprobados mediante acuerdo de la Junta General de socios de fecha [FECHA] (día) de [MES] (mes) de [AÑO] (año) [OTROS DATOS], estatutos que fueron elevados a públicos mediante escritura de fecha [FECHA] (día) de [MES] (mes) de [AÑO] (año) otorgada ante el Ilustre Notario de [LOCALIDAD] (lugar), D. incorporados como Anexo I.

La Compañía tiene todos los permisos, licencias, autorizaciones, aprobaciones preceptivos y no incumple ninguna ley o normativa urbanística, sobre medio ambiente o de cualquier otro tipo administrativo, y no se ha recibido notificación alguna sobre un eventual incumplimiento de las mismas.

Pacto de no concurrencia

Durante el plazo de [PLAZO] (meses/años) desde la conclusión del presente contrato, LA VENDEDORA se compromete a no realizar actividades por cuenta propia o ajena que de algún modo pudieran concurrir con la actividad desempeñada por la Compañía.

Durante la vigencia del presente paco LA VENDEDORA no podrá desempeñar, directa o indirectamente, y sin el consentimiento expreso de LA COMPRADORA cualquiera de las actividades que a continuación se describen:

- [ACTIVIDAD]

- [ACTIVIDAD]

El incumplimiento de este compromiso conllevará la obligación de indemnizar los daños y perjuicios causados.

Cláusula de confidencialidad

Cualquier información intercambiada con ocasión de la presente compraventa entre las partes será mantenida confidencial. La parte receptora de la información mantendrá la confidencialidad y evitará revelarla a toda persona que no sea empleado o subcontratante autorizado salvo que:

a) La parte receptora tenga evidencia que conoce previamente la información recibida;

b) La información recibida sea de dominio público;

c) La información recibida proceda de un tercero que no se encuentre bajo el deber de secreto;

La parte receptora se responsabilizará de que las personas que están a su cargo se sujeten a las limitaciones establecidas en esta cláusula.

Se entiende que cualquiera de las partes podrá revelar la información confidencial a sus asesores, contables y abogados siempre que se enmarque en el asesoramiento sobre asuntos relacionados con este acuerdo.

El incumplimiento de este compromiso conllevará la obligación de indemnizar los daños y perjuicios causados.

Resolución del contrato

El Contrato podrá resolverse por acuerdo de las Partes por escrito o por la voluntad de cualquiera de ellas cuando medie incumplimiento grave de las obligaciones pactadas. En este último caso, quien pretenda resolver el presente Contrato alegando el incumplimiento de la parte contraria deberá requerirle fehacientemente el cumplimiento de la obligación, otorgando a la parte incumplidora un plazo de [Nº] días para que pueda subsanar dicho incumplimiento.

Condición resolutoria por apartamiento de actividad

La compraventa que antecede queda condicionada por medio del establecimiento de la presente condición resolutoria a la falta de permanencia en el futuro en la prestación de servicios en la Compañía por parte de LA COMPRADORA, en cuyo caso procederá la resolución inmediata de la compraventa frente a LA VENDEDORA.

Elevación a escritura pública

A instancia de cualquiera de las partes y en el plazo de [PLAZO] a contar desde la conclusión del presente contrato el contrato deberá ser elevado a escritura pública e inscribirse en el Registro Mercantil.

Los gastos y derechos derivados de esta operación correrán a cargo de [ELEGIR: vendedora / compradora]

Gastos e impuestos

Todos los gastos e impuestos que se originen como consecuencia de la formalización, cumplimiento o extinción del presente contrato y de las obligaciones que de él se deriven serán de cargo de LA COMPRADORA.

Igualmente, los gastos judiciales que se ocasionen por incumplimiento del presente contrato serán por cuenta de la parte incumplidora, incluidos honorarios del Procurador y Abogado aunque sus intervenciones no fueran preceptivas.

[ELEGIR UNA OPCIÓN: Sumisión a tribunales / Sin cláusula penal / Con cláusula penal / — y además elegir: Sumisión a arbitraje / Sin cláusula penal / Con cláusula penal]

Notificaciones

Toda notificación que se efectúe entre las partes se hará por escrito y será entregada personalmente o de cualquier otra forma que certifique la recepción por la parte notificada en los respectivos domicilios indicados en el encabezamiento de este Contrato.

Cualquier cambio de domicilio de una de las partes deberá ser notificado a la otra de forma inmediata y por un medio que garantice la recepción del mensaje.

Generalidades

El presente contrato anula y reemplaza cualquier contrato o acuerdo anterior entre las partes con el mismo objeto y sólo podrá ser modificado por un nuevo acuerdo firmado por ambas partes.

Si alguna de las cláusulas del presente contrato fuere declarada nula o inaplicable, dicha cláusula se considerará excluida del contrato, sin que implique la nulidad del mismo. En este caso las partes harán cuanto esté a su alcance para encontrar una solución equivalente que sea válida y que refleje debidamente sus intenciones.

Los encabezamientos de las distintas cláusulas lo son sólo a efectos informativos, y no afectarán, calificarán o ampliarán la interpretación de este Contrato.

Y en prueba de conformidad y aceptación de cuanto antecede, ambas partes firman los [Nº] folios del presente CONTRATO DE COMPRAVENTA DE PARTICIPACIONES, extendido por duplicado y a un solo efecto, en la ciudad y fecha mencionados en el encabezamiento.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Fdo. Don [NOMBRE Y APELLIDOS]

(La Vendedora)

Fdo. Don [NOMBRE Y APELLIDOS]

(La Compradora)

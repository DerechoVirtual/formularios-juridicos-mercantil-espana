---
name: escritura-publica-compraventa-acciones-portador-sa-mer-0195
description: "Escritura pública de compraventa de acciones al portador de una SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura pública de compraventa de acciones al portador de una SA

> Formulario **MER-0195** del plugin **Sociedades de capital: juntas, administradores, capital y cuentas** (`formularios-sociedades-de-capital`) · Mercantil › Sociedades de capital (juntas, órganos, capital y cuentas) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura pública de compraventa de acciones al portador de una SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura pública de compraventa de acciones al portador de una SA” para mi caso». También puedes invocarla directamente con `/formularios-sociedades-de-capital:escritura-publica-compraventa-acciones-portador-sa-mer-0195`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-sociedades-de-capital:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Sociedades de capital: juntas, administradores, capital y cuentas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (14 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] AÑO (4 veces)
- [ ] DÍA (4 veces)
- [ ] IMPORTE (4 veces)
- [ ] MES (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] CALLE (3 veces)
- [ ] ACTIVIDAD (2 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] CLASE DE ACCIONES
- [ ] COLEGIO
- [ ] INSCRIPCIÓN
- [ ] LUGAR
- [ ] NOMBRE DE LOS FUNDADORES
- [ ] PLAZO
- [ ] PORCENTAJE
- [ ] SITUACIÓN DE LAS ACCIONES
- [ ] TOMO
- [ ] TÍTULO DE ADQUISICIÓN

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

ESCRITURA PÚBLICA DE COMPRAVENTA DE ACCIONES AL PORTADOR

NÚMERO DE PROTOCOLO:

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Ante mí, Notario del Ilustre Colegio de [COLEGIO].

COMPARECEN

De una parte, D./Dña.. [NOMBRE Y APELLIDOS], de nacionalidad [NACIONALIDAD] con Documento Nacionalidad de Identidad número [NÚMERO] y con domicilio en [LOCALIDAD], calle [CALLE] número [NÚMERO], C.P., en lo sucesivo EL VENDEDOR

De la otra parte, D./Dña.. [NOMBRE Y APELLIDOS], de nacionalidad [NACIONALIDAD]. con Documento Nacionalidad de Identidad número [NÚMERO] y con domicilio en [LOCALIDAD], calle [CALLE] número [NÚMERO], C.P., en lo sucesivo EL COMPRADOR.

Les identifico por sus respectivos D.N.I. antes reseñados, y tienen, a mi juicio, según intervienen, la capacidad legal necesaria para otorgar la presente escritura de COMPRAVENTA DE ACCIONES AL PORTADOR y a tal fin,

MANIFIESTAN

I.- Que EL VENDEDOR es dueño, en pleno dominio, de [Nº] acciones al portador con los números [Nº] al [Nº], ambos inclusive, de la mercantil [DENOMINACIÓN SOCIAL], S.A., cuyo domicilio social se halla sito en [LOCALIDAD], calle [CALLE], C.P., y fue constituida por [NOMBRE DE LOS FUNDADORES] mediante escritura autorizada por el Notario de D./Dña. [NOMBRE Y APELLIDOS] el [DÍA] de [MES] de [AÑO], bajo el número [NÚMERO] de los de su protocolo.

La citada sociedad se halla inscrita en el Registro Mercantil de [LOCALIDAD] al Tomo [TOMO], Folio, Hoja, inscripción [INSCRIPCIÓN], tiene un capital social de [IMPORTE] euros, dividido en [Nº] acciones de [IMPORTE] euros de valor nominal de cada una de ellas el cual se halla totalmente desembolsado, y le corresponde el CIF número

Título.- El VENDEDOR manifiesta ser socio de [DENOMINACIÓN SOCIAL], S.A. como propietario y titular de [Nº] acciones, que suponen un [Nº] por ciento del capital social, adquiridas por [TÍTULO DE ADQUISICIÓN] según resulta de los títulos que el compareciente me exhibe, sin que en lo omitido en nada amplíe, limite, condicione o contradiga lo expuesto, y en los que no figura nota alguna de transmisión posterior.

Cargas.- Manifiesta igualmente el VENDEDOR que las citadas acciones se hallan libres de toda carga, gravamen, responsabilidad o afección, manifestándose por la parte transmitente que se hayan [SITUACIÓN DE LAS ACCIONES].

II.- Que el COMPRADOR está interesado en adquirir las acciones descritas en la manifestación precedente, y que por ello ambas partes

ACUERDAN

Llevar a efecto el presente contrato de COMPRAVENTA DE ACCIONES AL PORTADOR mediante las siguientes

CLÁUSULAS

Objeto

LA VENDEDORA vende y transmite a LA COMPRADORA, que compra y adquiere libres de cargas y gravámenes las acciones de las que la primera es titular, esto es, [Nº] acciones [CLASE DE ACCIONES], las señaladas con los números [Nº] a la [Nº], y números [Nº] a la [Nº], todas ellas inclusive, que están totalmente desembolsadas y que representan el [PORCENTAJE] % del capital social de la Compañía (en lo sucesivo, “Las Acciones”).

[ELEGIR UNA OPCIÓN: Precio / Pago efectuado antes de la firma del contrato / Pago no aplazado efectuado después de la firma del contrato / Pago aplazado efectuado después de la firma del contrato]

Transmisión de la titularidad

La transmisión de la titularidad de las acciones se efectuará en el momento de la firma del presente Contrato y conlleva la transmisión de todos los derechos políticos y económicos inherentes a las mismas.

Declaraciónes y garantías

El capital social de La Compañía es de [IMPORTE] euros ( €) y está dividido en [Nº] acciones de [IMPORTE] euros de valor nominal cada una, por lo que las acciones que se transmiten representan el % del capital de la Compañía a la fecha de la firma del presente Contrato.

LA VENDEDORA declara, en su calidad de accionista de la Compañía, que se han cumplido todos los requisitos legales y aquellos previstos en los Estatutos Sociales en orden a la transmisión de las mismas.

Igualmente, LA VENDEDORA declara que no existen ningún litigio, procedimiento judicial, reclamación o inspección administrativa pendiente, y que no hay visos de contienda civil, mercantil, fiscal, administrativa, laboral o de cualquier otra índole.

Además, LA VENDEDORA manifiesta que las acciones objeto del presente Contrato le pertenecen en pleno dominio por justo y legítimo título y que las mismas están libres y exentas de cualesquiera opciones, gravámenes, convenios, compromisos, reclamaciones, embargos, afectaciones o gravámenes, no existiendo deuda alguna en relación con las mismas que afecte a LA VENDEDORA, o que de cualquier forma pudieran influenciar o condicionar los derechos que LA COMPRADORA adquiere.

LA VENDEDORA se hace responsable de los daños o perjuicios que le ocasione a LA COMPRADORA los eventuales incumplimientos o excepciones a las manifestaciones y garantías vertidas en los párrafos precedentes.

Situación de la compañia

LA VENDEDORA declara que la Compañía está debidamente constituida y registrada de conformidad con la legislación aplicable.

La Compañía no se encuentra en situación legal de insolvencia y en el momento actual no existe indicio alguno que sostenga una eventual declaración de insolvencia.

La Compañía tiene capacidad para desarrollar su actual actividad, para ser propietaria y gestionar sus bienes, derechos y obligaciones. Los estatutos sociales actuales de la Compañía son los aprobados mediante acuerdo de la Junta General de socios de fecha [DÍA] de [MES] de [AÑO], estatutos que fueron elevados a públicos mediante escritura de fecha [DÍA] de [MES] de [AÑO] otorgada ante el Ilustre Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS] incorporados como Anexo I.

La Compañía tiene todos los permisos, licencias, autorizaciones, aprobaciones preceptivos y no incumple ninguna ley o normativa urbanística, sobre medio ambiente o de cualquier otro tipo administrativo, y no se ha recibido notificación alguna sobre un eventual incumplimiento de las mismas.

Pacto de no concurrencia

Durante el plazo de [PLAZO] desde la conclusión del presente contrato, LA VENDEDORA se compromete a no realizar actividades por cuenta propia o ajena que de algún modo pudieran concurrir con la actividad desempeñada por la Compañía.

Durante la vigencia del presente pacto LA VENDEDORA no podrá desempeñar, directa o indirectamente, y sin el consentimiento expreso de LA COMPRADORA cualquiera de las actividades que a continuación se describen:

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

La compraventa que antecede queda condicionada por medio del establecimiento de la presente condición resolutoria a la falta de permanencia en el futuro en la prestación de servicios en la Compañía por parte de LA COMPRADORA, en cuyo caso procederá la resolución inmediata de la compraventa frente a LA VENDEDORA

Gastos

Todos los gastos originados por el presente contrato correrán por cuenta del [ELEGIR: vendedor / comprador].

Régimen legal

Este contrato reviste carácter mercantil y se regirá por sus propias cláusulas, y en lo en ellas no dispuesto, por la Ley de Sociedades de Capital, y en su defecto por el Código de Comercio, usos mercantiles, Leyes especiales y por lo previsto en el Código Civil.

Advertencia registral

Advierto al COMPRADOR de la obligación de comunicar a la Sociedad la presente transmisión a los efectos de la debida anotación en el Libro Registro de Socios.

[ELEGIR UNA OPCIÓN: Comunicación al registro mercantil / Presentación telemática / Presentación no telemática]

Protección de datos personales

Advierto expresamente al compareciente que sus datos van a ser incorporados al fichero del Protocolo y documentación notarial y al fichero de Administración y organización, así como del hecho de que, en su caso, tales datos pueden ser cedidos a aquellas Administraciones públicas que según una norma con rango de ley tengan derecho a ello. Hechas las advertencias de sus derechos al respecto.

Otorgamiento y autorización

Se han hecho las reservas y advertencias legales, en especial advierto de la necesidad de la inscripción en el Registro Mercantil de los actos formalizados en esta escritura y en particular y a efectos fiscales he advertido a los comparecientes de la obligación de presentación de la documentación a liquidar dentro de plazo y de las obligaciones y responsabilidades tributarias que les incumben en su aspecto material, formal y sancionador, y de las consecuencias de toda índole que se derivarían de la inexactitud de sus declaraciones.

Les leo, por su elección, esta escritura, advertidos de su derecho a leerla por sí, del que no usan y, tras hacerles las oportunas explicaciones verbales para su cabal conocimiento, manifiestan quedar enterados, la aceptan, se ratifican y firman.

Yo, el Notario, Doy fe de que el consentimiento ha sido libremente prestado y de que el otorgamiento se adecua a la legalidad y a la voluntad debidamente informada de los otorgantes.

Queda extendida en un total de [Nº] folios de papel notarial, el primero con el número y los demás con los números siguientes en orden correlativo.

Y de su contenido, DOY FE.

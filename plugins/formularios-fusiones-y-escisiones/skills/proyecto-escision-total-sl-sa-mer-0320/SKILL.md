---
name: proyecto-escision-total-sl-sa-mer-0320
description: "Proyecto de escisión total de una SL o SA. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Proyecto de escisión total de una SL o SA

> Formulario **MER-0320** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Proyecto de escisión total de una SL o SA» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Proyecto de escisión total de una SL o SA” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:proyecto-escision-total-sl-sa-mer-0320`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (21 veces)
- [ ] Nº (14 veces)
- [ ] LOCALIDAD (12 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] IMPORTE (8 veces)
- [ ] NIF (7 veces)
- [ ] ESTADO CIVIL (5 veces)
- [ ] FECHA (5 veces)
- [ ] NACIONALIDAD (5 veces)
- [ ] NÚMERO (5 veces)
- [ ] CALLE (3 veces)
- [ ] DIRECCIÓN (3 veces)
- [ ] OBJETO SOCIAL (3 veces)
- [ ] DATOS DE IDENTIFICACIÓN (2 veces)
- [ ] DATOS DEL BALANCE (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] C.P.
- [ ] CRITERIO DE ATRIBUCIÓN
- [ ] MÉTODOS DE VALORACIÓN
- [ ] NOMBRE O DENOMINACIÓN
- [ ] Nº DE ANEXO
- [ ] Nº DE ARTÍCULO
- [ ] OBJETIVO DE LA ESCISIÓN
- [ ] PLAZO

## Normas que cita el formulario

- art. 65 Real Decreto-ley 5/2023
- art. 69 Real Decreto-ley 5/2023
- art. 37 Real Decreto-ley 5/2023

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

Contenido del proyecto que formaliza la extinción de una sociedad, con división de todo su patrimonio en dos o más partes, cada una de las cuales se transmite en bloque por sucesión universal a una sociedad de nueva creación o es absorbida por una sociedad ya existente, recibiendo los socios un número de acciones, participaciones o cuotas de las sociedades beneficiarias proporcional a su respectiva participación en la sociedad que se escinde.

PROYECTO DE ESCISIÓN TOTAL DE LA SOCIEDAD «[NOMBRE O DENOMINACIÓN]»

Proyecto de escisión total que suscriben todos los miembros del órgano de administración de « [DENOMINACIÓN SOCIAL] » y de « [DENOMINACIÓN SOCIAL] así como los sujetos propuestos para ocupar los cargos de administrador de la futura sociedad creada con una de las partes escindidas « [DENOMINACIÓN SOCIAL] para su aprobación por la junta general de socios, tal y como se establece en el Real Decreto-ley 5/2023, de 28 de junio.

La modalidad de escisión propuesta a la junta general de socios consiste en la escisión total de « [DENOMINACIÓN SOCIAL] con división de su patrimonio en dos bloques, cada uno de ellos consistente en una unidad económica, uno de los cuales será traspasado por sucesión universal a la sociedad [DENOMINACIÓN SOCIAL] preexistente « [DENOMINACIÓN SOCIAL] y el otro será atribuido también por sucesión universal a una sociedad [ELEGIR: anónima / limitada] de nueva creación que tendrá el nombre de « [DENOMINACIÓN SOCIAL] Los socios de la empresa que se escinde recibirán [ELEGIR: acciones / participaciones] de las sociedades beneficiarias el equivalente a su respectiva participación en la sociedad que se escinde totalmente y por tanto, se extingue.

El proceso de escisión se somete al regulado en el Real Decreto-ley 5/2023. De esta forma, a este proyecto se le adjunta el preceptivo informe de los administradores exigido por el artículo 67 de la Ley antes mencionada y, al ser la sociedad [DENOMINACIÓN SOCIAL] » una sociedad anónima, también del informe de los expertos independientes requerido por el artículo 68 del mismo texto legal.

Los administradores de las sociedades participantes en la escisión, se abstendrán, a partir de la suscripción del presente proyecto de escisión, de intervenir y de ejecutar cualquier clase de acto o de concluir cualquier contrato que pueda perjudicar la aprobación de este proyecto o cambiar sustancialmente la ecuación de canje de las acciones indicadas en el mismo.

[ELEGIR UNA OPCIÓN: Con página web / Sin página web]

En cumplimiento de las previsiones contenidas en la regulación vigente, se formulan a continuación las menciones exigidas por los mismos:

Primero.- Identificación de sociedades.

1. Sociedad escindida.

A La sociedad escindida « [DENOMINACIÓN SOCIAL] » se constituyó por tiempo indefinido, en escritura autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], con el número [NÚMERO] de su protocolo. Consta inscrita en el Registro Mercantil de [LOCALIDAD], en el

B Su domicilio social se localiza en [DIRECCIÓN], calle [CALLE], número [NÚMERO] CP [C.P.] de [LOCALIDAD]

C Su capital social es de [IMPORTE] euros, dividido en [Nº] de [IMPORTE] euros de valor nominal cada una, numeradas del 1 al [Nº] ambos inclusive.

D Su Número de Identificación Fiscal es [NIF]

E El objeto social es [OBJETO SOCIAL]

F El ejercicio social se inicia el 1 de enero y finaliza el 31 de diciembre coincidiendo con el año natural.

G La administración de la empresa [DENOMINACIÓN SOCIAL] se lleva a cabo por un consejo de administración formado por [Nº] miembros, según se desprende de la inscripción núm. [Nº] de la sociedad en el Registro Mercantil. Las personas que forman parte del Consejo de Administración son:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], con DNI/NIF [NIF], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD]

2. Sociedad beneficiaria (preexistente).

A La sociedad beneficiaria « [DENOMINACIÓN SOCIAL] » fue constituida por tiempo indefinido, en escritura autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], [OTROS DATOS], el día [FECHA], con el número [NÚMERO] de su protocolo. Consta inscrita en el Registro Mercantil de [LOCALIDAD], en el

B Su domicilio social se halla ubicado en [DIRECCIÓN], calle [CALLE], número [NÚMERO] de [LOCALIDAD]

C Su Número de Identificación Fiscal es [NIF]

D El capital social es de [IMPORTE] euros, dividido en [Nº], de [IMPORTE] euros de valor nominal cada una, numeradas del 1 al [Nº] ambos inclusive.

E El objeto social es [OBJETO SOCIAL]

F El ejercicio social coincide con el año natural.

G La administración de la sociedad está confiada a un consejo de administración formado por [Nº] miembros. El órgano de administración está integrado por las personas que se detallan a continuación, según se desprende de la inscripción núm. [Nº] de la sociedad en el Registro Mercantil:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], con DNI/NIF [NIF], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD]

3. Sociedad beneficiaria (de nueva creación.

Sociedad a constituir por el otorgamiento de la escritura de escisión, bajo la denominación de « [DENOMINACIÓN SOCIAL] », según certificación del Registro Mercantil Central de fecha [FECHA] y con las siguientes características:

A El objeto social al que se dedicará esta nueva empresa será [OBJETO SOCIAL]

B Su domicilio social se localizará en [DIRECCIÓN], calle [CALLE], número [NÚMERO] de [LOCALIDAD]

C Contará con un capital social de [IMPORTE] euros, dividido en [Nº] de [IMPORTE] euros de valor nominal cada una, numeradas del 1 al [Nº] ambos inclusive.

D El ejercicio social coincidirá con el año natural

E La administración de la sociedad será ejercida por un consejo de administración integrado por [Nº] miembros que son los siguiente:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], con DNI/NIF [NIF], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD]

Segundo.- Tipo de canje y reparto.

[ELEGIR UNA OPCIÓN: Sin compensación en metálico. / Con compensación en metálico.]

El tipo de canje establecido ha sido calculado de conformidad con la valoración de mercado del patrimonio de las distintas sociedades participantes en la escisión, teniendo en cuenta el valor de sus activos en las circunstancias específicas en que se encuentran, y de los pasivos de las mismas.

Para ello se ha contado con el asesoramiento de [NOMBRE Y APELLIDOS], quien ha valorado los patrimonios sociales conforme a los siguientes métodos y criterios de valoración: [MÉTODOS DE VALORACIÓN].

El socio que se considere perjudicado por la relación de canje establecida, pueden impugnarla y reclamar un pago en efectivo ante el Tribunal de Instancia (Sección de lo Mercantil) del domicilio social, cuya competencia será exclusiva, o el tribunal arbitral estatutariamente previsto, siempre que no hayan votado a favor de la aprobación del acuerdo de fusión o no tengan derecho de voto dentro del plazo de dos meses desde la fecha de publicación del acuerdo de la junta general.

Tercero.- Procedimiento de canje.

El canje se efectuará en el plazo de un mes, a contar desde la inscripción de la escritura de escisión en el Registro Mercantil.

El canje de las no supondrá desembolso alguno para los socios.

Cuarto.- Elementos del activo y pasivo a transmitir.

1 Patrimonio de la sociedad escindida que se traspasa a « [DENOMINACIÓN SOCIAL] ».

2 Patrimonio de la sociedad escindida que se traspasa a « [DENOMINACIÓN SOCIAL] ».

3 Elementos patrimoniales no atribuidos.

Los elementos del activo y del pasivo que no estuvieran atribuidos en las relaciones anteriores se atribuirán según el criterio de [CRITERIO DE ATRIBUCIÓN].

No obstante, en caso de duda o conflicto, será de aplicación lo dispuesto en el artículo 65 del Real Decreto-ley 5/2023.

De acuerdo con lo establecido en el art.69 del Real Decreto-ley 5/2023, cualquier modificación importante del patrimonio de la Sociedad Escindida llevada a cabo entre la fecha de elaboración del Proyecto de Escisión y la fecha de reunión de la junta que haya de decidir sobre la misma será notificada por los administradores de la Sociedad Escindida a su junta de socios. La misma información proporcionarán los administradores de las Sociedades Beneficiarias y éstos a los administradores de la Sociedad Escindida, para que, a su vez, informe a su junta de socios.

Quinto.- Efectos de la escisión sobre derechos de socios y terceros.

1 No existe en la Sociedad Escindida [ELEGIR: acciones / participaciones] que lleven aparejadas prestaciones accesorias, que puedan resultar afectadas por la escisión (art. 40.4.ª RD-ley 5/2023).

2 La sociedad escindida no tiene titulares de derechos especiales distintos de las [ELEGIR: acciones / participaciones] ni tenedores de títulos distintos de los representativos del capital, por lo que no procede el otorgamiento de ningún derecho especial ni el ofrecimiento de ningún tipo de opciones.

3 No se otorga ventaja alguna a los expertos independientes que intervienen en el proyecto de escisión, así como tampoco se atribuyen ventajas de ninguna clase a los administradores sociales de las compañías participantes en la escisión, sin perjuicio de la retribución que a favor de los administradores de las sociedades beneficiarias establecen sus respectivos estatutos.

4 Las [ELEGIR: acciones / participaciones] de las sociedades beneficiarias atribuidas a los socios de la sociedad escindida darán derecho a participar en las ganancias sociales y ejercitar los demás derechos que tal titularidad les atribuye en la sociedad beneficiaria a partir del día [FECHA].

5 [OTROS DATOS].

Sexto.- Fecha de efectos contables de la escisión.

Las operaciones que realice « [DENOMINACIÓN SOCIAL] » a partir del día [FECHA], se entenderá, a efectos contables, que han sido realizadas por cuenta de « [DENOMINACIÓN SOCIAL] » o de « [DENOMINACIÓN SOCIAL] », según corresponda en virtud de la naturaleza del patrimonio atribuido.

Séptimo- Cumplimiento de obligaciones fiscales y laborales

La sociedad está al corriente en el cumplimiento de las obligaciones tributarias y frente a la Seguridad Social, acreditado mediante la aportación de los correspondientes certificados, válidos y emitidos por el órgano competente.

Octavo.- Fecha de las cuentas utilizadas para la escisión.

La fecha de las cuentas de la sociedad que se escinde que se utilizan para establecer las condiciones en que se realiza la escisión es [DATOS DEL BALANCE]. Por tanto y a efectos de lo previsto en el art. 43 RD-ley 5/2023 se considera como balance de escisión:

[ELEGIR UNA OPCIÓN: El último balance anual / Balance ad hoc]

La fecha de las cuentas de la sociedad beneficiaria preexistente que se utilizan para establecer las condiciones en que se realiza la escisión es [DATOS DEL BALANCE] Por tanto y a efectos de lo previsto en el art.43 del RD-ley 5/2023, se considera como balance de escisión:

[ELEGIR UNA OPCIÓN: El último balance del ejercicio / Balance ad hoc]

Los balances de escisión - deberán ser verificados por el auditor de cuentas de la sociedad y aprobadas por la junta general de accionistas que haya de resolver sobre la escisión, con carácter previo a la adopción del propio acuerdo de escisión.

Noveno.- Extinción de la sociedad que se escinde.

La sociedad « [DENOMINACIÓN SOCIAL] » escindida se extinguirá como consecuencia de la operación.

Décimo.- Modificación de estatutos de la sociedad beneficiaria preexistente.

La sociedad beneficiaria « [DENOMINACIÓN SOCIAL] » Procederá al aumento de su capital en la cantidad de [IMPORTE] euros, dividido en [Nº], de [IMPORTE] euros de valor nominal cada una, numeradas del [Nº] al [Nº] Quedando, por esta causa modificado el artículo [Nº DE ARTÍCULO] de los estatutos sociales, relativo al capital social, cuya redacción será la siguiente:

Las nuevas [ELEGIR: acciones / participaciones] emitidas, se asignarán a los accionistas de la Sociedad en proporción a sus respectivas participaciones en la entidad que se escinde, del siguiente modo:

Decimoprimero.- Estatutos de la nueva sociedad beneficiaria.

Como anexo [Nº DE ANEXO] se adjunta a este proyecto de escisión la propuesta de estatutos de la sociedad [DENOMINACIÓN SOCIAL]

Decimosegundo.- Órganos de administración de las sociedades participantes en la escisión.

1.º Sociedad beneficiaria de nueva creación.

La nueva sociedad creada será administrada [ELEGIR: por un administrador único / por varios administradores solidarios / por varios administradores mancomunados / por un consejo de administración].

Los administradores de esta nueva sociedad son:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], [DATOS DE IDENTIFICACIÓN], mayor de edad, de estado civil [ESTADO CIVIL], con DNI/NIF [NIF], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD]

Conforme dispone el proyecto de estatutos los cargos nombrados tendrán una duración de [PLAZO]

2 Sociedad beneficiaria preexistente.

La sociedad beneficiaria preexistente será administrada [ELEGIR: por un administrador único / por varios administradores solidarios / por varios administradores mancomunados / por un consejo de administración].

Los administradores de esta sociedad son:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], [DATOS DE IDENTIFICACIÓN], mayor de edad, de estado civil [ESTADO CIVIL], con DNI/NIF [NIF], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD]

Decimotercero.- Consecuencias de la escisión sobre el empleo, y la responsabilidad social de la empresa.

Empleo.

Como consecuencia de la escisión total de [DENOMINACIÓN SOCIAL] y su consiguiente disolución sin liquidación, no se extinguirán las relaciones laborales existentes en dicha sociedad. En su lugar, las Sociedades Beneficiarias se subrogarán en los derechos y obligaciones laborales y de Seguridad Social de la Sociedad Escindida, incluyendo los compromisos por pensiones y, en general, las obligaciones adquiridas en materia de protección social complementaria.

Responsabilidad social.

Como consecuencia de la escisión, las Sociedades Beneficiarias asumirán las deudas sociales de la Sociedad Escindida de conformidad con el criterio de reparto establecido.

De las deudas nacidas antes de la publicación del proyecto de escisión y aun no vencidas en ese momento asumidas frente a los acreedores de la sociedad escindida por una sociedad beneficiaria que resulten incumplidas, responderán solidariamente todas las sociedades beneficiarias hasta el importe de los activos netos atribuidos a cada una de ellas en la escisión y, si subsistiera, la propia sociedad escindida, hasta el importe de los activos netos que permanezcan en ella.

En esos mismos términos responderán solidariamente las sociedades beneficiarias de las deudas de la sociedad escindida nacidas antes de la publicación del proyecto de escisión y no vencidas en ese momento.

La responsabilidad solidaria de las sociedades participantes en la escisión prescribirá los cinco años.

En la Sociedad Escindida no existen socios con responsabilidad personal, por lo que no es de aplicación el régimen de responsabilidad extraordinario recogido en la regulación vigente.

Decimocuarto.- Otros datos.

1 La escisión total tiene como objetivo prioritario y principal [OBJETIVO DE LA ESCISIÓN]

2 La operación de escisión se acogerá al régimen especial establecido en la Ley 27/2014, de 27 de noviembre, del Impuesto sobre Sociedades

3 En virtud de lo dispuesto en el artículo 37 del Real Decreto-ley 5/2023, las [ELEGIR: acciones / participaciones] de las sociedades que participan en la escisión y que estuvieran en su poder, no pueden canjearse por [ELEGIR: acciones / participaciones] creadas como consecuencia de la escisión y deben ser amortizadas o extinguidas. Su valor en el patrimonio de la sociedad propietaria se ha tenido en cuenta a efectos de fijar la relación de canje.

4 Todos los administradores de las sociedades participantes en la escisión, solicitarán del Registro Mercantil de "domicilio de cualquiera de las Sociedades Beneficiarias o de la Sociedad Escindida", la designación de un experto independiente para la elaboración de un único informe sobre el proyecto de escisión y lleve a cabo la valoración del patrimonio no dinerario que se transmite a cada Sociedad Beneficiaria.

Decimoquinto.- Firmas de los miembros del órgano de administración.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

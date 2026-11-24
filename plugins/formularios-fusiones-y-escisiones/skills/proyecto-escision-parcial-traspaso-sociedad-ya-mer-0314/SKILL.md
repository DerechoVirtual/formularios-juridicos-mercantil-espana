---
name: proyecto-escision-parcial-traspaso-sociedad-ya-mer-0314
description: "Proyecto de escisión parcial con traspaso a una sociedad ya existente (escisión-absorción). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Proyecto de escisión parcial con traspaso a una sociedad ya existente (escisión-absorción)

> Formulario **MER-0314** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Los administradores de cada una de las sociedades que participen en la escisión parcial con atribución del patrimonio escindido a una sociedad preexistente habrán de redactar y suscribir un proyecto común de escisión con el contenido establecido en los arts. 39 y 64 del Real Decreto-ley 5/2023. Si falta la firma de alguno de ellos, se señalará al final del proyecto, con indicación de la causa.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Proyecto de escisión parcial con traspaso a una sociedad ya existente (escisión-absorción)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Proyecto de escisión parcial con traspaso a una sociedad ya existente (escisión-absorción)” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:proyecto-escision-parcial-traspaso-sociedad-ya-mer-0314`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (11 veces)
- [ ] NOMBRE Y APELLIDOS (9 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] IMPORTE (7 veces)
- [ ] FECHA (5 veces)
- [ ] NIF (5 veces)
- [ ] ESTADO CIVIL (3 veces)
- [ ] NACIONALIDAD (3 veces)
- [ ] CÓDIGO POSTAL (2 veces)
- [ ] DIRECCIÓN (2 veces)
- [ ] NOMBRE O DENOMINACIÓN (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] OBJETO SOCIAL (2 veces)
- [ ] ACTIVIDAD
- [ ] Nº DE ANEXO
- [ ] NÚMERO
- [ ] OBJETIVO DE LA ESCISIÓN
- [ ] PLAZO

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

Los administradores de cada una de las sociedades que participen en la escisión parcial con atribución del patrimonio escindido a una sociedad preexistente habrán de redactar y suscribir un proyecto común de escisión con el contenido establecido en los arts. 39 y 64 del Real Decreto-ley 5/2023. Si falta la firma de alguno de ellos, se señalará al final del proyecto, con indicación de la causa.


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

PROYECTO DE ESCISIÓN DE «[NOMBRE O DENOMINACIÓN]»

Proyecto de escisión que firman todos los miembros de los órganos de administración de «[NOMBRE O DENOMINACIÓN]» y « para su aprobación por la junta general de socios, de conformidad a lo previsto en los artículos 39, 40, 63 y 64 del RD-ley 5/2023.

El tipo de escisión propuesto a la junta general de socios consiste en la escisión parcial de « mediante el traspaso en bloque por sucesión universal de una parte de su patrimonio, que forma una unidad económica, a la sociedad [DENOMINACIÓN SOCIAL] preexistente «. Los socios de la sociedad que se escinde recibirán un número de [ELEGIR: acciones / participaciones] de la sociedad beneficiaria equivalentes a su respectiva participación en la sociedad que se escinde parcialmente. Sociedad esta, que procederá a reducir el capital social en la cuantía necesaria.

La escisión queda sujeta al régimen establecido en el Real Decreto-ley 5/2023, de 28 de junio, (…) detransposición de Directivas de la Unión Europeaen materia de modificaciones estructurales. Se adjunta a este proyecto el informe de los administradores previsto en el artículo 67 de aquella norma y, y también el de los expertos independientes exigido por el artículo 68 del mismo texto legal por ser la sociedad [DENOMINACIÓN SOCIAL] una Sociedad Anónima.

Los administradores de las sociedades participantes en la escisión, se abstendrán, a partir de la suscripción del presente proyecto de escisión, de intervenir y de ejecutar cualquier clase de acto o de concluir cualquier contrato que pueda perjudicar la aprobación de este proyecto o cambiar sustancialmente la ecuación de canje de las acciones indicadas en el mismo.

[ELEGIR UNA OPCIÓN: Con página web / Sin página web]

En cumplimiento de las previsiones contenidas en los arts.40 y 64 del RD- ley 5/2023, se formulan a continuación las menciones exigidas por los mismos:

Primero.- Identificación de las sociedades

1. Sociedad escindida.

A) La sociedad escindida «[DENOMINACIÓN SOCIAL]» se constituyó por tiempo indefinido, en escritura autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], con el número de su protocolo. Consta inscrita en el Registro Mercantil de [LOCALIDAD], en el

B) Su domicilio social está ubicado en [DIRECCIÓN], [CÓDIGO POSTAL] de [LOCALIDAD]

C) Su Número de Identificación Fiscal es [NIF]

D) El objeto social es [OBJETO SOCIAL]

E) El capital social es de [IMPORTE] euros, dividido en [Nº] de [ELEGIR: acciones / participaciones] de [IMPORTE] euros de valor nominal cada una, numeradas del 1 al [Nº] ambos inclusive.

F) El ejercicio social coincide con el año natural.

G) La administración de la sociedad se confía a un consejo de administración formado por [Nº] miembros. Según se desprende de la inscripción núm. [Nº] de la sociedad en el Registro Mercantil. El órgano de administración está integrado por las personas que se detallan a continuación:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] mayor de edad, de estado civil [ESTADO CIVIL], con DNI/NIF [NIF], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD]

B. Sociedad beneficiaria.

A) La sociedad beneficiaria «[DENOMINACIÓN SOCIAL]» se constituyó por tiempo indefinido, en escritura autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], con el número [NÚMERO] de su protocolo. Consta inscrita en el Registro Mercantil de [LOCALIDAD], en el
B) Su domicilio social se ubica en [DIRECCIÓN], [CÓDIGO POSTAL]
C) Su Número de Identificación Fiscal es [NIF]
D) El objeto social es [OBJETO SOCIAL]
E) El capital social es de [IMPORTE] euros, dividido en [Nº] de [ELEGIR: acciones / participaciones] de [IMPORTE] euros de valor nominal cada una, numeradas del 1 al [Nº] ambos inclusive.
F) El ejercicio social coincide con el año natural.
G) La administración de la sociedad está confiada a un consejo de administración formado por [Nº] miembros. Según se desprende de la inscripción núm. [Nº] de la sociedad en el Registro Mercantil el órgano de administración está integrado por las personas que se detallan a continuación:
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], con DNI/NIF [NIF], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD]

Segundo.- Tipo de canje y reparto

[ELEGIR UNA OPCIÓN: Sin compensación en metálico / Con compensación en metálico]

El tipo de canje establecido ha sido calculado de conformidad con la valoración de mercado del patrimonio de las distintas sociedades participantes en la escisión, teniendo en cuenta el valor de sus activos en las circunstancias específicas en que se encuentran, y de los pasivos de las mismas.

Para ello se ha contado con el asesoramiento de [NOMBRE Y APELLIDOS], quien ha valorado los patrimonios sociales conforme a los siguientes métodos y criterios de valoración:

El socio que se considere perjudicado por la relación de canje establecida, podrá solicitar del registrador mercantil de su domicilio social, en el plazo de un mes a contar desde la fecha de publicación del acuerdo de escisión en el Boletín Oficial del Registro Mercantil, la designación un experto independiente que fije la cuantía de una indemnización compensatoria, siempre y cuando así lo acuerde expresamente la junta general de socios que haya de decidir sobre la escisión, o, en su caso, si así se hubiera previsto en los estatutos sociales.

Tercero.- Procedimiento de canje

El canje se efectuará en el plazo de un mes, a contar desde la inscripción de la escritura de escisión en el Registro Mercantil.

El canje de las [ELEGIR: acciones / participaciones] no supondrá desembolso alguno para los socios

Cuarto.- Elementos del activo y pasivo

Los elementos del activo y del pasivo de la sociedad."que se transmiten a la Sociedad Beneficiaria, constituyen una unidad económica autónoma, dedicada a la actividad de [ACTIVIDAD], con capacidad de operar en el tráfico jurídico de forma autónoma con sus propios recursos.

Dichos elementos del activo y pasivo que integran el patrimonio segregado de la Sociedad Escindida, y que serán transmitidos a la Sociedad Beneficiaria, son los siguientes:

Se adjunta en el anexo [Nº DE ANEXO] la relación de los bienes, derechos y obligaciones que constituyen el activo y el pasivo que se transmitirá a la sociedad beneficiaria. Esta relación se encuentra reflejada en el balance de escisión de la sociedad escindida que sirve de base para la operación.

De acuerdo con lo establecido en el art. 69 del RD-ley 5/2023, cualquier modificación importante del patrimonio de la Sociedad Escindida llevada a cabo entre la fecha de elaboración del Proyecto de Escisión y la fecha de reunión de la junta que haya de decidir sobre la misma será notificada por los administradores de la Sociedad Escindida a su junta de socios. La misma información proporcionarán los administradores de las Sociedades Beneficiarias y éstos a los administradores de la Sociedad Escindida, para que, a su vez, informe a su junta de socios.

Quinto.- Consecuencias de la escisión sobre derechos de socios y terceros

- Las de la sociedad beneficiaria atribuidas a los socios de la sociedad escindida darán derecho a participar en las ganancias sociales y ejercitar los demás derechos que tal titularidad les atribuye en la sociedad beneficiaria a partir del día [FECHA].
- No existe en la Sociedad Escindida [ELEGIR: acciones / participaciones] que lleven aparejadas prestaciones accesorias que puedan resultar afectadas por la escisión.
- La sociedad escindida no tiene titulares de derechos especiales distintos de las [ELEGIR: acciones / participaciones] ni tenedores de títulos distintos de los representativos del capital, por lo que no procede el otorgamiento de ningún derecho especial ni el ofrecimiento de ningún tipo de opciones.
- No se otorga ninguna ventaja a los expertos independientes que intervienen en el proyecto de escisión, así como tampoco se atribuyen ventajas de ninguna clase a los administradores sociales de las compañías participantes, sin perjuicio de la retribución prevén sus respectivos estatutos.

Sexto.- Efectos contables de la escisión

A efectos contables, se entenderá que las operaciones que realice « a partir del día [FECHA], y que afecten al patrimonio integrante de la unidad económica que se escinde, habrán sido realizadas por cuenta de «.

Séptimo.- Cuentas utilizadas para la escisión

Las cuentas de la sociedad que se escinde que se utilizan para establecer las condiciones en que se realiza la escisión tienen la siguiente fecha [FECHA]. Por tanto y a efectos de lo previsto en el art.43 del RD-ley 5/2023 se considera como balance de escisión:

[ELEGIR UNA OPCIÓN: Último balance anual / Balance ad hoc]

Los balances de escisión y las modificaciones de valoración contenidas en el mismo, deberán ser verificados por el auditor de cuentas de la sociedad y aprobadas por la junta general de socios que haya de resolver sobre la escisión, con carácter previo a la adopción del propio acuerdo de escisión.

Octavo.- Modificaciones de estatutos

1. Sociedad escindida.

Como consecuencia de la escisión, la sociedad escindida «[DENOMINACIÓN SOCIAL]» reducirá su capital social en la cantidad de [IMPORTE] euros, por medio del siguiente procedimiento:

Como consecuencia de la reducción de capital se procede a modificar el artículo [Nº DE ARTÍCULO] de los estatutos sociales, que quedará redactado del siguiente modo:

2. Sociedad beneficiaria.

La sociedad beneficiaria «[DENOMINACIÓN SOCIAL]» aumenta su capital en la cantidad de [IMPORTE] euros, dividido en [Nº] de [IMPORTE] euros de valor nominal cada una, numeradas del [Nº] al [Nº]. Como consecuencia de la modificación descrita, se cambia la redacción del artículo [Nº DE ARTÍCULO] de los estatutos sociales, relativo al capital social:

Noveno.- Órganos de administración de las sociedades participantes en la escisión

1. Sociedad beneficiaria.

La sociedad beneficiaria será administrada por [ELEGIR: un administrador único / varios administradores solidarios / varios administradores mancomunados / un consejo de administración].

Los administradores de esta sociedad son:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ESTADO CIVIL], con DNI/NIF [NIF], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD]

Conforme dispone el proyecto de estatutos los cargos nombrados tendrán una duración de [PLAZO]

2. Sociedad que se escinde.

Décimo.- Consecuencias de la escisión sobre el empleo, y la responsabilidad social de la empresa

Empleo.

Como consecuencia de la escisión total de [DENOMINACIÓN SOCIAL] y su consiguiente disolución sin liquidación, no se extinguirán las relaciones laborales existentes en dicha sociedad. En su lugar, las Sociedades Beneficiarias se subrogarán en los derechos y obligaciones laborales y de Seguridad Social de la Sociedad Escindida, incluyendo los compromisos por pensiones y, en general, las obligaciones adquiridas en materia de protección social complementaria.

Responsabilidad social.

Como consecuencia de la escisión, las Sociedades Beneficiarias asumirán las deudas sociales de la Sociedad Escindida de conformidad con el criterio de reparto establecido, y sin perjuicio del derecho de oposición de los acreedores de las sociedades participantes en la escisión.

En caso de que alguna de las Sociedades Beneficiarias incumpla alguna de las obligaciones, las demás Sociedades Beneficiarias responderán solidariamente hasta el importe del activo neto atribuido en la escisión a cada una de ellas.

En la Sociedad Escindida no existen socios con responsabilidad personal, por lo que no es de aplicación el régimen de responsabilidad extraordinario recogido en el art. 52 del RD-ley 5/2023.

Decimoprimero.- Otros datos

1.º La escisión parcial tiene como finalidad principal [OBJETIVO DE LA ESCISIÓN]

2.º La operación de escisión se somete al régimen especial establecido en la Ley 27/2014, de 27 de noviembre, del Impuesto sobre Sociedades3.º En virtud de lo dispuesto en el artículo 37 del RD-ley 5/2023, de modificaciones estructurales de las sociedades mercantiles, las [ELEGIR: acciones / participaciones] de las sociedades que participan en la escisión y que estuvieran en su poder, no pueden canjearse por [ELEGIR: acciones / participaciones] creadas con motivo de la escisión y deben ser amortizadas o extinguidas. No obstante, su valor en el patrimonio de la sociedad propietaria se ha tenido en cuenta a efectos de fijar la relación de canje.

4ª Todos los administradores de las sociedades participantes en la escisión, solicitarán del Registro Mercantil de "domicilio de cualquiera de las Sociedades Beneficiarias o de la Sociedad Escindida", la designación de un experto independiente para la elaboración de un único informe sobre el proyecto de escisión y lleve a cabo la valoración del patrimonio no dinerario que se transmite a cada Sociedad Beneficiaria.

Decimosegundo.- Firmas de los miembros del órgano de administración

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

Firmado: D./Dña. [NOMBRE Y APELLIDOS]

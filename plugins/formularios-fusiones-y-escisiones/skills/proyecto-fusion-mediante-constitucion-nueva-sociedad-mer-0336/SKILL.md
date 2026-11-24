---
name: proyecto-fusion-mediante-constitucion-nueva-sociedad-mer-0336
description: "Proyecto de fusión mediante constitución de una nueva sociedad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Proyecto de fusión mediante constitución de una nueva sociedad

> Formulario **MER-0336** del plugin **Fusiones, escisiones y transformaciones de sociedades** (`formularios-fusiones-y-escisiones`) · Mercantil › Modificaciones estructurales (fusión, escisión, transformación) · normativa revisada el 24-11-2026.

## Qué es

Los administradores de cada una de las sociedades que participen en la fusión por creación de nueva Sociedad habrán de redactar y suscribir un proyecto común de fusión con el contenido establecido en el art. 40 Real Decreto-ley 5/2023. Si falta la firma de alguno de ellos, se señalará al final del proyecto, con indicación de la causa.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Proyecto de fusión mediante constitución de una nueva sociedad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Proyecto de fusión mediante constitución de una nueva sociedad” para mi caso». También puedes invocarla directamente con `/formularios-fusiones-y-escisiones:proyecto-fusion-mediante-constitucion-nueva-sociedad-mer-0336`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-fusiones-y-escisiones:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Fusiones, escisiones y transformaciones de sociedades) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (17 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] FECHA (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] Nº (4 veces)
- [ ] NOMBRE DE LA CALLE (2 veces)
- [ ] NOMBRE O DENOMINACIÓN (2 veces)
- [ ] Nº DE TÍTULOS (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] ACTIVIDAD
- [ ] CAUSA
- [ ] FORMA Y FECHA DE PAGO
- [ ] LUGAR
- [ ] NIF
- [ ] NÚMERO
- [ ] TIPO DE SOCIEDAD
- [ ] TOMO

## Normas que cita el formulario

- art. 39 Real Decreto-ley 5/2023
- art. 36.1 Real Decreto-ley 5/2023
- art. 43 Real Decreto-ley 5/2023
- art. 13 Real Decreto-ley 5/2023
- art. 52 Real Decreto-ley 5/2023

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

Los administradores de cada una de las sociedades que participen en la fusión por creación de nueva Sociedad habrán de redactar y suscribir un proyecto común de fusión con el contenido establecido en el art. 40 Real Decreto-ley 5/2023. Si falta la firma de alguno de ellos, se señalará al final del proyecto, con indicación de la causa.


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

PROYECTO DE FUSIÓN DE LAS SOCIEDADES «[NOMBRE O DENOMINACIÓN]» y «[NOMBRE O DENOMINACIÓN]»

Proyecto de fusión redactado y suscrito por los órganos de administración de las sociedades [DENOMINACIÓN SOCIAL] en cumplimiento de lo establecido por los arts. 39 y 40 del Real Decreto-ley 5/2023.

Por esta operación de Fusión las sociedades [DENOMINACIÓN SOCIAL] y [DENOMINACIÓN SOCIAL] se extinguirán, vía disolución sin liquidación, traspasando en bloque sus respectivos patrimonios a la sociedad de nueva creación ", que adquirirá por sucesión universal todos los derechos y obligaciones, entregando como contraprestación, a los socios de las sociedades extinguidas, un número de [ELEGIR: participaciones / acciones / cuotas] nuevas proporcional a sus respectivas [ELEGIR: participaciones / acciones / cuotas] en las sociedades extinguidas.

Las causas o razones que justifican la fusión de las sociedades citadas son:

Los administradores de las sociedades que intervienen en la fusión no deberán, a partir de la suscripción del presente proyecto de fusión, tal y como se establece en el artículo 39.2 RD-ley 5/2023, realizar cualquier clase de acto o de concluir cualquier contrato que pueda comprometer la viabilidad de este proyecto.

En cuanto a la tramitación a seguir se debe tener en cuenta que:

[ELEGIR UNA OPCIÓN: Con página web / Sin página web]

Primero.- Identificación de las sociedades que se fusionan

La fusión supondrá la extinción de las siguientes sociedades:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

• [ELEGIR: SRL / SA / SC por acc], NIF [NIF], con domicilio social en [LOCALIDAD] calle, [NOMBRE DE LA CALLE] número, [Nº], población [LOCALIDAD] constituida mediante escritura pública autorizada por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], el día [FECHA], con el número [NÚMERO] de su protocolo, e inscrita en el Registro Mercantil de [LOCALIDAD], tomo [TOMO],

La sociedad resultante de la fusión es:

« [ELEGIR: SRL / SA / SCpor acc] », cuyo domicilio se fijará en [LOCALIDAD], calle, [NOMBRE DE LA CALLE], número, [Nº], población [LOCALIDAD], y que tendrá como objeto social el desarrollo de [ACTIVIDAD], de conformidad con el proyecto de estatutos de la misma.

Segundo.- Tipo y procedimiento de canje

Tipo de canje.

La sociedad [ELEGIR: SRL / SA / SCpor acc], resultante de la fusión tendrá un capital de [IMPORTE], euros, dividido en [Nº], de [IMPORTE], euros de valor nominal cada una, numeradas del 1 al [Nº],

Estas participaciones [ELEGIR: Estas acciones acciones / Estas cuotas] se asignarán a los socios de las sociedades que se fusionan, teniendo en cuenta el valor real de los patrimonios sociales, tal y como se establece en el artículo 36.1 dell Real Decreto-ley 5/2023 en la siguiente proporción

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

A los socios de [DENOMINACIÓN SOCIAL] les corresponderá recibir, por cada [ELEGIR: participaciones / acciones / cuotas] de que son titulares en la citada sociedad [ELEGIR: participaciones / acciones / cuotas] de la sociedad de nueva creación [ELEGIR: SRL / SA / SCpor acc]

[OPCIONAL — incluir si procede]

Cuando existan acciones o participaciones propias o recíprocas

Igualmente se atribuye a los socios de cada sociedad la parte correspondiente a las [ELEGIR: participaciones / acciones / cuotas], propias o recíprocas detentadas por la propia sociedad y que son [Nº DE TÍTULOS], en « [DENOMINACIÓN SOCIAL], y [Nº DE TÍTULOS], en « [DENOMINACIÓN SOCIAL].

[OPCIONAL — incluir si procede]

Si existen fracciones en las acciones o participaciones

Debido a que el número de [ELEGIR: participaciones / acciones / cuotas] sociales resultante por el tipo de canje aplicado no es exacto, las fracciones de las [ELEGIR: participaciones / acciones / cuotas] sociales se compensarán en metálico, del siguiente modo:

Los socios de « [DENOMINACIÓN SOCIAL], » recibirán una compensación dineraria de [IMPORTE], euros por cada [ELEGIR: participaciones / acciones / cuotas], asignada, mientras que la compensación dineraria de los socios de « [DENOMINACIÓN SOCIAL], » será de [IMPORTE], euros por cada [ELEGIR: participaciones / acciones / cuotas], asignada [FORMA Y FECHA DE PAGO].

Procedimiento de canje.

Se procederá al canje de las [ELEGIR: participaciones / acciones / cuotas], personalmente o por correo, en el domicilio social, a partir de la firma de la escritura de fusión.

Por tratarse de la creación de una sociedad [TIPO DE SOCIEDAD], las antiguas [ELEGIR: participaciones / acciones / cuotas], quedarán amortizadas siendo posteriormente asignadas las nuevas en la escritura de fusión.

[OPCIONAL — incluir si procede]

Cuando las sociedades que se fusionan sean sociedades limitadas

No habrá intercambio físico de títulos, dado que las sociedades participantes en la fusión son sociedades de responsabilidad limitada.

Tercero.- Aportaciones de industria o prestaciones accesorias

En las sociedades que participan en el presente proceso de fusión no existen aportaciones de industria ni prestaciones accesorias.

Cuarto.- Derechos o títulos especiales

En las sociedades que participan en el presente proceso de fusión no existen titulares de derechos especiales distintos de las [ELEGIR: participaciones / acciones / cuotas]

Quinto.- Ventajas de expertos y administradores

En el presente proceso de fusión no se conceden ventajas especiales a favor de los expertos independientes ni de los administradores participantes [OTROS DATOS]

Sexto.- Fecha de inicio de participación en las ganancias

Desde la fecha de constitución de la sociedad resultante de la fusión las nuevas [ELEGIR: participaciones / acciones / cuotas], darán derecho a participar en las ganancias sociales [FECHA]

Séptimo.- Fecha de inicio de efectos contables

Las operaciones de las sociedades que se fusionan [DENOMINACIÓN SOCIAL] y [DENOMINACIÓN SOCIAL], se considerarán realizadas a efectos contables por cuenta de la nueva sociedad a partir de [FECHA].

Octavo.- Estatutos de [DENOMINACIÓN SOCIAL]

[ELEGIR UNA OPCIÓN: Reproducción / Anexo]

Noveno.- Valoración de activos y pasivos de las sociedades que se fusionan

El tipo de canje se ha determinado en base del valor real de los patrimonios de las sociedades que se fusionan, teniendo en cuenta el valor de sus activos y pasivos en las circunstancias específicas en que se encuentran a la fecha de inicio de la operación.

Los métodos de valoración han sido diseñados bajo el asesoramiento del experto, D./Dña. [NOMBRE Y APELLIDOS] quien ha valorado los patrimonios sociales conforme a criterios de valoración generalmente aceptados:

"Métodos de valoración empleados"

Décimo.- Fechas de las cuentas utilizadas para establecer las condiciones del proceso de Fusión

Las cuentas de las sociedades que se fusionan utilizadas para establecer las circunstancias y condiciones que rigen el presente proceso han sido cerradas a fecha [FECHA] En consecuencia, a efectos de lo previsto en el art.43 del Real Decreto-ley 5/2023, se considera como balance de fusión,

[ELEGIR UNA OPCIÓN: Último balance anual / Otro]

[OPCIONAL — incluir si procede]

Si es necesario realizar correcciones de valor

Se han procedido a efectuar correcciones de valor referentes a:

–Valor real del patrimonio inmobiliario.
–Valor de marcas, clientela, etc., capacidad de generar beneficios y fondo de comercio.
–Valor cierto de realización y cobro de los bines del activo circulante.
–Valor cierto del pasivo exigible.

Los balances de fusión y, en su caso, las modificaciones de valoración contenidas en el mismo, serán verificados por el auditor de cuentas de la sociedad y sometidos a la aprobación de la junta general de socios, con carácter previo a la adopción del propio acuerdo de fusión.

Decimoprimero.- Cumplimiento de obligaciones fiscales y laborales

Las sociedades que se fusionan están al corriente en el cumplimiento de las obligaciones tributarias y frente a la Seguridad Social, tal y como se acredita mediante la aportación de los correspondientes certificados, válidos y emitidos por el órgano competente

Decimosegundo.- Efectos de la fusión sobre el empleo, la responsabilidad social de la empresa e impacto de género en los órganos de administración

A) Consecuencias de la fusión sobre el empleo.

Tras la fusión por creación descrita, se mantienen todas las relaciones laborales existentes entre las sociedades que se fusionan, subrogándose la sociedad de nueva creación [DENOMINACIÓN SOCIAL] en los derechos y obligaciones laborales y de Seguridad Social de las sociedades que se desaparecen,

B) Órgano de administraciónresultante de la fusión.

Tal y como se establece en los estatutos sociales que se [ELEGIR: reproducen / anexan] al presente proyecto de fusión, la sociedad de nueva creación [DENOMINACIÓN SOCIAL], [OTROS DATOS] estará administrada por [ELEGIR: un administrador único / administradores solidarios / administradores mancomunados / un consejo de administración]

Los administrador/es de la sociedad de nueva creación [DENOMINACIÓN SOCIAL] quedará/n expresamente facultados para realizar, en nombre de la nueva sociedad, antes de la inscripción de ésta en el Registro Mercantil, cuantos actos de administración o de dominio sean necesarios o convenientes para la realización del objeto social, como el otorgamiento y revocación de poderes de todas clases. De forma que, una vez inscrita la fusión, la sociedad quedará obligada por tales actos sin necesidad de ratificación.

C) Incidencia en la responsabilidad social de la empresa.

Como consecuencia de la fusión, la sociedad de nueva creación [DENOMINACIÓN SOCIAL], asumirá las deudas sociales de las empresas que se extinguen sin perjuicio de los derechos regulados en el artículo 13 del Real Decreto-ley 5/2023 en favor de los acreedores.

[OPCIONAL — incluir si procede]

Ninguna de las sociedades que participan en este proceso de fusión cuentan con socios con responsabilidad personal, no siendo por ello de aplicación el régimen de responsabilidad extraordinario recogido en el art.52 del Real Decreto-ley 5/2023.

Decimotercero.- Otros efectos

[OPCIONAL — incluir si procede]

A) Amortización de [ELEGIR: participaciones / acciones / cuotas] propias o recíprocas.

Las [ELEGIR: participaciones / acciones / cuotas], de las sociedades participantes en el proceso de fusión, que estuvieran en poder de cualquiera de ellas o en el de otras personas que actuasen por cuenta de esas sociedades, no podrán canjearse por [ELEGIR: participaciones / acciones / cuotas], de la sociedad resultante de la fusión y deberán ser amortizadas o extinguidas.

Su valor en el patrimonio de la sociedad ha sido tenido en cuenta para calcular la relación o tipo de canje.

[OPCIONAL — incluir si procede]

B) Régimen fiscal especial.

• 1.º La fusión tiene como finalidad [CAUSA].

• 2.º Esta operación de fusión puede acogerse al régimen especial establecido en el Capítulo VII del Título VII de la Ley 27/2014, de 27 de noviembre del Impuesto sobre Sociedades.

Decimocuarto.- Lugar y fecha.

Este proyecto de fusión es suscrito en [LUGAR], a [FECHA],

Se procede a la firma de este proyecto de fusión por todos los administradores de las sociedades que se fusionan.

1.º Firmas de los administradores de la sociedad « [DENOMINACIÓN SOCIAL], »

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

2.º Firmas de los administradores de la sociedad « [DENOMINACIÓN SOCIAL], »

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS]

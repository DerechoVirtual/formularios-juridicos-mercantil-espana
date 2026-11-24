---
name: estatutos-sociales-sociedad-comanditaria-acciones-mer-0455
description: "Estatutos sociales de una sociedad comanditaria por acciones. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Estatutos sociales de una sociedad comanditaria por acciones

> Formulario **MER-0455** del plugin **Cooperativas, sociedades laborales y otras formas de empresa** (`formularios-cooperativas-y-otras-sociedades`) · Mercantil › Cooperativas, sociedades laborales y otras formas societarias · normativa revisada el 24-11-2026.

## Qué es

Modelo para la creación de estatutos sociales para una Sociedad Comanditaria por Acciones, en los que se concretan las bases de organización y funcionamiento de la sociedad, tales como la duración, domicilio, objeto y capital social, socio gestor, participación de los socios y disolución de la misma.

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Estatutos sociales de una sociedad comanditaria por acciones» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Estatutos sociales de una sociedad comanditaria por acciones” para mi caso». También puedes invocarla directamente con `/formularios-cooperativas-y-otras-sociedades:estatutos-sociales-sociedad-comanditaria-acciones-mer-0455`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-cooperativas-y-otras-sociedades:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Cooperativas, sociedades laborales y otras formas de empresa) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] Nº (18 veces)
- [ ] IMPORTE (7 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] CLASE (2 veces)
- [ ] CLASE DE ACCIONES (2 veces)
- [ ] CALLE
- [ ] DENOMINACIÓN SOCIAL
- [ ] OBJETO SOCIAL
- [ ] PERIODICIDAD

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

Modelo para la creación de estatutos sociales para una Sociedad Comanditaria por Acciones, en los que se concretan las bases de organización y funcionamiento de la sociedad, tales como la duración, domicilio, objeto y capital social, socio gestor, participación de los socios y disolución de la misma.


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

TÍTULO I.- DENOMINACIÓN, DURACIÓN, DOMICILIO y OBJETO

Artículo 1º. - Constitución.

La presente Sociedad Comanditaria por Acciones se regirá por su correspondiente contrato constitutivo, por los presentes estatutos, y en lo en ellos no dispuesto, por el Texto Refundido de la Ley de Sociedades de Capital así como por cuantas demás disposiciones resulten de aplicación.

Artículo 2º. - Denominación.

La Sociedad se denomina ‘, S.Com.por A.’.

Artículo 3º. - Duración.

La Sociedad tendrá una duración de carácter indefinido, dando comienzo al inicio de sus operaciones el día siguiente al del otorgamiento de la escritura de constitución, sin perjuicio de las consecuencias legales previstas para los actos y contratos celebrados en nombre de la Sociedad con anterioridad a su inscripción en el Registro Mercantil.

Los ejercicios sociales se computarán por años naturales.

Artículo 4º. - Domicilio.

El domicilio de la Sociedad se localiza en [LOCALIDAD], calle [CALLE] de [LOCALIDAD]

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

El órgano de administración podrá crear, suprimir o trasladar sucursales, así como cambiar el domicilio social dentro del Territorio Nacional.

El órgano de administración podrá crear, suprimir o trasladar sucursales. Los administradores no ostentan la competencia para cambiar el domicilio social, siendo este acuerdo de exclusiva competencia de la Junta de socios

Artículo 5º. - Objeto social.

El objeto social de la Sociedad será [OBJETO SOCIAL].

TITULO II.- CAPITAL SOCIAL

Artículo 6º. - Capital social.

El capital social se cifra en [IMPORTE] euros, totalmente suscrito y desembolsado por los socios fundadores en el acto de otorgamiento de la escritura de constitución, habiendo realizado cada uno de ellos las aportaciones que se describen a continuación:

[OPCIONAL — incluir si procede]

(Si se trata de aportaciones dinerarias)
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], aporta en efectivo por su valor nominal conjunto [IMPORTE] y suscribe [Nº] acciones, que son las numeradas [Nº] a [Nº]

[ELEGIR UNA OPCIÓN: Cuando exista ingreso previo / Cuando la entrega del efectivo se hace directamente al notario]

[OPCIONAL — incluir si procede]

(Si se trata de aportaciones no dinerarias)
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] aporta a la sociedad [DENOMINACIÓN SOCIAL] con el consentimiento de su cónyuge [NOMBRE Y APELLIDOS],(el bien que corresponda o la mitad indivisa), valorado en ", equivalente al - valor nominal de las acciones números

La totalidad de estas aportaciones ha sido realizada a título de propiedad, en pleno dominio, con todos sus derechos inherentes y accesorios y libres de toda carga y gravamen, arrendamientos, responsabilidad u otras afecciones.

En prueba de todo ello los comparecientes me entregan para unir a la presente documentación, a lo cual procedo, los correspondientes informes emitidos por el/los experto/s independiente/s nombrados a tal fin por el Registrador Mercantil de [LOCALIDAD] D./Dña. [NOMBRE Y APELLIDOS], en los que se describen y valoran las citadas aportaciones no dinerarias

[OPCIONAL — incluir si procede]

(Si se trata de aportaciones mixtas)
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS] con el consentimiento de su cónyuge, efectúa las siguientes aportaciones a la sociedad:

a). Dineraria: [IMPORTE] euros en efectivo metálico, correspondiente al - valor nominal de las acciones números " de [Nº] a [Nº].

b). No dineraria "(el bien que corresponda o la mitad indivisa), por su valor de [IMPORTE] correspondiente al valor nominal- de las acciones números [Nº] de [Nº] a [Nº]. Esta aportación no dineraria ha sido realizada a título de propiedad, en pleno dominio, con todos sus derechos inherentes y accesorios y libres de toda carga y gravamen, arrendamientos, responsabilidad u otras afecciones. Se anexa a la presente escritura el informe sobre la valoración de esta aportación.

Artículo 7º. - Acciones.

El capital social se halla dividido en [Nº] acciones, de las cuales [Nº] acciones corresponden a la clase [CLASE] y acciones corresponden a la clase [CLASE].

Las ACCIONES DE LA CLASE [CLASE DE ACCIONES] son las correspondientes al/ a los socio/s colectivo/s, y se trata de [Nº] acciones nominativas de [IMPORTE] euros de valor nominal cada una de ellas. Se encuentran totalmente desembolsadas, y están numeradas correlativamente con los números [Nº] al [Nº], ambos inclusive. Estas acciones no pueden transmitirse a terceras personas que no tengan la cualidad de socio colectivo sin el consentimiento de los restantes socios colectivos.

Las ACCIONES DE LA CLASE [CLASE DE ACCIONES] son las correspondientes a los socios comanditarios, y se trata de [Nº] acciones nominativas/al portador de [IMPORTE] euros de valor nominal cada una de ellas. Se encuentran totalmente desembolsadas, y están numeradas correlativamente con los números [Nº] al [Nº], ambos inclusive.

La modificación de la condición de socio, de colectivo a comanditario o viceversa, supondrá la correspondiente conversión del tipo de acciones de que en cada caso se sea titular.

TÍTULO III.- ÓRGANOS SOCIALES

Artículo 8º. - Administración.

El órgano de administración es el de administrador único, cargo que en todo caso deberá ser ostentado por un socio colectivo D./Dña. [NOMBRE Y APELLIDOS]. La duración del cargo será de [Nº] años, y quien lo desempeñe percibirá la cantidad de [IMPORTE] euros brutos anuales en concepto de retribución por el ejercicio de las funciones inherentes al mismo.

Artículo 9º. - Juntas de socios

Se reunirán [PERIODICIDAD] y adoptará los acuerdos según lo previsto en el Texto Refundido de la Ley de Sociedades de Capital, salvo disposición en contrario de los presentes estatutos.

TÍTULO IV.- MODIFICACIONES ESTATUTARIAS

Artículo 10º. - Modificaciones estatutarias.

Requerirán acuerdo de la junta general, adoptado con arreglo a lo previsto en la Ley de Sociedades de Capital, pero con las siguientes peculiaridades:

* Será preciso el consentimiento expreso de todos los socios colectivos cuando la modificación estatutaria tenga por objeto:

[OPCIONAL — incluir si procede]

- El nombramiento de administradores,

[OPCIONAL — incluir si procede]

- La modificación del régimen de administración,

[OPCIONAL — incluir si procede]

- El cambio del objeto social,

[OPCIONAL — incluir si procede]

- La continuación de la sociedad más allá del término previsto en los estatutos,

* En los acuerdos que tengan por objeto la separación de un administrador, el socio afectado deberá abstenerse de participar en la votación.

TÍTULO V.- EXTINCIÓN

Artículo 11º. - Disolución.

Además de por las causas de disolución previstas en la Ley de Sociedades de Capital, la sociedad se disolverá por fallecimiento, cese, incapacidad o apertura de la fase de liquidación en el concurso de todos los socios colectivos, salvo que en el plazo de [Nº] meses y mediante modificación de los estatutos se incorpore algún socio colectivo, o se acuerde la transformación de la sociedad en otro tipo social.

Artículo 12º. - Liquidación

La disolución de la sociedad abrirá el periodo de liquidación, excepto en los supuestos de modificación estructural como la fusión, la escisión total o la cesión global de activo y pasivo. Salvo disposición contraria en los estatutos, quienes fueren administradores al tiempo de la disolución quedarán convertidos en liquidadores. No obstante, la Junta General podrá nombrar a los liquidadores, fijando su número, que deberá ser impar, y las reglas de su actuación. Dicho nombramiento requerirá la misma mayoría que la exigida para el acuerdo de disolución.

Corresponde a los liquidadores la gestión y representación de la sociedad en liquidación con el fin de llevar a término las operaciones liquidatorias. En particular, deberán: a) Formular un inventario y un balance de la sociedad con referencia al día en que se hubiera disuelto. b) Concluir las operaciones pendientes y realizar las nuevas que sean necesarias para la liquidación. c) Percibir los créditos sociales y pagar las deudas sociales. d) Enajenar los bienes sociales. Para la venta de bienes inmuebles, los liquidadores actuarán con la diligencia de un ordenado empresario, eligiendo el procedimiento que consideren más beneficioso para los intereses de la sociedad, sin que sea preceptiva la pública subasta. e) Informar periódicamente a los socios y a los acreedores del estado de la liquidación. f) Someter a la aprobación de la Junta General un balance final, un informe completo sobre las operaciones de liquidación y un proyecto de división del activo resultante.

Una vez satisfechos los acreedores, el patrimonio resultante se repartirá entre los socios en proporción a su participación en el capital social. Salvo acuerdo unánime de los socios, estos tendrán derecho a percibir en dinero la cuota resultante de la liquidación, de acuerdo con lo establecido en el Artículo 393 del Texto refundido de la Ley de Sociedades de Capital.

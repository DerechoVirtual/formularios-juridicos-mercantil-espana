---
name: contrato-cesion-credito-frente-sociedad-concurso-mer-0808
description: "Contrato de cesión de un crédito frente a una sociedad en concurso. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de cesión de un crédito frente a una sociedad en concurso

> Formulario **MER-0808** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Contrato por el que se transmite el crédito que ostenta una sociedad frente a otra declarada en concurso. Mediante este pacto extrajudicial se comunican los efectos tanto a la Administración Concursal como al Consejo de Administración de la sociedad deudora e inmersa en el proceso concursal.

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de cesión de un crédito frente a una sociedad en concurso» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de cesión de un crédito frente a una sociedad en concurso” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:contrato-cesion-credito-frente-sociedad-concurso-mer-0808`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (14 veces)
- [ ] LOCALIDAD (11 veces)
- [ ] DENOMINACIÓN SOCIAL (10 veces)
- [ ] DNI/NIE (8 veces)
- [ ] CALLE (7 veces)
- [ ] FECHA (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] NOMBRE DE LA PARTE (4 veces)
- [ ] LUGAR (3 veces)
- [ ] Nº (3 veces)
- [ ] ACTO O RESOLUCIÓN (2 veces)
- [ ] HOJA (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] CÓDIGO POSTAL
- [ ] DIRECCIÓN
- [ ] NIF
- [ ] NÚMERO
- [ ] SEDE
- [ ] SUCURSAL
- [ ] TIPO Y Nº DE PROCEDIMIENTO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 352 TRLC

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

Contrato por el que se transmite el crédito que ostenta una sociedad frente a otra declarada en concurso. Mediante este pacto extrajudicial se comunican los efectos tanto a la Administración Concursal como al Consejo de Administración de la sociedad deudora e inmersa en el proceso concursal.


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

En [LUGAR], a [FECHA]
REUNIDOS

DE UNA PARTE,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos de CEDENTE)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CEDENTE.

Y DE OTRA,

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Datos del CESIONARIO)

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de estado civil [ELEGIR: soltero / soltera / casado / casada / divorciado / divorciada / separado / separada / viudo / viuda], de nacionalidad [NACIONALIDAD], con domicilio en [LOCALIDAD], y DNI/Pasaporte número [DNI/NIE].

[OPCIONAL — en caso de estado civil casado/a]

[ELEGIR: Casado / Casada]con D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI/Pasaporte número [DNI/NIE] en régimen económico matrimonial de [ELEGIR: gananciales / separación de bienes].

En lo sucesivo, CESIONARIO.

INTERVIENEN

[ELEGIR UNA OPCIÓN: en caso de que todas las partes actúen en nombre y representación propia / si alguna de las partes actúa en su propio nombre y representación]

[OPCIONAL — si alguna de las partes actúa en nombre y representación de persona física o jurídica]
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], en nombre y representación de:

[ELEGIR UNA OPCIÓN: Si se trata de persona física / Si se trata de una persona jurídica]

EXPONEN

(i) Que el CEDENTE es titular de un derecho de crédito por importe de [IMPORTE] euros, frente a la mercantil [DENOMINACIÓN SOCIAL], con NIF [NIF], con domicilio social en Calle [CALLE] de [LOCALIDAD].
(ii) En adelante [ÓRGANO], será denominada a los efectos de este contrato como «el DEUDOR», y el crédito que por importe de [IMPORTE] euros mantiene el CEDENTE frente al DEUDOR será denominado «el DERECHO DE CRÉDITO».
(iii) Que el DEUDOR se encuentra declarado en situación de concurso de acreedores. Dicho concurso es tramitado por la Plaza núm. 1 de la Sección de la Mercantil del Tribunal de Instancia de [SEDE], bajo el núm. [Nº] de autos [TIPO Y Nº DE PROCEDIMIENTO]. En el marco de dicho procedimiento, la Administración Concursal designada por el tribunal presentó, con fecha [FECHA], la lista definitiva de acreedores concursales del DEUDOR, constando como acreedor el CEDENTE por el referido importe de [IMPORTE] euros. Asimismo, en dicho procedimiento concursal se ha dictado Auto poniendo fin a la fase común del concurso y abriendo la fase de convenio.
(iv) Que el CEDENTE está interesado en transmitir al CESIONARIO el DERECHO DE CRÉDITO que ostenta frente al DEUDOR, y el CESIONARIO está interesado en su adquisición, a cuyos efectos ambas partes, reconociéndose mutuamente capacidad para este acto, acuerdan suscribir el presente CONTRATO DE CESIÓN DE CRÉDITO, que se regirá por las siguientes,

ESTIPULACIONES

Primera.- Cesión del derecho de crédito

1.1. Por medio del presente contrato el CEDENTE cede y transmite al CESIONARIO, quien correlativamente lo adquiere, el DERECHO DE CRÉDITO frente al DEUDOR.

Segunda.- Precio

2.1. El precio de la presente cesión se fija en el 50% del valor nominal del DERECHO DE CRÉDITO, es decir, en la cantidad de [IMPORTE] euros.

Tercera.- Pago del precio

3.1. El CESIONARIO satisface en este acto al CEDENTE el precio de la cesión mediante entrega del cheque núm. [NÚMERO], copia del cual las partes convienen unir a este contrato como Anexo I.

3.2. Con la entrega de dicho cheque, el CEDENTE manifiesta que se da por íntegramente satisfecho de cuántas pretensiones económicas pudiera tener frente al DEUDOR, sin que tenga nada más que reclamarle.

Cuarta.- Garantías del CEDENTE

4.1. La transmisión del DERECHO DE CRÉDITO se hace con todos sus derechos inherentes y accesorios, respondiendo el CEDENTE frente al CESIONARIO de su existencia y legitimidad, pero no de la solvencia del DEUDOR.

Quinta.- Manifestación del CESIONARIO

5.1. El CESIONARIO expresamente manifiesta conocer los efectos que sobre el DERECHO DE CRÉDITO pueden producirse como consecuencia de la situación concursal que afecta al DEUDOR.

5.2. El CESIONARIO manifiesta asimismo conocer que, en virtud de lo dispuesto en el art. 352 TRLConc, puede verse privado de derecho de voto en la Junta de Acreedores del DEUDOR en cuanto titular de un DERECHO DE CRÉDITO adquirido después de la declaración de concurso.

Sexta.- Comunicación al DEUDOR

6.1. Las partes acuerdan comunicar al DEUDOR la cesión del DERECHO DE CRÉDITO operada por medio del presente contrato, a cuyos efectos el CEDENTE faculta al CESIONARIO para que se encargue de enviar, mediante burofax con acuse de recibo y certificación de texto, las comunicaciones que se adjuntan a este contrato como Anexos II y III, dirigidas tanto al órgano de administración del DEUDOR como a su Administración Concursal.

Séptima.- Ley aplicable y jurisdicción competente

7.1. El presente contrato queda sometido a la Ley española.

7.2. Con expresa renuncia a cualquier otro fuero que pueda corresponderles, las partes acuerdan someter todo conflicto, controversia o reclamación en relación con la interpretación, validez, exigibilidad, incumplimiento, cumplimiento, resolución o efectos de este contrato a los Tribunales de la ciudad de

Y en prueba de conformidad con todo lo anterior, los reunidos, en la representación que ostentan, firman el presente contrato en duplicado ejemplar y a un solo efecto en el lugar y fecha indicada en el encabezamiento.

EL CEDENTE	EL CESIONARIO

D./Dña. [NOMBRE Y APELLIDOS] ()	D./Dña. [NOMBRE Y APELLIDOS] ()
ANEXO II

A la atención de la Administración Concursal de [DENOMINACIÓN SOCIAL],

En la persona de:

D./Dña. [NOMBRE Y APELLIDOS].

Administrador/a Concursal Letrado

C/ [CALLE]

En [LUGAR], a [FECHA].

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad española, con DNI núm. [DNI/NIE], y domicilio en Calle [CALLE] núm. [Nº] de [LOCALIDAD] de [PROVINCIA], con mismo domicilio, constituida e inscrita en el Registro Mercantil de [LOCALIDAD], Hoja [HOJA].

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad española, con DNI [DNI/NIE] y domicilio en la Calle [CALLE], de [LOCALIDAD], Consejero Delegado de la compañía [DENOMINACIÓN SOCIAL], con mismo domicilio, constituida e inscrita en el Registro Mercantil de [LOCALIDAD].

Por la presente informan a la administración concursal de [DENOMINACIÓN SOCIAL]:

Que en las listas definitivas de acreedores concursales de [DENOMINACIÓN SOCIAL] presentadas ante el Tribunal por esa Administración Concursal el pasado [FECHA], aparecía como acreedor reconocido [NOMBRE DE LA PARTE], con un crédito por importe de <> euros.

Que [NOMBRE DE LA PARTE], en virtud del contrato de cesión de crédito celebrado entre ambas partes el día de hoy, ha cedido la totalidad del referido crédito que tenía frente a [ACTO O RESOLUCIÓN], a la compañía [DENOMINACIÓN SOCIAL], lo que, de común acuerdo ponen en conocimiento de esa administración concursal, a los efectos oportunos.

Atentamente.

D./Dña. [NOMBRE Y APELLIDOS] D./Dña. [NOMBRE Y APELLIDOS]

ANEXO III

A la atención del Consejo de Administración de [DENOMINACIÓN SOCIAL]

Calle [CALLE]

Edificio [DIRECCIÓN]

Oficina [SUCURSAL]

En [LUGAR], a [FECHA].

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad española, con DNI núm. [DNI/NIE], y domicilio en Calle [CALLE] núm. [Nº] de [LOCALIDAD], [CÓDIGO POSTAL] de [PROVINCIA], con mismo domicilio, constituida e inscrita en el Registro Mercantil de [LOCALIDAD], Hoja [HOJA].

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, de nacionalidad española, con DNI [DNI/NIE] y domicilio en la Calle [CALLE], de [LOCALIDAD], Consejero Delegado de la compañía [DENOMINACIÓN SOCIAL], con mismo domicilio, constituida e inscrita en el Registro Mercantil de [LOCALIDAD].

Por la presente informan al Consejo de Administración de [DENOMINACIÓN SOCIAL]:

Que en las listas definitivas de acreedores concursales de [DENOMINACIÓN SOCIAL], presentadas ante el Tribunal por la Administración Concursal el pasado [FECHA], aparecía como acreedor reconocido [NOMBRE DE LA PARTE], con un crédito por importe de [IMPORTE] euros.

Que [NOMBRE DE LA PARTE], en virtud del contrato de cesión de crédito celebrado entre ambas partes el día de hoy, ha cedido la totalidad del referido crédito que tenía frente a [ACTO O RESOLUCIÓN], a la compañía <(S.L.)>, lo que, de común acuerdo ponen en conocimiento de ese Consejo de Administración, a los efectos oportunos.

Atentamente.

D./Dña D./Dña

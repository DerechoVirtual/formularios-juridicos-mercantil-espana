---
name: contrato-externalizacion-servicios-outsourcing-entre-mer-0545
description: "Contrato de externalización de servicios (outsourcing) entre empresas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de externalización de servicios (outsourcing) entre empresas

> Formulario **MER-0545** del plugin **Contratos mercantiles: compraventa, suministro, transporte y servicios** (`formularios-contratos-mercantiles`) · Mercantil › Compraventa mercantil, suministro, transporte y servicios · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de externalización de servicios (outsourcing) entre empresas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de externalización de servicios (outsourcing) entre empresas” para mi caso». También puedes invocarla directamente con `/formularios-contratos-mercantiles:contrato-externalizacion-servicios-outsourcing-entre-mer-0545`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-mercantiles:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos mercantiles: compraventa, suministro, transporte y servicios) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] PLAZO (4 veces)
- [ ] CALLE (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] DÍA
- [ ] FECHA
- [ ] FOLIO
- [ ] LIBRO
- [ ] MES
- [ ] Nº DE CUENTA (IBAN)
- [ ] NÚMERO DE LA CALLE
- [ ] OBJETO DEL CONTRATO
- [ ] TIPO DE INTERÉS
- [ ] TOMO
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 61.2 Ley 22/2003

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

- Junto a «…rato de acuerdo con el artículo 61.2 de la Ley 22/2003, de 9 de julio, Concursal»: La Ley 22/2003, Concursal, está derogada; hoy rige el texto refundido de la Ley Concursal (RDLeg 1/2020, reformado por la Ley 16/2022). Hay que citar el artículo equivalente del TRLC. Fuente: RDLeg 1/2020, disposición derogatoria única.
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

En [LOCALIDAD], a [DÍA] de [MES] 20 [AÑO]

Comparecen:

De una parte [NOMBRE Y APELLIDOS], como EMPRESA COLABORADORA (persona física o jurídica)

(Persona física: D/D.ª [NOMBRE Y APELLIDOS] mayor de edad, casado, con domicilio en [LOCALIDAD] c/ [CALLE] núm. con DNI/NIF núm. [DNI/NIE])

(Persona jurídica: constituída en escritura pública otorgada el día [FECHA] ante Notario de [LOCALIDAD] D/D.ª [NOMBRE Y APELLIDOS] e inscrita en el Registro Mercantil de [LOCALIDAD] Libro [LIBRO] Tomo [TOMO] Folio [FOLIO] domiciliada en [DOMICILIO] calle [CALLE] núm. [NÚMERO DE LA CALLE] y con CIF núm. representada por [ÓRGANO O PERSONA], mayor de edad, con domicilio en [LOCALIDAD] c/ [CALLE] núm. con DNI/NIF núm. cuyas facultades derivan del poder otorgando por el notario D/D.ª [NOMBRE Y APELLIDOS], debidamente inscrito, que es declarado vigente y sin modificación alguna)

De otra parte, como CLIENTE (persona física o jurídica)

Ambas partes se reconocen con carácter mutuo y tienen capacidad legal suficiente para otorgar el presente contrato de colaboración empresarial externa u outsourcing.

Convienen

1. Disposiciones generales: a) La EMPRESA COLABORADORA es una sociedad dedicada a prestar servicios de … (detallar actividad); b) el CLIENTE es una sociedad cuya actividad principal consiste en [ACTIVIDAD]; c) el CLIENTE requiere de los servicios de la EMPRESA COLABORADORA; d) el CLIENTE y la EMPRESA COLABORADORA celebran el presente acuerdo por el cual se procederá a la prestación de servicios mediante contraprestación.

2. Objeto. En virtud de este contrato, la EMPRESA COLABORADORA se obliga a prestar los servicios de [OBJETO DEL CONTRATO], incluyendo asistencia técnica para su correcto mantenimiento de los productos suministrados por la EMPRESA COLABORADORA, siendo de cuenta del CLIENTE los costes relativos a las piezas que hayan de sustituirse.

3. Plazo para la prestación del servicio. La EMPRESA COLABORADORA se compromete a acudir a las instalaciones del CLIENTE en el plazo de [PLAZO] y a reparar o sustituir el/los equipo/s dañados en el plazo de [PLAZO].

4. Contraprestación. El precio por la prestación de los servicios detallados en el apartado 2 ascienden a la cantidad de [IMPORTE], que se abonarán en el número de cuenta bancaria [Nº DE CUENTA (IBAN)], a nombre de la EMPRESA COLABORADORA, durante los diez primeros días de cada mes.

En caso de renovación del contrato conforme a lo establecidos en el apartado 4, se procederá a una actualización de la contraprestación de acuerdo a los índices habitualmente manejados.

5. Duración del contrato. Este contrato tiene una duración anual, y puede ser objeto de renovación automática en el caso de que ninguna de las partes proceda a su denuncia con al menos un mes de antelación a la fecha de su finalización.

6. Prohibición de subcontratación. Las prestaciones recogidas en el presente contrato han de ser ejecutadas directamente por la EMPRESA COLABORADORA. Queda prohibida la posibilidad de subcontratación de los servicios comprometidos.

7. Confidencialidad. Las partes contratantes quedan obligadas recíprocamente a mantener en secreto los datos relativos a cada una de las partes, que pudieran obtener como consecuencia de la ejecución de este contrato. Sin previo consentimiento por escrito de la otra parte no podrán revelar dato alguno. Este deber de confidencialidad se extiende a todos los empleados, debiendo la EMPRESA COLABORADORA y el CLIENTE responder de sus actuaciones.

El deber de confidencialidad permanece una vez finalizado el contrato durante [PLAZO].

8. Terminación y resolución del contrato. Se consideran causas de resolución de este contrato: a) la terminación de la relación, bien por haber concluido el tiempo pactado, por haberse ejecutado completamente su objeto o por acuerdo de las partes; b) por incumplimiento de cualquiera de las cláusulas del contrato sin subsanación por parte del incumplidor en el periodo de [PLAZO] desde que le fuera notificado por escrito dicho incumplimiento.

La declaración de concurso de cualquiera de las partes obliga a solicitar a la parte afectada la resolución del contrato de acuerdo con el artículo 61.2 de la Ley 22/2003, de 9 de julio, Concursal .

Con independencia de las cláusulas generales de resolución, el impago de cualquiera de las mensualidades del presente contrato dará derecho a al EMPRESA COLABORADORA a reclamar judicialmente la resolución del contrato y solicitar la correspondiente indemnización por daños y perjuicios. Se pacta un interés de demora de [TIPO DE INTERÉS] desde la fecha del incumplimiento. Igual facultad se otorga al CLIENTE en el supuesto de que la EMPRESA COLABORADORA no cumpla con sus obligaciones, pactándose una indemnización para el CLIENTE equivalente a [IMPORTE].

9. Gastos. Todos los gastos, impuestos, contribuciones, tasas arbitrios, presentes o futuros, originados por el presente contrato, serán satisfechos a partes iguales por ambas partes.

10. Elevación a documento público. Cualquiera de las partes puede solicitar la elevación a documento público del presente contrato, debiendo el solicitante hacer frente a los gastos derivados de la elevación.

11. Arbitraje. Las partes se comprometen a acudir a un arbitraje de Derecho privado, conforme a la legislación vigente, para dirimir todos los posibles conflictos que entre ellas pudiera surgir, en particular, como consecuencia de la interpretación o incumplimiento del presente contrato. Las partes renuncian expresamente al ejercicio de cualquiera acción ante tribunales.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

EMPRESA COLABORADORA

CLIENTE

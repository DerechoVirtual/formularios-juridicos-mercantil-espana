---
name: escritura-hipoteca-naval-mer-0643
description: "Escritura de hipoteca naval. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de hipoteca naval

> Formulario **MER-0643** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de hipoteca naval» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de hipoteca naval” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:escritura-hipoteca-naval-mer-0643`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (6 veces)
- [ ] IMPORTE (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] CALLE (3 veces)
- [ ] FECHA (3 veces)
- [ ] OTROS DATOS (3 veces)
- [ ] TIPO DE INTERÉS (2 veces)
- [ ] ÓRGANO (2 veces)
- [ ] ASEGURADORA
- [ ] COLEGIO
- [ ] DENOMINACIÓN DEL BUQUE
- [ ] DIMENSIONES (ESLORA, MANGA, PUNTAL)
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] EMPRESA Y LUGAR DE CONSTRUCCIÓN
- [ ] FOLIO
- [ ] FORMA DE AMORTIZACIÓN
- [ ] GASTOS A CARGO DEL PRESTATARIO
- [ ] LIBRO
- [ ] LUGAR Y FORMA DE PAGO
- [ ] MARCA/MODELO
- [ ] MATRÍCULA
- [ ] MOTOR
- [ ] NÚMERO DE LA CALLE
- [ ] SEÑAL DISTINTIVA
- [ ] TOMO
- [ ] TONELAJE
- [ ] ÓRGANO O PERSONA

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

En [LOCALIDAD], a fecha de [FECHA]

Y ante [ÓRGANO], Notario del Ilustre Colegio de [COLEGIO]

Comparecen:

De una parte [NOMBRE Y APELLIDOS], como DEUDOR HIPOTECANTE (persona física o jurídica)

(Persona fisica: D/D.ª [NOMBRE Y APELLIDOS] mayor de edad, casado, con domicilio en [LOCALIDAD] c/ [CALLE] núm. con DNI/NIF núm. [DNI/NIE])

(Persona jurídica: constituída en escritura pública otorgada el día [FECHA] ante Notario de [LOCALIDAD] D/D.ª [NOMBRE Y APELLIDOS] e inscrita en el Registro Mercantil de [LOCALIDAD] Libro [LIBRO] Tomo [TOMO] Folio [FOLIO] domiciliada en [DOMICILIO] calle [CALLE] núm. [NÚMERO DE LA CALLE] y con CIF núm. representada por [ÓRGANO O PERSONA], mayor de edad, con domicilio en [LOCALIDAD] c/ [CALLE] núm. con DNI/NIF núm. cuyas facultades derivan del poder otorgando por el notario D/D.ª [NOMBRE Y APELLIDOS], debidamente inscrito, que es declarado vigente y sin modificación alguna)

De otra parte, como ACREEDOR (persona física o jurídica).

Cláusulas

1. Buque. El DEUDOR HIPOTECANTE se declara propietario del buque que a continuación se detalla y respecto del que se constituirá la correspondiente hipoteca.

1.1 Denominación [DENOMINACIÓN DEL BUQUE];

1.2 Matrícula [MATRÍCULA];

1.3 Modelo [MARCA/MODELO];

1.4 Empresa y lugar de construcción [EMPRESA Y LUGAR DE CONSTRUCCIÓN];

1.5 Dimensiones del buque y características técnicas: dimensiones: eslora, manga, puntal [DIMENSIONES (ESLORA, MANGA, PUNTAL)]; tonelaje [TONELAJE]; motor [MOTOR]; código internacional de señales, señal distintiva [SEÑAL DISTINTIVA];

1.6 Seguros [ASEGURADORA]

1.7 Otros posibles datos distintivos [OTROS DATOS].

1.8 Inscripción del buque: el buque se encuentra inscrito en el Registro mercantil de [LOCALIDAD] y en el Registro de matrícula de la Jefatura provincial de la marina mercante [ÓRGANO].

1.9 Título de propiedad: el buque cuya descripción se detalla pertenece por título de propiedad al DEUDOR HIPOTECANTE, por contrato de compraventa formalizado ante notario [NOMBRE Y APELLIDOS].

1.10. Cargas de buque: el DEUDOR HIPOTECANTE declara que el buque no está sujeto a ninguna carga o gravamen y está asimismo libre de arrendatarios.

2. Préstamo. Características particulares: 1. Capital del préstamo [IMPORTE]; 2 amortización del préstamos [FORMA DE AMORTIZACIÓN]; 3. intereses [TIPO DE INTERÉS]; 4. comisiones [IMPORTE]; 5.gastos a cargo del prestatario [GASTOS A CARGO DEL PRESTATARIO]; 6. intereses de demora [TIPO DE INTERÉS]; 7. lugar y forma de pago [LUGAR Y FORMA DE PAGO]; 8. otras posibles cláusulas [OTROS DATOS].

3. Constitución de la hipoteca naval. Sin perjuicio de la responsabilidad personal e ilimitada del DEUDOR HIPOTECANTE, se constituye la siguiente hipoteca naval, sobre el buque descrito en la cláusula 1, a favor del ACREEDOR en garantía de la devolución del capital prestado, los intereses y los intereses de demora, por un importe de [IMPORTE], más las costas y gastos por importe de [IMPORTE].

4. Alcance de la hipoteca naval. La presente hipoteca alcanza al buque hipotecado y a cada uno de los conceptos establecidos en el artículo 134 de la Ley de Navagación Marítima (Se entenderán hipotecados juntamente con el casco del buque y responderán de los compromisos anejos a la hipoteca, salvo pacto expreso en contrario, el aparejo, respetos, pertrechos y máquinas, si fuere de vapor, que se hallen, a la sazón del dominio del dueño o dueños de la nave hipotecada; los fletes devengados y no percibidos por el viaje que estuviera haciendo, o el último que hubiere rendido al hacerse efectivo el crédito hipotecario; las indemnizaciones que al buque correspondan por abordaje u otros accidentes que den lugar a aquéllas y por la del seguro, caso de siniestro.) La hipoteca se extiende igualmente a las posibles obras y mejores que se realicen en el buque.

5. Duración de la hipoteca. El plazo de duración de la garantía hipotecaria estará vigente hasta el día [FECHA].

6. Vencimiento anticipado de la hipoteca naval. Sin perjuicio de lo señalado en la cláusula núm. 5, este plazo podrá extinguirse anticipadamente en los supuestos siguientes: 1. Incumplimiento de obligaciones: cualquiera de las derivadas de la póliza de préstamo o de la relación principal garantizada con la hipoteca. 2. Imposibilidad de inscripción de la hipoteca en el Registro mercantil. 3. Concurso del ACREEDOR HIPOTECANTE. 4. Destrucción o pérdida del buque. 5. Inutilización del buque para navegar. 6. Venta del buque a un extranjero. 7. Otros posibles supuestos de vencimiento anticipado [OTROS DATOS].

7. Obligaciones del deudor hipotecante. El DEUDOR HIPOTECANTE queda obligado a: 1. conservar el buque hipotecado con la diligencia de un buen padre de familia, debiendo realizar todas las obras de restauración y reforma que se consideren convenientes. 2. realizar todos los pagos que resulten necesarios para mantener el buque al corriente de todos los impuestos y contribuciones que sobre el buque pueden recaer pueden recaer. 3. no constituir sin el consentimiento del ACREEDOR un arrendamiento sobre el buque hipotecado. 4. comunicar al ACREEDOR cualquier procedimiento de expropiación que pueda tener lugar sobre el buque hipotecado a través de cualquier medio que deje constancia de su recepción. En tal comunicación el DEUDOR HIPOTECANTE apoderará al ACREEDOR, con carácter irrevocable, para que realice todas las gestiones oportunas para la ejecución de la expropiación y el cobro del justiprecio. 5. realizar el correspondiente contrato de seguro de incendio y responsabilidad, así como sobre todos los posibles riesgos propios de la naturaleza del buque y del uso a que se destine durante la duración de esta garantía y por una suma igual, como mínimo, a la correspondiente a la garantía hipotecaria.

8. Ejecución de la hipoteca y ejecución de la hipoteca-valor a efectos de subasta. El ACREEDOR podrá ejercitar la acción personal o hipotecaria por cualquiera de los procedimientos legales existentes. Las partes, ACREEDOR y DEUDOR HIPOTECANTE, acuerdan dotar de carácter ejecutivo a la primera copia autorizada de esta escritura. Será suficiente el certificado del ACREEDOR para determinar la exigibilidad de la deuda conforme al saldo de la cuenta.

Las partes tasan el buque hipotecado a efectos de subasta en la siguiente cantidad [IMPORTE] €.

9. Gastos. Todos los gastos derivados de la formalización del presente documentos serán de cuenta del DEUDOR HIPOTECANTE.

10. Inscripción de la hipoteca naval. Corresponde al Registro Mercantil de la provincia en la que está matriculado el buque, proceder a la inscripción de la hipoteca, que en este acto se solicita.

11. Notificaciones. Los domicilios del ACREEDOR y del DEUDOR HIPOTECANTE, son válidos para la práctica de las notificaciones necesarias para la ejecución de esta hipoteca.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

EL DEUDOR HIPOTECANTE

EL ACREEDOR

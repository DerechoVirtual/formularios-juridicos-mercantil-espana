---
name: escritura-reconocimiento-deuda-prenda-sobre-mer-0631
description: "Escritura de reconocimiento de deuda y prenda sobre participaciones sociales de una SL. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escritura de reconocimiento de deuda y prenda sobre participaciones sociales de una SL

> Formulario **MER-0631** del plugin **Banca, financiación, valores y garantías** (`formularios-banca-financiacion-y-garantias`) · Mercantil › Banca, financiación, valores y garantías · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **estatutos, actas, certificaciones y escrituras**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escritura de reconocimiento de deuda y prenda sobre participaciones sociales de una SL» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escritura de reconocimiento de deuda y prenda sobre participaciones sociales de una SL” para mi caso». También puedes invocarla directamente con `/formularios-banca-financiacion-y-garantias:escritura-reconocimiento-deuda-prenda-sobre-mer-0631`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-banca-financiacion-y-garantias:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Banca, financiación, valores y garantías) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (17 veces)
- [ ] FECHA (5 veces)
- [ ] Nº (5 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NACIONALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PROFESIÓN (2 veces)
- [ ] CAUSA
- [ ] COLEGIO
- [ ] CÓDIGO CNAE
- [ ] DATOS REGISTRALES
- [ ] DENOMINACIÓN SOCIAL
- [ ] LUGAR
- [ ] NIF
- [ ] NOMBRE DE LA PARTE
- [ ] Nº DE PROTOCOLO
- [ ] OBJETO SOCIAL
- [ ] PROVINCIA
- [ ] TIPO DE INTERÉS

## Normas que cita el formulario

- art. 20 Ley 14/2013
- art. 1872 CC

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

Establecimiento de Prenda en garantía del cumplimiento de obligaciones de pago de socio deudor

NÚMERO DE PROTOCOLO:

En [LUGAR], a [FECHA].

Ante mí, D./Dña. [NOMBRE Y APELLIDOS], Notario del Ilustre Colegio de [COLEGIO].

COMPARECEN

De una parte:

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domiciliado en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO]. En adelante deudor pignorante

De otra parte:

D./Dña. [NOMBRE Y APELLIDOS], de estado civil [ELEGIR: soltero / soltera / divorciado / divorciada / separado judicialmente / separada judicialmente / viudo / viuda / casado / casada], con profesión [PROFESIÓN] de nacionalidad [NACIONALIDAD], con domiciliado en [DOMICILIO], y [ELEGIR: DNI / pasaporte / permiso de residencia] número [NÚMERO]. En adelante, acreedor pignoraticio

Intervienen todos en su propio nombre y derecho.

Les identifico por su citado [ELEGIR: DNI / pasaporte / permiso de residencia]. Tienen, a mi juicio, según intervienen, la capacidad legal necesaria para otorgar la presente ESCRITURA DE RECONOCIMIENTO DE DEUDA Y PIGNORACIÓN DE PARTICIPACIONES SOCIALES, a cuyo efecto,

EXPONEN

I. Que D./Dña. [NOMBRE Y APELLIDOS] es dueño, en pleno dominio y con carácter ganancial de [Nº] participaciones sociales, números [Nº] a [Nº], ambos inclusive, de la empresa [DENOMINACIÓN SOCIAL] Sociedad de Responsabilidad Limitada, S.R.L." constituida por tiempo indefinido por el Notario de esta ciudad, D./Dña. [NOMBRE Y APELLIDOS], el [FECHA], número de protocolo [Nº DE PROTOCOLO] y domicilio social en [LOCALIDAD] provincia de [PROVINCIA], [NIF] que tiene por objeto [OBJETO SOCIAL] correspondiente a la clasificación CNAE [CÓDIGO CNAE] de conformidad con el art. 20 de la Ley 14/2013 y está inscrita en el Registro Mercantil de [LOCALIDAD], al [DATOS REGISTRALES] con un capital social de [IMPORTE] euros, dividido en [Nº] participaciones sociales, de [IMPORTE] euros de valor nominal cada una de ellas. Su NIF es: ".

D./Dña. [NOMBRE Y APELLIDOS] adquirió las citadas participaciones sociales:

[OPCIONAL — incluir si procede]

(Constitución)

Por suscripción en la escritura de constitución descrita

[OPCIONAL — incluir si procede]

(Aumento de capital)

Por suscripción en la escritura de aumento de capital autorizada el [FECHA] por el Notario de [LOCALIDAD], D./Dña. [NOMBRE Y APELLIDOS], número de protocolo, la cual está debidamente inscrita en el Registro Mercantil.

[OPCIONAL — incluir si procede]

(Por compra)

Por compra a D./Dña. [NOMBRE Y APELLIDOS] antiguo socio de la compañía que fue, formalizada mediante escritura autorizada por el Notario de [LOCALIDAD],D./Dña. [NOMBRE Y APELLIDOS], el [FECHA], número de protocolo.

Justifica su adquisición mediante exhibición de certificado del Libro-Registro de socios de la sociedad, expedido por D./Dña. [NOMBRE Y APELLIDOS], el [FECHA] fotocopia del cual, concordante con su original, incorporo a la presente.

Las participaciones están libres de toda carga, responsabilidad o afección, según manifiesta la parte pignorante.

Asimismo, afirma que:

- No está prohibida estatutariamente la pignoración ni transmisión de las descritas participaciones sociales
- Las participaciones de las que es titular no están vinculadas a prestación accesoria alguna

II. Que los comparecientes convienen la pignoración de las participaciones indicadas mediante las siguientes,

ESTIPULACIONES

Primera. Reconocimiento de deuda y aplazamiento.

El "deudor pignorante D./Dña. [NOMBRE Y APELLIDOS] reconoce adeudar en favor de D./Dña. [NOMBRE Y APELLIDOS] el "acreedor", que lo ratifica y acepta, la cantidad global de [IMPORTE] euros, como consecuencia de [CAUSA].

Que ambas partes contratantes, acuerdan que el pago de la mencionada deuda se lleve a cabo de la siguiente forma [ELEGIR: aplazamiento total / fraccionamiento]:

[ELEGIR UNA OPCIÓN: Aplazamiento total / Fraccionamiento]

El aplazamiento devengará, en favor de la parte acreedora, un interés de [TIPO DE INTERÉS] que será abonado -en las fechas y por las cuantías obrantes en el cuadro incorporado- junto con los respectivos vencimientos de capital

Todos los pagos deberán ser satisfechos a la parte acreedora en efectivo metálico en el domicilio descrito en la comparecencia.

La falta de pago de cualquiera de los plazos pactados, o de sus intereses, determinará el vencimiento total de la deuda reconocida y la pérdida del aplazamiento en favor de la parte deudora.

Segunda. Constitución de prenda.

D./Dña. [NOMBRE Y APELLIDOS] "socio deudor", con el previo consentimiento de su cónyuge por ser de carácter ganancial, constituye prenda sobre las PARTICIPACIONES SOCIALES de su propiedad descritas, en favor de D./Dña. [NOMBRE Y APELLIDOS] "acreedor" que acepta, y en garantía del cumplimiento de las obligaciones de pago fijadas en la estipulación anterior, tanto por capital como por intereses.

Manifiestan los comparecientes que, por la naturaleza de los derechos pignorados, se entienden estos puestos en posesión del acreedor por el otorgamiento de esta escritura, advirtiendo yo, el Notario, de la necesidad de inscribir la presente en el Libro-Registro de socios de la entidad para su plena eficacia.

Vencida y no pagada la obligación o los intereses asegurados, la parte acreedora podrá ejecutar la garantía mediante la enajenación de las participaciones sociales dadas en prenda por el procedimientos previsto en el art.1872 CC.

Tercera. Gastos.

Todos los gastos que origine esta escritura serán satisfechos por [NOMBRE DE LA PARTE].

OTORGAMIENTO

Hice las reservas y advertencias legales, en especial las de carácter fiscal.

Leo a los comparecientes, tras advertirles del derecho que tienen a hacerlo por sí, - al que renuncian- la presente escritura, prestan su consentimiento y firman conmigo.

AUTORIZACIÓN

De todo lo consignado en este instrumento público, extendido sobre "número" folios de papel de uso exclusivo notarial, serie y números "serie y núm. [Nº] de folios", yo, el Notario, doy fe.

Firmado: D./Dña. [NOMBRE Y APELLIDOS] Firmado: D./Dña. [NOMBRE Y APELLIDOS]

Firmado: D./Dña. [NOMBRE Y APELLIDOS]

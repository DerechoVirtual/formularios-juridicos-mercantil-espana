---
name: contrato-autorizacion-no-exclusiva-obra-artistica-mer-0720
description: "Contrato de autorización no exclusiva de obra artística por entidad de gestión. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato de autorización no exclusiva de obra artística por entidad de gestión

> Formulario **MER-0720** del plugin **Marcas, patentes y propiedad intelectual** (`formularios-marcas-patentes-y-propiedad-intelectual`) · Mercantil › Propiedad industrial e intelectual · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato de autorización no exclusiva de obra artística por entidad de gestión» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato de autorización no exclusiva de obra artística por entidad de gestión” para mi caso». También puedes invocarla directamente con `/formularios-marcas-patentes-y-propiedad-intelectual:contrato-autorizacion-no-exclusiva-obra-artistica-mer-0720`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-marcas-patentes-y-propiedad-intelectual:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Marcas, patentes y propiedad intelectual) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] TIPO DE SOCIEDAD (2 veces)
- [ ] AÑO
- [ ] DÍA
- [ ] FINALIDAD DE LA UTILIZACIÓN
- [ ] IMPORTE
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] MES
- [ ] MODALIDAD DE EXPLOTACIÓN
- [ ] NOMBRE DE LA OBRA
- [ ] Nº
- [ ] Nº DE SEGUNDOS

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

EXPONEN

I. Que la ENTIDAD tiene adjudicada la representación para la gestión de los derechos exclusivos de explotación sobre la obra [NOMBRE DE LA OBRA].

II. Que el USUARIO está interesado en utilizar dicha obra para [FINALIDAD DE LA UTILIZACIÓN], para lo cual solicita la preceptiva autorización no exclusiva a la ENTIDAD.

III. Que ambas partes celebran el presente contrato de autorización no exclusiva sobre la base de las siguientes

CLÁUSULAS

La ENTIDAD concede al USUARIO, bajo las condiciones que más adelante se establecen, el derecho de [MODALIDAD DE EXPLOTACIÓN]

El tiempo de duración de la grabación de la obra no podrá exceder de [Nº DE SEGUNDOS] segundos, para anunciar exclusivamente el producto o servicio mencionado en el exponendo II.

El USUARIO no podrá ejercer ningún otro derecho y modalidad de explotación distinto de los expresamente previstos en la cláusula anterior, cuya gestión será ejercitada por la ENTIDAD en su calidad de entidad de gestión colectiva mandataria de los mismos.

La cesión tiene carácter no exclusivo y queda limitada al territorio de cobertura de los respectivos medios indicados.

Los derechos autorizados abarcan la comunicación pública del spot publicitario en que se inserta la obra desde el día [FECHA] hasta el día [FECHA]

Si transcurriera el tiempo estipulado en la cláusula anterior sin que el USUARIO hubiera ejercido total o parcialmente los derechos cedidos, no le dará acción para reclamar ninguna de las cantidades satisfechas en virtud de este contrato.

La ENTIDAD hace reserva expresa del derecho moral del autor de la obra, prohibiéndose al USUARIO modificar, alterar, deformar o adaptar de cualquier forma las partes musical y literaria de la obra cuyos derechos de explotación se ceden.

Los derechos de explotación que se conceden en este contrato sobre la obra musical objeto del mismo, dejan a salvo, en todo caso, los derechos de los artistas intérpretes o ejecutantes, de los productores fonográficos y de los productores de grabaciones audiovisuales, por la utilización de sus respectivas prestaciones.

Las Partes acuerdan que las cesiones efectuadas en los anteriores apartados se realizan sin la facultad de emplear los derechos cedidos para el entrenamiento, alimentación o aprendizaje automático de ningún sistema de inteligencia artificial ni de tecnologías basadas en esta, entendiéndose por tal, a título enunciativo pero no limitativo, herramientas de generación de lenguaje natural, reconocimiento de voz, plataformas de aprendizaje automático, motores de administración de decisiones, plataformas de aprendizaje profundo, procesos de automatización robóticos, herramientas de análisis de textos y procesamiento de lenguaje natural y cualquier otra tecnología disruptiva relacionada (en adelante y en su conjunto, la "Inteligencia Artificial"). De tal manera que, el uso de los derechos cedidos por mor del presente Contrato para los enunciados usos constituirá un incumplimiento sustancial del mismo.

El USUARIO habrá de respetar el compromiso adquirido en virtud de la anterior Estipulación en los contratos, negocios y relaciones jurídicas que mantenga con terceros, sean personas físicas o jurídicas, adoptando todas las medidas necesarias a tal fin e incluyendo, si fuese necesario, previsiones escritas en los contratos que celebre con estos terceros.

Como remuneración por los derechos concedidos en este contrato, se fija la cantidad de [IMPORTE] euros, más el IVA correspondiente, por la primera autorización que entra en vigor a la firma del presente contrato. Dicha cantidad deberá hacerse efectiva por el USUARIO mediante cheque nominativo girado a nombre de la ENTIDAD y en el domicilio de la misma.

A los efectos que procedan se hace constar que la remuneración que antecede se ha establecido en un tanto alzado al amparo de la excepción prevista en el art. 46.2.c del Texto Refundido de la Ley de Propiedad Intelectual de 1996.

La presente autorización queda sometida a la condición suspensiva de que el USUARIO abone el importe de la remuneración prevista en el contrato y que se detalla en la factura núm. [Nº] que se acompaña adjunto, de modo que, en tanto no se realice dicho pago, esta autorización no tendrá ningún efecto y el USUARIO deberá abstenerse de reproducir y distribuir la obra en la forma expresada en este documento.

Los derechos concedidos en este contrato serán en todo caso intransmisibles a terceros.

A estos efectos, como quiera que el USUARIO se haya constituido en [TIPO DE SOCIEDAD], no se considerará que existe transmisión cuando los actuales titulares de las [ELEGIR: acciones / participaciones] de la entidad cesionaria de este contrato transmitan la totalidad de las [ELEGIR: acciones / participaciones] a uno o varios terceros por cualquier medio reconocido en Derecho. Tampoco se entenderá producida la transmisión de la empresa si el USUARIO decide transformarse en [TIPO DE SOCIEDAD] o en cualquier otra entidad con personalidad jurídica reconocida por el Derecho.

El presente contrato podrá ser resuelto a instancia de la ENTIDAD por el incumplimiento por parte del USUARIO de cualquiera de las obligaciones establecidas en el mismo, bastando para ello la notificación por escrito a su domicilio, haciendo suyas la ENTIDAD cuantas cantidades hubiera percibido del productor en concepto de indemnización de daños y perjuicios, dejando a salvo posibles reclamaciones de indemnizaciones mayores.

Los impuestos de toda índole que se deriven del presente contrato serán de cuenta exclusiva del USUARIO.

Para cuantas cuestiones puedan suscitarse en relación con el presente contrato, ambas partes se someten a la jurisdicción y competencia de los Tribunales de [LOCALIDAD], con renuncia expresa a cualquier otro fuero que pudiera corresponderles.

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

Y en prueba de conformidad con cuanto antecede, firman el presente contrato por duplicado en el lugar y fecha anteriormente indicados.

ENTIDAD DE GESTIÓN	USUARIO

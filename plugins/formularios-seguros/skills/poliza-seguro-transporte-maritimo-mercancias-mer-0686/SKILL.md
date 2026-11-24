---
name: poliza-seguro-transporte-maritimo-mercancias-mer-0686
description: "Póliza de seguro de transporte marítimo de mercancías. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Póliza de seguro de transporte marítimo de mercancías

> Formulario **MER-0686** del plugin **Seguros: pólizas, coberturas y reclamaciones** (`formularios-seguros`) · Mercantil › Seguros · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Póliza de seguro de transporte marítimo de mercancías» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Póliza de seguro de transporte marítimo de mercancías” para mi caso». También puedes invocarla directamente con `/formularios-seguros:poliza-seguro-transporte-maritimo-mercancias-mer-0686`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguros:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguros: pólizas, coberturas y reclamaciones) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (4 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] ASEGURADORA
- [ ] AÑO
- [ ] BANDERA
- [ ] CABALLOS DE POTENCIA
- [ ] CLASIFICACIÓN DEL BUQUE
- [ ] DÍA
- [ ] FECHA
- [ ] FOLIO
- [ ] MES
- [ ] NOMBRE DEL BUQUE
- [ ] PAÍS
- [ ] PIES CÚBICOS DE CAPACIDAD
- [ ] PLAZO
- [ ] TOMO
- [ ] TONELADAS DE PESO MUERTO
- [ ] TONELADAS DE REGISTRO
- [ ] VELOCIDAD EN NUDOS

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

En [LOCALIDAD], a [DÍA] de [MES], de [AÑO]

REUNIDOS

De una parte, la Compañía de Seguros [ASEGURADORA] con domicilio en [LOCALIDAD] e inscrita en el Registro mercantil con el número [NÚMERO]. Se halla representada por D./Dª [NOMBRE Y APELLIDOS], Consejero/a Delegado de la entidad, según poderes recogidos en escritura pública otorgada ante notario D./Dª. [NOMBRE Y APELLIDOS]. En adelante el ASEGURADOR.

MANIFESTAN

1.- El asegurado ostenta la propiedad de un buque de nombre [NOMBRE DEL BUQUE], bajo bandera [BANDERA] clasificado como [CLASIFICACIÓN DEL BUQUE] y de [TONELADAS DE REGISTRO] toneladas de Registro, con [CABALLOS DE POTENCIA] caballos de potencia, capaz de transportar [TONELADAS DE PESO MUERTO] toneladas de peso muerto, con [PIES CÚBICOS DE CAPACIDAD] pies cúbicos de capacidad y navegar a plena carga a la velocidad de [VELOCIDAD EN NUDOS] nudos en condiciones normales. Está inscrito en el Registro de buques al Tomo [TOMO], folio [FOLIO], número [NÚMERO].

2.- El asegurado necesita garantizar el riesgo derivado de la navegación y las responsabilidades que de él se derivan en el transporte de mercancías. En consecuencia, reconociéndose ambas partes capacidad bastante para el acto que celebran, deciden libremente concertar un contrato de seguro marítimo de transporte de mercancías sobre el bu- que descrito, con sujeción a las siguientes

ESTIPULACIONES

1.- Es objeto de este contrato la articulación de las condiciones de seguro de daños a las mercancías que transporte el buque anteriormente descrito, bien conjuntamente para un solo cargador, bien mediante cargas separadas de distintos cargadores.

2.- El asegurador toma a su cargo los daños a mercaderías que se produzcan por riesgos de mar, puerto, bahía, rada, ensenada, varadero, y consistan en los siguientes accidentes: abandono, pérdida total, contribución a la avería común, gastos de salvamento por naufragio, abordaje, varada embarrancada arribadas y escalas forzosas, explosiones de máquinas, roturas de los elementos de dirección, y demás riesgos de mar.

Quedan también comprendidos los perjuicios por retrasos en el viaje y consiguiente entrega retardada de mercaderías que no se deban a las anteriormente descritas en las que ya queda incluido, o fuerza mayor ajena a cualquier de las partes en la contratación, incluido el cargador

3.- El asegurador no responde de los riesgos producidos por guerras, movimientos revolucionarios, motines, huelgas, embargos gubernativos, retención por orden de potencia extranjera, saqueo, apresamiento, represalias,

cierre de puertos, ni de las consecuencias que de estos riesgos se derivan. Tampoco responde de los daños producidos por dolo o negligencia grave del asegurado, cargadores y consignatarios o mandatarios en tierra, por contrabando, comercio clandestino o prohibido y violaciones de bloqueo.

4.- La cobertura se iniciará a partir del día [FECHA] y tendrá una duración de [PLAZO], salvo que al término del plazo el buque se encontrara navegando, en cuyo caso se prorrogará hasta el tiempo de arribada a puerto, anclaje, amarraje, y todas las incidencias hasta su completa paralización y descarga, percibiendo la prima estipulada en proporción a los días que se gasten en la terminación de las operaciones.

5.- La prima se compone de una cantidad fija mensual, a cuenta de las operaciones de seguro de cada cargamento por separado, que se cifra en el [PORCENTAJE] % de la media de las efectuadas en el año anterior y otra que depende de la valoración de los cargamentos singularizados.

7.- Las mercancías transportadas que se aseguran serán objeto de una declaración por parte del asegurado, con base a los datos aportados por el cargador, con motivo de cada operación de transporte que realice, a cuyo fin se proveerá a la oportuna valoración por las partes contratantes del seguro, partiendo del precio de venta en factura y en otro caso, el precio medio que tuviere en el mercado del punto de embarque. Al propio tiempo y en función de su valor y de los riesgos que se corran, se determinará la prima del seguro por el transporte de las mercancías, que figurara por separado junto con cada declaración y se abonaran en su conjunto semestralmente, deducido el [PORCENTAJE] % hasta entonces abonado.

8.- El contrato será resuelto y las cantidades abonadas quedaran a favor del asegurador:

• si se demuestra una valoración inexacta de la mercancía

• falta de declaración del cargador de transportar mercancías peligrosas que exigen ciertas medidas de seguridad en su transporte.

• falta de aviso al asegurador de la existencia de cargas, embargos y otras contingencias que determinan un retraso del viaje.

• transmisión del buque a otro naviero sin comunicación anticipada al asegurador

9.- El contrato quedará extinguido por el transcurso del plazo de vigencia o las prórrogas, en su caso y en caso de siniestro del buque que ocasiones su pérdida total o parcial, con devolución de las primas a cuenta que correspondan a partir de ese momento y las que correspondan en concreto al cargamento, si no se hallaran comprendidas en la indemnización propia del seguro del buque.

10.- Todos los impuestos, tasas, arbitrios, corretajes y cuantos se originen por la formalización, tramitación, cumplimiento y extinción de este contrato serán a cargo de la parte que interviniere según la ley.

11.- Cualquier litigio, discrepancia entorno al cumplimiento e interpretación de este contrato, o que esté directa e indirectamente relacionado con él, se someterá a arbitraje, con renuncia expresa de las partes al fuero propio que haya de corresponderles y en el marco de la Cámara de Comercio de [LOCALIDAD], a la que se encomienda su gestión, administración, y designación de árbitros de conformidad a su reglamento y estatutos. En lo que por normas imperativas no pueda ser sometido a arbitraje, las parte, con renuncia al fuero propio que pueda corresponderles, se someten a la jurisdicción de los Tribunales de [LOCALIDAD].

12.- Para cuantas dudas no puedan ser resueltas con el presente con- trato, las partes se someten expresamente a la legislación del país [PAÍS], sin perjuicio de las normas imperativas y de orden público que resulten de aplicación por Derecho Internacional Privado

En el caso de que el cumplimiento de este Contrato suponga la necesidad de acceder a datos de carácter personal, como encargados del tratamiento, quedamos obligados al cumplimiento de la LO 3/2018, de 5 diciembre, de Protección de Datos Personales y Garantía de los Derechos Digitales y del Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016 (RGPD) y demás normativa aplicable.

De conformidad con lo anterior, firman ambas partes contratantes el presente contrato en el lugar y fecha arriba indicados.

El ASEGURADOR

El ASEGURADO

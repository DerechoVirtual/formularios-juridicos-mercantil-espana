---
name: acuerdo-administracion-concursal-resolver-leasing-sin-mer-0792
description: "Acuerdo con la administración concursal para resolver un leasing sin indemnización ni deuda nueva. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Acuerdo con la administración concursal para resolver un leasing sin indemnización ni deuda nueva

> Formulario **MER-0792** del plugin **Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso** (`formularios-pleitos-mercantiles-y-concurso`) · Mercantil › Litigios mercantiles, competencia desleal y concurso · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Acuerdo con la administración concursal para resolver un leasing sin indemnización ni deuda nueva» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Acuerdo con la administración concursal para resolver un leasing sin indemnización ni deuda nueva” para mi caso». También puedes invocarla directamente con `/formularios-pleitos-mercantiles-y-concurso:acuerdo-administracion-concursal-resolver-leasing-sin-mer-0792`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-pleitos-mercantiles-y-concurso:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Pleitos mercantiles: acuerdos sociales, administradores, competencia desleal y concurso) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] MARCA/MODELO (14 veces)
- [ ] NOMBRE DE LA PARTE (6 veces)
- [ ] NÚMERO (5 veces)
- [ ] DNI/NIE (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] DÍA (3 veces)
- [ ] FECHA (3 veces)
- [ ] LUGAR (3 veces)
- [ ] MES (3 veces)
- [ ] SEDE (3 veces)
- [ ] AÑO (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MATRÍCULA (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE SERIE (2 veces)
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO
- [ ] MES FINAL
- [ ] MES INICIAL
- [ ] Nº DE ANEXO

## Normas que cita el formulario

- art. 165 Real Decreto Legislativo 1/2020

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

- Junto a «…e la Sección de lo Mercantil del Tribunal de Instancia de [SEDE], plaza n.º [Nº]»: El Tribunal de Instancia es único por partido judicial (art. 84.1 LOPJ); lo que se numera es la plaza dentro de la Sección (DT 1.ª LO 1/2025). En escritos iniciales (demanda, solicitud, petición monitoria) no se indica plaza: «…DEL TRIBUNAL DE INSTANCIA DE [partido]», para reparto. Fuente: LOPJ art. 84.1-2 (redacc. LO 1/2025, BOE-A-2025-76; consolidado BOE-A-1985-12666) y LO 1/2025 DT 1.ª (plazas con la numeración del juzgado de procedencia).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) El presente acuerdo de resolución del contrato de leasing debe ser presentado por la administración concursal ante la plaza de la Sección de lo Mercantil del Tribunal de Instancia, siguiendo los trámites del art. 165.2 TRLConc, de modo que el Letrado de la Administración de Justicia citará a comparecencia ante la Sección de lo Mercantil del Tribunal de Instancia al concursado, a la administración concursal y a la otra parte en el contrato y, al existir acuerdo en cuanto a la resolución y sus efectos, la plaza de la Sección de lo Mercantil del Tribunal de Instancia dictará auto declarando resuelto el contrato de conformidad con lo acordado.


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

Acuerdo entre la empresa de leasing y la administración concursal para resolución de contrato de leasing posterior a la declaración del concurso, con condonación de crédito contra la masa por cuotas posteriores a dicha declaración concursal

En [LUGAR], a [FECHA].

REUNIDOS

De una parte,

[NOMBRE Y APELLIDOS], con domicilio social en [LOCALIDAD], nº [Nº], con C.I.F. nº [NÚMERO], y en su nombre el apoderado D./Dña [NOMBRE Y APELLIDOS], con D.N.I. nº [DNI/NIE]

D./Dña [NOMBRE Y APELLIDOS] con DNI [DNI/NIE], con domicilio a los presentes efectos en [DOMICILIO] - [LOCALIDAD], actuando en calidad de Administrador social de la mercantil

Y de otra,

D./Dña [NOMBRE Y APELLIDOS], con DNI. [DNI/NIE], quien integra la ADMINISTRACIÓN CONCURSAL designada en el Procedimiento de Concurso Voluntario / seguido ante la plaza de la Sección de lo Mercantil del Tribunal de Instancia de [SEDE], plaza n.º [Nº] , según consta en los autos del referido procedimiento, en el cual se declaró a dicha mercantil intervenida en sus facultades de administración y disposición.

Todas las partes intervinientes, en su respectivo carácter y representación se reconocen mutuamente la capacidad y legitimación suficientes para otorgar el presente documento.

ANTECEDENTES

I.- Entre la entidad [DENOMINACIÓN SOCIAL] y la CONCURSADA se formalizaron los Contratos de Arrendamiento Financiero que a continuación se detallan:

Nº Contrato	Fecha	Meses	Descripción del bien
	/ /2017	60	VEHÍCULO:
- Marca [MARCA/MODELO], Modelo [MARCA/MODELO]
- Matrícula [MATRÍCULA]
Nº Contrato	Fecha	Meses	Descripción del bien
	/ /2017	60	VEHÍCULO:
- Marca [MARCA/MODELO], Modelo [MARCA/MODELO]
- Matrícula [MATRÍCULA]

II.- Estando vigentes los contratos anteriormente mencionados, en fecha / /, la plaza de la Sección de lo Mercantil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO] declaró en Concurso Voluntario al ARRENDATARIO, motivo por el cual, el / /, [NOMBRE DE LA PARTE] comunicó a la Administración Concursal la existencia de los créditos a su favor derivados de los contratos suscritos entre las partes.

III.- Que a la vista de que el ARRENDATARIO, a través del presente documento, manifiesta formalmente a [NOMBRE DE LA PARTE] la imposibilidad sobrevenida de hacer frente a sus obligaciones contractuales, al amparo del art. 165 del Real Decreto Legislativo 1/2020, de 5 de mayo, por el que se aprueba el texto refundido de la Ley Concursal (en adelante TRLConc), solicita la resolución de los contratos referenciados en el Antecedente I, y propone la entrega voluntaria y pacífica de los vehículos arrendados, todo ello sin perjuicio de la subsistencia del crédito existente a favor de la arrendadora.

IV.-, atendidas las razones expuestas por el ARRENDATARIO, acepta la referida resolución y ambas partes, de común acuerdo, con la intervención de la Administración Concursal reseñada, la materializan conforme a las siguientes:

ESTIPULACIONES

Primera.- y [NOMBRE DE LA PARTE] declaran resuelto, con fecha de hoy, los contratos a que se ha hecho referencia en el punto I anterior.

Segunda.- En este acto el [NOMBRE DE LA PARTE], interesando la resolución extracontractual del citado contrato de arrendamiento, hace entrega a [NOMBRE DE LA PARTE], que los recepciona, de los vehículos objeto de los contratos referenciados, en el estado y con la documentación que figura en el ANEXO [Nº DE ANEXO], de este contrato.

Tercera.- Con independencia de la resolución del contrato, y de la entrega de los vehículos, las partes acuerdan:

- La renuncia de [NOMBRE DE LA PARTE] a las rentas vencidas e impagadas con posterioridad a la fecha de la declaración de concurso, cuyo importe total asciende a [IMPORTE] euros (Vencimientos [MES INICIAL] a [MES FINAL] de [AÑO]).
- La subsistencia del crédito correspondiente a las rentas vencidas e impagadas anteriores a la declaración concursal comprendidas desde [DÍA] de [MES] a [DÍA] de [MES], cuyo importe asciende a la cantidad de [IMPORTE] euros.

Cuarta.- El ARRENDATARIO asume cualesquiera cargas y gravámenes de los que responda el bien arrendado por impuestos, sanciones administrativas u otras causas, hasta el día de la fecha.

Quinta.- Las partes se obligan y comprometen a comunicar conjunta o separadamente la plaza de la Sección de lo Mercantil del Tribunal de Instancia de [SEDE], plaza n.º [NÚMERO], Autos de Procedimiento Concursal /, el contenido de este acuerdo en orden a que por dicho Órgano Judicial se proceda a su homologación y aprobación a la mayor brevedad posible.

Sexta.- RATIFICACIÓN POR LA ADMINISTRACIÓN CONCURSAL. La Administración Concursal acepta y ratifica con su firma el íntegro contenido de lo aquí convenido, y se obliga a sostener su validez y ratificarlo allá donde fuera preciso.

Y en prueba de aceptación y conformidad con cuanto antecede y queda estipulado, firman las partes el presente documento en lugar y fecha del encabezamiento en 4 ejemplares.

En [LUGAR], a [FECHA].

Fdo.:

Fdo.:

Fdo.:

ANEXO I

Yo, con DNI nº [DNI/NIE], por la firma del presente recibí, manifiesto haber retirado los siguientes vehículos:

- EXCAVADORA SOBRE RUEDAS:
Marca [MARCA/MODELO], Modelo [MARCA/MODELO]
Chasis Nº [NÚMERO].
Martillo Hidráulico Marca [MARCA/MODELO], Modelo [MARCA/MODELO], Nº Serie: [Nº DE SERIE].
- EXCAVADORA SOBRE ORUGAS:
Marca [MARCA/MODELO], Modelo [MARCA/MODELO]
Chasis Nº [NÚMERO].
Martillo Hidráulico Marca [MARCA/MODELO], Modelo [MARCA/MODELO], Nº Serie: [Nº DE SERIE].
- ANGLEDOZER sobre Orugas.
Marca [MARCA/MODELO], Modelo [MARCA/MODELO].
Bastidor:

Del mismo modo, doy fe de que los mismos se encuentran en aparente perfecto estado (o con los siguientes defectos que a continuación relaciono).

Así mismo manifiesto haber recibido la siguiente documentación de dichos vehículos (permiso de circulación, ficha técnica, I.V.T.M de fecha [FECHA] pagado, etc...).

En [LUGAR], a [DÍA] de [MES] de [AÑO].

Fdo.:
